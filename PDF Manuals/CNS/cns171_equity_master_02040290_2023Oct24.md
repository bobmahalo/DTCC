---
title: "CNS Equity Master File - Production AutoRoute ID: 02040290"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cns171_equity_master_02040290_2023Oct24.pdf"
pages: 5
size: "310.4 KB"
category: "CNS"
ingested_on: "2026-06-05"
---

# CNS Equity Master File - Production AutoRoute ID: 02040290

**Original File:** [cns171_equity_master_02040290_2023Oct24.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cns171_equity_master_02040290_2023Oct24.pdf)  
**Category:** CNS  
**Total Pages:** 5  
**File Size:** 310.4 KB  

---

## Page 1

[[CNS]]®
CNSEQUITYMASTERFILE- PRODUCTION
AUTOROUTEID:02040290
NOVEMBER6,2020
DocumentChangeHistory
Thefollowingtableshowsthechangehistoryforthisdocument:
VersionDate Summary
1.0 September9,
2014
Firstdraftofthedocument.
2.0 January7,
2015
l AddedSecurityTradingStatus.
l UpdatedFiledeliverytime.
3.0 September28,
2018 ImportantNotice#Z0169hasbeenpublished.
http://www.[[DTCC]].com/~/media/Files/pdf/2018/8/6/Z0169.pdf
4.0 June3,2020 DTCEligibilityIndicatorisnolongerpublished.
5.0 November5,
2020
Dailydistributiontimeforthisfilehaschangedfrom5:P.M.toapproximately
5:30P.M.Eastern Time.
FileContent
TheTrading/ClearingEquityMasterfilecontainsallactivelytradedandsuspendedequitiesavailablein
[[NSCC]].

---

## Page 2

FileDelivery
ThefileisavailablethroughtheAutoRouteProductID02040290.ItisproducedontheNSCCbusiness
dayatapproximately5:30P.M.andcontainsthesnapshotofdataasof5:30P.M.Eastern Time.
RecordLayout
ThefollowingtableshowstherecordlayoutforCNSEquityMasterFile-ProductionAutoRouteID:
02040290:
AutoRouteID02040290
RecordLayout
RecordLength=80
FieldName Length Start End Type Comments
[[CUSIP]] 9 1 9 A/N Nine-characternumberandletterformatasdes-
ignatedbytheCommitteeonUniformSecurities
IdentificationProcedures([[CUSIP]]).
WhenIssued
Indicator
1 10 10 A/N IndicatesifasecurityisWhenIssuedorRegular
Way.
Values:
l 0–RegularWay
l 1–WhenIssued
Foreign
DomesticIndic-
ator
1 11 11 A/N Indicatesifasecurityisdomesticorforeign.
l 0–Domestic
Defaultforallsecurities.
ExchangeIndic-
ator
1 12 12 A/N Exchangeonwhichasecurityislisted.
Values:
l 0–NewYorkStockExchange
l 1–NYSEAmexEquitiesExchange
l 2–OTCExchange
SecuritySym-
bol
15 13 27 A/N Abbreviationusedtouniquelyidentifypublicly
tradedsharesofaparticularstockonaparticular
stockmarket.
ProductionAutoRouteID:02040290
2

---

## Page 3

AutoRouteID02040290
RecordLayout
RecordLength=80
FieldName Length Start End Type Comments
CNSEligibility
Indicator
1 28 28 A/N IndicatesifasecurityiseligibleforCNSthrough
[[NSCC]].
Values:
l 0–Non-CNSEligible
l 1–CNSEligible
l 2–Suspended
DTCEligibility
Indicator
1 29 29 A/N NolongerpublishedasofFebruary25,2019.
Spaces.
SpecialTrade
Indicator
1 30 30 A/N IndicatesifthereisanytypeofNSCCspecial
processingrequiredforthissecurity.
Values:
l 0–NoSpecialTradeProcessing
l 1–ForeignSecurityNetting
l 3–NSCCSpecialTrade
Security
Description
35 31 65 A/N SecurityShortdescription
TradingDMM
(Designated
Market
Maker)
4 66 69 A/N Amarketmakerthatisobligatedtomaintainfair
andorderlymarketsforanassignedsetoflisted
firms.
Blank–PerImportantNotice#Z0169.
l ForNYSEandAMEXExchanges–Floor
ClearingNumber.
l ForOTCExchanges–Zeroesorspaces.
DMMClearing
Agent
4 70 73 A/N NSCCClearingAgent.
Blank–PerImportantNotice#Z0169.
l ForNYSEandAMEXExchanges–Spe-
cialistNumber.
l ForOTCExchanges–Zeroesorspaces.
ProductionAutoRouteID:02040290
3

---

## Page 4

AutoRouteID02040290
RecordLayout
RecordLength=80
FieldName Length Start End Type Comments
PostNumber 2 74 75 A/N SpecialPostNumber.
Blank–PerImportantNotice#Z0169.
l ForNYSEandAMEXExchanges–Post
Number.
l ForOTCExchanges–Spaces.
PanelID 2 76 77 A/N PanelID.
Blank–PerImportantNotice#Z0169.
l ForNYSEandAMEXExchanges–Panel
[[ID]].
l ForOTCExchanges–Spaces.
UnitOfTrade 1 78 78 A/N Minimumquantityofasecurityrequiredfor
regulartradingpurposes.
Values:
l 0–1-ShareRound-Lot
l 1–10-ShareRound-Lot
l 2–25-ShareRound-Lot
l 3–50-ShareRound-Lot
l 4–100-ShareRound-Lot
l 5–1000-ShareRound-Lot
SecurityTrad-
ingStatus
1 79 79 A/N IndicatesifasecurityiseligibleforTrading
throughNSCC.
Values:
l 1–Active
l 2–Suspended
Filler 1 80 80 A/N Reservedforfutureuse.
ENDOFRECORD
ProductionAutoRouteID:02040290
4

---

## Page 5

© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]]. The services described herein are 
provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). 
[[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and 
regulations of the particular country or countries in which such entity operates. Please see www.[[DTCC]].com for more 
information on [[DTCC]], its affiliates and the services they offer.
Doc Date: October 24, 2023
Publication Code: CNS171
Service: [[CNS]]
Title: [[CNS]] [[Equity]] Master File - Production AutoRoute [[ID]]: 02040290
For More Information
Email [[DTCC]] Learning at:
corelearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com