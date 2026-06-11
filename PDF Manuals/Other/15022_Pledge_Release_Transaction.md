---
title: "15022 ISO Pledge Release Transactions Mesage Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/15022_Pledge_Release_Transaction.pdf"
pages: 85
size: "1033.5 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# 15022 ISO Pledge Release Transactions Mesage Layouts

**Original File:** [15022_Pledge_Release_Transaction.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/15022_Pledge_Release_Transaction.pdf)  
**Category:** Other  
**Total Pages:** 85  
**File Size:** 1033.5 KB  

---

## Page 1



---

## Page 2

F ree Pledge 
Free Pledge  
Business Transaction: Free Pledge 
ISO Message Type: MT542 - Deliver Free 
Free Pledge allows you to pledge [[securities]] to any pledgee. You can indicate whether or not the pledge 
is being made from your Initial [[public offering]] ([[IPO]]) account. Money [[settlement]] occurs outside of [[DTC]]. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General 
Information 
:16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the 
function of the message 
:23G: NEWM 
M End of Block – General 
Information 
:16S: GENL 
Mandatory Sequence B - Trade Details 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade Details :16R: TRADDET  

---

## Page 3

  Free Pledge  
M/O Field Description Tag Qualifier(s) Content Rules 
M Loan Date 
Loan date for a pledge or pledge 
release transaction 
:98A: : SETT // yyyymmdd 
M ISIN 
Identification of the financial 
Instrument 
(Country Code, [[CUSIP]] and Check 
Digit) 
:35B:  The literal "ISIN" 
followed by a 
space followed by 
the 12 character 
ISIN.  
Note- [[DTC]] does 
not accept non-
U.S. ISIN 
Example-ISIN 
US1234567891. 
Note-[[DTC]] does 
not accept non-
U.S. ISIN 
M Business Transaction [[ID]] :22F: :PROC/DTCY/ PL02 
O Narrative - [[DTC]] Pledge 
Comments 
Provides additional [[settlement]] 
processing information 
:70E: :SPRO// 35x crlf 21x 
The maximum 
length [[DTC]] will 
accept is 56, 1 line 
of 35 characters 
and 1 line of 21 
characters. Each 
line should be 
separated by a 
CRLF (carriage 
return - line feed). 
M End of Block - Trade Details :16S:  TRADDET  

---

## Page 4

  Free Pledge  
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial instrument 
to be settled expressed as units 
such as share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole 
digit is required. 
No more than 9 
may be present. 
Fractions are not 
allowed. A decimal 
comma is always 
required. 
M Pledgor's [[DTCC]] [[participant]] 
Number 
Pledgor [[DTCC]] [[participant]] 
number 
:97A: :SAFE// 00009999 
0000 followed by 
4 digits. All 4 digits 
are required. 
M End of Block - Financial 
Instrument/Account 
:16S:  FIAC 
 
Mandatory Sequence E - [[settlement]] Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Details 
:16R:  SETDET 
O [[IPO]] Indicator :22F: :STCO/DTCY/ IPOY or IPON 

---

## Page 5

  Free Pledge  
M/O Field Description Tag Qualifier(s) Content Rules 
Indicator used for the [[IPO]] 
Tracking system. 
Indicates that the 
new [[IPO]] format is 
being used.  
'IPOY' - [[IPO]] format 
is being used. 
'IPON' - [[IPO]] 
format is not used. 
If the field is not 
populated, 'IPON' 
will be assumed. 
O PTA Indicator 
Indicates if the transaction 
should affect the Protected 
Transaction Account 
::22F: :STCO/DTCY/ PTAY or PTAN 
Valid Values:  
PTAY - Should 
affect the account 
or PTAN - Should 
not affect the 
account. If the 
field is not 
populated, 
'PTAN' will be 
assumed 
M Pledge Purpose 
Reason for the pledge such as 
for a new loan, loan increase, 
[[collateral]] increase or 
substitution. 
:22F: :SETR/DTCY/   4x 
Indicates the 
reason for the 
release request. 
0001 - New Loan. 
0002 - Increase in 
Loan.  
0003 - Additional 
[[collateral]].  
0004 - 
Substitution of 
[[collateral]]. 

---

## Page 6

  Free Pledge  
M/O Field Description Tag Qualifier(s) Content Rules 
M [[Hypothecation]] Code 
Mandatory code entered by the 
[[participant]] to effect deliveries 
for pledge activity 
:22F: :COLA/DTCY/ 4n 
Indicates to the 
pledgee the 
person(s) for 
whom this 
transaction is 
pledged.  
0001 - Each 
security in the 
pledge is carried 
for the account of 
one or more 
customers. 
0002 - All 
[[securities]] in the 
pledge are carried 
for the account of 
a single customer.  
0003 - No 
[[securities]] in the 
pledge are carried 
for the account of 
any customer.  
0007 - Used for 
Repo accounts. 
Each security in 
the pledge is 
carried for the 
account of one or 
more customers. 
0008 - Used for 
Repo accounts.  All 
[[securities]] in the 
pledge are carried 
for the account of 

---

## Page 7

  Free Pledge  
M/O Field Description Tag Qualifier(s) Content Rules 
a single customer. 
0009 - Used for 
Repo accounts. No 
[[securities]] in the 
pledge are carried 
for the account of 
any customer. 
M End of Block - [[settlement]] 
Details 
:16S:  SETDET 
 
 
 
 
 
 
 
 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Deliverer (Pledgor) 
[[participant]] that delivers the 
security; for a payment order 
the payee; for a [[collateral]] 
pledge, the pledgor. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed 
by 4 digits. All 
4 digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 
M/O Field Description Tag Qualifier(s) Content Rules 

---

## Page 8

  Free Pledge  
 
 
 
 
 
 
 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Receiver (Pledgee) 
[[participant]] that receives the 
security; for a payment order, 
the payor; for a [[collateral]] 
pledge the pledgee. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed 
by 4 digits. All 
4 digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - [[settlement]] 
Details 
:16S:  SETDET 

---

## Page 9

F ree Release Request 
Free Release Request  
Business Transaction: Free Release Request  
ISO Message Type: MT540 - Receive Free 
Free Release Request allows you to request the release of pledged [[securities]]. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General 
Information 
:16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the 
function of the message 
:23G: NEWM 
M End of Block – General 
Information 
:16S: GENL 

---

## Page 10

  Free Release Request  
Mandatory Sequence B - Trade Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade Details :16R:  TRADDET  
M Loan Date 
Loan date for a pledge or pledge 
release transaction 
:98A: : SETT // yyyymmdd 
M ISIN 
Identification of the financial 
instrument 
(Country Code, [[CUSIP]] and Check 
Digit) 
:35B:  The literal "ISIN" 
followed by a 
space followed by 
the 12 character 
ISIN.  
Note- [[DTC]] does 
not accept non-
U.S. ISIN 
Example-ISIN 
US1234567891. 
Note-[[DTC]] does 
not accept non-
U.S. ISIN 
M Business Transaction [[ID]] :22F: :PROC/DTCY/ PL06 
O Narrative - [[DTC]] Pledge 
Comments 
Provides additional [[settlement]] 
processing information 
:70E: :SPRO// 35x crlf 21x 
The maximum 
length [[DTC]] will 
accept is 56, 1 line 
of 35 characters 
and 1 line of 21 
characters. Each 
line should be 
separated by a 
CRLF (carriage 
return - line feed). 

---

## Page 11

  Free Release Request  
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - Trade Details :16S:  TRADDET  
 
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial instrument 
to be settled expressed as units 
such as share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole 
digit is required. 
No more than 9 
may be present. 
Fractions are not 
allowed. A decimal 
comma is always 
required. 
M Pledgor's [[DTCC]] [[participant]] 
Number 
Pledgor [[DTCC]] [[participant]] 
number 
:97A: :SAFE// 00009999 
0000 followed by 
4 digits. All 4 digits 
are required. 
M End of Block - Financial 
Instrument/Account 
:16S:  FIAC 
 
 
 
 
 

---

## Page 12

  Free Release Request  
Mandatory Sequence E - [[settlement]] Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Details 
:16R:  SETDET 
M Release Type 
Indicates the reason for the 
release request. 
:22F: :SETR/DTCY/ 4n 
Valid Values:  0001 
- Delivery. 0002 - 
Substitution of 
[[collateral]]. 0003 - 
Decrease of 
[[collateral]]. 0004 - 
Release of Excess 
[[collateral]] 
O [[CNS]] Indicator 
Indicates if [[securities]] should be 
made eligible for [[CNS]] 
processing. 
::22F: :NETT/DTCY/ CNSY or CNSN 
'N' = No [[CNS]] 
processing,  
'Y' = [[CNS]] 
processing is 
desired. 
If the field is blank, 
'N' will be 
assumed. 
 
 
 
 
 
 

---

## Page 13

  Free Release Request  
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Deliverer (Pledgor) 
[[participant]] that delivers the 
security; for a payment order, 
the payee; for a [[collateral]] 
pledge, the pledgor. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
 
 
 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Receiver (Pledgee) 
[[participant]] that receives the 
security; for a payment order, 
the payor; for a [[collateral]] 
pledge, the pledgee. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 

---

## Page 14

  Free Release Request  
 
M/O Field Description Tag Qualifier(s) Content 
Rules 
M End of Block - [[settlement]] Details :16S:  SETDET 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 

---

## Page 15

F ree Release Return 
Free Release Return  
Business Transaction: Free Release Return  
ISO Message Type: MT542 - Deliver Free 
Free Release Return allows the pledgee to release pledged [[securities]] without a request from the 
pledgor. Money [[settlement]] occurs outside of [[DTC]]. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General 
Information 
:16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the 
function of the message 
:23G: NEWM 
M End of Block – General 
Information 
:16S: GENL 

---

## Page 16

  Free Release Return  
Mandatory Sequence B - Trade Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade Details :16R:  TRADDET  
M Loan Date 
Loan date for a pledge or pledge 
release transaction 
:98A: : SETT // yyyymmdd 
M ISIN 
Identification of the financial 
instrument 
(Country Code, [[CUSIP]] and Check 
Digit) 
:35B:  The literal "ISIN" 
followed by a 
space followed by 
the 12 character 
ISIN.  
Note- [[DTC]] does 
not accept non-
U.S. ISIN 
Example-ISIN 
US1234567891. 
Note-[[DTC]] does 
not accept non-
U.S. ISIN 
M Business Transaction [[ID]] :22F: :PROC/DTCY/ PL04 
O Narrative - [[DTC]] Pledge 
Comments 
Provides additional [[settlement]] 
processing information 
:70E: :SPRO// 35x crlf 21x 
The maximum 
length [[DTC]] will 
accept is 56, 1 line 
of 35 characters 
and 1 line of 21 
characters. Each 
line should be 
separated by a 
CRLF (carriage 
return - line feed). 

---

## Page 17

  Free Release Return  
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - Trade Details :16S:  TRADDET  
 
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial instrument 
to be settled expressed as units 
such as share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole 
digit is required. 
No more than 9 
may be present. 
Fractions are not 
allowed. A decimal 
comma is always 
required. 
M [[DTCC]] Pledgee Bank Number 
[[DTCC]] pledgee bank number 
:97A: :SAFE// 00009999 
0000 followed by 
4 digits. All 4 digits 
are required. 
M End of Block - Financial 
Instrument/Account 
:16S:  FIAC 
 
 
 
 

---

## Page 18

F ree Release Return 
Mandatory Sequence E - [[settlement]] Details 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Details 
:16R: SETDET 
M Release Type 
Indicates the reason for the 
release request. 
:22F: :SETR/DTCY/ 4n 
Valid Values:  0001 
- Delivery. 0002 - 
Substitution of 
[[collateral]]. 0003 - 
Decrease of 
[[collateral]]. 0004 - 
Release of Excess 
[[collateral]] 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R: SETPRTY 
M Deliverer (Pledgee) 
[[participant]] that delivers the 
security; for a payment order, 
the payee; for a [[collateral]] 
pledge return, the pledgee 
bank. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S: SETPRTY 

---

## Page 19

F ree Release Return 
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R: SETPRTY 
M Receiver (Pledgor) 
[[participant]] that receives the 
security; for a payment order, 
the payor; for a [[collateral]] 
pledge return, the pledgor. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S: SETPRTY 
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R: SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] 
Parties 
:16S: SETPRTY 
M/O Field Description Tag Qualifier(s) Content 
Rules 
M End of Block - [[settlement]] Details :16S: SETDET 

---

## Page 20

V alued Pledge 
Valued Pledge 
Business Transaction: Valued Pledge 
ISO Message Type: MT543 - Deliver Against Payment 
Valued Pledge allows you to pledge [[securities]] to any pledgee with a [[DTC]] [[participant]] account and 
indicate whether or not the pledge is being made from your [[IPO]] account. Money [[settlement]] occurs 
within [[DTC]]'s [[settlement]] System. Valued pledges are subject to the pledgee's Receiver Authorized 
Delivery (RAD) limits. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General 
Information 
:16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the 
function of the message 
:23G: NEWM 
M End of Block – General 
Information 
:16S: GENL 

---

## Page 21

  Valued Pledge  
Mandatory Sequence B - Trade Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade Details :16R:  TRADDET  
M Loan Date 
Loan date for a pledge or pledge 
release transaction 
:98A: : SETT // yyyymmdd 
M ISIN 
Identification of the financial 
instrument 
(Country Code, [[CUSIP]] and Check 
Digit) 
:35B:  The literal "ISIN" 
followed by a 
space followed by 
the 12 character 
ISIN.  
Note- [[DTC]] does 
not accept non-
U.S. ISIN 
Example-ISIN 
US1234567891. 
Note-[[DTC]] does 
not accept non-
U.S. ISIN 
M Business Transaction [[ID]] :22F: :PROC/DTCY/ PL01 
O Narrative - [[DTC]] Pledge 
Comments 
Provides additional [[settlement]] 
processing information 
:70E: :SPRO// 35x crlf 21x 
The maximum 
length [[DTC]] will 
accept is 56, 1 line 
of 35 characters 
and 1 line of 21 
characters. Each 
line should be 
separated by a 
CRLF (carriage 
return - line feed). 

---

## Page 22

  Valued Pledge  
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - Trade Details :16S:  TRADDET  
 
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial instrument 
to be settled expressed as units 
such as share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole 
digit is required. 
No more than 9 
may be present. 
Fractions are not 
allowed. A decimal 
comma is always 
required. 
M Pledgor's [[DTCC]] [[participant]] 
Number 
Pledgor [[DTCC]] [[participant]] 
number 
:97A: :SAFE// 00009999 
0000 followed by 
4 digits. All 4 digits 
are required. 
M End of Block - Financial 
Instrument/Account 
:16S:  FIAC 
 
 
 
 
 

---

## Page 23

  Valued Pledge  
Mandatory Sequence E - [[settlement]] Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Details 
:16R:  SETDET 
O [[IPO]] Indicator 
Indicator used for the [[IPO]] 
Tracking system. 
:22F: :STCO/DTCY/ IPOY or IPON 
Indicates that the 
new [[IPO]] format is 
being used.  
'IPOY' - [[IPO]] format 
is being used. 
'IPON' - [[IPO]] 
format is not used. 
If the field is not 
populated, 'IPON' 
will be assumed. 
M Pledge Purpose 
Reason for the pledge such as 
for a new loan, loan increase, 
[[collateral]] increase, or 
substitution. 
:22F: :SETR/DTCY/   4x 
Indicates the 
reason for the 
release request. 
0001 - New Loan. 
0002 - Increase in 
Loan.  
0003 - Additional 
[[collateral]].  
0004 - 
Substitution of 
[[collateral]]. 
M [[Hypothecation]] Code 
Mandatory code entered by the 
[[participant]] to effect deliveries 
:22F: :COLA/DTCY/ 4n 
Indicates to the 
pledgee the 

---

## Page 24

  Valued Pledge  
M/O Field Description Tag Qualifier(s) Content Rules 
for pledge activity. person(s) for 
whom this 
transaction is 
pledged.  
0001 - Each 
security in the 
pledge is carried 
for the account of 
one or more 
customers. 
0002 - All 
[[securities]] in the 
pledge are carried 
for the account of 
a single customer.  
0003 - No 
[[securities]] in the 
pledge are carried 
for the account of 
any customer.  
0007 - Used for 
Repo accounts. 
Each security in 
the pledge is 
carried for the 
account of one or 
more customers. 
0008 - Used for 
Repo accounts.  All 
[[securities]] in the 
pledge are carried 
for the account of 
a single customer. 
0009 - Used for 
Repo accounts. No 
[[securities]] in the 

---

## Page 25

  Valued Pledge  
M/O Field Description Tag Qualifier(s) Content Rules 
pledge are carried 
for the account of 
any customer. 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Deliverer (Pledgor) 
[[participant]] that delivers the 
security; for a payment order, 
the payee; for a [[collateral]] 
pledge, the pledgor. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Receiver (Pledgee) 
[[participant]] that receives the 
security; for a payment order, 
the payor; for a [[collateral]] 
pledge, the pledgee. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required.digits 
are required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
  

---

## Page 26

  Valued Pledge  
 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
Mandatory Subsequence E3- Amounts (Loan Value) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Amounts 
:16R:  AMT 
M Loan Value :19A: :SETT// USD9999999999,99 
USD followed by at 
least 1 whole digit. 
No more than 10 
whole digits may 
be present. 
Fractional digits are 
optional, but no 
more than 2 may 
be present. A 
decimal comma is 
always required. 

---

## Page 27

  Valued Pledge  
 
 
 
M End of Block - [[settlement]] 
Amounts 
:16S:  AMT 
M/O Field Description Tag Qualifier(s) Content 
Rules 
M End of Block - [[settlement]] Details :16S:  SETDET 

---

## Page 28

V alued Release Request 
Valued Release Request  
Business Transaction: Valued Release Request  
ISO Message Type: MT541 - Receive Against Payment 
Valued Release Request allows you to request the release of pledged [[securities]] from any pledgee with a 
[[DTC]] [[participant]] account. Valued release requests are not subject to RAD limits, since both parties must 
take action on each transaction. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information  
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General 
Information 
:16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the 
function of the message 
:23G: NEWM 
M End of Block – General 
Information 
:16S: GENL 

---

## Page 29

  Valued Release Request  
Mandatory Sequence B - Trade Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade Details :16R:  TRADDET  
M Loan Date 
Loan date for a pledge or pledge 
release transaction 
:98A: : SETT // yyyymmdd 
M ISIN 
Identification of the financial 
instrument 
(Country Code, [[CUSIP]] and Check 
Digit) 
:35B:  The literal "ISIN" 
followed by a 
space followed by 
the 12 character 
ISIN.  
Note- [[DTC]] does 
not accept non-
U.S. ISIN 
Example-ISIN 
US1234567891. 
Note-[[DTC]] does 
not accept non-
U.S. ISIN 
M Business Transaction [[ID]] :22F: :PROC/DTCY/ PL05 
O Narrative - [[DTC]] Pledge 
Comments 
Provides additional [[settlement]] 
processing information 
:70E: :SPRO// 35x crlf 21x 
The maximum 
length [[DTC]] will 
accept is 56, 1 line 
of 35 characters 
and 1 line of 21 
characters. Each 
line should be 
separated by a 
CRLF (carriage 
return - line feed). 

---

## Page 30

  Valued Release Request  
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - Trade Details :16S:  TRADDET  
 
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial instrument 
to be settled expressed as units 
such as share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole 
digit is required. 
No more than 9 
may be present. 
Fractions are not 
allowed. A decimal 
comma is always 
required. 
M Pledgor's [[DTCC]] [[participant]] 
Number 
Pledgor [[DTCC]] [[participant]] 
number 
:97A: :SAFE// 00009999 
0000 followed by 
4 digits. All 4 digits 
are required. 
M End of Block - Financial 
Instrument/Account 
:16S:  FIAC 
 
 
 
 
 

---

## Page 31

  Valued Release Request  
Mandatory Sequence E - [[settlement]] Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Details 
:16R:  SETDET 
M Release Type 
Indicates the reason for the 
release request. 
:22F: :SETR/DTCY/ 4n 
Valid Values:  0001 
- Delivery. 0002 - 
Substitution of 
[[collateral]]. 0003 - 
Decrease of 
[[collateral]]. 0004 - 
Release of Excess 
[[collateral]] 
 
Mandatory Subsequence E1 -  [[settlement]] Parties (Deliverer) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Deliverer (Pledgor) 
[[participant]] that delivers the 
security; for a payment order 
the payee; for a [[collateral]] 
pledge, the pledgor. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
 
 

---

## Page 32

  Valued Release Request  
Mandatory Subsequence E1 -  [[settlement]] Parties (Receiver)  
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Receiver (Pledgee) 
[[participant]] that receives the 
security; for a payment order, 
the payor; for a [[collateral]] 
pledge, the pledgee. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
Mandatory Subsequence E1 -  [[settlement]] Parties (Place of [[settlement]])  
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
 
 
 
 
 
 
 

---

## Page 33

  Valued Release Request  
 
Mandatory Subsequence E3 - Amounts (Loan Value) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Amounts 
:16R:  AMT 
M Loan Value :19A: :SETT// USD9999999999,99 
USD followed by at 
least 1 whole digit. 
No more than 10 
whole digits may 
be present. 
Fractional digits are 
optional, but no 
more than 2 may 
be present. A 
decimal comma is 
always required. 
M End of Block - [[settlement]] 
Amounts 
:16S:  AMT 
 
M/O Field Description Tag Qualifier(s) Content 
Rules 
M End of Block - [[settlement]] Details :16S:  SETDET 
 
 
 
 

---

## Page 34

V alued Release Return 
Valued Release Return  
Business Transaction: Valued Release Return  
ISO Message Type: MT543 – Deliver Against Payment 
Valued Release Return allows the pledgee to release pledged [[securities]] without a request from the 
pledgor. [[settlement]] occurs within [[DTC]]'s [[settlement]] System. The releases are subject to the pledgor's 
Receiver Authorized Delivery (RAD) approval. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General 
Information 
:16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the 
function of the message 
:23G: NEWM 
M End of Block – General 
Information 
:16S: GENL 

---

## Page 35

  Valued Release Return  
Mandatory Sequence B - Trade Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade Details :16R:  TRADDET  
M Loan Date 
Loan date for a pledge or pledge 
release transaction 
:98A: : SETT // yyyymmdd 
M ISIN 
Identification of the financial 
instrument 
(Country Code, [[CUSIP]] and Check 
Digit) 
:35B:  The literal "ISIN" 
followed by a 
space followed by 
the 12 character 
ISIN.  
Note- [[DTC]] does 
not accept non-
U.S. ISIN 
Example-ISIN 
US1234567891. 
Note-[[DTC]] does 
not accept non-
U.S. ISIN 
M Business Transaction [[ID]] :22F: :PROC/DTCY/ PL03 
O Narrative - [[DTC]] Pledge 
Comments 
Provides additional [[settlement]] 
processing information 
:70E: :SPRO// 35x crlf 21x 
The maximum 
length [[DTC]] will 
accept is 56, 1 line 
of 35 characters 
and 1 line of 21 
characters. Each 
line should be 
separated by a 
CRLF (carriage 
return - line feed). 

---

## Page 36

  Valued Release Return  
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - Trade Details :16S:  TRADDET  
 
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial instrument 
to be settled expressed as units 
such as share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole 
digit is required. 
No more than 9 
may be present. 
Fractions are not 
allowed. A decimal 
comma is always 
required. 
M [[DTCC]] Pledgee Bank Number 
[[DTCC]] pledgee bank number 
:97A: :SAFE// 00009999 
0000 followed by 
4 digits. All 4 digits 
are required. 
M End of Block - Financial 
Instrument/Account 
:16S:  FIAC 
 
 
 
 
 

---

## Page 37

  Valued Release Return  
 
Mandatory Sequence E - [[settlement]] Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Details 
:16R:  SETDET 
M Release Type 
Indicates the reason for the 
release request. 
:22F: :SETR/DTCY/ 4n 
Valid Values:  0001 
- Delivery. 0002 - 
Substitution of 
[[collateral]]. 0003 - 
Decrease of 
[[collateral]]. 0004 - 
Release of Excess 
[[collateral]] 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Deliverer (Pledgee) 
[[participant]] that delivers the 
security; for a payment order, 
the payee; for a [[collateral]] 
pledge return, the pledgee 
bank. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 

---

## Page 38

  Valued Release Return  
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Receiver (Pledgor) 
[[participant]] that receives the 
security; for a payment order, 
the payor; for a [[collateral]] 
pledge return, the pledgor 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
 
 
 
 
 
 
 
 

---

## Page 39

  Valued Release Return  
Mandatory Subsequence E3 - Amounts (Loan Value) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Amounts 
:16R:  AMT 
M Loan Value :19A: :SETT// USD9999999999,99 
USD followed by at 
least 1 whole digit. 
No more than 10 
whole digits may 
be present. 
Fractional digits are 
optional, but no 
more than 2 may 
be present. A 
decimal comma is 
always required. 
M End of Block - [[settlement]] 
Amounts 
:16S:  AMT 
 
M/O Field Description Tag Qualifier(s) Content 
Rules 
M End of Block - [[settlement]] Details :16S:  SETDET 
 
 
 
 

---

## Page 40

F ree Fed Pledge 
Free Fed Pledge  
Business Transaction: Free Fed Pledge 
ISO Message Type: MT542 - Deliver Free 
Free Fed Pledge allows you to pledge [[securities]] to a Federal Reserve Bank (FRB) on behalf of a 
[[participant]] or non- [[participant]]. Money [[settlement]] occurs outside of [[DTC]]. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General 
Information 
:16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the 
function of the message 
:23G: NEWM 
M End of Block – General 
Information 
:16S: GENL 

---

## Page 41

F ree Fed Pledge 
Mandatory Sequence B - Trade Details 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade Details :16R: TRADDET  
M Loan Date 
Loan date for a pledge or pledge 
release transaction 
:98A: : SETT // yyyymmdd 
M ISIN 
Identification of the financial 
Instrument 
(Country Code, [[CUSIP]] and Check 
Digit) 
:35B: The literal "ISIN" 
followed by a 
space followed by 
the 12 character 
ISIN.  
Note- [[DTC]] does 
not accept non-
U.S. ISIN 
Example-ISIN 
US1234567891. 
Note-[[DTC]] does 
not accept non-
U.S. ISIN 
M Business Transaction [[ID]] :22F: :PROC/DTCY/ FP01 
O Narrative - [[DTC]] Pledge 
Comments 
Provides additional [[settlement]] 
processing information 
:70E: :SPRO// 35x crlf 1x 
The maximum 
length [[DTC]] will 
accept is 36, 1 line 
of 35 characters 
and 1 line of 1 
character. Each 
line should be 
separated by a 
CRLF (carriage 
return - line feed). 

---

## Page 42

F ree Fed Pledge 
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - Trade Details :16S: TRADDET  
Mandatory Sequence C - Financial Instrument/Account 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Financial 
Instrument/Account 
:16R: FIAC 
M Quantity 
Quantity of financial instrument 
to be settled expressed as units 
such as share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole 
digit is required. 
No more than 9 
may be present. 
Fractions are not 
allowed. A decimal 
comma is always 
required. 
M Pledgor's [[DTCC]] [[participant]] 
Number 
Pledgor [[DTCC]] [[participant]] 
number 
:97A: :SAFE// 00009999 
0000 followed by 
4 digits. All 4 digits 
are required. 
M End of Block - Financial 
Instrument/Account 
:16S: FIAC 

---

## Page 43

F ree Fed Pledge 
Mandatory Sequence E - [[settlement]] Details 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - 
[[settlement]] Details 
:16R: SETDET 
O Federal Reserve 
Purpose 
Reason for the free Fed 
pledge or release 
return. 
:22F: :STCO/DTCY/ 4x 
Indicates the 
reason for the 
request. 
0001 - Discount. 
0002 - Treasury Tax 
and Loan. 
0003 - Circular 176 
(Public Purposes). 
0004 - TTL (Term 
Invest Program 
T208). 
0005 - Daylight 
(Funds) Overdrafts. 
M Pledge Purpose 
Reason for the pledge 
such as for a new loan, 
loan increase, [[collateral]] 
increase, or 
substitution. 
:22F: :SETR/DTCY/  4x 
Indicates the 
reason for the 
release request. 
0001 - New Loan. 
0002 - Increase in 
Loan.  
0003 - Additional 
[[collateral]].  
0004 - Substitution 
of [[collateral]]. 

---

## Page 44

F ree Fed Pledge 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R: SETPRTY 
M Deliverer (Pledgor) 
[[participant]] that delivers the 
security; for a payment order, 
the payee; for a [[collateral]] 
pledge, the pledgor. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S: SETPRTY 
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R: SETPRTY 
M Receiver (Pledgee) 
[[participant]] that receives the 
security; for a payment order, 
the payor; for a [[collateral]] 
pledge, the pledgee. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S: SETPRTY 
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R: SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 

---

## Page 45

F ree Fed Pledge 
M End of Block - [[settlement]] 
Parties 
:16S: SETPRTY 
M/O Field Description Tag Qualifier(s) Content 
Rules 
M End of Block - [[settlement]] Details :16S: SETDET 
Optional Sequence F – Other Parties 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – Other Parties :16R: OTHRPRTY 
M Bank ABA Number 
The American Bankers 
Association ABA number 
identifying the settling bank 
account for a free FED pledge 
or release return. 
:95R: :MERE/DTCY/ 9x 
O Bank ABA Description 
Provides additional information 
about the ABA account. 
:97A: :SAFE// 20x 
M End of Block – Other Parties :16S: OTHRPRTY 

---

## Page 46

F ree Fed Release Request 
Free Fed Release Request  
Business Transaction: Free Fed Release Request  
ISO Message Type: MT540 - Receive Free 
Free Fed Release Request allows you to request the release of pledged [[securities]] from an FRB. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General 
Information 
:16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the 
function of the message 
:23G: NEWM 
M End of Block – General 
Information 
:16S: GENL 

---

## Page 47

  Free Fed Release Request  
Mandatory Sequence B - Trade Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade Details :16R:  TRADDET  
M Loan Date 
Loan date for a pledge or pledge 
release transaction 
:98A: : SETT // yyyymmdd 
M ISIN 
Identification of the financial 
instrument 
(Country Code, [[CUSIP]] and Check 
Digit) 
:35B:  The literal "ISIN" 
followed by a 
space followed by 
the 12 character 
ISIN.  
Note- [[DTC]] does 
not accept non-
U.S. ISIN 
Example-ISIN 
US1234567891. 
Note-[[DTC]] does 
not accept non-
U.S. ISIN 
M Business Transaction [[ID]] :22F: :PROC/DTCY/ FP02 
O Narrative - [[DTC]] Pledge 
Comments 
Provides additional [[settlement]] 
processing information 
:70E: :SPRO// 35x crlf 1x 
The maximum 
length [[DTC]] will 
accept is 36, 1 line 
of 35 characters 
and 1 line of 1 
character. Each 
line should be 
separated by a 
CRLF (carriage 
return - line feed). 

---

## Page 48

  Free Fed Release Request  
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - Trade Details :16S:  TRADDET  
 
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial instrument 
to be settled expressed as units 
such as share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole 
digit is required. 
No more than 9 
may be present. 
Fractions are not 
allowed. A decimal 
comma is always 
required. 
M Pledgor's [[DTCC]] [[participant]] 
Number 
Pledgor [[DTCC]] [[participant]] 
number 
:97A: :SAFE// 00009999 
0000 followed by 
4 digits. All 4 digits 
are required. 
M End of Block - Financial 
Instrument/Account 
:16S:  FIAC 
 
 
 
 
 

---

## Page 49

  Free Fed Release Request  
Mandatory Sequence E - [[settlement]] Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Details 
:16R:  SETDET 
O Federal Reserve Purpose 
Reason for the free Fed pledge 
or release return. 
:22F: :STCO/DTCY/ 4x 
Indicates the 
reason for the 
request.  
0001 - Discount.  
0002 - Treasury 
Tax and Loan. 
0003 - Circular 176 
(Public Purposes). 
0004 - TTL (Term 
Invest Program 
T208). 
0005 - Daylight 
(Funds) 
Overdrafts. 
M Release Type 
Indicates the reason for the 
release request. 
:22F: :SETR/DTCY/ 4n 
Valid Values:  0001 
- Delivery. 0002 - 
Substitution of 
[[collateral]]. 0003 - 
Decrease of 
[[collateral]]. 0004 - 
Release of Excess 
[[collateral]]. 
O [[CNS]] Indicator 
Indicates if [[securities]] should be 
::22F: :NETT/DTCY/ CNSY or CNSN 
'N' = No [[CNS]] 

---

## Page 50

  Free Fed Release Request  
M/O Field Description Tag Qualifier(s) Content Rules 
made eligible for [[CNS]] 
processing. 
processing,  
'Y' = [[CNS]] 
processing is 
desired. 
If the field is blank, 
'N' will be 
assumed. 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Deliverer (Pledgor) 
[[participant]] that delivers the 
security; for a payment order, 
the payee; for a [[collateral]] 
pledge, the pledgor. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
 
 
 
 
 
 
 
 

---

## Page 51

  Free Fed Release Request  
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Receiver (Pledgee) 
[[participant]] that receives the 
security; for a payment order, 
the payor; for a [[collateral]] 
pledge, the pledgee. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
M/O Field Description Tag Qualifier(s) Content 
Rules 
M End of Block - [[settlement]] Details :16S:  SETDET 
 
 
 
 
 

---

## Page 52

F ree Fed Release Request 
Optional Sequence F – Other Parties 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – Other Parties :16R: OTHRPRTY 
M Bank ABA Number 
The American Bankers 
Association ABA number 
identifying the settling bank 
account for a free FED pledge 
or release return. 
:95R: :MERE/DTCY/ 9x 
O Bank ABA Description 
Provides additional information 
about the ABA account. 
:97A: :SAFE// 20x 
M End of Block – Other Parties :16S: OTHRPRTY 

---

## Page 53

F ree Fed Release Return 
Free Fed Release Return  
Business Transaction: Free Fed Release Return  
ISO Message Type: MT542 - Deliver Free 
Federal Reserve Banks can use Free Fed Release Return to return pledged [[securities]] without a request 
from the pledgor. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General 
Information 
:16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the 
function of the message 
:23G: NEWM 
M End of Block – General 
Information 
:16S: GENL 

---

## Page 54

  Free Fed Release Return  
Mandatory Sequence B - Trade Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade Details :16R:  TRADDET  
M Loan Date 
Loan date for a pledge or pledge 
release transaction 
:98A: : SETT // yyyymmdd 
M ISIN 
Identification of the financial 
instrument 
(Country Code, [[CUSIP]] and Check 
Digit) 
:35B:  The literal "ISIN" 
followed by a 
space followed by 
the 12 character 
ISIN.  
Note- [[DTC]] does 
not accept non-
U.S. ISIN 
Example-ISIN 
US1234567891. 
Note-[[DTC]] does 
not accept non-
U.S. ISIN 
M Business Transaction [[ID]] :22F: :PROC/DTCY/ FP03 
O Narrative - [[DTC]] Pledge 
Comments 
Provides additional [[settlement]] 
processing information 
:70E: :SPRO// 35x crlf 1x 
The maximum 
length [[DTC]] will 
accept is 36, 1 line 
of 35 characters 
and 1 line of 1 
character. Each 
line should be 
separated by a 
CRLF (carriage 
return - line feed). 

---

## Page 55

  Free Fed Release Return  
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - Trade Details :16S:  TRADDET  
 
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial instrument 
to be settled expressed as units 
such as share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole 
digit is required. 
No more than 9 
may be present. 
Fractions are not 
allowed. A decimal 
comma is always 
required. 
M [[DTCC]] Pledgee Bank Number 
[[DTCC]] pledgee bank number 
:97A: :SAFE// 00009999 
0000 followed by 
4 digits. All 4 digits 
are required. 
M End of Block - Financial 
Instrument/Account 
:16S:  FIAC 
 
 
 
 
 

---

## Page 56

  Free Fed Release Return  
 
Mandatory Sequence E - [[settlement]] Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Details 
:16R:  SETDET 
O Federal Reserve Purpose 
Reason for the free Fed pledge 
or release return. 
:22F: :STCO/DTCY/ 4x 
Indicates the 
reason for the 
request.  
0001 - Discount.  
0002 - Treasury 
Tax and Loan. 
0003 - Circular 176 
(Public Purposes). 
0004 - TTL (Term 
Invest Program 
T208). 
0005 - Daylight 
(Funds) 
Overdrafts. 
M Release Type 
Indicates the reason for the 
release request. 
:22F: :SETR/DTCY/ 4n 
Valid Values:  0001 
- Delivery. 0002 - 
Substitution of 
[[collateral]]. 0003 - 
Decrease of 
[[collateral]]. 0004 - 
Release of Excess 
[[collateral]] 
 

---

## Page 57

  Free Fed Release Return  
 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Deliverer (Pledgee) 
[[participant]] that delivers the 
security; for a payment order, 
the payee; for a [[collateral]] 
pledge return, the pledgee 
bank. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Receiver (Pledgor) 
[[participant]] that receives the 
security; for a payment order, 
the payor; for a [[collateral]] 
pledge return, the pledgor. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
 
 
 
 

---

## Page 58

  Free Fed Release Return  
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Parties 
:16R:  SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] 
Parties 
:16S:  SETPRTY 
 
M/O Field Description Tag Qualifier(s) Content 
Rules 
M End of Block - [[settlement]] Details :16S:  SETDET 
 
Optional Sequence F  – Other Parties 
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – Other Parties :16R:  OTHRPRTY 
M Bank ABA Number 
The American Bankers 
Association ABA number 
identifying the settling bank 
account for a free FED pledge 
or release return. 
:95R: :MERE/DTCY/ 9x 
O Bank ABA Description 
Provides additional information 
about the ABA account. 
:97A: :SAFE// 20x 
M End of Block – Other Parties :16S:  OTHRPRTY 

---

## Page 59

F ree OCC Pledge 
1 
Free OCC Pledge  
Business Transaction: Free OCC Pledge 
ISO Message Type: MT542 - Deliver Free 
Free OCC Pledge allows you to pledge [[securities]] to the OCC (Options Clearing Corp). You can indicate 
whether or not the pledge is being made from your Initial [[public offering]] ([[IPO]]) account. Money 
[[settlement]] occurs outside of [[DTC]]. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information  
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General 
Information 
:16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the 
function of the message 
:23G: NEWM 
M End of Block – General 
Information 
:16S: GENL 

---

## Page 60

  Free OCC Pledge  
  2 
 
 
Mandatory Sequence B - Trade Details  
 
 
 M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade 
Details 
:16R:  TRADDET  
M Loan Date 
Loan date for a pledge 
or pledge release 
transaction 
:98A: : SETT // yyyymmdd. 
 The loan date for OCC pledges is always 
19730320. 
  
M ISIN 
Identification of the 
financial Instrument 
(Country Code, [[CUSIP]] 
and Check Digit) 
:35B:  The literal "ISIN" followed by a space 
followed by the 12 character ISIN.  
Note- [[DTC]] does not accept non-U.S. ISIN  
Example-ISIN US1234567891. Note-[[DTC]] does 
not accept non-U.S. ISIN 
M Business Transaction 
[[ID]] 
:22F: :PROC/DTCY/ OP01 
O Narrative – OCC 
Symbology 
Provides additional 
[[settlement]] processing 
information for OCC 
messages.  
:70E: :SPRO// 6*35x 
6 lines of 35 characters each, with each line 
separated by a CRLF (carriage return – line 
feed). 
Each field containing Symbology information 
will be prefixed by the Qualifier as noted 
below.  If more than one field is included on 
one line, the next field qualifier will be 
preceded by a comma (,). 
e.g. 
CLG>XX,CLM>XXXXX 
ACT>XX,ACI>XXXXXXXXXXXXXXX 

---

## Page 61

  Free OCC Pledge  
  3 
 
 M/O Field Description Tag Qualifier(s) Content Rules 
SYM>XXXXXX,EXY>YYYY,EXM>MM,EXD>DD 
COT>XX,OPT>X,SPI>NNNNNN,SPD>NNNNNN 
XRF>XXXXXXXXXXXXXXXXXXXX 
CAC>XXXXXXXXXXXXXXXXXXXX 
   CLG> OCC Clearing Group [[ID]] 
2x 
New Field – OCC Future Use 
   CLM> OCC Clearing [[Member]] Number 
(aka OCC 3rd Party) 
5x 
OCC Required Field 
Example ‘00005’ 
 
[[DTC]] required field for Options Release 
of Deposit Request (both two-party & 
three-party requests) 
    ACT> OCC Account Type 
2x 
OCC Required Field 
List of values: 
‘C ‘   –   Customer 
‘F ‘   –    Firm 
‘M ‘ –    [[Market Maker]] 
‘Z ‘   –   Clearing Fund 
 
[[DTC]] required field for Options Release of 
Deposit Request (two-party request only) 

---

## Page 62

  Free OCC Pledge  
  4 
 
 M/O Field Description Tag Qualifier(s) Content Rules 
   ACI> OCC Account / Sub-Account [[ID]] 
15x 
Optional Field 
Example: ‘ABC’ 
   SYM> OCC [[Option]] Symbol 
6x 
OCC required field when OCC [[collateral]] Type, 
below, is ‘ED’ – Escrow Deposit or ‘SD’ – 
Specific Deposit, otherwise, Optional. 
Example: ‘IBM’ 
[[DTC]] required field for Options Release of 
Deposit Request (three-party request only) 
   EXY> OCC [[Option]] Expiration Year 
4x 
OCC required field when OCC [[collateral]] Type, 
below, is ‘ED’ – Escrow Deposit or ‘SD’ – 
Specific Deposit, otherwise, Optional. 
Example: ‘2013’ 
[[DTC]] required field for Options Release of 
Deposit Request (three-party request only) 
   EXM> OCC [[Option]] Expiration Month 
2x 
OCC required field when OCC [[collateral]] Type, 
below, is ‘ED’ – Escrow Deposit or ‘SD’ – 
Specific Deposit, otherwise, Optional. 
Example: ‘06’ 
[[DTC]] required field for Options Release of 
Deposit Request (three-party request only) 
 

---

## Page 63

  Free OCC Pledge  
  5 
 
 M/O Field Description Tag Qualifier(s) Content Rules 
   EXD> OCC [[Option]] Expiration Day 
2x 
OCC required field when OCC [[collateral]] Type, 
below, is ‘ED’ – Escrow Deposit or ‘SD’ – 
Specific Deposit, otherwise, Optional. 
Example: ‘23’ 
[[DTC]] required field for Options Release of 
Deposit Request (three-party request only) 
   COT> OCC [[collateral]] Type 
2x 
OCC Required Field 
List of Values: 
‘ED’    –   Escrow Deposit 
‘GE’    –   GSE Debt 
‘GS’    –   Government Security 
‘MM’ –  Money Market Fund 
‘SD’    –   Specific Deposit 
‘VS’    –   Valued Security 
[[DTC]] required field for Options Release of 
Deposit Request (two-party request only) 
   OPT> OCC [[Option]] Type 
1x 
OCC required field when OCC [[collateral]] Type, 
above, is ‘ED’ – Escrow Deposit or ‘SD’ – 
Specific Deposit, otherwise, Optional. 
List of values: 
‘C’   –   Call 
‘P’   –   Put 

---

## Page 64

  Free OCC Pledge  
  6 
 
 M/O Field Description Tag Qualifier(s) Content Rules 
   SPI> OCC [[Option]] Strike Price (Integer) 
6n 
OCC required field when OCC [[collateral]] Type, 
above, is ‘ED’ – Escrow Deposit or ‘SD’ – 
Specific Deposit, otherwise, Optional. 
Example: 000135 
[[DTC]] required field for Options Release of 
Deposit Request (three-party request only) 
   SPD> OCC [[Option]] Strike Price (Decimal) 
6n 
OCC required field when OCC [[collateral]] Type, 
above, is ‘ED’ – Escrow Deposit or ‘SD’ – 
Specific Deposit, otherwise, Optional. 
Example: 502100 
   XRF> Cross Reference Number 
20X 
OCC required field only for [[collateral]] Type of 
Escrow Deposit representing the customer account 
name 
Example ‘12345678901234567890’ 
   CAC> Customer Account Number 
20X 
OCC required field only for [[collateral]] Type of 
Escrow Deposit representing the customer account 
number 
Example ‘12345678901234567890’ 
M End of Block - Trade 
Details 
:16S:  TRADDET  
 
 

---

## Page 65

  Free OCC Pledge  
  7 
 
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - 
Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial 
instrument to be 
settled expressed as 
units such as share 
quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole digit is 
required. No more than 9 may 
be present. Fractions are not 
allowed. A decimal comma is 
always required. 
M Pledgor's [[DTCC]] 
[[participant]] Number 
Pledgor [[DTCC]] 
[[participant]] number 
:97A: :SAFE// 00009999 
0000 followed by 4 digits. All 4 
digits are required. 
M End of Block - 
Financial 
Instrument/Account 
:16S:  FIAC 
 
  

---

## Page 66

  Free OCC Pledge  
  8 
 
Mandatory Sequence E - [[settlement]] Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - 
[[settlement]] Details 
:16R:  SETDET 
O [[IPO]] Indicator 
Indicator used for the 
[[IPO]] Tracking system. 
:22F: :STCO/DTCY/ IPOY or IPON 
Indicates that the new [[IPO]] format is being 
used.  
'IPOY'   –    [[IPO]] format is being used. 
'IPON’  –    [[IPO]] format is not used. If the field 
is not populated, 'IPON' will be 
assumed. 
O PTA Indicator 
Indicates if the 
transaction should affect 
the Protected 
Transaction Account 
::22F: :STCO/DTCY/ PTAY or PTAN 
Valid Values:   
‘PTAY’    –   Should affect the account 
‘PTAN’   –   Should not affect the account. If 
the field is not populated, 
'PTAN' will be assumed 
M Pledge Purpose 
Reason for the pledge 
such as for a new loan, 
loan increase, [[collateral]] 
increase or substitution. 
:22F: :SETR/DTCY/   4x 
Indicates the reason for the Pledge. 
‘0001’   –   New Loan. 
‘0002’   –   Increase in Loan.  
‘0003’   –   Additional [[collateral]].  
‘0004’   –   Substitution of [[collateral]]. 
M [[Hypothecation]] Code 
Mandatory code entered 
by the [[participant]] to 
effect deliveries for 
pledge activity 
:22F: :COLA/DTCY/ 4n 
Indicates to the pledgee the person(s) for 
whom this transaction is pledged.  
 

---

## Page 67

  Free OCC Pledge  
  9 
 
M/O Field Description Tag Qualifier(s) Content Rules 
‘0001’   –   Each security in the pledge is 
carried for the account of one or 
more customers. 
‘0002’   –   All [[securities]] in the pledge are 
carried for the account of a 
single customer.  
‘0003’   –   No [[securities]] in the pledge are 
carried for the account of any 
customer.  
‘0007’   –   Used for Repo accounts. Each 
security in the pledge is carried 
for the account of one or more 
customers. 
‘0008’   –   Used for Repo accounts. All 
[[securities]] in the pledge are 
carried for the account of a 
single customer. 
‘0009’   –   Used for Repo accounts. No 
[[securities]] in the pledge are 
carried for the account of any 
customer. 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] Parties :16R:  SETPRTY 
M Deliverer (Pledgor) 
[[participant]] that delivers the security; 
for a payment order the payee; for a 
[[collateral]] pledge, the pledgor. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 4 
digits. All 4 digits are 
required. 
M End of Block - [[settlement]] Parties :16S:  SETPRTY 
 

---

## Page 68

  Free OCC Pledge  
  10 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] Parties :16R:  SETPRTY 
M Receiver (Pledgee) 
[[participant]] that receives the 
security; for a payment order, the 
payor; for [[collateral]] pledge the 
pledgee. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 
4 digits. All 4 
digits are 
required. 
M End of Block - [[settlement]] Parties :16S:  SETPRTY 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] Parties :16R:  SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] Parties :16S:  SETPRTY 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - [[settlement]] 
Details 
:16S:  SETDET 
 

---

## Page 69

F ree OCC Release of Deposit Request 
1 
Free OCC Release of Deposit Request 
Business Transaction: Free OCC Release of Deposit Request  
ISO Message Type: MT540 – Receive Free 
The Free OCC Release of Deposit Request initiates the release of pledged [[securities]] whether the release 
is a 2- or 3- party release.  Members of the OCC (Options Clearing Corp) may request a release of 
[[collateral]] from the OCC by submitting a release of deposit request. 
Note: If you are a third party (a [[DTC]] [[participant]] but not a [[Member]] of the OCC) for whom pledges were 
submitted by another [[DTC]] [[participant]], you can also request the release of [[collateral]] by submitting an 
OCC Options Release of Deposit Request. The [[DTC]] [[participant]] who entered the pledge on your behalf 
must approve your request via an OCC [[Member]] Release of Deposit Authorization before the [[shares]] are 
returned. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General Information :16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the function of the message 
:23G: NEWM 
M End of Block – General Information :16S: GENL 

---

## Page 70

  Free OCC Release of Deposit Request  
  2 
 
Mandatory Sequence B - Trade Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Trade 
Details 
:16R:  TRADDET  
M Loan Date 
Loan date for a pledge 
or pledge release 
transaction 
:98A: : SETT // yyyymmdd 
The loan date for OCC pledges is always 
19730320. 
M ISIN 
Identification of the 
financial instrument 
(Country Code, [[CUSIP]] 
and Check Digit) 
:35B:  The literal "ISIN" followed by a space 
followed by the 12 character ISIN.  
Note - [[DTC]] does not accept non-U.S. ISIN 
Example - ISIN US1234567891. 
M Business Transaction [[ID]] :22F: :PROC/DTCY/ OP02 
O Narrative – OCC 
Symbology 
Provides additional 
[[settlement]] processing 
information for OCC 
messages.  
:70E: :SPRO// 6*35x 
6 lines of 35 characters each, with each line 
separated by a CRLF (carriage return – line 
feed). 
Each field containing Symbology information 
will be prefixed by the Qualifier as noted 
below.  If more than one field is included on 
one line, the next field qualifier will be 
preceded by a comma (,). 
e.g. 
CLG>XX,CLM>XXXXX 
ACT>XX,ACI>XXXXXXXXXXXXXXX 
SYM>XXXXXX,EXY>YYYY,EXM>MM,EXD>DD 
COT>XX,OPT>X,SPI>NNNNNN,SPD>NNNNNN 

---

## Page 71

  Free OCC Release of Deposit Request  
  3 
 
M/O Field Description Tag Qualifier(s) Content Rules 
XRF>XXXXXXXXXXXXXXXXXXXX 
CAC>XXXXXXXXXXXXXXXXXXXX 
   CLG> OCC Clearing Group [[ID]] 
2x 
New Field – OCC Future Use 
   CLM> OCC Clearing [[Member]] Number 
(aka OCC 3rd Party) 
5x 
OCC Required Field 
Example ‘00005’ 
[[DTC]] required field for Options Release of 
Deposit Request (both two-party & three-
party requests) 
   ACT> OCC Account Type 
2x 
OCC Required Field 
List of values: 
‘C’   –   Customer 
‘F’   –   Firm 
‘M’ –   [[Market Maker]] 
‘Z’   –   Clearing Fund 
[[DTC]] required field for Options Release of 
Deposit Request (two-party request only) 
   ACI> OCC Account / Sub-Account [[ID]] 
15x 
Optional Field 
Example: ‘ABC’ 

---

## Page 72

  Free OCC Release of Deposit Request  
  4 
 
M/O Field Description Tag Qualifier(s) Content Rules 
   SYM> OCC [[Option]] Symbol 
6x 
OCC required field when OCC [[collateral]] Type, 
below, is ‘ED’= Escrow Deposit or ‘SD’ = 
Specific Deposit, otherwise, Optional. 
Example: ‘IBM’ 
[[DTC]] required field for Options Release of 
Deposit Request (three-party request only) 
   EXY> OCC [[Option]] Expiration Year 
4x 
OCC required field when OCC [[collateral]] 
Type, below, is ‘ED’= Escrow Deposit or ‘SD’ 
= Specific Deposit, otherwise, Optional. 
Example: ‘2013’ 
[[DTC]] required field for Options Release of 
Deposit Request (three-party request only) 
   EXM> OCC [[Option]] Expiration Month 
2x 
OCC required field when OCC [[collateral]] 
Type, below, is ‘ED’– Escrow Deposit or ‘SD’ 
– Specific Deposit, otherwise, Optional. 
Example: ‘06’ 
[[DTC]] required field for Options Release of 
Deposit Request (three-party request only) 
   EXD> OCC [[Option]] Expiration Day 
2x 
OCC required field when OCC [[collateral]] 
Type, below, is ‘ED’ – Escrow Deposit or ‘SD’ 
– Specific Deposit, otherwise, Optional. 

---

## Page 73

  Free OCC Release of Deposit Request  
  5 
 
M/O Field Description Tag Qualifier(s) Content Rules 
Example: ‘23’ 
[[DTC]] required field for Options Release of 
Deposit Request (three-party request only) 
   COT> OCC [[collateral]] Type 
2x 
OCC Required Field 
List of Values: 
‘ED’   –  Escrow Deposit 
‘GE’  –  GSE Debt 
‘GS’  –  Government Security 
‘MM’–  Money Market Fund 
‘SD’   –  Specific Deposit 
‘VS’   –  Valued Security 
[[DTC]] required field for Options Release of 
Deposit Request (two-party request only) 
   OPT> OCC [[Option]] Type 
1x 
OCC required field when OCC [[collateral]] 
Type, above, is ‘ED’– Escrow Deposit or ‘SD’ 
– Specific Deposit, otherwise, Optional. 
List of values: 
‘C’   –   Call 
‘P’   –   Put 
   SPI> OCC [[Option]] Strike Price (Integer) 
6n 
OCC required field when OCC [[collateral]] 
Type, above, is ‘ED’– Escrow Deposit or ‘SD’ 
– Specific Deposit, otherwise, Optional. 

---

## Page 74

  Free OCC Release of Deposit Request  
  6 
 
M/O Field Description Tag Qualifier(s) Content Rules 
Example: 000135 
[[DTC]] required field for Options Release of 
Deposit Request (three-party request only) 
   SPD> OCC [[Option]] Strike Price (Decimal) 
6n 
OCC required field when OCC [[collateral]] 
Type, above, is ‘ED’ – Escrow Deposit or ‘SD’ 
– Specific Deposit, otherwise, Optional. 
Example: 502100 
   XRF> Cross Reference Number 
20X 
OCC required field only for [[collateral]] Type of 
Escrow Deposit representing the customer account 
name 
Example ‘12345678901234567890’ 
   CAC> Customer Account Number 
20X 
OCC required field only for [[collateral]] Type of 
Escrow Deposit representing the customer  account 
number 
Example ‘12345678901234567890’ 
M End of Block - Trade 
Details 
:16S:  TRADDET  
 
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 

---

## Page 75

  Free OCC Release of Deposit Request  
  7 
 
M Start of Block - Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial instrument to 
be settled expressed as units such 
as share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole digit is required. 
No more than 9 may be present. 
Fractions are not allowed. A 
decimal comma is always 
required. 
M Pledgor's [[DTCC]] [[participant]] Number 
Pledgor [[DTCC]] [[participant]] number 
:97A: :SAFE// 00009999 
0000 followed by 4 digits.  
All 4 digits are required. 
M End of Block - Financial 
Instrument/Account 
:16S:  FIAC 
 
Mandatory Sequence E - [[settlement]] Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] 
Details 
:16R:  SETDET 
M Release Type 
Indicates the reason for 
the release request. 
:22F: :SETR/DTCY/ 4n 
Valid Values:   
‘0001’   –  Delivery.  
‘0002’  –   Substitution of [[collateral]].  
‘0003’  –   Decrease of [[collateral]].  
‘0004’  –   Release of Excess [[collateral]] 
O [[CNS]] Indicator 
Indicates if [[securities]] 
should be made eligible 
::22F: :NETT/DTCY/ CNSY or CNSN 
‘N’  –   No [[CNS]] processing,  

---

## Page 76

  Free OCC Release of Deposit Request  
  8 
 
M/O Field Description Tag Qualifier(s) Content Rules 
for [[CNS]] processing. ‘Y’   –   [[CNS]] processing is desired. 
If the field is blank, 'N' will be assumed. 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
  
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] Parties :16R:  SETPRTY 
M Deliverer (Pledgor) 
[[participant]] that delivers the 
security; for a payment order the 
payee; for a [[collateral]] pledge, the 
pledgor. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 4 
digits. All 4 digits are 
required. 
M End of Block - [[settlement]] Parties :16S:  SETPRTY 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer’s [[intermediary]]) 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] Parties 
Deliverer’s [[intermediary]] 1 (OCC 
[[Member]]) 
:16R:  SETPRTY  
M OCC [[Member]] - The [[DTCC]] [[participant]] 
number of the Authorizing [[participant]] 
(i.e. the OCC [[Member]]) which will 
authorize the release of the security. 
:95R: :DEI1/DTCYPART/ 00009999 
0000 followed by 4 
digits. All 4 digits 
are required. 
M End of Block - [[settlement]] Parties :16S:  SETPRTY 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 
 
M/O Field Description Tag Qualifier(s) Content Rules 

---

## Page 77

  Free OCC Release of Deposit Request  
  9 
 
M Start of Block - [[settlement]] Parties :16R:  SETPRTY 
M Receiver (Pledgee) 
[[participant]] that receives the security; 
for a payment order, the payor; for a 
[[collateral]] pledge, the pledgee. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 4 
digits. All 4 digits are 
required. 
M End of Block - [[settlement]] Parties :16S:  SETPRTY 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] Parties :16R:  SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] Parties :16S:  SETPRTY 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - [[settlement]] Details :16S:  SETDET 
 

---

## Page 78

F ree OCC Release Return 
1 
Free OCC Release Return  
Business Transaction: Free OCC Release Return  
ISO Message Type: MT542 – Deliver Free 
Free OCC Release Return allows the OCC to release pledged [[securities]] with or without a request from 
the pledgor. Money [[settlement]] occurs outside of [[DTC]]. 
Key: M = Mandatory, O = Optional 
Mandatory Sequence A - General Information 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block – General Information :16R: GENL 
M Sender’s Reference Number 
Sender’s reference number 
:20C: :SEME// 16x 
M Message Function 
Field that identifies the function of the message 
:23G: NEWM 
M End of Block – General Information :16S: GENL 
Mandatory Sequence B - Trade Details 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - 
Trade Details 
:16R: TRADDET  
M Loan Date :98A: : SETT // yyyymmdd 

---

## Page 79

  Free OCC Release Return  
  2 
 
M/O Field Description Tag Qualifier(s) Content Rules 
Loan date for a 
pledge or pledge 
release transaction 
The loan date for OCC pledges is always 19730320. 
M ISIN 
Identification of 
the financial 
instrument 
(Country Code, 
[[CUSIP]] and Check 
Digit) 
:35B:  The literal "ISIN" followed by a space followed by the 
12 character ISIN.  
Note- [[DTC]] does not accept non-U.S. ISIN  
Example-ISIN US1234567891. 
M Business 
Transaction [[ID]] 
:22F: :PROC/DTCY/ OP05 
O Narrative - OCC 
Symbology 
Provides additional 
[[settlement]] 
processing 
information for 
OCC messages.  
:70E: :SPRO// 6*35x 
6 lines of 35 characters each, with each line 
separated by a CRLF (carriage return – line feed). 
Each field containing Symbology information will 
be prefixed by the Qualifier as noted below.  If 
more than one field is included on one line, the 
next field qualifier will be preceded by a comma (,). 
e.g. 
CLG>XX,CLM>XXXXX 
ACT>XX,ACI>XXXXXXXXXXXXXXX 
SYM>XXXXXX,EXY>YYYY,EXM>MM,EXD>DD 
COT>XX,OPT>X,SPI>NNNNNN,SPD>NNNNNN 
XRF>XXXXXXXXXXXXXXXXXXXX 
CAC>XXXXXXXXXXXXXXXXXXXX 
   CLG> OCC Clearing Group [[ID]] 
2x 
New Field  –  OCC Future Use 

---

## Page 80

  Free OCC Release Return  
  3 
 
M/O Field Description Tag Qualifier(s) Content Rules 
   CLM> OCC Clearing [[Member]] Number 
(aka OCC 3rd Party) 
5x 
OCC Required Field 
Example ‘00005’ 
[[DTC]] required field for Options Release of Deposit 
Request (both two-party & three-party requests) 
   ACT> OCC Account Type 
2x 
OCC Required Field 
List of values: 
‘C’   –   Customer 
‘F’   –   Firm 
‘M’ –   [[Market Maker]] 
‘Z ’ –   Clearing Fund 
[[DTC]] required field for Options Release of Deposit 
Request (two-party request only) 
   ACI> OCC Account / Sub-Account [[ID]] 
15x 
Optional Field 
Example: ‘ABC’ 
   SYM> OCC [[Option]] Symbol 
6x 
OCC required field when OCC [[collateral]] Type, below, 
is ‘ED’ – Escrow Deposit or ‘SD’ – Specific Deposit, 
otherwise, Optional. 
Example: ‘IBM’ 
 

---

## Page 81

  Free OCC Release Return  
  4 
 
M/O Field Description Tag Qualifier(s) Content Rules 
[[DTC]] required field for Options Release of Deposit 
Request (three-party request only) 
   EXY> OCC [[Option]] Expiration Year 
4x 
OCC required field when OCC [[collateral]] Type, below, 
is ‘ED’ – Escrow Deposit or ‘SD’ – Specific Deposit, 
otherwise, Optional. 
Example: ‘2013’ 
[[DTC]] required field for Options Release of Deposit 
Request (three-party request only) 
   EXM> OCC [[Option]] Expiration Month 
2x 
OCC required field when OCC [[collateral]] Type, below, 
is ‘ED’ – Escrow Deposit or ‘SD’ – Specific Deposit, 
otherwise, Optional. 
Example: ‘06’ 
[[DTC]] required field for Options Release of Deposit 
Request (three-party request only) 
   EXD> OCC [[Option]] Expiration Day 
2x 
OCC required field when OCC [[collateral]] Type, below, 
is ‘ED’ – Escrow Deposit or ‘SD’ – Specific Deposit, 
otherwise, Optional. 
Example: ‘23’ 
[[DTC]] required field for Options Release of Deposit 
Request (three-party request only) 
   COT> OCC [[collateral]] Type 
2x 
OCC Required Field 

---

## Page 82

  Free OCC Release Return  
  5 
 
M/O Field Description Tag Qualifier(s) Content Rules 
List of Values: 
‘ED’   –   Escrow Deposit 
‘GE’   –   GSE Debt 
‘GS’   –   Government Security 
‘MM’ –   Money Market Fund 
‘SD’    –   Specific Deposit 
‘VS’    –    Valued Security 
[[DTC]] required field for Options Release of Deposit 
Request (two-party request only) 
   OPT> OCC [[Option]] Type 
1x 
OCC required field when OCC [[collateral]] Type, above, 
is ‘ED’- Escrow Deposit or ‘SD’ - Specific Deposit, 
otherwise, Optional. 
List of values: 
‘C’   –   Call 
‘P’   –   Put 
   SPI> OCC [[Option]] Strike Price (Integer) 
6n 
OCC required field when OCC [[collateral]] Type, above, 
is ‘ED’– Escrow Deposit or ‘SD’ – Specific Deposit, 
otherwise, Optional. 
Example: 000135 
[[DTC]] required field for Options Release of Deposit 
Request (three-party request only) 
   SPD> OCC [[Option]] Strike Price (Decimal) 
6n 
OCC required field when OCC [[collateral]] Type, above, 
is ‘ED’ – Escrow Deposit or ‘SD’ – Specific Deposit, 

---

## Page 83

  Free OCC Release Return  
  6 
 
M/O Field Description Tag Qualifier(s) Content Rules 
otherwise, Optional. 
Example: 502100 
   XRF> Cross Reference Number 
20X 
OCC required field only for [[collateral]] Type of Escrow 
Deposit representing the customer account name  
Example ‘12345678901234567890’ 
   CAC> Customer Account Number 
20X 
OCC required field only for [[collateral]] Type of Escrow 
Deposit representing the customer account number  
Example ‘12345678901234567890’ 
M End of Block - 
Trade Details 
:16S:  TRADDET  
 
Mandatory Sequence C - Financial Instrument/Account  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - Financial 
Instrument/Account 
:16R:  FIAC 
M Quantity 
Quantity of financial 
instrument to be settled 
expressed as units such as 
share quantity. 
:36B: :SETT// UNIT/999999999, 
At least 1 whole digit is required. No more 
than 9 may be present. Fractions are not 
allowed. A decimal comma is always 
required. 
M [[DTCC]] Pledgee Bank 
Number 
:97A: :SAFE// 00009999 
0000 followed by 4 digits. All 4 digits are 

---

## Page 84

  Free OCC Release Return  
  7 
 
M/O Field Description Tag Qualifier(s) Content Rules 
[[DTCC]] pledgee bank 
number 
required. 
M End of Block - Financial 
Instrument/Account 
:16S:  FIAC 
 
Mandatory Sequence E - [[settlement]] Details  
 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] Details :16R:  SETDET 
M Release Type 
Indicates the reason for the 
release request. 
:22F: :SETR/DTCY/ 4n 
Valid Values:   
0001   –   Delivery.  
0002   –   Substitution of [[collateral]].  
0003   –   Decrease of [[collateral]].  
0004   –   Release of Excess [[collateral]]. 
 
Mandatory Subsequence E1 - [[settlement]] Parties (Deliverer) 
 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] Parties :16R:  SETPRTY 
M Deliverer (Pledgee) 
[[participant]] that delivers the 
security; for a payment order, the 
payee; for a [[collateral]] pledge 
return, the pledgee bank. 
:95R: :DEAG/DTCYPART/ 00009999 
0000 followed by 4 
digits. All 4 digits are 
required. 
M End of Block - [[settlement]] Parties :16S:  SETPRTY 
 

---

## Page 85

F ree OCC Release Return 
8 
Mandatory Subsequence E1 - [[settlement]] Parties (Receiver) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] Parties :16R: SETPRTY 
M Receiver (Pledgor) 
[[participant]] that receives the 
security; for a payment order, the 
payor; for a [[collateral]] pledge 
return, the pledgor. 
:95R: :REAG/DTCYPART/ 00009999 
0000 followed by 4 
digits. All 4 digits are 
required. 
M End of Block - [[settlement]] Parties :16S: SETPRTY 
Mandatory Subsequence E1 - [[settlement]] Parties (Place of [[settlement]]) 
M/O Field Description Tag Qualifier(s) Content Rules 
M Start of Block - [[settlement]] Parties :16R: SETPRTY 
M Place of [[settlement]] 
[[DTCC]] BIC Number 
:95P: :PSET// DTCYUS33 
M End of Block - [[settlement]] Parties :16S: SETPRTY 
M/O Field Description Tag Qualifier(s) Content Rules 
M End of Block - [[settlement]] Details :16S: SETDET 