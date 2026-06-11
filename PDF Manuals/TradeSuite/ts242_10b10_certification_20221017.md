---
title: "Guide for 10b-10 Certification"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ts242_10b10_certification_20221017.pdf"
pages: 32
size: "1297.1 KB"
category: "TradeSuite"
ingested_on: "2026-06-05"
---

# Guide for 10b-10 Certification

**Original File:** [ts242_10b10_certification_20221017.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ts242_10b10_certification_20221017.pdf)  
**Category:** TradeSuite  
**Total Pages:** 32  
**File Size:** 1297.1 KB  

---

## Page 1

TRADESUITEID®
GUIDEFOR10B-10CERTIFICATION
VERSION8.05
MONDAY,OCTOBER17,2022


---

## Page 2

©2022. Allrightsreserved.[[DTCC]],[[DTCC]](Stylized),ADVANCINGFINANCIALMARKETS.
TOGETHER,andtheInterlockergraphicareregisteredandunregisteredtrademarksofTheDepository
Trust&ClearingCorporation.
Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandnamebycertainaffiliatesofThe
DepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitselfdoesnotprovidesuchservices.Eachof
theseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsoftheparticularcountryor
countriesinwhichsuchentityoperates.Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,its
affiliatesandtheservicestheyoffer.
Disclaimer:Theinformationinthisdocumentisnotintendedaslegalguidance.Clientsareresponsible
fortheirowncertificationandforconsultingtheirownlegalcounselaboutcertificationwithSECRule10b-
10.

---

## Page 3

CONTENTS
Contents 3
1.Preface 4
Audience 4
ChangesinthisVersion 4
RelatedDocumentsandTraining 6
Questions? 6
2.Introductionto10b-10CertificationFields 7
AssetClassConfirmRecordMatrix 7
3.TradeInputandTradeSubmission 8
Record1 8
Record2 11
Record4 12
Record5 13
Record6 15
4.TradeOutputandTradeReceiving 17
Record1 17
Record2 20
Record4 24
Record5 26
Record6 27
A.SecurityTypesinEachAssetClassCategory 29

---

## Page 4

Preface 4
1.PREFACE
Thisdocumentliststhefields,includingthemachine-readable10b-10fields,thatclientsmustsendand
receivetocomplywiththeTradeSuiteID®service.
Audience
ThisdocumentisforthefollowingTradeSuiteIDserviceclients:
l Agents
l Brokers/dealers
l [[Institutions]]
l Interestedparties
l Primebrokers
ChangesinthisVersion
TradeSuiteID8.05(newchanges)
TheSecuritiesandExchangeCommission([[SEC]])approvedamendmentstoFINRARule2232(Customer
Confirmations)thatrequirememberfirmstodiscloseadditionaltransaction-relatedinformationtoretail
customersfortradesincertainfixedincomesecurities.Specifically,amendedRule2232requiresa
membertodisclosetheamountandpercentageofmark-upormark-downitappliestotradeswithretail
customersincorporateoragencydebtsecuritiesifthememberalsoexecutesanoffsettingprincipaltrade
inthesamesecurityonthesametradingday.Theamendedrulealsorequiresmemberstodisclosetwo
additionalitemsonallretailcustomerconfirmationsforcorporateandagencydebtsecuritytrades:(1)a
reference,andahyperlinkiftheconfirmationiselectronic,toawebpagehostedbyFINRAthatcontains
publiclyavailabletradingdataforthespecificsecuritythatwastraded,and(2)theexecutiontimeofthe
transaction,expressedtothesecond.TheMSRBRuleG-15andG-30hasalsochangedtoaccommodate
thesechanges.ThisnewregulationgoesintoeffectonMay14,2018.
Tocomplywiththeseregulatorychanges,DTCChasmadethefollowingadditionstorequiredcertification
fields.
ForTradeInputandTradeSubmission:
l Record2:
o FINRAMSRBEMMAURL
o SpecialInstructionsLine19,SpecialInstructionsLine20,SpecialInstructionsLine21
l Record5:
o TradeExecutionDate
o MarkUp/MarkDownPercentageSign
Guidefor10b-10Certification

---

## Page 5

Preface 5
o MarkUp/MarkDownPercentage
o BrokerLegalEntityIdentifier
o InstitutionLegalEntity
Guidefor10b-10Certification

---

## Page 6

Preface 6
ForTradeOutputandTradeReceiving:
l Record2:
o FINRAMSRBEMMAURL
o SpecialInstructionsLine19,SpecialInstructionsLine20,SpecialInstructionsLine21
l Record5:
o TradeExecutionDate
o MarkUp/MarkDownPercentageSign
o MarkUp/MarkDownPercentage
o BrokerLegalEntityIdentifier
o InstitutionLegalEntityIdentifier
TradeSuiteID8.0.4(previously communicatedchanges)
Tocomplywiththemarketsinfinancialinstrumentsdirective(MiFIDII)regulationsandallowforgreater
transparencyacrossthetradingprocess,theLocalTaxfieldisnowcalledResearchAmount.InRecord1
forbothtradeinputandtradeoutput,therecordfieldhaschangedfromLocalTaxtoResearchAmount.
SeetheinputRecord1andtheoutputRecord1.InadditiontotheMiFID IIinitiativechanges,the
appearanceandlayoutofthedocumentationhaschangedtoensureconsistencyacrossDTCC.
RelatedDocumentsandTraining
Forotherrelatedcontentandallreferencesinthisdocument,seeTradeSuiteIDontheDTCCLearning
Center.
Questions?
TheDTCC ClientCenterprovidesgeneralassistanceandtechnicalhelp.Visitwww.[[DTCC]].com/client-center
to:
l Enteraservicerequestorcheckthestatusofanexistingrequest
l Searchtheknowledgebase
l Obtaincontactinformation
Guidefor10b-10Certification

---

## Page 7

Introductionto10b-10CertificationFields 7
2.INTRODUCTIONTO10B-10CERTIFICATIONFIELDS
Thisguideprovidesthe10b-10certificationfields.The10b-10dedicatedfieldsareincludedinthedata
fields.ThepurposeofcertificationisforTradeSuiteIDserviceto:
l Maintaincounterpartycompatibilitywithitsusers.
l Ensurethatclientsarecompliantwithdatafields.
Disclaimer:Theinformationinthisdocumentisnotintendedaslegalguidance.Clientsareresponsible
fortheirowncertificationandforconsultingtheirownlegalcounselaboutcertificationwithSECRule10b-
10.
AssetClassConfirmRecordMatrix
Ataminimum,whenusingmachine-readableanddirectmessaging,youmustbeabletosubmitand
receivethespecifiedrecordsforcertification.Table2.1showstheTradeSuiteIDserviceconfirmrecords,
byassetclasscategory,thatarerequiredforprocessing.
Confirm
Record1
Confirm
Record2
Confirm
Record4
Confirm
Record5
Confirm
Record6
Equities X X
Fixedincome X X X
MBSsecurities X X X X
Financial/repo
[[securities]]
X X X X
Table2.1AssetClassConfirmRecords
Guidefor10b-10Certification

---

## Page 8

TradeInputandTradeSubmission 8
3.TRADEINPUTANDTRADESUBMISSION
Thissectionshowstherequiredcertificationfieldsfortradeinputandtradesubmissionof:
l Record1
l Record2
l Record4
l Record5
l Record6
Record1
Table3.1showstherequiredfieldsfortradeinputandtradesubmissionforrecord1.
RecordField 10b-10Field [[Equity]] FixedIncomeMBS FIN/Repo
TransactionType X X X X
ExecutingBrokerID X X X X
InstitutionIDNumber Y X X X X
AgentIDNumber X X X X
SecurityIdentifier Y X X X X
SettlementType X X X X
PrimeBrokerLong/ShortIndicator Y X X X X
Role1 Y X X X X
MarketCode X X X X
SideCode Y X X X X
NetPrice Y X X X X
[[shares]]/FaceValue Y X X X X
Price Y X X X X
PrincipalAmount X X X X
Table3.1TradeInputandTradeSubmission—Record1
1TocomplywithTradeSuiteIDservicecertificationandtheSECinterpretiveletterdatedNovember19,2010,
entertheRolefieldasadiscretefield,andthenpopulatethesamedatainoneoftheSpecialInstructionsfieldsin
Record1.ThereareeightSpecialInstructionsfieldswith32characterseachinRecord1,position359–614.For
moreinformation,seeTradeSuiteIDserviceConfirmTradeInputMessageSpecificationavailableinthe
TradeSuiteIDservice8.0sectionoftheInstitutionalTradeMatching-LearningCenter.
Guidefor10b-10Certification

---

## Page 9

TradeInputandTradeSubmission 9
RecordField 10b-10Field [[Equity]] FixedIncomeMBS FIN/Repo
Registration/Shipping/Section31Fees X X X X
Interest X X X X
ResearchAmount X X X X
CountryTax X X X X
Commission Y X X X X
OtherCharges X X X X
NetAmount X X X X
ExpandedSecurityType X X X X
BypassIndicator X X X X
SplitCurrencySettlementIndicator X X X X
QualitycontrolReportingExemptIndicator X X X X
AllocationSource X X X X
SettlementLocation X X X X
SecurityNumberingSystem X X X X
CurrencyCode X X X X
OriginalBrokerConfirmNumber X X X X
TradeDate Y X X X X
SettlementDate X X X X
SecurityDescriptionLine11 X X X X
AccountType Y X X X X
CancelCorrectionReasonCode X X X X
AgentInternalAccountNumber X X X X
[[Broker]]/DealerInternalAccountNumber X X X X
[[Broker]]/DealerConfirmNumber X X X X
SpecialInstructionsLines1through8 X X X X
SecurityFormCode X X X X
InterestedParty#1IDNumber X X X X
InterestedParty#1AccountNumber X X X X
Table3.1TradeInputandTradeSubmission—Record1
1TheTradeSuiteIDserviceserviceattemptstoobtainsecuritydescriptionsandfieldsfromJ.J.KennyforDTC-eli-
giblemunicipalsecurities.Includedaresecuritiesthesubmitteridentifiesasamunicipalsecurity(securitytype=
MUN).Thisdatareplacesthebroker/dealerdata.
Guidefor10b-10Certification

---

## Page 10

TradeInputandTradeSubmission 10
RecordField 10b-10Field [[Equity]] FixedIncomeMBS FIN/Repo
InterestedParty#1InstructionLine1 X X X X
InterestedParty#1InstructionLine2 X X X X
InterestedParty#2IDNumber X X X X
InterestedParty#2AccountNumber X X X X
InterestedParty#2InstructionLine1 X X X X
InterestedParty#2InstructionLine2 X X X X
AlternateCurrencyConversionRate X X X X
AlternateCurrencyISOCode X X X X
AlternateCurrencyNetAmount X X X X
Amortized/AccreditedFactor X X X X
Table3.1TradeInputandTradeSubmission—Record1
Guidefor10b-10Certification

---

## Page 11

TradeInputandTradeSubmission 11
Record2
Table3.2showstherequiredfieldsfortradeinputandtradesubmissionforrecord2.
RecordField 10b-10
Field
[[Equity]] Fixed
Income
MBS FIN/Repo
SecurityDescriptionLine21 X X X
SecurityDescriptionLine31 X X X
SecurityDescriptionLine41 X X X
SecurityDescriptionLine51 X X X
DiscountRate2 X X X
LegalStatus1 X X X
PaymentStatus1 X X X
BondTypeCode1 X X X
BasisIndicator1 X X X
ResultIndicator1 X X X
InterestAccrualDate1 X X X
InterestPaymentDate1 X X X
InterestRate1 X X X
MaturityDate1 Y X X X
OptionCallIndicator1 Y X X X
Call/PutFeature Y X X X
PutBondType1 X X X
PrerefundedorCallDate1 Y X X X
PrerefundedorCallPrice1 Y X X X
PutBondDate1 X X X
PutBondPrice1 X X X
BondFormCode1 X X X
InterestPaymentFrequency1 X X X
SpecialCouponIndicator1 X X X
Table3.2TradeInputandTradeSubmission—Record2
1TheTradeSuiteIDserviceattemptstoobtainsecuritydescriptionsandfieldsfromJ.J.KennyforDTC-eligible
municipalsecurities.Includedaresecuritiesthesubmitteridentifiesasamunicipalsecurity(securitytype=MUN).
Thisdatareplacesthebroker/dealerdata.
Guidefor10b-10Certification

---

## Page 12

TradeInputandTradeSubmission 12
RecordField 10b-10
Field
[[Equity]] Fixed
Income
MBS FIN/Repo
Flat/DefaultStatus1 X X X
TaxStatus1 X X X
Moody’sCreditRatings Y X X X
Standard&Poor’sCreditRatings Y X X X
SubjecttoFederalTax1 X X X
AlternateMinimumTax1 X X X
CurrentYield2 Y X X X
YieldtoMaturity2 Y X X X
YieldtoCall/Redemption2 Y X X X
DatedDate X X X
FINRAMSRBEMMAURL X X
SpecialInstructionsLine19,SpecialInstructionsLine
20,SpecialInstructionsLine21
Y X X X X
Table3.2TradeInputandTradeSubmission—Record2
Record4
Table3.3showstherequiredfieldsfortradeinputandtradesubmissionforrecord4.
RecordField 10b-10Field [[Equity]] FixedIncome MBS FIN/Repo
TradeTypeIndicator X
CurrentFace X
FactorEffectiveDate X
PoolNumber X
Table3.3TradeInputandTradeSubmission—Record4
1TheTradeSuiteIDserviceattemptstoobtainsecuritydescriptionsandfieldsfromJ.J.KennyforDTC-eligible
municipalsecurities.Includedaresecuritiesthesubmitteridentifiesasamunicipalsecurity(securitytype=MUN).
Thisdatareplacesthebroker/dealerdata.
2TocomplywithTradeSuiteIDcertificationandtheSECinterpretiveletterdatedNovember19,2010,enterthe
Rolefieldasadiscretefield,andthenpopulatethesamedatainoneoftheSpecialInstructionsfieldsinRecord1.
ThereareeightSpecialInstructionsfieldswith32characterseachinRecord1,position359–614.Formoreinform-
ation,seeTradeSuiteIDserviceConfirmTradeInputMessageSpecificationavailableintheInstitutionalTrade
Processing-TradeSuiteID.
Guidefor10b-10Certification

---

## Page 13

TradeInputandTradeSubmission 13
RecordField 10b-10Field [[Equity]] FixedIncome MBS FIN/Repo
(MBS)Yield X
RelatedReferenceNumber X
NumberofDaysAccruedInterest X
IssueDate X
SecurityClassCode X
OriginalTradePar X
GoodDeliveryMillions X
DeliveryDate X
EPNTime X
LotID X
Terminator X
MessageID X
PossibleDuplicates X
TradeNumber X
NumberofPools X
InternalID X
SubmitterAccountID X
ServiceType X
OptionType X
OptionExpirationDate X
RecordDate X
SpecificationCode1through16 X
SpecificationValue1through16 X
MBSInterestRate X
MBSMaturityDate X
Table3.3TradeInputandTradeSubmission—Record4
Record5
Table3.4showstherequiredfieldsfortradeinputandtradesubmissionforrecord5.
Guidefor10b-10Certification

---

## Page 14

TradeInputandTradeSubmission 14
RecordField 10b-10
Field
[[Equity]] FixedIncome MBS FIN/Repo
ClearingBroker/DealerInternalA/CNumber X X X X
ClearingAgentInternalA/CNumber X X X X
InstitutionInternalA/CNumber X X X X
InstitutionOrderRoutingReferenceNumber X X X X
ConfirmPurpose X X X X
DeliveryMethod X X X X
PriceType X X X X
BlockTradeIndicator X X X X
Give-upBroker/Dealer X X X X
[[Broker]]/DealerSalesman X X X X
TradeExecutionTime1 Y X X X X
TradeExecutionTimeZone1 Y X X X X
SIPCMember1 Y X X X X
FINRAMember X X X X
NYSEMember X X X X
MarketMaker1 Y X X X X
DeliveryInstructionsLines1and2 X X X X
WireInstructions X X X X
SpecialInstructionsLines9through18 X X X X
UserDefinedDisclosureCode X X X X
ConfirmDisclosureBypassIndicator X X X X
MarkUp/MarkDownSign1 Y X X X X
MarkUp/MarkDown1 Y X X X X
ThirdPartyRemunerationReceived1 Y X X X X
[[Broker]]/DealerTelephoneNumber X X X X
TradeExecutionDate X X
Table3.4TradeInputandTradeSubmission—Record5
1TocomplywithTradeSuiteIDcertificationandtheSECinterpretiveletterdatedNovember19,2010,enterthe
Rolefieldasadiscretefield,andthenpopulatethesamedatainoneoftheSpecialInstructionsfieldsinRecord1.
ThereareeightSpecialInstructionsfieldswith32characterseachinRecord1,position359–614.Formoreinform-
ation,seeTradeSuiteIDserviceConfirmTradeInputMessageSpecificationavailableintheInstitutionalTrade
Processing-TradeSuiteID.
Guidefor10b-10Certification

---

## Page 15

TradeInputandTradeSubmission 15
RecordField 10b-10
Field
[[Equity]] FixedIncome MBS FIN/Repo
MarkUp/MarkDownPercentageSign X X
MarkUp/MarkDownPercentage X X
BrokerLegalEntityIdentifier
InstitutionLegalEntity
Table3.4TradeInputandTradeSubmission—Record5
Record6
Table3.5showstherequiredfieldsfortradeinputandtradesubmissionforrecord6.
RecordField 10b-10Field [[Equity]] FixedIncome MBS FIN/Repo
TradeType X
LegIdentifier X
CollateralType X
Tri-PartyAgent X
StartDate X
EndDate/MaturityDate X
NumberofPiecesofCollateral X
ParentReferenceNumber X
AdditionalReferenceNumber1 X
AdditionalReferenceNumber2 X
FINRateSign X
FINRate X
FINRateType X
SecurityLendingFee X
AccrualMethod X
InterestDaysSign X
InterestDays X
AccruedInterestdueatMaturitySign X
AccruedInterestatMaturity X
Table3.5TradeInputandTradeSubmission—Record6
Guidefor10b-10Certification

---

## Page 16

TradeInputandTradeSubmission 16
RecordField 10b-10Field [[Equity]] FixedIncome MBS FIN/Repo
Index(Benchmark) X
SpreadtoBenchmarkorIndexSign X
SpreadtoBenchmarkorIndex X
[[Haircut]]% X
SubstitutionType X
SubstitutionNumber X
SubstitutionVariance X
SubstitutionFrequency X
Face(Par)orCashFillRepo X
RepoValue X
PremiumAmount X
InterestPaymentCalendarFrequency X
1stInterestCleanUpDate X
LookbackDays X
ResetIntervalFrequency X
1stRateResetDate X
FlexRepoPaybackFrequency X
1stFlexRepaymentDate X
CallDelay X
Table3.5TradeInputandTradeSubmission—Record6
Guidefor10b-10Certification

---

## Page 17

TradeOutputandTradeReceiving 17
4.TRADEOUTPUTANDTRADERECEIVING
Thissectionshowstherequiredcertificationfieldsfortradeoutputandtradereceivingof:
l Record1
l Record2
l Record4
l Record5
l Record6
Record1
Table4.1showstherequiredfieldsfortradeoutputandtradereceivingforrecord1.
RecordField 10b-10
Field
[[Equity]] Fixed
Income
MBS FIN/Repo
TransactionType X X X X
ExecutingBroker/DealerIDNumber X X X X
InstitutionIDNumber Y X X X X
AgentIDNumber X X X X
SecurityIdentifier Y X X X X
SettlementType X X X X
PrimeBrokerLong/ShortIndicator Y X X X X
Role Y X X X X
MarketCode X X X X
SideCode Y X X X X
NetPrice Y X X X X
[[shares]]/FaceValue Y X X X X
Price Y X X X X
PrincipalAmount X X X X
Registration/Shipping/Section31Fees X X X X
Interest X X X X
ResearchAmount X X X X
Table4.1TradeOutputandTradeReceiving—Record1
Guidefor10b-10Certification

---

## Page 18

TradeOutputandTradeReceiving 18
RecordField 10b-10
Field
[[Equity]] Fixed
Income
MBS FIN/Repo
CountryTax X X X X
Commission Y X X X X
OtherCharges X X X X
NetAmount X X X X
ExpandedSecurityType X X X X
AOCCIndicator X X X X
SplitCurrencySettlementIndicator X X X X
QualityControlReportingExemptIndicator X X X X
AllocationSource X X X X
SettlementLocation X X X X
SecurityNumberingSystem X X X X
CurrencyCode X X X X
OriginalBroker/DealerConfirmNumber X X X X
TradeDate Y X X X X
SettlementDate X X X X
SecurityDescriptionLine1 X X X X
AccountType Y X X X X
PaymentMethodIndicator X X X X
Cancelation/CorrectionReasonCode X X X X
AgentInternalAccountNumber X X X X
[[Broker]]/DealerInternalAccountNumber X X X X
[[Broker]]/DealerConfirmNumber X X X X
SpecialInstructionsLines1through8 X X X X
DTCSettlementMode X X X X
ConfirmProcessTime X X X X
SecurityFormCode X X X X
InterestedParty#1IDNumber X X X X
InterestedParty#1AccountNumber X X X X
InterestedParty#1InstructionLine1 X X X X
InterestedParty#1InstructionLine2 X X X X
Table4.1TradeOutputandTradeReceiving—Record1
Guidefor10b-10Certification

---

## Page 19

TradeOutputandTradeReceiving 19
RecordField 10b-10
Field
[[Equity]] Fixed
Income
MBS FIN/Repo
InterestedParty#2IDNumber X X X X
InterestedParty#2AccountNumber X X X X
InterestedParty#2InstructionLine1 X X X X
InterestedParty#2InstructionLine2 X X X X
DTCControlNumber X X X X
TransactionSequenceNumber X X X X
AlternateCurrencyConversionRate X X X X
AlternateCurrencyISOCode X X X X
AlternateCurrencyNetAmount X X X X
Amortized/AccreditedFactor X X X X
InterestedParty#1Type X X X X
InterestedParty#2Type X X X X
InterestedParty#3Type X X X X
InterestedParty#3IDNumber X X X X
InterestedParty#3AccountNumber X X X X
InterestedParty#3InstructionLine1 X X X X
InterestedParty#3InstructionLine2 X X X X
DTCControlNumber X X X X
TransactionSequenceNumber X X X X
AlternateCurrencyConversionRate X X X X
AlternateCurrencyISOCode X X X X
AlternateCurrencyNetAmount X X X X
Amortized/AccreditedFactor X X X X
InterestedParty#1Type X X X X
InterestedParty#2Type X X X X
InterestedParty#3Type X X X X
InterestedParty#3IDNumber X X X X
InterestedParty#3AccountNumber X X X X
InterestedParty#3InstructionLine1 X X X X
InterestedParty#3InstructionLine2 X X X X
Table4.1TradeOutputandTradeReceiving—Record1
Guidefor10b-10Certification

---

## Page 20

TradeOutputandTradeReceiving 20
RecordField 10b-10
Field
[[Equity]] Fixed
Income
MBS FIN/Repo
InstitutionContact X X X X
BypassIndicator X X X X
AttempttoCancel/CancelAfterAffirmationIndic-
ator
X X X X
MatchedIndicator X X X X
DTCEligibilityIndicator X X X X
AccountFoundIndicator X X X X
DisaffirmationIndicator X X X X
EligibilityReasonCodes X X X X
MatchingVariance X X X X
VarianceDirection X X X X
DesignatedAffirmingPartyType X X X X
DesignatedAffirmingPartyNumber X X X X
ConfirmProcessDate X X X X
ReportReceiverType X X X X
AffirmingPartyIndicator X X X X
ClearingBroker/DealerIDNumber X X X X
ClearingAgentIDNumber X X X X
SecurityDescriptionType X X X X
IDNetNumber X X X X
Table4.1TradeOutputandTradeReceiving—Record1
Record2
Table4.2showstherequiredfieldsfortradeoutputandtradereceivingforrecord2.
Guidefor10b-10Certification

---

## Page 21

TradeOutputandTradeReceiving 21
RecordField 10b-10
Field
[[Equity]] Fixed
Income
MBS FIN/Repo
SecurityDescriptionLine21 X X X
SecurityDescriptionLine31 X X X
SecurityDescriptionLine41 X X X
SecurityDescriptionLine51 X X X
DiscountRate2 X X X
LegalStatus1 X X X
PaymentStatus1 X X X
BondTypeCode1 X X X
BasisIndicator1 Y X X X
ResultIndicator1 X X X
InterestAccrualDate1 X X X
InterestPaymentDate1 X X X
InterestRate1 X X X
MaturityDate1 Y X X X
OptionCallIndicator1 Y X X X
Call/PutFeature Y X X X
PutBondType1 X X X
PrerefundedorCallDate1 Y X X X
PrerefundedorCallPrice1 Y X X X
PutBondDate1 X X X
PutBondPrice1 X X X
BondFormCode1 X X X
InterestPaymentFrequency1 X X X
SpecialCouponIndicator1 X X X
Table4.2TradeOutputandTradeReceiving—Record2
1TheTradeSuiteIDattemptstoobtainsecuritydescriptionsandfieldsfromJ.J.KennyforDTC-eligiblemunicipal
[[securities]].Includedaresecuritiesthesubmitteridentifiesasamunicipalsecurity(securitytype=MUN).Thisdata
replacesthebroker/dealerdata.
2TocomplywithTradeSuiteIDcertificationandtheSECinterpretiveletterdatedNovember19,2010,enterthe
Rolefieldasadiscretefield,andthenpopulatethesamedatainoneoftheSpecialInstructionsfieldsinRecord1.
ThereareeightSpecialInstructionsfieldswith32characterseachinRecord1,position359–614.Formoreinform-
ation,seeTradeSuiteIDserviceConfirmTradeInputMessageSpecificationavailableintheInstitutionalTrade
Processing-TradeSuiteID.
Guidefor10b-10Certification

---

## Page 22

TradeOutputandTradeReceiving 22
RecordField 10b-10
Field
[[Equity]] Fixed
Income
MBS FIN/Repo
Flat/DefaultStatus1 X X X
TaxStatus1 X X X
Moody’sCreditRatings Y X X X
Standard&Poor’sCreditRatings Y X X X
SubjecttoFederalTax1 X X X
AlternateMinimumTax1 X X X
InstitutionName X X X
AgentName X X X
ExecutingBroker/DealerName X X X
ClearingBroker/DealerName X X X
ClearingAgentName X X X
InterestedParty#1Name X X X
InterestedParty#2Name X X X
InterestedParty#3Name X X X
OriginalInputSecurityNumberingSystem X X X
OriginalInputSecurityIdentifier X X X
DTCControlNumber X X X
TransactionSequenceNumber X X X
[[CUSIP]]/CINSSecurityNumberingSystem X X X
[[CUSIP]]/CINSSecurityIdentifier X X X
CurrentYield2 Y X X X
YieldtoMaturity2 Y X X X
YieldtoCall/Redemption2 Y X X X
DatedDate X X X
Table4.2TradeOutputandTradeReceiving—Record2
1TradeSuiteIDattemptstoobtainsecuritydescriptionsandfieldsfromJ.J.KennyforDTC-eligiblemunicipal
[[securities]].Includedaresecuritiesthesubmitteridentifiesasamunicipalsecurity(securitytype=MUN).Thisdata
replacesthebroker/dealerdata.
2TocomplywithTradeSuiteIDservicecertificationandtheSECinterpretiveletterdatedNovember19,2010,
entertheRolefieldasadiscretefield,andthenpopulatethesamedatainoneoftheSpecialInstructionsfieldsin
Record1.ThereareeightSpecialInstructionsfieldswith32characterseachinRecord1,position359–614.For
moreinformation,seeTradeSuiteIDConfirmTradeInputMessageSpecificationavailableintheInstitutional
TradeProcessing-TradeSuiteID.
Guidefor10b-10Certification

---

## Page 23

TradeOutputandTradeReceiving 23
RecordField 10b-10
Field
[[Equity]] Fixed
Income
MBS FIN/Repo
FINRAMSRBEMMAURL X X
SpecialInstructionsLine19,SpecialInstructionsLine
20,SpecialInstructionsLine21
Y X X X X
Table4.2TradeOutputandTradeReceiving—Record2
Guidefor10b-10Certification

---

## Page 24

TradeOutputandTradeReceiving 24
Record4
Figure4.1showstherequiredfieldsfortradeoutputandtradereceivingforrecord4.
RecordField 10b-10Field [[Equity]] FixedIncome MBS FIN/Repo
TradeTypeIndicator X
CurrentFace X
FactorEffectiveDate X
PoolNumber X
Yield X
RelatedReferenceNumber X
NumberofDaysAccruedInterest X
IssueDate X
SecurityClassCode X
SecurityClassName X
OriginalTradePar X
GoodDeliveryMillions X
DeliveryDate X
EPNTime X
LotID X
Terminator X
MessageID X
PossibleDuplicate X
TradeNumber X
NumberofPools X
InternalID X
SubmitterAccountID X
ServiceType X
OptionType X
OptionExpirationDate X
RecordDate X
SpecificationCode1through16 X
SpecificationValue1through16 X
Figure4.1TradeOutputandTradeReceiving—Record4
Guidefor10b-10Certification

---

## Page 25

TradeOutputandTradeReceiving 25
RecordField 10b-10Field [[Equity]] FixedIncome MBS FIN/Repo
MBSInterestRate X
MBSMaturityDate X
Figure4.1TradeOutputandTradeReceiving—Record4
Guidefor10b-10Certification

---

## Page 26

TradeOutputandTradeReceiving 26
Record5
Table4.3showstherequiredfieldsfortradeoutputandtradereceivingforrecord5.
RecordField 10b-10Field [[Equity]] FixedIncomeMBS FIN/Repo
ClearingBroker/DealerInternalA/CNumber X X X X
ClearingAgentInternalAccountNumber X X X X
InstitutionInternalA/CNumber X X X X
InstitutionOrderRoutingNumber X X X X
AllocationBlockReferenceIdentifier X X X X
AllocationDetailReferenceIdentifier X X X X
ConfirmPurpose X X X X
DeliveryMethod X X X X
PriceType X X X X
BlockTradeIndicator X X X X
Give-upBroker/Dealer X X X X
[[Broker]]/DealerSalesman X X X X
TradeExecutionTime Y X X X X
TradeExecutionTimeZone Y X X X X
SIPCMember Y X X X X
FINRAMember - X X X X
NYSEMember - X X X X
MarketMaker Y X X X X
DeliveryInstructionsLine1&2 X X X X
WireInstructions X X X X
SpecialInstructionsLines9through18 X X X X
ConfirmDisclosureLink X X X X
DisclosureReferenceNumber X X X X
DisclosureFoundIndicator X X X X
UserDefinedDisclosureCode X X X X
ConfirmDisclosureBypassIndicator X X X X
MarkUp/MarkDownSign Y X X X X
Table4.3TradeOutputandTradeReceiving—Record5
Guidefor10b-10Certification

---

## Page 27

TradeOutputandTradeReceiving 27
RecordField 10b-10Field [[Equity]] FixedIncomeMBS FIN/Repo
MarkUp/MarkDown Y X X X X
3rdPartyRemunerationReceived Y X X X X
[[Broker]]/DealerTelephoneNumber X X X X
DTCControlNumber X X X X
TransactionSequenceNumber X X X X
TradeExecutionDate X X
MarkUp/MarkDownPercentageSign X X
MarkUp/MarkDownPercentage X X
BrokerLegalEntityIdentifier
InstitutionLegalEntityIdentifier
Table4.3TradeOutputandTradeReceiving—Record5
Record6
Table4.4showstherequiredfieldsfortradeoutputandtradereceivingforrecord6.
RecordField 10b-10Field [[Equity]] FixedIncome MBS FIN/Repo
TradeType X
LegIdentifier X
CollateralType X
Tri-PartyAgent X
StartDate X
EndDate/MaturityDate X
NumberofPiecesofCollateral X
ParentReferenceNumber X
AdditionalReferenceNumber1 X
AdditionalReferenceNumber2 X
FINRateSign X
FINRate X
FINRateType X
SecurityLendingFee X
Table4.4TradeOutputandTradeReceiving—Record6
Guidefor10b-10Certification

---

## Page 28

TradeOutputandTradeReceiving 28
RecordField 10b-10Field [[Equity]] FixedIncome MBS FIN/Repo
AccrualMethod X
InterestDaysSign X
InterestDays X
AccruedInterestdueatMaturitySign X
AccruedInterestatMaturity X
Index(Benchmark) X
SpreadtoBenchmarkorIndexSign X
SpreadtoBenchmarkorIndex X
[[Haircut]]% X
SubstitutionType X
SubstitutionNumber X
SubstitutionVariance X
SubstitutionFrequency X
Face(Par)orCashFillRepo X
RepoValue X
PremiumAmount X
InterestPaymentCalendarFrequency X
1stInterestCleanUpDate X
LookbackDays X
ResetIntervalFrequency X
1stRateResetDate X
FlexRepoPaybackFrequency X
1stFlexRepaymentDate X
CallDelay X
DTCControlNumber X
TransactionSequenceNumber X
Table4.4TradeOutputandTradeReceiving—Record6
Guidefor10b-10Certification

---

## Page 29

SecurityTypesinEachAssetClassCategory 29
A.SECURITYTYPESINEACHASSETCLASSCATEGORY
TableA.1showsabreakdownofthesecuritytypescontainedwithineachassetclasscategory.
AssetClassCode AssetClassDescription SecurityType SecurityTypeDescription
EQU Equities [[ADR]] AmericanDepositaryReceipt
EQU Equities CER RepresentativeCertificates
EQU Equities MSC Miscellaneous
EQU Equities OPC OptionsContracts
EQU Equities OPS OptionsShares
EQU Equities PRC PremiumContracts
EQU Equities PRS PremiumShares
EQU Equities RTE Rentes
EQU Equities RTS Rights
EQU Equities SHP Equities—PreferredShares
EQU Equities SHS Equities—[[shares]]
EQU Equities UNT Units
EQU Equities WTS [[Warrants]]
FXI FixedIncome AGS Agencies
FXI FixedIncome BAS Banker’sAcceptances
FXI FixedIncome CDS CorporateDebt
FXI FixedIncome COD CertificateofDeposit
FXI Repo COL [[collateral]]
FXI FixedIncome CON ConvertibleBond
FXI FixedIncome CPA CommercialPaper
FXI FixedIncome CPN Coupons
FXI FixedIncome CSH USCashWire
FXI FixedIncome CS1 USCashWireNumber1
FXI FixedIncome CS2 USCashWireNumber2
FXI FixedIncome CS3 USCashWireNumber3
FXI FixedIncome CS4 USCashWireNumber4
TableA.1SecurityTypesinEachAssetClassCategory
Guidefor10b-10Certification

---

## Page 30

SecurityTypesinEachAssetClassCategory 30
AssetClassCode AssetClassDescription SecurityType SecurityTypeDescription
FXI FixedIncome CS5 USCashWireNumber5
FXI FixedIncome DFI DTCOmnibus
FXI FixedIncome EBD Eurobonds
FXI FixedIncome ECD EuroCD
FXI FixedIncome [[ECP]] EuroCP
FXI FixedIncome ENT Euronotes
FXI FixedIncome FFI FixedIncomeOmnibus
FXI Repo FIN FinanceTransaction
FXI FixedIncome FPA Face,Principal,orNominalAmount
FXI FixedIncome GDS GovernmentDebtSecurities
FXI FixedIncome ITS IndexedTreasurySecurities
FXI FixedIncome MMI MoneyMarketInstruments
FXI FixedIncome MTN MediumTermNotes
FXI FixedIncome MUN MunicipalBonds
FXI FixedIncome NSD NonUSSovereignDebt
FXI FixedIncome OMM OtherMoneyMarketInstruments
FXI FixedIncome SLA StudentLoanMarketingAssociation
FXI FixedIncome TBI TreasuryBills
FXI FixedIncome TEM TaxExemptMoneyMarkets
FXI FixedIncome TRB TreasuryBonds
FXI FixedIncome TRN TreasuryNotes
FXI FixedIncome TRS TreasuryStrips
FXI FixedIncome XCP TaxExemptCommercialPaper
MBS Mortgage-BackedSecurities [[ABS]] [[Asset]]-BackedSecurity
MBS Mortgage-BackedSecurities CMO CollateralizedMortgageObligation
MBS Mortgage-BackedSecurities FMR FreddieMacRemics
MBS Mortgage-BackedSecurities FNM FannieMae
MBS Mortgage-BackedSecurities FNR FannieMaeRemics
MBS Mortgage-BackedSecurities FRM FreddieMac
MBS Mortgage-BackedSecurities GMR GinnieMaeRemics
MBS Mortgage-BackedSecurities GNM GinnieMae
TableA.1SecurityTypesinEachAssetClassCategory
Guidefor10b-10Certification

---

## Page 31

SecurityTypesinEachAssetClassCategory 31
AssetClassCode AssetClassDescription SecurityType SecurityTypeDescription
MBS Mortgage-BackedSecurities MBS Mortgage-BackedSecurities
MB Mortgage-BackedSecurities OMB OtherMortgage-BackedSecurities
TableA.1SecurityTypesinEachAssetClassCategory
Guidefor10b-10Certification

---

## Page 32

