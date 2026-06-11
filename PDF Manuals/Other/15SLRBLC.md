---
title: "15SLRBLC.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/15SLRBLC.pdf"
pages: 10
size: "320.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# 15SLRBLC.pdf

**Original File:** [15SLRBLC.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/15SLRBLC.pdf)  
**Category:** Other  
**Total Pages:** 10  
**File Size:** 320.4 KB  

---

## Page 1

 CF2/MQ Transmission Guides 
 
 
 
 
5.15: SLRBLC: 
Function User’s Guide 
 
 
 
 
 
 
 
 
The [[Depository Trust Company]] July 2014  


---

## Page 2

  Copyright  
5.15: SLRBLC Function User's Guide  ii 
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
 
5.15: SLRBLC Function User's Guide  iii 
 
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
5.15: SLRBLC Function User's Guide  iv 
Contents 
Copyright ................................ ................................ ................................ ................................ ........... ii 
Document History ................................ ................................ ................................ .............................  iii 
1. The SLRBLC Function ................................ ................................ ................................ ......................5 
1.1 Overview ............................................................................................................................................. 5 
1.2 Availability ........................................................................................................................................... 5 
2. Header and Trailer Records................................ ................................ ................................ .............6 
2.1 The [[CCF]] Header Record ...................................................................................................................... 6 
2.2 The CF2 Header and Trailer Records ................................................................................................... 7 
2.2.1 NDM – CF2 Header and Trailer Records ...................................................................................... 7 
2.2.2 FTP - CF2 Header and Trailer Records .......................................................................................... 8 
3. The SLRBLC Data Record ................................ ................................ ................................ .................9 
 
 

---

## Page 5

   Overview 
5.15: SLRBLC Function User's Guide  5 
1. The SLRBLC Function 
1.1 Overview 
In general, the "[[Stock]] Loan/Repo Composite Closing Balances" (SLRBLC) function enables all [[DTC]] 
Participants to access information concerning the composite balances by security of their [[Stock]] Loan 
and Repo accounts at [[DTC]].  The records will be generated for all eligible Participants that have an 
account balance, and will include data for those accounts that contain a net zero balance. 
1.2 Availability 
SLRBLC will generally be available from 10:00 P.M. until approximately 5:00 P.M. the next [[DTC]] 
business day.

---

## Page 6

   Header and Trailer Records 
5.15: SLRBLC Function User's Guide  6 
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
"SLRBLC" 
7 6 Character Data Type 
Created 
"SLRBLC" 
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
5.15: SLRBLC Function User's Guide  7 
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
"SLRBLC" 
14 6 Character Data Type 
Created 
"SLRBLC" 
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
5.15: SLRBLC Function User's Guide  8 
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
"SLRBLC" 
18 6 Character Data Type 
Created 
"SLRBLC" 
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

   The SLRBLC Data Record 
 
5.15: SLRBLC Function User's Guide  9 
3. The SLRBLC Data Record 
The remaining records on the file will be SLRBLC Data Records. 
The records are composed of two portions a universal 26-byte segment which is attached to the front of 
each Data Record, and the actual Data Record itself. 
Position Length Format Field 
Name 
Field Description 
 
1 
 
1 
 
Character 
 
Feedback 
Indicator 
 
Indicates record is in new format. A constant "*". 
 
2 
 
1 
 
Character 
 
Test/ 
Production 
Indicator 
 
For this function a constant "P". 
 
3 
 
6 
 
Character 
 
Record Type 
 
For this function a constant "SLRBLC". 
 
9 
 
2 
 
Numeric 
 
Record 
Suffix 
 
For this function a constant "00". 
 
11 
 
2 
 
Numeric 
 
Version 
Number 
 
Data format version. With this release a constant 
"01". 
 
13 
 
6 
 
Character 
 
User 
Reference 
Number 
 
For this function, a constant spaces. 
 
19 
 
8 
 
Character 
 
[[participant]] 
[[ID]] 
 
The [[participant]] or other entity for whom this data is 
created for. 
 
27 
 
9 
 
Character 
 
[[CUSIP]] 
 
[[CUSIP]] Number 
 
36 
 
1 
 
Character 
 
Security 
Issue Type 
"1" = [[Stock]] 
"5" = Corporate Bond 
"7" = Muni Bond 
 
37 
 
3 
 
Character 
 
Security 
Sub-Issue 
Type 
"000" = [[default]].  No sub-issue type 
"120" = Preferred Commercial Paper (CP) 
"220" = Muni VRDO/CP 
"330" = Muni CP 
"502" = Bankers Acceptance (BA) 
"504" = Institutional Certificate of Deposit (CD) 
"510" = Interest at Maturity (IAM) CP 
"520" = Discount CP 
"525" = Corporate CP 

---

## Page 10

   The SLRBLC Data Record 
 
5.15: SLRBLC Function User's Guide  10 
Position Length Format Field 
Name 
Field Description 
"526" = Corporate VRDO/CP 
"530" = Medium Term Note (MTN) 
"531" = Deposit Note 
"532" = Medium Term Bank Note 
"540" = Collateralized Mortgage Obligation (CMO) 
"541" = [[Asset]] Backed Security 
"550" = Short Term Bank Note 
"560" = Discount Note 
 
40 
 
13 
 
Numeric 
 
[[Stock]] Loan 
Composite 
Position 
 
Share quantity (signed) expressed in units of 1. If no 
position the field is set to high-values 
 
53 
 
13 
 
Numeric 
 
Repo 
Composite 
Position 
 
Share quantity (signed) expressed in units of 1. If no 
position the field is set to high-values. 
 