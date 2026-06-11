---
title: "ISO 15022 Message Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO_15022_Message_Layouts_Output_Messaging.pdf"
pages: 36
size: "294.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO 15022 Message Layouts

**Original File:** [ISO_15022_Message_Layouts_Output_Messaging.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO_15022_Message_Layouts_Output_Messaging.pdf)  
**Category:** Other  
**Total Pages:** 36  
**File Size:** 294.9 KB  

---

## Page 1

 
ISO 15022 Message Layouts 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
Output  
Messaging 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
July 2011 

---

## Page 2

[[Depository Trust Company]] - MT 544 - Receive Free Confirmation                                                                  Non-Confidential (Green) 
MT 544- Receive Free Confirmation 
Business Transaction: Receive Free Confirmation Version: 1.0
ISO Message Type: MT544 - Receive Free Confirmation
These messages are sent by the [[DTCC]] inventory and account process to inform the receiving [[participant]] the made
status of a transaction whether it is for value or free of value.
 Key: M = Mandatory, O = Optional  
Mandatory Sequence A - General Information
M/O Field Description Tag
Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M [[DTCC]] Tracking Number :20C: :SEME// 16x
M
Message Function
 Field that identifies the function of
 the
message
:23G: NEWM
O
Transaction Update Date/Time
 Date the transmission was updated :98C: :PREP// yyyymmddhhmmss
Mandatory 
Subsequence A1 - Linkages (IMS TID)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS Transaction [[ID]]
 Inventory Management System (IMS)
transaction identifier
:20C: :RELA// 16x
M End 
of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages ([[ID]] Control
 Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
[[ID]] Control Number
 
Unique reference used to identify
[[Institutional Delivery]]
 ([[ID]]) transactions
processed by Omgeo.
:20C: :COMM// 16x
M End of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages (Obligation Warehouse)
M/O Field
 Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK

---

## Page 3

M
Obligation Warehouse Control Number
 Obligation Warehouse Control Number for
OW 
DOs
:20C: :COMM//
16x 
Note- Mandatory for OW [[DO]]
transaction. Format is 16 characters.
The first character must be W and the
remainder must be numeric. Format-
WCCYYDDDNNNNNNNN where W is a
literal, CC-Century, YY-Year, DDD-
Julian Day, NNNNNNNN-8 byte
sequential number
M End of Block - Linkages :16S:
 LINK
Mandatory Subsequence A1 - Linkages
 (IMS TID of Reclaimed Transaction)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS TID of Reclaimed 
Transaction
 
Unique transaction reference number
assigned 
by the Inventory Management
System (IMS) and used to process a
reclaim or DK (don?t know) request.
:20C: :PREV// 16x
M End of Block - Linkages :16S:
 LINK
M/O Field Description Tag Qualifier(s) Content Rules
M End of
 Block - General Information :16S:  GENL
Mandatory Sequence B - Trade
 Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Trade Details :16R:  TRADDET
M
[[settlement]] Date
 Date on which the 
transaction should be
settled.
:98A: :SETT// yyyymmdd
M
Contract/Trade Date
 
The contract date for 
an security payment
order. The delivery date is the contract date
and is required for reason codes.
:98A: :TRAD// yyyymmdd
M
Actual [[settlement]] Date
 Date at which the 
transaction was actually
settled on.
:98A: :ESET// yyyymmdd
M
ISIN
 Identification of the financial 
Instrument
(Country Code, [[CUSIP]] and Check Digit)
:35B:
The literal "ISIN" followed by a space
followed by the 12 character ISIN. Note-
[[DTC]] does not accept Non U.S. ISIN 
Example-ISIN US1234567891. Note-[[DTC]]
does not accept Non U.S. ISIN
Optional Subsequence B1 - Financial Instrument Attributes
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Financial Instrument Attributes :16R:
 FIA
O
CMO Factor
 Factor to determine the 
face value of an
amortizing security. DOs only.
:92A: :CUFC//
99,999999999999 
No more than 2 whole digits may be
present. No more than 12 fractional
digits may be present. A decimal
comma is always required.
M End of Block - Financial Instrument Attributes :16S:  FIA

---

## Page 4

M/O Field Description Tag Qualifier(s) Content Rules
O
Fail Tracking Indicator
 Indicates whether a due 
bill is carried or not. :22F: :RPOR/DTCY/
DBLY or DBLN. Note- Formerly known as
Due Bill Indicator 
Indicates whether due bills are carried on
this issue. DBLY - Due bills are carried.
DBLN - Due bills are not carried. If the
field is not populated, DBLY will be
assumed. Note- Formerly known as Due
Bill Indicator
O
Narrative - [[DTC]] [[DO]] Comments
 Provides additional [[settlement]] processing
information
:70E: :SPRO//
35x
 crlf 35x crlf 35x crlf 35x crlf 35x crlf
35x crlf 35x crlf 35x crlf 35x crlf 35x 
The maximum length [[DTC]] will accept is
350, 10 lines of 35 characters. Each line
should be separated by a CRLF (carriage
return - line feed).
M End of Block - Trade Details :16S:
 TRADDET
Mandatory Sequence C - Financial
 Instrument/Account
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Financial Instrument/Account :16R:  FIAC
M
Quantity
 Quantity of financial instrument 
to be settled
expressed as units such as share quantity.
:36B: :ESTT//
UNIT/999999999, 
At least 1 whole digit is required. No more
than 9 may be present. Fractions are not
allowed. A decimal comma is always
required.
M
Safekeeper
 Identifies account where financial 
instruments
are maintained.
:97A: :SAFE// 35x
M End of Block - Financial Instrument/Account :16S:  FIAC
Mandatory Sequence E - [[settlement]]
 Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Details :16R:  SETDET
O
PTA Indicator
 Indicates if the transaction 
should affect the
Protected Transaction Account
:22F: :STCO/DTCY/
PTAY or PTAN 
Valid Values: PTAY - Should affect the
account or PTAN - Should not affect the
account. If the field is not populated,
'PTAN' will be assumed.
O
Activity Code
 A code identifying a 
transaction. :22F: :STCO/DTCYACTV 4x
M
Reason Code
 
The reason code for 
the transaction. This
required field must be filled with a 2-
character alpha-numeric reason code defined
by [[DTC]]. The validity of a reason code is
partly dependent upon the time of
transmission.
:22F: :SETR/DTCYREAS/ 4x 
0 followed by 3 digit [[DTCC]] reason code.
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:
 SETPRTY

---

## Page 5

M
Deliverer
 
[[participant]] that delivers the security; for a
payment order the payee; for a [[collateral]]
pledge the pledgor.
:95R: :DEAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
M
Deliverer's [[intermediary]] 1
 Deliverer's [[intermediary]] 1 :95Q: DEI1/ 35x 
max 
4 lines of 35 bytes
M
Deliverer's [[intermediary]] 2
 Deliverer's [[intermediary]] 2 :95R: DEI2/OCCX 34x 
max 
34 bytes
O
Deliverer's Account Number
 
Deliverer, payee, or pledgor 
account
number. Could be [[DTCC]] [[participant]]
number or the deliverer's internal account
number.
:97A: :SAFE// 35x
M End of Block - [[settlement]] Parties :16S:
 SETPRTY
Mandatory Subsequence E1 - [[settlement]]
 Parties (Receiver)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Receiver
 
[[participant]] that receives the 
security; for a
payment order, the payor; for a [[collateral]]
pledge the pledgee.
:95R: :REAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
M
Receiver's [[intermediary]] 1
 Receiver's [[intermediary]] 1 :95Q: REI1/ 35x 
max 
4 lines of 35 bytes
M
Receiver's [[intermediary]] 2
 Receiver's [[intermediary]] 2 :95R: REI2/OCCX 34x 
max 
34 bytes
O
Receiver's Account Number
 
Receiver, payor, or pledgee 
account
number. Could be [[DTCC]] [[participant]]
number or the receiver's internal account
number.
:97A: :SAFE// 35x
M End of Block - [[settlement]] Parties :16S:
 SETPRTY
Mandatory Subsequence E1 - [[settlement]]
 Parties (Place of [[settlement]])
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Place of [[settlement]]
 [[DTCC]] BIC Number :95P: :PSET// DTCYUS33
M End of
 Block - [[settlement]] Parties :16S:  SETPRTY
Mandatory Subsequence E3 - [[settlement]]
 Amounts ([[settlement]] Amount)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Amounts :16R:  AMT
M
[[settlement]] Amount
 Dollar Amount that was 
settled with
regards to this transaction.
:19A: :ESTT//
USD9999999999,99 
USD followed by at least 1 whole digit.
No more than 10 whole digits may be
present. Fractional digits are optional,
but no more than 2 may be present. A
decimal comma is always required.

---

## Page 6

~
M End of Block - [[settlement]] Amounts :16S:  AMT
M/O Field Description Tag Qualifier(s) Content Rules
M End of
 Block - [[settlement]] Details :16S:  SETDET
Optional Sequence F - Other
 Parties (Third Party Account)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Other Parties :16R:  OTHRPRTY
M
Third Party - Depository
 
Depository Third Party. If 
delivering or
receiving party is a depository, the Third
Party to the transaction.
:95R: :TRAG/DTCY/ 34x
M End of Block - Other Parties :16S:  OTHRPRTY

---

## Page 7

[[Depository Trust Company]] - MT 545 - Receive Against Payment Confirmation                               Non-Confidential (Green)
Print
MT 545 -Receive Against Payment Confirmation 
Business Transaction: Receive Against Payment Confirmation Version: 1.0
ISO Message Type: MT545 - Receive Against Payment Confirmation
These messages are sent by the [[DTCC]] inventory and account process to inform the receiving [[participant]] the made
status of a transaction whether it is for value or free of value.
 Key: M = Mandatory, O = Optional  
Mandatory Sequence A - General 
Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M [[DTCC]] Tracking Number :20C: :SEME// 16x
M
Message Function
 Field that identifies the function of the
message
:23G: NEWM
O
Transaction
 Update Date/Time
 Date the transmission was updated :98C: :PREP// yyyymmddhhmmss
Mandatory 
Subsequence A1 - Linkages (IMS TID)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS Transaction [[ID]]
 Inventory Management System (IMS)
transaction identifier
:20C: :RELA// 16x
M End of
 Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages 
([[ID]] Control Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
[[ID]] Control Number
 
Unique reference used to identify
[[Institutional Delivery]] ([[ID]]) transactions
processed
 by Omgeo.
:20C: :COMM// 16x
M End of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages 
(Obligation Warehouse)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK

---

## Page 8

M
Obligation Warehouse Control Number
 Obligation Warehouse Control Number for
OW DOs
:20C: :COMM//
16x 
Note
- Mandatory for OW [[DO]]
transaction. Format is 16 characters.
The first character must be W and the
remainder must be numeric. Format-
WCCYYDDDNNNNNNNN where W is a
literal, CC-Century, YY-Year, DDD-
Julian Day, NNNNNNNN-8 byte
sequential number
M End of Block - Linkages :16S:
 LINK
Mandatory Subsequence A1 - Linkages
 (IMS TID of Reclaimed Transaction)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS TID of Reclaimed Transaction
 
Unique transaction reference number
assigned by the Inventory
 Management
System (IMS) and used to process a
reclaim or DK (don?t know) request.
:20C: :PREV// 16x
M End of Block - Linkages :16S:
 LINK
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block
 - General Information :16S:  GENL
Mandatory Sequence B - Trade
 Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Trade Details :16R:  TRADDET
M
[[settlement]] Date
 Date on which the transaction should be
settled.
:98A:
:SETT// yyyymmdd
M
Contract/Trade Date
 
The contract date for an security payment
order.
 The delivery date is the contract date
and is required for reason codes.
:98A: :TRAD// yyyymmdd
M
Actual [[settlement]] Date
 Date at which the transaction was actually
settled
 on.
:98A: :ESET// yyyymmdd
M
ISIN
 Identification of the financial Instrument
(Country Code, [[CUSIP]]
 and Check Digit)
:35B:
The literal "ISIN" followed by a space
followed by the 12 character ISIN. Note-
[[DTC]] does not accept Non U.S. ISIN 
Example-ISIN US1234567891. Note-[[DTC]]
does not accept Non U.S. ISIN
Optional Subsequence B1 - Financial Instrument Attributes
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Financial Instrument Attributes :16R:
 FIA
O
CMO Factor
 Factor to determine the face value of
 an
amortizing security. DOs only.
:92A: :CUFC//
99,999999999999 
No more than 2 whole digits may be
present. No more than 12 fractional
digits may be present. A decimal
comma is always required.
M End of Block - Financial Instrument Attributes :16S:  FIA

---

## Page 9

M/O Field Description Tag Qualifier(s) Content Rules
O
Fail Tracking Indicator
 Indicates whether a due bill is carried
 or not. :22F: :RPOR/DTCY/
DBLY or DBLN. Note- Formerly known as
Due Bill Indicator 
Indicates whether due bills are carried on
this issue. DBLY - Due bills are carried.
DBLN - Due bills are not carried. If the
field is not populated, DBLY will be
assumed. Note- Formerly known as Due
Bill Indicator
O
Narrative - [[DTC]] [[DO]] Comments
 Provides additional [[settlement]] processing
information
:70E: :SPRO//
35x crlf 35x
 crlf 35x crlf 35x crlf 35x crlf
35x crlf 35x crlf 35x crlf 35x crlf 35x 
The maximum length [[DTC]] will accept is
350, 10 lines of 35 characters. Each line
should be separated by a CRLF (carriage
return - line feed).
M End of Block - Trade Details :16S:
 TRADDET
Mandatory Sequence C - Financial
 Instrument/Account
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Financial Instrument/Account :16R:  FIAC
M
Quantity
 Quantity of financial instrument to be settled
expressed
 as units such as share quantity.
:36B: :ESTT//
UNIT/999999999, 
At least 1 whole digit is required. No more
than 9 may be present. Fractions are not
allowed. A decimal comma is always
required.
M
Safekeeper
 Identifies account where financial instruments
are maintained.
:97A: :SAFE// 35x
M End
 of Block - Financial Instrument/Account :16S:  FIAC
Mandatory Sequence E - [[settlement]]
 Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Details :16R:  SETDET
O
PTA Indicator
 Indicates if the transaction should affect the
Protected
 Transaction Account
:22F: :STCO/DTCY/
PTAY or PTAN 
Valid Values: PTAY - Should affect the
account or PTAN - Should not affect the
account. If the field is not populated,
'PTAN' will be assumed.
O
Activity Code
 A code identifying a transaction. :22F: :STCO/DTCYACTV 4x
M
Reason
 Code
 
The reason code for the transaction. This
required
 field must be filled with a 2-
character alpha-numeric reason code defined
by [[DTC]]. The validity of a reason code is
partly dependent upon the time of
transmission.
:22F: :SETR/DTCYREAS/ 4x 
0 followed by 3 digit [[DTCC]] reason code.
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:
 SETPRTY

---

## Page 10

M
Deliverer
 
[[participant]] that delivers the security; for a
payment  order the payee; for a [[collateral]]
pledge the pledgor.
:95R: :DEAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
M
Deliverer's [[intermediary]] 1
 Deliverer's [[intermediary]] 1 :95Q: DEI1/ 35x 
max 4 lines
 of 35 bytes
M
Deliverer's [[intermediary]] 2
 Deliverer's [[intermediary]] 2 :95R: DEI2/OCCX 34x 
max 34 bytes
O
Deliverer's
 Account Number
 
Deliverer, payee, or pledgor account
number. Could be
 [[DTCC]] [[participant]]
number or the deliverer's internal account
number.
:97A: :SAFE// 35x
M End of Block - [[settlement]] Parties :16S:
 SETPRTY
Mandatory Subsequence E1 - [[settlement]]
 Parties (Receiver)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Receiver
 
[[participant]] that receives the security; for a
payment
 order, the payor; for a [[collateral]]
pledge the pledgee.
:95R: :REAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
M
Receiver's [[intermediary]] 1
 Receiver's [[intermediary]] 1 :95Q: REI1/ 35x 
max 4 lines
 of 35 bytes
M
Receiver's [[intermediary]] 2
 Receiver's [[intermediary]] 2 :95R: REI2/OCCX 34x 
max 34 bytes
O
Receiver's
 Account Number
 
Receiver, payor, or pledgee account
number. Could be
 [[DTCC]] [[participant]]
number or the receiver's internal account
number.
:97A: :SAFE// 35x
M End of Block - [[settlement]] Parties :16S:
 SETPRTY
Mandatory Subsequence E1 - [[settlement]]
 Parties (Place of [[settlement]])
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Place of [[settlement]]
 [[DTCC]] BIC Number :95P: :PSET// DTCYUS33
M End of Block -
 [[settlement]] Parties :16S:  SETPRTY
Mandatory Subsequence E3 - [[settlement]]
 Amounts ([[settlement]] Amount)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Amounts :16R:  AMT
M
[[settlement]] Amount
 Dollar Amount that was settled with
regards to
 this transaction.
:19A: :ESTT//
USD9999999999,99 
USD followed by at least 1 whole digit.
No more than 10 whole digits may be
present. Fractional digits are optional,
but no more than 2 may be present. A
decimal comma is always required.

---

## Page 11

M End of Block - [[settlement]] Amounts :16S:  AMT
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block
 - [[settlement]] Details :16S:  SETDET
Optional Sequence F - Other
 Parties (Third Party Account)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Other Parties :16R:  OTHRPRTY
M
Third Party - Depository
 
Depository Third Party. If delivering or
receiving party
 is a depository, the Third
Party to the transaction.
:95R: :TRAG/DTCY/ 34x
M End of Block - Other Parties :16S:  OTHRPRTY
Print

---

## Page 12

[[Depository Trust Company]] - MT 546 - Deliver Free Confirmation                                                                                   Non Confidential (Green)
MT 546-Deliver Free Confirmation 
Business Transaction: Deliver Free Confirmation Version: 1.0
ISO Message Type: MT546 - Deliver Free Confirmation
These messages are sent by the [[DTCC]] inventory and account process to inform the delivering [[participant]] the made
status of a transaction whether it is for value or free of value.
 Key: M = Mandatory, O = Optional  
Mandatory Sequence A - General Information
M/O Field 
Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M [[DTCC]] Tracking Number :20C: :SEME// 16x
M
Message Function
 Field that identifies the function of the
message
:23G: NEWM
O
Transaction Update
 Date/Time
 Date the transmission was updated :98C: :PREP// yyyymmddhhmmss
Mandatory Subsequence
 A1 - Linkages (IMS TID)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS Transaction [[ID]]
 Inventory Management System (IMS)
transaction identifier
:20C: :RELA// 16x
M End of Block
 - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages ([[ID]] 
Control Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
[[ID]] Control Number
 
Unique reference used to identify
[[Institutional Delivery]] ([[ID]]) transactions
processed by
 Omgeo.
:20C: :COMM// 16x
M End of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages (Obligation 
Warehouse)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK

---

## Page 13

M
Obligation Warehouse Control Number
 Obligation Warehouse Control Number for
OW DOs
:20C: :COMM//
16x 
Note-
 Mandatory for OW [[DO]]
transaction. Format is 16 characters.
The first character must be W and the
remainder must be numeric. Format-
WCCYYDDDNNNNNNNN where W is a
literal, CC-Century, YY-Year, DDD-
Julian Day, NNNNNNNN-8 byte
sequential number
M End of Block - Linkages :16S:
 LINK
Mandatory Subsequence A1 - Linkages (Deliverer
 Reference Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
Deliverer's Reference Number
 Assigned by payee (deliverer) for audit
trail
:20C: :TRRF// 16x
M End of
 Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages (IMS
 TID of Reclaimed Transaction)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS TID of Reclaimed Transaction
 
Unique transaction reference number
assigned by the Inventory Management
System
 (IMS) and used to process a
reclaim or DK (don?t know) request.
:20C: :PREV// 16x
M End of Block - Linkages :16S:  LINK
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block - General
 Information :16S:  GENL
Mandatory Sequence B - Trade Details
M/O Field
 Description Tag Qualifier(s) Content Rules
M Start of Block - Trade Details :16R:  TRADDET
M
[[settlement]] Date
 Date on which the transaction should be
settled.
:98A: :SETT// yyyymmdd
M
Contract/Trade
 Date
 
The contract date for an security payment
order. The
 delivery date is the contract date
and is required for reason codes.
:98A: :TRAD// yyyymmdd
M
Actual [[settlement]] Date
 Date at which the transaction was actually
settled on.
:98A:
:ESET// yyyymmdd
M
ISIN
 Identification of the financial Instrument
(Country Code, [[CUSIP]] and
 Check Digit)
:35B:
The literal "ISIN" followed by a space
followed by the 12 character ISIN. Note-
[[DTC]] does not accept Non U.S. ISIN 
Example-ISIN US1234567891. Note-[[DTC]]
does not accept Non U.S. ISIN

---

## Page 14

Optional Subsequence B1 - Financial Instrument Attributes
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Financial Instrument Attributes :16R:  FIA
O
CMO Factor
 Factor to determine the face value of an
amortizing
 security. DOs only.
:92A: :CUFC//
99,999999999999 
No more than 2 whole digits may be
present. No more than 12 fractional
digits may be present. A decimal
comma is always required.
M End of Block - Financial Instrument Attributes :16S:
 FIA
M/O Field Description Tag Qualifier(s) Content Rules
O
Fail Tracking Indicator
 Indicates whether a due bill is carried or
 not. :22F: :RPOR/DTCY/
DBLY or DBLN. Note- Formerly known as
Due Bill Indicator 
Indicates whether due bills are carried on
this issue. DBLY - Due bills are carried.
DBLN - Due bills are not carried. If the
field is not populated, DBLY will be
assumed. Note- Formerly known as Due
Bill Indicator
O
Narrative - [[DTC]] [[DO]] Comments
 Provides additional [[settlement]] processing
information
:70E: :SPRO//
35x crlf 35x crlf
 35x crlf 35x crlf 35x crlf
35x crlf 35x crlf 35x crlf 35x crlf 35x 
The maximum length [[DTC]] will accept is
350, 10 lines of 35 characters. Each line
should be separated by a CRLF (carriage
return - line feed).
M End of Block - Trade Details :16S:
 TRADDET
Mandatory Sequence C - Financial Instrument/Account
M/O Field
 Description Tag Qualifier(s) Content Rules
M Start of Block - Financial Instrument/Account :16R:  FIAC
M
Quantity
 Quantity of financial instrument to be settled
expressed as
 units such as share quantity.
:36B: :ESTT//
UNIT/999999999, 
At least 1 whole digit is required. No more
than 9 may be present. Fractions are not
allowed. A decimal comma is always
required.
M
Safekeeper
 Identifies account where financial instruments
are maintained.
:97A: :SAFE// 35x
M End of
 Block - Financial Instrument/Account :16S:  FIAC
Mandatory Sequence E - [[settlement]] Details
M/O Field
 Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Details :16R:  SETDET
O
PTA Indicator
 Indicates if the transaction should affect the
Protected Transaction
 Account
:22F: :STCO/DTCY/
PTAY or PTAN 
Valid Values: PTAY - Should affect the
account or PTAN - Should not affect the
account. If the field is not populated,
'PTAN' will be assumed.
O
Activity Code
 A code identifying a transaction. :22F: :STCO/DTCYACTV 4x
Reason Code

---

## Page 15

M  
The reason code for the transaction. This
required
 field must be filled with a 2-
character alpha-numeric reason code defined
by [[DTC]]. The validity of a reason code is
partly dependent upon the time of
transmission.
:22F: :SETR/DTCYREAS/ 4x 
0 followed by 3 digit [[DTCC]] reason code.
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:
 SETPRTY
M
Deliverer
 
[[participant]] that delivers the security; for a
payment
 order the payee; for a [[collateral]]
pledge the pledgor.
:95R: :DEAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
M
Deliverer's [[intermediary]] 1
 Deliverer's [[intermediary]] 1 :95Q: DEI1/ 35x 
max 4 lines
 of 35 bytes
M
Deliverer's [[intermediary]] 2
 Deliverer's [[intermediary]] 2 :95R: DEI2/OCCX 34x 
max 34 bytes
O
Deliverer's
 Account Number
 
Deliverer, payee, or pledgor account
number. Could be
 [[DTCC]] [[participant]]
number or the deliverer's internal account
number.
:97A: :SAFE// 35x
M End of Block - [[settlement]] Parties :16S:
 SETPRTY
Mandatory Subsequence E1 - [[settlement]]
 Parties (Receiver)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Receiver
 
[[participant]] that receives the security; for a
payment
 order, the payor; for a [[collateral]]
pledge the pledgee.
:95R: :REAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
M
Receiver's [[intermediary]] 1
 Receiver's [[intermediary]] 1 :95Q: REI1/ 35x 
max 4 lines
 of 35 bytes
M
Receiver's [[intermediary]] 2
 Receiver's [[intermediary]] 2 :95R: REI2/OCCX 34x 
max 34 bytes
O
Receiver's
 Account Number
 
Receiver, payor, or pledgee account
number. Could be
 [[DTCC]] [[participant]]
number or the receiver's internal account
number.
:97A: :SAFE// 35x
M End of Block - [[settlement]] Parties :16S:
 SETPRTY
Mandatory Subsequence E1 - [[settlement]]
 Parties (Place of [[settlement]])
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Place of [[settlement]]
 [[DTCC]] BIC Number :95P: :PSET// DTCYUS33
M End of Block -
 [[settlement]] Parties :16S:  SETPRTY

---

## Page 16

http://pbsp/ISOMessageFacility/next.[[DO]]?nextpage=documentview&rand=0.4373580219442905[4/29/2011 3:39:18 PM]
Mandatory Subsequence E3 - [[settlement]] Amounts ([[settlement]] Amount)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Amounts :16R:  AMT
M
[[settlement]] Amount
 Dollar Amount that was settled with
regards to
 this transaction.
:19A: :ESTT//
USD9999999999,99 
USD followed by at least 1 whole digit.
No more than 10 whole digits may be
present. Fractional digits are optional,
but no more than 2 may be present. A
decimal comma is always required.
M End of Block - [[settlement]] Amounts :16S:
 AMT
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block
 - [[settlement]] Details :16S:  SETDET
Optional Sequence F - Other
 Parties (Third Party Account)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Other Parties :16R:  OTHRPRTY
M
Third Party - Depository
 
Depository Third Party. If delivering or
receiving party
 is a depository, the Third
Party to the transaction.
:95R: :TRAG/DTCY/ 34x
M End of Block - Other Parties :16S:  OTHRPRTY

---

## Page 17

[[Depository Trust Company]] - MT547 - Deliver Against Payment Confirmation For [[collateral]] Pledges               Non-Confidential (Green)
Deliver Against Payment Confirmation For [[collateral]] Pledges 
Business Transaction: Deliver Against Payment Confirmation For [[collateral]] Pledges Version: 1.0
ISO Message Type: MT547 - Deliver Against Payment Confirmation
These messages are sent by the [[DTCC]] inventory and account process to inform the delivering [[participant]] the made
status of a transaction whether it is for value or free of value.
 Key: M = Mandatory, O = Optional  
Mandatory Sequence A - General
 Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M [[DTCC]] Tracking Number :20C: :SEME// 16x
M
Message Function
 Field that identifies the function
 of the
message
:23G: NEWM
O
Transaction Update Date/Time
 Date the transmission was updated :98C:
:PREP// yyyymmddhhmmss
Mandatory Subsequence A1 - Linkages (IMS TID)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS Transaction [[ID]]
 Inventory Management System (IMS)
transaction identifier
:20C:
:RELA// 16x
M End of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages
 (Deliverer Reference Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
Deliverer's Reference Number
 Assigned by payee (deliverer) for
 audit
trail
:20C: :TRRF// 16x
M End of Block - Linkages :16S:  LINK
M/O Field Description Tag Qualifier(s) Content Rules
M End of
 Block - General Information :16S:  GENL

---

## Page 18

Mandatory Sequence B - Trade Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Trade Details :16R:  TRADDET
O
Loan Date
 Loan date for a pledge
 or pledge release
transaction
:98A: :SETT// yyyymmdd
M
Actual [[settlement]] Date
 Date at which the transaction
 was actually
settled on.
:98A: :ESET// yyyymmdd
M
ISIN
 Identification of the financial Instrument
(Country
 Code, [[CUSIP]] and Check Digit)
:35B:
The literal "ISIN" followed by a space
followed by the 12 character ISIN. Note-
[[DTC]] does not accept Non U.S. ISIN 
Example-ISIN US1234567891. Note-[[DTC]]
does not accept Non U.S. ISIN
O
Narrative - [[DTC]] [[DO]] Comments
 Provides additional [[settlement]] processing
information
:70E: :SPRO//
35x
 crlf 35x crlf 35x crlf 35x crlf 35x crlf
35x crlf 35x crlf 35x crlf 35x crlf 35x 
The maximum length [[DTC]] will accept is
350, 10 lines of 35 characters. Each line
should be separated by a CRLF (carriage
return - line feed).
M End of Block - Trade Details :16S:
 TRADDET
Mandatory Sequence C - Financial
 Instrument/Account
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Financial Instrument/Account :16R:  FIAC
M
Quantity
 Quantity of financial instrument to
 be settled
expressed as units such as share quantity.
:36B: :ESTT//
UNIT/999999999, 
At least 1 whole digit is required. No more
than 9 may be present. Fractions are not
allowed. A decimal comma is always
required.
M
Safekeeper
 Identifies account where financial instruments
are
 maintained.
:97A: :SAFE// 35x
M End of Block - Financial Instrument/Account :16S:  FIAC
Mandatory Sequence E - [[settlement]]
 Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Details :16R:  SETDET
O
[[IPO]] Indicator
 Indicator used for the [[IPO]]
 Tracking system. :22F: :STCO/DTCY/
IPOY or IPON 
Indicates that the new [[IPO]] format is being
used. 'IPOY' - [[IPO]] format is being used.
'IPON' - [[IPO]] format is not used. If the
field is not populated, 'IPON' will be
assumed.
O
PTA Indicator
 Indicates if the transaction should
 affect the
Protected Transaction Account
:22F: :STCO/DTCY/
PTAY or PTAN 
Valid Values: PTAY - Should affect the
account or PTAN - Should not affect the
account. If the field is not populated,
'PTAN' will be assumed.
O
Activity Code
 A code identifying a transaction. :22F:
:STCO/DTCYACTV 4x
M
Reason Code
 The reason code for the
 transaction. :22F: :SETR/DTCYREAS/ 4x 
0 followed by 3 digit [[DTCC]] reason code.

---

## Page 19

O
Release Type
 Indicates the reason for the  release request :22F: :SETS/DTCY/
4n 
Valid Values: 0001 - Delivery. 0002 -
Substitution of [[collateral]]. 0003 - Decrease
of [[collateral]]. 0004 - Release of Excess
[[collateral]].
O
[[Hypothecation]] Code
 Mandatory code entered by the
 [[participant]] to
effect deliveries for pledge activity.
:22F: :COLA/DTCY/
4n 
Indicates to the pledgee the person(s) for
whom this transaction is pledged. 0001 -
Each security in the pledge is carried for
the account of one or more customers.
0002 - All [[securities]] in the pledge are
carried for the account of a single
customer. 0003 - No [[securities]] in the
pledge are carried for the account of any
customer. 0007 - Used for Repo accounts.
0008 - Used for Repo accounts. 0009 -
Used for Repo accounts.
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:
 SETPRTY
M
Deliverer (Pledgor)
 
[[participant]] that delivers the security;
 for a
payment order the payee; for a [[collateral]]
pledge the pledgor.
:95R: :DEAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
M End of Block - [[settlement]] Parties :16S:
 SETPRTY
Mandatory Subsequence E1 - [[settlement]]
 Parties (Receiver)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Receiver (Pledgee)
 
[[participant]] that receives the security;
 for a
payment order, the payor; for a [[collateral]]
pledge the pledgee.
:95R: :REAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
M End of Block - [[settlement]] Parties :16S:
 SETPRTY
Mandatory Subsequence E1 - [[settlement]]
 Parties (Place of [[settlement]])
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Place of [[settlement]]
 [[DTCC]] BIC Number :95P: :PSET// DTCYUS33
M End of
 Block - [[settlement]] Parties :16S:  SETPRTY
Mandatory Subsequence E3 - [[settlement]]
 Amounts ([[settlement]] Amount)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Amounts :16R:  AMT
M
[[collateral]] Amount
 Dollar Amount that was settled
 with
regards to this transaction.
:19A: :ESTT//
USD999999999999,99 
USD followed by at least 1 whole digit.
No more than 12 whole digits may be
present. Fractional digits are optional,
but no more than 2 may be present. A
decimal comma is always required.

---

## Page 20

M End of Block - [[settlement]] Amounts :16S:  AMT
M/O Field Description Tag Qualifier(s) Content Rules
M End of
 Block - [[settlement]] Details :16S:  SETDET

---

## Page 21

[[Depository Trust Company]] - MT 548 - [[settlement]] Status (Long Version)                                                                        Non Confidential (Green)
MT 548-[[settlement]] Status (Long Version) 
Business Transaction: [[settlement]] Status (Long Version) Version: 1.0
ISO Message Type: MT548 - [[settlement]] Status and Processing Advice
These are optional messages are sent to the [[participant]] for "non-made" state changes in IMS/ATP occurs.
 Key: M = Mandatory, O = Optional  
Mandatory Sequence A - 
General Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M [[DTCC]] Tracking Number :20C: :SEME// 16x
M
Message Function
 Field that identifies the function of
 the
message
:23G: INST
O
Transaction Update Date/Time
 Date the transmission was updated :98C: :PREP// yyyymmddhhmmss
Mandatory
 Subsequence A1 - Linkages (IMS TID)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS Transaction [[ID]]
 Inventory Management System (IMS)
transaction identifier
:20C: :RELA// 16x
M End
 of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - 
Linkages ([[ID]] Control Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
[[ID]] Control Number
 
Unique reference used to identify
[[Institutional Delivery]]
 ([[ID]]) transactions
processed by Omgeo.
:20C: :COMM// 16x
M End of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - 
Linkages (Obligation Warehouse)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK

---

## Page 22

M
Obligation Warehouse Control Number
 Obligation Warehouse Control Number for
OW DOs
:20C: :COMM//
16x 
Note
- Mandatory for OW [[DO]]
transaction. Format is 16 characters.
The first character must be W and the
remainder must be numeric. Format-
WCCYYDDDNNNNNNNN where W is a
literal, CC-Century, YY-Year, DDD-
Julian Day, NNNNNNNN-8 byte
sequential number
M End of Block - Linkages :16S:
 LINK
Mandatory Subsequence A1 - Linkages
 (Deliverer Reference Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
Deliverer's Reference Number
 Assigned by payee (deliverer) for audit
trail
:20C: :TRRF// 16x
M End
 of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages
 (IMS TID of Reclaimed Transaction)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS TID of Reclaimed Transaction
 
Unique transaction reference number
assigned by the Inventory
 Management
System (IMS) and used to process a
reclaim or DK (don?t know) request.
:20C: :PREV// 16x
M End of Block - Linkages :16S:
 LINK
Mandatory Subsequence A2 - Status
M/O Field
 Description Tag Qualifier(s) Content Rules
M Start of Block - Status :16R:  STAT
M
Status Code
 
The IMS or ATP states assigned as
 the
transaction is processed through IMS and
ATP.
:25D: :SETT/DTCY/
4x 
Valid Status Codes: AUTH - Authorized,
CANA - ATP Cancelled, CANC - IMS
Cancelled, MAKD - Made, NAL1 - [[CNS]]
Level 1 Received, NAL2 - [[CNS]] Level 2
Received, PDRI - IMS Permanently
Dropped, PDRP - Dropped Permanent,
PREA - Pre-Authorized, PREX - Pre-
Exempted, RATP - PDC Reduction
Processed, RAUT - RAD Authorized,
RDPR - ATP Dropped Reintroduced,
RGRN - Recycling Green, RJCF - IMS
Rejected to File, RJCT - ATP Rejected,
RJCI - IMS Rejected, RLSD - Released,
RSUB - Submitted to RAD, SUBA -
Submitted to ATP, UNPR - Unprocessed,
XMPT - Exempted, XPER - Recycling
Express
Optional Subsequence A2a - Reason
M/O Field Description Tag Qualifier(s) Content Rules

---

## Page 23

M Start of Block - Reason :16R:  REAS
M
Reject Code - Field Code
 Reject code :24B: :REJT/DTCY/ 4x
O
Reject Code - Error Message
 Reason for the reject :70D: :REAS//
35x crlf 35x crlf
 35x crlf 35x crlf 35x
crlf 35x 
The maximum length [[DTC]] will
accept is 210, 6 lines of 35
characters. Each line should be
separated by a CRLF (carriage
return - line feed).
M End of Block - Reason :16S:
 REAS
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block - Status :16S:  STAT
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block - General
 Information :16S:  GENL
Optional Sequence B - [[settlement]] Transaction
 Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Transaction Details :16R:  SETTRAN
M
ISIN
 Identification of the financial Instrument
(Country Code, [[CUSIP]] and
 Check Digit)
:35B:
The literal "ISIN" followed by a space
followed by the 12 character ISIN. Note-
[[DTC]] does not accept Non U.S. ISIN 
Example-ISIN US1234567891. Note-[[DTC]]
does not accept Non U.S. ISIN
M
Quantity
 Quantity of financial instrument to be settled
expressed as
 units such as share quantity.
:36B: :SETT//
UNIT/999999999, 
At least 1 whole digit is required. No more
than 9 may be present. Fractions are not
allowed. A decimal comma is always
required.
M
[[settlement]] Amount
 Dollar Amount that was settled with regards
to this
 transaction.
:19A: :SETT//
USD9999999999,99 
USD followed by at least 1 whole digit. No
more than 10 whole digits may be
present. Fractional digits are optional, but
no more than 2 may be present. A
decimal comma is always required.
M
Safekeeper
 Identifies account where financial instruments
are maintained.
:97A: :SAFE// 35x
M
Reason Code
 
The reason code for the transaction. This
required field
 must be filled with a 2-
character alpha-numeric reason code defined
by [[DTC]]. The validity of a reason code is
partly dependent upon the time of
transmission.
:22F: :SETR/DTCYREAS/ 4x 
0 followed by 3 digit [[DTCC]] reason code.
M Receiver/Deliverer Indicator :22H: :REDE//
DELI or RECE 
Valid Values: DELI - indicates that you
are the deliverer or RECE - indicates that
you are the receiver
M
Payment Indicator
 Indicates whether the underlying [[securities]]
are free or valued
:22H:
:PAYM//
APMT or FREE 
Valid values: APMT - indicates a valued
transaction or FREE - indicates a free
transaction
O
Internal Source Code
:22F: :STCO/DTCYISRC 4x

---

## Page 24

 Identifies the input media for the transaction
O
Transaction
 Type
 IMS transaction type :22F: :STCO/DTCYTXNT/ 4x
O
Activity Code
 A code identifying a transaction. :22F: :STCO/DTCYACTV 4x
O
3rd
 Party Status Indicator
 Indicator used for the Third Party approvals
status.
:22F:
:STCO/DTCY/
TRDP or TRDA or TRDD 
The IMS state for Third Party approvals.
TRDP - Pending Approval, TRDA -
Approved, TRDD - Disapproved.
O
[[CNS]] Level Indicator
 
Indicates how [[CNS]] short (levels 1 and
 2) and
long (level 4) [[shares]] should be processed. I.e.
Short [[shares]] can be exempted and long
[[shares]] anticipated.
:22F: :SETS/DTCY/ LVL1, LVL2, LVL3, LVL4 or LVLL
O
Actual [[settlement]] Date
 Date at which the transaction was actually
settled
 on.
:98A: :EXSE// yyyymmdd
M
[[settlement]] Date
 Date on which the transaction should be
settled.
:98A:
:SETT// yyyymmdd
O
Contract/Trade Date
 
The contract date for an security payment
order.
 The delivery date is the contract date
and is required for reason codes.
:98A: :TRAD// yyyymmdd
O
Narrative - [[DTC]] [[DO]] Comments
 Provides additional [[settlement]] processing
information
:70E: :SPRO//
35x crlf 35x
 crlf 35x crlf 35x crlf 35x crlf
35x crlf 35x crlf 35x crlf 35x crlf 35x 
The maximum length [[DTC]] will accept is
350, 10 lines of 35 characters. Each line
should be separated by a CRLF (carriage
return - line feed).
Optional Subsequence B1 - [[settlement]] Parties (Deliverer)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:
 SETPRTY
M
Deliverer
 
[[participant]] that delivers the security; for a
payment
 order the payee; for a [[collateral]]
pledge the pledgor.
:95R: :DEAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
M
Deliverer's [[intermediary]] 1
 Deliverer's [[intermediary]] 1 :95Q: DEI1/ 35x 
max 4 lines
 of 35 bytes
M
Deliverer's [[intermediary]] 2
 Deliverer's [[intermediary]] 2 :95R: DEI2/OCCX 34x 
max 34 bytes
O
Deliverer's
 Account Number
 
Deliverer, payee, or pledgor account
number. Could be
 [[DTCC]] [[participant]]
number or the deliverer's internal account
number.
:97A: :SAFE// 35x
M End of Block - [[settlement]] Parties :16S:
 SETPRTY
Optional Subsequence B1 - [[settlement]]
 Parties (Receiver)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY

---

## Page 25

M
Receiver
 
[[participant]] that receives the security; for  a
payment order, the payor; for a [[collateral]]
pledge the pledgee.
:95R: :REAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
M
Receiver's [[intermediary]] 1
 Receiver's [[intermediary]] 1 :95Q: REI1/ 35x 
max 4
 lines of 35 bytes
M
Receiver's [[intermediary]] 2
 Receiver's [[intermediary]] 2 :95R: REI2/OCCX 34x 
max 34
 bytes
O
Receiver's Account Number
 
Receiver, payor, or pledgee account
number. Could
 be [[DTCC]] [[participant]]
number or the receiver's internal account
number.
:97A: :SAFE// 35x
M End of Block - [[settlement]] Parties :16S:
 SETPRTY
Optional Subsequence B1 -
 [[settlement]] Parties (Place of [[settlement]])
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Place of [[settlement]]
 [[DTCC]] BIC Number :95P: :PSET// DTCYUS33
M End of Block
 - [[settlement]] Parties :16S:  SETPRTY
Optional Subsequence B1 -
 [[settlement]] Parties (Deliverer - [[intermediary]])
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Deliverer's [[intermediary]]
 Depository Third Party field :95R: :DEI1/DTCYPART 34x
M End
 of Block - [[settlement]] Parties :16S:  SETPRTY
Optional Subsequence B1 -
 [[settlement]] Parties (Receiver - [[intermediary]])
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Receiver's [[intermediary]]
 Depository Third Party field :95R: :REI1/DTCYPART 34x
M End
 of Block - [[settlement]] Parties :16S:  SETPRTY
M/O Field Description Tag Qualifier(s) Content Rules
M End of
 Block - [[settlement]] Transaction Details :16S:  SETTRAN

---

## Page 26

[[Depository Trust Company]] - MT 548 - [[settlement]] Status (Long Version) for Accounting                                     Non Confidential  (Green)
MT 548 [[settlement]] Status (Long Version) for Accounting 
Business Transaction: [[settlement]] Status (Long Version) for Accounting Version: 1.0
ISO Message Type: MT548 - [[settlement]] Status and Processing Advice
These are optional messages are sent to the [[participant]] for all state changes including "Made" in IMS/ATP occurs.
 Key: M = Mandatory, O = Optional  
Mandatory Sequence A - 
General Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M [[DTCC]] Tracking Number :20C: :SEME// 16x
M
Message Function
 Field that identifies the function of
 the
message
:23G: INST
O
Transaction Update Date/Time
 Date the transmission was updated :98C: :PREP// yyyymmddhhmmss
Mandatory
 Subsequence A1 - Linkages (IMS TID)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS Transaction [[ID]]
 Inventory Management System (IMS)
transaction identifier
:20C: :RELA// 16x
M End
 of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - 
Linkages (Deliverer Reference Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
Deliverer's Reference Number
 Assigned by payee (deliverer) for audit
trail
:20C:
:TRRF// 16x
M End of Block - Linkages :16S:  LINK
Mandatory Subsequence A2 - 
Status
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Status :16R:  STAT
4x 

---

## Page 27

M
Status Code
 
The IMS or ATP states assigned as  the
transaction is processed through IMS and
ATP.
:25D: :SETT/DTCY/
Valid Status Codes: AUTH - Authorized,
CANA - ATP Cancelled, CANC - IMS
Cancelled, MAKD - Made, NAL1 - [[CNS]]
Level 1 Received, NAL2 - [[CNS]] Level 2
Received, PDRI - IMS Permanently
Dropped, PDRP - Dropped Permanent,
PREA - Pre-Authorized, PREX - Pre-
Exempted, RATP - PDC Reduction
Processed, RAUT - RAD Authorized,
RDPR - ATP Dropped Reintroduced,
RGRN - Recycling Green, RJCF - IMS
Rejected to File, RJCT - ATP Rejected,
RJCI - IMS Rejected, RLSD - Released,
RSUB - Submitted to RAD, SUBA -
Submitted to ATP, UNPR - Unprocessed,
XMPT - Exempted, XPER - Recycling
Express
Optional Subsequence A2a - Reason
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Reason :16R:
 REAS
M
Reject Code - Field Code
 Reject code :24B: :REJT/DTCY/ 4x
O
Reject Code - Error
 Message
 Reason for the reject :70D: :REAS//
35x crlf 35x
 crlf 35x crlf 35x crlf 35x
crlf 35x 
The maximum length [[DTC]] will
accept is 210, 6 lines of 35
characters. Each line should be
separated by a CRLF (carriage
return - line feed).
M End of Block - Reason :16S:
 REAS
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block
 - Status :16S:  STAT
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block
 - General Information :16S:  GENL
Optional Sequence B - [[settlement]]
 Transaction Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Transaction Details :16R:  SETTRAN
M
ISIN
 Identification of the financial Instrument
(Country Code, [[CUSIP]]
 and Check Digit)
:35B:
The literal "ISIN" followed by a space
followed by the 12 character ISIN. Note-
[[DTC]] does not accept Non U.S. ISIN 
Example-ISIN US1234567891. Note-[[DTC]]
does not accept Non U.S. ISIN
M
Quantity
 Quantity of financial instrument to be settled
expressed
 as units such as share quantity.
:36B: :SETT//
UNIT/999999999, 
At least 1 whole digit is required. No more
than 9 may be present. Fractions are not
allowed. A decimal comma is always
required.
M
Safekeeper
 Identifies account where financial instruments
are maintained.
:97A: :SAFE// 35x
ADDS
 or SUBS or OVRL 
Must be one of the following values:

---

## Page 28

M Action Code :22F: :SETR/DTCY/ ADDS - Add to existing [[shares]], SUBS -
Subtract from existing [[shares]], OVRL -
Overlay existing [[shares]]
M Receiver/Deliverer Indicator :22H: :REDE//
DELI or RECE 
Valid Values: DELI - indicates that you
are the deliverer or RECE - indicates that
you are the receiver
M
Payment Indicator
 Indicates whether the underlying [[securities]]
are free or
 valued
:22H: :PAYM//
APMT or FREE 
Valid values: APMT - indicates a valued
transaction or FREE - indicates a free
transaction
O
Internal Source Code
 Identifies the input media for the transaction :22F:
:STCO/DTCYISRC 4x
O
Transaction Type
 IMS transaction type :22F: :STCO/DTCYTXNT/ 4x
O
Activity Code
 A code identifying a transaction. :22F: :STCO/DTCYACTV 4x
O
Actual
 [[settlement]] Date
 Date at which the transaction was actually
settled
 on.
:98A: :EXSE// yyyymmdd
M
[[settlement]] Date
 Date on which the transaction should be
settled.
:98A:
:SETT// yyyymmdd
O
Narrative - [[DTC]] [[DO]] Comments
 Provides additional [[settlement]] processing
information
:70E: :SPRO//
35x crlf 35x
 crlf 35x crlf 35x crlf 35x crlf
35x crlf 35x crlf 35x crlf 35x crlf 35x 
The maximum length [[DTC]] will accept is
350, 10 lines of 35 characters. Each line
should be separated by a CRLF (carriage
return - line feed).
Optional Subsequence B1 - [[settlement]] Parties (Deliverer)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:
 SETPRTY
M
Deliverer
 
[[participant]] that delivers the security; for a
payment
 order the payee; for a [[collateral]]
pledge the pledgor.
:95R: :DEAG/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits
are required.
O
Deliverer's Account Number
 
Deliverer, payee, or pledgor account
number. Could be
 [[DTCC]] [[participant]]
number or the deliverer's internal account
number.
:97A: :SAFE// 35x
O
Deliverer's Serial Number
 Deliverer's Serial number :20C: :PROC// 16x
M End of Block -
 [[settlement]] Parties :16S:  SETPRTY
Optional Subsequence B1 - [[settlement]]
 Parties (Place of [[settlement]])
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - [[settlement]] Parties :16R:  SETPRTY
M
Place of [[settlement]]
 [[DTCC]] BIC Number :95P: :PSET// DTCYUS33
M End of Block -
 [[settlement]] Parties :16S:  SETPRTY

---

## Page 29

http://pbsp/ISOMessageFacility/next.[[DO]]?nextpage=documentview&rand=0.62181859548994[4/29/2011 4:07:03 PM]
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block - [[settlement]] Transaction Details :16S:  SETTRAN

---

## Page 30

[[Depository Trust Company]] - MT 548 - [[settlement]] Status (Short Version)                                                                        Non Confidential (Green) 
07[[settlement]] Status (Short Version) 
Business Transaction: [[settlement]] Status (Short Version) Version: 1.0
ISO Message Type: MT548 - [[settlement]] Status and Processing Advice
These are optional messages are sent to the [[participant]] for "non-made" state changes in IMS/ATP occurs.
 Key: M = Mandatory, O = Optional  
Mandatory Sequence A - General Information
M/O Field Description Tag
Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M [[DTCC]] Tracking Number :20C: :SEME// 16x
M
Message Function
 Field that identifies the function of the
message
:23G: INST
O
Transaction
 Update Date/Time
 Date the transmission was updated :98C: :PREP// yyyymmddhhmmss
Mandatory Subsequence
 A1 - Linkages (IMS TID)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS Transaction [[ID]]
 Inventory Management System (IMS)
transaction identifier
:20C: :RELA// 16x
M End of
 Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages ([[ID]] Control
 Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
[[ID]] Control Number
 
Unique reference used to identify
[[Institutional Delivery]] ([[ID]]) transactions
processed
 by Omgeo.
:20C: :COMM// 16x
M End of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages (Obligation Warehouse)
M/O Field
 Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK

---

## Page 31

M
Obligation Warehouse Control Number
 Obligation Warehouse Control Number for
OW DOs
:20C: :COMM//
16x
 
Note- Mandatory for OW [[DO]]
transaction. Format is 16 characters.
The first character must be W and the
remainder must be numeric. Format-
WCCYYDDDNNNNNNNN where W is a
literal, CC-Century, YY-Year, DDD-
Julian Day, NNNNNNNN-8 byte
sequential number
M End of Block - Linkages :16S:
 LINK
Mandatory Subsequence A1 - Linkages (Deliverer
 Reference Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
Deliverer's Reference Number
 Assigned by payee (deliverer) for audit
trail
:20C:
:TRRF// 16x
M End of Block - Linkages :16S:  LINK
Mandatory Subsequence A1 - Linkages (IMS
 TID of Reclaimed Transaction)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
IMS TID of Reclaimed Transaction
 
Unique transaction reference number
assigned by the
 Inventory Management
System (IMS) and used to process a
reclaim or DK (don?t know) request.
:20C: :PREV// 16x
M End of Block - Linkages :16S:
 LINK
Mandatory Subsequence A2 - Status
M/O Field Description Tag
Qualifier(s) Content Rules
M Start of Block - Status :16R:  STAT
M
Status Code
 
The IMS or ATP states assigned
 as the
transaction is processed through IMS and
ATP.
:25D: :SETT/DTCY/
4x 
Valid Status Codes: AUTH - Authorized,
CANA - ATP Cancelled, CANC - IMS
Cancelled, MAKD - Made, NAL1 - [[CNS]]
Level 1 Received, NAL2 - [[CNS]] Level 2
Received, PDRI - IMS Permanently
Dropped, PDRP - Dropped Permanent,
PREA - Pre-Authorized, PREX - Pre-
Exempted, RATP - PDC Reduction
Processed, RAUT - RAD Authorized,
RDPR - ATP Dropped Reintroduced,
RGRN - Recycling Green, RJCF - IMS
Rejected to File, RJCT - ATP Rejected,
RJCI - IMS Rejected, RLSD - Released,
RSUB - Submitted to RAD, SUBA -
Submitted to ATP, UNPR - Unprocessed,
XMPT - Exempted, XPER - Recycling
Express
Optional Subsequence A2a - Reason
M/O Field Description Tag Qualifier(s) Content Rules

---

## Page 32

http://pbsp/ISOMessageFacility/next.[[DO]]?nextpage=documentview&rand=0.4263333643310163[4/29/2011 3:45:45 PM]
M Start of Block - Reason :16R:  REAS
M
Reject Code - Field Code
 Reject code :24B: :REJT/DTCY/ 4x
O
Reject Code - Error
 Message
 Reason for the reject :70D: :REAS//
35x crlf 35x
 crlf 35x crlf 35x crlf 35x
crlf 35x 
The maximum length [[DTC]] will
accept is 210, 6 lines of 35
characters. Each line should be
separated by a CRLF (carriage
return - line feed).
M End of Block - Reason :16S:
 REAS
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block -
 Status :16S:  STAT
M/O Field Description Tag Qualifier(s) Content Rules
M End of Block -
 General Information :16S:  GENL

---

## Page 33

[[Depository Trust Company]] - MT 548 - [[settlement]] Status (IPRC Version)                                                    Non-Confidential (Green)
MT 548 [[settlement]] Status (IPRC Version) 
Business Transaction: [[settlement]] Status (IPRC Version) Version: 1.0
ISO Message Type: MT548 - [[settlement]] Status and Processing Advice
These are optional messages are sent to the [[participant]] for "non-made" state changes in IMS/ATP occurs.
 Key: M = Mandatory, O = Optional  
Mandatory Sequence A - 
General Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M [[DTCC]] Tracking Number :20C: :SEME// 16x
M
Message Function
 Field that identifies the function of
 the
message
:23G: INST
Mandatory Subsequence A1 - Linkages (Senders Reference Number)
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Linkages :16R:  LINK
M
Sender's Reference Number
 Sender's reference number :20C: :RELA// 16x
M End of Block
 - Linkages :16S:  LINK
Optional Subsequence A2 - 
Status
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Status :16R:  STAT
M
Status
 
The IMS or ATP states assigned
 as the
transaction is processed through IMS and
ATP.
:25D: :IPRC/DTCY/
Optional, Repetitive Subsequence A2a - Reason
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Reason :16R:  REAS
M
Reject Code - Field Code
 Reject code :24B: :REJT/DTCY/ 4x
Reject Code -
 Error Message
35x crlf 35x crlf 35x crlf 35x crlf 35x
crlf 35x 
The maximum length [[DTC]] will

---

## Page 34

O  Reason for the reject :70D: :REAS// accept is  210, 6 lines of 35
characters. Each line should be
separated by a CRLF (carriage
return - line feed).
M End of Block - Reason :16S:
 REAS
Optional, Repetitive Subsequence A2a
 - Reason
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Reason :16R:  REAS
M
Reject Code - Field Code
 Reject code :24B: :REJT/DTCY/ 4x
O
Reject Code -
 Error Message
 Reason for the reject :70D: :REAS//
35x crlf
 35x crlf 35x crlf 35x crlf 35x
crlf 35x 
The maximum length [[DTC]] will
accept is 210, 6 lines of 35
characters. Each line should be
separated by a CRLF (carriage
return - line feed).
M End of Block - Reason :16S:
 REAS
Optional, Repetitive Subsequence A2a
 - Reason
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Reason :16R:  REAS
M
Reject Code - Field Code
 Reject code :24B: :REJT/DTCY/ 4x
O
Reject Code -
 Error Message
 Reason for the reject :70D: :REAS//
35x crlf
 35x crlf 35x crlf 35x crlf 35x
crlf 35x 
The maximum length [[DTC]] will
accept is 210, 6 lines of 35
characters. Each line should be
separated by a CRLF (carriage
return - line feed).
M End of Block - Reason :16S:
 REAS
Optional, Repetitive Subsequence A2a
 - Reason
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Reason :16R:  REAS
M
Reject Code - Field Code
 Reject code :24B: :REJT/DTCY/ 4x
O
Reject Code -
 Error Message
 Reason for the reject :70D: :REAS//
35x crlf
 35x crlf 35x crlf 35x crlf 35x
crlf 35x 
The maximum length [[DTC]] will
accept is 210, 6 lines of 35
characters. Each line should be
separated by a CRLF (carriage
return - line feed).
M End of Block - Reason :16S:
 REAS
Optional, Repetitive Subsequence A2a
 - Reason
M/O Field Description Tag Qualifier(s) Content Rules

---

## Page 35

http://pbsp/ISOMessageFacility/next.[[DO]]?nextpage=documentview&rand=0.4946600952965591[4/29/2011 4:00:40 PM]
M Start of Block - Reason :16R:  REAS
M
Reject Code - Field Code
 Reject code :24B: :REJT/DTCY/ 4x
O
Reject Code -
 Error Message
 Reason for the reject :70D: :REAS//
35x crlf
 35x crlf 35x crlf 35x crlf 35x
crlf 35x 
The maximum length [[DTC]] will
accept is 210, 6 lines of 35
characters. Each line should be
separated by a CRLF (carriage
return - line feed).
M End of Block - Reason :16S:
 REAS
M/O Field Description Tag Qualifier(s) Content Rules
M End of
 Block - Status :16S:  STAT
M/O Field Description Tag Qualifier(s) Content Rules
M End of
 Block - General Information :16S:  GENL

---

## Page 36

Status Codes 
 
 
Code Description 
Subsequence 
A2a Reason 
If Yes, then 
the Qualifier 
will be 
AUTH Authorized No  
CANA ATP Canceled Yes CAND 
CANC IMS Canceled Yes CAND 
MAKD Made * MT547 or MT546 will be sent 
NAL1 [[CNS]] Level 1 received No  
NAL2 [[CNS]] Level 2 received No  
PDRI IMS Permanently Dropped YES PENF 
PDRP Dropped Permanent YES PENF 
PREA Pre-Authorized No  
PREX Pre-Exempted No  
RATP PDC Reduction Processed No  
RAUT RAD Authorized No  
RDPR ATM Dropped 
Reintroduced YES PENF 
RGRN Recycling Green YES PEND 
RJCF IMS Rejected to File YES REJT 
RJCT ATP rejected YES REJT 
RJCI IMS rejected YES REJT 
RLSD Released No  
RSUB Submitted to RAD No  
SUBA Submitted to ATP No  
UNPR Unprocessed No  
XMPT Exempted No  
XPER Recycling Express YES PEND 
 
 
 
 
 