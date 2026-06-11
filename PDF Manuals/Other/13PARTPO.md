---
title: "5.13 PARTPO: Participant Account Return Payment Order"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/13PARTPO.pdf"
pages: 14
size: "1263.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# 5.13 PARTPO: Participant Account Return Payment Order

**Original File:** [13PARTPO.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/13PARTPO.pdf)  
**Category:** Other  
**Total Pages:** 14  
**File Size:** 1263.2 KB  

---

## Page 1

CF2/MQ TRANSMISSION GUIDES 
5.13 PARTPO: [[participant]] ACCOUNT RETURN PAYMENT ORDER 
J
UNE 2, 2022 
[[DTCC]] Public (White)

---

## Page 2

© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
D
oc Date: June 2, 2022 
Publication Code: SET 156 
Service: [[settlement]] 
Title: 5.13 PARTPO: [[participant]] Account Return Payment Order 
[[DTCC]] Public (White)

---

## Page 3

 
 
TABLE OF CONTENTS 
1. Overview ........................................................................................................................................................... 4 
1.1 Scheduling Use of PARTPO ......................................................................................................................... 4 
2. Header and Trailer Records ............................................................................................................................ 5 
2.1 The [[CCF]] Header Record ................................................................................................................... 5 
2.2.1 NDM – CF2 Header and Trailer Records .................................................................................................. 5 
2.2.2 FTP - CF2 Header and Trailer Records .................................................................................................... 6 
3. Transaction Detail Records ............................................................................................................................. 7 
3.1 SPO Transaction Detail Record ......................................................................................................... 7 
3.2 [[SFT]] PD Payment Order Transaction Detail Record .......................................................................... 8 
3.3 PPO Transaction Detail Record .......................................................................................................10 
4. Release Notes ............................................................................................................................................. 13 
 
[[DTCC]] Public (White)

---

## Page 4

 
1. Overview 4 
 
1. OVERVIEW 
A User may use the PARTPO function in order to receive [[DTC]] [[participant]] Account Return Payment Order 
Transaction information. 
When using the PARTPO function, the User will receive a series of machine-readable records. Each record 
corresponds to a Payment Order transaction which has updated a [[participant]]'s account balance.  
The PARTPO function consists of Payment Orders available for return transmission, at the end of daily 
[[settlement]] processing. The PARTPO transmission contains all original and reclaim Security Payment Order 
(SPO) and [[Premium]] Payment Order (PPO) transactions that have been processed by [[DTC]]'s [[settlement]] 
System during the business day. 
The information received via the PARTPO function may be used to automate the updating of a User's files and 
verification of the daily transaction processing sent by the User to [[DTC]]. 
1.1 Scheduling Use of PARTPO 
PARTPO will generally be available from 3:45 P.M. through 11:45 A.M. the following day.  
[[DTCC]] Public (White)

---

## Page 5

2. Header and Trailer Records 5  
2. HEADER AND TRAILER RECORDS
2.1 The [[CCF]] Header Record 
NDM users executing NDMDTF01, NDMDTFGP, or NDMDTFSP will receive the following [[CCF]] Header record.  
The [[CCF]] header record's format is as follows: 
Position Length Format  Field Name Field Description 
1 6 Character Data Type 
Requested 
Value "PARTPO". 
7 6 Character Data Type 
Created 
Value "PARTPO". 
13 8 Character Creation Date Date of data (MM/DD/YY). 
21 8 Character Spool Date [[DTC]] data load date (MM/DD/YY). 
29 8 Character Load Time [[DTC]] data load time (HH:MM:SS). 
37 2 Binary Record Size Size of each data record. 
39 4 Binary Block Count Number of data blocks input to CCFDTFDB. 
43 4 Binary Record Count Number of data records. 
47 ??? Character Filler [[DTC]] use only. [[DO]] not use. 
2.2 The CF2 Header and Trailer Records 
The CF2 Header and Trailer records come in two different formats; NDM and FTP.  
Note 
The Header and Trailer records are identical except for the first and last field of each record. 
2.2.1 NDM – CF2 Header and Trailer Records 
NDM users executing NDMDTF02 or NDMDTFGH will receive the following:  
Position Length Format  Field Name Field Description 
1 3 Character Record [[ID]] "HDR" or "TRL" 
4 4 Character Signon [[ID]] Signon [[ID]] 
8 6 Character Data Type 
Requested 
Value "PARTPO". 
[[DTCC]] Public (White)

---

## Page 6

 
2. Header and Trailer Records 6 
 
14 6 Character Data Type 
Created 
Value "PARTPO". 
20 8 Character Creation 
Date 
Data Creation Date (MM/DD/YY) 
28 8 Character Spool Date Data Load Date (MM/DD/YY) 
36 8 Character Load Time Data Load Time (HH:MM:SS) 
44 4 Numeric Record 
Length 
Record Length of data requested 
48 8 Numeric Record Count Number of data records in file. 
56 4 Numeric 80-Byte 
Record Count 
Number of 80-byte records per data type 
requested. (0001) 
60 ??? Character Filler [[DTC]] use only. [[DO]] not use. 
 
2.2.2 FTP - CF2 Header and Trailer Records 
FTP users will get the following: 
Position
  
Length  Format  Field Name  Field Description 
12 6 Character Data Type 
Requested 
Value "PARTPO". 
18 6 Character Data Type 
Created 
Value "PARTPO". 
24 8 Character Creation 
Date 
Data Creation Date (MM/DD/YY) 
32 8 Character Spool Date Data Load Date (MM/DD/YY) 
40 8 Character Load Time Data Load Time (HH:MM:SS) 
48 4 Numeric Record 
Length 
Record Length of data requested 
52 8 Numeric Record Count Number of data records in file. 
60 4 Numeric 80-Byte 
Record Count 
Number of 80-byte records per data type 
requested. (000 1) 
64 ??? Character Filler [[DTC]] use only. [[DO]] not use. 
 
[[DTCC]] Public (White)

---

## Page 7

 
3. Transaction Detail Records 7 
 
3. TRANSACTION DETAIL RECORDS 
The remaining records on the file are PARTPO transaction detail records. The two types of data records are 
SPO Transactions and PPO Transactions. Formats for these record types follow in respective order.    
3.1 SPO Transaction Detail Record 
The SPO Transaction Detail record contains detailed information regarding each Security Payment Order 
transaction. The following is a description of the detail records for Security Payment Orders. 
Position Length  Format  Field Name  Field Description 
1 1 Character Payee/Payor 
Code 
Indicates whether the recipient of this SPO 
transaction detail record is the Payee or Payor 
[[participant]]: 
1 = Payee [[participant]] is the recipient; 
2 = Payor [[participant]] is the recipient. 
2 1 Character Filler [[DTC]] use only. Must be initialized to spaces. 
3 4 Character Payee [[participant]] 
Number 
The [[DTC]] identification number of the originating 
[[participant]] (right justified, left zero filled). 
7 3 Character Filler [[DTC]] use only. Must be initialized to spaces. 
10 9 Character [[CUSIP]] Number The unique nine character identification number 
assigned to the security being traded. 
19 1 Character Filler [[DTC]] use only. Must be initialized to space. 
20 4 Character Payor [[participant]] 
Number 
The [[DTC]] identification number of the payor 
[[participant]] (right justified, left zero filled). 
24 5 Character Filler [[DTC]] use only. Must be initialized to spaces. 
29 7 Numeric Filler [[DTC]] use only. Must be initialized to zeroes. 
36 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
38 12 Numeric Dollar Amount Format PIC S9(10) V9(2). The amount of money 
involved in this SPO transaction. 
50 2 Character Reason Code The [[DTC]] defined reason (for payment) code. Valid 
SPO reason codes are: 
S0 = SPO Mark to Market; 
S1 = SPO Mark to Market Reclaim; 
S2 = SPO Due Bill Redemptions; 
S3 = SPO Due Bill Redemptions Reclaim; 
S4 = SPO Mark to Market/Fail; 
S5 = SPO Mark to Market/Fail Reclaim; 
S6 = SPO Buy in/[[pair off]]; 
[[DTCC]] Public (White)

---

## Page 8

 
3. Transaction Detail Records 8 
 
S7 = SPO Buy in/[[pair off]] Reclaim; 
S8 = SPO Fail [[pair off]]; 
S9 = SPO Fail [[pair off]] Reclaim. 
 
52 2 Numeric Activity Code The [[DTC]] generated code "78" identifying an SPO 
activity. 
54 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
56 7 Numeric New Price Format PIC S9(5) V9(2). The new price per share 
(after the price change). 
63 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
65 10 Numeric Adjustments Format PIC S9(8) V9(2). Any adjustments to the 
Amount field. 
75 6 Character Contract Date The date of the contract (MMDDYY). 
81 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
83 7 Numeric Old Price Format PIC S9(5) V9(2). The original price per share. 
90 30 Character Security 
Description 
[[DTC]]'s description for the security being traded. 
120 9 Numeric Share Quantity The number of [[shares]] involved in the [[Stock]] Loan 
transaction, in units of 1. 
129 21 Character Filler [[DTC]] use only. Must be initialized to spaces. 
150 60 Character Comments Additional comments describing this SPO transaction.  
If this is a reclaim this field may contain the reason for 
reclaim.  It may also contain third party information. 
210 1 Character [[settlement]] Code S = S ame Day Funds [[settlement]] 
211 30 Character Filler [[DTC]] use only. Must be initialized to spaces. 
 
3.2 [[SFT]] PD Payment Order Transaction Detail Record 
The [[SFT]] PD Payment Order contains detailed information regarding each [[SFT]] Price Differential Payment 
Order transaction for [[SFT]] [[Stock]] Loans. [[SFT]] PD (Price Differential) Payment Orders are a type of SPO. 
 
Position Length  Format  Field Name  Field Description 
1 1 Character Payee/Payor 
Code 
Indicates whether the recipient of [[SFT]] PD Payment 
Order detail record is the Payee or Payor [[participant]]: 
1 = Payee [[participant]] is the recipient; 
2 = Payor [[participant]] is the recipient. 
[[DTCC]] Public (White)

---

## Page 9

 
3. Transaction Detail Records 9 
 
Position Length  Format  Field Name  Field Description 
2 1 Character Filler [[DTC]] use only. Must be initialized to spaces. 
3 4 Character Payee [[participant]] 
Number 
The [[DTC]] identification number of the originating 
[[participant]] (right justified, left zero filled). 
7 3 Character Filler [[DTC]] use only. Must be initialized to spaces. 
10 9 Character [[CUSIP]] Number The unique nine character identification number 
assigned to the security being traded. 
19 1 Character Filler [[DTC]] use only. Must be initialized to space. 
20 4 Character Payor [[participant]] 
Number 
The [[DTC]] identification number of the payor 
[[participant]] (right justified, left zero filled). 
24 5 Character Filler [[DTC]] use only. Must be initialized to spaces. 
29 7 Numeric Filler [[DTC]] use only. Must be initialized to zeroes. 
36 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
38 12 Numeric Dollar Amount Format PIC S9(10) V9(2). The amount of money 
involved in this SPO transaction. 
50 2 Character Reason Code The [[DTC]] defined reason (for payment) code.  
SE =  [[SFT]] PD Payment Order 
 
52 2 Numeric Activity Code The [[DTC]] generated code "78-05" identifying an [[SFT]] 
PD (Price Differential) Payment Order activity. 
 
54 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
56 7 Numeric New Price Format PIC S9(5) V9(2). The new price per share 
(after the price change). 
63 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
65 10 Numeric Adjustments Format PIC S9(8) V9(2). Any adjustments to the 
Amount field. 
75 6 Character Contract Date The date of the contract (MMDDYY).  
81 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
83 7 Numeric Old Price Format PIC S9(5) V9(2). The original price per share. 
90 30 Character Security 
Description 
[[DTC]]'s description for the security being traded. 
120 9 Numeric Share Quantity The number of [[shares]] involved in the [[Stock]] Loan 
transaction, in units of 1. 
129 21 Character Filler [[DTC]] use only. Must be initialized to spaces. 
[[DTCC]] Public (White)

---

## Page 10

 
3. Transaction Detail Records 10 
 
Position Length  Format  Field Name  Field Description 
150 60 Character Comments Additional comments describing this SPO transaction.  
If this is a reclaim this field may contain the reason for 
reclaim.  It may also contain third party information. 
210 1 Character [[settlement]] Code S = S ame Day Funds [[settlement]] 
211 30 Character Filler [[DTC]] use only. Must be initialized to spaces. 
 
3.3 PPO Transaction Detail Record 
The PPO Transaction Detail record contains detailed information regarding a [[Premium]] Payment Order 
transaction. The following is a description of the detail records for [[Premium]] Payment orders.  
Note 
For the Options Symbology Initiative (OSI), see positions 214 through 239.  
Position Length  Format  Field Name  Field Description 
1 1 Character Payee/Payor 
Code 
Indicates whether the recipient of this PPO 
transaction 1 record is the Payee or Payor [[participant]]: 
1 = Payee [[participant]] is the recipient 
2 = Payor [[participant]] is the recipient 
2 1 Character Filler [[DTC]] use only. Must be initialized to space. 
3 4 Character Payee [[participant]] 
Number 
The [[DTC]] identification number of the originating 
[[participant]] 
(right justified, left zero filled). 
7 13 Character Filler [[DTC]] use only. Must be initialized to spaces. 
20 4 Character Payor [[participant]] 
Number 
The [[DTC]] identification number of the payor 
[[participant]] (right justified, left zero filled). 
24 5 Character Filler [[DTC]] use only. Must be initialized to spaces. 
29 5 Numeric Number of 
Contracts 
The number of [[Option]] contracts involved in this 
transaction. 
34 1 Character Receipt 
/Release 
1 = Receipt; 
2 = Release. 
35 1 Character Put/Call 1 = Pu t; 
2 = C all. 
36 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
38 12 Numeric Dollar Amount Format PIC S9(10) V9(2). The amount of money 
involved in this PPO transaction. 
[[DTCC]] Public (White)

---

## Page 11

 
3. Transaction Detail Records 11 
 
50 2 Character Reason Code The [[DTC]]-defined reason (for payment) code.  Valid 
PPO 
reason codes are: 
PO  = PPO Options [[Premium]] Payment - Put; 
P1 = PPO Options [[Premium]] - Put Reclaim; 
P2 = PPO Options [[Premium]] Payment - Call; 
P3 = PPO Options [[Premium]] - Call Reclaim. 
52 2 Numeric Activity Code The [[DTC]] generated code "82" identifying a PPO 
activity. 
54 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
56 7 Numeric Filler [[DTC]] use only. Must be initialized to Zeros. 
63 1 Character Open/Close Code 0 = PPO Opening Writing; 
1 = PPO C losing Purchase. 
64 2 Character Filler [[DTC]] use only. Must be initialized to spaces. 
66 2 Character Cross Reference 
Line Number 
The cross-reference line number as it relates to the 
Depository 
Release or Receipt of Deposit on the OCC form. 
68 7 Character Filler [[DTC]] use only. Must be initialized to spaces. 
75 6 Character Cross Reference 
Date 
The cross-reference date (MMDDYY). 
81 9 Character Bearing Serial 
Number 
The bearing serial number as it relates to the 
Depository 
Release or Receipt of Deposit on the OCC form. 
90 30 Character Bank Customer 
Name and 
Account Number 
This field will not be blank if the payee is an OCC. 
120 30 Character Options Clearing 
Corp 
OCC [[Member]] Name and Account Number. This field 
will not be blank if the payee is a bank. 
150 60 Character Comments Additional comments describing this PPO transaction.  
If this is a reclaim this field may contain the reason for 
reclaim. It may also contain third party information. 
210 1 Character [[settlement]] Code S = S ame Day Funds [[settlement]] 
211 3 Character Filler Reserved for [[DTC]] future use. 
214 6 Character [[Option]] Symbol 
Extended 
The extended symbol for the [[Option]] (previously called 
“Trading Symbol”) 
Note:  This field was extended, as a result of the 
Options Symbology Initiative (OSI). 
220 8 Character Expiration Date 
Extended 
Extended expiration date (CCYYMMDD) for the 
[[Option]]. 
[[DTCC]] Public (White)

---

## Page 12

 
3. Transaction Detail Records 12 
 
Note:  This field was extended, as a result of the 
Options Symbology Initiative (OSI).    
 
228 12 Numeric Exercise Price 
Extended 
Format PIC S9(6)V9(6).  The extended price at which 
the [[Option]] can be exercised.   
Note:  This field was extended, as a result of the 
Options Initiative (OSI).    
240 1 Character Filler  Reserved for future use. Initialized to spaces. 
 
[[DTCC]] Public (White)

---

## Page 13

 
3. Transaction Detail Records 13 
 
4. RELEASE NOTES 
This is the document history reflecting changes to the file. 
06/02/2022 The following changes were made to bring this document up to current standards: 
• As a result of the [[SFT]] Clearing initiative, added section 3.3 for [[SFT]] PD (Price Differential) 
Payment Orders.  
• Made general updates to remove outdated references and reformat the document.  
• Updated the document to follow up on release note 03/31/09. “After February 12, 2010, old 
fields (Trading Symbol, Expiration Date and Exercise Price) will not be populated any 
more.” They are now treated as filler. Position 10, Trading Symbol, and position 15, 
Expiration Date, are populated on output with spaces. Position 56, Exercise Price, is 
populated on output with zeros. 
 
07/14/14 The following changes were made to bring the existing document up to current 
standards. 
Added [[CCF]] Header Record description. 
Revised CF2 Header and Trailer Records 
Changed [[CCF]]-II references to read CF2. 
Identified existing CF2 HDR and TRL Record Format as NDM specific. 
Corrected “TLR” in Field Description (position 1) to read “TRL”. 
Added (0001) to Field Description (position 56). 
Expanded Filler (position 60) from 15 to ??? 
Removed Sequence Number field (position 75). 
Added FTP specific CF2 Header and Trailer Record Format. 
03/31/09 As a result of the Options Symbology Initiative (OSI), new fields are added to PPO record 
starting position 211 through 239 (pages 6-9). After February 12, 2010, old fields (Trading 
Symbol, Expiration Date and Exercise Price) will not be populated any more. 
 
 
 
 
 
 
[[DTCC]] Public (White)

---

## Page 14

3. Transaction Deail Records 14 
FOR MORE INFORMATION 
E
mail [[DTCC]] at: 
DTCSupport@[[DTCC]].com 
or visit us on the web at: 
http://www.[[DTCC]].com/client-center 
[[DTCC]] Public (White)