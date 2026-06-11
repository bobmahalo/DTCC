---
title: "CNS Seg Exemption Input: DataTrak ID 06121 - Original and Y2K Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cns165_rl_seg_exemption_input_06121_2022Sept13.pdf"
pages: 12
size: "1177.8 KB"
category: "CNS"
ingested_on: "2026-06-05"
---

# CNS Seg Exemption Input: DataTrak ID 06121 - Original and Y2K Format

**Original File:** [cns165_rl_seg_exemption_input_06121_2022Sept13.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cns165_rl_seg_exemption_input_06121_2022Sept13.pdf)  
**Category:** CNS  
**Total Pages:** 12  
**File Size:** 1177.8 KB  

---

## Page 1

[[CNS]]®
[[CNS]] SEG EXEMPTION: DATATRAK [[ID]] 06121 - ORIGINAL AND Y2K 
FORMAT
SEPTEMBER 13, 2022


---

## Page 2

[[CNS]]®SegExemption:DataTrakID06121-OriginalandY2KFormat 2
[[CNS]]®SEGEXEMPTION:DATATRAKID06121-ORIGINALANDY2KFORMAT
ViewtheCNSSegExemption:DataTrakID06121-OriginalandY2Kformat.
DataTrack/MQ:ParticipantInputtoNSCC.
OptionalHeaderRecord
ThefollowingtableshowstheOptionalHeaderrecorddetailsfortheCNSSegExemption:DataTrakID06121-
OriginalandY2Kformat:
DataTrakID06121-OriginalandY2KFormat
OptionalHeaderRecord
RecordLength=80
Description Length Start End Type Comments
FutureUse 10 1 10 A Reserved
FileDescription
(Left-justified)
13 11 23 A/N [[CNS]]-SEG-EDIT
Only12characters,butthelengthis13.
Date 6 24 29 A/N MMDDYY
FutureUse 1 30 30 A Reserved
OptionalDateY2K 8 31 38 A/N MMDDCCYY
FutureUse 42 39 80 A Reserved
ENDOFRECORD
DataTrakID06121-OriginalandY2KFormat

---

## Page 3

[[CNS]]®SegExemption:DataTrakID06121-OriginalandY2KFormat 3
ExemptionDetailRecord
ThefollowingtableshowstheExemptionDetailrecorddetailsfortheCNSSegExemption:DataTrakID06121-
OriginalandY2Kformat:
DataTrakID06121-OriginalandY2KFormat
ExemptionDetailRecord
RecordLength=80
Description Length Start End Type Comments
[[participant]] Clearing Number4 1 4 A/N Four-digitnumberassignedbyNSCC.
[[participant]] Subaccount 1 5 5 A/N l A=RegularAccount
l B=Open
l C=FormerlyStockBorrow
l D=DepositoryReceivable
l E=FullyPaidFor
l F=Open
l G=Reorg#1
l H=Reorg#2
l I–Q=Open
l R=ACATSLong
l S=ACATSShort
l T–Z=Open
Note:Exemptioninputisonlyacceptedfor
SubaccountAandS.
[[CUSIP]] 9 6 14 A/N
Constant 3 15 17 N Always=000
Quantity 9 18 26 N Quantitytobeexempted.
999,999,999
DataTrakID06121-OriginalandY2KFormat

---

## Page 4

[[CNS]]®SegExemption:DataTrakID06121-OriginalandY2KFormat 4
DataTrakID06121-OriginalandY2KFormat
ExemptionDetailRecord
RecordLength=80
Description Length Start End Type Comments
LevelExemption 1 27 27 N 1or2
Note:
l BothExemptionLevel1and2canbe
processedforSubaccountA.
l OnlyExemptionLevel1canbeprocessedfor
SubaccountS.
ExemptAllIndicator 1 28 28 A/N Acceptedvalues:
l 0orspace=Fieldisignored.
l Y=AllshortpositionsfortheCUSIPindicatedin
Bytes6-14areassignedthelevelexemption
indicatedinByte27.ForSub-AccountA,avalueof
1or2canbeusedinByte27.ForSub-AccountS,
onlyavalueof1canbeusedinByte27.
FutureUse 52 29 80 A Reserved
ENDOFRECORD
DataTrakID06121-OriginalandY2KFormat

---

## Page 5

[[CNS]]®SegExemption:DataTrakID06121-OriginalandY2KFormat 5
Level1,Trailer1
ThefollowingtableshowstheLevel1,Trailer1recorddetailsfortheCNSSegExemption:DataTrakID06121-
OriginalandY2Kformat:
DataTrakID06121-OriginalandY2KFormat
Level1,Trailer1
RecordLength=80
Description Length Start End Type Comments
[[participant]] Clearing Number4 1 4 A/N Four-digitnumberassignedbyNSCC.
ParticipantSubaccount 1 5 5 A/N l A=RegularAccount
l B=Open
l C=FormerlyStockBorrow
l D=DepositoryReceivable
l E=FullyPaidFor
l F=Open
l G=Reorg#1
l H=Reorg#2
l I–Q=Open
l R=ACATSLong
l S=ACATSShort
l T–Z=Open
Note:Exemptioninputisonlyacceptedfor
SubaccountAandS.
Constant 12 6 17 N Always=999999999999
RecordCount 9 18 26 N NumberofLevel1exemptions,includingheader
andtrailer.
999,999,999
RecordID 2 27 28 N Always=81
FutureUse 52 29 80 A Reserved
ENDOFRECORD
DataTrakID06121-OriginalandY2KFormat

---

## Page 6

[[CNS]]®SegExemption:DataTrakID06121-OriginalandY2KFormat 6
Level1,Trailer2
ThefollowingtableshowstheLevel1,Trailer2detailsfortheCNSSegExemption:DataTrakID06121-Originaland
Y2Kformat:
DataTrakID06121-OriginalandY2KFormat
Level1,Trailer2
RecordLength=80
Description Length Start End Type Comments
[[participant]] Clearing Number4 1 4 A/N Four-digitnumberassignedbyNSCC.
ParticipantSubaccount 1 5 5 A/N l A=RegularAccount
l B=Open
l C=FormerlyStockBorrow
l D=DepositoryReceivable
l E=FullyPaidFor
l F=Open
l G=Reorg#1
l H=Reorg#2
l I–Q=Open
l R=ACATSLong
l S=ACATSShort
l T–Z=Open
Note:Exemptioninputisonlyacceptedfor
SubaccountAandS.
Constant 12 6 17 N Always=999999999999
RecordCount 9 18 26 N TotalquantityforLevel1exemptions.
999,999,999
RecordID 2 27 28 N Always=91
FutureUse 52 29 80 A Reserved
ENDOFRECORD
DataTrakID06121-OriginalandY2KFormat

---

## Page 7

[[CNS]]®SegExemption:DataTrakID06121-OriginalandY2KFormat 7
Level2,Trailer1
ThefollowingtableshowstheLevel2,Trailer1recorddetailsfortheCNSSegExemption:DataTrakID06121-
OriginalandY2Kformat:
DataTrakID06121-OriginalandY2KFormat
Level2,Trailer1
RecordLength=80
Description Length Start End Type Comments
[[participant]] Clearing Number4 1 4 A/N Four-digitnumberassignedbyNSCC.
ParticipantSubaccount 1 5 5 A/N l A=RegularAccount
l B=Open
l C=FormerlyStockBorrow
l D=DepositoryReceivable
l E=FullyPaidFor
l F=Open
l G=Reorg#1
l H=Reorg#2
l I–Q=Open
l R=ACATSLong
l S=ACATSShort
l T–Z=Open
Note:Exemptioninputisonlyacceptedfor
SubaccountAandS.
Constant 12 6 17 N Always=999999999999
RecordCount 9 18 26 N 999,999,999
NumberofLevel2exemptions,includingheaderand
trailer.
RecordID 2 27 28 N Always=82
FutureUse 52 29 80 A Reserved
ENDOFRECORD
DataTrakID06121-OriginalandY2KFormat

---

## Page 8

[[CNS]]®SegExemption:DataTrakID06121-OriginalandY2KFormat 8
Level2,Trailer2
ThefollowingtableshowstheLevel2,Trailer2detailsfortheCNSSegExemption:DataTrakID06121-Originaland
Y2Kformat:
DataTrakID06121-OriginalandY2KFormat
Level2,Trailer2
RecordLength=80
Description Length Start End Type Comments
[[participant]] Clearing Number4 1 4 A/N Four-digitnumberassignedbyNSCC.
ParticipantSubaccount 1 5 5 A/N l A=RegularAccount
l B=Open
l C=FormerlyStockBorrow
l D=DepositoryReceivable
l E=FullyPaidFor
l F=Open
l G=Reorg#1
l H=Reorg#2
l I–Q=Open
l R=ACATSLong
l S=ACATSShort
l T–Z=Open
Note:Exemptioninputisonlyacceptedfor
SubaccountAandS.
Constant 12 6 17 N Always=999999999999
RecordCount 9 18 26 N TotalquantityforLevel2exemptions.
999,999,999
RecordID 2 27 28 N Always=92
FutureUse 52 29 80 A Reserved
ENDOFRECORD
DataTrakID06121-OriginalandY2KFormat

---

## Page 9

[[CNS]]®SegExemption:DataTrakID06121-OriginalandY2KFormat 9
PriorityDetail
ThefollowingtableshowsthePriorityDetailrecordinformationfortheCNSSegExemption:DataTrakID06121-
OriginalandY2Kformat:
DataTrakID06121-OriginalandY2KFormat
PriorityDetail
RecordLength=80
Description Length Start End Type Comments
[[participant]] Clearing Number4 1 4 A/N Four-digitnumberassignedbyNSCC.
ParticipantSubaccount 1 5 5 A/N l A=RegularAccount
l B=Open
l C=FormerlyStockBorrow
l D=DepositoryReceivable
l E=FullyPaidFor
l F=Open
l G=Reorg#1
l H=Reorg#2
l I–Q=Open
l R=ACATSLong
l S=ACATSShort
l T–Z=Open
Note:PriorityOverrideinputisonlyacceptedfor
SubaccountAandE.
[[CUSIP]] 9 6 14 A/N
Constant 3 15 17 N Always=000
FutureUse 8 18 25 A Reserved
RecordID 1 26 26 N 1
NightPriority 2 27 28 N l 64=Highpriority,night
l 68=Normalpriority,night
DataTrakID06121-OriginalandY2KFormat

---

## Page 10

[[CNS]]®SegExemption:DataTrakID06121-OriginalandY2KFormat 10
DataTrakID06121-OriginalandY2KFormat
PriorityDetail
RecordLength=80
Description Length Start End Type Comments
DayPriority 2 29 30 N l 64=Highpriority,night
l 68=Normalpriority,night
FutureUse 50 31 80 A Reserved
ENDOFRECORD
DataTrakID06121-OriginalandY2KFormat

---

## Page 11

[[CNS]]®SegExemption:DataTrakID06121-OriginalandY2KFormat 11
PriorityTrailer
ThefollowingtableshowsthePriorityTrailerrecordinformationfortheCNSSegExemption:DataTrakID06121-
OriginalandY2Kformat:
DataTrakID06121-OriginalandY2KFormat
PriorityTrailer
RecordLength=80
Description Length Start End Type Comments
[[participant]] Clearing Number4 1 4 A/N Four-digitnumberassignedbyNSCC.
ParticipantSubaccount 1 5 5 A/N l A=RegularAccount
l B=Open
l C=FormerlyStockBorrow
l D=DepositoryReceivable
l E=FullyPaidFor
l F=Open
l G=Reorg#1
l H=Reorg#2
l I–Q=Open
l R=ACATSLong
l S=ACATSShort
l T–Z=Open
Note:PriorityOverrideinputisonlyacceptedfor
SubaccountAandE.
Constant 12 6 17 N Always=999999999999
RecordCount 9 18 26 N 999,999,999
Numberofthepriority.
RecordID 2 27 28 N Always=84
FutureUse 52 29 80 A Reserved
ENDOFRECORD
DataTrakID06121-OriginalandY2KFormat

---

## Page 12

FORMOREINFORMATION
EmailDTCCLearningat:
corelearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com
©2022DTCC.Allrightsreserved.[[DTCC]],[[DTCC]](Stylized),ADVANCINGFINANCIALMARKETS.TOGETHER,
andtheInterlockergraphicareregisteredandunregisteredtrademarksofTheDepositoryTrustandClearing
Corporation.
Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandnamebycertainaffiliatesofTheDepository
TrustandClearingCorporation(“[[DTCC]]”).DTCCitselfdoesnotprovidesuchservices.Eachoftheseaffiliatesisa
separatelegalentity,subjecttothelawsandregulationsoftheparticularcountryorcountriesinwhichsuchentity
operates.Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,itsaffiliatesandtheservicestheyoffer.
DocInfo:September13,2022
PublicationCode:CNS165
Service:[[CNS]]
Title:CNSSegExemption:DataTrakID06121-OriginalandY2KFormat