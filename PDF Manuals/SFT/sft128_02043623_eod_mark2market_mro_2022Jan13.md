---
title: "SFT Clearing EOD Mark-to-Market MRO AutoRoute ID: Production 02043623 / PSE 02983623"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sft128_02043623_eod_mark2market_mro_2022Jan13.pdf"
pages: 4
size: "533.7 KB"
category: "SFT"
ingested_on: "2026-06-05"
---

# SFT Clearing EOD Mark-to-Market MRO AutoRoute ID: Production 02043623 / PSE 02983623

**Original File:** [sft128_02043623_eod_mark2market_mro_2022Jan13.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sft128_02043623_eod_mark2market_mro_2022Jan13.pdf)  
**Category:** SFT  
**Total Pages:** 4  
**File Size:** 533.7 KB  

---

## Page 1

SECURITIESFINANCING
TRANSACTION([[SFT]])CLEARING
EODMARK-TO-MARKETMROAUTOROUTEID:PRODUCTION02043623/PSE  02983623
JANUARY13,2022


---

## Page 2

EndofDay([[EOD]])Mark-to-MarketMROAutoRouteID:Production02043623/PSE02983623 2
ENDOFDAY([[EOD]])MARK-TO-MARKETMROAUTOROUTEID:PRODUCTION02043623/ PSE02983623
TheEndofDayMark-to-MarketMROisafilesubmittedbyNSCCaftertheDTCdropcutofftime.AMembercanuse
thisfiletobalancetheirnetdebit/creditofmarksforPriceDifferentialanddeliverorder([[DO]])off-legreturns(notrolled)
thatdidnotsettleatDTCwhereNSCChadtoprocessamark-to-marketontheunsettledtransaction.Thesemarkswill
beappliedtoafirm’sFedFundssettlement(FFS)code131balance(SFTMarks)ontheirNSCCParticipantAccount
Statement.
Note
Theendofdaymark-to-marketMROisfromNonReturnFailsandPriceDifferentialsthatdidnotsettleatDTC.
HeaderRecord
ThefollowingtableshowtheHeaderrecorddetailsfortheEODMark-to-MarketMROAutoRouteID:Production
02043623/PSE 02983623:
AutoRouteIDProduction02043623/PSE 02983623
HeaderRecord
RecordLength=300
No Description Length Start End Type Comments
1 ProcessingDate 8 1 8 A/N Format:
MMDDCCYY
2 Filler 272 9 300 A/N Forfutureuse.
ENDOFRECORD
DetailRecord
ThefollowingtableshowtheDetailrecorddetailsfortheEODMark-to-MarketMROAutoRouteID:Production
02043623/PSE 02983623:
AutoRouteIDProduction02043623/PSE 02983623
DetailRecord
RecordLength=300
No Description LengthStartEndTypeComments
1 ClearingMemberID 8 1 8 A/N PartyreceivingtheMROfile.
2 SFTClearing
MemberID
8 9 16 A/N SFTmemberA/CoftheClearingmember.
3 DTCCReferenceID 14 27 30 A/N DTCCReferenceIDfortheloanthathadanEODmark-to-
market.
4 [[CUSIP]] 9 31 39 A/N CUSIPoftheloanedshares.
5 ISIN 12 40 51 A/N ISINIDoftheloanedshares.
6 ClientOrderID 32 52 83 A/N ClientOrderIDfortheSFTmember.
AutoRouteID:Production02043623/PSE 02983623

---

## Page 3

EndofDay([[EOD]])Mark-to-MarketMROAutoRouteID:Production02043623/PSE02983623 3
AutoRouteIDProduction02043623/PSE 02983623
DetailRecord
RecordLength=300
No Description LengthStartEndTypeComments
7 ExecutionID 32 84 115 A/N VendororMarketplaceuniquereference.
8 ShareQuantity 11 116 126 N Sharequantityoftheoutstandingloan.
9 SideIndicator 1 127 127 A/N l D=Delivererofthesecurity([[Borrower]])
l R=Receiverofthesecurity(Lender)
10 SettlementDate 8 128 135 A/N Settlementdate.
Format:YYYYMMDD
11 [[mark-to-market]]
Amount
17 136 152 N DifferencebetweenthepriordayLoanSettlementAmount
oftheloanandnewLoanSettlementAmountforthe
outstandingLoanQuantity.
12345678901234512
Thefirstfifteendigitsareintegersandthelasttwodigits
aredecimals.
12 [[mark-to-market]]
AmountIndicator
1 153 153 A/N l D=DebitofMark-to-Market
l C=CreditofMark-to-Market
13 Contra
Clearing [[Member]] [[ID]]
8 154 161 A/N OriginalContrapartytothatloantransaction.
14 ContraSFTClearing
MemberID
8 162 169 A/N OriginalSFTClearingmemberaccountofthecontraparty
tothatloantransaction.
15 Filler 170 130 300 A/N Forfutureuse.
ENDOFRECORD
AutoRouteID:Production02043623/PSE 02983623

---

## Page 4

FORMOREINFORMATION
EmailDTCCLearningat:
corelearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com
©2022DTCC.Allrightsreserved.[[DTCC]],[[DTCC]](Stylized),ADVANCINGFINANCIALMARKETS.TOGETHER,
andtheInterlockergraphicareregisteredandunregisteredtrademarksofTheDepositoryTrust&Clearing
Corporation.
Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandnamebycertainaffiliatesofTheDepositoryTrust
&ClearingCorporation(“[[DTCC]]”).DTCCitselfdoesnotprovidesuchservices.Eachoftheseaffiliatesisaseparate
legalentity,subjecttothelawsandregulationsoftheparticularcountryorcountriesinwhichsuchentityoperates.
Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,itsaffiliatesandtheservicestheyoffer.
DocInfo:January13,2022
PublicationCode:SFT128
Service:SecuritiesFinancingTransaction([[SFT]])Clearing
Title:EODMark-to-MarketMROAutoRouteID:Production02043623/PSE 02983623