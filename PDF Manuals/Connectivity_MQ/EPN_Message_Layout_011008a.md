---
title: "EPN_Message_Layout_011008a.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/EPN_Message_Layout_011008a.pdf"
pages: 34
size: "477.0 KB"
category: "Connectivity_MQ"
ingested_on: "2026-06-05"
---

# EPN_Message_Layout_011008a.pdf

**Original File:** [EPN_Message_Layout_011008a.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/EPN_Message_Layout_011008a.pdf)  
**Category:** Connectivity_MQ  
**Total Pages:** 34  
**File Size:** 477.0 KB  

---

## Page 1

ADVANCING FINANCIAL MARKETS. TOGETHER.TM 
 
[[DTCC]] Public (White) 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
FIXED INCOME CLEARING 
CORPORATION: 
MBS EPN MESSAGE LAYOUTS 


---

## Page 2

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 2 
    
 
 
 
 
 
[[DTCC]] Public (White) 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
The MBS EPN Message Layouts guide (hereinafter, the "Guide") is provided as a convenience to Participants and for information  only. Although [[FICC]] 
may make this Guide available to Participants, it shall be under no obligation to [[DO]] so nor, having once or more done so, sha ll [[FICC]] have a continuing 
obligation to make available this Guide or other related information of a certain type.  
 
[[FICC]] DOES NOT REPRESENT THE ACCURACY, ADEQUACY, TIMELINESS, COMPLETENESS, OR FITNESS FOR ANY PARTICULAR PURPOSE 
OF ANY INFORMATION PROVIDED TO MEMBERS IN THIS GUIDE, WHICH IS PROVIDED AS -IS. [[FICC]] SHALL NOT BE LIABLE FOR ANY LOSS 
RELATED TO SUCH INFORMATION (OR THE ACT OR PROCESS OF PROVIDING SUCH INFORMATION) RESULTING DIRECTLY OR INDIRECTLY 
FROM MISTAKES, ERRORS, OR OMISSIONS, OTHER THAN THOSE CAUSED DIRECTLY BY GROSS NEGLIGENCE OR WILLFUL MISCONDUCT 
ON THE PART OF [[FICC]]. [[FICC]] SHALL NOT BE LIABLE FOR: (1) ANY LOSS RESULTING DIRECTLY OR INDIRECTLY FROM INTERRUPTIONS, 
DELAYS, OR DEFECTS ARISING FROM OR RELATED TO PROVIDING THIS GUIDE; AND (2) ANY SPECIAL, CONSEQUENTIAL, EXEMPLARY, 
INCIDENTAL, OR PUNITIVE DAMAGES. 
 
Further, the information contained in this Guide is subject to change. Participants and other authorized users of the Guide will find the most current version 
of the Guide on [[FICC]]’s internet site, www.[[DTCC]].com/clearing-services. [[FICC]] shall bear no responsibility for any losses associated with the failur e of 
Participants or other authorized users to follow [[FICC]]’s most current Guide.  
 
 

---

## Page 3

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 3 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Table of Contents 
1. Introduction .......................................................................................................................................................................................................................... 5 
2. ESP Message Record Layout ............................................................................................................................................................................................. 5 
ESP Message Header ............................................................................................................................................................................................................. 5 
ESP Pool Detail ....................................................................................................................................................................................................................... 9 
3. EPN Input Message Record Layouts ................................................................................................................................................................................ 10 
Message Header ................................................................................................................................................................................................................... 10 
Pool Detail ............................................................................................................................................................................................................................. 13 
Status Request ...................................................................................................................................................................................................................... 15 
Retransmission Request ....................................................................................................................................................................................................... 16 
Last Sequence ....................................................................................................................................................................................................................... 17 
Heartbeat Primary ................................................................................................................................................................................................................. 18 
Logon ..................................................................................................................................................................................................................................... 19 
4. EPN Output Messages Record Layouts ........................................................................................................................................................................... 20 
Header ................................................................................................................................................................................................................................... 20 
Pool Detail ............................................................................................................................................................................................................................. 22 
Last Sequence Reply ............................................................................................................................................................................................................ 24 
Heartbeat Acknowledgement ................................................................................................................................................................................................ 25 
Application Acknowledgment................................................................................................................................................................................................. 26 
Text Message ........................................................................................................................................................................................................................ 27 
5. EPN Edit and Validation Requirements ............................................................................................................................................................................ 28 
Header Record Mandatory Data............................................................................................................................................................................................ 28 
Header Record Optional Data ............................................................................................................................................................................................... 31 
Pool Detail Mandatory Data ................................................................................................................................................................................................... 32 

---

## Page 4

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 4 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Pool Detail Optional Data ...................................................................................................................................................................................................... 33 
 
  

---

## Page 5

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 5 
    
 
 
 
 
 
[[DTCC]] Public (White) 
1. INTRODUCTION 
This document provides participants with message layouts for processing messages via [[FICC]]’s Electronic Pool Notification (EPN) system. The document 
supplements the information provided in the: 
• EPN Implementation Guide 
• EaSy Pool Action Guide 
• MBS EPN Guidelines and Codes Guide 
 
Terms used in this Document 
Throughout this document, certain abbreviations are used to describe the input that must be included or the format of the fie ld. Under the TYPE heading, 
participants will see either an ‘A’, ‘N’ or both referenced. ‘A’ signifies that input into the field should be alpha format, ‘N’ means that a numeric format is 
required and if ‘A/N’ is listed, the field will take an alphanumeric input. Fields will be referenced as either ‘M’ or ‘O’. I nput into a field designated as ‘M’ is 
mandatory. Input in a field marked as ‘O’ is optional. 
 
2. ESP MESSAGE RECORD LAYOUT 
ESP Message Header 
The Header Record contains critical information as it relates to the sender, recipient and general trade terms and must be a comma delimited file (.csv). All 
input fields containing commas must be enclosed by double-quotes (“ ”) for application to read commas as literal therefore, double-quotes (“ ”) cannot be 
sent as field contents and be read as literal. All output fields containing commas will be enclosed by double-quotes (“ ”) upon executing “Save As” in 
application. Be sure that numeric fields [[DO]] not appear in scientific notation format as ESP cannot process these as such. Not ations in the “PIC” column 
such as “9 (09) V9 (02)” and “9 (03) V9 (09)” mean the field contains an implied decimal. This means the file should NOT contain an actual decimal point.  
ESP will assume the number of digits following the “V9” will read into the application on the right side of a decimal point.  
 
 
FIELD NAME FIELD DESCRIPTION LENGTH TYPE PIC M/O EDITS 
Date Received Date message received into 
application (CCYYMMDD) 
8 N 9 (08) M Input: Must be blank (a comma) Output: 
Populated by ESP 
Time Received Time message received into 
application 
6 N 9 (06) M Input: Must be blank (a comma) Output: 
Populated by ESP 

---

## Page 6

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 6 
    
 
 
 
 
 
[[DTCC]] Public (White) 
T2 Time T2 Time 6 N 9 (06) M Input: Must be blank (a comma) Output: 
Populated by ESP 
Message Type Indicates message type (ON, DK, 
CX, CC) 
2 A/N X (02) M Must be ON, DK, CX or CC 
Sequence Number Submitter sequence number, used 
for gap detection 
6 N 9 (06) M Populated by ESP on Input and Output 
Submitter / Local 
Submitter 
Account symbol of message initiator 
EPN(MBXX)/ 
Local symbol 
4/ 20 A/N X (04)/ X(20) M Input: Submitter or Local Submitter must 
be entered 
Output: Populated by ESP 
Submitter Name Name of Submitting Firm 40 A/N X (40) O Input: Will not be edited Output: 
Populated by ESP 
Contra /Local Contra Account symbol of message 
recipient EPN(MBXX)/Local Symbol 
4/20 A/N X (04)/ X(20) M Validated against a database/ will be 
convert by ESP is database populated 
Contra Name Name of Contra Firm 40 A/N X (40) O Input: Will not be edited 
Output: Populated by ESP if populated 
in database 
TBA [[CUSIP]]/ Local 
Security Symbol 
product code, agency, coupon , 
maturity and [[settlement]] month 
(01F082630) – as issued by 
Standard & Poors. 
9/20 A/N X (9)/ X(20) M Input: TBA [[CUSIP]] or Local Security 
Symbol must be entered Output: 
Populated by ESP 
Original Trade Par Par value of the Original Trade 11 N 9(09) V9(02) M Syntactical edit for numeric; must be > 
zero 
Price Decimal dollar amount paid for the 
[[securities]] 
12 N 9(03) V9 (09) M Syntactical edit for numeric; must be > 
zero 

---

## Page 7

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 7 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Good Delivery 
Millions 
Number of $MM lots delivered in 
accordance with standards 
4 N 9 (04) M Syntactical edit for numeric < SysParm 
Trade Date Date the trade was executed 
(CCYYMMDD) 
6/8 N 9 (08) M Will not be edited 
[[settlement]] Date Date the trade will settle 
(CCYYMMDD) 
8 N 9 (08) M Will not be edited for ON, DK and CX 
messages. For CC messages it must be 
a valid business/[[settlement]] date. 
Delivery Date Date the [[securities]] will be delivered 
(CCYYMMDD) 
8 N 9 (08) M Will not be edited 
Internal [[ID]] Unique reference number input by 
[[participant]] 
16 A/N X (16) O Will not be edited 
Subaccount/ 
Local Sub Account 
Identifies subaccount associated with 
an ON/ description of message 
recipient 
4/20 A/N X(04)/X(20) O Input: Subaccount or Local Subaccount 
must be entered. Output Populated by 
ESP if field was populated in database 
Reason Code Reason for the action taken (0123) 4 N 9 (04) O1 Validated against a database 
Target Message [[ID]] Message [[ID]] of the message being 
acted upon 
11 A/N X (11) O Will not be edited 
XREF Tag assigned by [[participant]] 15 A/N X (15) O Will not be edited 
 
1 Mandatory for DK and CX messages 

---

## Page 8

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 8 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Special Instructions Informational only trade terms 30 A/N X (30) O Will not be edited 
Number of Pools Number of pools contained within 
this 
message 
4 N 9 (04) O Validated against actual count of pools 
in 
Detail. If the number in this field does 
not match, it will be modified/changed to 
match count of pools in Detail. On CC 
messages the value must equal the 
number of replacement pools in the 
message. It will not be modified if it 
does not match the count, it will be 
rejected by EPN if it does not match the 
count in the message. 
Pos Dup Indication that input message may 
be a duplicate 
1 A/N X (01) O see table below2 
 
 Pos Dup Export Table 
 Received Message Imported Sent Msg Turned Sent Msg Entered in ESP & Sent 
Not Pos Dup blank I T E 
Pos Dup X Z Y Q 
 
 
 
2 On export, possible values in this field are as described in the above table.  
 
On Import, Pos Dup value should be X or blank; however values of Y,Z or Q will be associated with X, and values of T, I and E  will be associated with 
blank. 

---

## Page 9

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 9 
    
 
 
 
 
 
[[DTCC]] Public (White) 
ESP Pool Detail 
The Pool Detail Records contain the pool information subordinate to the associated Header Record. Pool Detail records must immediately follow their 
associated Pool Header record. After the last Pool Detail record, a “dummy” Pool Detail record must follow with “XXXXXX” popu lated in the “Lot [[ID]]” field. 
The next record will be the next Header record in the file. EPN currently allows for up to 250 Pool Detail Records per message. Any fields co ntaining 
commas must be enclosed by double-quotes (“ ”) for application to read commas as literal therefore, double-quotes (“ ”) cannot be sent as field contents 
and be read as literal. Be sure that numeric fields [[DO]] not appear in scientific notation format as ESP cannot process these a s such. Notations in the “PIC” 
column such as “9 (09) V9 (02)” and “9 (03) V9 (09)” mean the field contains an implied decimal. This means the file should NOT contain an actual decimal 
point. ESP will assume the number of digits following the “V9” will read into the application on the right side of a decimal point. Neither mandatory nor 
optional fields are edited. The entire message is rejected only if erroneous data is detected in the Header Record. 
 
FIELD NAME FIELD DESC RIPTIO N LENGTH TYPE PIC M/O EDITS 
Lot-[[ID]] Lot-sequence of GDMM pool(s) (1234AA) 6 A/N X (06) O Will not be edited 
Pool Number Number referencing a pool of mortgages 7 A/N X (07) M Will not be edited 
Original Face Principal amount of MBS at date of issue 9 N 9 (09) M Will not be edited 
Coupon Rate of interest recorded on the face of the 
certificate 
6 N 9 (02) V9 
(04) 
M Will not be edited 
Maturity Date Maturity date of the mortgage pool (CCYYMMDD) 8 N 9 (08) O Will not be edited 
New Issue Identifies a new pool issue (X or blank) 1 A/N X (01) O Will not be edited 
Trade Number Trade number 10 N 9 (10) O Will not be edited 
Control Number Individual pool detail reference number assigned by 
the user 
15 A/N X (15) O Will not be edited 
Current Face The outstanding principal of the mortgage 11 N 9 (09) V9 
(02) 
O Will not be edited 
Factor Percentage of original principal outstanding 10 N 9 (01) V9 
(09) 
O Will not be edited 
[[CUSIP]] Number Pool [[CUSIP]] Number 9 A/N X (09) O Will not be edited 
Issue Date Date the mortgage pool was issued (CCYYMMDD) 6/8 N 9 (08) O Will not be edited 
Terminator Value of GDMMs of preceding lot (Odd-lot=9999) 4 N 9 (04) M Will not be edited. 
See Terminators 
in the EPN 
Guidelines and 
Codes Guide 

---

## Page 10

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 10 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Principal The  unpaid balance of an obligation exclusive of 
interest 
11 N 9 (09) V9 
(02) 
O Will not be edited 
Interest Interest accrued on the balance 11 N 9 (09) V9 
(02) 
O Will not be edited 
Net Money Net Money 11 N 9 (09) V9 
(02) 
O Will not be edited 
Special 
Instructions 
Informational only pool detail terms 30 A/N X (30) O Will not be edited 
 
3. EPN INPUT MESSAGE RECORD LAYOUTS 
 
Message Header 
The Header record contains critical information regarding the sender, recipient, and general trade terms. Version 2 message t ype uses a 4-digit year 
format. All Mandatory fields are edited for format and, when possible, validated for content. Optional fields are not edited/validated.  
 
Field Name Field Description Length Type PIC M/O Edits 
Start Message 
Indicator 
Used to indicate start of message (“Hex 02”) 1 A/N X (01) M Must be “Hex 02” 
Message Type Indicates message type (ON, CC, DK, CX) 2 A/N X (02) M Validated against a 
database 
Sequence Number Submitter sequence number, used for gap detection 6 N 9 (06) M Must be
 in 
ascending order 
EPN Version 
Control 
Version control number established by EPN 3 N 9 (03) M Must be “002” 
Subscriber [[ID]] EPN [[Member]] [[ID]] (0123) 4 A/N X (04) M Validated against a 
database 
Connection [[ID]] EPN Connection [[ID]] 4 A/N X (04) M Validated against a 
database 

---

## Page 11

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 11 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Submitter EPN account symbol of message initiator (MBXX) 4 A/N X (04) M Validated against a 
database 
Contra EPN account symbol of message recipient (MBYY) 4 A/N X (04) M Validated against a 
database 
[[CUSIP]] [[CUSIP]] 9 A/N X (9) M Validated against a 
database 
Filler Filler 1 / / / Must be blank 
Original Trade Par Par value of the Original Trade 11 N 9 (09) V9 (02) M Edit for numeric; 
must be > zero 
Filler Filler 10 / / / Must be blank 
Price Decimal dollar amount paid for the [[securities]] 12 N 9 (03) V9 (09) M Edit for numeric; 
must be > zero 
Good Delivery 
Millions 
Number of $MM lots delivered in accordance with 
standards 
4 N 9 (04) M Edit for numeric < 
SysParm 
Trade Date Date the trade was executed (mmddyyyy) 8 N 9 (08) M Will not be edited 
[[settlement]] Date Date the trade will settle (mmddyyyy) 8 N 9 (08) M Will not be edited 
ON, DK, CX 
messages. On CC  
messages must be 
valid business 
date. 
Delivery Date Date the [[securities]] will be delivered (mmddyyyy) 8 N 9 (08) M Will not be edited 
Internal [[ID]] Unique reference number input by [[Member]] 16 A/N X (16) O Will not be edited 
Subaccount Identifies subaccount associated with an ON 4 A/N X (04) O Validated against a 
database 
Reason Code Reason for the action taken (0123) 4 N 9 (04) O3 Validated against a 
database 
 
3 Mandatory for DK and CX messages. 

---

## Page 12

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 12 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Target Message [[ID]] Message [[ID]] of the message being acted upon 11 A/N X (11) O Will not be edited 
XREF Tag assigned by [[Member]] 15 A/N X (15) O Will not be edited 
Filler Filler 4 / / / Must be blank 
Pos Dup Indication that input message may be a duplicate 1 A/N X (01) O Must be X or blank 
Special 
Instructions 
Informational only trade terms 30 A/N X (30) O Will not be edited 
Number of Pools Number of pools contained within this message 4 N 9 (04) M/O4 Will not be edited 
on  ON, DK and CX 
messages. Will be 
validated on Pool 
Substitution 
messages. 
 
  
 
4 Mandatory input on Pool Substitution messages; must equal the number of substituted pools in the message.  

---

## Page 13

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 13 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Pool Detail 
Pool Detail records contain pool information subordinate to the associated Header record. EPN currently allows for up to 250 Pool Detail records per message. 
 
Field Name Field Description Length Type PIC M/O Edits 
Lot-[[ID]] Lot-sequence of GDMM pool(s) (1234AA) 6 A/N X (06) O Will not be edited 
Filler Filler 2 / / / Must be blank 
Pool Number Number referencing a pool of mortgages 7 A/N X (07) M Will not be edited 
Original Face Principal amount of MBS at date of issue 9 N 9 (09) M Will not be edited 
Coupon Rate of interest recorded on the face of the certificate 6 N 9 (02) V9 (04) M Will not be edited 
Maturity Date Maturity date of the mortgage pool (mmddyyyy) 8 N 9 (08) O Will not be edited 
New Issue Identifies a new pool issue (X or blank) 1 A/N X (01) O Will not be edited 
Trade Number MBSD trade number 10 N 9 (10) O Will not be edited 
Control Number Individual pool detail reference number assigned by 
the user 
15 A/N X (15) O Will not be edited 
Filler Filler 15 / / / Must be blank 
Current Face The outstanding principal of the mortgage 11 N 9 (09) V9 (02) O Will not be edited 
Factor Percentage of original principal outstanding 10 N 9 (01) V9 (09) O Will not be edited 
[[CUSIP]] Number [[CUSIP]] Number 9 A/N X (09) O Will not be edited 
Filler Filler 5 / / / Must be blank 
Issue Date Date the mortgage pool was issued (mmddyyyy) 8 N 9 (08) O Will not be edited 
Terminator Value of GDMMs of preceding lot (Odd-lot=9999) 4 N 9 (04) M5 Will not be edited 
Principal The unpaid balance of an obligation exclusive of interest 11 N 9 (09) V9 (02) O Will not be edited 
Interest Interest accrued on the balance 11 N 9 (09) V9 (02) O Will not be edited 
 
5 On Pool Substitution messages, the cancel portion begins with a 6 and the substituted with a 7. The sum of the terminators on canceled lot(s) must equal 
the sum of the terminator on the substituted lot(s) that follow. 

---

## Page 14

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 14 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Net Money Net Money 11 N 9 (09) V9 (02) O Will not be edited 
Special 
Instructions 
 30 A/N X (30) O Will not be edited 
Filler Filler 10 / / / Must be blank 
End Message 
Indicator 
Used to indicate end of message (“Hex 03”) 1 A/N X (01) M6 Must be “Hex 03” 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
6 Mandatory on Last Pool Detail Record within a single message (space character on a ll other Pool Detail Records). 

---

## Page 15

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 15 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Status Request 
 
Field Name Field Description Lengt
h 
Type PIC M/O Edits 
Start Message 
Indicator 
Used to indicate start of message (“Hex 02”) 1 A/N X (01) M Must be “Hex 02” 
Message Type Indicates message type (SR) 2 A/N X (02) M Validated against a 
database 
Sequence Number Submitter sequence number, used for gap detection 6 N 9 (06) M Must be in 
ascending order 
EPN Version 
Control 
Version control number established by EPN 3 N 9 (03) M MBSD assigned 
current version 
Subscriber [[ID]] EPN [[participant]] [[ID]] (0123) 4 A/N X (04) M Validated against a 
database 
Connection [[ID]] EPN Connection [[ID]] of SR submitter 4 A/N X (04) M Validated against a 
database 
Account [[ID]] Account symbol to correlate with AA messages (MBXX) 4 A/N X (04) M Validated against a 
database 
Original 
Connection [[ID]] 
Connection [[ID]] of submitter of message(s) on SR 4 A/N X (04) M Validated against a 
database 
From Sequence # Starting point of Sequence # on Status Request 6 N 9 (06) M Must be < “To 
Sequence #” value 
To Sequence # Ending point of Sequence # on Status Request 6 N 9 (06) M Must be > “From 
Sequence #” value 
End Message 
Indicator 
Used to indicate end of message (“Hex 03”) 1 A/N X (01) M Must be “Hex 03” 
 
 
 

---

## Page 16

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 16 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Retransmission Request 
 
Field Name Field Description Length Type PIC M/O Edits 
Start Message 
Indicator 
Used to indicate start of message (“Hex 02”) 1 A/N X (01) M Must be “Hex 02” 
Message Type Indicates message type (RR) 2 A/N X (02) M Validated against a 
database 
Sequence Number Submitter sequence number, used for gap detection 6 N 9 (06) M Must be
 in 
ascending order 
EPN Version 
Control 
Version control number established by EPN 3 N 9 (03) M MBSD assigned 
current version 
Subscriber [[ID]] EPN [[participant]] [[ID]] (0123) 4 A/N X (04) M Validated against a 
database 
Connection [[ID]] EPN Connection [[ID]] of RR submitter 4 A/N X (04) M Validated against a 
database 
Account [[ID]] Account symbol to correlate with AA messages (MBXX) 4 A/N X (04) M Validated against a 
database 
Original 
Connection [[ID]] 
Connection [[ID]] from which message(s) originated 4 A/N X (04) M Validated against a 
database 
To Connection [[ID]] Connection [[ID]] to which message(s) are to be 
retransmitted 
4 A/N X (04) M Validated against a 
database 
From Sequence # Starting Sequence # of message(s) to be retransmitted 6 N 9 (06) M Must be < “To 
Sequence #” value 
To Sequence # Ending Sequence # of message(s) to be retransmitted 6 N 9 (06) M Must be > “From 
Sequence #” value 
End Message 
Indicator 
Used to indicate end of message (“Hex 03”) 1 A/N X (01) M Must be “Hex 03” 

---

## Page 17

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 17 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Last Sequence 
 
Field Name Field Description Length Type PIC M/O Edits 
Start Message Indicator Used to indicate start of message (“Hex 02”) 1 A/N X (01) M Must be “Hex 02” 
Message Type Indicates message type (LS) 2 A/N X (02) M Validated against a 
database 
Sequence Number Submitter sequence number, gaps are not detected 6 N 9 (06) M Will not be edited 
EPN Version Control Version control number established by EPN 3 N 9 (03) M MBSD assigned 
current version 
Subscriber [[ID]] EPN [[participant]] [[ID]] (0123) 4 A/N X (04) M Validated against a 
database 
Connection [[ID]] Submitting EPN Connection [[ID]] 4 A/N X (04) M Validated against a 
database 
Account [[ID]] Account symbol 4 A/N X (04) M Validated against a 
database 
Inquiring Connection [[ID]] Inquiry for this EPN Connection [[ID]] 4 A/N X (04) M Validated against a 
database 
End Message Indicator Used to indicate end of message (“Hex 03”) 1 A/N X (01)  Must be “Hex 03” 
 
  

---

## Page 18

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 18 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Heartbeat Primary 
 
Field Name Field Description Length Type PIC M/O Edits 
Start Message Indicator Used to indicate start of message (“Hex 02”) 1 A/N X (01) M Must be “Hex 02” 
Message Type Indicates message type (HP) 2 A/N X (02) M Validated against a 
database 
Sequence Number Submitter sequence number, gaps are detected 6 N 9 (06) M Must be ascending 
EPN Version Control Version control number established by EPN 3 N 9 (03) M MBSD assigned 
current version 
Subscriber [[ID]] EPN [[participant]] [[ID]] (0123) 4 A/N X (04) M Validated against a 
database 
Connection [[ID]] EPN Connection [[ID]] 4 A/N X (04) M Validated against a 
database 
Account [[ID]] Account symbol 4 A/N X (04) M Validated against a 
database 
End Message Indicator Used to indicate end of message (“Hex 03”) 1 A/N X (01) M Must be “Hex 03” 
 
  

---

## Page 19

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 19 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Logon 
 
Field Name Field Description Length Type PIC M/O Edits 
Start Message Indicator Used to indicate start of message (“Hex 02”) 1 A/N X (01) M Must be “Hex 02” 
Message Type Indicates message type (LO) 2 A/N X (02) M Validated against a 
database 
Sequence Number Submitter sequence number, gaps are detected 6 N 9 (06) M Must be ascending 
EPN Version Control Version control number established by EPN 3 N 9 (03) M MBSD assigned 
current version 
Subscriber [[ID]] EPN [[participant]] [[ID]] (0123) 4 A/N X (04) M Validated against a 
database 
Connection [[ID]] EPN Connection [[ID]] 4 A/N X (04) M Validated against a 
database 
Account [[ID]] Account symbol 4 A/N X (04) M Validated against a 
database 
Connection Authentication Connection Authentication Password / A/N / M / 
Connection Type TCP/IP Input only = I, TCP/IP Output only = O, TCP/IP 
Both Input and Output = B 
1 A X (01) M Must be ‘I’, ‘O’, ‘B’ 
Filler Filler 16 / / M Filler 
End Message Indicator Used to indicate end of message (“Hex 03”) 1 A/N X (01) M Must be “Hex 03” 
 
 
 
  

---

## Page 20

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 20 
    
 
 
 
 
 
[[DTCC]] Public (White) 
4. EPN OUTPUT MESSAGES RECORD LAYOUTS 
Header 
 
Field Name Field Description Length Type Picture Edits 
Start Message Indicator Used to indicate start of message (“Hex 02”) 1 A/N X (01) Output 
Message Type Indicates message type (ON, CC, DK, CX ) 2 A/N X (02) Output 
Sequence Number EPN generated sequence number, used for gap detection 6 N 9 (06) Output 
EPN Version Control Version control number established by EPN 3 N 9 (03) Output 
Subscriber [[ID]] EPN [[Member]] [[ID]] (0123) 4 A/N X (04) Output 
Connection [[ID]] EPN Connection [[ID]] 4 A/N X (04) Output 
Message [[ID]] EPN Message [[ID]] 11 A/N X (11) Output 
Submitter EPN account symbol of message initiator (MBXX) 4 A/N X (04) Output 
Submitter Name Name associated with Submitter account symbol 30 A/N X (30) Output 
Contra EPN account symbol of message recipient (MBYY) 4 A/N X (04) Output 
Contra Name Name associated with Contra account symbol 30 A/N X (30) Output 
[[CUSIP]] [[CUSIP]] 9 A/N X (9) Output 
Filler Filler 1 / / Output 
[[CUSIP]] Class Name Name associated with [[CUSIP]] Class Code 30 A/N X (30) Output 
Original Trade Par Par value of the Original Trade 11 A/N X (11) Output 
Filler Filler 10 / / Output 
Price Decimal dollar amount paid for the [[securities]] 12 A/N X (12) Output 
Good Delivery Millions Number of $MM lots delivered in accordance with standards 4 A/N X (04) Output 
Trade Date Date the trade was executed (mmddyyyy) 8 A/N X (08) Output 

---

## Page 21

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 21 
    
 
 
 
 
 
[[DTCC]] Public (White) 
[[settlement]] Date Date the trade will settle (mmddyyyy) 8 A/N X (08) Output 
Delivery Date Date the [[securities]] will be delivered (mmddyyyy) 8 A/N X (08) Output 
Internal [[ID]] Unique reference number input by [[Member]] 16 A/N X (16) Output 
Subaccount Subaccount [[ID]] used to identify subaccounts at the user side 4 A/N X (04) Output 
Reason Code Reason for the action taken (0123) 4 A/N X (04) Output 
Target Message [[ID]] Message [[ID]] of the message being acted upon 11 A/N X (11) Output 
XREF Tag assigned by [[Member]] 15 A/N X (15) Output 
Filler Filler 5 / / Output 
Special Instructions Informational trade terms 30 A/N X (30) Output 
T1 EPN Time-stamp #1 (12:31.45) 6 A/N X (06) Output 
T2 EPN Time-stamp #2 (12:31.45) 6 A/N X (06) Output 
T3 EPN Time-stamp #3 (12:31.45) 6 A/N X (06) Output 
T4 EPN Time-stamp #4 (12:31.45) 6 A/N X (06) Output 
T5 EPN Time-stamp #5 (12:31.45) 6 A/N X (06) Output 
Number of Pools Number of pool detail(s) submitted on message 4 A/N X (04) Output 
Pos Dup Indication that output message may be a duplicate (X or blank) 1 A/N X (01) Output 
 
  

---

## Page 22

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 22 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Pool Detail 
 
Field Name Field Description Length Type Picture Edits 
Lot-[[ID]] Lot-sequence of Good Delivery Million pool(s) (1234AA) 6 A/N X (06) Output 
Filler Filler 2 / / Output 
Pool Number Number referencing a pool of mortgages 7 A/N7 X (07) Output 
Original Face Principal amount of MBS at date of issue 9 A/N X (09) Output 
Coupon Rate of interest recorded on the face of the certificate 6 A/N X (06) Output 
Maturity Date Maturity date of the mortgage pool (mmddyyyy) 8 A/N X (08) Output 
New Issue Identifies a new pool issue (X or blank) 1 A/N X (01) Output 
Trade Number MBSD trade number 10 A/N X (10) Output 
Control Number Individual pool detail reference number assigned by the user 15 A/N X (15) Output 
Filler Filler 15 / / Output 
Current Face The outstanding principal of the mortgage 11 A/N X (11) Output 
Factor Percentage of original principal outstanding 10 A/N X (10) Output 
[[CUSIP]] Number [[CUSIP]] Number 9 A/N X (09) Output 
Filler Filler 5 / / Output 
Issue Date Date the mortgage pool was issued (mmddyyyy) 8 A/N X (08) Output 
 
7 Field should be right justified and padded on the left with zeroes (contrary to typical A/N fields). 

---

## Page 23

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 23 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Terminator Value of the Good Delivery Millions of the preceding lot of pools 4 A/N X (04) Output 
Principal The unpaid balance of an obligation  exclusive of interest 11 A/N X (11) Output 
Interest Interest accrued on the balance 11 A/N X (11) Output 
Net Money Net Money 11 A/N X (11) Output 
Special Instructions  Informational pool detail terms 30 A/N X (30) Output 
Filler Filler 10 / / Output 
End Message Indicator Used to indicate end of message (“Hex 03”) 1 A/N8 X (01) Output 
 
  
 
8 Populated on Last Pool Detail record within a single message (space character on all other Pool Deta il Records). 

---

## Page 24

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 24 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Last Sequence Reply 
 
Field Name Field Description Length Type Picture Edits 
Start Message Indicator Used to indicate start of message (“Hex 02”) 1 A/N X (01) Output 
Message Type Indicates message type (LS) 2 A/N X (02) Output 
Sequence Number EPN generated sequence number 6 N 9 (06) Output 
EPN Version Control Version control number established by EPN 3 N 9 (03) Output 
Subscriber [[ID]] EPN [[participant]] [[ID]] (0123) 4 A/N X (04) Output 
Connection [[ID]] Submitting EPN Connection [[ID]] 4 A/N X (04) Output 
Inquiring Connection [[ID]] Inquiry for this EPN Connection [[ID]] 4 A/N X (04) Output 
Inbound Seq Number Last seq number sent inbound to EPN for this Connection [[ID]] 6 A/N X (06) Output 
Outbound Seq Number Last seq number sent from EPN to this Connection [[ID]] 6 A/N X (06) Output 
End Message Indicator Used to indicate end of message (“Hex 03”) 1 A/N X (01) Output 
 
 
  

---

## Page 25

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 25 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Heartbeat Acknowledgement 
 
 
Field Name Field Description Length Type Picture Edits 
Start Message Indicator Used to indicate start of message (“Hex 02”) 1 A/N X (01) Output 
Message Type Indicates message type (HA) 2 A/N X (02) Output 
Sequence Number EPN generated sequence number 6 N 9 (06) Output 
EPN Version Control Version control number established by EPN 3 N 9 (03) Output 
Subscriber [[ID]] EPN [[participant]] [[ID]] (0123) 4 A/N X (04) Output 
Connection [[ID]] Submitting EPN Connection [[ID]] 4 A/N X (04) Output 
Heartbeat Type Response to HP=1 1 A/N X (01) Output 
Disaster Flag Disaster state, 0=normal, 1=disaster declared 2=DR available 1 A/N X (01) Output 
Original Seq Number Sequence number of original heartbeat message 6 A/N X (06) Output 
End Message Indicator Used to indicate end of message (“Hex 03”) 1 A/N X (01) Output 
 
  

---

## Page 26

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 26 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Application Acknowledgment 
 
Field Name Field Description Length Type Picture Edits 
Start Message Indicator Used to indicate start of message (“Hex 02”) 1 A/N X (01) Output 
Message Type Indicates message type (AA) 2 A/N X (02) Output 
Sequence Number EPN generated sequence number, used for gap detection 6 N 9 (06) Output 
EPN Version Control Version control number established by EPN 3 N 9 (03) Output 
Subscriber [[ID]] EPN [[participant]] [[ID]] (0123) 4 A/N X (04) Output 
Connection [[ID]] EPN Connection [[ID]] 4 A/N X (04) Output 
Internal [[ID]] Unique reference number input by [[participant]] 16 A/N X (16) Output 
Message [[ID]] EPN assigned Message [[ID]] 11 A/N X (11) Output 
Acknowledgment Code Indicates whether message is accepted or rejected (1234) 4 A/N X (04) Output 
EPN ACK Time-stamp Key Time-stamp indicating EPN Delivery (12:34.56) 6 A/N X(06) Output 
Original Sequence # Playback of User Sequence # used to match ACK 6 N 9 (06) Output 
End Message Indicator Used to indicate end of message (“Hex 03”) 1 A/N X (01) Output 
 
 
  

---

## Page 27

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 27 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Text Message 
 
Field Name Field Description Length Type Picture Edits 
Start Message Indicator Used to indicate start of message (“Hex 02”) 1 A/N X (01) Output 
Message Type Indicates message type (TX) 2 A/N X (02) Output 
Sequence Number EPN generated sequence number, used for gap detection 6 N 9 (06) Output 
EPN Version Control Version control number established by EPN 3 N 9 (03) Output 
Subscriber [[ID]] EPN [[participant]] [[ID]] (0123) 4 A/N X (04) Output 
Connection [[ID]] EPN Connection [[ID]] 4 A/N X (04) Output 
Text Type Indicates type of output message (Administrative or Gap Detection) 2 A/N X (02) Output 
Message Text Text of the output message if applicable 130 A/N X (130) Output 
End Message Indicator Used to indicate end of message (“Hex 03”) 1 A/N X (01) Output 
 
  

---

## Page 28

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 28 
    
 
 
 
 
 
[[DTCC]] Public (White) 
5. EPN EDIT AND VALIDATION REQUIREMENTS 
 
Header Record Mandatory Data 
The Header record contains critical information regarding the [[Buyer]], [[Seller]], and general trade terms. All mandatory fields ar e edited for syntax and, in 
some instances, validated for content. Most optional fields are not edited or validated.  
 
The entire message is rejected if the header record contains invalid mandatory data.  
 
Field Edit On-line Edit Comment 
Submitter Validated against a database Validated against a database Must be an active Account [[ID]]. 
Must NOT be an EPN-only [[Member]] if contra is an [[FICC]] account. 
Contra Validated against a database Validated against a database Must be an active Account [[ID]] 
TBA [[CUSIP]] Validated against a database Validated against a database Must be a valid TBA [[CUSIP]] as published by Standard & Poor’s 
Message 
Type 
Validated against a database Validated against a database Messages must be one of eight types: Original Notifications (ON), Don’t 
Know (DK), Cancel (CX), Pool Substitution (CC), Text (TX), Logon 
(LO), Application 
Acknowledgment (AA), Status Request (SR) or Retransmission 
Request (RR) for CTCI only 

---

## Page 29

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 29 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Original 
Trade Par 
Edits for numeric value Must 
be greater than zero 
Edits for numeric value Must 
be greater than zero 
Necessary to distinguish otherwise identical trades. EPN only 
validates if an odd lot is included in the ON message, tail PAR portion 
of this field will be part of the matching term for the targeted TBA 
position for allocation. If tail portion of this field is not found in [[Member]]’s 
matching open TBA position, [[FICC]] DKs the Odd Lot. 
 
For [[FICC]] outbound ON message to members, EPN populates it with 
Original Trade PAR of the targeted TBA Trade, and drop the digits 
higher from the billionth-place if Original Trade PAR is $1 billion or 
higher. 
Price Edits for numeric value Must 
be greater than zero 
Edits for numeric value Must 
be greater than zero 
Necessary to distinguish otherwise identical trades. If [[FICC]] and a Trade 
[[ID]] are included in the ON message, [[FICC]] will match up to and the 6th 
decimal point. If [[FICC]] and no Trade [[ID]] are included in the ON message, 
[[FICC]] will match up to and including the 9th decimal point. For DK and 
CC messages, price must match to the 6th decimal point of the 
targeted pool. 
Good 
Delivery 
Millions 
Edits for numeric value May 
contain a zero value to 
indicate the allocation of 
oddlot Must be less than 
system parameter 
Edits for numeric value May 
contain a zero value to 
indicate the allocation of 
oddlot or bad delivery Must 
be less than 
system parameter 
Necessary due to SIFMA variance 

---

## Page 30

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 30 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Trade Date Will not be edited Valid calendar date Necessary to distinguish otherwise identical trades 
[[settlement]] 
Date 
Will not be edited Valid calendar date Necessary to distinguish otherwise identical trades 
Delivery Date Will not be edited Valid calendar date Necessary to distinguish otherwise identical trades 
Reason Code Validated against a database Validated against a database Required for DKs and CXs to indicate the reason this action is taken 
Number of 
Pools 
Will not be edited Validated against actual 
number of pool details 
EPN verifies on-line entry 
 
  

---

## Page 31

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 31 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Header Record Optional Data 
 
Field CTCI Edit (if entered) On-line Edit (if entered) Comment 
Sub-Account Will not be edited Will not be edited Identify a specific customer of the submitter or recipient 
institution, “ZZZZ” used for unknown sub-account 
Target Message [[ID]] Will not be edited Will not be edited Used for DKs and Cancels to reference original EPN 
Message [[ID]] 
XREF Will not be edited Will not be edited Submitter’s in-house trade number (15 characters maximum) 
Special Instructions Will not be edited Will not be edited Informational free form field (30 characters maximum). STIP 
Position must include Trade [[ID]]. Generic TBA positions may 
optionally include Trade [[ID]]. Syntax: “TRID=VALUE=”, else 
system DKs the message. 
TRID’s value should be alphanumeric. 
 
Participants should see SPECIAL INSTRUCTIONS  
(MESSAGE HEADER) under the EPN General Guidelines  
section of the EPN Guidelines and Codes Guide for 
additional information. 
Internal [[ID]] Will not be edited Will not be edited Submitter’s unique identifier of a message Used 
to update internal systems when the EPN 
acknowledgment is received 
Used to track status of messages submitted to EPN Max. 
16 characters 
 
  

---

## Page 32

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 32 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Pool Detail Mandatory Data 
 
The Pool Detail records contain pool information subordinate to the associated Header record.  
 
Input: Neither mandatory nor optional Pool Detail record fields are edited. The message is rejected only if erroneous data is dete cted in the Header 
record. Fields not edited by EPN could contain illogical values, (e.g., alpha characters in the Coupon field). Users should anticipat e this potentially 
erroneous data entering their internal systems. 
 
On-line Input: Mandatory fields in the Pool Detail record are edited for format and, in some instances, validated for content. Optional fields are edited for 
format only. Errors that are detected upon submission are highlighted and must be corrected by the EPN user before the messag e can be processed. 
 
Field CTCI Edit (if entered) On-line Edit (if entered) Comment 
Lot-[[ID]] Will not be edited Mandatory 
Valid alpha/numeric 
Common method to communicate good delivery  millions to 
recipient. 
Common reference point needed to communicate DKs, CC 
and CXs of pool level details 
Pool Number Will not be edited Mandatory 
Valid alpha/numeric 
 
Original Face Will not be edited Mandatory 
Valid numeric 
Greater than zero 
Used to determine amortized amount 
Coupon Will not be edited Valid numeric Used for the possibility of different coupon rates being 
allocated to the same trade (e.g. COFIs). 
Terminator Will not be edited Mandatory 
Valid numeric 
Used to distinguish the mid and end of an individual lot of  
pools. Participants should see the Pool Terminators  
section of the EPN Guidelines and Codes Guide for  
additional information. 
 
 

---

## Page 33

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 33 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Pool Detail Optional Data 
 
Field CTCI Edit (if entered) On-line Edit (if entered) Comment 
Maturity Date Will not be edited Valid calendar date  
New Issue Will not be edited Must be “X” or Blank  
Trade Number Will not be edited Valid alphanumeric  
Control Number Will not be edited Valid alphanumeric  
Current Face Will not be edited Valid numeric Greater 
than zero 
 
Factor Will not be edited Valid numeric 
Greater or equal to zero and 
less than or equal to 2 
 
[[CUSIP]] Number Will not be edited Valid alpha/numeric  
Issue Date Will not be edited Valid calendar date  
Principal Will not be edited Valid numeric  

---

## Page 34

MBS EPN Message Layouts Version 1.2 
 
 
 
 
Page 34 
    
 
 
 
 
 
[[DTCC]] Public (White) 
Interest Will not be edited Valid numeric  
Net Money Will not be edited Valid numeric  
Special Instructions Will not be edited Will not be edited Informational free form field (30 characters maximum). 
EPNX={…} is an optional field for the submitter to  include a 
pool level reference number to link with Pool 
Instruct records. 
 
 
 