---
title: "Microsoft Word - MT548 - Settlement Status (Long Version) for Accounting File Specification for Settlement Matching.docx"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MT548_Long_Version_Accounting_for_Settlement_Matching.pdf"
pages: 4
size: "71.9 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# Microsoft Word - MT548 - Settlement Status (Long Version) for Accounting File Specification for Settlement Matching.docx

**Original File:** [MT548_Long_Version_Accounting_for_Settlement_Matching.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MT548_Long_Version_Accounting_for_Settlement_Matching.pdf)  
**Category:** Rules  
**Total Pages:** 4  
**File Size:** 71.9 KB  

---

## Page 1

[[settlement]] Status (Long Version) for Accounting  
Business Transaction: [[settlement]] Status (Long Version) for Accounting  Version: 1.0  
ISO Message Type: MT548 - [[settlement]] Status and Processing Advice  
These are optional messages are sent to the [[participant]] for all state changes including "Made" in 
IMS/ATP occurs.  
 
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
  
 
Mandatory Subsequence A1 - Linkages (Deliverer Reference Number)  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - Linkages  :16R:    LINK  
O  
Deliverer's Reference Number  
  Assigned by payee (deliverer) for 
audit trail 
 
:20C: :TRRF//  16x  
M  End of Block - Linkages  :16S:    LINK  
  
 
Mandatory Subsequence A2 - Status  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - Status  :16R:    STAT  
 

---

## Page 2

O  
Status Code 
The IMS or ATP states assigned as 
the transaction is processed 
through IMS and ATP. :25D: :SETT/DTCY/ 
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
U
nprocessed, XMPT -
Exempted, XPER - Recycling 
Express, RXMP – Receiver RAD 
Exempt
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
M/O Field Description  Tag Qualifier(s) Content Rules 
M  End of Block - General Information  :16S: GENL  
Optional Sequence B - [[settlement]] Transaction Details 
M/O Field Description  Tag Qualifier(s)  Content Rules 
M  Start of Block - [[settlement]] Transaction 
Details  :16R: SETTRAN  
O  
ISIN  
Identification of the financial :35B: 
The literal "ISIN" followed by a 
space followed by the 12 
character ISIN. Note-[[DTC]] does 

---

## Page 3

Instrument (Country Code, [[CUSIP]] 
and Check Digit) 
 
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
always required.  
O  
Safekeeper  
  Identifies account where financial 
instruments are maintained. 
 
:97A: :SAFE//  35x  
O  Action Code  :22F:  :SETR/DTCY/  
ADDS or SUBS or OVRL  
Must be one of the following 
values: ADDS - Add to existing 
[[shares]], SUBS - Subtract from 
existing [[shares]], OVRL - Overlay 
existing [[shares]]  
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
Actual [[settlement]] Date  
  Date at which the transaction was 
actually settled on. 
 
:98A: :EXSE//  yyyymmdd  
O  
[[settlement]] Date  
  Date on which the transaction 
should be settled. 
 
:98A: :SETT//  yyyymmdd  
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

---

## Page 4

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
Deliverer's Account Number  
  
Deliverer, payee, or pledgor 
account number. Could be [[DTCC]] 
[[participant]] number or the 
deliverer's internal account 
number. 
 
:97A: :SAFE//  35x  
O  
Deliverer's Serial Number  
  Deliverer's Serial number 
 
:20C: :PROC//  16x  
M  End of Block - [[settlement]] Parties  :16S:    SETPRTY  
  
 
Optional Subsequence B1 - [[settlement]] Parties (Place of [[settlement]])  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - [[settlement]] Parties  :16R:    SETPRTY  
O  
Place of [[settlement]]  
  [[DTCC]] BIC Number 
 
:95P: :PSET//  DTCYUS33  
M  End of Block - [[settlement]] Parties  :16S:    SETPRTY  
  
 
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  End of Block - [[settlement]] Transaction 
Details  :16S:    SETTRAN  
  
 
 