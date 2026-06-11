---
title: "EMIR Refit Functional Change v0.4"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/EMIR%20Refit%20Functional%20Change%20Document%20v0.4.pdf"
pages: 50
size: "1471.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# EMIR Refit Functional Change v0.4

**Original File:** [EMIR Refit Functional Change Document v0.4.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/EMIR%20Refit%20Functional%20Change%20Document%20v0.4.pdf)  
**Category:** Other  
**Total Pages:** 50  
**File Size:** 1471.2 KB  

---

## Page 1

 
 
 
Global Trade Repository 
FUNCTIONAL CHANGE DOCUMENT: EMIR REFIT 
VERSION (0.4) 
FEB 2024 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 2

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]]. The services described herein are 
provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  
[[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal entity, subject to the laws and 
regulations of the particular country or countries in which such entity operates. Please see www.[[DTCC]].com for more 
information on [[DTCC]], its affiliates and the services they offer. 
Doc Date: February 2024 
Service: RDS 
Title: EMIR Refit Functional Change Document 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 3

 
 
Document Revision History 
Date Author Version Description 
24 May 2023 EMIR Product Team V01 Initial Draft 
02 Oct 2023 EMIR Product Team V02 FC 2.1: Inbound Message Types and Submission Formats -
Updating schema versions to reflect final revised technical 
documents published by ESMA in September 2023.  
FC 3.1 Message Validations – Message Specifications 
spreadsheet updated for the changes introduced by ESMA 
in September 2023.  
FC 3.1.1. [[OTC]] and ETD submission – Updated rationale for 
segregation of submissions by O-Code. 
FC 3.3 Trade Identifiers – Clarification provided on the 
usage of Global UTI versus existing legacy Trade IDs.  
FC 3.5 [[Margin]] Message Submissions – Updated to point to 
links to final revised technical documents published by 
ESMA in September 2023 and validation rules related to 
[[Margin]] submissions in relation to trade submissions and 
derivative states.  
FC 3.6 Trade Valuation Submissions - Updated to point to 
links to final revised technical documents published by 
ESMA in September 2023 
FC 3.7 Action Type & Event Type – Clarifying behaviour for 
Action Type = REVI, [[Margin]] submission Auth.108 Action 
Types (MARU, CORR) and allowable Action Type 
sequences.  
FC 3.10 Correcting Historical Data and Back Reporting.  
FC 4.1 Response Format – Updated to illustrate the 092 
schema and how to identify a transaction, error code, 
description in an ACK/NACK.  
FC 5.2 Reporting – Clarifying that Abnormal Values and 
Warnings about missing and outdated margins and missing 
and outdated valuations are part of a single report.  
FC 5.3 Report File Naming Conventions and key for reports 
delivered via SFTP (in XML) and XML and CSV reports 
displayed in Portal.  
FC 5.5 Repeatable and Schedules on CSV Reports – 
illustration of how they will display in CSV reports.  
FC 7.1 EU EMIR Data Harmonisation Exercise – illustration 
of the data migration and data harmonization to support 
ongoing lifecycle events reporting for legacy [[Derivatives]].  
05 Dec 2023 EMIR Product Team V03 FC 5.2 Report Types – clarification on Execution Agent. 
1 Feb 2024 EMIR Product Team V04 FC 4.3 Response Format Channel – clarification on 
ReplyToQueue approach 
 
 
 

---

## Page 4

 
 
TABLE OF CONTENTS 
Document Revision History ................................................................................................................................ 1 
1. Summary ....................................................................................................................................................... 6 
Background ......................................................................................................................................................... 6 
In-Scope .............................................................................................................................................................. 6 
Out of Scope ....................................................................................................................................................... 7 
Reference Documents ........................................................................................................................................ 7 
Naming Conventions and Definitions.................................................................................................................. 7 
2. Functional change requirements.................................................................................................................... 9 
FC 1: Connectivity: Message Channel, Routing and Submission Methods  ....................................................... 9 
FC1.1 sFTP Connectivity .................................................................................................................................. 9 
FC1.2 MQ Connectivity ...................................................................................................................................10 
FC 2: Ingestion – Message Types and Submission Formats ...........................................................................11 
FC 2.1: Inbound Message Types and Submission Formats ...........................................................................11 
FC 2.2: [[DTCC]] Wrapper and Business Data Header ......................................................................................12 
FC 2.3 Special Characters ..............................................................................................................................15 
FC 3: Ingestion - Processing of Submissions ...................................................................................................15 
FC.3.1: Message Validations ..........................................................................................................................15 
FC.3.1.1: [[OTC]] and ETD Submissions ............................................................................................................16 
FC 3.2: Message Sequencing .........................................................................................................................16 
FC 3.3: Trade Identifiers..................................................................................................................................16 
FC 3.4: Uniqueness of a Trade .......................................................................................................................17 
FC 3.5: [[Margin]] Message Submissions ...........................................................................................................17 
FC 3.6: Trade Valuation Submissions .............................................................................................................18 
FC 3.7: Action Type and Event Type ..............................................................................................................18 
FC 3.8: Mergers and Corporate Events ..........................................................................................................23 
FC 3.9: EU and UK EMIR Refit Usage Guidelines .........................................................................................23 
FC 3.10: Correcting Historical Data and Back reporting .................................................................................24 
FC 4: Message Responses ..............................................................................................................................25 
FC 4.1 Response Format ................................................................................................................................25 

---

## Page 5

 
 
FC 4.2 Response Format/Channel .................................................................................................................29 
FC.4.1: Response Error Codes (ACK/NACK Codes) .....................................................................................29 
FC 5: Reports ....................................................................................................................................................31 
FC 5.2: XML and CSV Report .........................................................................................................................32 
FC 5.1: Report Types ......................................................................................................................................32 
FC 5.2: Merging of Trade Valuation Information onto Trade State Report .....................................................39 
FC 6: Intra and Inter-TR Reconciliation ............................................................................................................45 
FC 6.1: Reconciliation Eligibility ......................................................................................................................45 
FC 6.2 Reconciling trades up to 30 days post maturity or termination ...........................................................45 
FC 6.3 Reconcilable Fields .............................................................................................................................45 
FC 6.4 Reconciliation Statuses .......................................................................................................................46 
FC 6.5: Reconciliation Tolerances ..................................................................................................................46 
FC 6.5: Reconciliation based upon Event Date ..............................................................................................46 
FC 6.6: Valuation Reconciliation .....................................................................................................................47 
FC 6.7: Reconciling trades with two legs ........................................................................................................47 
FC 6.8: Reconciliation of schedule information ...............................................................................................47 
FC 6.8: Reconciliation during the EMIR Refit Transition Period .....................................................................47 
FC 7: Functionality Specific to Go-Live ............................................................................................................47 
FC 7.1: EU EMIR Data Harmonization Exercise .............................................................................................47 
FC 7.2:  Upgrading Live (Outstanding) Trades post Go-Live..........................................................................49 
FC 7.3:  Reporting During Transition Period ...................................................................................................49 
FC 7.4:  Go-Live Schedule ..............................................................................................................................49 
 

---

## Page 6

fUNCTIONAL CHANGE DOCUMENT: emir REFIT 
Summary 6 
1. SUMMARY 
Background 
This document is a high-level overview of the [[DTCC]] implementation of EMIR Refit. 
The European Market Infrastructure [[regulation]] (EMIR)  is a [[regulation]] aimed at reducing systemic 
counterparty and operational risk and thereby prevent future financial system collapses. Its focus is [[regulation]] of 
over the counter ([[OTC]]) [[Derivatives]], central counterparties, and trade repositories. It provides steer on reporting 
of derivative contracts, implementation of  risk management standards and common rules for central 
counterparties and trade repositories.  
 
EMIR mandates reporting of all [[Derivatives]] to Trade Repositories (TRs). TRs centrally collect and maintain the 
records of all derivative contracts. They play a  central role in enhancing the transparency of derivative markets 
and reducing risks to financial stability.  EMIR establishes the reporting obligation on both counterparties that 
should report the details of the derivative trades to one of the trade reposi tories (TRs), i.e., the buying party 
should report, and the selling party should report. EMIR also requires reporting of the transaction details for both 
types of [[Derivatives]] trades – exchange traded [[Derivatives]] (ETD) and [[OTC]] [[Derivatives]]. Credit, Interest Rates, 
Equities, Commodities and FX [[Derivatives]] transactions must be reported under EMIR.    
 
The purpose of the EMIR REFIT is to amend and simplify the EMIR [[regulation]] “to address the disproportionate 
compliance costs, transparency issues and insufficient access to clearing for certain counterparties”. 
In-Scope  
The scope of this document will cover the following changes: 
Items Description 
Compliance 
Date 
EU EMIR Refit: April 29th 2024 
UK EMIR Refit: September 30th 2024 
UPI Under the rules of EMIR Refit Trade Repositories must validate that the UPI is valid per the DSB UPI 
database.  
LEI LEI will be mandated for a number of fields including the Reporting Counterparty (RCP), Entity 
Responsible for Reporting (ERR), Clearing [[Member]], [[Broker]] [[ID]] and Central Counterparty.  
UTI UTI will be mandated for trade reporting. For all reporting post the go live of EMIR Refit the logic to 
determine trade uniqueness will be based upon the UTI +Trade Party 1.  
ISO XML 
ISO XML will be mandated for inbound messages  to the Trade Repository  
ISO XML schema does not support cross jurisdiction reporting.  
 
Each authority (FCA and ESMA) has published their respective schemas and Usage Guidelines. 
FPML FpML will be decommissioned with the mandate for ISO XML. We will no longer support FpML for 
EU and UK EMIR reporting. 
CSV 
CSV submissions will be decommissioned with the mandate of ISO XML. We will no longer support 
CSV for EU and UK EMIR reporting.   
This includes the decommissioning of the Harmonized , [[OTC]] Core , EU Lite and [[collateral]] legacy 
submission templates. 

---

## Page 7

fUNCTIONAL CHANGE DOCUMENT: emir REFIT 
Summary 7 
Trade Linking 
Logic The trade linking logic will only be based on UTI +Trade Party 1 
Data 
Harmonization 
It is incumbent on Trade Repositories to complete a harmonization exercise to align all EMIR data to 
the technical standards of EMIR Refit. Please see the ESMA Mapping Between Standards document 
published to the [[DTCC]] Learning Center.  
Message 
Specifications 
The message specifications that will support the requirements of the new [[regulation]] have been 
published by ESMA and the FCA respectively. [[DTCC]] specific requirements, such as [[DTCC]] Wrapper 
and Business Application Header have been outlined on the [[DTCC]] Learning Center. 
Message 
Types 
Trade Activity and Trade Valuations submissions will be supported by the Auth.030 XML Schema.  
[[Margin]] Activity submissions will be supported by the Auth.108 XML Schema. 
Reports 
Outbound to the regulator is XML format.  
For clients there will be a choice of the Regulatory XML reports and CSV output.  
Action Type / 
Event Type 
Rules 
Action Type and Event Type Orchestration Rules will be newly implemented 
 
Out of Scope 
This project will not include: 
• Ingestion of FpML and CSV format submissions into the trade repository is out of scope for this delivery. 
TRs will only be able to ingest submissions in an XML format.   
Reference Documents  
This document should be read in conjunction with the following documents: 
1. The EU EMIR Message Specification and all other documents related to this implementation will be 
available on the “EMIR Refit” section under the of the [[DTCC]] Learning Center. 
EU EMIR Regulatory Document will be published on the ESMA website at the following link: 
https://www.esma.europa.eu/data-reporting/emir-reporting 
2. UK EMIR Regulatory Document will be published on the ESMA website at the following link: 
https://www.fca.org.uk/markets/uk-emir 
 
Naming Conventions and Definitions 
Abbreviation/ 
Term Name Definition/Description 
ACK GTR Success Acknowledgement Message 
Channel A unidirectional link between two end points or queue managers that serves to transfer 
messages 

---

## Page 8

fUNCTIONAL CHANGE DOCUMENT: emir REFIT 
Summary 8 
Abbreviation/ 
Term Name Definition/Description 
CSV Comma Separated Values – a submission format accepted for messages in GTR 
[[DTCC]] The Depository Trust and Clearing Corporation 
FpML Financial Product Markup Language – XML based submission type for the GTR and Canada 
PPD 
GTR Global Trade Repository 
ESMA European [[securities]] and Markets Authority 
LEI Legal Entity Identifier 
MQ Message Queue – message-oriented middleware. Provides mechanism for applications to 
communicate. 
Message 
Specification 
Instructions for submitting into a given GTR application. Includes data attribute requirements, 
valid values, validations, submission layouts and parsing definitions.  This document can be 
found on the Learning Center. 
NACK GTR Negative Acknowledgement message 
O-Code Operations Code – used to segregate and permission accounts 
OCP Other Counterparty (also referenced as Trade Party 2 generically) 
RCP Reporting Counterparty (also referenced as Trade Party 1 generically) 
SDO Account Management System that [[DTCC]] uses to define accounts, products and services 
associated with these participants 
SFTP Secure File Transfer Protocol 
Trade State Trade state is the state of the derivative position created by the latest trade message that has 
been received and processed by GTR. 
TSR Trade State Report.  Daily report of all outstanding [[Derivatives]] transactions (with latest 
valuation information merged onto the report). 
UAT GTR Test Environment (“User Acceptance Testing”) 
UPI Unique Product Identifier 
UTI Unique Trade Identifier 
XML In this document, refers to ISO 20022 XML 
 

---

## Page 9

 
 
2. FUNCTIONAL CHANGE REQUIREMENTS 
FC 1: Connectivity: Message Channel, Routing and Submission 
Methods  
There will be no changes to the current submission methods supported by the GTR. The GTR will continue to 
offer users the ability to connect to the trade repository through the same existing protocols to submit or 
receive data. These are via the web portal, MQ and sFTP. 
It should be noted that the ISO XML message does not support a Reporting Obligation field therefore multi-
jurisdictional submission routing will not be supported post the implementation of EMIR Refit. The following 
submissions principles will be followed:  
(i)  The web upload feature that is offered through the Portal/GUI will only support direct upload to the 
jurisdiction service that the user selects on the screen. 
(ii) The dedicated sFTP product [[ID]] for EU and UK EMIR will determine the destination / jurisdiction 
service where the GTR must send the file. New Product IDs will be set up for EU and UK EMIR Refit. 
(iii) The dedicated message queues for EU and UK EMIR Refit will determine the destination / 
jurisdiction service to direct user submissions.  
File based web upload or sFTP submissions will allow for multiple records (trade activities or [[Margin]] activities) 
within a file, however MQ submissions will be based on single record (trade activity or [[Margin]] activity) per 
message. Trade activity and [[Margin]] activity submissions should not be comingled in a single file as trade 
activities and [[Margin]] activities are reported using different ISO 20022 XML schemas.  
For more information on the configuring sFTP and MQ  functionality please refer to the Connectivity section of 
the Learning Center.  The relevant starter packs are referenced below.  
• GTR JFSA Rewrite and EMIR Refit sFTP Connectivity Starter Pack 
• GTR JFSA Rewrite and EMIR Refit MQ Starter Pack 
FC1.1 sFTP Connectivity  
 
EMIR Refit Product IDs:  
With the implementation of the EMIR Refit project there will be a suite of new report Product IDs that must be 
provisioned to allow GTR users to submit into the GTR. Additionally there is a suite of new outbound  reporting 
product IDs that must be provisioned to allow GTR users to receive reports back via sFTP. Please refer to the 
Connectivity Starter Pack available on the [[DTCC]] Learning Center for more details. 
Network Connectivity  
With the implementation of the EMIR Refit project all reporting via sFTP will be made available on the [[DTCC]] 
distributed servers. Please refer to the Connectivity Starter Pack available on the [[DTCC]] Learning Center for 
more details. 
  

---

## Page 10

 
 
FC1.2 MQ Connectivity 
 
EMIR Refit MQ Network Connectivity 
Reporting via the MQ protocol will be available on the existing Mainframe servers (system) with the 
implementation of the EMIR Refit project. Clients should continue to connect to the existing [[DTCC]] MQ Queue 
Managers and, channels on these queue managers, c an also be re-used. Whilst the existing Queue Managers 
and Channels can be reused with the implementation of the EMIR Refit project it should be noted that GTR users 
will be required to target new EU EMIR Refit queues. Please refer to the Connectivity Star ter Pack available on 
the Learning Center.  
EMIR Refit MQ Routing  
As part of the EMIR Refit implementation, GTR users will also have to configure Dynamic Response Queue 
routing utilizing MQ’s ReplyToQ functionality , which is defined in the MQ Header (MQMD). Ple ase refer to the 
MQ support guide also available in the GTR JFSA Rewrite and EMIR Refit MQ Starter Pack for more details. 
For reference the new EU EMIR Refit Input queues have been outlined below:  
EU EMIR Refit MQ Input Queues  
Description Queue Manager [[DTCC]] Input Alias Queue Name 
[[DTCC]] input queue for EU EMIR (Refit) MU1R, MP1R GTR.EMIR_COMMODITY.A01 
[[DTCC]] input queue for EU EMIR (Refit) MU1R, MP1R GTR.EMIR_CREDITS.A01 
[[DTCC]] input queue for EU EMIR (Refit) MU1R, MU2R, MP2R GTR.EMIR_EQUITY.A01 
[[DTCC]] input queue for EU EMIR (Refit) MU1R, MP5R-MP9R GTR.EMIR_FX.A01 
[[DTCC]] input queue for EU EMIR (Refit) MU1R, MP1R GTR.EMIR_RATES.A01 
[[DTCC]] input queue for EU EMIR (Refit) MU1R, MP1R GTR.EMIR_MARGIN.A01 
 
Please note the MQ queues for the UK EMIR Refit implementation have not been provisioned as yet. Details of 
these queues will be included in a future version of this document.  
  

---

## Page 11

 
 
FC 2: Ingestion – Message Types and Submission Formats 
FC 2.1: Inbound Message Types and Submission Formats 
It should be noted that with the implementation of EU and UK EMIR Refit all legacy CSV and FpML message 
formats will no longer be supported by the GTR. All submissions into the EU and UK EMIR trade repository 
must be in the regulatory ISO 20022 XML schema. Both ESMA and the FCA have published their own version 
of the ISO Schema. Details of these XML schemas can be found at the links below:  
EU EMIR Refit ISO XML Schemas and Validation Rules 
• Validation rules, reconciliation tolerances and template for notifi cation of errors and omissions in 
reporting (applicable from 29 April 2024) 
• XML EMIR Reporting Schemas 
o Incoming messages (applicable from 29 April 2024) 
The following ISO Schemas should be used for reporting into the EU EMIR Trade Repository:  
 
Message Type Action Type Schema Requirements 
Trade Activity New derivative – NEWT auth.030.001.03_ESMAUG_DATTAR_1.1.0  
Trade Activity Modification – MODI auth.030.001.03_ESMAUG_DATTAR_1.1.0  
Trade Activity Correction – CORR auth.030.001.03_ESMAUG_DATTAR_1.1.0  
Trade Activity Early Termination - TERM auth.030.001.03_ESMAUG_DATTAR_1.1.0  
Trade Activity Error – EROR auth.030.001.03_ESMAUG_DATTAR_1.1.0  
Trade Activity Revive – REVI auth.030.001.03_ESMAUG_DATTAR_1.1.0  
Trade Activity Position Component - POSC auth.030.001.03_ESMAUG_DATTAR_1.1.0  
Trade Activity Valuation – VALU auth.030.001.03_ESMAUG_DATTAR_1.1.0  
[[Margin]] Activity [[Margin]] update – MARU auth.108.001.01_ESMAUG_DATMDA_1.1.0  
[[Margin]] Activity [[Margin]] Correction - CORR auth.108.001.01_ESMAUG_DATMDA_1.1.0  
 
UK EMIR Refit ISO XML Schemas and Validation Rules 
• Final UK EMIR Validation rules (applicable from 30 September 2024).  
• XML Schemas under UK EMIR (applicable from 30 September 2024).  
o Incoming messages 
The following ISO Schemas should be used for reporting into the UK EMIR Trade Repository:  
Message Type Action Type Applicable Schema  
Trade Activity New derivative – 
NEWT 
auth.030.001.03_FCAUG_DATTAR.0.0.1 

---

## Page 12

 
 
Message Type Action Type Applicable Schema  
Trade Activity Modification – MODI auth.030.001.03_FCAUG_DATTAR.0.0.1 
Trade Activity Correction – CORR auth.030.001.03_FCAUG_DATTAR.0.0.1 
Trade Activity Early Termination – 
TERM 
auth.030.001.03_FCAUG_DATTAR.0.0.1 
Trade Activity Error – EROR auth.030.001.03_FCAUG_DATTAR.0.0.1 
Trade Activity Revive – REVI auth.030.001.03_FCAUG_DATTAR.0.0.1 
Trade Activity Position Component – 
POSC 
auth.030.001.03_FCAUG_DATTAR.0.0.1 
Trade Activity Valuation – VALU auth.030.001.03_FCAUG_DATTAR.0.0.1 
[[Margin]] Activity [[Margin]] update – MARU auth.108.001.01_FCAUG_DATMDA.0.0.1 
[[Margin]] Activity [[Margin]] Correction – 
CORR 
auth.108.001.01_FCAUG_DATMDA.0.0.1 
FC 2.2: [[DTCC]] Wrapper and Business Data Header 
In addition to the regulatory XML ISO schemas the following additions must be included  to report to the Global 
Trade Repository under the rules of EMIR Refit.  
[[DTCC]] Wrapper  
The [[DTCC]] wrapper has two branches. 
• The first branch is a [[DTCC]] extension which was approved  by ESMA to contain an optional tag for 
market participants that want to identify the Execution Agent of the Reporting Counterparty as part 
of their submission.  Note: Execution Agent  is not a field in the ESMA ISO 20022 Incoming 
Messages Authority schemas for the submission of [[Derivatives]] Trade Activity and [[Margin]] Activity. 
Please see the EU EMIR Refit [[DTCC]] Message Specification for more details.  
• The second branch contains the Business Data Header message structure.  
• Please note the [[DTCC]] Wrapper is only applicable for reporting under EU EMIR REFIT. The [[DTCC]] 
Wrapper should not be populated when submitting under UK EMIR REFIT. Submissions under UK 
EMIR REFIT should only be made using the Business Data Header. Please see the learning center 
for templates, samples and more details.  
Business Data Header 
The Business Data Header has two branches: Header and Payload:  
• Header: The Header contains the Application Header (ISO20022 message definition 
head.001.001.0x) has been defined  by the ISO 20022 community and can be combined with any 

---

## Page 13

 
 
other ISO20022 message definition to form a business message. The Application Header contains 
five mandatory components: 
o From – must contain an O-code identifying the sender 
o To – identifies the receiver of the submission i.e. DDRIE 
o Business Message [[ID]] - holds a submission identification 
o Message Definition [[ID]] – identifies the schema reflected in the Payload 
o Creation Date – contains the submission creation date 
• Payload: The Payload contains the ESMA ISO  20022 Authority Schemas for the [[Derivatives]] 
submissions for Trade Activity and [[Margin]] Activity. 
 
UK EMIR REFIT and EU EMIR REFIT submission schemas:  
As previously stated, under EMIR REFIT, the EU and UK TRs will only be able accept submissions in an ISO 
XML format. The distinct submission schemas that must be used have been outlined below:  
 
Incoming 
Message Type 
Incoming Message Schema 
EU EMIR Refit UK EMIR Refit 
Trade Activity auth.030.001.03_ESMAUG_DATTAR_1.1.0  auth.030.001.03_FCAUG_DATTAR.0.0.1 
[[Margin]] Activity auth.108.001.01_ESMAUG_DATMDA_1.1.0  auth.108.001.01_FCAUG_DATMDA.0.0.1 
 
 
 
 
 
 
  

---

## Page 14

 
 
Format for submitting under EU EMIR Refit:  
The below diagram outlines the format for which users of the GTR should be submitting messages 
under EU EMIR Refit.  
 
Format for submitting under UK EMIR Refit:  
The below diagram outlines the format for which users of the GTR should be submitting messages 
under UK EMIR Refit. As you can see from the diagram below the [[DTCC]] wrapper is not to be used 
when submitting under UK EMIR REFIT.  
 
  


---

## Page 15

 
 
FC 2.3 Special Characters 
All submissions must have the characters set to UTF-8.   
Generally, the  ISO schema expects that all characters should be alphanumeric. Fields are generally 
alphanumeric unless otherwise explicitly mentioned in the message specifications. [[DTCC]] will implement 
validations in this regard as per the published Validation Rules and EU and UK EMIR Refit Usage Guidelines. 
FC 3: Ingestion - Processing of Submissions 
FC.3.1: Message Validations  
Whilst there are largescale changes to the EU and UK EMIR REFIT Business Validation rules with the 
implementation of the new regulations it should be noted there will be no changes to the [[BASIC]] process by 
which messages are validated by the GTR.  The validation process includes:  
• Schema Validation (validates that the message is formatted correctly so that it can be parsed)  
• Permission Validation (validates that the submitter has permission to submit the message) 
o The submitter must be onboarded to submissions to the EMIR Refit TR 
o The submitter must be explicitly permissioned by the reporting counterparty or entity 
responsible for report to submit on their behalf 
• Core Validation ([[BASIC]] global validations as defined in the Message Specifications)  
• Jurisdictional Validation (validations specific to each jurisdiction as defined in the Message 
Specifications) 
 
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
 
 
Further details on validations performed on each submission can be found in the Message Specifications 
spreadsheet in the EU EMIR Refit Message Specs and Templates (UAT) .zip file. Please note the UK EMIR 
REFIT validation rules and Message Specifications  are also published on the Learning Center .  
 

---

## Page 16

 
 
FC.3.1.1: [[OTC]] and ETD Submissions  
Whilst [[OTC]] and ETD trades will be reported under an aligned format/message template with the 
introduction of a standardized ISO XML schema clients must continue to submit ETD and [[OTC]] trades 
separately via the existing O-Codes in place for submitting ETD and [[OTC]] messages. This segregation 
is due to Trade Repository processing and not a regulatory requirement. Additionally, in this case the 
reference to “ETD” is applicable for all conventional ETD trades and not just those designated as ETD 
under the jurisdictional EU and UK EMIR rules.  Failure to [[DO]] so will result in the trades submitted 
under the wrong OCODE being rejected.  
[[collateral]] O-Code =  0XXX 
[[OTC]] O-Code =  8XXX, 6XXX, 5XXX, 4XXX, 3XXX, 2XXX 
ETD O-Code =   7XXX 
 
FC 3.2: Message Sequencing  
There will be no changes to the way messages are processed in the GTR in terms of sequencing. If messages 
related to the same trade are submitted in sequence within the same channel or file (MQ or SFTP or Web 
Upload) then [[DTCC]] will process those messages in the order received.  Sequencing cannot be guaranteed 
when messages related to the same trade are submitted across different channels . For users that may have 
multiple connections to the same SFTP site and intend to send files in quick succession it is recommended to 
use the same connection or otherwise wait until an acknowledgement is received before sending another file in 
from a different connection. 
Please note that message responses over MQ may be returned in a different sequence than the original 
submission due to load balancing functions in the GTR.  This does not mean that the messages have been 
processed out of sequence. 
FC 3.3: Trade Identifiers  
For [[Derivatives]] concluded on or after EU and UK EMIR REFIT, a global UTI that adheres to ISO 23897 
standards must be reported when using Action Type “NEWT” and “POSC”.  
Legacy Trade IDs for existing outstanding [[Derivatives]] can continue to be reported in the UTI field when 
reporting amendments or lifecycle events to the existing outstanding [[Derivatives]] after EU and UK EMIR Refit 
go live. The legacy Trade IDs [[DO]] not need to adhere to the ISO 23897 standards.  
Within the Action Type block of the Auth.030 schema, the UTI field has different layouts for Action Types = 
NEWT/POSC versus the other Action Types.  
For Action Type = NEWT/POSC, as this is supposed to be used when reporting newly concluded [[Derivatives]] 
on and after EMIR REFIT goes live, the UTI field has 1 end point  (../CmonTradData/TxData/TxId/UnqTxIdr'). 
The x-path ../CmonTradData/TxData/TxId/UnqTxIdr should be used when reporting [[Derivatives]] concluded on 
and after EMIR REFIT goes live and their associated lifecycle events. This x -path has a strict data type and 
format of "[A-Z0-9]{18}[0-9]{2}[A-Z0-9]{0,32}", meaning 52 upper case alphanumeric where the first 18 
characters are uppercase alphanumeric, the 19th and 20th characters are numeric only, and the remaining 
characters are uppercase alphanumeric. No special characters are allowed on this x-path.  
On all other Action Type blocks (i.e. Action Type <> NEWT/POSC), the UTI field has 2 end points 
(../CmonTradData/TxData/TxId/UnqTxIdr and .../CmonTradData/TxData/TxId/Prtry/[[ID]]) for Action Type <> 
NEWT / POSC.  
The x-path .../CmonTradData/TxData/TxId/Prtry/[[ID]] should be used when reporting [[Derivatives]] concluded 
before EMIR REFIT goes live (i.e. legacy [[Derivatives]]) and their associated lifecycle events. This x -path in the 
schema allows for up to 72 text characters including special characters, but as per the validation rules, there 

---

## Page 17

 
 
are jurisdictional validation rules that restrict the value to up to 52 alphanumeric characters and only four 
special characters are allowed ":", ".",  "-", " _" .  Special characters are not allowed at the beginning or the end. 
FC 3.4: Uniqueness of a Trade  
Currently, trade uniqueness is defined as follows: 
• The uniqueness of a trade is determined by the concatenation of Trade [[ID]] + Trade Party 1 + Trade 
Party 2. This is often referred to as the “Triplet”. 
With the introduction of the new EMIR Refit rules trade uniqueness for anything submitted as “NEWT” and 
“POSC” will be determined as follows:  
• For EMIR reporting the uniqueness of a trade will be determined by the concatenation of UT I + Trade 
Party 1. This will be referred to as the “Duplet”.  
It should be noted that this logic will be implemented for new [[Derivatives]] that are reported post the go live of 
EU and UK EMIR Refit. All existing [[Derivatives]] within the respective EU and UK EM IR trade repositories will 
remain unique at the level of the Triplet.  
Additionally, whilst [[OTC]] and ETD must continue to be reported separately into the GTR (See section FC 3.1.1) 
a UTI must be completely unique across both. For clarity this means that if a UTI was reported under an ETD 
O-code (i.e. 7XXX) then it cannot be recycled and also reported under an [[OTC]] O code (i.e. 8XXX or 2 to 
6XXX) by a single counterparty. 
Please note that this change in uniqueness for new submissions post the implementation of  EMIR Refit is a 
regulatory requirement outlined in the EMIR Reporting Guidelines.  
FC 3.5: [[Margin]] Message Submissions 
[[collateral]] must continue to be reported under the rules of UK and EU EMIR Refit. To align with the regulatory 
terms, [[collateral]] will be referred to as [[Margin]] going forward.  
The main changes and key points for reporting [[Margin]] under EU and UK EMIR Refit are as follows:  
• [[Margin]] messages can only be submitted in an XML format. Submissions via CSV will not be accepted 
post the implementation of EU and UK EMIR Refit.  
• The applicable ISO schema for reporting [[Margin]] updates under EU and UK EMIR Refit are defined in 
section 2.2 above. Links to the EU and UK EMIR Refit schemas are provided in section 2.1 above. .  
• Post the implementation of the new EU and UK EMIR Refit rules [[Margin]] will continue be reported via 
the O-code “0” (for example “0XXX”).  
• These messages can be submitted via Web Upload, SFTP and MQ.  
• Under the [[Margin]] Activity schema there are two allowable Action Type values:  
o “MARU” for [[Margin]] Update 
o “CORR” for [[Margin]] Correction  
• Submission permissions will work the same as for all other message types.  
• Validations will be performed as specified in the Message Specifications. 
• The [[collateral]] Link message as used today will no longer be available with the introduction of the new 
EU and UK EMIR Refit rules. Any submissions using the legacy [[collateral]] Link message will be 
rejected.  
• Trades collateralised at a portfolio level can be reported as such using the Trade activity schema 
(Auth.030) and populating the [[collateral]] Portfolio Indicator and [[collateral]] Portfolio Code fields.  
Trade Level or Portfolio Level [[collateral]]  
• [[Margin]] submissions are either at trade or portfolio level.   

---

## Page 18

 
 
• For trade level [[Margin]] submissions:  
o Trade-level [[Margin]] submissions must contain a UTI. 
o The [[Margin]] update submission will only be accepted if the Event Date reported for the unique 
position (using either the duplet (UTI + RCP) or triplet (UTI + RCP + OCP) ) is equal or greater 
than the Execution Timestamp or equal or less than the Expiration Date (if populated) or equal 
or less than the Early Termination Date (if populated)  
o [[collateral]] Portfolio Indicator must be “false”. 
• For Portfolio-level [[collateral]] ([[Margin]] Activity) submissions: 
o If [[collateral]] is reported on a portfolio basis, a unique code assigned by counterparty 1 to the 
portfolio must be reported in the [[collateral]] portfolio code field 
o A portfolio-level [[collateral]] submission does not need to have the UTI field.  
o The portfolio level [[Margin]] submission will only be accepted if the Event Date reported for the 
portfolio is equal or greater than the earliest Execution Timestamp of the UTIs in the portfolio 
or equal or less than the latest Expiration Date (if populated) of the UTIs in the portfolio, or 
equal or less than the latest Early Termination Date (if populated) of the UTIs in the portfolio.   
o [[collateral]] Portfolio Indicator must be reported as “true”. 
• [[Margin]] cannot be reported for a unique derivative position that has been errored out (with the 
submission of Action Type = EROR). [[Margin]] cannot be reported for a portfolio where all UTIs in the 
portfolio have been errored out.  
 
It should also be noted [[Margin]] submission information will not be merged onto the Trade State Report but will 
be reported on a daily [[Margin]] Submission Report, [[Margin]] Activity Report and [[Margin]] State Report. For further 
information on the availability of [[Margin]] reports please refer to the Reporting section of  this document (FC 5 
Reports). 
FC 3.6: Trade Valuation Submissions 
Trade Valuation messages will continue to be applicable for EU and UK EMIR REFIT reporting. 
• Trade Valuations need to be submitted to the GTR daily through a Valuation message indicated by 
Action Type “VALU”. The applicable ISO schema for reporting trade valuation updates under EU EMIR 
REFIT and UK EMIR REFIT are outlined in section 2.1 and 2.2 above. Valuations will only be accepted 
if there is an established unique position identified using the duplet (UTI + RCP) or triplet (UTI + RCP + 
OCP).  
• The valuation submission will be reported as activity in the Trade Activity Report and Trade 
Submission Report. Any reported Trade Valuations will be reflected in the next applicable Trad e State 
Report.  
FC 3.7: Action Type and Event Type  
ESMA and the FCA have both introduced the concept of the “Event Type” field. This field allows for reporting of 
the business reason behind the submission and is used in conjunction with the Action Type. The Action Type 
field can be considered “the What” (e.g. what is being reported – a modification) and the Event Type can be 
considered “the Why” (e.g. why is a modification being reported). All trade submissions received post go -live 
must contain the applicable “Action Type” and “Event Type” values. It shoul d be noted that the Event Type field 
is not applicable for certain Action Types on the Trade Activity submission and when submitting [[Margin]] 
activities.    
Action Type: 
Whilst the Action Type field is an existing concept it should be noted that there will b e two new reportable 
values and one reportable action type has been removed.  

---

## Page 19

 
 
• Action Type = REVI/Revive: this field will allow for the reviving of the UTI of a trade that was previously 
cancelled with action type ‘EROR’ or where a derivative position was early terminated by mistake with 
action type “TERM” or if a derivative position was reported with an incorrect Expiration Date and 
consequently naturally expired when it arrived at that incorrect date 
• Action Type = MARU/[[Margin]] Update: this field will allow for submission of [[Margin]] updates. Under the 
current rules of EMIR [[Margin]] updates and trade valuations are reported using an action type = V. Post 
go live [[Margin]] updates will only be accepted utilizing a [[Margin]] activity schema (Auth.108) with action 
type MARU. Corrections to previously reported [[Margin]] updates can be done using [[Margin]] activity 
schema (Auth.108) with action type CORR. Trade valuations will only be accepted when reported 
using the trade activity schema (Auth.030) with an action type = VALU.  
• Action Type = Z: this field will no longer be supported post the go live of EMIR Refit. Post trade risk 
reduction events such as compressions will be indicated using the Event Type field.  
Note: Action Type = CORR is an existing value that can be used on both trade activity schema (Auth.030) and 
[[Margin]] activity schema (Auth.108). When used on a trade activity schema (Auth.030), it is a report correcting 
the erroneous data fields of a previously submitted trade activity submission. When used on a [[Margin]] activi ty 
schema (Auth.108), it is a report correcting the erroneous data fields of a previously submitted [[Margin]] activity 
submission.  
The applicable values that are reportable for the Action Type field are defined below:  
Action Type Value Description  New or E xisting 
Concept  
New NEWT A report of a derivative, at a trade or position level, for the first time Existing 
Modify MODI A modification to the terms or details of a previously reported 
derivative, at a trade or position level, but not a correction of a 
report 
Existing 
Correct CORR A report correcting the erroneous data fields of a previously 
submitted report 
Existing 
Terminate TERM A termination of an existing derivative at a trade or position level.  Existing 
Error EROR A cancellation of a wrongly submitted entire report in case the 
derivative, at a trade or position level, never came into existence 
or was not subject to [[regulation]]  (EU) No 648/2012 reporting 
requirements but was reported to a trade repository by mistake or 
a cancellation of a duplicate report.                         
Existing 
Revive REVI Re-opening of a derivative, at a trade or position level, that was 
cancelled with action type ‘Error’ or terminated by mistake.  
New 
Valuation  VALU An update of a valuation of a derivative.      Existing 
Position 
Component  
POSC A report of a new derivative that is included in a separate position 
report on the same day. 
Existing 
[[Margin]] Update MARU a new [[Margin]] balance or a modification of the details of the 
margins shall be identified as ‘[[Margin]] update’; 
New 
 

---

## Page 20

 
 
 
 
 
 
The diagram below outlines the Action Type Sequence that the Trade Repository will be able to accept:  
 
 
Source: Paragraph 108, ESMA74-362-2281_final_report_guidelines_emir_refit  
 
The key points from this diagram have been outlined below. 
 
• The first submission to establish the traded derivative position must always be via an action type 
NEWT or POSC. 
• No specific action type submission is required when a trade naturally retires per its Expiration Date 
(Field 2.44).   
• The diagram above outlines the process that will logically move trades from “outstanding” to “non-
outstanding” status.   
• MODI,CORR and VALU action type submissions to expired or terminated trades are allowed so 
participants can update the historical records (indicated through the population  of the Event Date field). 
EROR is allowed on Terminated (Non-Outstanding) positions as well as outstanding positions. REVI 
are also allowed on positions that are non-outstanding (Condition 5 for field 2.151). 
• When a trade is Early Terminated (TERM) or  Errored (EROR), its status will change from outstanding 
to non-standing and it will not appear on the Trade State Report.  


---

## Page 21

 
 
• When a trade is added to a Position Component (POSC) on the Level = TCTN (Transaction), its status 
changes from Not-Reported to Terminated (Non-Outstanding) and it will also not appear on the Trade 
State Report.  
• Once a trade is Early Terminated or Errored the only way for it to appear again on the TSR is through 
the submission of a REVI. If the Expiration Date reported on the REVI is in the future, the derivative will 
be made outstanding again and will then be visible once again on the Trade State Report.   
• Once a trade reaches its natural Expiration Date, it will appear on the TSR for the last time on the 
Event Date for the report that is equivalent to the Expiration Date and then never appear on the TSR 
again. They only way to have the position appear on the TSR after that point is through the submission 
of a REVI where the Expiration Date is set in the future.  
• Whilst MODI and CORR can be used to update previously reported data on [[Derivatives]] that are non-
outstanding, the dates that determine whether the derivative is outstanding or non -outstanding cannot 
be changed to change the state of the derivative. MODI and CORR submissions for a n on-outstanding 
derivative that attempt to change the derivative state to outstanding will be rejected.  
• Once a TERM message is submitted and ACK’d and the state becomes Terminated (Non -
Outstanding), a subsequent TERM submitted would be rejected because for  a non-outstanding 
derivative, only REVI and EROR is allowed.  
• Once an EROR message is submitted and ACK’d and the state becomes Errored (Non -Outstanding), 
a subsequent EROR submitted would be rejected because for a non-outstanding derivative, only REVI 
is allowed.  
• A NEWT submitted after a POSC for the same derivative position will be rejected. A POSC sent after a 
NEWT would also be rejected.  
• To preserve the data quality on reporting and to ensure ingestion and reporting are aligned, the 
Reporting Timestamp on subsequent submissions must be later than or equal to the Reporting 
Timetamp of the ACK’d NEWT/POSC or the later than or equal to the Reporting Timestamp of the last 
ACK’d submission.   
 
Stateful validations (i.e. validations that can only be performed by referencing previous submissions for the 
same trade) on the Action Type field control the allowable sequences of Action Types. Each new submission 
will be validated to confirm that the action type is consistent with the allowable sequence as per the action type 
state diagram above.  These validations will be performed per unique trade (see trade uniqueness section 3.4) 
and at a jurisdictional level.  
Event Type:  
The applicable values that are reportable for the new Event Type field are as follows:  
Event Type Value Description  
New or 
Existing 
Concept  
Trade TRAD Conclusion of a derivative or renegotiation of its terms 
that does not result in change of a counterparty New  
Step-In NOVA 
An event, where part or entirety of the derivative is 
transferred to a counterparty 2 (and reported as a new 
derivative) and the existing derivative is either 
terminated or its notional is modified.  
New  
PTRR COMP Post-trade risk reduction exercise        New  
Early Termination ETRM Termination of a derivative at a trade or position level           New  

---

## Page 22

 
 
Clearing CRLG Clearing as defined in Article 2 point (3) of [[regulation]] 
(EU) No 648/2012    New  
Exercise EXER The exercise of an [[Option]] or a swaption by one 
counterparty of the transaction, fully or partially. New  
Allocation  ALOC 
Allocation event, where an existing derivative is 
allocated to different counterparties and reported as 
new [[Derivatives]] with reduced notional amounts. 
New  
Credit Event CREV 
Applies only to credit [[Derivatives]]. A credit event that 
results in a modification of a derivative, at a trade or 
position level  
New  
Corporate Event CORP A corporate action on [[Equity]] underlying that impacts the 
[[Derivatives]] on that [[Equity]] New  
Inclusion in Position INCP 
Inclusion of CCP -cleared derivative or CFD into a 
position, where an existing derivative is terminated  and 
either a new position is created or the notional of an 
existing position is modified. 
New  
Update  UPDT 
Update of an outstanding derivative performed during 
the transition period in order to ensure its conformity 
with the amended reporting requirements 
New 
 
Action Type and Event Type Combinations:  
Whilst these are also specified in the Message Specification conditions the below table indicates the allowable 
combinations of Action and Event Type. Please note in the diagram below  ‘T’ represents Level = TCTN 
(Trade) submissions and ‘P’ represents Level = PSTN (Position) submissions.  
Event Type 
  
Trade 
Step-In 
PTRR 
Early Termination 
Clearing 
Exercise 
Allocation  
Credit Event 
Inclusion in 
Position 
Corporate Event 
Update  
No Event Type 
Required 
Actio
n 
Type 
New T T,P T   T T T   P T,P     
Modify T,P T,P T,P T,P   T,P T T,P P T,P T,P P 
Correct                       T,P 
Terminate   T,P T,P T,P T T,P T T,P T,P T,P     
Error             
  
      T,P 
Revive                       T,P 


---

## Page 23

 
 
Valuation                       T,P 
Position 
Component  
      
 
              T 
[[Margin]] Update                 
 
    T,P 
 
 
 
 
 
Action and Event Type Validations:  
Stateless validations restrict the valid combinations of the “Action Type”, and “Event Type” fields. The table 
above contains the valid combinations of the Action type and Event type field for Level = PSTN and TCTN.  
The above combinations can be validated solely based on content of the message they can be tested using the 
Simulator.   
Action Type Validations and the Transition Period 
For trades that are already “live” when EU and UK EMIR Refit is implemented, [[DTCC]] will harmonise the state 
of the derivative during go-live weekend to align it to EMIR Refit data technical standards (in accordance with 
the “mapping between standards” document published by ESMA). Post go-live submissions will be accepted 
according to these action type validations regardless of whether the trade was live pre EMIR Refit go live.  
FC 3.8: Mergers and Corporate Events   
Currently when a counterparty undertakes a Merger or Corporate Event that results in a change in LEI the Trade 
Repository must administer this change within its internal systems on behalf of the requestor. The rules for such 
Mergers or Corporate Events are currently specified under ESMA EMIR Q&A40. Under the rules of EMIR Refit 
the process for administering such Mergers or Corporate Events have now been amended and moved into the 
Regulatory Technical Standards. 
 
Further details on the GTR Mergers and Corporate Events process will be provided in a later version of this 
document.  
FC 3.9: EU and UK EMIR Refit Usage Guidelines 
Both ESMA and the FCA have published Usage Guidelines in support of their ISO 20022 XML schemas. T he 
usage guidelines define restrictions on the fields being submitted. For example, valuation data can be reported  
on an Action Type = NEWT if the valuation information is known at the time of reporting the NEWT or alternatively, 
valuation data should be reported using Action Type = VALU. The Action Type = VALU only contains valuation 
data points and as such details like ‘Execution Timestamp’ cannot be reported via an Action Type = VALU. The 
ISO Schemas and Usage Guidelines published by ESMA and the FCA have been outlined in section 2.1 above.   
 
Sample schema valid incoming messages for EU EMIR REFIT are published on the [[DTCC]] Learning Center. A 
similar set for UK EMIR REFIT will be published in due course.  


---

## Page 24

 
 
FC 3.10: Correcting Historical Data and Back reporting  
The EMIR Refit guideline 383 requires counterparties and ERRs to submit historical activities to Trade 
Repositories when identifying any data that was omitted or misreported in the past.  
 
For EU EMIR REFIT, guideline 564 requires the EU EMIR Trade Repository to have in place a process to re-
generate corrected historical TSRs when requested by authorities or counterparties (RSE, ERRs and RCP). 
Note: The exception to this scenario is when the historical submission is for a derivative position that was non -
outstanding as at EU EMIR REFIT Go Live. EU EMIR Trade Repositories will not be regenerating TSRs on the 
back of submissions such as these.  
 
Whilst UK Trade Repositories are expected to be able to ingest historical submissions, there is not equivalent 
requirement to regenerate historical TSRs.  
 
Historical Activities are any submissions (for derivative trade or [[Margin]] records) that are accepted and have an 
Event date that is more than 1 business day in the past from the Reporting Timestamp (date).  
 
Historical Activities may be categorized as one of the following types of activities: 
• Historical submission: when a trade or [[Margin]] activity  is submitted for trade or [[Margin]] record 
already reported to the trade repository where the Event date is more than 1 business day in the 
past from the Reporting Timestamp (date).  
• Late activity (back reporting): when a derivative position that has never been reported to the 
trade repository is submitted for the first time albeit late representing the NEWT/POSC trade 
activity where the E vent date is more than 1 business day in the past  from the Re porting 
Timestamp (date) 
 
A h istorical activity (late activity or historical  submission ) will be accepted  with an event date more than 1 
business day in the past, if the event date of the submission falls between the trade’s execution timestamp and 
expiration date (if populated) or early termination date if the trade is early terminated provided all other validations 
pass. Such historical activities will be used to update historical trade states and [[Margin]] states. 
 
The reporting processes will update the outstanding and non-outstanding derivative trade states or [[Margin]] states 
for past event dates from the event date of the historical activity until the event date on the next applicable activity) 
in the DDRIE data warehouse only. Historically corrected derivative trade state reports and [[Margin]] state reports 
are not automatically re-generated nor resent. 
 
Authorities will have to make an explicit request for any historical corrected [[Derivatives]] trade state or [[Margin]] state 
report to be re-generated and transmitted to them.  
 

---

## Page 25

 
 
Participants will be able to request an updated view of the corrected [[Derivatives]] trade state or [[Margin]] state 
through the Portal’s online trade state search service once the historical trade state and [[Margin]] states have been 
corrected. More details on this feature will be provided in future versions of this document.  
.  
FC 4: Message Responses  
FC 4.1 Response Format  
The message response format will be changing to XML instead of the current FpML or CSV response formats to 
align with the ISO XML inbound submission format.  
  
 
EU EMIR Response File:  
 
For EU EMIR responses will be generated in the schema specified below. The auth.092 schema will be used for 
the immediate response (i.e. ACK/NACK) and will provide details on whether the submi ssion was accepted or 
rejected by the trade repository. It should be noted this schema will also be used for the End of Day Rejection 
Results, which will provide a summary of submissions within a reporting day alongside a small number of 
statistics. Please see section 5 for more details.  
 
The excerpt from the XML message response schema (auth.092.001.03_ESMAUG_DATREJ_1.0.0) is shown 
below. The ACK/NACK status for a trade or [[Margin]] activity will be indicated in the red block below.  
 
…Rpt/RjctnSttstcs : In a file with multiple trade activities or [[Margin]] activities, this block will repeat per the number 
of activities in the file.  
…Rpt/RjctnSttstcs/DerivSttstcs/DtldSttstcs/TxsRjctnsRsn/DtldVldtnRule: this block is repeatable to illustrate all 
the errors on a specific trade or [[Margin]] activity.  
 
…Rpt/RjctnSttstcs/DerivSttstcs/DtldSttstcs/TxsRjctnsRsn/Sts will display the ACK/NACK status per activity (e.g. 
ACPT = Accepted, RJCT = Rejected, CRPT = Corrupted Message or File, NAUT = Not Authorised to submit to 
the TR). 
 
Where it is a NACK (i.e. RJCT = Rejected, CRPT = Corrupted Message or File, NAUT = Not Authorised to submit 
to the TR). 
 
…Rpt/RjctnSttstcs/DerivSttstcs/DtldSttstcs/TxsRjctnsRsn/DtldVldtnRule/[[ID]] will display the ESMA Error Codes or 
[[DTCC]] Proprietary Error Codes. 
…Rpt/RjctnSttstcs/DerivSttstcs/DtldSttstcs/TxsRjctnsRsn/DtldVldtnRule/Desc will display the ESMA Error Code 
Descriptions or [[DTCC]] Proprietary Error Code Descriptions.  
…Rpt/RjctnSttstcs/DerivSttstcs/DtldSttstcs/TxsRjctnsRsn/DtldVldtnRule/SchmeNm/ Cd will display the schema 
contained in the Payload of the incoming message that is being rejected. 
 

---

## Page 26

 
 
 
 
 
The ACK / NACK message response (auth.092.001.03_ESMAUG_DATREJ_1.0.0) generated by the GTR will 
provide the same BizMsgIdr used in the submitted file or message. It will be populated in the /BizMsgIdr tag as 
shown below (see highlighted in yellow).  
 


---

## Page 27

 
 
 
 
ESMA expect the identification of each submission in the ACK / NACK message response will be based on the 
Counterparty 1, RSE, ERR (…Rpt/RjctnSttstcs/CtrPtyId) (see purple box below) plus the Transaction [[ID]] 
(…Rpt/RjctnSttstcs/DerivSttstcs/DtldSttstcs/TxsRjctnsRsn/TxId) and its components (Action Type, Reporting 
Timestamp, Derivative Event Type, Derivative Event Date, Other Counterparty, UTI, [[collateral]] Portfolio Code) 
(see green box below).   
 


---

## Page 28

 
 
 
  
 
Sample files illustrating the XML response layouts for the different scenarios can be found on the Learning 
Center. 
 
UK EMIR Response File:  
For UK EMIR responses will be generated in the schema specified below.  
The auth.031 schema will be used for the immediate response (i.e.  ACK/NACK) and will provide details on 
whether the submission was accepted or rejected by the trade repository.  
It should be noted that this schema differs from that used for the End of Day Feedback File as this will be utilising 
the auth.092 schema in li ne with EU EMIR. The UK EMIR end of day report will also provide a summary of 
submissions within a reporting day alongside a small number of statistics. Please see section 5 for more details.  
 


---

## Page 29

 
 
 
FC.4.2: Response Error Codes (ACK/NACK Codes) 
Currently the GTR has a globally consistent set of Error Codes, which get generated by each jurisdictional 
trade repository or SDR during the file validation process. These Error Codes highlight the reason for rejecting 
a submission.  
Under the rules of EU and UK EMIR Refit both ESMA and the FCA have provided a list of their own regulatory 
Error Codes as defined in their respective Validation Rules documents. Whilst these new regulatory Error 
Codes as defined by ESMA and the FCA will be adopted, [[DTCC]] will also continue to  provide proprietary codes 
where we see that additional information can be provided by the validations that our ingestion layer provide.  
Please see the EU EMIR [[DTCC]] Message Specifications as published on the [[DTCC]] Learning Center for more 
details on regulatory and proprietary error codes.  
FC 4.3 Response Format/Channel  
The response format and channel will be as follows across both EU and UK EMIR.  
Submission 
Channel 
Submission 
Format 
Response 
Format Response  Receiver 
MQ ISO XML message ISO XML ISO XML message Data Submitter 
Web Upload ISO XML files ISO XML ISO XML files Data Submitter 
SFTP ISO XML files ISO XML ISO XML files Data Submitter 
 
 
It should be noted that whilst the message response will be returned to the Data Submitter the Entity 
Responsible for Reporting and Reporting Counterparty will also be able to access the feedback messages via 
the GTR portal through the Submission Search feature. 
 
Clients are also able to receive immediate feedback responses on their MQ channel through the 
“ReplytoQueue” feature. To leverage the JMSReplyTo MQ Property over the outbound queue setup in the 
[[DTCC]] onboarding system to receive MQ ACK/NACK response please use below guidance  
 
➢ Populate MQMD Header Properties as below 
 
 
 
➢ When %RHQ is not populated as part of MQMD. REPLY_TO_Q property GTR will use the outbound 
queue setup from [[DTCC]] onboarding system for MQ ACK/NACK response, if configured. 
 
➢ Please make sure the Queue Manager and Queue Name populated in MQMD Header is correct  and 
consistent with the Queue properties configured as part of client set up. If the Queue properties 


---

## Page 30

 
 
configured as part of the client set up is different to the details provided as part of the 
MQMD.REPLY_TO_Q property on the MQ submission itself, it’s likely that ACK responses would be 
sent to the Queue set up as part of the client account set up and NACK responses would be sent to 
the queues noted on the MQMD.REPLY_TO_Q properties of the MQ submissions itself.  
 
FC 4.4 ACK/NACK Naming Convention 
  
BizMsgIdr_EUEMIR_BDR_BatchInfoID_OCODE_YYYY-MM-DD.HH_MM_SS.gz (or zip)  
 
  
Component  Description  
    
BizMsgIdr  Value populated in corresponding submission files header for which the ACKNACK is sent  
EUEMIR  Jurisdiction  
BDR  Report Name  
BatchInfoID  
Generated by GTR as our internal reference. 
sFTP inbound files - GTR internal sequence number  
Portal inbound files - Portal generated batch [[ID]] when client submits files via the portal  
OCODE  4-character OCODE received on the inbound file for which the ACKNACK is sent  
YYYY-MM-
DD.HH_MM_SS  Timestamp  
.gz (or zip)  compression format when file is sent by GTR  
  
EMIR Refit – ACK/NACK File Naming Convention Examples 
  
  
Input method of 
Submission file  ACK/NACK report delivered via the portal  ACK/NACK report delivered via sFTP  
Web Input  Naming convention (Compressed file)  Naming convention (Compressed file)  

---

## Page 31

 
 
  
  
  
 
BizMsgIdr_EUEMIR_BDR_BatchInfoID_OCO
DE_YYYY-MM-DD.HH_MM_SS.zip  
  
e.g: 
TEST0123_EUEMIR_BDR_994_2BAM_2023
-11-07.15_08_49.zip  
  
Naming convention (File within the 
compressed file)  
 - InputMode-InputRegion-BatchInfoId.xml  
  
e.g: WEB-ND-994.xml  
sFTP_BizMsgIdr_EUEMIR_BDR_BatchInfoID_
OCODE_YYYY-MM-DD.HH_MM_SS.zip(or .gz 
based on client config for compression method)  
  
e.g: 
sFTP_TEST0123_EUEMIR_BDR_994_2BAM_2
023-11-07.15_08_49.zip (or .gz based on client 
config for compression method)  
  
Naming convention (File within the 
compressed file)  
sFTP_BizMsgIdr_EUEMIR_BDR_BatchInfoID_
OCODE_YYYY-MM-DD.HH_MM_SS.xml  
  
e.g: 
sFTP_TEST0123_EUEMIR_BDR_994_2BAM_2
023-11-07.15_08_49.xml  
SFTP Input  
  
Naming convention (Compressed file)  
BizMsgIdr_EUEMIR_BDR_BatchInfoID_OCO
DE_YYYY-MM-DD.HH_MM_SS.zip  
  
  
e.g : 
TEST0123_EUEMIR_BDR_994_2BAM_2023
-11-07.15_08_49.zip  
  
Naming convention (File within the 
compressed file)  
  
InputMode-InputRegion-BatchInfoId.xml  
  
e.g: SFP-ND-994.xml  
Naming convention (Compressed file)  
sFTP_BizMsgIdr_EUEMIR_BDR_BatchInfoID_
OCODE_YYYY-MM-DD.HH_MM_SS.zip(or .gz 
based on client config for compression method)  
  
e.g:  
sFTP_TEST0123_EUEMIR_BDR_994_2BAM_2
023-11-07.15_08_49.zip (or .gz based on client 
config for compression method)  
  
Naming convent ion (File within the 
compressed file)  
sFTP_BizMsgIdr_EUEMIR_BDR_BatchInfoID_
OCODE_YYYY-MM-DD.HH_MM_SS.xml  
  
e.g: 
sFTP_TEST0123_EUEMIR_BDR_994_2BAM_2
023-11-07.15_08_49.xml 
 
FC 5: Reports  

---

## Page 32

 
 
Daily reports will be made available through the [[DTCC]] Portal and via sFTP upon request. For access to reports 
via the Global Portal GTR users will be required to subscribe to the reports they require via the Manage Services 
application. For access to reports via sFTP GTR users will  be required to request a subscription via the GTR 
Connectivity team.  
 
Please note more information will be provided on report subscription in due course.  
FC 5.1: XML and CSV Report  
Trade Repositories are mandated to provide reports to market participants in an XML format as a minimum 
regulatory requirement. The ISO Schemas and Usage Guidelines for these reports have been created by the 
respective regulatory authorities and are available via their website (links shown below:  
ESMA EU EMIR Refit Regulatory Report ISO XML Schemas  
FCA UK EMIR Refit Regulatory Report ISO XML Schemas 
[[DTCC]] will be providing a subset of reports in a CSV format. When subscribing to reports in the Manage Services 
application GTR users will be able to choose their required report format.  
FC 5.2: Report Types 
The following reports will be made available upon request on a daily basis.  
Type Description 
Trade State 
Report 
• Trade State Reports will no longer contain Allege Reports within them. There will be a separate 
Allege Report (provided in .CSV format only).  
• Only unique trades should be displayed in the TSR. The uniqueness of a new trade is defined by the 
concatenation of the UTI + RCP1. For example, if position 1 is UTI + RCP1 + OCP1 & position 2 is 
UTI + RCP2 and OCP1, then they are considered unique positions. Existing open trades at the point 
of go live will retain uniqueness at the level of the triplet (please see section 3.5 for more details).  
• The TSR generated on a given day contains the latest view of the position based upon the Event 
Date minus 2 days. It includes valuations but excludes [[collateral]] state information.  
• The TSR is run and generated on a daily basis from Tuesday to Saturday after midnight UTC. All 
positions up to Event Date T-2 are included in the TSR sent out on T.  
• EMIR Refit mandates that the following parties have access to the reports: Report Submitting Entity 
(RSE), Reporting Counterparty (RCP) and Entity Responsible for Reporting (ERR).  
• Execution Agent:  
o In the EU, Execution Agent is not a field in the ESMA ISO 20022 XML Trade Activity 
Schema. To account for that, [[DTCC]] is supporting the capture of the identification of 
Execution Agent of the Reporting Counterparty (where market participants need to identify 
them). As such, Execution Agent data won’t appear in the XML version of the TSR but it will 
be added to the CSV version of the TSR.  The Execution Agent of the RCP will also have 
access to the reports. 
o In the UK, Execution Agent is included as a field in the UK ISO 20022 XML. As such, this 
data will be available in the TSR in XML format and in CSV format. Where identified, they 
will also have access to the reports.   
- Each position on the report should only contain the information related to that position. If optional 
fields are left blank in a user submission (after a previous submission had a value populated for those 

---

## Page 33

 
 
Type Description 
optional fields), the ‘latest is greatest’ principle will mean that the field will be blank on the TSR. The 
exception to the rule is Other Payments fields where the following approach is applied:  
o If the MODI contains Other Payments details that were previously reported on the NEWT, 
then the MODI details will be applied to the TSR following the latest is greatest approach.  
o if the MODI contains Other Payment types that were not previously reported on previous 
submissions, then Other Payment details on the MODI is added to the Other Payment 
details reported on the TSR (represented as separate additional payments) 
o similarly if on a TERM, there are Other Payment types that were not previously reported on 
previous submissions, then the Other Payment types on the TERM will be added onto the 
final state of the trade (represented as separate additional payments)  
o Action Type = CORR can be used to correct the details of other payment data previously 
reported or to 'erase' a payment previously by submitted by reporting with other payment 
amount (2.74) = 0.  
•  
• There is no masking of fields in EU and UK EMIR Refit as the TSR will no longer contain allege 
records. 
•  The final XML and CSV report formats will be published on the Learning Center. 
• This report is created per the [[Asset]] class(es) configured under the [[DTCC]] O-Code, which can be 
configured during the onboarding process and amended upon request. Whilst there are no explicit 
changes mandated under the EMIR Refit implementation users can request amendments at any time.  
• Trades which have been submitted with action type TERM or EROR (and not subsequently revived) 
or have been submitted with action type POSC are excluded from the TSR (as they are positions that 
are classified to have a non-outstanding status even if their expiration date is in the future). 
• When counterparties are reporting schedules, they should report the full schedule up front if it is 
available. As specified by the EMIR Guidelines, the GTR will only include the current value from the 
schedules reported, as opposed to including all the values from the schedules, in the Trade State 
report. This is applicable for the following fields: 2.50-2.52 (‘Price’), 2.57-2.59 (‘Notional amount of leg 
1’), 2.61-2.63 (‘Notional quantity of leg 1’), 2.66-2.68 (‘Notional amount of leg 2’), 2.70-2.72 (‘Notional 
quantity of leg 2’), and 2.135-2.137 (‘Strike price’). 
• Other Payments 
o There are 6 Other Payments fields (2.73-2.78) – type, amount, currency, date, payer, 
receiver.  
o The information provided in other payment fields is only to be reported for the reportable 
event to which the payment relates and once the payment details have been reported, the 
values [[DO]] not need to be re-reported in subsequent submissions into the trade repository. 
o Data elements pertaining to the ’other payments‘ can be reported multiple times, for multiple 
payments.  
o For Other Payments fields, the values that appear in the TSR will follow a blended approach 
of ‘latest is greatest’ and ‘additive’. For Other Payment fields, approach will be:   
▪ If the MODI contains Other Payments details (type, date, payer, receiver) that were 
previously reported on the NEWT, then the Other payment (amount, currency) 
details on the MODI will be applied to the TSR following the latest is greatest 
approach.  
▪ if the MODI contains Other Payment details (type, date, payer, receiver) that were 
not previously reported on previous submissions, then the Other Payment details 

---

## Page 34

 
 
Type Description 
on the MODI is added to the Other Payment details reported on the NEWT on the 
TSR (represented as separate additional payments) 
▪ Similarly if on a TERM, there are Other Payment details (type, date, payer, 
receiver) that were not previously reported on previous submissions, then the Other 
Payment details on the TERM will be added onto the state of the trade 
(represented as separate additional payments)  
▪ Action Type = CORR can be used to correct the details of other payment data 
previously reported. 
• Commodities repeatable fields (2.122 - 2.131), all schedules for these fields will be available on the 
TSR irrespective of the event date used to construct the TSR. 
 
Trade Activity 
Report 
• The Activity report will only include messages accepted into the GTR and exclude rejected 
submissions. 
• A report will only contain activity between two report generation periods. For instance, the report 
generated on Wednesday morning UTC will contain accepted trade messages submitted between 
Tuesday 00:00:00 UTC to Tuesday 23:59:59 UTC. The only exception where this report contains 
multiple days’ worth of submissions is the report generated on Tuesday morning UTC which would 
contain accepted trade messages submitted between Saturday 00:00:00 UTC to Monday 23:59:59 
UTC.  
• Multiple trade submissions with the same identifier would be displayed multiple times if they are 
submitted successfully within the reporting window. 
• Each record on the report will only contain the information related to that submission.  
• If an optional field is excluded from the user submission, it will be blank on the report 
• The Trade Activity report will contain only trade messages or valuation messages but exclude 
[[collateral]] submissions which will be on a separate [[collateral]] activity report. 
• Allege records will not be included in the Trade Activity Report.  
• The TAR is run and generated on a daily basis from Tuesday to Saturday after midnight UTC. 
• EMIR Refit mandates that the following parties have access to the reports: Report Submitting Entity 
(RSE), Reporting Counterparty (RCP) and Entity Responsible for Reporting (ERR).  
• There is no masking of fields in the Activity report  
• The final XML and CSV report formats will be published in the learning center. 
 
• This report is created per the [[Asset]] class(es) configured under the [[DTCC]] O-Code, which can be 
configured during the onboarding process and amended upon request. Whilst there are no explicit 
changes mandated under the EMIR Refit implementation users can request amendments at any time.  
• Execution Agent:  
o In the EU, Execution Agent is not a field in the ESMA ISO 20022 XML Trade Activity 
Schema. To account for that, [[DTCC]] is supporting the capture of the identification of 
Execution Agent of the Reporting Counterparty (where market participants need to identify 
them). As such, Execution Agent data won’t appear in the XML version of the TAR but it will 
be added to the CSV version of the TAR.  The Execution Agent of the RCP will also have 
access to the reports. 

---

## Page 35

 
 
Type Description 
o In the UK, Execution Agent is included as a field in the UK ISO 20022 XML. As such, this 
data will be available in the TAR in XML format and in CSV format. Where identified, they 
will also have access to the reports.   
Trade 
Submission 
Report 
• The Submission Report contains all the successful and unsuccessful submissions submitted by the 
report submitting entity (RSE). All Accepted and Rejected submissions are included in the report. 
• [[EOD]] cutoff is 23:59 UTC Monday to Friday meaning any submissions that are received based on 
submission received timestamp of 23:59:59 UTC is eligible for reporting on that day’s submission 
reports even if it is processed by the GTR the next day. 
• The Submission Report contains trade and valuation messages but excludes [[collateral]] messages. 
[[collateral]] submissions will be reflected on a separate report. 
• The Submission Report will only be available in CSV format. 
• The Submission Report is run and generated on a daily basis from Tuesday to Saturday after 
midnight UTC. 
• The following parties will have access to the Submission Report: Submitter Identifier (RSE) and 
Reporting Counterparty (RCP). The submitter identifier (RSE) will see all trade sides they have 
submitted, whether accepted or rejected but cannot view any submissions they did not submit.  
• The Reporting Counterparty (RCP) will see their own side of the trade with themselves as RCP and 
their counterparty as OCP, whether accepted or rejected. The Reporting Counterparty (RCP) will see 
all the successful and unsuccessful submissions submitted by themselves. 
• The ERR does not have access to the Submission Report, unless the ERR is also the RSE or RCP. 
• There is no masking of fields in the EU and UK EMIR Submission Report 
• The final report format will be published in the learning center.  
• This report is created per the [[Asset]] class(es) configured under the [[DTCC]] O-Code, which can be 
configured during the onboarding process and amended upon request. Whilst there are no explicit 
changes mandated under the EMIR Refit implementation users can request amendments at any time.  
[[Margin]] State 
Report 
• The [[Margin]] State Report is run and generated on a daily basis from Tuesday to Saturday after 
midnight UTC 
• The [[Margin]] State Report contains the latest [[collateral]] view on a daily basis between 00:00:00 UTC to 
23:59:59 UTC. As [[Margin]] updates are expected to be submitted on a daily basis even when there is 
no change, we will not carry forward [[Margin]] information from prior day’s reports if they are not 
submitted for a particular day.  
• The MSR is run and generated on a daily basis from Tuesday to Saturday after midnight UTC. All 
positions up to Event Date T-2 are included in the MSR sent out on T.  
• EMIR Refit mandates that the following parties have access to the reports: Report Submitting Entity 
(RSE), Reporting Counterparty (RCP) and Entity Responsible for Reporting (ERR).  
• The [[Margin]] State Report will only include [[Margin]] messages accepted at GTR and exclude rejects 
• Each record on the report will only contain the information related to that [[Margin]] state. If an optional 
field is excluded from the user submission after a value was previously submitted for that field, due to 
the ‘latest in greatest’ rule, the value in the MSR will be shown as blank for that field.  
• There is no masking of fields in EMIR Refit as MSR is only available to the RCP and ERR 
•  The final XML and CSV report formats will be published in the learning center. 

---

## Page 36

 
 
Type Description 
• Execution Agent:  
o In the EU, Execution Agent is not a field in the ESMA ISO 20022 XML [[Margin]] State 
Schema. To account for that, [[DTCC]] is supporting the capture of the identification of 
Execution Agent of the Reporting Counterparty (where market participants need to identify 
them). As such, Execution Agent data won’t appear in the XML version of the MSR but it will 
be added to the CSV version of the MSR. The Execution Agent of the RCP will also have 
access to the reports. 
[[Margin]] Activity 
Report 
• The [[Margin]] Activity report should only include “MARU” and “CORR” action type messages on Auth. 
108 schemas (for EU and the UK respectively) that are accepted at the respective GTRs and exclude 
rejects. 
• A report should only contain activity between two report generation periods. For instance, the report 
generated on Wednesday morning UTC will contain accepted [[Margin]] messages submitted between 
Tuesday 00:00:00 UTC to Tuesday 23:59:59 UTC. The only exception where this report contains 
multiple days’ worth of submissions is the report generated on Tuesday morning UTC which would 
contain accepted [[collateral]] messages submitted between Saturday 00:00:00 UTC to Monday 
23:59:59 UTC. Multiple trade submissions with the same identifier would be displayed multiple times 
if they are submitted successfully within the reporting window. 
• Each record on the report will only contain the information related to that submission. If an optional 
field is excluded from the user submission, it will be blank on the report 
• The [[Margin]] Activity report should contain only [[Margin]] message submissions.  
• The [[collateral]] Activity Report is run and generated on a daily basis from Tuesday to Saturday after 
midnight UTC.  
• EMIR Refit mandates that the following parties have access to the reports: Report Submitting Entity 
(RSE), Reporting Counterparty (RCP) and Entity Responsible for Reporting (ERR).  
• The final XML and CSV report formats will be published in the learning center. 
• Execution Agent:  
o In the EU, Execution Agent is not a field in the ESMA ISO 20022 XML [[Margin]] Activity 
Schema. To account for that, [[DTCC]] is supporting the capture of the identification of 
Execution Agent of the Reporting Counterparty (where market participants need to identify 
them). As such, Execution Agent data won’t appear in the XML version of the MSR but it will 
be added to the CSV version of the MSR. The Execution Agent of the RCP will also have 
access to the reports. 
[[Margin]] 
Submission 
Report 
• The [[Margin]] Submission Report contains all the successful and unsuccessful submissions submitted 
by the report submitting entity (RSE). All Accepted and Rejected submissions are included in the 
report. 
• [[EOD]] cutoff is 23:59 UTC Monday to Friday meaning any submissions that are received based on 
submission received timestamp of 23:59:59 UTC is eligible for reporting on that day’s submission 
reports even if it is processed by GTR the next day. 
• The [[Margin]] Submission Report contains only [[Margin]] messages based on action type MARU and 
CORR on [[Margin]] Activity schema (Auth.108).  
• The [[Margin]] Submission Report will only be available in CSV format 
• The [[Margin]] Submission Report is generated on a daily basis from Tuesday to Saturday after midnight 
UTC. 

---

## Page 37

 
 
Type Description 
• The following parties will have access to the [[Margin]] Submission Report: Submitter Identifier (RSE) 
and Submitted for Party (RCP). The Submitter Identifier (RSE) will see all trade sides they have 
submitted, whether accepted or rejected but must not be able to view any submissions they did not 
submit. 
• The Reporting Counterparty (RCP) will see their own side of the trade with themselves as Trade 
Party 1 and their counterparty as Trade Party 2, whether accepted or rejected. The Reporting 
Counterparty (RCP) will see all the successful and unsuccessful submissions submitted by 
themselves. 
• There is no masking of fields in the EMIR Refit [[Margin]] Submission Report 
• The final CSV report format will be published in the learning center. 
 
Reconciliation 
Statistics Report 
• This report will contain reconciliation statistics of [[Derivatives]] eligible and included in the reconciliation 
process. 
• The Reconciliation Statistics report generated on a given day will consist of the latest reconciliation 
statistics based upon Event Date minus 3 days 
o In case reconciliation takes place on Wednesday; the [[Derivatives]] reported whose event date 
is Monday or earlier will be included in the reconciliation for Wednesday and will be available 
on the Reconciliation Statistics report generated on Thursday. 
• [[Derivatives]] which have been non-outstanding for thirty-one calendar days or more will be removed 
from the reconciliation process and will not be included in the Reconciliation statistics report. 
• The final XML and CSV report formats will be published in the learning center 
• This report is created per the [[Asset]] class(es) configured under the [[DTCC]] O-Code, which can be 
configured during the onboarding process and amended upon request. Whilst there are no explicit 
changes mandated under the EMIR Refit implementation users can request amendments at any time. 
• This report occurs in 2 forms:  
o Immediate [[EOD]] reconciliation statistics report (delivered 1 hour after the end of the 
reconciliation process) 
o [[EOD]] reconciliation statistics reports (delivered in accordance with the SLAs for EU (06:00 
UTC) and UK (09:00 UTC) 
Rejections 
Statistics Report 
• This report will contain statistics of accepted and rejected [[Derivatives]] received on a given day. 
• This report is created per the [[Asset]] class(es) configured under the [[DTCC]] O-Code, which can be 
configured during the onboarding process and amended upon request. Whilst there are no explicit 
changes mandated under the EMIR Refit implementation users can request amendments at any time. 
• The final XML report format will be published in the learning center 
• A report will only contain activity between two report generation periods. For instance, the report 
generated on Wednesday morning UTC will contain statistics of accepted and rejected trade 
messages submitted between Tuesday 00:00:00 UTC to Tuesday 23:59:59 UTC. The only exception 
where this report contains multiple days’ worth of submissions is the report generated on Tuesday 
morning UTC which would contain statistics of accepted and rejected trade messages submitted 
between Saturday 00:00:00 UTC to Monday 23:59:59 UTC.  
Abnormal 
Values and 
Warnings 
Report 
• The Abnormal Values and Warnings report will contain a combination of the following 
o Missing Valuations 
o Missing Margins 

---

## Page 38

 
 
Type Description 
o Abnormal Values  
• The Missing Valuations section will consist of outstanding [[Derivatives]] for which no valuation has been 
reported or for which the valuation that was reported is dated i.e. Valuation Timestamp is more than 
14 calendar days earlier than the day for which the report is generated. This section of the report will 
be based off the Trade State Report 
• The Missing [[Margin]] section will consist of outstanding [[Derivatives]] for which no [[Margin]] has been 
reported or for which the [[Margin]] that was reported is dated i.e. [[collateral]] Timestamp is more than 14 
calendar days earlier than the day for which the report is generated. This section of the report will be 
based off the Trade State Report 
• The Abnormal Values section  contains submissions with action type ‘NEWT’, ‘POSC’, ‘MODI’ or 
‘CORR’ received on a given day whose notional amounts are abnormal for the class of [[Derivatives]]. 
This report will be based off the Trade Activity Report. 
• Abnormal values (outliers) will be identified for the following fields; 
o 2.55 ‘Notional amount of leg 1’,   
o 2.59 ‘Notional amount in effect on associated effective date of leg 1’,   
o 2.60 ‘Total notional quantity of leg 1’,  
o 2.63 ‘Notional quantity in effect on associated effective date of leg 1’,  
o 2.64 ‘Notional amount of leg 2’,   
o 2.68 ‘Notional amount in effect on associated effective date of leg 2’,  
o 2.69 ‘Total notional quantity of leg 2’,  
o 2.72 ‘Notional quantity in effect on associated effective date of leg 2’. 
• A derivative report will be included into the abnormal values section when at least one of the fields 
above was populated with an abnormal value. 
• This section will only contain activity between two report generation periods. For instance, the report 
generated on Wednesday morning UTC will contain accepted trade messages submitted between 
Tuesday 00:00:00 UTC to Tuesday 23:59:59 UTC for the action types mentioned above whose 
notional amounts are abnormal fort the class of [[Derivatives]]. The only exception where this report 
contains multiple days’ worth of submissions is the report generated on Tuesday morning UTC which 
would contain accepted trade messages submitted between Saturday 00:00:00 UTC to Monday 
23:59:59 UTC.  
• This report is created per the [[Asset]] class(es) configured under the [[DTCC]] O-Code, which can be 
configured during the onboarding process and amended upon request. Whilst there are no explicit 
changes mandated under the EMIR Refit implementation users can request amendments at any time 
End of Day 
Allege Trade 
State Report 
• The End of Day allege report will consist of the Allege view of the trade and will be provided only in 
CSV format. 
• This report will be based off the TSR and will contain the Allege view of positions based upon Event 
Date minus 2 days.  
• The party receiving this report will be the  Other Counterparty of the trades. 
• This report is created per the [[Asset]] class(es) configured under the [[DTCC]] O-Code, which can be 
configured during the onboarding process and amended upon request. Whilst there are no explicit 
changes mandated under the EMIR Refit implementation users can request amendments at any time. 

---

## Page 39

 
 
Type Description 
Intraday Allege 
Activity Report 
• The intention of this new GTR report will be to facilitate a way for counterparties to share data 
intraday. 
• This report is not one mandated by the regulators. It is a GTR proprietary report. 
• The Intraday Allege Activity Report will only include messages accepted into the GTR. Rejected 
messages will be excluded.  
• The Intraday Allege Activity Report will only include submissions accepted with an Action Type = 
NEWT, POSC, EROR and REVI.   
• The Intraday Allege Activity Report will be generated in CSV only. 
• The Intraday Allege Activity Report will be generated at 10:00 UTC, 18:00 UTC and 00:00 UTC. 
• If an optional field is excluded from the user submission it will also be blank on the report 
• This report is created per the [[Asset]] class(es) configured under the standard [[DTCC]] O-Code. 
• A new View Only account type will be created to facilitate the distribution of this report to non-
onboarded entities. More details will be provided on this account type in due course.  
 
Users who wish to have the NEW reports sent to them via SFTP will need to set up configurations for the new 
product IDs with our connectivity team (GTRConnectivity@[[DTCC]].com). 
FC 5.3: Merging of Trade Valuation Information onto Trade State Report 
1) Merging of fields from Valuation submission onto TSR:  When merging the valuation details onto 
the TSR, only valuation specific fields should be updated from the valuation message. The EU and UK 
EMIR Refit valuation related fields are Reporting timestamp, Valuation amount, Valuation currency, 
Valuation timestamp, Valuation method and Delta.  
The TSR on T includes Trade and Valuations submissions where Event Date = T-2.   
All other timestamp fields on the TSR will continue to be based on the information on the Trade 
submission (i.e., they will not be updated with the values from the Trade Valuation submiss ion). 
2) Timestamp used for merging the “latest” valuation:  The valuation submission used for merging 
onto the TSR will be based on the latest Valuation Timestamp. 
When matching a Valuation to a base trade for merging information onto the TSR at end of day, the UTI + RCP 
+ OCP must match. 
FC 5.4: Report Naming Conventions 
Delivery 
Method Format Report Type File Naming Convention 
SFTP XML 
All Client 
Reports 
excluding TSR 
and MSR  
sFTP_EUEMIR_Frequency_Report 
Description_ProductID_UTCTimestamp_FileNumber&Sequnce_Client
O-Code.xml 
TSR and MSR 
sFTP_EUEMIR_Frequency_Report 
Description_ProductID_UTCTimestamp_FileNumber&Sequnce_ClientO
-Code-Version.xml 

---

## Page 40

 
 
Portal XML 
All Client 
Reports 
excluding TSR 
and MSR  
EUEMIR_Frequency_Report 
Description_ProductID_UTCTimestamp_FileNumber&Sequnce_Client
O-Code.xml 
TSR and MSR 
EUEMIR_Frequency_Report 
Description_ProductID_UTCTimestamp_FileNumber&Sequnce_ClientO
-Code-Version.xml 
SFTP CSV 
All Client 
Reports 
excluding TSR 
and MSR  
sFTP_EUEMIR_Frequency_Report 
Description_ProductID_UTCTimestamp_ClientO-Code.csv 
TSR and MSR sFTP_EUEMIR_Frequency_Report 
Description_ProductID_UTCTimestamp_ClientO-Code-Version.csv 
Portal CSV 
All Client 
Reports 
excluding TSR 
and MSR  
EUEMIR_Frequency_Report 
Description_ProductID_UTCTimestamp_ClientO-Code.csv 
TSR and MSR EUEMIR_Frequency_Report 
Description_ProductID_UTCTimestamp_ClientO-Code-Version.csv 
 
 
Frequency – Delivery Frequency of report i.e. [[EOD]] or Intra day 
Report Description – Name of Report separated with underscores i.e. Margin_Activity_Report 
Product [[ID]] – Unique [[ID]] assigned by GTR for a given report type and report format combination 
UTCTimestamp - Report As of Date in YYYY-MM-DD.HH_MM_SS format.  i.e. a report delivered on 
03/08/2023 will contain the date of 2023-08-02.05_49_02 in the report name 
Client OCODE – 4 character client OCODE 
FileNumber&Sequnce – Applicable only to XML reports. Is made up of two parts. The first part indicates the 
number of total files, and the second part indicates the sequence of the file (E.g. 005001 meaning there are 5 
files in total and this file is file 1 in the sequence).  
CSV reports will be provided as a single file and will not be split into multiple files similar to XML reports. 
Clients need to be mindful of file sizes and the recommendation is that larger clients segregate by [[Asset]] class 
and/or use XML reports 
 
 
 
File Name Examples 
Report Format Delivery 
Method Example File Name 

---

## Page 41

 
 
Trade Activity 
Report 
XML 
sFTP sFTP_EUEMIR_EOD_Trade_Activity_Report_02503501_YYYY-MM-
DD.HH_MM_SS_005001_8XXX.xml 
Portal EUEMIR_EOD_Trade_Activity_Report_02503501_YYYY-MM-
DD.HH_MM_SS_005001_8XXX.xml 
CSV 
sFTP sFTP_EUEMIR_EOD_Trade_Activity_Report_02503510_YYYY-MM-
DD.HH_MM_SS_8XXX.csv 
Portal EUEMIR_EOD_Trade_Activity_Report_02503510_YYYY-MM-
DD.HH_MM_SS_8XXX.csv 
Trade State 
Report 
XML 
sFTP sFTP_EUEMIR_EOD_Trade_State_Report_02503502_YYYY-MM-
DD.HH_MM_SS_005001_8XXX-0.xml 
Portal EUEMIR_EOD_Trade_State_Report_02503502_YYYY-MM-
DD.HH_MM_SS_005001_8XXX-0.xml 
CSV 
sFTP sFTP_EUEMIR_EOD_Trade_State_Report_02503511_YYYY-MM-
DD.HH_MM_SS_8XXX-0.csv 
Portal EUEMIR_EOD_Trade_State_Report_02503511_YYYY-MM-
DD.HH_MM_SS_8XXX-0.csv 
[[Margin]] Activity 
Report 
XML 
sFTP sFTP_EUEMIR_EOD_Margin_Activity_Report_02503503_YYYY-MM-
DD.HH_MM_SS_005001_0XXX.xml 
Portal EUEMIR_EOD_Margin_Activity_Report_02503503_YYYY-MM-
DD.HH_MM_SS_005001_0XXX.xml 
CSV 
sFTP sFTP_EUEMIR_EOD_Margin_Activity_Report_02503512_YYYY-MM-
DD.HH_MM_SS_0XXX.csv 
Portal EUEMIR_EOD_Margin_Activity_Report_02503512_YYYY-MM-
DD.HH_MM_SS_0XXX.csv 
[[Margin]] State 
Report 
XML 
sFTP sFTP_EUEMIR_EOD_Margin_State_Report_02503504_YYYY-MM-
DD.HH_MM_SS_005001_0XXX-0.xml 
Portal EUEMIR_EOD_Margin_State_Report_02503504_YYYY-MM-
DD.HH_MM_SS_005001_0XXX-0.xml 
CSV 
sFTP sFTP_EUEMIR_EOD_Margin_State_Report_02503513_YYYY-MM-
DD.HH_MM_SS_0XXX-0.csv 
Portal EUEMIR_EOD_Margin_State_Report_02503513_YYYY-MM-
DD.HH_MM_SS_0XXX-0.csv 
Trade  
Submission 
Report 
CSV 
sFTP sFTP_EUEMIR_EOD_Trade_Submission_Report_02503519_YYYY-MM-
DD.HH_MM_SS_8XXX.csv 
Portal EUEMIR_EOD_Trade_Submission_Report_02503519_YYYY-MM-
DD.HH_MM_SS_8XXX.csv 
[[Margin]] 
Submission 
Report 
CSV 
sFTP sFTP_EUEMIR_EOD_Margin_Submission_Report_02503520_YYYY-MM-
DD.HH_MM_SS_0XXX.csv 
Portal EUEMIR_EOD_Margin_Submission_Report_02503520_YYYY-MM-
DD.HH_MM_SS_0XXX.csv 

---

## Page 42

 
 
End of Day 
Rejections 
Statistics 
Report 
XMl 
sFTP sFTP_EUEMIR_EOD_Rejections_Report_02503505_YYYY-MM-
DD.HH_MM_SS_005001_8XXX.xml 
Portal EUEMIR_EOD_Rejections_Report_02503505_YYYY-MM-
DD.HH_MM_SS_005001_8XXX.xml 
End of Day 
Reconciliation 
Statistics 
Report 
XML 
sFTP sFTP_EUEMIR_EOD_Recon_Status_Report_02503506_YYYY-MM-
DD.HH_MM_SS_005001_8XXX.xml 
Portal EUEMIR_EOD_Recon_Status_Report_02503506_YYYY-MM-
DD.HH_MM_SS_005001_8XXX.xml 
CSV 
sFTP sFTP_EUEMIR_EOD_Recon_Status_Report_02503515_YYYY-MM-
DD.HH_MM_SS_8XXX.csv 
Portal EUEMIR_EOD_Recon_Status_Report_02503515_YYYY-MM-
DD.HH_MM_SS_8XXX.csv.g 
Immediate 
Reconciliation 
Feedback 
Report 
XML 
sFTP sFTP_EUEMIR_Immediate_Recon_Feedback_Report_02503522_YYYY-
MM-DD.HH_MM_SS_005001_8XXX.xml 
Portal EUEMIR_Immediate_Recon_Feedback_Report_02503522_YYYY-MM-
DD.HH_MM_SS_005001_8XXX.xml 
Abnormal 
Values and 
Warnings 
Report 
XML sFTP sFTP_EUEMIR_EOD_Abnormal_Values_Report_02503509_YYYY-MM-
DD.HH_MM_SS_005001_8XXX.xml 
 Portal EUEMIR_EOD_Abnormal_Values_Report_02503509_YYYY-MM-
DD.HH_MM_SS_005001_8XXX.xml 
End of Da 
Allege Trade 
State Report 
CSV 
sFTP sFTP_EUEMIR_EOD_Allege_Trade_State_Report_02503521_YYYY-MM-
DD.HH_MM_SS_8XXX.csv 
Portal EUEMIR_EOD_Allege_Trade_State_Report_02503521_YYYY-MM-
DD.HH_MM_SS_8XXX.csv 
Intraday Allege 
Activity Report CSV 
sFTP sFTP_EUEMIR_Intraday_Allege_UTI_Report_02503533_YYYY-MM-
DD.HH_MM_SS_8XXX.csv 
Portal EUEMIR_Intraday_Allege_UTI_Report_02503533_YYYY-MM-
DD.HH_MM_SS_8XXX.csv 
 
FC 5.5: Repeatables and Schedules on CSV reports  
When multiple schedules are present on a single trade, this data will be displayed on a single row and will 
be separated by semicolons i.e.1 row will be displayed for each unique trade: e.g. UT1+ RCP+ OCP 
e.g. 
Submission 

---

## Page 43

 
 
  
CSV Trade Activity report 
 
. 
This logic will be applied to the following fields 
• Fields 2.50-2.52 price schedules 
• Fields 2.57-2.59 notional amount schedules 
• Fields 2.61-2.63 notional quantity schedules 
• Fields 2.66-2.68 notional amount schedules 
• Fields 2.70-2.72 notional quantity schedules 
• Fields 2.135-2.137 strike price schedules 
• Fields 2.73-2.78 other payments 
• Fields 2.122-2.131 energy delivery 
 
Single fields where multiple values are allowed on the schema – will be displayed in a single cell and will 
be semicolon separated on the CSV report, e.g.  Identifier of the basket’s constituents 
Submission 


---

## Page 44

 
 
  
CSV Trade Activity Report 
  
Edge cases 
Scenario 1 
Days of the week where a single schedule row has multiple days of the week.  
Solution - Days of the week for a single schedule will be comma separated and each schedule will be 
semicolon separated See example below (i.e. a mix of commas and semicolons will be used as separators in 
this instance 
 
Scenario 2 
RTS1/RTS2 data where the number of start and end dates don’t match.   
  
Solution – when the date is not available 2 semicolons will be added (no spaces in between). See example 
highlighted below.  
 


---

## Page 45

 
 
 
 
 
FC 6: Intra and Inter-TR Reconciliation  
Although the concept of Pairing and Matching will remain there will be largescale changes to the Intra and 
Inter-TR Reconciliation with the implementation of EMIR Refit.  
FC 6.1: Reconciliation Eligibility  
Under the rules of EMIR Refit [[DTCC]] will only include in the reconciliation process trades where the following 
conditions are fulfilled:   
- Counterparty 1 has reporting obligation, i.e. it is a counterparty established in the EU or an AIF, whose 
AIFM is established in the EU, based on the GLEIF. 
- Counterparty 2 has reporting obligation as indicated if established in the EU or an AIF, whose AIFM is 
established in the EU, based on the GLEIF or the field 1.14 ‘Reporting obligation of the counterparty 2’ 
is populated with ‘True’.  
- The derivative has not been subject to a report with action type ‘EROR’, unless it has been followed by 
a report with action type ‘REVI’.  
-  The derivative is outstanding, as referred to in Article 2(2)(a) and 2(2)(b) of the ITS on reporting, or it 
has been outstanding in the last thirty calendar days.  
It should also be noted that trades reported at both a Trade and Position level will continue to be entered into 
the reconciliation process. Additionally, late reported trades will still be included into the reconciliation process 
if the late reported trades is subject to reconciliation under the conditions outlined above.  
FC 6.2 Reconciling trades up to 30 days post maturity or termination 
The GTR will remove trades from the reconciliation process that have been non -outstanding for thirty-one 
calendar days or more, and this should be determined based on the earliest date reported in either field 
’Expiration date’ or field ‘Early termination date’. Moreover, [[Derivatives]] that have received a report with action 
type ’EROR’ will also be removed. 
FC 6.3 Reconcilable Fields  
The number of reconcilable fields has increased from 57 to 146. This incorporates 82 fields at the point of go 
live on April 29th, 2024 and 64 fields two years later on April 29th 2026. Please see the Message Specifications 
Rules as published on the [[DTCC]] Learning Center for more details on the reconcilable fields.  
  


---

## Page 46

 
 
FC 6.4 Reconciliation Statuses 
Currently there are a number of different reconciliation statuses that indicate the results of the reconciliation 
process including Paired, Matched, Reconciled and Exempt. Under the rules of EMIR Refit the reconciliation 
statuses have been simplified to the following: 
- Pairing Statuses: Paired or Unpaired 
- Trade Reconciliation Statuses: Reconciled or Not Reconciled.  
- Valuation Reconciliation: Reconciled or Not Reconciled or Not Applicable (please note: Not applicable 
will be used to account for NFC- entities not being obliged to submit valuations).  
FC 6.5: Reconciliation Tolerances  
Under the rules of EMIR Refit the reconciliation tolerances have been provided within the Validation Rules 
provided by both ESMA and the FCA. The GTR will adhere to these tolerances within its reconciliation pr ocess. 
FC 6.5: Reconciliation based upon Event Date 
Under the rules of EMIR Refit the Trade State Report will be moving to a model whereby it is generated on a 
given day it will contain the latest view of the position based upon the Event Date minus 2 days  (See section 
FC 5.1 Report Types for more details). The intra and inter-TR reconciliation is based upon the trade state 
therefor this model will also be adopted for the reconciliation processes.  
The table below outlines the timeline for trades appearing in the Trade State Reports and when they will be 
subject to the reconciliation process. This is a substantial change from the reconciliation model adopted today 
by Trade Repositories, which is currently based upon the Latest is Greatest concept.   
 
  


---

## Page 47

 
 
FC 6.6: Valuation Reconciliation   
As specified by the technical standards and reporting guidelines Trade Repositories will commence reconciling 
valuations two years post the go live of EMIR Refit. For EU EMIR this means that from April 29 th 2026 and from 
September 30th 2026  
FC 6.7: Reconciling trades with two legs    
As stated by the EMIR Reporting Guidelines the GTR will attempt to reconcile trades with two legs by 
reconciling each of the legs as reported by the counterparties. For certain trades with two l egs (such as 
interest-rate swaps, cross-currency swaps and FX swaps) the order cannot be unequivocally defined, as there 
is no specific prevalence of one leg over the other, therefore additional logic may be required. Any logic the 
GTR implements to reconcile such trades will be discussed with applicable trade associations, the other trade 
repositories and the regulatory authorities.  
Please note that as yet this logic has not defined.As stated by the reporting guidelines when an outstanding 
position is the result of netting of a position to zero (Level = P and Quantity=0) the GTR will exclude from the 
reconciliation process the fields ‘Direction’, ‘Direction of leg 1’ and ‘Direction of leg 2’. In this scenario these 
fields will be treated as reconciled.  
FC 6.8: Reconciliation of schedule information   
As specified by the EMIR Reporting Guidelines published by ESMA the GTR will only reconcile data on the 
schedule fields that are included in the Trade State Report. This means that regardless of whether a full  
schedule of values were reported the GTR will only reconcile the current values from the schedules reported as 
these are the values displayed within the Trade State Report (see section 5.1 Report Types for more details).  
FC 6.8: Reconciliation during the EMIR Refit Transition Period  
The GTR will continue to reconcile trades throughout the respective EU and UK EMIR Refit transition periods. 
As previously noted in section FC 7.2 all counterparties are expected to upgrade their live trade population to 
the latest technical standard through the submission of a modification message within six months of the go 
lives dates. Throughout this period trade repositories will be expected to reconcile trades regardless of whether 
both sides have been upgraded to the latest technical standards or not. Whilst it has been acknowledged by 
the regulatory authorities that there may be data quality challenges throughout this time period there is still an 
expectation that counterparties attempt to reconcile and resolve any breaks.  
FC 7: Functionality Specific to Go-Live 
Users are expected to upgrade their open trades to the new data standards as defined in the message 
specifications after go-live.  This section describes relevant functionality to support that process and other go-
live related processes. 
 
Please note that these activities will be performed during both UAT and Production go -lives. 
FC 7.1: EU EMIR Data Harmonization Exercise  
It is incumbent on trade repositories to harmonize all EMIR data that it stores. This mean s that data from all 
three standards of EMIR must be transformed into a single consistent view (i.e. a harmonized view that will be 
based on the EMIR Refit standards). This will ensure that all data can be populated on the published XML 
schemas enabling a consistent approach to both regulator and TR [[participant]] reporting.  
In support of this exercise ESMA have published a document entitled the “Mapping between standards” 
document. This document contains mappings between the EU EMIR RTS 1.0 (i.e. the technic al standards 

---

## Page 48

 
 
dated February 2014) and the EU EMIR RTS 2.0 (i.e. the technical standards dated October 2017) to the new 
EMIR Refit technical standards. All data including trade, valuation and [[collateral]] elements will need to be 
harmonized. The following harmonized views will be established and visible to GTR users on their reports and 
online searches:  
- Trade State Harmonized View 
- [[Margin]] State Harmonized View 
- Trade Activity Harmonized View (only visible if accessing historical data)  
- [[Margin]] Activity Harmonized View (only visible if accessing historical data) 
These harmonized views of legacy outstanding EMIR [[Derivatives]] trade and [[Margin]] data will be used to 
generate the initial regulatory and client trade and [[Margin]] state reports once EMIR Refit goes live. 
Submission activity prior to EMIR REFIT go live will also be harmonized into the REFIT technical standards 
format.  
The below diagram provides some context around a one-time harmonization exercise that will take place 
just before go-live and how the resulting harmonized views will be integrated into the post EMIR Refit 
ingestion and reporting processes. 
 
 
Please see the ESMA document “Mappings Between Standards” as published on the [[DTCC]] Learning Center 
for more details.   
Data profiling exercises on the UK EMIR Refit data is in progress to ascertain what type of data harmonization 
will be required for UK EMIR Refit data. More information will be provided in near future.  
 
 
 
 


---

## Page 49

 
 
 
Dry Run 
  
FC 7.2:  Upgrading Live (Outstanding) Trades post Go-Live 
Existing outstanding [[Derivatives]] at go-live must be upgraded to the new EMIR Refit data technical standards 
within 180 days of the go-live. If there is a logical business or lifecycle event this “BAU” submission will be 
sufficient to upgrade the trade. If there is no logical business or lifecycle event then a specific trade activity 
message must be submitted with Action Type = “MODI” and Event Type = “UPDT”.  
FC 7.3:  Reporting During Transition Period 
After go-live:  
• In the EU, all reporting will be done using the new schemas in the outgoing messages usage 
guidelines pack from ESMA.  
• In the UK, during the transition period, a subset of reports (Trade State, [[collateral]] State and 
Reconciliation Reports) will be generated using Relaxed schemas in the outgoing m essages usage 
guidelines pack from the FCA. After the transition period, all reporting will be done using the enforced 
schemas in the outgoing messages usage guidelines pack from the FCA.  
The submission and activity-based reports will reflect all data submitted in the new format after go-live.  
FC 7.4:  Go-Live Schedule 
A precise schedule of go-live weekend activities will be published separately closer to implementation.   


---

## Page 50

 
 
 
 
For More Information 
Email [[DTCC]] Learning at: 
derivativeslearning@[[DTCC]].com 
or visit us on the web at: 
derivativeslearning@[[DTCC]].com 