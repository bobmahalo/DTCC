---
title: "ISO 15022 Message Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/15022_Segregation_Memo_InvestmentID.pdf"
pages: 11
size: "84.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO 15022 Message Layouts

**Original File:** [15022_Segregation_Memo_InvestmentID.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/15022_Segregation_Memo_InvestmentID.pdf)  
**Category:** Other  
**Total Pages:** 11  
**File Size:** 84.7 KB  

---

## Page 1

 
ISO 15022 Message Layouts 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
Segregation/Segregation 
Release/Memo 
Segregation/Investment 
[[ID]]/Investment [[ID]] 
Release Input 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
July 2011 

---

## Page 2

[[Depository Trust Company]] - ISO Message Test Facility - Segregation
Segregation 
Business Transaction: Segregation Version: 1.0
ISO
 Message Type: MT524 - Intra-Position Instruction
Sub-account segregation allows you to segregate [[securities]] from your general free account. [[securities]] are segregated
to make them unavailable for any transactions until you authorize [[DTC]] to release them to your free account.
 Key: M = Mandatory,  O = Optional  
Mandatory Sequence
 A - General Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M
Sender's Reference
 Number
 Sender's reference
 number :20C: :SEME// 16x
M
Message Function
 Field that
 identifies the function of the
message
:23G: NEWM
M End of Block - General Information :16S:  GENL
Mandatory Sequence
 B - Intra-Position Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Intra-Position Details :16R:  INPOSDET
O [[participant]] Number :95R:
:ACOW/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits are
required.
M
Safekeeper - [[DTCC]]
 Identifies account
 where financial instruments
are maintained.
:97A: :SAFE// [[DTCC]]
M
Quantity
 Quantity of
 financial instrument to be settled
expressed as units such as share quantity.
:36B: :SETT//
UNIT/999999999, 
At least 1 whole digit is required. No
more than 9 may be present. Fractions
are not allowed. A decimal comma is
always required.
M
ISIN
 Identification of
 the financial Instrument
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
M Business Transaction
 [[ID]] :22F: :FORM/DTCY/ SG01

---

## Page 3

[[Depository Trust Company]] - ISO Message Test Facility - Segregation
O
Serial Number
 Serial  number supplied by the [[participant]] :13B: :VERN/DTCY/
7x 
Serial number provided by the
[[participant]]. Permissible values are:
0000001 - 0000009 (Reg.) or 0000100
(Foreign Ownership)
O Sequence Number :70E: :FIAN// 5x
M End of Block - Financial Instrument Attributes :16S:
 FIA
M/O Field
 Description Tag Qualifier(s) Content Rules
M
[[settlement]] Date
 Date
 on which the transaction should be
settled.
:98A: :SETT// yyyymmdd
O
Narrative - [[DTC]] Comments
 Provides
 additional [[settlement]] processing
information
:70E: :SPRO//
35x crlf 35x crlf 10x 
The maximum length [[DTC]] will accept is
80, 2 lines of 35 characters and 1 line of
10 characters. Each line should be
separated by a CRLF (carriage return -
line feed).
M
Balance From
 
Balance
 from which the security is moving.
Applies to Minimum Amount (MA) or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :FROM//
AVAI 
Balance from which the security is
moving - Available
M
Balance To
 
Balance
 to which the security is moving. For
Minimum Amount (MA) account or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :TOBA//
BLOK 
Balance to which the security is moving -
Blocked
M End of Block - Intra-Position Details :16S:
 INPOSDET

---

## Page 4

[[Depository Trust Company]] - ISO Message Test Facility - Segregation Release
Segregation Release 
Business Transaction: Segregation Release Version: 1.0
ISO Message Type: MT524 - Intra-Position Instruction
Segregation release allows you to instruct [[DTC]] to release segregated [[securities]] back to your general free account.
[[securities]] are segregated to make them unavailable for any transactions until you authorize [[DTC]] to release them to
your free account.
 Key: M =  Mandatory, O = Optional  
Mandatory
 Sequence A - General Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M
Sender's
 Reference Number
 Sender's
 reference number :20C: :SEME// 16x
M
Message Function
 Field
 that identifies the function of the
message
:23G: NEWM
M End of Block - General Information :16S:  GENL
Mandatory
 Sequence B - Intra-Position Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Intra-Position Details :16R:  INPOSDET
O [[participant]]
 Number :95R: :ACOW/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits are
required.
M
Safekeeper - [[DTCC]]
 Identifies
 account where financial instruments
are maintained.
:97A: :SAFE// [[DTCC]]
M
Quantity
 Quantity
 of financial instrument to be settled
expressed as units such as share quantity.
:36B: :SETT//
UNIT/999999999, 
At least 1 whole digit is required. No
more than 9 may be present. Fractions
are not allowed. A decimal comma is
always required.
M
ISIN
 Identification
 of the financial Instrument
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

## Page 5

[[Depository Trust Company]] - ISO Message Test Facility - Segregation Release
M Business Transaction [[ID]] :22F: :FORM/DTCY/ SG02
O
Serial Number
 Serial
 number supplied by the [[participant]] :13B: :VERN/DTCY/
7x 
Serial number provided by the
[[participant]]. Permissible values are:
0000001 - 0000009 (Reg.) or 0000100
(Foreign Ownership)
O Sequence Number :70E: :FIAN// 5x
M End of Block - Financial Instrument Attributes :16S:
 FIA
M/O Field
 Description Tag Qualifier(s) Content Rules
M
[[settlement]] Date
 Date
 on which the transaction should be
settled.
:98A: :SETT// yyyymmdd
O
Narrative - [[DTC]] Comments
 Provides
 additional [[settlement]] processing
information
:70E: :SPRO//
35x crlf 35x crlf 10x 
The maximum length [[DTC]] will accept is
80, 2 lines of 35 characters and 1 line of
10 characters. Each line should be
separated by a CRLF (carriage return -
line feed).
M
Balance From
 
Balance
 from which the security is moving.
Applies to Minimum Amount (MA) or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :FROM//
BLOK 
Balance from which the security is
moving - Blocked
M
Balance To
 
Balance
 to which the security is moving. For
Minimum Amount (MA) account or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :TOBA//
AVAI 
Balance to which the security is moving -
Available
M End of Block - Intra-Position Details :16S:
 INPOSDET

---

## Page 6

[[Depository Trust Company]] - ISO Message Test Facility - Memo Segregation
Memo Segregation 
Business Transaction: Memo Segregation Version: 1.0
ISO Message Type: MT524 - Intra-Position Instruction
Memo Segregation allows you to create a memo position within your general free account to protect [[securities]] that
your customers have paid for in full. Memo segregation is similar to segregation. However, whereas Segregation allows
you to move only existing positions, Memo Segregation allows you to create memo-segregated positions within your
free account, thus allowing you to protect anticipated, fully-paid-for customer [[securities]].
 Key: M =  Mandatory, O = Optional  
Mandatory
 Sequence A - General Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M
Sender's
 Reference Number
 Sender's
 reference number :20C: :SEME// 16x
M
Message Function
 Field
 that identifies the function of the
message
:23G: NEWM
M End of Block - General Information :16S:  GENL
Mandatory
 Sequence B - Intra-Position Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Intra-Position Details :16R:  INPOSDET
O [[participant]]
 Number :95R: :ACOW/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits are
required.
M
Safekeeper - [[DTCC]]
 Identifies
 account where financial instruments
are maintained.
:97A: :SAFE// [[DTCC]]
M
Quantity
 Quantity
 of financial instrument to be settled
expressed as units such as share quantity.
:36B: :SETT//
UNIT/999999999, 
At least 1 whole digit is required. No
more than 9 may be present. Fractions
are not allowed. A decimal comma is
always required.
M
ISIN
 Identification
 of the financial Instrument
(Country Code, [[CUSIP]] and Check Digit)
:35B:
The literal "ISIN" followed by a space
followed by the 12 character ISIN. Note-
[[DTC]] does not accept Non U.S. ISIN 
Example-ISIN US1234567891. Note-[[DTC]]
does not accept Non U.S. ISIN
Optional Subsequence B1 - Financial Instrument Attributes
M/O Field Description Tag Qualifier(s) Content Rules

---

## Page 7

[[Depository Trust Company]] - ISO Message Test Facility - Memo Segregation
M Start of Block - Financial Instrument Attributes :16R:  FIA
M Business
 Transaction [[ID]] :22F: :FORM/DTCY/ MS01
O Action Code :22F: :PADI/DTCY/
ADDS or SUBS or OVRL 
Must be one of the following values:
ADDS - Add to existing [[shares]], SUBS -
Subtract from existing [[shares]], OVRL -
Overlay existing [[shares]]
O Sequence Number :70E: :FIAN// 5x
M End of Block - Financial Instrument Attributes :16S:
 FIA
M/O Field
 Description Tag Qualifier(s) Content Rules
M
[[settlement]] Date
 Date
 on which the transaction should be
settled.
:98A: :SETT// yyyymmdd
O
Narrative - [[DTC]] Comments
 Provides
 additional [[settlement]] processing
information
:70E: :SPRO//
35x crlf 35x crlf 10x 
The maximum length [[DTC]] will accept is
80, 2 lines of 35 characters and 1 line of
10 characters. Each line should be
separated by a CRLF (carriage return -
line feed).
M
Balance From
 
Balance
 from which the security is moving.
Applies to Minimum Amount (MA) or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :FROM//
AVAI 
Balance from which the security is
moving - Available
M
Balance To
 
Balance
 to which the security is moving. For
Minimum Amount (MA) account or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :TOBA//
BLOK 
Balance to which the security is moving -
Blocked
M End of Block - Intra-Position Details :16S:
 INPOSDET

---

## Page 8

[[Depository Trust Company]] - ISO Message Test Facility - Investment [[ID]]
Investment [[ID]] 
Business Transaction: Investment [[ID]] Version: 1.0
ISO Message Type: MT524 - Intra-Position Instruction
Investment Identification allows you to segregate [[securities]] for a Firm, Partner, or Omnibus account that were
purchased for investment reasons. The [[securities]] are delivered from your general free account into your Investment
Identification account. The Investment [[ID]] account is used for reporting information to the IRS about [[securities]]
purchased for investment purposes.
 Key: M =  Mandatory, O = Optional  
Mandatory
 Sequence A - General Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M
Sender's
 Reference Number
 Sender's
 reference number :20C: :SEME// 16x
M
Message Function
 Field
 that identifies the function of the
message
:23G: NEWM
M End of Block - General Information :16S:  GENL
Mandatory
 Sequence B - Intra-Position Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Intra-Position Details :16R:  INPOSDET
O [[participant]]
 Number :95R: :ACOW/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits are
required.
M
Safekeeper - [[DTCC]]
 Identifies
 account where financial instruments
are maintained.
:97A: :SAFE// [[DTCC]]
M
Quantity
 Quantity
 of financial instrument to be settled
expressed as units such as share quantity.
:36B: :SETT//
UNIT/999999999, 
At least 1 whole digit is required. No
more than 9 may be present. Fractions
are not allowed. A decimal comma is
always required.
M
ISIN
 Identification
 of the financial Instrument
(Country Code, [[CUSIP]] and Check Digit)
:35B:
The literal "ISIN" followed by a space
followed by the 12 character ISIN. Note-
[[DTC]] does not accept Non U.S. ISIN 
Example-ISIN US1234567891. Note-[[DTC]]
does not accept Non U.S. ISIN
Optional Subsequence B1 - Financial Instrument Attributes
M/O Field Description Tag Qualifier(s) Content Rules

---

## Page 9

[[Depository Trust Company]] - ISO Message Test Facility - Investment [[ID]]
M Start of Block - Financial Instrument Attributes :16R:  FIA
M Business
 Transaction [[ID]] :22F: :FORM/DTCY/ IN01
O
Serial Number
 Serial
 number supplied by the [[participant]] :13B: :VERN/DTCY/
7x 
Serial number provided by the
[[participant]]. Permissible values are:
0100001 - 0199999 (Firm), 0200001 -
0299999 (Partner), 0300001 - 0399999
(Omnibus)
O Sequence Number :70E: :FIAN// 5x
M End of Block - Financial Instrument Attributes :16S:
 FIA
M/O Field
 Description Tag Qualifier(s) Content Rules
M
[[settlement]] Date
 Date
 on which the transaction should be
settled.
:98A: :SETT// yyyymmdd
O
Narrative - [[DTC]] Comments
 Provides
 additional [[settlement]] processing
information
:70E: :SPRO//
35x crlf 35x crlf 10x 
The maximum length [[DTC]] will accept is
80, 2 lines of 35 characters and 1 line of
10 characters. Each line should be
separated by a CRLF (carriage return -
line feed).
M
Balance From
 
Balance
 from which the security is moving.
Applies to Minimum Amount (MA) or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :FROM//
AVAI 
Balance from which the security is
moving - Available
M
Balance To
 
Balance
 to which the security is moving. For
Minimum Amount (MA) account or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :TOBA//
BLOK 
Balance to which the security is moving -
Blocked
M End of Block - Intra-Position Details :16S:
 INPOSDET

---

## Page 10

[[Depository Trust Company]] - ISO Message Test Facility - Investment [[ID]] Release
Investment [[ID]] Release 
Business Transaction: Investment [[ID]] Release Version: 1.0
ISO Message Type: MT524 - Intra-Position Instruction
[[securities]] that are segregated via Investment Identification for Internal Revenue Service purposes can be released
back to your general free account. Use Investment [[ID]] Release to release [[securities]] segregated specifically for
investment purposes.
 Key: M =  Mandatory, O = Optional  
Mandatory
 Sequence A - General Information
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - General Information :16R:  GENL
M
Sender's
 Reference Number
 Sender's
 reference number :20C: :SEME// 16x
M
Message Function
 Field
 that identifies the function of the
message
:23G: NEWM
M End of Block - General Information :16S:  GENL
Mandatory
 Sequence B - Intra-Position Details
M/O Field Description Tag Qualifier(s) Content Rules
M Start of Block - Intra-Position Details :16R:  INPOSDET
O [[participant]]
 Number :95R: :ACOW/DTCYPART/
00009999 
0000 followed by 4 digits. All 4 digits are
required.
M
Safekeeper - [[DTCC]]
 Identifies
 account where financial instruments
are maintained.
:97A: :SAFE// [[DTCC]]
M
Quantity
 Quantity
 of financial instrument to be settled
expressed as units such as share quantity.
:36B: :SETT//
UNIT/999999999, 
At least 1 whole digit is required. No
more than 9 may be present. Fractions
are not allowed. A decimal comma is
always required.
M
ISIN
 Identification
 of the financial Instrument
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

## Page 11

[[Depository Trust Company]] - ISO Message Test Facility - Investment [[ID]] Release
M Business Transaction [[ID]] :22F: :FORM/DTCY/ IN02
O
Serial Number
 Serial
 number supplied by the [[participant]] :13B: :VERN/DTCY/
7x 
Serial number provided by the
[[participant]]. Permissible values are:
0100001 - 0199999 (Firm), 0200001 -
0299999 (Partner), 0300001 - 0399999
(Omnibus)
O Sequence Number :70E: :FIAN// 5x
M End of Block - Financial Instrument Attributes :16S:
 FIA
M/O Field
 Description Tag Qualifier(s) Content Rules
M
[[settlement]] Date
 Date
 on which the transaction should be
settled.
:98A: :SETT// yyyymmdd
O
Narrative - [[DTC]] Comments
 Provides
 additional [[settlement]] processing
information
:70E: :SPRO//
35x crlf 35x crlf 10x 
The maximum length [[DTC]] will accept is
80, 2 lines of 35 characters and 1 line of
10 characters. Each line should be
separated by a CRLF (carriage return -
line feed).
M
Balance From
 
Balance
 from which the security is moving.
Applies to Minimum Amount (MA) or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :FROM//
BLOK 
Balance from which the security is
moving - Blocked
M
Balance To
 
Balance
 to which the security is moving. For
Minimum Amount (MA) account or Net
Additions (NA) account position transfers. Also
used to designate [[securities]] as available or
blocked for segregation, memo segregation,
and Investment [[ID]].
:93A: :TOBA//
AVAI 
Balance to which the security is moving -
Available
M End of Block - Intra-Position Details :16S:
 INPOSDET