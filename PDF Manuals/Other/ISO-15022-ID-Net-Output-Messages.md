---
title: "ISO-15022-ID-Net-Output-Messages.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO-15022-ID-Net-Output-Messages.pdf"
pages: 77
size: "696.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO-15022-ID-Net-Output-Messages.pdf

**Original File:** [ISO-15022-ID-Net-Output-Messages.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO-15022-ID-Net-Output-Messages.pdf)  
**Category:** Other  
**Total Pages:** 77  
**File Size:** 696.6 KB  

---

## Page 1

  
 


---

## Page 2

 Overview 
Overview 
Business Transaction: Receive Against Payment Confirmation 
ISO Message Type: MT545 - Receive Against Payment Confirmation 
These messages are sent to the receiving [[participant]] to inform them of the “made” status of free and 
valued transactions.   

---

## Page 3

 Receive Against Payment Confirmation 
Standard ISO Output Message Blocks 
All ISO messages destined for [[DTC]] must contain the following 4 message blocks: 
• [[BASIC]] Header Block - Contains the general information identifying the message and some 
additional control information.  
• Application Header Block - Contains information specific to the application and is required for 
messages exchanged between users or between the system and users.  
• User Header Block - Contains user reference information.  
• Text Block - Contains the actual data being transmitted.  
 
Key: M = Mandatory, O = Optional 
[[BASIC]] Header Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 1 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 2 2 Block Identifier 1: Must contain a value of "1:" 
M 4 1 Message 
Identifier 
F Must contain a value of "F" 
M 5 2 Protocol 
Identifier 
01 Must contain a value of "01" 
M 7 8 Recipient's 
Bank/Firm 
Code 
12345678 Recipient's Bank Identifier Code 
(BIC) or the user's [[participant]] [[ID]] 
(If the recipient is a Group User, 
this [[ID]] must be connected in 
[[DTCC]]'s Group User eligibility 
table) 
M 15 1 Logical X Identifies terminal type 

---

## Page 4

 Receive Against Payment Confirmation 
M/O Tag Length Field 
Description 
Example Description 
Terminal 
M 16 3 Branch Code 123 Identifies branch 
M 19 4 Session 
Number 
0000 A 4 digit value assigned by a 
[[DTCC]] subsidiary. Its [[default]] is 
0000 
M 23 6 Sequence 
Number 
000000 A 6 digit value assigned by a 
[[DTCC]] subsidiary. Its [[default]] is 
000000 
M 29 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
Application Header Block  
 
 
M/O Tag Length Field 
Description 
Example Description 
M 30 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 31 2 Block Identifier 2: Must contain a value of "2:" 
M 33 1 Input/ Output 
Identifier 
O Must contain a value of "O" 
M 34 3 ISO Message 
Type 
545 Must contain a valid 3 digit ISO 
Message Type [[ID]] 
M 37 4 Receipt Time HHMM Format is: HHMM 
The time the message was 
received by the receiving [[DTCC]] 

---

## Page 5

 Receive Against Payment Confirmation 
M/O Tag Length Field 
Description 
Example Description 
subsidiary 
M 41 6 Receipt Date YYMMDD Format is: YYMMDD 
The date the message was 
received by the receiving [[DTCC]] 
subsidiary 
M 47 8 Submitter's 
Bank/Firm 
Code 
12345678 Submitter's Bank Identifier 
Code (BIC) or the Submitter's 
[[participant]] [[ID]] (the same 
number passed to [[DTC]] in the 
ISOINP message) 
M 55 1 Logical 
Terminal 
x Identifies terminal type. "A" for 
Swift messages, "X" for non-
Swift messages 
M 56 3 Branch Code  Always Spaces 
M 59 4 Session 
Number 
1234 A 4 digit value assigned by the 
submitter. The session number 
is set to 0000 if it is not passed 
by a [[DTCC]] subsidiary 
M 63 6 Sequence 
Number 
123456 A 6 digit value assigned by the 
submitter. The sequence 
number is set to 000000 if it is 
not passed by a [[DTCC]] subsidiary 
M 69 6 Transmission 
Date 
YYMMDD Format is: YYMMDD 
The date the message was sent 
from a [[DTCC]] subsidiary to the 
recipient 
M 75 4 Transmission HHMM Format is: HHMM 

---

## Page 6

 Receive Against Payment Confirmation 
M/O Tag Length Field 
Description 
Example Description 
Time The time the message was sent 
from a [[DTCC]] subsidiary to the 
recipient 
M 79 1 Message 
Priority 
N Must contain a value of “N” 
M 80 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
User Header Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 81 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 82 2 Block Identifier 3: Must contain a value of "3:" 
M 84 5 Version 
Number Tag 
{113: Must contain a value of "{113:" 
M 89 4 Version 
Number 
1234 Must contain a value of "0301" 
for [[settlement]] ISO Messages 
Must contain a value of "0701" 
for EuroCCP ISO Messages 
M 93 1 Ending 
Delimiter of 
Version 
Number Tag 
} The character } is used to 
indicate the end of the tag 
M 94 5 Submitter's {108: Must contain a value of "{108:" 

---

## Page 7

 Receive Against Payment Confirmation 
M/O Tag Length Field 
Description 
Example Description 
Reference Key 
Tag 
M 99 16 Submitter's 
Reference Key 
XXXXXXXXX
XXXXXXX 
Unique key created by the 
submitter to identify the 
transaction 
Format: 16x 
M 115 1 Ending 
Delimiter of 
Submitter's 
Reference Key 
Tag 
} The character } is used to 
indicate the end of the tag 
M 116 5 Tag for 
expanded time 
{115: Must contain value of "{115:" 
M 121 11 Expanded 
Time 
HH.MM.SS.
NN 
Format is: HH.MM.SS.NN 
 Since blocks 1 and 2 [[DO]] not 
allow for seconds in the time 
fields, this field gives the time 
down to the second. It contains 
either the time a [[DTCC]] 
subsidiary received the message 
from the submitter or the time 
the message was created by a 
[[DTCC]] subsidiary 
M 132 1 Ending 
Delimiter of 
Expanded 
Time Tag 
} The character } is used to 
indicate the end of the tag 
M 133 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 

---

## Page 8

 Receive Against Payment Confirmation 
Text Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 134 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 135 2 Starting Block 
Identifier 
4: Must contain a value of "4:" 
M 137 2 Carriage 
Return – Line 
Feed (crlf) 
crlf Must contain the carriage 
return - line feed (crlf) 
combination 
M 139 1-27,000 
bytes 
Message Data  The actual contents of the 
message will be inserted here 
M 
 
3 End of 
Message Data 
Carriage 
Return - Line 
Feed (crlf) and 
hyphen 
crlf - Must contain the carriage 
return - line feed combination 
followed by a hyphen 
M  1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
 

---

## Page 9

 Message Data  
Message Data 
Mandatory Sequence A - General Information  
 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: GENL Start of 
Block 
:16R:GENL  
M :20C: :SEME// CDTS 
Tracking 
Number 
:20C::SEME//xxxxxxxxx
xxxxxxx 
[[DTCC]] Generated, used 
to track transaction 
from submission to 
final state 
Format:  16x 
M :23G: NEWM Message 
Function - 
New 
:23G:NEWM This field identifies the 
function of the 
message 
O :98C: :PREP// Transaction 
Update 
Date/Time 
:98C::PREP//yyyymmd
dhhmmss 
Date/time at which 
message was prepared 
 
Repetitive Mandatory Subsequence A1 - Linkages 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: LINK Start of 
Block 
:16R:LINK  
M :20C: :RELA// IMS 
Transaction 
[[ID]] 
:20C::RELA//xxxxxxxxxxx
xxxxx 
IMS generated - used 
to track/update 
transaction from the 
time it is processed in 

---

## Page 10

 Message Data  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
IMS to final state 
Format: 16x 
M :16S: LINK End of 
Block 
:16S:LINK  
M :16R: LINK Start of 
Block 
:16R:LINK  
M :20C: :TRRF// ATP RECAD :20C::TRRF//xxxxxxxxxxx
xxxxx 
ATP generated - used 
to identify, link and 
update transactions in 
ART 
Format: 16x 
M :16S: LINK End of 
Block 
:16S:LINK  
M :16R: LINK Start of 
Block 
:16R:LINK  
M :20C: :COMM// [[ID]] Control 
Number 
:20C::COMM//xxxxxxxxx [[ID]] Control Number 
generated by Omgeo 
Format: 9x 
M :16S: LINK End of 
Block 
:16S:LINK  
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16S GENL End of 
Block 
:16S:GENL  
 
End of Sequence A - General Information 

---

## Page 11

 Message Data  
 
Mandatory Sequence B - Trade Details 
 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: TRADDET Start of Block :16R:TRADDET  
O :98A: :SETT// Original 
[[settlement]] 
Date 
:98A::SETT//yyyymmdd Date at which the 
transaction is 
supposed to be 
settled on 
M :98A: :ESET// Actual 
[[settlement]] 
Date 
:98A::ESET//yyyymmdd Date at which the 
transaction was 
actually settled on 
M :35B: ISIN ISIN :35B:ISIN 
XXXXXXXXXXXX 
Country Code, [[CUSIP]] 
and Check Digit  
ISIN US1234567891 
The literal "ISIN" 
followed by a space 
followed by the 12 
character ISIN. 
Note- [[DTC]] does not 
accept Non U.S. ISIN  
Format: 12x 
 
Optional Subsequence B1 - Financial Instrument Attributes 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: FIA Start of Block :16R:FIA  FIA 

---

## Page 12

 Message Data  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
O :92A: :CUFC: CMO Factor :92A::CUFC//00,0000
00000000 
Tranche Factor 
99,999999999999 
No more than 2 whole 
digits may be present. 
No more than 12 
fractional digits may 
be present. A decimal 
comma is always 
required.  
Format: 15d 
M :16S: FIA End of Block :16S:FIA  FIA 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
O :70E: :SPRO// Narrative - 
[[DTC]] [[DO]] 
Comments 
:70E::SPRO//xxxxxxxx
xxxxxxxxetc. 
The maximum length 
[[DTC]] will accept is 350, 
10 lines of 35 
characters. Each line 
should be separated by 
a CRLF (carriage 
return - line feed) 
Format: 10*35x 
M :16S: TRADDET End of Block :16S:TRADDET  
 
End of Sequence B - Trade Details 
 
 

---

## Page 13

 Message Data  
Mandatory Sequence C - Financial Instrument/Account 
 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: FIAC Start of Block :16R:FIAC FIAC 
M :36B: :ESTT// Quantity 
expressed as 
units 
:36B::ESTT//UNIT/000
0000050000,0 
[[shares]] associated with 
ISIN, must be greater 
than zero 
UNIT/999999999, At 
least 1 whole digit is 
required. No more 
than 9 may be 
present. Fractions are 
not allowed. A 
decimal comma is 
always required 
M :97A: :SAFE// Safekeeper :97A::SAFE//xxxxxxxx [[Broker]] [[DTCC]] 
[[participant]] Number 
Format: 8x 
M :16S: FIAC End of Block :16S:FIAC FIAC 
 
End of Sequence C - Financial Instrument/Account 
 
 
 
 

---

## Page 14

 Message Data  
Mandatory Sequence E - [[settlement]] Details 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: SETDET Start of 
Block 
:16R:SETDET  
O :22F: STCO/DTCY Activity 
Code 
:22F::STCO/DTCYACTV/
xxxx 
Deliver Order value is 
26 
M :22F: SETR/DTCY
REAS 
Reason 
Code 
:22F::SETR/DTCYREAS/
xxxx 
Reason Code of the 
transaction 
 
Repetitive Mandatory Subsequence E1 - [[settlement]] Parties 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: SETPRTY Start of 
Block 
:16R:SETPRTY   
M :95R: :DEAG/ Deliverer :95R::DEAG/DTCYPART
/0000nnnn 
Delivering [[participant]] 
Format: 8x 
O :97A: :SAFE// AIA account 
number 
:97A::SAFE//nnnnnnnn
nnnnnnnnn 
AIA account number 
Format: 35x 
M :16S: SETPRTY End of 
Block 
:16S:SETPRTY   
M :16R: SETPRTY Start of 
Block 
:16R:SETPRTY   
M :95R: :REAG/ Receiver :95R::REAG/DTCYPART
/0000nnnn 
Receiving [[participant]] 
Format: 8x 

---

## Page 15

 Message Data  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
O :97A: :SAFE// BIA account 
number 
:97A::SAFE//nnnnnnnn
nnnnnnnnn 
BIA account number 
Format: 35x 
M :16S: SETPRTY End of 
Block 
:16S:SETPRTY   
M :16R: SETPRTY Start of 
Block 
:16R:SETPRTY   
M :95Q: :PSET Place of 
[[settlement]] 
:95Q::PSET//DTCYUS33 Place of [[settlement]] 
Format: 35x 
M :16S: SETPRTY End of 
Block 
:16S:SETPRTY   
 
Repetitive Mandatory Subsequence E3 - Amounts 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: AMT Start of 
Block 
:16R:AMT  
M :19A: :ESTT// [[settlement]] 
Amount 
:19A::ESTT//USD00000
0000000,00 
Dollar Amount that 
was settled with 
regards to this 
transaction - will 
always be greater than 
zero. 
 
USD9999999999,99 
 
USD followed by at 
least 1 whole digit. 
No more than 10 
whole digits may be 
present. Fractional 
digits are optional, but 
no more than 2 may be 

---

## Page 16

 Message Data  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
present. A decimal 
comma is always 
required 
 
Format: 15d 
M :16S: AMT End of 
Block 
:16S:AMT  
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16S: SETDET End of Block :16S:SETDET  
 
End of Sequence E [[settlement]] Details 
 
Repetitive Optional Sequence F - Other Parties 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: OTHRPRTY Start of Block :16R:OTHRPRTY  
M :95R: :TRAG/ Third Party :95R::TRAG/DTCYPAR
T/0000nnnn 
[[Broker]] Account 
Number 
Format: 8x 
M :16S: OTHRPRTY End of Block :16S:OTHRPRTY  
 
End of Sequence F - Other Parties 
 

---

## Page 17

 Reason/Code Indicators  
Reason/Code Indicators 
PEND Reason Indicators  
  
Spaces  Not 'pended'    
N Pended for receiver's [[collateral]] deficiency 
C Pended for deliverer's [[collateral]] deficiency 
D Pended for receiver's debit deficiency 
A Pended for deliverer's insufficient position 
 
DROP Reason Indicators 
  
Space If [[DO]]-OUT-[[DTC]]-STATUS-IND = 'D', please refer to Drop Code Indicators. Otherwise this was 
not dropped 
I Dropped for receiver's [[collateral]] deficiency  
C Dropped for deliverer's [[collateral]] deficiency 
A Dropped for deliverer insufficient position  
J Dropped when deliverer's [[settlement]] bank unavailable 
N Dropped when receiver's [[settlement]] bank unavailable 
M Dropped when market value is exceeded 
V Dropped when [[collateral]] monitor value is exceeded 
R Dropped when receiver's debit cap limit is reached 
Z Dropped when PEND (recycle) cutoff was taken at the other Depository 
 
DROP Code Indicators 
 
Space Not dropped 
C PEND (recycle) cutoff taken at [[DTC]] 
S No short available for [[CNS]] transactions 
A [[shares]] are not pendable 
T [[collateral]] monitor is not pendable 
D Debit is not pendable 
X Unknown  

---

## Page 18

 Overview 
Overview 
Business Transaction: Deliver Against Payment Confirmation 
ISO Message Type: MT547 - Deliver Against Payment Confirmation 
These messages are sent by the [[DTCC]] inventory and account process to inform the delivering [[participant]] 
of the “made” status of a transaction whether it is for value or free of value.

---

## Page 19

 Deliver Against Payment Confirmation  
Standard ISO Output Message Blocks 
All ISO messages destined for [[DTC]] must contain the following 4 message blocks: 
• [[BASIC]] Header Block - Contains the general information identifying the message and some 
additional control information. 
• Application Header Block - Contains information specific to the application and is required for 
messages exchanged between users or between the system and users. 
• User Header Block - Contains user reference information. 
• Text Block - Contains the actual data being transmitted. 
 
Key: M = Mandatory, O = Optional 
[[BASIC]] Header Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 1 1 Starting Block 
Delimiter 
{ The character {  is used to 
indicate the beginning of a 
block 
M 2 2 Block Identifier 1: Must contain a value of "1:" 
M 4 1 Message 
Identifier 
F Must contain a value of "F" 
M 5 2 Protocol 
Identifier 
01 Must contain a value of "01" 
M 7 8 Recipient's 
Bank/Firm 
Code 
12345678 Recipient's Bank Identifier Code 
(BIC) or the user's [[participant]] [[ID]] 
(If the recipient is a Group User, 
this [[ID]] must be connected in 
[[DTCC]]'s Group User eligibility 
table) 
M 15 1 Logical X Identifies terminal type 

---

## Page 20

 Deliver Against Payment Confirmation  
M/O Tag Length Field 
Description 
Example Description 
Terminal 
M 16 3 Branch Code 123 Identifies branch 
M 19 4 Session 
Number 
0000 A 4 digit value assigned by a 
[[DTCC]] subsidary. Its [[default]] is 
0000 
M 23 6 Sequence 
Number 
000000 A 6 digit value assigned by a 
[[DTCC]] subsidary. Its [[default]] is 
000000 
M 29 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
Application Header Block  
 
 
M/O Tag Length Field 
Description 
Example Description 
M 30 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 31 2 Block Identifier 2: Must contain a value of "2:" 
M 33 1 Input/Output 
Identifier 
0 Must contain a value of "0" 
M 34 3 ISO Message 
Type 
547 Must contain a valid 3 digit ISO 
Message Type [[ID]] 
M 37 4 Receipt Time HHMM Format is: HHMM 
The time the message was 
received by the receiving [[DTCC]] 

---

## Page 21

 Deliver Against Payment Confirmation  
M/O Tag Length Field 
Description 
Example Description 
subsidary 
M 41 6 Receipt Date YYMMDD Format is: YYMMDD 
The date the message was 
received by the receiving [[DTCC]] 
subsidary 
M 47 8 Submitter's 
Bank/Firm 
Code 
12345678 Submitter's Bank Identifier 
Code (BIC) or the Submitter's 
[[participant]] [[ID]] (the same 
number passed to [[DTC]] in the 
ISOINP message) 
M 55 1 Logical 
Terminal 
X Identifies terminal type. "A" for 
Swift messages, "X" for non-
Swift messages 
M 56 3 Branch Code  Always Spaces 
M 59 4 Session 
Number 
1234 A 4 digit value assigned by the 
submitter. The session number 
is set to 0000 if it is not passed 
by a [[DTCC]] subsidary 
M 63 6 Sequence 
Number 
123456 A 6 digit value assigned by the 
submitter. The sequence 
number is set to 000000 if it is 
not passed by a [[DTCC]] subsidary 
M 69 6 Transmission 
Date 
YYMMDD Format is: YYMMDD 
The date the message was sent 
from a [[DTCC]] subsidary to the 
recipient 
M 75 4 Transmission HHMM Format is: HHMM 

---

## Page 22

 Deliver Against Payment Confirmation  
M/O Tag Length Field 
Description 
Example Description 
Time The time the message was sent 
from a [[DTCC]] subsidary to the 
recipient 
M 79 1 Message 
Priority 
N Must contain a value of "N" 
M 80 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
User Header Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 81 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 82 2 Block Identifier 3: Must contain a value of "3:" 
M 84 5 Version 
Number Tag 
{113: Must contain a value of “{   
113:” 
M 89 4 Version 
Number 
1234 Must contain a value of "0301" 
for [[settlement]] ISO Messages 
Must contain a value of "0701" 
for EuroCCP ISO Messages 
M 93 1 Ending 
Delimiter of 
Verion 
Number Tag 
} The character } is used to 
indicate the end of the tag 

---

## Page 23

 Deliver Against Payment Confirmation  
M/O Tag Length Field 
Description 
Example Description 
M 94 5 Submitter's 
Reference Key 
Tag 
{108: Must contain a value of "{108:" 
M 99 16 Submitter's 
Reference Key 
XXXXXXXXX
XXXXX 
Unique key created by the 
submitter to identify the 
transaction. 
Format: 16x 
M 115 1 Ending 
Delimiter of 
Submitter's 
Reference Key 
Tag 
} The character } is used to 
indicate the end of the tag 
M 116 5 Tag for 
expanded time 
{115: Must contain value of "{115:" 
M 121 11 Expanded 
Time 
HH.MM.SS.
NN 
Format is: HH.MM.SS.NN 
Since blocks 1 and 2 [[DO]] not 
allow for seconds in the time 
fields, this field gives the time 
down to the second. It contains 
either the time a [[DTCC]] 
subsidiary received the message 
from the submitter or the time 
the message was created by a 
[[DTCC]] subsidiary 
M 132 1 Ending 
Delimiter of 
Expanded 
Time Tag 
} The character } is used to 
indicate the end of the tag 
M 133 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 

---

## Page 24

 Deliver Against Payment Confirmation  
Text Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 134 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 135 2 Starting Block 
Identifier 
4: Must contain a value of "4:" 
M 137 2 Carriage 
Return - Line 
Feed (crlf) 
crlf Must contain the carriage 
return - line feed (crlf) 
combination 
M 139 1 – 27,000 
Bytes 
Message Data  The actual contents of the 
message will be inserted here 
M  3 End of 
Message Data 
Carriage 
Return - Line 
Feed (crlf) and 
hyphen 
crlf- Must contain the carriage 
return - line feed combination 
followed by a hyphen 
M  1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
 

---

## Page 25

 Message Data  
Message Data 
Mandatory Sequence A - General Information  
 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: GENL Start of 
Block 
:16R:GENL  
M :20C: :SEME// CDTS 
Tracking 
Number 
:20C::SEME//xxxxxxxxxx
xxxxxx 
[[DTCC]] Generated, used 
to track transaction from 
submission to final state 
Format: 16x 
M :23G: NEWM Message 
Function - 
New 
:23G:NEWM This field identifies the 
function of the message 
O :98C: :PREP// Transaction 
Update 
Date/Time 
:98C::PREP//yyyymmdd
hhmmss 
Date/time at which 
message was prepared 
 
Repetitive Mandatory Subsequence A1 - Linkages 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: LINK Start of 
Block 
:16R:LINK  

---

## Page 26

 Message Data  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :20C: :RELA// IMS 
Transaction 
[[ID]] 
:20C::RELA//xxxxxxxxxxxx
xxxx 
IMS generated - used to 
track/update 
transaction from the 
time it is processed in 
IMS to final state 
Format: 16x 
M :16S: LINK End of Block :16S:LINK  
M :16R: LINK Start of 
Block 
:16R:LINK  
M :20C: :TRRF// ATP RECAD :20C::TRRF//xxxxxxxxxxxx
xxxx 
ATP generated - used to 
identify, link and update 
transactions in ART. 
Format: 16x 
M :16S: LINK End of Block :16S:LINK  
M :16R: LINK Start of 
Block 
:16R:LINK  
M :20C: :COMM// [[ID]] Control 
Number 
:20C::COMM//xxxxxxxxx [[ID]] Control Number 
generated by Omgeo 
Format: 9x 
M :16S: LINK End of Block :16S:LINK  
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16S GENL End of 
Block 
:16S:GENL  
 

---

## Page 27

 Message Data  
End of Sequence A - General Information 
 
 
Mandatory Sequence B - Trade Details 
 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: TRADDET Start of Block :16R:TRADDET  
O :98A: :SETT// Original 
[[settlement]] 
Date 
:98A::SETT//yyyymmdd Date at which the 
transaction is 
supposed to be 
settled on 
M :98A: :ESET// Actual 
[[settlement]] 
Date 
:98A::ESET//yyyymmdd Date at which the 
transaction was 
actually settled on 
M :35B: ISIN ISIN :35B:ISIN 
XXXXXXXXXXXX 
Country Code, [[CUSIP]] 
and Check Digit 
ISIN  US1234567891 
The literal "ISIN" 
followed by a space 
followed by the 12 
character ISIN. 
Note- 
[[DTC]] does not accept 
Non U.S. ISIN 
Example-ISIN 
US1234567891. 
Format:12x 
 

---

## Page 28

 Message Data  
Optional Subsequence B1 - Financial Instrument Attributes 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: FIA Start of Block :16R:FIA FIA 
O :92A: :CUFC: CMO Factor :92A::CUFC//00,0000
00000000 
[[DO]] only. Tranche 
Factor. 
99,999999999999 
No more than 2 whole 
digits may be present. 
No more than 12 
fractional digits may 
be present. A decimal 
comma is always 
required.  
Format: 15d 
M :16S: FIA End of Block :16S:FIA FIA  
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
O :70E: :SPRO// Narrative - 
[[DTC]] [[DO]] 
Comments 
:70E::SPRO//xxxxxxxx
xxxxxxxx etc. 
The maximum length 
[[DTC]] will accept is 350, 
10 lines of 35 
characters. Each line 
should be separated by 
a CRLF (carriage 
return - line feed) 
Format: 10*35x 
M :16S: TRADDET End of Block :16S:TRADDET  
 
End of Sequence B - Trade Details 
 

---

## Page 29

 Message Data  
Mandatory Sequence C - Financial Instrument/Account 
 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: FIAC Start of Block :16R:FIAC  
M :36B: :ESTT// Quantity 
expressed as 
units 
:36B::ESTT//UNIT/000
0000050000,0 
[[shares]] associated with 
ISIN, must be greater 
than zero. 
UNIT/999999999, At 
least 1 whole digit is 
required. No more 
than 9 may be 
present. Fractions are 
not allowed. A 
decimal comma is 
always required 
M :97A: :SAFE// Safekeeper :97A::SAFE//xxxxxxxx [[Broker]] [[DTCC]] 
[[participant]] Number 
Format: 8x 
M :16S: FIAC End of Block :16S:FIAC  
 
End of Sequence C - Financial Instrument/Account 
 
Mandatory Sequence E - [[settlement]] Details 
 

---

## Page 30

 Message Data  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: SETDET Start of 
Block 
:16R:SETDET  
O :22F: STCO/DTCY Activity 
Code 
:22F::STCO/DTCYACTV/
xxx 
Deliver Order value is 
26 
M :22F: SETR/DTCY
REAS 
Reason 
Code 
:22F::SETR/DTCYREAS/
Rxxx 
Reason Code of the 
transaction 
 
Repetitive Mandatory Subsequence E1 - [[settlement]] Parties 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: SETPRTY Start of 
Block 
:16R:SETPRTY  
M :95R: :DEAG/ Deliverer :95R::DEAG/DTCYPART
/0000nnnn 
Delivering [[participant]] 
Format: 8x 
O :97A: :SAFE// BIA Account 
Number 
:97A::SAFE//nnnnnnnn
nnnnnnnnn 
BIA Account Number 
Format:35x 
M :16S: SETPRTY End of Block :16S:SETPRTY  
M :16R: SETPRTY Start of 
Block 
:16R:SETPRTY  
M :95R: :REAG/ Receiver  :95R::REAG/DTCYPART
/0000nnnn 
Receiving [[participant]] 
Format:8x 
O :97A: :SAFE// AIA Account 
Number 
:97A::SAFE//nnnnnnnn
nnnnnnnnn 
AIA Account Number 
Format:35x 
M :16S: SETPRTY End of Block :16S:SETPRTY  

---

## Page 31

 Message Data  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: SETPRTY Start of 
Block 
:16R:SETPRTY  
M :95Q: :PSET Place of 
[[settlement]] 
:95Q::PSET//DTCYUS33 Place of [[settlement]] 
Format:35x 
M :16S: SETPRTY End of Block :16S:SETPRTY  
 
Repetitive Mandatory Subsequence E3 - Amounts 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: AMT Start of 
Block 
:16R:AMT  
M :19A: :ESTT// [[settlement]] 
Amount 
:19A::ESTT//USD00000
0000000,00 
Dollar Amount that 
was settled with 
regards to this 
transaction - will 
always be greater than 
zero. 
USD9999999999,99 
 
USD followed by at 
least 1 whole digit. 
No more than 10 
whole digits may be 
present. Fractional 
digits are optional, but 
no more than 2 may be 
present. A decimal 
comma is always 
required 
 
Format: 15d 

---

## Page 32

 Message Data  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16S: AMT End of 
Block 
:16S:AMT  
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16S: SETDET End of Block :16S:SETDET  
 
End of Sequence E [[settlement]] Details 
 
Repetitive Optional Sequence F - Other Parties 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: OTHRPRTY Start of Block :16R:OTHRPRTY  
M :95R: :TRAG/ Third Party :95R::TRAG/DTCYPAR
T/0000nnnn 
[[Broker]] Account 
Number 
Format: 8x 
M :16S: OTHRPRTY End of Block :16S:OTHRPRTY  
 
End of Sequence F - Other Parties 
 

---

## Page 33

 Reason/Code Indicators  
Reason/Code Indicators 
PEND Reason Indicators  
  
Spaces  Not 'pended'    
N Pended for receiver's [[collateral]] deficiency 
C Pended for deliverer's [[collateral]] deficiency 
D Pended for receiver's debit deficiency 
A Pended for deliverer's insufficient position 
 
DROP Reason Indicators 
  
Space If [[DO]]-OUT-[[DTC]]-STATUS-IND = 'D', please refer to Drop Code Indicators. Otherwise this was 
not dropped 
I Dropped for receiver's [[collateral]] deficiency  
C Dropped for deliverer's [[collateral]] deficiency 
A Dropped for deliverer insufficient position  
J Dropped when deliverer's [[settlement]] bank unavailable 
N Dropped when receiver's [[settlement]] bank unavailable 
M Dropped when market value is exceeded 
V Dropped when [[collateral]] monitor value is exceeded 
R Dropped when receiver's debit cap limit is reached 
Z Dropped when PEND (recycle) cutoff was taken at the other Depository 
 
DROP Code Indicators 
 
Space Not dropped 
C PEND (recycle) cutoff taken at [[DTC]] 
S No short available for [[CNS]] transactions 
A [[shares]] are not pendable 
T [[collateral]] monitor is not pendable 
D Debit is not pendable 
X Unknown  

---

## Page 34

 Overview 
Overview 
Business Transaction: [[settlement]] Status (Long Version for Accounting) 
ISO Message Type: MT548 – [[settlement]] Status and Processing Advice 
These are optional messages that are sent to the [[participant]] for “non-made” state changes in IMS/ATP 
occurs. 

---

## Page 35

 [[settlement]] Status (Long Version)  
Standard ISO Output Message Blocks 
All ISO messages destined for [[DTC]] must contain the following 4 message blocks: 
• [[BASIC]] Header Block - Contains the general information identifying the message and some 
additional control information.  
• Application Header Block - Contains information specific to the application and is required for 
messages exchanged between users or between the system and users.  
• User Header Block - Contains user reference information.  
• Text Block - Contains the actual data being transmitted.  
Key: M = Mandatory, O = Optional 
[[BASIC]] Header Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 1 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 2 2 Block Identifier 1: Must contain a value of "1:" 
M 4 1 Message 
Identifier 
F Must contain a value of "F" 
M 5 2 Protocol 
Identifier 
01 Must contain a value of "01" 
M 7 8 Recipient's 
Bank/Firm 
Code 
12345678 Recipient's Bank Identifier Code 
(BIC) or the user's [[participant]] [[ID]] 
(If the recipient is a Group User, 
this [[ID]] must be connected in 
[[DTCC]]'s Group User eligibility 
table) 
M 15 1 Logical 
Terminal 
X Identifies terminal type 

---

## Page 36

 [[settlement]] Status (Long Version)  
M/O Tag Length Field 
Description 
Example Description 
M 16 3 Branch Code 123 Identifies branch 
M 19 4 Session 
Number 
0000 A 4 digit value assigned by a 
[[DTCC]] subsidiary 
Its [[default]] is 0000 
M 23 6 Sequence 
Number 
000000 A 6 digit value assigned by a 
[[DTCC]] subsidiary 
Its [[default]] is 000000 
M 29 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
Application Header Block  
 
 
M/O Tag Length Field 
Description 
Example Description 
M 30 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 31 2 Block Identifier 2: Must contain a value of "2:" 
M 33 1 Input/Output 
Identifier 
0 Must contain a value of "0" 
M 34 3 ISO Message 
Type 
548 Must contain a valid 3 digit ISO 
Message Type [[ID]] 

---

## Page 37

 [[settlement]] Status (Long Version)  
M/O Tag Length Field 
Description 
Example Description 
M 37 4 Receipt Time HHMM Format is: HHMM 
The time the message was 
received by the receiving [[DTCC]] 
subsidiary 
M 41 6 Receipt Date YYMMDD Format is: YYMMDD 
The date the message was 
received by the receiving [[DTCC]] 
subsidiary 
M 47 8 Submitter's 
Bank/Firm 
Code 
12345678 Submitter's Bank Identifier 
Code (BIC) or the Submitter's 
[[participant]] [[ID]] (the same 
number passed to [[DTC]] in the 
ISOINP message) 
M 55 1 Logical 
Terminal 
X Identifies terminal type. "A" for 
Swift messages, "X" for non-
Swift messages 
M 56 3 Branch Code  Always Spaces 
M 59 4 Session 
Number 
1234 A 4 digit value assigned by the 
submitter 
The session number is set to 
0000 if it is not passed by a 
[[DTCC]] subsidiary 
M 63 6 Sequence 
Number 
123456 A 6 digit value assigned by the 
submitter 
The sequence number is set to 
000000 if it is not passed by a 
[[DTCC]] subsidiary 

---

## Page 38

 [[settlement]] Status (Long Version)  
M/O Tag Length Field 
Description 
Example Description 
M 69 6 Transmission 
Date 
YYMMDD Format is: YYMMDD 
The date the message was sent 
from a [[DTCC]] subsidiary to the 
recipient 
M 75 4 Transmission 
Time 
HHMM Format is: HHMM 
The time the message was sent 
from a [[DTCC]] subsidiary to the 
recipient 
M 79 1 Message 
Priority 
N Must contain a value of "N" 
M 80 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
User Header Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 81 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 82 2 Block Identifier 3: Must contain a value of "3:" 
M 84 5 Version 
Number Tag 
{113: Must contain a value of "{113:" 

---

## Page 39

 [[settlement]] Status (Long Version)  
M/O Tag Length Field 
Description 
Example Description 
M 89 4 Version 
Number 
1234 Must contain a value of "0301" 
for [[settlement]] ISO Messages 
Must contain a value of "0701" 
for EuroCCP ISO Messages 
M 93 1 Ending 
Delimiter of 
Version 
Number Tag 
} The character } is used to 
indicate the end of the tag 
M 94 5 Submitter's 
Reference Key 
Tag 
{108: Must contain a value of "{108:" 
M 99 16 Submitter's 
Reference Key 
XXXXXXXXX
XXXXXXX 
Unique key created by the 
submitter to identify the 
transaction 
Format: 16x 
M 115 1 Ending 
Delimiter of 
Submitter's 
Reference Key 
Tag 
} The character } is used to 
indicate the end of the tag 
M 116 5 Tag for 
expanded time 
{115: Must contain value of "{115:" 

---

## Page 40

 [[settlement]] Status (Long Version)  
M/O Tag Length Field 
Description 
Example Description 
M 121 11 Expanded 
Time 
HH.MM.SS.
NN 
Format is: HH.MM.SS.NN 
Since blocks 1 and 2 [[DO]] not 
allow for seconds in the time 
fields, this field gives the time 
down to the second 
 It contains either the time a 
[[DTCC]] subsidiary received the 
message from the submitter or 
the time the message was 
created by a [[DTCC]] subsidiary 
M 132 1 Ending 
Delimiter of 
Expanded 
Time Tag 
} The character } is used to 
indicate the end of the tag 
M 133 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
Text Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 134 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 135 2 Starting Block 
Identifier 
4: Must contain a value of “14:” 

---

## Page 41

 [[settlement]] Status (Long Version)  
M/O Tag Length Field 
Description 
Example Description 
M 137 2 Carriage 
Return - Line 
Feed (crlf) 
crlf Must contain the carriage 
return - line feed (crlf) 
combination 
M 139 1-27,000 
bytes 
Message Data  The actual contents of the 
message will be inserted here 
M 
 
3 End of 
Message Data 
Carriage 
Return -Line 
Feed (crlf) and 
hyphen 
crlf- Must contain the carriage 
return - line feed combination 
followed by a hyphen 
M  1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
 

---

## Page 42

 Reason/Code Indicators  
Message Data 
Mandatory Sequence A - General Information  
 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: GENL Start of 
Block 
:16R:GENL  
M :20C: :SEME// CDTS 
Tracking 
Number 
:20C::SEME//xxxxxxxxx
xxxxxxx 
[[DTCC]] generated, used 
to track transaction 
from submission to 
final state 
Format: 16x 
M :23G: INST Message 
Function - 
INST 
:23G:INST This field identifies the 
function of the 
message 
M :98C: :PREP// Transaction 
Update 
Date/Time 
:98C::PREP//yyyymmd
dhhmmss 
Date/time at which 
message was prepared 
 
Repetitive Mandatory Subsequence A1 - Linkages 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: LINK Start of 
Block 
:16R:LINK  

---

## Page 43

 Reason/Code Indicators  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :20C: :RELA// IMS 
Transaction 
[[ID]] 
:20C::RELA//xxxxxxxxxxx
xxxxx 
IMS generated - used 
to track/update 
transaction from the 
time it is processed in 
IMS to final state 
Format: 16x 
M :16S: LINK End of 
Block 
:16S:LINK  
M :16R: LINK Start of 
Block 
:16R:LINK  
M :20C: :TRRF// ATP RECAD :20C::TRRF//xxxxxxxxxxx
xxxxx 
ATP generated - used 
to identify, link and 
update transactions in 
ART 
Format: 16x 
M :16S: LINK End of 
Block 
:16S:LINK  
M :16R: LINK Start of 
Block 
:16R:LINK  
M :20C: :COMM// [[ID]] Control 
Number 
:20C::COMM//xxxxxxxxx [[ID]] Control Number 
generated by Omgeo 
Format: 9x 
M :16S: LINK End of 
Block 
:16S:LINK  
 
Repetitive Mandatory Subsequence A2 - Status 

---

## Page 44

 Reason/Code Indicators  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: STAT Start of 
Block 
:16R:STAT  
M :25D: SETT/ Status 
Code 
:25D:SETT/DTCY/AUTH, 
SUBA, etc. 
IMS or ATP State, states 
are assigned as 
transaction is processed 
through IMS and ATP 
Format: 4x 
 
Repetitive Optional Subsequence A2a - Reason     
  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: REAS Start of Block :16R:REAS  
M :24B: :REJT/ PACK, CAND, 
PEND, REJT, or 
PENF 
:24B::REJT/DTCY/xxxx Refer to Processing 
Status tab 
Format: 4x 
O :70D: :REAS// Error message :70D::REAS//xxxxxxxx
xxxxxxxx etc. 
Provides explanation 
for the reject, pend, 
drop, or cancel 
Format: 16x 
M :16S: REAS End of Block :16S::REAS  
 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16S: STAT End of Block :16S:STAT  

---

## Page 45

 Reason/Code Indicators  
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16S: GENL End of Block :16S:GENL  
 
End of Sequence A - General Information      
      
 
Optional Sequence B - [[settlement]] Transaction Details    
   
 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: SETTRAN Start of Block :16R:SETTRAN  
M :35B: ISIN ISIN :35B:ISIN 
XXXXXXXXXXXX 
Country Code, [[CUSIP]] 
and Check Digit 
ISIN US1234567891 
The literal "ISIN" 
followed by a space 
followed by the 12 
character ISIN.  
Note - [[DTC]] does not 
accept Non U.S. ISIN 
 
Format:12x 
M :36B: :SETT// Quantity 
expressed as 
units 
:36B::SETT//UNIT/000
0000050000,0 
[[shares]] associated with 
ISIN, must be greater 
than zero 
UNIT/999999999, At 

---

## Page 46

 Reason/Code Indicators  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
least 1 whole digit is 
required. No more 
than 9 may be present. 
Fractions are not 
allowed. A decimal 
comma is always 
required 
Format: 15d 
M :19A: :SETT// [[settlement]] 
Amount 
:19A::SETT//USD00000
0000000,00 
Dollar Amount 
associated with ISIN 
Format: 15d 
M :97A: :SAFE// Safekeeper :97A::SAFE//xxxxxxxxx
xxxxxxxx etc. 
Identifies account 
where financial 
instruments are 
maintained 
Format: 35x 
M :22F: :SETR/ Reason Code :22F::SETR/DTCYREAS/
xxxx 
[[DTC]] Reason Code, 
identifies purpose of 
PO 
Format: 4x 
M :22H: :REDE/ Receiver/ 
Deliverer 
Indicator 
:22H::REDE//xxxx It is mandatory to 
specify a delivering 
agent:DELI 
Format: 4 
M :22H: :PAYM/ Payment 
Indicator 
:22H::PAYM//xxxx APMT for valued 
transactions or FREE 
for free transactions 
Format: 4 
O :22F: :STCO/ Internal :22F::STCO/DTCYISRC/ Identifies the input 
media for the 

---

## Page 47

 Reason/Code Indicators  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
Source Code xxxx transaction 
Format: 4x 
O :22F: :STCO/ Transaction 
Type 
:22F::STCO/DTCYTXNT/
xxxx 
IMS Transaction type, 
OTHR 
Format: 4x 
O :22F: :STCO/ Activity Code :22F::STCO/DTCYACTV
/xxxx 
SPO is 78, PPO is 82  
Format: 4x 
O :98A: :EXSE// Actual 
[[settlement]] 
Date 
:98A::EXSE// 
yyyymmdd 
Date at which the 
transaction was 
actually settled on 
M :98A: :SETT// Original 
[[settlement]] 
Date 
:98A::SETT// 
yyyymmdd 
Date at which the 
transaction is suppose 
to be settled on 
O :70E: :SPRO// Narrative - 
[[DTC]] 
Comments 
:70E::SPRO//xxxxxxxxx
xxxxxxx etc. 
Provides additional 
[[settlement]] processing 
information 
The maximum length 
[[DTC]] will accept is 350, 
10 lines of 35 
characters.  Each 
lineshould be 
separated by a CRLF 
(carriage return - line 
feed) 
  
Format: 10*35x 
 
Repetitive Optional Subsequence B1 - [[settlement]] Parties     

---

## Page 48

 Reason/Code Indicators  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: SETPRTY Start of 
Block 
:16R:SETPRTY  
M :95R: :DEAG/[[DTC]]
YPART 
Delivering 
[[participant]] 
:95R::DEAG/DTCYPART/
0000nnnn 
Delivering [[participant]] 
Format: 8x 
O :97A: :SAFE// BIA or AIA 
Account 
Number 
:97A::SAFE//nnnnnnnnn
nnnnnnnn 
BIA Account number 
will be displayed if the 
deliverer number = 919, 
otherwise the AIA 
Account number will be 
displayed 
Format: 35x 
M :16S: SETPRTY End of Block :16S:SETPRTY  
M :16R: SETPRTY Start of 
Block 
:16R:SETPRTY  
M :95R: :REAG/DTCY
PART 
Receiving 
[[participant]] 
:95R::REAG/DTCYPART/
0000nnnn 
Receiving [[participant]] 
Format: 8x 
O :97A: :SAFE// BIA or AIA 
Account 
Number 
:97A::SAFE//nnnnnnnnn
nnnnnnnn 
BIA Account number 
will be displayed if the 
receiver number = 719, 
otherwise the AIA 
Account number will be 
displayed 
Format: 8x 
M :16S: SETPRTY End of Block :16S:SETPRTY  
M :16R: SETPRTY Start of 
Block 
:16R:SETPRTY  
M :95P: :PSET// Place of :95P::PSET//DTCYUS33 Place of [[settlement]] 

---

## Page 49

 Reason/Code Indicators  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
[[settlement]] 
M :16S: SETPRTY End of Block :16S:SETPRTY  
M :16R: SETPRTY Start of 
Block 
:16R:SETPRTY  
M :95R: :DEI1/DTCY
PART 
Deliverer's 
[[intermediary]] 
:95R::DEI1/DTCYPART/0
000nnnn 
Depository Third Party 
field will be displayed if 
the deliverer number = 
919 
Format: 8x 
M :16S: SETPRTY End of Block :16S:SETPRTY  
 
OR 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: SETPRTY Start of Block :16R:SETPRTY  
M :95R: :REI1/DTCY
PART 
Receiver's 
[[intermediary]] 
:95R::REI1/DTCYPART
/0000nnnn 
Depository Third Party 
field will be displayed if 
the receiver number = 
719 
Format: 8x 
M :16S: SETPRTY End of Block :16S:SETPRTY  
 
End of Sequence B1 [[settlement]] Parties       
            
     

---

## Page 50

 Reason/Code Indicators  
Reason/Code Indicators 
PEND Reason Indicators  
  
Spaces  Not 'pended'    
N Pended for receiver's [[collateral]] deficiency 
C Pended for deliverer's [[collateral]] deficiency 
D Pended for receiver's debit deficiency 
A Pended for deliverer's insufficient position 
 
DROP Reason Indicators 
  
Space If [[DO]]-OUT-[[DTC]]-STATUS-IND = 'D', please refer to Drop Code Indicators. Otherwise this was 
not dropped 
I Dropped for receiver's [[collateral]] deficiency  
C Dropped for deliverer's [[collateral]] deficiency 
A Dropped for deliverer insufficient position  
J Dropped when deliverer's [[settlement]] bank unavailable 
N Dropped when receiver's [[settlement]] bank unavailable 
M Dropped when market value is exceeded 
V Dropped when [[collateral]] monitor value is exceeded 
R Dropped when receiver's debit cap limit is reached 
Z Dropped when PEND (recycle) cutoff was taken at the other Depository 
 
DROP Code Indicators 
 
Space Not dropped 
C PEND (recycle) cutoff taken at [[DTC]] 
S No short available for [[CNS]] transactions 
A [[shares]] are not pendable 
T [[collateral]] monitor is not pendable 
D Debit is not pendable 
X Unknown  

---

## Page 51

 Overview 
Overview 
Business Transaction: [[settlement]] Status (Short Version) 
ISO Message Type: MT548 – [[settlement]] Status and Processing Advice 
These are optional messages that are sent to the [[participant]] for “non-made” state changes in IMS/ATP 
occurs. 

---

## Page 52

 [[settlement]] Status (Short Version)  
Standard ISO Output Message Blocks 
All ISO messages destined for [[DTC]] must contain the following 4 message blocks : 
• [[BASIC]] Header Block - Contains the general information identifying the message and some 
additional control information.  
• Application Header Block - Contains information specific to the application and is required for 
messages exchanged between users or between the system and users.  
• User Header Block - Contains user reference information.  
• Text Block - Contains the actual data being transmitted.  
Key: M = Mandatory, O = Optional 
[[BASIC]] Header Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 1 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 2 2 Block Identifier 1: Must contain a value of "1:" 
M 4 1 Message 
Identifier 
F Must contain a value of "F" 
M 5 2 Protocol 
Identifier 
01 Must contain a value of "01" 
M 7 8 Recipient's 
Bank/Firm 
Code 
12345678 Recipient's Bank Identifier Code 
(BIC) or the user's [[participant]] [[ID]] 
(If the recipient is a Group User, 
this [[ID]] must be connected in 
[[DTCC]]'s Group User eligibility 
table) 
M 15 1 Logical 
Terminal 
X Identifies terminal type 

---

## Page 53

 [[settlement]] Status (Short Version)  
M/O Tag Length Field 
Description 
Example Description 
M 16 3 Branch Code 123 Identifies branch 
M 19 4 Session 
Number 
0000 A 4 digit value assigned by a 
[[DTCC]] subsidiary 
Its [[default]] is 0000 
M 23 6 Sequence 
Number 
000000 A 6 digit value assigned by a 
[[DTCC]] subsidiary 
 Its [[default]] is 000000 
M 29 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
Application Header Block  
 
 
M/O Tag Length Field 
Description 
Example Description 
M 30 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 31 2 Block Identifier 2: Must contain a value of "2:" 
M 33 1 Input/Output 
Identifier 
0 Must contain a value of "0" 
M 34 3 ISO Message 
Type 
548 Must contain a valid 3 digit ISO 
Message Type [[ID]] 
M 37 4 Receipt Time HHMM Format is: HHMM 
The time the message was 
received by the receiving [[DTCC]] 

---

## Page 54

 [[settlement]] Status (Short Version)  
M/O Tag Length Field 
Description 
Example Description 
subsidiary 
M 41 6 Receipt Date YYMMDD Format is: YYMMDD 
The date the message was 
received by the receiving [[DTCC]] 
subsidiary 
M 47 8 Submitter's 
Bank/Firm 
Code 
12345678 Submitter's Bank Identifier 
Code (BIC) or the Submitter's 
[[participant]] [[ID]] (the same 
number passed to [[DTC]] in the 
ISOINP message) 
M 55 1 Logical 
Terminal 
X Identifies terminal type. "A" for 
Swift messages, "X" for non-
Swift messages 
M 56 3 Branch Code  Always Spaces 
M 59 4 Session 
Number 
1234 A 4 digit value assigned by the 
submitter 
The session number is set to 
0000 if it is not passed by a 
[[DTCC]] subsidiary 
M 63 6 Sequence 
Number 
123456 A 6 digit value assigned by the 
submitter 
The sequence number is set to 
000000 if it is not passed by a 
[[DTCC]] subsidiary 

---

## Page 55

 [[settlement]] Status (Short Version)  
M/O Tag Length Field 
Description 
Example Description 
M 69 6 Transmission 
Date 
YYMMDD Format is: YYMMDD 
The date the message was sent 
from a [[DTCC]] subsidiary to the 
recipient 
M 75 4 Transmission 
Time 
HHMM Format is: HHMM 
The time the message was sent 
from a [[DTCC]] subsidiary to the 
recipient 
M 79 1 Message 
Priority 
N Must contain a value of "N" 
M 80 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
User Header Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 81 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 82 2 Block Identifier 3: Must contain a value of "3:" 
M 84 5 Version 
Number Tag 
{113: Must contain a value of "{113:" 

---

## Page 56

 [[settlement]] Status (Short Version)  
M/O Tag Length Field 
Description 
Example Description 
M 89 4 Version 
Number 
1234 Must contain a value of "0301" 
for [[settlement]] ISO Messages 
Must contain a value of "0701" 
for EuroCCP ISO Messages 
M 93 1 Ending 
Delimiter of 
Version 
Number Tag 
} The character } is used to 
indicate the end of the tag 
M 94 5 Submitter's 
Reference Key 
Tag 
{108: Must contain a value of "{108:" 
M 99 16 Submitter's 
Reference Key 
XXXXXXXXX
XXXXXXX 
Unique key created by the 
submitter to identify the 
transaction 
Format: 16x 
M 115 1 Ending 
Delimiter of 
Submitter's 
Reference Key 
Tag 
} The character } is used to 
indicate the end of the tag 
M 116 5 Tag for 
expanded time 
{115: Must contain value of "{115:" 

---

## Page 57

 [[settlement]] Status (Short Version)  
M/O Tag Length Field 
Description 
Example Description 
M 121 11 Expanded 
Time 
HH.MM.SS.
NN 
Format is: HH.MM.SS.NN 
Since blocks 1 and 2 [[DO]] not 
allow for seconds in the time 
fields, this field gives the time 
down to the second. It contains 
either the time a [[DTCC]] 
subsidary received the message 
from the submitter or the time 
the message was created by a 
[[DTCC]] subsidiary 
M 132 1 Ending 
Delimiter of 
Expanded 
Time Tag 
} The character } is used to 
indicate the end of the tag 
M 133 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
Text Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 134 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 135 2 Starting Block 
Identifier 
4: Must contain a value of “4:” 
M 137 2 Carriage 
Return - Line 
Feed (crlf) 
crlf Must contain the carriage 
return - line feed (crlf) 
combination 

---

## Page 58

 [[settlement]] Status (Short Version)  
M/O Tag Length Field 
Description 
Example Description 
M 139 1-27,000 
bytes 
Message Data  The actual contents of the 
message will be inserted here 
M 
 
3 End of 
Message Data 
Carriage 
Return -Line 
Feed (crlf) and 
hyphen 
crlf- Must contain the carriage 
return - line feed combination 
followed by a hyphen 
M  1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
 

---

## Page 59

 Message Data  
Message Data 
Mandatory Sequence A - General Information  
 
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: GENL Start of 
Block 
:16R:GENL  
M :20C: SEME CDTS 
Tracking 
Number 
:20C::SEME//xxxxxxxxx
xxxxxxx 
[[DTCC]] Generated, used 
to track transaction 
from submission to 
final state 
Format:16x 
M :23G: INST Message 
Function - 
INST 
:23G:INST This field identifies the 
function of the 
message 
M :98C: :PREP// Transaction 
Update 
Date/Time 
:98C::PREP//yyyymmd
dhhmmss 
Date/time at which 
message was prepared 
 
Repetitive Mandatory Subsequence A1 - Linkages 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: LINK Start of 
Block 
:16R:LINK  

---

## Page 60

 Message Data  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :20C: :RELA// IMS 
Transaction 
[[ID]] 
:20C::RELA//xxxxxxxxxxx
xxxxx 
IMS generated - used 
to track/update 
transaction from the 
time it is processed in 
IMS to final state 
Format: 16x 
M :16S: LINK End of 
Block 
:16S:LINK  
M :16R: LINK Start of 
Block 
:16R:LINK  
M :20C: :TRRF// ATP RECAD :20C::TRRF//xxxxxxxxxxx
xxxxx 
ATP generated - used 
to identify, link and 
update transactions in 
ART 
Format: 16x 
M :16S: LINK End of 
Block 
:16S:LINK  
M :16R: LINK Start of 
Block 
:16R:LINK  
M :20C: :COMM// [[ID]] Control 
Number 
:20C::COMM//xxxxxxxxx [[ID]] Control Number 
generated by Omgeo 
Format: 9x 
M :16S: LINK End of 
Block 
:16S:LINK  
 
 
 
 
 

---

## Page 61

 Message Data  
 
Repetitive Mandatory Subsequence A2 - Status 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: STAT Start of 
Block 
:16R:STAT  
M :25D: SETT/ Status 
Code 
:25D:SETT/DTCY/AUTH, 
SUBA, etc. 
IMS or ATP State, states 
are assigned as 
transaction is processed 
through IMS and ATP 
Format: 4x 
 
Repetitive Optional Subsequence A2a - Reason 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16R: REAS Start of Block :16R:REAS  
M :24B: Status PACK, CAND, 
PEND, REJT, 
or PENF 
:24B::REJT/DTCY/xxxx Refer to Processing 
Status tab 
Format: 4x 
O :70D: REAS Reject Error 
message 
:70D::REAS//xxxxxxxxxxxx
xxxx etc. 
Provides explanation for 
the reject, pend, drop, or 
cancel 
Format: 16x 
M :16S: REAS End of Block :16S::REAS  
 
 
 

---

## Page 62

 Message Data  
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16S: STAT End of Block :16S::STAT  
 
M/O Tag Qualifier(s) Field 
Description 
Example Description 
M :16S: GENL End of Block :16S:GENL  
 
End of Sequence A - General Information       
 

---

## Page 63

 Reason/Code Indicators  
Reason/Code Indicators 
PEND Reason Indicators  
  
Spaces  Not 'pended'    
N Pended for receiver's [[collateral]] deficiency 
C Pended for deliverer's [[collateral]] deficiency 
D Pended for receiver's debit deficiency 
A Pended for deliverer's insufficient position 
 
DROP Reason Indicators 
  
Space If [[DO]]-OUT-[[DTC]]-STATUS-IND = 'D', please refer to Drop Code Indicators. Otherwise this was 
not dropped 
I Dropped for receiver's [[collateral]] deficiency  
C Dropped for deliverer's [[collateral]] deficiency 
A Dropped for deliverer insufficient position  
J Dropped when deliverer's [[settlement]] bank unavailable 
N Dropped when receiver's [[settlement]] bank unavailable 
M Dropped when market value is exceeded 
V Dropped when [[collateral]] monitor value is exceeded 
R Dropped when receiver's debit cap limit is reached 
Z Dropped when PEND (recycle) cutoff was taken at the other Depository 
 
DROP Code Indicators 
 
Space Not dropped 
C PEND (recycle) cutoff taken at [[DTC]] 
S No short available for [[CNS]] transactions 
A [[shares]] are not pendable 
T [[collateral]] monitor is not pendable 
D Debit is not pendable 
X Unknown  

---

## Page 64

  Overview     
Overview 
Business Transaction: Intra-day Continuous Net [[settlement]] Message on [[settlement]] Day  
ISO Message Type: MT570 - Intra-day Continuous Net [[settlement]] 
This ISO15022 message will be sent to participants when their [[CNS]] position changes due to new settling 
trades or new miscellaneous activity in the day cycle. 
• Sequence A will contain general information about the message being sent 
• Sequence B will contain information about the Participants [[CNS]] position 
• Sequence C will contain information about new trades settled in the day cycle 
• Sequence D will contain information about miscellaneous activity taking place during the day 
cycle 
Note (1): A [[participant]] will never receive Sequence C and Sequence D information together.  
Note (2): Normally each message will contain either one (1) Sequence C or one (1) Sequence (D) 
Note (3): The ISO Field tag is defined as a unique string of characters identifying the meaning and format 
of the data item. Field tags with multiple formats such as 98 (format can be for date or date & time) or 
95 (format for party may be expressed in BIC, local market identifiers including a data source scheme, or 
free format such as name & address) are expressed on the www.iso15022.org website as 98a and 95a 
respectively. The field tags are expressed in the message by the actual format used.  
For example: 98a Date/Time is either expressed as 98A (qualifier) (date)     
 or 98C (qualifier) (date) (time) 

---

## Page 65

  Intraday Continuous Net [[settlement]]     
Standard ISO Output Message Blocks 
All ISO messages destined for [[DTC]] must contain the following 4 message blocks: 
• [[BASIC]] Header Block - Contains the general information identifying the message and some 
additional control information.  
• Application Header Block - Contains information specific to the application and is required for 
messages exchanged between users or between the system and users.  
• User Header Block - Contains user reference information.  
• Text Block - Contains the actual data being transmitted.  
 
Key: M = Mandatory, O = Optional 
[[BASIC]] Header Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 1 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 2 2 Block Identifier 1: Must contain a value of "1:" 
M 4 1 Message 
Identifier 
F Must contain a value of "F" 
M 5 2 Protocol 
Identifier 
01 Must contain a value of "01" 
M 7 8 Recipient's 
Bank/Firm 
Code 
12345678 Recipient's Bank Identifier Code 
(BIC) or the user's [[participant]] [[ID]] 
(If the recipient is a Group User, 
this [[ID]] must be connected in 
[[DTCC]]'s Group User eligibility 
table) 
M 15 1 Logical 
Terminal 
X Identifies terminal type 

---

## Page 66

  Intraday Continuous Net [[settlement]]     
M/O Tag Length Field 
Description 
Example Description 
M 16 3 Branch Code 123 Identifies branch 
M 19 4 Session 
Number 
0000 A 4 digit value assigned by a 
[[DTCC]] subsidiary. Its [[default]] is 
0000 
M 23 6 Sequence 
Number 
000000 A 6 digit value assigned by a 
[[DTCC]] subsidiary. Its [[default]] is 
000000 
M 29 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
Application Header Block  
 
 
M/O Tag Length Field 
Description 
Example Description 
M 30 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 31 2 Block Identifier 2: Must contain a value of "2:" 
M 33 1 Input/ Output 
Identifier 
O Must contain a value of "O" 
M 34 3 ISO Message 
Type 
545 Must contain a valid 3 digit ISO 
Message Type [[ID]] 
M 37 4 Receipt Time HHMM Format is: HHMM 
The time the message was 
received by the receiving [[DTCC]] 
subsidiary 

---

## Page 67

  Intraday Continuous Net [[settlement]]     
M/O Tag Length Field 
Description 
Example Description 
M 41 6 Receipt Date YYMMDD Format is: YYMMDD 
The date the message was 
received by the receiving [[DTCC]] 
subsidiary 
M 47 8 Submitter's 
Bank/Firm 
Code 
12345678 Submitter's Bank Identifier 
Code (BIC) or the Submitter's 
[[participant]] [[ID]] (the same 
number passed to [[DTC]] in the 
ISOINP message) 
M 55 1 Logical 
Terminal 
x Identifies terminal type. "A" for 
Swift messages, "X" for non-
Swift messages 
M 56 3 Branch Code  Always Spaces 
M 59 4 Session 
Number 
1234 A 4 digit value assigned by the 
submitter. The session number 
is set to 0000 if it is not passed 
by a [[DTCC]] subsidiary 
M 63 6 Sequence 
Number 
123456 A 6 digit value assigned by the 
submitter. The sequence 
number is set to 000000 if it is 
not passed by a [[DTCC]] subsidiary 
M 69 6 Transmission 
Date 
YYMMDD Format is: YYMMDD 
The date the message was sent 
from a [[DTCC]] subsidiary to the 
recipient 
M 75 4 Transmission 
Time 
HHMM Format is: HHMM 
The time the message was sent 
from a [[DTCC]] subsidiary to the 
recipient 

---

## Page 68

  Intraday Continuous Net [[settlement]]     
M/O Tag Length Field 
Description 
Example Description 
M 79 1 Message 
Priority 
N Must contain a value of “N” 
M 80 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
User Header Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 81 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 82 2 Block Identifier 3: Must contain a value of "3:" 
M 84 5 Version 
Number Tag 
{113: Must contain a value of "{113:" 
M 89 4 Version 
Number 
1234 Must contain a value of "0301" 
for [[settlement]] ISO Messages 
Must contain a value of "0701" 
for EuroCCP ISO Messages 
M 93 1 Ending 
Delimiter of 
Version 
Number Tag 
} The character } is used to 
indicate the end of the tag 
M 94 5 Submitter's 
Reference Key 
Tag 
{108: Must contain a value of "{108:" 

---

## Page 69

  Intraday Continuous Net [[settlement]]     
M/O Tag Length Field 
Description 
Example Description 
M 99 16 Submitter's 
Reference Key 
XXXXXXXXX
XXXXXXX 
Unique key created by the 
submitter to identify the 
transaction 
Format: 16x 
M 115 1 Ending 
Delimiter of 
Submitter's 
Reference Key 
Tag 
} The character } is used to 
indicate the end of the tag 
M 116 5 Tag for 
expanded time 
{115: Must contain value of "{115:" 
M 121 11 Expanded 
Time 
HH.MM.SS.
NN 
Format is: HH.MM.SS.NN 
 Since blocks 1 and 2 [[DO]] not 
allow for seconds in the time 
fields, this field gives the time 
down to the second. It contains 
either the time a [[DTCC]] 
subsidiary received the message 
from the submitter or the time 
the message was created by a 
[[DTCC]] subsidiary 
M 132 1 Ending 
Delimiter of 
Expanded 
Time Tag 
} The character } is used to 
indicate the end of the tag 
M 133 1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 
 
 
 

---

## Page 70

  Intraday Continuous Net [[settlement]]     
Text Block 
 
 
M/O Tag Length Field 
Description 
Example Description 
M 134 1 Starting Block 
Delimiter 
{ The character { is used to 
indicate the beginning of a 
block 
M 135 2 Starting Block 
Identifier 
4: Must contain a value of "4:" 
M 137 2 Carriage 
Return – Line 
Feed (crlf) 
crlf Must contain the carriage 
return - line feed (crlf) 
combination 
M 139 1-27,000 
bytes 
Message Data  The actual contents of the 
message will be inserted here 
M 
 
3 End of 
Message Data 
Carriage 
Return - Line 
Feed (crlf) and 
hyphen 
crlf - Must contain the carriage 
return - line feed combination 
followed by a hyphen 
M  1 Ending Block 
Delimiter 
} The character } is used to 
indicate the end of a block 
 

---

## Page 71

   Message Data      
 
MT 570 Intra-day Continuous Net [[settlement]] Message on [[settlement]] Day  
 
M/O Tag Field 
Description 
Data Field Format Example 
M 16R Start of Block GENL 16R:GENL 
M 20C Senders 
Reference 
:4!c//16x 20C:SEME//16x 
Message Control number 
M 23G Function of 
the message 
4!c[/4!c] 23G:NEWM 
O 98a Preparation  
Date/Time 
:4!c//8!n6!n :98C:PREP//yyyymmddhhmmss 
[[CNS]] will be using the 98C [[Option]] of 
this tag for this data item 
M 16S End of Block 16S 16S: GENL 
M 16R Start of Block POSINFO 16R:POSINFO 
M 95a [[participant]] 
Number 
 :4!c/4!c[4c]/34z   95R: CLBR/DTCY/<partnum> 
[[CNS]] will be using the 95R [[Option]] of 
this tag for this product 
M 22F [[CNS]] Sub 
account 
:4!c/[4!c[4c]]/4!c 22F: ACCL/DTCY/1 digit alpha 
 *[[DTCC]] values are at the end of 
this document 
* DTCY Qualifier overrides 
requirement for 4 character data 

---

## Page 72

   Message Data      
M/O Tag Field 
Description 
Data Field Format Example 
M 35B Identification 
of the 
Financial 
Instrument 
[ISIN1!e12!c] 
[4*35x] 
35B:<country><[[CUSIP]]><check> 
where <country> is stored in 
Country Code field,  
<[[CUSIP]]> is stored in [[CUSIP]] field, and 
<check> is stored in Check Digit 
field in Transaction Table. 
M 93B First Opening 
position  
:4!c/[4!c[4c]]/4!c/[s]15
d  
93B:FIOP//UNIT/+15d 
Net Opening position at start of 
day cycle 
M 22H Cycle of 
Position 
:4!c//4!c  22H: OPDC//OPDC 
Day Cycle 
M 36B Net Settling 
Trades 
:4!C//4!C/15d 36B:NSTT//UNIT/15d  
Net of settling Trades in day cycle 
Cumulative to this point 
M 22H Credit/debit 
indicator 
:4!c//4!c  22H:CRDB//CRED or  
22H:CRDB//DEBT 
This tag qualifies Net Of Settling 
Trades 
M 36B Net 
Miscellaneous 
Activity 
:4!C//4!C/15d 36B:NMAC//UNIT/15d 
Net of day cycle Miscellaneous 
Activity cumulative to this point 
M 22H Credit/debit 
indicator 
:4!c//4!c: 22H:CRDB//CRED or  
22H:CRDB//DEBT 
This tag qualifies Net of Day Cycle 
Miscellaneous Activity 
M 36B Quantity 
Allocated 
:4!c//4!c/15d  36B:ALLO//UNIT/15d 
Net of day cycle [[shares]] Received or 

---

## Page 73

   Message Data      
M/O Tag Field 
Description 
Data Field Format Example 
 Delivered Cumulative to this point 
M 22H Credit/debit 
indicator 
:4!c//4!c  22H:CRDB//CRED = [[short position]]  
22H:CRDB//DEBT = Long Position 
This tag qualifies the New of Day 
Cycle [[shares]] Received 
M 93B Aggregate 
Balance 
:4!c/[4!c[4c]]/4!c/[s]15
d  
93B:AGGR//UNIT/+15d 
Net of Current [[CNS]] Position 
M 16R Start of Block B1 16R:DEPINFO 
M 11A [[settlement]] 
Currency 
:4!c//3!a  11A: SETT//USD 
M 95a Depositary 
Bank 
 :4!c/4!c[4c]/34z  95R: DEBA/DTCY/<partnum ([[DTC]]) 
[[CNS]] will be using the 95R [[Option]] of 
this tag for this product 
M 16S End of Block 
(B1) 
DEPINFO 16S: DEPINFO 
M 16S End of Block 
(B) 
POSINFO 16S: POSINFO 
M 16R Start of Block 16R 16R: NSTD 
M 94B Place of Trade :4!c/[4!c[4c]]/4!c[/30z]  
 
94B: TRAD/DTCY/< [[Stock Exchange]] 
Code 
*[[DTCC]] Values are at the end of this 
document. 
M 22H Buy/Sell :4!c//4!c  22H:BUSE//BUYI <<< this is a 
capital letter “eye” 
22H:BUSE//SELL 

---

## Page 74

   Message Data      
M/O Tag Field 
Description 
Data Field Format Example 
M 36B Quantity of 
[[securities]] 
:4!C//4!C/15d 36B:QSEC//UNIT/15d 
M 95a Contra [[Broker]]  :4!c/4!c[4c]/34z  95R: CTRA/DTCY/<partnum> 
[[CNS]] will be using the 95R [[Option]] of 
this tag for this product 
M 22H Net Settling 
Trade Cycle 
:4!c//4!c  22H: NSDC//NSDC Day Cycle 
M 19A Contract 
Value 
:4!c//[s]3!a15d  19A:PRIN//(s)USD15d 
M 98a Trade  
Date 
:4!c//8!n  98A:TRAD//MMDDCCYY 
[[CNS]] will be using the 98A [[Option]] of 
this tag for this product 
O 20C Exchange/ 
VMU 
Reference 
:4!c//16x 20C:EVMU//16x 
M 16S End of Block 16S 16S: NSTD 
M 16R Start of Block 16R 16R: MSAC 
M 22H Net Misc. 
Activity Cycle 
:4!c//4!c 22H: NMDC//NMDC Day Cycle 
M 36B Quantity of 
Miscellaneous 
activity 
:4!C//4!C/15d 36B:ADJU//UNIT/15d 
M 22H Credit/debit 
indicator 
:4!c//4!c  22H:CRDB//CRED = [[short position]]  
22H:CRDB//DEBT = Long Position 
M 19A  :4!c//[s]3!a15d  19A:VALU//(s)USD15d 

---

## Page 75

   Message Data      
M/O Tag Field 
Description 
Data Field Format Example 
M 22F Type of 
Adjustment 
:4!c/[4!c[4c]]/4!c  22F:TYMA/DTCY/xx  
*[[DTCC]] Values are at the end of this 
document. 
 * DTCY Qualifier overrides 
requirement for 4 character data  
M 98a Internal time 
stamp 
:4!c//8!n6!n  :98C:PROC//yyyymmddhhmmss 
[[CNS]] will be using the 98C [[Option]] of 
this tag for this product 
M 16S End of Block 16S 16S: MSAC 
 

---

## Page 76

  Value Indicators      
[[CNS]] Intraday Value Indicators 
[[CNS]] Sub-Account  
  
A Regular Account 
E Fully Paid Account 
G Reorg 1 Account 
H Reorg 2 Account 
J Reorg 3 Account 
K Reorg 4 Account 
L Reorg 5 Account 
M Reorg 6 Account 
R ACATS Long 
S ACATS Short 
 
 
Place of Trade 
  
AB  Exchange Traded Funds 
AM [[NYSE]] Mkt 
AN [[NYSE]] [[Bonds]] 
BA BATS BZX 
BN [[NASDAQ]] OMX BX 
BY BATS BYX 
CR Correspondent Clearing 
DA Direct Edge EDGA 
DX Direct Edge EDGX 
[[ID]]  [[DTC]] [[ID]] ([[Prime Broker]]) 
MU RTTM Muni [[Bonds]] 
MW Chicago [[Stock Exchange]] 
NQ [[NASDAQ]] 
NY [[New York Stock Exchange]] 
OC Over The Counter 
OP Options Clearing Corp 
PC [[NYSE]] ARCA 
PH [[NASDAQ]] OMX PHLX 
UN RTTM [[UIT]] 
 
 
 
 
 

---

## Page 77

  Value Indicators      
 
 
Type of Adjustment 
 
02 Ineligible Security Cutouts  
15 OW 
17 [[ID]] NET 
18 [[ID]] NET Reject/Reversal  
20 [[Member]] Firm Merger  
25 Honest [[Broker]]  
30 Name Change  
35 ACATS-ODS  
36 ACATS-ODS / [[DTC]]  
39 Order Out - [[DTC]] Portion  
40 Supplemental Trade - NISS  
50 Reorg - Name Change  
51 Reorg - MERGER  
52 Reorg - Redemption  
53 Reorg - Inelig Tnder  
54 Reorg - Revrse Split  
55 Daily Bal After Aloc  
56 Reorg Exit  
59 Index Wts Exercise  
65 ACATS  
66 ACATS / [[DTC]]  
71 JNL - Trd Adjustment  
73 JNL - Div Adjustment  
74 Inter Acct Netting 
75 JNL - REC/DEL ADJ  
76 RIO B/O INTO [[CNS]] 
77 JNL - BUY-IN EXECUTE 
79 JNL - [[CNS]] INELIG ADJ 
81 JNL - Reorg Adj 
81 JNL - Reorg Adj  
83 JNL - Mem Firm Adj  
91 [[Stock]] Borrow  
92 Transfer Into FPF  
93 Transfer Out Of FPF  
  
 