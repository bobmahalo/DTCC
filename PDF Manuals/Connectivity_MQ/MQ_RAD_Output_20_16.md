---
title: "20.16 MQ RAD Output Function User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_RAD_Output_20_16.pdf"
pages: 13
size: "223.7 KB"
category: "Connectivity_MQ"
ingested_on: "2026-06-05"
---

# 20.16 MQ RAD Output Function User Guide

**Original File:** [MQ_RAD_Output_20_16.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_RAD_Output_20_16.pdf)  
**Category:** Connectivity_MQ  
**Total Pages:** 13  
**File Size:** 223.7 KB  

---

## Page 1

  
 
 
[[settlement]] 
20.16-MQ RAD OUTPUT FUNCTION USER GUIDE 
 
NOVEMBER 26, 2018 
 


---

## Page 2

20.16-MQ RAD Output Function User Guide 
 
 4 
 
 
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
 
 
Doc Info: November 26, 2018 
Publication Code: SET 110 
Service: [[settlement]] / CF2/MQ Transmission Guides 
Title: 20.16 - MQ RAD Output Function User’s Guide 
 

---

## Page 3

20.16-MQ RAD Output Function User Guide 
 
Document History 4 
 
 
DOCUMENT HISTORY 
03/01/2013 Added [[settlement]] Matching detail (pages 4 & 6). 
 
08/01/2013 Updated [[settlement]] Matching dates (pages 4 & 6) and added “Transaction Type 
Indicator” 4 (page 6). 
 
11/30/2018 Removed formatting and references to old changes 
 

---

## Page 4

20.16-MQ RAD Output Function User Guide 
 
Contents 5 
 
 
CONTENTS 
Document History ......................................................................................................................... iv 
Introduction to Receiver Authorized Delivery ............................................................................6  
Cutoff Times ............................................................................................................................................ 6 
Rad Output Transaction ........................................................................................................................ 7 

---

## Page 5

20.16-MQ RAD Output Function User Guide 
 
Introduction to Receiver Authorized Delivery 6 
 
 
INTRODUCTION TO RECEIVER AUTHORIZED DELIVERY 
RAD allows you to review and either approve or cancel incoming deliveries before they are processed so you 
can avoid reclamations. 
You can route the following transaction types through RAD: 
• Deliver Orders (DOs) 
• Payment Orders (POs) 
• Valued pledges 
• Valued releases 
 
Cutoff Times 
RAD output is generated real-time when a transaction is sent to RAD. For [[ID]] trades and NDOs (night deliver 
orders), transactions are sent to RAD in the night cycle. 
For day transactions, the cutoff times are: 
• Valued MMI Issuances–2:45 p.m. 
• Valued [[DO]]/PO/Pledges–3:30 p.m. 
• [[DO]] to Settling Bank–5:00 p.m. 
• Free DOs–6:15 p.m. 

---

## Page 6

20.16-MQ RAD Output Function User Guide 
 
Rad Output Transaction 7 
 
 
RAD OUTPUT TRANSACTION 
This output provides the user with notification messages for transactions subject to RAD  processing. 
The First 74 bytes of the transaction comprises the MQ header. The next 20 bytes comprises the Message 
prefix. The remaining bytes comprise the actual data transaction. 
Field name Pos Length Field Attributes 
Message Header 1-74 74 74 byte MQ Header. See MQ User Guide. 
Filler 75 1 VALUE SPACE 
Message Flag 76 1 ‘O’: current day original message 
 
‘R’: current day reprint 
 
‘U’: current day requested out-of- sequence 
 
‘Y’: prior day 
Filler 77 1 Value space 
DESTINATION [[participant]] 
ACCOUNT 
78 8 Individual [[participant]] Number or Group 
User Number 
DESTINATION-SYMBOL 86 2 DESTINATION Symbol-Numeric 
Filler 88 1 Value ‘-’ 
DESTINATION ACCOUNT SEQUENCE 
NUMBER 
89 6 Sequence number of the transaction –unique for 
each account destination 
TYPE-OF-08-RESPONSE 95 1 Value ‘R’ (RAD Data) 
RAD-ORIGIN-CODE 96 1 [[DTC]] System Origination Codes: 
 
- 2 = [[CCF]] 
 
- 3 = [[PTS]]/[[PBS]]/[[settlement]] Web 
 
- 4 = [[ID]] 
 
- 5 = MQH 
 
- 0 = Other 
DELIVERING [[participant]] NUMBER 97 8 Delivering [[participant]] Number 
Filler 105 2 Value Spaces 

---

## Page 7

20.16-MQ RAD Output Function User Guide 
 
Rad Output Transaction 8 
 
 
Field name Pos Length Field Attributes 
[[CUSIP]] NUMBER 107 9 [[CUSIP]] Number 
Filler 116 1 Value space 
RECEIVING [[participant]] NUMBER 117 8 Receiving [[participant]] Number 
RAD AUTH. RECORD TYPE 125 1 Type of RAD processing: 
 
‘R’ = Regular RAD 
 
‘M’ = MMI Index-to-Principal RAD 
Intended Delivery Date 
 
 
126 5 The date the transaction is scheduled for 
processing.  ‘Julian’ date format. 
[[settlement]] Date 
 
 
131 5 The intended [[settlement]] date of the transaction. 
‘Julian’ date format. 
Filler 
 
 
136 1 [[DTC]] use only–reserved for future use 
DOLLAR AMOUNT 137 13 Dollars and cents value of the trade PIC 9(11)V9(2) 
RAD-VERSION-CONTROL 
(Formerly : ‘filler’) 
150 01 Value ‘ ‘ = current format 
RAD-DLV-RCV-INDICATOR 151 1 Value ‘D’ or ‘R’. 
REASON-CODE 152 3 Reason Code 
RAD SEQUENCE NUMBER 155 8 Unique sequence number, assigned by [[DTC]], 
identifying this item. 
RAD INPUT SOURCE [[ID]] 163 4 Input source of the original RAD transaction. 
RAD PROCESSING PERIOD 167 2 Possible values: 
 
P1 = Valued [[DO]] (Non-Settling Bank) 
P2 = Valued [[DO]] (Settling Bank) 
P3 = Free [[DO]] 

---

## Page 8

20.16-MQ RAD Output Function User Guide 
 
Rad Output Transaction 9 
 
 
Field name Pos Length Field Attributes 
ACTIVITY CODE 169 3 Activity Code Values: 
 
- ‘014’ = SPO 
 
- ‘026’ = [[DO]] Delivery 
 
- ‘027’ = [[DO]] Receive 
 
- ‘046’ = [[DO]] [[participant]]-[[IPO]]-acct to the same 
[[participant]]-Free-acct 
 
- ‘047’ = [[DO]] DLV-[[IPO]]-acct to RCV-[[IPO]]-acct. 
 
- ‘048’ = [[DO]] DLV-[[IPO]]-acct to RCV-Free-acct. 
 
- ‘049’ = [[DO]] DLV-Free-acct to RCV-[[IPO]]-acct. 
 
- ‘052’ = Valued Pledge from [[IPO]] acct. 
 
- ‘054’ = Valued Pledge 
 
- ‘055’ = Valued Release-Return 
RAD ACTION CODE 172 1 Action Code Values: 
 
- ‘W’ = Waiting for Approval or Cancellation 
 
- ‘A’ = Approved 
 
- ‘R’ = Cancelled by Receiver 
 
- ‘D’ = Cancelled by Deliverer 
 
- ‘E’ = Exempted by  Receiver 

---

## Page 9

20.16-MQ RAD Output Function User Guide 
 
Rad Output Transaction 10 
 
 
Field name Pos Length Field Attributes 
Transaction Type Indicator 173 1 ‘1’–Affirmed Institutional Transaction ([[ID]]) 
‘2’–Future Dated Deliver Orders, e.g., NDOs 
‘3’–Other (Same Day Transactions, e.g., [[DO]], PO, 
Pledge) 
‘4’–[[ID]] Net 
COMMENTS 
(from original transaction) 
174 307 Positions: 
1–74 : Special A/C # Info. 
 
75–79 : MQ Seq # of Original [[DO]] (if available) 
 
80 : Space 
 
81–307 : Delivering [[participant]]’s Remarks 
 
If Deliver Order was generated from an Issuance 
Instruction: 
 
1–57 : Special Issuance Information 
 
58–62 : MQ Seq # of Original [[DO]] (if available) 
 
63–307 : Remarks from Original Issuance Instruction 
REASON FOR CANCEL (Line-2) 481 13 (See position 495 below) 
Filler 494 1 Value Space 
REASON FOR CANCEL (Line-1) 495 13 Supplied by the party who is cancelling the 
transaction 
Filler 508 1 Value Space 
RAD AUTHORIZATION DATE 509 5 ‘Julian’ date. This field must be sent back on all 
‘approval’ or ‘cancellation’ records. 
Filler 514 1 Value Spaces 
RAD-MUNI-BOND-IND 515 1 ‘Muni’ or ‘Regular’ Bond Indicator values: 
 
‘B’ = Regular Bond 
 
‘M’ = Muni-Bond 
 
‘ ‘ = [[Stock]] (non-bond) 
Filler 516 01 Value Spaces 

---

## Page 10

20.16-MQ RAD Output Function User Guide 
 
Rad Output Transaction 11 
 
 
Field name Pos Length Field Attributes 
RAD-SHARE-QTY-NEW 517 09 Share quantity (new format where 1 = 1 for all 
issues) 
Filler 526 02 Value Spaces 

---

## Page 11

20.16-MQ RAD Output Function User Guide 
 
Rad Output Transaction 12 
 
 
RAD-SUBISSUE-TYPE 528 03 Sub-Issue type for SDFS Cusips. 
 
Values: ‘000’ = NOT APPLICABLE 
 
‘030’ = LMTD PARTNRSHP 
 
‘040’ = CMO-UNITS 
 
‘041’ = [[ABS]]-UNITS 
 
‘042’ = ISSUE-UNITS 
 
‘110’ = [[ADR]] 
 
‘120’ = PFD-CP 
 
‘320’ = MUNI VRDO/CP 
 
‘330’ = MUNI CP 
 
‘340’ = BEARER-ZERO CPN 
 
‘502’ = BA’S 
 
‘504’ = CD’S 
 
‘505’ = CERTIFIED MMI 
 
‘506’ = CERTFIED MMI- PERIODIC 
 
‘525’ = CORPORATE CP 
 
‘526’ = CORP. VRDO/CP 
 
‘530’ = MTN’S (repl. By 533) 
 
‘531’ = Deposit Notes 
 
‘532’ = M/T Bank Notes 
 
‘533’ = MMI MTN’s 

---

## Page 12

20.16-MQ RAD Output Function User Guide 
 
Rad Output Transaction 13 
 
 
Field name Pos Length Field Attributes 
 
‘540’ = CMO 
 
‘541’ = [[ABS]] 
 
‘542’ = NON-CMO/[[ABS]] AMORTIZ. 
 
‘550’ = S/T Bank Notes 
 
‘551’ = Zero CPN./INIT PRINC 
 
‘560’ = MMI DISCOUNT NOTE 
RAD-[[CUSIP]]-DESC 531 20 [[CUSIP]] Description 
RAD-MATURITY-DATE 551 08 Maturity date for a BOND issue. 
Format = CCYYMMDD 
RAD-DATED-DATE 559 08 Dated-date for a BOND issue. Format = ccyymmdd 
Filler 567 04 Value spaces. 
 
  

---

## Page 13

20.16-MQ RAD Output Function User Guide 
 
Rad Output Transaction 14 
 
 
 
 
FOR MORE INFORMATION 
 
Email Core Learning Service at: 
DTCSupport@[[DTCC]].com 
or visit us on the web at: 
http://www.[[DTCC]].com/client-center 