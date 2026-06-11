---
title: "MBS Novation: MRO Samples"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs141_nov_mro_samples.pdf"
pages: 30
size: "412.6 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBS Novation: MRO Samples

**Original File:** [mbs141_nov_mro_samples.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs141_nov_mro_samples.pdf)  
**Category:** MBSD  
**Total Pages:** 30  
**File Size:** 412.6 KB  

---

## Page 1

 
FIXED INCOME CLEARING CORPORATION 
MBS [[Novation]]: MRO SAMPLES 
VERSION 1.03 
FEBRUARY 9, 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself 
does not provide such services.  Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
This document (the “Document”) is provided as a convenience to members and is for informational purposes only. The specific processes and services referenced in 
this Document are subject to the U.S. [[Securities and Exchange Commission]]’s approval of the Clearing Rules of the Mortgage- Backed [[securities]] Division (“MBSD”) of 
the Fixed Income  Clearing Corporation (“[[FICC]]”).  
This Document should not be regarded as a definitive or exhaustive description of [[FICC]]/MBSD’s services or risk -management framework; nor should it be regarded 
as a substitute for the Clearing Rules, which govern in all respects, the relationship between [[FICC]]/MBSD and its members. In all cases, members should refer to the 
Clearing Rules for a complete statement of [[FICC]]/MBSD procedures, [[obligations]], and requirements. Nothing in this Document shal l be deemed to impose any 
obliga tions on [[FICC]]/MBSD that are not set forth in the Clearing Rules, and in the case of any discrepancy between this Document and  the Clearing Rules, the 
Clearing Rules shall govern. The services and risk -management practices described in this Document may be amended at any time without prior notice.  
 
 
Doc Date: February 9, 2023 
Publication Code:  MBS141 
Service: Fixed Income Clearing Corporation 
Title: MBS [[Novation]] : MRO Samples 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................................................ 5 
1. Sample MROs ............................................................................................................................................................................... 6 
1.1 Pool Netting Detail............................................................................................................ 6 
1.2 Pool Netting Summary ...................................................................................................... 7 
1.3 Compressed Open Commitment ......................................................................................... 8 
1.4 Purchase & Sale ............................................................................................................ 10 
1.5 CCP Uncompared .......................................................................................................... 12 
1.6 CCP Pool Instruct Activity ................................................................................................ 13 
1.7 CCP Pool Obligation Activity ............................................................................................ 15 
1.8 CCP Compared Pool Instruct Status.................................................................................. 17 
1.9 CCP Pool Obligation Pending [[settlement]] / Status ............................................................... 18 
1.10 CCP Fail ....................................................................................................................... 19 
1.11 CCP Pool Instruct TAP Detail ........................................................................................... 20 
1.12  TBA Net D etail ............................................................................................................... 20 
1.13 Pool Conversion............................................................................................................. 22 
1.14 Expanded Pool Net Summary .......................................................................................... 23 
1.15 Expanded Pool Net Detail ................................................................................................ 24 
1.16 D NA Status ................................................................................................................... 25 
1.17 TBA Repric e and  Varianc e TAP........................................................................................ 26 
1.18 POID Facto r Upd ate ....................................................................................................... 27 
1.19 Cash Trade (Same Day Settle) Conversion ........................................................................ 27 

---

## Page 4

 
 
1.20 Split/Splice MRO ............................................................................................................ 29 
 

---

## Page 5

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  5 
VERSION CONTROL PAGE 
Date Version# Name Description of Change 
8/15/2016 1.0 MBSD Initial version.  
10/6/2016 1.01 MBSD Add note for CCP Uncompared, CCP Pool Instruct Activity and CCP Compared 
Pool Status to indicate that new fields (Trade Date and/or EPN Pool Reference 
Number) are only applicable for  [[Novation]] -eligible CUSIPs. 
3/30/2017 1.02 MBSD Section 2.6 TBA Reprice and Variance TAP, corrected report [[ID]] to MB8106 in 
card code 01 (was  erroneously listed as MB8107).  
7/20/2017 1.03 MBSD Updated Section 2.2 Pool Conversion and 2.8 Cash Trade (Same Day Settle) 
Conversion to reflect that POID resulting from generic  TBA does not provide 
Trade [[ID]]. In addition, in Cash Trade output, provide example where single PID 
mapped to multiple  trades and converted to POID.  
n/a n/a [[DTCC]] Learning  Updated formatting only. Content is unchanged.  
2/9/2023 1.03 MBSD Removed “Overview of MBS [[Novation]] ” section.  
 

---

## Page 6

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  6 
1. SAMPLE MROS 
1.1 Pool Netting Detail 
Purpose Reflect the results of the current day’s pool netting cycle in detail, including netting eligible and non netting eligible PI  Ds as well as resulting POIDs 
versus [[FICC]] @ syste m price.  
Layout Changes Content Changes  
None  This existing report show results of daily net, which includes all netting eligible PIDs  targeting TBA 
trades (TFTD/TBA and SBON), resulting in POIDs versus [[FICC]] @ system price.  
In addition to reflecting netting eligible PIDs and resulting POIDs as processed through the net 
algorithm (as done today), this output will include PIDs targeting these TBA trades, but not  netting 
eligible 1 (e.g. excluded from the net) along with resulti ng POIDs. 
Specifically:  
• Each non netting eligible PID processed will be reflected via Pool Instruct Detail Record (card 
Code 03) 
• Each resulting POID generated will be reflected via Pool Obligation Detail Record  (card Code 
04) 
 
The example below reflects a file generated for business date 7/28/2016. 
Header of Pool Net Detail 
01MB8008- N95001MBXX20160728 
For [[CUSIP]] 01F022477, 1 PID is included in net 
0201F022477BD22093140F9N351033437500000002016072900000000000064295C00000000000000000C 
0320160719201607290000016-072716 0000000000BXREF12345 
0000000002910960000000002910960000000000000000000000000000000000000000030055044000000000000000 
0400162100000147B2016071920160729FICC0000000002910960000000002910960000000000000000000000000000000000000000030119339000000000000000 
Trailer 
99 MBXX 0000002 0000004 
 
1 For example, PID targets trade with CSD in prior month, or late turn-around. 

---

## Page 7

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  7 
1.2 Pool Netting Summary 
Purpose Reflect the results of the current day’s pool netting cycle in summary, including netting eligible and non netting eligible P IDs. 
Layout Changes Content Changes  
Pool Instruct Detail Record (CC=02)  
Using space in “fille r” record, add:  
• Delivery Date 
This existing report show results of daily net in summary, which includes all 
netting eligible PIDs targeting TBA trades (TFTD/TBA and SBON).  
In addition to reflecting summary of netting eligible PIDs processed through the 
net algorithm (as done today) , this output will include PIDs targeting these TBA 
trades, but not  netting eligible 2 (e.g. excluded from the net).  
 
The example below reflects a file generated for business date 7/28/2016. 
Header of Pool Net Summary 
01MB8009-N11901MBGS20160728 
2 summary records 
0201F022477BD22093140F9N35000000000291096000000000291096000000000003011933900000000000000000000000000000000000000000000000000 
00000000291096C00000000029109600C00000000030119339D00000000000064295C20160729 
0201F022477BD22113140F9N50000000000708904000000000708904000000000007334941100000000000000000000000000000000000000000000000000
 00000000708904C00000000070890400C00000000073349411D00000000000156579C20160729 
Trailer 
99 MBGS 0000002 0000004 
  
 
2 For example, PID targets trade with CSD in prior month, or late turn-around. 

---

## Page 8

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  8 
1.3 Compressed Open Commitment 
Purpose Condensed listing of all open trades.  
Layout Changes Content Changes  
Modify Dealer Detail Record (CC=03)  
Using space in “filler” record, add:  
• Commission  
• Trade Sub-Type (for TFTD only, can be TBA, SPT or STIP)  
• Pool Number (for SPT only)  
• Original Trade Par  
 
Modify [[Broker]] Detail Record (CC=07)  
Using space in “filler” record, add:  
• Selling Dealer Commission  
• Buying Dealer Commission  
• Trade Sub-Type (for TFTD only, can be TBA, SPT or STIP)  
• Pool Number (for SPT only)  
• Original Trade Par  
Dealer Detail Record (CC=03)  
• Give-Up Date obsolete, will be blank  
• Contra will be FTBA, FSTP or FSTI upon [[Novation]], as appropriate  
• SBON will be vs. FTBA, @ system price and can be odd -lot 
• SPT can be FSET due to real -time cash SPT Conversion 3. If FSET, trade 
will not appear in following version.  
 
[[Broker]] Detail Record (CC=07)  
• Give-Up Date obsolete, will be blank  
• Trade Type can no longer be OPTN  
The example below reflects a file generated for business date 7/28/2016. 
Header of Compressed OCR 
01MB4891-A95001MBXXTEST DEALER 20160728P 
 
For [[CUSIP]] 01F022469, 1 TFTD/TBA 
0220160601F022469 MBXX FNMA SINGLE FAMILY 103406250000000 
0320160601F022469 MBXX5845702209XREF5593 FMATTFTDB201605252016060220160526 FTBA
 102476562500000000286657120000029375636270000000TBA 0002866571200 
0520160601F022469 MBXX 000286657120000029375636270000026650154C000000000000000000000000000000000000000C 
 
3 This only occurs when [[Member]] submit/match SPT with CSD<=today; it is immediately settled via SPTNOS and converted to POID.  This is 1st time FSET seen in AM Pass report, as NOS previously [[EOD]] event 
only. 

---

## Page 9

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  9 
For [[CUSIP]] 21H030666, 1 SBON, 1 SPT and 1 STIP 
0220160621H030666 MBXX GNMAII JUMBOS 104750000000000 
0320160621H030666 MBXX5870111234 PSETSBONB201606162016062120160616 FTBA 
103354166000000000015000000000001550312490000000  0000500000000 
0320160621H030666 MBXX5871245325XREF554 FMATTFTDB201606032016060720160603 FSPT 
  103916015625000000179273300000018638330710000000SPT MA37350001792733000 
0320160621H030666 MBXX5993817865XREF646 FMATTFTDS201606212016062220160621 FSTI  103843750  
000000000020000000000002076875000000000STIP  0000200000000 
0520160621H030666 MBXX 000194273300000020188643200000017044864C000020000000000002076875000000001812500D 
 
For [[CUSIP]] 01F032682, 1 SBOD with commission 
0220160801F032682 MBXX FNMA SINGLE FAMILY 105406250000000 
0320160801F032682 MBXX5892701220XREF201 FMATSBODS201607192016080020160719 FTBAMBZZ10539062500000000007000000000 
0007377343750109375 0000700000000 
0520160801F032682 MBXX 000000000000000000000000000000000000000C000070000000000007377343750000000109375D 
Report footer and trailer 
06 MBXX 000000000000000000000000000000000100007000000000000737734375000300048093042000004956427947000
 100002000000000000207687500000000000000000000000000000000000000000000000000000000000000 
99 MBXX 0000012 0000014 

---

## Page 10

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  10 
1.4 Purchase & Sale 
Purpose The Purchase and Sale Report serves as the sole binding confirmation of all matched trades. It also reports any subsequent activity associ ated with 
a trade i.e., [[Novation]], cancel, settle, etc. 
Layout Changes Content Changes  
Modify Dealer Detail Record (CC=03)  
Using space in “filler” record, add:  
• Trade Sub-Type (for TFTD only, can be TBA, SPT or STIP)  
• Pool Number (for SPT only)  
Dealer Detail Record (CC=03)  
• Activity Type GUP obsolete 
• Activity Type NOV is new, and reflects trade [[Novation]] 
• Activity Type RCRT is new,  and reflects a replacement trade generated due 
to the TBA Reprice process.  
• Give-Up Date obsolete, will be blank  
• Contra will be FTBA, FSPT  or FSTI upon [[Novation]], as appropriate after 
[[Novation]] 
• SBON will be vs. FTBA, @ system price and can be odd -lot 
• SPT can be FSET due to real -time SPT Conversion 4. 
 
[[settlement]] Record (CC=05)  
• Control Number/Internal XREF can be DNANOS, RPCNOS or SPTNOS 5 
• Pool Number will be equal to dummy NOS value (999999) for DNANOS and 
RPCNOS; will be equal to pool on SPT trade for SPT NOS. NOS due from 
STIP or non- net eligible PIDs will have FICCNOS as today.  
Notes: 
DNANOS and RPCNOS will appear in PM version only  
[[Broker]] Detail Record (CC=07)  
• Give-Up Date obsolete, will be blank  
• Trade Type can no longer be OPTN  
 
 
4 This only occurs when [[Member]] submit/match SPT with CSD<=today; it is immediately settled via SPTNOS and converted to POID. This is 1st time FSET seen in AM Pass report, as NOS previously [[EOD]] event 
only. 
5 As [[Member]] can no longer submit external NOS, control number values will only be FICCNOS, DNANOS, RPCNOS or SPTNOS. 

---

## Page 11

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  11 
The example below reflects a file generated for business date 4/12/2016. 
Header of Purchase & Sale 
01MB4761-A95001MBXXTEST DEALER 20160412P 
[[CUSIP]] Header for 02R080645 
0220160402R080645 MBXX FHLMC GOLD SINGLE FAMILY 
Below reflects the [[settlement]] of a TFTD/TBA (via DNA NOS) due to DNA [[settlement]] 
0320160402R080645 MBXX5665702116NOS CSSTEST2A TFTD S201604112016041220160413 20160411FTBA
 0000000FSET10014257812500010014257812500000010000000000000000000000TBA 
0520160402R080645 MBXX56657021169999999 0001000000000DNANOS 20160412 
Below reflects the [[settlement]] of a TFTD/TBA (via [[FICC]] NOS) due to 2 pool allocations, and remaining position repriced (original trade fully settled via 
reprice NOS; replacement TBA trade created) 
0320160402R080645 MBXX5665702121NOS CSSTEST4 TFTD B201604112016041220160413 20160411FTBA 
0000000FSET09997656250000009997656250000000010000001330000000000000TBA 
0520160402R080645 MBXX56657021210DH0002 0000200000617FICCNOS 20160412 
0520160402R080645 MBXX56657021210DH0003 0000299999516FICCNOS 20160412 
0520160402R080645 MBXX56657021219999999 0000500000000RPCNOS  20160412 
0320160402R080645 MBXX5666800405RCRT CSSTEST4 TFTD B201604112016041120160413 20160412FTBA 
0000000FMAT11621875000000011621875000000000005000000000000581093750TBA 
Below reflects the [[settlement]] of a SPT trade (via SPT NOS) when it is converted to an obligation 
0320160402R080645 MBXX5666700119NOS CSSTS3A TFTD S201604122016041220160413 20160412FSPT 
0000000FSET10048828125000010048828125000000015123535000000000000000SPT 0DH0001 
0520160402R080645 MBXX56667001190DH0001   0001512353500SPTNOS  20160412 
Below reflects the [[settlement]] of a STIP trade (via [[FICC]] NOS) due to pool allocation 
0320160402R080645 MBXX5666700124NOS CSSTS6B TFTD S201604122016041220160413 20160412 FSTI 
0000000PSET10000781250000010000781250000000005000020600000500039063STIP 
0520160402R080645 MBXX56667001240DH0003 0000500002060FICCNOS 20160412 
Below reflects [[Novation]] of a SBOD trade (with [[Broker]] commission) 
0320160402R080645 MBXX5897615769NOV CSS618 SBOD S201604112016041220160400 20160412 
FTBAMBZZ0097656FMAT10530664062500010530859375000000050000000000005265429688 
Trailer 
99 MBXX 0000013 0000015 

---

## Page 12

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  12 
1.5 CCP Uncompared 
Purpose Reflect uncompared pool submissions.  
Layout Changes Content Changes  
Uncompared Pool Submission Detail Record (CC=02)  
Using space in “filler” record, add:  
• Trade Date 
This existing output shows pool instructs submitted by members that did not 
bilaterally match against an advisory. Previously, this output reflected the DK 
code on any [[Member]] instructs that were DKed by the counterparty; as all 
instructs are now versus [[FICC]], this DK code field is obsolete and will no longe r 
be used (e.g. will always have value “NONE”).  
Notes: 
The terms for bilateral match have been expanded to include Trade Date.  
Notes: 
The Trade Date is only applicable for [[Novation]] -eligible CUSIPs; it will always be 
blank for PIDs with non- [[Novation]]- eligible CUSIPs. 
The example below reflects a file generated for business date 7/28/2016. 
Header of CCP Uncompared 
01MB8001-N95001MBXX20160728 
2 Pool Instructs canceled, one by [[Member]] and one by system 
0220160701F022477BD28513140FAEZ1CANCCANCBXREFCSS005 0000033-072716 
20160727201607192016080155501FSTI00000000015000000000000015000000103122876000000000000015487181N NNONE 20160718 
0220160701F030470BA28823140E7FY1SCANCANCSXREFCSS104 0000101-072616 
20160726201607192016072955501FTBA00000000003426800000000003166720104389138000000000000003310462N NNONE 20160718 
3 Pool Instructs remain uncompared 
0220160701F030470BA69363140EBV65UNCPUNCPBXREFCSS21 0000056-072816 
20160728201607192016080155501FTBA00000000060011600000000056252836104898437500000000000059092725N YNONE 20160715 
0220160702R040672Q338423132QQHU9UNCPUNCPBXREFCSS95 0000178-072716 
20160727201607142016080155501FSTI00000000069114800000000057548603107018188000000000000061670598N NNONE 20160712 
0220160702R040672Q351253132QRVT4UNCPUNCPBXREFCSS35 0000029-072716 
20160727201607142016080155501FTBA00000000038418100000000028640825107018188000000000000030692262N YNONE 20160713 
Trailer 
99 MBXX 0000005 0000007 

---

## Page 13

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  13 
1.6 CCP Pool Instruct Activity 
Purpose Reflects newly compared Pool Instructs and all subsequent updates.  
Layout Changes Content Changes  
Pool Instruct Activity Item Detail Record (CC=02)  
Using space in “filler” record, add:  
• Trade Date 
• EPN Pool Reference Number  
Pool Instruct Activity Item Detail Record (CC=02)  
New Activity Codes, as follows: 
• FCMP - Force compare [[Member]] advisory  
• MFYD – Delivery date change 
• PNCV – Non netting eligible PID converted to POID  
• PDCV – STIP PID converted to POID  
Following codes no longer used:  
• XNET – PID excluded from netting 
Notes: 
The Trade Date and EPN Pool Reference Number are only applicable for 
[[Novation]]-  eligible CUSIPs; they will always be blank for PIDs with non -[[Novation]]-
eligible CUSIPs.  
The example below reflects a file generated for business date 7/28/2016. 
Header for Pool Instruct Activity 
01MB8004-N95001MBXX20160728 
Below represents a PID that is force compared today and then included in the pool net. Note [[Member]] supplied EPN pool reference number on 
corresponding allocation. 
0220160701F022477BD22093140F9N35FCMPCOMP0016072700000011S0000090-072816 0000312-072816 
016072820160728201607192016072955501FTBA00000000029109600000000029109600103122876000000000000030055044N N 20160714EPNX548 
0220160701F022477BD22093140F9N35NET  CANC0016072700000011S0000090-072816 0000312-072816 
2016072820160728201607192016072955501FTBA00000000029109600000000029109600103122876000000000000030055044N N 20160714EPNX548 
Below represents a PID that is force-compared today, with no EPN pool reference number supplied by [[Member]] 
0220160701F030470AZ04613138YRQP6FCMPCOMP0016072700000028S0000091-072816 0000058-072716 
2016072820160728201607192016073055501FSTI00000000086524700000000072739039104898437500000000000076411224N N 20160714 

---

## Page 14

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  14 
Below represents a PID that is not net-eligible and therefore directly converted to a Pool Obligation 
0220160701F030470BA69363140EBV65PNCVCANC0016072700000030SXREF0554 0000053 -072716 
2016072720160727201607192016072955501FTBA00000000009567500000000008968250104898437500000000000009421006N N20160714EPNX133 
Below represents a STIP PID that is bilaterally-compared by [[Member]] and then converted to a Pool Obligation 
0220160701N04267478320236241LRX6COMPCOMP0016072800000019SXREF00021 0000319-072816 
2016072820160728201607202016072955501FSTI00000000089702500000000025999998110017514000000000000028666301N N 20160713EPNX765 
0220160701N04267478320236241LRX6PDCVCANC0016072800000019SXREF00021 0000319-072816 
2016072820160728201607202016072955501FSTI00000000089702500000000025999998110017514000000000000028666301N N 20160713EPNX765 
Below represents PID whose delivery date is changed post-comparison (at [[Member]] request) 
0220160701N042674AD494736180GP87MDADCOMP0016072800000015B0000035-072616 0000711-072616
 2016072620160726201607202016073055501FTBA00000000074000000000000074000000109937500000000000000081529500N N 20160715EPNX004 
Trailer 
99 MBXX 0000007 0000009 

---

## Page 15

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  15 
1.7 CCP Pool Obligation Activity 
Purpose Reflects newly compared Pool Instructs and all subsequent updates.  
Layout Changes Content Changes  
Pool Obligation Activity Item Detail Record (CC=02)  
Using space in “filler” record, add:  
• Trade Date 
Pool Obligation Activity Item Detail Record (CC=02)  
New Activity Codes, as follows: 
• PNCV – POID generated from conversion of non netting eligible PID  
• PDCV – POID generated from conversion of STIP PID  
• STCV – POID generated from conversion of SPT PID 
• CXFC – POID cancel via factor update 
• REFC – Replacement POID via factor update 
• CXDK – POID cancel due to DK of CC  
• REDK – Original POID restored due to DK of CC  
The Trade Date field is new and will be populated differently based on [[FICC]] 
account:  
• FSTP (SPT trades): Trade Date will reflect the associated SPT trade date 
• FSTI (STIP allocations): Trade Date will reflect the associated STIP trade 
date. 
• [[FICC]] (generic TBA trade allocations): Trade Date will be blank  
The example below reflects a file generated for business date 7/28/2016. 
Header for Pool Obligation Activity 
01MB8005-N12601MBXX20160728 
Below reflects a POID generated from conversion of non-netting eligible PID 
0220160701F022477BD22093140F9N35PNCVRND 
00162100000157S2016071920160729FICC00000000029109600000000029109600103343750000000000000030119339000000000000000000000000014641D 
Below reflects a POID generated from conversion of STIP PID 
0220160701F022477BD22113140F9N50PDCVRND 
00162100000159S2016071920160729FSTI00000000070890400000000070890400103343750000000000000073349411000000000000000000000000035656D20160715 
Below reflects a POID generated from conversion of SPT trade 
0220160701F030470AZ04613138YRQP6STCVRND 
00162100000208S2016072920160729FSPT00000000086524700000000072739039104750000000000000000076303252000000000000000000000000037092D20160727 

---

## Page 16

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  16 
Below reflects a STIP CC that was DK'ed, and therefore the replacement pool canceled and original pool restored. 
0220160701F030470BA69363140EBV65CXDKCANC 
00162000000451S2016071920160801FSTI00000000015887900000000014892778104781250000000000000015627178000000000000000000000000000000D20160715 
0220160701F030470BC49433140F0P57REDKRND 
00162100015340S2016071920160729FSTI00000000016178800000000014892796104781250000000000000015627197000000000000000000000000007597D20160715 
Trailer 
99 MBXX 0000005 0000007 
The example below reflects a file generated for business date 7/6/2016. 
Header for Pool Obligation Activity 
01MB8005-N12601MBXX20160706 
Below reflects a POID that has [[settlement]] date in blackout period, and therefore canceled / replaced when new factor is received 
0220160701F030470AZ04613138YRQP6CXFCCANC 
00162100000204S2016070420160706FICC00000000086524700000000072739039104750000000000000000076212328000000000000000000000000000000D 
0220160701F030470AZ04613138YRQP6REFCRND 
00170000000203S2016070420160707FICC00000000086524700000000072561038104750000000000000000076025872000000000000000000000000011087D 
Trailer 
99 MBXX 0000002 0000004 

---

## Page 17

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  17 
1.8 CCP Compared Pool Instruct Status 
Purpose Reflect all Pool Instruct positions and their current state.  
Layout Changes Content Changes  
Compared Pool Instruct Detail Record (CC=02)  
Using space in “filler” record, add:  
• Trade Date 
• EPN Pool Reference Number  
This existing output shows a [[Member]]’s compared pool instructs, and will now 
reflect the Trade Date, which has been added as a matching term.  
Notes: 
The Trade Date and EPN Poo l Reference Number are only applicable for 
[[Novation]]-  eligible CUSIPs; they will always be blank for PIDs with non -[[Novation]]-
eligible CUSIPs.  
The example below reflects a file generated for business date 7/28/2016. 
Header for Compared Pool Instruct Status 
01MB8006-N95001MBXX20160728 
3 compared PIDs, 2 with EPNX and one without 
0220160701F030470AZ04613138YRQP6104750000000COMP0016072700000023S0000091-072716 0000078-072716 
2016072720160727201607192016080155501FTBA00000000086524700000000072739039104389138000000000000076040764N  Y  20160714EPNX555 
0220160701F030470BA59613140EATT0104750000000COMP0016072800000055S0000157-072816 0000088-072816 
2016072820160728201607192016080155501FTBA  00000000045108900000000043737212104389138000000000000045722504N  Y  201607141134EX 
0220160701F030470BA69363140EBV65104750000000COMP0016072700000076BXREF1134TG 0000102 -072716
 2016072720160727201607192016080155501FTBA00000000009567500000000008968250104389138000000000000009375331N Y  20160714 
Trailer 
99 MBXX 0000003 0000005 
  

---

## Page 18

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  18 
1.9 CCP Pool Obligation Pending [[settlement]] / Status 
Purpose Reflect all pool [[obligations]] that are pending [[settlement]], settled or canceled on the current business day.  
Layout Changes Content Changes  
Pool Obligation Pending [[settlement]] Detail Record (CC=02)  
Using space in “filler” record, add:  
• Trade Date 
This existing output shows pool [[obligations]] pending [[settlement]], including those 
generated from pool netting, SPT trade conversion and STIP allocations.  
 
The Trade Date field is new and will be populated differently based on [[FICC]] 
account:  
• FSTP (SPT tra des): Trade Date will reflect the associated SPT trade date 
• FSTI (STIP allocations): Trade Date will reflect the associated STIP trade 
date. 
• [[FICC]] (generic TBA trade allocations): Trade Date will be blank.  
The example below reflects a file generated for business date 7/28/2016. 
Header of CCP Pool Obligation Pending [[settlement]] / Status 
01MB8010-N95001MBXX20160728 
3 [[obligations]] pending [[settlement]], a generic TBA, STIP and SPT 
0220160601F042665AV33593138XEWV6108937500000000RND   
00161130000034S2016061320160728FICC000000001540436000000000829999721091875 00000000000000090750094000000000427464D 
0220160601N042666AP399636188RNM6109812500000000RND   
00161790000091B2016062120160728FSTI00000000003790200000000003748501110000000000000000000004132722000000000019204C  20160615 
0220160701F022477AB598231417CUG8103406250000000RND   
00161070000112B2016071920160728FSPT00000000271941900000000099999977103468750000000000000103593726000000000000000C  20160713 
1 canceled obligation, a generic TBA 
0220160701F042673AS36543138WDBY6108937500000000CANC00161230026143S2016071420160728FICC000000000351887000000000175660671090000000000000000
00019175558000000000000000C 
1 settled obligation, a STIP 
0220160702R040672Q351253132QRVT4106875000000000SETT00161020000033B2016071420160728FSTI000000000699827000000000521723421069062500000000000
00055850854000000000000000C  20160711 

---

## Page 19

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  19 
Trailer 
99 MBXX 0000005 0000007 
1.10 CCP Fail 
Purpose Reflect all failing pool clearance [[obligations]] versus [[FICC]] (delivery date = report date)  
Layout Changes Content Changes  
Pool Obligation Fail Detail Record (CC=02)  
Using space in “filler” record, add:  
• Trade Date 
This existing output shows pool [[obligations]] with delivery date = today, but 
failed to settle.  
 
The Trade Date field is new and will be populated differently based on [[FICC]] 
account:  
• FSTP (SPT trades): Trade Date will reflect the associated SPT trade date 
• FSTI (STIP allocations): Trade Date will reflect the associated STIP trade 
date. 
• [[FICC]] (generic TBA trade allocations): Trade Date will be blank.  
 
The example below reflects a file generated for business date 7/28/2016. 
Header of CCP Fail 
01MB8011-N195001MBXX20160728 
3 failing [[obligations]]; a generic TBA, a SPT and a STIP 
0220160621H040665MA324536179RTA7RND  
00161740000907B2016062120160728FICC00000000110595900000000100000085106640620000000000000106862933000000004350760C000000000197399C 
0220160701F032674AS42133138WDVF5RND  
00161960000501S2016071420160728FSPT00000000015216200000000011902307105609370000000000000012584994000000000000000C000000000009177D20160712 
0220160701F032674BC27493140EXBT9RND  
00161970000543S2016071420160728FSTI00000000020198800000000019999727105484370000000000000021121863000000000000000C000000000015401D20160711 
Trailer 
99 MBXX 0000003 0000005 
  

---

## Page 20

MBS [[Novation]]: MRO Samples 
Version C ontrol Page  20 
1.11 CCP Pool Instruct TAP Detail 
Purpose Reflect all compared Pool Instructs processed in the current business day’s Pool Netting cycle and the associated Transaction Adjustment Payment 
for each individual Pool Instruct.  
Layout Changes Content Changes  
None  This existing report show netting eligible PIDs processed through the daily net, 
along with associated pool TAP.  
 
In addition to reflecting netting eligible PIDs (as done today), this output will 
now include the following:  
 
• PIDs processed through the daily net, but not netting eligible  
• PIDs, regardless of netting eligibility, processed through the Expanded Pool 
Net (on SIFMA 24hr day only)  
All of these PIDs result in POIDs @ system price and therefore have 
associated TAP.  
Each PID above will be reflected via Pool Instruct TAP Detail Record (CC=02).  
 
The example below reflects a file generated for business date 7/19/2016. 
Header of CCP Pool Instruct TAP Detail 
01MB8013-N95001MBXX20160719 
2 PIDs processed in netting cycles on current business day 
0220160701F022477BD22093140F9N35201607200000010-071916   XREF1 
B55501FTBA00000000029109600000000029109600103122876000000000000000300550441033437500000000000000003011933900000000000064295C 
0220160701F022477BD22113140F9N50201607210000011-071916   XREF2 
B55501FTBA00000000070890400000000070890400103122876000000000000000731928321033437500000000000000007334941100000000000156579C 
Trailer 
99 MBXX 0000002 0000004 
1.12  TBA Net Detail 

---

## Page 21

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  21 
Purpose Display details about TBA Net – including SBOD trades included in the SBO process along with corresponding TBA TAP, and resulting SBON 
[[obligations]] versus FTB A @  system price.  
 
The example below reflects a file generated for business date 4/13/2016 (72 hr day) 
Header of TBA Net Detail 
01MB8101-N95001MBXXTEST DEALER 20160413 
SBOD trades included in net 
0201F082646MBXX5667700354XREF000001 
SBODS20160413201604FTBA0005000000000100664062500000000503320312511596875000000000057984375000000765234375D 
0201F082646MBXX5667700356XREF000002 
SBODS20160413201604FTBA0001000000000100625000000000000100625000011596875000000000011596875000000153437500D 
0201F082646MBXX5667700358XREF000003 
SBODS20160413201604FTBA0001000000000100585937500000000100585937511596875000000000011596875000000153828125D 
0201F082646MBXX5667700360XREF000004 
SBODS20160413201604FTBA0004000000000100546875000000000402187500011596875000000000046387500000000616875000D 
0201F082646MBXX5667700361XREF000005 
SBODB20160413201604FTBA0005000000000100507812500000000502539062511596875000000000057984375000000773046875C 
0201N022445MBXX5665700266XREF000006 
SBODB20160411201604FTBA0000099999900100125000000000000010012490010284375000000000001028436470000002718747C 
0201N022445MBXX5665700268XREF000007 
SBODB20160411201604FTBA0000000100000100125000000000000000010012510284375000000000000001028440000000002719C 
0201N022445MBXX5665700270XREF000008 
SBODB20160411201604FTBA0001000000000100125000000000000100125000010284375000000000010284375000000027187500C 
0201N022445MBXX5665700272XREF000009 
SBODB20160411201604FTBA0000100000000100125000000000000010012500010284375000000000001028437500000002718750C 
0201N022445MBXX5665700274XREF000010 
SBODB20160411201604FTBA0000100000000099000000000000000009900000010284375000000000001028437500000003843750C 
0201N022445MBXX5665700276XREF000011 
SBODB20160411201604FTBA0000300000000099000000000000000029700000010284375000000000003085312500000011531250C 
0201N022445MBXX5665700278XREF000012 
SBODS20160411201604FTBA0000180000000099125000000000000017842500010284375000000000001851187500000006693750D 
0201N022445MBXX5665700280XREF000013 
SBODS20160411201604FTBA0000050000000098125000000000000004906250010284375000000000000514218750000002359375D 
0202R082641MBXX566770037511TC142A 
SBODB20160413201604FTBA0005000000000100156250000000000500781250011643750000000000058218750000000814062500C 
0202R082641MBXX566770037811TC142B 
SBODS20160413201604FTBA0004000000000100234375000000000400937500011643750000000000046575000000000648125000D 

---

## Page 22

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  22 
0202R082641MBXX566770038011TC142C 
SBODS20160413201604FTBA0001000000000100273437500000000100273437511643750000000000011643750000000161 640625D 
0202R082641MBXX566770038211TC142D 
SBODS20160413201604FTBA0001000000000100312500000000000100312500011643750000000000011643750000000161250000D 
0202R082641MBXX566770038411TC142E 
SBODS20160413201604FTBA0005000000000100351562500000000501757812511643750000000000058218750000000804296875D 
Resulting SBON [[obligations]] vs FTBA 
0301F082646MBXX5667403602SBONS2016041320160418FTBA00060000000001159687500000000006958125000 
0301N022445MBXX5667403575SBONB2016041320160418FTBA00013000000001028437500000000001336968750 
0301N022445MBXX5667403608SBONB2016041320160418FTBA00000701099001028437500000000000072103650 
0302R082641MBXX5667403603SBONS2016041320160418FTBA00060000000001164375000000000006986250000 
Trailer 
99 MBXX 0000022 0000024 
1.13 Pool Conversion 
Purpose Reflect SPT and allocations (STIP and generic TBA) converted to POIDs @ trade execution price on the current business day.  
The example below reflects a file generated for business date 4/12/2016. 
Header of Pool Conversion, business date 4/12/2016 
01MB8102-N95001MBXXTEST DEALER 20160412 
2 SPT trades converted to Pool [[obligations]] 
0202R080645MBXX5666700162XERF143A TFTDSPT 
S2016041220160413FSPTA591263128KND7510054687500000000000000300000000000000270000000000000272196563C 
0402R080645MBXX00161030001997 5666700162S201604122016041320160413FSPTA591263128KND7510054687500000000000000300
 000000000000270000000000000272196563C 
0202R080645MBXX5666700119XREF93A TFTDSPT 
S2016041220160413FSPTDH000131295DHT010048828125000000000003500000000000001512353500000001523770981C 
0402R080645MBXX00161030001985  5666700119S201604122016041320160413FSPTDH000131295DHT010 
    048828125000000000003500000000000001512353500000001523770981C 
STIP PID converted to Pool Obligation 
0302R080645MBXX000001215-0412165666700124T5ISSS7P061865 
TFTDSTIPS201604122016041320160413FSTIDH000331295DHB910000781250000000000000726800000000000500002060000000501374461C 

---

## Page 23

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  23 
0402R080645MBXX00161030001791000001215-
0412165666700124S201604122016041320160413FSTIDH000331295DHB910000781250000000000000726800000000000500002060000000501374461C 
Generic PID converted to Pool Obligation (only applicable for PIDs with non-SIFMA CSD, booked via [[FICC]] operations with delivery date = next 
business day after daily pool net cycle ran) 
0302R080645MBXX000001215-0412175666700125T5ISSS7P061865 TFTDTBA 
S201604122016041320160413FTBADH000331295DHB910000781250000000000000726800000000000500002060000000501374461C 
0402R080645MBXX00161030001791000001215-041217 
S201604122016041320160413FICCDH000331295DHB910000781250000000000000726800000000000500002060000000501374461C 
Trailer 
99 MBXX 0000008 0000010 
1.14 Expanded Pool Net Summary 
Purpose Reflects the summary results of the current day’s expanded pool netting cycle, run as part of DNA/Reprice.  
The example below reflects a file generated for business date 7/19/2016 (SIFMA CSD-1) 
Header of Expanded Pool Net Summary 
01MB8105-N95001MBXX20160719 
3 Pool Netting summary records 
0201F030470AS59793138WFUD6000000000000000000000000000000000000000000000000000000000009838400000000008219961000000000086227390 
00000000098384D00000000008219961D00000000008622739C00000000000029663D20160721 
0201F030470AZ04613138YRQP6000000000865247000000000727390390000000007630325200000000000000000000000000000000000000000000000000 
00000000865247C00000000072739039C00000000076303252D00000000000107972D20160721 
0201F030470BA69363140EBV65000000000000000000000000000000000000000000000000000000000083162500000000077953703000000000817734340000000008316
25D00000000077953703D00000000081773434C00000000000326980D20160722 
Trailer 
99 MBXX 0000003 0000005 

---

## Page 24

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  24 
1.15 Expanded Pool Net Detail 
Purpose Reflects the detailed results of the current day’s expanded pool netting cycle, run as part of DNA/Reprice.  
 
The example below reflects a file generated for business date 7/19/2016 (SIFMA CSD-1) 
Header of Expanded Pool Net Detail 
01MB8104-N95001MBXX20160719 
For Pool [[CUSIP]] 36241LRX6, 2 Pool Instructs net flat; no resulting Pool [[obligations]] 
0201N04267478320236241LRX61098125000000002016072100000000000037053D00000000000000000C 
0320160720201607210000045-071916  0000000000BXREF8104A 
0000000008970250000000002599999800000000000000000000000000000000000000028666301000000000000000 
0320160720201607210000341-071916  0000000000SXREF8104B 
0000000000000000000000000000000000000000089702500000000025999998000000000000000000000028629248 
For [[CUSIP]] 3622A2T51, 2 Pool Instructs are netted and result in 2 Pool [[obligations]] vs [[FICC]] 
0201N0426747841723622A2T511098125000000002016072200000000000518259C00000000000000000C 
0320160720201607220000098-071916  0000000000BXREFJX601 
0000000002630630000000002591711800000000000000000000000000000000000000028181626000000000000000 
0320160720201607220000099-071916  0000000000BXREFJX602 
0000000001377310000000001356933700000000000000000000000000000000000000014754958000000000000000 
0400162100000193B2016072020160722FICC0000000001377310000000001356933700000000000000000000000000000000000000014933055000000000000000 
0400162100000191B2016072020160722FICC0000000002630630000000002591711800000000000000000000000000000000000000028521788000000000000000 
Trailer 
99 MBXX 0000008 0000010 

---

## Page 25

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  25 
1.16 DNA Status 
Purpose To capture the DNA requests sent by members. This report will allow members to track their DNA activity and reconcile money differences 
generated by the pair offs.  
 
The example below reflects a file generated for business date 4/12/2016 (SIFMA CSD-1) 
Header of DNA Status 
01MB8103-N95001MBXXTEST DEALER 20160412 
Below DNA, which was assigned to 3 trades (2 sell and 1 buy), was settled 
0202R080645MBXX5665001806DHDNA2 20160413STLD00000000000673828C 
0302R080645MBXX5665001806DHDNA2 5665702116TFTDS20160411201604131001425781250000000000100000000000000001000000000000001001425781 
0302R080645MBXX5665001806DHDNA2 5665702122TFTDS20160411201604130999375000000000000000075000000000000000500000000000000499687500 
0302R080645MBXX5665001806DHDNA2 5665702119SBONB20160411201604131000292968750000000000200000000000000001500000000000001500439453 
Below DNA, which was assigned to 2 trades (1 sell and 1 buy), was canceled 
0202R080645MBXX5665001807DHDNA3 20160413CANC00000000000390625C 
0302R080645MBXX5665001807DHDNA3 5665702115TFTDS20160411201604131001074218750000000000050000000000000000500000000000000500537109 
0302R080645MBXX5665001807DHDNA3 5665702119SBONB20160411201604131000292968750000000000200000000000000000500000000000000500146484 
Trailer 
99 MBXX 0000007 0000009 
  

---

## Page 26

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  26 
1.17 TBA Reprice and Variance TAP 
Purpose Capture the TBA trade reprice activity occurring on the current business day. This report will allow members to reconcile this reprice activity and  
any associated money differences.  
In addition, capture cash differences associated with allocation variance, allowing members to r econcile these money differences.  
 
The example below reflects a file generated for business date 4/12/2016 
Header of TBA Reprice and Variance TAP 
01MB8106-N95001MBXXTEST DEALER 20160412 
3 trades below were repriced. Note: 1st two were also allocated and as such, have variance TAP (see below). 
0201F030652MBXXAB88261079RATJTSRJH SBON 
B2016040620160413FTBA101250000000000000120000000000012150000005666700650110906250000000000133087500000000000115875000C 
0202R080645MBXX5665702115DHTEST1 TFTDTBA 
S2016041120160413FTBA10010742187500000005000000000000500537109566670045411621  8750000000000058109380000000000080556641D 
0202R080645MBXX5665702122DHTEST5A TFTDTBA 
S2016041120160413FTBA099937500000000000020000000000001998750005666700417116218750000000000023243750000000000032562500D 
4 trades below had pools allocated and as such, have associated variance TAP. Note: 1st two were also repriced (see above) 
0301F050643MBXX5662701079RATJTSRJH SBON  B2016040620160413FTBA1012500000000000000000052160U110906250000000000000000000 05037C 
0302R080645MBXX5665702115DHTEST1 TFTDTBA  S2016041120160413FTBA1001074218750000000000027150O11621875000000000000000000004374C 
0302R080645MBXX5669000214DHMRO1B TFTDTBA  B2016041220160413FTBA1000722656250000000000059230O116218750000000000000000000 09564D 
0302R080645MBXX5669000217DHMRO1C TFTDTBA  S2016041220160413FTBA1004687500000000000000013858O116218750000000000000000000 02183C 
Trailer 
99 MBXX 0000007 0000009 
  

---

## Page 27

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  27 
1.18 POID Factor Update 
Purpose Capture cash differences due to factor updates for POIDs that already settled and have CSD in blackout period. This report wi ll allow members to 
reconcile the money differences based on the factor updates  
 
The example below reflects a file generated for business date 5/6/2015 
Header of POID Factor Update 
01MB8107-N95001MBXXTEST DEALER 20160412 
2 [[obligations]] have factor updated 
0201F030652MBXXAB882631417FYY8141290025807 
B201505032015050320160503FICC000000002059671000000002049372651030000000000000000002111195390009950000000009946770000000000020487073700000
0211051004000000000068535C 
0201F030652MBXXAB882631417FYY8141290025549 
B201505032015050320160504FSPT000000001000000000000000995000000991250000000000000000986459580009950000000009946770000000000009946770000000
0098613936000000000032022C 
Trailer 
99 MBXX 0000002 0000004 
1.19 Cash Trade (Same Day Settle) Conversion 
Purpose Provide details on cash trades (SPT and allocations)  converted to POIDs on real -time basis. 
 
The example below reflects a file generated for business date 4/12/2016 
Header of TBA Reprice and Variance TAP 
01MB8108-N95001MBXXTEST DEALER 20160412 
Same day generic PID converted to POID, where PID assigned to single trade 
0301F050544MBXX000003015-0411165665701277XREF123456 
TFTDTBA  B201604112016041220160412FTBA25473331371K4S7105115000000000000000001000000000000000998 22056000000105080460C 
0401F050544MBXX00161030001890000003015-041116
 B201604112016041220160412FTBA25473331371K4S710511500000000000000000100000000000000099822056000000105080460C 

---

## Page 28

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  28 
Same day generic PID converted to POID, where PID assigned to multiple trades 
0301F050544MBXX000003020-0411165665712345XREF1A TFTDTBA 
B201604112016041220160412FTBA25473331371K4S710511500000000000000000050000000000000049911028000000052540230C 
0301F050544MBXX000003020-0411165665745678XREF1B TFTDTBA 
B201604112016041220160412FTBA25473331371K4S710511500000000000000000050000000000000049911028000000052540230C 
0401F050544MBXX00161030001890000003015-041116
 B201604112016041220160412FTBA25473331371K4S710511500000000000000000100000000000000099822056000000105080460C 
“as-of” SPT with CSD=4/8/2016 converted to single POID 
0202R080645MBXX5008891162DHMRO467 TFTDSPT 
B2016040720160408FSPTA591263128KND7510054687500000000000000300000000000000270000000000000271896563D 
0402R080645MBXX00161030001997
 5008891162B201604072016040820160413FSPTA591263128KND7510054687500000000000000300000000000000270000000000000271896563D 
SPT with CSD=next business day converted to 2 POIDs (this SPT was submitted and matched after 4:30pm cutoff) 
0202R080645MBXX5666700120DHMRO56 TFTDSPT 
S2016041220160413FSPTDH000131295DHT010048828125000000000008000872500000007734443446000007772929283C 
0402R080645MBXX001610300019865666700120S201604122016041320160413FSPTDH000131295DHT0100488281250000000000050000000000000048335000000000048
57821074C 
0402R080645MBXX00161030001987  5666700120S201604122016041320160413 
FSPTDH000131295DHT010048828125000000000003000872500000002900943446000002915828209C 
Same day STIP PID converted to POID 
0302R080645MBXX000001215-0412165666700124XREFSTIP061865 
TFTDSTIPS201604102016041220160412FSTIDH000331295DHB9100007812500000000000007268000000000005000 02060000000501263350C 
0402R080645MBXX00161030001890000001215-
0412165666700124S201604102016041220160412FSTIDH000331295DHB910000781250000000000000726800000000000500002060000000501 263350C 
Trailer 
99 MBXX 00000012 0000014 

---

## Page 29

MBS [[Novation]]: MRO Samples  
Version C ontrol Page  29 
1.20 Split/Splice MRO 
Purpose This output identifies dealer trades matched as a result of Net Position match (a.k.a. Net Position Match), allowing members to reconcile this  activity.  
The example below reflects a file generated for business date 4/12/2016. 
Header for Split/Splice 
01MB8109-N95001MBXXTEST DEALER 20160412 
Below represents a split, where 1 trade is split into two trades. Note 1 resulting trade is fully matched, and one partially matched. 
0201F022477MBXX0000000000700915SPCX1930705681XREF001 SBODB201604122016041220160401 MBZZ1037109375000000005000000000 
0201F022477MBXX0000000000700915SPCR5883700901XREF001 SBODB201604122016041220160401FMATMBZZ1037109375000000003400000000 
0201F022477MBXX0000000000700915SPCR5883700902XREF001 SBODB201604122016041220160401PMATMBZZ1037109375000000001600000000 
Below represents a split/splice combo, where 2 trades are combined and split into 2 resulting trades of different sizes 
0201F030488MBXX0000000000705407SPCX1930755098XREF002 SBODB201604122016041220160401 MBZZ1049179687500000006000000000 
0201F030488MBXX0000000000705407SPCX1930890012XREF003 SBODB201604122016041220160401 MBZZ1049179687500000004000000000 
0201F030488MBXX0000000000705407SPCR5883700956 SBODB201604122016041220160401PMATMBZZ1049179687500000002000000000 
0201F030488MBXX0000000000705407SPCR5883700989 SBODB201604122016041220160401FMATMBZZ1049179687500000008000000000 
Below represents a splice, where 2 trades are combined into 1 
0201F030488MBXX0000000000706483SPCX1940000101XREF004 TFTDS201604122016041220160415 MBZZ10212500000000 00005000000000TBA 
0201F030488MBXX0000000000706483SPCX1930000102XREF005 TFTDS201604122016041220160415 MBZZ1021250000000000005000000000 TBA 
0201F030488MBXX0000000000706483SPCR5883600405 TFTDS201604122016041220160415FMATMBZZ1021250000000000010000000000TBA 
Trailer 
99 MBXX 0000010 0000012 
 

---

## Page 30

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 