---
title: "Confirm Trade Input Message Specification"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ts256_confirm_input_20231017.pdf"
pages: 86
size: "604.0 KB"
category: "TradeSuite"
ingested_on: "2026-06-05"
---

# Confirm Trade Input Message Specification

**Original File:** [ts256_confirm_input_20231017.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ts256_confirm_input_20231017.pdf)  
**Category:** TradeSuite  
**Total Pages:** 86  
**File Size:** 604.0 KB  

---

## Page 1

TradeSuiteID®
CONFIRMTRADEINPUTMESSAGE
SPECIFICATION
VERSION8.1
OCTOBER17,2023

---

## Page 2

TABLEOFCONTENTS
Preface 4
Audience 4
ChangesinThisVersion 4
RelatedDocumentsandTraining 7
Questions? 7
1.GeneralInformation 8
TradeInputFileUsingCCFandMQ 8
DataValidation 8
Mandatory,Optional,andConditionalColumn 8
Validation 9
2.InputRecordFormats 10
RecordsintheInputFile 10
LegendforAllRecordFormats 11
VersionoftheRecordFormats 11
Record1:GeneralTradeInput 11
Record2:AdditionalFixedIncomeInput 31
Record3:AdditionalPartyInput 40
Record4:Mortgage-BackedSecuritiesInput 44
Record5:SupplementalInput 55
Record6:Financing/REPOTransactionInput 69
A.FourthQuarter2005Modifications 83
Fails/[[Locate]](RegulationSHO–Rule203) 83
Section31FeeConfirmationLabel 83
ConfirmTradeInputMessageSpecification
TableOfContents 2

---

## Page 3

B.June1998Modifications 84
ConfirmTradeInputMessageSpecification
TableOfContents 3

---

## Page 4

PREFACE
ThisdocumentdescribestheTradeSuiteID ®servicetradeinputfilethatbroker/dealersusetosend
confirmation,cancellation,andresubmissiontrademessages.Itdescribestherequiredrecordformats
andexplainsmodificationsoftherecordssincethepreviousrelease.
TheTradeSuiteIDisacomprehensivetradeprocessingsolutionthatautomatesmessagingand
settlementforequityandfixedincomesecurities.Investmentmanagers([[Institutions]]),[[Broker]]/dealers,
[[Custodians]],andinterestedpartiesusetheTradeSuiteIDforpost-tradeprocessingondomesticandcross-
bordertradesofU.S.[[securities]].
Audience
Thisdocumentisforinformationtechnologyprofessionals,businessanalysts,andotherswhoare
responsibleforimplementingoroperatingthefollowingsystems:
l Computerfacility([[CCF]])
l
MessageQuerying(MQ)
Itisnecessarytounderstandthesecuritiesindustryandknowhowtheindustryhandlestrades.Youmust
haveabasicunderstandingofelectronictradeandtransactionprocessingconceptsandaworking
knowledgeoftheWindowsoperatingsystem.
Changes in This Version
ThissectiondescribesthechangesfortheConfirmInputMessageSpecification.
TradeSuite ID8.08 (newchanges)
IntheInputRecordFormatssection:
l Changed the TradeSuite [[ID]] setup contact information.
l TradeSuite has five optional records, the old specification only noted 3 optional records.
Confirm Trade Input Message Specification
Preface
4

---

## Page 5

TradeSuiteID8.07(previouslycommunicatedchanges)
l Record1:Share/FaceValue–Position82–98addedthefollowingnote:Themaximumvalueaccept-
ableforprocessingintheDTCsettlementsystemsandonlyappliestoconfirminputwithaDTC/BRC
settlementlocationis999,999,999.
l Record1:NetAmount–Position180-193addedthefollowingnote:Themaximumvalueacceptable
intheDTC/BRCsettlementsystemandapplytoconfirminputwithaDTCsettlementlocationis
$9,999,999,999.99.
TradeSuiteID8.06(previouslycommunicatedchanges)
TheMUNIEnrichmentchangestopsreplacingindividualMUNIfieldswhendatavaluesforagivenMUNI
EnrichmentDatabase(onthemainframe)containanon-blank/null/zerovaluesinConfirmTradeInput.
Inaddition,thisdocumentcontainsbetterdefinitionsfor:
l Record1:SecurityDescriptionLine1.Seepage25.
l Record2:SecurityDescriptionLines2-5.Seepage32.
TradeSuiteID8.05(previouslycommunicatedchanges)
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
thesechanges.ThisnewregulationwentintoeffectonMay14,2018.
Tocomplywiththeseregulatorychanges,DTCChasmadethefollowingchangestotheDirectInput
records:
l Record2:AdditionalFixedIncomeInputPositions462-511(fieldname:FINRAMSRBEMMAURL)
containsURLlinkstotheappropriatewebsites:FINRAorMSRB.
l Record2:AdditionalFixedIncomeInputPositions512-543(fieldname:SpecialInstructionsLine19);
Positions544-575(fieldname:SpecialInstructionsLine20);Positions576-607(fieldname:Special
InstructionsLine21).Thesefieldsarefree-formtextforthebroker/dealertoaddtotheconfirmation.
ConfirmTradeInputMessageSpecification
Preface 5

---

## Page 6

l Record5:SupplementalInputPositions616-623(fieldname: TradeExecutionDate).TheTradeExe-
cutionDatefieldmustbeinCCYYMMDD format.
l Record5:SupplementalInputPosition624(fieldname:MarkUp/MarkDownPercentageSign)can
be:
o +=Positive
o -=Negative
o Space=notsupplied
l Record5:SupplementalInputPositions625-632(fieldname:MarkUpMarkDownPercentage).Field
informationforthebroker/dealertodiscloseanypercentageoftheMarkUp/MarkDowndifference
betweenthereportedpriceandthepricetothecustomerinvolvedinthetransaction.
l Record5:SupplementalInputPositions689-708(fieldname: BrokerLegalEntityIdentifier)isaunique
alphanumericbrokeridentifier(ISO17442).ThisupdateisaMIFID II-relatedchange.
l Record5:SupplementalInputPositions709-728(fieldname: InstitutionLegalEntityIdentifier)isa
uniquealphanumericbrokeridentifier(ISO17442).ThisupdateisaMIFID II-relatedchange.
TradeSuiteID8.0.4(previouslycommunicatedchanges)
Tocomplywiththemarketsinfinancialinstrumentsdirective(MiFIDII)regulationsandallowforgreater
transparencyacrossthetradingprocess,Record1:GeneralTradeInputhasbeenupdatedwiththe
followingchanges:
l LocalTaxfieldhasbeenreplacedwiththeResearchAmountfield.SeetheResearchAmountfield.
l UsetheCountryTaxfieldforcountryandfederaltaxes.ThisfieldisalsousedfortheAmericandepos-
itaryreceipt([[ADR]])foreigntaxes.SeetheCountryTaxfield.
l UsetheOtherChargesfieldforallotherreasons.SeetheOtherChargesfield.
l CreatedICMerrorcodesrelatedtotheresearchamount.Foralistofcancellationreasoncodes,see
Input/OutputInformation.
InadditiontotheMiFID IIinitiativechanges,theappearanceandlayoutofthedocumentationhas
changedtoensureconsistencyacrossDTCC.
TradeSuiteID8.0.3(previouslycommunicatedchanges)
UpdatestothefielddescriptionsforthefollowingfieldsinRecord2:
l InterestPaymentFrequency
l SubjecttoFederalTax
l AlternateMinimumTax
ConfirmTradeInputMessageSpecification
Preface 6

---

## Page 7

TradeSuiteID8.0.2(previouslycommunicatedchanges)
l UpdatedtoAdditionalFixedIncomeInformationintheMunicipalSecurities(MUNI)printedandarchive
confirmationreportstoavoidmisinterpretation.Formoreinformation,seeInputRecordFormats
l ModifiedlinkstothedocumentationtoenableaccesstothenewlydesignedDTCCLearningCenter.
l RevampedtheappearanceandlayoutofthedocumentationtoensureconsistencyacrossallDTCC
applications.
TradeSuiteID8.0(previouslycommunicatedchanges)
ThisversionoftheConfirmInputMessageSpecificationcontainsthefollowingchangesforTradeSuiteID
8.0service:
l AddedaSellShortExempt(E)indicatortotheLong/ShortIndicatorfieldinposition66,inRecord1:
GeneralTradeInput.
l AddedaRisklessPrincipal(0-RisklessPrincipal)valuetotheRoleindicatorinposition67,inRecord
1:GeneralTradeInput.
l ExpandedtheAgentInternalAccountNumberfieldto35charactersinrecord5,inpositions576-606,
inRecord5:SupplementalInput.
l AddedtheCommissionEquivalentvalueinpositions607-615,inRecord5:SupplementalInput.
RelatedDocumentsandTraining
Forrelateddocumentsandtraining,seeTradeSuiteID®ontheDTCCLearningCenter.
Questions?
TheClientCenterprovidesgeneralassistanceandtechnicalhelp.Visitto:
l Enteraservicerequestorcheckthestatusofanexistingservicerequest.
l Searchtheknowledgebase.
l Obtaincontactinformation.
ConfirmTradeInputMessageSpecification
Preface 7

---

## Page 8

1.GENERALINFORMATION
Thissectiondescribesthetradeinputfileanddatavalidation.Italsoexplainsthemandatory,optional,and
conditionalcolumnincludedinthedatainformationtables.
TradeInputFileUsingCCFandMQ
DTCCprovidesenhancedComputer-to-ComputerFacility([[CCF]])andMessageQuerying(MQ)
processing.ThesesystemsallowforinteractivereceiptanddistributionofTradeSuiteIDdata.
Notes
l Alldetailrecordscontainatransactionheaderinpositions1-26andamailboxprefix.
l ForCCFapplication-orientederrors,TradeSuiteIDappendsamessageprefixtothefrontofthe
record.Theapplicationalsoappendsablocktotheendoftherecord.Formoreinformationsee
Input/OutputInformation.
DataValidation
DuringTradeSuiteIDdatavalidation,eachfieldshownintherecordformatsasValidate=Yesvalidates
againstseveralcriteria.Forexample,theTradeSuiteIDservicevalidatesTradeSuiteIDnumbers,
numeric,space-filledfields,zero-filledfields,andTradeSuiteIDvalues,suchasmarket.Formore
information,seeInputRecordFormats.
Theindustryconsidersfieldsthatareunabletobevalidatedassupplementalinformation.TheTradeSuite
IDservicegeneratesaconfirmevenifthesefieldscontainerroneousvalues.
DTCCrecommendsthatyouuseallofthepertinentpositions.Forexample,althoughtheTradeSuiteID
servicecannotvalidatethecontentsofpositions335–346,allsubmittingbroker/dealerssupplyinformation
inthisfield.Formoreinformation,seetheBroker/DealerInternalAccountNumberfieldinrecord1:
Generaltradeinput.AlthoughtheTradeSuiteIDservicedoesnotvalidatesupplementfields,suchas
position347,itreportsthesefieldsintact.Formoreinformation,seethePaymentStatus fieldinrecord2:
AdditionalFixedIncomeInput.
Mandatory,Optional,andConditionalColumn
TheTradeSuiteIDdatainformationtablescontainamandatory,optional,orconditional(MOC)column.
Thiscolumnprovidesinformationabouttheconfirmedtransaction.Table1.1indicatesthetypeof
ConfirmTradeInputMessageSpecification
1.GeneralInformation 8

---

## Page 9

information.
Legend Description
M Mandatory,containsessentialdetails.
SomemandatoryfieldsbecomeoptionalforWhen-IssuedorWhen-Distributedtrades.Thefielddescriptionscolumn
containsinformationabouttheimpactedfields.
O Optional,suppliesextrameaningorclarity.
C Conditional,containsinformationrequiredonlyincertaincircumstances.
Table1.1MOCColumn
Validation
ThefollowingtableshowsthelegenddescriptionfortheValidationcolumnavailableinthedetailrecord
tables.
Legend Description
Y TradeSuiteIDfieldvalidationoccurs.
N SubmittersentthedataortheMUNIEnrichmentdatabasereportsthedataasintact(notvalidated).
– TheTradeSuiteIDservicegeneratesthedata.
Table1.2ValidationColumn
ConfirmTradeInputMessageSpecification
1.GeneralInformation 9

---

## Page 10

2.INPUTRECORDFORMATS
ThissectiondescribestherecordformatsfortheTradeSuiteIDtradeinputfile.
RecordsintheInputFile
Theinteractiveinputspecificationsdescribedinthisdocumentconsistofonerequiredrecordandfive
optionalrecords.Youcanchoosetoreceivethesecondrecordforadditionalfixedincomeinformationall
ofthetimeornotatall.Youcanchoosetoreceivethethird,fourth,fifth,andsixthrecordsonanoptional
basis.
Toreceivearecord,submitacaseviaMyDTCC.TheTradeSuiteIDmasterfileallowsyoutominimizethe
amountofdatareceivedbycontrollingthetransmissionofthe2nd,3rd,4th,5thand6threcords.Table2.1
describeseachrecord.
Record Description
1 Providesgeneraltradeinformationforinputmessages.
2 ProvidesadditionalFixedIncomeinformationandmeetsthespecificrequirementsofsecuritydescriptionsfor
municipaldebtsecurities.Fivelinesof78charactersareavailableforsecuritydescriptionat:
l SecurityDescriptionLine1inrecord1,position237–314
l SecurityDescriptionLine2,3,4,and5inrecord2,positions28–339
Lines1,2,and3showwhetherMUNI Enrichmentreceivesasecuritydescriptionforadditionalfixedincome
information.Discretefieldsinrecord2,positions340–420containthesameMUNI Enrichmentinformation,mostlyin
numericvalues.
3 Relatestheinstitutioninstructionstotheconfirms.Therecordcontainsinformation,suchasinternalaccountnum-
bers,additionalinterestedparties,andinstitutionalreferencenumbers.
4 Meetsthespecificrequirementsofmortgage-backedsecuritiestrades.
5 Providessupplementaloradditionalinformationaboutaconfirm,suchas10b–10informationandadditionalspecial
instructionfields.
6 Meetsthespecificrequirementsoffinancingtransactionsregardingrepurchaseagreements(REPOs).
Table2.1InputFileRecordDescriptions
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 10

---

## Page 11

LegendforAllRecordFormats
Forallrecords,1–6,thefollowingapplies:
l CharacterX(n)—nnumberofalphanumericcharacters,includinga–z,0–9,andspecialcharacters.
l Numeric9(n)—Integercontainingnpositions.Forexample,Numeric9(8):maximumvalueof
99,999,999.Allnumericintegerfieldsareright-justifiedwithleadingzeros.
l Numeric9(x)V9(y)—Fractionalnumbercontainingxpositionstotheleftofthedecimalpointandypos-
itionstotherightoftheimplieddecimalpoint.Forexample,enterNumeric9(12)V9(5):for258.43as:
00000000025843000.Allnumericfieldswithdecimalpositionsareright-justifiedwithleadingandtrail-
ingzeros.
VersionoftheRecordFormats
IntheVersionNumberfield(position11–12)ofeachrecord,supplytheversionnumberoftherecord
format.Thecurrentversionoftherecordformatis01.
Theinputrecordsinclude:
l Record1:GeneralTradeInput
l Record2:AdditionalFixedIncomeInput
l Record3:AdditionalPartyInput
l Record4:Mortgage-BackedSecuritiesInput
l Record5:SupplementalInput
l Record6:Financing/REPOTransactionInput
Record1:GeneralTradeInput
Table2.2showsthegeneraltradeinformationforinputmessages.
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 11

---

## Page 12

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
Positions1–26:TransactionHeader
1 1 CharacterX
(1)
FeedbackIndicator O N Indicatesthereturnofthisrecord
becauseoferrors.Forafull
descriptionofthisprocessing,seethe
InterfaceControlManager.
l .*=Ifnoerrors.
l ?=Iftherecordcontainserrors.
2 1 CharacterX
(1)
Production/Test
Indicator
M Y Indicateswhethertherecordisfor
productionortest.Required.
l P=Production
l T=Test
3–8 6 CharacterX
(6)
RecordType M Y Typeofdatacontainedinthe
message.
l TRADEI=TradeInput
9–10 2 Numeric9(2) RecordSuffix M Y Identifiesthephysicalrecordnumber.
l 01=GeneralTradeInput
11–12 2 Numeric9(2) VersionNumber M Y Versionnumberthatdefinesthe
recordformat.
l VersionNumberalways=01
13–18 6 CharacterX
(6)
RecordSequence
Number
O N Uniquetransactionidentifierofthe
user(optional).Returnedonlyduring
errorreporting.
19–26 8 CharacterX
(8)
Filler – – Reserved.Donotuse.
Positions27–807:TransactionalData
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 12

---

## Page 13

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
27 1 Numeric9(1) TransactionType M Y Identifiesthetypeofconfirm
transaction.
1=NewConfirm
3=Cancellation
4=Resubmission
5=Reservedforfutureuse
Cancellationsrequire:
l Executingbroker/dealernum-
ber.
l [[Broker]]/dealerconfirmnumber
(identifyingthecancellation).
l Originalbroker/dealerconfirm
number(identifyingtheconfirm
tocancel).
l Cancellationreasoncode.
TheTradeSuiteIDserviceignoresall
otherfieldswithintheinputrecord.For
thecancellationtooccur,ensurethat
theOriginalBroker/DealerConfirm
Number(position209–220)matches
theexistingconfirm.
28 1 CharacterX
(1)
Filler – – Reserved.Donotuse.
29–36 8 Numeric9(8) Executing
[[Broker]]/DealerID
Number
M Y ValidTradeSuiteIDnumberofthe
[[Broker]]/dealerwhoexecutedthetrade.
Forexample,enter123as00000123.
Right-justified,zero-filled.
37–44 8 Numeric9(8) InstitutionIDNumberM Y ValidTradeSuiteIDnumberofthe
institutionorthepartythatplacesthe
tradeorderwiththebroker/dealer.
Right-justified,zero-filled.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 13

---

## Page 14

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
45–52 8 Numeric9(8) AgentIDNumber M Y TheTradeSuiteIDnumberofthe
agent,generallyacustodianbank,
responsibleforreceivingor
deliveringthesecuritiesonbehalfof
theinstitutionoritscustomer.Must
beavalidAgentTradeSuiteID
number.Rightjustified,zerofilled.
TheTradeSuiteIDmasterfilecan
overwritethisagentID numberifthe
Institutionishard-codedtoanagent
IDnumber.
53–64 12 CharacterX
(12)
SecurityIdentifier M Y Securityidentificationnumber
assignedtothetradedsecurity.Usea
validCUSIP,SEDOL,orISINnumber
whentheSecurityNumberingSystem
field(position204–205)isUS,GB,or
ISrespectively.TheTradeSuiteID
servicevalidatesthisfieldonlywhen
theSecurityNumberingSystemfield
(position204–205)isCUSIP(U.S.),
SEDOL(GB),orISIN(IS).
l 53–54X(02)=ISINcountry
codeforISINonly;otherwise,
spaces.
l 55–63X(09)=securitynumber:
l SEDOL
l ISIN
l [[CUSIP]]
l 64–64X(01)=ISINcheckdigit
forISINonly;otherwise,
spaces.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 14

---

## Page 15

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
65 1 Numeric9(1) SettlementType M Y Indicateshowthetradeistosettle.
RegularWaytradessettleaccording
tolocalmarketconventions.For
example,intheU.S.,tradesin
corporatesecuritiesandmunicipal
bondssettlethreebusinessdaysafter
thetradedate(T+3).Theinitialpublic
offering([[IPO]])usesthethreeother
categories.
1=RegularWay
2=When-Issued
3=When-Distributed
4=When-IssuedorWhen-Distributed
TheTradeSuiteIDservicerequires
thisfieldtodeterminethepossible
valuesforseveralfieldsnotedon
succeedingfields.Thisfieldcan
containzerosforWhen-Issuedor
When-Distributedtrades.Suchfields
are:
l [[shares]]/FaceValue(position
82–98)
l Price(position99–109)
l PrincipalAmount(position110–
123)
l SettlementDate(position231–
236)
66 1 CharacterX
(1)
Long/ShortIndicatorC Y l L=SellLong
l S=SellShort
l E=SellShortExempt
l Spaces=Unavailableornot
applicable
Mandatoryfieldforallprimebrokers
–selltrades.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 15

---

## Page 16

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
67 1 CharacterX
(1)
Role M Y Identifiestheroleofthebroker/dealer
asoneofthefollowing:
1=Executingbroker/dealeractsas
agentforthecustomer(AGNT).
2=Executingbroker/dealeractsas
principalfortheirownaccount(PRIN).
3=Executingbroker/dealeractsas
agentforapersonotherthanthe
customer(OTHR).
4=Executingbroker/dealeractsas
agentforboththecustomerand
anotherperson(CUST).
5=Averagepricetrade;the
[[Broker]]/dealeractsasprincipalfor
someexecutionsandagentforothers
inthetransaction(AVGR).
6=Executingbroker/dealeractsas
bothprincipalandagentinthe
transaction(PRAG).
7=Executingbroker/dealeractsas
principal,agent,andagentforanother
personinthetransaction(PAGC).
8=Crossingasagent-Executing
[[Broker]]/dealeriscrossingtransaction
asanagentonbehalfofthecustomer
(CAGN).
9=Crossingasprincipal-Executing
[[Broker]]/dealersarecrossing
transactionasprincipalfortheirown
account(CPRN).
A=Actingasrisklessprincipal-
Executingbroker/dealeristradingasa
risklessprincipal.Thatis,theorderto
buy(sell)iscontemporaneouslyoffset
byanordertosell(buy)withanother
party(RISP).
Whenappropriate,theTradeSuiteID
Inquiryscreensdisplaycharacter
values,suchasPRINandAVGR,that
followtheexplanation.
Note:Theaveragepriceindicator
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 16

---

## Page 17

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
usedfortradeswherethe
[[Broker]]/dealerfillstheorderwitha
numberofsmallerexecutions.When
theaveragepriceistherole,the
[[Broker]]/dealeractsastheprincipalfor
someexecutionsandagentforothers
inthetransaction.
WhenusedintheMarketCodefield
(position68–69),
l AVGPindicatesthattheorder
occursovermultipleexe-
cutions.
l AVGRindicatesthattheorder
occursacrossmultipleexe-
cutionsinmultipleexchanges,
suchasNYSE,[[NASDAQ]],and
[[OTC]].
Pricesofindividualtradeexecutions
areavailablefromtheexecuting
[[Broker]]/dealeruponwrittenrequest.
Note:Toallowformorefieldvalues,
theTradeSuiteIDservicechangedthe
dataformatfromNumeric9(1)to
Alpha/Numeric-CharacterX(1).
68–69 2 CharacterX
(2)
MarketCode M Y Marketinwhichthetradewas
executed.WhenusedintheMarket
Codefield,AveragePriceindicates
thattheorderexecutesovermultiple
markets,suchasNYSE,[[NASDAQ]],or
[[OTC]].Ifthevalueisinvalid,the
TradeSuiteIDservicerejectsthe
record.Foralistofmarketcodes,see
Input/OutputInformation.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 17

---

## Page 18

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
70 1 Numeric9(1) SideCode M Y Indicateswhethertheinstitution
boughtorsoldtheunderlying
[[securities]].
l
1=SELL;[[Broker]]/dealeris
receiving
Iftheinstitutionisselling,the
submittingbroker/dealeris
thereceiverandtheinstitution
oftheagentisthedeliverer.
l
2=BUY;[[Broker]]/dealeris
delivering
Iftheinstitutionisbuying,the
submittingbroker/dealeris
thedelivererandthe
institutionoftheagentisthe
receiver.
71–81 11 Numeric9
(5)V9(6)
NetPrice O Y Differencebetweenthequotedprice
andthemark-upormark-down(rule
10b–10).Right-justified,zero-filled.
82–98 17 Numeric9
(12)V9(5)
[[shares]]/FaceValue M Y Numberofsharesforequityissuesor
thefacevalueofdebtissues.
Maximumof9integerswithleading
zeros.Forsettlement,enterzerofor
fractions.Thisfieldallowszerosfor
When-IssuedandWhen-Distributed
settlementtypes.Forothersettlement
types,thevalueisgreaterthanzero.
Right-justified,zero-filled.
Note:Themaximumvalueacceptable
forprocessingintheDTCsettlement
systemsandonlyappliestoconfirm
inputwithaDTC/BRCsettlement
locationis999,999,999.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 18

---

## Page 19

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
99–109 11 CharacterX
(11)
Price M Y Pricepershareatwhichthissecurity
trades,exclusiveofcommissionand
othercharges.Thisfieldcancontaina
floatingdecimalinanyposition;all
otherpositionsarenumeric.Whole
numbersdonotrequireadecimal
point(10b–10field).Ifthereisno
embeddeddecimal,TradeSuiteID
assumesawholenumber.
ThisfieldallowszerosforWhen-
IssuedandWhen-Distributed
settlementtypes.Forothersettlement
types,thevalueisgreaterthanzero.
PricePerSharecanbeX(11)onuser
input.TheTradeSuiteIDservice
convertsto9(5)V9(6)forinternal
processing,andthenbacktoX(11)on
output.Right-justified,zero-filled.
110–123 14 Numeric9
(12)V99
PrincipalAmount M Y [[shares]]/FaceValuemultipliedbythe
Price.Thisfieldallowszerosfor
When-IssuedandWhen-Distributed
settlementtypes.Forothersettlement
types,thevalueisgreaterthanzero.
Right-justified,zero-filled.
124–132 9 Numeric9
(7)V99
Registration/
ShippingorFees
O Y Statutoryfeeleviedonthesaleof
equitysecuritiesregisteredonan
exchangeorcertainequitysecurities
inOTCmarketsintheUnitedStates.
Usetoreportregistrationorshipping
costsforsecuritiessettlingoutsidethe
UnitedStates.Right-justified,zero-
filled.
133–143 11 Numeric9
(9)V99
Interest O Y Interestaccruedonadebtinstrument
(bond)accountedforatthetimeof
sale.Right-justified,zero-filled.
144–152 9 Numeric9
(7)V99
ResearchAmount O Y Thecostoftheresearchprovidedby
thesell-side.Rightjustified,zerofilled.
Note:ThisMiFIDIIfieldreplacedthe
LocalTaxfield.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 19

---

## Page 20

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
153–161 9 Numeric9
(7)V99
CountryTax O Y Countryandfederaltaxesthatapply
tothistransaction.Right-justified,
zero-filled.
ThisCountryTaxfieldisalsousedfor
theAmericandepositaryreceipt
([[ADR]])foreigntaxes.
162–170 9 Numeric9
(7)V99
Commission O Y Feeeitherdirectlychargedbythe
[[Broker]]/dealertoitscustomeror
allocatedtothistransaction.Right-
justified,zero-filled.
171–179 9 Numeric9
(7)V99
OtherCharges O Y Sumofanychargesthatapplytothis
tradeforwhichnootherfieldhasbeen
designated.Right-justified,zero-filled.
180–193 14 Numeric9
(12)V99
NetAmount M Y Cashsettlementamountthatisthe
sumoftheprincipalamountand
interest,plusorminusthefollowing
cashfields:
l Registration/ShippingorFees
l ResearchAmount
l CountryTax
l Commission
l OtherCharges
ThisfieldallowszerosforWhen-
IssuedandWhen-Distributed
settlementtypes.Forothersettlement
types,thevalueisgreaterthanzero.
Right-justified,zero-filled.
Note:Themaximumvalueacceptable
intheDTCsettlementsystemand
applytoconfirminputwithaDTC/BRC
settlementlocationis
$9,999,999,999.99.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 20

---

## Page 21

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
194–196 3 CharacterX
(3)
ExpandedSecurity
Type1
M Y Typeofsecuritythatisthesubjectof
thetrade.TheTradeSuiteIDservice
usesthesecuritytypetogenerate
settlementinstructions.
Forafulllistofsecuritytypes,see
Input/OutputInformation.
197 1 CharacterX
(1)
Filler – – Reserved.Donotuse.
Note: Withtheeliminationofthe
BypassSIDindicator,thisfieldisno
longerused.
198 1 CharacterX
(1)
SplitCurrency
SettlementIndicator
O Y Identifieswhensecuritiesandcash
settleindifferentlocations.
l Y=Yes
l N=No
199 1 CharacterX
(1)
QualityControl
ReportingExempt
Indicator
O N Indicateswhethertoexcludethe
confirmfromtheQualityControl
report.
l Y=Excludefromthereport.
l Spaces=Includeinthereport.
Thisfieldallowsexceptionstothe
QualityControlreport.Forexample,if
thetradedoesnotfallunderFINRA
rule11860,NASDrule64,or
MunicipalSecuritiesRulemaking
Board(MSRB)ruleG-15,the
[[Broker]]/dealercanexcludethe
confirmationinthereport.
Table2.2Record1:GeneralTradeInput
1TheTradeSuiteIDattemptstoobtainsecuritydescriptionsandfieldsfromtheMUNIenrichmentdatabaseforDTC-eligiblemunicipalsecuritiesandforanysecuritythe
submitteridentifiesasamunicipalsecurity(securitytype=MUN).Whenidentified,thedatafromtheMUNIenrichmentdatabasereplacestheExecutingBroker'sdata.
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 21

---

## Page 22

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
200 1 CharacterX
(1)
AllocationSource O Y [[Broker]]/dealeridentifiesordiscloses
thesourceorsystemtheinvestment
managerusestosendtheallocation
tothebroker/dealertoprocessthe
tradeconfirmation.Ifsupplied,enter
oneofthefollowingvalidvalues:
1=NA
2=TradeXpress(TradeWeb)
3=FIX
4=MarketAxess
5=Manual(phoneorfax)
Space=Notsupplied
201–203 3h CharacterX
(3)
SettlementLocation M Y Countryordepositorywherethe
securityistosettle.OutsideoftheUS,
settlementlocationsarebycountry,
exceptforEuroclearandCEDEL
(Clearstream).Left-justified,space-
filled.
Herearetheprimaryvalues.
l [[DTC]]=TheDepositoryTrust
Company
l BRC=Brokercustody([[DTC]]
tradeswherebroker/dealeris
alsothecustodian/agent).
l CED=CEDEL(Clearstream)
l EUR=Euroclear
l FED=TheFederalReserve
BankofNewYork
l NFS=Notforsettlement
l US=U.S.physical
ForISOcountrycodesandcountryof
[[settlement]],seeInput/Output
Information.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 22

---

## Page 23

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
204–205 2 CharacterX
(2)
SecurityNumbering
System
M Y Nationaloruser-originatednumbering
systemassociatedwiththesecurity
identifierintheSecurityIdentifierfield
(positions53–64).Thesystem
defaultstothesecurityidentifierused
bythebroker/dealerontradeinput.
However,thesystemallowsthe
outputrecipienttochangethedefault
toanyoftheotherallowablesecurity
numberingsystems.
Forafulllistofthesecuritynumbering
system,seeInput/OutputInformation.
DatainputofSEDOL(GB),ISIN(IS),
orCUSIP(U.S.)inthisfield
automaticallymakestheSecurity
Identifier(positions53–64)arequired
field.Thedatamustadheretothe
formatconventionsofthatnumbering
system,suchascheckdigit.Ifthe
valueisinvalid,theTradeSuiteID
rejectstherecord.
Thesystemallowsyoutooverridethe
defaultbysettlementlocation.For
example,setadefaultforSEDOL
numbersforallsettlementlocations
exceptClearstream,whichprefers
receivingthemessagesusingthe
Luxembourgcode.
ForDTC-eligibletrades,thesystem
defaultstoanon-editableCUSIP
numberforalloutputmessagestothe
clearingagentsandclearingbrokers
responsibleforsettlingthetradein
[[DTC]].
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 23

---

## Page 24

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
206–208 3 CharacterX
(3)
CurrencyCode M Y Validcurrencydenominationofthe
securitytradedandnetamount.Ifthe
valueisinvalid,theTradeSuiteID
servicerejectstherecord.
Ifthetradeistosettleinacurrency
otherthanthecurrencyofthesecurity,
reporttheAlternateCurrency
ConversionRatefield(position763–
789).Foralistofcurrencycodes,see
Input/OutputInformation.
209–220 12 CharacterX
(12)
Original
[[Broker]]/Dealer
ConfirmNumber
C Y Uniqueinternaltransactionnumbers,
assignedbythebroker/dealerona
priorconfirmthatwasreissuedforthis
trade.
RequiredifTransactionType=3
(Cancellation).
221–224 4 CharacterX
(4)
Filler – – Reserved.Donotuse.
225–230 6 Numeric9(6) TradeDate M Y Dateonwhichthetransaction
executesasreportedbythe
[[Broker]]/dealer,inMM/DD/YYformat.
ForsettlementintheUS,thetrade
dateislessthanorequaltothe
currentdate.Else,thetradedate
cannotexceedthecurrentdate,U.S.
EasternStandardTimebymorethan
oneday.Forallsettlementlocations,
thetradedatecannotbelessthanthe
currentdateminus250days.
231–236 6 Numeric9(6) SettlementDate M Y Date,inMM/DD/YYformat,whenthe
tradeisduetosettle.Thesettlement
dateisgreaterthanorequaltothe
tradedate.ForWhen-Issuedor
When-Distributedtrades,thevalue
canbezero.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 24

---

## Page 25

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
237–314 78 CharacterX
(78)
SecurityDescription
Line1 1
O N Nameofthesecuritytraded.Four
additional78-characterdescriptions
areavailableinRecord2.
315–316 2 Numeric9(2) AccountType M Y Typeorclassofaccountinwhichthe
[[Broker]]/dealerrecordedthetrade.
Allowedvaluesare:
02=Cashaccountsthatsettleon
apayment-on-delivery(POD)or
collect-on-delivery(COD)basis.
05=Shortsaleaccounts.
09=Marginaccountsforwhich
thebroker/dealerprovidesthe
financing.
10=Primebroker/dealeraccounts
whereabroker,actingasa
clearer,directsotherbrokersto
executethetrade.Formore
information,seeOperating
Procedures.
99=Othermiscellaneousaccount
types.
Allfivevaluesfallwithinrule
387/[[NASD]],rule64/MSRB,andruleG-
15.QualityControlreportsthevalues.
317–319 3 CharacterX
(3)
Filler – – Reserved.Donotuse.
320–322 3 Numeric9(3) Cancellation/
CorrectionReason
Code
O Y Reasonforcorrectionorcancellation.
Enterareasoninthisfieldwhen
TransactionType=3(Cancellation).
Forafulllist,seeInput/Output
Information.
Table2.2Record1:GeneralTradeInput
1 TheTradeSuiteIDattemptstoobtainsecuritydescriptionsandfieldsfromtheMUNIenrichmentdatabaseforDTC-eligiblemunicipalsecuritiesandforanysecuritythe
submitteridentifiesasamunicipalsecurity(securitytype=MUN).Whenidentified,thedatafromtheMUNIenrichmentdatabasereplacestheExecutingBroker'sdata.
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 25

---

## Page 26

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
323–334 12 CharacterX
(12)
AgentInternal
AccountNumber 1
O N Agent'sinternalaccountnumber
(AIA).Limitedtothefirst12characters
oftheagentinternalaccountnumber.
Usethisfieldwhentheagentinternal
accountnumberis12charactersor
lessandwhentheAgentInternal
AccountNumberinrecord5,position
572containsjustspaces.If
unavailableornotprovided,setto
spaces.Free-formtext.
335–346 12 CharacterX
(12)
[[Broker]]/Dealer
InternalAccount
Number
O N Internalaccountnumberofthebroker-
/dealer.Free-formtext.
347–358 12 CharacterX
(12)
[[Broker]]/Dealer
ConfirmNumber
M Y Uniqueinternaltransactionnumber
assignedtothetradebytheexecuting
[[Broker]]/dealer,whichdiffersfromthe
controlnumberassignedby
TradeSuiteID.
Forcancellations,thisreference
numberisdifferentfromtheone
reportedintheoriginalconfirm.Free-
formtext.
Table2.2Record1:GeneralTradeInput
1Whenmatchingatrade,theALERT®platformcanfillorreplacethedatainthisfield.
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 26

---

## Page 27

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
359–390 32 CharacterX
(32)
SpecialInstruction 1O N Free-formtextforthebroker/dealerto
addtotheconfirmation.Fillunused
specialinstructionfieldswithspaces.
Forspecialinstructionsaboutusing
codesandinformationrelatedto10b–
10requirements,seeOperating
Procedures.
391–422 32 CharacterX
(32)
SpecialInstruction 2O N
423–454 32 CharacterX
(32)
SpecialInstruction 3O N
455–486 32 CharacterX
(32)
SpecialInstruction 4O N
487–518 32 CharacterX
(32)
SpecialInstruction 5O N
519–550 32 CharacterX
(32)
SpecialInstruction 6O N
551–582 32 CharacterX
(32)
SpecialInstruction 7O N
583–614 32 CharacterX
(32)
SpecialInstruction 8O N
615–621 7 CharacterX
(7)
Filler – – Reserved.Donotuse.
622 1 CharacterX
(1)
SecurityFormCode O N Securityformcode.
0=UndeterminedSecurityForm
Code
1=NotBearerBond
2=BearerBond
623–630 8 Numeric9(8) InterestedParty #1
[[ID]]
Number1
O Y IDnumberfortheinterestedparty
number1orbroker/dealersub-
custodian.
Zero-filledwhenthereisnointerested
partynumber1orbroker/dealersub-
custodian.Thebroker/dealersub-
custodianisoptional.
Right-justified,zero-filled.
631–642 12 CharacterX
(12)
InterestedParty #1
AccountNumber1
O N Interestedpartynumber1or
[[Broker]]/dealersub-custodianaccount
number.
Free-formtext.
Table2.2Record1:GeneralTradeInput
1 Whenmatchingatrade,theALERTplatformcanfillorreplacethedatainthisfield.
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 27

---

## Page 28

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
643–667 25 CharacterX
(25)
InterestedParty #1
InstructionLine 1
O N TextthatappearsonConfirmation
InstructionLine1associatedwith
interestedpartynumber1or
[[Broker]]/dealersub-custodian.Thisfield
isusuallyforthebeneficialnameof
theaccount.Free-formtext.
668–692 25 CharacterX
(25)
InterestedParty #1
InstructionLine 2
O N TextthatappearsonConfirmation
InstructionLine2associatedwith
interestedpartynumber1or
[[Broker]]/dealersub-custodian.Thisfield
isusuallyforthebeneficialnameof
theaccount.Free-formtext.
693–700 8 Numeric9(8) InterestedParty #2
IDNumber1
O Y IDnumberforinterestedpartynumber
2oragentsub-custodian.
Zero-filledwhennointerestedparty
number2oragentsub-custodian.
Agentsub-custodianisoptional.
Right-justified,zero-filled.
701–712 12 CharacterX
(12)
InterestedParty #2
AccountNumber1
O N Interestedpartynumber2oragent
sub-custodianaccountnumber.Free-
formtext.
713–737 25 CharacterX
(25)
InterestedParty #2
InstructionLine 1
O N TextthatappearsontheConfirmation
InstructionLine1associatedwith
interestedpartynumber2oragent
sub-custodian;usuallyforbeneficial
nameofaccount.Free-formtext.
738–762 25 CharacterX
(25)
InterestedParty #2
InstructionLine 2
O N TextthatappearsontheConfirmation
InstructionLine2associatedwith
interestedpartynumber2oragent
sub-custodian;usuallyforbeneficial
nameofaccount.Free-formtext.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 28

---

## Page 29

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
763–772 10 Numeric9
(5)V9(5)
AlternateCurrency
ConversionRate
O Y Conversionrateforthealternate
currencyspecifiedfortheconfirm,
whenspecified.Usetheconversion
rate:
l Forinformationpurposeswith
theAlternateCurrencyCode
field.
l Forsettlementpurposeswith
boththeAlternateCurrencyISO
CodeandAlternateCurrency
NetAmountfields.
Zero-filledwhenunused.
773–775 3 CharacterX
(3)
AlternateCurrency
ISOCode
C Y Ifthetradeistosettleinacurrency
differentfromthecurrencyofthe
security(positions206–208),usethis
field.UsethisfieldwiththeAlternate
CurrencyConversionRatefieldfor
informationpurposes.
IftheAlternateCurrencyConversion
RateandAlternateCurrencyNet
Amountfieldsarezeros,enterspaces.
Otherwise,thisfieldcontainsavalid
ISOcurrencycode.
Tocommunicateonlyaforeign
exchangeraterelativetothetrade,
usetheAlternateCurrencyISOCode
withtheAlternateCurrency
ConversionRate,positions763–772.
Ifthesecuritytradedisdifferentfrom
thelistedcurrencyforthesettlement,
completeallthreealternatefields,
positions763–789.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 29

---

## Page 30

Position Length Format Field
Name
M/O
/C
Vali-
date
FieldDescription
776–789 14 Numeric9
(12)V99
AlternateCurrency
NetAmount
O Y AlternateCurrencyNetAmount,
coupledwiththeAlternateCurrency
ISOCodefield,designatesthe
alternatesettlementamountwhen
differentfromthecurrencyofthe
security.
Zero-filledwhenthesecurityisto
settleinthecurrencyshownin
positions206–208.
790–807 18 Numeric9
(6)V9(12)
Amortized/
AccreditedFactor
O Y Prorationoftheoutstandingprincipal
balanceonpass-throughGinnieMae,
FreddieMac,FannieMae,and
mortgage-backedsecuritytoits
originalprincipalbalanceexpressed
asadecimal.Right-justified,zero-
filled.
Table2.2Record1:GeneralTradeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 30

---

## Page 31

Record2:AdditionalFixedIncomeInput
Table2.3showstheadditionalfixedincomeinformationforinputmessages.
PositionLength Format FieldName M
O
C
ValidateFieldDescription
Positions1–26:TransactionHeader
1 1 Character
X(1)
Feedback
Indicator
O N Indicatesthereturnofthisrecordbecauseof
errors.Forafulldescriptionofthisprocessing,
seetheInterfaceControlManager.
l .*=Ifnoerrors.
l ?=Iftherecordcontainserrors.
2 1 Character
X(1)
Production/Test
Indicator
M Y Indicateswhethertherecordisforproductionor
test.Required.
l P=Production
l T=Test
3–8 6 Character
X(6)
RecordType M Y Typeofdatacontainedinthemessage.
l TRADEI=TradeInput
9–10 2 Numeric9
(2)
RecordSuffix M Y Identifiesthephysicalrecordnumber.
l 02=AdditionalFixedIncomeInformation
Input
11–12 2 Numeric9
(2)
VersionNumberM Y Versionnumberthatdefinestherecordformat.
l VersionNumberalways=01
13–18 6 Character
X(6)
Record
Sequence
Number
O N Uniquetransactionidentifieroftheuser
(optional).Returnedonlyduringerrorreporting.
19–26 8 Character
X(8)
Filler – – Reserved.Donotuse.
Positions27–807:TransactionalData
27 1 Character
X(1)
Filler – – Reserved.Donotuse.
Table2.3Record2:AdditionalFixedIncomeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 31

---

## Page 32

PositionLength Format FieldName M
O
C
ValidateFieldDescription
28–105 78 Character
X(78)
Security
DescriptionLine 
2 1
O N Issuerandissueelementsthatcanbe
segmentedintotwomore78-characterfields.
Theseelementsaremergedwiththe78-
characterdescriptionfromthefirstdetail
record.Theelementscouldinclude:.
l Nameofissuer
l Issuerlocation
l Titleofcompany
l Descriptionofobligororlienposition
l Revenuetypeandallotherapplicable
MunicipalSecuritiesRulemakingBoard
(MSRB)dataelements,asrequired
Free-formtext.
106–183 78 Character
X(78)
Security
DescriptionLine 
3 *
O N
184–261 78 Character
X(78)
Security
Description
Line 4*
O N Twomore78-characterfields.Thefirstthree
linesoftheSecurityDescriptionfieldcontain
datafurnishedbyDTCorobtainedfromthe
MUNI enrichmentdatabase.Thebroker/dealer
canuselines4and5forextrainformation.If
securitydescriptionsareunavailablefromthe
DepositoryTrustCompany([[DTC]])orfromthe
MUNIenrichmentdatabase,thebroker/dealer
canuseallfivelinesforthesecuritydescription.
Freeformtext.
262–339 78 Character
X(78)
Security
Description
Line 5*
O N
340–344 5 Numeric9
(2)V9(3)
DiscountRate  O N Rateatwhichthetradewasdiscounted.
345 1 Character
X(1)
Filler – – Reserved.Donotuse.
346 1 Character
X(1)
LegalStatus  O N 0=Undetermined/nolegalstatus
1=MSRBex-legal
Table2.3Record2:AdditionalFixedIncomeInput
1TheTradeSuiteIDserviceattemptstoobtainsecuritydescriptionsandfieldsfromtheMUNI Enrichment
databaseforDTC-eligiblemunicipalsecuritiesandforanysecuritythesubmitteridentifiesasamunicipalsecurity
(securitytype=MUN).Whenidentified,thedatafromtheMUNIenrichmentdatabasereplacestheExecuting
[[Broker]]'sdata.Theenrichmentprocessdoesnotreplacebrokervalueswithzeroorblankwhenthebrokerhas
providedavalue.
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 32

---

## Page 33

PositionLength Format FieldName M
O
C
ValidateFieldDescription
347 1 Character
X(1)
PaymentStatus O N 0=Undetermined/nopayment
1=Noperiodicpayments
2=Callablebelowmaturityvalue
3=Non-registeredsecurity
4=Noperiodicpayments,callablebelow
maturityvalue
348 1 Character
X(1)
BondTypeCode O N 0=Undetermined/nobondtype
1=Generalobligation
2=Revenuebond
3=G.O./limitedtax
349 1 Character
X(1)
BasisIndicator O N 0=Undetermined/Nobasis
1=Yieldbasis
2=Dollarbasis
3=Parbasis
4=Discountbasis
350–351 2 Character
X(2)
ResultIndicator *O N 00=Undetermined/noresult
01=Pricetocall
02=Pricetoparoption
03=Pricetomaturity
04=Yieldtocall
05=Yieldtoparoption
06=Yieldtomaturity
07=Parbasis
352–357 6 Character
X(6)
InterestAccrual
Date *
O N Interestaccrualdate,inMMDDYYformat.
358–363 6 Character
X(6)
InterestPayment
Date *
O N Interestpaymentdate,inMMDDYYformat.
Table2.3Record2:AdditionalFixedIncomeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 33

---

## Page 34

PositionLength Format FieldName M
O
C
ValidateFieldDescription
364–368 5 Numeric9
(2)V9(3)
InterestRate* O N IftheSpecialCouponIndicator(position406)
fromtheMUNIenrichmentdatabaseequals0
(NoSpecialCoupon)or3(AdjustableRate),
theTradeSuiteIDserviceusesthe
[[Broker]]/dealersuppliedvaluefortheinterest
rateinsteadofthevaluefromtheMUNI
enrichmentdatabase.
Ifthebroker/dealerdoesnotsupplydata,the
MUNIenrichmentdataisused,regardlessof
thisindicator.
369–374 6 Character
X(6)
MaturityDate* O N Dateonwhichtheprincipalamountofthe
securitybecomesdueandpayablebythe
[[issuer]],inMMDDYYformat(10b–10field).
375–376 2 Character
X(2)
OptionCall
Indicator*
O N 00=Undetermined/nooptionalcall
01=Callableatapremium
02=Callableatpar
03=Callableatadiscount
04=Pre-refunded
05=Escrowedtomaturity
06=Noncallable
07=Callable,featureunavailable(10b–10
field)
377 1 Character
X(1)
Call/PutFeature
Indicator*
O N 0=Undetermined/NoCall/PutFeatures
1=Callable
2=Puttable
3=CallableandPuttable
4=Retired(10b–10field)
Table2.3Record2:AdditionalFixedIncomeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 34

---

## Page 35

PositionLength Format FieldName M
O
C
ValidateFieldDescription
378–379 2 Character
X(2)
PutBondType* O N 00=Undetermined/noputbondtype
01=Conditionalput
02=Limitedput
03=Optionalput
04=Mandatoryrepurchase
05=Mandatoryput
380–385 6 Character
X(6)
Prerefundedor
CallDate*
O N Prerefundeddateormaturitydate,fixedbycall
notice,inMMDDYYformat(10b–10field).
386–391 6 Character
9(3)V9(3)
Prerefundedor
CallPrice *
O N Amountoftheprerefundedorcallprice(10b–
10field).
392–397 6 Character
X(6)
PutBondDate * O N Maturitydatefixedbyputnotice,inMMDDYY
format.
398–403 6 Numeric9
(3)V9(3)
PutBondPrice *O N Amountoftheputbondprice.
404 1 Character
X(1)
BondForm
Code *
O N 0=Undetermined/NoBondForm
1=Fullyregistered
2=Book-entryonly
3=Registeredastoprincipalonly
4=Custodialreceipts
405 1 Character
X(1)
InterestPayment
Frequency *
O N 0=Undeterminedfrequency
1=Annual
2=Semi-annual
3=Quarterly
4=Monthly
5=Weekly
6=Biweekly
7=Interestatmaturity
8=Noperiodicinterest
9-Unknown
Table2.3Record2:AdditionalFixedIncomeInput
*TheTradeSuiteIDserviceattemptstoobtainsecuritydescriptionsandfieldsfromtheMUNIEnrichment
databaseforDTC-eligiblemunicipalsecuritiesandforanysecuritythesubmitteridentifiesasamunicipalsecurity
(securitytype=MUN).Whenidentified,thedatafromtheMUNIenrichmentdatabasereplacestheExecuting
[[Broker]]'sdata.Theenrichmentprocessdoesnotreplacebrokervalueswithzeroorblankwhenthebrokerhas
providedavalue.
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 35

---

## Page 36

PositionLength Format FieldName M
O
C
ValidateFieldDescription
406 1 Character
X(1)
SpecialCoupon
Indicator *
O N 0=Undetermined/nospecialcoupon
1=Zerocoupon
2=Originalissuediscount
3=Adjustablerate
4=Couponbearing
5=Steppedcoupon
407 1 Character
X(1)
Flat/[[default]]
Status *
O N 0=Undetermined/noflat/defaultstatus
1=Flat
2=Flat/indefault
408 1 Character
X(1)
TaxStatus * O N 0=Undetermined/notaxstatus
1=Taxable
2=Non-taxable
409–411 3 Character
X(3)
Filler – – Reserved.Donotuse.
412–413 2 Character
X(2)
Moody'sCredit
Rating *
O N Moody'sCreditRating.
Foralistofvalues,seeInput/Output
Information.
414–416 3 Character
X(3)
Filler – – Reserved.Donotuse.
417–418 2 Character
X(2)
Standard&
Poor'sCredit
Rating *
O N Standard&Poor'sCreditRating.
Foralistofvalues,seeInput/Output
Information.
419 1 Character
X(1)
Subjectto
FederalTax *
O N l 0orspaces=Undetermined
l Y=Yes
l N=No
Table2.3Record2:AdditionalFixedIncomeInput
*TheTradeSuiteIDserviceattemptstoobtainsecuritydescriptionsandfieldsfromtheMUNIEnrichment
databaseforDTC-eligiblemunicipalsecuritiesandforanysecuritythesubmitteridentifiesasamunicipalsecurity
(securitytype=MUN.Whenidentified,thedatafromtheMUNIenrichmentdatabasereplacestheExecuting
[[Broker]]'sdata.Theenrichmentprocessdoesnotreplacebrokervalueswithzeroorblankwhenthebrokerhas
providedavalue.
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 36

---

## Page 37

PositionLength Format FieldName M
O
C
ValidateFieldDescription
420 1 Character
X(1)
Alternate
MinimumTax *
O N l 0orspaces=Undetermined
l Y=Yes
l N=No
421–431 11 Character
X(11)
CurrentYield O N Informationforbroker/dealertodisclosethe
currentyieldofthefixedincomesecurity
involvedinthetransaction.
Expectedcharactersincludenumbers(0
through9),onedecimalpoint,andeitherone
plus(+)orminus(-)indicatorintherightmost
position.Cancontainafloatingdecimalinany
position;allotherpositionsarenumeric.Whole
numbersdonotrequireadecimalpoint(10b–
10field).Ifthereisnoembeddeddecimal,the
TradeSuiteIDserviceassumesawhole
number.Ifnotsupplied,thisfieldallowsspaces.
Ifsupplied,numericonlyvalues.Valid
examplesare:
l 008.897000-
l 002.097000-
Right-justified,zero-filled.
Note:Thisfieldwillbevalidatedinthefuture.
Enforcementwilloccuratalaterdate.
Table2.3Record2:AdditionalFixedIncomeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 37

---

## Page 38

PositionLength Format FieldName M
O
C
ValidateFieldDescription
432–442 11 Character
X(11)
YieldtoMaturityO N Informationforthebroker/dealertodisclosethe
yieldtomaturityofthefixedincomesecurity
involvedinthetransaction.
Expectedcharactersincludenumbers(0
through9),onedecimalpoint,andeitherone
plus(+)orminus(-)indicatorintherightmost
position.Thisfieldcancontainafloating
decimalinanyposition;allotherpositionsare
numeric.Wholenumbersdonotrequirea
decimalpoint(10b–10field).Ifnotsupplied,this
fieldallowsspaces.
Ifsupplied,numericonlyvalues.Valid
examplesare:
l 008.897000-
l 002.097000-
Right-justified,zero-filled.
Note:Thisfieldwillbevalidatedinthefuture.
Enforcementwilloccuratalaterdate.
443–453 11 Character
X(11)
YieldtoCall/
Redemption
O N Informationforthebroker/dealertodisclosethe
currentyieldofthefixedincomesecurity
involvedinthetransaction.
Expectedcharactersincludenumbers(0
through9),onedecimalpoint,andeitherone
plus(+)orminus(-)indicatorintherightmost
position.Cancontainafloatingdecimalinany
position;allotherpositionsarenumeric.Whole
numbersdonotrequireadecimalpoint(10b–
10field).Ifthereisnoembeddeddecimal,the
TradeSuiteIDserviceassumesawhole
number.Ifnotsupplied,thisfieldallowsspaces.
Numericonlyvalues,ifsupplied.Valid
examplesare:
l 008.897000-
l 002.097000-
Right-justified,zero-filled.
Note:Thisfieldwillbevalidatedinthefuture.
Enforcementwilloccuratalaterdate.
Table2.3Record2:AdditionalFixedIncomeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 38

---

## Page 39

PositionLength Format FieldName M
O
C
ValidateFieldDescription
454–461 8 Character
X(8)
DatedDate O N Informationforthebroker/dealertoidentifythe
dateddateofthefixedincomesecurityinvolved
inthetransaction,inYYYYMMDDformat.If
supplied,enteravaliddate.Spaces=Not
supplied
462–511 50 Character
X(50)
FINRAMSRB
EMMAURL
O N Ifprovided,thisfieldcontainstheURLlinkto
theMSRBElectronicMunicipalMarket
Access.
MSRBURLshouldbeahyperlinktoMSRB
WebSite:
(SampleweblinkCUSIP0006449ER9:
http://www.emma.msrb.org/[[CUSIP]]/006449ER
9
FINRAURLshouldbeahyperlinktoFINRA
WebSite:
(SampleweblinkCUSIP01F0224B8:
https://bondfacts.[[FINRA]].org/01F0224B8
TheExecutingBrokerisresponsiblefor
providingthecorrectURLforthesecurity
identifiedintheconfirm.
TheTradeSuiteIDservicewillnotverifythe
existenceorvalidityofURL.
512-543 32 Character
X(32) Special
Instructions
Line19
O N AdditionalSpecialInstructionfree-formtext.
Usefree-formtexttoincludeinformationabout
thefrontoftheconfirm,asnodefinedfields
exist.Thisinformationincludescontactnames,
taxIDs,phonenumbers,10b-10information,fin-
ancing/REPOtransactionadditionalinform-
ation,orconfirmbackeritems.544-575 32 Character
X(32) Special
Instructions
Line20
O N
576-607 32 Character
X(32) Special
Instructions
Line21
O N
608-807 200 Character
X(200)
Filler - - Reserved.Donotuse.
Table2.3Record2:AdditionalFixedIncomeInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 39

---

## Page 40

Record3:AdditionalPartyInput
Table2.4showstheadditionalpartyinformationforinputmessages.
Position Length Format Field
Name
M
O
C
Validate FieldDescription
Positions1–26:TransactionHeader
1 1 CharacterX
(1)
Feedback
Indicator
O N Indicatesthereturnofthisrecordbecause
oferrors.Forafulldescriptionofthis
processing,seetheInterfaceControl
Manager.
l .*=Ifnoerrors.
l ?=Iftherecordcontainserrors.
2 1 CharacterX
(1)
Production/Test
Indicator
M Y Indicateswhethertherecordisfor
productionortest.Required.
l P=Production
l T=Test
3–8 6 CharacterX
(6)
RecordType M Y Typeofdatacontainedinthemessage.
l TRADEI=TradeInput
9–10 2 Numeric9
(2)
RecordSuffix M Y Identifiesthephysicalrecordnumber.
l 03=AdditionalPartyInput
11–12 2 Numeric9
(2)
VersionNumber M Y Versionnumberthatdefinestherecord
format.
l VersionNumberalways=01
13–18 6 CharacterX
(6)
RecordSequence
Number
O N Uniquetransactionidentifieroftheuser
(optional).Returnedonlyduringerror
reporting.
19–26 8 CharacterX
(8)
Filler – – Reserved.Donotuse.
Positions27–807:TransactionalData
27 1 CharacterX
(1)
Filler – – Reserved.Donotuse.
Table2.4Record3:AdditionalPartyInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 40

---

## Page 41

Position Length Format Field
Name
M
O
C
Validate FieldDescription
28–43 16 CharacterX
(16)
Clearing
[[Broker]]/Dealer
InternalA/C
Number1
O N Internalaccountnumberoftheclearing
[[Broker]]/dealer.Left-justified,space-filled.
44–59 16 CharacterX
(16)
ClearingAgent
InternalA/C
Number1
O N Internalaccountnumberoftheclearing
agent.Left-justified,space-filled.
60–75 16 CharacterX
(16)
InstitutionInternal
A/CNumber1
O N Codeornumbertheinvestmentmanager
usestoidentifyitscustomeraccount.Left-
justified,space-filled.
76–91 16 CharacterX
(16)
InstitutionOrder
RoutingReference
No1
O N Numberprovidedtothebroker/dealerby
aninvestmentmanagerthatenablesan
investmentmanagertotrackorders.Left-
justified,space-filled.
92–99 8 Numeric9
(8)
AdditionalParty #1
[[ID]] Number
O Y IDnumberfortheadditionalpartynumber
1orbroker/dealersub-custodian.
Right-justified,zero-filledwhenno
additionalpartynumber1orbroker/dealer
sub-custodian.Thebroker/dealersub-
custodianisoptional.
100–111 12 CharacterX
(12)
AdditionalParty #1
Account Number
O N Additionalpartynumber1orbroker/dealer
sub-custodianaccountnumber.
112–136 12 CharacterX
(12)
AdditionalParty #1
InstructionLine 1
O N Line1oftexttoappearontheTradeSuite
IDconfirmationassociatedwiththe
additionalpartynumber1orbroker/dealer
sub-custodian.Thisfieldisusuallyforthe
beneficialnameoftheaccount.
137–161 25 CharacterX
(25)
AdditionalParty #1
InstructionLine 2
O N Line2oftexttoappearontheTradeSuite
IDconfirmationassociatedwiththe
additionalpartynumber1orbroker/dealer
sub-custodian.Thisfieldisusuallyforthe
beneficialnameoftheaccount.
Table2.4Record3:AdditionalPartyInput
1Somefieldsfromrecord3alsoappearinrecord5.Thisduplicationeliminatestheneedforaclienttosubmitboth
records3and5whenreferencingonlythesefields.Ifsubmittingbothrecords3and5,record5takesprecedence.
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 41

---

## Page 42

Position Length Format Field
Name
M
O
C
Validate FieldDescription
162–169 8 Numeric9
(8)
AdditionalParty #2
[[ID]] Number
O Y IDnumberfortheadditionalpartynumber
2oragentsub-custodian.Zero-filledwhen
noadditionalpartynumber2oragentsub-
custodian.Theagentsub-custodianis
optional.Right-justified,zero-filled.
170–181 12 CharacterX
(12)
AdditionalParty #2
Account Number
O N Additionalpartynumber2oragentsub-
custodianaccountnumber.
182–206 25 CharacterX
(25)
AdditionalParty #2
InstructionLine 1
O N Line1oftexttoappearontheTradeSuite
IDconfirmationassociatedwiththe
additionalpartynumber2oragentsub-
custodian.Thisfieldisusuallyforthe
beneficialnameoftheaccount.
207–231 25 CharacterX
(25)
AdditionalParty #2
InstructionLine 2
O N Line2oftexttoappearontheTradeSuite
IDconfirmationassociatedwithadditional
partynumber2oragentsub-custodian.
Thisfieldisusuallyforthebeneficialname
oftheaccount.
232–239 8 Numeric9
(8)
AdditionalParty #3
[[ID]] Number
O Y Eight-digitIDnumberoftheadditional
party.Populateonlywithanadditional
party.Zero-filledwhenthereisno
additionalpartynumber3.Right-justified,
zero-filled.
240–251 12 CharacterX
(12)
AdditionalParty #3
Account Number
O N Accountnumberoftheadditionalparty
number3.
252–276 25 CharacterX
(25)
AdditionalParty #3
InstructionLine 1
O N Line1oftexttoappearontheTradeSuite
IDconfirmationassociatedwiththe
additionalpartynumber3.
277–301 25 CharacterX
(25)
AdditionalParty #3
InstructionLine 2
O N Line2oftexttoappearontheTradeSuite
IDconfirmationassociatedwiththe
additionalpartynumber3.
302–309 8 Numeric9
(8)
AdditionalParty #4
[[ID]] Number
O Y Eight-digitadditionalpartyIDnumber.
Populateonlywithanadditionalparty.
Invalidfordomestictradessincetheycan
containonlythreeadditionalparties.Zero-
filledwhenthereisnoadditionalparty
number4.Right-justified,zero-filled.
Table2.4Record3:AdditionalPartyInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 42

---

## Page 43

Position Length Format Field
Name
M
O
C
Validate FieldDescription
310–321 12 CharacterX
(12)
AdditionalParty #4
Account Number
O N Accountnumberatadditionalparty
number4.
322–346 25 CharacterX
(25)
AdditionalParty #4
InstructionLine 1
O N Line1oftexttoappearontheTradeSuite
IDconfirmationassociatedwithadditional
partynumber4.
347–371 25 CharacterX
(25)
AdditionalParty #4
InstructionLine 2
O N Line2oftexttoappearontheTradeSuite
IDconfirmationassociatedwithadditional
partynumber4.
372–379 8 CharacterX
(8)
AdditionalParty #5
[[ID]] Number
O Y Eight-digitadditionalpartyIDnumber.
Populateonlywithanadditionalparty.
Invalidfordomestictradesbecausethey
cancontainonlythreeadditionalparties.
Zero-filledwhenthereisnoadditional
partynumber5.Right-justified,zero-filled.
380–391 12 CharacterX
(12)
AdditionalParty #5
Account Number
O N Accountnumberatadditionalparty
number5.
392–416 25 CharacterX
(25)
AdditionalParty #5
InstructionLine 1
O N Line1oftexttoappearontheTradeSuite
IDconfirmationassociatedwiththe
additionalpartynumber5.
417–441 25 CharacterX
(25)
AdditionalParty #5
InstructionLine 2
O N Line2oftexttoappearontheTradeSuite
IDconfirmationassociatedwiththe
additionalpartynumber5.
442–449 8 Numeric9
(8)
Customer
[[ID]] Number
O Y IDnumberforthecustomer.
450–807 358 CharacterX
(358)
Filler – – Reserved.Donotuse.
Table2.4Record3:AdditionalPartyInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 43

---

## Page 44

Record4:Mortgage-BackedSecuritiesInput
Table2.5showsthemortgage-backedsecurityinformationforinputmessages.
Position Length Format FieldName M
O
C
Validate FieldDescription
Positions1–26:TransactionHeader
1 1 CharacterX(1) FeedbackIndicator O N Indicatesthereturnofthis
recordbecauseoferrors.
Forafulldescriptionofthis
processing,seethe
InterfaceControl
Manager.
l .*=Ifnoerrors.
l ?=Iftherecordcon-
tainserrors.
2 1 CharacterX(1) Production/TestIndicator M Y Indicateswhetherthe
recordisforproductionor
test.Required.
l P=Production
l T=Test
3–8 6 CharacterX(6) RecordType M Y Typeofdatacontainedin
themessage.
l TRADEI=Trade
Input
9–10 2 Numeric9(2) RecordSuffix M Y Identifiesthephysical
recordnumber.
l 04=Mortgage-
BackedSecurities
Input
11–12 2 Numeric9(2) VersionNumber M Y Versionnumberthat
definestherecordformat.
l VersionNumber
always=01
13–18 6 CharacterX(6) RecordSequenceNumberO N Uniquetransaction
identifieroftheuser
(optional).Returnedonly
duringerrorreporting.
Table2.5Record4:Mortgage-BackedSecuritiesInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 44

---

## Page 45

Position Length Format FieldName M
O
C
Validate FieldDescription
19–26 8 CharacterX(8) Filler – – Reserved.Donotuse.
Positions27–807:TransactionalData
27 1 CharacterX(1) Filler – – Reserved.Donotuse.
28–29 2 CharacterX(2) TradeTypeIndicator M Y Typeofmortgage-backed
securitytransactionbeing
confirmed.Mandatoryfor
allmortgage-backed
securitytrades.
00=Ignoremortgage-
backedsecurityrecord
01=GenericTBA
02=SpecifiedTBA
03=SpecifiedPoolTBA
Trade
11=SpecifiedPoolTrade
12=GenericPoolTrade
50=Othermortgage-
backedsecuritytrade
Withthe00tradetype,the
TradeSuiteIDservice
ignoresrecord4andthe
currentnonmortgage-
backedsecuritytrade
processingapplies.With
the02,03,and11trade
types,provideatleastone
fieldspecificationcode
andfieldspecification
value.Ensurethe
ExpandedSecurityType
field(record1,position
194–196)isoneofthe
mortgage-backedsecurity
types:[[ABS]],CMO,FMR,
FNM,FNR,FRM,GMR,
GNM,MBS,orOMB.Ifthe
valueisinvalid,the
TradeSuiteIDservice
rejectstherecord.
Table2.5Record4:Mortgage-BackedSecuritiesInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 45

---

## Page 46

Position Length Format FieldName M
O
C
Validate FieldDescription
30–46 17 Numeric9(12)V9
(5)
CurrentFace O Y Currentunpaidor
remainingprincipalofa
mortgage-backed
security,whichchanges
eachmonthbytheamount
ofthepay-downorpay-up
associatedwiththe
underlyingmortgages
supportingthemortgage-
backedsecurity.Right-
justified,zero-filled.
47–54 8 CharacterX(8) FactorEffectiveDate O Y Effectivedateofthefactor
used,inYYYYMMDD
format.Ifused,entera
validdayoftheyear,
inclusiveofSaturday,
Sunday,andholidays.If
notsupplied,theprogram
setsthefieldtospaces.
55–61 7 CharacterX(7) PoolNumber C Y Agency-assignednumber
referencingthepoolof
mortgagesthat
collateralizeamortgage-
backedsecurity.
Ifsupplied,entereithera
poolnumberorsecurity
numberforSpecifiedPool
orGenericPooltrades.If
notsupplied,DTCCsets
thisfieldtospaces.Pool
numberisinvalidfor
genericTBAs.
Table2.5Record4:Mortgage-BackedSecuritiesInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 46

---

## Page 47

Position Length Format FieldName M
O
C
Validate FieldDescription
62–72 11 CharacterX(11) Yield O Y Annualpercentagereturn,
ascomputedin
accordancewithstandard
industrypractices;thatis,
earnedonasecurity.
Ifsupplied,thisfieldcan
containafloatingdecimal
inanypositionandall
otherpositionsare
numeric.Ifthereisno
embeddeddecimal,the
TradeSuiteIDservice
assumesawholenumber.
Thisfieldcontainsspaces
whentheyieldis
unavailableornot
applicable.
73–88 16 CharacterX(16) RelatedReference
Number
O N Internalbroker/dealer
referencenumberfora
TBA-relatedpool
confirmation.Left-justified,
space-filled.
89–91 3 Numeric(3) NumberofDaysAccrued
Interest
O Y Totalnumberofdaysto
calculatetheinterest.
Right-justified,zero-filled.
92–99 8 CharacterX(8) IssueDate O Y Mortgage-backedsecurity
issueororigindate,in
YYYYMMDDformat.
Ifsupplied,enteravalid
dayoftheyear,inclusive
ofSaturday,Sunday,and
holidays.Ifnotsupplied,
DTCCsetstospaces.
Table2.5Record4:Mortgage-BackedSecuritiesInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 47

---

## Page 48

Position Length Format FieldName M
O
C
Validate FieldDescription
100–108 9 CharacterX(9) SecurityClassCode O N Mortgage-backedsecurity
clearingcorporation
(MBSCC)security
identifier.TheMBSCC
makesthecomponents
available.Indicates
agency,productcode,
coupon,andmaturity.
109 1 CharacterX(1) Filler – – Reserved.Donotuse.
110–120 11 Numeric9(9)V9(2) OriginalTradePar O Y Parvalueoftheoriginal
trade.Right-justified,zero-
filled.
121–124 4 Numeric9(4) GoodDeliveryMillions O Y Numberofmilliondollar
lotsdeliveredin
accordancewithPSA
guidelines.Right-justified,
zero-filled.
125–132 8 CharacterX(8) DeliveryDate O Y Scheduleddeliverydateof
thesecuritiestothecontra
party,inYYYYMMDD
format.
Ifsupplied,enteravalid
dayoftheyear,inclusive
ofSaturday,Sunday,and
holidays.Ifnotsupplied,
DTCCsetsthisfieldto
spaces.
133–138 6 CharacterX(6) EPNTime O Y Time,inHH:MM:SS
format,theelectronicpool
notification(EPN)
messenger(EPNgood
deliverytimestamp)
receivesthemessage.If
supplied,enterthetimein
militaryformat.Ifnot
supplied,DTCCsetsthis
fieldtospaces.
Table2.5Record4:Mortgage-BackedSecuritiesInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 48

---

## Page 49

Position Length Format FieldName M
O
C
Validate FieldDescription
139–144 6 CharacterX(6) LotID O N Lotnumberandpool
sequencewithinthelot,
indicatingapoolorgroup
ofpoolsconsistingof
one/manygooddelivery
millions.
145–148 4 Numeric9(4) Terminator O Y Valueofthegooddelivery
millionsofthepreceding
lotofpools.Right-justified,
zero-filled.
149–159 11 CharacterX(11) MessageID O N UniquemessageID
assignedbyEPNtothe
originalmessage.
160 1 CharacterX(1) PossibleDuplicate O Y EPNindicatestotheuser
thataninputmessagecan
beaduplicate.
l X=Duplicate
l Space=Non-Duplic-
ate
161–170 10 CharacterX10) TradeNumber O N Numberreferencingthe
MBSCCtradenumber.
171–174 4 Numeric9(4) NumberofPools O Y Numberofpools
containedwithintheEPN
message.Right-justified,
zero-filled.
175–190 16 CharacterX(16) InternalID O N Uniquereferencenumber
assignedbythesubmitter.
191–194 4 CharacterX(4) Submitter Account IDO N AccountIDoftheaccount
submittingthemessage.
Table2.5Record4:Mortgage-BackedSecuritiesInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 49

---

## Page 50

Position Length Format FieldName M
O
C
Validate FieldDescription
195–198 4 CharacterX(4) ServiceType O N Typeofmessageinputto
theMBSCCindicating
currentlysupportedtrade
types.
l TFTD=Trade-for-
trade
l SBOD=Useforall
tradesinclasseseli-
giblefornetting
whennettingis
desired
l CMPT=Com-
parisontrade
l CMPC=Com-
parisontradecan-
cellation
l OPTN=[[Option]]
trades
199–202 4 CharacterX(4) OptionType O N Currentlysupported
optiontypes.
l CALL
l PUTS
203–210 8 CharacterX(8) OptionExpirationDate O Y Datewhentheoptionisto
expire,inYYYYMMDD
format.
Ifsupplied,enteravalid
dayoftheyear,inclusive
ofSaturday,Sunday,and
holidays.Ifnotsupplied,
DTCCsetsthisfieldto
spaces.
Table2.5Record4:Mortgage-BackedSecuritiesInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 50

---

## Page 51

Position Length Format FieldName M
O
C
Validate FieldDescription
211–218 8 CharacterX(8) RecordDate O Y Date,inYYYYMMDD
format,setbythetrustee
todeterminewhentopay
theprincipalandinterest
onasecurity.
Ifsupplied,enteravalid
dayoftheyear,inclusive
ofSaturday,Sunday,and
holidays.Ifnotsupplied,
DTCCsetsthisfieldto
spaces.
219–221 3 CharacterX(3) Specification #1Code * O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
222–236 15 CharacterX(15) Specification #1Value O Y Textforspecificationcode
#1.
237–239 3 CharacterX(3) Specification #2 Code *O Y Coderepresentinga
conditiontothetrade.
Termsorconditions
agreedtowhenthetrade
executes(variance
percent,poolsize,number
ofpools).Right-justified,
zero-filled.
240–254 15 CharacterX(15) Specification #2Value O Y Textforspecificationcode
#2.
255–257 3 CharacterX(3) Specification #3 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
258–272 15 CharacterX(15) Specification #3Value O Y Textforspecificationcode
#3.
273–275 3 CharacterX(3) Specification #4 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
Table2.5Record4:Mortgage-BackedSecuritiesInput
*InvalidifTradeTypeindicator=01(GenericTBA)or12(GenericPoolTrades).Requiresatleastone
specificationcodewhenTradeType=11(SpecifiedPoolTrades),02(SpecifiedTBAs),or03(SpecifiedPoolTBA
Trades).
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 51

---

## Page 52

Position Length Format FieldName M
O
C
Validate FieldDescription
276–290 15 CharacterX(15) Specification #4Value O Y Textforspecificationcode
#4.
291–293 3 CharacterX(3) Specification #5 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
294–308 15 CharacterX(15) Specification #5 ValueO Y Textforspecificationcode
#5.
309–311 3 CharacterX(3) Specification #6Code* O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
312–326 15 CharacterX(15) Specification #6Value O Y Textforspecificationcode
#6.
327–329 3 CharacterX(3) Specification #7 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
330–344 15 CharacterX(15) Specification #7Value O Y Textforspecificationcode
#7.
345–347 3 CharacterX(3) Specification #8 Code * O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
348–362 15 CharacterX(15) Specification #8Value O Y Textforspecificationcode
#8.
363–365 3 CharacterX(3) Specification #9 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
366–380 15 CharacterX(15) Specification #9Value O Y Textforspecificationcode
#9.
381–383 3 CharacterX(3) Specification #10 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
Table2.5Record4:Mortgage-BackedSecuritiesInput
*InvalidifTradeTypeindicator=01(GenericTBA)or12(GenericPoolTrades).Requiresatleastone
specificationcodewhenTradeType=11(SpecifiedPoolTrades),02(SpecifiedTBAs),or03(SpecifiedPoolTBA
Trades).
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 52

---

## Page 53

Position Length Format FieldName M
O
C
Validate FieldDescription
384-398 15 CharacterX(15) Specification #10Value O Y Textforspecificationcode
#10.
399–401 3 CharacterX(3) Specification #11 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
402–416 15 CharacterX(15) Specification#11Value O Y Textforspecificationcode
#11.
417–419 3 CharacterX(3) Specification #12 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
420–434 15 CharacterX(15) Specification #12Value O Y Textforspecificationcode
#12.
435–437 3 CharacterX(3) Specification #13 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
438–452 15 CharacterX(15) Specification #13Value O Y Textforspecificationcode
#13.
453–455 3 CharacterX(3) Specification #14 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
456–470 15 CharacterX(15) Specification #14Value O Y Textforspecificationcode
#14.
471–473 3 CharacterX(3) Specification #15 Code *O Y Coderepresentinga
conditiontothetrade.
Right-justified,zero-filled.
474–488 15 CharacterX(15) Specification #15Value O Y Textforspecificationcode
#15.
489–491 3 CharacterX(3) Specification#16 Code * O Y Coderepresentingacon-
ditiontothetrade.Right-
justified,zero-filled.
492–506 15 CharacterX(15) Specification #16Value O Y Textforspecificationcode
#16.
Table2.5Record4:Mortgage-BackedSecuritiesInput
*InvalidifTradeTypeindicator=01(GenericTBA)or12(GenericPoolTrades).Requiresatleastonespe-
cificationcodewhenTradeType=11(SpecifiedPoolTrades),02(SpecifiedTBAs),or03(SpecifiedPoolTBA
Trades).
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 53

---

## Page 54

Position Length Format FieldName M
O
C
Validate FieldDescription
507–514 8 Numeric9(3)V9(5) MBSInterestRate O N Mortgage-backedsecurity
interestrate.
515–522 8 CharacterX(8) MBSMaturityDate O N Mortgage-backedsecurity
maturitydate,in
YYYYMMDDformat.
523–807 285 CharacterX(285) Filler – – Reserved.Donotuse.
Table2.5Record4:Mortgage-BackedSecuritiesInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 54

---

## Page 55

Record5:SupplementalInput
Table2.6showsthesupplementalinformationforinputmessages.
Position Length Format FieldName M
O
C
Validate FieldDescription
Positions1–26:TransactionHeader
1 1 CharacterX(1) FeedbackIndicator O N Indicatesthereturnofthis
recordbecauseoferrors.
Forafulldescriptionofthis
processing,seethe
InterfaceControlManager.
l .*=Ifnoerrors.
l ?=Iftherecordcon-
tainserrors.
2 1 CharacterX(1) Production/TestIndicatorM Y Indicateswhetherthe
recordisforproductionor
test.Required.
l P=Production
l T=Test
3–8 6 CharacterX(6) RecordType M Y Typeofdatacontainedin
themessage.
l TRADEI=Trade
Input
9–10 2 Numeric9(2) RecordSuffix M Y Identifiesthephysical
recordnumber.
l 05=Supplemental
InformationInput
11–12 2 Numeric9(2) VersionNumber M Y Versionnumberthat
definestherecordformat.
l VersionNumber
always=01
13–18 6 CharacterX(6) RecordSequence
Number
O N Uniquetransaction
identifieroftheuser
(optional).Returnedonly
duringerrorreporting.
19–26 8 CharacterX(8) Filler – – Reserved.Donotuse.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 55

---

## Page 56

Position Length Format FieldName M
O
C
Validate FieldDescription
Positions27–807:TransactionalData
27 1 CharacterX(1) Filler – – Reserved.Donotuse.
28–43 16 CharacterX(16) Clearing [[Broker]]/Dealer
InternalA/CNumber *
O N Internalaccountnumberof
theclearingbrokerdealer.
Left-justified,space-filled.
44–59 16 CharacterX(16) Clearing AgentInternal 
A/C Number *
O N Internalaccountnumberof
theclearingagent.Left-
justified,space-filled.
60–75 16 CharacterX(16) InstitutionInternal A/C 
Number *
O N Codeornumberthe
institutionusestoidentify
theaccountofthe
customer.Left-justified,
space-filled.
76–91 16 CharacterX(16) InstitutionOrderRouting
ReferenceNumber *
O N Numberprovidedtothe
[[Broker]]/dealerbyan
institutionthatenablesthe
institutiontotrackorders.
Left-justified,space-filled.
92–115 24 CharacterX(24) Filler – – Reserved.Donotuse.
Table2.6Record5:SupplementalInput
*Somefieldsfromrecord3alsoappearinrecord5.Thisduplicationeliminatestheneedforaclienttosubmitboth
records3and5whentheclientisreferencingonlythesefields.Ifaclientsubmitsbothrecords3and5,record5
takesprecedence.
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 56

---

## Page 57

Position Length Format FieldName M
O
C
Validate FieldDescription
116–117 2 CharacterX(2) ConfirmPurpose O Y Providesthecustomerwith
thereasonforissuingthe
confirm.Ifsupplied,entera
validvalue.
00=Notspecified
01=Original
02=Substitution
03=Marginreprice/cash
call
04=[[Margin]]
reprice/collateralcall
05=Rollover
99=Other
Spaces=Notsupplied.
Ifsupplied,enteravalid
value.theTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
118–119 2 CharacterX(2) DeliveryMethod M Y Determinesthedelivery
methodbasedonsecurity
typeorpurposeoftrade.
01=Free
02=Bookentry
03=Physical
04=DVP/RVP
05=Cash
06=Hold-in-[[custody]]
07=Tri-party
08=Quadparty
99=Other
Mandatoryforthe
expandedsecuritytypes
FINorCOL.Supplyavalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidorno
values.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 57

---

## Page 58

Position Length Format FieldName M
O
C
Validate FieldDescription
120–121 2 CharacterX(2) PriceType O Y Pricetypethatisassociated
withthePricefieldinrecord
1,position99–109.
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
19=PrimaryExchange
99=Other
Spaces=Notsupplied.
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 58

---

## Page 59

Position Length Format FieldName M
O
C
Validate FieldDescription
122 1 CharacterX(1) BlockTradeIndicator O Y Indicatesthattheconfirm
representsablocklevel
trade.
l B=Block
l Space=Notablock
Ifsupplied,enteravalid
value.theTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
123–134 12 CharacterX(12) Give-UpBroker/DealerO N Identifierofthegive-up
[[Broker]]/dealer.Indicatesthe
feeduetoabroker/dealer
thatarrangedthe
transaction(associatedwith
[[Broker]]/dealer).
135–142 8 CharacterX(8) [[Broker]]/DealerSalesmanO N Salespersonnumber.
143–148 6 CharacterX(6) TradeExecutionTime O Y Timeofdaythe
[[Broker]]/dealerbookedthe
trade,inHH:MM:SSformat.
Spaces=Notsupplied.
Ifsupplied,enteravalid
time.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
149–151 3 CharacterX(3) TradeExecutionTime
Zone
O N l EST
l GMT
l PST
l CST
l MST
l OTH=Other
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 59

---

## Page 60

Position Length Format FieldName M
O
C
Validate FieldDescription
152 1 CharacterX(1) SIPCMember O Y Denoteswhetherthe
[[Broker]]/dealerisaSIPC
[[Member]].(10b-10field)
l Y=Yes
l N=No
l Spaces=Notsup-
plied.
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
153 1 CharacterX(1) FINRAMember O Y Denoteswhetherthe
[[Broker]]/dealerisamember
ofFINRA(10b–10field).
l Y=Yes
l N=No
l Spaces=Notsup-
plied.
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
154 1 CharacterX(1) NYSEMember O Y Denoteswhetherthe
[[Broker]]/dealerisaNYSE
[[Member]](10b–10field).
l Y=Yes
l N=No
l Spaces=Notsup-
plied.
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 60

---

## Page 61

Position Length Format FieldName M
O
C
Validate FieldDescription
155 1 CharacterX(1) MarketMaker O Y Denoteswhetherthe
[[Broker]]/dealerisamarket
makerinthesecurity(10b–
10field).
l Y=Yes
l N=No
l Spaces=Notsup-
plied.
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
156–187 32 CharacterX(32) DeliveryInstructionsLine
1
O N Whereinvestmentmanager
orfunddeliversorreceives
securitiesfrom(Re:
Physicaldeliveries—canbe
aphysicalstreetlocation).
Free-formtext.
188–219 32 CharacterX(32) DeliveryInstructionsLine
2
O N Whereinvestmentmanager
orfunddeliversorreceives
securitiesfrom,for
example,thephysical
deliveries.Free-formtext.
220–251 32 CharacterX(32) WireInstructions O N Ifneededforthetri-partyor
ifaphysicalsecurity
deliveryisnecessary.
MinimallyneedtheABA
number.Free-formtext.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 61

---

## Page 62

Position Length Format FieldName M
O
C
Validate FieldDescription
252–283 32 CharacterX(32) SpecialInstructions
Line 9
O N Useformtexttoinclude
informationaboutthefront
oftheconfirmandno
definedfieldsexist.This
informationincludes
contactnames,taxIDs,
phonenumbers,10b–10
information,
financing/REPOtransaction
additionalinformation,or
confirmbackeritems.
284–315 32 CharacterX(32) SpecialInstructions
Line 10
O N
316–347 32 CharacterX(32) SpecialInstructions
Line 11
O N
348–379 32 CharacterX(32) SpecialInstructions
Line 12
O N
380–411 32 CharacterX(32) SpecialInstructions
Line 13
O N
412–443 32 CharacterX(32) SpecialInstructions
Line 14
O N
444–475 32 CharacterX(32) SpecialInstructions
Line 15
O N
476–507 32 CharacterX(32) SpecialInstructions
Line 16
O N
508–539 32 CharacterX(32) SpecialInstructions
Line 17
O N
540–571 32 CharacterX(32) SpecialInstructions
Line 18
O N
572–606 35 CharacterX(35) AgentInternalAccount
Number
O N Agent'sinternalaccount
number(AIA).Usethisfield
inplaceoftheAgent
InternalAccountNumberin
record1,position323.This
fieldallowsforsupportof
theagentinternalaccount
numberbeyond12
charactersandupto35
characters.Ifnotprovided,
settospaces.Free-form
text.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 62

---

## Page 63

Position Length Format FieldName M
O
C
Validate FieldDescription
607–615 9 Numeric9(7)V99 CommissionEquivalentO Y Reportanynon-monetary
benefitamounts
disclosedascommission
equivalentthesameas
theamountsandvalueof
commissionpaidina
correspondingsale.Often
usedtoexecuteriskless
principaltrades.
Untilallexecutingbrokers
haveprogrammedtothis
newspecification,this
fieldischeckedfornon-
numericdata.Ifthefield
containsnon-numeric
data,thecharacters
providedarereplaced
withzeros.Valid
CommissionEquivalent
valuescontainonly
numberswithanimplied
decimalpoint.
616–623 8 CharacterX(8) TradeExecutionDate O Y ValidationofTrade
ExecutionDate.
l Datethatthebroker-
/dealerbookedthe
trademustbein
CCYYMMDDformat.
l Ifsupplied,mustbea
validcalendardate
(spaces=notsup-
plied).The
TradeSuiteIDser-
vicegeneratesa
tradeerrorforinvalid
values.
l Spaces=Notsup-
plied.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 63

---

## Page 64

Position Length Format FieldName M
O
C
Validate FieldDescription
624 1 CharacterX(1) MarkUp/MarkDownPer-
centageSign
O Y AssociatedwiththeMark-
UporMark-Down
Percentagefield.This
fieldcanbe:
l +=Positive
l -=Negative
l Space=notsupplied
625-632 8 Numeric9(3)V9(5) MarkUp/MarkDown
Percentage
O Y Fieldinformationforthe
[[Broker]]/dealertodisclose
anypercentageofthe
MarkUp/MarkDown
differencebetweenthe
reportedpriceandthe
pricetothecustomer
involvedinthe
transaction.Displayedas
apercentage.
Ifthevalueisnot
numeric,theTradeSuite
IDservicegeneratesa
tradeerror.
Right-justifiedandzero-
filled.
633-638 6 CharacterX(6) Filler O Y Reserved.Donotuse.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 64

---

## Page 65

Position Length Format FieldName M
O
C
Validate FieldDescription
639–654 16 CharacterX(16) UserDefinedDisclosure
Code
O Y User-definedcodeusedin
theconfirmbacker/
disclosureenrichment.Itis
datasuppliedbythe
[[Broker]]/dealerthatalso
residesonthe
backer/disclosure
repositoryasenrichment
criteria.Thisfieldresideson
therepositoryforthe
[[Broker]]/dealertodefine
enrichmentcriteriafor
confirmdisclosures.
Entertheexactmatch
conformingwiththeallowed
valuesenteredinthe
disclosurerepositoryallows
only0–9andA–Zvaluesin
upperorlowercase.Ifthe
backer/disclosure
repositorydoesnothavea
correspondingvalueasthe
definedcriteria,the
TradeSuiteIDservice
generatesatradeerroras
longastheuser-defined
codeisprovidedandthe
[[Broker]]/dealersubscribesto
thedisclosureenrichment.
Freeformtext.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 65

---

## Page 66

Position Length Format FieldName M
O
C
Validate FieldDescription
655 1 CharacterX(1) ConfirmDisclosure
BypassIndicator
O Y Fieldforbroker/dealerto
instruct,theTradeSuiteID
servicetobypassor
overridetheindicatorforthe
confirmdisclosure
enrichmentforatrade.
l B=BypassConfirm
DisclosureEnrich-
ment
l Space=EnrichCon-
firmDisclosure(if
subscribed)
[[Broker]]/dealerbypass
enrichmentfortheconfirm
disclosuresforatrade.The
TradeSuiteIDservice
generatesatradeerrorfor
invalidvalues.
Note:Whenusingthe
bypassIndicator,the
[[Broker]]/dealermust
distributethe
backer/disclosure
informationtocounter-
partiesbysomeother
means.
656 1 CharacterX(1) MarkUp/MarkDown
PercentageSign
O Y AssociatedwiththeMark-
UporMark-Downfield.
Indicateswhetherthemark-
upormark-downisless
thanorgreaterthan.
l +=Positive
l -=Negative
l Space=notsupplied
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 66

---

## Page 67

Position Length Format FieldName M
O
C
Validate FieldDescription
657–667 11 CharacterX(11) MarkUp/MarkDown O Y [[Broker]]/dealerdisclosesany
mark-up,mark-down,or
differencebetweenthe
reportedpriceandtheprice
tothecustomerinvolvedin
thetransaction(10b–10
field).
Cancontainafloating
decimalinanyposition.All
otherpositionsarenumeric.
Wholenumbersdonot
requireadecimalpoint.If
notsupplied,settospaces.
TheTradeSuiteIDservice
generatesatradeerror
whenthevalueisnot
numeric.Right-justified,
zero-filled.
668 1 CharacterX(1) 3rdPartyRemuneration
Received
O Y Fieldforbroker/dealerto
denotewhetherthe
[[Broker]]/dealerreceivedany
third-partyremunerationin
thetransaction(10b–10
field).
l Y=Yes
l N=No
l Space=notsup-
plied.
TheTradeSuiteIDservice
generatesatradeerrorfor
invalidvalues.
669–688 20 CharacterX(20) [[Broker]]/DealerTelephone
Number
O N Fieldinformationforthe
[[Broker]]/dealertodisclose
thetelephonenumberused
forcontactingpurposes.
Freeformtext.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 67

---

## Page 68

Position Length Format FieldName M
O
C
Validate FieldDescription
689-708 20 CharacterX(20) [[Broker]]/DealerLegal
EntityIdentifier
O N Auniquealphanumeric
brokeridentifier
(ISO17442).
709-728 20 CharacterX(20) InstitutionLegalEntity
Identifier
O N Auniquealphanumericinsti-
tutionidentifier(ISO17442).
729–741 13 CharacterX(13) Filler – – Reserved.Donotuse.
742–807 66 CharacterX(66) Reserved – – Reservedforinternaluse
forCTM/USDI.
Table2.6Record5:SupplementalInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 68

---

## Page 69

Record6:Financing/REPOTransactionInput
Table2.7showsthefinancing/REPOtransactioninformationforinputmessages.
Position Length Format FieldName M
O
C
Validate FieldDescription
Positions1–26:TransactionHeader
1 1 CharacterX(1) FeedbackIndicator O N Indicatesthereturnofthis
recordbecauseoferrors.For
afulldescriptionofthis
processing,seetheInterface
ControlManager.
l .*=Ifnoerrors.
l ?=Iftherecordcon-
tainserrors.
2 1 CharacterX(1) Production/Test
Indicator
M Y Indicateswhethertherecord
isforproductionortest.
Required.
l P=Production
l T=Test
3–8 6 CharacterX(6) RecordType M Y Typeofdatacontainedinthe
message.
l TRADEI=TradeInput
9–10 2 Numeric9(2) RecordSuffix M Y Identifiesthephysicalrecord
number.
l 06=Financing/REPO
Input
11–12 2 Numeric9(2) VersionNumber M Y Versionnumberthatdefines
therecordformat.
l VersionNumber
always=01
13–18 6 CharacterX(6) RecordSequence
Number
O N Uniquetransactionidentifier
oftheuser(optional).
Returnedonlyduringerror
reporting.
19–26 8 CharacterX(8) Filler – – Reserved.Donotuse.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 69

---

## Page 70

Position Length Format FieldName M
O
C
Validate FieldDescription
Positions27–807:TransactionalData
27 1 CharacterX(1) Filler – – Reserved.Donotuse.
28–29 2 CharacterX(2) TradeType M Y Identifiesthetradetype.
01=REPO
02=ReverseREPO
03=Sell/buyback
04=Buy/sellback
05=Participation
06=Securitylending
07=Securityborrowing
99=Other
Whenselectingtheexpanded
securitytypesFINorCOL,
useRecord6.Selectthe
tradetype,andsupplyavalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidornovalues.
30–31 2 CharacterX(2) LegIdentifier M Y Identifieswhethertheconfirm
isafirstlegconfirm,second
legconfirm,orboth.
l LO=Onleg
l LC=Offleg
l LB=Bothlegs
FortheFINexpanded
securitytype,thisfieldis
mandatory.FortheCOL
expandedsecuritytype,this
fieldisoptional.Supplya
validvalue.TheTradeSuite
IDservicegeneratesatrade
errorforinvalidornovalues.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 70

---

## Page 71

Position Length Format FieldName M
O
C
Validate FieldDescription
32–33 2 CharacterX(2) CollateralType M Y Identifiesthetypeofcollateral
involvedinthetransaction.
Forsecuritylending,canuse
specialinstructionsfieldto
specifyothercollateraltypes
notsuppliedhere.
01=Treasuries
02=Governmentagencies
03=[[Asset]]-backedsecurities
04=CMO
05=Mortgage-backed
[[securities]]
06=Equities
07=Moneymarkets
08=Corporatebonds
09=Municipalbonds
10=Wholeloans
11=Generalcollateral
12=Letterofcredit
13=Privatelabels
14=Cash
15=Sovereignbonds
16=Indexfunds
17=Exchangetradedfunds
99=Other
FortheFINexpanded
securitytype,thisfieldis
mandatory.Supplyavalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
34–73 40 CharacterX(40) Tri-PartyAgent O N Nameofthetri-partyagent.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 71

---

## Page 72

Position Length Format FieldName M
O
C
Validate FieldDescription
74–81 8 CharacterX(8) StartDate O Y DatethattheREPOstarted
accruinginterest,in
YYYYMMDDformat.Itis
equivalenttosettlementdate
ofthefirstleg.
Spaces=Notsupplied.If
supplied,enteravaliddateof
theyear,includingweekends
andholidays.TheTradeSuite
IDservicegeneratesatrade
errorforinvalidvalues.
82–89 8 CharacterX(8) EndDate/MaturityDate O Y ClosedateoftheREPOor
reverseREPOintereststops
accruing,inYYYYMMDD
format.
Iftheenddateisunknown,
createanopenREPOusing
allspaces.Ifclosinganopen
REPO,usetheactualend
date.
Spaces=Notsupplied.If
supplied,enteravaliddateof
theyear,includingweekends
andholidays.TheTradeSuite
IDservicegeneratesatrade
errorforinvalidvalues.
90–92 3 Numeric9(3) Numberofpiecesof
[[collateral]]
O Y Itemcountforthenumberof
collateralpieces.Ifthevalue
isnotnumeric,the
TradeSuiteIDservice
generatesatradeerror.
Right-justified,zero-filled.
93–108 16 CharacterX(16) ParentReference
Number
O N Cross-referencesaparent
tradewithallassociatedchild
orcollateraltrades.
Referencenumbercanbe
retainedonrollovers,
substitutions.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 72

---

## Page 73

Position Length Format FieldName M
O
C
Validate FieldDescription
109–124 16 CharacterX(16) Additional Reference
Number 1
O N Canpotentiallyusetolink
buysandsellsforsell/buy
backandbuy/sellbacktrades
orforanyotherreference
numbers.
125–140 16 CharacterX(16) Additional Reference
Number 2
O N
141 1 CharacterX(1) FINRateSign O Y Denoteswhethertheinterest
rateispositiveornegative.
l +=Positive
l -=Negative
l Space=blank,notsup-
plied
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
142–149 8 Numeric9(2)V9(6) FINRate O Y Numericvalueoftheinterest
rateatwhichthetransaction
accrues.Ifthevalueisnot
numeric,theTradeSuiteID
servicegeneratesatrade
error.Right-justified,zero-
filled.
150 1 CharacterX(1) FINRateType O Y Specifieswhetherthetradeis
afixedorvariablerate.
l F=Fixed
l V=Variable
l Space=blank,notsup-
plied
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
151–164 14 Numeric9(12)V99SecurityLendingFee O Y Ifthevalueisnotnumeric,the
TradeSuiteIDservice
generatesatradeerror.
Right-justified,zero-filled.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 73

---

## Page 74

Position Length Format FieldName M
O
C
Validate FieldDescription
165–166 2 CharacterX(2) AccrualMethod O Y Calculationtypeusedto
arriveatthetotalinterest
paymentonthetrade.
00=Notspecified
01=30/360
02=30/365
03=30/actual
04=Actual/360
05=Actual/365
06=Actual/actual
07=Actual/365L
99=Other
Spaces=Notsupplied
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
167 1 CharacterX(1) InterestDaysSign O Y DenoteswhethertheInterest
Daysfieldispositiveor
negative.
l +=Positive
l -=Negative
l Space=blank
l Spaces=Notsupplied
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 74

---

## Page 75

Position Length Format FieldName M
O
C
Validate FieldDescription
168–171 4 Numeric9(4) InterestDays O Y Numericvalueoftheinterest
accrualdays.Ifthevalueis
notnumeric,theTradeSuite
IDservicegeneratesatrade
error.Right-justified,zero-
filled.
172 1 CharacterX(1) AccruedInterestdueat
MaturitySign
O Y DenoteswhethertheAccrued
InterestdueatMaturityfieldis
positiveornegative.
l +=Positive
l -=Negative
l Space=blank
l Spaces=Notsupplied
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
173–186 14 Numeric9(12)V99AccruedInterestdueat
Maturity
O Y Numericcalculatedvalue
derivedfromtheREPOrate
andthenumberofinterest
days.Ifthevalueisnot
numeric,theTradeSuiteID
servicegeneratesatrade
error.Right-justified,zero-
filled.
187–188 2 CharacterX(2) Index(Benchmark) O Y Benchmarkrateofinterest
accrual,associatedwithor
consideredafloatingrate
REPO.
l Spaces=Notsupplied
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.Fora
fulllisting,seeInput/Output
Information.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 75

---

## Page 76

Position Length Format FieldName M
O
C
Validate FieldDescription
189 1 CharacterX(1) SpreadtoBenchmark
Sign
O Y DenoteswhethertheSpread
toBenchmarkfieldispositive
ornegative.
l +=Positive
l -=Negative
l Space=blank
l Spaces=Notsupplied
Ifsupplied,enteravalid
value.theTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
190–192 3 Numeric9(3) SpreadtoBenchmark
orIndex(forFloating
Rate)
O Y Numericvaluebasispoints
awayfromthebenchmarkor
index,usedtodeterminethe
rate.Ifthevalueisnot
numeric,theTradeSuiteID
servicegeneratesatrade
error.Right-justified,zero-
filled.
193–200 8 Numeric9(3)V9(5) [[Haircut]]% O Y Margincollateralassociated
withREPOtypetransactions
toaccountforthemarketor
interestpaymentsonthe
underlyingsecurities,
displayedasapercentage.If
thevalueisnotnumeric,the
TradeSuiteIDservice
generatesatradeerror.
Right-justified,zero-filled.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 76

---

## Page 77

Position Length Format FieldName M
O
C
Validate FieldDescription
201 1 CharacterX(1) SubstitutionType O Y Typeofcollateralsubstitution.
l
P=Parvalueofthe
securitytimesthe
pricedeterminesthe
transactionprincipal
amount.
l
M=Moneyfilled.
Principalamount
assignedtothe
[[collateral]].
l
Space=Blank.
Valuenotsupplied.
Ifsupplied,enteravalid
value.TheTradeSuiteID
servicegeneratesatrade
errorforinvalidvalues.
202–203 2 CharacterX(2) SubstitutionNumber O N Numberoftimesthatthe
collateralcanbesubstituted
overthelifeoftheREPO.To
specifyunlimited,usespace
orU.
204–211 8 Numeric9(3)V9(5) SubstitutionVariance O Y Numericpercentagebywhich
theprincipalvalueofthe
replacementcollateraldiffers
fromtheprincipalofthe
original.Parfillsonly.Ifthe
valueisnotnumeric,the
TradeSuiteIDservice
generatesatradeerror.
Right-justified,zero-filled.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 77

---

## Page 78

Position Length Format FieldName M
O
C
Validate FieldDescription
212–213 2 CharacterX(2) SubstitutionFrequencyO N Periodoverwhichthe
specifiednumberof
substitutionscantakeplace.
Number1–9inthefirst
characterpositionfollowedby
oneofthefollowingletters:
l H=Half
l Q=Quarter
l M=Month
l W=Week
Forexample:
l 1Q=onceaquarter
l 2W=twiceaweek
214 1 CharacterX(1) Face(Par)orCashFill
REPO
O Y BasisfortheREPO
collateralization.Ifface,face
timespriceequalscollateral
value.
l F=Face(Par)
l C=CashFill
l Space=blank.Ifsup-
plied,enteravalid
value.
l Spaces=Notsupplied
TheTradeSuiteIDservice
generatesatradeerrorfor
invalidvalues.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 78

---

## Page 79

Position Length Format FieldName M
O
C
Validate FieldDescription
215–228 14 Numeric9(12)V99REPOValue O Y Numericmarketvalue
roundedusingthe
appropriatemarketpractice
conventionforthatparticular
instrumentintheREPO
market.Marketvalueofthe
securitywithhaircut
considered.Ifthevalueisnot
numeric,theTradeSuiteID
servicegeneratesatrade.
Right-justified,zero-filled.
229–242 14 Numeric9(12)V99PremiumAmount O Y Differenceinmoneybetween
theopenandcloselegsofa
REPOtransaction.Ifthe
valueisnotnumeric,the
TradeSuiteIDservice
generatesatradeerror.
Right-justified,zero-filled.
243–244 2 CharacterX(2) InterestPayment
CalendarFrequency
O N Paymentinterval,suchas3
monthsor6monthsfor
interestcleanupschedule.
Number1–9inthefirst
characterpositionfollowedby
oneofthefollowingletters:
l H=Half
l Q=Quarter
l M=Month
l W=Week
Forexample:
l 1Q(onceaquarter)
l 2W(twiceaweek)
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 79

---

## Page 80

Position Length Format FieldName M
O
C
Validate FieldDescription
245–252 8 CharacterX(8) 1stInterestCleanup
Date
O Y Firstdateonwhichtobase
thescheduleofinterest
cleanuppayments,in
YYYYMMDDformat.
Spaces=Notsupplied.If
supplied,enteravaliddateof
theyear,includingweekends
andholidays.TheTradeSuite
IDservicegeneratesatrade
errorforinvalidvalues.
253–255 3 Numeric9(3) LookbackDays(for
floatingrate)
O Y Numberofbusinessdays
beforethefloatingratereset
datewhenthebenchmark
priceiscapturedandusedto
determinethenewrateupon
reset.Ifthevalueisnot
numeric,theTradeSuiteID
servicegeneratesatrade
error.Right-justified,zero-
filled.
256–257 2 CharacterX(2) ResetInterval
Frequency(forfloating
rates)
O N Resetinterval,suchas3
monthsor6months.Number
1–9inthefirstcharacter
positionfollowedbyoneof
thefollowingletters:
l H=Half
l Q=Quarter
l M=Month
l W=Week
Forexample:
l 1Q(onceaquarter)
l 2W(twiceaweek)
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 80

---

## Page 81

Position Length Format FieldName M
O
C
Validate FieldDescription
258–265 8 CharacterX(8) 1stRateResetDate O Y Firstdateonwhichtobase
thescheduleofratereset
dates,inYYYYMMDDformat.
Ifsupplied,enteravaliddate
oftheyear,including
weekendsandholidays.The
TradeSuiteIDservice
generatesatradeerrorfor
invalidvalues.Spaces=Not
supplied.
266–267 2 CharacterX(2) FlexREPOPayback
Frequency
O N Singlematurity;however,itis
possibletoreturnthecashof
themoneygiver,usuallybya
predeterminedpaydown
schedule.Number1–9inthe
firstcharacterposition
followedbyoneofthe
followingletters:
l H=Half
l Q=Quarter
l M=Month
l W=Week
Forexample:
l 1Q(onceaquarter)
l 2W(twiceaweek)
268–275 8 CharacterX(8) 1stFlexRepayment
Date
O Y Firstdateonwhichtobase
scheduleofflexrepayments,
inYYYYMMDDformat.If
supplied,enteravaliddateof
theyear,includingweekends
andholidays.TheTradeSuite
IDservicegeneratesatrade
errorforinvalidvalues.
Spaces=Notsupplied.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 81

---

## Page 82

Position Length Format FieldName M
O
C
Validate FieldDescription
276–278 3 Numeric9(3) CallDelay O Y Minimumnumberofdays
noticeacounter-partyneeds
forterminatingthe
transaction.Ifthevalueisnot
numeric,theTradeSuiteID
servicegeneratesatrade
error.Right-justified,zero-
filled.
279–807 529 CharacterX(529) Filler – – Reserved.Donotuse.
Table2.7Record6:Financing/REPOTransactionInput
ConfirmTradeInputMessageSpecification
2.InputRecordFormats 82

---

## Page 83

A.FOURTHQUARTER2005
MODIFICATIONS
UnderSecuritiesandExchangeCommission([[SEC]])RegulationSHOrule203andSection31btransaction
fees,themachine-readablespecificationscontainthefollowingchanges:
l AdditionofPrimeBrokerLong/Shortindicatoronposition66
l AllinstancesofSECFeechangedtoFee
Fails/[[Locate]](RegulationSHO–Rule203)
Themachine-readableconfirmrecordlayoutaddedthePrimeBrokerLong/Shortindicatorinboththeinput
andoutputspecifications.Aone-characterfillerareaonposition66ofboththeinputandoutputrecord
layoutaccommodatesthisfield.Anewerrormessageappearswhenthefieldisunpopulatedcorrectly.
Section31FeeConfirmationLabel
TheSECmandatedchangestothelanguageusedtolabelfeesonconfirmations.Feereplacesall
instancesofSECFee.
ConfirmTradeInputMessageSpecification
A.FourthQuarter2005Modifications 83

---

## Page 84

B.JUNE1998MODIFICATIONS
InJuneof1998,thesecuritytranslationprocessoftheTradeSuiteIDservicewasmodified.Thisprocess
enablescross-referenceinternationalsecurityidentifiersforbothmembersoftheTradeSuiteIDservice
andoverseasclientsthatusesecurityidentifiersotherthanCUSIPorCINSintheirtrademessages.
TheTradeSuiteIDclientrepresentativesatDTCCneedthefollowingdataelementstosetupsecurity
identificationpreferencesforindividualclients:
l TradeSuiteIDusernumber
l Usertype(role)
l Settlementlocation
l SecurityIDpreference
ImplementingsecurityidentifiersubstitutionintheTradeSuiteIDserviceensuresthattheinitialtranslation
ofthetradeinputtimeisconsistentforthelifeoftheconfirm/affirmprocess.Translationprocessingoccurs
onlyonceforallpartiesofthetradeattradeinput.AllchangesandupdatesintheSecurityTranslation
databaseapplyonlytonewtrades.NoimpactoccursfortradesalreadyrecordedontheTradetable.
TheTradeSuiteIDtradeinputfiledoesnothaveanyrequiredchanges.Continuetoidentifythesecurity
numberingsystemandsecurityidentifierusedfortheoriginaltrade.Theprimarypartiestoaneligibletrade
thatsettleatDTC—thatis,clearingagentandclearingbroker—mustalwayshaveaCUSIPorCINSin
messagessenttothem.
Ifthedatabasefailstoprovideacorrespondingsecurityidentifier,theTradeSuiteIDservicedefaultstothe
securityidentifiersubmittedbytheoriginatorofthetradeinputrecord.Consequencesofthisactionare
thatatradeeligiblefortheDepositoryTrustCompany([[DTC]])automatedsettlementbecomesineligible,
andtheTradeSuiteIDclientmustsubmitaseparateDeliverOrder.
Forthesecuritynumberingsystemcodes,TableB.1showsthefournewvaluesandonemodifiedvalue.
FieldName Position Format FieldContents Comments
Record1SecurityNumberingSys-
tem
204–205 CharacterX(2) CE=CEDEL(Clearstream)
ES=Spain
LU=Luxembourg
SE=Sweden
XS=CommonCode(CEDEL/Euroclear)
New
New
Modified
New
New
TableB.11998SecurityNumberingSystemCodeAdditions
ConfirmTradeInputMessageSpecification
B.June1998Modifications 84

---

## Page 85

Previously,CEDEL(Clearstream)andLuxembourgshareda7-digitsecuritynumberingsystemcode(LU).
Now,Luxembourgexclusivelyusesthis7-digitcode,andCEDEL(CE)usesanew6-digitcode.Notethe
changeonbothtradeinputandtradeoutput,sincethenewsecuritynumbertranslationprocessvalidates
thesecuritynumberingsystemcodeagainstthelengthofthesecurityidentifierstring.
ConfirmTradeInputMessageSpecification
B.June1998Modifications 85

---

## Page 86

©2023DTCC.Allrightsreserved.DTCCandDTCC(Stylized)areregisteredandunregisteredtrademarksofThe
DepositoryTrust&ClearingCorporation.Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandname
bycertainaffiliatesofTheDepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitselfdoesnotprovidesuch
services.Eachoftheseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsoftheparticularcountry
orcountriesinwhichsuchentityoperates.Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,itsaffiliatesand
theservicestheyoffer.
DocDate:October17,2023
PublicationCode:TS256
Service:TradeSuiteID
Title:ConfirmTradeInputMessageSpecification
ForMoreInformation
EmailDTCCLearningat:
DTCCLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com