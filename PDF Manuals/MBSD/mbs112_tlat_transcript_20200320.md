---
title: "MBSD Trade Lifecycle Activities Tutorial Transcript"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs112_tlat_transcript_20200320.pdf"
pages: 33
size: "913.8 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD Trade Lifecycle Activities Tutorial Transcript

**Original File:** [mbs112_tlat_transcript_20200320.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs112_tlat_transcript_20200320.pdf)  
**Category:** MBSD  
**Total Pages:** 33  
**File Size:** 913.8 KB  

---

## Page 1

 
 
MBSD 
MBSD TRADE LIFECYCLE ACTIVITIES TUTORIAL TRANSCRIPT 
VERSION 1.4 
MARCH 20, 2020 
 
 
 


---

## Page 2

 
 
© 2020 The Depository Trust & Clearing Corporation. All rights reserved.   
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: March 20, 2020 
Publication Code: MBS112 
Service: MBSD 
Title: MBSD Trade Lifecycle Activities Tutorial Transcript 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
MBSD Trade Lifecycle Activity Map ................................................................................................................... 5 
SBOD Trade Activity ............................................................................................................................................ 6 
[[settlement]] Balanced Order Destined (SBOD) Trade Lifecycle .......................................................................... 6 
SBOD – Trade Date .......................................................................................................................................... 6 
SBOD – Contractual [[settlement]] Date Minus 3 (72-Hour Day) ......................................................................... 7 
SBOD – Contractual [[settlement]] Date Minus 2 (48-Hour Day) ......................................................................... 8 
SBOD – Contractual [[settlement]] Date Minus 1 (24-Hour Day) ....................................................................... 10 
SBOD – Contractual [[settlement]] Date ............................................................................................................. 12 
TFTD TBA Trade Activity ................................................................................................................................... 13 
Trade for Trade To-Be-Announced (TFTD TBA) Trade Lifecycle .................................................................... 13 
TFTD TBA – Trade Date ................................................................................................................................. 13 
TFTD TBA – Contractual [[settlement]] Date Minus 3 (72-Hour Day) ................................................................ 14 
TFTD TBA – Contractual [[settlement]] Date Minus 2 (48-Hour day) ................................................................. 15 
TFTD TBA – Contractual [[settlement]] Date Minus 1 (24-Hour day) ................................................................. 17 
TFTD TBA – Contractual [[settlement]] Date ...................................................................................................... 19 
STIP Trade Activity ............................................................................................................................................ 20 
Trade for Trade Stipulated (STIP) Trade Lifecycle ........................................................................................... 20 
STIP Trade – Trade Date ................................................................................................................................ 20 
STIP Trade – Contractual [[settlement]] Date Minus 3 (72-Hour Day) ............................................................... 21 
STIP Trade – Contractual [[settlement]] Date Minus 2 (48-Hour Day) ............................................................... 22 
STIP Trade – Contractual [[settlement]] Date Minus 1 (24-Hour Day) ............................................................... 24 
STIP Trade – Contractual [[settlement]] Date ..................................................................................................... 25 
SPT Trade Activity ............................................................................................................................................. 26 
Specified Pool Trade (SPT) Trade Lifecycle .................................................................................................... 26 
Specified Pool Trade – Trade Date ................................................................................................................. 26 
Specified Pool Trade – Contractual [[settlement]] Date Minus 3 (72-Hour Day) ................................................ 27 
Specified Pool Trade – Contractual [[settlement]] Date Minus 2 (48-Hour Day) ................................................ 28 
Specified Pool Trade – Contractual [[settlement]] Date Minus 1 (24-Hour Day) ................................................ 29 

---

## Page 4

 
 
Specified Pool Trade – Contractual [[settlement]] Date ..................................................................................... 30 
[[Option]] Trade Activity ....................................................................................................................................... 31 
[[Option]] (OPTN) Trade Lifecycle ........................................................................................................................ 31 
[[Option]] Trade – Trade Date ............................................................................................................................. 31 
 

---

## Page 5

MBSD Trade Lifecycle Activities Tutorial Transcript 
MBSD Trade Lifecycle Activity Map 5 
MBSD TRADE LIFECYCLE ACTIVITY MAP 
Below is the high level MBSD Trade Lifecycle Activity Map used throughout the tutorial. It (and all images 
shown in this transcript document) is included for reference only. Please see the online tutorial (log in required) 
for a detailed visual breakdown of the steps described. 
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/
TBA
Dealer 
B
Dealer 
A
Pool Instruct
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
DNA TAP
[[DO]] Not Allocate
SBON TFTD/
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
Trade Lifecycle Activities
  

---

## Page 6

MBSD Trade Lifecycle Activities Tutorial Transcript 
SBOD Trade Activity 6 
SBOD TRADE ACTIVITY 
[[settlement]] Balanced Order Destined (SBOD) Trade Lifecycle 
SBOD – Trade Date 
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/
TBA
Dealer 
B
Dealer 
A
Pool Instruct
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
DNA TAP
[[DO]] Not Allocate
SBON TFTD/
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
On trade date, members submit 
SBOD trades to RTTM®.
Upon trade comparison, trades match 
& novate vs. [[FICC]] TBA [[Novation]] 
account.
*[[FICC]] TBA [[Novation]] Account*[[FICC]] Stipulated Account*[[FICC]] Specified Pool Trade 
Account*TBA - To Be Announced
 
On trade date, members submit their [[settlement]] Balance Order Destined trades (or SBODs) for trade matching 
and [[Novation]] to the Real Time Trade Matching System (RTTM). SBOD trades are trade types that are eligible 
for the TBA Net. TBA Stands for To Be Announced. Upon trade comparison, a [[Member]]’s SBOD trade will 
match and novate versus the [[FICC]] TBA [[Novation]] account referred to as FTBA.  

---

## Page 7

MBSD Trade Lifecycle Activities Tutorial Transcript 
SBOD Trade Activity 7 
SBOD – Contractual [[settlement]] Date Minus 3 (72-Hour Day) 
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/
TBA
Dealer 
B
Dealer 
A
Pool Instruct
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
DNA TAP
[[DO]] Not Allocate
SBON TFTD/
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
On CSD - 3, members may submit 
SBOD trades until 4 pm ET.
At 4 pm ET, TBA Net begins.
*CSD - Contractual [[settlement]] Date
- or -
TBA Net Detail report produced when 
TBA Net is completed.
Any resulting TBA Net position is 
referred to as SBON.
SBON has FTBA as its counterparty.
TBA NET TAP accounts for +/-
between TP vs. [[FICC]] system price.
TBA Net Detail Report
TBA NET TAP
 
Three days prior to the SIFMA Contractual [[settlement]] Date, Members have up until 4 pm ET to submit their 
SBOD trades. At 4 pm, the TBA Net kicks off. Once completed, Members receive their netting output, the TBA 
Net Detail report. If a [[Member]] has any resulting position from the TBA Net, it is referred to as SBON. Like 
SBODs, the SBON position has the FTBA as the counterparty.  A TBA Net transaction adjustment payment 
(TBA NET TAP) is also generated to account for the difference between the trade price vs the [[FICC]] system 
price that was used for the TBA NET. This TBA NET TAP is discussed later and settles on Contractual 
[[settlement]] Date.
  

---

## Page 8

MBSD Trade Lifecycle Activities Tutorial Transcript 
SBOD Trade Activity 8 
SBOD – Contractual [[settlement]] Date Minus 2 (48-Hour Day) 
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/
TBA
Dealer 
B
Dealer 
A
Pool Instruct
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
DNA TAP
[[DO]] Not Allocate
SBON TFTD/
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
On CSD - 2, members have two 
options to process SBON:
1. [[DO]] Not Allocate (DNA)
- OR -
2. Allocate via EPN
If a [[Member]] has offsetting SBON 
and TFTD TBA position (same CSD 
and TBA [[CUSIP]]), SBON positions 
can be paired off or DNA.
This cash differential is the DNA 
Transaction Adjustment Payment 
(DNA TAP) and is processed on the 
SIFMA CSD.
If a [[Member]] has no pair offs, they 
must allocate SBON via EPN.
Selling [[Member]] must submit ON 
message to FTBA by 3 pm ET.
If [[FICC]] successfully validates ON 
message it is sent to the [[Buyer]].
If ON message doesn’t meet criteria 
[[FICC]] will DK or reject it.
Once ON message is successfully 
processed, a Pool Instruct is 
generated for pool netting/
pool conversion process.
 
On 48-Hour Day (two days prior to the SIFMA Contractual [[settlement]] Date), Members have two possible 
options to process their SBON positions: 
• [[DO]]-Not-Allocate (DNA) -OR-  
• Allocate through Electronic Pool Notification (EPN). 
 
If a [[Member]] has an offsetting SBON and TBA TFTD position with the same CSD and TBA [[CUSIP]], it can be 
paired off or DNA’d. (Note that there are a few requirements for trades to be eligible for DNA.) The result will be 
the cash difference between the two paired off trades. This cash differential is referred to as the DNA 
Transaction Adjustment Payment (or DNA TAP). The DNA TAP is processed on the SIFMA Contractual 
[[settlement]] Date. Most Members prefer to DNA SBON positions on 48-Hour Day to take advantage of being 

---

## Page 9

MBSD Trade Lifecycle Activities Tutorial Transcript 
SBOD Trade Activity 9 
able to pair-off their offsetting positions instead of allocating them and settling pool [[obligations]] at the clearing 
bank. 
If a [[Member]] does not have any potential pair offs, they must allocate their SBON position through EPN. To 
initiate the allocation the Selling [[Member]] must submit an Original Notification (ON) message to the FTBA 
account on EPN. For [[settlement]] to take place on the SIFMA CSD, members must submit their ON messages 
by 3 pm ET on 48-Hour day. [[FICC]]’s allocation engine will validate the ON message and if successful, will send 
the message to the [[Buyer]]. If the ON message does not meet the criteria or if there is an error, [[FICC]] will either 
DK or reject the message (depending on the circumstances). Once the ON message has been successfully 
processed, a pool instruct will be generated for the pool netting/pool conversion process. Any trade allocated 
after 3 pm ET on 48-Hour Day up until 4:30 pm ET on 24-Hour Day goes through the Expanded Pool Net 
process. 
 

---

## Page 10

MBSD Trade Lifecycle Activities Tutorial Transcript 
SBOD Trade Activity 10 
SBOD – Contractual [[settlement]] Date Minus 1 (24-Hour Day) 
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/
TBA
Dealer 
B
Dealer 
A
Pool Instruct
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
[[DO]] Not Allocate
SBON TFTD/
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
Pool Instructs from CSD-2 submitted ON messages 
are processed through Pool Net by 2 pm ET.
Resulting Pool Net positions called Pool [[obligations]] 
(POID) face the [[FICC]] Pool Net account.
Pool Netting Detail Report
Refer to the Pool Netting Detail report to see what 
pool instructs went into pool net & generated POID.
TAP
Pool Net Transaction Adjustment Payment (TAP) 
accounts for +/- between pool instruct price & [[FICC]]. 
TAP gets processed on SIFMA CSD.
Open SBON positions can still be DNA or Allocated 
via EPN until 4:30 pm ET but won’t settle on CSD.
DNA, Expanded Pool Net & Reprice processes
begin at 4:30 pm ET.
1. DNA is marked settled.
2. CSD-2 trades go through Expanded Pool Netting 
process. See EXP Pool Netting Report.
EXP TAP accounts for +/- between pool instruct price 
& [[FICC]] price used in expanded pool netting. 
EXP TAP
EXP TAP is processed on CSD. 
SBON positions not allocated via EPN on CSD-1 are 
repriced to [[FICC]] and assigned a new trade [[ID]].
RPC TAP is generated for reprice process and is also 
processed on CSD.
RPC TAP
EXP Pool Netting Detail
 
On 24-Hour Day, one day prior to the SIFMA Contractual [[settlement]] Date, the Pool Net takes place at 2 pm 
ET. As a result, the pool instructs eligible for pool netting that were generated from the ON messages 
submitted prior to 3 pm ET on 48-Hour day are processed through the Pool Net. The resulting positions from 
the Pool Net are called Pool [[obligations]] (POIDs) and face the [[FICC]] Pool Net account, [[FICC]].  
Members can refer to the Pool Netting Detail report to see what pool instructs went into the Pool Net and the 
resulting Pool [[obligations]] that were generated.  
A Pool Net Transaction Adjustment Payment (called TAP) is generated to account for the price difference 
between the prices on the Pool Instructs and the [[FICC]] system price used during pool netting. This TAP is 
processed on the SIFMA Contractual [[settlement]] Date.  

---

## Page 11

MBSD Trade Lifecycle Activities Tutorial Transcript 
SBOD Trade Activity 11 
If a [[Member]] has any remaining open SBON position, they can continue to submit DNA requests to RTTM -OR- 
ON messages to EPN until 4:30 pm. Please remember that any ON messages submitted after 3 pm ET on 48-
Hour Day will not settle on their original Contractual [[settlement]] Date. 
At 4:30 pm ET, the DNA, Expanded Pool Net and Reprice processes begin.  
As a result, DNA requests are marked as settled.  
Any trade allocated after 3 pm ET on 48-Hour Day up until 4:30 pm ET on 24-Hour Day goes through the 
Expanded Pool Net process. Members can refer to the Expanded Pool Netting Detail report to see what pool 
instructs went into the Expanded Pool Net and the resulting Pool [[obligations]] that were generated. An 
Expanded Pool Net Transaction Adjustment Payment (called EXP TAP) is generated to account for the price 
difference between the prices on the pool instructs and the [[FICC]] system price used during Expanded Pool 
Netting. This EXP TAP is processed on the SIFMA Contractual [[settlement]] Date.  
Any SBON positions not allocated or DNA’d by end of 24-Hour Day will now be repriced to the [[FICC]] system 
price on Contractual [[settlement]] Date minus 1. The original trades are marked as settled and new trades are 
booked with the [[FICC]] system price and are assigned a new trade [[ID]]. For the reprice process, there is also a 
Reprice Transaction Adjustment Payment referred to as the RPC TAP (which is also processed on SIFMA 
CSD).  

---

## Page 12

MBSD Trade Lifecycle Activities Tutorial Transcript 
SBOD Trade Activity 12 
SBOD – Contractual [[settlement]] Date 
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/
TBA
Dealer 
B
Dealer 
A
Pool Instruct
Generation for Pool 
Net/Conversion
Pool Netting / Conversion
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Pool Conversion
EPN
[[DO]] Not Allocate
SBON TFTD/
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)
*CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]]
Clearing 
Bank for 
[[settlement]]
SBON 
POIDs
CSD
On CSD, MBSD sends SBON POIDs and [[settlement]] 
instructions to Clearing Bank which facilitates 
delivery of [[securities]] and payment over Fedwire vs. 
[[FICC]]. All TAPs settle via Cash Only [[settlement]] at 
Cash Settling Bank.
The Pool Obligation Pending [[settlement]] Report 
shows Pool [[obligations]] awaiting [[settlement]].
SBON Positions not allocated via EPN before 3 pm 
on 48-Hour Day will not settle on CSD.
Start Over
Pool Obligation 
Pending [[settlement]]
 
On Contractual [[settlement]] Date, MBSD sends the Pool [[obligations]] and [[settlement]] instructions to the Clearing 
Bank, which will facilitate the delivery of [[securities]] and full payment over the Fedwire versus [[FICC]]. All the 
various TAPs associated with the TBA Net, DNA, Pool Net, Expanded Pool Net, and Reprice settle through the 
Cash-Only [[settlement]] process at the Cash Setting bank.  
The Pool Obligation Pending [[settlement]] Report allows members to see what Pool [[obligations]] are awaiting 
[[settlement]] between their account and [[FICC]]. Lastly, barring any exception processing requests, note that any 
SBON Position not allocated via EPN before 3 pm ET on 48-Hour Day will not settle on CSD. 

---

## Page 13

MBSD Trade Lifecycle Activities Tutorial Transcript 
TFTD TBA Trade Activity 13 
TFTD TBA TRADE ACTIVITY 
Trade for Trade To-Be-Announced (TFTD TBA) Trade Lifecycle 
TFTD TBA – Trade Date 
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/ 
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/ 
TBA
Dealer 
B
Dealer 
A
Pool Instruct 
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
DNA TAP
[[DO]] Not Allocate
SBON TFTD/ 
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
On trade date, members submit 
TFTD TBA trades to RTTM®.
Upon trade comparison, trades match 
& novate vs. [[FICC]] TBA [[Novation]] 
account (FTBA).
*[[FICC]] TBA [[Novation]] Account*[[FICC]] Stipulated Account*[[FICC]] Specified Pool Trade 
Account*TBA - To Be Announced
 
On trade date, members submit their Trade for Trade To-Be-Announced trades (TFTD TBA) for trade matching 
and [[Novation]] to the Real Time Trade Matching System (RTTM). Trade for Trade TBA trades are trade types 
that are submitted when TBA Netting is not desired or are submitted after the TBA Net has already taken 
place. Upon trade comparison, a [[Member]]’s Trade for Trade TBA trade will match and novate versus the [[FICC]] 
TBA [[Novation]] account referred to as FTBA. 

---

## Page 14

MBSD Trade Lifecycle Activities Tutorial Transcript 
TFTD TBA Trade Activity 14 
TFTD TBA – Contractual [[settlement]] Date Minus 3 (72-Hour Day) 
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/ 
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/ 
TBA
Dealer 
B
Dealer 
A
Pool Instruct 
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
DNA TAP
[[DO]] Not Allocate
SBON TFTD/ 
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
TFTD TBAs are not subject to TBA 
Net and have no CSD-3 submission 
deadline. Like SBON, TFTD TBA has 
FTBA as its counterparty.
*CSD - Contractual [[settlement]] Date
- or -
TBA NET
 
Unlike SBOD trades, Trade for Trade TBAs are not required to be submitted by 4 pm ET on CSD-3. Like 
SBOD trades and SBON positions, the TFTD TBA position has the [[FICC]] TBA account (FTBA) as the 
counterparty.  

---

## Page 15

MBSD Trade Lifecycle Activities Tutorial Transcript 
TFTD TBA Trade Activity 15 
TFTD TBA – Contractual [[settlement]] Date Minus 2 (48-Hour day) 
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/ 
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/ 
TBA
TFTD/ 
TBA
Dealer 
B
Dealer 
A
Pool Instruct 
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
DNA TAP
[[DO]] Not Allocate
SBON TFTD/ 
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
On CSD - 2, members have two 
options to process TFTD TBA:
1. [[DO]] Not Allocate (DNA)
- OR -
2. Allocate via EPN
If a [[Member]] has offsetting SBON 
and TFTD TBA position (same CSD 
and TBA [[CUSIP]]), TFTD TBA 
positions can be paired off or DNA.
This cash differential is the DNA 
Transaction Adjustment Payment 
(DNA TAP) and is processed on the 
SIFMA CSD.
If a [[Member]] has no pair offs, they 
must allocate TFTD TBA via EPN.
Selling [[Member]] must submit ON 
message to FTBA by 3 pm ET.
If [[FICC]] successfully validates ON 
message it is sent to the [[Buyer]].
If ON message doesn’t meet criteria 
[[FICC]] will DK or reject it.
Once ON message is successfully 
processed, a Pool Instruct is 
generated for pool netting/
pool conversion process.
 
On 48-Hour Day (two days prior to the SIFMA Contractual [[settlement]] Date), Members have two possible 
options to process their Trade for Trade TBA positions: 
• [[DO]]-Not-Allocate (DNA) -OR-  
• Allocate through Electronic Pool Notification (EPN). 
 
If a [[Member]] has an offsetting [[settlement]] Balance Order Netted (SBON) position and Trade for Trade TBA 
position or two offsetting Trade for Trade TBA positions with the same CSD and TBA [[CUSIP]], it can be paired 
off or DNA’d. (Note that there are a few requirements for trades to be eligible for DNA.) The result will be the 
cash difference between the two paired off trades. This cash differential is referred to as the DNA Transaction 
Adjustment Payment (or DNA TAP). The DNA TAP is processed on the SIFMA Contractual [[settlement]] Date. 

---

## Page 16

MBSD Trade Lifecycle Activities Tutorial Transcript 
TFTD TBA Trade Activity 16 
Most Members prefer to DNA Trade for Trade TBA positions on 48-Hour Day to take advantage of being able 
to pair-off their offsetting positions instead of allocating them and settling pool [[obligations]] at the clearing bank.  
If a [[Member]] does not have any potential pair offs, they must allocate their Trade for Trade TBA position 
through EPN. To initiate the allocation the Selling [[Member]] must submit an Original Notification (ON) message 
to the FTBA account on EPN. For [[settlement]] to take place on the SIFMA CSD, Members must submit their ON 
messages by 3 pm ET on 48-Hour day. [[FICC]]’s allocation engine will validate the ON message and if 
successful, will send the message to the [[Buyer]]. If the ON message does not meet the criteria or if there is an 
error, [[FICC]] will either DK or reject the message (depending on the circumstances). Once the ON message has 
been successfully processed, a pool instruct will be generated for the pool netting/pool conversion process. 
Any trade allocated after 3 pm ET on 48-Hour Day up until 4:30 pm ET on 24-Hour Day goes through the 
Expanded Pool Net process.  

---

## Page 17

MBSD Trade Lifecycle Activities Tutorial Transcript 
TFTD TBA Trade Activity 17 
TFTD TBA – Contractual [[settlement]] Date Minus 1 (24-Hour day) 
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/ 
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/ 
TBA
Dealer 
B
Dealer 
A
Pool Instruct 
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
[[DO]] Not Allocate
SBON TFTD/ 
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
Pool Instructs from CSD-2 submitted ON messages 
are processed through Pool Net by 2 pm ET.
Resulting Pool Net positions called Pool [[obligations]] 
(POID) face the [[FICC]] Pool Net account.
Pool Netting Detail Report
Refer to the Pool Netting Detail report to see what 
pool instructs went into pool net & generated POID.
TAP
Pool Net Transaction Adjustment Payment (TAP) 
accounts for +/- between pool instruct price & [[FICC]]. 
TAP gets processed on SIFMA CSD. Open TFTD TBA 
positions can still be DNA or Allocated via EPN until 
4:30 pm ET but won’t settle on CSD.
DNA, Expanded Pool Net & Reprice processes
begin at 4:30 pm ET.
1. DNA is marked settled.
2. CSD-2 trades go through Expanded Pool Netting 
process. See EXP Pool Netting Report.
EXP TAP accounts for +/- between pool instruct price 
& [[FICC]] price used in expanded pool netting. 
EXP TAP
EXP TAP is processed on CSD. 
TFTD TBA positions not allocated via EPN on CSD-1 
are repriced to [[FICC]] and assigned a new trade [[ID]].
RPC TAP is generated for reprice process and is also 
processed on CSD.
RPC TAP
EXP Pool Netting Detail
 
On 24-Hour Day, one day prior to the SIFMA Contractual [[settlement]] Date, the Pool Net takes place at 2 pm 
ET. As a result, the pool instructs eligible for pool netting that were generated from the ON messages 
submitted prior to 3 pm ET on 48-Hour day are processed through the Pool Net. The resulting positions from 
the Pool Net are called Pool [[obligations]] (POIDs) and face the [[FICC]] Pool Net account, [[FICC]].  
Members can refer to the Pool Netting Detail report to see what pool instructs went into the Pool Net and the 
resulting Pool [[obligations]] that were generated.  
A Pool Net Transaction Adjustment Payment (called TAP) is generated to account for the price difference 
between the prices on the Pool Instructs and the [[FICC]] system price used during pool netting. This TAP is 
processed on the SIFMA Contractual [[settlement]] Date.  

---

## Page 18

MBSD Trade Lifecycle Activities Tutorial Transcript 
TFTD TBA Trade Activity 18 
If a [[Member]] has any remaining open Trade for Trade TBA position, they can continue to submit DNA requests 
to RTTM -OR- ON messages to EPN until 4:30 pm. Please remember that any ON messages submitted after 3 
pm ET on 48-Hour Day will not settle on their original Contractual [[settlement]] Date. 
At 4:30 pm ET, the DNA, Expanded Pool Net and Reprice processes kick off.  
As a result, DNA requests are marked as settled.  
Any trade allocated after 3 pm ET on 48-Hour Day up until 4:30 pm ET on 24-Hour Day goes through the 
Expanded Pool Net process. Members can refer to the Expanded Pool Netting Detail report to see what pool 
instructs went into the Expanded Pool Net and the resulting Pool [[obligations]] that were generated. An 
Expanded Pool Net Transaction Adjustment Payment (called EXP TAP) is generated to account for the price 
difference between the prices on the pool instructs and the [[FICC]] system price used during Expanded Pool 
Netting. This EXP TAP is processed on the SIFMA Contractual [[settlement]] Date.  
Any Trade for Trade TBA positions not allocated or DNA’d by end of 24-Hour Day will now be repriced to the 
[[FICC]] system price on Contractual [[settlement]] Date minus 1. The original trades are marked as settled and new 
trades are booked with the [[FICC]] system price and are assigned a new trade [[ID]]. For the reprice process, there 
is also a Reprice Transaction Adjustment Payment referred to as the RPC TAP (which is also processed on 
SIFMA CSD). 
 
 

---

## Page 19

MBSD Trade Lifecycle Activities Tutorial Transcript 
TFTD TBA Trade Activity 19 
TFTD TBA – Contractual [[settlement]] Date 
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/ 
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/ 
TBA
Dealer 
B
Dealer 
A
Pool Instruct 
Generation for Pool 
Net/Conversion
Pool Netting / Conversion
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Pool Conversion
EPN
[[DO]] Not Allocate
SBON TFTD/ 
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)
*CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]]
Clearing 
Bank for 
[[settlement]]
SBON 
POIDs
CSD
On CSD, MBSD sends TFTD TBA POIDs & [[settlement]] 
instructions to Clearing Bank which facilitates 
delivery of [[securities]] and payment over Fedwire vs. 
[[FICC]]. All TAPs settle via Cash Only [[settlement]] at 
Cash Settling Bank.
The Pool Obligation Pending [[settlement]] Report 
shows Pool [[obligations]] awaiting [[settlement]].
TFTD TBA Positions not allocated via EPN before 3 
pm on 48-Hour Day will not settle on CSD.
Start Over
Pool Obligation 
Pending [[settlement]]
 
On Contractual [[settlement]] Date, MBSD sends the Pool [[obligations]] and [[settlement]] instructions to the Clearing 
Bank, which will facilitate the delivery of [[securities]] and full payment over the Fedwire versus [[FICC]]. All the 
various TAPs associated with the DNA, Pool Net, Expanded Pool Net, and Reprice settle through the Cash-
Only [[settlement]] process at the Cash Settling bank.  
The Pool Obligation Pending [[settlement]] Report allows members to see what Pool [[obligations]] are awaiting 
[[settlement]] between their account and [[FICC]]. Lastly, barring any exception processing requests any Trade for 
Trade TBA Positions not allocated via EPN before 3 pm on 48-Hour Day will not settle on CSD. 
  

---

## Page 20

MBSD Trade Lifecycle Activities Tutorial Transcript 
STIP Trade Activity 20 
STIP TRADE ACTIVITY 
Trade for Trade Stipulated (STIP) Trade Lifecycle 
STIP Trade – Trade Date 
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/ 
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/ 
TBA
Dealer 
B
Dealer 
A
Pool Instruct 
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
DNA TAP
[[DO]] Not Allocate
SBON TFTD/ 
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
On trade date, members submit 
STIP trades to RTTM®.
Upon trade comparison, STIP trades 
match & novate vs. [[FICC]] Stipulated 
account (FSTI).
*[[FICC]] TBA [[Novation]] Account*[[FICC]] Stipulated Account*[[FICC]] Specified Pool Trade 
Account*TBA - To Be Announced
 
On trade date, members submit their Trade for Trade Stipulated Trades (or STIP trades) for trade matching 
and [[Novation]] to the Real Time Trade Matching System (RTTM). STIP trades are trades in which there is a 
stipulation on one or more of the trade terms. Although members submit trades into RTTM indicating they are 
STIP trades, the actual stipulated terms are unknown to [[FICC]]. Upon trade comparison, a [[Member]]’s STIP 
trades will match and novate versus the [[FICC]] Stipulated Account referred to as FSTI. 
  

---

## Page 21

MBSD Trade Lifecycle Activities Tutorial Transcript 
STIP Trade Activity 21 
STIP Trade – Contractual [[settlement]] Date Minus 3 (72-Hour Day) 
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/ 
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/ 
TBA
Dealer 
B
Dealer 
A
Pool Instruct 
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
DNA TAP
[[DO]] Not Allocate
SBON TFTD/ 
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
STIP trades are not eligible for the 
TBA Net and have no CSD-3 
submission deadline. STIP has FSTI 
as its counterparty.
*CSD - Contractual [[settlement]] Date
- or -
TBA NET
 
STIP trades are not eligible for the TBA Net and are therefore not required to be submitted by 4 pm ET on CSD 
-3.  As mentioned during the STIP Trade Date phase, STIP trades have the [[FICC]] Stipulated Account as their 
counterparty. 
  

---

## Page 22

MBSD Trade Lifecycle Activities Tutorial Transcript 
STIP Trade Activity 22 
STIP Trade – Contractual [[settlement]] Date Minus 2 (48-Hour Day) 
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/ 
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/ 
TBA
TFTD/ 
TBA
Dealer 
B
Dealer 
A
Pool Instruct 
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
DNA TAP
[[DO]] Not Allocate
SBON TFTD/ 
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
On CSD - 2, Members allocate via 
EPN STIP trades vs. FSTI.
STIP trades are not eligible for DNA.
Via EPN, selling Members submit ON 
messages to FSTI (w/RTTM Trade [[ID]]).
STIP allocation methods:
1. Good Delivery Millions (GDM)
-OR-
2. Bid List Terminators
Members must submit ON 
messages by 3 pm ET on CSD-2 for 
CSD [[settlement]]. Trade buy side is 
responsible for validation.
If ON message does not meet 
criteria (or if in error) [[FICC]] or [[Buyer]] 
will either DK or reject it.
Once ON message is successfully 
processed, a Pool Instruct is 
generated for pool conversion 
process.
 
On 48-Hour Day (two days prior to the SIFMA Contractual [[settlement]] Date), Members allocate via Electronic 
Pool Notification (EPN) their Stipulated Trades versus the FSTI account. Unlike SBON and TBA TFTD 
positions, Stipulated Trades are not eligible for the [[DO]]-Not-Allocate (DNA) [[pair off]] process.  
To initiate the allocation the Selling [[Member]] must submit an Original Notification (ON) message to the FSTI 
account on EPN. Members must include the RTTM Trade [[ID]] in the STIP allocation. 
There are two methods of STIP allocation: 
• Good Delivery Millions (GDM) – The allocation is fully validated based on the SIFMA compliance rules; -
OR- 
• Bid List Terminators – No validation is done based on SIFMA compliance rules.  

---

## Page 23

MBSD Trade Lifecycle Activities Tutorial Transcript 
STIP Trade Activity 23 
For [[settlement]] to take place on the SIFMA CSD, members must submit their ON messages by 3 pm ET on 48-
Hour Day. [[FICC]]’s allocation engine will validate the ON message and if successful, will send the message to 
the [[Buyer]]. The buy side of the trade is responsible for the validation of all underlying stipulations.  
If the ON message does not meet the criteria or if there is an error, [[FICC]] or the [[Buyer]] will either DK or reject 
the message (depending on the circumstances). Once the ON message has been successfully processed, a 
pool instruct will be generated for the pool conversion process. 
  

---

## Page 24

MBSD Trade Lifecycle Activities Tutorial Transcript 
STIP Trade Activity 24 
STIP Trade – Contractual [[settlement]] Date Minus 1 (24-Hour Day) 
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/ 
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/ 
TBA
Dealer 
B
Dealer 
A
Pool Instruct 
Generation for Pool 
Net/Conversion
Pool Netting / ConversionSettlement
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Clearing 
Bank for 
[[settlement]]
Pool Conversion
EPN
[[DO]] Not Allocate
SBON TFTD/ 
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
SBON 
POIDs
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
Instructs
STIP Pool 
[[obligations]] 
(POIDs)
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)CSD *CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
Members with any remaining open STIP position can 
submit ON messages to EPN until 4:30 pm ET.
Any ON messages submitted after 3 pm ET on CSD-2 
won’t settle on their original CSD.
Pool Conversion process begins at 4:30 pm.
Pool instructs targeting STIP trades are converted 
into pool [[obligations]] on day before delivery date. 
Resulting receive and deliver [[obligations]] are vs. FSTI 
at trade price.
Members can refer to the POID Conversion report to 
see STIP pool instructs converted to pool [[obligations]].
STIP not allocated via EPN on CSD-2 up until 4:30 pm 
ET on CSD-1 will not be repriced to [[FICC]] system 
price on CSD-1.
Original trade price remains unchanged.
POID Conversion Report
 
On 24-Hour Day, one day prior to the SIFMA Contractual [[settlement]] Date, if a [[Member]] has any remaining 
open STIP position, they can continue to submit ON messages to EPN until 4:30 pm ET.  Any ON messages 
submitted after 3 pm ET on 48-Hour Day will not settle on their original Contractual [[settlement]] Date. At 4:30 
pm, the Pool Conversion process kicks off.  
As a result, pool instructs targeting STIP trades, which are not eligible for the pool netting service, are directly 
converted into pool [[obligations]] on the day before delivery date. Resulting receive and deliver [[obligations]] will be 
versus [[FICC]] Stipulated Account (FSTI) at trade price. Members can refer to the POID Conversion report to see 
what STIP pool instructs were converted to pool [[obligations]].
 
Any STIP positions not allocated through EPN on 48-Hour Day up until 4:30 pm ET on 24-Hour day will not be 
repriced to the [[FICC]] system price on Contractual [[settlement]] Date minus 1. The original trade price at the time 
of trade submission remains unchanged. 

---

## Page 25

MBSD Trade Lifecycle Activities Tutorial Transcript 
STIP Trade Activity 25 
STIP Trade – Contractual [[settlement]] Date 
[[settlement]] 
Balance Order 
Destined 
(SBOD)
FTBA* FSTI* FSPT*
Trade Matching via 
RTTM and [[Novation]]
[[settlement]] 
Balance Order 
Net (SBON)
SBOD
SBOD
SBOD
SBON STIP SPTTFTD/ 
TBA OPTN
Trade Positions
TBA NETDo-Not-Allocate (DNA)  Allocation via EPN
[[FICC]]
SBON STIP TFTD/ 
TBA
Dealer 
B
Dealer 
A
Pool Instruct 
Generation for Pool 
Net/Conversion
Pool Netting / Conversion
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Pool Net
TFTD/ 
TBA 
POIDs
STIP 
POIDs
SPT 
POIDs
Pool Conversion
EPN
[[DO]] Not Allocate
SBON TFTD/ 
TBA
EPN
Cash [[settlement]] -
No Delivery of 
[[securities]]
FSTIFTBA FSPT
[[Option]] Trade 
(OPTN)
Trade Lifecycle Activities
STIP Pool 
[[obligations]] 
(POIDs)
STIP Pool 
Instructs
SPT Pool 
[[obligations]] 
(POIDs)
SPT Trade 
Positions
CSD – 2
(48-Hour Day)
CSD – 1
(24-Hour Day)
*CSD – 3
(72-Hour Day) Trade Date
Stipulated 
Trade-for-Trade 
(TFTD/STIP)
Trade-for-
Trade/TBA*
(TFTD/TBA)
Specified Pool 
Trade-for-Trade 
(TFTD/SPT)
- or -
Pool [[obligations]] 
(POIDs) vs. [[FICC]]
SBON
TFTD/ 
TBA
Expanded Pool Net
[[settlement]]
Clearing 
Bank for 
[[settlement]]
SBON 
POIDs
CSD
On CSD, MBSD sends STIP POIDs & [[settlement]] 
instructions to Clearing Bank which facilitates 
delivery of [[securities]] and payment over Fedwire vs. 
[[FICC]] Stipulated Account, FSTI. 
The Pool Obligation Pending [[settlement]] Report 
shows Pool [[obligations]] awaiting [[settlement]].
Start Over
Pool Obligation 
Pending [[settlement]]
 
On Contractual [[settlement]] Date, MBSD sends the Pool [[obligations]] and [[settlement]] instructions to the Clearing 
Bank, which will facilitate the delivery of [[securities]] and full payment over the Fedwire versus the [[FICC]] 
Stipulated Account, FSTI. The Pool Obligation Pending [[settlement]] Report allows members to see what Pool 
[[obligations]] are awaiting [[settlement]] between their account and [[FICC]]. 
  

---

## Page 26

MBSD Trade Lifecycle Activities Tutorial Transcript 
SPT Trade Activity 26 
SPT TRADE ACTIVITY 
Specified Pool Trade (SPT) Trade Lifecycle 
Specified Pool Trade – Trade Date 
 
On trade date, members submit their Trade for Trade Specified Pool Trades (or SPT trades) for trade matching 
and [[Novation]] to the Real Time Trade Matching System (RTTM). A Specified Pool Trade is a trade where the 
pool number and original face are agreed upon at the time of trade execution. The [[Seller]] of the trade is 
required to deliver that specified pool to satisfy the terms of the trade. Upon trade comparison, a [[Member]]’s 
Specified Pool Trade will match and novate versus the [[FICC]] Specified Pool Trade Account referred to as 
FSPT.  


---

## Page 27

MBSD Trade Lifecycle Activities Tutorial Transcript 
SPT Trade Activity 27 
Specified Pool Trade – Contractual [[settlement]] Date Minus 3 (72-Hour Day) 
 
Specified Pool Trades are not eligible for the TBA Net and are therefore not required to be submitted by 4 pm 
ET on CSD -3.  As mentioned during the SPT Trade Date phase, SPT trades have the [[FICC]] Specified Pool 
Trade Account as their counterparty. 
  


---

## Page 28

MBSD Trade Lifecycle Activities Tutorial Transcript 
SPT Trade Activity 28 
Specified Pool Trade – Contractual [[settlement]] Date Minus 2 (48-Hour Day) 
 
For Specified Pool Trades on 48-Hour Day (two days prior to the SIFMA Contractual [[settlement]] Date), there 
are no allocations submitted via Electronic Pool Notification (EPN). Neither are Specified Pool Trades eligible 
for the [[DO]]-Not-Allocate (DNA) pairoff process. Specified Pool Trades [[DO]] not qualify for EPN allocation or DNA 
submissions because the pool number and original face are known at the time of trade execution. 
  


---

## Page 29

MBSD Trade Lifecycle Activities Tutorial Transcript 
SPT Trade Activity 29 
Specified Pool Trade – Contractual [[settlement]] Date Minus 1 (24-Hour Day) 
 
At 4:30 PM ET on 24-Hour Day, one day prior to the SIFMA Contractual [[settlement]] Date, the Pool Conversion 
process begins. As a result, Specified Pool Trades, which are not eligible for the pool netting service, are 
directly converted into pool [[obligations]] on the day before delivery date. Resulting receive and deliver 
[[obligations]] will be versus the [[FICC]] Specified Pool Trade Account (FSPT) at trade price. (Unlike SBON 
positions and TBA Trade for Trade positions, Specified Pool Trades are not subject to the reprice process. The 
original trade price at the time of trade submission remains unchanged.)  
Members can view the POID Conversion report to see what Specified Pool Trades were converted to pool 
[[obligations]]. 
  


---

## Page 30

MBSD Trade Lifecycle Activities Tutorial Transcript 
SPT Trade Activity 30 
Specified Pool Trade – Contractual [[settlement]] Date 
 
Specified Pool Trades that match and novate on Contractual [[settlement]] Date, or match and novate with a 
Contractual [[settlement]] Date prior to the current business date, will be immediately converted to pool 
[[obligations]]. MBSD sends the pool [[obligations]] and [[settlement]] instructions to the Clearing Bank for [[settlement]]. 
The Clearing Bank facilitates the delivery of [[securities]] and full payment over the Fedwire versus the [[FICC]] 
Specified Pool Trade Account, FSPT. 
Members can refer to the Cash Trade POID Conversion report to view their Specified Pool Trades converted 
for same day [[settlement]] into pool [[obligations]], and the Pool Obligation Pending [[settlement]] Report to see what 
pool [[obligations]] are awaiting [[settlement]] between their account and [[FICC]]. 
  


---

## Page 31

MBSD Trade Lifecycle Activities Tutorial Transcript 
[[Option]] Trade Activity 31 
[[Option]] TRADE ACTIVITY 
[[Option]] (OPTN) Trade Lifecycle 
[[Option]] Trade – Trade Date 
 
On trade date, members submit their [[Option]] trades (or OPTN trades) for trade matching to the Real Time 
Trade Matching System (RTTM). RTTM compares put and [[Call option]] trades. Unlike the other MBSD trade 
types, Options [[DO]] not go through the processing flow displayed from 72-Hour day to [[settlement]] Date.  
Because options are a type of derivative where the underlying security is a TBA, options are neither eligible for 
TBA Netting nor Pool Netting and are not allocated pools during the allocation process. [[Option]] trades [[DO]] NOT 


---

## Page 32

MBSD Trade Lifecycle Activities Tutorial Transcript 
[[Option]] Trade Activity 32 
novate versus [[FICC]]. In addition, [[Option]] trades can not be paired off through the [[DO]]-Not-Allocate (DNA) 
process. 
For Options, MBSD Members can choose to exercise the trade up until the expiration date or cancel the trade. 
If the [[Buyer]] of the [[Option]] chooses to exercise the [[Option]], both parties need to cancel the trade to remove the 
[[Option]] from [[FICC]]’s books. Both parties need to subsequently submit a Trade Instruct to [[FICC]] for the 
underlying TBA trade for comparison and risk management. [[FICC]] does not link the [[Option]] to the resulting TBA 
trade. 
Upon expiration of the [[Option]], both members should submit a cancel to remove the [[Option]] trade from [[FICC]]’s 
books and risk management process. [[FICC]] does not systemically purge Options after expiration. 
  

---

## Page 33

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 