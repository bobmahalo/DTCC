---
title: "Manual Cost Basis Template Rules and Best Practice Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs146_manual_transfer_statement-rules-bp_2023Jun5.pdf"
pages: 16
size: "481.0 KB"
category: "CBRS"
ingested_on: "2026-06-05"
---

# Manual Cost Basis Template Rules and Best Practice Guide

**Original File:** [cbrs146_manual_transfer_statement-rules-bp_2023Jun5.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs146_manual_transfer_statement-rules-bp_2023Jun5.pdf)  
**Category:** CBRS  
**Total Pages:** 16  
**File Size:** 481.0 KB  

---

## Page 1

COST BASIS REPORTING SERVICE 
(CBRS)
MANUAL COST BASIS TRANSFER TEMPLATE RULES AND BEST PRACTICE 
GUIDE 
A
UGUST 6, 2018 


---

## Page 2

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
About This User Guide 2 
1. ABOUT THIS USER GUIDE 
This user guide is intended to be used with the Cost Basis Manual Transfer Statement and NOT [[DTCC]]’S Cost 
Basis Report Service (CBRS). This guide provides descriptions and best practices for the fields on the Cost 
Basis Manual Statement. For additional examples and more information regarding best practices, business 
processes, and information flow, see the CBRS User Guide available on the [[DTCC]] Learning Center. 
Note: 
[[DO]] not use the manual transfer statement with the Cost Basis Reporting Service (CBRS).  
Cost Basis Contact List 
FIS Global has created a Cost Basis Forum site for users to provide and update their cost basis contacts and 
view other contacts for purposes to passing manual cost basis. To obtain access to this forum site, email 
FIS.CBRS.Contacts@fisglobal.com. After setup is complete, you will receive a confirmation email. After access 
has been granted, the forum site is available at 
https://projects.wsc.com/public/index.php?path_info=projects/cbcs-forum.
   
For more information, email FIS.CBRS.Contacts@fisglobal.com.  

---

## Page 3

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 3 
2. MANUAL COST BASIS TRANSFER STATEMENT BEST 
PRACTICES 
The following table provides the field information and comments to enable you to enter the values in the 
Manual Cost Basis Transfer statement: 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
Record Type  A 1  A/N  REQ  Values: 
• A = [[Asset]] 
• T = Tax Lot 
Record Content 
Indicator 
B 2 A/N REQ Values: 
• 01 = Original tax lot record 
• 02 = Corrected tax lot record 
• 03 = Rejected 
• 04 = Request 
Rule: 
If this field on the [[Asset]] Record is 02 = Corrected [[Asset]] 
record, this field in at least one of the accompanying tax lot 
records must have a value of 02 = Corrected tax lot record. 
Transaction 
Type 
C 2 A/N  REQ  Firm to Firm:  
• 01 = ACATS  
• 02 = Free [[DTC]] Deliver Order (Non-ACATS) 
• 03 = Valued [[DTC]] Deliver Order 
• 04 = Conversion 
• 05 = Mutual Fund Transfer (Non-ACATS) [change of 
[[Broker]]-dealer] 
• 06 =Fed  
• 07 = Physical Movement [[settlement]] (Non-ACATS) 
• 08 = OCC transfer (Non-ACATS) 
• 09 = Non-Domestic Depository (Foreign) 
• 10 = Other 
• 11 – 25 = Reserved for future use 
Firm & [[transfer agent]]: 
• Agent submits/firm receives CBRS original/corrected 
record: 
o 26 = [[DWAC]] Deposit 
o 27 = Certificate Deposit 
o 28 = [[DRS]] Profile/[[DO]] 
o 29 – 35 = Reserved for future use 
• Firm submits/agent receives CBRS original/corrected 
record: 
o 36 = [[DWAC]] Withdrawal 
o 37 = Withdrawal by Transfer (WT) 
o 38 – 40 = Reserved for future use 

---

## Page 4

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 4 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
• Either Agent submits/firm receives or Firm submits/agent 
receives CBRS original/corrected record: 
o 41 = Direct Presentation 
o 42 – 45 Reserved for future use 
Firm & Fund (In-kind Mutual Fund Transfers): 
• Fund submits/firm receives CBRS original/corrected 
record: 
o 46 = Fund to Firm Mutual Fund Transfer [via ACATS 
Fund/SERV interface; also known as PTF, Position 
Transfer Fund ACATS transfer type] 
o 47 – 50 = Reserved for future use 
• Firm submits/fund receives CBRS original/corrected 
record: 
o 51 = Firm to Fund Mutual Fund Transfer [via ACATS 
Fund/SERV interface; also known as PTF, Position 
Transfer Fund ACATS transfer type] 
o 52 – 55 = Reserved for future use 
• Either fund submits/firm receives or firm submits/fund 
receives CBRS original/corrected record: 
o 56 = Networking Transaction 
o 57 = Manual Mutual Fund Transfer 
o 58 – AIP  
o 59 – Alternative Investment (Non-AIP) 
o 60 – 65 = Reserved for future use 
Receiver 
Customer 
Account 
Number  
D 20  A/N  REQ  Populate this field with the customer account number at the 
firm that received the [[Asset]] transfer. 
Deliverer 
Customer 
Account 
Number  
E 20  A/N  
COND  Populate this field with the customer account number at the 
firm that delivered the [[Asset]] transfer. 
Not required for transaction type 26, 27, 28, 36, 37 
[[Asset]] Category F 4 A/N REQ Populate this field with the [[Asset]] category that corresponds to 
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

---

## Page 5

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 5 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
• MFNM = Mutual Fund Non-Money Market 
• MUNI = Municipal [[Bonds]] 
• OPT = Options 
• REIT = Real Estate Investment Trust 
• RGT = Right 
• UARP = [[UIT]] (Auction Rate Preferred) 
• UDSC = [[UIT]] (Deferred Sale Charge) 
• [[UIT]] = Unit Investment Trust 
• UNT = Units 
• WAR = Warrant 
• ZERO = Zero Coupon [[Bonds]]  
This field must equal MFNM, for the following transaction types: 
• 46 = Fund to Firm Mutual Fund Transfer 
• 51 = Firm to Fund Mutual Fund Transfer 
• 56 = Networking Transaction 
• 5 7 = Manual Mutual Fund Transfer 
Otherwise, the receiving firm rejects the record. 
Value OPT is required for the Transaction Type 08 = OCC 
transfer (Non-ACATS). Value OPT is valid only for the following 
transaction types:  
• 01 = ACATS 
• 04 = Conversion 
• 06 = FED 
• 08 = OCC transfer (Non-ACATS) 
• 09 = Non-Domestic Depository 
• 10 = Other 
Otherwise, the receiving firm rejects the record. 
ISIN Country 
Code  
G 2  A/N  REQ Populate this field with the Industry recognized two-character 
country code 
ISIN Security 
Issue [[ID]] 
([[CUSIP]] 
number) 
H 9  A/N  REQ Populate this field with the industry recognized [[CUSIP]]. If there 
is no Industry recognized [[CUSIP]], the field may be populated 
with the USER [[CUSIP]] maintained on the delivering firm’s 
system.  
ISIN Security 
Check Digit 
I 1 A/N REQ 
Required if ISIN Country Code is anything but blank (presumed 
US) or US, and ISIN Security Issue [[ID]] ([[CUSIP]] number) is 
populated.  
Put/Call 
Indicator 
J 1 A/N COND Values: 
• C = Call  
• P = Put 
Required if the [[Asset]] Category is OPT. 
Allowed for the following transaction types: 
• 01 = ACATS 
• 04 = Conversion 
• 06 = Fed 
• 08 = OCC transfer (Non-ACATS) 
• 09 = Non-Domestic Depository 

---

## Page 6

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 6 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
• 10 = Other 
If this field is populated for any other transaction type, the 
receiving firm rejects the record. 
[[Option]] Symbol  K 6  A/N  COND  Required if the [[Asset]] Category is OPT. 
Allowed for the following transaction types: 
• 01 = ACATS 
• 04 = Conversion 
• 06 = Fed 
• 08 = OCC transfer (Non-ACATS) 
• 09 = Non-Domestic Depository 
• 10 = Other 
If this field is populated for any other transaction type, the 
receiving firm rejects the record. 
[[Option]] 
Expiration Date  
L 8 A/N  
COND  Required if the [[Asset]] Category is OPT. 
Allowed for the following transaction types: 
• 01 = ACATS 
• 04 = Conversion 
• 06 = Fed 
• 08 = OCC transfer (Non-ACATS) 
• 09 = Non-Domestic Depository 
• 10 = Other 
If this field is populated for any other transaction type, the 
receiving firm rejects the record. 
Format: CCYYMMDD 
[[Option]] Strike 
Price  
M 8  NUM  
COND  Required if the [[Asset]] Category is OPT. 
Allowed for the following transaction types: 
• 0 1 = ACATS 
• 04 = Conversion 
• 06 = Fed 
• 08 = OCC transfer (Non-ACATS) 
• 09 = Non-Domestic Depository 
• 10 = Other 
If this field is populated for any other transaction type, the 
receiving firm rejects the record. 
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places.
 
[[Asset]] 
Description  
N 140  A/N  
COND  Required when ISIN is not populated and when the 
Transaction Type is 41 = Direct Presentation. 
Contains a text-based description of the [[Asset]].  
Quantity  O 17 A/N  REQ  Total associated with the row. For rows representing the full 
[[Asset]], include the total quantity being transferred for that 
[[CUSIP]] and account. For rows representing tax lots, include the 
quantity for that lot. 

---

## Page 7

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 7 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
The receiving firm will sum up the tax lot quantities and 
compare them to the quantity in the row representing the [[Asset]]. 
If the sum of the tax lot quantities does not equal the value in 
this field, the receiving firm rejects the record. 
Zero is not a valid value for this field. 
Position of decimal denoted by a ‘.’ (period). Supports up to 
four decimal places.  
[[settlement]] Date 
of Transfer 
P 8 A/N REQ [[settlement]] date of the transfer of the security. 
If submitted date is not a valid calendar date, the receiving firm 
rejects the record.   
Format: CCYYMMDD 
Position Code  Q 1  A/N  REQ Values: 
• L = Long position  
• S = [[short position]] 
If the transaction type is 46, 51, 56, 57, this value must be L = 
Long position. 
[[shares]] to Cover 
Short Indicator 
R 1 A/N COND Values:  
• Y=Yes 
• N=No 
The submitter should populate this field with a Y when it 
receives a customer request to deliver [[shares]] to satisfy a short 
position at the receiving firm. The receiving firm will then expect 
cost basis to [[Close Out]] the short. 
[[default]] value is N 
ACATS [[Asset]] 
Sequence 
Number 
S 6 NUM COND Required when the transaction type is 01 = ACATS and the 
[[settlement]] Date of Transfer is later than July 26, 2012. Format 
is six digits. Value in this field must be numeric and greater 
than zero. Use leading zeros if necessary.  
This field should be the ACATS [[Asset]] Sequence Number from 
the original transfer. 
Noncovered / 
Pending 
Indicator 
T 2 A/N COND Should be used when the basis is unknown, unverifiable, or 
pending. Values: 
• 01 = Noncovered lot 
• 02 = Noncovered account 
• 03 = Pending 
• 04 = Certificate in Customer Name 
Required if the Acquisition Date field is blank. Otherwise, the 
receiving firm rejects the record. 
Best Practice 
If this field is blank, the receiver will consider the lot covered if 
the Position Code is L = Long. If the Position Code is S = 
Short, the covered status of the position is not determined until 
the [[shares]] are acquired. 

---

## Page 8

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 8 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
Gifted or 
Inherited 
Indicator 
U 2 A/N COND Values: 
• 01 = Gifted 
• 02 = Inherited 
• 03 = Inherited then Gifted 
If the Date of Gift is populated and this field is blank the 
receiving firm rejects the record. 
If the Fair Market Value as of Date of Gift is populated and 
this field is populated with a value other than 01 = Gifted or 03 
= Inherited then Gifted, or is blank, the receiving firm rejects 
the record. 
Date of Gift V 8 A/N COND This field is required if Fair Market Value as of Date of Gift is 
populated. Otherwise, the receiving firm rejects the record. 
Format: CCYYMMDD 
Fair Market 
Value as of 
Date of Gift 
W 16 A/N COND Fair market value of the tax lot as of the date of gift. 
Position of decimal denoted by a ‘.’ (period). Format is 8 digits 
to the left of the decimal, and 8 digits to the right of the decimal. 
 
Best Practice 
Must be populated if known for a gifted security. 
Exchange Rate 
for FMV as of 
Date of Gift 
X 18 A/N COND Required if ISO Currency Code is not USD and Fair Market 
Value as of Date of Gift is populated. 
Spot exchange rate used to convert the Fair Market Value as of 
Date of Gift. Rate is the amount of local currency equal to one 
dollar. For example, if ISO Currency Code = JPY, the value in 
this field is 86.4428 for acquisition date December 01, 2009. 
Leave this field blank if ISO Currency Code = USD. If ISO 
Currency Code = USD and submitter populates this field with 
anything but a blank value, the receiving firm rejects the record. 
If Fair Market Value as of Date of Gift field is blank, and this 
field is populated, the receiving firm rejects the record. 
Acquisition Date 
of Tax Lot 
Y 8  A/N  COND Trade or acquisition date for the tax lot. For lots affected by 
wash sales, this is the adjusted acquisition date. This date is 
used to determine gain or loss, and short term or long term 
holding period. 
This field is required unless the Zero Basis Indicator is 02 = 
Unknown. If this field is populated and the Zero Basis 
Indicator is 02 = Unknown, the receiving firm rejects the 
record. 
If this field is blank, Noncovered/Pending Indicator field must 
be populated.  
This date must be equal to or earlier than the date in the 
Original Acquisition Date for Wash Sale Adjustment field. 
Otherwise, the receiving firm rejects the record.  
Format: CCYYMMDD  

---

## Page 9

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 9 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
19010101 is a valid value and signifies various dates Allowed 
for average cost [[Mutual Funds]] acquired at least five years from 
the date of the transfer.  
Original 
Acquisition Date 
for Wash Sale 
Adjustment 
Z 8 A/N COND Used only for wash sales. The acquisition date for a lot that has 
been adjusted for wash sales. 
Format: CCYYMMDD 
Best Practice 
Must be populated if the tax lot is the result of a wash sale. 
Wash Sale 
Adjustment 
Amount 
AA 16 A/N COND (A.K.A. Disallowance amount) - Used only for wash sales. 
Amount in USD of the disallowed loss from a wash sale, which 
has been added to the cost basis. 
This field should be greater than zero, if the Original Acquisition 
Date for Wash Sale Adjustment is populated. If this field is 
populated and Original Acquisition Date for Wash Sale 
Adjustment is blank, the receiving firm rejects the record. 
If a Wash Sale occurred on a fixed income product (CDCP, 
CORP, GOVT, MUNI, MBS, or ZERO), then both the Wash 
Sale Adjustment Amount and the Original Acquisition Date for 
Wash Sale Adjustment are required to be populated if the tax 
lot is covered. 
If Original Acquisition Date for Wash Sale Adjustment is not 
populated then the Wash Sale Amount should be blank. (zero 
can be accepted in place of blank.)  
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places.
 
Best Practice:   
• Current Cost Basis for Fixed income [[securities]] should not 
be adjusted for the disallowed loss, resulting from a wash 
sale. 
• For all other security types, the original and current cost 
basis should be adjusted for the disallowed amount. 
Currency Code  AB 3  A/N  REQ  Valid values for this field are the standard ISO Currency Codes 
(for example: USD, CAD, JPY).  
If populated value is not USD, the ISO Currency Code is the 
currency corresponding to the value in the Exchange Rate 
field.  
Exchange Rate AC 18 A/N COND Required if ISO Currency Code is not USD. 
Spot exchange rate used when converting the Tax Lot Current 
Cost. Rate is the amount of local currency equal to one dollar. 
For example, if ISO Currency Code = JPY, the value in this 
field is 86.4428 for acquisition date 12/01/2009. 
Leave this field blank if ISO Currency Code = USD. If ISO 
Currency Code = USD and submitter populates this field with 
anything but a blank value, the receiving firm rejects the record. 

---

## Page 10

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 10 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
Tax Lot Original 
Cost 
AD 17  A/N  COND This field is required if: 
• Covered [[Asset]] and the [[Asset]] Category is: 
o CDCP = CD or Commercial Paper 
o CORP = Corporate Bond 
o FDEB = Foreign Debt 
o GOVT = US Govt. and Govt. Agency 
o MBS = Mortgage Backed [[securities]] 
o MUNI = Municipal [[Bonds]] 
o ZERO = Zero Coupon [[Bonds]] 
• Non-covered/ Pending Indicator is blank, unless Zero 
Basis Indicator is 02 = Unknown. 
Total original cost, in USD, of the tax lot. This value should be 
the cost of the security when it was acquired. 
For equities, this value should be adjusted for wash sales. 
For covered fixed income [[securities]], this value should not be 
adjusted for wash sales. 
Valid values include zeroes. A blank value is allowed when Tax 
Lot Original Cost is unknown.  
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places. 
Best Practice 
Include Total Original Cost for the [[Asset]] backed [[securities]]. 
Tax Lot Current 
Cost 
AE 17 A/N  COND This field is required unless the [[Asset]] Category = MBS or Zero 
Basis Indicator is 02 = Unknown 
This value should be in USD. The current cost should be 
adjusted for wash sales, when the [[Asset]] is not a fixed income 
security. For fixed income [[securities]], the current cost should be 
modified as of the [[settlement]] date of the transfer for: corporate 
actions, return of principal, OID, accretion/amortization, etc.  
Valid values include zeroes or blanks. A blank value is allowed 
when Tax Lot Current Cost is unknown 
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places. 
Best Practices 
If Position Code is S = Short and the security is covered by 
the legislation, this field should equal the gross proceeds of the 
[[short position]]. 
For a non-covered average cost mutual fund position with at 
least one lot with unknown basis, populate this field with the 
actual current cost for each lot with known basis. 
Include adjusted cost for Fixed Income [[securities]] other than 
[[Asset]] Backed [[securities]]. 
Tax Lot Current Cost should be populated for Section 1256 
options with Acquisition Basis. 

---

## Page 11

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 11 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
Zero Basis 
Indicator 
AF 2 A/N COND Required if the Tax Lot Current Cost is zero or blank. 
Values: 
• 01 = True Zero 
• 02 = Unknown 
If Tax Lot Current Cost is populated with spaces, this field 
must be 02 = Unknown. Otherwise, the receiving firm rejects 
the record. 
If Tax Lot Current Cost is zero and this field is blank, the 
receiving firm rejects the record. 
If either Covered, or the Non-covered/ Pending Indicator is 
blank, and this field is 02 = Unknown, then the receiving firm 
rejects the record. 
Tax Lot Original 
Unit Price  
AG 17  A/N COND The per share price, in USD, of the original trade. 
Valid values include zeroes. A blank value is allowed when Tax 
Lot Original Unit Price is unknown. 
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places. 
Best Practice 
Should only populate this field for a mortgage-backed security. 
Accrue Market 
Discount 
Election 
AH 1 A/N COND Election to accrue market discount using a constant yield.  
Values: 
• Y = Yes 
• N = No 
This field is required if Non-covered/ Pending Indicator is blank 
and the [[Asset]] Category is one of the following: 
• CORP = Corporate Bond 
• GOVT = US Govt. and Govt. Agency 
• MUNI = Municipal [[Bonds]] 
• ZERO = Zero Coupon [[Bonds]] 
• The field may be populated for CDCP, CORP, FDEB, 
GOVT, MUNI, or ZERO where the Non-covered/Pending 
Indicator is populated The field may also be populated for 
[[Asset]] Category MBS, CBRS will pass the record. If this field is 
populated for any other [[Asset]] category, the receiving firm 
rejects the record.  
Include Market 
Discount in 
Income Election 
AI 1 A/N COND Election to include market discount in income currently. 
Values: 
• Y = Yes 
• N = No 
This field is required if [[Asset]] Category is CORP = Corporate 
Bond, GOVT = US Govt. and Govt. Agency, MUNI = Municipal 
[[Bonds]], or ZERO = Zero Coupon [[Bonds]] and Non-
covered/Pending Indicator is blank. The field may be populated 

---

## Page 12

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 12 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
for CDCP, CORP, FDEB, GOVT, MUNI, or ZERO where the 
Non-covered/Pending Indicator is populated. The field may also 
be populated for the [[Asset]] Category MBS. If this field is 
populated for any other [[Asset]] category, the receiving firm 
rejects the record.  
Amortize 
[[Premium]] 
Election 
AJ 1 A/N COND Election to amortize [[Premium]]. 
Values: 
• Y = Yes 
(Means the client has been amortizing the [[Premium]]) 
• N = No  
(Means the client elected not to amortize the [[Premium]]) 
This field is required if [[Asset]] Category is CORP = Corporate 
Bond, GOVT = US Govt. and Govt. Agency, MUNI = Municipal 
[[Bonds]], or ZERO = Zero Coupon [[Bonds]] and Non-covered / 
Pending Indicator is blank.  
The field may be populated for CDCP, CORP, FDEB, GOVT, 
MUNI, or ZERO and Non-covered / Pending Indicator is 
populated. This field may also be populated for [[Asset]] 
Category MBS. If this field is populated for any other [[Asset]] 
category, the receiving firm rejects the record.  
Spot Rate 
Election 
AK 1 A/N COND Spot rate election for interest accruals with respect to a 
covered debt instrument denominated in a currency other than 
U.S. Dollar. 
Values: 
• Y = Yes   
• N = No 
This field is required if [[Asset]] Category is CORP = Corporate 
Bond, GOVT = US Govt. and Govt. Agency, MUNI = Municipal 
[[Bonds]], or ZERO = Zero Coupon [[Bonds]] and Non-
covered/Pending Indicator is blank. The field may be populated 
for CDCP, CORP, FDEB, GOVT, MUNI, or ZERO and Non-
covered/Pending Indicator is populated. This field may also be 
populated for [[Asset]] Category MBS. If this field is populated for 
any other [[Asset]] category, the receiving firm rejects the record.  
Market Discount AL 16 A/N  OPT  This field may be populated for [[Asset]] Categories CDCP, 
CORP, FDEB, GOVT, MBS, MUNI, or ZERO. If this field is 
populated for any other [[Asset]] category, the receiving firm 
rejects the record. 
Valid values include zeroes. A blank value is allowed when 
Market Discount is unknown or not applicable  
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places. 
Bond [[Premium]] AM 16 A/N  OPT  Allowed for [[Asset]] Categories CDCP, CORP, FDEB, GOVT, 
MBS, MUNI, or ZERO. If this field is populated for any other 
[[Asset]] category, the receiving firm rejects the record. 

---

## Page 13

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 13 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
Valid values include zeroes. A blank value is allowed when 
Bond [[Premium]] is unknown or not applicable. 
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places. 
Best Practice: 
Bond [[Premium]] varies depending on how the Amortization 
[[Premium]] Election was populated.  
• If yes, the amount of the bond [[Premium]] reported should be 
as of the last interest payment (coupon) date. 
• If no, the bond [[Premium]] field should be zero. 
Acquisition 
[[Premium]] 
AN 16 A/N  OPT  Allowed for [[Asset]] Categories CDCP, CORP, FDEB, GOVT, 
MBS, MUNI, or ZERO. If this field is populated for any other 
[[Asset]] category, the receiving firm rejects the record. 
Valid values include zeroes. A blank value is allowed when 
Acquisition [[Premium]] is unknown or not applicable. 
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places. 
Best Practice: 
Acquisition [[Premium]] must be adjusted daily and the amount 
reported should be as of the [[settlement]] date of the transfer. 
Accrued OID AO 16 A/N  OPT  Allowed for [[Asset]] Categories CDCP, CORP, FDEB, GOVT, 
MBS, MUNI, or ZERO. If this field is populated for any other 
[[Asset]] category, the receiving firm rejects the record. 
Valid values include zeroes. A blank value is allowed when 
Accrued OID is unknown or not applicable. 
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places. 
Last Adjustment 
Date 
AP 8 A/N COND Date of last interest accrual for purposes of calculating the 
current cost of a fixed income security. This field is required 
for covered fixed income assets submissions. 
Allowed field for the [[Asset]] category:   
• CDCP = CD or Commercial Paper 
• CORP = Corp Bond 
• FDEB = Foreign Debt 
• GOVT = US Govt. and Govt. Agency 
• MBS = Mortgage backed  
• MUNI = Municipal [[Bonds]] 
• ZERO = Zero Coupon [[Bonds]] 
Field should be blank for any other [[Asset]] category, otherwise, it 
will be rejected. 
Format: CCYYMMDD 
If submitted, date must be a valid calendar date. May be 
spaces or valid calendar date. Zeroes are not a valid value. 

---

## Page 14

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 14 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
Carryover 
Offset 
AQ 16 A/N OPT The amount of Amortized Bond [[Premium]] to be carried over to 
the date of disposition (The Current Cost basis should NOT be 
adjusted by this amount). The Carryover Offset amount must 
be carried over until the disposition of the [[Asset]]
. 
Allowed field for the [[Asset]] category:   
• CDCP = CD or Commercial Paper 
• CORP = Corp Bond 
• FDEB = Foreign Debt,  
• GOVT = US Govt. and Govt. Agency 
• MBS = Mortgage backed 
• MUNI = Municipal [[Bonds]] 
• ZERO = Zero Coupon [[Bonds]] 
Field should be blank or zeroes for any other [[Asset]] category, 
otherwise it will be rejected.  
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places. 
Prior Year Mark 
to Market 
AR 16 A/N COND Use only when Section 1256 options have transferred. 
When reporting cost basis of 1256 options: 
• If the 1256 [[Option]] was acquired prior to year-end of the 
previous year, use the year end (fair market value). Year-
end fair market value used in reporting unrealized profit or 
loss on the open contracts in box 10 of the 1099-B 
• If the 1256 [[Option]] was acquired in the same year as the 
transfer, populate the Prior Year Mark to Market with zero. 
The [[Asset]] category must equal options for 1256 [[Option]] 
submissions, any other selection will reject when the Prior Year 
Mark to Market field is populated. 
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places. 
[[settlement]] Date AS 8 A/N COND [[settlement]] date of the original acquisition for the Tax Lot being 
transferred. 
This field is required for covered fixed income. Fixed 
income [[Asset]] categories include: 
• CDCP = CD or Commercial Paper 
• CORP = Corp Bond,  
• FDEB = Foreign Debt,  
• GOVT = US Govt. and Govt. Agency 
• MBS = Mortgage backed 
• MUNI = Municipal [[Bonds]] 
• ZERO = Zero Coupon [[Bonds]] 
Format: CCYYMMDD 
If submitted date is not a valid calendar date, or is in the future, 
the receiving firm rejects the record. Zeroes are not a valid 
value. 
May be spaces or valid calendar date.  

---

## Page 15

Manual Cost Basis Transfer Template Rules and Best Practice Guide 
Manual Cost Basis Transfer Statement Best Practices 15 
FIELD NAME COLUMN LENGTH TYPE OPT/ 
REQ/ 
COND  
COMMENTS 
Best Practice: 
For [[Asset]] categories that this field is required, If [[settlement]] 
Date is unknown, this field should be populated with the date 
the accrual calculations began. 
Accrued 
Unrealized 
Market Discount 
AT 16 A/N OPT The amount of market discount on the fixed income security 
that has been accrued but not realized. 
Position of decimal denoted by a ‘.’ (period). Supports up to two 
decimal places. 
 
 

---

## Page 16

© 2023 The Depository Trust & Clearing Corporation. All rights reserved.   
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.  
Recipient acknowledges that the CBRS Record Layouts ("Information") provided herein are the property of The Depository 
Trust & Clearing Corporation and/or subsidiaries (collectively, "[[DTCC]]"). Recipient agrees to protect the proprietary position 
of [[DTCC]], and further agrees that without [[DTCC]]'s prior written consent, Recipient shall not publish, transfer or sell such 
Information or copies thereof, or any extracts or any of the Information therefrom in any form, or summaries thereof, to any 
other person or organization, or permit any other person or organization to use or distribute such Information, including 
clients of a recipient, who, to a Recipient's knowledge, provides the Information to an entity that does so; provided, 
however, that this restriction shall not be deemed to prohibit the use of the Information by Recipient for its internal purposes 
in the ordinary course of clearing and settling its [[securities]] transactions through [[DTCC]]. 
Doc Info: Jun 5, 2023 
Publication Code: CBRS146 
Service: Cost Basis Reporting Service (CBRS) 
Title: Manual Cost Basis Template Rules and Best Practice Guide 
FOR MORE INFORMATION 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or
 visit us on the web at: 
www.dtcclearning.com 