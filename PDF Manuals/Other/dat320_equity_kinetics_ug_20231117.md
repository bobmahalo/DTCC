---
title: "Equity Kinetics User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat320_equity_kinetics_ug_20231117.pdf"
pages: 25
size: "322.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Equity Kinetics User Guide

**Original File:** [dat320_equity_kinetics_ug_20231117.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat320_equity_kinetics_ug_20231117.pdf)  
**Category:** Other  
**Total Pages:** 25  
**File Size:** 322.2 KB  

---

## Page 1

EquityKinetics
USERGUIDE
NOVEMBER17,2023

---

## Page 2

TABLEOFCONTENTS
FieldLayouts 3
CommonlyUsedTerms 3
SFTPDataFields 4
DailyFile 4
Five-DayRollingandIntradayFiles 7
SnowflakeDataFields 9
DailyTable 9
Five-DayRollingandIntradayTable 10
NotesonData 13
KnownIssueforSomeAggregationValues 13
UnderstatedAggregatesorMissingValues 13
Comparing1Day,Intraday,and/orFive-DayVolumes 14
LegacyDatabaseValues 14
April28,2022Refresh 15
CalculationSpecifics 16
ConcentrationValues 16
SellandShortVolume 18
FrequentlyAskedQuestions 19
ProductSupportandDocumentation 24
DTCCEquityKineticsUserGuide
TableOfContents 2

---

## Page 3

FIELDLAYOUTS
CommonlyUsedTerms
Term/ Acronym Description
Tier1 AnaggregationviewofallNSCCclearingIDsforthe
date,symbol,andtransactiontypeinquestionforthe
10mostactiveNSCCclearingIDs,intermsoftotal
[[shares]].
GlobalBrokerDealerAggregation(GBDA) Anaggregationviewofafixedgroupof9clearingIDs
thatshareacommoncharacteristic.
Industry AnaggregationviewofallNSCCclearingIDsforthe
date,symbol,andtransactiontypeinquestion.
CommonlyUsedTerms
DTCCEquityKineticsUserGuide
FieldLayouts 3

---

## Page 4

SFTPDataFields
ThissectiondocumentsthedatafieldswhenaccessingDTCC EquityKineticsdatafromanSFTPdelivery.
DailyFile
Usersofthisdatareceivefouruniquefilesforthespecificationsdescribedinthenexttable(Buy,Sell,
ShortSell,andShortSellExempt).Forviewingpurposes,thefieldlayoutinthenexttableistransposed.In
theactualdatafile,datarowfieldslistedintheFieldNamecolumnappearascolumnheaders,witheach
rowrepresentingasecuritytradedate.
FieldsLabel Format Description
TradeDate l Type:Date4y
l Width:10
l Decimal:0
Datethesharesaretraded.
ISIN l Type:Alphanumeric
l Width:15
12-characterISIN.
[[CUSIP]] l Type:Alphanumeric
l Width:15
9-characterCUSIP
Ticker l Type:Alphanumeric
l Width:10
Theuniquetickersymbolfortrading
(ExchangeSymbol).
IndustryVolume l Type:Numeric
l Width:16
l Decimal:0
TotalIndustrysumofshares.
IndustryVWAP l Type:Numeric
l Width:16
l Decimal:8
VolumeWeightedAveragePrice.Cal-
culatedasanaverageofexecutionprice,
weightbynumberofsharestradedfor
theindustryaggregate.
IndustryBrokerCount l Type:Numeric
l Width:5
CountofUniqueIDsofIndustryPar-
ticipants.
IndustryCon-
centration
l Type:Numeric
l Width:6
l Decimal:4
SummationofIndustrybrokers'market
sharessquared.Forspecifics,
SFTPDataFields-EndofDay([[EOD]])File
DTCCEquityKineticsUserGuide
FieldLayouts 4

---

## Page 5

FieldsLabel Format Description
IndustryBrokerR1 l Type:Numeric
l Width:6
l Decimal:14
Anonymousmarketsharepercentageof
themostactiveClearingIDinthiscat-
egory.
IndustryBrokerR2 l Type:Numeric
l Width:6
l Decimal:14
Anonymousmarketsharepercentageof
thesecondmostactiveClearingIDin
thiscategory.
IndustryBrokerR3 l Type:Numeric
l Width:6
l Decimal:14
Anonymousmarketsharepercentageof
thethirdmostactiveClearingIDinthis
category.
Tier1Volume l Type:Numeric
l Width:6
l Decimal:0
TotalTier1sumofshares.
Tier1VWAP l Type:Numeric
l Width:16
l Decimal:8
VolumeWeightedAveragePrice.Cal-
culatedasanaverageofexecutionprice,
weightedbythenumberofsharestraded
fortheTier1aggregate.
Tier1UniqueBrokers l Type:Numeric
l Width:16
l Decimal:8
CountofUniqueIDsofTier1Par-
ticipants.
Tier1Concentration l Type:Numeric
l Width:6
l Decimal:4
SummationofTier1brokers'market
sharesquared.Forspecifics,seeFre-
quentlyAskedQuestionsonpage 1.
Tier1BrokerR l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthemostact-
iveClearingIDinthiscategory.
Tier1BrokerR2 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthesecond
mostactiveClearingIDinthiscategory.
Tier1BrokerR3 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthethird
mostactiveClearingIDinthiscategory.
GBDAVolume l Type:Numeric
l Width:16
l Decimal:0
TotalGBDAsumofshares.
SFTPDataFields-EndofDay([[EOD]])File
DTCCEquityKineticsUserGuide
FieldLayouts 5

---

## Page 6

FieldsLabel Format Description
GBDAVWAP l Type:Numeric
l Width:16
l Decimal:0
VolumeWeightedAveragePrice.Cal-
culatedasanaverageofexecutionprice,
weightedbythenumberofsharestraded
fortheGBDA.
GBDABrokerCount l Type:Numeric
l Width:3
CountofUniqueIDsofGBDAPar-
ticipants.
GBDAConcentration l Type:Numeric
l Width:6
l Decimal:4
SummationofGlobalBrokerDealers'
marketsharesquared.Forspecifics,
seeFrequentlyAskedQuestionson
page 1.
GBDA R1 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthemostact-
iveClearingIDinthiscategory.
GBDA R2 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthesecond
mostactiveClearingIDinthiscategory.
GBDA R3 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthethird
mostactiveClearingIDinthiscategory.
RefCode l Type:Alphanumeric
l Width:2
Incaseswherethecountofbrokersin
theGBDAgroupislessthan9,and"NA"
willbedisplayed.
SFTPDataFields-EndofDay([[EOD]])File
DTCCEquityKineticsUserGuide
FieldLayouts 6

---

## Page 7

Five-DayRollingandIntradayFiles
Notes
l Tosimplifydelivery,the5-DayRollingandIntradayfilesareeachconsolidatedintoonefile,ratherthan
beingdeliveredasfourseparatefilespertradetypeasthedailyfilesaredelivered.Asaresult,these
twofilescontainanadditionalTradeSidefieldthatidentifiestheuniquetradetypes.
l AlthoughtheDailyEquityKineticsFileincludesfourdistincttradetypes(buy,sell,shortsell,andshort
sellexempt),the5-dayandintradayreportscontainthreedistincttradetypes(indicatedbyBforBuy,S
forSell,andSSforbothShortsellandShortSellExempt).ShortSellExemptandShortSellaggreg-
ationsarenowcombinedintoasingleview.
l Theroundinganddecimalizationofthesefilesdiffersfromthedailyfile.
l TheConcentrationandMarketShare1,2,and3forthetradedate,[[Stock]],andtradesideareblankfor
concentrationvaluesgreaterthan5.
FieldName Format Description
TradeDate l Type:Date4y
l Width:10
l Decimal:0
Datethesharesaretraded.
TradeSide l Type:Char
l Width:2
Thetradesidethatis
executed.Validvalues:
l B:Buy
l S:Sell
l SS:ShortSell
ISIN l Type:Alphanumeric
l Width:15
12-characterISIN.
[[CUSIP]] l Type:Alphanumeric
l Width:15
9-characterCUSIP
Ticker l Type:Alphanumeric
l Width:10
Theuniquetickersymbolfor
trading.(ExchangeSymbol).
SFTPDataFields-DayRollingandIntradayFiles
DTCCEquityKineticsUserGuide
FieldLayouts 7

---

## Page 8

FieldName Format Description
IndustryVolume l Type:Numeric
l Width:16
l Decimal:0
TotalIndustrysumofshares,
roundedtothenearest1000.
IndustryVWAP l Type:Numeric
l Width:16
l Decimal:3
VolumeWeightedAverage
Price.Calculatedasan
averageofexecutionprice,
weightbynumberofshares
tradedfortheindustry
aggregate.
IndustryBrokerCount l Type:Numeric
l Width:5
CountofUniqueIDsof
IndustryParticipants.
IndustryConcentration l Type:Numeric
l Width:6
l Decimal:3
SummationofIndustry
brokers'marketshares
squared.Forspecifics,see
FrequentlyAskedQuestions
onpage 1.
IndustryBrokerR1 l Type:Numeric
l Width:6
l Decimal:3
Anonymousmarketshare
percentageofthemost
activeClearingIDinthis
category.
SFTPDataFields-DayRollingandIntradayFiles(continued)
DTCCEquityKineticsUserGuide
FieldLayouts 8

---

## Page 9

SnowflakeDataFields
ThissectiondocumentsthedatafieldswhenaccessingDTCC EquityKineticsdatafromtheSnowflake
datamarketplace.
DailyTable
FieldName Format Description
TRADE_DATE l Type:Date4y
l Width:10
l Decimal:0
Datethesharesaretraded.
TRADE_TYPE l Type:Alpha
l Width:3
B:Buy
S:Sell
SS:ShortSell
SSE:ShortSellExempt
TRADE_TYPE_DESC l Type:Alpha
l Width:17
EK_BUY
EK_SELL
EK_SHORTSELL
EK_SHORTSELLEXEMPT
ISIN l Type:Alphanumeric
l Width:15
12-characterISIN.
[[CUSIP]] l Type:Alphanumeric
l Width:15
9-characterCUSIP
TICKER l Type:Alphanumeric
l Width:10
Theuniquetickersymbolfortrading.
(ExchangeSymbol).
INDUSTRY_VOLUME l Type:Numeric
l Width:16
l Decimal:0
TotalIndustrysumofshares.
SFTPData-DayRollingandIntradayTable
DTCCEquityKineticsUserGuide
FieldLayouts 9

---

## Page 10

FieldName Format Description
INDUSTRY_VWAP l Type:Numeric
l Width:16
l Decimal:8
VolumeWeightedAveragePrice.Calculated
asanaverageofexecutionprice,weightby
numberofsharestradedfortheindustry
aggregate.
INDUSTRY_BROKER_
COUHNT
l Type:Numeric
l Width:5
CountofUniqueIDsofIndustryParticipants.
REF_CODE l Type:Alphanumeric
l Width:2
Incaseswherethecountofbrokersinthe
GBDAgroupislessthan9,and"NA"willbe
displayed.
SFTPData-DayRollingandIntradayTable(continued)
Five-DayRollingandIntradayTable
FieldName Format Description
TRADE_DATE l Type:Date4y
l Width:10
l Decimal:0
Datethesharesaretraded.
TRADE_TYPE l Type:Alpha
l Width:3
l B:Buy
l S:Sell
l SS:ShortSell
l SSE:ShortSellExempt
TRADE_TYPE_DESC l Type:Alpha
l Width:17
l EK_BUY
l EK_SELL
l EK_SHORTSELL
ISIN l Type:Alphanumeric
l Width:15
12-characterISIN.
[[CUSIP]] l Type:Alphanumeric
l Width:15
9-characterCUSIP
SnowflakeData-Five-DayRollingandIntradayTable
DTCCEquityKineticsUserGuide
FieldLayouts 10

---

## Page 11

FieldName Format Description
TICKER l Type:Alphanumeric
l Width:10
Theuniquetickersymbolfor
trading.(ExchangeSymbol).
INDUSTRY_VOLUME l Type:Numeric
l Width:16
l Decimal:0
TotalIndustrysumofshares.
INDUSTRY_VWAP l Type:Numeric
l Width:16
l Decimal:8
VolumeWeightedAverage
Price.Calculatedasanaverage
ofexecutionprice,weightby
numberofsharestradedforthe
industryaggregate.
INDUSTRY_BROKER_
COUHNT
l Type:Numeric
l Width:5
CountofUniqueIDsofIndustry
Participants.
INDUSTRY_
CONCENTRATION
l Type:Numeric
l Width:6
l Decimal:4
SummationofIndustrybrokers'
marketsharessquared.For
specifics,seeFrequentlyAsked
Questionsonpage 22.
INDUSTRY_BROKER_
RANK1
l Type:Numeric
l Width:6
l Decimal:14
Anonymousmarketshare
percentageofthemostactive
ClearingIDinthiscategory.
INDUSTRY_BROKER_
RANK2
l Type:Numeric
l Width:6
l Decimal:14
Anonymousmarketshare
percentageofthesecondmost
activeClearingIDinthis
category.
INDUSTRY_BROKER_
RANK3
l Type:Numeric
l Width:6
l Decimal:14
Anonymousmarketshare
percentageofthethirdmost
activeClearingIDinthis
category.
TIER1_VOLUME l Type:Numeric
l Width:6
l Decimal:0
TotalTier1sumofshares.
SnowflakeData-Five-DayRollingandIntradayTable(continued)
DTCCEquityKineticsUserGuide
FieldLayouts 11

---

## Page 12

FieldName Format Description
TIER1_VWAP l Type:Numeric
l Width:16
l Decimal:8
VolumeWeightedAverage
Price.Calculatedasanaverage
ofexecutionprice,weightedby
thenumberofsharestradedfor
theTier1aggregate.
TIER1_UNIQUE_BROIKERSl Type:Numeric
l Width:16
l Decimal:8
CountofUniqueIDsofTier1
Participants.
TIER1_CONCENTRATIONl Type:Numeric
l Width:6
l Decimal:4
SummationofTier1brokers'
marketsharesquared.For
specifics,seeFrequentlyAsked
Questionsonpage 22.
TIER1_BROKER_RANK1 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthe
mostactiveClearingIDinthis
category.
TIER1_BROKER_RANK2 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthe
secondmostactiveClearingID
inthiscategory.
TIER1_BROKER_RANK3 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthe
thirdmostactiveClearingIDin
thiscategory.
GDPA_VOLUME l Type:Numeric
l Width:16
l Decimal:0
TotalGBDAsumofshares.
GDPA_VWAP l Type:Numeric
l Width:16
l Decimal:0
VolumeWeightedAverage
Price.Calculatedasanaverage
ofexecutionprice,weightedby
thenumberofsharestradedfor
theGBDA.
GDPA_BROKER_COUNT l Type:Numeric
l Width:3
CountofUniqueIDsofGBDA
Participants.
SnowflakeData-Five-DayRollingandIntradayTable(continued)
DTCCEquityKineticsUserGuide
FieldLayouts 12

---

## Page 13

FieldName Format Description
GDPA_CONCENTRATIONl Type:Numeric
l Width:6
l Decimal:4
SummationofGlobalBroker
Dealers'marketsharesquared.
Forspecifics,seeFrequently
AskedQuestionsonpage 22..
GDPA_RANK1 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthe
mostactiveClearingIDinthis
category.
GDPA_RANK2 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthe
secondmostactiveClearingID
inthiscategory.
GDPA_RANK3 l Type:Numeric
l Width:6
l Decimal:4
Anonymousmarketshareofthe
thirdmostact-iveClearingIDin
thiscategory.
REF_CODE l Type:Alphanumeric
l Width:2
Incaseswherethecountof
brokersintheGBDAgroupis
lessthan9,and"NA"willbe
displayed.
SnowflakeData-Five-DayRollingandIntradayTable(continued)
NOTESONDATA
KnownIssueforSomeAggregationValues
ThereisaknownissueforsomeaggregationvaluespriortoMay28,2016.Insuchcases,
reversal/correctiontradesmightbeincludedinaggregatecalculations.Asaresult,theseaggregationscan
beoverstated.Inthebulkofknowncases,theimpacttotheaggregationislessthan1%oftheaggregation
amount.Thiscircumstanceimpactedlessthan2%ofallaggregations.
UnderstatedAggregatesorMissingValues
Thereareminoranomaliesthatcausetheaggregationofthedatatobeunderreported.
DTCCEquityKineticsUserGuide
NotesOnData 13

---

## Page 14

1. LateTradeReporting: Occasionallyasmallnumberoftradesmaynotbeincludedduetolatetrade
reporting.Inallknowncasesthisimpacts<2%ofaggregatevolumepersymbol,pertrade,pertrade
side,andfewerthanfive(5)symbolsperdayareimpacted.
2. “Whenissued”Trades:Thesetradesarenotincludedinthereport.
Comparing1Day,Intraday,and/orFive-DayVolumes
Therearesomekeyfactstorememberwhenlookingatthedifferentaggregates.TheDailyservicewas
launchedinAugustof2018andtheIntraday;theFive-DayenhancementsbecameeffectiveinJuneof
2021.Historiccutsofalldatasetswerenotcreatedusingthecurrentproductionprocessandsome
differentrulesappliedtotheDailydataascomparedtotheIntradayandFiveDay.DuetoDTCC's
compliancerules,thevolumesintheIntradayandFiveDayareroundedtonearest1,000shares,however
theDailyformatdoesnothavethatrounding.ComparisonsofIndustryvolumeamountswilldifferbecause
oftherounding.Thehistorydatausedlegacydatabasetechnologiesandhaveafewknownanomalies
whichmaycauseunusualvaluestooccurinspecificcases.Theseanomalieshavebeennotedinthis
guideforanyknowncases.Itispossiblesimilarissuesexistonotherhistoricdates.
LegacyDatabaseValues
Duetolegacydatabaseissuesnotedinthepriorsection,thefollowingdateshavebeenidentifiedas
havinginconsistenciesbetweenthe1Day,FiveDay,and/orIntradayfiles.Theonlydatebelowthatthe
historicdatacamefromthecurrentdatabasetechnologywasMarch15,2021,thiswasduetoanisolated
productionissue.Noneofthesediscrepanciesarerelatedtothecodeusedtoaggregatethedata.
Onaverage,thenumberofsecuritiesimpactedperdaywas21fromJune1,2016topresent.Intheearlier
history,May31,2016andbackwards,theaveragewasaround1,000securitiesperday.Overall,thisissue
occursinlessthan1%ofalltheaggregatesacrosstheentirehistory.
Somesecuritieswillappeartohavegreaterorlowervolumethanexpectedwhencomparinganyofthe
aggregations:
l May25,2016–December31,2016:theIntradayandDailyvolumesequaleachotherformostIndustry
volumes.Thisissueisduetomissingtimestampsfromalegacydatabasetoolthathassincebeen
retired.Asaresult,theIntradayvolumeswillbeoverstatedonthesehistoricdates.
l Theissuesnotedabovewillimpactsomevaluesonthefollowingdates:
4/2/2012 7/31/20181/2/2019 6/11/201910/31/2019
2/26/20148/1/2018 1/3/2019 6/13/201911/1/2019
2/27/20148/2/2018 1/4/2019 6/14/201911/5/2019
2/28/20148/7/2018 1/9/2019 6/17/201911/7/2019
DTCCEquityKineticsUserGuide
NotesOnData 14

---

## Page 15

3/3/2014 8/9/2018 1/17/20196/18/201911/8/2019
3/4/2014 8/10/20181/25/20196/19/201911/11/2019
3/5/2014 8/13/20181/30/20196/20/201911/13/2019
3/6/2014 8/14/20181/31/20196/21/201911/14/2019
3/7/2014 8/15/20182/1/2019 6/24/201911/15/2019
3/10/20148/21/20182/4/2019 6/25/201911/18/2019
3/11/20148/22/20182/6/2019 6/26/201911/19/2019
3/12/20148/23/20182/8/2019 6/27/201911/22/2019
3/13/20148/24/20182/11/20196/28/201911/25/2019
3/14/20148/27/20182/14/20197/1/2019 11/26/2019
3/17/20148/28/20182/20/20197/2/2019 11/27/2019
3/18/20148/29/20182/21/20197/3/2019 12/2/2019
3/19/20149/4/2018 2/22/20197/5/2019 12/3/2019
DTCCisreviewingifoptionstoresolvethehistoricaldeviationscanbeaddressedinfuturereleases.There
areadditionaldetailsregardingthistopicinthenextsection,FrequentlyAskedQuestionsonpage 1.
April28,2022Refresh
AftertheApril1refresh,theissuesoutlinedaboveaffectthefollowingdates:
l 3/24/2017
l 7/15/2016
l 4/11/2016
l 3/15/2021
DTCCEquityKineticsUserGuide
NotesOnData 15

---

## Page 16

CALCULATIONSPECIFICS
ConcentrationValues
ConcentrationmetricsarecalculatedbasedontheHirschmanHerfindahlIndex.Calculationsoccursas
follows:
l Takeeachmemberofanaggregateandcalculateitsvolumemarketshare.
l Foreachmarketshare,takethesquareofitsvalue,orpowerof2.
l Sumthetotalofeachmarketsharesquaretofindtheconcentration.
ForeachaggregatecreatedintheDTCCETFKineticsservice,thevariousversionsofconcentration
calculatedarediscretelycreated,basedonthemembersaofaspecificaggregateand/ortimeperiod.
Forexample,thevalueknownas‘industryconcentration’isbasedonallbrokersforaparticular
security,tradedate,andtradeside.Theotherconcentrationmetrics(Tier1orGBDA)arecreated
basedonlyonthebrokersincludedinthataggregateforatradedateandtradeside.
ThetablesthatfollowcontainsamplecalculationsforeachConcentrationmetric.Alldatainthesetablesis
fakeor"dummy"data.
CompaniesTrading
Security Volume Rank GBDA Market
Share
MarketShare
Squared
Broker1 182,536 1 Y 0.1340 0.0179
Broker2 136,289 2 N 0.1000 0.0100
Broker3 131,030 3 N 0.0962 0.0092
Broker4 124,323 4 Y 0.0912 0.0083
Broker5 122,613 5 N 0.0900 0.0081
Broker6 104,000 6 Y 0.0763 0.0058
Broker7 83,278 7 Y 0.0611 0.0037
Broker8 59,648 8 N 0.0438 0.0019
Broker9 58,632 9 N 0.0430 0.0019
Broker10 47,987 10 N 0.0352 0.0012
Broker11 44,148 11 N 0.0324 0.0010
IndustryConcentration
DTCCEquityKineticsUserGuide
CalculationSpecifics 16

---

## Page 17

CompaniesTrading
Security Volume Rank GBDA Market
Share
MarketShare
Squared
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
CompaniesTradingSecurityVolume Rank MarketShare MarketShareSquared
Broker1 182,536 1 0.1738 0.0302
Broker2 136,289 2 0.1298 0.0168
Broker3 131,030 3 0.1248 0.0156
Broker4 124,323 4 0.1184 0.0140
Broker5 122,613 5 0.1167 0.0136
Broker6 104,000 6 0.0990 0.0098
Broker7 83,278 7 0.0793 0.0063
Broker8 59,648 8 0.0568 0.0032
Broker9 58,632 9 0.0558 0.0031
Broker10 47,987 10 0.0457 0.0021
TotalSharesTraded:1,050,336
Tier1Concentration:0.1148
Tier1Concentration
DTCCEquityKineticsUserGuide
CalculationSpecifics 17

---

## Page 18

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
SellandShortVolume
WhentheSellandShortSellvolume(and/orShortSellExemptVolume)aresummedforasingledateand
[[Equity]],thereareseveralscenariosthatrelatetothecomputationbalanceasitrelatestothebuyvolume.
l TheTier1andGDBAvolumeswillnotbalanceinmostcasesbecausethetradesidesarecomputed
independently.
l FortheDailyIndustryVolume,incaseswherethebuyandallsellmetricsareavailable(meaningnot
blockedbythethreshold),thesumoftheIndustrySellVolumesequalstheIndustryBuy,withafew
exceptionsnotedinthisdocument.
DTCCEquityKineticsUserGuide
CalculationSpecifics 18

---

## Page 19

FREQUENTLYASKEDQUESTIONS
1. WhenwasDTCCEquityKineticsfirstreleased?
Theoriginalversion(DailyAggregates)ofDTCCEquityKineticsservicewentliveinAugust,2018.
2. WhenweretheFive-DayandIntradayAggregatesreleased?
BothfeatureswereaddedinJune,2021.
3. Whyaresometickervalues"ZZZZ"?
TheZZZZvalueisoccasionallydisplayedonthedayanewissuebeginstradingorwhenthereisa
changeinsymbolduetotimingupofupdatestotheunderlyingsecuritymasterfile.Thequeryto
generatethisdatausesISINtocalculatetheaggregates.
4. Howmuchhistoricaldataisavailable?
TheDTCCEquityKineticsserviceincludeshistoricaldatadatingbacktoDecember1,2011viaa
one-timedelivery,asdetailedinthenexttable
Product HistoricalDatadatingbackto...
Buy 12/1/2011
Sell 12/1/2011
ShortSell* 2/10/2012
ShortSellExempt* 4/27/2012
*SECRule13h-1wasintroducedinNovember2015,requiringbrokerstoreportshortsale
transactionsinrealtime.Priortotherule,suchreportingwasoptionalandsomeofthesetrades
willhavebeenrecordedassellratherthanshortorshortsellexempt.Asaresult,theshortand
shortsellexemptvolumesinEquityKineticswillappearlowerinaggregatethanexpectedprior
totherulebeingineffect.FormoreinformationseeSecuritiesandExchangeCommissionSR-
[[NSCC]]-2015-004ontheSECwebsite.
5. HowmuchoftheU.S.equitymarketiscapturedintheDTCCEquityKineticsservice?
TheDTCCEquityKineticsservicecapturesaviewofactivityacrossallU.S.equityexchanges,[[ATS]],
anddarkpools.
6. Whatisthedatadeliveryformatandmethod?
DTCCEquityKineticsdataisdeliveredincomma-separated(CSV)files,standardoutputformat,
whichsubscriberscanloadintootherapplicationsorsystems.
7. Whenisdatadelivered?
DTCCEquityKineticsUserGuide
FrequentlyAskedQuestions 19

---

## Page 20

Dailyand5-DayRollingdataaredeliveredbeforethestartofeachbusinessday.Intradaydatais
deliveredby3PMET.DTCCdistributesDTCCEquityKineticsfilestosubscribers.Historicaldata
(fromDecember1,2011)isavailableviaaone-timedelivery.
8. HowdoestheDTCCEquityKineticsservicecomparetootherproductsinthemarket?
UserscangetvolumeandVWAPdatafromothersources,suchasexchangesandothermarket
datavendors.However,othersourcesdonothavebrokerattributiontoderivethevarious
aggregationsthatDTCChascreated,suchasTier1orthePeerGroups.
TheotherservicesalsolackextensiveviewsonequityshortactivitydeliveredonaT+1and/or
intradaybasis.DTCCEquityKineticsprovidesthisdatainaconsolidatedformat,whichisnot
availableelsewhere.
9. WhatdoesNAmeaninthepeerfeatures?
NAsignifiesthattherearenotenoughbrokerstradingtheissuetomeettheminimumthresholdto
displayvalues.
10. WhataretheDTCCEquityKineticsaggregationrules?
a. DTCCEquityKineticsdataisaggregatedbyTradeDateandSecurity.Theremustbeatleastten
uniquebrokerstradingtheissueforvaluestobedisplayed.
b. TheGlobalBroker-DealerAggregatemusthaveactivityfromall9uniquemembers.If1ormore
oftheGBDAmembersdoesnothaveactivity,allmetricsforthisaggregatearenotavailable.In
thesecases,avalueof"NA"appearsinthereferencefield.
c. Iftheconcentrationmetricisgreaterthan.5intheIntradayandFive-Dayviewsofthedata,the
con-centrationandmarketsharemetricsforthespecificaggregatearenotavailable.Thefields
willbeblankinsuchcases.
11. Doesindustryvolumeencompassallbrokers?
Yes,alistofallNSCCclearingmembersisavailableathttps://www.[[DTCC]].com/client-center/[[NSCC]]-
directories.
12. Howdoesthisdatacomparetoservicesthatinclude‘Tick’information?
Tickdataservicesshowindividualtransactionsandquotations,usuallysourcedfromexchanges.
DTCCEquityKineticsdeliversaggregatetradingmetricsbasedonactivityclearedthroughNSCC.
Althoughtickserviceshaveavalue,theydonotofferthesameinsightintothedepthofmarket,
brokercategorization,orextensiveshortsaledataonaT+1basisand/orIntradaybasisthatis
availableinDTCCEquityKinetics.
13. WhyaresomeTickervaluestruncated?
Sometickervaluesaregreaterthanfive(5)characters.TheDTCCEquityKineticsservicetruncates
anythingpastthefifthcharacter.
14. WhyaretheremultiplerowsforthesameISIN?
Theremaybetwo(2)ormoreaggregationsforthesameISINinthesecases:
DTCCEquityKineticsUserGuide
FrequentlyAskedQuestions 20

---

## Page 21

l Whenasymbolhaschangedduetomessagesusinglegacysymbols.
l Ifthetickerwasavailableinthesystemsaftertradesoccurred,thetickerwillinitiallybereflected
asUnknown.
15. HowaretheconcentrationvaluescalculatedfortheDTCCEquityKineticsservice?
ConcentrationmetricsarecalculatedbasedontheHirschmanHerfindahlIndex.Calculationsoccurs
asfollows
a. Takeeachmemberofanaggregateandcalculateitsvolumemarketshare.
b. Foreachmarketshare,takethesquareofitsvalue,orpowerof2.
c. Sumthetotalofeachmarketsharesquaretofindtheconcentration.
d. ForeachaggregatecreatedintheDTCCEquityKineticsservice,thevariousversionsofcon-
centrationcalculatedarediscretelycreated,basedonthemembersaofaspecificaggregate
and/ortimeperiod.Forexample,thevalueknownas‘industryconcentration’isbasedonall
brokersforaparticularsecurity,tradedate,andtradeside.Theotherconcentrationmetrics(Tier
1orGBDA)arecreatedbasedonlyonthebrokersincludedinthataggregateforatradedateand
tradeside.ThislogicalsoappliestotheIntradayandFive-dayaggregates.
e. ThetablesthatfollowcontainsamplecalculationsforeachConcentrationmetric.Alldatain
thesetablesisfakeor"dummy"data.
[[Companies]]
Trading
Security
Volume Rank GBDA Market
Share
Market
Share
Squared
Broker1 182,536 1 Y 0.1340 0.0179
Broker2 136,289 2 N 0.1000 0.0100
Broker3 131,030 3 N 0.0962 0.0092
Broker4 124,323 4 Y 0.0912 0.0083
Broker5 122,613 5 N 0.0900 0.0081
Broker6 104,000 6 Y 0.0763 0.0058
Broker7 83,278 7 Y 0.0611 0.0037
Broker8 59,648 8 N 0.0438 0.0019
Broker9 58,632 9 N 0.0430 0.0019
Broker10 47,987 10 N 0.0352 0.0012
Broker11 44,148 11 N 0.0324 0.0010
IndustryConcentration
DTCCEquityKineticsUserGuide
FrequentlyAskedQuestions 21

---

## Page 22

[[Companies]]
Trading
Security
Volume Rank GBDA Market
Share
Market
Share
Squared
Broker12 40,616 12 N 0.0298 0.0009
Broker13 37,367 13 Y 0.0274 0.0008
Broker14 34,378 14 Y 0.0252 0.0006
Broker15 31,627 15 N 0.0232 0.0005
Broker16 29,097 16 Y 0.0214 0.0005
Broker17 26,769 17 Y 0.0196 0.0004
IndustryConcentration(continued)
[[Companies]]
TradingSecurity Volume Rank Market
Share
Market
Share
Squared
Broker1 182,536 1 0.1738 0.0302
Broker2 136,289 2 0.1298 0.0168
Broker3 131,030 3 0.1248 0.0156
Broker4 124,323 4 0.1184 0.0140
Broker5 122,613 5 0.1167 0.0136
Broker6 104,000 6 0.0990 0.0098
Broker7 83,278 7 0.0793 0.0063
Broker8 59,648 8 0.0568 0.0032
Broker9 58,632 9 0.0558 0.0031
Broker10 47,987 10 0.0457 0.0021
Tier1Concentration
CompaniesTrading
Security Volume Market
Share
MarketShare
Squared
Broker1 182,536 0.2833 0.0802
GDPAConcentration
DTCCEquityKineticsUserGuide
FrequentlyAskedQuestions 22

---

## Page 23

CompaniesTrading
Security Volume Market
Share
MarketShare
Squared
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
GDPAConcentration(continued)
16. IftheSellandShortSellvolume(and/orShortSellExemptVolumearesummedforasingle
dateandequity,willthecomputationbalancewiththebuyvolume?
Severalscenariosapplytothisquestion:
l TheTier1andGDBAvolumeswillnotbalanceinmostcases,asthetradesidesarecomputed
inde-pen-dently.
l FortheDailyIndustryVolume,incaseswherethebuyandallsellmetricsareavailable(meaning
notblockedbythethreshold),thesumoftheIndustrySellVolumesequalstheIndustryBuywitha
fewexcep-tionsnotedinthisdocument.
l Inalimitednumberofscenarios,theselltotalsforIntradayvolumesmaylooklowerthanthebuys
duetotim-ingdifferencesatthetimeofthemid-daysnapshotusedtocreatetheIntradayview.
Thisissueoccursonaverageinlessthanoneequitypertradingday;intheknowncasesthedif-
ferentintotalvolumeislessthan.05%.
l DuetotheroundingofvolumesintheIntradayandFive-DayAggregate,therecanbeanetdif-
ferenceofupto2000sharesduetothenumbersbeingrounded.Asaresult,thesumofthe
Industrysellandshortsellvolumeamountscomparedtotheindustrybuyvolumemaydifferin
somecases.
DTCCEquityKineticsUserGuide
FrequentlyAskedQuestions 23

---

## Page 24

PRODUCTSUPPORTAND
DOCUMENTATION
UsethefollowinginformationtocontactDTCCDataServicessupport:
l Phone:CalltheClientContactCenterat1-888-382-2721andselectoption8.
l Email:DataServicesSupport(dataservicessupport@[[DTCC]].com).
l Web:https://www.dtccdata.com/contact-us-support.
l ConnectivityandSFTPSupport:DirectallconnectivityandSFTPsupportinquiriesthoughthe
MyDTCC.comsupportportal>ConnectivityManagement.Theseinquiriesinclude
o WhitelistingIPaddresses
o Missingfiles
o SFTPpasswordchanges
o Filenameupdates
l ToobtainFileSpecifications,FAQs,andSampleFiles,logontotheDTCCLearningCenter.
Notes
l Forrequestsrequiringnetworkupdates,suchaswhitelistingIPaddresses,youmustnotify
DTCCatleast10businessdayspriortotheeffectivedate.
l Contactdataservicessupport@[[DTCC]].comforaccesstoMyDTCC.com.
DTCCEquityKineticsUserGuide
ProductSupportAndDocumentation 24

---

## Page 25

©2023.Allrightsreserved.[[DTCC]],[[DTCC]](Stylized)andFinancialMarkets.Forward.areregisteredandunregistered
trademarksofTheDepositoryTrust&ClearingCorporationDTCC.Theservicesdescribedhereinareprovidedunder
the“[[DTCC]]”brandnamebycertainaffiliatesofTheDepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitself
doesnotprovidesuchservices.Eachoftheseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsof
theparticularcountryorcountriesinwhichsuchentityoperates.Pleaseseewww.[[DTCC]].comformoreinformationon
[[DTCC]],itsaffiliatesandtheservicestheyoffer.
DocDate:November17,2023
PublicationCode:DAT320
Service:EquityKinetics
Title:UserGuide
ForMoreInformation
EmailDTCCLearningat:
DataLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com