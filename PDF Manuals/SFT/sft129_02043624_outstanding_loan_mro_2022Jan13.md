---
title: "SFT Clearing Outstanding Loan MRO AutoRoute ID: Production 02043624 / PSE 02983624"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sft129_02043624_outstanding_loan_mro_2022Jan13.pdf"
pages: 7
size: "547.6 KB"
category: "SFT"
ingested_on: "2026-06-05"
---

# SFT Clearing Outstanding Loan MRO AutoRoute ID: Production 02043624 / PSE 02983624

**Original File:** [sft129_02043624_outstanding_loan_mro_2022Jan13.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sft129_02043624_outstanding_loan_mro_2022Jan13.pdf)  
**Category:** SFT  
**Total Pages:** 7  
**File Size:** 547.6 KB  

---

## Page 1

SECURITIESFINANCING
TRANSACTION([[SFT]])CLEARING
OUTSTANDINGLOANMROAUTOROUTEID:PRODUCTION02043624/PSE02983624
JANUARY13,2022


---

## Page 2

OutstandingLoanMROAutoRouteID:Production02043624/PSE02983624 2
OUTSTANDINGLOANMROAUTOROUTEID:PRODUCTION02043624/ PSE02983624
TheOutstandingLoanMROisanend-ofdayfilethatwillbedistributedbyNSCC.ItwillreporttoeachMembertheir
street-sideSFTsthatareoutstandingwithNSCCattheendofthebusinessday,whichisaround5:30P.M.Eastern
Time.ItwillalsoreportallopenrecallsagainstthoseSFTs.Thefilewillbedistributedatapproximately5:45P.M.
EasternTime.AMembercanusethisfiletobalancetheirnetdebit/creditofovernightrebateinterest.Thisinterestwill
beappliedthenextbusinessdaytotheirFedFundssettlement(FFS)code130balance(RebateInterest)ontheir
NSCCParticipantaccountstatement.
TherewillbethreerecordtypesforthisMROasoutlinedbelow.
l HeaderRecordwiththeprocessingdate–Onerecordperparticipant.
l OutstandingLoanDetailRecord–OnepereachoutstandingSFTforeachparticipatingSFTClearingMember.
l LoanRecallDetailRecord(ifany)–OnepereachopenrecallforeachparticipatingSFTClearingMember.The
recalldetailsectionwillonlybepopulatediftheRecallIndicatorfield=YintheOutstandingLoandetailrecord(Byte
293).
HeaderRecord
ThefollowingtableshowtheHeaderrecorddetailsfortheOutstandingLoanMROAutoRouteID:Production
02043624/PSE 02983624:
 AutoRouteIDProduction02043624/PSE02983624
HeaderRecord
Length=400
No Description Length Start End Type Comments
1 ProcessingDate 8 1 8 A/N Format:
MM/DD/CCYY
2 Filler 392 9 400 A/N Forfutureuse.
ENDOFRECORD
AutoRouteID:Production02043624/PSE02983624

---

## Page 3

OutstandingLoanMROAutoRouteID:Production02043624/PSE02983624 3
LoanDetailRecord
ThefollowingtableshowtheLoanDetailrecorddetailsfortheOutstandingLoanMROAutoRouteID:Production
02043624/PSE 02983624:
 AutoRouteIDProduction02043624/PSE02983624
LoanDetailRecord
Length=400
No Description LengthStartEnd TypeComments
1 SFTClearingMember
[[ID]]
8 1 8 A/N SFTClearingMemberaccountoftheClearing
[[Member]].
2 ClearingMemberID 8 9 16 A/N PartyreceivingtheMROfile.
3 Recordtype 2 17 18 A/N L=Loan
4 DTCCReferenceID 14 19 32 A/N DTCCReferenceIDoftheoutstandingloan.
5 SideIndicator 1 33 33 A/N l D=Deliverer/Returneroftheshares([[Borrower]])
l R=Receiveroftheshares(Lender)
6 LegIndicator 1 34 34 A/N O=Off-leg
7 LoanStatus 4 35 38 A/N PEND=PendingSettlement
8 SettlementDate 8 39 46 A/N Settlementdate.
Format:YYYYMMDD
9 ISIN 12 47 58 A/N SecurityISINIDoftheloanedshares.
10 [[CUSIP]] 9 59 67 A/N SecurityCUSIPIDoftheloanedshares.
11 ShareQuantity 11 68 78 N Sharequantityoftheoutstandingloan.
12 SharePrice 13 79 91 N Priceofsecurityinloantransaction.
1234567123456
Thefirstsevendigitsareintegersandthelastsix
digitsaredecimals.
13 ContractAmount 17 92 108 N Calculatedcontractamountoftheloantransaction.
(ShareQuantity*SharePrice)
12345678901234512
Thefirstfifteendigitsareintegersandthelasttwo
digitsaredecimals.
14 IndependentAmount
Rate
10 109 118 N RateforIndependentAmountcalculation.
1234561234
Thefirstsixdigitsareintegersandthelastfourdigits
aredecimals.
15 IndependentAmount 17 119 135 N CalculatedIndependentAmount.
12345678901234512
Thefirstfifteendigitsareintegersandthelasttwo
digitsaredecimals.
AutoRouteID:Production02043624/PSE02983624

---

## Page 4

OutstandingLoanMROAutoRouteID:Production02043624/PSE02983624 4
 AutoRouteIDProduction02043624/PSE02983624
LoanDetailRecord
Length=400
No Description LengthStartEnd TypeComments
16 RoundingRuleCode 1 136 136 A/N IndicatesRoundingRuleforSettlePriceCalculation:
l 0=Norounding
l 1=Uptothenearest$0.01
l 2=Uptonearest$0.05
l 3=Uptonearest$0.10
l 4=Uptonearest$0.25
l 5=Uptonearest$1.00
17 SettlementPrice 13 137 149 N CalculatedsettlementpricetodeterminetheLoan
SettlementAmount.
1234567123456
Thefirstsevendigitsareintegersandthelastsix
digitsaredecimals.
18 SettlementAmount 17 150 166 N OutstandingContractAmountofDTCCReferenceID.
12345678901234512
Thefirstfifteendigitsareintegersandthelasttwo
digitsaredecimals.
19 RebateInterestAmount17 167 183 N Calculatedas:
(LoanOutstandingSettlementValue*Numberof
Days*Rate)/360
12345678901234512
Thefirstfifteendigitsareintegersandthelasttwo
digitsaredecimals.
20 RebateInterestAmount
Indicator
1 184 184 A/N l D=DebitofRebateInterest
l C=CreditofRebateInterest
l Spaces=NoRebateInterest
21 Lending/InterestRate
Indicator
1 185 185 A/N l N=NoRate
l B=PaidtoOriginalBorrower
l L=PaidtoOriginalLender
22 Lending/InterestRate 10 186 195 N RateforInterestAmountcalculation.
1234561234
Thefirstsixdigitsareintegersandthelastfourdigits
aredecimals.
AutoRouteID:Production02043624/PSE02983624

---

## Page 5

OutstandingLoanMROAutoRouteID:Production02043624/PSE02983624 5
 AutoRouteIDProduction02043624/PSE02983624
LoanDetailRecord
Length=400
No Description LengthStartEnd TypeComments
23 Corporate
Action Indicator
1 196 196 A/N Securityloanisundergoinganupcomingcorporate
action.
l N=NoActiveCorpActionsfortheSecurity
l Y=SecurityisunderCorpAction
24 ExecutingParticipantID8 197 204 A/N ExecutingParticipantIDforthemajororparty
receivingtherecord.
25 IntroducingParticipant
[[ID]]
8 205 212 A/N IntroducingParticipantIDforthemajororparty
receivingtherecord
26 ClientOrderID 32 213 244 A/N ClientOrderIDoftheSFTClearingMember.
27 ExecutionID 32 245 276 A/N VendororMarketplaceuniquereferenceID.
28 ContraClearing
MemberID
8 277 284 A/N OriginalContraParticipantIDtotheloantransaction.
29 ContraSFTClearing
MemberID
8 285 292 A/N OriginalSFTClearingMemberaccountofthecontra
partytotheloantransaction.
30 RecallIndicator 1 293 293 A/N l Y=Recall
l N=Norecall
IfpopulatedwithaY,seetheRecallDetailRecord.
31 Filler 107 294 400 A/N Forfutureuse.
ENDOFRECORD
AutoRouteID:Production02043624/PSE02983624

---

## Page 6

OutstandingLoanMROAutoRouteID:Production02043624/PSE02983624 6
RecallDetailRecord
ThefollowingtableshowtheRecallDetailrecorddetailsfortheOutstandingLoanMROAutoRouteID:Production
02043624/PSE 02983624:
 AutoRouteIDProduction02043624/PSE02983624
RecallDetailRecord
Length=400
No Description LengthStartEnd TypeComments
1 SFTClearing
MemberID
8 1 8 A/N SFTClearingMemberaccountoftheClearingmember.
2 ClearingMemberID 8 9 16 A/N IDoftheClearingMember.
3 Recordtype 2 17 18 A/N R=Recall
4 DTCCReferenceID 14 19 32 A/N DTCCReferenceIDoftheoutstandingloan.
5 RecallID 2 33 34 A/N DTCCRecallID
6 RecallStatus 4 35 38 A/N OPEN=Open
7 RecallDate 8 39 46 A/N Datewhentherecallwasinitiated.
Format:YYYYMMDD
8 ISIN 12 47 58 A/N SecurityISINIDoftherecalledshares.
9 [[CUSIP]] 9 59 67 A/N SecurityCUSIPIDoftherecalledshares.
10 ShareQuantity 11 68 78 N Sharequantityoftheoutstandingrecall.
11 AllowedDateof
Execution
8 79 86 A/N Recallallowedexecutiondate.
Format:YYYYMMDD
12 RecallTime 8 87 94 A/N TimewhentherecallwasreceivedbySAS.
Format:HH.MM.SS
13 Filler 306 95 400 A/N Forfutureuse.
ENDOFRECORD
AutoRouteID:Production02043624/PSE02983624

---

## Page 7

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
PublicationCode:SFT129
Service:SecuritiesFinancingTransaction([[SFT]])Clearing
Title:OutstandingLoanMROAutoRouteID:Production02043624/PSE02983624