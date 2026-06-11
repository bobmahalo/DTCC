---
title: "CNS Due Bill Activity MRO: AutoRoute ID 02040786"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cns154_rl_due_bill_activity_02040786_2022Aug18.pdf"
pages: 6
size: "1274.2 KB"
category: "CNS"
ingested_on: "2026-06-05"
---

# CNS Due Bill Activity MRO: AutoRoute ID 02040786

**Original File:** [cns154_rl_due_bill_activity_02040786_2022Aug18.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cns154_rl_due_bill_activity_02040786_2022Aug18.pdf)  
**Category:** CNS  
**Total Pages:** 6  
**File Size:** 1274.2 KB  

---

## Page 1

[[CNS]]®
[[CNS]] DUE BILL ACTIVITY MRO: AUTOROUTE [[ID]] 02040786
JUNE 22, 1999


---

## Page 2

[[CNS]]®DueBillActivityMRO:AutoRouteID02040786 2
[[CNS]]® DUE BILL ACTIVITY MRO: 
AUTOROUTE [[ID]] 02040786
ViewtheCNSDueBillActivityMROoutputinformationforAutoRouteID:02040786.
AutoRoute:ParticipantoutputfromNSCC.
Header Record
ThefollowingtableshowstheHeaderrecorddetailsfortheCNSDueBillActivityMROforAutoRouteID02040786:
AutoRoute [[ID]] 02040786
Header Record
Record Length = 220
Description Length Start End Type Comments
RecordType 1 1 1 A/N H
Title 44 2 45 A CNSDUEBILLACTIVITYMRO
ParticipantNumber 4 46 49 A/N Participantnumber
ProcessDate 10 50 59 A/N MM/DD/CCYY
SettlementDate 10 60 69 A/N MM/DD/CCYY
Filler 151 70 220 A/N Forfutureuse.
END OF RECORD
AutoRouteID02040786

---

## Page 3

[[CNS]]®DueBillActivityMRO:AutoRouteID02040786 3
DetailRecord
ThefollowingtableshowstheDetailrecorddetailsfortheCNSDueBillActivityMROforAutoRouteID02040786:
AutoRouteID02040786
DetailRecord
RecordLength=220
Description Length Start End Type Comments
RecordType 1 1 1 A/N l C=Cashpayment
l S=Stockpayment
l P=Spinoffstockpayment
SecurityNumber 9 2 10 A/N CUSIPissuingduebillorbondpayment.
WhenIssuedindicator 1 11 11 A/N WhenIssuedindicatorforissuingCUSIP
l 0=Regular
l 1=Whenissued
CUSIPDescription 30 12 41 A/N CUSIPdescription.
ActionSequenceNumber4 42 45 N Internaltrackingnumberforduebillorbondpayment.
ParticipantNumber 4 46 49 A/N Participantnumber
Sub-accounttype 1 50 50 A/N l A=RegularAccount
l C=StockBorrow
l D=DepositoryReceivable
l E=FullyPaidFor
l G=ReorgAccount#1
l H=ReorgAccount#2
l I–Z=Unassigned
Sub-accountName 23 51 73 A/N l TypeA=Blanks
l TypesC–H(Seeliteralnamesabove)
l TypesI–Z=Blanks
RateSequenceNumber 4 74 77 A/N Internaltrackingnumberforduebillorbondcomponent
rate.
PositionSequence
Number
4 78 81 A/N Internaltrackingnumberforeligibleposition.
AutoRouteID02040786

---

## Page 4

[[CNS]]®DueBillActivityMRO:AutoRouteID02040786 4
AutoRoute [[ID]] 02040786
Detail Record
Record Length = 220
Description Length Start End Type Comments
PositionQuantity 9 82 90 N Positiononwhichduebillorbondiscalculated.No
decimalplaces.
Ratio 9 91 99 N Rateappliedtopositiontodeterminepayment.
9999.99999
PaymentValue 17 100 116 N PositionQuantity*Rate.
999,999,999,999,999.99
[[Stock]]/spinoffpaymentsalwayswholenumbers.
Sign 1 117 117 A/N +or-=Definespaymentvalue.
ClosingPrice 12 118 129 A/N Usedforcashinlieucalculations.
999,999.999999
PayDate 8 130 137 A/N Payabledateofduebillorbond.
CCYYMMDD
Ex-DividendDate 8 138 145 A/N Ex-dividenddateofduebill.
CCYYMMDD
Spacesforbondpayment.
RecordDate 8 146 153 A/N RecordDateofduebillorbond.
CCYYMMDD
Remarks 35 154 188 A/N Descriptionofunusualpayments,suchaslate,or
reversals.
Currencyindicator 3 189 191 A/N Spaces=USD
Noothercurrentvalues.
Debit/CreditCode 1 192 192 A/N l D=Debit
l C=Credit
SpinoffCUSIP 9 193 201 A/N Forspinoffs,CUSIPofstockbeingpaid,otherwise
spaces.
SpinoffWhenIssued
Indicator
1 202 202 A/N WhenissuedindicatorforspinoffCUSIP.
l 0=Regular
l 1=Whenissued
l Otherwisespaces
DuebillIndicator 1 203 203 A/N D
AutoRouteID02040786

---

## Page 5

[[CNS]]®DueBillActivityMRO:AutoRouteID02040786 5
AutoRouteID02040786
DetailRecord
RecordLength=220
Description Length Start End Type Comments
CashinlieuIndicator 1 204 204 A/N Yindicatescashpaymentiscashinlieu.
Long/ShortIndicator 1 205 205 A/N Definesthepositionquantity.
l L=LongPosition
l S=ShortPosition
Filler 15 206 220 A/N Forfutureuse.
ENDOFRECORD
TrailerRecord
ThefollowingtableshowstheTrailerrecorddetailsfortheCNSDueBillActivityMROforAutoRouteID02040786:
AutoRouteID02040786
TrailerRecord
RecordLength=220
Description Length Start End Type Comments
RecordType 1 1 1 A/N T
Filler 44 2 45 A Spaces
ParticipantNumber 4 46 49 A/N Participantnumber
DetailCount 8 50 57 A/N Numberofdetailrecordssent.
99,999,999
Filler 163 58 220 A/N Forfutureuse.
ENDOFRECORD
AutoRouteID02040786

---

## Page 6

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, 
and the Interlocker graphic are registered and unregistered trademarks of The Depository Trust and Clearing 
Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository 
Trust and Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a 
separate legal entity, subject to the laws and regulations of the particular country or countries in which such entity 
operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Doc Info: August 18, 2022
Publication Code: CNS154
Service: [[CNS]]
Title: [[CNS]] Due Bill Activity MRO: AutoRoute [[ID]] 02040786
FOR MORE INFORMATION
Email [[DTCC]] Learning at:
corelearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com