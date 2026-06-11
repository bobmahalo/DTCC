---
title: "SFT Clearing Service: Input and Output Message Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sft134a_input_output_2022Jul13.pdf"
pages: 71
size: "1864.6 KB"
category: "SFT"
ingested_on: "2026-06-05"
---

# SFT Clearing Service: Input and Output Message Layouts

**Original File:** [sft134a_input_output_2022Jul13.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sft134a_input_output_2022Jul13.pdf)  
**Category:** SFT  
**Total Pages:** 71  
**File Size:** 1864.6 KB  

---

## Page 1

[[securities]] FINANCING TRANSACTION 
([[SFT]]) CLEARING
INPUT AND OUTPUT MESSAGE LAYOUTS
MARCH 3, 2022


---

## Page 2

MESSAGE LAYOUTS
Message and File Types
TosupportSFTprocessing,DTCCleveragesexistingclientinterfaces.Theseinclude
l Universal Trade Capture (UTC)
TheUTCdatafeedcomprisesaseriesofvariable-lengthsequencedmessagesfollowingthe FIXversion4.4conventions .WhiletheFIXtag-based
structureisleveraged,messagesmaybesentthroughtheFIXengineorMessageQueue(MQ).
Formoreinformationabouttagstructureandrequirements,seethe UniversalTradeCapture(UTC)UserGuide locatedintheDTCCLearningCenter.
l [[securities]] Financing Accounting System (SAS)
AsaresultofleveragingNSCC’sCNSprocessingstructure,theSASinterfaceallowsISOmessagingfortransactioninputandoutputandmachine-
readableoutput(MRO)forendofdayfiles.Formoreinformation,seethe [[SFT]] ClearingTechnicalResources sectionintheDTCC LearningCenter.
l [[DTC]]
DTCprocessingincludesnewsettlementcodestosupportSFTprocessing;however,themessaginginterfacestructurewillnotchange.
SFTClearing:InputandOutputMessageLayouts
MessageLayouts 2

---

## Page 3

UTCMessageTypes
WiththeSFTClearingservice,thereareeightmessagetypesthatcanbesubmittedforprocessingtotheUTCsystem.Forallmessagetypes,the
counterpartiesonthemessageshouldalwaysbepopulatedintheirroleofhowtheon-legwasoriginallysubmittedtoDTCC.Forexample,ifBroker0123
wastheoriginalborrower([[Buyer]])onthenewLoanMessageandBroker0122wasthelender([[Seller]]),forallothermessagessubmittedtoDTCCregarding
thatsameDTCCReferenceID,suchasSend-to-Settle,Broker0123shouldalwaysbetheborrower([[Buyer]])and0122thelender([[Seller]]).
TheoutputfromtheUTCsystemisbaseduponhowtheinputwassubmitted.ThefollowingtableprovidesadescriptionofalltheSFTClearingmessage
types:
Note
AlltimesareinEasternTime(ET).
MessageTypeInputavailability: Cutoff SubmissionRules:
NewLoan
(Street-side)
4:00A.M. -3:00 P.M. ETAnewSFTbetweentwoSFTmemberswheretheon-leg([[shares]]
andsettlementvalue)isprocessedtosettlethroughtheNSCC
ClearingaccountatDTC.Afterthattransactionsettles,theoff-leg
thatissettobereturnedthenextbusinessdaywillbenovatedto
[[NSCC]].
Pre-established
Bilateral Loan
4:00A.M.-3:00P.M.ET AnewSFTbetweentwoSFTmemberswheretheon-leg([[shares]]
andsettlementvalue)alreadysettleddirectlybetweentheSFT
membersatDTC.Uponreceipt,theoff-legthatissettobereturned
thenextbusinessdaywillbenovatedtoNSCC.
Roll 4:00 A.M. - 11:30 A.M. ETAnewSFTbetweentwoSFTmembersthatinstructsNSCCtonet
thenewSFTagainstanoff-legSFTthatissettobereturnedthe
currentbusinessday.ThisresultsinNSCCprocessingaPrice
DifferentialchargethatwillsettlebetweentheSFTmembersthrough
theNSCCClearingaccountatDTC.
SFTClearing:InputandOutputMessageLayouts
MessageLayouts 3

---

## Page 4

MessageTypeInputavailability: Cutoff SubmissionRules:
Send-to-Settle4:00A.M.-3:00P.M.ET AtransactionmessagebetweentwoSFTmemberssubmitted
againstanexistingoff-legreturn.Dependingonthestatusofthe
DTCCReferenceID,itdoesthefollowing:
l Acceleratesthefullsharereturnoftheoff-legbefore11:30A.M.
ETontheoriginal(orcurrent)settlementdateoftheoff-legSFT
return.
l Acceleratesthefullorpartialsharereturnoftheoff-legfromthe
original(ornext)settlementdatetothecurrentsettlementdate.
l Ifthemessageisbeingusedfor
NewLoans,thequantityfieldmust
besubmittedwiththefullshare
amountoftheDTCCReference
[[ID]].
l Ifthemessageisbeingusedfor
Pre-establishedBilateralLoans,
thequantityfieldcanbesubmitted
withaquantityequaltoorless
thantheDTCCReferenceIDof
theoff-legreturnpendinginthe
database.
CancelMessage4:00A.M.–3:00P.M.ET AtransactionmessagebetweentwoSFTmemberssubmitted
againstanexistingon-legoroff-legreturn.Dependingonthestatus
oftheDTCCReferenceID,itdoesoneofthefollowing:
l Cancelstheon-legDOtransactionthatisPendingatDTC(from
receiptofaNewLoanMessage).
l Cancelstheon-legPriceDifferentialchargethatisPendingat
[[DTC]](fromreceiptofarolltransaction).
l CancelsaPendingDOoff-legreturnatDTCaftera
Send-to-Settlemessagewassubmittedthatacceleratedthe
returnofsharesfromthenextbusinessdaytothecurrent
businessday.
l Ifthemessageisbeingusedfor
NewLoansorPre-established
BilateralLoans,thequantityfield
mustbesubmittedwiththefull
shareamountoftheDTCC
ReferenceIDalongwiththe
correctTag66value.
l Ifthemessageisbeingusedfor
Rolls,thequantityfieldmustbe
submittedwithaquantityequalto
aSend-to-Settlemessagethat
waspreviouslysubmittedwhich
generatedtheoff-legreturn
PendingatDTCalongwiththe
correctassociatedTag66value.
SFTClearing:InputandOutputMessageLayouts
MessageLayouts 4

---

## Page 5

MessageTypeInputavailability: Cutoff SubmissionRules:
Rate
Modification
4:00 A.M. - 3:45 P.M. ETAtransactionbetweentwoSFTmemberssubmittedagainstan
existingDTCCReferenceID.ThisinformsNSCCthateither1)the
lendinginterestrateontheoutstandingSFThasbeenupdatedor2)
thepartywhoisgettingpaidtheinteresthasbeenupdated.[[NSCC]]
willusethisupdatedlendingratetocalculatetheovernightrebate
interest.
Ratemodificationmessagescanbe
receivedanytimeofthedayuntil3:45
P.M.ET.
Loan
Termination
4:00A.M.-4:30P.M.ET AtransactionbetweentwoSFTmemberssubmittedagainstan
existingDTCCReferenceID.ThisinstructsNSCCtoremovethe
outstandingDTCCReferenceIDfromclearing.
SFTTerminationscanonlybe
processedagainstanoff-legreturnat
thefollowingtimesduringthecourse
ofabusinessday:
l Until11:30A.M.ET(onthe
originalSDitwassettobe
returned)aslongastheoff-leg
returnwasnotrolledortheDO
returnwasnotsenttoDTCfor
[[settlement]].
l Anytimeduringtheday(onthe
samedaytheon-legsettledand
theoff-legreturnissettobe
returnedthenextbusinessday)
providednoSend-to-Settle
Messagewasreceivedorifa
Send-to-SettleMessagewas
received,thereisnoDOPending
atDTC.
l AfterDTCSettlementDROP
cutoff4:30P.M.ET(Termination
cutofftime).
SFTClearing:InputandOutputMessageLayouts
MessageLayouts 5

---

## Page 6

MessageTypeInputavailability: Cutoff SubmissionRules:
Buy-side 4:00A.M.-3:00P.M.ET AnSFTbetweenanSFTmember,suchasaSponsoringMember
andtheirSponsoredMembers.TheSponsoringMembermayenter
intoaback-to-backtradewhentheyaretakingonaprincipallending
orprincipalborrowingrelationshipwithaSponsoredMember.  The
back-to-backtradehasNSCCinthemiddleofallobligationsand,as
such,NSCCisthecentralcounterpartytoallpartiesofthe
transaction.ThereisnoDTCsettlementonthetransaction.
SFTClearing:InputandOutputMessageLayouts
MessageLayouts 6

---

## Page 7

UTC  InputandOutputFormats
ThefollowingtableprovidesadescriptionforalltheUTCinput/outputformats:
Format Description
InputFormats
UTCInputFix/MQ Format InputformatsusedbytheApprovedSFTSubmittertosubmitbuy-sideand/orstreet-sideSFTmessage
transactionstoUTCusingtheFIXprotocolviaFIXengineorMQchannel.
UTCInputEODTotalsFIX/MQFormat InputformatusedbytheApprovedSFTSubmitterthatrecapsthenumberofSFTmessagetransactions
theysenttoUTCfortheprocessingday.ThiswillbeanEndofDay([[EOD]])balancingmessagewhichwillbe
thelasttransactionmessageofthedaysentbytheApprovedSFTSubmitter.Afterthismessageissent,no
moremessagetransactionswillbeacceptedfromthatApprovedSFTSubmitterforthatprocessingday.
TheEODmessagewillbeusedbyUTCforreconciliation.
OutputFormats
UTCOutputFIX/MQFormat OutputformatsentbyUTCtotheApprovedSFTSubmitterandSFTClearingMembersthatprovidesareal
timeupdatestatus(eitherAcceptedorRejected)ofeachSFTmessagetransactionthatwasreceivedafter
inputsubmission.
Note:ArejectedmessageisjustsenttotheApprovedSFTSubmitter.
UTCOutboundGapFillRequestFIX/MQ
Format
OutputformatsentbytoUTCtotheApprovedSFTSubmittertoalertthemthatamessagetransactiongap
wasdetectedbyUTC.
UTCOutboundEODConfirmationtoMarket
FIX/MQFormat
OutputformatsentbyUTCastheendofdayconfirmationtothemarket.
UTCOutboundBuy-SideCutoffFIX/MQ
Format(3:00P.M.ET)
OutputformatsentbyUTCtotheSponsoringSFTClearingMembertoalertthemthatmaturingoff-leg
returntransactions(betweenthemandtheirSponsors)havebeenreleasedfromNSCCsguaranty
obligation.
UTCOutboundEODMessagesto
ParticipantsbyMarket
OutputformatsentbyUTCtoeachSFTClearingMemberthathadtransactionsfortheprocessingday
whichcontainstheaggregatetotaltransactions,[[shares]],andamountforthatSFTClearingMember.Thisis
areconciliationmessageforSFTClearingMembers.
SFTClearing:InputandOutputMessageLayouts
MessageLayouts 7

---

## Page 8

UTCINPUTFILEFORMATS
ThefollowinginputfileformatsareavailablefortheSFTClearingservice:
l UTCInputFix/MQ Format
l UTCInputEODTotalsFIX/MQFormat
UTCInputFix/MQ  Format
Note
WhenbecominganApprovedTradeSubmitter,youmustindicatetoNSCCifyouwillbesubmittingSFTtransactionsaseither1)aVendor(independent
third-partythatisnotacounterpartytoanSFTtransaction)or2)acounterpartytotheSFTtransaction,whichisalsoadirectNSCCSFTMember.
IfyouareaVendor,yourSendingEntitymusthaverelationshipssetupinUTCfortheSFTmembersthatyoucansubmitfor.UTCvalidatestheSFT
transactioninputbycheckingyourSendingEntityIDintheUTCtabletoseeifitisaVendorsetupandwhetherthatVendorcansubmitforbothMembers
intheSFTClearingservice.InTag448(SubmittedbyIndicator),youmustalwayssettheValue=0.
IfyouareanNSCCSFTMember,yourSendingEntitymusthavearelationship(s)setupinUTCtotheirSFTMembertheyaresubmittingfor.InTag448
(SubmittedbyIndicator),youmustalwayssettheValue=1or2.Usethevalueof1ifyouaretheborrower/buyertotheSFTtransaction.Usethevalueof2
ifyouarethelender/sellertotheSFTtransaction.
ThefollowingtableprovidestheUTCinputfortheFIX/MQ format:
FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
Roll Send-
to-
Settle
CancelTerminate
HEADER Y=Required/N=Optional
8 BeginString 7 A/N Identifies the beginning of a new
messagegeneratedbyFIX.
Defaultvalue:FIX.4.4
Y Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 8

---

## Page 9

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
Roll Send-
to-
Settle
CancelTerminate
9 Body Length 4 N Messagelengthgeneratedby
FIX.
Note:NotrequiredforMQ.
Y Y Y Y Y Y Y Y
35 MessageType 2 A/N AE=TradeCaptureReport
ThedefaultvalueofAE is
required.
Y Y Y Y Y Y Y Y
49 SenderCompID 8 A/N Assignedvalueusedtoidentify
firmsendingthemessage.
TBDforeachSendingEntity.
Note:NotrequiredforMQ.
Y Y Y Y Y Y Y Y
115 SendingEntity 4 A/N Identifiesthesourcesubmittinga
tradeortransaction.Usedin
conjunctionwiththeSending
SubsystemandTradeSequence
Numbertouniquelyidentifythe
trademessage.Value
predeterminedbyNSCC.
Y Y Y Y Y Y Y Y
56 TargetCompID 4 A/N Assignedvalueusedtoidentify
thereceivingfirmmessage.
Defaultvalue:[[NSCC]]
Y Y Y Y Y Y Y Y
34 TradeSequence 9 N Uniquemessageidentifier
generatedbyFIX.
Note:NotrequiredforMQ.
Y Y Y Y Y Y Y Y
52 SendingTime 21 A/N TimestampgeneratedbyFIX.
Note:NotrequiredforMQ.
Y Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 9

---

## Page 10

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
Roll Send-
to-
Settle
CancelTerminate
50 SendingSubsystem 3 A/N UsedinconjunctionwithSending
EntityandTradeSequence
Numbertouniquelyidentifythe
trademessage.
N N N N N N N N
DETAIL(Y=Required/N=Optional)
571 TradeSequenceNumber8 A/N SequentialTradeMessage
IdentifiergeneratedbytheMarket.
Muststartat00000001and
increasesequentiallywith
subsequenttransactions.
Incombinationwithtags115and
50(optional),itprovidesunique
identificationtoeachtrade
message,whichwillbeusedby
UTCfordetectinggapsinthe
trademessagesequencenumber.   
Y Y Y Y Y Y Y Y
22 SecurityIDSource 1 A/N l 1=[[CUSIP]]
l 4=ISIN
Y Y N Y Y Y N N
48 SecurityID 12 A/N SecurityIdentifierassociatedwith
Tag22.
Y Y N Y Y Y N N
32 ShareQTY 11 N ShareQuantity,Maximumvalue
accepted999,999,999
Y Y N Y Y Y Y N
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 10

---

## Page 11

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
Roll Send-
to-
Settle
CancelTerminate
31 UnitPrice 13 A/N ContractPrice.
12Digits+1(periodindicatingsix
decimalpointoffset)
N N N N N N N N
30 MarketCode 3 A/N NumericCodetoidentify
submittingExchangeinUTC.
200=SFTMarket
Y Y Y Y Y Y Y Y
75 TradeDate 8 N YYYYMMDD=Format N N N N N N N N
60 TradeExecutionTime 9 A/N HHMMSSMSS
CurrentTimeReceivedbyUTC=
[[default]]
N N N N N N N N
526 DTCCReferenceID 14 A/N UniqueDTCCReferenceIDofan
On-legorOff-legtransaction.
N N Y N Y Y Y Y
11 BuyClientOrderID
Formoreinformation
aboutusingTag11,see
the5.8Additional
ReferenceIDsonSFT
SubmissiontoUTC
sectioninthe
[[SFT]] ClearingGeneral
ServiceGuide.
32 A/N Firstoccurrenceofthetag.
UniqueClientOrderIDofthe
[[Borrower]].
Note:Onlythefirst16bytesare
passeddownstreamontheISO
messagingoutput.
N N N N N N N N
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 11

---

## Page 12

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
Roll Send-
to-
Settle
CancelTerminate
11 SellClientOrderID
Formoreinformation
aboutusingTag11,see
the5.8Additional
ReferenceIDsonSFT
SubmissiontoUTC
sectioninthe
[[SFT]] ClearingGeneral
ServiceGuide.
32 A/N Secondoccurrenceofthetag.
UniqueClientOrderIDofthe
Lender.
Note:Onlythefirst16bytesare
passeddownstreamontheISO
messagingoutput.
N N N N N N N N
66 ExecutionID
Formoreinformation
aboutusingTag66,see
the5.8Additional
ReferenceIDsonSFT
SubmissiontoUTC
sectioninthe
[[SFT]] ClearingGeneral
ServiceGuide.
32 A/N VendororMarketplaceUnique
ReferenceID.
Space=[[default]]
N N N N N N N N
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 12

---

## Page 13

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
Roll Send-
to-
Settle
CancelTerminate
453 NoPartyID 1 N NumberofpartyIDstofollow. 
Mustbeatleastthree(BuySFT
ClearingMember,SellSFT
ClearingMember,andSubmitted
ByParticipantarerequired)and
uptoamaximumofsevencanbe
specified.
Thefollowingarerequired:
l BuySFTClearingMember
l SellSFTClearingMember
l SubmittedByParticipant
Y Y Y Y Y Y Y Y
448 BuySFTClearing
AccountNumber
8 A/N [[Buyer]]([[Borrower]])SFTClearing
AccountNumber
Y Y Y Y Y Y Y Y
452 PartyRole 2 N 04=SFTClearingMember Y Y Y Y Y Y Y Y
448 BuyEntering/Executing
[[Broker]]
8 A/N MarketMnemonic/MPID N N N N N N N N
452 PartyRole 2 N 01=ExecutingFirm N N N N N N N N
448 Buy Introducing Broker8 A/N BuyIntroducingBroker N N N N N N N N
452 PartyRole 2 N 06=IntroducingFirm N N N N N N N N
448 SellSFTAccount
Number
8 A/N [[Seller]](Lender)SFTAccount
Number
Y Y Y Y Y Y Y Y
452 PartyRole 2 N 18=ContraSFTClearing
[[Member]]
Y Y Y Y Y Y Y Y
448 SellEntering/Executing
[[Broker]]
8 A/N MarketMnemonic/MPID N N N N N N N N
452 PartyRole 2 N 37=ContraTrader N N N N N N N N
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 13

---

## Page 14

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
Roll Send-
to-
Settle
CancelTerminate
448 Sell Introducing Broker8 A/N SellIntroducingBroker N N N N N N N N
452 PartyRole 2 N 17=ContraFirm N N N N N N N N
448 SubmittedByIndicator
Note:Thevalueusedin
thistagdeterminesthe
valueusedinTag54for
anapprovedsubmitter
output).
IfTag448hasavalueof
0or2,Tag54hasavalue
of2onoutput
([[Seller]]/Lender).
IfTag448hasavalueof
1,Tag54hasaValueof
1onoutput
([[Buyer]]/[[Borrower]]).
1 A/N Valueofeither
l 0=byMarket
(Thisvalueisusedbyan
ApprovedTradeSubmitter
whoisnotacounterpartyto
theSFT,suchasaVendor).
l 1=byBuyerParticipant
(Thisvalueisusedifthe
ApprovedTradeSubmitteris
alsoacounterpartytotheSFT
intheroleoftheborrower).
l 2=bySellerParticipant
(Thisvalueisusedifthe
ApprovedTradeSubmitteris
alsoacounterpartytotheSFT
intheroleofthelender).
Y Y Y Y Y Y Y Y
452 PartyRole 2 N 36=EnteringTrader(which
representstheSubmitterofthe
messagethatgoeswithtag448-
SubmittedbyParticipant).
Y Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 14

---

## Page 15

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
Roll Send-
to-
Settle
CancelTerminate
81 SFTTransactionType
Code
1 A/N SFTTypeCode:
l A=Pre-establishedBilateral
Loan
l B=Buy-Side
l C=Cancel
l M=RateModification
l N=NewLoan
l R=Roll
l S=Send-to-Settle
l T=Terminate
Y Y Y Y Y Y Y Y
578 SourceofTransaction/
MarketSystem
2 A/N Codethatdenotesthesystemat
themarketonwhichtheexecution
occurred.
TobeassignedbyNSCCperuser
request.
Examples:
l S1–submittedbyamember
orbuy-sidetransaction
l S2–submittedbyvendor          
Y Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 15

---

## Page 16

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
Roll Send-
to-
Settle
CancelTerminate
825 Lending/InterestRate
Indicator
1 A/N Lending/InterestRateIndicator
informsNSCCofthecounterparty
totheloanwhoshouldbecredited
theovernightrebateintereston
theloantransaction:
l N=NoRate
l B=PaidtoBorrower
l L=PaidtoLender
l space=N/A
Y Y Y Y Y N N N
158 Lending/InterestRate 10 N RateforInterestAmount
calculation.
9Digits+1(periodindicatingfour
decimalpointoffset) 
Note
*=RequiredforTag825=BorL.
Y* Y* Y* Y* Y* N N N
159 IndependentAmount
Rate
10 N RateforIndependentAmount
calculation.
9Digits+1(periodindicatingfour
decimalpointoffset) 
N N N N N N N N
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 16

---

## Page 17

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
Roll Send-
to-
Settle
CancelTerminate
581 RoundingRuleCode 1 A/N IndicatesRoundingRuleforSettle
PriceCalculation:
l 0=norounding
l 1=uptonearest$0.01
l 2=uptonearest$0.05
l 3=uptonearest$0.10
l 4=uptonearest$0.25
l 5=uptonearest$1.00
Y Y N Y Y N N N
TRAILER(Y=Required/N=Optional)
10 CheckSum 3 A/N GeneratedbyFIX.
Tag10isrequiredonthelastfield
ofallmessagestomarktheendof
thetransaction.
Separategrouptransactionwith
tag10(CheckSum)ordelimiter
X'03'.
Y Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 17

---

## Page 18

UTCInputEODTotalsFIX/MQFormat
ThefollowingtableprovidestheUTCinputendofdaytotalsfortheFIX/MQformat:
FIX
Tag
Name LengthTypeDescription Y=Required/
N=Optional
HEADER FIX MQ
8 BeginString 7 A/N Identifies the beginningofanewmessagegeneratedbyFIX.
DefaultValue:FIX.4.4
Y Y
9 BodyLength 4 N MessagelengthgeneratedbyFIX. Y N
35 MessageType 2 A/N h=TradingSessionStatus Y Y
56 TargetCompID 4 A/N Assignedvalueusedtoidentifyreceivingfirmmessage.
Defaultvalue:[[NSCC]]
Y Y
34 TradeSequence 9 N UniquemessageidentifiergeneratedbyFIX. Y N
52 SendingTime 21 A/N TimestampgeneratedbyFIX. Y N
49 SenderCompID 8 A/N Assignedvalueusedtoidentifyfirmsendingmessage. Y N
115 SendingEntity 4 A/N Identifiesthesourcesubmittingatradeortransaction.
ValuepredeterminedbyNSCC.
Y Y
DETAIL FIX MQ
336 TradingSessionID 12 A/N MARKETTONSCC N N
340 TradingSessionStatus 1 A/N 3=Closed N N
58 ProcessDate 8 N UTCprocessdate. N N
387 Sending Entity Processing Total9 N NumberofStockLoanrecordssenttoUTCfromtheSendingEntity
duringtheday.
Y Y
TRAILER FIX MQ
10 CheckSum 3 A/N GeneratedbyFIX. Y Y
SFTClearing:InputandOutputMessageLayouts
UTCInputFileFormats 18

---

## Page 19

UTCOUTPUTFILEFORMATS
ThefollowingoutputfileformatsareavailablefortheSFTClearingservice:
l UTCOutputFIX/MQFormat
l UTCOutboundGapFillRequestFIX/MQFormat
l UTCOutboundBuy-SideCutoffFIX/MQFormat(3:00P.M.ET)
l UTCOutboundEODMessagestoParticipantsbyMarket
UTCOutputFIX/MQFormat
ThefollowingtableprovidestheUTCoutputlayoutfortheFIX/MQformat:
FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
HEADER Y=Required/N=Optional
8 BeginString 7 A/N Identifies the beginning
ofanewmessage
generatedbyFIX.
DefaultValue:FIX.4.4
Y Y Y Y Y Y Y Y
9 BodyLength 4 N Messagelength
generatedbyFIX.
Note:Notrequiredfor
MQ.
Y Y Y Y Y Y Y Y
35 MessageType 2 A/N AE=TradeCapture
Report
Y Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 19

---

## Page 20

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
49 SenderCompID 8 A/N Assignedvalueusedto
identifyfirmsending
message.
Defaultvalue:[[NSCC]]
Y Y Y Y Y Y Y Y
56 TargetCompID 4 A/N Assignedvalueusedto
identifyreceivingfirm
message.
TBDforeachrecipient
Y Y Y Y Y Y Y Y
34 TradeSequence9 N Uniquemessage
identifiergeneratedby
FIX.
Note:Notrequiredfor
MQ.
Y Y Y Y Y Y Y Y
52 SendingTime 21 A/N Timestampgenerated
byFIX.
Y Y Y Y Y Y Y Y
DETAIL(Y=Required/N=Optional)
571 TradeReportID 15 A/N TradeIdentifier
generatedbythe
market,combinationof
inputtags115,50
(optional),and571.
Y Y Y Y Y Y Y Y
22 SecurityIDSource1 A/N l 1=[[CUSIP]]
l 4=ISIN
Y Y N Y Y Y N N
48 SecurityID 12 A/N SecurityIdentifier
associatedwithTag22.
Y Y N Y Y Y N N
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 20

---

## Page 21

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
55 SecuritySymbol 15 A/N Symboloftraded
security.
Y Y N Y Y Y N N
460 SecurityType
(Product)
2 N l 3=Corporate
l 5=[[Equity]]
l 11=Municipal
l 12=Other
l 14=[[UIT]]
Y Y N Y Y Y N N
32 ShareQTY 11 N Sharequantity.
Maximumvalue
acceptedis999,999,999
Y Y N Y Y Y Y N
31 UnitPrice 13 A/N ContractPrice
12Digits+1(period
indicatingsixdecimal
pointoffset).
Yesterday'sMarket
ClosePrice=[[default]]
Y Y N Y Y N N N
30 MarketCode 3 A/N NumericCodetoidentify
submittingExchangein
UTC.
200=SFTMarket
Y Y Y Y Y Y Y Y
75 TradeDate 8 N YYYYMMDD=Format
CurrentDate=[[default]]
Y Y Y Y Y Y Y Y
60 TradeExecution
Time
9 A/N HHMMSSMSS
CurrentTime=[[default]]
N N N N N N N N
64 SettlementDate 8 N YYYYMMDD=FormatY Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 21

---

## Page 22

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
11 ClientOrderID 32 A/N UniqueClientOrderID
Note:
Onlythefirst16bytes
arepasseddownstream
onISOmessaging
output.
N N N N N N N N
526 DTCCReference
[[ID]]-referring
14 A/N UniqueDTCC
ReferenceIDofaloan.
Note:Notrequiredfor
MQ.
Y Y Y Y Y Y Y Y
526 DTCCReference
[[ID]]
14 A/N UniqueDTCC
ReferenceIDofanew
Off-legtransactionfor
theroll
N N N N Y N N N
66 ExecutionID 32 A/N MarketExecutionID N N N N N N N N
54 SideIndicator 1 A/N l 1=Buy/[[Borrower]]
l 2=Sell/Lender
Y Y Y Y Y Y Y Y
453 NoPartyIDs 1 N NumberofpartyIDsto
follow. Mustbeatleast
two(BuyandSellSFT
ClearingMembersare
required)anduptoa
maximumofninecanbe
specified.
Y Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 22

---

## Page 23

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
448 SFTClearing
MemberAccount
Number
8 A/N SFTClearingMember
AccountNumber
Y Y Y Y Y Y Y Y
452 PartyRole 2 N 04=SFTClearing
[[Member]]
Y Y Y Y Y Y Y Y
448 Entering/
ExecutingBroker
8 A/N MarketMnemonic/
MPID
N N N N N N N N
452 PartyRole 2 N 01=ExecutingFirm N N N N N N N N
448 IntroducingBroker8 A/N IntroducingBroker N N N N N N N N
452 PartyRole 2 N 06=IntroducingFirm N N N N N N N N
448 SettlingBroker 8 A/N NSCCParticipant
Number
Y Y Y Y Y Y Y Y
452 PartyRole 2 N 11=SettlingAccount Y Y Y Y Y Y Y Y
448 ContraSFT
ClearingMember
Account
8 A/N NSCCContraSFT
ClearingMember
Number
Y Y Y Y Y Y Y Y
452 PartyRole 2 N 18=ContraSFT
ClearingMember
Y Y Y Y Y Y Y Y
448 ContraEntering/
ExecutingBroker
8 A/N MarketMnemonic/
MPID
N N N N N N N N
452 PartyRole 2 N 37=ContraTrader N N N N N N N N
448 ContraIntroducing
[[Broker]]
8 A/N ContraIntroducing
[[Broker]]
N N N N N N N N
452 PartyRole 2 N 17=ContraFirm N N N N N N N N
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 23

---

## Page 24

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
448 ContraSettling
[[Broker]]
8 A/N NSCCParticipant
Number
Y Y Y Y Y Y Y Y
452 PartyRole 2 N 12=ContraSettling
Account
Y Y Y Y Y Y Y Y
448 SubmittedBy
Indicator
1 A/N l 0=byMarket
l 1=byBuyer
[[participant]]
l 2=bySeller
[[participant]]
Y Y Y Y Y Y Y Y
452 PartyRole 2 N 36=EnteringTrader Y Y Y Y Y Y Y Y
81 SFTTransaction
TypeCode
1 A/N SFTTypeCode:
l A=Pre-established
BilateralLoan
l B=Buy-Side
l C=Cancel
l M=Rate
Modification
l N=NewLoan
l R=Roll
l S=Send-to-Settle
l T=Terminate
Y Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 24

---

## Page 25

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
578 Sourceof
Transaction/
MarketSystem
2 A/N Codewhichdenotesthe
systematthemarketon
whichtheexecution
occurred.Examples:
l S1=submittedby
memberorbuy-side
transaction
l S2=submittedby
vendor               
Y Y Y Y Y Y Y Y
825 Lending/Interest
RateIndicator
1 A/N Lending/InterestRate
Indicator:
l N=NoRate
l B=PaidtoBorrower
l L=PaidtoLender
l space=N/A
Y Y Y Y Y N N N
381 Principal/Contract
LoanAmount
17 N UnitPricexShare
Quantity
16Digits+1(period
indicatingtwodecimal
pointoffset)
Y Y N Y Y N N N
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 25

---

## Page 26

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
581 RoundingRule
Code
1 A/N IndicatesRoundingRule
forSettlePrice
Calculation:
l 0=norounding
l 1=uptonearest
$0.01
l 2=uptonearest
$0.05
l 3=uptonearest
$0.10
l 4=uptonearest
$0.25
l 5=uptonearest
$1.00
Y Y N Y Y N N N
6 SettlementPrice 13 A/N SettlePrice
12Digits+1(period
indicatingtwodecimal
pointoffset).
[Unitprice*(1+IArate)]
roundedasdirectedby
RoundingRuleCodein
Tag581.
Y Y N Y Y N N N
118 [[settlement]]
Amount
17 N PrincipalAmount+
IndependentAmount
16Digits+1(period
indicatingtwodecimal
pointoffset)
Y Y N Y Y N N N
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 26

---

## Page 27

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
158 Lending/Interest
Rate
10 N RateforInterestAmount
calculation.
9Digits+1(period
indicatingfourdecimal
pointoffset) 
*RequiredforTag
825=BorL.
Y* Y* Y* Y Y* N N N
159 Independent
AmountRate
10 N RateforIndependent
Amountcalculation.
9Digits+1(period
indicatingfourdecimal
pointoffset) 
N N N N N N N N
920 RebateInterest
Amount
17 N InterestAmountpaid
overnight,calculatedas
(LendingRate/100*Net
settlementAmt*#days/
360).16Digits+1
(periodindicatingtwo
decimalpointoffset).
Thiscalculationisonly
populatedonoutputifa
valueofB=Buy-sideis
populatedinTag71;
otherwise,thetagis
populatedwith0.00.
N N N Y*
off-leg
only
N N N N
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 27

---

## Page 28

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
751 NSCCReject
Code
2 N l 00=AcceptedTrade
l 01=Invalid
ParticipantInfo
l 02=InvalidTrade
Date
l 03=InvalidSecurity
l 04=InvalidQuantity
l 05=InvalidPrice
l 06=InvalidTrade
Source
l 07=InvalidMarket
l 09=Invalid
Relationship
l 11=DuplicateTrade
l 12=InvalidMessage
Type
l 13=InvalidTrade
Type
l 14=InvalidSending
Entity
l 15=InvalidTrade
SequenceNumber
l 16=Invalid
Submitted-by
Indicator
l 21=Invalid
SettlementDate
Y Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 28

---

## Page 29

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
l 23=InvalidTrade
Amount
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 29

---

## Page 30

FIX
Tag
Name LengthTypeDescription New
Loan
Pre-
established
Bilateral
Loan
Rate
Modification
Buy-
Side
RollSend-
to-
Settle
CancelTerminate
751 NSCCReject
Code
(Continued)
2 N l 54=MissedCutoff
l 55=InvalidRate
l 56=InvalidLoan
Status
l 57=InvalidDTCC
referenceID
l 58=Invalid
TransactionType
l 59=Invalid
RoundingRule
Indicator
l 60=Security
Undergoing
CorporateAction
l 61=Loanis
ineligibleforthe
requestduetoa
recallaction
Y Y Y Y Y Y Y Y
TRAILER(Y=Required/N=Optional)
10 CheckSum 3 A/N GeneratedbyFIX. Y Y Y Y Y Y Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 30

---

## Page 31

UTCOutboundGapFillRequestFIX/MQFormat
ThefollowingtableprovidestheUTCoutboundgapfillrequestfortheFIX/MQformat:
FIX
Tag
Name LengthTypeDescription Y=Required/
N=Optional
HEADER FIX MQ
8 BeginString 7 A/N Identifies the beginningofanewmessagegeneratedbyFIX.
Defaultvalue:FIX.4.4
Y Y
9 BodyLength 4 N MessagelengthgeneratedbyFIX. Y N
35 MessageType2 A/N AD=TradeCaptureReportRequest Y Y
49 SenderComp
[[ID]]
4 A/N Assignedvalueusedtoidentifyfirmsendingmessage.
Defaultvalue=[[NSCC]]
Y N
56 TargetComp
[[ID]]
8 A/N Assignedvalueusedtoidentifyreceivingfirmmessage.
TBDforeachSendingEntity.
Note:NotrequiredforMQ.
Y N
115 SendingEntity4 A/N IdentifiesthesubmittingsourceforwhichatrademessagegapwasdetectedbyUTC. Y Y
34 Trade
Sequence
9 N UniquemessageidentifiergeneratedbyFIX.
Note:NotrequiredforMQ.
Y N
DETAIL FIX MQ
50 Sending
Subsystem
3 A SendingsubsystemforwhichatrademessagegapwasdetectedbyUTC.Usedinconjunction
withSendingEntityandTradeSequenceNumberforuniqueidentificationoftrademessage.
ThistagissentonlyifitisprovidedoninputbythemarketontheUTCCommonTradeInput
formatforthissendingentity.
Y Y
52 SendingTime 21 A/N TimestampgeneratedbyFIX. Y N
568 TradeRequest
[[ID]]
14 A/N Value:GapFillRequest’ Y Y
569 Traderequest
Type
1 N 3=UnreportedTrades Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 31

---

## Page 32

FIX
Tag
Name LengthTypeDescription Y=Required/
N=Optional
571 Beginning
Sequence
Number
8 A/N BeginningSequenceNumberoftheGap Y Y
818 Ending
Sequence
Number
8 A/N EndingSequenceNumberoftheGap Y Y
TRAILER FIX MQ
10 CheckSum 3 A/N GeneratedbyFIX.
NotrequiredthroughtheMQInterface.
Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 32

---

## Page 33

UTCOutboundEODConfirmationtoMarketFix/MQ  Format
ThefollowingtableprovidestheUTCoutboundendofdayconfirmationtomarketfortheFIX/MQ format:
FIX
Tag
Name LengthTypeDescription Y=Required/
N=Optional
HEADER
8 BeginString 7 A/N Identifies the beginningofanewmessagegeneratedbyFIX.
DefaultValue:FIX.4.4
Y
9 BodyLength 4 N MessagelengthgeneratedbyFIX. Y
35 MessageType 2 A/N h=TradingSessionStatus Y
56 TargetCompID 8 A/N Assignedvalueusedtoidentifyreceivingfirmmessage.
Defaultvalue:[[NSCC]]
Y
115 SendingEntity 4 A/N AssignedvalueusedtoidentifythesendingentityfromwhichNSCChad
receivedtradedataduringtheday.
ValuepredeterminedbyNSCC.
Y
97 PossResend 1 A/N Indicatesthatthemessagemaycontaininformationthathasbeensentunder
anothersequencenumber.
l N=OrigTrans
l Y=PossResend
Y
34 Message Identifier
(MsgSeqNum)
9 N UniquemessageidentifiergeneratedbyFIX.
MaynotarriveinsequencenumberorderwhentransmittedoverMQ.
Y
52 SendingTime 21 A/N TimestampgeneratedbyFIX. Y
49 SenderCompID 4 A/N Assignedvalueusedtoidentifyfirmsendingmessage.
Possiblevalue=[[NSCC]].
Y
DETAIL
336 TradingSessionID 12 A/N NSCCTOMARKET Y
340 TradingSessionStatus 1 A/N 3=Closed Y
58 ProcessDate 8 N UTCprocessdate. Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 33

---

## Page 34

FIX
Tag
Name LengthTypeDescription Y=Required/
N=Optional
20001BalanceIndicator 1 A/N l Y=Inbalance
l N=Outofbalance
Y
20002NSCCProcessingTotal 9 N SFTrecordscounterforthesendingentity,includingvalidandrejected
transactionsprocessedbyNSCC.
Y
387 Sending Entity Processing Total8 N NumberofStockLoanrecordssenttoUTCfromtheSendingEntityduringthe
dayandreportedinthesendingentityintheGoodNightmessage.
Y
TRAILER
10 CheckSum 3 A/N FIXtag10isprovidedonallendofdaymessages. Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 34

---

## Page 35

UTCOutboundBuy-SideCutoffFIX/MQFormat(3:00P.M.ET)
ThefollowingtableprovidestheUTCoutboundbuy-sidecutofffortheFIX/MQformat(3:00P.M.EasternTime):
FIXTag Name Length Type Description Y=Required/N=Optional
HEADER FIX MQ
8 BeginString 7 A/N Identifies the beginningofanewmessage
generatedbyFIX.
Defaultvalue:FIX.4.4
Y Y
9 BodyLength 4 N MessagelengthgeneratedbyFIX. Y N
35 MessageType 2 A/N B=News Y Y
49 SenderCompID 4 A/N Assignedvalueusedtoidentifyfirm
sendingmessage.
Defaultvalue=[[NSCC]]
Y N
56 TargetCompID 8 A/N ReceivingSponsorMemberID
Example00000111
Y Y
34 TradeSequence 9 N Uniquemessageidentifiergeneratedby
FIX.
Note:NotrequiredforMQ.
Y N
52 SendingTime 21 A/N TimestampgeneratedbyFIX.
Note:NotrequiredforMQ.
Y N
Detail FIX MQ
148 Headline 8 A/N CurrentdateinYYYYMMDDformat Y Y
33 Nolinesoftext. 1 N Value1 Y Y
58 Text 47 A/N Bodyofthemessage:
Releasematuringbuy-sideoff-legsfrom
[[Margin]].
Y Y
TRAILER FIX MQ
10 CheckSum 3 A/N GeneratedbyFIX. Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 35

---

## Page 36

UTCOutboundEODMessagestoParticipantsbyMarket
ThefollowingtableprovidestheUTCoutboundendofdaymessagestoparticipantsbymarket:
FIXTag Name Length Type Description Y=Required/N=Optional
HEADER FIX MQ
8 BeginString 7 A/N Identifies the beginningofanewmessage
generatedbyFIX.
Defaultvalue:FIX.4.4
Y Y
9 BodyLength 4 N MessagelengthgeneratedbyFIX. Y N
35 MessageType 2 A/N h=TradingSessionStatus Y Y
49 SenderCompID 4 A/N Assignedvalueusedtoidentifyfirmsending
message.
Defaultvalue=[[NSCC]]
Y N
56 TargetCompID 8 A/N ReceivingSFTClearingMemberAccount
Number.
Example:00000111
Y Y
34 TradeSequence 9 N UniquemessageidentifiergeneratedbyFIX.
Note:NotrequiredforMQ.
Y N
52 SendingTime 21 A/N TimestampgeneratedbyFIX.
Note:NotrequiredforMQ.
Y N
DETAIL FIX MQ
336 TradingSessionID 12 A/N NSCCTOPARTIC Y Y
340 TradeSessionStatus 1 A/N 5=PreClose Y Y
58 ProcessDate 8 A/N ProcessDateYYYYMMDD Y Y
20003 RegionName 5 A/N Example:USA Y Y
20004 Market 5 A/N UTCmarketcode.
Example:200
Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 36

---

## Page 37

FIXTag Name Length Type Description Y=Required/N=Optional
387 ProcessingTotalforaMarket 9 N TotalnumberoftradesprocessedbyUTCfor
theparticipant,includingvalidandrejected
trades
Y Y
20005 NumberofRepeatingGroupTags 2 N NumberofCurrencyTotals1 Y Y
20006 CurrencyCode 3 A/N Example:USD Y Y
20007 ValidTradeTotal 9 N NumberofvalidtradesprocessedbyUTCfor
theparticipantandcurrency.
Y Y
20008 ValidShareQuantityTotal 13 N TotalShareQuantityinvalidtrades
processedbyUTCfortheparticipantand
currency.
Y Y
20009 ValidContractAmountTotal 16 N TotalContractAmountinvalidtrades
processedbyUTCfortheparticipantand
currency.
Y Y
TRAILER FIX MQ
10 CheckSum 3 A/N GeneratedbyFIX. Y Y
SFTClearing:InputandOutputMessageLayouts
UTCOutputFileFormats 37

---

## Page 38

UTCREJECTCODES
ThefollowingtableprovidestheUTCrejectcodes:
CodeandDescription PossibleCause
00=AcceptedTrade TransactionpassedallvalidationsandacceptedforDTCCprocessing.
01=InvalidParticipantInfo l OneorbothSFTparticipantswerenotsubmitted.
l OneorbothsubmittedSFTparticipantsarenotvalidfortheSFTClearingtransaction.
02=InvalidTradeDate l SubmittedTradedate(FIXTag75)isnotcurrentprocessdate.
l SFTsubmittedonaBankholiday.
03=InvalidSecurity l Security(FIXTag48)wasnotsubmittedtheSFTClearingtransaction.
l SubmittedsecurityisnotanequityoranequitythatiseligibleforSFTClearingprocessing.
l Submittedsecurityhasaninvalidtradingstatus,inactive,ornotfoundinDTCCSecurityMastertables.
l SecurityisineligibleforCNSorhasaDTCDeliverOrder([[DO]])chill.
l SubmittedsecurityforaRollSFTTransaction(R)orSend-to-SettleSFTtransaction(S)doesnotmatchthe
securityoftheoutstandingoff-legreturn.
04=InvalidQuantity l [[shares]](FIXTag32)werenotsubmittedfortheSFTtransactiontype.
l SharessubmittedfortheSFTtransactiontypeexceedsthresholdof999,999,999.
l SharessubmittedfortheSFTRolltransaction(R)isnotequalorlessthanthesharesoftheoutstandingoff-leg
return.
l SharessubmittedfortheSFTCanceltransaction(C)whichistocancelaDOoff-legreturnisnotequaltothe
samesharesofthepreviouslysubmittedSFTSend-to-Settletransaction(S).
l SharessubmittedfortheSFTCanceltransaction(C)whichistocancelanon-legisnotequaltothesame
sharesoftheprevioussubmittedon-leg.
l SharessubmittedfortheSFTSend-to-Settletransaction(S)whichisforanoutstandingoff-legreturnwitha
settlementdateofthenextbusinessdateisnotequalorlessthanthesharesoftheoutstandingoff-legreturn.
l SharessubmittedfortheSFTSend-to-Settletransaction(S)whichisforanoutstandingoff-legreturnwitha
settlementdateofthecurrentbusinessdateisnotequaltothesamesharesoftheoutstandingoff-legreturn.
SFTClearing:InputandOutputMessageLayouts
UTCRejectCodes 38

---

## Page 39

CodeandDescription PossibleCause
05=InvalidPrice l Price(FIXTag31)submittedfortheSFTtransactionislessthantheminimumpriceallowed($5.00).
l MarketclosingpriceforthesubmittedSFTtransactionislessthantheminimumallowed($5.00).
06=InvalidTradeSource SourceoftheTransaction/MarketSystem(FIXTag578)wasnotsubmittedorinvalid.
07=InvalidMarket l MarketCode(FIXTag30)isnotsubmitted.
l SubmittedMarketCodeisnotdefinedinUTC. 
l SubmittedMarketCodeisnoteligibleforSFTClearing.
08=MultipleRejects NotapplicableforSFTClearing.
09=InvalidRelationship ForBuy-sidesubmittedSFTtransactiontype(B),theSponsor-sponsoredrelationshipisnotvalid.
11=DuplicateTrade NotapplicableforSFTClearing.Willbebypassed,andnotreportedbacktothesender.
12=InvalidMessageType NotapplicableforSFTClearing.
13=InvalidTradeType NotapplicableforSFTClearing.
14=InvalidSendingEntity l SendingEntityisnotdefinedinUTC.
l SendingEntity/Market/MarketSource/SubmittingParticipantrelationshipisnotdefinedinUTCdatabase.
15 = Invalid TradeSequence
Number
SequenceNumber(FIXTag571)wasnotsubmittedornotnumeric.
16=InvalidSubmitted-byIndicator l Submitted-byIndicator(FIXTag448)wasnotsubmitted.
l Submittedsubmitted-byindicatorisnot0,1,or2.
l Submitted-byIndicatoris0forParticipanttypeofSendingEntity.
21=InvalidSettlementDate SettlementdateisnotequaltocurrentsettlementdateforsubmittedSFTtransaction
23=InvalidTradeAmount CalculatedSettlementAmountforsubmittedSFTtransactionexceedsthreshold9,999,999,999.99.
25=InvalidCurrencyCode NotapplicableforSFT.
27=Other NotapplicableforSFT.
54=MissedCutoff                    SubmittedSFTtransactionreceivedaftercutoff.
SFTClearing:InputandOutputMessageLayouts
UTCRejectCodes 39

---

## Page 40

CodeandDescription PossibleCause
55=InvalidRate   l LendingRateIndicator(FIXTag825)wasnotsubmittedorinvalidforsubmittedSFTtransaction.
l LendingRate(FIXTag158)wasnotsubmittedornotnumericforSFTtransactionandsubmittedLendingRate
IndicatorhasvalueofBorL.
l LendingRate(FIXTag158)wassubmittedandgreaterthanzeroforSFTtransactionandsubmittedLending
RateIndicatorhasvalueofN.
l BothsubmittedLendingRateandLendingRateIndicatorinRateModificationSFT(M)matchtherateandthe
indicatorintheoriginalloan.
l SubmittedIndependentAmountRateforaRollSFT(R)doesnotmatchtherateintheoriginalloan.
l IArate(FixTag159)thatwassubmittedwasinvalidornotnumericforSFTtransaction.
56=Invalidloanstatus Off-legreturninSASdatabasehasinvalidstatusforsubmittedSFTtransaction. 
57 = Invalid [[DTCC]] Reference IDl DTCCLoanReferenceID(FIXTag526)wasnotsubmittedfortheSFTtransaction.
l SubmittedDTCCLoanReferenceID(FIXTag526)wasnotsubmittedforaSFTisnotfoundintheSAS
database.
58=InvalidTransactionType SFTType(FIXTag81)wasnotsubmittedorinvalid
59 = Invalid Rounding Rule IndicatorRoundingRuleIndicator(FIXTag581)wasnotsubmittedorinvalidforNewloanorRollSFT(A,N,orR).
60 = Security UndergoingCorporate
Action
SecuritysubmittedforNewLoanSFTtransactiontype(NorA)orRollSFTtransactiontype(R)isundergoinga
corporateaction.
61=DTCCReferenceIDhasa
Recall
SubmittedRollSFTtransaction(R)forDTCCReferenceIDhasarecall.
SFTClearing:InputandOutputMessageLayouts
UTCRejectCodes 40

---

## Page 41

ISOMESSAGEQUEUE(MQ)MESSAGEFORMATS
TheSASsystemusesthefollowingoutputmessagetypes:
l MT548MessageFormat
MT548isastatusUPDATEmessage.TheMT548ISOmessageisgeneratedbytheSASsystem,whichkeepstrackofoutstandingSFTs.Thismessage
isonlygeneratedafteranewSFTisreceivedandacceptedbytheUTCsystemandforwardedtoSASforprocessing.TheSASsystemusesthis
messagetoupdatemessagesubscribers,suchassubmittingentitiesandcounterpartiestotheSFT,aboutchangestothestatusoftheirSFT.These
updatescanincludeevents,suchaspendingandterminated.
l MT547/MT545(InclusiveofRateModification)MessageFormat
MT545andMT547arebothMADEmessages.TheMT547MADEmessageisonlyfortheDELIVERER,andtheMT545MADEmessageisforthe
RECEIVER.TheMT547/545messagesaregeneratedfromtheSASsystem,whichusesthemtocommunicatewithmessagesubscriberswhenMADEs
aredone.TheMT545/547messagesarealsousedfortheratemodificationpurpose.TheCommonDataTransferServices(CDTS)Productis
CNSESFTO.
l MT548:RecallandBuy-InExecutionOutputMessageFormats
MT548isprovidedtotheApprovedSFTSubmitter,MemberstotheSFT,orboth.Itincludesoutputonarecall,cancelrecall,buy-inexecution,and
cancelbuy-inexecution.ItisalsousedforupdatestooutstandingrecallsagainstanSFTthatwasupdatedresultingfromaSend-toSettleorCorporate
Actionbeingprocessed.TheoutputisMT548andtheCDTSProductisCNSISOO.
TheSASsystemalsousetheMT542:RecallandBuy-InInputMessageFormatsinputmessagetype.MT542istheinputISOformatforrecallandbuy-
intransactions.ItisusedbytheApprovedSFTSubmittertoinputarecall,cancelrecall,buy-inexecution,orcancelbuy-inexecutionmessage.TheCDTS
ProductisCNSISOI.
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 41

---

## Page 42

ThefollowingtableprovidesanoverviewforSASISOmessages:
FieldName Description/Values MT548MT547/545RateMod.
(MT547/545)
Process/MessageTimestampApplicationprocesstimestamp
Format:ccyymmddhhmmss
X X X
DTCCReferenceID LoanreferenceIDassignedbyUTCwhennew,Pre-establishedBilateralLoan,
buy-side,orrollloantransactionisreceived.Willbepopulatedwithpreviously
assignedIDforratemodification,send-to-settleandterminationmessage.
Format:YYMMDDofcurrentdate+eightdigitsequencenumber.
X X X
ClientOrderID ClientAssignedNumberonBuyorSellside X X X
ExecutionID ClientAssigned(Vendor)BuyorSellExecutionID X X X
SFTTradeDate Shouldalwaysbethecurrentdate. X X X
SFTSettlementDate NextDaySettlementforoff-legtransactions,currentdateforothers. X X X
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 42

---

## Page 43

FieldName Description/Values MT548MT547/545RateMod.
(MT547/545)
SFTTransaction Type CodeValues:
l NEWS-Pre-establishedBilateralLoan
l NEWL-NewLoan
l RMOD-RateModification
(applicableonlyforMT547/545)
l ROLL-Roll
l SNDS-Send-to-Settle
l TERN-NSCCTermination
(applicableonlyforMT547/545)
l TERC-LoanTermination
(applicableonlyforMT547/545)
l NROL-NoRoll
l CANC-CanceledbyClient
l PDIF-PriceDifferential
(NSCCInitiated)
l NRCA-NoRoll&CorporateAction
(applicableonlyincombinationwithspecificcorporateaction)
l BEXE-Buy-InExecution
(applicableonlyforMT547/545)
l BKRO-BrokerRe-Org
X X X
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 43

---

## Page 44

FieldName Description/Values MT548MT547/545RateMod.
(MT547/545)
SFTStatusCode Values:
l PEND-Pending(inSASpendingoff-letreturn)
l DROP-Dropped
l CANC-Canceled
l NRET-NonReturnFail
l TERN-TerminatedbyNSCC
l TERC-TerminatedbyClient
l RJCT-Rejected
l MADE-On-legSettled
X Not
Applicable
sinceitis
onlyfor
MADE.
Not
Applicable
sinceitisonly
forMADE.
LegIndicator Values:
l ONLG-On-leg
l OFFL-Off-leg
l OTHR–Othervalue
X X X
SecurityISINID SecurityIDinaISINformat. NospotX Nospot
SecurityCUSIPID SecurityIDinaCUSIPformat. X X X
BuyParticipantSettlementID NSCCidentifieroftheOriginalBuyparticipant.                                                       X X X
BuyParticipantSFTID NSCCidentifieroftheOriginalBuyparticipant-SFTaccount. X X X
Sell [[participant]] [[settlement]] IDNSCCidentifieroftheOriginalSellparticipant.                                                       X X X
SellParticipantSFTID NSCCidentifieroftheOriginalSellparticipant-SFTaccount. X X X
NumberofShares Quantityofsharesbeingtraded. X X N/A
SharePrice Pricepershareofthetransaction. NospotX Nospot
LendingRateIndicator Values:
l NRTE-NoRate
l LEND-PaidtoLenderofsecurity
l BRRW-PaidtoBorrowerofsecurity
X X X
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 44

---

## Page 45

FieldName Description/Values MT548MT547/545RateMod.
(MT547/545)
LendingRate Interest/LendingRateinpercent (%) NospotX Repurpose
theNumber
ofShares
field.
AMOR
qualifier.
IndependentAmountRate RatetocalculateIndependentAmountforthetransactioninpercent(%). No spotX Nospot
ContractAmountinUSD CalculatedasPricexShares X X N/A
Lending/InterestAmount Lending/InterestAmount NospotX Repurpose
theContract
Amountfield
RebateInterestAmount OvernightRebateInterest NospotX Nospot
SettlementAmount Calculatedas
ContractAmount +IndependentAmount
X X X
SFTActivityType Value:
STKL-StockLoan
X X X
RoundingValue Values:
l NRND-NoRounding
l RND1-Roundedtonearest$0.01
l RND2-Roundedtonearest$0.05
l RND3-Roundedtonearest$0.10
l RND4-Roundedtothenearest$0.25
l RND5-Roundedtothenearest$1.00
X X X
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 45

---

## Page 46

FieldName Description/Values MT548MT547/545RateMod.
(MT547/545)
CorporateActionsIndicator Values:
l CPAN-NotUndergoingaCorporateAction
l CAUN-UndergoingaNon-supportedCorporateAction
l FSSP-ForwardStockSplit
l RSSP-ReverseStockSplit
l CHMR-CashMerger
l STMR-StockMerger
l CSMR-CashandStockMerger
l NMCG-NameChange
X X N/A
Free-FormTextCommentsReservedforfutureuse. X X X
RateModificationIndicator Values:
l UIND-InterestwasUpdated(refertotheLending/InterestAmountfield).
l PRTY-PartieswereUpdated(refertotheLendingRateIndicatorfield).
l BOTH-Interest&PartiesUpdated(refertoboththeLending/InterestAmount
andLendingRateIndicatorfields).
N/A X X
SendingEntityID NSCCidentifieroftheSendingEntity(Vendor). X X X
RecallCounter Numberofrecallsassociated. X X N/A
RecallTotalQuantity Totalquantityoftheassociatedrecalls. X X N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 46

---

## Page 47

MT548MessageFormat
ThefollowingtableshowstheSFTClearingMT548messageformat:
MT548 Description/Values Lengthof
DataField
Input Tag Number
(if applicable)
:16R:GENL N/A
:20C::SEME//xxxxxxxxxxxxxxxxDTCCgenerated.Usedtotracktransactionfromsubmissiontofinalstate. Char16 N/A
:23G:INST N/A
:98C::PREP//ccyymmddhhmmssApplicationprocesstimestamp Char14 N/A
:16R:LINK N/A
:20C::RELA//xxxxxxxxxxxxxx DTCCReferenceDassignedbyUTCwhennew,newalreadysettled,buy-
side,orrollloantransactionisreceived.
Format:YYMMDDofcurrentdate+eight-digitsequencenumber.
Char14 Tag526
:16S:LINK N/A
:16R:LINK N/A
:20C::TRRF//xxxxxxxxxxxxxx l ClientOrderIDassignedbytheBuyerorSeller.
l Onlythefirst16outof32bytesaredisplayed.
l Ifgreaterthan16bytes,thewholeIDdisplaysinthe70ESPROfield.
Char16 Tag11
:16S:LINK N/A
:16R:LINK N/A
:20C::COMM//xxxxxxxxxxxxxx l Execution(Vendor)IDassignedbytheBuyerorSeller.
l Onlythefirst16outof32bytesaredisplayed.
l Ifgreaterthan16bytes,thewholeIDdisplaysinthe70ESPROfield.
Char16 Tag66
:16S:LINK N/A
:16R:STAT N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 47

---

## Page 48

MT548 Description/Values Lengthof
DataField
Input Tag Number
(if applicable)
:25D:SETT/DTCY/xxxx SFTstatuscode.
Values:
l PEND–Pending(processedbyCNS)
l DROP–Dropped
l CANC–Canceled
l NRET–Non-returnFail
l RJCT–Rejected
l MADE–On-legSettled
l TERC–TerminatedbyClient
l TERN–TerminatedbyNSCC
Char4 N/A
:16S:STAT N/A
:16S:GENL N/A
:16R:SETTRAN N/A
:35B:/US/XXXXXXXXX [[CUSIP]] Char 9 l Tag 48
(ifTag22=4)
l N/A
(ifTag22=1)
l :36B::SETT//UNIT/00000000000,0
-or-
l :36B::SETT//AMOR/00000,0000
l Quantityofsharesbeingtraded.
-or-
l Sharequantityorlendingrate.TheAMOR qualifierisusedonlywhenthe
TransactionType=RMOD.
9(11)
-or-
If AMOR, use
PIC9(5).9(4)
Tag32
(ShareQuantity)
-or-
Tag158
(LendingRate)
:36B::SETT//FAMT/00000000000,0RecallTotalQuantity 9(11)
:19A::OCMT//USD000000000000,00Contractamount,whichiscalculatedasPricexShares(UNIT).
-or-
Interestamount(AMOR).
9(12).9(2) N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 48

---

## Page 49

MT548 Description/Values Lengthof
DataField
Input Tag Number
(if applicable)
:19A::SETT//USD000000000000,00SettlementAmount
CalculatedasContractAmount +IndependentAmount
9(12).9(2) N/A
:97A::SAFE//xxxxxxx SellerforOn-legandBuyerforOff-leg
Identifiesaccountwherefinancialinstrumentsaremaintained.
(On-leg=Lender,Off-leg=[[Borrower]])
Char8 N/A
:22F::SETR/DTCYREAS/xxxxLegindicator.
Values:
l ONLG–On-leg
l OFFL–Off-leg
l OTHR–Othervalue
Char4 N/A
:22H::REDE//xxxx Values:
l DELI–UsedifyouarethedelivererofsharesatDTC.
l RECE–UsedifyouarethereceiverofsharesatDTC.
Char4 N/A
:22H::PAYM//xxxx Values:
l APMT–Forvaluedtransactions.
l FREE–Forfreetransactions.
Char4 N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 49

---

## Page 50

MT548 Description/Values Lengthof
DataField
Input Tag Number
(if applicable)
:22F::STCO/DTCYTXNT/xxxxTransactiontype.
Values:
l BKRO-BrokerRe-Org
l CANC–CanceledbyClient
l NEWS–Pre-establishedBilateralLoan
l NEWL–NewLoan
l NRCA-NoRoll&CorporateAction
l NROL–NoRoll
l PDIF–PriceDifferential
l ROLL–Roll
l RMOD–RateModification
l SNDS–Send-to-Settle
Char4 Tag81
(whereapplicable)
:22F::STCO/DTCYACTV/xxxxActivitytype.
Value:
STKL-StockLoan
Char4 N/A
:22F::STCO/DTCYDGCA/xxxxValues:
l CPAN–NotUndergoingaCorporateAction
l CAUN-UndergoingaNon-supportedCorporateAction
l FSSP-ForwardStockSplit
l RSSP-ReverseStockSplit
l CHMR-CashMerger
l STMR-StockMerger
l CSMR-CashandStockMerger
l NMCG-NameChange
Char4 N/A
:22F::BLOC/DTCY/xxxx RecallCounter Char4
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 50

---

## Page 51

MT548 Description/Values Lengthof
DataField
Input Tag Number
(if applicable)
:22F::SETS/DTCY/xxxx Interest/LendingRateindicator.
Values:
l NRTE–NoRate
l LEND–PaidtotheLenderofthesecurity
l BRRW–PaidtotheBorrowerofthesecurity
Char4 Tag825
:22F::COLA/DTCY/xxxx RoundingValues:
l NRND–NoRounding
l RND1–Roundedtonearest$0.01
l RND2–Roundedtonearest$0.05
l RND3–Roundedtonearest$0.10
l RND4–Roundedtothenearest$0.25
l RND5-Roundedtothenearest$1.00
Char4 Tag581
:98A::SETT//ccyymmdd SFTsettlementdate.
NextDaySettlementforoff-legtransactions,currentdateforothers.
Char8 N/A
:98A::TRAD//ccyymmdd SFTtradedate.
Shouldalwaysbethecurrentdate.
Char8 Tag75
:70E::SPRO//xxxxxxxxxxxxxxxxetc.Reservedforfutureuse. Char 35*10N/A
:16R:SETPRTY N/A
:95Q::BUYR//xxxxxxxx NSCCidentifieroftheOriginalBuyparticipant–Settlementaccount.For
example,iftheon-leg-borroweristhebuyer,thelenderistheseller;Ifthe
off-leg-lenderisthebuyer,theborroweristheseller.
Char8 Tag448
(with Tag 452 = 04)
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95R::DEAG/DTCYPART/xxxxxxxxNSCCidentifieroftheOriginalBuyparticipant–SFTaccount. Forexample,
iftheon-leg-borroweristhebuyer,thelenderistheseller.Iftheoff-leg-
lenderisthebuyer,theborroweristheseller.
Char8 N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 51

---

## Page 52

MT548 Description/Values Lengthof
DataField
Input Tag Number
(if applicable)
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95Q::DEI1//xxxx NSCCidentifieroftheSendingEntity(vendor). Char4 Tag115
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95Q::SELL//xxxxxxxx NSCCidentifieroftheOriginalSellparticipant–Settlementaccount.For
example,iftheon-leg-borroweristhebuyer,thelenderistheseller;Ifthe
off-leg-lenderisthebuyer,theborroweristheseller.
Char8 Tag448
(withTag 452 =04)
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95R::REAG/DTCYPART/xxxxxxxxNSCCidentifieroftheOriginalSellparticipant–SFTaccount.Forexample,
iftheon-leg-borroweristhebuyer,thelenderistheseller;Iftheoff-leg-
lenderisthebuyer,theborroweristheseller.
Char8 N/A
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95P::PSET//DTCYUS33 PlaceofSettlement Char8 N/A
:16S:SETPRTY N/A
:16S:SETTRAN N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 52

---

## Page 53

MT547/MT545(InclusiveofRateModification)MessageFormat
ThefollowingtableshowsthemessageformatforMT547/545,inclusiveoftheratemodification:
MT547/MT545 Description/Values Lengthof
DataField
InputTagNumber
(ifapplicable)
:16R:GENL N/A
:20C::SEME//xxxxxxxxxxxxxxxxDTCCgenerated.Usedtotracktransactionfromsubmissiontofinalstate.Char 16 N/A
:23G:NEWM N/A
:98C::PREP//ccyymmddhhmmssApplicationprocesstimestamp. Char14 N/A
:16R:LINK N/A
:20C::RELA//xxxxxxxxxxxxxx DTCCReferenceIDassignedbyUTCforthetransactionthatisMADE.
Format:YYMMDDofcurrentdate+eight-digitsequencenumber.
Char14 Tag526
:16S:LINK N/A
:16R:LINK N/A
:20C::TRRF//xxxxxxxxxxxxxx l ClientOrderIDassignedbytheBuyerorSeller.
l Onlythefirst16outof32bytesaredisplayed.
l Ifgreaterthan16bytes,thewholeIDisdisplayed
l inthe70ESPROfield.
Char16 Tag11
:16S:LINK N/A
:16R:LINK N/A
:20C::COMM//xxxxxxxxxxxxxx l Execution(Vendor)IDassignedbytheBuyerorSeller.
l Onlythefirst16outof32bytesaredisplayed.
l Ifgreaterthan16bytes,thewholeIDdisplaysinthe70ESPROfield.
Char16 Tag66
:16S:LINK N/A
:16S:GENL N/A
:16R:TRADDET N/A
:98A::TRAD//ccyymmdd SFTtradedate.
Shouldalwaysbethecurrentdate.
Char8 Tag75
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 53

---

## Page 54

MT547/MT545 Description/Values Lengthof
DataField
InputTagNumber
(ifapplicable)
:98A::ESET//ccyymmdd SFTsettlementdate.
NextDaySettlementforOff-Legtransactions,currentdateforothers.
Char8 N/A
:90A::DEAL//ACTU/USD000000,00000Pricepershareofthetransaction. 9(6).9(5) Tag31
:35B:ISINXXXXXXXXXXXX ISINID Char12 l Tag48(ifTag22
=4)
l N/A(ifTag
22=1)
:16R:FIA N/A
:92A::CUFC//00000,0000 RatetocalculatetheIndependentAmountforthetransactioninpercent
(%).
9(5).9(4) Tag159
:92A::INTR//00000,0000 Interest/LendingRateisinpercent(%).
ThisfieldispopulatedonlywhenSFTTransactionTypeisRMOD forRate
Modification.
9(5).9(4) Tag158
:35B:/US/XXXXXXXXX [[CUSIP]] Char9 l Tag 48 
(if Tag 22 = 1)
l N/A(ifTag
22=4)
:16S:FIA N/A
:70E::SPRO//xxxxxxxxxxxxxxxxetc.Reservedforfutureuse. Char35*10 N/A
:16S:TRADDET N/A
:16R:FIAC N/A
:36B::ESTT//UNIT/00000000000,0Quantityofsharesbeingtraded. 9(11) Tag32
:36B::RSTT//UNIT/00000000000,0RecallTotalQuantity 9(11)
:97A::SAFE//xxxxxxxx Sellerforon-legandBuyerforoff-leg.
Identifiesaccountwherethefinancialinstrumentsaremaintained.
Char8 N/A
:16S:FIAC N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 54

---

## Page 55

MT547/MT545 Description/Values Lengthof
DataField
InputTagNumber
(ifapplicable)
:16R:SETDET N/A
:22F::STCO/DTCYTXNT/xxxx SFTTransactionType.
Values:
l BEXE–Buy-inExecution
l BKRO–BrokerReorg
l CANC–CanceledbyClient
l NEWL–NewLoan
l NEWS–Pre-establishedBilateralLoan
l NROL–NoRoll
l NRCA–NoRoll&CorporateAction
l PDIF–PriceDifferential
l RMOD–RateModification
l ROLL–Roll
l SNDS–Send-to-Settle
l TERC–LoanTermination
l TERN–NSCCTermination
Char4 Tag81
:22F::STCO/DTCYACTV/xxxx ActivityType
Value:STKL–StockLoan
Char4 N/A
:22F::STCO/DTCYDGCA/xxxxValues:
l CAUN-UndergoingaNon-supportedCorporateAction
l CHMR-CashMerger
l CPAN–NotUndergoingaCorporateAction
l CSMR-CashandStockMerger
l FSSP-ForwardStockSplit
l NMCG-NameChange
l RSSP-ReverseStockSplit
l STMR-StockMerger
Char4 N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 55

---

## Page 56

MT547/MT545 Description/Values Lengthof
DataField
InputTagNumber
(ifapplicable)
:22F::STCO/DTCY/xxxx ThisfieldisdisplayedonlywhentheTransactionTypeisRMODforRate
Modification.
Values:
l UIND–Interestwasupdated(refertofieldLending/InterestAmount).
l PRTY–Partieswereupdated(refertofieldLendingRateIndicator).
l BOTH–Interestandpartieswereupdated(refertobothfields
Lending/InterestAmount&LendingRateIndicator).
Char4 N/A
:22F::SETR/DTCY/xxxx LegIndicator
Values:
l ONLG–On-leg
l OFFL–Off-leg
l OTHR–Othervalue
Char4 N/A
:22F::BLOC/DTCY/xxxx RecallCounter Char4
:22F::SETS/DTCY/xxxx Interest/LendingRateIndicator
Values:
l NRTE–NoRate
l LEND–PaidtoLenderofsecurity
l BRRW–PaidtoBorrowerofsecurity
Char4 Tag825
:22F::COLA/DTCY/xxxx RoundingValues:
l NRND–NoRounding
l RND1–Roundedtonearest$0.01
l RND2–Roundedtonearest$0.05
l RND3–Roundedtonearest$0.10
l RND4–Roundedtothenearest$0.25
l RND5-Roundedtothenearest$1.00
Char4 Tag581
:16R:SETPRTY N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 56

---

## Page 57

MT547/MT545 Description/Values Lengthof
DataField
InputTagNumber
(ifapplicable)
:95Q::BUYR//xxxxxxxx NSCCidentifieroftheOriginalBuyparticipant–SettlementAccount. Char8 Tag448
(withTag452=04)
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95R::DEAG/DTCYPART/xxxxxxxxNSCCidentifieroftheOriginalBuyparticipant–SFTAccount. Char8 N/A
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95Q::DEI1//xxxx NSCCidentifieroftheSendingEntity(vendor). Char4 Tag115
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95Q::SELL//xxxxxxxx NSCCidentifieroftheOriginalSellparticipant–SettlementAccount. Char8 Tag448
(with Tag 452 = 04)
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95R::REAG/DTCYPART/xxxxxxxxNSCCidentifieroftheOriginalSellparticipant–SFTAccount. Char8 N/A
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95P::PSET//DTCYUS33 PlaceofSettlement Char8 N/A
:16S:SETPRTY N/A
:16R:AMT N/A
:19A::ACRU//USD000000000000,00Lending/InterestAmount
PopulatedonlywhentheTransactionTypeisRMODforRateModification.
9(12).9(2) N/A
:16S:AMT N/A
:16R:AMT N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 57

---

## Page 58

MT547/MT545 Description/Values Lengthof
DataField
InputTagNumber
(ifapplicable)
:19A::DEAL//USD000000000000,00ContractAmount
CalculatedasPricexShares
9(12).9(2) N/A
:16S:AMT N/A
:16R:AMT N/A
:19A::ESTT//USD000000000000,00SettlementAmount
CalculatedasContractAmount+IndependentAmount
9(12).9(2) N/A
:16S:AMT N/A
:16R:AMT N/A
:19A::OTHR//USD000000000000,00Independentamount. 9(12).9(2) N/A
:16S:AMT N/A
:16S:SETDET N/A
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 58

---

## Page 59

RecallandBuy-InMessageFormats
Viewtheinputandoutputfileformatsforrecallandbuy-in:
l MT548:RecallandBuy-InExecutionOutputMessageFormats
l MT542:RecallandBuy-InInputMessageFormats
MT548:RecallandBuy-InExecutionOutputMessageFormats
ThefollowingtableshowstheISOMT548outputmessageformatsforRecallandBuy-Intransactions.ThisoutputisprovidedtotheApprovedSFT
Submitter,MemberstotheSFT,orboth.Itincludesoutputonarecall,cancelrecall,buy-inexecution,andcancelbuy-inexecution.Itisalsousedfor
updatestooutstandingrecallsagainstanSFTthatwasupdatedresultingfromaSend-toSettleorCorporateActionbeingprocessed.TheoutputisMT548
andtheCDTSProductisCNSISOO.
ISOTagMT548 Description LengthofData
Field
MandatorySequenceAGeneralInformation
:16R:GENL StartofBlock
:20C::SEME//xxxxxxxxxxxxxxxxDTCCgenerated.Usedtotrackthetransactionfromsubmissiontothe
finalstate.
:23G:INST
:98C::PREP//yyyymmddhhmmssProcessingtimestamp. Char14
RepetitiveMandatorySubsequenceA1Linkages
:16R:LINK StartofBlock
:20C::RELA//xxxxxxxxxxxxxx DTCCReferenceIDoftheoutstandingSFT. Char14
:16S:LINK EndofBlock
:16R:LINK StartofBlock
:20C::COMM//xx DTCCgenerated.
RecallIDorBuy-inID
Char2
:16S:LINK EndofBlock
EndofSubsequenceA1Linkages
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 59

---

## Page 60

ISOTagMT548 Description LengthofData
Field
RepetitiveMandatorySubsequenceA2Status
:16R:STAT StartofBlock
:25D:SETT/DTCY/xxxx Statusofthetransaction.
Values:
l ACPT=Accepted
l CLSD=Closed
l EXED=Full/PartialRecallExecution(willbesentforpartialSFTExecution)
l MADE=Full/PartialRecallMADE(willbesentforpartialSFTMADE)
l RCVD=Buy-InExecutionReceived
l RJCT=Rejected
l UPDT=RecallupdateduetoaCorporateAction
Char4
RepetitiveOptionalSubsequenceA2aReason
:16R:REAS StartofBlock
:24B::REJT/DTCY/xxxx Optional.Usedonlyforrejectedtransactions.
Value:
RJCT=Rejected
Char4
:70D::REAS//xxxxxxxxxxxxxxxxetc.Optional.Usedonlyforrejectedtransactions.
Explainswhythemessagewasnotprocessed.
Char1-210
:16S:REAS EndofBlock
EndofSubsequenceA2aReason
:16S:STAT EndofBlock
EndofSubsequenceA2Status
:16S:GENL EndofBlock
EndofSequenceAGeneralInformation
OptionalSequenceBSettlementTransactionDetails
:16R:SETTRAN StartofBlock
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 60

---

## Page 61

ISOTagMT548 Description LengthofData
Field
:35B:/US/XXXXXXXXX SecurityIDinaCUSIPformat. Char9
l :36B::SETT//UNIT/00000000000,0
-or-
l :36B::SETT//AMOR/00000,0000
l Quantityofsharesbeingtraded.
-or-
l Sharequantityorlendingrate.TheAMOR qualifierisusedonlywhentheTransaction
Type=RMOD.
Num11
-or-
If AMOR, use
PIC9(5).9(4)
:19A::SETT//USD000000000000,00Totalamountofthebuy-inexecutioncalculatedas:
TotalSharesoftheExecutionxAveragePrice
Num15
:19A::OCMT//USD000000000000,00AccruedInterest.
FutureuseforwhenexpandedtoCorporateBonds.
Num15
:97A::SAFE//xxxxxxxx SFTClearingMember(alwaysBorrower)-inpossessionofsecurities. Char8
:22F::SETR/DTCYREAS/xxxxRoleofthemessagerecipient.
Values:
l LEND=Lender
l BRRW=[[Borrower]]
Char4
:22H::REDE//xxxx Deliverer/Recipientindicatorforthemessagerecipient.
Values:
l DELI=UsedifyouarethedelivererofsharesatDTC([[Borrower]]).
l RECE=UsedifyouarethereceiverofsharesatDTC(Lender).
Char4
:22H::PAYM//xxxx Paymentindicator.
Value:
FREE=forfreetransactions.
Char4
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 61

---

## Page 62

ISOTagMT548 Description LengthofData
Field
:22F::STCO/DTCYTXNT/xxxxTransactionTypes
Values:
l BEXE=Buy-InExecution
l CBEX=CancelBuy-InExecution
l CRCL=CancelRecall
l RCLL=Recall
l RMOD=RateModification
l SNDS=Sent-to-Settle
Char4
:22F::SETS/DTCY/xxxx Sub-AccountCode.
Value:
l SUBT=SFTSub-account
Char4
:22F::SETS/DTCY/xxxx Lendrateindicator.
Values:
l BRRW-PaidtotheBorrower
l LEND-PaidtotheLender
l NRTE-NoRate
l OTHR-Othervalue
Char4
:98C::EXSE//ccyymmddhhmmssTimetherecallwasreceived.
UsedonlyforRCLL=Recallmessages.
Char14
:98A::SETT//yyyymmdd Datetherecallwasreceived. Char8
:98A::TRAD//yyyymmdd Alloweddateoftheexecution.
UsedonlyforacceptedRCLL=Recallmessages.
Char8
:70E::SPRO//xxxxxxxxxxxxxxetc. ContactInformation,5linesupto35characterseach:
l ContactNameonthefirstline.
l Contacttelephonenumberonthesecondline.
l Contactemailonlines3,4,and5.
Char0-175
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 62

---

## Page 63

ISOTagMT548 Description LengthofData
Field
RepetitiveOptionalSubsequenceB1SettlementParties
:16R:SETPRTY StartofBlock
:95Q::BUYR//xxxxxxxx SFTClearingAccountoftheoriginallendersubmittingthemessage. Char8
:16S:SETPRTY EndofBlock
:16R:SETPRTY StartofBlock
:95R::DEAG/DTCYPART/xxxxxxxxSettlingaccountoftheoriginallendersubmittingthemessage. Char8
:16S:SETPRTY EndofBlock
:16R:SETPRTY StartofBlock
:95Q::DECI//xxxx SubmittingEntity.
Partythatsubmitsonbehalfofthemember.
Char4
:16S:SETPRTY EndofBlock
:16R:SETPRTY StartofBlock
:95Q::SELL//xxxxxxxx SFTClearingAccountoftheoriginalBorrowersubmittingthemessage. Char8
:16S:SETPRTY EndofBlock
:16R:SETPRTY StartofBlock
:95R::REAG/DTCYPART/xxxxxxxxSettlingaccountoftheoriginalBorrower. Char8
:16S:SETPRTY EndofBlock
:16R:SETPRTY StartofBlock
:95P::PSET//DTCYUS33 DepositoryID.
Value:
DTCYUS33
Char8
:16S:SETPRTY EndofBlock
EndofSequenceB1SettlementParties
:16S:SETTRAN EndofBlock
EndofSequenceBSettlementTransactionDetails
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 63

---

## Page 64

MT542:RecallandBuy-InInputMessageFormats
ThefollowingtableshowstheISOMT542inputmessageformatsforRecallandBuy-Intransactions,CDTSProduct-–CNSISOI.Thismessageformatwill
beusedbytheApprovedSFTSubmittertoinputarecall,cancelrecall,buy-inexecution,orcancelbuy-inexecutionmessage.
ISOTagMT542 InputValuesandRules LengthofData
Field
MandatorySequenceAGeneralInformation
:16R:GENL StartofBlock
:20C::SEME//xxxxxxxxxxxxxxxxSender'sreferencenumber.
:23G:NEWM NEWMwillbepopulated(Newmessage).
OptionalRepetitiveSubsequenceA1Linkages
:16R:LINK StartofBlock
:20C::RELA//xxxxxxxxxxxxxx DTCCReferenceIDoftheoutstandingloan.
Rule:
Ifnotsubmitted,notfoundinNSCC,orineligiblefortherequest,rejectedwithcode57.
Char14
:16S:LINK EndofBlock
EndofSubsequenceA1Linkages
OptionalRepetitiveSubsequenceA1Linkages
:16R:LINK StartofBlock
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 64

---

## Page 65

ISOTagMT542 InputValuesandRules LengthofData
Field
:20C::COMM//xx RecallID orBuy-InID.
Rules:
l Ifnotsubmittedfortherequiredtransactiontypes,CRCL=CancelRecallorCBEX=
CancelBuy-inExecution,rejectedwithcode09.
o RecallIDtobecanceledfortheCRCL=CancelRecallmessagetype.
o Rejectwithcode09ifitdoesnotmatchanypendingRecallinNSCC.
l Buy-inExecutionIDiscanceledfortheCBEX=CancelBuy-inExecutionmessagetype.
o IfitdoesnotmatchanypendingBuy-InExecutioninNSCC,rejectedwithcode09.
o IfsubmittedfortheRCLL=RecallorBEXE=Buy-inExecutionmessagetype,[[NSCC]]
ignores.
Note:TheRecallIDisnotneededonabuy-inexecutionastheexecutioncanbeformultiple
RecallIDs.NSCCalwaysusesabuy-inexecutiontooffsetthesharesoutstandingofthe
oldestrecallinthesystemfirst.
Char2
:16S:LINK EndofBlock
EndofSubsequenceA1Linkages
:16S:GENL EndofBlock
EndofSequenceAGeneralInformation
MandatorySequenceBTradeDetails
:16R:TRADDET StartofBlock
:98A::SETT//yyyymmdd Transactionprocessingdate.ShouldbethecurrentdateinYYYYMMDDformat.
Rule:
ForBEXE,ifpriorthantheoldestAllowedExecutionDateonopenrecallsfortheloan,
rejectedwithcode02.
Char8
:35B:ISINXXXXXXXXXXXX SecurityISINIDontheloan.
Rule:
MustmatchISINontheoriginalloan;otherwise,rejectedwithcode03.
Char12
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 65

---

## Page 66

ISOTagMT542 InputValuesandRules LengthofData
Field
:35B:/US/XXXXXXXXX [[CUSIP]] [[ID]] ontheloan.
Rule:
MustmatchCUSIPontheoriginalloan;otherwise,rejectedwithcode03.
CHAR9
OptionalSubsequenceB1FinancialInstrumentAttributes
:16R:FIA StartofBlock
:92A::INTR//000000000000,00 ForfutureuseforAccruedInterest.
Rules:
l Currently,notusedbyNSCC;ignoredifsubmitted.
Num5
:90B::EXER//ACTU/USD000000,000000Averagepricepersharefortheexecution.
Rules:
l RequiredfortheBEXE=Buy-inExecutionmessagetype.Ifnotsubmittedornon-
numeric,rejectedwithcode05.
l IfsubmittedfortheRCLL=Recall,CRCL=CancelRecall,orCBEX=CancelBuy-In
Executionmessagetype,NSCCignores.
Numeric
999999,999999
:16S:FIA EndofBlock
EndofSubsequenceB1FinancialInstrumentAttributes
:22F::PROC/DTCY/ISOI MessageID.
Rule:
ISOI=CNSISOInput([[default]])
Char4
:70E::SPRO//xxxxxxxxxxxxxxxxetcContactInformation,5linesupto35characterseach:
l ContactNameonthefirstline.
l Contacttelephonenumberonthesecondline.
l Contactemailonlines3,4,and5.
Char0-175
:16S:TRADDET EndofBlock
EndofSequenceBTradeDetails
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 66

---

## Page 67

ISOTagMT542 InputValuesandRules LengthofData
Field
MandatorySequenceCFinancialInstrument/Account
:16R:FIAC StartofBlock
:36B::SETT//UNIT/0000000000000,0Sharequantity.
Rules:
l RequiredfortheRCLL=RecallorBEXE=Buy-inExecutionmessagetype.
l ForCRCL=CancelRecallandCBEX=CancelBuy-inExecution,sharequantityofzero
(0)isaccepted.
l ForRCLL=Recall,cannotexceedoutstandingnot-recalledsharesoftheoff-leg;
otherwise,rejectedwithcode04.
l ForBEXE=Buy-InExecution,cannotexceedsumofsharesofallopenrecallsforthe
loan;otherwise,rejectedwithcode04.
Note:NopartialcancellationisallowedforaRecalloraBuy-InExecution.Itmustalwaysbe
forthefullamountoftheshares.
Num11
:97A::SAFE//xxxxxxxx SFTClearingAccountIDoftheoriginalLendersubmittingthemessage.
Rule:
MustmatchLenderSFTParticipantIDontheoriginaloff-leg;otherwise,rejectedwithcode
01.
Char8
:16S:FIAC EndofBlock
EndofSequenceCFinancialInstrument/Account
MandatorySequenceESettlementDetails
:16R:SETDET StartofBlock
:22F::SETS/DTCY/SUBT NSCCSub-AccountCode.
l SUBT=Sub-Account,wherebyTistheidentifierforSFTClearing.
Char4
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 67

---

## Page 68

ISOTagMT542 InputValuesandRules LengthofData
Field
:22F::SETR/DTCYTXNT/xxxx Transactiontype.
Allowedvalues:
l BEXE=Buy-inExecution
l CBEX=CancelBuy-inExecution
l CRCL=CancelRecall
l RCLL=Recall
Otherwise,themessageisbypassed.
Char4
RepetitiveMandatorySubsequenceE1SettlementParties
:16R:SETPRTY StartofBlock
:95R::DEAG/DTCYPART/xxxx SubmittingFirmID/SendingEntityID
DTCIDofthefirmsubmittingthemessage;sameastheSendingEntityinUTC.
Rule:
MustmatchtheSubmittingFirmIDontheoriginalloan;otherwise,rejectedwithcode14.
Char4
:16S:SETPRTY EndofBlock
:16R:SETPRTY StartofBlock
:95P::PSET//DTCYUS33 Settlementlocation.DepositoryID
Value:
DTCYUS33
Char8
:16S:SETPRTY EndofBlock
EndofSubsequenceE1SettlementParties
:16S:SETDET EndofBlock
EndofSubsequenceESettlementDetails
SFTClearing:InputandOutputMessageLayouts
ISOMessageQueue(MQ)MessageFormats 68

---

## Page 69

DTCINPUTANDOUTPUTMESSAGES
ThefollowingtableprovidelinksfortheDTCinputmessages:
Note
Toaccesstheinputandoutputmessaging,includingtheProprietaryDO,ISO [[DO]] Input,DTFDO Output,MQ DOOutput,MQ PO Output,andISO Output
Messagefiles,seetheCCF Settlementfilesavailableat:
https://www.[[DTCC]].com/[[settlement]]-and-[[Asset]]-services/[[settlement]]/[[CCF]]-new-[[settlement]]
MessageType Format MessageTypeComments
Deliver Order Input File
(DOI1/DOI5)
Proprietary l MQ
l FTP
l NDM
ModifiedtoincludeSFTDOs(reasoncode200,receiver881andcrossreferenceincomments)
DeliverOrders
(DOX1/DOX5)
Proprietary l MQ
l FTP
l NDM
ModifiedtoincludeSFTDOs(reasoncode200,receiver881andcrossreferenceincomments)
DeliverOrderInput ISO MT543 ModifiedtoincludeSFTDOs(reasoncode200,receiver881andcrossreferenceincomments)
Table7.1DTCInputMessages
SFTClearing:InputandOutputMessageLayouts
DTCInputandOutputMessages 69

---

## Page 70

ThefollowingtableprovidelinksfortheDTCoutputmessages:
MessageType Format MessageType Comments
[[settlement]] [[participant]] Activity
(DTFPART)
DTF MQ ModifiedtoaccommodateSFTDOs.
SettlementStatus ISO l MT545
l MT547
l MT548
ModifiedtoaccommodateallSFTactivity.
SettlementParticipantActivity
(PARTPO)
DTF MQ ModifiedtoaccommodateSFTPOs.
ProprietaryOutput Proprietary SMART ModifiedtoincludeSFTDOsandPOs.
SFTDropFile Drops MT548 ModifiedtoincludeproprietaryandISOdrops(TBD).
Table7.2DTCOutputMessages
SFTClearing:InputandOutputMessageLayouts
DTCInputandOutputMessages 70

---

## Page 71

FOR MORE INFORMATION
EmailDTCCLearningat:
corelearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com
© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and unregistered 
trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). 
[[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or 
countries in which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Doc Info: July 12, 2022
Publication Code: SFT134a
Service: [[securities]] Financing Transaction ([[SFT]]) Clearing
Title: Input and Output Message Layouts