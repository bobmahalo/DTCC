---
title: "ISO 15022 Message Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/15022_MA_NA_PositionTransfer.pdf"
pages: 3
size: "43.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO 15022 Message Layouts

**Original File:** [15022_MA_NA_PositionTransfer.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/15022_MA_NA_PositionTransfer.pdf)  
**Category:** Other  
**Total Pages:** 3  
**File Size:** 43.2 KB  

---

## Page 1

 
ISO 15022 Message Layouts 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
MA/NA Position 
Transfer 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
July 2011 

---

## Page 2

[[Depository Trust Company]] - 07MA/NA Position Transfer1RQ&RQILGHQWLDO*UHHQ
MA/NA Position Transfer 
Business Transaction: MA/NA Position Transfer Version: 1.0
ISO Message
 Type: MT524 - Intra-Position Instruction
MA/NA Position Transfer allows you to make same-day position transfers from your Minimum Amount (MA) account to
your Net Additions (NA) account and vice-versa. Day Transfer Position results in same-day position transfers. Night
Transfer Position results in same-day night cycle position transfers.
 Key: M = Mandatory, O  = Optional  
Mandatory Sequence A
 - General Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M
Sender's Reference Number
 Sender's reference number :20C:
:SEME// 16x
M
Message Function
 Field that identifies
 the function of the
message
:23G: NEWM
M End of Block - General Information :16S:  GENL
Mandatory Sequence B
 - Intra-Position Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Intra-Position Details :16R:  INPOSDET
O [[participant]] Number :95R: :ACOW/DTCYPART/
00009999
 
0000 followed by 4 digits. All 4 digits are
required.
M
Safekeeper - [[DTCC]]
 Identifies account where
 financial instruments
are maintained.
:97A: :SAFE// [[DTCC]]
M
Quantity
 Quantity of financial
 instrument to be settled
expressed as units such as share quantity.
:36B: :SETT//
UNIT/999999999, 
At least 1 whole digit is required. No
more than 9 may be present. Fractions
are not allowed. A decimal comma is
always required.
M
ISIN
 Identification of the
 financial Instrument
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

---

## Page 3

[[Depository Trust Company]] - ISO Message Test Facility - MA/NA Position Transfer
M Business Transaction [[ID]] :22F: :FORM/DTCY/ MN01
M End of Block - Financial Instrument Attributes :16S:  FIA
M/O Field
 Description Tag Qualifier(s) Content Rules
M
[[settlement]] Date
 Date
 on which the transaction should be
settled.
:98A: :SETT// yyyymmdd
M
Balance From
 
Balance
 from which the security is moving.
Applies to Minimum Amount (MA) or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :FROM/DTCY/
MAAC or NAAC 
Balance from which the security is
moving - MA or NA
M
Balance To
 
Balance
 to which the security is moving. For
Minimum Amount (MA) account or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :TOBA/DTCY/
MAAC or NAAC 
Balance to which the security is moving -
MA or NA
M End of Block - Intra-Position Details :16S:
 INPOSDET