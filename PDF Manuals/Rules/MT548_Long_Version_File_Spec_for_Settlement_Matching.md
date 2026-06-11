---
title: "Microsoft Word - MT548 -  Settlement Status (Long Version) File Specification for Settlement Matching.docx"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MT548_Long_Version_File_Spec_for_Settlement_Matching.pdf"
pages: 6
size: "91.3 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# Microsoft Word - MT548 -  Settlement Status (Long Version) File Specification for Settlement Matching.docx

**Original File:** [MT548_Long_Version_File_Spec_for_Settlement_Matching.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MT548_Long_Version_File_Spec_for_Settlement_Matching.pdf)  
**Category:** Rules  
**Total Pages:** 6  
**File Size:** 91.3 KB  

---

## Page 1

 
[[settlement]] Status (Long Version)  
Business Transaction: [[settlement]] Status (Long Version)  Version: 1.0  
ISO Message Type: MT548 - [[settlement]] Status and Processing Advice  
These are optional messages are sent to the [[participant]] for "non-made" state changes in IMS/ATP 
occurs.  
 
 Key: M = Mandatory, O = Optional   
 
Mandatory Sequence A - General Information  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - General Information  :16R:    GENL  
O  [[DTCC]] Tracking Number  :20C: :SEME//  16x  
O  
Message Function  
  Field that identifies the function of the 
message 
 
:23G:  INST  
O  
Transaction Update Date/Time  
  Date the transmission was updated 
 
:98C: :PREP//  yyyymmddhhmmss  
 
Mandatory Subsequence A1 - Linkages (IMS TID)  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - Linkages  :16R:    LINK  
O  
IMS Transaction [[ID]]  
  Inventory Management System 
(IMS) transaction identifier 
 
:20C: :RELA//  16x  
M  End of Block - Linkages  :16S:    LINK  
  
 
Mandatory Subsequence A1 - Linkages ([[ID]] Control Number)  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - Linkages  :16R:    LINK  
O  
[[ID]] Control Number  
  
Unique reference used to identify 
[[Institutional Delivery]] ([[ID]]) 
transactions processed by Omgeo. 
 
:20C: :COMM//  16x  
M  End of Block - Linkages  :16S:    LINK  
  
 
Mandatory Subsequence A1 - Linkages (Obligation Warehouse)  
M/O Field Description  Tag  Qualifier(s)  Content Rules  

---

## Page 2

M  Start of Block - Linkages :16R: LINK  
O  
Obligation Warehouse Control Number 
Obligation Warehouse Control 
Number for OW DOs 
:20C: :COMM//  
16x  
Note- Mandatory for OW [[DO]] 
transaction. Format is 16 
characters. The first character 
must be W and the remainder 
must be numeric. Format- 
WCCYYDDDNNNNNNNN where W 
is a literal, CC-Century, YY-Year, 
DDD-Julian Day, NNNNNNNN-8
byte sequential number
M  End of Block - Linkages :16S: LINK  
Mandatory Subsequence A1 - Linkages (Deliverer Reference Number)  
M/O Field Description  Tag  Qualifier(s) Content Rules 
M  Start of Block - Linkages :16R: LINK  
O  
Deliverer's Reference Number 
Assigned by payee (deliverer) for 
audit trail 
:20C: :TRRF//  16x  
M  End of Block - Linkages :16S: LINK  
Mandatory Subsequence A1 - Linkages (IMS TID of Reclaimed Transaction) 
M/O Field Description  Tag  Qualifier(s) Content Rules 
M  Start of Block - Linkages :16R: LINK  
O  
IMS TID of Reclaimed Transaction  
Unique transaction reference 
number assigned by the Inventory 
Management System (IMS) and 
used to process a reclaim or DK 
(don t know) request. 
:20C: :PREV//  16x  
M  End of Block - Linkages :16S: LINK  
Mandatory Subsequence A2 - Status  
M/O Field Description  Tag  Qualifier(s) Content Rules 
M  Start of Block - Status :16R: STAT  
O  
Status Code 
The IMS or ATP states assigned as 
the transaction is processed 
through IMS and ATP. 
:25D: :SETT/DTCY/ 
4x  
Valid Status Codes: AUTH - 
Authorized, CANA - ATP 
Cancelled, CANC - IMS 
Cancelled, MAKD - Made, NAL1 
- [[CNS]] Level 1 Received, NAL2
- [[CNS]] Level 2 Received, PDRI -
IMS Permanently Dropped,
PDRP - Dropped Permanent,
PREA - Pre-Authorized, PREX - 

---

## Page 3

Pre-Exempted, RATP - PDC 
Reduction Processed, RAUT - 
RAD Authorized, RDPR - ATP 
Dropped Reintroduced, RGRN - 
Recycling Green, RJCF - IMS 
Rejected to File, RJCT - ATP 
Rejected, RJCI - IMS Rejected, 
RLSD - Released, RSUB - 
Submitted to RAD, SUBA - 
Submitted to ATP, UNPR - 
Unprocessed, XMPT - 
Exempted, XPER - Recycling 
Express , RXMP – Receiver 
RAD exempt 
Optional Subsequence A2a - Reason  
M/O Field Description  Tag  Qualifier(s) Content Rules 
M  Start of Block - Reason  :16R: REAS  
O  
Reject Code - Field Code 
Reject code :24B: :REJT/DTCY/ 4x  
O  
Reject Code - Error Message 
Reason for the reject :70D: :REAS//  
35x crlf 35x crlf 35x crlf 35x 
crlf 35x crlf 35x  
The maximum length [[DTC]] will 
accept is 210, 6 lines of 35 
characters. Each line should 
be separated by a CRLF 
(carriage return - line feed).  
M  End of Block - Reason :16S: REAS  
M/O Field Description  Tag  Qualifier(s) Content Rules 
M  End of Block - Status :16S: STAT  
M/O Field Description  Tag  Qualifier(s) Content Rules 
M  End of Block - General Information  :16S: GENL  
Optional Sequence B - [[settlement]] Transaction Details 
M/O Field Description  Tag Qualifier(s)  Content Rules 
M  Start of Block - [[settlement]] Transaction 
Details  :16R: SETTRAN  
O  
ISIN  
Identification of the financial 
Instrument (Country Code, [[CUSIP]] 
and Check Digit) 
:35B: 
The literal "ISIN" followed by a 
space followed by the 12 
character ISIN. Note-[[DTC]] does 
not accept Non U.S. ISIN  
Example-ISIN US1234567891. 
Note-[[DTC]] does not accept Non 
U.S. ISIN  
O  
Quantity  
Quantity of financial instrument to 
be settled expressed as units such 
as share quantity. 
:36B: :SETT//  
UNIT/999999999,  
At least 1 whole digit is 
required. No more than 9 may 
be present. Fractions are not 
allowed. A decimal comma is 

---

## Page 4

always required.  
O  
[[settlement]] Amount  
  Dollar Amount that was settled with 
regards to this transaction. 
 
:19A: :SETT//  
USD9999999999,99  
USD followed by at least 1 
whole digit. No more than 10 
whole digits may be present. 
Fractional digits are optional, 
but no more than 2 may be 
present. A decimal comma is 
always required.  
O  
Safekeeper  
  Identifies account where financial 
instruments are maintained. 
 
:97A: :SAFE//  35x  
O  
Reason Code  
  
The reason code for the transaction. 
This required field must be filled 
with a 2-character alpha-numeric 
reason code defined by [[DTC]]. The 
validity of a reason code is partly 
dependent upon the time of 
transmission. 
 
:22F:  :SETR/DTCYREAS/  
4x  
0 followed by 3 digit [[DTCC]] 
reason code.  
O  Receiver/Deliverer Indicator  :22H: :REDE//  
DELI or RECE  
Valid Values: DELI - indicates 
that you are the deliverer or 
RECE - indicates that you are 
the receiver  
O  
Payment Indicator  
  Indicates whether the underlying 
[[securities]] are free or valued 
 
:22H: :PAYM//  
APMT or FREE  
Valid values: APMT - indicates a 
valued transaction or FREE - 
indicates a free transaction  
O  
Internal Source Code  
  Identifies the input media for the 
transaction 
 
:22F:  :STCO/DTCYISRC  4x  
O  
Transaction Type  
  IMS transaction type 
 
:22F:  :STCO/DTCYTXNT/ 4x  
O  
Activity Code  
  A code identifying a transaction. 
 
:22F:  :STCO/DTCYACTV  4x  
O  
3rd Party Status Indicator  
  Indicator used for the Third Party 
approvals status. 
 
:22F:  :STCO/DTCY/  
TRDP or TRDA or TRDD  
The IMS state for Third Party 
approvals. TRDP - Pending 
Approval, TRDA - Approved, 
TRDD - Disapproved.  
O  
[[CNS]] Level Indicator  
  
Indicates how [[CNS]] short (levels 1 
and 2) and long (level 4) [[shares]] 
should be processed. I.e. Short 
[[shares]] can be exempted and long 
[[shares]] anticipated. 
 
:22F:  :SETS/DTCY/  LVL1, LVL2, LVL3, LVL4 or LVLL  
O  
Actual [[settlement]] Date  
  Date at which the transaction was 
actually settled on. 
 
:98A: :EXSE//  yyyymmdd  
O  
[[settlement]] Date  
  Date on which the transaction 
should be settled. 
 
:98A: :SETT//  yyyymmdd  
O  Contract/Trade Date  :98A: :TRAD//  yyyymmdd  

---

## Page 5

  
The contract date for an security 
payment order. The delivery date is 
the contract date and is required for 
reason codes. 
 
O  
Narrative - [[DTC]] [[DO]] Comments  
  Provides additional [[settlement]] 
processing information 
 
:70E:  :SPRO//  
35x crlf 35x crlf 35x crlf 35x crlf 
35x crlf 35x crlf 35x crlf 35x crlf 
35x crlf 35x  
The maximum length [[DTC]] will 
accept is 350, 10 lines of 35 
characters. Each line should be 
separated by a CRLF (carriage 
return - line feed).  
 
Optional Subsequence B1 - [[settlement]] Parties (Deliverer)  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - [[settlement]] Parties  :16R:    SETPRTY  
O  
Deliverer  
  
[[participant]] that delivers the 
security; for a payment order 
the payee; for a [[collateral]] 
pledge the pledgor. 
 
:95R: :DEAG/DTCYPART/ 
00009999  
0000 followed by 4 digits. All 4 
digits are required.  
O  
Deliverer's [[intermediary]] 1  
  Deliverer's [[intermediary]] 1 
 
:95Q: DEI1/  35x  
max 4 lines of 35 bytes  
O  
Deliverer's [[intermediary]] 2  
  Deliverer's [[intermediary]] 2 
 
:95R: DEI2/OCCX  34x  
max 34 bytes  
O  
Deliverer's Account Number  
  
Deliverer, payee, or pledgor 
account number. Could be [[DTCC]] 
[[participant]] number or the 
deliverer's internal account 
number. 
 
:97A: :SAFE//  35x  
M  End of Block - [[settlement]] Parties  :16S:    SETPRTY  
  
 
Optional Subsequence B1 - [[settlement]] Parties (Receiver)  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - [[settlement]] Parties  :16R:    SETPRTY  
O  
Receiver  
  
[[participant]] that receives the 
security; for a payment order, 
the payor; for a [[collateral]] pledge 
the pledgee. 
 
:95R: :REAG/DTCYPART/ 
00009999  
0000 followed by 4 digits. All 4 
digits are required.  
O  
Receiver's [[intermediary]] 1  
  Receiver's [[intermediary]] 1 
 
:95Q: REI1/  35x  
max 4 lines of 35 bytes  
O  
Receiver's [[intermediary]] 2  
  Receiver's [[intermediary]] 2 
 
:95R: REI2/OCCX  34x  
max 34 bytes  
O  
Receiver's Account Number  
  Receiver, payor, or pledgee :97A: :SAFE//  35x  

---

## Page 6

account number. Could be [[DTCC]] 
[[participant]] number or the 
receiver's internal account 
number. 
 
M  End of Block - [[settlement]] Parties  :16S:    SETPRTY  
  
 
Optional Subsequence B1 - [[settlement]] Parties (Place of [[settlement]])  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - [[settlement]] Parties  :16R:    SETPRTY  
O  
Place of [[settlement]]  
  [[DTCC]] BIC Number 
 
:95P: :PSET//  DTCYUS33  
M  End of Block - [[settlement]] Parties  :16S:    SETPRTY  
  
 
Optional Subsequence B1 - [[settlement]] Parties (Deliverer - [[intermediary]])  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - [[settlement]] Parties  :16R:    SETPRTY  
O  
Deliverer's [[intermediary]]  
  Depository Third Party field 
 
:95R: :DEI1/DTCYPART 34x  
M  End of Block - [[settlement]] Parties  :16S:    SETPRTY  
  
 
Optional Subsequence B1 - [[settlement]] Parties (Receiver - [[intermediary]])  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - [[settlement]] Parties  :16R:    SETPRTY  
O  
Receiver's [[intermediary]]  
  Depository Third Party field 
 
:95R: :REI1/DTCYPART 34x  
M  End of Block - [[settlement]] Parties  :16S:    SETPRTY  
  
 
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  End of Block - [[settlement]] Transaction 
Details  :16S:    SETTRAN  
  
 
 