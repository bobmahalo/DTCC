---
title: "Microsoft Word - MT548 - Settlement Status (Short Version) File Specification for Settlement Matching.docx"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MT548_Short_Version_File_Spec_for_Settlement_Matching.pdf"
pages: 3
size: "47.9 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# Microsoft Word - MT548 - Settlement Status (Short Version) File Specification for Settlement Matching.docx

**Original File:** [MT548_Short_Version_File_Spec_for_Settlement_Matching.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MT548_Short_Version_File_Spec_for_Settlement_Matching.pdf)  
**Category:** Rules  
**Total Pages:** 3  
**File Size:** 47.9 KB  

---

## Page 1

 
[[settlement]] Status (Short Version)  
Business Transaction: [[settlement]] Status (Short Version)  Version: 1.0  
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

M  Start of Block - Linkages  :16R:    LINK  
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
  
 
Mandatory Subsequence A1 - Linkages (IMS TID of Reclaimed Transaction)  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  Start of Block - Linkages  :16R:    LINK  
O  
IMS TID of Reclaimed Transaction  
  
Unique transaction reference 
number assigned by the Inventory 
Management System (IMS) and 
used to process a reclaim or DK 
(don t know) request. 
 
:20C: :PREV//  16x  
M  End of Block - Linkages  :16S:    LINK  
  
 
Mandatory Subsequence A2 - Status  
M/O Field Description  Tag  Qualifier(s)  Content Rules  
M  
 
 
 
 
 
 
 
Start of Block - Status  
 
 
 
 
 
 
:16R:    STAT  

---

## Page 3

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
Express , RXMP – Receiver 
RAD Exempt
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