---
title: "ASIC & MAS Rewrite Functional Change Document"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ASIC%20MAS%20Rules%20Rewrite%20Functional%20Change%20v0.4.pdf"
pages: 69
size: "1897.9 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# ASIC & MAS Rewrite Functional Change Document

**Original File:** [ASIC MAS Rules Rewrite Functional Change v0.4.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ASIC%20MAS%20Rules%20Rewrite%20Functional%20Change%20v0.4.pdf)  
**Category:** Rules  
**Total Pages:** 69  
**File Size:** 1897.9 KB  

---

## Page 1

 
 
Ncoding 
other 
 
 
 
 
 
 
 
 
GLOBAL TRADE REPOSITORY 
FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS RULES REWRITE 
VERSION 0.4 
JAN 31, 2024 
 


---

## Page 2

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: 31 January 2024 
Service: RDS 
Title: ASIC & MAS RULES REWRITE FUNCTIONAL CHANGE 
 

---

## Page 3

 
 
Document Revision History 
Date Author Version Description 
30/6/2023 PL E, FA 0.1 Initial Draft 
20/10/2023 PL E, FA 0.2 (a) In Scope under Summary – Updated information of LEI and 
Reports for ASIC and MAS 
(b) FC 1 – Updated MQ input queue and sFTP product IDs for 
ASIC and MAS 
(c) FC 2.3 – Added information about header elements, 
definition, xpaths and sample values 
(d) FC 3.1 – Provided examples of schema validation scenario 
(e) FC 3.3 – Updated requirement for UTI and support of the 
proprietary [[ID]] tag in the Unique transaction identifier (UTI) data 
element 
(f) FC 3.5 – Updated Trade Level and Portfolio Level [[Margin]] 
valuation for MAS to align with ASIC 
(g) FC 3.7 – Updated for clarity 
(h) FC 3.9 – Updated when trades drop off TSR and [[Margin]] 
reporting for MAS. Updated Action type diagrams for ASIC and 
MAS 
(i) FC 3.12 – Added additional explanation about Usage 
Guidelines 
(j) FC 3.14, 3.15, 3.16, 4.3 – Added new sections 
(k) FC 4.2 – Added Response Channels 
(l) FC 5.1 – Updated reports retention duration and details 
about Intraday Allege Activity Report Corrected typos and text 
for more clarity 
(m) FC 5.3 – Added new section 
(n) FC 6.3: Updated requirement of UTI  
(o) FC 6.6: Go live schedule updated 
(p) FC 7.1, 7.2: Added new sections 

---

## Page 4

 
 
30/11/2023 PL E, FA 0.3 (a) Background and In-Scope under Summary – Updated 
information of MAS rules finalization 
(b) FC 1 – Updated MQ input queue and sFTP product IDs for 
ASIC and MAS 
(c) FC 2.3 – Introduced validation requirements for BizMsgIdr 
(d) FC 3.1, 3.5 – Updated for clarity 
(e) FC 3.9 – Updated Stateful validation and Action Type 
workflow to align with CDE v3.0: TERM submissions are 
allowed for Expired trade 
(f) FC 3.11 – Action Type MODI is not allowed to change 
Counterparty 
(g) FC 3.12 – Same UTI is not allowed to be reused 
(h) FC 3.16 – Updated Other Payment uniqueness key by 
replacing Other Payment Currency to Other Payment Date and 
use-case scenarios 
(i) FC 4.1 – Updated specifications on the Batch ACK/NACK 
response format 
(j) FC 5.1 – Update to TSR/MSR: Trades that become 
terminated/expired for that day will not be on the TSR/MSR 
generated of that day 
(k) FC 5.4 – Added new section 
(l) FC 6.2 – Updated for clarity 
(m) FC 6.7 – Go live schedule updated 
31/1/2024 PL E, FA 0.4 (a) FC 1 – Added links for GTR Rewrites sFTP and MQ 
Connectivity Client Pack and details for parallel environment 
when ASIC and MAS Rewrite UAT goes live 
(b) FC 1.1, 1.2 – Added new sections 
(c) FC 3.1 – Added illustration of an example for numeric data 
type 
(d) FC 3.3 – Update to updating existing trade post rewrite: 
Proprietary [[ID]] should be used 

---

## Page 5

 
 
(e) FC 3.5 – Included Action type “CORR” as corrections are 
allowed for [[Margin]] messages 
(f) FC 3.7 – Updated for clarity 
(g) FC 3.8 – Execution Agent of Counterparty 1 added as an 
optional field for MAS Message Specifications v0.3 
(h) FC 3.11, 3.12 – Updated expected result for use cases 
(i) FC 3.13 – Added links for ASIC and MAS Usage Guidelines 
(j) FC 3.17 – Added examples of how values from the 
Schedules will be reported in the TSR CSV Reports  
(k) FC 4.1 – Updated to reflect BDR filenames 
(l) FC 5.1 – The [[Margin]] Submission and Activity Reports will 
contain [[Margin]] messages with Action type “CORR’ 
(m) FC 6.2 – Updated information for Data Migration for ASIC 
and MAS 
(n) FC 7.1, 7.2 – Added details for Global Portal changes  
 
 

---

## Page 6

 
 
TABLE OF CONTENTS 
Document Revision History ................................................................................................................................ 3 
1. Summary ........................................................................................................................................................... 8 
Background ......................................................................................................................................................... 8 
In-Scope .............................................................................................................................................................. 8 
Out of Scope .....................................................................................................................................................10 
Reference Documents ......................................................................................................................................11 
Naming Conventions and Definitions................................................................................................................11 
2. Functional Change Requirements ................................................................................................................ 13 
FC 1: Connectivity: Message Channel, Routing and Submission Methods  .....................................................13 
FC 1.1: MQ Connectivity .................................................................................................................................14 
FC 1.2: sFTP Connectivity ..............................................................................................................................14 
FC 2: Ingestion – Message Types and Submission Formats ...........................................................................17 
FC 2.1: Inbound Message Types and Submission Formats ...........................................................................17 
FC 2.2: Special Characters .............................................................................................................................18 
FC 2.3: Message Header Format ....................................................................................................................18 
FC 3: Ingestion - Processing of Submissions ...................................................................................................20 
FC.3.1: Message Validations ..........................................................................................................................20 
FC 3.2: Message Sequencing .........................................................................................................................22 
FC 3.3: Trade Identifiers..................................................................................................................................22 
FC 3.4: Uniqueness of a Trade .......................................................................................................................23 
FC 3.5: [[Margin]] Message Submissions ...........................................................................................................23 
FC 3.6: Trade Valuation Submissions .............................................................................................................25 
FC 3.7: Reporting Counterparty and Entity Responsible for Reporting ..........................................................25 
FC 3.8: Execution Agent of Counterparty 1 ....................................................................................................26 
FC 3.9: Action Type and Event Type Validations ...........................................................................................26 
FC 3.10: Submissions with Reduced Validations ...........................................................................................31 
FC 3.11: Change of Counterparty ...................................................................................................................31 
FC 3.12: Change of Reporting Counterparty ..................................................................................................32 

---

## Page 7

 
 
FC 3.13: ASIC & MAS Usage Guidelines .......................................................................................................33 
FC 3.14: Introduction of an Aggregated O-Code ............................................................................................34 
FC 3.15: Unique Product Identifier (UPI) ........................................................................................................34 
FC 3.16: Other Payment Fields .......................................................................................................................35 
FC 3.17: Schedule Fields ................................................................................................................................40 
FC 4: Message Responses ..............................................................................................................................46 
FC 4.1 Response Format ................................................................................................................................46 
FC 4.2 Response Format/Channel .................................................................................................................52 
FC 4.3 MQ Response to be sent to ReplytoQueue ........................................................................................52 
FC 5: Reports ....................................................................................................................................................52 
FC 5.1: Report Types ......................................................................................................................................52 
FC 5.2: Merging of Trade Valuation Information onto Trade State Report .....................................................57 
FC 5.3 Self-Service Report Management Functionality ..................................................................................57 
FC 5.4 Report Filename Formats ....................................................................................................................58 
FC 6: Functionality Specific to Go-Live ............................................................................................................62 
FC 6.1:  Transition Period – Data Migration Background ...............................................................................63 
FC 6.2:  [[DTCC]] Data Migration at Go-live – Trade State .................................................................................64 
FC 6.3:  Removal of “Duplicate” Positions Due to Trade Uniqueness Change ..............................................65 
FC 6.4: Trades with Special Characters in Trade Identifiers ..........................................................................65 
FC 6.5: Exclusion of Self Trades .....................................................................................................................65 
FC 6.6: Reporting During Transition Period ....................................................................................................65 
FC 6.7: Go-Live Schedule ...............................................................................................................................66 
FC 7: Portal Changes .......................................................................................................................................66 
FC 7.1: Simulator UAT ....................................................................................................................................66 
FC 7.2: Trade Identifier Service ......................................................................................................................67 
 

---

## Page 8

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
PAGE 8 
 
1. SUMMARY 
Background 
This is a high-level document covering the ASIC & MAS GTR Rules Rewrite implementation. 
The upcoming Rules Rewrite initiative will ensure that the GTR implements the rule changes announced by 
both ASIC and MAS. 
ASIC published ASIC Derivative Transaction Rules (Reporting) 2024 on 19 December 2022. These rules 
repeal and remake ASIC Derivative Transaction Rules (Reporting) 2022 on 21 October 2024. The changes 
associated with the Rules Rewrite initiative will impact all five existing reportable [[Asset]] classes (Credit, Interest 
rates, Equities, Commodities, and Foreign Exchange), Valuation, and [[Margin]] reporting. There are 104 data 
fields proposed by ASIC. Firms will be required to submit in ISO XML 20022 format commencing  21 October 
2024 and the transition deadline to update existing trades is set on 20 April 2025.  
MAS started seeking views on the proposed amendments to the [[securities]] and Futures (Reporting of 
[[Derivatives]] Contracts) Regulations 2013 in July 2021. Since then, MAS has continually engaged industry 
members and other APAC regulators before finalizing and publishing the rules. The commencement date for 
the MAS reporting rules changes is 21 October 2024 and confirmed via a circular published on 27 November 
2023. There are 134 reportable data fields. ISO XML 20022 format is required for submissions when the rules 
commence and re-reporting is done to be within 6 months of rules commencement. There will be an exemption 
for re-reporting of any information required for MAS Rewrites but previously was not captured at the point when 
the contract was executed. No re-reporting is required for contracts with a maturity of less than 6 months from 
the commencement of rules. 
In-Scope 
The scope of this document will cover the following changes: 
Items ASIC Description MAS Description 
Compliance Date 1 step approach 
Go-live date: 21 October 2024 – Required fields submitted in ISO XML format  
Re-reporting of outstanding contracts deadline: 6 months from go-live date up till 20 April 2025  
UPI UPI is mandated for new trades beginning 21 October 2024 and must be re-reported for 
existing trades by the end of the transition period. 
LEI Renewed LEI (GLEIF registration status: 
Issued, Pending transfer, Pending archival) 
will be mandated for the Reporting 
Counterparty (RCP), Entity Responsible for 
Reporting (ERR), Report Submitting Entity 
(RSE), Execution Agent of Counterparty 1, 
[[Broker]] [[ID]] and Central Counterparty.  
 
Renewed LEI (GLEIF registration status: Issued, 
Pending transfer, Pending archival) will be 
mandated for the Reporting Counterparty 
(RCP), Entity Responsible for Reporting (ERR), 
Report Submitting Entity (RSE) and Central 
Counterparty.  
 

---

## Page 9

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
PAGE 9 
 
If LEI is reported for Counterparty 2 (OCP) 
and Beneficiary 1, LEI will be validated 
against GLEIF and the GLEIF registration 
status must be either Issued, Lapsed, 
Pending transfer, Pending archival. 
 
LEI is mandated for Clearing [[Member]] and 
Custom Basket Code LEI. Validation against 
GLEIF will be done but it can be of any 
status 
 
If LEI is reported for Other payment payer 
and Other payment receiver, LEI will be 
validated against GLEIF but it can be of any 
status 
 
Details are covered in the ASIC Message 
Specifications 
If LEI is reported for Clearing [[Member]], LEI will 
be validated against GLEIF and the GLEIF 
registration status must be either Issued, 
Lapsed, Pending transfer, Pending archival. 
 
LEI is mandated for Clearing [[Member]] and 
Custom Basket Code LEI. Validation against 
GLEIF will be done but it can be of any status 
 
If LEI is reported for Other payment payer and 
Other payment receiver, LEI will be validated 
against GLEIF but it can be of any status 
 
Details are covered in the MAS Message 
Specifications 
UTI UTI will be mandated for new trades. The trade linking logic will only be based on UTI +Trade 
Party 1. USI and the Transaction [[ID]] fields will be retired and removed from the trade linking 
logic.   
ISO XML ISO XML will be mandated for all inbound messages starting 21 October, 2024. ISO XML 
schema does not support cross jurisdiction reporting. [[DTCC]] XML will not be supported. 
ASIC and MAS Usage Guidelines have been published.  
FPML FpML will be decommissioned with the mandate of ISO XML. We will no longer support FpML 
for ASIC and MAS reporting. 
For cross jurisdiction reporting with jurisdictions who continue to accept FpML, submissions will 
need to be made separately. 
CSV CSV submissions will be decommissioned with the mandate of ISO XML. We will no longer 
support CSV for ASIC and MAS reporting. 
This includes both the Harmonized and [[OTC]] Legacy submission templates. 
For cross jurisdiction reporting with jurisdictions who continue to accept CSV, submissions will 
need to be made separately. 
Trade Linking Logic The trade linking logic will only be based on UTI + Trade Party 1 for new trades. For legacy 
trades, it will be Proprietary UTI + Trade Party 1.   
Data Migration A limited Data Migration exercise is expected from DDRS. The migration details will be covered 
on a separate document.   
Message 
Specifications 
There will be changes to the way existing fields are supported and ingested. 
The Message Specifications will support the requirements of the new regulations. 
Message Types Trade State, Valuations and [[Margin]] Valuation message will be supported via Action Type Rules 
Reports Outbound to the regulator is XML format. For the users, it will be CSV reports. Users will 
receive CSV as [[default]] though there may be exceptional cases where the users need both, and 
users can configure to [[DO]] so via the reports management tool 

---

## Page 10

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
PAGE 10 
 
Action Type / Event 
Type Rules 
Action Type/Event Type Rules will be newly implemented 
Out of Scope 
This project will not include: 
• Fee Schedule Pricing Changes which will be reviewed at a future date.  
  

---

## Page 11

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
PAGE 11 
 
Reference Documents  
This document should be read in conjunction with the following documents: 
1. The Message Specifications for both jurisdictions and all other documents related to this implementation 
will be available on the “Upcoming Changes” section under the ASIC & MAS Re-Write of the GTR 
Learning Center. 
2. Usage Guidelines for each jurisdiction and other published regulations/documentation 
Naming Conventions and Definitions 
Abbreviation/ 
Term Name 
Definition/Description 
ACK GTR Success Acknowledgement Message 
ASIC Australian [[securities]] & Investments Commission 
ANNA-DSB Association of National Numbering Agencies (ANNA) - [[Derivatives]] Service Bureau (DSB) 
CDE Critical Data Elements 
Channel A unidirectional link between two end points or queue managers that serves to transfer 
messages 
CSV Comma Separated Values – a submission format accepted for messages in GTR 
[[DTCC]] The Depository Trust and Clearing Corporation 
ERR Entity Responsible for Reporting – A CDE field.  
In ASIC, the field equivalent to ERR is Reporting Entity. In MAS, the field equivalent to ERR 
is Report Specified Person 
FpML Financial Product Markup Language – XML based submission type for the GTR and Canada 
PPD 
GTR Global Trade Repository 
GUI Graphical User Interface 
LEI Legal Entity Identifier 
MAS Monetary Authority of Singapore 
Message 
Specification 
Instructions for submitting into a given GTR application. Includes data attribute requirements, 
valid values, validations, CSV submission layouts and parsing definitions. This document can 
be found on the Learning Center. 
MQ Message Queue – message-oriented middleware. Provides mechanism for applications to 
communicate. 
NACK GTR Negative Acknowledgement message 
O-Code Operations Code – used to segregate and permission accounts 
OurRef Short for Our Reference, and referring to Trade Party 1 Transaction [[ID]] and Trade Party 2 
Transaction [[ID]] 

---

## Page 12

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
PAGE 12 
 
OCP Other Counterparty (also referenced as Trade Party 2 generically) 
RCP Reporting Counterparty (also reference as Trade Party 1 generically) 
RSE A CDE field – Report Submitting Entity  
In ASIC, the field equivalent has the same field name. In MAS, the field equivalent to RSE is 
Data Submitter 
SDO Account Management System that [[DTCC]] uses to define accounts, products and services 
associated with these participants 
SDR Swap Data Repository 
sFTP Secure File Transfer Protocol 
Trade State Trade state is the latest trade message that has been received and processed by GTR. 
TSR Trade State Report. Daily report of all open [[Derivatives]] transactions (with latest valuation 
information merged onto the report). 
UAT GTR Test Environment (“User Acceptance Testing”) 
UPI Unique Product Identifier 
USI Unique Swap Identifier 
UTI Unique Trade Identifier 
XML In this document, refers to ISO 20022 XML 
 
  

---

## Page 13

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
PAGE 13 
 
2. FUNCTIONAL CHANGE REQUIREMENTS 
FC 1: Connectivity: Message Channel, Routing and Submission 
Methods  
There will be no changes to the current submission channels and methods supported by the GTR. The GTR 
will continue to offer users the ability to connect to the application through the same channels or protocols to 
submit or receive data namely, web portal, MQ and sFTP. 
The ISO XML message does not support a Service destination / Reporting Obligation field; therefore, routing 
will be determined from the following three sub-points and each jurisdiction will have separate inbound product 
IDs / queues. 
(i) The web upload feature that is offered through the Portal / GUI will only support direct upload to the 
jurisdiction service that the user selects on the screen. 
(ii)  The dedicated sFTP product [[ID]] for ASIC & MAS will determine the destination / jurisdiction service where 
the GTR must send the file. These product IDs will be newly setup for the re-writes and require new 
subscriptions to be setup by reporting firms. 
(iii) The dedicated message queue will determine the destination / jurisdiction service where the users must 
send the message to. The queue details are provided below. 
Further description of the current functionality can be found on the Learning Center in the Connectivity section: 
Refer here for the Learning Centre connectivity documentation page. Overall requirements will be found in the 
Learning Center.   
Specific connectivity details regarding the ASIC and MAS Rewrite can be found in the starter pack including 
onboarding details, report product IDs and connectivity guidance.  
• GTR Rewrites and Refit sFTP Connectivity Client Pack 
• GTR Rewrites and Refit MQ Connectivity Client Pack 
There will be a parallel UAT environment for ASIC and MAS post go-live of the ASIC and MAS Rewrite UAT 
environment. There will be no change to that for users with existing sFTP and MQ connectivity as the existing 
connection setups can be leveraged for legacy submissions. 
However, users with existing SFTP connection to [[DTCC]] Mainframe system will require to make a separate 
SFTP connection to [[DTCC]] Distributed system. 
For any connectivity questions, please contact GTRConnectivity@[[DTCC]].com or submit a query via the 
Connectivity Support tile in the MyDTCC portal. 
 

---

## Page 14

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
PAGE 14 
 
FC 1.1: MQ Connectivity 
Clients who report via MQ will need to target new queues dedicated for ASIC and MAS Rules Rewrite using 
the dynamic queue functionality provided on the MQ header. It should be noted that users will be required to 
target new input queues. Please refer to the Connectivity Starter Pack available on the Learning Center.  
For reference the new ASIC and MAS Input queues have been outlined below:  
ASIC RDS MQ Input Queues 
[[Asset]] Class/Product RDS Sub-
Services 
Queue 
Manager [[DTCC]] Input Queue Name Description 
Commodity ASIC MU1R, MP1R GTR.ASIC_COMMODITY.A01 [[DTCC]] input queue for ASIC 
(Re-Write) 
Credits ASIC MU1R, MP1R GTR.ASIC_CREDITS.A01 [[DTCC]] input queue for ASIC 
(Re-Write) 
[[Equity]] ASIC MU1R, MU2R, 
MP2R GTR.ASIC_EQUITY.A01 [[DTCC]] input queue for ASIC 
(Re-Write) 
FX ASIC MU1R, MP5R-
MP9R GTR.ASIC_FX.A01 [[DTCC]] input queue for ASIC 
(Re-Write) 
Rates ASIC MU1R, MP1R GTR.ASIC_RATES.A01 [[DTCC]] input queue for ASIC 
(Re-Write) 
[[Margin]] Activity Submission ASIC MU1R, MP1R GTR.ASIC_MARGIN.A01 [[DTCC]] input queue for ASIC 
(Re-Write) 
 
MAS RDS MQ Input Queues 
[[Asset]] Class/Product RDS Sub-
Services 
Queue 
Manager 
[[DTCC]] Input Queue 
Name Description 
Commodity MAS MU1R, MP1R GTR.MAS_COMMODITY.A01 [[DTCC]] input queue for MAS 
(Re-Write) 
Credits MAS MU1R, MP1R GTR.MAS_CREDITS.A01 [[DTCC]] input queue for MAS 
(Re-Write) 
[[Equity]] MAS MU1R, MU2R, 
MP2R GTR.MAS_EQUITY.A01 [[DTCC]] input queue for MAS 
(Re-Write) 
FX MAS MU1R, MP5R-
MP9R GTR.MAS_FX.A01 [[DTCC]] input queue for MAS 
(Re-Write) 
Rates MAS MU1R, MP1R GTR.MAS_RATES.A01 [[DTCC]] input queue for MAS 
(Re-Write) 
[[Margin]] Activity Submission MAS MU1R, MP1R GTR.MAS_MARGIN.A01 [[DTCC]] input queue for MAS 
(Re-Write) 
 
FC 1.2: sFTP Connectivity 
There will be a suite of new report Product IDs that must be provisioned to allow users to submit into the GTR. 
Additionally, there is a suite of new outbound reporting product IDs that must be provisioned to allow GTR 
users to receive reports via sFTP. Please refer to the Connectivity Starter Pack available on the [[DTCC]] 
Learning Center for more details. 
A summary of the sFTP product IDs is provided below where the report IDs in green and denoted with an 
asterisk are for Production.  UAT product IDs are prefixed with 298 instead of 250. 
 

---

## Page 15

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
PAGE 15 
 
ASIC 
Schema Description Format [[Margin]] Commodity Credit [[Equity]] Rates FX 
auth.030.001.03_ASICUG_DATTAR_1.0.0 ASIC Trade Activity Submission 
XML ISO20022XML   60988 
auth.108.001.01_ASICUG_DATMDA_1.0.0 ASIC [[Margin]] Activity Submission 
XML ISO20022XML 60989   
auth.031.001.01_ASICUG_FDRES_1.0.0 ASIC GTR Batch ACK/NACK 
Report XML ISO20022XML 2503250* 
auth.030.001.03_ASICUG_DATTAR_1.0.0 ASIC Trade Activity Report XML ISO20022XML   2503251* 
auth.107.001.03_ASICUG_TRADTSR_1.0.0 ASIC Trade State Report XML ISO20022XML   2503252* 
auth.108.001.01_ASICUG_DATMDA_1.0.0 ASIC [[Margin]] Activity Report 
XML ISO20022XML 2503253*   
auth.109.001.01_ASICUG_DATMDS_1.0.0 ASIC [[Margin]] State Report XML ISO20022XML 2503254*   
auth.030.001.03_ASICUG_DATTAR_1.0.0 ASIC Trade Activity Report CSV CSV equivalent   2503255* 
auth.107.001.03_ASICUG_TRADTSR_1.0.0 ASIC Trade State Report CSV CSV equivalent   2503256* 
auth.108.001.01_ASICUG_DATMDA_1.0.0 ASIC [[Margin]] Activity Report 
CSV CSV equivalent 2503257*   
auth.109.001.01_ASICUG_DATMDS_1.0.0 ASIC [[Margin]] State Report CSV CSV equivalent 2503258*   
N/A ASIC [[Margin]] Submission Report 
CSV CSV only 2503259*   
N/A ASIC Daily Submission Report 
CSV CSV only  2503260* 
N/A ASIC [[EOD]] Allege Report CSV CSV only  2503261* 
N/A ASIC Intraday Allege Report 
CSV CSV only  2503262* 
auth.030.001.03_ASICUG_DATTAR_1.0.0 ASIC Regulator Trade Activity 
Report XML ISO20022XML   2503263* 
auth.107.001.03_ASICUG_TRADTSR_1.0.0 ASIC Regulator Trade State 
Report XML ISO20022XML   2503264* 
auth.108.001.01_ASICUG_DATMDA_1.0.0 ASIC Regulator [[Margin]] Activity 
Report XML ISO20022XML 2503265*   
auth.109.001.01_ASICUG_DATMDS_1.0.0 ASIC Regulator [[Margin]] State 
Report XML ISO20022XML 2503266*   
 
 
  

---

## Page 16

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
PAGE 16 
 
MAS
Schema Description Format [[Margin]] Commodity Credit [[Equity]] Rates FX 
auth.030.001.03_MASUG_DATTAR_1.0.0 MAS Trade Activity Submission 
XML 
ISO20022XML   60997 
auth.108.001.01_MASUG_DATMDA_1.0.0 MAS [[Margin]] Activity Submission 
XML 
ISO20022XML 60998   
auth.031.001.01_MASUG_FDRES_1.0.0 MAS GTR Batch ACK/NACK 
Report XML 
ISO20022XML 2503270* 
auth.030.001.03_MASUG_DATTAR_1.0.0 MAS Trade Activity Report XML ISO20022XML   2503271* 
auth.107.001.03_MASUG_TRADTSR_1.0.0 MAS Trade State Report XML ISO20022XML   2503272* 
auth.108.001.01_MASUG_DATMDA_1.0.0 MAS [[Margin]] Activity Report 
XML 
ISO20022XML 2503273*   
auth.109.001.01_MASUG_DATMDS_1.0.0 MAS [[Margin]] State Report XML ISO20022XML 2503274*   
auth.030.001.03_MASUG_DATTAR_1.0.0 MAS Trade Activity Report CSV CSV equivalent   2503275* 
auth.107.001.03_MASUG_TRADTSR_1.0.0 MAS Trade State Report CSV CSV equivalent   2503276* 
auth.108.001.01_MASUG_DATMDA_1.0.0 MAS [[Margin]] Activity Report 
CSV 
CSV equivalent 2503277*   
auth.109.001.01_MASUG_DATMDS_1.0.0 MAS [[Margin]] State Report CSV CSV equivalent 2503278*   
N/A MAS [[Margin]] Submission Report 
CSV 
CSV only 2503279*   
N/A MAS Daily Submission Report 
CSV 
CSV only   2503280* 
N/A MAS [[EOD]] Allege Report CSV CSV only  2503281* 
N/A MAS Intraday Allege Report 
CSV 
CSV only  2503282* 
auth.030.001.03_MASUG_DATTAR_1.0.0 MAS Regulator Trade Activity 
Report XML 
ISO20022XML   2503283* 
auth.107.001.03_MASUG_TRADTSR_1.0.0 MAS Regulator Trade State 
Report XML 
ISO20022XML   2503284* 
auth.108.001.01_MASUG_DATMDA_1.0.0 MAS Regulator [[Margin]] Activity 
Report XML 
ISO20022XML 2503285*   
auth.109.001.01_MASUG_DATMDS_1.0.0 MAS Regulator [[Margin]] State 
Report XML 
ISO20022XML 2503286*   

---

## Page 17

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 17 
FC 2: Ingestion – Message Types and Submission Formats 
FC 2.1: Inbound Message Types and Submission Formats 
The following message types are allowed, utilizing the inbound submission formats in this table. Note that 
[[Asset]]-class based Legacy CSV message formats will no longer be supported. 
ASIC 
 
MAS 
Message Type Schema Requirements 
Transaction (Trade State) XML - auth.030.001.03_MASUG_DATTAR_1.0.0 
Valuation XML - auth.030.001.03_MASUG_DATTAR_1.0.0 
[[Margin]] XML - auth.108.001.01_MASUG_DATMDA_1.0.0 
 
Legacy CSV templates & FpML for Trade State submissions will no longer be supported.  
The [[DTCC]] Message Specifications contain the detailed formats for each of the data fields, the business rules 
and the XML x-paths details. 
Usage Guidelines will supplement the Message Specifications and illustrate the data field requirements, 
including formats and enumerations that users must adhere to.  
[[DTCC]] will support submissions via the Portal web upload, MQ and sFTP. File based web upload or sFTP 
submissions will allow for multiple records within a file, however MQ submissions will be based on single 
record per message. Message sample formats for ASIC can be found here. For MAS, it will be shared in the 
Learning Center when available. 
 
 
 
Message Type Schema Requirements 
Transaction (Trade State) XML - auth.030.001.03_ASICUG_DATTAR_1.0.0 
Valuation XML - auth.030.001.03_ASICUG_DATTAR_1.0.0 
[[Margin]] XML - auth.108.001.01_ASICUG_DATMDA_1.0.0 

---

## Page 18

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 18 
FC 2.2: Special Characters 
All submissions should limit their character sets to UTF-8.   
Generally, the ISO schema expects that all characters should be alphanumeric. Unless explicitly mentioned, 
fields are generally alphanumeric unless otherwise explicitly mentioned in the message specifications. [[DTCC]] 
will implement validations in this regard as per the Message Specifications and Usage Guidelines.  
FC 2.3: Message Header Format 
Each submission must follow a prescribed header format. Otherwise, the entire file or message would be 
rejected. The samples which will be published on the Learning Centre shows the relevant tags that would be 
required. The table below shows the header elements, definition, xpaths and sample values.  To prevent 
unauthorized submissions to incorrect entities, the validations include the following: 
(a) For SFTP mode, GTR will validate the o-code present in sftp filename against the AppHdr o-code, and 
if there is a mismatch in the o-code, a file reject would occur.  
(b) For Web portal submissions, GTR will validate the o-code user select while uploading their 
submissions in the portal with AppHdr o-code, and if there is a mismatch in the o-code, a file reject 
would occur. 
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

---

## Page 19

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 19 
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
01.02 DDRS 
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
For ASIC 
auth.030.001.03_ASI
C_DATTAR_1.0.0 
 
For MAS 
auth.030.001.03_MA
S_DATTAR_1.0.0 
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
 
 
 
 
 
 
 
 
 
 

---

## Page 20

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 20 
 
“Hdr” 
 
 
“Pyld” 
 
 
The o-code indicated in the “From” tag in the message header will be checked against each submitted record’s 
“SubmitgAgt” tag to ensure the record submitted is valid and to prevent unauthorized submissions of 
accidentally submitting on behalf of some other entity that does not correspond to the  header submitter details. 
FC 3: Ingestion - Processing of Submissions 
FC.3.1: Message Validations  
Although there are significant changes to the specific validations required based on the new ASIC & MAS Re-
write regulations, there will be no changes to the [[BASIC]] process by which messages are validated for reporting. 
The validation process includes: 
• File level Schema Validation validates that the message is formatted correctly so that it can be parsed . 
Your submission will be validated at the message level and the detail records if there are multiple records 
within a file. An example of a CRPT file level reject is an incorrect or incomplete headers GTR would not 
validate at the record level if the file is corrupted. Examples of these scenarios are : 


---

## Page 21

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 21 
(a) BizData header is missing / malformed. Refer to FC 2.3 for the header requirements  that will cause a 
full file rejection 
(b) MQ submissions containing > 1 activity (/Rpt Blocks) 
(c) sFTP submissions containing > 100k activities (/Rpt Blocks) 
The error code would be at message status level. 
 
Message Status 
CodeName Name Definition 
ACPT Accepted Whole message has been accepted. 
CRPT CorruptedFile File containing the report is corrupted. 
 
Another example of a schema rejection occurs at the record level (trade level). For example, if an optional 
field is submitted with the XML tag but with the value as blank, the message will be schema rejected. To 
pass the schema validation, the entire XML tag must be removed for optional fields unless a value is also 
submitted to accompany the XML tag. These would be validated at each record level. 
 
Detailed Status 
CodeName Name Definition 
ACPT Accepted Record has been accepted. 
RJCT Rejected Record has been rejected. 
 
• Permission Validation (validates that the submitter has permission to submit the message) 
• Core Validation ([[BASIC]] global validations of key fields as defined in the Message Specifications  and Usage 
Guidelines). For example, a data type of Num(31,13) allows for up to 18 numeric values prior to the 
decimal and up to 13 numeric values after but only 18 digits in total. This equivalent to (18,13) in CDE & 
ISO XML. Assuming a submitted value is '11111111111111.1100000000000', this will be rejected as the 
total is 27 digits. If the user omits the trailing zeros and submits '11111111111111.11', then it will be 
accepted. 
• Jurisdictional Validation (validations specific to each jurisdiction as defined in the Message Specifications  
and Usage Guidelines) 
 
The below diagram illustrates the common message validation process.  

---

## Page 22

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 22 
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
There will be no changes to the way messages are processed in the GTR in terms of sequencing. If messages 
related to the same trade are submitted in sequence within the same cha nnel or file (MQ or sFTP or Web 
Upload), [[DTCC]] will process those messages in the order received. Sequencing cannot be guaranteed when 
messages related to the same trade are submitted across these channels. For users who may have multiple 
connections to the same sFTP site and intend to send files in quick succession, they are recommended to use 
the same connection or otherwise wait till an acknowledgement is received before sending another file in from 
a different connection. 
With the implementation of Action Type sequencing rules (see section FC 3.8), it is especially important that 
the users consider and factor in what and when to send messages based on Action Type.  
Please note that message responses over MQ may be returned in a different sequence than the original 
submission due to load balancing functions in the GTR. This does not mean that the messages have been 
processed out of sequence. 
FC 3.3: Trade Identifiers  
A UTI is required for all new trades submitted for ASIC & MAS reporting after the go-live (using Action Type 
“NEWT”). No special characters are allowed, and UTI must be within 52 alphanumeric characters for future 
reporting. 
For trades remain live at the Re-Write go-live, the Primary Key will be migrated to Proprietary [[ID]] tag. The 
Primary Key is the first of either the UTI or USI or TID in that order that is populated in the [[participant]] Trade 
State reports. Proprietary identifier should be used to update outstanding trades post rewrite. For example, 
when firms want to modify their existing trade, the Prtry/[[ID]] tag should be used. Global UTI tag of UnqTxIdr 
should be used for new trades post go live. Please note the difference in format requirements for each tag. 

---

## Page 23

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 23 
However, a termination and resubmission is required if the Primary Key doesn’t meet the Global UTI format, 
otherwise reporting entities can continue to submit such trades via the Prtry/[[ID]] tag. 
DDRS will perform an exercise to identify the existing trade identifiers with ampersand “&” and those identifiers 
that will not be able to fit into the Proprietary [[ID]] tag of 72 characters limitation and perform an outreach 
regarding such positions. 
Validations performed will be as defined in the Message Specifications. 
FC 3.4: Uniqueness of a Trade  
Currently, trade uniqueness is defined as follows: 
• For current reporting, the uniqueness of a trade follows a waterfall logic where UTI + Trade Party 1 + 
Trade Party 2 is the primary consideration for trade uniqueness followed by USI + Trade Party 1 + Trade 
Party 2 followed by OurRef + Trade Party 1 + Trade Party 2. 
With the ASIC & MAS Re-Write implementation, trade uniqueness in the GTR will be simplified as follows:  
• The uniqueness of a trade will be determined by the concatenation of UTI or Proprietary Identification + 
Trade Party 1 
• For brevity, the remainder of this document will use “UTI + RCP” to reference this uniqueness. 
This change will require the removal of “duplicate” trades, where there may be the same values for (UTI + USI 
+ OurRef) + RCP 1 and “UTI + USI + OurRef” + RCP 2. Firms need to review their existing Position Reports for 
such trades and exit the appropriate trades prior to go-live and DDRS Operations staff will reach out to users 
bilaterally regarding such positions.  If this clean-up is not performed, [[DTCC]] will choose the most recently 
updated trade to carry forward and discontinue reporting of other duplicate trades with the same (UTI + USI + 
OurRef) + RCP 1.  
This functionality change has implications for how users will manage changes to the counterparty of a trade 
that will be different than today.  Please see section 3.11 for further details. 
FC 3.5: [[Margin]] Message Submissions 
[[Margin]] reporting will be introduced for MAS reporting. ASIC currently requires [[BASIC]] [[collateral]] reporting. 
Submissions 
• [[Margin]] submissions must minimally satisfy the auth.108.001.01_ASICUG_DATMDA_1.0.0 or 
auth.108.001.01_MASUG_DATMDA_1.0.0 xml schema for the respective jurisdictions. Failure to adhere 
to the schema requirements will result in the message being rejected upfront.  
For example, if the user submits a MARU action type and indicate economic fields such as Fixed Rate or 
Expiration Date, then the message will be rejected. 
• [[Margin]] messages must be submitted in XML format and via the o-code “0xxx”. (Details on the validations 
can be found in the Message Specifications). Message samples will also be provided once available.  
• These messages can be submitted via Web Upload, sFTP and MQ 

---

## Page 24

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 24 
• [[Margin]] messages are distinguished by the Action Type value of “MARU” in the submission.  
• Corrections can be made to previously reported [[Margin]] messages with Action Type value of “CORR”. 
However, the first submission to an auth.108 cannot be a “CORR” action type. 
• Submission permissions will work the same as for all other message types.  
• Validations will be performed as specified in the Message Specifications. 
Trade Level or Portfolio Level [[Margin]]  
• [[Margin]] valuation is either at Trade Level or Portfolio Level.   
• For Trade Level [[Margin]] Valuations: 
o Trade-level [[Margin]] messages must contain a UTI and will only be accepted if there is a base trade 
which matches the [[Margin]] valuation submission (UTI + RCP + OCP must match).  The base trade 
must be “Open”, “Terminated”, or “Expired”.  If there is no base trade or the status of the base trade 
is not “Open”, “Terminated” or “Expired”, the message with be rejected 
o Trade-level [[Margin]] messages submitted on trades that have been “Errored” (action type EROR) or 
“Transferred Out” (action type PRTO) will be rejected (NACK-ed). 
o [[collateral]] Portfolio Indicator must be derived as “false” so that UTI can be populated. 
o One of Initial [[Margin]] [[collateral]] Portfolio Code or Variation [[Margin]] [[collateral]] Portfolio code must be 
submitted on both the auth.030 and auth.108 messages after 21 October 2024. If the [Initial [[Margin]] 
[[collateral]] portfolio code] is not applicable to your trade, users should submit the value [NOAP] to 
represent "Not Applicable" 
 
• For Portfolio-level [[Margin]] Valuations: 
o Two portfolio codes are defined (Initial [[Margin]] [[collateral]] Portfolio Code & Variation [[Margin]] [[collateral]] 
Portfolio Code).  At least one of these must be populated on each [[Margin]] message if [[collateral]] 
Portfolio Indicator is derived as “true” 
o If the [Variation [[Margin]] [[collateral]] portfolio code] is not applicable to your trade, clients could submit 
the value [NOAP] to represent "No Applicable" in "/NoPrtfl" XML. 
o Portfolio-level [[Margin]] messages will be validated for the existence of one or more underlying trades 
which contain the given Initial [[Margin]] Portfolio Code and/or Variation [[Margin]] Portfolio Code.  (Initial 
and/or Variation [[Margin]] Portfolio Codes + RCP + OCP must match) 
o As it is required that either one of Initial [[Margin]] Portfolio Code & Variation [[Margin]] [[collateral]] Portfolio 
Code for portfolio-based [[Margin]] reporting, the ingestion validation lookup to the existence of at least 
one underlying trade will be on the basis of the concatenated value of both the portfolio codes on the 
MARU message against the base trade. 
 
New “0” o-codes (0ABC) will be configured to support [[Margin]] reporting, though this should already be setup for 
clients who are reporting to ASIC today. (it is not [[Asset]]-class aligned, so will not naturally fit with existing user 
o-codes).   
[[Margin]] valuation submission information will not be merged onto the Trade State Report but will be reported on 
an [[EOD]] [[Margin]] Submission Report, [[Margin]] Activity Report and [[Margin]] State Report.  For further information 
on [[Margin]] valuation reporting, please refer to the Reporting section of this document (FC 5 Reports). 

---

## Page 25

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 25 
FC 3.6: Trade Valuation Submissions 
Trade Valuation messages are applicable for ASIC & MAS reporting. 
Trade Valuations need to be submitted to the GTR daily through a Valuation message indicated by Action Type 
“VALU” 
Valuations will only be accepted if there is a base trade which matches the valuation submission (UTI + RCP + 
OCP). Any valuation submitted on a position without a base trade will be rejected (NACK -ed). 
Valuations that are submitted on inactive trades (Expired or Terminated) will be accepted. In this scenario the 
valuation submission will be reported as activity in the [[EOD]] Activity Report but will not be reported on Trade 
State Reports for both the regulators and participants.  
As per the Message Specifications, valuations submitted on trades that have been Errored (action type EROR) 
or Transferred Out (action type PRTO) will be rejected. (NACK-ed) 
FC 3.7: Reporting Counterparty and Entity Responsible for Reporting  
The Entity Responsible for Reporting (ERR) is newly introduced as part of the Re-writes.  
Note: In the table below, there are some common fields that are used by both ASIC and MAS but have 
different names in the different jurisdiction rules. We will be using the harmonized field names to refer to the 
fields in this document for simplicity. 
Harmonized field ASIC MAS 
Entity Responsible for 
Reporting (ERR) 
Reporting Entity  
Current LEI of the Reporting Entity. 
Report Specified Person 
Identifier of the specified person with 
the reporting obligation in respect of 
the contract 
Report Submitting 
Entity (RSE) 
Report Submitting Entity 
The LEI of the person submitting 
the report of a Reportable 
Transaction. 
Data Submitter 
Identifier of the entity submitting 
information on the contract, which is 
reported to a licensed trade repository 
or licensed foreign trade repository. 
 
The ERR and the RCP must have a valid renewed LEI in GLIEF which is validated at the point of submission. 
Both the RSE and the ERR must be an active account onboarded in SDO for ASIC and MAS reporting. At the 
point of ingestion, a validation rule will be executed to check that RSE has permission to report for ERR. The 
permission is required to be set in Manage Services if RSE is not the same as ERR . If it is found that RSE has 
no permission to report for ERR, the submissions will be NACK-ed. 
However, this condition will not be triggered if RSE is the same as ERR. 

---

## Page 26

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 26 
Also, a third-party service provider cannot be named as the Reporting Counterparty in all submissions. Such 
submissions regardless of Action Type will be NACK-ed.  
FC 3.8: Execution Agent of Counterparty 1  
Execution Agent is available as an ASIC data field in the upcoming ASIC Re-write.  
MAS did not include this field in the close to final rules however it will be included as an optional field in MAS 
Rewrite Message Specifications as a business requirement from industry and DDRS. 
FC 3.9: Action Type and Event Type Validations  
Submissions received after go-live must contain the relevant “Action Type” and “Event Type” values.  These 
values must pass both “stateless” validations (i.e. validations that can be performed solely based on the 
content of the message) as well as “stateful” validations (i.e. validations that can only be performed by 
referencing previous submissions for the same trade).  
The “Action Type” values for ASIC and MAS are largely the same other than “PRTO” which is not in the list for 
Allowed Valid Values for MAS. 
“Stateless” Validations 
These validations restrict the valid combinations of the “Action Type”, and “Event Type” fields. The Message 
Specifications contain a tab called “Action type & Event type” which details the valid combinations of these 
fields for all messages. As these combinations can be validated solely based on content of the message, they 
can be tested using the Simulator.   
“Stateful” Validations 
These validations control the allowable sequences of Action Types. Each new submission will be validated to 
confirm that the action type is consistent with the allowable sequence as per the action type state diagrams 
below. These validations will be performed per unique trade (see Trade Uniqueness section 3.4) + per 
Jurisdiction. The latest version of these diagrams will always be contained in the Message Specifications. 
Some main points are described below. Note that both jurisdictions will follow the ESMA approach for 
consistency. 
• The first submission for a trade must be NEWT.  
• No submission is required to Expire a trade.  An end-of-day process will remove expired trades from the 
Trade State Report (TSR) on the day after expiration date (as it does currently for ASIC & MAS 
reporting).  In the state diagram below, this process will logically move trades from “Outstanding” to 
“Expired” status.  
• MODI, CORR, VALU, and MARU submissions to terminated trades are allowed. This is to allow reporting 
entities to submit historical modifications, corrections, valuations and [[Margin]] information for terminated 
trades. Submitters are responsible for ensuring relevant dates are accurate and information submitted is 
correct. Trade linkage for MODI and CORR will be on the basis of UTI + RCP.  

---

## Page 27

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 27 
• There would not be any validation on the data fields being submitted and it is possible that OCP could be 
changed on a terminated trade prior to submitting a REVI. However on the REVI submission, the OCP 
cannot be amended, and it would be necessary to submit the last accepted UTI + RCP + OCP. All other 
fields are allowed to be amended on the REVI as long as they are applicable as indicated on the Message 
Specifications.    
• When a trade is successfully submitted for a TERM, EROR, or PRTO, it will not appear on the Trade State 
Report on the Report Date of the corresponding submission.  Once a trade status Terminated or Errored, 
the only way for it to appear again on the TSR is to submit a REVI message with a future expiration date. 
A TERM or REVI submission will be validated on the basis of an existing base trade with the same UTI + 
RCP + OCP 
• A REVI with a future expiration date on a Terminated or Errored status will bring the trade status to 
“Outstanding” while a REVI with past expiration date keeps the status as “Terminated”. 
• TERM submissions to expired trades is allowed. 
• Firms can submit CORR after a REVI to change other fields thereafter including OCP .  
• VALU and MARU linkage to the base trade position will be on the basis of UTI + RCP + OCP 
• [[Margin]] Update linkage to the derivative that was reported depends on how the derivative is collateralized:  
(a) If the trade is not collateralized as part of a portfolio (derivative based) – the submission will have UTI 
and the linkage will be UTI + RCP + OCP. If there is no base trade, then the MARU message must be 
rejected 
(b) If the trade is collateralized as part of a portfolio – the submission will have Initial and/or Variation 
[[Margin]] [[collateral]] Portfolio Codes so the linkage will be Initial and/or Variation [[Margin]] Portfolio Codes 
+ RCP + OCP. There must be at least one active UTI in the portfolio for the MARU message to be 
accepted.  
  
Note that the linking does not refer to actual linking of the [[Margin]] values to the Trade State Report but 
guidance for how you perform reconciliations from the [[Margin]] State Reports to the Trade State Report  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 28

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 28 
ASIC 
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 


---

## Page 29

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 29 
MAS
 
Some use case examples are provided below.  
 
Scenario Sub
# 
Action 
Type 
Event 
Type UTI RCP OCP Validation Expected 
Result Comments 
UC1 
1 NEWT TRAD 123 Bank A Bank B UTI + RCP ACK   
2 MODI TRAD 123 Bank A Bank B UTI + RCP ACK Post Trade for the same 
UTI and OCP should ACK 
as linking is by UTI + 
RCP 
UC2 
1 NEWT TRAD 123 Bank A Bank B UTI + RCP ACK   
2 MODI TRAD 123 Bank A Bank C UTI + RCP ACK Post Trade for the same 
UTI even if OCP is 
different it should ACK as 
linking is by UT I+ RCP 


---

## Page 30

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 30 
UC3 
1 NEWT TRAD 123 Bank A Bank B UTI + RCP ACK   
2 MODI TRAD 123 Bank B Bank A UTI + RCP NACK Post Trade cannot be 
submitted without a base 
trade 
UC4 
1 NEWT TRAD 123 Bank A Bank B UTI + RCP ACK   
2 TERM ETRM 123 Bank A Bank B UTI+RCP+OCP ACK Post Trade for the same 
UTI and OCP should ACK 
as linking is by 
UTI+RCP+OCP 
3 REVI* NA 123 Bank A Bank B UTI+RCP+OCP ACK Post Trade for the same 
UTI and OCP should ACK 
as linking is by 
UTI+RCP+OCP 
UC5 
1 NEWT TRAD 123 Bank A Bank B UTI + RCP ACK   
2 TERM ETRM 123 Bank A Bank B UTI+RCP+OCP ACK   
3 REVI* NA 123 Bank A Bank C UTI+RCP+OCP NACK Post Trade for the same 
UTI even if OCP is 
different it should NACK 
as linking is by 
UTI+RCP+OCP 
UC6 
1 NEWT TRAD 123 Bank A Bank B UTI + RCP ACK   
2 TERM ETRM 123 Bank A Bank B UTI+RCP+OCP ACK   
3 REVI* NA 123 Bank B Bank A UTI+RCP+OCP NACK Post Trade cannot be 
submitted without a base 
trade 
 
ASIC and MAS will primarily follow what was consulted in the CDE Consult published in August 2022 which 
states the following definitions 
 
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

---

## Page 31

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 31 
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
Note: Not applicable for MAS 
 
For trades that are already “live” when the ASIC and MAS Rules Rewrite are implemented, [[DTCC]] will initialize 
the state of the trade during go-live weekend such that post go-live submissions will be accepted according to 
these action type validations.  This logic is described further in Section 6 of this document.  
FC 3.10: Submissions with Reduced Validations  
After the ASIC & MAS Rules Rewrite, some submissions (with action type = TERM, EROR, PRTO) will 
continue to have reduced validations.  While these action types use the same schema for validation as 
submissions with Action type = NEWT or MODI, the message does not undergo the same validation for several 
fields. Details are contained in the Message Specifications.  
FC 3.11: Change of Counterparty 
In the current ASIC & MAS GTR application, given the trade uniqueness follows a waterfall logic where UTI + 
Trade Party 1 + Trade Party 2 is the primary consideration for trade uniqueness followed by USI + Trade Party 
1+ Trade Party 2 followed by OurRef + Trade Party 1 + Trade Party 2, a trade must be exited and resubmitted 
to change the Counterparty (Trade Party 2) on the trade. This resubmission is allowed to retain the original USI 
in the current application. 
• With the change to Trade Uniqueness as part of the Re-writes, both submissions with either Action Type 
CORR with different TP2 from the NEWT submission will be possible if TP2 was reported erroneously 
 
 
 
 
 

---

## Page 32

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 32 
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
3 CORR TRAD 123 Bank A Bank A Bank C ACK Change of OCP allowed with  
same UTI + RCP 
4 NEWT TRAD 123 Bank B Bank B Bank A NACK NEWT already exists for  
UTI + RCP and submission  
#2 and #4 are the same, so 
two consecutive NEWTs are  
not allowed 
 
Use Case 2 
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
3 TERM NOVA 123 Bank A Bank A Bank B NACK Termination cannot occur because 
trade is no longer active 
4 NEWT TRAD 123 Bank A Bank A Bank B NACK UTI Technical guidance states that 
UTI cannot be re-used even if the 
previous use was on a transaction 
that is no longer open  
FC 3.12: Change of Reporting Counterparty 
In the current application and the future post re-writes application, a trade must be exited and resubmitted to 
change the Reporting Party (Trade Party 1) on the trade.  
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

---

## Page 33

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 33 
2 TERM/EROR - 123 Bank A Bank A Bank B ACK   
3 NEWT TRAD 123 Bank C Bank C Bank B NACK UTI Technical guidance states that 
UTI cannot be re-used even if the 
previous use was on a transaction that 
is no longer open  
FC 3.13: ASIC & MAS Usage Guidelines 
ASIC and MAS require 3 of the 4 message types excluding Real-Time messages 
 ASIC MAS 
Transaction auth.030.001.03_ASICUG_DATTAR_1.0.0 auth.030.001.03_MASUG_DATTAR_1.0.0 
Valuation auth.030.001.03_ASICUG_DATTAR_1.0.0 auth.030.001.03_MASUG_DATTAR_1.0.0 
[[Margin]] auth.108.001.01_ASICUG_DATMDA_1.0.0 auth.108.001.01_MASUG_DATMDA_1.0.0 
While the transaction and valuation messages share the same ingestion schema, the intent of the Usage 
Guidelines is to define restrictions that will tighten the fields being submitted. For example, a valuation action 
type should in theory only contain valuation related fields even though it would be possible to submit other 
economic fields that are in the baseline auth.030.001.03.xsd schema. The Usage Guidelines are meant to 
address this gap. 
The UG is built through the MyStandards portal via SWIFT. There will be 2 sets UG; one each for ASIC and 
MAS.  Additionally, the PDF and/or excel version could be provided along with the XSD for users of the system 
and distributed to ASIC and MAS users outside of SWIFT in order to minimize users requesting permission to 
access the usage guidelines via MyStandards. Additionally, the ASIC and MAS UG will be setup as public in 
the MyStandards portal.  
The Usage Guidelines will cover: 
1. Mandatory field validation by action type where the ISO baseline schema is optional.  
2. Tighter enumerations than the ISO baseline schema.  
3. Tighter format restrictions than the ISO baseline schema 
4. Any not applicable fields classified by action type for ASIC and MAS. The fields which are not applicable 
by each action type and if they are submitted by a firm, they will receive a rejection response for invalid 
schema based on the Usage Guidelines 
To assist users, [[DTCC]] sample messages have been published in the Learning Centre . 
• ASIC Usage Guidelines 
• MAS Usage Guidelines 
 
 

---

## Page 34

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 34 
FC 3.14: Introduction of an Aggregated O-Code 
Starting from the Rewrite, clients can choose whether to consolidate all core [[Asset]] classes under 8ABC or 
continue with their existing [[Asset]] class level segregation (ie) 2 = CO, 3 = Credit etc. 8ABC offers an aggregate 
of all [[OTC]] Core, including data submitted under the 2-6 o-codes. This is not mandatory, and clients can 
choose what makes sense for them. Utilizing 8ABC will enable firms to consolidate all their [[OTC]] submissio ns 
into a single report agnostic of [[Asset]] class. 0ABC will remain for [[Margin]] reporting.   
FC 3.15: Unique Product Identifier (UPI) 
While DDRS will migrate the current ISDA Product Taxonomy to the Unique Product Identifier (UPI) proprietary 
tag, this will purely be a transitional update as firms are expected to re-report a UPI within the re-reporting 
period. For new trades, reporting entities are to generate or reference an existing UPI via a designated 
regulatory third party supplier (ANNA-DSB).  
DDRS will receive a real time feed of UPI data for validation. If a UPI does not exist against the UPI database 
provided from the designated regulatory third party supplier (ANNA-DSB), submissions will be rejected. Any 
UPI status will be accepted.  
Production UPI data (from ANNA-DSB) will be incorporated into DDRS’s UAT Simulator and DDRS’s UAT 
environment at a future date (TBD)  
Additionally, there are other fields which will rely on UPI data elements for validation.  
▪ For ASIC – Notional amount - Leg 1, Notional amount - Leg 2, Call amount, Put amount, Notional 
currency - Leg 1, Notional currency - Leg 2, Call currency, Put currency, Notional amount schedule 
amount - Leg 1, Fixed rate - Leg 1, Fixed rate - Leg 2, CDS index attachment point, Index factor 
▪ For MAS (TBD) – Fixed rate of leg 1, Fixed rate of leg 2, Notional amount of the contract or leg 1, 
Notional currency of the contract or leg 1, Notional amount of leg 2, Notional currency of leg 2, Call 
amount, Call currency, Put amount, Put currency 
There will be no cross validations of UPI values between message types (Trade State and Valuation).  
For subsequent UPI submissions and validations, UPI field can be updated with Action Types that are not 
VALU or MARU. The latest submitted UPI will appear in reporting and the submitted UPI is not validated 
against previous UPI submissions. 
Where the ASIC and MAS Message Specification fields overlap with UPI attributes (e.g., Notional currency, 
[[settlement]] currency, [[Asset]] class), Message Specification fields will take precedence and need not be validated 
to match the corresponding UPI attributes. 
For trades that are live prior to the Rewrite go-live, UPI will be migrated to Proprietary UPI tag. Firms will have 
to generate and report UPI generated of these trades once they update the trade. Proprietary UPI cannot be 
updated.  
 

---

## Page 35

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 35 
FC 3.16: Other Payment Fields 
For the ASIC and MAS Rewrite, we have 6 data fields to capture information relating to Other Payments. 
These fields are listed below: 
1. Other payment amount 
2. Other payment type 
3. Other payment currency 
4. Other payment payer 
5. Other payment receiver 
6. Other payment date (Only applicable for ASIC) 
These fields accept multiple values and there are validation rules applied to ensure the number of values 
populated in each field are consistently reported. E.g, if multiple values are reported, the number of Other 
payment amount, Other payment type, Other payment currency, Other payment date, Other payment payer 
and Other payment receiver must be the same, otherwise the submission will be rejected. Please refer to 
business rules in the Message Specification for details. 
Note that the allowed values for Other Payment Type for ASIC and MAS are slightly different. ASIC accepts 
Upfront Payment (UFRO) and Unwind (UWIN) while MAS accepts both and an additional value, Principle 
Exchange (PEXH) 
From a CSV reporting perspective, the following fields forms the unique key for determining how the other 
payments fields are displayed on the end of day Trade State Reports (TSR).  
Other Payment Uniqueness Key: 
1. Other payment type 
2. Other payment date (Only applicable for ASIC) 
3. Other payment receiver 
4. Other payment payer 
 
Based on the Other Payment uniqueness key: 
a) For submissions with the same unique key, the latest values are stored for under the Event Timestamp 
approach. 
b) For submissions where there is a change to the unique key, the values from this submission will be 
cumulated and appended to respective fields on the Trade State Report.  
For example: If a Payment Type of UFRO was submitted on a NEWT, and subsequently a PEXH is 
submitted on a MODI action type, as there is a change in one of the 4 fields which determines the 
Other Payment Uniqueness Key, the PEXH details on this second submission will be added to 
details reported on the NEWT in the TSR (represented as separate additional values semi-colon 
separate.) instead of over writing the values in the NEWT submission. 

---

## Page 36

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 36 
c) The [Action Type] of CORR can be used to correct the details of other payment data previously 
reported or to ‘erase’ a payment previously submitted by reporting with other payment amount = 0.  
See details in the Other Payments table below for examples. 

---

## Page 37

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 37 
Sub 
No: 
Inbound Submission via XML Outbound CSV Report Display of Values 
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

## Page 38

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 38 
Sub 
No: 
Inbound Submission via XML Outbound CSV Report Display of Values 
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

## Page 39

FUNCTIONAL CHANGE DOCUMENT: ASIC & MAS REWRITE 
 
 39 
Sub 
No: 
Inbound Submission via XML Outbound CSV Report Display of Values 
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
A new [Other Payment Type] - value 'UWIN’ 
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

---

## Page 40

 
 
*ASIC: The Other Payment uniqueness key is combination of [Other Payment Type] & [Other payment date] & 
[Other payment payer] & [Other payment receiver]. 
*MAS: The Other Payment uniqueness key is combination of [Other Payment Type] & [Other payment payer] & 
[Other payment receiver]. 
FC 3.17: Schedule Fields 
For the ASIC Rewrite, we have 2 sets of Schedule fields listed below: 
Schedules Jurisdictional 
Field 
Schedule 
Values Reporting Logic in CSV 
Notional 
amount 
schedule - 
Leg 1 
Notional 
amount - Leg 1 
Reported 
Value or 
derived from 
Schedule 
where 
applicable. 
1. If [Notional amount schedule - notional amount in effect on 
associated effective date of leg 1] is populated, report the 
current value of the Notional amount from the Notional 
amount Leg 1 schedule between the indicated Effective dates 
and End dates. 
2. If there is NO End date given, continue to report the value 
of the notional amount of leg 1 in the schedule from the 
Effective date. 
3. Where the different schedule dates are not given 
continuously, report the value in the [Notional amount of leg 
1] field until the Effective Date of the next schedule. (If the 
value is blank, report blank.) 
Notional 
amount 
schedule 
effective date - 
Leg 1 
Effective date 
from Schedule Schedule fields: Report values as submitted. 
Notional 
amount 
schedule end 
date - Leg 1 
End date from 
Schedule Schedule fields: Report values as submitted. 
Notional 
amount 
schedule 
amount - Leg 1 
Value from 
Schedule Schedule fields: Report values as submitted. 
Notional 
amount 
schedule - 
Leg 2 
Notional 
amount - Leg 2 
Reported 
Value or 
derived from 
Schedule 
where 
applicable. 
1. If [Notional amount schedule - notional amount in effect on 
associated effective date of leg 2] is populated, report the 
current value of the Notional amount from the Notional 
amount Leg 2 schedule between the indicated Effective dates 
and End dates. 
2. If there is NO End date given, continue to report the value 
of the notional amount of leg 2 in the schedule from the 
Effective date. 
3. Where the different schedule dates are not given 
continuously, report the value in the [Notional amount of leg 
2] field until the Effective Date of the next schedule. (If the 
value is blank, report blank.) 

---

## Page 41

 
 
Notional 
amount 
schedule 
effective date - 
Leg 2 
Effective date 
from Schedule Schedule fields: Report values as submitted. 
Notional 
amount 
schedule end 
date - Leg 2 
End date from 
Schedule Schedule fields: Report values as submitted. 
Notional 
amount 
schedule 
amount - Leg 2 
Value from 
Schedule Schedule fields: Report values as submitted. 
 
For the MAS Rewrite, we also have 2 sets of Schedule fields listed below: 
Schedules Jurisdictional 
Field 
Schedule 
Values Reporting Logic in CSV 
Price 
Schedule 
Price 
Reported Value 
or derived from 
Schedule 
where 
applicable. 
1. If [Price schedules - Price in effect between the unadjusted 
effective date and unadjusted end date inclusive] is 
populated, report the value of the price from the Price 
schedule between the indicated Effective dates and End 
dates. 
2. If there is NO End date given, continue to report the value 
of the price in the schedule from the Effective date. 
3. Where the different schedule dates are not given 
continuously, report the value in the [Price] field until the 
Effective Date of the next schedule. (If the value is blank, 
report blank.) 
Unadjusted 
effective date 
of the price 
(Price 
schedule) 
Effective date 
from Schedule Schedule fields: Report values as submitted. 
Unadjusted end 
date of the 
price (Price 
schedule) 
End date from 
Schedule Schedule fields: Report values as submitted. 

---

## Page 42

 
 
Price in effect 
between the 
unadjusted 
effective date 
and end date 
(Price 
schedule) 
Value from 
Schedule Schedule fields: Report values as submitted. 
Strike Price 
Schedule 
Strike price 
Reported Value 
or derived from 
Schedule 
where 
applicable. 
1. If [Strike price schedules - Strike price in effect between 
the unadjusted effective date and unadjusted end date 
inclusive] is populated, report the current value of the strike 
price from the Strike Price schedule between the indicated 
Effective dates and End dates. 
2. If there is End date given, continue to report the value of 
the strike price in the schedule from the Effective date. 
3. Where the different schedule dates are not given 
continuously, report the value in the [Strike Price] field until 
the Effective Date of the next schedule. (If the value is blank, 
report blank.) 
Effective date 
of strike price 
(Strike price 
schedule) 
Effective date 
from Schedule Schedule fields: Report values as submitted. 
End date of 
strike price 
(Strike price 
schedule) 
End date from 
Schedule Schedule fields: Report values as submitted. 
Strike price in 
effect on 
associated 
effective date 
(Strike price 
schedule) 
Value from 
Schedule Schedule fields: Report values as submitted. 
The schedule fields accept multiple values. Validation rules applied to ensure the values populated in each 
field are consistently and logically reported. Submission will be rejected if the rules are not adhered to. 
1. For each set of schedules, we will reject the submission if the number of Value s and Effective dates 
submitted does not match. E.g. For ASIC, if the number of [Notional amount schedule amount - Leg 1] 
fields and the number of [Notional amount schedule effective date - Leg 1] fields are not the same. 
2. The End date for each schedule is optional, but if it is populated, we will reject the submission if the 
number of Values, Effective date and End date values does not match 
3. The Effective dates submitted must be in sequential order. 
4. The Effective dates submitted cannot be before than the End Dates of the previous payment schedule. 
5. The End dates submitted must be in sequential order. 
 
 
 
 

---

## Page 43

 
 
Examples are acceptable and rejected values are illustrated in the tables below:  
Case 1 
 
XML 
Block Field Value Expected behaviour 
1 Unadjusted effective date of the price (Price schedule) 2023-09-01 
Accepted 
Unadjusted end date of the price (Price schedule) 2023-09-30 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 9000 
2 Unadjusted effective date of the price (Price schedule) 2023-10-01 
Unadjusted end date of the price (Price schedule) 2023-10-31 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 8000 
3 Unadjusted effective date of the price (Price schedule) 2023-11-01 
Unadjusted end date of the price (Price schedule) 2023-11-30 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 7000 
 
 
 Case 2       
Block Field Value Expected behaviour 
1 
Unadjusted effective date of the price (Price schedule) 2023-11-01 
Rejected – The blocks are not arranged 
in sequential order - from earliest date 
range to latest date range. 
Unadjusted end date of the price (Price schedule) 2023-11-30 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 9000 
2 
Unadjusted effective date of the price (Price schedule) 2023-09-01 
Unadjusted end date of the price (Price schedule) 2023-09-30 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 8000 
3 
Unadjusted effective date of the price (Price schedule) 2023-10-01 
Unadjusted end date of the price (Price schedule) 2023-10-31 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 7000 
 
 
Case 3      
Block Field Value Expected behaviour 
1 
Unadjusted effective date of the price (Price schedule) 2023-09-01 
Rejected – Block 2's start date overlaps 
with Block 1's end date. 
Unadjusted end date of the price (Price schedule) 2023-09-30 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 9000 

---

## Page 44

 
 
2 
Unadjusted effective date of the price (Price schedule) 2023-09-30 
Unadjusted end date of the price (Price schedule) 2023-10-31 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 8000 
3 
Unadjusted effective date of the price (Price schedule) 2023-11-01 
Unadjusted end date of the price (Price schedule) 2023-11-30 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 7000 
 
 
 Case 4  
Block Field Value Expected behaviour 
1 Unadjusted effective date of the price (Price schedule) 2023-09-01 
Accepted – End date can be blank. 
Unadjusted end date of the price (Price schedule) Blank 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 9000 
2 Unadjusted effective date of the price (Price schedule) 2023-10-01 
Unadjusted end date of the price (Price schedule) Blank 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 8000 
3 Unadjusted effective date of the price (Price schedule) 2023-11-01 
Unadjusted end date of the price (Price schedule) Blank 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 7000 
 
Case 5 
Block Field Value Expected behaviour 
1 
Unadjusted effective date of the price (Price schedule) 2023-11-01 
Rejected - Blocks are not arranged in 
chronological order from earliest date 
range to latest date range 
Unadjusted end date of the price (Price schedule) Blank 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 9000 
2 
Unadjusted effective date of the price (Price schedule) 2023-09-01 
Unadjusted end date of the price (Price schedule) Blank 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 8000 
3 
Unadjusted effective date of the price (Price schedule) 2023-10-01 
Unadjusted end date of the price (Price schedule) Blank 
Price in effect between the unadjusted effective date and end date 
(Price schedule) 7000 
 

---

## Page 45

 
 
Based on Case 1, below are some examples of how values reported in the schedules will display in the TSR 
CSV Reports. 
1) Report date is 2023-09-16 
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
price (Price schedule) 
UTI1 LEI1 LEI2 9000 9000;8000;7000 
2023-09-01;2023-10-
01; 
2023-11-01 
2023-09-30;2023-10-31; 
2023-11-30 
 
2) Report date is 2023-10-16 
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
price (Price schedule) 
UTI1 LEI1 LEI2 8000 9000;8000;7000 
2023-09-01;2023-10-
01; 
2023-11-01 
2023-09-30;2023-10-31; 
2023-11-30 
 
3) Report date is 2023-11-16 
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
price (Price schedule) 
UTI1 LEI1 LEI2 7000 9000;8000;7000 
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
This applies to all the schedule fields: Price schedule, Strike price schedule, Notional amount schedule - Leg 1 
and Notional amount schedule - Leg 2 
 
 
 
 

---

## Page 46

 
 
FC 4: Message Responses  
FC 4.1 Response Format  
The message response format will be changed to XML instead of the current FpML or CSV response formats 
to align with the ISO XML inbound submission format. The response file formats are returned in zip 
compression format with .xml as the file extension within the zip file: 
Description Format Proposed File Name  
ASIC GTR Batch 
ACK/NACK Report XML ISO20022XML 
SFTP File Name: 
sFTP_BizMsgIdr_ASIC_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.zip or 
sFTP_BizMsgIdr_ASIC_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.gz 
 
sFTP File Name within the compressed file: 
sFTP_BizMsgIdr_ASIC_BDR_BatchInfoID_6XXX_2023-10-20.01_10_06.xml  
Portal: 
BizMsgIdr_ASIC_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.zip 
 
Portal File Name within the compressed file: 
WEB-US-BatchInfoID.xml or SFP-US-BatchInfoID.xml 
 
Note: Clients may configure the compression method to .gz or .zip. GZIP (.gz) is for UNIX 
based systems and WINZIP (.ZIP) is for Windows based systems 
  
 
MAS GTR Batch 
ACK/NACK Report XML ISO20022XML 
SFTP File Name: 
sFTP_BizMsgIdr_MAS_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.zip or 
sFTP_BizMsgIdr_MAS_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.gz 
 
sFTP File Name within the zip file: 
sFTP_BizMsgIdr_MAS_BDR_BatchInfoID_6XXX_2023-10-20.01_10_06.xml 
Portal: 
BizMsgIdr_MAS_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.zip 
Portal File Name within the compressed file: 
WEB-US-BatchInfoID.xml or SFP-US-BatchInfoID.xml 
 
Note: Clients may configure the compression method to .gz or .zip. GZIP (.gz) is for UNIX 
based systems and WINZIP (.ZIP) is for Windows based systems 
 
 
 
(a) BizMsgIdr is a 35-character identifier that the client indicates on the xml header in the submission file. This 
string does not allow most special characters, and would only accept alphanumeric (0-9a-zA-Z), underscore 
(_), hyphen (-) and dot (.) 
(b) The BatchInfoID would be an [[ID]] that GTR generates to identify the file reference 
(c) 6XXX refers to the o-code you submitted from 
(d) YYYY-MM-DD.HH_MM_SS is the timestamp of the response file generation in UTC 
The ISO 20022 XML template shows there will be 2 levels of validation response (ACK /NACK).  
 
1. Message / file level  
2. Submission level  
 
The excerpt from the XML message response schema (auth.031.001.01) below shows these 2 levels of ACK / 
NACK.  
 

---

## Page 47

 
 
• The <MsgSts> within the blue section below is the element where the message / file level validation response 
will be provided. There will always be one ACK / NACK response for a submitted message / file. <MsgSts> can 
be only one of these two value:  
o <Sts>CRPT</Sts> = CRPT (Corrupt) means entire message / file is rejected. Positions inside the message 
are not open/updated on [[DTCC]] side.  
o <Sts>ACPT</Sts> = ACPT (ACK) means message / file was correctly read.  
 
• The <RcrdSts> within the red section is the element where the submission level validation respo nse will be 
provided. If the submission file contains 100 submissions, then there will be 100 ACK / NACK responses. 
<MsgSts> can be only one of these two value:  
o <Sts>RJCT</Sts> = RJCT (NACK) means record is rejected  
o <Sts>ACPT</Sts> = ACPT (ACK) means record is accepted  
 

---

## Page 48

 
 
 
The Business Message Header [[ID]] (BizMsgIdr tag, as shown below) must be present in the Application Header 
of each file or message submitted to the GTR. Submissions can be sent using version 01 or version 02 of the 
Business Application Header (BAH). 
 


---

## Page 49

 
 
 
 
The ACK / NACK message response (auth.031.001.01) generated by the GTR will provide the same BizMsgIdr 
used in the submitted file or message. This will be found in the MsgRptIdr tag highlighted below in red.  


---

## Page 50

 
 
 
Identification of each submission in the ACK / NACK message response will be based on the T echnical Record 
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

## Page 51

 
 
 
 
Sample files illustrating the XML response layouts can be found on the Learning Center: 
• Message Response Samples (TBD) 
 
 
 
 
 
 


---

## Page 52

 
 
FC 4.2 Response Format/Channel  
There will be changes to the response format and channel based on the ASIC & MAS Rules Rewrite 
Implementation. As a reference, this table summarizes the future functionality: 
Submission 
Channel 
Submission 
Format 
Response 
Format 
Response  Receiver Response 
Channel 
MQ ISO XML 
message 
ISO XML ISO XML 
message 
Report Submitting 
Entity 
MQ 
Web Upload 
(a) Without sFTP 
subscription 
(b) With sFTP 
subscription 
ISO XML files ISO XML ISO XML files Report Submitting 
Entity 
(a) Portal 
(b) Portal and 
sFTP 
destination 
sFTP ISO XML files ISO XML ISO XML files Report Submitting 
Entity 
sFTP destination 
and Portal 
 
FC 4.3 MQ Response to be sent to ReplytoQueue 
To enhance the client experience, we will introduce a functionality to allow clients to specify where the 
ACK/NACK response message should be delivered. This comes at the back of client feedback and has already 
been implemented in NoA. 
This functionality allows you to be able to indicate where you want your responses to be sent via the Reply To 
– Queue Manager and Reply to – Queue Name details on the MQ message header so that the response would 
be returned to the queue name indicated. 
FC 5: Reports  
Daily reports are generated and made available through the [[DTCC]] Portal.  Further details on functionality 
within the portal can be found on the Learning Center. The reports that exist today will no longer be available. 
[[DO]] note that blank [[participant]] reports will not be generated should there be cases where the report criteria are 
not met for a particular day; for example no submissions within a reporting window.  
FC 5.1: Report Types 
The following reports will be created daily. Details of the report layouts are available on Learning Center when 
ready. The report format would be CSV by [[default]]. 
Type Description 
[[EOD]] Trade State Report • Alleged records where the report recipient is named as the OCP should not be 
displayed on the Trade State Report.  
• Only unique trades should be displayed in the TSR. The uniqueness of a trade is 
defined by the concatenation of the UTI + RCP1. For example, if position 1 is UTI + 
RCP1 + OCP1 & position 2 is UTI + RCP2 and OCP1, then they are considered 

---

## Page 53

 
 
unique positions. Another example is if an RCP and ERR is the same on a position, 
then the position is expected to appear only once on the TSR even though both RCP 
and ERR get access to the TSR 
• If a position is early terminated via the applicable exit action types or expired based 
on Expiration Date between a report generation window, that position will not be on 
the TSR generated for that day,  
• The TSR contains the latest view of the position but excludes valuation and [[Margin]] 
messages, though valuation data fields will be merged to the position (VALU & MARU 
Action Types) 
• The TSR is run and generated daily from Tuesday to Saturday after midnight SGT 
• The reports will be available on the portal for up to 12 months on a going forward 
basis from go live date. 
• The following parties will have access to the TSR: Reporting Counterparty (RCP), 
Entity Responsible for Reporting (ERR) and Execution Agent of Counterparty  
• TSR (Position Report) should only include messages accepted at GTR and exclude 
rejects 
• Each position on the report should only contain the information related to that 
submission. If an optional field is excluded from the user submission, it will be blank 
on the report 
• There is no masking of fields as TSR (Position Report) is only available to the RCP 
and ERR 
• The final report format will be published in the Message Specifications. 
• This report is created per [[Asset]] class per jurisdiction. 
• Trades which have been submitted with action type TERM or EROR (and not 
subsequently revived) or have been submitted with action type PRTO but not re-
opened successfully are excluded (even if their expiration date is in the future). 
[[EOD]] Trade Activity 
Report 
• The Activity report should only include messages accepted at GTR and exclude 
rejects. 
• The Activity report should only contain activity between two report generation periods. 
For instance, the report generated on Wednesday morning SGT should contain 
accepted trade messages submitted between Tuesday 00:00:00 SGT to Tuesday 
23:59:59 SGT. The only exception where this report contains multiple days’ worth of 
submissions is the report generated on Tuesday morning SGT which would contain 
accepted trade messages submitted between Saturday 00:00:00 SGT to Monday 
23:59:59 SGT. The timestamp to be considered is based on the submission 
timestamp which is the time submitted by the user. Multiple trade submissions with 
the same identifier would be displayed multiple times if they are submitted 
successfully within the reporting window. 
• Each position on the report should only contain the information related to that 
submission. If an optional field is excluded from the user submission, it will be blank 
on the report 
• The [[EOD]] Trade Activity report should contain only trade messages or valuation 
messages but exclude [[Margin]] submissions which will be on a separate [[Margin]] 
activity report. 
• Allege records where the report recipient is named as the OCP should not be 
displayed on the Trade Activity Report 
• The TAR is run and generated daily from Tuesday to Saturday after midnight SGT 
• The reports will be available on the portal for up to 12 months on a going forward 
basis from go live date. 
• The following parties will have access to the Activity report: RCP and ERR 
• There is no masking of fields in the Activity report  

---

## Page 54

 
 
• The final report format will be published in the Message Specifications. 
• This report is created per [[Asset]] class per jurisdiction. 
[[EOD]] Submission Report • The Submission Report contains all the successful and unsuccessful submissions 
submitted by the Report Submitting Entity (RSE). All Accepted and Rejected 
submissions are included in the report. 
• [[EOD]] cutoff is 23:59 SGT Monday to Friday meaning any submissions that are 
received based on submission received timestamp of 23:59:59 SGT is eligible for 
reporting on that day’s submission reports even if it is processed by GTR past the 
next day. 
• The Submission Report contains trade and valuation messages but excludes [[Margin]] 
messages. [[Margin]] submissions will be reflected on a separate report 
• The Submission Report will only be available in CSV format 
• The Submission Report is run and generated daily from Tuesday to Saturday after 
midnight SGT 
• The reports will be available on the portal for up to 12 months on a going forward 
basis from go live date. 
• The following parties will have access to the Submission Report: Submitter Identifier 
(RSE) and Reporting Counterparty (RCP). The Submitter Identifier (RSE) will see all 
trade sides they have submitted, whether accepted or rejected but cannot view any 
submissions they did not submit.  
• The Reporting Counterparty (RCP) will see their own side of the trade with 
themselves as RCP and their counterparty as OCP, whether accepted or rejected. 
The Reporting Counterparty (RCP) will see all the successful and unsuccessful 
submissions submitted by themselves. 
• The ERR does not have access to the Submission Report, unless the ERR is also the 
RSE or RCP. 
• There is no masking of fields in the Submission Report 
• The final report format will be published in the Message Specifications.  
• This report is created per [[Asset]] class per jurisdiction. 
[[EOD]] [[Margin]] State Report • The [[Margin]] State Report is run and generated daily from Tuesday to Saturday after 
midnight SGT 
• The [[Margin]] State Report will be available on the portal for up to 12 months on a going 
forward basis from go live date. 
• The [[Margin]] State Report contains the latest [[Margin]] view based on event timestamp 
against open positions at the point of the report generation if they were collateralized 
on a trade or portfolio basis.  
• For [[Derivatives]] collateralized on a trade basis:  
(a) if the derivative position (UTI + RCP + OCP) was terminated on 15/5/2024, the 
[[Margin]] state for that derivative position will not be on the MSR published to the 
client on report generated on 16/5/2024 (Report Date 15/5/2024) but will be on 
the report generated on 15/5/2024 (Report Date 14/5/2024) 
(b) if the derivative position (UTI + RCP + OCP) reached its Expiration Date on 
15/5/2024 (maturity), the [[Margin]] state for that derivative position will not be on 
the MSR published to the client on the report generated on 16/5/2024 (Report 
Date 15/5/2024) 
• For [[Derivatives]] collateralized on a portfolio basis:  
(a) If at least 1 derivative position (UTI + RCP + OCP) within the portfolio 
(concatenated value of IM/VM portfolio code) is outstanding on 15/5/2024 (and 
that includes derivative positions in that portfolio that might have an Expiration 
Date of 15/5/2024), the [[Margin]] state for that [[collateral]] portfolio will be on the 
MSR published to the client on 15/5/2024 but will drop off on 16/5/2024 

---

## Page 55

 
 
assuming there is no new derivative position associated with the IM/VM portfolio 
code with an expiration date after 15/5/2024. 
(b) all derivative positions (UTI + RCP + OCP) within the portfolio (concatenated 
value of IM/VM portfolio code) is non-outstanding on 15/5/2024 (including being 
early terminated on 15/5/2024), the [[Margin]] state for that [[collateral]] portfolio will 
not be on the MSR published to the client on 16/5/2024 
• The following parties will have access to the MSR: Reporting Counterparty (RCP) and 
Entity Responsible for Reporting (ERR) 
• The [[Margin]] State Report should only include [[collateral]] messages accepted at GTR 
and exclude rejects 
• Each line on the report should only contain the information related to that submission. 
If an optional field is excluded from the user submission, it will be blank on the report 
• There is no masking of fields in ASIC and MAS as MSR is only available to the RCP 
and ERR 
• The final report format will be published in the Message Specifications. 
[[EOD]] [[Margin]] Activity 
Report 
• The [[Margin]] Activity report should only include “MARU” and “CORR” action type 
messages that are accepted at GTR and exclude rejects. 
• [[Margin]] Activity report should only contain activity between two report generation 
periods. For instance, the report generated on Wednesday morning SGT should 
contain accepted [[Margin]] messages submitted between Tuesday 00:00:00 SGT to 
Tuesday 23:59:59 SGT. The only exception where this report contains multiple days’ 
worth of submissions is the report generated on Tuesday morning SGT which would 
contain accepted [[Margin]] messages submitted between Saturday 00:00:00 SGT to 
Monday 23:59:59 SGT. The timestamp to be considered is based on the submission 
timestamp which is the time submitted by the user. Multiple trade submissions with 
the same identifier would be displayed multiple times if they are submitted 
successfully within the reporting window. 
• Each line on the report should only contain the information related to that submission. 
If an optional field is excluded from the user submission, it will be blank on the report 
• The [[Margin]] Activity report should contain only [[Margin]] messages 
• Allege records where the report recipient is named as the Trade Party 2 should not 
be displayed on the [[Margin]] Activity Report 
• The [[Margin]] Activity Report is run and generated daily from Tuesday to Saturday after 
midnight SGT 
• The reports will be available on the portal for up to 12 months on a going forward 
basis from go live date. 
• The following parties will have access to the Activity report: RCP and ERR 
• There is no masking of fields in the [[Margin]] Activity report  
• The final report format will be published in the Message Specifications. 
[[EOD]] [[Margin]] Submission 
Report 
• The [[Margin]] Submission Report contains all the successful and unsuccessful 
submissions submitted by the report submitting entity (RSE). All Accepted and 
Rejected submissions are included in the report. 
• [[EOD]] cutoff is 23:59 SGT Monday to Friday meaning any submissions that are 
received based on submission received timestamp of 23:59:59 SGT is eligible for 
reporting on that day’s submission reports even if it is processed by GTR past the 
next day. 
• The [[Margin]] Submission Report contains only [[Margin]] messages based on action type 
MARU and CORR. 
• The [[Margin]] Submission Report will only be available in CSV format 
• The [[Margin]] Submission Report is run and generated daily from Tuesday to Saturday 
after midnight SGT 

---

## Page 56

 
 
• The reports will be available on the portal for up to 12 months on a going forward 
basis from go live date. 
• The following parties will have access to the [[Margin]] Submission Report: Submitter 
Identifier (RSE) and Submitted for Party (RCP). The Submitter Identifier (RSE) will 
see all trade sides they have submitted, whether accepted or rejected but must not be 
able to view any submissions they did not submit. 
• The Reporting Counterparty (RCP) will see their own side of the trade with 
themselves as Trade Party 1 and their counterparty as Trade Party 2, whether 
accepted or rejected. The Reporting Counterparty (RCP) will see all the successful 
and unsuccessful submissions submitted by themselves. 
• There is no masking of fields in the [[Margin]] Submission Report 
• Report Format will be published in the Message Specifications. 
[[EOD]] Trade Allege Report • The End of Day allege report will consist of the Allege view of the trade and will be 
provided only in CSV format. 
• This report will be based off the TSR and will contain the Allege view of positions at 
[[EOD]] 
• The party receiving this report will be the Other Counterparty of the trades if the Other 
Counterparty is onboarded 
• Only unique trades should be displayed in the Allege Report. The uniqueness of a 
trade is defined by the concatenation of the UTI + OCP.  
• If a position is early terminated via the applicable exit action types or expired based 
on Expiration Date between a report generation window, that position will be 
excluded from Allege Report generated for that day.  
• The Allege Report contains the latest view of the position but excludes valuation and 
[[Margin]] data. 
• The Allege Report is run and generated daily from Tuesday to Saturday after 
midnight SGT 
• The reports will be available on the portal for up to 12 months on a going forward 
basis from go live date. 
• The following parties will have access to the Allege Report: Other Counterparty 
(OCP) if they are onboarded 
• The Allege Report should only include messages accepted at GTR and exclude 
rejects 
• Each position on the report should only contain the information related to that 
submission. If an optional field is excluded from the user submission, it will be blank 
on the report 
• The final report format will be published in the Message Specifications. 
• This report is created per [[Asset]] class per jurisdiction 
Intraday Allege Activity 
Report 
• The intention of this new GTR report will be to facilitate a way for counterparties to 
share data intraday. 
• This report is not mandated by the regulators. It is a GTR proprietary report. 
• The Intraday Allege Report will only include messages accepted into the GTR 
between the intraday reporting windows. Rejected messages will be excluded. 
• The Intraday Allege Activity Report will only include submissions, that have been 
accepted (Rejected messages will be excluded) on that particular day, with the Action 
Types of NEWT, EROR, REVI where the client (for whom report is being generated) 
is listed as CP2 
• The Intraday Allege Report will be generated in CSV only. 
• The Intraday Allege Report will be generated thrice daily at 10:00am SGT and 
18:00pm and 00:00am SGT between Monday to Friday. The Intraday Allege Activity 

---

## Page 57

 
 
Report will include eligible submissions accepted up to the point of generation of the 
report (will be cumulative). 
6pm Report - include eligible Action Types accepted between 00:00:00 am and 
17:59:59pm 
• The reports will be available on the portal for up to 12 months on a going forward 
basis from go live date. The following parties will have access to the Intraday Allege 
Report: Other Counterparty (OCP) if they are onboarded 
• If an optional field is excluded from the user submission it will also be blank on the 
report 
• The final report format is published in the Message Specifications. 
• This report is created per the [[Asset]] class(es) configured under the standard [[DTCC]] O-
Code 
• A detailed report specification is provided on the learning centre 
 
Users who wish to have the NEW reports sent to them via sFTP will need to set up configurations for the new 
product IDs with our connectivity team (GTRConnectivity@[[DTCC]].com). 
FC 5.2: Merging of Trade Valuation Information onto Trade State Report 
1. Merging of fields from Valuation submission onto TSR:  When merging the valuation details onto the 
TSR, only valuation specific fields should be updated from the valuation message.   
2. The ASIC valuation related fields are Valuation timestamp, Valuation amount, Valuation currency, 
Valuation method, Delta, Leg 1 and Leg 2 of Next floating reference reset date  
3. The MAS valuation related fields are Valuation timestamp, Valuation amount, Valuation currency, and 
Valuation method. 
4. We will follow latest is greatest approach for valuation submissions when linking the valuation fields to the 
position on the TSR. 
5. All other timestamp fields on the TSR will continue to be based on the information on the Trade 
submission (i.e., they will not be updated with the values from the Trade Valuation submission).  
6. Timestamp used for merging the “latest” valuation:  The valuation submission used for merging onto 
the TSR will be based on the latest Valuation Timestamp. 
7. When matching a Valuation to a base trade for merging information onto the TSR at end of day, the UTI + 
RCP + OCP must match. 
FC 5.3 Self-Service Report Management Functionality 
As ASIC, MAS and various other jurisdictions [[DO]] not regulatorily mandate [[participant]] reports to be in a 
particular format, our understanding is that firms may need a choice of receiving reports in XM L, CSV or XML 
and CSV. However, [[DO]] note that [[DTCC]] proprietary reports (refer to FC 5.1) will only be available in CSV only.  
Report Management will be an additional landing tile on the Manage Services screen. Selecting the tile allows 
firms to add and configure reports per service and the [[default]] setup will be CSV format for all reports. Reports 
will be aggregated by type (eg) Trade State Report and clients cannot choose to further segregate the same 
report by [[Asset]] class.  

---

## Page 58

 
 
This functionality does not require any specific build from clients and require a one-time setup and subscription. 
Once subscribed, reports will be generated from that day going forward in the selected format. Clients can also 
unsubscribe from reports to stop receiving them, and the plan is to implement this functionality ahead of both 
actual UAT and Production dates to allow for clients to perform their setups in advance . 
For further details, refer to Report Management Section on the Learning Centre. 
FC 5.4 Report Filename Formats 
Description Format Proposed File Name 
ASIC Trade 
Activity Report 
XML 
ISO20022XML 
sFTP 
sFTP_ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
sFTP_ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
sFTP_ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
sFTP_ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
sFTP_ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
 
Portal 
ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
ASIC Trade 
State Report 
XML 
ISO20022XML 
sFTP 
sFTP_ASIC_EOD_Trade_State_Report_02503252-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
sFTP_ASIC_EOD_Trade_State_Report_02503252-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
sFTP_ASIC_EOD_Trade_State_Report_02503252-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
sFTP_ASIC_EOD_Trade_State_Report_02503252-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
sFTP_ASIC_EOD_Trade_State_Report_02503252-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
 
Portal 
ASIC_EOD_Trade_State_Report_02503252-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
ASIC_EOD_Trade_State_Report_02503252-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
ASIC_EOD_Trade_State_Report_02503252-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
ASIC_EOD_Trade_State_Report_02503252-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
ASIC_EOD_Trade_State_Report_02503252-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
ASIC [[Margin]] 
Activity Report 
XML 
ISO20022XML 
sFTP 
sFTP_ASIC_EOD_Margin_Activity_Report_02503253-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
 
Portal 
ASIC_EOD_Margin_Activity_Report_02503253-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
ASIC [[Margin]] 
State Report 
XML 
ISO20022XML 
sFTP 
sFTP_ASIC_EOD_Margin_State_Report_02503254-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
 
Portal 
ASIC_EOD_Margin_State_Report_02503254-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
ASIC Trade 
Activity Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_2XXX.csv 

---

## Page 59

 
 
ASIC Trade 
State Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_ASIC_EOD_Trade_State_Report_02503256-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_ASIC_EOD_Trade_State_Report_02503256-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_ASIC_EOD_Trade_State_Report_02503256-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_ASIC_EOD_Trade_State_Report_02503256-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_ASIC_EOD_Trade_State_Report_02503256-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
ASIC_EOD_Trade_State_Report_02503256-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
ASIC_EOD_Trade_State_Report_02503256-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
ASIC_EOD_Trade_State_Report_02503256-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
ASIC_EOD_Trade_State_Report_02503256-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
ASIC_EOD_Trade_State_Report_02503256-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
ASIC [[Margin]] 
Activity Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_ASIC_EOD_Margin_Activity_Report_02503257-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
 
Portal 
ASIC_EOD_Margin_Activity_Report_02503257-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
ASIC [[Margin]] 
State Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_ASIC_EOD_Margin_State_Report_02503258-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
 
Portal 
ASIC_EOD_Margin_State_Report_02503258-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
ASIC [[Margin]] 
Submission 
Report CSV 
CSV only 
sFTP 
sFTP_ASIC_EOD_Margin_Submission_Report_02503259-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
 
Portal 
ASIC_EOD_Margin_Submission_Report_02503259-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
ASIC Trade 
Submission 
Report CSV 
CSV only 
sFTP 
sFTP_ASIC_EOD_Submission_Report_02503260-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_ASIC_EOD_Submission_Report_02503260-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_ASIC_EOD_Submission_Report_02503260-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_ASIC_EOD_Submission_Report_02503260-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_ASIC_EOD_Submission_Report_02503260-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
ASIC_EOD_Submission_Report_02503260-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
ASIC_EOD_Submission_Report_02503260-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
ASIC_EOD_Submission_Report_02503260-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
ASIC_EOD_Submission_Report_02503260-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
ASIC_EOD_Submission_Report_02503260-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
ASIC [[EOD]] 
Allege Report CSV only 
 
 
sFTP 
sFTP_ASIC_EOD_Allege_Trade_State_Report_02503261-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_ASIC_EOD_Allege_Trade_State_Report_02503261-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_ASIC_EOD_Allege_Trade_State_Report_02503261-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_ASIC_EOD_Allege_Trade_State_Report_02503261-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_ASIC_EOD_Allege_Trade_State_Report_02503261-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
 
Portal 
ASIC_EOD_Allege_Trade_State_Report_02503261-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
ASIC_EOD_Allege_Trade_State_Report_02503261-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
ASIC_EOD_Allege_Trade_State_Report_02503261-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
ASIC_EOD_Allege_Trade_State_Report_02503261-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
ASIC_EOD_Allege_Trade_State_Report_02503261-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
 
  

---

## Page 60

 
 
ASIC Intraday 
Allege Report CSV only 
sFTP 
sFTP_ASIC_Intraday_Allege_Report_02503262-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_ASIC_Intraday_Allege_Report_02503262-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_ASIC_Intraday_Allege_Report_02503262-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_ASIC_Intraday_Allege_Report_02503262-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_ASIC_Intraday_Allege_Report_02503262-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
Portal 
ASIC_Intraday_Allege_Report_02503262-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
ASIC_Intraday_Allege_Report_02503262-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
ASIC_Intraday_Allege_Report_02503262-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
ASIC_Intraday_Allege_Report_02503262-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
ASIC_Intraday_Allege_Report_02503262-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
  
 
Description Format Proposed File Name 
MAS Trade 
Activity Report 
XML 
ISO20022XML 
sFTP 
sFTP_MAS_EOD_Trade_Activity_Report_02503271-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
sFTP_MAS_EOD_Trade_Activity_Report_02503271-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
sFTP_MAS_EOD_Trade_Activity_Report_02503271-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
sFTP_MAS_EOD_Trade_Activity_Report_02503271-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
sFTP_MAS_EOD_Trade_Activity_Report_02503271-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
 
Portal 
MAS_EOD_Trade_Activity_Report_02503271-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
MAS_EOD_Trade_Activity_Report_02503271-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
MAS_EOD_Trade_Activity_Report_02503271-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
MAS_EOD_Trade_Activity_Report_02503271-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
MAS_EOD_Trade_Activity_Report_02503271-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
MAS Trade 
State Report 
XML 
ISO20022XML 
sFTP 
sFTP_MAS_EOD_Trade_State_Report_02503272-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
sFTP_MAS_EOD_Trade_State_Report_02503272-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
sFTP_MAS_EOD_Trade_State_Report_02503272-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
sFTP_MAS_EOD_Trade_State_Report_02503272-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
sFTP_MAS_EOD_Trade_State_Report_02503272-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
 
Portal 
MAS_EOD_Trade_State_Report_02503272-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
MAS_EOD_Trade_State_Report_02503272-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
MAS_EOD_Trade_State_Report_02503272-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
MAS_EOD_Trade_State_Report_02503272-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
MAS_EOD_Trade_State_Report_02503272-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml 
MAS [[Margin]] 
Activity Report 
XML 
ISO20022XML 
sFTP 
sFTP_MAS_EOD_Margin_Activity_Report_02503273-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
 
Portal 
MAS_EOD_Margin_Activity_Report_02503273-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
MAS [[Margin]] 
State Report 
XML 
ISO20022XML 
sFTP 
sFTP_MAS_EOD_Margin_State_Report_02503274-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
 
Portal 
MAS_EOD_Margin_State_Report_02503274-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml 
MAS Trade 
Activity Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_MAS_EOD_Trade_Activity_Report_02503275-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_MAS_EOD_Trade_Activity_Report_02503275-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_MAS_EOD_Trade_Activity_Report_02503275-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_MAS_EOD_Trade_Activity_Report_02503275-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_MAS_EOD_Trade_Activity_Report_02503275-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
MAS_EOD_Trade_Activity_Report_02503275-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
MAS_EOD_Trade_Activity_Report_02503275-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
MAS_EOD_Trade_Activity_Report_02503275-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
MAS_EOD_Trade_Activity_Report_02503275-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
MAS_EOD_Trade_Activity_Report_02503275-YYYY-MM-DD.HH_MM_SS_2XXX.csv 

---

## Page 61

 
 
MAS Trade 
State Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_MAS_EOD_Trade_State_Report_02503276-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_MAS_EOD_Trade_State_Report_02503276-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_MAS_EOD_Trade_State_Report_02503276-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_MAS_EOD_Trade_State_Report_02503276-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_MAS_EOD_Trade_State_Report_02503276-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
MAS_EOD_Trade_State_Report_02503276-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
MAS_EOD_Trade_State_Report_02503276-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
MAS_EOD_Trade_State_Report_02503276-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
MAS_EOD_Trade_State_Report_02503276-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
MAS_EOD_Trade_State_Report_02503276-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
MAS [[Margin]] 
Activity Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_MAS_EOD_Margin_Activity_Report_02503277-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
 
Portal 
MAS_EOD_Margin_Activity_Report_02503277-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
MAS [[Margin]] 
State Report 
CSV 
CSV 
equivalent 
sFTP 
sFTP_MAS_EOD_Margin_State_Report_02503278-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
 
Portal 
MAS_EOD_Margin_State_Report_02503278-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
MAS [[Margin]] 
Submission 
Report CSV 
CSV only 
sFTP 
sFTP_MAS_EOD_Margin_Submission_Report_02503279-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
 
Portal 
MAS_EOD_Margin_Submission_Report_02503279-YYYY-MM-DD.HH_MM_SS_0XXX.csv 
MAS Trade 
Submission 
Report CSV 
CSV only 
sFTP 
sFTP_MAS_EOD_Submission_Report_02503280-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_MAS_EOD_Submission_Report_02503280-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_MAS_EOD_Submission_Report_02503280-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_MAS_EOD_Submission_Report_02503280-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_MAS_EOD_Submission_Report_02503280-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
MAS_EOD_Submission_Report_02503280-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
MAS_EOD_Submission_Report_02503280-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
MAS_EOD_Submission_Report_02503280-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
MAS_EOD_Submission_Report_02503280-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
MAS_EOD_Submission_Report_02503280-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
MAS [[EOD]] 
Allege Report CSV only 
 
 
 
sFTP 
sFTP_MAS_EOD_Allege_Trade_State_Report_02503281-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_MAS_EOD_Allege_Trade_State_Report_02503281-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_MAS_EOD_Allege_Trade_State_Report_02503281-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_MAS_EOD_Allege_Trade_State_Report_02503281-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_MAS_EOD_Allege_Trade_State_Report_02503281-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
Portal 
MAS_EOD_Allege_Trade_State_Report_02503281-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
MAS_EOD_Allege_Trade_State_Report_02503281-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
MAS_EOD_Allege_Trade_State_Report_02503281-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
MAS_EOD_Allege_Trade_State_Report_02503281-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
MAS_EOD_Allege_Trade_State_Report_02503281-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
 
  

---

## Page 62

 
 
MAS Intraday 
Allege Report CSV only 
sFTP 
sFTP_MAS_Intraday_Allege_Report_02503282-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
sFTP_MAS_Intraday_Allege_Report_02503282-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
sFTP_MAS_Intraday_Allege_Report_02503282-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
sFTP_MAS_Intraday_Allege_Report_02503282-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
sFTP_MAS_Intraday_Allege_Report_02503282-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
Portal 
MAS_Intraday_Allege_Report_02503282-YYYY-MM-DD.HH_MM_SS_6XXX.csv 
MAS_Intraday_Allege_Report_02503282-YYYY-MM-DD.HH_MM_SS_5XXX.csv 
MAS_Intraday_Allege_Report_02503282-YYYY-MM-DD.HH_MM_SS_4XXX.csv 
MAS_Intraday_Allege_Report_02503282-YYYY-MM-DD.HH_MM_SS_3XXX.csv 
MAS_Intraday_Allege_Report_02503282-YYYY-MM-DD.HH_MM_SS_2XXX.csv 
 
  
 
Points to note regarding the report formats: 
(a) For XML based reports, the same day reports will be split when it contains more than 500,000 records. 
Part of the report filename contains 001001 where the first three digits represent the number of total 
files, and the second three digits represent the sequence of the file (E.g. 005001 meaning there are 5 
files in total and this file is file 1 in the sequence).    
(b)  The report timestamp DD.HH_MM_SS will be displayed in UTC timezone. 
(c) The report names in the table above indicate the actual file names that are within the compressed file. 
For sFTP-ed reports, the compressed file could either be configured to have compression type as 
GZIP (.gz) which is for UNIX based systems or WINZIP (.zip) for Windows based  systems. For 
example, the filename within the compressed file would be:  
sFTP_ASIC_EOD_Trade_Activity_Report_02503255-YYYY-MM-DD.HH_MM_SS_6XXX.csv OR 
sFTP_ASIC_EOD_Trade_Activity_Report_02503251-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
however the zipped filename could be  
sFTP_ASIC_EOD_Trade_Activity_Report_02503255-2023-10-27.17_34_31_2CHR.csv.gz OR 
sFTP_ASIC_EOD_Trade_Activity_Report_02503255-2023-10-27.17_34_31_2CHR.csv.zip 
 
FC 6: Functionality Specific to Go-Live 
Users are expected to upgrade their open trades to the new data standards as defined in the message 
specifications after go-live.  This section describes relevant functionality to support that process and other go -
live related processes. 
Please note that these activities will be performed during both UAT and Production go-lives. 
 
 
 

---

## Page 63

 
 
FC 6.1:  Transition Period – Data Migration Background 
ASIC 
ASIC published public consultation around data fields, best market practice guidelines, and UTI generation 
guide on their website on 20 December 2022. Any transactions (ie) positions that does not mature as of 20 
October 2025 are considered in scope under the new rules. There are 104 fields proposed and ASIC mandates 
ISO XML on 21 October 2024.  
On Day 1, the full set of fields for new reportable transactions is to be reported. Re-reporting for in-scope 
legacy positions is to be done by 20 April 2025. 
MAS 
MAS started seeking views on the proposed amendments to the [[securities]] and Futures (Reporting of 
[[Derivatives]] Contracts) Regulations 2013 in July 2021. The commencement date for the MAS reporting rules 
changes is expected to be in October 2024 and confirmed via the second consultation response published on 
May 16. In the proposed close-to-final rules, there are 134 reportable data fields. ISO XML 20022 format is 
required for submissions when the rules commence. There will be an exemption for re-reporting of any 
information required for MAS Rewrite but previously was not captured at the point when the contract was 
executed. No re-reporting is required for contracts with a maturity of less than 6 months from the 
commencement of rules. 
There is no additional build expected in April 2025 for ASIC & MAS as the front to back functionality would 
already be built including the ingestion framework (full set of data fields including UPI and Delta, message 
response mechanism and methodology) and reporting framework (full set of end state reports) and portal 
functionality.  
Data migration is expected on Day 1 (ongoing discussion with /MAS). There are many considerations around 
how and what kind of data should be migrated. Analysis was done between the Rewrite and current data fields 
to see how the fields should be mapped. It was found that there were some fields that are too complex to be 
mapped due to many fields were being mapped into 1 field, the sheer amount of technical effort required or 
verification difficulty. There are some data type changes for some fields which we will be unable to migrate. 
How Day 1 TSR will look like will be dependent on data migration.  
Another consideration is the ISO XML 20022 schema which will be used for reporting in the upcoming Rewrite. 
The data fields will have to be mapped to the XML format which will be used by firms to submit their reporting.  
There are concerns for some fields like 
• UPI – Currently, ISDA taxonomy is used. The legacy value should be stored in a field as firms will have 
to report UPI when Re-writes start. Proposed field is Propriety UPI. For update of trades submitted 
before Re-writes, ASIC have stated that the UPI needs to be included as part of the re-reporting. 
• Non-LEI values reported by firms – Now, firms are able to report other values like AVOX and 
SWIFTBIC and DDRS will [[DO]] a lookup in SDO and report LEI values to the regulators. We should 
consider how to migrate such values and outreach to clients to report LEIs instead.  

---

## Page 64

 
 
• Duplicated trades – Post Re-writes, the uniqueness of the trade will be determined by UTI+ LEI of 
Reporting Party. Hence there will be some duplicate trades and a need to clean up those positions  
• Action type – Migrate status of trade instead of Action type. All open positions will be active. For 
update of trades submitted before Re-writes, firms will have to follow the combination of action type 
and event type. 
• Fields with fixed and floating – There is limitation as the xml schema splits this between fixed and 
floating. Currently, firms may have reported this differently for different [[Asset]] classes. 
The field set for Data migration for Rewrite is currently being discussed with ASIC and MAS. Keeping the 
considerations in mind and lots of in-depth analysis done, this will allow data migration to be done properly and 
transition to Rewrite to be as smooth as possible. 
FC 6.2:  [[DTCC]] Data Migration at Go-live – Trade State 
In order to support new functionality required to validate action type sequences once the rules commence for 
both ASIC and MAS, the GTR will need to maintain the status of every trade per the Action Type Sequence 
diagram (“Open”, “Terminated”, “Errored”, “Expired”, or “Transferred Out”), and use this status to compare to 
action types received on subsequent message submissions.  At go-live, this information about each trade will 
need to be migrated in the GTR application to support validations on submissions post go-live.  This migration 
will be performed per Trade and Jurisdiction (UTI + RCP).  Please refer to further information on Acti on Type 
Rules as defined in section FC 3.8.   
Not all the data fields can be migrated as the current data type for the fields may be different the future data 
standards. There are also new data elements that are added for ASIC and MAS Rewrite. Hence post 
migration, there is a need to review and re-report the migrated positions. 
Accordingly, GTR will perform the data migration at go-live: 
• On Day 0 at 18 October 2024 23:59 SGT, all active positions remaining will be taken as the eligible trade 
population for migration (i.e., trades which have not been exited on or before 18 October 2024, and whose 
expiration date is greater than 18 October 2024) will be migrated.  This will enable “stateful” validations 
which will prevent further NEWT submissions for these trades, and to allow for subsequent action types 
which would be allowed to follow Open trades.  
• The Primary Key for all positions with a future maturity date where the maturity date is equal to or greater 
than 19 October 2024 will be migrated to the Proprietary Identification field in the new database. Users will 
have to submit the Primary Key value into the Proprietary Identification tag 21 October 2024 onwards for 
the active positions that are migrated. A profiling exercise for trades will be carried out to ensure there are 
no special characters contained within the legacy primary key identifier. Users are informed to resubmit 
the legacy trades to remove special characters before go-live, however should they not take the 
necessary action, those trades will be excluded from the migration.  
• All other historical USI which are any trades that have matured, expired or terminated prior to 18 October 
2024 23:59 SGT and/or not migrated to the new architecture, will not be considered for migration. Any re-
reporting required to correct the historical record for these should be submitted starting with a “NEWT”.  
Please note that although these are historical trades, they must comply with all new validations.  

---

## Page 65

 
 
• For ASIC, there are 67 fields that are to be migrated. Examples of the fields that will be migrated are 
Primary Key, Trade Party 1, Trade Party 2 and maturity date. The full set of fields being migrated are 
finalized with ASIC. The draft of ASIC Trade Migration Specification can be found in this link. 
• MAS: Currently in discussion with MAS to finalize. 
• The current plan is to produce a CSV file that contains information on trades that are migrated on go-live. 
There will be a dry-run data migration which will be done prior go live. 
FC 6.3:  Removal of “Duplicate” Positions Due to Trade Uniqueness Change 
As noted in section FC 3.4, trade uniqueness changes will require the removal of “duplicate” trades at go -live.  
These are defined as open trades where there is the same value for (UTI + USI + OurRef) + RCP 1 and (UTI + 
USI + OurRef) + RCP 2. It is strongly recommended that users explicitly EXIT any duplicate positions prior to 
go-live so that they can control which trade remains for the given UTI / USI. 
However, if users [[DO]] not remove these duplicate open trades prior to go-live, [[DTCC]] will discontinue reporting 
them on the Trade State Report after go-live.  [[DTCC]] will select the open trade which has been most recently 
updated based on the latest message submitted timestamp as the position considered for initialization.  While 
[[DTCC]] will keep a record internally of what has occurred for these trades, explicit reporting of EXIT activity will 
not be provided to participants or regulators.  
FC 6.4: Trades with Special Characters in Trade Identifiers 
As the Unique Transaction Identifier (UTI) format post rewrite [[DO]] not allow special characters such as 
ampersand “&” to be submitted in the UTI value, [[DTCC]] will remove any open trades at go-live which contain 
special characters in the Primary Key which is either UTI, USI or TID.  
FC 6.5: Exclusion of Self Trades 
Self-trades would be excluded from the action type initialization. While they exist internally in the database 
today, they are not exposed to clients in any reports. Self-trades are defined as trades where the Counterparty 
1 and Counterparty 2 are the same. Post go-live, self-trades will be validated and rejected at ingestion.  
FC 6.6: Reporting During Transition Period 
After go-live, all reporting will be done using the new report formats. The submission and activity-based reports 
will reflect all data submitted in the new format after go-live.  
ASIC 
Users who are ready on 21 October 2024, are encouraged to re-report open positions when the rules 
commence, as full re-reporting is anyways required. Information that is not originally captured into systems 
need not be sourced and added to systems for re-reporting. [[DO]] note that the transition period of 180 days ends 
on 20 April 2025. 
 

---

## Page 66

 
 
MAS 
Re-reporting of outstanding contracts is to be done within 6 months when rules commence. There will be an 
exemption for re-reporting of any information required for MAS Rewrite but previously was not captured at the 
point when the contract was executed. 
FC 6.7: Go-Live Schedule 
A precise schedule of go-live weekend activities will be published separately closer to implementation.  At a 
high level, the production implementation plan is below: 
 
FC 7: Portal Changes 
There will be updates to the Global Portal. 
FC 7.1: Simulator UAT 
The Simulator is a web-based application built to provide users with a self-servicing utility and enables a user 
test and verify their submissions for the upcoming Rewrite in a stand-alone environment. 
The simulator will include database lookup validations for UPI against the UPI database which is a new feature 
(e.g. The current simulator does not validate against GLEIF for LEIs).  
For ASIC, the Simulator UAT is available in the portal on January 24, 2024.  
For MAS, the Simulator UAT will be done in 2 releases.  
• UAT Release 1 – FX [[Asset]] class, Valuation (VALU) and [[collateral]] (MARU): February 23, 2024  


---

## Page 67

 
 
• UAT Release 2 – All: March 20, 2024 
Please also note that the PSE - Global Industry Tools for the current ASIC and MAS reporting requirements will 
no longer be available. However, the existing Production Global Industry Tools will remain open so users will 
still be able to pre-validate trade submissions in line with the current trade reporting rules.  
FC 7.2: Trade Identifier Service 
Firms will be able to request for UTI generation using Trade Identifier Service in the Global Portal. This service 
enables generation of up to 1,000 Unique Trade Identifiers for trade submissions . UTI [[ID]] generated is a 
concatenated value of DDRS LEI and UTI [[ID]]. 
This is available for ASIC on January 24, 2024. 
1. DDRS LEI: 549300Q66C0HZ24OVJ18 
2. UTI [[ID]]: [[DTCC]]<YYYY><MM><DD>D<HH24><MINUTES><SECONDS><11 digit s random number> 
• Up to 32 characters long 
• Uppercase alphanumeric characters (A to Z and 0 to 9 only) 
Sample UTI [[ID]] generated: 549300Q66C0HZ24OVJ18DTCC20230928D12061910868058069 
It can be accessed through “PSE - GTR Industry Tools” tile by clicking on the “Identifier Service” menu [[Option]] 
and following the instructions below: 
1. Select the correct jurisdiction from drop down menu 
2. Enter the number of UTIs required (1 - 1,000) 
3. Click the “Generate” button 
4. Output Views: 
• “List View” provides UTI Prefix and UTI [[ID]] in csv format that can be downloaded by using the 
‘Download CSV’ button. 
• “JSON View” provides a JSON file that can be downloaded using the ‘Download JSON’ button.  
5. To begin a new request, click the “Reset” button 

---

## Page 68

 
 
 


---

## Page 69

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
Derivativeslearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 