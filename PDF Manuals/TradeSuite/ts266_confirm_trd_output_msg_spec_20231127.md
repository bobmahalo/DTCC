---
title: "Confirm Trade Output Message Specification"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ts266_confirm_trd_output_msg_spec_20231127.pdf"
pages: 89
size: "655.8 KB"
category: "TradeSuite"
ingested_on: "2026-06-05"
---

# Confirm Trade Output Message Specification

**Original File:** [ts266_confirm_trd_output_msg_spec_20231127.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ts266_confirm_trd_output_msg_spec_20231127.pdf)  
**Category:** TradeSuite  
**Total Pages:** 89  
**File Size:** 655.8 KB  

---

## Page 1

TradeSuiteID®
CONFIRMTRADEOUTPUTMESSAGE
SPECIFICATION
VERSION
NOVEMBER27,2023

---

## Page 2

TABLEOFCONTENTS
Preface 4
Audience 4
ChangesinThisVersion 4
RelatedDocumentsandTraining 9
Questions? 9
1.GeneralInformation 10
TradeOutputFileUsingCCFandMQ 10
Availability 10
2.FormatSpecifications 11
RecordsintheOutputFile 11
RestrictionsonRecords 11
AdditionalParties 12
ChangeofEligibility 12
Validation 12
3.OutputRecordFormats 14
LegendforAllRecordFormats 14
HeaderRecord 14
TrailerRecord 16
VersionoftheRecordFormats 18
DetailRecord1:GeneralTradeOutput 18
DetailRecord2:AdditionalFixedIncomeInformationOutput 40
DetailRecord3:AdditionalPartyOutput 54
DetailRecord4:Mortgage-BackedSecuritiesOutput 61
ConfirmTradeOutputMessageSpecification
TableOfContents 2

---

## Page 3

DetailRecord5:SupplementalOutput 69
DetailRecord6:Financing/REPOTransactionOutput 79
ConfirmTradeOutputMessageSpecification
TableOfContents 3

---

## Page 4

PREFACE
ThisdocumentdescribesthetradeoutputfilefortheTradeSuiteID®service.Itdescribestherequired
recordformatsandexplainsmodificationsoftherecordssincethepreviousrelease.
TradeSuiteIDisacomprehensivetradeprocessingsolutionthatautomatesmessagingandsettlementfor
equityandfixedincomesecurities.Investmentmanagers([[Institutions]]),[[Broker]]/dealers,[[Custodians]],and
interestedpartiesuseTradeSuiteIDforpost-tradeprocessingondomesticandcross-bordertradesof
U.S.[[securities]].
Audience
Thisdocumentisforinformationtechnologyprofessionals,businessanalysts,andotherswhoare
responsibleforimplementingoroperatingthefollowingsystems:
l Computerfacility([[CCF]])
l MessageQuerying(MQ)
Itisnecessarytounderstandthesecuritiesindustryandknowhowtheindustryhandlestrades.Youmust
haveabasicunderstandingofelectronictradeandtransactionprocessingconceptsandaworking
knowledgeoftheWindowsoperatingsystem.
ChangesinThisVersion
ThissectiondescribesthechangesfortheConfirmOutputMessageSpecification.
TradeSuiteID8.3(NewChanges)
l Record5:
l DetailRecord5:SupplementalOutputPositions897-904(fieldname:MatchDate)hasbeenadded.
TheDateofwhichtheconfirmwasmatchedinTradeMatch.InFormatCCYYMMDD.Thisnewfieldis
currentlyintheTestsystemandwillbeavailableintheproductionsystemintheT1releaseinMay
2024
l DetailRecord5:SupplementalOutputPositions905-910(fieldname:MatchTime)hasbeenadded.
TheTimeofwhichtheconfirmwasmatchedinTradeMatch.InFormatHHMMSS.Thisnewfieldiscur-
rentlyintheTestsystemandwillbeavailableintheproductionsystemintheT1releaseinMay2024
ConfirmTradeOutputMessageSpecification
Preface 4

---

## Page 5

TradeSuiteID8.2
l Record1(18):
o ThefieldRecordTypeRAFCAN/RAFCORnowappliestobothReverseAffirmationandDisaf-
firmation.
TradeSuiteID8.1(previouslycommunicatedchanges)
l Record1(18):
o ThedescriptionfortheexistingDTCControlNumberhasbeenupdatedasfollows: Number
assignedbytheTradeSuiteID®servicetoabroker/dealer’strade.Thisnumbercanalsobeused
toassociatethisrecordwithitsotherrecords.TheDTCControlNumbersarerecycledbasedon
overalltradeactivity.
o TheAllocationSourcedescriptionsfortwovalidvalueshavebeenupdated:
Thedescriptionfor6isnowCTMviaUSDI.
Thedescriptionfor7isnowCTMviaUSDM
l Record2(40):ThedescriptionfortheexistingDTCControlNumberhasbeenupdatedas
follows: NumberassignedbytheTradeSuiteID®servicetoabroker/dealer’strade.Thisnumbercan
alsobeusedtoassociatethisrecordwithitsotherrecords.TheDTCControlNumbersarerecycled
basedonoveralltradeactivity.
l Record3(54):ThedescriptionfortheexistingDTCControlNumberhasbeenupdatedas
follows: NumberassignedbytheTradeSuiteID®servicetoabroker/dealer’strade.Thisnumbercan
alsobeusedtoassociatethisrecordwithitsotherrecords.TheDTCControlNumbersarerecycled
basedonoveralltradeactivity.
l Record4(61):ThedescriptionfortheexistingDTCControlNumberhasbeenupdatedas
follows: NumberassignedbytheTradeSuiteID®servicetoabroker/dealer’strade.Thisnumbercan
alsobeusedtoassociatethisrecordwithitsotherrecords.TheDTCControlNumbersarerecycled
basedonoveralltradeactivity.
l Record5(78):
o ThedescriptionfortheexistingDTCControlNumberhasbeenupdatedasfollows: Number
assignedbytheTradeSuiteID®servicetoabroker/dealer’strade.Thisnumbercanalsobeused
toassociatethisrecordwithitsotherrecords.TheDTCControlNumbersarerecycledbasedon
overalltradeactivity.
o CTMBrokerReferenceNumber(positions881-896)hasbeenaddedasanewfield.Itprovidesa
referencenumbertolinkallM2i(USDI/USDM)tradesprocessedthroughtheUSDepositoryfrom
theCTM®servicetotheTradeSuiteID®serviceviaCMI.
o DuetotheadditionofthenewCTMBrokerReferenceNumberfield,thepositionsforthe
reservedFillerfieldhavebeenupdatedto897-978.
ConfirmTradeOutputMessageSpecification
Preface 5

---

## Page 6

l Record6(78):ThedescriptionfortheexistingDTCControlNumberhasbeenupdatedas
follows: NumberassignedbytheTradeSuiteID®servicetoabroker/dealer’strade.Thisnumbercan
alsobeusedtoassociatethisrecordwithitsotherrecords.TheDTCControlNumbersarerecycled
basedonoveralltradeactivity.
TradeSuiteID8.06(previouslycommunicatedchanges)
TheMUNIEnrichmentchangestopsreplacingindividualMUNIfieldswhendatavaluesforagivenMUNI
EnrichmentDatabase(onthemainframe)containanon-blank/null/zerovaluesinConfirmTradeInput.
Inaddition,thisdocumentcontainsbetterdefinitionsfortheMUNI-EnrichedFields:
l Record1:SecurityDescriptionLine1(28):
l Record2(page40):
o SecurityDescriptionLines
2&3
o MSRBInterestAccrual
Date
o MSRBInterestPayment
Date
o MSRBInterestRate
o MSRBMaturityDate
o MSRBOptionCallIndicator
o MSRBCall/PutFeature
Indicator
o MSRBPutBondType
o MSRBPrerefundedorCall
Date
o MSRBPrerefundedorCall
Price
o MSRBPutBondDate
o MSRBPutBondPrice
o MSRBBondFormCode
o MSRBInterestPayment
Frequency
o MSRBSpecialCoupon
Indicator
o MSRBFlat/DefaultStatus
o MSRBTaxStatus
o MSRBMoody'sCreditRat-
ing
o MSRBS&PCreditRating
o MSRBSubjecttoFederal
Tax
o MSRBAlternateMinimum
Tax
TradeSuite8.05 (previouslycommunicatedchanges)
TheSecuritiesandExchangeCommission([[SEC]])approvedamendmentstoFINRARule2232
(CustomerConfirmations)thatrequirememberfirmstodiscloseadditionaltransaction-related
informationtoretailcustomersfortradesincertainfixedincomesecurities.Specifically,amendedRule
2232requiresamembertodisclosetheamountandpercentageofmark-upormark-downitappliesto
tradeswithretailcustomersincorporateoragencydebtsecuritiesifthememberalsoexecutesan
offsettingprincipaltradeinthesamesecurityonthesametradingday.Theamendedrulealsorequires
memberstodisclosetwoadditionalitemsonallretailcustomerconfirmationsforcorporateandagency
debtsecuritytrades:(1)areference,andahyperlinkiftheconfirmationiselectronic,toawebpage
hostedbyFINRAthatcontainspubliclyavailabletradingdataforthespecificsecuritythatwastraded,
and(2)theexecutiontimeofthetransaction,expressedtothesecond.TheMSRBRuleG-15andG-30
hasalsochangedtoaccommodatethesechanges.ThisnewregulationgoesintoeffectonMay14,
2018.
ConfirmTradeOutputMessageSpecification
Preface 6

---

## Page 7

Tocomplywiththeseregulatorychanges,DTCChasmadethefollowingchangestotheDirectOutput
records.
l DetailRecord2:AdditionalFixedIncomeInformationOutputPositions829-878(fieldname: [[FINRA]]
MSRBEMMAURL).ThisfieldcontainsURL linkstotheappropriatewebsites: FINRAorMSRB.
l DetailRecord2:AdditionalFixedIncomeInformationOutputPosition879-910(fieldname: Special
InstructionsLine19).Thisfieldcontainsadditionalspecialinstructionsinfree-formtext.
l DetailRecord2:AdditionalFixedIncomeInformationOutputPosition911-942(fieldname: Special
InstructionsLine20).Thisfieldcontainsadditionalspecialinstructionsinfree-formtext.
l DetailRecord2:AdditionalFixedIncomeInformationOutputPosition943-974(fieldname: Special
InstructionsLine21).Thisfieldcontainsadditionalspecialinstructionsinfree-formtext.
l DetailRecord5:SupplementalOutput.TheexistingPositions824-893(fieldname: IDNetDisclosure
Line1)havebeenremoved.
l DetailRecord5:SupplementalOutput.TheexistingPositions894-963(fieldname: IDNetDisclosure
Line2)havebeenremoved.
l DetailRecord5:SupplementalOutputPositions824-831(fieldname:TradeExecutionDate)have
beenadded.TheoutputrepresentstheTradeExecutionDatethatthebroker/dealerbookedthetrade.
l DetailRecord5:SupplementalOutputPosition832(fieldname:MarkUp/MarkDownPercentage
Sign)hasbeenadded.Thisfieldcanbe:
o +=Positive
o -=Negative
o Space=notprovided
l DetailRecord5:SupplementalOutputPositions833-840(fieldname:MarkUp/MarkDownPer-
centage)hasbeenadded.Thisfieldenablesthebroker/dealertoreportanypercentageoftheMarkUp
/MarkDowndifferencebetweenthereportedpriceandthepricetothecustomerinvolvedinthetrans-
action,displayedasapercentage.
l DetailRecord5:SupplementalOutputPositions841-860(fieldname: BrokerLegalEntityIdentifier)
havebeenadded.Theoutputisauniquealphanumericbrokeridentifier(ISO17442).ThisisaMIFID II-
relatedchange.
l DetailRecord5:SupplementalOutputPositions861-880(fieldname: InstitutionLegalEntityIdentifier)
havebeenadded.Theoutputisauniquealphanumericbrokeridentifier(ISO17442).ThisisaMIFID II-
relatedchange.
ThisversionalsoincludesadditionstoallocationvaluesfortheCTM®service.
l DetailRecord1:GeneralTradeOutput(fieldname:AllocationSource)allowstwonewvalues:6(USDI
viaM2i)and7USDMviaM2I).
TradeSuiteID8.0.4(previouslycommunicatedchanges)
ConfirmTradeOutputMessageSpecification
Preface 7

---

## Page 8

Tocomplywiththemarketsinfinancialinstrumentsdirective(MiFIDII)regulationsandallowforgreater
transparencyacrossthetradingprocess,DetailRecord1:GeneralTradeOutputhasbeenupdatedwith
thefollowingchanges:
l LocalTaxfieldhasbeenreplacedwiththeResearchAmountfield.SeetheResearchAmountfield.
l UsetheCountryTaxfieldforcountryandfederaltaxes.ThisfieldisalsousedfortheAmericandepos-
itaryreceipt([[ADR]])foreigntaxes.SeetheCountryTaxfield.
l UsetheOtherChargesfieldforallotherreasons.SeetheOtherChargesfield.
l CreatedICMerrorcodesrelatedtotheresearchamount.Foralistofcancellationreasoncodes,see
sectionCancellationReasonCodesinInput/OutputInformation.
InadditiontotheMiFIDIIinitiativechanges,theappearanceandlayoutofthedocumentationhas
changedtoensureconsistencyacrossDTCC.
TradeSuiteID8.0.3(previouslycommunicatedchanges)
UpdatestothefielddescriptionsforthefollowingfieldsinRecord2:
l InterestPaymentFrequency
l SubjecttoFederalTax
l AlternateMinimumTax
TradeSuiteID8.0.2(previouslycommunicatedchanges)
l UpdatedDetailedrecord2:municipalsecurityoutputtoAdditionalFixedIncomeInformationinthe
MunicipalSecurities(MUNI)printedandarchiveconfirmationreportstoavoidmisinterpretation.For
moreinformation,seeDetailRecord2:AdditionalFixedIncomeInformationOutput
l ModifiedlinkstothedocumentationtoenableaccesstothenewlydesignedDTCCLearningCenter.
l RevampedtheappearanceandlayoutofthedocumentationtoensureconsistencyacrossallDTCC
applications.
TradeSuiteID8.0.1(previouslycommunicatedchanges)
l AddedtheVendorControlIDfieldinposition754-762.SeeDetailRecord5:SupplementalOutput.
TradeSuiteID8.0(previouslycommunicatedchanges)
ConfirmTradeOutputMessageSpecification
Preface 8

---

## Page 9

l AddedaSellShortExempt(E)indicatortotheLong/ShortIndicatorfieldinposition66.SeeDetail
Record1:GeneralTradeOutput.
l AddedaRisklessPrincipal(0-RisklessPrincipal)valuetotheRoleindicatorinposition67.SeeDetail
Record1:GeneralTradeOutput.
l ExpandedtheAgentInternalAccountNumberfieldinposition689-723to35characters.SeeDetail
Record5:SupplementalOutput.
l AddedtheCommissionEquivalentvalueinposition724-732.SeeDetailRecord5:SupplementalOut-
put.
l ProvidedmoreIDNewDisclosureinformationinpositions894-963and964-978.SeeDetailRecord
5:SupplementalOutput.
l ProvidedanewlinkandreferencenumbertotheOperatingProceduresguideinpositions733-748
and774-823.SeeDetailRecord5:SupplementalOutput.
RelatedDocumentsandTraining
Forrelateddocumentsandtraining,seeTradeSuiteID®ontheDTCCLearningCenter.
Questions?
TheClientCenterprovidesgeneralassistanceandtechnicalhelp.Visitto:
l Enteraservicerequestorcheckthestatusofanexistingservicerequest.
l Searchtheknowledgebase.
l Obtaincontactinformation.
ConfirmTradeOutputMessageSpecification
Preface 9

---

## Page 10

1.GENERALINFORMATION
Thissectiondescribestheavailabilityofthetradeoutputfile.
TradeOutputFileUsingCCFandMQ
DTCCprovidesenhancedComputer-to-ComputerFacility([[CCF]])andMessageQuerying(MQ)
processing.ThesesystemsallowforinteractivereceiptanddistributionofTradeSuiteIDdata.
Notes
l Alldetailrecordscontainatransactionheaderinpositions1-26andamailboxprefix.
l ForCCFapplication-orientederrors,TradeSuiteIDappendsamessageprefixtothefrontofthe
record.Theapplicationalsoappendsablocktotheendoftherecord.Formoreinformationsee
Input/OutputInformation.
Availability
Interactiveoutputisavailablethroughoutthedayfromapproximately1:30A.M.tomidnight,EasternTime.
Sendandreceiveconfirmationsinteractively.
RecordsareunsortedanddonotcontainTradeSuiteIDheadersortrailers.However,end-of-dayreports,
suchastheCumulativeEligibleTradesandUnaffirmedreports,includeaheaderandtrailer.The
TradeSuiteIDserviceproducesthechangeofeligibilityconfirmsandincludestheconfirmswithinthe
messagequeue(themailbox).However,theseend-of-dayreportsdonotcontainheadersortrailers.
ConfirmTradeOutputMessageSpecification
1.GeneralInformation 10

---

## Page 11

2.FORMATSPECIFICATIONS
Thissectiondescribestheoutputfileformatspecifications.
RecordsintheOutputFile
Theinteractiveoutputspecificationsdescribedinthisdocumentconsistofonerequiredrecordandthree
optionalrecords.Youcanchoosetoreceivethesecondrecordforadditionalfixedincomeinformationall
ofthetimeornotatall.Youcanchoosetoreceivethethirdandfourthrecordsonanoptionalbasis.
Toreceivearecord,faxyourrequeststotheTradeSuiteIDSupportUnitatwww.[[DTCC]].com/client-center.
TheTradeSuiteIDmasterfileallowsyoutominimizetheamountofdatareceivedbycontrollingthe
transmissionofthe2nd,3rd,and4threcords.Table2.1describeseachrecord.
Record Description
1 Providesgeneraltradeinformationforoutputmessages.
2 Meetsthespecificrequirementsofsecuritydescriptionsformunicipaldebtsecurities.Fivelinesof78charactersare
availableforsecuritydescriptionat:
l SecurityDescriptionLine1inrecord1,position237–314
l SecurityDescriptionLine2,3,4,and5inrecord2,positions28–339
Lines1,2,and3showiftheMUNIEnrichmentdatabasereceivesasecuritydescriptionforadditionalfixedincome
information.Discretefieldsinrecord2,positions340–420containthesameMUNIEnrichmentdata,mostlyin
numericvalues.
3 Relatestheinstitutioninstructionstotheconfirms.Therecordcontainsinformation,suchasinternalaccountnum-
bers,additionalinterestedparties,andinstitutionalreferencenumbers.
4 Meetsthespecificrequirementsofmortgage-backedsecuritiestrades.
5 Providessupplementaloradditionalinformationaboutaconfirm,suchas10b–10informationandadditionalspecial
instructionfields.
6 Meetsthespecificrequirementsoffinancingtransactionsregardingrepurchaseagreements(REPOs).
Table2.1OutputFileRecordDescriptions
RestrictionsonRecords
Youreceivethe2nd,3rd,4th,5th,and6threcordsforallconfirmandchangeofeligibilityreporttypes.
However,youdonotreceivetherecordsfortheunaffirmedandcumulativeeligibletradereports.
ConfirmTradeOutputMessageSpecification
2.FormatSpecifications 11

---

## Page 12

Toallowforinteractivedistributionofdata,atransactionheaderispartofthedetailrecordsandtherecord
includesamessageprefix.Sincethemessageprefixisnotconsideredapplication-oriented,itdisplays
separately.
AdditionalParties
Additionalpartiesincludecustomers,interestedparties,andsub-[[Custodians]].Formoreinformation,see
Input/OutputInformation.
ForconfirmationssettlingatDepositoryTrustCompany([[DTC]]),thereisroomforthreeadditionalparties,
includingacustomer.FortradeconfirmationsnotsettlingatDTC,thereisroomforuptotwoadditional
parties,includingacustomer.TradesthatdonotsettleatDTCcontainonelessadditionalparty,since
settlementinformation(eithercontrasub-custodianoraccountidentifieratdepositoriesotherthanDTC)
usesthefirstslot.Itispossibletoaddadditionalinterestedpartiesonconfirmationsinthefuture.
ChangeofEligibility
Atthecloseofeachbusinessdaythroughsettlement-1(S-1),theTradeSuiteIDserviceevaluatesthe
confirm’seligibilitywiththesettlementlocationofDTCorbrokercustody.TheTradeSuiteIDserviceoffers
intra-daychangeofeligibility(COE)confirmationsassociatedwithtransactionsthatareeligibletosettle
throughtheDTC,CNSandIDNetserviceofDTCC.TheTradeSuiteIDservicegeneratesaduplicate
confirmationwithaneweligibilitystatuswhenaDTC,CNSandIDNettradeconfirmationeligibility
changesdueto
l SettlementactionstakenbyclearingpartiesatDTCC.
l OthereligibilitychecksperformedbyDTCC.
TheTradeSuiteIDserviceincludesthisinformationinthedesignatedmessagequeue(themailbox).
DeterminethechangeofeligibilitybytheCOELIGvalueintheRecordTypefield,positions3–8ofthe
transactionheaderrecord.
Validation
ThefollowingtableshowsthelegenddescriptionfortheValidationcolumnavailableinthedetailrecord
tables.
ConfirmTradeOutputMessageSpecification
2.FormatSpecifications 12

---

## Page 13

Legend Description
Y TradeSuiteIDfieldvalidationoccurs.
N SubmittersentthedataortheMUNIEnrichmentdatabasereportsthedataasintact(notvalidated).
– TheTradeSuiteIDservicegeneratesthedata.
Table2.2ValidationColumn
ConfirmTradeOutputMessageSpecification
2.FormatSpecifications 13

---

## Page 14

3.OUTPUTRECORDFORMATS
ThissectiondescribestherecordformatsfortheTradeSuiteIDtradeoutputfile.
LegendforAllRecordFormats
Forallrecords,1through6,thefollowingapplies:
l CharacterX(n)—nnumberofalphanumericcharacters,includinga–z,0–9,andspecialcharacters.
l Numeric9(n)—Integercontainingnpositions.Forexample,Numeric9(8):maximumvalueof
99,999,999.Allnumericintegerfieldsareright-justifiedwithleadingzeros.
l Numeric9(x)V9(y)—Fractionalnumbercontainingxpositionstotheleftofthedecimalpointandypos-
itionstotherightoftheimplieddecimalpoint.Forexample,enterNumeric9(12)V9(5):for258.43as:
00000000025843000.Allnumericfieldswithdecimalpositionsareright-justifiedwithleadingandtrail-
ingzeros.
HeaderRecord
OneTradeSuiteIDheaderrecordprecedesadetailrecordorbatchofdetailrecordsforend-of-day
CumulativeEligibleTrade(CUMETR)andUnaffirmed(S1MUAFS1UNAF,orS2UNAF)reports.Table3.1
showsthedetailsoftheheaderrecord.
Position Length Format FieldName Validate FieldDescription
Positions1through26:TransactionHeader
1 1 Character X(1) FeedbackIndicatorN Indicatesthereturnofthisrecordbecause
oferrors.Forafulldescriptionofthis
processing,seetheInterfaceControl
Manager.
l .*=Ifnoerrors
l ?=Ifrecordcontainserrors
2 1 Character X(1) Production/Test
Indicator
Y Indicateswhethertherecordisfor
productionortest.Required.
l P=Production
l T=Test
Table3.1HeaderRecord
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 14

---

## Page 15

Position Length Format FieldName Validate FieldDescription
3–8 6 Character X(6) RecordType Y Typeofdatacontainedinthemessage.
l CUMETR=CumulativeEligible
Tradereport
l S1MUAF=S-1MiddayUnaffirmed
report
l S1UNAF=S-1Unaffirmedreport
l S2UNAF=S-2Unaffirmedreport
9–10 2 Numeric9(2) RecordSuffix Y Recordnumberidentifierbecauseasingle
logicalrecordcancontainmorethanone
record.
l 01=GeneralConfirmRecord
11–12 2 Numeric9(2) VersionNumber Y Versionnumberthatdefinestherecord
format,incrementedbytheTradeSuiteID
servicewhenaddingordeletingfieldsfrom
theformat.
13–18 6 Character X(6) Filler – Reserved.Donotuse.
19–26 8 CharacterX(8) Addressee Y TradeSuiteIDdestinationoftheuserfor
whomtherecordwasproduced,enabling
agroupusertoredistributetherecord.
Positions27–978:TransactionalData
27 1 Character X(1) RecordType Y 0=TradeSuiteIDheaderrecord
28–35 8 CharacterX(8) ReceiverNumber Y Eight-digitIDofreceiverassignedtothe
userreceivingoutput.Right-justified,zero-
filled.
36–41 6 Numeric 9(6) ProcessDate Y Processingdatewhentheoutputwascre-
ated,inMM/DD/YYformat.
42 1 Character X(1) Filler – Reserved.Donotuse.
43–44 2 Character X(02) ReceiverType Y Typeofuserreceivingtheoutput:
01=Institution
02=Agent
03=[[Broker]]/dealer
04=InterestedParty
05=Reserved
06=[[Broker]]/dealerSub-custodian
07=AgentSub-custodian
08=Clearingbroker/dealer
09=ClearingAgent
10=Customer
45–978 934 Character X(934) Filler – Reserved.Donotuse.
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 15

---

## Page 16

TrailerRecord
OneTradeSuiteIDtrailerrecordfollowsonedetailrecordorbatchofdetailrecordsforend-of-day
CumulativeEligibleTrade(CUMETR)andUnaffirmed(S1MUAF,S1UNAF,andS2UNAF)reports.Table
3.2showsthedetailsofthetrailerrecord.
Position Length Format FieldName Validate FieldDescription
Positions1through26:TransactionHeader
1 1 Character X
(1) Feedback
Indicator
N Indicatesthereturnofthisrecordbecause
oferrors.Forafulldescriptionofthis
processing,seetheInterfaceControl
Manager.
l .*=Ifnoerrors
l ?=Ifrecordcontainserrors
2 1 Character X
(1) Production/Test
Indicator
Y Indicateswhethertherecordisfor
productionortest.Required.
l P=Production
l T=Test
3–8 6 Character X
(6) RecordType Y Typeofdatacontainedinthemessage.
l CUMETR=CumulativeEligibleTrade
report
l S1MUAF=S-1MiddayUnaffirmed
report
l S1UNAF=S-1Unaffirmedreport
l S2UNAF=S-2Unaffirmedreport
9–10 2 Numeric9
(2)
RecordSuffix Y Recordnumberidentifier,sincemorethan
onerecordcanbecontainedinasingle
logicalrecord.
l 01=Generalconfirmrecord
11–12 2 Numeric9
(2)
VersionNumber Y Versionnumberthatdefinestherecord
format,incrementedbytheTradeSuiteID
servicewhenaddingordeletingfieldsfrom
theformat.
Table3.2TrailerRecord
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 16

---

## Page 17

Position Length Format FieldName Validate FieldDescription
13–18 6 CharacterX
(6)
Filler – Reserved.Donotuse.
19–26 8 CharacterX
(8)
Addressee Y TradeSuiteIDdestinationoftheuserfor
whomtherecordwasproduced,enabling
agroupusertoredistributetherecord.
Position27–978:TransactionalData
27 1 Character X
(1) RecordType Y 9=TradeSuiteIDtrailerrecord
28–35 8 Character X
(8) ReceiverNumber Y Eight-digitidentifierofuserreceiving
output.Right-justified,zero-filled.
36–37 2 Character X
(2) ReceiverType Y Identifierofthetypeofuserreceivingthe
output.
01=Institution
02=Agent
03=[[Broker]]/dealer
04=Interestedparty
05=Reserved
06=[[Broker]]/dealersub-custodian
07=Agentsub-custodian
08=Clearingbroker/dealer
09=Clearingagent
10=Customer
38–48 9 Numeric9
(9)
RecordCount Y Numberofphysicalrecordsonthefile
includingheaderandtrailerrecords.Right-
justified,zero-filled.
47–63 17 Numeric 9
(12)V9(5)
Quantity Y Sharequantityofentirefile.Right-justified,
zero-filled.
64–77 14 Numeric 9
(12)V99
NetAmount Y Netamountoftheentirefile.Right-
justified,zero-filled.
78–978 901 CharacterX
(901)
Filler – Reserved.Donotuse.
Table3.2TrailerRecord(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 17

---

## Page 18

VersionoftheRecordFormats
TheTradeSuiteIDheaderrecordprecedesthedetailrecordorbatchofdetailrecordsoftheCUMETR,
S1UNAF,S2UNAF,orS3UNAFtypeandfollowedbyaTradeSuiteIDtrailerrecord.Detailrecordsofthe
CONFRMandAOCCNFtypehavenoheaderandtrailerrecords.Formoreinformationaboutheadersand
trailers,seeHeaderRecordandTrailerRecord.
Thedetailrecordsinclude:
l DetailRecord1:GeneralTradeOutput
l DetailRecord2:AdditionalFixedIncomeInformationOutput
l DetailRecord3:AdditionalPartyOutput
l DetailRecord4:Mortgage-BackedSecuritiesOutput
l DetailRecord5:SupplementalOutput
l DetailRecord6:Financing/REPOTransactionOutput
DetailRecord1:GeneralTradeOutput
Table3.3showsthegeneraltradeinformationforoutputmessages.
Position Length Format Field
Name
Validate FieldDescription
Positions1–26:TransactionHeader
1 1 Character X
(1)
FeedbackIndicator N Indicatesthereturnofthisrecordbecauseof
errors.Forafulldescriptionofthis
processing,seetheInterfaceControl
Manager.
l .*=Noerrors.
l ?=Recordcontainserrors.
2 1 Character X
(1)
Production/Test
Indicator
Y Indicateswhetherrecordisforproductionor
test.Required.
l P=Production
l T=Test
Table3.3DetailRecord1:GeneralTradeOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 18

---

## Page 19

Position Length Format Field
Name
Validate FieldDescription
3–8 6 CharacterX
(6)
RecordType Y Typeofdatacontainedinthemessage.
l CONFRM=Confirm
l COELIG=ChangeofEligibility
l CUMETR=CumulativeEligibleTrade
Report
l S1MUAF=S–1MiddayUnaffirmed
Report
l S1UNAF=S–1UnaffirmedReport
l S2UNAF=S–2UnaffirmedReport
l AOCCNF=AdviceofCancellationor
Correction
l RAFCAN=ReverseAffirmation/Disaf-
firmationthroughAdviceofCan-
cellation
l RAFCOR=ReverseAffirmation/
DisaffirmationthroughAdviceofCor-
rection
Note:DisaffirmationonlyappliestoPrime
Brokeraffirmedconfirms.Todistinguish
disaffirmationfromreverseaffirmationuse
theDisaffirmationIndicatorinPosition915.
9–10 2 Numeric9(2) RecordSuffix Y Recordnumberidentifierbecauseasingle
logicalrecordcancontainmorethanone
record.
l 01=GeneralConfirmRecord
11–12 2 Numeric9(2) VersionNumber Y Versionnumberthatdefinestherecord
format.
l VersionNumberalways=01
13–18 6 CharacterX
(6)
Filler – Reserved.Donotuse.
19–26 8 CharacterX
(8)
Addressee Y TradeSuiteID
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 19

---

## Page 20

Position Length Format Field
Name
Validate FieldDescription
Positions27–978:TransactionalData
27 1 Numeric9(1) TransactionType Y Identifiesthetypeofconfirmtransaction.
1=NewConfirm
3=Cancellation
4=Resubmission
6=Affirmation/ConfirmationReversal
Whenthetransactiontypeis6,theRecord
Type(position3–8)populateswithavalueof
RAFCANorRAFCORonoutput.
28 1 Character X
(1)
Filler – Reserved.Donotuse.
29–36 8 Numeric9(8) Executing
[[Broker]]/DealerID
Number
Y ValidTradeSuiteIDnumberofthe
[[Broker]]/dealerwhoexecutedthetrade.Must
beavalidagentTradeSuiteIDnumber.For
example,enter123as00000123.Right-
justified,zero-filled.
37–44 8 Numeric9(8) InstitutionIDNumberY ValidTradeSuiteIDnumberoftheinstitution
orthepartythatplacesthetradeorderwith
thebroker/dealer.Mustbeavalidagent
TradeSuiteIDnumber.Forexample,enter
123as00000123.Right-justified,zero-filled.
45–52 8 Numeric9(8) AgentIDNumber Y ValidTradeSuiteIDnumberoftheagent,
generallyacustodianbank,responsiblefor
receivingordeliveringthesecuritieson
behalfoftheinstitutionoritscustomer.Must
beavalidagentTradeSuiteIDnumber.For
example,enter123as00000123.Right-
justified,zero-filled.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 20

---

## Page 21

Position Length Format Field
Name
Validate FieldDescription
53–64 12 Character X
(12)
SecurityIdentifier Y Securityidentificationnumberassignedto
thetradedsecurity.Whenasecuritynumber
translationoccurs,thisfieldpopulateswith
theconvertedinformationintheSecurity
NumberingSystemfield(position204–205).
l 53–54X(02)=ISINcountrycodefor
ISINonly;otherwise,spaces.
l 55–63X(09)=securitynumber
l 64–64X(01)=ISINcheckdigitforISIN
only;otherwise,spaces.
Left-justified,space-filledtotherightfor
positions55–63whenthesecurityidentifier
islessthan9bytesinlength.FortheISO
countrycodes,seeInput/OutputInformation.
65 1 Numeric9(1) SettlementType Y Indicateshowthetradeistosettle.Regular
Waytradessettleaccordingtolocalmarket
conventions.Forexample,intheU.S.,trades
incorporatesecuritiesandmunicipalbonds
settlethreebusinessdaysafterthetrade
date(T+3).Theinitialpublicoffering([[IPO]])
usesthethreeothercategories.
1=RegularWay
2=When-Issued
3=When-Distributed
4=When-IssuedorWhen-Distributed
66 1 Character X
(1)
Long/ShortIndicatorY .
l L=SellLong
l S=SellShort
l E=SellShortExempt
l Space=Unavailableornotapplicable
Mandatoryfieldforallprimebrokers-sell
trades.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 21

---

## Page 22

Position Length Format Field
Name
Validate FieldDescription
67 1 Character X
(1)
Role Y Identifiestheroleofthebroker/dealerasone
ofthefollowing:
1=Executingbroker/dealeractsasagentfor
thecustomer(AGNT).
2=Executingbroker/dealeractsasprincipal
fortheirownaccount(PRIN).
3=Executingbroker/dealeractsasagentfor
apersonotherthanthecustomer(OTHR).
4=Executingbroker/dealeractsasagentfor
boththecustomerandanotherperson
(CUST).
5=Averagepricetrade;thebroker/dealer
actasprincipalforsomeexecutionsand
agentforothersinthetransaction(AVGR).
6=Executingbroker/dealeractsasboth
principalandagentinthetransaction
(PRAG).
7=Executingbroker/dealeractsasa
principal,agent,andagentforanother
personinthetransaction(PAGC).
8=Crossingasagent–Executing
[[Broker]]/dealeriscrossingtransactionas
agentonbehalfofthecustomer(CAGN).
9=Crossingasprincipal–Executing
[[Broker]]/dealersarecrossingtransactionas
principalfortheirownaccount(CPRN).
A=Actingasrisklessprincipal–Executing
[[Broker]]/dealeristradingasariskless
principal.Thatis,theordertobuy(sell)is
contemporaneouslyoffsetbyanordertosell
(buy)withanotherparty(RISP).
Whenappropriate,theTradeSuiteIDInquiry
screensdisplaycharactervalues,suchas
PRINandAVGR,thatfollowtheexplanation.
Note:Theaveragepriceindicatorusedfor
tradeswherethebroker/dealerfillstheorder
withanumberofsmallerexecutions.When
theaveragepriceistherole,the
[[Broker]]/dealeractsasprincipalforsome
executionsandagentforothersinthe
transaction.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 22

---

## Page 23

Position Length Format Field
Name
Validate FieldDescription
WhenusedintheMarketCodefield(position
68–69),
l AVGPindicatesthattheorderoccurs
overmultipleexecutions.
l AVGRindicatesthattheorderoccurs
acrossmultipleexecutionsinmultiple
exchanges,suchasNYSE,[[NASDAQ]],
andOTC.
Pricesofindividualtradeexecutionsare
availablefromtheexecutingbroker/dealer
uponwrittenrequest.
Note:Toallowformorefieldvalues,the
TradeSuiteIDservicechangedthedata
formatfromNumeric9(1)toAlpha/Numeric–
CharacterX(1).
68–69 2 Character X
(2)
MarketCode Y Marketinwhichthetradewasexecuted.
WhenusedintheMarketCodefield,
AveragePriceindicatesthattheorder
executesovermultiplemarkets,suchas
[[NYSE]],[[NASDAQ]],orOTC.Ifthevalueis
invalid,theTradeSuiteIDservicerejectsthe
record.Foralistofmarketcodes,see
Input/OutputInformation.
70 1 Numeric9(1) SideCode Y Indicateswhethertheinstitutionboughtor
soldtheunderlyingsecurities.
l
1=SELL;[[Broker]]/dealerisreceiving
Iftheinstitutionisselling,the
submittingbroker/dealeristhe
receiverandtheinstitutionofthe
agentisthedeliverer.
l
2=BUY;[[Broker]]/dealerisdelivering
Iftheinstitutionisbuying,the
submittingbroker/dealeristhe
delivererandtheinstitutionofthe
agentisthereceiver.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 23

---

## Page 24

Position Length Format Field
Name
Validate FieldDescription
71–81 11 Numeric 9
(5)V9(6)
NetPrice Y Differencebetweenthequotedpriceandthe
mark-upormark-down(rule10b–10).Right-
justified,zero-filled.
82–98 17 Numeric 9
(12)V9(5)
[[shares]]/FaceValue Y Sharesorfacevalue.Maximumofnine
integerswithleadingzeros.ForaDTC
[[settlement]],thefractioniszero.Right-
justified,zero-filled.
99–109 11 CharacterX
(11)
Price * Y Pricepershareatwhichthissecuritytraded.
Thisfieldcancontainafloatingdecimalin
anyposition;allotherpositionsarenumeric.
Wholenumbersdonotrequireadecimal
point.Right-justified,zero-filled.
110–123 14 Numeric9
(12)V99
PrincipalAmount * Y [[shares]]/facevaluemultipliedbytheprice.
Right-justified,zero-filled.
124–132 9 Numeric9
(7)V99
Registration/
ShippingorFees
Y Registration/shipping(fortradesnotsettling
inUS)orfees(fortradessettlinginUS).
Right-justified,zero-filled.
133–143 11 Numeric9
(9)V99
Interest Y Interestaccruedonabondandaccounted
forinitssale.Right-justified,zero-filled.
144–152 9 Numeric9
(7)V99
ResearchAmount Y Thecostoftheresearchprovidedbythesell-
side.Rightjustified,zerofilled.
Note:ThisMiFIDIIfieldreplacedtheLocal
Taxfield.
153–161 9 Numeric9
(7)V99
CountryTax Y Countryandfederaltaxesthatapplytothis
transaction.Right-justified,zero-filled.
ThisCountryTaxfieldisalsousedforthe
Americandepositaryreceipt([[ADR]])foreign
taxes.
162–170 9 Numeric9
(7)V99
Commission Y Commissioneitherdirectlychargedor
allocatedtothistrade.Right-justified,zero-
filled.
171–179 9 Numeric9
(7)V99
OtherCharges Y Sumofanychargesthatapplytothistrade
forwhichnootherfieldisdesignated.Right-
justified,zero-filled.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 24

---

## Page 25

Position Length Format Field
Name
Validate FieldDescription
180–193 14 Numeric 9
(12)V99
NetAmount * Y Cashsettlementamount,whichisthesumof
theprincipalamountandinterest,plusor
minusthefollowingfields:
l Registration/Shipping/Fees
l Interest
l ResearchAmount
l CountryTax
l Commission
l OtherCharges.
Right-justified,zero-filled.
194–196 3 CharacterX
(3)
ExpandedSecurity
Type
Y Typeofsecuritythatisthesubjectofthe
trade.TheTradeSuiteIDserviceusesthe
securitytypetogeneratesettlement
instructionsfromtheTradeSuiteIDmaster
file.
TheTradeSuiteIDserviceattemptstoobtain
securitydescriptionsandfixedfieldsfromthe
MUNIEnrichmentdatabaseforDTC-eligible
municipalsecuritiesandforanysecuritythe
submitteridentifiesasamunicipalsecurity
(securitytype=MUN).Thisdatareplacesthe
[[Broker]]/dealer'sdata.
Forafulllistofsecuritytypes,see
Input/OutputInformationguide.
197 1 Character X
(1)
AOCCIndicator Y l Y=Yes,Issuedanadviceofcor-
rectionorcancellationforthistrade.
l Space=N/A
Table3.3DetailRecord1:GeneralTradeOutput(continued)
*ThisfieldallowszerosforWhen-IssuedorWhen-Distributedtrades.Forothersettlementtypes,thevalueis
greaterthanzero.
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 25

---

## Page 26

Position Length Format Field
Name
Validate FieldDescription
198 1 Character X
(1)
SplitCurrency
SettlementIndicator
Y Indicateswhensecuritiesandcashsettlein
differentlocations.Usewithsettlement
locationswheresecuritiessettleinone
locationandcashinanotherlocation,either
withinoroutsidethecountryofsecurity
[[settlement]].
l Y=Yes
l N=No
199 1 Character X
(1)
QualityControl
ReportingExempt
Indicator
N Indicateswhethertoexcludetheconfirm
fromtheQualityControlreport.
l Y=excludedfromtheQualityControl
report.
l Anyothervalueornovalue=include
theconfirmintheQualityControl
report.
200 1 CharacterX
(1)
AllocationSource Y [[Broker]]/dealeridentifiesordisclosesthe
sourceorsystemtheinvestmentmanager
usestosendtheallocationtothe
[[Broker]]/dealertoprocessthetrade
confirmation.Ifsupplied,enteroneofthe
followingvalidvalues:
l 1=NA
l 2=TradeXpress(TradeWeb)
l 3=FIX
l 4=MarketAxess
l 5=Manual(phoneorFax)
l 6=USDIviaM2i
l 7=USDMviaM2i
l Space=Notsupplied
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 26

---

## Page 27

Position Length Format Field
Name
Validate FieldDescription
201–203 3 CharacterX
(3)
SettlementLocationY Countryordepositorywherethesecurityisto
settle.Thesettlementlocationsabroadare
bycountry,exceptforEuroclearandCEDEL
(Clearstream).
Herearetheprimaryvalues.
l [[DTC]]=TheDepositoryTrustCompany
l BRC=Brokercustody(DTCtrades
wherebroker/dealerisalsothecus-
todian/agent).
l CED=CEDEL(Clearstream)
l EUR=Euroclear
l FED=TheFederalReserveBankof
NewYork
l NFS=Notforsettlement
l US=U.S.physical
Left-justified,space-filled.Foracompletelist
ofthecountryofsettlement,seeInput/Output
Information.
204–205 2 CharacterX
(2)
SecurityNumbering
System
Y NumberingsystemsameastheSecurity
Identifierfield(positions53–64).Populates
withtheconvertedsecuritynumbering
systemwhenthesecuritynumbertranslation
occurs.Foracompletelist,seeInput/Output
Information.
206–208 3 CharacterX
(3)
CurrencyCode Y Currencyofthesecuritytraded.Ifthetradeis
tosettleinacurrencyotherthanthecurrency
ofthesecurity,reporttheAlternateCurrency
ConversionRatefield(position774).Fora
listofcurrencycodes,seeInput/Output
Information.
209–220 12 CharacterX
(12)
Original
[[Broker]]/Dealer
ConfirmNumber
Y [[Broker]]/dealer’sconfirmnumber,foruse
whentheTransactionTypefield(position27)
is3(cancellation)or4(resubmission);
otherwise,blank.
221–224 4 CharacterX
(4)
Filler – Reserved.Donotuse.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 27

---

## Page 28

Position Length Format Field
Name
Validate FieldDescription
225–230 6 Numeric9(6) TradeDate Y Dateonwhichthetransactionexecutesas
reportedbythebroker/dealer,inMM/DD/YY
format.
231–236 6 Numeric9(6) SettlementDate Y Datewhenthetradeisduetosettle,in
MM/DD/YYformat.
237–314 78 Character X
(78)
SecurityDescription
Line 1 *
N Nameofthesecuritytraded.Fouradditional
78-characterdescriptionsareavailablein
Record2.Fordetailedinformation,seepage
40.
Note:Enrichmentrules,asdefinedin
ConfirmTradeInputMessageSpecification
canaffecttheoutputdata.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
*WhentheExpandedSecurityTypefield(Record1,position194)equalsMUNandthesecurityisDTC-eligible,
thedataobtainedfromtheMUNIEnrichmentprocessreplacesthedatatheExecutingBrokerprovidesforthis
field..
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 28

---

## Page 29

Position Length Format Field
Name
Validate FieldDescription
315–316 2 Numeric9(2) AccountType Y Typeorclassofaccountinwhichthe
[[Broker]]/dealerrecordedthetrade.Allowed
valuesare:
l
02=Cashaccountsthatsettleona
payment-on-delivery(POD)or
collect-on-delivery(COD)basis.
l
05=Shortsaleaccounts.
l
09=Marginaccountsforwhichthe
[[Broker]]/dealerprovidesthefinancing.
l
10=Primebroker/dealeraccounts
whereabroker/dealer,actingasa
clearer,directsotherbroker/dealers
toexecutethetrade.Formore
information,seetheOperating
Procedures.
l
99=Othermiscellaneousaccount
types.
Allfivecategoriesfallwithinrule387/
NASDrule64/MSRBruleG-15andappear
intheQualityControlreport.
317–318 2 Character X
(2)
Filler – Reserved.Donotuse.
319 1 Character X
(1)
PaymentMethod
Indicator
– Paymentmethodindicator.
0=NotApplicable.Thesettlementlocationis
notDTCorbrokercustody.
1=Same-DayFundssettlement.
2=Next-DayFundssettlement.
DeterminedfromtheTradeSuiteIDmaster
fileofeligiblesecurities.
320–322 3 Numeric9(3) Cancellation/
CorrectionReason
Code
Y ReasonforcorrectionorcancellationFora
fulllist,seeInput/OutputInformation.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 29

---

## Page 30

Position Length Format Field
Name
Validate FieldDescription
323–334 12 CharacterX
(12)
AgentInternal
AccountNumber
N Agent'sinternalaccountnumber(AIA).
Limitedtothefirst12charactersoftheAgent
InternalAccountNumber.Spacesare
providedwhennoAgentInternalAccount
Numberisavailable.
335–346 12 CharacterX
(12)
[[Broker]]/Dealer
InternalAccount
Number
N Internalaccountnumberofthebroker/dealer.
Ifunavailable,settospaces.
347–358 12 CharacterX
(12)
[[Broker]]/Dealer
ConfirmNumber
Y [[Broker]]/dealerconfirmnumberthatuniquely
identifieseachtrade.
359–390 32 CharacterX
(32)
SpecialInstruction 1N Free-formtextforthebroker/dealertoaddto
theconfirmation.Forunusedspecial
instructionfields,settospaces.Forspecial
instructionsaboutusingcodesand
informationrelatedto10b–10requirements,
seetheOperatingProcedures.
391–422 32 CharacterX
(32)
SpecialInstruction 2N
423–454 32 CharacterX
(32)
SpecialInstruction 3N
455–486 32 CharacterX
(32)
SpecialInstruction 4N
487–518 32 CharacterX
(32)
SpecialInstruction 5N
519–550 32 CharacterX
(32)
SpecialInstruction 6N
551–582 32 CharacterX
(32)
SpecialInstruction 7N
583–614 32 CharacterX
(32)
SpecialInstruction 8N
615 1 Character X
(1)
DTCSettlement
Mode
– Settlementmode(formerlySettlement
[[Option]])isdeterminedduringtheaffirmation
processing.
Setto0,NotDeterminedbeforeaffirmation.
0=NotDetermined
2=PDQ-DTCSettlement
4=[[CNS]]-NSCCSettlement
6=IDNet
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 30

---

## Page 31

Position Length Format Field
Name
Validate FieldDescription
616–621 6 CharacterX
(6)
ConfirmProcess
Time
– TimewhentheTradeSuiteIDservice
processedtheconfirm,theaffirmationorthe
changeofeligibility(EasternTime),in
HH:MM:SSformat.Usethisfieldwiththe
ConfirmProcessDatefield,positions945–
950todeterminethedateandtimeofthe
confirmdependingontheconfirmstatus.
622 1 Character X
(1)
SecurityFormCode N Securityformcode.
0=Undeterminedsecurityformcode
1=Notbearerbond
2=Bearerbond
623–630 8 Numeric9(8) InterestedParty #1
IDNumber *
Y Customer,interestedparty,orsub-custodian
(determinedbytheInterestedParty#1Type
field,position819).
Sub-custodiancanappearfortradesthatdo
notsettleatDTC.Zero-filledwhenthereisno
interestedpartynumber1.Right-justified,
zero-filled.
631–642 12 Character X
(12)
InterestedParty #1
AccountNumber *
N Accountnumberoftheinterestedparty
number1.
643–667 25 CharacterX
(25)
InterestedParty #1
InstructionLine 1
N Line1oftextappearsonInstructionLine1of
theconfirmationassociatedwithinterested
partynumber1.Thisfieldisusuallyforthe
beneficialnameoftheaccount.Free-form
text.
668–692 25 CharacterX
(25)
InterestedParty #1
InstructionLine 2
N Line2oftextappearsonInstructionLine2of
theconfirmationassociatedwithinterested
partynumber1.Thisfieldisusuallyforthe
beneficialnameoftheaccount.Free-form
text.
693–700 8 Numeric9(8) InterestedParty #2
IDNumber *
Y Customer,interestedparty,orsub-custodian
(determinedbyinterestedpartynumber2
Type,position820).Sub-custodiancan
appearfortradesthatdonotsettleatDTC.
Zero-filledwhenthereisnointerestedparty
number2.Right-justified,zero-filled.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 31

---

## Page 32

Position Length Format Field
Name
Validate FieldDescription
701–712 12 CharacterX
(12)
InterestedParty #2
AccountNumber *
N Interestedpartynumber2accountnumber.
713–737 25 CharacterX
(25)
InterestedParty #2
InstructionLine 1
N Line1oftextappearsonInstructionLine1of
theconfirmationassociatedwithinterested
partynumber2.Thisfieldisusuallyforthe
beneficialnameoftheaccount.Free-form
text.
738–762 25 CharacterX
(25)
InterestedParty #2
InstructionLine 2
N Line2oftextappearsonInstructionLine2of
theconfirmationassociatedwithinterested
partynumber2.Thisfieldisusuallyforthe
beneficialnameoftheaccount.Free-form
text.
763–771 9 CharacterX
(9)
DTCControlNumber– NumberassignedbytheTradeSuiteIDser-
vicetoabroker/dealer'strade.Thisnumber
canalsobeusedtoassociatethisrecordwith
itsotherrecords.TheDTCControlNumbers
arerecycledbasedonoveralltradeactivity.
772–773 2 CharacterX
(2)
Transaction
SequenceNumber
– Sequencenumberassignedbythe
TradeSuiteIDservicetoindicatewhether
morerecordsareassociatedwiththisrecord.
11=Oneofone
12=Oneoftwo
13=Oneofthree
14=Oneoffour
15=Oneoffive
16=Oneofsix
774–783 10 Numeric 9
(5)V9(5)
AlternateCurrency
ConversionRate
Y Conversionrateforthealternatecurrency
specifiedfortheconfirm,whenspecified.If
unused,zero-filled.
Conversionrateused:
l Forinformationpurposeswiththe
alternatecurrencycode.
l Forsettlementpurposeswithboththe
AlternateCurrencyISOCodeand
AlternateCurrencyNetAmountfields.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
*Whenmatchingatrade,theALERT®servicecanfillorreplacethedatainthisfield.
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 32

---

## Page 33

Position Length Format Field
Name
Validate FieldDescription
784–786 3 CharacterX
(3)
AlternateCurrency
ISOCode
Y Ifthetradeistosettleinacurrencydifferent
fromthecurrencyofthesecurity(Currency
Codefield,positions206–208),usethisfield.
Usethisfieldforinformationpurposeswith
theAlternateCurrencyConversionRate
field,position774–783.
IftheAlternateCurrencyConversionRate
andAlternateCurrencyNetAmountare
zeros,enterspaces.Otherwise,enteravalid
ISOcurrencycode.Forafulllist,seethe
Input/OutputInformation.
Tocommunicateonlyaforeignexchange
raterelativetothetrade,usetheAlternate
CurrencyISOCodefieldwiththeAlternate
CurrencyConversionRatefield,positions
774–783.Ifthesecuritytradedisdifferent
fromthelistedcurrencyforthesettlement,
completeallthreealternatefields,positions
774–783,784–786,and787–800.
787–800 14 Numeric 9
(12)V99
AlternateCurrency
NetAmount
Y Alternatecurrencynetamount,coupledwith
thealternatecurrencyISOcode,designates
thesettlementamountwhendifferentfrom
thecurrencyofthesecurity.Zero-filledwhen
thesecurityistosettleinthecurrencyshown
inposition206–208.
801–818 18 Numeric 9
(6)V9(12)
Amortized/
AccreditedFactor
Y Prorationoftheoutstandingprincipal
balanceonpass-throughGinnieMae,
FreddieMac,FannieMae,andmortgage-
backedsecuritytoitsoriginalprincipal
balanceexpressedasadecimal.Right-
justified,zero-filled.
819 1 Character X
(1)
InterestedParty #1
Type
– Typeofinterestedpartynumber1.Typea
spaceifthereisnointerestedpartynumber
1.
l C=Customer
l P=Interestedparty
l B=[[Broker]]/dealersub-custodian
l A=Agentsub-custodian
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 33

---

## Page 34

Position Length Format Field
Name
Validate FieldDescription
820 1 Character X
(1)
InterestedParty #2
Type
– Typeofinterestedpartynumber2.Typea
spaceifthereisnoInterestedparty#2.
l C=Customer
l P=Interestedparty
l B=[[Broker]]/dealersub-custodian
l A=Agentsub-custodian
821 1 Character X
(1)
InterestedParty #3
Type
– Typeofinterestedpartynumber3.Typea
spaceifthereisnoInterestedparty#3.
l C=Customer
l P=InterestedParty
l B=[[Broker]]/dealersub-custodian
l A=Agentsub-custodian
822–829 8 NumericX(8) InterestedParty #3
IDNumber*
Y IDnumberforthecustomer,interestedparty,
orsub-custodian(determinedbythe
InterestedParty#3Typefield,position821).
Zero-filledwhennointerestedpartynumber
3.Sub-custodiancanappearfortradesthat
settleawayfromDTC.Right-justified,zero-
filled.
830–841 12 CharacterX
(12)
InterestedParty #3
AccountNumber*
N Accountnumberforinterestedpartynumber
3.Thesub-custodiancanappearfortrades
thatsettleawayfromDTC.
842–866 25 CharacterX
(25)
Interested Party #3
InstructionLine 1
N Line1oftexttoappearontheconfirmation
associatedwithinterestedpartynumber3.
Thesub-custodiancanappearfortradesthat
settleawayfromDTC.
Ifabroker/dealerenrichesatradefromthe
inSITE™service,theinSITEserviceURL
populatesthisfield.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
*Whenmatchingatrade,theALERTservicecanfillorreplacethedatainthisfield.
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 34

---

## Page 35

Position Length Format Field
Name
Validate FieldDescription
867–891 25 CharacterX
(25)
InterestedParty #3
InstructionLine 2
N Line2oftexttoappearontheconfirmation
associatedwiththeInterestedParty#3Type
field,position821.Sub-custodiancan
appearfortradesthatsettleawayfromDTC.
IfabrokerenrichesatradefromtheinSITE,
theinSITEbrokerdisclosurereference
numberpopulatesthisfield.
892–909 18 CharacterX
(18)
InstitutionContact – Phonenumberofthecontactattheinstitution
tocalltoresolveaffirmationproblems.Use
thisfieldwithunaffirmedreports.
910 1 Character X
(1)
Filler – Reserved.DonotUse.
Note:WiththeeliminationofSID,thisfieldis
nolongerused.
911 1 Character X
(1)
CancellationAfter
Acknowledged
– Indicatesanattempttocancelthetradeafter
matchingoraffirmation.
l Y=Cancellationattemptedafter
matchingoraffirmation
l Space=N/A
912 1 Character X
(1)
MatchedIndicator – Indicateswhetherthetradeisintendedfor
matchingtoinstitutioninstructionsand
whetherithasmatched.
0=Notintendedformatching
1=Intendedformatching,butunmatched
2=Tradehasmatched
UsedwithAffirmingPartyIndicator(position
953)toobtaincompletematchingand
affirmationstatus.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 35

---

## Page 36

Position Length Format Field
Name
Validate FieldDescription
913 1 Numeric9(1) DTCEligibility
Indicator
– Indicateswhethertheissuetradediseligible
forDTCsettlement.
0=Notapplicable
1=Eligible
2=Ineligible
3=Lateaffirm(eligibletradeaffirmedafterS-
1=settleex-TradeSuiteID)
ForsecuritiessettlingawayfromDTC,0=
notapplicableapplies.ForDTC-eligible
[[securities]],theconfirmationcanshow2=
Ineligible.Foralistofeligibilityreasoncodes,
seetheEligibilityReasonCodesfield,
position916–925.
914 1 Character X
(1)
AccountFound
Indicator
– Indicateswhethertheaccountwasfound.
l Y=Accountfound,tradeoutput
enrichedbytheALERT®service
l N=Accountnotfound,tradeinput
usedexclusively
915 1 Character X
(1)
Disaffirmation
Indicator
– l Y=Tradedisaffirmedbytheprime
[[Broker]]/dealer
l Spaces=N/A
916–925 10 Numeric9
(10)
EligibilityReason
Codes
– Ten-positionnumericfieldcontainingall
tradeeligibilitymessagespertainingtothis
trade.Thisareahasfivecontinuous2-
positioncodes.
Showsthereasonsfortheineligibility.When
theconfirmisineligible,thisfieldcontainsthe
reasonsfortheineligibility.Providesupto
fivereasonsusingthetwo-character
ineligibleconfirmationcodesapplicable.For
afulllistofeligiblecodes,seethe
Input/OutputInformation.
926–932 7 CharacterX
(7)
MatchingVariance – Differencebetweenthenetamountofthis
tradeandthenetamountonthematching
allocation.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 36

---

## Page 37

Position Length Format Field
Name
Validate FieldDescription
933 1 Character X
(1)
VarianceDirection – Indicatesthevariancedirection.
l I=Allocationnetamountgreaterthan
[[Broker]]/dealertradeinput.
l B=[[Broker]]/dealertradeinputnet
amountgreaterthaninstitutionnet
amount.
l Spaces=Institutionnetamount
equalsbroker/dealernetamountor
confirmnotintendedformatching.
934 1 Character X
(1)
DesignatedAffirming
PartyType *
– Identifieswhichpartycanaffirmthetrade.
l B=Institutionoragent
l I=Institution
l A=Agent
l P=Interestedparty
l C=Customer
935–942 8 Numeric9(8) DesignatedAffirming
PartyNumber *
– IDnumberoftheinterestedpartyor
customerthatisaffirmingthetrade.Thisfield
containszeroswhentheinstitutionoragent
isaffirmingthetrade.
943–944 2 CharacterX
(2)
Filler – Reserved.Donotuse.
945-950 6 Numeric9(6) ConfirmProcess
Date
– Datewhenthistradewasinitiallyprocessed
oraffirmedorwhenchangeofeligibility
occurred,inMM/DD/YYformat.
Clientscanusethisfieldinadditiontothe
ConfirmProcessTimefield(positions616–
621)todeterminethedateandtimeofthe
confirmdependingontheconfirmstatus.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
*Whenmatchingatrade,theALERTservicecanfillorreplacethedatainthisfield.
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 37

---

## Page 38

Position Length Format Field
Name
Validate FieldDescription
951–952 2 Numeric9(2) ReportReceiver
Type
– Identifierofintendedreportrecipient:
01=Institution
02=Agent
03=[[Broker]]/dealer
04=Interestedparty
05=Reserved
06=[[Broker]]/dealersub-custodian
07=Agentsub-custodian
08=Clearingbroker/dealer
09=Clearingagent
10=Customer
953 1 Numeric9(1) AffirmingParty
Indicator
– Usedintheaffirmedandmatched/affirmed
confirmationstoindicatethepartythathas
affirmedthetrade.
0=Tradenotyetaffirmed(confirmation
stage).
1=Tradeaffirmedbytheagent
2=Tradeaffirmedbytheinstitution.
3=Noaffirmingpartyspecified.Trade
affirmedbytheagentasdeterminedbythe
TradeSuiteIDservice.
4=Noaffirmingpartyspecified.Trade
affirmedbytheinstitutionasdeterminedby
theTradeSuiteIDservice.
5=Tradeaffirmedbythecustomeror
interestedparty.
UsedwiththeMatchedIndicatorfield
(position912)toobtaincompletematching
andaffirmationstatus.
954–961 8 Numeric9(8) Clearing
[[Broker]]/DealerID
Number
– Eight-digitidentifierofthebroker/dealer’s
clearer.IfthesettlementlocationisDTC,this
fieldcontainstheDTCparticipantnumber;
otherwise,itcontainsthebroker/dealerID
number.Right-justified,zero-filled.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 38

---

## Page 39

Position Length Format Field
Name
Validate FieldDescription
962–969 8 Numeric9(8) ClearingAgentID
Number
– Eight-digitidentifieroftheagent'sclearer.If
thesettlementlocationisDTC,thisfield
containstheDTCparticipantnumber;
otherwise,itcontainsthebroker/dealerID
number.Right-justified,zero-filled.
970 1 Numeric9(1) SecurityDescription
Type
– Sourceofsecuritydescriptions.
0=Nosecuritydescription
1=[[Broker]]/dealertradeinput
2=MUNI enrichmentdatabase
3=TheDepositoryTrustCompany
971–978 8 CharacterX
(8)
IDNetNumber N IDNetnumber(formerlyDepositoryThird-
Party).Populatedwiththeomnibusaccount
719or919usedforprocessingIDNet
eligibletrades.
Table3.3DetailRecord1:GeneralTradeOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 39

---

## Page 40

DetailRecord2:AdditionalFixedIncomeInformation
Output
Table3.4showstheadditionalfixedincomeinformationforoutputmessages.
Position Length Format FieldName Validate FieldDescription
Positions1–26:TransactionHeader
1 1 Character X(1) FeedbackIndicator N Indicatesthereturnofthisrecordbecause
oferrors.Forafulldescriptionofthis
processing,seetheInterfaceControl
Manager.
l .*=Ifnoerrors.
l ?=Iftherecordcontainserrors.
2 1 Character X(1) Production/TestIndic-
ator
Y Indicateswhethertherecordisfor
productionortest.Required.
l P=Production
l T=Test
3–8 6 CharacterX(6) RecordType Y Typeofdatathemessagecontains.
l CONFRM=Confirm
l COELIG=ChangeofEligibility
l CUMETR=CumulativeEligible
TradeReport
l S1MUAF=S-1MiddayUnaffirmed
Report
l S1UNAF=S-1UnaffirmedReport
l S2UNAF=S-2UnaffirmedReport
9–10 2 Numeric9(2) RecordSuffix Y Identifiesthephysicalrecordnumber.
l 02=Municipal/NameRecord
11–12 2 Numeric9(2) VersionNumber Y Versionnumberthatdefinestherecord
format.
l Versionnumberalwaysequals01.
13–18 6 CharacterX(6) Filler – Reserved.Donotuse.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 40

---

## Page 41

Position Length Format FieldName Validate FieldDescription
19–26 8 CharacterX(8) Addressee Y TheTradeSuiteIDdestinationoftheuser
forwhomtherecordwasproduced,
enablingagroupusertoredistributethe
record.
Positions27–978:TransactionalData
27 1 Character X(1) Filler – Reserved.Donotuse.
28–105 78 Character X
(78)
SecurityDescription
Line 2
N Additionalinformation(upto78
charactersoffree-formtextineachfield)
forthesecuritytradedforsecurity
descriptionpurposes.
Note:Enrichmentrules,asdefinedin
ConfirmTradeInputMessage
Specification,canaffecttheoutputdata.
Issuerandissueelementsthatcanbe
segmentedintotwomore78-character
fields.Theseelementsaremergedwith
the78-characterdescriptionfromthefirst
detailrecord.Theelementscouldinclude:
l Nameofissuer
l Issuerlocation
l Titleofcompany
l Descriptionofobligororlienpos-
ition
l Revenuetypeandallotherapplic-
ableMunicipalSecuritiesRule-
makingBoard(MSRB)data
elements,asrequired
106–183 78 CharacterX
(78)
SecurityDescription
Line 3
N
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 41

---

## Page 42

Position Length Format FieldName Validate FieldDescription
184–261 78 CharacterX
(78)
SecurityDescription
Line 4
N Twoadditional78-charcterfieldsforthe
ExecutingBrokertoprovidefreeform
text.
ThefirstthreelinesoftheSecurity
Descriptionfieldcontaindatefurnished
byDTCorobtainedfromtheMUNI
Enrichmentprocess.Thebroker/dealer
canuselines4and5forextra
information.Ifsecuritydescriptionsare
unavailablefromothersources,the
[[Broker]]/dealercanuseallfivelinesfor
thesecuritydescription.
Free-formtext.
262–339 78 CharacterX
(78)
SecurityDescription
Line 5
N
340–344 5 Numeric 9
(2)V9(3)
DiscountRate1 N Rateatwhichthetradewasdiscounted.
Note:Thisfieldisnotincludedinthe
MUNIEnrichmentprocess.Thebrokeris
expectedtoprovideaDiscountRate,if
applicable.
345
1 Character X(1) Filler – Reserved.Donotuse.
346 1 Character X(1) LegalStatus2 N LegalStatusorOpinion:
0=Undetermined/nolegalstatus
1=MSRBex-legal
Note:Thisfieldisnotincludedinthe
MUNIEnrichmentprocess.Thebrokeris
expectedtoprovideaLegalStatus,if
applicable.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
1Zero-filledifnumeric(denoted9…)orspace-filledifalphanumeric(denotedX…)forallsecuritytypesother
thanDTC-eligiblemunicipalsorsecuritytypesmanuallydefinedasmunicipals.OccurswhentheMUNIisinputas
theExpandedSecurityType,inposition194ofthefirstrecord.
2Zero-filledifnumeric(denoted9…)orspace-filledifalphanumeric(denotedX…)forallsecuritytypesother
thanDTC-eligiblemunicipalsorsecuritytypesmanuallydefinedasmunicipals.OccurswhentheMUNIisinputas
theExpandedSecurityType,inposition194ofthefirstrecord.
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 42

---

## Page 43

Position Length Format FieldName Validate FieldDescription
347 1 Character X(1) PaymentStatus 1 N PaymentStatus:
0=Undetermined/nopayment
1=Noperiodicpayments
2=Callablebelowmaturityvalue
3=Non-registeredsecurity
4=Noperiodicpayments,callablebelow
maturityvalue
Note:Thisfieldisnotincludedinthe
MUNIEnrichmentprocess.Thebrokeris
expectedtoprovideaPaymentStatus,if
applicable.
348 1 Character X(1) BondTypeCode 1 N BondTypeCode:
0=Undetermined/nobondtype
1=Generalobligation
2=Revenuebond
3=G.O./limitedtax
Note:Thisfieldisnotincludedinthe
MUNIEnrichmentprocess.Thebrokeris
expctedtoprovideaBondTypeCode,if
applicable.
349 1 Character X(1) BasisIndicator1 N BasisIndicator:
0=Undetermined/Nobasis
1=Yieldbasis
2=Dollarbasis
3=Parbasis
4=Discountbasis
Note:Thisfieldisnotincludedinthe
MUNIEnrichmentprocess.Thebrokeris
expectedtoprovideaDiscountRate,if
applicable.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 43

---

## Page 44

Position Length Format FieldName Validate FieldDescription
350–351 2 CharacterX(2) ResultIndicator 1 N ResultIndicator:
00=Undetermined/noresult
01=Pricetocall
02=Pricetoparoption
03=Pricetomaturity
04=Yieldtocall
05=Yieldtoparoption
06=Yieldtomaturity
07=Parbasis
Note:Thisfieldisnotincludedinthe
MUNIEnrichmentprocess.Thebrokeris
expectedtoprovideaResultIndicator,if
applicable.
352–357 6 CharacterX(6) InterestAccrual
Date 1
N Interestaccrualdate,inMMDDYYformat.
358–363 6 CharacterX(6) InterestPayment
Date 1
N Interestpaymentdate,inMMDDYY
format.
364–368 5 Numeric9
(2)V9(3)
InterestRate 1 N IftheSpecialCouponIndicatorfield
(position406)fromtheMUNIEnrichment
databaseequals0(Nospecialcoupon)or
3(Adjustablerate),theTradeSuiteID
serviceusesthebroker/dealersupplied
valuefortheinterestrateinsteadofthe
valueobtainedfromtheMUNIEnrichment
process.
Ifthebroker/dealerdoesnotsupplydata,
theTradeSuiteIDserviceusesthedata
obtainedfromtheMUNIEnrichment
process,regardlessofthisindicator.
369–374 6 CharacterX(6) MaturityDate 1 N Dateonwhichtheprincipalamountofthe
securitybecomesdueandpayablebythe
[[issuer]],inMMDDYYformat(10b–10field).
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 44

---

## Page 45

Position Length Format FieldName Validate FieldDescription
375–376 2 CharacterX(2) MSRBOptionCall
Indicator 1
N OptionCallofRedemptionIndicator:
00=Undetermined/nooptionalcall
01=Callableatapremium
02=Callableatpar
03=Callableatadiscount
04=Pre-refunded
05=Escrowedtomaturity
06=Noncallable
07=Callable,featureunavailable(10b–
10field)
377 1 CharacterX(1) MSRB Call/Put
FeatureIndicator 1
N Call/PutFeatureIndicator:
0=Undetermined/NoCall/PutFeatures
1=Callable
2=Puttable
3=Callableandputtable
4=Retired(bondcompletelycalled)
378–379 2 CharacterX(2) MSRBPutBond
Type 1
N PutBondType:
00=Undetermined/noputbondtype
01=Conditionalput
02=Limitedput
03=Optionalput
04=Mandatoryrepurchase
05=Mandatoryput
380–385 6 CharacterX(6) PrerefundedorCall
Date 1
N Prerefundeddateormaturitydatefixedby
callnotice,inMMDDYYformat(10b–10
field).
386–391 6 Numeric(3)V9
(3)
PrerefundedorCall
Price 1
N Amountoftheprerefundedorcallprice
(10b–10field).
392–397 6 CharacterX(6) PutBondDate 1 N Maturitydatefixedbyputnotice,in
MMDDYYformat.
398–403 6 Numeric(3)V9
(3)
PutBondPrice 1 N Amountoftheputbondprice.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
1
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 45

---

## Page 46

Position Length Format FieldName Validate FieldDescription
404 1 CharacterX(1) MSRBBondForm
Code 1
N BondFormCode:
0=Undetermined/NoBondForm
1=Fullyregistered
2=Book-entryonly
3=Registeredastoprincipalonly
4=Custodialreceipts
405 1 CharacterX(1) MSRBInterest
PaymentFrequency 1
N InterestPaymentFrequency
0=Undeterminedfrequency
1=Annual
2=Semi-annual
3=Quarterly
4=Monthly
5=Weekly
6=Biweekly
7=Interestatmaturity
8=Noperiodicinterest
9=Unknown
406 1 CharacterX(1) MSRBSpecial
CouponIndicator 1
N SpecialCouponIndicator:
0=Undetermined/nospecialcoupon
1=Zerocoupon
2=Originalissuediscount
3=Adjustablerate
4=Couponbearing
5=Steppedcoupon
407 1 CharacterX(1) MSRBFlat/[[default]]
Status 1
N Flat/DefaultStatus 
0=Undetermined/noflat/defaultstatus
1=Flat
2=Flat/indefault
408 1 CharacterX(1) MSRBTaxStatus N TaxStatus:
0=Undetermined/notaxstatus
1=Taxable
2=Non-taxable
409–411 3 CharacterX(3) Filler – Reserved.Donotuse.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
1.
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 46

---

## Page 47

Position Length Format FieldName Validate FieldDescription
412–413 2 CharacterX(2) Moody’sCreditRating
1
N Moody'sCreditRating.
Foralistofvalues,seeInput/Output
Information.
414–416 3 CharacterX(3) Filler – Reserved.Donotuse.
417–418 2 CharacterX(2) Standard&Poor’s
CreditRating 1
N Standard&Poor'sCreditRating.
Foralistofvalues,seeInput/Output
Information.
419 1 CharacterX(1) MSRBSubjectto
FederalTax 1
N SubjecttoFederalTax":
l 0orspaces=Undetermined
l Y=Yes
l N=No
Note:TheMUNIEnrichmentprocess
doesnotprovideavalueforthisfield,so
itisalwayssetto0(undetermined)
whentheExecutingBrokerdoesnot
provideavalue.
420 1 CharacterX(1) MSRB Alternate
MinimumTax 1
N AlternateMinimumTax:
l 0orspaces=Undetermined
l Y=Yes
l N=No
Note:TheMUNIEnrichmentprocess
doesnotprovideavalueforthisfield,so
itisalwayssetto0(undetermined)
whentheExecutingBrokerdoesnot
provideavalue.
421–460 40 CharacterX
(40)
InstitutionName – Institutionnameasitappearsonthe
TradeSuiteIDservicemasterfile.
461–500 40 CharacterX
(40)
AgentName – Nameoftheagentasitappearsinthe
TradeSuiteIDservicemasterfile.
501–540 40 CharacterX
(40)
Executing
[[Broker]]/DealerName
– Nameoftheexecutingbrokerdealerasit
appearsintheTradeSuiteIDservice
masterfile.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
1
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 47

---

## Page 48

Position Length Format FieldName Validate FieldDescription
541–580 40 CharacterX
(40)
Clearing
[[Broker]]/DealerName
– Nameoftheclearingbroker/dealerasit
appearsintheTradeSuiteIDservice
masterfile.
581–620 40 CharacterX
(40)
ClearingAgentName – Nameoftheclearingagentasitappears
intheTradeSuiteIDservicemasterfile.
621–660 40 CharacterX
(40)
InterestedParty #1
Name
– Interestedparty#1’snameasitappears
intheTradeSuiteIDservicemasterfile.
661–700 40 CharacterX
(40)
InterestedParty #2
Name
– Interestedparty#2’snameasitappears
intheTradeSuiteIDservicemasterfile.
701–740 40 CharacterX
(40)
InterestedParty #3
Name
– Interestedparty#3’snameasitappears
intheTradeSuiteIDservicemasterfile.
741–742 2 CharacterX(2) OriginalInputSecurity
NumberingSystem
– Securitynumberingsystemusedonthe
tradeinput.Thisfieldremainsblankinthe
absenceofsecuritynumbertranslation
processing.Forentries,seeInput/Output
Information.
743–754 12 CharacterX
(12)
OriginalInputSecurity
Identifier
Y Securityidentifierusedonthetradeinput.
Thisfieldremainsblankintheabsenceof
securitynumberprocessing.
l 743–744X(2)ISINcountrycode
onlyforISIN
l 745–753X(9)SecurityNumber
l 754X(1)ISINCheckDigit
Whenusingthesecuritynumbering
translation,thisfieldcontainstheOriginal
InputSecurityIdentifier.Left-justified,
space-filledtotherightforcaseswhere
theidentifier(position745–753)isless
than9bytes.Forthelengthofeachtype
ofsecurityidentifier,seeInput/Output
Information.
755–762 8 CharacterX(8) Filler – Reserved.Donotuse.
763–771 9 CharacterX(9) DTCControlNumber– NumberassignedbytheTradeSuite
[[ID]] servicetoabroker/dealer'strade.This
numbercanalsobeusedtoassociatethis
recordwithitsotherrecords.The
[[DTC]] ControlNumbersarerecycledbased
onoveralltradeactivity.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 48

---

## Page 49

Position Length Format FieldName Validate FieldDescription
772–773 2 CharacterX(2) Transaction
SequenceNumber
– Sequencenumberassignedby
TradeSuiteIDtoindicatewhethermore
recordsareassociatedwiththisrecord.
22=Twooftwo
23=Twoofthree
24=Twooffour
25=Twooffive
26=Twoofsix
774–775 2 CharacterX(2) [[CUSIP]]/CINSSecurity
NumberingSystem
– PopulatedwiththeCUSIP/CINSsecurity
numberingsystemwhenevertheprimary
SecurityNumberingSystemfieldin
record1,position204–206isavalue
otherthanCUSIP/CINS.Thisfield
containsaconstantvalueofUSorblankif
aCUSIP/CINSdoesnotexist.
776–787 12 CharacterX
(12)
[[CUSIP]]/CINSSecurity
Identifier
– PopulatedwiththeCUSIP/CINSsecurity
identifierwhenevertheprimarySecurity
NumberingSystemfieldinrecord1,
position204–206isavalueotherthana
[[CUSIP]]/CINSandthereisa
correspondingCUSIP/CINSnumber.
Thisfieldremainsblankwhenthe
[[CUSIP]]/CINSdoesnotexist.
l 776–777X(2)USorblank
l 778–786X(9)SecurityNumber
l 787X(1)ISINCheckDigit
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 49

---

## Page 50

Position Length Format FieldName Validate FieldDescription
788–798 11 CharacterX
(11)
CurrentYield N Informationforthebroker/dealerto
disclosethecurrentyieldofthefixed
incomesecurityinvolvedinthe
transaction.
Expectedcharactersincludenumbers(0
through9),onedecimalpoint,andeither
oneplus(+)orminus(-)indicatorinthe
rightmostposition.Cancontainafloating
decimalinanyposition;allotherpositions
arenumeric.Wholenumbersdonot
requireadecimalpoint(10b–10field).If
thereisnoembeddeddecimal,
TradeSuiteIDassumesawholenumber.
Ifnotsupplied,thisfieldallowsspaces.
Numericonlyvalues,ifsupplied.Valid
examplesare:
l 008.897000-
l 002.097000-
Right-justified,zero-filled.
Note:Thisfieldwillbevalidatedinthe
future.Enforcementwilloccuratalater
date.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 50

---

## Page 51

Position Length Format FieldName Validate FieldDescription
799–809 11 CharacterX
(11)
YieldtoMaturity N Informationforthebroker/dealerto
disclosetheyieldtomaturityofthefixed
incomesecurityinvolvedinthe
transaction.
Expectedcharactersincludenumbers(0
through9),onedecimalpoint,andeither
oneplus(+)orminus(-)indicatorinthe
rightmostposition.Thisfieldcancontaina
floatingdecimalinanyposition;allother
positionsarenumeric.Wholenumbersdo
notrequireadecimalpoint(10b–10field).
Ifnotsupplied,thisfieldallowsspaces.
Ifsupplied,numericonlyvalues.Valid
examplesare:
l 008.897000-
l 002.097000-
Right-justified,zero-filled.
Note:Thisfieldwillbevalidatedinthe
future.Enforcementwilloccuratalater
date.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 51

---

## Page 52

Position Length Format FieldName Validate FieldDescription
810–820 11 CharacterX
(11)
YieldtoCall/
Redemption
– Informationforthebroker/dealerto
disclosetheyieldtocall/redemptionofthe
fixedincomesecurityinvolvedinthe
transaction.Expectedcharactersinclude
numbers(0through9),onedecimalpoint,
andeitheroneplus(+)orminus(-)
indicatorintherightmostposition.This
fieldcancontainafloatingdecimalinany
position;allotherpositionsarenumeric.
Wholenumbersdonotrequireadecimal
point(10b–10field).Ifthereisno
embeddeddecimal,TradeSuiteID
assumesawholenumber.Ifnotsupplied,
thisfieldallowsspaces.
Expectedcharactersincludenumbers
(0through9),onedecimalpoint,and
eitheroneplus(+)orminus(-)indicator
intherightmostposition.Thisfieldcan
containafloatingdecimalinany
position;allotherpositionsarenumeric.
Wholenumbersdonotrequirea
decimalpoint(10b–10field).
Ifnotsupplied,thisfieldallowsspaces.
Ifsupplied,numericonlyvalues.Valid
examplesare:
l 008.897000-
l 002.097000-
Right-justified,zero-filled.
Note:Thisfieldwillbevalidatedinthe
future.Enforcementwilloccuratalater
date.
821–828 8 CharacterX(8) DatedDate – Informationforthebroker/dealerto
identifythedateddateofthefixedincome
securityinvolvedinthetransaction,in
YYYYMMDDformat.Ifsupplied,entera
validdate.
829-878 50 CharacterX
(50)
FINRAMSRBEMMA
URL
N ThisfieldcontainstheURLlinktothe
URL intheappropriatewebsites:
[[FINRA]] orMSRB.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 52

---

## Page 53

Position Length Format FieldName Validate FieldDescription
879-910 32 CharacterX
(32)
SpecialInstructions
Line19
N AdditionalSpecialInstructionfree-form
textUsefree-formtexttoincludeinform-
ationaboutthefrontoftheconfirmwhere
nodefinedfieldsexist.Thisinformation
includescontactnames,taxIDs,phone
numbers,10b–10information,fin-
ancing/REPOtransactionadditional
information,orconfirmbackeritems.
911-942 32 CharacterX
(32)
SpecialInstructions
Line20
N
943-974 32 CharacterX
(32)
SpecialInstructions
Line21
N
975-978 4 CharacterX(4) Filler – Reserved.Donotuse.
Table3.4DetailRecord2:AdditionalFixedIncomeInformation(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 53

---

## Page 54

DetailRecord3:AdditionalPartyOutput
Table3.5showstheadditionalpartyinformationforoutputmessages.
Position Length Format FieldName Validate FieldDescription
Positions1–26:TransactionHeader
1 1 CharacterX(1) FeedbackIndicatorN Indicatesthereturnofthisrecord
becauseoferrors.Forafulldescription
ofthisprocessing,seetheInterface
ControlManager.
l .*=Ifnoerrors.
l ?=Iftherecordcontainserrors.
2 1 CharacterX(1) Production/Test
Indicator
Y Indicateswhethertherecordisfor
productionortest.Required.
l P=Production
l T=Test
3–8 6 CharacterX(6) RecordType Y Typeofdatacontainedinthemessage.
l CONFRM=Confirm
l COELIG=ChangeofEligibility
9–10 2 Numeric9(2) RecordSuffix Y Identifiesthephysicalrecordnumber
becauseasinglelogicalrecordcan
containmorethanonerecord.
l 03=AdditionalPartyOutput
11–12 2 Numeric9(2) VersionNumber Y Versionnumberthatdefinestherecord
format.
l VersionNumberalways=01
13–18 6 CharacterX(6) Filler – Reserved.Donotuse.
19–26 8 CharacterX(8) Addressee Y TradeSuiteIDdestinationoftheuser
forwhomtherecordwasproduced,
enablingagroupusertoredistribute
therecord.
Positions27–978:TransactionalData
27 1 CharacterX(1) Filler – Reserved.Donotuse.
Table3.5DetailRecord3:AdditionalPartyOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 54

---

## Page 55

Position Length Format FieldName Validate FieldDescription
28–43 16 CharacterX(16) Clearing
[[Broker]]/Dealer
InternalA/C
Number
N Internalaccountnumberoftheclearing
[[Broker]]/dealer.Left-justified,space-
filled.
44–59 16 CharacterX(16) ClearingAgent
InternalA/C
Number
N Internalaccountnumberoftheclearing
agent.Left-justified,space-filled.
60–75 16 CharacterX(16) InstitutionInternal
A/CNumber
N Codeornumbertheinvestment
managerusestoidentifyitscustomer
account.
Left-justified,space-filled.
76–91 16 CharacterX(16) InstitutionOrder
Routing
Reference #
N Numberprovidedtothebroker/dealer
byaninvestmentmanagerthatenables
aninvestmentmanagertotrackorders.
Left-justified,space-filled.
92–103 12 CharacterX(12) AllocationBlock
ReferenceIdentifier
N Institutioninternalreferenceidentifier
fromthecommonrecordofan
institutioninstruction.Ifmatched,
appendedfromtheallocation.
104–115 12 CharacterX(12) AllocationDetail
ReferenceIdentifier
N Institutioninternalreferenceidentifier
fromthedetailrecordofaninstitution
instruction.Ifmatched,appendedfrom
theallocation.
116 1 CharacterX(1) AdditionalParty
 #1Type
– Typeofadditionalpartynumber1.
l Space=Noadditionalpartynum-
ber1
l C=Customer
l P=Interestedparty
l B=[[Broker]]/dealersub-custodian
l A=Agentsub-custodian
117–124 8 Numeric9(8) AdditionalParty #1
[[ID]] Number
Y IDnumberofcustomer,interested
party,orsub-custodian(determinedby
AdditionalPartyType#1fieldin
position116).Sub-custodiancan
appearfortradesthatsettleawayfrom
[[DTC]].Zero-filledwhentheAdditional
Party#1Typefield(position116)isa
space.Right-justified,zero-filled.
Table3.5DetailRecord3:AdditionalPartyOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 55

---

## Page 56

Position Length Format FieldName Validate FieldDescription
125–136 12 CharacterX(12) AdditionalParty #1
Account Number
N Accountnumberforadditionalparty#1.
137–161 25 CharacterX(25) AdditionalParty #1
InstructionLine 1
N Textthatappearsontheconfirmation
instructionline1associatedwiththe
additionalpartynumber1or
[[Broker]]/dealersub-custodian.Thisfield
isusuallyforthebeneficialnameofthe
account.
162–186 25 CharacterX(25) AdditionalParty #1
InstructionLine 2
N Textthatappearsontheconfirmation
instructionline1associatedwiththe
additionalpartynumber1or
[[Broker]]/dealersub-custodian.Thisfield
isusuallyforthebeneficialnameofthe
account.
187–226 40 CharacterX(40) AdditionalParty #1
Name
N Nameoftheadditionalparty#1asit
appearsintheTradeSuiteIDmaster
file.
227 1 CharacterX(1) AdditionalParty #2
Type
– Typeofadditionalpartynumber2:
l Space=Noadditionalpartynum-
ber2
l C=Customer
l P=Interestedparty
l B=[[Broker]]/dealersub-custodian
l A=Agentsub-custodian
228–235 8 Numeric9(8) AdditionalParty #2
[[ID]] Number
Y IDnumberofcustomer,interested
party,orsub-custodian(determinedby
AdditionalPartyType#2inposition
227).Sub-custodiancanappearfor
tradesthatsettleawayfromDTC.Zero-
filledwhentheAdditionalParty#2Type
field(position227)isaspace.Right-
justified,zero-filled.
236–247 12 CharacterX(12) AdditionalParty #2
Account Number
N Accountnumberforadditionalparty#2.
248–272 25 CharacterX(25) AdditionalParty #2
InstructionLine 1
N Textthatappearsontheconfirmation
instructionline1associatedwith
additionalparty#2.Thisfieldisusually
forthebeneficialnameoftheaccount.
Table3.5DetailRecord3:AdditionalPartyOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 56

---

## Page 57

Position Length Format FieldName Validate FieldDescription
273–297 25 CharacterX(25) AdditionalParty #2
InstructionLine 2
N Textthatappearsontheconfirmation
instructionline2associatedwith
additionalparty#2.Thisfieldisusually
forthebeneficialnameoftheaccount.
298–337 40 CharacterX(40) AdditionalParty #2
Name
N Nameoftheadditionalparty#2asit
appearsintheTradeSuiteIDmaster
file.
338 1 CharacterX(1) AdditionalParty #3
Type
– Typeofadditionalpartynumber3:
l Space=Noadditionalpartynum-
ber3
l C=Customer
l P=Interestedparty
l B=[[Broker]]/dealersub-custodian
l A=Agentsub-custodian
339–346 8 Numeric9(8) AdditionalParty #3
[[ID]] Number
Y IDnumberofcustomer,interested
party,orsub-custodian(determinedby
theAdditionalPartyType#3fieldin
position338).Sub-custodiancan
appearfortradesthatsettleawayfrom
[[DTC]].Zero-filledwhentheAdditional
Party#3Typefield(position338)isa
space.
Right-justified,zero-filled.
347–358 12 CharacterX(12) AdditionalParty #3
Account Number
N Accountnumberforadditionalparty#3.
359–383 25 CharacterX(25) AdditionalParty #3
InstructionLine 1
N Textthatappearsontheconfirmation
instructionline1associatedwith
additionalparty#3.Thisfieldisusually
forthebeneficialnameoftheaccount.
384–408 25 CharacterX(25) AdditionalParty #3
InstructionLine 2
N Textthatappearsontheconfirmation
instructionline2associatedwith
additionalparty#3.Thisfieldisusually
forthebeneficialnameoftheaccount.
409–448 40 CharacterX(40) AdditionalParty #3
Name
N Nameoftheadditionalparty#3asit
appearsintheTradeSuiteIDmaster
file.
Table3.5DetailRecord3:AdditionalPartyOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 57

---

## Page 58

Position Length Format FieldName Validate FieldDescription
449 1 CharacterX(1) AdditionalParty #4
Type
– Typeofadditionalpartynumber4:
l Space=Noadditionalpartynum-
ber4
l C=Customer
l P=Interestedparty
l B=[[Broker]]/dealersub-custodian
l A=Agentsub-custodian
450–457 8 Numeric9(8) AdditionalParty #4
[[ID]] Number
Y IDnumberofcustomer,interested
party,orsub-custodian(determinedby
AdditionalPartyType#4inposition
449).Sub-custodiancanappearfor
tradesthatsettleawayfromDTC.Zero-
filledwhentheAdditionalParty#4Type
field(position449)isaspace.Right-
justified,zero-filled.
458–469 12 CharacterX(12) AdditionalParty #4
Account Number
N Accountnumberforadditionalparty#4.
470–494 25 CharacterX(25) AdditionalParty #4
InstructionLine 1
N Textthatappearsontheconfirmation
instructionline1associatedwith
additionalparty#4.Thisfieldisusually
forthebeneficialnameoftheaccount.
495–519 25 CharacterX(25) AdditionalParty #4
InstructionLine 2
N Textthatappearsontheconfirmation
instructionline2associatedwith
additionalparty#4.Thisfieldisusually
forthebeneficialnameoftheaccount.
520–559 40 CharacterX(40) AdditionalParty #4
Name
N Nameoftheadditionalparty#4asit
appearsintheTradeSuiteIDmaster
file.
560 1 CharacterX(1) AdditionalParty #5
Type
– Typeofadditionalpartynumber5:
l Space=Noadditionalpartynum-
ber5
l C=Customer
l P=Interestedparty
l B=[[Broker]]/dealersub-custodian
l A=Agentsub-custodian
Table3.5DetailRecord3:AdditionalPartyOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 58

---

## Page 59

Position Length Format FieldName Validate FieldDescription
561–568 8 Numeric9(8) AdditionalParty #5
[[ID]] Number
Y IDnumberofcustomer,interested
party,orsub-custodian(determinedby
AdditionalPartyType#5inposition
560).Sub-custodiancanappearfor
tradesthatsettleawayfromDTC.Zero-
filledwhentheAdditionalParty#5Type
field(position560)isaspace.
Right-justified,zero-filled.
569–580 12 CharacterX(12) AdditionalParty #5
Account Number
N Accountnumberforadditionalparty
number5.
581–605 25 CharacterX(25) AdditionalParty #5
InstructionLine 1
N Textthatappearsontheconfirmation
instructionline1associatedwith
additionalparty#5.Thisfieldisusually
forthebeneficialnameoftheaccount.
606–630 25 CharacterX(25) AdditionalParty #5
InstructionLine 2
N Textthatappearsontheconfirmation
instructionline2associatedwith
additionalparty#5.Thisfieldisusually
forthebeneficialnameoftheaccount.
631–670 40 CharacterX(40) AdditionalParty #5
Name
N Nameoftheadditionalparty#5asit
appearsintheTradeSuiteIDmaster
file.
671 1 CharacterX(1) AdditionalParty #6
Type
– Typeofadditionalpartynumber6:
l Space=Noadditionalpartynum-
ber6
l C=Customer
l P=Interestedparty
l B=[[Broker]]/dealersub-custodian
l A=Agentsub-custodian
672–679 8 Numeric9(8) AdditionalParty #6
[[ID]] Number
Y IDnumberofcustomer,interested
party,orsub-custodian(determinedby
AdditionalPartyType#6inposition
671).Sub-custodiancanappearfor
tradesthatsettleawayfromDTC.Zero-
filledwhentheAdditionalParty#6Type
field(position671)isaspace.Right-
justified,zero-filled.
680–691 12 CharacterX(12) AdditionalParty #6
Account Number
N Accountnumberforadditionalparty#6.
Table3.5DetailRecord3:AdditionalPartyOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 59

---

## Page 60

Position Length Format FieldName Validate FieldDescription
692–716 25 CharacterX(25) AdditionalParty #6
InstructionLine 1
N Textthatappearsontheconfirmation
instructionline1associatedwith
additionalparty#6.Thisfieldisusually
forthebeneficialnameoftheaccount.
717–741 25 CharacterX(25) AdditionalParty #6
InstructionLine 2
N Textthatappearsontheconfirmation
instructionline2associatedwith
additionalparty#6.Thisfieldisusually
forthebeneficialnameoftheaccount.
742–762 21 CharacterX(21) Filler – Reserved.Donotuse.
763–771 9 CharacterX(9) DTCControl
Number
– NumberassignedbytheTradeSuite
[[ID]] servicetoabroker/dealer'strade.
Thisnumbercanalsobeusedtoasso-
ciatethisrecordwithitsotherrecords.
TheDTC ControlNumbersare
recycledbasedonoveralltradeactivity.
772–773 2 CharacterX(2) Transaction
SequenceNumber
– Sequencenumberassignedbythe
TradeSuiteIDservicetoindicate
whethermorerecordsareassociated
withthisrecord:
22=Twooftwo
23=Twoofthree
24=Twooffour
25=Twooffive
33=Threeofthree
34=Threeoffour
35=Threeoffive
36=Threeofsix
774–813 40 CharacterX(40) AdditionalParty #6
Name
– Nameoftheadditionalparty#6asit
appearsintheTradeSuiteIDmaster
file.
814–978 165 CharacterX(165) Filler – Reserved.Donotuse.
Table3.5DetailRecord3:AdditionalPartyOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 60

---

## Page 61

DetailRecord4:Mortgage-BackedSecuritiesOutput
Table3.6showsthemortgage-backedsecurityinformationforoutputmessages.
Position Length Format FieldName Validate FieldDescription
Positions1–26:TransactionHeader
1 1 CharacterX(1) FeedbackIndicatorN Indicatesthereturnofthisrecord
becauseoferrors.Forafulldescription
ofthisprocessing,seetheInterface
ControlManager.
l .*=Ifnoerrors.
l ?=Iftherecordcontainserrors.
2 1 CharacterX(1) Production/Test
Indicator
Y Indicateswhethertherecordisfor
productionortest.Required.
l P=Production
l T=Test
3–8 6 CharacterX(6) RecordType Y Typeofdatacontainedinthemessage.
l CONFRM=Confirm
l COELIG=ChangeofEligibility
l AOCCNF=AdviceofCan-
cellationorCorrection
l RAFCAN=ReverseAffirmation
throughAdviceofCancellation
l RAFCOR=ReverseAffirmation
throughAdviceofCorrection
9–10 2 Numeric9(2) RecordSuffix Y Identifiesthephysicalrecordnumber.
l 04=Mortgage-BackedSecur-
itiesOutput
11–12 2 Numeric9(2) VersionNumber Y Versionnumberthatdefinestherecord
format.
l VersionNumberalways=01
13–18 6 CharacterX(6) Filler – Reserved.Donotuse.
19–26 8 CharacterX(8) Addressee Y TradeSuiteIDdestinationoftheuser
forwhomtherecordwasproduced,
enablingagroupusertoredistribute
therecord.
Table3.6DetailRecord4:Mortgage-BackedSecuritiesOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 61

---

## Page 62

Position Length Format FieldName Validate FieldDescription
Positions27–978:TransactionalData
27 1 CharacterX(1) Filler – Reserved.Donotuse.
28–29 2 CharacterX(2) TradeType
Indicator
Y Typeofmortgage-backedsecurity
transactionbeingconfirmed.
01=GenericTBA
02=SpecifiedTBA
03=SpecifiedPoolTBATrade
11=SpecifiedPoolTrade
12=GenericPoolTrade
50=OtherMortgage-backedsecurity
Trade
30–46 17 Numeric9(12)V9
(5)
CurrentFace Y Currentunpaidorremainingprincipalof
amortgage-backedsecurity.This
amountchangeseachmonthbythe
amountofthepay-downorpay-up
associatedwiththeunderlying
mortgagessupportingtheMBS.Right-
justified,zero-filled.
47–54 8 CharacterX(8) Factor/Effective
Date
Y Effectivedate,inYYYYMMDDformat,
ofthefactor.Enteravaliddayofthe
year,inclusiveofSaturday,Sunday,
andholidays.Ifnotsupplied,setto
spaces.
55–61 7 CharacterX(7) PoolNumber Y Agency-assignednumberreferencing
thepoolofmortgagesthatcollateralize
amortgage-backedsecurity.Supply
eitherapoolnumberorsecurity
numberforthespecifiedpooltrades
(TradeType=11)orGenericPool
trades(TradeType=12).Poolnumber
isinvalidforGenericTBAs(TradeType
=01).Ifnotsupplied,settospaces.
Table3.6DetailRecord4:Mortgage-BackedSecuritiesOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 62

---

## Page 63

Position Length Format FieldName Validate FieldDescription
62–72 11 CharacterX(11) Yield N Informationforbroker/dealerto
disclosetheYieldofthefixedincome
securityinvolvedinthetransaction.
Expectedcharactersincludenumbers
(0through9),onedecimalpoint,and
eitheroneplus(+)orminus(-)indicator
intherightmostposition.Cancontaina
floatingdecimalinanyposition;all
otherpositionsarenumeric.Whole
numbersdonotrequireadecimalpoint
(10b–10field).Ifthereisnoembedded
decimal,theTradeSuiteIDservice
assumesawholenumber.Ifnot
supplied,thisfieldallowsspaces.
Validexamplesare:
l 008.897000-
l 002.097000-
Right-justified,zero-filled.
Note:Thisfieldwillbevalidatedinthe
future.Enforcementwilloccuratalater
date.
73–88 16 CharacterX(16) RelatedReference
Number
N Internalbroker/dealerreference
numberforaTBA-relatedpool
confirmation.
89–91 3 Numeric9(3) NumberofDays
AccruedInterest
Y Totalnumberofdaystocalculatethe
interest.Right-justified,zero-filled.
92–99 8 CharacterX(8) IssueDate Y Mortgagepoolissueororigindate,in
YYYYMMDDformat.Enteravalidday
oftheyear,inclusiveofSaturday,
Sunday,andholidays.Ifnotsupplied,
settospaces.
100–108 9 CharacterX(9) SecurityClassCodeN FixedIncomeClearingCorporation
([[FICC]])andmortgage-backedsecurity
clearingcorporation(MBSCC)security
identifier.[[FICC]]/MBSCCmakes
componentsavailable.Indicates
agency,productcode,coupon,and
maturity.
109 1 CharacterX(1) Filler – Reserved.Donotuse.
Table3.6DetailRecord4:Mortgage-BackedSecuritiesOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 63

---

## Page 64

Position Length Format FieldName Validate FieldDescription
110–139 30 CharacterX(30) SecurityClass
Name
N Descriptionassociatedwithsecurity
classcode.
140–150 11 Numeric9(9)V9(2) OriginalTradePar Y Parvalueoftheoriginaltrade.Right-
justified,zero-filled.
151–154 4 Numeric9(4) GoodDelivery
Millions
Y Numberofmilliondollarlotsdelivered
inaccordancewithPSAguidelines.
Right-justified,zero-filled.
155–162 8 CharacterX(8) DeliveryDate Y Scheduleddeliverydateofthe
securitiestothecontraparty,in
YYYYMMDDformat.
Enteravaliddayoftheyear,including
Saturday,Sunday,andholidays.Use
thisfieldwiththeEPN/[[FICC]]/MBSCC
link.Ifnotsupplied,settospaces.
163–168 6 CharacterX(6) EPNTime Y Time,inHH:MM:SSformat,the
electronicpoolnotification(EPN)
messager(EPNgooddeliverytime
stamp)receivesthemessage.If
supplied,enterthetimeinmilitary
format.Ifnotsupplied,settospaces.
169–174 6 CharacterX(6) LotID N Lotnumberandpoolsequencewithin
thelot,indicatingapoolorgroupof
poolscomprisingone/manygood
deliverymillions.
175–178 4 Numeric9(4) Terminator Y Valueofthegooddeliverymillionsof
theprecedinglotofpools.Right-
justified,zero-filled.
179–189 11 CharacterX(11) MessageID N UniquemessageIDassignedbyEPN
totheoriginalmessage.
190 1 CharacterX(1) PossibleDuplicateY EPNindicatortotheuserthataninput
messagecanbeaduplicate.
l X=Duplicate
l Space=Non-duplicate
191–200 10 CharacterX(10) TradeNumber N NumberreferencingtheMBSCCtrade
number.
201–204 4 Numeric9(4) NumberofPools Y Numberofpoolscontainedwithinthe
EPNmessage.Right-justified,zero-
filled.
Table3.6DetailRecord4:Mortgage-BackedSecuritiesOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 64

---

## Page 65

Position Length Format FieldName Validate FieldDescription
205–220 16 CharacterX(16) InternalID N Uniquereferencenumberassignedby
thesubmitter.
221–224 4 CharacterX(4) SubmitterAccount
[[ID]]
N AccountIDoftheaccountsubmitting
themessage.
225–228 4 CharacterX(4) ServiceType N TypeofmessageinputtotheMBSCC.
l TFTD=Trade-for-trade
l SBOD=Useforalltradesin
classeseligiblefornettingwhen
nettingisdesired
l CMPT=Comparisontrade
l CMPC=Comparisontradecan-
cellation
l OPTN=Optiontrades
229–232 4 CharacterX(4) OptionType N Currentlysupportedoptionsforuse
withEPN/[[FICC]]/MBSCClink:
l CALL
l PUTS
233–240 8 CharacterX(8) OptionExpiration
Date
Y Date,inYYYYMMDDformat,whenthe
optionistoexpire.Enteravaliddayof
theyear,inclusiveofSaturday,
Sunday,andholidays.Usethisfield
withtheEPN/[[FICC]]/MBSCClink.Ifnot
supplied,settospaces.
241–248 8 CharacterX(8) RecordDate Y Date,inYYYYMMDDformat,setbythe
trusteetodeterminewhentopaythe
principalandinterestonasecurity.If
supplied,enteravaliddayoftheyear,
inclusiveofSaturday,Sunday,and
holidays.Ifnotsupplied,settospaces.
249–251 3 CharacterX(3) Specification #1
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
252–266 15 CharacterX(15) Specification #1
Value
Y Textforspecificationcode#1.
Table3.6DetailRecord4:Mortgage-BackedSecuritiesOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 65

---

## Page 66

Position Length Format FieldName Validate FieldDescription
267–269 3 CharacterX(3) Specification #2
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
270–284 15 CharacterX(15) Specification #2
Value
Y Textforspecificationcode#2.
285–287 3 CharacterX(3) Specification #3
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
288–302 15 CharacterX(15) Specification #3
Value
Y Textforspecificationcode#3.
303–305 3 CharacterX(3) Specification #4
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
306–320 15 CharacterX(15) Specification #4
Value
Y Textforspecificationcode#4.
321–323 3 CharacterX(3) Specification #5
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
324–338 15 CharacterX(15) Specification #5
Value
Y Textforspecificationcode#5.
339–341 3 CharacterX(3) Specification #6
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
342–356 15 CharacterX(15) Specification #6
Value
Y Textforspecificationcode#6.
357–359 3 CharacterX(3) Specification #7
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
360–374 15 CharacterX(15) Specification #7
Value
Y Textforspecificationcode#7.
Table3.6DetailRecord4:Mortgage-BackedSecuritiesOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 66

---

## Page 67

Position Length Format FieldName Validate FieldDescription
375–377 3 CharacterX(3) Specification #8
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
378–392 15 CharacterX(15) Specification #8
Value
Y Textforspecificationcode#8.
393–395 3 CharacterX(3) Specification #9
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
396–410 15 CharacterX(15) Specification #9
Value
Y Textforspecificationcode#9.
411–413 3 CharacterX(3) Specification #10
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
414–428 15 CharacterX(15) Specification #10
Value
Y Textforspecificationcode#10.
429–431 3 CharacterX(3) Specification #11
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
432–446 15 CharacterX(15) Specification #11
Value
Y Textforspecificationcode#11.
447–449 3 CharacterX(3) Specification #12
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
450–464 15 CharacterX(15) Specification #12
Value
Y Textforspecificationcode#12.
465–467 3 CharacterX(3) Specification #13
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
468–482 15 CharacterX(15) Specification #13
Value
Y Textforspecificationcode#13.
Table3.6DetailRecord4:Mortgage-BackedSecuritiesOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 67

---

## Page 68

Position Length Format FieldName Validate FieldDescription
483–485 3 CharacterX(3) Specification #14
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
486–500 15 CharacterX(15) Specification #14
Value
Y Textforspecificationcode#14.
501–503 3 CharacterX(3) Specification #15
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
504–518 15 CharacterX(15) Specification #15
Value
Y Textforspecificationcode#15.
519–521 3 CharacterX(3) Specification #16
Code
Y Coderepresentingaconditiontothe
trade.Right-justified,zero-filled.For
mortgage-backedsecurityspecification
codes,seeInput/OutputInformation.
522–536 15 CharacterX(15) Specification #16
Value
Y Textforspecificationcode#16.
537–544 8 Numeric9(3)V9(5) MBSInterestRate N Mortgage-backedsecurityinterestrate.
545–552 8 CharacterX(8) MBSMaturityDate N Mortgage-backedsecuritymaturity
date,inYYYYMMDDformat.
553–762 210 CharacterX(210) Filler – Reserved.Donotuse.
763–771 9 CharacterX(9) DTCControl
Number
– NumberassignedbytheTradeSuiteID
servicetoabroker/dealer’strade.This
numbercanalsobeusedtoassociate
thisrecordwithitsotherrecords.The
DTCControlNumbersarerecycled
basedonoveralltradeactivity.
Table3.6DetailRecord4:Mortgage-BackedSecuritiesOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 68

---

## Page 69

Position Length Format FieldName Validate FieldDescription
772–773 2 CharacterX(2) Transaction
SequenceNumber
– Sequencenumberassignedbythe
TradeSuiteIDservicetoindicate
whethermorerecordsareassociated
withthisrecord:
22=Twooftwo
23=Twoofthree
24=Twooffour
33=Threeofthree
34=Threeoffour
35=Threeoffive
44=Fouroffour
45=Fouroffive
46=Fourofsix
774–978 205 CharacterX(205) Filler – Reserved.Donotuse.
Table3.6DetailRecord4:Mortgage-BackedSecuritiesOutput(continued)
DetailRecord5:SupplementalOutput
Table3.7showsthesupplementalinformationforoutputmessages.
PositionLengthFormat FieldName ValidateFieldDescription
Positions1–26:TransactionHeader
1 1 Character X
(1)
FeedbackIndicator N Indicatesthereturnofthisrecordbecauseof
errors.Forafulldescriptionofthisprocessing,
seetheInterfaceControlManager.
l .*=Noerrors.
l ?=Recordcontainserrors.
2 1 Character X
(1)
Production/Test
Indicator
Y Indicateswhetherrecordisforproductionortest.
Required.
l P=Production
l T=Test
3–8 6 CharacterX
(6)
RecordType Y Typeofdatacontainedinthemessage.
l CONFRM=Confirm
l COELIG=ChangeofEligibility
Table3.7DetailRecord5:SupplementalOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 69

---

## Page 70

PositionLengthFormat FieldName ValidateFieldDescription
9–10 2 Numeric9
(2)
RecordSuffix Y Identifiesthephysicalrecordnumber.
l 05=SupplementalInformationOutput
11–12 2 Numeric9
(2)
VersionNumber Y Versionnumberthatdefinestherecordformat:
l VersionNumberalways=01
13–18 6 CharacterX
(6)
Filler – Reserved.Donotuse.
19–26 8 CharacterX
(8)
Addressee Y TradeSuiteIDdestinationoftheuserforwhom
therecordwasproduced,enablingagroupuser
toredistributetherecord.
Positions27–978:TransactionalData
27 1 Character X
(1)
Filler – Reserved.Donotuse.
28–43 16 Character X
(16)
Clearing
[[Broker]]/DealerInternal
A/C
Number *
N Internalaccountnumberoftheclearingbroker.
44–59 16 CharacterX
(16)
ClearingAgent
InternalA/CNumber *
N Internalaccountnumberoftheclearingagent.
60–75 16 CharacterX
(16)
InstitutionInternalA/C
Number *
N Codeornumbertheinstitutionusestoidentify
theaccountofthecustomer.
76–91 16 CharacterX
(16)
InstitutionOrder
RoutingReference #
N Numberprovidedtothebroker/dealerbyan
institutionthatenablestheinstitutiontotrack
orders.Ifmatched,appendedfromallocation.
92–103 12 CharacterX
(12)
AllocationBlock
ReferenceIdentifier
N Institutioninternalreferenceidentifierfromthe
commonrecordofaninstitutioninstruction.If
matched,appendedfromallocation.
104–115 12 CharacterX
(12)
AllocationDetail
ReferenceIdentifier
N Institutioninternalreferenceidentifierfromthe
detailrecordofaninstitutioninstruction.If
matched,appendedfromallocation.
Table3.7DetailRecord5:SupplementalOutput(continued)
*Whentradeinputincludesabroker/dealerinternalaccountnumber(BIA)thatislinkedtoinstitutioninformation
abouttheALERTplatform,theALERTplatformfillsorreplacesthedatainthisfield.
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 70

---

## Page 71

PositionLengthFormat FieldName ValidateFieldDescription
116–117 2 CharacterX
(2)
ConfirmPurpose Y Providesthecustomerwiththereasonfor
issuingtheconfirm.Ifsupplied,enteravalid
value.
00=Notspecified
01=Original
02=Substitution
03=Marginreprice/cashcall
04=Marginreprice/collateralcall
05=Rollover
99=Other
Spaces=Notsupplied
118–119 2 CharacterX
(2)
DeliveryMethod Y Determinesthedeliverymethodbasedon
securitytypeorpurposeoftrade.Mandatoryfor
theFINorCOLexpandedsecuritytypes.If
supplied,enteravalidvalue.
01=Free
02=Bookentry
03=Physical
04=DVP/RVP
05=Cash
06=Hold-in-[[custody]]
07=Tri-party
08=Quadparty
99=Other
Table3.7DetailRecord5:SupplementalOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 71

---

## Page 72

PositionLengthFormat FieldName ValidateFieldDescription
120–121 2 CharacterX
(2)
PriceType Y PricetypeassociatedwiththePricefieldin
record1,position99–109.Ifsupplied,entera
validvalue.
00=Notspecified
01=Spot
02=Clean
03=Dirty
04=Forward
05=All-in
06=Bid
07=Ask
08=High
09=Low
10=Open
11=Close
12=Mid
13=Mean
14=Lasttrade
15=Compositetrade
16=Issue
17=Kassa
18=Evaluation
19=Primaryexchange
99=Other
Spaces=Notsupplied
122 1 Character X
(1)
BlockTradeIndicatorY IndicatesthattheconfirmrepresentsaBlock
leveltrade.Ifsupplied,enteravalidvalue.
l B=Block
l Space=NotaBlock
123–134 12 CharacterX
(12)
Give-Up
[[Broker]]/Dealer
N Identifierofagive-upbroker/dealer.Indicates
thatafeemightbeduetoabroker/dealerthat
arrangedthetransaction(associatedwiththe
[[Broker]]/dealer).
135–142 8 CharacterX
(8)
[[Broker]]/Dealer
Salesman
N Salespersonnumber.
Table3.7DetailRecord5:SupplementalOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 72

---

## Page 73

PositionLengthFormat FieldName ValidateFieldDescription
143–148 6 CharacterX
(6)
TradeExecutionTimeY Timeofday,inHH:MM:SSformat,thatthe
dealerbookedthetrade.Ifsupplied,enteravalid
time.Spaces=Notsupplied.
149–151 3 CharacterX
(3)
TradeExecutionTime
Zone
N Forexample:
l EST
l GMT
l PST
l CST
l MST
l OTH=Other
152 1 CharacterX
(1)
SIPCMember Y Denoteswhetherthebroker/dealerisaSIPC
[[Member]](10b–10field).Ifsupplied,enteravalid
value.Spaces=Notsupplied.
l Y=Yes
l N=No
153 1 CharacterX
(1)
FINRAMember Y Denoteswhetherthebroker/dealerisamember
ofFINRA(10b–10field).Ifsupplied,enteravalid
value.Spaces=Notsupplied.
l Y=Yes
l N=No
154 1 CharacterX
(1)
NYSEMember Y Denoteswhetherthebroker/dealerisaNYSE
[[Member]](10b–10field).Ifsupplied,enteravalid
value.Spaces=Notsupplied.
l Y=Yes
l N=No
155 1 CharacterX
(1)
MarketMaker Y Denoteswhetherthebroker/dealerisamarket
makerinthesecurity(10b–10field).Ifsupplied,
enteravalidvalue.Spaces=Notsupplied.
l Y=Yes
l N=No
156–187 32 CharacterX
(32)
DeliveryInstructions
Line 1
N Whereinvestmentmanagerorfunddeliversor
receivessecuritiesfrom;forexample,the
physicaldeliveries.Canbeaphysicalstreet
location.Free-formtext.
Table3.7DetailRecord5:SupplementalOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 73

---

## Page 74

PositionLengthFormat FieldName ValidateFieldDescription
188–219 32 CharacterX
(32)
DeliveryInstructions
Line 2
N Whereinvestmentmanagerorfunddeliversor
receivessecuritiesfrom;forexample,the
physicaldeliveries.Canbeaphysicalstreet
location.Free-formtext.
220–251 32 CharacterX
(32)
WireInstructions N Ifneededfortri-partyorifthephysicalsecurity
deliveryisnecessary.MinimallyneedtheABA
number.Free-formtext.
252–283 32 CharacterX
(32)
Special Instructions
Line 9
N Useforcontactnames,taxIDs,phonenumbers,
10b–10information,financing/REPOtransaction
additionalinformation,orconfirmbackeritemsto
includeonthefrontoftheconfirm,butnodefined
fieldsexist.Free-formtext.
284–315 32 CharacterX
(32)
Special Instructions
Line 10
N
316–347 32 CharacterX
(32)
Special Instructions
Line 11
N
348–379 32 CharacterX
(32)
Special Instructions
Line 12
N
380–411 32 CharacterX
(32)
Special Instructions
Line 13
N
412–443 32 CharacterX
(32)
Special Instructions
Line 14
N
444–475 32 CharacterX
(32)
Special Instructions
Line 15
N
476–507 32 CharacterX
(32)
Special Instructions
Line 16
N
508–539 32 CharacterX
(32)
Special Instructions
Line 17
N
540–571 32 CharacterX
(32)
Special Instructions
Line 18
N
572–621 50 CharacterX
(50)
DisclosureLink – ContainstheURLlinkforthebroker/dealer
confirmbacker/disclosureinformationfromthe
inSITEdisclosurerepository.Usetoaccessthe
repositorytoviewtheconfirmbacker/disclosure
informationassociatedorspecifictothetrade
confirmation.
Table3.7DetailRecord5:SupplementalOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 74

---

## Page 75

PositionLengthFormat FieldName ValidateFieldDescription
622–637 16 CharacterX
(16)
DisclosureReference
Number
– Disclosurereferencenumberassignedby
backer/disclosurerepositorytoidentifythe
specificbacker/disclosureassociatedwiththe
tradeconfirmation.Toviewrequiredinformation
forthebacker/disclosuredocument,goto
AccessProductServicesandselectyour
product.
638 1 CharacterX
(1)
ConfirmDisclosure
FoundIndicator
– IndicateswhetheraconfirmdisclosureURLand
referencenumberwasenrichedorfoundon
tradeconfirmoutput.
l Y=Backer/disclosureURLandreference
found
l N=Backer/disclosureURLandreference
notfound
l U=Notsubscribed
l Space=Brokerhasbypasseddisclosure
enrichment.
639–654 16 CharacterX
(16)
UserDefined
DisclosureCode
Y User-definedcodeusedinconfirm
backer/disclosureenrichment.Itis
[[Broker]]/dealer-supplieddatathatalsoresideson
backer/disclosurerepositoryasenrichment
criteria.Thefieldresidesontherepositoryforthe
[[Broker]]/dealertodefinethecriteria.
655 1 CharacterX
(1)
ConfirmDisclosure
BypassIndicator
Y Fieldforbroker/dealertoinstructtheTradeSuite
IDservicetobypassoroverrideindicatorfor
confirmdisclosureenrichmentforatrade.
l B=Bypassconfirmdisclosureenrichment
l Space=Enrichconfirmdisclosure,ifsub-
scribed
656 1 CharacterX
(1)
MarkUp/MarkDown
Sign
Y AssociatedwiththeMark-UporMark-Down
field.Indicateswhetherthemark-upormark-
downislessthanorgreaterthan.
l +=Positive
l -=Negative
l Spacenotsupplied
Table3.7DetailRecord5:SupplementalOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 75

---

## Page 76

PositionLengthFormat FieldName ValidateFieldDescription
657–667 11 CharacterX
(11)
MarkUp/MarkDown Y Informationforthebroker/dealertodiscloseany
mark-up,mark-down,ordifferencebetweenthe
reportedpriceandthepricetothecustomer
involvedinthetransaction.
Datacancontainafloatingdecimalinany
position.Enternumericforallotherpositions.
Wholenumbersdonotrequireadecimalpoint.If
notsupplied,thisfieldallowsspaces.Right-
justified,zero-filled.
668 1 CharacterX
(1)
3rdParty
Remuneration
Received
Y Fieldtodenotewhetherthebroker/dealer
receivedanythird-partyremunerationinthe
transaction.
l Y=Yes
l N=No
l Spacenotsupplied
669–688 20 CharacterX
(20)
[[Broker]]/Dealer
TelephoneNumber
N Telephonenumberofthebroker/dealer.
Informationforbroker/dealertodiscloseits
telephonenumberusedforcontactingpurposes
withcounterparty.Freeformtextallowed.
689–723 35 CharacterX
(35)
AgentInternal
AccountNumber
N Agent'sinternalaccountnumber(AIA).If
populated,theTradeSuiteIDserviceusesthe
35-characterfieldinsteadoftheAgentInternal
AccountNumberinrecord1,position323.
Settospaceswhentheagentinternalaccount
numberisunavailableornotapplicable.Free-
formtext.
724–732 9 Numeric9
(7)V99
Commission
Equivalent
Y Reportanynon-monetarybenefitamounts
disclosedascommissionequivalent,asfaras
possible,thesameastheamountsandvalueof
commissionpaidinacorrespondingsale.
Commissionequivalentisoftenusedtoexecute
risklessprincipaltrades.
Thisfieldcontainszeroswhenthecommission
equivalentisunavailableornotapplicable.
Table3.7DetailRecord5:SupplementalOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 76

---

## Page 77

PositionLengthFormat FieldName ValidateFieldDescription
733–748 16 CharacterX
(16)
TradeSuiteID
Operating Procedures
GuideReference
Number
TradeSuiteIDOperatingProceduresguide
referencenumberassignedbytheinSITE
repositorytoidentifythespecificTradeSuiteID
OperatingProceduresguideassociatedwith
thetradeconfirmation.Toviewthisguideon
theinSITErepository,theTradeSuiteID
servicerequiresthisfieldandthe
correspondingTradeSuiteIDinstitutionguide
URL linkspecifiedintheIDNetDisclosure
Line1andLine2andOperatingProcedures
GuideLinkfields.
749–753 5 CharacterX
(5)
Filler – Reserved.Donotuse.
754–762 9 CharacterX
(9)
VendorControlID – ControlIDassignedbythebroker'svendortoa
[[Broker]]/dealer’strade.
763–771 9 CharacterX
(9)
DTCControlNumber– NumberassignedbytheTradeSuiteIDservice
toabroker/dealer’strade.Thisnumbercanalso
beusedtoassociatethisrecordwithitsother
records.TheDTCControlNumbersarerecycled
basedonoveralltradeactivity.
772–773 2 CharacterX
(2)
Transaction
SequenceNumber
– SequencenumberassignedbytheTradeSuite
IDservicetoindicatewhethermorerecordsare
associatedwiththisrecord.
22=Twooftwo
23=Twoofthree
33=Threeofthree
34=Threeoffour
44=Fouroffour
45=Fouroffive
55=Fiveoffive
56=Fiveofsix
774–823 50 CharacterX
(50)
TradeSuiteID
OperatingProcedures
GuideLink
– ContainstheURLlinkfortheTradeSuiteID
serviceOperatingProceduresguide
informationavailablefromtheinSITE
disclosurerepository.Thisfieldisusedto
accesstherepositorytoviewtheTradeSuite
IDserviceOperatingProceduresguidein
effectwhenthetradewasprocessed.To
accesstheURLlink,gotoAccessProduct
Servicesandselectyourproduct.
Table3.7DetailRecord5:SupplementalOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 77

---

## Page 78

PositionLengthFormat FieldName ValidateFieldDescription
824-831 8 CharacterX
(8)
TradeExecutionDate Y TradeExecutionDatethatthebroker/dealer
bookedthetrade,inCCYYMMDDformat.
832 1 CharacterX
(1)
MarkUp/MarkDown
PercentageSign
Y AssociatedwiththeMarkUporMarkDown
field.Indicateswhethertheassociatedfieldis
lessthenorgreaterthan:
l +=Positive
l -=Negative
l Space=notsupplied
833-840 8 Numeric9
(3)V9(5)
MarkUp/Mark
DownPercentage
Y Fieldinformationforthebroker/dealertodis-
closeanypercentageoftheMarkUp/Mark
Downthatrepresentsdifferencebetweenthe
reportedpriceandthepricetothecustomer
involvedinthetransaction.Displayedasaper-
centage.
841-860 20 CharacterX
(20)
BrokerLegalEntity
Identifier
Y Auniquealphanumericbrokeridentifier
(ISO17442).ThisisaMIFIDII-relatedchange.
861-880 20 CharacterX
(20)
InstitutionLegalEntity
Identifier
Y Auniquealphanumericinstitutionidentifier
(ISO17442).ThisisaMIFIDII-relatedchange.
881-896 16 CharacterX
(16)
CTMBrokerRefer-
enceNumber
N CTMBrokerReferenceNumberisonlyavailable
forallM2i(USDI/USDM)trades,ifthebroker
providedthefieldintheCTMservice.Thisfield
canonlybepassedtotheTradeSuiteIDservice
fromtheCTMservice.Thevalueiscaptured
fromthefollowingTradeDetailReferencecom-
posite:TradeDe-
tailReference>ClientAllocationReference.
897-904 8 CharacterX
(8)
MatchDate N Thedateofwhichtheconfirmwasmatchedin
TradeMatch.InFormatCCYYMMDD.Thisnew
fieldiscurrentlyintheTestsystemandwillbe
availableintheproductionsystemintheT1
releaseinMay2024
905-910 6 CharacterX
(6)
MatchTime N ThetimeofwhichtheconfirmwasMatchedin
TradeMatch.InFormatHHMMSSThisnewfield
iscurrentlyintheTestsystemandwillbeavail-
ableintheproductionsystemintheT1releasein
May2024
897-978 98 CharacterX
(98)
Filler - Reserved.Donotuse.
Table3.7DetailRecord5:SupplementalOutput(continued)
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 78

---

## Page 79

DetailRecord6:Financing/REPOTransactionOutput
Table3.8showsthefinancing/REPOtransactioninformationforoutputmessages.
Position Length Format FieldName Validate FieldDescription
Positions1–26:TransactionHeader
1 1 Character X(1) FeedbackIndicator N Indicatesthereturnofthisrecord
becauseoferrors.Forafull
descriptionofthisprocessing,see
theInterfaceControlManager.
l .*=Ifnoerrors.
l ?=Iftherecordcontains
errors.
2 1 Character X(1) Production/Test
Indicator
Y Indicateswhetherrecordisfor
productionortest.Required.
l P=Production
l T=Test
3–8 6 CharacterX(6) RecordType Y Typeofdatacontainedinthe
message.
l CONFRM=Confirm
l COELIG=ChangeofEli-
gibility
9–10 2 Numeric9(2) RecordSuffix Y Identifiesthephysicalrecord
number.
l 06=Financing/REPOOut-
put
11–12 2 Numeric9(2) VersionNumber Y Versionnumberthatdefinesthe
recordformat:
l VersionNumberalways=01
13–18 6 CharacterX(6) Filler – Reserved.Donotuse.
19–26 8 CharacterX(8) Addressee Y TradeSuiteIDdestinationofthe
userforwhomtherecordwas
produced,enablingagroupuserto
redistributetherecord.
Positions27–978:TransactionalData
27 1 Character X(1) Filler – Reserved.Donotuse.
Table3.8DetailRecord6:Financing/REPOTransactionOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 79

---

## Page 80

Position Length Format FieldName Validate FieldDescription
28–29 2 CharacterX(2) TradeType Y Identifiesthetradetype.When
selectingtheexpandedsecurity
typeFINorCOL,userecord6.
Selectthetype,andsupplyavalid
value.
01=REPO
02=ReverseREPO
03=Sell/buyback
04=Buy/sellback
05=Participation
06=Securitylending
07=Securityborrowing
99=Other
30–31 2 CharacterX(2) LegIdentifier Y Identifieswhethertheconfirmisa
firstlegconfirm,secondleg
confirm,orboth.Mandatorywhen
selectingtheFINexpanded
securitytype.Optionalwhen
selectingtheCOLexpanded
securitytype.Supplyavalidvalue.
l LO–Onleg
l LC–Offleg
l LB–Bothlegs
Table3.8DetailRecord6:Financing/REPOTransactionOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 80

---

## Page 81

Position Length Format FieldName Validate FieldDescription
32–33 2 CharacterX(2) CollateralType Y Identifiesthetypeofcollateral
involvedinthetransaction.For
securitylending,canusespecial
instructionsfieldtospecifyother
collateraltypesnotsuppliedhere.
Mandatorywhenselectingeither
theFINorCOLexpandedsecurity
type.Supplyavalidvalue.
01=Treasuries
02=Governmentagencies
03=[[Asset]]-backedsecurities
04=CMO
05=Mortgage-backedsecurities
06=Equities
07=Moneymarkets
08=Corporatebonds
09=Municipalbonds
10=Wholeloans
11=Generalcollateral
12=Letterofcredit
13=Privatelabels
14=Cash
15=SovereignBonds
16=IndexFunds
17=Exchangetradedfunds
99=Other
34–73 40 CharacterX(40) Tri-PartyAgent N Nameofthetri-partyagent.
74–81 8 CharacterX(8) StartDate Y DatethattheREPOstarted
accruinginterest,inYYYYMMDD
format.Itisequivalenttothe
settlementdateofthefirstleg.If
supplied,enteravaliddateofthe
year,includingweekendsand
holidays.Spaces=Notsupplied.
Table3.8DetailRecord6:Financing/REPOTransactionOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 81

---

## Page 82

Position Length Format FieldName Validate FieldDescription
82–89 8 CharacterX(8) EndDate/MaturityDate Y ClosingdateoftheREPOor
reverseREPO.Intereststops
accruing.Iftheenddateis
unknown,createanopenREPO
usingallspaces.Ifclosinganopen
REPO,usetheactualenddate.If
supplied,enteravaliddateofthe
year,inYYYYMMDDformat.Valid
datesincludeweekendsand
holidays.Spaces=Notsupplied.
90–92 3 Numeric9(3) Numberofpiecesof
[[collateral]]
Y Itemcountfornumberofcollateral
pieces.Right-justified,zero-filled.
93–108 16 CharacterX(16) ParentReference
Number
N Cross-referencesaparenttrade
withallassociatedchildor
collateraltrades.Reference
numbercanberetainedon
rollovers,substitutions,andso
forth.
109–124 16 CharacterX(16) Additional Reference
Number 1
N UsetolinkbuysandsellsforSBB
andBSBtradesorforanyother
referencenumbers.125–140 16 CharacterX(16) Additional Reference
Number 2
N
141 1 Character X(1) FINRateSign Y Denoteswhethertheinterestrateis
positiveornegative.Ifsupplied,
enteravalidvalue.Spaces=Not
supplied.
l +=Positive
l -=Negative
l Space=blank
142–149 8 Numeric9(2)V9(6) FINRate Y Interestratethatthetransaction
accrues.Right-justified,zero-filled.
150 1 CharacterX(1) FINRateType Y Specifieswhethertherateisafixed
orvariablerate.Ifsupplied,entera
validvalue.Spaces=Notsupplied.
l F=Fixed
l V=Variable
l Space=blank
Table3.8DetailRecord6:Financing/REPOTransactionOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 82

---

## Page 83

Position Length Format FieldName Validate FieldDescription
151–164 14 Numeric9(12)V99SecurityLendingFee Y Negotiatedflatfeeassociatedwith
securitieslendingorwitha
securitiesloan.
Right-justified,zero-filled.
165–166 2 CharacterX(2) AccrualMethod Y Calculationtypeusedtoarriveat
thetotalinterestpaymentonthe
trade.
00=NotSpecified
01=30/360
02=30/365
03=30/Actual
04=Actual/360
05=Actual/365
06=Actual/Actual
07=Actual/365L
99=Other.Ifsupplied,enteravalid
value.
Spaces=Notsupplied.
167 1 Character X(1) InterestDaysSign Y DenoteswhethertheInterestDays
fieldispositiveornegative.If
supplied,enteravalidvalue.
Spaces=Notsupplied.
l +=Positive
l -=Negative
l Space=blank
168–171 4 Numeric9(4) InterestDays Y Interestaccrualdays.
Right-justified,zero-filled.
172 1 Character X(1) AccruedInterestdueat
MaturitySign
Y Denoteswhethertheaccrued
interestdueatMaturityfieldis
positiveornegative.Ifsupplied,
enteravalidvalue.Spaces=Not
supplied.
l +=Positive
l -=Negative
l Space=blank
Table3.8DetailRecord6:Financing/REPOTransactionOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 83

---

## Page 84

Position Length Format FieldName Validate FieldDescription
173–186 14 Numeric9(12)V99AccruedInterestdueat
Maturity
Y Calculatedvaluederivedfromthe
REPOrateandthenumberof
Interestdays.Right-justified,zero-
filled.
187–188 2 CharacterX(2) Index(Benchmark) Y Benchmarkrateofinterestaccrual,
associatedwithorconsidereda
floatingrateREPO.Ifsupplied,
enteravalidvalue.Spaces=Not
supplied.Forindex(benchmarks)
codes,seeInput/Output
Information.
189 1 Character X(1) SpreadtoBenchmark
Sign
Y Denoteswhetherspreadto
benchmarkispositiveornegative.
Ifsupplied,enteravalidvalue.
Spaces=Notsupplied.
l +=Positive
l -=Negative
l Space=blank
190–192 3 Numeric9(3) SpreadtoBenchmarkor
Index(forFloatingRate)
Y Basispointsawayfromthe
benchmarkorindexusedto
determinetherate.Right-justified,
zero-filled.
193–200 8 Numeric9(3)V9(5) [[Haircut]] % Y Margincollateralassociatedwith
REPOtypetransactionstoaccount
formarketorinterestpaymentson
theunderlyingsecurities.Asa
percentage.Right-justified,zero-
filled.
Table3.8DetailRecord6:Financing/REPOTransactionOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 84

---

## Page 85

Position Length Format FieldName Validate FieldDescription
201 1 Character X(1) SubstitutionType Y Typeofcollateralsubstitution.
Spaces=Notsupplied.
l
P=Parvalueofthe
securitytimestheprice
determinesthetransaction
principalamount.
l
M=Moneyfilled.A
principalamountis
assignedtothecollateral.
l Space=Blank
Ifsupplied,enteravalidvalue.
202–203 2 CharacterX(2) SubstitutionNumber N Numberoftimesthatcollateralcan
besubstitutedoverthelifeofthe
REPO.Torepresentunlimited
numberofsubstitutions,denoteas
aspacefollowedbyU.
204–211 8 Numeric9(3)V9(5) SubstitutionVariance Y Percentagebywhichtheprincipal
valueofthereplacementcollateral
candifferfromtheprincipalofthe
original.Asapercentage.Parfills
only.Right-justified,zero-filled.
212–213 2 CharacterX(2) SubstitutionFrequencyN Periodoverwhichthespecified
numberofsubstitutionscantake
place.Number1–9infirstcharacter
positionfollowedbyoneofthe
followingletters:
l H=Half
l Q=Quarter
l M=Month
l W=Week
Forexample:
l 1Q(onceaquarter)
l 2W(twiceaweek)
Table3.8DetailRecord6:Financing/REPOTransactionOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 85

---

## Page 86

Position Length Format FieldName Validate FieldDescription
214 1 Character X(1) Face(Par)orCashFill
REPO
Y BasisfortheREPOtocollateralize.
Ifsupplied,enteravalidvalue.
l
F=Face(Par)
Ifface,facetimesprice
equalscollateralvalue.
l C=Cashfill
l Space=blank
l Spaces=Notsupplied.
215–228 14 Numeric9(12)V99REPOValue Y Marketvalueroundedusingthe
appropriatemarketpractice
conventionforthatparticular
instrumentintheREPOmarket.
Marketvalueofthesecuritywith
haircutconsidered.Right-justified,
zero-filled.
229–242 14 Numeric9(12)V99PremiumAmount Y Differenceinmoneybetweenthe
openandcloselegsofaREPO
transaction.Right-justified,zero-
filled.
243–244 2 CharacterX(2) InterestPayment
CalendarFrequency
N PaymentInterval,suchas3
monthsor6monthsfortheinterest
cleanupschedule.Number1–9in
thefirstcharacterpositionfollowed
byoneofthefollowingletters:
l H=Half
l Q=Quarter
l M=Month
l W=Week
Forexample:
l 1Q(onceaquarter)
l 2W(twiceaweek)
Table3.8DetailRecord6:Financing/REPOTransactionOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 86

---

## Page 87

Position Length Format FieldName Validate FieldDescription
245–252 8 CharacterX(8) 1stInterestCleanup
Date
Y Firstdateonwhichtobase
scheduleofinterestcleanup
payments,inYYYYMMDDformat.
Ifsupplied,enteravaliddateofthe
year,includingweekendsand
holidays.Spaces=Notsupplied.
253–255 3 Numeric9(3) LookbackDays(for
floatingrate)
Y Numberofbusinessdaysbefore
thefloatingrateresetdatewhen
thebenchmarkpriceiscaptured
andusedtodeterminethenewrate
uponreset.Right-justified,zero-
filled.
256–257 2 CharacterX(2) ResetInterval
Frequency(forfloating
rates)
N Resetinterval,suchas3monthsor
6months.Number1–9inthefirst
characterpositionfollowedbyone
ofthefollowingletters:
l H=Half
l Q=Quarter
l M=Month
l W=Week
Forexample:
l 1Q(onceaquarter)
l 2W(twiceaweek)
258–265 8 CharacterX(8) 1stRateResetDate Y Firstdateonwhichtobase
scheduleofrateresetdates,in
YYYYMMDDformat.Ifsupplied,
enteravaliddateoftheyear,
includingweekendsandholidays.
Spaces=Notsupplied.
Table3.8DetailRecord6:Financing/REPOTransactionOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 87

---

## Page 88

Position Length Format FieldName Validate FieldDescription
266–267 2 CharacterX(2) FlexREPOPayback
Frequency
N Singlematuritybutmoneygiver’s
cashcanbereturnedmostoftenon
apredeterminedpaydown
schedule.Number1–9inthefirst
characterpositionfollowedbyone
ofthefollowingletters:
l H=Half
l Q=Quarter
l M=Month
l W=Week
Forexample:
l 1Q(onceaquarter)
l 2W(twiceaweek)
268–275 8 CharacterX(8) 1stFlexRepayment
Date
Y Firstdateonwhichtobase
scheduleofflexrepayments,in
YYYYMMDDformat.Ifsupplied,
enteravaliddateoftheyear,
includingweekendsandholidays.
Spaces=Notsupplied.
276–278 3 Numeric9(3) CallDelay Y Minimumnumberofdaysnoticea
counterpartyneedsforterminating
thetransaction.Right-justified,
zero-filled.
279–762 484 CharacterX(484) Filler – Reserved.Donotuse.
763–771 9 CharacterX(9) DTCControlNumber – Numberassignedbythe
TradeSuiteIDservicetoabroker-
/dealer’strade.Thisnumbercan
alsobeusedtoassociatethis
recordwithitsotherrecords.The
DTCControlNumbersarerecycled
basedonoveralltradeactivity.
772–773 2 CharacterX(2) TransactionSequence
Number
– Sequencenumberassignedbythe
TradeSuiteIDservicetoindicate
whethermorerecordsare
associatedwiththisrecord.
33=Threeofthree
44=Fouroffour
55=Fiveoffive
66=Sixofsix
774–978 205 Character X(205) Filler – Reserved.Donotuse.
Table3.8DetailRecord6:Financing/REPOTransactionOutput
ConfirmTradeOutputMessageSpecification
3.OutputRecordFormats 88

---

## Page 89

©2023DTCC.Allrightsreserved.DTCCandDTCC(Stylized)areregisteredandunregisteredtrademarksofThe
DepositoryTrust&ClearingCorporation.Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandname
bycertainaffiliatesofTheDepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitselfdoesnotprovidesuch
services.Eachoftheseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsoftheparticularcountry
orcountriesinwhichsuchentityoperates.Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,itsaffiliatesand
theservicestheyoffer.
DocDate:November27,2023
PublicationCode:TS266
Service:TradeSuiteID
Title:ConfirmTradeOutputMessageSpecification
ForMoreInformation
EmailDTCCLearningat:
DTCCLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com