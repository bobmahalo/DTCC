---
title: "MT548 IPA Participant Confirmation (Output to MT530 Transaction Command)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MT548_%20IPA_Participant_Confirmation.pdf"
pages: 16
size: "2396.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MT548 IPA Participant Confirmation (Output to MT530 Transaction Command)

**Original File:** [MT548_ IPA_Participant_Confirmation.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MT548_%20IPA_Participant_Confirmation.pdf)  
**Category:** Other  
**Total Pages:** 16  
**File Size:** 2396.9 KB  

---

## Page 1

[[settlement]]
MT548 [[IPA]] [[participant]] CONFIRMATION (OUTPUT TO MT530 TRANSACTION 
COMMAND) 
OCTOBER 24, 2022 
[[DTCC]] Public (White)

---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com/ for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 18, 2022 
Publication Code: SET 194 
Service: [[settlement]] 
Title: MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
 
[[DTCC]] Public (White)

---

## Page 3

 
 
TABLE OF CONTENTS 
Standard ISO Output Message Blocks............................................................................................................... 4 
[[BASIC]] Header Block............................................................................................................................................. 4 
Application Header Block .................................................................................................................................... 5 
User Header Block .............................................................................................................................................. 6 
Text Block ........................................................................................................................................................... 7 
SWIFT ISO Input Message Blocks ...................................................................................................................... 8 
[[BASIC]] Header Block............................................................................................................................................. 8 
Application Header Block .................................................................................................................................... 9 
User Header Block ............................................................................................................................................10 
Text Block .........................................................................................................................................................10 
MT548 - [[IPA]] [[participant]] Confirmation .............................................................................................................. 11 
Mandatory Sequence A - General Information .................................................................................................11 
Mandatory Subsequence A1 – Linkages (IMS TID) ........................................................................................11 
Mandatory Subsequence A2 - Status .............................................................................................................12 
Optional Subsequence A2a – Reason ..........................................................................................................12 
Optional Sequence B - [[settlement]] Transaction Details ..................................................................................13 
Release Notes ..................................................................................................................................................... 15 
 
[[DTCC]] Public (White)

---

## Page 4

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
Standard ISO Output Message Blocks 4 
STANDARD ISO OUTPUT MESSAGE BLOCKS 
This [[DTC]] proprietary ISO header message is an alternative to the SWIFT ISO header message.  
All ISO messages destined for [[DTC]] must contain the following 4 message blocks:  
• [[BASIC]] Header Block - Contains the general information identifying the message and some additional 
control information.  
• Application Header Block - Contains information specific to the application and is required for messages 
exchanged between users or between the system and users.  
• User Header Block - Contains user reference information.  
• Text Block - Contains the actual data being transmitted.  
 
Key: M = Mandatory, O = Optional 
[[BASIC]] Header Block 
M/O Tag Length Field Description Example Description 
M 1 1 Starting Block 
Delimiter 
{ The character { is used to indicate the 
beginning of a block 
M 2 2 Block Identifier 1: Must contain a value of "1:" 
M 4 1 Message Identifier F Must contain a value of "F" 
M 5 2 Protocol Identifier 01 Must contain a value of "01" 
M 7 8 Recipient's 
Bank/Firm Code 
12345678 Recipient's Bank Identifier Code (BIC) 
or the user's [[participant]] [[ID]] (If the 
recipient is a Group User, this [[ID]] must 
be connected in [[DTCC]]'s Group User 
eligibility table) 
M 15 1 Logical Terminal X Identifies terminal type 
M 16 3 Branch Code 123 Identifies branch 
M 19 4 Session Number 0000 A 4 digit value assigned by a [[DTCC]] 
subsidiary. Its [[default]] is 0000 
M 23 6 Sequence Number 000000 A 6 digit value assigned by a [[DTCC]] 
subsidiary. Its [[default]] is 000000 
M 29 1 Ending Block 
Delimiter 
} The character } is used to indicate the 
end of a block 
 
  
[[DTCC]] Public (White)

---

## Page 5

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
Standard ISO Output Message Blocks 5 
Application Header Block 
M/O Tag Length Field Description Example Description 
M 30 1 Starting Block 
Delimiter 
{ The character { is used to indicate the 
beginning of a block 
M 31 2 Block Identifier 2: Must contain a value of "2:" 
M 33 1 Input/ Output 
Identifier 
O Must contain a value of "O" 
M 34 3 ISO Message Type 548 Must contain a valid 3 digit ISO 
Message Type [[ID]] 
M 37 4 Receipt Time HHMM Format is: HHMM 
The time the message was received by 
the receiving [[DTCC]] subsidiary 
M 41 6 Receipt Date YYMMDD Format is: YYMMDD 
The date the message was received by 
the receiving [[DTCC]] subsidiary 
M 47 8 Submitter's 
Bank/Firm Code 
12345678 Submitter's Bank Identifier Code (BIC) 
or the Submitter's [[participant]] [[ID]] (the 
same number passed to [[DTC]] in the 
ISOINP message) 
M 55 1 Logical Terminal x Identifies terminal type. "A" for Swift 
messages, "X" for         non-Swift 
messages 
M 56 3 Branch Code  Always Spaces 
M 59 4 Session Number 1234 A 4 digit value assigned by the 
submitter. The session number is set to 
0000 if it is not passed by a [[DTCC]] 
subsidiary 
M 63 6 Sequence Number 123456 A 6 digit value assigned by the 
submitter. The sequence number is set 
to 000000 if it is not passed by a [[DTCC]] 
subsidiary 
M 69 6 Transmission Date YYMMDD Format is: YYMMDD 
The date the message was sent from a 
[[DTCC]] subsidiary to the recipient 
M 75 4 Transmission Time HHMM Format is: HHMM 
The time the message was sent from a 
[[DTCC]] subsidiary to the recipient 
M 79 1 Message Priority N Must contain a value of “N” 
M 80 1 Ending Block 
Delimiter 
} The character } is used to indicate the 
end of a block 
 
[[DTCC]] Public (White)

---

## Page 6

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
Standard ISO Output Message Blocks 6 
User Header Block 
M/O Tag Length Field Description Example Description 
M 81 1 Starting Block 
Delimiter 
{ The character { is used to indicate the 
beginning of a block 
M 82 2 Block Identifier 3: Must contain a value of "3:" 
M 84 5 Version Number 
Tag 
{113: Must contain a value of "{113:" 
M 89 4 Version Number 1234 Must contain a value of "0301" for 
[[settlement]] ISO Messages 
Must contain a value of "0701" for 
EuroCCP ISO Messages 
M 93 1 Ending Delimiter of 
Version Number 
Tag 
} The character } is used to indicate the 
end of the tag 
M 94 5 Submitter's 
Reference Key Tag 
{108: Must contain a value of "{108:" 
M 99 16 Submitter's 
Reference Key 
XXXXXXXXXXX
XXXXX 
Unique key created by the submitter to 
identify the transaction 
Format: 16x 
M 115 1 Ending Delimiter of 
Submitter's 
Reference Key Tag 
} The character } is used to indicate the 
end of the tag 
M 116 5 Tag for expanded 
time 
{115: Must contain value of "{115:" 
M 121 11 Expanded Time HH.MM.SS.NN Format is: HH.MM.SS.NN 
 Since blocks 1 and 2 [[DO]] not allow for 
seconds in the time fields, this field 
gives the time down to the second. It 
contains either the time a [[DTCC]] 
subsidiary received the message from 
the submitter or the time the message 
was created by a [[DTCC]] subsidiary 
M 132 1 Ending Delimiter of 
Expanded Time 
Tag 
} The character } is used to indicate the 
end of the tag 
M 133 1 Ending Block 
Delimiter 
} The character } is used to indicate the 
end of a block 
 
  
[[DTCC]] Public (White)

---

## Page 7

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
Standard ISO Output Message Blocks 7 
Text Block 
M/O Tag Length Field Description Example Description 
M 134 1 Starting Block 
Delimiter 
{ The character { is used to indicate the 
beginning of a block 
M 135 2 Starting Block 
Identifier 
4: Must contain a value of "4:" 
M 137 2 Carriage Return – 
Line Feed (crlf) 
crlf Must contain the carriage return - line 
feed (crlf) combination 
M 139 1-27,000 
bytes 
Message Data  The actual contents of the message will 
be inserted here 
M  3 End of Message 
Data Carriage 
Return - Line Feed 
(crlf) and hyphen 
crlf - Must contain the carriage return - line 
feed combination followed by a hyphen 
M  1 Ending Block 
Delimiter 
} The character } is used to indicate the 
end of a block 
 
[[DTCC]] Public (White)

---

## Page 8

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
SWIFT ISO Input Message Blocks 8 
SWIFT ISO INPUT MESSAGE BLOCKS 
All ISO messages destined for [[DTC]] must contain the following 4 message blocks.  
• [[BASIC]] Header Block - Contains the general information identifying the message and some additional 
control information. 
• Application Header Block - Contains information specific to the application and is required for messages 
exchanged between users or between the system and users.  
• User Header Block - Contains user reference information. 
• Text Block - Contains the actual data being transmitted. 
 
All alphabetic characters in the 3 header blocks ([[BASIC]], Application and User) must be in upper -case. The 
system does not recognize lower-case letters as equivalent to upper-case. 
[[BASIC]] Header Block 
Field Description Position  Length  Content Rules Input Value 
Starting Block Delimiter 1 1 The character { is used to indicate 
the beginning of a block 
{ 
Block Identifier 2 2 Must contain a value of “1:” 1: 
Message Identifier 4 1 Must contain a value of “F” F 
Protocol Identifier 5 2 Must contain a value of "01" 01 
Submitter's Bank/ Firm Code 7 8 Submitter's Bank Identifier Code 
(BIC) or the user's [[participant]] [[ID]] 
(If the submitter is a Group User, 
this [[ID]] must be connected in 
[[DTCC]]'s Group User eligibility 
table) 
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
validated by the receiving [[DTCC]] 
subsidiary 
000000 
[[DTCC]] Public (White)

---

## Page 9

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
SWIFT ISO Input Message Blocks 9 
Field Description Position  Length  Content Rules Input Value 
Ending Block Delimiter 29 1 The character } is used to indicate 
the end of a block 
} 
 
Application Header Block 
Field Description Position  Length  Content Rules Input Value 
Starting Block Delimiter 30 1 The character { is used to indicate 
the beginning of a block 
{ 
Block Identifier 31 2 Must contain a value of "2:" 2: 
Input/ Output Identifier 33 1 Must contain a value of "I" I 
ISO Message Type 34 3 Must contain a valid 3 digit ISO 
Message Type [[ID]] 
548 
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
Recipient's Bank/Firm Code 
X 
Branch Code 46 3 Identifies branch when a BIC [[ID]] is 
entered as the Recipient's 
Bank/Firm Code 
123 
Message Priority 49 1 Must contain a value of "N" N 
Delivery Monitoring 50 1 Must contain a value of "2" 2 
Ending Block Delimiter 51 1 The character } is used to indicate 
the end of a block 
} 
 
  
[[DTCC]] Public (White)

---

## Page 10

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
SWIFT ISO Input Message Blocks 10 
User Header Block 
Field Description Position  Length  Content Rules Input Value 
Starting Block Delimiter 52 1 The character { is used to 
indicate the beginning of a block 
{ 
Block Identifier 53 2 Must contain a value of "3:" 3: 
Version Number Tag 55 5 Must contain a value of "{113:" {113: 
Version Number 60 4 Must contain a value of "0301" 
for [[settlement]] ISO Messages 
Must contain a value of "0701" 
for EuroCCP ISO Messages 
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
86 1 The character} is used to 
indicate the end of the tag 
} 
Ending Block Delimiter 87 1 The character } is used to 
indicate the end of a block 
} 
 
Text Block 
Field Description Position  Length  Content Rules Input Value 
Starting Block Delimiter 88 1 The character { is used to indicate 
the beginning of a block 
{ 
Starting Block Identifier 89 2 Must contain a value of "4:" 4: 
Carriage Return - Line Feed 
(crlf) 
91 2 Must contain the carriage return - 
line feed (crlf) combination 
crlf 
Message Data 93 1-27,000 
bytes 
The actual contents of the 
message will be inserted here 
 
End of Message Data 
Carriage Return - Line Feed 
(crlf) and hyphen 
 3 Must contain the carriage return - 
line feed combination followed by 
a hyphen 
crlf- 
Ending Block Delimiter  1 The character} is used to indicate 
the end of a block 
} 
 
[[DTCC]] Public (White)

---

## Page 11

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
MT548 - [[IPA]] [[participant]] Confirmation 11 
MT548 - [[IPA]] [[participant]] CONFIRMATION  
Business Transaction: [[participant]] Confirmation   
ISO Message Type: MT548 – [[settlement]] Status and Processing Advice   
The message will be used to send confirmation/status updates to participants and IPAs.  
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
O Transaction Update 
Date/Time 
:98C: :PREP// yyyymmddhhmmss 
 
Mandatory Subsequence A1 – Linkages (IMS TID) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Linkages :16R:     LINK  
M IMS Transaction [[ID]] 
Inventory Management 
system (IMS) transaction 
identifier 
:20C:   :RELA//  16x  
M End of Block - Linkages :16S:     LINK  
 
  
[[DTCC]] Public (White)

---

## Page 12

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
MT548 - [[IPA]] [[participant]] Confirmation 12 
Mandatory Subsequence A2 - Status 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Status  :16R:     STAT  
M Status Code 
The status of processing 
:25D:  :SETT/DTCYSTAT/  
 
4x 
• RCVD – Received 
• ACPT – Accepted 
• NACT – Not Accepted 
• INFO – Informational  
 
Optional Subsequence A2a – Reason 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – Reason  :16R:     REAS 
M Reason 
Reason Code 
:24B:  :PACK/DTCYREAS/ 
 
:RJET/DTCYREAS/  
(If Status Code is  
NACT) 
4x 
• PROF – Processed due to 
Partially/Fully Funded Message 
or 
• Funding Profile has been added 
• CMND – Processed due to 
Funding Decision command 
• ANFF – Acronym is not fully 
funded 
• UNRT – Not processed due to 
unknown rate for acronym 
• MPRP – Not processed due to 
MPs and RPs of the acronym 
• FUND – Partial Funded Amount 
is less than the current partial 
funding 
• PNDM–Command is processed 
but transactions are pending in 
Staging Area and waiting for all 
other IPAs to make a funding 
decision  
• OTHR – Other reason; More 
details in Error message 
O Error Message :70D: :REAS// 35x crlf 35x crlf 35x crlf 35x 
crlf 35x crlf 35x 
The maximum length [[DTC]] will 
accept is 210, 6 lines of 35 
characters. Each line should be 
separated by a CRLF (carriage 
return - line feed). 
M End of Block – Reason   :16S:     REAS 
 
[[DTCC]] Public (White)

---

## Page 13

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
MT548 - [[IPA]] [[participant]] Confirmation 13 
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - Status :16S:     STAT 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - General 
Information 
:16S:     GENL 
 
Optional Sequence B - [[settlement]] Transaction Details 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Transaction 
Details 
:16R:     SETTRAN  
M Acronym 
MMI [[issuer]] Acronym  
:35B:   /XX/<acronym> 
“/XX/” followed by  4 characters of 
MMI [[issuer]] Acronym 
M Funding Amount :36B: :SETT//UNIT 15d 
Note:  
For use with SWIFT Header 
Message. 
M Safekeeper 
Identifies account where 
financial instruments are 
maintained.  
:97A:  :SAFE// 35x 
M Receive/Deliver Indicator :22H: REDE • DELI – Deliverer 
• RECE – Receiver 
Note: 
For use with SWIFT Header 
Message. 
M Payment Indicator :22H: PAYM • APMT – Against Payment 
• FREE – Free of Payment 
Note: 
For use with SWIFT Header 
Message. 
[[DTCC]] Public (White)

---

## Page 14

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
MT548 - [[IPA]] [[participant]] Confirmation 14 
M/O Field Description Tag Qualifier(s) Content Rules 
M Funding Type Indicator :22F: :SETR/DTCYFUND/ 4x 
• FULL – Fully Funded 
• PART – Partially Funded 
• RTPY – Refusal To Pay 
• TRTP – Temporary Refusal To 
Pay 
• PNCL – PEND Cancel a 
Transaction in Staging Area 
M [[settlement]] Date 
Date on which the 
transaction should be settled. 
:98A:: :SETT// yyyymmdd 
O Narrative - Comments 
 
:70E: :SPRO// 35x crlf 35x crlf 35x crlf 35x crlf 35x 
crlf 35x crlf 35x crlf 35x crlf 35x crlf 
35x 
The maximum length [[DTC]] will 
accept is 350, 10 lines of 35 
characters. Each line should be 
separated by a CRLF (carriage 
return - line feed). 
M End of Block - [[settlement]] 
Transaction Details 
:16S:  SETTRAN 
 
  
[[DTCC]] Public (White)

---

## Page 15

MT548 [[IPA]] [[participant]] Confirmation (Output to MT530 Transaction Command) 
Release Notes 15 
RELEASE NOTES 
10/24/2022 Reformatted the document to current on brand template. 
12/18/2015  Added documentation for the [[DTC]] proprietary ISO header message. This is an alternative to the 
SWIFT ISO header message. Added the following three fields to MT548 - [[IPA]] [[participant]] 
Confirmation in Optional Sequence B - [[settlement]] Transaction Details for use with the SWIFT 
header message: Funding Amount, Receive/Deliver Indicator, and Payment Indicator. 
Added new reason code fields to MT548 - [[IPA]] [[participant]] Confirmation in Optional Subsequence 
A2a – Reason. 
09/01/2015 Created MT548 [[IPA]] [[participant]] Confirmation a new funding message for the MMI Finality Through 
Optimization initiative. The message will notify IPAs of the outcome after processing commands.   
 
[[DTCC]] Public (White)

---

## Page 16

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] at: 
DTCSupport@[[DTCC]].com  
or visit us on the web at: 
http://www.[[DTCC]].com/client-center  
[[DTCC]] Public (White)