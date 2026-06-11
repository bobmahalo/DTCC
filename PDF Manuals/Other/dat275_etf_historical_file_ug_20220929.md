---
title: "ETF Portfolio Data Service - Historical File User's Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat275_etf_historical_file_ug_20220929.pdf"
pages: 16
size: "1186.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ETF Portfolio Data Service - Historical File User's Guide

**Original File:** [dat275_etf_historical_file_ug_20220929.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat275_etf_historical_file_ug_20220929.pdf)  
**Category:** Other  
**Total Pages:** 16  
**File Size:** 1186.4 KB  

---

## Page 1

ETFPORTFOLIOSERVICE
HISTORICALFILEUSER'SGUIDE
SEPTEMBER29,2022


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
DocInfo:September29,2022
PublicationCode:DAT276
Service:ETFPortfolioService
Title:HistoricalFileUser'sGuide

---

## Page 3

3
TABLEOFCONTENTS
HistoricalPortfolioMROFileLayout:AutoRoute02262222 4
Type1–HeaderRecord 4
Type2–PortfolioHeaderRecord 5
Type3–ComponentDetailRecord 10
Type99–TrailerRecord 15
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 4

HistoricalPortfolioMROFileLayout:AutoRoute02262222 4
HISTORICALPORTFOLIOMROFILELAYOUT:AUTOROUTE02262222
ThefollowingsectionscontaintheinformationfortheHistoricalPortfolioMROFileLayout:AutoRoute02262222record
layout.
Type1–HeaderRecord
ThefollowingtableshowtheType1–HeaderRecorddetailsfortheHistoricalPortfolioMROFileLayout:AutoRoute
02262222recordlayout:
AutoRoute02262222
Type1–HeaderRecord
Recordlength=500
Seq Description Length Start Type Comments
1 RecordType 2 1 A/N 01=HeaderRecord
Oneperfile
2 FileDescription25 3 A/N HISTORICALETFPORTFOLIOS
3 CustomerNum-
ber
8 28 N CustomerNumber
4 FileIdentifier 8 36 A/N Insertfirsteight(startingfromtheright)charactersoftheRequestIDfrom
TBETF14_PTFLO_RQST_HIST.
5 NSCCPro-
cessingDate
8 44 N CCYYMMDD
6 NSCCPro-
cessingTime
6 52 N HHMMSS
7 FutureUse 443 58 Spaces.
ENDOFRECORD
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 5

HistoricalPortfolioMROFileLayout:AutoRoute02262222 5
Type2–PortfolioHeaderRecord
ThefollowingtableshowtheType2–PortfolioHeaderRecorddetailsfortheHistoricalPortfolioMROFileLayout:
AutoRoute02262222recordlayout:
AutoRoute02262222
Type2–PortfolioHeaderRecord
Recordlength=500
Seq Description Length Start Type Comments
1 RecordType 2 1 A/N 02=RecordType2
OneperPortfolio
2 ETFTradingCUSIP 9 3 A/N S&PAssigned
3 ETFTradingISIN 12 12 A/N
4 NSCCPortfolioID 9 24 A/N NSCCassignedPortfolioIDofthebasket.
5 ETFDescription 60 33 A/N FromtheSecurityMasterfile,iffound;otherwise,theETFagent
supplieddescriptionisused.
6 PortfolioTradeDate 8 93 N CCYYMMDD
7 ETFAgent 8 101 N NSCCMemberNumber
8 ComponentCount 8 109 N 99,999,999
9 EstimatedT-1Cash
AmountPerCreation
Unit
14 117 N 999,999,999,999.99
10 SignfieldforEstimated
T-1CashAmountPer
CreationUnit
1 131 A/N "-"indicatesnegativevalue
Space=PositiveValue
11 NetAssetValuePer
CreationUnit
18 132 N 999,999,999,999.999999
Decimalplaceexpandsto6digits
12 SignfieldforNetAsset
ValuePerCreationUnit
1 150 A/N "-"indicatesnegativevalue
Space=PositiveValue
13 EstimatedT-1Cash
AmountPerETF
14 151 N 999,999,999,999.99
14 SignfieldforEstimated
T-1CashAmountPer
[[ETF]]
1 165 A/N "-"indicatesnegativevalue
Space=PositiveValue
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 6

HistoricalPortfolioMROFileLayout:AutoRoute02262222 6
AutoRoute02262222
Type2–PortfolioHeaderRecord
Recordlength=500
Seq Description Length Start Type Comments
15 NetAssetValuePer
[[ETF]]
18 166 N 999,999,999,999.999999
Decimalplaceexpandsto6digits.
16 SignfieldforNetAsset
ValuePerETF
1 184 A/N "-"indicatesnegativevalue
Space=PositiveValue
17 TotalCashAmountPer
CreationUnit
14 185 N 999,999,999,999.99
18 SignfieldforTotalCash
AmountPerCreation
Unit
1 199 A/N "-"indicatesnegativevalue
Space=PositiveValue
19 TotalSharesOut-
standingPerETFonT-1
12 200 N 999,999,999,999
20 DividendAmountPer
ETFonT-1
14 212 N 999,999,999,999.99
21 SignfieldforDividend
AmountPerETFonT-1
1 226 A/N "-"indicatesnegativevalue
Space=PositiveValue
22 EstimatedValueofcash-
in-lieuComponentsper
CreationUnit
14 227 N 999,999,999,999.99
23 CashOnlyIndicator 1 241 A/N l Y=CashOnly(create/redeemwithCashOnly)
l Space=Norestrictions(anycombinationofcashor
[[securities]])
24 ETFExpenseRatioon
T-1
3 242 N ExpressedinBasisPoints
25 TotalAssetValueofETF
FundonT-1
18 245 N 999,999,999,999.999999
Decimalplaceexpandsto6digits.
26 ETFSharesPer
Create/RedeemUnits
9 263 N 999,999,999-fromSecurityMaster
27 ETFSymbol 15 272 A/N FromSecurityMaster
28 CNSEligibilityIndicator 1 287 A/N FromSecurityMaster
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 7

HistoricalPortfolioMROFileLayout:AutoRoute02262222 7
AutoRoute02262222
Type2–PortfolioHeaderRecord
Recordlength=500
Seq Description Length Start Type Comments
29 ETFCreateRedeem
Identifier
1 288 A/N l Y=Basketcanbecreatedorredeemed
l N=Basketcannotbecreatedorredeemed
30 PriorDay'sPortfolio
beingused
1 289 A/N l Space=Today'sportfoliobeingused
l Y=Priorday'sportfoliobeingused
31 BasketType 2 290 A/N l 01=Standard
l 02=Restricted
l 03=Pricing
l 04=Rebalance
l 05=CreateOnly
l 06=RedeemOnly
l 07=Negotiated
32 ForeignorDomestic 1 292 A/N l D=Domestic
l F=Foreign
33 NSCCNewPortfolio 1 293 A/N l Y=Newportfolio
l Space=existingportfolio
34 ETFClassificationCode 6 294 A/N ForfutureusetoclassifyETFs.
35 ETFBasketUnitSize 9 300 N DefinesthesizeofthisbasketthatisdifferentfromtheETF
CreationUnitsize.SpecifiedonlyonRebalancebaskets.
Optional.Allzeroesifnotprovided.
999,999,999
36 VariableFees 8 309 N 999,999.99
37 BabyBondCashValue 10 317 N 99,999,999.99
38 FixedIncomeFace
ValueAdjustment
10 327 N 99,999,999.99
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 8

HistoricalPortfolioMROFileLayout:AutoRoute02262222 8
AutoRoute02262222
Type2–PortfolioHeaderRecord
Recordlength=500
Seq Description Length Start Type Comments
39 AssetClassification
CodeforUnderlying
Components
2 337 A/N Assetclassificationcode:
l 01=[[Equity]]
l 02=FixedIncome
l 03=Commodity
l 04=MixedAsset
l 05=Alternative
l 06=Currency
40 LeverageIndicatorCode 2 339 A/N l 01=Unleveraged
l 02=Leveraged
l 03=InverseLeveraged
41 LeverageFactor 4 341 A/N 99.99
42 TransferAgentID 8 345 N TransferagentID.
43 TransferAgentName 48 353 A/N Nameofthetransferagent.
44 FundLEI 20 401 A/N Legalentityidentifierofthefund.
45 FundSize 23 421 N FundAUM,attheshareclassorproductlevel.
99,999,999,999.999999999999
46 ShareClassAppor-
tionmentRatio
1 444 N Identifiesifthefundhasshareclassesandtheproportional
ownershipofthefundifithasshareclasses.
ForU.S.,ETFsalways=1.
Spaceifnotprovided.
47 ProjectedTransaction
Fee
7 445 N EMEA-specific:estimatedtransactionfee.
99,999.99
48 DateforProjectedTrans-
actionFee
8 452 N Effectivetradedateofthebasket,inCCYYMMDDformat.
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 9

HistoricalPortfolioMROFileLayout:AutoRoute02262222 9
AutoRoute02262222
Type2–PortfolioHeaderRecord
Recordlength=500
Seq Description Length Start Type Comments
49 ConfirmedTransaction
Fee
7 460 N Actualcostofthetransaction-alsoknownasthe
Create/Redeemfee.
99,999.99
50 DateforConfirmed
TransactionFee
8 467 N Effectivetradedateofthebasket,inCCYYMMDDformat.
51 ProjectedCashforPri-
cingBasket
14 475 N Projectedcashfigurefortradedatebasedonpricingbasket.
999,999,999,999.99
52 BasketsOutstanding 6 489 N Numberofbasket/unitsoutstandinginthefund,attheshare
classorproductlevel.
999999
53 PricingUsageIndicator 1 495 A(Y,
N)
l Y=StandardbaskettobeusedasaPricingbasket.
l N=FullFundPricingbasketwillbesubmittedforthis
fund.
l Space=DefaultstoY.
54 CreationOrderUsage 1 496 A(Y,
N)
l Y=StandardNSCCInstructionIDtobeusedforstand-
ardandcreationorders.
l N=CreateOnlybasket(baskettype05)willbesubmitted
andpublishedonETFoutput.TheNSCCPortfolioID
associatedwiththetype05basketisusedforcreation
orders.
l Space=DefaultstoY
55 RedemptionOrder
Usage
1 497 A(Y,
N)
l Y=StandardNSCCInstructionIDtobeusedforstand-
ardandredemptionorders.
l N=RedeemOnlybasket(baskettype06)willbesub-
mittedandpublishedonETFoutput.TheNSCCPortfolio
IDassociatedwiththetype06basketisusedforredemp-
tionorders.
l Space=DefaultstoY.
56 FutureUse 3 498 Spaces.
ENDOFRECORD
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 10

HistoricalPortfolioMROFileLayout:AutoRoute02262222 10
Type3–ComponentDetailRecord
ThefollowingtableshowtheType3–ComponentDetailRecordinformationfortheHistoricalPortfolioMROFileLayout:
AutoRoute02262222recordlayout:
AutoRoute02262222
Type3–ComponentDetailRecord
Recordlength=500
Seq Description Length Start Type Comments
1 RecordType 2 1 A/N 03=RecordType3
2 ETFTradingCUSIP 9 3 A/N S&PAssigned
3 ETFTradingISIN 12 12 A/N
4 NSCCPortfolioID 9 24 A/N NSCCassignedPortfolioIDofthebasket
5 PortfolioTradeDate 8 33 N CCYYMMDD
6 ComponentIDCode 2 41 A/N l 01=[[CUSIP]]
l 02=Sedol
l 03=ISIN
l 04=ISIN/Sedol
l 05=Bloomberg
l 06=Reuters
l 07=NYSELife
l 99=Other
7 ComponentID 25 43 ThisisdefinedbythevalueinComponentIDCodefield
l CUSIPNumber 9 43 A/N IdentifiesDomesticcomponent
l Sedol 7 43 A/N OfficialSedolnumber
l ISIN/Sedol 19 43 CombinationISIN/
SEDOLnumber.
Recommended
fornon-US
domiciled
[[securities]].
o ISINNumber 12 43 A/N IdentifiesForeigncomponent
o SedolNumber7 55 A/N OfficialSedolnumber
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 11

HistoricalPortfolioMROFileLayout:AutoRoute02262222 11
AutoRoute02262222
Type3–ComponentDetailRecord
Recordlength=500
Seq Description Length Start Type Comments
l Allothertypes 25 43 A/N Freeformfieldidentifyingothertypeofassetclass
8 ComponentQuantity 21 68 N Numberofsharesofthisstockpercreationunit
9 SignFieldforCom-
ponentQuantity
1 89 A/N -indicatesnegativevalue(shortposition).
Note:ifanycomponentisshort,thenitcanonly
becreated/redeemedforcash.
10 NewSecurityIndicator1 90 A/N l N=Newcomponentintheportfolioasper
theETFagent.
l Space=notnew
11 CashInLieuIndicator 1 91 A/N l Y=ETFagentprovidedindicatorforcom-
ponenttobesubstitutedforcashinacre-
ate/redeem;
l X=NSCCappliedindicatorforcomponent
tobesubstitutedforcashinacreateand
redeem(perbelowmentionedrules)
l space=Nosubstitution
Note:CILissettoXifoneofthefollowingis
met:
l Componentisnotcreate/redeemeligiblein
SMD.
l Portfolioisacashonlyportfolio.
12 ComponentSymbol 15 92 A/N TradingSymbolofComponent
13 ComponentWIIndic-
ator
1 107 WIindicatorofDomesticComponent
14 Componentunder-
goingcorporateaction
1 108 A/N l Space=Nocorporateaction
l M=MandatoryCorporateAction
l V=VoluntaryCorporateAction
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 12

HistoricalPortfolioMROFileLayout:AutoRoute02262222 12
AutoRoute02262222
Type3–ComponentDetailRecord
Recordlength=500
Seq Description Length Start Type Comments
15 SettlementLocation 1 109 A/N l 1=[[CNS]]
l 2=TFT
l 3=[[GSD]]*
l 4=MBSD*
l 5=OCC*
* Futureenhancement.
16 ComponentCNSIndic-
ator
1 110 A/N l Y=CNSeligible
l N=NotCNSeligible
17 ExternalSettlement
Date
8 111 N ETFAgentprovidedsettlementdatefornon-set-
tlingcomponents.
18 ComponentDescrip-
tion
60 119 A/N OverrideinputiffoundinSMD.
19 ComponentPrice
Amount
16 179 N Displayallzeros.
Futureenhancement.
9,999,999,999.999999
Note:ThisfieldisnotinAutoRoute02261256.
20 SecurityIssueType 1 195 A/N l S=[[Stock]]
l B=Bond
Note:ThisfieldisnotinAutoRoute02261256.
21 WhenIssuedIndicator1 196 A/N AgentprovidesWhenIssued(WI)indicatorfor
FixedIncomecomponents:
l Y=WhenIssued
l N=NotWhenIssued
22 AccruedInterestNon-
standardSettlement
11 197 N 999,999,999.99
23 AccruedInterestStand-
ardSettlement
11 208 N 999,999,999.99
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 13

HistoricalPortfolioMROFileLayout:AutoRoute02262222 13
AutoRoute02262222
Type3–ComponentDetailRecord
Recordlength=500
Seq Description Length Start Type Comments
24 AssetClass 27 219 A Freeformfieldtoidentifytheassetclassofthe
security.
25 ExcludedFromPricing 21 246 N PricingBasketOnly
Quantityofsecuritiesownedbythefundper
basket/unit,butdifficulttoprice.
26 Price(inFundBase
Currency)
24 267 N PricingBasketOnly
PriceofthesecurityontheNAVdate.
999,999,999,999,999,999.999999
27 LocalCurrency 3 291 A Identifiesthecurrencyofthesecurity.For
example,USD.
28 Factor 24 294 N Decimalvaluereflectingaproportionofthe
outstandingprincipalvalueofthefactorbonds
thatchangesovertime.Alsoappliestoequity
factors,suchasstocksplitonexdate.
999,999,999,999,999,999.999999
29 SyntheticsLocalCur-
rency
3 318 A Identifiesthecurrencyofthesecurity.For
example,USD.
30 SyntheticsPriceMul-
tiplier
24 321 N Designatedpricemultiplier.
999,999,999,999,999,999.999999
31 SyntheticsContract
Size
24 345 N Agreednotionalsizeofthefuturescontract.
999,999,999,999,999,999.999999
32 SyntheticsAverage
ContractOpenPrice
24 369 N Averageofthefuturetradeprice.
999,999,999,999,999,999.999999
33 FXRatesBaseCur-
rency
3 393 A Identifiesthebasecurrencyofthefund.For
example,USD
34 FXRatesCurrencies 3 396 A SpotFXratesofrespectivecurrenciesagainst
thebasecurrencyofthefund.
Forexample,EUR,GBR,USD.
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 14

HistoricalPortfolioMROFileLayout:AutoRoute02262222 14
AutoRoute02262222
Type3–ComponentDetailRecord
Recordlength=500
Seq Description Length Start Type Comments
35 FXForwardsCurrency
Pair
6 399 A Identifiesthecurrencypairassociatedwiththe
FXforward.
Forexample,EURUSD
36 FXForwardsValue
Date
8 405 N SettlementdateoftheFXforward,in
CCYYMMDDformat.
37 FXForwardsQuantity 9 413 N Fundhedgedquantity.
9,999,999.99
38 FXForwardsRate 7 422 N Interpolatedrate:rateusedforNAVcalculation,
includingforwardpointinterpolation.
9.999999
39 FXForwardsValue 9 429 N CurrencymarketvalueoftheFXforward.
9,999,999.99
40 FXForwardsCurrency3 438 A IdentifiesthebasecurrencyoftheFXforward
contract.
Forexample,EUR
41 SWAPsNotionalValue 7 441 N Totalamountofasecurity'sunderlyingasset.
9,999,999
42 SWAPsSpread 5 448 N CostoftheunderlyingfeefromtheSWAP
counterparty.
9.9999
43 SWAPsMarketValue 9 453 N AgreeduponpriceoftheSWAP.
9,999,999.99
44 FutureUse 39 462 Spaces.
ENDOFRECORD
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 15

HistoricalPortfolioMROFileLayout:AutoRoute02262222 15
Type99–TrailerRecord
ThefollowingtableshowtheType99–TrailerRecorddetailsfortheHistoricalPortfolioMROFileLayout:AutoRoute
02262222recordlayout:
AutoRoute02262222
Type99–TrailerRecord
Recordlength=500
Seq Description Length Start Type Comments
1 RecordType 2 1 A/N 99=TrailerRecord
Oneperfile.
2 ProcessingDate 8 3 N CCYYMMDD
3 TransmissionType 1 11 A/N H=HistoricalTransmission
Note:ThisisalwayssettoH.
4 RecordCount 13 12 N Numberofrecordsintransmission(includingtrailer).
5 FutureUse 476 25 Spaces.
ENDOFRECORD
ETFPortfolioService-HistoricalFileUser'sGuide

---

## Page 16

FORMOREINFORMATION
EmailDTCCLearningat:
DataLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com