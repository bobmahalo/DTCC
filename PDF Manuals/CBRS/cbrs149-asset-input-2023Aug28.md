---
title: "CBRS Asset Input (A) - DATATRAK SYSID: PROD 36708 / PSE 46708"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs149-asset-input-2023Aug28.pdf"
pages: 34
size: "503.3 KB"
category: "CBRS"
ingested_on: "2026-06-05"
---

# CBRS Asset Input (A) - DATATRAK SYSID: PROD 36708 / PSE 46708

**Original File:** [cbrs149-asset-input-2023Aug28.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs149-asset-input-2023Aug28.pdf)  
**Category:** CBRS  
**Total Pages:** 34  
**File Size:** 503.3 KB  

---

## Page 1

Cost Basis Reporting Service (CBRS) 
CBRS [[Asset]] INPUT (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
AUGUST 28, 2023 
 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 
The rules and edits for the Original [[Asset]] record and Corrected [[Asset]] record (Record content indicator 01 and 
02) are in the following table. For the rules and edits for the Reject and Request records (Record content 
indicator 03 and 04), see the table in the Firm Reject and Request section. 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
Field Name Length Start End Type OPT/ 
REQ/ 
COND 
Comments 
Record Type  1  1 1 A/N  REQ  Always A 
Rule 
If this field is populated with a value other than ‘A’, CBRS drops 
the record as unknown 
Record Length  4  2 5 NUM  REQ  Always 1000 
Record Content 
Indicator 
2 6 7 A/N REQ Values: 
• 01 = Original [[Asset]] record 
• 02 = Corrected [[Asset]] record 
• 03 = Firm reject record 
• 04 = Request record 
Edit 

---

## Page 2

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 2 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
If field is 02 = Corrected [[Asset]] record, at least one 
accompanying tax lot record must have a value of 02 = 
Corrected tax lot record in its Record Content Indicator field 
There is no edit between the Corrected [[Asset]] record and the 
previous Original [[Asset]] record 
The value 03 = Firm reject record refers to a record that the 
receiver of the original or corrected [[Asset]] record cannot apply to 
its system. The firm reject record is different from a system 
reject, where CBRS rejects a submitted record—regardless of 
record content indicator—because the record violates system 
rules and edits.  
• If the submitter populates the Date Transfer was Initiated 
field with a date of 01/35/2011, CBRS rejects the record 
because 01/35/2011 is an invalid date. This is a system 
reject.  
• If a submitter sends an [[Asset]] record with a quantity of 
1,000 [[shares]] and the receiver has only one position of 500 
[[shares]] on its books, the receiver can send a reject record 
to the submitter because the receiver cannot apply 1,000 
[[shares]] of cost basis to a 500 share position. This is a firm 
reject. 
Transaction Type 2 8 9 A/N  REQ  Firm to Firm:  
01 = ACATS  
02 = Free [[DTC]] Deliver Order (Non-ACATS) 
03 = Valued [[DTC]] Deliver Order 
04 = Conversion 
05 = Mutual Fund Transfer (Non-ACATS) [change of [[Broker]]-
dealer] 
06 = Fed  
07 = Physical Movement [[settlement]] (Non-ACATS) 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository (Foreign)  
10 = Other 
11 – 25 Reserved for future use 
 
Firm & [[transfer agent]]: 
Agent submits/firm receives CBRS original/corrected 
record: 
26 = [[DWAC]] Deposit 
27 = Certificate Deposit 
28 = [[DRS]] Profile/[[DO]] 

---

## Page 3

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 3 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
29 – 35 Reserved for future use 
 
Firm submits/agent receives CBRS original/corrected 
record: 
36 = [[DWAC]] Withdrawal 
37 = Withdrawal by Transfer (WT) 
38 – 40 Reserved for future use 
 
Either Agent submits/firm receives or Firm submits/agent 
receives CBRS original/corrected record: 
41 = Direct Presentation 
42 – 45 Reserved for future use 
 
Firm & Fund (In-kind Mutual Fund Transfers): 
Fund submits/firm receives CBRS original/corrected 
record: 
46 = Fund to Firm Mutual Fund Transfer [via ACATS 
Fund/SERV interface; also known as PTF, Position Transfer 
Fund ACATS transfer type] 
47 – 50 Reserved for future use 
Firm submits/fund receives CBRS original/corrected 
record: 
51 = Firm to Fund Mutual Fund Transfer [via ACATS 
Fund/SERV interface; also known as PTF, Position Transfer 
Fund ACATS transfer type] 
52 – 55 Reserved for future use 
Either fund submits/firm receives or firm submits/fund 
receives CBRS original/corrected record: 
56 = Networking Transaction 
57 = Manual Mutual Fund Transfer 
58 – AIP  
59 – Alternative Investment (Non-AIP)  
60 – 65 Reserved for future use 
Note: record will be rejected if submitter/receiver codes [[DO]] not 
match the rules above 
Transfer Control 
Number  
30 10 39 A/N  REQ  Association between the [[Asset]] (A) and the Tax Lot (T) records 
is established when the contents of the Control Number of the 
two records are equal. 
Edit 

---

## Page 4

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 4 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
If transaction type is 01 = ACATS; this field should be the 
ACATS control number from the original transfer. For 
Transaction Type 01 = ACATS, CBRS edits this field to ensure it 
is a 14-byte numeric value. (The format of the ACATS control 
number is CCYYDDDNNNNNNN.)  
Best Practices 
If transaction type is 02 = Free [[DTC]] Deliver Order (Non-
ACATS), or 03 = Valued [[DTC]] Deliver Order; this field is the 
IMS Transaction [[ID]] number (16 bytes) as specified on the 
original transaction processed at [[DTC]]. 
If transaction type is 06 = Fed and the transfer occurred at the 
Fed, this field is the Input Message Accountability Data (IMAD) 
number assigned by the Fed to the transfer. 
If transaction type is 08 = OCC transfer (Non-ACATS), this field 
is the number assigned by the OCC to the transfer. 
If transaction type is 26 = [[DWAC]] Deposit, 27 = Certificate 
Deposit, 28 = [[DRS]] Profile/[[DO]], 36 = [[DWAC]] Withdrawal, 37 = 
Withdrawal by Transfer (WT); this field contains a reference [[ID]] 
number whose values and number of bytes changes depending 
on the original transaction processed at [[DTC]]. 
If transaction type is 41 = Direct Presentation; this field is 26 
characters: 
Julian Date (3 bytes: DDD) + [[participant]] Number (5 bytes) + 
Customer Account Number (18 bytes) 
If transaction type is 46 = Fund to Firm Mutual Fund Transfer 
or 51 = Firm to Fund Mutual Fund Transfer; this field is the 
FundSERV control number. Firms should use the Fund/SERV 
Control # from the ACATS Fund/SERV Statistics File, and add 
the letters ‘CATS’ to the front of it, in order to match the number 
that Funds should provide in this field. 
If the transaction type is 56 = Networking Transaction, the 
control number is the Networking control number 
For all other transaction types, 04 = Conversion, 05 = Mutual 
Fund Transfer (Non-ACATS), 07 = Physical Movement 
[[settlement]], 09 = Non-Domestic Depository, 10 = Other, 57 = 
Manual Mutual Fund Transfer; this field is the control number 
agreed upon by the contraparties involved in the original 
[[securities]] transaction. 
Alternate Control 
Number 
30 40 69 A/N COND Required if Transaction Type is 46 = Fund to Firm Mutual 
Fund Transfer, 51 = Firm to Fund Mutual Fund Transfer, or 
58 - AIP; the submitted value must be greater than spaces.  
Optional field for all other Transaction Types. 
Best Practices: 
For Transaction Types 46 = Fund to Firm Mutual Fund 
Transfer or 51 = Firm to Fund Mutual Fund Transfer, 
populate this field with the ACATS Control Number. 

---

## Page 5

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 5 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
For Transaction Type 58 AIP, populate this field with the AIP 16 
byte SIN Number ([[NSCC]] Security Identifier). CBRS rejects the 
record if greater or less than 16 bytes is populated.  
Filler 20 70 89 A/N REQ Reserved for future use. Spaces. 
Contra Firm 
Number  
8 90 97 A/N  COND  Populate this field with the number for the firm who is receiving 
the CBRS record. 
Use leading zeros. If a firm has a [[DTC]], [[NSCC]], or Transfer 
Agent Number, populate this field with that number. If the firm’s 
only identifying number is the CBRS Account Number, populate 
this field with that number. 
Rules for transaction types 36 = [[DWAC]] Withdrawal or 37 = 
Withdrawal by Transfer (WT) are as follows: 
• For transaction types 36 = [[DWAC]] Withdrawal or 37 
= Withdrawal by Transfer (WT) where the security 
is an unsponsored [[ADR]], CBRS will not be able to 
find the [[transfer agent]] number on the [[DTC]] security 
master file. In these cases, the submitter must 
populate this field. If the submitter leaves this field 
blank in these cases, CBRS rejects the record. 
• For all other [[securities]], if Transaction Type is 36 = 
[[DWAC]] Withdrawal or 37 = Withdrawal by Transfer 
(WT); the field would be left blank as CBRS performs 
a lookup of Contra Firm Number on the [[DTC]] security 
master file based upon [[CUSIP]]. 
• When Record content indicator is 01 = Original [[Asset]] 
record, and the submitter populates this field, CBRS 
will overwrite the submitter’s value with the value it 
finds on the [[DTC]] security master file. 
• When Record content indicator is 02 = Corrected 
[[Asset]] record, and the submitter populates this field, 
CBRS accepts the submitter’s value 
The field is required for all other transaction types. 
Filler 2 98 99 A/N REQ  
Contra Firm Type 6 100 105 A/N REQ Populate this field with the type of firm who is receiving the 
CBRS record. This type corresponds to the type of number in 
the Contra Firm Number field.  
Values: 
• AGTNBR = [[transfer agent]] 

---

## Page 6

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 6 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
• CBRACT = CBRS User 
• DTCPRT = [[DTC]] [[participant]] 
• NSCPRT = [[NSCC]] [[participant]] 
More values possible in future enhancements 
Edit 
If the Transaction Type is 01 = ACATS, 02 = Free [[DTC]] Deliver 
Order, 03 = Valued [[DTC]] Deliver Order, 04 = Conversion, 05 
= Mutual Fund Transfer (non-ACATS), 06 = Fed, 07 = 
Physical Movement [[settlement]], 08 = OCC transfer (Non-
ACATS), 09 = Non-Domestic Depository; 10 = Other, the 
Contra Firm Type must be NSCPRT = [[NSCC]] [[participant]], 
DTCPRT = [[DTC]] [[participant]], or CBRACT = CBRS User. 
If the Transaction Type is 26 = [[DWAC]] Deposit, 27 = Certificate 
Deposit, 28 = [[DRS]] Profile/[[DO]]; this field must be DTCPRT = 
[[DTC]] [[participant]]. 
If the Transaction Type is 36 = [[DWAC]] Withdrawal, 37 = 
Withdrawal by Transfer (WT), this field must be AGTNBR = 
[[transfer agent]]. 
If the Transaction Type is 41= Direct Presentation; this field 
must be AGTNBR = [[transfer agent]] or CBRACT = CBRS User 
or DTCPRT = [[DTC]] [[participant]]. 
If the Transaction Type is 46 = Fund to Firm Mutual Fund 
Transfer, this field must be DTCPRT = [[DTC]] [[participant]] or 
NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 51 = Firm to Fund Mutual Fund 
Transfer, this field must be DTCPRT = [[DTC]] [[participant]] or 
NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 56 = Networking Transaction, this 
field must be DTCPRT = [[DTC]] [[participant]] or NSCPRT = [[NSCC]] 
[[participant]]. 
If the Transaction Type is 57 = Manual Mutual Fund Transfer, 
58-AIP, 59-Alternative Investment (Non-AIP), this field must 
be CBRACT = CBRS User, DTCPRT = [[DTC]] [[participant]], or 
NSCPRT = [[NSCC]] [[participant]]. 
Filler 10 106 115 A/N REQ Reserved for future use. Spaces. 
Submitting Firm 
Number  
8 
 
116 123 A/N  REQ  Populate this field with the number of the firm who is submitting 
the CBRS record. Use leading zeros if a firm has a [[DTC]], [[NSCC]], 
or [[transfer agent]] Number, populate this field with that number. 
If the firm’s only identifying number is the CBRS Account 
Number, populate this field with that number. 
Filler 2 124 125 A/N REQ Reserved for future use. Spaces.  
Submitting Firm 
Type 
6 126 131 A/N REQ Populate this field with the type of the firm who is submitting the 
CBRS record. This type corresponds to the type of number in 
the Submitting Firm Number field.  

---

## Page 7

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 7 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
Values: 
• AGTNBR = [[transfer agent]] 
• CBRACT = CBRS User 
• DTCPRT = [[DTC]] [[participant]] 
• NSCPRT = [[NSCC]] [[participant]] 
More values possible in future enhancements 
Edit 
If the Transaction Type is, 01 = ACATS 02 = Free [[DTC]] Deliver 
Order, 03 = Valued [[DTC]] Deliver Order, 04 = Conversion, 05 
= Mutual Fund Transfer (non-ACATS), 06 = Fed, 07 = 
Physical Movement [[settlement]], 08 = OCC transfer (Non-
ACATS), 09 = Non-Domestic Depository; 10 = Other, the 
Submitting Firm Type must be NSCPRT = [[NSCC]] [[participant]], 
DTCPRT = [[DTC]] [[participant]], or CBRACT = CBRS User. 
If the Transaction Type is 26 = [[DWAC]] Deposit, 27 = Certificate 
Deposit, 28 = [[DRS]] Profile/[[DO]]; the Submitting Firm Type must 
be AGTNBR = [[transfer agent]], CBRACT=CBRS User, 
DTCPRT=[[DTC]] [[participant]], NSCPRT=[[NSCC]] [[participant]]. 
If the Transaction Type is, 36 = [[DWAC]] Withdrawal, 37 = 
Withdrawal by Transfer (WT); the Submitting Firm Type must 
be DTCPRT = [[DTC]] [[participant]], CBRACT=CBRS User, 
NSCPRT=[[NSCC]] [[participant]]. 
If the Transaction Type is 41= Direct Presentation; the 
Submitting Firm Type must be AGTNBR = [[transfer agent]] or 
CBRACT = CBRS User or DTCPRT = [[DTC]] [[participant]]. 
If the Transaction Type is 46 = Fund to Firm Mutual Fund 
Transfer, this field must be DTCPRT = [[DTC]] [[participant]] or 
NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 51 = Firm to Fund Mutual Fund 
Transfer, this field must be DTCPRT = [[DTC]] [[participant]] or 
NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 56 = Networking Transaction, this 
field must be DTCPRT = [[DTC]] [[participant]] or NSCPRT = [[NSCC]] 
[[participant]]. 
If the Transaction Type is 57 = Manual Mutual Fund Transfer, 
58-AIP, 59-Alternative Investment (Non-AIP) this field must be 
CBRACT = CBRS User, DTCPRT = [[DTC]] [[participant]], or 
NSCPRT = [[NSCC]] [[participant]]. 
Filler 18 132 149 A/N REQ Reserved for future use. Spaces. 
Receiver 
Customer Account 
Number  
20  150 169 A/N  COND  
 
Populate this field with the customer account number at the firm 
that received the [[Asset]] transfer. 
Required field for Transaction Types:  01 = ACATS, 02 = 
Free [[DTC]] Deliver Order (Non-ACATS), 03 = Valued [[DTC]] 
Deliver Order, 05 = Mutual Fund Transfer (Non-ACATS), 06 = 
Fed, 07 = Physical Movement [[settlement]], 08 = OCC transfer 

---

## Page 8

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 8 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
(Non-ACATS), 09 = Non Domestic Depository, 10 = Other, 46 
= Fund to Firm Mutual Fund Transfer, 51 = Firm to Fund Mutual 
Fund Transfer, 56 = Networking Transaction, 57 = Manual 
Mutual Fund Transfer, 58-AIP, 59-Alternative Investment 
(Non-AIP). 
Optional field for all other Transaction Types. 
Filler 10 170 179 A/N REQ Reserved for future use. Spaces. 
Deliverer 
Customer Account 
Number  
20  180 199 A/N  COND Populate this field with the customer account number at the firm 
that delivered the [[Asset]] transfer. 
Required field for Transaction Types: 01 = ACATS, 02 = Free 
[[DTC]] Deliver Order (Non-ACATS), 03 = Valued [[DTC]] Deliver 
Order, 04 = Conversions, 05 = Mutual Fund Transfer (Non-
ACATS). 06 = Fed, 07 = Physical Movement [[settlement]], 08 = 
OCC transfer (Non-ACATS), 09 = Non-Domestic Depository, 
10 = Other, 46 = Fund to Firm Mutual Fund Transfer, 51 = Firm 
to Fund Mutual Fund Transfer, 56 = Networking Transaction, 57 
= Manual Mutual Fund Transfer, 58-AIP, 59-Alternative 
Investment (Non-AIP). 
Optional field for all other Transaction Types. 
Best Practice 
The submitter should populate this field for Transaction Type. 
04 = Conversion. 
Filler 10 200 209 A/N REQ Reserved for future use. Spaces. 
ISIN Country 
Code  
2  210 211 A/N  OPT  [[default]] value is US. 
 
Edit 
Association between the [[Asset]] (A) and the Tax Lot (T) records 
is established when the contents of ISIN Country Code 
combined with ISIN Security Issue [[ID]] and ISIN Security Check 
Digit of the two records are equal.  
ISIN Security 
Issue [[ID]] ([[CUSIP]] 
number) 
9  212 220 A/N  COND  Required if [[Asset]] Category is not OPT. 
Required for all Transaction Types except 41 = Direct 
Presentation. 
If both ISIN Security Issue [[ID]] and [[Asset]] Description fields are 
left blank, CBRS rejects the record 
 
Edit 
Association between the [[Asset]] (A) and the Tax Lot (T) records 
is established when the contents of ISIN Security Issue [[ID]] 
combined with ISIN Country Code and ISIN Security Check Digit 
of the two records are equal.  

---

## Page 9

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 9 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
ISIN Security 
Check Digit  
1  221 221 A/N  COND  Required if ISIN Country Code is anything but blank or US, and 
ISIN Security Issue [[ID]] ([[CUSIP]] number) is populated. 
 
Edit 
Association between the [[Asset]] (A) and the Tax Lot (T) records 
is established when the contents of ISIN Security Check Digit 
combined with ISIN Country Code and ISIN Issue [[ID]] of the two 
records are equal.  
Filler 10 222 231 A/N REQ Reserved for future use. Spaces. 
 
 
Put - Call Indicator  1  232 232 A/N  COND  Values: 
• C = Call  
• P= Put 
Allowed for Transaction Types: 
01 = ACATS 
04 = Conversion 
06 = Fed 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository 
10 = Other 
If this field is populated for any other transaction type, CBRS 
rejects the record. 
Required if [[Asset]] Category = OPT. 
Edit 
Association between the [[Asset]] (A) and the Tax Lot (T) records 
is established when the contents of [[Option]] Symbol combined 
with Put-Call Indicator, [[Option]] Expiration Date, [[Option]] Strike 
Price Integer, and [[Option]] Strike Price Decimal of the two 
records are equal. 
[[Option]] Symbol  6  233 238 A/N  COND  Allowed for Transaction Types:  
01 = ACATS 
04 = Conversion 
06 = Fed 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository 
10 = Other 

---

## Page 10

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 10 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
If this field is populated for any other transaction type, CBRS 
rejects the record. 
Required if [[Asset]] Category = OPT. 
Edit 
Association between the [[Asset]] (A) and the Tax Lot (T) records 
is established when the contents of [[Option]] Symbol combined 
with Put-Call Indicator, [[Option]] Expiration Date, [[Option]] Strike 
Price Integer, and [[Option]] Strike Price Decimal of the two 
records are equal. 
[[Option]] Expiration 
Date 
–or– 
Last Factor Date 
(for MBS) 
8 239 246 A/N  COND  
• [[Option]] Expiration Date 
Allowed for Transaction Types: 
01 = ACATS 
04 = Conversion 
06 = Fed 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository 
10 = Other 
If this field is populated for any other transaction type, CBRS 
rejects the record. 
Required field if [[Asset]] Category = OPT. 
–or– 
• Last Factor Date 
When the [[Asset]] Category field is set to  
MBS = Mortgage Backed [[securities]], you can 
repurpose this field to input the last factor date. 
When using this field for the last factor information, 
you must input the same date value in both this 
[[Asset]] (A) and also the Tax Lot (T) records.  
Edits 
Association between the [[Asset]] (A) and the Tax Lot (T) records 
is established when the contents of [[Option]] Symbol combined 
with Put-Call Indicator, [[Option]] Expiration Date, [[Option]] Strike 
Price Integer, and [[Option]] Strike Price Decimal of the two 
records are equal. 
Format: CCYYMMDD 
If submitted date is not a valid calendar date, CBRS rejects the 
record. May be spaces or valid calendar date. Zeroes are not a 
valid value. 
 
 

---

## Page 11

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 11 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
[[Option]] Strike 
Price Integer  
5  247 251 NUM COND  Allowed for Transaction Types: 
01 = ACATS 
04 = Conversion 
06 = Fed 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository 
10 = Other 
If this field is populated for any other transaction type, CBRS 
rejects the record. 
Required if [[Asset]] Category = OPT. 
 
Edit 
Association between the [[Asset]] (A) and the Tax Lot (T) records 
is established when the contents of [[Option]] Symbol combined 
with Put-Call Indicator, [[Option]] Expiration Date, [[Option]] Strike 
Price Integer, and [[Option]] Strike Price Decimal of the two 
records are equal. 
[[Option]] Strike 
Price Decimal  
3 252 254 
NUM COND  Allowed for Transaction Types: 
01 = ACATS 
04 = Conversion 
06 = Fed 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository 
10 = Other 
If this field is populated for any other transaction type, CBRS 
rejects the record. Required if [[Asset]] Category = OPT.  
 
Edits 
Association between the [[Asset]] (A) and the Tax Lot (T) records 
is established when the contents of [[Option]] Symbol combined 
with Put-Call Indicator, [[Option]] Expiration Date, [[Option]] Strike 
Price Integer, and [[Option]] Strike Price Decimal of the two 
records are equal. 
The only valid values are 000 through 999 which represent 
decimal format. 
Filler 10 255 264 A/N REQ Reserved for future use. Spaces. 
 

---

## Page 12

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 12 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
[[Asset]] Description  140  265 404 A/N  COND  Contains a text-based description of the [[Asset]].  
Required when Transaction Type is 41 = Direct Presentation 
and ISIN Security Issue [[ID]] is blank. 
If both ISIN Security Issue [[ID]] and [[Asset]] Description fields are 
left blank, CBRS rejects the record. 
If this field is blank, ISIN Security Issue [[ID]] is populated, and 
CBRS cannot find the ISIN Security Issue [[ID]] in its master file, 
CBRS rejects the record. 
If this field is populated, ISIN Security Issue [[ID]] is populated 
and CBRS cannot find the ISIN Security Issue [[ID]] in its master 
file, CBRS will pass the record and add the words, Submitter 
ISIN to the end of this field. 
Best Practice 
Populate [[Asset]] Description field at all times. 
Edit 
Association between the [[Asset]] (A) and the Tax Lot (T) records 
is established when the contents of this field are equal, only 
when ISIN Security Issue [[ID]] is blank, and [[Asset]] Category is not 
OPT. 
[[Asset]] Category  4  405 408 A/N  REQ  Populate this field with the [[Asset]] category that corresponds to 
the transferred security. This is an important field that drives 
validation rules for the rest of the record. 
Values: 
• ALT = Alternative Investment 
• ANNU = Annuities 
• CDCP = CD & Commercial Paper 
• CORP = Corporate Bond 
• EQU = Equities 
• FCUR = Foreign Currency 
• FDEB = Foreign Debt 
• FEQU = Foreign [[Equity]] 
• GOVT = US Govt. and Govt. Agency 
• LPAR = Limited Partnership 
• MBS = Mortgage Backed [[securities]] (FNMA, GNMA, 
FHLMC) 
• MFNM = Mutual Fund Non-Money Market 
• MUNI = Municipal [[Bonds]] 
• OPT = Options 
• REIT = Real Estate Investment Trust 

---

## Page 13

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 13 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
• RGT = Right 
• UARP = [[UIT]] (Auction Rate Preferred) 
• UDSC = [[UIT]] (Deferred Sale Charge) 
• [[UIT]] = Unit Investment Trust 
• UNT = Units 
• WAR = Warrant 
• ZERO = Zero Coupon [[Bonds]]  
For Transaction Types 46 = Fund to Firm Mutual Fund 
Transfer, 51 = Firm to Fund Mutual Fund Transfer, 56 = 
Networking Transaction, or 57 = Manual Mutual Fund 
Transfer this field must equal MFNM. Otherwise, CBRS rejects 
the record. 
Value OPT is required for Transaction Type 08 = OCC 
transfer (Non-ACATS). Value OPT is valid only for Transaction 
Types: 01 = ACATS, 04 = Conversion, 06 = FED, or 08 = OCC 
transfer (Non-ACATS), 09 = Non-Domestic Depository, 10 = 
Other. Otherwise, CBRS rejects the record. 
Filler 10 409 418 A/N REQ Reserved for future use. Spaces. 
Total Position 
Quantity  
17  419 435 A/N  REQ  Total quantity of all tax lots associated with this [[Asset]]. 
CBRS sums up the tax lot quantities and compare them to the 
value populated in this field. If the sum of the tax lot quantities 
does not equal the value in this field, CBRS rejects the record. 
Zero is not a valid value for this field. 
The position of the decimal is denoted by a comma (,). Up to 
four decimal places are supported before truncation occurs. 
Filler 20 436 455 A/N REQ Reserved for future use. Spaces. 
Date Transfer was 
Initiated 
8 456 463 A/N COND Date when the transfer of the security was initiated. Date can be 
today or in the past. A future date is not a valid value for this 
field.  
If submitted date is not a valid calendar date, or is in the future, 
CBRS rejects the record. May be spaces or valid calendar date. 
Zeroes are not a valid value. 
Either Date Transfer was Initiated or [[settlement]] Date of 
Transfer is required for the following Transaction Types: 01 = 
ACATS, 02 = Free [[DTC]] Deliver Order, 03 = Valued [[DTC]] Deliver 
Order, 04 = Conversion, 05 = Mutual Fund Transfer (non-
ACATS), 06 = Fed, 07 = Physical Movement [[settlement]], 09 
=Non-Domestic Depository,10 = Other, 26 = [[DWAC]] Deposit, 
27 = Certificate Deposit, 28 = [[DRS]] Profile/[[DO]], 36 = [[DWAC]] 
Withdrawal, 37 = Withdrawal by Transfer (WT), 41 = Direct 
Presentation, 46 = Fund to Firm Mutual Fund Transfer, 51 = 
Firm to Fund Mutual Fund Transfer, 56 = Networking 

---

## Page 14

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 14 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
Transaction, 57 = Manual Mutual Fund Transfer, 58-AIP, 59-
Alternative Investment (Non-AIP). 
Format: CCYYMMDD 
[[settlement]] Date of 
Transfer 
8 464 471 A/N COND [[settlement]] date of the transfer of the security. 
If submitted date is not a valid calendar date, CBRS rejects the 
record. May be spaces or valid calendar date. Zeroes are not a 
valid value. 
Required if Transaction Type is 08 = OCC transfer (Non-
ACATS). 
Either Date Transfer was Initiated or [[settlement]] Date of 
Transfer is required for the following Transaction Types: 01 = 
ACATS, 02 = Free [[DTC]] Deliver Order, 03 = Valued [[DTC]] Deliver 
Order, 04 = Conversion, 05 = Mutual Fund Transfer (non-
ACATS), 06 = Fed, 07 = Physical Movement [[settlement]], 09 
=Non-Domestic Depository,10 = Other, 26 = [[DWAC]] Deposit, 
27 = Certificate Deposit, 28 = [[DRS]] Profile/[[DO]], 36 = [[DWAC]] 
Withdrawal, 37 = Withdrawal by Transfer (WT), 41 = Direct 
Presentation, 46 = Fund to Firm Mutual Fund Transfer, 51 = 
Firm to Fund Mutual Fund Transfer, 56 = Networking 
Transaction, 57 = Manual Mutual Fund Transfer, 58-AIP, 59-
Alternative Investment (Non-AIP).  
Format: CCYYMMDD 
Position Code  1  472 472 A/N  REQ Values: 
• L = Long position  
• S = [[short position]] 
If at least one firm on the record is a [[transfer agent]] or 
transaction type 46, 51, 56, 57, CBRS will set this value to L = 
Long position. Otherwise, if the submitter populates this field 
with anything other than L or S, CBRS rejects the record. 
Value B = Borrowed is valid only when Record content 
indicator is 04 = Request record. If this field is populated with 
B = Borrowed, and Record content indicator is not 04 = 
Request record, CBRS rejects the record. 
For the value B = Borrowed, Total Original Cost, Total 
Current Cost, and Total Average Cost should not be 
populated. If the cost fields are populated when this field is B = 
Borrowed, CBRS rejects the record. 
Note: Value B = Borrowed position means that the delivery 
creates a [[short position]] on the submitter’s books. 
Filler 131 473 603 A/N REQ Reserved for future use. Spaces. 
 

---

## Page 15

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 15 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
Disposition 
Method Used 
2  604 605 A/N  OPT  Indicates the lot disposition method used by the delivering firm. 
The list of values below does not include all possible disposition 
methods. 
Values:  
• 01 = FIFO (First In First Out) 
• 02 = LIFO (Last In First Out) 
• 03 = High Cost 
• 04 = Low Cost 
• 05 = Average Cost 
• 06 = Select Lot 
If this field is populated with an invalid value, CBRS spaces out 
the field and pass the record.  
Note:  
The list of valid values does not represent all possible standing 
instructions, but the values above are the only valid values for 
CBRS. 
[[shares]] to Cover 
Short Indicator 
1 606 606 A/N OPT The submitter should populate this field with a Y when it 
receives a customer request to deliver [[shares]] to satisfy a short 
position at the receiving firm. The receiving firm will then expect 
cost basis to [[Close Out]] the short. 
Values:  
• Y = Yes 
• N = No ([[default]]) 
Firm Reject 
Reason Code 
2 607 608 A/N COND Only applicable if Record Content Indicator is 03 = Firm reject 
record. Otherwise, leave blank. 
Values: 
• 01 = Receiver cannot apply received cost basis record 
• 02 = CBRS quantity is greater than delivered quantity 
• 03 = [[CUSIP]] does not belong to [[issuer]]/[[transfer agent]] 
Field is required if Record content indicator is 03 = Firm 
reject record. 
Value 03 = [[CUSIP]] does not belong to [[issuer]] Transaction is 
valid only when Transaction Type is 36 = [[DWAC]] Withdrawal 
or 37 = Withdrawal by Transfer and Record Content 
Indicator is 03 = Firm reject record.  
If this value is used is used for any other transaction types when 
Record Content Indicator is 03 = Firm reject record, CBRS 
rejects the record. 
If field is populated when Record content indicator is 01 = 
Original [[Asset]] record, 02 = Corrected [[Asset]] record, or 04 = 
Request record, CBRS spaces out the field and continue to 
pass the record. 

---

## Page 16

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): ORIGINAL AND CORRECTED 16 
COST BASIS [[Asset]] INPUT (A) ORIGINAL AND CORRECTED RECORDS 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
ACATS [[Asset]] 
Sequence 
Number 
6 609 614 NUM COND This field should be the ACATS [[Asset]] Sequence Number from 
the original transfer. 
Required when Transaction Type is 01 = ACATS and the ‘Date 
Transfer was Initiated’ or the ‘[[settlement]] Date of Transfer’ is 
later than 07/26/2012. Format is 6 digits. Value in this field must 
be numeric and greater than zero. Use leading zeros if 
necessary.  
If Transaction Type is 01 = ACATS and both the ‘Date Transfer 
was Initiated’ and the ‘[[settlement]] Date of Transfer’ are equal or 
prior to 07/26/2012, the field may contain spaces, all zeroes, or 
a valid numeric value. Otherwise CBRS rejects the record. 
For all other transaction types, CBRS spaces out the field and 
passes the record. 
Filler 386 615 1000 A/N REQ Reserved for future use. Spaces. 
 
  

---

## Page 17

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 17 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 
For the rules and edits for the Original [[Asset]] record and Corrected [[Asset]] record (Record content indicator 01 
and 02), see the table in the Original and Correct Records section. For the rules and edits for the Reject and 
Request records (Record content indicator 03 and 04), see the following table: 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
FIELD NAME  LENGTH  START END TYPE  OPT/ 
REQ/ 
COND  
COMMENTS  
Record Type  1  1 1 A/N  REQ  Always A. 
Rule 
If this field is populated with a value other than ‘A’, CBRS 
drops the record as unknown. 
Record Length  4  2 5 NUM  REQ  Always 1000. 
Record Content 
Indicator 
2 6 7 A/N REQ Values: 
• 01 = Original [[Asset]] record 
• 02 = Corrected [[Asset]] record 
• 03 = Firm reject record 
• 04 = Request record 
If field is 03 = Firm reject record or 04 = Request 
record, only certain fields will be required as defined in 
the following layout. 
If field is 03 = Firm reject record or 04 = Request 
record, there will be no corresponding tax lot record(s). 
Note:  
The value 03 = Firm reject record refers to a record that 
the receiver of the original or corrected [[Asset]] record 
cannot apply to its system. The firm reject record is 
different from a system reject, where CBRS rejects a 
submitted record—regardless of record content indicator—
because the record violates system rules and edits. For 
example, if the submitter populates the Date Transfer 
was Initiated field with a date of 01/35/2011, CBRS 
rejects the record because 01/35/2011 is not a valid 
calendar date. This is a system reject. On the other hand, 
if a submitter sends an [[Asset]] record with a quantity of 
1,000 [[shares]], and the receiver has only one lot of 500 
[[shares]] on its books, the receiver can send a reject record 
to the submitter because the receiver cannot apply 1,000 
[[shares]] of cost basis to a 500 share lot. This is a firm 
reject. 
 
 

---

## Page 18

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 18 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
Transaction Type 2 8 9 A/N  REQ  Firm to Firm:  
01 = ACATS  
02 = Free [[DTC]] Deliver Order (Non-ACATS) 
03 = Valued [[DTC]] Deliver Order 
04 = Conversion 
05 = Mutual Fund Transfer (Non-ACATS) [change of 
[[Broker]]-dealer] 
06 = Fed  
07 = Physical Movement [[settlement]] (Non-ACATS) 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository (Foreign)  
10 = Other 
11 – 25 Reserved for future use 
 
Firm & [[transfer agent]]: 
Agent submits/firm receives CBRS original/corrected 
record: 
26 = [[DWAC]] Deposit 
27 = Certificate Deposit 
28 = [[DRS]] Profile/[[DO]] 
29 – 35 Reserved for future use 
Firm submits/agent receives CBRS original/corrected 
record: 
36 = [[DWAC]] Withdrawal 
37 = Withdrawal by Transfer (WT) 
38 – 40 Reserved for future use 
 
Either Agent submits/firm receives or Firm 
submits/agent receives CBRS original/corrected 
record: 
41 = Direct Presentation 
42 – 45 Reserved for future use 
 
 
 
 

---

## Page 19

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 19 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
Firm & Fund (In-kind Mutual Fund Transfers): 
Fund submits/firm receives CBRS original/corrected 
record: 
46 = Fund to Firm Mutual Fund Transfer [via ACATS 
Fund/SERV interface; also known as PTF, Position 
Transfer Fund ACATS transfer type]. 
47 – 50 Reserved for future use 
Firm submits/fund receives CBRS original/corrected 
record: 
51 = Firm to Fund Mutual Fund Transfer [via ACATS 
Fund/SERV interface; also known as PTF, Position 
Transfer Fund ACATS transfer type]. 
52 – 55 Reserved for future use 
Either fund submits/firm receives or firm submits/fund 
receives CBRS original/corrected record: 
56 = Networking Transaction 
57 = Manual Mutual Fund Transfer 
58- AIP 
59- Alternative Investment (Non-AIP) 
58 – 65 Reserved for future use 
Note: record will be rejected if submitter/receiver codes [[DO]] 
not match the rules above. 
Transfer Control 
Number  
30 10 39 A/N  REQ  If the Record content indicator is 03 = Firm reject 
record, this field is the control number of the Original 
[[Asset]] record or Corrected [[Asset]] record received. 
If the Record content indicator is 04 = Request record, 
follow the formats below: 
 
Edit 
If transaction type is 01 = ACATS; this field should be the 
ACATS control number from the original transfer. For 
Transaction Type 01 = ACATS, CBRS edits this field to 
ensure it is a 14-byte numeric value. (The format of the 
ACATS control number is CCYYDDDNNNNNNN.)  
 
Best Practices 
If transaction type is 02 = Free [[DTC]] Deliver Order (Non-
ACATS), or 03 = Valued [[DTC]] Deliver Order; this field is 
the IMS Transaction [[ID]] number (16 bytes) as specified on 
the original transaction processed at [[DTC]]. 

---

## Page 20

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 20 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
If transaction type is 06 = Fed the transfer occurred at the 
Fed, this field is the Input Message Accountability Data 
(IMAD) number assigned by the Fed to the transfer. 
If transaction type is 08 = OCC transfer (Non-ACATS), 
this field is the number assigned by the OCC to the 
transfer. 
If transaction type is 26 = [[DWAC]] Deposit, 27 = 
Certificate Deposit, 28 = [[DRS]] Profile/[[DO]], 36 = [[DWAC]] 
Withdrawal, 37 = Withdrawal by Transfer (WT); this field 
contains a reference [[ID]] number whose values and number 
of bytes changes depending on the original transaction 
processed at [[DTC]]. 
If transaction type is 41 = Direct Presentation; this field is 
26 characters: 
Julian Date (3 bytes: DDD) + [[participant]] Number (5 bytes) 
+ Customer Account Number (18 bytes) 
If transaction type is 46 = Fund to Firm Mutual Fund 
Transfer or 51 = Firm to Fund Mutual Fund Transfer; 
this field is the FundSERV control number. Firms should 
use the Fund/SERV Control # from the ACATS 
Fund/SERV Statistics File, and add the letters ‘CATS’ to 
the front of it, in order to match the number that Funds 
should provide in this field. 
If the transaction type is 56 = Networking Transaction, 
the control number is the Networking control number. 
For all other transaction types, 04 = Conversion, 05 = 
Mutual Fund Transfer (Non-ACATS), 06 = Fed, 07 = 
Physical Movement [[settlement]], 09 = Non-Domestic 
Depository, 10 = Other, 57 = Manual Mutual Fund 
Transfer; this field is the control number agreed upon by 
the contraparties involved in the original [[securities]] 
transaction. 
Alternate Control 
Number 
30 40 69 A/N COND Required if Transaction Type is 46 = Fund to Firm 
Mutual Fund Transfer, 51 = Firm to Fund Mutual Fund 
Transfer, 58- AIP; the submitted value must be greater 
than spaces. For all other Transaction Types, this field 
is optional. 
 
Best Practice 
For Transaction Types 46 = Fund to Firm Mutual Fund 
Transfer or 51 = Firm to Fund Mutual Fund Transfer, 
populate this field with the ACATS Control Number. 
For Transaction Type 58 AIP, populate this field with the 
AIP SIN Number ([[NSCC]] Security Identifier). 
Filler 20 70 89 A/N REQ Reserved for future use. Spaces. 

---

## Page 21

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 21 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
Contra 
Firm Number  
8 90 97 A/N  COND  Populate this field with the number for the firm who is 
receiving the CBRS record. 
Use leading zeros, If a firm has a [[DTC]], [[NSCC]], or Transfer 
Agent Number, populate this field with that number. If the 
firm’s only identifying number is the CBRS Account 
Number, populate this field with that number. 
Rules for transaction types 26 = [[DWAC]] Deposit, 27 = 
Certificate Deposit, or 28 = [[DRS]] Profile/[[DO]] are as 
follows: 
• For transaction types 26 = [[DWAC]] Deposit, 27 = 
Certificate Deposit, or 28 = [[DRS]] Profile/[[DO]] where 
the security is an unsponsored [[ADR]], CBRS cannot 
[[Locate]] the [[transfer agent]] number on the [[DTC]] security 
master file. In these cases, the submitter must 
populate this field. If the submitter leaves this field 
blank in these cases, CBRS rejects the record. 
• For all other [[securities]], if Transaction Type is 26 = 
[[DWAC]] Deposit, 27 = Certificate Deposit, or 28 = 
[[DRS]] Profile/[[DO]]; the field would be left blank as 
CBRS performs a lookup of Receiver Firm Number 
on the [[DTC]] security master file based upon [[CUSIP]]. 
• When Record content indicator is 03 = Firm reject 
record, and the submitter populates this field, CBRS 
accepts the submitter’s value. 
• When Record content indicator is 04 = Request 
record, and the submitter populates this field, CBRS 
will overwrite the submitter’s value with the value it 
finds on the [[DTC]] security master file. 
Required field for all other transaction types. 
Filler 2 98 99 A/N REQ Reserved for future use. Spaces. 
Contra Firm Type 6 100 105 A/N REQ Populate this field with the type of firm who is receiving the 
CBRS record. This type corresponds to the type of 
number in the Contra Firm Number field.  
Values: 
• AGTNBR = [[transfer agent]] 
• CBRACT = CBRS User 
• DTCPRT = [[DTC]] [[participant]] 
• NSCPRT = [[NSCC]] [[participant]] 
More values possible in future enhancements. 
Edit 
If the Transaction Type is, 01 = ACATS, 02 = Free [[DTC]] 
Deliver Order, 03 = Valued [[DTC]] Deliver Order, 04 = 
Conversion, 05 = Mutual Fund Transfer (non-ACATS), 
06 = Fed, 07 = Physical Movement [[settlement]], 08 = 

---

## Page 22

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 22 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
OCC transfer (Non-ACATS), 09 = Non-Domestic 
Depository; 10 = Other, the Submitting Firm Type must 
be NSCPRT = [[NSCC]] [[participant]], DTCPRT = [[DTC]] 
[[participant]], or CBRACT = CBRS User. 
If the Transaction Type is, 26 = [[DWAC]] Deposit, 27 = 
Certificate Deposit, 28 = [[DRS]] Profile/[[DO]]; this field must 
be AGTNBR = [[transfer agent]], NSCPRT=[[NSCC]] 
[[participant]], DTCPRT= [[DTCC]] [[participant]], 
CBRACT=CBRS User. 
If the Transaction Type is 36 = [[DWAC]] Withdrawal, 37 = 
Withdrawal by Transfer (WT); this field must be 
DTCPRT=[[DTC]] [[participant]] CBRACT=CBRS User, 
NSCPRT= [[NSCC]] [[participant]].  
If the Transaction Type is 41= Direct Presentation; this 
field must be AGTNBR = [[transfer agent]] or CBRACT = 
CBRS User or DTCPRT = [[DTC]] [[participant]]. 
If the Transaction Type is 46 = Fund to Firm Mutual 
Fund Transfer, this field must be DTCPRT = [[DTC]] 
[[participant]] or NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 51 = Firm to Fund Mutual 
Fund Transfer, this field must be DTCPRT = [[DTC]] 
[[participant]] or NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 56 = Networking Transaction, 
this field must be DTCPRT = [[DTC]] [[participant]] or 
NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 57 = Manual Mutual Fund 
Transfer, 58-AIP, 59-Alternative Investment (Non-AIP); 
this field must be CBRACT = CBRS User, DTCPRT = 
[[DTC]] [[participant]], or NSCPRT = [[NSCC]] [[participant]]. 
Filler 10 106 115 A/N REQ Reserved for future use. Spaces. 
Submitting Firm 
Number  
8 116 123 A/N  REQ  Populate this field with the number of the firm who is 
submitting this CBRS record.  
Use leading zeros. If a firm has a [[DTC]], [[NSCC]], or Transfer 
Agent Number, populate this field with that number. If the 
firm’s only identifying number is the CBRS Account 
Number, populate this field with that number. 
Filler 2 124 125 A/N REQ Reserved for future use. Spaces. 
Submitting Firm 
Type 
6 126 131 A/N REQ Populate this field with the type of the firm who is 
submitting this CBRS record. This type corresponds to the 
type of number in the Submitting Firm Number field.  
Values: 
• AGTNBR = [[transfer agent]] 
• CBRACT = CBRS User 
• DTCPRT = [[DTC]] [[participant]] 
• NSCPRT = [[NSCC]] [[participant]] 

---

## Page 23

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 23 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
More values possible in future enhancements 
Edit 
If Transaction Type is, 01 = ACATS 02 = Free [[DTC]] 
Deliver Order, 03 = Valued [[DTC]] Deliver Order, 04 = 
Conversion, 05 = Mutual Fund Transfer (non-ACATS), 
06 = Fed, 07 = Physical Movement [[settlement]], 08 = 
OCC transfer (Non-ACATS), 09 = Non-Domestic 
Depository; 10 = Other, the Submitting Firm Type must 
be NSCPRT = [[NSCC]] [[participant]], DTCPRT = [[DTC]] 
[[participant]], or CBRACT = CBRS User. 
If the Transaction Type is 26 = [[DWAC]] Deposit, 27 = 
Certificate Deposit, 28 = [[DRS]] Profile/[[DO]]; the Submitting 
Firm Type must be DTCPRT=[[DTC]] [[participant]].  
If the Transaction Type is, 36 = [[DWAC]] Withdrawal, 37 = 
Withdrawal by Transfer (WT); the Submitting Firm Type 
must be AGTNBR = [[transfer agent]].  
If the Transaction Type is 41= Direct Presentation, the 
Submitting Firm Type must be AGTNBR = Transfer 
Agent or CBRACT = CBRS User or DTCPRT = [[DTC]] 
[[participant]]. 
If the Transaction Type is 46 = Fund to Firm Mutual 
Fund Transfer, this field must be DTCPRT = [[DTC]] 
[[participant]] or NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 51 = Firm to Fund Mutual 
Fund Transfer, this field must be DTCPRT = [[DTC]] 
[[participant]] or NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 56 = Networking Transaction, 
this field must be DTCPRT = [[DTC]] [[participant]] or 
NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 57 = Manual Mutual Fund 
Transfer, 58-AIP, 59-Alternative Investment (Non-AIP) 
this field must be CBRACT = CBRS User, DTCPRT = 
[[DTC]] [[participant]], or NSCPRT = [[NSCC]] [[participant]]. 
Filler 18 132 149 A/N REQ Reserved for future use. Spaces. 
Receiver Customer 
Account Number  
20  150 169 A/N  OPT  Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be the Receiver Customer 
Account Number (for example, the receiver of the cost 
basis, not the receiver of the reject record) on the Original 
[[Asset]] record or Corrected [[Asset]] record received. 
If the Record content indicator is 04 = Request record, 
this field should be the Receiver Customer Account 
Number on the original transaction that triggered the need 
to pass cost basis. 

---

## Page 24

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 24 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
Filler 10 170 179 A/N REQ Reserved for future use. Spaces. 
Deliverer Customer  
Account Number  
20  180 199 A/N  OPT Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be the Deliverer Customer 
Account Number (for example, the submitter of the cost 
basis information, not the submitter of the reject record) on 
the Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be the Deliverer Customer Account 
Number on the original transaction that triggered the need 
to pass cost basis. 
Filler 10 200 209 A/N REQ Reserved for future use. Spaces. 
ISIN Country Code  2  210 211 A/N  OPT  [[default]] value is ‘US’ 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 
ISIN Security Issue 
[[ID]] ([[CUSIP]] number) 
9  212 220 A/N  COND  Required if [[Asset]] Category is not OPT. 
For reject records (Record Content Indicator is 03 = 
Firm reject record), ISIN Security Issue [[ID]] ([[CUSIP]] 
number) is required for all Transaction Types except 41 = 
Direct Presentation. 
For request records (Record Content Indicator is 04 = 
Request record), ISIN Security Issue [[ID]] ([[CUSIP]] number) 
is required for all Transaction Types except 41 = Direct 
Presentation. 
 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 

---

## Page 25

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 25 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
ISIN Security 
Check Digit  
1  221 221 A/N  COND  Required if ISIN Country Code is anything but blank or 
US, and ISIN Security Issue [[ID]] ([[CUSIP]] number) is 
populated. 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 
Filler 10 222 231 A/N REQ Reserved for future use. Spaces. 
Put - Call Indicator  1  232 232 A/N  COND  Values: 
• C = Call  
• P = Put 
Allowed for Transaction Types:  
01 = ACATS 
04 = Conversion 
06 = Fed 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository 
10 = Other. If this field is populated for any other 
transaction type, CBRS rejects the record. 
Required if [[Asset]] Category = OPT.  
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 
[[Option]] Symbol  6  233 238 A/N  COND  Allowed for Transaction Types: 01 = ACATS, 04 = 
Conversion, 06 = Fed, 08 = OCC transfer (Non-ACATS), 
09 = Non-Domestic Depository, 10 = Other. If this field 
is populated for any other transaction type, CBRS rejects 
the record. 
Required if [[Asset]] Category = OPT. 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 

---

## Page 26

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 26 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis.  
[[Option]] Expiration 
Date 
–or– 
Last Factor Date 
(for MBS) 
8 239 246 A/N  COND  • [[Option]] Expiration Date 
Allowed for Transaction Types: 
01 = ACATS 
04 = Conversion 
06 = Fed 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository 
10 = Other 
If this field is populated for any other transaction type, 
CBRS rejects the record. 
Required field if [[Asset]] Category = OPT. 
–or– 
• Last Factor Date 
When the [[Asset]] Category field is set to  
MBS = Mortgage Backed [[securities]], you can 
repurpose this field to input the last factor 
date. When using this field for the last factor 
information, you must input the same date 
value in both this [[Asset]] (A) and also the Tax 
Lot (T) records.  
Edits 
Association between the [[Asset]] (A) and the Tax Lot (T) 
records is established when the contents of [[Option]] 
Symbol combined with Put-Call Indicator, [[Option]] 
Expiration Date, [[Option]] Strike Price Integer, and [[Option]] 
Strike Price Decimal of the two records are equal. 
Format: CCYYMMDD 
If submitted date is not a valid calendar date, CBRS 
rejects the record. May be spaces or valid calendar 
date. Zeroes are not a valid value. 
[[Option]] Strike Price 
Integer  
5  247 251 NUM  
COND  Allowed for Transaction Types: 
01 = ACATS 
04 = Conversion 
06 = Fed 
08 = OCC transfer (Non-ACATS) 

---

## Page 27

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 27 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
09 = Non-Domestic Depository 
10 = Other 
If this field is populated for any other transaction type, 
CBRS rejects the record. 
Required if [[Asset]] Category = OPT. 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 
[[Option]] Strike Price 
Decimal  
3 252 254 NUM  COND  Allowed for Transaction Types: 01 = ACATS, 04 = 
Conversion, 06 = Fed, 08 = OCC transfer (Non-ACATS), 
09 = Non-Domestic Depository, 10 = Other. If this field 
is populated for any other transaction type, CBRS rejects 
the record. 
Required if [[Asset]] Category = OPT. 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 
Filler 10 255 264 A/N REQ Reserved for future use. Spaces. 
[[Asset]] Description  140  265 404 A/N  COND  Contains a text-based description of the [[Asset]].  
Required when Transaction Type is 41 = Direct 
Presentation and ISIN Security Issue [[ID]] is blank. 
If both ISIN Security Issue [[ID]] and [[Asset]] Description fields 
are left blank, CBRS rejects the record. 
If this field is blank, ISIN Security Issue [[ID]] is populated, 
and CBRS cannot find the ISIN Security Issue [[ID]] in its 
master file, CBRS rejects the record. 
If this field is populated, ISIN Security Issue [[ID]] is 
populated, and CBRS cannot find the ISIN Security Issue 
[[ID]] in its master file, CBRS will pass the record and add the 
words, “Submitter ISIN” to the end of this field. 
Best Practice 
Populate [[Asset]] Description field at all times. 

---

## Page 28

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 28 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 
[[Asset]] Category  4  405 408 A/N  REQ Populate this field with the [[Asset]] category that 
corresponds to the transferred security. This is an 
important field that drives validation rules for the rest of the 
record. 
Values: 
• ALT = Alternative Investment 
• ANNU = Annuities 
• CDCP = CD & Commercial Paper 
• CORP = Corporate Bond 
• EQU = Equities 
• FCUR = Foreign Currency 
• FDEB = Foreign Debt 
• FEQU = Foreign [[Equity]] 
• GOVT = US Govt. and Govt. Agency 
• LPAR = Limited Partnership 
• MBS = Mortgage Backed [[securities]] (FNMA, GNMA, 
FHLMC) 
• MUNI = Municipal [[Bonds]] 
• MFNM = Mutual Fund Non-Money Market 
OPT = Options 
• REIT = Real Estate Investment Trust 
• RGT = Right 
• UARP = [[UIT]] (Auction Rate Preferred) 
• UDSC = [[UIT]] (Deferred Sale Charge) 
• [[UIT]] = Unit Investment Trust 
• UNT = Units 
• WAR = Warrant 
• ZERO = Zero Coupon [[Bonds]]  
For Transaction Types 46 = Fund to Firm Mutual Fund 
Transfer, 51 = Firm to Fund Mutual Fund Transfer, 56 = 
Networking Transaction, or 57 = Manual Mutual Fund 
Transfer this field must equal MFNM. Otherwise, CBRS 
rejects the record. 

---

## Page 29

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 29 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
Value OPT is required for Transaction Type 08 = OCC 
transfer (Non-ACATS). Value OPT is valid only for 
Transaction Types 01 = ACATS, 04 = Conversion, 06 = 
Fed, or 08 = OCC transfer (Non-ACATS), 09 = Non-
Domestic Depository, 10 = Other.  Otherwise, CBRS 
rejects the record. 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
the submitter should populate this field with the category 
they used for the [[Asset]]. 
Filler 10 409 418 A/N REQ Reserved for future use. Spaces. 
Total Position 
Quantity  
17  419 435 A/N  REQ  Total quantity of all tax lots associated with this [[Asset]]. 
The position of the decimal is denoted by a comma (,). Up 
to four decimal places are supported before truncation 
occurs. 
Zero is not a valid value for this field. 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 
Filler 20 436 455 A/N REQ Reserved for future use. Spaces. 
Date transfer was 
Initiated 
8 456 463 A/N 
COND Date when the transfer of the security was initiated. 
Date can be today or in the past. A future date is not a 
valid value for this field. 
If submitted date is not a valid calendar date, or is in the 
future, CBRS rejects the record. May be spaces or valid 
calendar date. Zeroes are not a valid value. 
Either Date Transfer was Initiated or [[settlement]] Date of 
Transfer is required for the following Transaction 
Types:  
01 = ACATS 
02 = Free [[DTC]] Deliver Order 
03 = Valued [[DTC]] Deliver Order 

---

## Page 30

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 30 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
04 = Conversion 
05 = Mutual Fund Transfer (non-ACATS) 
06 = Fed 
07 = Physical Movement [[settlement]] 
09 = Non-Domestic Depository 
10 = Other 
26 = [[DWAC]] Deposit 
27 = Certificate Deposit 
28 = [[DRS]] Profile/[[DO]] 
36 = [[DWAC]] Withdrawal 
37 = Withdrawal by Transfer (WT) 
41 = Direct Presentation 
46 = Fund to Firm Mutual Fund Transfer 
51 = Firm to Fund Mutual Fund Transfer 
56 = Networking Transaction 
57 = Manual Mutual Fund Transfer 
58-AIP 
59-Alternative Investment (Non-AIP) 
Format: CCYYMMDD 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 
[[settlement]] Date of 
Transfer 
8 464 471 A/N COND [[settlement]] date of the transfer of the security. 
If the submitted date is not a valid calendar date, CBRS 
rejects the record. May be spaces or valid calendar date. 
Zeroes are not a valid value. 
Required if Transaction Type is 08 = OCC transfer (Non-
ACATS). 
Either Date Transfer was Initiated or [[settlement]] Date of 
Transfer is required for the following Transaction 
Types: 
01 = ACATS 
02 = Free [[DTC]] Deliver Order 

---

## Page 31

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 31 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
03 = Valued [[DTC]] Deliver Order 
04 = Conversion 
05 = Mutual Fund Transfer (non-ACATS) 
06 = Fed 
07 = Physical Movement [[settlement]] 
09 = Non-Domestic Depository 
10 = Other 
26 = [[DWAC]] Deposit 
27 = Certificate Deposit 
28 = [[DRS]] Profile/[[DO]] 
36 = [[DWAC]] Withdrawal 
37 = Withdrawal by Transfer (WT) 
41 = Direct Presentation 
46 = Fund to Firm Mutual Fund Transfer 
51 = Firm to Fund Mutual Fund Transfer 
56 = Networking Transaction 
57 = Manual Mutual Fund Transfer 
58-AIP 
59-Alternative Investment (Non-AIP) 
Format: CCYYMMDD 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 
Position Code  1  472 472 A/N  REQ Values: 
• S = [[short position]] 
• L = Long position 
• B = Borrowed position 
If at least one firm on the record is a [[transfer agent]] or 
transaction type 46, 51, 56, 57, CBRS will set this value to 
L = Long position. Otherwise, if the submitter populates 
this field with anything other than L or S, CBRS rejects the 
record. 
Value B = Borrowed is valid only when Record content 
indicator is 04 = Request record. If this field is populated 

---

## Page 32

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 32 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
with B = Borrowed, and Record content indicator is not 
04 = Request record, CBRS rejects the record. 
Note 
Value B = Borrowed position means that the delivery 
creates a [[short position]] on the submitter’s books. 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be what was populated on the original 
transaction that triggered the need to pass cost basis. 
Filler 131 473 603 A/N REQ Reserved for future use. Spaces.  
Disposition Method 
Used 
(formerly Partial 
Cost Basis 
Indicator) 
2  604 605 A/N  OPT  Indicates the lot disposition method used by the delivering 
firm. The list of valid values does not represent all possible 
standing instructions, but these values are the only valid 
values for CBRS. 
Valid values:  
• 01 = FIFO (First In First Out) 
• 02 = LIFO (Last In First Out) 
• 03 = High Cost 
• 04 = Low Cost 
• 05 = Average Cost  
• 06 = Select Lot 
If this field is populated with an invalid value, CBRS 
spaces out the field and pass the record.  
[[shares]] to Cover 
Short Indicator 
1 606 606 A/N OPT The submitter should populate this field when it receives a 
customer request to deliver [[shares]] to satisfy a short 
position at the receiving firm. The receiving firm will then 
expect cost basis to [[Close Out]] the short. 
Values:  
• Y = Yes 
• N = No 
Best Practice 
If the Record content indicator is 03 = Firm reject 
record, this field should be what was populated on the 
Original [[Asset]] record or Corrected [[Asset]] record 
received. 
If the Record content indicator is 04 = Request record, 
this field should be blank. 

---

## Page 33

CBRS [[Asset]] Input (A)  
DATATRAK SYSID: PROD 36708 / PSE 46708 
[[Asset]] INPUT (A): FIRM REJECT AND REQUEST 33 
COST BASIS [[Asset]] INPUT (A) FIRM REJECT AND REQUEST RECORDS 
DATATRAK SYSID: 36708 Production (46708 Test) 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE: 1/5/2022 
Firm Reject 
Reason Code 
2 607 608 A/N COND Values: 
• 01 = Receiver cannot apply received cost basis 
record 
• 02 = CBRS quantity is greater than delivered quantity 
• 03 = [[CUSIP]] does not belong to [[issuer]]/Transfer 
Agent 
Field is required if Record content indicator is 03 = Firm 
reject record. 
Value 03 = [[CUSIP]] does not belong to [[issuer]]/Transfer 
Agent is valid only when Transaction Type is 36 = 
[[DWAC]] Withdrawal or 37 = Withdrawal by Transfer and 
Record Content Indicator is 03 = Firm reject record.  
If this value is used is used for any other transaction types 
when Record Content Indicator is 03 = Firm reject 
record, CBRS rejects the record. 
If field is populated when Record content indicator is 01 
= Original [[Asset]] record, 02 = Corrected [[Asset]] record, 
or 04 = Request record, CBRS spaces out the field and 
continue to pass the record. 
ACATS [[Asset]] 
Sequence Number 
6 609 614 NUM COND This field should be the ACATS [[Asset]] Sequence Number 
from the original transfer. 
Required when Transaction Type is 01 = ACATS and the 
‘Date Transfer was Initiated’ or the ‘[[settlement]] Date of 
Transfer’ is later than 07/26/2012. Format is 6 digits. Value 
in this field must be numeric and greater than zero. Use 
leading zeros if necessary.  
If Transaction Type is 01 = ACATS and both the ‘Date 
Transfer was Initiated’ and the ‘[[settlement]] Date of 
Transfer’ are equal or prior to 07/26/2012, the field may 
contain spaces, all zeroes, or a valid numeric value. 
Otherwise CBRS rejects the record. 
For all other Transaction Types CBRS spaces out the field 
and pass the record. 
Filler 386 615 1000 A/N REQ Reserved for future use. Spaces.  
 
 

---

## Page 34

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. The services described herein are provided under the “[[DTCC]]” brand name by 
certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  
Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in 
which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they 
offer. 
Doc Date: August 28, 2023 
Publication Code: CBRS149 
Service: Cost Basis Reporting Service (CBRS) 
Title: CBRS [[Asset]] Input (A) - DATATRAK SYSID: PROD 36708 / PSE 46708 
 
 
For More Information 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 