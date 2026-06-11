---
title: "CNS Intraday ISO 15022 Message Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cns175_rl_intraday_output_iso15022_2023Oct26.pdf"
pages: 12
size: "297.8 KB"
category: "CNS"
ingested_on: "2026-06-05"
---

# CNS Intraday ISO 15022 Message Format

**Original File:** [cns175_rl_intraday_output_iso15022_2023Oct26.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cns175_rl_intraday_output_iso15022_2023Oct26.pdf)  
**Category:** CNS  
**Total Pages:** 12  
**File Size:** 297.8 KB  

---

## Page 1

[[CNS]]®
CNSINTRADAYISO15022MESSAGEFORMAT
JUNE27,2017
HereistheISO15022outputmessageformatfromCNS®.SeealsotheISO15022site.ThismessageissenttoparticipantswhentheirCNS
positionchangesduetonewsettlingtradesornewmiscellaneousactivityinthedaycycle.
l SequenceAcontainsgeneralinformationaboutthemessagebeingsent.
l SequenceBcontainsinformationabouttheParticipantsCNSposition.
l SequenceCcontainsinformationaboutnewtradessettledinthedaycycle.
l SequenceDcontainsinformationaboutmiscellaneousactivitytakingplaceduringthedaycycle.
Notes
l AparticipantneverreceivesSequenceCandSequenceDinformationtogether.
l Normallyeachmessagecontainseitherone(1)SequenceCorone(1)Sequence(D).
l TheISOfieldtagisdefinedasauniquestringofcharactersidentifyingthemeaningandformatofthedataitem.Fieldtagswith
multipleformats,suchas98(formatcanbefordateordateandtime)or95(formatforpartymaybeexpressedinBIC,localmar-
ketidentifiersincludingadatasourcescheme,orfreeformatsuchasnameandaddress)areexpressedonthe
www.iso15022.orgwebsiteas98aand95a,respectively.Thefieldtagsareexpressedinthemessagebytheactualformat
used.Forexample,
98aDate/Timeiseitherexpressedas98A(qualifier)(date)or
98C(qualifier)(date)(time)
ISO15022MessageFormat
1

---

## Page 2

MT570IntradayCNSMessageonSettlementDay
ThefollowingtableshowstheMT570IntradayCNSMessageonSettlementDay:
ISOTag
Status
ISO
Tag
ISO
Qualifier
ISOGenericField
Name
ISODetailedField
Name
ISOContent
/Options
DTCCDataFieldExample
MandatorySequenceAGeneralInformation
M 16R StartofBlock GENL 16R:GENL
M 20C SEME REFERENCE SendersReference :4!c//16x 20C:SEME//16x
MessageControlnumber.
M 23G Functionofthemessage4!c[/4!c] 23G:NEWM
O 98a PREP Date/Time PreparationDate/Time:4!c//8!n6!n :98C:PREP//yyyymmddhhmmss
CNSusesthe98Coptionofthistagfor
thisdataitem.
M 16S EndofBlock 16S 16S:GENL
MandatorySequenceBPositionInformation
M 16R StartofBlock POSINFO 16R:POSINFO
ISO15022MessageFormat
2

---

## Page 3

ISOTag
Status
ISO
Tag
ISO
Qualifier
ISOGenericField
Name
ISODetailedField
Name
ISOContent
/Options
DTCCDataFieldExample
M 95a CLBR Party ParticipantNumber :4!c/4!c[4c]/34z 95R:CLBR/DTCY/<partnum>
CNSusesthe95Roptionofthistagfor
thisproduct.
M 22F ACCL Indicator CNSSubaccount :4!c/[4!c
[4c]]/4!c
22F:ACCL/DTCY/1digitalpha
SeeDTCCValues.
*TheDTCYqualifieroverridesthe
requirementforfourcharacterdata.
M 35B Identificationofthe
FinancialInstrument
[ISIN1!e12!c]
[4*35x]
35B:<country><[[CUSIP]]><check>
whereTransactiontablestoresthe
following:
l <country>isstoredintheCountryCode
field.
l <[[CUSIP]]>isstoredintheCUSIPfield.
l <check>isstoredintheCheckDigit
field.
ISO15022MessageFormat
3

---

## Page 4

ISOTag
Status
ISO
Tag
ISO
Qualifier
ISOGenericField
Name
ISODetailedField
Name
ISOContent
/Options
DTCCDataFieldExample
M 93B FIOP Position
(repetitivefield)
FirstOpeningposition :4!c/[4!c
[4c]]/4!c/[s]15d
93B:FIOP//UNIT/+15d
NetOpeningpositionatstartofdaycycle.
M 22H OPDC Indicator
(repetitivefield)
CycleofPosition :4!c//4!c 22H:OPDC//OPDC
DayCycle
M 36B NSTT Quantity NetSettlingTrades :4!C//4!C/15d36B:NSTT//UNIT/15d
Netofsettlingtradesinthedaycycle.
Cumulativetothispoint.
M 22H CRDB Indicator Credit/debitindicator :4!c//4!c 22H:CRDB//CRED
22H:CRDB//DEBT
ThistagqualifiesNetOfSettlingTrades.
ISO15022MessageFormat
4

---

## Page 5

ISOTag
Status
ISO
Tag
ISO
Qualifier
ISOGenericField
Name
ISODetailedField
Name
ISOContent
/Options
DTCCDataFieldExample
M 36B NMAC Quantity NetMiscellaneous
Activity
:4!C//4!C/15d36B:NMAC//UNIT/15d
NetofdaycycleMiscellaneousactivity.
Cumulativetothispoint.
M 22H CRDB Indicator Credit/debitindicator :4!c//4!c: 22H:CRDB//CRED
22H:CRDB//DEBT
ThistagqualifiesNetofDayCycle
Miscellaneousactivity.
M 36B ALLO Quantity QuantityAllocated :4!c//4!c/15d 36B:ALLO//UNIT/15d
NetofdaycycleSharesReceivedor
Delivered.
Cumulativetothispoint.
M 22H CRDB Indicator Credit/debitindicator :4!c//4!c l 22H:CRDB//CRED=ShortPosition
l 22H:CRDB//DEBT=LongPosition
ThistagqualifiestheNewofDayCycle
sharesreceived.
ISO15022MessageFormat
5

---

## Page 6

ISOTag
Status
ISO
Tag
ISO
Qualifier
ISOGenericField
Name
ISODetailedField
Name
ISOContent
/Options
DTCCDataFieldExample
M 93B AGGR Balance AggregateBalance :4!c/[4!c[4c]]/4!c/
[s]15d 93B:AGGR//UNIT/+15d
NetofCurrentCNSPosition
MandatorySequenceB1PositionDepositoryInformation
M 16R StartofBlock B1 16R:DEPINFO
M 11A SETT CurrencyCode SettlementCurrency :4!c//3!a 11A:SETT//USD
M 95a DEBA Party DepositaryBank :4!c/4!c
[4c]/34z
95R:DEBA/DTCY/<partnum([[DTC]])
CNSusesthe95Roptionofthistagfor
thisproduct.
M 16S EndofBlock(B1) DEPINFO 16S:DEPINFO
M 16S EndofBlock(B) POSINFO 16S:POSINFO
OptionalSequenceCNetSettlingTradesDetail
(EntireBlockcanrepeat.AsCNSiscurrentlyformattingthismessage,norepetitiveblocksaregenerated).
M 16R StartofBlock 16R 16R:NSTD
ISO15022MessageFormat
6

---

## Page 7

ISOTag
Status
ISO
Tag
ISO
Qualifier
ISOGenericField
Name
ISODetailedField
Name
ISOContent
/Options
DTCCDataFieldExample
M 94B TRAD Place PlaceofTrade :4!c/[4!c
[4c]]/4!c[/30z]
94B:TRAD/DTCY/<StockExchange
Code
ThisfieldisalwaysSpaces.
M 22H BUSE Indicator Buy/Sell :4!c//4!c 22H:BUSE//BUYI
Note:Thisisacapitalletter“eye”.
22H:BUSE//SELL
M 36B QSEC Quantityof
Financial
Instrument
QuantityofSecurities :4!C//4!C/15d36B:QSEC//UNIT/15d
M 95a CTRA Party ContraBroker :4!c/4!c
[4c]/34z
95R:CTRA/DTCY/<partnum>
CNSusesthe95Roptionofthistagfor
thisproduct.
M 22H NSDC Indicator NetSettlingTrade
Cycle
:4!c//4!c 22H:NSDC//NSDC
DayCycle
M 19A PRIN Amount ContractValue :4!c//[s]3!a15d 19A:PRIN//(s)USD15d
ISO15022MessageFormat
7

---

## Page 8

ISOTag
Status
ISO
Tag
ISO
Qualifier
ISOGenericField
Name
ISODetailedField
Name
ISOContent
/Options
DTCCDataFieldExample
M 98a TRAD Date/Time TradeDate :4!c//8!n 98A:TRAD//MMDDCCYY
CNSusesthe98Aoptionofthistagfor
thisproduct.
O 20C EVMU REFERENCE Exchange/VMU
Reference
:4!c//16x 20C:EVMU//16x
M 16S EndofBlock 16S 16S:NSTD
OptionalSequenceDMiscellaneousActivity
(EntireBlockcanrepeat.AsCNSiscurrentlyformattingthismessage,norepetitiveblocksaregenerated).
M 16R StartofBlock 16R 16R:MSAC
M 22H NMDC Indicator NetMisc.ActivityCycle :4!c//4!c 22H:NMDC//NMDC
DayCycle
M 36B ADJU Quantityof
Financial
Instrument
Quantityof
Miscellaneousactivity
:4!C//4!C/15d36B:ADJU//UNIT/15d
M 22H CRDB Indicator Credit/debitindicator :4!c//4!c l 22H:CRDB//CRED=ShortPosition
l 22H:CRDB//DEBT=LongPosition
ISO15022MessageFormat
8

---

## Page 9

ISOTag
Status
ISO
Tag
ISO
Qualifier
ISOGenericField
Name
ISODetailedField
Name
ISOContent
/Options
DTCCDataFieldExample
M 19A VALU Amount :4!c//[s]3!a15d 19A:VALU//(s)USD15d
M 22F TYMA Indicator TypeofAdjustment :4!c/[4!c[4c]]/4!c22F:TYMA/DTCY/xx
SeeDTCCValues.
*TheDTCYqualifieroverridesthe
requirementforfourcharacterdata.
M 98a PROC Date/Time Internaltimestamp :4!c//8!n6!n :98C:PROC//yyyymmddhhmmss
CNSusesthe98Coptionofthistagfor
thisproduct.
M 16S EndofBlock 16S 16S:MSAC
ENDOFMESSAGE
ISO15022MessageFormat
9

---

## Page 10

DTCCValues
CNSSub-AccountValuesSequenceBTag22F:
l A=RegularAccount
l E=FullyPaidFor
l G=Reorg#1
l H=Reorg#2
l R=ACATSLong
l S=ACATSShort
TypeofAdjustmentValuesSequenceDTag22F:
l 02=CNSIneligible/MuniBondExit
l 17=IDNet
l 18=IDNetReject/Reversal
l 20=MemberFirmMerger
l 25=HonestBroker
l 30=NameChange
l 35=ACATS-ODS(CNSEligible)
l 36=ACATS-ODS([[DTC]],notCNSEligible)
l 50=Reorg-NameChange
l 51=Reorg-Merger
l 52=Reorg-Redemption
l 53=Reorg-Ineligible-Tender
l 54=Reorg-ReverseSplit
l 55=DailyBalAfterAllocation
l 56=ReorgExit
l 59=IndexWTSExercise
l 65=ACATS(CNSEligible)
ISO15022MessageFormat
10

---

## Page 11

l 66=ACATS([[DTC]],notCNSEligible)
l 71=JNL-TradeAdjustment
l 73=JNL-DividendAdjustment
l 74=InterAccountNetting/InterAcctTransfer
l 75=JNL-Received/DeliveredAdj
l 76=RIOB/OIntotheCNSsystem
l 77=JNL-Buy-InExecution
l 79=JNL-CNSIneligibleAdjustment
l 81=JNL-ReorgAdjustment
l 83=JNL-MemberFirmAdjustment
l 92=TransferIntoFullyPaidForAccount
l 93=TransferOutOfFullyPaidForAccount
ISO15022MessageFormat
11

---

## Page 12

© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation [[DTCC]]. The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of 
The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see www.[[DTCC]].com for more 
information on [[DTCC]], its affiliates and the services they offer.
Doc Date: October 26, 2023
Publication Code: CNS175
Service: [[CNS]]
Title: [[CNS]] Intraday ISO 15022 Message Format
For More Information
Email [[DTCC]] Learning at:
corelearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com