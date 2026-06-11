---
title: "23FFSBST.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/23FFSBST.pdf"
pages: 9
size: "322.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# 23FFSBST.pdf

**Original File:** [23FFSBST.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/23FFSBST.pdf)  
**Category:** Other  
**Total Pages:** 9  
**File Size:** 322.2 KB  

---

## Page 1

 CF2/MQ Transmission Guides 
 
 
 
 
5.23 Fed Funds [[settlement]] / Settling Bank 
Balances (FFSBST): 
Function User’s Guide 
 
 
 
 
 
 
 
 
The [[Depository Trust Company]] July 2014  


---

## Page 2

  Copyright  
5.23 FFSBST Function User's Guide  ii 
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
 
5.23 FFSBST Function User's Guide  iii 
 
Document History 
 
03/06/2003   New document  
03/19/14 The following changes were made to bring the existing document up to current 
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
5.23 FFSBST Function User's Guide  iv 
Contents 
Copyright ................................ ................................ ................................ ................................ ........... ii 
Document History ................................ ................................ ................................ .............................  iii 
1. Overview ................................ ................................ ................................ ................................ .......5 
1.1 Holiday Processing .............................................................................................................................. 5 
2. Header and Trailer Records................................ ................................ ................................ .............6 
2.1 The [[CCF]] Header Record ...................................................................................................................... 6 
2.2 The CF2 Header and Trailer Records ................................................................................................... 7 
2.2.1 NDM – CF2 Header and Trailer Records ...................................................................................... 7 
2.2.2 FTP - CF2 Header and Trailer Records .......................................................................................... 8 
3. FFSBST Data Records ................................ ................................ ................................ ......................9 
 
 

---

## Page 5

   Overview 
5.23 FFSBST Function User's Guide  5 
1. Overview 
The FFSBST function will provide Settling Banks with a Legal Entity [[settlement]] balance file.  The file 
will be produced at approximately 4:00 P.M. each day after Final Figures, and will consist of the 
Bank’s Legal Entity [[participant]] accounts and their corresponding [[NSCC]] and [[DTC]] [[settlement]] balances.  
A net [[settlement]] balance will be provided for each [[participant]] along with the participants’ net debits 
and credits.  [[NSCC]] and [[DTC]] balances will be listed separately and will be distinguished by an 
indicator on each record.  
1.1 Holiday Processing 
All Closed: 
Banks, Exchange, [[DTC]] and [[NSCC]] are all closed:  (New Year’s Day, Martin Luther King Day, President’s 
Day, Memorial Day, Independence Day (July 4th), Labor Day, Thanksgiving Day and Christmas Day.   
Processing will not occur and the file will not be available during this time. 
Banks Closed, Exchange, [[DTC]] and [[NSCC]] Open: (Columbus Day, Veterans Day) 
Processing will not occur and the file will not be available during this time. 
Banks and [[DTC]] Open, Exchange and [[NSCC]] Closed: (e.g. Good Friday) 
Normal processing will occur and the file will be available during this time.

---

## Page 6

   Header and Trailer Records 
5.23 FFSBST Function User's Guide  6 
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
"FFSBST" 
7 6 Character Data Type 
Created 
"FFSBST" 
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
5.23 FFSBST Function User's Guide  7 
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
"FFSBST" 
14 6 Character Data Type 
Created 
"FFSBST" 
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
5.23 FFSBST Function User's Guide  8 
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
"FFSBST" 
18 6 Character Data Type 
Created 
"FFSBST" 
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

   [[CCF]] and CF2 Tape Backup Procedure 
 
5.23 FFSBST Function User's Guide  9 
3. FFSBST Data Records 
The remaining records on the deblocked file are APIBAL data records whose format is described below. 
Position Length Format Field 
Name 
FFSBST Record Format Description 
 
1 
 
1 
 
Character 
 
[[CCF]]-TYPE-IND 
 
 ‘*’. 
 
2 
 
1 
 
Character 
 
[[CCF]]-TEST-
PROD-IND 
 
‘P’ Production / ‘T’ Test 
 
3 
 
6 
 
Character 
 
[[CCF]]-REC-TYPE 
 
Function name ‘FFSBST’. 
 
9 
 
2 
 
Character 
 
[[CCF]]-REC-
SUFFIX 
 
‘01’ 
 
11 
 
2 
 
Numeric 
 
[[CCF]]-REC-
VERSION 
 
Version 01 
 
13 
 
6 
 
Character 
 
[[CCF]]-USER-
REF 
 
User Reference number. 
 
19 
 
8 
 
Numeric [[CCF]]-ORG-[[ID]]  
Bank Organization [[ID]]. 
 
27 
 
8 
 
Numeric [[CCF]]-BANK-
ACCOUNT 
 
Settling Bank number. 
 
35 
 
8 
 
Numeric [[CCF]]-LEGAL-
ENTITY 
Legal Entity Account number. 
 
 
43 
 
17 
 
Numeric [[CCF]]-GROSS-
DEBIT PIC 
9(15)V99 
Gross Debit Balance. 
Right Justified left zero filled 
 
60 
 
17 
 
Numeric [[CCF]]-GROSS-
CREDIT 
9(15)V99 
Gross Credit Balance. 
Right Justified left zero filled 
 
77 
 
17 
 
Numeric 
 
[[CCF]]-NET-
DEBIT 
9(15)V99 
 
Netted Balance if Debit 
Right Justified left zero filled 
 
94 
 
17 
 
Numeric 
 
[[CCF]]-NET-
CREDIT 
9(15)V99 
 
Netted Balance if Credit 
Right Justified left zero filled 
 
111 
 
1 
 
Character 
 
[[CCF]]-PART-
IND 
 
‘D’ [[DTC]] Balance / ‘N’ [[NSCC]] Balance 
 
112 
 
 47 
 
Character 
 
Filler 
 
Spaces 
 