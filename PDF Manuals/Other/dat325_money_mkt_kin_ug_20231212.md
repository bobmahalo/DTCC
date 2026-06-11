---
title: "DTCC Money Market Kinetics User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat325_money_mkt_kin_ug_20231212.pdf"
pages: 20
size: "291.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# DTCC Money Market Kinetics User Guide

**Original File:** [dat325_money_mkt_kin_ug_20231212.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat325_money_mkt_kin_ug_20231212.pdf)  
**Category:** Other  
**Total Pages:** 20  
**File Size:** 291.7 KB  

---

## Page 1

MoneyMarketKinetics
USERGUIDE
DECEMBER12,2023

---

## Page 2

TABLEOFCONTENTS
Overview 3
FrequentlyAskedQuestions 4
FieldSpecifications 5
FileDeliverySchedule 12
CUSIPDescriptionBreakdown 13
ShortDescriptionFormatting 13
ShortDescription 13
SectorCodes 17
ReferenceEquityCUSIPMappingLogic 18
SampleData 19

---

## Page 3

OVERVIEW
TheDTCCMoneyMarketKineticsofferingprovidesasingle,dailyfeedofanonymizedCPandCD
secondarysettlementtransactionsdata—excludingprimaryIPAtodealer—toenhanceanalysisofthis
enormousmarket.
DTCCMoneyMarketKineticsUserGuide
Overview 3

---

## Page 4

FREQUENTLYASKEDQUESTIONS
1. WhydosomeEquityCUSIPfieldscontainthevalue999999999?
999999999representsunknownvalues.
2. Whydoesthelastrowineachfilecontainsomethinglike“Hub*TRL0000002691”?
Thisrowisatrailerrecordthatcontainstherowcountineachfile.
3. Commercialpaperhasatypical270-daylifespan.WhatarethecommercialpaperCUSIPs
withdurationsgreaterthan270days?
DTCCdoesnothaveaspecificruleregardingCPmaturitydurationstheyareissuer-provided.
[[DTCC]] cannotaddressthereasonswhysomeissuerschoosetocallsecuritieswithdurationslonger
than270daysCP.
4. GiventhatDTCConlysettlesinMAX lotsof50million,whatarethesettlementamountsthat
aregreater?
Transactionsthataregreaterthan50millionrepresentMaturityPresentments.Thesetransactions
areprocessedasadeliver-order;althoughtheyareincludedintheMoneyMarketKineticsreport,
theycanbeignored.
5. Whichfieldsareusedtovalidatesettlementbyparticipants?
Nospecificfieldsarematched.Therearetwoparties:onepresentsthesettlementandthesecond
(the"receiver")approvestheactivity,butnotataspecificfieldlevel.
6. CanIPAsissueadditionalpaperunderanexistingCPProgram?
Yes.IPAscanaddadditionalissuancetoanexistingCUSIPpriortotheCUSIP'smaturity.
7. Whydoesthe"InterestRate"intheoutputnotchangethroughoutthelifeofanMMICUSIP?
DTCCusestheissuancerangeasprovidedbytheissuer([[IPA]])whentheMMIfirstbecomesDTC-
eligible.ThisrateissourcedfromtheDTCSecurityMasterFile.DTCdoesnotreceivethetraded
rateforsecondarymarkettransactions.ThetradedrateisnotarequiredmatchingfieldforDTC
[[settlement]].
DTCCMoneyMarketKineticsUserGuide
FrequentlyAskedQuestions 4

---

## Page 5

FIELDSPECIFICATIONS
Thenexttabledocumentsthefieldsinthefile,alongwiththeirdatatypes.
HeaderText Type Description
[[CUSIP]] Alphanumeric(9) Aunique9-characteralphanumeric
identifierassignedtotheMMI
security.ExceptforEquityCUSIP,all
valuesintheservicecorrespondto
thisfield.
CUSIPDescription Character(20) MMIEligibleCUSIPdescription
(MRO)
SeeCUSIPDescriptionBreakdown
onpage 13.
ProductType Character(2) Identifiestheproductcategoryto
whichthesecuritybelongs.
ValidValues:
l CP
l CD
IssuerName Character(22) TheNameoftheissuer.
SettlementDate Character(10) ThedeliverydateoftheMMIsecurity
inYYYYMMDDformat.
Dated/IssueDate Character(10) Thedateofissuanceandthedateon
whichintereststartstoaccruefordebt
[[securities]],inYYYMMDDformat.
MaturityDate Character(10) Thedateonwhichthematurity
proceedsaredueandpayable,in
YYYYMMDDformat.
DTCCMoneyMarketKineticsFieldSpecifications
DTCCMoneyMarketKineticsUserGuide
FieldSpecifications 5

---

## Page 6

HeaderText Type Description
PrincipalAmount Character(20) Thefacevalueofthesecurity. The
fieldisanumericfieldthatisleft-
justifiedwithtrailingblanks.The
numericfieldisformattedasfollows:
999999999.99.
SettlementAmount Character(15) Thenetproceedsofthetransaction.
Thefieldisanumericfieldthatisleft-
justifiedwithtrailingblanks.The
numericfieldisformattedasfollows:
999999999.99.
InterestRate Character(9) Therateofincomeearnedat
issuance.Thenumericfieldis
formattedasfollows:999.999999.
Notes:
l Fordiscountnotes,thisrateis
representativeofthediscount
rate
l ForVariableRateSecurities,
thereisnoInterestRateavail-
able.Forallsettlementsrep-
resentingVariableRate
Issuances,aplaceholdervalue
of.01appears.The.01valuehas
norelationshiptotheissuanceor
settlementactivity.
InterestRateType Character(1) Theratetype—eitherfixedor
variable.
Validvalues:
l F
l V
IncomePaymentType Character(1) Indicatesthetypeofincome
structure:
l P:PeriodicIncomepayments
l I:Incomeatmaturity
l Z:ZeroCoupon
l D:Discount.
DTCCMoneyMarketKineticsFieldSpecifications(continued)
DTCCMoneyMarketKineticsUserGuide
FieldSpecifications 6

---

## Page 7

HeaderText Type Description
FirstPaymentDate Character(8) Thedatetheholderofthesecurityis
targetedtoreceivethefirstincome
payment,inYYYYMMDDformat.
PaymentFrequencyType Character(1) Indicatestheperiodicincome
paymentfrequencytype:
l Y:Year
l M:Month
l W:Week
l D:Day
Defaultvalueofspaces.
PaymentFrequencyCount Character(3) Indicatestheperiodicincome
paymentfrequencyusedin
conjunctionwiththefrequencytype.
Forexample,avalueof90witha
frequencytypeofDmeans90days.
Defaultvalueofspaces.
PutOption Character(1) IndicateswhetherrepaymentPUT
optiontermsareineffect.
Validvalues:
l Y
l N
Call Character(1) Indicateswhetherthesecurityhasa
CALLfeature.Validvalues:
l Y
l N
IndexedPrincipal Character(1) Indicatesiftheprincipalpaymentsare
determinedviaaspecificindex.
Validvalues:
l Y
l N
DTCCMoneyMarketKineticsFieldSpecifications(continued)
DTCCMoneyMarketKineticsUserGuide
FieldSpecifications 7

---

## Page 8

HeaderText Type Description
PeriodicPrincipal Character(1) Indicatesifthesecurityhasperiodic
amortizationofprincipalpayments.
Validvalues
l Y
l N
ExtendableMaturity Character(1) IndicateswhethertheMMIhasan
extendablematurityprovision.
ValidValues:
l Y
l N
RenewableNote Character(1) Indicateswhetherthesecurityis
renewable.
ValidValues:
l Y
l N
RepaymentPutUpon
Death
Character(1) Indicateswhetherthesecuritycanbe
redeemediftheholderofthe
securitiesdies.
ValidValues:
l Y
l N
ChangeableInterest
Payment
Character(1) Indicateswhetherthesecurityhasa
featureallowingachangeinthe
frequencyofincomepayments.Valid
Values:
l Y
l N
DTCCMoneyMarketKineticsFieldSpecifications(continued)
DTCCMoneyMarketKineticsUserGuide
FieldSpecifications 8

---

## Page 9

HeaderText Type Description
InterestRateReset Character(1) Indicatesifthespreadorspread
multiplierforavariableratesecurity
canberesetattheoptionofthe
Issuerorafixedratesecurityifthe
fixedratecanbereset.ValidValues:
l Y
l N
InterestStep-up Character(1) Indicateswhetherthesecuritycan
haveitsincomerateresetoneother
timeduringitslife.
ValidValues:
l Y
l N
Exchangeable Character(1) Indicateswhetherthesecurityis
Exchangeable.
l Y
l N
TransactionID Character(16) Theuniquetransactionidentifierof
thetransactions.
Itistheexpandedhexvalueofthe8
characterscarriedinthesystem
tables.
PartiestoTransaction
Classification
Character(41) Thisfieldcontainstwovalues:
l IPATONON-DEALER
l DEALERTONON-[[IPA]]
Note:Theserviceonlyincludes
settlementactivitythataDealeror
IPAinitiates.Datainitiatedbyother
partiesisnotincluded.
DTCCMoneyMarketKineticsFieldSpecifications(continued)
DTCCMoneyMarketKineticsUserGuide
FieldSpecifications 9

---

## Page 10

HeaderText Type Description
SectorCode Character(3) Issuerindustrysectorcode.
Note:For30-minuteusers,the
followingfieldsmaynotbepopulated
fornewlyissuedsecuritiesonthe
issuances'firstdayofactivity
Term Character(5) Durationofissue(>365Days=Long;
<365Days=Short)
Duration(Days) Number(6) Durationofissueindays
DaystoMaturity Number(6) Daysremainingtoissuematurity
(MaturityDate–SettlementDate)
1stSettlementDate* Character(10) Theissue’sfirsteligiblesettlement
date,inYYYYMMDDformat.
Note: Anysecuritythatsettledbefore
November11,2014willnothavea
FirstSettlementdateavailableand
willbereplacedbyazerovalue.
Thesesecuritieswereissuedbefore
[[DTCC]]'sdatabasehistoryof
settlementactivity
CountryCode Character(3) Theissuer’scountrydomicile.
Note:For30-minuteusers,the
followingfieldsmaynotbepopulated
fornewlyissuedsecuritiesonthe
issuances'firstdayofactivity
DTCCMoneyMarketKineticsFieldSpecifications(continued)
DTCCMoneyMarketKineticsUserGuide
FieldSpecifications 10

---

## Page 11

HeaderText Type Description
EquityCUSIP*** Alphanumeric(9) Aunique9-characteralphanumeric
identifierassignedtoareference
equitysecurity.Thisnumberisa
referencemappingtoa
correspondingequityinstrumentfrom
thesameissuer.
Notes:For30-minuteusers,the
followingfieldsmaynotbepopulated
fornewlyissuedsecuritiesonthe
issuances'firstdayofactivity.
*AnysecuritythatsettledbeforeNovember11,2014willnothaveaFirstSettlementdateavailable
andwillbereplacedbyazerovalue.ThesesecuritieswereissuedbeforeDTCC'sdatabase
historyofsettlementactivity.
**For30-minuteusers,thefollowingfieldsmaynotbepopulatedfornewlyissuedsecuritiesonthe
issuances'firstdayofactivity.
***.
DTCCMoneyMarketKineticsFieldSpecifications(continued)
DTCCMoneyMarketKineticsUserGuide
FieldSpecifications 11

---

## Page 12

FILEDELIVERYSCHEDULE
DTCCMoneyMarketKineticsfilesaredeliveredovertheInternetviaSFTP.
l Endofday:Theendofdayfile,whichcontainsalltransactionsfortheday,isdeliveredatapprox-
imately5:10PMET.
l Intraday:Intradayfilesaredeliveredeveryhalfhourfrom8:15AM ETto5:10PMET(thecumulative
file).
DTCCMoneyMarketKineticsUserGuide
FileDeliverySchedule 12

---

## Page 13

CUSIPDESCRIPTIONBREAKDOWN
ShortDescriptionFormatting
----+----1----+----2
ShortDescription
¢MNAGP*CG4604500GLM%
l ¢-literal"¢"
l MN-MMIproduct
l AGP*-Acronym
l DIS-DiscountedCUSIPsthattendtohavehighervaluesintheinterestratefield
l CG-maturitymonthanddayof(031646-MaturityDate)representedbythefollowingcodes:
o MaturityMonth:
'01A'
'02B'
'03C'
'04D'
'05E'
'06F'
'07G'
'08H'
'09J'
'10K'
'11L'
'12M'
o MaturityDay:
DTCCMoneyMarketKineticsUserGuide
CUSIPDescriptionBreakdown 13

---

## Page 14

'011'
'022'
'033'
'044'
'055'
'066'
'077'
'088'
'099'
'10A'
'11B'
'12C'
'13D'
'15F'
'14E'
'16G'
DTCCMoneyMarketKineticsUserGuide
CUSIPDescriptionBreakdown 14

---

## Page 15

l 46-maturityyear(031646-MaturityDate)
l 04500
EVALUATETRUE
WHENINC-PAY-TYPE= 'Z'
MOVE'*DIS*'TODTC-DESC-POS-12-16
WHENINC-PAY-TYPE= 'V'
MOVE'*VAR*'TODTC-DESC-POS-12-16
WHENOTHER
MOVEMMIEDTCA-DISCNT-POS-2-6 TODTC-DESC-POS-12-16
ENDEVALUATE
l GL--'
WHENIC-GLOBAL-IN= 'Y
EVALUATETRUE
WHENIX-PRINCPAL-IN= 'Y'
MOVE'GF'TODTC-DESC-POS-17-18
WHENOTHER
MOVE'GL'TODTC-DESC-POS-17-18
ENDEVALUATE
ENDEVALUATE
DTCCMoneyMarketKineticsUserGuide
CUSIPDescriptionBreakdown 15

---

## Page 16

l M - MarketType(MARKETCODEontheIssuer)
% -
- WHENINC-PAY-TYPE= 'I'
EVALUATETRUE
MOVE'&'TODTC-DESC-POS-20
WHENOTHER
MOVE'+'TODTC-DESC-POS-20
ENDEVALUATE
WHENINC-PAY-TYPE= 'P'
EVALUATETRUE
WHENISSUANCE-TYPE= 'P'
MOVE'@'TODTC-DESC-POS-20
WHENOTHER
MOVE'%'TODTC-DESC-POS-20
ENDEVALUATE
WHENINC-PAY-TYPE= 'Z'
EVALUATETRUE
MOVE'C'TODTC-DESC-POS-20
WHENOTHER
MOVE'$'TODTC-DESC-POS-20
ENDEVALUATE
DTCCMoneyMarketKineticsUserGuide
CUSIPDescriptionBreakdown 16

---

## Page 17

SECTORCODES
Code Name Definition
AGR AGRICULTURE Farmingandorotheragriculturalproducts.
CGM CONGLOMORATE Multiplelargebusinessesthatcannotbeassociatedwitha
singlecategory.
CNM CONSUMERNON-MANDATORY Consumerproductsthatareconsideredluxuryorabove
necessities.
COM CONSUMERMANDATORY Consumerproducts,suchasfood,clothingorothernecessities.
ENE ENERGY Explorationand/orproductionofOil,Gas,Coal,Wind,Solar,or
otherformsofenergy,aswellasinfrastructure,suchas
pipelinesorotherequipmentassociatedwiththeexplorationor
usageofenergy.
FIN FINANCE Banks,Brokers,Dealers,andInvestmentManagers.
HCR HEALTHCARE Anyformofhealth-relatedservice,suchasbiotechnology,
hospitals,pharmaceuticals,ormedicaldevices
IND INDUSTRIALS Involvedwiththecreationofcomponentsorendproductsof
manufacturing.
MAT MATERIALS RawmaterialsuchasChemicalsorotherbasecomponents.
PF PUBLICFINANCE Governmentbackedorsponsoredentities.
TEC TECHNOLOY Anyformoftechnology,underlyingand/ordeliverydevices.
TEL TELECOM Communications,suchasphones,internet,television,and
otherforms.
TRA TRANSPORTATION Airlines,Railroads,Cargoorothertransportationactivities
UTL UTITLITIES Water,Power,and/orotherutilityfunctions.
OTR OTHER Noneofthecategoriesonthislistdescribethecompany's
activities.
SectorCodes
DTCCMoneyMarketKineticsUserGuide
SectorCodes 17

---

## Page 18

REFERENCEEQUITYCUSIPMAPPING
LOGIC
MoneyMarketIssuernameshavebeenmappedtothecorrespondingequityissuersofthesameorsimilar
issuenametocreatetheEquityCUSIPfield.TheequityissueCUSIPofthecorrespondingissuergets
displayed.
DTCCMoneyMarketKineticsUserGuide
ReferenceEquityCUSIPMappingLogic 18

---

## Page 19

SAMPLEDATA
OpenthesampledatafiletoviewsampledatafortheDTCCMoneyMarketKineticsservice,postedontheDTCC
LearningCenter.
DTCCMoneyMarketKineticsUserGuide
SampleData 19

---

## Page 20

©2023.Allrightsreserved.[[DTCC]],[[DTCC]](Stylized)andFinancialMarkets.Forward.areregisteredandunregistered
trademarksofTheDepositoryTrust&ClearingCorporationDTCC.Theservicesdescribedhereinareprovidedunder
the“[[DTCC]]”brandnamebycertainaffiliatesofTheDepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitself
doesnotprovidesuchservices.Eachoftheseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsof
theparticularcountryorcountriesinwhichsuchentityoperates.Pleaseseewww.[[DTCC]].comformoreinformationon
[[DTCC]],itsaffiliatesandtheservicestheyoffer.
DocDate:December12,2023
PublicationCode:DAT325
Service:MoneyMarketKinetics
Title:UserGuide
ForMoreInformation
EmailDTCCLearningat:
DataLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com