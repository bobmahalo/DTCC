---
title: "G:\BSD\CCFWEB\WORDPERFMISCCOLOAN.PDF"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/06coloan.pdf"
pages: 8
size: "150.0 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# G:\BSD\CCFWEB\WORDPERFMISCCOLOAN.PDF

**Original File:** [06coloan.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/06coloan.pdf)  
**Category:** Other  
**Total Pages:** 8  
**File Size:** 150.0 KB  

---

## Page 1

[[CCF]]/[[CCF]]-II/MDH Transmission Guides
16.6 [[collateral]] Loan Closing Balances
(COLOAN) via [[CCF]]/[[CCF]]-II: User's Guide
The [[Depository Trust Company]] July 1997

---

## Page 2

THE [[Depository Trust Company]]
16.6 COLOAN: FUNCTION USER'S GUIDE JULY 1997Copyright © 1997 by The [[Depository Trust Company]]
Copyright © 1997 by The [[Depository Trust Company]] (“[[DTC]]”). All right s
reserved. This work is proprietary and is intended for the exclusive use of [[DTC]]’s
Participants and other users of [[DTC]]’s services. No part of this work may b e
reproduc ed or distributed (including by transmission) in any form or by an y
means, or stored in any information storage and retrieval system, without [[DTC]]’s
prior written permission.

---

## Page 3

THE [[Depository Trust Company]]
16.6 COLOAN: FUNCTION USER'S GUIDE JULY 1997Copyright © 1997 by The [[Depository Trust Company]]
16.6 [[collateral]] Loan Closing Balances (COLOAN) via
[[CCF]]/[[CCF]]-II: User's Guide
Table of Contents
Section Title Page
1. Objectives of This Chapter .............................................. 1
2. The COLOAN Function: Overview ....................................... 1
2.1 Availability of COLOAN ............................................. 1
2.2 Available Transmission Modes ........................................ 1
3. COLOAN Record Templates ............................................ 2
3.1 [[CCF]] Header Record ................................................ 3
3.2 [[CCF]]-II Header and Trailer Record ..................................... 4
3.3 [[collateral]] Loan Closing Balance Record ................................. 5

---

## Page 4

THE [[Depository Trust Company]]
16.6 COLOAN: FUNCTION USER'S GUIDE Page 1 NOVEMBER 1996Copyright © 1996 by The [[Depository Trust Company]]
1. Objectives of This Chapter
The objectives of this chapter are:
• To give information about the [[collateral]] Loan function (COLOAN).
• Illustrate the formats for required COLOAN records.
2. The COLOAN Function: Overview
[[CCF]]/[[CCF]] II users can receive [[DTC]] [[collateral]] Loan Closing Balance information via
the COLOAN function. In general, the COLOAN function gives [[DTC]] Pledgee Banks
daily access to the [[collateral]] Loan Closing Balance via [[CCF]]/[[CCF]] II in a machine-
readable format.
Information received via the DTF/COLOAN function can be used to automate the
updating of users’ files and to verify transaction processing sent to [[DTC]].
2.1 Availability of COLOAN
COLOAN is normally available daily from 4:00 a.m. until 5:00 p.m. (Eastern Time).
2.2 Available Transmission Modes
COLOAN files are available via [[CCF]] and [[CCF]]-II. Users requesting COLOAN via
[[CCF]] receive a file consisting of a [[CCF]] Header Record followed by the requested
COLOAN record. Users requesting COLOAN via [[CCF]]-II receive a file consisting of
[[CCF]]-II Header and Trailer Records separated by the requested COLOAN record.
The formats for the [[CCF]] Header Record, [[CCF]]-II Header and Trailer Records,
followed by the [[collateral]] Loan Closing Balance Record are described in Section 3,
COLOAN Record Templates, beginning on page 2.

---

## Page 5

THE [[Depository Trust Company]]
16.6 COLOAN: FUNCTION USER'S GUIDE Page 2 NOVEMBER 1996Copyright © 1996 by The [[Depository Trust Company]]
3. COLOAN Record Templates
As mentioned in Section 2.2 (page 1), transmission record structure depends on
whether a [[participant]] is using [[CCF]] or [[CCF]]-II.
• For [[CCF]] users, the record structure consists of the [[CCF]] Header Record,
followed by the [[collateral]] Loan Closing Balance Record.
• For [[CCF]]-II users, the record structure consists of the [[CCF]]-II Header Record,
followed by the [[collateral]] Loan Closing Balance Record, followed by the
[[CCF]]-II Trailer Record.
The formats of these records are detailed in the remaining parts of this section.

---

## Page 6

THE [[Depository Trust Company]]
16.6 COLOAN: FUNCTION USER'S GUIDE Page 3 NOVEMBER 1996Copyright © 1996 by The [[Depository Trust Company]]
3.1 [[CCF]] Header Record
The [[CCF]] Header Record format is shown below.
Note: NDM users executing NDMDTF01, and RJE 3770 users executing
RJESDTF2, receive the [[CCF]] Header Record described below:
[[CCF]] Header Record Format
Position Length Format Field Name Field Description
1 6 Character Data Type COLOAN Data type name
Requested with which this data was
requested.
7 6 Character Data Type COLOAN Data type name
Created with which this data was
created.
13 8 Character Data Date mm/dd/yy.
21 8 Character Data Load mm/dd/yy.
Date
29 8 Character [[DTC]] Data Load hh:mm:ss.
Time
37 2 binary Record Size Size of each data record.
39 4 Binary Block Count Number of data blocks input to
CCFDTFDB.
43 4 Binary Record Count Number of data records.
47 ??? Character Filler [[DTC]] use only; [[DO]] not use.

---

## Page 7

THE [[Depository Trust Company]]
16.6 COLOAN: FUNCTION USER'S GUIDE Page 4 NOVEMBER 1996Copyright © 1996 by The [[Depository Trust Company]]
3.2 [[CCF]]-II Header and Trailer Record
The format of each [[CCF]]-II Header and Trailer Record is as described below. Please
note that the Header and Trailer Records are identical except for the first and last
field of each record.
CFF-II Header and Trailer Record ([[DTC]] Transmits to User) Format
Position Length Format Field Name Field Description
1 3 Character Record HDR or TLR.
Identifier
4 4 Character Signon [[ID]] Signon [[ID]].
8 6 Character Data Type COLOAN.
Requested
14 6 Character Data Type COLOAN.
Created
20 8 Character Data Creation mm/dd/yy.
Date
28 8 Character Data Load mm/dd/yy.
Date
36 8 Character Data Load hh:mm:ss.
Time
44 4 Numeric Record Length Record Length of data
requested.
48 8 Numeric Record Count Number of data records in file.
56 4 Numeric 80-byte Record Number of 80-byte records per
Count data type requested.
60 15 Character Filler [[DTC]] use only; [[DO]] not use.
75 6 Numeric Sequence Numbering sequence; used as a
data integrity check.
HDR 000000
TLR 999999

---

## Page 8

THE [[Depository Trust Company]]
16.6 COLOAN: FUNCTION USER'S GUIDE Page 5 NOVEMBER 1996Copyright © 1996 by The [[Depository Trust Company]]
3.3 [[collateral]] Loan Closing Balance Record
The following is a description of the [[collateral]] Loan Closing Balance Record:
[[collateral]] Loan Closing Balance Record Format
Position Length Format Field Name Field Description
1 4 Character Filler [[DTC]] use only; [[DO]] not use.
5 4 Character [[participant]] nnnn 4-character [[participant]]
Number number.
9 5 Character Date of Loan yyddd.
14 2 Character Filler [[DTC]] use only; [[DO]] not use.
16 9 Character [[CUSIP]] Number 9-character [[CUSIP]] number.
25 1 Character Filler [[DTC]] use only; [[DO]] not use.
26 36 Numeric Filler [[DTC]] use only; [[DO]] not use.
62 13 Numeric Share Quantity Share quantity, in units of 1.
75 14 Numeric Expanded Price 9(7)V9(7) seven whole dollar
Per Share characters followed by
seven fractional dollar
characters, with an implied
decimal point in between
(see note below).
89 18 Numeric Expanded 9(16)V9(2) sixteen whole
Valuation dollar characters followed
by two characters repre-
senting cents, with an
implied decimal point in
between.
107 4 Character Filler [[DTC]] use only; [[DO]] not use.
Note: The price per share is provided on a best-efforts basis only. [[DTC]] does not
guarantee the accuracy of this field.