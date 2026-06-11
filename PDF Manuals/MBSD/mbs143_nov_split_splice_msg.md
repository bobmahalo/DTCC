---
title: "MBS Novation: Split/Splice Messaging Overview"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs143_nov_split_splice_msg.pdf"
pages: 12
size: "587.4 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBS Novation: Split/Splice Messaging Overview

**Original File:** [mbs143_nov_split_splice_msg.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs143_nov_split_splice_msg.pdf)  
**Category:** MBSD  
**Total Pages:** 12  
**File Size:** 587.4 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
MBS [[Novation]]: SPLIT/SPLICE INTERACTIVE MESSAGING OVERVIEW 
VERSION 1.1 
JANUARY 11, 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Deposito ry Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
This document (the “Document”) is provided as a convenience to members and is for informational purposes only. The 
specific processe s and services referenced in this Document are subject to the U.S. [[securities]] and Exchange 
Commission’s approval of the Clearing Rules of the Mortgage -Backed [[securities]] Division (“MBSD”) of the Fixed Income 
Clearing Corporation (“[[FICC]]”).  
 
This Document should not be regarded as a definitive or exhaustive description of [[FICC]]/MBSD’s services or risk -
management framework; nor should it be regarded as a substitute for the Clearing Rules, which govern in all respects, the 
relationship between [[FICC]]/MBSD and its m embers. In all cases, members should refer to the Clearing Rules for a 
complete statement of [[FICC]]/MBSD procedures, [[obligations]], and requirements. Nothing in this Document shall be deemed 
to impose any [[obligations]] on [[FICC]]/MBSD that are not set forth in the Clearing Rules, and in the case of any discrepancy 
between this Document and the Clearing Rules, the Clearing Rules shall govern. The services and risk -management 
practices described in this Document may be amended at any time without prior notice.  
 
 
Doc Date: January 11, 2023 
Publication Code:  MBS143 
Service: Fixed Income Clearing Corporation 
Title: MBS [[Novation]] : Split/Splice Interactive Messaging Overview  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ....................................................................................................................... 4 
1. Split/Splice Processing Overview .................................................................................................. 5 
1.1 Splice Example ................................................................................................................ 5 
1.2 Split Example................................................................................................................... 5 
1.3 Combo ( Splice  an d Splice)  Exa mple.................................................................................... 6 
2. Split/Splice Messaging Overview ................................................................................................... 7 
2.1 Ex act Matc h Flo w ............................................................................................................. 8 
2.2 Splice Flow...................................................................................................................... 9 
2.3 Split Flow ...................................................................................................................... 10 
2.4 Combo (Split and Splice) Flow.......................................................................................... 11 
 

---

## Page 4

MBS [[Novation]]: Split/Splice Interactive Messaging Overview  
Version C ontrol Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change  
09/14/2016 1.0 C. Swords  Initial version  
n/a n/a [[DTCC]] Learning  Updated formatting only. Content is unchanged.  
01/11/2023 1.1 J.Sheeran  
 
 
Removed MBSD [[Novation]]  proposal overview  from 2017 
 
 
  

---

## Page 5

MBS [[Novation]]: Split/Splice Interactive Messaging Overview  
Version C ontrol Page 5 
1. SPLIT/SPLICE PROCESSING OVERVIEW 
A unique business practice associated with [[Broker]] trading is “ticket splitting and splicing.” This occurs when 
trades with matching terms submitted by a [[Broker]] and Dealer [[DO]] not match on par value on a trade- by-trade 
basis, but they [[DO]] match on a net par basis. In this case, “split-splice processing” occurs, which will “split” or 
“splice” the Dealer trades as necessary to match to the [[Broker]] trades. Specifically, MBSD will cancel the 
Dealer trades, and create new Dealer trades that exactly match the [[Broker]]’s submissions. SPT and STIP 
trades are excluded from split/splice processing. Examples help clarify this process. 
1.1 Splice Example 
A “splice” occurs when multiple dealer trades are matched against a single [[Broker]] trade. In this simple 
example, the following occurs: 
1. [[Broker]] B submits a trade where they buy 10MM from Dealer A and sells 10MM to Dealer C. 
2. Dealer A submits a sell of 6MM and 4MM. Neither trade exactly matches the [[Broker]] trade; however, the 
total par of 10MM (6+4) does match. 
3. The two dealer trades are combined (“spliced”) into a single trade by MBSD by cancelling the original 
trades submit by Dealer A, and automatically creating new trade for 10MM. 
4. The new trade of 10MM is now matched against the original [[Broker]] trade of 10MM. 
 
 
1.2 Split Example 
A “split” occurs when a single dealer trade is matched against multiple [[Broker]] trades. In this simple example, 
the following occurs: 
1. [[Broker]] B submits two trades, where they buy 3MM from Dealer A and sells to Dealer C, and another trade 
where they buy 2MM from Dealer A and sells to Dealer D. 
2. Dealer A submits a single sell of 5MM. This trade does not exactly match to either [[Broker]] trade; however, 
the total par of the [[Broker]]’s trades does match (3+2=5). 


---

## Page 6

MBS [[Novation]]: Split/Splice Interactive Messaging Overview  
Version C ontrol Page 6 
3. The dealer trade is “split” by MBSD by cancelling the original trade submit by Dealer A, and automatically 
creating two new trades of 3MM and 2MM. 
4. The new trades of 3MM and 2MM are now matched against the original [[Broker]] trades of equal par value. 
 
 
1.3 Combo (Splice and Splice) Example 
A “split/splice” or “combo” occurs when multiple dealer trades are matched against multiple [[Broker]] trades. This 
can get quite complex as both “split” and “splice” occurs in the same set of trades, as indicated in example 
below. 
 


---

## Page 7

MBS [[Novation]]: Split/Splice Interactive Messaging Overview  
Version C ontrol Page 7 
2. SPLIT/SPLICE MESSAGING OVERVIEW 
This section highlights certain messages/tags and how they are populated in a split/splice matching scenario.  
NOTE: 
As described, only dealer trades are split/ spliced –the [[Broker]] trades remain in original form and are not processed differently 
depending on type of match occurring. As such, the below refers to dealer messages only.  
Tag Type of Match Comment 
Exact Split Splice Combo 
MT509 Trade Matched  
COMM Yes No No No If the trade was matched via exact match, this message will 
have tag COMM that contains the RTTM assigned Trade [[ID]]. If 
matched via split/splice, this tag will NOT  be present.  
BASK Yes–if versus 
[[Broker]]  
Yes Yes Yes If the trade is matched against a [[Broker]], this message will have 
tag BASK that contains the “[[Broker]] match identifier” linking all 
[[Broker]] and dealer trades  together; noting that this could be an 
exact match (so only 1 dealer trade and 1 [[Broker]] trade will 
have same BASK) or split/splice match (so a set of dealer and  
[[Broker]] trades will have the same BASK).  
MAST Yes Yes Yes Yes This message will always have MAST that contains the 
[[Member]]-defined reference number (XREF) for the matched 
trade (e.g. original trade that was submitted by  [[Member]]) 
MT518 Comparison Request Advisory (due to match)  
CTRD Yes Yes Yes Yes This message will always have the CTRD tag that contains the 
RTTM assigned Trade [[ID]] associated with the (contra) trade 
that was matched (and therefore resulting in this advisory 
being canceled). It’s important to note that as RTTM Trade [[ID]] 
is the same between two matching parties, the Trade [[ID]] in this 
field is also the same as assigned to the recipient’s trade. 
NOTE: when a split/splice situation occurs and RTTM cancels 
dealers original trades and creates replacement trades to 
match the brokers, it is in th is CTRD tag that can get the  trade 
[[ID]] of the new dealer’s trades.  
BASK Yes–if versus 
[[Broker]]  
Yes Yes Yes BASK is present when associated with [[Broker]] trade, as 
described with MT509 Trade Matched.  
MAST No No No No MAST is not present.  
MT518 Trade Novated  
MAST Yes Yes No No MAST is present when there is a non- blank XREF on the 
trade. When this trade resulted from exact match, or split 
situation, the XREF is non- blank so will be returned in this 
MAST tag; when trade resulted from splice or combo match, 
the XREF is blank so this ta g is not present.  

---

## Page 8

MBS [[Novation]]: Split/Splice Interactive Messaging Overview  
Version C ontrol Page 8 
Tag Type of Match Comment 
Exact Split Splice Combo 
BASK Yes–if versus 
[[Broker]]  
Yes Yes Yes BASK is present when trade matched to [[Broker]], as described 
with MT509 Trade Matched.  
LIST Yes Yes Yes Yes LIST is always returned and will have RTTM Trade [[ID]] –noting 
that this is the same as returned in CTRD in the MT518 Cancel 
Request Cancel (due to match)  mentioned above.  
 
In the sections that follow, various messaging flows are shown, with the tags mentioned above highlighted. 
2.1 Exact Match Flow 
In this example, Dealer A submits one trade (50MM) that is matched to a single [[Broker]] trade (50MM), as 
follows: 
 


---

## Page 9

MBS [[Novation]]: Split/Splice Interactive Messaging Overview  
Version C ontrol Page 9 
Note: 
For exact match, as split/splice has not occurred, the BASK is assigned with the Trade [[ID]] value. In other words, 
SS1=TRD1, and SS2=TRD2. 
2.2 Splice Flow 
In this example, Dealer A submits two trades (30MM and 20MM) that are matched against a single [[Broker]] 
trade (50MM), as follows: 
 


---

## Page 10

MBS [[Novation]]: Split/Splice Interac tive Messaging Overview 
Version C ontrol Page 10 
2.3 Split Flow 
In this example, Dealer A submits one trade (50MM) that is matched against a two [[Broker]] trades (30MM and 
20MM), as follows: 
 


---

## Page 11

MBS [[Novation]]: Split/Splice Interactive Messaging Overview  
Version C ontrol Page 11 
2.4 Combo (Split and Splice) Flow 
In this example, Dealer A submits two trades (40MM and 10M) that are matched against a two [[Broker]] trades of 
different sizes (30MM and 20MM), as follows: 
 
 
 


---

## Page 12

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
Corelearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 