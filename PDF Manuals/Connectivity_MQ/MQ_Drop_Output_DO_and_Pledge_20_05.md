---
title: "20.05_MQ_Drop_Notification_Output_DO_and_Pledge"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_Drop_Output_DO_and_Pledge_20_05.pdf"
pages: 24
size: "210.5 KB"
category: "Connectivity_MQ"
ingested_on: "2026-06-05"
---

# 20.05_MQ_Drop_Notification_Output_DO_and_Pledge

**Original File:** [MQ_Drop_Output_DO_and_Pledge_20_05.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_Drop_Output_DO_and_Pledge_20_05.pdf)  
**Category:** Connectivity_MQ  
**Total Pages:** 24  
**File Size:** 210.5 KB  

---

## Page 1

 CF2/MQ Transmission Guides 
 
 
 
 
20.05 MQ DROP NOTIFICATION OUTPUT 
(FOR DELIVER ORDER AND PLEDGE ACTIVITY) 
 
 
 
 
 
 
 
The Depository Trust & Clearing Corporation November 2018 
  


---

## Page 2

  Copyright  
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  ii 
Copyright © 2018 by The Depository Trust & Clearing Corporation (“[[DTCC]]”). 
All rights reserved. This work (including, without limitation, all text, images, logos, compilation and design) is 
proprietary and protected by copyright, and is for the exclusive use of users authorized by [[DTCC]]. If this work is 
received from [[DTCC]] in any electronic medium, authorized users of this work are granted a limited, non-exclusive, 
non-transferable, non-sublicensable and freely revocable license to make reproductions and transmissions necessary 
for downloading and storage of this work on the users' computers and to print one or more paper copies from the 
electronic version for their own use. Other than to this limited extent, no part of this work (including any paper copies 
thereof or print versions thereof) may be printed, copied, altered, modified, posted, reproduced, displayed, published, 
sold, licensed, used or distributed (including by transmission) in any form or by any means, or stored in any 
information storage and retrieval system, without [[DTCC]]'s prior written permission.  
All product or service names are the property of their respective owners. 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
Doc Info: November, 2018 
Publication Code: SET 111 
Service: [[settlement]] / CF2/MQ Transmission Guides 
Title: 20.05 – MQ Drop Notification for [[DO]] and Pledge Function User's Guide 
 
 

---

## Page 3

  Document History  
 
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  iii 
 
Document History 
 
11/01/13 Revision – Added IMS TID for RAD Stage 3 target implementation 
12/01/13 Revision – Removed erroneous filler field in position 168 
01/01/14 Revision – Added RAD sequence number in position 116 
06/01/14 Revision – Amended RAD Sequence Number Field Name in position 116, IMS 
TID Field Name and Field Attributes in position 168), and Drop Pend Indicator 
Field Attributes in position 259. 
09/01/15 Revision – Added references to the current MQSeries IBM protocol and inserted 
the 74-character [[DTC]] MQ message data for output into the layout for positions 
1-74. 
Added MMI Finality Through Optimization Changes.  Added new Pend and Drop 
Reason indicators shown in Exhibits 1 - and 2. Added values for positions 185 
and 392 Drop Reason; and position 129 Drop [[DTC]] Original Record on ATP  for 
drop Dos and position 301 for drop pledge activity. 
03/10/16 Revision – Modified the field attributes in position 129 DROP-[[DTC]]-ORIG-REC#. 
11/30/2018 Removed formatting and references to old changes 
 
    

---

## Page 4

  Contents     
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  iv 
Contents 
Copyright .................................................................................................  Error! Bookmark not defined. 
Document History ............................................................................................................................. iii 
1. Overview ....................................................................................................................................5  
2. MQ Message Header ......................................................................................................................6  
2. Drop [[DO]] Output .........................................................................................................................7  
3. Drop Pledge' Activity ........................................................................................................................... 15 
3. Exhibit 1 - PEND Reason Indicators ..................................................................................................... 22 
3. Exhibit 2 - DROP Reason Indicators..................................................................................................... 22 
3. Exhibit 3 - DROP Code Indicators ........................................................................................................ 24 
 

---

## Page 5

     Overview      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  5 
1. Overview 
This document describes, specifically, the output requirements for obtaining Deliver Order Drop and 
Pledge Drop activity via [[DTC]]'s MQ system. 
The types of data available are: 
• Deliver Order Drops (DOD) types '026' thru '028', '046' thru '049' 
• Pledge Drops (PLD) Notification - Type '051', '054', '055', and '056'. 
 

---

## Page 6

     MQ Message Header      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  6 
2. MQ Message Header 
The fields in starting positions 01-74 make up the MQ message Header. 
Position Length Field Name Field Description 
01 02 Message Type ‘A1’ for  original messages 
‘R2’ for replayed messages 
03 02 Version Number Currently must be “01” 
05 06 Timestamp When message sent by [[DTCC]](HHMMSS) 
11 08 User [[ID]] User [[ID]] of message receiver 
19 02 Box# Box# associated with message 
21 23 Reserved Reserved for future use 
44 01 Response Code For replay only  
‘A’ = Accepted 
‘R’ =  Rejected 
45 02 Reason Code For replay only 
47 08 Control File 
Number 
Control File [[ID]] 
Control Number 
(YYYYDDDS) 
55 04 Message Count Currently  set to ‘0001’ 
59 08 Total Length of 
all messages 
(including the 
length field) 
Length of message(s) following the header 
67 08 Length of 
following 
message 
(including length 
field) 
Length of each message(s) including this field 
 
 

---

## Page 7

     Drop DOs      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  7 
3. Drop [[DO]] Output 
The format below is an example of a drop transaction. 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
Filler 75 02 For [[DTC]] internal use only 
Filler 77 01 Value space 
DEST-PARTIC-ACCOUNT 78 08 Individual [[participant]] # or group user # 
DEST-SYMBOL 86 02 Destination symbol – numeric 
Filler 88 01 Value '–' 
DEST-ACCOUNT-SEQ-# 89 06 Sequence # of the transaction unique —for 
each account destination 
TYPE-OF-08-RESPONSE 95 01 Value 'X' (DROP [[DO]]) 
[[DTC]]-SYS-ORIGIN-CODE 96 01 [[DTC]] System origination values: 
• 2 = CF2 
• 3 = [[PTS]] 
• 4 =[[ID]] 
• 5 = MQ 
• 0 = Other 
DROP-DELV-PART-NO 97 08 Deliverer's [[participant]] number 
DROP-COPY-IND  105  01 Values:  
Space = Original copy  
'Q' = Duplicate copy 
DROP-VERSION-CWTL-IND 106 01 Values: 
Space = current format 
DROP-[[CUSIP]]-NUMBER 107 09 [[CUSIP]] number 
DROP-RAD- 116   8 Unique RAD sequence number, assigned by 

---

## Page 8

     Drop DOs      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  8 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
SEQUENCE_NUMBER [[DTCC]] identifying this item 
FILLER 124 5 Value Spaces 
DROP-[[DTC]]-ORIG-REC# 
 
129 08 Pointer to the original [[DO]] record on the [[DTC]] 
central ATP data base 
00000000 for transactions in the MMI 
Staging Engine. 
DROP-ACCT-TYPE 137 03 Value '010' (General unpledged) 
Value '[[IPO]]' ([[IPO]] tracking) 
DROP-ACTION-CODE 140 01 Values: 
0 = No action • 
1 = Add if a '14', '27', '28' or 
 46'–'49' record 
2 = Subtract if a '14', '26',  
 '28' or '46'–'49' record 
DROP-ACTIVITY-CODE 141 03 Values: 
014 = Payor/Payee SPO or PPO 
026 = Deliver [[DO]] 
027 = Receive [[DO]] 
028 = Deliver/Receive for CP Maturity 
Presentment Drop 
046 = [[DO]] Partic-[[IPO]]-acct to the same Partic-
Free-acct 
047 = [[DO]] DLV-[[IPO]]-acct to RCV-[[IPO]]-acct. 
048 = [[DO]] DLV-[[IPO]]-acct to RCV-Free- acct. 
049 = [[DO]] DLV-Free-acct to RCV-[[IPO]]-acct. 
DROP-RECEIVING-PART. 144 08 Receiving [[participant]] number 

---

## Page 9

     Drop DOs      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  9 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
IMS TID 152 16 This is the number generated by [[DTC]] which 
uniquely identifies any transaction. 
Filler 168 1 Value spaces 
DROP-DOLLARS 169 13 Dollars involved in this transaction; PIC 
9(11)V9(2) 
DROP-DELV-RECV-IND 182 01 Shows which side the DROP is for. 
Values: 
‘D’ = For the Deliverer 
‘R’ = For the Receiver 
DROP-RAD-INDICATOR 183 01 Values:  
' ' = Did not process thru RAD 
‘'R' = Was processed thru RAD 
'M' = Was processed thru IRAD 
DROP-JOURNAL-CODE  184 01 Values: 
'0' = This is not a Journal 
'1' = This is a Journal 
DROP-REASON-CODE  185 01 [[DTC]]'s reason for this transaction being 
'pended' or 'dropped'. For list of possible 
PEND-REASON values see section 3. Exhibit 
1s. For a list of possible DROP-REASON 
values see section 3. Exhibit 2.   
DROP-DROP-CODE 186 01 [[DTC]]'S reason for this transaction being 
automatically 'dropped'. For a list of 
possible DROP-CODE values see section 3. 
Exhibit 3 - DROP Code Indicators 
DROP-ORIG-INPUT-SRCE 187 04 Originating system input source (Assigned 
by [[DTC]]) 

---

## Page 10

     Drop DOs      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  10 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
DROP-DELIVERER-ACCT-NO 191 17 Deliverer's account code 
DROP-RECEIVER-ACCT-NO 208 17 Receiver's account code 
DROP-SETTLE-BANK-ACCT-
# 
225 17 [[settlement]] Bank's Account Number 
DROP-TRADE-DATE 242 06 Trade date 
DROP-REASON-CODE 248 03 Reason code (numeric or S0-S9) 
 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
DROP-COND-[[DO]]-IND 251 01 Conditional [[DO]] Indicator 
DROP-THIRD-PARTY 252 06 Third party identifier 
Filler 258 01 Value spaces 
DROP-PEND-INDICATOR 259 01  Values: 
'P' = [[settlement]] (ATP) Drops/Cancels 
'U' = RAD Drops/Cancels 
DROP-DAY-NITE-IND 260 01 Values: 
' ' = SPO/PPO 
'D' = Day [[DO]]  
'N' = Night [[DO]] 
DROP-DATE  261 06 Date processed by MQ 
MMDDYY - When PEND-INDICATOR = 'P' 
YYMMDD - When PEND-INDICATOR = 'U' 
DROP-TIME 267 06 Time processed by MQ. 
Format = HHMMSS 

---

## Page 11

     Drop DOs      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  11 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
DROP-[[CUSIP]]-DESC 273 20 [[CUSIP]] Description 
DROP-COMMENTS  293 90 Comments  
(For [[IPO]] D0-Drops this field will contain 
'[[IPO]]-Cust-Intrnal-Acct #', '[[IPO]]-I.D.-Agt-Bk-
Identifier', and '[[IPO]]-Trade-Date' fields) 
DROP-MUNI-BOND-IND  383 01 Municipal Bond Indicator 
Values: 
'M' = Municipal Bond 
'B' = Other Bond 
' ' = Neither 
DROP-[[FAST]]-IND 384  01 [[FAST]] Indicator  
Values: 
'F' = [[FAST]]  
' ' = Other 
DROP-SDFS-IND 385 01  Same Day Funds Indicator  
Values:' 
'S' = Same Day Funds [[CUSIP]] 
'C' = Commercial Paper (SubI=525) 
'M' =Medium Term Note (SubI=530) 
' ' = Other 
DROP-TRANS-SEQ-NO 386 05 Transaction sequence number 
DROP-CANCEL-TYPE  
(SDFS-RAD system only)  
391 01 Values: 
'C' = Cancel by Receiver 
'D' = Cancel by Deliverer 
' ' = Unapproved 

---

## Page 12

     Drop DOs      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  12 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
DROP-REASON-IND 
(NDFS/SDFS-ATP System 
only) 
 
392 01 Values: 
' ' = Prevent-PEND [[Option]] exercised 
'A' = Delivering [[participant]] has insufficient 
position for C.P. 
'C' = Delivering [[participant]] has insufficient 
[[collateral]] 
'D' = Receiving [[participant]] debit cap reached 
'F' = Dropped for FIFO processing 
'O' = Receiving [[participant]] has insufficient 
[[collateral]] 
'S' = Delivering [[participant]] has insufficient 
position 
‘T’ = Pending MMI Funding Decision 
‘W’ = Pending MMI Optimization 
DROP-FOSP-IND 393 01 Values: 
'0' = Security is not eligible for Foreign  
 Ordinary [[shares]] Processing 
'1' = Security is eligible for Foreign  
 Ordinary [[shares]] Processing 
DROP-SHARE-QTY-NEW 394 09 Share quantity (new format where 1=1 
for all issues) 
Filler 403 02 Value spaces 

---

## Page 13

     Drop DOs      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  13 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
DROP-SUBISSUE-TYPE 405 03 Sub-Issue type for SDFS CUSIPs 
Values: '000' = NOT APPLICABLE 
'030' = LIMITED PARTNRSHIP 
'040' = CMO in units  
'041' = [[ABS]] in units  
'042' = ISSUE in units  
'110' = [[ADR]] 
'120' = PFD-CP  
'320' = MUNI VRDO/CP  
'330' = MUNI CP 
'340' = BEARER/ZERO CPN 
'502' = BA'S  
'504' = CD'S  
'505' = CERTFD MMI 
'506' = CERTFD MMI-PER. 
'525' = CORPORATE CP 
'526' = CORP. VRDO/CP 
'530' = MTN'S 
'531' = Deposit Notes 
'532' = M/T Bank Notes 
'533' = MMI MTNs 
'540' = CMO 
'541' = [[ABS]] 
'542' = Non-CMO/[[ABS]] 
'550' = S/T Bank Notes 
'551' = ZERO COUPON 
'560' = DISCOUNT NOTES 

---

## Page 14

     Drop DOs      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  14 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
DROP-CUSTOMER-
INTERNAL-ACCOUNT–
NUMBER 
408 12 Present if [[CUSIP]] is [[IPO]]-tracked 
Format = alphanumeric 
DROP-[[ID]]-AGENT-BANK- 
IDENTIFIER 
420  08 Optional. If present, Customer Internal 
Account-# must be present. 
Format = alphanumeric 
DROP-TRADE-DATE  428 08 Optional. If present, I.D. Agent Bank 
Identifier must be present. 
Format = MMDDCCYY 
DROP-DIS-TRAN# 436 12 (For Depository use only) 
Filler 448 03 Value spaces. 
 
 

---

## Page 15

     Drop Pledge Activity      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  15 
 
3.1 Drop Pledge' Activity 
Refer to section 2. MQ Message Header to see the fields in starting positions 01-74 that make up the 
MQ message Header which must precede the pledge drop transactions. 
 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
Filler 75 02 For [[DTC]] internal use only 
Filler 77 01 Value space  
Dest-Partic-Account 78 08  Individual [[participant]] # or group user # 
Dest-Symbol 86 02 Destination symbol – numeric 
Filler 88 01 Value '–' 
Dest-Account-Seq-# 89 06 Sequence # of the transaction, unique for 
each account destination 
Type-Of-08-Response 95 01 Value 'Y' (Drop Pledge) 
[[DTC]]-SYS-Origin-Code 96 01 [[DTC]] system origination 
Values: 
• 2 = CF2 
• 3 = [[PTS]] 
• 4 = [[ID]] 
• 5 = MQ 
• O = Other 
P-Drop-Pledgor-Part-No 97 08 Pledgor's [[participant]] number 
P-Drop-Copy-Ind  105 01 Value: 
Space = Original copy 
'Q' = Duplicate copy 
Filler 106 01 Value space 

---

## Page 16

     Drop Pledge Activity      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  16 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
P-Drop-[[CUSIP]]-Number 107 09 [[CUSIP]] number 
 P-DROP-RAD-
SEQUENCE-NUMBER 
116 8 Unique RAD sequence number, assigned by 
[[DTCC]] identifying this item 
Filler 124 13 Value spaces 
P-Drop-Acct-Type 
  
137 03 Values: 
'010' = Pledge 
'014' = Return 
'[[IPO]]' =[[IPO]] 
P-Drop-Action-Code 140 01 Values:  
0 = No action 
1 = Add if this is a '55' or '56' record 
2 = Subtract if this is '50', '51', '52' or '54' 
record 
P-Drop-Activity-Code 141 03 Values: 
'050' = Free pledge from [[IPO]] a/c 
'051' = pledge – Free 
'052' = Valued pledge from [[IPO]] a/c  
'054' = Pledge – Valued 
'055' = Return – Valued 
'056' = Return – Free 
P-Drop-Pledgee-Part-# 144 08 Pledgee [[participant]] number (or zeros if none 
exists) 
Filler 152 06 Value spaces 
P-Drop-[[shares]] 158 09 Number of [[shares]] involved in this transaction 
Filler 167 02 Value spaces 

---

## Page 17

     Drop Pledge Activity      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  17 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
P-Drop-Dollars 169 13 Dollars involved in this transaction; PIC 
9(11)V9(2) 
Filler 182 01 Value spaces 
P-Drop-RAD-Ind 183 01 Values: 
' ' = Did not process thru RAD 
'R' = Was processed thru RAD 
P-Drop-Journal-Code 184 01  Values: 
 0 = This is not a Journal 
 1 = This is a Journal 
Filler 185 01 Value space 
P-Drop-SDFS-Ind 186 01 Same Day Funds Indicator 
Values: 
'S' = Same Day Funds [[CUSIP]] 
'C' = Commercial Paper (SubI=525) 
'M' = Medium Term Note (SubI=530) 
' ' = Other 
Filler 187 02 Value spaces 
P-Drop-Loan-Date 189 06 Pledge loan date 
Filler 195 02 Value spaces 
P-Drop-Date 197 06 Date processed by MQ 
MMDDYY - When RAD-INDICATOR = ' ' 
YMMDD - When RAD-INDICATOR = 'R' or 'M' 
Filler 203 02 Value spaces 
P-Drop-Time 205 06 Time processed by MQ (HHMMSS) 

---

## Page 18

     Drop Pledge Activity      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  18 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
P-Drop-[[CUSIP]]-Desc 211 20 [[CUSIP]] description 
P-Drop-Comments 231 56 Comments: (Available only on RAD drops) 
P-Drop-Muni-Bond-Ind 287 01 Municipal bond indicator  
Values: 
'M' = Municipal bond 
'B' = Other bond 
' ' = Neither 
P-Drop-[[FAST]]-Ind 288 01 [[FAST]] Indicator 
Values: 
'F' = [[FAST]] 
' ' = Other 
P-Drop-Loan-Rel-Type 289 01 Values: '1' thru '4' 
P-Drop-Loan-Hypothcat'n 290 01 Values: Space, and '1' thru '3' 
Filler 291 02 Value spaces 
P-Drop-Trans-Seq-No 293 05 Transaction sequence number (Available only 
on RAD drops) 
Filler 298 01 Value space 
P-Drop-Cancel-Type 
(SDFS-RAD system only) 
299 01 Values:  
'C' = Cancel by receiver 
'D' = Cancel by deliverer 
' ' = Unapproved (or dropped in ATP) 
Filler 300 01 Value space 

---

## Page 19

     Drop Pledge Activity      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  19 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
P-Drop-Reason-Ind 301 01 Values: 
' ' = Prevent-Pend [[Option]] exercised (or 
dropped in RAD system) 
'A' = Delivering [[participant]] has insufficient 
position for C.P. 
'C' = Delivering [[participant]] has insufficient 
[[collateral]] 
'D' = Receiving [[participant]] debit cap reached 
'F' = Fended for FIFO processing 
'0' = Receiving [[participant]] has insufficient 
[[collateral]] 
'S' = Delivering [[participant]] has insufficient 
position 
‘T’ = Pending MMI Funding Decision 
‘W’ = Pending MMI Optimization 
Filler 302 01 Value space 
P-Drop-Plg-Bank-# 303 08 Pledgee bank number 
Filler 311 01 Value spaces 
P-DROP-[[shares]]-NEW 312 09 Share quantity (new format where 1 = 1 for 
all issues) 
Filler 321 02 Value spaces 

---

## Page 20

     Drop Pledge Activity      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  20 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
P-DROP-SUBISSUE-TYPE 323 03 Sub-Issue type for SDFS CUSIPS 
Values:  
• '000' = NOT APPLICABLE 
• '030' = LIMITED PARTNRSHP 
• '040' = CMO in units 
• '041' = [[ABS]] in units 
• '042' = ISSUE in units 
• '110' = [[ADR]] 
• '120' = PFD-CP 
• '320' = MUNI VRDO/CP 
• '330' = MUNI CP 
• '340' = BEARER/ZERO CPN 
• '502' = BA's 
• '504' = CD's  
• '505' = CERTFD MMI 
• '506' = CERTFD MMI-PER. 
• '525' = CORPORATE CP 
• '526' = CORP. VRDO/CP 
• '530' = MTN's 
• '531' = Deposit notes 
• '532' = M/T bank notes 
• '533' = MMI MTN's 
• '540' = CMO 
• '541' = [[ABS]] 
• '542' = Non-CMO/[[ABS]] 
• '550' = S/T Bank notes 
• '551' = ZERO COUPON 
• '560' = DISCOUNT NOTES 
Filler 326 02 Value spaces 
P-Drop-Maturity-Date 328 06 Maturity date for C.P. CUSIPS 
Filler 334 02 Value spaces 
P-Drop-ATORIGSC 336 04 Pledge/Release origin-source 
P-Drop-PTA-Indicator 340 01 Possible values: 'Y', 'N' or ' ' 

---

## Page 21

     Drop Pledge Activity      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  21 
 
Field Name 
 
Position 
 
Length 
 
Field Attributes 
P-DROP-FOSP-IND 341 01 Foreign Ordinary [[securities]] Indicator: 
'0' = Security is not eligible for Foreign 
Ordinary [[securities]] Processing 
'1' = Security is eligible for Foreign Ordinary 
[[securities]] Processing 
P-DROP-IMS-TID 342 16 This is the number generated by [[DTC]] which 
uniquely identifies any transaction. 
Filler 358 93 Value spaces 
 
 
 

---

## Page 22

     Pend and Drop Reason Codes      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  22 
 
 
3. Exhibit 1 - PEND Reason Indicators 
Code Meaning 
' ' Not 'pended' 
'N' Pended for receiver's [[collateral]] deficiency 
'S' Pended for [[shares]] 
'O' Pended for receiver's [[collateral]] deficiency 
'C' Pended for deliverer's [[collateral]] deficiency 
'D' Pended for receiver's debit deficiency 
'E' Pended for deliverer's debit deficiency 
'A' Pended for deliverer insufficient position 
'B' Pended for receiver insufficient position 
'P' Pended for deliverer insufficient pledged position 
'F' Pended for FIFO processing 
‘T’ Pending for MMI Funding Decision 
 
3. Exhibit 2 - DROP Reason Indicators 
Code Meaning 
' ' If [[DO]]-OUT-[[DTC]]-STATUS-IND = 'D' please refer to Exhibit 
21c on the next page. Otherwise this was not 'dropped'. 
'I' Dropped for receiver's [[collateral]] deficiency 

---

## Page 23

     Pend and Drop Reason Codes      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  23 
Code Meaning 
'S' Dropped for [[shares]] 
'O' Dropped for receiver's [[collateral]] deficiency 
'C' Dropped for deliverer's [[collateral]] deficiency 
'E' Dropped for deliverer's debit deficiency 
'A' Dropped for deliverer insufficient position 
'B' Dropped for receiver insufficient petition 
'P' Dropped for deliverer insufficient pledged position 
'J' Dropped when deliverer's [[settlement]] bank unavailable 
'N' Dropped when receiver's [[settlement]] bank unavailable 
'M' Dropped when the market value exceeded 
'V' Dropped when [[collateral]] monitor value exceeded 
'L' Dropped when deliverer's debit cap limit reached 
'R' Dropped when receiver's debit cap limit reached 
'D' Dropped when the adjustable debit cap exceeded 
'Z' Dropped when PEND (recycle) cutoff was taken at the 
other depository 
‘T’ Dropped due to MMI Refusal to Pay (permanent only) 
Temporary will not generate a message 
‘W’ Dropped from MMI Optimizer at cutoff. 
‘X’ Dropped due to MMI Edit Reject. 

---

## Page 24

     Pend and Drop Reason Codes      
20.05 MQ System User Guide for Drop Notification Output (For Deliver Order and Pledge Activity)  24 
 
3. Exhibit 3 - DROP Code Indicators 
Code Meaning 
' ' Not dropped 
'C' PEND (recycle) cutoff taken at [[DTC]] 
'S' No short available for [[CNS]] transactions 
'A' [[shares]] are not pendable 
'T' [[collateral]] monitor is not pendable 
'D' Debit is not pendable 
'X' Unknown reason 
 
 