---
title: "SWIFT MT541/543 Message Specification"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sim026_swift_notif_ui_20240201.pdf"
pages: 55
size: "435.8 KB"
category: "SIM"
ingested_on: "2026-06-05"
---

# SWIFT MT541/543 Message Specification

**Original File:** [sim026_swift_notif_ui_20240201.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sim026_swift_notif_ui_20240201.pdf)  
**Category:** SIM  
**Total Pages:** 55  
**File Size:** 435.8 KB  

---

## Page 1

SettlementInstructionManager
SWIFTMT541/543MESSAGESPECIFICATION
FEBRUARY01,2024

---

## Page 2

TABLEOFCONTENTS
Preface 3
Audience 3
ChangesinthisVersionoftheDocument 3
RelatedDocumentsandTraining 3
Questions? 3
1.SWIFTMT541/543Message 4
Introduction 4
SWIFTMT541/543MessageLayout 4
CrossCurrencyTrade 52
DEAG/REAGMapping 52
Handlingofnon-SWIFTcharactersintextfields 54
SupportofCTMOrganizationswithoutValidRegisteredSWIFTBIC 54
SWIFTMT541/543MessageSpecification
TableOfContents 2

---

## Page 3

PREFACE
ThisdocumentprovidesdetailedinformationontheformatoftheSWIFTMT541/543messagesgeneratedbythe
ITPSettlementInstructionManagerservicefororganizationssubscribedtothePostTradeSettlementNotification
serviceandoptionallysubscribedtothePostTradeSettlementNotification–PreMAGRservice.
Audience
Readthismanualifyourbusinessrequirementsincludethefollowing:
l InvestmentmanagerswhouseCTMandwishtosendSWIFTMT541/543messagesatMatchAgreed(MAGR),
CancelMatchAgreed,andPreMatchAgreed(NMAG)totheirsettlingagent,otherparties,and/ortheirown
organization
l BrokerswhouseCTMandwishtosendSWIFTMT541/543messagesatMatchAgreed(MAGR)andCancel
MatchAgreedtotheirsettlingagent,otherparties,and/ortheirownorganization
l [[Custodians]],banks,thirdparties,andexecutingbrokerswhoreceiveSWIFT MT541/543messagesfromtheir
investmentmanagerclientviaCTM
Note
DTCCofferssettlementservicesonlyfortheInstructingPartyorExecutingBrokerontradecomponents.
ChangesinthisVersionoftheDocument
Thisversionofthedocumentincludeschangesbasedonthe2023FunctionalRelease4.
RelatedDocumentsandTraining
Forrelateddocumentsandtraining,seeSettlementInstructionManagerontheDTCCLearningCenter.
Questions?
TheClientCenterprovidesgeneralassistanceandtechnicalhelp.Visitto:
l Enteraservicerequestorcheckthestatusofanexistingservicerequest.
l Searchtheknowledgebase.
l Obtaincontactinformation.
SWIFTMT541/543MessageSpecification
Preface 3

---

## Page 4

1.SWIFTMT541/543MESSAGE
Introduction
ThischapterdescribestheSWIFTMT541/543messagelayout.TheITPSettlementInstructionManagerservice
supportsthesendingofSWIFTMT541/543messages
l ForinvestmentmanagersthisoptionallyincludestheOmnibusBlockSettlementtrades,oncetheallocation
hasreachedMatchAgreed(MAGRandCancelMatchAgreed(CMAG)inCTM.
l UponausertakinganactiontoRelease,AmendorCancelwithintheITPSettlementInstructionManagerUI.
l ForinvestmentmanagersthisoptionallyincludesPreMatchAgreed(NMAG)iftheuserinitiatesthatworkflow
fromCTM.
SWIFTMT541/543MessageLayout
Table1describesthecontentsoftheMT541/543columnheadersintheSWIFTMT541/543Specification:
Thedarkshadedrowsindicatethefollowing:
l SequencesintheMT541/543.
l Whenincludinganarrow(→),correspondingsub-sequencesintheMT541/543.
ThelightershadedrowsdemarcateStartandEndofBlocktags.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 4

---

## Page 5

ColumnHeader Description
SWIFTTag/Qualifier&
Line#
Theinformationinthiscolumncontainsthefollowing:
l SWIFTTag/Qualifier—Ifapplicable,thefieldcorrespondstothesametagandqualifierinaSWIFT
MT541/543.
l LineNo.—ForreferencingSWIFTtaglocationsinaSWIFTmessage.
SWIFTFieldName/
Format/Example
Theinformationinthiscolumncontainsthefollowing,whencorrespondingSWIFTelementsexist:
l SWIFTFieldName—Ifapplicable,thefieldcorrespondstothesamefieldnameinaSWIFTMT541/543.
l SWIFTCodes—Ifapplicable,identifiesallstaticSWIFTcodevaluesCTMsupports:
l CommasseparatethecodesandSWIFTallowsonecodeperfield
l Asuperscriptnumbersuchas1(orseparatesectioninthecaseof5)indicatesthatthe
correspondingtablefootnotecontainsanextensivelistofsupportedcodevalues.
Example—AnexamplefieldvalueasitappearsinthemessagerowofaSWIFTfile.
SWIFTCodes
---
M-O-C
Theinformationinthiscolumnindicatesthefollowing:
l SWIFTCodes—SupportedcodesthatapplytostandardSWIFTtags.
l Mandatory,Optional,andConditionalelementswithincompositesconformtoSWIFTmandatoryand
optionalfields.Forexample,theCurrencycompositecontainstheoptionalSignelementandthemandatory
CurrencyCodeandAmountelements.
AG/TD TheinformationinthiscolumnindicatesthesourcethatCTMusestoderivedatafortheSWIFTmessage:
l AG—AutomaticallygeneratedfromCTMduringthetradecycleandsettlementprocess.Examplesare
theCTMTradeDetailIDandCTMTradeSideIdvalues.
l TD—TradeDetailthatyouoryourcounterpartysubmittedaccordingtotherulesdescribedforthefieldin
.
Table1 SWIFTMT541/543Specification—ColumnHeaderKey
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 5

---

## Page 6

ColumnHeader Description
CTMSource
---
SettlementInstruction
ManagerUIMapping
Theinformationinthiscolumnindicatesthefollowing:
l CTMSource—ThenameoftheelementintheTradeDetailthatCTMusestoderiveormapdataforthe
settlementdetail.Iftheelementisnotuniqueinthemessage,theXPathisincluded.Forexample,
PartyValueisanelementintheInstructingPartyandExecutingBrokercomposites.Whenusedfor
mapping,thePartyValueXPathis:
l InstructingParty/PartyValue
l ExecutingBroker/PartyValue
l SettlementInstructionManagerUIMapping—ThecorrespondingfieldnameintheSettlement
InstructionManagerUI,accessedthroughtheITP portal.
Note NotesincludewhetherCTMmapstheinstructingpartyorexecutingbrokervalue,sourcingrules,andother
validationsthatCTMapplies.
Table1 SWIFTMT541/543Specification—ColumnHeaderKey
ThefollowingtableprovidestheSWIFTMT541/543specification.Italsocontainsonlyfieldsapplicableto
settlementaccordingtoSWIFTrequirements.
SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
BasicHeaderBlock(Block1)
HDR Name:BlockIdentifier
Format:String
Example:1
{
1
:F01OMGOUS33ADNM0000
000000}
NA
---
M
AG NA
---
NA
Valueisalways1.
HDR Name:ApplicationIdentifier
Format:String
Example:F
{1:
F
01OMGOUS30ADNM00000
00000}
NA
---
M
AG NA
---
NA
ValueisalwaysFtoindicatea
FinancialApplication(FIN)message.
Table2 SWIFTMT541/543Specification
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 6

---

## Page 7

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
HDR Name:ServiceIdentifier
Format:String
Example:01
{1:F
01OMGOUS30ADNM00000
00000}
NA
---
M
AG NA
---
NA
Valueisalways01toindicateaFIN
user-to-usermessageservice.
HDR Name:LT(LogicalTerminal)
Identifier
Format:String
Example:
OMGOUS33ADNM
{1:F01
OMGOUS33ADNM00000
00000}
NA
---
M
AG NA
---
NA
ValueisalwaystheDTCCBIC(8
char),LogicalTerminalCode(1char)
andbranchcode(3char).Startingin
2021,theSettlementInstruction
ManagerUIintheITP Portaluses
OMGOUS33ADNMastheLogical
TerminalIdentifier.
HDR Name:SessionNumber
Format:4!n
Example:0000
{1:F01OMGOUS30ADNM
0000
000000}
NA
---
M
AG NA
---
NA
Valueisalways0000toindicateFIN
sessionnumber.
HDR Name:SequenceNumber
Format:6!n(String)
Example:000000
{1:OMGOUS30ADNM0000
000000}
NA
---
M
AG NA
---
NA
Valueisalways000000toindicate
Inputsessionsequencenumber.
ApplicationHeaderBlock(Block2)
HDR Name:BlockIdentifier
Format:String
Example:2
{2:I541BANKUS33AXXXN}
{4
NA
---
M
AG NA
---
NA
Valueisalways2.
HDR Name:Input/OutputIdentifier
Format:String
Example:I
{2:I541BANKUS33AXXXN}
{4
NA
---
M
AG NA
---
NA
ValueisalwaysI(Input)toSWIFT.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 7

---

## Page 8

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
HDR Name:MessageType
Format:3!n
Example:541
{2:I541BANKUS33AXXXN}
{4
NA
---
M
TD BuySellIndicator
---
Buy/Sell
MessageTypeismappedasfollows:
l IfBuy/Sell=SELL,Message
Type=543
l IfBuy/Sell=BUYI,Message
Type=541
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 8

---

## Page 9

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
HDR Name:Receiver’sAddress
Format:12x
Example:
BANKUS33AXXXN
{2:I541
BANKUS33AXXXNN}{4:
NA
---
M
TD ReceiverAgentBIC,
CustodianBIC,or
SubAgentBIC
---
UIdoesnotdisplaythesource
fields.ItdisplaysthePrimary
Receiver’sAddress(akaSettling
Agent).FieldnameisSettlingAgent
BIC.
l Forprimaryreceiver(settling
agent):
l IfReceiverAgentBICis
presentandvalid,itis
usedasReceiver’s
Address.
l IfReceiverAgentBICis
notpresentorifitis
invalid,CustodianBICis
usedasReceiver’s
Address–ifitispresent
andvalid.
l IfCustodianBICisnot
presentorifitisinvalid,
SubAgentBICisusedas
Receiver’sAddress–ifit
ispresentandvalid.
Notethatthereceiverobtainedfrom
abovelogicgetsoriginalSWIFT(23G
taghasNEWMorCANCasvalue).
l Fornon-PrimaryReceiver(third
party,interestedparty):
l Thereceiver’saddress
(BICvalue)isobtained
fromtheorg’seventpro-
fileand/ordestinationpro-
file.
l Thereceiverobtained
fromtheeventprofilegets
acopyofSWIFT(23Gtag
hasNEWM/COPYor
CANC/COPYasvalue).
NotethatLogicalTerminalCodeAis
insertedinthe9thpositionofReceiver
BIC.Forexample,ifReceiverBICis
BANKUS30XXX,thevaluethatgets
mappedtoSWIFTis
BANKUS30AXXX.Itappliestoboth
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 9

---

## Page 10

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
PrimaryReceiverandnon-Primary
Receiver.
HDR Name:MessagePriority
Format:1x(String)
Example:N}
{2:I541BANKUS33AXXXNN}
{4:
NA
---
M
AG NA ValueisalwaysN(Normal).
TextBlock(Block4)
HDR Name:TextBlock
Format:String
Example:4:
{2:I541BANKUS33N}{4:
NA
---
M
AG NA Valueisalways4foraFINmessage.
MandatorySequenceAGeneralInformation
16R
LineNo.
1
StartofBlock/OptionR—16c
Example::16R:GENL
20C
SEME
LineNo.
2
Name:Sender’sMessage
Reference
Format::4!c//16x(Qualifier)
(Reference)
Example:
:20C::SEME//123456
NA
---
M
AG
or
TD
FunctionOfTheMessageor
CTMTradeDetailID
---
CTMAllocationID
Mappingrulesasfollows:
l WhenFunctionOfTheMessage
isNEWM,CTMTradeDetailIDis
mappedtoSender’sMessage
Reference.
l WhenFunctionOfTheMessage
isCANC,anauto-generated
valueismappedtoSender’s
MessageReference
Whenacanceledallocation(manual
fromtheSettlementInstruction
ManagerUI)getsamendedfromUI,an
auto-generatedvalueismappedto
20CSEMEintheresultingnew
SWIFT.Inthesamemessage,the20C
PREVtaggetsmappedwithSender’s
MessageReferenceoforiginal
message.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 10

---

## Page 11

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
23G
LineNo.
3
Name:Functionofthe
Message
Format:4!c[/4!c](Function)
[Subfunction]|
Examples:
:23G:NEWM
:23G:NEWM/COPY
:23G:CANC
:23G:CANC/COPY
NEWM
CANC
---
M
TD FunctionOfTheMessage
---
NA
The4-charvalueof
FunctionOfTheMessageismappedto
theFunction:
l NEWM—Directsthecustodian
toprocessthesettlementinstruc-
tion.
l CANC—Directsthecustodianto
cancelaprevioussettlement
instruction.
NotethatCOPYisusedasthe
Subfunctioninmessagescreatedfor
non-Primaryrecipients,suchas
interestedparties.
98C
PREP
LineNo.
4
Name:Preparation
Date/Time
Format::4!c//8!n6!n
(Qualifier)(Date)(Time)
Example:
:98C::PREP//202104050930
15
NA
---
AG NA
---
NA
SWIFTcreationDateTime(UTC)is
mappedtopreparationDate/Time.
DateandTimeisbasedon
CoordinatedUniversalTimeZone
(UTC).
99B
TOSE
Name:TotalofLinked
SettlementInstructions
Format:
:4!c//3!n(Qualifier)(Number)
Example:
:99B::TOSE//002
NA
---
O
AG TotalSettlementInstructionNumber
---
NA
OnlymappedforOmnibusinstructions
withAllocationTypeofOMNIorDEPD.
ItisaCTMgenerated3-digitvalue,
representingthenumberofdependent
allocationsassociatedtoanOmni
allocation.Themaximumnumberof
dependentscanbe999.
99B
SETT
Name:CurrentSettlement
InstructionNumber
Format:
:4!c//3!n(Qualifier)(Number)
Example:
:99B::SETT//001
NA
---
O
AG CurrentSettlementInstructionNumb
er
---
NA
OnlymappedforOmnibusinstructions
withAllocationTypeofOMNIorDEPD.
ItisaCTMgenerated3-digitvalue,
representingthecurrentinstruction
numberoftheOMNIlinkedallocations.
AnOMNIwillalwayshaveavalueof
000.Dependentinstructionswill
alwayshaveavaluefrom001-999
dependingontheircount.
→OptionalRepetitiveSubsequenceA1Linkages
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 11

---

## Page 12

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
16R
LineNo.
6
StartofBlock/OptionR—16c
Example::16R:LINK
20C
PREV
LineNo.
9
Name:PreviousReference
Format::4!c//16x(Qualifier)
(Reference)
Example:
:20C::PREV//123456
NA
---
M/C
AG
or
TD
CTMTradeDetailID
---
CTMAllocationID
Mappingrulesasfollows:
l WhenFunctionOfTheMessage
isCANC,CTMTradeDetailIDis
mappedtoPreviousReference.
l WhenFunctionOfTheMessage
isNEWM,PreviousReferenceis
notcreated
16S
LineNo.
11
EndofBlock/OptionS—16c
Example::16S:LINK
16R
LineNo.
6
StartofBlock/OptionR—16c
Example::16R:LINK
20C
RELA
LineNo.
9
Name:RelatedReference
Format::4!c//16x(Qualifier)
(Reference)
Example::20C::RELA//8933
NA
---
O
TD TDReferenceType=RELA
---
RelatedTransactionRef
TDReferences/TDReferenceValueis
mappedtoRELA (RelatedReference).
NotethatRelatedReferenceisnot
populatedwhen
FunctionOfTheMessageisCANC.
16S
LineNo.
11
EndofBlock/OptionS—16c
Example::16S:LINK
16R
LineNo.
6
StartofBlock/OptionR—16c
Example::16R:LINK
20C
POOL
LineNo.
9
Name:PoolRelated
Reference
Format::4!c//16x(Qualifier)
(Reference)
Example::20C::POOL//8931
NA
---
O
TD TDReferenceType=POOL
---
PoolReference
TDReferences/TDReferenceValueis
mappedtoPOOLRelatedReference.
NotethatPoolRelatedReferenceis
notpopulatedwhen
FunctionOfTheMessageisCANC.
16S
LineNo.
11
EndofBlock/OptionS—16c
Example::16S:LINK
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 12

---

## Page 13

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
16R
LineNo.
6
StartofBlock/OptionR—16c
Example::16R:LINK
20C
TRRF
LineNo.
9
Name:DealReference
Format::4!c//52x(Qualifier)
(UTIReference)
Example:
:20U::TRRF//8931ABC908
NA
---
O
TD AllocationUTI
---
AllocationUTI
AllocationUTIisismappedtoDeal
Reference.NotethatAllocationUTIis
auto-generatedinCTMforinvestment
managersorbrokerssubscribedto
auto-generationusingtheAuto
GenerateTradeUTIssubscription
[[Option]](AUTI=Y).Investment
managersorbrokersthatarenot
subscribedtoAUTIcanprovidethe
AllocationUTIvalueduringtrade
submissiontoCTM.
16S
LineNo.
11
EndofBlock/OptionS—16c
Example::16S:LINK
16S
LineNo.
12
EndofBlock/OptionS—16c
Example::16S:GENL
MandatorySequenceBTradeDetails
16R
LineNo.
13
StartofBlock/OptionR—16c
Example::16R:TRADDET
94a
CLEA
LineNo.
14
Name:PlaceofClearing
FormatOptionH:
:4!c//4!a2!a2!c[3!c
(Qualifier)(IdentifierCode)
ExampleOptionH:
:94H::CLEA//OMGOUS33XX
X
NA
---
O
TD PlaceOfClearing
---
NA
SettlementInstructionManagermaps
avalidBICtoPlaceofClearing,which
representstheplaceofclearingforthe
allocation.Notethefollowing:
l IfBICis11char,itismappedto
thePlaceofClearingtag,asis.
l IfBICis8char,itispaddedwith
XXXandthenmappedtothe
PlaceofClearingtag.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 13

---

## Page 14

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
94b
TRAD
LineNo.
14
Name:PlaceofTrade
FormatOptionB::4!c/[8c]/4!c
[/30x](Qualifier)(Data
SourceScheme)(Place
Code)[Narrative]
ExampleOptionB:
:94B::TRAD//EXCH/XNYS
:94B::TRAD//OTCO/US
:94B::TRAD//VARI/US
EXCH
OTCO
VARI
---
O
TD PlaceOfTrade/PlaceCode
(wherePlaceCode=EXCH,
OTCO,orVARI)and
PlaceOfTrade/PlaceNarrative
---
PlaceofTradeCode,
PlaceofTradeMIC,or
PlaceofTradeNarrative
SettlementInstructionManagermaps
PlaceCodeandPlaceNarrativeintothe
PlaceofTradetag.NotethattheData
SourceSchemeisnotused.
98a
SETT
LineNo.
15
Name:SettlementDate
FormatOptionA::4!c//8!n
(Qualifier)(Date)
ExampleOptionA:
:98A::SETT//20210606
NA
---
M
TD SettlementDate
---
SettlementDate
MappingformatisYYYYMMDD.
98a
TRAD
LineNo.
15
Name:TradeDate/Time
FormatOptionA::4!c//8!n
(Qualifier)(Date)
ExampleOptionA:
:98A::TRAD//20210404
FormatOptionC::4!c//8!n6!
(Qualifier)(Date)(Time)
ExampleOptionC:
:98C::TRAD//202104041103
25
NA
---
M
TD TradeDateTime
---
TradeDate
Mappedasfollows:
l IftheOriginatorofMessageis
subscribedtotheTradeDateto
SWIFT(TTOS)subscription
[[Option]],thendateandtime
(YYYYMMDDHHMMSS)are
mappedtoTradeDateusing
optionC.
l IftheOriginatorofMessageis
notsubscribedtotheTradeDate
toSWIFT(TTOS)subscription
[[Option]],thendateonly
(YYYYMMDD)ismappedto
TradeDateusingoptionA.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 14

---

## Page 15

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
90a
DEAL
LineNo.
16
Name:DealPrice
FormatOptionA:
:4!c//4!c/15d(Qualifier)
(PercentageTypeCode)
(Price)
ExampleOptionA:
:90A::DEAL//PRCT/10,25
FormatOptionB:
:4!c//4!c/3!a15d(Qualifier)
(AmountTypeCode)
(CurrencyCode)(Price)
ExampleOptionB:
:90B::DEAL//ACTU/ARS100,
PRCT
ACTU
---
M
TD SecurityTypeGroup,
DealPrice/Amount,and
DealPrice/CurrencyCode
---
FinancialInstrumentClass,
DealPrice,and
TradeCurrency
Mappedasfollows:
l IfSecurityTypeGroup=DBT,
thenDealPriceisformattedwith
OptionAusingthePRCTcode
(PercentageCode).
l IfSecurityTypeGroup=EQT,
thenDealPriceisformattedwith
OptionBusingtheACTUcode
(ActualAmount).
99A
DAAC
LineNo.
17
Name:NumberofDays
Accrued
Format::4!c//[N]3!n
(Qualifier)(Sign)(Number)
Example::99A::DAAC//009
NA
---
O
TD NumberOfDaysAccrued
---
DaysAccrued
SettlementInstructionManagermaps
thevalueofNumberOfDaysAccrued.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 15

---

## Page 16

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
35B
LineNo.
18
Name:Identificationofthe
FinancialInstrument
Format:[ISIN1!e12!c][4*35x]
IdentificationofSecurity
DescriptionofSecurity
Example:
:35B:ISINUS0378331005
AppleInc
OneAppleParkWay
Cupertino,CA95014
408-996-1010
NA
---
M
TD CountryCode,NumberingAgency
Code,SecurityCode,and
DescriptionOfTheSecurity
---
FinancialInstrumentIDand
FinancialInstrument
Description
Mappedasfollows:
l IfthevalueofNum-
beringAgencyCodeisISIN,then
the12-charactervalueofSecur-
ityCodeismappedtoformatthis
tag.ThestringISIN(uppercase)
isincludedinthetagfollowedby
aspace.Thespaceisthenfol-
lowedby12characterSecur-
ityCode.Ifavailable,upto4
linesofDescriptionofSecurityis
mappedfromDescrip-
tionOfTheSecurityfield.There
shouldbenogapbetweenlines.
l IfthevalueofNum-
beringAgencyCodeisnotISIN,
thenCountryCodeismappedfol-
lowedbySecurityCode.The
CountryCodeisenclosedin
slashes.Example:/US/.Ifavail-
able,theDescrip-
tionOfTheSecurityismappedin
therestofthethreeDescription
ofSecurityfields.Thereshould
benogapbetweenlines.
Note:
IfFinancialInstrumentDescription
textstartswithacolonorhyphenin
anyofthe4lines,itisreplacedwith
space.
→OptionalSubsequenceB1FinancialInstrumentAttributes
Note:CTMonlycreatesOptionalSubsequenceB1blockifSecurityTypeGroup=DBTandthemarketdeterminedbyPSETisnot
Germany.
16R
LineNo.
19
StartofBlock/OptionR—16c
Example::16R:FIA
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 16

---

## Page 17

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
98A
MATU
LineNo.
24
Name:MaturityDate
Format::4!c//8!n
Example:
:98A::MATU//20410410
NA
---
O
TD MaturityDate
---
MaturityDate
MapstheMaturityDate(YYYYMMDD)
totheMaturityDatetag.Fixedincome
(debt)instrumentsonly.
92A
CUFC
LineNo.
25
Name:Rate(CurrentFactor)
FormatOptionA::4!c//[N]15d
(Qualifier)(Sign)(Rate)
ExampleOptionA:
:92A:://CUFC/14,
NA
---
O
TD CurrentFactor/Signand
CurrentFactor/Amount
---
CurrentFactor
MapstheSignandAmount(if
negative)totheCurrentFactortag.
NotethattheNegativesignismapped
asNinSWIFTtag.
92A
INTR
LineNo.
25
Name:CouponRate
Format::4!c//[N]15d
(Qualifier)(Sign)(Rate)
Example::92A::INTR//5,4
NA
---
O
TD CouponRate
---
CouponRate
MapsthevalueofCouponRatetothe
CouponRatetag.Fixedincome(debt)
instrumentsonly.
92A
YMTR
LineNo.
25
Name:YieldtoMaturityRate
Format::4!c//[N]15d
(Qualifier)(Rate)
Example::92A::YTMR//5,3
NA
---
O
TD YieldType(MATR)
---
NA
MapsthevalueofYieldTypetoYieldto
MaturityRate.Fixedincome(debt)
instrumentsonly.
13B
POOL
LineNo.
26
Name:NumberIdentification
(PoolNumber)
FormatOptionB::4!c/
[8c]/30x(Qualifier)(Data
SourceScheme)(Number)
ExampleOptionB:
:13B::POOL//1256
NA
---
O
TD PoolNumber
---
PoolNumber
MapsthevalueofPoolNumberto
NumberIdentification(PoolNumber)
tag.
16S
LineNo.
32
EndofBlock/OptionS—16c
Example::16S:FIA
22F
TTCO
LineNo.
33
Name:Indicator
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example:
:22F::TTCO//BUTC
1
---
O
TD TradeTransactionCondition
Indicator
---
TradeConditions
Eachoccurrenceofthe
TradeTransactionConditionIndicatoris
mappedtothe22FTTCOIndicator
tag.Inotherwords,22FTTCOcan
appearmultipletimesintheSWIFT
message,witheachinstance
containingadifferentindicatorvalue.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 17

---

## Page 18

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
11A
FXIS
FXIB
LineNo.
34
Name:Currency
Format::4!c//3!a(Qualifier)
(CurrencyCode)
Example::11A::FXIS//USD
NA
---
O
TD BuySellIndicatorand
FXDealCurrencyCode
---
Buy/Sell
FXDealCurrency
Mappedasfollows:
l IfBuy/Sell=SELL,FXISqualifier
ismapped.
l IfBuy/Sell=BUYI,FXIBqualifier
ismapped.
NotethattheFXDealCurrencyCodeis
mappedtoinstructtherecipientof
settlementinstructiontoexecuteanFX
deal.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 18

---

## Page 19

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
25D
MTCH
AFFM
LineNo.
35
Name:Status
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(StatusCode)
ExamplesPre-Match
Agreed:
:25D:://AFFM//NAFI
:25D:://MTCH//NMAT
ExamplesMatchAgreed:
:25D::MTCH//MACH
:25D::AFFM//AFFI
MACH
AFFI
---
M,C
AG NA
---
Allocations
Mappedasfollows:
1. ForPre-MatchAgreed,ifthe
investmentmanagerissub-
scribedtotheTargettoSecur-
itiesDepositorysubscription
[[Option]](T2SD=Y))andthePSET
(CentralizedSecuritiesDepos-
itory)oftradeallocationissub-
scribedtotheTargetto
SecuritiesIdentificationsub-
scriptionoption(T2SI=Y),then
theAFFMqualifierandNAFI
codeareusedformapping.
Otherwise,theMTCHqualifier
andNMATcodeareusedfor
mappingaNotMatchAgreed
allocationwithstateMISMor
NMAT.
2. ForMatchAgreed,iftheOri-
ginatorofMessageissubscribed
totheTargettoSecuritiesDepos-
itorysubscriptionoption
(T2SD=Y))andthePSET(Cen-
tralizedSecuritiesDepository)of
tradeallocationissubscribedto
theTargettoSecuritiesIden-
tificationsubscriptionoption
(T2SI=Y),thentheAFFMqual-
ifierandAFFIcodeareusedfor
mapping.
Otherwise,theMTCHqualifier
andMACHcodeareusedfor
mappingaMatchAgreed
allocation.
Notethatthistagismappedonlyfora
newmessage
(FunctionOfTheMessage=NEWM)and
isnotmappedforacancellation
(FunctionOfTheMessage=CANC)and
isnotmappedforAllocationType=
DEPD(OmnibusDependent
Allocations).
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 19

---

## Page 20

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
70E
SPRO
LineNo.
36
Name:SettlementInstruction
ProcessingNarrative
Format::4!c//10*35x
(Qualifier)(Narrative)
Example::70E::SPRO//Cpty
coversregistrationcost
NA
---
O
TD AdditionalText,TDReferenceType
(whereTDReferenceType=XCBT),
andTDReferenceValue
---
SettlementNarrative1,
SettlementNarrative2,
...uptoandincluding...
SettlementNarrative10,and
CptyCashBondTradingRef
Thistagismappedtosupplyadditional
informationtoaninstruction—inthe
exactordersubmittedtoCTMinthe
AdditionalTextfieldthatsupportsmax
of10lines(35chareach).
IfAdditionalTextisnotpresentandthe
counterpartybrokerhasa
TDReferenceTypeofXCBT,thenthe
TDReferenceValueisappendedtothe
proprietarycodeCBT.
Example:IfTDReferenceType=XCBT
andTDReferenceValue=123,thenthis
tagisformattedasfollows:
:70E::SPRO//CBT123.
16S
LineNo.
37
EndofBlock/OptionS16c
Example:16S:TRADDET
RepetitiveMandatorySequenceCFinancialInstrument/Account
16R
LineNo.
38
StartofBlock/OptionR
16c:16R:FIAC
36B
SETT
LineNo.
39
Name:QuantityofFinancial
Instrument
Format::4!c//4!c/15d
(Qualifier)(QuantityType
Code)(Quantity)
Examples:
:36B::SETT//FAMT/123,50
:36B::SETT//UNIT/1000,
FAMT
UNIT
---
M
TD QuantityTypeCodeand
QuantityAllocated
---
QuantityTypeandQuantity
QuantityTypeCodeand
QuantityAllocatedaremappedto
QuantityofFinancialInstrumenttag.
NotethattheQuantityTypeCodecan
eitherbeFAMTorUNIT.
36B
SETT
LineNo.
39
Name:QuantityofFinancial
Instrument
Format::4!c//4!c/15d
(Qualifier)(QuantityType
Code)(Quantity)
Example:
:36B::SETT//AMOR/2000
AMOR
---
O
TD CurrentFaceValue
---
CurrentFaceValue
CurrentFaceValueismappedto
QuantityofFinancialInstrumentif
anotherinstanceoftag36BSETT
containsFAMTasQuantityType
Code.QuantityTypeCodeAMORis
mappedwhentheCurrentFaceValue
ismapped.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 20

---

## Page 21

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
97A
SAFE
LineNo.
43
Name:Account
(SafekeepingAccount)
FormatOptionA::4!c//35x
(Qualifier)(AccountNumber)
ExampleOptionA:
:97A::SAFE//12345
NA
---
M
TD SecurityAccountorID2
---
AccountatSettlingAgent
Sourcedasfollows:
l Ifcounterparty'sPSETisoneof
thefollowingIBRCESMM,
IBRCESMMSCL,
IBRCESMMCDE,
IBRCESMMMVL,or
IBRCESMMXXX,then:
l IfSecurityAccountisavail-
able,thatvalueisusedfor
mappingtoSafekeeping
Accounttag.
l IfSecurityAccountisnot
available,MessageOri-
ginator'sID2isusedformap-
pingtoSafekeeping
Accounttag.
l IfbothSecurityAccountand
ID2arenotavailable,aFatal
errorisgenerated.
l IfCounterparty'sPSETisnotone
ofthefollowingIBRCESMM,
IBRCESMMSCL,
IBRCESMMCDE,
IBRCESMMMVL,or
IBRCESMMXXX,then:
l IfSecurityAccountisavail-
able,thatvalueisusedfor
mappinginSafekeeping
Accounttag.
l IfSecurityAccountisnot
available,aFatalerroris
generated.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 21

---

## Page 22

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
97a
CASH
LineNo.
43
Name:Account(Cash
Account)
FormatOptionA::4!c//35x
(Qualifier)(AccountNumber)
ExampleOptionA:
:97A::CASH//3434
FormatOptionE::4!c//34x
(Qualifier)(International
BankAccountNumber)
ExampleOptionE:
:97E::CASH//IBAN1234567
NA
---
O
TD CashAccountNo
---
CashAccount
Sourcedasfollows:
l Ifthefirsttwocharactersoffield
CashAccountNocontainavalid
countrycode,97Eisusedfor
mapping.
l Ifthefirsttwocharactersoffield
CashAccountNodonotcontain
avalidcountrycode,97Ais
used
ACashAccountNovaluewithfirsttwo
charactersasacountrycodeis
assumedtobeanInternationalBank
AccountNumber.
94a
SAFE
LineNo.
44
Name:Place(Placeof
Safekeeping)
FormatOptionC::4!c//2!a
(Qualifier)(Country)
ExampleOptionC:
:94C::SAFE//US
FormatOptionF:
:4!c//4!c/4!a2!a2c[3!c]
(Qualifier)(Place)(BIC/BEI)
ExampleOptionF:
:94F::SAFE//[[DTCC]]
NA
---
O
TD PlaceOfSafekeepingType,
PlaceofSafekeepingPlace,and
PlaceofSafekeepingValue
---
PSAFEType,PSAFEBIC,
PSAFECountry,and
PSAFEPlace
Sourcedasfollows:
l IfPlaceOfSafe-
keepingType=COUN,then
OptionCisusedtomapthePla-
ceofSafekeepingValue
l IfPlaceOufSafe-
keepingType=BICthenOptionF
isusedtomapthePla-
ceofSafekeepingValuealong
withthePla-
ceofSafekeepingPlacevalueof
CUST,NCSD,ICSD,orSHHE
NotethatonlyvalidBICsaremapped
toPlaceofSafekeepingtag:
l IfBICis11char,itismappedas-
istoPlaceofSafekeepingtag
l IfBICis8char,itispaddedwith
XXXandthenmappedtoPlace
ofSafekeepingtag
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 22

---

## Page 23

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
16S
LineNo.
52
EndofBlock/OptionS—16c:16S:FIAC
RepetitiveMandatorySequenceESettlementDetails
Note:SWIFTrequiresatleastoneinstanceofTag:22FinSequenceE.
16R
LineNo.
62
StartofBlock/OptionR—16c:16R:SETDET
22F
STCO
LineNo.
63
Name:Indicator([[settlement]]
TransactionCondition)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::STCO/CLEN
2
---
O
TD SettlementTransactionConditionInd
icator
---
SettlementConditions
Valueof
SettlementTransactionConditionIndica
torismappedto22FSTCOtag(except
forthevalue‘SINO’thatgetsmapped
to22F::FXCXtag).Notethatthevalue
ineachoccurrenceof
SettlementTransactionConditionIndica
torismappedtothe22FSTCO
Indicatortag.The22FSTCOtagcan
appearmultipletimesinaSWIFT
message—eachtimewithadifferent
indicatorvalue.TheSWIFTtag
:95C::PSETmustuseOptionCifthe
22FSTCOSWIFTcodeisPHYS.
Otherwise,aFatalerrorisgenerated.
22F
SETR
LineNo.
63
Name:Indicator(Typeof
SettlementTransaction)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::SETR/TRAD
3
---
M
TD TypeOfTransactionIndicator
---
TypeofSettlementTransaction
ValueofTypeOfTransactionIndicator
ismappedto22FSETRtag.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 23

---

## Page 24

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
22F
STAM
LineNo.
63
Name:Indicator(Stamp
Duty)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Examples:
:22F::STAM/CRST/GBT3
:22F::STAM/CCAS/FUSD
:22F::STAM/ECLR/IEYX
:22F::STAM/FUSD
:22F::STAM/STRA/USTN
4
---
O
TD SettlementTransactionCondition
Indicator
---
StampDutyExemption
Sourcedasfollows:
l IfthevalueofSet-
tle-
mentTrans-
actionConditionIndicatorisfrom
thelistofvaluesthatmapto
StampDutyIndicator,itis
mappedto22FSTAM.Seethe
codesonthirdcolumnfromthe
leftofthistableforlistofvalues
thatmapto22FSTAM.
l ForcodeUSTN,STRAisused
astheDataSourceScheme.
l Ifcounterparty'sPSET-
T=XHKCHKH1or
XHKCHKH1XXX,CCASisused
astheDataSourceScheme
whencodesareFUSDorHASD.
l Ifcounterparty's
PSET≠XHKCHKH1or
XHKCHKH1XXX,thentheData
SourceSchemeisnotusedfor
codesFUSDandHASD.
l IfcodesstartwithGB(suchas
GBAX,GBBX,andsoon),then
CRSTisusedastheData
SourceScheme.
l IfcodesstartwithIE(suchas
IEYX,IEQX,andsoon),then
ECLRisusedastheData
SourceScheme.
Notethatifthereismorethanone
valuein
SettlementTransactionConditionIndica
torthatcouldbemappedto22F
STAM,onlythefirstvalueismappedto
22FSTAM.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 24

---

## Page 25

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
22F
RTGS
LineNo.
63
Name:Indicator([[securities]]
Real-TimeGrossSettlement)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::RTGS/NRTG
NRTG
YRTG
---
O
TD SettlementTransactionConditionInd
icator
---
Real-TimeGrossSettlement
System
Ifthevalueof
SettlementTransactionConditionIndica
tor=NRTGorYRTG,itismappedto
22FRTGS.NotethatifbothNRTGand
YRTGarepresentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FRTGS.
22F
REGT
LineNo.
63
Name:Indicator
(Registration)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::REGT/NREG
NREG
YREG
---
O
TD SettlementTransactionConditionInd
icator
---
Registration
Ifthevalueof
SettlementTransactionConditionIndica
tor=NREGorYREG,itismappedto
22FREGT.NotethatifbothNREG
andYREGarepresentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FREGT.
22F
BENE
LineNo.
63
Name:Indicator(Beneficial
Ownership)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::BENE/NBEN
NBEN
YBEN
---
O
TD SettlementTransactionCondition
Indicator
---
BeneficialOwnership
Ifthevalueof
SettlementTransactionConditionIndica
tor=NBENorYBEN,itismappedto
22FBENE.NotethatifbothNBENand
YBENarepresentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FBENE.
22F
CASY
LineNo.
63
Name:Indicator(Cash
SettlementSystem)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::CASY/NETS
GROS
NETS
---
O
TD SettlementTransactionConditionInd
icator
---
CashSettlementSystem
Ifthevalueof
SettlementTransactionConditionIndica
tor=GROSorNETS,itismappedto
22FCASY.NotethatifbothGROS
andNETSarepresentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FCASY.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 25

---

## Page 26

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
22F
FXCX
LineNo.
63
Name:Indicator(Foreign
ExchangeCancellation)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Examples:
:22F::FXCX/FXYE
:22F::FXCX/FXNO
:22F::FXCX//SINO
FXYE
FXNO
---
O
TD NA
---
NA
WhentheoriginalMT54xhas11A
populatedinsequenceBandthe
FunctionOfTheMessageisCANCand:
l IfaclientelectstokeepFXin
place(CancelFXFlagisN)in
theSettlementInstruction
ManagerUI,thentheFXNO
indicatorispopulated.
l IfuserviatheSettlement
InstructionManagerUIelects
tocancelFXinplace(Cancel
FXFlagisY),thenFXYE
indicatorispopulated.
Also,iftheMatchAgreedTradeis
canceledviaCTMandtheoriginal
instructioncontained11Ainsequence
B,thentheFXYEindicatoris
populated.
WhenFunctionOfTheMessageis
NEWM,SINOindicatorwillbemapped
tothisfieldprovideditisselectedby
theuserviaSettlementInstruction
ManagerUI.
Inanewmessage(field:23G:NEWM),
:22F::FXCX//SINOindicatesthata
forexstandinginstructionshouldNOT
applyasanoriginalFXorderhasbeen
retained.
QualifierFXCXisNOTrepeatablein
theSWIFTmessage.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 26

---

## Page 27

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
22F
BLOC
LineNo.
63
Name:Indicator(Foreign
ExchangeCancellation)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::BLOC/BLCH
BLCH
BLPA
---
O
TD SettlementTransactionCondition
Indicator
---
BlockTradeIndicator
Ifthevalueof
SettlementTransactionConditionIndica
tor=BLCHorBLPA,itismappedto22F
BLOC.NotethatifbothBLCHand
BLPAarepresentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FBLOC.
22F
REST
LineNo.
63
Name:Indicator
(Restrictions)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::REST/NRST
144A
NRST
RSTR
---
O
TD SettlementTransactionCondition
Indicator
---
Restrictions
Ifthevalueof
SettlementTransactionConditionIndica
tor=144A,NRSTorRSTR,itis
mappedto22FREST.Notethatif
multiplecodes(fromabove)are
presentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FREST.
22F
SETS
LineNo.
63
Name:Indicator([[settlement]]
System/Method)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::SETS/YSET
NSET
YSET
---
O
TD SettlementTransactionCondition
Indicator
---
SettlementSystem/Method
Ifthevalueof
SettlementTransactionConditionIndica
tor=NSETorYSET,itismappedto
22FSETS.NotethatifbothNSETand
YSETarepresentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FSETS.
22F
NETT
LineNo.
63
Name:Indicator(Netting
Eligibility)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::NETT/YNET
NNET
YNET
---
O
TD SettlementTransactionCondition
Indicator
---
NettingEligibility
Ifthevalueof
SettlementTransactionConditionIndica
tor=NNETorYNET,itismappedto
22FNETT.NotethatifbothNNETand
YNETarepresentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FNETT.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 27

---

## Page 28

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
22F
CCPT
LineNo.
63
Name:Indicator(Central
CounterPartyEligibility)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::CCPT/YCCP
NCCP
YCCP
---
O
TD SettlementTransactionCondition
Indicator
---
CentralCounterpartyEligibility
Ifthevalueof
SettlementTransactionConditionIndica
tor=NCCPorYCCP,itismappedto
22FCCPT.NotethatifbothNCCPand
YCCParepresentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FCCPT.
22F
LEOG
LineNo.
63
Name:Indicator(Letterof
Guarantee)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::LEOG/NLEG
NLEG
YLEG
---
O
TD SettlementTransactionCondition
Indicator
---
LetterofGuarantee
Ifthevalueof
SettlementTransactionConditionIndica
tor=NLEGorYLEG,itismappedto
22FLEOG.NotethatifbothNLEGand
YLEGarepresentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FLEOG.
22F
COLE
LineNo.
63
Name:Indicator([[collateral]]
Pool)
Format::4!c/[8c]/4!c
(Qualifier)(DataSource
Scheme)(Indicator)
Example::22F::COLE/COLA
COLA
COLN
---
O
TD SettlementTransactionCondition
Indicator
---
CollateralPoolTradeIndicator
Ifthevalueof
SettlementTransactionConditionIndica
tor=COLAorCOLN,itismappedto
22FCOLE.NotethatifbothCOLAand
COLNarepresentin
SettlementTransactionConditionIndica
tor,onlythefirstvalueisusedfor
mappingto22FCOLE.
→  RepetitiveMandatorySubsequenceE1SettlementParties
16R
LineNo.
64
StartofBlock/OptionR—16c:16R:SETPRTY
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 28

---

## Page 29

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
95a
BUYR
SELL
LineNo.
65
Name:Party
FormatOptionP:
:4!c//4!a2!a2!c[3!c](Qualifier)
(BIC/BEI)
ExamplesOptionP:
:95P::BUYR//BANKUS30XX
X
:95P::SELL//BANKUS30XXX
FormatOptionQ::4!c//4*35x
(Qualifier)(Name&Address)
ExampleOptionQ:
:95Q::BUYR//ABC
BuyerA,100BuyerLane,NY,
NY55555
FormatOptionR::4!c/8c/34x
(Qualifier)(DataSource
Scheme)(ProprietaryCode)
ExamplesOptionR:
:95R::BUYR/OMGUSXXYZ
:95R::BUYR/IBRC/COD1234
5678
:95R::BUYR/DTCYID/23456
789
NA
---
M
TD ISRTDExecutingBrokeror
ISRTDInstructingParty/ID2,
TLEBSettlement/ID2,
ExecutingBrokeror
InstructingParty*/[[settlement]]
Instructions/INSTorBrokerID,
ExecutingBrokeror
InstructingParty*/[[settlement]]
Instructions/ID3,
ExecutingBrokeror
InstructingParty*/[[settlement]]
Instructions/InstitutionBIC,
ExecutingBrokeror
InstructingParty*/PartyValue
(CTMBICvalue),and
ExecutingBrokeror
InstructingParty*/OrgName
---
CptyLocalCode(ID2),
CptyID3,CptyBIC,and
CptyName
*SourcedfromCounterparty’s
side
Sourcedfromoneofthefollowing,in
order:
1. Ifthecounterparty’sPSETis
IBRCESMMXXX,then5andID2
isavailableandcontainsa9or
11charactervalue,ID2is
mappedto95aBUYR/SELLtag.
IBRCisusedastheDataSource
Schemeformapping.
IfID2isnota9-character(COD)value
oran11-character(NIF)value,orifitis
notpresent,thenrule#3triggers.
2. Ifthecounterparty’sPSETis
FRNYUS33XXX(USFEDWire)
orDTCYUS33XXX([[DTC]])and:
l IfINSTorBrokerIDispresent,
itisusedformappingto95a
BUYR/SELLtag.DTCYIDis
usedasDataSourceScheme.
l IfINSTorBrokerIDisnot
present,ID3isusedformap-
pingto95aBUYR/SELLtag.
DTCYIDisusedasData
SourceScheme.
l IfbothINSTorBrokerIDand
ID3arenotpresent,rule#3
triggers.
l IfPSETisnotequaltoones
from#1and#2above,logic
startsfrom#3below.
3. InstitutionBICisusedtomapto
95aBUYR/SELLtag.IftheInsti-
tutionBICisnotavalidBICorifit
isnotavailable,rule#4triggers.
4. ExecutingBrokerorInstruct-
ingParty(Coun-
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 29

---

## Page 30

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
terparty’s)/PartyValue(CTMBIC
Value)isusedtomaptothe95a
BUYR/SELLtag.IfthisBICisnot
validorifitisnotavailable,then
rule#5triggers.
5. ExecutingBrokerorInstruct-
ingParty(Coun-
terparty’s)/OrgNameisusedto
maptothe95aBUYR/SELLtag.
IfOrgNameisnotpresentand
95aBUYR/SELLtagcannotbe
createdwithanyotherrules,a
Fatalerrorisgenerated.
Alsonote:
l WhenaBICvalueispresent,[[Option]]
Pisusedtoformatthetag.
l WhenaProprietaryCode(suchas
ID3,ID2)ispresent,OptionRis
used.
l WhenOrgNameispresent,[[Option]]
Qisused.
l IfBuy/Sell=SELL,then95aBUYRis
used.
l IfBuy/Sell=BUYI,then95aSELLis
used.
l IftheBICis11characterslong,itis
mappedas-is.
l IftheBICis8characterslong,itis
paddedwithXXX,andthenmapped
toSWIFTtag.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 30

---

## Page 31

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
95L
ALTE
LineNo.
65
Name:Party
FormatOptionL:4!c//18!c2!n
(Qualifier)(LegalEntity
Identifier)
ExampleOptionL:
:95L::ALTE//ABCDEFGHIJK
LMQRS
NA
---
O
TD LEI(sourcedfromcounterparty's
SSI)
---
CptyLEI
Iftheinvestmentmanagerorbroker
(i.e.OriginatorofMessage)is
subscribedtotheThirdParty
Notification-LEIsubscriptionoption
(TLEI=Y)andanLEIisavailable,itis
mappedtothe95LALTEtag.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 31

---

## Page 32

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
97A
SAFE
LineNo.
66
Name:SafekeepingAccount
FormatOptionA::4!c//35x
(Qualifier)(AccountNumber)
ExampleOptionA:
:97A::SAFE//12345
NA
---
O
TD SecurityAccountor
ID2
(sourcedfromcounterparty'sSSI)
---
CptyA/C#atGlobalCustodianor
CptyLocalCode(ID2)
Sourcedfromoneofthefollowing,in
order:
1. Ifthecounterparty’sPSETisone
ofthefollowing:IBRCESMM,
IBRCESMMSCL,
IBRCESMMCDE,
IBRCESMMMVL,or
IBRCESMMXXXand:
l IfSecurityAccountisavail-
able,thatvalueisusedfor
mappingto97ASAFEtag.
l IfSecurityAccountisnotavail-
able,ID2isusedformapping
to97ASAFEtag.
l IfbothSecurityAccountand
ID2arenotavailable,97A
SAFEtagisnotcreated.
2. Ifcounterparty’sPSETisnotone
ofthefollowing:IBRCESMM,
IBRCESMMSCL,
IBRCESMMCDE,
IBRCESMMMVL,
IBRCESMMXXX:
l IftheSecurityAccountisavail-
able,itisusedformapping
intothe97ASAFEtag.
l IftheSecurityAccountisnot
available,97ASAFEtagisnot
created.
16S
LineNo.
70
EndofBlock/OptionS—16c:16S:SETPRTY
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 32

---

## Page 33

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
16R
LineNo.
64
StartofBlock/OptionR—16c:16R:SETPRTY
95a
DEAG
REAG
LineNo.
65
Name:Party
FormatOptionP:
:4!c//4!a2!a2!c[3!c](Qualifier)
(BIC/BEI)
ExamplesOptionP:
:95P::DEAG//ABCABCABCX
X
:95P::REAG//ABCABCABCX
X
FormatOptionQ::4!c//4*35x
(Qualifier)(Name&Address)
ExampleOptionQ:
:95Q::DEAG//CustodianA,
300SubagentLane,NY,NY
55555
FormatOptionR::4!c/8c/34x
(Qualifier)(DataSource
Scheme)(ProprietaryCode)
ExampleOptionR:
:95R::REAG//OMGUSAXXX
NA
---
M
TD SubAgentBIC,ID1,
SubAgentName1,
SubAgentAddress1,
SubAgentName2,and
SubAgentAddress2
(sourcedfromcounterparty'sSSI)
---
CptySubagentBICand
CptyA/C#atDepository(ID1)
SeeDEAG/REAGMapping.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 33

---

## Page 34

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
97A
SAFE
LineNo.
66
Name:SafekeepingAccount
FormatOptionA::4!C//35x
(Qualifier)(AccountNumber)
ExampleOptionA:
:97A::SAFE//12345
NA
---
O,C
TD SecurityAccountorID2
(sourcedfromcounterparty'sSSI)
---
CptyA/C#atGlobalCustodianor
LocalCode(ID2)
Sourcedfromoneofthefollowing,in
order:
1. Ifthecounterparty’sPSETisone
ofthefollowing:IBRCESMM,
IBRCESMMSCL,
IBRCESMMCDE,
IBRCESMMMVL,or
IBRCESMMXXXand:
l IfSecurityAccountisavail-
able,thatvalueisusedfor
mappingto97ASAFEtag.
l IfSecurityAccountisnot
available,ID2isusedfor
mappingto97ASAFEtag.
l IfbothSecurityAccount
andID2arenotavailable,
97ASAFEtagisnotcre-
ated.
2. Ifcounterparty’sPSETisnotone
ofthefollowing:IBRCESMM,
IBRCESMMSCL,
IBRCESMMCDE,
IBRCESMMMVL,
IBRCESMMXXX:
l IftheSecurityAccountis
available,itisusedfor
mappingintothe97A
SAFEtag.
l IftheSecurityAccountis
notavailable,97ASAFE
tagisnotcreated.
16S
LineNo.
70
EndofBlock/OptionS—16c:16S:SETPRTY
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 34

---

## Page 35

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
16R
LineNo.
64
StartofBlock/OptionR—16c:16R:SETPRTY
95a
DECU
RECU
LineNo.
65
Name:Party
FormatOptionP:
:4!c//4!a2!a2!c[3!c](Qualifier)
(BIC/BEI)
ExamplesOptionP:
:95P::DECU//ABCABCABCX
X
:95P::RECU//ABCABCABCX
X
FormatOptionQ::4!c//4*35x
(Qualifier)(Name&Address)
ExampleOptionQ:
:95Q::RECU//CustodianA,
200CustodianLane,NY,NY
55555
NA
---
O
TD CustodianBIC,CustodianName1,
andCustodianName2
(sourcedfromcounterparty'sSSI)
---
CptyCustodianBIC,
CptyCustodianName1,
andCptyCustodianName2
Sourcedasfollows,inorder:
1. IfCustodianBICispresentand
valid,itisusedtocreate95a
DECU/RECUtagusingOptionP.
2. IfCustodianBICisnotpresentor
invalid,CustodianName1and/or
CustodianName2fieldsareused
tocreate95aDECU/RECUusing
OptionQ.
Ifconditionsfrom#1and#2arenot
met,95aDECU/RECUtagisnot
created.
Notethefollowing:
l IfBuy/Sell=SELL,95aRECUis
used.
l IfBuy/Sell=BUYI,95aDECUis
used.
l IfBICis11characterslong,itis
mappedas-is.
l IfBICis8characterslong,itis
paddedwith‘XXX’andthen
mappedtoSWIFTtag.
97a
SAFE
LineNo.
66
Name:SafekeepingAccount
Format::4!c//35x(Qualifier)
(AccountNumber)
Example:
:97A::SAFE//12345
NA
---
O
TD SubAccountNo
(sourcedfromcounterparty'sSSI)
---
CptyA/C#atLocalAgent
IfSubAccountNoispresent,itisused
tomapto97ASAFE;ifnot,97ASAFE
isnotcreated.
16S
LineNo.
70
EndofBlock/OptionS—16c:16S:SETPRTY
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 35

---

## Page 36

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
16R
LineNo.
64
StartofBlock/OptionR—16c:16R:SETPRTY
95a
DEI1
REI1
LineNo.
65
Name:Party
FormatOptionP:
:4!c//4!a2!a2!c[3!c](Qualifier)
(BIC/BEI)
ExampleOptionP:
:95P::DEI1//ABCABCABCX
X
:95P::REI1//ABCABCABCX
X
FormatOptionQ::4!c//4*35x
(Qualifier)(Name&Address)
ExampleOptionQ:
:95Q::REI1//CustodianA,
400CorrespondentLane,
NY,NY55555
NA
---
O
TD Relationship,CorrespBIC,
CorrespName1,and
CorrespName2
(sourcedfromcounterparty'sSSI)
---
CptyCorrRelationshipand
CptyCorrSecurityParty
WhenRelationship=S:
l IfCorrespBICispresentandvalid,
itisusedtocreate95aDEI1/REI1
tagusingOptionP.
l IfCorrespBICisnotpresentor
invalid,CorrespName1and/or
CorrespName2fieldsareusedto
create95aDEI1/REI1using
OptionQ.
l Ifconditionsfrom#1and#2are
notmet,95aDEI1/REI1tagisnot
created.
Note:
l IfBuy/Sell=SELL,95aREI1is
used.
l IfBuy/Sell=BUYI,95aDEI1is
used.
l IfBICis11characterslong,itis
mappedas-is.
l IfBICis8characterslong,itis
paddedwithXXXandthen
mappedtoSWIFTtag.
l If95aDECU/RECUisnotcreated
butdataneededtocreate95a
DEI1/REI1ispresent,95a
DECU/RECUiscreatedusingthe
datathatwouldnormallycreate
95aDEI1/REI1.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 36

---

## Page 37

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
97a
SAFE
LineNo.
66
Name:SafekeepingAccount
Format::4!c//35x(Qualifier)
(AccountNumber)
Example:
:97A::SAFE//12345
NA
---
O
TD Relationshipand
CorrespSecAccountNo
(sourcedfromcounterparty'sSSI)
---
CptyCorrRelationshipand
CptyCorrSecurityAccount
WhenRelationship=S:
l IfCorrespSecAccountNoispresent,
itisusedtocreate97ASAFEtag
usingOptionP.
l IfCorrespSecAccountNoisnot
present,97ASAFEisnotcreated.
Note:
If95aDECU/RECUisnotcreatedbut
dataneededtocreate95aDEI1/REI1
ispresent,95aDECU/RECUis
createdusingthedatathatwould
normallycreate95aDEI1/REI1.Ifthis
happens,97ASAFE(thatwould
normallybebeneaththe95a
DEI1/REI1tag)getsmappedtosame
instanceas95aDECU/RECU.
16S
LineNo.
70
EndofBlock/OptionS—16c:16S:SETPRTY
16R
LineNo.
64
StartofBlock/OptionR—16c:16R:SETPRTY
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 37

---

## Page 38

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
95a
DECU
RECU
LineNo.
65
Name:Party
FormatOptionP::4!c//2!a
(Qualifier)(CountryCode)
ExampleOptionC:
:95C::PSET//US
FormatOptionP:
:4!c//4!a2!a2!c[3!c](Qualifier)
(BIC/BEI)
ExampleOptionP:
:95P::DECU//ABCABCABCX
X
:95P::RECU//ABCABCAB
CXX
FormatOptionQ:
:4!c//4*35x(Qualifier)
(Name&Address)
ExampleOptionQ:
:95Q::RECU//CustodianA,
200CustodianLane,NY,
NY55555
NA
---
O
TD CustodianBIC,CustodianName1,
andCustodianName2
(sourcedfromcounterparty'sSSI)
---
CptyCustodianBIC,
CptyCustodianName1,
andCptyCustodianName2
Sourcedasfollows,inorder:
1. IfCustodianBICispresentand
valid,itisusedtocreate95a
DECU/RECUtagusingOptionP
2. IfCustodianBICisnotpresentor
invalid,CustodianName1and/or
CustodianName2fieldsareused
tocreate95aDECU/RECUusing
OptionQ
Ifconditionsfrom#1and#2arenot
met,95aDECU/RECUtagisnot
created.
Notethefollowing:
l IfBuy/Sell=SELL,95aRECUis
used.
l IfBuy/Sell=BUYI,95aDECUis
used.
l IfBICis11characterslong,itis
mappedas-is.
l IfBICis8characterslong,itispad-
dedwith‘XXX’andthenmappedto
SWIFTtag.
97a
SAFE
LineNo.
66
Name:SafekeepingAccount
Format::4!c//35x(Qualifier)
(AccountNumber)Example:
:97A::SAFE//12345
NA
---
O
TD SubAccountNo(sourcedfrom
counterparty'sSSI)
---
CptyA/C#atLocalAgent
IfSubAccountNoispresent,itisused
tomapto97ASAFE;ifnot,97ASAFE
isnotcreated.
16S
LineNo.
70
EndofBlock/OptionS—16c:16S:SETPRTY
16RLine
No.64
StartofBlock/OptionR—16c:16R:SETPRTY
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 38

---

## Page 39

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
95a
PSET
LineNo.
65
Name:PartyFormatOption
C::4!c//2!a(Qualifier)(Coun-
tryCode)ExampleOptionC:
:95C::PSET//USFormat
OptionP::4!c//4!a2!a2!c[3!c]
(Qualifier)(BIC/BEI)
ExampleOptionP:
:95P::PSET//ABCABCABCX-
X
NA
---
M
TD PSET(sourcedfrom
counterparty'sSSI)
---
SettlementLocationBIC
andSettlementLocationCountry
Mappedasfollows:
l IfvalueofPSETis2charvalid
countrycode,95aPSETiscre-
atedwithOptionC
l IfvalueofPSETisvalidBIC,
95aPSETiscreatedwithOption
P
l IfPSETisnotpresentorifitis
invalid,aFatalerrorgetsgen-
erated.
Notethefollowing:
l IfBICis11characterslong,itis
mapped‘asis’
l IfBICis8characterslong,itis
paddedwith‘XXX’andthen
mappedtoSWIFTtag.
SWIFTtag:95C::PSETmustuse
OptionCif22FSTCOSWIFTcodeis
PHYS.Else,Fatalerrorisgenerated.
16SLine
No.70
EndofBlock/OptionS—16c:16S:SETPRTY
→  OptionalSubsequenceE2CashParties
16R
LineNo.
71
StartofBlock/OptionR—16c:16R:CSHPRTY
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 39

---

## Page 40

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
95a
ACCW
LineNo.
72
Name:Party(Accountwith
Institution)
FormatOptionP:
:4!c//4!a2!a2!c[3!c](Qualifier)
(BIC/BEI)
ExampleOptionP:
:95P::ACCW//ABCABCABC
XX
FormatOptionQ::4!c//4*35x
(Qualifier)(Name&Address)
ExampleOptionQ:
:95Q::ACCW//CustodianA,
TwoBankLane,NY,NY
55555
NA
---
O
TD Relationship,CorrespBIC,
CorrespName1,and
CorrespName2
(sourcedfromcounterparty'sSSI)
---
CptyCorrRelationshipand
CptyCorrCashParty
WhenRelationship=C,mappedas
follows,inorder:
l IfCorrespBICispresentandvalid,it
isusedtocreate95aACCWtag
usingOptionP
l IfCorrespBICisnotpresentor
invalid,CorrespName1and/orCor-
respName2fieldsareusedtocreate
95aACCWusingOptionQ
l Ifconditionsfrom#1and#2arenot
met,95aACCWtagisnotcreated.
Note:
IfBICis11characterslong,itis
mapped‘asis’
IfBICis8characterslong,itis
paddedwith‘XXX’andthenmapped
toSWIFTtag.
97a
CASH
LineNo.
73
Name:CashAccount
FormatOptionA::4!c//35x
(Qualifier)(AccountNumber)
ExampleOptionA:
:97A::CASH//3434343434
FormatOptionE::4!c//34x
(Qualifier)(International
BankAccountNumber)
ExampleOptionE:
:97E::CASH//IBAN1234567
NA
---
O
TD CorrespCashAccountNo
(sourcedfromcounterparty'sSSI)
---
CptyCorrCashAccount
WhenRelationship=C:
Iffirsttwocharactersoffield
CorrespCashAccountNoareavalid
countrycode,97ESAFEisusedfor
mapping.
Andiffirsttwocharactersoffield
CorrespCashAccountNoarenota
validcountrycode,97ASAFEisused
IfCorrespCashAccountNoisnot
present,97aSAFEisnotcreated.
Note:ACorrespCashAccountNovalue
withfirsttwocharactersasacountry
codeisassumedanInternationalBank
AccountNumber.
16S
LineNo.
75
EndofBlock/OptionS—16c:16S:CSHPRTY
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 40

---

## Page 41

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
→RepetitiveMandatorySubsequenceE3Amounts
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
ACRU
LineNo.
78
Name:AccruedInterest
Amount
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::ACRU//KRW5000,
NA
---
O
TD AccruedInterestAmount/
Sign,CurrencyCode,andAmount
---
TradeCurrencyand
AccruedInterest
Mapsthevaluesofsourcefieldsto19A
ACRU.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
CHAR
LineNo.
78
Name:ChargesorFees
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::CHAR//CAD40000,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=CHAR)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=CHARGES_FEES)
Mapsthevaluesofsourcefieldsto19A
CHAR.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 41

---

## Page 42

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
19A
COUN
LineNo.
78
Name:Country,National,
FederalTax
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::COUNR//GBR,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=COUN)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=COUNTRY_
NATIONAL_FEDERAL_TAX)
Mapsthevaluesofsourcefieldsto19A
COUN.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
DEAL
LineNo.
78
Name:TradeAmount
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::DEAL//SEK100,
NA
---
M
TD TradeAmount/Sign,CurrencyCode,
andAmount
---
TradeCurrencyand
TradeAmount
Mapsthevaluesofsourcefieldsto19A
DEAL.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
EXEC
LineNo.
78
Name:Charges/Fees
(ExecutingBroker)
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::EXEC//GBR10,
NA
---
O
TD Commission/Sign,CurrencyCode,
andAmount
(whereChargeTaxType=EXEC)
---
TradeCurrencyand
CommissionAmount
(whereType=EXECUTING_
BROKER_COMMISSION)
Mapsthevaluesofsourcefieldsto19A
EXEC.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 42

---

## Page 43

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
LADT
LineNo.
78
Name:LocalTax(country
specific1)
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::LADT//EUR4,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=LADT)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=LOCAL_TAX_
COUNTRY_SPECIFIC)
Mapsthevaluesofsourcefieldsto19A
LADT.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
LEVY
LineNo.
78
Name:PaymentLevyTax
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::LEVY//BRL153,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=LEVY)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=PAYMENT_LEVY
_TAX)
Mapsthevaluesofsourcefieldsto19A
LEVY.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 43

---

## Page 44

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
19A
LOCL
LineNo.
78
Name:LocalTax
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::LOCL//CNY15,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=LOCL)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=LOCAL_TAX)
Mapsthevaluesofsourcefieldsto19A
LOCL.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
LOCO
LineNo.
78
Name:LocalBroker’s
Commission
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::LOCO//DKK15,
NA
---
O
TD Commission/Sign,CurrencyCode,
andAmount
(whereChargeTaxType=LOCO)
---
TradeCurrencyand
CommissionAmount
(whereType=LOCAL_
BROKER_COMMISSION)
Mapsthevaluesofsourcefieldsto19A
LOCO.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
OTHR
LineNo.
78
Name:OtherAmount
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::OTHR//SEK15.
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=OTHR)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=OTHER_AMOUNT)
Mapsthevaluesofsourcefieldsto19A
OTHR.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 44

---

## Page 45

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
RSCH
LineNo.
78
Name:ResearchAmount
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::RSCH//DKK15,
NA
---
O
TD Commission/Sign,CurrencyCode,
andAmount
(whereChargeTaxType=RSCH)
---
TradeCurrencyand
CommissionAmount
(whereType=RESEARCH_FEE)
Mapsthevaluesofsourcefieldsto19A
RSCH.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
REGF
LineNo.
78
Name:RegulatoryAmount
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::REGF//BRL15,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=REGF)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=REGULATORY_
AMOUNT)
Mapsthevaluesofsourcefieldsto19A
REGF.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 45

---

## Page 46

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
19A
SETT
LineNo.
78
Name:SettlementAmount
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
19A::19A::SETT//USD37204
5,00
NA
---
M
TD SettlementAmount/Sign,
CurrencyCode,andAmount,and
NetCashAmount/Sign,
CurrencyCode,andAmount
---
SettlementAmount/Institution
SettlementAmount(forcross
currency)and
SettlementCurrency
Mapsthevaluesofsourcefieldsto19A
SETT.
IfSettlementInstructionManager
determinesthatthetrademeetsthe
criteriaofanoncrosscurrencytrade,
then
-Mapthevaluesofsourcefieldsto
19ASETT
Else
-forcrosscurrencytrades,
Maptotheoptionalfieldsof
:19A::RESUand:92B::EXCHas
displayedbelow.
19A
RESU
Line
No.78
Name:ResultingAmount
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example::19A::
:19A::RESU//GBR1002,45
NA
---
O
TD NetCashAmount/Sign,
CurrencyCode,andAmount
---
NetCashAmount
IfSettlementInstructionManager
determinesthatthetrademeetsthe
criteriaofacrosscurrencytrade,
then
Mapthevaluesofsourcefieldsto
19ARESU.
92B
EXCH
Line
No.80
Name:ExchangeRate
Format::4!c//3!a/3!a/15d
(Qualifier)(FirstCurrency
Code)(SecondCurrency
Code)(Rate)
Example::
92B::EXCH//GBP/USD/1,6
19or
:92B::EXCH//USD/GBP/0,
618
NA
---
O
TD ExchangeRate/FromCurrency,To
Currency,ExchangeRateAmount
---
FromCurrency,ToCurrency,
ExchangeRate
IfSettlementInstructionManager
determinesthatthetrademeetsthe
criteriaofacrosscurrencytrade,
then
Mapthevaluesofsourcefieldsto
92BEXCH.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 46

---

## Page 47

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
19A
SHIP
LineNo.
78
Name:ShippingAmount
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::SHIP//CNY15,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=SHIP)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=SHIPPING_FEES)
Mapsthevaluesofsourcefieldsto19A
SHIP.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
SPCN
LineNo.
78
Name:SpecialConcessions
Amount
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::SPCN//HKD15,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=SPCN)
---
TradeCurrencyand
CommissionAmount
(whereType=SPECIAL_
CONCESSION)
Mapsthevaluesofsourcefieldsto19A
SPCN.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 47

---

## Page 48

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
19A
STAM
LineNo.
78
Name:StampDuty
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::STAM//GBR15,
4
---
Optional
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=STAM)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=STAMP_DUTY)
Mapsthevaluesofsourcefieldsto19A
STAM.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
STEX
LineNo.
78
Name:StockExchangeTax
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::STEX//JPY15,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=STEX)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=STOCK_
EXCHANGE_TAX)
Mapsthevaluesofsourcefieldsto19A
STEX.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 48

---

## Page 49

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
19A
TRAN
LineNo.
78
Name:TransferTax
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::TRAN//USD15,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=TRAN)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=TRANSFER_TAX)
Mapsthevaluesofsourcefieldsto19A
TRAN.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
19A
TRAX
LineNo.
78
Name:TransactionTax
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::TRAX//ARS15,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=TRAX)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=TRANSACTION_
_TAX)
Mapsthevaluesofsourcefieldsto19A
TRAX.
Notethefollowing:
l Ifthemarketdeterminedby
PSETisAustralia,
ChargeTaxTypeofTRAXis
mappedto19A::VATA.
l IfSequenceE/22Fcontains
StampDutyIndicatoranditis
mappedwithDataSource
SchemeofCRST(suchas-
STAM/CRST/value),thenTRAX
ismappedto19A::STAM.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16R
LineNo.
76
StartofBlock/OptionR—16c:16R:AMT
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 49

---

## Page 50

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
19A
VATA
LineNo.
78
Name:Value-AddedTax
Format::4!c//[N]3!a15d
(Qualifier)(Sign)(Currency
Code)(Amount)
Example:
:19A::VATA//BRL15,
NA
---
O
TD ChargeAmount/Sign,
CurrencyCode,
andAmount
(whereChargeTaxType=VATA)
---
TradeCurrencyand
Charge/Tax/Fee
(whereType=VALUE_ADDED_
TAX)
Mapsthevaluesofsourcefieldsto19A
VATA.
16S
LineNo.
81
EndofBlock/OptionS—16c:16S:AMT
16S
LineNo.
82
EndofBlock/OptionS—16c:16S:SETDET
MandatorySequenceFOtherParties
Note:ThissequenceisoptionalforSWIFT,butSettlementInstructionManagermanditorilymapsSequenceF.
16R
LineNo.
83
StartofBlock/OptionR—16c:16R:OTHRPRTY
95a
MEOR
LineNo.
84
Name:Originatorof
Message
FormatOptionP:
:4!c//4!a2!a2!c[3!c](Qualifier)
(BIC/BEI)
ExampleOptionP:
:95P::MEOR//THANUS31XX
X
NA
Mandato
ry
TD InstructingParty/PartyValue
ExecutingBroker/PartyValue
(wherePartyType=BIC)
---
BIC
l BICofInstructingPartymapsto95P
MEORforInvestmentmanager
instructions
l BICofExecutingBrokermapsto
95PMEORforExecutingBroker
instructions
Notethefollowing:
l IftheBICis11characterslong,
itismappedas-is.
l IftheBICis8characterslong,it
ispaddedwith‘XXX’andthen
mappedtoSWIFTtag.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 50

---

## Page 51

SWIFT
Tag/
Qualifi
er&
Line#
SWIFTField
Name/Format/Exampl
e
SWIFT
Codes
---
M-O-C
AG/
TD
CTMSource
---
SettlementInstruction
ManagerUIMapping
Note
16S
LineNo.
88
EndofBlock/OptionS—16c:16S:OTHRPRTY
-}
1 CTMsupportsthefollowingSWIFTcodes:BCFD,BCPD,CBNS,CCPN,CDIV,CRTS,GTDL,SPCU,SPEX,
XBNS,XCPN,XDIV,andXRTS.
2 CTMsupportsthefollowingSWIFTcodes:BUTC,CLEN,DIRT,EXER,FRCL,NOMC,NPAR,PART,PHYS,
RPTO,SHOR,SPDL,SPST,UNEX,andTRIP.
3 CTMsupportsthefollowingSWIFTcodes:CONV,ETFT,ISSU,NETT,OAUX,OTCS,OWNI,PLAC,and
TRAD.
4 CTMsupportsthefollowingSWIFTcodes:GBAX,GBBX,GBCX,GBDX,GBEX,GBFX,GBGX,GBHX,GBIX,
GBLX,GBMX,GBNX,GBOX,GBPX,GBRX,GBSX,
GBTX,GBUX,GBVX,GBWX,GBXX,GB2X,GB3X,GB4X,GB5X,GB6X,GB7X,IEJX,IEQX,IEYX,IE1X,IE8X,
andUSTN.
5 ThefollowingPSETBICsmergedintoasingleBIC,IBRCESMMXXX:IBRCESMM,IBRCESMMSCL,
IBRCESMMCDE,IBRCESMMMVL,andIBRCESMMXXX.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 51

---

## Page 52

CrossCurrencyTrade
Thesettlementdetailisdeterminedtobeacrosscurrencytradewhen
l TheinvestmentmanagerhasprovidedaSettlementAmount
l TheinvestmentmanagerhasprovidedanExchangeRate,wheretheFromCurrencyandToCurrency
containsdifferentcurrencies.
DEAG/REAGMapping
Sourcedfromoneofthefollowing,inorder:
1. IfCounterparty’sPSET=FRNYUS33XXXorDTCYUS33XXX,95aDEAG/REAGismappedwithvaluefrom
ID1.DataSourceSchemeforFRNYUS33XXXandDTCYUS33XXXareUSFWandDTCYIDrespectively.
IfID1isnotpresent,Fatalerrorgetsgenerated.
2. IfCounterparty’sPSETisa2-charactervalidcountrycode,
a. 95aDEAG/REAGismappedwithvaluefromSubAgentBIC.IfSubAgentBICisinvalid,Fatalerrorisgen-
erated.
b. IfSubAgentBICisnotpresent,valuefromSubAgentName1,SubAgentAddress1,SubAgentName2and
SubA-gentAddress2isusedtomapto95aDEAG/REAG.
c. If95aDEAG/REAGcannotbecreatedfromabovetwoways,FatalErrorisgenerated.
3. IfCounterparty’sPSETisnotfrom#1and#2above,95aDEAG/REAGiscreatedbasedontheDel/RecAgent
FormatPriority(akaBICLIDPriority)configurationofthatPSETBIC.
a. IfBICLIDPriorityisBICFormatOnly(akaBICX),95aDEAG/REAGismappedwithSubAgentBIC.If
SubA-gentBICisnotpresentorifitisinvalid,Fatalerrorisgenerated.
b. IfBICLIDPriorityisID1FormatOnly(akaLIDX),95aDEAG/REAGismappedwithID1.DataSource
Scheme(relatedtothePSET)isobtained.IfEitherID1orDataSourceSchemeisnotavailable,Fatal
Errorisgenerated.
c. IfBICLIDPriorityisBICFormatSupersedesID1Format(akaBICP):
i. 95aDEAG/REAGismappedwithSubAgentBICasfirstpriority.IfSubAgentBICisinvalid,Fatalerror
isgen-erated.
ii. IfSubAgentBICisnotpresent,asasecondpriorityID1ususedtomapto95aDEAG/REAG.Data
SourceScheme(relatedtothePSET)isobtainedfromtheDTCCproprietarydatabase.
iii. IfSubAgentBICisnotpresentandID1orDataSourceSchemeisnotavailable,FatalErrorisgen-
erated.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 52

---

## Page 53

4. IfBICLIDPriorityisID1FormatSupersedesBICFormat(akaLIDP):
a. 95aDEAG/REAGismappedwithID1asfirstpriority.DataSourceScheme(relatedtothePSET)is
obtained.
b. IfEitherID1orDataSourceSchemeisnotavailable,SubAgentBICisusedasasecondprioritytomapto
95aDEAG/REAG.
c. IfID1orDataSourceSchemeisnotpresentandSubAgentBICisnotpresentorinvalid,Fatalerroris
gen-erated.
5. IfBICLIDpriorityisBICFormatSupersedesAddress:
a. 95aDEAG/REAGismappedwithSubAgentBICasfirstpriority.IfSubAgentBICisinvalid,Fatalerroris
gen-erated.
b. IfSubAgentBICisnotpresent,SubAgentName1,SubAgentAddress1,SubAgentName2andSubA-
gentAddress2isusedtomapto95aDEAG/REAG.
c. If95aDEAG/REAGisnotcreatedfromabovetwoways,Fatalerrorisgenerated.
Alsonotethefollowing:
l WhenaBICvalueispresent,OptionPisusedtoformatthetag.
l WhenaProprietaryCode(suchasID1)ispresent,OptionRisused.
l WhenNames(likeSubAgentName1,SubAgentAddress1,etc)arepresent,OptionQisused.
And:
l IfBuy/Sell=SELL,95aREAGisusedforInvestmentmanagerinstructionsand95aDEAGforExecutingBroker
instructions.
l IfBuy/Sell=BUYI,95aDEAGisusedforInvestmentmanagerinstructionsand95aREAGforExecutingBroker
instructions.
And:
l IfBICis11characterslong,itismappedas-is.
l IfBICis8characterslong,itispaddedwithXXXandthenmappedtoSWIFTtag.
l IfBICLIDPriorityisnotavailable,95aDEAG/REAGgetsmappedwithBICFormatSupersedesID1Format
logic.
And:
l Ifanon-SWIFT characterisreceivedintextfields(i.e.,fieldswithx-characterset),itisreplacedwithspaceand
errorwillnotbegenerated.TheSWIFTwillbecreatedwithresultingvalue.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 53

---

## Page 54

Handlingofnon-SWIFTcharactersintextfields
l Ifanon-SWIFTcharacterisreceivedintextfields(i.e.,fieldswithx-characterset),itisreplacedwithspaceand
noerrorwillbegenerated.TheSWIFTwillbecreatedwiththeresultingvalue.
SupportofCTMOrganizationswithoutValidRegistered
SWIFTBIC
IfaCTMorganizationissetupwithaninvalidSWIFTBIC,the95aMEOROriginatorofMessageissourced
basedonthebelowpriority:
o BICCodeofinstructingpartyorexecutingbrokerismappedto95aMEORasafirstpriority.TheSWIFTwill
becreatedwiththeresultingvalue.
o IfBICCodeofinstructingpartyorexecutingbrokerisnotavalidregisteredSWIFTBIC,Institution/Execut-
ingBrokerBICfromtheInstructingParty’sorExecutingBroker’sSSIismappedto95aMEORasasecond
priority.TheSWIFTwillbecreatedwiththeresultingvalue.
o IfInstitution/ExecutingBrokerBICfromtheInstructingParty’sorExecutingBroker’sSSIisnotavalid
registeredSWIFTBICorisnotprovided,theFatalErrorisgenerated.
SWIFTMT541/543MessageSpecification
1.SWIFTMT541/543Message 54

---

## Page 55

©2024Allrightsreserved.[[DTCC]],[[DTCC]](Stylized)andFinancialMarkets.Forward.areregisteredandunregistered
trademarksofTheDepositoryTrust&ClearingCorporationDTCC.Theservicesdescribedhereinareprovidedunder
the“[[DTCC]]”brandnamebycertainaffiliatesofTheDepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitself
doesnotprovidesuchservices.Eachoftheseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsof
theparticularcountryorcountriesinwhichsuchentityoperates.Pleaseseewww.[[DTCC]].comformoreinformationon
[[DTCC]],itsaffiliatesandtheservicestheyoffer.
DocDate:February01,2024
PublicationCode:SIM026
Service:SettlementInstructionManager
Title:SWIFTMT541/543MessageSpecification
ForMoreInformation
EmailDTCCLearningat:
DTCCLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com