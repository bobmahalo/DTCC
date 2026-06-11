---
title: "20.02 MQ Payment Order Output (For SPO, PPO AND ACATS PO)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_Payment_Order_Output_20_02.pdf"
pages: 18
size: "1569.2 KB"
category: "Connectivity_MQ"
ingested_on: "2026-06-05"
---

# 20.02 MQ Payment Order Output (For SPO, PPO AND ACATS PO)

**Original File:** [MQ_Payment_Order_Output_20_02.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_Payment_Order_Output_20_02.pdf)  
**Category:** Connectivity_MQ  
**Total Pages:** 18  
**File Size:** 1569.2 KB  

---

## Page 1

MQ TRANSMISSION USER GUIDES 
20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
JUNE 2, 2022 
[[DTCC]] Public (White)

---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
 
Doc Date: JUNE 2, 2022 
Publication Code: SET 159 
Service: [[settlement]]/CF2/MQ Transmission Guides 
Title: 20.02 MQ Payment Order Output (For SPO, PPO AND ACATS PO) 
 
[[DTCC]] Public (White)

---

## Page 3

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
 
I. Overview 3 
TABLE OF CONTENTS 
I. Overview ............................................................................................................................................................ 4 
II. MQ Message Header ........................................................................................................................................ 5 
III. MQ SPO Output ............................................................................................................................................... 6 
IV. MQ PPO Output ............................................................................................................................................ 10 
V. MQ ACAT Payment Order ............................................................................................................................. 13 
VI. Release Notes ............................................................................................................................................... 17 
 
 
 
[[DTCC]] Public (White)

---

## Page 4

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
 
I. Overview 4 
I. OVERVIEW 
MQ Payment Order Output provides clients their Security Payment Order (SPO), [[Premium]] Payment Order (PPO) 
and ACAT Payment Order transactions that have been processed by [[DTC]]’s [[settlement]] system during the 
business day.  
The types of Payment Order data available are: 
Payment Order (PO) Types SPO '078', PPO '082' and ACATS Payment Order '079'. 
Each record corresponds to a Payment Order transaction which has updated a client’s account balance.  
 
[[DTCC]] Public (White)

---

## Page 5

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
II. MQ Message Header 5 
II. MQ MESSAGE HEADER 
The fields starting in positions 01-74 make up the MQ message header. Following this MQ-header will be the 
standard Message Delivery header (20 bytes) followed by the application data (starting in position 95).  
Position Length Field Name Field Description 
01 02 Message Type ‘A1’ for original messages 
‘R2’ for replayed messages 
03 02 Version Number Currently must be “01” 
05 06 Timestamp When message sent by [[DTCC]](HHMMSS) 
11 08 User [[ID]] User [[ID]] of message receiver 
19 02 Box# Box# associated with message 
21 23 Reserved Reserved for future use 
44 01 Response Code For replay only 
‘A’ = Accepted 
‘R’ = Rejected 
45 02 Reason Code For replay only 
47 08 Control File Number Control File [[ID]] Control Number (YYYYDDDS) 
55 04 Message Count Currently set to ‘00 01’ 
59 08 Total Length of all 
messages (including 
the length field) 
Length of message(s) following the header 
67 08 Length of following 
message (including 
length field) 
Length of each message(s) including this field 
75 02 Filler For [[DTC]] internal use only 
77 01 Filler Value space 
78 08 DEST-PARTIC-
ACCOUNT 
Individual [[participant]] # or Group User # 
86 02 DEST-SYMBOL Destination Symbol-Numeric 
88 01 Filler Value '-' 
89 06 DEST-ACCOUNT-
SEQ-# 
Sequence of the transaction unique for each account 
destination 
 
[[DTCC]] Public (White)

---

## Page 6

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
III. MQ SPO Output 6 
III. MQ SPO OUTPUT 
The following is the record format of an SPO transaction. 
The fields starting in positions 01-74 make up the MQ message header. Following this MQ-header will be the 
standard Message Delivery header (20 bytes) followed by the application data (starting in position 95). 
Refer to the MQ Message Header section for more information. 
Field Name Pos Len Field Attributes 
TYPE-OF-08-RESPONSE 95 01 Value 'P' (PO data) 
[[DTC]]-SYS-ORIGIN-CODE 96 01 [[DTC]] system origination 
Values: 
2 = CF2 
3 = [[PTS]] 
4 = [[ID]] 
5 = MQ 
0 = Other 
[[DTC]]-SYS-ACTIVITY-CODE 97 03 Value '078' (Security Payment Order) 
SPO-OUT-PAYEE-NUMBER 100 08 [[participant]] number of the payee 
SPO-OUT-COPY-IND 108 01 Values: 
Space = Original copy (Payor) 
'Q' = Duplicate copy (Payor) 
'E' = Original copy (Payee) 
Filler 109 01 Value space 
SPO-OUT-[[CUSIP]]-NUMBER 110 09 [[CUSIP]] number 
SPO-OUT-PAYOR-NUMBER 119 08 [[participant]] number of the payor 
Filler 127 02 Value spaces 
SPO-OUT-SHARE-QUANTITY 129 07 Share quantity 
Filler 136 02 Value spaces 
SPO-OUT-MONEY-AMOUNT 138 12 Dollars and cents value of the payment (decimal point 
assumed). 
PIC 9(10)V9(2) 
Filler 150 02 Value spaces 
[[DTCC]] Public (White)

---

## Page 7

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
III. MQ SPO Output 7 
Field Name Pos Len Field Attributes 
SPO-OUT-REASON-CODE 152 02 Reason code: 
'S0' = Mark to market/[[Stock]] loan 
'S1' = Mark to market/[[Stock]] loan reclaim 
'S2' = Due bill redemptions 
'S3' = Due bill redemptions reclaim 
'S4' = Mark to market/fail 
'S5' = Mark to market/fail reclaim 
'S6' = Buy in/[[pair off]] 
'S7' = Buy in/[[pair off]] reclaim 
'S8' = Fail [[pair off]] 
'S9' = Fail [[pair off]] reclaim 
Note: 
The following 10 fields correspond exactly to the 10 
fields above. The only difference is that the following 
codes are internally generated within [[DTC]] and may not 
be used by a [[participant]] in a '05' data transmission 
block to [[DTC]]. 
'SA' = Mark to market/[[Stock]] loan 
'SB' = Mark to market/[[Stock]] loan reclaim 
'SC' = Due bill redemptions 
'SD' = Due bill redemptions/reclaim 
'SE' = Mark to market/fail Note: Use for [[SFT]] Payment 
Differentials.  
'SF' = Mark to market/fail reclaim 
'SG' = Buy in/[[pair off]] 
'SH' = Buy in/[[pair off]] reclaim 
'SI' = Fail [[pair off]] 
'SJ' = Fail [[pair off]] reclaim 
SPO-OUT- NEW-PRICE 154 07 New price ($/¢) of share value (decimal point is 
assumed). 
PIC 9(5)V9(2) 
Filler 161 02 Value spaces 
SPO-OUT-OLD-PRICE 163 07 Old price ($/¢) of share value (decimal point is 
assumed). 
PIC 9(5)V9(2) 
Filler 170 02 Value spaces 
SPO-OUT-ADJUSTMENTS 172 10 Adjustment figure ($/¢) (decimal point is assumed). 
PIC 9(8)V9(2) 
Filler 182 02 Value spaces 
[[DTCC]] Public (White)

---

## Page 8

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
III. MQ SPO Output 8 
Field Name Pos Len Field Attributes 
SPO-OUT-CONTRACT-DATE 184 06 Contract date (MMDDYY format) 
SPO-OUT-PAYEE-REP-NAME 190 30 Representative's name of the payee 
SPO-OUT-PAYEE-REP-PHONE 220 10 Representative's phone number of the payee 
SPO-OUT-PAYOR-REP-NAME 230 30 Representative's name of the payor 
SPO-OUT-PAYOR-REP-PHONE 260 10 Representative's phone number of the payor 
SPO-OUT-COMMENTS 270 60 Comments 
SPO-OUT-[[settlement]]-DATE 330 06 [[settlement]] Date-MMDDYY format 
SPO-OUT-PAYABLE-DATE 336 06 Payable Date-MMDDYY format 
SPO-OUT-RECORD-DATE 342 06 Record Date-MMDDYY format 
SPO-OUT-[[CUSIP]]-DESC 348 20 [[CUSIP]] description 
SPO-OUT-TIME-STAMP 368 06 Time at which the SPO was processed at [[DTC]] in 
HHMMSS format 
Filler 374 1 Value space 
SPO-OUT-[[DTC]]-RBN-REC# 375 8 Pointer to this record on the [[DTC]] Central ATP data 
base 
Filler 383 13 Value spaces 
SPO-OUT-MUNI/BOND-IND 396 01 Muni or regular bond indicator values: 
'B' = Regular bond 
'M' = Muni bond 
' ' = [[Stock]] (non-bond) 
SPO-OUT-ATP-STATUS 397 01 Values: 
'M' = Make 
'P' = Pending (SDFS only) 
'E' = Error 
SPO-OUT-SDFS-IND 398 01 Same Day Funds System [[CUSIP]] involved. 
Values: 
'S' = SDFS 
'C' = Commercial paper (SubI=525) 
'M' = Medium term note (SubI=530) 
' ' = Non-SDFS 
Filler 399 01 Value space 
SPO-OUT-SHARE-PTY-NEW 400 09 Share quantity (new format where 1 = 1 for all issues) 
Filler 409 02 Value space 
[[DTCC]] Public (White)

---

## Page 9

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
III. MQ SPO Output 9 
Field Name Pos Len Field Attributes 
SPO-OUT-SUBISSUE-TYPE 411 03 Sub-issue type for SDFS Cusips. 
Values: 
'000' = NOT APPLICABLE 
'030' = LMTD PARTNRSHP 
'040' = CMO in units 
'041' = [[ABS]] in units 
'042' = ISSUE in units 
'110' = [[ADR]] 
'120' = PFD-CP 
'320' = MUNI VRDO/CP 
'330' = MUNI CP 
'340' = BEARER/ZERO CPN 
'502' = BAs 
'504' =CDs 
'505' = CERTFD MMI 
'506' = CTFD MMI-PER. 
'525' = CORPORATE CP 
'526' = CORP. VRDO/CP 
'530' = MTNs 
'531' = Deposit notes 
'532' = M/T bank notes 
'533' = MMI MTNs 
'540' = CMO 
'541' = [[ABS]] 
'542' = NON-CMO/[[ABS]] 
'550' = S/T bank notes 
'551' = ZERO COUPON 
'560' = DISCOUNT NOTES 
RAD Sequence Number 414 08 This field is the IMS TID displayed in the “non-
displayable character” version. This is the current 
format used in RAD output. 
IMS TID 422 16 This is the number generated by [[DTC]] which uniquely 
identifies any transaction. 
Filler 438 13 Value spaces 
 
 
[[DTCC]] Public (White)

---

## Page 10

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
IV. MQ PPO Output 10 
IV. MQ PPO OUTPUT 
The following is the record format of a PPO transaction. 
The fields starting in positions 01-74 make up the MQ message header. Following this MQ header will be the 
standard Message Delivery header (20 bytes) followed by the application data (starting in position 95).  Refer to 
the MQ Message Header section for more information. 
Field Name Pos Len Field Attributes 
TYPE-OF-08-RESPONSE 95 01 Value 'P' (PO data) 
[[DTC]]-SYSTEM-ORIGIN-CODE 96 01 System at [[DTC]] through which the participants 
originally sent in the data: 
2 = CF2 
3 = [[PTS]] 
4 = [[ID]] 
5 = MQ 
0 = Other 
[[DTC]]-SYS-ACTIVITY-CODE 97 03 Value '082' (PPO) 
PPO-OUT-PAYEE-NUMBER 100 08 [[participant]] number of the payee 
PPO-OUT-COPY-IND 108 01 Values: 
Space = Original copy (payor) 
'Q' = Duplicate copy (payor) 
'E' = Original copy (payee) 
Filler 109 12 Value spaces 
PPO-OUT-PAYOR-NUMBER 121 08 [[participant]] number of the payor 
Filler 129 02 Value spaces 
PPO-OUT-RECEIPT-RELEASE 131 01 Values: 
'1' = Receipt 
'2' = Release 
PPO-OUT-PUT-CALL 132 01 Values: 
'1' = Put 
‘2’ = Call 
PPO-OUT-MONEY-AMOUNT 133 12 Dollar and cents value of the payment (decimal point is 
assumed). PIC 9(10)V9(2) 
Filler 145 02 Value spaces 
[[DTCC]] Public (White)

---

## Page 11

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
IV. MQ PPO Output 11 
PPO-OUT-REASON-CODE 147 02 Values: 
'P0' = Put 
'P1' = Put reclaim 
'P2' = Call 
'P3' = Call reclaim 
Note: 
The following four fields correspond exactly to the four 
fields above. The only difference is that the following 
codes are internally generated within [[DTC]] and may not 
be used by a [[participant]] in a '05' data transmission 
block to [[DTC]]. 
'P4' = Put 
'P5' = Put reclaim 
'P6' = Call 
'P7' = Call reclaim 
Filler 149 09 Value spaces 
PPO-OUT-LINE-NUMBER 158 02 Line number 
PPO-OUT-XREF-DATE 160 06 Cross reference date (MMDDYY format) 
PPO-OUT-NUMBER-CONTRACTS 166 05 Number of contracts 
PPO-OUT-SERIAL-NUMBER 171 09 Serial number 
PPO-OUT-BANK-NAME 180 30 Bank name 
PPO-OUT-OCC-NAME 210 20 OCC [[Member]] name 
Filler 230 1 Value space 
PPO-OUT-[[DTC]]-RBN-REC# 231 8 Pointer to this record on the [[DTC]] Central ATP data 
base 
Filler 239 1 Value space 
PPO-OUT-PAYEE-REP-NAME 240 30 Representative's name of the payee 
PPD-OUT-PAYEE-REP-PHONE 270 10 Representative's phone number of the payee 
PPO-OUT-PAYOR-REP-NAME 280 30 Representative's name of the payor 
PPO-OUT-PAYOR-REP-PHONE 310 10 Representative's phone number of the payor 
PPO-OUT-COMMENTS 320 60 Comments 
PPO-OUT-[[CUSIP]]-NO 380 09 [[CUSIP]] number 
PPO-OUT-TIME-STAMP 389 06 Time that PPO was processed at [[DTC]]-HHMMSS 
format 
Filler 395 01 Value space 
PPO-OUT-MUNI-BOND-IND 396 01 Muni or regular bond indicator values: 
[[DTCC]] Public (White)

---

## Page 12

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
IV. MQ PPO Output 12 
'B' = Regular bond 
'M' = Muni bond 
' ' = [[Stock]] (non-bond) 
PPO-OUT-ATP-STATUS 397 01 Values: 
'M' = Made 
'E' = Edit Error 
PPO-OUT-SDFS-IND 398 01 Same Day Funds System [[CUSIP]] involved. 
Values: 
'S' = SDFS 
'C' = Commercial paper (SubI=525) 
'M' = Medium term note (SubI=530) 
' ' = Non-SDFS 
PPO-OUT-[[Option]]-SYMBOL-EXT 399 06 [[Option]] symbol extended (previously referred to as 
“Trading Symbol”) 
Note: 
This field was extended, as a result of the Options 
Symbology Initiative (OSI). 
PPO-OUT-EXPIRATION-DATE-EXT 405 08 Contract's expiration date (YYYYMMDD) 
extended 
Note: 
This field was extended, as a result of the Options 
Symbology Initiative (OSI). 
PPO-OUT-EXERCISE-PRICE-EXT 413 12 Exercise price ($/¢) of [[shares]] extended 
(decimal point is assumed). PIC 9(6)V9(6) 
Note: 
This field was extended, as a result of the Options 
Symbology Initiative (OSI) 
RAD Sequence Number 425 08 This field is the IMS TID displayed in the “non-
displayable character” version. This is the current 
format used in RAD output. 
IMS TID 433 16 This is the number generated by [[DTC]] which uniquely 
identifies any transaction. 
Filler 449 2 Value space 
 
[[DTCC]] Public (White)

---

## Page 13

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
V. MQ ACAT Payment Order 13 
V. MQ ACAT PAYMENT ORDER 
The following is the record format of an ACAT Payment Order transaction. 
The fields starting in positions 01-74 make up the MQ Message Header. Following this MQ-header will be the 
standard Message Delivery header (20 bytes) followed by the application data (starting in position 95).  
Refer to the MQ Message Header section for more information. 
Field Name Pos Len Field Attributes 
TYPE-OF-08-RESPONSE 95 01 Value 'P' (PO data) 
[[DTC]]-SYS-ORIGIN-CODE 96 01 [[DTC]] System origination 
Values: 
2 = CF2 
3 = [[PTS]] 
4 = [[ID]] 
S = MQ 
0 =Other 
[[DTC]]-SYS-ACTIVITY-CODE 97 03 Value '079' (ACAT Payment Order) 
ACAT-OUT-PAYEE-NUMBER 100 08 [[participant]] number of the payee. 
ACAT-OUT-COPY-IND 108 01 Values: 
Space = Original copy (Payor) 
'Q' = Duplicate copy (Payor) 
'E' = Original copy (Payee) 
Filler 109 01 Value space 
ACAT-OUT-[[CUSIP]]-NUMBER 110 09 [[CUSIP]] number 
ACAT-OUT-PAYOR-NUMBER 119 08 [[participant]] number of the payor 
Filler 127 01 Value spaces 
ACAT-OUT-SHARE-QUANTITY 128 09 Share quantity 
Filler 137 02 Value spaces 
ACAT-OUT-MONEY-AMOUNT 139 12 Dollars and cents value of the payment (decimal point 
assumed). 
PIC 9(10)V9(2) 
Filler 151 03 Value spaces 
ACAT-OUT-REASON-CODE 154 03 Reason code: '791' 
Filler 157 01 Value space 
ACAT-OUT-ACT-CODE 158 01 Action code : '+' or '–' 
[[DTCC]] Public (White)

---

## Page 14

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
V. MQ ACAT Payment Order 14 
Field Name Pos Len Field Attributes 
ACAT-OUT-JRNL-CODE 159 01 Journal code: 'O', 'N' or 'S' 
ACAT-OUT-PEND-RSN 160 01 Reason for pend: 
' ' = no pend 
'C' = for major [[collateral]] 
'O' = for minor [[collateral]] 
'G' = for pledgee [[collateral]] 
'D' = for minor net debit 
'E' = for major net debit 
'H' = for pledgee net debit 
'A' = for major other NA 
'B' = for minor other NA 
'P' = for major other NA 
'S' = for insufficient [[shares]] 
Filler 161 01 Value space 
ACAT-ORIGIN-SOURCE 162 04 Value 'PCAT' 
ACAT-STATUS-CODE 166 01 Possible values: 
'P' = pending 
'M' = made 
'D' = drop 
ACAT-OUT-COMMENTS 167 210 Comments: 
pos. 12-31 = orig. rcvr. cust. # 
pos. 42-55 = ACAT cntl. # 
pos. 65-70 = [[Asset]] seq. # pos.  
78-79 = rsn. code = A0 pos.  
91-94 = orig. rcvr. corresp. 
pos. 107-126 = orig. dlv. cust. # 
pos. 137-140 = original receiver 
pos. 152-155 = original deliverer 
pos. 179-187 = orig. rcvr. cust. primary soc. [[SEC]]. # 
pos. 202-210 = orig. rcvr. cust. secondary soc. [[SEC]]. # 
Filler 377 01 Value space 
ACAT-DUE-BILL-IND 378 01 Possible values: 
'Y' = due-bill 
'N' = No due-bill 
' ' = No due-bill 
ACAT-CMO-FACTOR 379 14 CMO factor 
Format = 9(2)V9(12) 
[[DTCC]] Public (White)

---

## Page 15

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
V. MQ ACAT Payment Order 15 
Field Name Pos Len Field Attributes 
ACAT-3RD-PARTY-[[ID]] 393 06 Third party identifier 
ACAT-OUT-[[CUSIP]]-DESC 399 20 [[CUSIP]] description 
ACAT-PROCESS-DATE 419 08 Format = CCYYMMDD 
Filler 427 1 Value space 
ACAT-PROCESS-TIME 428 06 Time that transaction was processed at [[DTC]]-
HHMMSS format 
Filler 434 1 Value space 
ACAT-OUT-[[DTC]]-RBN-REC# 435 8 Pointer to this record on the [[DTC]] Central ATP data 
base 
Filler 443 01 Value space 
ACAT-MUNI/BOND-IND 444 01 Muni or regular bond indicator values: 
'B' = Regular bond 
'M' = Muni bond 
' ' = [[Stock]] (non-bond) 
ACAT-OUT-SDFS-IND 445 01 Same Day Funds System [[CUSIP]] involved. 
Values: 
'S' = SDFS 
'C' = Commercial paper (SubI=525) 
'M' = Medium term note (SubI=530) 
' ' = Non-SDFS 
ACAT-SUBISSUE-TYPE 446 03 Sub-issue type for SDFS Cusips. 
Values: 
'000' = NOT APPLICABLE 
'030' = LMTD PARTNRSHP 
'040' = CMO in units 
'041' = [[ABS]] in units 
'042' = ISSUE in units 
'110' = [[ADR]] 
'120' = PFD-CP 
'320' = MUNI VRDO/CP 
'330' = MUNI CP 
'340' = BEARER/ZERO CPN 
'502' = BAs 
'504' = CDs 
'505' = CERTFD MMI 
'506' = CTFD MMI-PER. 
'525' = CORPORATE CP 
'526' = CORP. VRDO/CP 
[[DTCC]] Public (White)

---

## Page 16

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
V. MQ ACAT Payment Order 16 
Field Name Pos Len Field Attributes 
'530' = MTNs 
'531' = Deposit notes 
'532' = M/T bank notes 
'533' = MMI MTNs 
'540' = CMO 
'541' = [[ABS]] 
'542' = NON-CMO/[[ABS]] 
'550' = S/T bank notes 
'551' = ZERO COUPON 
'560' = DISCOUNT NOTES 
RAD Sequence Number/(IMS TID) 449 08 This field is the IMS TID displayed in the “non-
displayable character” version. This is the current 
format used in RAD output. 
Filler 457 08 Reserved for Future Use 
 
 
[[DTCC]] Public (White)

---

## Page 17

20.02 MQ PAYMENT ORDER OUTPUT (FOR SPO, PPO AND ACATS PO) 
VI. Release Notes 17 
VI. RELEASE NOTES 
This is the document history reflecting changes to the file. 
06/02/2022 The following changes were made to bring this document up to current standards:  
• For [[SFT]] POs, updated position 152 SPO-OUT-REASON-CODE field with the [[SFT]] 
Price Differential PO Reason code ‘SE’ - Mark to market/fail. 
• Made general updates to remove outdated references and reformat the document.  
o  R emoved references to MDH retired technology and updated to reflect the 
MQ header format used currently. 
o The fields starting in positions 01-74 make up the MQ message header. 
Following this MQ-header will be the standard Message Delivery header (20 
bytes) followed by the application data (starting in position 95). 
• In MQ PPO Output, we redesignated several fields as filler to account for fields 
which are no longer used. 
o W e combined positions 109, 110, 115, and 119 into a single 12 length filler 
field because the following fields are no longer used: PPO-OUT-
TRADING-SYMBOL position 110 length 05 and PPO-OUT-EXPIRATION-
DATE position 115 length 04. Position 119 length 2 is already filler. Thus, 
we combined all four fields into one filler field. 
o A filler field in position 149 changed from 2 to 9 in length. The following 
field was redesignated as filler because it is no longer used: PPO-OUT-
EXERCISE-PRICE position 156 length 02. Thus, we combined position 
149 and 156 into a single 9 length filler field 
11/30/2018 Removed formatting and references to old changes. 
08/01/2013 Amended RAD Zero dates for RAD Stage 3 (Figures 7-9 Data Response Blocks for SPO, 
PPO, and ACAT respectively). 
03/01/2013 [[settlement]] Matching Updates for RAD Stage 3 (Figures 7-9 Data Response Blocks for SPO, 
PPO, and ACAT respectively). 
02/01/2010 For the Options Symbology Initiative (OSI), effective February 2010, [[DTC]] took existing 
filler, beginning on position 399 and ending on position 424, and used it for the extended 
format of the fields affected by OSI. 
 
 
[[DTCC]] Public (White)

---

## Page 18

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] at: 
DTCSupport@[[DTCC]].com 
or visit us on the web at: 
http://www.[[DTCC]].com/client-center  
[[DTCC]] Public (White)