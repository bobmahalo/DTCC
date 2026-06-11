---
title: "DTCC OTC Direct Connect User's Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat318_otd_direct_connectug_20240102.pdf"
pages: 91
size: "475.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# DTCC OTC Direct Connect User's Guide

**Original File:** [dat318_otd_direct_connectug_20240102.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat318_otd_direct_connectug_20240102.pdf)  
**Category:** Other  
**Total Pages:** 91  
**File Size:** 475.4 KB  

---

## Page 1

DTCCOTCDirectConnect
USER'SGUIDE
JANUARY02,2024

---

## Page 2

TABLEOFCONTENTS
Overview 3
OTCDirectConnectDataDictionary 4
UpdatesforNorthAmericaPhase2Rewrite 90
DTCOTCDirectConnectUser'sGuide
TableOfContents 2

---

## Page 3

OVERVIEW
[[DTCC]]’sOTCDirectConnectserviceprovidessubscriberswithasystematicdeliverymechanismforOTCderivativestransactiondatapublishedonDTCCData
Repository(U.S.)LLC’s(DDR)publicpricedisseminationdashboard(PPDDashboard).OTCDirectConnectisanindependentofferingofDTCCSolutionsLLCand
isnotaserviceofferingofDDR.
AlldataisdeliveredontheAWSDataExchange,providingafast,frictionless,andsecuredatadeliverysolutionthatenablessubscriberstomanagemarketand
tradingriskfactorsinnearreal-time.
ClicktheselinksforinformationrelatedtoAWSDataExchange:
l WhatisAWSDataExchange?
l SubscribetoS3dataaccess
l Privateproductandoffers
DTCOTCDirectConnectUser'sGuide
Overview 3

---

## Page 4

OTCDirectConnectDataDictionary
CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
1 Dissemination
Identifier
Dissemination
Identifier
Amount-Numeric-
38-0
UniqueGTR-generated
identifierforeachpublicly
disseminationmessage.
AsgeneratedbytheGTRservice l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
2 OriginalDis-
seminationIden-
tifier
OriginalDis-
seminationIden-
tifier
Amount-Numeric-
38-0 Forallactiontypesother
thanNEWT,the
Disseminationidentifier
fortheinitial,publicly-
disseminatedswap
transactionandpricing
data.
AsgeneratedbyGTRservice l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
4

---

## Page 5

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
3 Actiontype Actiontype Enumerated-
Code-List
Typeofactiontakenon
theswaptransactionor
typeofend-of-dayreport-
ing.
l NEWT:New.Anactionthatreportsa
newswaptransaction.Itappliesto
thefirstmessagerelatingtoanew
USIorUTI.
l MODI:Modify.Anactionthat:mod-
ifiesthestateofapreviouslysub-
mittedtransaction(forexample,
creditevent);changesatermofa
previouslysubmittedtransaction
duetoanewlynegotiatedmodi-
fication(amendment);updatespre-
viouslymissinginformation(for
example,apostpriceswap).Itdoes
notincludecorrectionofaprevious
transaction.
l CORR:Correction.Anactionthat
correctserroneousdataofapre-
viouslysubmittedtransaction.
l EROR:Error.Anactionofcan-
cellationofawronglysubmitted
entiretransactionincaseitnever
cameintoexistenceorwasnotsub-
jecttopart43/part45reporting
requirements,butwasreportederro-
neously;oracancellationofduplic-
atereport.
l TERM:Terminate.Anactionthat
closesanexistingtransaction
becauseofanewevent(for
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
5

---

## Page 6

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
example,Compression,[[Novation]]).
Thistypedoesnotapplytotrans-
actionsthatterminatedatthecon-
tractualmaturitydate.
l REVI:Revive.Anactionthatrein-
statesaswaptransactionthatwas
reportedaserrororterminatedby
mistake.
l PRTO:Transferout.Anactionthat
transfersswaptransactionfromone
SDRtoanotherSDR(changeof
swapdatarepository).
l VALU:Anupdatetovaluationdata.
Therewillbenocorresponding
Eventtype.
l MARU:Anupdatetocollateralmar-
gindata.Therewillbenocor-
respondingEventtype.
DTCOTCDirectConnectUser'sGuide
6

---

## Page 7

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
4 Eventtype Eventtype Enumerated-
Code-List
Explanationorreasonfor
theactiontakenonthe
swaptransaction.
Eventsmayinclude,but
arenotlimitedto,trade,
[[Novation]],compression
orriskreduction
exercise,early
termination,clearing,
exercise,allocation,
clearingandallocation,
creditevent,and
transfer.
l TRAD:Trade.Acreation,ormodi-
ficationofatransaction.
l NoVA:[[Novation]].Anovationlegally
movespartialorallofthefinancialrisks
ofaswapfromatransferortoatrans-
feree.Ithastheeffectofter-
minating/modifyingtheoriginal
transactionandcreatinganewtrans-
actiontoidentifytheexposurebetween
thetransferor/transfereeandthe
remainingparty.
l COMP:CompressionorRiskReduc-
tion.Compressionsandriskreduction
exercisesgenerallyhavetheeffectof
terminatingormodifying(thatis.,redu-
cingthenotionalvalue)asetofexisting
transactionsandofcreatingasetof
newtransaction(s).Theseprocesses
resultinlargelythesameexposureof
marketriskthatexistedpriortothe
eventforthecounterparty.
l ETRM:Earlytermination.Termination
ofanexistingswaptransactionpriorto
thescheduledterminationormaturity
date.
l CLRG:Clearing.Centralclearingisa
processwhereaderivativesclearing
organizationinterposesitselfbetween
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
7

---

## Page 8

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
counterpartiestocontracts,becoming
thebuyertoeverysellerandtheseller
toeverybuyer.Ithastheeffectofter-
minatinganexistingtransaction
betweenthebuyerandthesellerand
therebyensuringtheperformanceof
opencontracts
l EXER:Exercise.Theprocessbywhich
acounterpartyfullyorpartiallyexer-
cisestheirrightsspecifiedinthecon-
tractofanoptionoraswaption.
l ALOC:Allocation.Theprocessby
whichanagent,havingfacilitateda
singleswaptransactiononbehalfof
severalclients,allocatesaportionof
theexecutedswaptotheclients
l CLAL:ClearingandAllocation.Asim-
ultaneousclearingandallocationevent
inaderivativesclearingorganization.
l CREV:Creditevent.Aneventortrigger
thatresultsintheterminationormodi-
ficationofthestateofapreviouslysub-
mittedcreditderivativetransaction.
Appliesonlytocreditderivatives.
l PTNG:Transfer.Areportingcoun-
terpartymaychangetheswapdata
repositorytowhichthetransactionis
DTCOTCDirectConnectUser'sGuide
8

---

## Page 9

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
reportedpursuanttorule§45.10(d).
Theprocessbywhichaswapistrans-
ferredtoanotherSDRthathasthe
effectoftheclosingoftheswaptrans-
actionatoneSDRoropeningofthe
sameswaptransactionusingthesame
UTI/USIinadifferentSDR(new).
l CORP:Corporateevent.Acorporate
actiononequityunderlyingthatimpacts
thetransactionsonthatequity.
l UPDT:Upgrade.Anupdateofanout-
standingtransactionperformedduring
thetransitionperiodintoensureitscon-
formitywiththeamendedreporting
requirements.
DTCOTCDirectConnectUser'sGuide
9

---

## Page 10

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
5 EventtimestampEventtimestampISO8601-
DateTimeYYYY-
MM-
DDTHH:MM:SSZ,
basedonUTC
Dateandtimeofoccur-
renceoftheevent,as
determinedbythereport-
ingcounterpartyoraser-
viceprovider.
l Forcollateralupdates
(Actiontype=MARU),
itisthedateforwhich
theinformationcon-
tainedinthereportis
provided.
l Forclearingevents,it
istheclearingevent,
dateandtimewhen
theoriginalswapwas
acceptedbythederiv-
ativeclearingorgan-
ization(DCO)for
clearingandrecorded
bytheDCO’ssystem..
Anyvaliddate/time.Boththedateand
timeportionarerequiredtobereported.
Thetimeelementisasspecificas
technologicallypracticable.Ifthetime
portionwasnotavailable,thetime
portionisreportedas00:00:00.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
6 Amendmentindic-
ator
Amendmentindic-
ator
Boolean Indicatorofwhetherthe
modificationoftheswap
transactionreflectsnewly
agreeduponterm(s)from
thepreviouslynegotiated
terms.
l True
l False
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
10

---

## Page 11

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
7 AssetClass AssetClass Enumerated-
Code-List
UPIRDL:Indicates
whethertheasset,bench-
mark,orotherderivatives
contractunderlyinga
derivativescontractis,or
references,anequity,
rate,credit,commodityor
foreignexchangeasset.
l CFTCTradeState,PPD,andValu-
ation:Commodity,Credit,[[Equity]],For-
eignExchange,InterestRate
l SECTradeStateandPPD:Credit,
[[Equity]],InterestRate
l CanadaTradeStateandValuation:
Commodity,Credit,[[Equity]],For-
eignExchange,InterestRate
l CanadaPPD:Credit,[[Equity]],
InterestRate
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
8 Productname Productname Enumerated-
Code-List
RequiredforGTRpro-
cessingtoderiveval-
idationbasedontheISDA
taxonomy.Itisalower-
leveldescriptionofthe
characteristicsofanasset
orcontractunderlyinga
derivative.
SeetheISDA websiteforafulllistof
ISDAProductIDCodes.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
9 Cleared Cleared Enumerated-
Code-List
Indicatorofwhetherthe
transactionhasbeen
clearedorisintendedto
beclearedbyacentral
counterparty.
l Y:Yes,centrallyclearedforbetaand
gammatransactions.
l N:No,notcentrallycleared.
l I:Intenttoclear;foralphatransactions
thatareplannedtobesubmittedto
clearing.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
11

---

## Page 12

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
10 Mandatoryclearing
indicator
Mandatoryclearing
indicator
Boolean Anindicatorofwhether
thetransactionissubject
tomandatoryclearing.
l True
l False
l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
12

---

## Page 13

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
11 Execution
Timestamp
Execution
Timestamp
ISO8601-
DateTimeYYYY-
MM-
DDTHH:MM:SSZ,
basedonUTC.
Boththedateand
timeportionare
requiredtobe
reported.Ifthe
timeelementisnot
requiredinapar-
ticularjurisdiction,
timemaybe
droppedgiventhat
–inthecaseofrep-
resentationswith
reducedaccuracy
–ISO8601allows
thecompleterep-
resentationtobe
omitted,theomis-
sionstartingfrom
theextremeright-
handside(inthe
orderfromthe
leasttothemost
significant).
Dateandtimeatrans-
actionwasoriginally
executed,resultinginthe
generationofanewUTI.
Thisdataelement
remainsunchanged
throughoutthelifeofthe
UTI.
Forclearingswaps,the
executiontimestampis
thedateandtimewhen
theDCOacceptsthe
originalswap.
Anyvaliddate/time l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
13

---

## Page 14

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
12 EffectiveDate EffectiveDate ISO8601-UTC-
DateYYYY-MM-
DDbasedonUTC
Unadjusteddateonwhich
obligationsunderthe
OTCderivativetrans-
actioncomeintoeffect,as
includedinthecon-
firmation.
Forcommoditiesswaps,
itisthepricingstart
date.
Anyvaliddate. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
13 ExpirationDate ExpirationDate ISO8601-UTC-
DateYYYY-MM-
DDbasedonUTC
Unadjusteddateonwhich
obligationsunderthe
OTCderivativetrans-
actionstopbeingeffect-
ive,asincludedinthe
confirmation.
Forcommoditiesswaps,
itisthepricingenddate.
Anyvaliddate. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
14 Maturitydateofthe
underlier
Maturitydateofthe
underlier
ISO8601-UTC-
DateYYYY-MM-
DDbasedonUTC
Thedateonwhichthe
underlyingtransaction
settlesiftheoptionisexer-
cised.
Forswaptions,itisthe
maturitydateofthe
underlyingswap.
Anyvaliddate l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
14

---

## Page 15

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
15 Non-standardized
termindicator
Non-standardized
termindicator
Boolean Indicatorofwhetherthe
swaphasoneormore
additionalterm(s)orpro-
vision(s)thatmaterially
affect(s)thepriceofthe
swap(otherthanthose
disseminatedtothepublic
pursuanttopart43).
l True
l False
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
15

---

## Page 16

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
16 PlatformidentifierPlatformidentifierEnumerated-
Code-List
Identifierofthetrading
facility(forexample,
exchange,multilateral
tradingfacility,swapexe-
cutionfacility)onwhich
thetransactionwas
executed.
l SeetheISOwebsiteforalitofISO
10383SegmentMarketIdentifier
Codes.
l Ifnotradingfacilitywasinvolvedinthe
transaction:
o XOFF:fortransactionsinlisted
instruments
o XXXX:fortransactionsininstru-
mentsthatarenotlistedinany
venue
o BILT:ifthereportingcoun-
terpartycannotdetermine
whethertheinstrumentislisted
ornot,asperjurisdictional
requirements.
l WheretheSegmentMICdoesnot
exist,theOperatingMICisused.SDRs
arenotexpectedtoverifywhetherthe
reportedvalueisaSegmentMICor
OperatingMIC,aslongasitisinthelist
ofMICcodesinISO10383
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
16

---

## Page 17

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
17 Primebrokerage
transactionindic-
ator
Primebrokerage
transactionindic-
ator
Boolean Indicatorofwhetherthe
swaptransactionsatisfies
thedefinitionof“mirror
swap”or“triggerswap”in
§43.2(a)oftheCom-
mission’sregulations.
l True
l False
l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:No
18 Blocktradeelec-
tionindicator
Blocktradeelec-
tionindicator
Boolean Indicatorofwhetherthe
swaptransactionsatisfied
thedefinitionof“mirror
swap”or“triggerswap”in
§43.2(a)oftheCom-
mission’sregulations.
l True
l False
l Blank
l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:No
19 Largenotionaloff-
facilityswapelec-
tionindicator
Largenotionaloff-
facilityswapelec-
tionindicator
Boolean Indicatorofwhetheran
electionwasmadeto
reporttheswaptrans-
actionasaLargeNotional
Off-facilitySwapbythe
reportingcounterparty,or
ascalculatedbyeitherthe
swapdatarepositoryact-
ingonbehalfofthereport-
ingcounterpartyorby
usingathirdparty.
l True
l False
l Blank
l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
17

---

## Page 18

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
20 Notionalamount-
Leg1
Notionalamount-
Leg1
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Foreachlegofthetrans-
action,whereapplicable:
l OTCderivativetrans-
actionsnegotiatedin
monetaryamounts:
theamountspecified
inthecontract.
l OTCderivativetrans-
actionsnegotiatedin
non-monetary
amounts:referto
AppendixBinthe
CFTCTechSpe-
cificationforcon-
vertingnotional
amountsfornon-mon-
etaryamounts.Inaddi-
tion:
l OTCderivativetrans-
actionswitha
notionalamount
schedule:theinitial
notionalamount
agreedbythecoun-
terpartiesattheincep-
tionofthetransaction.
l AmendmentsorLife-
cycleevents:theres-
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
18

---

## Page 19

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
ultingoutstanding
notionalamountrepor-
ted.Inthecaseofa
Lifecycleeventthatis
afulltermination
beforetheswapmatur-
itydate,itisthefullter-
minatedvalue.
l Notionalamountsfor
CDSreflectthegross
amountandnotthe
netamount.
DTCOTCDirectConnectUser'sGuide
19

---

## Page 20

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
21 Notionalamount-
Leg2
Notionalamount-
Leg2
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Foreachlegofthetrans-
action,whereapplicable:
ForOTCderivative
transactionsnegotiated
inmonetaryamounts,it
istheamountspecified
inthecontract.
ForOTCderivative
transactionsnegotiated
innon-monetary
amounts,referto
AppendixBinthe
CFTCTech
Specificationfor
convertingnotional
amountsfornon-
monetaryamounts.In
addition:
ForOTCderivative
transactionswitha
notionalamount
schedule,itistheinitial
notionalamount,agreed
bythecounterpartiesat
theinceptionofthe
transaction.
Foramendmentsor
Lifecycleevents,the
resultingoutstanding
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
20

---

## Page 21

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
notionalamountis
reported.Inthecaseof
aLifecycleeventthatis
afullterminationbefore
theswapmaturitydate,
itisthefullterminated
value.
Notionalamountfor
CDSreflectthegross
amountandnotthenet
amount.
22 Notionalcurrency-
Leg1
Notionalcurrency-
Leg1
Enumerated-
Code-List
Currencyinwhichthe
notionalamountisdenom-
inatedforeachlegofthe
transaction.
SeetheISO websiteforalistofISO4217
CurrencyCodes.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
23 Notionalcurrency-
Leg2
Notionalcurrency-
Leg2
Enumerated-
Code-List
Currencyinwhichthe
notionalamountisdenom-
inatedforeachlegofthe
transaction.
SeetheISO websiteforalistofISO4217
CurrencyCodes.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
21

---

## Page 22

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
24 Notionalquantity-
Leg1
Notionalquantity-
Leg1
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Forswaptransactions
(eachleg)negotiatedin
non-monetaryamounts
withfixednotionalquant-
ityforeachschedule
period(i.e.,50barrelsper
month).
TheQuantityfrequency
andtheQuantityunitof
measurefieldsareused
asareference.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
25 Notionalquantity-
Leg2
Notionalquantity-
Leg2
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Forswaptransactions
(eachleg)negotiatedin
non-monetaryamounts
withfixednotional
quantityforeach
scheduleperiod(i.e.,50
barrelspermonth).
TheQuantityfrequency
andtheQuantityunitof
measurefieldsareused
asareference.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
22

---

## Page 23

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
26 Totalnotional
quantity-Leg1
Totalnotional
quantity-Leg1
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Foreachlegofthetrans-
action,itistheaggregate
Notionalquantityofthe
underlyingassetforthe
termofthetransaction.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
27 Totalnotional
quantity-Leg2
Totalnotional
quantity-Leg2
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Foreachlegofthetrans-
action,itistheaggregate
Notionalquantityofthe
underlyingassetforthe
termofthetransaction.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
28 Quantityfrequency
multiplier-Leg1
Quantityfrequency
multiplier-Leg1
Amount-Numeric-
3-0
Thenumberoftimeunits
fortheQuantityfre-
quency.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
23

---

## Page 24

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
29 Quantityfrequency
multiplier-Leg2
Quantityfrequency
multiplier-Leg2
Amount-Numeric-
3-0
Thenumberoftimeunits
fortheQuantityfre-
quency.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
30 Quantityunitof
measure-Leg1
Quantityunitof
measure-Leg1
Enumerated-
Code-List Unitofmeasureinwhich
theTotalnotional
quantityandNotional
quantityareexpressed
(ForeachLeg).
SeetheISOUnitOfMeaureCodepagefor
allowedvalues.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
31 Quantityunitof
measure-Leg2
Quantityunitof
measure-Leg2
Enumerated-
Code-List
Unitofmeasureinwhich
theTotalnotionalquantity
andNotionalquantityare
expressed(Foreach
Leg).
SeetheISOUnitOfMeaureCodepagefor
allowedvalues.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
24

---

## Page 25

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
32 Quantityfre-
quency-Leg1
Quantityfre-
quency-Leg1
Enumerated-
Code-List
Therateatwhichthe
quantityisquotedonthe
swap.
l HOUL:Hourly
l DAIL:Daily
l WEEK:Weekly
l MNTH:Monthly
l ONDE:OnDemand
l YEAR:Yearly
l EXPI:Endofterm
l ADHO=Adhoc;applieswhenpay-
mentsareirregular.
o 3:Torepresentquarterly,report
[Quantityfrequency]=‘MNTH’
and[Quantityfrequencymul-
tiplier]
o 6: Torepresentsemi-annual,
report[Quantityfrequency]=
‘MNTH’and[Quantityfrequency
multiplier]
o Toallowforcross-jurisdictional
submissions,thefollowingvalues
willbeacceptedandmapped1-
1:
n DAIL:PerCalendarDay
n DAIL:PerBusinessDay
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
25

---

## Page 26

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
n HOUL: PerHour
n MNTH: PerMonth
n EXPI:Term
DTCOTCDirectConnectUser'sGuide
26

---

## Page 27

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
33 Quantityfre-
quency-Leg2
Quantityfre-
quency-Leg2
Enumerated-
Code-List
Therateatwhichthe
quantityisquotedonthe
swap.
l HOUL:Hourly
l DAIL:Daily
l WEEK:Weekly
l MNTH:Monthly
l ONDE:OnDemand
l YEAR:Yearly
l EXPI:Endofterm
l ADHO=Adhoc;applieswhenpay-
mentsareirregular.
o 3:Torepresentquarterly,report
[Quantityfrequency]=‘MNTH’
and[Quantityfrequencymul-
tiplier]
o 6: Torepresentsemi-annual,
report[Quantityfrequency]=
‘MNTH’and[Quantityfrequency
multiplier]
o Toallowforcross-jurisdictional
submissions,thefollowingvalues
willbeacceptedandmapped1-
1:
n DAIL:PerCalendarDay
n DAIL:PerBusinessDay
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
27

---

## Page 28

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
n HOUL: PerHour
n MNTH: PerMonth
n EXPI:Term
34 Notionalamountin
effectonasso-
ciatedeffective
date-Leg1
Notionalamountin
effectonasso-
ciatedeffective
date-Leg1
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
ForOTCderivativetrans-
actionsnegotiatedinmon-
etaryamountswitha
notionalamountsched-
ule,thenotionalamount
whichbecomeseffective
ontheassociatedunad-
justedeffectivedate.
Theinitialnotional
amountandassociated
unadjustedeffectiveand
enddatearereportedas
thefirstvaluesofthe
schedule.
Thisdataelementisnot
validforOTCderivative
transactionswith
notionalamountsthat
arecondition-orevent-
dependent.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
28

---

## Page 29

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
35 Notionalamountin
effectonasso-
ciatedeffective
date-Leg2
Notionalamountin
effectonasso-
ciatedeffective
date-Leg2
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
ForOTCderivative
transactionsnegotiated
inmonetaryamounts
withanotionalamount
schedule,theNotional
amountthatbecomes
effectiveonthe
associatedunadjusted
effectivedate.
Theinitialnotional
amountandassociated
unadjustedeffectiveand
enddatearereportedas
thefirstvaluesofthe
schedule.
Thisdataelementisnot
validforOTCderivative
transactionswith
notionalamountsthat
arecondition-orevent-
dependent.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
29

---

## Page 30

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
36 Effectivedateof
thenotional
amount-Leg1
Effectivedateof
thenotional
amount-Leg1
ISO8601-UTC-
DateYYYY-MM-
DDbasedonUTC
ForOTCderivativetrans-
actionsnegotiatedinmon-
etaryamountswitha
notionalamountschedule
,theunadjusteddateon
whichtheassociated
notionalamountbecomes
effective.
Thisdataelementisnot
applicabletoOTC
derivativetransactions
withnotionalamounts
thatarecondition-or
event-dependent.
Anyvaliddate. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
37 Effectivedateof
thenotional
amount-Leg2
Effectivedateof
thenotional
amount-Leg2
ISO8601-UTC-
DateYYYY-MM-
DDbasedonUTC
ForOTCderivativetrans-
actionsnegotiatedinmon-
etaryamountswitha
notionalamountsched-
ule,theunadjusteddate
onwhichtheassociated
notionalamountbecomes
effective
l Thisdataelementis
notapplicabletoOTC
derivativetransactions
withnotionalamounts
thatarecondition-or
event-dependent.
Anyvaliddate. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
30

---

## Page 31

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
38 Enddateofthe
notionalamount-
Leg1
Enddateofthe
notionalamount-
Leg1
ISO8601-UTC-
DateYYYY-MM-
DDbasedonUTC
ForOTCderivativetrans-
actionsnegotiatedinmon-
etaryamountswitha
notionalamountsched-
ule:
l ThisfieldistheUnad-
justedenddateofthe
notionalamount.
l Thisdataelementis
notapplicabletoOTC
derivativetransactions
withnotionalamounts
thatarecondition-or
event-dependent.
Anyvaliddate. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
31

---

## Page 32

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
39 Enddateofthe
notionalamount-
Leg2
Enddateofthe
notionalamount-
Leg2
ISO8601-UTC-
DateYYYY-MM-
DDbasedonUTC
ForOTCderivativetrans-
actionsnegotiatedinmon-
etaryamountswitha
notionalamountsched-
ule:
l ThisfieldistheUnad-
justedenddateofthe
notionalamount.
l Thisdataelementis
notapplicabletoOTC
derivativetransactions
withnotionalamounts
thatarecondition-or
event-dependent.
Anyvaliddate. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
40 Callamount-Leg1 Callamount
FieldName
Changed
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Forforeignexchange
options,isthemonetary
amountthattheoption
givestherighttobuy.Itis
applicabletoallasset
classes.
Anyvaluegreaterthanzero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
32

---

## Page 33

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
41 Callamount-Leg2 Callamount-Leg
2
FieldNoLonger
Used
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Forforeignexchange
options,thisfieldisthe
monetaryamountthatthe
optiongivestherightto
buy.Itisapplicabletoall
assetclasses.
Anyvaluegreaterthanzero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
42 Callcurrency-Leg
1 Callcurrency
FieldName
Changed
Enumerated-
Code-List
Forforeignexchange
options,thecurrencyin
whichtheCallamountis
denominated.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
43 Callcurrency-Leg
2 Callcurrency-Leg
2
FieldNoLonger
Used
Enumerated-
Code-List Forforeignexchange
options,thethe
currencyinwhichthe
Callamountis
denominated.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
33

---

## Page 34

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
44 Putamount-Leg1 Putamount
FieldName
Changed
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Forforeignexchange
options,themonetary
amountthattheoption
givestherighttosell.
ThePutamountandthe
correspondingcurrency
dataelementare
applicableforallasset
classes.
Anyvaluegreaterthanzero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
45 Putamount-Leg2 Putamount-Leg
2
FieldNoLonger
Used
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Forforeignexchange
options:Thisfiledisthe
monetaryamountthat
theoptiongivestheright
tosell.
ThePutamountandthe
correspondingcurrency
dataelementare
applicableforallasset
classes.
Anyvaluegreaterthanzero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
46 Putcurrency-Leg1 Putcurrency
FieldName
Changed
Enumerated-
Code-List
Forforeignexchange
options,thecurrencyin
whichthePutamountis
denominated.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
34

---

## Page 35

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
47 Putcurrency-Leg2 Putcurrency-Leg
2
FieldNoLonger
Used
Enumerated-
Code-List
Forforeignexchange
options,thecurrencyin
whichthePutamountis
denominated.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
48 Exchangerate Exchangerate Amount-
Numeric-31-13
Note: Thelength
isnotfixed,butis
limitedto18
numerical
characters,
includingupto13
numerical
charactersafter
thedecimalpoint.
TheExchangerate
betweenthetwodifferent
currenciesspecifiedinthe
OTCderivativetrans-
actionagreedbythecoun-
terpartiesattheinception
ofthetransaction.
Itisexpressedasthe
rateofexchangefrom
convertingtheunit
currencyintothequoted
currency.
Forexample,0.9426
USD/EUR,USDisthe
unitcurrencyandEUR
isthequotedcurrency;
USD1=EUR0.9426.
ForFX,thisfieldisthe
forwardexchangerate.
Anyvaluegreaterthan0. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
35

---

## Page 36

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
49 Exchangerate
basis
Exchangerate
basis
Enumerated-
Code-List
TheCurrencypairand
orderinwhichthe
exchangerateisdenom-
inated.Itisexpressedas
unitcurrency/quotedcur-
rency.
Forexample,0.9426
USD/EUR,USDisthe
unitcurrencyandEUR
isthequotedcurrency,
USD1=EUR0.9426.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
36

---

## Page 37

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
50 Firstexercisedate Firstexercisedate ISO8601-UTC-
DateYYYY-MM-
DDbasedonUTC
Firstunadjusteddatedur-
ingtheexerciseperiodin
whichanoptioncanbe
exercised.
l ForEuropean-style
options,thisdateis
sameastheExpiration
date.
l ForAmerican-style
options,thefirstpos-
sibleexercisedateis
theunadjusteddate
includedintheExe-
cutiontimestamp.
l Forknock-inoptions,
wherethefirstexer-
cisedateisnotknown
whenanewtrans-
actionisreported,the
firstexercisedateis
updatedasitbecomes
available.
Thisdataelementisnot
applicableifthe
instrumentisnotan
optionordoesnot
embedanyoptionality.
Anyvaliddate. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
37

---

## Page 38

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
51 Fixedrate-Leg1 Fixedrate-Leg1 Monetary-
Numeric-21-10
(Thelengthisnot
fixedbutlimitedto
11numericalchar-
actersincludingup
totennumerical
charactersafter
thedecimalpoint.)
ForOTCderivativetrans-
actionswithperiodicpay-
ments:
Thisfieldistheper
annumrateofthefixed
leg(s).
Positiveandnegativevaluesexpressedin
decimalformat(forexample:0.0257
insteadof2.57%)
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
52 Fixedrate-Leg2 Fixedrate-Leg2 Monetary-
Numeric-21-10
Thelengthisnot
fixedbutislimited
to11numerical
characters,
includingupto
tennumerical
charactersafter
thedecimalpoint.
ForOTCderivativetrans-
actionswithperiodicpay-
ments:
Thisfieldistheper
annumrateofthefixed
leg(s).
Positiveandnegativevaluesexpressedin
decimalformat(forexample:0.0257
insteadof2.57%)
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
38

---

## Page 39

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
53 OptionPremium
Amount
OptionPremium
Amount Monetary-
Numeric-30-5
Thelengthisnot
fixedbutlimited
to25numerical
characters,
includingupto
fivenumerical
charactersafter
thedecimalpoint.
Foroptionsandswap-
tionsofallassetclasses,
themonetaryamount
paidbytheoptionbuyer.
Note: Thisdataelement
isnotapplicableifthe
instrumentisnotan
optionordoesnot
embedanyoptionality.
Anyvaluegreaterthanorequalto0. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
54 OptionPremium
Currency
OptionPremium
Currency
Enumerated-
Code-List
Foroptionsandswap-
tionsofallassetclasses,
thecurrencyinwhichthe
optionpremiumamountis
denominated.
Note: Thisdataelement
isnotapplicableifthe
instrumentisnotan
optionordoesnot
embedanyoptionality.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
39

---

## Page 40

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
55 Price Price Amount-
Numeric-31-13
Thelengthisnot
fixed,butis
limitedto18
numerical
characters,
includingupto13
numerical
charactersafter
thedecimalpoint.
PricespecifiedintheOTC
derivativetransaction.It
doesnotincludefees,
taxesorcommissions.
l Forcommodityfixed/-
floatswapsandsimilar
productswithperiodic
payments,thisdata
elementreferstothe
fixedpriceofthefixed
leg(s).
l Forcommodityand
equityforwardsand
similarproducts,this
dataelementrefersto
theforwardpriceofthe
underlyingorref-
erenceasset.
l Forequityswaps,port-
foliosswaps,andsim-
ilarproducts,thisdata
elementreferstothe
initialpriceofthe
underlyingorref-
erenceasset.
l Forcontractsfordif-
ferenceandsimilar
products,thisdataele-
mentreferstotheini-
l 1:Anyvalue,if[CDE-Pricenotation]
l 3:Anyvalueexpressedasdecimal(for
example,0.0257insteadof2.57%),if
[CDE-Pricenotation]
l Fortransactionswheretheswapprice
isnotknownatthetimetoexecution,
reporttheunknownswapprice-related
fieldsasblankuntilthepriceisknown.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
40

---

## Page 41

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
tialpriceoftheunder-
lier.
Thisdataelementisnot
applicableto:
l Interestrateswaps
andforwardrateagree-
mentsbecausethe
informationincludedin
thedataelements
FixedrateandSpread
maybeinterpretedas
thepriceofthetrans-
action.
l Interestrateoptions
andinterestrateswap-
tionsbecausethe
informationincludedin
thedataelements
StrikepriceandOption
premiummaybeinter-
pretedasthepriceof
thetransaction.
l Commoditybasis
swapsandthefloating
legofcommodity
fixed/floatswaps
becausetheinform-
DTCOTCDirectConnectUser'sGuide
41

---

## Page 42

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
ationincludedinthe
dataelementSpread
maybeinterpretedas
thepriceofthetrans-
action.
l Foreignexchange
swaps,forwardsand
options,becausethe
informationincludedin
thedataelements
Exchangerate,Strike
price,andOption
premiummaybeinter-
pretedasthepriceof
thetransaction.
l Equityoptions
becausetheinform-
ationincludedinthe
dataelementsStrike
priceandOption
premiummaybeinter-
pretedasthepriceof
thetransaction.
l Creditdefaultswaps
andcredittotalreturn
swaps,becausethe
informationincludedin
thedataelements
DTCOTCDirectConnectUser'sGuide
42

---

## Page 43

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
Fixedrate,Spreadand
Upfrontpayment
(Otherpaymenttype:
Upfrontpayment)may
beinterpretedasthe
priceofthetrans-
action.
l Commodityoptions,
becausethatthe
informationincludedin
thedataelements
StrikepriceandOption
premiummaybeinter-
pretedasthepriceof
thetransaction.
56 Priceunitofmeas-
ure
Priceunitofmeas-
ure
Enumerated-
Code-List
Unitofmeasureinwhich
thepriceisexpressed. SeetheISOUnitOfMeaureCodepagefor
allowedvalues.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
43

---

## Page 44

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
57 Spread-Leg1 Spread-Leg1 Amount-
Numeric-31-13
Thelengthisnot
fixedbutislimited
to18numerical
characters,
includingupto13
numerical
charactersafter
thedecimalpoint.
ForOTCderivativetrans-
actionswithperiodicpay-
mentsspreadonthe
individualfloatingleg(s)
indexreferenceprice,in
thecasewherethereisa
spreadonafloatingleg(s)
(e.g.,interestratefixed/-
floatswaps,interestrate
basisswaps,commodity
swaps),.
Forexample,USD-
LIBOR-BBAplus.03or
WTIminusUSD14.65;
ordifferencebetween
thereferencepricesof
thetwofloatingleg
indexes.Forexample,
the9.00USD“Spread”
foraWCSvs.WTIbasis
swapwhereWCSis
pricedat43USDand
WTIispricedat52USD.
Forequityswaps,
portfolioswaps,and
contractfordifference
(CFDs),itshowsthe
weightedoverallspread
forthebasketinsteadof
individuallegs.
l 1:Anyvalue,if[CDE-Spreadnotation-
Leg1
l 3:Anyvalueexpressedasdecimal(for
example,0.0257insteadof2.57%),if
[CDE-Spreadnotation-Leg1]
l 4:Anyintegervalueexpressedinbasis
points(forexample.,257insteadof
2.57%),if[CDE-Spreadnotation-Leg
1]:4
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
44

---

## Page 45

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
58 Spread-Leg2 Spread-Leg2 Amount-
Numeric-31-13
Thelengthisnot
fixedbutislimited
to18numerical
characters,
includingupto13
numerical
charactersafter
thedecimalpoint.
ForOTCderivative
transactionswith
periodicpayments
spreadontheindividual
floatingleg(s)index
referenceprice,inthe
casewherethereisa
spreadonafloatingleg
(s)(e.g.,interestrate
fixed/floatswaps,
interestratebasis
swaps,commodity
swaps),.
Forexample,USD-
LIBOR-BBAplus.03or
WTIminusUSD14.65;
ordifferencebetween
thereferencepricesof
thetwofloatingleg
indexes.Forexample,
the9.00USD“Spread”
foraWCSvs.WTIbasis
swapwhereWCSis
pricedat43USDand
WTIispricedat52USD.
Forequityswaps,
portfolioswaps,and
contractfordifference
(CFDs),itshowsthe
weightedoverallspread
l 1: Anyvalue,if[CDE-Spreadnotation-
Leg2]
l 3: Anyvalueexpressedasdecimal(for
example,,0.0257insteadof2.57%),if
[CDE-Spreadnotation-Leg2]
l 4: Anyintegervalueexpressedinbasis
points(forexample,57insteadof
2.57%),if[CDE-Spreadnotation-Leg
2]
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
45

---

## Page 46

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
forthebasketinsteadof
individuallegs.
59 Spreadcurrency-
Leg1
Spreadcurrency-
Leg1
Enumerated-
Code-List
Thecurrencyinwhichthe
spreadisdenominated.
Thisdataelementis
onlyapplicableifSpread
notation=1.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
60 Spreadcurrency-
Leg2
Spreadcurrency-
Leg2
Enumerated-
Code-List
Thecurrencyinwhichthe
spreadisdenominated.
Thisdataelementis
onlyapplicableifSpread
notation=1.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
46

---

## Page 47

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
61 StrikePrice StrikePrice Amount-Numeric-
31-13(Thelength
isnotfixedbutlim-
itedto18numer-
icalcharacters,
includingupto13
numericalchar-
actersafterthe
decimalpoint.)
ForoptionsotherthanFX
options(swaptionsand
similarproducts):the
priceatwhichtheowner
ofanoptioncanbuyor
selltheunderlyingasset
oftheoption.
Forforeignexchange
options,exchangerate
atwhichtheoptioncan
beexercised,expressed
astherateofexchange
fromconvertingtheunit
currencyintothequoted
currency.
Forexample,0.9426
USD/EUR,USDisthe
unitcurrencyandEUR
isthequotedcurrency;
USD1=EUR0.9426.
Forvolatilityand
varianceswapsand
similarproducts,the
volatilitystrikepriceis
reportedinthisdata
element.
l 1:Anyvalue,if[CDE-Pricenotation]
l 3:Anyvalueexpressedasdecimal(for
example,0.0257insteadof2.57%),if
[CDE-Pricenotation]
l Fortransactionswheretheswapprice
isnotknownatthetimetoexecution,
reporttheunknownswapprice-related
fieldsasblankuntilthepriceisknown.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
47

---

## Page 48

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
62 Strikepricecur-
rency/currencypair
Strikepricecur-
rency/currencypair
Enumerated-
Code-List
Forequityoptions,com-
modityoptions,andsim-
ilarproducts:thisisthe
currencyinwhichthe
strikepriceisdenom-
inated.
Forforeignexchange
options:Currencypair
andorderinwhichthe
strikepriceis
expressed.Itis
expressedasunit
currency/quoted
currency.
Forexample0.9426
USD/EUR,USDisthe
unitcurrencyandEUR
isthequotedcurrency,
USD1=EUR0.9426
TheStrike
pricecurrency/currency
pairisonlyapplicableif
Strikepricenotation=1.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
48

---

## Page 49

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
63 Post-pricedswap
indicator
Post-pricedswap
indicator
Boolean Indicatorofwhetherthe
swaptransactionsatisfies
thedefinitionof“post-
pricedswap”in§43.2(a)
oftheCommission’sreg-
ulations.
l True
l False
l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:Yes
64 Pricecurrency Pricecurrency Enumerated-
Code-List
TheCurrencyinwhichthe
priceisdenominated.
Pricecurrencyisonly
applicableifPrice
notation=1.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
65 Pricenotation Pricenotation Enumerated-
Code-List
Thisfieldisthemannerin
whichthepriceis
expressed.
1:Monetaryamount
3:Decimal
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
66 Spreadnotation-
Leg1
Spreadnotation-
Leg1
Enumerated-
Code-List
Thisfieldisthemannerin
whichthespreadis
expressed.
l 1:Monetaryamount
l 3:Decimal
l 4:Basispoints
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
49

---

## Page 50

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
67 Spreadnotation-
Leg2
Spreadnotation-
Leg2
Enumerated-
Code-List
Thisfieldisthemannerin
whichthespreadis
expressed.
l 1:Monetaryamount
l 3:Decimal
l 4:Basispoints
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
68 Strikepricenota-
tion
Strikepricenota-
tion
Enumerated-
Code-List
Thisfieldisthemannerin
whichthestrikepriceis
expressed.
l 1:Monetaryamount
l 3:Decimal
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
50

---

## Page 51

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
69 Fixedrateday
countconvention-
leg1
Fixedrateday
countconvention-
leg1
Enumerated-
Code-List
Thisfieldisthedaycount
convention(oftenalso
referredtoasdaycount
fractionordaycount
basisordaycount
method)thatdetermines
howinterestpayments
arecalculated.Itisused
tocomputetheyearfrac-
tionofthecalculation
period,andindicatesthe
numberofdaysinthecal-
culationperioddividedby
thenumberofdaysinthe
year.
l A001
l A002
l A003
l A004
l A005
l A006
l A007
l A008
l A009
l A010
l A011
l A012
l A013
l A014
l A015
l A016
l A017
l A018
l A019
l A020
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
51

---

## Page 52

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
l NARR
Foradescriptionoftheallowablevalues
seeAppendixCintheCFTCTech
Specification.
Toallowforcross-jurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1:
l 30/360:A001
l ACT/360:A004
l ACT/365.FIXED:A005
l ACT/ACT.ICMA:A006
l 30E/360.ISDA:A007
l ACT/ACT.ISDA:A008
l ACT/365L:A009
l ACT/ACT.AFB:A010
l 30E/360:A011
l ACT/ACT.ISMA:A015
l BUS/252:A018
l 1/1:A020
DTCOTCDirectConnectUser'sGuide
52

---

## Page 53

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
70 Fixedrateday
countconvention-
leg2
Fixedrateday
countconvention-
leg2
Enumerated-
Code-List Thisfieldistheday
countconvention(often
alsoreferredtoasday
countfractionorday
countbasisordaycount
method)thatdetermines
howinterestpayments
arecalculated.Itisused
tocomputetheyear
fractionofthe
calculationperiod,and
indicatesthenumberof
daysinthecalculation
perioddividedbythe
numberofdaysinthe
year.
l A001
l A002
l A003
l A004
l A005
l A006
l A007
l A008
l A009
l A010
l A011
l A012
l A013
l A014
l A015
l A016
l A017
l A018
l A019
l A020
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
53

---

## Page 54

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
l NARR
Foradescriptionoftheallowablevalues
seeAppendixCintheCFTCTech
Specification.
Toallowforcross-jurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1:
l 30/360:A001
l ACT/360:A004
l ACT/365.FIXED:A005
l ACT/ACT.ICMA:A006
l 30E/360.ISDA:A007
l ACT/ACT.ISDA:A008
l ACT/365L:A009
l ACT/ACT.AFB:A010
l 30E/360:A011
l ACT/ACT.ISMA:A015
l BUS/252:A018
l 1/1:A020
DTCOTCDirectConnectUser'sGuide
54

---

## Page 55

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
71 Floatingrateday
countconvention-
leg1
Floatingrateday
countconvention-
leg1
Enumerated-
Code-List
Thisfieldisthedaycount
convention(oftenalso
referredtoasdaycount
fractionordaycount
basisordaycount
method)thatdetermines
howinterestpayments
arecalculated.
Itisusedtocomputethe
yearfractionofthe
calculationperiod,and
indicatesthenumberof
daysinthecalculation
perioddividedbythe
numberofdaysinthe
year.
l A001
l A002
l A003
l A004
l A005
l A006
l A007
l A008
l A009
l A010
l A011
l A012
l A013
l A014
l A015
l A016
l A017
l A018
l A019
l A020
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
55

---

## Page 56

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
l NARR
Foradescriptionoftheallowablevalues
seeAppendixCintheCFTCTech
Specification.
Toallowforcross-jurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1:
l 30/360:A001
l ACT/360:A004
l ACT/365.FIXED:A005
l ACT/ACT.ICMA:A006
l 30E/360.ISDA:A007
l ACT/ACT.ISDA:A008
l ACT/365L:A009
l ACT/ACT.AFB:A010
l 30E/360:A011
l ACT/ACT.ISMA:A015
l BUS/252:A018
l 1/1:A020
DTCOTCDirectConnectUser'sGuide
56

---

## Page 57

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
72 Floatingrateday
countconvention-
leg2
Floatingrateday
countconvention-
leg2
Enumerated-
Code-List
Thisfieldisthedaycount
convention(oftenalso
referredtoasdaycount
fractionordaycount
basisordaycount
method)thatdetermines
howinterestpayments
arecalculated.
Itisusedtocomputethe
yearfractionofthe
calculationperiod,and
indicatesthenumberof
daysinthecalculation
perioddividedbythe
numberofdaysinthe
year.
l A001
l A002
l A003
l A004
l A005
l A006
l A007
l A008
l A009
l A010
l A011
l A012
l A013
l A014
l A015
l A016
l A017
l A018
l A019
l A020
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
57

---

## Page 58

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
l NARR
Foradescriptionoftheallowablevalues
seeAppendixCintheCFTCTech
Specification.
Toallowforcross-jurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1:
l 30/360:A001
l ACT/360:A004
l ACT/365.FIXED:A005
l ACT/ACT.ICMA:A006
l 30E/360.ISDA:A007
l ACT/ACT.ISDA:A008
l ACT/365L:A009
l ACT/ACT.AFB:A010
l 30E/360:A011
l ACT/ACT.ISMA:A015
l BUS/252:A018
l 1/1:A020
DTCOTCDirectConnectUser'sGuide
58

---

## Page 59

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
73 Floatingratereset
frequencyperiod-
leg1
Floatingratereset
frequencyperiod-
leg1
Enumerated-
Code-List
Thetimeunitassociated
withthefrequencyof
resets(e.g.day,week,
month,yearortermofthe
stream).
l DAIL:Daily
l WEEK:Weekly
l MNTH:Monthly
l YEAR:Yearly
l ADHO:Adhoc;applieswhenpay-
mentsareirregular
l EXPI:Paymentatterm
Toallowforcrossjurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1asbelow:
l D:DAIL:Daily
l W:WEEK:Weekly
l M:MNTH:Monthly
l Y:YEAR:Yearly
l T:EXPI:Paymentatterm(ForFpML,
onlywhentheschemawillalsoallowT)
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
59

---

## Page 60

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
74 Floatingratereset
frequencyperiod-
leg2
Floatingratereset
frequencyperiod-
leg2
Enumerated-
Code-List Thetimeunitassociated
withthefrequencyof
resets(e.g.day,week,
month,yearortermof
thestream).
l DAIL:Daily
l WEEK:Weekly
l MNTH:Monthly
l YEAR:Yearly
l ADHO:Adhoc;applieswhenpay-
mentsareirregular
l EXPI:Paymentatterm
Toallowforcrossjurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1asbelow:
l D:DAIL:Daily
l W:WEEK:Weekly
l M:MNTH:Monthly
l Y:YEAR:Yearly
l T:EXPI:Paymentatterm(ForFpML,
onlywhentheschemawillalsoallowT)
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
60

---

## Page 61

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
75 Floatingratereset
frequencyperiod
multiplier-leg1
Floatingratereset
frequencyperiod
multiplier-leg1
Amount-Numeric-
3-0 Thenumberoftime
units(asexpressedby
theFloatingratereset
frequencyperiod)that
determinesthe
frequencyatwhich
periodicpaymentdates
forresetoccur.
Forexample,a
transactionwithreset
paymentsoccurring
everytwomonthsis
representedwitha
Floatingratereset
frequencyperiodof
“MNTH”(monthly)anda
Floatingratereset
frequencyperiod
multiplierof2.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
61

---

## Page 62

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
76 Floatingratereset
frequencyperiod
multiplier-leg2
Floatingratereset
frequencyperiod
multiplier-leg2
Amount-Numeric-
3-0
Thenumberoftimeunits
(asexpressedbythe
Floatingrateresetfre-
quencyperiod)that
determinesthefrequency
atwhichperiodicpayment
datesforresetoccur.
Forexample,a
transactionwithreset
paymentsoccurring
everytwomonthsis
representedwitha
Floatingratereset
frequencyperiodof
“MNTH”(monthly)anda
Floatingratereset
frequencyperiod
multiplierof2.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
77 Otherpayment
amount
Otherpayment
amount
Monetary-
Numeric-30-5(The
lengthisnotfixed
butlimitedto25
numericalchar-
actersincludingup
tofivenumerical
charactersafter
thedecimalpoint.)
Thisfieldshowspayment
amountswithcor-
respondingpayment
typestoaccommodate
requirementsoftrans-
actiondescriptionsfrom
differentassetclasses.
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
62

---

## Page 63

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
78 Fixedratepayment
frequencyperiod-
Leg1
Fixedratepayment
frequencyperiod-
Leg1
Enumerated-
Code-List
Thetimeunitassociated
withthefrequencyofpay-
ments(e.g.,day,week,
monthyearortermofthe
stream).
Forexample,to
representquarterly
payment([Payment
frequencyperiod]=
‘MNTH’and[Payment
frequencyperiod
multiplier]=‘3’)isused.
Forsemi-annual
payment,[Payment
frequencyperiod]=
‘MNTH’and([Payment
frequencyperiod
multiplier]=‘6’)isused.
l DAIL:Daily
l WEEK:Weekly
l MNTH:Monthly
l YEAR:Yearly
l ADHO:Adhoc;applieswhenpay-
mentsareirregular
l EXPI:Paymentatterm
Toallowforcrossjurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1asbelow:
l D:DAIL:Daily
l W:WEEK:Weekly
l M:MNTH:Monthly
l Y:YEAR:Yearly
l T:EXPI:Paymentatterm(ForFpML,
onlywhentheschemawillalsoallowT)
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
63

---

## Page 64

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
79 Floatingratepay-
mentfrequency
period-Leg1
Floatingratepay-
mentfrequency
period-Leg1
Enumerated-
Code-List
Thetimeunitassociated
withthefrequencyofpay-
ments(e.g.,day,week,
month,yearortermofthe
stream).
Forexample,to
representquarterly
paymentreport
[Paymentfrequency
period]=‘MNTH’and
([Paymentfrequency
periodmultiplier]=‘3’)is
used.Forsemi-annual
payment,report
([Paymentfrequency
period]=‘MNTH’and
[Paymentfrequency
periodmultiplier]=‘6’)is
used.
l DAIL:Daily
l WEEK:Weekly
l MNTH:Monthly
l YEAR:Yearly
l ADHO:Adhoc;applieswhenpay-
mentsareirregular
l EXPI:Paymentatterm
Toallowforcrossjurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1asbelow:
l D:DAIL:Daily
l W:WEEK:Weekly
l M:MNTH:Monthly
l Y:YEAR:Yearly
l T:EXPI:Paymentatterm(ForFpML,
onlywhentheschemawillalsoallowT)
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
64

---

## Page 65

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
80 Fixedratepayment
frequencyperiod-
Leg2
Fixedratepayment
frequencyperiod-
Leg2
Enumerated-
Code-List
Thetimeunitassociated
withthefrequencyofpay-
ments(e.g.,day,week,
month,yearortermofthe
stream).
Forexample,to
representquarterly
paymentreport
[Paymentfrequency
period]=‘MNTH’and
([Paymentfrequency
periodmultiplier]=‘3’)is
used.Forsemi-annual
payment,report
([Paymentfrequency
period]=‘MNTH’and
[Paymentfrequency
periodmultiplier]=‘6’)is
used.
l DAIL:Daily
l WEEK:Weekly
l MNTH:Monthly
l YEAR:Yearly
l ADHO:Adhoc;applieswhenpay-
mentsareirregular
l EXPI:Paymentatterm
Toallowforcrossjurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1asbelow:
l D:DAIL:Daily
l W:WEEK:Weekly
l M:MNTH:Monthly
l Y:YEAR:Yearly
l T:EXPI:Paymentatterm(ForFpML,
onlywhentheschemawillalsoallowT)
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
65

---

## Page 66

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
81 Floatingratepay-
mentfrequency
period-Leg2
Floatingratepay-
mentfrequency
period-Leg2
Enumerated-
Code-List
Thetimeunitassociated
withthefrequencyofpay-
ments(e.g.,day,week,
month,yearortermofthe
stream).
Forexample,to
representquarterly
paymentreport
[Paymentfrequency
period]=‘MNTH’and
([Paymentfrequency
periodmultiplier]=‘3’)is
used.Forsemi-annual
payment,report
([Paymentfrequency
period]=‘MNTH’and
[Paymentfrequency
periodmultiplier]=‘6’)is
used.
l DAIL:Daily
l WEEK:Weekly
l MNTH:Monthly
l YEAR:Yearly
l ADHO:Adhoc;applieswhenpay-
mentsareirregular
l EXPI:Paymentatterm
Toallowforcrossjurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1asbelow:
l D:DAIL:Daily
l W:WEEK:Weekly
l M:MNTH:Monthly
l Y:YEAR:Yearly
l T:EXPI:Paymentatterm(ForFpML,
onlywhentheschemawillalsoallowT)
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
66

---

## Page 67

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
82 Fixedratepayment
frequencyperiod
multiplier-Leg1
Fixedratepayment
frequencyperiod
multiplier-Leg1
Multiplier-Numeric-
3-0
Thisfieldisthenumberof
timeunits(asexpressed
bythePaymentfre-
quencyperiod)that
determinesthefrequency
atwhichperiodicpayment
datesoccur.
Forexample,a
transactionwith
paymentsoccurring
everytwomonthsis
representedwitha
Paymentfrequency
periodof“MNTH”
(monthly)anda
Paymentfrequency
periodmultiplierof2.
Thisdataelementisnot
applicableifthe
Paymentfrequency
periodis“ADHO.”
IfPaymentfrequency
periodis“EXPI”,then
thePaymentfrequency
periodmultiplieris1.
IfthePayment
frequencyisintraday,
thenthePayment
frequencyperiodis
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
67

---

## Page 68

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
“DAIL”andthePayment
frequencymultiplieris0.
DTCOTCDirectConnectUser'sGuide
68

---

## Page 69

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
83 Floatingratepay-
mentfrequency
periodmultiplier-
Leg1
Floatingratepay-
mentfrequency
periodmultiplier-
Leg1
Multiplier-Numeric-
3-0
Thisfieldisthenumberof
timeunits(asexpressed
bythePaymentfre-
quencyperiod)that
determinesthefrequency
atwhichperiodicpayment
datesoccur.
Forexample,a
transactionwith
paymentsoccurring
everytwomonthsis
representedwitha
Paymentfrequency
periodof“MNTH”
(monthly)anda
Paymentfrequency
periodmultiplierof2.
Thisdataelementisnot
applicableifthe
Paymentfrequency
periodis“ADHO.”
IfPaymentfrequency
periodis“EXPI”,then
thePaymentfrequency
periodmultiplieris1.
IfthePayment
frequencyisintraday,
thenthePayment
frequencyperiodis
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
69

---

## Page 70

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
“DAIL”andthePayment
frequencymultiplieris0.
DTCOTCDirectConnectUser'sGuide
70

---

## Page 71

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
84 Fixedratepayment
frequencyperiod
multiplier-Leg2
Fixedratepayment
frequencyperiod
multiplier-Leg2
Multiplier-Numeric-
3-0
Thenumberoftimeunits
(asexpressedbythePay-
mentfrequencyperiod)
thatdeterminethefre-
quencyatwhichperiodic
paymentdatesoccur.
Forexample,a
transactionwith
paymentsoccurring
everytwomonthsis
representedwitha
Paymentfrequency
periodof“MNTH”
(monthly)anda
Paymentfrequency
periodmultiplierof2.
Thisdataelementisnot
applicableifthe
Paymentfrequency
periodis“ADHO.”Ifthe
Paymentfrequency
periodis“EXPI”,the
Paymentfrequency
periodmultiplieris1.If
thePaymentfrequency
isintraday,thePayment
frequencyperiodis
"DAIL"andthePayment
frequencymultiplieris
0.“DAIL”andthe
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
71

---

## Page 72

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
Paymentfrequency
multiplieris0.
DTCOTCDirectConnectUser'sGuide
72

---

## Page 73

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
85 Floatingratepay-
mentfrequency
periodmultiplier-
Leg2
Floatingratepay-
mentfrequency
periodmultiplier-
Leg2
Multiplier-Numeric-
3-0 Thisfieldisthenumber
oftimeunits(as
expressedbythe
Paymentfrequency
period)thatdetermines
thefrequencyatwhich
periodicpaymentdates
occur.
Forexample,a
transactionwith
paymentsoccurring
everytwomonthsis
representedwitha
Paymentfrequency
periodof“MNTH”
(monthly)anda
Paymentfrequency
periodmultiplierof2.
Thisdataelementisnot
applicableifthe
Paymentfrequency
periodis“ADHO.”
IfPaymentfrequency
periodis“EXPI”,then
thePaymentfrequency
periodmultiplieris1.
IfthePayment
frequencyisintraday,
Anyvaluegreaterthanorequaltozero. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
73

---

## Page 74

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
thenthePayment
frequencyperiodis
“DAIL”andthePayment
frequencymultiplieris0.
86 Otherpayment
type
Otherpayment
type
Enumerated-
Code-List
TheTypeofOtherpay-
mentamount.
Optionpremium
paymentisnot
consideredasa
paymenttypeas
premiumsforoptions
areshownintheoption
premiumdedicateddata
element.
l UFRO:UpfrontPayment.Forexample,
theinitialpaymentmadebyoneofthe
counterparties,eithertobringatrans-
actiontofairvalueorforanyother
reasonthatmaybethecauseofanoff
markettransaction.
l UWIN: UnwindorFulltermination,that
is,thefinalsettlementpaymentmade
whenatransactionisunwoundpriorto
itsenddate;Paymentsthatmayresult
duetofullterminationofderivative
transaction(s)
l PEXH: PrincipalExchange,thatis,
Exchangeofnotionalvaluesforcross-
currencyswaps
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
87 Otherpaymentcur-
rency
Otherpaymentcur-
rency
Enumerated-
Code-List
Thecurrencyinwhich
Otherpaymentamountis
denominated.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
74

---

## Page 75

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
88 Settlementcur-
rency-Leg1
Settlementcur-
rency-Leg1
Enumerated-
Code-List
Thecurrencyforthecash
settlementofthetrans-
action.
Formulti-currency
productsthatdonotnet,
thisshowsthe
settlementcurrencyof
eachleg.
Thisdataelementisnot
applicabletophysically
settledproducts(e.g.,
physicallysettled
swaptions).
ISO4217CurrencyCodes. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
89 Settlementcur-
rency-Leg2
Settlementcur-
rency-Leg2
Enumerated-
Code-List
Thecurrencyforthecash
settlementofthetrans-
action.
Formulti-currency
productsthatdonotnet,
thisshowsthe
settlementcurrencyof
eachleg.
Thisdataelementisnot
applicabletophysically
settledproducts(e.g.,
physicallysettled
swaptions).
ISO4217CurrencyCodes. l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
75

---

## Page 76

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
90 Settlementloc-
ation-Leg1 [[settlement]]
location
FieldName
Changed
Enumerated-
Code-List
Theplaceofsettlementof
thetransactionasstip-
ulatedinthecontract.
Thisdataelementis
onlyapplicablefor
transactionsthatinvolve
anoffshorecurrency
(i.e.acurrencywhichis
notincludedintheISO
4217currencylist,for
exampleCNH).
Two-characterISO3166Countrycodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
91 Settlementloc-
ation-Leg2 [[settlement]]
location-Leg2
FieldNoLonger
Used
Enumerated-
Code-List
Theplaceofsettlementof
thetransactionasstip-
ulatedinthecontract.Itis
onlyapplicabletotrans-
actionsthatinvolvesan
offshorecurrency.These
currenciesarenot
includedintheISO4217
currencylist,forexample
CNH).
Two-characterISO3166Countrycodes l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
76

---

## Page 77

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
92 Collateralisation
category
Collateralisation
category
Enumerated-
Code-List
Indicatorofwhetheracol-
lateralagreement(s)
betweenthecoun-
terpartiesexist(uncol-
lateralised/partially
collateralised/one-waycol-
lateralised/fullycol-
lateralised).Thisdata
elementisprovidedfor
eachtransactionoreach
portfolio,dependingon
whetherthecol-
lateralisationisperformed
atthetransactionlevelor
attheportfoliolevel.This
fieldisapplicabletoboth
clearedanduncleared
transactions.
l UNCL
l PRC1
l PRC2
l PRCL
l OWC1
l OWC2
l OWP1
l OWP2
l FLCL
Thenamesanddefinitionsforthese
allowablevaluesareprovidedin
AppendixEoftheCFTCTechnical
Specification.
Toallowforcross-jurisdictional
submissions,thefollowingvalueswillbe
acceptedandmapped1:1:
l UNCOLLATERALIZED:UNCL
l PARTIAL:PRCL
l FULLY:FLCL
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
77

---

## Page 78

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
93 Custombasket
indicator
Custombasket
indicator
Boolean Indicatorofwhetherthe
swaptransactionisbased
onacustombasket.
l True
l False
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
94 Indexfactor Indexfactor Monetary-
Numeric-21-10
Thelengthisnot
fixed,butis
limitedto11
numerical
characters,
includingupto
tennumerical
charactersafter
thedecimalpoint.
Theindexversionfactor
orpercent.Itisexpressed
asadecimalvaluethat,
multipliedbytheNotional
amountyieldsthe
notionalamountcovered
bythesellerofprotection
forthecreditdefault
swap.
Anyvaluebetween0and1(including0
and1),expressedindecimalformat(for
example,0.05insteadof5%).
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
95 UnderlierID-Leg1 UnderlierID-Leg1 [[ID]]-Text-200 UPIRDL:Anidentifier
thatsedtodeterminethe
[[Asset]](s),index(indices)
orbenchmarkunderlying
acontract.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
78

---

## Page 79

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
96 UnderlierID-Leg2 UnderlierID-Leg2 Enumerated-
Code-List
UPIRDL:Anidentifier
usedtodeterminethe
[[Asset]](s),index(indices),
orbenchmarkunderlying
thecontract.
l Agricultural
l Benzene
l Bullion
l Coal
l Composite
l Commodity
l Indices
l Diesel
l Fuel
l Electricity
l Emissions
l Allowances
l EthanolandBioFuels
l FuelOil
l FreightGasOil
l GasolineHeatingOil
l JetFuel
l Kerosene
l Metals
l Methanol
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
79

---

## Page 80

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
l Naptha
l NaturalGas
l NGL
l Oil
l Paper
l Plastic
l Weather
DTCOTCDirectConnectUser'sGuide
80

---

## Page 81

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
97 UnderlierID
source-Leg1
UnderlierID
source-Leg1
Enumerated-
Code-List
UPIRDL:Theorigin,or
publisher,oftheasso-
ciatedunderlierID.
l Basket
l Bloomberg
l [[CUSIP]]
l Index
l REDID
l ISIN
l LEI
l RIC
l SEDOL
l SingleOther
l Valoren
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
98 UnderlyingAsset
Name
UnderlyingAsset
Name
FreeFormat-Text-
100
Thenameoftheunder-
lyingasset.Requiredfor
multi-jurisdictionreporting
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
81

---

## Page 82

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
99 Underlyingasset
subtypeorunder-
lyingcontractsub-
type-Leg1
Underlyingasset
subtypeorunder-
lyingcontractsub-
type-Leg1
FreeFormat-Text-
150
UPIRDL:Alower-level
descriptionofthechar-
acteristicsofanassetor
contractunderlyingthe
derivative;requiredfor
CFTCPPDtime-delaycal-
culations.
AnyvaluethattheReportingPartyhas
submitted.Novalidationwasperformed
onthevalueentered.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
100 Underlyingasset
subtypeorunder-
lyingcontractsub-
type-Leg2
Underlyingasset
subtypeorunder-
lyingcontractsub-
type-Leg2
FreeFormat-Text-
150
UPIRDL:Alower-level
descriptionofthechar-
acteristicsofanassetor
contractunderlyingthe
derivative;requiredfor
CFTCPPDtime-delaycal-
culations.
AnyvaluethattheReportingPartyhas
submitted.Novalidationwasperformed
onthevalueentered.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
DTCOTCDirectConnectUser'sGuide
82

---

## Page 83

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
101 EmbeddedOption
type
EmbeddedOption
type
Enumerated-
Code-List
Thetypeofoptionor
optionalprovisionembed-
dedinthecontract.
l MDET:Mandatoryearlytermination
l OPET:Optionalearlytermination
l CANC:Cancelable
l EXTD:Extendible
l OTHR:OtherT
Toallowforcross-jurisdictional
submissions,thefollowingvaluesare
acceptedandmapped1:1:
l CancelableProvision:CANC
l ExtendibleProvision:EXTD
l MandatoryEarlyTermination:MDET
l OptionalEarlyTerminationProvision:
OPET
l Other:OTHR
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
83

---

## Page 84

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
102 OptionType OptionType Enumerated-
Code-List
Thetypeofoptionbeing
reported.
l Put
l Call
l Payer
l Receiver
l Straddle
l NonStandard
l Other
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
103 OptionStyle OptionStyle Enumerated-
Code-List
Indicatestheoptionstyle
thatenablestheGTRser-
vicetodeterminetheexer-
cisedates.
l American
l Asian
l Bermudan
l European
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
104 PackageindicatorPackageindicatorBoolean Indicatorofwhetherthe
swaptransactionispartof
apackagetransaction.
l True
l False
l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
84

---

## Page 85

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
105 Packagetrans-
actionprice
Packagetrans-
actionprice Amount-
Numeric-31-13
Note: Thelength
isnotfixed,butis
limitedto18
numerical
characters,
includingupto13
numerical
charactersafter
thedecimalpoint.
Thetradedpriceofthe
entirepackageinwhich
thereportedderivative
transactionisacom-
ponent.
Note: Thisdataelement
isnotapplicableifno
packagewasinvolved
orthepackage
transactionspreadwas
used.Pricesandthe
transaction'related
elements(Price
currency,Pricenotation,
Priceunitofmeasure)
thatrepresentindividual
componentsofthe
packagearereported
whenavailable.The
Packagetransaction
pricemaynotbeknown
whenanewtransaction
isreportedbutmaybe
updatedlater.
l 1:Anyvalue,if[CDE-Packagetrans-
actionpricenotation]
l 3:Anyvalueexpressedasdecimal
(e.g.,0.0257insteadof2.57%),if[CDE
-Packagetransactionpricenotation]
l Defaultvaluewithall9s,foranyofthe
allowableformats,isacceptedwhen
thevalueisunknown.When[CDE-
Packagetransactionpricenotation]:‘1’
use“99999.9999999999999”(18
numericalcharactersincluding13
decimalplaces).When[CDE-Package
transactionpricenotation]:‘3’use
“9.9999999999”(11numericalchar-
actersincluding10decimalplaces).
l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
85

---

## Page 86

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
106 Packagetrans-
actionpricecur-
rency
Packagetrans-
actionpricecur-
rency
Enumerated-
Code-List
Thecurrencyinwhichthe
Packagetransactionprice
isdenominated.
Note: Thisdataelement
isnotapplicableifno
packagewasinvolved,if
thePackagetransaction
pricewasused,orifthe
Packagetransaction
pricenotation=3.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:Yes
107 Packagetrans-
actionpricenota-
tion
Packagetrans-
actionpricenota-
tion
Enumerated-
Code-List
Themannerinwhichthe
Packagetransactionprice
isexpressed.
Note: Thisdataelement
isnotapplicableifno
packagewasinvolved
orifthePackage
transactionpricewas
used.
l 1:Monetaryamount
l 3:Decimal
l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
86

---

## Page 87

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
108 Packagetrans-
actionspread
Packagetrans-
actionspread Amount-
Numeric-31-13.
Note: Thelength
isnotfixed,butis
limitedto18
numerical
characters,
includingupto13
numerical
charactersafter
thedecimalpoint.
l TheTradedpriceof
theentirepackagein
whichthereported
derivativetransaction
wasacomponentofa
packagetransaction.
l ThePackagetrans-
actionpricewhenthe
priceofthepackageis
expressedasaspread
differencebetween
tworeferenceprices.
l TheSpreadand
relateddataelements
ofthetransactions
(spreadcurrency,
Spreadnotation)that
representindividual
componentsofthe
packagearereported
whenavailable.Pack-
agetransaction
spreadmaynotbe
knownwhenanew
transactionisreported
butmaybeupdated
later."
Note: Thisdataelement
l 1:Anyvalue,if[CDE-Packagetrans-
actionpricenotation]
l 3:Anyvalueexpressedasdecimal
(e.g.,0.0257insteadof2.57%),if[CDE
-Packagetransactionpricenotation]
l Defaultvaluewithall9s,foranyofthe
allowableformats,isacceptedwhen
thevalueisunknown.
o When[CDE-Packagetrans-
actionpricenotation]:‘1’use
“99999.9999999999999”(18
numericalcharactersincluding
13decimalplaces).
o When[CDE-Packagetrans-
actionpricenotation]:‘3’use
“9.9999999999”(11numerical
charactersincluding10decimal
places).
l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
87

---

## Page 88

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
isnotapplicableifno
packagewasinvolved
orifthePackage
transactionpricewas
used.
109 Packagetrans-
actionspreadcur-
rency
Packagetrans-
actionspreadcur-
rency
Enumerated-
Code-List
Thecurrencyinwhichthe
Packagetransaction
spreadisdenominated.
ISO4217CurrencyCodes l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:Yes
110 Packagetrans-
actionspreadnota-
tion
Packagetrans-
actionspreadnota-
tion
Enumerated-
Code-List
MannerinwhichthePack-
agetransactionspreadis
expressed.
Thisdataelementisnot
applicableifnopackage
wasinvolvedorifthe
Packagetransaction
pricewasused.
l 1:Monetaryamount
l 3:Decimal
l 4:Basispoints
l [[CFTC]]:
Yes
l Canada:
No
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
88

---

## Page 89

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
111 Physicaldelivery
location-Leg1
Physicaldelivery
location-Leg1
Freeformat-Text-
40
Thedeliverylocation. 0 l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:No
112 DeliveryType DeliveryType Enumerated-
Code-List
UPIRDL:Indicates
whetherthederivatives
contractdeliveredaphys-
icalassetoracashequi-
valentatsettlement.
l Cash
l CashOrPhysical
l Election
l NotApplicable
l Optional
l Physical
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
113 N/A UPI
NewField
[[ID]]-Text-12 ISO4914Uniqueproduct
identifierAlistofallow-
ablevaluesandtheir
formatwillbepublished
bytheUPIissuer.(DSB
ANNA)Mustbeavalid
UPIasperANNADSB.
l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
DTCOTCDirectConnectUser'sGuide
89

---

## Page 90

CSV
Position
DataElement
(Rewrite)
DataElement
(Phase2Rewrite)
DataType Definition PossibleValues Jurisdiction
Applicability
114 N/A UPI-ShortName
(FISN)
NewField
Freeformat-Text-
500
ReportedbyGTRbased
onUPIvalue AsgeneratedbyGTR l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
115 N/A UPI-Underlier
Name
NewField
Freeformat-Text-
500
ReportedbyGTRbased
onUPIvalue
AsgeneratedbyGTR l [[CFTC]]:
Yes
l Canada:
Yes
l [[SEC]]:Yes
UpdatesforNorthAmericaPhase2Rewrite
FieldsDecommissionedforNorthAmericaPhase2Rewrite FieldsAddedforNorthAmericaPhase2Rewrite
OutboundField OutboundField
Callamount-Leg2 UniqueProductIdentifier
Callcurrency-Leg2 UPI-ShortName(FISN)
Putamount-Leg2 UPIUnderlierName
Putcurrency-Leg2
Settlementlocation-Leg2 
DTCOTCDirectConnectUser'sGuide
90

---

## Page 91

FORMOREINFORMATION
EmailDTCCLearningat:
DataLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com