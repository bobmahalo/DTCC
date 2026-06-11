---
title: "Settlement Participant Activity (DTFPART): Function User’s Guide (5.11) "
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/DTFPART_05_11.pdf"
pages: 34
size: "2443.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Settlement Participant Activity (DTFPART): Function User’s Guide (5.11) 

**Original File:** [DTFPART_05_11.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/DTFPART_05_11.pdf)  
**Category:** Other  
**Total Pages:** 34  
**File Size:** 2443.7 KB  

---

## Page 1

 
 
 
 
CF2/MQ TRANSMISSION GUIDES 
5.11 [[settlement]] [[participant]] ACTIVITY (DTFPART): FUNCTION USER’S 
GUIDE 
JUNE 2, 2022 
 
[[DTCC]] Public (White)

---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
 
Doc Date: June 2, 2022 
Publication Code: SET 155 
Service: [[settlement]]/CF2/MQ Transmission Guides 
Title: 5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
 
[[DTCC]] Public (White)

---

## Page 3

 
 
TABLE OF CONTENTS 
1. The DTFPART Functions ................................................................................................................................. 4 
1.1 Availability of DTFPART ............................................................................................................................... 4 
2. Header and Trailer Records ............................................................................................................................ 5 
2.1 The [[CCF]] Header Record .............................................................................................................................. 5 
2.2 The CF2 Header and Trailer Records .......................................................................................................... 5 
2.2.1 NDM – CF2 Header and Trailer Records ................................................................................................. 5 
2.2.2 FTP-CF2 Header and Trailer Records ..................................................................................................... 6 
3. DTFPART Data Record .................................................................................................................................... 7 
4. Appendices ..................................................................................................................................................... 21 
4.1 Withdrawal-By-Transfer Code Descriptions ...............................................................................................21 
4.1.1 Auto-WT Edit Error Codes (position 241-266) .......................................................................................21 
4.1.2 WT Adjustment/Drop/Pend Codes (position 267-269) ...........................................................................22 
4.2 MMI [[CUSIP]] Descriptor Format ...................................................................................................................23 
4.3 Valid Reason Codes ...................................................................................................................................24 
Release Notes ..................................................................................................................................................... 32 
 
[[DTCC]] Public (White)

---

## Page 4

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
1. The DTFPART Functions 4 
1. THE DTFPART FUNCTIONS 
A CF2 User may use the DTFPART functions in order to receive [[DTCC]]'s [[participant]] Account Return 
Transactions information. When using the DTFPART functions, the CF2 User will receive a series of machine-
readable records. Each record corresponds to a data transaction that has updated a [[participant]]'s Account 
Balance. 
The DTFPART functions consist of the following seven data types available for return transmission, at various 
times of the business day, to the User: 
• DTFPDQ-Transactions that "processed" at the end of the PDQ system. 
• DTFMTM-Transactions that "processed" by morning in the ATP (Account Transaction Processor) system.  
• DTFMTH-Transactions that "processed" by mid-morning in the ATP system. 
• DTFMTI-Transactions that "processed" by midday in the ATP system. 
• DTFMTD-Transactions that "processed" by early afternoon in the ATP system. 
• DTFMTA-Transactions that "processed" by afternoon in the ATP system. 
• DTFMTE-Transactions that "processed" or "dropped" by end of day in the ATP system.  
Note: 
All of the above "processed" data types returned by the DTFPART functions contain data that is mutually exclusive. 
The information received through use of the DTFPART functions may be used to automate the updating of a 
User's files and the verification of the daily transaction processing sent by the User to [[DTCC]].  
1.1 Availability of DTFPART 
DTFPART will generally be available as follows: 
• DTFPDQ-from 2:00 a.m. to 4:00 p.m. 
• DTFMTM-from 10:30 a.m. to 6:15 a.m. (next day) 
• DTFMTH-from 12:05 p.m. to 8:05 a.m. (next day) 
• DTFMTI-from 1:30 p.m. to 9:30 a.m. (next day); 
• DTFMTD-from 2:30 p.m. to 10:30 a.m. (next day); 
• DTFMTA-from 4:15 p.m. to 12 p.m. (next day); and 
• DTFMTE-from 7:30 p.m. to 3:30 p.m. (next day). 
[[DTCC]] Public (White)

---

## Page 5

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
2. Header and Trailer Records 5 
2. HEADER AND TRAILER RECORDS 
2.1 The [[CCF]] Header Record 
NDM users executing NDMDTF01, NDMDTFGP, or NDMDTFSP will receive the following CF2 Header record.  
The CF2 header record's format is as follows: 
CF2 Header Record Format 
Position Length Format Field Name Field Description 
1 6 Character Data Type 
Requested 
DTFPDQ, DTFMTM, DTFMTH, DTFMTI, DTFMTD, DTFMTA, 
DTFMTE 
7 6 Character Data Type Created DTFPDQ, DTFMTM, DTFMTH, DTFMTI, DTFMTD, DTFMTA, 
DTFMTE 
13 8 Character Creation Date Date of data (MM/DD/YY). 
21 8 Character Spool Date [[DTC]] data load date (MM/DD/YY). 
29 8 Character Load Time [[DTC]] data load time (HH:MM:SS). 
37 2 Binary Record Size Size of each data record. 
39 4 Binary Block Count Number of data blocks input to CCFDTFDB. 
43 4 Binary Record Count Number of data records. 
47 ??? Character Filler [[DTC]] use only. [[DO]] not use. 
2.2 The CF2 Header and Trailer Records 
The CF2 Header and Trailer records come in two different formats; NDM and FTP.  
Note: 
The Header and Trailer records are identical except for the first and last field of each record. 
2.2.1 NDM – CF2 Header and Trailer Records 
NDM users executing NDMDTF02 or NDMDTFGH will receive the following:  
CF2 Header and Trailer Record Format-NDM 
Position Length Format Field Name Field Description 
1 3 Character Record [[ID]] "HDR" or "TRL" 
4 4 Character Signon [[ID]] Signon [[ID]] 
[[DTCC]] Public (White)

---

## Page 6

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
2. Header and Trailer Records 6 
CF2 Header and Trailer Record Format-NDM 
Position Length Format Field Name Field Description 
8 6 Character Data Type 
Requested 
DTFPDQ, DTFMTM, DTFMTH, DTFMTI, DTFMTD, 
DTFMTA, DTFMTE 
14 6 Character Data Type 
Created 
DTFPDQ, DTFMTM, DTFMTH, DTFMTI, DTFMTD, 
DTFMTA, DTFMTE 
20 8 Character Creation Date Data Creation Date (MM/DD/YY) 
28 8 Character Spool Date Data Load Date (MM/DD/YY) 
36 8 Character Load Time Data Load Time (HH:MM:SS) 
44 4 Numeric Record Length Record Length of data requested 
48 8 Numeric Record Count Number of data records in file. 
56 4 Numeric 80-Byte Record 
Count 
Number of 80-byte records per data type requested. 
(0001) 
60 ??? Character Filler [[DTC]] use only. [[DO]] not use. 
2.2.2 FTP-CF2 Header and Trailer Records 
FTP users will get the following: 
CF2 Header and Trailer Record Format-FTP 
Position Length Format Field Name Field Description 
1 3 Character Record [[ID]] "HDR" or "TRL" 
4 8 Character Sign-on [[ID]] Sign-on [[ID]] 
12 6 Character Data Type 
Requested 
DTFPDQ, DTFMTM, DTFMTH, DTFMTI, DTFMTD, 
DTFMTA, DTFMTE 
18 6 Character Data Type 
Created 
DTFPDQ, DTFMTM, DTFMTH, DTFMTI, DTFMTD, 
DTFMTA, DTFMTE 
24 8 Character Creation Date Data Creation Date (MM/DD/YY) 
32 8 Character Spool Date Data Load Date (MM/DD/YY) 
40 8 Character Load Time Data Load Time (HH:MM:SS) 
48 4 Numeric Record Length Record Length of data requested 
52 8 Numeric Record Count Number of data records in file. 
60 4 Numeric 80-Byte Record 
Count 
Number of 80-byte records per data type requested. 
(0001) 
64 ??? Character Filler [[DTC]] use only. [[DO]] not use. 
[[DTCC]] Public (White)

---

## Page 7

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 7 
3. DTFPART DATA RECORD 
The remaining records on the file will be DTFPART data records. The format of DTFPART data records is 
described below. 
Position Length Format Field Name Field Description 
1 1 Character Data Type 
Requested 
"A" = DTFPDQ 
"C" = DTFMTM 
"D" = DTFMTA 
"F" = DTFMTE 
"G" = DTFMTD 
"H" = DTFMTH 
"I" = DTFMTI 
"K" = DTFPDQ-DTFMTE 
2 1 Character System 
Origination 
Code 
"1" = API Tape System 
"2" = CF2 System 
"3" = [[PTS]] 
"4" = [[ID]] System 
"5" = Auto W/T System 
"6" = STS System 
"7" = Depository Interface System 
"8" = CF2 System 
"9" = Mainframe Dual Host System 
"A" = Reserved for Future Use 
"B" = Reserved for Future Use 
"C" = RDP System 
"D" = [[settlement]] System 
"E" = CP Issuances System 
"F" = CP Turnaround [[DO]] System 
"G" = RAD (cancelled or unapproved) 
"0" = Batch input ([[default]]) 
3 1 Character Status Code "M" = Made Transaction 
"E" = Edit Error Input 
"D" = Drop 
"P" = Pend 
"R" = Conditional Reject 
"C" = Cancelled 
"U" = Unapproved (RAD only) 
“T” = Dropped in the staging area 
“W” = Dropped from Optimizer  
[[DTCC]] Public (White)

---

## Page 8

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 8 
Position Length Format Field Name Field Description 
4 2 Character Version Control 
Number 
Value = "02". 
6 4 Character Transaction 
Originating 
Source 
For reference only. 
10 12 Character Account 
Number 
[[IPO]] Customer Internal Account Number. 
22 1 Character [[settlement]] 
Code 
"S" = Same Day Funds [[settlement]] 
23 4 Character [[participant]] 
Number 
The number of the [[DTC]] [[participant]] requesting the 
transmission. 
27 3 Character Filler [[DTC]] use only. [[DO]] not use. 
30 9 Character [[CUSIP]] Number [[CUSIP]] number. 
39 4 Packed Serial Number Serial number for investment identification activity. 
43 2 Character Filler [[DTC]] use only. [[DO]] not use. 
45 1 Character [[CNS]] Sub-
Account Type 
" " = Non-[[CNS]] item 
"A" = Trading Account 
"C" = [[Stock]] Loan Acct. 
"E" = Fully Paid Account 
"G" = Reorg Account 
"H" = Reorg Account (used only for competing offers and 
election mergers.) 
“R” = [[CNS]] Longs 
46 3 Character Expanded 
Reason Code 
Reason Codes are applicable only for activity types 26, 
27, 47, 48 and 49. A list of valid reason codes appears in 
Appendix 4.3.  
49 4 Packed Loan Date YYMMDD format. 
[[DTCC]] Public (White)

---

## Page 9

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 9 
Position Length Format Field Name Field Description 
53 2 Packed Account Type "10" = General Unpledged 
"14" = General Pledged 
"18" = General Investment 
"22" = General Investment/Seg 
"26" = Called Security without Accrued Interest 
"28" = Called Security with Accrued Interest 
"40" = Withdrawal By Transfer 
Note: 
1. Expanded Account Type, in position 420 contains 
more detailed information. 
2. HIGH VALUES in this field indicates that there is NO 
TRANSLATED ACCOUNT TYPE. Refer to position 
420 for the Expanded Account Type. 
55 1 Packed Action Code "0" = No Update (i.e.: recycle). 
"1" = Add to Account. 
"2" = Subtract from Account. 
56 2 Packed Transaction 
Type 
"07" = [[participant]] Swing 
"08" = Security Swing 
"17" = Pledge to [[DTC]] 
"18" = [[syndicate]] [[DO]] 
"20" = Certificate on Demand 
"26" = Deliver Order 
"27" = Receive Balance Order 
"30" = Deposit 
"31" = [[Stock]] Split 
"32" = [[Stock]] [[Dividend]] 
"33" = Reorg Deposit 
"34" = Investment [[ID]] 
"41" = Pend Canceled Multicurrency Segregation 
"44" = Investment Reversal 
"51" = Pledge 
"56" = Release 
"80" = W/T [[participant]] Account 
"81" = Long [[participant]] W/T Account 
"82" = Deliver to [[participant]] 
"93" = [[Dividend]] Distributions (Spin-Offs) 
"95" = Reorganization Distributions 
"97" = Reorganization Redemptions 
[[DTCC]] Public (White)

---

## Page 10

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 10 
Position Length Format Field Name Field Description 
"110" = Call Lottery 
"120" = Call Lottery (with accrued interest) 
Note: 
1. Expanded Transaction Type, in position 417 contains 
more detailed information. 
2. HIGH VALUES in this field indicates there is NO 
TRANSLATED TRANSACTION TYPE. Refer to 
position 417 for the Expanded Transaction Type. 
58 1 Character Municipal 
Dealer 
Comparison 
Trade 
"M" = Municipal 
Blank = Other 
59 4 Character Contra 
[[participant]] 
Number 
[[DO]]'s only. 
63 3 Character Security Sub-
Issue Type 
"000" = [[default]]. No sub-issue type. 
"120" = Preferred Commercial Paper (CP) 
"220" = Muni VRDO/CP 
"330" = Muni CP 
"502" = Bankers' Acceptance (BA) 
"504" = Institutional Certificate of Deposit (CD) 
"510" = Interest at Maturity (IAM) CP 
"520" = Discount CP 
"525" = Corporate CP 
"526" = Corporate VRDO/CP 
"530" = Medium Term note (MTN) 
"531" = Deposit note 
"532" = Medium Term Bank note 
"540" = Collateralized Mortgage Obligation (CMO) 
"541" = [[Asset]] Backed Security 
"550" = Short Term Bank note 
"560" = Discount note 
66 3 Character Filler [[DTC]] use only. [[DO]] not use. 
69 4 Packed Trade Date Trade Date (MMDDYY format). For transaction types 34, 
35 and 44, the actual date or constant "71111" will appear. 
All other transaction types will contain a date or be zero-
filled. 
73 6 Character Filler [[DTC]] use only. [[DO]] not use. 
79 2 Packed Cents Amount Cents amount for valued transactions. 
[[DTCC]] Public (White)

---

## Page 11

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 11 
Position Length Format Field Name Field Description 
81 6 Packed Dollar Amount Dollars amount for valued transactions. 
87 1 Packed Journal Code "0" = Original transaction 
"1" = Journal adjustment 
88 7 Character Filler [[DTC]] use only. [[DO]] not use. 
95 4 Character Contra-
[[participant]] 
Contra-[[participant]] for CM Swing activity. If Transaction 
Type is "07", this field contains the Contra [[participant]] 
number. 
99 2 Character Filler [[DTC]] use only. [[DO]] not use. 
101 12 Character Account 
Number 
[[Institutional Delivery]] System agent internal account 
number ([[ID]] Trades only). 
113 17 Character Account 
Number 
Deliverer's account number. 
130 17 Character Account 
Number 
Receiver's account number. 
147 17 Character Account 
Number 
Subordinate bank account number. 
164 6 Character [[settlement]] 
Date 
MMDDYY format. 
170 6 Packed Control 
Number 
[[Institutional Delivery]] System control number ([[ID]] [[DO]]'s 
only). 
This field will be populated with one of the following values 
for [[ID]] [[DO]]’s: 
The Institutional Control Number for trades confirmed at 
[[DTCC]]’s Institutional Trade Processing (ITP) service. 
A value of 1 for Institutional Deliveries for trades confirmed 
at either BSTP or SS&C instead of the actual 
alphanumeric [[ID]] Control Number (refer to Expanded 
Control Number position 569) 
If the transaction is not an [[ID]] [[DO]], this field is set to 
zeroes. 
176 9 Character Contra [[CUSIP]]  Contra-[[CUSIP]] for Security Swing activity. If transaction 
Type is "08", this field contains the "swung from" [[CUSIP]] 
number. 
185 1 Character Fractional 
[[shares]] 
Indicator 
Space = Non-Fractional Share [[CUSIP]]. 
"F" = Fractional Share [[CUSIP]]. 
186 6 Character As of Date MMDDYY format. 
192 5 Packed ATP Record 
Address 
ATP Transaction Record Address. 
197 1 Character Filler [[DTC]] use only. [[DO]] not use. 
[[DTCC]] Public (White)

---

## Page 12

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 12 
Position Length Format Field Name Field Description 
198 1 Character PTA Indicator Pending Transaction Account Indicator 
Y = Pending 
Space = Not Pending 
199 1 Character Due Bill 
Indicator 
[[DO]] Due Bill Indicator: 
"Y" = Due Bills Carried 
"N" = No Due Bills 
Blank = Non-[[DO]] activity. 
200 1 Character Filler [[DTC]] use only. [[DO]] not use. 
201 210 Character Remarks Remarks. Content depends on transaction type. Positional 
breakdown is: 
Deliver Orders: 
201-410 = Optional remarks. 
 
[[custody]] Activity 
201-204 = [[custody]] Identifier “CTDY” 
205-220 = Reference [[ID]] 
221-240 = Customer Number 
241-245 = From Location 
246-250 = To Location 
251-258 = Issue Date 
 
STS System Withdrawal-By-Transfer Items: 
201-215 = [[Broker]] Reference information received by 
[[DTCC]]. 
216-410 = Remainder of free form comments. 
 
AUTO W/T System Withdrawals-by-Transfer: 
201-240 = [[Broker]] Reference Information received by 
[[DTCC]]. 
241-266 = Auto-WT Reject Code(s), ONLY for WTs with 
Status Code "E" (Refer to appendix 4.1.1). 
267-269 = WT Adjustment/Drop/Pend Code (Refer to 
appendix 4.1.2). 
270-410 = Filler blanks. 
 
RDS Activity 
201-204 =RDS Identifier ‘RDSI’ 
205-244 = Reference [[ID]] 
245-258 = Total Quantity for Deposit 
259 = Restricted Type  
[[DTCC]] Public (White)

---

## Page 13

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 13 
Position Length Format Field Name Field Description 
 
RDS Activity Clearing Transfer 
201-244 = RDS Identifier ‘RDSI’ 
205-244 = Reference [[ID]]  
 
Pledges and Releases: 
201-312 = Four, 28-byte fields of pledgee or pledgor 
comments. 
313-317 = Mainframe Dual Host (MQ) 5-character 
Sequence Number. 
318-410 = Filler blanks. 
 
Reorg Segregation Activity: 
201-206 = Reorg Seg Sub-Account [[ID]]. 
Format is XYYYZZ, where: 
X = Reorg Activity Code 
YYY = RAMS Activity Code 
ZZ = RAMS Sequence Number. 
207-209 = Reorg Seg Sub-Activity Code. 
210-280 = Filler blanks. 
281-296 = Control [[ID]] (when available) 
297-410 = Filler blanks  
 
[[Direct Registration]] [[DO]] Activity 
1-13 = Transaction [[ID]] 
14-15 = Filler 
16-52 = [[participant]] Account Number 
53-54 = Filler 
55 = Reason Code 
56-57 = Filler 
58-67 = Process Date 
68-69 = Filler 
70 = Value "1" 
71-110 = [[participant]] or Correspondent Name 
111-112 = Filler 
113-123 = Social Security Number 
124-139 = Filler 
140 = Value "2" 
141-175 = [[DRS]] Registration 
176-209 = Filler 
210 = Value "3" 
[[DTCC]] Public (White)

---

## Page 14

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 14 
Position Length Format Field Name Field Description 
Note:  
For DOs related to [[SFT]], bytes 1-80 are used for remarks. 
These must be left justified  and followed by the exact 14-
digit UTC Loan [[ID]]. 
411 6 Character Third Party 
Number 
Used for third party deliveries. 
417 3 Character Expanded 
Transaction 
Type 
A more specific description of Transaction Type (position 
56). 
"007" = [[participant]] Swing 
"008" = [[CUSIP]] Swing 
"017" = Pledge to [[DTC]] 
"020" = Certificate on Demand 
"021" = Direct Withdrawal 
"022" = Withdrawal/Exit 
"025" = [[CNS]] Deliver Order ([[Stock]] Borrow) 
"026" = Deliver Order 
"027" = Receive Balance Order (Night Pends Only) 
"028" = Maturity Presentment 
"030" = Deposit 
"031" = [[Stock]] Split 
"032" = [[Stock]] [[Dividend]] 
"033" = Reorg Deposit 
"034" = Investment I.D. 
"035" = Deposit Segregation 
"036" = Segregations 
"037" = Direct Deposits 
"038" = CP Issuance Deposit 
"039" = [[IPO]] Deposit 
"040" = Multicurrency Segregation Deliver Order 
"041" = Multicurrency Segregation 
"044" = Investment Reversal 
"045" = Seg Release 
"046" = [[IPO]] Release 
"047" = [[IPO]] Delivery ([[IPO]] to [[IPO]] acct) 
"048" = [[IPO]] Delivery ([[IPO]] to Free acct) 
"049" = [[IPO]] Delivery (Free to [[IPO]] acct) 
"050" = [[IPO]] Pledge 
"051" = Pledge 
"052" = Valued [[IPO]] Pledge 
[[DTCC]] Public (White)

---

## Page 15

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 15 
Position Length Format Field Name Field Description 
"054" = Valued Pledge 
"055" = Valued Release 
"056" = Release 
"059" = Release of Matured CP 
"080" = W/T [[participant]] Account 
"081" = Long [[participant]] W/T Account 
"082" = Deliver from [[participant]] W/T Account 
"089" = Rush Transfer (WT) 
"093" = [[Dividend]] Distributions (Spin-Offs) 
"095" = Reorganization Distributions 
"097" = Reorganization Redemptions 
"110" = Call Lottery 
"120" = Call Lottery (with Accrued Interest) 
"122" = MMI Withdrawal 
"126" = Reorg Currency Submission 
"220" = Redemptions 
"226" = Reorg Currency Reversal 
"231" = Reorg Deposit [[settlement]] Exit 
"240" = Conversions 
"900" = Pend Canceled Multicurrency Segregation 
420 3 Character Expanded 
Account Type 
A more specific description of Account Type (position 53). 
"MS" = Matured (Sweep). 
"RRG" = Reorg Segregation account. 
"[[IPO]]" = [[IPO]] Tracked Account. 
423 20 Character [[CUSIP]] 
Descriptor 
[[CUSIP]] Descriptor for Money Market Instrument 
transactions (MMI). 
443 14 Character CMO Trade 
Factor 
Collateralized Mortgage Obligation Trade Factor value 
9(2) V9 (12). If not supplied as input by the [[participant]] the 
field will be zeroes for CMO [[DO]]'s only. For non-CMOs the 
field will contain blanks. 
457 13 Numeric Share Quantity Share Quantity (signed), expressed in units of 1. PIC S9 
(13). 
470 8 Character Bank Identifier [[IPO]] [[ID]] Agent Bank Identifier. 
478 8 Character Bank Number Pledgee Bank Number. 
486 12 Character Account 
Number 
[[IPO]] [[Broker]] Internal Account Number. 
498 12 Character Account 
Number 
[[IPO]] Correspondent Account Number. 
510 9 Packed Filler [[DO]] NOT USE OR REASSIGN THIS FIELD! 
[[DTCC]] Public (White)

---

## Page 16

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 16 
Position Length Format Field Name Field Description 
519 8 Numeric ATP Original 
Reference 
ATP Original Transaction Reference Number 
527 7 Numeric Expanded 
Serial Number 
Expanded Serial number for investment identification 
activity.  
Note: 
This is the expanded version of Serial Number in position 
39.  
534 8 Numeric Expanded 
Loan Date 
YYYYMMDD format 
Note: 
This is the expanded version of Loan Date in position 49. 
542 2 Character New Expanded 
Account Type 
"10" = General Unpledged 
"14" = General Pledged 
"18" = General Investment 
"22" = General Investment/Seg 
"26" = Called Security without Accrued Interest 
"28" = Called Security with Accrued Interest 
"40" = Withdrawal By Transfer 
Note: 
This is the expanded version of Account Type in position 
53. 
544 1 Character New Expanded 
Action Code 
"0" = No Update (i.e.: recycle). 
"1" = Add to Account. 
"2" = Subtract from Account. 
Note: 
This is the expanded version of Action Code in position 55. 
545 3 Character New Expanded 
Transaction 
Type 
"07" = [[participant]] Swing 
"08" = Security Swing 
"17" = Pledge to [[DTC]] 
"18" = [[syndicate]] [[DO]] 
"20" = Certificate on Demand 
"26" = Deliver Order 
"27" = Receive Balance Order 
"30" = Deposit 
"31" = [[Stock]] Split 
"32" = [[Stock]] [[Dividend]] 
[[DTCC]] Public (White)

---

## Page 17

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 17 
Position Length Format Field Name Field Description 
"33" = Reorg Deposit 
"34" = Investment [[ID]] 
"41" = Pend Canceled Multicurrency Segregation 
"44" = Investment Reversal 
"51" = Pledge 
"56" = Release 
"80" = W/T [[participant]] Account 
"81" = Long [[participant]] W/T Account 
"82" = Deliver to [[participant]] 
"93" = [[Dividend]] Distributions (Spin-Offs) 
"95" = Reorganization Distributions 
"97" = Reorganization Redemptions 
"110" = Call Lottery 
"120" = Call Lottery (with accrued interest)  
Note: 
1. Expanded Transaction Type, in position 417 contains 
more detailed information. 
2. HIGH VALUES in this field indicates there is NO 
TRANSLATED TRANSACTION TYPE. Refer to 
position 417 for the Expanded Transaction Type. 
3. This is the expanded version of Transaction Type in 
position 56. 
548 8 Numeric Expanded 
Trade Date 
Trade Date (MMDDYYYY format). For transaction types 
34, 35 and 44, the actual date or constant "71111" will 
appear. All other transaction types will contain a date or 
be zero-filled. 
Note: 
This is the expanded version of Trade Date in position 69.  
556 2 Numeric Expanded 
Cents Amount 
Cents amount for valued transactions. 
Note: 
This is the expanded version of Cents amount in position 
79.  
558 10 Numeric Expanded 
Dollar Amount 
Dollars amount for valued transactions. 
Note: 
This is the expanded version of Dollar Amount in position 
81. 
[[DTCC]] Public (White)

---

## Page 18

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 18 
Position Length Format Field Name Field Description 
568 1 Character Expanded 
Journal Code 
"0" = Original transaction 
"1" = Journal adjustment 
Note: 
This is the expanded version of Journal Code in position 
87. 
569 10 Character Expanded 
Control 
Number 
[[Institutional Delivery]] System control number ([[ID]] [[DO]]'s 
only). 
Will contain either a numeric or alpha-numeric [[ID]] Control 
Number, preceded by a zero. 
579 8 Numeric Expanded ATP 
Record 
Address 
ATP Transaction Record Address Number. 
Note: 
This is the expanded version of ATP Record Address in 
position 192. 
587 3 Character Batch Variable Batch Variable. 
590 3 Character Batch Constant Batch Constant. 
593 8 Character [[transfer agent]] 
# 
The [[transfer agent]] number for Activity Codes 021 and 
037. 
601 1 Character FOSP Indicator "0" = Security is not eligible for FOSP Processing 
"1" = Security is eligible for FOSP Processing 
Blank = Unavailable, call [[DTC]] 
602 9 Numeric ABA Bank Identifier Account for the FED [[participant]] required 
when the Deliverer or receiver is the FED Account (6072). 
611 20 Character Fed Sub 
Account 
Bank Sub Account for the FED [[participant]] required when 
the Deliverer or Receiver is the FED Account (6072). 
631 40 Character Fed Third Party 
Deliverer Text 
Third Party Deliverer Text and Account Information. 
671 40 Character Fed Third Party 
Receiver Text 
Third Party Receiver Text and Account Information. 
711 3 Character Filler  
714 2 Character OCC Clearing 
Group [[ID]] 
New Field 
716 5 Numeric OCC Clearing 
[[Member]] 
Number 
Replacing OCC 3rd. Party 
 
Required field 
5 digit numeric 
[[DTCC]] Public (White)

---

## Page 19

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 19 
Position Length Format Field Name Field Description 
721 2 Character OCC Account 
Type 
Replacing OCC Account Type 
 
OCC Required field 
List of values: 
‘C ’-Customer 
‘F ’-Firm 
‘M ’-[[Market Maker]] 
‘Z ’-Clearing Fund 
723 15 Character OCC Account 
[[ID]]  
New Field 
 
Optional 
(a.k.a. OCC Sub – Account [[ID]]) 
738 2 Character OCC [[collateral]] 
Type 
Replacing OCC Entry Type 
 
OCC Required field 
List of values: 
‘GE’ – GSE Debt 
‘GS’ – Government Security 
‘MM’ – Money Market Fund 
‘SD’ – Specific Deposit 
‘VS’ – Valued Security 
740 6 Character OCC [[Option]] 
Symbol 
Replacing OCC Trade Symbol 
 
OCC required field for [[collateral]] Type of “Specific 
Deposit” 
746 4 Numeric OCC [[Option]] 
Expiration Year 
Replacing OCC Expiration Year 
 
OCC required field for [[collateral]] Type of “Specific 
Deposit” 
750 2 Numeric OCC [[Option]] 
Expiration 
Month 
Replacing OCC Expiration Month 
 
OCC required field for [[collateral]] Type of “Specific 
Deposit” 
752 2 Numeric OCC [[Option]] 
Expiration Day 
New Field 
OCC required field for [[collateral]] Type of “Specific 
Deposit” 
[[DTCC]] Public (White)

---

## Page 20

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
3. DTFPART Data Record 20 
Position Length Format Field Name Field Description 
754 1 Character OCC [[Option]] 
Type 
Replacing OCC Put or Call Code 
OCC required field for [[collateral]] Type of “Specific 
Deposit” 
 
List of values: 
‘C’ – Call 
‘P’ – Put 
755 6 Numeric OCC [[Option]] 
Strike Price 
Replacing OCC Exercise Price. 
OCC required field for [[collateral]] Type of “Specific 
Deposit” 
6 digit numeric 
761 6 Numeric OCC [[Option]] 
Strike Price 
(Decimal) 
Replacing OCC Fraction 
OCC required field for [[collateral]] Type of “Specific 
Deposit” 
6 digit numeric 
767 20 Character OCC Cross 
Reference 
Replacing OCC Cross Reference  
Optional 
787 20 Character OCC Customer 
Account 
Replacing OCC Customer Account 
Optional 
807 1 Character OCC Old/New 
Format 
Indicator 
Indicates whether or not the OCC is receiving data using 
the new or old symbol formats. Values are “O” or “N” 
 
808 16 Character IMS 
Transaction [[ID]] 
IMS TID for all made [[DTC]] transactions; filled with blanks if 
not available or for non-made transactions. 
(Inventory Management Transaction Identifier (IMS TID) is 
a unique [[ID]] that stays with a transaction throughout its life 
regardless of a status change. The IMS TID is designed to 
replace the existing ATP Transaction Record Address or 
Record Block Number (RBN) that changes with each 
status.) 
824 14 Character Blank Not used, filled with spaces. 
[[DTCC]] Public (White)

---

## Page 21

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 21 
4. APPENDICES 
4.1 Withdrawal-By-Transfer Code Descriptions 
Descriptions for WT Edit Error Codes and Adjustment/Drop/Pend Codes follow. These codes may appear in 
the remarks section of DTFPART Withdrawal-by-Transfer records. 
4.1.1 Auto-WT Edit Error Codes (position 241-266) 
Code Description 
A Invalid transaction code. 
B Ineligible or chilled [[CUSIP]]. 
C Ineligible [[participant]] or SDFS [[participant]]. 
D Frozen [[participant]] number. 
E Non-numeric total quantity. 
F Total quantity is not equal to pieces time’s denominations. 
G Date not numeric. 
H Non-numeric sequence number. 
I Number of pieces or denomination not numeric. 
J Invalid TEFRA code. 
K Invalid type of taxpayer [[ID]] 
L Invalid taxpayer [[ID]]. 
M Ineligible Muni Bond type. 
N Invalid assignment type. 
O Invalid or illogical deletion date. 
P Tax waiver code not equal to "3". 
Q Record date item, pend or drop. 
R Sequence error. 
S Non-numeric sequence-deletion. 
T Bond quantity not multiple of 1000. 
U Assignment lines blank. 
V Invalid input mode-Government or Communication issue. 
W Invalid [[UIT]] code. 
X Invalid DMA code or ineligible DMA [[participant]]. 
[[DTCC]] Public (White)

---

## Page 22

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 22 
Code Description 
Y Invalid REINV [[CUSIP]] number. 
Z Invalid input mode or TA is not W/T eligible. 
4.1.2 WT Adjustment/Drop/Pend Codes (position 267-269) 
NEW TRANSACTIONS 
Code Description 
012 Pended. Insufficient [[participant]] position. 
013 Adjustment Pended. Insufficient [[DTC]] position. 
015 Pended. Record date item. 
016 Pended. Insufficient [[collateral]] on SDFS item. 
022 Dropped. Insufficient [[participant]] position. 
023 Adjustment Dropped. Insufficient [[DTC]] position. 
025 Dropped. Record date item. 
026 Dropped. Insufficient [[collateral]] on SDFS item. 
 
PREVIOUSLY PENDED TRANSACTIONS 
Code Description 
032 Pended. Insufficient [[participant]] position. 
033 Adjustment Pended. Insufficient [[DTC]] position. 
035 Pended. Record date item. 
036 Pended. Insufficient [[collateral]] on SDFS item. 
037 Dropped or deleted after one month in pending status. 
 
DELETION TRANSACTIONS 
Code Description 
045 Dropped. Delete transaction was accepted. 
046 Dropped. No matching pending transaction. 
[[DTCC]] Public (White)

---

## Page 23

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 23 
4.2 MMI [[CUSIP]] Descriptor Format 
Position Contents 
1 "4" denotes SDFS and MMI issue 
2-3 Issue Type: 
• CD = Institutional Certificate of Deposit (CD Program) 
• CV = Corporate Variable Rate [[DO]] CP (VRDO/CP) 
• MC = Municipal CP, Tax-Exempt (TECP Program) 
• MT = Municipal CP, Taxable (TECP Program) 
• MV = Municipal CP, VRDO/CP, Tax-Exempt 
• MX = Municipal CP, VRDO/CP, Taxable 
• BS = Bank note, Short Term (STBN Program) 
• DN = Discount note (DN Program) 
• PC = Preferred [[Stock]] in CP Mode (FD/CP Program) 
• BM = Bank note, Medium-Term (MTN Program) 
• CP = Corporate Commercial Paper (CP Program) 
• DP = Deposit note, Medium-Term (MTN Program) 
• MN = Medium-Term note, excluding Deposit/ 
4-7 [[issuer]] Acronym assigned by [[DTC]] 
8-11 Maturity Date in MDYY format. Maturity Month and Day are alphanumeric, Maturity Year is 
numeric. 
12-16 Income Rate 
• For issues paying a FIXED rate this field contains five numeric characters, with an implied 
decimal point after the second character. 
• For issues paying a VARIABLE income rate this field contains "*VAR*". 
• For paper issued at a DISCOUNT and Zero-Coupon issues this field contains "*DIS*". 
17-18 [[book-entry]] only ("BE") or Global ("GL") Program Indicator. 
19 Market Indicator 
For non-restricted (public) programs: 
• N = [[New York Stock Exchange]] ([[NYSE]])  
• @ = American [[Stock Exchange]] (AMEX) 
• + = Over The Counter ([[DTC]]) 
• X = Multiple Markets 
 
For [[SEC]] [[Rule 144A]] restricted ([[Private Placement]]) programs: 
• M = Multiple Markets 
• P = Portal ([[NASD]]) only 
• S = SITUS (AMEX) only 
• Y = System 144A ([[NYSE]]) only 
• A = Over the Counter only 
 
For 4(2) and other non-144A restricted programs: 
• R = Over the Counter 
[[DTCC]] Public (White)

---

## Page 24

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 24 
Position Contents 
20 Debt/[[Equity]] Income Structure Indicator 
For Debt issues: 
• + = Interest at Maturity Only 
• % = Periodic Interest Payments 
• $ = Discount or Zero Coupon 
 
For [[Equity]] issues (PFD/CP): 
• & = Interest at Maturity Only 
• @ = Periodic Interest Payments 
• 4 = Discount or Zero Coupon 
4.3 Valid Reason Codes 
The list of valid [[DO]] Reason Codes follows. Transactions marked by an asterisk ("*") are not accepted by [[DTCC]] outside 
"regular" Deliver Order processing hours. 
Code Description 
000 *Other 
001 Reclaim DK 
002 Reclaim wrong quantity 
003 Reclaim wrong security 
004 Reclaim wrong money 
005 Reclaim partial 
006 Reclaim need more a/c info 
007 Reclaim needs due bill 
008 Partial reclaim–partial return 
010 [[Stock]] loan 
011 [[Stock]] loan reclaim–DK 
012 [[Stock]] loan rec wrong qty 
013 [[Stock]] loan rec wrong security 
014 [[Stock]] loan rec wrong money 
015 [[Stock]] loan rec partial 
016 [[Stock]] loan rec needs a/c info 
017 [[Stock]] loan rec needs due bill 
018 [[Stock]] loan partial reclaim–partial return 
[[DTCC]] Public (White)

---

## Page 25

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 25 
Code Description 
019 *[[Stock]] loan recall 
020 [[Stock]] loan return 
021 [[Stock]] loan ret rec DK 
022 [[Stock]] loan ret rec wrong qty 
023 [[Stock]] loan ret rec wrong [[SEC]] 
024 [[Stock]] loan ret rec wrong money 
025 [[Stock]] loan ret rec partial 
026 [[Stock]] loan ret rec a/c info 
027 [[Stock]] loan ret rec need due bill 
028 [[Stock]] loan ret reclaim partial–rec partial return 
029 [[Stock]] loan recall reclamation 
030 *Delivery versus payment 
031 DVP reclaim DK 
032 DVP reclaim wrong quantity 
033 DVP reclaim wrong [[SEC]] 
034 DVP reclaim wrong money 
035 DVP reclaim partial 
036 DVP rec needs a/c info 
037 DVP reclaim needs due bill 
038 DVP partial reclaim–partial return 
039 *Trade–for–trade balance order 
040 *Transfer of customer account 
041 Trans cust a/c rec DK 
042 Trans cust a/c rec wrong qty 
043 Trans cust a/c rec wrong [[SEC]] 
044 Trans cust a/c rec wrong money 
045 Trans cust a/c rec partial 
046 Trans cust a/c rec a/c info 
047 Trans cust a/c rec due bill 
048 Trans cust a/c partial reclaim–partial return 
049 S/B "[[ID]] [[syndicate]] Trade" 
[[DTCC]] Public (White)

---

## Page 26

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 26 
Code Description 
050 New issue 
051 New issue reclaim DK 
052 New issue rec wrong qty 
053 New issue rec wrong [[SEC]] 
054 New issue rec wrong money 
055 New issue rec partial 
056 New issue rec needs a/c info 
057 New issue rec needs due bill 
058 New issue partial reclaim–partial return 
060 *Net balance order 
061 Net balance order rec DK 
062 Net balance order rec wrong qty 
063 Net balance order rec wrong [[SEC]] 
064 Net balance order rec wrong money 
065 Net balance order rec partial 
066 Net balance order rec a/c info 
067 Net balance order rec needs due bill 
068 Net balance order reclaim partial–rec partial return 
070 *Del vs pymt, use SPO for (D/B) 
071 *Fail to deliver 
072 Fail to deliver reclamation 
073 Delivery to [[CNS]] 
074 *SPO mark–to–market 
075 SPO mark–to–market reclaim 
076 [[Institutional Delivery]] reclaim 
077 *[[ID]]/NIDS 
078 Trade–for–trade freeze 
079 Frozen security reclamation 
080 Inventory/free movement 
081 Repo Tracking (SDFS Only – non Commercial Paper) 
082 Generated CPI Issuance Delivery 
[[DTCC]] Public (White)

---

## Page 27

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 27 
Code Description 
083 CP Early Maturity 
084 *PPO Options [[Premium]] 
085 PPO Options [[Premium]] Reclaim 
086 Municomparison Trade [[settlement]] 
087 *DVP–Due Bill, (D/B)/check spent 
088 ACATS – 412 – [[DO]] 
089 S/B "Night Secondary Offering" 
090 S/B "[[DTC]] Input – [[Underwriting]] Dept" 
091 [[DTC]] Correction 
092 Delivery on Warrant Exercise 
093 [[DTC]] set – [[PTS]] [[Stock]] Loan 
094 [[DTC]] set adj – Part [[PTS]] Problem 
095 ACATS Valued (Reduces MEMO SEG Position) 
096 [[DTC]] set adj-Reclaim Interface 
097 Delivery vs. Payment (Reduces MEMO SEG Position) 
098 Transfer of Account (Prevents MEMO SEG Position Reduction) 
099 Bulk Transfer of Account 
101 MMI Issuance [[DO]] Reclaim DK 
102 MMI Issuance [[DO]] Reclaim Wrong Quantity 
103 MMI Issuance [[DO]] Reclaim Wrong Security 
104 MMI Issuance [[DO]] Reclaim Wrong Money 
105 MMI Issuance [[DO]] Reclaim Partial 
106 MMI Issue [[DO]] Reclaim Need More A/C Info 
107 MMI Issuance [[DO]] Reclaim Needs Due Bill 
108 MMI Issuance [[DO]] Reclaim Rec Partial Ret 
109 MMI Issuance [[DO]] Wrong Rate 
110 MMI Issue [[DO]] Wrong Safekeeping A/C NBR 
111 MMI Issuance [[DO]] Wrong Maturity Date 
112 MMI Issuance [[DO]] Should Be Discounted 
113 MMI Issue [[DO]] Should Be Interest Bearing 
120 MMI [[DO]] Redelivery 
[[DTCC]] Public (White)

---

## Page 28

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 28 
Code Description 
121 MMI [[DO]] Reclaim DK 
122 MMI [[DO]] Reclaim Wrong Quantity 
123 MMI [[DO]] Reclaim Wrong Security 
124 MMI [[DO]] Reclaim Wrong Money 
125 MMI [[DO]] Reclaim Partial 
126 MMI [[DO]] Reclaim Need More A/C Info 
127 MMI [[DO]] Reclaim Needs Due Bill 
128 MMI [[DO]] Partial Rec Partial Ret 
129 MMI [[DO]] Wrong Rate 
130 MMI [[DO]] Wrong Safekeeping A/C Number 
131 MMI [[DO]] Wrong Maturity Date 
132 MMI [[DO]] Should Be Discounted 
133 MMI [[DO]] Should Be Interest Bearing 
134 MMI SECONDARY [[DO]]-BYPASS FUNDING DECISION 
135 MMI SECONDARY [[DO]] – RECLAIM BYPASS FUNDING DECISION 
200 [[SFT]] [[Stock]] Loan 
201 [[SFT]] [[Stock]] Loan Return 
280 [[ADR]] [[Stock]] Loan (untracked) 
281 [[ADR]] [[Stock]] Loan Reclaim DK 
282 [[ADR]] [[Stock]] Loan Reclaim Wrong Quantity 
283 [[ADR]] [[Stock]] Loan Reclaim Wrong Security 
284 [[ADR]] [[Stock]] Loan Reclaim Wrong Money 
285 [[ADR]] [[Stock]] Loan Reclaim Partial 
286 [[ADR]] [[Stock]] Loan Need More A/C Info 
287 [[ADR]] [[Stock]] Loan Needs Due Bill 
288 [[ADR]] [[Stock]] Loan Partial Rec Partial Ret 
290 [[ADR]] [[Stock]] Loan Return (untracked) 
291 [[ADR]] [[Stock]] Loan Return DK 
330 Direct Rollover To IRA 
331 Direct Rollover To IRA Rec DK 
332 Direct Rollover To IRA Rec Wrong Quantity 
[[DTCC]] Public (White)

---

## Page 29

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 29 
Code Description 
333 Direct Rollover To IRA Rec Wrong Security 
334 Direct Rollover To IRA Rec Wrong Money 
335 Direct Rollover To IRA Rec Partial 
336 Direct Rollover To IRA Rec Need More A/C Info 
337 Direct Rollover To IRA Rec Needs Due Bill 
338 Direct Rollover To IRA Rec Partial Rec Partial Ret 
340 Direct Rollover To Qualified Plan 
341 Direct Rollover To Qualified Plan Reclaim DK 
342 Direct Rollover To Qualified Plan Rec Wrong Quantity 
343 Direct Rollover To Qualified Plan Rec Wrong Security 
344 Direct Rollover To Qualified Plan Rec Wrong Money 
345 Direct Rollover To Qualified Plan Rec Partial 
346 Direct Rollover To Qualified Plan Need More A/C Info 
347 Direct Rollover To Qualified Plan Need Due Bill 
348 Direct Rollover To Qualified Plan Partial Rec Partial Ret 
530 [[IPO]] Direct Concession 
531 [[IPO]] Direct Concession Reclaim DK 
532 [[IPO]] Direct Concession Rec Wrong Quantity 
533 [[IPO]] Direct Concession Rec Wrong Security 
534 [[IPO]] Direct Concession Rec Wrong Money 
535 [[IPO]] Direct Concession Rec Partial 
536 [[IPO]] Direct Concession Rec Need A/C Info 
537 [[IPO]] Direct Concession Rec Needs Due Bill 
538 [[IPO]] Direct Concession Partial Rec Partial Ret 
539 [[ID]] [[IPO]] Directed Concession 
540 [[IPO]] [[syndicate]] Over Subscribed 
541 [[IPO]] Over Subscribed Reclaim DK 
542 [[IPO]] Over Subscribed Rec Wrong Quantity 
543 [[IPO]] Over Subscribed Rec Wrong Security 
544 [[IPO]] Over Subscribed Rec Wrong Money 
545 [[IPO]] Over Subscribed Rec Partial 
[[DTCC]] Public (White)

---

## Page 30

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 30 
Code Description 
546 [[IPO]] Over Subscribed Rec Need A/C Info 
547 [[IPO]] Over Subscribed Rec Needs Due Bill 
548 [[IPO]] Over Subscribed Partial Rec Partial Ret 
549 [[ID]] [[IPO]] Over Subscribed 
550 [[IPO]] [[syndicate]] Directed and Over Subscribed 
551 [[IPO]] [[syndicate]] (550) Reclaim DK 
552 [[IPO]] [[syndicate]] (550) Rec Wrong Quantity 
553 [[IPO]] [[syndicate]] (550) Rec Wrong Security 
554 [[IPO]] [[syndicate]] (550) Rec Wrong Money 
555 [[IPO]] [[syndicate]] (550) Rec Partial 
556 [[IPO]] [[syndicate]] (550) Rec Need A/C Info 
557 [[IPO]] [[syndicate]] (550) Rec Needs Due Bill 
558 [[IPO]] [[syndicate]] (550) Rec Partial Rec Partial Ret 
559 [[ID]] [[IPO]] [[syndicate]] Directed and Over Subscribed 
560 [[ID]] Foreign Distribution 
600 [[collateral]] [[DO]] 
601 [[collateral]] [[DO]] Reclaim DK 
602 [[collateral]] [[DO]] Rec Wrong Quantity 
603 [[collateral]] [[DO]] Rec Wrong Security 
605 [[collateral]] [[DO]] Rec Partial 
606 [[collateral]] [[DO]] Rec Needs A/C Info 
607 [[collateral]] [[DO]] Rec Needs Due Bill 
608 [[collateral]] [[DO]] Prtl Rec Partial Ret 
609 [[collateral]] [[DO]] Recall 
610 [[collateral]] [[DO]] Return 
611 [[collateral]] [[DO]] Ret Rec DK 
612 [[collateral]] [[DO]] Ret Rec Wrong Qty 
613 [[collateral]] [[DO]] Ret Rec Wrong [[SEC]] 
615 [[collateral]] [[DO]] Ret Rec Partial 
616 [[collateral]] [[DO]] Ret Rec A/C Info 
617 [[collateral]] [[DO]] Ret Rec Need Due Bill 
[[DTCC]] Public (White)

---

## Page 31

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
4. Appendices 31 
Code Description 
618 [[collateral]] [[DO]] Ret Prtl Rec Prtl Ret 
619 [[collateral]] [[DO]] Recall Reclamation 
620 Balance Order 
621 Balance Order Rec DK 
622 Balance Order Rec Wrong Qty 
623 Balance Order Rec Wrong [[SEC]] 
624 Balance Order Rec Wrong Money 
625 Balance Order Rec PRTL 
626 Balance Order Rec A/C Info 
627 Balance Order Rec Due Bill 
628 Balance Order Prtl Rec Prtl Ret 
 
 
  
[[DTCC]] Public (White)

---

## Page 32

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
Release Notes 32 
RELEASE NOTES 
 
This is the document history reflecting changes to the file. 
09/03/2020 Added [[SFT]] Clearing [[DO]] Reason codes: [[SFT]] [[Stock]] Loan “200” and [[SFT]] [[Stock]] Loan Return 
“201” to Section 4.
3 Valid Reason Codes. Added note in Comments field, for DOs related to 
[[SFT]] Clearing.  
• Removed "042" Security Holder Tracking Service from position 417 in the Expanded
T
ransaction Type field.
• Made general updates to remove outdated references and reformat the document.
11/30/2018 Removed formatting and references to old changes. 
08/16/2016 Content of Control Number (in position 170) and Expanded Control Number (in position 569) is 
changing with the introduction of the new Matching Utilities (see Important Notice B# 3706- 16), 
alphanumeric [[ID]] Control Numbers were introduced.  See Field Description for changes.  
09/03/2015 Added status code “T” and “W” in Section 3 Position 3 – MMI Finality Through Optimization 
Changes. Added reason codes: 
• 134 MMI SECONDARY [[DO]] – BYPASS FUNDING DECISION
• 135 MMI SECONDARY [[DO]] – RECLAIM BYPASS FUNDING DECISION
05/12/2014 Added [[CNS]] Sub-Account types “R” to position 45.
12/18/2012 The following changes were made to bring the existing document up to current standards.
Revised [[CCF]] Header Record description.
Removed references to CCRDTFDB and added NDMDTFGP and NDMDTFSP.
Revised CF2 Header and Trailer Records
Changed [[CCF]]-II references to read CF2. 
Identified existing CF2 HDR and TRL Record Format as NDM specific. 
Corrected “TLR” in Field Description (position 1) to read “TRL”. 
Added (0001) to Field Description (position 56). 
Expanded Filler (position 60) from 15 to ??? 
Removed Sequence Number field (position 75). 
Added FTP specific CF2 Header and Trailer Record Format. 
06/30/2010 Added a new field IMS Transaction [[ID]] in position 808. 
09/12/2008 Added a new value to the Expanded Transaction Type field in position 417 on page 16, “42” =  
Security Holder Tracking Service 
01/30/2008 Added OCC Symbology and Sub-Accounting fields (123 characters) starting position 714 
through 837 (pages 16-17). 
[[DTCC]] Public (White)

---

## Page 33

5.11 [[settlement]] [[participant]] Activity (DTFPART): Function User’s Guide 
Release Notes 33 
 
 
 
11/01/2004 Changed wording in position 417 Expanded Transaction Type 
025 = [[CNS]] Deliver Order (SIAC Loan). 
Added Reason Codes 620 thru 628 to Section 4.3 Valid Reason Codes.  
03/01/2003 Added [[ID]] Control number to position 201 under Reorg Segregation Activity: 
08/07/2001 Added field description information relating to RDS Activity and RDS Activity Clearing Transfer 
Remarks (position 201). Added a new Transaction Type 41 (Pend Canceled Multicurrency 
Segregation) to position 56. Added new Transaction Types 040 (Multicurrency Segregation 
Deliver Order), 41 (Multicurrency Segregation), and 900 (Pend Canceled Multicurrency   
Segregation) to position 417. Added Transaction Type 41 (Pend Canceled Multicurrency 
Segregation) to position 545. Added the following fields starting in position 587: Batch Variable, 
Batch Constant, [[transfer agent]] #, FOSP Indicator, Contra- Pledgee, ABA, Fed Sub account, 
Third Party Info. 
04/10/2001 Added reason codes 600-619 to appendix 4.3 Valid Reason Codes. 
01/12/2001 Position 510 format changed from character to packed, field name changed to filler and the 
phrase “[[DTC]] Internal Control Information” was eliminated. 
01/11/2000 Expanded DTFPART Record from 518 bytes to 666 bytes. 
Added the following fields starting in byte 519: 
ATP Original Transaction Reference Number - new 
Expanded Serial Number - unpacked 
Expanded Loan Date - unpacked 
New Expanded Account Type - unpacked 
New Expanded Action Code - unpacked 
New Expanded Transmission Type - unpacked 
Expanded Trade Date - unpacked 
Expanded Cents Amount - unpacked 
Expanded Dollar Amount - unpacked 
Expanded Journal Code - unpacked 
Expanded Control Number - unpacked 
Expanded ATP Record Address - unpacked 
01/26/1998 [[custody]] Activity codes added to DTFPART data record. 
11/24/1997 Made correction to Loan Date field of DTFPART record (MMDDYY to YYMMDD).  
10/23/1997 Removed errant T of C entries from field description in DTFPART Data Record field [[CUSIP]] 
Descriptor and narrative in section 1.3 [[CCF]]-II Header and Trailer record. Regenerated T of C. 
 
 
[[DTCC]] Public (White)

---

## Page 34

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] at: 
DTCSupport@[[DTCC]].com 
or visit us on the web at: 
http://www.[[DTCC]].com/client-center 
[[DTCC]] Public (White)