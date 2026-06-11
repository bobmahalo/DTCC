---
title: "Processing Rules for Broker Dealer of Record Change: B2B Client Transmission"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/irs102_20201020_b2b_clients_rules_for_bdofr_techguide.pdf"
pages: 15
size: "315.9 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# Processing Rules for Broker Dealer of Record Change: B2B Client Transmission

**Original File:** [irs102_20201020_b2b_clients_rules_for_bdofr_techguide.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/irs102_20201020_b2b_clients_rules_for_bdofr_techguide.pdf)  
**Category:** Rules  
**Total Pages:** 15  
**File Size:** 315.9 KB  

---

## Page 1

 [[DTCC]] Public (White) 
 
 
 
INSURANCE & RETIREMENT 
SERVICES 
PROCESSING RULES FOR [[Broker]] DEALER OF RECORD CHANGE: B2B 
CLIENT TRANSMISSION 
APRIL 15, 2020 
 


---

## Page 2

 
 [[DTCC]] Public (White) 
© 2020 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: April 15, 2020 
Publication Code: IRS102 
Service: Insurance & Retirement Services 
Title: Processing Rules for [[Broker]] Dealer of Record Change: B2B Client Transmission 
 
 

---

## Page 3

 
 [[DTCC]] Public (White) 
CHANGE HISTORY 
Dates Description 
April 15, 2020 In support of the September 2020 release, required to enter a CRD Number and/or NPN 
Number for all Agents. 
 

---

## Page 4

 
 [[DTCC]] Public (White) 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 5 
Processing Rules ................................................................................................................................................. 6 
Best Practice ....................................................................................................................................................... 12 
GENERAL ......................................................................................................................................................... 12 
AGENT Information........................................................................................................................................... 12 
Non-Custodial to Non-Custodial Rules ............................................................................................................. 12 
RELATIONSHIP Information ........................................................................................................................... 12 
Non-Custodial or Custodial to Custodial Rules ................................................................................................ 13 
RELATIONSHIP Information ........................................................................................................................... 13 
Custodial to Non-Custodial Rules ..................................................................................................................... 13 
RELATIONSHIP Information ........................................................................................................................... 13 
Non-Qualified Rules .......................................................................................................................................... 14 
RELATIONSHIP Information ........................................................................................................................... 14 
 

---

## Page 5

Processing Rules For [[Broker]] Dealer Of Record Change: B2B Client Transmission 
Introduction 5 [[DTCC]] Public (White) 
INTRODUCTION 
The following are the significant data elements supporting the [[Broker]] Dealer of Record Change (Change of 
Financial Institution). When building the B2B Policy Administration (TXLife 113) request message, build the 
message supporting these elements and the rules supporting each of the five (5) Change or Financial 
Institution transfer types.  
Important:  
To produce a valid message for processing, the below requirements in this document must be used in combination with the 
[[DTCC]] Policy Administration IFT web services schema requirements. The request message delivered to the carrier should 
be consistent of a Policy Administration request message generated from the IFT Access Platform or from a client’s B2B 
transmission.  
Supported transfer types are 
Current [[Broker]] TO New [[Broker]] 
Custodial  Custodial (Qualified) 
Non-Custodial  Custodial (Qualified) 
Non-Custodial   Non-Custodial (Qualified) 
Custodial   Non-Custodial (Qualified) 
Non-Custodial   Non-Custodial (Non-Qualified) 
 
 

---

## Page 6

Processing Rules For [[Broker]] Dealer Of Record Change: B2B Client Transmission 
Processing Rules 6 [[DTCC]] Public (White) 
PROCESSING RULES 
 
[[Broker]] Dealer of Record Max 
Length 
Custodial to 
Custodial and 
Non-Custodial 
to Custodial 
Non-Custodial 
to Non-
Custodial 
Custodial to 
Non-Custodial 
Non-Qualified 
(Non-Custodial 
to Non-
Custodial) 
Contract Number 
 
Holding.Policy.PolNumber 
 
 30 
R R R R 
Client Account Number 
 
Holding.DistributorClientAcctNum 
 
 30 
R R R R 
Continue SWP? 
 
* Yes (1) 
*No  (0) 
* Unknown (don’t populate) 
 
Holding.Arrangement.ContinueArr
angementInd  
O 
Populate when 
response = Yes 
or No, else (ie 
unknown) don’t 
populate 
Arrangement 
Object 
O 
Populate when 
response = Yes 
or No, else  (ie 
unknown) don’t 
populate 
Arrangement 
Object 
O 
Populate when 
response = Yes 
or No, else  (ie 
unknown) don’t 
populate 
Arrangement 
Object 
O 
Populate when 
response = Yes 
or No, else  (ie 
unknown) don’t 
populate 
Arrangement 
Object 
Relationship Type 
 
* Owner (8) 
Joint Owner (184) 
* Primary Beneficiary (34) 
* Contingent Beneficiary (36) 
* Annuitant (35) 
*Joint Annuitant (183) 
 
Relation.RelationRoleCode 
30 
Owner – R 
(1 occurrence) 
 
Annuitant – R (1 
occurrence) 
 
Beneficiary – R 
(1 occurrence) 
Owner – R 
(1 occurrence) 
 
Annuitant  - O 
(0,1 occurrence) 
Owner – R 
(1 occurrence) 
 
Annuitant – R 
(1 occurrence) 
 
Beneficiary –R 
(1,8 occurrence) 
Owner (or Joint 
Owner)– R 
(1, 10 occurrence) 
 
Annuitant (or Joint 
Annuitant) – O 
(0, 2 occurrence) 
 
Use ‘Joint Owner’ 
for all when multi 
Owner 
 
Use ‘Joint 
Annuitant’ for all 
when multi 
Annuitants 
 
First Name 
 
Party.Person.FirstName 
25 
C 
Required for 
Annuitant 
C 
Required for each 
Relation Role 
Owner – R 
Annuitant –R 
Beneficiary– C 
Required when 
‘Natural Person’ 
C 
Required if 
Relationship Type 
is Present and 
Owner is ‘Natural 
Person’. 
 
Required if 
Relationship Type 
is 'Annuitant' 

---

## Page 7

Processing Rules For [[Broker]] Dealer Of Record Change: B2B Client Transmission 
Processing Rules 7 [[DTCC]] Public (White) 
[[Broker]] Dealer of Record Max 
Length 
Custodial to 
Custodial and 
Non-Custodial 
to Custodial 
Non-Custodial 
to Non-
Custodial 
Custodial to 
Non-Custodial 
Non-Qualified 
(Non-Custodial 
to Non-
Custodial) 
Last Name 
 
Party.Person.LastName 
30 
C 
Required for 
Annuitant 
C 
Required for each 
Relation Role 
Owner – R 
Annuitant –R 
Beneficiary– C 
Required when 
‘Natural Person’ 
C 
Required if 
Relationship Type 
is Present and 
Owner is ‘Natural 
Person’. 
 
Required if 
Relationship Type 
is 'Annuitant' 
Entity Name 
 
Party.Organization.FullName 
105 
C 
Required for 
Owner and 
Beneficiary (both 
should be the 
same value) 
Not used Beneficiary– C 
Required when 
‘Non-Natural’ 
(Trust) 
C 
Required if 
Relationship Type 
is Present and 
Owner is a ‘Non-
Natural’ 
 
 
Tax [[ID]] Qualifier 
 
* SSN (1) 
* TIN (2) 
 
Party.GovtIDInfo.GovtIDTC 
 
 3 
R 
Required for each 
Relation Role 
R 
Required for each 
Relation Role 
R 
Required for each 
Relation Role 
R 
Required for each 
Relation Role 
Tax [[ID]] 
 
Party.GovtIDInfo.GovtID 
 
 9 
R R 
 
R R 
Beneficiary  
Date of Birth 
 
Party.Person.BirthDate 
 
 8 
Not used Not used O 
 
Populate when 
Beneficiary is 
‘Natural Person’ 
 
Format: 
yyyy-mm-dd 
Not used 
Beneficiary  
Allocation Pct. 
 
(whole numbers only) 
 
Relation.InterestPercent 
3 
Set to 100 Not used R 
Mutually 
Exclusive with 
Distribution 
[[Option]] – Enter for 
all Beneficiaries 
with same role 
(Primary vs. 
Contingent) 
Not used 

---

## Page 8

Processing Rules For [[Broker]] Dealer Of Record Change: B2B Client Transmission 
Processing Rules 8 [[DTCC]] Public (White) 
[[Broker]] Dealer of Record Max 
Length 
Custodial to 
Custodial and 
Non-Custodial 
to Custodial 
Non-Custodial 
to Non-
Custodial 
Custodial to 
Non-Custodial 
Non-Qualified 
(Non-Custodial 
to Non-
Custodial) 
Beneficiary Distribution 
[[Option]] 
 
Equal (1) 
 
Relation.DistributionOption 
 
  
Not used Not used R 
Mutually 
Exclusive with 
Beneficiary 
Allocation Pct. – 
Enter for all 
Beneficiaries with 
same role 
(Primary vs 
Contingent) 
Not used 
Is the Beneficiary 
Irrevocable? 
 
* Yes (1) 
* No (0) 
 
Relation.IrrevokableInd 
 
 3 
Not used Not used R 
Required for all 
Beneficiaries 
Not used 
Address Type 
 
* Business (2) 
* Residence (1) 
* General Mailing (17) 
 
Party.Address.AddressTypeCode 
 
 20 
C 
Required when 
relationship is 
Owner 
Not used C 
Required for 
Owner, Optional 
for Beneficiary 
Not used 
Street Address - Line 1 
 
Parry.Address.Line1 
 
 35 
C 
Required when 
relationship is 
Owner 
Not used C 
Required for 
Owner, Optional 
for Beneficiary 
Not used 
Street Address - Line 2 
 
Party.Address.Line2 
 
 35 
O Not used O Not used 
City 
 
Party.Address.City 
 
 30 
C 
Required when 
relationship is 
Owner 
Not used C 
Required for 
Owner, Optional 
for Beneficiary 
Not used 
State 
 
Party.Address.AddressStateTC 
30 
C 
Required when 
relationship is 
Owner 
Not used C 
Required for 
Owner, Optional 
for Beneficiary 
 
(See special rules 
for non-US 
States) 
Not used 

---

## Page 9

Processing Rules For [[Broker]] Dealer Of Record Change: B2B Client Transmission 
Processing Rules 9 [[DTCC]] Public (White) 
[[Broker]] Dealer of Record Max 
Length 
Custodial to 
Custodial and 
Non-Custodial 
to Custodial 
Non-Custodial 
to Non-
Custodial 
Custodial to 
Non-Custodial 
Non-Qualified 
(Non-Custodial 
to Non-
Custodial) 
Zip Code 
 
Party.Address.Zip 
5 
numeric 
(cty = 
US) 
 
15 
alphanu
meric 
(cty = 
non-US) 
C 
Required when 
relationship is 
Owner 
Not used C 
Required for 
Owner, Optional 
for Beneficiary 
Not used 
Country 
 
Party.Address.AddressCountryTC 
15 
C 
Required when 
relationship is 
Owner 
Not used C 
Required for 
Owner, Optional 
for 
Beneficiary 
 
(See special rules 
for non-US 
Country) 
Not used 
Agent Relationship Type 
 
* Primary Agent (37) 
* Servicing Agent (38) 
*  Agent (11) 
 
Relation.RelationRoleCode 
 
 30 
R 
(1, 20 occurrence) 
R 
(1, 20 occurrence) 
R 
(1, 20 occurrence) 
R 
(1, 20 occurrence) 
First Name 
 
Party.Person.FirstName 
 
 25 
R R R R 
Last Name 
 
Party.Person.LastName 
 
 35 
R R R R 
 
Agent 
Tax [[ID]] Qualifier 
 
* SSN (1) 
 
Party.GovtIDInfo.GovtIDTC 
 
 3 
R R R R 
Agent  
Tax [[ID]] 
 
Party.GovtIDInfo.GovtID 
 
 9 
R R R R 

---

## Page 10

Processing Rules For [[Broker]] Dealer Of Record Change: B2B Client Transmission 
Processing Rules 10 [[DTCC]] Public (White) 
[[Broker]] Dealer of Record Max 
Length 
Custodial to 
Custodial and 
Non-Custodial 
to Custodial 
Non-Custodial 
to Non-
Custodial 
Custodial to 
Non-Custodial 
Non-Qualified 
(Non-Custodial 
to Non-
Custodial) 
Agent Allocation Percent 
 
(whole numbers only) 
 
Relation.InterestPercent 
 
 3 
R R R R 
Agent  (CRD) Central 
Registration Number 
 
Party.Producer.CRDNumber 
 
10 
C 
Mutually 
Exclusive with 
NPN Number- 
Required to enter 
CRD Number 
and/or NPN 
Number. 
C 
Mutually 
Exclusive with 
NPN Number- 
Required to enter 
CRD Number 
and/or NPN 
Number. 
C 
Mutually 
Exclusive with 
NPN Number- 
Required to enter 
CRD Number 
and/or NPN 
Number. 
C 
Mutually 
Exclusive with 
NPN Number- 
Required to enter 
CRD Number 
and/or NPN 
Number. 
Agent (NPN) National 
Producer Number 
 
Party.Producer.NIPRNumber 
 
10 
C 
Mutually 
Exclusive with 
CRD Number- 
Required to enter 
NPN Number 
and/or CRD 
Number. 
C 
Mutually 
Exclusive with 
CRD Number- 
Required to enter 
NPN Number 
and/or CRD 
Number. 
C 
Mutually 
Exclusive with 
CRD Number- 
Required to enter 
NPN Number 
and/or CRD 
Number. 
C 
Mutually 
Exclusive with 
CRD Number- 
Required to enter 
NPN Number 
and/or CRD 
Number. 
Agent Team [[ID]] 
 
Grouping.FullName 
 
 20 
O O O O 
Carrier Assigned Agent [[ID]] 
 
Party.Producer.CarrierAppointmen
t.CompanyProducerID 
 20 
O O O O 
Distributor Assigned Agent 
[[ID]] 
 
Party.Producer.ProducerAgreeme
nt.OLifeExtension.FirmAssignedPr
oducerID 
 20 
O O O O 
Form  Name 
 
FormInstance.FormName 
 
 30 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
Attachment Type 
 
Document (1) 
Form (5) 
 
FormInstance.Attachment.Attachm
entType 
 
 1 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 

---

## Page 11

Processing Rules For [[Broker]] Dealer Of Record Change: B2B Client Transmission 
Processing Rules 11 [[DTCC]] Public (White) 
[[Broker]] Dealer of Record Max 
Length 
Custodial to 
Custodial and 
Non-Custodial 
to Custodial 
Non-Custodial 
to Non-
Custodial 
Custodial to 
Non-Custodial 
Non-Qualified 
(Non-Custodial 
to Non-
Custodial) 
Mime Type 
 
PDF (17) 
TIFF (11) 
 
FormInstance.Attachment.MimeTy
peTC 
 
 2 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
Attachment 
 
FormInstance.Attachment.Attachm
entHashValue 
  
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
C 
Required when 
your Carrier 
partner requires 
your 
documentation 
Required Change Type(s) 
 
1004900077 
67 
66 
74 
27 
30 
 
1004900077 
27 
 
1004900077 
67 
66 
74 
27 
30 
 
 
1004900077 
27 
 
 

---

## Page 12

Processing Rules For [[Broker]] Dealer Of Record Change: B2B Client Transmission 
Best Practice 12 [[DTCC]] Public (White) 
BEST PRACTICE 
BIN: if [[Broker]] does not have a BIN number at time of data entry, enter zero “0” as the BIN. Carrier will use that 
value as the new BIN number at the receiving [[Broker]] until further notice.      
GENERAL  
• Each TXLife 113 request message will contain a single contract. 
• Partial SSN are not acceptable. Full SSN (no hyphens)  is to be used with element <GovtID>  
Note:  
For Agents identification, [[DTCC]] is working toward removing SSN and applying CRD and/or NPN Number which is currently 
available for data entry. 
• Product Code, Carrier Code, [[CUSIP]] Number are not supported in this message for Change of Financial 
Institution.  
• Based on the transfer type, certain rules and validations will apply. 
AGENT Information 
• Only 1 Primary Agent is allowed per transaction 
o All transactions must have at least the Primary Agent      
• Maximum of 20 Agents are allowed per transaction     
• Each Agent Tax [[ID]] must be unique      
• Agent Allocation Percent must sum to 100% 
• Agent Allocation Percent must be whole number (eg: 0 = 0%, 5 = 5%, 10 = 10%, 100 = 100%)  
• Only one Team [[ID]] is allowed per TXLife 113 transaction. All Agents identified on the transaction with a 
Team [[ID]], will be on the same Team. 
• Required to enter a CRD Number and/or NPN Number for all Agents. 
Non-Custodial to Non-Custodial Rules 
RELATIONSHIP Information  
• Owner is Required and Annuitant is Optional 
• Owner and Annuitant are to be allowed one occurrence each per transaction  

---

## Page 13

Processing Rules For [[Broker]] Dealer Of Record Change: B2B Client Transmission 
Best Practice 13 [[DTCC]] Public (White) 
Non-Custodial or Custodial to Custodial Rules 
RELATIONSHIP Information  
• Owner and Annuitant are Required   
• Only 1 Owner and Annuitant are allowed per transaction  
• Address Information is required for Relationship Type = 'Owner'   
• Complete the 'Beneficiary' Relationship Type information based on the 'Owner' information entered:  
o Set Owner's to Entity Name to Beneficiary Entity Name  
o Set Owner's to Tax [[ID]] Qualifier and Tax [[ID]] to Beneficiary Tax [[ID]] Qualifier and Beneficiary Tax [[ID]] 
o Set Beneficiary Allocation Percent = 100  
o Beneficiary Allocation Percent must be whole number (eg: 100 = 100%)  
Custodial to Non-Custodial Rules 
RELATIONSHIP Information          
• Owner, Annuitant and Beneficiary are Required      
• Only 1 Owner, 1 Annuitant and maximum 8 Beneficiaries are allowed per transaction 
• Beneficiary relationship can be either Natural (Person) or Non-Natural Entity    
• At least 1 Beneficiary must be the Primary Beneficiary       
• If more than 1 Beneficiary is entered, they can be any combination of Beneficiary (ie: Primary or 
Contingent) 
• If Primary or Contingent Beneficiary’s Date of Birth is entered, the date must not be a future date from the 
current date.          
• Total of Beneficiary Allocation Percent must = 100 (per Primary and/or Contingent Beneficiary) 
• Beneficiary Allocation Percent must be whole number (eg: 0 = 0%, 5 = 5%, 10 = 10%, 100 = 100%)  
• Distribution [[Option]] of ‘equal distribution’ (value 1) among beneficiaries is available for either Primary 
and/or Contingent beneficiaries. 
Note:  
Beneficiary Allocation amounts or Distribution [[Option]] are mutually exclusive. Therefore, both options cannot be combined 
with any one beneficiary type (Primary or Contingent) per transaction.    
• Address Information is required for Relationship Type = 'Owner'      
• Address Information is optional for Relationship Type = 'Beneficiary' 
• If Address Information for Country = US: 
o Use the ACORD State code.  
o Use ‘US’ Country represented with ACORD Country (value 1) 
• If Address Information for Country is non-US: 
o Transmit to carrier the ACORD code value of '1000' to represent State and '2147483647' to represent 
Country. 

---

## Page 14

Processing Rules For [[Broker]] Dealer Of Record Change: B2B Client Transmission 
Best Practice 14 [[DTCC]] Public (White) 
o If Non-US addresses are entered, all address information text (including State and Country) will be 
transmitted verbatim to carrier.            
Non-Qualified Rules 
RELATIONSHIP Information  
• Owner is Required, Annuitant is Optional 
• If more than 1 Owner, they should all be assigned as 'Joint Owner'  
• Owner relationship can be either Natural (Person) or Non-Natural Entity  
• Maximum number of total Relationships (counting both Owner and Annuitant) are 10 per transaction  
• Only Natural (Person) Owners can have more than 1 Owner relationship  
• If an 'Annuitant' or 'Joint Annuitant' is to be entered, max of 2 Annuitants should be entered per 
transaction. 
• If more than 1 Annuitant, they should both be assigned as 'Joint Annuitant' 
 
 
 

---

## Page 15

 
 [[DTCC]] Public (White) 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 