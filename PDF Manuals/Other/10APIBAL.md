---
title: "10APIBAL.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/10APIBAL.pdf"
pages: 12
size: "344.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# 10APIBAL.pdf

**Original File:** [10APIBAL.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/10APIBAL.pdf)  
**Category:** Other  
**Total Pages:** 12  
**File Size:** 344.9 KB  

---

## Page 1

 CF2/MQ Transmission Guides 
 
 
 
 
5.10 [[participant]] Closing Balances (APIBAL): 
Function User’s Guide 
 
 
 
 
 
 
 
 
 
 
The [[Depository Trust Company]] July 2014  


---

## Page 2

  Copyright  
5.10 APIBAL Function User's Guide  ii 
Copyright 
Copyright © 2014 by The [[Depository Trust Company]] (“[[DTC]]”). All rights reserved. This work is 
proprietary and is intended for the exclusive use of [[DTCC]]’s Participants and other users of [[DTCC]]’s 
services. No part of this work may be reproduced or distributed (including by transmission) in any 
form or by any means, or stored in any information storage and retrieval system, without [[DTCC]]’s 
prior written permission. 
All requests for additional copies of this work or inquiries about this work should be directed to 
[[DTCC]] [[participant]] Interface Planning, The Depository Trust & Clearing Corporation, 55 Water Street, 
New York, NY 10041, USA. 
 

---

## Page 3

  Document History  
 
5.10 APIBAL Function User's Guide  iii 
 
Document History 
 
6/17/97 Modified APIBAL Record Layout.  Seven byte (7) filler at position 19 broken into 
two separate fields: 19-22 Expanded Pledgee Bank Number, 23-25 Filler. 
6/18/97 Changed Filler descriptions. Deleted i.e. reference from Factor field in APIBAL 
record. 
3/23/99 Added rows to table in section 4.0. Reformatted whole document to [[CCF]] 
formats. 
6/22/99  Changed APIBAL Record Format (p8) Filler length from 28 to 29. 
2/7/01 Added the following rows to section 4.0; Expanded Loan Date (pos. 100); 
Expanded Serial Number (pos. 106), Expanded Trade Date (pos. 114), and Filler 
(pos. 120).  
2/20/03  Document converted from WordPerfect format to MS Word.  
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
5.10 APIBAL Function User's Guide  iv 
Contents 
Copyright ................................ ................................ ................................ ................................ ........... ii 
Document History ................................ ................................ ................................ .............................  iii 
1. The APIBAL Function ................................ ................................ ................................ ......................5 
1.1 Availability of APIBAL .......................................................................................................................... 5 
2. Header and Trailer Records................................ ................................ ................................ .............6 
2.1 The [[CCF]] Header Record ...................................................................................................................... 6 
2.2 The CF2 Header and Trailer Records ................................................................................................... 7 
2.2.1 NDM – CF2 Header and Trailer Records ...................................................................................... 7 
2.2.2 FTP - CF2 Header and Trailer Records .......................................................................................... 8 
3. APIBAL Data Records ................................ ................................ ................................ ......................9 
 
 

---

## Page 5

   The APIBAL Function 
5.10 APIBAL Function User's Guide  5 
1. The APIBAL Function 
A [[CCF]] or CF2 user may use the APIBAL function to receive [[DTC]]'s [[participant]] Account Return Closing 
Balances information. 
When using the APIBAL function, the [[CCF]] or CF2 user will receive a series of machine-readable 
records.  Each record indicates the closing balance for a specific [[CUSIP]] in one of the [[participant]]'s 
[[DTC]] accounts. 
The APIBAL function contains [[participant]] Account Closing Balance information.  APIBAL is available 
for transmission to [[DTC]] participants at the beginning of the next day after the close of business.  
APIBAL contains Closing Balance information from the previous business day. 
The information received via the APIBAL function may be used to automate both the verification of 
a [[participant]]'s closing balance by [[CUSIP]]/Account and the determination of a [[participant]]'s position 
with [[DTC]] at the end of the previous business day. 
1.1 Availability of APIBAL 
APIBAL function will generally be available at approximately 1:00 A.M. the day after closing. 

---

## Page 6

   Header and Trailer Records 
5.10 APIBAL Function User's Guide  6 
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
"APIBAL" 
7 6 Character Data Type 
Created 
"APIBAL" 
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
5.10 APIBAL Function User's Guide  7 
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
"APIBAL" 
14 6 Character Data Type 
Created 
"APIBAL" 
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
5.10 APIBAL Function User's Guide  8 
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
"APIBAL" 
18 6 Character Data Type 
Created 
"APIBAL" 
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

      APIBAL Data Records 
 
5.10 APIBAL Function User's Guide  9 
3. APIBAL Data Records 
The remaining records on the deblocked file are APIBAL data records whose format is described below. 
Position Length Format Field 
Name 
APIBAL Record Format Description 
 
1 
 
9 
 
Character 
 
[[CUSIP]] 
Number 
 
[[CUSIP]] number 
 
10 
 
1 
 
Binary 
 
 
Account 
Type 
 
Account type:  (binary representation) 
10 = general unpledged 
14 =  general pledged 
18 =  general investment 
40 =  withdrawal by transfer 
Note: If this field contains High Values, there is no 
applicable binary account type.  Refer to position 33-35 
for Expanded Account Type. 
 
11 
 
8 
 
Character 
 
Record [[ID]] 
Key 
 
Based on EXPANDED account type.  Positional 
breakdown is: 
EXPANDED Account Types 010 and 040: 
11-18 = low values. 
EXPANDED Account Type 014: 
11-12 = pledgee bank number (packed); 
13-14 = low values; 
15-18 = loan date in YYMMDD format (packed). 
EXPANDED Account Types 018 and 022: 
11-14 = serial number denoting segregation of 
investment security (packed); 
15-18 = low values. 
EXPANDED Account Types 026 and 028: 
11-12 = zero (packed); 
13-14 = low values; 
15-18 = zero (packed). 
EXPANDED Account type RRG: 
11-16 = Reorg Seg Sub-Account [[ID]] 
Format is XYYYZZ, where 
 X = Reorg RRG Sub-account 
 YYY = RAMS Activity Code 
 ZZ  = RAMS Sequence Number. 
17-18  = low values. 
Note: positions 11-18 are unique for a given [[CUSIP]] 
number and Account type. 
 
19 
 
4 
 
Numeric 
 
Expanded 
Pledgee Bank 
Number 
 
For expanded account type 14. For all other account 
types, initialize to zeroes. 
 
23 
 
3 
 
Numeric 
 
Filler 
 
[[DTC]] use only. [[DO]] not use. 
 
26 
 
4 
 
Packed 
 
Trade Date 
 
Trade date in YYMMDD format, for Investment accounts 

---

## Page 10

      APIBAL Data Records 
 
5.10 APIBAL Function User's Guide  10 
Position Length Format Field 
Name 
APIBAL Record Format Description 
only. 
 
30 
 
3 
 
Packed 
 
[[participant]] 
Number 
 
[[participant]] number. 
 
33 
 
3 
 
Character 
 
Expanded 
Account Type 
 
010 =  general unpledged 
014 =  general pledged 
018 =  general investment 
022 =  segregation 
026 =  called security without accrued interest 
028 =  called security with accrued interest 
040 =  withdrawal by transfer 
RRG =  Reorg RRG Sub-account 
[[IPO]] =   [[IPO]] Tracked Position 
 
36 
 
1 
 
Character 
 
Security Issue 
Type 
 
1 = [[Stock]] 
5 = bond 
7 = municipal bond 
 
37 
 
3 
 
Character 
 
Security Sub-
Issue Type 
 
Amortizing sub-issue types are indicated by an asterisk, 
and an Amortized and Accreted Factor will appear in 
position 61-75 (if available) 
000   = [[default]].  No sub-issue type. 
030   = Limited Partnership 
*040 = CMO security denominated in units or 
“'undivided interest”. 
*041 = [[Asset]]-Backed Security denominated in units or 
'undivided interest'. 
*042 = Amortizing Issue not identified as a CMO or [[ABS]], 
denominated in 'units' or 'undivided interest'. 
110   = American Depositary Receipt ([[ADR]]) 
120   = MMI Preferred [[Stock]] (CP-like mode) 
320   = MMI Municipal VRDO (CP-like mode) 
330   = MMI Municipal Commercial Paper (CP) 
340   = Bearer, callable Zero Coupon bond 
502   = MMI Bankers' Acceptance note (BA) 
504   = MMI Institutional Certificate of Deposit (CD) 
505   = Certificated Money Market Instrument (MMI) 
506   = Certified MMI - Periodic Payor 
510   = Interest at Maturity (IAM) CP 
520   = Discount CP 
525   = MMI Corporate CP 
526   = MMI Corporate VRDO (CP-like mode) 
530   = Medium-Term Note (MTN) issued prior to 
8/15/95 and not converted to the MMI 
program. 
*531 = MMI Deposit Note 
*532 = MMI Medium-Term Bank Note 
*533 = MMI Medium-Term Note 
*540 =  Collateralized Mortgage Obligation (CMO) or 
global CMO. 

---

## Page 11

      APIBAL Data Records 
 
5.10 APIBAL Function User's Guide  11 
Position Length Format Field 
Name 
APIBAL Record Format Description 
*541 =  [[Asset]]-Backed Security ([[ABS]]) or global [[ABS]]. 
*"542 =  Amortizing Issue not identified as a CMO or 
[[ABS]]. 
550   =  MMI Short Term Bank Note 
*551 =  Zero Coupon bond denominated in initial 
principal amount. 
560   =  MMI Discount Note 
790   =  Unit Investment Trust ([[UIT]]) 
 
40 
 
1 
 
Character 
 
Security 
[[settlement]] 
Type 
 
1  =   Same Day Funds [[settlement]]. 
 
41 
 
6 
 
Character 
 
Last Activity 
Date 
 
The date this combination of [[participant]]/ [[CUSIP]] last had 
activity at [[DTC]], in YYMMDD format. 
 
47 
 
13 
 
Numeric 
 
Share 
Quantity 
 
Signed, expressed in units of 1. 
 
60 
 
1 
 
Character 
 
Fractional 
[[shares]] 
Indicator 
 
Space = Non-Fractional Share [[CUSIP]] 
F        = Fractional Share [[CUSIP]] 
 
61 
 
14 
 
Character 
 
Factor 
 
Amortized and Accredited Factor for Collateralized 
Mortgage [[obligations]], [[Asset]]-Backed [[securities]] and other 
Amortizing Issues that are not identified as a CMO or 
[[ABS]]. 
For all [[securities]] that are amortizing issues, this field's 
format is 9(2)V9(12), and it will contain a factor (if 
available) or zeroes if the factor is unknown. 
For all other Sub-issue types this field will contain spaces. 
 
75 
 
9 
 
Numeric 
 
Interest Rate 
 
Interest rate 
Format = 9(03)V9(6) 
 
84 
 
8 
 
Character 
 
Maturity Date 
 
Maturity date 
Format = CCYYMMDD 
 
92 
 
8 
 
Numeric 
 
Expanded 
[[participant]] 
Number 
 
Expanded [[participant]] number with leading zeros. 
 
100 
 
6 
 
Character 
 
Expanded 
Loan Date 
 
For expanded account type 014 loan date in YYMMDD 
format. For all other account types initialize to spaces 
 
106 
 
8 
 
Character 
 
Expanded 
Serial 
Number 
 
For account types 018 & 022: Serial Number denoting 
segregation of investment security.  For all other account 
types this field contains low values. 
 
114 
 
6 
 
Character 
 
Expanded 
Trade Date 
 
Expanded Trade Date for investment accounts only in 
YYMMDD format. For all other accounts this field 
contains spaces. 

---

## Page 12

      APIBAL Data Records 
 
5.10 APIBAL Function User's Guide  12 
Position Length Format Field 
Name 
APIBAL Record Format Description 
 
120 
 
1 
 
Character 
 
Filler 
 
[[DTCC]] use only.  [[DO]] not use. 
 