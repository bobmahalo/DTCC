---
title: "CSV File Format Specification"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sim021_csv_file_format_spec_20231010.pdf"
pages: 64
size: "1131.3 KB"
category: "SIM"
ingested_on: "2026-06-05"
---

# CSV File Format Specification

**Original File:** [sim021_csv_file_format_spec_20231010.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sim021_csv_file_format_spec_20231010.pdf)  
**Category:** SIM  
**Total Pages:** 64  
**File Size:** 1131.3 KB  

---

## Page 1

[[settlement]] Instruction Manager
CSV FILE FORMAT SPECIFICATION
OCTOBER 10, 2023
 

---

## Page 2

TABLE OF CONTENTS
Preface 4
Audience 4
Changes in this Version of the Document 4
Related Documents and Training 4
Questions? 5
1. CSV File 6
Introduction 6
Overview 6
File Naming and Other Applicable Rules 7
SWIFT Fields, Codes, and Sample Values 8
Mapping SWIFT Fields with Multiple or Concatenated Values to CSV 9
Handling Fields with Multiple Values 9
Concatenated Values 9
Narrative Value ([[settlement]] Instruction Processing Narrative) 9
CSV File Layout 10
Cross Currency Trade 51
Delivering/Receiving Agent Mapping (95a DEAG/REAG) 52
Handling of non-SWIFT characters in text fields 53
Support of CTM Organizations without Valid Registered SWIFT BIC 54
Example of a CSV File 54
CSVFileFormatSpecification
TableOfContents 3

---

## Page 3

PREFACE
This document provides comprehensive information on the CSV file format containing [[settlement]] 
instructions generated by Settlements Instruction Manager for release to [[Custodians]] and interested parties 
that [[DO]] not have SWIFT connectivity. This caters to organizations subscribed to Post Trade [[settlement]] 
Notifications service and optionally subscribed to the Post Trade [[settlement]] Notification – Pre MAGR 
service.
Audience
Read this manual if your business requirements include the following:
 l Investment managers who use CTM and wish to send CSV messages at Match Agreed (MAGR), 
Cancel Match Agreed, or Pre Match Agreed (NMAG) to their custodian, other parties, and/or their own 
organization.
 l Brokers who use CTM and wish to send CSV messages at Match Agreed (MAGR) and Cancel Match 
Agreed to their custodian, other parties, and/or their own organization.
 l [[Custodians]], banks, third parties, and executing brokers who receive CSV messages from their invest-
ment manager   or [[Broker]] clients via [[settlement]] Instruction Manager.
Note
[[DTCC]] offers [[settlement]] services only for the party that identifies as the InstructingParty or ExecutingBroker on             trade 
components.
Since both parties to a trade supply extensive enrichment of allocations and contracts (also known as 
confirmations) this reference is for both trade sides.
Changes in this Version of the Document
This version of the document includes changes based on the 2023 Functional Release 4. The section 
Support of CTM Organizations without Valid Registered SWIFT BIC has been added.
Related Documents and Training
For related documents and training, see [[settlement]] Instruction Manager on the [[DTCC]] Learning Center.
CSVFileFormatSpecification
Preface 4

---

## Page 4

Questions?
The Client Center provides general assistance and technical help. Visit to:
 l Enter a service request or check the status of an existing service request.
 l Search the knowledge base.
 l Obtain contact information.
CSVFileFormatSpecification
Preface 5

---

## Page 5

1. CSV FILE
Introduction
This chapter describes the CSV file layout and includes an example CSV file. The Settlements Instruction 
Manager service supports the creating of CSV file
 l once the allocation has reached Match Agreed (MAGR) and Cancel Match Agreed (CMAG) in CTM,
 l upon a user taking an action to Release, Amend or Cancel within the [[settlement]] Instruction Manager 
UI
 l and optionally at Pre Match Agreed (NMAG) if the user initiates that workflow from CTM.
Overview
The [[settlement]] Instruction Manager service provides the [[Option]] of constructing a CSV file containing 
[[settlement]] instructions for release to [[Custodians]] and interested parties. It releases the CSV notifications 
using secure File Transfer Protocol (SFTP) as the delivery method.
With a CSV file, the [[settlement]] Instruction Manager service:
 l Constructs [[settlement]] instructions and releases [[settlement]] notifications to [[Custodians]] and interested 
parties
 l Provides multiple parties that [[DO]] not have SWIFT connectivity with relevant trade data in CSV format.
The data included in the CSV file conforms to SWIFT formatting, data length, and optional/mandatory rules 
and specifications.
The CSV file contains MT541/543 message fields and several administrative fields. The CSV file 
represents MT541/543 fields using the X character set.
The administrative fields in the CSV file display all the special characters that are used for corresponding 
fields in the [[settlement]] Instruction Manager service. For example, the [[settlement]] Instruction Manager 
service represents the CTM's MasterReference administrative field with a value of “ABCabc%#123”   as 
“ABCabc%#123” in a CSV file.
Note
For more information about CTM format notation and the X character set, refer to the CTM XML Message Spe-
cification corresponding to your [[Asset]] class.
CSVFileFormatSpecification
1.CSVFile 6

---

## Page 6

File Naming and Other Applicable Rules
The file naming convention in the [[settlement]] Instruction Manager service is:
<NEWM/CANC><underscore><Notification [[ID]]><underscore><Notification 
Order><underscore><Timestamp><period>csv
Example:
NEWM_80008983_1_03142014_141458.csv
When creating CSV files, the [[settlement]] Instruction Manager service applies the following rules:
 l The CSV file contains all mandatory MT541/543 SWIFT fields and required administrative fields.
 l The [[settlement]] Instruction Manager service uses the same validation rules processing as SWIFT. 
Fields you submit must be constructed and ordered in accordance with those rules.
 l Fields in the CSV file structure use the same formatting rules and fulfill the same mandatory/optional 
requirements as the SWIFT fields. For example, if [[settlement]] Date is formatted as 20161203 in an 
MT541/543, the [[settlement]] Instruction Manager service formats it the same way in the CSV file.         
Correct Incorrect
SWIFT format is 20161203CSV format is 03-Dec-16
 l The CSV file contains two rows.
 o The first row contains column identifiers separated by commas
 o The second row contains corresponding values to those in the first row separated by commas.
In both rows, the [[settlement]] Instruction Manager service does not include space(s) between a field 
value and the preceding or following comma, unless the space(s) is part of the field value.                 
Correct Incorrect
Message Type,Receiver’s Address,Buy Sell IndicatorMessage Type, Receiver's Address, Buy Sell Indicator
 l The file fields follow the X character set. The [[settlement]] Instruction Manager service replaces char-
acters that are not in the X character set (invalid for SWIFT) with a <space>, in accordance with 
MT541/543 message rules.
 l The administrative fields follow the Z character set and [[DO]] not map to SWIFT. Those field values are 
mapped directly from source fields and conform to the Z character set.
CSVFileFormatSpecification
1.CSVFile 7

---

## Page 7

 l The [[settlement]] Instruction Manager service escapes fields containing a comma by embedding the field 
inside double quotes.                 
Correct
data1,”data2A,data2B”,data3
 l The [[settlement]] Instruction Manager service does not escape fields containing slashes (/) or any other 
special characters.
 l The [[settlement]] Instruction Manager service populates optional fields in the CSV file only when they are 
present in the MT541/543 message. If an optional field value is not present, the column header is cre-
ated for the field but the [[settlement]] Instruction Manager service inserts only the comma.
SWIFT Fields, Codes, and Sample Values
The [[settlement]] Instruction Manager service always populates the CSV file fields in the following table with 
the corresponding SWIFT codes.
SWIFT Field Name SWIFT Code(s) Example Value
Currency FXIB, FXIS FXIS/USD
Deal Price PRCT, ACTU ACTU/USD19493,
Place of Trade EXCH, OTCO, VARI OTCO/US
Quantity of Financial Instru-
ment
FAMT, UNIT FAMT/19493,
Current Face Value AMOR AMOR/2000,
[[Buyer]]/[[Seller]] BUYR, SELL SELL/BICXXXXX
Delivering/Receiving Agent DEAG, REAG DEAG/SUBAGENT1/SUBAGENT2/SUBAGENT 
ADDRESS1/SUBAGENT ADDRESS2
Deliverer's/Receiver's Cus-
todian
DECU, RECU DECU/CUST 1/CUST 2
Deliverer's/Receiver's Inter-
mediary
DEI1, REI1 DEI1/BICXXXXX
Place of [[settlement]] PSET PSET/HK
[[Buyer]]/[[Seller]] LEI ALTE ALTE/98450071B09598A06E11
Table 1.1  SWIFT fields, codes, and sample values
CSVFileFormatSpecification
1.CSVFile 8

---

## Page 8

Mapping SWIFT Fields with Multiple or Concatenated Values 
to CSV
This section describes MT541/543 message and corresponding CSV file fields containing multiple 
concatenated values.
Handling Fields with Multiple Values
Some fields in the CSV file can contain multiple values. All possible values for the fields are specified in the 
SWIFT Code column in the .
If any of the fields have multiple values, the [[settlement]] Instruction Manager service populates the values 
in the same CSV file field, separated by slashes (/) and in the same serial order that they appear on the 
SWIFT message. The [[settlement]] Instruction Manager service does not populate the qualifier or the Data 
Source Scheme (DSS) for Trade Transaction Condition Indicator. Slashes separate SWIFT code from 
each value. For example,   Trade Transaction Condition Indicator maps to XCPN/XRTS/XDIV.
Note
For fields that contain a DSS, the [[settlement]] Instruction Manager service always separate the DSS by a slash. Refer 
to www.swift.com for more information about the DSS in SWIFT messaging.
Concatenated Values
The CSV file value for the Place of Safekeeping composite is a concatenation of the optional Place of 
Safekeeping Place, Place of Safekeeping Type, and Place of Safekeeping Value elements separated by 
slashes. The following rules apply:
 l For [[Option]] F: Place of Safekeeping Type=BIC (for example, CUST/BIC/INSTXX34)
 l For [[Option]] C: Place of Safekeeping Type=COUN (for example, COUN/AG)
Narrative Value ([[settlement]] Instruction Processing Narrative)
Due to its potential length, the [[settlement]] Instruction Manager service maps the [[settlement]] Instruction 
Processing Narrative field as follows:
CSVFileFormatSpecification
1.CSVFile 9

---

## Page 9

 l Where this field can have 10 lines, if there are any empty lines sourced from CTM, [[settlement]] Instruc-
tion Manager service ignores any such empty lines. For example, if only Line 1 and Line 3 are present, 
the CSV file will output this field value as: "Line1/Line3"
 l If the field specifies an exact number of lines, then the [[settlement]] Instruction Manager service omits all 
references after the last line. For example, if Line 4 onward is not present: "Line1/Line2/Line3"
The [[settlement]] Instruction Manager service maps all other SWIFT tags and qualifiers sourced from the 
CTM trade data to CSV fields with source trade data only. CSV files [[DO]] not include SWIFT tags and 
slashes.
CSV File Layout
The [[settlement]] Instruction Manager service provides the [[Option]] of constructing a CSV file containing 
[[settlement]] instructions for release to [[Custodians]] and interested parties. The [[settlement]] Instruction 
Manager service releases the CSV notifications using Secure File Transfer Protocol (SFTP) as the 
delivery method.
With a CSV file, the [[settlement]] Instruction Manager service:
 l Constructs and releases [[settlement]] instructions and notifications to [[Custodians]] and interested parties.
 l Provides multiple parties that [[DO]] not have SWIFT connectivity with relevant trade data in CSV format.
Table 1.2 describes the contents of the column headers in the CSV File Specification table:
The dark shaded rows indicate the following:
 l Sequences in the MT541/543.
 l When including an arrow (→), corresponding sub-sequences in the MT541/543.
CSVFileFormatSpecification
1.CSVFile 10

---

## Page 10

Column Header Description
CSV Field Name The information in this column provides the CSV field name in the Header row of a CSV 
file.
SWIFT Tag/Qualifier/Field 
Name/Codes CSV 
Example
The information in this column contains the following, when corresponding SWIFT ele-
ments exist:
 l SWIFT Tag/Qualifier—If applicable, the field corresponds to the same tag and qualifier in a SWIFT MT541/543.
 l SWIFT Field Name—If applicable, the field corresponds to the same field name in a SWIFT MT541/543.
 l SWIFT Codes—If applicable, identifies all static SWIFT code val-ues the [[settlement]] Instruction Manager service supports:
 o Commas separate the codes and SWIFT allows one code per field
 o A superscript number such as 1 indicates that the cor-responding table footnote contains an extensive list of sup-ported code values.
 l CSV Example—An example field value as it appears in the mes-sage row of a CSV file.
AG / TD The information in this column indicates the source that [[settlement]] Instruction Manager 
service uses to derive data for the CSV file:
 l AG—Automatically generated from CTM/ [[settlement]] Instruction Manager service during the trade cycle and [[settlement]] process. Examples are the CTMTradeDetailID and CTMTradeSideId val-ues.
 l TD—TradeDetail that you or your counterparty submit according to the rules described for the field in SWIFT MT541/543 Layout.
CTM Mapping
Source / 
[[settlement]] Instruction 
Manager UI Mapping
The information in this column indicates the following:
 l Source—The name of the element in CTM TradeDetail that   Set-tlement Instruction Manager service uses to derive or map data for the instruction. If the element is not unique in the message, the CTM XPath is included. For example, PartyValue is an ele-ment in the InstructingParty and ExecutingBroker composites in CTM. When used for mapping, the PartyValue XPath is:
 o InstructingParty/PartyValue
 o ExecutingBroker/PartyValue
Mandatory and optional elements within composites conform to SWIFT mandatory 
and optional fields. For example, the Currency composite contains the optional Sign 
element and the mandatory CurrencyCode and Amount elements.
[[settlement]] Instruction Manager UI Mapping—The corresponding field name in the 
[[settlement]] Instruction Manager UI, accessed through the ITP portal.
Note Notes include whether CTM maps the instructing party or executing [[Broker]] value and 
other rules or validations CTM / [[settlement]] Instruction Manager service applies.
Table 1.2  CSV File Specification—Column Header Key
CSVFileFormatSpecification
1.CSVFile 11

---

## Page 11

The following table provides the CSV file specification. It only contains fields applicable to [[settlement]] 
according to CSV requirements.
CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Header Information (Block 1 and Block 2)
Message Type SWIFT Tag/Qualifier: 
HDR 
Field Name: Message 
Type 
CSV Example: 541
TD BuySellIndicator 
---
Buy/Sell
If BuySell=SELL, Message Type=543
 
If BuySell=BUYI, Message Type=541
Receiver’s 
Address
SWIFT Tag/Qualifier: 
HDR 
Field Name: Receiver’s 
Address 
CSV Example: 
10.115.54.13/22//Home/
CTM Training
AG N/A 
---
N/A
Concatenation of Domain Name, Port 
Number, and Destination Directory in the 
eligible Destination Profile.
Buy Sell Indic-
ator
SWIFT Tag/Qualifier: 
HDR 
Field Name: Message 
Type
CSV Example: BUYI
TD BuySellIndicator 
--- 
Buy/Sell 
 
Trade Side [[ID]] CSV Example: 200000 AG CTMTradeSideId 
---
CTM Block [[ID]] 
 
TradeDetail [[ID]] CSV Example: 222222 AG CTMTradeDetailID 
---
CTM Allocation [[ID]]
 
Master 
Reference
CSV Example: 987654 TD MasterReference 
---
Block [[ID]]
 
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 12

---

## Page 12

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Client Allocation 
Reference
CSV Example: 10987653TD ClientAllocationReference 
---
Allocation [[ID]] 
 
Version NumberCSV Example: 1 TD N/A 
---
N/A
Administrative field 
Version Number will always be 1
Notification [[ID]] CSV Example: 888888 AG N/A 
--- 
N/A
Administrative field 
Unique [[ID]] generated by [[settlement]] 
Instruction Manager that can be up to 
16 characters in length
Notification 
Order
CSV Example: 1 AG N/A 
--- 
N/A
Administrative field
Notification Order Number will always 
be 1
→ General Information (Mandatory Sequence A)
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 13

---

## Page 13

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Sender’s 
Reference
SWIFT Tag/Qualifier: 
:20C::SEME 
Field Name: Sender’s 
Message Reference 
CSV Example: 123456
AG or 
TD
CTMTradeDetailID 
---
CTM Allocation [[ID]]
Mapping rules as follows:
 l When Func-
tionOfTheMessage is 
NEWM, CTMTradeDetailID 
is mapped to Sender’s Mes-
sage Reference.
 l When Func-
tionOfTheMessage is CANC, 
or when a manually can-
celled allocation gets 
amended from UI, an iden-
tifier (up to 16 characters in 
length) auto-generated by 
[[settlement]] Instruction Man-
ager is mapped to Sender’s 
Message Reference. In the 
same message, the Previous 
Reference gets mapped with 
Sender’s Reference of ori-
ginal message.
Function of the 
Message
SWIFT Tag/Qualifier: 
:23G: 
Field Name: Function of 
the Message 
SWIFT Codes: NEWM, 
CANC 
CSV Example: NEWM
TD FunctionOfTheMessage 
---
N/A
The 4-char value of 
FunctionOfTheMessage is mapped to 
the Function:
 l NEWM—Directs the cus-
todian to process the set-
tlement instruction.
 l CANC—Directs the cus-
todian to cancel a previous 
[[settlement]] instruction.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 14

---

## Page 14

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Preparation 
Date/Time
SWIFT Tag/Qualifier: 
:98C::PREP 
Field Name: Preparation 
Date/Time 
CSV Example: 
20220705093016
AG N/A 
--- 
N/A
Administrative field. 
CSV creation Date Time (UTC) is 
mapped to preparation Date/Time in 
the format YYYYMMDDHHMMSS. 
Date and Time is based on 
Coordinated Universal Time Zone 
(UTC). 
→ Linkages (Optional Subsequence A1—Qualifier 20C) 
Previous 
Reference
SWIFT Tag/Qualifier: 
:20C::PREV 
Field Name: Previous 
Reference
CSV Example: 123456
TD CTMTradeDetailI 
---
Previous Transaction Ref
Mapping rules as follows:
 l When Func-
tionOfTheMessage is CANC, 
CTMTradeDetailID is 
mapped to Previous Refer-
ence.
 l When Func-
tionOfTheMessage is 
NEWM, Previous Reference 
is not created
Exception to the second rule above 
occurs when a canceled allocation 
(manual cancellation from [[settlement]] 
Instruction Manager UI) gets amended 
from UI, an autogenerated value is 
mapped to Sender’s Reference 
resulting in new SWIFT. In the same 
message, the 20C PREV tag for 
Previous Reference gets created and 
is mapped with the Sender’s Message 
Reference (CTMTradeDetailID) of 
original message.
 
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 15

---

## Page 15

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Related 
Reference
SWIFT Tag/Qualifier: 
:20C::RELA
Field Name: Related 
Reference
CSV Example: 1893
TD TDReferenceType=RELA 
---
Related Transaction Ref
TDReferences/TDReferenceValue is 
mapped to Related Reference(RELA). 
Note that Related Reference is not pop-
ulated when FunctionOfTheMessage is 
CANC.
Pool Related 
Reference
SWIFT Tag/Qualifier: 
:20C::POOL 
Field Name: Pool Related 
Reference 
CSV Example: 8933
TD TDReferenceType=POOL 
---
Pool Ref
TDReferences/TDReferenceValue is 
mapped to Pool Related Reference. 
Note that Pool Related Reference is not 
populated when FunctionOfTheMessage 
is CANC.
Trade Details (Mandatory Sequence B)
Place of Trade SWIFT Tag/Qualifier: 
:94B::TRAD
Field Name: Place of 
Trade
SWIFT Codes: EXCH, 
OTCO, VARI
CSV Example: 
EXCH/XNYS
TD PlaceOfTrade/PlaceCode
PlaceOfTrade/PlaceNarrativ
e 
---
Place of Trade Code
Place of Trade MIC/Place of 
Trade Narrative
[[settlement]] Instruction Manager maps 
PlaceCode and PlaceNarrative into the 
Place of Trade. Note that the Data 
Source Scheme is not used.
[[settlement]] Date SWIFT Tag/Qualifier: 
:98A::SETT 
Field Name: [[settlement]] 
Date 
CSV Example: 20220603
TD SettlementDate 
---
[[settlement]] Date
Mapping format is YYYYMMDD.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 16

---

## Page 16

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Trade Date SWIFT Tag/Qualifier: 
:98A::TRAD 
Field Name: Trade Date 
/Time
CSV Example: 20220602
TD TradeDateTime 
---
Trade Date
Mapped as follows: 
 l If the investment manager/ [[Broker]] 
(orginator of message) is 
subscribed to the Trade Date to 
SWIFT (TTOS) subscription 
[[Option]], then date and time 
(YYYYMMDDHHMMSS) are 
mapped to Trade Date 
 l If the investment manager/ [[Broker]] 
(originator of message) is not 
subscribed to the Trade Date to 
SWIFT (TTOS) subscription 
[[Option]], then date only 
(YYYYMMDD) is mapped to 
Trade Date 
Deal Price SWIFT Tag/Qualifier: 
:90a::DEAL
Field Name: Deal Price
SWIFT Codes: PRCT, 
ACTU
CSV Example: 
ACTU/JPY3925
TD SecurityTypeGroup 
DealPrice/CurrencyCode
DealPrice/Amount 
---
Financial Instrument Class 
Deal Price
Trade Currency
Mapped as follows: 
 l If SecurityTypeGroup=DBT, then 
Deal Price is mapped using the 
PRCT code (Percentage Code). 
 l If SecurityTypeGroup=EQT, then 
Deal Price is mapped using the 
ACTU code (Actual Amount). 
 l Note that the SecurityTypeGroup 
is derived from the investment 
manager's side of the trade.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 17

---

## Page 17

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Number of Days 
Accrued
SWIFT Tag/Qualifier: 
:99A::DAAC
Field Name: Number of 
Days Accrued
CSV Example: 123
TD NumberOfDaysAccrued 
---
Days Accrued
Only positive value is mapped that does 
not include Sign.
Country Code SWIFT Tag/Qualifier: 
:35B
Field Name: Identification 
of the Financial 
Instrument
CSV Example: GB
TD CountryCode 
---
N/A
Only mapped when Num-
beringAgencyCode is not ISIN.
Numbering 
Agency Code
SWIFT Tag/Qualifier: 
:35B
Field Name: Identification 
of the Financial 
Instrument
CSV Example: ISIN
TD NumberingAgencyCode 
---
Financial Instrument [[ID]] Type
 
Security Code SWIFT Tag/Qualifier: 
:35B
Field Name: Identification 
of the Financial 
Instrument
CSV Example: 
JP3245400001
TD SecurityCode 
---
Financial Instrument [[ID]]
 
Description of 
The Security 1
SWIFT Tag/Qualifier: 
:35B
Field Name: Identification 
of the Financial 
Instrument
CSV Example: AEON 
YUSHU
TD DescriptionOfTheSecurity 
---
Financial Instrument 
Description
Maps the first line of Descrip-
tionOfTheSecurity, if present.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 18

---

## Page 18

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Description of 
The Security 2
SWIFT Tag/Qualifier: 
:35B
Field Name: Identification 
of the Financial 
Instrument
CSV Example: IDFI2
TD DescriptionOfTheSecurity 
---
Financial Instrument 
Description
Maps the second line of Descrip-
tionOfTheSecurity, if present.
Description of 
The Security 3
SWIFT Tag/Qualifier: 
:35B
Field Name: Identification 
of the Financial 
Instrument
CSV Example: IDFI3
TD DescriptionOfTheSecurity 
---
Financial Instrument 
Description
Maps the third line of Descrip-
tionOfTheSecurity, if present.
Description of 
The Security 4
SWIFT Tag/Qualifier: 
:35B
Field Name: Identification 
of the Financial 
Instrument
CSV Example: IDFI4
TD DescriptionOfTheSecurity 
---
Financial Instrument 
Description
Maps the fourth line of Descrip-
tionOfTheSecurity, if present.
→ Financial Instrument/Account (Optional Subsequence B1)
    Note: Only populated when PSET is NOT Germany and SecurityTypeGroup=DBT.
Current Factor  SWIFT Tag/Qualifier: 
:92A::CUFC 
Field Name: Current 
Factor 
CSV Example: "1,559" 
TD CurrentFactor/Sign
CurrentFactor/Amount 
---
Current Factor
Negative sign is mapped/indicated by an 
N at the start of the value.
Pool Number SWIFT Tag/Qualifier: 
:13B::POOL 
Field Name: Pool Number
 
CSV Example: 4 
TD PoolNumber 
---
Pool Number
 
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 19

---

## Page 19

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Maturity Date SWIFT Tag/Qualifier: 
:98A::MATU
Field Name: Maturity 
Date 
CSV Example: 20250511
TD MaturityDate 
---
Maturity Date
Mapping format is YYYYMMDD.
Coupon Rate SWIFT Tag/Qualifier: 
:92A::INTR
Field Name: Coupon 
Rate
CSV Example: "5,4"
TD CouponRate/Sign
CouponRate/Amount 
---
Coupon Rate
Negative sign is mapped/indicated by an 
N at the start of the value.
Trade 
Transaction 
Condition 
Indicator
SWIFT Tag/Qualifier: 
:22F::TTCO
Field Name: Trade 
Transaction Condition 
Indicator
SWIFT Codes: 1
CSV Example: 
CDIV/BCFD
TD TradeTransactionConditionIn
dicator 
---
Trade Conditions
Each occurrence of TradeTrans-
actionConditionIndicator is mapped and 
separated by slash.
Currency SWIFT Tag/Qualifier: 
:11A::FXIB/FXIS
Field Name: Currency to 
Buy/Sell
SWIFT Codes: FXIB or 
FXIS
CSV Example: FXIS/CNY
TD BuySellIndicator and 
FXDealCurrencyCode 
---
FX Deal Currency
Mapped as follows: 
 l If BuySell=SELL, FXIS qual-
ifier is mapped.
 l If BuySell=BUYI, FXIB qual-
ifier is mapped
FXDealCurrencyCode is mapped to 
instruct the recipient of [[settlement]] 
instruction to execute an FX deal.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 20

---

## Page 20

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
TD Match StatusSWIFT Tag/Qualifier: 
:25D::MTCH or 
:25D::AFFM
Field Name: Match Status
SWIFT Codes: MACH or 
NMAT or AFFI or NAFI
CSV Example: MACH
AG TDMatchStatus 
---
Allocation Status
Mapped as follows (mapped only when 
FunctionOfTheMessage=NEWM, not 
mapped for Allocation Type = DEPD 
(Omnibus Dependent Allocations), not 
mapped when 
FunctionOfTheMessage=CANC):
 1. For Pre-Match Agreed, if the 
investment manager is sub-
scribed to the Target to 
[[securities]] Depository sub-
scription [[Option]] (T2SD=Y)) 
and the PSET (Centralized 
[[securities]] Depository) of 
trade allocation is sub-
scribed to the Target to 
[[securities]] Identification sub-
scription [[Option]] (T2SI=Y), 
then the AFFM qualifier and 
NAFI code are used for map-
ping. Otherwise, the MTCH 
qualifier and NMAT code 
are used for mapping a Not 
Match Agreed allocation.
 2. For Match Agreed, if the 
investment manager/ 
executing [[Broker]] (originator 
of message) is subscribed 
to the Target to [[securities]] 
Depository subscription 
[[Option]] (T2SD=Y)) and the 
[[Broker]]'s PSET (Centralized 
[[securities]] Depository) of 
trade allocation is sub-
scribed to the Target to 
[[securities]] Identification sub-
scription [[Option]] (T2SI=Y), 
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 21

---

## Page 21

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
then the AFFM qualifier and 
AFFI code are used for map-
ping. Otherwise, the MTCH 
qualifier and MACH code 
are used for mapping a 
Match Agreed allocation. 
[[settlement]] 
Instruction 
Processing 
Narrative
SWIFT Tag/Qualifier: 
:70E::SPRO
Field Name: [[settlement]] 
Instruction Processing 
Narrative
CSV Example: 
Counterparty covers 
registration cost.
TD AdditionalText
TDReferenceType (where 
TDReferenceType=XCBT), 
and TDReferenceValue 
---
[[settlement]] Narrative 1, 
[[settlement]] Narrative 2, ... up 
to and including ... [[settlement]] 
Narrative 10, and Cpty Cash 
Bond Trading Ref
This field is mapped to supply 
additional information to an instruction 
and supports max of 10 lines (35 char 
each). See Narrative Value mapping. 
If AdditionalText is not present and the 
counterparty [[Broker]] has a 
TDReferenceType of XCBT, then the 
TDReferenceValue is appended to the 
proprietary code CBT. 
Example: If TDReferenceType=XCBT 
and TDReferenceValue=123, then the 
value mapped to this field will be 
CBT123.
Financial Instrument/Account (Mandatory Sequence C)
Quantity of 
Financial 
Instrument
SWIFT Tag/Qualifier: 
:36B::SETT
Field Name: Quantity of 
Financial Instrument
SWIFT Codes: FAMT or 
UNIT
CSV Example: 
"UNIT/200,"
TD QuantityTypeCode and 
QuantityAllocated 
---
Quantity Type and Quantity
Both QuantityTypeCode and Quant-
ityAllocated are mapped. Quant-
ityTypeCode can either be FAMT or 
UNIT.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 22

---

## Page 22

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Current Face 
Value
SWIFT Tag/Qualifier: 
:36B::SETT
Field Name: Quantity of 
Financial Instrument
SWIFT Code: AMOR
CSV Example: 
"AMOR/3344,"
TD CurrentFaceValue 
---
Current Face Value
CurrentFaceValue is mapped to Quantity 
of Financial Instrument if another 
instance of tag 36B SETT contains 
FAMT as Quantity Type Code. Quantity 
Type Code AMOR is mapped when the 
CurrentFaceValue is mapped.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 23

---

## Page 23

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Security 
Account SWIFT Tag/Qualifier: 
:97A::SAFE 
Field Name: Account 
(Safekeeping Account) 
CSV Example: 3434- 
343434 
TD SecurityAccount or ID2 
---
Account at Settling Agent
Sourced as follows:                 
 l If counterparty's PSET is 
IBRCESMM, 
IBRCESMMSCL, 
IBRCESMMCDE, 
IBRCESMMMVL, or 
IBRCESMMXXX, then: 
 o SecurityAccount value 
is mapped, if available.
 o If SecurityAccount is 
not available, ID2 is 
used for mapping to 
Safekeeping Account.
 o  If both Secur-
ityAccount and ID2 are 
not available, a Fatal 
error is generated.
 l If counterparty's PSET is not 
one of the following - 
IBRCESMM, 
IBRCESMMSCL, 
IBRCESMMCDE, 
IBRCESMMMVL, or 
IBRCESMMXXX, then:                       
 o SecurityAccount value 
is mapped if available.
 o If SecurityAccount is 
not available, a Fatal 
error is generated
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 24

---

## Page 24

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Cash Account SWIFT Tag/Qualifier: 
:97A::CASH/97E::CASH
Field Name: Account 
(Cash Account)
CSV Example: 5000-
6000-700
TD CashAccountNo 
---
Cash Account
[[settlement]] Instruction Manager maps 
the cash account number, including 
the [[Option]] to use an International Bank 
Account Number (IBAN), for the 
settling allocation. (For mapping 
options, see SWIFT tag 97a CASH 
Line No. 43).
A CashAccountNo value with first two 
characters as a country code is 
assumed to be an International Bank 
Account Number.
Place of 
Safekeeping
SWIFT Tag/Qualifier: 
:94a::SAFE
Field Name: Place (Place 
of Safekeeping)
CSV Example: 
 l US
 l NSCD/DTCYUS33
XXX
TD PlaceOfSafekeepingType, 
PlaceofSafekeepingPlace, 
PlaceofSafekeepingValue 
---
PSAFE Type 
PSAFE BIC 
PSAFE Country
PSAFE Place
Sourced as follows:
 l If 
PlaceOfSafekeepingType=COUN, 
then 2 char Country Code is used 
to map the 
PlaceofSafekeepingValue
 l If PlaceOfSafekeepingType=BIC, 
then 8 or 11 char BIC is used to 
map the 
PlaceofSafekeepingValue, along 
with the PlaceofSafekeepingPlace 
value.
Note that only valid BICs are mapped 
to Place of Safekeeping:
 l If BIC is 11 char, it is mapped as-is
 l If BIC is 8 char, it is padded with 
XXX and then mapped.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 25

---

## Page 25

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Repetitive [[settlement]] Details (Mandatory Sequence E)
[[settlement]] 
Transaction 
Condition 
Indicator
SWIFT Tag/Qualifier: 
:22F::STCO
Field Name: Indicator 
([[settlement]] Transaction 
Condition Indicator)
SWIFT Codes: 2
CSV Example: CLEN
TD SettlementTransactionConditi
on Indicator 
---
[[settlement]] Conditions
Each occurrence of 
SettlementTransactionConditionIndica
tor is mapped and separated by slash.
If the 22F STCO SWIFT code is PHYS, 
the SWIFT tag :95C::PSET must use 
[[Option]] C. Otherwise, a Fatal error is 
generated.
Type of 
[[settlement]] 
Transaction 
Indicator
SWIFT Tag/Qualifier: 
:22F::SETR
Field Name: Indicator 
(Type of [[settlement]] 
Transaction Indicator) 
SWIFT Codes: 3
CSV Example: TRAD
TD TypeOfTransactionIndicator 
---
Type of [[settlement]] 
Transaction
If there is Data Source Scheme, it will be 
mapped.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 26

---

## Page 26

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Stamp Duty 
Indicator
SWIFT Tag/Qualifier: 
:22F::STAM
Field Name: Indicator 
(Stamp Duty Indicator)
SWIFT Codes: 4
CSV Example: 
CRST/GBT
TD SettlementTransactionConditi
onIndicator 
---
Stamp Duty Exemption
If there is Data Source Scheme, it will 
be mapped.
Sourced as follows:
 l If the value of Set-
tle-
mentTrans-
actionConditionIndicator is 
from the list of values that 
map to Stamp Duty Indicator, 
it is mapped to 22F STAM. 
See the SWIFT codes that 
map to 22F STAM.
 l For code USTN, STRA is 
used as the Data Source 
Scheme.
 l If counterparty's PSET-
T=XHKCHKH1 or 
XHKCHKH1XXX, CCAS is 
used as the Data Source 
Scheme when codes are 
FUSD or HASD.
 l If counterparty's 
PSET≠XHKCHKH1 or 
XHKCHKH1XXX, then the 
Data Source Scheme is not 
used for codes FUSD and 
HASD.
 l If codes start with GB (such 
as GBAX, GBBX, and so on), 
then CRST is used as the 
Data Source Scheme.
 l If codes start with IE (such as 
IEYX, IEQX, and so on), then 
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 27

---

## Page 27

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
ECLR is used as the Data 
Source Scheme.
Note that if there is more than one 
value in 
SettlementTransactionConditionIndica
tor that could be mapped to 22F 
STAM, only the first value is mapped.
Registration 
Override 
Indicator
SWIFT Tag/Qualifier: 
:22F::REGT
Field Name: Indicator 
(Registration Indicator) 
SWIFT Codes: NREG or 
YREG
CSV Example: NREG
TD SettlementTransactionConditi
on Indicator 
---
Registration
Mapped if the value of 
SettlementTransactionConditionIndica
tor=NREG or YREG.   
Note that if both NREG and YREG are 
present in 
SettlementTransactionConditionIndica
tor, only the first value is mapped. 
Beneficial 
Ownership 
Override 
Indicator
SWIFT Tag/Qualifier: 
:22F::BENE
Field Name: Indicator 
(Beneficial Ownership 
Indicator)
SWIFT Codes: NBEN or 
YBEN
CSV Example: NBEN
TD SettlementTransactionConditi
onIndicator 
---
Beneficial Ownership
Mapped if the value of 
SettlementTransactionConditionIndica
tor=NBEN or YBEN. 
Note that if both NBEN and YBEN are 
present in 
SettlementTransactionConditionIndica
tor, only the first value is mapped. 
Cash [[settlement]] 
System 
Override 
Indicator
SWIFT Tag/Qualifier: 
:22F::CASY
Field Name: Indicator 
(Cash [[settlement]] System 
Indicator)
SWIFT Codes: GROS or 
NETS
CSV Example: NETS
TD SettlementTransactionConditi
onIndicator 
---
Cash [[settlement]] System
Mapped if the value of 
SettlementTransactionConditionIndica
tor=GROS or NETS.   
Note that if both GROS and NETS are 
present in 
SettlementTransactionConditionIndica
tor, only the first value is mapped. 
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 28

---

## Page 28

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Forex Order 
Cancellation 
Indicator
SWIFT Tag/Qualifier: 
:22F::FXCX
Field Name: Indicator 
(Forex Order Cancellation 
Indicator)
SWIFT Codes: FXYE or 
FXNO
CSV Example: FXNO
TD N/A 
---
N/A
When FunctionOfTheMessage is 
CANC and if the original NEWM 
message had tag 11A populated.
 l If user elects to keep FX in place 
(Cancel FX Flag is N) in the 
[[settlement]] Instruction Manager UI, 
then the FXNO indicator is 
populated.
 l If user via the [[settlement]] 
Instruction Manager UI elects to 
cancel FX in place (Cancel FX 
Flag is Y), then FXYE indicator is 
populated.
Also, if the Match Agreed Trade is 
canceled via CTM and the original 
instruction contained tag 11A, then the 
FXYE indicator is populated.
When FunctionOfTheMessage is 
NEWM, SINO indicator will be mapped 
to this field provided it is selected by 
the user via [[settlement]] Instruction 
Manager UI.
Netting Eligibility 
Indicator
SWIFT Tag/Qualifier: 
:22F::NETT
Field Name: Indicator 
(Netting Eligibility 
Indicator) 
SWIFT Codes: NNET or 
YNET
CSV Example: YNET
TD SettlementTransactionConditi
onIndicator 
---
Netting Eligibility
Mapped if the value of 
SettlementTransactionConditionIndica
tor=NNET or YNET. 
Note that if both NNET and YNET are 
present in 
SettlementTransactionConditionIndica
tor, only the first value is mapped. 
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 29

---

## Page 29

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Central Counter 
Party Eligibility 
Indicator
SWIFT Tag/Qualifier: 
:22F::CCPT
Field Name: Indicator 
(Central Counterparty 
Eligibility Indicator)
SWIFT Codes: NCCP or 
YCCP
CSV Example: NCCP
TD SettlementTransactionConditi
onIndicator 
---
Central Counterparty Eligibility
Mapped if the value of 
SettlementTransactionConditionIndica
tor=NCCP or YCCP.   
Note that if both NCCP and YCCP are 
present in 
SettlementTransactionConditionIndica
tor, only the first value is mapped. 
Letter of 
Guarantee 
Indicator
SWIFT Tag/Qualifier: 
:22F::LEOG
Field Name: Indicator 
(Letter of Guarantee 
Indicator) 
SWIFT Codes: NLEG or 
YLEG
CSV Example: NLEG
TD SettlementTransactionConditi
onIndicator 
---
Letter of Guarantee
Mapped if the value of 
SettlementTransactionConditionIndica
tor=NLEG or YLEG.   
Note that if both NLEG and YLEG are 
present in 
SettlementTransactionConditionIndica
tor, only the first value is mapped. 
[[settlement]] 
System Method 
Indicator
SWIFT Tag/Qualifier: 
:22F::SETS
Field Name: Indicator 
([[settlement]] 
System/Method Indicator
SWIFT Codes: NSET or 
YSET
CSV Example: YSET
TD SettlementTransactionConditi
onIndicator 
---
[[settlement]] System/Method
Mapped if the value of 
SettlementTransactionConditionIndica
tor=NSET or YSET. 
Note that if both NSET and YSET are 
present in 
SettlementTransactionConditionIndica
tor, only the first value is mapped. 
Real-Time 
Gross 
[[settlement]] 
System 
Indicator
SWIFT Tag/Qualifier: 
:22F::RTGS
Field Name: Indicator 
([[securities]] Real-Time 
Gross [[settlement]] 
Indicator)
SWIFT Codes: NRTG or 
YRTG
CSV Example: NRTG
TD SettlementTransactionConditi
onIndicator 
---
Real-Time Gross [[settlement]] 
System
Mapped if the value of 
SettlementTransactionConditionIndica
tor=NRTG or YRTG. 
Note that if both NRTG and YRTG are 
present in 
SettlementTransactionConditionIndica
tor, only the first value is mapped. 
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 30

---

## Page 30

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Restrictions 
Indicator
SWIFT Tag/Qualifier: 
:22F::REST 
Field Name: Indicator 
(Restrictions Indicator) 
SWIFT Codes: NRST, 
RSTR, or 144A
CSV Example: NRST
TD SettlementTransactionConditi
onIndicator 
---
Restrictions
Mapped if the value of 
SettlementTransactionConditionIndica
tor=NRST, RSTR or 144A. 
Note that if multiple codes are present 
in 
SettlementTransactionConditionIndica
tor (from above), only the first value is 
mapped. 
Block Trade 
Indicator
SWIFT Tag/Qualifier: 
:22F::BLOC
Field Name: Indicator 
(Block Trade Indicator) 
SWIFT Codes: BLCH or 
BLPA
CSV Example: BLPA
TD SettlementTransactionConditi
onIndicator 
---
Block Trade Indicator
Mapped if the value of 
SettlementTransactionConditionIndica
tor= BLPA or BLCH. 
Note that if both BLPA and BLCH are 
present in 
SettlementTransactionConditionIndica
tor, only the first value is mapped. 
→ [[settlement]] Parties (Mandatory Repetitive Subsequence E1)
Note: [[settlement]] Instruction Manager only maps the parties in the TradeDetail. For example, if there is not a SubAgent 
for the trade, [[settlement]] Instruction Manager omits the Delivering/Receiving Agent and corresponding Safekeeping 
Account fields.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 31

---

## Page 31

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
[[Buyer]]/[[Seller]] SWIFT Tag/Qualifier: 
:95a::BUYR or SELL 
Field Name: Party
CSV Example: 
BUYR/ABCJPYABXXX
TD ISRTDExecutingBroker or 
ISRTDInstructingParty/ID2, 
TLEBSettlement/ID2, 
ExecutingBroker or 
InstructingParty*/[[settlement]] 
Instructions/INSTor BrokerID, 
ExecutingBroker or 
InstructingParty*/[[settlement]] 
Instructions/ID3, 
ExecutingBroker or 
InstructingParty*/[[settlement]] 
Instructions/InstitutionBIC, 
ExecutingBroker or 
InstructingParty*/PartyValue 
(CTM BIC value), and 
ExecutingBroker or 
InstructingParty*/OrgName 
---
Cpty Local Code (ID2), Cpty 
ID3, Cpty BIC, and Cpty Name
 
*Sourced from 
Counterparty’s side
If there is Data Source Scheme, it will 
be mapped. Sourced from one of the 
following, in order:
 1. If the counterparty’s PSET 
is IBRCESMMXXX, then 5 
and ID2 is available and con-
tains a 9 or 11 char value, 
ID2 is mapped. IBRC is 
used as the Data Source 
Scheme for mapping.
If ID2 is not a 9-char (COD) value 
or a 11- char (NIF) value, or if it is 
not present, then rule #3 triggers.
 2. If the counterparty’s PSET 
is FRNYUS33XXX (US FED 
Wire) or DTCYUS33XXX 
([[DTC]]) and:
 l If INSTorBrokerID is 
present, that is 
mapped. DTCYID is 
used as Data Source 
Scheme.
 l If INSTorBrokerID is not 
present, ID3 is mapped. 
DTCYID is used as 
Data Source Scheme.
 l If both INSTorBrokerID 
and ID3 are not 
present, rule #3 trig-
gers.If PSET is not 
equal to ones from #1 
and # 2 above, logic 
starts from #3 below.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 32

---

## Page 32

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
 3. InstitutionBIC is mapped, if 
available. If the Insti-
tutionBIC is not a valid BIC 
or if it is not available, rule 
#4 triggers.
 4. ExecutingBroker or Instruct-
ingParty (Coun-
terparty’s)/PartyValue (CTM 
BIC Value) is mapped. If this 
BIC is not valid or if it is not 
available, then rule #5 trig-
gers.
 5. ExecutingBroker or Instruct-
ingParty (Coun-
terparty’s)/OrgName is 
mapped. If OrgName is not 
present and 95a 
BUYR/SELL tag cannot be 
created with any other rules, 
a Fatal error is generated.
Also note:
 l If BuySell=SELL, then 95a 
BUYR qualifier is used.
 l If BuySell=BUYI, then 95a 
SELL qualifier is used.
 l If the BIC is 11 characters 
long, it is mapped as-is.
 l If the BIC is 8 characters 
long, it is padded with XXX, 
and then mapped.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 33

---

## Page 33

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
[[Buyer]]/[[Seller]] 
Safekeeping 
Account
SWIFT Tag/Qualifier: 
:97A::SAFE   Field Name: 
Safekeeping Account 
CSV Example: 67891-
0123-4567 
TD SecurityAccount or ID2 
(sourced from 
counterparty's SSI) 
---
Cpty A/C # at Global 
Custodian or Cpty Local 
Code (ID2)
Sourced from one of the following, in 
order:
 1. If the counterparty’s PSET 
is IBRCESMM, 
IBRCESMMSCL, 
IBRCESMMCDE, 
IBRCESMMMVL, or 
IBRCESMMXXX and:If the 
counterparty’s PSET is 
IBRCESMM, 
IBRCESMMSCL, 
IBRCESMMCDE, 
IBRCESMMMVL, or 
IBRCESMMXXX and:
 l If SecurityAccount is 
available, that value is 
mapped
 l If SecurityAccount is 
not available, ID2 is 
mapped
 l If both SecurityAccount 
and ID2 are not avail-
able, there will no value 
mapped (97A SAFE tag 
is not created).
 2. If counterparty’s PSET is 
not one of the following: 
IBRCESMM, 
IBRCESMMSCL, 
IBRCESMMCDE, 
IBRCESMMMVL, 
IBRCESMMXXX:
 l If the SecurityAccount 
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 34

---

## Page 34

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
is available, then it is 
mapped.
 l If the SecurityAccount 
is not available, there 
will no value mapped 
(97A SAFE tag is not 
created).
Deliverer’s/ 
Receiver’s 
Custodian
SWIFT Tag/Qualifier: 
:95a::DECU or RECU
Field Name: Party
CSV Example: 
DECU/HIJABCABCXX
TD CustodianBIC, 
CustodianName1, and 
CustodianName2 (sourced 
from counterparty's SSI) 
---
Cpty Custodian BIC, Cpty 
Custodian Name 1, and Cpty 
Custodian Name 2
Sourced as follows, in order:
 1. If CustodianBIC is present 
and valid, then it is mapped.
 2. If CustodianBIC is not 
present or invalid, Cus-
todianName1 and/or Cus-
todianName2 fields are 
mapped.
If conditions from #1 and #2 are not 
met, no value is mapped (95a 
DECU/RECU tag is not created). Note 
the following:
 l If BuySell=SELL, 95a RECU 
is used.
 l If BuySell=BUYI, 95a DECU 
is used.
 l If BIC is 11 characters long, it 
is mapped as-is.
 l If BIC is 8 characters long, it 
is padded with ‘XXX’ and 
then mapped.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 35

---

## Page 35

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Deliverer’s/ 
Receiver’s 
Custodian's 
Safekeeping 
Account
SWIFT Tag/Qualifier: 
:97A::SAFE 
Field Name: Safekeeping 
Account
CSV Example: 67891-
0123-4567
TD SubAccountNo (sourced from 
counterparty's SSI) 
---
Cpty A/C# at Local Agent
If SubAccountNo is present, it is 
mapped; if not, no value is mapped (97A 
SAFE is not created).
Delivering/ 
Receiving Agent
SWIFT Tag/Qualifier: 
:95a::DEAG or REAG
Field Name: Party
CSV Example:   
DEAG/ABCABCABCXX
TD SubAgentBIC, ID1, 
SubAgentName1, 
SubAgentAddress1, 
SubAgentName2, and 
SubAgentAddress2 (sourced 
from counterparty's SSI) 
---
Cpty SubagentBIC and Cpty 
A/C # at Depository (ID1)
See DEAG/REAG Mapping. 
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 36

---

## Page 36

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Delivering/ 
Receiving 
Agent’s 
Safekeeping 
Account
SWIFT Tag/Qualifier: 
:97A::SAFE 
Field Name: Safekeeping 
Account
CSV Example: 2345-
6789-1234
TD ID1 or ID2 (sourced from 
counterparty's SSI) 
---
Cpty A/C # at Depository (ID1) 
or Local Code (ID2)
Sourced as follows:
 l If PSET= FRNYUS33XXX 
and ID1 was used to pop-
ulate 95a:DEAG/REAG, 97A 
SAFE is mapped with ID2.
 l If ID2 is not present, Fatal 
error is generated.
 l If PSET ≠ FRNYUS33XXX 
normal logic shown below is 
followed: 
 o If SubAgentBIC or one 
or more of the following 
Name/Ad-dress fields 
(SubA-gentName1, 
SubAgentName2, 
SubA-gentAddress1, 
SubA-gentAddress2) 
was used to populate 
95a:DEAG/REAG, 
then, 97A SAFE is 
mapped with ID1.
 o If ID1 is not present, no 
value is mapped. (97A 
SAFE is not created)
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 37

---

## Page 37

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Deliverer's/Rec-
eiver's Inter-
mediary
SWIFT Tag/Qualifier: 
:95a::DEI1 or REI1 
Field Name: Party 
CSV Example: 
DEI1/ABCABCABCXX 
TD Relationship, CorrespBIC, 
CorrespName1, and 
CorrespName2 (sourced 
from counterparty's SSI) 
---
Cpty Corr Relationship and 
Cpty Corr Security Party
When Relationship=S:
 l If CorrespBIC is present and 
valid, then it is mapped.
 l If CorrespBIC is not present 
or invalid, CorrespName1 
and/or CorrespName2 fields 
are mapped.
 l If conditions from #1 and #2 
are not met, no value is 
mapped (95a DEI1/REI1 tag 
is not created).
Note:
 l If BuySell=SELL, 95a REI1 is 
used.
 l If BuySell=BUYI, 95a DEI1 is 
used.
 l If BIC is 11 characters long, it 
is mapped as-is.
 l If BIC is 8 characters long, it 
is padded with XXX and then 
mapped.
 l If 95a DECU/RECU is not cre-
ated but data needed to cre-
ate 95a DEI1/REI1 is 
present, 95a DECU/RECU is 
created using the data that 
would normally create 95a 
DEI1/REI1.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 38

---

## Page 38

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Deliverer's/Rec-
eiver's Inter-
mediary's 
Safekeeping 
Account
SWIFT Tag/Qualifier: 
:97A::SAFE 
Field Name: 
Safekeeping Account 
CSV Example: 2345-
6789-1234 
TD Relationship and 
CorrespSecAccountNo 
(sourced from 
counterparty's SSI) 
---
Cpty Corr Relationship and 
Cpty Corr Security Account
When Relationship = S:
 l If CorrespSecAccountNo is 
present, then it is mapped.
 l If CorrespSecAccountNo is 
not present, no value is 
mapped (97A SAFE is not 
created).
Note:
 l If 95a DECU/RECU is not cre-
ated but data needed to cre-
ate 95a DEI1/REI1 is 
present, 95a DECU/RECU is 
created using the data that 
would normally create 95a 
DEI1/REI1. 
 l If this happens, 97A SAFE 
(that would normally be 
beneath the 95a DEI1/REI1 
tag) gets mapped to same 
instance as 95a 
DECU/RECU.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 39

---

## Page 39

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Place of Set-
tlement SWIFT Tag/Qualifier: 
:95a::PSET 
Field Name: Party 
CSV Example: 
PSET/ABCABCABXXX
 
TD PSET (sourced from 
counterparty's SSI) 
---
[[settlement]] Location Type 
[[settlement]] Location BIC 
[[settlement]] Location Country
 
Mapped as follows:
 l Value of PSET can be a 2-
char valid country code OR 
an 8 or 11 char BIC
 l If PSET is not present or if it 
is invalid, a Fatal error gets 
generated.
Note the following:
 l If BIC is 11 characters long, it 
is mapped ‘as is’
 l If BIC is 8 characters long, it 
is padded with ‘XXX’ and 
then mapped.
→ Repetitive Cash Parties (Optional Subsequence E2)
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 40

---

## Page 40

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Account with 
Institution
SWIFT Tag/Qualifier: 
:95a::ACCW
Field Name: Party 
(Account with Institution) 
CSV Example: 
ABCABCABXXX
TD Relationship, CorrespBIC, 
CorrespName1, and 
CorrespName2 (sourced from 
counterparty's SSI) 
---
Cpty Corr Relationship and 
Cpty Corr Cash Party
When Relationship=C, mapped as fol-
lows:
 l If CorrespBIC is present and 
valid, then it is mapped.
 l If CorrespBIC is not present 
or invalid, CorrespName1 
and/or CorrespName2 fields 
are mapped.
 l If conditions from #1 and #2 
are not met, no value is 
mapped (95a ACCW tag is 
not created).
Notes:
 l If BIC is 11 characters long, it 
is mapped ‘as is’.
 l If BIC is 8 characters long, it 
is padded with ‘XXX’ and 
then mapped.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 41

---

## Page 41

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Cash Account SWIFT Tag/Qualifier: 
:97a::CASH 
Field Name: Cash 
Account
CSV Example: 1111-
2222-3333-4444
TD CorrespCashAccountNo 
(sourced from counterparty's 
SSI) 
---
Cpty Corr Cash Account
Used only when Relationship = C (Cor-
respondent). [[settlement]] Instruction Man-
ager maps the Correspondent Cash 
Account Number, including the [[Option]] to 
use an International Bank Account Num-
ber (IBAN), for the settling allocation. 
(For mapping options, see SWIFT tag 
97a CASH Line No. 73):
 l The first two characters of 
field CorrespCashAccountNo 
can be a valid country code, 
and if so, it is assumed to be 
an International Bank 
Account Number.
 l If CorrespCashAccountNo is 
not present, no value is 
mapped (97a SAFE is not cre-
ated).
→ Repetitive Amounts (Mandatory Subsequence E3)
Accrued Interest 
Amount
SWIFT Tag/Qualifier: 
:19A::ACRU 
Field Name: Accrued 
Interest Amount 
CSV Example: “USD500,”
TD AccruedInterestAmount/ Sign, 
CurrencyCode, and Amount 
---
Trade Currency and Accrued 
Interest
Negative sign is mapped/indicated by an 
N at the start of the value
Charges or FeesSWIFT Tag/Qualifier: 
:19A::CHAR 
Field Name: Charges or 
Fees 
CSV Example: 
“GBR40000,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where ChargeTaxType= 
CHAR) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=CHARGES_ FEES)
Negative sign is mapped/indicated by an 
N at the start of the value
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 42

---

## Page 42

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Country 
National Federal 
Tax
SWIFT Tag/Qualifier: 
:19A::COUN
Field Name: Country, 
National Federal Tax 
CSV Example: “JPY100,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=COUN) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=COUNTRY_ 
NATIONAL_FEDERAL_TAX)
Negative sign is mapped/indicated by an 
N at the start of the value
Trade Amount SWIFT Tag/Qualifier: 
:19A::DEAL 
Field Name: Trade 
Amount
CSV Example: “EUR100,”
TD TradeAmount/Sign, 
CurrencyCode, and Amount 
---
Trade Currency and Trade 
Amount
Negative sign is mapped/indicated by an 
N at the start of the value
Executing 
[[Broker]]’s Amount
SWIFT Tag/Qualifier: 
:19A::EXEC
Field Name: Executing’s 
[[Broker]] Amount 
CSV
Example: “USD1007,”
TD Commission/Sign, 
CurrencyCode, and Amount 
(where 
CommissionType=EXEC) 
---
Trade Currency and 
Commission Amount (where 
Type=EXECUTING_ 
BROKER_COMMISSION)
Negative sign is mapped/indicated by an 
N at the start of the value
Payment Levy 
Tax
SWIFT Tag/Qualifier: 
:19A::LEVY
Field Name: Payment 
Levy Tax
CSV Example: “USD41,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=LEVY) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=PAYMENT_LEVY _
TAX)
Negative sign is mapped/indicated by an 
N at the start of the value
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 43

---

## Page 43

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Local Tax SWIFT Tag/Qualifier: 
:19A::LOCL 
Field Name: Local Tax
CSV Example: “ARS23,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=LOCL) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=LOCAL_TAX)
Negative sign is mapped/indicated by an 
N at the start of the value
Local [[Broker]]’s 
Commission
SWIFT Tag/Qualifier: 
:19A::LOCO
Field Name: Local 
[[Broker]]’s Commission 
CSV Example: “USD15,”
TD Commission/Sign, 
CurrencyCode, and Amount 
(where CommissionType 
=LOCO) 
---
Trade Currency and 
Commission Amount (where 
Type=LOCAL_ BROKER_
COMMISSION)
Negative sign is mapped/indicated by an 
N at the start of the value
Other Amount SWIFT Tag/Qualifier: 
:19A::OTHR 
Field Name: Other 
Amount
CSV Example: “DKK10,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=OTHR) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=OTHER_ AMOUNT)
Negative sign is mapped/indicated by an 
N at the start of the value
Regulatory 
Amount
SWIFT Tag/Qualifier: 
:19A::REGF 
Field Name: Regulatory 
Amount 
CSV Example: “GBR12,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=REGF) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=REGULATORY_ 
AMOUNT)
Negative sign is mapped/indicated by an 
N at the start of the value
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 44

---

## Page 44

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
[[settlement]] 
Amount
SWIFT Tag/Qualifier: 
:19A::SETT 
Field Name: [[settlement]] 
Amount 
CSV Example: “JPY15,”
TD SettlementAmount/Sign, 
CurrencyCode, and Amount, 
and NetCashAmount/Sign, 
CurrencyCode, and Amount 
---
[[settlement]] Amount and 
[[settlement]] Currency
If [[settlement]] Instruction Manager 
determines that the trade meets the 
criteria of a cross currency trade, then
- Mapping is performed from the 
SettlementAmount provided by the 
investment manager; else
- for non cross currency trades.
If the SettlementAmount from the 
Executing [[Broker]] was provided, it is 
mapped to 19A SETT ; otherwise, 19A 
SETT is mapped with 
NetCashAmount.
Negative sign is mapped/indicated by 
an N at the start of the value
Shipping 
Amount
SWIFT Tag/Qualifier: 
:19A::SHIP
Field Name: Shipping 
Amount 
CSV Example: “EUR67,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=SHIP) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=SHIPPING_ FEES)
Negative sign is mapped/indicated by an 
N at the start of the value
Special 
Concessions 
Amount
SWIFT Tag/Qualifier: 
:19A::SPCN
Field Name: Special 
Concessions Amount 
CSV Example: “EUR6,”
TD Commission/Sign, 
CurrencyCode, and Amount 
(where 
CommissionType=SPCN) 
---
Trade Currency and 
Commission Amount (where 
Type = SPECIAL_
CONCESSION )
Negative sign is mapped/indicated by an 
N at the start of the value
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 45

---

## Page 45

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Stamp Duty SWIFT Tag/Qualifier: 
:19A::STAM 
Field Name: Stamp Duty
CSV Example: “EUR9,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=STAM) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=STAMP_DUTY)
Note the following:
 l If 22F Stamp Duty Indicator is 
mapped with Data Source Scheme 
of CRST (such as 
STAM/CRST/value), then TRAX is 
mapped to 19A::STAM.
 l Negative sign is 
mapped/indicated by an N at the 
start of the value
[[Stock]] Exchange 
Tax
SWIFT Tag/Qualifier: 
:19A::STEX 
Field Name: [[Stock]] 
Exchange Tax 
CSV Example: “EUR30,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=STEX) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=STOCK_ EXCHANGE_
TAX)
Negative sign is mapped/indicated by an 
N at the start of the value
Transfer Tax SWIFT Tag/Qualifier: 
:19A::TRAN 
Field Name: Transfer Tax
CSV Example: “EUR34,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=TRAN) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=TRANSFER_TAX)
Negative sign is mapped/indicated by an 
N at the start of the value
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 46

---

## Page 46

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Transaction Tax SWIFT Tag/Qualifier: 
:19A::TRAX 
Field Name: Transaction 
Tax 
CSV Example: “EUR3,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=TRAX) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=TRANSACTION_ TAX)
Note the following:
 l If the market determined by 
PSET is Australia, 
ChargeTaxType of TRAX is 
mapped to 19A::VATA.
 l If 22F Stamp Duty Indicator is 
mapped with Data Source 
Scheme of CRST (such as 
STAM/CRST/value), then 
TRAX is mapped to 
19A::STAM.
Negative sign is mapped/indicated by 
an N at the start of the value
Value Added 
Tax
SWIFT Tag/Qualifier: 
:19A::VATA 
Field Name: Value Added 
Tax 
CSV Example: “EUR23,”
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=VATA) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=VALUE_ADDED_ TAX)
Negative sign is mapped/indicated by an 
N at the start of the value
→ Other Parties (Mandatory Subsequence F)
Originator of 
Message
SWIFT Tag/Qualifier: 
:95P::MEOR
Field Name: Party 
Originator of Message 
CSV Example: 
THANUS31XXX
TD InstructingParty/PartyValue 
ExecutingBroker/PartyValue 
(where PartyType=BIC) 
---
BIC
Note the following:
 l If the BIC is 11 characters 
long, it is mapped as-is.
 l If the BIC is 8 characters 
long, it is padded with ‘XXX’ 
and then mapped.
Additional Fields (See SWIFT Tag Location for the sequence or subsequence identifier of the fields.)
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 47

---

## Page 47

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Place of 
Clearing
SWIFT Tag/Qualifier: 
:94H::CLEA SWIFT Tag 
Location: Sequence B 
Field Name: Place of 
Clearing 
CSV Example: 
OMGOUS33XXX
TD PlaceOfClearing 
---
N/A
[[settlement]] Instruction Manager maps a 
valid BIC to Place of Clearing, which rep-
resents the place of clearing for the alloc-
ation.
Note the following:
 l If the BIC is 11 characters 
long, it is mapped as-is.
 l If the BIC is 8 characters 
long, it is padded with ‘XXX’ 
and then mapped.
[[collateral]] Pool 
Indicator
SWIFT Tag/Qualifier: 
:22F::COLE SWIFT Tag 
Location: Sequence E
Field Name: Indicator 
([[collateral]] Pool Indicator) 
SWIFT Codes: COLA or 
COLN
CSV Example: COLA
TD SettlementTransactionConditi
onIndicator 
---
[[collateral]] Pool Trade Indicator
Mapped if the value of 
SettlementTransactionConditionIndica
tor=COLA or COLN. 
Note that if both COLA and COLN are 
present in 
SettlementTransactionConditionIndica
tor, only the first value is mapped. 
Local Tax 
(country specific 
1)
SWIFT Tag/Qualifier: 
:19A::LADT SWIFT Tag 
Location: Subsequence 
E3
Field Name: Local Tax 
(country specific 1) 
CSV Example: EUR21,
TD ChargeAmount/Sign, 
CurrencyCode, and Amount 
(where 
ChargeTaxType=LADT) 
---
Trade Currency and 
Charge/Tax/Fee (where 
Type=LOCAL_TAX_ 
COUNTRY_SPECIFIC)
Negative sign is mapped/indicated by an 
N at the start of the value
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 48

---

## Page 48

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Yield to 
Maturity
SWIFT Tag/Qualifier: 
:92A::YTMR
SWIFT Tag Location: 
Subsequence B1
Field Name: Yield to 
Maturity Rate
CSV Example: “5,3”
TD Yield/YieldType=MATR
Yield/Sign, Yield/Amount 
---
N/A
Maps the value of YieldType to Yield to 
Maturity Rate. Only mapped for fixed 
income debt instruments. 
Negative sign is mapped/indicated by 
an N at the start of the value 
[[Buyer]]/[[Seller]] 
LEI
SWIFT Tag/Qualifier: 
:95L/ALTE
SWIFT Tag Location: 
Subsequence E1
Field Name: Party
CSV Example: 
ALTE/7478000080RH
C4YFEI25
TD LEI (sourced from 
counterparty's SSI) 
---
Cpty LEI
If the investment manager/ executing 
[[Broker]] (originator of message) is sub-
scribed to the Third Party Notification-LEI 
subscription [[Option]] (TLEI=Y) and an LEI 
is available, it is mapped to this field (95L 
ALTE tag).
Research Com-
mission SWIFT Tag/Qualifier   
:19A::RSCH
SWIFT Tag Location: 
Subsequence E3
Field Name: Research 
Amount
CSV Example: 
“EUR8000,”   
TD Commission/Sign, 
CurrencyCode, and Amount 
(where CommissionType 
=RSCH) 
---
Trade Currency and 
Commission Amount (where 
Type=RESEARCH_FEE)
Negative sign is mapped/indicated by an 
N at the start of the value
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 49

---

## Page 49

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Allocation UTI SWIFT Tag/Qualifier   
:20U::TRRF
SWIFT Tag Location: 
Subsequence A1
Field Name: Deal 
Reference
CSV Example: 
“CAD15,”     
TD AllocationUTI 
---
Allocation UTI
AllocationUTI is auto-generated in CTM 
for investment managers subscribed to 
auto-generation using the Auto Generate 
Trade UTIs subscription [[Option]] 
(AUTI=Y). Investment managers/ execut-
ing brokers that are not subscribed to 
AUTI can provide the AllocationUTI 
value during trade submission to CTM.
Resulting 
Amount SWIFT Tag/Qualifier: 
:19A::RESU
SWIFT Tag Location: 
Subsequence E3 
Field Name: Net Cash 
Amount CSV Example: 
“EUR51,” 
TD NetCashAmount 
--- 
Net Cash Amount 
If [[settlement]] Instruction Manager 
determines that the trade meets the 
criteria of a cross currency trade, then 
Map the values of source fields to 19A 
RESU. 
Exchange Rate SWIFT Tag/Qualified: : 
92B::EXCH 
SWIFT Tag Location: 
Subsequence E3
Field Name: Exchange 
Rate 
CSV Example: 
“GBP/USD/1,168” 
TD ExchangeRate/FromCurren
cy, 
ExchangeRate/ToCurrency, 
ExchangeRate/ExchangeR
ateAmount 
--- 
From Currency, To 
Currency, Exchange Rate 
If [[settlement]] Instruction Manager determ-
ines that the trade meets the criteria of a 
cross currency trade, then map the val-
ues of source fields to 92B EXCH.
Table 1.3  CSV File Specification
CSVFileFormatSpecification
1.CSVFile 50

---

## Page 50

CSV Field 
Name
SWIFT Tag / Qual-
ifier Field Name 
Codes CSV 
Example
AG/
TD/T-
L
CTM Mapping 
Source 
--- 
[[settlement]] 
Instruction Manager 
UI Mapping
 Note
Total Linked 
Instructions SWIFT Tag/Qualifier: : 
99B::TOSE 
SWIFT Tag Location: 
Sequence A 
Field Name: Total 
Linked Instructions 
CSV Example: 002
TD TotalSettlementInstructionN
umber
---
N/A
This value represents the number of 
dependent allocations associated to an 
Omni allocation. The maximum number 
of dependents can be 999.
Current Instruc-
tion Number SWIFT Tag/Qualifier: : 
99B::SETT
SWIFT Tag Location: 
Sequence A
Field Name: Current 
Instruction Number
CSV Example: 001
TD CurrentSettlementInstructio
nNumber
---
N/A
This value represents the current instruc-
tion number of the Omni linked alloc-
ations. An OMNI will always have a value 
of 000. Dependent instructions will 
always have a value from 001-999.
1   [[settlement]] Instruction Manager supports the following SWIFT codes: BCFD, BCPD, CBNS, CCPN, CDIV, CRTS, GTDL, 
SPCU, SPEX, XBNS, XCPN, XDIV, and XRTS.
2   [[settlement]] Instruction Manager supports the following SWIFT codes: BUTC, CLEN, DIRT, EXER, FRCL, NOMC, NPAR, PART, 
PHYS, RPTO, SHOR, SPDL, SPST, UNEX, and TRIP.
3   [[settlement]] Instruction Manager supports the following SWIFT codes: CONV, ETFT, ISSU, NETT, OAUX, OTCS, OWNI, PLAC, 
and TRAD.
4  [[settlement]] Instruction Manager supports the following SWIFT codes: GBAX, GBBX, GBCX, GBDX, GBEX, GBFX, GBGX, 
GBHX, GBIX, GBLX, GBMX, GBNX, GBOX, GBPX, GBRX, GBSX, GBTX, GBUX, GBVX, GBWX, GBXX, GB2X, GB3X, GB4X, 
GB5X, GB6X, GB7X, IEJX, IEQX, IEYX, IE1X, IE8X, and USTN.
5  The following PSET BICs merged into a single BIC, IBRCESMMXXX: IBRCESMM, IBRCESMMSCL, IBRCESMMCDE, 
IBRCESMMMVL, and IBRCESMMXXX.
Table 1.3  CSV File Specification
Cross Currency Trade
The [[settlement]] detail is determined to be a cross currency trade when
CSVFileFormatSpecification
1.CSVFile 51

---

## Page 51

 l The investment manager has provided a [[settlement]] Amount
 l The investment manager has provided an Exchange Rate, where the From Currency and To Currency 
contains different currencies.
Delivering/Receiving Agent Mapping (95a 
DEAG/REAG)
Sourced from one of the following, in order:
1. If Counterparty’s PSET = FRNYUS33XXX or DTCYUS33XXX, Delivering/Receiving Agent 
(95a DEAG/REAG) is mapped with value from ID1. Data Source Scheme for FRNYUS33XXX 
and DTCYUS33XXX are USFW and DTCYID respectively.
If ID1 is not present, Fatal error gets generated.
2. If Counterparty’s PSET is a 2-character valid country code,
 a. Delivering/Receiving Agent is mapped with value from SubAgentBIC. If SubAgentBIC is 
invalid, Fatal error is generated.
 b. If SubAgentBIC is not present, value from SubAgentName1, SubAgentAddress1, SubA-
gentName2 and SubAgentAddress2 is used to map to Delivering/Receiving Agent.
 c. If Delivering/Receiving Agent cannot be mapped from above two ways, Fatal error is gen-
erated.
3. If Counterparty’s PSET is not from #1 and #2 above, Delivering/Receiving Agent is mapped 
based on the Del/Rec Agent Format Priority (aka BIC LID Priority) configuration of that PSET 
BIC.
 a. If BIC LID Priority is BIC Format Only (aka BICX), Delivering/Receiving Agent is mapped 
with SubAgentBIC. If SubAgentBIC is not present or if it is invalid, Fatal error is generated.
 b. If BIC LID Priority is ID1 Format Only (aka LIDX), Delivering/Receiving Agent is mapped with 
ID1. Data Source Scheme (related to the PSET) is obtained. If Either ID1 or Data Source 
Scheme is not available, Fatal error is generated.
 c. If BIC LID Priority is BIC Format Supersedes ID1 Format (aka BICP):
 i. Delivering/Receiving Agent is mapped with SubAgentBIC as first priority. If SubA-
gentBIC is invalid, Fatal error is generated.
 ii. If SubAgentBIC is not present, as a second priority ID1 us used to map to Deliv-
ering/Receiving Agent. Data Source Scheme (related to the PSET) is obtained from the 
[[DTCC]] proprietary database.
 iii. If SubAgentBIC is not present and ID1 or Data Source Scheme is not available, Fatal 
error is generated.
 d. If BIC LID Priority is ID1 Format Supersedes BIC Format (aka LIDP):
CSVFileFormatSpecification
1.CSVFile 52

---

## Page 52

 i. Delivering/Receiving Agent is mapped with ID1 as first priority. Data Source Scheme 
(related to the PSET) is obtained.
 ii. If Either ID1 or Data Source Scheme is not available, SubAgentBIC is used as a second 
priority to map to Delivering/Receiving Agent.
 iii. If ID1 or Data Source Scheme is not present and SubAgentBIC is not present or invalid, 
Fatal error is generated.
 e. If BIC LID priority is BIC Format Supersedes Address:
 i. Delivering/Receiving Agent is mapped with SubAgentBIC as first priority. If SubA-
gentBIC is invalid, Fatal error is generated.
 ii. If SubAgentBIC is not present, SubAgentName1, SubAgentAddress1, SubAgentName2 
and SubAgentAddress2 is used to map to Delivering/Receiving Agent.
 iii. If Delivering/Receiving Agent is not mapped from above two ways, Fatal error is gen-
erated.
Note the following:
 
 l If BuySell=SELL, qualifier REAG is used.
 l If BuySell=BUYI, qualifier DEAG is used.
 l If BIC is 11 characters long, it is mapped as-is.
 l If BIC is 8 characters long, it is padded with XXX and then mapped.
 l If BIC LID Priority is not available, Delivering/Receiving Agent gets mapped with BIC Format Super-
sedes ID1 Format logic.
 l If a non-SWIFT character is received in text fields (i.e., fields with x-character set), it is replaced with 
space and error will not be generated. The CSV notification will be created with resulting value.
Handling of non-SWIFT characters in text fields
If a non-SWIFT character is received in text fields (i.e., fields with x-character set), it is replaced with space 
and no error will be generated. The CSV notification will be created with resulting value.
CSVFileFormatSpecification
1.CSVFile 53

---

## Page 53

Support of CTM Organizations without Valid 
Registered SWIFT BIC
If a CTM organization is set up with an invalid SWIFT BIC, the Originator of Message is sourced based 
on the below priority:
 o BIC Code of instructing party or executing [[Broker]] is mapped to Originator or the Message column 
as a first priority. The CSV will be created with the resulting value.
 o If BIC Code of instructing party or executing [[Broker]] is not a valid registered SWIFT BIC, Institution / 
Executing [[Broker]] BIC from the Instructing Party’s or Executing [[Broker]]’s SSI is mapped to Ori-
ginator of the Message column as a second priority.
 o If Institution / Executing [[Broker]] BIC from the Instructing Party’s or Executing [[Broker]]’s SSI is not a 
valid registered SWIFT BIC or is not provided, the Fatal Error is generated.
Example of a CSV File
The [[settlement]] Instruction Manager service requires that investment managers and brokers open the 
[[settlement]] Instruction Manager UI to view the CSV file format. Before you attempt viewing the CSV file 
format, ensure that you have the required subscriptions, and user roles.
To view the CSV file format:
 1. Open the [[settlement]] Instruction Manager UI and depending on your set-up, adjust the date range of 
the allocations shown below using Filters button.                                 
 2. Click on the CTM Allocation [[ID]] for the instruction you want to view.       
The [[settlement]] Instruction Detail View appears, an example of which is shown below.
CSVFileFormatSpecification
1.CSVFile 54

---

## Page 54

 3. Click on the hyperlinked CSV value in the Format column. The Notification Transmission – CSV 
window displays the full CSV file, an example of which is shown below.       
For more information, see CSV File Example below for instruction created on behalf of an InstructingParty. 
It shows how the CSV file header and data rows in the preceding figure correspond to a CTM TradeDetail. 
The shaded rows in the following table correlate to SWIFT sequences.
CSVFileFormatSpecification
1.CSVFile 55

---

## Page 55

The column headers represent the following:
 l Inbound to [[settlement]] Instruction Manager — CTM TradeDetail XPath: The XPaths in the column 
assume the TradeDetailBody composite as the root element. Each path is subsequent to one indent 
level.
For example, the first XPath InstructingParty/PartyValue represents:
 o InstructingParty at indent level 2, which is also a composite.
 o PartyValue at indent level 3, which is an element in the InstructingParty composite.
 l Outbound to Receiver—CSV File Header-Data Rows: The column lists the header row field and cor-
responding data row value or values, depending on the information in the CTM TradeDetail.
 l Meaning: Describes the value for the CSV file field.
 
Inbound to [[settlement]] Instruction 
Manager - CTM TradeDetail XPath
Outbound to Receiver CSV 
File Header-Data Rows
Meaning
Header Information
BuySellIndicator and InstructingParty/
PartyValue
Header: Message Type
Data: 541
The CSV file represents an 
instructing party where the 
BuySellIndicator=BUYI, which 
translates to an MT541.
CustodianBIC Header: Receiver’s Address
Data: 192.168.1.1/22/192.16.8.1.1.
Concatenation of domain name, 
port number, and destination 
directory for the CustodianBIC is 
192.168.1.1/22/192.168.1.1.
BuySellIndicator Header: Buy Sell Indicator
Data: BUYI
The instructing party is a [[Buyer]].
CTMTradeSideId Header: Trade Side [[ID]]
Data: 1561008333
CTM-supplied sender’s 
reference identifier for the block 
is 1561008333.
CTMTradeDetailID Header: TradeDetail [[ID]]
Data: 1561008333
CTM-supplied sender’s 
reference identifier for the 
allocation is 1561008333.
MasterReference Header: Master Reference
Data: NN060302443449
Client-supplied 
MasterReference is 
NN060302443449.
Table 1.4  CSV File Example
CSVFileFormatSpecification
1.CSVFile 56

---

## Page 56

Inbound to [[settlement]] Instruction 
Manager - CTM TradeDetail XPath
Outbound to Receiver CSV 
File Header-Data Rows
Meaning
ClientAllocationReference Header: Client Allocation Reference
Data: Alc-SNTF4
Client-supplied 
ClientAllocationReference is 
Alc-SNTF4.
NA—[[settlement]] Instruction Manager generates the 
value.
Header: Version Number
Data: 1
Administrative field.
NA—[[settlement]] Instruction Manager generates the 
value.
Header: Notification [[ID]]
Data: 96864
Administrative field.
NA—[[settlement]] Instruction Manager generates the 
value.
Header: Notification Order
Data: 1
Administrative field.
General Information
CTMTradeDetailID or [[settlement]] Instruction 
Manager generated value.
Header: Sender’s Reference
Data: 15610083334
Since FunctionOfTheMessage 
is NEWM, sender’s reference 
identifier is 15610083334.
FunctionOfTheMessage Header: Function of the Message
Data: NEWM
[[settlement]] instruction is for a 
new trade.
[[settlement]] Instruction Manager generates the 
value.
Header: Preparation Date/Time
Data: 20220603184507
Preparation date and time of 
instruction is June 3, 2022 at 
06:45:07 PM.
[[settlement]] Instruction Manager generates the 
value.
Header: Previous
Data: ,
Not generated since 
FunctionOfTheMessage is 
NEWM.
TDReferences/TDReferenceType,
TDReferences/TDReferenceValue
Header: Related Reference
Data: ,
Not supplied in the TradeDetail 
because it is not a block 
[[settlement]] trade.
TDReferences/TDReferenceType,
TDReferences/TDReferenceValue
Header: Pool Related Reference
Data: ,
Not supplied in the TradeDetail 
because it is not a block 
[[settlement]] trade.
Mandatory Trade Details
PlaceOfTrade/PlaceCode, PlaceOfTrade/ 
PlaceNarrative 
Header: Place of Trade Data:  Not supplied in the Trade Detail.
SettlementDate  Header: [[settlement]] Date Data: 
20220606
[[settlement]] date is June 06, 
2022.
TradeDateTime Header: Trade Date Data: 20220602 Trade date is June 02, 2022.
DealPrice/CurrencyCode, DealPrice/ Amount 
SecurityTypeGroup   
Header: Deal Price 
Data: "EUR27,12,”
Deal price for the allocation and 
corresponding instructions is 
€27.12
CSVFileFormatSpecification
1.CSVFile 57

---

## Page 57

Inbound to [[settlement]] Instruction 
Manager - CTM TradeDetail XPath
Outbound to Receiver CSV 
File Header-Data Rows
Meaning
Mandatory Identification of a Security
NumberOfDaysAccrued Header: Number of Days Accrued
Data: ,
Not supplied in the TradeDetail.
CountryCode Header: Country Code
Data: ,
Not supplied in the TradeDetail.
NumberingAgencyCode Header: Numbering Agency Code
Data: ISIN
Numbering agency code 
identifier for the traded security 
is ISIN.
SecurityCode Header: Security Code
Data: NO0008000015
Security code for the traded 
security is NO0008000015.
DescriptionOfTheSecurity Header: Description of The Security 1
Data: ODIN MARTIM
The security description is ODIN 
MARTIM.
DescriptionOfTheSecurity Header: Description of The Security 2
Data: ,
Not supplied in the TradeDetail.
DescriptionOfTheSecurity Header: Description of The Security 3
Data: ,
Not supplied in the TradeDetail.
DescriptionOfTheSecurity Header: Description of The Security 4
Data: ,
Not supplied in the TradeDetail.
Mandatory Financial Instrument/Account
CurrentFactor/Sign, CurrentFactor/Amount Header: Current Factor
Data: ,
Not supplied in the 
TradeDetail—allocation is not 
for a debt instrument.
PoolNumber Header: Pool Number
Data: ,
Not supplied in the 
TradeDetail—allocation is not 
for a mortgage-backed security.
MaturityDate Header: Maturity Date
Data: ,
Not supplied in the 
TradeDetail—allocation is not 
for a debt instrument.
CouponRate Header: Coupon Rate
Data: ,
Not supplied in the 
TradeDetail—allocation is not 
for a debt instrument.
TradeTransactionConditionIndicator Header: Trade Transaction Condition 
Indicator
Data: ,
Not supplied on the TradeDetail.
CSVFileFormatSpecification
1.CSVFile 58

---

## Page 58

Inbound to [[settlement]] Instruction 
Manager - CTM TradeDetail XPath
Outbound to Receiver CSV 
File Header-Data Rows
Meaning
BuySellIndicator and FXDealCurrencyCode Header: Currency
Data: ,
Not supplied on the 
TradeDetail—allocation does 
not require foreign exchange.
TDMatchStatus—CTM generates the value. Header: TD Match Status
Data: MACH
All L1 elements pair and L2 
elements for the trade 
components match. The 
allocation status of the trade is 
MATCHED.
AdditionalText Header: [[settlement]] Instruction 
Processing Narrative
Data: ,
Not supplied on the TradeDetail.
QuantityOfTheBlockTrade Header: Quantity of Financial Instrument
Data: “UNIT/2500,”
The allocation is for 2500 units 
of the traded security.
CurrentFaceValue Header: Current Face Value
Data: ,
Not supplied in the 
TradeDetail—not a debt 
instrument.
SecurityAccount Header: Security Account
Data: 654-328
Instructing party requires 
deposit of the 2500 bond units in 
security account 654-328.
CashAccountNo Header: Cash Account
Data: ,
Not supplied in the TradeDetail 
because instructing party uses a 
security account.
PlaceOfSafekeeping/Value, 
PlaceOfSafekeeping/Place
Header: Place Of SafeKeeping
Data: ,
Not supplied in the TradeDetail.
TradeDetailData/
SettlementTransactionConditionIndicator
Header: [[settlement]] Transaction 
Condition Indicator
Data: ,
Not supplied in the TradeDetail.
TypeOfTransactionIndicator Header: Type of [[settlement]] Transaction 
Indicator
Data: TRAD
[[settlement]] transaction relates to 
the [[settlement]] of a trade.
SettlementTransactionConditionIndicatorHeader: Stamp Duty Indicator
Data: ,
Not supplied in the TradeDetail.
Header: Registration Override Indicator
Data: ,
Header: Beneficial Ownership Override 
Indicator
Data: ,
CSVFileFormatSpecification
1.CSVFile 59

---

## Page 59

Inbound to [[settlement]] Instruction 
Manager - CTM TradeDetail XPath
Outbound to Receiver CSV 
File Header-Data Rows
Meaning
SettlementTransactionConditionIndicatorHeader: Cash [[settlement]] System 
Override Indicator
Data: ,
Not supplied in the TradeDetail.
Header: Forex Order Cancellation 
Indicator
Data: ,
Header: Netting Eligibility Indicator
Data: ,
SettlementTransactionConditionIndicatorHeader: Central Counter Party Eligibility 
Indicator
Data: ,
Not supplied in the TradeDetail.
Header: Letter of Guarantee Indicator
Data: ,
Header: [[settlement]] System Method 
Indicator
Data: ,
SettlementTransactionConditionIndicatorHeader: Real-Time Gross [[settlement]] 
System Indicator
Data: ,
Not supplied in the TradeDetail.
Header: Restrictions Indicator
Data: ,
Header: Block Trade Indicator
Data: ,
Mandatory [[settlement]] Details
BuySellIndicator and 
InstructingParty/PartyValue
Header: [[Buyer]]/[[Seller]]
Data: SELL/OMGOUS33XXX
Executing [[Broker]] is the [[Seller]] 
and its BIC is OMGOUS33XXX.
SecurityAccount Header: [[Buyer]]/[[Seller]] Safekeeping 
Account
Data: 23484493
Executing [[Broker]]’s safekeeping 
account number is 23484493.
CustodianBIC, CustodianName1, CustodianName2Header: Deliverer’s/Receiver’s 
Custodian
Data: ,
Not supplied in the 
TradeDetail—instructing party 
does not use a global custodian 
for the specified trade type.
CSVFileFormatSpecification
1.CSVFile 60

---

## Page 60

Inbound to [[settlement]] Instruction 
Manager - CTM TradeDetail XPath
Outbound to Receiver CSV 
File Header-Data Rows
Meaning
SubAccountNo Header: Deliverer’s/Receiver’s 
Custodian's Safekeeping   Account
Data: ,
Not supplied in the TradeDetail.
SubAgentBIC, ID1, or one or more of the following:
 l SubAgentName1 and SubA-gentName2
 l SubAgentAddress1 and SubA-gentAddress2
Header: Delivering/Receiving Agent
Data: BNPANOKKXXX
Executor is [[Seller]] and 
BNPANOKKXXX is the 
SubAgent BIC.
ID1, ID2 Header: Delivering/Receiving Agent’s 
Safekeeping Account
Data: 
Not supplied in the TradeDetail.
Relationship and CorrespBIC,
CorrespName1, CorrespName2
Header: Deliverer’s/Receiver’s 
[[intermediary]]
Data: ,
Not supplied in the 
TradeDetail—instructing party 
does not use an [[intermediary]] or 
correspondent for the trade type.
Relationship, CorrespSecAccountNo Header: Deliverer’s/Receiver’s 
[[intermediary]]’s Safekeeping Account
Data: ,
Not supplied in the TradeDetail.
PSET Header: Place of [[settlement]]
Data: VPSNNOKKXXX
Place of [[settlement]] is 
VPSNNOKKXXX.
Cash Parties 
Relationship, CorrespBIC Header: Account with Institution
Data: ,
Not supplied in the TradeDetail.
Relationship, CorrespCashAccountNo Header: Cash Account
Data: ,
Mandatory Amounts
AccruedInterestAmount/Sign, 
AccruedInterestAmount/CurrencyCode, 
AccruedInterestAmount/Amount
Header: Accrued Interest Amount
Data: ,
Not supplied in the TradeDetail.
ChargeAmount/Sign, ChargeAmount/
CurrencyCode, ChargeAmount/Amount
Header: Charges or Fees
Data: ,
ChargeAmount/Sign, 
ChargeAmount/CurrencyCode, 
ChargeAmount/Amount
Header: County National Federal Tax
Data: ,
TradeAmount/Sign,TradeAmount/CurrencyCode, 
TradeAmount/Amount
Header: Trade Amount
Data: “EUR67500,”
The cost of the allocation is 
€67500.
CSVFileFormatSpecification
1.CSVFile 61

---

## Page 61

Inbound to [[settlement]] Instruction 
Manager - CTM TradeDetail XPath
Outbound to Receiver CSV 
File Header-Data Rows
Meaning
CommissionReasonCode, 
Commission/CurrencyCode, Commission/Amount
Header: Executing [[Broker]]’s Amount
Data: ,
Not supplied in the TradeDetail.
ChargeAmount/Sign, 
ChargeAmount/CurrencyCode, 
ChargeAmount/Amount
Header: Payment Levy Tax
Data: ,
ChargeAmount/Sign, 
ChargeAmount/CurrencyCode, 
ChargeAmount/Amount
Header: Local Tax
Data: ,
CommissionReasonCode, 
Commission/CurrencyCode, Commission/Amount
Header: Local [[Broker]]'s Commission
Data: “,”
Not supplied in the TradeDetail.
ChargeAmount/Sign, 
ChargeAmount/CurrencyCode, 
ChargeAmoun/Amount
 
Header: Other Amount
Data: ,
Not supplied in the TradeDetail.
Header: Regulatory Amount
Data: ,
SettlementAmount/Sign, 
SettlementAmount/CurrencyCode, 
SettlementAmount/Amount
Header: [[settlement]] Amount
Data: “EUR68200,”
[[settlement]] amount is 
EUR68200.
Note: The SettlementAmount 
composite was populated, so 
CTM derived the value. If the 
SettlementAmount had been left 
blank, CTM would have derived 
the NetCashAmount composite.
ChargeAmount/Sign, 
ChargeAmount/CurrencyCode, 
ChargeAmount/Amount
Header: Shipping Amount
Data: ,
Not supplied in the TradeDetail.
ChargeAmount/Sign, 
ChargeAmount/CurrencyCode, 
ChargeAmount/Amount
Header: Special Concessions Amount
Data: “,”
Not supplied in the TradeDetail.
ChargeAmount/Sign, 
ChargeAmount/CurrencyCode, 
ChargeAmount/Amount
Header: Stamp Duty
Data: ,
Not supplied in the TradeDetail.
Header: [[Stock]] Exchange Tax
Data: ,
Header: Transfer Tax
Data: ,
ChargeAmount/Sign, 
ChargeAmount/CurrencyCode, 
ChargeAmount/Amount
Header: Transaction Tax
Data: ,
Not supplied in the TradeDetail.
CSVFileFormatSpecification
1.CSVFile 62

---

## Page 62

Inbound to [[settlement]] Instruction 
Manager - CTM TradeDetail XPath
Outbound to Receiver CSV 
File Header-Data Rows
Meaning
ChargeAmount/Sign, 
ChargeAmount/CurrencyCode, 
ChargeAmount/Amount
Header: Value Added Tax
Data: ,
Not supplied in the TradeDetail.
InstructingParty/PartyValue Header: Originator of Message
Data: ZYOTUS30CCA
Originator of message is the 
Instructing Party BIC 
ZYOTUS30CCA.
Place Of Clearing Header: Place Of Clearing
Data: ,
Not supplied in the TradeDetail.
IndicatorSettlementTransactionConditionIndicatorHeader: [[collateral]] Pool Indicator
Data: ,
ChargeAmount/Sign, 
ChargeAmount/CurrencyCode, 
ChargeAmount/Amount
Header: Local Tax (country specific 1)
Data: ,
Yield/YieldType=MATR Yield/Sign Yield/Amount  Header: Yield to Maturity 
Data: , 
Not supplied in the TradeDetail.
LEI (sourced from counterparty's SSI) Header: [[Buyer]]/[[Seller]] LEI 
Data: 
ALTE/549300DMVUWLVUJLNM35, 
The legal entity identifier of the 
Executing [[Broker]] is 
549300DMVUWLVUJLNM35.
CommissionReasonCode, Com-
mission/CurrencyCode, Commission/Amount Header: Research Commission 
Data: , 
Not supplied in the TradeDetail.
AllocationUTI Header: Allocation UTI 
Data: 
Not supplied in the TradeDetail.
NetCashAmount/Sign,   NetCashA-
mount/CurrencyCode, NetCashAmount/Amount  Header: Resulting Amount* 
Data:   
Not supplied in the TradeDetail.
ExchangeRate/FromCurrency 
ExchangeRate/ToCurrency ExchangeRate/Ex-
changeRateAmount 
Header: Exchange Rate* 
Data:   
Not supplied in the TradeDetail.
TotalSettlementInstructionNumber Header: Total Linked Instructions* 
Data:
Not present as this trade is not 
an Omnibus Block [[settlement]] 
trade
CSVFileFormatSpecification
1.CSVFile 63

---

## Page 63

Inbound to [[settlement]] Instruction 
Manager - CTM TradeDetail XPath
Outbound to Receiver CSV 
File Header-Data Rows
Meaning
CurrentSettlementInstructionNumber Header: Current Instruction Number* 
Data:
Not present as this trade is not 
an Omnibus Block [[settlement]] 
trade
* These [[DO]] not appear in the example above, but note, that the header name will always appear in the CSV message. 
 l The values Resulting Amount and Exchange Rate will only be present if supplied in   the Trade Detail 
and   the trade is identified as a Cross Currency Trade.
 l The values for Total Linked Instructions and Current Instruction Number will only be present for an 
Omnibus Block [[settlement]] trade.
CSVFileFormatSpecification
1.CSVFile 64

---

## Page 64

© 2023 [[DTCC]]. All rights reserved.   [[DTCC]], [[DTCC]] (Stylized), and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust 
& Clearing Corporation (“[[DTCC]]”).   [[DTCC]] itself does not provide such services.   Each of these affiliates is a separate 
legal entity, subject to the laws and regulations of the particular country or countries in which such entity operates. 
Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
 
 
Doc Date: October 10, 2023
Publication Code: SIM021
Service: [[settlement]] Instruction Manager
Title: CSV File Format Specification
For More Information
 
Email [[DTCC]] Learning at:
DTCCLearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com