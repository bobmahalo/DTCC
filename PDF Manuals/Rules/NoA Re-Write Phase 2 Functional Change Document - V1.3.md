---
title: "NoA Re-Write 2 Functional Change Document "
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/NoA%20Re-Write%20Phase%202%20Functional%20Change%20Document%20-%20V1.3.pdf"
pages: 25
size: "787.5 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# NoA Re-Write 2 Functional Change Document 

**Original File:** [NoA Re-Write Phase 2 Functional Change Document - V1.3.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/NoA%20Re-Write%20Phase%202%20Functional%20Change%20Document%20-%20V1.3.pdf)  
**Category:** Rules  
**Total Pages:** 25  
**File Size:** 787.5 KB  

---

## Page 1

Global Trade Repository 
FUNCTIONAL CHANGE DOCUMENT:  NORTH 
AMERICA (NOA) RULES RE-WRITE PHASE 2 
VERSION 1.3 
OCTOBER 2023 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
Document Revision History 

---

## Page 2

Date Author Version Description 
June 2023 JY 1.0 Completed Initial Version 
June 30, 2023 JY 1.1 Updated a subset of Slice File outbound field names 
where the equivalent Leg 2 field was removed 
September 27, 2023 RS 1.2 Removing Part 43 details as it’s been deferred  
Added UPI validation examples, Identifier Service 
Updates and updated the PPD Slice files fields
 
October 26, 2023 PC 1.3 Update to Public Website Section 
 

---

## Page 3

TABLE OF CONTENTS 
Document Revision History ................................................................................................................................ 1 
1. Summary ........................................................................................................................................................... 5 
Background ........................................................................................................................................................ 5 
In-Scope ............................................................................................................................................................. 5 
Out of Scope ....................................................................................................................................................... 5 
Reference Documents ........................................................................................................................................ 5 
Naming Conventions and Definitions ................................................................................................................. 5 
2. Functional Change requirements................................................................................................................... 7 
FC 1: Ingestion - Processing of Submissions .................................................................................................... 7 
FC.1.1: Message Validations ............................................................................................................................ 7 
FC 1.2: Message Validations for UPI ................................................................................................................ 7 
FC 1.2.1: UPI Validations against the UPI Database ...................................................................................... 7 
FC 1.2.2: Subsequent UPI submissions and validations ................................................................................ 8 
FC 1.2.3: Other Product fields ......................................................................................................................... 9 
FC 1.3: [[CFTC]] Technical Specification and Guidebook changes ..................................................................... 9 
FC 1.3.1: Action Type and Event Type Validations ........................................................................................ 9 
FC 1.3.2: Additional Technical Specification and Guidebook updates ......................................................... 11 
FC 1.4: Simulator UAT .................................................................................................................................... 12 
FC 1.5: Calculation of Large Notional Off Facility Swap Indicator .................................................................. 12 
FC 2:  PPD Dissemination Changes ................................................................................................................ 12 
FC 2.1:  Time Delay ........................................................................................................................................ 12 
FC 2.2:  Rounding / Capping / Scaling Logic .................................................................................................. 12 
FC 2.3:  Disseminated Fields / Layout of Slice Files ...................................................................................... 16 
FC 2.4:  Public Website Changes – Functionality .......................................................................................... 18 
FC 3: Reports ................................................................................................................................................... 19 
FC 3.1: Report Types, Reporting cycle and Submission Cut-off .................................................................... 19 
FC 3.2: Updates to Report Layouts and Portal Search features .................................................................... 20 
FC 3.3: Merging of Trade Valuation Information onto Trade State Report ..................................................... 22 
FC 4: Other Functional Changes ...................................................................................................................... 24 
FC 4.1:  Trade Identifier Service ..................................................................................................................... 24 
FC 5: Functionality Specific to Go-Live ............................................................................................................ 24 
FC 5.1:  Upgrading Open Trades After Go-Live ............................................................................................. 24 

---

## Page 4

FC 5.2:  Go-Live Schedule.............................................................................................................................. 24 

---

## Page 5

1.  SUMMARY 
Background 
This Functional Document provides an overview of the implementation for compliance date January 29, 2024, 
as part of the North America Rules Re-Write Phase 2.   
In order to keep alignment between North American jurisdictions ([[CFTC]], [[SEC]], and Canada’s 13 provinces 
and territories), changes will be made concurrently across all reporting regimes.  [[SEC]] “no action relief” 
expects this alignment to be applicable with [[CFTC]] requirements, and Canada regulations require UPI as soon 
as it is available.  Also, DDR has agreement with Canadian regulators since go- live that reporting will be in 
line with [[CFTC]], with some Canada specific exceptions.  
In-Scope 
The scope of this document will cover the following changes: 
• Implementation of UPI (Unique Product Identifier) for four [[Asset]] classes (Credit, Interest Rates, Equities, 
Foreign Exchange) where applicable based on jurisdiction.   
• Other changes to the Technical Specifications impacting all [[Asset]] classes  
Out of Scope 
This project will not include: 
• Implementation of ISO20022 for either inbound (to [[DTCC]]) or outbound (to participants or regulators) 
reporting. 
• Implementation of UPI (Unique Product Identifier) for Commodities 
• Public Price Dissemination / Large Trade Calculation Requirements for all [[Asset]] classes based on the 
jurisdictional requirements.  ([[CFTC]]/[[SEC]]) (Note: This change has been deferred until further regulatory 
communication is received)  
 
This functionality will be implemented at a future date which is still to be determined.  
Reference Documents  
This document should be read in conjunction with the following documents: 
1. The NOA Message Specification and all other documents related to this implementation will be available on 
the “Upcoming Changes” section under North America Rules Re-Write of the GTR Learning Center. 
2. [[CFTC]] Technical Specification and other published regulations 
Naming Conventions and Definitions 
Abbreviation/ 
Term Name 
Definition/Description 
ACK GTR Success Acknowledgement Message 
[[CFTC]] Commodity Futures Trading Commission 
Channel A unidirectional link between two end points or queue managers that serves to transfer 
messages 

---

## Page 6

CSV Comma Separated Values – a submission format accepted for messages in GTR 
CSV Message 
Templates 
Field by field layouts of CSV messages defining formats for submissions.  These layouts are 
per message type and are contained as tabs in the message specifications. 
[[DTCC]] Depository Trust and Clearing Corporation 
FpML Financial Product Markup Language – XML based submission type for the GTR and Canada 
PPD 
GTR Global Trade Repository 
Guidebook This document was published by the [[CFTC]] to the SDRs and defines their expectations for 
SDRs for how data is to be reported to them (timing, frequency, report contents, field layouts, 
etc.).  This includes additional fields to be reported which are not contained in the [[CFTC]] 
Technical Specifications. 
LEI Legal Entity Identifier 
MQ Message Queue – message-oriented middleware. Provides mechanism for applications to 
communicate. 
Message 
Specification 
Instructions for submitting into a given GTR application. Includes data attribute requirements, 
valid values, validations, CSV submission layouts and parsing definitions.  This document 
can be found on the Learning Center. 
NACK GTR Negative Acknowledgement message 
NOA North America (referring to [[CFTC]], [[SEC]], and Canada jurisdictions) 
O-Code Operations Code – used to segregate and permission accounts 
P43 and P45 Refer to “Part 43” regulations (also referred to as “PPD”) and “Part 45” [[CFTC]] regulations 
(also referred to as “Trade State”), respectively.  
PPD Acronym for “Public Price Dissemination”, referring to the processing and dissemination of 
(“RT” = “real time”) messages to the public ticker as per Part 43 regulations. 
SDO Account Management System that [[DTCC]] uses to define accounts, products and services 
associated with these participants 
SDR Swap Data Repository 
SFTP Secure File Transfer Protocol 
Trade State Trade state is the latest trade message that has been received and processed by GTR. 
TSR Trade State Report.  Daily report of all open swaps (with latest valuation information merged 
onto the report). 
UAT GTR Test Environment (“User Acceptance Testing”) 
UPI Unique Product Identifier 
USI Unique Swap Identifier 
UTI Unique Trade Identifier 
XML In this document, refers to [[DTCC]] proprietary message format for XML submissions (available 
for NOA submissions only). 

---

## Page 7

2. FUNCTIONAL CHANGE REQUIREMENTS 
FC 1: Ingestion - Processing of Submissions 
FC.1.1: Message Validations  
While there are significant changes to the specific validations required based on the new regulations (as specified 
in the NOA Message Specifications), there will be no changes to the [[BASIC]] process by which messages are 
validated for NOA GTR.  The validation process includes: 
• Schema Validation (validates that the message is formatted correctly so that it can be parsed)  
• Permission Validation (validates that the submitter has permission to submit the message)  
• Core Validation ([[BASIC]] global validations of key fields as defined in the Message Specifications)  
• Jurisdictional Validation (validations specific to each jurisdiction as defined in the Message Specifica tions) 
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
 
 
Further description of the current functionality can be found on the Learning Center : 
Message Validation and Exception Management 
Details of specific validations performed on each message and field are contained in the [[DTCC]] Message 
Specifications.   
GTR NoA Rewrite Phase 2 Message Specification 
A summary of message specification updates for the North America Phase 2 Re- Write can be found on the 
Learning Center: 
[[CFTC]]/Canada/[[SEC]]: GTR North America Rewrite Phase 2 Message Specification –  Summary of Updates 
FC 1.2: Message Validations for UPI 
The Unique Product Identifier (UPI) field will be added to Trade State, PPD and Valuation messages for the 
Credit, Rates, FX and Equities [[Asset]] classes. Commodities will have no change to product fields or product 
validations as UPI will be out of scope. 
FC 1.2.1: UPI Validations against the UPI Database 
DDR will receive a real time feed of UPI data for validation. If a UPI does not exist against the UPI database 
provided from the designated regulatory third party supplier (ANNA-DSB), submissions will be rejected. Any UPI 
status will be accepted. DDR’s UAT Simulator and DDR’s UAT environment will use UAT UPI data (from ANNA -
DSB) at go-live in August and September 2023, respectively, for validations. Production UPI data (from ANNA-

---

## Page 8

DSB) will not be available until October 2023. Production UPI data (from ANNA-DSB) will be incorporated into 
DDR’s UAT Simulator and DDR’s UAT environment and available November 1st 2023. 
Please note there is no affiliation between the third party UPI supplier and DDR. For all inquires on UPI please 
contact ANNA-DSB directly.  
Additionally, there are other fields which will rely on UPI data elements for validation. DDR will receive the 
underlying data elements from the third party supplier related to the UPI submitted in order to perform these 
validations as part of ingestion. 
There will be no cross validations of UPI values between message types (Trade State, PPD and Valuation).  
FC 1.2.2: Subsequent UPI submissions and validations   
The UPI field can be updated with each submission. There is no merging of UPI values to Trade State reporting 
from PPD or valuation submissions. The latest submitted UPI will appear in reporting and the submitted UPI is not 
validated against previous UPI submissions. DDR will not update the UPI or related UPI data elements in reports 
until a subsequent message is submitted and processed. 
Note: UPI will NOT be added to trade uniqueness and there will be no change to trade uniqueness in the NOA 
GTR which is defined as follows: 
• For Trade State (P45) reporting AND Public Price Dissemination (P43) reporting, the uniqueness of a 
trade will be determined by the concatenation of UTI (UTI [[ID]] prefix + UTI [[ID]] value) + USI (U SI [[ID]] prefix + 
USI [[ID]] value) + Trade Party 1 ([[ID]] Type + [[ID]]). 
For brevity, the remainder of this document will use “UTI/USI + TP1” to reference this uniqueness . 
 
UPI Validation Examples:  
• UPI Validation for Trade State, PPD and Valuation  
 
• Modifying a UPI 


---

## Page 9

 
 
FC 1.2.3: Other Product fields   
Current GTR product fields which are redundant with UPI will be removed from ingestion and where the [[CFTC]] 
Technical Specification fields overlap with UPI attributes (e.g., Notional currency, [[settlement]] currency, [[Asset]] 
class), the [[CFTC]] has specified that Technical Specification fields take precedence and need not be validated to 
match the corresponding UPI attributes.   
Submissions with the same UPI Data Elements and [[CFTC]] Tech Spec fields Example: 
 
 
FC 1.3: [[CFTC]] Technical Specification and Guidebook changes 
There are other [[CFTC]] Technical Specification and Guidebook changes that will be included in the January 2024 
implementation. These are included in the Phase 2 Message Specification as well as the Message Specification 
Summary noted above on the Learning Center.  
 
FC 1.3.1: Action Type and Event Type Validations  
Submissions received must contain the relevant “NOA – Action Type” and “Event Type” values.  These values 
must pass both “stateless” validations (i.e., validations that can be performed solely based on the content of the 
message) as well as “stateful” validations (i.e., validations that can only be performed by referencing previous 
submissions for the same trade).  


---

## Page 10

There are no changes to “Stateless” or “Stateful” Validations for Action and Event Types as part of the North 
America Re-Write Phase 2 Implementation in January 2024. There was one new Stateless combination 
(NEWT/UPDT) added to the [[CFTC]] Technical Specification, originally intended for January 2024 but will be 
implemented in June 2023 based on discussions with regulators. Additional details below.  
“Stateless” Validations 
These validations restrict the valid combinations of the “Message type”, “Action Type”, and “Event Type” fields.  
The Message Specifications contain a tab called “Action Type” which details the valid combinations of these fields 
for all messages.  As these combinations can be validated solely based on content of the message, they can be 
tested using the Simulator.   
“NEWT-UPDT” Stateless combination 
Starting June 2023, 'NEWT-UPDT' will be an allowable Action Type/Event Type combo for Trade State 
and PPD messages for CSV, XML and FpML submissions. 
Note: This change was originally scheduled for January 2024 as part of the [[CFTC]] Technical Specification 
version 3.2 updates: “NEWT-UPDT is used for upgrading existing ‘exotic’, ‘complex’, or ‘non-standard’ 
swaps to accurately report and comply with the [[CFTC]] Technical Specification”  
Based on recent discussions, regulators would like firms to use this action/event type combo for 
backloading (see use case below) and this change has been moved to the June 2023 maintenance 
release. 
Backloading Use Case: 
Submission 
Date 
Message 
Type 
Action Transaction 
Type 
Action 
Type 
Event 
Type 
UTI USI Prior 
USI 
Comment 
1/1/2020 Snapshot New Trade       123abc   Trade was submitted and exited prior to the 
Re-arch implementation in Nov 2020. This 
trade was not initialized for the Re-Write 
implementation.  1/1/2020 Snapshot New Exit       123abc   
7/1/2023 Trade 
State 
    NEWT UPDT 456abc   123abc Firm needs to backload valuation message. 
A trade state message needs to be 
submitted to establish the base trade since 
this was not initialized in the Re-Write 
implementation. A UTI must be submitted, 
and the USI can be included in the Prior USI 
trade state field.  
7/1/2023 Trade 
State 
    TERM NOAV 456abc   123abc 
7/1/2023 Valuation     VALU   456abc     
 
Note: Trades that are backloaded that are Expired or Terminated will not be reported on the Trade State 
Report. Submissions will be reported in the Activity Reports.  
 
“Stateful” Validations 
These validations control the allowable sequences of Action Types.  Each new submission will be validated to 
confirm that the action type is consistent with the allowable sequence as per the action type state diagrams below.  
These validations will be performed per unique trade + per Jurisdiction and will be done separately for P43 (PPD) 
and P45 (Trade State) submissions.  The latest version of these diagrams will always be contained in the 
Message Specifications.  
 

---

## Page 11

 
 
FC 1.3.2: Additional Technical Specification and Guidebook updates   
Other changes that will be implemented across all jurisdictions and will impact all [[Asset]] classes, include the 
following:   
Open
Transferred Out
ERORTerminated Expired
(No action type needed to expire)
Errored
NEWT*
PRTO***
NEWT*/
(PTNG)
MODI*, 
CORR*
MODI**, 
CORR**,
VALU, MARU
MODI, CORR, 
VALU, MARU
MODI*, CORR*, 
VALU, MARU
TERM
REVI* EROR REVI*
Action Type State Diagram – Part 45
NEWT**
REVI**
EROR
NOTES:     * with Expiration Date >= today
                ** with Expiration Date < today
              *** PRTO is also accepted (but not expected) for terminated or expired 
REVI**
TERM
Open or Expired
ERORTerminated Errored
NEWT
MODI, CORR
MODI, CORR
TERM
REVI EROR REVI
Action Type State Diagram – Part 43

---

## Page 12

• Updates to valid values to allow for negative amounts for Notional Amount fields (Notional Amount, Put 
Amount, Call Amount, Notional amount in effect on associated effective date)  
• Removal of Leg 2 fields for Call Amount, Call currency, Put amount, Put currency and [[settlement]] location. 
• Change of [[Asset]] class application (“XA” to “FX”) for [CDE - Call amount-Leg 1], [CDE - Call currency-Leg 
1], [CDE - Put amount-Leg 1] and [CDE - Put currency-Leg 1]) 
• Addition of [Other Payment Payer [[ID]] Type] and [Other Payment Receiver [[ID]] Type] fields for Trade State 
submissions 
• Updated Validations for [CDE - Other Payment Payer [[ID]]] and [CDE - Other Payment Receiver [[ID]]] which 
will be validated based on respective [[ID]] Type entered (LEI, NPID, etc.) 
Please refer to the latest Phase 2 Message Specification on the Learning Center for the latest changes.  
FC 1.4: Simulator UAT 
The Simulator is a web-based application built to provide users with a self-servicing utility and enables a user test 
and verify their submissions in a stand-alone environment.  
For the North America Re-Write Phase 2, the simulator will include database lookup validations for UPI against the 
UPI database which is a new feature (e.g., The current simulator does not validate against GLEIF for LEIs).  
FC 1.5: Calculation of Large Notional Off Facility Swap Indicator 
Currently, [[DTCC]] supports the calculation of inbound harmonized field “Large Trade Indicator” for P43 (RT/PPD) 
and Part 45 (Trade State) submissions for non-SEF/DCM submitters (based on role of submitter in SDO) if the 
field is left blank. 
Current details of how the GTR determines whether a given submission qualifies as “large” and what inbound 
fields are published on the Learning Center:   
 
Large Trade Size Calculation  (Current functionality) 
 
Note: Part 43 regulatory changes have been deferred for Phase 2 until further details are received from regulators. 
There will be no updates to this functionality planned for January 2024. 
FC 2:  PPD Dissemination Changes  
Once RT submissions are parsed and validated, the GTR performs additional functions as required to prepare the 
message for dissemination and to disseminate it onto the public ticker.  This [[BASIC]] functionality is largely 
unchanged except where reference to new data elements is required. 
 
FC 2.1:  Time Delay 
Regulators have specified the following Time Delays when disseminating PPD submissions to the public. There 
are no changes to Time Delay logic in the Phase 2 implementation. 
FC 2.2:  Rounding / Capping / Scaling Logic 
Rounding, Capping and Scaling logic is applied to Notional or Principal amounts and other financial fields in order 
to protect the anonymity of swap counterparties. In the NoA Re-Write, Rounding, Capping and Scaling logic 
remains largely unchanged. The majority of the changes for the NoA Re-Write relate to newly added, removed or 
updated fields and the respective valid values allowed, which are summarized below:   

---

## Page 13

Note: Part 43 regulatory changes have been deferred for Phase 2 until further details are received from regulators. 
Updates for January 2024 for [[CFTC]] Technical Specification/Guidebook updates are noted below.  
 
Rounding logic ([[CFTC]] / [[SEC]] only) 
There is no change to the rounding logic on notional amount fields. Rounding rules are applied as follows:  
 
[[CFTC]] and [[SEC]] Rounding Scale and Examples 
Floor Ceiling Round to (if equidistant, always to 
the highest multiple) 
Use Cases 
Notional Amount 
(Submitted Value) Rounded 
>= 0 < 5 5 (Value cannot be less than 5) 2 5 
     
>= 5 < 1,000 Nearest multiple of 5 222 220 
222.5 225 
          
>= 1,000 < 10,000 Nearest multiple of 100 8,640 8,600 
8,650 8,700 
          
>= 10,000  < 100,000 Nearest multiple of 1,000 44,300 44,000 
44,500 45,000 
          
>= 100,000 < 1,000,000 Nearest multiple of 10,000 744,500 740,000 
745,000 750,000 
          
>= 1,000,000 < 100,000,000 Nearest multiple of 1,000,000 89,100,000 89,000,000 
89,800,000 90,000,000 
          
>= 100,000,000 < 500,000,000 Nearest multiple of 10,000,000 372,000,000 370,000,000 
377,000,000 380,000,000 
          
>= 500,000,000 < 1,000,000,000 Nearest multiple of 50,000,000 810,000,000 800,000,000 
835,000,000 850,000,000 
          
>= 1,000,000,000 < 100,000,000,000 Nearest multiple of 100,000,000 66,650,000,000 67,700,000,000 
87,010,000,000 87,000,000,000 
          
>= 100,000,000,000 None Nearest multiple of 10,000,000,000 101,000,000,000 100,000,000,000 
227,000,000,000 230,000,000,000 
 
Canada Rounding Scale and Examples 
Floor Ceiling Round to (if equidistant, always to 
the highest multiple) 
Use Cases 
Notional Amount 
(Submitted Value) Rounded 
>= 0 < 1,000 Nearest multiple of 5 1 5 
986 985 
        
>= 1,000 < 10,000 Nearest multiple of 100 8,867 8,900 
8,849 8,800 
        
>= 10,000  < 100,000 Nearest multiple of 1,000 10,234 10,000 
10,598 11,000 
        
>= 100,000 < 1,000,000 Nearest multiple of 10,000 478,237 480,000 
494,363 490,000 
        
>= 1,000,000 < 10,000,000 Nearest multiple of 100,000 9,163,000 9,200,000 
9,130,000 9,100,000 
        

---

## Page 14

>= 10,000,000 < 50,000,000 Nearest multiple of 1,000,000 48,650,000 49,000,000 
42,320,000 42,000,000 
        
>= 50,000,000 < 100,000,000 Nearest multiple of 10,000,000 
61,500,000 60,000,000 
66,500,000 70,000,000 
        
>= 100,000,000 < 500,000,000 Nearest multiple of 50,000,000 460,000,000 450,000,000 
380,000,000 400,000,000 
        
>= 500,000,000 < 1,000,000,000 Nearest multiple of 100,000,000 
625,000,000 600,000,000 
850,000,000 900,000,000 
        
>= 1,000,000,000 < 100,000,000,000 Nearest multiple of 500,000,000 
30,750,000,000 31,000,000,000 
56,535,530,000 56,500,000,000 
     
>= 100,000,000,000  Nearest multiple of 50,000,000,000 
175,000,000,000 200,000,000,000 
255,000,000,000 250,000,000,000 
 
Rounding, Capping and Scaling for Notional Amount fields (All jurisdictions) 
Logic to apply the rounding, capping and scaling logic for Notional Amount fields will start with a Chosen Leg.  
Capping and rounding is applied to all fields in the chosen leg prior to scaling and the application of capping and 
rounding requirements to the other leg and other financial fields. 
As part of the Phase 2 implementation: 
(1) The following fields were changed from "XA" to "FX": 
a. [CDE - Call amount-Leg 1] and [CDE - Call currency-Leg 1] 
b. [CDE - Put amount-Leg 1] and [CDE - Put currency-Leg 1]  
(2) The following fields were removed: 
a. [CDE - Call amount-Leg 2] and [CDE - Call currency-Leg 2] 
b. [CDE - Put amount-Leg 2] and [CDE - Put currency-Leg 2] 
Changes are reflected below in purple.  
Fields included in Leg 1 and Leg 2:  
Leg 1 Leg 2 
 [Notional Amount 1]*  [Notional Amount 2]* 
 [CDE - Notional amount in effect on associated 
effective date-Leg 1] 
 [CDE - Notional amount in effect on associated 
effective date-Leg 2] 
 [CDE - Call amount-Leg 1] (FX only)  [CDE - Call amount-Leg 2] 
 [CDE - Put amount-Leg 1] (FX only)  [CDE - Put amount-Leg 2] 
 [Leg 1 - Total Notional Quantity] (EQ, CO only)  [Leg 2 - Total Notional Quantity] (EQ, CO only) 
 [Leg 1 - Notional Quantity] (CO only)  [Leg 2 - Notional Quantity] (CO only) 
 
*The Chosen Leg is Chosen leg first using [Notional Amount 1] or [Notional Amount 2] for FX, IR, EQ and CR 
determined by the logic below. [Notional Amount 1] is used to determine capping and scaling for CO.  
 
• If [Notional Amount 2] = 0 or [Notional Currency 2] is blank, choose [Notional Amount 1] (Leg 1 - because there 
is no leg 2) 

---

## Page 15

• ELSE If [Notional Currency 1] AND [Notional Currency 2] = USD, choose the largest Notional amount between 
[Notional Amount 1] and [Notional Amount 2]. If [Notional Amount 1] and [Notional Amount 2] are equal, choose 
both. 
• ELSE if [Notional Currency 1] AND [Notional Currency 2] are both not USD, convert both to USD and choose the 
largest Notional amount between [Notional Amount 1] and [Notional Amount 2]. If [Notional Amount 1] and 
[Notional Amount 2] are equal, rounding and capping will be applied to both, and the Chosen Leg will be Leg 1. 
Conversion is up to 5 decimal places – rounded half up or down. 
• If the Notional Amount is “99999999999999999999.99999” which is accepted when the value is not available at 
the time of reporting, no capping, scaling, or rounding rules will be applied. Disseminate as 
“99999999999999999999.99999”. The chosen leg is the Notional Amount field that is not 
“99999999999999999999.99999”. If both legs are “99999999999999999999.99999”, the chosen leg is [Notional 
Amount 1] / Leg 1. 
 
Notional Amount Valid Value updates 
The Notional Amount fields will be updated in the Phase 2 implementation to include any value. (Previously 
‘Greater than Zero’). If either [Notional Amount 1] and [Notional Amount 2] are negative values, DDR will take the 
absolute value.  This absolute value will be the value used in the process of capping, rounding and scaling.  These 
fields include:  
• [Notional Amount 1] 
• [CDE - Notional amount in effect on associated effective date-Leg 1] 
• [Notional Amount 2] 
• [CDE - Notional amount in effect on associated effective date-Leg 2] 
• [CDE - Call amount-Leg 1] (FX only) 
• [CDE - Put amount-Leg 1] (FX only) 
 
Field Updates (All jurisdictions) 
The tables below show the additional fields that are capped, rounded or scaled and fields used as input for the 
PPD transformation logic. (Note: There are no changes for the January 2024 implementation from current Re -
Write logic below:) 
   
 
Re-Write / 
Re-Write 
Phase 2 
Capping & 
Rounding 
Scaling 
Notes: 
CDE - Other payment amount 
(This field replaces ‘Payment 1 – Amount’) 
XA    
• Scaling will be applied to the first 10 
values submitted and only 10 values are 
disseminated. Values are separated by 
“;” in one field for reporting. 
• Added - Commodity and FX [[Asset]] Class 
applicability 
[[Premium]] Amount XA      
Price 1 - Price CO, EQ       
 
Inbound fields used as input for Capping, Rounding and Scaling logic: (Note: There are no changes for the 
January 2024 implementation from current Re-Write logic below:) 
Use Re-Write Field [[Asset]] Class 
Applicability 
Currency conversions and categories for Capping 
Notional Currency 1 XA 
Notional Currency 2 XA 
CDE - Call currency-Leg 1 XA 
CDE - Call currency-Leg 2 XA 

---

## Page 16

CDE - Put currency-Leg 1 XA 
CDE - Put currency-Leg 2 XA 
Tenor Calculation 
CDE - Expiration Date IR, CR 
Maturity Date of the Underlying IR, CR 
CDE - Effective Date IR, CR 
Original Execution Timestamp IR, CR 
Scaling for Price 1 - Price Price 1 - Units CO, EQ 
Spread Amount (in Basis Points) Calculation  
CDE - Spread notation-Leg 1 CR 
Leg 1 - Spread Amount CR 
CDE - Spread notation-Leg 2 CR 
Leg 2 - Spread Amount CR 
FC 2.3:  Disseminated Fields / Layout of Slice Files 
There will be three additional fields for the slice files as part of the Phase 2 implementation which have been 
added to the end of the slice files: 
Change:  Slice File Field Names 
  Dissemination Identifier 
  Original Dissemination Identifier 
 Action type 
 Event type 
  Event timestamp 
 Amendment indicator 
 [[Asset]] Class 
 Product name 
  Cleared 
 Mandatory clearing indicator 
  Execution Timestamp 
 Effective Date 
 Expiration Date 
 Maturity date of the underlier 
 Non-standardized term indicator 
 Platform identifier 
 Prime brokerage transaction indicator 
 Block trade election indicator 
 Large notional off-facility swap election indicator 
 Notional amount-Leg 1 
 Notional amount-Leg 2 
 Notional currency-Leg 1 
 Notional currency-Leg 2 
 Notional quantity-Leg 1 
 Notional quantity-Leg 2 
 Total notional quantity-Leg 1 
 Total notional quantity-Leg 2 
 Quantity frequency multiplier-Leg 1 
 Quantity frequency multiplier-Leg 2 
 Quantity unit of measure-Leg 1 
 Quantity unit of measure-Leg 2 
 Quantity frequency-Leg 1 
 Quantity frequency-Leg 2 
 Notional amount in effect on associated effective date-Leg 1 
 Notional amount in effect on associated effective date-Leg 2 
 Effective date of the notional amount-Leg 1 
 Effective date of the notional amount-Leg 2 
 End date of the notional amount-Leg 1 

---

## Page 17

Change:  Slice File Field Names 
 End date of the notional amount-Leg 2 
Updated field name Call amount-Leg 1 
Removed Call amount-Leg 2 
Updated field name Call currency-Leg 1 
Removed Call currency-Leg 2 
Updated field name Put amount-Leg 1 
Removed Put amount-Leg 2 
Updated field name Put currency-Leg 1 
Removed Put currency-Leg 2 
  Exchange rate 
  Exchange rate basis 
 First exercise date 
 Fixed rate-Leg 1 
 Fixed rate-Leg 2 
  [[Option]] [[Premium]] Amount 
  [[Option]] [[Premium]] Currency 
 Price 
 Price unit of measure 
 Spread-Leg 1 
 Spread-Leg 2 
 Spread currency-Leg 1 
 Spread currency-Leg 2 
 Strike Price 
 Strike price currency/currency pair 
 Post-priced swap indicator 
 Price currency 
 Price notation 
 Spread notation-Leg 1 
 Spread notation-Leg 2 
 Strike price notation 
 Fixed rate day count convention-leg 1 
 Fixed rate day count convention-leg 2 
 Floating rate day count convention-leg 1 
 Floating rate day count convention-leg 2 
 Floating rate reset frequency period-leg 1 
 Floating rate reset frequency period-leg 2 
 Floating rate reset frequency period multiplier-leg 1 
 Floating rate reset frequency period multiplier-leg 2 
 Other payment amount 
 Fixed rate payment frequency period-Leg 1 
 Floating rate payment frequency period-Leg 1 
 Fixed rate payment frequency period-Leg 2 
 Floating rate payment frequency period-Leg 2 
 Fixed rate payment frequency period multiplier-Leg 1 
 Floating rate payment frequency period multiplier-Leg 1 
 Fixed rate payment frequency period multiplier-Leg 2 
 Floating rate payment frequency period multiplier-Leg 2 
 Other payment type 
 Other payment currency 
 [[settlement]] currency-Leg 1 
 [[settlement]] currency-Leg 2 
Updated field name [[settlement]] location Leg 1 
Removed [[settlement]] location Leg 2 
 Collateralisation category 
 Custom basket indicator 

---

## Page 18

Change:  Slice File Field Names 
 Index factor 
 Underlier [[ID]]-Leg 1 
 Underlier [[ID]]-Leg 2 
 Underlier [[ID]] source-Leg 1 
 Underlying [[Asset]] Name 
 Underlying [[Asset]] subtype or underlying contract subtype-Leg 1 
 Underlying [[Asset]] subtype or underlying contract subtype-Leg 2 
 Embedded [[Option]] type 
 [[Option]] Type 
 [[Option]] Style 
 Package indicator 
 Package transaction price 
 Package transaction price currency 
 Package transaction price notation 
 Package transaction spread 
 Package transaction spread currency 
 Package transaction spread notation 
 Physical delivery location-Leg 1 
 Delivery Type 
New Unique Product Identifier  
New UPI FISN  
New UPI Underlier Name  
 
FC 2.4:  Public Website Changes – Functionality 
The Daily/ Historical Search includes two tabs to select data submitted before and after the Re- Write Phase 2 in 
their respective report format. DDR maintains one year’s worth of public data on the website. This historical look 
up for Pre Re-Write (Re-Architecture format) will be removed as all data will be in the Re-Write format by the 
Phase 2 implementation.   
 
The PPD Ticker Screen organizes transactions according to [[Asset]] class. Users must click on the respective 
[[Asset]] class tab link to see the PPD data related [[Asset]] classes.  
 
Previously, the ticker showed the most recent transaction by [[Asset]] class and product [[ID]] and a subset of fields. In 
the Re-Write Phase 2, the Ticker Tab module contains the latest 100 transactions by [[Asset]] class with a scroll bar 
at the bottom of the screen to view all fields. It contains the same fields found in the slice file layouts 
.  


---

## Page 19

 
 
 
RSS Feeds will be decommissioned in this implementation.
FC 3: Reports  
Daily reports are generated and made available through the [[DTCC]] Portal.  Further details on functionality within 
the portal can be found on the Learning Center.    
NoA Portal Overview 
FC 3.1: Report Types, Reporting cycle and Submission Cut-off 
The following reports will be created daily. There have been no changes to the report types.  
 Type  Description 
 Trade State 
Report 
• Contains the latest trade state for all open trades for each unique trade that contains the relevant jurisdiction 
value in the Reporting destination data element.  
• This report is created per [[Asset]] class per jurisdiction. 
• Trades which expire on or after reporting date are included.   
• Trades which have been submitted with action type TERM or EROR (and not subsequently revived) or have 
been submitted with action type PRTO (and not ported back in) are not included (even if their expiration date 
is in the future). 
• Trade valuation data is merged onto this report.  [[collateral]] valuation data is NOT merged onto this report. 
 Trade Activity 
Report 
• Contains all successful submissions for trade state (not PPD/RT, valuation and [[collateral]]) message types 
that contain the relevant jurisdictional value in the Reporting destination data element. 
• This report is created per [[Asset]] class per jurisdiction. 
 Submission 
Report 
• Contains all the successful (ACK) and unsuccessful (NACK) submissions submitted by the client as well as 
those submissions made on their behalf.  
• This report is created per [[Asset]] class per jurisdiction. 
• There will be a separate [[collateral]] submission report. 
 Public Price 
Status Report 
• Contains all the successful PPD submissions received for the reporting date, as well as PPD submissions 
which may have been received on a previous date, but which were disseminated on the reporting date.  
• The PPD status report includes transformed (rounded, capped, scaled) values as well as original values 
submitted. 
• This report is created per [[Asset]] class per jurisdiction. 
Valuation 
Activity Report  
• Contains all successful Valuation submissions processed for the reporting date. 
• This report is created per [[Asset]] class per jurisdiction. 
• It will be provided to submitters, reporting parties, and regulators. 


---

## Page 20

Error! No text of specified style in document. 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 20 
 Type  Description 
 [[collateral]] 
Activity Report 
  
• Contains all successful [[collateral]] Valuation submissions processed for the reporting date.   
• This report will be produced per jurisdiction (currently [[CFTC]] only). 
• This report is not produced per [[Asset]] class as the content is not [[Asset]]-class specific. 
• It will be provided to submitters, reporting parties, and regulators. 
 Trade State 
Allege Report 
• Contains the latest trade state for all open trades for each unique trade that contains the relevant jurisdiction 
value in the Reporting destination data element where the report recipient is named as “Trade Party 2”  
• This report is created per [[Asset]] class per jurisdiction. 
• Trades which expire on or after reporting date are included.   
• Trades which have been submitted with action type TERM or EROR (and not subsequently revived) or have 
been submitted with action type PRTO (and not ported back in) are not included (even if their expiration date 
is in the future). 
• Trade valuation data and [[collateral]] valuation data are NOT merged onto this report. 
 
There are no changes to the current reporting cycle and submission times which are produced according to the 
following schedule: 
 
Report 
Date 
Report 
Run Date Reporting Includes 
Monday Tuesday All applicable submissions received between 00:00:00 ET Monday up to but not including 00:00:00 ET Tuesday 
Tuesday Wednesday All applicable submissions received between 00:00:00 ET Tuesday up to but not including 00:00:00 ET Wednesday 
Wednesday Thursday All applicable submissions received between 00:00:00 ET Wednesday up to but not including 00:00:00 ET Thursday 
Thursday Friday All applicable submissions received between 00:00:00 ET Thursday up to but not including 00:00:00 ET Friday 
Friday Saturday All applicable submissions received between 00:00:00 ET Friday up to but not including 00:00:00 ET Saturday 
Saturday Sunday All applicable submissions received between 00:00:00 ET Saturday up to but not including 00:00:00 ET Sunday 
Sunday Monday All applicable submissions received between 00:00:00 ET Sunday up to but not including 00:00:00 ET Monday 
 
FC 3.2: Updates to Report Layouts and Portal Search features 
There are several updates to the Report Layouts as a result of new fields. Fields no longer ingested will continue 
to be reported until a new submission in the North America Re- Write Phase 2 is processed. There will be no 
removed [[participant]] or regulatory reporting fields as part of this implementation. The list of new fields added to 
the respective reports are listed below. The Portal Search will also include the fields below for selection and 
extraction.  
 
 
[[CFTC]], [[SEC]], Canada 
[[CFTC]], 
Canada [[CFTC]] 
 
Submission 
Report 
Trade State 
Report 
Trade State 
Activity 
Trade State 
Allege 
PPD 
Status 
Valuation 
Activity 
[[collateral]] 
Activity 

---

## Page 21

Error! No text of specified style in document. 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 21 
Counterparty 1 identifier 
source*        
Clearing [[Member]] [[ID]] Source*            
Unique product identifier          
Other Payment Payer [[ID]] Type              
Other Payment Receiver [[ID]] 
Type              
*These fields are current inbound fields that are included in submission reports 
Additionally, 56 UPI Data Elements will be included on Trade State Reports based on the UPI submitted in the 
Trade State message. These fields will be available for extraction on the Portal Search when performing running 
a query.  
1. UPI-[[Asset]] Class 
2. UPI-Instrument Type 
3. UPI-Level 
4. UPI-Product 
5. UPI-Additional Sub Product 
6. UPI-Base Product 
7. UPI-Contract Specification 
8. UPI-Debt Seniority 
9. UPI-Delivery Type 
10. UPI-Instrument ISIN 
11. UPI-Instrument LEI 
12. UPI-Notional Currency 
13. UPI-Notional Schedule 
14. UPI-[[Option]] Exercise Style 
15. UPI-[[Option]] Type 
16. UPI-Other Additional Sub Product 
17. UPI-Other Base Product 
18. UPI-Other Leg Reference Rate 
19. UPI-Other Leg Reference Rate Term Unit 
20. UPI-Other Leg Reference Rate Term Value 
21. UPI-Other Leg Underlier Characteristic 
22. UPI-Other Notional Currency 
23. UPI-Other Reference Rate 
24. UPI-Other Sub Product 
25. UPI-Other Underlier Characteristic 
26. UPI-Place of [[settlement]] 
27. UPI-Reference Rate 
28. UPI-Reference Rate Term Unit 
29. UPI-Reference Rate Term Value 
30. UPI-Return or Payout Trigger 
31. UPI-[[settlement]] Currency 
32. UPI-Sub Product 
33. UPI-Underlier Characteristic 
34. UPI-Underlying [[Asset]] Type 
35. UPI-Underlying Credit Index Series 
36. UPI-Underlying Credit Index Version 
37. UPI-Underlying Instrument Index 
38. UPI-Underlying Instrument Index Prop 
39. UPI-Underlying Instrument Index Term Unit 
40. UPI-Underlying Instrument Index Term Value 
41. UPI-Underlying instrument ISIN 

---

## Page 22

Error! No text of specified style in document. 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 22 
42. UPI-Underlying instrument LEI 
43. UPI-Underlying Instrument DSB 
44. UPI-Underlying [[issuer]] Type 
45. UPI-Valuation Method or Trigger 
46. UPI-Last Update Date Time 
47. UPI-Status 
48. UPI-Status Reason 
49. UPI-CFI Delivery Type 
50. UPI-CFI [[Option]] Style and Type 
51. UPI-Classification Type 
52. UPI-Short Name 
53. UPI-Single or Multiple Currency 
54. UPI-Underlier Name 
55. UPI-Further Grouping 
56. UPI- DSB UPI 
 
FC 3.3: Merging of Trade Valuation Information onto Trade State Report 
There is no change to the current functionality. UPI will NOT be merged from Valuation reports to Trade State 
Reporting even if the Trade State submission is blank and the Valuation submission contains a UPI.  
Current Functionality: 
1) Merging of fields from Valuation submission onto TSR:  This will continue to be the case (EXCEPT 
for the fields Initial [[Margin]] Portfolio Code and Variation [[Margin]] Portfolio Code) after the Phase 2 
Implementation.  Based on [[CFTC]] instructions, when merging trade valuations onto the Trade State 
Report, the values for Initial [[Margin]] Portfolio Code and Variation [[Margin]] Portfolio Code are to be 
selected from the Valuation submission with the most recent valuation timestamp.  If no Valuation 
message has ever been received into the GTR for the trade, the values from the Trade State 
submission will be reported on the TSR.   
Note that this means the fields Submitter and Submission Timestamp on the TSR will continue to be 
based on the information on the Trade State submission (i.e., they will not be updated with the values 
from the Trade Valuation submission). 
2) Timestamp used for merging the “latest” valuation:  The valuation submission used for merging 
onto the TSR will be based on the Valuation Timestamp. 
3) Adding UTI to a trade using the Valuation submissions:   This functionality will not change.  If a 
UTI is added to a USI-only trade using a Valuation message, we allow this to be added to the trade for 
reporting. 
As is the case currently, when matching a Valuation to a base trade for merging information onto the TSR at 
end of day, the UTI + USI + Trade Party 1 + Trade Party 2 + Jurisdiction must match.  
Examples for Merge of Portfolio Codes onto Trade State Report: 

---

## Page 23

Error! No text of specified style in document. 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 23 
  
Case Message 
Received T/S
Valuation 
Date/Time Message Type
IM 
Portfolio 
C
ode
VM 
Portfolio 
C
ode
Reported   
IM Portfolio 
C
ode
Reported   
VM 
P
ortfolio 
Code
Comments
2/11/2022 18:59 (N/A) Trade State TS-IM1 TS-VM1
2/11/2022 21:59 2/11/2022 20:59 Valuation VL-IM1 VL-VM1
2/11/2022 18:59 (N/A) Trade State TS-IM1 TS-VM1
2/11/2022 21:59 2/11/2022 20:59 Valuation (blank) (blank)
3 2/11/2022 18:59 (N/A) Trade State TS-IM1 TS-VM1 TS-IM1 TS-VM1 No Valuation Message Received - use values from 
Trade State submission.
2/11/2022 18:59 (N/A) Trade State TS-IM1 (blank)
2/11/2022 21:59 2/11/2022 20:59 Valuation (blank) VL-VM1
2/11/2022 18:59 (N/A) Trade State (blank) (blank)
2/11/2022 21:59 2/11/2022 20:59 Valuation VL-IM1 VL-VM1
2/11/2022 22:59 2/9/2022 17:59 Valuation VL-IM2 VL-VM2
Reported DataSubmitted Data
VL-VM1
(blank)
VL-VM1
VL-VM15 VL-IM1
Use the Valuation Value with the most recent 
Valuation Timestamp (not the most recent 
m
essage received timestamp).
2 (blank) Use the Valuation Value when available (even if 
blank)
4 (blank) Use the Valuation Value when available (will not 
mix/match partial information)
1 VL-IM1 Use the Valuation Value when available (even if 
different from trade state submission)

---

## Page 24

Error! No text of specified style in document. 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 24 
FC 4: Other Functional Changes   
FC 4.1:  Trade Identifier Service 
Identifier Service for [[CFTC]], [[SEC]] and Canada will generate identifiers in the [UTI [[ID]]] field only. The UTI [[ID]] will 
no longer be split between [UTI Prefix] and [UTI [[ID]]] 
FC 5: Functionality Specific to Go-Live 
Clients are expected to upgrade their open trades to the new data standards as defined in the message 
specifications after go-live.  This section describes relevant functionality to support that process and other go-
live related processes. 
 
Please note that these activities will be performed during both UAT and Production go- lives.  
FC 5.1:  Upgrading Open Trades After Go-Live 
Open trades at go-live can be upgraded to the new data standards after go-live by either successfully 
submitting a specific trade state message with Action Type = “MODI” and Event Type = “UPDT”, or by 
successfully submitting the next logical trade lifecycle event as per the normal course of business.    
 
Public Price Disseminations (PPD/RT) [[DO]] not require an explicit upgrade to new data standards.  Submissions 
after go-live should be the appropriate post-trade event. 
FC 5.2:  Go-Live Schedule 
A precise schedule of go-live weekend activities will be published separately closer to implementation.  At a 
high level, the production implementation plan includes: 
- Completion of final reporting cycle in current production environment for business date Friday, January 
26, 2024. 
- System downtime for new code implementation, removal of duplicate trades, and Action Type 
initialization activities (timing TBD). 
- System startup with new code in place, ready for firms to begin submissions which comply with new 
rules (timing TBD). 

---

## Page 25

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. The services described herein are provided under the “[[DTCC]]” brand name by 
certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  
Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in 
which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they 
offer. 
Doc Date:  
Publication Code:  
Service:  
Title: 
For More Information 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 