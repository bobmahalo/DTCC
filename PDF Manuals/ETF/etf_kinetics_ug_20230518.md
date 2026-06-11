---
title: "DTCC ETF Kinetics User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/etf_kinetics_ug_20230518.pdf"
pages: 17
size: "1191.7 KB"
category: "ETF"
ingested_on: "2026-06-05"
---

# DTCC ETF Kinetics User Guide

**Original File:** [etf_kinetics_ug_20230518.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/etf_kinetics_ug_20230518.pdf)  
**Category:** ETF  
**Total Pages:** 17  
**File Size:** 1191.7 KB  

---

## Page 1

ETFKINETICS
USERGUIDE
MAY18,2023


---

## Page 2

©2023DTCC.Allrightsreserved.[[DTCC]],[[DTCC]](Stylized),ADVANCINGFINANCIALMARKETS.
TOGETHER,andtheInterlockergraphicareregisteredandunregisteredtrademarksofTheDepository
Trust&ClearingCorporation.
DocInfo:May18,2023
PublicationCode:DAT299
Service:ETFKinetics
Title:UserGuide

---

## Page 3

TABLEOFCONTENTS
[[DTCC]] ETFKinetics 4
Overview 4
FileDelivery 4
DataFields 5
CommonlyUsedTerms 5
PrimaryMarketAggregations 5
Portfolio-LevelFields 5
Component-LevelFields 7
ETFKineticsSecondaryMarketAggregations 8
CalculationSpecifics 11
ConcentrationValues 11
SellandShortVolume 14
FrequentlyAskedQuestions 15
PrimaryMarketFAQs 15
SecondaryMarketFAQs 15

---

## Page 4

[[DTCC]] ETFKinetics 4
[[DTCC]]  ETFKINETICS
Overview
[[DTCC]]’sETFKineticsserviceprovidestransparencyandinsightsintoETFprimaryandsecondaryMarketstoinform
marketparticipants'investmentdecisions.
Byaggregatingandanonymizingtheseactivities,theserviceprovidesmarketparticipantsinsightintoETFs':
l depthofmarketparticipation
l concentration
l fundflows
l associateddemandsonunderlyingsecurities
FileDelivery
l PrimarymarketaggregationswillbedeliveredonT+3,Monday–Friday,atorshortlyafter5:00P.M.ET
l SecondarymarketaggregationswillbedeliveredtoclientsT+1,Tuesday–Saturday,priorto5AMET
DTCCETFKineticsUserGuide

---

## Page 5

DATAFIELDS
Thissectioncontainsafilespecificationwithdetailsrelatedtodatafieldsinthefiles.
CommonlyUsedTerms
Thetablebelowprovidesdefinitionsofcommonlyusedtermsinthedatafields.
Term/ Acronym Description
Tier1 AnaggregationviewofallNSCCclearingIDsforthedate,symbol,andtransaction
typeinquestionforthe10mostactiveNSCCclearingIDs,intermsoftotalshares.
GlobalBrokerDealer
Aggregation(GBDA)
Anaggregationviewofafixedgroupof9clearingIDsthatshareacommonchar-
acteristic.
Industry AnaggregationviewofallNSCCclearingIDsforthedate,symbol,andtransaction
typeinquestion.
PrimaryMarketAggregations
Portfolio-LevelFields
ThetablebelowdescribesthefieldsfoundwithinthePrimaryMarketAggregations.
Field Format Description
TradeDate l Type:Date
l Width:10
Containsareferencetoaparticularday
representedwithinacalendarsystemfor
whentheTradehasoccurred.
ETFISIN l Type:Alphanumeric
andNumeric
l Width:12
Acombinationofoneormorenumbers,
letters,orspecialcharactersthat
designatesaspecificoccurrenceofa
SecuritiesAndExchangeCommission
InternationalSecurityIdentification
Number.
InstrumentDescription l Type:Alphanumeric
l MaxWidth:256
TheexplanationofanInstrument.
PrimaryMarketAggregationFields

---

## Page 6

Field Format Description
ETFSharesPer
Create/RedeemUnitor
CreationUnitSizeAmount
l Type:Numeric
l MaxWidth:9
l Decimal:9
DefinesthesmallestblockofETFshares
thatcanbeboughtorsoldfromthefund
companyatnetassetvalue(NAV).
CreationUnitQuantity l Type:Numeric
l MaxWidth:13
Totalsumofcreationunits.
SharesCreated l Type:Numeric
l MaxWidth:13
TotalsumofETFsharescreated.
RedemptionUnitQuantity l Type:Numeric
l MaxWidth:13
Totalsumofredemptionunits.
SharesRedeemed l Type:Numeric
l MaxWidth:13
TotalsumofETFsharesredeemed.
TotalETFSettlementValue
(Creations)
l Type:Numeric
l MaxWidth:20
l Decimal:6
TotalsumofthecreationunitNetAsset
Value.
TotalETFSettlementValue
(Redemptions)
l Type:Numeric
l MaxWidth:20
l Decimal:6
TotalsumoftheredemptionunitNet
AssetValue.
DTCCFundFlow l Type:Numeric
l MaxWidth:13
Netcapitalbeingaddedtoorwithdrawn
fromtheETFclearedthroughNSCC.
FundFlow l Type:Numeric
l MaxWidth:13
l Decimal:6
Netcapitalbeingaddedtoorwithdrawn
fromtheETF.
DTCCchangeinShares
Outstanding
l Type:Numeric
l MaxWidth:13
NetnumberofETFsharesthathave
beencreatedorredeemedcleared
throughNSCC.
TotalchangeinShares
Outstanding
l Type:Numeric
l MaxWidth:13
NetnumberofETFsharesthathave
beencreatedorredeemed.
PrimaryMarketAggregationFields(continued)

---

## Page 7

Component-LevelFields
Thenexttabledescribescomponent-levelETFKineticsfieldsforthePrimaryMarketAggregations.
Field Format Description
TradeDate l Type:Date
l Width:10
Containsareferencetoaparticulardayrepresented
withinacalendarsystemforwhentheTradehas
occurred.
ETFISIN l Type:Alphanumericand
Numeric
l Width:12
Acombinationofoneormorenumbers,letters,or
specialcharactersthatdesignatesaspecific
occurrenceofaSecuritiesAndExchange
CommissionInternationalSecurityIdentification
Number.
ComponentISIN l Type:Alphanumericand
Numeric
l Width:12
Acombinationofoneormorenumbers,letters,or
specialcharactersthatdesignatesaspecific
occurrenceofaSecuritiesAndExchange
CommissionInternationalSecurityIdentification
Number.
Component
Security
Description
l Type:Alphanumeric
l MaxWidth:256
Theexplanationoftheinstrument.
Component
[[shares]]
Redeemed
l Type:Numeric
l MaxWidth:13
TotalsumofcomponentsharesdeliveredfromETF.
Component
SharesCreated
l Type:Numeric
l MaxWidth:13
TotalsumofcomponentsharesdeliveredtoETF.
Netchangein
componentshares
l Type:Numeric
l MaxWidth:13
Netnumberofcomponentsharesthathavebeen
deliveredtoordeliveredfromtheETF.
Component-LevelFields

---

## Page 8

ETFKineticsSecondaryMarketAggregations
ThenexttabledescribesETFKineticsfieldswithintheSecondaryMarketAggregations.
Field Format Description
TRADEDATE l Type:Date
l Width:10
Containsareferencetoaparticulardayrepresented
withinacalendarsystemforwhentheTrade
occurred.
TRADESIDE l Type:Alphanumeric
l Width:2
l B:BuyS:Sell
l SS:ShortSell
ISIN l Type:Alphanumeric
andNumeric
l Width:12
12-characterETFISIN.
[[CUSIP]] l Type:Alphanumeric
andNumeric
l Width:9
9-characterETFCUSIP
IndustryVolume l Type:Numeric
l Width:16
TotalIndustrysumofshares.
IndustryVWAP l Type:Numeric
l Width:13Decimal:3
VolumeWeightedAveragePrice.Calculatedasan
averageofexecutionprice,weightbynumberof
sharestradedfortheindustryaggregate.
IndustryBroker
Count
l Type:Numeric
l Width:5
CountofUniqueIDsofIndustryParticipants.
Industry
Concentration
l Type:Numeric
l Width:6
l Decimal:4
SummationofIndustrybrokers'marketshares
squared.
IndustryBroker
Rank1
l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketsharepercentageofthemost
activeClearingIDinthiscategory.
IndustryBroker
Rank2
l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketsharepercentageofthesecond
mostactiveClearingIDinthiscategory.
SecondaryMarketAggregationFields

---

## Page 9

Field Format Description
IndustryBroker
Rank3
l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketsharepercentageofthethird
mostactiveClearingIDinthiscategory.
Tier1Volume l Type:Numeric
l Width:16
TotalTier1sumofshares.
Tier1VWAP l Type:Numeric
l Width:13
l Decimal:3
VolumeWeightedAveragePrice.Calculatedasan
averageofexecutionprice,weightedbythenumber
ofsharestradedfortheTier1aggregate.
Tier1Unique
Brokers
l Type:Numeric
l Width:5
CountofUniqueIDsofTier1Participants.
Tier1
Concentration
l Type:Numeric
l Width:6
l Decimal:4
SummationofTier1brokers'marketsharesquared.
Tier1Broker
Rank1
l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthemostactive
ClearingIDinthiscategory.
Tier1Broker
Rank2
l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthesecondmostactive
ClearingIDinthiscategory.
Tier1Broker
Rank3
l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthethirdmostactive
ClearingIDinthiscategory.
GBDAVolume l Type:Numeric
l Width:16
TotalGBDAsumofshares.
GBDAVWAP l Type:Numeric
l Width:13
l Decimal:3
VolumeWeightedAveragePrice.Calculatedasan
averageofexecutionprice,weightedbythenumber
ofsharestradedfortheGBDA.
GBDABroker
Count
l Type:Numeric
l Width:3
CountofUniqueIDsofGBDAParticipants.
SecondaryMarketAggregationFields(continued)

---

## Page 10

Field Format Description
GBDA
Concentration
l Type:Numeric
l Width:6
l Decimal:4
SummationofGlobalBrokerDealers'marketshare
squared.
GBDARank1 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthemostactive
ClearingIDinthiscategory.
GBDARank2 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthesecondmostactive
ClearingIDinthiscategory.
GBDARank3 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthethirdmostactive
ClearingIDinthiscategory.
RefCode l Type:Alphanumeric
l Width:2
IncaseswherethecountofbrokersintheGBDA
groupislessthan9,and"NA"willbedisplayed.
SecondaryMarketAggregationFields(continued)

---

## Page 11

CalculationSpecifics 11
CALCULATIONSPECIFICS
ConcentrationValues
ConcentrationmetricsarecalculatedbasedontheHirschmanHerfindahlIndex.Calculationsoccursasfollows:
l Takeeachmemberofanaggregateandcalculateitsvolumemarketshare.
l Foreachmarketshare,takethesquareofitsvalue,orpowerof2.
l Sumthetotalofeachmarketsharesquaretofindtheconcentration.
ForeachaggregatecreatedintheDTCCETFKineticsservice,thevariousversionsofconcentrationcalculated
arediscretelycreated,basedonthemembersaofaspecificaggregateand/ortimeperiod.Forexample,the
valueknownas‘industryconcentration’isbasedonallbrokersforaparticularsecurity,tradedate,andtrade
side.Theotherconcentrationmetrics(Tier1orGBDA)arecreatedbasedonlyonthebrokersincludedinthat
aggregateforatradedateandtradeside.
ThetablesthatfollowcontainsamplecalculationsforeachConcentrationmetric.Alldatainthesetablesisfakeor
"dummy"data.
CompaniesTradingSecurity Volume Rank GBDA MarketShare MarketShareSquared
Broker1 182,536 1 Y 0.1340 0.0179
Broker2 136,289 2 N 0.1000 0.0100
Broker3 131,030 3 N 0.0962 0.0092
Broker4 124,323 4 Y 0.0912 0.0083
Broker5 122,613 5 N 0.0900 0.0081
Broker6 104,000 6 Y 0.0763 0.0058
Broker7 83,278 7 Y 0.0611 0.0037
Broker8 59,648 8 N 0.0438 0.0019
Broker9 58,632 9 N 0.0430 0.0019
IndustryConcentration
DTCCETFKineticsUserGuide

---

## Page 12

CalculationSpecifics 12
CompaniesTradingSecurity Volume Rank GBDA MarketShare MarketShareSquared
Broker10 47,987 10 N 0.0352 0.0012
Broker11 44,148 11 N 0.0324 0.0010
Broker12 40,616 12 N 0.0298 0.0009
Broker13 37,367 13 Y 0.0274 0.0008
Broker14 34,378 14 Y 0.0252 0.0006
Broker15 31,627 15 N 0.0232 0.0005
Broker16 29,097 16 Y 0.0214 0.0005
Broker17 26,769 17 Y 0.0196 0.0004
Broker18 24,628 18 N 0.0181 0.0003
Broker19 22,658 19 Y 0.0166 0.0003
Broker20 20,845 20 N 0.0153 0.0002
TotalSharesTraded:1,362,469
IndustryConcentration:0.0737
IndustryConcentration(continued)
CompaniesTradingSecurity Volume Rank MarketShare MarketShareSquared
Broker1 182,536 1 0.1738 0.0302
Broker2 136,289 2 0.1298 0.0168
Broker3 131,030 3 0.1248 0.0156
Broker4 124,323 4 0.1184 0.0140
Broker5 122,613 5 0.1167 0.0136
Tier1Concentration
DTCCETFKineticsUserGuide

---

## Page 13

CalculationSpecifics 13
CompaniesTradingSecurity Volume Rank MarketShare MarketShareSquared
Broker6 104,000 6 0.0990 0.0098
Broker7 83,278 7 0.0793 0.0063
Broker8 59,648 8 0.0568 0.0032
Broker9 58,632 9 0.0558 0.0031
Broker10 47,987 10 0.0457 0.0021
TotalSharesTraded:1,050,336
Tier1Concentration:0.1148
Tier1Concentration(continued)
CompaniesTradingSecurity Volume MarketShare MarketShareSquared
Broker1 182,536 0.2833 0.0802
Broker4 124,323 0.1929 0.0372
Broker6 104,000 0.1614 0.0260
Broker7 83,278 0.1292 0.0167
Broker13 37,367 0.0580 0.0034
Broker14 34,378 0.0533 0.0028
Broker16 29,097 0.0452 0.0020
Broker17 26,769 0.0415 0.0017
Broker19 22,658 0.0352 0.0012
TotalSharesTraded:644,406
GBDAConcentration:0.714
GBDAConcentration
DTCCETFKineticsUserGuide

---

## Page 14

CalculationSpecifics 14
SellandShortVolume
WhentheSellandShortSellvolume(and/orShortSellExemptVolume)aresummedforasingledateandequity,
thereareseveralscenariosthatrelatetothecomputationbalanceasitrelatestothebuyvolume.
l TheTier1andGDBAvolumeswillnotbalanceinmostcasesbecausethetradesidesarecomputedinde-
pendently.
l FortheDailyIndustryVolume,incaseswherethebuyandallsellmetricsareavailable(meaningnotblockedby
thethreshold),thesumoftheIndustrySellVolumesequalstheIndustryBuy,withafewexceptionsnotedinthis
document.
DTCCETFKineticsUserGuide

---

## Page 15

FrequentlyAskedQuestions 15
FREQUENTLYASKEDQUESTIONS
ThissectionanswersfrequentlyaskedquestionsrelatedtoPrimaryandSecondaryETFKineticsdata.
PrimaryMarketFAQs
Q.Whataretheprimarymarketaggregationrules?
l ETFscontainingmunicipalbondcomponentshavebeenexcludedfromtheservice.
l MetricswithinETFprimarymarketaggregationsarepopulatedwith-1whenallordersaredoneagainstnon-
standardbaskets.
Q.Whydoesn'ttheDTCCFundFlowmatchFundFloworanothersourceofFundFlow?
l ETFprimarymarketordersdoneagainstnon-standardbaskettypeshavebeenexcludedfromtheDTCCFund
FlowaggregationsThebasketsincludedintheprimarymarketaggregationsinclude:Standard(01),Create
Only(05),andRedeemOnly(06)
l TheETFsharesoutstandingutilizedwithintheFundFlowcalculationmaynotbecorrect.Ifthereisadis-
crepancybetweenthereportedsharesoutstandingindifferentbaskettypesonthesameday,thefundflow
closettoDTCC’svaluewillbechosen.
Q.Whydothesharecountswithinthecomponentaggregationappeartobelowerthan
expected?
l Theprimarymarketordersmayhavebeendoneincashversusin-kind.
l TheprimarymarketcomponentorderrecordsmayhavebeenmissingtheNSCCPortfolioId,andasaresult
beenexcludedfromtheaggregation.
Q.Howmuchhistoryisavailable?
HistoryisavailablebacktoJanuary26,2018forprimaryandcomponentaggregations
SecondaryMarketFAQs
Q.Howmuchhistoryisavailable?
HistoryisavailablebacktoNovember10,2015forsecondaryaggregations.
DTCCETFKineticsUserGuide

---

## Page 16

FrequentlyAskedQuestions 16
Q.Whatarethesecondarymarketaggregationrules?
l ETFscontainingmunicipalbondcomponentshavebeenexcludedfromtheservice.
l ETFKineticsisaggregatedbyTradeDateandSecurity.Theremustbeatleasttenuniquebrokerstradingthe
issueforvaluestobedisplayed.
l TheGlobalBroker-DealerAggregatemusthaveactivityfromallnineuniquemembers.Ifoneormoreofthe
GBDAmembersdoesnothaveactivity,allmetricsforthisaggregateareunavailable.Inthesecases,avalue
ofNAappearsinthereferencefield.
Q.Doestheindustryvolumeencompassallbrokers?
Yes;alistofallNSCCclearingmembersisavailableathttps://www.[[DTCC]].com/client-center/[[NSCC]]-directories.
Q.WhyareRefCodesometimesNullorZero(0)?
ThescenariothatwouldpresentanNArefcodeiswhereGBDAis>0but<threshold.
WhenGBDAisnullANDrefcodeisnullisanindicationthatzeroGBDAwerefound.
Q.HowmuchoftheU.S.equitymarketiscapturedintheDTCCETFKineticsservice?
TheDTCCETFKineticsservicecapturesaviewofactivityacrossallU.S.equityexchanges,[[ATS]],anddarkpools.
Q.Whatisthedatadeliveryformatandmethod?
DTCCETFKineticsdataisdeliveredincomma-separated(CSV)files,standardoutputformat.Subscriberscan
loadthisdataintootherapplicationsorsystems.TheETFKineticsserviceisalsoofferedviatheSnowflakemar-
ketplacethroughsecureviews.
DTCCETFKineticsUserGuide

---

## Page 17

FORMOREINFORMATION
EmailDTCCLearningat:
DTCCLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com