---
title: "MQ Deliver Order Output (Both Day and Night Activity) (20.01) "
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_Deliver_Order_Output_20_01.pdf"
pages: 26
size: "2047.9 KB"
category: "Connectivity_MQ"
ingested_on: "2026-06-05"
---

# MQ Deliver Order Output (Both Day and Night Activity) (20.01) 

**Original File:** [MQ_Deliver_Order_Output_20_01.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_Deliver_Order_Output_20_01.pdf)  
**Category:** Connectivity_MQ  
**Total Pages:** 26  
**File Size:** 2047.9 KB  

---

## Page 1

MQ TRANSMISSION USER GUIDES 
20.01 MQ DELIVER ORDER OUTPUT (DAY AND NIGHT ACTIVITY) 
J
UNE 2, 2022 
[[DTCC]] Public (White)

---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
 
Doc Date: June 2, 2022 
Publication Code: SET 158 
Service: [[settlement]]/CF2/MQ Transmission Guides 
Title: 20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
 
[[DTCC]] Public (White)

---

## Page 3

 
 
TABLE OF CONTENTS 
I. Overview ............................................................................................................................................................ 4 
II. MQ M essage Header ....................................................................................................................................... 5 
III. MQ [[DO]] Output ................................................................................................................................................. 7 
Exhibit 1- PEND Reason Indicators .................................................................................................................. 21 
Exhibit 2 - DROP Reason Indicators................................................................................................................. 22 
Exhibit 3 - DROP Code Indicators..................................................................................................................... 24 
Release Notes ..................................................................................................................................................... 25 
 
[[DTCC]] Public (White)

---

## Page 4

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
I. Overview 4 
I. OVERVIEW 
This document describes, specifically, the output requirements for Deliver Order activity processing via MQ. 
The types of Deliver Order ([[DO]]) data available are types '026' through '028' and '046' through '049'. 
 
 
[[DTCC]] Public (White)

---

## Page 5

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
II. MQ Message Header 5 
II. MQ MESSAGE HEADER 
The fields starting in positions 01-74 make up the MQ message header.  Following this MQ-header will be the 
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
47 08 Control File 
Number 
Control File [[ID]] Control Number (YYYYDDDS) 
55 04 Message Count Currently set to ‘00 01’ 
59 08 Total Length of all 
messages (including the 
length field) 
Length of message(s) following the header 
67 08 Length of following 
message (including 
length field) 
Length of each message(s) including this field 
75 02 02 Filler For [[DTC]] internal use only 
77 01 Filler Value space 
78 08 DEST-PARTIC- 
ACCOUNT 
Individual [[participant]] # or Group User # 
86 02 DEST-SYMBOL Destination Symbol - Numeric 
[[DTCC]] Public (White)

---

## Page 6

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
II. MQ Message Header 6 
Position Length Field Name Field Description 
88 01 Filler Value '-' 
89 06 DEST-ACCOUNT-SEQ-# Sequence of the transaction unique for each account destination 
 
 
 
[[DTCC]] Public (White)

---

## Page 7

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 7 
III. MQ [[DO]] OUTPUT 
The following is the record format for a deliver order transaction. 
 
Field Name Position Length Field Attributes 
TYPE-OF-08- RESPONSE 95 01 Value 'D' ([[DO]] data) 
[[DO]]-OUT-ORIGIN- CODE 96 01 [[DTC]] System origination code. Values: 
2 = CF2 
3 = [[PTS]] 
4 = [[ID]] 
5 = MQ 
0 = Other 
[[DO]]-OUT-DLV-PART- NUM 97 08 Delivering [[participant]] number 
 
 
 
 
 
[[DTCC]] Public (White)

---

## Page 8

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 8 
 
Field Name Position Length Field Attributes 
[[DO]]-OUT-COPY-IND 105 01 Values: 
Space = Original copy 
'Q' = Duplicate copy 
[[DO]]-OUT-VERSION- 
CONTROL 
(Formerly : 'filler') 
106 01 Value '1' = [[IPO]] Tracking (560) Value '2' = FED/GNMA 
fields (724) 
[[DO]]-OUT-[[CUSIP]] 107 09 [[CUSIP]] number 
[[DO]]-OUT-CMO- FACTOR 116 14 CMO Factor 
Format 9(2)V9(12) 
[[DO]]-OUT-RSN-FOR- 
PEND-IND 
130 01 Values: 
'-' No Pend 
'A' = Delivering [[participant]] has insufficient position for C.P. 
'C' = Delivering [[participant]] has insufficient [[collateral]] 
'D' = Receiving [[participant]] debit cap reached 
'F' = Pending for FIFO processing 
'O' = Receiving [[participant]] has insufficient [[collateral]] 
'S' = Delivering [[participant]] has insufficient position 
‘T’ = Pending Funding Decision 
‘W’ = Pending MMI Optimization 
[[DO]]-OUT-MQ-TIME 131 06 Time when MQ processed the record to the output queue 
(HHMMSS format) 
  
[[DTCC]] Public (White)

---

## Page 9

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 9 
Field Name Position Length Field Attributes 
[[DO]]-OUT-ACCOUNT- 
TYPE 
137 03 Account type. 
Value: '010' (General unpledged) Value: '[[IPO]]' ([[IPO]] 
Tracking) 
[[DO]]-OUT-ACTION- CODE 140 01 Action Code. Values: 
'0': No action. 
'1': Add to account if Activity Code is '27,' 
'28' or 
'46' '49' 
'2': Subtract from account if Activity Code is 
'26,'.'28,' '46' '49' 
[[DO]]-OUT-ACTIVITY- 
CODE 
141 03 Activity Code. Values: 
'026' = [[DO]] Delivery 
'027' = [[DO]] Receive 
'028' = [[DO]] Deliver/Receive for CP Maturity 
Presentment 
'046' = [[DO]] Partic-[[IPO]]-acct to the same 
Partic-Free- acct 
'047' = [[DO]] DLV-[[IPO]]-acct to RCV-[[IPO]]-acct 
'048' = [[DO]] DLV-[[IPO]]-acct to RCV-Free-acct 
'049' = [[DO]] DLV-Free-acct to RCV-[[IPO]]-acct 
[[DO]]-OUT-RCV-PART- 
NUM 
144 08 Receiving [[participant]] number 
(Zeros if activity-code = '46') 
[[DO]]-OUT-PTA-IND 152 01 Pending transaction indicator. Permissible values: 
'N' = No Position has been reserved for 
'pending' Deliver Orders 
'Y' = Position has been reserved for 
'pending' Deliver Orders 
Blank = [[default]] to 'no' 
  
[[DTCC]] Public (White)

---

## Page 10

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 10 
Field Name Position Length Field Attributes 
[[DO]]-OUT-FOSP-IND 153 01 Values: 
'0' = Security is not eligible for Foreign 
Ordinary [[shares]] Processing 
'1' = Security is eligible for Foreign Ordinary 
[[shares]] Processing 
[[DO]]-OUT-ORIG-INPUT- 
SRCE (Was: [[DO]]- TRADE-
DATE) 
154 04 Originating system input source (assigned by 
D.T.C.) 
[[DO]]-OUT-MATURITY- 
DATE 
158 08 Maturity date for a BOND issue. Format 
CCYYMMDD 
[[DO]]-OUT-SUBACT- CODE 166 03 Sub-activity code. Values: 
'100' = MMI Reorg Presentment 
'926' = [[DO]]/PO Matched Reclaim 
[[DO]]-OUT-MONEY- VALUE 169 13 Dollars and cents value of the trade 
(decimal point is assumed). PIC 9(11)V9(2) 
[[DO]]-OUT-DELV-RECV- 
IND 
182 01 Shows which side the [[DO]] is for. Values: 
'D' = For the Deliverer 
'R' = For the Receiver 
  
[[DTCC]] Public (White)

---

## Page 11

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 11 
Field Name Position Length Field Attributes 
[[DO]]-OUT-RAD- 
INDICATOR 
183 01 Values: 
' ' = Did not process thru RAD 
'R' = Was processed thru RAD 
[[DO]]-OUT-JOURNAL- 
CODE 
184 01 Journal code 
Values: 
'0' = Non-journal 
'1' = Journal 
[[DO]]-OUT-BATCH-VAR- 
CON 
185 06 Defines the source of input to [[DTC]] (internal code). 
[[DO]]-OUT-DLV- 
ACCOUNT-NUM 
191 17 Deliverer's account number 
[[DO]]-OUT-RCV- 
ACCOUNT-NUM 
208 17 Receiver's account number 
[[DO]]-OUT-SUB-BANK- 
ACCT-NUM 
225 17 Subordinate Bank's account number 
[[DO]]-OUT-SETTLE-DATE 242 06 [[settlement]] Date (MMDDYY format) 
[[DO]]-OUT-REASON- 
CODE 
248 03 Reason Code 
Note: for the [[SFT]] Clearing initiative: 
[[SFT]] [[Stock]] Loans = Reason code “200” 
[[SFT]] [[Stock]] Loan Return =  Reason code “201.” 
 
[[DO]]-OUT-COND-[[DO]]- [[ID]]-
IND 
251 01 Conditional [[DO]]/[[ID]] indicator. Values: 
'C' = Conditional [[DO]] 
'R' = Conditional [[DO]] Return 
'I' = [[Institutional Delivery]] [[DO]] 
[[DTCC]] Public (White)

---

## Page 12

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 12 
 
 
Field Name Position Length Field Attributes 
[[DO]]-OUT-THIRD- PARTY-
[[ID]] 
252 06 Third Party Identifier 
[[DO]]-OUT-DUE-BILL- IND 258 01 Due-Bill Indicator values: 
'Y' = Due-Bill 
'N' = No Due-Bill 
' ' No Due-Bill ([[ID]]-originated) 
[[DO]]-OUT-[[DTC]]- STATUS-
IND (Was: [[DO]]-OUT-
PEND-IND) 
259 01 [[DO]] [[DTC]] Processing Status Values: 
' ' = [[DO]] 'made' 
'P' = [[DO]] 'pending' (recycling) 
'X' = [[DO]] 'made' after originally 'pending' 
'C' = [[CNS]] Deliver [[DO]] 'drop', that is, Reclaim due to 
overage 
'D' = SDFS Prevent-Pend Drop 
'K' = 'Kill' of Pending [[DO]] 
‘T’ = Pending Funding Decision 
‘W’ = Pending MMI Optimization 
‘Q’ = ‘Kill’ of Transaction Pending in Staging 
Area 
‘E’ = Edit Reject in ATP 
Note: For SDFS CUSIPS, depositories receive 
'R's for re-pended items. 
[[DO]]-OUT-DAY-NIGHT- 
IND 
260 01 [[DO]] 'day' or 'night' indicator 
Values: 
'D' = Day [[DO]] 
'N' = Night [[DO]] 
[[DO]]-OUT-DATE- STAMP 261 06 Date that the [[DO]] was updated at [[DTC]] (MMDDYY 
format) 
  
[[DTCC]] Public (White)

---

## Page 13

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 13 
Field Name Position Length Field Attributes 
[[DO]]-OUT-TIME-STAMP 267 06 Time that the [[DO]] was updated by ATP at 
[[DTC]] (HHMMSS format) 
[[DO]]-OUT-[[CUSIP]]-DESC 273 20 [[CUSIP]] description 
[[DO]]-OUT-COMMENTS 293 210 Comments 
For Night [[ID]] DOs: Pos. 1 - 17 = Filler 
Pos. 18 - 26 = Confirm Number 
Pos. 27 - 94 = Filler 
Pos. 95 - 106 = Agent Acct. # 
Pos. 107- 174 = Filler 
Pos. 175- 186 = Bkr Dir # 
Pos. 187- 210 = Filler 
 
For Night [[ID]] Dos submitted by other depositories 
(#6942/6070): 
Pos. 1 - 156 = Filler 
Pos. 157- 165 = Confirm Number 
Pos. 166 - 210 = Filler 
 
For non-[[ID]] DOs submitted by other depositories 
(#6942/6070): 
Pos. 1 - 80 = User's comments 
Pos. 81 - 87 = Fi ller 
Pos. 88 - 99 = Dep-Trans-# 
Pos. 100- 107 = Filler 
Pos. l08 - 108 = Dep-Trade-Type 
Pos. 109 - 210 = Filler 
  
[[DTCC]] Public (White)

---

## Page 14

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 14 
Field Name Position Length Field Attributes 
    
For [[DO]]'s with [[IPO]] CUSIPS: 
Pos. 1 - 135 = User's comments 
Pos. 136- 210 = Filler 
 
For [[Direct Registration]] ([[DRS]]) Dos submitted by 
transfer agents: 
Pos. 1 - 13 = Transaction [[ID]] 
Pos. 14 - 15 = Filler 
Pos. 16 - 52 = Partic. A/C # 
Pos. 53 - 54 = Filler 
Pos. 55 = Reason Code 
Pos. 56 - 57 = Filler 
Pos. 58 - 67 = Process Date 
Pos. 68 - 69 = Filler 
Pos. 70 = Value '1' 
Pos. 71 - 110 = [[participant]] or Corresp. Name 
Pos. 111- 112 = Filler 
Pos. 113- 123 = Soc. Secur. # 
Pos. 124- 139 = F iller 
Pos. 140 = Value '2' 
Pos. 141- 175 = [[DRS]] Registr. 
Pos. 176- 209 = Filler 
Pos. 210 = Value '3' 
 
For [[DO]]’s from FED/GNMA project; 
Pos. 1 - 180 = User's comments 
Pos. 181- 210 = FED rej. Reason 
 
Note: 
For DOs related to [[SFT]], bytes 1-80 are used for 
comments. These must be left justified and followed 
by the exact 14-digit UTC Loan [[ID]]. 
 
  
[[DTCC]] Public (White)

---

## Page 15

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 15 
 
Field Name Position Length Field Attributes 
[[DO]]-OUT-MUNI-BOND 503 01 'Muni' or 'Bond' [[CUSIP]] involved. Value: 
'B' = Bond 
'M' = Muni 
Space = Regular Security 
[[DO]]-OUT-[[FAST]]-IND 504 01 '[[FAST]]' [[CUSIP]] involved. Value: 
'F' = [[FAST]] 
Space = Non-[[FAST]] 
[[DO]]-OUT-SDFS-IND 505 01 'Same Day Funds System' [[CUSIP]] involved. Value: 
'S' = SDFS 
'C' = Commercial Paper (SubI=525) 
'M' = Medium Term Note (SubI=530)  
Space = Non-SDFS 
[[DO]]-OUT-TRANS-SEQ# 506 05 User-assigned seq # of input [[DO]] 
transaction. This will contain spaces if this is a 
Code '28' (CP Maturity Sweep) generated [[DO]]. 
[[DO]]-OUT-[[DTC]]-CURR- 
REC# 
511 08 Pointer to this record on the [[DTC]] central 
ATP data base. 
‘00000000’ (8 zeros) for transactions in the 
Staging Engine and MMI Optimizer 
[[DO]]-OUT-REPEND- INDIC 519 01 If transaction is 'pending': 
' R' = repended 
' ' = not repended 
  
[[DTCC]] Public (White)

---

## Page 16

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 16 
 
Field Name Position Length Field Attributes 
[[DO]]-OUT-SHARE-QTY- 
NEW 
520 09 Share quantity. Numeric right-justified. (where 1 = 1 
for all issues). 
[[DO]]-OUT-PEND-DROP- 
REASON 
529 01 [[DTC]]'s reason for this transaction being 
'pended' or 'dropped.' For a list of possible PEND-
REASON values see Exhibit 1. For a list of possible 
DROP- REASON values see Exhibit 2. 
[[DO]]-OUT-DROP-CODE 530 01 [[DTC]]'s reason for this transaction being 
automatically 'dropped.' For a list of possible 
DROP- CODE values see Exhibit 3. 
[[DO]]-OUT-SUBISSUE- 
TYPE 
531 03 Sub-Issue type for SDFS CUSIPs. Values: 
'000' = Not applicable 
'030' = LIMTD PARTNRSHP 
'040' = CMO in Units 
'041' = [[ABS]] in Units 
'042' = ISSUE in Units 
'110' = [[ADR]] 
'120' = PFD-CP 
'320' = MUNI VRDO/CP 
'330' = MUNI VRDO/CP 
'340' = BEARER/Zero Cpn 
'502' = BAs 
'504' = CDs 
'505' = CERTIFIED MMI 
'506' = CERTFD MMI-Periodic 
'525' = CORPORATE CP 
  
[[DTCC]] Public (White)

---

## Page 17

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 17 
Field Name Position Length Field Attributes 
   '526' = CORP. VRDO/CP 
'530' = MTN's (repl. by 533) 
'531' = Deposit Notes 
'532' = M/T Bank Notes 
'533' = MMI MTNs 
'540' = CMO 
'541' = ABC 
'542' = Non-CMO/[[ABS]] Amort. 
'550' = S/T Bank Notes 
'551' = ZERO COUPON 
'560' = DISCOUNT NOTES 
 
[[DO]]-OUT-[[CNS]]-SUB- 
ACCT 
534 01  
Describe processing of [[CNS]]-receives. 
Values: 
'A' = Trading account 
'C' = [[Stock]] Loan acct 
'E' = Fully-paid acct 
'G' = Reorg account 
'H' = Reorg account (for competing offers or 
election mergers) 
“S” = [[CNS]] ACATS Short Cover 
“R” = [[CNS]] ACATS Long Allocation 
 
[[DO]]-OUT-PEND-POS- 
NEW NUMBER 
535 09  
Available share position  (where 
1=1 for all issues) on pended DOs 
(deliverers only) 
<Spaces> if the transaction is in the Staging 
Engine/MMI Optimizer 
Format = alphanumeric 
  
[[DTCC]] Public (White)

---

## Page 18

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 18 
Field Name Position Length Field Attributes 
[[DO]]-OUT-[[IPO]]-[[ID]]-AGT- 
BANK IDENTIFIER 
(This field will contain 
data only if the [[DO]]- OUT-
VERSION = '1') 
564 08 Present if [[CUSIP]] is [[IPO]]-tracked and either party is 
a Bank. 
Format = alphanumeric 
[[DO]]-OUT-[[IPO]]-TRADE- 
DATE 
572 08 Present if [[CUSIP]] is [[IPO]]-tracked and either party is 
a Bank. 
Format = MMDDCCYY 
[[DO]]-OUT-[[IPO]]-BROKR- 
INTRNL ACCOUNT- 
NUMBER 
580 12 Optional 
Format = alphanumeric 
[[DO]]-OUT-[[IPO]]- 
CORRESPONDNT 
ACCOUNT-NUMBER 
(AKA: EXECUTING- BKR-
#) 
592 08 Present if [[CUSIP]] is [[IPO]]-tracked and submitting 
party is clearing for executing [[Broker]]. 
Format = numeric, right-aligned/lead zeros 
[[DO]]-OUT-[[IPO]] BUY- SELL 600 01 Present if [[CUSIP]] is [[IPO]]-tracked BUY/SELL 
indicator. Values: ‘B’ = Buy,   ‘S’ = Sell  
Filler 601 03 Value spaces 
[[DO]]-OUT-[[DTC]]-ORIG- 
REC# 
604 08 Pointer to the prior record for this transaction. This 
field will contain data if TRANS-STATUS is 'P' 
(Pend), 'X' (Make-after- Pend), or 'K' (Pend-Kill). 
Also present if this transaction is a 'reclaim' of a 
prior Deliver Order. 
[[DO]]-OUT-RECLAIM- 
DATE Format = MMDDYY 
612 06 Contains the original date of the [[DO]] that is being 
reclaimed when this TRANS-STATUS is 
' ' or 'X.' 
  
[[DTCC]] Public (White)

---

## Page 19

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 19 
Field Name Position Length Field Attributes 
[[DO]]-OUT-DIS-TRANS-# 618 12 Contains the Depository transaction number 
(optional) that is involved in this trade. 
Filler 630 01 Value spaces. 
***EXPANSION*** 631 164 Following fields available for FED/GNMA 
project 
(output version ind. = 2) 
[[DO]]-OUT-FED-ABA- ACCT 631 09 The bank acct. Identifier for the FED [[participant]] 
(req’d when the Delvr or Rcvr is the FED acct 
(6072)). 
[[DO]]-OUT-FED-SUB- 
ACCT 
640 20 The bank Sub acct. Identifier for the FED [[participant]] 
(req’d when the Delvr or Rcvr is the FED acct 
(6072)). 
[[DO]]-OUT-3RDPTY- DLV-
TEXT 
660 40 The Third-party deliverer text/acct information. 
[[DO]]-OUT-3RDPTY- REC-
TEXT 
700 40 The Third-party receiver text/acct information. 
Filler 740 9 Value spaces 
IMS TID 
(Stage 3 change targeted 
for June 
2014) 
749 16 This is the number generated by [[DTC]] which 
uniquely identifies any transaction. (Available in 
Version 2 only) 
RAD Sequence 
Number 
(Stage 3 change targeted 
for June 
2014) 
765 8 This field is the IMS TID displayed in the “non-
displayable character” version. This is the current 
format used in RAD output (Available in Version 2 
only) 
  
[[DTCC]] Public (White)

---

## Page 20

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
III. MQ [[DO]] Output 20 
Field Name Position Length Field Attributes 
IDNETOUT Output 
Subscription Indicator 
(Stage 3 change targeted 
for June 
2014) 
773 1 Contains “1” if originated from IDNETOUTPUT 
subscription, and a space “ “ from all other output 
types 
Filler 774 21 Value Spaces 
 
 
[[DTCC]] Public (White)

---

## Page 21

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
Exhibit 1- PEND Reason Indicators 21 
EXHIBIT 1- PEND REASON INDICATORS 
 
Code Meaning 
' ' Not 'pended' 
'N' Pended for Receiver's [[collateral]] deficiency 
'S' Pended for [[shares]] 
'O' Pended for Receiver's [[collateral]] deficiency 
'C' Pended for Deliverer's [[collateral]] deficiency 
'D Pended for Receiver's debit deficiency 
'E' Pended for Deliverer's debit deficiency 
'A' Pended for Deliverer insufficient position 
'B' Pended for Receiver insufficient position 
'P' Pended for Deliverer insufficient pledged position 
'F' Pended for FIFO processing 
‘T’ Pending for Funding Decision 
 
 
 
[[DTCC]] Public (White)

---

## Page 22

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
Exhibit 2 - DROP Reason Indicators 22 
EXHIBIT 2 - DROP REASON INDICATORS 
 
Code Meaning 
' ' If [[DO]]-OUT-[[DTC]]-STATUS-IND = 'D', please refer to Exhibit 
3 following. Otherwise, this was not 'dropped.' 
'I' Dropped for Receiver's [[collateral]] deficiency 
'S' Dropped for [[shares]] 
'0' Dropped for Receiver's [[collateral]] deficiency 
'C' Dropped for Deliverer's [[collateral]] deficiency 
'E' Dropped for Deliverer's debit deficiency 
'A' Dropped for Deliverer insufficient position 
'B' Dropped for Receiver insufficient position 
'P' Dropped for Deliverer Insufficient Pledged position 
'J' Dropped when Deliverer's [[settlement]] bank unavailable 
'N' Dropped when Receiver's [[settlement]] bank unavailable 
'M' Dropped when the market value is exceeded 
'V' Dropped when [[collateral]] monitor value is exceeded 
'L' Dropped when Deliverer's debit cap limit is reached 
'R' Dropped when Receiver's debit cap limit is reached 
'D' Dropped when the adjustable debit cap is exceeded 
  
[[DTCC]] Public (White)

---

## Page 23

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
Exhibit 2 - DROP Reason Indicators 23 
Code Meaning 
'Z' Dropped when PEND (recycle) cutoff was taken at the other Depository 
‘T’ Dropped due to Refusal to Pay (permanent only) Temporary will not 
generate a message 
‘W’ Dropped from MMI Optimizer at cutoff. 
‘X’ Dropped due to Edit Reject 
 
[[DTCC]] Public (White)

---

## Page 24

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
Exhibit 3 - DROP Code Indicators 24 
EXHIBIT 3 - DROP CODE INDICATORS 
 
Code Meaning 
' ' Not dropped 
'C' PEND (recycle) cutoff taken at [[DTC]] 
'S' No short available for [[CNS]] transactions 
'A' [[shares]] are not pendable 
'T' [[collateral]] monitor is not pendable 
'D' Debit is not pendable 
'X' Unknown 
 
  
[[DTCC]] Public (White)

---

## Page 25

20.01 MQ DELIVER ORDER OUTPUT (Day and Night Activity) 
Release Notes 25 
RELEASE NOTES 
This is the document history reflecting changes to the file. 
06/02/2022 For position 248 [[DO]]-OUT-REASON-CODE field added note in documentation that [[SFT]] 
Clearing DOs use [[Stock]] Loan Reason code “200” and [[SFT]] [[Stock]] Loan Return code “201.” 
Documented the use of position 293 [[DO]]-OUT-COMMENTS field for DOs related to [[SFT]]. 
• Made general updates to remove outdated references and reformat the document.  
o Removed references to MDH retired technology and updated to reflect the MQ 
header format used currently. 
o The fields starting in positions 01-74 make up the MQ message header. 
Following this MQ-header will be the standard Message Delivery header (20 
bytes) followed by the application data (starting in position 95). 
11/30/2018 Removed formatting and references to old changes. 
05/31/2017 Revision – Updated field attributes for [[DO]]-OUT-[[DTC]]-CURR-REC# position 511 with 8 zeros 
for transactions in the MMI Finality Staging Engine and Optimizer. 
12/18/2015 Revision – Updated [[DO]] [[DTC]] Processing Status Values within MQ [[DO]] Output. 
09/01/2015
 Revision – Added references to the current MQSeries IBM protocol and inserted the 74-
character [[DTC]] MQ message data for output into the layout for positions 1-74. 
Added MMI Finality Through Optimization Changes. 
• Added new Pend and Drop Reason indicators shown in Exhibits 1 and 2.  
o  Added values for position 130 Pend Reason; position 259 [[DO]] [[DTC]] 
Processing Status; position 511 [[DTC]] Current Record on ATP; position 529 
[[DTC]]’s Pend Drop reason; and position 535 [[DO]] Pend new share position. 
04/01/2014 Revision – Added [[ID]] Net Output indicator in filler position 773 
04/01/2014 Revision – Added [[CNS]] ACAT subaccount types R and S 
11/01/2013 Revision – Amended IMS TID, Filler and RAD Sequence # 
08/01/2013 Revision – Amended RAD Zero dates for RAD Stage 3 target implementation 
03/01/2013 Revision – [[settlement]] Matching Updates for RAD Stage 3 
09/04/2001 Revision – Added new FED fields to expanded [[DO]]-Output record. 
 
[[DTCC]] Public (White)

---

## Page 26

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
[[DTCC]] Public (White)