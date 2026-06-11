---
title: "MBS RTTM Novation: SWIFT Interactive Messaging Examples"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs161_mbsd_rttm_nov_msg_examples.pdf"
pages: 284
size: "2516.7 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBS RTTM Novation: SWIFT Interactive Messaging Examples

**Original File:** [mbs161_mbsd_rttm_nov_msg_examples.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs161_mbsd_rttm_nov_msg_examples.pdf)  
**Category:** MBSD  
**Total Pages:** 284  
**File Size:** 2516.7 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
MBSD RTTM® [[Novation]]: SWIFT INTERACTIVE MESSAGING EXAMPLES 
VERSION 1.02 
JULY 19, 2017 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: July 19, 2017 
Publication Code:  MBS161 
Service: Fixed Income Clearing Corporation 
Title: MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Examples  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ......................................................................................................................12  
1. Overview.....................................................................................................................................14  
1.1 Message Conventions..................................................................................................... 14 
1.2 General Changes ........................................................................................................... 14 
2. TBA Trade Samples .....................................................................................................................15  
2.1 Set 1 ............................................................................................................................ 18 
2.1.1 (01) MT515 Instruct ........................................................................................................ 18 
2.1.2 (02) MT509 Trade Create Accepted .................................................................................. 20 
2.1.3 (03) MT518 Comparison Request ..................................................................................... 20 
2.1.4 (04) MT515 Instruct ........................................................................................................ 22 
2.1.5 (05) MT509 Trade Create Accepted .................................................................................. 23 
2.1.6 (06) MT509 Trade Create Unbalanced............................................................................... 24 
2.1.7 (07) MT515 Instruct ........................................................................................................ 25 
2.1.8 (08) MT509 Trade Create Accepted .................................................................................. 26 
2.1.9 (09) MT509 Trade Create Unbalanced............................................................................... 27 
2.1.10 (10) MT509 Trade Create Balanced .................................................................................. 28 
2.1.11 (11) MT509 Trade Create Balanced .................................................................................. 29 
2.1.12 (12) MT518 Comparison Request ..................................................................................... 30 
2.1.13 (13) MT518 Comparison Request ..................................................................................... 31 
2.1.14 (14) MT509 Trade Create Matched ................................................................................... 33 
2.1.15 (15) MT509 Trade Create Matched ................................................................................... 34 
2.1.16 (16) MT509 PMAT (Long Side) ......................................................................................... 35 
2.1.17 (17) MT518 Comparison Request Cancel (due to Match)...................................................... 36 
2.1.18 (18) MT518 Comparison Request Cancel (due to Match)...................................................... 37 
2.1.19 (19) MT515 Instruct ........................................................................................................ 38 
2.1.20 (20) MT509 Trade Create Accepted .................................................................................. 40 
2.1.21 (21) MT518 Comparison Request ..................................................................................... 40 
2.1.22 (22) MT509 Trade Create Matched ................................................................................... 42 

---

## Page 4

 
 
2.1.23 (23) MT509 Trade Create Matched ................................................................................... 43 
2.1.24 (24) MT509 PMAT (Short Side) ........................................................................................ 44 
2.1.25 (25) MT518 Comparison Request Cancel (due to Match)...................................................... 45 
2.1.26 (26) MT518 Comparison Request Cancel (due to Match)...................................................... 46 
2.1.27 (27) MT509 FMAT .......................................................................................................... 48 
2.1.28 (28) MT518 Trade Novated .............................................................................................. 48 
2.1.29 (29) MT518 Trade Novated .............................................................................................. 50 
2.2 Set 2 ............................................................................................................................ 52 
2.2.1 (BRK MOD 19) MT515 Modify Set .................................................................................... 53 
2.2.2 (BRK MOD 20) MT509 Modify Set Accepted ...................................................................... 54 
2.2.3 (BRK MOD 21) MT509 Modify Set Processed .......................................................................... 55 
2.3 Set 3 ............................................................................................................................ 56 
2.3.1 (COM MOD 19) MT515 Modify ......................................................................................... 57 
2.3.2 (COM MOD 20) MT509 Modify Accepted ........................................................................... 58 
2.3.3 (COM MOD 21) MT509 Modify Processed............................................................................... 59 
2.3.4 (COM MOD 22) MT518 Comparison Request Modify (due to Contra) ..................................... 60 
2.4 Set 4 ............................................................................................................................ 62 
2.4.1 (CON MOD 19) MT515 Modify ......................................................................................... 63 
2.4.2 (CON MOD 20) MT509 Modify Accepted............................................................................ 64 
2.4.3 (CON MOD 21) MT509 Modify Processed .......................................................................... 65 
2.4.4 (CON MOD 22) MT518 Comparison Request Cancel (due to Contra) ..................................... 66 
2.4.5 (CON MOD 23) MT518 Comparison Request ..................................................................... 67 
2.5 Set 5 ............................................................................................................................ 69 
2.5.1 (DLR MOD 30) MT515 Modify .......................................................................................... 69 
2.5.2 (DLR MOD 31) MT509 Modify Accepted ................................................................................. 71 
2.5.3 (DLR MOD 32) MT509 Modify Processed................................................................................ 72 
2.6 Set 6 ............................................................................................................................ 73 
2.6.1 (DK INST 04) MT515 DK .................................................................................................  73 
2.6.2 (DK INST 05) MT509 DK Ac cep ted ................................................................................... 75 
2.6.3 (DK INST 06) MT518 Comparison Request Modify (due to DK) ............................................. 75 

---

## Page 5

 
 
2.6.4 (DK INST 07) MT518 DK Advice ....................................................................................... 76 
2.6.5 (DK INST 08) MT509 DK Processed ................................................................................. 78 
2.7 Set 7 ............................................................................................................................ 79 
2.7.1 (DK INST 19) MT515 DK .................................................................................................  80 
2.7.2 (DK INST 20) MT509 DK Ac cep ted ................................................................................... 81 
2.7.3 (DK INST 21) MT518 Comparison Request Modify (due to DK) ............................................. 82 
2.7.4 (DK INST 22) MT518 DK Advice ....................................................................................... 83 
2.7.5 (DK INST 23) MT509 DK Processed ................................................................................. 85 
2.8 Set 8 ............................................................................................................................ 86 
2.8.1 (BRK CAN 07) MT515 Cancel .......................................................................................... 86 
2.8.2 (BRK CAN 08) MT509 Cancel Accepted ............................................................................ 88 
2.8.3 (BRK CAN 09) MT509 Cancel Processed .......................................................................... 89 
2.9 Set 9 ............................................................................................................................ 90 
2.9.1 (BRK CAN 14) MT515 Cancel Set..................................................................................... 90 
2.9.2 (BRK CAN 15) MT509 Cancel Set Accepted....................................................................... 92 
2.9.3 (BRK CAN 16) MT509 Cancel Set Processed ..................................................................... 92 
2.9.4 (BRK CAN 17) MT518 Comparison Request Cancel (due to Contra) ...................................... 93 
2.9.5 (BRK CAN 18) MT518 Comparison Request Cancel (due to Contra) ...................................... 95 
2.10 Set 10........................................................................................................................... 97 
2.10.1 (BRK CAN 19) MT515 Canc el Set..................................................................................... 97 
2.10.2 (BRK CAN 20) MT509 Cancel Set Accepted....................................................................... 99 
2.10.3 (BRK CAN 21) MT518 Cancel Request.............................................................................100  
2.10.4 (BRK CAN 22) MT515 Cancel .........................................................................................101  
2.10.5 (BRK CAN 23) MT509 Cancel Accepted ...........................................................................103  
2.10.6 (BRK CAN 24) MT518 Cancel Request.............................................................................104  
2.10.7 (BRK CAN 25) MT509 Cancel Processed .........................................................................105  
2.10.8 (BRK CAN 26) MT509 Cancel Set Processed ....................................................................106  
2.10.9 (BRK CAN 27) MT518 Comparison Request Cancel (due to Contra) .....................................107  
2.11 Set 11..........................................................................................................................109  
2.11.1 (DLR CAN 04) MT515 Cancel .........................................................................................109  

---

## Page 6

 
 
2.11.2 (DLR CAN 05) MT509 Cancel Accepted ...........................................................................110  
2.11.3 (DLR CAN 06) MT509 Cancel Processed..........................................................................111  
2.11.4 (DLR CAN 07) MT518 Comparison Request Cancel (due to Contra) .....................................112  
2.12 Set 12..........................................................................................................................114  
2.12.1 (DLR CAN 30) MT515 Cancel .........................................................................................114  
2.12.2 (DLR CAN 31) MT509 Cancel Accepted ...........................................................................116  
2.12.3 (DLR CAN 32) MT518 Cancel Request ................................................................................117  
2.12.4 (DLR CAN 33) MT518 Cancel Request (Info).....................................................................118  
2.12.5 (DLR CAN 34) Cancel Remove via WFE...........................................................................120  
2.12.6 (DLR CAN 35) MT509 Cancel Lifted by [[participant]] .............................................................120  
2.12.7 (DLR CAN 36) MT518 Cancel Request Cancel (due to Contra) ............................................121  
2.12.8 (DLR CAN 37) MT518 Cancel Request Cancel (due to Contra) (Info) ....................................123  
2.13 Set 13..........................................................................................................................125  
2.13.1 (DK DLR CAN 34) MT515 DK (Cancel) .............................................................................125  
2.13.2 (DK DLR CAN 35) MT509 DK (Cancel) Accepted ...............................................................127  
2.13.3 (DK DLR CAN 36) MT509 DK (Cancel) Processed .............................................................128  
2.13.4 (DK DLR CAN 37) MT518 Cancel Request Modify (due to DK).............................................129  
2.13.5 (DK DLR CAN 38) MT518 DK (Cancel) Advice...................................................................130  
2.13.5 (DK DLR CAN 39) MT518 DK (Cancel) Advice (Info) ..........................................................132  
2.14 Set 14..........................................................................................................................134  
2.14.1 (REJ 02) MT509 Trade Create Rejected ...........................................................................134  
2.15 Set 15..........................................................................................................................135  
2.15.1 (REJ CAN 19) MT515 Cancel Set ....................................................................................136  
2.15.2 (REJ CAN 20) MT509 Cancel Set Rejected .......................................................................137  
2.16 Set 16..........................................................................................................................138  
2.16.1 (REJ CAN 30) MT515 Cancel..........................................................................................139  
2.16.2 (REJ CAN 31) MT509 Cancel Rejected ............................................................................140  
2.17 Set 17..........................................................................................................................141  
2.17.1 (REJ DK INST 04) MT515 DK .........................................................................................142  
2.17.2 (REJ DK INST 05) MT509 DK Rejected ............................................................................143  

---

## Page 7

 
 
2.18 Set 18..........................................................................................................................144  
2.18.1 (STIP 01) MT515 Instruct................................................................................................144  
2.18.2 (STIP 02) MT509 Trade Create Accepted .........................................................................145  
2.18.3 (STIP 03) MT518 Comparison Request ............................................................................146  
2.18.4 (STIP 04) MT515 Instruct................................................................................................147  
2.18.5 (STIP 05) MT509 Trade Create Accepted .........................................................................148  
2.18.6 (STIP 06) MT518 Comparison Request ............................................................................149  
2.18.7 (STIP 07) MT509 Trade Matched .....................................................................................150  
2.18.8 (STIP 08) MT509 Trade Matched .....................................................................................151  
2.18.9 (STIP 09) MT518 Comparison Request Cancel (due to Match) .............................................152  
2.18.10 (STIP 10) MT518 Comparison Request Cancel (due to Match) .........................................154  
2.18.11 (STIP 11) MT518 Trade Novated..................................................................................155  
2.18.12 (STIP 12) MT518 Trade Novated..................................................................................157  
2.19 Set 19..........................................................................................................................159  
2.19.1 (NETPOS 19) MT515 Instruct..........................................................................................160  
2.19.2 (NETPOS 20) MT509 Trade Create Accepted....................................................................161  
2.19.3 (NETPOS 21) MT518 Comparison Request.......................................................................162  
2.19.4 (NETPOS 22) MT515 Instruct..........................................................................................1 63 
2.19.5 (NETPOS 23) MT509 Trade Create Accepted....................................................................164  
2.19.6 (NETPOS 24) MT518 Comparison Request.......................................................................165  
2.19.7 (NETPOS 25) MT509 Trade Matched ...............................................................................166  
2.19.8 (NETPOS 26) MT509 Trade Matched ...............................................................................167  
2.19.9 (NETPOS 27) MT509 Trade Matched ...............................................................................167  
2.19.10 (NETPOS 28) MT509 Trade PMAT...............................................................................168  
2.19.11 (NETPOS 29) MT518 Comparison Request Cancel (due to match) ...................................168  
2.19.12 (NETPOS 30) MT518 Comparison Request Cancel (due to match) ...................................169  
2.19.13. (NETPOS 31) MT518 Comparison Request Cancel (due to match) ...................................170  
2.19.14. (NETPOS 32) MT509 Trade FMAT ...............................................................................170  
2.19.15. (NETPOS 33) MT518 Trade Novated............................................................................171  
2.19.16 (NETPOS 34) MT518 Trade Novated............................................................................171  

---

## Page 8

 
 
2.20 Set 20..........................................................................................................................173  
2.20.1 (OPT 01) MT515 Instruct ................................................................................................173  
2.20.2 (OPT 02) MT509 Trade Create Accepted ..........................................................................174  
2.20.3 (OPT 03) MT518 Comparison Request .............................................................................175  
3. Specified Pool Trade (SPT) Dealer Message Samples .................................................................. 177 
3.1 Set 1 ...........................................................................................................................178  
3.1.1 (01) MT515 Instruct .......................................................................................................178  
3.1.2 (02) M509 Trade Create Accepted ...................................................................................180  
3.1.3 (03) MT518 Comparison Request ....................................................................................180  
3.2 Set 2 ...........................................................................................................................182  
3.2.1 (DEFVAL 01) MT515 Instruct ..........................................................................................182  
3.2.2 (DEFVAL 02) MT509 Trade Create Accepted ....................................................................182  
3.2.3 (DEFVAL 03) MT518 [[default]] Values Applied .....................................................................183  
3.2.4 (DEFVAL 04) MT518 Compariso n Req ues t ............................................................................184  
3.3 Set 3 ...........................................................................................................................185  
3.3.1 (REP 04) MT518 Repricing .............................................................................................185  
3.4 Set 4 ...........................................................................................................................187  
3.4.1 (MKDL 04) MT518 Repricing ...........................................................................................187  
3.4.2 (MKDL 05) MT509 Trade Instruct Marked for Deletion.........................................................189  
3.4.3 (MKDL 06) MT518 Comparison Request Cancel (due to System) .........................................190  
3.5 Set 5 ...........................................................................................................................191  
3.5.1 POOLID (01) MT515 Instruct...........................................................................................192  
3.5.2 POOLID (02) MT509 Trade Create Accepted.....................................................................193  
3.5.3 POOLID (03) MT518 Comparison Request........................................................................193  
3.5.4 POOLID (04) MT515 Instruct...........................................................................................193  
3.5.5 POOLID (05) MT509 Trade Create Accepted.....................................................................195  
3.5.6 POOLID (06) MT518 Comparison Request........................................................................196  
3.5.7 POOLID (07) MT509 Trade Matched ................................................................................197  
3.5.8 POOLID (08) MT509 Trade Matched ................................................................................198  
3.5.9 POOLID (09) MT518 Comparison Request Cancel (due to Match) ........................................199  

---

## Page 9

 
 
3.5.10 POOLID (10) MT518 Comparison Request Cancel (due to Match) ........................................200  
3.5.11 POOLID (11) MT518 Trade Novated ................................................................................201  
3.5.12 POOLID (12) MT518 Trade Novated ................................................................................203  
3.6 Set 6 ...........................................................................................................................205  
3.6.1 (MKDL 13) MT518 Repricing ...........................................................................................205  
3.6.2 (MKDL 14) MT518 Repricing ...........................................................................................207  
3.6.3 (MKDL 15) MT509 Trade Instruct Marked for Deletion.........................................................208  
3.6.4 (MKDL 16) MT509 Trade Instruct Marked for Deletion.........................................................209  
4. Specified Pool Trade (SPT) [[Broker]]-to-Dealer Message Samples ................................................... 211 
4.1 Set 1 ...........................................................................................................................212  
4.1.1 (01) MT515 Instruct .......................................................................................................212  
4.1.2 (02) MT509 Trade Create Accepted .................................................................................214  
4.1.3 (03) MT509 Trade Unbalanced ........................................................................................215  
4.1.4 (04) MT515 Instruct .......................................................................................................216  
4.1.5 (05) MT509 Trade Create Accepted .................................................................................217  
4.1.6 (06) MT509 Trade Unbalanced ........................................................................................218  
4.1.7 (07) MT509 Trade Balanced............................................................................................219  
4.1.8 (08) MT509 Trade Balanced............................................................................................220  
4.1.9 (09) MT518 Comparison Request ....................................................................................221  
4.1.10 (10) MT518 Comparison Request ....................................................................................223  
4.1.11 (11) MT515 Instruct .......................................................................................................224  
4.1.12 (12) MT509 Trade Create Accepted .................................................................................225  
4.1.13 (13) MT518 Comparison Request ....................................................................................226  
4.1.14 (14) MT509 Trade Matched.............................................................................................227  
4.1.15 (15) MT509 Trade Matched.............................................................................................228  
4.1.16 (16) MT509 PMAT (Long Side) ........................................................................................229  
4.1.17 (17) MT518 Comparison Request Cancel (due to Match).....................................................230  
4.1.18 (18) MT518 Comparison Request Cancel (due to Match).....................................................232  
4.1.19 (19) MT518 Repricing ....................................................................................................233  
4.1.20 (20) MT518 Repricing ....................................................................................................235  

---

## Page 10

 
 
4.1.21 (21) MT518 Repricing ....................................................................................................237  
4.2 Set 2 ...........................................................................................................................239  
4.2.1 (DFLT VAL 01) MT515 Instruct ........................................................................................239  
4.2.2 (DFLT VAL 02) MT509 Trade Create Accepted ..................................................................241  
4.2.3 (DFLT VAL 03) MT509 Trade Unbalanced ........................................................................242  
4.2.4 (DFLT VAL 04) MT518 [[default]] Values Applied...................................................................243  
4.2.5 (DFLT VAL 05) MT515 Instruct ........................................................................................245  
4.2.6 (DFLT VAL 06) MT509 Trade Create Acc epted ..................................................................246  
4.2.7 (DFLT VAL 07) MT509 Trade Unbalanced ........................................................................247  
4.2.8 (DFLT VAL 08) MT518 [[default]] Values Applied...................................................................248  
4.2.9 (DFLT VAL 09) MT509 Trade Balanced ............................................................................250  
4.2.10 (DFLT VAL 10) MT509 Trade Balanced ............................................................................251  
4.2.11 (DFLT VAL 11) MT518 Comparison Request .....................................................................252  
4.2.12 (DFLT VAL 12) MT518 Comparison Request .....................................................................253  
4.3 Set 3 ...........................................................................................................................255  
4.3.1 (TRD DEL 19) MT518 Repricing ......................................................................................255  
4.3.2 (TRD DEL 20) MT518 Repricing ......................................................................................257  
4.3.3 (TRD DEL 21) MT518 Repricing ......................................................................................259  
4.3.4 (TRD DEL 22) MT509 Trade Instruct Marked for Deletion ....................................................260  
4.3.5 (TRD DEL 23) MT509 Trade Instruct Marked for Deletion ....................................................261  
4.3.6 (TRD DEL 24) MT509 Trade Instruct Marked for Deletion ....................................................262  
4.3.7 (TRD DEL 25) MT518 Comparison Request Cancel (due to System Action) ...........................263  
5. [[DO]] Not Allocate (DNA) Message Samples.................................................................................... 266 
5.1 Set 1 ...........................................................................................................................267  
5.1.1 (01) MT515 DNA ...........................................................................................................267  
5.1.2 (02) MT509 DNA Accepted .............................................................................................269  
5.1.3 (03) MT518 DNA Assigned .............................................................................................270  
5.2 Set 2 ...........................................................................................................................272  
5.2.1 (DNACAN 04) MT515 DNA Cancel ..................................................................................272  
5.2.2 (DNACAN 05) MT509 DNA Cancel Accepted ....................................................................273  

---

## Page 11

 
 
5.3 Set 3 ...........................................................................................................................275  
5.3.1 (TRDID 01) MT515 DNA................................................................................................. 275 
5.3.2 (TRDID 02) MT509 DNA Accepted...................................................................................277  
5.3.3 (TRDID 03) MT518 DNA Assigned ...................................................................................277  
5.4 Set 4 ...........................................................................................................................280  
5.4.1 (SCR 01) MT518 Screen Input Replay (DNA) ....................................................................280  
5.4.2 (SCR 02) MT518 Screen Input Replay (DNA Cancel)..........................................................281  
5.5 Set 5 ...........................................................................................................................282  
5.5.1 (DNA REJ 01) MT509 DNA Rejected................................................................................282  
5.5.2 (DNA REJ 02) MT509 DNA Cancel Rejected .....................................................................283  
 

---

## Page 12

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 12 
VERSION CONTROL PAGE 
Date Version # Name Description of Change  
2/24/2016 3.01 (1.0) MBSD Made following document formatting changes:  
• Converted document and flows into standard template and format  
• Incorporated SPT examples previously included in separate SWIFT 
RTTM document that were not covered by RTTM TBA examples.  
Made following enhancements to support [[Novation]]:  
• Added MT518 [[Novation]] for all flows related to  compared dealer/dealer, 
and FMAT [[Broker]]/dealer trades.  
• Reflect [[FICC]] as contra on messages post -[[Novation]]. 
• Added DNA message examples.  
• Added split/splice message examples.  
• Added [[Broker]] Match Identifier (BASK) tags for dealers matching 
against brokers.  
• Added STIP trade message examples.  
• Added support for new SPT pool identifiers.  
• Indicate that RTTM assigned Trade [[ID]] is no longer common between 
matching dealers (whether Dealer/Dealer, or [[Broker]]/Dealer).  
• As give -up is no longer necessary (as [[FICC]] becomes contra), all 
GUPP indicators in the Trade Processing Narrative (70E::TPRO) have 
been removed.  
Made following general changes:  
• Due to SWIFT changes, Standing Instructions Override 
(17B::STAN//N) is no longer required on the MT518 and as such, will 
be removed  
Made following corrections:  
• BRK MOD 2 where [[Broker]] modify their reference pre- balancing 
removed as this is not allowed.  
• Added Match Trade [[ID]] tag (20C::COMM) to MT509 match messages 
for TBA trades; was previously missing.  
• BRK MOD 4 where [[Broker]] modify their reference on FMAT trade 
removed as redundant to modify their reference on PMAT trade.  
4/1/2016 3.0.2 
(1.01) 
C. Swords  Made following changes:  
• Added 20C::MAST to MT518 Trade Novated messages where 
applicable – specifically message sample 28, 29, STIP 11, STIP 12, 
NETPOS 34, POOLID 11, POOLID 12.  
• Corrected Contra Reference 70E::DECL//GSCC/CTRD value in 
following message samples 26, STIP 09, STIP 10, POOLID 09, 
POOLID 10,NETPOS 29, NETPOS 30.  
• Removed 20C::COMM from MT509 PMAT messages in SPT (16)  
7/19/2017 1.0.2 C. Swords  Made following changes:  
• Update document to reflect that trade [[ID]]’s are not returned in MT518 
DNA Assigned message when DNA submitted via terms.  This affects 
Section 5.1 DNA Set 1, Section 5.1.3 (03) MT518 DNA Assigned and 
Section 5.3.3 (TRDID 03) MT518 DNA Assigned.  

---

## Page 13

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 13 
Date Version # Name Description of Change  
n/a n/a [[DTCC]] 
Learning  
Updated formatting only. Content is unchanged.  

---

## Page 14

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 14 
1. OVERVIEW 
In this document, multiple message samples are provided (referred to as “sets” of messages), where each set 
starts with a message flow diagram showing communication to/from members and RTTM, followed by specific 
examples of each message. 
Note: 
Each message sample provided correlates to a step from the flow diagram; for reference purposes, each message example 
will be identified by unique identifier, for example “(01)”, or “(TRDID 03)”.  
1.1 Message Conventions 
In the messages examples included in this document, several fields are set to [[default]] values, as indicated 
below:  
For MT515 messages: 
• Password: In the Message Header, the password must be set to the value assigned to the [[Member]] by 
MBS [[Novation]]. For the purposes of this document, the password is not shown; the value of <password> is 
displayed.  
 
For MT509 and MT518 messages:  
• Sender’s Message Reference: In the General Block (16R:GENL), the Sender’s Message Reference 
(20C::SEME) is a unique number generated by RTTM to uniquely identify each message. For the 
purposes of this document, a unique number will not be shown; the value of <nextsequence> is displayed.  
• Preparation Date/Time: In the General Block (16R:GENL), the Preparation Date/Time (98C::PREP) 
indicates that date and time the message was prepared by RTTM. For the purposes of this document, the 
date/time is not shown; the value of <prepdatetime> is displayed.  
Note: 
In all messages, the header (composed of the password, the sender, the message type and the receiver) should be 
regarded as one single field (formatted as a string with carriage returns where required).  However, these 4 data elements 
have been represented separately (i.e. one per line) in the message samples below in order to enhance their clarity.  
1.2 General Changes 
1. As flat commission is no longer supported, examples with flat rate commission were updated to reflect 
rate-based commission. This does not indicate a change to message format, but rather a change in 
example content only. 
2. As give-up is no longer necessary (as [[FICC]] becomes contra), all GUPP indicators in the Trade 
Processing Narrative (70E::TPRO) have been removed. 
3. Due to SWIFT changes, Standing Instructions Override (17B::STAN//N) is no longer required on the 
MT518 and, as such, will be removed. 

---

## Page 15

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 15 
2. TBA TRADE SAMPLES 
This section contains samples for TBA trades, including both [[Broker]] and dealer messages. The examples are 
based on the following: 
On March 6, 2001, [[Broker]] [[participant]] B (account “BRKB”) buys $5,000,000 of [[CUSIP]] 01F070633 from Dealer 
[[participant]] A (account “DLRA”) and sells the same $5,000,000 to Dealer [[participant]] C (account “DLRC”). Both 
trades are executed at a price of 99.125 and are to settle trade for trade (TFTD) for next day (March 7) 
[[settlement]] using Exact Match. [[Broker]] [[participant]] B charges a commission rate of 3/512 of a percent to Dealer 
[[participant]] A and 3/512 of a percent commission to Dealer [[participant]] C. 
The reference numbers used by the various parties to this trade, as well as those assigned by RTTM, are 
summarized in the grid below: 
Reference Numbers Dealer [[participant]] A 
(account “DLRA”)  
[[Broker]] [[participant]] B 
(account “BRKB”)  
Dealer [[participant]] C 
(account “DLRC”)  
Sender’s Reference SENREFDLRA015 SENREFBKRB0221 (buy)  
SENREFBKRB0222 (sell)  
SENREFDLRC0331 
X-REF XREFDLRA001 XREFBKBR021B (buy)  
XREFBKRB021S (sell)  
XREFDLRC001 
[[Broker]] Reference N/A BREF021 N/A 
[[Broker]] Match Identifier  BMID001 N/A BMID002 
RTTM Submission [[ID]]  N/A 000001-1306 (buy)  
000002-1306 (sell)  
N/A 
RTTM Transaction [[ID]]  7096000001 7096000002 7096000003 
RTTM Trade [[ID]]  2049000001 2049000002 
 
Based on these trade details, different scenarios below have been constructed. Each of these scenarios is 
illustrated by a series of message samples, which represent a “flow” of events. The grid below describes each 
of these scenarios and indicates which sequence of message samples corresponds to a given scenario: 
 Scenario Message Sequence 
1 Dealer A submits their  sell, then [[Broker]] B submits both legs of their  trade and finally 
Dealer C submits their  buy. The trade is fully matched and novated.  
(01) - (29) 
2 Dealer A submits their  sell, then [[Broker]] B submits both legs of their  trade with an 
erroneous [[Broker]] Reference. After the trade has been partially matched, [[Broker]] B 
modifies the [[Broker]] Reference on their  trade. 
(01) - (18) 
and  
BRK MOD (19) - (21) 
3 Dealer A submits their  sell, then [[Broker]] B submits both legs of their  trade but they 
indicate an erroneous commission for their  sell side to Dealer C. [[Broker]] B modifies 
the commission on the unmatched (i.e. short) side of the partially matched trade.  
(01) - (18) 
and  
COM MOD (19 ) - (22) 

---

## Page 16

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 16 
 Scenario Message Sequence 
4 Dealer A submits their  sell, then [[Broker]] B submits both legs of their  trade but they 
erroneously indicate Dealer C instead of Dealer D for their  sell side. [[Broker]] B 
modifies the contra -party on the unmatched (i.e. short) side of the partially m atched 
trade. 
(01) - (18) 
and  
CON MOD (19) - (23) 
5 Dealer A submits their  sell with an erroneous x -ref and then [[Broker]] B and Dealer C 
submit their trades. Dealer A modifies their  x-ref post-comparison/[[Novation]]. 
(01) - (29) 
and  
DLR MOD (28) – (30) 
6 Dealer A submits their  sell, but [[Broker]] B DK’s Dealer A’s Comparison Request.  (01) - (03) 
and  
DK INST (04) - (08) 
7 Dealer A submits their  sell, then [[Broker]] B submits both legs of their  trade but Dealer 
C DK’s [[Broker]] B’s Comparison Request.  
(01) - (18) 
and  
DK INST (19) - (23) 
8 [[Broker]] B submits the buy side of their  trade and then cancels this leg pre -balancing.  (04) - (06) 
and  
BRK CAN (07) - (09) 
9 [[Broker]] B submits both sides of their  trade and then cancels this balanced set of 
submissions post -balancing but pre-comparison.  
(04) - (13) 
and  
BRK CAN (14) - (18) 
10 Dealer A submits their  sell and then [[Broker]] B submits both legs of their  trade. This 
partially matched trade is then canceled bilaterally by [[Broker]] B and Dealer A.  
(01) - (18) 
and  
BRK CAN (19) - (27) 
11 Dealer A submits their  sell and then cancels it pre - comparison.  (01) - (03) 
and  
DLR CAN (04) - (07) 
12 Dealer A submits their  sell and then [[Broker]] B and dealer C submit their trades. 
Dealer A submits a Cancel message for this fully matched and novated trade, but 
before any contra- party reacts, A removes their  Cancel message (“un -cancels”) via 
WFE. 
(01) ) - (29) 
and  
DLR CAN (30) - (37) 
13 Dealer A submits their  sell and then [[Broker]] B and dealer C submit their trades. 
Dealer A submits a Cancel message for this fully matched  and novated trade, but 
Dealer C DK’s Dealer A’s Cancel Request.  
(01) - (29) 
and  
DLR CAN (30) - (33) 
and  
DK DLR CAN (34) - (39) 
14 Dealer A submits their  sell using an external reference number that is not unique 
(they have already used this reference number previously for a message that is 
currently on the system). As a result, the message is rejected by RTTM.  
(01) 
and  
REJ (02) 
15 Dealer A submits their  sell and then [[Broker]] B submits both legs of their  trade. [[Broker]] 
B submits a Cancel Set message in order to cancel this partially matched trade, but 
this message is rejected by RTTM as [[Broker]] B uses an incorrect password.  
(01) - (18) 
and  
REJ CAN (19) - (20) 
16 Dealer A submits their  sell and then [[Broker]] B and dealer C submit their trades. After 
the trade has been fully matched  and novated, Dealer A submits a Cancel message 
using an incorrect password – as a result, RTTM rejects A’s Cancel message.  
(01) - (29) 
and  
REJ CAN (30) - (31) 

---

## Page 17

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 17 
 Scenario Message Sequence 
17 Dealer A submits t heir  sell, but [[Broker]] B DK’s Dealer A’s  Comparison Request. 
[[Broker]] B’s DK message is rejected by RTTM because the trade is not found ([[Broker]] 
B supplied an incorrect contra transaction reference).  
(01) - (03) 
and  
REJ DK INST (04) - (05) 
 
In addition to the scenarios above that all relate to TFTD (trade for trade) trades, the scenario below has been 
added for Stipulated Pool Trades (STIP). 
 Scenario Message Sequence 
18 Dealer A submits their  sell for a STIP trade, and Dealer C submits a matching trade. 
The trades are matched and novated.  
STIP (01) - (12) 
 
In order to show a split/splice scenario, assume Dealer A and [[Broker]] B submit trades as previously indicated of 
par value $5,000,000. However, Dealer C submits two trades, one of $3,000,000 and one of $2,000,000. 
Dealer A and [[Broker]] B trades are exactly matched (as previously shown), however, Dealer C and [[Broker]] B are 
matched via split/splice. 
 Scenario Message Sequence 
19 Dealer A and [[Broker]] B submit trades of the same terms and par value and they 
match, resulting in a PMAT [[Broker]] trade. Dealer C then submits multiple trades that 
are matched against the [[Broker]] trade via Split/Splice, resulting in a FMAT [[Broker]] 
trade. 
(01) – (18) 
and 
NETPOS (19) – (34) 
 
In addition to the scenarios above, the scenario below has been added that relates to an OPTN ([[Option]]) trade. 
 Scenario Message Sequence 
20 On March 21, 2001, Dealer A submits a Trade Create to RTTM for a sell of a put 
[[Option]] to dealer C. RTTM sends a Trade Create Accepted to Dealer A and a 
Comparison Request to Dealer C.  
OPT (01) - (03) 

---

## Page 18

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples 
Version C ontrol Page 18 
2.1 Set 1 
In this set, the following messages are included. 
[[Broker]] B [[Broker]] B
5d.
MT518 Comparison Request
[[Broker]] B
(06)
MT509 Trade Create Unbalanced
(10)
MT509 Trade Create Balanced
(05)
MT509 Trade Create Accepted
(08)
MT
509 Trade Create Accepted
(09)
MT
509  Trade Create Unbalanced
(11)
MT
509 Trade Create Balanced
(04)
MT
515 Instruct (vs. A)
(07) 
MT
515 Instruct (vs. C)
Dealer A
(12)
MT
518 Comparison Request
(02)
MT
509 Trade Create Accepted
(14)
MT
509 Trade Create Matched
(17)
MT
518 Comparison Request 
Cancel (due to match)
(03)
MT
518 Comparison Request
(15)
MT
509 Trade Create Matched
(16)
MT
509 Trade PMAT (long side)
(18)
MT
518 Comparison Request 
Cancel (due to match)
(01) 
MT
515 Instruct
(13)
MT
518 Comparison Request
[[Broker]] BDealer C
(20)
MT
509 Trade Create Accepted
(22)
MT
509 Trade Create Matched
(25)
MT
518 Comparison Request 
Cancel (due to match)
(21)
MT
518 Comparison Request
(23)
MT
509 Trade Create Matched
(24)
MT
509 Trade PMAT (short side)
(26)
MT
518 Comparison Request 
Cancel (due to match)
(19) 
MT
515 Instruct
RTTM
(27)
MT
509 Trade FMAT
(29)
MT
518 Trade Novated
(28)
MT
518 Trade Novated
 
Scenario Message Sequence 
Dealer A submits their  sell, then [[Broker]] B submits both legs of their  trade and finally 
Dealer C submits their  buy. The Trade is fully matched and novated  
(01) - (29) 
2.1.1 (01) MT515 Instruct 
MESSAGE SAMPLE (01) MT515 Dealer A Submits Sell to RTTM  FIELD DESCRIPTION 
PSSWRD123 Password  
DLRA Sender  

---

## Page 19

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 19 
MESSAGE SAMPLE (01) MT515 Dealer A Submits Sell to RTTM  FIELD DESCRIPTION 
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA015 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306100526 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing  
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative Trade 
Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 

---

## Page 20

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 20 
2.1.2 (02) MT509 Trade Create Accepted 
MESSAGE SAMPLE (02) MT509  
Trade Create Accepted sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM005 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306100913 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA015 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.1.3 (03) MT518 Comparison Request 
MESSAGE SAMPLE (03) MT518  
Comparison Request for Matching Buy sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  

---

## Page 21

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 21 
MESSAGE SAMPLE (03) MT518  
Comparison Request for Matching Buy sent to [[Broker]] B  
FIELD DESCRIPTION 
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM006 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306100952 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 

---

## Page 22

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 22 
2.1.4 (04) MT515 Instruct 
MESSAGE SAMPLE (04) MT515  
[[Broker]] B Submits Buy (Long Side) to RTTM  
FIELD DESCRIPTION 
PSSWRD234 Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0221 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306103913 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing  Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU  Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  

---

## Page 23

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 23 
MESSAGE SAMPLE (04) MT515  
[[Broker]] B Submits Buy (Long Side) to RTTM  
FIELD DESCRIPTION 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative Trade 
Service Type - Trade for Trade  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.1.5 (05) MT509 Trade Create Accepted 
MESSAGE SAMPLE (05) MT509  
Trade Create Accepted sent to [[Broker]] B (Long Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM007 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306103938 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0221 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 

---

## Page 24

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version Control Page 24 
MESSAGE SAMPLE (05) MT509  
Trade Create Accepted sent to [[Broker]] B (Long Side)  
FIELD DESCRIPTION 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.1.6 (06) MT509 Trade Create Unbalanced 
MESSAGE SAMPLE (06) MT509  
Transaction Unbalanced sent to [[Broker]] B (Long Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM008 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306103940 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  

---

## Page 25

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 25 
MESSAGE SAMPLE (06) MT509  
Transaction Unbalanced sent to [[Broker]] B (Long Side)  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TUNB Trade Create Unbalanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.1.7 (07) MT515 Instruct 
MESSAGE SAMPLE (07) MT515  
[[Broker]] B Submits Sell (Short Side) to RTTM  
FIELD DESCRIPTION 
PSSWRD234 Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0222 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104038 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 

---

## Page 26

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 26 
MESSAGE SAMPLE (07) MT515  
[[Broker]] B Submits Sell (Short Side) to RTTM  
FIELD DESCRIPTION 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing  Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative Trade 
Service Type - Trade for Trade  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.1.8 (08) MT509 Trade Create Accepted 
MESSAGE SAMPLE (08) MT509  
Trade Create Accepted sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM009 Sender’s RTTM Reference for this  Message 

---

## Page 27

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 27 
MESSAGE SAMPLE (08) MT509  
Trade Create Accepted sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104119 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0222 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000002-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.1.9 (09) MT509 Trade Create Unbalanced 
MESSAGE SAMPLE (09) MT509  
Transaction Unbalanced sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM010 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104121 Preparation Date/Time 

---

## Page 28

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 28 
MESSAGE SAMPLE (09) MT509  
Transaction Unbalanced sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000002-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TUNB Trade Create Unbalanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.1.10 (10) MT509 Trade Create Balanced 
MESSAGE SAMPLE (10) MT509  
Transaction Balanced sent to [[Broker]] B (Long Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM011 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104124 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//000001-1306 Previous Submission Reference 

---

## Page 29

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 29 
MESSAGE SAMPLE (10) MT509  
Transaction Balanced sent to [[Broker]] B (Long Side)  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TBAL Trade Create Balanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.1.11 (11) MT509 Trade Create Balanced 
MESSAGE SAMPLE (11) MT509  
Transaction Balanced sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM012 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104125 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//000002-1306 Previous Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 

---

## Page 30

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 30 
MESSAGE SAMPLE (11) MT509  
Transaction Balanced sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TBAL Trade Create Balanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.1.12 (12) MT518 Comparison Request 
MESSAGE SAMPLE (12) MT518  
Comparison Request for Matching Sell sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM013 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104126 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  

---

## Page 31

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 31 
MESSAGE SAMPLE (12) MT518  
Comparison Request for Matching Sell sent to Dealer A  
FIELD DESCRIPTION 
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:20C::PROC//7096000002 [[Buyer]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative Trade 
Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.1.13 (13) MT518 Comparison Request 
MESSAGE SAMPLE (13) MT518  
Comparison Request for Matching Buy sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM014 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  

---

## Page 32

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 32 
MESSAGE SAMPLE (13) MT518  
Comparison Request for Matching Buy sent to Dealer C  
FIELD DESCRIPTION 
:98C::PREP//20010306104127 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative Trade 
Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 33

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 33 
2.1.14 (14) MT509 Trade Create Matched 
MESSAGE SAMPLE (14) MT509  
Transaction Matched sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM015 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104136 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BMID001 [[Broker]] Match Identifier  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//2049000001 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 34

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 34 
2.1.15 ( 15) MT509 Trade Create Matched 
MESSAGE SAMPLE (15) MT509  
Transaction Matched sent to [[Broker]] B (Long Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM016 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104138 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//2049000001 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 35

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 35 
2.1.16 (16) MT509 PMAT (Long Side) 
MESSAGE SAMPLE (16) MT509  
Trade Partially Matched (Long Side) sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM017 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104139 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//7096000002 Previous Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH/GSCC/MAPL Trade Partially Matched - Long Side 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 36

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 36 
2.1.17 ( 17) MT518 Comparison Request Cancel (due to Match) 
MESSAGE SAMPLE (17) MT518  
Comparison Request Cancel (due to Match) sent to Dealer A  
FIELD DESCRIPTION 
 Password 
MBSCTRRS Sender 
518/000/GSCC Message Type 
DLRA Receiver 
:16R:GENL Mandatory Block Start 
:20C::SEME//SENREFRTTM018 Sender’s RTTM Reference for this message 
:23G:CANC Message Function = Cancel 
:98C::PREP//20010306104142 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BMID001 [[Broker]] Match Identifier 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CADV Comparison Request Cancel 
:22H::PAYM//APMT Against Payment Indicator 
:22F::CATB//PERU Per Unit Charges Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:20C::PROC//7096000002 [[Buyer]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000001 [[participant]] Declaration Details Narrative [[Buyer]] 
(Contra) Trade Reference 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]] 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par) 

---

## Page 37

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 37 
MESSAGE SAMPLE (17) MT518  
Comparison Request Cancel (due to Match) sent to Dealer A  
FIELD DESCRIPTION 
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRMACH Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Match 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO Indicator = Reporting Purposes 
:16R:AMT Optional Block Start 
:19A::LOCO//USD292,97 Commission Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.1.18 ( 18) MT518 Comparison Request Cancel (due to Match) 
MESSAGE SAMPLE (18) MT518 Comparison Request Cancel 
(due to Match) sent to [[Broker]] B (Long Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM019 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104143 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 

---

## Page 38

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 38 
MESSAGE SAMPLE (18) MT518 Comparison Request Cancel 
(due to Match) sent to [[Broker]] B (Long Side)  
FIELD DESCRIPTION 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000001 [[participant]] Declaration Details Narrative [[Seller]] 
(Contra) Trade Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRMACH Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
- End of Message 
2.1.19 (19) MT515 Instruct 
MESSAGE SAMPLE (19) MT515  
Dealer C Submits Buy to RTTM 
FIELD DESCRIPTION 
PSSWRD345 Password  
DLRC Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRC0331 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104702 Preparation Date/Time 

---

## Page 39

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 39 
MESSAGE SAMPLE (19) MT515  
Dealer C Submits Buy to RTTM 
FIELD DESCRIPTION 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 40

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 40 
2.1.20 (20) MT509 Trade Create Accepted 
MESSAGE SAMPLE (20) MT509  
Trade Create Accepted sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM020 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104729 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRC0331 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000003 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged  / Validated 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.1.21 (21) MT518 Comparison Request 
MESSAGE SAMPLE (21) MT518  
Comparison Request for Matching Sell sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  

---

## Page 41

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 41 
MESSAGE SAMPLE (21) MT518  
Comparison Request for Matching Sell sent to [[Broker]] B  
FIELD DESCRIPTION 
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM021 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104743 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000003 [[Buyer]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 

---

## Page 42

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 42 
MESSAGE SAMPLE (21) MT518  
Comparison Request for Matching Sell sent to [[Broker]] B  
FIELD DESCRIPTION 
:16S:SETDET Block End 
- End of Message 
2.1.22 (22) MT509 Trade Create Matched 
MESSAGE SAMPLE (22) MT509  
Transaction Matched sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM022 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104746 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000003 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BMID002 [[Broker]] Match Identifier  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//2049000002 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 43

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 43 
2.1.23 (23) MT509 Trade Create Matched 
MESSAGE SAMPLE (23) MT509  
Transaction Matched sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM023 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104748 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//2049000001 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 44

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 44 
2.1.24 (24) MT509 PMAT (Short Side) 
MESSAGE SAMPLE (24) MT509  
Trade Partially Matched (Short Side) sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM024 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104750 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//7096000002 Previous Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH/GSCC/MAPS Trade Partially Matched - Short Side 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 45

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 45 
2.1.25 ( 25) MT518 Comparison Request Cancel (due to Match) 
MESSAGE SAMPLE (25) MT518 Comparison Request Cancel 
(due to Match) sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM025 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104753 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000003 [[Buyer]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000001 [[participant]] Declaration Details Narrative 
[[Buyer]] (Contra) Trade Reference 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 

---

## Page 46

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 46 
MESSAGE SAMPLE (25) MT518 Comparison Request Cancel 
(due to Match) sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRMACH Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.1.26 ( 26) MT518 Comparison Request Cancel (due to Match) 
MESSAGE SAMPLE (26) MT518  
Comparison Request Cancel (due to Match) sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM026 Sender’s RTTM Reference for this message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104755 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BMID002 [[Broker]] Match Identifier  
:16S:LINK Repeat Block End 

---

## Page 47

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 47 
MESSAGE SAMPLE (26) MT518  
Comparison Request Cancel (due to Match) sent to Dealer C  
FIELD DESCRIPTION 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000002 [[participant]] Declaration Details Narrative 
[[Seller]] (Contra) Trade Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD /MSGRMACH  Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 48

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 48 
2.1.27 (27) MT509 FMAT 
MESSAGE SAMPLE (27) MT509  
Trade Fully Matched sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM027 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104801 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH/GSCC/MAFM Trade Fully Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.1.28 ( 28) MT518 Trade Novated 
MESSAGE SAMPLE (28) MT518  [[Novation]] for Dealer A  FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM021 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  

---

## Page 49

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 49 
MESSAGE SAMPLE (28) MT518  [[Novation]] for Dealer A  FIELD DESCRIPTION 
:98C::PREP//20010306104743 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 List Reference Number  (trade [[ID]])  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BMID001 [[Broker]] Match Identifier  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/NOVT [[Novation]] Advice 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTFTBA Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  

---

## Page 50

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 50 
MESSAGE SAMPLE (28) MT518  [[Novation]] for Dealer A  FIELD DESCRIPTION 
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.1.29 ( 29) MT518 Trade Novated 
MESSAGE SAMPLE (29) MT518  [[Novation]] for Dealer C  FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM021 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104743 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000002 List Reference Number  (trade [[ID]])  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BMID002 [[Broker]] Match Identifier  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 

---

## Page 51

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 51 
MESSAGE SAMPLE (29) MT518  [[Novation]] for Dealer C  FIELD DESCRIPTION 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/NOVT [[Novation]] Advice 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTFTBA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 52

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 52 
2.2 Set 2 
In this set, the following messages are included (shaded in gray). 
[[Broker]] B [[Broker]] B
[[Broker]] B
(06)
MT509 Trade Create Unbalanced
(10)
MT509 Trade Create Balanced
(05)
MT509 Trade Create Accepted
(08)
MT509 Trade Create Accepted
(09)
MT509  Trade Create Unbalanced
(11)
MT509 Trade Create Balanced
(04)
MT515 Instruct (vs. A)
(07) 
MT515 Instruct (vs. C)
Dealer A
(12)
MT518 Comparison Request
(02)
MT509 Trade Create Accepted
(14)
MT509 Trade Create Matched
(17)
MT518 Comparison Request 
Cancel (due to match)
(03)
MT518 Comparison Request
(15)
MT509 Trade Create Matched
(16)
MT509 Trade PMAT (long side)
(18)
MT518 Comparison Request 
Cancel (due to match)
(01) 
MT515 Instruct
(13)
MT518 Comparison Request
Dealer C
RTTM
BRK MOD (19) 
MT515 Modify Set
BRK MOD (20) 
MT509 Modify Set Accepted
BRK MOD (21) 
MT509 Modify Set Processed
 
Description Message Sequence 
Dealer A submits their  sell, then [[Broker]] B submits both legs of their  trade with an 
erroneous [[Broker]] Reference. After the trade has been partially matched, [[Broker]] B modifies 
the [[Broker]] Reference on their  trade. 
(01) - (18) 
and  
BRK MOD (19) - (21) 
 
Note: 
The messages are the same if the [[Broker]] modified their reference on a fully matched trade.  

---

## Page 53

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 53 
2.2.1 (BRK MOD 19) MT515 Modify Set 
MESSAGE SAMPLE (BRK MOD 19) MT515  
[[Broker]] B Modifies [[Broker]] Ref for PMAT Trade  
FIELD DESCRIPTION 
PSSWRD234 Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0441 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104528 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//BREF021 Previous [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF921 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/MDSE Modify Set Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 

---

## Page 54

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 54 
MESSAGE SAMPLE (BRK MOD 19) MT515  
[[Broker]] B Modifies [[Broker]] Ref for PMAT Trade  
FIELD DESCRIPTION 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade  
:16S:CONFDET Block End 
- End of Message 
2.2.2 (BRK MOD 20) MT509 Modify Set Accepted 
MESSAGE SAMPLE (BRK MOD 20) MT509 Modify Set 
Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM020 Sender’s RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104530 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::PREV//BREF021 Previous [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0441 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF921 [[Broker]] Reference Number  

---

## Page 55

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 55 
MESSAGE SAMPLE (BRK MOD 20) MT509 Modify Set 
Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/PAMS Modify Set Accepted  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.2.3 (BRK MOD 21) MT509 Modify Set Processed 
MESSAGE SAMPLE(BRK MOD 21) MT509 Modify Set 
Processed sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM021 Sender’s RTTM Reference for this message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104532 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::PREV//BREF021 Previous [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF921 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/YPPR Modify Set Processed  
:16S:STAT Repeat Block End 

---

## Page 56

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 56 
MESSAGE SAMPLE(BRK MOD 21) MT509 Modify Set 
Processed sent to [[Broker]] B  
FIELD DESCRIPTION 
:16S:GENL Block End 
- End of Message 
2.3 Set 3 
In this set, the following messages are included (shaded in gray). 
[[Broker]] B [[Broker]] B
[[Broker]] B
(06)
MT
509 Trade Create Unbalanced
(10)
MT
509 Trade Create Balanced
(05)
MT
509 Trade Create Accepted
(08)
MT
509 Trade Create Accepted
(09)
MT
509  Trade Create Unbalanced
(11)
MT
509 Trade Create Balanced
(04)
MT
515 Instruct (vs. A)
(07) 
MT
515 Instruct (vs. C)
Dealer A
(12)
MT
518 Comparison Request
(02)
MT
509 Trade Create Accepted
(14)
MT
509 Trade Create Matched
(17)
MT
518 Comparison Request 
Cancel (due to match)
(03)
MT
518 Comparison Request
(15)
MT
509 Trade Create Matched
(16)
MT
509 Trade PMAT (long side)
(18)
MT
518 Comparison Request 
Cancel (due to match)
(01) 
MT
515 Instruct
(13)
MT
518 Comparison Request
Dealer C
RTTM
COM MOD (19) 
MT
515 Modify
COM MOD (20) 
MT
509 Modify Accepted
COM MOD (21) 
MT
509 Modify Processed
COM MOD (22) 
MT
518 Comparison Request 
Modify (due to Contra)
 
Description Message Sequence 
Dealer A submits their  sell, then [[Broker]] B submits both legs of their  trade but they indicate 
an erroneous commission for their  sell side to Dealer C. [[Broker]] B modifies the commission 
on the unmatched (i.e. short) side of the partially matched trade.  
(01) - (18) 
and  
COM MOD (19) - (22) 

---

## Page 57

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 57 
2.3.1 (COM MOD 19) MT515 Modify 
MESSAGE SAMPLE (COM MOD 19) MT515 [[Broker]] B Modifies 
Commission on Unmatched Side of PMAT Trade  
FIELD DESCRIPTION 
PSSWRD234 Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0223 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104451 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Referenc e 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/MDFC Modify Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 

---

## Page 58

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 58 
MESSAGE SAMPLE (COM MOD 19) MT515 [[Broker]] B Modifies 
Commission on Unmatched Side of PMAT Trade  
FIELD DESCRIPTION 
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.3.2 (COM MOD 20) MT509 Modify Accepted 
MESSAGE SAMPLE(COM MOD 20) MT509  
Modify Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM020 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104453 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0223 Related Reference Number (sender’s reference)  

---

## Page 59

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 59 
MESSAGE SAMPLE(COM MOD 20) MT509  
Modify Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/MODA Modify Accepted 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.3.3 (COM MOD 21) MT509 Modify Processed 
MESSAGE SAMPLE (COM MOD 21) MT509 Modify Processed 
sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM021 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104454 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 

---

## Page 60

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 60 
MESSAGE SAMPLE (COM MOD 21) MT509 Modify Processed 
sent to [[Broker]] B  
FIELD DESCRIPTION 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/MODP Modify Processed 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.3.4 (COM MOD 22) MT518 Comparison Request Modify (due to Contra) 
MESSAGE SAMPLE (COM MOD 22) MT518  Comparison 
Request Modify (due to Contra) sent to Dealer C.  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM022 Sender’s RTTM Reference for this message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104456 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CRQM Comparison Request Modify  

---

## Page 61

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 61 
MESSAGE SAMPLE (COM MOD 22) MT518  Comparison 
Request Modify (due to Contra) sent to Dealer C.  
FIELD DESCRIPTION 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD /MSGRCOAC  Trade Instruction Processing Narrative Trade 
Service Type - Trade for Trade 
Message Reason - Due to Contra Action 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 62

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 62 
2.4 Set 4 
In this set, the following messages are included (shaded in gray). 
[[Broker]] B [[Broker]] B
[[Broker]] B
(06)
MT509 Trade Create Unbalanced
(10)
MT509 Trade Create Balanced
(05)
MT509 Trade Create Accepted
(08)
MT509 Trade Create Accepted
(09)
MT509  Trade Create Unbalanced
(11)
MT
509 Trade Create Balanced
(04)
MT
515 Instruct (vs. A)
(07) 
MT
515 Instruct (vs. C)
Dealer A
(12)
MT
518 Comparison Request
(02)
MT
509 Trade Create Accepted
(14)
MT
509 Trade Create Matched
(17)
MT
518 Comparison Request 
Cancel (due to match)
(03)
MT
518 Comparison Request
(15)
MT
509 Trade Create Matched
(16)
MT
509 Trade PMAT (long side)
(18)
MT
518 Comparison Request 
Cancel (due to match)
(01) 
MT
515 Instruct
(13)
MT
518 Comparison Request
Dealer C
RTTM CON MOD (19) 
MT
515 Modify
CON MOD (20) 
MT
509 Modify Accepted
CON MOD (21) 
MT
509 Modify Processed
CON MOD (22) 
MT
518 Comparison Request 
Cancel (due to Contra)
Dealer D
CON MOD (23) 
MT
518 Comparison Request
 
Description Message Sequence 
Dealer A submits their  sell, then [[Broker]] B submits both legs of their  trade but they erroneou sly 
indicate Dealer C instead of Dealer D for their  sell side. [[Broker]] B modifies the contra -party on 
the unmatched (i.e. , short) side of the partially matched trade.  
(01) - (18) 
and  
CON MOD (19) - (23) 

---

## Page 63

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 63 
2.4.1 (CON MOD 19) MT515 Modify 
MESSAGE SAMPLE (CON MOD 19) MT515 [[Broker]] B Modifies 
Contra for PMAT Trade  
FIELD DESCRIPTION 
PSSWRD234 Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0441 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104528 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
 or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/MDFC Modify Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRD Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 

---

## Page 64

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 64 
MESSAGE SAMPLE (CON MOD 19) MT515 [[Broker]] B Modifies 
Contra for PMAT Trade  
FIELD DESCRIPTION 
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative Trade 
Service Type - Trade for Trade  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97, Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.4.2 (CON MOD 20) MT509 Modify Accepted 
MESSAGE SAMPLE (CON MOD 20) MT509  
Modify Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM020 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104530 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0441 Related Reference Number (sender’s reference)  

---

## Page 65

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 65 
MESSAGE SAMPLE (CON MOD 20) MT509  
Modify Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/MODA Modify Accepted 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.4.3 (CON MOD 21) MT509 Modify Processed 
MESSAGE SAMPLE (CON MOD 21) MT509  
Modify Processed sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM021 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104532 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 

---

## Page 66

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 66 
MESSAGE SAMPLE (CON MOD 21) MT509  
Modify Processed sent to [[Broker]] B  
FIELD DESCRIPTION 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Referenc e 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/MODP Modify Processed  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.4.4 (CON MOD 22) MT518 Comparison Request Cancel (due to Contra) 
MESSAGE SAMPLE (CON MOD 22) MT518  
Comparison Request Cancel (due to Contra) sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM022 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104535 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 

---

## Page 67

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 67 
MESSAGE SAMPLE (CON MOD 22) MT518  
Comparison Request Cancel (due to Contra) sent to Dealer C  
FIELD DESCRIPTION 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRCOAC Trade Instruction Processing Narrative Trade 
Service Type - Trade for Trade 
Message Reason - Due to Contra Action 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.4.5 (CON MOD 23) MT518 Comparison Request 
MESSAGE SAMPLE(CON MOD 23) MT518 Comparison 
Request sent to Dealer D  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 

---

## Page 68

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 68 
MESSAGE SAMPLE(CON MOD 23) MT518 Comparison 
Request sent to Dealer D  
FIELD DESCRIPTION 
DLRD Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM023 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104536 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRD Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Tr ade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  

---

## Page 69

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 69 
MESSAGE SAMPLE(CON MOD 23) MT518 Comparison 
Request sent to Dealer D  
FIELD DESCRIPTION 
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.5 Set 5 
In this set, the following messages are included (shaded in gray). 
RTTM
Dealer A DLR MOD (30) 
MT515 Instruct
DLR MOD (31) 
MT509 Modify Accepted
DLR MOD (32) 
MT509 Modify Processed
Continued from 
FMAT Trade in Set 1
(01) – (29)
 
Description Message Sequence 
Dealer A submits their  sell with an erroneous x -ref and then [[Broker]] B and Dealer C submit 
their trades. Dealer A modifies their  x-ref post-comparison/[[Novation]]. 
(01) - (29) 
and  
DLR MOD (30) – (32) 
2.5.1 (DLR MOD 30) MT515 Modify 
MESSAGE SAMPLE (DLR MOD 30) MT515  
Dealer A Modifies X -ref Post-Comparison  
FIELD DESCRIPTION 
PSSWRD123 Password  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA026 Sender’s Reference for this Message 
:23G:NEWM Message Function = New 
:98C::PREP//20010306104609 Preparation Date/Time 

---

## Page 70

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 70 
MESSAGE SAMPLE (DLR MOD 30) MT515  
Dealer A Modifies X -ref Post-Comparison  
FIELD DESCRIPTION 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA002 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//XREFDLRA001 Previous x -ref 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/MDFC Modify Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTFTBA Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 

---

## Page 71

MBSD RTTM® [[Novation]]: SWIFT Inte ractive Messaging Examples 
Version C ontrol Page 71 
MESSAGE SAMPLE (DLR MOD 30) MT515  
Dealer A Modifies X -ref Post-Comparison  
FIELD DESCRIPTION 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.5.2 (DLR MOD 31) MT509 Modify Accepted 
MESSAGE SAMPLE (DLR MOD 31) MT509  
Modify Accepted sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM028 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104612 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA002 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//XREFDLRA001 Previous x -ref 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA026 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 

---

## Page 72

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 72 
MESSAGE SAMPLE (DLR MOD 31) MT509  
Modify Accepted sent to Dealer A  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/MODA Modify Accepted 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.5.3 (DLR MOD 32) MT509 Modify Processed 
MESSAGE SAMPLE (DLR MOD 32) MT509  
Modify Processed sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM029 Sender’s RTTM Reference for this message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104613 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA002 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//XREFDLRA001 Previous x -ref 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/MODP Modify Processed  
:16S:STAT Repeat Block End 

---

## Page 73

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 73 
MESSAGE SAMPLE (DLR MOD 32) MT509  
Modify Processed sent to Dealer A  
FIELD DESCRIPTION 
:16S:GENL Block End 
- End of Message 
2.6 Set 6 
In this set, the following messages are included (shaded in gray). 
[[Broker]] BDealer A
RTTM
(02)
MT509 Trade Create Accepted
DK INST (07)
MT518 DK Advice
(03)
MT518 Comparison Request
DK INST (05)
MT509 DK Accepted
DK INST (06)
MT518 Comparison Request 
Modify (due to DK)
DK INST (08)
MT509 DK Processed
(01) 
MT515 Instruct 
DK INST (04) 
MT515 DK
 
Description Message Sequence 
Dealer A submits their  sell, but [[Broker]] B DK’s Dealer A’s Comparison Request.  (01) - (03) 
and  
DK INST (04) - (08) 
2.6.1 (DK INST 04) MT515 DK 
MESSAGE SAMPLE (DK INST 04) MT515  
[[Broker]] B DK’s Dealer A’s Comparison Request  
FIELD DESCRIPTION 
PSSWRD234 Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0221 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306103614 Preparation Date/Time 

---

## Page 74

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Example s 
Version C ontrol Page 74 
MESSAGE SAMPLE (DK INST 04) MT515  
[[Broker]] B DK’s Dealer A’s Comparison Request  
FIELD DESCRIPTION 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//NONREF Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/TDDK DK Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 Contra Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/DKRSE006 Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
DK Reason - Bad Trade Date 
:16S:CONFDET Block End 
- End of Message 

---

## Page 75

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 75 
2.6.2 (DK INST 05) MT509 DK Accepted 
MESSAGE SAMPLE (DK INST 05) MT509  
DK Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM007 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306103616 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0221 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PROG//7096000001 RTTM Assigned Contra Reference  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/PADK DK Accepted 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.6.3 (DK INST 06) MT518 Comparison Request Modify (due to DK) 
MESSAGE SAMPLE(DK INST 06) MT518  
Comparison Request Modify (due to DK) sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM009 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  

---

## Page 76

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 76 
MESSAGE SAMPLE(DK INST 06) MT518  
Comparison Request Modify (due to DK) sent to [[Broker]] B  
FIELD DESCRIPTION 
:98C::PREP//20010306103619 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CRQM Comparison Request Modify  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRDKTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to DK 
:16S:CONFDET Block End 
- End of Message 
2.6.4 (DK INST 07) MT518 DK Advice 
MESSAGE SAMPLE (DK INST 07) MT518  
DK Advice sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  

---

## Page 77

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 77 
MESSAGE SAMPLE (DK INST 07) MT518  
DK Advice sent to Dealer A  
FIELD DESCRIPTION 
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM008 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306103622 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start  
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/NAFI DK Advice 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/DKRSE006 Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade DK Reason - 
Bad Trade Date 
:16S:CONFDET Block End 

---

## Page 78

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 78 
MESSAGE SAMPLE (DK INST 07) MT518  
DK Advice sent to Dealer A  
FIELD DESCRIPTION 
- End of Message 
2.6.5 (DK INST 08) MT509 DK Processed 
MESSAGE SAMPLE (DK INST 08) MT509  
DK Processed sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM010 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306103625 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::PROG//7096000001 RTTM Assigned Contra Reference  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/DPPR DK Processed 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 79

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 79 
2.7 Set 7 
In this set, the following messages are included (shaded in gray). 
[[Broker]] B [[Broker]] B
[[Broker]] B
(06)
MT509 Trade Create Unbalanced
(10)
MT509 Trade Create Balanced
(05)
MT509 Trade Create Accepted
(08)
MT509 Trade Create Accepted
(09)
MT509  Trade Create Unbalanced
(11)
MT509 Trade Create Balanced
(04)
MT515 Instruct (vs. A)
(07) 
MT515 Instruct (vs. C)
Dealer A
(12)
MT518 Comparison Request
(02)
MT509 Trade Create Accepted
(14)
MT509 Trade Create Matched
(17)
MT518 Comparison Request 
Cancel (due to match)
(03)
MT518 Comparison Request
(15)
MT509 Trade Create Matched
(16)
MT509 Trade PMAT (long side)
(18)
MT518 Comparison Request 
Cancel (due to match)
(01) 
MT515 Instruct
(13)
MT518 Comparison Request
Dealer C
RTTM
DK INST(19) 
MT515 DK
DK INST (22) 
MT518 DK Advice
DK INST(20) 
MT509 DK Accepted
DK INST(21) 
MT518 Comparison 
Request Modify (due to DK)
DK INST(23) 
MT509 DK Processed
 
Description Message Sequence 
Dealer A submits their  sell, then [[Broker]] B submits both legs of their  trade but Dealer C DK’s 
[[Broker]] B’s Comparison Request.  
(01) - (18) 
and  
DK INST (19) - (23) 

---

## Page 80

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 80 
2.7.1 (DK INST 19) MT515 DK 
MESSAGE SAMPLE (DK INST 19) MT515  
Dealer C DK’s B’s Comparison Request  
FIELD DESCRIPTION 
PSSWRD345 Passwo rd 
DLRC Sender 
515/000/GSCC Message Type 
MBSCTRRS Receiver 
:16R:GENL Block Start 
:20C::SEME//SENREFDLRC0331 Sender’s Reference for this  Message 
:23G:NEW M Message Function = New 
:98C::PREP//20010306104310 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator 
:16R:LINK Repeat Block Start 
:20C::MAST//NONREF Master Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/TDDK DK Processing Indicator 
:22H::PAYM//APMT Against Payment Indic ator 
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTBKRB Party = Sell er 
:20C::PROC//7096000002 Cont ra Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount  (Par) 

---

## Page 81

MBSD RTTM® [[Novation]]: SWIFT In teractive Messaging Examples 
Version C ontrol Page 81 
MESSAGE SAMPLE (DK INST 19) MT515  
Dealer C DK’s B’s Comparison Request  
FIELD DESCRIPTION 
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD//DKRSE999 Trade Instruction  Processing Narrative 
Trade Service Ty pe - Trade for Trade 
DK Reason - Other Bad Data 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO Indi cator = Reporti ng Purpos es 
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.7.2 (DK INST 20) MT509 DK Accepted 
MESSAGE SAMPLE (DK INST 20) MT509  
DK Accepted sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM020 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104312 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRC0331 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PROG//7096000002 RTTM Assigned Contra Reference  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/PADK DK Accepted 

---

## Page 82

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 82 
MESSAGE SAMPLE (DK INST 20) MT509  
DK Accepted sent to Dealer C  
FIELD DESCRIPTION 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.7.3 (DK INST 21) MT518 Comparison Request Modify (due to DK) 
MESSAGE SAMPLE (DK INST 21) MT518  
Comparison Request Modify (due to DK) sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM022 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104317 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CRQM Comparison Request Modify  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 

---

## Page 83

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 83 
MESSAGE SAMPLE (DK INST 21) MT518  
Comparison Request Modify (due to DK) sent to Dealer C  
FIELD DESCRIPTION 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRDKTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to DK 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.7.4 (DK INST 22) MT518 DK Advice 
MESSAGE SAMPLE (DK INST 22) MT518  
DK Advice sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM021 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104320 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start  
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 

---

## Page 84

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 84 
MESSAGE SAMPLE (DK INST 22) MT518  
DK Advice sent to [[Broker]] B  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/NAFI DK Advice 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/DKRSE999 Trade Instruction Processing Narrative 
Trade Service Type - Trade for Tr ade 
DK Reason - Other Bad Data 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 

---

## Page 85

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 85 
MESSAGE SAMPLE (DK INST 22) MT518  
DK Advice sent to [[Broker]] B  
FIELD DESCRIPTION 
- End of Message 
2.7.5 (DK INST 23) MT509 DK Processed 
MESSAGE SAMPLE (DK INST 23) MT509  
DK Processed sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM023 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104322 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::PROG//7096000002 RTTM Assigned Contra Reference  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/DPPR DK Processed 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
 
  

---

## Page 86

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 86 
2.8 Set 8 
In this set, the following messages are included (shaded in gray). 
[[Broker]] B [[Broker]] B(06)
MT509 Trade Create Unbalanced
(05)
MT509 Trade Create Accepted
(04)
MT515 Instruct (vs. A) RTTM BRK CAN (07)
MT515 Cancel
BRK CAN (08)
MT509 Cancel Accepted
BRK CAN (09)
MT509 Cancel Processed
 
Description Message Sequence 
[[Broker]] B submits the buy side of their  trade and then cancels this leg pre -balancing.  (04) - (06) 
and  
BRK CAN (07) - (09) 
2.8.1 (BRK CAN 07) MT515 Cancel 
MESSAGE SAMPLE (BRK CAN 07) MT515  
[[Broker]] B Cancels Buy Submission Pre- Balancing 
FIELD DESCRIPTION 
PSSWRD234 Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0222 Sender’s Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306103955 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 

---

## Page 87

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 87 
MESSAGE SAMPLE (BRK CAN 07) MT515  
[[Broker]] B Cancels Buy Submission Pre- Balancing 
FIELD DESCRIPTION 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CANC Cancel Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 

---

## Page 88

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 88 
MESSAGE SAMPLE (BRK CAN 07) MT515  
[[Broker]] B Cancels Buy Submission Pre- Balancing 
FIELD DESCRIPTION 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.8.2 (BRK CAN 08) MT509 Cancel Accepted 
MESSAGE SAMPLE (BRK CAN 08) MT509  
Cancel Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM009 Sender’s RTTM Reference for this  Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306103956 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0222 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC//PACK Cancel Accepted 
:16S:STAT Repeat Block End 

---

## Page 89

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 89 
MESSAGE SAMPLE (BRK CAN 08) MT509  
Cancel Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
:16S:GENL Block End 
- End of Message 
2.8.3 (BRK CAN 09) MT509 Cancel Processed 
MESSAGE SAMPLE (BRK CAN 09) MT509  
Cancel Processed sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM010 Sender’s RTTM Reference for this Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306103958 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC//CAND Cancel Processed  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 90

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 90 
2.9 Set 9 
In this set, the following messages are included (shaded in gray). 
[[Broker]] B [[Broker]] B
[[Broker]] B
(06)
MT509 Trade Create Unbalanced
(10)
MT
509 Trade Create Balanced
(05)
MT
509 Trade Create Accepted
(08)
MT509 Trade Create Accepted
(09)
MT509  Trade Create Unbalanced
(11)
MT
509 Trade Create Balanced
(04)
MT515 Instruct (vs. A)
(07) 
MT515 Instruct (vs. C)
Dealer A
(12)
MT518 Comparison Request
(13)
MT518 Comparison Request
Dealer C
RTTM
BRK CAN (14) 
MT
515 Cancel Set
BRK CAN (15) 
MT
509 Cancel Set Accepted
BRK CAN (16) 
MT
509 Cancel Set Processed
BRK CAN (17) 
MT
518 Comparison Request 
Cancel (due to Contra)
BRK CAN (18) 
MT
518 Comparison Request 
Cancel (due to Contra)
 
Description Message Sequence 
[[Broker]] B submits both sides of their  trade and then cancels this balanced set of submissions 
post -balancing but pre-comparison.  
(04) - (13) 
and  
BRK CAN (14) - (18) 
2.9.1 (BRK CAN 14) MT515 Cancel Set 
MESSAGE SAMPLE(BRK CAN 14) MT515 [[Broker]] B Cancels 
Transaction Post -Balancing (Pre- Comparison) 
FIELD DESCRIPTION 
PSSWRD234 Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 

---

## Page 91

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 91 
MESSAGE SAMPLE(BRK CAN 14) MT515 [[Broker]] B Cancels 
Transaction Post -Balancing (Pre- Comparison) 
FIELD DESCRIPTION 
:20C::SEME//SENREFBKRB0223 Sender’s Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104148 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CASE Cancel Set Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 

---

## Page 92

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 92 
2.9.2 (BRK CAN 15) MT509 Cancel Set Accepted 
MESSAGE SAMPLE (BRK CAN 15) MT509  
Cancel Set Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM015 Sender’s RTTM Reference for this  Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306104150 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0223 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC/GSCC/PACS Cancel Set Accepted  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.9.3 (BRK CAN 16) MT509 Cancel Set Processed 
MESSAGE SAMPLE (BRK CAN 16) MT509  
Cancel Set Processed sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  

---

## Page 93

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 93 
MESSAGE SAMPLE (BRK CAN 16) MT509  
Cancel Set Processed sent to [[Broker]] B  
FIELD DESCRIPTION 
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM016 Sender’s RTTM Reference for this  Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306104151 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC/GSCC/XPPR Cancel Set Processed 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.9.4 (BRK CAN 17) MT518 Comparison Request Cancel (due to Contra) 
MESSAGE SAMPLE (BRK CAN 17) MT518  
Comparison Request Cancel (due to Contra) sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM017 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104153 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 

---

## Page 94

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 94 
MESSAGE SAMPLE (BRK CAN 17) MT518  
Comparison Request Cancel (due to Contra) sent to Dealer A  
FIELD DESCRIPTION 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:20C::PROC//7096000002 [[Buyer]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRCOAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Contra Action 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 95

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 95 
2.9.5 (BRK CAN 18) MT518 Comparison Request Cancel (due to Contra) 
MESSAGE SAMPLE (BRK CAN 18) MT518  
Comparison Request Cancel (due to Contra) sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM018 Sender’s RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104156 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  

---

## Page 96

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 96 
MESSAGE SAMPLE (BRK CAN 18) MT518  
Comparison Request Cancel (due to Contra) sent to Dealer C  
FIELD DESCRIPTION 
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD//MSGRCOAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Contra Action 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
 
  

---

## Page 97

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 97 
2.10 Set 10 
In this set, the following messages are included (shaded in gray). 
Dealer A [[Broker]] B
[[Broker]] BDealer C
BRK CAN (27)
MT518 Comparison Request 
Cancel (due to contra)
Continued from PMAT 
Trade in Set 1
(01) – (18)
BRK CAN (19)
MT515 Cancel Set
BRK CAN (20)
MT509 Cancel Set Accepted
BRK CAN (24)
MT518 Cancel RequestRTTM
BRK CAN (26)
MT509 Cancel Set Processed
BRK CAN (21)
MT518 Cancel Request
BRK CAN (23)
MT509 Cancel Accepted
BRK CAN (25)
MT509 Cancel Processed
BRK CAN (22) 
MT515 Cancel
 
Description Message Sequence 
Dealer A submits their  sell and then [[Broker]] B submits both legs of their  trade. This partially 
matched trade is then canceled bilaterally by [[Broker]] B and Dealer A.  
(01) - (18) 
and  
BRK CAN (19) - (27) 
2.10.1 (BRK CAN 19) MT515 Cancel Set 
MESSAGE SAMPLE (BRK CAN 19) MT515  
[[Broker]] B Cancels PMAT Trade 
FIELD DESCRIPTION 
PSSWRD234 Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0223 Sender’s Reference for this Message 
:23G:CANC Message Function = Cancel  

---

## Page 98

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 98 
MESSAGE SAMPLE (BRK CAN 19) MT515  
[[Broker]] B Cancels PMAT Trade 
FIELD DESCRIPTION 
:98C::PREP//20010306104650 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CASE Cancel Set Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade  
:16S:CONFDET Block End 
- End of Message 

---

## Page 99

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 99 
2.10.2 (BRK CAN 20) MT509 Cancel Set Accepted 
MESSAGE SAMPLE (BRK CAN 20) MT509  
Cancel Set Accepted sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM020 Sender’s RTTM Reference for this  Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306104653 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0223 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC/GSCC/PACS Cancel Set Accepted  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
  

---

## Page 100

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 100 
2.10.3 (BRK CAN 21) MT518 Cancel Request 
MESSAGE SAMPLE (BRK CAN 21) MT518  
Cancel Request sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM021 Sender’s RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104655 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start  
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CREQ Cancel Request 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 

---

## Page 101

MBSD RTTM® [[Novation]]: SWIF T Interactive Messaging Examples 
Version C ontrol Page 101 
MESSAGE SAMPLE (BRK CAN 21) MT518  
Cancel Request sent to Dealer A  
FIELD DESCRIPTION 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.10.4 (BRK CAN 22) MT515 Cancel 
MESSAGE SAMPLE (BRK CAN 22) MT515  
Dealer A Submits Corresponding Cancel of PMAT  
FIELD DESCRIPTION 
PSSWRD123 Passwo rd 
DLRA Sender 
515/000/GSCC Message Type 
MBSCTRRS Receiver 
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA 016 Sender’s Reference for this  Message 
:23G:CANC Message Function = Cancel 
:98C::PREP//20010306105823 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number 

---

## Page 102

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 102 
MESSAGE SAMPLE (BRK CAN 22) MT515  
Dealer A Submits Corresponding Cancel of PMAT  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previo us Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 
or 
:20C::LIST//2049000001 
RTTM Assi gned Tr ansaction Reference 
or 
RTTM Assi gned Tr ade Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CANC Cancel Processing Indicator 
:22H::PAYM//APMT Against Payment Indic ator 
:22F::CATB//PERU Per Unit Charges Indic ator 
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]] 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount  (Par) 
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction  Processing Narrative 
Trade Service Ty pe - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO Indi cator = Reporti ng Purpos es 
:16R:AMT Optional Block Start 

---

## Page 103

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 103 
MESSAGE SAMPLE (BRK CAN 22) MT515  
Dealer A Submits Corresponding Cancel of PMAT  
FIELD DESCRIPTION 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.10.5 (BRK CAN 23) MT509 Cancel Accepted 
MESSAGE SAMPLE (BRK CAN 23) MT509  
Cancel Accepted sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM022 Sender’s RTTM Reference for this  Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306105825 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA016 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC//PACK Cancel Accepted  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 104

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging E xamples 
Version C ontrol Page 104 
2.10.6 (BRK CAN 24) MT518 Cancel Request 
MESSAGE SAMPLE (BRK CAN 24) MT518  
Cancel Request sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM023 Sender’s RTTM Reference for this message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306105827 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start  
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CREQ Cancel Request 
:22H::PAYM//APMT Against Payment Indicator  

---

## Page 105

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 105 
MESSAGE SAMPLE (BRK CAN 24) MT518  
Cancel Request sent to [[Broker]] B  
FIELD DESCRIPTION 
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.10.7 (BRK CAN 25) MT509 Cancel Processed 
MESSAGE SAMPLE (BRK CAN 25) MT509  
Cancel Processed sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM024 Sender’s RTTM Reference for this Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306105828 Preparation Date/Time 

---

## Page 106

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 106 
MESSAGE SAMPLE (BRK CAN 25) MT509  
Cancel Processed sent to Dealer A  
FIELD DESCRIPTION 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC//CAND Cancel Processed 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.10.8 (BRK CAN 26) MT509 Cancel Set Processed 
MESSAGE SAMPLE (BRK CAN 26) MT509  
Cancel Set Processed sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM025 Sender’s RTTM Reference for this  Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306105829 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  

---

## Page 107

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 107 
MESSAGE SAMPLE (BRK CAN 26) MT509  
Cancel Set Processed sent to [[Broker]] B  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC/GSCC/XPPR Cancel Set Processed 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.10.9 (BRK CAN 27) MT518 Comparison Request Cancel (due to Contra) 
MESSAGE SAMPLE (BRK CAN 27) MT518  
Comparison Request Cancel (due to Contra) sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM026 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306105832 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  

---

## Page 108

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 108 
MESSAGE SAMPLE (BRK CAN 27) MT518  
Comparison Request Cancel (due to Contra) sent to Dealer C  
FIELD DESCRIPTION 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD /MSGRCOAC  Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Contra Action 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
 
  

---

## Page 109

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 109 
2.11 Set 11 
In this set, the following messages are included (shaded in gray). 
Dealer A [[Broker]] B
RTTM
(02)
MT509 Trade Create Accepted
(03)
MT
518 Comparison 
Request
(01)
MT515 Instruct
DLR CAN (07)
MT518 Comparison Request 
Cancel (due to Contra)
DLR CAN (05)
MT509 Trade Create Accepted
DLR CAN (04)
MT515 Cancel
DLR CAN (06)
MT509 Trade Create Processed
 
Description Message Sequence 
Dealer A submits their  sell and then cancels it pre - comparison.  (01) - (03) 
and  
DLR CAN (04) - (07) 
2.11.1 (DLR CAN 04) MT515 Cancel 
MESSAGE SAMPLE (DLR CAN 04) MT515  
Dealer A Cancels Trade Pre- Comparison 
FIELD DESCRIPTION 
PSSWRD123 Password  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA016 Sender’s Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306101447 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  

---

## Page 110

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 110 
MESSAGE SAMPLE (DLR CAN 04) MT515  
Dealer A Cancels Trade Pre- Comparison 
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CANC Cancel Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
2.11.2 (DLR CAN 05) MT509 Cancel Accepted 
MESSAGE SAMPLE (DLR CAN 05) MT509  
Cancel Accepted sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 

---

## Page 111

MBSD RTTM® [[Novation]]: SW IFT Interactive Messaging Examples 
Version C ontrol Page 111 
MESSAGE SAMPLE (DLR CAN 05) MT509  
Cancel Accepted sent to Dealer A  
FIELD DESCRIPTION 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM007 Sender’s RTTM Reference for this Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306101449 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA016 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC//PACK Cancel Accepted 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.11.3 (DLR CAN 06) MT509 Cancel Processed 
MESSAGE SAMPLE (DLR CAN 06) MT509  
Cancel Processed sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM008 Sender’s RTTM Reference for this Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306101452 Preparation Date/Time 

---

## Page 112

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 112 
MESSAGE SAMPLE (DLR CAN 06) MT509  
Cancel Processed sent to Dealer A  
FIELD DESCRIPTION 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC//CAND Cancel Processed 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.11.4 (DLR CAN 07) MT518 Comparison Request Cancel (due to Contra) 
MESSAGE SAMPLE (DLR CAN 07) MT518 Comparison 
Request Cancel (due to Contra) sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM009 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306101454 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 

---

## Page 113

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 113 
MESSAGE SAMPLE (DLR CAN 07) MT518 Comparison 
Request Cancel (due to Contra) sent to [[Broker]] B (Short Side)  
FIELD DESCRIPTION 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRCOAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Contra Action 
:16S:CONFDET Block End 
- End of Message 
 
  

---

## Page 114

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples 
Version C ontrol Page 114 
2.12 Set 12 
In this set, the following messages are included (shaded in gray). 
Dealer A [[Broker]] B
[[Broker]] BDealer C
Continued from FMAT 
Trade in Set 1
(01) – (29)
RTTM
DLR CAN (32)
MT518 Cancel Request
DLR CAN (31)
MT509 Cancel Accepted
DLR CAN (30) 
MT515 Cancel
DLR CAN (33)
MT518 Cancel Request (Info)
DLRCAN (34)
Cancel Remove 
(via WFE)
DLR CAN (35)
MT509 Cancel Lifted by [[participant]]
DLR CAN (36)
MT518 Cancel Request 
Cancel (due to Contra)
DLR CAN (37)
MT518 Cancel Request 
Cancel (due to Contra) (Info)
 
Description Message Sequence 
Dealer A submits their  sell and then [[Broker]] B and dealer C submit their trades. Dealer A 
submits a Cancel message for this fully matched  and novated trade, but before any contra-
party reacts, A removes their  Cancel message (“un -cancels”) via WFE.  
(01) - (29) 
and  
DLR CAN (30) - (37) 
2.12.1 (DLR CAN 30) MT515 Cancel 
MESSAGE SAMPLE (DLR CAN 30) MT515  
Dealer A Cancels Trade Post -Comparison 
FIELD DESCRIPTION 
PSSWRD123 Password  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA016 Sender’s Reference for this Message 
:23G:CANC Message Function = Cancel  

---

## Page 115

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 115 
MESSAGE SAMPLE (DLR CAN 30) MT515  
Dealer A Cancels Trade Post -Comparison 
FIELD DESCRIPTION 
:98C::PREP//20010306110723 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CANC Cancel Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTFTBA Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 

---

## Page 116

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 116 
MESSAGE SAMPLE (DLR CAN 30) MT515  
Dealer A Cancels Trade Post -Comparison 
FIELD DESCRIPTION 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.12.2 (DLR CAN 31) MT509 Cancel Accepted 
MESSAGE SAMPLE (DLR CAN 31) MT509  
Cancel Accepted sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM028 Sender’s RTTM Reference for this  Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306110726 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA016 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 

---

## Page 117

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 117 
MESSAGE SAMPLE (DLR CAN 31) MT509  
Cancel Accepted sent to Dealer A  
FIELD DESCRIPTION 
:25D::CPRC//PACK Cancel Accepted 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.12.3 (DLR CAN 32) MT518 Cancel Request 
MESSAGE SAMPLE(DLR CAN 32) MT518  
Cancel Request sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM029 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306110728 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start  
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 

---

## Page 118

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 118 
MESSAGE SAMPLE(DLR CAN 32) MT518  
Cancel Request sent to Dealer C  
FIELD DESCRIPTION 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CREQ Cancel Request 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTFTBA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.12.4 (DLR CAN 33) MT518 Cancel Request (Info) 
MESSAGE SAMPLE (DLR CAN 33) MT518  
Informational Cancel Request sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  

---

## Page 119

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 119 
MESSAGE SAMPLE (DLR CAN 33) MT518  
Informational Cancel Request sent to [[Broker]] B  
FIELD DESCRIPTION 
:20C::SEME//SENREFRTTM030 Sender’s RTTM Reference for this message 
:23G:CANC/COPY Message Function = Cancel (info  only)  
:98C::PREP//20010306110729 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CREQ Cancel Request 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 

---

## Page 120

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 120 
MESSAGE SAMPLE (DLR CAN 33) MT518  
Informational Cancel Request sent to [[Broker]] B  
FIELD DESCRIPTION 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.12.5 (DLR CAN 34) Cancel Remove via WFE 
MESSAGE SAMPLE (DLR CAN 34) Dealer A  
Removes Cancel via WFE (at 20010306112544)  
FIELD DESCRIPTION 
 
[WFE COMMAND ONLY – NO MT515 EQUIVALENT] 
2.12.6 (DLR CAN 35) MT509 Cancel Lifted by [[participant]] 
MESSAGE SAMPLE(DLR CAN 35) MT509  
Cancel Lifted by [[participant]] sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM031 Sender’s RTTM Reference for this Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306112551 Preparation Date/Time 
:16R:LINK Repeat Block Start 

---

## Page 121

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples 
Version C ontrol Page 121 
MESSAGE SAMPLE(DLR CAN 35) MT509  
Cancel Lifted by [[participant]] sent to Dealer A  
FIELD DESCRIPTION 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC/GSCC/UPBP Cancel Lifted by [[participant]]  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.12.7 (DLR CAN 36) MT518 Cancel Request Cancel (due to Contra) 
MESSAGE SAMPLE (DLR CAN 36) MT518  
Cancel Request Cancel (due to Contra) sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM032 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306112552 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start  
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 

---

## Page 122

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 122 
MESSAGE SAMPLE (DLR CAN 36) MT518  
Cancel Request Cancel (due to Contra) sent to Dealer C  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CCRQ Cancel Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTFTBA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRCOAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Contra Action 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 123

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 123 
2.12.8 (DLR CAN 37) MT518 Cancel Request Cancel (due to Contra) (Info) 
MESSAGE SAMPLE (DLR CAN 37) MT518  Informational Cancel 
Request Cancel (due to Contra) sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM033 Sender’s RTTM Reference for this message 
:23G:CANC/COPY Message Function = Cancel (Info only)  
:98C::PREP//20010306112554 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CCRQ Cancel Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  

---

## Page 124

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 124 
MESSAGE SAMPLE (DLR CAN 37) MT518  Informational Cancel 
Request Cancel (due to Contra) sent to [[Broker]] B  
FIELD DESCRIPTION 
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRCOAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Contra Action 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
 
  

---

## Page 125

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 125 
2.13 Set 13 
In this set, the following messages are included (shaded in gray). 
Dealer A [[Broker]] B
[[Broker]] B
Dealer C
Continued from FMAT 
Trade in Set 1
(01) – (29)
RTTM
DLR CAN (32)
MT518 Cancel Request
DLR CAN (31)
MT509 Cancel Accepted
DLR CAN (30) 
MT515 Cancel
DLR CAN (33)
MT518 Cancel Request (Info)
DK DLR CAN (34)
MT515 DK (Cancel)
DLR CAN (39)
MT518 DK (Cancel) Advice (Info)
DK DLR CAN (36)
MT509 DK (Cancel) Processed
DK DLR CAN (37)
MT518 Cancel Request 
Modify (due to DK)
DK DLR CAN (35)
MT509 DK (Cancel) Accepted
DK DLR CAN (38)
MT518 DK (Cancel) Advice
 
Description Message Sequence 
Dealer A submits their  sell and then [[Broker]] B and dealer C submit their trades. Dealer A 
submits a Cancel message for this fully matched  and novated trade, but Dealer C DK’s 
Dealer A’s Cancel Request.  
(01) - (29) 
and  
DLR CAN(30) - (33) 
and  
DK DLR CAN(34) - (39) 
2.13.1 (DK DLR CAN 34) MT515 DK (Cancel) 
MESSAGE SAMPLE (DK DLR CAN 34) MT515  
Dealer C DK’s a Cancel Request submitted against them 
FIELD DESCRIPTION 
PSSWRD345 Password  
DLRC Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 

---

## Page 126

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 126 
MESSAGE SAMPLE (DK DLR CAN 34) MT515  
Dealer C DK’s a Cancel Request submitted against them 
FIELD DESCRIPTION 
:20C::SEME//SENREFDLRC0332 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306112018 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/TDDK DK Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTFTBA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/DKRSE100 Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
DK Reason - Unknown Cancel  
:16S:CONFDET Block End 

---

## Page 127

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 127 
MESSAGE SAMPLE (DK DLR CAN 34) MT515  
Dealer C DK’s a Cancel Request submitted against them 
FIELD DESCRIPTION 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.13.2 (DK DLR CAN 35) MT509 DK (Cancel) Accepted 
MESSAGE SAMPLE (DK DLR CAN 33) MT509  
DK (Cancel) Accepted sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM031 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306112019 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRC0332 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/PADK DK Accepted 
:16S:STAT Repeat Block End 

---

## Page 128

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 128 
MESSAGE SAMPLE (DK DLR CAN 33) MT509  
DK (Cancel) Accepted sent to Dealer C  
FIELD DESCRIPTION 
:16S:GENL Block End 
- End of Message 
2.13.3 (DK DLR CAN 36) MT509 DK (Cancel) Processed 
MESSAGE SAMPLE (DK DLR CAN 36) MT509  
DK (Cancel) Processed sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM032 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306112020 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/DPPR DK Processed 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 129

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 129 
2.13.4 (DK DLR CAN 37) MT518 Cancel Request Modify (due to DK) 
MESSAGE SAMPLE (DK DLR CAN 37) MT518  
Cancel Request Modify (due to DK) sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM033 Sender’s RTTM Reference for this message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306112023 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start  
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/MCRQ Cancel Request Modify 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 

---

## Page 130

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 130 
MESSAGE SAMPLE (DK DLR CAN 37) MT518  
Cancel Request Modify (due to DK) sent to Dealer C  
FIELD DESCRIPTION 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTFTBA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRDKTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to DK 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.13.5 (DK DLR CAN 38) MT518 DK (Cancel) Advice 
MESSAGE SAMPLE (DK DLR CAN 38) MT518  
DK (Cancel) Advice sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM034 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306112024 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start  
:20C::MAST//XREFDLRA001 Master Reference Number  

---

## Page 131

MBSD RTTM® [[Novation]] : SWIFT Interactive Messaging Examples 
Version C ontrol Page 131 
MESSAGE SAMPLE (DK DLR CAN 38) MT518  
DK (Cancel) Advice sent to Dealer A  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/NAFI DK Advice 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTFTBA Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/DKRSE100 Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
DK Reason - Unknown Cancel  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  

---

## Page 132

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 132 
MESSAGE SAMPLE (DK DLR CAN 38) MT518  
DK (Cancel) Advice sent to Dealer A  
FIELD DESCRIPTION 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.13.5 (DK DLR CAN 39) MT518 DK (Cancel) Advice (Info) 
MESSAGE SAMPLE (DK DLR CAN 39) MT518  
Informational DK (Cancel) Advice sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM035 Sender’s RTTM Reference for this message 
:23G:CANC/COPY Message Function = Cancel (Info only)  
:98C::PREP//20010306112025 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Optional Repeat Block Start  
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  

---

## Page 133

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 133 
MESSAGE SAMPLE (DK DLR CAN 39) MT518  
Informational DK (Cancel) Advice sent to [[Broker]] B  
FIELD DESCRIPTION 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/NAFI DK Advice 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY   Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/DKRSE100 Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
DK Reason - Unknown Cancel  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 134

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 134 
2.14 Set 14 
In this set, the following messages are included (shaded in gray). 
Dealer A [[Broker]] B
RTTM
(01) 
MT515 Instruct
REJ (02)
MT509 Trade Create Rejected
 
Description Message Sequence 
Dealer A submits their  sell using an external reference number that is not unique ( they have 
already used this reference number previously for a message that is currently on the system).  
As a result, the message is rejected by RTTM.  
(01) 
and  
REJ (02) 
2.14.1 (REJ 02) MT509 Trade Create Rejected 
MESSAGE SAMPLE- (REJ 02) MT509  
Trade Create Rejected sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM005 Sender’s RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306100913 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA015 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//REJT Message Rejected  

---

## Page 135

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 135 
MESSAGE SAMPLE- (REJ 02) MT509  
Trade Create Rejected sent to Dealer A  
FIELD DESCRIPTION 
:16R:REAS Optional Repeat Block Start  
:24B::REJT/GSCC/E001 Reject Reason - External Reference Error  
:16S:REAS Repeat Block End 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.15 Set 15 
In this set, the following messages are included (shaded in gray). 
[[Broker]] B [[Broker]] B
[[Broker]] B
(06)
MT509 Trade Create Unbalanced
(10)
MT509 Trade Create Balanced
(05)
MT509 Trade Create Accepted
(08)
MT509 Trade Create Accepted
(09)
MT509  Trade Create Unbalanced
(11)
MT509 Trade Create Balanced
(04)
MT515 Instruct (vs. A)
(07) 
MT515 Instruct (vs. C)
Dealer A
(12)
MT518 Comparison Request
(02)
MT509 Trade Create Accepted
(14)
MT509 Trade Create Matched
(17)
MT518 Comparison Request 
Cancel (due to match)
(03)
MT518 Comparison Request
(15)
MT509 Trade Create Matched
(16)
MT509 Trade PMAT (long side)
(18)
MT518 Comparison Request 
Cancel (due to match)
(01) 
MT515 Instruct
(13)
MT518 Comparison Request
Dealer C
RTTM
REJ CAN (19) 
MT515 Cancel Set
REJ CAN (20) 
MT509 Cancel Set Rejected
 

---

## Page 136

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 136 
Description Message Sequence 
Dealer A submits their  sell and then [[Broker]] B submits both legs of their  trade. [[Broker]] B submits 
a Cancel Set message in order to cancel this partially matched trade, but this message is 
rejected by RTTM as [[Broker]] B uses an incorrect password.  
(01) - (18) 
and  
REJ CAN (19) - (20) 
2.15.1 (REJ CAN 19) MT515 Cancel Set 
MESSAGE SAMPLE (REJ CAN 19) MT515  
[[Broker]] B Cancels PMAT Trade 
FIELD DESCRIPTION 
BADPSSWRD Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0223 Sender’s Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104650 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 

---

## Page 137

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 137 
MESSAGE SAMPLE (REJ CAN 19) MT515  
[[Broker]] B Cancels PMAT Trade 
FIELD DESCRIPTION 
:22F::PROC/GSCC/CASE Cancel Set Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
2.15.2 (REJ CAN 20) MT509 Cancel Set Rejected 
MESSAGE SAMPLE(REJ CAN 20) MT509  
Cancel Set (of PMAT Trade) Rejected sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type  
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM020 Sender’s RTTM Reference for this Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306104653 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0223 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 

---

## Page 138

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 138 
MESSAGE SAMPLE(REJ CAN 20) MT509  
Cancel Set (of PMAT Trade) Rejected sent to [[Broker]] B  
FIELD DESCRIPTION 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC//REJT Cancel Rejected 
:16R:REAS Optional Repeat Block Start  
:24B::REJT/GSCC/E016 Reject Reason - Password Error 
:70D::REAS//CSRJ Cancel Set Rejected  
:16S:REAS Repeat Block End 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.16 Set 16 
In this set, the following messages are included (shaded in gray). 
Dealer A [[Broker]] B
Continued from FMAT 
Trade in Set 1
(01) – (29)
RTTM
REJ CAN (30)
MT515 Cancel
REJ CAN (31)
MT509 Cancel Rejected
 
Description Messages 
Dealer A submits their  sell and then [[Broker]] B and dealer C submit their trades. After the trade 
has been fully matched  and novated, Dealer A submits a Cancel message using an incorrect 
password – as a result, RTTM rejects A’s Cancel message.  
(01) - (29) 
and  
REJ CAN (30) - (31) 

---

## Page 139

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 139 
2.16.1 (REJ CAN 30) MT515 Cancel 
MESSAGE SAMPLE (REJ CAN 30) MT515 Dealer A Cancels 
Trade Post-Comparison 
FIELD DESCRIPTION 
BADPSSWRD Password  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA016 Sender’s Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306110723 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CANC Cancel Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 

---

## Page 140

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 140 
MESSAGE SAMPLE (REJ CAN 30) MT515 Dealer A Cancels 
Trade Post-Comparison 
FIELD DESCRIPTION 
:95R::BUYR/GSCC/PARTFTBA Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.16.2 (REJ CAN 31) MT509 Cancel Rejected 
MESSAGE SAMPLE (REJ CAN 31) MT509  
Post- Comparison Cancel Rejected sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM028 Sender’s RTTM Reference for this  Message 
:23G:CAST Message Function - Cancel  
:98C::PREP//20010306110726 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  

---

## Page 141

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 141 
MESSAGE SAMPLE (REJ CAN 31) MT509  
Post- Comparison Cancel Rejected sent to Dealer A  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA016 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 
or 
:20C::LIST//2049000001 
RTTM Assigned Transaction Reference 
or 
RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC//REJT Cancel Rejected 
:16R:REAS Optional Repeat Block Start  
:24B::REJT/GSCC/E016 Reject Reason - Password Error 
:16S:REAS Repeat Block End 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.17 Set 17 
In this set, the following messages are included (shaded in gray). 
[[Broker]] BDealer A
(02)
MT509 Trade Create Accepted
(03)
MT518 Comparison Request
(01) 
MT515 Instruct RTTM
REJ DK INST (04) 
MT515 DK
REJ DK INST (05) 
MT509 DK Rejected
 
Description Messages 
Dealer A submits their  sell, but [[Broker]] B DK’s Dealer A’s Comparison Request. [[Broker]] B’s 
DK message is rejected by RTTM because the trade is not found ([[Broker]] B supplied an 
incorrect contra transaction reference).  
(01) - (03) 
and  
REJ DK INST (04) - (05) 

---

## Page 142

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 142 
2.17.1 (REJ DK INST 04) MT515 DK 
MESSAGE SAMPLE (REJ DK INST 04) MT515  
[[Broker]] B DK’s Dealer A’s Comparison Request  
FIELD DESCRIPTION 
PSSWRD234 Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0221 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306103614 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//NONREF Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/TDDK DK Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//BADREFERENCE Contra Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 

---

## Page 143

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 143 
MESSAGE SAMPLE (REJ DK INST 04) MT515  
[[Broker]] B DK’s Dealer A’s Comparison Request  
FIELD DESCRIPTION 
:70E::TPRO//GSCC/TDSVTFTD/DKRSE006 Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
DK Reason - Bad Trade Date 
:16S:CONFDET Block End 
- End of Message 
2.17.2 (REJ DK INST 05) MT509 DK Rejected 
MESSAGE SAMPLE (R EJ DK INST 05) MT509  
DK Rejected sent to [[Broker]] B 
FIELD DESCRIPTION 
 Passwo rd 
MBSCTRRS Sender 
509/000/GSCC Message Type 
BKRB Receiver 
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM007 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306103616 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0221 Related Reference Number (sende r’s reference) 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PROG//7096000001 RTTM Assi gned Contra Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//REJT Message Rejected 
:16R:REAS Optional Repeat Block Start 
:24B::REJT/GSCC/E998 Reject Reason - Trade not  found 
:70D::REAS//DKRJ DK Rejected 
:16S:REAS Repeat Block End 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 144

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 144 
2.18 Set 18 
In this set, the following messages are included (shaded in gray). 
Dealer A
STIP (01) 
MT515 Instruct
STIP (02)
MT509 Trade Create Accepted
Dealer C
STIP (03)
MT518 Comparison Request
STIP (04) 
MT515 Instruct
STIP (06)
MT518 Comparison Request
STIP (05)
MT509 Trade Create Accepted
STIP (07)
MT509 Trade Create Matched
STIP (08)
MT509 Trade Create Matched
STIP (09)
MT518 Comparison Request 
Cancel (due to Match)
STIP (10)
MT518 Comparison Request 
Cancel (due to Match)
RTTM
STIP (11)
MT518 Trade Novated
STIP (12)
MT518 Trade Novated
 
Description Message Sequence 
Dealer A submits their  sell for a STIP trade, and Dealer C submits a matching trade.  The 
trades are matched and novated.  
STIP (01) – (12) 
2.18.1 (STIP 01) MT515 Instruct 
MESSAGE SAMPLE (STIP 01) MT515  
Dealer A Submits Sell to RTTM (Trade Create)  
FIELD DESCRIPTION 
PSSWRD123 Password  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA015 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306100526 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  

---

## Page 145

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 145 
MESSAGE SAMPLE (STIP 01) MT515  
Dealer A Submits Sell to RTTM (Trade Create)  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing  
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVSTIP Trade Instruction Processing Narrative 
Trade Service Type – STIP Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
2.18.2 (STIP 02) MT509 Trade Create Accepted 
MSSAGE SAMPLE (STIP 02)  MT509  
Trade Create Accepted sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM005 Sender’s RTTM Reference for this  Message 

---

## Page 146

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 146 
MSSAGE SAMPLE (STIP 02)  MT509  
Trade Create Accepted sent to Dealer A  
FIELD DESCRIPTION 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306100913 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA015 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.18.3 (STIP 03) MT518 Comparison Request 
MESSAGE SAMPLE (STIP 03) MT518  
Comparison Request for Matching Buy sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM006 Sender’s RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306100952 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  

---

## Page 147

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 147 
MESSAGE SAMPLE (STIP 03) MT518  
Comparison Request for Matching Buy sent to Dealer C  
FIELD DESCRIPTION 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVSTIP Trade Instruction Processing Narrative 
Trade Service Type – STIP Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
2.18.4 (STIP 04) MT515 Instruct 
MESSAGE SAMPLE (STIP 04) MT515  
Dealer C Submits Buy to RTTM (Trade Create)  
FIELD DESCRIPTION 
PSSWRD123 Password  
DLRC Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRC0331 Sender’s Reference for this Message 
:23G:NEWM Message Function = New 
:98C::PREP//20010306100526 Preparation Date/Time 

---

## Page 148

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 148 
MESSAGE SAMPLE (STIP 04) MT515  
Dealer C Submits Buy to RTTM (Trade Create)  
FIELD DESCRIPTION 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing  
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 
:70E::TPRO//GSCC/TDSVSTIP Trade Instruction Processing Narrative 
Trade Service Type – STIP Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
2.18.5 (STIP 05) MT509 Trade Create Accepted 
MESSAGE SAMPLE (STIP 05)  MT509 Trade Create Accepted 
sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 

---

## Page 149

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 149 
MESSAGE SAMPLE (STIP 05)  MT509 Trade Create Accepted 
sent to Dealer C  
FIELD DESCRIPTION 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM007 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306100913 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRC0331 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000003 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.18.6 (STIP 06) MT518 Comparison Request 
MESSAGE SAMPLE (STIP 06) MT518 Comparison Request for 
Matching Sell sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM008 Sender’s RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306100952 Preparation Date/Time 

---

## Page 150

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 150 
MESSAGE SAMPLE (STIP 06) MT518 Comparison Request for 
Matching Sell sent to Dealer A  
FIELD DESCRIPTION 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000003 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVSTIP Trade Instruction Processing Narrative 
Trade Service Type – STIP Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
2.18.7 (STIP 07) MT509 Trade Matched 
MESSAGE SAMPLE (STIP 07) MT509  
Transaction Matched sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 

---

## Page 151

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 151 
MESSAGE SAMPLE (STIP 07) MT509  
Transaction Matched sent to Dealer A  
FIELD DESCRIPTION 
:20C::SEME//SENREFRTTM009 Sender’s RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104136 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//2049000001 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.18.8 (STIP 08) MT509 Trade Matched 
MESSAGE SAMPLE (STIP 08) MT509  
Transaction Matched sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM010 Sender’s RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104136 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  

---

## Page 152

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 152 
MESSAGE SAMPLE (STIP 08) MT509  
Transaction Matched sent to Dealer C  
FIELD DESCRIPTION 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000003 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//2049000002 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.18.9 (STIP 09) MT518 Comparison Request Cancel (due to Match) 
MESSAGE SAMPLE (STIP 09) MT518  
Comparison Request Cancel (due to Match) sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM011 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104142 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 

---

## Page 153

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 153 
MESSAGE SAMPLE (STIP 09) MT518  
Comparison Request Cancel (due to Match) sent to Dealer A  
FIELD DESCRIPTION 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000003 [[Buyer]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000001 [[participant]] Declaration Details Narrative (Contra) 
Trade Reference 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVSTIP/MSGRMACH Trade Instruction Processing Narrati ve 
Trade Service Type – STIP Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 154

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 154 
2.18.10 (STIP 10) MT518 Comparison Request Cancel (due to Match) 
MESSAGE SAMPLE (STIP 10) MT518  
 Comparison Request Cancel (due to Match) sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM012 Sender’s RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104755 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000002 [[participant]] Declaration Details Narrative (Contra) 
Trade Reference 
:16S:CONFPRTY Repeat Block End 

---

## Page 155

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 155 
MESSAGE SAMPLE (STIP 10) MT518  
 Comparison Request Cancel (due to Match) sent to Dealer C  
FIELD DESCRIPTION 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVSTIP/MSGRMACH Trade Instruction Processing Narrative 
Trade Service Type – STIP Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
2.18.11 (STIP 11) MT518 Trade Novated 
MESSAGE SAMPLE (STIP 11) MT518  [[Novation]] for Dealer A  FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM013 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104743 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 List Reference Number  (trade [[ID]])  
:16S:LINK Repeat Block End 

---

## Page 156

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 156 
MESSAGE SAMPLE (STIP 11) MT518  [[Novation]] for Dealer A  FIELD DESCRIPTION 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/NOVT [[Novation]] Advice 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTFSTI Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVSTIP Trade Instruction Processing Narrative 
Trade Service Type – STIP Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
 
  

---

## Page 157

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 157 
2.18.12 (STIP 12) MT518 Trade Novated 
MESSAGE SAMPLE (STIP 12) MT518  [[Novation]] for Dealer C  FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM014 Sender’s RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104743 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000002 List Reference Number  (trade [[ID]])  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/NOVT [[Novation]] Advice 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTFSTI Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 

---

## Page 158

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 158 
MESSAGE SAMPLE (STIP 12) MT518  [[Novation]] for Dealer C  FIELD DESCRIPTION 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVSTIP Trade Instruction Processing Narrative 
Trade Service Type – STIP Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 159

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 159 
2.19 Set 19 
In this set, the following messages are included (shaded in gray). 
[[Broker]] BDealer C
NETPOS (20)
MT509 Trade Create Accepted
Continued from PMAT 
Trade in Set 1
(01) – (18)
RTTM
NETPOS (21)
MT518 Comparison Request
NETPOS (19)
MT515 Instruct
NETPOS (22)
MT515 Instruct
NETPOS (24)
MT518 Comparison Request
NETPOS (25)
MT509 Trade Matched
NETPOS (28)
MT509 Trade PMAT
NETPOS (31)
MT518 Comparison Request 
Cancel (due to match)
NETPOS (30)
MT518 Comparison Request 
Cancel (due to match)
NETPOS (29)
MT518 Comparison Request 
Cancel (due to match)
NETPOS (27)
MT509 Trade Matched
NETPOS (23)
MT509 Trade Create Accepted
NETPOS (26)
MT509 Trade Matched
NETPOS (32)
MT509 Trade FMAT
NETPOS (34)
MT518 Trade Novated
Dealer A
NETPOS (33)
MT518 Trade Novated
 
Description Messages 
Dealer A and [[Broker]] B submit trades of the same terms and par value and they match, 
resulting in a PMAT [[Broker]] trade.  Dealer C then submits multiple trades that are matched 
against the [[Broker]] trade via Split/Splice, resulting in a FMAT [[Broker]] trade.  
(01) – (18) 
and  
NETPOS (19) – (34) 

---

## Page 160

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 160 
2.19.1 (NETPOS 19) MT515 Instruct 
MESSAGE SAMPLE (NETPOS 19) MT515 Dealer C Submits Buy 
Trade Instruct for 3MM Sell to RTTM (Trade Create)  
FIELD DESCRIPTION 
PSSWRD123 Password  
DLRC Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRC0331 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306100526 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Sell 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing  
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/3000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 

---

## Page 161

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 161 
MESSAGE SAMPLE (NETPOS 19) MT515 Dealer C Submits Buy 
Trade Instruct for 3MM Sell to RTTM (Trade Create)  
FIELD DESCRIPTION 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trades  
:16S:CONFDET Block End 
- End of Message 
2.19.2 (NETPOS 20) MT509 Trade Create Accepted 
MESSAGE SAMPLE (NETPOS 20 )  MT509  
Trade Create Accepted sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM020 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306100913 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRC0331 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000003 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 162

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 162 
2.19.3 (NETPOS 21) MT518 Comparison Request 
MESSAGE SAMPLE (NETPOS 21) MT518  
Comparison Request for Matching Sell sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BRKB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM021 Sender’s RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306100952 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000003 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/3000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 

---

## Page 163

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 163 
2.19.4 (NETPOS 22) MT515 Instruct 
MESSAGE SAMPLE (NETPOS 22) MT515 Dealer C Submits Buy 
Trade Instruct for 2MM Sell to RTTM (Trade Create)  
FIELD DESCRIPTION 
PSSWRD123 Password  
DLRC Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRC0332 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306100526 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC002 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Sell 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing  
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/2000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 [[CUSIP]] 

---

## Page 164

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples 
Version C ontrol Page 164 
MESSAGE SAMPLE (NETPOS 22) MT515 Dealer C Submits Buy 
Trade Instruct for 2MM Sell to RTTM (Trade Create)  
FIELD DESCRIPTION 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trades  
:16S:CONFDET Block End 
- End of Message 
2.19.5 (NETPOS 23) MT509 Trade Create Accepted 
MESSAGE SAMPLE (NETPOS 23)  MT509  
Trade Create Accepted  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM022 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306100913 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC002 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRC0332 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000004 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 165

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 165 
2.19.6 (NETPOS 24) MT518 Comparison Request 
MESSAGE SAMPLE (NETPOS 24) MT518  
Comparison Request for Matching Sell sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BRKB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM023 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306100952 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095810 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000004 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/3000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 

---

## Page 166

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 166 
2.19.7 (NETPOS 25) MT509 Trade Matched 
MESSAGE SAMPLE (NETPOS 25) MT509  
Transaction Matched sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM024 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104136 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000003 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:20C::BASK//BMID002 [[Broker]] Match Identifier  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
 
  

---

## Page 167

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 167 
2.19.8 (NETPOS 26) MT509 Trade Matched 
MESSAGE SAMPLE (NETPOS 26) MT509  
Transaction Matched sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM025 Sender’s RTTM Reference for this  Message 
:23G:INST Message Function - Instruct 
:98C::PREP//20010306104136 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC002 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000004 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:20C::BASK//BMID002 [[Broker]] Match Identifier  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.19.9 (NETPOS 27) MT509 Trade Matched 
MESSAGE SAMPLE (NETPOS 27) MT509  
Transaction Matched sent to [[Broker]] B  
FIELD DESCRIPTION 
 
Same as message (23) 
  

---

## Page 168

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 168 
2.19.10 (NETPOS 28) MT509 Trade PMAT 
MESSAGE SAMPLE (NETPOS 28) MT509  
Transaction Matched sent to [[Broker]] B PMAT (Short Side)  
FIELD DESCRIPTION 
 
Same as message (24) 
2.19.11 (NETPOS 29) MT518 Comparison Request Cancel (due to match) 
MESSAGE SAMPLE (NETPOS 29) MT518  
Comparison Request Cancel  (due to Match) sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BRKB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM028 Sender’s RTTM Reference for this  Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104755 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CADV Comparison Request Cancel 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  

---

## Page 169

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 169 
MESSAGE SAMPLE (NETPOS 29) MT518  
Comparison Request Cancel  (due to Match) sent to [[Broker]] B  
FIELD DESCRIPTION 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000003 [[Seller]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000001 [[participant]] Declaration Details Narrative (Contra) 
Trade Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/3000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRMACH Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
- End of Message 
2.19.12 (NETPOS 30) MT518 Comparison Request Cancel (due to match) 
MESSAGE SAMPLE (NETPOS 30) MT518  
Comparison Request Cancel (due to Match) sent to [[Broker]] B  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BRKB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM029 Sender’s RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20010306104755 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095714 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 

---

## Page 170

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 170 
MESSAGE SAMPLE (NETPOS 30) MT518  
Comparison Request Cancel (due to Match) sent to [[Broker]] B  
FIELD DESCRIPTION 
:90A::DEAL//PRCT/99,119140625 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000004 [[Seller]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000001 [[participant]] Declaration Details Narrative (Contra) 
Trade Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/2000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD/MSGRMACH Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
- End of Message 
2.19.13. (NETPOS 31) MT518 Comparison Request Cancel (due to match) 
MESSAGE SAMPLE (NETPOS 31) MT518  
Comparison Request Cancel (due to Match) sent to Dealer C  
FIELD DESCRIPTION 
 
Same as message (26) 
 
2.19.14. (NETPOS 32) MT509 Trade FMAT 
MESSAGE SAMPLE (NETPOS 32) MT509  
Trade Fully Matched sent to [[Broker]] B  
FIELD DESCRIPTION 
 
Same as message (27)  

---

## Page 171

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 171 
2.19.15. (NETPOS 33) MT518 Trade Novated 
MESSAGE SAMPLE (NETPOS 33) MT518  [[Novation]] for Dealer A  FIELD DESCRIPTION 
 
Same as message (28) 
2.19.16 (NETPOS 34) MT518 Trade Novated 
MESSAGE SAMPLE (NETPOS 33) MT518  [[Novation]] for Dealer C  FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM021 Sender’s RTTM Reference for this  Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010306104743 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::LIST//2049000002 List Reference Number  (trade [[ID]])  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BMID002 [[Broker]] Match Identifier  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20010307 [[settlement]] Date 
:90A::DEAL//PRCT/99,125 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/NOVT [[Novation]] Advice 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit  
:16R:CONFPRTY Mandatory Repeat Block Start  

---

## Page 172

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 172 
MESSAGE SAMPLE (NETPOS 33) MT518  [[Novation]] for Dealer C  FIELD DESCRIPTION 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTFTBA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Security Identifier – [[CUSIP]] 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
Note: 
As this trade was created as a result of splice matching (e.g. , multiple dealer trades combined to form a trade), it does not 
have a corresponding [[Member]] -Xref. Therefore, tag “20C::MAST” is not present.  
  

---

## Page 173

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 173 
2.20 Set 20 
In this set, the following messages are included (shaded in gray). 
Dealer A
OPT (01) 
MT515 Instruct
OPT (02)
MT509 Trade Create Accepted
Dealer C
OPT (03)
MT518 Comparison Request
STIP (04) 
MT515 InstructRTTM
 
Description Message Sequence 
Dealer A submits a Trade Create to RTTM for a sell of a [[Put Option]] to dealer C. RTTM 
sends a Trade Create Accepted to Dealer A and a Comparison Request to Dealer C.  
OPT (01) - (03) 
2.20.1 (OPT 01) MT515 Instruct 
MESSAGE SAMPLE (OPT 01) MT515  
Dealer A Submits [[Option]] Trade to RTTM  
FIELD DESCRIPTION 
PSSWRD123 Password  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA083 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010321154708 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA056 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20010321154623 Trade Date & Time 

---

## Page 174

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 174 
MESSAGE SAMPLE (OPT 01) MT515  
Dealer A Submits [[Option]] Trade to RTTM  
FIELD DESCRIPTION 
:98A::SETT//20010701 [[settlement]] Date 
:90A::DEAL//PRCT/96,75 Deal Price – Percentage 
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing  
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/10000000, Quantity as Face Amount (Par)  
:35B:/US/02R060670 [[CUSIP]] 
:16R:FIA Block Start 
:12B::OPTI//PUTO [[Option]] Type - Put 
:98A::EXPI//20010606 Expiry Date 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVOPTN Trade Instruction Processing Narrative 
Trade Service Type - [[Option]] 
:16S:CONFDET Block End 
- End of Message 
2.20.2 (OPT 02) MT509 Trade Create Accepted 
MESSAGE SAMPLE (OPT 02) MT509  
[[Option]] Trade Create Accepted sent to Dealer A  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFRTTM092 Sender’s RTTM Reference for this  Message 

---

## Page 175

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 175 
MESSAGE SAMPLE (OPT 02) MT509  
[[Option]] Trade Create Accepted sent to Dealer A  
FIELD DESCRIPTION 
:23G:INST Message Function - Instruct 
:98C::PREP//20010321154722 Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA056 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA083 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7107002238 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
2.20.3 (OPT 03) MT518 Comparison Request 
MESSAGE SAMPLE (OPT 03) MT518  
Comparison Request for Matching [[Option]] Buy sent to Dealer C  
FIELD DESCRIPTION 
 Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//SENREFRTTM093 Sender’s RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20010321154723 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  

---

## Page 176

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 176 
MESSAGE SAMPLE (OPT 03) MT518  
Comparison Request for Matching [[Option]] Buy sent to Dealer C  
FIELD DESCRIPTION 
:98C::TRAD//20010321154623 Trade Date & Time 
:98A::SETT//20010701 [[settlement]] Date 
:90A::DEAL//PRCT/96,75 Deal Price – Percentage 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7107002238 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/10000000, Quantity as Face Amount (Par)  
:35B:/US/02R060670 Security Identifier – [[CUSIP]] 
:16R:FIA Block Start 
:12B::OPTI//PUTO [[Option]] Type - Put 
:98A::EXPI//20010606 Expiry Date 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVOPTN Trade Instruction Processing Narrative  
Trade Service Type - [[Option]] 
:16S:CONFDET Block End 
 End of Message 

---

## Page 177

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 177 
3. SPECIFIED POOL TRADE (SPT) DEALER MESSAGE 
SAMPLES  
This section contains samples for Specified Pool Trades between Dealers. The examples are based on the 
following: 
On March 6, 2011, Dealer [[participant]] C (account “DLRC”) buys $5,000,000 of Pool AW9961 (TBA [[CUSIP]] 
01F050650, [[issuer]] F, Pool [[CUSIP]] 3138Y0B71) from Dealer [[participant]] A (account “DLRA”). The trade is 
executed at a price of 100, to settle trade for trade (TFTD) for next day (March 7) [[settlement]]. The factor for this 
fictitious trade is 1.0. 
The reference numbers used by the various parties to this trade, as well as those assigned by RTTM, are 
summarized in the grid below: 
Reference Numbers Dealer [[participant]] A  
(account “DLRA”)  
Dealer [[participant]] C  
(account “DLRC”)  
Sender’s Reference SENREFDLRA015 SENREFDLRC0331 
X-ref XREFDLRA001 XREFDLRC001 
RTTM Submission [[ID]]  N/A N/A 
RTTM Transaction [[ID]]  7096000001 7096000003 
RTTM Trade [[ID]] 2049000001 2049000002 
 
Based on the above trade details, the scenarios below have been constructed. Each of these scenarios is 
illustrated by a series of message samples, which represent a “flow” of events. The grid below describes each 
of these scenarios and indicates which sequence of message samples corresponds to a given scenario: 
# Scenario Message Sequence 
1 Dealer A submits sel l to RTTM, identifying the poo l using TBA [[CUSIP]] and Pool Number. (01) – (03) 
2 Dealer A submits sell to RTTM with incorrect final money ; the pool is identified using 
TBA [[CUSIP]] and Pool Number.  
DEFVAL (01) – (04) 
3 Dealer A’s trade is repriced due to factor update (pre-comparison) – the factor is .85 (01) – (03) 
and  
REP (04) 
4 Dealer A’s trade is repriced due to factor update (pre- comparison) - factor is zero; 
Dealer A’s trade instruct is deleted due to fully paid -down security and Dealer C’s 
comparison request is cancelled due to system action.  
(01) – (03) 
and  
MKDL (04) – (06) 
5 Dealer A submits sell to RTTM using [[issuer]] and pool number; Dealer C submits using 
pool [[CUSIP]] only; they compare and get novated – noting that all MT518 messages 
relating to the SPT reflec ts TBA [[CUSIP]] and pool number, regardless of how the pool 
was identified in the MT515.  
POOLID (01) - (12) 

---

## Page 178

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 178 
# Scenario Message Sequence 
6 Dealer A’s trade is repriced due to factor update (post -comparison) – factor is zero; 
trade is deleted due to fully paid -down security.  
MKDL(13) – (16) 
3.1 Set 1 
In this set, the following messages are included (shaded in gray). 
Dealer A
(01) 
MT515 Instruct
(02)
MT509 Trade Create Accepted
Dealer B
(03)
MT518 Comparison Request
RTTM
 
Scenario Message Sequence 
Dealer A submits sell to RTTM, identifying the pool using TBA [[CUSIP]] and Pool Number.  (01) – (03) 
3.1.1 (01) MT515 Instruct 
MT515 Dealer A Submits Sell to RTTM 
Field/Tag Field Description 
<password>  Password (not shown)  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA015 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20110306100526 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  

---

## Page 179

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 179 
MT515 Dealer A Submits Sell to RTTM 
Field/Tag Field Description 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing 
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 

---

## Page 180

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 180 
3.1.2 (02) M509 Trade Create Accepted 
MT509 Trade Create Accepted sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA015 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/ Validated  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
3.1.3 (03) MT518 Comparison Request 
MT518 Comparison Request for Matching Buy sent to Dealer C  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 

---

## Page 181

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 181 
MT518 Comparison Request for Matching Buy sent to Dealer C  
Field/Tag Field Description 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/123456 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 

---

## Page 182

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 182 
3.2 Set 2 
In this set, the following messages are included (shaded in gray). 
Dealer A
DEFVAL (01) 
MT
515 Instruct
DEFVAL (02)
MT509 Trade Create Accepted
Dealer B
DEFVAL (04)
MT518 Comparison Request
DEFVAL (03)
MT518 Notification of 
[[default]] Values Applied
RTTM
 
Scenario Messages 
Dealer A submits sell to RTTM with incorrect final money; the pool is identified using TBA 
[[CUSIP]] and Pool Number.  
DEFVAL (01) – (04) 
3.2.1 (DEFVAL 01) MT515 Instruct 
MT515 Dealer A Submits Sell to RTTM, where the final money is incorrect.  
Field/Tag Field Description 
 
This message is the same as (01), with the following changes: 
• The Final Money value specified by the [[Member]] is incorrect ==> :19A::SETT//USD5000000, 
3.2.2 (DEFVAL 02) MT509 Trade Create Accepted 
MT509 Trade Create Accepted sent to Dealer A  
Field/Tag Field Description 
 
This message is the same as (02) 

---

## Page 183

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 183 
3.2.3 (DEFVAL 03) MT518 [[default]] Values Applied 
MT518 [[default]] Values Applied Record Sent to Dealer A with corrected final money.  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/DFVA [[default]] Values Applied Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  

---

## Page 184

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 184 
MT518 [[default]] Values Applied Record Sent to Dealer A with corrected final money.  
Field/Tag Field Description 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to RTTM Action  
:16S:CONFDET Block End 
- End of Message 
3.2.4 (DEFVAL 04) MT518 Comparison Request 
MT518 Comparison Request for Matching Buy sent to Dealer C with correct final money 
Field/Tag Field Description 
 
This message is the same as (03) 
  

---

## Page 185

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 185 
3.3 Set 3 
In this set, the following messages are included (shaded in gray). 
Dealer A
(01) 
MT515 Instruct
(02)
MT509 Trade Create Accepted
Dealer B
(03)
MT518 Comparison Request
REP (04)
MT518 Repricing
RTTM
Factor 
Update
 
Scenario Message Sequence 
Dealer A’s trade is repriced due to factor update (pre-comparison) – the factor is .85 (02) – (03) 
and  
REP (04) 
3.3.1 (REP 04) MT518 Repricing 
MT518 Repricing Record Sent to Dealer A (for Unmatched Trade) - Factor Update of .85 
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 

---

## Page 186

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 186 
MT518 Repricing Record Sent to Dealer A (for Unmatched Trade) - Factor Update of .85 
Field/Tag Field Description 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD4253541,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/YTPR Repricing Record Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to RTTM Action  
:16S:CONFDET Block End 
- End of Message 
 
  

---

## Page 187

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 187 
3.4 Set 4 
In this set, the following messages are included (shaded in gray). 
Dealer A
(01) 
MT
515 Instruct
(02)
MT509 Trade Accepted
Dealer C
(03)
MT518 Comparison Request
MKDL (04)
MT518 Repricing
MKDL (05)
MT509 Instruct Deleted (due to 
Fully Paid-Down Security)
RTTM
MKDL (06)
MT518 Comparison Request 
Cancel (due to System Action)
Factor 
Update
[[EOD]] 
Processing
 
Scenario Message Sequence 
Dealer A’s trade is repriced due to factor update (pre-comparison) - factor is zero; Dealer A’s 
trade instruct is deleted due to fully paid -down security and Dealer C’s comparison request is 
cancelled due to system action.  
(02) – (03) 
and  
MKDL (04) – (06) 
3.4.1 (MKDL 04) MT518 Repricing 
MT518 Repricing Record Sent to Dealer A (for Unmatched Trade) - Zero Factor 
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 

---

## Page 188

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 188 
MT518 Repricing Record Sent to Dealer A (for Unmatched Trade) - Zero Factor 
Field/Tag Field Description 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD0, [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/YTPR Repricing Record Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Tr ade 
Message Reason - Due to RTTM Action  
:16S:CONFDET Block End 
- End of Message 

---

## Page 189

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 189 
3.4.2 (MKDL 05) MT509 Trade Instruct Marked for Deletion 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/DEPS Pool Instruct Marked for Deletion due to Fully 
Paid-Down Security 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
Note: 
This message will be sent end -of-day of Contractual [[settlement]] Date (“CSD”) and is not a real - time message. 
  

---

## Page 190

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 190 
3.4.3 (MKDL 06) MT518 Comparison Request Cancel (due to System) 
MT518 Comparison Request Cancel (Due to System) sent to Dealer C  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD0, [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  

---

## Page 191

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 191 
MT518 Comparison Request Cancel (Due to System) sent to Dealer C  
Field/Tag Field Description 
:35B:/US/01F050650 Security Identifier – [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to System Action  
:16S:CONFDET Block End 
- End of Message 
3.5 Set 5 
In this set, the following messages are included (shaded in gray). 
Dealer A
POOLID (01) 
MT515 Instruct
POOLID (02)
MT509 Trade Create Accepted
Dealer C
POOLID (03)
MT518 Comparison Request
POOLID (04) 
MT515 Instruct
POOLID (06)
MT518 Comparison Request
POOLID (05)
MT509 Trade Create Accepted
POOLID (07)
MT509 Trade Create Matched
POOLID (08)
MT509 Trade Create Matched
POOLID (09)
MT518 Comparison Request 
Cancel (due to Match)
POOLID (10)
MT518 Comparison Request 
Cancel (due to Match)
RTTM
POOLID (11)
MT518 Trade Novated
POOLID (12)
MT518 Trade Novated
 
Scenario Message Sequence 
Dealer A submits sell to RTTM using [[issuer]] and pool number; Dealer C submits using pool 
[[CUSIP]] only; they compare and get novated – noting that all MT518 messages relating to the 
SPT reflects TBA [[CUSIP]] and pool number, regardless of how the pool was identified in the 
MT515. 
POOLID (01) - (12)  
  

---

## Page 192

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 192 
3.5.1 POOLID (01) MT515 Instruct 
MT515 Instruct Dealer A Submits Sell to RTTM ([[issuer]] and Pool Number)  
Field/Tag Field Description 
<password>  Password  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA015 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20110306100526 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing 
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  

---

## Page 193

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 193 
MT515 Instruct Dealer A Submits Sell to RTTM ([[issuer]] and Pool Number)  
Field/Tag Field Description 
:35B:/US/NONCUSIP NO TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961/ISSR/F Pool Number and [[issuer]]  
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
3.5.2 POOLID (02) MT509 Trade Create Accepted 
MT509 Trade Create Accepted sent to Dealer A  
Field/Tag Field Description 
 
This message is the same as (02) 
3.5.3 POOLID (03) MT518 Comparison Request 
MT518 Comparison Request for Matching Buy sent to Dealer C  
Field/Tag Field Description 
 
This message is the same as (03) 
3.5.4 POOLID (04) MT515 Instruct 
MT515 Instruct Dealer C Submits Buy to RTTM (Pool [[CUSIP]] Only)  
Field/Tag Field Description 
<password>  Password  
DLRC Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRC0331 Sender’s Reference for this Message 

---

## Page 194

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 194 
MT515 Instruct Dealer C Submits Buy to RTTM (Pool [[CUSIP]] Only)  
Field/Tag Field Description 
:23G:NEWM Message Function = New  
:98C::PREP//20110306400126 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing 
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
35B:/US/NONCUSIP TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/CUSP/AW9961 Pool Number [[CUSIP]] 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 

---

## Page 195

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 195 
3.5.5 POOLID (05) MT509 Trade Create Accepted 
MT509 Trade Create Accepted sent to Dealer C  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRC0331 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000003 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/ Validated  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
 
  

---

## Page 196

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 196 
3.5.6 POOLID (06) MT518 Comparison Request 
MT518 Comparison Request for Matching Sell sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67  [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000003 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 

---

## Page 197

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 197 
MT518 Comparison Request for Matching Sell sent to Dealer A  
Field/Tag Field Description 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
Note: 
TBA [[CUSIP]] and Pool Number are populated.  
3.5.7 POOLID (07) MT509 Trade Matched 
MT509 Trade Matched sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender’s RTTM Reference for this message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//2049000001 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  

---

## Page 198

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 198 
MT509 Trade Matched sent to Dealer A  
Field/Tag Field Description 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
3.5.8 POOLID (08) MT509 Trade Matched 
MT509 Trade Matched sent to Dealer C  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender’s RTTM Reference for this message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000003 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//2049000002 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 199

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 199 
3.5.9 POOLID (09) MT518 Comparison Request Cancel (due to Match) 
MT518 Comparison Request Cancel (Due to System) sent to Dealer A   
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67  [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000003 [[Seller]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000001 [[participant]] Declaration Details Narrative  
(Contra) Trade Reference 

---

## Page 200

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 200 
MT518 Comparison Request Cancel (Due to System) sent to Dealer A   
Field/Tag Field Description 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 Security Identifier – [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRMACH Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
- End of Message 
3.5.10 POOLID (10) MT518 Comparison Request Cancel (due to Match) 
MT518 Comparison Request Cancel (Due to System) sent to Dealer C   
Field/Tag Field Description 
 <password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 

---

## Page 201

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 201 
MT518 Comparison Request Cancel (Due to System) sent to Dealer C   
Field/Tag Field Description 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67  [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000002 [[participant]] Declaration Details Narrative (Contra ) 
Trade Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 Security Identifier – [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961  Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRMACH Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
- End of Message 
3.5.11 POOLID (11) MT518 Trade Novated 
MT518 Trade Novated sent to Dealer A   
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 

---

## Page 202

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 202 
MT518 Trade Novated sent to Dealer A   
Field/Tag Field Description 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender’s RTTM Reference for this message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST/2049000001 List Reference Number  (trade [[ID]])  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67  [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/NOVT [[Novation]] Advice 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTFSPT Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 Security Identifier – [[CUSIP]] 
:16R:FIA Block Start 

---

## Page 203

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 203 
MT518 Trade Novated sent to Dealer A   
Field/Tag Field Description 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
3.5.12 POOLID (12) MT518 Trade Novated 
MT518 Trade Novated sent to Dealer C  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender’s RTTM Reference for this message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST/2049000002 List Reference Number  (trade [[ID]])  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20010306095844 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 

---

## Page 204

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 204 
MT518 Trade Novated sent to Dealer C  
Field/Tag Field Description 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/NOVT [[Novation]] Advice 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTFSPT Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 Security Identifier – [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
 
  

---

## Page 205

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 205 
3.6 Set 6 
In this set, the following messages are included (shaded in gray). 
Dealer A Dealer C
MKDL (13)
MT518 Repricing
MKDL (15)
MT509 Instruct Deleted (due to 
Fully Paid-Down Security)
RTTM
MKDL (16)
MT518 Comparison Request 
Cancel (due to System Action)
Factor 
Update
[[EOD]] 
Processing
Continued from FMAT 
Trade in Set 5
POOLID (01) – (12)
MKDL (14)
MT518 Repricing
 
Scenario Message Sequence 
Dealer A’s trade is repriced due to factor update (post -comparison) – factor is zero; trade is 
deleted due to fully paid -down security.  
MKDL (13) – (16) 
3.6.1 (MKDL 13) MT518 Repricing 
MT518 Repricing (Zero Factor) Record Sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  

---

## Page 206

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 206 
MT518 Repricing (Zero Factor) Record Sent to Dealer A  
Field/Tag Field Description 
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD0, [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/YTPR Repricing Record Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTFSPT Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End  
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Tr ade 
Message Reason - Due to RTTM Action  
:16S:CONFDET Block End 
- End of Message 

---

## Page 207

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Exampl es 
Version C ontrol Page 207 
3.6.2 (MKDL 14) MT518 Repricing 
MT518 Repricing (Zero Factor) Record Sent to Dealer C  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000002 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD0, [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - [[Buyer]] 
:22F::PROC/GSCC/YTPR Repricing Record Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTFSPT Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 

---

## Page 208

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 208 
MT518 Repricing (Zero Factor) Record Sent to Dealer C  
Field/Tag Field Description 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Tr ade 
Message Reason - Due to RTTM Action  
:16S:CONFDET Block End 
- End of Message 
3.6.3 (MKDL 15) MT509 Trade Instruct Marked for Deletion 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security) sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA015 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Transaction Reference 

---

## Page 209

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 209 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security) sent to Dealer A  
Field/Tag Field Description 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/DEPS Pool Instruct Marked for Deletion due to Fully 
Paid-Down Security 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
Note: 
This message will be sent end -of-day of Contractual [[settlement]] Date (“CSD”) and is not a real - time message. 
3.6.4 (MKDL 16) MT509 Trade Instruct Marked for Deletion 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security) sent to Dealer C  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRC001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLR33115 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 

---

## Page 210

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 210 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security) sent to Dealer C  
Field/Tag Field Description 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/DEPS Pool Instruct Marked for Deletion due to Fully 
Paid-Down Security 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
Note: 
This message will be sent end -of-day of Contractual [[settlement]] Date (“CSD”) and is not a real - time message. 

---

## Page 211

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 211 
4. SPECIFIED POOL TRADE (SPT) [[Broker]]-TO-DEALER 
MESSAGE SAMPLES  
This section contains samples for Specified Pool Trades between [[Broker]] and Dealers. The examples are 
based on the following: 
On March 6, 2011, [[Broker]] [[participant]] B (account “BRKB”) buys $5,000,000 of Pool AW9961 (TBA [[CUSIP]] 
01F050650 [[issuer]] F, Pool [[CUSIP]] 3138Y0B71) from Dealer [[participant]] A (account “DLRA”) and sells the same 
$5,000,000 to Dealer [[participant]] C (account “DLRC”). Both trades are executed at a price of 100 and are to 
settle trade-for-trade (TFTD) for next day (March 7) [[settlement]] using Exact Match. [[Broker]] [[participant]] B 
charges a commission rate of 3/512 of a percent to Dealer [[participant]] A and no commission to Dealer 
[[participant]] C. The factor for this fictitious trade is 1.0. 
The reference numbers used by the various parties to this trade, as well as those assigned by RTTM, are 
summarized in the grid below. 
Reference Numbers Dealer [[participant]] A 
(account “DLRA”)  
[[Broker]] [[participant]] B  
(account “BRKB”)  
Dealer [[participant]] C 
(account “DLRC”)  
Sender’s Reference SENREFDLRA015 SENREFBKRB0221 (buy)  
SENREFBKRB0222 (sell)  
SENREFDLRC0331 
X-REF XREFDLRA001 XREFBKRB021B (buy)  
XREFBKRB021S (sell)  
XREFDLRC001 
[[Broker]] Reference N/A BREF021 N/A 
[[Broker]] Match Identifier  BMID001 N/A BMID002 
RTTM Submission [[ID]]  N/A 000001-1306 (buy)  
000002-1306 (sell)  
N/A 
RTTM Transaction [[ID]]  7096000001 7096000002 7096000003 
RTTM Trade [[ID]]  2049000001 2049000002 
 
Based on the above trade details, the scenarios below have been constructed. Each of these scenarios is 
illustrated by a series of message samples that represent a “flow” of events. The grid below describes each of 
these scenarios and indicates which sequence of message samples corresponds to a given scenario: 
# Scenario Message Sequence 
1 [[Broker]] B submits both legs of the trade and then Dealer A submits their  sell (PMAT); the 
trade is repriced (due to factor update of .85)  
(01) – (20) 
2 [[Broker]] B submits both sides of the trade but with incorrect final money. RTTM defaults 
to the correct final money.  
DFLT VAL (01) - (12) 
3 PMAT Marked for Deletion (due to fully paid -down security)  (01) - (18) 
TRD DEL (19) - (25) 

---

## Page 212

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 212 
4.1 Set 1 
In this set, the following messages are included (shaded in gray). 
[[Broker]] B [[Broker]] B
[[Broker]] B
(03)
MT509 Trade Create Unbalanced
(07)
MT509 Trade Create Balanced
(02)
MT509 Trade Create Accepted
(05)
MT509 Trade Create Accepted
(06)
MT509  Trade Create Unbalanced
(08)
MT509 Trade Create Balanced
(01)
MT515 Instruct (vs. A)
(04) 
MT515 Instruct (vs. C)
Dealer A
(09)
MT518 Comparison Request
(12)
MT509 Trade Create Accepted
(14)
MT509 Trade Create Matched
(17)
MT518 Comparison Request 
Cancel (due to match)
(13)
MT518 Comparison Request
(15)
MT509 Trade Create Matched
(16)
MT509 Trade PMAT (long side)
(18)
MT518 Comparison Request 
Cancel (due to match)
(11) 
MT515 Instruct
[[Broker]] BDealer C
RTTM
(10)
MT518 Comparison Request
(21)
MT518 Repricing (19)
MT518 Repricing (vs. A)
(20)
MT518 Repricing (vs. C)
 
# Scenario Message Sequence 
1 [[Broker]] B submits both legs of the trade and then Dealer A submits their  sell (PMAT); the 
trade is repriced (due to factor update of .85)  
(01)– (20) 
4.1.1 (01) MT515 Instruct 
MT515 [[Broker]] B Submits Buy (Long Side) to RTTM vs. A  
Field/Tag Field Description 
<password>  Password  
BKRB Sender  

---

## Page 213

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 213 
MT515 [[Broker]] B Submits Buy (Long Side) to RTTM vs. A  
Field/Tag Field Description 
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0221 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20110306103913 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type – Buy 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing 
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  

---

## Page 214

MBSD RTTM® [[Novation]]: SWIFT I nteractive Messaging Examples 
Version C ontrol Page 214 
MT515 [[Broker]] B Submits Buy (Long Side) to RTTM vs. A  
Field/Tag Field Description 
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
4.1.2 (02) MT509 Trade Create Accepted 
MT509 Trade Create Accepted sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function – Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 

---

## Page 215

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 215 
MT509 Trade Create Accepted sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
:20C::RELA//SENREFBKRB0221 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.1.3 (03) MT509 Trade Unbalanced 
MT509 Transaction Unbalanced sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function – Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Submission Reference 

---

## Page 216

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 216 
MT509 Transaction Unbalanced sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TUNB Trade Create Unbalanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.1.4 (04) MT515 Instruct 
MT515 [[Broker]] B Submits Sell (Short Side) to RTTM vs. C  
Field/Tag Field Description 
<password>  Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0222 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20110306104038 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 

---

## Page 217

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Exam ples 
Version C ontrol Page 217 
MT515 [[Broker]] B Submits Sell (Short Side) to RTTM vs. C  
Field/Tag Field Description 
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004166,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type – Sell 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing 
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
4.1.5 (05) MT509 Trade Create Accepted 
MT509 Trade Create Accepted sent to [[Broker]] B (Short Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  

---

## Page 218

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 218 
MT509 Trade Create Accepted sent to [[Broker]] B (Short Side)  
Field/Tag Field Description 
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function – Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0222 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000002-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.1.6 (06) MT509 Trade Unbalanced 
MT509 Transaction Unbalanced sent to [[Broker]] B (Short Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 

---

## Page 219

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 219 
MT509 Transaction Unbalanced sent to [[Broker]] B (Short Side)  
Field/Tag Field Description 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function – Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000002-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TUNB Trade Create Unbalanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.1.7 (07) MT509 Trade Balanced 
MT509 Transaction Balanced sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function – Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 

---

## Page 220

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 220 
MT509 Transaction Balanced sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//000001-1306 Previous Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TBAL Trade Create Balanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.1.8 (08) MT509 Trade Balanced 
MT509 Transaction Balanced sent to [[Broker]] B (Short Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function – Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  

---

## Page 221

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 221 
MT509 Transaction Balanced sent to [[Broker]] B (Short Side)  
Field/Tag Field Description 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//000002-1306 Previous Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TBAL Trade Create Balanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.1.9 (09) MT518 Comparison Request 
MT518 Comparison Request for Matching Sell sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  

---

## Page 222

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 222 
MT518 Comparison Request for Matching Sell sent to Dealer A  
Field/Tag Field Description 
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type – Sell 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:20C::PROC//7096000002 [[Buyer]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 223

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 223 
4.1.10 (10) MT518 Comparison Request 
MT518 Comparison Request for Matching Buy sent to Dealer C  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type – Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 

---

## Page 224

MBSD RTTM® [[Novation]]: SWIFT  Interactive Messaging Examples 
Version C ontrol Page 224 
MT518 Comparison Request for Matching Buy sent to Dealer C  
Field/Tag Field Description 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
4.1.11 (11) MT515 Instruct 
MT515 Dealer A Submits Sell to RTTM 
Field/Tag Field Description 
PSSWRD123 Password  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFDLRA015 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20110306100526 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/99,994140625 Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type – Sell 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing 
Indicator 
:22H::PAYM//APMT Against Payment Indicator  

---

## Page 225

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 225 
MT515 Dealer A Submits Sell to RTTM 
Field/Tag Field Description 
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
4.1.12 (12) MT509 Trade Create Accepted 
MT509 Trade Create Accepted sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function – Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 

---

## Page 226

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 226 
MT509 Trade Create Accepted sent to Dealer A  
Field/Tag Field Description 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFDLRA015 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.1.13 (13) MT518 Comparison Request 
MT518 Comparison Request for Matching Buy sent to [[Broker]] B  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/99,994140625 Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  

---

## Page 227

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Ex amples 
Version C ontrol Page 227 
MT518 Comparison Request for Matching Buy sent to [[Broker]] B  
Field/Tag Field Description 
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
4.1.14 (14) MT509 Trade Matched 
MT509 Transaction Matched sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 

---

## Page 228

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 228 
MT509 Transaction Matched sent to Dealer A  
Field/Tag Field Description 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//2049000001 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BMID001 [[Broker]] Match Identifier  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.1.15 (15) MT509 Trade Matched 
MT509 Transaction Matched sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message  
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 

---

## Page 229

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 229 
MT509 Transaction Matched sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//2049000001 RTTM Assigned Trade (Match) Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH//MACH Trade Create has been Matched  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.1.16 (16) MT509 PMAT (Long Side) 
MT509 Trade Partially Matched (Long Side) sent to [[Broker]] B  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 

---

## Page 230

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 230 
MT509 Trade Partially Matched (Long Side) sent to [[Broker]] B  
Field/Tag Field Description 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//7096000002 Previous Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Trade Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::MTCH/GSCC/MAPL Trade Partially Matched - Long Side 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.1.17 (17) MT518 Comparison Request Cancel (due to Match) 
MT518 Comparison Request Cancel (due to Match) sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 

---

## Page 231

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 231 
MT518 Comparison Request Cancel (due to Match) sent to Dealer A  
Field/Tag Field Description 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BMID001 [[Broker]] Match Identifier  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000001 [[participant]] Declaration Details Narrative 
(Contra) Trade Reference 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 

---

## Page 232

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 232 
MT518 Comparison Request Cancel (due to Match) sent to Dealer A  
Field/Tag Field Description 
:70E::TPRO//GSCC/TDSVTFTD/MSGRMACH Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
4.1.18 (18) MT518 Comparison Request Cancel (due to Match) 
MT518 Comparison Request Cancel (due to Match) sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 

---

## Page 233

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 233 
MT518 Comparison Request Cancel (due to Match) sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
:90A::DEAL//PRCT/99,994140625 Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:20C::PROC//7096000001 [[Seller]] (Contra) Transaction Reference 
:70E::DECL//GSCC/CTRD2049000001 [[participant]] Declaration Details Narrative  
(Contra) Trade Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRMACH Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to Match  
:16S:CONFDET Block End 
- End of Message 
4.1.19 ( 19) MT518 Repricing 
MT518 Repricing Record sent to [[Broker]] B (versus A)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 

---

## Page 234

MBSD RTTM® [[Novation]]: SWI FT Interactive Messaging Examples 
Version C ontrol Page 234 
MT518 Repricing Record sent to [[Broker]] B (versus A)  
Field/Tag Field Description 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD4253541,67  [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/YTPR Repricing Record Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  

---

## Page 235

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 235 
MT518 Repricing Record sent to [[Broker]] B (versus A)  
Field/Tag Field Description 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to System Action  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD249,02 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
4.1.20 (20) MT518 Repricing 
MT518 Repricing Record sent to [[Broker]] B (versus C)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 

---

## Page 236

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 236 
MT518 Repricing Record sent to [[Broker]] B (versus C)  
Field/Tag Field Description 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD4253541,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/YTPR Repricing Record Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to System Action  

---

## Page 237

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 237 
MT518 Repricing Record sent to [[Broker]] B (versus C)  
Field/Tag Field Description 
:16S:CONFDET Block End 
- End of Message 
4.1.21 (21) MT518 Repricing 
MT518 Repricing Record sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD4253541,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type – Sell 
:22F::PROC/GSCC/YTPR Repricing Record Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  

---

## Page 238

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 238 
MT518 Repricing Record sent to Dealer A  
Field/Tag Field Description 
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to System Action  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD249,02 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 239

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 239 
4.2 Set 2 
In this set, the following messages are included (shaded in gray). 
[[Broker]] B [[Broker]] B
(11)
MT518 Comparison Request
Dealer C
(12)
MT518 Comparison Request
[[Broker]] B
(03)
MT509 Trade Create Unbalanced
(02)
MT509 Trade Create Accepted
RTTM
(06)
MT509 Trade Create Accepted
(07)
MT509  Trade Create Unbalanced
(08)
MT518 [[default]] Values Applied
(01) 
MT515 Instruct (vs. A)
(05) 
MT515 Instruct (vs. C)
Dealer A
[[Broker]] B
(04)
MT518 [[default]] Values Applied
(09)
MT509 Trade Create Balanced
(10)
MT509 Trade Create Balanced
 
Scenario Message Sequence 
[[Broker]] B submits both sides of the trade but with incorrect final money. RTTM defaults to 
the correct final money.  
DFLT VAL (01) - (12) 
4.2.1 (DFLT VAL 01) MT515 Instruct 
MT515 [[Broker]] B Submits Buy (Long Side) to RTTM vs. A  
Field/Tag Field Description 
<password>  Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  

---

## Page 240

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 240 
MT515 [[Broker]] B Submits Buy (Long Side) to RTTM vs. A  
Field/Tag Field Description 
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0221 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20110306103913 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5000000, [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing 
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 

---

## Page 241

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 241 
MT515 [[Broker]] B Submits Buy (Long Side) to RTTM vs. A  
Field/Tag Field Description 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason – Due to System Action  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD292,97 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
4.2.2 (DFLT VAL 02) MT509 Trade Create Accepted 
MT509 Trade Create Accepted sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0221 Related Reference Number (sender’s reference)  
:16S:LINK Repeat Block End 

---

## Page 242

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 242 
MT509 Trade Create Accepted sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.2.3 (DFLT VAL 03) MT509 Trade Unbalanced 
MT509 Transaction Unbalanced sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 

---

## Page 243

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 243 
MT509 Transaction Unbalanced sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TUNB Trade Create Unbalanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.2.4 (DFLT VAL 04) MT518 [[default]] Values Applied 
MT518 [[default]] Values Applied Record Sent to [[Broker]] B (Long Side) 
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST// XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 

---

## Page 244

MBSD RTTM® [[Novation]]: S WIFT Interactive Messaging Examples 
Version C ontrol Page 244 
MT518 [[default]] Values Applied Record Sent to [[Broker]] B (Long Side) 
Field/Tag Field Description 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/DFVA [[default]] Values Applied Processing 
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:20C::PROC//000001-1306 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type – trade for trade 
Message Reason due to RTTM Action  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD249,02 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 

---

## Page 245

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 245 
MT518 [[default]] Values Applied Record Sent to [[Broker]] B (Long Side) 
Field/Tag Field Description 
- End of Message 
4.2.5 (DFLT VAL 05) MT515 Instruct 
MT515 [[Broker]] B Submits Sell (Short Side) to RTTM vs. C  
Field/Tag Field Description 
<password>  Password  
BKRB Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SENREFBKRB0222 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//20110306103913 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5000000, [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Buy 
:22F::PROC/GSCC/INST Instruct (i.e. Trade Create) Processing 
Indicator 
:22H::PAYM//APMT Against Payment Indicator  

---

## Page 246

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 246 
MT515 [[Broker]] B Submits Sell (Short Side) to RTTM vs. C  
Field/Tag Field Description 
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 
4.2.6 (DFLT VAL 06) MT509 Trade Create Accepted 
MT509 Trade Create Accepted sent to [[Broker]] B (Short Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  

---

## Page 247

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 247 
MT509 Trade Create Accepted sent to [[Broker]] B (Short Side)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SENREFBKRB0222 Related Reference Number (sender’s  reference)  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000002-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//PACK Trade Create is Acknowledged/Validated  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.2.7 (DFLT VAL 07) MT509 Trade Unbalanced 
MT509 Transaction Unbalanced sent to [[Broker]] B (Short Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST// XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 

---

## Page 248

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 248 
MT509 Transaction Unbalanced sent to [[Broker]] B (Short Side)  
Field/Tag Field Description 
:20C::LIST//000002-1306 RTTM Assigned Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TUNB Trade Create Unbalanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
4.2.8 (DFLT VAL 08) MT518 [[default]] Values Applied 
MT518 [[default]] Values Applied Record Sent to [[Broker]] B (Short Side) 
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST// XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000002-1306 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 

---

## Page 249

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 249 
MT518 [[default]] Values Applied Record Sent to [[Broker]] B (Short Side) 
Field/Tag Field Description 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Buy 
:22F::PROC/GSCC/DFVA [[default]] Values Applied Processing 
Indicator 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//000002-1306 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Original Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason due to RTTM Action  
:16S:CONFDET Block End 
- End of Message 

---

## Page 250

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 250 
4.2.9 (DFLT VAL 09) MT509 Trade Balanced 
MT509 Transaction Balanced sent to [[Broker]] B (Long Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//000001-1306 Previous Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TBAL Trade Create Balanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 251

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 251 
4.2.10 (DFLT VAL 10) MT509 Trade Balanced 
MT509 Transaction Balanced sent to [[Broker]] B (Short Side)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::PREV//000002-1306 Previous Submission Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/TBAL Trade Create Balanced  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 

---

## Page 252

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 252 
4.2.11 (DFLT VAL 11) MT518 Comparison Request 
MT518 Comparison Request for Matching Sell sent to Dealer A 
Field/Tag Field Description  
<password>  Password  (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver 
:16R:GENL Mandatory Block Start 
:20C::SEME//<nextsequence>  Sender's RTTM Reference for this Message 
:23G:NEWM Message Func tion = New 
:98C::PREP//<prepdatetime>  Preparation  Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indic ator 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percent age 
:19A::SETT//USD5004116,67 [[settlement]] Amount  – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/CMPR Comparison Request 
:22H::PAYM//APMT Against  Payment Indica tor 
:22F::CATB//PERU Per Unit Charges Indi cator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:20C::PROC//7096000002 [[Buyer]] (Contra) Transacti on Reference 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]] 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quanti ty as Face Amount (Par) 
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 

---

## Page 253

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 253 
MT518 Comparison Request for Matching Sell sent to Dealer A 
Field/Tag Field Description  
:13B::POOL/GSCC/AW9961 Pool  Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processin g Narrative 
Trade Service Type  - Trade for Trade 
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO Indic ator = Reporting Purpo ses 
:16R:AMT Optional Block Start 
:19A::LOCO//USD292,97 Commissi on Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
4.2.12 (DFLT VAL 12) MT518 Comparison Request 
MT518 Comparison Request for Matching Buy sent to Dealer C  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 

---

## Page 254

MBSD RTTM® [[Novation]]:  SWIFT Interactive Messaging Examples 
Version C ontrol Page 254 
MT518 Comparison Request for Matching Buy sent to Dealer C  
Field/Tag Field Description 
:19A::SETT//USD5004116,67 [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CMPR Comparison Request  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
:16S:CONFDET Block End 
- End of Message 

---

## Page 255

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 255 
4.3 Set 3 
In this set, the following messages are included (shaded in gray). 
Dealer A [[Broker]] B
(21)
MT518 Repricing
(19)
MT518 Repricing vs. A
RTTM
(continued from B/D SPT 
PMAT flow in Set 1)
Repricing
(22)
MT509 Instruct Deleted (due to 
Fully Paid-Down Security) vs. A
(23)
MT509 Instruct Deleted (due to 
Fully Paid-Down Security) vs. C
(24)
MT509 Instruct Deleted (due to 
Fully Paid
-Down Security) [[EOD]] 
Processing
(20)
MT518 Repricing vs. C
Dealer C
(25)
MT518 Comparison Request 
Cancel (due to System Action)
 
Scenario Message Sequence 
PMAT Marked for Deletion (due to fully paid -down security)  (01) - (18) 
TRD DEL (19) - (25) 
4.3.1 (TRD DEL 19) MT518 Repricing 
MT518 Repricing Record (Zero Factor) sent to [[Broker]] B (vs. A)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = Cancel  
:98C::PREP//<prepdatetime> Preparation Date/Time 

---

## Page 256

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 256 
MT518 Repricing Record (Zero Factor) sent to [[Broker]] B (vs. A)  
Field/Tag Field Description 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021B Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Transaction Reference 
:16S: LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD0, [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/YTPR Repricing Record Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 

---

## Page 257

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 257 
MT518 Repricing Record (Zero Factor) sent to [[Broker]] B (vs. A)  
Field/Tag Field Description 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD//MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to System Action  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Block Start 
:19A::LOCO//USD0, Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
4.3.2 (TRD DEL 20) MT518 Repricing 
MT518 Repricing Record (Zero Factor) sent to [[Broker]] B (vs. C)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = Cancel  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 

---

## Page 258

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 258 
MT518 Repricing Record (Zero Factor) sent to [[Broker]] B (vs. C)  
Field/Tag Field Description 
:16S: LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095810 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD0, [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type - Sell 
:22F::PROC/GSCC/YTPR Repricing Record Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD/MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to System Action  
:16S:CONFDET Block End 
- End of Message 

---

## Page 259

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 259 
4.3.3 (TRD DEL 21) MT518 Repricing 
MT518 Repricing Record (Zero Factor) sent to Dealer A  
Field/Tag Field Description 
 <password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKRB021S Master Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//000001-1306 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD0, [[settlement]] Amount – Final Money  
:22H::BUSE//SELL Trade Type – Sell 
:22F::PROC/GSCC/YTPR Repricing Record Processing Indicator  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  

---

## Page 260

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 260 
MT518 Repricing Record (Zero Factor) sent to Dealer A  
Field/Tag Field Description 
:95R::BUYR/GSCC/PARTBKRB Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTDLRA Party = [[Seller]]  
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 TBA [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD//MSGRGSAC Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to System Action  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  
:19A::LOCO//USD0, Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
4.3.4 (TRD DEL 22) MT509 Trade Instruct Marked for Deletion 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security) sent to [[Broker]] B (vs. A)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 

---

## Page 261

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 261 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security) sent to [[Broker]] B (vs. A)  
Field/Tag Field Description 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this 
Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKBR021B Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Transaction 
Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/DEPS Pool Instruct Marked for Deletion 
due to Fully Paid-Down Security 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
Note: 
This message will be sent end -of-day of Contractual [[settlement]] Date (“CSD”) and is not a real -time message. 
4.3.5 (TRD DEL 23) MT509 Trade Instruct Marked for Deletion 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security ) sent to [[Broker]] B (vs. C)  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
BKRB Receiver  
:16R:GENL Block Start 

---

## Page 262

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 262 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security ) sent to [[Broker]] B (vs. C)  
Field/Tag Field Description 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFBKBR021S Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//7096000002 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::BASK//BREF021 [[Broker]] Reference Number  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/DEPS Pool Instruct Marked for Deletion due to Fully 
Paid-Down Security 
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
Note: 
This message will be sent end -of-day of Contractual [[settlement]] Date (“CSD”) and is not a real-time message. 
4.3.6 (TRD DEL 24) MT509 Trade Instruct Marked for Deletion 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security) sent to Dealer A  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 

---

## Page 263

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 263 
MT509 Trade Instruct Marked for Deletion (due to Fully Paid -Down Security) sent to Dealer A  
:23G:INST Message Function - Instruct 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//XREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//2049000001 RTTM Assigned Transaction Reference 
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC/GSCC/DEPS Pool Instruct Marked for Deletion due to Fully 
Paid-Paid-Down Security  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
Note: 
This message will be sent end -of-day of Contractual [[settlement]] Date (“CSD”) and is not a real-time message. 
4.3.7 (TRD DEL 25) MT518 Comparison Request Cancel (due to System 
Action) 
MT518 Comparison Request Cancel (due to System Action) sent to Dealer C  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRC Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender's RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 

---

## Page 264

MBSD RTTM® Novatio n: SWIFT Interactive Messaging Examples 
Version C ontrol Page 264 
MT518 Comparison Request Cancel (due to System Action) sent to Dealer C  
Field/Tag Field Description 
:20C::PREV//NONREF Previous Reference Number  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//20110306095714 Trade Date & Time 
:98A::SETT//20110307 [[settlement]] Date 
:90A::DEAL//PRCT/100, Deal Price – Percentage 
:19A::SETT//USD0, [[settlement]] Amount – Final Money  
:22H::BUSE//BUYI Trade Type - Buy 
:22F::PROC/GSCC/CADV Comparison Request Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:22F::CATB//PERU Per Unit  Charges Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/PARTDLRC Party = [[Buyer]] 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/PARTBKRB Party = [[Seller]]  
:20C::PROC//7096000002 [[Seller]] (Contra) Transaction Reference 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F050650 Security Identifier – [[CUSIP]] 
:16R:FIA Block Start 
:13B::POOL/GSCC/AW9961 Pool Number 
:16S:FIA Block End 
:70E::TPRO//GSCC/TDSVTFTD /MSGRGSAC  Trade Instruction Processing Narrative 
Trade Service Type - Trade for Trade 
Message Reason - Due to System Action  
:16S:CONFDET Block End 
:16R:SETDET Optional Block Start  
:22F::SETR//RPTO Indicator = Reporting Purposes  
:16R:AMT Optional Block Start  

---

## Page 265

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 265 
MT518 Comparison Request Cancel (due to System Action) sent to Dealer C  
Field/Tag Field Description 
:19A::LOCO//USD0,00 Commission Amount  
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 

---

## Page 266

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 266 
5. [[DO]] NOT ALLOCATE (DNA) MESSAGE SAMPLES 
In this section, message flows and examples related to DNA are provided.  
The DNA facts and reference numbers used, as well as those assigned by RTTM, are summarized in the grid 
below: 
Reference Numbers  Dealer A  
Sender’s Reference  SREFA20150618nnn 
where nnn is a sequence number starting from 001 and incrementing by 1 for 
each message sent (e.g. 001, 002, 003 etc).  
DNA XREF  DXREFDLRA001  
RTTM DNA [[ID]] 1803710498 
 
The following DNA scenarios below have been constructed. Each of these scenarios is illustrated by a series of 
message samples, which represent a “flow” of events. The grid below describes each of these scenarios and 
indicates which sequence of message samples corresponds to a given scenario: 
# Scenario Message Sequence 
1 Dealer A submits a DNA Create request, specifying terms only.  (01) – (03) 
2 Dealer A submits a DNA Cancel, targeting a previously created DNA.  (01) - (03) 
and  
DNACAN (04) –(05) 
3 Dealer A submits a DNA Create request, specifying specific Trade [[ID]]’s to target.  TRDID (01) – (03) 
4 Dealer submits a DNA Create via WFE, then subsequently cancels it via WFE.  SCR (01) – (02) 
5 Dealer A submits a DNA Create request that is rejected due to insufficient position.  They 
then attempt to cancel the DNA, but RTTM rejects the request as the DNA is not found.  
DNAREJ (01) – (02) 

---

## Page 267

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 267 
5.1 Set 1 
This set covers actions of DNA Create (via terms). 
Dealer A
(01)
MT515 DNA Request
(via terms)
(02)
MT509 DNA Accepted
(03)
MT518 DNA Assigned
RTTM
 
In the flow above, the following occurs:  
1. Dealer A (account “DLRA”) submits a “terms-only” DNA, proving 1 buy and 2 sell terms (step 01-02): 
a. TBA [[CUSIP]] = 01F040693 and CSD = 9/17/2015 
b. Buy terms of Price = 101.5, Trade Date = September 15, 2015, Par = 5,000,000  
c. Sell terms of Price = 100.78125, Trade Date = September 16, 2015, Par = 3,000,000  
d. Sell terms of Price = 102, Trade Date = September 16, 2015, Par = 2,000,000  
2. RTTM assigns this DNA to various trades (step 03). 
Note: 
As this DNA is via terms, specific Trade [[ID]] information is not provided. 1 
sScenario Message Sequence 
Dealer A submits a DNA Create request, specifying terms only.  (01) – (03) 
5.1.1 (01) MT515 DNA 
Dealer A submits a DNA to RTTM, with 1 buy and 2 sell terms specified  
Field/Tag Field Description 
<password>  Password (not shown)  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SREFA20150618001 Sender’s Reference for this Message 
 
1 The DNA Status MRO will provide information about each trade that the DNA is assigned to, including Trade [[ID]] and par amount. 

---

## Page 268

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 268 
Dealer A submits a DNA to RTTM, with 1 buy and 2 sell terms specified  
Field/Tag Field Description 
:23G:NEWM Message Function = New  
:98C::PREP//20150618094956 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//DXREFDLRA001 Master Reference Number = DNA Reference 
assigned by [[participant]]  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//99991231000000 Trade Date & Time = Dec 31st, 9999 ([[default]])  
:98A::SETT//20150917 [[settlement]] Date 
:90A::DEAL//PRCT/0, Deal Price = 0 ([[default]])  
:22H::BUSE//BUYI Business Use Indicator = Buy ([[default]])  
:22F::PROC/GSCC/DNAL Processing Indicator = DNA Create 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/DLRA [[Buyer]] = DLRA 
:70E::DECL//GSCC/FAMT5000000,/PRCT101,5/TDDT20150915 [[participant]] Financial Amount Declaration  
DNA Par = 5,000,000 
DNA Price = 101.5 
DNA Trade Date = September 15, 2015 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
95R::SELL/GSCC/DLRA [[Seller]] = DLRA 
:70E::DECL//GSCC/FAMT3000000,/PRCT100,78125/ 
TDDT20160916 
[[participant]] Financial Amount Declaration  
DNA Par = 3,000,000 
DNA Price = 100.78125 
DNA Trade Date = September 16, 2015 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
95R::SELL/GSCC/DLRA [[Seller]] = DLRA 

---

## Page 269

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 269 
Dealer A submits a DNA to RTTM, with 1 buy and 2 sell terms specified  
Field/Tag Field Description 
:70E::DECL//GSCC/FAMT2000000,/PRCT102,/TDDT20160916 [[participant]] Financial Amount Declaration  
DNA Par = 2,000,000 
DNA Price = 102 
DNA Trade Date = September 16, 2015 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F040693 Identification of Security (TBA [[CUSIP]])  
:16S:CONFDET Block End 
- End of Message 
5.1.2 (02) MT509 DNA Accepted 
RTTM sends an acknowledgement of the DNA to Dealer A, indicating that the DNA was processed successfully 
by RTTM.  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender’s RTTM Reference for this Message 
:23G:INST Message Function = Instruct  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//DXREFDLRA001 Master Reference Number = XREF of DNA  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SREFA20150618001 Related Reference = SEME of MT515 being 
acknowledged  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:20C::LIST//1803710498 RTTM Reference = DNA [[ID]] assigned by RTTM  
:16S:LINK Repeat Block End 

---

## Page 270

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 270 
RTTM sends an acknowledgement of the DNA to Dealer A, indicating that the DNA was processed successfully 
by RTTM.  
Field/Tag Field Description 
:16R:STAT Repeat Block Start 
:25D::IPRC//GSCC/DNAL Status Code = DNA Accepted by RTTM  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
5.1.3 (03) MT518 DNA Assigned 
RTTM sends a DNA assigned message to Dealer A, indicating the DNA was assigned to specific trades by RTTM.  
Field/Tag Field Description 
<Password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender’s RTTM Reference for this message 
:23G:NEWM Message Function = New  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//DXREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//1803710498 RTTM Reference = DNA [[ID]] assigned by RTTM  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//99991231000000 Trade Date & Time = Dec 31st, 9999 ([[default]])  
:98A::SETT//20150917 [[settlement]] Date 
:90A::DEAL//PRCT/0, Deal Price = 0 ([[default]])  

---

## Page 271

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 271 
RTTM sends a DNA assigned message to Dealer A, indicating the DNA was assigned to specific trades by RTTM.  
Field/Tag Field Description 
:22H::BUSE//BUYI Business Use Indicator = Buy ([[default]])  
:22F::PROC/GSCC/DNAP Processing Indicator = DNA Assigned  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/DLRA [[Buyer]] = DLRA 
:70E::DECL//GSCC/FAMT5000000,/PRCT101,5/TDDT20150915 [[participant]] Financial Amount Declaration  
DNA Par = 5,000,000 
DNA Price = 101.5 
DNA Trade Date = September 15, 2015 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/DLRA [[Seller]] = DLRA 
:70E::DECL//GSCC/FAMT3000000,/PRCT100,78125/ 
TDDT20150916 
[[participant]] Financial Amount Declaration  
DNA Par = 3,000,000 
DNA Price = 100.78125 
DNA Trade Date = September 16, 2015 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/DLRA Party = [[Seller]]  
:70E::DECL//GSCC/FAMT2000000,/PRCT102,/TDDT20150916 [[participant]] Financial Amount Declaration  
DNA Par = 2,000,000 
DNA Price = 102 
DNA Trade Date = September 16, 2015 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000,  Quantity as Face Amount (Par)  
:35B:/US/01F070633 Identification of Security (TBA [[CUSIP]])  
:16S:CONFDET Block End 
- End of Message 

---

## Page 272

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 272 
5.2 Set 2 
This set covers actions of DNA cancel. 
Dealer A
(01)
MT515 DNA Request
(via terms)
(02)
MT509 DNA Accepted
(03)
MT518 DNA Assigned
DNACAN (04)
MT515 DNA Cancel
RTTM
DNACAN (05)
MT509 DNA Cancel Accepted & Processed
 
Scenario Message Sequence 
Dealer A submits a DNA Cancel, targeting a previously created DNA.  (01) - (03) 
and  
DNACAN (04) –(05) 
5.2.1 (DNACAN 04) MT515 DNA Cancel 
Dealer A submits a DNA Cancel to RTTM, targeting the DNA previously created (message 02).  
Field/Tag Field Description 
<password>  Password (not shown)  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SREFA20150618002 Sender’s Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//20150618103000 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//DXREFDLRA001 Master Reference Number = DNA Reference 
assigned by [[participant]]  

---

## Page 273

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 273 
Dealer A submits a DNA Cancel to RTTM, targeting the DNA previously created (message 02).  
Field/Tag Field Description 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//1803710498 RTTM Reference = DNA [[ID]] assigned by RTTM  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//99991231000000 Trade Date & Time = Dec 31st, 9999 ([[default]])  
:98A::SETT//20150917 [[settlement]] Date 
:90A::DEAL//PRCT/0, Deal Price = 0 ([[default]])  
:22H::BUSE//BUYI Business Use Indicator = Buy ([[default]])  
:22F::PROC/GSCC/CDNA Processing Indicator = DNA Cancel  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/DLRA [[Buyer]] = DLRA 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F040693 Identification of Security (TBA [[CUSIP]])  
:16S:CONFDET Block End 
- End of Message 
5.2.2 (DNACAN 05) MT509 DNA Cancel Accepted 
RTTM sends an acknowledgement of the DNA Cancel to Dealer A, indicating that the cancel was processed 
successfully by RTTM.  
Field/Tag Field Description 
<password>  Password (blank)  
MBSCTRRS Sender  
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender’s RTTM Reference for this Message 

---

## Page 274

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples 
Version C ontrol Page 274 
RTTM sends an acknowledgement of the DNA Cancel to Dealer A, indicating that the cancel was processed 
successfully by RTTM.  
Field/Tag Field Description 
:23G:INST Message Function = Instruct  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//DXREFDLRA001 Master Reference Number = XREF of DNA  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SREFA20150618002 Related Reference = SEME of MT515 being 
acknowledged  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:20C::LIST//1803710498 RTTM Reference = DNA [[ID]] assigned by RTTM  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::CPRC//GSCC/CDNA Status Code = DNA Cancel Accepted & 
Processed by RTTM  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
 
  

---

## Page 275

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 275 
5.3 Set 3 
This set covers actions of DNA Create (via Trade [[ID]]). 
Dealer A
(TRDID 01)
MT515 DNA Request
(via trade [[ID]])
(TRDID 02)
MT509 DNA Accepted
(TRDID 03)
MT518 DNA Assigned
RTTM
 
In the flow above, the following occurs:  
1. Dealer A (account “DLRA”) submits a DNA specifying specific trades to target, as follows (step TRDID 01-
02): 
a. TBA [[CUSIP]] = 01F040693 and CSD = 9/17/2015 
b. 5MM to buy Trade [[ID]] = 2049000111, Price = 101.5, Trade Date = September 15, 2015 
c. 3MM to sell Trade [[ID]] = 2049000222, Price = 100.78125, Trade Date = September 16, 2015 
d. 1MM to sell Trade [[ID]] = 2049000333, Price = 102, Trade Date = September 16, 2015 
e. 1MM to sell Trade [[ID]] = 2049000444, Price = 102, Trade Date = September 16, 2015 
2. RTTM assigns this DNA to the trades indicated (step TRDID 03) 
 
Scenario Message Sequence 
Dealer A submits a DNA Create request, specifying specific Trade [[ID]]’s to target.  TRDID (01) – (03) 
5.3.1 (TRDID 01) MT515 DNA 
Dealer A submits a DNA to RTTM, with specific Trade [[ID]]’s provided  
Field/Tag Field Description 
<password>  Password (not shown)  
DLRA Sender  
515/000/GSCC Message Type 
MBSCTRRS Receiver  
:16R:GENL Block Start 
:20C::SEME//SREFA20150618001 Sender’s Reference for this Message 
:23G:NEWM Message Function = New  

---

## Page 276

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 276 
Dealer A submits a DNA to RTTM, with specific Trade [[ID]]’s provided  
Field/Tag Field Description 
:98C::PREP//20150618094956 Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//DXREFDLRA001 Master Reference Number = DNA Reference 
assigned by [[participant]]  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Block Start 
:98C::TRAD//99991231000000 Trade Date & Time = Dec 31st, 9999 ([[default]])  
:98A::SETT//20150917 [[settlement]] Date 
:90A::DEAL//PRCT/0, Deal Price = 0 ([[default]])  
:22H::BUSE//BUYI Business Use Indicator = Buy ([[default]])  
:22F::PROC/GSCC/DNAL Processing Indicator = DNA Create 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Repeat Block Start 
:95R::BUYR/GSCC/DLRA [[Buyer]] = DLRA 
:70E::DECL//GSCC/FAMT5000000,/PRCT101,5/TDDT20150915/  
TRID2049000111 
[[participant]] Financial Amount Declaration  
DNA Par = 5,000,000 
DNA Price = 101.5 
DNA Trade Date = September 15, 2015 
Trade [[ID]] = 2049000111 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
95R::SELL/GSCC/DLRA [[Seller]] = DLRA 
:70E::DECL//GSCC/FAMT3000000,/PRCT100,78125/ 
TDDT20150916/TRID2049000222 
[[participant]] Financial Amount Declaration  
DNA Par = 3,000,000 
DNA Price = 100.78125 
DNA Trade Date = September 16, 2015 
Trade [[ID]] = 2049000222 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
95R::SELL/GSCC/DLRA [[Seller]] = DLRA 
:70E::DECL//GSCC/FAMT1000000,/PRCT102,/TDDT20150916/  
TRID2049000333 
[[participant]] Financial Amount Declaration  
DNA Par = 1,000,000 
DNA Price = 102 

---

## Page 277

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 277 
Dealer A submits a DNA to RTTM, with specific Trade [[ID]]’s provided  
Field/Tag Field Description 
DNA Trade Date = September 16, 2015  
Trade [[ID]] = 2049000333 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Repeat Block Start 
95R::SELL/GSCC/DLRA [[Seller]] = DLRA 
:70E::DECL//GSCC/FAMT1000000,/PRCT102,/TDDT20150916/  
TRID2049000444 
[[participant]] Financial Amount Declaration  
DNA Par = 1,000,000 
DNA Price = 102 
DNA Trade Date = September 16, 2015 
Trade [[ID]] = 2049000444 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F040693 Identification of Security (TBA [[CUSIP]])  
:16S:CONFDET Block End 
- End of Message 
5.3.2 (TRDID 02) MT509 DNA Accepted 
RTTM sends an acknowledgement of the DNA to Dealer A, indicating that the DNA was processed successfully by 
RTTM. 
Field/Tag Field Description 
 
This message is the same as DNA (02). 
5.3.3 (TRDID 03) MT518 DNA Assigned 
RTTM sends a DNA assigned message to Dealer A, indicating the DNA was assigned to specific trades by RTTM.  
Field/Tag Field Description 
<Password>  Password (blank)  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender’s RTTM Reference for this message 
:23G:NEWM Message Function = New  

---

## Page 278

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 278 
RTTM sends a DNA assigned message to Dealer A, indicating the DNA was assigned to specific trades by RTTM.  
Field/Tag Field Description 
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//DXREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//1803710498 RTTM Reference = DNA [[ID]] assigned by RTTM  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//99991231000000 Trade Date & Time = Dec 31st, 9999 ([[default]])  
:98A::SETT//20150917 [[settlement]] Date 
:90A::DEAL//PRCT/0, Deal Price = 0 ([[default]])  
:22H::BUSE//BUYI Business Use Indicator = Buy ([[default]])  
:22F::PROC/GSCC/DNAP Processing Indicator = DNA Assigned  
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/DLRA [[Buyer]] = DLRA 
:70E::DECL//GSCC/FAMT5000000,/PRCT101,5/TDDT20150915/
TRID2049000111 
[[participant]] Financial Amount Declaration  
DNA Par = 5,000,000 
DNA Price = 101.5 
DNA Trade Date = September 15, 2015 
Trade [[ID]] = 2049000111 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/DLRA [[Seller]] = DLRA 
:70E::DECL//GSCC/FAMT3000000,/PRCT100,78125/ 
TDDT20150916/TRID2049000222 
[[participant]] Financial Amount Declaration  
DNA Par = 3,000,000 
DNA Price = 100.78125 
DNA Trade Date = September 16, 2015 
Trade [[ID]] = 2049000222 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/DLRA Party = [[Seller]]  

---

## Page 279

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 279 
RTTM sends a DNA assigned message to Dealer A, indicating the DNA was assigned to specific trades by RTTM.  
Field/Tag Field Description 
:70E::DECL//GSCC/FAMT1000000,/PRCT102,/TDDT20150916/  
TRID2049000333 
[[participant]] Financial Amount Declaration  
DNA Par = 1,000,000 
DNA Price = 102 
DNA Trade Date = September 16, 2015 
Trade [[ID]] = 2049000333 
:16S:CONFPRTY Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::SELL/GSCC/DLRA Party = [[Seller]]  
:70E::DECL//GSCC/FAMT1000000,/PRCT102,/TDDT20150916/T
RID2049000444 
[[participant]] Financial Amount Declaration  
DNA Par = 1,000,000 
DNA Price = 102 
DNA Trade Date = September 16, 2015 
Trade [[ID]] = 2049000444 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Identification of Security (TBA [[CUSIP]])  
:16S:CONFDET Block End 
- End of Message 
 
  

---

## Page 280

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version Control Page 280 
5.4 Set 4 
This set covers DNA actions entered from the WFE, including DNA create and DNA cancel.  
Dealer A
WFE action #1: DNA Create
RTTM
(SCR 02)
MT518 Screen Input Replay (DNA Cancel)
(SCR 01)
MT518 Screen Input Replay (DNA)
WFE action #2: DNA Cancel
 
In the flow above, the following occurs:  
1. Dealer A (account “DLRA”) creates a DNA via WFE specifying specific trades to target, as follows (step 
1): 
a. TBA [[CUSIP]] = 01F040693 and CSD = 9/17/2015 
b. 5MM to buy Trade [[ID]] = 2049000111 Price = 101.5, Trade Date = September 15, 2015 
c. 3MM to sell Trade [[ID]] = 2049000222 = Price = 100.78125, Trade Date = September 16, 2015 
d. 1MM to sell Trade [[ID]] = 2049000333 Sell terms of Price = 102, Trade Date = September 16, 2015 
e. 1MM to sell Trade [[ID]] = 2049000444 Sell terms of Price = 102, Trade Date = September 16, 2015 
2. Dealer A cancels this DNA via WFE (step 2) 
Note: 
The DNA specified in this example is the same as in the prior set.  
Scenario Message Sequence 
Dealer submits a DNA create via WFE, then subsequently cancels it via WFE.  SCR (01) – (02) 
5.4.1 (SCR 01) MT518 Screen Input Replay (DNA) 
RTTM sends a DNA Screen Input Replay message to Dealer A, providing details on the DNA created via WFE, 
including Trade [[ID]] assignments.  
Field/Tag Field Description 
 
This message is the same as Set 3 (TRDID 03), with the following changes: 
• The Processing Indicator reflects Screen Input Replay for DNA => :22F::PROC/GSCC/SDNA 

---

## Page 281

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 281 
5.4.2 (SCR 02) MT518 Screen Input Replay (DNA Cancel) 
RTTM sends a DNA Screen Input Replay message for DNA Cancel to Dealer A, providing details on DNA 
targeted for cancel.  
Field/Tag Field Description 
<password>  Password  
MBSCTRRS Sender  
518/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Mandatory Block Start  
:20C::SEME//<nextsequence> Sender’s RTTM Reference for this Message 
:23G:CANC Message Function = Cancel  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:22F::TRTR/GSCC/CASH Buy/Sell Trade Indicator  
:16R:LINK Repeat Block Start 
:20C::MAST//DXREFDLRA001 Master Reference Number  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//1803710498 RTTM Reference = DNA [[ID]] assigned by RTTM  
:16S:LINK Repeat Block End 
:16S:GENL Block End 
:16R:CONFDET Mandatory Block Start  
:98C::TRAD//99991231000000 Trade Date & Time = Dec 31st, 9999 ([[default]])  
:98A::SETT//20150917 [[settlement]] Date 
:90A::DEAL//PRCT/0, Deal Price = 0 ([[default]])  
:22H::BUSE//BUYI Business Use Indicator = Buy ([[default]])  
:22F::PROC/GSCC/SDNA Processing Indicator = Screen Input DNA 
Replay 
:22H::PAYM//APMT Against Payment Indicator  
:16R:CONFPRTY Mandatory Repeat Block Start  
:95R::BUYR/GSCC/DLRA [[Buyer]] = DLRA 
:16S:CONFPRTY Repeat Block End 
:36B::CONF//FAMT/5000000, Quantity as Face Amount (Par)  
:35B:/US/01F070633 Identification of Security (TBA [[CUSIP]])  

---

## Page 282

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 282 
RTTM sends a DNA Screen Input Replay message for DNA Cancel to Dealer A, providing details on DNA 
targeted for cancel.  
Field/Tag Field Description 
:16S:CONFDET Block End 
- End of Message 
5.5 Set 5 
This set covers DNA reject scenarios. 
Dealer A
MT515 DNA
(DNAREJ 01)
MT509 Reject (DNA)
RTTM
MT515 DNA Cancel
(DNAREJ 02)
MT509 Reject (DNA Cancel)
 
In the flow above, the following occurs: 
1. Dealer A (account “DLRA”) submits the same DNA as indicated in Set DNA1, but RTTM rejects the 
request for insufficient position. 
2. Dealer A then attempts to cancel the DNA as indicated in Set DNA1, but RTTM rejects the request as the 
DNA was not found. 
Note: 
Please refer to Set 1 for the MT515 DNA and MT515 DNA Cancel messages.  
Scenario Message Sequence 
Dealer A submits a DNA Create request that is rejected due to insufficient position. They then 
attempt to cancel the DNA, but RTTM rejects the request as the DNA is not found.  
DNAREJ (01) – (02) 
5.5.1 (DNA REJ 01) MT509 DNA Rejected 
RTTM sends a DNA rejection to Dealer A, indicating that the DNA was rejected by RTTM.  
Field/Tag Field Description 
<password>  Password (not shown)  
MBSCTRRS Sender  

---

## Page 283

MBSD RTTM® [[Novation]]: SWIFT Interactive Messaging Examples  
Version C ontrol Page 283 
RTTM sends a DNA rejection to Dealer A, indicating that the DNA was rejected by RTTM.  
Field/Tag Field Description 
509/000/GSCC Message Type 
DLRA Receiver  
:16R:GENL Block Start 
:20C::SEME//<nextsequence> Sender’s RTTM Reference for this Message 
:23G:INST Message Function = Instruct  
:98C::PREP//<prepdatetime> Preparation Date/Time 
:16R:LINK Repeat Block Start 
:20C::MAST//DXREFDLRA001 Master Reference Number = XREF of DNA  
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::RELA//SREFA20150618001 Related Reference = SEME of MT515 being 
rejected  
:16S:LINK Repeat Block End 
:16R:STAT Repeat Block Start 
:25D::IPRC//REJT Status Code = Rejected 
:16R:REAS Optional Repeat Block End  
:24B::REJT/GSCC/E156 Reject Reason – E156 No available TBA position 
for DNA 
:70D::REAS//GSCC/DNRJ Reject Reason Narrative = DNA request rejected  
:16S:REAS Optional Repeat Block End  
:16S:STAT Repeat Block End 
:16S:GENL Block End 
- End of Message 
5.5.2 (DNA REJ 02) MT509 DNA Cancel Rejected 
RTTM sends a DNA rejection to Dealer A, indicating that the DNA was rejected by RTTM.  
Field/Tag Field Description 
 
This message is the same as DNAREJ (01) with the following changes: 
• The Message Function reflects Cancel => :23G:CAST 
• The Status Code reflects rejection of a cancel => :25D::CPRC//REJT 

---

## Page 284

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 