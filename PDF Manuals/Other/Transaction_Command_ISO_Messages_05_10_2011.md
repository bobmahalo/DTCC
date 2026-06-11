---
title: "ISO 15022 Message Layouts – MT530 Transaction Command Processing User's Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Transaction_Command_ISO_Messages_05_10_2011.pdf"
pages: 20
size: "409.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO 15022 Message Layouts – MT530 Transaction Command Processing User's Guide

**Original File:** [Transaction_Command_ISO_Messages_05_10_2011.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Transaction_Command_ISO_Messages_05_10_2011.pdf)  
**Category:** Other  
**Total Pages:** 20  
**File Size:** 409.1 KB  

---

## Page 1

[[settlement]]
ISO 15022 MESSAGE LAYOUTS – MT530 TRANSACTION COMMAND 
PROCESSING 
FEBRUARY 1, 2023 
[[DTCC]] Public (White)

---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com/ for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: February 1, 2023 
Publication Code:  SET 198 
Service: [[settlement]] 
Title: ISO 15022 Message Layouts – MT530 Transaction Command Processing 
 
 
[[DTCC]] Public (White)

---

## Page 3

 
 
TABLE OF CONTENTS 
Transaction Command ........................................................................................................................................ 4 
Standard ISO Input Message Blocks ................................................................................................................. 5 
[[BASIC]] Header Block............................................................................................................................................. 5 
Application Header Block .................................................................................................................................... 7 
User Header Block .............................................................................................................................................. 7 
Text Block ........................................................................................................................................................... 9 
Transaction Command ...................................................................................................................................... 10 
Mandatory Sequence A - General Information ................................................................................................. 10 
Mandatory Sequence B - Request Details ....................................................................................................... 10 
Optional, Repetitive Subsequence A1 - Linkages (Reference) ....................................................................... 12 
Optional, Repetitive Subsequence A1 - Linkages (Reference) ....................................................................... 13 
Optional, Repetitive Subsequence A1 - Linkages (Reference) ....................................................................... 13 
Optional, Repetitive Subsequence A1 - Linkages (Reference) ....................................................................... 13 
Optional, Repetitive Subsequence A1 - Linkages (Reference) ....................................................................... 14 
Optional, Repetitive Subsequence A1 - Linkages (Reference) ....................................................................... 14 
Optional, Repetitive Subsequence A1 - Linkages (Reference) ....................................................................... 14 
Optional, Repetitive Subsequence A1 - Linkages (Reference) ....................................................................... 15 
Optional, Repetitive Subsequence A1 - Linkages (Reference) ....................................................................... 15 
Optional, Repetitive Subsequence A1 - Linkages (Reference) ....................................................................... 15 
Optional Sequence C - Additional Information ................................................................................................. 16 
Optional Sequence C1 - Status ........................................................................................................................ 17 
Optional Repetitive Subsequence C1a - Reason .......................................................................................... 17 
Release Notes ..................................................................................................................................................... 19 
 
[[DTCC]] Public (White)

---

## Page 4

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Transaction Command 4 
TRANSACTION COMMAND 
This MT530 message type is sent by a [[DTC]] [[participant]] to [[DTCC]] for messages related to receiver authorized 
delivery (RAD), authorizations, cancels, pend holds, promotions, and exemptions.  
 
[[DTCC]] Public (White)

---

## Page 5

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Standard ISO Input Message Blocks 5 
STANDARD ISO INPUT MESSAGE BLOCKS 
This [[DTC]] proprietary ISO header message is an alternative to the SWIFT ISO header message. 
All ISO messages destined for [[DTC]] must contain the following 4 message blocks: 
• [[BASIC]] Header Block - Contains the general information identifying the message and some additional 
control information.  
• Application Header Block - Contains information specific to the application and is required for messages 
exchanged between users or between the system and users.  
• User Header Block - Contains user reference information.  
• Text Block - Contains the actual data being transmitted.  
 
All alphabetic characters in the 3 header blocks ([[BASIC]], Application and User) must be in upper-case. The 
system does not recognize lower-case letters as equivalent to upper-case. 
Key: M = Mandatory, O = Optional 
[[BASIC]] Header Block 
Field Description Position  Length  Content Rules Input Value 
Starting Block Delimiter 1 1 The character { is used to indicate 
the beginning of a block 
{ 
Block Identifier 2 2 Must contain a value of “1:” 1: 
Message Identifier 4 1 Must contain a value of “F” F 
Protocol Identifier 5 2 Must contain a value of "01" 01 
Submitter's Bank/Firm Code 7 8 Submitter's Bank Identifier Code 
(BIC) or the user's [[participant]] [[ID]] 
(If the submitter is a Group User, 
this [[ID]] must be connected in 
[[DTCC]]'s Group User eligibility 
table.) 
12345678 
Logical Terminal 15 1 Identifies terminal type. "A" for 
Swift messages, "X" for non-Swift 
messages 
X 
Branch Code 16 3 Identifies branch 123 
Session Number 19 4 A 4 digit value assigned by the 
submitter. Its [[default]] is 0000. The 
Session Number is not validated 
by the receiving [[DTCC]] subsidiary 
0000 
Sequence Number 23 6 A 6 digit value assigned by the 
submitter. Its [[default]] is 000000. 
The Session Number is not 
000000 
[[DTCC]] Public (White)

---

## Page 6

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Standard ISO Input Message Blocks 6 
Field Description Position  Length  Content Rules Input Value 
validated by the receiving [[DTCC]] 
subsidiary. 
Ending Block Delimiter 29 1 The character } is used to indicate 
the end of a block 
} 
 
 
 
 
 
 
[[DTCC]] Public (White)

---

## Page 7

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Standard ISO Input Message Blocks 7 
Application Header Block 
Field Description Position  Length  Content Rules Input Value 
Starting Block Delimiter 30 1 The character { is used to indicate 
the beginning of a block. 
{ 
Block Identifier 31 2 Must contain a value of "2:" 2: 
Input/Output Identifier 33 1 Must contain a value of "I" I 
ISO Message Type 34 3 Must contain a valid 3 digit ISO 
Message Type [[ID]] 
530 
Recipient's Bank/Firm Code 37 8 The value of this field should be 
one of the following based on 
function definition: 
1. Recipient's Bank Identifier 
Code (BIC) 
2. Recipient's [[participant]] [[ID]] 
3. Value of "INTDTC" (Internal 
[[DTC]] User) when the function 
used is a one party 
transaction and the recipient 
of the message is an internal 
[[DTC]] application 
12345678 
Logical Terminal 45 1 Identifies a terminal type when a 
BIC [[ID]] is entered as the 
Recipient's Bank/Firm Code. 
X 
Branch Code 46 3 Identifies branch when a BIC [[ID]] is 
entered as the Recipient's 
Bank/Firm Code. 
123 
Message Priority 49 1 Must contain a value of "N" N 
Delivery Monitoring 50 1 Must contain a value of "2" 2 
Ending Block Delimiter 51 1 The character } is used to indicate 
the end of a block. 
} 
 
User Header Block 
Field Description Position  Length  Content Rules Input Value 
Starting Block Delimiter 52 1 The character { is used to 
indicate the beginning of a 
block. 
{ 
Block Identifier 53 2 Must contain a value of "3:" 3: 
Version Number Tag 55 5 Must contain a value of "{113:" {113: 
[[DTCC]] Public (White)

---

## Page 8

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Standard ISO Input Message Blocks 8 
Field Description Position  Length  Content Rules Input Value 
Version Number 60 4 Must contain a value of "0301" 
for [[settlement]] ISO Messages. 
1234 
Ending Delimiter of Version 
Number Tag 
64 1 The character } is used to 
indicate the end of the tag 
} 
Submitter's Reference Key 
Tag 
65 5 Must contain a value of "{108:" {108: 
Submitter's Reference Key 70 16 Unique key created by the 
submitter to identify the 
transaction 
XXXXXXXXXXXXXXXX 
Ending Delimiter of 
Submitter's Reference Key 
Tag 
86 1 The character } is used to 
indicate the end of the tag. 
} 
Ending Block Delimiter 87 1 The character } is used to 
indicate the end of a block. 
} 
 
  
[[DTCC]] Public (White)

---

## Page 9

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Standard ISO Input Message Blocks 9 
Text Block 
Field Description Position  Length  Content Rules Input Value 
Starting Block Delimiter 88 1 The character { is used to 
indicate the beginning of a 
block. 
{ 
Starting Block Identifier 89 2 Must contain a value of "4:" 4: 
Carriage Return-Line Feed 
(crlf) 
91 2 Must contain the carriage return-
line feed (crlf) combination. 
crlf 
Message Data 93 1-27,000 
bytes 
The actual contents of the 
message will be inserted here. 
 
End of Message Data 
Carriage Return-Line Feed 
(crlf) and hyphen 
 3 Must contain the carriage return-
line feed combination followed 
by a hyphen. 
crlf- 
Ending Block Delimiter  1 The character} is used to 
indicate the end of a block. 
} 
 
[[DTCC]] Public (White)

---

## Page 10

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Transaction Command 10 
TRANSACTION COMMAND 
Business Transaction: Transaction Command 
ISO Message Type: MT530 - Transaction Command 
This message is sent by a [[participant]] to [[DTCC]] for messages related to receiver authorized delivery (RAD), 
authorizations, cancels, pend holds, promotions, and exemptions.  
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - General 
Information 
:16R:   GENL 
O Sender's Reference Number 
Sender's reference number 
:20C: :SEME// 16x 
O Message Function 
Field that identifies the 
function of the message 
:23G:  NEWM 
O Safekeeper 
Identifies account where 
financial instruments are 
maintained. 
:97A:  :SAFE//  35x  
M End of Block - General 
Information 
:16S:  GENL 
 
Mandatory Sequence B - Request Details 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Request 
Details  
:16R:    REQD  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction. RELA is 
also used with the text MULTIPLE to 
[[DTCC]] Public (White)

---

## Page 11

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Transaction Command 11 
M/O Field Description Tag Qualifier(s) Content Rules 
indicate multiple reference numbers that 
are specified in the B1 subsequence. 
Multiple reference numbers are specified 
with a command scope of GLBL, LIST 
and ASTN.  
M Command Indicator 
A [[settlement]] command that 
is applied to transactions. For 
example, authorize, exempt, 
and pend are commands. 
:22F:  :SETT/DTCY/  4x  
Command must be one of the following: 
AUTH - authorization, XMPT - exemption, 
UXMP - unexemption (Invalid with the 
SECU scope), CANC - cancel transaction 
(Valid only with the LIST scope and 
invalid with the CNSS transaction type), 
RCAN – RAD Receiver cancels (only 
valid for RAD receiver cancels, RAD 
deliverer cancels should use CANC), 
PENC - cancel pending transaction (Valid 
only with the LIST scope), PENH - pend 
hold transaction (Valid only with the LIST 
scope), PENB - pend hold with blockage 
(Valid only with the LIST scope), PENA - 
pend activate to release the pend hold or 
hold with blockage (Valid only with the 
LIST scope), MODE - change mode 
(Invalid with the LIST scope), PATH - 
partially authorize (Valid only with the 
SECU and LIST scopes), PXMP - 
partially exempt (Valid only with the 
SECU and LIST scopes), RLSD - release 
(Valid only with the LIST, ASTN or SECU 
scopes), PAUS - pause (Valid only with 
the GLBL scope), UNPS - unpause (Valid 
only with the GLBL scope), CPRI - 
promote transactions (Valid only with the 
LIST scope), UNAU - unauthorize (Invalid 
with the SECU scope), FREL - free 
release request (Valid only with the LIST 
scope), VREL - valued release request 
(Valid only with the LIST scope), FEDR - 
free release request to Federal Reserve 
Bank (Valid only with the LIST scope), 
FRAP - free release approval (Valid only 
with the LIST scope), VRAP - valued 
release approval (Valid only with the LIST 
scope), FEDA - release approval by 
Federal Reserve Bank (Valid only with 
the LIST scope), QIBA- Third Party 
Approval for a Security Holder tracked 
transaction (Only valid with a command 
scope of LIST), QIBD - Third Party Dis-
Approval for a Security Holder tracked 
transaction (Only valid with a command 
scope of LIST), RAUT - receiver RAD 
authorize (Valid only with the LIST 
[[DTCC]] Public (White)

---

## Page 12

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Transaction Command 12 
M/O Field Description Tag Qualifier(s) Content Rules 
scope), RRVS – receiver reversal (Valid 
only with the LIST scope), FULL – Fully 
Fund Acronym (Valid only with the ACRM 
scope); PART – Partially Fund Acronym 
(Valid only with the ACRM scope); RTPY 
– Refusal to Pay Acronym (Valid only 
with the ACRM scope); TRTP – 
Temporary Refusal to Pay Acronym 
(Valid only with the ACRM scope); PNCL 
– Pend Cancel A Transaction in Staging 
Area (Valid only with the LIST scope) 
M Command Scope Indicator 
Defines the parameters of 
the [[settlement]] command that 
is applied to transactions. For 
example, scope could apply 
to transactions globally, in a 
list, or by [[Asset]] class-
transaction type. 
:22F:  :PROC/DTCY/  4x  
Command scope must be one of the 
following: GLBL - global (Invalid with the 
RCAN, RRVS, CANC, RAUT, PENC, 
PENH, PENB and PENA commands and 
invalid with the CNSS transaction type), 
ASTN - by [[Asset]] class/transaction type 
(Invalid with the CANC, PENC, PENH, 
PENB and PENA commands. LIST - list 
of transactions, SECU - by security (Valid 
only with the PATH, PXMP, RAUT, 
RCAN, RRVS and RLSD commands), 
ACTV or PASS - authorization profile 
status (Valid only with the MODE 
command). ACRM – Acronym Scope 
(Only valid for FULL, PART, RTPY, TRTP 
and PNCL) 
 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:    LINK  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction.  
M End of Block - Linkages  :16S:    LINK  
 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
[[DTCC]] Public (White)

---

## Page 13

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Transaction Command 13 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:    LINK  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction.  
M End of Block - Linkages  :16S:    LINK  
 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:    LINK  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction.  
M End of Block - Linkages  :16S:    LINK  
 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:    LINK  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction.  
M End of Block - Linkages  :16S:    LINK  
 
[[DTCC]] Public (White)

---

## Page 14

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Transaction Command 14 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:    LINK  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction.  
M End of Block - Linkages  :16S:    LINK  
 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:    LINK  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction.  
M End of Block - Linkages  :16S:    LINK  
 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:    LINK  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction.  
M End of Block - Linkages  :16S:    LINK  
[[DTCC]] Public (White)

---

## Page 15

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Transaction Command 15 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:    LINK  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction.  
M End of Block - Linkages  :16S:    LINK  
 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:    LINK  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction.  
M End of Block - Linkages  :16S:    LINK  
 
Optional, Repetitive Subsequence A1 - Linkages (Reference) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:    LINK  
M Reference [[ID]] 
A reference number carried 
throughout the life of a 
transaction. Could be 
assigned by a matching 
utility, the deliverer, and the 
IMS or ATP systems. 
:20C:  :COMM//  
:PREV//  
:RELA//  
:TRRF//  
16x  
COMM is used for the TID assigned to 
the transaction by the matching utility. 
TRRF is used with the TID assigned to 
the transaction by the deliverer. PREV is 
used with the TID ATP assigned to the 
transaction. RELA is used with the TID 
IMS assigned to the transaction.  
M End of Block - Linkages  :16S:    LINK  
[[DTCC]] Public (White)

---

## Page 16

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Transaction Command 16 
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - Request 
Details 
:16S:  REQD 
 
Optional Sequence C - Additional Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Additional 
Information  
:16R:    ADDINFO  
O Classification Type 
Type of [[DTCC]] defined [[Asset]] 
class 
:12A:  :CLAS/DTCY/  4x4x  
The first 4 characters is a [[DTC]] defined 
[[Asset]] class: ALLA - all [[Asset]] classes 
MMIS - money market instruments EQTS 
- equities CRBD - corporate [[Bonds]] MUNI 
- municipal [[Bonds]] The last 4 characters is 
a valid transaction type: ALLT - all 
transaction types MITS - matched 
institutional trades NDOC - night deliver 
orders ACAT - ACATS transactions 
CNSS - [[CNS]] transactions RDRP - 
reintroduced drops BALO - balance 
orders from [[NSCC]] PETS - [[participant]] 
entered transactions LMIT - late affirmed 
institutional trades  
O Identification of the Financial 
Instrument  
ISIN (Country Code, [[CUSIP]] 
and Check Digit) 
/XX/ (Proprietary scheme for 
MMI [[issuer]] Acronym) 
:35B:  ISIN 
/XX/ACRM 
The literal "ISIN" followed by a space 
followed by the 12 character ISIN.  
Example-ISIN US1234567891. Note-[[DTC]] 
does not accept Non U.S. ISIN  
Or The literal “/XX/” followed by literal 
scheme “ACRM” followed by the actual 4 
character MMI [[issuer]] Acronym. There is 
a space between the literal scheme 
“ACRM” and the actual 4 character MMI 
[[issuer]] Acronym. 
Example: 
/XX/ACRM AAA* 
O Quantity of financial 
instrument to be settled 
UNIT (Quantity of expressed 
as units such as share 
quantity.) 
FAMT (Partial Funding 
Amount in USD for PART 
command) 
:36B:  :SETT//UNIT 
:SETT//FAMT 
UNIT/999999999,  
At least 1 whole digit is required. No more 
than 9 may be present. Fractions are not 
allowed. A decimal comma is always 
required. 
Or FAMT/999999999999,99 
 At least 1 whole digit required. No more 
than 12 whole digits may be present. At 
most 2 fractional digits are allowed. A 
decimal comma is always required. 
[[DTCC]] Public (White)

---

## Page 17

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Transaction Command 17 
M/O Field Description Tag Qualifier(s) Content Rules 
  
O Loan Date 
Loan date for a pledge or 
pledge release transaction 
:98A:  :EFDD//  yyyymmdd 
O Refusal to Pay Contact  
Contact Person Name and 
Phone Number 
:95Q: :MEOR// 4*35x 
Contact Name and phone number is only 
valid for RTPY or TRTP Commands. 
There is a carriage return and line feed 
between the Contact Name and Phone 
Number. The Phone Number can accept 
10 numeric digits as shown in the 
example. 
Example: 
:MEOR//Mr. Smith 
8885551212 
O Pledgor's [[DTCC]] [[participant]] 
Number 
 
:95R:  :MEOR//  00009999  
0000 followed by 4 digits. All 4 digits are 
required.  
O Pledgee's [[DTCC]] [[participant]] 
Number 
 
:95R:  :MERE//  00009999  
0000 followed by 4 digits. All 4 digits are 
required.  
M End of Block - Additional 
Information  
:16S:    ADDINFO  
 
Optional Sequence C1 - Status 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Additional 
Information 
:16R:  STAT 
M INSTRUCTION 
PROCESSING STATUS 
:25D:  :IPRC//PACK 
:IPRC//CAND 
:IPRC//RRVS 
:IPRC//RTPY 
:IPRC//TRTP 
CAND- Cancelled (used for cancel 
commands), PACK – Acknowledged, 
RRVS – Receiver Reversal, 
RTPY – Refusal to Pay Acronym, 
TRTP – Temporary Refusal to Pay 
Acronym 
Optional Repetitive Subsequence C1a - Reason 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – Reason :16R:   REAS 
[[DTCC]] Public (White)

---

## Page 18

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Transaction Command 18 
M Reason :24B:  :CAND//NARR 
:PACK//NARR 
:RRVS//NARR 
:RTPY//NARR 
:TRTP//NARR 
Narrative Reason  
O Reason Narrative :70D:  :REAS// Narrative Comments 2*13 to support 
proprietary comments length 
M End of Block Reason :16S:  REAS 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block Status :16S:   STAT 
 
 
[[DTCC]] Public (White)

---

## Page 19

ISO 15022 Message Layouts – MT530 Transaction Command Processing 
Release Notes 19 
RELEASE NOTES 
02/09/2023 Reformatted the document to current on brand template.  Made small changes to reconcile 
the most recent document with the May 2011 version. These included noting three 
mandatory fields which had appeared optional in Mandatory Sequence B for Reference [[ID]], 
Command Indicator, and Command Scope Indicator.   
2/11/2016 Updated the Partial Funding Amount field in “Optional Sequence C - Additional Information” 
to allow a 12-digit dollar amount and 2-digit decimals. 
12/18/2015 Added documentation for the [[DTC]] proprietary ISO header message. This is an alternative to 
the SWIFT ISO header message.  
09/01/2015 Updates made to the MT530 Transaction Command message for the MMI Finality Through 
Optimization initiative. New command indicators were added: Full; PART; RTPY; TRTP; and 
PNCL. Acronym and Partial Funding Amount were added to the Additional Information 
sequence. Instruction processing statuses and reasons were also updated with new 
qualifiers.  
 
[[DTCC]] Public (White)

---

## Page 20

 
 
 
FOR MORE INFORMATION 
Email [[DTCC]] at: 
DTCSupport@[[DTCC]].com  
or visit us on the web at: 
http://www.[[DTCC]].com/client-center  
 
[[DTCC]] Public (White)