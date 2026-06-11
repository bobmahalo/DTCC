---
title: "Security Master File Data - MMI IntraDay Securities User's Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat315_sec_mas_prem_ug_20231017.pdf"
pages: 92
size: "509.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Security Master File Data - MMI IntraDay Securities User's Guide

**Original File:** [dat315_sec_mas_prem_ug_20231017.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat315_sec_mas_prem_ug_20231017.pdf)  
**Category:** Other  
**Total Pages:** 92  
**File Size:** 509.2 KB  

---

## Page 1

SecurityMasterFileData
PREMIUMMASTERFILEUSER'SGUIDE
OCTOBER17,2023

---

## Page 2

TABLEOFCONTENTS
1.Introduction/Background 4
2.SupportandAssistance 5
3.MessageHandling 6
StandardFileHeader 6
StandardMessageStarter 8
ProgrammerNotes 8
MessageLength 8
MessageFiller 9
HeaderMessageSpecifics 9
TrailerMessageSpecifics 10
DataMessageSpecifics 10
4.FileDescriptionsandAcronyms 13
InternationalUpdateFiles-MessagesandVolumes 13
InternationalMasterFiles-Messages&Volumes 13
DescriptiveUpdateFiles-MessagesandVolumes 14
DescriptiveMasterFiles-Messages&Volumes 15
MiscFiles-MessagesandVolumes 16
AgentFiles-MessagesandVolumes 18
5.FileDelivery 19
DeliveryInformation 19
FileAvailabilityandDelivery 19
6.MessageFormats 21
SecurityMasterFileData- PremiumMasterFileUser'sGuide
TableOfContents 2

---

## Page 3

HeaderMessage-H01 21
InternationalMessage-I01 21
IssuerMessage-D01 23
IssuanceMessage-D02 25
IssueMessage-D03 29
DescriptiveMessage-D05 38
DepositoryStatusMessage-D06 40
AgentMessage-A01 48
AgentDescriptiveMessage-A02 51
LimitedEligibilityMessage–L01 54
TrailerMessage-T01 55
A.DTCSub-IssueTypes 57
B.DTCSecurityClassification 62
C.ISOUnitedStatesandCanadianProvinces 64
D.ISOCountryCodes 68
E.ISOCurrencyCodes 80
F.MBSProductIDValues 90
SecurityMasterFileData- PremiumMasterFileUser'sGuide
TableOfContents 3

---

## Page 4

1.INTRODUCTION/BACKGROUND
SecurityMasterFileDataconsistsofaseriesofmultiplemessagetypesthatcover:
l eligibility
l formalorlegalissuedescriptions
l agentinformation
l eventdata(corporateactions,distributionsandredemptions)
Thefiledeliveryconsistsofend-of-dayactivity(ormasterfiles)segmentedbysixDTCproducttypes,
specifically:
l Equities
l CorporateFixedIncome
l Municipals,Government
l Mortgage/AssetBacked
l MoneyMarketInstruments
Theserviceaddressescustomerneedsbycentralizingandstandardizingsecurityinformationandby
providingthedatadirectlyintocustomersystems.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
1.Introduction/ Background 4

---

## Page 5

2.SUPPORTANDASSISTANCE
Ifyouhaveanyquestionsregardingthisdocumentoranyissueregardingtheinformationhereinorits
delivery,call1-800-253-2488.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
2.SupportAndAssistance 5

---

## Page 6

3.MESSAGEHANDLING
StandardFileHeader
AllfileshavethestandardheaderandtheHeaderMessage.Thenexttabledescribestheformatofthefile
header.TheCreationDateandLoadDatearepopulatedwiththecurrentDTCCbusinessdateonthe
dateoffilecreation.
Note
SeeMessageFormatsintheMessageFormatsonpage 21forinformationontheHeaderMessage.
Position Length Format Description
1 3 Character RecordID:
l HDR
-or-
l TRL
4 8 Character SignonID
12 6 Character DataTypeRequested
18 6 Character DataTypeCreated
24 8 Character DataCreationDate(YYYYMMDD)
32 8 Character DataLoadDate(YYYYMMDD)
40 8 Character DataLoadTime(HH:MM:SS)
48 4 Numeric DataLengthofDataRequested
52 8 Numeric Numberofdatarecordsinthefile
Table3.1MessageHandling
SecurityMasterFileData- PremiumMasterFileUser'sGuide
3.MessageHandling 6

---

## Page 7

Position Length Format Description
60 4 Numeric NumberofRecordsperdatatyperequested(0001)
64 Function
Length
Numeric Reservedfilledwithspacesforfutureuse.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
3.MessageHandling 7

---

## Page 8

StandardMessageStarter
Thenexttablecontainsalistingoftheinitial31charactersofmostmessages,withtheexceptionofthe
header,trailerandagentrecords.
Position Length Format FieldName Description
1–2 3 Character MessageType ThetypeofMessage.ThevalueisI01
(International).
4–9 6 Numeric Message
SequenceNumber
Identifiesthesequencenumberwithinthe
Messagetype.Initializedto000001.
10–10 1 Character MessageStatus
Type
IndicatesifDTCisaddinganewmessageor
updatinganexistingmessage.
Thevaluesare:
l A:Add
l U:Update
l M:Matured(onlyinI01andD03
messages)
MasterfilehavetheirstatustypesettoA.
Limitedeligibilityfileshavethefollowingvalues:
l A:Add
l C:ExistingSecurity
11–19 9 Character Issue
Identifier
The9-characterCUSIPnumber.
20–31 12 Character International
Identifier
The12-characterISIN(InternationalSecurities
IdentificationNumber)number,ifavailable.
Table3.2StandardMessageStarter
ProgrammerNotes
MessageLength
Eachmessageis300charactersinlength.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
3.MessageHandling 8

---

## Page 9

MessageFiller
Currentlyallmessagesalsohavefillerthatallowsforappendingadditionaldatatothemessage.Notethe
followingrelatedtodevelopingprogramsforthesemessages:
l Messagesshouldreflectthatthesefillercomponentswillbeeventuallybefilledwithdata.
l Ensurethatprogramswillnotifdataisappendedtothefillerareaofthemessage.
l Developprogramswiththecapacitytostoreandpotentiallyretrievedatafromthesefillerareas.
l Iftheentiremessageisfilled,itispossibletoaddmoremessageswithadditionalinformationtothe
messagetype.
HeaderMessageSpecifics
TheHeadermessageprovidesdetailsregardingthefileanditsdateofcreation.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
3.MessageHandling 9

---

## Page 10

TrailerMessageSpecifics
TheTrailermessageprovidesdetailsonthenumberofrecordsprocessedandindicatestheendoffile.
DataMessageSpecifics
DataMessagesallstartwiththesameinitial31charactersthatprovidethefollowinginformation:
l MessageType:TheMessageTypereferencesthetypeofmessage(seeTable3.2),allowingusers
tofocuson(ordisregard)messagesthatcontainspecificinformationofinterest.Analphanumeric
indicatorallowsforexpandingthenumberofmessagetypeforadditionaldata.
l MessageSequenceNumber:Thisnumberisinitializedat000001.Ifasecurityrequiresadditional
data,suchasforaseriesofevents,theywillberepeatedandthecounter-incremented.
l MessageStatusType:Thestatustypeindicateswhethertherecordisanadded,change,orsecurity
matured.
l SecurityIdentifier:Everyrecordcontainstheapplicableissueorinternationalidentifierthatisunique
tothatsecurity.
o Theinclusionofthisidentifieroneachrecordsoffersusersmaximumflexibilityindownloading
messagestodifferentmedia,suchasspreadsheetsorapplications,aswellthedataparsingcap-
abilities.
o Theintentistomaximizetheavailabilityofthedatabothtomainframesanddiscreteapplications
andthereinassistingorganizationsinstandardizinginformationfromDTC.
l SecurityMaturityHandling:
l IntheStandardMessageStarter,securitiesthathavematuredareonlydesignatedinthe
DescriptiveMessageD03,unlessreceivingtheInternationalmessage.
l M:Matured(onlyin01andD03messages).
l DataHandling:
WhenDTCCisnotprovidedadateassociatewithadistribution,DTCCsuppliesdefaultvaluesinthe
datefieldwhichcanbedisregarded.Thedefaultvaluesare:
00010101
00010102
99999999
SecurityMasterFileData- PremiumMasterFileUser'sGuide
3.MessageHandling 10

---

## Page 11

00000000
blank
Securitieswithamaximummaturitydate,suchasaperpetualbond,willhavethevalueof29991231.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
3.MessageHandling 11

---

## Page 12

l NotesonEBCDICForm:TheinformationcontainedinthisserviceisderivedfromDTCCmainframe
systems,whicharecompiledinEBCDIC.Assuch,certainvaluessignalingpositiveandnegativeare
presentedinEBCDICform.These“signed”fieldsareindicatedbythevalue“S”priortoformat(for
example.S9(7)V9(8)).Thenexttablepresentsthetranslations.
LastIntegerValue Positive Negative
0 { }
1 A J
2 B K
3 C L
4 D M
5 E N
6 F O
7 G P
8 H Q
9 I R
Table3.3EBCDIC-FormattedValues
SecurityMasterFileData- PremiumMasterFileUser'sGuide
3.MessageHandling 12

---

## Page 13

4.FILEDESCRIPTIONSANDACRONYMS
Thischaptercontainsalistingofthecurrentlyavailablefiles.Allfilescontainaseriesofmessagesgrouped
together,andthatincludebothheaderandtrailerrecords.Volumesarereportedintheaveragenumberof
recordstobeexpected.ThedescriptiveandactivityfilesaresegmentedbyDTCProducttypes,compiled
fromtheDTCsub-issuetypesusedfordepositoryprocessinganddefinedinDTCSecurityClassification
onpage 62.
InternationalUpdateFiles-MessagesandVolumes
Table4.1liststhefilesthatcancurrentlyberequestedbyInternationalCentralSecurityDepositories
(ICSDs).
FileName FileType SecurityType ContainsRecords ExpectedVolume
CSDCUP DescriptionUpdates ManagedList H01,S01,T01 300
REGSUP NewSecurities RegulationSSecurities H01,S02,T01 30
Table4.1InternationalUpdateFiles
InternationalMasterFiles-Messages&Volumes
Table4.2listthecurrentlyavailablefiles.
FileName FileType Security
Type
Contains
Records
Expected
Volume
CSDMST DescriptionUpdates ManagedList H01,S01,T01 1,500
REGSMF MasterFile RegulationSSecurities H01,S02,T01 8,000
Table4.2InternationalMasterFiles
SecurityMasterFileData- PremiumMasterFileUser'sGuide
4.FileDescriptionsAndAcronyms 13

---

## Page 14

DescriptiveUpdateFiles-MessagesandVolumes
4liststhechangefilesthatarecurrentlyavailableforrequest.
File
Name
FileType Security
Type
Contains
Records Expected
Volume
AMBCUP Descriptive
Change
Assetand
Mortgage
backed
l H01
l D01
l D02
l D03
l D05
l D06
l A01
l T01
2,000–
5,000
MUNCUP Descriptive
Change
Municipals l H01
l D01
l D02
l D0
l D05
l D06
l A01
l T01
8,000–
70,000
InternationalMasterFiles
SecurityMasterFileData- PremiumMasterFileUser'sGuide
4.FileDescriptionsAndAcronyms 14

---

## Page 15

DescriptiveMasterFiles-Messages&Volumes
Table4.3liststhemasterfilesthatareavailableforseparaterequest.Duetotheirlargesize,thefileswill
onlybegeneratedonweekendsandwillrequireapre-arrangedschedulingwithDTCCDataServices
personnel.
FileName FileType Security
Type
Contains
Records
ExpectedVolume
AMBMST DescriptiveMaster Assetand
Mortgagebacked
l H01
l D01
l D02
l D03
l D05
l D06
l A01
l T01
7,000,00
CRPMST DescriptiveMaster CorporateBond,
Derivativesand
Trusts
l H01
l D01
l D02
l D03
l D05
l D06
l A01
l T01
10,000,000
EQTMST Descriptive
Master
EquityandEquity
Type
l H01
l D01
l D02
l D03
l D05
l D06
l A01
l T01
1,000,000
Table4.3DescriptiveMasterFiles
SecurityMasterFileData- PremiumMasterFileUser'sGuide
4.FileDescriptionsAndAcronyms 15

---

## Page 16

FileName FileType Security
Type
Contains
Records
ExpectedVolume
GOVMST DescriptiveMaster Government l H01
l D01
l D02
l D03
l D05
l D06
l A01
l T01
200,000
MMIMST DescriptiveMaster MoneyMarket
Instruments(CP,
VRDO,MTNs,and
soon)
l H01
l D01
l D02
l D03
l D05
l D06
l A01
l T01
1,000,000
MUNMST Descriptive
Master
Municipals l H01
l D01
l D02
l D03
l D05
l D06,
l A01
l T01
8,000,000
MiscFiles-MessagesandVolumes
Table4.4liststhefilethatiscurrentlyavailableforrequest.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
4.FileDescriptionsAndAcronyms 16

---

## Page 17

FileName FileType SecurityType Contains
Records
ExpectedVolume
LTDMST Alladdedand
currentLimited
EligibilitySecurities
NewandCurrent l H01
l D01
l D02
l D03
l D05
l D06
l A01
l L01
l T01
1,000
Table4.4MiscFiles
SecurityMasterFileData- PremiumMasterFileUser'sGuide
4.FileDescriptionsAndAcronyms 17

---

## Page 18

AgentFiles-MessagesandVolumes
Table4.5liststhefilesthatarecurrentlyavailableforrequest.
FileName FileType SecurityType Contains
Records
ExpectedVolume
AGNTUP AgentUpdate Agentchanges l H01
l A02
l T01
150
AGNTMF AgentMaster Listingofallagent
informationfor
MMIsonly
l H01
l A02
l T01
15,000
NAMMMF AgentMaster Listingofallagent
informationfornon-
MMIs
l H01
l A02
l T01
48,000
Table4.5AgentFiles
SecurityMasterFileData- PremiumMasterFileUser'sGuide
4.FileDescriptionsAndAcronyms 18

---

## Page 19

5.FILEDELIVERY
[[DTCC]] deliversthefilesusingFTP(filetransferprotocol)orNDM(NetworkDataMover).Subscriberswho
requestthefilewillberequiredtoprovidecontactinformationtotheirDTCCDataServicesRelationship
Managementcontact,whowillforwardtheinformationtoDTCC’sInterfacePlanningGroup(IPG).
DeliveryInformation
Inyouremail,statetheservice(s)youarerequesting,alongwiththefollowinginformation:
l OfficialCompanyName
l CompanyAddress
l DTCCSign-on/ParticipantNumbers:tobeconfirmedorassignedbyIPG
l ContactName:ContactTitle
l ContactTelephoneNumber(a)
l ContactE-mailAddress
l GeneralRequestDescription:EstablishFiledeliveryof......
IfyourfirmcurrentlycommunicateswithDTC,providethesign-on/participantnumberusedto
receive/sendinformation,andspecifywhetheryouareusingadial-upconnectionoradedicatedline.
IfyouareanewusertoDTCCandplanonusingadial-upconnection,InterfacePlanningwillforward
informationregardingestablishingconnectivityviaATT'sAGNSnetwork.
YourresponseswillbeforwardedtotheInterfacePlanningGroup,whichmanagethesetupof
communicationsandcoordinatestheschedulingoftheprocessestomakethefilesavailable.
FileAvailabilityandDelivery
l AllDWIZdailyfiles(*changefiles)becomeavailablebetween9-10pmandareavailablefor20hours.
l TheonlyfilethatisnotcreateddailyisNAMMMF,whichiscreateweekly,everySaturdaymorningat
approximately1PM,andisavailablefortheweek.
l Masterfiles:
o AllmasterfilesarecreatedonmonthlybasisonthelastSaturdayofthemonthandareavailable
forthenexttwoweeks.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
5.FileDelivery 19

---

## Page 20

o IfyourequireadditionalMasterfiles,schedulethemonapre-arrangedbasiswithDTCC Data
ServicesrepresentativesandtheInterfacePlanningGroupatleasttwoweeksinadvance.These
fileswillbegeneratedoveraweekendandwillbeavailableforpickupthesameday.
o Masterfileswill onlybedeliveredviaFTP.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
5.FileDelivery 20

---

## Page 21

6.MESSAGEFORMATS
HeaderMessage-H01
ThenexttabledescribestheHeadermessage,whichistheinitialmessageattachedtoeveryfiletype.
Position Length Format FieldName Description
1–3 3 Character MessageType Identifiesthemessagetype.ThevalueisH01
(HeaderMessage).
4–9 6 Character Message
Sequence
Number
Identifiesthesequencenumberwithinthe
messagetype.Initialized to000001.
10–17 8 Numeric FileDate Thedatethefile wasprocessedinCCYYMMDD
format.
18–25 8 Character FileName Thenameofthefile.Thevaluesareprovidedin
FileDescriptionsandAcronymsonpage 13.
26–300 273 Character Filler Reservedforfutureuse.
Table6.1IssuerMessage-D01
InternationalMessage-I01
ThenexttabledescribestheInternationalMessage,whichiscurrentlyusedexclusivelyforCSDs(Central
SecurityDepositories).
Position Length Format FieldName Description
1–3 3 Character MessageType ThetypeofMessage.ThevalueisI01(International).
4–9 6 Numeric Message
Sequence
Number
Identifiesthesequencenumberwithinthe
Messagetype.Initializedto000001.
Table6.2IssuerMessage-D01
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 21

---

## Page 22

Position Length Format FieldName Description
10–10 1 Character Message
StatusType
IndicatesifDTCisaddinganewmessageorupdating
anexistingmessage.
l A:Add
l U:Update
l M:Matured
11–19 9 Character IssueIdentifier The9-characterCUSIPnumber.
20–31 12 Character International
Identifier(ISIN)
The12-characterISIN(InternationalSecurities
IdentificationNumber)number,ifavailable.
32–91 60 Character IssuerName ThefirstoccurrenceoftheformalIssuername
appearingontheProspectusorOfferingStatement
thatissuppliedtoDTCduringeligibilityprocessing.
Thisdescriptionprovidesaconsistentissuername
acrosstheissuanceandissues.TheIssuerorIssuing
Agentmayalsoprovidethedescriptionifthesecurity
doesnotgothroughtheeligibilityprocess(for
example,forMBSsecurities).
92–94 3 Character IssuerCountry
ofOrigin
Thethree-characterISOcountrycode.Thevalues
arecontainedinISOCountryCodesonpage 68.
95–95 1 Character IssueType Thetypeofsecurity.Thevaluesare:
o 1:[[Equity]]
o 5:CorporateDebt
o 7:MunicipalDebt.
96–98 3 Character Sub-Issue
Type
Thetypeofissueorsub-issueusedbyDTCtoclassify
asecurity.ThevaluesarecontainedinDTCSub-
IssueTypesonpage 57.
99–99 1 Character DeliverOrder
ChillActivity
Flag
IndicateswhetherthesecurityiseligibleforDTC
DeliverOrderactivity.Thevaluesare:
l Y:Yes
l N:No
l Blank:NotApplicable/NotAvailable
100–
300
201 Character Filler Reservedforfutureuse.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 22

---

## Page 23

IssuerMessage-D01
ThenexttabledescribestheIssuerMessage,whichcontainsIssuerinformationabouttheDTCsearch,as
wellasashortdescription,stateanddomicileofissuance.
Position Length Format FieldName Description
1–3 3 Character MessageType ThetypeofMessage.ThevalueisD01([[issuer]]).
4–9 6 Numeric Message
Sequence
Number
Identifiesthesequencenumberwithinthemessage
type.ThisvalueisInitializedto000001.
10–10 1 Character MessageStatus
Type
IndicateswhetherDTCisaddinganewMessageor
updatinganexistingMessage.
l A:Add
l U:Update
11–19 9 Character IssueIdentifier The9-characterCUSIPnumber.
20-31 12 Character International
Identifier
The12-characterISIN(InternationalSecurities
IdentificationNumber)number.
32-34 3 Character StateofIssuance Thetwo-digitstatecodeformunicipalandcorporate
securitiesissuedintheUnitedStates,itsterritories
andCanadianprovinces.Thisfieldcontainsthestate
codeofissuanceformunicipalsecurities,andthe
statecodeofincorporationforcorporatesecurities.
ThevaluesarecontainedinISOUnitedStatesand
CanadianProvincesonpage 64.
35-37 3 Character Countryof
Issuance([[issuer]]
Countryof
Origin)
Thethree-digitISOcountrycode(fornon-United
Statesandterritorysecurities).Thevaluesare
containedinISOCountryCodesonpage 68.
Table6.3IssuerMessage-D01
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 23

---

## Page 24

Position Length Format FieldName Description
38-97 60 Character IssuerName ThefirstoccurrenceoftheformalIssuername
appearingontheProspectusorOfferingStatement
thatissuppliedtoDTCduringeligibilityprocessing.
Thisdescriptionprovidesaconsistentissuername
acrosstheissuanceandissues.TheIssueror
IssuingAgentmayalsoprovidethedescriptionifthe
securitydoesnotgothroughtheeligibilityprocess
(forexample,forMBSsecurities).
98-127 30 Character DTCShort
Description
Theabbreviatedsecuritydescriptiontraditionally
suppliedinDTCfiles.
128–134 7 Character Corresponding
BaseCUSIP
UndertheDTCMMIdiscountnumberingscheme
program,issuersrequestdualbase
CUSIPsfromtheCUSIPServiceBureau.Thebase
CUSIPsareassignedandusedbaseduponleap
yearandsubsequentevenandoddyears.
ThesebaseCUSIPnumbersallowtheIPAto
seamlesslyissueandprocesstransactions.The
CorrespondingBaseCUSIPistheoneassociated
withtheselectedsecurity.ApplicableforMMI
securitiesonly.
135–135 1 Character BaseCUSIP
CheckDigit
ThecheckdigitforthecurrentBaseCUSIP.
ApplicableforMMIsecuritiesonly
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 24

---

## Page 25

Position Length Format FieldName Description
136-136 1 Character SpanishTax
Withholding
Indicator
Indicateswhetherthesecurityissubjectto
SpanishTaxWithholdingregulations.
l Y:SubjecttoSpanishTaxWithholding
regulations.
Note:TolimitSpanishtaxwithholding,client
nameandcountryofresidencewillbe
disclosedtotheIssuer/SpanishGovt.[[DO]]
NOTPURCHASEIFYOUDONOT
CONSENT.
l N:Blank:NotApplicable,NotAvail-
ableUnderSpanishtaxregulation,
investorsinpreferredsecurities,
seniornotesorsubordinatednoteslis-
tedonanorganizedmarketinan
OECDcountry,withnotaxresidency
inSpainandnotactingthroughaper-
manentestablishmentinSpain,are
exemptfromtheSpanishNon-res-
identIncomeTax("NRIT"),provided
certaininformationobligationsrelat-
ingtoidentityandresidenceofbene-
ficialownersentitledtoreceive
distributionsarecompliedwith.If
theseinformationobligationsarenot
compliedwith,Spanishissuershave
towithholdtheNRIT.
137–300 164 Character Filler Reservedforfutureuse.
IssuanceMessage-D02
ThenexttabledescribestheIssuanceMessage,whichcontainsissuedate,currency,andissuance
amountinformation.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 25

---

## Page 26

Position Length Format FieldName Description
1–3 3 Character MessageType ThetypeofMessage.
ThevalueisD02
(Issuance).
4–9 6 Numeric Message
Sequence
Number
Identifiesthesequence
numberwithinthe
messagetype.Initialized
to000001.
10–10 1 Character MessageStatus
Type
IndicateswhetherDTCis
addinganew
messageorupdatingan
existingmessage.
l A:Add
l U:Update
11–19 9 Character IssueIdentifier The9-characterCUSIP
number.
20-31 12 Character International
Identifier(ISIN)
The12-characterISIN
(InternationalSecurities
IdentificationNumber)
number.
32–39 8 Character ExpectedIssue
Date
Currentlypopulatedwith
DatedDateThedate
whenthesecurityis
releasedorsold
l Forequity
securitiesin
CCYYMMDD
format.
l ForMMI-eli-
giblesecurities
theMessage
dateisequi-
valenttothe
issuedate.
Table6.4IssuanceMessage-D02
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 26

---

## Page 27

Position Length Format FieldName Description
40-42 3 Character Issuance
Currency
Thethree-characterISO
currencycodeofthe
certificate.Thevalues
arecontainedinISO
CurrencyCodeson
page 80.
43-45 3 Character Income
Currency
Thethree-characterISO
currencycodeinwhich
incomewouldbepaidfor
asecurity.Thevaluesare
containedinISO
CurrencyCodeson
page 80.
46-58 13 Numeric Original
Issuance
Amount
Theoriginaloffering
amountthatdoesnot
includetheoverallotment
ofsharesinthenew
issue.Thisamount
typicallyappliesto
municipalsandisalways
blankforMMIprograms.
Inwholenumberformat.
59-69 11 Numeric OfferingShares Thenumberofshares
initiallyissuedforthis
security;forequityissues
inwholenumberformat.
70-76 7 Numeric OfferingPrice Theoriginaloffering
shareprice;forequity
issuesin9(4)V9(3)
format.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 27

---

## Page 28

Position Length Format FieldName Description
77-77 1 Character IPOTracking
Indicator
Avaluethatindicates
whetheraleadmanager
requestedIPOtracking
forthissecurity.
l Y:Yes
l N:No
l Blank:No
Applicable/Not
Available
78-85 8 Numeric IPOStartDate ThestartdateoftheIPO
tracking,inCCYYMMDD
format.
86-86 1 Character DTCEligibility
Indicator-
obsoletefield,
notsupported
Avaluethatindicates
whetherthesecurityis
eligibleforDTC’s
services.
l Y:Yes
l N:No
l Blank:No
Applicable/Not
Available
87-94 8 Numeric Prospectus
Received
ThedatethatDTC
receivedaProspectusor
OfferingStatementfora
givensecurity.
Displayedin
CCYYMMDDformat.
95-103 9 Numeric Minimum
Denomination
Anumericminimum
denominationfortrading
(typicallythenumberof
sharesorbondsorthe
principalamount),in
wholenumberformat.
104-112 9 Numeric Multiple
Denomination
Anumericamountof
issuanceforuniquely
denominatedsecurities,
inwholenumberformat.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 28

---

## Page 29

Position Length Format FieldName Description
113-113 1 Character Issuance
Indicator
Indicateswhetherthe
issuanceisoriginalor
secondary. Thevalues
are:
l O:Original
l S:Secondary
l Blank:Not
Applicable/Not
Available
114-114 1 Character IssueStatus
Code
FirstPaymentIndicator
Possiblevalues:
l S:ShortFirst
Payment
l L:LongFirst
Payment
l Y:Yearly
l E: Payment
Omitted
l D:[[default]]
l X:ExtraLong
l P:Possible
[[default]]
l Space:First
Paymentis
Regular/not
applicable/not
available
115-300 186 Character Filler Reservedforfutureuse
IssueMessage-D03
ThenexttabledescribestheIssueMessage,whichcontainsspecificinformationabout:
l coupon
l maturity
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 29

---

## Page 30

l registration
l exchange
l issueamount
l amountoutstanding
Position Length Format FieldName Description
1-3 3 Character MessageType ThetypeofMessage.ThevalueisD03
(Issue).
4-9 6 Numeric MessageSequence
Number
Identifies thesequencenumberwithin
themessagetype.Initializedto000001.
10–10 1 Character MessageStatus
Type
IndicateswhetherDTCisaddinganew
messageorupdatinganexisting
message.
l A:Add
l U:Update
l M:Matured
11–19 9 Character IssueIdentifier The9-characterCUSIPnumber.
20-31 13 Character International
Identifier
The12-characterISIN(International
SecuritiesIdentificationNumber)
number.
32-44 13 Numeric Amount
Outstanding -
obsolete,defaulted
tozeroes
Thenumberofsecurities(eitherpar
amountorshares)thatDTC“Cede&Co”
islistedastheholderofrecord,inwhole
numberformat.Thisinformationislisted
inparamountforfixedincomesecurities
andsharesforequitysecurities.
45-51 7 Numeric Coupon/Interest
Rate
Thecouponorinterestrate.Thisfield
doesnotappearforequitysecurities.
Therateisin9(3)V9(6)format.Thefield 
iszero-filledfordiscountprogramMMI
securitiesandotherswithoutarate.For
variableratesecurities,thevalueis
indicatedasonecent.
Table6.5IssueMessage-D03
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 30

---

## Page 31

Position Length Format FieldName Description
52-59 8 Numeric MaturityDate ThematuritydateinCCYYMMDD
format.
60-67 8 Numeric DatedDate/ DatedDate-DatefromwhichInterest
startsaccruingfordebtinstrumentsin
CCYYMMDDformat:
68-68 1 Character RegistrationType Theregistrationtypeofasecurity.
l B: Bearer
l E,U,X:BookEntry
l A,D,I:Interchangeable
l M,R: FullyRegister
69-69 1 Character TaxableIndicator Avaluethatindicateswhetherthe
securityissubjecttofederalincome
taxes;formunicipalsecuritiesonly.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
70-70 1 Character Rule144AIndicator Avaluethatindicateswhetherasecurity
isissuedunderSEC Rule144Aasa
privateplacement.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
71-71 1 Character RegulationS
Indicator
Avaluethatindicateswhetherthe
securityissubjecttoRegulationSofthe
FederalReserveBoard.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 31

---

## Page 32

Position Length Format FieldName Description
72–72 1 Character Rule3c-7Indicator Avaluethatindicateswhetherasecurity
isrelyingontheexemptionfromSection
3(C.)(7)oftheInvestmentCompanyAct
of1940.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
73-80 8 Numeric FirstInterestPay
Date-defaultedto
zeroes
Thefirstinterestpaydateforafixed
incomesecurity,inCCYYMMDDformat.
81–90 10 Character TickerSymbol Anarrangementofcharacters(usually
letters)representingaparticularsecurity
listedonanexchangeorotherwise
tradedpublicly.OnlythePrimary
ExchangeTickerSymbolisdisplayed.
91-105 15 Character Exchange Theexchangeonwhichthesecurityyou
wantinformationaboutislisted.The
valuesare:
l AMEX:AmericanStock
Exchange
l [[NYSE]]:NewYorkStock
Exchange
l [[OTC]]:OvertheCounter
l [[NASDAQ]]:NationalAsso-
ciationofSecuritiesDealers
AutomatedQuote.
106-115 10 Character PoolID Theidentifierappliedtomortgage-
backedsecurities.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 32

---

## Page 33

Position Length Format FieldName Description
116-116 1 Character GlobalIssue Avaluethatindicateswhetherthe
securityusesforeignclearanceor
[[settlement]].
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
117-117 1 Character IssueType Identifiesthetypeofsecurity.Thevalues
are:
l 1:[[Equity]]
l 5: CorporateDebt
l 7:MunicipalDebt
118–120 3 Character Sub-IssueType Thetypeofissueorsub-issueusedby
DTCtoclassifyasecurity.Thevalues
arecontainedin.
AppendixI-DTCSub-IssueTypes.
121-121 1 Character PutIndicator Avaluethatindicateswhethertheissue
hasaputfeature.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
122-122 1 Character CallIndicator Avaluethatindicateswhethertheissue
issubjecttoacallredemption.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 33

---

## Page 34

Position Length Format FieldName Description
123-123 1 Character SinkingFund
Indicator
Avaluethatindicateswhetherasinking
fundprovisionappliestothissecurity.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
124-124 1 Character Prerefunded
Indicator
Avaluethatindicateswhetheranissue
hasfundsthathavebeenputasideto
redeemtheissueatitsearliestcalldate.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
125-125 1 Character Principal
Amortization
Indicator
Avaluethatindicateswhetherthe
principalissubjecttoamortization.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
126-126 1 Character IndexedPrincipal
Indicator(MMIs
Only)
Avaluethatindicateswhetherthe
interestpaymentsarelinkedtoanindex.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
127-127 1 Character RenewableNote
Indicator(MMIs
Only)
AvaluethatindicateswhetheraMTN
hasarenewablefeature.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 34

---

## Page 35

Position Length Format FieldName Description
128-128 1 Character InterestStep-up
Indicator(MMIs
Only)
Avaluethatindicateswhetherthe
securityhasaninterestratestep-up
feature.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
129-129 1 Character InterestReset
Indicator(MMIs
Only)
Avaluethatindicateswhetherthe
securityhasarateresetfeature.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
130-130 1 Character Changeable
PaymentIndicator
(MMIsOnly)
Avaluethatindicateswhetherthe
securitycanmodifythepaymentamount
ordate.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
131-143 13 Numeric IssueAmount Theamountissuedspecifictothis
security,inwholenumberformat.Oftena
subsetoftheOriginalIssuance.
144-144 1 Character ForeignOrdinary
ProcessingIndicator
Avaluethatindicateswhetherthe
securityiseligibleforforeignordinary
processing.
l Y:Yes
l N:No
l Blank:NotApplicable/Not
Available
145-146 2 Character MBSProductID DescribestheDifferentTypesofMBS
[[Bonds]].Forvalues,seeMBSProductID
Valuesonpage 90.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 35

---

## Page 36

Position Length Format FieldName Description
147-148 2 Character MBSCategoryID TheClassificationofthedifferentterms
thatapplytoMBSBonds.Forvalues,
seeMBSProductIDValuesonpage 90.
149-149 1 Character TaxCreditinLieuof
InterestIndicator
Thisfieldidentifieswhetherasecurityis
aBuildAmericaBondthathasaTax
Creditfeature.
l Y:Yes
l N:No
150-150 1 Character TaxCreditBond
Type
Thisfieldidentifiesthepaymentfeatures
associatedwithaTaxCreditsecurity
l 1: Comboforredemption
andtaxcredit.
l 2:Comboforredemption,
taxcreditandinterest.
l 3:Stripfortaxcredit.
l 4: stripforredemption
l 5:Stripforredemptionand
interest.
l 6: Stripforinterest
151-159 9 Numeric TaxCreditRate ThisfieldwillcontaintheactualTax
Creditrateforthesecurity.Thefirstthree
digitsrepresentdollars.Thelastsixdigits
inthefieldrepresentcents.
160-162 3 Numeric TaxCreditRecord
Date–Numberof
Days
Thisisthenumberofdaystherecord
dateisgoingtobeoffsetfromthe
paymentdate.
163-163 1 Character TaxCreditRecord
Date–Numberof
Days-
Business/Calendar
Indicator
ThisindicateswhethertheRecordDate
offsetisspecifiedasnumberofbusiness
orcalendardays.
l B: Business
l C:Calendar
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 36

---

## Page 37

Position Length Format FieldName Description
164-171 8 Character TaxCreditRecord
Date–FixedDate
Thisisthetwopre-establishedrecord
datesforthesecurity.
l Thefirstfourbytescontain
thefirstrecorddatewitha
formatMMDD
l Thelastfourbytescontain
thesecondrecorddatewith
thesameformatMMDD.
FormatMMDDMMDD
172-172 1 Character TaxCreditPayment
Frequency
Thisisthestatedfrequencyforpayments
forthesecurity.
l 1:Annual
l 2:Semi-annual
l 4:Quarterly,
l 8: Monthly
173-180 8 Character TaxCreditFirst
PaymentDate
Thisisthedatewhenthefirstinterest
paymentonthissecurityisdue.
FormatCCYYMMDD
181-181 1 Character StockforMaturity
Indicator
Thisfieldindicateswhetherabondhas
theoptiontopayMaturityproceedsas
StockinsteadofCash.
l Y:Yes
l N:No
182-182 1 Character ExtendedMaturity
Indicator
Thisfieldindicateswhetherabondhas
theoptionofextendingitsstatedMaturity
Date.
l Y:Yes
l N:No
183-183 1 Character SovereignDebt
Indicator
Thisfieldidentifiesabondasbeing
SovereignDebt,issuedbyanon-US
Sovereignentity.
l Y:Yes
l N:No
184–300 117 Character Filler Reservedforfutureuse.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 37

---

## Page 38

DescriptiveMessage-D05
ThenexttabledetailstheDescriptiveMessage,whichcontainsformalissuancedescriptioninformation
derivedfromDTC'seligibilityprocess.Thisdescriptioncomesfromtheprospectusorofferingfiling.In
somecases,thisdescriptionissuppliedtoDTCdirectlyfromcontributorssuchastheMMIsystem,and
thereforemaynotrepresentaformaldescription.
Position Length Format FieldName Description
1-3 3 Character Message
Type
ThetypeofMessage.ThevalueisD05
(Descriptive).
4-9 6 Numeric Message
Sequence
Number
Identifiesthesequencenumberwithinthe
messagetype.Initializedto000001.
10–10 1 Character Message
Status
Type
IndicateswhetherDTCisaddinganew
messageorupdatinganexisting
message.
l A:Add
l U:Update
11–19 9 Character [[issuer]]
Identifier
The9-characterCUSIPnumber.
20–31 12 Character International
Identifier
The12-characterISIN(International
SecuritiesIdentificationNumber)number.
32–91 60 Character Issue
Description
Thesecuritydescription,whichisthe
formalIssuernameappearingonthe
ProspectusorOfferingStatementthatis
suppliedtoDTCduringeligibility
processing.TheIssueror
IssuingAgentmayalsoprovidethe
descriptionifthesecuritydoesnotgo
throughtheeligibilityprocess(for
example,forMBS
[[securities]]).Thisfieldconsistsofthefirstof
thefourlines(60byteseach)of
information.
Table6.6DescriptiveMessage-D05
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 38

---

## Page 39

Position Length Format FieldName Description
92–271 180 Character Issue
Description
Thisfieldconsistsofthenextthreeofthe
fourlines(60byteseach)ofinformation.
272–300 29 Character Filler Reservedforfutureuse.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 39

---

## Page 40

DepositoryStatusMessage-D06
ThenexttabledescribestheDepositoryStatusMessage,whichcontainsDTCprocessingandstatus
informationforthesecurity.
Position Length Format FieldName Description
1–3 3 Character MessageType ThetypeofMessage.ThevalueisD06
(DepositoryStatus).
4–9 6 Numeric MessageSequence
Number
Identifiesthesequencenumberwithinthe
messagetype.Initializedto000001.
10–10 1 Character MessageStatus
Type
IndicateswhetherDTCisaddinganew
messageorupdatinganexistingmessage.
l A:Add
l U:Update
11–19 9 Character IssueIdentifier The9-characterCUSIPnumber.
20–31 12 Character International
Identifier
The12-characterISIN(InternationalSecurities
IdentificationNumber)number.
32–32 1 Character SameDayFund
SettlementEligibility
Indicator–obsolete
field,notsupported
Avaluethatindicateswhetherthesecurityis
eligibletosettleinsame-dayfunds.
l Y:Yes
l N:No
33–33 1 Character FASTCOD&WT FASTCOD&WT.Avaluethatindicatesifthe
issueiseligibleforDTC'sFASTCOD&WT(Full
[[FAST]])service.
l Y:Yes,FullFast
l N:No,NotFullFast
Table6.7DepositoryStatusMessage
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 40

---

## Page 41

Position Length Format FieldName Description
34–34 1 Character [[Dividend]]
Reinvestment
ServiceEligibility
Indicator
AvaluethatindicateswhethertheCUSIPis
eligibleforDTC'sDividendReinvestment
service.
l Y:Yes
l N:No
l Blank:NotApplicable/NotAvail-
able
35–35 1 Character CustodyService
EligibilityIndicator
AvaluethatindicateswhethertheCUSIPis
eligibleforDTC'sCustodyservice.
l Y:Yes
l N:No
l Blank:NotApplicable/NotAvail-
able
36–36 1 Character FederalBook-Entry
EligibilityIndicator
AvaluethatindicateswhethertheCUSIPisFed
Bookeligible.
l Y:Yes
l N:No
l Blank:NotApplicable/NotAvail-
able
37–37 1 Character DirectRegistration
EligibilityIndicator
AvaluethatindicateswhethertheCUSIPis
eligibleforDTC'sDirectRegistrationservice.
l Y:Yes
l N:No
l Blank:NotApplicable/NotAvail-
able
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 41

---

## Page 42

Position Length Format FieldName Description
38–38 1 Character Communications
IssueIndicator
Avaluethatindicateswhethertheissueisa
communicationsissue.
l Y:Yes
l N:No
l Blank:NotApplicable/NotAvail-
able
39–39 1 Character DepositActivity
ChillIndicator
Indicatesthatthissecurityislockedfromany
depositactivityatDTC.
l Y:Yes
l N:No
40–40 1 Character ChillCOD Indicatesthatthissecurityislockedfromany
COD(Certificateondemand)activityatDTC.
l Y:Yes
l N:No
41–41 1 Character ChillWT Indicatesthatthissecurityislockedfromany
WT(withdrawals-by-transfer)activityatDTC.
l Y:Yes
l N:No
42–42 1 Character ChillDO Indicatesthatthissecurityislockedfromany
[[DO]](DeliverOrder)activityatDTC.
l Y:Yes
l N:No
43–43 1 Character ChillSegregation Indicatesthatthissecurityislockedfromany
segregationactivityatDTC.
l Y:Yes
l N:No
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 42

---

## Page 43

Position Length Format FieldName Description
44–44 1 Character PledgeChillIndicator Indicatesthatthissecurityislockedfromany
pledgeactivityatDTC.
l Y:Yes
l N:No
45–45 1 Character ThinIssueIndicator Avaluethatindicateswhethertheissueisathin
issue.
l Y:Yes
l N:No
l Blank:NotApplicable/NotAvail-
able
46–65 20 Character Reserved Reservedforfutureuse.
66–66 1 Character FractionalDollars/
CentsEligible
IndicatesifthesecuritycancontainFractional
Share/amountcomponent.
l Y:Yes
l N:No
l Blank:NotApplicable/NotAvail-
able
Afractionalshareisaunitofstockthatisless
thanonefullshare.Forexample.,ifa
shareholderparticipatesinadividend
reinvestmentprogramandthedividendsbeing
reinvestedarenotenoughtopurchaseafull
shareatthemarketprice,theshareholderwill
becreditedwithafractionalshareuntilenough
dividendsaccruetopurchaseonefullshare.
67–67 1 Character Segregation100
NumberEligibility
Indicator
Avaluethatindicateswhethertheissueisa
segregated100issue.
l Y:Yes
l N:No
l Blank:NotApplicable/NotAvail-
able
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 43

---

## Page 44

Position Length Format FieldName Description
68–68 1 Character AutoCertification
EligibilityIndicator
Avaluethatindicateswhethertheissueis
eligibleforDTC'sautocertificationprogram.
l Y:Yes
l N:No
l Blank:NotApplicable/NotAvail-
able
69–69 1 Character Non-Transferable
Issue
Informationaboutthestatusofwhethera
securitycanbemovedortransferredbetween
participants.
70–70 1 Character RecordDate
Weekend/Holiday
Indicator
Indicatesthemethodbywhichtherecorddate
willbeadjustedifitfallsonaholidayor
weekend.
l B:Before
l A:After
l Blank:NotApplicable/NotAvail-
able
71–71 1 Character RecordDate
Business/Calendar
Indicator
IndicateswhethertheRecordDateoffsetis
specifiedasnumberofbusinessorcalendar
daysThevaluesare:
l B:Business
l C:Calendar
l Blank:NotApplicable/NotAvail-
able
72–119 48 Character DTCDescription
(Long)
The48-characterDTCissuedescription.
120-139 20 Character DTCDescription
(Short)
The20-characterDTCshortissuedescription,
typicallysystem-generated.
140-147 8 Character VaultLocation ThelocationofsecuritiesheldbyCede&Co.
148-150 3 Character CouponNumber ThenextCouponNumber(applicableforBearer
andInterchangeablecertificates).
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 44

---

## Page 45

Position Length Format FieldName Description
151-151 1 Character Networkingfor
EquitiesIndicator-
obsolete???
Indicateswhetherthesecurityiseligiblefor
[[DTCC]]'sNetworkingforEquitiesprogram.:
l N:SecurityisnoteligiblefortheNet-
workingforEquitiesprogram.
l Y:SecurityiseligiblefortheNet-
workingforEquitiesprogram.
152-152 1 Character FASTWT Avaluethatindicatesiftheissueiseligiblefor
[[DTC]]'sFASTWTserviceonly.
l Y:Yes
l N:No
153-153 1 Character BookEntryOnly
SecurityDRS
Eligibility Indicator
l 0:Securityiseligiblefor"WT"in
statementformonlyatDTC.Cer-
tificatesareavailableatthetransfer
agent.
l 1:Securityiseligiblefor"WT"in
statementformonly.
l 2:SecurityisDRSeligiblebutnot
participating.Certificatesonlyare
available.
Note:A“space”inthisfieldindicatesthatthe
issueisnotDRS-eligible.
154-154 1 Character Filler Reservedforfutureuse.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 45

---

## Page 46

Position Length Format FieldName Description
155-155 1 Character OARateTimelines
AttestationCode
l 1:ConformingCUSIP
l 2,3:NonconformingCUSIP
ThisfieldisapplicableonlyforSub-IssueType
‘540’CMOand‘541’[[ABS]]
Where:
Conformingmeansthatthissecurityis
structuredinawaythatmakesitlikelyforthe
finalratetobecalculatedanddisseminatedto
DTCpriortothepayabledate.
-and-
Non-conformingmeansthatthissecurityis
structuredinawaythatmakesitunlikelyforthe
finalratetobecalculatedand
disseminatedtoDTCpriortothepayabledate.
156-156 1 Character CNSEligibility
Indicator
Indicateswhetherasecurityiseligiblefor
ContinuousNetSettlement([[CNS]])through
[[NSCC]].
l Y:Yes
l N:No
157-157 1 Character OFACSanctioned
Indicator
IndicatesifsecurityisrestrictedduetoOFAC
sanctions.
l Y:Yes
l N:No
158-158 1 Character GlobalLockIndicator Thisfieldindicatesifthesecurityisfrozenand
globallylockedfromanyactivityatDTC.
l Y:Yes,theSecurityisglobally
locked.
l N:No,theSecurityisnotglobally
locked.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 46

---

## Page 47

Position Length Format FieldName Description
159-159 1 Character GlobalLockReason ThisfieldprovidesareasonfortheGlobalLock.
l Space:Securityisnotglobally
locked.Reasonisnotapplicable
l 0:[[DTCC]]-AppliedGlobalLock
l 1:[[DTCC]]-AppliedGlobalLock-Com-
plianceRelated.
l 2-9:Reservedforfutureuse.
160-207 48 Character UnitComponent
RatioTextBox
Specifiestheratioofunitstoeachofits
components.Applicableforsub-issuetypes
'780'EquityUnit’(EquityIssuetype)and
'781'DebtUnit’(CorporateBondIssuetype)
208-208 1 Character DepositChill
Reason
ThisfieldprovidesareasonfortheDeposit
Chill.
l Space: Securitydoesnothavea
DepositChill.Reasonisnot
applicable.
l 0:[[DTCC]]-AppliedDepositChill.
l 1:[[DTCC]]-AppliedDepositChill-
ComplianceRelated.
l 2-9::Reservedforfutureuse.
209-209 1 Character 871(m)TransactionIndicatesifthesecurityissubjectto
regulation871(m).
Validvalues:
l Y:yes
l N:No
l Space:Notapplicable/notavail-
able
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 47

---

## Page 48

Position Length Format FieldName Description
210-210 1 Character ContractType ContractTypefor871(m)Transaction.
Validvalues:
l S:Simple
l C:Complex
l Space:Notapplicable
211-217 7 Numeric Delta ThevalueofDeltaforSimpleContractType
(the“delta”ofaninstrumentisameasureof
therelationshipbetweenchangesinvalue
oftheinstrumentandchangesinvalueof
theunderlyingstock).
Format:9(1)V9(6)format,upto6decimal
points.
Validvalues:from0800000(0.8)to1000000
(1.0)[[default]]=zeroes
218-300 83 Character Filler Reservedforfutureuse.
AgentMessage-A01
ThenexttabledescribestheAgentMessage,whichidentifiestheagent(s)involvedwiththesecurity.The
agentidentifierisblankifanagentisnotapplicableforagivensecurity.
Position Length Format FieldName Description
1-3 3 Character MessageType ThetypeofMessage.Thevalueis
A01(Agent).
4–9 6 Numeric MessageSequence
Number
Identifies thesequencenumber
withinthemessagetype.Initialized
to000001.
Table6.8AgentMessage-A01
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 48

---

## Page 49

Position Length Format FieldName Description
10–10 1 Character MessageStatusType IndicateswhetherDTCisaddinga
newmessageorupdatingan
existingmessage.
l A:Add
l U: Update
11–19 9 Character IssueIdentifier The9-characterCUSIPnumber.
20–31 12 Character InternationalIdentifier The12-characterISIN(International
SecuritiesIdentificationNumber)
number.
32–39 8 Character DDAAgentID Theidentificationnumberofthe
DividendDisbursingAgentsthatare
registeredforthissecurity.
40–40 1 Character MMIIndicatorForPayingAgent IndicateswhetherthePayingAgent
isanMMIPayingAgent,andtheir
identificationnumberisactuallya
ParticipantID.Thevaluesare:
l Y:Yes
l N:No
l Blank:NotApplicable/
NotAvailable
41–48 8 Character PayingAgentID Theidentificationnumbersofthe
PayingAgentsthatareregistered
forthissecurity.
49–56 8 Character TransferAgentID Theidentificationnumbersofthe
TransferAgentsthatareregistered
forthissecurity.
57–64 8 Character RemarketingAgentID Theidentificationnumbersofthe
RemarketingAgentsthatare
registeredforthissecurity.The
RemarketingAgentIDisthesame
asaparticipantID.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 49

---

## Page 50

Position Length Format FieldName Description
65–72 8 Character RedemptionAgentID Theidentificationnumbersofthe
RedemptionAgentsthatare
registeredforthissecurity.
73–80 8 Character ConversionAgent
[[ID]]–obsolete,notpopulated
Theidentificationnumbersofthe
ConversionAgentsthatare
registeredforthissecurity.
81–88 8 Character InformationAgentID–obsolete,
notpopulated
Theidentificationnumbersofthe
InformationAgentsthatare
registeredforthissecurity.
89–96 8 Character ExchangeAgentID
–obsolete,notpopulated
Theidentificationnumbersofthe
ExchangeAgentsthatare
registeredforthissecurity.
97–104 8 Character TrusteeAgentID Theidentificationnumbersofthe
TrusteeAgentsthatareregistered
forthissecurity.
105–112 8 Character TenderAgentID Theidentificationnumbersofthe
TenderAgentsthatareregistered
forthissecurity.
113–113 1 Character MMIIndicatorForTheIssuing
Agent
IndicatorsthataresetbytheIssuing
Agent.Theyappearonlywhenthe
securityisanMMIandarerequired
becausetheAgentIDforMMIsis
actuallytheparticipantID.
114–121 8 Character IssuingAgent Thenamesandidentification
numbersoftheIssuingAgentsthat
areregisteredforthissecurity.The
Agentsaregroupedbyfunction.
122–129 8 Character DTCT/ADropAgentID Thenamesandidentification
numbersoftheDTCTransfer
Agentsthatareregisteredforthis
security.TheAgentsaregroupedby
function.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 50

---

## Page 51

Position Length Format FieldName Description
130–137 8 Character ExternalCustodianAgent Theidentificationnumbersofthe
ExternalCustodianAgentsthatare
registeredforthissecurity.
138–300 163 Character Filler Reservedforfutureuse.
AgentDescriptiveMessage-A02
ThenexttabledescribestheAgentDescriptiveMessage,whichcontainstheDTCAgentID,firmname,
andaddress.
Position Length Format FieldName Description
1–3 3 Character MessageType Identifiesthemessagetype.ThevalueisA02(Agent
DescriptiveMasterMessage).
4–9 6 Character Message
Sequence
Number
IdentifiestheactivitytypeoftheAgentsortedinthe
alphabeticalorder.Initializedto000001.
10–10 1 Character Message
Status
Type
IndicateswhetherDTCisaddinganew
messageorupdatinganexistingmessage.The
valuesare:
l A:Add
l U:Update
11–19 9 Character Filler Reservedforfutureuse.
20–31 12 Character Filler Reservedforfutureuse.
32–39 8 Character AgentID TheDTCidentificationnumberforanagent.
Table6.9AgentDescriptiveMessage-A02
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 51

---

## Page 52

Position Length Format FieldName Description
40–41 2 Character AgentType AgentType
l 1:TransferAgent
l 2:PayingAgent(non-MMIandMMI)
l 3:RedemptionAgent
l 4: DDA
l 5: Trustee
l 31:TenderAgent
l 32:RemarketingAgent
l 55: MMIIssuingAgent
42–89 48 Character AgentName Thefirmnamefortheagent
90–137 48 Character AgentAddress
1
Thestreetorsuiteaddressfortheagent.
138–185 48 Character AgentAddress
2
Thestreetorsuiteaddressfortheagent.
186–205 20 Character AgentCity Thecityfortheagent.
206–208 3 Character AgentState Thestateofoperationfortheagent.Formore
information,seeISOUnitedStatesandCanadian
Provinces..
209–211 3 Character AgentCountry CountryofoperationforAgent.Formore
information,seeISOCountryCodes..
212–220 9 Character AgentZip ThePostalZipcode.
221–229 9 Number ABANumber TheAmericanBankersAssociationNumber(if
applicable).
230–234 5 Number AgentPostal
Code
Thefive-digitPostalZipCode.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 52

---

## Page 53

Position Length Format FieldName Description
235-235 1 Character [[participant]]
AgentFlag
IndicateswhethertheagentIDisalsoaParticipant
IDinthecaseoftransferorMMIAgents.
l Y:Yes
l N:No
l Blank: No
236–300 65 Character Filler Reservedforfutureuse.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 53

---

## Page 54

LimitedEligibilityMessage–L01
ThenexttabledescribestheLimitedEligibilityMessage,whichonlyappearsintheLTDMSTfile.
Position Length Format FieldName Description
1-3 3 Character MessageType ThetypeofMessage.ThevalueisL01(LimitedElig).
4-9 6 Numeric Message
Sequence
Number
Identifiesthesequencenumberwithinthemessage
type.Initializedto000001.
10–10 1 Character Message
Status
Type
IndicateswhetherDTCisaddinganewmessageor
updatinganexistingmessage.Thevaluesare:
l A:Add
l U:Update
11–19 9 Character IssueIdentifier The9-characterCUSIPnumber.
20–31 12 Character International
Identifier
The12-characterISIN(InternationalSecurities
IdentificationNumber)number.
32–32 1 Character Limited
Eligibilityflag
Indicateswhetherornotthesecurityisa“Limited
Eligibility”Security.
l Y:Yes
l N:No
l Blank:N/Aornotavailable
33–35 3 Character Eligibility 
country1
Therecanbeuptofivecountriesofeligibility.The
three-digitISOcountrycode(fornon-UnitedStates
andterritorysecurities)asa3-charactercodewillbe
used.
Thevaluewillbespacesifnocountryisfound.
Table6.10LimitedEligibilityMessage–L01
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 54

---

## Page 55

Position Length Format FieldName Description
36–38 3 Character Eligibility 
country
2
Therecanbeuptofivecountriesofeligibility.
Thethree-digitISOcountrycode(fornon-United
Statesandterritorysecurities)asa3-charactercode
willbeused.
Thevaluewillbespacesifnocountryisfound.
39–41 3 Character Eligibility 
country3
Therecanbeuptofivecountriesofeligibility.The
three-digitISOcountrycode(fornon-UnitedStates
andterritorysecurities)asa3-charactercodewillbe
used.
Thevaluewill bespacesifnocountryisfound.
42–44 3 Character Eligibility 
country4
Therecanbeuptofivecountriesofeligibility.The
three-digitISOcountrycode(fornon-UnitedStates
andterritorysecurities)asa3-charactercodewillbe
used.
Thevaluewillbespacesifnocountryisfound.
45–47 3 Character Eligibility 
country
5
Therecanbeuptofivecountriesofeligibility.
Thethree-digitISOcountrycode(fornon-United
Statesandterritorysecurities)asa3charcodewill
beused.
Thevaluewillbespacesifnocountryisfound.
TrailerMessage-T01
ThenexttabledescribetheTrailerMessage,whichisthelastmessagethatisattachedtoeveryfiletype.
Position Length Format FieldName Description
1–3 3 Character MessageType Identifiesthemessagetype.ThevalueisT01
(TrailerMessage).
4–9 6 Character MessageSequence
Number
Identifiesthesequencenumberwithinthe
messagetype.Initializedto000001.
Table6.11TrailerMessage-T01
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 55

---

## Page 56

Position Length Format FieldName Description
10-17 8 Numeric TotalMessages Thetotalnumberofmessagesonthefile,
includingtheheader,detail,andtrailer
messagetypes.
18-300 283 Character Filler Reservedforfutureuse.
SecurityMasterFileData- PremiumMasterFileUser'sGuide
6.MessageFormats 56

---

## Page 57

A.DTCSUB-ISSUETYPES
Value Description
(blank) NotApplicable
000 NotApplicable
005 [[Equity]]
010 CommonStock
011 ConvertibleCommonStock
012 CommonStockREIT
020 PreferredStock
022 PreferredStockREIT
023 ConvertiblePreferredStock
024 TenderRatePreferredStock
030 LimitedPartnership
040 CMODenomin"Units"or"UndividedInterest"
041 ABSDenomin"Units"or"UndividedInterest"
042 IssueDenomin"Units"or"UndividedInterest"
102 AuctionRatePreferredStock(ARPS)
110 AmericanDepositaryReceipt([[ADR]])
111 DepositaryShare
112 MunicipalOptionCallRight
TableA.1DTCSub-IssueTypes
SecurityMasterFileData- PremiumMasterFileUser'sGuide
A.DTCSub-IssueTypes 57

---

## Page 58

Value Description
117 ExchangeTradedFunds([[ETF]])
120 MMIPreferredStock(inCP-likemode)
121 Equity144ADesignatedInvestors
125 SealedEnvelope
126 CustodyUserCUSIP
127 Non-StandardAssetUserCUSIPs
130 Real-EstateInvestmentTrust(REIT)
310 MunicipalBond
311 MunicipalNote
312 MunicipalAuctionRateNote(ARN)
313 MunicipalVariableModeObligation (VMO)
314 MunicipalVariableRateDemandObligation(VRDO)
315 MunicipalInsuredCustodialReceipt
320 MMIMunicipalVRDO/CP
330 MMIMunicipalCommercial Paper
340 Bearer,CallableZeroCouponBond
346 MunicipalOtherTaxExempt
450 GNMAREMIC
451 GNMAPassthrough
452 GNMASerialNote
500 CorporateBond(CB)orGlobalCorpBond(GCB)
SecurityMasterFileData- PremiumMasterFileUser'sGuide
A.DTCSub-IssueTypes 58

---

## Page 59

Value Description
502 MMIBankers'AcceptanceNote(BA)
504 MMIInstitutionalCertificatesofDeposit
505 CertificatedMoneyMarketInstrument
506 CertificatedMoneyMarket–PeriodicPayer
507 CertificatesofDeposit
510 CPIInterestatMaturity(IAM)CommercialPaper
511 PeriodicPaymentCommercialPaper
520 CPIDiscountCommercialPaper(CP)
525 MMICorporateCommercialPaper
526 MMICorporateVRDO/CP
530 MTNMediumTermNote
531 MMIDepositNote
532 MMIMedium-TermBankNote
533 MMIMediumTermNote
540 CollateralizedMtgeObligationorGlobalCMO
541 [[Asset]]-BackedSecurity([[ABS]])orGlobalABS(GABS)
542 Non-CMO/ABSAmortizingIssue
546 CorporateOtherTaxExempt
550 MMIShort-TermBankNote
551 ZCPNDenominInitialPrincipalAmt
560 MMIDiscountNote
SecurityMasterFileData- PremiumMasterFileUser'sGuide
A.DTCSub-IssueTypes 59

---

## Page 60

Value Description
571 CorporateAuctionRateNote
572 ConvertibleCorporateDebt
573 CorporateVariableModeObligation(CVMO)
574 CorporateShort-TermNote
575 CorporateDebenture
576 CorporateVRDO/MunicipalVRDO(MMD)
577 CorporateInsuredCustodialReceipt
578 TenderRateNote
579 ZeroCouponBond
601 GovernmentSecurity
602 GovernmentTrustCertificate
603 JunkandTreasuryGrowthReceipt(JGR)
610 USTreasurySecurity
611 USTreasuryBill
612 USTreasuryNote
613 USTreasuryBond
620 USGovernmentAgencySecurity
700 Package
704 CorporateDebtDerivative
705 EquityDerivative
706 MunicipalDerivative
SecurityMasterFileData- PremiumMasterFileUser'sGuide
A.DTCSub-IssueTypes 60

---

## Page 61

Value Description
708 MunicipalAmortizedIssue
710 OptionDerivative
720 Warrant
730 Right
760 MutualFund
761 ClosedEndFund
762 (IMMI)InstitutionalMMIMutualFundShares
780 EquityUnit
781 DebtUnit
790 UnitInvestmentTrust([[UIT]])-NuveenOnly)
791 GlobalUnitTrust
795 UnitInvestmentTrust([[UIT]])
SecurityMasterFileData- PremiumMasterFileUser'sGuide
A.DTCSub-IssueTypes 61

---

## Page 62

B.DTCSECURITYCLASSIFICATION
TableB.1containsthesecurityclassifications,theissuetypes,andthesub-issuetypeswithineach
securityclassification.
Security
Classification
Ifthesecur-
ityhasIssue
typeof...
Andhasasub-issue
typeof...
UpdateFileNameMasterFileName
[[Equity]] 1 005,010,011,012,020,
022,023,024,030,042,
102,110,111,121,125,
126,127,507,700,
704,705,710,720,730,
762,780
EQTCUP EQTMST
Funds/Trusts 1 117,130,760,761,762,
781,790,791,795
CRPCUP CRPMST
Corporate
Fixed
Income
5 126,127,340,500,542,
571,572,573,574,575,
576,577,578, 579,
704, 781
CRPCUP CRPMST
Government
[[securities]]
5 601,602,603,610,611,
612,613,620
GOVCUP GOVMST
MoneyMarket
Instruments
5 120,320,330,502,504,
505,506,507,510,511,
520,525,526,530,531,
532,533,550,560
MMICUP MMIMST
Mortgage
Backed
MBS
5 450,451,452,650,651,
652
AMBCUP AMBMST
TableB.1DTCSecurityClassification
SecurityMasterFileData- PremiumMasterFileUser'sGuide
B.DTCSecurityClassification 62

---

## Page 63

Security
Classification
Ifthesecur-
ityhasIssue
typeof...
Andhasasub-issue
typeof...
UpdateFileNameMasterFileName
AssetBacked
([[ABS]])/
Collateralized
Mortgage
[[obligations]]
(CMO)
5 040,041,540,541,551 AMBCUP AMBMST
Municipal
[[securities]]
7 310,311,312,313,314,
315,346,576,706,708
MUNCUP MUNMST
TableB.1DTCSecurityClassification(continued)
SecurityMasterFileData- PremiumMasterFileUser'sGuide
B.DTCSecurityClassification 63

---

## Page 64

C.ISOUNITEDSTATESANDCANADIAN
PROVINCES
State/ProvinceName State/ProvinceCode CountryCode
ALBERTA AB CA
ALASKA AK US
ALABAMA AL US
ARKANSAS AR US
AMERICANSAMOA AS US
ARIZONA AZ US
BRITISHCOLUMBIA BC CA
CALIFORNIA CA US
COLORADO CO US
CONNECTICUT CT US
DISTRICTOFCOLUMBIA DC US
DELAWARE DE US
FLORIDA FL US
FEDERATEDSTATESOF
MICRONESIA
FM US
GEORGIA GA US
GUAM GU US
HAWAII HI US
TableC.1ISOUnitedStatesandCanadianProvinces
SecurityMasterFileData- PremiumMasterFileUser'sGuide
C.ISOUnitedStatesAndCanadianProvinces 64

---

## Page 65

State/ProvinceName State/ProvinceCode CountryCode
IOWA IA US
IDAHO [[ID]] US
ILLINOIS IL US
INDIANA IN US
KANSAS KS US
KENTUCKY KY US
LOUISIANA LA US
LABRADOR LB CA
MASSACHUSETTS MA US
MANITOBA MB CA
MARYLAND MD US
MAINE ME US
MARSHALLISLANDS MH US
MICHIGAN MI US
MINNESOTA MN US
MISSOURI MO US
NORTHERN MARIANAISLANDS MP US
MISSISSIPPI MS US
MONTANA MT US
NEWBRUNSWICK NB CA
NORTHCAROLINA NC US
SecurityMasterFileData- PremiumMasterFileUser'sGuide
C.ISOUnitedStatesAndCanadianProvinces 65

---

## Page 66

State/ProvinceName State/ProvinceCode CountryCode
NORTHDAKOTA ND US
NEBRASKA NE US
NEWFOUNDLAND NF CA
NEWHAMPSHIRE NH US
NEWJERSEY NJ US
NEWMEXICO NM US
NOVASCOTIA NS CA
NORTHWEST TERRITORIES NT CA
NEVADA NV US
NEWYORK NY US
OHIO OH US
OKLAHOMA OK US
ONTARIO ON CA
OREGON OR US
PENNSYLVANIA PA US
PRINCEEDWARDISLAND PE CA
QUEBEC PQ CA
PUERTORICO PR US
PALAU PW US
RHODEISLAND RI US
SOUTHCAROLINA SC US
SecurityMasterFileData- PremiumMasterFileUser'sGuide
C.ISOUnitedStatesAndCanadianProvinces 66

---

## Page 67

State/ProvinceName State/ProvinceCode CountryCode
SOUTHDAKOTA SD US
SASKATCHEWAN SK CA
TENNESSEE TN US
TEXAS TX US
UTAH UT US
VIRGINIA VA US
VIRGINISLANDS VI US
VERMONT VT US
WASHINGTON WA US
WISCONSIN WI US
WESTVIRGINIA WV US
WYOMING WY US
YUKONTERRITORY YT CA
SecurityMasterFileData- PremiumMasterFileUser'sGuide
C.ISOUnitedStatesAndCanadianProvinces 67

---

## Page 68

D.ISOCOUNTRYCODES
Two-DigitCountryCode Three-DigitCountryCode Description
AD AND ANDORRA
AE ARE U.A.E.
AF AFG AFGHANISTAN
AG N/A ANTIGUAANDBARBUDA
AI N/A ANGUILLA
AL ALB ALBANIA
AM N/A ARMENIA
AN ANT NETH.ANTILLES
AO AGO ANGOLA
AQ N/A ANTARTICA
AR ARG ARGENTINA
AS ASM AMERICANSAMOA
AT AUT AUSTRIA
AU AUS AUSTRALIA
AW N/A ARUBA
AZ N/A AZERBAIJAN
BA N/A BOSNIA-HERZEGOVINA
BB BRB BARBADOS
TableD.1ISOCountryCodes
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 68

---

## Page 69

Two-DigitCountryCode Three-DigitCountryCode Description
BD BGD BANGLADESH
BE BEL BELGIUM
BF N/A BURKINAFASO
BG BGR BULGARIA
BH BHR BAHRAIN
BI BDI BURUNDI
BJ BEN BENIN
BM BMU BERMUDA
BN BRN BRUNEI DARUSSALAM
BO BOL BOLIVIA
BR BRA BRAZIL
BS BHS BAHAMAS
BT BTN BHUTAN
BV N/A BOUVET ISLAND
BW BWA BOTSWANA
BY BYS BELARUS
BZ BLZ BELIZE
CA CAN CANADA
CC CCK COCOS(KEELING) ISLANDS
CF CAF CENTRALAFRICANREPUBLIC
CG COG CONGO
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 69

---

## Page 70

Two-DigitCountryCode Three-DigitCountryCode Description
CH CHE SWITZERLAND
CI CIV COTED'IVOIRE
CK COK COOKISLANDS
CL CHL CHILE
CM CMR CAMEROON
CN CHN CHINA
CO COL COLOMBIA
CR CRI COSTARICA
CS CSK CZECHOSLOVAKIA
CU CUB CUBA
CV CPV CAPEVERDE
CX CXR CHRISTMASISLAND
CY CYP CYPRUS
CZ N/A CZECHREPUBLIC
DE DEU GERMANY
DJ DJI DJIBOUTI
DK DNK DENMARK
DM DMA DOMINICA
[[DO]] DOM DOMINICANREPUBLIC
DZ DZA ALGERIA
EC ECU ECUADOR
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 70

---

## Page 71

Two-DigitCountryCode Three-DigitCountryCode Description
EE N/A ESTONIA
EG EGY EGYPT
EH ESH WESTERNSAHARA
ES ESP SPAIN
ET ETH ETHIOPIA
FI FIN FINLAND
FJ FJI FIJI
FK FLK FALKLANDISLANDS(MALVINAS)
FM N/A MICRONESIA
FO [[FRO]] FAEROEISLANDS
FR FRA FRANCE
GA GAB GABON
GB GBR UNITEDKINGDOM
GD GRD GRENADA
GE N/A GEORGIA
GF GUF FRENCH  GUIANA
GG N/A GUERNSEY, C.I.
GH GHA GHANA
GI GIB GIBRALTAR
GL GRL GREENLAND
GM GMB GAMBIA
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 71

---

## Page 72

Two-DigitCountryCode Three-DigitCountryCode Description
GN GIN GUINEA
GP GLP GUADELOUPE
GQ GNQ EQUATORIAL GUINEA
GR GRC GREECE
GT GTM GUATEMALA
GU GUM GUAM
GW GNB GUINEA-BISSAU
GY GUY GUYANA
HK HKG HONGKONG
HM N/A HEARDANDMCDONALDISLANDS
HN HND HONDURAS
HR N/A CROATIA
HT HTI HAITI
HU HUN HUNGARY
HV HVO UPPERVOLTA
[[ID]] IDN INDONESIA
IE IRL IRELAND
IL ISR ISRAEL
IM N/A ISLEOFMAN
IN IND INDIA
IO IOT BRITISHINDIANOCEANTERRITORY
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 72

---

## Page 73

Two-DigitCountryCode Three-DigitCountryCode Description
IQ IRQ IRAQ
IR IRN IRAN(ISLAMICREPUBLICOF)
IS ISL ICELAND
IT ITA ITALY
JE N/A JERSEY,C.I.
JM JAM JAMAICA
JO JOR JORDAN
JP JPN JAPAN
JT JTN JOHNSTONISLANDS
KE KEN KENYA
KG N/A KYRGYZSTAN
KH KHM CAMBODIA
KI KIR KIRIBATI
KM COM COMOROS
KN N/A SAINTKITTSANDNEVIS
KP PRK KOREA,DEMOCRATICPEOPLE'SREP.OF
KR KOR KOREA,REPUBLICOF
KW KWT KUWAIT
KY CYM CAYMANISLANDS
KZ N/A KAZAKHSTAN
LA LAO LAOPEOPLE'S DEMOCRATICREPUBLIC
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 73

---

## Page 74

Two-DigitCountryCode Three-DigitCountryCode Description
LB LBN LEBANON
LC LCA SAINTLUCIA
LI LIE LIECHTENSTEIN
LK LKA SRILANKA
LR LBR LIBERIA
LS LSO LESOTHO
LT N/A LITHUANIA
LU LUX LUXEMBOURG
LV N/A LATVIA
LY LBY LIBYAN ARABJAMAHIRIYA
MA MAR MOROCCO
MC MCO MONACO
MD N/A MOLDOVA,REPUBLIC OF
MG MDG MADAGASCAR
MH N/A MARSHALLISLANDS
ML MLI MALI
MM N/A MYANMAR
MN MNG MONGOLIA
MO MAC MACAU
MP N/A NORTHERN MARIANAISLANDS
MQ MTQ MARTINIQUE
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 74

---

## Page 75

Two-DigitCountryCode Three-DigitCountryCode Description
MR MRT MAURITANIA
MS N/A MONTSERRAT
MT MLT MALTA
MU MUS MAURITIUS
MV MDV MALDIVES
MW MWI MALAWI
MX MEX MEXICO
MY MYS MALAYSIA
MZ MOZ MOZAMBIQUE
NA NAM NAMIBIA
NC NCL NEWCALEDONIA
NE N/A NIGER
NF NFK NORFOLK ISLAND
NG NGA NIGERIA
NI NIC NICARAGUA
NL NLD NETHERLANDS
NO NOR NORWAY
NP NPL NEPAL
NR NRU NAURU
NT N/A NEUTRALZONE(BETWEENSAUDIAND
IRAQ)
NU NIU NIUE
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 75

---

## Page 76

Two-DigitCountryCode Three-DigitCountryCode Description
NZ NZL NEWZEALAND
OM OMN OMAN
PA PAN PANAMA
PE PER PERU
PF PYF FRENCH POLYNESIA
PG PNG PAPUANEWGUINEA
PH PHL PHILIPPINES
PK PAK PAKISTAN
PL POL POLAND
PM SPM ST.PIERREANDMIQUELON
PN PCN PITCAIRNISLAND
PR PRI PUERTORICO
PT PRT PORTUGAL
PW N/A PALAU
PY PRY PARAGUAY
PZ N/A PANAMACANALZONE
QA QAT QATAR
RE REU REUNION
RO ROM ROMANIA
RU N/A RUSSIA
RW RWA RWANDA
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 76

---

## Page 77

Two-DigitCountryCode Three-DigitCountryCode Description
SA SAU SAUDI ARABIA
SB SLB SOLOMONISLANDS
SC SYC SEYCHELLES
SD SDN SUDAN
SE SWE SWEDEN
SG SGP SINGAPORE
SH SHN ST.HELENA
SI N/A SLOVENIA
SJ SJM SVALBARDANDJANMAYENISLANDS
SK N/A SLOVAKIA
SL SLE SIERRALEONE
SM SMR SANMARINO
SN SEN SENEGAL
SO SOM SOMALIA
SR SUR SURINAME
ST STP SAOTOMEANDPRINCIPE
SU SUN UNIONOFSOVIETSOCIALIST REPUBLICS
SV SLV ELSALVADOR
SY SYR SYRIANARABREPUBLIC
SZ SWZ SWAZILAND
TC TCA TURKSANDCAICOSISLANDS
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 77

---

## Page 78

Two-DigitCountryCode Three-DigitCountryCode Description
TD TCD CHAD
TF N/A FRENCH  SOUTHERN  TERRITORIES
TG TGO TOGO
TH THA THAILAND
TJ N/A TAJIKISTAN
TK TKL TOKELAU
TM N/A TURKMENISTAN
TN TNN TUNISIA
TO TON TONGA
TP TMP EASTTIMOR
TR TUR TURKEY
TT TTO TRINIDADANDTOBAGO
TV TUV TUVALU
TW N/A TAIWAN
TZ TZA TANZANIA,UNITEDREPUBLICOF
UA UKR UKRAINE
UG UGA UGANDA
UM N/A UNITEDSTATESMINOROUTLYING
ISLANDS
US USA UNITEDSTATES
UY URY URUGUAY
UZ N/A UZBEKISTAN
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 78

---

## Page 79

Two-DigitCountryCode Three-DigitCountryCode Description
VA VAT VATICANCITYSTATE
VC VCT SAINTVINCENT ANDTHEGRENADINES
VE VEN VENEZUELA
VG VGB VIRGINISLANDS(BRITISH)
VI VIR VIRGINISLANDS,U.S.
VN VNM VIETNAM
VU VUT VANUATU
WF WLF WALLISANDFUTUNAISLANDS
WS WSM SAMOA
YE YEM YEMEN,REPUBLICOF
YU YUG YUGOSLAVIA
ZA ZAF SOUTHAFRICA
ZM ZMB ZAMBIA
ZR ZAR ZAIRE
ZW ZWE ZIMBABWE
XS N/A CEDELEUROCLEAR
SecurityMasterFileData- PremiumMasterFileUser'sGuide
D.ISOCountryCodes 79

---

## Page 80

E.ISOCURRENCYCODES
Code Description
ADP ANDORRANPESETA
AED UAEDIRHAM
AFA AFGHANI
ALL LEK
ANG NETHERLANDS ANTILLEAN GUILDER
AON NEWKWANZA
ARS ARGENTINE PESO
[[ATS]] SHILLING
AUD AUSTRALIANDOLLAR
AWG ARUBANGUILDER
BBD BARBADOSDOLLAR
BDT TAKA
BEF BELGIANFRANC
BGL LEV
BHD BAHRAINIDINAR
BIF BURUNDI FRANC
BMD BERMUDIAN DOLLAR
BND BRUNEI DOLLAR
TableE.1ISOCurrencyCodes
SecurityMasterFileData- PremiumMasterFileUser'sGuide
E.ISOCurrencyCodes 80

---

## Page 81

Code Description
BOB BOLIVIANO
BRL BRAZILIANREAL
BSD BAHAMIANDOLLAR
BTN NGULTRUM
BWP PULA
BYB BELARUSSIANRUBLE
BZD BELIZEDOLLAR
CAD CANADIANDOLLAR
CHF SWISSFRANC
CLF UNIDADES DEFORMENTO
CLP CHILEANPESO
CNY YUANRENMINBI
COP COLOMBIAN PESO
CRC COSTARICANCOLON
CUP CUBANPESO
CVE CAPEVERDEESCUDO
CYP CYPRUSPOUND
CZK CZECHKORUNA
DEM DEUTSCHEMARK
DJF DJIBOUTIFRANC
DKK DANISHKRONE
SecurityMasterFileData- PremiumMasterFileUser'sGuide
E.ISOCurrencyCodes 81

---

## Page 82

Code Description
DOP DOMINICANPESO
DZD ALGERIANDINAR
ECS SUCRE
EEK KROON
EGP EGYPTIANPOUND
ESP SPANISHPESETA
ETB ETHIOPIANBIRR
EUR EURODOLLAR
FIM MARKKA
FJD FIJIDOLLAR
FKP FALKLANDISLANDSPOUND
FRF FRENCHFRANC
GBP POUNDSTERLING
GEK GEORGIANCOUPON
GHC CEDI
GIP GIBRALTAR POUND
GMD DALASI
GNF GUINEAFRANC
GRD DRACHMA
GTQ QUETZAL
GWP GUINEA-BISSAU PESO
SecurityMasterFileData- PremiumMasterFileUser'sGuide
E.ISOCurrencyCodes 82

---

## Page 83

Code Description
GYD GUYANA DOLLAR
HKD HONGKONGDOLLAR
HNL LEMPIRA
HRD CROATIANDINAR
HRK KUNA
HTG GOURDE
HUF FORINT
IDR RUPIAH
IEP IRISHPOUND
ILS SHEKEL
INR INDIANRUPEE
IQD IRAQIDINAR
IRR IRANIANRIAL
ISK ICELAND  KRONA
ITL ITALIANLIRA
JMD JAMAICANDOLLAR
JOD JORDANIANDINAR
JPY YEN
KES KENYAN SHILLING
KGS SOM
KHR RIEL
SecurityMasterFileData- PremiumMasterFileUser'sGuide
E.ISOCurrencyCodes 83

---

## Page 84

Code Description
KMF COMOROFRANC
KPW NORTHKOREANWON
KRW WON
KWD KUWAITIDINAR
KYD CAYMANISLANDSDOLLAR
KZT TENGE
LAK KIP
LBP LEBANESEPOUND
LKR SRILANKARUPEE
LRD LIBERIANDOLLAR
LSL LOTI
LTL LITHUANIANLITAS
LTT TALONAS
LUF LUXEMBOURG FRANC
LVL LATVIANLATS
LVR LATVIANRUBLE
LYD LIBYANDINAR
MAD MOROCCANDIRHAM
MDL MOLDOVANLEU
MGF MALAGASYFRANC
MKD DENAR
SecurityMasterFileData- PremiumMasterFileUser'sGuide
E.ISOCurrencyCodes 84

---

## Page 85

Code Description
MMK KYAT
MNT TUGRIK
MOP PATACA
MRO OUGUIYA
MTL MALTESELIRA
MUR MAURITIUSRUPEE
MVR RUFIYAA
MWK KWACHA
MXN MEXICANNUEVOPESO
MYR MALAYSIANRINGGIT
MZM METICAL
NAD NAMIBIADOLLAR
NGN NAIRA
NIO CORDOBA ORO
NLG NETHERLANDS GUILDER
NOK NORWEGIAN KRONE
NPR NEPALESERUPEE
NZD NEWZEALANDDOLLAR
OMR RIALOMANI
PAB BALBOA
PEN NUEVOSOL
SecurityMasterFileData- PremiumMasterFileUser'sGuide
E.ISOCurrencyCodes 85

---

## Page 86

Code Description
PGK KINA
PHP PHILIPPINEPESO
PKR PAKISTANRUPEE
PLN POLISHZLOTKY
PLZ ZLOTY
PTE PORTUGUESE ESCUDO
PYG GUARANI
QAR QATARIRIAL
ROL LEU
RUR RUSSIANRUBLE
RWF RWANDAFRANC
SAR SAUDIRIYAL
SBD SOLOMONISLANDSDOLLAR
SCR SEYCHELLES RUPEE
SDD SUDANESEDINAR
SEK SWEDISHKRONA
SGD SINGAPOREDOLLAR
SHP ST.HELENAPOUND
SIT TOLAR
SKK SLOVAKKORUNA
SLL LEONE
SecurityMasterFileData- PremiumMasterFileUser'sGuide
E.ISOCurrencyCodes 86

---

## Page 87

Code Description
SOS SOMALISHILLING
SRG SURINAMGUILDER
STD DOBRA
SVC ELSALVADORCOLON
SYP SYRIANPOUND
SZL LILANGENI
THB BAHT
TMM MANAT
TND TUNISIANDINAR
TOP PA'ANGA
TPE TIMORESCUDO
TRL TURKISHLIRA
TTD TRINIDADANDTOBAGODOLLAR
TWD NEWTAIWANDOLLAR
TZS TANZANIANSHILLING
UAK KARBOVANET
UGX UGANDASHILLING
USD USDOLLAR
USN USDOLLAR,NEXTDAYFUNDS
UYU PESOURUGUAYO
UZS UZBEKISTAN SUM
SecurityMasterFileData- PremiumMasterFileUser'sGuide
E.ISOCurrencyCodes 87

---

## Page 88

Code Description
VEB BOLIVAR
VND DONG
VUV VATU
WST TALA
XAF CFAFRANC BEAC
XAG SILVER
XAU GOLD
XBA EUROPEANCOMPOSITEUNIT(EURCO)
XBB EUROPEANMONETARYUNIT(EMU-6)
XBC EUROPEANUNITOFACCOUNT-9(EU)
XBD EUROPEANUNITOFACCOUNT-17 (E)
XCD EASTCARIBBEANDOLLAR
XDR SDRINT'LMONETARYFUND(I.M.F)
XEU EUROPEANCURRENCYUNIT(ECU)
XFO GOLD-FRANC (SPECIALSETTLEMENT)
XFU UIC-FRANC(SPECIALSETTLEMENT)
XOF CFAFRANCBCEAO
XPD PALLADIUM
XPF CFPFRANC
XPT PLATINUM
XXX TRANSACTIONS WITHOUTCURRENCY
SecurityMasterFileData- PremiumMasterFileUser'sGuide
E.ISOCurrencyCodes 88

---

## Page 89

Code Description
YER YEMENIRIAL
YUN YUGOSLAVIAN DINAR
ZAL FINANCIALRAND
ZAR RAND
ZMK KWACHA
ZRN NEWZAIRE
ZWD ZIMBABWEDOLLAR
SecurityMasterFileData- PremiumMasterFileUser'sGuide
E.ISOCurrencyCodes 89

---

## Page 90

F.MBSPRODUCTIDVALUES
ProductIDvaluesdescribedinTableF.1areinSIM.TBSIM45_PRODUCT.
Code MBSAgencyShortName MBSAgencyDescription
AR FHLMC FHLMCREMICAR
CR FHLMC CRIIMIMAE
DR FHLMC FHLMCGIANT
D2 FHLMC FHLMCIIGIANT
FG FHLMC FHLMCGOLDPC
FM FHLMC FHLMCPC
FN FNMA FEDERALNATLMORTAGEASSN
GR GNMA GNMAREMIC
G1 GNMA GNMAI
G2 GNMA GNMAII
HR FHLMCF HLMCREMIC
K2 FNMA FNMAIIREMIC
L2 FHLMC FHLMCGIIREMIC
M2 GNMA GNIIREMIC/FNMAREMICCOLL
NR FNMA FNMAIREMIC
P1 GNMA GNMAIPLATINUM
P2 GNMA GNMAIIPLATINUM
TableF.1MBSProductIDValues
SecurityMasterFileData- PremiumMasterFileUser'sGuide
F.MBSProductIDValues 90

---

## Page 91

Code MBSAgencyShortName MBSAgencyDescription
QR GNMA GNMAREREMIC18THPAYOR
RM GNMA GNMAREREMIC25THPAYOR
RR GNMA GNMAIREREMIC
R2 GNMA GNMAIIREMIC
SR GMRM1 GINNIEMAEMORTGAGEREMIC
UR GNMA GNMAREREMIC25THPAYOR
VR VA VAREMIC
RT GNMA GNMAREMIC27THPAYOR
SecurityMasterFileData- PremiumMasterFileUser'sGuide
F.MBSProductIDValues 91

---

## Page 92

©2023.Allrightsreserved.[[DTCC]],[[DTCC]](Stylized)andFinancialMarkets.Forward.areregisteredandunregisteredtrademarks
ofTheDepositoryTrust&ClearingCorporationDTCC.Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandname
bycertainaffiliatesofTheDepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitselfdoesnotprovidesuchservices.Eachof
theseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsoftheparticularcountryorcountriesinwhichsuch
entityoperates.Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,itsaffiliatesandtheservicestheyoffer.
DocDate:October17,2023
PublicationCode:DAT315
Service:SecurityMasterFileData
Title:PremiumMasterFileUser'sGuide
ForMoreInformation
EmailDTCCLearningat:
DTCCLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com