---
title: "JFSA Rewrite Functional Change Document (Prod)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/JFSA%20Rules%20Rewrite%20Functional%20Change_1.0%20%28Prod%29.pdf"
pages: 67
size: "1445.9 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# JFSA Rewrite Functional Change Document (Prod)

**Original File:** [JFSA Rules Rewrite Functional Change_1.0 (Prod).pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/JFSA%20Rules%20Rewrite%20Functional%20Change_1.0%20%28Prod%29.pdf)  
**Category:** Rules  
**Total Pages:** 67  
**File Size:** 1445.9 KB  

---

## Page 1

 
 
 
 
 
 
 
 
 
 
GLOBAL TRADE REPOSITORY 
FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE 
VERSION 1.0 [PROD] 
FEB 15, 2024 
 


---

## Page 2

[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository 
Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a 
separate legal entity, subject to the laws and regulations of the particular country or countries in which such entity 
operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: 15 Feb 2024 
Service: RDS 
Title: JFSA RULES REWRITE FUNCTIONAL CHANGE 
 

---

## Page 3

[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
 
 
Document Revision History 
Date Author Version Description 
2/10/2023 FA 0.1 Initial Draft 
2/28/2023 FA 0.2 First External Version 
5/12/2023 FA 0.3 (a) FC 5.2 – Added Delta as a field to consider when 
merging to TSR under point 1  
(b) FC 6.3, 6.4 – Added data migration exclusions 
(c) FC 1 – Updated connectivity links to the learning 
centre to specifically reference JFSA instructions and 
connectivity details and MQ details 
(d) FC 3.1 – Provided example of schema validation 
scenario 
(e) FC 3.7 – Updated validation conditions for ERR 
and RCP 
(f) FC 5 – Blank Reports will not be generated 
(g) FC 3.5 & 3.6 – Removed the requirement on 
restricting trade level [[collateral]] and trade valuations 
on matured/exited trades up till 180 days 
(h) FC 5.1 – Updated report names from [[collateral]] to 
[[Margin]] Activity and State Reports 
(i) FC 3.8 – Updated Action Type Rules and 
Validations 
(j) FC 4.1 – Updated specifications on the ACK/NACK 
response format 
7/14/2023 FA 0.4 (a) FC 6.5 – Submission of legacy trades post go-live 
(b) FC 3.8 – Updated conditions for Action Type Rules 
for REVI and MARU 
(c) FC 1 – Updated sFTP 
 product IDs for clarity between UAT and Prod 
(d) FC 2.1 – added link to message samples 
(e) FC 3.5 – updated mandatory requirement to 
submit portfolio code so [[DTCC]] can derive portfolio 
indicator 
(f) FC 2.3, 3.13, 5.3, 5.4, 3.14, 3.15 – Added new 
sections 
(g) FC 6.1 – Clarified MODI requirement for 
resubmitting post go-live and include CORR 
(h) FC 5.1 – Added [[EOD]] Allege Report and Intraday 
Allege Activity Report and concept of Event 

---

## Page 4

[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
 
Date Author Version Description 
Timestamp on TSR 
(i) FC 3.1 – Added details around file rejection 
scenarios 
(j) FC 4.1 – added batch download report filename 
format details 
 
9/15/2023 FA 0.5 (a) FC 5.4 – Updated typo on Report File Name for 
JFSA Trade State Report CSV and updated naming 
convention for several reports to include the JFSA 
jurisdiction & the filename convention and Intraday 
Allege Report specifications. Increased report 
availability on portal to up to 12 months 
(b) FC 3.8 – Updated the action type workflow 
diagram to clarify sub bullet point 5, though no 
changes to the actual workflow 
(c) FC 3.1 – added scenario (d) for a file level reject 
and description of case-sensitive approach 
(d) FC 7 – Added billing sections 
(e) FC 4.1 – updated file response formats to include 
zip 
(f) FC 2.3 – added validation of the from tag on the 
message header against each records’ SubmitgAgt 
tag 
(g) FC 3.3 – updated to include the support of the 
proprietary [[ID]] tag in the Unique transaction identifier 
(UTI) data element 
(h) FC 6 – Introduced the Proprietary [[ID]] tag for trade 
identifiers, hence the entire section need to be 
reviewed 
(i) FC 4.3 – Introduced MQ Reply to Queue 
functionality to return ACK/NACK responses 
(j) FC 3.14 – updated Other Payments uniqueness 
key and use case scenarios 
11/17/2023 FA 0.6 (a) FC 5.3 Added report management hyperlink to 
[[DTCC]] Learning 
(b) FC 6.2 Updated action type event type validation 
requirements on initialized trades for clarity 
(c) FC 4.1 – corrected typo to remove space before 
BizMsgIdr in the sFTP filename and updated start of 
the filename from SFTP to lowercase sFTP 
(d) FC 3.16 – new section 

---

## Page 5

[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
 
Date Author Version Description 
(e) FC 3.14 – updated Other Payment uniqueness key 
by replacing Other Payment Currency to Other 
Payment Date and use-case scenarios 
(f) FC 5.4 – updated report filenames for clarity, and 
also ERR to get access to Trade Submission Report 
and [[Margin]] Submission Report 
(g) FC 2.3 – introduced validation requirements for 
BizMsgIdr 
(h) FC 3.13 – Aggregated o-code timeline update 
 
01/31/2024 FA 0.7 (a) FC 4.1 – updated to reflect current BDR filename 
and future filename 
(b) FC 6.2 – updated prod dry run date 
(c) FC 3.1 – added illustration of an example for 
numeric data type 
02/15/2024 FA 1.0 (a) FC 3.8 – Added Event Type Table for illustration 
and added example of stateful validation around event 
and reporting timestamp.  
(b) FC 6.7 – updated schedule for UAT5 
(c) FC 7.2 – updated Billing Substantiation Report 
format 
(d) FC 6.2 – Updated data initialization dry run date 
and report names 
(e) FC 3.10/11 – updated use cases for change in 
counterparty and reporting counterparty 
 
 

---

## Page 6

[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
 
TABLE OF CONTENTS 
Document Revision History ................................................................................................................................ 3 
1. Summary ........................................................................................................................................................... 8 
Background ......................................................................................................................................................... 8 
In-Scope .............................................................................................................................................................. 8 
Out of Scope ....................................................................................................................................................... 9 
Reference Documents ......................................................................................................................................10 
Naming Conventions and Definitions................................................................................................................10 
2. Functional Change Requirements ................................................................................................................ 12 
FC 1: Connectivity: Message Channel, Routing and Submission Methods  .....................................................12 
FC 2: Ingestion – Message Types and Submission Formats ...........................................................................14 
FC 2.1: Inbound Message Types and Submission Formats ...........................................................................14 
FC 2.2: Special Characters .............................................................................................................................14 
FC 2.3: Message Header Format ....................................................................................................................14 
FC 3: Ingestion - Processing of Submissions ...................................................................................................17 
FC.3.1: Message Validations ..........................................................................................................................17 
FC 3.2: Message Sequencing .........................................................................................................................18 
FC 3.3: Trade Identifiers..................................................................................................................................19 
FC 3.4: Uniqueness of a Trade .......................................................................................................................19 
FC 3.5: [[collateral]] Message Submissions .......................................................................................................19 
FC 3.6: Trade Valuation Submissions .............................................................................................................21 
FC 3.7: Reporting Counterparty and Entity Responsible for Reporting ..........................................................21 
FC 3.8: Action Type and Event Type Validations ...........................................................................................22 
FC 3.9: Submissions with Reduced Validations..............................................................................................27 
FC 3.10: Change of Counterparty ...................................................................................................................28 
FC 3.11: Change of Reporting Counterparty ..................................................................................................29 
FC 3.12: JFSA Usage Guidelines ...................................................................................................................30 
FC 3.13: Introduction of an Aggregated O-Code ............................................................................................30 
FC 3.14 Other Payment Fields ........................................................................................................................31 

---

## Page 7

[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
 
FC 3.15 Schedule Fields .................................................................................................................................36 
FC 3.16 Event Timestamp & Reporting Timestamp .......................................................................................41 
FC 4: Message Responses ..............................................................................................................................47 
FC 4.1 Response Format ................................................................................................................................47 
FC 4.2 Response Format/Channel .................................................................................................................53 
FC 4.3 MQ Response to be sent to ReplytoQueue ........................................................................................53 
FC 5: Reports ....................................................................................................................................................53 
FC 5.1: Report Types ......................................................................................................................................53 
FC 5.2: Merging of Trade Valuation Information onto Trade State Report .................................................5857 
FC 5.3: Self-Service Report Management Functionality ..................................................................................58 
FC 5.4: Report Filename Formats ....................................................................................................................58 
FC 6: Functionality Specific to Go-Live ............................................................................................................61 
FC 6.1:  [[DTCC]] Action Type Initialization at Go-live – Trade State .................................................................61 
FC 6.2: Data Migration Dry Run Plan ..............................................................................................................62 
FC 6.3:  Removal of “Duplicate” Positions Due to Trade Uniqueness Change ..............................................63 
FC 6.4: Exclusion of Self Trades .....................................................................................................................64 
FC 6.5: Upgrading Open Trades After Go-Live ..............................................................................................64 
FC 6.6:  Reporting During Transition Period ...................................................................................................64 
FC 6.7: Go-Live Schedule ...........................................................................................................................6564 
FC 7: Billing .......................................................................................................................................................65 
FC 7.1:  Billing Hierarchy.................................................................................................................................65 
FC 7.2:  Billing Substantiation Report .............................................................................................................65 
 

---

## Page 8

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 8 
 
 
1. SUMMARY 
Background 
The JFSA Rules Re-write initiative will ensure that the GTR implements the JFSA’s newly adopted 
amendments to the swap reporting regulations for the April 1, 2024, compliance date. The changes associated 
with the Rules Rewrite initiative will impact all five reportable [[Asset]] classes (credit, interest rates, equities, 
commodities, and FX) for Trade State, and introduce Trade Valuation, and [[Margin]] reporting. Note that 
commodities become in scope for reporting if crypto trades are classified under Commodities [[Asset]] class. All 
other traditional commodities products remain out of scope for JFSA reporting. There are 137 proposed data 
fields consisting of 98 CDE, 20 ESMA, and 19 [[CFTC]] fields. Delta and UPI are proposed to be optional for 1 
April 2024, and JFSA is proposing to implement UPI on April 7, 2025, thus arriving at the end state of 139 data 
fields. Users will be required to submit in ISO XML 20022 format commencing April 1, 2024, and the transition 
deadline to update trades is set on 27 Sep 2024, which is 180 days from the initial go-live date.  There will be a 
minimum set of required fields required on Day 1 for backloading existing open positions, followed by a Phase 
2 where the users are expected to enrich the remainder of the data fields and to enrich all historical positions in 
accordance with the final rules. The same approach applies to direct reporters who will commence reporting 
through DDRJ. The users who are ready on April 1, 2024, are encouraged to backload fully enriched open 
positions on April 1, 2024, and full re-reporting is required from existing DDRJ users. For the avoidance of 
doubt, the brand-new trades executed/reported on/after April 1, 2024, need to be reported with all required 
fields populated under new framework.  
In-Scope 
The scope of this document will cover the following changes: 
Items Description 
Compliance Date 2 step approach 
First go-live date: 1 April 2024 – Minimum required fields (refer 
to the JFSA message specifications), in ISO XML format. All 
trade submissions after this date regardless of if they are new or 
historical transactions will be validated the same way 
Second date: 27 September 2024 – Enrichment of rest of data 
fields expected and re-reporting deadline 
UPI While the rules are clear that UPI is out of scope for April 1, 
2024, UPI will be made optional. JFSA has proposed to 
implement UPI for April 7, 2025 
LEI 
 
  
Renewed LEI will be mandated for the Reporting Counterparty 
(RCP), Entity Responsible for Reporting (ERR) and Central 
Counterparty. RCP and LEI will be validated using the GLEIF 
database for a valid status. Details are covered in the message 
specifications 

---

## Page 9

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 9 
 
 
Out of Scope 
This project will not include: 
• Full Implementation of UPI (Unique Product Identifier) which is being reviewed for a future implementation 
date currently expected to be 7 April 2025 
• Fee Schedule Changes which will be reviewed at a future date  
Items Description 
UTI UTI will be mandated for reporting new trades. The trade linking 
logic will only be based on UTI + RCP + OCP in most cases but 
UTI + RCP for some action types. USI and the Transaction [[ID]] 
fields will be retired and removed from the trade linking logic. 
ISO XML ISO XML will be mandated for inbound messages. 
ISO XML schema does not support cross jurisdiction reporting. 
[[DTCC]] XML will not be supported. 
Usage guidelines will be published.  
FPML FpML will be decommissioned with the mandate of ISO XML. 
We will no longer support FpML for JFSA reporting. 
For cross jurisdiction reporting with jurisdictions who continue to 
accept FpML, submissions will need to be made separately. 
CSV CSV submissions will be decommissioned with the mandate of 
ISO XML. We will no longer support CSV for JFSA reporting. 
This includes both the Harmonized and [[OTC]] Legacy submission 
templates. 
For cross jurisdiction reporting with jurisdictions who continue to 
accept CSV, submissions will need to be made separately. 
Trade Linking Logic The trade linking logic will only be based on UTI +RCP + OCP in 
most cases but UTI + RCP for some action types. 
Data Migration No data migration expected from the TR. Data initialization 
details are described in the requirements under Section 6 
Message Specifications There will be changes to the way existing fields are supported 
and ingested. 
The message specifications illustrate the requirements of the 
new [[regulation]]. 
Message Types Trade State, Valuations and [[collateral]] Valuation message will be 
supported via Action Type Rules 
Reports Outbound to the regulator is XML format. For the users, it will be 
CSV reports. Users will only receive CSV as [[default]] though there 
may be exceptional cases where the users need both.  
Action Type / Event Type Rules Action Type/Event Type Rules will be newly implemented 

---

## Page 10

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 10 
 
 
Reference Documents  
This document should be read in conjunction with the following documents: 
1. The JFSA Message Specification and all other documents related to this implementation will be available 
on the “Upcoming Changes” section under the JFSA Re-Write of the GTR Learning Center. 
2. JFSA Usage Guidelines and other published regulations/documentation  
Naming Conventions and Definitions 
Abbreviation/ 
Term Name 
Definition/Description 
ACK GTR Success Acknowledgement Message 
Channel A unidirectional link between two end points or queue managers that serves to transfer 
messages 
CSV Comma Separated Values – a submission format accepted for messages in GTR 
[[DTCC]] The Depository Trust and Clearing Corporation 
FpML Financial Product Markup Language – XML based submission type for the GTR and Canada 
PPD 
GTR Global Trade Repository 
JFSA Financial Services Agency of Japan 
LEI Legal Entity Identifier 
MQ Message Queue – message-oriented middleware. Provides mechanism for applications to 
communicate. 
Message 
Specification 
Instructions for submitting into a given GTR application. Includes data attribute requirements, 
valid values, validations, CSV submission layouts and parsing definitions.  This document can 
be found on the Learning Center. 
NACK GTR Negative Acknowledgement message 
O-Code Operations Code – used to segregate and permission accounts 
OCP Other Counterparty (also referenced as Trade Party 2 generically) 
RCP Reporting Counterparty (also reference as Trade Party 1 generically) 
SDO Account Management System that [[DTCC]] uses to define accounts, products and services 
associated with these participants 

---

## Page 11

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 11 
 
 
Abbreviation/ 
Term Name 
Definition/Description 
SDR Swap Data Repository 
sFTP Secure File Transfer Protocol 
Trade State Trade state is the latest trade message that has been received and processed by GTR. 
TSR Trade State Report.  [[EOD]] report of all open [[Derivatives]] transactions (with latest valuation 
information merged onto the report). 
UAT GTR Test Environment (“User Acceptance Testing”) 
UPI Unique Product Identifier 
USI Unique Swap Identifier 
UTI Unique Trade Identifier 
XML In this document, refers to ISO 20022 XML 
 
  

---

## Page 12

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 12 
 
 
2. FUNCTIONAL CHANGE REQUIREMENTS 
FC 1: Connectivity: Message Channel, Routing and Submission 
Methods  
There will be no changes to the current submission channels and methods supported by the GTR. The GTR 
will continue to offer users the ability to connect to the application through the same channels or protocols to 
submit or receive data, namely: web portal, MQ and sFTP. 
The ISO XML message does not support a Service destination / Reporting Obligation field; therefore, routing 
will be determined from the following three sub-points. Each jurisdiction will have separate inbound product IDs 
/ queues. 
(i) The web upload feature that is offered through the Portal/GUI will only support direct upload to the 
jurisdiction service that the user selects on the screen. 
(ii)  The dedicated sFTP product [[ID]] for JFSA will determine the destination / jurisdiction service where the 
GTR must send the file. These product IDs will be newly setup for the JFSA re-writes and will require new 
subscriptions to be setup by reporting firms. 
(iii) The dedicated message queue for JFSA will determine the destination / jurisdiction service where the 
users must send the message to. The queue details are provided below. 
RDS MQ Input Queues 
[[Asset]] Class/Product RDS Sub-
Services 
Queue 
Manager 
[[DTCC]] Input Queue 
Name Description 
Commodity JFSA MU1R, MP1R GTR.JFSA_COMMODITY.A01 [[DTCC]] input queue for JFSA 
(Re-Write) 
Credits JFSA MU1R, MP1R GTR.JFSA_CREDITS.A01 [[DTCC]] input queue for JFSA 
(Re-Write) 
[[Equity]] JFSA MU1R, MU2R, 
MP2R GTR.JFSA_EQUITY.A01 [[DTCC]] input queue for JFSA 
(Re-Write) 
FX JFSA MU1R, MP5R-
MP9R GTR.JFSA_FX.A01 [[DTCC]] input queue for JFSA 
(Re-Write) 
Rates JFSA MU1R, MP1R GTR.JFSA_RATES.A01 [[DTCC]] input queue for JFSA 
(Re-Write) 
[[Margin]] Activity Submission JFSA MU1R, MP1R GTR.JFSA_MARGIN.A01 [[DTCC]] input queue for JFSA 
(Re-Write) 
 
Further description of the current functionality can be found on the Learning Center in the Connectivity section: 
Refer here for the Learning Centre connectivity documentation page. Overall connectivity requirements can be 
found in the GTR JFSA Rewrite and EMIR Refit sFTP Connectivity Starter Pack on the Learning Center.   
Specific connectivity details regarding the JFSA Re-Write can be found in the starter pack including onboarding 
details, report product IDs and connectivity guidance. A summary of the sFTP product IDs is provided below 
where the report IDs in green and denoted with an asterisk are for Production.  UAT product IDs are prefixed 
with 298 instead of 250.

---

## Page 13

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 13 
 
 
  
Schema Description Format [[collateral]] Commodity Credit [[Equity]] Rates FX 
auth.030.001.03_JFSAUG_DATTAR_1.0.0  JFSA Trade Activity 
Submission XML ISO20022XML   60978 
auth.108.001.01_JFSAUG_DATMDA_1.0.0  JFSA [[Margin]] Activity 
Submission XML ISO20022XML 60979   
auth.031.001.01_JFSAUG_FDRES_1.0.0 
JFSA GTR Batch 
ACK/NACK Report 
XML 
ISO20022XML 2503233 * 
auth.030.001.03_JFSAUG_DATTAR_1.0.0  JFSA Trade Activity 
Report XML ISO20022XML   2503234 * 
auth.107.001.01_JFSAUG_DATTSR_1.0.0 JFSA Trade State 
Report XML ISO20022XML   2503235 * 
auth.108.001.01_JFSAUG_DATMDA_1.0.0 JFSA [[Margin]] Activity 
Report XML ISO20022XML 2503236 *   
auth.109.001.01_JFSAUG_DATMDS_1.0.0  JFSA [[Margin]] State 
Report XML ISO20022XML 2503237 *   
auth.030.001.03_JFSAUG_DATTAR_1.0.0  JFSA Trade Activity 
Report CSV CSV equivalent   2503238 * 
auth.107.001.01_JFSAUG_DATTSR_1.0.0 JFSA Trade State 
Report CSV CSV equivalent   2503239 * 
auth.108.001.01_JFSAUG_DATMDA_1.0.0 JFSA [[Margin]] Activity 
Report CSV CSV equivalent 2503240 *   
auth.109.001.01_JFSAUG_DATMDS_1.0.0  JFSA [[Margin]] State 
Report CSV CSV equivalent 2503241 *   
N/A 
JFSA [[collateral]] 
Submission Report 
CSV 
CSV only 2503242 *   
N/A JFSA [[EOD]] Submission 
Report CSV CSV only   2503243 * 
N/A JFSA [[EOD]] Allege 
Report CSV CSV only  2503248 * 
N/A JFSA Intraday Allege 
Report CSV CSV only  2503249 * 
auth.030.001.03_JFSAUG_DATTAR_1.0.0  JFSA Regulator Trade 
Activity Report XML ISO20022XML   2503244 * 
auth.107.001.01_JFSAUG_DATTSR_1.0.0 JFSA Regulator Trade 
State Report XML ISO20022XML   2503245 * 
auth.108.001.01_JFSAUG_DATMDA_1.0.0 JFSA Regulator [[Margin]] 
Activity Report XML ISO20022XML 2503246 *   
auth.109.001.01_JFSAUG_DATMDS_1.0.0  JFSA Regulator [[Margin]] 
State Report XML ISO20022XML 2503247 *   

---

## Page 14

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 14 
 
FC 2: Ingestion – Message Types and Submission Formats 
FC 2.1: Inbound Message Types and Submission Formats 
The following message types are allowed, utilizing the inbound submission formats in this table.   Note that 
[[Asset]]-class based Legacy CSV and FpML message formats will no longer be supported. 
 
Legacy CSV templates & FpML for Trade State submissions will no longer be supported.  
The [[DTCC]] Message Specifications contain the detailed formats for each of the data fields, the business rules, 
and the XML x-paths details. 
JFSA Usage Guidelines will supplement the message specifications and illustrate the data field requirements, 
including formats and enumerations that users must adhere to.  
[[DTCC]] will support submissions via the Portal web upload, MQ and sFTP. File -based web upload or sFTP 
submissions will allow for multiple records within a file, however MQ submissions will be based on single 
record per message. Message sample formats are provided here. 
FC 2.2: Special Characters 
All submissions should limit their character sets to UTF-8.   
Generally, the ISO schema expects that all characters should be alphanumeric. Unless explicitly mentioned, 
fields are generally alphanumeric unless otherwise explicitly mentioned in the message specif ications. [[DTCC]] 
will implement validations in this regard as per the Message Specifications and JFSA Usage Guidelines.  
FC 2.3: Message Header Format 
Each submission must follow a prescribed header format. Otherwise, the entire file or message will be rejected. 
The samples published on the learning centre shows the relevant tags that will be required. The table below 
shows the header elements, the definition, the xpaths and sample values. To prevent unauthorized 
submissions to incorrect entities, the validations include the following: 
(a) For SFTP mode, GTR will validate the o-code present in sftp filename against the AppHdr o-code, and 
if there is a mismatch in the o-code, a file reject would occur  
Message Type Schema Requirements 
Transaction 
(Trade State) 
XML - auth.030.001.03_JFSAUG_DATTAR_1.0.0 
Valuation XML - auth.030.001.03_JFSAUG_DATTAR_1.0.0 
[[collateral]]/[[Margin]] XML - auth.108.001.01_JFSAUG_DATMDA_1.0.0 

---

## Page 15

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 15 
 
(b) For Web portal submissions, GTR will validate the o-code user select while uploading their 
submissions in the portal with AppHdr o-code, and if there is a mismatch in the o-code, a file reject 
would occur 
(c) For all the modes including MQ, we are validating the submitting agent o-code within each of the xml 
report against the AppHdr o-code 
Other validations include: 
(a) The date value on Creation Date timestamp cannot be more than 1 day from the message received 
timestamp date 
(b) The date value on Creation Date cannot be a future date 
 
 
Element 
Name  Usage Xpath  Data 
type  
Cond
ition 
Schema 
version  Sample value  
Hdr 
Envelope to 
include 
Application 
Header 
//element(*,BusinessDa
taHeaderV01)/Hdr strict  Mand
atory 
head.003.0
01.01.xsd Refer to picture “Hdr” 
Pyld 
Includes the 
body of the 
Business 
Message. Pyld 
would 
encapsulate 
<Document> 
which is the 
trade data 
based on 
auth.030 or 
auth.108. 
//element(*,BusinessDa
taHeaderV01)/Pyld N/A Mand
atory 
head.003.0
01.01.xsd Refer to picture “Pyld” 
From  
[[ID]] of 
BusinessApplic
ation A. Firms 
to indicate 
report 
submitting 
entity o-code 
AppHdr/Fr/OrgId/[[ID]]/Org
[[ID]]/Othr/[[ID]] 
Max35T
ext 
Mand
atory 
head.001.0
01.02 6ABC 
To 
[[ID]] of 
BusinessApplic
ation B. Firms 
to indicate 
submission to 
the applicable 
trade 
repository 
service 
AppHdr/To/OrgId/[[ID]]/Or
gId/Othr/[[ID]] 
Max35T
ext 
Mand
atory 
head.001.0
01.02 DDRJ 
BusinessMess
ageIdentifier 
Identification of 
the Business 
Message. A 
unique 
identifier firms 
can use to 
identify their 
submission file 
AppHdr/BizMsgIdr 
Max35T
ext 
Alphanu
meric(0-
9a-zA-
Z), 
undersco
re(_), 
hyphen(-
) and 
dot(.) 
Mand
atory 
head.001.0
01.02 ABC123456789 

---

## Page 16

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 16 
 
MessageDefini
tionIdentifier 
Identification of 
the Message 
Definition   
AppHdr/MsgDefIdr Max35T
ext 
Mand
atory 
head.001.0
01.02 
auth.030.001.03_JFS
A_DATTAR_1.0.0 
CreationDate 
Date and Time 
of the creation 
of the 
BusinessApplic
ationHeader 
and Business 
Message 
(Payload/Trade
/[[Margin]] Data) 
AppHdr/CreDt ISODate
Time 
Mand
atory 
head.001.0
01.02 
2001-12-
17T09:30:47Z 
 
“Hdr” 
 
 
 
“Pyld” 
 
 


---

## Page 17

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 17 
 
The o-code indicated in the “From” tag in the message header will be checked against each submitted record’s 
“SubmitgAgt” tag to ensure the record submitted is valid and to prevent unauthorized submissions of 
accidentally submitting on behalf of some other entity that does not correspond to the header submitter details. 
FC 3: Ingestion - Processing of Submissions 
FC.3.1: Message Validations  
Although there are significant changes to the specific validations required based on the new JFSA Re -write 
regulations, there will be no changes to the [[BASIC]] process by which messages are validated for JFSA reporting.  
The validation process includes: 
• File level Schema Validation validates that the message is formatted correctly so that it can be parsed . 
Your submission will be validated at the message level and the detail records if there are multiple records 
within a file. An example of a CRPT file level reject is an incorrect or incomplete headers . GTR would not 
validate at the record level if the file is corrupted. Examples of these scenarios are: 
(a) BizData header is missing / malformed. Refer to FC 2.3 for the header requirements that will cause a 
full file rejection. 
(b) MQ submissions containing > 1 activity (/Rpt Blocks) 
(c) sFTP submissions containing > 100k activities (/Rpt Blocks) 
The error code would be at the message status level. 
Message Status 
  
CodeName Name Definition 
ACPT Accepted Whole message has been accepted. 
CRPT CorruptedFile File containing the report is corrupted. 
 
Another example of a schema rejection occurs at the record level (trade level) For example, if an optional field 
is submitted with the XML tag but with the value as blank, the message will be schema rejected. To pass the 
schema validation, the entire XML tag must be removed for optional fields unless a value is also submitted to 
accompany the XML tag. These would be validated at each record level. 
 
Detailed Status 
  
CodeName Name Definition 
ACPT Accepted Record has been accepted. 
RJCT Rejected Record has been rejected 
 
• Permission Validation (validates that the submitter has permission to submit the message)  
• Core Validation ([[BASIC]] global validations of key fields as defined in the Message Specifications  and Usage 
Guidelines). For example, a data type of Num(31,13) allows for up to 18 numeric values prior to the 
decimal and up to 13 numeric values after but only 18 digits in total. This is equivalent to (18,13) in CDE & 
ISO XML. Assuming a submitted value is '11111111111111.1100000000000', this will be rejected as the 

---

## Page 18

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 18 
 
total is 27 digits. If the user omits the trailing zeros and submits '11111111111111.11', then it will be 
accepted. 
• Jurisdictional Validation (validations specific to each jurisdiction as defined in the Message Specifications  
and Usage Guidelines) 
 
 
The below diagram illustrates the common message validation process.  
Authorization 
(Permission)
Jurisdictional 
Validation
Schema 
Validation
Control 
Processing 
(Core Validation)
Store
NACK
ACK
1
2
3
4
5
 
Further description of the current functionality can be found on the Learning Center:  
Details of specific validations performed on each message and field are contained in the [[DTCC]] Message 
Specifications. 
FC 3.2: Message Sequencing  
There will be no changes to the way messages are processed in the GTR in terms of sequencing.  If messages 
related to the same trade are submitted in sequence within the same channel or file (MQ or sFTP or Web 
Upload), [[DTCC]] will process those messages in the order received.  Sequencing cannot be guaranteed when 
messages related to the same trade are submitted across these channels. For users who may have multiple 
connections to the same sFTP site and intend to send files in quick succession, they are recommended to use 
the same connection or otherwise wait till an acknowledgement is received before sending another file in from 
a different connection. 
With the implementation of Action Type sequencing rules (see section FC 3.8), it is especially important that 
the users consider and factor in what and when to send messages based on Action Type.  
Please note that message responses over MQ may be returned in a different sequence tha n the original 
submission due to load balancing functions in the GTR.  This does not mean that the messages have been 
processed out of sequence. 
 

---

## Page 19

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 19 
 
FC 3.3: Trade Identifiers  
A UTI is generally required for all new trades submitted for JFSA reporting after the go-live (using Action Type 
“NEWT”).  The global UTI format requirement applies to new trades that may require a temporary UTI and new 
trades that the UTI generating party generates, however, any existing trades can be submitted with the 
proprietary [[ID]] tag post go-live.  
Validations performed will be as defined in the Message Specifications. 
The USI Value without the USI Prefix on trades that are live prior to the Re-Write go-live will be migrated to the 
Proprietary [[ID]] tag. Firms may choose to upgrade their existing trade population with the UnqTxIdr or continue 
using the Prtry/[[ID]] tag post go live however please note the difference in format requirements for each tag. 
FC 3.4: Uniqueness of a Trade  
Currently, trade uniqueness is defined as follows: 
• For current JFSA reporting, the uniqueness of a trade is determined by the concatenation of USI (USI [[ID]] 
prefix + USI [[ID]] value) + Trade Party 1 ([[ID]] Type + [[ID]]) + Trade Party 2 ([[ID]] Type + [[ID]]).  For brevity, this is 
often referred to as “USI+TP1+TP2”. 
With the JFSA Re-Write implementation, trade uniqueness in the JFSA GTR will be simplified as follows:  
• For JFSA reporting, the uniqueness of a trade will be determined by the concatenation of UTI  or 
Proprietary [[ID]] + Trade Party 1 
• For brevity, the remainder of this document will use “UTI + RCP” to reference this uniqueness. 
This change will require the removal of “duplicate” trades, where trades with the same USI+TP1 exist with 
multiple different Trade Party 2 (“TP2”) parties (which were allowed under the current trade uniqueness rules).  
Users need to review their existing Position Reports for such trades and exit the appropriate trades prior to go -
live and DDRJ Operations staff will reach out to you bilaterally regarding such positions.  If this clean -up is not 
performed, [[DTCC]] will choose the most recently updated trade to carry forward and discontinue reporting of 
other duplicate trades with the same USI+TP1.   
This functionality change has implications for how users will manage changes to the counterparty of a trade 
that will be different than today.  Please see section 3.10 for further details. 
FC 3.5: [[collateral]] Message Submissions 
[[collateral]] messages will be newly introduced for JFSA reporting.   
Submissions 
• [[collateral]] submissions must minimally satisfy the auth.108.001.01_JFSAUG_DATMDA_1.0.0 xml 
schema. Failure to adhere to the schema requirements will result in the message being rejected upfront. 
For example, if the user submits a MARU action type and indicates economic fields such as Fixed Rate or 
Expiration Date, the message will be rejected. 

---

## Page 20

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 20 
 
• [[collateral]] messages must be submitted in XML format and via the o-code “0xxx”. (Details on the 
validations can be found in the Message Specifications). Message samples have also been published on 
the learning center. 
• These messages can be submitted via Web Upload, sFTP and MQ 
• [[collateral]] messages are distinguished by the Action Type value of “MARU” in the submission.  
• Submission permissions will work the same as for all other message types.  
• Validations will be performed as specified in the Message Specifications. 
Trade Level or Portfolio Level [[collateral]]  
• [[collateral]] valuation is either at Trade Level or Portfolio Level.   
• For Trade Level [[collateral]] Valuations: 
o Trade-level [[collateral]] messages must contain a UTI and will only be accepted if there is a base trade 
that matches the [[collateral]] valuation submission (UTI + RCP + OCP must match).  The base trade 
must be “Open”, “Terminated”, or “Expired.   
o Trade-level [[collateral]] messages submitted on trades that have been “Errored” (action type EROR) or 
“Transferred Out” (action type PRTO) will be rejected (NACK-ed). 
o [[collateral]] Portfolio Indicator must be “false” so that UTI can be populated.  
o One of Initial [[Margin]] [[collateral]] Portfolio Code or Variation [[Margin]] [[collateral]] Portfolio code must be 
submitted on both the auth.030 and auth.108 messages after 1 April 2024. If the [Initial [[Margin]] 
[[collateral]] portfolio code] is not applicable to a trade, clients should submit the value [NOAP] to 
represent "Not Applicable" 
• For Portfolio-level [[collateral]] Valuations: 
o Two portfolio codes are defined (Initial [[Margin]] [[collateral]] Portfolio Code & Variation [[Margin]] [[collateral]] 
Portfolio Code).  At least one of these must be populated on each [[collateral]] message if [[collateral]] 
Portfolio Indicator is “true” 
o Portfolio-level [[collateral]] messages will be validated for the existence of one or more underlying 
trades which contain the given Initial [[Margin]] [[collateral]] Portfolio Code and/or Variation [[Margin]] 
[[collateral]] Portfolio Code. 
o As JFSA requires either one of Initial [[Margin]] Portfolio Code & Variation [[Margin]] [[collateral]] Portfolio 
Code for portfolio-based [[Margin]] reporting, the ingestion validation lookup to the existence of at least 
one underlying trade will be on the basis of the concatenated value of both the portfolio codes (case-
sensitive) on the MARU message against the base trade. 
New “0” o-codes will be configured in JFSA for each user to support [[collateral]] reporting (it is not [[Asset]] -class 
aligned, so will not naturally fit with existing user O-Codes).   
[[collateral]] valuation submission information will not be merged onto the Trade State Report , but will be reported 
on a [[EOD]] [[Margin]] Submission Report, [[Margin]] Activity Report and [[Margin]] State Report.  For further information 
on [[collateral]] valuation reporting, please refer to the Reporting section of this document (FC 5 Reports).  
 
 

---

## Page 21

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 21 
 
FC 3.6: Trade Valuation Submissions 
Trade Valuation messages are applicable for JFSA reporting. 
Trade Valuations need to be submitted to the GTR daily through a Valuation message indicated by Action Type 
“VALU” 
Valuations will only be accepted if there is a base trade which matches the valuation submission (UTI + RCP + 
OCP). Any valuation submitted on a position without a base trade will be rejected (NACK -ed). 
Valuations that are submitted on inactive trades (expired or terminated) will be accepted. In this scenario the 
valuation submission will be reported as activity in the [[EOD]] Activity Report but will not be reported on Trade 
State Reports for both the regulators and participants.  
As per the Message Specifications, valuations submitted on trades that have been Errored (action type EROR) 
or Transferred Out (action type PRTO) will be rejected. (NACK-ed) 
FC 3.7: Reporting Counterparty and Entity Responsible for Reporting  
The Entity Responsible for Reporting (ERR) is newly introduced as part of the re -writes and is defined as “The 
identifier of the financial institution that has the reporting obligation”. While this is mostly the same as the 
Reporting Counterparty (RCP), there are cases for JFSA reporting where they are different (eg) The Trust 
Bank is the ERR but the fund is the RCP. The validation conditions related to trust banks are as follows based 
on the published JFSA guidelines: 
(a) If an onboarded JFSA account only has a service role of “Trust Bank”, then any submission where the 
“Trust Bank” account is indicated as the Reporting Party or Other Counterparty must be rejected. This 
means that RCP and OCP on any submission cannot have a role of only “Trust Bank” in SDO 
 
(b) The ERR and the RCP must have a valid renewed LEI in GLIEF which is validated at the point of 
submission. Both the Report Submitting Entity (RSE) and the ERR must be an active account 
onboarded in SDO for JFSA reporting. At ingestion, a validation rule will be implemented to check if 


---

## Page 22

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 22 
 
there is a permission between the RSE <-> ERR. The permission is required to be set in Manage 
Services if RSE is not the same as ERR, however this condition will not be triggered if RSE = ERR. To 
illustrate the likely scenarios, some use-case examples are provided below. 
Case Roles Explicit 
Permission 
Comments 
Case 1 Onboarded Trust Bank A = ERR & 
RSE 
Non-onboarded Fund A = CP1 
(RCP) 
No Majority use-case scenario. Even though RCP is not 
onboarded, this is considered self-reporting, hence 
permission is not needed.  
Case 2 Onboarded Trust Bank B = RSE 
Onboarded Trust Bank A = ERR 
Non-onboarded Fund A = CP1 
(RCP) 
Yes Trust Bank B effectively acts as a third-party submitter 
and needs to request Permission to submit for Trust Bank 
A as ERR. 
Trust Bank A will need to approve the request in Manage 
Services 
 
(c) A third-party service provider cannot be named as the Reporting Counterparty in all submissions. Such 
submissions regardless of Action Type will be NACK-ed.  
FC 3.8: Action Type and Event Type Validations  
Submissions received after go-live must contain the relevant “Action Type” and “Event Type” values.  These 
values must pass both “stateless” validations (i.e. validations that can be performed solely based on the 
content of the message) as well as “stateful” validations (i.e. validations that can only be performed by 
referencing previous submissions for the same trade).  
“Stateless” Validations 
These validations restrict the valid combinations of the “Action Type”, and “Event Type” fields.  The Message 
Specifications contain a tab called “Action type & Event type,” which details the valid combinations of these 
fields for all messages.  As these combinations can be validated solely based on content of the message, they 
can be tested using the Simulator.   
“Stateful” Validations 
These validations control the allowable sequences of Action Types.  Each new submission will be validated to 
confirm that the action type is consistent with the allowable sequence as per the action type state diagrams 
below.  These validations will be performed per unique trade (see trade uniqueness section 3.4) + per 
Jurisdiction.  The latest version of these diagrams will always be contained in the Message Specifications. 
Some main points are described below. Note that JFSA will follow the ESMA approach for consistency. 
• The first submission for a trade must be NEWT.  
• No submission is required to Expire a trade.  An end-of-day process will remove expired trades from the 
Trade State Report (TSR) on the day of expiration (as it does currently for JFSA reporting).   In the state 
diagram below, this process will logically move trades from “Outstanding” to “Termi nated” status. A TERM 
submission will be validated on the basis of an existing base trade with the same UTI+RCP+OCP  

---

## Page 23

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 23 
 
• MODI, CORR, VALU, and MARU submissions to terminated trades are allowed. This is to allow reporting 
entities to submit historical modifications, corrections, valuations and [[collateral]] information for terminated 
trades. Submitters are responsible for ensuring relevant dates are accurate and information submitted is 
correct. Another example is that if the TERM has an event timestamp prior to the event timestamp of the 
previously successfully submitted event, the status of the trade will be taken from the TERM even though 
the event timestamp is earlier. This is because we systematically are unable to tell which of the event was 
incorrectly submitted. Maintaining as TERM would allow the reporting entity to make subsequent 
corrections as necessary through a MODI, CORR or REVI as required. Trade linkage for MODI and 
CORR will be on the basis of UTI + RCP. 
• There would not be any validation on the data fields being submitted and its possible that OCP could be 
changed on a terminated trade prior to submitting a REVI. However on the REVI submission, the OCP 
cannot be amended and it would be necessary to submit the latest accepted OCP. All other fields are 
allowed to be amended on the REVI as long as they are applicable as indicated on the message 
specifications.   
• When a trade is successfully submitted for a TERM, EROR, or PRTO, it will not appear on  the Trade State 
Report on the same day of the corresponding submission.  Once a trade status Terminated or Errored, the 
only way for it to appear again on the TSR is to submit a REVI message  with a future expiration date. 
TERM, EROR and PRTO will be validated for an existing position on the basis of UTI + RCP + OCP. 
• To REVI the trade, the same UTI+RCP+OCP must be submitted, and we will check for an existing 
UTI+RCP+OCP. A REVI with a future expiration date on a terminated or errored status will bring the trade 
status to “Outstanding” while a REVI with past expiration date keeps the status as “Terminated”. REVI 
allows reporting counterparties to modify or correct the Early Termination Date  
• Firms can submit MODI or CORR to change other fields thereafter including OCP 
• VALU and MARU linkage to the base trade position will be on the basis of UTI + RCP + OCP 
• [[Margin]] Update linkage to the derivative that was reported depends on how the derivative is collateralized:  
(a) If the trade is not collateralized as part of a portfolio (derivative based) – the submission will have UTI 
and so linkage is UTI + RCP + OCP. If there is no base trade, then the MARU must be rejected 
(b) If the trade is collateralized as part of a portfolio, the submission will have Initial and/or Variation 
[[Margin]] [[collateral]] portfolio Codes so the linkage is Initial and/or Variation [[Margin]] [[collateral]] Portfolio 
Codes + RCP + OCP. There must be at least one existing UTI in the portfolio for the MARU message 
to be accepted. 
Note that the linking does not refer to actual linking of the [[Margin]] values to the Trade State Report but 
guidance for how you perform reconciliations from the [[Margin]] State Reports to the Trade State Report 
• Unique to JFSA, the regulations provide a threshold for mandatory reporting parties who has more than 
JPY 300 billion average notional combining FX and IR only between the beginning of April to end March 
fiscal year, and only the firms above this threshold need to report for one year starting from July each 
year. If firms fall below the threshold, they are not required to report but they need to submit a letter to 
JFSA and DDRJ. DDRJ will continue to bill for account management fees and position fees until the firms 
exit the positions from GTR if they fall below the reporting threshold. If the firm falls below threshold, they 
are required to submit a written document (they will stop reporting) in Japanese to JFSA and DDRJ and 
will be required to submit Action type=PRTO (Transfer out) and Event type =PTNG (Transfer) to exit the 
positions. Should the firm go above threshold in subsequent years, then firms can submit the same UTI 
with Action Type: NEWT and any applicable Event Type since we are unable to distinguish newly 

---

## Page 24

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 24 
 
reportable transactions vs re-reported transactions that become in scope because of the firm going above 
threshold.  
 
 
 
Some use case examples are provided below.  
 
Scenario Sub# Action 
Type 
Event 
Type UTI RCP OCP [[Margin]] Portfolio  
(Initial/Variation) Validation Expected 
Result Comments 
UC1 
1 NEWT TRAD 123 Bank 
A 
Bank 
B 
NA UTI+RCP ACK   
2 MODI TRAD 123 Bank 
A 
Bank 
B 
NA UTI+RCP ACK Post Trade for 
the same UTI 
and OCP 
should ACK as 
linking is by 
UTI+RCP 
UC2 
1 NEWT TRAD 123 Bank 
A 
Bank 
B 
NA UTI+RCP ACK   
2 MODI TRAD 123 Bank 
A 
Bank 
C 
NA UTI+RCP ACK Post Trade for 
the same UTI 
even if OCP is 


---

## Page 25

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 25 
 
different it 
should ACK as 
linking is by 
UTI+RCP 
UC3 
1 NEWT TRAD 123 Bank 
A 
Bank 
B 
NA UTI+RCP ACK   
2 MODI TRAD 123 Bank 
B 
Bank 
A 
NA UTI+RCP NACK Post Trade 
cannot be 
submitted 
without a base 
trade 
UC4 
1 NEWT TRAD 123 Bank 
A 
Bank 
B 
NA    UTI+RCP ACK   
2 TERM ETRM 123 Bank 
A 
Bank 
B 
NA UTI+RCP+OCP ACK Post Trade for 
the same UTI 
and OCP 
should ACK as 
linking is by 
UTI+RCP+OCP 
3 REVI* NA 123 Bank 
A 
Bank 
B 
NA UTI+RCP+OCP ACK Post Trade for 
the same UTI 
and OCP 
should ACK as 
linking is by 
UTI+RCP+OCP 
UC5 
1 NEWT TRAD 123 Bank 
A 
Bank 
B 
NA UTI+RCP ACK   
2 TERM ETRM 123 Bank 
A 
Bank 
B 
NA UTI+RCP+OCP ACK   
3 REVI* NA 123 Bank 
A 
Bank 
C 
NA UTI+RCP+OCP NACK Post Trade for 
the same UTI 
even if OCP is 
different it 
should NACK 
as linking is by 
UTI+RCP+OCP 
UC6 
1 NEWT TRAD 123 Bank 
A 
Bank 
B 
NA UTI+RCP ACK   
2 TERM ETRM 123 Bank 
A 
Bank 
B 
NA UTI+RCP+OCP ACK   
3 REVI* NA 123 Bank 
B 
Bank 
A 
NA UTI+RCP+OCP NACK Post Trade 
cannot be 
submitted 
without a base 
trade 
 
JFSA will primarily follow what was consulted in the CDE Consult published in August 2022, which states the 
following definitions 
 
 
 
 
 
 
 
 

---

## Page 26

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 26 
 
Action type Allowable 
value 
Details to be reported 
New NEWT The creation of the first transaction resulting in the generation of a new UTI. 
Modify MODI A modification of the terms of a previously reported transaction due to a newly 
negotiated modification (amendment) or a filling in of previously missing 
information (e.g., post price transaction). It does not include correction of a 
previously reported transaction. 
Correct CORR A correction of erroneous data of a previously reported transaction. 
Terminate TERM A termination of an existing transaction. 
Error EROR A cancellation of a wrongly submitted entire transaction in case it never came 
into existence or was not subject to the reporting requirements under the 
applicable law of a given jurisdiction, or a cancellation of a duplicate report. 
Revive REVI An action that reinstates a reported transaction that was reported with action type 
“Error” or terminated by mistake or expired due to an incorrectly reported 
Expiration date. 
Valuation VALU An update of a valuation of a transaction. There will be no corresponding Event 
type. 
[[collateral]] or 
[[Margin]] update 
MARU An update to [[collateral]] [[Margin]] data. There will be no corresponding Event type.  
Transfer out PRTO A transfer of a transaction from one trade repository to another trade repository 
(change of trade repository). 
 
Event type Allowable 
value 
Details to be reported 
Trade TRAD A creation or modification of a transaction. 
[[Novation]] NOVA 
A [[Novation]] legally moves partial or all of the financial risks of a swap 
from a transferor to a transferee and has the effect of 
terminating/modifying the original transaction and creating a new 
transaction to identify the exposure between the transferor/transferee and 
remaining party. 
Compression COMP 
Compressions and risk reduction exercises generally have the effect of 
terminating or modifying (i.e., reducing the notional value) a set of 
existing transactions and of creating a set of new transaction(s). These 

---

## Page 27

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 27 
 
processes result in largely the same exposure of market risk that existed 
prior to the event for the counterparty. 
Early 
Termination ETRM Termination of an existing swap transaction prior to scheduled 
termination or maturity date. 
Clearing CLRG 
Central clearing is a process where a [[Derivatives]] clearing organization 
interposes itself between counterparties to contracts, becoming the [[Buyer]] 
to every [[Seller]] and the [[Seller]] to every [[Buyer]]. It has the effect of 
terminating an existing transaction between the [[Buyer]] and the [[Seller]] and 
thereby ensuring the performance of open contracts. 
Clearing & 
Allocation CLAL A simultaneous clearing and allocation event in a [[Derivatives]] clearing 
organization 
Exercise EXER The process by which a counterparty fully or partially exercises their 
rights specified in the contract of an [[Option]] or a swaption. 
Allocation ALOC 
The process by which an agent, having facilitated a single swap 
transaction on behalf of several clients, allocates a portion of the executed 
swap to the clients 
Credit Event CREV 
An event or trigger that results in the termination or modification of the 
state of a previously submitted credit derivative transaction. Applies only 
to credit [[Derivatives]]. 
Corporate 
Event CORP A corporate action on [[Equity]] underlying that impacts the transactions on 
that [[Equity]]. 
Transfer PTNG 
The process by which a swap is transferred to another SDR that has the 
effect of the closing of the swap transaction at one SDR or opening of the 
same swap transaction using the same UTI/USI in a different SDR (new). 
Upgrade UPDT An upgrade of an outstanding transaction performed in order to ensure its 
conformity with the amended reporting requirements. 
 
For trades that are already “live” when the JFSA Rules Rewrite is implemented, [[DTCC]] will initialize the state of 
the trade during go-live weekend, such that post go-live submissions will be accepted according to these action 
type validations.  This logic is described further in Section 6 of this document.  
FC 3.9: Submissions with Reduced Validations  
After the JFSA Rules Rewrite, some submissions (with action type = TERM, EROR, PRTO) will continue to have 
reduced validations.  While these action types use the same schema for validation as submissions with Action 
type = NEWT or MODI, the message does not undergo the sa me validation for several fields. Details are 
contained in the Message Specifications.   

---

## Page 28

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 28 
 
FC 3.10: Change of Counterparty 
In the current JFSA GTR application, given the USI+CP1+CP2 trade uniqueness, a trade must be exited and 
resubmitted to change the Counterparty (Trade Party 2) on the trade.   This resubmission is allowed to retain 
the original USI in the current application. 
• Note that JFSA would allow users to submit an EROR followed by a NEWT (with a new UTI) to correct a 
mis-reported TP2 though there will be no validation check that the UTI reported is unique. 
• With the change to Trade Uniqueness as part of the re-writes, both submissions with either Action Type of 
MODI or CORR with different TP2 from the NEWT submission) will be possible.  
Please see examples below: 
 
Use 
Case 1 
                
Sub# Action 
Type 
Event 
Type 
UTI Submitted 
For 
Party 1 
(RCP) 
Party 2 
(OCP) 
Expected 
Result 
 Comments 
1 NEWT TRAD 123 Bank A Bank A Bank B ACK   
2 NEWT TRAD 123 Bank B Bank B Bank A ACK GTR does not reject if the same  
UTI is used by two or more  
different RCPs 
3 MODI TRAD 123 Bank A Bank A Bank C ACK Change of OCP allowed with  
same UTI+RCP 
4 NEWT TRAD 123 Bank B Bank B Bank A NACK NEWT already exists for  
UTI+RCP and submission  
#2 and #4 are the same, so 
two consecutive NEWTs are  
not allowed 
 
 
Use Case 
2 
                
Sub# Action 
Type 
Event 
Type 
UTI Submitted 
For 
Party 1 
(RCP) 
Party 2 
(OCP) 
Expected 
Result 
 Comments 
1 NEWT TRAD 123 Bank A Bank A Bank B ACK   
2 TERM NOVA 123 Bank A Bank A Bank B ACK   
3 TERM NOVA 123 Bank A Bank A Bank B NACK Termination cannot occur 
because trade is no 
longer active 

---

## Page 29

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 29 
 
Use Case 
2 
                
4 NEWT TRAD 123 Bank A Bank A Bank B NACK UTI Technical Guidance 
states UTI cannot be re-
used, which JFSA will 
follow 
FC 3.11: Change of Reporting Counterparty 
In the current JFSA application and the future post re-writes application, a trade must be exited and 
resubmitted to change the Reporting Party (Trade Party 1) on the trade. This resubmission is allowed to retain 
the original trade identifiers (UTI).   
Use 
Case 3 
                
Sub# Action Type Event 
Type 
UTI Submitted 
For 
Party 1 
(RCP) 
Party 2 
(OCP) 
Expected 
Result 
 Comments 
1 NEWT TRAD 123 Bank A Bank A Bank B ACK   
2 TERM/EROR - 123 Bank A Bank A Bank B ACK   
3 NEWT TRAD 123 Bank C Bank C Bank B ACK UTI Technical Guidance states UTI 
cannot be re-used, which JFSA will 
follow, however #3 is allowed as the 
UTI+RCP combination is unique. 
 

---

## Page 30

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 30 
 
FC 3.12: JFSA Usage Guidelines 
JFSA requires 3 of the 4 message types excluding Real-Time messages 
(a) Transaction – auth.030.001.03_JFSAUG_DATTAR_1.0.0 
(b) Valuation – auth.030.001.03_JFSAUG_DATTAR_1.0.0 
(c) [[collateral]] – auth.108.001.01_JFSAUG_DATMDA_1.0.0 
While the transaction and valuation messages share the same ingestion schema, the intent of the usage 
guidelines is to define restrictions that will tighten the fields being submitted. For example, a valuation 
action type should in theory only contain valuation related fields even though it would be possible to 
submit other economic fields that are in the baseline auth.030.001.03.xsd schema. The usage guidelines 
are meant to address this gap. 
The UG is built through the MyStandards portal via SWIFT. [[DTCC]] upon agreement with JFSA would own 
the publication and maintenance of the UG. Additionally, the PDF and/or excel version could be provided 
along with the XSD for users of the system and distributed to DDRJ users outside of SWIFT in order to 
minimize users requesting permission to access the usage guidelines via MyStandards. Additionally, the 
JFSA UG will be setup as private in the MyStandards portal and [[DTCC]] can invite and approve viewers 
and users of the JFSA UG 
The usage guidelines will cover: 
(a) Mandatory field validation by action type where the ISO baseline schema is optional.  
(b) Tighter enumerations than the ISO baseline schema.  
(c)Tighter format restrictions than the ISO baseline schema 
(d) Any not applicable fields classified by action type for JFSA. The fields which are not applicable for 
JFSA by each action type and if they are submitted by a firm, they will receive a rejection response 
for invalid schema based on the Usage Guidelines 
To assist users, [[DTCC]] sample messages have been published in the Learning Centre. 
FC 3.13: Introduction of an Aggregated O-Code 
Starting with the rewrites, clients can choose whether to consolidate all core [[Asset]] classes under 8ABC or 
continue with their existing [[Asset]] class level segregation (ie) 2 = CO, 3 = Credit etc. 8ABC offers an 
aggregate of all [[OTC]] Core, including data submitted under the 2-6 o-codes. This is not mandatory, and 
clients can choose what makes sense for them. Utilizing 8ABC will enable firms to consolidate all their 
[[OTC]] submissions into a single report agnostic of [[Asset]] class. 0ABC will remain for [[Margin]] reporting. This 
functionality is expected to be available in late Q1 2024 for UAT as it is not on the critical path as a 
regulatory deliverable.  
  

---

## Page 31

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 31 
 
FC 3.14 Other Payment Fields 
For the JFSA rewrite, we have 6 data fields to capture information relating to Other Payments. These 
fields are listed below. 
1. Other payment amount 
2. Other payment type 
3. Other payment currency 
4. Other payment date 
5. Other payment payer 
6. Other payment receiver 
 
These fields accept multiple values and there are validation rules applied to ensure the number of values 
populated in each field are consistently reported. E.g, if multiple values are reported, the number of Other 
payment amount, Other payment type, Other payment currency, Other payment date, Other payment 
payer and Other payment receiver must be the same, otherwise the submission will be rejected. Please 
refer to business rules in the Message Specification for details. 
From a CSV reporting perspective, the following fields forms the unique key for determining how the other 
payments fields are displayed on the end of day Trade State Reports (TSR). 
Other Payment Uniqueness Key: 
1. Other payment type 
2. Other payment date 
3. Other payment payer 
4. Other payment receiver 
 
Based on the Other Payment uniqueness key: 
a) For submissions with the same unique key, the latest values are stored for under the latest Event 
Timestamp approach. 
b) For submissions where there is a change to the unique key, the values from this submission will 
be cumulated and appended to respective fields on the Trade State Report. 
For example: If a Payment Type of UFRO was submitted on a NEWT, and subsequently a PEXH 
is submitted on a MODI action type, as there is a change in one of the 4 fields which determines 
the Other Payment Uniqueness Key, the PEXH details on this second submission will be 
added to details reported on the NEWT in the TSR (represented as separate additional values 
semi-colon separate.) instead of over writing the values in the NEWT submission. 
c) The [Action Type] of CORR can be used to correct the details of other payment data previously 
reported or to indicate that the amount with the applicable combination shouldn’t have been 
reported previously by reporting with other payment amount = 0.  
See details in the Other Payments table below for examples. 
 

---

## Page 32

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 32 
 
 
Sub 
No: 
Inbound Submission via XML Outbound CSV Report Display of Values. 
Comments Action 
Type 
Other 
payment 
type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date* 
Other 
payment 
type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
1 NEWT UFRO LEI123 LEI456 GBP 100 2023-02-20 UFRO LEI123 LEI456 GBP 100 2023-02-20 
New trade submitted with Other Payment 
Fields populated.  
Display values submitted. 
2 MODI UFRO LEI123 LEI456 USD 100 2023-02-20 UFRO LEI123 LEI456 USD 100 2023-02-20 
The Other Payment uniqueness key - [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] have been submitted with the 
same values. 
For same combination of [Other Payment 
Type] & [Other payment date] & [Other 
payment payer] & [Other payment receiver], 
the values from the latest submission will be 
displayed. 
3 MODI UFRO LEI123 LEI456 GBP 100 2023-03-20 UFRO 
UFRO 
LEI123 
LEI123 
LEI456 
LEI456 
USD 
GBP 
100 
100 
2023-02-20 
2023-03-20  
The Other Payment uniqueness key - [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] have been changed as the  
[Other payment date] was updated. 
For the different combination of [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] fields, the values will be appended 
on to the report.  
4 MODI UFRO LEI123 LEI456 USD 100 2023-03-20 UFRO; 
URFO 
LEI123; 
LEI123 
LEI456; 
LEI456 
USD; 
USD 
100; 
100 
2023-02-20; 
2023-03-20 
The Other Payment uniqueness key - [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] exists so the latest USD other 
payment currency would be updated for that 
key. 
For the different combination of [Other 
Payment Type] & [Other payment currency] 
& [Other payment payer] & [Other payment 
receiver] fields, the values will be appended 
on to the report. 

---

## Page 33

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 33 
 
Sub 
No: 
Inbound Submission via XML Outbound CSV Report Display of Values. 
Comments Action 
Type 
Other 
payment 
type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date* 
Other 
payment 
type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
5 MODI UFRO LEI123 LEI456 USD 300 2023-03-20 UFRO; 
URFO 
LEI123; 
LEI123 
LEI456; 
LEI456 
USD; 
USD 
100; 
300 
2023-02-20; 
2023-03-20 
On one the previous combination of [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] have been submitted with the 
same values. 
Only the [Other payment amount] was 
updated. 
For same combination of [Other Payment 
Type] & [Other payment date] & [Other 
payment payer] & [Other payment receiver], 
the values from the latest submission will be 
displayed. 
6 MODI PEXH LEI123 LEI456 USD 500 2023-04-20 
UFRO; 
URFO; 
PEXH 
LEI123; 
LEI123; 
LEI123 
LEI456; 
LEI456; 
LEI456 
USD; 
USD; 
USD 
100; 
300; 
500 
2023-02-20; 
2023-03-20; 
2023-04-20 
The Other Payment uniqueness key - [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] has changed as the [Other payment 
Type] was updated. 
For the different combination of [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] fields, the values will be appended 
on to the report. 
7 MODI PEXH; 
PEXH 
LEI123; 
LEI456 
LEI456; 
LEI123 
USD; 
GBP 
500; 
160 
2023-04-
20; 
2023-05-20 
UFRO; 
URFO; 
PEXH; 
PEXH 
LEI123; 
LEI123; 
LEI123; 
LEI456 
LEI456; 
LEI456; 
LEI456; 
LEI123 
USD; 
USD; 
USD; 
GBP 
100; 
300; 
500; 
160 
2023-02-20; 
2023-03-20; 
2023-04-20; 
2023-05-20 
The combination of [Other Payment Type] & 
[Other payment date] & [Other payment 
payer] & [Other payment receiver] has 
changed as additional [Other payment date] 
was submitted. 
For the different combination of [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] fields, the values will be appended 
on to the report.  

---

## Page 34

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 34 
 
Sub 
No: 
Inbound Submission via XML Outbound CSV Report Display of Values. 
Comments Action 
Type 
Other 
payment 
type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date* 
Other 
payment 
type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
8 MODI PEXH; 
PEXH 
LEI123; 
LEI456 
LEI456; 
LEI123 USD;GBP 400;320 
2023-04-
20; 
2023-05-20 
UFRO; 
URFO; 
PEXH; 
PEXH 
LEI123; 
LEI123; 
LEI123; 
LEI456 
LEI456; 
LEI456; 
LEI456; 
LEI123 
USD; 
USD; 
USD; 
GBP 
100; 
300; 
400; 
320 
2023-02-20; 
2023-03-20; 
2023-04-20; 
2023-05-20 
On one the previous combination of [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] have been submitted with the 
same values.  
Only the [Other payment amount] was 
updated. 
For same combination of [Other Payment 
Type] & [Other payment date] & [Other 
payment payer] & [Other payment receiver], 
the values from the latest submission will be 
displayed. 
9 MODI UWIN LEI456 LEI123 USD 100 2023-04-18 
UFRO; 
URFO; 
PEXH; 
PEXH; 
UWIN 
LEI123; 
LEI123; 
LEI123; 
LEI456; 
LEI456 
LEI456; 
LEI456; 
LEI456; 
LEI123; 
LEI123 
USD; 
USD; 
USD; 
GBP; 
USD 
100; 
300; 
400; 
320; 
100 
2023-02-20; 
2023-03-20; 
2023-04-20; 
2023-05-20; 
2023-04-18 
A new [Other Payment Type] - value 'UWIN' 
is submitted. 
For the different combination of [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] fields, the values will be appended 
on to the report. 
 
*Note 'UWIN' can be interpreted as a 
historical correction on [Other Payment 
Type] as 'UWIN' indicates this trade is fully 
terminated when the value 'UWIN' is 
submitted (2023-04-18). 
10 MODI UFRO LEI456 LEI123 USD 300 2023-03-20 
UFRO; 
URFO; 
PEXH; 
PEXH; 
UWIN; 
UFRO 
LEI123; 
LEI123; 
LEI123; 
LEI456; 
LEI456; 
LEI456 
LEI456; 
LEI456; 
LEI456; 
LEI123; 
LEI123; 
LEI123 
USD; 
USD; 
USD; 
GBP; 
USD; 
USD 
100; 
300; 
400; 
320; 
100; 
300 
2023-02-20; 
2023-03-20; 
2023-04-20; 
2023-05-20; 
2023-04-18; 
2023-03-20 
The Other Payment uniqueness key - [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] has changed as the Other payment 
payer] & [Other payment receiver] was 
updated. 
For the different combination of [Other 
Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment 
receiver] fields, the values will be appended 
on to the report. 

---

## Page 35

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 35 
 
Sub 
No: 
Inbound Submission via XML Outbound CSV Report Display of Values. 
Comments Action 
Type 
Other 
payment 
type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date* 
Other 
payment 
type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
11 CORR UFRO LEI456 LEI123 USD 0 2023-03-20 
UFRO; 
URFO; 
PEXH; 
PEXH; 
UWIN; 
UFRO 
LEI123; 
LEI123; 
LEI123; 
LEI456; 
LEI456; 
LEI456 
LEI456; 
LEI456; 
LEI456; 
LEI123; 
LEI123; 
LEI123 
USD; 
USD; 
USD; 
GBP; 
USD; 
USD 
100; 
300; 
400; 
320; 
100; 
0 
2023-02-20; 
2023-03-20; 
2023-04-20; 
2023-05-20; 
2023-04-18; 
2023-03-20 
To indicate that the amount for the 
applicable combination shouldn’t have been 
reported previously, use Action Type =CORR 
and submit the other payment amount as 
zero '0' for the applicable combination. 
 
 
*The Other Payment uniqueness key is combination of [Other Payment Type] & [Other payment date] & [Other payment payer] & [Other payment 
receiver]. 

---

## Page 36

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 36 
 
FC 3.15 Schedule Fields 
For the JFSA rewrite, we have 6 set of Schedule fields listed below. 
 
1. Price schedule 
2. Strike price schedule 
3. Notional amount schedule - Leg 1 
4. Notional amount schedule - Leg 2 
5. Notional quantity schedule - Leg 1 
6. Notional quantity schedule - Leg 2 
 
Each of these schedules have 3 related data fields, an Effective Date, an End Date, and the Value in effect between the Effective date and End date. 
From a CSV reporting perspective, if a schedule is submitted in your XML message, we will use the Value within that schedule as primary value to update 
the related jurisdiction field. Please see the table below for the fields used. 
 
 
Schedules Jurisdictional Field Schedules values Reporting Logic in CSV 
Price schedule 
Price Reported Value or derived from 
Schedule where applicable. 
1. If [Price schedules - Price in effect between the unadjusted 
effective date and unadjusted end date inclusive] is populated, 
report the value of the price from the Price schedule between the 
indicated Effective dates and End dates. 
2. If there is NO End date given, continue to report the value of the 
price in the schedule from the Effective date. 
3. Where the different schedule dates are not given continuously, 
report the value in the [Price] field until the Effective Date of the next 
schedule. (If the value is blank, report blank.) 
Price schedules - Price in effect between the 
unadjusted effective date and unadjusted end date 
inclusive 
Value from Schedule 
Schedule fields: Report values as submitted. Price schedules - Unadjusted effective date of the 
price Effective date from Schedule 
Price schedules - Unadjusted end date of the price End Date from Schedule 
Strike price 
schedule Strike Price Reported Value or derived from 
Schedule where applicable. 
1. If [Strike price schedules - Strike price in effect between the 
unadjusted effective date and unadjusted end date inclusive] is 
populated, report the current value of the strike price from the Strike 
Price schedule between the indicated Effective dates and End 
dates. 

---

## Page 37

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 37 
 
Schedules Jurisdictional Field Schedules values Reporting Logic in CSV 
2. If there is NO End date given, continue to report the value of the 
strike price in the schedule from the Effective date. 
3. Where the different schedule dates are not given continously, 
report the value in the [Strike Price] field until the Effective Date of 
the next schedule. 
Strike price schedules - Strike price in effect between 
the unadjusted effective date and unadjusted end 
date inclusive. 
Value from Schedule 
Schedule fields: Report values as submitted. Strike price schedules - Unadjusted effective date of 
the strike price Effective date from Schedule 
Strike price schedules - Unadjusted end date of the 
strike price End Date from Schedule 
Notional amount 
schedule - Leg 1 
Notional amount of leg 1 Reported Value or derived from 
Schedule where applicable. 
1. If [Notional amount schedule - notional amount in effect on 
associated effective date of leg 1] is populated, report the current 
value of the Notional amount from the Notional amount Leg 1 
schedule between the indicated Effective dates and End dates. 
2. If there is NO End date given, continue to report the value of the 
notional amount of leg 1 in the schedule from the Effective date. 
3. Where the different schedule dates are not given continously, 
report the value in the [Notional amount of leg 1] field until the 
Effective Date of the next schedule. 
Notional amount schedule - notional amount in effect 
on associated effective date of leg 1 Value from Schedule 
Schedule fields: Report values as submitted. Notional amount schedule - unadjusted effective date 
of the notional amount of leg 1 Effective date from Schedule 
Notional amount schedule - unadjusted end date of 
the notional amount of leg 1 End Date from Schedule 
Notional amount 
schedule - Leg 2 
Notional amount of leg 2 Reported Value or derived from 
Schedule where applicable. 
1. If [Notional amount schedule - notional amount in effect on 
associated effective date of leg 2] is populated, report the current 
value of the Notional amount from the Notional amount Leg 2 
schedule between the indicated Effective dates and End dates. 
2. If there is NO End date given, continue to report the value of the 
notional amount of leg 2 in the schedule from the Effective date. 
3. Where the different schedule dates are not given continuously, 
report the value in the [Notional amount of leg 2] field until the 
Effective Date of the next schedule. (If the value is blank, report 
blank.) 
Notional amount schedule - notional amount in effect 
on associated effective date of leg 2 Value from Schedule 
Schedule fields: Report values as submitted. Notional amount schedule - unadjusted effective date 
of the notional amount of leg 2 Effective date from Schedule 
Notional amount schedule - unadjusted end date of 
the notional amount of leg 2 End Date from Schedule 

---

## Page 38

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 38 
 
Schedules Jurisdictional Field Schedules values Reporting Logic in CSV 
Notional quantity 
schedule - Leg 1 
CDE-Total notional quantity of leg 1 Reported Value or derived from 
Schedule where applicable. 
1. If [Notional quantity schedules - Notional quantity which becomes 
effective on the associated unadjusted effective date of leg 1] is 
populated, report the current value of the Notional quantity from the 
Notional Quantity Leg 1 schedule between the indicated Effective 
dates and End dates. 
2. If there is NO End date given, continue to report the value of the 
notional quantity of leg 1 in the schedule from the Effective date. 
3. Where the different schedule dates are not given continuously, 
report the value in the [Total notional quantity of leg 1] field until the 
Effective Date of the next schedule. (If the value is blank, report 
blank.) 
Notional quantity schedules - Notional quantity which 
becomes effective on the associated unadjusted 
effective date of leg 1 
Value from Schedule 
Schedule fields: Report values as submitted. Notional quantity schedules - Unadjusted date on 
which the associated notional quantity becomes 
effective of leg 1 
Effective date from Schedule 
Notional quantity schedules - Unadjusted end date of 
the notional quantity of leg 1 End Date from Schedule 
Notional quantity 
schedule - Leg 2 
CDE-Total notional quantity of leg 2 Reported Value or derived from 
Schedule where applicable. 
1. If [Notional quantity schedules - Notional quantity which becomes 
effective on the associated unadjusted effective date of leg 2] is 
populated, report the current value of the Notional quantity from the 
Notional Quantity Leg 2 schedule between the indicated Effective 
dates and End dates. 
2. If there is NO End date given, continue to report the value of the 
notional quantity of leg 2 in the schedule from the Effective date. 
3. Where the different schedule dates are not given continuously, 
report the value in the [Total notional quantity of leg 2] field until the 
Effective Date of the next schedule. (If the value is blank, report 
blank.) 
Notional quantity schedules - Notional quantity which 
becomes effective on the associated unadjusted 
effective date of leg 2 
Value from Schedule 
Schedule fields: Report values as submitted. Notional quantity schedules - Unadjusted date on 
which the associated notional quantity becomes 
effective of leg 2 
Effective date from Schedule 
Notional quantity schedules - Unadjusted end date of 
the notional quantity of leg 2 End Date from Schedule 

---

## Page 39

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 39 
 
The schedule fields accept multiple values. Validation rules applied to ensure the values populated in each 
field are consistently and logically reported. Submission will be rejected if the rules are not adhered to. 
1. For each set of schedules, we will reject the submission if the number of Values and Effective dates 
submitted does not match. E.g. If the number of [Price schedules - Price in effect between the unadjusted 
effective date and unadjusted end date inclusive] fields and the number of [Price schedules - Unadjusted 
effective date of the price] fields are not the same. 
2. The End date for each schedule is optional, but if it is populated, we will reject the submission if the 
number of Values, Effective date and End date values does not match 
3. The Effective dates submitted must be in sequential order. 
4. The Effective dates submitted cannot be smaller than the End Dates of the previous payment schedule. 
5. The End dates submitted must be in sequential order. 
 
Examples are acceptable and rejected values are illustrated in the tables below: 
Case 1 
 
XML 
Block Field Value Expected behaviour 
1 Unadjusted effective date of the price 2023-09-01 
Accepted 
Unadjusted end date of the price 2023-09-30 
Price in effect between the unadjusted effective and end date 9000 
2 Unadjusted effective date of the price 2023-10-01 
Unadjusted end date of the price 2023-10-31 
Price in effect between the unadjusted effective and end date 8000 
3 Unadjusted effective date of the price 2023-11-01 
Unadjusted end date of the price 2023-11-30 
Price in effect between the unadjusted effective and end date 7000 
  

---

## Page 40

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 40 
 
 Case 2       
Block Field Value Expected behaviour 
1 
Unadjusted effective date of the price 2023-11-01 
Rejected – The blocks are not arranged 
in sequential order - from earliest date 
range to latest date range. 
Unadjusted end date of the price 2023-11-30 
Price in effect between the unadjusted effective and end date 9000 
2 
Unadjusted effective date of the price 2023-09-01 
Unadjusted end date of the price 2023-09-30 
Price in effect between the unadjusted effective and end date 8000 
3 
Unadjusted effective date of the price 2023-10-01 
Unadjusted end date of the price 2023-10-31 
Price in effect between the unadjusted effective and end date 7000 
  
Case 3       
Block Field Value Expected behaviour 
1 
Unadjusted effective date of the price 2023-09-01 
Rejected – Block 2's start date overlaps 
with Block 1's end date. 
Unadjusted end date of the price 2023-09-30 
Price in effect between the unadjusted effective and end date 9000 
2 
Unadjusted effective date of the price 2023-09-30 
Unadjusted end date of the price 2023-10-31 
Price in effect between the unadjusted effective and end date 8000 
3 
Unadjusted effective date of the price 2023-11-01 
Unadjusted end date of the price 2023-11-30 
Price in effect between the unadjusted effective and end date 7000 
  
 Case 4   
Block Field Value Expected behaviour 
1 Unadjusted effective date of the price 2023-09-01 
Accepted – End date can be blank. 
Unadjusted end date of the price Blank 
Price in effect between the unadjusted effective and end date 9000 
2 Unadjusted effective date of the price 2023-10-01 
Unadjusted end date of the price Blank 
Price in effect between the unadjusted effective and end date 8000 
3 Unadjusted effective date of the price 2023-11-01 
Unadjusted end date of the price Blank 
Price in effect between the unadjusted effective and end date 7000 
 

---

## Page 41

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 41 
 
Case 5 
Block Field Value Expected behaviour 
1 
Unadjusted effective date of the price 2023-11-01 
Rejected - Blocks are not arranged in 
chronological order from earliest date 
range to latest date range 
Unadjusted end date of the price Blank 
Price in effect between the unadjusted effective and end date 9000 
2 
Unadjusted effective date of the price 2023-09-01 
Unadjusted end date of the price Blank 
Price in effect between the unadjusted effective and end date 8000 
3 
Unadjusted effective date of the price 2023-10-01 
Unadjusted end date of the price Blank 
Price in effect between the unadjusted effective and end date 7000 
 
 
Assuming today’s report date is 2023-10-16, then the values will be reported in the TSR CSV Reports as 
below. 
Unique 
transaction 
identifier 
RCP OCP Price 
Price in effect between 
the unadjusted effective 
date and end date  
(Price schedule) 
Unadjusted effective 
date of the price (Price 
schedule) 
Unadjusted end date of the 
price  
(Price schedule) 
UTI1 LEI1 LEI2 8000 9000;8000;7000 
2023-09-01;2023-10-
01; 
2023-11-01 
2023-09-30;2023-10-31; 
2023-11-30 
 
Note: As part of the XML schema, the related “notation” or “currency” tags must be provided as part of the 
schedule XML block. However, these values submitted in as part of the schedule will not be used to derive the 
values in the separate notation or currency fields. 
For example: When clients submit a value for the Price Notation field and for the Price Notation in the schedule 
block, we will only display the value received the Price Notation field and will not use the value from the 
schedule block.  
This applies to all the schedule fields: Price schedule, Strike price schedule, Notional amount schedule - Leg 1, 
Notional amount schedule - Leg 2, Notional quantity schedule - Leg 1 and Notional quantity schedule - Leg 2. 
FC 3.16 Event Timestamp & Reporting Timestamp 
For the JFSA rewrite, we will introduce timestamp-based validations. In chronological order, all submissions 
must have the Execution Timestamp =< Event Timestamp =< Reporting Timestamp =< Message Received 
Timestamp =< Message Processed Timestamp. While the first three are submitted by reporting entities, 
Message Received Timestamp and Message Processed Timestamp are derived by GTR.  
To determine the position that gets reflected on the Trade State Report as per FC 5.1, we will look use the 
above waterfall approach based on the timestamps. To be able to determine the accuracy of the positions 

---

## Page 42

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 42 
 
being reflected on the TSR, timestamp-based ingestion rules are introduced. The ingestion rules and the use case examples are illustrated below. 
Jurisdictional 
Field 
4/1/2024 onwards  4/1/2024 Onwards 
Business Rules when 
[Action Type] = NEWT, 
MODI, CORR, REVI 
4/1/2024 
Business Rules when [Action 
Type] = PRTO, EROR 
Business Rules when 
[Action Type] = TERM 
[[collateral]] Business 
Rules 
[Action Type] = MARU 
Valuation Business Rules 
[Action Type] = VALU 
Reporting 
timestamp 
(a) [Reporting timestamp] 
must be equal to or later 
than the value in 
[Execution timestamp]. 
(b) [Reporting timestamp] 
must be equal to or 
before the [Message 
Received timestamp] 
derived by the TR. 
(c) The date value of the 
[Reporting timestamp] 
must NOT be more than 2 
days before the date 
value of the [Message 
Received timestamp]. 
(a) [Reporting timestamp] 
must be equal to or later than 
the value in [Execution 
timestamp]. 
(b) [Reporting timestamp] 
must be equal to or before 
the [Message Received 
timestamp] derived by the TR. 
(c) The date value of the 
[Reporting timestamp] must 
NOT be more than 2 days 
before the date value of the 
[Message Received 
timestamp]. 
(a) [Reporting timestamp] 
must be equal to or later 
than the value in [Execution 
timestamp]. 
(b) [Reporting timestamp] 
must be equal to or before 
the [Message Received 
timestamp] derived by the 
TR. 
(c) The date value of the 
[Reporting timestamp] must 
NOT be more than 2 days 
before the date value of the 
[Message Received 
timestamp]. 
(a) [Reporting 
timestamp] must be 
equal to or before the 
[Message Received 
timestamp] derived by 
the TR. 
(b) The date value of 
the [Reporting 
timestamp] must NOT 
be more than 2 days 
before the date value 
of the [Message 
Received timestamp]. 
(a) [Reporting timestamp] 
must be equal to or before 
the [Message Received 
timestamp] derived by the 
TR. 
(b) The date value of the 
[Reporting timestamp] 
must NOT be more than 2 
days before the date value 
of the [Message Received 
timestamp]. 
(c) [Reporting timestamp] 
must be equal to or 
greater than the [Valuation 
timestamp] 

---

## Page 43

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 43 
 
Event 
timestamp 
(a) If [Action Type] = 
NEWT, MODI, CORR, the 
date value of the [Event 
timestamp] must be 
equal to or later than the 
date value in [Execution ti
mestamp]. 
(b) If [Action Type] = 
NEWT, MODI, CORR, the 
date value of the [Event 
timestamp] must be 
equal to or before the 
date value of the 
[Reporting timestamp]. 
(c) If [Action Type] = REVI, 
the date value of the 
[Event timestamp] must 
be equal to the date 
value [Reporting 
timestamp]. 
(d) If [Action Type] = 
NEWT, MODI, CORR, the 
date value in the [Event 
timestamp] should be 
equal to or before BOTH 
the [Expiration date] OR 
the [Early termination 
date] where populated. 
(a) [Event timestamp] must be 
equal to or later than the valu
e in [Execution timestamp] 
(b) The date value of the 
[Event timestamp] must be 
equal to the date value 
[Reporting timestamp]. 
(c) The date value in the 
[Event timestamp] should be 
equal to or before BOTH 
the [Expiration date] OR the 
[Early termination date] 
where populated. 
(a) [Event timestamp] must 
be equal to or greater 
than the value in [Execution
 timestamp] 
(b) [Event timestamp] must 
be equal to or before the 
[Reporting timestamp] 
(c) The date value in the 
[Event timestamp] must be 
equal to or before 
the [Expiration Date] 
(d) The date value in the 
[Event Timestamp] and the 
date value in the [Early 
termination date] should be 
the same. 
(a) The date value in 
the [Event timestamp] 
must be equal to or 
before the date value 
in the [Reporting 
timestamp]. 
[N/A] 
 
 
 
 
 
 

---

## Page 44

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 44 
 
Trade Timestamp Use-Case 
 
Events prior to the latest event timestamp will not overwrite the UTI's TSR record. There will be no determination by the TR of what needs to be 
corrected on the latest TSR record from the historical correction event (ie) any amendments on a historical event timestamp t hat is before the latest 
event timestamp will not be reflected in the latest record and firms will be responsible for reflecting the accurate version of the record  at present time. 
 
 
 
 
 
 
 
 
 
 


---

## Page 45

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 45 
 
Valuation Timestamp Use-Case 
 
 
The valuation record that is picked and merged onto the TSR record is based on Valuation Timestamp followed by Reporting Timestamp followed by 
Message Received Timestamp therefore historical valuations [[DO]] not overwrite a current valuation . When merging the valuation details onto the TSR, 
only valuation-specific fields should be updated from the valuation message. The JFSA valuation-related fields are  Valuation amount, Valuation 
currency, Valuation timestamp, Valuation method and Delta. All other timestamp fields apart from Reporting Timestamp and Valuation Timestam p on 
the TSR will continue to be based on the information on the Trade submission and not the VALU submission (i.e., they will not  be updated with the 
values from the Trade Valuation submission). 
 
 
 
 
 
 


---

## Page 46

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 46 
 
[[Margin]] Event Timestamp Use-Case 
 
The [[Margin]] State Report contains the latest [[Margin]] view based on event timestamp followed by Reporting Timestamp followed by Message Received 
Timestamp followed by Message Processed Timestamp against open positions at the point of the report generation regardless if they were 
collateralized on a trade or portfolio basis


---

## Page 47

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 47 
 
FC 4: Message Responses 
FC 4.1 Response Format  
The message response format will be changing to XML instead of the current FpML or CSV response formats  
to align with the ISO XML inbound submission format. The response file formats are returned in zip 
compression format with .xml as the file extension within the zip file: 
Description Format Current File Name 
JFSA GTR 
Batch 
ACK/NACK 
Report XML 
ISO20022XML 
SFTP File Name: 
sFTP_BizMsgIdr_JFSA_ACKNACK_Report_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.zip or 
sFTP_BizMsgIdr_JFSA_ACKNACK_Report_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.gz 
sFTP File Name within the compressed file: 
sFTP_BizMsgIdr_JFSA_ACKNACK_Report_BatchInfoID_6XXX_2023-10-20.01_10_06.xml  
Portal: 
BizMsgIdr_JFSA_ACKNACK_Report_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.zip 
 
Portal File Name within the compressed file: 
WEB-US-BatchInfoID.xml or SFP-US-BatchInfoID.xml 
 
Note: Clients may configure the compression method to .gz or .zip for sFTP. GZIP (.gz) is for UNIX 
based systems and WINZIP (.ZIP) is for Windows based systems. 
 
 
(a) BizMsgIdr is a 35-character identifier that the client indicates on the xml header in the submission file. This 
string does not allow most special characters, and would only accept alphanumeric (0-9a-zA-Z), underscore 
(_), hyphen (-) and dot (.) 
(b) The BatchInfoID would be an [[ID]] that GTR generates to identify the file reference 
(c) 6XXX refers to the o-code you submitted from 
(d) YYYY-MM-DD.HH_MM_SS is the timestamp of the response file generation in UTC 
**Note: The current BDR file name will remain as they are until at least go-live. However, if clients use the 
maximum 35 characters limit of the BizMsgIdr, the filename would get truncated due to a system limitation of 
the file delivery mechanism of only allowing up to 96 characters in the filename. While we will not reduce the 
restriction on the BizMsgIdr to less than 35 characters, firms are recommended to limit the BizMsgIdr to 25 
characters until the proposed filename changes are implemented. 
The future proposed filename in the future would be: 
 
Description Format Future Proposed File Name 
JFSA GTR 
Batch 
ACK/NACK 
Report XML 
ISO20022XML 
SFTP File Name: 
sFTP_BizMsgIdr_JFSA_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.zip or 
sFTP_BizMsgIdr_JFSA_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.gz 
sFTP File Name within the compressed file: 
sFTP_BizMsgIdr_JFSA_BDR_BatchInfoID_6XXX_2023-10-20.01_10_06.xml  
Portal: 

---

## Page 48

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 48 
 
BizMsgIdr_JFSA_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.zip 
 
Portal File Name within the compressed file: 
WEB-US-BatchInfoID.xml or SFP-US-BatchInfoID.xml 
 
Note: Clients may configure the compression method to .gz or .zip. GZIP (.gz) is for UNIX based 
systems and WINZIP (.ZIP) is for Windows based systems. 
 
 
The timeline for the implementation is proposed for post go live in Q3 2024 at the end of the transition period. 
One change is the shortening of “JFSA_ACKNACK_Report” to “BDR” and the other is the addition of .xml 
before the .zip or .gz sFTP file name. 
 
 
The ISO 20022 XML template shows there will be 2 levels of validation response (ACK /NACK).  
 
1. Message / file level  
2. Submission level  
 
The excerpt from the XML message response schema (auth.031.001.01) below shows these 2 levels of ACK / 
NACK.  
 
• The <MsgSts> within the blue section below is the element where the message / file level validation response 
will be provided. There will always be one ACK / NACK response for a submitted message / file. <MsgSts> can 
be only one of these two value:  
o <Sts>CRPT</Sts> = CRPT (Corrupt) means entire message / file is rejected. Positions inside the message 
are not open/updated on [[DTCC]] side.  
o <Sts>ACPT</Sts> = ACPT (ACK) means message / file was correctly read.  
 
• The <RcrdSts> within the red section is the element where the submission level validation response will be 
provided. If the submission file contains 100 submissions, then there will be 100 ACK / NACK responses. 
<MsgSts> can be only one of these two value:  
o <Sts>RJCT</Sts> = RJCT (NACK) means record is rejected  
o <Sts>ACPT</Sts> = ACPT (ACK) means record is accepted  

---

## Page 49

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 49 
 
 
The Business Message Header [[ID]] (BizMsgIdr tag, as shown below) must be present in the Application 
Header of each file or message submitted to the GTR. Submissions can be sent using version 01 or version 02 
of the Business Application Header (BAH). 
 


---

## Page 50

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 50 
 
 
 
The ACK / NACK message response (auth.031.001.01) generated by the GTR will provide the same BizMsgIdr 
used in the submitted file or message. This will be found in the MsgRptIdr tag highlighted below in red.  


---

## Page 51

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 51 
 
 
Identification of each submission in the ACK / NACK message response will be based on the Technical Record 
[[ID]]. Each submission (record) present in a file or message to the TR can contain a Technical Record [[ID]] (TRI) in  
the body of the XML message as highlighted below. This identifier should be unique, to allow the recipient to 
match the submission to the validation response. The Technical Record [[ID]] is required on the submission. It is 
highly recommended that firms populate this value to be able to uniquely identify and reconcile against the 
submitted record. While you may populate UTI in this field, the drawback of relying on the UTI in the Technical 
Record [[ID]] is that firms would not be able to easily identify multiple submissions with the same UTI in the same 
submission file. 
 
This Technical Record [[ID]] (TRI) will be replayed as the Original Record [[ID]] (ORI) on the validation response 
(ACK/NACK) to each submission (record), generated by the TR, using the auth.031.001.01 schema.  
 


---

## Page 52

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 52 
 
 
 
Sample files illustrating the XML response layouts can be found on the Learning Center  
 
 
 
 
 


---

## Page 53

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 53 
 
FC 4.2 Response Format/Channel  
There will be changes to the response format and channel based on the JFSA Rules Rewrite Implementation.  
As a reference, this table summarizes the future functionality: 
Submission Channel Submission 
Format 
Response 
Format 
Response  Receiver Response 
Channel 
MQ ISO XML 
message 
ISO XML ISO XML 
message 
Data Submitter MQ 
Web Upload 
(a) Without sFTP 
subscription 
(b) With sFTP subscription 
ISO XML 
files 
ISO XML ISO XML 
files 
Data Submitter (a) Portal 
(b) Portal and 
sFTP 
destination 
sFTP ISO XML 
files 
ISO XML ISO XML 
files 
Data Submitter sFTP destination 
and Portal 
 
FC 4.3 MQ Response to be sent to ReplytoQueue  
To enhance the client experience, we will introduce a functionality to allow clients to specify where the 
ACK/NACK response message should be delivered. This comes at the back of client feedback  and has already 
been implemented in NoA. 
This functionality allows you to be able to indicate where you want your responses to be sent via the Reply To 
– Queue Manager and Reply to – Queue Name details on the MQ message header so that the response would 
be returned to the queue name indicated. 
FC 5: Reports  
Daily reports are generated and made available through the [[DTCC]] Portal.  Further details on functional ity 
within the portal can be found on the Learning Center. The reports as they exist today, including the ROR and 
other reports will no longer be available. [[DO]] note that blank [[participant]] reports will not be generated should 
there be cases where the report criteria are not met for a particular day; for example no submissions within a 
reporting window. 
FC 5.1: Report Types 
The following reports will be created daily.  Details of the report layouts are available on Learning Center and 
the message specifications.  
Type Description 
JFSA [[EOD]] 
Trade 
State 
Report 
• Alleged records where the report recipient is named as the OCP should not be displayed on the Trade 
State Report.  
• Only unique trades should be displayed in the TSR. The uniqueness of a trade is defined by the 
concatenation of the UTI + RCP1. For example, if position 1 is UTI + RCP1 + OCP1 & position 2 is UTI 
+ RCP2 and OCP1, then they are considered unique positions. Another example is if an RCP and ERR 

---

## Page 54

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 54 
 
Type Description 
is the same on a position, then the position is expected to appear only once on the TSR even though 
both RCP and ERR get access to the TSR. 
• If a position is early terminated via the applicable exit action types or expired based on Expiration Date 
between a report generation window, that position will be excluded from TSR generated for that day.  
• The TSR contains the latest view of the position but excludes valuation and [[collateral]] messages, though 
valuation data fields will be merged to the position.  The latest position view of the TSR will be based on 
the latest event timestamp for that record. For example, a correction submitted for a past event 
timestamp will not overwrite a submission with a current event timestamp. 
• The TSR is run and generated daily from Tuesday to Saturday after midnight JST. 
• The reports will be available on the portal for up to 12 months on a going forward basis from go live 
date.  
• The following parties will have access to the TSR: Reporting Counterparty (RCP) and Entity 
Responsible for Reporting (ERR) 
• TSR (Position Report) should only include messages accepted at GTR and exclude rejects. 
• Each position on the report should only contain the information related to that submission. If an optional 
field is excluded from the user submission, it will be blank on the report. 
• There is no masking of fields in JFSA as TSR (Position Report) is only available to the RCP and ERR 
•  The final report format is published in the message specifications. 
• This report is created per [[Asset]] class per jurisdiction. 
• Trades which have been submitted with action type TERM or EROR (and not subsequently revived) or 
have been submitted with action type PRTO but not re-opened successfully are excluded (even if their 
expiration date is in the future). 
JFSA [[EOD]] 
Trade 
Activity 
Report 
• The Activity report should only include messages accepted at GTR and exclude rejects. 
• A report should only contain activity between two report generation periods. For instance, the report 
generated on Wednesday morning JST should contain accepted trade messages submitted between 
Tuesday 00:00:00 JST to Tuesday 23:59:59 JST. The only exception where this report contains multiple 
days’ worth of submissions is the report generated on Tuesday morning JST which would contain 
accepted trade messages submitted between Saturday 00:00:00 JST to Monday 23:59:59 JST. The 
timestamp to be considered is based on the submission timestamp which is the time submitted by the 
user. Multiple trade submissions with the same identifier would be displayed multiple times if they are 
submitted successfully within the reporting window. 
• Each position on the report should only contain the information related to that submission. If an optional 
field is excluded from the user submission, it will be blank on the report. 
• The [[EOD]] Activity report should contain only trade messages or valuation messages but exclude 
[[collateral]] submissions which will be on a separate [[collateral]] activity report. 
• Allege records where the report recipient is named as the OCP should not be displayed on the Trade 
Activity Report 
• The TAR is run and generated daily from Tuesday to Saturday after midnight JST. 
• The reports will be available on the portal for up to 12 months on a going forward basis from go live 
date. 
• The following parties will have access to the Activity report: RCP and ERR 
• There is no masking of fields in the Activity report.  
• The final report format is published in the message specifications. 
• This report is created per [[Asset]] class per jurisdiction. 
JFSA [[EOD]] 
Submission 
Report 
• The Submission Report contains all the successful and unsuccessful submissions submitted by the 
report submitting entity (RSE). All Accepted and Rejected submissions are included in the report. 

---

## Page 55

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 55 
 
Type Description 
• [[EOD]] cutoff is 23:59 JST Monday to Friday meaning any submissions that are received based on 
submission received timestamp of 23:59:59 JST is eligible for reporting on that day’s submission reports 
even if it is processed by GTR past the next day. 
• The Submission Report contains trade and valuation messages but excludes [[collateral]] messages. 
[[collateral]] submissions will be reflected on a separate report. 
• The Submission Report will only be available in CSV format. 
• The Submission Report is run and generated daily from Tuesday to Saturday after midnight JST. 
• The reports will be available on the portal for up to 12 months on a going forward basis from go live 
date. 
• The following parties will have access to the Submission Report: Submitter Identifier (RSE), Reporting 
Counterparty (RCP) and Entity Responsible for Reporting (ERR). The submitter identifier (RSE) will see 
all trade sides they have submitted, whether accepted or rejected but cannot view any submissions they 
did not submit.  
• If the Reporting Counterparty (RCP) and Entity Responsible for Reporting (ERR) are different, both will 
see the trade with themselves as RCP or ERR and their counterparty as OCP, whether accepted or 
rejected. The Reporting Counterparty (RCP) and Entity Responsible for Reporting (ERR) will see all the 
successful and unsuccessful submissions submitted by themselves. 
• There is no masking of fields in the JFSA Submission Report 
• The final report format is published in the message specifications.  
• This report is created per [[Asset]] class per jurisdiction. 
JFSA [[EOD]] 
[[Margin]] 
State 
Report 
• The [[Margin]] State Report is run and generated daily from Tuesday to Saturday after midnight JST. 
• The [[Margin]] will be available on the portal for up to 12 months on a going forward basis from go live 
date. 
• The [[Margin]] State Report contains the latest [[Margin]] view based on event timestamp against open 
positions at the point of the report generation regardless if they were collateralized on a trade or 
portfolio basis.  
• For [[Derivatives]] collateralized on a trade basis:  
(a) if the derivative position (RCP-OCP-UTI) was Early Terminated on 15/5/2024, the [[Margin]] state for 
that derivative position MUST NOT be on the MSR published to the client on 16/5/2024 but will be 
on the 15/5/2024 report. 
(b) if the derivative position (RCP-OCP-UTI) reached its Expiration Date on 15/5/2024, the [[Margin]] 
state for that derivative position MUST BE on the MSR published to the client on 15/5/2024 but 
drops off from the MSR on 16/5/2024. 
• For [[Derivatives]] collateralized on a portfolio basis:  
(a) If at least 1 derivative position (RCP-OCP-UTI) within the portfolio (concatenated value of IM/VM 
portfolio code) is outstanding on 15/5/2024 (and that includes derivative positions in that portfolio 
that might have a Expiration Date of 15/5/2024), the [[Margin]] state for that [[collateral]] portfolio MUST 
BE on the MSR published to the client on 15/5/2024 but will drop off on 16/5/2024 assuming there 
is no further outstanding derivative position associated with the IM/VM portfolio code with an 
expiration date after 15/5/2024(b) all derivative positions (RCP-OCP-UTI) within the portfolio 
(concatenated value of IM/VM portfolio code) is non-outstanding on 15/5/2024 (including being 
early terminated on 15/5/2024), the [[Margin]] state for that [[collateral]] portfolio MUST NOT be on the 
MSR published to the client on 16/5/2024 
• The following parties will have access to the MSR: Reporting Counterparty (RCP) and Entity 
Responsible for Reporting (ERR) 
• The [[Margin]] State Report should only include [[collateral]] messages accepted at GTR and exclude rejects. 
• Each line on the report should only contain the information related to that submission. If an optional field 
is excluded from the user submission, it will be blank on the report. 
• There is no masking of fields in JFSA as MSR is only available to the RCP and ERR 

---

## Page 56

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 56 
 
Type Description 
•  The final report format is published in the message specifications. 
JFSA [[EOD]] 
[[Margin]] 
Activity 
Report 
• The [[Margin]] Activity report should only include “MARU” action type messages that are accepted at GTR 
and exclude rejects. 
• A report should only contain activity between two report generation periods. For instance, the report 
generated on Wednesday morning JST should contain accepted [[collateral]] messages submitted 
between Tuesday 00:00:00 JST to Tuesday 23:59:59 JST. The only exception where this report 
contains multiple days’ worth of submissions is the report generated on Tuesday morning JST which 
would contain accepted [[collateral]] messages submitted between Saturday 00:00:00 JST to Monday 
23:59:59 JST. The timestamp to be considered is based on the submission timestamp which is the time 
submitted by the user. Multiple trade submissions with the same identifier would be displayed multiple 
times if they are submitted successfully within the reporting window. 
• Each line on the report should only contain the information related to that submission. If an optional field 
is excluded from the user submission, it will be blank on the report. 
• The [[Margin]] Activity report should contain only [[collateral]] messages. 
• Allege records where the report recipient is named as the Trade Party 2 should not be displayed on the 
[[Margin]] Activity Report 
• The [[Margin]] Activity Report is run and generated daily from Tuesday to Saturday after midnight JST. 
• The reports will be available on the portal for up to 12 months on a going forward basis from go live 
date. . 
• The following parties will have access to the Activity report: RCP and ERR 
• There is no masking of fields in the [[Margin]] Activity report.  
• The final report format is published in the message specifications. 
JFSA [[EOD]] 
[[Margin]] 
Submission 
Report 
• The [[Margin]] Submission Report contains all the successful and unsuccessful submissions submitted by 
the report submitting entity (RSE). All Accepted and Rejected submissions are included in the report. 
• [[EOD]] cutoff is 23:59 JST Monday to Friday meaning any submissions that are received based on 
submission received timestamp of 23:59:59 JST is eligible for reporting on that day’s submission reports 
even if it is processed by GTR past the next day. 
• The [[Margin]] Submission Report contains only [[collateral]] messages based on action type MARU. 
• The [[Margin]] Submission Report will only be available in CSV format. 
• The [[Margin]] Submission Report is run and generated daily from Tuesday to Saturday after midnight 
JST. 
• The reports will be available on the portal for up to 12 months on a going forward basis from go live 
date. 
• The following parties will have access to the Submission Report: Submitter Identifier (RSE), Reporting 
Counterparty (RCP) and Entity Responsible for Reporting (ERR). The submitter identifier (RSE) will see 
all trade sides they have submitted, whether accepted or rejected but cannot view any submissions they 
did not submit.  
• If the Reporting Counterparty (RCP) and Entity Responsible for Reporting (ERR) are different, both will 
see the trade with themselves as RCP or ERR and their counterparty as OCP, whether accepted or 
rejected. The Reporting Counterparty (RCP) and Entity Responsible for Reporting (ERR) will see all the 
successful and unsuccessful submissions submitted by themselves. 
• There is no masking of fields in the JFSA [[Margin]] Submission Report 
• The final report format is published in the message specifications. 
JFSA [[EOD]] 
Allege 
Trade 
• The End of Day allege report will consist of the Allege view of the trade and will be provided only in CSV 
format. 
• This report will be based off the TSR and will contain the Allege view of positions at [[EOD]]. 

---

## Page 57

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 57 
 
 
 
Users who wish to have the NEW reports sent to them via sFTP will need to set up configurations for the new 
product IDs with our connectivity team (GTRConnectivity@[[DTCC]].com). 
 
Type Description 
State 
Report 
• The party receiving this report will be the Other Counterparty of the trades if the Other Counterparty is 
onboarded. 
• Only unique trades should be displayed in the Allege Report. The uniqueness of a trade is defined by 
the concatenation of the UTI + OCP.  
• If a position is early terminated via the applicable exit action types or expired based on Expiration Date 
between a report generation window, that position will be excluded from Allege Report generated for 
that day.  
• The Allege Report contains the latest view of the position but excludes valuation and [[Margin]] data. 
• The Allege Report is run and generated daily from Tuesday to Saturday after midnight JST. 
• The reports will be available on the portal for up to 12 months on a going forward basis from go live 
date. 
• The following parties will have access to the Allege Report: Other Counterparty (OCP) if they are 
onboarded. 
• The Allege Report should only include messages accepted at GTR and exclude rejects. 
• Each position on the report should only contain the information related to that submission. If an optional 
field is excluded from the user submission, it will be blank on the report. 
• The final report format will be published in the message specifications. 
• This report is created per [[Asset]] class per jurisdiction. 
 
JFSA 
Intraday 
Allege 
Activity 
Report 
• The intention of this new GTR report will be to facilitate a way for counterparties to share data intraday. 
• This report is not mandated by the regulators. It is a GTR proprietary report. 
• The Intraday Allege Report will only include messages accepted into the GTR between the intraday 
reporting windows. Rejected messages will be excluded. 
• The Intraday Allege Activity Report will only include submissions, that have been accepted (Rejected 
messages will be excluded) on that particular day, with the Action Types of NEWT, EROR, REVI where 
the client (for whom report is being generated) is listed as CP2 
• The Intraday Allege Report will be generated in CSV only. 
• The Intraday Allege Report will be generated thrice daily at 10:00am JST and 18:00pm and 00:00am 
JST between Monday to Friday. The Intraday Allege Activity Report will include eligible submissions 
accepted up to the point of generation of the report (will be cumulative). 
 
6pm Report - include eligible Action Types accepted between 00:00:00 am and 17:59:59pm 
• The reports will be available on the portal for up to 12 months on a going forward basis from go live 
date. The following parties will have access to the Intraday Allege Report: Other Counterparty (OCP) if 
they are onboarded 
• If an optional field is excluded from the user submission it will also be blank on the report 
• The final report format is published in the message specifications. 
• This report is created per the [[Asset]] class(es) configured under the standard [[DTCC]] O-Code 
• A detailed report specification is provided on the learning centre 

---

## Page 58

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 58 
 
FC 5.2: Merging of Trade Valuation Information onto Trade State Report 
1. Merging of fields from Valuation submission onto TSR:  When merging the valuation details onto the 
TSR, only valuation-specific fields should be updated from the valuation message. The JFSA valuation -
related fields are Reporting timestamp, Valuation amount, Valuation currency, Valuation timestamp, 
Valuation method and Delta  
2. We will follow latest valuation timestamp approach for valuation submissions for JFSA when linking the 
valuation fields to the position on the TSR. 
3. All other timestamp fields on the TSR will continue to be based on the information on the Trade 
submission (i.e., they will not be updated with the values from the Trade Valuation submission).  
4. Timestamp used for merging the “latest” valuation:  The valuation submission used for merging onto 
the TSR will be based on the latest Valuation Timestamp. 
5. When matching a Valuation to a base trade for merging information onto the TSR at end of day, the UTI + 
RCP + OCP must match. 
FC 5.3: Self-Service Report Management Functionality  
As JFSA and various other jurisdictions [[DO]] not regulatorily mandate [[participant]] reports to be in a particular 
format, our understanding is that firms may need a choice of receiving reports in XML, CSV or XML and CSV. 
[[DO]] however note that [[DTCC]] proprietary reports (refer to FC 5.1) will only be available in CSV only.  
Report Management will be an additional landing tile on the Manage Services screen. Selecting the tile allows 
firms to add and configure reports per service and the [[default]] setup will be CSV format for all reports. Reports 
will be aggregated by type (for example, Trade State Report). Clients cannot choose to further segregate the 
same report by [[Asset]] class.  
This functionality will not require any specific build from clients but will require a one-time setup and 
subscription. Once subscribed, reports will be generated in the selected format from that day going forward. 
Clients can also unsubscribe from reports to stop receiving them. [[DTCC]] plans to implement this functionality 
ahead of both actual UAT and Production dates to allow for clients to perform their setups in advance.  
For further details, refer to Report Management Section on the Learning Centre. 
FC 5.4: Report Filename Formats  
Description Format Proposed File Name 
JFSA Trade 
Activity Report 
XML 
ISO20022XML 
sFTP 
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
 
Portal 
JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 

---

## Page 59

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 59 
 
JFSA Trade 
State Report 
XML 
ISO20022XML 
sFTP 
sFTP_JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
sFTP_JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
sFTP_JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
sFTP_JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
sFTP_JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
 
Portal 
JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
JFSA [[Margin]] 
Activity Report 
XML 
ISO20022XML 
sFTP 
sFTP_JFSA_EOD_Margin_Activity_Report_02503236-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
 
Portal 
JFSA_EOD_Margin_Activity_Report_02503236-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
JFSA [[Margin]] 
State Report 
XML 
ISO20022XML 
sFTP 
sFTP_JFSA_EOD_Margin_State_Report_02503237-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
 
Portal 
JFSA_EOD_Margin_State_Report_02503237-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
JFSA Trade 
Activity Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
JFSA Trade 
State Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
JFSA [[Margin]] 
Activity Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_JFSA_EOD_Margin_Activity_Report_02503240-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
 
Portal 
JFSA_EOD_Margin_Activity_Report_02503240-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
JFSA [[Margin]] 
State Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_JFSA_EOD_Margin_State_Report_02503241-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
 
Portal 
JFSA_EOD_Margin_State_Report_02503241-YYYY-MM-DD.HH_MM_SS_0XXX.csv 

---

## Page 60

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 60 
 
JFSA [[Margin]] 
Submission 
Report CSV 
CSV only 
sFTP 
sFTP_JFSA_EOD_Margin_Submission_Report_02503242-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
 
Portal 
JFSA_EOD_Margin_Submission_Report_02503242-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
JFSA Trade 
Submission 
Report CSV 
CSV only 
sFTP 
sFTP_JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
JFSA [[EOD]] 
Allege Report CSV only 
sFTP 
sFTP_JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
 
Portal 
JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
JFSA Intraday 
Allege Report CSV only 
sFTP 
sFTP_JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
 
Points to Note regarding the report formats: 
(a) For XML based reports, the same day reports will be split when it contains more than 500,000 records. 
Part of the report filename contains 001001 where the first three digits represent the number of total 
files, and the second three digits represent the sequence of the file (E.g. 00 5001 meaning there are 5 
files in total and this file is file 1 in the sequence).    
(b)  The report timestamp DD.HH_MM_SS will be displayed in UTC timezone. 
(c) The report names in the table above indicate the actual file names that are within the compressed file. 
For sFTP-ed reports, the compressed file could either be configured to have compression type as 
GZIP (.gz) which is for UNIX based systems or WINZIP (.zip) for Windows based systems.  For 
example, the filename within the compressed file would be:  

---

## Page 61

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 61 
 
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_6XXX.csv OR 
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
 
however the zipped filename could be  
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-2023-10-27.17_34_31_2CHR.csv.gz OR 
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-2023-10-27.17_34_31_2CHR.csv.zip 
 
FC 6: Functionality Specific to Go-Live 
Users are expected to upgrade their open trades to the new data standards as defined in the message 
specifications after go-live.  This section describes relevant functionality to support that process and other go -
live related processes. 
Please note that these activities will be performed during both UAT and Product ion go-lives. 
FC 6.1:  [[DTCC]] Action Type Initialization at Go-live – Trade State 
In order to support new functionality required to validate action type sequences, the GTR will need to maintain 
the status of every trade per the Action Type Sequence diagram (“Open”, “Terminated”, “Errored”, “Expired”, or 
“Transferred Out”), and use this status to compare to action types received on subsequent message 
submissions.  At go-live, this information about each trade will need to be initialized in the GTR application to 
support validations on submissions post go-live.  This initialization will be performed per Trade and Jurisdiction 
(UTI + RCP).  Please refer to further information on Action Type Rules as defined in section FC 3.8.   
Accordingly, GTR Action Type initialization will perform the following at go-live: 
• On Day 0 at 29 March 2024 23:59 JST, all active positions remaining will be taken as the eligible trade 
population for data initialization (i.e., trades which have not been exited on or before Mar 29, 2024, a nd 
whose expiration date is greater than Mar 29, 2024) will be initialized as “Open”.  This will enable “stateful” 
validations that will prevent further NEWT submissions for these trades and to allow for subsequent action 
types which would be allowed to follow Open trades. All “Open” initialized positions at the point of go live 
need to be minimally updated with a MODI-UPDT action type/event type combination after 1 April 2024 
before any subsequent action types such as VALU or MARU can be submitted.  
• However, as we [[DO]] not know the positions that have been previously submitted directly to JFSA and will 
be re-reported into the trade repository, such users are required to submit an Action Type of “NEWT” and 
Event Type of “PTNG” as the first submission into the trade repository. 
• The USI Value for all positions with a future maturity date where the maturity date is equal to or greater 
than 30 March 2024 will be migrated to the Proprietary [[ID]] tag in the new database. The USI Prefix field 
will be ignored. Users can continue to submit the legacy uppercase USI value into the proprietary [[ID]] tag or 
the Global UTI tag (if the current USI happens to meet the format requirement of the Global UTI which is 
([A-Z0-9]{18}[0-9]{2}[A-Z0-9]{0,32})) once they are ready to enrich their legacy positions  

---

## Page 62

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 62 
 
• All other historical /USI which were “dead” prior to 29 March 2024 23:59 JST and/or not migrated to the 
new architecture, will have no initialization of Action Type information, so any re-reporting required to 
correct the historical record for these should be submitted starting with a “NEWT”. Please note that 
although these are historical trades, they must comply with all new validations.  
 
• Apart from initializing the trades, we will capture and store the following fields: USI Value (without the 
prefix), Trade Party 1 and maturity date. For absolute clarity, while we would store this information for the 
purposes of validating subsequent submissions including modifications, terminations and valuations; the 
active positions would not appear on the TSR unless they have successfully been re -submitted from 30 
March 2024 onwards. Regarding valuation submissions and linking to the base position, the valuation 
message will not be accepted if the trade MODI has not been submitted, so the expected user behavior is 
for the resubmission of the base trade modification based on the new field and validation rules prior to the 
valuation message submission. This is because there is no feasibility of migrating the current complex 
legacy data set which had not changed since JFSA first went live in 2013.  
• The current plan is to produce a csv file in Feb 2024 based on production data that contains information 
on trades that are migrated on go-live with the [[BASIC]] field information including the initialized USI value, 
RCP, OCP and RSE stated in the above point. 
FC 6.2: Data Migration Dry Run Plan 
• Firms are encouraged to seed positions in UAT by 23:59 JST on 28 September 2023 to be considered for 
the UAT data migration initialization. While we don’t expect a complex data migration initialization exercise 
as part of the UAT or Production migration, firms can test a MODI after the migration on trades that are 
considered for the data initialization. Therefore, any trades submitted into UAT before 28 September 2023 
and has a maturity date beyond that will be in scope if the positions are not excluded due to any of the 
reasons mentioned in FC 6.3 to FC 6.4. Even if your firm is not ready to test, you are encouraged to at 
least seed some trades to eventually test when you are ready. 
• During the UAT migration period between 29 September 2023 to 8 October 2023, we will perform the 
initialization of the UAT positions. Once completed, [[Asset]] class-based CSV reports containing the 
initialized USI value, RCP, RSE and [[Asset]] class will be produced to indicate what was initialized and what 
wasn’t. Firms can then test performing a MODI-UPDT on the initialized positions. All other action type and 
event type combinations on initialized trades will be rejected if there wasn’t a preceding successfully ACK -
ed MODI-UPDT. As the TSR would not be ready until end-November in UAT, firms can only verify these 
submissions on the TAR and subsequently validate them on the TSR when available. This will simulate 
the actual production migration on 1 April 2024. 
• After the end-November UAT, a dry run based on production data will be conducted on 9 Feb 2024. This 
will reflect the positions considered for trade initialization at that date, so firms can have an early preview 
of what is considered and what was excluded for data initialization though you would not be able to test 
the MODI-UPDT. The trades that did not get initialized will be captured in the EXCL TRADE REPORT 
while the trades that are successfully initialized will be captured in the DMIG TRADE REPORT. Both are 
cross-[[Asset]] reports with a consolidated view of all eligible positions for ease of reconciliations. 

---

## Page 63

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 63 
 
 
 
FC 6.3:  Removal of “Duplicate” Positions Due to Trade Uniqueness Change 
As noted in section FC 3.4, trade uniqueness changes will require the removal of “duplicate” trades at go -live.  
These are defined as open trades where the same combination of /USI + Reporting Party (Trade Party 1) 
exists with multiple different Counterparties (Trade Party 2).  It is strongly recommended that users explicitly 
EXIT any duplicate positions prior to go-live so that they can control which trade remains for the given UTI/USI. 
However, if users [[DO]] not remove these duplicate open trades prior to go-live, [[DTCC]] will discontinue reporting 
them on the Trade State Report after go-live.  [[DTCC]] will select the open trade which has been most recently 
updated based on the latest message submitted timestamp as the position considered for initialization.  While 
[[DTCC]] will keep a record internally of what has occurred for these trades, explicit reporting of EXIT activity will 
not be provided to participants or regulators.  
Example of /USI+TP1 combination with multiple TP2 positions existing at go-live: 
USI Trade 
Party 1 
Trade 
Party 2 
Last 
Update 
Comment 
USI1 LEIa LEIb 01/12/22 If users [[DO]] not exit, [[DTCC]] would discontinue reporting this after go-
live. 
USI1 LEIa LEIc 01/15/22 If users [[DO]] not exit, [[DTCC]] would discontinue reporting this after go-
live. 
USI1 LEIa LEId 01/27/22 If users [[DO]] not exit, [[DTCC]] would discontinue reporting this after go-
live. 
USI1 LEIa LEIe 03/21/22 [[DTCC]] will retain the most recently updated trade. 


---

## Page 64

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 64 
 
USI Trade 
Party 1 
Trade 
Party 2 
Last 
Update 
Comment 
USI1 LEIa LEIf 01/15/22 If users [[DO]] not exit, [[DTCC]] would discontinue reporting this after go-
live. 
FC 6.4: Exclusion of Self Trades 
Self-trades would be excluded from the action type initialization. While they exist internally in the database 
today, they are not exposed to clients in any reports. Self-trades are defined as trades where the Counterparty 
1 and Counterparty 2 are the same. Post go-live, self-trades will be validated and rejected at ingestion.  
FC 6.5: Upgrading Open Trades After Go-Live 
Open trades at go-live can be upgraded to the new data standards after go-live. Submit a specific trade state 
message with Action Type = “MODI” and Event Type = “UPDT” before submitting the next logical trade 
lifecycle event, as per the normal course of business.  
FC 6.6:  Reporting During Transition Period 
After go-live, all reporting will be done using the new report formats.  The submission and activity -based 
reports will reflect all data submitted in the new format after go-live. Any pre go-live active positions would not 
appear on the TSR unless they have successfully been re-submitted post data initialization based on the post 
go live validation rules. Users who are ready on April 1, 2024, are encouraged to backload fully enriched open 
positions on April 1, 2024, as full re-reporting is anyways required from existing DDRJ users. [[DO]] note that the 
transition period of 180 days ends on 27 September 2024. 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 65

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 65 
 
FC 6.7: Go-Live Schedule 
A precise schedule of go-live weekend activities will be published separately closer to implementation.  At a 
high level, the production implementation plan is below: 
 
 
FC 7: Billing 
FC 7.1:  Billing Hierarchy  
While DDRJ will not be implementing fee schedule changes as part of the April 1, 2024 go-live, the parties 
considered for billing will be based off a hierarchy of “Entity Responsible for Reporting” followed by 
“Counterparty 1 (reporting counterparty)” followed by “Submitter identifier”. As Entity Responsible for Reporting 
is required to be onboarded to the JFSA service, all positions are expected to be billed to this entity. The 
existing fee schedule and month end billing approach will remain until further notice of the fee schedule 
reviews post go-live. 
FC 7.2:  Billing Substantiation Report  
The future billing substantiation report will contain the following fields and will continue to be produced on a 
monthly basis for all clients who have billable positions. The JFSA substantiation reports will be updated to 
remove out of date and unrequired fields, incorporate ERR fields, change to singular UTI field in line with re -
write change to a single trade identifier (UTI) post re-write, remove Execution Agent fields as this is not a 
billable party for JFSA. 
[[Asset]] Class 
UTI 


---

## Page 66

 
[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
PAGE 66 
 
Submitted For Reporting Destination 
Billing Period (Month) 
Entity Responsible for Reporting LEI 
Entity Responsible for Reporting [[DTCC]] 
Account 
Entity Responsible for Reporting [[DTCC]] Name 
Submitted For LEI 
Submitted For [[DTCC]] Account 
Submitted For Name 
Data Submitter LEI 
Data Submitter [[DTCC]] Account 
Data Submitter Name 
Party 1 LEI 
Party 1 Name 
Party 2 LEI 
Party 2 Name 
Billable [[DTCC]] Account 
Billable Corporate Parent Account 
Billing Exception Reason 

---

## Page 67

[FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE] 
 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
Derivativeslearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 