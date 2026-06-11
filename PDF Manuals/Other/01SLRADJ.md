---
title: "01SLRADJ.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/01SLRADJ.pdf"
pages: 11
size: "342.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# 01SLRADJ.pdf

**Original File:** [01SLRADJ.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/01SLRADJ.pdf)  
**Category:** Other  
**Total Pages:** 11  
**File Size:** 342.1 KB  

---

## Page 1

 CF2/MQ Transmission Guides 
 
 
 
 
5.14 SLRADJ: 
Function User’s Guide 
 
 
 
 
 
 
 
 
The [[Depository Trust Company]] July 2014  


---

## Page 2

  Copyright  
5.14 SLRADJ Function User's Guide  ii 
Copyright 
Copyright © 2014 by The [[Depository Trust Company]] (“[[DTC]]”). All rights reserved. This work is 
proprietary and is intended for the exclusive use of [[DTC]]’s Participants and other users of [[DTC]]’s 
services. No part of this work may be reproduced or distributed (including by transmission) in any 
form or by any means, or stored in any information storage and retrieval system, without [[DTC]]’s 
prior written permission. 
All requests for additional copies of this work or inquiries about this work should be directed to 
[[DTCC]] [[participant]] Interface Planning, The Depository Trust & Clearing Corporation, 55 Water Street, 
New York, NY 10041, USA. 

---

## Page 3

  Document History  
 
5.14 SLRADJ Function User's Guide  iii 
 
Document History 
 
03/25/14 The following changes were made to bring the existing document up to current 
standards.  
  Revised [[CCF]] Header Record description.  
Removed references to CCRDTFDB and added NDMDTFGP and 
NDMDTFSP. 
Revised CF2 Header and Trailer Records   
  Changed [[CCF]]-II references to read CF2.  
 Identified existing CF2 HDR and TRL Record Format as NDM specific.  
 Corrected “TLR” in Field Description (position 1) to read “TRL”.  
 Added (0001) to Field Description (position 56).  
 Expanded Filler (position 60) from 15 to ???   
 Removed Sequence Number field (position 75).  
   Added FTP specific CF2 Header and Trailer Record Format. 

---

## Page 4

  Contents     
5.14 SLRADJ Function User's Guide  iv 
Contents 
Copyright ................................ ................................ ................................ ................................ ........... ii 
Document History ................................ ................................ ................................ .............................  iii 
1. The SLRADJ Function ................................ ................................ ................................ ......................5 
1.1 Overview ............................................................................................................................................. 5 
1.2 Availability ........................................................................................................................................... 5 
2. Header and Trailer Records................................ ................................ ................................ .............6 
2.1 The [[CCF]] Header Record ...................................................................................................................... 6 
2.2 The CF2 Header and Trailer Records ................................................................................................... 7 
2.2.1 NDM – CF2 Header and Trailer Records ...................................................................................... 7 
2.2.2 FTP - CF2 Header and Trailer Records .......................................................................................... 8 
3. The SLRADJ Data Record ................................ ................................ ................................ .................9 
 
 

---

## Page 5

   Overview 
5.14 SLRADJ Function User's Guide  5 
1. The SLRADJ Function 
1.1 Overview 
The [[Stock]] Loan /Repo Adjustment Activity function, SLRADJ, enables Participants to receive a file 
containing transaction activity against their [[Stock]] Loan/Repo accounts at [[DTC]].  The records will 
include only [[Stock]] Loan/Repo account adjustment related activity.  Some activity will represent 
actual [[Stock]] Loan and Repo adjustments, and some are implicit adjustments resulting from other 
transactions ( e.g. Deliver Orders). 
Activity reported via the SLRADJ function will not be available in other activity reporting functions. 
1.2 Availability 
SLRADJ will generally be available from 10:00 P.M. until approximately 5:00 P.M. the next [[DTC]] 
business day.

---

## Page 6

   Header and Trailer Records 
5.14 SLRADJ Function User's Guide  6 
2. Header and Trailer Records 
2.1 The [[CCF]] Header Record 
NDM users executing NDMDTF01, NDMDTFGP, or NDMDTFSP will receive the following [[CCF]] Header 
record. 
The [[CCF]] header record's format is as follows: 
 
[[CCF]] Header Record Format 
 
Position 
 
Length 
 
Format 
 
Field Name 
 
Field Description 
1 6 Character Data Type 
Requested 
"SLRADJ" 
7 6 Character Data Type 
Created 
"SLRADJ" 
13 8 Character Creation Date Date of data (MM/DD/YY). 
21 8 Character Spool Date [[DTC]] data load date (MM/DD/YY). 
29 8 Character Load Time [[DTC]] data load time (HH:MM:SS). 
37 2 Binary Record Size Size of each data record. 
39 4 Binary Block Count Number of data blocks input to 
CCFDTFDB. 
43 4 Binary Record Count Number of data records. 
47 ??? Character Filler [[DTC]] use only. [[DO]] not use. 
 
 
  

---

## Page 7

   Header and Trailer Records 
5.14 SLRADJ Function User's Guide  7 
2.2 The CF2 Header and Trailer Records 
The CF2 Header and Trailer records come in two different formats; NDM and FTP.  
NOTE that the Header and Trailer records are identical except for the first and last field of each 
record. 
2.2.1 NDM – CF2 Header and Trailer Records 
NDM users executing NDMDTF02 or NDMDTFGH will receive the following: 
CF2 Header and Trailer Record Format - NDM 
Position Length Format Field 
Name 
Field Description 
1 3 Character Record [[ID]] "HDR" or "TRL" 
4 4 Character Signon [[ID]] Signon [[ID]] 
8 6 Character Data Type 
Requested 
"SLRADJ" 
14 6 Character Data Type 
Created 
"SLRADJ" 
20 8 Character Creation 
Date 
Data Creation Date (MM/DD/YY) 
28 8 Character Spool Date Data Load Date (MM/DD/YY) 
36 8 Character Load Time Data Load Time (HH:MM:SS) 
44 4 Numeric Record 
Length 
Record Length of data requested 
48 8 Numeric Record 
Count 
Number of data records in file. 
56 4 Numeric 80-Byte 
Record 
Count 
Number of 80-byte records per data type 
requested. (0001) 
60 ??? Character Filler [[DTC]] use only. [[DO]] not use. 
 
  

---

## Page 8

   Header and Trailer Records 
5.14 SLRADJ Function User's Guide  8 
2.2.2 FTP - CF2 Header and Trailer Records 
FTP users will get the following: 
 CF2 Header and Trailer Record Format - FTP  
Position Length Format Field 
Name 
Field Description 
1 3 Character Record [[ID]] "HDR" or "TRL" 
4 8 Character Sign-on [[ID]] Sign-on [[ID]] 
12 6 Character Data Type 
Requested 
"SLRADJ" 
18 6 Character Data Type 
Created 
"SLRADJ" 
24 8 Character Creation 
Date 
Data Creation Date (MM/DD/YY) 
32 8 Character Spool Date Data Load Date (MM/DD/YY) 
40 8 Character Load Time Data Load Time (HH:MM:SS) 
48 4 Numeric Record 
Length 
Record Length of data requested 
52 8 Numeric Record 
Count 
Number of data records in file. 
60 4 Numeric 80-Byte 
Record 
Count 
Number of 80-byte records per data type 
requested.  (0001) 
64 ??? Character Filler [[DTC]] use only. [[DO]] not use. 

---

## Page 9

   SLRADJ Data Record 
 
5.14 SLRADJ Function User's Guide  9 
3. The SLRADJ Data Record 
The remaining records on the file will be SLRADJ data records.  
Data records are composed of two parts; a 26-character Transaction Header area followed by a [[Stock]] Loan 
or Repo Transaction. 
Position Length Format Field 
Name 
Field Description 
Standard DTF TRANSACTION HEADER area. 
 
1 
 
1 
 
Character 
 
Feedback 
Indicator 
 
Indicates record is in new format.  A constant "*". 
 
2 
 
1 
 
Character 
 
Production/ 
Test Indicator 
 
For this function, a constant "P". 
 
3 
 
6 
 
Character 
 
Record Type 
 
For this function, a constant "SLRADJ". 
 
9 
 
2 
 
Numeric 
 
Record Suffix 
 
For this function, a constant "01". 
 
11 
 
2 
 
Numeric 
 
Version 
Number 
 
Data format version. 
With this release, a constant "02". 
 
13 
 
6 
 
Character 
 
User 
Reference 
Number 
 
For this function, constant spaces. 
 
19 
 
8 
 
Character 
 
Addressee [[ID]]. 
 
The [[participant]] or other entity for whom this record is 
created. 
 
27 
 
3 
 
Character Transaction 
Type 
 
"007" = CM Swing 
"008" = Security Swing 
"026" = Deliver Order with SLN/RPO  reason 
"031" = [[Stock]] Split 
"131" = Security Exit 
"210" = [[Stock]] Loan Adjustment 
"211" = Repo Adjustment 
 
30 
 
3 
 
Character 
 
Deliver Order 
Reason Code 
"000"            =   [[default]] 
"010"-"029"  =   [[Stock]] Loan [[DO]] 
"081"            =   Repo [[DO]] 
 
33 
 
4 
 
Character 
 
Transaction 
Origin Source 
Code 
For reference purpose only.  A list of valid Codes will 
become available in the near future. 
PLEASE NOTE: the remainder of the SLRADJ file is unchanged in regard to its content, however ALL FIELDS ARE 
DISPLACED BY 6 CHARACTERS from their original positions in VERSION NUMBER 01.  
 
37 
 
1 
 
Character 
 
Journal Code 
 
"0" = Original transaction 
"S" = Same day journal adjustment 

---

## Page 10

   SLRADJ Data Record 
 
5.14 SLRADJ Function User's Guide  10 
Position Length Format Field 
Name 
Field Description 
"N" = Next day journal adjustment 
 
38 
 
3 
 
Character 
 
Account Type 
 
"SLN"  = [[Stock]] Loan 
"RPO"  = Repo 
 
41 
 
1 
 
Character 
 
Status Code 
 
"M" = made transaction  
"E" = edit error input 
"D" = drop reason 
"R" = conditional reject 
 
42 
 
1 
 
Character 
 
Action Code 
 
" "  =  No update (space) 
"+" =  Add to account 
"-"  =  Subtract from account 
 
43 
 
9 
 
Character 
 
[[CUSIP]]  
 
52 
 
1 
 
Character 
 
[[settlement]] 
Code 
"N" = Next Day Fund [[settlement]] 
"S" = Same Day Fund [[settlement]] 
 
53 
 
1 
 
Character 
 
Security Issue 
Type 
"1" = [[Stock]] 
"5" = Corporate Bond 
"7" = Muni Bond 
 
54 
 
3 
 
Character 
 
Security Sub-
Issue Type 
"000" = [[default]]. No sub-issue type 
"120" = Preferred Commercial Paper (CP) 
"220" = Muni VRDO/CP 
"330" = Muni CP 
"502" = Banker Acceptance (BA) 
"504" = Institutional Certificate of Deposit  (CD) 
"510" = Interest at Maturity (IAM) CP 
"520" = Discount CP 
"525" = Corporate CP 
"526" = Corporate VRDO/CP 
"530" = Medium Term Note (MTN) 
"531" = Deposit Note 
"532" = Medium Term Bank Note 
"540" = Collateralized Mortgage Obligation  (CMO) 
"541" = [[Asset]] Backed Security  
"550" = Short Term Bank Note 
"560" = Discount Note 

---

## Page 11

   SLRADJ Data Record 
 
5.14 SLRADJ Function User's Guide  11 
Position Length Format Field 
Name 
Field Description 
 
57 
 
13 
 
Numeric 
 
Share 
Quantity 
(Signed) 
Expressed in units of 1. 
 
70 
 
8 
 
Character  
 
Contra 
[[participant]] 
 
 
78 
 
9 
 
Character 
 
Contra [[CUSIP]] 
 
Activity "08" only. 
 
87 
 
20 
 
Character 
 
[[CUSIP]] 
Description 
 
For MMI only. 
 
107 
 
9 
 
Character 
 
Transaction 
[[ID]] 
 
Record number on [[DTC]] database. For reference 
purposes only. 
 
116 
 
8 
 
Character 
 
Date 
Processed 
 
CCYYMMDD. 
 
124 
 
6 
 
Character 
 
Time 
Processed 
 
HHMMSS. 
 
130 
 
78 
 
Character 
 
Comments 
 
 
 