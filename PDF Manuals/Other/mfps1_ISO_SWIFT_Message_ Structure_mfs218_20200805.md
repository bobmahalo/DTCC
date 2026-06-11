---
title: "mfps1_ISO_SWIFT_Message_ Structure_mfs218_20200805.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps1_ISO_SWIFT_Message_%20Structure_mfs218_20200805.pdf"
pages: 21
size: "398.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# mfps1_ISO_SWIFT_Message_ Structure_mfs218_20200805.pdf

**Original File:** [mfps1_ISO_SWIFT_Message_ Structure_mfs218_20200805.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps1_ISO_SWIFT_Message_%20Structure_mfs218_20200805.pdf)  
**Category:** Other  
**Total Pages:** 21  
**File Size:** 398.4 KB  

---

## Page 1

 
 
 
MUTUAL FUND PROFILE SERVICE 
PRICE AND RATE 
ISO / S.W.I.F.T. MESSAGE STRUCTURE REFERENCE GUIDE  
 


---

## Page 2

 
 
© 2020 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: August 5, 2020 
Publication Code: MFS218 
Service: Mutual Fund Profile Service 
Title: ISO/S.W.I.F.T Message Structure Guide 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 3

 
 
 
 
 
CHANGE HISTORY 
August 5, 2020 Document rebranded 

---

## Page 4

 
 
TABLE OF CONTENTS 
ISO/SWIFT ............................................................................................................................................................. 5 
What is ISO and SWIFT? .................................................................................................................................. 5 
What is a ISO / S.W.I.F.T. message? ............................................................................................................... 6 
ISO/SWIFT Message Structure ............................................................................................................................ 7 
A.  How is an ISO / S.W.I.F.T. message formatted? ..................................................................................... 7 
B.  S.W.I.F.T. Character Set .......................................................................................................................... 7 
C:  Message Presentation .............................................................................................................................. 9 
D:  General Rules ........................................................................................................................................... 9 
E:  [[BASIC]] Header Blocks ...............................................................................................................................10 
F:  Application Header Block ........................................................................................................................11 
G:  User Header Block .................................................................................................................................12 
H:  Text Block ...............................................................................................................................................13 
I:  Trailer Block .............................................................................................................................................14 
J:  Example of complete input message for MFPS: .....................................................................................15 
K:  Message Validation ................................................................................................................................15 
Technical Information ........................................................................................................................................ 16 
A Field Separators .........................................................................................................................................16 
B Input/Output Requirements ........................................................................................................................17 
 

---

## Page 5

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT 5 
ISO/SWIFT 
This document was created to provide a [[BASIC]] overview of how to build an ISO / S.W.I.F.T. standard message 
for the Mutual Fund Profile Service (MFPS) application. 
What is ISO and SWIFT? 
Based in Geneva, Switzerland, the ISO (International Organization for Standardization) is a worldwide 
federation of national standards bodies. The organization’s objective is to promote the development of 
international or worldwide standards in all important fields of business. These standards are developed by 
technical committees composed of experts in each field who are nominated by the respective branches of 
industry. Any [[Member]] organization that wishes to participate in a technical committee may [[DO]] so.  
Once standards have been developed, 75 percent of the ISO body must approve the standards prior to 
acceptance and promulgation. The ISO restricts itself to ensuring orderly processing and publishing of the 
standards. That is, it protects against a premature promulgation of standards by considering the interests of all 
parties concerned. 
Underlying the ISO’s work is a philosophy which includes conserving all existing national systems to the 
maximum extent possible. This philosophy allows marketplaces, such as [[Mutual Funds]], to retain good routines 
and valuable experience, and it facilitates the introduction and implementation of new systems which use 
exiting formats and procedures. 
A standard scheme for message types (roughly equivalent to Fund/SERV and NETWORKING record types) 
has been developed by an ISO working group. Each type message is represented by a three- digit code 
indicating category, group and type. For example, the category for all [[securities]] transactions is “5".  
Within the United States the organization that administers the development of ISO message formats is The 
Society for Worldwide Interbank Financial Telecommunications, S.W.I.F.T.  In order to ensure compatibility of 
the multitude of practices, conventions and habits of S.W.I.F.T. users, all messages transmitted via the 
S.W.I.F.T. network must adhere to these message text standards. 
 
  

---

## Page 6

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT 6 
What is a ISO / S.W.I.F.T. message? 
The international standard describes the content and format of message types for use by professionals engaged in 
the [[securities]] business. The standard applies to the core of a message which is independent from the communication 
method. For the purpose of these standards the following definitions apply. 
Term  Definition 
Message A message is a communication containing one or more transactions or related 
information. 
Message Type (MT) A message type is a specific classification for messages which have a defined 
function(s) or content. 
Message Type 
Code 
A message type code is a code that designates the function on and/or the action 
requested by the message. It is always a three-digit code. 
Field A field is the smallest element, identified by a field tag or a name in the message text.  
Field Tag A field tag is a unique string of characters used in formatted messages which 
identifies the meaning of the associated data field. 
Subfield A subfield is a predetermined division of a field. 
Format A format describes the structure and the limitation(s) in the use of the data in the field 
for telecommunication processing. 
 
  

---

## Page 7

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT Message Structure 7 
ISO/SWIFT MESSAGE STRUCTURE 
A.  How is an ISO / S.W.I.F.T. message formatted? 
All S.W.I.F.T. messages conform to a defined block structure. Each block of a message contains data of a 
particular type and is used for a particular purpose. 
Each block of a message begins and ends with a curly bracket (or brace) character ‘{’ and ‘}’ respectively. All 
main blocks are numbered, and the block number followed by a colon (:) are always the first characters within 
any block. 
A typical S.W.I.F.T. user-to-user message may consist of: 
{1:[[BASIC]] Header Block} 
{2:Application Header Block} 
{3:User Header Block} 
{4:Text Block} 
{5:Trailer Block} 
 
Blocks 1, 2 and 3 relate to header information; block 4, the text of the message; and block 5, trailer information.  
Note:  Mutual Fund Profile Service will use block 1, 2, 4, and 5. 
 
B.  S.W.I.F.T. Character Set 
Only characters belonging to the S.W.I.F.T. character set, shown below, will be accepted by Mutual Fund 
Profile Service for input and output transmission: 
a b c d e f g h i j k l m n o p q r s t u v w x y z 
A B C D E F G H I J K L M N O P Q R S T U V 
W X Y Z 0 1 2 3 4 5 6 7 8 9 
/ - ? : ( ) . , ' + { } 
Cr Lf Space 
 
 
(In EBCDIC format, Cr is HEX'0D', Lf is HEX'25'. 
In ASCII format, Cr is HEX'0D', Lf is HEX'0A'.) 
 
 
 
 
 
 

---

## Page 8

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT Message Structure 8 
The specifications on field or subfield content may consist of restrictions on the length or subfield content according to the 
following legend: 
Restrictions on Characters 
n Digits only   ex:  2n=up to 2 digits 
(Right justified) 
a Letters only   ex:  3a=always three letters 
(Left justified, blank filled where applicable) 
a Letters and digits only 
(Left justified, blank filled where applicable) 
x Any character accepted by SWIFT 
(Left justified, blank filled where applicable) 
b Blank space 
number A number field with decimal represented by a comma “,” 
The fractional part may be missing, but the decimal comma must always be present. (Right 
justified) 
Example of valid numbers:        0, 
0,67 
10000, 
123,99 
Example of invalid numbers:      0 
.67 
,67 
123.99 
YYYYMMDD Date format with     YYYY = Year 
                                MM=Month 
        DD=Day 
(Zero filled on left for each subfield. e.g.: 20200108) 
 
Restrictions on Length 
N Maximum length of N 
ex:  8n = a number with up to 8 digits 
N-N Minimum and maximum length  
ex:  10-20 = minimum length of 10 and maximum of 20 
N Fixed length 
ex: 8a = a 8-byte alphabetic field, with no blank(s) 
      3n = a 3-digit field, zero filled on the left where applicable.  


---

## Page 9

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT Message Structure 9 
N*N Maximum number of lines times maximum line length  
ex: 4*35x = Up to 4 lines of up to 35 characters each 
C:  Message Presentation 
Each main block is sub-divided into a number of fields and each field contains particular information (e.g. date, 
time, price or a tag number followed by the appropriate variable content). 
All fields within header blocks 1 and 2 are of fixed length and are continuous. No field separators are used. 
In the case of the text of a user-to-user message, all message text within the Text Block (block 4) begins with a 
Carriage Return and Line Feed (CrLf) and ends with CrLf followed by a hyphen (-). Each field within the text 
begins with a tag number followed by a colon, followed by the appropriate variable content. (See Section III 
Technical Information) 
Fields within the text block of a system message or system command are seen as sub-blocks of block 4 and 
are delimited by further pairs of curly brackets. Each sub-block begins with a three digit tag number followed by 
a colon. 
D:  General Rules 
• A curly bracket ({, }) within any field is prohibited. (It is only used as a field delimiter)  
• Brackets ([]) around a subfield indicates that the latter is optional. 
• The date format is YYYYMMDD. 
• The ISO country and currency codes are used. 
• The fields of each message type must be in the sequence specified in the format specification 
of the message type. 
• All specified subfields must be present in the sequence specified. 
• When a field format is shown on 2 or more lines, the information must be formatted with CrLf 
character separating each line. 
• A field not specified in the format specification of a particular message type must never 
appear. 
• A field must appear only once in a message, unless it is in the repeatable sequence where 
repetition is allowed. 
• The alphabetic characters in all headers must be in upper case only. 
• Only characters belonging to SWIFT character set can be used. 
 
In summary the structural features are: 
 
• The major blocks are numbered from 1 to 5; the block number is followed by a ":".  
• Each block starts with a "{" character and ends with a "}". Blocks are NOT separated by CrLf  
(carriage return and line feed) characters. 
• Each main block is sub-divided into a number of fields. 
• Each field contains a particular piece of information. All fields in blocks 1 and 2 are fixed in 
length, with no field separators. 

---

## Page 10

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT Message Structure 10 
• The message text in block 4 begins with Carriage Return and Line Feed (CrLf) and ends with 
CrLf followed by a hyphen, "-". 
• For MFPS, “input” is from [[participant]] to [[NSCC]], and “output” is from [[NSCC]] to participants.  
E:  [[BASIC]] Header Blocks 
• It is mandatory. 
• It appears in all S.W.I.F.T. messages: User-to-user, system and acknowledgment. 
• The format is the same for both the input (relative to S.W.I.F.T. network) and output message.  
• It contains eight fields as shown (with no field separator between any two consecutive fields):      
 
1 22 3 44 555555555555 6666 777777 8 
Field No. Field Name Length (bytes) Values  
1 [[BASIC]] Block Header 
initiation identifier 
1 {  
2 Block Identifier 2X 1:  
3 SWIFT Application [[ID]] 1a F  
4 Application Protocol Data Unit 
(APDU) 
2n 01  
5 SWIFT Address or BIC 
(Bank [[ID]] Code) 
12x Bytes 1- 4 
 
 
 
 
 
 
 
Bytes 5- 7 
  Bytes 8-12 
Input to MFPS = Sender clearing 
number 
MFPS Output /Batch participants 
price and rate info = [[NSCC]] 
MFPS Output /Batch participants 
rejected message = recipient 
clearing number MFPS Output / 
Interactive participants = recipient 
clearing number (all messages) 
MFP 
XXXXX 
6 Transmission Session 
Number 
4n 0000  
7 Sequence Number 6n 000000  
8 [[BASIC]] Block Header 
Termination identifier 
1x }  
 Total Block Length 29   
 
[[BASIC]] Header Block Example: {1:F015501MFPXXXXX0000000000} 
  

---

## Page 11

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT Message Structure 11 
F:  Application Header Block 
• It is mandatory for MFPS user-to-user message. 
• Its structure depends on whether the message is an input (relative to S.W.I.F.T. network) or 
output. 
 
F1:  Application Block Input Format - Input From [[participant]] to [[NSCC]] 
Input format: 1 22 3 444 55555555555 6 7 888 9 (with no field separators) 
Field No. Field Name Length (bytes) Values  
1 Application Block Header 
Input Initiation Identifier 
1 {  
2 Block Identifier 2X 2:  
3 Input Identifier 1a I  
4 Message Type Number 3n nnn  
5 Recipient’s SWIFT Address 
or BIC (Bank [[ID]] Code) 
12x Bytes 1-4 
Bytes 5-7 
Bytes 8-12 
[[NSCC]] 
MFP 
XXXXX 
6 Message Priority Indicator 1a N  
7 Delivery Monitoring 
Indicator 
1n 2  
8 Obsolescence Period 3n 002  
9 Application Block Input 
Header Termination 
Identifier 
1x }  
 Total Block Length (bytes) 25   
 
Application Header Block - Input Example: {2:I55YNSCCMFPXXXXXN2002} 
  

---

## Page 12

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT Message Structure 12 
F2:  Application Block Output Format - Output From [[NSCC]] to [[participant]] 
Output (relative to S.W.I.F.T. network) format: 
122 3 444 5555 6666666666666666666666666666 77777777 8 9 
Field No. Field Name Length 
(bytes) 
Values  
1 Application Block Header 
Output Initiation Identifier 
1 {  
2 Block Identifier 2X 2:  
3 Output Identifier 1a O  
4 Message Type Number 3n nnn  
5 Sender Input Time 4 Time (hhmm)  
6 Message Input 
Reference 
30x Bytes 1-8 
Bytes 9-12 
Bytes 13-15 
Bytes 16-20 
Bytes 21-30 
Date of output message (YYYYMMDD) 
[[NSCC]] 
MFP 
XXXXX  
000000000 
7 Output Date 8n YYYYMMDD  
8 Message Priority 
Indicator 
1a N  
9 Application Block Header 
Termination identifier 
1x }  
 Total Block Length 
(bytes) 
51   
 
Application Header Block - Output Example: 
{2:O55X104719980925NSCCMFPXXXXX000000000019980925N} 
G:  User Header Block 
      Not used by MFPS. 
  

---

## Page 13

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT Message Structure 13 
H:  Text Block 
• Block 4 is the text block. 
• The block begins with Carriage Return and Line Feed (CrLf) and ends with CrLf followed by a 
hyphen, "-". 
• Each field within block 4 begins with a ":", then a field tag, a ":", and the field content, as 
shown: 
:30:930814 
 
• The field content must not start with a ":", a "-" or a CrLf. Also, it must not be entirely 
composed of blank characters. If a field is made up of more than one line, each line must not 
start with a ":" or a "-". 
• Field content is immediately followed by a CrLf. In the text of user to user messages CrLf is a 
mandatory delimiter at the end of field content. (Refer to the section on “Technical 
Information” further down in this document for additional detail.) 
• The format is detailed for each message type presented in the record layout document (see 
Mutual Fund Profile Service Price/Rate Record Layouts ISO Format). 
• An example of the text block in a typical user-to-user message is as shown: 
 
{4: 
:20:MFPR601512345678 
:TT:MFRP 
:04A:SUBD/19980925 
:05G:165330/US/NYC 
:35B:ISIN US1960944031 
:IT:PRCO 
:35H:USD8,95 
:35B:ISIN US1960923081 
:IT:PRCO 
:35H:USD6,48 
:IT:DIVO 
:35H:USD0,0013331 
:DD:003 
:35B:ISIN US1960923081 
:04A:PRCE/19980924 
:IT:PRCC 
:35H:USD6,46 
-} 
 
 
Note:  Refer to Mutual Fund Profile Service Price/Rate Record Layouts ISO Format for field tags and message syntax. 
 
 
  

---

## Page 14

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT Message Structure 14 
I:  Trailer Block 
• It is used for control purposes, such as conveying information on how to handle the given 
message. 
• The format is the same for both the input (relative to S.W.I.F.T. network) and output message.  
• Mandatory for MFPS applications. 
 
Format: 1 22 3333333333333 444444 5  
 
Field No. Field Name Length 
(bytes) 
Values 
1 Trailer Block Header Initiation 
Identifier 
1 { 
2 Block Identifier 2X 5: 
3 Sub Block Identifier 13a {MAC:TRAILER} 
4 Training (Test) Indicator  6a {TNG} 
5 Trailer Block Termination Identifier 1x } 
 Maximum Block Length (bytes) 23  
 
For MFPS, the trailer block will have the following 2 formats: 
{5:{MAC:TRAILER}} 
(A total of 17 characters.) 
OR 
{5:{MAC:TRAILER}{TNG:}} 
(A total of 23 characters. The code, "TNG:", identifies the message as a training message, not a live 
message) 
The 2 formats will be used in the following ways: 
After MFPS Proprietary System goes into production, all live messages will use the first trailer format.  
For a new [[participant]] who wants to test the validity of any of its messages created, the second trailer format 
should be used. When MFPS receives the message sent by the new [[participant]], it will subject the message to 
validation process: If the received message fails the validation checking, a corresponding reject -message, with 
the appropriate error codes and the same trailer block (the second format), will be generated and sent back to 
the [[participant]]; if the received message passes the validation checking, it will not be loaded into MFPS 
database. 
  

---

## Page 15

ISO / S.W.I.F.T. Message Structure Reference Guide 
ISO/SWIFT Message Structure 15 
J:  Example of complete input message for MFPS: 
 
{1:F015501MFPXXXXX0000000000}{2:I55YNSCCMFPXXXXXN2002}{4: 
:20:MFPR601512345678 
:TT:MFRP 
:04A:SUBD/19980925 
:05G:165330/US/NYC 
:35B:ISIN US1960944031 
:IT:PRCO 
:35H:USD8,95 
:35B:ISIN US1960923081 
:IT:PRCO 
:35H:USD6,48 
:IT:DIVO 
:35H:USD0,0013331 
:DD:001 
:35B:ISIN US1960923081 
:04A:PRCE/19980924 
:IT:PRCC 
:35H:USD6,46 
-}{5:{MAC:TRAILER}} 
 
K:  Message Validation 
If a S.W.I.F.T. message is sent via the S.W.I.F.T. network, it will be rejected if an error is found in the message 
structure. The sender will receive a negative acknowledgment (NAK) from S.W.I.F.T. MFPS has no immediate 
plans to send or receive S.W.I.F.T. messages via the S.W.I.F.T. network. However, conformation to S.W.I.F.T. 
format is strictly observed: Any change applied by MFPS on the field specification is done within S.W.I.F.T. 
requirements. 
A message will be rejected if any of the following conditions are not met: 
1. The sequence of fields must be correct. 
2. Mandatory fields must be present. 
3. Only those permitted optional fields for a given message type are present. 
4. Each field has the correct content as specified by the field format. 
5. Only the permitted S.W.I.F.T. character set can be used. 
6. The decimal comma must be present in numbers and amounts. 
7. The date fields have the right content (e.g., the day not higher than 31). 
8. The conditional fields must be present if a certain condition is present. 
9. The number of digits after the decimal comma for the currency of the message field must  be 
correct (e.g., not more than 2 for USD.) 
10. All alphabetic characters in all headers must be in upper case. 
11. The curly brackets ({}) are to be used as delimiters, not in text.  

---

## Page 16

ISO / S.W.I.F.T. Message Structure Reference Guide 
Technical Information 16 
TECHNICAL INFORMATION 
A Field Separators 
Carriage Return/Line Feed (CrLf) 
Carriage Return/Line Feed (CrLf) is a two-byte field which has different meaning and representation in 
EBCDIC based systems (as IBM mainframe) and ASCII based systems (as most PC’s and LAN’s).  
CrLf in EBCDIC Based Systems 
1. Hexadecimal representation is ’0D25’. 
2. Does not indicate end of line (or record) and does not cause the next character to start a new line 
(or record). 
3. Does not have displayable representation. 
4. Can be seen when browsing or editing a file if the browsing or editing software has the capability 
of showing characters in their hexadecimal representation 
 
CrLf in ASCII Based Systems 
1. Hexadecimal representation is ’0D0A’. 
2. Indicates end of line (or record) and causes the next character to start a new line (or record).  
3. May have displayable representation (depends on the system). 
4. Cannot be seen when browsing or editing a file by standard browsing or editing software. Its 
existence is indicated by the fact that one line ends and another line starts. 
 
Rules for the use of Field Separators 
The following are S.W.I.F.T. rules regarding field separators in the message text (block 4):  
1. Fields are separated by a CrLf. 
2. The first field is preceded by a CrLf. 
3. The last field is followed by a CrLf. 
4. When the format of a sub-field is shown on a separate line than the format of the main field (e.g. 
field 35B) the sub-field is separated from the main field by a CrLf. 
5. When the format of a field or a sub-field indicates number of lines (as the format n*n), the lines are 
separated by a CrLf. 
 
MFPS follows S.W.I.F.T. rules regarding field separators with the exception as noted in the Batch Input section 
below. 
 
  

---

## Page 17

ISO / S.W.I.F.T. Message Structure Reference Guide 
Technical Information 17 
B Input/Output Requirements 
MFPS accepts input and creates output in either of two formats: 
Format 1 
1. The whole message is one record as follows: 
{1: [[BASIC]] Header Block}{2: Application Header Block}{4: Text Block}{5: Trailer Block} 
 
2. CrLf (where required) is present with its EBCDIC representation (‘0D25’). 
 
Example: 
The following is an example of block 4 (CrLf is indicated by the symbol <0D25>. The block is wrapped around because 
the page is not wide enough): 
{4:<0D25>:20:550319980925<0D25>:TT:MFRP<0D25>:04A:SUBD/19980925<0D25>:05:174045US 
BOSTON<0D25>:35B:ISIN US999999990<0D25>TEST SECURITY ISSUE<0D25>FOR EXAMPLE 
ONLY<0D25>IT:PRCO<0D25>:35H:USD7,01<0D25>:IT:DIVO<0D25>:35H:USD0,001344<0D25>: 
DD:001<0D25>-} 
Format 2 
1. The message is made of multiple records 
2. CrLf is not present 
3. When CrLf is required, the record ends and the next character starts a new record.  
 
Example: 
The following is an example of this format (each line is a separate record in the input file):  
{1:F015505MFPXXXXX0000000000}{2:I55YNSCCMFPXXXXXN2002}{4: 
:20:550319980925 
:TT:MFRP 
:04A:SUBD/19980925 
:05G:174045USBOSTON 
:35B:ISIN US999999990 
TEST SECURITY ISSUE 
FOR EXAMPLE ONLY 
:IT:PRCO 
:35H:USD7,01 
:IT:DIVO 
:35H:USD0,001344 
:DD:001 
-}{5:{MAC:TRAILER}} 
 
 
 
 

---

## Page 18

ISO / S.W.I.F.T. Message Structure Reference Guide 
Technical Information 18 
Mutual Fund Profile Service Batch Input 
MFPS receives batch input through DataTrak variable length files (RECFM=VB) or fixed length files 
RECFM=FB). The following limitations apply: 
Variable Length File 
1. Maximum record length is 3300 bytes (LRECL = 3304). 
2. Maximum message length is 3300 bytes. 
Note: When using Format 2 (as described below) the two bytes CrLf must be counted (even 
though they are not present) for every end of line, for the limit of 3300 bytes. 
3. Up to 20 secondary repeating sequences (Price/Rate sections) are allowed within a primary 
repeating sequence (Security Issue section). 
 
Fixed Length File 
1. Only Format 2 (as described above) is allowed. 
2. Record length is 80 bytes (LRECL = 80). 
3. Maximum message length is 3300 bytes. 
Note: the two bytes CrLf must be counted (even though they are not present) for every end of 
line, for the limit of 3300 bytes. 
4. Up to 20 secondary repeating sequences (Price/Rate section) are allowed within a primary 
repeating sequence 1 (Security Issue section). 
 
Mutual Fund Profile Service Batch Output 
MFPS submits batch output through AutoRoute variable length files (RECFM=VB) or fixed length files 
(RECFM=FB). The following apply: 
Variable Length File 
1. Only Format 1 (as described above) is created. 
2. Maximum record (message) length is 3500 bytes (LRECL = 3504). 
3. Up to 20 secondary repeating sequences (Price/Rate sections) are created within a primary 
repeating sequence (Security Issue section). 
Note:  When transferring an output file to an ASCII base system (as a PC or LAN) it might look like Format 2 as described 
above since EBCDIC CrLf will be translated to ASCII CrLf and create a new line. 
 
 
Fixed Length File 
1. Only Format 2 (as described above) is created. 
2. Record length is 90 bytes (LRECL = 90). 
3. Maximum message length is 3500 bytes. 
4. Up to 20 secondary repeating sequences (Price/Rate sections) are created within a primary 
repeating sequence (Security Issue section). 

---

## Page 19

ISO / S.W.I.F.T. Message Structure Reference Guide 
Technical Information 19 
Mutual Fund Profile Service Interactive Input 
MFPS receives interactive input through MQM queues. The following limitations apply:  
 
1. Only Format 1 (as described above) is allowed. 
2. Maximum record (message) length is 3300 bytes. 
3. Up to 20 secondary repeating sequences (Price/Rate sections) are allowed within a primary repeating 
sequence (Security Issue section). 
 
Mutual Fund Profile Service Interactive Output 
MFPS submits interactive output through MQM queues. The following apply: 
1. Only Format 1 (as described above) is created. 
2. Maximum record (message) length is 3500 bytes. 
3. Up to 20 secondary repeating sequences (Price/Rate sections) are created within a primary 
repeating sequence (Security Issue section). 
 
  

---

## Page 20

ISO / S.W.I.F.T. Message Structure Reference Guide 
Technical Information 20 
Output versus Input 
Output messages are built by MFPS on output time from input which have been received until that time. Output 
messages are not exact copy images of input messages. For example, if MFPS received three (3) messages, 
each containing one security issue with its price, on output time MFPS will sent out one message containing all 
three security issues with their prices. 
The following should be noted: 
Output Reference Numbers are created by MFPS and [[DO]] not relate to input Reference Numbers.  
When MFPS rejects an input message, it populates the output Related Reference Number with the input 
Reference Number. 
MFPS does not use the input Related Reference Number of a subsequent transaction (as correction) as a key 
to access original data. The key to access original data is always: 
• Security Issue 
• Information Type (first three bytes) 
• Effective Date 
 
On output time, if MFPS finds multiple Price/Rate data with the same key (e.g. a price for a specific security 
issue for a specific date and a price correction for same security issue for same date, or multiple price 
corrections for same security issue for same date) to be sent out, only the last piece of data will be sent out 
within that output cycle. As a result, a [[participant]] may receive a correction to a price or rate without previously 
receiving the original Price/Rate. The [[participant]] should treat this correction as the original Price/Rate.  
 
 
 
 
.

---

## Page 21

 
 
 
 
 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 