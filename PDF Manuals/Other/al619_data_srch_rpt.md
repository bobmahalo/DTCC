---
title: "ALERT Data Search Reports"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/al619_data_srch_rpt.pdf"
pages: 33
size: "694.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ALERT Data Search Reports

**Original File:** [al619_data_srch_rpt.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/al619_data_srch_rpt.pdf)  
**Category:** Other  
**Total Pages:** 33  
**File Size:** 694.6 KB  

---

## Page 1

ALERT®
DATASEARCHREPORTS
MARCH16,2022


---

## Page 2

©2022DTCC.Allrightsreserved.[[DTCC]],[[DTCC]](Stylized),ADVANCINGFINANCIALMARKETS.
TOGETHER,andtheInterlockergraphicareregisteredandunregisteredtrademarksofTheDepository
Trust&ClearingCorporation.
Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandnamebycertainaffiliatesofThe
DepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitselfdoesnotprovidesuchservices.Eachof
theseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsoftheparticularcountryor
countriesinwhichsuchentityoperates.Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,its
affiliatesandtheservicestheyoffer.
DocInfo:March16,2022
PublicationCode:AL619
Service:ALERT
Title:DataSearchReports

---

## Page 3

TABLEOFCONTENTS
Preface 4
RelatedDocumentsandTraining 4
Questions? 4
Introduction 5
DataSearchFileTypes 6
Account/ModelSettlementInstructionDataSearch 7
GeneralAccountsDataSearch 19
BrokerInternalAccountDataSearch 24
ConfirmDeliveryDataSearch 26

---

## Page 4

PREFACE
RelatedDocumentsandTraining
Forrelateddocumentsandvideos,andalldocumentsreferencedinthisdocument,gototheInstitutionalTradeProcessing-
ALERTLearningCenter.
Questions?
TheDTCCClientCenterprovidesgeneralassistanceandtechnicalhelp.Visitwww.[[DTCC]].com/client-centerto:
l Enteraservicerequestorcheck
l Searchtheknowledgebase
l Obtaincontactinformation

---

## Page 5

INTRODUCTION
DataSearchisthereplacementforthelegacyDARTreporttoolandthefilescreatedbythistool.Clientswhopreviouslycodedto
theDARTformatmustupdatetheirsystemstoacceptthenewDataSearchformats.
Onrequest,DTCCstaffcanruntheALERT®platformDataSearchreportstocreatecomprehensivedatafilesthatinclude
informationbelongingtoclientsortheircounterparties.Thereisafeeforthisservice.
Datasearchfiletypesinclude:
l Accountandmodelsettlementinstructions
l Generalaccounts
l Brokerinternalaccountnumbers(BIAs)
l Confirmdeliveryfiles
ThisdocumentdescribesthecontentsoftheDataSearchfiles,theirformat,andhowthefieldsmaptothelegacyDARTfields.

---

## Page 6

DATASEARCHFILETYPES
DataSearchfilesfromtheALERTplatformareinoneofthefollowingformats:
l .csv(commaseparatedvalues)
l .xls(MicrosoftExcel)
Eachfilehasaheaderrowwithstandardcolumnnames.
DataType Format BrokerDirectMessage*
AccountSettlementInstructions .csv 48
ModelSettlementInstructions .csv 47
GeneralAccounts .csv 3B
BrokerInternalAccount(BIA) .xls 5A
ConfirmDelivery .csv A1
Table1 DataSearchFileTypes
*TheBrokerDirectMessagenumberisprovidedforreference.DataSearchdoesnotusetheBrokerDirectmessageformatto
retrievedata.

---

## Page 7

ACCOUNT/MODELSETTLEMENTINSTRUCTIONDATASEARCH
TheAccount/ModelSettlementInstruction(ASI/MSI)DataSearchreturnssettlementinstructions(SSI)dataforbroker-orbank-
owneddata,oraccountSSIsforcounterparties.
Table2liststhefieldsavailableinanASI/MSIDataSearchreport.
HeaderField Length Notes
RefID 36 ReferenceIDforALERTplatformSSIs.
Status 10 Typicallyblank;usedforALERTplatform
uploads.
Action 1 Typicallyblank;usedforALERTplatform
uploads.
Acronym 8
AccessCode 12
ModelOwner 8 PopulatedformodelSSIsonly.
ModelName 12 PopulatedformodelSSIsonly.
SellSideLEIdentifier 20 [[Broker]]/dealer's20-characteralphanumericLegal
EntityIdentifier.
Country 2 ISOcountrycode
Security 3 3-charactercode
MethodType 11 COLL=[[collateral]]
Purpose 35 ANY,INITIAL,orVARIATION
MarginType 35 ANY,DELIVER,orRECEIVE
MarginDirection 35 ANY,CALL,orRECALL
MarginIndicator 35
Table2 ASI/MSIDataSearchReportFileHeaders

---

## Page 8

HeaderField Length Notes
ID1 35
ID2 35
ID3 35
ID4 35
ID5 35
AgentID 8
InstitutionID 8
ParticipantName1 35
ParticipantName2 35
A/CRef1 35
A/CRef2 35
A/C#atGlobalCustodian 35
SubA/CRef1 35
SubA/CRef2 35
A/C#atLocalAgent 35
CashA/CNumber 35
PaymentCurrency 3 ISOcurrencycode
AlternateCurrency 3 ISOcurrencycode
AlternateCashA/CNumber 35
CustodianName1 35

---

## Page 9

HeaderField Length Notes
CustodianName2 35
CustodianBIC 11 8-digitBICshaveXXXappended.
CustodianAddress1 35
CustodianAddress2 35
CustodianCity 35
CustodianState/Province 35
CustodianCountry 2 ISOcurrencycode
CustodianPostCode 15
SubAgentName1 35
SubAgentName2 35
SubAgentBIC 11 8-digitBICshaveXXXappended.
SubAgentAddress1 35
SubAgentAddress2 35
SubAgentCity 35
SubAgentState/Province 35
SubAgentCountry 2 ISOcurrencycode
SubAgentPostCode 15
CorrespName1 35
CorrespName2 35
CorrespBIC 11 8-digitBICshaveXXXappended.

---

## Page 10

HeaderField Length Notes
CorrespAddress1 35
CorrespAddress2 35
CorrespCity 35
CorrespState/Province 35
CorrespCountry 2 ISOcurrencycode
CorrespPostCode 15
CorrespCashA/CNumber 35
CorresSecA/CNumber 35
Relationship 1 C=Correspondent,S=SubAgent
RegName1 140
PSET 11or2
RegAddress1 35
RegAddress2 35
RegBIC 11 8-digitBICshaveXXXappended.
RegCity 35
RegState/Province 35
RegCountry 2 ISOcurrencycode
RegPostalCode 15
SettlementContact 35
SettlementPhone 20

---

## Page 11

HeaderField Length Notes
SpecialInstr1 35
SpecialInstr2 35
InstitutionName 35
InstitutionBIC 11 8-digitBICshaveXXXappended.
InstitutionContact 35
InstitutionPhone 20
I/P1ID 8
I/P1BIC 11 8-digitBICshaveXXXappended.
I/P1A/CNumber 25
I/P1Name 35
I/P1Contact 35
I/P1Phone 20
I/P1SpecialInstr1 35
I/P1SpecialInstr2 35
I/P2ID 8
I/P2BIC 11 8-digitBICshaveXXXappended.
I/P2A/CNumber 25
I/P2Name 35
I/P2Contact 35
I/P2Phone 20

---

## Page 12

HeaderField Length Notes
I/P2SpecialInstr1 35
I/P2SpecialInstr2 35
I/P3ID 8
I/P3BIC 11 8-digitBICshaveXXXappended.
I/P3A/CNumber 25
I/P3Name 35
I/P3Contact 35
I/P3Phone 20
I/P3SpecialInstr1 35
I/P3SpecialInstr2 35
ReceivingAgentBIC 11 8-digitBICshaveXXXappended.

---

## Page 13

Table3liststhedifferencesbetweenthenewreportfieldsandthelegacyDARTreportfields.
LegacyField NewReportField
RefID
Status
Action
MessageType
ErrorCode
ModelOwner
ModelName
Acronym Acronym
AccessCode AccessCode
Country Country
Security Security
Priority
Method MethodType
Rev_Date
Eff_Date
StoredVersion
ID_1 ID1
ID_2 ID2
ID_3 ID3
Table3 ASI/MSIMaptoLegacyDARTReportFields

---

## Page 14

LegacyField NewReportField
ID_4 ID4
ID_5 ID5
AgentID
InstitutionID
Participant_Name_1 ParticipantName1
Participant_Name_2 ParticipantName2
AC_Ref_1 A/CRef1
AC_Ref_2 A/CRef2
Security_AC_No A/C#atGlobalCustodian
Sub_AC_Ref_1 SubA/CRef1
Sub_AC_Ref_2 SubA/CRef2
Sub_AC_No A/C#atLocalAgent
Cash_AC_No CashA/CNumber
Payment_Currency PaymentCurrency
Alternate_Currency AlternateCurrency
Alternate_Cash_AC_No AlternateCashA/CNumber
Custodian_Name_1 CustodianName1
Custodian_Name_2 CustodianName2
Custodian_BIC CustodianBIC
Custodian_Address_1 CustodianAddress1

---

## Page 15

LegacyField NewReportField
Custodian_Address_2 CustodianAddress2
Custodian_City CustodianCity
Custodian_Locality CustodianState/Province
Custodian_Country CustodianCountry
Custodian_Post_Code CustodianPostCode
Sub_Agent_Name_1 SubAgentName1
Sub_Agent_Name_2 SubAgentName2
Sub_Agent_BIC SubAgentBIC
Sub_Agent_Address_1 SubAgentAddress1
Sub_Agent_Address_2 SubAgentAddress2
Sub_Agent_City SubAgentCity
Sub_Agent_Locality SubAgentState/Province
Sub_Agent_Country SubAgentCountry
Sub_Agent_Post_Code SubAgentPostCode
Corresp_Name_1 CorrespName1
Corresp_Name_2 CorrespName2
Corresp_BIC CorrespBIC
Corresp_Address_1 CorrespAddress1
Corresp_Address_2 CorrespAddress2
Corresp_City CorrespCity

---

## Page 16

LegacyField NewReportField
Corresp_Locality CorrespState/Province
Corresp_Country CorrespCountry
Corresp_Post_Code CorrespPostCode
Corresp_Cash_AC_No CorrespCashA/CNumber
Corresp_Sec_AC_No CorresSecA/CNumber
Reg_BIC
Relationship Relationship
Reg_Name_1 RegName1
PSET PSET
Reg_Address_1 RegAddress1
Reg_Address_2 RegAddress2
RegBIC
Reg_City RegCity
Reg_Locality RegState/Province
Reg_Country RegCountry
Reg_Post_Code RegPostalCode
Settlement_Contact SettlementContact
Settlement_Phone SettlementPhone
Institution_Name InstitutionName
Special_Instr_1 SpecialInstr1

---

## Page 17

LegacyField NewReportField
Special_Instr_2 SpecialInstr2
Institution_BIC InstitutionBIC
Institution_Contact InstitutionContact
Institution_Phone InstitutionPhone
IP_1_ID I/P1ID
IP_1_BIC I/P1BIC
IP_1_AC_No I/P1A/CNumber
IP_1_Name I/P1Name
IP_1_Contact I/P1Contact
IP_1_Phone I/P1Phone
IP_1_Special_Instr_1 I/P1SpecialInstr1
IP_1_Special_Instr_2 I/P1SpecialInstr2
IP_2_ID I/P2ID
IP_2_BIC I/P2BIC
IP_2_AC_No I/P2A/CNumber
IP_2_Name I/P2Name
IP_2_Contact I/P2Contact
IP_2_Phone I/P2Phone
IP_2_Special_Instr_1 I/P2SpecialInstr1
IP_2_Special_Instr_2 I/P2SpecialInstr2

---

## Page 18

LegacyField NewReportField
IP_3_ID I/P3ID
IP_3_BIC I/P3BIC
IP_3_AC_No I/P3A/CNumber
IP_3_Name I/P3Name
IP_3_Contact I/P3Contact
IP_3_Phone I/P3Phone
IP_3_Special_Instr_1 I/P3SpecialInstr1
IP_3_Special_Instr_2 I/P3SpecialInstr2
ReceivingAgentBIC

---

## Page 19

GENERALACCOUNTSDATASEARCH
TheGeneralAccountsDataSearchreturnsaccountinformationownedbyoraccessibletotheclientascounterpartydata.
Table4liststhefieldsavailableinaGeneralAccountDataSearchreport.
HeaderField Length Notes
RefID 36 ReferenceIDforALERTplatformgeneral
account.
Status 10 Typicallyblank;usedforALERTPlatforms'
webinterfaceupload.
Action 1 Typicallyblank;usedforALERTPlatforms'
webinterfaceupload.
Acronym 8
AccessCode 12
OmniAccessCode 12
FundISIN 12
BuySideLEIdentifier 20 Investmentmanager’s20-character
alphanumericLegalEntityIdentifier
AccountName 55
AccountName2 55
ShortName 50
AccountType 55
AffirmingParty 55
TaxID/SSIndicator 3
Table4 GeneralAccountsDataSearchReportHeaders

---

## Page 20

HeaderField Length Notes
TaxID/SSValue 30
TaxIDExpirationDate 10 MM/DD/YYYY
CharityA/CRef 30
Withholding 1 Y/N
TaxExempt 1 Y/N
CountryOfOrigin 2
FundType 55
InvestmentAdvisor 1 Y/N
InstitutionName 70
InstitutionContact 35
InstitutionPhone 20
InstitutionBIC 11
AccessCodeLEIdentifier 55
LargeTraderID 55

---

## Page 21

Table5liststhedifferencesbetweenthenewreportfieldsandthelegacyDARTreportfields.
Legacyfields NewReportFields
RefID
Status
Action
MessageType
ErrorCode
Acronym Acronym
AccessCode AccessCode
Rev_Date
Eff_Date
ModelOwner
ModelName
Keep-asindicator
StoredVersion
OmniAccessCode
FundISIN
BuySideLEIdentifier
AccountName_1 AccountName
AccountName_2 AccountName2
ShortName ShortName
Table5 GeneralAccountsMaptoLegacyDARTReport

---

## Page 22

Legacyfields NewReportFields
Memo
TaxID TaxID/SSValue
TaxID/SSIndicator
TaxIDExpirationDate
USTaxWithheld Withholding
CountryofOrigin CountryOfOrigin
TypeofAccount AccountType
ClientofIA InvestmentAdvisor
RegistrationName
InstitutionName InstitutionName
ContactName InstitutionContact
ContactPhone InstitutionPhone
InstitutionBIC InstitutionBIC
SettlementModel
AffirmingParty AffirmingParty
AccountType FundType
USTaxID
SuppressBroker
Statement
MailBrokerConfirm
MailOriginalConfirm

---

## Page 23

Legacyfields NewReportFields
SendMonthlyStatement
TaxExempt TaxExempt
CharityAcct.Ref CharityA/CRef
AccessCodeLEIdentifier
LargeTraderID

---

## Page 24

BROKERINTERNALACCOUNTDATASEARCH
Thebrokerinternalaccount(BIA)DataSearchreturnsbrokerinternalaccountnumbersmappedtoacronyms,accesscodes,
countries,andsecuritytypes.
Table6liststhefieldsavailableinaBIADataSearchreport.
HeaderField Length Notes
RefID 36 ReferenceIDforALERTplatformBIA.
Status 10 Typicallyblank;usedforALERTPlatform'swebinterfaceupload.
Action 1 Typicallyblank;usedforALERTPlatform'swebinterfaceupload.
BDAcronym 8
IMAcronym 8
AccessCode 12
BIA# 20
Country 2 ISOcountrycode
Security 3 3-charactercode
Table6 BIADataSearchReportFileHeaders
Table7liststhedifferencesbetweenthenewreportfieldsandthelegacyDARTreportfields.
LegacyFields NewReportFields
RefID
Status
Action
Datainformation
Table7 BIAMaptoLegacyDARTReport

---

## Page 25

LegacyFields NewReportFields
MessageType
ErrorFieldcode
BDAcronym
Acronym IMAcronym
AccessCode AccessCode
Account_name_1
Account_name_2
Country_1 Country
Security_1 Security
BIA_1 BIA#
Country_2
Security_2
BIA_2

---

## Page 26

CONFIRMDELIVERYDATASEARCH
TheConfirmDeliveryDataSearchprovidesconfirminformationforclientaccountstowhichabrokerhasbeengrantedaccess.
Table8liststhefieldsavailableinaConfirmDeliveryDataSearchreport.
HeaderField Length Notes
RefID 36 ReferenceIDforALERTplatformconfirm.
Status 10 Typicallyblank;usedforALERTPlatform'sweb
interfaceupload.
Action 1 Typicallyblank;usedforALERTPlatform'sweb
interfaceupload.
Acronym 8
AccessCode 12
ConfirmNumber 1 1-8
MailName1 35
MailName2 35
MailAddress1 35
MailAddress2 35
MailCity 35
MailLocality 35
MailPostCode 15
MailCountry 2 ISOcountrycode
Attention1 35
Attention2 35
Table8 ConfirmDeliveryDataSearchReportFileHeaders

---

## Page 27

HeaderField Length Notes
Attention3 35
SendDuplicateConfirm 1 Y/N
SendOriginalConfirm 1 Y/N
SendStatement 1 Y/N
ConfirmByPhone 1 A-E
ConfirmByEmail 1 A-E
ConfirmByETC 1 A-E
ConfirmByFax 1 A-E
ConfirmByMail 1 A-E
ConfirmRecipientCode 2 SeetheConfirmRecipientCodestable{/color}.
ConfirmRecipientCategory 30 SeetheConfirmRecipientCodestable{/color}.
ConfirmByMailCount 2 1-10
ConfirmTelephone1 20
ConfirmTelephone2 20
ConfirmFax1 20
ConfirmFax2 20
ConfirmBICCode 11
ConfirmEmailAddress 35
OasysAcronym 8
OasysAccessCode 12
ConfirmETCCode 20

---

## Page 28

Table9liststhedifferencesbetweenthenewreportfieldsandthelegacyDARTreportfields.
LegacyField NewReportField
RefID
Status
Action
MessageType
ErrorCode
Acronym Acronym
AccessCode AccessCode
Conf_ID ConfirmNumber
Rev_Date
Eff_Date
StoredVersion
Name_1 MailName1
Name_2 MailName2
Address_1 MailAddress1
Address_2 MailAddress2
City MailCity
Locality MailLocality
PostalCode MailPostCode
Table9 ConfirmDeliveryMaptoLegacyDARTReport

---

## Page 29

LegacyField NewReportField
Country MailCountry
Attention1 Attention1
Attention2 Attention2
Attention3 Attention3
SendDuplicateConfirm SendDuplicateConfirm
SendOriginalConfirm SendOriginalConfirm
SendStatement SendStatement
Phone ConfirmByPhone
E-mail ConfirmByEmail
ETC ConfirmByETC
FAX ConfirmByFax
TELEX
Mail ConfirmByMail
ConfirmRecipientCode
Recipient ConfirmRecipientCategory
Nbr.ofMailedCopies ConfirmByMailCount
PhoneNbr.1 ConfirmTelephone1
PhoneNbr.2 ConfirmTelephone2
FAXNbr.1 ConfirmFax1
FAXNbr.2 ConfirmFax2
TELEXNbr.1

---

## Page 30

LegacyField NewReportField
TELEXNbr.2
BIC ConfirmBICCode
E-mailAddress ConfirmEmailAddress
OASYSAcronym OasysAcronym
OASYSAccessCode OasysAccessCode
OtherETCCode ConfirmETCCode
SpecInstr_1
SpecInstr_2
SpecInstr_3
SpecInstr_4
SpecInstr_5
SpecInstr_6
SpecInstr_7
SpecInstr_8

---

## Page 31

Table10mapstheconfirmrecipientcodestotheconfirmrecipientcategories.
ConfirmRecipientCode ConfirmRecipientCategory
H Customer
I ExecutingBroker/Dealer
J ClearingBroker/Dealer
K GlobalCustodian
L SubCustodian
M InterestedParty
N Other
O InvestmentManager
P I/M-Domestic
Q I/M-International
R I/M-[[Equity]]
S I/M-DomesticEquity
T I/M-DomesticBond
U I/M-InternationalEquity
V I/M-InternationalBond
W I/M-GovernmentBond
X I/M-InternationalandGovernmentBond
Y I/M-Europe
Z I/M-EuropeandUK
Table10ConfirmRecipientCodes

---

## Page 32

ConfirmRecipientCode ConfirmRecipientCategory
AA I/M-FarEast
AB I/M-PacificRim
AC I/M-NorthAmerica
AD I/M-LatinAmerica
AE I/M-EmergingMarket
AF I/M-Japan
AG BeneficialOwner

---

## Page 33

FORMOREInformation
EmailDTCCLearningat:
DTCCLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com