---
title: "MBSD Pair-Off MRO Specifications"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs175_po_mro_specs_json.pdf"
pages: 15
size: "356.4 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD Pair-Off MRO Specifications

**Original File:** [mbs175_po_mro_specs_json.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs175_po_mro_specs_json.pdf)  
**Category:** MBSD  
**Total Pages:** 15  
**File Size:** 356.4 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
MBSD PAIR-OFF MRO SPECIFICATIONS  
 
VERSION 1.0 
JUNE 1, 2023 
 
 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, 
and the Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing 
Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository 
Trust & Clearing Corporation (“[[DTC]] C”). [[DTCC]] itself does not provide such services.  Each of these affiliates is a 
separate legal entity, subject to the laws and regulations of the particular country or countries in which such entity 
operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: June 1, 2023 
Publication Code:  MBS175 
Service: Fixed Income Clearing Corporation 
Title: MBSD Pair-Off MRO Specifications  
 

---

## Page 3

MBSD PAIR-OFF MRO Specifications 
 
 
TABLE OF CONTENTS 
 
Table of Contents...................................................................................................................... i 
Introduction to the Documentation .............................................................................................1  
Pair-Off MRO Specif ication........................................................................................................1  
Aud ienc e ................................................................................................................................1  
Distribution ............................................................................................................................1  
Related Materials .....................................................................................................................1  
JSON....................................................................................................................................1  
[[FICC]].....................................................................................................................................1  
Version C on tr ol In for ma tion .......................................................................................................1  
1. JSON Messaging Guidelines ..................................................................................................2  
Overview ................................................................................................................................2  
Mess ag e Structure ...................................................................................................................2  
Mess ag e Head er ....................................................................................................................2  
Blocks and Sub-blocks ............................................................................................................2  
Fields....................................................................................................................................4  
2. Communications ...................................................................................................................5  
3. Detail Message Specifications ................................................................................................6  
Mess ag e Fo rmat Guidelines ......................................................................................................6  
Fo rmatting Rules ....................................................................................................................6  
Formatting Conventions...........................................................................................................7  
Pair-Off Status MRO ................................................................................................................8  
Pair-Off Activity MRO ...............................................................................................................9  
 
 

---

## Page 4

MBSD PAIR-OFF MRO Specifications  
 
Introduction to the Documentation 1 
INTRODUCTION TO THE DOCUMENTATION 
Pair-Off MRO Specification 
This document provides an overview of Pair-Off MRO specifications (output) that will be used to support 
MBS Pair-Off Service 
Audience 
This document was written for systems and development personnel, including managers, analysts, and 
programmers. It presumes readers are familiar with technical concepts and terms, understand JSON 
Messaging specifications, and have a [[BASIC]] understanding of the products and services of the Mortgage-
Backed [[securities]] Division (MBSD) of the Fixed Income Clearing Corporation ([[FICC]]). 
Distribution 
MBSD EPN Members 
Related Materials 
JSON 
The specifications are based o n JSON messages. Readers are therefore strongly urged to refer to JSON 
user documentation to obtain a complete and comprehensive understanding of these message 
standards. JSON information (including many applicable message formats) can also be found at 
http://www.json.org/. 
[[FICC]] 
For additional information regarding RTTM®, readers can refer to documentation found on 
[[DTCC]] learning.com for MBSD. 
Version Control Information 
Date Version Number Name Description of Changes  
08/11/2022 1.0 E. Badalov  Initial draft 
6/1/2023 n/a [[DTCC]] Learning  Formatting updates  
 

---

## Page 5

 
1.  JSON Messaging Guidelines 2 
1. JSON MESSAGING GUIDELINES 
This section of the document provides some background information that may be useful for interpreting 
the detailed message specifications that follow. 
Overview 
[[FICC]] has adopted the JSON message formats for machine readable output associated with MBS Pair-Off 
Services. [[FICC]] uses a proprietary network for communication between MBS and its Members. 
Message Structure 
JSON is a text format that is completely language-independent but uses conventions that are familiar to 
virtually all modern programming languages. These properties make JSON an ideal data-interchange 
language. 
JSON message formats are constructed using a modular methodology based on the premise that 
information can be identified and programmed once, then reused wherever needed. Using this approach, 
data is configured into logical groups (i.e., TAG-identified fields and blocks) according to business 
purpose.  
Message Header 
The Message Header contains the message identifier and is populated as a continuous string of data. 
Blocks and Sub-blocks 
A block may be defined as a group of fields containing related business information that is framed by 
start-of-block and end-of-block designators. The use of a block is not restricted to any given message; it 
can be reused across a number of messages and combined with other blocks to fulfill a variety of 
business requirements.  
Each message generated by [[FICC]] contains one main block and several sub-blocks for each business 
line. These blocks may be mandatory or optional within a particular message, and are structured as 
follows: 
• A start-of-block designator (represented by the tag “ { ”), indicating the start of a group of related 
information. 
• An end-of-block designator (represented by the tag “ } ”), indicating the end of a group of related 
information. 
 
An information block may be further divided into sub-blocks containing groups of fields that further define 

---

## Page 6

 
1.  JSON Messaging Guidelines 3 
the block. The structure of a sub-block is the same as that of a block, the difference being that it is 
“nested” or contained within the block. For example, each business line will contain the tag and the value 
of that tag would be sub-blocks of that business Details block. Sub-blocks, under certain circumstances, 
can be repeated in a block. 
  

---

## Page 7

 
1.  JSON Messaging Guidelines 4 
Fields 
At a minimum, each field is composed of an identifying tag and its associated field data with colon as a 
delimiter. A tag contains a start and end double-quote and will end with a colon (“ : ”). The field data also 
contains a start and end double-quote as a string value unless it is a start of sub-block as in the case of 
business line. The format for field data is a string of alphanumeric characters. Each field is separated from 
the next field by a separator character comma (“ , ”). 

---

## Page 8

 
2.  Communications 5 
2. COMMUNICATIONS 
Members receive files containing JSON-formatted records from [[DTCC]] via [[DTCC]]’s Common Data 
Transfer System (CDTS).  
Product IDs for each file: 
Filename Production UAT 
Pair-Off Activity  MRO 13157401 13987401 
Pair-Off Status MRO 13157400 13987400 
 

---

## Page 9

 
3.  Detail Message Specifications 6 
3. DETAIL MESSAGE SPECIFICATIONS 
This section contains the detailed specifications for the Pair-Off Activity and Status Machine Readable 
Output (MRO). 
Message Format Guidelines 
Formatting Rules 
The following Message and Message Field rules apply to all messages in the Pair-Off (PO) Message 
Specif ications: 
Message Rules 
1. Direction: Messages are sent from [[FICC]]. 
 
2. Variable Length: All messages can vary in length up to a maximum allowable number of characters 
per message type. 
 
3. Header: All messages begin with a standard fixed-length header that will identify the start of the 
message, business date, and deposit account. 
 
4. Trailer: All messages end with a standard fixed-length trailer that identifies the end of the message. 
 
5. Message Fields: A message is composed of one or more message fields. 
 
6. Character Set: A-Z, a-z, 0-9, white space and the following punctuation " : / { } [ ] - " 
 
7. Field Delimiter: The field delimiter sequence is Carriage Return Line Feed, “CRLF” (ASCII 
Character 13, ASCII Character 10). This sequence immediately follows the data. 
Message Field Rules 
1. Field Tag: Each field begins with a field tag. 
 
2. Tag Delimiter: Each tag is prefixed and suffixed by the double-quote “ “ ” and ends with a colon “:” 
(e.g., “dep_acct”:). 
 
3. Field Data: Field data immediately follows the tag suffix delimiter. 
 
4. Data Format: Data conforms to format rules.    

---

## Page 10

 
3.  Detail Message Specifications 7 
Formatting Conventions 
Please note that all layouts for the JSON messages (included in this Section of the document) are 
organized using the following columns of data: 
Column Heading  Description 
M/O/R The M/O/R column  defines  whether the field is always M- Mandatory, or is R – 
Mandatory if block is present , or if the field is O- Optional block.  
Tag The Tag column  defines  the exact tag value that must precede the field. Tags are 
always delimited by “:” (meaning  a “:” would be the character immediately  before and  
after the tag). 
Field Description The Field Description column  provides a text description of the purpose or use of a 
data field. 
Data Format  The Data Format column  specifies the size and characters allowe d within a data field.  
 
The following characters may appear in the Data Format Column or in any discussion of data format and 
content: 
Character Meaning Example 
 
Example Usage 
a Upper Case Alpha Characters  6a ABCDEF 
c Alphanumeric Characters (upper case 
only)  
6c AB12EF 
d Decimal Number (decimal period)  15d 2035.45 
e Space 1e (1blank space)  
n Numeric Characters  8n 19950131 
x Any Printable ASCII Symbol  20x Anytime & Anyplace  
/ The literal “/” as a separator  6a/2a AB12EF/NY 
[ ] Optional element format  [/4c] [optional data]  
[-] Optional “sign” (negative) format  [-] : “total_funds”:” -5.45” 
! Fixed length field  12!c ABCDEFGHIJKL 
 
All fields are, by definition, variable in length with a maximum field size specified, unless a fixed length 
f ormat is defined by inclusion of the “!”, in which case the size specified is the fixed field size. In the case 
where the data value in the fixed length field is smaller than the field size specified, the data should be 
left-justified with trailing blanks. 
  

---

## Page 11

 
3.  Detail Message Specifications 8 
Pair-Off Status MRO 
This section includes the detailed specification for the Pair-Off Status MRO record 
 
M/O/R Tag Field Description Data Format  
Message Header 
M PO_Status_Header_ Header will include date and de stination 
account  
YYYYMMDD_4!c 
O  { Block Start  
R  “[[participant]] _id”: MBS EPN [[participant]]  [[ID]] “3!c”, 
R  “aggregate_id ”: MBS EPN Aggregate  [[ID]] “2!c”, 
R  “account_id ”: MBS EPN Account  [[ID]] “4!c”[,] 
O “pairoff_records ”: Individual  Pair-Off request status as 
repeating block  
 
R  [ Repeat Block Start  
R  { Block Start  
R “orig_sbmsn_ ts”: Original Submission Timestamp  “YYYYMMDDHHMMSS”, 
R “stl_dt”: [[settlement]] Date  “YYYYMMDD”, 
R “tba_cusip ”: TBA [[CUSIP]] “9!c”, 
R  “submitter_id ”: Submitter Account  [[ID]] of the [[pair off]] 
request 
“4!c”, 
R  “contra_id ”: Contra Account  [[ID]] of the [[pair off]] 
request 
“4!c”, 
O  “sub_contra_id ”: SubContra  Account  [[ID]] of the [[pair off]] 
request 
“4!c”, 
R  “pairoff _id”: [[pair off]] [[ID]] assigned “15!c”, 
R  “pairoff _status”: [[pair off]] status  
PEND - pending,  
AFFM - affirmed,  
DKED - DKed,  
CANC – canceled, 
MKDL – marked for delet ion : pending 
items that are marked for delet ion  on the 
last day of the month 
“4!c”, 

---

## Page 12

 
3.  Detail Message Specifications 9 
M/O/R Tag Field Description Data Format  
CLSD – closed : affirmed items that are 
marked as closed on  the last day of the 
month 
R “pairoff_payment ”: [[pair off]] payment   “[-]15d”, 
R “trade_details ”: Trade Details corresponding to Pair -Off 
request as repeating block  
 
R  [ Repeat Block Start  
R  { Block Start  
R “trade_xref”: Trade Xref provided by original PO 
submission  
“16c”, 
R “buy_sell ”: Buy/Sell Indicator  “1!c”, 
R “trade_dt”:  Trade Date  “YYYYMMDD”, 
R “trade_price”:  Trade Price  “12d”, 
R “orig_trade_par ”: Original Trade Par   “13n”, 
R “pairoff _par”: [[pair off]] Par  “13n”, 
R } Block End   [,] 
R ] Repeat Block End   
R } Block End   [,] 
R ] Repeat Block End   
O } Block End    
Message Trailer 
M PO_Status_Trailer_ Trailer will include date and destination 
account  
 YYYYMMDD_4!c 
Pair-Off Activity MRO 
This section includes the detailed specification for the Pair-Off Activity MRO record 
 
M/O/R Tag Field Description Data Format  
Message Header 
M PO_Activity _Header_ Header will include date and destination 
accoun t 
YYYYMMDD_4!c 
O  { Block Start  

---

## Page 13

 
3.  Detail Message Specifications 10 
M/O/R Tag Field Description Data Format  
R “participant_id ”: MBS EPN [[participant]]  [[ID]] “3!c”, 
R “aggregate_id ”: MBS EPN Aggregate  [[ID]] “2!c”, 
R “account_id ”: MBS EPN Account  [[ID]] “4!c”[,] 
O “message_details ”: Individual Pair -Off request message 
details  as repeating block  
 
R  [ Repeat Block Start  
R  { Block Start  
R “msg_id ”: EPN message [[ID]] assigned for current 
event 
“15!c”, 
R “stl_dt”: [[settlement]] Date  “YYYYMMDD”, 
R “tba_cusip ”: TBA [[CUSIP]] “9!c”, 
R “submitter_id ”: Submitter Account  [[ID]] of the message “4!c”, 
R “contra_id ”: Contra Account  [[ID]] of the message “4!c”, 
O “sub_contra_id ”: SubContra Account  [[ID]] of the message “4!c”, 
R “pairoff _id”: [[pair off]] [[ID]] assigned  “15!c”, 
R “msg_process_time ”: Processing Timestamp  “YYYYMMDDHHMMSS”, 
R “msg_xref ”: Message External Reference provided 
by submitter 
“16c”, 
R “pairoff _action”:  Pair-Off action   
PO – Original Pair-Off request,  
PD – DK of PO,  
PF – Af firm of PO,  
PC – Cancel of PO. 
“2!c”, 
R “pairoff _payment”:  [[pair off]] payment  “[-]15d”, 
O “dk_reason ”: DK Reason code, available only on DK 
of Pair-Off (PD) activities  
“4!c”, 
O “trade_details ”: Trade Details corresponding to Pair -Off 
request as repeating block  – Only 
available on original PO actions  
 
R  [ Repeat Block Start  
R  { Block Start  
R “trade_xref”: Trade Xref provided by original PO 
submission  
“16c”, 
R “buy_sell ”: Buy/Sell indicator  “1!c”, 

---

## Page 14

 
3.  Detail Message Specifications 11 
M/O/R Tag Field Description Data Format  
R “trade_dt”:  Trade Date  “YYYYMMDD”, 
R “trade_price”:  Trade Price  “12d”, 
R “orig_trade_par ”: Original Trade Par   “13n”, 
R “pairoff _par”: [[pair off]] Par  “13n”, 
R } Block End   [,] 
R ] Repeat Block End   
R } Block End   [,] 
R ] Repeat Block End   
O } Block End    
Message Trailer 
M PO_Activity_Trailer_ Trailer will include date and destination 
account  
 YYYYMMDD_4!c 
 
  

---

## Page 15

 
3.  Detail Message Specifications 12 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 