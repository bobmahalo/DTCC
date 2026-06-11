---
title: "MBS Novation STIP Pool Conversion"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs144_nov_pid_conv.pdf"
pages: 12
size: "580.4 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBS Novation STIP Pool Conversion

**Original File:** [mbs144_nov_pid_conv.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs144_nov_pid_conv.pdf)  
**Category:** MBSD  
**Total Pages:** 12  
**File Size:** 580.4 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
MBS [[Novation]]: POOL (PID) CONVERSION 
VERSION 1.02 
FEBRUARY 10, 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
This document (the “Document”) is provided as a convenience to members and is for informational pu rposes only. The 
specific processes and services referenced in this Document are subject to the U.S. [[securities]] and Exchange 
Commission’s approval of the Clearing Rules of the Mortgage -Backed [[securities]] Division (“MBSD”) of the Fixed Income 
Clearing Corpor ation (“[[FICC]]”).  
 
This Document should not be regarded as a definitive or exhaustive description of [[FICC]]/MBSD’s services or risk -
management framework; nor should it be regarded as a substitute for the Clearing Rules, which govern in all respects, the 
relationship between [[FICC]]/MBSD and its members. In all cases, members should refer to the Clearing Rules for a 
complete statement of [[FICC]]/MBSD procedures, [[obligations]], and requirements. Nothing in this Document shall be deemed 
to impose any [[obligations]] on [[FICC]]/M BSD that are not set forth in the Clearing Rules, and in the case of any discrepancy 
between this Document and the Clearing Rules, the Clearing Rules shall govern. The services and risk -management 
practices described in this Document may be amended at any time without prior notice.  
 
 
Doc Date: February 10, 2023 
Publication Code:  MBS144 
Service: Fixed Income Clearing Corporation 
Title: MBS [[Novation]] : Pool (PID) Conversion  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ....................................................................................................................... 4 
1. Overview...................................................................................................................................... 5 
2. Generic TBA ................................................................................................................................ 6 
2.1 GDM/Tail Lot Allocations ................................................................................................... 6 
2.2 GDM/Tail Lot Allocations with SIFMA Exception .................................................................... 6 
3. STIP Trades .................................................................................................................................  8 
3.1 GDM/Tail Lot Allocations ................................................................................................... 8 
3.2 Bidlist Allocations ............................................................................................................. 9 
3.3 CC Proc es sing ............................................................................................................... 11 
 

---

## Page 4

MBS [[Novation]]: Pool (PID) Conversion 
Version C ontrol Page 4 
VERSION CONTROL PAGE 
Date Version# Name Description of Change 
05/05/2017 1.0 C. Swords  Initial version  
6/26/2017 1.01 C. Swords  Updated as follows:  
• Renamed document from “STIP Pool Conversion” to “Pool 
(PID) Conversion”, as this now includes allocations to generic 
TBA that are non -SIFMA compliant.  
• Streamline bidlist conversion rules to be at “lot level”.  
• Add exception processing for generic TBA for ov er-variance 
SIFMA exception.  
• Clarified CC processing rules  
11/29/2017 1.02 C. Swords  Updated as follows:  
• Clarified in Overview Section that allocations to generic TBA 
trades result in POIDs at either system price (for netted PIDs) 
or trade price (for direct conversions).  
n/a n/a [[DTCC]] Learning  Updated formatting only. Content is unchanged.  
2/10/2023 1.02 J. Sheeran  Removed Overview of MBS [[Novation]] section  
 
  

---

## Page 5

MBS [[Novation]]: Pool (PID) Conversion 
Version C ontrol Page 5 
1.  OVERVIEW 
In the [[Novation]] system, all trades, including those with stipulations, are settled though [[FICC]]. Members submit 
allocations via EPN, which automatically are fed to the Pool Net system and result in associated Pool Instructs 
(PIDs). 
For generic TBA trades, on day before delivery date (or earlier), these PIDs are netted or directly converted 
into Pool [[obligations]] (POIDs). This results in: 1) automatic draw down of the TBA trade open position using 
internal FICCNOS and 2) automatic generation of a corresponding POID(s) versus [[FICC]] at either system price 
(for netted PIDs) or trade price (for direct conversions). 
To support stipulations, members submit trades with TFTD sub-type “STIP” which identifies that a TBA trade 
has stipulations attached. Pool allocations for these trades are submitted via EPN in the usual manner, but 
must identify the specific trade to target, using the RTTM-assigned Trade [[ID]]. As with all pool allocations, these 
are automatically fed to the Pool Net system and result in associated PIDs, although STIP allocations are not 
subject to netting. On day before delivery date (or earlier), these PIDs are directly converted to Pool 
[[obligations]] (POIDs) resulting in: 1) automatic draw down of the STIP trade open position using internal 
FICCNOS and 2) automatic generation of a corresponding POID versus FSTI at the trade’s execution price. 
In all cases, the generated POIDs are sent to the Clearing Banks for [[settlement]] on the delivery day of the 
corresponding PID. 
While PIDs in a lot typically have the same delivery date (and thus are converted at same day), CC and/or 
delivery date changes can cause mixed delivery dates within a lot. In the next sections of this document, the 
specific rules governing when a PID is converted, on day before delivery date (DD-1) or earlier, are explained. 

---

## Page 6

MBS [[Novation]]: Pool (PID) Conversion 
Version C ontrol Page 6 
2.  GENERIC TBA 
PIDs targeting generic TBA trades are converted to POIDs on the individual PIDs DD-12. 
Note: 
This conversion occurs as part of the 2pm Pool Net process or 4:30pm Pool Conversion Process (for PIDs with delivery 
date = NBD that missed daily pool net cycle 3). In addition, this conversion can occur intra -day when a pool DD is changed 
to current business day.  
2.1 GDM/Tail Lot Allocations 
Presume a [[Member]] allocates a GDM/Tail with 2 PIDs and then does a CC pushing out the DD on one of the 
pools. Each of these pools will be processed/converted to a POID on their individual DD-1, as shown below. 
Diagram 1: Generic TBA 
 
2.2 GDM/Tail Lot Allocations with SIFMA Exception 
An exception to the generic TBA conversion rule is when a [[Member]] requests a SIFMA exception allocation 
and/or CC to be processed4 that is ov er-variance and the DD within the lot are different. In this case, the PIDs 
in the lot are not converted individually, but rather converted at the same time on the minimum DD-1 of the 
pending PIDs in the lot (referred to as “lot level” DD-1). This is done to prevent the situation where a subset of 
the pools in the lot have earlier DD and reach within variance, thereby causing the TBA trade to be drawn 
prematurely as the pool(s) with later DD has not yet been processed. 
 
2 Note: bound [[Buyer]] and [[Seller]] PIDs are converted at the same time; in the situation where a late turnaround occurs ([[Buyer]] DD is a day later than [[Seller]] DD), 
the [[Buyer]] PID will be converted based on the [[Seller]] PID’s DD. 
3 This can occur due to operations DD update, or processing of DK on pre-net CC. 
4 Non-SIFMA compliant allocations and CC are accommodated at [[Member]]’s request through the assistance of [[FICC]] operations. 


---

## Page 7

MBS [[Novation]]: Pool (PID) Conversion 
Version C ontrol Page 7 
For example, presume a [[Member]] allocates a GDM/Tail with 3 PIDs and then does a CC pushing out the DD on 
one of the pools. A sub-set of the pools allocate the GDM/Tail within variance. Each of these pools will be 
processed/converted to a POID on a the minimum DD-1 of the pools within this lot, as shown below. 
Diagram 2: Generic TBA with Over-Variance SIFMA Exception 
 


---

## Page 8

MBS [[Novation]]: Pool (PID) Conversion 
Version C ontrol Page 8 
3.  STIP TRADES 
In contrast to generic TBA trades, PIDs targeting STIP trades are always converted to POIDs on the lot level 
DD-1. In other words, the PIDs are converted at the same time on the minimum DD-1 of PIDs in the lot5. 
Note: 
This conversion occurs as part of the  4:30pm Pool Conversion Process or intra -day when a pool DD is changed to current 
business day.  
3.1 GDM/Tail Lot Allocations 
Presume a [[Member]] allocates a GDM/Tail with 2 PIDs and then does a CC pushing out the DD on one of the 
pools. Each of these pools will be processed/converted to a POID on the minimum DD-1 of all PIDs in the lot, 
as shown below. 
Diagram 3: STIP Trade with GDM/Tail 
 
Note: 
Each GDM/Tail lot is treated separately, so that if multiple lots exist with overlapping DD, they are converted indi vidually 
and [[DO]] not impact each other.  
Continuing from example above, presume [[Member]] submits another GDMlot with a 3rd PID, which has same 
DD as the CC’ed pool. The PIDs in each lot will be processed/converted to POIDs as shown below. 
 
5 Note: bound [[Buyer]] and [[Seller]] PIDs are converted at the same time; in the situation where a late turnaround occurs ([[Buyer]] DD is a day later than [[Seller]] DD), 
the [[Buyer]] PID will be converted based on the [[Seller]] PID’s DD. 


---

## Page 9

MBS [[Novation]]: Pool (PID) Conversion 
Version C ontrol Page 9 
Diagram 4: STIP Trade with Multiple GDM/Tail 
 
3.2 Bidlist Allocations 
For bidlists (which are only applicable to STIPs), PID are also converted at the minimum DD-1 of all pending 
PIDs. However, it is important to note that a bidlist is considered a single large lot, regardless of the number of 
individual submissions (one or more 8888, followed by a single 8889) or number of days the bidlist spans. As 
such, when the DD in multiple bidlist submissions overlap, the conversion of PIDs in one submission may be 
triggered by the DD in a separate bidlist submission. 
Consider the previous example, but presume the submissions are part of a bidlist, rather than GDM lot. 
Note: 
2nd bidlist submission is converted based on DD -1 in 1st bidlist submission. This occurs regardless of whether th e 2nd 
submission is 8888, or 8889 (final submission).  


---

## Page 10

MBS [[Novation]]: Pool (PID) Conversion 
Version C ontrol Page 10 
Diagram 5: STIP Trade with Multiple Bidlist Submissions 
 
It’s important to note that the conversion rules for bidlists [[DO]] not affect GDM allocations; in other words, if a 
STIP is allocated with GDMs and bidlist, the GDMPIDs will be converted on minimum DD-1 within the GDM lot 
as usual and is not impacted by DD in the bidlist. 
Diagram 6: STIP Trade with GDM and Bidlist (GDM DD < Bidlist DD) 
 


---

## Page 11

MBS [[Novation]]: Pool (PID) Conversion 
Version C ontrol Page 11 
Diagram 7: STIP Trade with GDM and Bidlist (GDM DD > Bidlist DD) 
 
3.3 CC Processing 
In addition to converting PIDs to POIDs on DD-1 (or earlier) as part of the normal STIP pool conversion 
process (as described above), PIDs in a bidlist may converted to POIDs as part of CC processing under certain 
scenarios: 
1. Pools targeted in CC are mix of PIDs and POIDs in an open bidlist lot: CC processing requires that 
pools targeted in a CC are the same type; either all PIDs or all POIDs. When a CC targets a mix of PIDs 
and POIDs, the system will first convert the PIDs into POIDs (regardless of DD) and then perform the CC 
on the resulting POIDs
6. 
Note: 
Only bidlist “lots” can have a mix of DD – this occurs when a bidlist is submitted across multiple days, DD change 
and/or when a CC pushes out DD. As such, it is possible that at certain times a bidlist has a mix of both PIDs and 
POIDs. 
2. CC on finalized bidlist where bidlist is mix of PIDs and POIDs: When a CC occurs on a finalized bidlist 
lot (8889 received) and this lot is a mix of PIDs and POIDs, if the CC targets at least 1 POID, then all 
outstanding PIDs in the bidlist are converted to POIDs before the CC occurs. This occurs regardless of 
whether these PIDs were targeted for CC, or not. 
 
 
 
6 If the CC targets PIDs only, the PIDs are not converted, regardless of whether the associated bidlist is “mixed”. 


---

## Page 12

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 