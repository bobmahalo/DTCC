---
title: "GSD IM Member Specs for Comparison Input & Output"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd200_gsd_im_member_specs_comparison_io_2023.pdf"
pages: 303
size: "2578.8 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD IM Member Specs for Comparison Input & Output

**Original File:** [gsd200_gsd_im_member_specs_comparison_io_2023.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd200_gsd_im_member_specs_comparison_io_2023.pdf)  
**Category:** GSD  
**Total Pages:** 303  
**File Size:** 2578.8 KB  

---

## Page 1

 
 
 
[[FICC]] – [[GSD]] 
[[GSD]] INTERACTIVE MESSAGING (IM) [[Member]] SPECIFICATIONS FOR 
COMPARISON INPUT & OUTPUT 
VERSION 4.1 
MARCH 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in wh ich such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: March 2023 
Publication Code:  GSD200 
Service: [[FICC]] – [[GSD]]   
Title: [[GSD]] Interactive Messaging (IM) [[Member]]  Specifications fo r Comparison Input & Output 
 
 
The [[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output (hereinafter, the " document ") is 
provided as a convenience to [[Member]] s and is for information purposes only. Although [[FICC]] may make this document  
available to Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have a 
continuing obligation to make available this document  or other related information of a certain ty pe.  
 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose 
of any information provided to M embers in this document , which is provided as -is. [[FICC]] shall not be liable for any 
loss related to such in formation (or the act or process of providing such information) resulting directly or 
indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable f or: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
 
Further, the information contained in this document is subject to change. Members  and other authorized users of the 
document  will find the most current version of the document on [[DTCC]]’s Learning Center  site, 
www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow  
[[FICC]]’s most current document . 
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Overview ......................................................................................................................................... 6  
Introduction..................................................................................................................................... 7  
Comparison Interactive Message Overview ....................................................................................... 8  
Message Overview ......................................................................................................................... 8  
Message Formatting Structure......................................................................................................... 8  
Formatting Structure Overview ....................................................................................................... 8  
Mess ag e Head er ......................................................................................................................... 9  
Bloc ks and  Sub-blocks.................................................................................................................. 9  
Data Fields ............................................................................................................................... 10 
Mess ag e Fo rmatting Rules ........................................................................................................... 11 
Mess ag e Rules.......................................................................................................................... 11 
Mess ag e Field  Rules .................................................................................................................. 11 
Fo rmatting Conventions .............................................................................................................. 12 
Communications Overview............................................................................................................. 14 
Mess ag e Exc hang e ..................................................................................................................... 14 
Comparison Interactive Message Specifications – MT515 ..................................................................15  
MT515 Trade Input Message Description ......................................................................................... 15 
MT515 Inp ut Mes sag e Sp ec ific atio ns............................................................................................... 17 
MT515 General Format ................................................................................................................ 17 
MT515 Field Sp ec ific atio ns ........................................................................................................... 22 
MT515 Ins truct Mes s ag e Mapp ing ................................................................................................. 30 
Comparison Interactive Message Specifications – MT509 ..................................................................41  
MT509 Trade Status Message Description ....................................................................................... 41 
MT509 Trade Status Message Specifications.................................................................................... 44 
MT509 General Format ................................................................................................................ 44  
MT509 Field Specifications ........................................................................................................... 48 
MT509 Field Analysis ................................................................................................................... 53 
Comparison Interactive Message Specifications – MT518 ..................................................................63  

---

## Page 4

 
 
MT518 Contra-Side Me ssa ge De scription......................................................................................... 63 
MT518 Contra-Sid e Mess ag e Sp ec ificatio ns ..................................................................................... 65 
MT518 General Format ................................................................................................................ 65 
MT518 Field Specifications ........................................................................................................... 71 
MT518 Field Analysis ................................................................................................................... 80 
Comparison Interactive Message Specifications – MT599 ................................................................ 100 
MT599 Message Description .........................................................................................................100  
MT599 Message Specifications .....................................................................................................101  
MT599 General Format ...............................................................................................................102  
MT599 Field Specifications ..........................................................................................................104  
Appendices .................................................................................................................................. 106 
List of Appendices .......................................................................................................................106  
Appendix A – Mandatory Data ......................................................................................................107  
Mand ato ry  D ata fo r Buy/Sell (Cas h) Trans actio ns ..........................................................................107  
Mand ato ry  D ata fo r Repo  Trans actio ns ........................................................................................107  
Appendix B – Mes s ag e Flo ws ......................................................................................................108  
Bilateral Comparison Trade Flows ...............................................................................................112  
D emand  Trad e Flo ws ................................................................................................................136  
Locked-in Trade Flows...............................................................................................................157  
Appendix C – Mess ag e Samp les ..................................................................................................177  
Sample # C1 – Bilateral Next-D ay Settling  Trad e Rejected ..............................................................178  
Sample # C2 – Bilateral Same-Day Starting Transaction Compared .................................................181  
Sample # C3 – Bilateral Next-Day Starting Transaction Canceled Post-Comparison ...........................198  
Sample # C4 – D emand  Nex t-Day Starting Transaction DK’d, Modified and Compared .......................228  
Sample # C5 – Repo  Substitutio n Proc ess ed  o n D emand Trad e ......................................................259  
Sample # C6 – Various MT599 Administrative Messages ................................................................283  
Appendix D – Mess ag e Structure D iag rams....................................................................................287  
Mess ag e Struc ture D iag rams – MT515 ........................................................................................287  
Mess ag e Struc ture D iag rams – MT509 ........................................................................................288  
Mess ag e Struc ture D iag rams – MT518 ........................................................................................289  

---

## Page 5

 
 
Appendix E – Reaso n Cod e Tab les ...............................................................................................290  
Reject Message Reason Codes ..................................................................................................290  
DK Message Reason Codes.......................................................................................................292  
Other Message Reason Codes ...................................................................................................293  
Appendix F – Detailed Field Analysis Res ults – Comp ariso n Mess ag es ..............................................294  
 

---

## Page 6

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Overview 6 
OVERVIEW 
Interactive Messaging for Real-Time Comparison  
This document provides Members of the Fixed Income Clearing Corporation‘s (“[[FICC]]”) Government [[securities]] 
Division (“[[GSD]]”) with interactive messaging input and output specifications for real-time trade comparison 
messages used to support [[GSD]]’s products and services.  
Audience 
This document was written for systems and development personnel including managers, analysts and 
programmers of [[GSD]] [[Member]] firms. It presumes readers are familiar with technical concepts and terms as 
well as having a [[BASIC]] understanding of [[GSD]]'s products and services. 
Related Materials 
The specifications for interactive messages supporting trade comparison are based on SWIFT messages. 
Users of this document are therefore strongly urged to refer to SWIFT user documentation to obtain a complete 
and comprehensive understanding of these message standards. SWIFT information (including message 
formats) can be found at www.iso15022.org. The specifications of interactive messaging for [[GSD]]’s netting 
output used to support [[GSD]] products and services can be found in the latest version of the “[[GSD]] Interactive 
Messaging (IM) [[Member]] Specifications for Netting Output” document. 
Additional inquiries regarding Real-time Comparison services may be directed to your [[FICC]] Relationship 
Manager. 
Communication 
For information on [[FICC]] Connectivity, please contact [[FICC]] Integration at ficcintegration@[[DTCC]].com. 
  

---

## Page 7

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Introduction 7 
INTRODUCTION 
This document provides the real-time comparison specifications for Interactive Messaging related to the 
support of [[GSD]]’s products and services, enabling [[GSD]] Members to receive trade status messages on an 
interactive/intra-day basis using standardized SWIFT formats.  
Members have the ability to submit trade input to [[GSD]] intra-day, as trades are executed, using the SWIFT 
MT515 message format. Submitters can immediately receive trade status information (e.g. notification of 
whether the trade has been accepted or rejected) via the SWIFT MT509 message format. This format is also 
used to provide up-to-the-minute trade status information to Members as transactions are processed by [[GSD]] 
(for example, a message is sent when a trade compares, is canceled or is modified). 
Trade counterparties can also be notified immediately via a SWIFT MT518 message when a trade has been 
submitted against them. The SWIFT MT518 message contains full trade details and is similar to the MT515. It 
is also used to communicate to the [[Member]] those changes that [[GSD]] may have made to trade records that 
were previously submitted. 
Messages discussed in this document will give Members the ability to take in important trade status information 
on a real-time basis. 
It should be noted that this document is a technical specification and is not, in any way, intended to 
communicate legal definitions as to when trades are guaranteed or novated by [[GSD]]. Members should refer to 
the [[FICC]] [[GSD]] Rulebook for such information. 
For additional service details, please refer to the Clearing Services > Fixed Income – [[GSD]] section available at 
www.[[DTCC]].com
. 
Note: 
[[GSD]] utilizes SWIFT standardized messages, but it does not utilize the SWIFT network. [[GSD]] currently utilizes its 
proprietary network for communication between [[GSD]] and its Members. The SWIFT outbound and inbound messaging 
format [[GSD]] employs is meant to be compliant with SWIFT standards  so that the SWIFT network could be used in the 
future. [[GSD]] utilizes the flexible ISO 15022 message formats for its outbound and inbound real -time messaging. Such 
flexibility allows [[GSD]] to deploy new coding for these formats as new functionalities or services are added.  

---

## Page 8

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Ov erview 8 
COMPARISON INTERACTIVE MESSAGE OVERVIEW 
Message Overview 
The Interactive Messaging (supporting trade input and trade status output) that is outlined in this document are 
message types: 
• MT515 – The MT515 (Trade Input) message is used by [[GSD]] Members to submit trades to [[GSD]], enter 
trade cancellations, modify [[Member]] reference numbers on previously submitted trades and to submit DK 
notifications on trades, as applicable, submitted against them.  
o [[GSD]] uses three styles of this message: 
» DVP – This format is used by Members using the DVP system 
» GCF – This format is used by Members using the GCF system 
» CCIT – This format is used by CCIT Members using the GCF system  
• MT509 – The MT509 Trade Status Message is used by [[GSD]] to communicate the status of each input 
(submission, modification, cancellation or DK) message that has been submitted to [[GSD]] for processing by 
a [[GSD]] [[Member]] or a [[GSD]] [[Member]]’s service bureau.  
• MT518 – The MT518 Message is used by [[GSD]] to communicate to [[GSD]] Members that a trade input 
(submission, modification, cancellation or DK) message has been submitted for a transaction for which  
they are a party to. 
• MT599 – The MT599 Message is used by [[GSD]] to communicate to [[GSD]] Members system administrative 
information such as system availability and major system events to Members. 
 
The upcoming sections will contain message formatting information and the detailed specifications for the 
MT515, MT509, MT518 and MT599 Messages. 
Message Formatting Structure 
This document presents specifications for the SWIFT Message Types mentioned above. Three of the message 
types (MT515, MT509 and MT518) utilize ISO 15022 Formats. The fourth message type (MT599) is a Free 
Format Message. A [[BASIC]] overview of the ISO 15022 Message Structure can be found below. 
Formatting Structure Overview 
This section of the document provides some background information that may be useful for interpreting the 
detailed message specifications that follow. Much of the information that appears in this section of the 
document has been derived from the “SWIFT Standards Category 5 [[securities]] Market Message Usage 
Guidelines - September, 2000 Edition.” 
ISO 15022 SWIFT message formats are constructed using a modular methodology based on the premise that 
information can be identified and programmed once, then reused wherever needed. Using this approach, data 
is configured into logical groups (e.g., generic fields and blocks) according to business purpose. These groups 
are then uniquely identified (using tags, qualifiers and start/end of block designators) so that they can be used 

---

## Page 9

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Ov erview 9 
whenever needed to fulfill particular business purposes across a number of messages without requiring 
extensive reprogramming. 
If the [[BASIC]] message structure were diagramed from the top down (going from the more general to the more 
specific), you would have a Message Header followed by one or more information blocks (potentially containing 
sub-blocks), composed of one or more fields. Each of these components is defined below. 
Note: 
While [[GSD]] has elected to use SWIFT standardized messages, it is not utiliz ing  the SWIFT network. [[GSD]] utilizes its 
proprietary network for communication between [[GSD]] and its members. The messages are intended, however, to be 
compliant with SWIFT standards . 
Message Header 
The message header specifies the sending and receiving parties of the message and provides the message 
type. The message header is the first component of every message and are in a fixed format. The header is 
populated as a continuous string of data (complying with the requirement specifying the allowable characters 
for a given line in a message) and terminates as a regular data field (with a carriage return line feed “CRLF”). 
Within the header is a “Password” field, which is a unique identifier provided by [[GSD]] for each [[Member]] to input 
on their MT515 messages sent to [[GSD]]. For all [[GSD]] outbound comparison messages (MT509, MT518 and 
MT599), the password field will be blank-filled. 
Message Header Format 
The Message Type Field contained in the message header defines the purpose of the message. As Indicated 
previously, this message header will be utilized on all [[GSD]] comparison interactive messages: MT515, MT509, 
MT518 and MT599.  
M/O Tag Block/Qualifier Sub-qualifier/Options Field Description Data Format  
    Message Header  
M    Password  12!c 
M    Sender  8!c 
M    Message Type 3!n/3!n/4!c  
M    Receiver  8!c 
 
Blocks/Qualifiers 
A block or qualifier may be defined as a group of fields containing related business information that is framed 
by Start of Block and End of Block designators. The use of a block is not restricted to any given message. It 
can be reused across a number of messages and combined with other blocks to fulfill a variety of business 
purposes. For example, the General Information (GENL) block found in the MT515, MT509 and MT518 
messages in this document, contain general information regarding the trade, such as trade reference numbers. 
The Confirmation Details (CONFDET) block found in the MT515 and MT518, contains specific trade 

---

## Page 10

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Ov erview 10 
information such as trade date, [[settlement]] date, price, security and information regarding the confirming 
parties. 
Each message contains one or more blocks. A typical message contains a General Information (GENL) block, 
followed by a series of detail blocks. These blocks may be mandatory or optional within a particular message, 
and are structured as follows: 
• A Start of Block designator (represented by the tag 16R), indicating the start of a group of related 
information 
• One or more sub-qualifiers and/or fields 
• An End of Block designator (represented by the tag 16S), indicating the end of a group of related 
information. 
Data Fields 
There are two types of ISO15022 data fields: generic fields and discrete fields. A  generic field is used to 
express the data of a family or business class of data items of the same nature, for example, dates, amounts.  
Note: A generic data field tag uses a qualifier to specify the precise meaning of each business element of the 
business class. A discrete field is used to express a specific single business data item. Note: A discrete data 
field tag does not need a qualifier to further define the meaning of the data.  
At a minimum, each field is composed of an identifying tag and its associated field data. For example, 98A is 
the generic tag used to indicate a date/time field in a particular format (YYYYMMDD).
1 The format for a tag 
includes two delimiters – one to indicate the start of the tag, and a second to indicate the end of the tag. These 
delimiters are indicated using a colon. Continuing with 98A tag as an example, the proper format for the 
generic tag used to indicate a date in the YYYYMMDD format would be “:98A:”. 
Because there are a number of different types of dates that may be associated with any given trade, the 
generic field tag must be further described if it is to be useful. Qualifiers are used to provide this additional level 
of description. For example, the tag 98A followed by the qualifier SETT means that the corresponding field data 
is the [[settlement]] date (Start Leg [[settlement]] Date if the record is for a Repo Transaction) for the trade. The tag 
98A followed by the qualifier TRAD means the corresponding field data is the trade date and time for the trade. 
Qualifiers for generic tags are always preceded by an additional colon “:”. 
The generic field for a [[settlement]] date of September 28, 2020 in the YYYYMMDD format, including the generic 
tag, the qualifier and the field data would be “:98A::SETT//20200928”. Tags that are part of a block must 
remain within the “start” and “end” block tags. 
  
 
1 The alpha character in the tag is used to indicate which format [[Option]] has been applied. If the alpha character in the tag is  lowercase in 
the SWIFT format documentation, this means that there are several format options for the field and that there is free choice to use any of 
these options. If the alpha character in the tag is uppercase, this means that, while there are several format options for the field, the [[Option]] 
designated by the uppercase alpha character must be used. G SD has mandated the options that Members must use in the layouts. 

---

## Page 11

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Ov erview 11 
Message Formatting Rules 
The following Message and Message Field rules apply to all interactive messages used to support [[GSD]]’s 
products and services: 
Message Rules 
Message Rules 
1 Direction  Messages are sent either to or from [[GSD]]  
2 Variable Length  All messages can vary in length up to a maximum allowable number of characters 
per message type 
3 Header All messages begin with a standard fixed length header  
4 Terminator  All messages end with a standard terminator sequence reflected by a Carriage 
Return/Line Feed (“CRLF”) and a Dash (“–”) 
5 Message Type Each message belongs to a specified message type 
6 Message Fields  A message is composed of one or more message fields  
7 Character Set A-Z, a-z, 0-9, white space and the following punctuation “:/, -” 
Message Field Rules 
Message Field Rules 
1 Field Tag  Each field begins with a field tag  
2 Tag Format  Each tag is composed of 2 digits and an optional character (2!c[1a])  
3 Tag Delimiter  Each tag is prefixed and suffixed by the character “:” (e.g., :23G:)  
4 Field Data Field data (including qualifiers and sub- qualifiers) immediately follows the tag suffix 
delimiter. Generic tags are prefixed by an additional “:”  
5 Data Format  Data conforms to format rules for a specified tag  
6 Data Elements  Field data may be divided into multiple elements or sub field s 
7 Qualifiers  Qualifiers within a data field provide additional format definition. If a qualifier is used, 
it must appear immediately after the tag suffix delimiter (e.g., :98A::SETT). If further 
data is required after the qualifier, and the data complies with SWIFT standards, the 
qualifier is delimited by the characters “//” and the data follows (e.g., 
:98A::SETT//20200928 or :20C::MAST// 202000928815). If the data is [[GSD]] specific, 
then the [[GSD]] [[issuer]] code is included (e.g., :95R::BUYR/GSCC/PART88T2).  
8 Field Delimiter  The field delimiter sequence is Carriage Return Line Feed , “CRLF”  ( “CR” is 
represented by ASCII Character 13 and “LF” is represented by ASCII Character 10). 
This sequence immediately follows the data. The combination of Carriage Return 
Line Feed, Colon (“CRLF:”) indicates the end of one field and the beginning of the 
next. 
  

---

## Page 12

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Ov erview 12 
Formatting Conventions 
All the layouts for each of the messages included in this document are organized using the following columns 
of data:  
Column Heading  Description 
M/O The M/O column defines whether the field is always Mandatory or is Optional in the particular 
message according to SWIFT standards. This column does not provide information as to whethe r 
the field is required or optional for [[FICC]] [[GSD]]. Refer to the Appendix  A, which provides a list of 
required fields for both REPO and CASH trades.  
Tag The Tag column defines the exact tag value that must precede the field. Tags are always 
delimited by “:” (meaning a “:” would be the character immediately before and after the tag (e.g., 
“:98A:” indicates a date with a format of YYYYMMDD will follow).  
Block/Qualifier  The Block or Qualifier column specifies the Block Name in the case of a start of block (16R) or 
end of block (16S) tag. Otherwise, it specifies the required quali fier for the tag (e.g., :98A::SETT 
indicates a [[settlement]] Date field).  
Sub-qualifier/Options  The Options column specifies the different options available for individual qualifiers for a tag. 
Each tag, qualifier and [[Option]] combination uniquely specifies a data element (e.g., 
90A::DEAL//YIEL/ indicates a trade price will follow with a “yield” price type).  
Field Description  The Field Description column provides a text description of the purpose or use of a data field.  
Data Field Format The Data Field Format column specifies the size and characters allowed within a data field, as 
specified by SWIFT. The Field Specifications that follow each layout indicate how each field 
should be populated for [[GSD]] input/output. The format provided in this column reflects the  data 
that the [[Member]] must populate the field with (e.g., :98A::SETT// has a format of YYYYMMDD). 
 
It should be reiterated that the Mandatory/Optional (M/O) Field on the layout indicates if the field is SWIFT 
mandatory or optional for the message/sequence. It does not denote, however, if the field is required for 
submission to [[GSD]]. Fields that are SWIFT mandatory and/or [[GSD]] mandatory must be reflected on the MT515, 
or the message (Instruct, Modify, Cancel, or DK) will be rejected. 
The Data Format field on the layouts is intended to reflect the format of the data that Members and/or [[GSD]] 
must use to populate the field. For example, the format for the [[settlement]] Date field (:98A::SETT//20200928) is 
reflected as “YYYYMMDD.” 
All fields are, by definition, variable in length with a maximum field size specified, unless a fixed length format is 
defined by inclusion of the “!”, in which case the size specified is the fixed field size. In the case where the data 
value in the fixed length field is smaller than the field size specified, the data should be left justified with trailing 
blanks. There are not only differences in data field sizes (as noted previously in this document), but field 
formats can also be different for the population of the SWIFT standard. For example, date fields on the [[GSD]] 
MT515, MT509 and MT518 SWIFT records are reflected as “YYYYMMDD” rather than the SWIFT format of 
“MMDDYYYY”, which is also used on the [[GSD]] proprietary layout. Another difference can be found in the 
commission field. On the SWIFT standard format, the commission is reflected as “amount per trade”, whereas 
on the [[GSD]] proprietary format the commission is stated as a percentage. 
In addition, all fields on the SWIFT messages are left justified, and if the field has a decimal format (d), it must 
use a decimal comma, rather than a decimal (i.e. 50.01 should be 50,01). 

---

## Page 13

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Ov erview 13 
As a supplement to the message format, a detailed description of each field format is shown in the below table. 
The table displays when a field can contain optional element, defines the fields usage and shows an example 
for  each field. The following characters may appear in the Data Field Format Column or in any discussion of 
data format and content: 
Character Meaning Example Format Example Usage 
A  Alphabetic Characters  (A through Z) (upper case 
only   
6a  ABCDEF  
C  Alphanumeric Characters (upper case only)  6c  AB12EF  
D  Decimal (decimal comma)  15d  2035,45  
E  Blank Space  1e  (1blank space)  
N  Numeric Characters (0 through 9 ) Only  8n  20200928  
X  any character of the “X” permitted set(incl. / – ? : ( ) . 
, ‘ + CRLF Space) 
20x   
/  The literal “/” as a separator  6c/2a  AB12EF/NY  
[ ]  Optional element format  [/4c]  [optional data]  
[N]  Optional “sign” (negative) format  [N]  :92A::REPO//N3,45  
!  Fixed length field  12!c  ABCDEFGHIJKL  
 
Typical Message Form  
Form Example 
<PASSWORD><SENDER><MESSAGE TYPE> <RECEIVER><cr><lf>  
:<BLOCK START TAG>:<BLOCK NAME><cr><lf>  
:<GENERIC TAG 1>::QUALIFIER//DATA FIELD 1 <cr><lf>  
:<TAG 2>:DATA FIELD 2<cr><lf> 
:<GENERIC TAG 3>::QUALIFIER//DATA FIELD 2  <cr><lf> 
:<GENERIC TAG 4>::QUALIF/[[issuer]] CODE/DATA FIELD  3<cr><lf> 
:<BLOCK START TAG>:<BLOCK NAME><cr><lf>  
:<GENERIC TAG 5>::QUALIFIER//DATA FIELD 4<cr><lf> 
:<BLOCK END TAG>:<BLOCK NAME><cr><lf> 
:<BLOCK END TAG>:<BLOCK NAME><cr><lf> 
GSADDF    88T2     515/000/GSCCG SCCTRRS 
:16R:GENL 
:20C::SEME//000315976306 
:23G:NEWM 
:98C::PREP//20180928081211 
:22F::TRTR/GSCC/CASH 
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

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Ov erview 14 
Communications Overview 
[[GSD]] employs MQ Series as a message exchange facility to support reliable submission of trade messages 
and delivery of status messages. As noted in the Introduction, currently [[GSD]] does not use the SWIFT network 
as a communications facility. [[GSD]] will, however, attempt to comply with SWIFT format standards to facilitate 
the transition to the SWIFT network, should it be deemed desirable in the future. Previou sly, [[GSD]] implemented 
the [[participant]] Access Network as a TCP/IP communications facility to support a reliable, secure connection to 
Members’ systems. These facilities are explained in further detail below. 
Message Exchange 
A message exchange facility is used by [[GSD]] to support the receipt of trade messages and delivery of status 
and advisory messages to/from [[Member]] systems. A message exchange facility requires support for the 
implementation of queues, which are typically time-ordered lists of messages (trade messages, cancellation 
messages, status messages, etc.). This allows [[Member]] and/or vendor systems, as applicable, to generate 
trade messages as trades are executed, and these trade messages are “queued” onto the “To [[GSD]]” queue. If 
the communications connection is enabled (including all the links, from the dial-up or leased line up to the 
messaging product itself), then the message is immediately sent to [[GSD]]. Otherwise, messages will 
accumulate on the queue until a connection is completely established. 
The same procedure holds true on the return side, meaning as [[GSD]] processes trades from trade acceptance 
through comparison (and eventually through netting), the status updates will be queued for delivery back to 
[[Member]] and/or vendor systems, as applicable. [[Member]] and/or vendor systems must have a connection 
enabled and a program (e.g., a process or thread) that is waiting for messages to appear on the “From [[GSD]]” 
queue in order to process [[GSD]] responses interactively. Additional details, including the full naming convention 
that will be utilized, will be distributed to Members separately. 

---

## Page 15

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 15 
COMPARISON INTERACTIVE MESSAGE SPECIFICATIONS 
– MT515 
This section contains the detailed specifications including layout and field descriptions for MT515 Messages 
supporting comparison input for [[GSD]]’s products and services. The MT515 Message is considered a Trade 
Input Message and is used by [[GSD]] Members to submit trade details to [[GSD]]. 
MT515 Trade Input Message Description 
The SWIFT MT515 is specified as a Client Confirmation of Purchase or Sale. It can also serve as a binding 
electronic contract. The MT515 message will be used by [[GSD]] Members (including a Demand Trade Source) 
and authorized Locked-in submitters to submit trades to [[GSD]], to enter trade cancellations, to modify the 
[[Member]] reference numbers on previously submitted trades, and to DK trades submitted against them.  
Field 22F PROC in the Confirmation Details (CONFDET) block will enable the [[Member]] to indicate to [[GSD]] the 
type of record being sent. Additionally, field :70E:: TPRO// can indicate the reason for the event occurring 
preceded by the mnemonic MSGR (message reason). On DK messages this field will also provide the reason 
for the DK having been submitted against the recipient’s trade (preceded by the mnemonic “DKRS” (DK 
reason)). A MT515 Message may be sent by a [[GSD]] [[Member]] or authorized Locked-in submitter for the 
following trade inputs and products as detailed below: 
• DVP: regular buy/sell, repo/revr, auction buy/sell 
• GCF: repo/revr (DK messages does not apply to this product) 
• CCIT: repo/revr (DK messages does not apply to this product) 
 
Message Type This message is used to:  DVP GCF  CCIT 
Instruct Message 
(:22F::PROC/GSCC/INST) 
submit trade details to [[GSD]] for regular buy/sell transactions  
and repurchase agreements (“repos”) executed by 
Members (including a Demand Trade Source) or approved 
Locked -in submitters. This message will support:  
1) all fields required to effect trade comparison; and  
2) certain other SWIFT and [[GSD]] mandatory and opti onal 
fields.  
   
Cancel Message 
(:22F::PROC/GSCC/CANC) 
initiate the cancellation of a previously submitted trade. A 
Cancel Message should be an exact copy of an Instruct 
Message, and as such will contain full trade details. The 
Cancel Message should contain the last version of the 
trade details as it is on the [[GSD]] system.  
Once a trade has been fully canceled, a new trade may be 
submitted using the same [[Member]] reference number as 
the original Instruct message.  Otherwise the new instruct 
will be rejected f or using the same [[Member]] external 
reference number.  
   

---

## Page 16

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 16 
Message Type This message is used to:  DVP GCF  CCIT 
• If the trade is not Locked -in and the trade has already 
been bilaterally compared , then both parties must submit a 
Cancel Message. 
• If the trade has not been bilaterally compared or it has 
been record ed and registered based on the input of a valid 
Locked -in submitter, only the original, or Locked -in 
submitter can submit a Cancel Message for the trade.  
• If the counterparty of a Locked -in trade (Locked- in 
recipient), submitted by an authorized Locked -in submitter, 
enters a Cancel Message, the Locked -in submitter will 
receive a Cancel Request.  
Modify Message 
(:22F::PROC/GSCC/MDFC) 
submit a modification to a previously entered trade. 
Currently, the only field that may be modified using this 
SWIFT message type will be the [[Member]]  Reference 
Number. 
In order to modify any other trade information via an 
MT515, the trade must be canceled and resubmitted (using 
a Cancel Message and a new Instruct Message) or submit 
your modifications via the [[GSD]] Real-Time Trade Matching 
(RTTM®) Web application. Note: On bilaterally compared 
trades, only reference Numbers can be modified via the 
[[GSD]] RTTM Web application .  
   
DK Message 
(:22F::PROC/GSCC/TDDK) 
submit a notification to [[GSD]] (and the Counterparty) that it 
does not know, or agree with, the trade submitted against it 
by the Counterparty. The DK message will reflect the entire 
details of the Compa rison Request received by the DK’ing 
party, along with a reason for the DK.  
   
 
Note:  
Members utilizing interactive input will submit data to [[GSD]] in real -time as trades/events occur, and immediate notification 
regarding the trade’s status will be generated via the MT509 Message by [[GSD]]. 
  

---

## Page 17

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 17 
MT515 Trade Input Message Specifications 
MT515 Trade Input Message General Format 
This section provides the general format for the MT515 Message. As described in the MT515 Message 
Description, the MT515 will be sent by Members or Locked-in submitters to [[GSD]] for the following trade input 
events: 
• Instruct 
• Cancel 
• Modify 
• DK 
Note: 
A list of applicable DK Reason Codes can be found in Appendix E (Reason Code Tables) of this document.    
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  DVP GCF CCIT 
    Message Header     
M       Password  12!c    
M       Sender  8!c    
M       Message Type 3!n/3!n/4!c     
M       Receiver  8!c    
M :16R: GENL   Mandatory Start of 
Block 
     
M :20C: :SEME//   Sender's Message 
Reference 
16x    
M :23G: NEWM   Function of the 
Message – New        
or 
4!c    
    CANC   Cancel lation Request      
O :98C: :PREP//   Preparation 
Date/Time 
YYYYMMDDHHMMSS    
M :22F: :TRTR/ GSCC/CASH Trade Transaction 
Type – Cash Trade 
Indicator              
or 
4!c    
M   GSCC/REPO Repo Trade Indicator             
or 
    
   GSCC/TRLK Locked -in Cash 
Trade Indicator  
or 
    

---

## Page 18

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 18 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  DVP GCF CCIT 
   GSCC/TRLR Locked -in Repo 
Trade Indicator  
or 
    
   GSCC/TRDC Demand Cash Trade 
Indicator  
or 
    
   GSCC/TRDR Demand Repo Trade 
Indicator  
    
M :16R: LINK   Mandatory Repeat 
Start of Block  
     
M :20C: :MAST//   Master ([[Member]])  
Reference Number 
16x    
M :16S: LINK   End of Block      
M :16R: LINK   Mandatory Repeat 
Start of Block 
     
O :20C: :PREV//   Previous Reference 
Number  
16x    
M :16S: LINK   End of Block      
M :16R: LINK   Mandatory Repeat 
Start of Block 
     
O :20C: :LIST//   [[GSD]] Assigned 
Reference Number 
(Receiver’s TID) 
16x    
M :16S: LINK   End of Block      
M :16R: LINK   Mandatory Repeat 
Start of Block 
     
O :20C: :BASK//   [[Broker]] Reference 
Number 
16x    
M :16S: LINK   End of Block      
M :16S: GENL   End of Block      
M :16R: CONFDET   Mandatory Start of 
Block 
     
M :98C: :TRAD//   Trade Date & Time YYYYMMDDHHMMSS    
M :98A: :SETT//   [[settlement]] Date (or 
Start Leg [[settlement]] 
Date if REPO)  
YYYYMMDD     
M :90A: :DEAL/ /PRCT/ Deal Price – 
Percentage        
or   
15d    

---

## Page 19

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 19 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  DVP GCF CCIT 
   /YIEL/ Yield                   
or 
[N]15d    
   /DISC/ Discount      
O :19A: :SETT/ /USD [[settlement]] Amount 
(or Start Amount if 
REPO) 
15d    
M :22H: :BUSE/ /BUYI Trade Type Indicator 
– Buy (REVR)               
or 
4!c    
      /SELL Sell (REPO)      
O :22F: :PROC/ GSCC/INST Processing Indicator  
– Instruct   
or                                  
4!c    
      GSCC/CANC Cancel               
or                           
     
      GSCC/MDFC Modify                
or 
     
      GSCC/TDDK DK      
M :22H: :PAYM/ /APMT Against Payment 
Indicator – vs. 
Payment  
4!c    
M :16R: CONFPRTY   Mandatory Repeat 
Start of Block 
     
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]] 34x    
O :20C: :PROC//   Processing 
Reference – [[Buyer]] 
(Counterparty ) X-ref 
16x    
O :70E: :DECL/ /GSCC Declaration Details 
Narrative 
(10*35x)    
      /CORR Party = [[Buyer]]’s 
Executing firm  
5c    
O :70C: :PACO/ /GSCC Party Narrative (4*35x)    
      /TDID [[Buyer]] ( Counterparty ) 
Trader [[ID]] 
20c    
M :16S: CONFPRTY   End of Block      
M :16R: CONFPRTY   Mandatory Repeat 
Start of Block 
     
M :95R: :SELL/ GSCC/PART Party = [[Seller]]  34x    

---

## Page 20

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 20 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  DVP GCF CCIT 
O :20C: :PROC//   Processing 
Reference – [[Seller]] 
(Counterparty ) X-ref 
16x    
O :70E: :DECL/ /GSCC Declaration Details 
Narrative 
(10*35x)    
      /CORR Party = [[Seller]]’s 
Executing firm  
5c    
  :70C: :PACO/ /GSCC Party Narrative (4*35x)    
      /TDID [[Seller]] (Counterparty ) 
Trader [[ID]] 
20c    
M :16S: CONFPRTY   End of Block      
M :36B: :CONF/ FAMT/ Quantity of Face 
Amount (Par)  
15d    
M :35B: /US/   Identification of 
Financial Instrument/  
Security ([[CUSIP]]) 
(4*35x)    
O :70E: TPRO/ /GSCC Trade Instruction 
Processing Narrative 
 
(10*35x)    
   /MSGR Message Reason 
(see Appendix E)  
4!c    
   /DKRS DK Reason (see 
Appendix E)  
4!c    
M :16S: CONFDET  End of Block      
M :16R: SETDET  Optional Start of 
Block  
    
M  :22F:  :SETR  /RPTO  [[settlement]] 
Transaction Indicat or  
4!c     
M :16R:  AMT   Optional Start of 
Block 
    
O  :17B:  :STAN/  /N  Standing Instruction 
Override = No  
1!a     
M  :19A:  :LOCO/  /USD  [[Broker]]’s Commission  15d     
M :16S:  AMT       End of Block     
M :16S:  SETDET   End of Block     
M :16R:  REPO   Optional Start of 
Block 
    
O :98A:  :REPU//   End Leg [[settlement]] 
Date  
YYYYMMDD     

---

## Page 21

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 21 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  DVP GCF CCIT 
O :20C:  :SECO//   Secondary 
Reference Number 
16x     
O :92A:  :REPO//   Repo Rate  [N]15d     
O 19A:  :REPA//  /USD  End Leg [[settlement]] 
Amount  
15d     
M :16S:  REPO  End of Block     
 
 
 
 
 
  

---

## Page 22

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 22 
MT515 Trade Input Message Field Specifications 
This section provides the detailed field specifications for the MT515 Message.   
Block/Tag Notes 
Message 
Header 
Each message must contain a Message Header. All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password   12!c A unique identifier will be  assigned by [[GSD]] enabling the sender to submit trades on 
behalf of specific [[Member]](s).  
Sender   8!c  [[Member]] [[ID]]  
Message Type 3!n/3!n/4!c  The first 3 characters indicate to the recipient the message type (515); the second 3 
positions reflect the version of the message interface (currently always 000). The last 
4 characters indicate the [[issuer]] code to be used in the message (GSCC ). 
Receiver 8!c “GSCCTRRS” ([[GSD]] Trade Registration and Reconciliation System) for DVP, 
“GCFCTRRS” (GCF Trade Registration and Reconciliation System) for GCF/CCIT will 
always be the recipient of the MT515 messages.  
GENL This mandatory block provides general information regarding the message. It appears only 
once in a trade contract.  
20C Sender's Message Reference  
• SEME// – This field contains the sender’s message reference number. It is mandatory and 
must contain a unique number to unambiguously identify each message sent to [[GSD]]. This 
is a communications message number, not a trade number. It is suggested that members 
use a number that includes a date followed by either a time stamp or a sequence number. 
This way uniqueness can be ensured.  
e.g., :20C::SEME//100120065614SA9 
Note: 
This field must be populated with an uppercase alphanumeric value. It cannot contain symbols or 
hyphens. 
 
23G Function of the Message  
This mandatory field identifies the function of the message. It will either be a new message (NEWM) 
for an Instruct, Modify or DK, or a cancellation (CANC) of a previous message. [[GSD]] does not suppor t 
the Replace (REPL) message via interactive messaging. Members must submit a cancel (CANC) and 
a new trade (NEWM) to replace a previously existing trade in the system. Members may choose to 
retain their original reference number on the new trade, or use a new reference number, where 
desired.  
• NEWM – will be used  for a new trade, a trade modification or DK message . 
• CANC – will be used to request the cancellation of a trade. .  
e.g., :23G:NEWM  
98C Preparation Date and Time  
• PREP// – This field contains the date and time the message sent to [[GSD]] was prepared.  
e.g., :98C::PREP//20201001113328  

---

## Page 23

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Out put 
Comparison Interactive M essage Specifications  – MT515 23 
Block/Tag Notes 
Note: 
The “C” Format for this (98) tag indicates a Date/Time Format of “YYYYMMDDHHMMSS”.  
22F Trade Transaction Type Indicator (TRTR)  
This mandatory field specifies whether the trade is cash or repo and if the trade is Bilateral, Locked -in 
or Demand.  
• TRTR/GSCC/CASH – This qualifier/[[Option]] should be used on buy/sell trades requiring two - 
sided (Bilateral) comparison.  
• TRTR/GSCC/REPO – This qualifier/[[Option]] should be used on repo trades requiring Bilateral 
comparison.  
• TRTR/GSCC/TRLK – This qualifier/[[Option]] should be used on Locked -in cash trades.  
• TRTR/GSCC/TRLR – This qualifier/[[Option]] should be used on Locked -in repo trades.  
• TRTR/GSCC/TRDC – This qualifier/[[Option]] should be used on Demand cash trades.  
• TRTR/GSCC/TRDR – This qualifier/[[Option]] should be used on Demand repo trades.  
e.g., :22F::TRTR/GSCC/TRDR  
LINK The LINK Block will be repeated for the various reference qualifiers required on a Trade 
Contract. It is intended to provide the required information to identify the trade. Each 
Reference Number must be enclosed within a Start Link Block (:16R:LINK) and End Link Block 
(:16S:LINK). Each LINK repeating subsequence is within the GENL Block. At least one LINK 
sequence is required on the MT515 Message.  
20C Reference  
The Reference Num bers provided by the [[Member]] must contain uppercase alphanumeric 
characters - and must not contain symbols or hyphens. As indicated above, each reference number 
must be enclosed in a LINK Start and End block. MT515 DK messages (submitted against 
counterpart y trades) will not contain reference numbers in this sequence but require the MAST 
qualifier to be included on the record.  
• MAST// – Master Reference Number  – This qualifier contains the [[Member]]’s Reference 
Number for the trade (External Reference Number). This field must be unique for an 
Instruct and should be populated with the primary reference number that the [[Member]] will 
use to track trades on the [[GSD]] system . It is mandatory for inbound MT515 INSTRUCT 
and DK messages. For DKs , this field should be populated with the value “NONREF”. For 
Cancels and Modifies, the [[Member]] can elect to send either the External Reference 
Number (MAST) or the [[GSD]] Reference Number (LIST).  
• PREV// – Previous Reference Number  – This qualifier is used on either Trade Modify or 
Trade Cancel MT515 records. On Modify records, it is used to modify the reference 
number and should contain the [[Member]]’s Previous External Reference Number. For 
MT515 Cancel records you are submitting (:23G:CANC and :22F::PROC/GSCC/CANC in 
the Confirmation Details (CONFDET) block), this field should be populated with the value 
“NONREF”. This field will not be used on Instruct or DK records.  
• LIST// – [[GSD]] Reference N umber – This qualifier contains [[GSD]]’s assigned reference 
number (TID) for the trade. This field can be used on Modify and Cancel record s, and 
where supplied, this will be used by [[GSD]] to identify the trade, rather than the reference 
provided in the Master R eference Number Field  (MAST). For Cancels and Modifies, the 
[[Member]] can elect to send either the External Reference Number (MAST) or the [[GSD]] 
Reference Number (LIST). This field will not be used on Instruct or DK records.  

---

## Page 24

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 24 
Block/Tag Notes 
• BASK// – [[Broker]] Reference Number – This qualifier specifies the [[Broker]] reference, 
which is required for [[Broker]] submitted trades. This field will not be used on DK records.  
e.g., :20C::MAST//PART NO12020 
Note: 
This field must be populated with an uppercase alphanumeric value. It can not contain symbols or 
hyphens, except where the reference number is assigned by [[GSD]] .  
 
CONFDET The mandatory CONFDET (Confirmation Details) block appears only once in a Trade Contract. 
It contains Trade and Confirming Party Details.  
98C Trade Date  
• TRAD// – This field is used on all messages to specify Trade Date and Trade Time. (The “C” 
format for this “ 98” tag indicates a Date/Time Format of “YYYYMMDDHHMMSS”.)  
e.g. :98C::TRAD//20191125105127  
98A [[settlement]] Date  
• SETT// – This field is used on all messages to specify the [[settlement]] Date for a cash trade, 
or the Start Leg [[settlement]] Date, in case of a repo. (The “A” Format for this tag “98” indicat e s 
a Date Format of “YYYYMMDD”.)  
e.g., :98A::SETT//20191124  
90A Deal Price  
This field is reflected on all messages. It contains the Execution Price Type and Price. Only one t ag 
“90A” is allowed per trade contract. The price is left justified, with commas removed, and a comma 
used instead of a decimal. The following price types may be specified:  
• DEAL//PRCT/ – This qualifier/[[Option]] is used for dollar prices and repo rates. Where the trade 
is a repo, however, the price portion of the field must be populated with “0,”. Repo rates will 
be populated in the REPO Block.  
• DEAL//YIEL/ – This qualifier/[[Option]] is used for Yield priced trades.  This qualifier/[[Option]] 
cannot be used on messages for r epo trades . 
• DEAL//DISC/ – This qualifier/[[Option]] is used for Discount Rates.  This qualifier/[[Option]] cannot 
be used on messages for repo trades.   
e.g., :90A::DEAL//PRCT/0  
Note: 
The [[GSD]] system supports a field size of 14d. The field should be populated with a value no larger than 
14d. 
19A [[settlement]] Amount  
• SETT// – This field is used to specify the [[settlement]] Amount for buy/sell trades and the 
Start Leg [[settlement]] Amount for Repo trades.  
 
The amount is left justified, with commas removed, and a comma used instead of a decimal. The 
amount is always preceded by the I SO 3-character Currency Code (“USD” for [[GSD]] Trades).  
For repo trades, this field must be populated with the Start  Leg [[settlement]] Amount.  

---

## Page 25

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 25 
Block/Tag Notes 
e.g., :19A::SETT//USD51000000, 
Note: 
This field can accommodate a value of 15d . Also, only 2 decimal places after the comma are 
allowed.  
 
22H Trade Type Indicator (BUSE)  
This field is required on all MT515 messages and has two allowable values for this BUSE qualifier:  
• BUSE//BUYI – This qualifier/[[Option]] indicates that the trade submitted is either a buy, in the 
case of a cash trade, or a reverse, in the case of a repo trade.  
• BUSE//SELL – This qualifier/[[Option]] indicates that the trade submitted is either a sell, in the 
case of a cash  trade, or a repo, in the case of a repo trade.  
e.g., :22H::BUSE//BUYI  
Note: 
The inclusion of a REPO block and the use of a Repo qualifier in Tag 22F (TRTR/GSCC/REPO, 
TRTR/GSCC/TRLR or TRTR/GSCC/TRDR) in the GENL block will indicate that the trade is a repo 
trade, rather than a cash trade.  
22F Processing Indicator (PROC)  
This processing indicator enables the [[Member]] to indicate to [[GSD]] the type of record/command being 
submitted on this MT515.  
The allowable values for this field are:  
• PROC/GSCC/INST – This qualifier/[[Option]] indicates that the MT515 is an INSTRUCT record.  
• PROC/GSCC/CANC – This qualifier/[[Option]] indicates that the MT515 is a CANCEL record.  
• PROC/GSCC/MDFC - –This qualifier/[[Option]] indicates that the MT515 is a MODIFY record.  
• PROC/GSCC/TDDK – This qualifier/[[Option]] indicates that the MT515 is a DK record.                          
e.g., :22F::PROC/GSCC/INST  
22H Payment Indicator (PAYM)  
This Payment Indicator field is mandatory for the MT515 message. All trades submitted to [[GSD]] must 
provide the following qualifier:  
• PAYM//APMT - This qualifier/[[Option]] indicates that the trade will settle against payment.   
e.g., :22H::PAYM//APMT  
36B Quantity of [[securities]] (CONF) 2 
• CONF//FAMT/ – This field is mandatory, and for the purposes of [[GSD]], must use the [[Option]] 
‘FAMT’, indicating face amo unt (par). The quantity of the financial instrument is left justified, 
with commas removed, and a comma used instead of a decimal.  
e.g., :36B::CONF//FAMT/50000000,  
Note: 
This field can accommodate a value of 15d.  
 
2 Tags 36B, 35B and 70E::TPRO// in the CONFDET block must be placed on the message following the confirming party subsequences.  

---

## Page 26

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 26 
Block/Tag Notes 
35B Identification of Financial Instrument/Security ([[CUSIP]]) 3 
The security/[[collateral]] involved is identified in the US by specifying the ISO country identifier (‘/US/’), 
followed by the [[CUSIP]] number.  
e.g., :35B:/US/912810SH2 
Note: 
This field will only populate a value of 9!c (alpha numeric) for the [[CUSIP]] .  
70E Trade Instruction Processing Narrative (TPRO) 3  
This field is intended to reflect transaction related information not supported by the MT515 layout. It 
will be used on all MT515 DK messages to reflect the reason for the DK.  
• TPRO//GSCC – denotes narrative trade instruction processing information related to [[GSD]].   
• /DKRS – Should be used to specify the reason for the DK. The 4 -character code can be 
found in Appendix E of this  document.                                                                                    
 e.g., :70E::TPRO//GSCC/DKRSE009  
CONFPRTY The Mandatory Confirming Party Block must be repeated for each party to a trade. Each party 
specified must be enclosed within a Start Party block (:16R:CONFPRTY) and End Party block 
(:16S:CONFPRTY). Please note that on every trade there should be at least two (one [[Buyer]] and 
one [[Seller]]) repeating Confirming Party sequences, and one of these parties will also be the 
submitter of the MT515 record. It should be noted that certain fields in this block must follow 
the Confirming Party subsequences (36B, 35B and 70E).  
95R Party  
• BUYR/GSCC/PART – specifies the [[Buyer]] or Reverse Party (the “GSCC” [[issuer]] code allows 
the specification to include the [[GSD]] [[Member]] or counterparty  [[ID]], depending on who is acting 
as [[Buyer]] or [[Seller]]).  
• SELL/GSCC/PART – specifies the [[Seller]] or Repo Party.  
e.g., :95R::BUYR/GSC C/PART9ZX1  
Note: 
The [[Member]] must populate the field with the appropriate qualifier and 4- character [[Member]] [[ID]], for 
[[Buyer]] or [[Seller]].  
20C Processing Reference  
PROC// – This field must be used on DK messages in the appropriate [[Buyer]] or [[Seller]] subsequence to  
indicate the Counterparty ’s External Reference Number of the trade being DK’d.  
 e.g., :20C::PROC//CPXREF100  
70E Declaration Details Narrative (DECL)  
This field will be used in each subsequence to identify the executing firm, where applicable.  
• DECL//GSCC – denotes narrative information specific to [[GSD]].  
• /CORR – should be used in the BUYR and/or SELL confirming party sequence(s) to indicate 
the 4- or 5-character symbol (s) for the applicable [[Buyer]] and/or [[Seller]]’s executing firm(s).  
 
3 Tags 36B, 35B and 70E::TPRO// in the CONFDET block must be placed on the message following the confirming party subsequences.  

---

## Page 27

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 27 
Block/Tag Notes 
e.g., :70E::DECL//GSCC/CORREXFIRM  
Note: 
Only executing firm symbols with documented and established relationships in the [[GSD]] system should 
be enter ed in this field.  
70C Party Narrative (PACO)  
This field will be used in the appropriate [[Buyer]] or [[Seller]] confirming party sequence on MT515 Instructs, 
Cancels or Modifies submitted to provide information regarding the individual/desk at the counterparty  
that executed the trade.  It should be noted that the trader [[ID]] field is for informational purposes only 
and will be captured for the purposes of passing the information to the counterparty  on MT518 
Comparison Request messages. This field will not be compared or validated, nor  wil l it be a basis for 
rejection or DK capabilities.  
• PACO//GSCC – denotes [[Member]] contact narrative information specific to [[GSD]].  
• /TDID – should be used in the appropriate BUYR or SELL confirming party sequence to 
indicate the following:  
o on MT515 Instruct, Cancel or Modify Records, this qualifier should be used by the 
submitter to indicate the [[Buyer]] or [[Seller]] counterparty  [[ID]] of the trader that executed 
the trade.  
o on MT515 DK messages, this qualifier should be used to reflect the buying or selling 
submitter’s [[ID]] of the trader that executed the trade (as originally submitted by the 
counterparty ).  
e.g., :70C::PACO//GSCC/TDIDMARK15  
SETDET This Optional block, and the AMT subsequence, are necessary only when commission is 
specified on the trade. Currently, [[GSD]] accepts commission on When Issue (WI) trades for 
coupon bearing instruments submitted prior to auction, or on Repo trades.  
22F [[settlement]] Transaction Indicator (SETR)  
This field is mandatory for the Block.  
• SETR//RPTO – Indicates that this trade confirmation is for reporting purposes only.  
e.g., :22F::SETR//RPTO  
Note: 
This field is not used by [[GSD]] although it is SWIFT mandatory in order to support the inclusion of the 
Commission Amount field. 
AMT As indicated above, this Optional sequence is only necessary to support the inclusion of 
[[Broker]] commission on a WI trade or a commission amount on a Repo Trade. This block should 
always be included within the [[settlement]] Details (SETDET) block.  
17B Standing Instructions Override  
This field is mandatory for the Block.  
• STAN//N – This indicates that standing instructions should not be overridden.  
e.g., :17B::STAN//N  

---

## Page 28

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 28 
Block/Tag Notes 
Note: 
This field is not used by [[GSD]] although it is SWIFT mandatory in order to support the inclusion of the 
Commission Amount field.  
19A [[Broker]]’s Commission  
LOCO//USD – This field specifies the [[Broker]]’s commission amount on WI trades or Repo trades. The 
commission amount field is left justified, with commas removed, and a comma used in lieu of a 
decimal. The amount must be preceded by a 3- character ISO currency code.  
e.g., :19A::LOCO//USD55,  
Note: 
The value in this field is an AMOUNT - this differs from the rate field format within the [[GSD]] system. The 
Commission Amount per trade should be included in this field – e.g., where the commission is $40 per 
million, for a two million dollar trade the field should be displayed “LOCO//USD80,” . 
Note: 
The commission amount submitted for a Repo trade should not be included in the net money. [[GSD]] will 
not process the value in this field for Repo trades . 
REPO The Optional Repo Block ap pears only on trade contract involving a repurchase/ reverse 
repurchase trade. It appears only once in the contract. Its inclusion indicates that the trade is 
either a Repo or Reverse trade, based on the BUSE indicator in the CONFDET Block (BUYI = 
Reverse, SELL = Repo). This block must be included on a MT515 record for a Repo trade.  
98A Repurchase Date  
• REPU// – This mandatory field specifies the Repo End Leg [[settlement]] Date in the format 
“YYYYMMDD”.  
e.g., :98A::REPU//20191128  
20C Secondary Reference  
• SECO// – This field is optional, but if used, should include the qualifier “SECO” to support an 
additional reference number for the [[Member]]’s REPO trade.  
e.g., :20C::SECO//2NDREFNUM 
Note: 
This field must be populated with an uppercase alphanumeric value. It cannot contain symbols or 
hyphens . 
92A Repo Rate  
• REPO// – The mandatory REPO Rate field is left justified with a comma inserted in lieu of a 
decimal.  
e.g., :92A::REPO//4,25 

---

## Page 29

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 29 
Block/Tag Notes 
Note: 
The [[GSD]] system only supports a field size of [N]15d. The [[Member]] should populate the field with a 
value no larger than [N]15d. For neg ative repo rates, the “N” is counted as part of the 15d. Also, only 2 
decimal places after the comma are allowed.  
19A Repurchase Amount  
• REPA// – The End Leg [[settlement]] Amount  is always prefixed by the ISO currency code 
(USD) and is left -justified with commas removed, and a comma used in lieu of a decimal.  
e.g., :19A::REPA//USD52125100,25  
Note: 
This field can accommodate a value of 15d.  Also, only 2 decimal places after the c omma are allowed.  
 
 
 
 
 
 
 
  

---

## Page 30

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 30 
MT515 Trade Instruct Message Mapping 
This section provides a mapping of the MT515 message to [[GSD]]’S proprietary inbound INSTRUCT record. It is intended to provide a guide as to how to 
best populate the new MT515 messages. From the mapping it can be noted where there are differences in data requirements, field sizes and field 
formats. The mapping is presented using the MT515 format. 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field 
Description 
Data Field 
Format 
[[GSD]] Field Length Start  End Format Comment 
    Message Header        
M       Password  12!c Password  12 17 28 A/N Unique identifier to be 
assigned by [[GSD]] - trailing 
blanks  
M       Sender  8!c [[Member]] [[ID]] 4 33 36 N [[Member]] [[ID]] – trailing blanks. 
Where submitter is not 
[[Member]], [[GSD]] to assign [[ID]]  
M       Message Type 3!n/3!n/4!c       Message 
type/version/[[issuer]] [[ID]]  
515/000/GSCC  
Version = “000” 
M       Receiver  8!c      [[GSD]] receiving system - 
“GSCCTRRS” or 
“GCFCTRRS”. This field will 
be used to route the 
message to the appropriate 
application.  
M :16R: GENL   Mandatory Start 
of Block 
        
M :20C: :SEME//   Sender's 
Message 
Reference 
16x      No corresponding field on 
[[GSD]] proprietary layout.  

---

## Page 31

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 31 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
[[Member]]’s Message number 
(communications) – any 
combination of uppercase 
alphanumeric characters - 
no symbols/hyphens.  
M :23G: NEWM   Function of the 
Message – New 
or 
4!c      Where 23G = NEWM, the 
record will either be an 
Instruct, Modify, or a DK 
message. 
    CANC   Cancel         Where 23G = CANC, the 
record will be mapped to a 
Cancel record.  
O :98C: :PREP//   Preparation 
Date/Time 
YYYYMMDDHH
MMSS 
     No corresponding field on 
[[GSD]] proprietary layout.  
M :22F: :TRTR/ GSCC/CASH Trade 
Transaction Type 
– Cash Trade 
Indicator            
or 
4!c Locked -in 1 210 210 A/N Where 22F = 
TRTR/GSCC/REPO or 
CASH, the trade is 
submitted for bilateral 
comparison  
Where 22F = 
TRTR/GSCC/TRLR or 
TRLK, the trade is locked -in
 
Where 22F = 
TRTR/GSCC/TRDC or 
TRDR, the trade is demand.
 
M   GSCC/REPO Repo Trade 
Indicator            
or 
       
   GSCC/TRLK Locked -in Cash 
Trade Indicator  
or 
       

---

## Page 32

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 32 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
   GSCC/TRLR Locked -in Repo 
Trade Indicator  
or 
       
   GSCC/TRDC Demand Cash 
Trade Indicator  
or 
       
   GSCC/TRDR Demand Repo 
Trade Indicator  
       
M :16R: LINK   Mandatory 
Repeat Start of 
Block 
        
M :20C: :MAST//   Master ([[Member]])  
Reference 
Number 
16x External 
Reference 
Number 
16 63 78 A/N This field is required on all 
Instruct Records. All Cancel 
and Modify records must 
reflect either the “External 
Reference Number” 
(MAST) or the TID (LIST) of 
the trade record being 
canceled or modified. DK 
records must reflect 
“NONREF” in the “MAST” 
field.  
M :16S: LINK   End of Block         
M :16R: LINK   Mandatory 
Repeat Start of 
Block 
        
O :20C: :PREV//   Previous 
Reference 
Number  
16x      NA for Instruct and DK 
Records  
For MT515 Modify Records, 
this field will contain the 
[[Member]]’s Previous 
External Reference.  

---

## Page 33

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 33 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
On MT515 Cancel records, 
the [[Member]] must populate 
the field with the value 
“NONREF”. 
M :16S: LINK   End of Block         
M :16R: LINK   Mandatory 
Repeat Start of 
Block 
        
O :20C: :LIST//   [[GSD]] Assigned 
Reference 
Number 
(Receiver’s TID)  
16x      This field may be populated 
by Members, on Cancels 
and Modifies, such as 
change of X-ref. 
NA for Instruct and DK 
records.  
M :16S: LINK   End of Block         
M :16R: LINK   Mandatory 
Repeat Start of 
Block 
        
O :20C: :BASK//   [[Broker]] Reference 
Number 
16x [[Broker]] 
Reference 
Number 
16 43 58 A/N If [[Broker]] submits trade, 
required [[Broker]] Reference 
Number is mapped here. 
NA for DK records.  
M :16S: LINK   End of Block         
M :16S: GENL   End of Block         
M :16R: CONFDET   Mandatory Start 
of Block 
        
M :98C: :TRAD//   Trade Date & 
Time 
YYYYMMDDHH
MMSS 
Trade Date 8 87 94 A/N 
MMDD
YYYY 
Please note differences in 
date format. 

---

## Page 34

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 34 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
      Trade time 6 194 199 A/N 
HHMM
SS 
 
M :98A: :SETT//   [[settlement]] Date  YYYYMMDD  [[settlement]] 
Date 
8 95 102 A/N 
MMDD
YYYY 
Where trade is a cash 
trade, map [[settlement]] date 
here. 
Please note differences in 
date format. 
      Start Leg 
[[settlement]] 
Date 
8 239 246 A/N 
MMDD
YYYY 
Where trade is a repo trade, 
map repo start date here.  
Please note differences in 
date format. 
M :90A: :DEAL/ /PRCT/ Deal Price – 
Percentage 
or   
15d Pricing 
Method 
1 150 150 A/N Where price type is Dollar 
Price or Repo Rate - 
populate field with “PRCT”.  
      Price/Repo 
Rate 
14 136 149 A/N If trade is repo, price must 
be “0,” otherwise, place 
dollar price here.  
   /YIEL/ Yield                  
or 
[N]15d Pricing 
Method 
1 150 150 A/N YIEL = ‘Y’ = Yield  
      Price/Repo 
Rate 
14 136 149 A/N  
   /DISC/ Discount  15d Pricing 
Method 
1  150 150 A/N DISC = ‘D’ = Discount  
      Price/Repo 
Rate 
14  136 149 A/N  
O :19A: :SETT/ /USD [[settlement]] 
Amount 
15d Net Money  18 151 168 A/N Where trade is a cash 
trade, map net money here.  

---

## Page 35

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 35 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
      Start Leg 
[[settlement]] 
Amount 
18 221 238 A/N Where trade is a repo trade, 
map Start Amount here.  
M :22H: :BUSE/ /BUYI Trade Type – Buy 
(REVR)              
or 
4!c Transaction 
Type  
4 83 86 A/N Where trade is Buy or 
Reverse, populate field with 
“BUYI”. 
      /SELL Sell (REPO)   Transaction 
Type  
4 83 86 A/N Where trade is Sell or 
Repo, populate field with 
“SELL”. 
O :22F: :PROC/ GSCC/INST Processing 
Indicator – 
Instruct   
or                                  
4!c Command 
Type  
4 29 32 A/N Where 22F = 
PROC/GSCC/INST 
populate command type = 
“INST” 
      GSCC/CANC Cancel               
or                           
  Command 
Type  
4 29 32 A/N NA for INST record.  
      GSCC/MDFC Modify               
or 
  Command 
Type  
4 29 32 A/N NA for INST record.  
      GSCC/TDDK DK   Command 
Type  
4 29 32 A/N NA for INST record.  
M :22H: :PAYM/ /APMT Against Payment 
Indicator – vs. 
Payment  
4!c      This field is SWIFT 
mandatory for all MT515 
records.  
M :16R: CONFPRTY   Mandatory 
Repeat Start of 
Block 
        
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]] 34x [[Member]] [[ID]] 4 33 36 N Where Buying party is 
[[Member]], map [[Member]] [[ID]] 
here. 
      Counterparty 
Firm 
4 169 172 N Where Buying party is 
Counterparty, map 
Counterparty Firm [[ID]] here.  

---

## Page 36

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications – MT515 36 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
O :20C: :PROC//   Processing 
Reference – 
[[Buyer]] 
(Counterparty) X -
ref 
16x      NA for INST record. 
Applicable to DK record 
only.  
O :70E: :DECL/ /GSCC Declaration 
Details Narrative 
(10*35x)      The below fields can be 
included within this 
narrative field, where 
appropriate.  
      /CORR Party = [[Buyer]]’s 
Executing firm  
5c [[Member]]’s 
Executing 
Firm 
5 200 204 A/N Where Buying party has an 
Executing Firm customer  
trade, populate field with 
either [[Member]] or 
Counterparty Executing 
Firm symbol , as applicable . 
      Counterparty’
s Executing 
Firm 
5 205 209 A/N  
O :70C: :PACO/ /GSCC Party Narrative (4*35x)       
      /TDID [[Buyer]] 
(Counterparty) 
Trader [[ID]] 
20c      On Instruct, Modify and 
Cancel, populate this field 
with Counterparty Trader 
[[ID]], where known. (On DK 
records this will represent 
submitter’s Trader [[ID]]).  
No corresponding field on 
[[GSD]] proprietary layout.  
M :16S: CONFPRTY   End of Block         
M :16R: CONFPRTY   Mandatory 
Repeat Start of 
Block 
        

---

## Page 37

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 37 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
M :95R: :SELL/ GSCC/PART Party = [[Seller]]  34x [[Member]] [[ID]] 4 33 36 N Where Selling party is 
[[Member]], map [[Member]] [[ID]] 
here. 
      Counterparty 
Firm 
4 169 172 N Where Selling party is 
Counterparty, map 
Counterparty Firm [[ID]] here.  
O :20C: :PROC//   Processing 
Reference – 
[[Seller]] 
(Counterparty) X -
ref 
16x      NA for INST record. 
Applicable to DK record 
only.  
O :70E: :DECL/ /GSCC Declaration 
Details Narrative 
(10*35x)      The below fields can be 
included within this 
narrative field, where 
appropriate.  
      /CORR Party = [[Seller]]’s 
Executing firm  
5c [[Member]]’s 
Executing 
Firm 
5 200 204 A/N Where Selling party has an 
Executing Firm customer 
trade, populate field with 
either [[Member]] or 
Counterparty Executing 
Firm system, as app licable . 
      Counterparty’
s Executing 
Firm 
5 205 209 A/N  
  :70C: :PACO/ /GSCC Party Narrative (4*35x)       
      /TDID [[Seller]] 
(Counterparty) 
Trader [[ID]] 
20c      On Instruct, Modify and 
Cancel, populate this field 
with Counterparty Trader 
[[ID]], where known. (On DK 
records this will represent 
submitter’s Trader [[ID]]).  
No corresponding field on 
[[GSD]] proprietary layout.  

---

## Page 38

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 38 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
M :16S: CONFPRTY   End of Block         
M :36B: :CONF/ FAMT/ Quantity of Face 
Amount (Par)  
15d Quantity  18 118 135 A/N  
M :35B: /US/   Identification of 
Financial 
Instrument/ 
Security ([[CUSIP]]) 
(4*35x) [[CUSIP]] 9 103 111 A/N  
O :70E: TPRO/ /GSCC Trade Instruction 
Processing 
Narrative  
(10*35x)       
   /MSGR Message Reason 
(see Appendix E)  
4!c       
   /DKRS DK Reason (see 
Appendix E)  
4!c      NA for INST record. 
Applicable to DK record 
only.  
M :16S: CONFDET  End of Block         
M :16R: SETDET  Optional Start of 
Block  
      This sequence is required 
where there is [[Broker]] 
commission on WI trades - 
or to support submission of 
commission infor mation on 
REPO trades.  
M  :22F:  :SETR  /RPTO  [[settlement]] 
Transaction 
Indicator 
(Reporting 
Purposes)  
4!c       This field is mandatory 
where commission exists 
on WI or repo trade.  
M :16R:  AMT   Optional Start of 
Block 
       

---

## Page 39

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 39 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
O  :17B:  :STAN/  /N  Standing 
Instruction 
Override = No  
1!a       This field is mandatory 
where commission exists 
on WI or repo trade.  
M  :19A:  :LOCO/  /USD  [[Broker]]’s 
Commission  
15d  Commission  11 179 189 A/N For WI trades as well as 
REPO trades. Total 
Commission Amount shou ld 
be stated on a per -trade 
amount, rather than on a 
rate basis.  
NOTE: For REPO trades 
submitted, this commission 
amount should NOT be 
included in net money.  
[[GSD]] systems will maintain 
the commission for WI 
trades in rate, rather than 
amount, format. 
M :16S:  AMT       End of Block        
M :16S:  SETDET   End of Block        
M :16R:  REPO   Optional Start of 
Block 
      This block must be included 
on repo trades. NA for cash 
trades. 
O :98A:  :REPU//   End Leg 
[[settlement]] Date  
YYYYMMDD  [[settlement]] 
Date 
8 95 102 A/N 
MMDD
YY 
This field = [[settlement]] date 
of End Leg. Please note 
differences in date formats.  
O :20C:  :SECO//   Secondary 
Reference  
16x  Secondary 
Reference 
Number 
16 247 262 A/N Where 22F = 
TRTR/GSCC/REPO or 
TRLR, map this field to 
[[Member]]’s Secondary 
Reference number.  
O :92A:  :REPO//   Repo Rate  [N]15d  Price/Repo 
Rate 
14 136 149 A/N For repo trades, map 
Price/Repo Rate here.  

---

## Page 40

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT515 40 
SWIFT MT515 Record Format  [[GSD]] Record Fields 
O 19A:  :REPA//  /USD  End Leg 
[[settlement]] 
Amount  
15d  Net Money  18 151 168 A/N For repo trades, map Net 
Money here.  
M :16S:  REPO  End of Block        
 
 
 

---

## Page 41

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 41 
COMPARISON INTERACTIVE MESSAGE SPECIFICATIONS 
– MT509 
This section contains the detailed specifications including layout and field descriptions for MT509 Messages 
supporting comparison output for [[GSD]]’s products and services.  
MT509 Trade Status Message Description 
The SWIFT MT509 Message is specified as a Trade Status Message and will be used by [[GSD]] as a means to 
communicate status messages related to the [[GSD]] Comparison process. The MT509 Message does not 
contain full trade details, but rather provides the trade status along with the full set of reference numbers to 
enable the [[Member]] to identify the trade being reported on (e.g., [[Member]] Reference Number, Secondary 
Reference Number, Counterparty External Reference Number, [[Broker]] Reference Number (or [[Broker]] TID) and 
the [[GSD]] Assigned Reference Number (Receiver’s TID), where appropriate). 
Certain status messages also include additional fields, such as reason codes for reject messages, etc. Field 
25D in the Status (STAT) Block indicates to the recipient the type of record being sent. In the case of a Modify 
or DK reject, a second field, 70D in the Reason (REAS) block, must also be read to determine the record type. 
These MT509 Messages also contain a “Ack” (Accepted/Validated) or “Nack” (Rejected) Status unlike the 
MT509 Netting Status Messages. The qualifiers representing the type of record being sent in Field 25D, are 
shown below.  
As it relates to [[GSD]]’s Comparison process, MT509 Messages will be generated for each of the following 
products and trade statuses seen below: 
• DVP: regular buy/sell, repo/revr, auction buy/sell (Trade Balanced does not apply) 
• GCF: repo/revr  (Repo Substitution Processed, DK Rejected, DK Accepted, DK Processed, Trade 
Canceled due to DK, Trade Compared through Par Summarization, Cancel Lifted by [[participant]] [[DO]] not 
apply to this product) 
• CCIT: repo/revr (Repo Substitution Processed, DK Rejected, DK Accepted, DK Processed, Trade 
Canceled due to DK, Trade Compared through Par Summarization, Cancel Lifted by [[participant]], Trade 
Balanced [[DO]] not apply to this product) 
 
Message Type This message will be sent to : DVP GCF  CCIT 
Trade Input Accepted 
(:25D::IPRC//PACK) 
the submitting party once their trade input has been validated 
by the [[GSD]] system . 
   
Trade Input, Modify, or DK 
Rejected (:25D::IPRC//REJT)  
the submitting party to indicate that their input, modification or 
DK has been rejected by [[GSD]]’s validation process. A list of 
applicable Reason Codes can be found in the Appendix E 
(Reason Code Tables) . 
   

---

## Page 42

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 42 
Message Type This message will be sent to : DVP GCF  CCIT 
Repo Substitution Processed 
(:25D::IPRC/GSCC/RPSP) 
to all parties, indicating a substitution has occurred and that 
[[GSD]] has changed the terms of the repo in its system to 
reflect the new details. All parties will also receive an MT518 
reflecting new trade details.  
   
Modify Accepted 
(:25D::IPRC/GSCC/MODA) 
the submitting party once their trade modification has been 
validated by the [[GSD]] system.  
   
Modify Processed 
(:25D::IPRC/GSCC/MODP) 
the submitting party once their trade modification has been 
processed by the [[GSD]] system.  
   
Deleted Uncompared 
Transaction 
(:25D::IPRC/GSCC/DELE) 
the submitting party indicating that an uncompared trade has 
been deleted from [[GSD]]’ s processing system. Currently, 
trades are deleted if they remain uncompared in the system 
for three days or, in the case of when issued trades on 
auction date + 3, or for forward start repo trades on start date 
+ 3. The counterparty  will receive an MT518 indicating that 
the advisory has been deleted.  
   
DK Accepted 
(:25D::IPRC/GSCC/PADK) 
the submitting party once their DK has been validated by the 
[[GSD]] system . 
   
DK Processed 
(:25D::IPRC/GSCC/DPPR) 
the submitting party once their DK has been processed by the 
[[GSD]] system . 
   
Trade Canceled due to DK 
(:25D::IPRC//DEDK) 
inform the trade submitter that their trade has been 
administratively canceled by the [[GSD]] system because it was 
DK’d by the counterparty . 
   
Trade Balanced 
(:25D::IPRC/GSCC/BALC) 
the [[Broker]] to acknowledge that a trade has balanced .    
Cancel Accepted 
(:25D::CPRC//PACK) 
the submitting party once their trade cancellation has been 
validated by the [[GSD]] system . 
   
Cancel Rejected 
(:25D::CPRC//REJT) 
the submitting party to indicate that their trade cancellation 
has been rejected by [[GSD]]’s validation process.  
   
Cancel Processed 
(:25D::CPRC//CAND) 
the submitting party once their trade cancellation has been 
processed by the [[GSD]] system.  
   
Cancel Lifted by [[participant]] 
(:25D::CPRC/GSCC/UPBP) 
the [[Member]] when a previously submitted Cancel message 
(for a Compared trade) has been removed/lifted by [[GSD]] at 
the request of the [[Member]] . 
   
Trade Compared 
(:25D::MTCH//MACH) 
the submitting party once their trade has been compared 
(either bilaterally or administratively) by the [[GSD]] system . 
   
Trade Compared through Par 
Summarization 
(:25D::MTCH/GSCC/PSUM) 
all trade parties when a submitted trade has been compared 
during the enhanced comparison process, based on a 
presumed match of data using par summarization. One record 
will be sent to a [[Member]] for each submitted trade that was 
compared via Par Summarization. No Counterparty External 
Reference Numbers will be provided on these messages.  
   

---

## Page 43

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 43 
Message Type This message will be sent to : DVP GCF  CCIT 
Note:  
Par summarization presumes a match of trades if the total par 
and final money of one or multiple buy sides equals the total 
par and final money of one or multiple sell sides.  
  

---

## Page 44

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 44 
MT509 Trade Status Message Specifications 
MT509 Trade Status Message General Format 
This section provides the general format for the MT509 Message. As described in the MT509 Message 
Description, the MT509 will be sent by [[GSD]] to Members for the following trade status events: 
• Trade Input Accepted 
• Trade Input Rejected 
• Repo Substitution Processed 
• Modify Accepted 
• Modify Rejected 
• Modify Processed 
• Deleted Uncompared Transaction 
• DK Accepted 
• DK Rejected 
• DK Processed 
• Trade Canceled due to DK 
• Trade Balanced 
• Cancel Accepted 
• Cancel Rejected 
• Cancel Processed 
• Cancel Lifted by [[participant]] 
• Trade Compared 
• Trade Compared Through Par Summarization 
 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  DVP GCF CCIT 
    Message Header     
M       Password  12!c    
M       Sender  8!c    
M       Message Type 3!n/3!n/4!c     
M       Receiver  8!c    
M :16R: GENL   Mandatory Start of 
Block 
     
M :20C: :SEME//   Sender's Message 
Reference 
16x    
M :23G: INST   Message Function – 
Instruct 
or 
4!c    

---

## Page 45

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 45 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  DVP GCF CCIT 
    CAST   Cancel       
O :98C: :PREP//   Preparation Date/Time YYYYMMDDHHMMSS    
M :16R: LINK   Mandatory Repeat 
Start of Block 
     
M :20C: :MAST//   Master ([[Member]])  
Reference Number 
16x    
M :16S: LINK   End of Block      
M :16R: LINK   Mandatory Repeat 
Start of Block 
     
O :20C: :PREV//   Previous Reference 
Number 
16x    
M :16S: LINK   End of Block      
M :16R: LINK   Mandatory Repeat 
Start of Block 
     
O :20C: :RELA//  Related Reference 
Number (Sender's 
Reference)  
16x    
M :16S: LINK   End of Block      
M :16R: LINK   Mandatory Repeat 
Start of Block 
     
O :20C: :INDX//  Secondary Reference 
Number 
16x    
M :16S: LINK   End of Block      
M :16R: LINK   Mandatory Repeat 
Start of Block 
     
O :20C: :LIST//   [[GSD]] Assigned 
Reference Number 
(Receiver’s TID)  
16x    
M :16S: LINK   End of Block      
M :16R: LINK   Mandatory Repeat 
Start of Block 
     
O :20C: :PROG//  Counterparty  
Reference Number 
16x    
M :16S: LINK   End of Block      
M :16R: LINK   Mandatory Repeat 
Start of Block 
     

---

## Page 46

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 46 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  DVP GCF CCIT 
O :13B: :LINK/ GSCC/CASH Linked Message – 
Cash Trade Indicator 
 or 
4!c    
   GSCC/REPO Repo Trade Indicator  
 or 
    
   GSCC/TRLK Locked-in Cash Trade 
Indicator 
  or 
    
   GSCC/TRLR Locked-in Repo Trade 
Indicator 
or 
    
   GSCC/TRDC Demand Cash Trade 
Indicator 
or 
    
   GSCC/TRDR Demand Repo Trade 
Indicator 
    
O :20C: :BASK//   [[Broker]] (Counterparty) 
Reference Number 
([[Broker]] Xref or [[Broker]] 
TID) 
16x    
M :16S: LINK   End of Block      
M :16R: STAT   Mandatory Start of 
Block 
     
M :25D: :IPRC/ /PACK Trade Input 
Accepted/Validated                                                   
or  
4!c    
      /REJT Trade, Trade Modify, or 
DK is rejected                                    
or  
    
   GSCC/RPSP Repo Substitution 
Processed  
or 
    
      GSCC/MODA Modify Accepted                       
or 
    
      GSCC/MODP Modify Processed                     
or 
    
   GSCC/DELE Deleted Uncompared 
Transaction  
or 
    

---

## Page 47

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 47 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  DVP GCF CCIT 
   GSCC/PADK DK Accepted                           
or 
    
      GSCC/DPPR DK Processed                        
or 
    
   GSCC/DEDK Trade Canceled due to 
DK 
or 
    
   GSCC/BALC Trade Balanced  
or 
    
    :CPRC/ /PACK Cancel Accepted                      
or 
     
    /REJT Cancel Rejected                       
or 
    
      /CAND Cancel Processed                    
or  
     
      /GSCC/UPBP Cancel Lifted by 
[[participant]] (Uncancel 
processed)               
or  
     
    :MTCH/ /MACH Trade Compared  
or  
     
   GSCC/PSUM Trade Compared 
Through Par 
Summarization  
    
M :16R: REAS   Optional Start of 
Block 
     
M :24B: :REJT/  Reject Reason Code 
(see Appendix E)  
4!c    
O :70D: :REAS/ /GSCC Reject Reason 
Narrative 
(6*35x)    
   /MDRJ Modify Rejected  
or  
    
   /DKRJ DK Rejected      
M :16S: REAS  End of Block      
M :16S:  STAT       End of Block     
M :16S:  GENL   End of Block     
  

---

## Page 48

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 48 
MT509 Trade Status Message Field Specifications 
This section provides the detailed field specifications for the MT509 Message.   
Block/Tag Notes 
Message 
Header 
Each message must contain a Message Header. All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password   12!c This field will be blank -filled on all MT509 Messages.  
Sender   8!c “GSCCTRRS” ([[GSD]] Trade Registration and Reconciliation System) for DVP, 
“GCFCTRRS” (GCF Trade Registration and Reconciliation System) for GCF/CCIT will 
always be the sender of the MT509 messages.  
Message Type 3!n/3!n/4!c  The first 3 characters indicate to the recipient the message type (509); the second 3 
positions reflect the version of the message interface (currently always 000). The last 
4 characters indicate the [[issuer]] code to be used in the message (GSCC ). 
Receiver 8!c [[Member]] [[ID]] 
GENL This mandatory block provides general information regarding the message. It appears only 
once in a Trade Status message.  
20C Sender's Message Reference  
• SEME// – This mandatory field contains the Sender’s ([[GSD]]) Message Reference Number.  
It is used on all messages sent by [[GSD]] and will contain a unique number to 
unambiguously identify each message. This is a Communications Message Number, not a 
Trade Number. 
e.g., :20C::SEME//GSDNUMREF1 
Note: 
This field must be populated with an uppercase alphanumeric value. It cannot contain symbols or 
hyphens.  
 
23G Function of the Message  
This mandatory field is used on all messages to identify the Function of the Message. It will either be 
the status of an Instruct, Modify, or DK (INST), or regarding the submission of a cancellation of a 
previous message (CAST).  
• INST – This qualifier will be used for Trade Status messages usually referring to Instructs, 
Modifies or DKs. It will also be reflected on all MT509 reject messages where the MT515 was 
rejected.  
• CAST – This qualifier will be used on the various messages referring to cancellations.  
e.g., :23G:INST   
98C Preparation Date and Time  
• PREP// – This field contains the date and time the message sent by [[GSD]] was prepared.  
e.g., :98C::PREP//20191125110459 
Note: 
The “C” Format for this (98) tag indicates a Date/Time Format of “YYYYMMDDHHMMSS”.  

---

## Page 49

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 49 
Block/Tag Notes 
LINK The LINK Block will be repeated for as many reference qualifiers as need to be included in a 
Trade Status Message. Each subsequence contains reference numbers to identify the trade or 
record for which the status is being reported. Each reference number will be enclosed within a 
Start Link Block (:16R:LINK) and End Link Block (:16S:LINK). All LINK repeating subsequences 
are within the GENL Block.  
20C Reference 
The Reference Numbers that have been provided by Members must contain uppercase 
alphanumeric characters and should not contain symbols. As indicated above, each Reference 
Number will be enclosed in a LINK Start and End Block.  
• MAST// – Master Reference Number  - This qualifier contains the [[Member]]’s Referen ce 
Number for the trade (External Reference Number). The MAST qualifier will be present on 
all MT509’s except where an MT515 message was rejected for being non -SWIFT 
compliant and on MT509’s referring to MT515 DK records submitted.  
• PREV// – Previous Reference Number  - This qualifier is used only on records where the 
External Reference Number has been modified by the [[Member]] and will contain the 
[[Member]]’s Previous Reference Number.                                                                                                         
• RELA// – MT515 Sender's Message Reference Number - This qualifier will contain the 
Sender’s Message Reference Number (20C::SEME//) from the MT515 submitted by the 
[[Member]]. It will only appear on those MT509 messages, which are acknowledgements of 
receipt, or rejections, of MT515 [[Member]] messages.  
• INDX// – Secondary Reference Number - This qualifier will contain the [[Member]]’s 
Secondary Reference Number on Status Messages for Repo Trades, where the number 
was originally provided by the [[Member]].  
• LIST// – [[GSD]] Reference Number  - This qualifier will contain the [[GSD]] Reference Number 
(TID - Transaction Identification) for the trade.  
• PROG// – Counterparty Reference Number  -  This field reflects the Counterparty 
External Reference Number. It will  only appear on MT509 messages related to 
Comparison Notification (e.g., Trade Compared (:25D::MTCH//MACH), and on MT509 
messages providing the status of MT515 DK records submitted to [[GSD]].)                                                                                    
• BASK// – [[Broker]] Reference Number  - This field specifies the [[Member]]’s (or 
Counterparty's) [[Broker]] Reference, either a [[GSD]] Assigned Reference Number (TID) 
assigned to the [[Broker]]’s Trade or a [[Broker]] External Reference provided by the [[Broker]] . 
This field is required for [[Broker]] Submitted Trades. The [[Broker]] Reference Number field will 
be preceded by a Linked Message Trade Indicator field. The only exception to this would 
be if the record being reported is due to an input, modify, DK or cancel rejec ted or DK 
accepted. 
e.g., :20C::MAST//PARTNUM1 
Note:  
On MT509 Trade Status messages, the [[Broker]] External Reference will appear in this field. One 
exception to this rule is for MT509 Trade Compared (MACH) messages. For MT509 Trade 
Compared (MACH) messages sent intra- day, where the receiving [[Member]] is the [[Broker]] 
counterparty to a Brokered Demand Same- Day Starting Repo Transaction where either the Start 
Leg and/or End Leg of such transaction is eligible for [[settlement]] through [[GSD]]'s Same- Day Settling 
Service, the [[Broker]]'s [[GSD]] Assigned Reference Number (TID) will appear in this field.  

---

## Page 50

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 50 
Block/Tag Notes 
Note:  
This field will be populated with an uppercase alphanumeric value. It will not contain symbols or 
hyphens except where the Reference Number has been assigned by [[GSD]] . 
 
13B Linked Message  
The Link Message field indicates the Message type number/message identifier of the message 
referenced in the linkage sequence in this sequence, this field indicates that the trade is being 
reported as a Repo and whether the trade is Demand. This field will only appear on a record if a 
[[Broker]] Reference Number (:20C::BASK//) is also included on the record. The only exception to this 
would be if the record being reported is due to an input, modify, DK or cancel rejected or DK ac cepted. 
• LINK/GSCC/CASH – This qualifier/[[Option]] will be used on Cash trades.                              
• LINK/GSCC/REPO – This qualifier/[[Option]] will be used on repo trades requiring Bilateral 
comparison. 
• LINK/GSCC/TRLK – This qualifier/[[Option]] will be used on Locked- in Cash trades   
• LINK/GSCC/TRLR – This qualifier/[[Option]] will be used on Locked- in Repo trades.                              
• LINK/GSCC/TRDC – This qualifier/[[Option]] will be used on Demand cash trades.  
• LINK/GSCC/TRDR – This qualifier/[[Option]] will be used on Demand repo trades.  
e.g., :13B::LINK/GSCC/REPO  
Note:  
This field is not a LINK Block and will only appear when the trade being reported includes a [[Broker]] 
Reference. 
STATUS The Status Block will appear on every MT509 message and will notify the [[Member]] of the type of 
MT509 record being sent, as well as the status of the trade, or record, that was submitted to 
[[GSD]]. 
25D Status Code  
The Status Code indicates the record type/type of Status Message being sent by [[GSD]]. The following 
are the various mess age types, which will be used for Interactive Messaging to support real -time 
comparison.  
• IPRC//PACK – This qualifier/[[Option]] is used to indicate that an instruction message has been 
accepted by [[GSD]].  
• IPRC//REJT – This qualifier/[[Option]] is used to indicate tha t an Instruct, a Modify, or a DK 
message has been rejected by [[GSD]]. Where this is used to indicate that a Modify, or DK 
record has been rejected, field 70D in the REAS block will be populated as follows: 
“:70D::REAS//GSCC/MDRJ” or “:70D::REAS//GSCC/DKRJ”. T he IPRC//REJT qualifier will be 
used in all instances where an incoming MT515 is rejected for being non -SWIFT compliant 
(:24B::REJT/GSCC/F999). 
• IPRC/GSCC/RPSP – This qualifier/[[Option]] is used to indicate to all parties to a repo trade that 
a repo substituti on has been processed.  
• IPRC/GSCC/MODA – This qualifier/[[Option]] is used to indicate to the submitter that a trade 
modification record has been accepted.                                                                                        

---

## Page 51

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 51 
Block/Tag Notes 
• IPRC/GSCC/MODP – This qualifier/[[Option]] is used to indicate to the submitter that the trade 
modification requested has been processed.  
• IPRC/GSCC/DELE – This qualifier/[[Option]] is used to indicate to the submitter that a trade that 
was pending comparison has been deleted.  
• IPRC/GSCC/PADK – This qualifier/[[Option]] is used to indicate to the submitter that a DK 
record has been accepted and is awaiting further processing.  
• IPRC/GSCC/DPPR – This qualifier/[[Option]] is used to indicate to the submitter that a DK 
record accepted by the system has been processed.  
• IPRC/GSCC/DEDK – This qualifier/[[Option]] is used to indicate that a trade previously 
submitted to [[GSD]] has been canceled due to DK.                                                           
• IPRC/GSCC/BALC – This qualifier/[[Option]] is used to indicate to the submitting [[Broker]] that 
their trade has been balanced.  
• CPRC//PACK – This qualifier/[[Option]] is used to indicate to the submitter that a Cancel Record 
has been accepted by [[GSD]].  
• CPRC//REJT – This qualifier/[[Option]] is u sed to indicate to the submitter that a Cancel Record 
submitted to [[GSD]] has been rejected.                                                                                                 
• CPRC//CAND – This qualifier/[[Option]] is used to indicate that a Cancel instruction has been 
processed (trade instruction has been canceled). This record will be sent when [[GSD]] has 
processed a cancellation requested by a [[Member]].  
• CPRC/GSCC/UPBP – This qualifier/[[Option]] is used to indicate that a Cancel record previously 
submitted has been removed or ‘lifted’ by either the [[Member]] or [[GSD]].  
• MTCH//MACH – This qualifier/[[Option]] is used to indicate to the parties on a trade that a trade 
has compared.   
• MTCH/GSCC/PSUM – This qualifier/[[Option]] is used to identify the trades that have compared 
via par summarization. These records will be sent to a [[Member]] for its trades that have been 
par summarized. 
e.g., :25D::IPRC/GSCC/PADK   
REASON The Reason Block will only appear on MT509 messages where an MT515 (Instruct, Modify, 
Cancel or DK) submitted by the [[Member]] has been rejected by [[GSD]]. Each Reason Code must 
be enclosed within a Start Reason (:16R:REAS) and End Reason (:16S:REAS) Block.  
 
24B Reason Code  
This field is mandatory in the block and will appear on all Reject messages. There can be multiple 
reason codes on any MT509 Reject Message; each Reason Code must be enclosed within a Start 
Reason (:16R:REAS) and End Reason (:16S:REAS) Block. The Reason Code will be populated with 
the following value:  
• REJT/ – this qualifier will be reflected on all messages that indicate to the [[Member]] that the 
MT515 they submitted was rejected by [[GSD]].  
e.g., :24B::REJT/GSCC/E018 
Note:  
As the list of error codes can be expanded in the future, the list will be amended, without modifying the 
entire specification. Please refer to Appendix E of this document for a list of all error conditions (and 
associated codes) that would result in the rejection of a [[Member]]’s MT515 message.  
70D Reason Narrative (REAS)  

---

## Page 52

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 52 
Block/Tag Notes 
• REAS//GSCC – The reason narrative field can contain narrative on those MT509 reject 
messages created in response to receiving a non -SWIFT compliant MT515, or can  contain 
the following qualifier:  
• /MDRJ – This qualifier will be included on an MT509 Instruct Reject Message when a trade 
modification MT515 is rejected by [[GSD]].  
• /DKRJ – This qualifier will be included on an MT509 Instruct Reject Message when an 
MT515 DK s ubmitted is rejected by [[GSD]].  
e.g., :70D::REAS//GSCC/DKRJ                                                                                                     
Note:  
This narrative field will appear in the first repeating REAS sequence.  
 
 
  

---

## Page 53

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specification s – MT509 53 
MT509 Trade Status Message Field Analysis 
This section contains an analysis of the fields that may be found on each MT509 Comparison Message. The analysis is separated into two categories; 
1) Trade Input, Modify or DK and 2) Trade Cancel and Match. For each applicable record type, a check mark will be found where it is possible for that 
field to appear on that record. It should be noted, however, that where a check mark appears, the check mark is not intended to indicate that a field is 
mandatory for a given record type. Where there is no check mark in a given box, that field is not applicable for the record type in question. 
Trade Input, Modify or DK 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description IPRC// 
PACK 
IPRC// 
REJT 
IPRC/ 
GSCC/ 
RPSP 
IPRC/ 
GSCC/ 
MODA 
IPRC/ 
GSCC/ 
MDRJ 
IPRC/ 
GSCC/ 
MODP 
IPRC/ 
GSCC/ 
PADK 
IPRC/ 
GSCC/ 
DKRJ 
IPRC/ 
GSCC/ 
DPPR 
IPRC// 
DEDK 
IPRC/ 
GSCC/ 
BALC 
        Message Header                     
M       Password             
M       Sender             
M       Message Type            
M       Receiver             
M :16R: GENL   Mandatory Start of 
Block 
                    
M :20C: :SEME//   Sender's Message 
Reference 
           
M :23G: INST   Message Function – 
Instruct 
           
    CAST   Cancel                      
O :98C: :PREP//   Preparation 
Date/Time 
           
M :16R: LINK   Repeat Block Start                     
M :20C: :MAST//   Master ([[Member]])  
Reference Number 
              

---

## Page 54

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 54 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description IPRC// 
PACK 
IPRC// 
REJT 
IPRC/ 
GSCC/ 
RPSP 
IPRC/ 
GSCC/ 
MODA 
IPRC/ 
GSCC/ 
MDRJ 
IPRC/ 
GSCC/ 
MODP 
IPRC/ 
GSCC/ 
PADK 
IPRC/ 
GSCC/ 
DKRJ 
IPRC/ 
GSCC/ 
DPPR 
IPRC// 
DEDK 
IPRC/ 
GSCC/ 
BALC 
M :16S: LINK   End of Block                     
M :16R: LINK   Repeat Block Start                     
O :20C: :PREV//   Previous Reference 
Number 
                 
M :16S: LINK   End of Block                     
M :16R: LINK   Repeat Block Start                     
O :20C: :RELA//   Related Reference 
Number (Sender's 
Reference)  
              
M :16S: LINK   End of Block                     
M :16R: LINK   Repeat Block Start                     
O :20C: :INDX//   Secondary 
Reference Number 
              
M :16S: LINK   End of Block                     
M :16R: LINK   Repeat Block Start                     
O :20C: :LIST//   [[GSD]] Assigned 
Reference Number 
(Receiver’s TID)  
               
M :16S: LINK   End of Block                     
M :16R: LINK   Repeat Block Start                     
O :20C: :PROG//   Counterparty 
Reference Number 
                 
M :16S: LINK   End of Block                     
M :16R: LINK   Repeat Block Start                     

---

## Page 55

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 55 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description IPRC// 
PACK 
IPRC// 
REJT 
IPRC/ 
GSCC/ 
RPSP 
IPRC/ 
GSCC/ 
MODA 
IPRC/ 
GSCC/ 
MDRJ 
IPRC/ 
GSCC/ 
MODP 
IPRC/ 
GSCC/ 
PADK 
IPRC/ 
GSCC/ 
DKRJ 
IPRC/ 
GSCC/ 
DPPR 
IPRC// 
DEDK 
IPRC/ 
GSCC/ 
BALC 
O :13B: :LINK/ GSCC/CASH Linked Message – 
Cash Trade Indicator 
 or 
 
 
  
 
         
      GSCC/REPO Repo Trade Indicator  
 or 
 
 
  
 
         
   GSCC/TRLK Locked-in Cash 
Trade Indicator 
or 
           
   GSCC/TRLR Locked-in Repo 
Trade Indicator 
or 
           
   GSCC/TRDC Demand Cash Trade 
Indicator 
or 
           
   GSCC/TRDR Demand Repo Trade 
Indicator 
           
O :20C: :BASK//   [[Broker]] 
(Counterparty) 
Reference Number 
([[Broker]] Xref or 
[[Broker]] TID) 
              
M :16S: LINK   End of Block                     
M :16R: STAT   Repeat Block Start                     
M :25D: :IPRC/ /PACK Trade Input 
Accepted/Validated   
or  
                   

---

## Page 56

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 56 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description IPRC// 
PACK 
IPRC// 
REJT 
IPRC/ 
GSCC/ 
RPSP 
IPRC/ 
GSCC/ 
MODA 
IPRC/ 
GSCC/ 
MDRJ 
IPRC/ 
GSCC/ 
MODP 
IPRC/ 
GSCC/ 
PADK 
IPRC/ 
GSCC/ 
DKRJ 
IPRC/ 
GSCC/ 
DPPR 
IPRC// 
DEDK 
IPRC/ 
GSCC/ 
BALC 
      /REJT Trade, Trade Modify, 
or DK is rejected  
or  
                 
   GSCC/RPSP Repo Substitution 
Processed  
or 
           
      GSCC/MODA Modify Accepted  
or 
                   
      GSCC/MODP Modify Processed  
or 
                   
      GSCC/PADK DK Accepted  
or 
                   
      GSCC/DPPR DK Processed  
or 
                   
      GSCC/DEDK Trade Canceled due 
to DK 
or 
                   
   GSCC/BALC Trade Balanced  
or 
           
    :CPRC/ /PACK Cancel Accepted  
or 
                    
      /REJT Cancel Rejected  
or 
                    
      /CAND Cancel Processed  
or 
                    

---

## Page 57

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 57 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description IPRC// 
PACK 
IPRC// 
REJT 
IPRC/ 
GSCC/ 
RPSP 
IPRC/ 
GSCC/ 
MODA 
IPRC/ 
GSCC/ 
MDRJ 
IPRC/ 
GSCC/ 
MODP 
IPRC/ 
GSCC/ 
PADK 
IPRC/ 
GSCC/ 
DKRJ 
IPRC/ 
GSCC/ 
DPPR 
IPRC// 
DEDK 
IPRC/ 
GSCC/ 
BALC 
      GSCC/UPBP Cancel Lifted by 
[[participant]] 
(Uncancel 
processed)  
or  
                    
    :MTCH/ /MACH Trade Compared  
or 
                    
   GSCC/PSUM Trade Compared 
Through Par 
Summarization  
           
M :16R: REAS   Optional Repeat 
Block Start  
                    
M :24B: :REJT/   Reject Reason Code 
(see Appendix E)  
                 
O :70D: :REAS/ /GSCC Reject Reason 
Narrative 
                   
      /MDRJ Modify Rejected  
or 
                   
      /DKRJ DK Rejected                     
M :16S: REAS   End of Block                     
M :16S: STAT   End of Block                     
M :16S: GENL   End of Block                     
 
 
 
 

---

## Page 58

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 58 
Trade Cancel & Match 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description CPRC// 
PACK 
CPRC// 
REJT 
CPRC// 
CAND 
CPRC/ 
GSCC/ 
UPBP 
MTCH// 
MACH 
MTCH/ 
GSCC/ 
PSUM 
        Message Header            
M       Password        
M       Sender        
M       Message Type       
M       Receiver        
M :16R: GENL   Mandatory Start of 
Block 
           
M :20C: :SEME//   Sender's Message 
Reference 
      
M :23G: INST   Message Function – 
Instruct 
          
    CAST   Cancel         
O :98C: :PREP//   Preparation Date/Time       
M :16R: LINK   Repeat Block Start            
M :20C: :MAST//   Master ([[Member]])  
Reference Number 
      
M :16S: LINK   End of Block            
M :16R: LINK   Repeat Block Start            
O :20C: :PREV//   Previous Reference 
Number 
           
M :16S: LINK   End of Block            
M :16R: LINK   Repeat Block Start            

---

## Page 59

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 59 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description CPRC// 
PACK 
CPRC// 
REJT 
CPRC// 
CAND 
CPRC/ 
GSCC/ 
UPBP 
MTCH// 
MACH 
MTCH/ 
GSCC/ 
PSUM 
O :20C: :RELA//   Related Reference 
Number (Sender's 
Reference)  
         
M :16S: LINK   End of Block            
M :16R: LINK   Repeat Block Start            
O :20C: :INDX//   Secondary Reference 
Number 
      
M :16S: LINK   End of Block            
M :16R: LINK   Repeat Block Start            
O :20C: :LIST//   [[GSD]] Assigned 
Reference Number 
(Receiver’s TID)  
      
M :16S: LINK   End of Block            
M :16R: LINK   Repeat Block Start            
O :20C: :PROG//   Counterparty Reference 
Number 
          
M :16S: LINK   End of Block            
M :16R: LINK   Repeat Block Start             
O :13B: :LINK/ GSCC/CASH Linked Message – Cash 
Trade Indicator 
 or 
 
 
    
      GSCC/REPO Repo Trade Indicator  
 or 
 
 
    
   GSCC/TRLK Locked-in Cash Trade 
Indicator 
      

---

## Page 60

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 60 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description CPRC// 
PACK 
CPRC// 
REJT 
CPRC// 
CAND 
CPRC/ 
GSCC/ 
UPBP 
MTCH// 
MACH 
MTCH/ 
GSCC/ 
PSUM 
or 
   GSCC/TRLR Locked-in Repo Trade 
Indicator 
or 
      
   GSCC/TRDC Demand Cash Trade 
Indicator 
or 
      
   GSCC/TRDR Demand Repo Trade 
Indicator 
      
O :20C: :BASK//   [[Broker]] (Counterparty) 
Reference Number 
([[Broker]] Xref or [[Broker]] 
TID) 
      
M :16S: LINK   End of Block            
M :16R: STAT   Repeat Block Start            
M :25D: :IPRC/ /PACK Trade Input 
Accepted/Validated  
or  
           
      /REJT Trade, Trade Modify, or 
DK is rejected  
or  
           
      GSCC/MODA Modify Accepted  
or 
           
      GSCC/MODP Modify Processed  
or 
           
      GSCC/PADK DK Accepted             

---

## Page 61

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 61 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description CPRC// 
PACK 
CPRC// 
REJT 
CPRC// 
CAND 
CPRC/ 
GSCC/ 
UPBP 
MTCH// 
MACH 
MTCH/ 
GSCC/ 
PSUM 
or 
      GSCC/DPPR DK Processed  
or 
           
      GSCC/DEDK Trade Canceled due to 
DK 
or 
           
    :CPRC/ /PACK Cancel Accepted  
or 
          
      /REJT Cancel Rejected  
or 
          
      /CAND Cancel Processed  
or  
          
      /GSCC/UPBP Cancel Lifted by 
[[participant]] (Uncancel 
processed)  
or  
          
    :MTCH/ /MACH Trade Compared  
or 
          
   GSCC/PSUM Trade Compared 
Through Par 
Summarization  
      
M :16R: REAS   Optional Repeat Block 
Start  
           
M :24B: :REJT/   Reject Reason Code 
(see Appendix E)  
          
O :70D: :REAS/ /GSCC Reject Reason Narrative             

---

## Page 62

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT509 62 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description CPRC// 
PACK 
CPRC// 
REJT 
CPRC// 
CAND 
CPRC/ 
GSCC/ 
UPBP 
MTCH// 
MACH 
MTCH/ 
GSCC/ 
PSUM 
      /MDRJ Modify Rejected  
or 
           
      /DKRJ DK Rejected             
M :16S: REAS   End of Block            
M :16S: STAT   End of Block            
M :16S: GENL   End of Block            

---

## Page 63

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 63 
COMPARISON INTERACTIVE MESSAGE SPECIFICATIONS 
– MT518 
This section contains the detailed specifications including layout and field descriptions for MT518 Messages 
supporting comparison output for [[GSD]]’s products and services. 
MT518 Contra-Side Message Description 
The SWIFT MT518 Message is specified as a Market Side [[securities]] Trade Confirmation and will be used by 
[[GSD]] as a means to communicate full trade information to the counterparty associated with the transaction 
being reported on. This will include information relate to Instruct, Cancel, Modify and DK input messages 
submitted against the counterparty on such transactions. This contra-side trade status message will also be 
used to notify Members when their trades have been DK’d (or where previously submitted DKs have been 
removed).  
The field :22F::PROC in the Confirmation Details (CONFDET) block will indicate to the [[Member]] the record type 
being sent. Also, the field :70E:: TPRO// may indicate the reason for the event occurring preceded by the 
mnemonic MSGR (message reason). On DK messages this field will also provide the reason for the DK having 
been submitted against the recipient’s trade (preceded by the mnemonic “DKRS” (DK reason)).  
The following MT518 Messages may be generated for the products and contra-side trade status changes: 
• DVP: regular buy/sell, repo/revr, auction buy/sell 
• GCF: repo/revr (Locked-In Trade Advice, Yield to Price - Assumed Coupon, Yield to Price - Real Coupon, 
Coupon Reset (of UST FRNs), Repo Substitution Details, (Notification of) [[default]] Values Applied, Post 
Comparison Cancel Advice (of Locked-in Trade), DK Advice, DK Remove Advice [[DO]] not apply to this 
product)) 
• CCIT: repo/revr (Locked-In Trade Advice, Yield to Price - Assumed Coupon, Yield to Price - Real Coupon, 
Repo Substitution Details, (Notification of) [[default]] Values Applied, Post Comparison Cancel Advice (of 
Locked-in Trade), DK Advice, DK Remove Advice [[DO]] not apply to this product) 
 
Message Type This message will be sent to : DVP GCF  CCIT 
Comparison Request 
(:22F::PROC/GSCC/CMPR) 
the counterparty to inform the [[Member]] that a Trade Instruct 
message has been submitted against them.  
   
Comparison Request Modify 
(:22F::PROC/GSCC/CRQM) 
the counterparty to inform the [[Member]] that a Trade Modify 
message has been submitted against them on a trade that 
their awaiting comparison.  
   
Comparison Request Cancel 
(:22F::PROC/GSCC/CADV) 
the counterparty to inform the [[Member]] that a comparison 
request/advice has been canceled either due to counterparty 
action or [[GSD]].  
   

---

## Page 64

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 64 
Message Type This message will be sent to : DVP GCF  CCIT 
Locked -in Trade Advice 
(:22F::PROC/GSCC/LCTA) 
inform a [[Member]] that a trade has been booked on the 
[[Member]]’s behalf based on the submission of either a Locked -
in or Demand Trade against that [[Member]].  
This message will only be generated by [[GSD]] where a 
Locked -in or Demand trade is still available for comparison at 
end of day, as part of administrative comparison. Where a 
Locked -in Trade Advice is generated, the Locked -in, or 
Demand submitter will receive an MT518 Comparison 
Request message. 
Note:  
Where available, [[GSD]] will append the Locked -in, or Demand, 
submitter’s trade reference number to the record. (A MT509 
Trade Compared message will also be sent).  
   
Cancel Request 
(:22F::PROC/GSCC/CREQ) 
the counterparty to inform the [[Member]] that a Cancel message 
has been submitted on a compared trade they are a p arty to. 
   
Cancel Request Cancel 
(:22F::PROC/GSCC/CCRQ) 
the counterparty to inform the [[Member]] that a removal of a 
cancel request message has been submitted on trade the 
[[Member]] had already compared but was pending cancellation.
 
   
Post Comparison Cancel 
Advice (of Locked -in Trade ) 
(:22F::PROC/GSCC/PCCA) 
inform a [[Member]] that a Cancel m essage has been submitted 
against it by an authorized Locked -in submitter for a Locked -
in trade. 
The trade has been canceled unilaterally; the [[Member]] does 
not need to take any action with [[GSD]].  
   
Yield to Price – A ssumed 
Coupon (of WI trade) 
(:22F::PROC/GSCC/YTPA) 
inform all parties to a when -issued (WI) trade that the final 
money has changed based on a change in the assumed 
coupon.  
   
Yield to Price – R eal Coupon 
(of WI trade)  
(:22F::PROC/GSCC/YTPR) 
inform all parties to a when -issued (WI) trade of the 
recalculated final money based on using the real coupon 
announced at auction.  
   
Coupon Reset  (of UST FRNs)  
(:22F::PROC/GSCC/CPNR 
inform all parties to a trade in a U.S. Treasury Floating Rate 
Note of the recalculated  final money after coupon reset date 
   
Repo Substitution Details 
(:22F::PROC/GSCC/RPSD) 
provide [[collateral]] substitution details to all parties to the 
substituted repo transaction . It will reflect the new details of 
the repo transaction, such as the new quantity, security and 
final money.  
   
Trade Compared with 
Modifications 
(:22F::PROC/GSCC/CMPM) 
the parties to a trade if modifications were made to th e trade 
being reported on as part of the comparison process, e.g.  
Enhanced Matching/Phased Comparison process.  
   
Post Comparison Trade 
Modification 
(:22F::PROC/GSCC/MDAD) 
to the parties to a trade when the trade being reported on has 
been modified after comparison.  
   

---

## Page 65

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 65 
Message Type This message will be sent to : DVP GCF  CCIT 
Post Comparison Counterparty 
Trade Modification 
(:22F::PROC/GSCC/CMDA) 
the counterparty to inform the [[Member]] that a trade 
modification message was submitted on a trade that has 
already been compared.  
   
[[default]] Values Appl ied 
(:22F::PROC/GSCC/DFVA) 
to the [[Member]] if [[GSD]] has to apply [[default]] values to the trade 
details of a trade, e.g.  final money or trade date.  
   
Screen Input Trade Replay 
(:22F::PROC/GSCC/SITR) 
the [[Member]] when a trade has been added, modified, or 
canceled via screen input ( within [[GSD]] RTTM Web). 
   
DK Advice 
(:22F::PROC/GSCC/NAFI) 
to the counterparty to inform the [[Member]] that a DK has been 
submitted against them on a trade they previously submitted.  
   
DK Remove Advice 
(:22F::PROC/GSCC/DCCX) 
the counterparty to inform the [[Member]] that  that the removal 
of a DK has been submitted against them on a trade they 
previously submitted, and for which was subsequently DK’d.  
   
  
MT518 Contra-Side Message Specifications 
MT518 Contra-Side Message General Format 
This section provides the general format for the MT518 Contra-Side Message. As previously stated, this 
message type will be used by [[GSD]] to notify Members that a trade input (Instruct, Modify, Cancel or DK) has 
been submitted against them. As described in the MT518 Message Description in this document, the MT518 
will be sent by [[GSD]] to the [[Member]] for the following events: 
• Comparison Request 
• Comparison Request Modify 
• Comparison Request Cancel 
• Locked-in Trade Advice 
• Cancel Request 
• Cancel Request Cancel 
• Post Comparison Cancel Advice (of Locked-in Trade) 
• Yield to Price – Assumed Coupon (of WI trade) 
• Yield to Price – Real Coupon (of WI trade) 
• Coupon Reset (of UST FRNs) 
• Repo Substitution Details 
• Trade Compared with Modifications 
• Post Comparison Trade Modification 
• Post Comparison Counterparty Trade Modification 
• [[default]] Values Applied 
• Screen Input Trade Replay 
• DK Advice 
• DK Remove Advice 

---

## Page 66

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 66 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format DVP GCF CCIT 
        Message Header      
M       Password  12!c    
M       Sender  8!c    
M       Message Type 3!n/3!n/4!c     
M       Receiver  8!c    
M :16R: GENL   Mandatory Start of 
Block 
     
M :20C: :SEME//   Sender's Message 
Reference 
16x    
M :23G: NEWM   Function of the Message 
– New 
or 
4!c    
    CANC   Cancel lation Request       
O :98C: :PREP//   Preparation Date/Time YYYYMMDDHHMMSS    
M :22F: :TRTR/ GSCC/CASH Trade Transaction Type –  
Cash Trade Indicator  
or 
 4!c    
   GSCC/REPO Repo Trade Indicator  
or 
    
   GSCC/TRLK Locked -in Cash Trade 
Indicator  
or 
    
   GSCC/TRLR Locked -in Repo Trade 
Indicator  
 or 
    
   GSCC/TRDC Demand Cash  Trade 
Indicator  
or 
    
      GSCC/TRDR Demand Repo Trade 
Indicator  
4!c    
M :16R: LINK   Optional Repeat Block 
Start 
     
M :20C: :MAST//   Master ([[Member]])  
Reference Number 
16x    
M :16S: LINK   End of Block      
M :16R: LINK   Repeat Block Start      
O :20C: :PREV//   Previous Reference 
Number 
16x    

---

## Page 67

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 67 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format DVP GCF CCIT 
M :16S: LINK   End of Block      
M :16R: LINK   Repeat Block Start      
O :20C: :LIST//   [[GSD]] Reference Number  16x    
M :16S: LINK   End of Block      
M :16R: LINK   Repeat Block Start      
O :20C: :BASK//   [[Broker]] (Counterparty) 
Reference Number 
([[Broker]] Xref) 
16x    
M :16S: LINK   End of Block      
M :16S: GENL   End of Block      
M :16R: CONFDET   Mandatory Start of 
Block 
     
M :98C: :TRAD//   Trade Date & Time YYYYMMDDHHMMSS    
M :98A: :SETT//   [[settlement]] Date (or Start 
Leg [[settlement]] Date if 
REPO)  
YYYYMMDD     
M :90A: :DEAL/ /PRCT/ Deal Price – Percentage 
or 
15d    
   /YIEL/ Yield  
or 
[N]15d    
   /DISC/ Discount  15d    
O :19A: :SETT/ /USD [[settlement]] Amount (or 
Start Leg [[settlement]] 
Amount if REPO)  
15d    
M :22H: :BUSE/ /BUYI Trade Type – Buy 
(REVR) 
or 
4!c    
      /SELL Sell (REPO)      
O :22F: :PROC/ GSCC/CMPR Processing Indicator – 
Comparison Request  
or 
4!c    
      GSCC/CRQM Comparison Request 
Modify  
or 
     
      GSCC/CADV Comparison Request 
Cancel  
or 
     

---

## Page 68

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 68 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format DVP GCF CCIT 
   GSCC/LCTA Locked -in Trade Advice  
or 
    
      GSCC/CREQ Cancel Request  
or 
     
      GSCC/CCRQ Cancel Request Cancel  
or 
     
   GSCC/PCCA Post Comparison Cancel 
Advice (of Locked -in 
Trade)   
or 
    
   GSCC/YTPA Yield to Price (Assumed 
Coupon)  
or 
    
   GSCC/YTPR Yield to Price (Real 
Coupon)  
or 
    
   GSCC/CPNR Coupon Reset  (of UST 
FRNs)                          
or 
    
   GSCC/RPSD Repo Substitution Details  
or 
    
      GSCC/CMPM Trade Compared with 
Modifications  
or 
     
      GSCC/MDAD Post Comparison Trade 
Modification  
or 
     
      GSCC/CMDA Post Comparison 
Counterparty  Trade 
Modification  
or 
     
      GSCC/DFVA [[default]] Values Applied  
or 
     
      GSCC/SITR Screen Input Trade 
Replay  
or 
     
      GSCC/NAFI DK Advice  
or 
     
      GSCC/DCCX DK Remove Advice             
M :22H: :PAYM/ /APMT Against Payment 
Indicator – vs. Payment  
4!c    

---

## Page 69

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 69 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format DVP GCF CCIT 
M :16R: CONFPRTY   Mandatory Repeat Start 
of Block 
     
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]] 34x    
O :20C: :PROC//   Processing Reference – 
[[Buyer]] ( Counterparty ) X-
ref 
16x    
O :70E: :DECL/ /GSCC Declaration Details 
Narrative 
(10*35x)    
      /PREV [[Buyer]] ( Counterparty ) 
Previous X-ref 
16x    
      /CORR Party = [[Buyer]]’s 
Executing firm  
5c    
O :70C: :PACO/ /GSCC Party Narrative (4*35x)    
      /TDID [[Buyer]] ( Counterparty ) 
Trader [[ID]] 
20c    
M :16S: CONFPRTY   End of Block      
M :16R: CONFPRTY   Mandatory Repeat Start 
of Block 
     
M :95R: :SELL/ GSCC/PART Party = [[Seller]]  34x    
O :20C: :PROC//   Processing Reference – 
[[Seller]] (Counterparty ) X-
ref 
16x    
O :70E: :DECL/ /GSCC Declaration Details 
Narrative 
(10*35x)    
      /PREV [[Seller]] (Counterparty ) 
Previous X-ref 
16x    
      /CORR Party = [[Seller]]’s Executing 
firm 
5c    
  :70C: :PACO/ /GSCC Party Narrative (4*35x)    
      /TDID [[Seller]] (Counterparty ) 
Trader [[ID]] 
20c    
M :16S: CONFPRTY   End of Block      
M :36B: :CONF/ FAMT/ Quantity of Face Amount 
(Par)  
15d    
M :35B: /US/   Identification of Financial 
Instrument/ Security 
([[CUSIP]]) 
(4*35x)    

---

## Page 70

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Out put 
Comparison Interactive M essage Specifications  – MT518 70 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format DVP GCF CCIT 
O :70E: :TPRO/ /GSCC Trade Instruction 
Processing Narrative  
(10*35x)    
      /MSGR Message Reason (see 
Appendix E)  
4!c    
      /DKRS DK Reason (see 
Appendix E)  
4!c    
M :16S: CONFDET   End of Block      
M :16R: SETDET   Optional Start of Block        
M :22F: :SETR /RPTO [[settlement]] Transaction 
Indicator  
4!c    
M :16R: AMT   Optional Start of Block        
O :17B: :STAN/ /N Standing Instruction 
Override = No  
1!a    
M :19A: :LOCO/ /USD [[Broker]]’s Commission  15d    
M :16S: AMT   End of Block      
M :16S: SETDET   End of Block      
M :16R: REPO   Optional Start of Block        
O :98A: :REPU//   End Leg [[settlement]] Date YYYYMMDD    
O :20C: :SECO//   Secondary Reference 
Number 
16x    
O :92A: :REPO//   Repo Rate [N]15d    
O :19A: :REPA// /USD End Leg [[settlement]] 
Amount 
15d    
M :16S: REPO   End of Block      
  

---

## Page 71

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 71 
MT518 Contra-Side Message Field Specifications 
This section provides the detailed field specifications for the MT518 Message.   
Block/Tag Notes 
Message 
Header 
Each message must contain a Message Header. All header fields are mandatory fixed format with 
trailing blanks, where required.  
Password 12!c This field will be  blank -filled on MT518 messages. 
Sender 8!c “GSCCTRRS” ([[GSD]] Trade Registration and Reconciliation System) for DVP, 
“GCFCTRRS” (GCF Trade Registration and Reconciliation System) for GCF/CCIT 
will always be the sender of the MT518 messages in this document.  
Message 
Type 
3!n/3!n/4!c  The first 3 charac ters indicate to the recipient the message type (518); the second 3 
positions reflect the version of the message interface (currently always 000); the last 
4 characters indicate the [[issuer]] code to be used in the message (GSCC).  
Receiver 8!c [[Member]] [[ID]] 
GENL This mandatory block provides general information regarding the message. It appears only once 
in a trade confirm.  
20C Sender's Message Reference 
• SEME// – This mandatory field contains the sender’s ([[GSD]]) message reference number. It is 
used on all messages and will contain a unique number to unambiguously identify each 
message sent by [[GSD]]. This is a communications message number, not a trade number.  
e.g., :20C::SEME//2019GSDCMPMESS1 
Note:  
This field must be populated with an uppercase alphanumeric value. It cannot contain symbols or 
hyphens.  
 
23G Function of the Message 
This mandatory field is used on all messages to identify the function of the message. It will either be a 
new message (NEWM) related to an Instruct, Modify or DK, or the cancellation of a previous trade 
(CANC). 
• NEWM – This qualifier will be used for a new trade, a trade modification, or a DK message.  
• CANC – This qualifier will be u sed for various cancellation messages.  
e.g., :23G:NEWM   
98C Preparation Date and Time 
• PREP// – This field will be reflected on all messages to indicate the date and time the message 
sent by [[GSD]] was prepared.  
e.g., :98C::PREP//20191124113533 
Note:  
The “C” Format for this (98) tag indicates a Date/Time Format of “YYYYMMDDHHMMSS”.  
 

---

## Page 72

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 72 
Block/Tag Notes 
22F Trade Transaction Type Indicator (TRTR)  
This field specifies that the trade is being reported as a Repo and whether the trade is Demand or 
requires bilateral comparison.  
• TRTR/GSCC/CASH – This qualifier/[[Option]] should be used on buy/sell trades requiring two - 
sided (Bilateral) comparison.  
• TRTR/GSCC/REPO – This qualifier/[[Option]] should be used on repo trades requiring Bilateral 
comparison.  
• TRTR/GSCC/TRLK – This qualifier/[[Option]] should be us ed on Locked- in cash trades.  
• TRTR/GSCC/TRLR – This qualifier/[[Option]] should be used on Locked -in repo trades.  
• TRTR/GSCC/TRDC – This qualifier/[[Option]] should be used on Demand cash trades.  
• TRTR/GSCC/TRDR – This qualifier/[[Option]] should be used on Demand repo t rades.  
e.g., :22F::TRTR/GSCC/TRDR 
LINK The LINK Block can be repeated for as many reference qualifiers as need to be included in a 
Trade Confirm. It is intended to provide the required information to identify the trade. Each 
reference number must be enclosed within a Start Link Block (:16R:LINK) and End Link Block 
(:16S:LINK). Each LINK repeating subsequence is within the GENL Block.  
20C Reference 
This set of fields in the MT518 will contain the relevant reference numbers associated with your trade. 
The four types of reference numbers that may appear in the LINK block are:  
1) the Master Reference Number (MAST), generally referred to as the external reference number 
or x-ref 
2) the Previous Reference Number for the trade (PREV)  
3) the [[GSD]] Reference Number (LIST), also referred to as the Trade [[ID]] or TID   
4) the [[Broker]] Reference Number (BASK). 
The data provided in these reference number fields for any given trade are determined based upon a 
number of criteria. These include submitter type ([[Broker]], dealer or Locked -in submitter), message 
category (advisory, Locked -in Trade advices or advices referring to trades submitted by the message 
receiver (“your trades”), and message type (Cancel, Modify, etc.). The [[BASIC]] rules for reporting data for 
each reference num ber type are provided below.  
It should be noted that, on MT518 Advisories, where counterparty  trade reference numbers are provided, 
the counterparty ’s external as well as previous reference numbers will appear in the appropriate [[Buyer]] or 
[[Seller]] Confirming Party Subsequence. They will not appear in this subsequence.  
• MAST// – Master Reference Number  - On advices referring to the receiving [[Member]]’s ( your ) 
trades, this field will contain your external reference number. On Locked -in Trade Advices 
supporting Lock ed-in or Demand trades, this field will contain the external reference number 
generated by [[GSD]] on your behalf. This field will not appear on advisories.  
• PREV// – Previous Reference Number  - Under most circumstances, this field will not appear 
on MT518’s (advisories, Locked -in Trade advices, or advices referring to the receiving 
[[Member]]’s ( your ) trades).  
o One exception to this rule is for Cancels. There is a SWIFT requirement that the data 
field associated with the “PREV” qualifier be populated on all MT518 and MT515 
cancel (:23G:CANC) records. All MT518 Cancel records will therefore reflect the PREV 
qualifier populated with the value “NONREF”.  
o The second exception to this rule is for Screen Input Trade Replay Records 
(:22F::PROC/GSCC/SITR) where the [[Member]] ha s made entries on a [[GSD]] terminal. 

---

## Page 73

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 73 
Block/Tag Notes 
For these trades, the data field associated with the PREV qualifier will be populated as 
follows:  
 If the screen input was a trade cancellation, the data field associated with the 
PREV qualifier will be populated with “NONR EF”. 
 If the screen input was a trade modification, which included the modification 
of an external reference number, the data field associated with the PREV 
qualifier will contain the [[Member]]’s Previous External Reference Number.  
 At this point in time, this field will not appear under any other circumstances.  
As indicated above, if the counterparty  has changed its external reference number, the 
counterparty ’s previous reference number will appear.  
• LIST// – [[GSD]] Reference Number  – On Locked -in trade advices, for Locked -in or Demand 
trades, and advices referring to the receiving [[Member]]’s ( your ) trades, this field will contain the 
[[GSD]] Assigned Reference Number (TID) for the trade. This field will not appear on advisories.  
• BASK// – [[Broker]] Reference Number  - For trades submitted by brokers, this field will contain 
the [[Broker]]’s Reference Number on advices, referring to the [[Broker]]’s trade. This field will not 
appear on advisories or Locked- in trade advices.  
e.g., :20C::MAST//PARTREF2019 
Note:  
This field must be populated with an uppercase alphanumeric value. It will not contain symbols or 
hyphens except where the reference number has been assigned by [[GSD]].                                                                                                                                
CONFDET The CONFDET (Confirmation Details) block appears only once in a Trade Contract. It contains 
Trade and Confirming Party Details.  
98C Trade Date 
• TRAD// – This field is used on all messages to specify Trade Date and Trade Time. (The “C” 
format for this (98) tag indicates a Date/Time Format of “YYYYMMDDHHMMSS”.)  
e.g., :98C::TRAD//20191125105153 
98A [[settlement]] Date 
• SETT// – This field is used on all messages to specify the [[settlement]] Date for a cash trade, or 
the Start Leg [[settlement]] Date, in case of a repo. The “A” Format for this tag (98) indicates a 
Date Format of “YYYYMMDD”. 
e.g., :98A::SETT//20191124 
90A Deal Price 
This field is reflected on all MT518 messages. It contains the Execution Price Type and Price. Only one 
Tag 90A is allowed per trade contract. The following price types may be specified:  
• DEAL//PRCT/ – This qualifier/[[Option]] is used for dollar prices a nd repo rates. Where the trade is 
a repo, however, the price portion of the field must be populated with “0,”. Repo rates can be 
found in the REPO Block.  
• DEAL//YIEL/ – This qualifier/[[Option]] is used for Yield priced trades.  
• DEAL//DISC/ – This qualifier/opti on is used for Discount Rates.  
e.g., :90A::DEAL//PRCT/0  

---

## Page 74

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 74 
Block/Tag Notes 
Note:  
The [[GSD]] system supports a size of 14d. The field should only be populated with a value no larger than 
14d. 
 
19A [[settlement]] Amount  
• SETT// – This field is used to specify the [[settlement]] Amount for buy/sell trades and the Start  
Leg [[settlement]] Amount for Repo trades.  
The amount is left justified, with commas removed, and a comma used instead of a decimal. 
The amount is always preceded by the ISO  3-character Currency Code (“USD” for [[GSD]] 
Trades).  
For repo trades, this field must be populated with the Start  Leg [[settlement]] Amount. 
e.g., :19A::SETT//USD51000000, 
Note:  
This field can accommodate a value of 15d.  
 
22H Trade Type Indicator (BUSE)  
This field is required on all messages and has two allowable values for this BUSE qualifier:  
• BUSE//BUYI – This qualifier/[[Option]] indicates that the record represents either a buy, in the case 
of a cash trade, or a reverse, in the case of a repo trade.  
• BUSE//SELL – This qualifier/[[Option]] indicates that the record represents either a sell, in the case 
of a cash trade, or a repo, in the case of a repo trade.  
e.g., :22H::BUSE//BUYI 
Note:  
The inclusion of a REPO block and the use of a Repo qualifier in Tag 22F (TRTR/GSCC/REPO, 
TRTR/GSCC/TRLR or TRTR/GSCC/TRDR) in the GENL block will indicate that the trade is a repo trade, 
rather than a cash trade.  
 
22F Processing Indicator (PROC)  
This processing indicator enables [[GSD]] to indicate to the [[Member]] the type of record/command being 
submitted on this MT518. The allowable values for this field are:  
• PROC/GSCC/CMPR – This qualifier/[[Option]] indicates that the MT518 record is a Comparison 
Request. 
• PROC/GSCC/CRQM –This qualifier/[[Option]] indicates that the MT518 record is a Comparison 
Request Modify.  
• PROC/GSCC/CADV - This qualifier/[[Option]] indicates that the MT518 record is a Comparison 
Request Cancel Advice (previously called a Pre- comparison Cancel Advice).  
• PROC/GSCC/LCTA – This qualifier/[[Option]] indicates that the MT518 record is a Locked -in Trade 
Advice.  
• PROC/GSCC/CREQ – This qualifier/[[Option]] indicates that the MT518 record is a Cancel 
Request (of an already compared trade).  
• PROC/GSCC/CCRQ – This qualifier/[[Option]] indicates that the MT518 record is for a Cancel 
Request Canc el. 
• PROC/GSCC/PCCA – This qualifier/[[Option]] indicates that the MT518 record is a Post 
Comparison Cancel Advice of a Locked- in Trade.  

---

## Page 75

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 75 
Block/Tag Notes 
• PROC/GSCC/YTPA – This qualifier/[[Option]] indicates that the MT518 record is a Yield to Price  
recalculation using an assumed co upon.   
• PROC/GSCC/YTPR – This qualifier/[[Option]] indicates that the MT518 record is a Yield to Price 
recalculation using the real coupon.  
• PROC/GSCC/CPNR – This qualifier/[[Option]] indicates that the MT518 record is a U.S. Treasury 
Floating Rate Note r ecalculation after coupon reset date. 
• PROC/GSCC/RPSD – This qualifier/[[Option]] indicates that the MT518 record is for providing 
Repo Substitution Details.   
• PROC/GSCC/CMPM – This qualifier/[[Option]] indicates that the MT518 record is a Compared with 
Modifications.  
• PROC/GSCC/MDAD – This qualifier/[[Option]] indicates that the MT518 record is a Post 
Comparison Trade Modification (recipient’s trade).  
• PROC/GSCC/CMDA – This qualifier/[[Option]] indicates that the MT518 record is a Post 
Comparison Counterparty  Trade Modification.  
• PROC/GSCC/DFVA – This qualifier/[[Option]] indicates that the MT518 record is for [[default]] Values 
Applied.  
• PROC/GSCC/SITR – This qualifier/[[Option]] indicates that the MT518 record is for Screen Input 
Trade Replay.  
• PROC/GSCC/NAFI – This qualifier/[[Option]] indicates that the MT518 r ecord is for a DK Advice 
(DK of the recipient’s previously submitted trade).  
• PROC/GSCC/DCCX – This qualifier/[[Option]] indicates that the MT518 record is for DK Remove 
Advice (removing the DK status from the recipient’s trade).  
e.g., :22F::PROC/GSCC/CMPR 
 
22H Payment Indicator (PAYM)  
This Payment indicator field is mandatory for the MT518 message. All MT518 records will reflect the 
following tag/qualifier:  
• PAYM//APMT – This qualifier/[[Option]] indicates that the trade will settle against  payment.  
e.g., :22H::PAYM//APMT 
36B Quantity of [[securities]] (CONF) 4 
• CONF//FAMT/ – This field is mandatory, and for the purposes of [[GSD]], must use the [[Option]] 
‘FAMT’ - indicating face amount (par). The quantity of the financial instrument is left justified, 
with commas removed, and a comma used instead of a decimal.  
e.g., :36B::CONF//FAMT /25000000, 
Note:  
This field can accommodate a value of 15d.  
 
35B Identification of Financial Instrument/Security ([[CUSIP]]) 4 
The security/[[collateral]] involved is identified in the US by specifying the ISO country identifier (‘/US/’), 
followed by the [[CUSIP]] number.  
e.g., :35B:/US/9128282A7 
 
4
 Tags 35B and 36B::TPRO// in the CONFDET block must be placed on the message following the confirming party subsequences . 

---

## Page 76

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 76 
Block/Tag Notes 
Note:  
This field will only populate a value of 9!c (alpha numeric) for the [[CUSIP]].  
 
70E Trade Instruction Processing Narrative (TPRO) 5 
This field is intended to reflect transaction related information not supported by the MT515 layout. It will 
be used on all MT515 DK messages to reflect the reason for the DK.  
• TPRO//GSCC – denotes narrative trade instruction processing information related to [[GSD]].  
• /MSGR – will be used to indicate the message reason.  
• /DKRS – will be used to indicate the reason for the DK message.  
e.g., :70E::TPRO//GSCC/MSGRMACH  
Note: 
Reason codes can be found in Appendix E of this document.  
 
CONFPRTY The Confirming Party Block must be repeated for each party to a trade. Each party specified must 
be enclosed within a start party block (:16R:CONFPRTY) and end party block (:16S:CONFPRTY). 
Please note that on every MT518 record there will be at least two (one [[Buyer]] and one [[Seller]]) 
repeating Confirming Party sequences.  
95R Party 
• BUYR/GSCC/PART – specifies the [[Buyer]] or Reverse Party (the “GSCC” [[issuer]] code allows the 
specification to reflect the [[GSD]] [[Member]] or counterparty  [[ID]], depending on who is acting as 
[[Buyer]] or [[Seller]]).  
• SELL/GSCC/PART – specifies the [[Seller]] or Repo Party.  
e.g., :95R::BUYR/GSCC/PART9XX1 
Note:  
The [[Member]] must populate the field with the appropriate qualifier and 4- character [[Member]] [[ID]], for [[Buyer]] 
or [[Seller]].  
20C Processing Reference 
• PROC// – Processing Reference Number  – This field will reflect the Counterparty  Reference 
in the appropriate [[Buyer]] or [[Seller]] confirming party subsequence. It will only appear on MT518 
Advisory and Locked -in Trade Advice records.  
e.g., :20C::PROC//CPREF4523 
70E Declaration Details Narrative (DECL)  
This field will be used in each MT518 subsequence to identify the Counterparty ’s Previous Reference 
number (where the Counterparty  has changed their External Reference Number) and/or the [[Buyer]]’s 
and/or [[Seller]]’s executing firm, where applicable.  
• DECL//GSCC – denotes declaration narrative information specific to [[GSD]].  
• /PREV – will be used in the BUYR or SELL confirming party sequence to indicate the Previous 
Counterparty  External Reference Number on a Trade Modification Advisory (Comparison 
Request Modify or Post Comparison Counterparty  Modification Advice). Where this field is 
populated, this communicates to the recipient of the MT518 that the Counterparty’s  X-ref has 
 
5 Tag 70E::TPRO// in the CONFDET block must be placed on the message following the confirming party subsequences.    

---

## Page 77

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 77 
Block/Tag Notes 
changed. The recipient should use this reference number to [[Locate]] the original advisory/trade 
that has changed. Where this field is populated, the current X -ref will always be in the field 
described above (:20C::PROC).  
• /CORR – will be used in the BUYR and/or SELL confirming party sequence(s) to indicate the 4- 
or 5-character symbol(s) for the applicable [[Buyer]] and/or [[Seller]]’s executing firm(s). Where there 
is no Previous External Reference Number or Executing [[Broker]] for either the [[Buyer]] or [[Seller]] 
confirming party, this field will not appear on the MT518 record.  
Where there is no Previous External Reference Number or applicable submitter  for either the [[Buyer]] or 
[[Seller]] confirming party, this field will not appear on the MT518 record.  
e.g., :70E::DECL//GSCC/CORREXECFIRM12 
Note:  
While this field can support a narrative 10 * 35x, the [[Member]], at this time, will only receive the above 
qualifie rs and the 16-character Previous Reference Number and/or the [[GSD]] assigned executing firm 
symbol  in this field. In the future this field can be used to support additional information related to the 
[[Buyer]] and/or [[Seller]], where required.                                                                                                   
70C Party Narrative (PACO)  
This field will be used in the appropriate [[Buyer]] or [[Seller]] confirming party sequence on MT518 messages 
to provide infor mation regarding the individual/desk that executed the trade.  
• PACO//GSCC – denotes [[Member]] contact narrative information specific to [[GSD]].  
• /TDID – will be used in the appropriate [[Buyer]] or [[Seller]] sequence to indicate the following:  
o on MT518’s sent to the trade submitter, this will represent the counterparty ’s trader [[ID]]. 
o on MT518 advisories, this will represent the recipient’s trader [[ID]].  
e.g., :70C::PACO//GSCC/TDIDGEO518 
SETDET This block, and the AMT subsequence, are necessary only when [[Broker]] commission is specified 
on the trade. Currently, [[GSD]] accepts commission on WI trades for coupon bearing instruments 
submitted prior to auction, or on Repo trades.  
22F [[settlement]] Transaction Indicator (SETR) 
This field is mandatory for the Block.  
• SETR//RPTO – Indicates that this trade confirmation is for reporting purposes only.  
e.g., :22F::SETR//RPTO  
Note: 
This field is not used by [[GSD]] although it is SWIFT mandatory in order to support the inclusion of the 
Commission Amount field.  
AMT As indicated above, this sequence is only necessary to support the inclusion of [[Broker]] 
commission on a WI trade, or a Commission Amount on Repo trades. This block will a lways be 
included in the [[settlement]] Details (SETDET) block.  
17B Standing Instructions Override  
This field is mandatory for the Block.  
• STAN//N – This indicates that standing instructions should not be overridden.  
e.g., :17B::STAN//N  

---

## Page 78

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 78 
Block/Tag Notes 
Note: 
This field is not used by [[GSD]] although it is SWIFT mandatory in order to support the inclusion of the 
Commission Amount field.  
19A [[Broker]]’s Commission  
• LOCO//USD – This field specifies the [[Broker]]’s commission amount on WI trades or Repo 
trades. The commission amount field is left justified, with commas removed, and a comma used 
in lieu of a decimal. The amount must be preceded by a 3- character ISO currency code.  
e.g., :19A::LOCO//USD40,  
Note:  
The value in this field is an AMOUNT - this differs from the rate field format within the [[GSD]] system. The 
Commission Amount per trade should be included in this field – e.g., where the commission is $40 per 
million, for a two million dollar trade the field should be displayed “LOCO//USD80,”.  
Note:  
The commission amount submitted for a Repo trade should not be included in the net money.  
REPO The Repo Block appears only on trade confirm involving a repurchase/reverse repurchase trade. 
It appears only once in the confirm. Its inclusion indicates that the trade is either a Repo or 
Reverse trade based on the BUY/SELL indicator in the CONFDET Block (BUYI = Reverse, SELL = 
Repo). 
98A Repurchase Date 
• REPU// – This Mandatory field specifies the Repo End Leg [[settlement]] Date in the format 
“YYYYMMDD”. 
e.g., :98A::REPU//20191127  
20C Secondary Reference 
• SECO// – This field is optional, but if used, should include the qualifier “SECO” to support an 
additional reference number for the [[Member]]’s REPO trade. This field will be populated on 
MT518 records related to your trade, and where included on the MT518, will refl ect your 
Secondary Reference Number. Advisories will not reflect the Counterparty  Secondary 
Reference Number. 
e.g., :20C::SECO//2NDREFNUM 
Note:  
This field must be populated with an uppercase alphanumeric value. It cannot contain symbols or 
hyphens.  
 
92A Repo Rate 
• REPO// – The Mandatory REPO Rate field is left justified, with a comma inserted in lieu of a 
decimal.  
e.g., :92A::REPO//2,75 

---

## Page 79

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 79 
Block/Tag Notes 
Note:  
The [[GSD]] system supports a size of 14d. The field should only be populated with a value no larger than 
14d. 
 
19A Repurchase Amount  
• REPA// – The End Leg [[settlement]] Amount  is always prefixed by the ISO currency code (USD) 
and is left-justified with commas removed, and a comma used in lieu of a decimal.  
e.g., :19A::REPA//USD26075000, 
Note:  
This field can accommodate a value of 15d.  
 
 
 
 
 
 
 
  

---

## Page 80

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 80 
MT518 Contra-Side Message Field Analysis 
This section contains an analysis of the fields that may be found on each MT518 Contra-Side Trade Status Message. The analysis is separated into two 
categories; 1) Advisories and Locked-in Advices and 2) Advices Referring to Receiving [[Member]]’s (Your) Trades. For each applicable record type, a 
check mark will be found where it is possible for that field to appear on that record. It should be noted, however, that where a check mark appears, the 
check mark is not intended to indicate that a field is mandatory for a given record type. Where there is no check mark in a given box, that field is not 
applicable for the record type in question. 
Advisories and Locked-in Advices 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CMPR 
PROC/ 
GSCC/ 
CRQM 
PROC/ 
GSCC/ 
CADV 
PROC/ 
GSCC/ 
CMDA 
PROC/ 
GSCC/ 
LCTA 
PROC/ 
GSCC/ 
PCCA 
        Message Header           
M       Password        
M       Sender        
M       Message Type       
M       Receiver        
M :16R: GENL   Mandatory Start of 
Block 
          
M :20C: :SEME//   Sender's Message 
Reference 
      
M :23G: NEWM   Function of the Message 
– New 
or 
  
 
  
 
    CANC   Cancel           
O :98C: :PREP//   Preparation Date/Time       

---

## Page 81

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 81 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CMPR 
PROC/ 
GSCC/ 
CRQM 
PROC/ 
GSCC/ 
CADV 
PROC/ 
GSCC/ 
CMDA 
PROC/ 
GSCC/ 
LCTA 
PROC/ 
GSCC/ 
PCCA 
M :22F: :TRTR/ GSCC/CASH Trade Transaction Type 
– Cash Trade Indicator                   
or 
     
 
   GSCC/REPO Repo Trade Indicator            
or 
      
   GSCC/TRLK Locked -in Cash Trade 
Indicator  
or 
      
   GSCC/TRLR Locked -in Repo Trade 
Indicator  
or 
      
   GSCC/TRDC Demand Cash Trade 
Indicator  
or 
      
   GSCC/TRDR Demand Repo Trade 
Indicator  
      
M :16R: LINK   Optional Repeat Block 
Start 
          
M :20C: :MAST//   Master ([[Member]])  
Reference Number 
         
M :16S: LINK   End of Block     
 
    
M :16R: LINK   Repeat Block Start            
O :20C: :PREV//   Previous Reference 
Number 
         
M :16S: LINK   End of Block 
   
  
 
M :16R: LINK   Repeat Block Start            

---

## Page 82

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 82 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CMPR 
PROC/ 
GSCC/ 
CRQM 
PROC/ 
GSCC/ 
CADV 
PROC/ 
GSCC/ 
CMDA 
PROC/ 
GSCC/ 
LCTA 
PROC/ 
GSCC/ 
PCCA 
O :20C: :LIST//   [[GSD]] Assigned 
Reference Number 
(Receiver’s TID)  
         
M :16S: LINK   End of Block 
   
  
 
M :16R: LINK   Repeat Block Start            
O :20C: :BASK//   [[Broker]] (Counterparty) 
Reference Number 
([[Broker]] Xref) 
          
M :16S: LINK   End of Block           
M :16S: GENL   End of Block           
M :16R: CONFDET   Mandatory Start of 
Block 
          
M :98C: :TRAD//   Trade Date & Time       
M :98A: :SETT//   [[settlement]] Date (or 
Start Leg [[settlement]] 
Date if REPO)  
      
M :90A: :DEAL/ /PRCT/ Deal Price – Percentage        
or   
      
   /YIEL/ Yield                   
or 
      
   /DISC/ Discount        
O :19A: :SETT/ /USD [[settlement]] Amount (or 
Start Leg [[settlement]] 
Amount if REPO)  
      
M :22H: :BUSE/ /BUYI Trade Type - Buy 
(REVR) 
      

---

## Page 83

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications – MT518 83 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CMPR 
PROC/ 
GSCC/ 
CRQM 
PROC/ 
GSCC/ 
CADV 
PROC/ 
GSCC/ 
CMDA 
PROC/ 
GSCC/ 
LCTA 
PROC/ 
GSCC/ 
PCCA 
or 
      /SELL Sell (REPO)       
O :22F: :PROC/ GSCC/CMPR Processing Indicator – 
Comparison Request                  
or 
       
 
      GSCC/CRQM Comparison Request 
Modify  
or 
         
      GSCC/CADV Comparison Request 
Cancel  
or 
         
   GSCC/LCTA Locked -in Trade Advice  
or 
      
      GSCC/CREQ Cancel Request                           
or 
          
      GSCC/CCRQ Cancel Request Cancel  
or 
          
   GSCC/PCCA Post Comparison 
Cancel Advice (of 
Locked in Trade)  
or 
      
   GSCC/YTPA Yield to Price (Assumed 
Coupon) of WI Trade  
or 
      
   GSCC/YTPR Yield to Price (Real 
Coupon) of WI Trade  
or 
      
   GSCC/CPNR Coupon Reset  (of UST 
FRNS)                          
or 
      

---

## Page 84

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 84 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CMPR 
PROC/ 
GSCC/ 
CRQM 
PROC/ 
GSCC/ 
CADV 
PROC/ 
GSCC/ 
CMDA 
PROC/ 
GSCC/ 
LCTA 
PROC/ 
GSCC/ 
PCCA 
   GSCC/RPSD Repo Substitution 
Details  
or  
      
      GSCC/CMPM Trade Compared with 
Modifications                                                    
or 
          
      GSCC/MDAD Post Comparison Trade 
Modification                                 
or 
          
      GSCC/CMDA Post Comparison 
Counterparty  Trade 
Modification                                 
or 
        
 
      GSCC/DFVA [[default]] Values Applied                
or 
          
      GSCC/SITR Screen Input Trade 
Replay  
or 
          
      GSCC/NAFI DK Advice                                   
or 
          
      GSCC/DCCX DK Remove Advice                  
M :22H: :PAYM/ /APMT Against Payment 
Indicator – vs. Payment  
      
M :16R: CONFPRTY   Mandatory Repeat 
Start of Block 
         
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]]       
O :20C: :PROC//   Processing Reference – 
[[Buyer]] ( Counterparty ) X-
ref 
     
 

---

## Page 85

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 85 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CMPR 
PROC/ 
GSCC/ 
CRQM 
PROC/ 
GSCC/ 
CADV 
PROC/ 
GSCC/ 
CMDA 
PROC/ 
GSCC/ 
LCTA 
PROC/ 
GSCC/ 
PCCA 
O :70E: :DECL/ /GSCC Declaration Details 
Narrative 
          
      /PREV [[Buyer]] ( Counterparty ) 
Previous X-ref 
       
 
      /CORR Party = [[Buyer]]’s 
Executing firm  
      
O :70C: :PACO/ /GSCC Party Narrative           
      /TDID [[Buyer]] ( Counterparty ) 
Trader [[ID]] 
      
M :16S: CONFPRTY   End of Block 
   
  
 
M :16R: CONFPRTY   Mandatory Repeat 
Start of Block  
   
  
 
M :95R: :SELL/ GSCC/PART Party = [[Seller]]        
O :20C: :PROC//   Processing Reference – 
[[Seller]] (Counterparty ) X-
ref 
     
 
O :70E: :DECL/ /GSCC Declaration Details 
Narrative 
   
  
 
      /PREV [[Seller]] (Counterparty ) 
Previous X-ref 
       
 
      /CORR Party = [[Seller]]’s 
Executing firm  
      
  :70C: :PACO/ /GSCC Party Narrative 
   
  
 
      /TDID [[Seller]] (Counterparty ) 
Trader [[ID]] 
      
M :16S: CONFPRTY   End of Block 
   
  
 

---

## Page 86

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 86 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CMPR 
PROC/ 
GSCC/ 
CRQM 
PROC/ 
GSCC/ 
CADV 
PROC/ 
GSCC/ 
CMDA 
PROC/ 
GSCC/ 
LCTA 
PROC/ 
GSCC/ 
PCCA 
M :36B: :CONF/ FAMT/ Quantity of Face 
Amount (Par)  
      
M :35B: /US/   Identification of 
Financial Instrument/  
Security ([[CUSIP]]) 
      
O :70E: :TPRO/ /GSCC Trade Instruction 
Processing Narrative  
          
      /MSGR Message Reason (see 
Appendix E)  
      
      /DKRS DK Reason (see 
Appendix E)  
          
M :16S: CONFDET   End of Block       
M :16R: SETDET   Optional Start of Block             
M :22F: :SETR /RPTO [[settlement]] Transaction 
Indicator (Reporting 
Purposes)  
      
M :16R: AMT   Optional Start of Block             
O :17B: :STAN/ /N Standing Instruction 
Override = No  
      
M :19A: :LOCO/ /USD [[Broker]]’s Commission        
M :16S: AMT   End of Block 
   
  
 
M :16S: SETDET   End of Block           
M :16R: REPO   Optional Start of Block   
   
  
 
O :98A: :REPU//   End Leg [[settlement]] 
Date 
      

---

## Page 87

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 87 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CMPR 
PROC/ 
GSCC/ 
CRQM 
PROC/ 
GSCC/ 
CADV 
PROC/ 
GSCC/ 
CMDA 
PROC/ 
GSCC/ 
LCTA 
PROC/ 
GSCC/ 
PCCA 
O :20C: :SECO//   Secondary Reference 
Number 
          
O :92A: :REPO//   Repo Rate       
O :19A: :REPA// /USD End Leg [[settlement]] 
Amount 
      
M :16S: REPO    End of Block           
 
Advices Referring to Receiving [[Member]]’s (Your) Trades 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CREQ 
PROC/ 
GSCC/ 
CCRQ 
PROC/ 
GSCC/ 
YTPA 
PROC/ 
GSCC/ 
YTPR 
PROC/ 
GSCC/
CPNR 
PROC/ 
GSCC/
RPSD 
PROC/ 
GSCC/ 
CMPM 
PROC/ 
GSCC/ 
MDAD 
        Message Header             
M       Password          
M       Sender          
M       Message Type         
M       Receiver          
M :16R: GENL   Mandatory Start of 
Block 
            
M :20C: :SEME//   Sender's Message 
Reference 
        
M :23G: NEWM   Function of the 
Message – New 
or 
  
      

---

## Page 88

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 88 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CREQ 
PROC/ 
GSCC/ 
CCRQ 
PROC/ 
GSCC/ 
YTPA 
PROC/ 
GSCC/ 
YTPR 
PROC/ 
GSCC/
CPNR 
PROC/ 
GSCC/
RPSD 
PROC/ 
GSCC/ 
CMPM 
PROC/ 
GSCC/ 
MDAD 
    CANC   Cancel            
O :98C: :PREP//   Preparation Date/Time         
M :22F: :TRTR/ GSCC/CASH Trade Transaction 
Type – Cash Trade 
Indicator                    
or 
        
   GSCC/REPO Repo Trade Indicator            
or 
        
   GSCC/TRLK Locked -in Cash Trade 
Indicator  
or 
        
   GSCC/TRLR Locked -in Repo Trade 
Indicator  
or 
        
   GSCC/TRDC Demand Cash Trade 
Indicator  
or 
        
   GSCC/TRDR Demand Repo Trade 
Indicator  
        
M :16R: LINK   Optional Repeat 
Block Start 
            
M :20C: :MAST//   Master ([[Member]])  
Reference Number 
        
M :16S: LINK   End of Block         
 
  
M :16R: LINK   Repeat Block Start              
O :20C: :PREV//   Previous Reference 
Number 
          

---

## Page 89

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 89 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CREQ 
PROC/ 
GSCC/ 
CCRQ 
PROC/ 
GSCC/ 
YTPA 
PROC/ 
GSCC/ 
YTPR 
PROC/ 
GSCC/
CPNR 
PROC/ 
GSCC/
RPSD 
PROC/ 
GSCC/ 
CMPM 
PROC/ 
GSCC/ 
MDAD 
M :16S: LINK   End of Block 
  
    
  
M :16R: LINK   Repeat Block Start              
O :20C: :LIST//   [[GSD]] Assigned 
Reference Number 
(Receiver’s TID)  
        
M :16S: LINK   End of Block 
  
    
  
M :16R: LINK   Repeat Block Start              
O :20C: :BASK//   [[Broker]] (Counterparty) 
Reference Number 
([[Broker]] Xref) 
        
M :16S: LINK   End of Block             
M :16S: GENL   End of Block             
M :16R: CONFDET   Mandatory Start of 
Block 
            
M :98C: :TRAD//   Trade Date & Time         
M :98A: :SETT//   [[settlement]] Date (or 
Start Leg [[settlement]] 
Date if REPO)  
        
M :90A: :DEAL/ /PRCT/ Deal Price – 
Percentage        
or   
        
   /YIEL/ Yield                   
or 
        
   /DISC/ Discount          

---

## Page 90

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 90 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CREQ 
PROC/ 
GSCC/ 
CCRQ 
PROC/ 
GSCC/ 
YTPA 
PROC/ 
GSCC/ 
YTPR 
PROC/ 
GSCC/
CPNR 
PROC/ 
GSCC/
RPSD 
PROC/ 
GSCC/ 
CMPM 
PROC/ 
GSCC/ 
MDAD 
O :19A: :SETT/ /USD [[settlement]] Amount (or 
Start Leg [[settlement]] 
Amount if REPO)  
        
M :22H: :BUSE/ /BUYI Trade Type – Buy 
(REVR) 
or 
        
      /SELL Sell (REPO)         
O :22F: :PROC/ GSCC/CMPR Processing Indicator – 
Comparison Request  
or 
 
        
 
      GSCC/CRQM Comparison Request 
Modify  
or 
  
 
        
      GSCC/CADV Comparison Request 
Cancel  
or 
        
 
  
   GSCC/LCTA Locked -in Trade Advice 
or 
        
      GSCC/CREQ Cancel Request                      
or 
           
      GSCC/CCRQ Cancel Request Cancel  
or 
           
   GSCC/PCCA Post Comparison 
Cancel Advice (of 
Locked in Trade)  
or 
        

---

## Page 91

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 91 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CREQ 
PROC/ 
GSCC/ 
CCRQ 
PROC/ 
GSCC/ 
YTPA 
PROC/ 
GSCC/ 
YTPR 
PROC/ 
GSCC/
CPNR 
PROC/ 
GSCC/
RPSD 
PROC/ 
GSCC/ 
CMPM 
PROC/ 
GSCC/ 
MDAD 
   GSCC/YTPA Yield to Price 
(Assumed Coupon) of 
WI Trade 
or 
        
   GSCC/YTPR Yield to Price (Real 
Coupon) of WI Trade  
or 
        
   GSCC/CPNR Coupon Reset (of UST 
FRNs)                          
or 
        
   GSCC/RPSD Repo Substitution 
Details  
or  
        
      GSCC/CMPM Trade Compared with 
Modifications                           
or 
           
      GSCC/MDAD Post Comparison Trade 
Modification                             
or 
           
      GSCC/CMDA Post Comparison 
Counterparty Trade 
Modification                             
or 
            
      GSCC/DFVA [[default]] Values Applied  
or 
            
      GSCC/SITR Screen Input Trade 
Replay  
or 
            

---

## Page 92

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 92 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CREQ 
PROC/ 
GSCC/ 
CCRQ 
PROC/ 
GSCC/ 
YTPA 
PROC/ 
GSCC/ 
YTPR 
PROC/ 
GSCC/
CPNR 
PROC/ 
GSCC/
RPSD 
PROC/ 
GSCC/ 
CMPM 
PROC/ 
GSCC/ 
MDAD 
      GSCC/NAFI DK Advice                                
or 
            
      GSCC/DCCX DK Remove Advice                    
M :22H: :PAYM/ /APMT Against Payment 
Indicator – vs. Payment  
        
M :16R: CONFPRTY   Mandatory Repeat 
Start of Block 
  
 
        
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]]         
O :20C: :PROC//   Processing Reference 
– [[Buyer]] (Counterparty) 
X-ref 
            
O :70E: :DECL/ /GSCC Declaration Details 
Narrative 
            
      /PREV [[Buyer]] (Counterparty) 
Previous X-ref 
            
      /CORR Party = [[Buyer]]’s 
Executing firm  
        
O :70C: :PACO/ /GSCC Party Narrative             
      /TDID [[Buyer]] (Counterparty) 
Trader [[ID]] 
        
M :16S: CONFPRTY   End of Block 
  
    
  
M :16R: CONFPRTY   Mandatory Repeat 
Start of Block  
  
    
  
M :95R: :SELL/ GSCC/PART Party = [[Seller]]          

---

## Page 93

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 93 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CREQ 
PROC/ 
GSCC/ 
CCRQ 
PROC/ 
GSCC/ 
YTPA 
PROC/ 
GSCC/ 
YTPR 
PROC/ 
GSCC/
CPNR 
PROC/ 
GSCC/
RPSD 
PROC/ 
GSCC/ 
CMPM 
PROC/ 
GSCC/ 
MDAD 
O :20C: :PROC//   Processing Reference 
– [[Seller]] (Counterparty) 
X-ref 
            
O :70E: :DECL/ /GSCC Declaration Details 
Narrative 
  
    
  
      /PREV [[Seller]] (Counterparty) 
Previous X-ref 
            
      /CORR Party = [[Seller]]’s 
Executing firm  
        
  :70C: :PACO/ /GSCC Party Narrative 
  
    
  
      /TDID [[Seller]] (Counterparty) 
Trader [[ID]] 
        
M :16S: CONFPRTY   End of Block 
  
    
  
M :36B: :CONF/ FAMT/ Quantity of Face 
Amount (Par)  
        
M :35B: /US/   Identification of 
Financial Instrument/ 
Security ([[CUSIP]]) 
        
O :70E: :TPRO/ /GSCC Trade Instruction 
Processing Narrative  
            
      /MSGR Message Reason (see 
Appendix E)  
        
      /DKRS DK Reason (see 
Appendix E)  
            
M :16S: CONFDET   End of Block 
  
      
 

---

## Page 94

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 94 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
CREQ 
PROC/ 
GSCC/ 
CCRQ 
PROC/ 
GSCC/ 
YTPA 
PROC/ 
GSCC/ 
YTPR 
PROC/ 
GSCC/
CPNR 
PROC/ 
GSCC/
RPSD 
PROC/ 
GSCC/ 
CMPM 
PROC/ 
GSCC/ 
MDAD 
M :16R: SETDET   Optional Start of 
Block  
            
M :22F: :SETR /RPTO [[settlement]] Transaction 
Indicator (Reporting 
Purposes)  
        
M :16R: AMT   Optional Start of 
Block  
            
M :17B: :STAN/ /N Standing Instruction 
Override = No  
        
M :19A: :LOCO/ /USD [[Broker]]’s Commission          
M :16S: AMT   End of Block 
  
    
  
M :16S: SETDET   End of Block             
M :16R: REPO   Optional Start of 
Block  
        
 
  
O :98A: :REPU//   End Leg [[settlement]] 
Date 
        
O :20C: :SECO//   Secondary Reference 
Number 
        
O :92A: :REPO//   Repo Rate         
O :19A: :REPA// /USD End Leg [[settlement]] 
Amount 
        
M :16S: REPO   End of Block             
 
 
 

---

## Page 95

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 95 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
DFVA 
PROC/ 
GSCC/ 
SITR 
PROC/ 
GSCC/ 
NAFI 
PROC/ 
GSCC/ 
DCCX 
        Message Header         
M       Password      
M       Sender      
M       Message Type     
M       Receiver      
M :16R: GENL   Mandatory Start of 
Block 
        
M :20C: :SEME//   Sender's Message 
Reference 
    
M :23G: NEWM   Function of the 
Message – New 
or 
    
    CANC   Cancel         
O :98C: :PREP//   Preparation Date/Time     
M :22F: :TRTR/ GSCC/CASH Trade Transaction 
Type – Cash Trade 
Indicator                    
or 
    
   GSCC/REPO Repo Trade Indicator            
or 
    
   GSCC/TRLK Locked -in Cash Trade 
Indicator  
or 
    
   GSCC/TRLR Locked -in Repo Trade 
Indicator  
or 
    
   GSCC/TRDC Demand Cash Trade 
Indicator  
or 
    
   GSCC/TRDR Demand Repo Trade 
Indicator  
    
M :16R: LINK   Optional Repeat 
Block Start 
        
M :20C: :MAST//   Master ([[Member]])  
Reference Number 
    
M :16S: LINK   End of Block   
 
  
 
M :16R: LINK   Repeat Block Start          

---

## Page 96

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 96 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
DFVA 
PROC/ 
GSCC/ 
SITR 
PROC/ 
GSCC/ 
NAFI 
PROC/ 
GSCC/ 
DCCX 
O :20C: :PREV//   Previous Reference 
Number 
       
M :16S: LINK   End of Block 
    
M :16R: LINK   Repeat Block Start          
O :20C: :LIST//   [[GSD]] Assigned 
Reference Number 
(Receiver’s TID)  
    
M :16S: LINK   End of Block 
    
M :16R: LINK   Repeat Block Start          
O :20C: :BASK//   [[Broker]] (Counterparty) 
Reference Number 
([[Broker]] Xref) 
    
M :16S: LINK   End of Block         
M :16S: GENL   End of Block         
M :16R: CONFDET   Mandatory Start of 
Block 
        
M :98C: :TRAD//   Trade Date & Time     
M :98A: :SETT//   [[settlement]] Date (or 
Start Leg [[settlement]] 
Date if REPO)  
    
M :90A: :DEAL/ /PRCT/ Deal Price – 
Percentage        
or   
    
   /YIEL/ Yield                   
or 
    
   /DISC/ Discount      
O :19A: :SETT/ /USD [[settlement]] Amount (or 
Start Leg [[settlement]] 
Amount if REPO)  
    
M :22H: :BUSE/ /BUYI Trade Type – Buy 
(REVR) 
or 
    
      /SELL Sell (REPO)     
O :22F: :PROC/ GSCC/CMPR Processing Indicator – 
Comparison Request  
or 
        
      GSCC/CRQM Comparison Request 
Modify  
or 
 
  
 
  

---

## Page 97

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 97 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
DFVA 
PROC/ 
GSCC/ 
SITR 
PROC/ 
GSCC/ 
NAFI 
PROC/ 
GSCC/ 
DCCX 
      GSCC/CADV Comparison Request 
Cancel  
or 
  
 
  
 
   GSCC/LCTA Locked -in Trade 
Ad vice 
or 
    
      GSCC/CREQ Cancel Request                      
or 
        
      GSCC/CCRQ Cancel Request 
Cancel  
or 
        
   GSCC/PCCA Post Comparison 
Cancel Advice (of 
Locked in Trade)  
or 
    
   GSCC/YTPA Yield to Price 
(Assumed Coupon) of 
WI Trade 
or 
    
   GSCCYTPR Yield to Price (Real 
Coupon) of WI Trade  
or 
    
   GSCC/CPNR Coupon Reset  (of UST 
FRNs)                       
or 
    
   GSCC/RPSD Repo Substitution 
Details  
or  
    
      GSCC/CMPM Trade Compared with 
Modifications                           
or 
        
      GSCC/MDAD Post Comparison 
Trade Modification                             
or 
        
      GSCC/CMDA Post Comparison 
Counterparty  Trade 
Modification                             
or 
        
      GSCC/DFVA [[default]] Values Applied  
or 
       
      GSCC/SITR Screen Input Trade 
Replay  
or 
       
      GSCC/NAFI DK Advice                                
or 
       

---

## Page 98

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 98 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
DFVA 
PROC/ 
GSCC/ 
SITR 
PROC/ 
GSCC/ 
NAFI 
PROC/ 
GSCC/ 
DCCX 
      GSCC/DCCX DK Remove Advice               
M :22H: :PAYM/ /APMT Against Payment 
Indicator – vs. Payment  
    
M :16R: CONFPRTY   Mandatory Repeat 
Start of Block 
 
  
 
  
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]]     
O :20C: :PROC//   Processing Reference 
– [[Buyer]] ( Counterparty ) 
X-ref 
        
O :70E: :DECL/ /GSCC Declaration Details 
Narrative 
        
      /PREV [[Buyer]] ( Counterparty ) 
Previous X-ref 
        
      /CORR Party = [[Buyer]]’s 
Executing firm  
    
O :70C: :PACO/ /GSCC Party Narrative         
      /TDID [[Buyer]] ( Counterparty ) 
Trader [[ID]] 
    
M :16S: CONFPRTY   End of Block 
    
M :16R: CONFPRTY   Mandatory Repeat 
Start of Block  
    
M :95R: :SELL/ GSCC/PART Party = [[Seller]]      
O :20C: :PROC//   Processing Reference 
– [[Seller]] (Counterparty ) 
X-ref 
        
O :70E: :DECL/ /GSCC Declaration Details 
Narrative 
    
      /PREV [[Seller]] ( Counterparty ) 
Previous X-ref 
        
      /CORR Party = [[Seller]]’s 
Executing firm  
    
  :70C: :PACO/ /GSCC Party Narrative 
    
      /TDID [[Seller]] ( Counterparty ) 
Trader [[ID]] 
    
M :16S: CONFPRTY   End of Block 
    

---

## Page 99

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT518 99 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description PROC/ 
GSCC/ 
DFVA 
PROC/ 
GSCC/ 
SITR 
PROC/ 
GSCC/ 
NAFI 
PROC/ 
GSCC/ 
DCCX 
M :36B: :CONF/ FAMT/ Quantity of Face 
Amount (Par)  
    
M :35B: /US/   Identification of 
Financial Instrument/  
Security ([[CUSIP]]) 
    
O :70E: :TPRO/ /GSCC Trade Instruction 
Processing Narrative  
        
      /MSGR Message Reason (see 
Appendix E)  
     
      /DKRS DK Reason (see 
Appendix E)  
       
M :16S: CONFDET   End of Block 
 
  
 
  
M :16R: SETDET   Optional Start of 
Block  
        
M :22F: :SETR /RPTO [[settlement]] Transaction 
Indicator (Reporting 
Purposes)  
    
M :17B: :STAN/ /N Standing Instruction 
Override = No  
    
M :16R: AMT   Optional Start of 
Block  
        
M :19A: :LOCO/ /USD [[Broker]]’s Commission      
M :16S: AMT   End of Block 
    
M :16S: SETDET   End of Block         
M :16R: REPO   Optional Start of 
Block  
  
 
  
 
O :98A: :REPU//   End Leg [[settlement]] 
Date 
    
O :20C: :SECO//   Secondary Reference 
Number 
    
O :92A: :REPO//   Repo Rate     
O :19A: :REPA// /USD End Leg [[settlement]] 
Amount 
    
M :16S: REPO   End of Block         

---

## Page 100

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specification s – MT599 100 
COMPARISON INTERACTIVE MESSAGE SPECIFICATIONS 
– MT599 
This section contains the detailed specifications including layout and field descriptions for the MT599 
Messages supporting output for [[GSD]]’s products and services. 
MT599 Administrative Message Description 
The SWIFT MT599 Administrative Message is a free-format SWIFT message which [[GSD]] utilizes to 
communicate administrative messages to Members (and their service providers, as applicable). [[GSD]] also uses 
this message type to notify Members regarding start and end-of-day processing, as well as cutoffs for trade 
inputs (e.g. DK cutoff).  
The following MT599 Messages may be generated to provided system administrative information to Members: 
Message Type This message is used to:  DVP GCF/ 
CCIT  
[[GSD]] Start-of-Day Notification 
(:79:GSCC/GADM/PREP/ …/GSOD/) 
inform a [[Member]] at the beginning of each business day that the 
[[GSD]] system is available for the submission of trades to be 
included for that days’ processing.  
  
[[GSD]] Demand Trade Submission 
Cutoff Message 
(:79:GSCC/GADM/PREP/ …/ SCDM/) 
inform Members when then may no longer submit transactions for 
demand comparison for that day. Any transactions submitted to 
[[GSD]] after this point will be submitted for bilateral comparison . 
  
[[GSD]] DK Submission Cutoff  Message 
(:79:GSCC/GADM/PREP/ …/ SCDK/) 
inform Members when they may no longer submit DK notices on 
demand trades submitted against them by a counterparty. Any DK 
notices submitted after this point will be rejected . 
  
[[GSD]] Submission Cutoff End- of-Day 
Message  
(:79:GSCC/GADM/PREP/ …/EDCS/) 
inform Members when then may no longer submit transactions to 
be included for processing for that day. Any transactions 
submitted to [[GSD]] after this point will be included in the next 
business day’s comparison processing.  
Note:  
No acknowledgements or rejections will be sent to Mem bers for 
trades submitted after this point until the system is next available 
(after the ‘/GSOD/’ start- of-day message is sent).  
  
[[GSD]] Processing End -of-Day 
Message  
(:79:GSCC/GADM/PREP/ …/EODC/) 
inform Members that the [[GSD]] system has completed batch 
processing for that business day, and that all interactive output to 
be generated that day has been transmitted. At this point no more 
interactive messages will be sent by [[GSD]] for that business day.  
  
[[GSD]] GCF/CCIT Net Processing 
Message  
(:79:GSCC/GADM/PREP/ …/SNET) 
inform Members that the [[GSD]] system has commenced the 
GCF/CCIT Netting process for that business day.  
  
  

---

## Page 101

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT599 101 
MT599 Administrative Message Specifications 
All MT599 messages sent by [[GSD]] will provide the [[Member]] with the date and time of message preparation and 
the date for the business day in question. End-of-day messages will also contain the next [[GSD]] valid trade 
submission date. 
One start-of-day message will be sent out for each business day, when the [[GSD]] system is open for trade 
submis sion (DVP and GCF/CCIT messages will be sent out separately): 
• /GSOD/  
Two end-of -day messages will be sent to Members nightly (DVP and GCF/CCIT messages will be sent out 
separately): 
• /EDCS/   
• / EODC/  
Other cutoff and end-of-day messages that will be sent to Members, as applicable: 
• /SCDM/  
• /SCDK/  
• /SNET/  
Note: 
/NXTD/ - This qualifier will not appear as a standalone in any MT599 message. It will appear in conjunction with SCDM, 
SCDK, EDCS and EODC qualifiers.  
MT599 Administrative Message Format Differences 
It is important to note that these MT599 messages are based on an older SWIFT message type, which is 
slightly different in format from the other ISO 15022 messages implemented to support [[GSD]]’s Real-time 
Comparison process. 
As can be noted on the following pages: 
• there is no Start or End of Block tags (16R and 16S), 
• tags [[DO]] not always include the optional 1-character format suffix, and 
• there are no generic fields, qualifiers or repeating sequences. 
 
We have included qualifiers in Tag 79 in an attempt to maintain similar formats to other messages 
implemented, given that any type of text can be included in narrative fields. [[GSD]], for this purpose, has 
attempted to delineate, and label, the ‘sub fields’ included in this tag in a similar manner to those on other 
messages in the interactive messaging specifications distributed. Tag 79 will provide a reference to the record 
type being sent, which always follows the message preparation date and time. 
  

---

## Page 102

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT599 102 
MT599 Administrative Message General Format 
This section provides the general format for the MT599 Administrative Message. As described in the MT599 
Message Description, the MT599 will be sent by [[GSD]] to Members for the following events: 
• [[GSD]] Start-of-Day Notification 
• [[GSD]] Demand Trade Submission Cutoff Message 
• [[GSD]] DK Submission Cutoff Message  
• [[GSD]] Submission Cutoff End-of-Day Message 
• [[GSD]] Processing End-of-Day Message 
• G SD GCF/CCIT Net Processing Message 
 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  
    Message Header  
M       Password  12!c 
M       Sender  8!c 
M       Message Type 3!n/3!n/4!c  
M       Receiver  8!c 
M :20:    Transaction (sender’s message) 
Reference Number 
 16x 
M 79:   Narrative (35*50x) 
  GSCC/GADM  [[GSD]] Administrative Message 4!c/4!c 
  /PREP/  Preparation Date/Time (8!n6!n) 
YYYYMMDDHHMMSS 
  /GSOD/  [[GSD]] Start-of-Day Notification  
or 
YYYYMMDD 
  /SCDM/  [[GSD]] Demand Trade Submission 
Cutoff Message  
or  
YYYYMMDD 
  /SCDK/  [[GSD]] DK Submission Cutoff 
Message 
or 
YYYYMMDD 
  /EDCS/  [[GSD]] Submission Cutoff End- of-
Day Message 
or 
YYYYMMDD 
  /EODC/  [[GSD]] Processing End -of-Day 
Message 
or 
YYYYMMDD 

---

## Page 103

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT599 103 
M/O Tag Block/ 
Qualifier 
Sub-qualifier/ 
Options 
Field Description Data Field Format  
  /SNET/  [[GSD]] GCF/CCIT Net Processing 
Message 
YYYYMMDD 
  /NXTD/  Next [[GSD]] ‘Trade Submission’ Day                                         YYYYMMDD 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 104

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT599 104 
MT599 Administrative Message Field Specifications 
This section provides the detailed field specifications for the MT599 Administrative Message.   
Block/Tag Notes 
Message 
Header 
Each message must contain a Message Header. All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password   12!c This field will be blank -filled on all outbound MT599 Messages . 
Sender   8!c “GSCCTRRS” ([[GSD]] Trade Registration and Reconciliation System) for DVP, 
“GCFCTRRS” (GCF Trade Registration and Reconciliation System) for GCF/CCIT will 
always be the sender  of the MT599 messages.  
Message Type 3!n/3!n/4!c  The first 3 characters indicate to  the recipient the message type (599); the second 3 
positions reflect the version of the message interface (currently always 000). The last 
4 characters indicate the [[issuer]] code to be used in the message (GSCC).  
Receiver 8!c [[Member]] [[ID]] 
20 Sender’s Message Reference 
This field contains the sender’s message reference number. It is mandatory and will  contain a 
unique number to unambiguously identify each message sent from [[GSD]]. This  is a communications 
message number, not a trade number.  
e.g., :20:1112190656149 
Note: 
This field will be populated with an uppercase alphanumeric value. It will not contain symbols or 
hyphens .                                                                                   
 
79 Narrative  
This field will contain the various administrative message data, including the type of message,  using 
the following qualifiers:  
• GSCC/GADM – this qualifier/[[Option]] indicates that this is an administrative message being 
sent by [[GSD]] followed by : 
• /PREP/ – this field contains the message preparation date and time, and either 
• /GSOD/ – this qualifier indicates to [[Member]] s that this MT599 message is [[GSD]]’s  beginning of 
day notification for the business date noted. Subsequent to receiving this  message, Members 
can begin to send transactions to [[GSD]] to be included in that day’s  processing. Any 
messages received by [[GSD]] after this point, and before the end -of-day submission cutoff, will 
result in immediate acknowledgement/rejection. [[GSD]] will also, at  this point, begin sending 
acknowledgement/rejection MT509 output for all trades received  after the prior business 
day’s cutoff point , or  
• /SCDM/ – this qualifier  indicates that this MT599 message is [[GSD]]’s notification to the 
[[Member]] that they may no longer submit transactions for demand comparison for that 
business day. Any transactions submitted to [[GSD]] after this point will be submitted for 
bilateral c omparison , or 
• /SCDK/ – this qualifier indicates that this MT599 message is [[GSD]]’s notification to the 
[[Member]] that they may no longer submit DK notices on demand trades submitted against 
them by a counterparty  for that business day , or 
• /EDCS/ – this qualifier indicates that this MT599 message is [[GSD]]’s notification to the 
[[Member]] that any trades received by [[GSD]] after this tim e will not be included in that day’s  

---

## Page 105

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Comparison Interactive M essage Specifications  – MT599 105 
Block/Tag Notes 
processing. All trades received by [[GSD]] after this cutoff (until the next night’s cutoff/  “EDCS” 
message) will be included in processing for the next processing/trade date indicated below 
(following the qualifier ‘/NXTD/ ’), or  
• /EODC/ – this qualifier indicates that this MT599 message is [[GSD]]’s notification to  
• Members that [[GSD]] has completed its batch processes and no more interactive  comparison 
output will be generated for [[GSD]] for that business day. Any comparison related  output sent 
by [[GSD]] after this point (through the generation of the next ‘EODC’  message) will be for the 
business day indicated below (following the qualifier ‘/NXTD/’) , or 
• /SNET/ – this qualifier indicates  that this MT599 message is the GCF system’s notification to 
Members that the current day’s net has begun , and as applicable 
• /NXTD/ – this field provides the next valid [[GSD]] trade submission date and will be included  on 
all [[GSD]] end -of-day messages.  
e.g., :79:GSCC/GADM/PREP/20200323200150/EDCS /20200323/NXTD/20200324  
Note: 
/NXTD/ - This qualifier will not appear as a standalone in any MT599 message. It will appear in 
conjunction with SCDM, SCDK, EDCS and EODC qualifiers where the sender is GSCCTRRS . 
 
 
 

---

## Page 106

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 106 
APPENDICES 
List of Appendices 
A. Mandatory Data 
B. Message Flows 
C. Message Samples 
D. Message Structure Diagrams 
E. Reason Code Tables 
F. Detailed Field Analysis Results – Comparison Messages 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 107

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 107 
Appendix A – Mandatory Data 
This appendix of Mandatory Data contains [[GSD]] Mandatory Data for Buy/Sell (Cash) and Repo Trade Input. 6 
Mandatory Data for Buy/Sell (Cash) Transactions 
The following is a list of data that are mandatory on [[GSD]] input for buy/sell (cash) transactions: 
1. [[Member]]’s Firm [[ID]] 
2. [[Broker]] Reference Number (for Repo [[Broker]] submissions only) 
3. External Reference Number 
4. Transaction Type 
5. Trade Date 
6. [[settlement]] Date 
7. Security ([[CUSIP]] Number) 
8. Par Amount/Quantity 
9. Price 
10. Pricing Method 
11. [[settlement]] Amount/Final Money 
12. Counterparty’s (Contra) Firm [[ID]] 
13. Submitting [[Member]]’s Executing Firm (where applicable) 
14. Counterparty Submitting [[Member]]’s Executing Firm (where applicable) 
15. DK Reason Code (DK records only) 
Mandatory Data for Repo Transactions 
The following is a list of data that are mandatory on [[GSD]] input for Repo Transactions: 
1. [[Member]]’s Firm [[ID]] 
2. [[Broker]] Reference Number (for Repo [[Broker]] submissions only) 
3. External Reference Number 
4. Transaction Type 
5. End Leg [[settlement]] Date 
6. Security ([[CUSIP]] Number) 
7. Par Amount/Quantity 
8. Contract Repo Rate 
9. End Leg [[settlement]] Amount/Final Money 
10. Counterparty (Contra) Firm [[ID]] 
11. Submitting [[Member]]’s Executing Firm (where applicable) 
12. Counterparty Submitting [[Member]]’s Executing Firm (where applicable) 
13. Start Leg [[settlement]] Amount 
14. Start Leg [[settlement]] Date 
15. DK Reason Code (DK records only) 
 
6 In all cases, Members should refer to the [[FICC]] Government [[securities]] Division ("[[GSD]]") Rulebook for the 
complete listing of required data. 

---

## Page 108

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 108 
Appendix B – Message Flows  
This appendix of Message Flows contains detailed diagrams depicting the flows of messages to and from [[GSD]] 
for a various transaction related scenarios. As this document is meant to provide message specification details 
relating to the support of [[GSD]]’s comparison system processing, the flows reflected in this Appendix B will 
include various trade input and trade status messaging flows only. 
The following should be noted:  
1. All flows have been ordered based on whether the flow is applicable to the Bilateral Comparison process, 
or whether the flow depicts messaging for Demand or Locked-in Trades.  
2. Rather than using the terminology “[[participant]] A” and “[[participant]] B,” [[GSD]] has amended all flows to 
reflect “[[Member]] A” and “[[Member]] B”. Where the flows depict scenarios for Locked-in or Demand Trades, 
[[Member]] A will always be the Demand or Locked-in Submitter. [[Member]] B will always be the Demand or 
Locked-in Recipient. 
3. All Demand and Locked-in flows assume Bilateral Comparison, unless “Administrative Comparison” has 
been indicated. 
4. These f lows are based on those messages that would be generated from the Comparison system only. 
These flows will not include those messages that would be generated from the Netting system (netting 
and/or [[settlement]] messages). You may refer to the most current “[[GSD]] Interactive Messaging (IM) 
[[Member]] Specifications for Netting Output” document for flows that will contain comparison, netting and/or 
[[settlement]] related messages. 
 
 
 
  

---

## Page 109

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 109 
Listed below are the flows contained in this section: 
Bilateral Comparison Trade Flows 
B.B1 – Bilateral Trade Compared 
B.B2 – Bilateral Trade Rejected 
B.B3 – Bilateral Trade Modified Pre-comparison (via Interactive Messaging) 
B.B4 – Bilateral Trade Modified Pre-comparison (Screen Input Trade Replay via RTTM)  
B.B5 – Bilateral Trade Modified Post Comparison (Change does not affect Trade Details) 
B.B6 – Bilateral Trade Canceled Pre-comparison 
B.B7 – Bilateral Trade Canceled Post Comparison 
B.B8 – Bilateral Trade Cancel Remove (via RTTM) 
B.B9 – Bilateral Trade Compared with Final Money Difference 
B.B10 – Repo Substitution Request (via RTTM) 
B.B11 – Yield to Price conversion of Buy/Sell trade (Assumed or Real Coupon) 
B.B12 – Bilateral Uncompared Trade Deleted  
B.B13 – Bilateral Trade Input (Screen Input Trade Replay via RTTM) Compared 
B.B14 – Bilateral Trade Modified (Screen Input Trade Replay via RTTM) Post Comparison (Change does not 
affect Trade Details) 
B.B15 – [[default]] Values Applied to Bilateral Trade  
B.B16 – Bilateral Trades Compared through Par Summarization 
B.B17 – Bilateral Trade DK’d (via Interactive Messaging) 
B.B18 – Bilateral Trade DK’d (via RTTM) 
B.B19 – Bilateral Trade DK Rejected (DK via Interactive Messaging) 
B.B20 – Bilateral Trade DK’d and then Canceled 
B.B21 – Bilateral Trade DK’d, then Modified (Screen Input Trade Replay via RTTM) and Compared 
B.B22 – Bilateral Trade DK Removed (Undo DK via RTTM) 
B.B23 – Bilateral Trade DK’d, then DK Removed (Undo DK via RTTM) and Compared 
B.B24 – Bilateral Trade Canceled Due to DK 

---

## Page 110

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 110 
Demand Trade Flows 
B.D1 – Demand Trade Bilaterally Compared 
B.D2 – Demand Trade Administratively Compared 
B.D3 – Demand Trade Modified Pre-comparison (via Interactive Messaging) 
B.D4 – Demand Trade Modified Pre-comparison (Screen Input Trade Replay via RTTM) 
B.D5 – Demand Trade Modified Post Comparison by Demand Submitter (via Interactive Messaging) (Change 
does not affect Trade Details) 
B.D6 – Demand Trade Modified Post Comparison by Demand Submitter (Screen Input Trade Replay via 
RTTM) (Change does not affect Trade Details) 
B.D7 – Demand Trade Modified Post Comparison by Demand Recipient (via Interactive Messaging) (Change 
does not affect Trade Details) 
B.D8 – Demand Trade Modified Post Comparison by Demand Recipient (Screen Input Trade Replay via 
RTTM) (Change does not affect Trade Details) 
B.D9 – Demand Trade Canceled Pre-comparison  
B.D10 – Demand Trade Canceled Post Comparison (Cancel Originated by Demand Submitter) 
B.D11 – Demand Trade Canceled Post Comparison (Cancel Originated by Demand Recipient) 
B.D12 – Demand Trade Cancel Removed (Cancel Originated by Demand Submitter) 
B.D13 – Demand Trade Cancel Removed (Cancel Originated by Demand Recipient) 
B.D14 – Demand Trade DK’d (via Interactive Messaging)  
B.D15 – Demand Trade DK’d (via RTTM) 
B.D16 – Demand Trade DK Rejected (DK via Interactive Messaging)  
B.D17 – Demand Trade DK’d and then Canceled  
B.D18 – Demand Trade DK’d, then Modified (Screen Input Trade Replay via RTTM) and Compared 
B.D19 – Demand Trade DK Removed (Undo DK via RTTM) 
B.D20 – Demand Trade DK'd, then DK Removed (Undo DK via RTTM) and Compared 
B.D21 – Demand Trade Canceled Due to DK  
 
 
 

---

## Page 111

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 111 
Locked-in Trade Flows 
B.L1 – Locked-in Trade Bilaterally Compared  
B.L2 – Locked-in Trade Administratively Compared 
B.L3 – Locked-in Trade Modified Pre-comparison (via Interactive Messaging) 
B.L4 – Locked-in Trade Modified Pre-comparison (Screen Input Trade Replay via RTTM) 
B.L5 – Locked-in Trade Modified Post Comparison by Locked-in Submitter (via Interactive Messaging) 
(Change does not affect trade details) 
B.L6 – Locked-in Trade Modified Post Comparison by Locked-in Submitter (Screen Input Trade Replay via 
RTTM) (Change does not affect trade details) 
B.L7 – Locked-in Trade Modified Post Comparison by Locked-in Recipient (via Interactive Messaging) (Change 
does not affect trade details) 
B.L8 – Locked-in Trade Modified Post Comparison by Locked-in Recipient (Screen Input Trade Replay via 
RTTM) (Change does not affect trade details) 
B.L9 – Locked-in Trade Canceled Pre-comparison  
B.L10 – Locked-in Trade Canceled Post Comparison (Cancel Originated by Locked-in Submitter) 
B.L11 – Locked-in Trade Canceled Post Comparison (Cancel Originated by Locked-in Recipient) 
B.L12 – Locked-in Trade Cancel Removed (Cancel Originated by Locked-in Recipient)  
B.L13 – Locked-in Trade DK’d (via Interactive Messaging)  
B.L14 – Locked-in Trade DK’d (via RTTM)  
B.L15 – Locked-in Trade DK Rejected (DK via Interactive Messaging) 
B.L16 – Locked-in Trade DK’d and then Canceled 
B.L17 – Locked-in Trade DK’d, then Modified (Screen Input Trade Replay via RTTM) and Compared 
B.L18 – Locked-in Trade DK Removed (Undo DK via RTTM) 
B.L19 – Locked-in Trade DK’d, then DK Removed (Undo DK via RTTM) and Compared  
B.L20 – Locked-in Trade  DK’d, then DK Removed (Undo DK via RTTM) and Administratively Compared 
  

---

## Page 112

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 112 
Bilateral Comparison Trade Flows  
B. B1 - Bilateral Trades Compared 
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
 
  

---

## Page 113

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output 
Appendices 113 
B.B2 – Bilateral Trade Rejected 
[[Member]] A 2. MT509 Trade 
Rejected
1. MT515 Trade 
Submission
[[GSD]] 
RTTM 
(Match)
 
  

---

## Page 114

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 114 
B.B3 – Bilateral Trade Modified Pre-comparison (via Interactive Messaging) 
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4c. MT509 Modify 
Processed
4b. MT518 Comparison 
Request Modify
3. MT515 Trade Modify
4a. MT509 Modify 
Accepted
[[GSD]] 
RTTM 
(Match)
 
  

---

## Page 115

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 115 
B.B4 – Bilateral Trade Modified Pre-comparison (Screen Input Trade Replay via RTTM)  
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4b. MT518 Comparison 
Request Modify
3. Trade Modify via RTTM 
(No MT515 Submitted)
4a. MT518 Screen Input 
Trade Replay (Modify 
vi a RTTM)
[[GSD]] 
RTTM 
(Match)
  

---

## Page 116

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications  for Comparison Input & Output  
Appendices 116 
B.B5 – Bilateral Trade Modified Post Comparison (Change does not affect Trade Details) 
[[Member]] A
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
6. MT515 Trade Modify 7b. MT518 Post Comparison 
Contra Trade Modification
7a. MT509 Modify 
Accepted
7c. MT509 Modify 
Processed
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
 
 
  

---

## Page 117

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 117 
B.B6 – Bilateral Trade Canceled Pre-comparison 
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4c. MT509 Cancel 
Processed
4b. MT518 Comparison 
Request Cancel 
(due to contra action)
3. MT515 Trade Cancel
4a. MT509 Cancel 
Accepted
[[GSD]] 
RTTM 
(Match)
 
  

---

## Page 118

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 118 
B.B7 – Bilateral Trade Canceled Post Comparison 
[[Member]] AMember A
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
6. MT515 Trade Cancel 8. MT515 Trade Cancel
7a. MT509 Cancel 
Accepted
10a. MT509 Cancel 
Processed
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT518 Cancel 
Requested
10b. MT509 Cancel 
Processed
9b. MT518 Cancel 
Requested
9a. MT509 Cancel 
Accepted
 
  

---

## Page 119

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 119 
B.B8 – Bilateral Trade Cancel Remove (via RTTM) 
[[Member]] AMember A
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
8. Cancel Remove 
(via RTTM)
7a. MT509 Cancel 
Accepted
6. MT515 Trade Cancel
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT518 Cancel 
Requested
9a. MT509 Cancel 
Lifted by [[participant]]
9b. MT518 Cancel 
Request Cancel
 
  

---

## Page 120

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 120 
B.B9 – Bilateral Trade Compared with Final Money Difference ([[Member]] A’s trade is modified) 
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
5d. MT518 Comparison 
Request Cancel (due to match)
5e. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
5c. MT518 Trade Compared 
with Modifications
 
  

---

## Page 121

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 121 
B.B10 – Repo Substitution Request (via RTTM) 
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
[[GSD]] 
RTTM 
(Match)
1. Repo Sub Request 
entered (via RTTM)
 
  

---

## Page 122

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 122 
B.B11 – Yield to Price conversion of Buy/Sell trade (Assumed or Real Coupon) 
[[Member]] B
[[GSD]] 
RTTM 
(Match)
1. MT518 Yield to Price Conversion
 (Assumed or Real Coupon)
 
  

---

## Page 123

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 123 
B.B12 – Bilateral Uncompared Trade Deleted  
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
[[Member]] A
 [[Member]] B
3a. MT509 Deleted 
Uncompared Transaction
3b. MT518 Comparison 
Request Cancel (due to 
[[GSD]] action)
[[GSD]] 
RTTM 
(Match)
 
  

---

## Page 124

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 124 
B.B13 –Bilateral Trade Input (Screen Input Trade Replay via RTTM) Compared 
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT518 Screen Input 
Trade Replay
1. Trade Entered via RTTM 
(No MT515 Submitted)
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
 
  

---

## Page 125

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 125 
B.B14 – Bilateral Trade Modified (Screen Input Trade Replay via RTTM) Post Comparison (Change does 
not affect Trade Details) 
[[Member]] A
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
6. Trade Modified via RTTM 
(No MT515 Submitted)
7b. MT518 Post Comparison 
Contra Trade Modification
7a. MT518 Screen Input 
Trade Replay (Modify)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
 
  

---

## Page 126

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 126 
B.B15 – [[default]] Values Applied to Bilateral Trade  
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade 
Submission
2c. MT518 [[default]] 
Values Applied
[[GSD]] 
RTTM 
(Match)
 
  

---

## Page 127

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 127 
B.B16 – Bilateral Trades Compared through Par Summarization 
[[Member]] A
2b. MT518 Comparison 
Requested (Trade #1)
2a. MT509 Trade 
Accepted (Trade #1)
1. MT515 Trade 
Submission (Trade #1)
5. MT515 Trade 
Submission
7a. MT509 Trade Compared 
Through Par Summarization 
(Trade #1)
7c. MT509 Trade Compared 
Through Par Summarization
8c. MT518 Comparison 
Request Cancel (due to match)
8a. MT518 Comparison 
Request Cancel (Trade #1) 
(due to match)
3. MT515 Trade 
Submission (Trade #2)
[[Member]] A
 [[Member]] B
[[GSD]] 
RTTM 
(Match)
4a. MT509 Trade 
Accepted (Trade #2)
6b. MT518 Comparison 
Requested
4b. MT518 Comparison 
Requested (Trade #2)
[[Member]] A
[[Member]] A
[[GSD]] 
RTTM 
(Match)
6a. MT509 Trade 
Accepted
7b. MT509 Trade Compared 
Through Par Summarization 
(Trade #2)
[[Member]] A
5c. MT518 Comparison 
Request Cancel (Trade #2) 
(due to match)
[[Member]] A
[[Member]] B
 
  

---

## Page 128

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 128 
B.B17 – Bilateral Trade DK’d (via Interactive Messaging) 
2b. MT518 Comparison 
Requested2a. MT509 Trade 
Accepted
3. MT515 Trade DK1. MT515 Trade 
Submission
[[Member]] A
 [[Member]] B
[[GSD]] 
RTTM 
(Match)
4b. MT518 DK Advice
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
[[Member]] B4d. MT509 DK 
Processed
[[GSD]] 
RTTM 
(Match)
 
  

---

## Page 129

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 129 
B.B18– Bilateral Trade DK’d (via RTTM) 
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4a. MT518 DK Advice
[[GSD]] 
RTTM 
(Match)
3. DK Entered via RTTM 
(No MT515 Submitted)
4b. MT518 Comparison 
Request Cancel
 (due to DK)
 
  

---

## Page 130

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 130 
B.B19 – Bilateral Trade DK Rejected (DK via Interactive Messaging) 
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
[[GSD]] 
RTTM 
(Match)
3. MT515 Trade DK
4. MT509 DK Rejected
 
  

---

## Page 131

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 131 
B.B20 – Bilateral Trade DK’d and then Canceled 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A
 [[Member]] B
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
6b. MT509 Cancel 
Processed
[[GSD]] 
RTTM 
(Match)
[[Member]] A
6a. MT509 Cancel 
Accepted
5. MT515 Trade Cancel
 
  

---

## Page 132

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 132 
B.B21 – Bilateral Trade DK’d, then Modified (Screen Input Trade Replay via RTTM) and Compared 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
6b. MT518 Comparison 
Requested
6a. MT518 Screen Input 
Trade Replay (Modify 
vi a RTTM)
[[Member]] B
[[GSD]] 
RTTM 
(Match)
7. MT515 Trade 
Submission
5. Trade Modify via RTTM 
(No MT515 Submitted)
[[Member]] A
 [[Member]] B
8a. MT509 Trade 
Accepted
8b. MT518 Comparison 
Requested
[[GSD]] 
RTTM 
(Match)
9a. MT509 Trade 
Compared
9b. MT509 Trade 
Compared
9c. MT518 Comparison 
Request Cancel (due to match)
9d. MT518 Comparison 
Request Cancel (due to match)
 
  

---

## Page 133

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 133 
B.B22 – Bilateral Trade DK Removed (Undo DK via RTTM) 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A
 [[Member]] B
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
[[Member]] A
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
[[Member]] B
[[GSD]] 
RTTM 
(Match)
6b. MT518 Comparison 
Requested 
(due to DK Rem ove)
5. DK Remove (via 
RTTM)
6a. MT518 DK Remove 
Advice 
(due to contra action)
 
  

---

## Page 134

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 134 
B.B23 – Bilateral Trade DK’d, then DK Removed (Undo DK via RTTM) and Compared 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
6b. MT518 DK Remove 
Advice (due to contra action)
[[Member]] B
[[GSD]] 
RTTM 
(Match)
5. DK Remove (via 
RTTM)
[[Member]] A
 [[Member]] B
8a. MT509 Trade 
Accepted
8b. MT518 Comparison 
Requested
[[GSD]] 
RTTM 
(Match)
9a. MT509 Trade 
Compared
9b. MT509 Trade 
Compared
9c. MT518 Comparison 
Request Cancel (due to match)
9d. MT518 Comparison 
Request Cancel (due to match)
7. MT515 Trade 
Submission
6a. MT518 Comparison 
Requested
 (due to DK Rem ove)
 
  

---

## Page 135

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 135 
B.B24 – Bilateral Trade Canceled Due to DK 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A
 [[Member]] B
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
[[Member]] A
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
[[GSD]] 
RTTM 
(Match)
5. MT509 Trade 
Canceled (due to DK)
 
 
 
 
 
 
 
 
 
 
 

---

## Page 136

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 136 
Demand Trade Flows 
B.D1 – Demand Trade Bilaterally Compared 
[[Member]] AMember A
[[Member]] A
(Demand Submitter)
[[Member]] B
(Demand Recipient)
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
(Demand Submitter)
[[Member]] B
(Demand Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
  

---

## Page 137

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 137 
B.D2 – Demand Trade Administratively Compared 
[[Member]] AMember A
[[Member]] A
(Demand Submitter)
[[Member]] B
(Demand Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
3b. MT518 Comparison 
Requested
3a. MT518 Locked-in 
Trade Advice
[[Member]] A
(Demand Submitter)
[[Member]] B
(Demand Recipient)
4a. MT509 Trade 
Compared
4b. MT509 Trade 
Compared
[[GSD]] 
RTTM 
(Match)
4c. MT518 Comparison 
Request Cancel (due to match)
4d. MT518 Comparison 
Request Cancel (due to match)
  

---

## Page 138

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 138 
B.D3 – Demand Trade Modified Pre-comparison (via Interactive Messaging) 
[[Member]] A
(Demand Submitter)
[[Member]] B 
(Demand Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4c. MT509 Modify 
Processed
4b. MT518 Comparison 
Request Modify
3. MT515 Trade Modify
4a. MT509 Modify 
Accepted
[[GSD]] 
RTTM 
(Match)
  

---

## Page 139

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 139 
B.D4 – Demand Trade Modified Pre-comparison (Screen Input Trade Replay via RTTM) 
[[Member]] A
(Demand Submitter)
[[Member]] B 
(Demand Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4b. MT518 Comparison 
Request Modify
3. Trade Modify via RTTM 
(No MT515 Submitted)
4a. MT518 Screen Input 
Trade Replay (Modify 
vi a RTTM)
[[GSD]] 
RTTM 
(Match)
  

---

## Page 140

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 140 
B.D5 – Demand Trade Modified Post Comparison by Demand Submitter (via Interactive Messaging) 
(Change does not affect Trade Details) 
[[Member]] A
[[Member]] A
(Demand Submitter)
[[Member]] B
(Demand Recipient)
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
Demand Submitter)
[[Member]] B
(Demand Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
6. MT515 Trade Modify 7b. MT518 Post Comparison 
Contra Trade Modification
7a. MT509 Modify 
Accepted
7c. MT509 Modify 
Processed
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
  

---

## Page 141

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 141 
B.D6 – Demand Trade Modified Post Comparison by Demand Submitter (Screen Input Trade Replay via 
RTTM) (Change does not affect Trade Details) 
[[Member]] A
[[Member]] A
(Demand Submitter)
[[Member]] B
(Demand Recipient)
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
Demand Submitter)
[[Member]] B
(Demand Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
6. Trade Modify via RTTM 
(No MT515 Submitted
7b. MT518 Post Comparison 
Contra Trade Modification
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
7a. MT518 Screen Input Trade 
Replay (Modify via RTTM)
  

---

## Page 142

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 142 
B.D7 – Demand Trade Modified Post Comparison by Demand Recipient (via Interactive Messaging) 
(Change does not affect Trade Details) 
[[Member]] A
[[Member]] A
(Demand Submitter)
[[Member]] B
(Demand Recipient)
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
Demand Submitter)
[[Member]] B
(Demand Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
7b. MT518 Post Comparison 
Contra Trade Modification
7a. MT509 Modify 
Accepted
7c. MT509 Modify 
Processed
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
6. MT515 Trade Modify
  

---

## Page 143

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 143 
B.D8 – Demand Trade Modified Post Comparison by Demand Recipient (Screen Input Trade Replay via 
RTTM) (Change does not affect Trade Details) 
[[Member]] A
[[Member]] A
(Demand Submitter)
[[Member]] B
(Demand Recipient)
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
Demand Submitter)
[[Member]] B
(Demand Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
6. Trade Modify via RTTM 
(No MT515 Submitted
7b. MT518 Post Comparison 
Contra Trade Modification
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
7a. MT518 Screen Input Trade 
Replay (Modify via RTTM)
 
  

---

## Page 144

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 144 
B.D9 – Demand Trade Canceled Pre-comparison  
[[Member]] A
(Demand Submitter)
[[Member]] B
(Demand Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4c. MT509 Cancel 
Processed
4b. MT518 Comparison 
Request Cancel 
(due to contra action)
3. MT515 Trade Cancel
4a. MT509 Cancel 
Accepted
[[GSD]] 
RTTM 
(Match)
  

---

## Page 145

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 145 
B.D10 – Demand Trade Canceled Post Comparison (Cancel Originated by Demand Submitter) 
[[Member]] AMember A
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
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
(Demand Submitter)
[[Member]] B
(Demand Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
6. MT515 Trade Cancel 8. MT515 Trade Cancel
7a. MT509 Cancel 
Accepted
10a. MT509 Cancel 
Processed
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT518 Cancel 
Requested
10b. MT509 Cancel 
Processed
9b. MT518 Cancel 
Requested
9a. MT509 Cancel 
Accepted
  

---

## Page 146

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 146 
B.D11 – Demand Trade Canceled Post Comparison (Cancel Originated by Demand Recipient) 
[[Member]] AMember A
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
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
(Demand Submitter)
[[Member]] B
(Demand Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
8. MT515 Trade Cancel 6. MT515 Trade Cancel
7b. MT518 Cancel 
Requested
10a. MT509 Cancel 
Processed
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7a. MT509 Cancel 
Accepted
10b. MT509 Cancel 
Processed
9b. MT518 Cancel 
Requested
9a. MT509 Cancel 
Accepted
  

---

## Page 147

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 147 
B.D12 – Demand Trade Cancel Removed (Cancel Originated by Demand Submitter) 
[[Member]] AMember A
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
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
(Demand Submitter)
[[Member]] B
(Demand Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
8. Cancel Remove 
(via RTTM)
7a. MT509 Cancel 
Accepted
6. MT515 Trade Cancel
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT518 Cancel 
Requested
9a. MT509 Cancel 
Lifted by [[participant]]
9b. MT518 Cancel 
Request Cancel
  

---

## Page 148

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 148 
B.D13 – Demand Trade Cancel Removed (Cancel Originated by Demand Recipient) 
[[Member]] AMember A
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
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
(Demand Submitter)
[[Member]] B
(Demand Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
8. Cancel Remove 
(via RTTM)
6. MT515 Trade Cancel
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT518 Cancel 
Requested
9a. MT509 Cancel 
Lifted by [[participant]]
9b. MT518 Cancel 
Request Cancel
7a. MT509 Cancel 
Accepted
[[GSD]] 
RTTM 
(Match)
  

---

## Page 149

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 149 
B.D14 – Demand Trade DK’d (via Interactive Messaging)  
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK1. MT515 Trade 
Submission
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
[[GSD]] 
RTTM 
(Match)
4b. MT518 DK Advice
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
[[Member]] B
(Demand Recipient)
4d. MT509 DK 
Processed
[[GSD]] 
RTTM 
(Match)
  

---

## Page 150

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 150 
B.D15 – Demand Trade DK’d (via RTTM) 
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4a. MT518 DK Advice
[[GSD]] 
RTTM 
(Match)
3. DK Entered via RTTM 
(No MT515 Submitted)
4b. MT518 Comparison 
Request Cancel
 (due to DK)
  

---

## Page 151

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 151 
B.D16 – Demand Trade DK Rejected (DK via Interactive Messaging)  
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
[[GSD]] 
RTTM 
(Match)
3. MT515 Trade DK
4. MT509 DK Rejected
  

---

## Page 152

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 152 
B.D17 – Demand Trade DK’d and then Canceled  
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
6b. MT509 Cancel 
Processed
[[GSD]] 
RTTM 
(Match)
[[Member]] A 
(Demand Submitter)
6a. MT509 Cancel 
Accepted
5. MT515 Trade Cancel
  

---

## Page 153

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 153 
B.D18 – Demand Trade DK’d, then Modified (Screen Input Trade Replay via RTTM) and Compared 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A 
(Demand Submitter)
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
6b. MT518 Comparison 
Requested
6a. MT518 Screen Input 
Trade Replay (Modify 
vi a RTTM)
[[Member]] B
(Demand Recipient)
[[GSD]] 
RTTM 
(Match)
7. MT515 Trade 
Submission
5. Trade Modify via RTTM 
(No MT515 Submitted)
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)8a. MT509 Trade 
Accepted
8b. MT518 Comparison 
Requested
[[GSD]] 
RTTM 
(Match)
9a. MT509 Trade 
Compared
9b. MT509 Trade 
Compared
9c. MT518 Comparison 
Request Cancel (due to match)
9d. MT518 Comparison 
Request Cancel (due to match)
  

---

## Page 154

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 154 
B.D19 – Demand Trade DK Removed (Undo DK via RTTM) 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
[[Member]] A 
(Demand Submitter)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
[[Member]] B
(Demand Recipient)
[[GSD]] 
RTTM 
(Match)
6b. MT518 Comparison 
Requested 
(due to DK Rem ove)
5. DK Remove (via 
RTTM)
6a. MT518 DK Remove 
Advice 
(due to contra action)
  

---

## Page 155

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 155 
B.D20 – Demand Trade DK'd, then DK Removed (Undo DK via RTTM) and Compared 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A 
(Demand Submitter)
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
6b. MT518 DK Remove 
Advice (due to contra action)
[[Member]] B
(Demand Recipient)
[[GSD]] 
RTTM 
(Match)
5. DK Remove (via 
RTTM)
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
8a. MT509 Trade 
Accepted
8b. MT518 Comparison 
Requested
[[GSD]] 
RTTM 
(Match)
9a. MT509 Trade 
Compared
9b. MT509 Trade 
Compared
9c. MT518 Comparison 
Request Cancel (due to match)
9d. MT518 Comparison 
Request Cancel (due to match)
7. MT515 Trade 
Submission
6a. MT518 Comparison 
Requested
 (due to DK Rem ove)
  

---

## Page 156

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 156 
B.D21 – Demand Trade Canceled Due to DK  
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A 
(Demand Submitter)
[[Member]] B
(Demand Recipient)
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Cancel
 (due to DK)
[[Member]] A 
(Demand Submitter)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
[[GSD]] 
RTTM 
(Match)
5. MT509 Trade 
Canceled (due to DK)
  

---

## Page 157

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 157 
Locked-in Trade Flows  
B.L1 – Locked-in Trade Bilaterally Compared  
[[Member]] AMember A
[[Member]] A
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
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
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
  

---

## Page 158

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 158 
B.L2 – Locked-in Trade Administratively Compared 
[[Member]] AMember A
[[Member]] A
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
3b. MT518 Comparison 
Requested
3a. MT518 Locked-in 
Trade Advice
[[Member]] A
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
4a. MT509 Trade 
Compared
4b. MT509 Trade 
Compared
[[GSD]] 
RTTM 
(Match)
4c. MT518 Comparison 
Request Cancel (due to match)
4d. MT518 Comparison 
Request Cancel (due to match)
  

---

## Page 159

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 159 
B.L3 – Locked-in Trade Modified Pre-comparison (via Interactive Messaging) 
[[Member]] A
(Locked-in Submitter)
[[Member]] B 
(Locked-in Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4c. MT509 Modify 
Processed
4b. MT518 Comparison 
Request Modify
3. MT515 Trade Modify
4a. MT509 Modify 
Accepted
[[GSD]] 
RTTM 
(Match)
  

---

## Page 160

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output 
Appendices 160 
B.L4 – Locked-in Trade Modified Pre-comparison (Screen Input Trade Replay via RTTM) 
[[Member]] A
(Locked-in Submitter)
[[Member]] B 
(Locked-in Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4b. MT518 Comparison 
Request Modify
3. Trade Modify via RTTM 
(No MT515 Submitted)
4a. MT518 Screen Input 
Trade Replay (Modify 
vi a RTTM)
[[GSD]] 
RTTM 
(Match)
  

---

## Page 161

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 161 
B.L5 – Locked-in Trade Modified Post Comparison by Locked-in Submitter (via Interactive Messaging) 
(Change does not affect trade details) 
[[Member]] A
[[Member]] A
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
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
Demand Submitter)
[[Member]] B
(Locked-in Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
6. MT515 Trade Modify 7b. MT518 Post Comparison 
Contra Trade Modification
7a. MT509 Modify 
Accepted
7c. MT509 Modify 
Processed
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
  

---

## Page 162

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 162 
B.L6 – Locked-in Trade Modified Post Comparison by Locked-in Submitter (Screen Input Trade Replay 
via RTTM) (Change does not affect trade details) 
[[Member]] A
[[Member]] A
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
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
Demand Submitter)
[[Member]] B
(Locked-in Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
6. Trade Modify via RTTM 
(No MT515 Submitted
7b. MT518 Post Comparison 
Contra Trade Modification
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
7a. MT518 Screen Input Trade 
Replay (Modify via RTTM)
  

---

## Page 163

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications  for Comparison Input & Output  
Appendices 163 
B.L7 – Locked-in Trade Modified Post Comparison by Locked-in Recipient (via Interactive Messaging) 
(Change does not affect trade details) 
[[Member]] A
[[Member]] A
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
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
Demand Submitter)
[[Member]] B
(Locked-in Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
7b. MT518 Post Comparison 
Contra Trade Modification
7a. MT509 Modify 
Accepted
7c. MT509 Modify 
Processed
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
6. MT515 Trade Modify
  

---

## Page 164

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 164 
B.L8 – Locked-in Trade Modified Post Comparison by Locked-in Recipient (Screen Input Trade Replay 
via RTTM) (Change does not affect trade details) 
[[Member]] A
[[Member]] A
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
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
Demand Submitter)
[[Member]] B
(Locked-in Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
6. Trade Modify via RTTM 
(No MT515 Submitted
7b. MT518 Post Comparison 
Contra Trade Modification
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
7a. MT518 Screen Input Trade 
Replay (Modify via RTTM)
  

---

## Page 165

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 165 
B.L9 – Locked-in Trade Canceled Pre-comparison  
[[Member]] A
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
4c. MT509 Cancel 
Processed
4b. MT518 Comparison 
Request Cancel 
(due to contra action)
3. MT515 Trade Cancel
4a. MT509 Cancel 
Accepted
[[GSD]] 
RTTM 
(Match)
  

---

## Page 166

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 166 
B.L10 – Locked-in Trade Canceled Post Comparison (Cancel Originated by Locked-in Submitter) 
[[Member]] AMember A
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
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
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
6. MT515 Trade Cancel
7a. MT509 Cancel 
Accepted
8a. MT509 Cancel 
Processed
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT518 Post 
Comparison Cancel Advice
8b. MT509 Cancel 
Processed
  

---

## Page 167

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 167 
B.L11 – Locked-in Trade Canceled Post Comparison (Cancel Originated by Locked-in Recipient) 
[[Member]] AMember A
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
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
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
8. MT515 Trade Cancel 6. MT515 Trade Cancel
10a. MT509 Cancel 
Processed
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT518 Cancel 
Requested
10b. MT509 Cancel 
Processed
9b. MT518 Post 
Comparison Cancel Advice
9a. MT509 Cancel 
Accepted
7a. MT509 Cancel 
Accepted
  

---

## Page 168

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 168 
B.L12 – Locked-in Trade Cancel Removed (Cancel Originated by Locked-in Recipient)  
[[Member]] AMember A
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
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
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
8. Cancel Remove 
(via RTTM)
6. MT515 Trade Cancel
[[GSD]] 
RTTM 
(Match)
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT518 Cancel 
Requested
9b. MT509 Cancel 
Lifted by [[participant]]
9a. MT518 Cancel 
Request Cancel
7a. MT509 Cancel 
Accepted
[[GSD]] 
RTTM 
(Match)
  

---

## Page 169

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 169 
B.L13 – Locked-in Trade DK’d (via Interactive Messaging)  
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK1. MT515 Trade 
Submission
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
[[GSD]] 
RTTM 
(Match)
4b. MT518 DK Advice
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Modify
 (due to DK)
[[Member]] B
(Locked-in Recipient)
4d. MT509 DK 
Processed
[[GSD]] 
RTTM 
(Match)
  

---

## Page 170

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 170 
B.L14 – Locked-in Trade DK’d (via RTTM)  
3. Trade DK via RTTM 
(No MT515 Submitted
1. MT515 Trade 
Submission
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
[[GSD]] 
RTTM 
(Match)
[[GSD]] 
RTTM 
(Match)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
4b. MT518 DK Advice
4a. MT518 Comparison 
Request Modify
 (due to DK)
  

---

## Page 171

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 171 
B.L15 – Locked-in Trade DK Rejected (DK via Interactive Messaging) 
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
[[GSD]] 
RTTM 
(Match)
3. MT515 Trade DK
4. MT509 DK Rejected
  

---

## Page 172

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 172 
B.L16 – Locked-in Trade DK’d and then Canceled 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Modify
 (due to DK)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
6c. MT509 Cancel 
Processed
[[GSD]] 
RTTM 
(Match)
[[Member]] A 
(Locked-in Submitter)
6a. MT509 Cancel 
Accepted
5. MT515 Trade Cancel
[[Member]] B
(Locked-in Recipient)
6b. MT518 Comparison 
Request Cancel 
(due to Contra A ction)
  

---

## Page 173

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 173 
B.L17 – Locked-in Trade DK’d, then Modified (Screen Input Trade Replay via RTTM) and Compared 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A 
(Locked-in Submitter)
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Modify
 (due to DK)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
6b. MT518 Comparison 
Request Modify 
(due to Contra A ction)
6a. MT518 Screen Input 
Trade Replay (Modify 
vi a RTTM)
[[Member]] B
(Locked-in Recipient)
[[GSD]] 
RTTM 
(Match)
7. MT515 Trade 
Submission
5. Trade Modify via RTTM 
(No MT515 Submitted)
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)8a. MT509 Trade 
Accepted
8b. MT518 Comparison 
Requested
[[GSD]] 
RTTM 
(Match)
9a. MT509 Trade 
Compared
9b. MT509 Trade 
Compared
9c. MT518 Comparison 
Request Cancel (due to match)
9d. MT518 Comparison 
Request Cancel (due to match)
  

---

## Page 174

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 174 
B.L18 – Locked-in Trade DK Removed (Undo DK via RTTM) 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Modify
 (due to DK)
[[Member]] A 
(Locked-in Submitter)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
[[Member]] B
(Locked-in Recipient)
[[GSD]] 
RTTM 
(Match)
6b. MT518 Comparison 
Request Modify 
(due to DK Rem ove)
5. DK Remove (via 
RTTM)
6a. MT518 DK Remove 
Advice 
(due to contra action)
  

---

## Page 175

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 175 
B.L19 – Locked-in Trade DK’d, then DK Removed (via MT515 Trade Submission) and Compared  
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A 
(Locked-in Submitter)
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Modify
 (due to DK)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
6b. MT518 DK Remove 
Advice (due to contra action)
[[Member]] B
(Locked-in Recipient)
[[GSD]] 
RTTM 
(Match)
5. DK Remove (via 
MT515 Trade 
Submission)
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
6a. MT509 Trade 
Accepted
6c. MT518 Comparison 
Requested
[[GSD]] 
RTTM 
(Match)
7a. MT509 Trade 
Compared
7b. MT509 Trade 
Compared
7c. MT518 Comparison 
Request Cancel (due to match)
7d. MT518 Comparison 
Request Cancel (due to match)
 
  

---

## Page 176

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 176 
B.L20 – Locked-in Trade  DK’d, then DK Removed (Undo DK via RTTM) and Administratively Compared 
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
3. MT515 Trade DK
[[Member]] A 
(Locked-in Submitter)
[[GSD]] 
RTTM 
(Match)
4a. MT509 DK 
Accepted
4c. MT518 Comparison 
Request Modify
 (due to DK)
4d. MT509 DK 
Processed
1. MT515 Trade 
Submission
4b. MT518 DK Advice
6. MT518 DK Remove 
Advice (due to contra action)
[[Member]] B
(Locked-in Recipient)
[[GSD]] 
RTTM 
(Match)
5. DK Remove (via 
RTTM)
[[Member]] A 
(Locked-in Submitter)
[[Member]] B
(Locked-in Recipient)
7b. MT518 Comparison 
Requested
[[GSD]] 
RTTM 
(Match)
8a. MT509 Trade 
Compared
8b. MT509 Trade 
Compared
8c. MT518 Comparison 
Request Cancel (due to match)
8d. MT518 Comparison 
Request Cancel (due to match)
7a. MT518 Locked-in 
Trade Advice
 
  

---

## Page 177

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 177 
Appendix C – Message Samples 
This appendix of Message Samples provides examples of a variety of MT515, MT509, and MT518 messages 
for Cash and Repo trades. This appendix also provides examples of a MT599 messages sent to Members for 
administrative purposes. 
It should be noted that the message samples contained in this appendix are not necessarily intended to 
represent the actual flow of events that would generate messages Members would receive, but rather 
individual samples to help Members become familiar with the message structure. The introductory text for each 
scenario is intended to clarify how the different message samples were populated. It also should be noted that 
the comparison related message samples displayed in this appendix are based on SWIFT 15022 Standard 
Formats, with exception of the MT599 messages. 
Listed below are the sample scenarios depicted in this appendix: 
C1 – Bilateral Next-Day Settling Trade Rejected 
C2 – Bilateral Same-Day Settling Trade Compared 
C3 – Bilateral Next-Day Settling Trade Canceled Post Comparison  
C4 – Demand Next-Day Settling Trade DK’d, Modified and Compared 
C5 – Repo Substitution Processed on Demand Trade 
C6 – Various MT599 Administrative Messages 
 
  

---

## Page 178

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 178 
Sample # C1 – Bilateral Next-Day Settling Trade Rejected  
On April 28, 2020, Dealer [[Member]] 88T2 executes a next day settling sell trade for 100,000 of U.S. Treasury 
Note – [[CUSIP]] 9128282A7. The [[settlement]] date for the trade is April 29, 2020 and the final money is 
$106,886.68. The trade is submitted to [[FICC]] [[GSD]] by Dealer [[Member]] 88T2 with a counterparty [[ID]] (87X9) that 
is not a Non-[[Member]] of [[GSD]]. 
[[Member]] Reference Numbers 88T2 
Message Reference 0000000315 
External Reference 2A75020200428315 
New External Reference N/A 
[[Broker]] Reference N/A 
[[GSD]] Reference (TID)  N/A 
Secondary Reference N/A 
 
The message samples presented on the following pages are all based on the above scenario.  
C1.a MT515 Dealer [[Member]] 88T2 Submits Sell Trade to [[GSD]] 
C1.b MT509 Trade Rejected Record sent to Dealer [[Member]] 88T2 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated. Also, these sample messages are only those messages that would be generated from 
the Comparison system and not those that would be generated from the Netting system (netting and/or [[settlement]] 
messages). You may refer to the most current “[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output” 
document for netting and/or [[settlement]] related me ssages.  
 
  

---

## Page 179

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 179 
Sample C1.a MT515 Dealer [[Member]] 88T2  Submits Sell Trade to [[GSD]]  
Message Content  Comments 
GSADDF [[GSD]] Assigned Unique Identifier  
88T2 Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//0000000315 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200428081211 Date and Time of Message Preparation  
:22F::TRTR/GSCC/CASH Cash Trade Indicator  
:16R:LINK   
:20C::MAST//2A75020200428315 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200428081201 Trade Date and Time 
:98A::SETT//20200429 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/106,4375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD106,886,68 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO)  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/INST Instruct Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87X9 [[Buyer]] (Reverse Party) Information - Contra -party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88T2 [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/100000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/9128282A7 Identification of Financial Instrument /Security ([[CUSIP]]) 
:16S:CONFDET   
- End of Message 

---

## Page 180

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 180 
 
Sample C1.b MT509 Trade Rejected Record sent to Dealer [[Member]] 88T2 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
88T2 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001912 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200428081219 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//2A75020200428315 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//0000000315 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:STAT   
:25D::IPRC//REJT Trade Input Rejected Status 
:16R:REAS  
:24B::REJT/GSCC/E010 Reject Reason Code (E010 = Bad [[Buyer]] Party)  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
  

---

## Page 181

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 181 
Sample # C2 – Bilateral Same-Day Starting Transaction Compared  
On April 29, 2020, Repo Dealer [[Member]] 88ZT executes an overnight same-day starting Repo transaction with 
Repo Dealer [[Member]] 899A for 50,000,000 of U.S. Treasury Bond – [[CUSIP]] 912810SC3. The Contract Repo 
Rate is 3.875% and the Start Leg [[settlement]] Amount is $51,000,000.00. The End Leg [[settlement]] Date is April 
30, 2020 and the End Leg [[settlement]] Amount for the overnight repo is $ 51,005,489.58.  
[[Member]] Reference Numbers 88ZT 899A 
Message Reference 0000035607 0000062113 
External Reference 739B200429135 WLP50429202015 
New External Reference N/A N/A 
[[Broker]] Reference N/A N/A 
[[GSD]] Reference (TID)  003FB8-0429 003FC2-0429 
Secondary Reference N/A N/A 
 
The message samples presented on the following pages are all based on the above scenario.  
C2.a MT515 Repo Dealer [[Member]] 88ZT Submits Repo Transaction to [[GSD]] 
C2.b MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 88ZT 
C2.c MT518 Comparison Request sent to Repo Dealer [[Member]] 899A 
C2.d MT515 Repo Dealer [[Member]] 899A Submits Reverse Repo Transaction to [[GSD]] 
C2.e MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 899A 
C2.f MT518 Comparison Request sent to Repo Dealer [[Member]] 88ZT 
C2.g MT509 Trade Compared Record sent to Repo Dealer [[Member]] 88ZT 
C2.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 899A 
C2.i MT509 Trade Compared Record sent to Repo Dealer [[Member]] 899A 
C2.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 88ZT 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are s olely intended to demonstrate how 
various records might be populated. Also, these sample messages are only those messages that would be generated from 
the Comparison system and not those that would be generated from the Netting system (netting and/or settl ement 
messages). You may refer to the most current “[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output” 
document for netting and/or [[settlement]] related messages.  
  

---

## Page 182

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 182 
Sample C2.a MT515 Repo Dealer [[Member]] 88ZT  Submits Repo Transaction to [[GSD]] 
Message Content  Comments 
GOVXNT [[GSD]] Assigned Unique Identifier  
88ZT Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//0000035607 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200429080231 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::MAST//739B200429135 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200429080112 Trade Date and Time 
:98A::SETT//20200429 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/INST Instruct Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART899A [[Buyer]] (Reverse Party) Information - Contra -party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88ZT [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810SC3 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  

---

## Page 183

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 183 
Sample C2.a MT515 Repo Dealer [[Member]] 88ZT  Submits Repo Transaction to [[GSD]] 
:98A::REPU//20200430 End Leg [[settlement]] Date 
:92A::REPO//3,875 Repo Rate 
:19A::REPA//USD51005489,58 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message 
 
 
 
 
 
 
 
 
 
  

---

## Page 184

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 184 
Sample C2.b MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 88ZT 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
88ZT Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000000314 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200429080240 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//739B200429135 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//0000035607 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:LINK   
:20C::LIST//003FB8-0429 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
  

---

## Page 185

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 185 
Sample C2.c MT518 Comparison Request sent to Repo Dealer [[Member]] 899A  
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
518/000/GSCC Message Type 
899A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000000317 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200429080243 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200429080112 Trade Date and Time 
:98A::SETT//20200429 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART899A [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88ZT [[Seller]] (Repo Party) Information - Contra -party [[ID]] 
:20C::PROC//739B200429135 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912810SC3 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200430 End Leg [[settlement]] Date 
:92A::REPO//3,875 Repo Rate 

---

## Page 186

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 186 
Sample C2.c MT518 Comparison Request sent to Repo Dealer [[Member]] 899A  
:19A::REPA//USD51005489,58 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 187

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 187 
Sample C2.d MT515 Repo Dealer [[Member]] 899A  Submits Reverse Repo Transaction  to [[GSD]] 
Message Content  Comments 
WGSOZT [[GSD]] Assigned Unique Identifier  
899A Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//0000062113 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200429082022 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::MAST//WLP50429202015 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200429080112 Trade Date and Time 
:98A::SETT//20200429 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/INST Instruct Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART899A [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88ZT [[Seller]] (Repo Party) Information - Contra -party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810SC3 Identification of Financial Instrument ([[CUSIP]] Number)  
:16S:CONFDET   
:16R:REPO  

---

## Page 188

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 188 
Sample C2.d MT515 Repo Dealer [[Member]] 899A  Submits Reverse Repo Transaction  to [[GSD]] 
:98A::REPU//20200430 End Leg [[settlement]] Date 
:92A::REPO//3,875 Repo Rate 
:19A::REPA//USD51005489,58 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
  

---

## Page 189

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 189 
Sample C2.e MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 899A 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
899A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001528 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200429082031 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//WLP50429202015 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//0000062113 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:LINK   
:20C::LIST//003FC2-0429 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 190

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 190 
Sample C2.f MT518 Comparison Request sent to Repo Dealer [[Member]] 88ZT 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
518/000/GSCC Message Type 
88ZT Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001531 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200429082042 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200429080112 Trade Date and Time 
:98A::SETT//20200429 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART899A [[Buyer]] (Reverse Party) Information - Contra -party [[ID]] 
:20C::PROC//WLP50429202015 [[Buyer]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88ZT [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810SC3 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200430 End Leg [[settlement]] Date 
:92A::REPO//3,875 Repo Rate 

---

## Page 191

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 191 
Sample C2.f MT518 Comparison Request sent to Repo Dealer [[Member]] 88ZT 
:19A::REPA//USD51005489,58 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 192

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 192 
Sample C2.g MT509 Trade Compared Record sent to Repo Dealer [[Member]] 88ZT 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
88ZT Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001537 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200429082104 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//739B200429135 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//003FB8-0429 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:20C::PROG//WLP50429202015 Contra -party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 193

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 193 
Sample C2.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 899A 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
518/000/GSCC Message Type 
899A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001542 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200429082114 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200429080112 Trade Date and Time 
:98A::SETT//20200429 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CADV Comparison Request Cancel Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART899A [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88ZT [[Seller]] (Repo Party) Information - Contra -party [[ID]] 
:20C::PROC//739B200429135 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810SC3 Identification of Financial Instrument/Security ([[CUSIP]])  
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match  

---

## Page 194

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 194 
Sample C2.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 899A 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200430 End Leg [[settlement]] Date 
:92A::REPO//3,875 Repo Rate 
:19A::REPA//USD51005489,58 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
  

---

## Page 195

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 195 
Sample C2.i MT509 Trade Compared Record sent to Repo Dealer [[Member]] 899A  
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
899A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001548 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200429082123 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//WLP50429202015 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//003FC2-0429 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:20C::PROG//739B200429135 Contra -party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 196

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 196 
Sample C2.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 88ZT 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
518/000/GSCC Message Type 
88ZT Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001556 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200429082125 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200429080112 Trade Date and Time 
:98A::SETT//20200429 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/CADV Comparison Request Cancel Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART899A [[Buyer]] (Reverse Party) Information - Contra -party [[ID]] 
:20C::PROC//WLP50429202015 [[Buyer]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88ZT [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810SC3 Identification of Financial Instrument/Security ([[CUSIP]])  

---

## Page 197

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 197 
Sample C2.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 88ZT 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200430 End Leg [[settlement]] Date 
:92A::REPO//3,875 Repo Rate 
:19A::REPA//USD51005489,58 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 198

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 198 
Sample # C3 – Bilateral Next-Day Starting Transaction Canceled Post-Comparison   
On April 20, 2020, Repo Dealer [[Member]] 8877 executes a term next-day starting repo transaction with Repo 
Dealer [[Member]] 890A for 50,000,000 of U.S. Treasury Bond – [[CUSIP]] 912810RV2. The Contract Repo Rate is 
3.10% and the Start Leg [[settlement]] Amount is $70,000,000.00. The End Leg [[settlement]] Date is April 23, 2020 
and the End Leg [[settlement]] Amount is $70,018,083.33. On April 20, 2020, both counterparties decide to 
cancel the trade. 
[[Member]] Reference Numbers 8877 890A 
Message Reference 000005670014 000000110022 
External Reference 2020NUM0069504 GOVRV2069504 
New External Reference N/A N/A 
[[Broker]] Reference N/A N/A 
[[GSD]] Reference (TID)  001F5B-0420 001F78-0420 
Secondary Reference N/A N/A 
 
The message samples presented on the following pages are all based on the above scenario.  
C3.a MT515 Repo Dealer [[Member]] 8877 Submits Repo Transaction to [[GSD]] 
C3.b MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 8877 
C3.c MT518 Comparison Request sent to Repo Dealer [[Member]] 890A 
C3.d MT515 Repo Dealer [[Member]] 890A Submits Reverse Repo Transaction to [[GSD]] 
C3.e MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 890A 
C3.f. MT518 Comparison Request sent to Repo Dealer [[Member]] 8877 
C3.g MT509 Trade Compared Record sent to Repo Dealer [[Member]] 8877 
C3.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 890A 
C3.i MT509 Trade Compared Record sent to Repo Dealer [[Member]] 890A 
C3.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8877 
C3.k MT515 Repo Dealer [[Member]] 8877 Submits Cancel (post comparison) to [[GSD]] 
C3.l MT509 Cancel Accepted Record sent to Repo Dealer [[Member]] 8877 
C3.m MT518 Cancel Requested sent to Repo Dealer [[Member]] 890A 
C3.n MT515 Repo Dealer [[Member]] 890A Submits Cancel (post comparison) to [[GSD]] 
C3.o MT509 Cancel Accepted Record sent to Repo Dealer [[Member]] 890A 

---

## Page 199

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 199 
C3.p MT518 Cancel Requested sent to Repo Dealer [[Member]] 8877 
C3.q MT509 Trade Canceled sent to Repo Dealer [[Member]] 8877 
C3.r MT509 Trade Canceled sent to Repo Dealer [[Member]] 890A 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated. Also, these sample messages are only those messages that would be generated from 
the Comparison system and not those that would be generated from the Netting system (netting and/or [[settlement]] 
messages). You may refer to the most current “[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output” 
document for netting and/or [[settlement]] related me ssages.  
 
 
 
 
 
 
 
 
 
  

---

## Page 200

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 200 
Sample C3.a MT515 Repo Dealer [[Member]] 8877 Submits Repo Tra nsaction to [[GSD]] 
Message Content  Comments 
TZDSFL [[GSD]] Assigned Unique Identifier  
8877 Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//000005670014 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200420070210 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indic ator 
:16R:LINK   
:20C::MAST//2020NUM0069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200420070104 Trade Date and Time 
:98A::SETT//20200420 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD70000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/INST Instruct Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART890A [[Buyer]] (Reverse Party) Information - Contra -party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8877 [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810RV2 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  

---

## Page 201

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 201 
Sample C3.a MT515 Repo Dealer [[Member]] 8877 Submits Repo Tra nsaction to [[GSD]] 
:98A::REPU//20200423 End Leg [[settlement]] Date 
:92A::REPO//3,1 Repo Rate 
:19A::REPA//USD70018083,33 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 202

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 202 
Sample C3.b MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 8877 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
8877 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001106 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200420070216 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//2020NUM0069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//000005670014 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:LINK   
:20C::LIST//001F5B-0420 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 203

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 203 
Sample C3.c MT518 Comparison Request sent to Repo Dealer [[Member]] 890A  
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
518/000/GSCC Message Type 
890A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001110 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200420070226 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200420070104 Trade Date and Time 
:98A::SETT//20200420 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD70000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade  Record  
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART890A [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8877 [[Seller]] (Repo Party) Information - Contra -party [[ID]] 
:20C::PROC//2020NUM0069504 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810RV2 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200423 End Leg [[settlement]] Date 
:92A::REPO//3,1 Repo Rate 

---

## Page 204

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 204 
Sample C3.c MT518 Comparison Request sent to Repo Dealer [[Member]] 890A  
:19A::REPA//USD70018083,33 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 205

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 205 
Sample C3.d MT515 Repo Dealer [[Member]] 890A Submits Reverse Repo Transaction to [[GSD]] 
Message Content  Comments 
FGSCDB [[GSD]] Assigned Unique Identifier  
890A Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//000000110022 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200420070456 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::MAST// GOVRV2069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200420070104 Trade Date and Time 
:98A::SETT//20200420 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD70000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/INST Instr uct Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART890A [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8877 [[Seller]] (Repo Party) Information - Contra -party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810RV2 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  

---

## Page 206

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 206 
Sample C3.d MT515 Repo Dealer [[Member]] 890A Submits Reverse Repo Transaction to [[GSD]] 
:98A::REPU//20200423 End Leg [[settlement]] Date 
:92A::REPO//3,1 Repo Rate 
:19A::REPA//USD70018083,33 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
  

---

## Page 207

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 207 
Sample C3.e MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 890A 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
890A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001185 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200420070502 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//GOVRV2069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//000000110022 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:LINK   
:20C::LIST//001F78-0420 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 208

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 208 
Sample C3.f MT518 Comparison Request sent to Repo Dealer [[Member]] 8877 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
518/000/GSCC Message Type 
8877 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001189 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200420070511 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200420070104 Trade Date and Time 
:98A::SETT//20200420 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD70000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART890A [[Buyer]] (Reverse Party) Information - Contra -party [[ID]] 
:20C::PROC//GOVRV2069504 [[Buyer]]’s (Contra) Exte rnal Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8877 [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810RV2 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200423 End Leg [[settlement]] Date 
:92A::REPO//3,1 Repo Rate 

---

## Page 209

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output 
Appendices 209 
Sample C3.f MT518 Comparison Request sent to Repo Dealer [[Member]] 8877 
:19A::REPA//USD70018083,33 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 210

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 210 
Sample C3.g MT509 Trade Compared Record sent to Repo Dealer [[Member]] 8877 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
8877 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001198 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200420070335 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//2020NUM0069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//000A08-9829 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:20C::PROG//GOVRV2069504 Contra -party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 211

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 211 
Sample C3.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 890A 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
518/000/GSCC Message Type 
890A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001205 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200420070342 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200420070104 Trade Date and Time 
:98A::SETT//20200420 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD70000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CADV Comparison Request Cancel Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART890A [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8877 [[Seller]] (Repo Party) Information - Contra -party [[ID]] 
:20C::PROC//2020NUM0069504 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810RV2 Identification of Financial Instrument/Security ([[CUSIP]])  

---

## Page 212

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications  for Comparison Input & Output  
Appendices 212 
Sample C3.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 890A 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200423 End Leg [[settlement]] Date 
:92A::REPO//3,1 Repo Rate 
:19A::REPA//USD70018083,33 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
  

---

## Page 213

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 213 
Sample C3.i MT509 Trade Compared Record sent to Repo Dealer [[Member]] 890A  
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
890A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001211 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200420070347 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//GOVRV2069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//001F78-0420 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:20C::PROG//2020NUM0069504 Contra -party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 214

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 214 
Sample C3.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8877 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
518/000/GSCC Message Type 
8877 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001224 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200420070352 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200420070104 Trade Date and Time 
:98A::SETT//20200420 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD70000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/CADV Comparison Request Cancel Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART890A [[Buyer]] (Reverse Party) Information - Contra -party [[ID]] 
:20C::PROC//GOVRV2069504 [[Buyer]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8877 [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810RV2 Identification of Financial Instrument/Security ([[CUSIP]])  

---

## Page 215

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 215 
Sample C3.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8877 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200423 End Leg [[settlement]] Date 
:92A::REPO//3,1 Repo Rate 
:19A::REPA//USD70018083,33 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
  

---

## Page 216

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 216 
Sample C3.k MT515 Repo Dealer [[Member]] 8877 Submits Cancel (post comparison) to [[GSD]]  
Message Content  Comments 
TZDSFL [[GSD]] Assigned Unique Identifier  
8877 Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//000005670065 Sender’s Message Reference Number  
:23G:CANC Cancel Message 
:98C::PREP//20200420083816 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::MAST//2020NUM0069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200420070104 Trade Date and Time 
:98A::SETT//20200420 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD70000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/CANC Cancel Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART890A [[Buyer]] (Reverse Party) Information - Contra -party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8877 [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  

---

## Page 217

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 217 
Sample C3.k MT515 Repo Dealer [[Member]] 8877 Submits Cancel (post comparison) to [[GSD]]  
:35B:/US/912810RV2 Identification of Financial Instrument/Securit y ([[CUSIP]]) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200423 End Leg [[settlement]] Date 
:92A::REPO//3,1 Repo Rate 
:19A::REPA//USD70018083,33 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
  

---

## Page 218

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 218 
Sample C3.l MT509 Cancel Accepted Record sent to Repo Dealer [[Member]] 8877 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
8877 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000003566 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel)  
:98C::PREP//20200420083824 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//2020NUM0069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//000005670065 Related Reference ([[Member]]'s SEME from MT515 Cancel Record)  
:16S:LINK   
:16R:LINK   
:20C::LIST//001F5B-0420 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:STAT   
:25D::CPRC//PACK Cancel Accepted Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 219

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 219 
Sample C3.m MT518 Cancel Requested sent to Repo Dealer [[Member]] 890A 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
518/000/GSCC Message Type 
890A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000003570 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200420083833 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK  
:16R:LINK  
:20C::LIST//001F78-0420 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200420070104 Trade Date and Time 
:98A::SETT//20200420 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD70000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CREQ Cancel Requested Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART890A [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8877 [[Seller]] (Repo Party) Information - Contra -party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  

---

## Page 220

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 220 
Sample C3.m MT518 Cancel Requested sent to Repo Dealer [[Member]] 890A 
:35B:/US/912810RV2 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200423 End Leg [[settlement]] Date 
:92A::REPO//3,1 Repo Rate 
:19A::REPA//USD70018083,33 End Leg [[settlement]] Amount 
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
  

---

## Page 221

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 221 
Sample C3.n MT515 Repo Dealer [[Member]] 890A Submits Cancel (post comparison) to [[GSD]]  
Message Content  Comments 
FGSCDB [[GSD]] Assigned Unique Identifier  
890A Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//000000110099 Sender’s Message Reference Number  
:23G:CANC Cancel Message 
:98C::PREP//20200420084412 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::MAST//GOVRV2069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200420070104 Trade Date and Time 
:98A::SETT//20200420 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD70000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CANC Cancel Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART890A [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8877 [[Seller]] (Repo Party) Information - Contra -party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  

---

## Page 222

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 222 
Sample C3.n MT515 Repo Dealer [[Member]] 890A Submits Cancel (post comparison) to [[GSD]]  
:35B:/US/912810RV2 Identification of Financial Instrument/S ecurity ([[CUSIP]]) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200423 End Leg [[settlement]] Date 
:92A::REPO//3,1 Repo Rate 
:19A::REPA//USD70018083,33 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
 
 
 
  

---

## Page 223

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 223 
Sample C3.o MT509 Cancel Accepted Record sent to Repo Dealer [[Member]] 890A  
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
890A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000003737 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel)  
:98C::PREP//20200420084420 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//GOVRV2069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//000000110099 Related Reference ([[Member]]'s SEME from MT515 Cancel Record)  
:16S:LINK   
:16R:LINK   
:20C::LIST//001F78-0420 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:STAT   
:25D::CPRC//PACK Cancel Accepted Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 224

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 224 
Sample C3.p MT518 Cancel Requested sent to Repo Dealer [[Member]] 8877 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
518/000/GSCC Message Type 
8877 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000003743 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200420084445 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK  
:20C::MAST//2020NUM0069504 Master External Reference Number  
:16S:LINK  
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK  
:16R:LINK  
:20C::LIST//001F5B-0420 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200420070104 Trade Date and Time 
:98A::SETT//20200420 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD70000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/CREQ Cancel Requested Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART890A [[Buyer]] (Reverse Party) Information - Contra -party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   

---

## Page 225

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 225 
Sample C3.p MT518 Cancel Requested sent to Repo Dealer [[Member]] 8877 
:95R::SELL/GSCC/PART8877 [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810RV2 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200423 End Leg [[settlement]] Date 
:92A::REPO//3,1 Repo Rate 
:19A::REPA//USD70018083,33 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
 
 
  

---

## Page 226

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 226 
Sample C3.q MT509 Trade Canceled Record sent to Repo Dealer [[Member]] 8877 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
8877 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000003749 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel)  
:98C::PREP//20200420084452 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//2020NUM0069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//001F5B-0420 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:STAT   
:25D::CPRC//CAND Cancel Processed  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 227

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 227 
Sample C3.r MT509 Trade Canceled Record sent to Repo Dealer [[Member]] 890A  
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
890A Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000003754 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel)  
:98C::PREP//20200420084501 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//GOVRV2069504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//001F78-0420 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:STAT   
:25D::CPRC//CAND Cancel Processed  
:16S:STAT   
:16S:GENL   
- End of Message  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 228

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 228 
Sample # C4 – Demand Next-Day Starting Transaction DK’d, Modified and Compared 
On the morning of April 13, 2020,Repo [[Broker]] [[Member]] 87D3 executes a term next-day starting repo trade with 
Repo Dealer [[Member]] 87P8 for 50,000,000 of U.S. Treasury Note – [[CUSIP]] 912828SV3. The Contract Repo 
Rate is 1.63% and the Start Leg [[settlement]] Amount is $51,500,000.00. The Start Leg [[settlement]] Date is April 
14, 2020, the End Leg [[settlement]] Date is April 17, 2020 and the End Leg [[settlement]] Amount for the term repo 
is $51,506,995.42. On April 13, 2020, the Repo Dealer [[Member]] 87P8 DKs the trade (DK Reason code E998 – 
Trade not found). The Repo [[Broker]] [[Member]] 87D3 modifies the trade to add a Secondary Reference Number. 
The repo transaction is later compared by Repo Dealer [[Member]] 87P8.  
 
[[Member]] Reference Numbers 87D3 87P8 
Message Reference 000001120313 000000141542 
External Reference 2000JCT069104 GSS002010812 
New External Reference N/A N/A 
[[Broker]] Reference R1357245 N/A 
[[GSD]] Reference (TID)  003D43-0413 003E78-0413 
Secondary Reference GSS724635 N/A 
 
The message samples presented on the following pages are all based on the above scenario.  
C4.a MT515 Repo [[Broker]] [[Member]] 87D3 Submits Repo Transaction to [[GSD]] 
C4.b MT509 Trade Accepted Record sent to Repo [[Broker]] [[Member]] 87D3 
C4.c MT518 Comparison Request sent to Repo Dealer [[Member]] 87P8 
C4.d MT515 Repo Dealer [[Member]] 87P8 Submits DK Message to [[GSD]] 
C4.e MT509 Trade DK Accepted (DK submitted via IM) sent to Repo Dealer [[Member]] 87P8            
C4.f MT509 Trade DK Processed (DK submitted via IM) sent to Repo Dealer [[Member]] 87P8 
C4.g MT518 Comparison Request Cancel (due to DK) sent to Repo Dealer [[Member]] 87P8 
C4.h MT518 DK Advice sent to Repo [[Broker]] 87D3              
C4.i MT515 Repo [[Broker]] [[Member]] 87D3 Submits Trade Modify on Repo Transaction to [[GSD]] 
C4.j MT509 Trade Modify Accepted Record sent to Repo [[Broker]] [[Member]] 87D3 
C4.k MT518 Comparison Request sent to Repo Dealer [[Member]] 87P8 
C4.l MT515 Repo Dealer [[Member]] 87P8 Submits Reverse Repo Transaction to [[GSD]] 
C4.m MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 87P8 

---

## Page 229

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 229 
C4.n MT518 Comparison Request sent to Repo [[Broker]] [[Member]] 87D3 
C4.o MT509 Trade Compared Record sent to Repo [[Broker]] [[Member]] 87D3 
C4.p MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 87P8 
C4.q MT509 Trade Compared Record sent to Repo Dealer [[Member]] 87P8 
C4.r MT518 Comparison Request Cancel (due to match) sent to Repo [[Broker]] [[Member]] 87D3 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated. Also, these sample messages are only those messages that would be generated from 
the Comparison system and not those that would be generated from the Netting system (netting and/or [[settlement]] 
messages). You may refer to the most current “[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output” 
document for netting and/or [[settlement]] related me ssages.  
 
  

---

## Page 230

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 230 
Sample C4.a MT515 Repo [[Broker]] [[Member]]  87D3 Submits Repo Transaction to [[GSD]] 
Message Content  Comments 
GRIHEZ [[GSD]] Assigned Unique Identifier  
87D3 Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//000001120313 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200413100745 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::MAST//2000JCT069104 Receiving [[Member]]’s External Reference Number  
:16S:LINK  
:16R:LINK  
:20C::BASK//R1357245 [[Broker]] Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/INST Instruct Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – Contra -Party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  

---

## Page 231

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 231 
Sample C4.a MT515 Repo [[Broker]] [[Member]]  87D3 Submits Repo Transaction to [[GSD]] 
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200417 End Leg [[settlement]] Date 
:92A::REPO//1,63 Repo Rate 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
  

---

## Page 232

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 232 
Sample C4.b MT509 Trade Accepted Record sent to Repo [[Broker]] [[Member]]  87D3 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
87D3 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001018 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200413100752 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//2000JCT069104 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//000001120313 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:LINK   
:20C::LIST//003D43-0413 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:13B::LINK/GSCC/TRDR Linked Message – D emand Repo Trade Indicator  
:20C::BASK//R1357245 [[Broker]] Reference Number  
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status  
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 233

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 233 
Sample C4.c MT518 Comparison Request sent to Repo Dealer [[Member]] 87P8 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
87P8 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001021 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200413100753 Date and Time of Message Preparation  
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – Contra -Party [[ID]] 
:20C::PROC//2000JCT069104 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO   
:98A::REPU//20200417 End Leg [[settlement]] Date 
:92A::REPO//1,63 Repo Rate 

---

## Page 234

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 234 
Sample C4.c MT518 Comparison Request sent to Repo Dealer [[Member]] 87P8 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO   
- End of Message  
  

---

## Page 235

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 235 
Sample C4.d MT515 Repo Dealer [[Member]] 87P8 Submits DK Message to [[GSD]] 
Message Content  Comments 
ZTOPZI [[GSD]] Assigned Unique Identifier  
87P8 Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//000000141542 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200413100758 Date and Time of Message Preparation  
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator  
:16R:LINK   
:20C::MAST//NONREF For DKs this field should be populated with the value “NONREF”.  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/TDDK DK Message Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – Contra -Party [[ID]] 
:20C::PROC//2000JCT069104 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  
:70E::TPRO//GSCC/DKRSE998 Trade Instruction Processing Narrative – DK Reason Code (Trade not found)  

---

## Page 236

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 236 
Sample C4.d MT515 Repo Dealer [[Member]] 87P8 Submits DK Message to [[GSD]] 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200417 End Leg [[settlement]] Date 
:92A::REPO//1,63 Repo Rate 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
  

---

## Page 237

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 237 
Sample C4.e MT509 Trade DK Accepted (DK submitted via IM only) Record sent to Repo Dealer [[Member]] 87P8 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
87P8 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001098 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200413100800 Date and Time of Message Preparation  
:16R:LINK   
:20C::RELA//000000141542 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:LINK   
:20C::PROG//2000JCT069104 Contra -party X-ref (will only appear on MT509 messages related to Comparison 
Notification (e.g., Trade Compared (:25D::MTCH//MACH) and on MT509 
messages providing the status of MT515 DK records submitted to [[GSD]] . 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/PADK Trade DK Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message  
  

---

## Page 238

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 238 
Sample C4.f MT509 Trade DK Processed (DK submitted via IM only) Record sent to Repo Dealer [[Member]]  87P8 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
87P8 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001100 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200413100801 Date and Time of Message Preparation  
:16R:LINK   
:20C::PROG//2000JCT069104 Contra -party X-ref (will only appear on MT509 messages related to Comparison 
Notification (e.g., Trade Compared (:25D::MTCH//MACH) and on MT509 
messages providing the status o f MT515 DK records submitted to [[GSD]] . 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/DPPR Trade DK Processed Status  
:16S:STAT   
:16S:GENL   
- End of Message  
  

---

## Page 239

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 239 
Sample C4.g MT518 Comparison Request Cancel (due to DK) sent to Repo Dealer [[Member]] 87P8 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
87P8 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001102 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200413100802 Date and Time of Message Preparation  
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator  
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CADV Comparison Request Cancel Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – Contra -Party [[ID]] 
:20C::PROC//2000JCT069104 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  

---

## Page 240

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 240 
Sample C4.g MT518 Comparison Request Cancel (due to DK) sent to Repo Dealer [[Member]] 87P8 
:70E::TPRO//GSCC/DKRSE998/ 
MSGRYRAC 
Trade Instruction Processing Narrative- Message Reason due to your Action 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200417 End Leg [[settlement]] Date 
:92A::REPO//1,63 Repo Rate 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message 
  

---

## Page 241

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 241 
Sample C4.h MT518 DK Advice sent to Repo [[Broker]] [[Member]] 87D3 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
87D3 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001104 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Cancel Record Indicator  
:98C::PREP//20200413100802 Date and Time of Message Preparation  
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator  
:16R:LINK   
:20C::MAST//2000JCT069104 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//003D43-0413 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK  
:16R:LINK  
:20C::BASK//R1357245 [[Broker]] Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/NAFI Comparison Request Cancel Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – Contra -Party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   

---

## Page 242

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 242 
Sample C4.h MT518 DK Advice sent to Repo [[Broker]] [[Member]] 87D3 
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  
:70E::TPRO//GSCC/DKRSE998 Trade Instruction Processing Narrative- DK Reason (Trade not found)  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200417 End Leg [[settlement]] Date 
:92A::REPO//1,63 Repo Rate 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
  

---

## Page 243

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 243 
Sample C4.i MT515 Repo [[Broker]] [[Member]]  87D3 Submits Trade Modify on Repo Transaction to [[GSD]] 
Message Content  Comments 
GRIHEZ [[GSD]] Assigned Unique Identifier  
87D3 Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//00000011018 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200413101005 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::MAST//2000JCT069104 Receiving [[Member]]’s External Reference Number  
:16S:LINK  
:16R:LINK  
:20C::BASK//R1357245 [[Broker]] Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/MDFC Modify Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – Contra -Party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  

---

## Page 244

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 244 
Sample C4.i MT515 Repo [[Broker]] [[Member]]  87D3 Submits Trade Modify on Repo Transaction to [[GSD]] 
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200417 End Leg [[settlement]] Date 
:20C::SECO//GSS724635 Secondary Reference Number  
:92A::REPO//1,63 Repo Rate 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
  

---

## Page 245

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 245 
Sample C4.j MT509 Trade Modify Accep ted Record sent to Repo [[Broker]] [[Member]] 87D3 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
87D3 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001128 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200413101016 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//2000JCT069104 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//00000011018 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:LINK   
:20C::LIST//003D43-0413 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:13B::LINK/GSCC/TRDR Linked Message – D emand Repo Trade Indicator  
:20C::BASK//R1357245 [[Broker]] Reference Number  
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/MODA Trade Modification  Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 246

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 246 
Sample C4.k MT518 Comparison Request sent to Repo Dealer [[Member]] 87P8 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
87P8 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001131 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200413101018 Date and Time of Message Preparation  
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – Contra -Party [[ID]] 
:20C::PROC//2000JCT069104 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO   
:98A::REPU//20200417 End Leg [[settlement]] Date 
:20C::SECO//GSS724635 Secondary Reference Number  

---

## Page 247

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 247 
Sample C4.k MT518 Comparison Request sent to Repo Dealer [[Member]] 87P8 
:92A::REPO//1,63 Repo Rate 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO   
- End of Message  
  

---

## Page 248

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 248 
Sample C4.l MT515 Repo Dealer [[Member]]  87P8 Submits Reverse Repo Transaction to [[GSD]] 
Message Content  Comments 
ZTOPZI [[GSD]] Assigned Unique Identifier  
87P8 Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//000000141652 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200413101745 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::MAST//GSS002010812 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/INST Instruct Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – Contra -Party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  

---

## Page 249

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 249 
Sample C4.l MT515 Repo Dealer [[Member]]  87P8 Submits Reverse Repo Transaction to [[GSD]] 
:98A::REPU//20200417 End Leg [[settlement]] Date 
:92A::REPO//1,63 Repo Rate 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
  

---

## Page 250

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 250 
Sample C4.m MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 87P8 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
87P8 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001142 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200413101750 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//GSS002010812 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//000000141652 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:LINK   
:20C::LIST//003E78-0413 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status  
:16S:STAT   
:16S:GENL   
- End of Message  
  

---

## Page 251

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 251 
Sample C4.n MT518 Comparison Request sent to Repo [[Broker]]  [[Member]] 87D3 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
87D3 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001145 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200413101752 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – Contra -Party [[ID]] 
:20C::PROC//GSS002010812 [[Buyer]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO   
:98A::REPU//20200417 End Leg [[settlement]] Date 
:20C::SECO//GSS724635 Secondary Reference Number  

---

## Page 252

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 252 
Sample C4.n MT518 Comparison Request sent to Repo [[Broker]]  [[Member]] 87D3 
:92A::REPO//1,63 Repo Rate 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO   
- End of Message  
  

---

## Page 253

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 253 
Sample C4.o MT509 Trade Compared  Record sent to Repo [[Broker]] [[Member]]  87D3 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
87D3 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001148 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200413101756 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//2000JCT069104 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//003D43-0413 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:20C::PROG//GSS002010812 Contra -Party’s External Reference Number 
:16S:LINK   
:16R:LINK   
:13B::LINK/GSCC/TRDR Linked Message – D emand Repo Trade Indicator  
:20C::BASK//R1357245 [[Broker]] Reference Number  
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared  Status 
:16S:STAT   
:16S:GENL   
- End of Message  
  

---

## Page 254

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 254 
Sample C4.p MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 87P8 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
87P8 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001150 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200413101756 Date and Time of Message Preparation  
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator  
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CADV Comparison Request Cancel Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – Contra -Party [[ID]] 
:20C::PROC//2000JCT069104 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match  

---

## Page 255

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 255 
Sample C4.p MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 87P8 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200417 End Leg [[settlement]] Date 
:92A::REPO//1,63 Repo Rate 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message 
  

---

## Page 256

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output 
Appendices 256 
Sample C4.q MT509 Trade Compared Record sent to Repo Dealer [[Member]] 87P8 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
87P8 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001152 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200413101758 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//GSS002010812 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//003E78-0413 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:20C::PROG//2000JCT069104 Contra -Party External Reference Number  
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared  Status 
:16S:STAT   
:16S:GENL   
- End of Message  
  

---

## Page 257

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 257 
Sample C4.r MT518 Comparison Request Cancel (due to match) sent to Repo [[Broker]]  [[Member]] 87D3 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
87D3 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001158 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200413101758 Date and Time of Message Preparation  
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator  
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200413100732 Trade Date and Time 
:98A::SETT//20200414 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD51500000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/CADV Comparison Request Cancel Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART87P8 [[Buyer]] (Reverse Party) Information – Contra -Party [[ID]] 
:20C::PROC//GSS002010812 [[Buyer]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87D3 [[Seller]] (Repo Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912828SV3 Identification of Financial Instrument/Security ([[CUSIP]])  
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match  

---

## Page 258

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 258 
Sample C4.r MT518 Comparison Request Cancel (due to match) sent to Repo [[Broker]]  [[Member]] 87D3 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200417 End Leg [[settlement]] Date 
:92A::REPO//1,63 Repo Rate 
:19A::REPA//USD51506995,42, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
 
 
 
 
  

---

## Page 259

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications  for Comparison Input & Output  
Appendices 259 
Sample # C5 – Repo Substitution Processed on Demand Trade 
April 27, 2020 – Repo Start 
On August 21, 2019, Repo [[Broker]] [[Member]] 88R1 executes a term same-day starting Repo transaction with 
Repo Dealer [[Member]] 8523 for 50,000,000 of U.S. Treasury Bond – [[CUSIP]] 912810QX9. The Contract Repo 
Rate is 2.75% and the Start Leg [[settlement]] Amount is $50,000,000. The End Leg [[settlement]] Date is 
December 31, 2020 and the End Leg [[settlement]] Amount is $50,947,222.22 
April 29, 2020 – Repo Substitution 
At 09:00 AM ET on Aril 29, 2020, Repo [[Broker]] [[Member]] 88R1 enters a repo [[collateral]] substitution request 
notification into [[GSD]] RTTM Web for the above referenced trade. The request consist of substituting the current 
[[collateral]] with 50,000,000 of U.S. Treasury Bond – [[CUSIP]] 912810QY7, Contract Repo Rate is 2.75%, Start 
Leg [[settlement]] Amount is $50,250,000 with an End Leg [[settlement]] Amount of $51,201,958.33.  
Current [[collateral]]  Replacement [[collateral]] 
[[CUSIP]] 912810QX9  [[CUSIP]] 912810QY7 
Repo Rate 2.75%  Repo Rate 2.75% 
Start Amount  50,000,000  Start Amount  50,250,000 
Final Money  50,947,222.22  Final Money  51,201,958.33 
 
Note:  
Currently, [[GSD]] does not support the interactive messaging input of a repo [[collateral]] substitution request via interactive 
messaging. All repo [[collateral]] repo substitution requests must be entered via the [[GSD]] RTTM Web application.  
Note:  
Currently, the Contract Repo Rate on a repo transaction cannot be changed through a repo [[collateral]] substitution request.  
 
[[Member]] Reference Numbers 88R1 8523 
Message Reference 00000052074 000001108555 
External Reference RNB09C07001006 RP000V2001357 
New External Reference N/A N/A 
[[Broker]] Reference BRKR9C07 N/A 
[[GSD]] Reference (TID)  002C0B-0427 002F08-0427 
Secondary Reference N/A N/A 
 
  

---

## Page 260

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 260 
For the purposes of this example, assume the following: 
• Repo [[Broker]] [[Member]] 88R1 has also executed a term same-day starting Reverse Repo transaction of 
equal value with another Repo Dealer [[Member]], the details of which will not be included in this scenario 
• All trades have been bilateral compared on trade date/start date.  
• The Start Leg settles on April 27. 2020.  
• Repo [[Broker]] [[Member]] 88R1 also enters a repo [[collateral]] substitution request notification in [[GSD]] RTTM 
Web to substitute the [[collateral]] for their Reverse Repo transaction referenced above. 
 
The message samples presented on the following pages are all based on the above scenario.  
C5.a MT515 Repo [[Broker]] [[Member]] 88R1 Submits Repo Transaction to [[GSD]] 
C5.b MT509 Trade Accepted Record sent to Repo [[Broker]] [[Member]] 88R1 
C5.c MT518 Comparison Request sent to Repo Dealer [[Member]] 8523 
C5.d MT515 Repo Dealer [[Member]] 8523 Submits Reverse Repo Transaction to [[GSD]] 
C5.e MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 8523 
C5.f MT518 Comparison Request sent to Repo [[Broker]] [[Member]] 88R1 
C5.g MT509 Trade Compared Record sent to Repo [[Broker]] [[Member]] 88R1 
C5.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8523 
C5.i MT509 Trade Compared Record sent to Repo Dealer [[Member]] 8523 
C5.j MT518 Comparison Request Cancel (due to match) sent to Repo [[Broker]] [[Member]] 88R1 
C5.k MT518 Notification of Repo Substitution Details sent to Repo Dealer [[Member]] 8523 
C5.l MT518 Notification of Repo Substitution Details sent to Repo [[Broker]] [[Member]] 88R1 
C5.m MT509 Repo Substitution Processed sent to Repo Dealer [[Member]] 8523 
C5.n MT509 Repo Substitution Processed sent to Repo [[Broker]] [[Member]] 88R1 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrat e how 
various records might be populated. Also, these sample messages are only those messages that would be generated from 
the Comparison system and not those that would be generated from the Netting system (netting and /or [[settlement]] 
messages). You may ref er to the most current “[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output” 
document for netting and/or [[settlement]] related messages.  
  

---

## Page 261

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 261 
Sample C5.a MT515 Repo [[Broker]] [[Member]]  88R1 Submits Repo Transaction to [[GSD]] 
Message Content  Comments 
KR13E2 [[GSD]] Assigned Unique Identifier  
88R1 Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
:16R:GENL   
:20C::SEME//00000052074 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200427100858 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::MAST//RNB09C07001006 Receiving [[Member]]’s External Reference Number  
:16S:LINK  
:16R:LINK  
:20C::BASK//BRKR9C07 [[Broker]] Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200427100854 Trade Date and Time 
:98A::SETT//20200427 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD50000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/INST Instruct Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8523 [[Buyer]] (Reverse Party) Information – Contra -Party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88R1 [[Seller]] (Repo Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  

---

## Page 262

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 262 
Sample C5.a MT515 Repo [[Broker]] [[Member]]  88R1 Submits Repo Transaction to [[GSD]] 
:35B:/US/912810QX9 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20201231 End Leg [[settlement]] Date 
:92A::REPO//2,75 Repo Rate 
:19A::REPA//USD50947222,22, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
  

---

## Page 263

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 263 
Sample C5.b MT509 Trade Accepted Record sent to Repo [[Broker]] [[Member]]  88R1 
Message Content Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
88R1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001428 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200427100916 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//RNB09C07001006 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//00000052074 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:LINK   
:20C::LIST//002C0B-0427 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:13B::LINK/GSCC/TRDR Linked Message – D emand Repo Trade Indicator  
:20C::BASK//BRKR9C07 [[Broker]] Reference Number  
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
  

---

## Page 264

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 264 
Sample C5.c MT518 Comparison Request sent to Repo Dealer [[Member]] 8523 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
8523 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001431 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200427100921 Date and Time of Message Preparation  
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200427100854 Trade Date and Time 
:98A::SETT//20200427 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD50000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8523 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88R1 [[Seller]] (Repo Party) Information – Contra -Party [[ID]] 
:20C::PROC//RNB09C07001006 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912810QX9 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO   
:98A::REPU//20201231 End Leg [[settlement]] Date 
:92A::REPO//2,75 Repo Rate 

---

## Page 265

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 265 
Sample C5.c MT518 Comparison Request sent to Repo Dealer [[Member]] 8523 
:19A::REPA//USD50947222,22, End Leg [[settlement]] Amount  
:16S:REPO   
- End of Message  
 
  

---

## Page 266

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 266 
Sample C5.d MT515 Repo Dealer [[Member]] 8523 Submits Reverse Repo Transaction to [[GSD]] 
Message Content  Comments 
GSPSWL [[GSD]] Assigned Unique Identifier  
8523 Sender [[ID]] ( [[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ( [[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//000001108555 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input  
:98C::PREP//20200427101201 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::MAST//RP000V2001357 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200427100854 Trade Date and Time 
:98A::SETT//20200427 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD50000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/INST Instruct Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8523 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88R1 [[Seller]] (Repo Party) Information – Contra -Party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810QX9 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  

---

## Page 267

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 267 
Sample C5.d MT515 Repo Dealer [[Member]] 8523 Submits Reverse Repo Transaction to [[GSD]] 
:98A::REPU//20201231 End Leg [[settlement]] Date 
:92A::REPO//2,75 Repo Rate 
:19A::REPA//USD50947222,22, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
  

---

## Page 268

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 268 
Sample C5.e MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 8523 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
8523 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001511 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200427101212 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//RP000V2001357 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::RELA//000001108555 Related Reference ([[Member]]'s SEME from MT515 Instruct Message)  
:16S:LINK   
:16R:LINK   
:20C::LIST//002F08-0427 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
  

---

## Page 269

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 269 
Sample C5.f MT518 Comparison Request sent to Repo [[Broker]] [[Member]]  88R1 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
88R1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001515 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200427101216 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200427100854 Trade Date and Time 
:98A::SETT//20200427 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD50000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8523 [[Buyer]] (Reverse Party) Information – Contra -Party [[ID]] 
:20C::PROC//RP000V2001357 [[Buyer]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88R1 [[Seller]] (Repo Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810QX9 Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20201231 End Leg [[settlement]] Date 
:92A::REPO//2,75 Repo Rate 

---

## Page 270

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 270 
Sample C5.f MT518 Comparison Request sent to Repo [[Broker]] [[Member]]  88R1 
:19A::REPA//USD50947222,22, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
  

---

## Page 271

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 271 
Sample C5.g MT509 Trade Compared Record sent to Repo [[Broker]] [[Member]]  88R1 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
88R1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001519 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200427101221 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//RNB09C07001006 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//002C0B-0427 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:20C::PROG//RP000V2001357 Contra -party External Reference Number 
:16S:LINK  
:16R:LINK  
:13B::LINK/GSCC/TRDR Linked Message – D emand Repo Trade Indicator  
:20C::BASK//BRKR9C07 [[Broker]] Reference Number  
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
  

---

## Page 272

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 272 
Sample C5.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8523 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
8523 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001520 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200427101222 Date and  Time of Message Preparation  
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator  
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200427100854 Trade Date and Time 
:98A::SETT//20200427 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD50000000, Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/CADV Comparison Request Cancel Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8523 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88R1 [[Seller]] (Repo Party) Information – Contra -Party [[ID]] 
:20C::PROC//RNB09C07001006 [[Seller]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810QX9 Identification of Financial Instrument/Security ([[CUSIP]])  
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match  

---

## Page 273

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 273 
Sample C5.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8523 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20201231 End Leg [[settlement]] Date 
:92A::REPO//2,75 Repo Rate 
:19A::REPA//USD50947222,22, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
 
  

---

## Page 274

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 274 
Sample C5.i MT509 Trade Compared Record sent to Repo Dealer [[Member]] 8523 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
509/000/GSCC Message Type 
8523 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001525 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200427101222 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//RP000V2001357 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//002F08-0427 [[GSD]] Assigned Reference Number (Receiver’s TID)  
:16S:LINK   
:16R:LINK   
:20C::PROG//RNB09C07001006 Contra -party External Reference Number 
:16S:LINK   
:16R:LINK   
:13B::LINK/GSCC/REPO Linked Message – R epo Trade Indicator  
:20C::BASK//002C0B-0427 [[Broker]] (Counterparty) Reference Number ([[Broker]] Xref or [[Broker]] TID) 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status  
:16S:STAT   
:16S:GENL   
- End of Message  
 
  

---

## Page 275

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 275 
Sample C5.j MT518 Comparison Request Cancel (due to match) sent to Repo [[Broker]] [[Member]]  88R1 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
88R1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001527 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator  
:98C::PREP//20200427101224 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages  
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200427100854 Trade Date and Time 
:98A::SETT//20200427 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO)  
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD50000000, Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/CADV Comparison Request Cancel Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8523 [[Buyer]] (Reverse Party) Information – Contra -Party [[ID]] 
:20C::PROC//RP000V2001357 [[Buyer]]’s (Contra) External Reference Number  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88R1 [[Seller]] (Repo Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount)  
:35B:/US/912810QX9 Identification of Financial Instrument/Security ([[CUSIP]])  
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match  

---

## Page 276

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 276 
Sample C5.j MT518 Comparison Request Cancel (due to match) sent to Repo [[Broker]] [[Member]]  88R1 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20201231 End Leg [[settlement]] Date 
:92A::REPO//2,75 Repo Rate 
:19A::REPA//USD50947222,22, End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message 
 
  

---

## Page 277

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 277 
Sample C5.k MT518 Notification of Repo Substitution Details  sent to Repo Dealer [[Member]] 8523 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
8523 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001513 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200429090032 Date and Time of Message Preparation  
:22F::TRTR/GSCC/REPO Repo Trade Indicator  
:16R:LINK  
:20C::MAST//RP000V2001357 Receiving [[Member]]’s External Reference Number  (of trade modified by R epo 
Substitution)  
:16S:LINK  
:16R:LINK  
:20C::LIST//002F08-0427 [[GSD]] Assigned Reference Number (Receiver’s TID)  (of trade modified by Repo 
Substitution)  
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200427100854 Original Trade Date and Time 
:98A::SETT//20200427 Start Leg [[settlement]] Date 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD50250000, Original Start Leg [[settlement]] Amount  or New Start Leg [[settlement]] Amount  
:22H::BUSE//BUYI Buy (REVR) Trade Record  
:22F::PROC/GSCC/RPSD Repo Substitution Details Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8523 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88R1 [[Seller]] (Repo Party) Information – Contra -Party [[ID]] 

---

## Page 278

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 278 
Sample C5.k MT518 Notification of Repo Substitution Details  sent to Repo Dealer [[Member]] 8523 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Original Quantity of Security or New Quantity of Security (FAMT = Face 
Amount) 
:35B:/US/912810QY7 New Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO   
:98A::REPU//20201231 End Leg [[settlement]] Date 
:92A::REPO//2,75 Repo Rate 
:19A::REPA//USD51201958,33 End Leg [[settlement]] Amount  
:16S:REPO   
- End of Message  
  

---

## Page 279

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 279 
Sample C5.l MT518 Notification of Repo Substitution Details  sent to Repo [[Broker]] [[Member]]  88R1 
Message Content  Comments 
  Password  - Blank on MT 518 
GSCCTRRS Sender [[ID]] ( [[GSD]] Trade Registration and Reconciliation System ) 
518/000/GSCC Message Type 
88R1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001515 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator  
:98C::PREP//20200429090033 Date and Time of Message Preparation  
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator  
:16R:LINK  
:20C::MAST//RNB09C07001006 Receiving [[Member]]’s External Reference Number (of trade modified by R epo 
Substitution)  
:16S:LINK  
:16R:LINK  
:20C::LIST//002C0B-0427 [[GSD]] Assigned Reference Number (Receiver’s TID)  (of trade modified by Repo 
Substitution)  
:16S:LINK  
:16R:LINK  
:20C::BASK//BRKR9C07 [[Broker]] Reference Number  
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200427100854 Original Trade Date and Time 
:98A::SETT//20200427 Start Leg [[settlement]] Date 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade)  
:19A::SETT//USD50250000, Original Start Leg [[settlement]] Amount  or New Start Leg [[settlement]] Amount  
:22H::BUSE//SELL Sell (REPO) Trade Record  
:22F::PROC/GSCC/RPSD Repo Substitution Details  Record  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8523 [[Buyer]] (Reverse Party) Information – Contra -Party [[ID]] 

---

## Page 280

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 280 
Sample C5.l MT518 Notification of Repo Substitution Details  sent to Repo [[Broker]] [[Member]]  88R1 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART88R1 [[Seller]] (Repo Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Original Quantity of Security or New Quantity of Security (FAMT = Face 
Amount) 
:35B:/US/912810QY7 New Identification of Financial Instrument/Security ([[CUSIP]])  
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20201231 End Leg [[settlement]] Date 
:92A::REPO//2,75 Repo Rate 
:19A::REPA//USD51201958,33 End Leg [[settlement]] Amount  
:16S:REPO  
- End of Message  
  

---

## Page 281

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 281 
Sample C5.m MT509 Repo Substitution Processed sent to Repo Dealer [[Member]] 8523 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
8523 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001517 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200429090033 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//RP000V2001357 Receiving [[Member]]’s External Reference Number  (of trade modified by Repo 
Substitution)  
:16S:LINK   
:16R:LINK   
:20C::LIST//002F08-0427 [[GSD]] Assigned Reference Number (Receiver’s TID)  (of trade modified by Repo 
Substitution)  
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/RPSP Repo Substitution Processed  
:16S:STAT   
:16S:GENL   
- End of Message  
  

---

## Page 282

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 282 
Sample C5.n MT509 Repo Substitution Processed sent to Repo [[Broker]] [[Member]]  88R1 
Message Content  Comments 
  Password  - Blank on MT 509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
509/000/GSCC Message Type 
88R1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000001520 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction)  
:98C::PREP//20200429090033 Date and Time of Message Preparation  
:16R:LINK   
:20C::MAST//RNB09C07001006 Receiving [[Member]]’s External Reference Number  (of trade modified by R epo 
Substitution)  
:16S:LINK   
:16R:LINK   
:20C::LIST//002C0B-0427 [[GSD]] Assigned Reference Number (Receiver’s TID)  (of trade modified by Repo 
Substitution)  
:16S:LINK   
:16R:LINK   
:13B::LINK/GSCC/TRDR Linked Message – D emand Repo Trade Indicator  
:20C::BASK//BRKR9C07 [[Broker]] Reference Number  
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/RPSP Repo Substitution Processed  
:16S:STAT   
:16S:GENL   
- End of Message  
  

---

## Page 283

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 283 
Sample # C6 – Various MT599 Administrative Messages 
The message samples presented on the following pages are listed below:  
C6.a MT599 DVP System – Start of Day Notification Administrative Message 
C6.b MT599 DVP System – End of Day Submission Cutoff Administrative Message 
C6.c MT599 DVP System – End of Day Processing Completed Administrative Message 
C6.d MT599 DVP System – Demand Trade Submission Cutoff Administrative Message 
C6.e MT599 DVP System – DK Submission Cutoff Administrative Message 
C6.f MT599  GCF/CCIT System – Start of Day Notification Administrative Message 
C6.g MT599 GCF/CCIT System – End of Day Submission Cutoff Administrative Message 
C6.h MT599 GCF/CCIT System – Net Processing Administrative Message 
C6.i MT599 GCF/CCIT System – End of Day Processing Completed Administrative Message 
 
 
 
 
 
 
 
 
 
 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated.  
 
 
 

---

## Page 284

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 284 
C6.a MT599 DVP System – Start of Day Notification Administrative Message 
 Password  - Blank on MT 599 
GSCCTRRS  Sender  [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
599/000/GSCC   Message Type 
88Z1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:20:0000000778898105 Transaction Message Reference Number  
:79:GSCC/GADM/PREP/20200506060143 
/GSOD/20200506 
DVP Start of Day Notification Administrative Message with 
Preparation Date/ Time stamp  and Current Business Date included  
 
 
C6.b MT599 DVP System – End of Day Submission Cutoff Administrative Message 
 Password  - Blank on MT 599 
GSCCTRRS  Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
599/000/GSCC   Message Type 
88Z1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:20:0000000394891036 Transaction Message Reference Number  
:79:GSCC/GADM/PREP/20200505200326 
/EDCS/20200505/NXTD/20200506 
DVP End of Day Submission Cutoff Administrative Message with 
Preparation Date/Time stamp, Current Business Date, Next Day 
Trade Submission qualifier with the Next Business Date included  
 
 
C6.c MT599 DVP System – End of Day Processing Completed Administrative Message 
 Password  - Blank on MT 599 
GSCCTRRS  Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
599/000/GSCC   Message Type 
88Z1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:20:0000000395299376 Transaction Message Reference Number  
:79:GSCC/GADM/PREP/20200505214823 
/EODC/20200506/NXTD/20200507 
DVP End of Day Processing Completed Administrative Message 
with Preparation Date/Time stamp, Current Business Date, Next 
Day Trade Submission quali fier with the Next Business Date 
included  
 
 
  

---

## Page 285

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 285 
C6.d MT599 DVP System – Demand Trade Submission Cutoff Administrative Message 
 Password  - Blank on MT 599 
GSCCTRRS  Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
599/000/GSCC   Message Type 
88Z1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:20:0000000788923485 Transaction Message Reference Number  
:79:GSCC/GADM/PREP/20200505160031 
/SCDM/20200505/NXTD/20200506 
Demand Trade Submission Cutoff Administrative Message with 
Preparation Date/Time stamp, Current Business Date, Next Day 
Trade Submission qualifier with the Next Business Date included  
 
 
C6.e MT599 DVP System – DK Submission Cutoff Administrative Message 
 Password  - Blank on MT 599 
GSCCTRRS  Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System)  
599/000/GSCC   Message Type 
88Z1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:20:0000000778899915 Transaction Message Reference Number  
:79:GSCC/GADM/PREP/20200505163006 
/SCDK/20200505/NXTD/20200506 
DK Submission Cutoff Administrative Message with Preparation 
Date/Time stamp, Current Business Date, Next Day Trade 
Submission qualifier with the Next Business Date included  
 
 
C6.f MT599 GCF/CCIT System – Start of Day Notification Administrative Message 
 Password  - Blank on MT 599 
GCFCTRRS Sender [[ID]] (GCF Trade Registration and Reconciliation System) 
599/000/GSCC Message Type 
88Z1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:20:2020050607587896 Transaction Message Reference Number  
:79:GSCC/GADM/PREP/20200506065520 
/GSOD/20200506 
GCF/CCIT Start of Day Notification Administrative Message with 
Preparation Date/Time stamp and Current Business Date included  
 
 
  

---

## Page 286

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 286 
C6.g MT599 GCF/CCIT System – End of Day Submission Cutoff Administrative Message 
 Password  - Blank on MT 599 
GCFCTRRS Sender [[ID]] (GCF Trade Registration and Reconciliation System) 
599/000/GSCC Message Type 
88Z1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:20:2020050607590897 Transaction Message Reference Number  
:79:GSCC/GADM/PREP/20200506150543 
/EDCS/20200506 
GCF/CCIT End of Day Submission Cutoff Administrative Message 
with Preparation Date/Time stamp and Current Business Date 
included  
 
 
C6.h MT599 GCF/C CIT System – Net Processing Administrative Message 
 Password  - Blank on MT 599 
GCFCTRRS Sender [[ID]] (GCF Trade Registration and Reconciliation System) 
599/000/GSCC Message Type 
88Z1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:20:2020050607590942 Transaction Message Reference Number  
:79:GSCC/GADM/PREP/20200506151112 
/SNET/20200506 
GCF/CCIT Net Processing Administrative Message with 
Preparation Date/Time stamp  and Current Business Date included 
 
 
C6.i MT599 GCF/CCIT System – End of Day Processing Completed Administra tive Message 
 Password  - Blank on MT 599 
GCFCTRRS Sender [[ID]] (GCF Trade Registration and Reconciliation System) 
599/000/GSCC Message Type 
88Z1 Receiver [[ID]] ( [[Member]] [[ID]]) 
:20:2020050607587836 Transaction Message Reference Number  
:79:GSCC/GADM/PREP/20200505160821 
/EODC/20200505 
GCF/CCIT End of Day Processing Completed Administrative 
Message with Preparation Date/Time stamp, Current Business 
Date, Next Day Trade Submission quali fier with the Next Business 
Date included  
 
 
  

---

## Page 287

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 287 
Appendix D – Message Structure Diagrams 
This appendix on Message Structure Diagrams contains diagrams for SWIFT reflecting the structure of the 
MT515, MT509 and MT518 messages used by [[FICC]] [[GSD]]. 
Message Structure Diagrams – MT515 
MT515
Confirmation Details
General Information
[[settlement]] Details
Linkages
Confirmation Parties
Financial Instrument  
Attributes
[[settlement]] Parties
Amounts
Two Leg Transaction 
Details 
(Repo Transaction Details)
Mandatory/Nonrepetitive – Includes references to this 
message and the function of this message (A)
Mandatory/Repetitive – A repeating sub -block 
which includes other reference for this 
message (A1)
Mandatory/Nonrepetitive – Includes details of trade 
being confirmed, i.e. [[settlement]] date, [[collateral]], pricing, 
etc. (C)
Mandatory/Repetitive – A repeating sub -block 
providing party identification ([[Buyer]], [[Seller]], 
etc.) (C1)
Optional/Nonrepetitive – Includes [[settlement]] details of 
the trade, type [[settlement]], etc. (D)
Optional/Nonrepetitive – If the message is confirming a 
Repo trade, the Repo Transaction details are provided 
here (F)
Optional/Repetitive – A repeating sub -block 
providing amount information ([[settlement]], 
cash, etc.) (D3)
Optional/Nonrepetitive – Includes additional 
information about the [[collateral]] for this trade 
(C2)
Optional/Repetitive – A repeating sub -block 
providing party identification (deliverer, 
sender, etc.) (D1)
  

---

## Page 288

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 288 
Message Structure Diagrams – MT509 
MT509
General Information
Linkages
Mandatory/Nonrepetitive – Includes references to this 
message and the function of this message (A)
Optional/Repetitive – A repeating sub -block 
which includes other reference for this 
message (A1)
Status
Reason
Mandatory/Repetitive – A repeating sub -block 
which provides the status of the reported 
trade (A2)
Optional/Repetitive – A repeating 
sub-block which includes the reason 
for this status (A2a)
  

---

## Page 289

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 289 
Message Structure Diagrams – MT518 
MT518
Confirmation Details
General Information
[[settlement]] Details
Linkages
Confirmation Parties
Financial Instrument  
Attributes
[[settlement]] Parties
Amounts
Two Leg Transaction 
Details 
(Repo Transaction Details)
Mandatory/Nonrepetitive – Includes references to this 
message and the function of this message (A)
Optional/Repetitive – A repeating sub -block 
which includes other reference for this 
message (A1)
Mandatory/Nonrepetitive – Includes details of trade 
being confirmed, i.e. [[settlement]] date, [[collateral]], pricing, 
etc. (B)
Mandatory/Repetitive – A repeating sub -block 
providing party identification ([[Buyer]], [[Seller]], 
etc.) (B1)
Optional/Nonrepetitive – Includes [[settlement]] details of 
the trade, type [[settlement]], etc. (C)
Optional/Nonrepetitive – If the message is confirming a 
Repo trade, the Repo Transaction details are provided 
here (E)
Optional/Repetitive – A repeating sub -block 
providing amount information ([[settlement]], 
cash, etc.) (C3)
Optional/Nonrepetitive – Includes additional 
information about the [[collateral]] for this trade 
(B2)
Optional/Repetitive – A repeating sub -block 
providing party identification (deliverer, 
sender, etc.) (C1)
 
 
 
 
 
 

---

## Page 290

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 290 
Appendix E – Reason Code Tables 
This appendix of Reason Code Tables contains reason codes for Rejects, DK’s and messages used in the 
MT515, MT509 and MT518 messages. 
Reject Message Reason Codes 
The following is a list of Reject Reason Codes that may appear on MT509 messages: 
Reject Error Code Qualifiers (to be used on MT509) in 
field :24B::REJT/ 
Error Conditions Which Can Cause an MT515 to be 
Rejected by G SD 
GSCC/E001  External Reference Error   
GSCC/E002  Previous External Reference Error  
GSCC/E003  Trade Not Eligible f or Cancellation  
GSCC/E004  Unknown Security  
GSCC/E005  Bad Quantity  
GSCC/E006  Bad Trade Date 
GSCC/E007  Bad [[settlement]] Date  
GSCC/E008  Bad Price 
GSCC/E009  Bad Amount  
GSCC/E010  Bad [[Buyer]] Party  
GSCC/E011  Bad [[Seller]] Party  
GSCC/E012  [[Broker]] Reference Number Error  
GSCC/E013  Transaction Type Error  
GSCC/E014  Price Method Error  
GSCC/E015  Commission Error  
GSCC/E016  Password Error 
GSCC/E017  [[Buyer]] Executing Firm Error  
GSCC/E018  [[Seller]] Executing Firm Error  
GSCC/E019  Start Amount Error  
GSCC/E020  Start Date Error  
GSCC/E021  End Amount Error  
GSCC/E022  End Date Error  
GSCC/E023  Repo Rate Error  
GSCC/E024  Secondary X -ref Error  
GSCC/E030  Trade Not in Same State  

---

## Page 291

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 291 
Reject Error Code Qualifiers (to be used on MT509) in 
field :24B::REJT/ 
Error Conditions Which Can Cause an MT515 to be 
Rejected by G SD 
GSCC/E998  Trade Not Found 
GSCC/E999  Other Bad Data 
GSCC/F001  Illegal Operation Attempted  
GSCC/F002  Internal Process Error 
GSCC/F999 Non -SWIFT Compliant Message  
  

---

## Page 292

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 292 
DK Message Reason Codes 
The following is a list of Reject Reason Codes that may be sent on MT515 messages and may appear on 
MT518 messages: 
DK Reason Codes (to be used on MT515 and MT518 in 
field :70E::TPRO//GSCC/DKRS) 
DK Reasons 
E004 Unknown Security  
E005  Bad Quantity  
E006 Bad Trade Date 
E007 Bad [[settlement]] Date 
E008 Bad Price 
E009 Bad Amount 
E010 Bad [[Buyer]] Party  
E011 Bad [[Seller]] Party  
E013 Transaction Type Error  
E014 Price Method Error  
E015 Commission Error  
E017 [[Buyer]] Executing Firm Error  
E018 [[Seller]] Executing Firm Error  
E019 Start Amount Error  
E020 Start Date Error  
E021 End Amount Error  
E022 End Date Error  
E023 Repo Rate Error 
E998 Trade not found 
E999 Other Bad Data 
 
  

---

## Page 293

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 293 
Other Message Reason Codes 
The following is a list of Other Message Reason Codes that may appear on MT518 messages: 
Message Reason Codes (to be used on MT518 in field 
:70E::TPRO//GSCC/MSGR) 
Message Reasons 
DKTD  Due to DK 
DCTD  Due to DK Remove  
MACH  Due to Match  
COAC  Due to Contra Action  
GSAC  Due to GSCC Action  
YRAC Due to your Action  
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 294

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 294 
Appendix F – Detailed Field Analysis Results – Comparison Messages 
This appendix on Detailed Field Analysis Results - Comparison Messages is intended to provide development 
personnel with the ‘tools’ to code for [[GSD]]’s current outbound messaging and for future releases without 
causing a disruption to [[Member]] service .  
[[GSD]] is, to the extent possible, committed to adhering to the guidelines presented in this document. As new 
services are offered by [[GSD]] which can be supported by Interactive Messaging, messages representing new 
events may be identified that [[DO]] not fit into the categories presented in this matrix. In this event, [[GSD]] will notify 
Members with sufficient advance notice for programming support. 
Assumptions 
• Analysis was performed in order to minimize [[Member]] programming for subsequent phases, and to help 
ensure that any changes implemented by [[GSD]] in the future can be done so using one production version 
of the application, without requiring ‘big bang’ changes by Members. 
• MT515 Inbound Messages and MT599 Administrative Messages are not included in the analysis. 
• Analysis was performed on all messages generated to date including changes made in support of the 
[[GSD]]’s Same-Day Settling Service. 
• No changes have been made to qualifiers for any messages already in production. 
• If new events are recognized, new messages may need to be processed by all Members. 
 
Approach 
Seven major categories of comparison-related events on system were identified: 
1. Record Accepted  
2. Record Rejected  
3. Record Processed  
4. Events sourced in the [[GSD]] system (not submitted by Members through a machine-to-machine interface) 
5. Advisories/Requests for Action  
6. Removal of Advisories  
7. Contra Modifies 
 
All record types were then sorted by the above categories, and then further sorted by whether they were 
related to the following instruction type: 
• Instruct 
• Modify 
• Cancel 
• DK 
 
Within each category we also identified whether the message 
• was already in production, 
• would be implemented in the next release of the Interactive Messaging software, or  
• was not yet identified (Future Messages).  

---

## Page 295

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 295 
Record Category Record MT Tag Code Words 
1. Record Accepted (Instruct sourced in [[Member]] or as applicable, vendor  system) 
1a) Instruct Accepted      
Version 1.0 Messages      
 Trade Accepted  509 25D IPRC/PACK 
Future Messages      
 ___Instruct Accepted  509 25D IPRC/GSCC/PA____ 
1b) Modify Accepted      
Version 1.0 Messages      
 Modify Accepted  509 25D IPRC/GSCC/MODA 
Future Messages      
 ___Modify Accepted  509 25D  
1c) Cancel Accepted      
Version 1.0 Messages      
 Cancel Accepted  509 25D CPRC/PACK 
Future Messages      
 ___Cancel Accepted  509 25D CPRC/GSCC/PA___ 
1d) DK Accepted      
Version 1.0 Messages  NA    
Future Messages      
 ___DK Accepted  509 25D IPRC/GSCC/PADK 
 
  

---

## Page 296

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 296 
Record Category Record MT Tag Code Words 
2. Record Rejected (Instruct sourced in [[Member]] or as applicable, vendor system)  
2a) Instruct Rejected      
Version 1.0 Messages      
 Trade Rejected  509 25D IPRC/REJT 
   24B REJT/GSCC/XXXX 
 Trade Rejected  (due to…)  509 25D IPRC/GSCC/PA____ 
   24B REJT/GSCC/XXXX 
   70D REAS//GSCC/____ 
2b) Modify Rejected      
 Modify Rejected  509 25D IPRC/REJT 
   24B REJT/GSCC/XXXX 
   70D REAS//GSCC/MDRJ 
 Modify Rejected(due to…)  509 25D IPRC/REJT 
   24B REJT/GSCC/XXXX 
   70D REAS//GSCC/____ 
2c) Cancel Rejected      
 Cancel Rejected  509 25D CPRC/REJT 
   24B REJT/GSCC/XXXX 
 Cancel Rejected(due to…)  509 25D CPRC/REJT 
   24B REJT/GSCC/XXXX 
   70D REAS//GSCC/____ 
2d) DK Rejected      
 DK Rejected  (due to…)  509 25D IPRC/REJT 
   24B REJT/GSCC/XXXX 
   70D REAS//GSCC/____ 
 e.g. DK Rejected (due to…)  509 25D IPRC/REJT 
   24B REJT/GSCC/E030 
   70D REAS//GSCC/DKRJ 
 
  

---

## Page 297

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 297 
Record Category Record MT Tag Code Words 
3. Record Processed ((Instruct sourced in [[Member]] or as applicable, vendor system)  
3a) Instruct Processed      
 Trade Compared  509 25D MTCH//MACH 
 Trade Compared via Par 
Summarization  
509 25D MTCH/GSCC/PSUM 
3b) Modify Processed      
 Trade Modified/ Modify Processed  509 25D IPRC/GSCC/MACH 
 Repo Substitution Processed  509 25D IPRC/GSCC/RPSP 
3c) Cancel Processed (of your 
trade) 
    
 Trade Canceled/Cancel Processed 509 25D CPRC//CAND 
 Uncompared Deleted Transaction 509 25D IPRC/GSCC/DELE 
 Trade Canceled due to DK  509 25D IPRC/GSCC/DEDK 
3d) DK Processed (your DK of 
trade submitted against you)  
    
 DK Processed (due to…)  509 25D IPRC/GSCC/DP__ 
3e) The Cancel Remove 
submitted by the party who 
originated the cancel,  has been 
Processed  
    
 Cancel Lifted (due to…)  509 23G CAST 
   25D CPRC/GSCC/UP__ 
 
 
  

---

## Page 298

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 298 
Record Category Record MT Tag Code Words 
4. Messages for events ‘ sourced’ in [[GSD]] system) 
4a) A Trade Instruct has been 
created for you on the [[GSD]] 
system 
    
 Screen Input Trade Replay - Instruct 518 23G NEWM 
   22F PROC/GSCC/SITR 
 Locked in Trade Advice (Locked in 
Trade) 
518 23G NEWM 
   22F TRTR/GSCC/TRLK or 
TRLR 
   22F PROC/GSCC/LCTA 
Future Messages      
 A trade was booked for you in the 
[[GSD]] system (due to…)  
518 23G NEWM 
   22F PROC/GSCC/TADD 
   70E TPRO//GSCC/MSGRXXXX 
4b) Your Trade has been 
Modified in the [[GSD]] system  
    
 Screen Input Trade Replay - Modify  518 23G NEWM 
   22F PROC/GSCC/SITR 
 [[default]] values applied  518 23G NEWM 
   22F PROC/GSCC/DFVA 
 Coupon Reset (of UST FRNs)  518 23G NEWM 
   22F PROC/GSCC/CPNR 
 Repo substitution details  518 23G NEWM 
   22F PROC/GSCC/RPSD 
 Compared with Modifications  518 23G NEWM 
   22F PROC/GSCC/CMPM 
 Post Comparison Trade Modification 
(modified by part or contra -party ) 
518 23G NEWM 
   22F PROC/GSCC/MDAD 
 Yield to Price - Assumed 518 23G NEWM 
   22F PROC/GSCC/YTPA 
 Yield to Price - Real 518 23G NEWM 

---

## Page 299

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 299 
Record Category Record MT Tag Code Words 
   22F PROC/GSCC/YTPR 
Future Messages      
 Your trade has been modified in the 
[[GSD]] system due to….  
518 23G NEWM 
   22F PROC/GSCC/TMOD 
   70E TPRO//GSCC/MSGRXXXX 
4c) A Cancel has been Applied 
to your Trade in the GSCC 
system 
    
 Screen Input Trade Replay - Cancel  518 23G CANC 
   22F PROC/GSCC/SITR 
 Post Comparison Cancel Advice 
(trade unilaterally canceled by locked-
in submitter) 
518 23G CANC 
   22F PROC/GSCC/PCCA 
Future Messages      
 A cancel has been applied to your 
trade in the [[GSD]] system (due to…)  
518 23G CANC 
   22F PROC/GSCC/TCAN 
   70E TPRO//GSCC/MSGRXXXX 
4d) A DK was Applied to your 
record  
N/A (See 4d)     
  

---

## Page 300

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 300 
Record Category Record MT Tag Code Words 
5. Advisories- Request for Action  
5a) Request for Comparison      
 Comparison Request  518 23G NEWM 
   22F PROC/GSCC/CMPR 
 Comparison Request (due to ...)  518 23G NEWM 
   22F PROC/GSCC/CMPR 
   70E TPRO//GSCC/MSGRXXXX 
5b) Modification of Comparison 
Requests  
    
 Comparison Request Modify  518 23G NEWM 
   22F PROC/GSCC/CRQM 
 Comparison Request Modify (due 
to…) 
518 23G NEWM 
   22F PROC/GSCC/CRQM 
   70E TPRO//GSCC/MSGRXXXX 
5c) Cancel Requests      
 Cancel Request (Post Comparison)  518 23G CANC 
   22F PROC/GSCC/CREQ 
 Cancel Request (due to…)  518 23G CANC 
   22F PROC/GSCC/CREQ 
   70E TPRO//GSCC/MSGRXXXX 
5d) Your Trade has been DK’d - 
please Modify/Cancel  
    
 DK Advice (Your trade has been DK’d 
due to…)  
518 23G NEWM 
   22F PROC/GSCC/NAFI 
   70E TPRO//GSCC/DKRSXXXX 
 
 
  

---

## Page 301

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 301 
Record Category Record MT Tag Code Words 
6. Removal of Advisories 
6a) Advisory (Comparison 
Request) Removed  
    
 Comparison Request Cancel  518 23G CANC 
   22F PROC/GSCC/CADV 
 Comparison Request Cancel (due to 
…) 
518 23G CANC 
   22F PROC/GSCC/CADV 
   70E TPRO//GSCC/MSGRXXX 
  or 70E TPRO//GSCC/DKRSXXXX/ 
MSGRXXX 
6b) Modify Re moved  N/A    
6c) The Cancel Request 
Submitted against you has been 
Removed  
    
 Cancel Request Cancel (due to…)  518 23G CANC 
   22F PROC/GSCC/CCRQ 
   70E TPRO//GSCC/MSGRXXX 
6d) The DK on your Trade has 
been Removed  
    
 The DK on your trade has been 
removed (due to…)  
518 23G CANC 
   22F PROC/GSCC/DCCX 
   70E TPRO//GSCC/MSGRXXX 
 
 
 
 
 
  

---

## Page 302

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input & Output  
Appendices 302 
Record Category Record MT Tag Code Words 
7. Contra Modifies  
7a) Contra Trade has been 
Modified Post Comparison  
    
 Post Comparison Contra Trade 
Modification  
518 23G NEWM 
   22F PROC/GSCC/CMDA 
 Post Comparison Contra Trade 
Modification (due to…)  
518 23G NEWM 
   22F PROC/GSCC/CMDA 
   70E TRPO/GSCC/MSGRXXXX 
  e.g. 70E TPRO//GSCC/MSGRCOAC 
 
 

---

## Page 303

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 