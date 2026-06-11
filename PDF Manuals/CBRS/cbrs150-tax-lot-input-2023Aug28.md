---
title: "CBRS Tax Lot Input (T) - DATATRAK SYSID: PROD 36708 / PSE 46708"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs150-tax-lot-input-2023Aug28.pdf"
pages: 26
size: "493.5 KB"
category: "CBRS"
ingested_on: "2026-06-05"
---

# CBRS Tax Lot Input (T) - DATATRAK SYSID: PROD 36708 / PSE 46708

**Original File:** [cbrs150-tax-lot-input-2023Aug28.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs150-tax-lot-input-2023Aug28.pdf)  
**Category:** CBRS  
**Total Pages:** 26  
**File Size:** 493.5 KB  

---

## Page 1

Cost Basis Reporting Service (CBRS) 
CBRS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
AUGUST 28, 2023 
 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
FIELD NAME  LENG  START END TYPE  OPT/ 
REQ/ 
COND  
COMMENTS  
Record Type  1  1 1 A/N  REQ  Always T. 
 
Rule 
If this field is populated with a value other than T, 
CBRS drops the record as unknown. 
Record Length  4  2 5 NUM  REQ  Always 1000. 
Record Content Indicator 2 6 7 A/N REQ Values: 
• 01 = Original tax lot record. 
• 02 = Corrected tax lot record. 
 
Edit 
If this field on the corresponding [[Asset]] Record is 
02 = Corrected [[Asset]] record, then this field in at 
least one of the accompanying tax lot records must 
have a value of 02 = Corrected tax lot record. 
 
 
 

---

## Page 2

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 2 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
Transaction Type 2 8 9 A/N  REQ  Firm to Firm  
01 = ACATS  
02 = Free [[DTC]] Deliver Order (Non-ACATS) 
03 = Valued [[DTC]] Deliver Order 
04 = Conversion 
05 = Mutual Fund Transfer (Non-ACATS) [change of 
[[Broker]]-dealer] 
06 =Fed  
07 = Physical Movement [[settlement]] (Non-ACATS) 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository (Foreign) 
10 = Other 
11 – 25  = Reserved for future use. 
 
Firm & [[transfer agent]] 
Agent submits/firm receives CBRS 
original/corrected record: 
26 = [[DWAC]] Deposit 
27 = Certificate Deposit 
28 = [[DRS]] Profile/[[DO]] 
29 – 35 Reserved for future use 
 
Firm submits/agent receives CBRS 
original/corrected record: 
36 = [[DWAC]] Withdrawal 
37 = Withdrawal by Transfer (WT) 
38 – 40 Reserved for future use 
 
Either Agent submits/firm receives or Firm 
submits/agent receives CBRS original/corrected 
record: 
41 = Direct Presentation 
42 – 45 = Reserved for future use. 
 
 
 

---

## Page 3

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 3 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
Firm & Fund (In-kind Mutual Fund Transfers): 
Fund submits/firm receives CBRS 
original/corrected record: 
46 = Fund to Firm Mutual Fund Transfer [via ACATS 
Fund/SERV interface; also known as PTF, Position 
Transfer Fund ACATS transfer type] 
47 – 50 Reserved for future use 
Firm submits/fund receives CBRS 
original/corrected record: 
51 = Firm to Fund Mutual Fund Transfer [via ACATS 
Fund/SERV interface; also known as PTF, Position 
Transfer Fund ACATS transfer type] 
52 – 55 = Reserved for future use. 
 
Either fund submits/firm receives or firm 
submits/fund receives CBRS original/corrected 
record: 
56 = Networking Transaction 
57 = Manual Mutual Fund Transfer 
58 – AIP  
59 – Alternative Investment (Non-AIP) 
60 – 65 = Reserved for future use. 
Transfer Control Number  30 10 39 A/N  REQ  Association between the [[Asset]] (A) and the Tax Lot 
(T) records is established when the contents of the 
Control Number of the two records are equal. 
Edit 
If transaction type is 01 = ACATS; this field should 
be the ACATS control number from the original 
transfer. For Transaction Type 01 = ACATS, CBRS 
edits this field to ensure it is a 14-byte numeric 
value. (The format of the ACATS control number is 
CCYYDDDNNNNNNN.)  
Best Practices: 
If transaction type is 02 = Free [[DTC]] Deliver Order 
(Non-ACATS), or 03 = Valued [[DTC]] Deliver Order; 
this field is the IMS Transaction [[ID]] number (16 
bytes) as specified on the original transaction 
processed at [[DTC]]. 
If transaction type is 06 = Fed and the transfer 
occurred at the Fed, this field is the Input Message 
Accountability Data (IMAD) number assigned by the 
Fed to the transfer. 

---

## Page 4

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 4 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
If transaction type is 08 = OCC transfer (Non-
ACATS), this field is the number assigned by the 
OCC to the transfer.  
If transaction type is 26 = [[DWAC]] Deposit, 27 = 
Certificate Deposit, 28 = [[DRS]] Profile/[[DO]], 36 = 
[[DWAC]] Withdrawal, 37 = Withdrawal by Transfer 
(WT); this field contains a reference [[ID]] number 
whose values and number of bytes changes 
depending on the original transaction processed at 
[[DTC]]. 
If transaction type is 41 = Direct Presentation; this 
field is 26 characters: 
• Julian Date (3 bytes: DDD) + [[participant]] Number 
(5 bytes) + Customer Account Number (18 
bytes) 
If transaction type is 46 = Fund to Firm Mutual 
Fund Transfer or 51 = Firm to Fund Mutual Fund 
Transfer; this field is the FundSERV control 
number. Firms should use the Fund/SERV Control # 
from the ACATS Fund/SERV Statistics File, and add 
the letters CATS to the front of it, to match the 
number that Funds should provide in this field. 
If transaction type is 56 = Networking Transaction, 
then the control number is the Networking control 
number. 
For all other transaction types, 04 = Conversion, 05 
= Mutual Fund Transfer (Non-ACATS), 06 = Other 
Depository Deliveries, 07 = Physical Movement 
[[settlement]], 57 = Manual Mutual Fund Transfer; 
this field is the control number agreed upon by the 
contraparties involved in the original [[securities]] 
transaction. 
Alternate Control Number 30 40 69 A/N COND Required field if Transaction Type is one of the 
following and the submitted value must be greater 
than spaces: 
• 46 = Fund to Firm Mutual Fund Transfer 
• 51 = Firm to Fund Mutual Fund Transfer 
• 58 = AIP  
Optional field for all other transaction types. 
Best Practice 
For Transaction Types 46 = Fund to Firm Mutual 
Fund Transfer or 51 = Firm to Fund Mutual Fund 
Transfer, populate this field with the ACATS Control 
Number. 

---

## Page 5

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 5 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
For Transaction Type 58 AIP, populate this field 
with the AIP SIN Number ([[NSCC]] Security 
Identifier). 
Filler 20 70 89 A/N REQ Reserved for future use. Spaces. 
Contra Firm Number  8 90 97 A/N  COND Populate this field with the number for the firm who 
is receiving the CBRS record. 
Use leading zeros   If a firm has a [[DTC]], [[NSCC]], or 
[[transfer agent]] Number, populate this field with that 
number. If the firm’s only identifying number is the 
CBRS Account Number, populate this field with that 
number. 
Rules for transaction types 36 = [[DWAC]] Withdrawal 
or 37 = Withdrawal by Transfer (WT) are as 
follows: 
• For transaction types 36 = [[DWAC]] Withdrawal 
or 37 = Withdrawal by Transfer (WT) where the 
security is an unsponsored [[ADR]], CBRS cannot 
[[Locate]] the [[transfer agent]] number on the [[DTC]] 
security master file. In these cases, the submitter 
must populate this field. If the submitter leaves 
this field blank in these cases, CBRS rejects the 
record. 
• For all other [[securities]], if Transaction Type is 36 
= [[DWAC]] Withdrawal or 37 = Withdrawal by 
Transfer (WT); then field would be left blank as 
CBRS performs a lookup of Receiver Firm 
Number on the [[DTC]] security master file based 
upon [[CUSIP]]. 
• When Record content indicator is 01 = Original 
[[Asset]] record, and the submitter populates this 
field, CBRS overwrites the submitter’s value with 
the value it finds on the [[DTC]] security master file. 
• When Record content indicator is 02 = Corrected 
[[Asset]] record, and the submitter populates this 
field, CBRS accepts the submitter’s value. 
Required field for all other transaction types. 
Filler 2 98 99 A/N REQ Reserved for future use. Spaces. 
Contra Firm Type 6 100 105 A/N REQ Populate this field with the type of firm who is 
receiving the CBRS record. This type corresponds 
to the type of number in the Contra Firm Number 
field.  
Values: 
• AGTNBR = [[transfer agent]] 
• CBRACT = CBRS User 

---

## Page 6

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 6 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
• DTCPRT = [[DTC]] [[participant]] 
• NSCPRT = [[NSCC]] [[participant]] 
More values possible in future enhancements. 
Edit 
If Transaction Type is, 01 = ACATS, 02 = Free [[DTC]] 
Deliver Order, 03 = Valued [[DTC]] Deliver Order, 04 
= Conversion, 05 = Mutual Fund Transfer (non-
ACATS), 06 = Fed, 07 = Physical Movement 
[[settlement]], 08 = OCC transfer (Non-ACATS), 09 = 
Non-Domestic Depository; 10 = Other, the Contra 
Firm Type must be NSCPRT = [[NSCC]] [[participant]], 
DTCPRT = [[DTC]] [[participant]], or CBRACT = CBRS 
User. 
If Transaction Type is, 26 = [[DWAC]] Deposit, 27 = 
Certificate Deposit, 28 = [[DRS]] Profile/[[DO]]; this field 
must be DTCPRT = [[DTC]] [[participant]], 
If Transaction Type is 36 = [[DWAC]] Withdrawal, 37 
= Withdrawal by Transfer (WT); then this field 
must be AGTNBR = [[transfer agent]]. 
If Transaction Type is 41= Direct Presentation; 
then this field must be AGTNBR = [[transfer agent]] 
or CBRACT = CBRS User or DTCPRT = [[DTC]] 
[[participant]]. 
If Transaction Type is 46 = Fund to Firm Mutual 
Fund Transfer, this field must be DTCPRT = [[DTC]] 
[[participant]] or NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 51 = Firm to Fund 
Mutual Fund Transfer, this field must be DTCPRT 
= [[DTC]] [[participant]] or NSCPRT = [[NSCC]] 
[[participant]]. 
If the Transaction Type is 56 = Networking 
Transaction, this field must be DTCPRT = [[DTC]] 
[[participant]] or NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 57 = Manual Mutual 
Fund Transfer, 58 – AIP, 59 – Alternative 
Investment (Non-AIP); this field must be CBRACT 
= CBRS User, DTCPRT = [[DTC]] [[participant]], or 
NSCPRT = [[NSCC]] [[participant]]. 
Filler 10 106 115 A/N REQ Reserved for future use. Spaces. 
Submitting Firm Number  8 116 123 A/N  REQ  Populate this field with the number of the firm who is 
submitting the CBRS record. Use leading zeros. If a 
firm has a [[DTC]], [[NSCC]], or [[transfer agent]] Number, 
populate this field with that number. If the firm’s only 
identifying number is the CBRS Account Number, 
populate this field with that number. 

---

## Page 7

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 7 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
Filler 2 124 125 A/N REQ Reserved for future use. Spaces. 
Submitting Firm Type 6 126 131 A/N REQ Populate this field with the type of the firm who is 
submitting the CBRS record. This type corresponds 
to the type of number in the Submitting Firm 
Number field.  
Values: 
• AGTNBR = [[transfer agent]] 
• CBRACT = CBRS User 
• DTCPRT = [[DTC]] [[participant]] 
• NSCPRT = [[NSCC]] [[participant]] 
More values possible in future enhancements. 
Edit 
If Transaction Type is, 01 = ACATS 02 = Free [[DTC]] 
Deliver Order, 03 = Valued [[DTC]] Deliver Order, 04 
= Conversion, 05 = Mutual Fund Transfer (non-
ACATS), 06 = Fed, 07 = Physical Movement 
[[settlement]], 08 = OCC transfer (Non-ACATS), 09 = 
Non-Domestic Depository; 10 = Other, then the 
Submitting Firm Type must be NSCPRT = [[NSCC]] 
[[participant]], DTCPRT = [[DTC]] [[participant]], or 
CBRACT = CBRS User. 
If Transaction Type is 26 = [[DWAC]] Deposit, 27 = 
Certificate Deposit, 28 = [[DRS]] Profile/[[DO]]; the 
Submitting Firm Type must be AGTNBR = Transfer 
Agent, CBRACT=CBRS User, DTCPRT=[[DTC]] 
[[participant]], NSCPRT=[[NSCC]] [[participant]]. 
If Transaction Type is, 36 = [[DWAC]] Withdrawal, 37 
= Withdrawal by Transfer (WT); the Submitting 
Firm Type must be DTCPRT = [[DTC]] [[participant]], 
CBRACT=CBRS User, NSCPRT=[[NSCC]] 
[[participant]]. 
If Transaction Type is 41= Direct Presentation; the 
Submitting Firm Type must be AGTNBR = 
[[transfer agent]] or CBRACT = CBRS User or 
DTCPRT = [[DTC]] [[participant]]. 
If Transaction Type is 46 = Fund to Firm Mutual 
Fund Transfer, this field must be DTCPRT = [[DTC]] 
[[participant]] or NSCPRT = [[NSCC]] [[participant]]. 
If the Transaction Type is 51 = Firm to Fund 
Mutual Fund Transfer, this field must be DTCPRT 
= [[DTC]] [[participant]] or NSCPRT = [[NSCC]] 
[[participant]]. 
If the Transaction Type is 56 = Networking 
Transaction, this field must be DTCPRT = [[DTC]] 
[[participant]] or NSCPRT = [[NSCC]] [[participant]]. 

---

## Page 8

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 8 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
If the Transaction Type is 57 = Manual Mutual 
Fund Transfer, 58-AIP, 59-Alternative Investment 
(Non-AIP) this field must be CBRACT = CBRS 
User, DTCPRT = [[DTC]] [[participant]], or NSCPRT = 
[[NSCC]] [[participant]]. 
Filler 18 132 149 A/N REQ Reserved for future use. Spaces. 
Receiver 
Customer Account Number  
20  150 169 A/N  COND  Populate this field with the customer account 
number at the firm that received the [[Asset]] transfer. 
Required field for Transaction Types  
01 = ACATS 
02 = Free [[DTC]] Deliver Order (Non-ACATS) 
03 = Valued [[DTC]] Deliver Order 
05 = Mutual Fund Transfer (Non-ACATS) 
06 = FED 
07 = Physical Movement [[settlement]] 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository 
10 = Other 
46 = Fund to Firm Mutual Fund Transfer 
51 = Firm to Fund Mutual Fund Transfer 
56 = Networking Transaction 
57 = Manual Mutual Fund Transfer 
58-AIP 
59-Alternative Investment (Non-AIP) 
Optional field for all other Transaction Types. 
Filler 10 170 179 A/N REQ Reserved for future use. Spaces. 
Deliverer Customer 
Account 
Number  
20  180 199 A/N  COND  Populate this field with the customer account 
number at the firm that delivered the [[Asset]] transfer. 
Required field for Transaction Types  
01 = ACATS 
02 = Free [[DTC]] Deliver Order (Non-ACATS) 
03 = Valued [[DTC]] Deliver Order 
04 = Conversions 
05 = Mutual Fund Transfer (Non-ACATS) 
06 = Fed 
07 = Physical Movement [[settlement]] 

---

## Page 9

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 9 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
08 = OCC transfer (Non-ACATS) 
09 = Non-Domestic Depository 
10 = Other 
46 = Fund to Firm Mutual Fund Transfer 
51 = Firm to Fund Mutual Fund Transfer 
56 = Networking Transaction 
57 = Manual Mutual Fund Transfer 
58-AIP 
59-Alternative Investment (Non-AIP). 
 
Optional field for all other Transaction Types. 
 
Best Practices 
The submitter should populate this field for 
Transaction Type. 
04 = Conversion 
Filler 10 200 209 A/N REQ Reserved for future use. Spaces. 
ISIN Country Code  2  210 211 A/N  COND  [[default]] value is US. 
Not required if [[Asset]] Category = OPT. 
Required for all Transaction Types except 41 = 
Direct Presentation. 
Edit 
Association between the [[Asset]] (A) and the Tax Lot 
(T) records is established when the contents of ISIN 
Country Code combined with ISIN Security Issue [[ID]] 
and ISIN Security Check Digit of the two records are 
equal.  
ISIN Security 
Issue [[ID]] ([[CUSIP]] number) 
9  212 220 A/N  
COND  Required field if [[Asset]] Category is not OPT. 
Required for all Transaction Types except 41 = 
Direct Presentation. 
If both ISIN Security Issue [[ID]] and [[Asset]] 
Description fields are left blank, CBRS rejects the 
record. 
Edit 
Association between the [[Asset]] (A) and the Tax Lot 
(T) records is established when the contents of ISIN 
Security Issue [[ID]] combined with ISIN Country Code 
and ISIN Security Check Digit of the two records are 
equal.  

---

## Page 10

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 10 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
ISIN Security Check Digit  1  221 221 A/N  COND  Required field if ISIN Country Code is anything but 
blank or US, and ISIN Security Issue [[ID]] ([[CUSIP]] 
number) is populated. 
Edit 
Association between the [[Asset]] (A) and the Tax Lot 
(T) records is established when the contents of ISIN 
Security Check Digit combined with ISIN Country 
Code and ISIN Issue [[ID]] of the two records are 
equal.  
Filler 10 222 231 A/N REQ Reserved for future use. Spaces. 
Put/Call Indicator 1 232 232 A/N COND Values: 
• C = Call  
• P = Put 
Allowed for Transaction Types 01 = ACATS, 04 = 
Conversion, 06 = Fed, 08 = OCC transfer (Non-
ACATS); 09 = Non-Domestic Depository; 10 = 
Other. If this field is populated for any other 
transaction type, CBRS rejects the record. 
Required field if [[Asset]] Category = OPT. 
Edit 
Association between the [[Asset]] (A) and the Tax Lot 
(T) records is established when the contents of 
[[Option]] Symbol combined with Put-Call Indicator, 
[[Option]] Expiration Date, [[Option]] Strike Price Integer, 
and [[Option]] Strike Price Decimal of the two records 
are equal. 
[[Option]] Symbol  6  233 238 A/N  COND  Allowed for Transaction Types 01 = ACATS, 04 = 
Conversion, 06 = Fed, 08 = OCC transfer (Non-
ACATS); 09 = Non-Domestic Depository; 10 = 
Other. If this field is populated for any other 
transaction type, CBRS rejects the record. 
Required field if [[Asset]] Category = OPT. 
Edit 
Association between the [[Asset]] (A) and the Tax Lot 
(T) records is established when the contents of 
[[Option]] Symbol combined with Put-Call Indicator, 
[[Option]] Expiration Date, [[Option]] Strike Price Integer, 
and [[Option]] Strike Price Decimal of the two records 
are equal. 
 
 
 

---

## Page 11

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 11 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
[[Option]] Expiration Date 
–or–
Last Factor Date (for MBS)
8 239 246 A/N COND • [[Option]] Expiration Date
Allowed for Transaction Types:
01 = ACATS
04 = Conversion
06 = Fed
08 = OCC transfer (Non-ACATS)
09 = Non-Domestic Depository
10 = Other
If this field is populated for any other transaction
type, CBRS rejects the record.
Required field if [[Asset]] Category = OPT.
–or–
• Last Factor Date
When the [[Asset]] Category field is set to 
MBS = Mortgage Backed [[securities]], you 
can repurpose this field to input the last 
factor date. When using this field for the 
last factor information, you must input the 
same date value in both the [[Asset]] (A) 
and also this Tax Lot (T) records.
Edits 
Association between the [[Asset]] (A) and the Tax Lot 
(T) records is established when the contents of
[[Option]] Symbol combined with Put-Call Indicator,
[[Option]] Expiration Date, [[Option]] Strike Price Integer,
and [[Option]] Strike Price Decimal of the two records
are equal.
Format: CCYYMMDD 
If submitted date is not a valid calendar date, CBRS 
rejects the record. May be spaces or valid calendar 
date. Zeroes are not a valid value. 
[[Option]] Strike Price Integer 5 247 251 NUM COND Allowed for Transaction Types: 
• 01 = ACATS
• 04 = Conversion
• 06 = Fed
• 08 = OCC transfer (Non-ACATS)
• 09 = Non-Domestic Depository
• 10 = Other
If this field is populated for any other transaction 
type, CBRS rejects the record. 
Required field if [[Asset]] Category = OPT. 

---

## Page 12

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 12 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
Edit 
Association between the [[Asset]] (A) and the Tax Lot 
(T) records is established when the contents of 
[[Option]] Symbol combined with Put-Call Indicator, 
[[Option]] Expiration Date, [[Option]] Strike Price Integer, 
and [[Option]] Strike Price Decimal of the two records 
are equal. 
[[Option]] Strike Price Decimal  3 252 254 NUM COND  Allowed for Transaction Types: 
• 01 = ACATS 
• 04 = Conversion 
• 06 = Fed 
• 08 = OCC transfer (Non-ACATS) 
• 09 = Non-Domestic Depository 
• 10 = Other 
If this field is populated for any other transaction 
type, CBRS rejects the record. 
Required field if [[Asset]] Category = OPT. 
Edit 
Association between the [[Asset]] (A) and the Tax Lot 
(T) records is established when the contents of 
[[Option]] Symbol combined with Put-Call Indicator, 
[[Option]] Expiration Date, [[Option]] Strike Price Integer, 
and [[Option]] Strike Price Decimal of the two records 
are equal. 
The only valid values are 000 through 999, which 
represent decimal format only. 
[[Asset]] Description  140  255 394 A/N  COND  Contains a text-based description of the [[Asset]].  
Required field when Transaction Type is 41 = 
Direct Presentation. 
If this field is blank, ISIN Security Issue [[ID]] is 
populated, and CBRS cannot find the ISIN Security 
Issue [[ID]] in its master file, CBRS rejects the record. 
If this field is populated, ISIN Security Issue [[ID]] is 
populated, and CBRS cannot find the ISIN Security 
Issue [[ID]] in its master file, CBRS passes the record 
and add the words, “Submitter ISIN” to the end of 
this field. 
If both ISIN Security Issue [[ID]] and [[Asset]] 
Description fields are left blank, CBRS rejects the 
record 
Edit 
Association between the [[Asset]] (A) and the Tax Lot 
(T) records is established when the contents of this 

---

## Page 13

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 13 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
field are equal, only when ISIN Security Issue [[ID]] is 
blank, and [[Asset]] Category is not OPT. 
Best Practice 
Populate [[Asset]] Description field at all times. 
Certificate Number Prefix 8 395 402 A/N OPT Physical certificate number prefix that corresponds 
to the tax lot. 
Applicable for Transaction Types 27 = Certificate 
Deposit and 41 = Direct Presentation. 
If field is populated for any other transaction type, 
CBRS spaces out the field and pass the record. 
Certificate Number 12 403 414 A/N COND Physical certificate number that corresponds to the 
tax lot. 
Use leading zeros. 
Required for Transaction Type 27 = Certificate 
Deposit. 
Required for Transaction Type 41 = Direct 
Presentation, when the submitter is Submitting 
Firm Type AGTNBR = [[transfer agent]] or CBRACT 
= CBRS User. 
If field is populated for any other transaction type, 
CBRS spaces out the field and pass the record. 
If field is left blank when Transaction Type is 27 = 
Certificate Deposit or 41 = Direct Presentation, 
CBRS rejects the record. 
Filler 12 415 426 A/N REQ Reserved for future use. Spaces. 
Noncovered / 
Pending Indicator 
2 427 428 A/N COND Should be used when the basis is unknown, 
unverifiable, or pending.  
Values: 
• 01 = Noncovered lot 
• 02 = Noncovered account 
• 03 = Pending 
• 04 = Certificate in Customer Name 
Required field if Acquisition Date field is blank. 
Otherwise, CBRS rejects the record. 
Best Practice 
If field is left blank, the receiver will consider the lot 
covered if the Position Code is L = Long. If the 
Position Code is S = Short, the covered status of 
the position is not determined until the [[shares]] are 
acquired. 

---

## Page 14

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 14 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
Taxes Reported by 
[[issuer]]/[[transfer agent]] 
1 429 429 A/N OPT If the submitting firm is an [[issuer]] or [[transfer agent]], 
and has reported the tax results of a cash reorg 
event to the IRS for this lot, populate this field with Y 
= Yes. 
Values: 
• Y = Yes 
• N = No 
 
If a value is provided in this field, the Submitting 
Firm Type must be equal to AGTNBR; otherwise, 
CBRS rejects the record. 
Filler 9 430 438 A/N REQ Reserved for future use. Spaces. 
Gifted or Inherited Indicator 2 439 440 A/N COND Values: 
• 01 = Gifted 
• 02 = Inherited 
• 03 = Inherited then Gifted 
If submitter populates this field with a value other 
than 01 = Gifted or 
02 = Inherited or 03 = Inherited 
then Gifted or spaces, CBRS rejects the record. 
 
If Date of Gift is populated and this field is 
populated with a value other than 01 = Gifted or 03 
= Inherited then Gifted, CBRS rejects the record. 
 
If Fair Market Value as of Date of Gift is populated 
and this field is populated with a value other than 01 
= Gifted or 03 = Inherited then Gifted, CBRS 
rejects the record. 
Date of Gift 8 441 448 A/N COND Required field if Fair Market Value as of Date of 
Gift is populated. Otherwise, CBRS rejects the 
record. 
Format: CCYYMMDD 
CBRS rejects the record if the submitted date is not 
a valid calendar date. May be spaces or valid 
calendar date. Zeroes are not a valid value. 
Filler 10 449 458 A/N REQ Reserved for future use. Spaces.  
Fair Market Value as of Date 
of Gift 
17 459 475 A/N OPT Fair market value of tax lot as of date of gift, 
represented as total cost.  
Valid values include zeroes. The position of the 
decimal is denoted by a comma (,). Up to two 

---

## Page 15

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 15 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
decimal places are supported before truncation 
occurs. 
Best Practice 
Must be populated if known for a gifted security. 
Exchange Rate for FMV as 
of Date of Gift 
19 476 494 A/N COND Spot exchange rate used to convert the Fair Market 
Value as of Date of Gift as of the Date of Gift. Rate 
is the amount of local currency equal to one dollar. 
For example, if ISO Currency Code = JPY, the value 
in this field is 86.4428 for acquisition date 
12/01/2009. 
Required field if ISO Currency Code is not USD 
and Fair Market Value as of Date of Gift is 
populated. 
Leave this field blank if ISO Currency Code = USD. 
If ISO Currency Code = USD and submitter 
populates this field with anything but a blank value, 
CBRS rejects the record. 
If Fair Market Value as of Date of Gift field is blank, 
and this field is populated, CBRS rejects the record. 
The position of the decimal is denoted by a comma 
(,). Format is 9 digits to the left of the decimal and 9 
digits to the right of the decimal. Use leading zeros if 
necessary.  
Filler 1 495 495 A/N REQ Reserved for future use. Spaces. 
Tax Lot Quantity  17 496 512 A/N  REQ  The quantity of the transferred tax lot. 
Zero is not a valid value for this field. 
CBRS sums up the tax lot quantities and compare 
them to the value populated in Total Position 
Quantity field on the [[Asset]] record. If the sum of the 
tax lot quantities does not equal the value in the 
Total Position Quantity, CBRS rejects the record. 
The position of the decimal is denoted by a comma 
(,). Up to four decimal places are supported before 
truncation occurs. 
Filler 10 513 522 A/N REQ Reserved for future use. Spaces. 
Position Code  1  523 523 A/N  REQ Values: 
• L = Long position  
• S = [[short position]] 
If at least one firm on the record is a [[transfer agent]] 
or transaction type 46, 51, 56, 57, CBRS sets this 
value to L = Long position. Otherwise, if the 

---

## Page 16

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 16 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
submitter populates this field with anything other 
than L or S, CBRS rejects the record. 
Best Practice: 
Transfer agents and [[Mutual Funds]] [[default]] to  
L = Long position. 
Filler 10 524 533 A/N REQ Reserved for future use. Spaces. 
Acquisition Date of Tax Lot 8  534 541 A/N  COND Trade or acquisition date of the security. For lots 
affected by wash sales, this is the adjusted 
acquisition date. This date is used to determine gain 
or loss, and short term or long term holding period. 
Required field unless the Zero Basis Indicator is 
02 = Unknown. If this field is populated and the 
Zero Basis Indicator is 02 = Unknown, CBRS 
rejects the record. 
If this field is blank, Noncovered/Pending Indicator 
field must be populated.  
This date must be equal to or earlier than the date in 
the Original Acquisition Date for Wash Sale 
Adjustment field. Otherwise, CBRS rejects the 
record.  
Format: CCYYMMDD  
If submitted date is not a valid calendar date, or is in 
the future, CBRS rejects the record. Zeroes are not 
a valid value. 
19010101 is a valid value and signifies various 
dates. 
Original Acquisition Date for 
Wash Sale Adjustment 
8 542 549 A/N OPT Used only for wash sales. Date of the original trade 
date for a lot that has been adjusted for wash sales. 
Format: CCYYMMDD 
 
If submitted date is not a valid calendar date, CBRS 
rejects the record. May be spaces or valid calendar 
date. Zeroes are not a valid value. 
Best Practice: 
Must be populated if the tax lot is the result of a 
wash sale. 
Wash Sale Adjustment 
Amount 
17 550 566 A/N COND (A.K.A. Disallowance amount) - Used only for 
wash sales. Amount in USD of the disallowed loss 
from a wash sale, which has been added to the cost 
basis. 
 

---

## Page 17

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 17 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
This field should be greater than zero if the Original 
Acquisition Date for Wash Sale Adjustment is 
populated. If this field is populated and Original 
Acquisition Date for Wash Sale Adjustment is blank, 
CBRS rejects the record. 
If a Wash Sale occurred on a fixed income product 
(CDCP, CORP, GOVT, MUNI, MBS, or ZERO), then 
both the Wash Sale Adjustment Amount and the 
Original Acquisition Date for Wash Sale Adjustment 
are required to be populated if the tax lot is covered. 
If Original Acquisition Date for Wash Sale 
Adjustment is populated and this field is populated 
for any other [[Asset]] Category, CBRS passes the 
record. 
If Original Acquisition Date for Wash Sale 
Adjustment is not populated, the Wash Sale Amount 
should be blank. (zero can be accepted in place of 
blank.) In this case, CBRS populates this field with 
zeroes and pass the record. 
In the case of blank value, CBRS populates this field 
with zeroes and pass the record. 
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
 
Best Practice: 
• Fixed income [[securities]] should not be 
adjusted for the disallowed loss, resulting 
from a wash sale on the current cost 
basis. 
• For all other security types, the original 
and current cost basis should be adjusted 
for the disallowed amount. 
Filler 3 567 569 A/N REQ Reserved for future use. Spaces. 
ISO Currency Code  3  570 572 A/N  REQ  Note: There is no system [[default]]. The submitter 
must populate this field. 
 
Valid values for this field are the standard ISO 
Currency Codes, such as USD, CAD, JPY.  
 
If the populated value is not USD, the ISO Currency 
Code is the currency corresponding to the value in 
the Exchange Rate field.  

---

## Page 18

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 18 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
Exchange Rate 
–or– 
Last Factor (for MBS) 
19 573 591 A/N COND • Exchange Rate 
Spot exchange rate used when converting the 
Tax Lot Current Cost. Rate is the amount of local 
currency equal to one dollar. For example, if ISO 
Currency Code = JPY, the value in this field is 
86.4428 for acquisition date 12/01/2009. 
Required field if ISO Currency Code is not 
USD. 
Leave this field blank if ISO Currency Code = 
USD. If ISO Currency Code = USD and 
submitter populates this field with anything but a 
blank value, CBRS rejects the record. 
–or– 
• Last Factor 
When the [[Asset]] Category field is set to MBS = 
Mortgage Backed [[securities]], you can 
repurpose this field to input the last factor.  
The position of the decimal is denoted by a comma 
(,). Format is 9 digits to the left of the decimal and 9 
digits to the right of the decimal. Use leading zeros if 
necessary.  
Filler 20 592 611 A/N REQ Reserved for future use. Spaces. 
Tax Lot Original Cost 17  612 628 A/N  COND Total original cost, in USD, of the tax lot. This value 
should be the cost of the security the day it was 
acquired. 
For equities, this value should be adjusted for wash 
sales. For covered fixed income [[securities]], this 
value should not be adjusted for wash sales. 
 
Required field if A Covered [[Asset]] and the [[Asset]] 
Category is: 
CDCP = CD or Commercial Paper 
CORP = Corporate Bond 
FDEB = Foreign Debt 
GOVT = US Govt. and Govt. Agency 
MBS = Mortgage Backed [[securities]] 
MUNI = Municipal [[Bonds]] 
ZERO = Zero Coupon [[Bonds]] 
and Non-covered/ Pending Indicator is blank, unless 
Zero Basis Indicator is 02 = Unknown. 
Valid values include zeroes. A blank value is 
allowed when Tax Lot Original Cost is unknown. In 

---

## Page 19

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 19 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
this case, CBRS populates this field with zeroes and 
pass the record. 
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
Best Practice 
Include Total Original Cost for [[Asset]] Backed 
[[securities]]. 
Filler 20 629 648 A/N REQ Reserved for future use. Spaces. 
Tax Lot Current Cost 17 649 665 A/N  COND This value should be in USD. The current cost 
should be adjusted for wash sales when the [[Asset]] is 
not a fixed income security. For fixed income 
[[securities]], the current cost should be modified as of 
the [[settlement]] date of the transfer for: corporate 
actions, return of principal, OID, 
accretion/amortization, etc.  
Required field unless [[Asset]] Category = MBS or 
Zero Basis Indicator is 02 = Unknown.   
If [[Asset]] Category is set to MBS = Mortgage Backed 
[[securities]] and this field is populated, CBRS passes 
the record. If this field is populated and Zero Basis 
Indicator is 02 = Unknown, CBRS rejects the record. 
Valid values include zeroes or blanks. A blank value 
is allowed when Tax Lot Current Cost is unknown. 
In this case, CBRS populates this field with zeroes 
and pass the record. 
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
Best Practices 
If Position Code is S = Short and the security is 
covered by the legislation, this field should equal the 
gross proceeds of the [[short position]]. 
For a non-covered average cost mutual fund 
position with at least one lot with unknown basis, 
populate this field with the actual current cost for 
each lot with known basis. 
Include adjusted cost for Fixed Income [[securities]] 
other than [[Asset]] Backed [[securities]]. 
Tax Lot Current Cost should be populated for 
Section 1256 options with Acquisition Basis. 
Filler 20 666 685 A/N REQ Reserved for future use. Spaces. 

---

## Page 20

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 20 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
Zero Basis Indicator 2 686 687 A/N COND Required field if Tax Lot Current Cost is zero or 
blank. 
Values: 
• 01 = True Zero 
• 02 = Unknown 
If Tax Lot Current Cost is populated with spaces, 
this field must be 02 = Unknown. Otherwise, CBRS 
rejects the record. 
If Tax Lot Current Cost is zero and this field is 
blank, CBRS rejects the record. 
If Tax Lot Current Cost is greater than zero and 
this field is populated, CBRS rejects the record. 
If either Covered, or the Non-covered/ Pending 
Indicator is blank, and this field is 02 = Unknown, 
then CBRS rejects the record. 
Tax Lot Original 
Unit Price  
17  688 704 A/N  OPT The per share price, in USD, of the original trade. 
Valid values include zeroes. A blank value is 
allowed when Tax Lot Original Unit Price is 
unknown. 
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
Best Practice 
Should only populate this field for a mortgage-
backed security. 
Filler 20 705 724 A/N REQ Reserved for future use. Spaces. 
Employee Plan [[shares]] 
Indicator 
2 725 726 A/N OPT Values: 
• 01 = Qualified Employee [[Stock]] Purchase Plan 
• 02 = Incentive [[Stock]] [[Option]] Plan 
Best Practice 
If this field is populated, a third party—not the 
submitter—should provide the cost basis for the tax 
lot. 
Accrue Market Discount 
Election 
1 727 727 A/N 
COND Election to accrue market discount using a constant 
yield.  
Values: 
• Y = Yes 
• N = No 
Required field if [[Asset]] Category is CORP = 
Corporate Bond, GOVT = US Govt. and Govt. 

---

## Page 21

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 21 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
Agency, MUNI = Municipal [[Bonds]], or ZERO = Zero 
Coupon [[Bonds]] and Non-covered/ Pending Indicator 
is blank. If this field is populated for CDCP, CORP, 
FDEB, GOVT, MUNI, or ZERO and Non-
covered/Pending Indicator is populated, CBRS 
passes the record. If this field is populated for [[Asset]] 
Category is MBS = Mortgage Backed [[securities]], 
CBRS passes the record. If this field is populated for 
any other [[Asset]] Category, CBRS rejects the record.  
Include Market Discount in 
Income Election 
1 728 728 A/N COND Election to include market discount in income 
currently. 
Values: 
• Y = Yes 
• N = No 
Required field if [[Asset]] Category is CORP = 
Corporate Bond, GOVT = US Govt. and Govt. 
Agency, MUNI = Municipal [[Bonds]], or ZERO = Zero 
Coupon [[Bonds]] and Non-covered/Pending Indicator 
is blank. If this field is populated for CDCP, CORP, 
FDEB, GOVT, MUNI, or ZERO and Non-
covered/Pending Indicator is populated, CBRS 
passes the record. If this field is populated for [[Asset]] 
Category is MBS = Mortgage Backed [[securities]] , 
CBRS passes the record. If this field is populated for 
any other [[Asset]] Category, CBRS rejects the record.  
Filler 1 729 729 A/N REQ Reserved for future use. Spaces. 
Amortize [[Premium]] Election 1 730 730 A/N COND Election to amortize [[Premium]]. 
Values: 
• Y = Yes (Means the client has been amortizing 
the [[Premium]]) 
• N = No (Means the client elected not to 
amortize the [[Premium]]) 
Required field if [[Asset]] Category is CORP = 
Corporate Bond, GOVT = US Govt. and Govt. 
Agency, MUNI = Municipal [[Bonds]], or ZERO = Zero 
Coupon [[Bonds]] and Non-covered / Pending Indicator 
is blank. If this field is populated for CDCP, CORP, 
FDEB, GOVT, MUNI, or ZERO and Non-covered / 
Pending Indicator is populated, CBRS passes the 
record. If this field is populated for [[Asset]] Category 
MBS = Mortgage Backed [[securities]], CBRS passes 
the record. If this field is populated for any other 
[[Asset]] Category, CBRS rejects the record.  
Spot Rate Election 1 731 731 A/N COND Spot rate election for interest accruals regarding a 
covered debt instrument denominated in a currency 
other than U.S. Dollar. 

---

## Page 22

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 22 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
Values: 
• Y = Yes 
• N = No 
Required field if [[Asset]] Category is CORP = 
Corporate Bond, GOVT = US Govt. and Govt. 
Agency, MUNI = Municipal [[Bonds]], or ZERO = Zero 
Coupon [[Bonds]] and Non-covered/Pending Indicator 
is blank. If this field is populated for CDCP, CORP, 
FDEB, GOVT, MUNI, or ZERO and Non-
covered/Pending Indicator is populated, CBRS 
passes the record. If this field is populated for [[Asset]] 
Category MBS = Mortgage Backed [[securities]], 
CBRS passes the record. If this field is populated for 
any other [[Asset]] Category, CBRS rejects the record.  
Filler 2 732 733 A/N REQ Reserved for future use. Spaces. 
Purchase / [[Dividend]] 
Reinvestment Indicator  
1  734 734 A/N  OPT  
• P = Purchase ([[default]]) 
• R = Reinvestment 
Market Discount 17 735 751 A/N  OPT  Allowed for [[Asset]] Categories CDCP, CORP, FDEB, 
GOVT, MBS, MUNI, or ZERO. If this field is 
populated for any other [[Asset]] Category, CBRS 
rejects the record. 
Valid values include zeroes. A blank value is 
allowed when Market Discount is unknown or not 
applicable. In this case, CBRS populates this field 
with zeroes and pass the record.  
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
Bond [[Premium]] 17 752 768 A/N  OPT  Allowed for [[Asset]] Categories CDCP, CORP, FDEB, 
GOVT, MBS, MUNI, or ZERO. If this field is 
populated for any other [[Asset]] Category, CBRS 
rejects the record. 
Valid values include zeroes. A blank value is 
allowed when Bond [[Premium]] is unknown or not 
applicable. In this case, CBRS populates this field 
with zeroes and pass the record.  
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
Best Practice: 
Bond [[Premium]] varies depending on how the 
Amortization [[Premium]] Election was populated.  
If yes, the amount of the bond [[Premium]] reported 
should be as of the last interest payment (coupon) 
date. 

---

## Page 23

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 23 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
If no, the bond [[Premium]] field should be zero. 
Acquisition [[Premium]] 17 769 785 A/N  OPT  Allowed for [[Asset]] Categories CDCP, CORP, FDEB, 
GOVT, MBS, MUNI, or ZERO. If this field is 
populated for any other [[Asset]] Category, CBRS 
rejects the record. 
Valid values include zeroes. A blank value is 
allowed when Acquisition [[Premium]] is unknown or 
not applicable. In this case, CBRS populates this 
field with zeroes and pass the record.  
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
Best Practice: 
Acquisition [[Premium]] must be adjusted daily, and the 
amount reported on CBRS should be as of the 
[[settlement]] date of the transfer. 
Accrued OID 17 786 802 A/N  OPT  Allowed for [[Asset]] Categories CDCP, CORP, FDEB, 
GOVT, MBS, MUNI, or ZERO. If this field is 
populated for any other [[Asset]] Category, CBRS 
rejects the record. 
Valid values include zeroes. A blank value is 
allowed when Accrued OID is unknown or not 
applicable. In this case, CBRS populates this field 
with zeroes and pass the record.  
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
Last Adjustment Date 8 803 810 A/N COND Date of last interest accrual for purposes of 
calculating the current cost of a fixed income 
security.  
Required field for covered fixed income assets 
submissions. 
Allowed field for [[Asset]] Category:   
CDCP = CD or Commercial Paper 
CORP = Corp Bond 
FDEB = Foreign Debt 
GOVT = US Govt. and Govt. Agency 
MBS = Mortgage Backed [[securities]]  
MUNI = Municipal [[Bonds]] 
ZERO = Zero Coupon [[Bonds]] 
Field should be blank for any other [[Asset]] Category, 
otherwise rejected. 

---

## Page 24

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 24 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
Format: CCYYMMDD 
If submitted, date must be a valid calendar date. 
May be spaces or valid calendar date. Zeroes are 
not a valid value. 
Filler 17 811 827 A/N OPT Reserved for future use. Spaces. 
Carryover Offset 17 828 844 A/N OPT The amount of Amortized Bond [[Premium]] to be 
carried over to the date of disposition (The Current 
Cost basis should NOT be adjusted by this amount). 
The Carryover Offset amount must be carried over 
until the disposition of the [[Asset]]. 
Allowed field for [[Asset]] Category:   
• CDCP = CD or Commercial Paper 
• CORP = Corp Bond 
• FDEB = Foreign Debt 
• GOVT = US Govt. and Govt. Agency 
• MBS = Mortgage Backed [[securities]]  
• MUNI = Municipal [[Bonds]] 
• ZERO = Zero Coupon [[Bonds]] 
Field should be blank or zeroes for any other [[Asset]] 
Category, otherwise rejected. In the case of blank 
value, CBRS populates this field with zeroes and 
pass the record. 
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
Prior Year Mark to Market 17 845 861 A/N COND Section 1256 Options must be submitted on the 
transfer statement beginning 1/1/2016. 
Use only when Section 1256 options have 
transferred. 
When reporting cost basis of 1256 options: 
• If the 1256 [[Option]] was acquired prior to year-end 
of the previous year, use the year end (fair 
market value). Year-end fair market value used 
in reporting unrealized profit or loss on the open 
contracts in box 10 of the 1099-B 
• If the 1256 [[Option]] was acquired in the same year 
as the transfer, populate the Prior Year Mark to 
Market with zero. 
The [[Asset]] category must equal options for 1256 
[[Option]] submissions, any other selection will reject 
when the “Prior Year Mark to Market” field is 
populated. 

---

## Page 25

CBRS Tax Lot Input (T) 
DATATRAK SYSID: Prod 36708 / PSE 46708 
ERROR! NO TEXT OF SPECIFIED STYLE IN DOCUMENT. 25 
COST BASIS TAX LOT INPUT (T) 
DATATRAK SYSID: PROD 36708 / PSE 46708 
RECORD LENGTH: 1,000 
RECORD TYPE: VARIABLE 
REVISION DATE:  April 27, 2023 
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
[[settlement]] Date 8 862 869 A/N COND [[settlement]] date of the original acquisition for the 
Tax Lot being transferred. 
Required field for covered fixed income.  
Fixed income [[Asset]] categories include: 
• CDCP = CD or Commercial Paper 
• CORP = Corp Bond 
• FDEB = Foreign Debt 
• GOVT = US Govt. and Govt. Agency 
• MBS = Mortgage Backed [[securities]] 
• MUNI = Municipal [[Bonds]] 
• ZERO = Zero Coupon [[Bonds]] 
 
If this field is populated for any other [[Asset]] 
Category, CBRS passes the record. 
 
Format: CCYYMMDD 
 
May be spaces or valid calendar date. If the 
submitted date is not a valid calendar date or is in 
the future, CBRS rejects the record. Zeroes are not 
a valid value. 
Best Practice: 
If the [[settlement]] Date is unknown, this field should 
be populated with the date the accrual calculations 
began. 
Accrued Unrealized Market 
Discount 
17 870 886 A/N OPT The amount of market discount on the fixed income 
security that has been accrued but not realized. 
The position of the decimal is denoted by a comma 
(,). Up to two decimal places are supported before 
truncation occurs. 
In the case of blank value, CBRS populates this field 
with zeroes and pass the record. 
Filler 114 887 1000 A/N REQ Reserved for future use. Spaces.  
 
 

---

## Page 26

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. The services described herein are provided under the “[[DTCC]]” brand name by 
certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  
Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in 
which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they 
offer. 
Doc Date: August 28, 2023 
Publication Code: CBRS150 
Service: Cost Basis Reporting Service (CBRS) 
Title: CBRS Tax Lot Input (T) - DATATRAK SYSID: PROD 36708 / PSE 46708 
For More Information 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 