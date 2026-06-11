---
title: "S:\CCFWEB\CCFREPLA\02MEMSEG.PDF"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/02MEMSEG.PDF"
pages: 30
size: "132.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# S:\CCFWEB\CCFREPLA\02MEMSEG.PDF

**Original File:** [02MEMSEG.PDF](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/02MEMSEG.PDF)  
**Category:** Other  
**Total Pages:** 30  
**File Size:** 132.6 KB  

---

## Page 1

[[CCF]]/[[CCF]]-II/MDH Transmission Guides
4.02 Memo Segregation via [[CCF]]-II (MEMSEG):
Function User's Guide
The Depository Trust & Clearing Corporation May 2001

---

## Page 2

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
Copyright © 2001 by The Depository Trust & Clearing Corporation (“[[DTCC]]”). Al l
rights reserved. This work is proprietary and is intended for exclusive use by [[DTCC]]’s
Participants and other users of [[DTCC]]’s services. No part of this work may b e
reproduced  or distributed (including by transmission) in any form or by any means ,
or store d in any information storage and retrieval system, without [[DTCC]]’s prio r
written permission.
All requests for additional copies of this work or inquiries about this work should be
directed to [[DTCC]] [[participant]] Interface Planning.

---

## Page 3

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
4.02 MEMSEG: Function User's Guide
Table of Contents
Section Page
1.0 The [[CCF]]-II Memo Segregation System ................................. 1
1.1 [[CCF]]-II MEMSEG Function Availability and Cutoff Times ................ 2
2.0 [[CCF]]-II Summary ................................................... 3
2.1 Transmitting Transactions to [[DTC]] ................................... 4
2.2 Initiating a MEMSEG Transmission ................................. 5
2.3 Testing the MEMSEG Function ..................................... 5
2.4 Recovery Procedures ............................................. 5
2.5 Backup for [[CCF]]-II ............................................... 6
3.0 The MEMSEG Transmission File (Input) ............................... 7
3.1 MEMSEG Transmission Records ................................... 7
3.2 MEMSEG Transmission Editing .................................... 8
3.3 MEMSEG Transaction Editing ..................................... 9
4.0 MEMSEG Transmission Record Formats .............................. 10
4.1 The [[CCF]]-II Transmission SECURITY Record ("PSW") ................. 11
4.2 The MEMSEG Transmission HEADER Record ("HDR") ................ 12
4.3 The MEMSEG Transmission Data Record ("DAT") .................... 13
4.4 The MEMSEG Transmission TRAILER Record ("TLR") ............... 14
5.0 The MEMSEG Acknowledgement File (Output) ......................... 15
5.1 MEMSEG Acknowledgement Records .............................. 16
6.0 MEMSEG Acknowledgement Record Format ........................... 17
6.1 The [[CCF]]-II Acknowledgement Error Record ("ERR") .................. 17
6.2 The MEMSEG Acknowledgement Control Record ("CTL") .............. 19
6.3 The MEMSEG Acknowledgement Rejected Header Record ("HDR") ...... 21
6.4 The MEMSEG Acknowledgement Rejected Data Record ("DAT") ........ 23
6.5 The MEMSEG Acknowledgement Rejected Trailer Record ("TLR") ....... 25
6.6 The MEMSEG Acknowledgement Audit Record ("ADT") .............. 27

---

## Page 4

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 1 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
1.0 The [[CCF]]-II Memo Segregation System
The purpose of the [[CCF]]-II MEMO SEGREGATION system is to provide a facility which will monitor
and control activities in issues which contain fully paid customer [[securities]] on deposit at the Depository. 
Participants are requested to supply MEMSEG entries only for those CUSIPs where a delivery
requirement is anticipated that day or the following day's PDQ (night) cycle.
MEMO SEGREGATION is a service separate and distinct from the SEGREGATION facility currently
provided at [[DTC]], and is intended to further protect customer assets not fully safeguarded by the
Segregation Systems.  The SEGREGATION facility physically segregates [[securities]] in a [[participant]]'s
account from all [[DTC]] services, until instructions are received from the [[participant]] to release either all or
a portion of the segregated [[securities]].  This release instruction physically swings back the [[securities]]
indicated, thereby availing this position to [[participant]]-initiated activities.
MEMO SEGREGATION (MEMSEG) creates a "MEMSEG" position within the free account.  This
"logical" separation allows [[DTC]] Participants to protect a designated security quantity, even if it is greater
than the actual free account position in an issue.  In this way, MEMSEG protects against the unintended
delivery of fully paid [[securities]] that are in the free account, or that may be received during the daily
processing cycle.
MEMSEG instructions can be transmitted via the Computer-to-Computer Facility ([[CCF]]), [[CCF]]-II, or the
[[participant]] Terminal System, and consist of a security quantity identified as fully paid customer
[[securities]] and a [[CUSIP]] number. The size of the protected position can be changed either by an
eligible transaction, or by retransmitting the [[CUSIP]] number with an appropriate action code and
security quantity to cover or overlay or adjust the "memo" segregated security quantity.
Eligible transactions that decrement MEMSEG positions are Withdrawals-by-Transfer, Certificate-on-
Demand Withdrawals, and free Deliver Orders that are not identified as [[Stock]] loans or [[Stock]]-loan
returns.  For these transaction types, [[DTC]] checks the free account, and, if there are sufficient
[[securities]], reduces it and the MEMSEG account by the same amount.

---

## Page 5

1.0 The [[CCF]]-II Memo Segregation System (Continued)
THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 2 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
A free account "excess position" is calculated by subtracting the MEMSEG position from the free
account security balance.  The excess position is available for valued [[book-entry]] deliveries, free [[Stock]]-
loan deliveries and returns, [[syndicate]] deliveries, deliveries to the National [[securities]] Clearing
Corporation's Continuous Net [[settlement]] system, and [[collateral]] loan pledges, all of which reduce only
the free account.
If the "excess position" is insufficient for a transaction–even though the free account total position may
be sufficient–these actives will recycle, except for loan pledges, which will drop.
The [[CCF]]-II MEMO SEGREGATION function will provide immediate validity editing of the
transmission.  The [[participant]] will receive a return transmission indicating any errors found during the
editing process.
1.1 [[CCF]]-II MEMSEG Function Availability and Cutoff Times
The [[CCF]]-II MEMO SEGREGATION function will be available from 4:00 A.M. until 6:30 P.M.  This
means that [[CCF]]-II MEMSEG transmissions will be accepted if they begin between 4:00 A.M. and
6:30 P.M. daily.  Test MEMSEG transmissions will be accepted during [[PTS]] operating hours with
TEST=YES on the CCFUSER control card and  position 28= 'T' ("Processing [[Option]]") on the
MEMSEG Header Record( 'HDR'). 
If the 6:30 P.M. cutoff time is reached during a MEMSEG transmission, processing will continue until
the transmission is completed.  In no event, however, will a MEMSEG transmission be accepted if it
begins after the 6:30 P.M. cutoff.

---

## Page 6

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 3 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
2.0 [[CCF]]-II Summary
[[DTC]]'s Computer-to-Computer Facility Two ([[CCF]]-II) is a medium enabling the transmission of data back
and forth between the Depository Trust & Clearing Corporation and its participants/users.  The user
transmits data to [[DTC]] (the Transmission file), and then receives data in reply from [[DTC]] (the
Acknowledgment file).
[[CCF]]-II transmissions to and from [[DTC]] utilize either:
C IBM's Remote Job Entry (RJE) software
C IBM's Remote Job Entry/System Network Architecture (RJESNA) software.
C Systems Center Network Data Mover (NDM) software
In order for a [[CCF]]-II user to transmit data to [[DTC]], he must prepare an input file of transactions in the
[[DTC]]-specified format.  The user then executes RJE-, RJES- or NDM-based JCL in order to communicate
with [[DTC]]'s computer system.
After the transmission completes, [[DTC]] will edit the input Transmission file and return an Acknowledgement
file to the user, indicating the status of the transmission and any errors that were detected in the transmitted
transactions.
This document discusses all aspects of transmission via [[DTC]]'s Computer-to-Computer Facility Two ([[CCF]]-
II).

---

## Page 7

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 4 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
2.1 Transmitting Transactions to [[DTC]]
When a [[CCF]]-II user wishes to transmit data to [[DTC]], he must prepare JCL as specified in either the
[[CCF]]-II/RJE User's Guide, [[CCF]]-II/NDM USER'S GUIDE or [[CCF]]-II/RJESNA USER'S GUIDE
For a more complete understanding of specific JCL requirements the RJE and/or NDM User Guides
must be consulted.
After creating a file of input transactions in the appropriate RJE or NDM format, the user transmits
the [[DTC]]-specified JCL in order to initiate a job within [[DTC]]'s Computer System.  The input file
records are then edited and any records in error will be transmitted back to the user.  Valid
transactions will be processed if no "severe" errors are detected.
The user must submit the following generic procedure name and overriding parameter in the
transmitted JCL to indicate the [[CCF]]-II function being processed:
procedure name:  "RJExxxxx"  "RJESxxxx"  "NDMxxxxx"
override parameter: "FUNC=yyyyyy"
where:
RJExxxxx = [[DTC]]'s [[CCF]]-II/RJE processing procedures; "xxxxx" is the suffix referring to the
transmitted function.
RJESxxxx = [[DTC]]'s [[CCF]]-II/REJSNA processing procedure; refer to the User's Guide for the
proper suffix.  
NDMxxxxx = [[DTC]]'s [[CCF]]-II/NDM processing procedure; "xxxxx" is the suffix referring to the
transmitted function.
yyyyyy = the name of the CF2 function being transmitted.

---

## Page 8

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 5 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
2.2 Initiating a MEMSEG Transmission
The user then executes RJE- or NDM- based JCL to [[DTC]] to initiate MEMSEG transmissions.  The
[[BASIC]] format of the JCL "EXEC" statement appears in the appropriate [[CCF]]-II User's Guide.
2.3 Testing the MEMSEG Function
By placing a "T" or a "P" in the processing [[Option]] field (position 28) of the transmission header
record, the user may specify whether the transmission is for "Test" or "Production" purposes.
Production All Memo Segregation transactions in a "production" (live) MEMSEG transmission that
comply with MEMSEG edit criteria and are deemed fully valid affect the "MEMSEG"
position within a [[participant]]'s free account.
Test No Memo Segregation transactions in a MEMSEG "test" transmission affect the [[participant]]'s
free account.  These transactions are listed (at [[DTC]]) and, if invalid, are returned to the
Issuing [[participant]].  "Test" listings are available from [[DTC]] upon request.  [[DTC]] has created
the "test" [[Option]] to facilitate development of [[CCF]]-II functions on the Participants' computer
systems.
2.4 Recovery Procedures
Restart capability is available for [[CCF]]-II users.  Details of the procedures to be followed in the event
that RESTART is necessary are provided in the [[CCF]]-II SYSTEM USER'S GUIDE in the section
entitled "RECOVERY/RESTART PROCEDURES".

---

## Page 9

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 6 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
2.5 Backup for [[CCF]]-II
If, for any reason, a user is unable to use [[CCF]]-II to enter his transactions as scheduled, [[DTC]]
Network Operations should be notified immediately.
If the user is not able to enter his transactions via [[CCF]]-II because of modem or telephone line
equipment failures at his site, he has the [[Option]] of creating a magnetic tape in the format of the
specific [[CCF]]-II Transmission file involved (in this case Memo Segregation - MEMSEG) and send it to
[[DTC]] via messenger.  The tape should be created with these characteristics:
C NON-LABELLED
C 1600 / 6250 bpi
C RECFM = FB
C LRECL = 80
C BLKSIZE = Efficient Block Size
[[DTC]] will input the transactions from the tape and then return it to the user.
Participants who, in the emergency, will not be able to deliver a magnetic tape to [[DTC]] via messenger
before the appropriate cutoff time for the [[CCF]]-II function involved (see "[[CCF]]-II MEMSEG Function
Availability and Cutoff Time" on page 3), are responsible for making other arrangements for backup in
case of modem or telephone equipment failures.
Participants should realize that when using [[CCF]]-II to input transactions to [[DTC]], they are bound by
computer and data communications equipment availability at their site.  [[DTC]] cannot afford to delay its
entire processing cycle to accommodate equipment failures at any [[participant]] site.  It is strongly
suggested that all users maintain redundant [[CCF]]-II equipment (computers and communication
controllers)
IN NO EVENT will [[DTC]] accept any responsibility for a [[participant]]'s inability to submit any type of
[[CCF]]-II transmission to the Depository.

---

## Page 10

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 7 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
3.0 The MEMSEG Transmission File (Input)
The [[CCF]]-II Memo Segregation file consists of four different types of record, each of which contains 80
characters.  The first two and the last record on the Transmission file, the "Security", "Header" and "Trailer"
records, are for control purposes.  The MEMSEG "Data" record provides instructions for a MEMSEG
segregation transaction.  A description of each MEMSEG record type appears in the following section.
3.1 MEMSEG Transmission Records
1. [[CCF]]-II Transmission Security record:  specifies the SIGNON [[ID]]. of the transmitter utilizing
[[DTC]]'s MEMSEG function, his legitimate password, and the transmission's unique identifying
number.  The Security "PSW") record must be the first record in the file, but is considered a
[[CCF]]-II record rather than a MEMSEG Transmission record.  The Security ("PSW") record is for
input purposes only, and is therefore not returned in [[DTC]]'s Acknowledgement file.
2. Transmission Header record:  identifies the transmitter of the Memo Segregation transactions and
confirms that the transmission was not previously submitted.  The Header ("HDR" ) record must
be the first record in the MEMSEG Transmission file, however, it is NOT to be included in record
count tabulations.
3. Memo Segregation Transaction Data record:  contains detailed information regarding a single
MEMSEG transaction.  The MEMSEG Data record has record type "DAT".
4. Transmission Trailer record:  contains control information for all MEMSEG transactions in the
transmission.  The "TLR" record must be the LAST record of the MEMSEG transmission,
however, it is NOT to be included in record count tabulations.  Totals appearing in the MEMSEG
Trailer record will be verified by [[DTC]].  If a trailer record is transmitted as anything but the last
record, the entire transmission will be cancelled by [[DTC]].

---

## Page 11

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 8 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
3.2 MEMSEG Transmission Editing
There are four [[BASIC]] levels of MEMSEG Transmission file error editing.
A "security" error will cause the entire MEMSEG Transmission file to be refused.  This happens when
the Security ("PSW") record fails to properly identify the transmitter to [[DTC]]'s [[CCF]]-II system.  When
a "security" error is detected, the MEMSEG Acknowledgment file will contain a single record, the
Error ("ERR") record.
A "header" error will cause the remainder of the MEMSEG Transmission file to be refused.  If the
Header ("HDR") record fails to properly identify the transmission (i.e. TranID is invalid), or contains
other edit errors, the transmission is refused.  When a "header" error is detected, the MEMSEG
Acknowledgement file will contain only three records, the Control ("CTL") record, the Rejected
Header ("HDR") record and the Audit ("ADT") record.
Any of the following "severe" errors will cause the entire MEMSEG transmission to be cancelled.  All
records are returned unaccepted, but as much editing as possible will be done, and error flags will be
set to provide the user with maximum Acknowledgement information:
C the transmission is received later than the last MEMSEG cutoff time (6:30 p.m.).
C a record type is invalid (not "PSW", "HDR", "DAT" or "TLR");
C a record sequence error is detected (e.g. the last record is not the "TLR");
C a numeric Trailer record field contains non-numeric data; or
C a Trailer record total does not match the [[DTC]]-calculated total for all Data/Remarks records
received.  This may occur if the Trailer total is incorrect or the corresponding field on any
Data record contains non-numeric data.

---

## Page 12

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 9 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
3.3 MEMSEG Transaction Editing
The [[CCF]]-II Memo Segregation system will accept one data record for each MEMSEG transaction.
A transaction "edit" error will cause that Data record to be rejected.  If any of the following "edit"
errors occurs, the MEMSEG transaction is rejected, and the returned Acknowledgement record will
contain appropriately set error flags:
C a field contains invalid data;
C a field is not properly formatted (e.g. non-numeric data in a numeric field); or
C an unused field is not properly initiated (see next page).
As long as no "security", "header/TranID" or "severe" errors are detected, [[DTC]] will accept and
process all MEMSEG transactions that are deemed valid.

---

## Page 13

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 10 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
4.0 MEMSEG Transmission Record Formats
Note: Please ensure that the following standard [[CCF]]-II editing criteria are adhered to for all MEMSEG
Transmission records:
Numeric fields (NUM) -- MUST be right-justified, with leading zeroes.  MUST contain numeric data
only.  If unused, MUST be initialized to zeroes.
Character fields (CHAR) -- should be left-justified, with trailing spaces.  If unused, MUST be initialized
to spaces.
Failure to comply with the above criteria will cause a MEMSEG record to be rejected.
Please ensure that all MEMSEG fields which are not used, whether "Filler", "Optional", "Reserved" or "Not
Allowed", are initialized as described above.  Any such field which contains low-values is considered an edit
error, and will result in rejection of the MEMSEG record.

---

## Page 14

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 11 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
4.1 The [[CCF]]-II Transmission SECURITY Record ("PSW")
The [[CCF]]-II Security record transmitted to [[DTC]] introduces and identifies the transmitter to the [[CCF]]-II
system.  This is done via the SIGNON [[ID]] and Password, which must always be valid and up-to-date.
Where security is a consideration at the user's site, the record may be concatenated in front of the data file
from another source.
The Security record is for input purposes only, and therefore is not returned in [[DTC]]'s Acknowledgement
filer.  Its format is described below.
[[CCF]]-II Transmission Security Record ("PSW")
Position Length Format Field Name Field Description
1 3 Character Record Identifier Must be "PSW", identifying the Security/Password
record.
4 4 Character SIGNON [[ID]] Must be a valid [[DTC]] [[participant]] number ("nnnn") or
Group User [[ID]].  ("Gnnn").
8 2 Character Filler [[DTC]] use only; [[DO]] not use.
10 6 Character [[DTC]]-Assigned Obtained from [[DTC]]'s [[participant]] Interface Planning
Password Group.
16 6 Character Activity Type Must be "MEMSEG" specifying the nature of the
transmission.
22 3 Numeric Transmission [[ID]] Identifies this transmission as unique for the
submitting SIGNON [[ID]].  Must agree with TranID in the
"HDR" record to follow.
25 56 Character Filler [[DTC]] use only; [[DO]] not use.

---

## Page 15

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 12 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
4.2 The MEMSEG Transmission HEADER Record ("HDR")
.
The MEMSEG Header ("HDR") record is considered the first record in the Memo Segregation file.  Its format
appears in the table below
MEMSEG Transmission Header Record ("HDR")
Position Length Format Field Name Field Description
1 3 Character Record Identifier Must be "HDR", identifying the MEMSEG Header
record.
4 4 Character Filler [[DTC]] use only; [[DO]] not use.
8 4 Character SIGNON [[ID]] Identifies the transmitting [[participant]] or service bureau,
"Gnnn" for Group Users or "nnnn" for Participants.
12 6 Numeric Transmission MMDDYY format.
Date
18 6 Character Activity Type Must be "MEMSEG", identifying a Memo Segregation
transmission.
24 3 Numeric Transmission [[ID]] Identifies this transmission as unique for the
submitting SIGNON [[ID]].  Must agree with TRANID in
the "PSW" record.
27 1 Character Filler [[DTC]] use only. [[DO]] not use.
28 1 Character Processing Indicating whether the transmission is for live
[[Option]] (Production) or testing purposes.
"T" = Test transmission
"P" = Production transmission
29 52 Character Filler [[DTC]] use only; [[DO]] not use.

---

## Page 16

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 13 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
4.3 The MEMSEG Transmission Data Record ("DAT")
Each MEMSEG Data ("DAT") record represents a single MEMSEG Segregation transaction.  The record format
appears in the table below.
MEMSEG Transmission Data Record ("DAT")  (Part 1 of 2)
Position Length Format Field Name Field Description
1 3 Character Record Identifier Must be "DAT", identifying the MEMSEG Data record.
4 4 Character Filler [[DTC]] use only. [[DO]] not use.
8 4 Character [[participant]] Must match the "HDR" record"s SIGNON [[ID]] or be an
Number eligible [[Member]] for the Group User SIGNON [[ID]] that
initiated the MEMSEG transmission.
12 2 Character Filler [[DTC]] use only; [[DO]] not use.
14 9 Character [[CUSIP]] Number [[CUSIP]] Number of the security to be segregated.
23 1 Character Filler [[DTC]] use only; [[DO]] not use.
24 9 Numeric Security The total number of [[securities]] to be Segregated.
Quantity
33 1 Character Action Code The code representing the MEMSEG segregation action
to be taken.
"  ","0" [blank or zero] Segregate this
number of [[securities]], or
overlay the previous
segregation with this amount.
"A" Add these [[securities]] to
the quantity previously
segregated.
"S" Subtract these [[securities]]
from the quantity
previously segregated.
34 1 Character Version Control Current value is:
"D" Security Quantity for Stocks
and [[Bonds]] 1 = 1.
35 46 Character Filler [[DTC]] use only; [[DO]] not use.

---

## Page 17

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 14 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
4.4 The MEMSEG Transmission TRAILER Record ("TLR") 
The Trailer record is required as the last record of each MEMSEG transmission.  It includes control totals for the
number of Data records and number of [[securities]] within the transmission.  Its format is described in the following
table.
MEMSEG Transmission Trailer Record ("TLR")
Position Length Format Field Name Field Description
1 3 Character Record Must be "TLR", indicating the Trailer record.
Identifier
4 4 Character Filler [[DTC]] use only. [[DO]] not use.
8 4 Character SIGNON [[ID]] SIGNON [[ID]] of the transmitting [[participant]] or Group
User.
12 6 Character Activity Type Must be "MEMSEG".
18 3 Numeric Transmission- Must match TranID of MEMSEG "HDR" record.
[[ID]]
21 5 Numeric Total Data The total number of DATA records in this MEMSEG
Record Count transmission.  This total EXCLUDES THE TRAILER
RECORD.  It must be right-justified with leading zeroes,
and must equal the [[DTC]]-calculated total Data record
count.
26 13 Numeric Total Security The total Security Quantity for all Data records in this
Quantity MEMSEG transmission.  Must be right-justified with
leading zeroes, and must equal the [[DTC]]-calculated total
security quantity.
39 42 Character Filler [[DTC]] use only; [[DO]] not use.

---

## Page 18

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 15 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
5.0 The MEMSEG Acknowledgement File (Output)
The [[CCF]]-II Memo Segregation Acknowledgement file consists of six different types of record, each of
which consists of 80 characters.  The "Error", "Control" and "Audit" records are for control purposes.  The
remaining Acknowledgement records are Rejected "Header", "Data" and "Trailer" records, returned with
embedded error flags to indicate the type and severity of edit error that is detected.
The MEMSEG Acknowledgement file is composed of:
C an Error ("ERR") record (if a "security" violation occurs);
----     OR    ----
C a Control ("CTL") record; AND
C Zero or more Rejected "HDR", "DAT", and "TLR" records; AND
C an Audit ("ADT") record describing the data accepted.
If the MEMSEG Transmission is accepted as fully valid, the MEMSEG Acknowledgement File is returned to
the user, containing summary information in the Control ("CTL") and Audit ("ADT") records.

---

## Page 19

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 16 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
5.1 MEMSEG Acknowledgement Records
The six record types which may appear in the [[CCF]]-II Memo Segregation Acknowledgement file,
along with [[BASIC]] rules for their appearance, are provided below.
1. [[CCF]]-II Acknowledgement Error record:  whenever the MEMSEG Security "PSW" record's
signon and/or password fail [[DTC]]'s security check, the Acknowledgement file contains only
an "Error" ("ERR") record.
2. MEMSEG Acknowledgement Control record:  if no security violations are detected, a Control
("CTL") record is the first record of the Acknowledgement File.
3. MEMSEG Acknowledgement Rejected Header record:  if a "header" or "severe" edit error is
detected, the Rejected Header ("HDR") follows the "CTL" record in the Acknowledgement
file.  A "header" edit violation results in the "HDR" being the only Rejected record type on the
Acknowledgement file (i.e. no further editing is done by [[DTC]]).  A "severe" edit error implies
that the input "HDR" was accepted, but that the entire transmission has been rejected, and
more Rejected records will follow.
4. MEMSEG Acknowledgement Rejected Data ("DAT") records:  any MEMSEG transactions
that contains "edit" error is rejected, and returned as an Acknowledgement Rejected Data
"DAT" record with error flags embedded.  The record may also be rejected and returned if
the MEMSEG transmission contains "severe" edit errors.
5. MEMSEG Acknowledgement Rejected Trailer record:  if a "severe" edit error is detect, the
Rejected Trailer ("TLR") will be the penultimate record in the Acknowledgement file.  The
Rejected "TLR" record provides details of any errors detected in the input Trailer record.
6. MEMSEG Acknowledgement Audit record: appears as the last record of the
Acknowledgement file, if no "security" edit errors are detected.  The "ADT" record provides
summary totals for all accepted MEMSEG Transmission records.

---

## Page 20

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 17 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
6.0 MEMSEG Acknowledgement Record Format
6.1 The [[CCF]]-II Acknowledgement Error Record ("ERR")
A [[CCF]]-II Error ("ERR") record is created by the [[CCF]]-II system whenever a security violation occurs.  If the
Security ("PSW") input record contains erroneous information, the Error "ERR" record is returned as the ONLY
Acknowledgement record.
The format of the Error ("ERR") record is described in the table appearing 
[[CCF]]-II Acknowledged Error Record ("ERR")  (Part 1 of 2)
Position Length Format Field Name Field Description
1 3 Character Record Identifier Will be "ERR", indicating the Error record.
4 4 Character Filler [[DTC]] use only;  [[DO]] not use.
8 4 Character SIGNON [[ID]] SIGNON [[ID]] from JCL parameter.
12 8 Character Filler [[DTC]] use only; [[DO]] not use.
20 6 Numeric Transmission Date Transmission Date: for Acknowledgement File (current
date - MMDDYY).
26 6 Character Activity Type Activity Type from JCL parameter
32 3 Numeric Transmission [[ID]] Transmission [[ID]] from JCL parameter.
35 2 Character Filler [[DTC]] use only;  [[DO]] not use.
37 3 Numeric Error Status Code Indicating the nature of the security violation detected
by [[DTC]]'s [[CCF]]-II system.
222 Invalid Password detected
300 Invalid Activity Type
detected.
333 Signon Ineligible for Activity
Type.
40 5 Character Filler [[DTC]] use only; [[DO]] not use.
45 6 Numeric [[DTC]] Transmission HHMMSS format.
Arrival Time

---

## Page 21

THE DEPOSITORY TRUST & CLEARING CORPORATION
6.1 The [[CCF]]-II Acknowledgement Error Record ("ERR") (Continued)
[[CCF]]-II Acknowledged Error Record ("ERR")  (Part 2 of 2)
Position Length Format Field Name Field Description
4.02 MEMSEG USER'S GUIDE Page 18 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
51 6 Numeric [[DTC]] Edit Completion HHMMSS format.
Time
57 24 Character Error Description A brief description of the security violation.

---

## Page 22

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 19 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
6.2 The MEMSEG Acknowledgement Control Record ("CTL")
Whenever a Security record is fully validated (i.e. no security violations are detected), the Control ("CTL")
record will be the first record of the MEMSEG Acknowledgement file.  The Control record, summarizing
[[DTC]]'s processing of the MEMSEG transmission file, in described below.
MEMSEG Acknowledgement Control Record ("CTL")  ( Part 1 of 2)
Position Length Format Field Name Field Description
1 3 Character Record Identifier Will be "CTL", indicating the Control record.
4 4 Character Filler [[DTC]] use only; [[DO]] not use.
8 4 Character SIGNON [[ID]]. SIGNON [[ID]].: From JCL parameter.
12 8 Character Filler [[DTC]] use only;  [[DO]] not use.
20 6 Numeric Processing Date The date the transmission was processed by [[DTC]]
(MMDDYY).
26 6 Character Activity Type Activity Type will be "MEMSEG".
32 3 Numeric Transmission [[ID]] Transmission [[ID]].: From JCL parameter.
35 1 Character Filler [[DTC]] use only;  [[DO]] not use.
36 1 Character Processing Processing [[Option]] from "HDR" record.
[[Option]]
37 3 Character Transmission Indicates the status of the MEMSEG Transmission, as
Processing Status processed by [[CCF]]-II.
Code 000 Transmission fully accepted. 
No invalid transactions.
010 Transmission partially
accepted.  Invalid
transactions to follow.
*** Status codes above 099
indicate that Header, Trailer
or Cutoff Time errors
occurred.  The entire
MEMSEG transmission will
be returned.

---

## Page 23

THE DEPOSITORY TRUST & CLEARING CORPORATION
6.2 The MEMSEG Acknowledgement Control Record ("CTL") (Continued)
MEMSEG Acknowledgement Control Record ("CTL")  ( Part 2 of 2)
Position Length Format Field Name Field Description
4.02 MEMSEG USER'S GUIDE Page 20 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
37 Transmission Processing Status Code (continued) :
"333" [[participant]] invalid for Group
User Signon [[ID]].
"444" No file was
transmitted/received.
"555" Transmission received
outside cutoff parameters.
"600" Header and Trailer records
invalid.
"666" Function MEMSEG
temporarily unavailable.
"700" Trailer Total Record Count
does not match [[DTC]]
calculation.
"777" Trailer Total Security
Quantity does not match
[[DTC]] calculation.
"800" Trailer Record missing.
"888" Trailer record contains invalid
data.
"900" Header record missing.
"900" Header and Trailer records
missing.
"999" Header record contains
invalid data.
40 5 Numeric Returned Record The total number of erroneous records returned to the
Count transmitter.
45 6 Numeric [[DTC]] HHMMSS format.
Transmission
Arrival Time
51 6 Numeric [[DTC]] Edit HHMMSS format.
Completion Time
57 24 Character Filler [[DTC]] use only;  [[DO]] not use.

---

## Page 24

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 21 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
6.3 The MEMSEG Acknowledgement Rejected Header Record ("HDR")
Whenever a "header" edit error is detected, the remainder of the MEMSEG Transmission file is refused.  In this
case, the MEMSEG Acknowledgement file will contain only two records -- the "CTL" and Rejected "HDR" records. 
A "header" edit error is distinguished by a non-zero value in one more) of the Rejected "HDR" record's error flags.
"Severe" edit errors also cause the Rejected "HDR" record to appear in the Acknowledgement file, but in these
situations each of the Rejected "HDR" record's error flags will contain zeroes.  A Rejected "HDR" record with no
error flags set on (i.e. set to a non-zero value) implies that a "severe" edit error was detected, and that each
subsequent record of the MEMSEG Transmission (input) file will, in turn, appear as a rejected record in the
MEMSEG Acknowledgement file.
The format of the Rejected Header record follows.
MEMSEG Acknowledgement Rejected Header Record ("HDR")  (Part 1 of 2)
Position Length Format Field Name Field Description
1 3 Character Record Identifier Will be "HDR", indicting the rejected Header record.
4 25 Character Input Header Record This area contains the information received in positions
4-28 of the MEMSEG Transmission file's "HDR" record.
29 6 Numeric Header Record's Error A series of six, 1-byte fields to provide indication of the
Flags type and severity of error that may have occurred.
29 1 Numeric Flag #1 Record Identifier:
"0" = first Record received is "HDR".
"1" = first Record received is not "HDR".
30 1 Numeric Flag #2 SIGNON [[ID]]:
"0" = Signon [[ID]] is valid.
"1" = Signon [[ID]] does not match JCL Signon [[ID]].
31 1 Numeric Flag #3  Transmission Date:
"0" = Valid Transmission date.
"1" = Non-numeric Transmission date.
"2" = Transmission date does not match [[DTC]]
Processing date.
32 1 Numeric Flag #4 Activity Type:
"0" = Activity type is "MEMSEG"
"1" = Activity type not "MEMSEG".

---

## Page 25

THE DEPOSITORY TRUST & CLEARING CORPORATION
6.3 The MEMSEG Acknowledgement Rejected Header Record ("HDR") (Continued)
MEMSEG Acknowledgement Rejected Header Record ("HDR")  (Part 2 of 2)
Position Length Format Field Name Field Description
4.02 MEMSEG USER'S GUIDE Page 22 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
33 1 Numeric Flag #5 Transmission [[ID]]:
"0" = TranID is accepted.
"1" = TranID is non-numeric.
"2" = TranID is zero.
"3" = TranID is not unique today.
"4" = TranID does not match JCL TranID.
34 1 Numeric Flag #6 Processing [[Option]]:
"0" = Processing [[Option]] valid.
"1"  =Processing [[Option]] not "T" or "P".
35 44 Character Filler [[DTC]] use only;  [[DO]] not use.

---

## Page 26

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 23 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
6.4 The MEMSEG Acknowledgement Rejected Data Record ("DAT") 
Whenever a MEMSEG Data ("DAT") record contains an edit error, it is returned in the Acknowledgement file, with
one or more of its 5 embedded error flags set to indicate the type of error encountered.  The format of the Rejected
Data Record appears below.
MEMSEG Acknowledgement Rejected Data Record ("DAT")  (Part 1 of 2)
Position Length Format Field Name Field Description
1 3 Character Record Identifier Record Identifier from input record ("DAT", if field is valid).
4 34 Character Input Data This area contains the information received in positions 4-37 of
Record the MEMSEG Data record.
38 - 42 5 Numeric Data Record's A series of five, 1-byte fields to provide indication of the type
Error Flags and severity of error that may have occurred.
38 1 Numeric Flag #1 Record Identifier:
"0"  = Record Identifier is valid.
"1"  =  Record Identifier is not "DAT".
39 1 Numeric Flag #2 [[participant]] Number: 
"0"  =  [[participant]] Number is valid.
"1"  =  [[participant]] Number not valid for Group User Sign-on [[ID]]
"2"  =  [[participant]] Number is non-numeric.
"3"  =  [[participant]] Number does not match Sign-on [[ID]].
"4"  =  [[participant]] is ineligible for [[DTC]] processing.
"5"  =  [[participant]] is frozen for [[DTC]] processing
40 1 Numeric Flag #3 [[CUSIP]] Number:
"0" =  [[CUSIP]] is valid.
"1" =  [[CUSIP]] is invalid.
"2" =  [[CUSIP]] is ineligible for [[DTC]] processing
"3" =  [[CUSIP]] is bond and format (odd lot debt) indicator does not
equal "D"
41 1 Numeric Flag #4 Security Quantity:
"0"  =  Security Quantity is valid.
"1"  =  Security Quantity is non-numeric.
"2"  =  Security Quantity is zero for Action Codes "A" or "S".

---

## Page 27

THE DEPOSITORY TRUST & CLEARING CORPORATION
6.4 The MEMSEG Acknowledgement Rejected Data Record ("DAT")  (Continued)
MEMSEG Acknowledgement Rejected Data Record ("DAT")  (Part 2 of 2)
Position Length Format Field Name Field Description
4.02 MEMSEG USER'S GUIDE Page 24 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
42 1 Numeric Flag #5 Action Code:
"0"  =  Action Code is valid.
"1"  =  Action Code is invalid (not blank, "0", "A" or "S").
43 38 Character Filler [[DTC]] use only; [[DO]] not use.

---

## Page 28

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 25 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
6.5 The MEMSEG Acknowledgement Rejected Trailer Record ("TLR")
A "severe" edit error will cause the Rejected "TLR" record to be returned in the Acknowledgement file.  If each of
the Rejected "TLR" record's error flags contains zeroes, the MEMSEG transmission was rejected due to a non-
Trailer related "severe" edit error.  If any of the Rejected "TLR" record's error flags does not contain zeroes, the
Trailer record was the source of the "severe" edit error.
The format of the Rejected Trailer record follows.
MEMSEG Acknowledgement Rejected Trailer Record ("TLR")  (Part 1 of 2)
Position Length Format Field Name Field Description
1 3 Character Record Identifier Record Identifier should be "TLR"
4 40 Character Input Trailer This area contains the information received in positions 4-43
Record of the MEMSEG Trailer record.
44 6 Numeric Trailer Record's A series of seven, 1-byte fields to provide indication of the
Error Flags type and severity of error that may have occurred.
44 1 Numeric Flag #1 Record Identifier: 
"0" = Record Identifier is valid.
"1" = Record Identifier is not "TLR".
45 1 Numeric Flag #2 SIGNON [[ID]]:
"0" = Signon [[ID]] is valid.
"1" = Signon [[ID]] does not match JCL parameter.
46 1 Numeric Flag #3 Activity Type:
"0" = Activity Type is valid.
"1" = Activity type not "MEMSEG".
47 1 Numeric Flag #4 Transmission [[ID]]: 
"0" = TranID is valid.
"1" = TranID is non-numeric.
"2" = TranID does not match JCL parameter
48 1 Numeric Flag #5 Total Data Record Count:
"0" = Total Record Count is valid.
"1" = Total Record Count is non-numeric.
"2" = Total Record Count does not match [[DTC]] Calculated
total.

---

## Page 29

4.02.06.05  The MEMSEG Acknowledgement REJECTED TRAILER Record ("TLR") (Continued)
THE DEPOSITORY TRUST & CLEARING CORPORATION
MEMSEG Acknowledgement Rejected Trailer Record ("TLR")  (Part 2 of 2)
Position Length Format Field Name Field Description
4.02 MEMSEG USER'S GUIDE Page 26 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
49 1 Numeric Flag #6 Total Security Quantity:
"0" = Total Security Quantity is valid.
"1" = Total Security Quantity is non-numeric.
"2" = Total Security Quantity does not match [[DTC]]-calculated
total.
50 31 Character Filler [[DTC]] use only; [[DO]] not use.

---

## Page 30

THE DEPOSITORY TRUST & CLEARING CORPORATION
4.02 MEMSEG USER'S GUIDE Page 27 May 2001
Copyright © 2001 by The Depository Trust & Clearing Corporation
6.6 The MEMSEG Acknowledgement Audit Record ("ADT") 
The Audit ("ADT") record is the last record of the MEMSEG Acknowledgement file, except when the incoming
transmission experience "security" edit errors.  If no "security" error is detected, the Acknowledgement file's "CTL"
and "ADT" records will bracket any Acknowledgement Rejected records that are returned.
The Audit ("ADT") record has a similar format to the MEMSEG input Transmission Trailer record.  Its identifying
fields, however, are derived from the input Transmission Header record (when it is present), and its totals are
derived from ACCEPTED Data records only.
When transmitted, the Audit ("ADT") record is the final MEMSEG Acknowledgement record.  The MEMSEG
"ADT" Audit record is described in the table below.
MEMSEG Acknowledgement Audit Record ("ADT")  (Part 1 of 2)
Position Length Format Field Name Field Description
1 3 Character Record Identifier Record Identifier:  Will be "ADT".
4 4 Character Filler [[DTC]] use only. [[DO]] not use.
8 4 Character SIGNON [[ID]]. SIGNON [[ID]].:  From JCL parameter.
12 6 Character Activity Type Activity Type:  Will be "MEMSEG".
18 3 Numeric Transmission [[ID]]. Transmission [[ID]].  From JCL parameter.
21 2 Character Filler [[DTC]] use only. [[DO]] not use.
23 5 Numeric Total Accepted The total number of Data records in this MEMSEG transmission
Record Count that were accepted, as calculated by [[DTC]].
28 2 Character Filler [[DTC]] use only; [[DO]] not use.
30 13 Numeric Total Accepted The total Security Quantity from all the accepted Data records in
Security this MEMSEG transmission, as calculated by [[DTC]].
Quantity
43 38 Character Filler [[DTC]] use only; [[DO]] not use.