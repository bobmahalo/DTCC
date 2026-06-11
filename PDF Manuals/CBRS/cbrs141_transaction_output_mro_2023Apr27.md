---
title: "Cost Basis Transaction MRO: AutoRoute Production 02400264/Test 02980264"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs141_transaction_output_mro_2023Apr27.pdf"
pages: 15
size: "388.4 KB"
category: "CBRS"
ingested_on: "2026-06-05"
---

# Cost Basis Transaction MRO: AutoRoute Production 02400264/Test 02980264

**Original File:** [cbrs141_transaction_output_mro_2023Apr27.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs141_transaction_output_mro_2023Apr27.pdf)  
**Category:** CBRS  
**Total Pages:** 15  
**File Size:** 388.4 KB  

---

## Page 1

 
 
COST BASIS REPORTING SERVICE 
(CBRS) 
COST BASIS TRANSACTION MRO 
AutoRoute Production 02400264 / PSE 02980264 
APRIL 27, 2023 
 
 
 


---

## Page 2

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 2 
COST BASIS TRANSACTION MRO 
The following table show the output Cost Basis Transaction MRO: AutoRoute Production 02400264 / 
PSE 02980264 record layout: 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
Record Type  2 1 2 A/N  • AO = [[Asset]] Output 
• TO = Tax Lot Output  
Record Length  4 3 6 NUM  • [[Asset]] Output 1500 
• Tax Lot Output 1500 
Distribution Side  1 7 7 A/N  • S = Submitting User 
• B = Both Receiving [[participant]] and 
Submitting User 
Cost Basis Control Number  17 8 24 A/N  Cost Basis system generated. 
Format: CCYYDDDCBNNNNNNNN 
For example, 2011255CB00000001 
Processing Date  8 25 32 A/N  Format: CCYYMMDD  
Filler  7 33 39 A/N  Reserved for future use. Spaces. 
Distribution Firm Number  8 40 47 A/N   
Distribution Firm Type 6 48 53 A/N  
System Action  1 54 54 A/N  • 1 = System Accepted 
• 2 = System Modified 
• 3 = System Rejected  
System Reject Reason  2 55 56 A/N  • 01 = Invalid Field 
• 02 = Associated Record is Invalid 
• 03 = Invalid Length Record 
• 04 = Invalid Physical Sequence – [[Asset]] 
record not present 
• 05 = Invalid Physical Sequence – tax lot 
record(s) not present 
• 06 = Reserved for future use. 
• 07 = Invalid Accumulated Quantity 
• 08 = Reserved for future use. 
• 09 = No Corrected Tax Lot present for 
corrected [[Asset]] Input 
• 10 = Invalid Physical Sequence – Tax Lot 
invalid with [[Asset]] Input reject or request. 
• Space = Not rejected  
 

---

## Page 3

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 3 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
LPA Number 8 57 64 A/N Submitting [[transfer agent]]’s Limited 
[[participant]] Account (LPA) number, used only 
for Transaction Type 28 = [[DRS]] Profile/[[DO]] 
with Record Content Indicator 01 = Original 
[[Asset]] Record or 02 = Corrected [[Asset]] 
Record. 
LPA Type 6 65 70 A/N Submitting [[transfer agent]]’s Limited 
[[participant]] Account (LPA) number type, used 
only for Transaction Type:  
28 = [[DRS]] Profile/[[DO]] with Record Content 
Indicator  
01 = Original [[Asset]] Record  
–or– 
02 = Corrected [[Asset]] Record 
Always DTCPRT. 
Filler  19 71 89 A/N  Reserved for future use. Spaces. 
Data area for [[Asset]] Input Status 
and [[Asset]] Input (A)  
     Used when [[Asset]] Input (A) record exists. 
AO Record Type Status  1 90 90 A/N  Status code values: 
• 0 = Valid 
• 1 = System Changed 
• 2 = Error 
• Space = No Change  
AO Record Length Status  1 91 91 A/N  Status code values: 
• 0 = Valid 
• 1 = System Changed 
• 2 = Error 
• Space = No Change 
AO Record Content Indicator 
Status 
1 92 92 A/N  Status code values: 
• 0 = Valid 
• 1 = System Changed 
• 2 = Error 
• Space = No Change 
AO Transaction Type Status 1 93 93 A/N Status code values: 
• 0 = Valid 
• 1 = System Changed 
• 2 = Error 
• Space = No Change 

---

## Page 4

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 4 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
AO Transfer Control Number Status  1 94 94 A/N  See status code values. 
AO Alternate Control Number 
Status 
1 95 95 A/N See status code values. 
AO Contra Firm Number Status  1 96 96 A/N  See status code values. 
AO Contra Firm Type Status 1 97 97 AN See status code values. 
AO Submitting Firm Number Status  1 98 98 A/N  See status code values. 
AO Submitting Firm Type Status 1 99 99 AN See status code values. 
Filler 1 100 100 A/N  Reserved for future use. Spaces. 
AO Receiver Customer Account 
Number Status  
1 101 101 A/N  See status code values. 
AO Deliverer Customer Account 
Number Status  
1 102 102 A/N  See status code values. 
AO ISIN Country Code Status  1 103 103 A/N  See status code values. 
AO ISIN Security Issue [[ID]] Status  1 104 104 A/N  See status code values. 
AO ISIN Security Check Digit 
Status  
1 105 105 A/N  See status code values. 
AO Put – Call Indicator Status 1 106 106 A/N  See status code values. 
AO [[Option]] Symbol Status  1 107 107 A/N  See status code values. 
AO [[Option]] Expiration Date Status  
–or– 
Last Factor Date (for MBS) Status 
1 108 108 A/N  See status code values. 
AO [[Option]] Strike Price Integer 
Status 
1 109 109 A/N  See status code values. 
AO [[Option]] Strike Price Decimal 
Status  
1 110 110 A/N  See status code values. 
AO [[Asset]] Description Status  1 111 111 A/N  See status code values. 
AO [[Asset]] Category Status  1 112 112 A/N  See status code values. 
AO Total Position Quantity Status  1 113 113 A/N  See status code values. 
AO Date Transfer was Initiated 
Status 
1 114 114 A/N See status code values. 
AO [[settlement]] Date of Transfer 
Status 
1 115 115 A/N See status code values. 

---

## Page 5

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 5 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
AO Position Code Status  1 116 116 A/N  See status code values. 
Filler 3 117 119 A/N  Reserved for future use. Spaces. 
AO Disposition Method Used 
Status  
1 120 120 A/N  See status code values. 
AO [[shares]] to Cover Short Status 1 121 121 A/N See status code values. 
AO Firm Reject Reason Code 
Status 
1 122 122 A/N See status code values. 
AO ACATS [[Asset]] Sequence 
Number Status 
1 123 123 A/N See status code values. 
Filler 25 124 148 A/N Reserved for future use. Spaces. 
AO Record Type  1 149 149 A/N  A 
AO Record Length  4 150 153 NUM  1000 
AO Record Content Indicator 2 154 155 A/N  Values: 
• 01 = Original [[Asset]] record 
• 02 = Corrected [[Asset]] record 
• 03 = Firm reject record 
• 04 = Request record 
AO Transaction Type 2 156 157 A/N See the list in Cost Basis [[Asset]] Input (A) - 
DATATRAK SYSID: 36708 Production / 
46708 Test. 
AO Transfer Control Number  30 158 187 A/N  Format is as defined on the input layout. 
AO Alternate Control Number 30 188 217 A/N Format is as defined on the input layout. 
Filler  20 218 237 A/N  Reserved for future use. Spaces. 
AO Contra Firm Number 8 238 245 A/N   
Filler 2 246 247 A/N Reserved for future use. Spaces. 
AO Contra Firm Type 6 248 253 A/N Type of Receiving Firm 
Filler  10 254 263 A/N  Reserved for future use. Spaces. 
AO Submitting Firm Number  8 264 271 A/N   
Filler 2 272 273 A/N Reserved for future use.  
AO Submitting Firm Type 6 274 279 A/N Type of submitting firm. 
Filler 18 280 297 A/N Reserved for future use. Spaces. 

---

## Page 6

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 6 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
AO Receiver Customer Account 
Number  
20 298 317 A/N   
Filler  10 318 327 A/N  Reserved for future use. Spaces. 
AO Deliverer Customer Account 
Number  
20 328 347 A/N   
Filler  10 348 357 A/N  Reserved for future use. Spaces. 
AO ISIN Country Code  2 358 359 A/N   
AO ISIN Security Issue [[ID]]  9 360 368 A/N  [[CUSIP]] 
AO ISIN Security Check Digit  1 369 369 A/N   
Filler 10 370 379 A/N  Reserved for future use. Spaces. 
AO Put – Call Indicator  1 380 380 A/N  Values: 
• C = Call 
• P = Put 
AO [[Option]] Symbol 6 381 386 A/N   
AO [[Option]] Expiration Date  
–or– 
Last Factor Date (for MBS) 
8 387 394 A/N  Format: CCYYMMDD 
AO [[Option]] Strike Price Integer  5 395 399 A/N   
AO [[Option]] Strike Price Decimal  3 400 402 A/N  Valid values are 000 through 999, which 
represent only the decimal format. 
Filler 10 403 412 A/N Reserved for future use. Spaces. 
AO [[Asset]] Description  140 413 552 A/N   
AO [[Asset]] Category  4 553 556 A/N  Values: 
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
• MBS = Mortgage Backed [[securities]] 
(FNMA, GNMA, FHLMC) 
• MUNI = Municipal [[Bonds]] 

---

## Page 7

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 7 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
• MFNM = Mutual Fund Non –Money 
Market 
• OPT = Options 
• REIT = Real Estate Investment Trust 
• RGT = Right 
• UARP = [[UIT]] (Auction Rate Preferred) 
• UDSC = [[UIT]] (Deferred Sale Charge) 
• UNT = Units 
• [[UIT]] = Unit Investment Trust 
• WAR = Warrant 
• ZERO = Zero Coupon [[Bonds]]  
Filler  10 557 566 A/N  Reserved for future use. Spaces. 
AO Total Position Quantity  17 567 583 A/N  Decimal position denoted by a comma (,).  
Filler 20 584 603 A/N Reserved for future use. Spaces. 
AO Date Transfer Was Initiated 8 604 611 A/N Format: CCYYMMDD 
AO [[settlement]] Date of Transfer 8 612 619 A/N Format: CCYYMMDD 
AO Position Code  1 620 620 A/N  Values: 
• L = Long 
• S = Short    
• B = Borrowed 
Filler  131 621 751 A/N  Reserved for future use. Spaces. 
AO Disposition Method Used  2 752 753 A/N  Values: 
• 01 = FIFO (First In First Out) 
• 02 = LIFO (Last In First Out) 
• 03 = High Cost 
• 04 = Low Cost 
• 05 = Average Cost  
• 06 = Select Lot 
AO [[shares]] to Cover Short Indicator 1 754 754 A/N  
AO Firm Reject Reason Code 2 755 756 A/N Values: 
• 01 = Receiver cannot apply received cost 
basis record 
• 02 = CBRS quantity is greater than 
delivered quantity 
• 03 = [[CUSIP]] does not belong to 
[[issuer]]/[[transfer agent]] or spaces 
AO ACATS [[Asset]] Sequence 
Number  
6 757 762 A/N  

---

## Page 8

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 8 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
Filler  738 763 1500 A/N  Reserved for future use. Spaces. 
Data area for Tax Lot Input Status 
and Tax Lot Input (T)  
     Used when Tax Lot Input (T) record exists  
TO Record Type Status  1 90 90 A/N  Values for Status Code: 
• 0 = Valid 
• 1 = System Changed 
• 2 = Error 
• Space = No Change  
TO Record Length Status  1 91 91 A/N  See status code values. 
TO Record Content Indicator Status 1 92 92 A/N  See status code values. 
TO Transaction Type Status 1 93 93 A/N  See status code values. 
TO Transfer Control Number Status  1 94 94 A/N  See status code values. 
To Alternate Control Number Status 1 95 95 A/N  See status code values. 
TO Contra Firm Number Status  1 96 96 A/N  See status code values. 
TO Contra Firm Type Status 1 97 97 A/N  See status code values. 
TO Submitting Firm Number Status  1 98 98 A/N  See status code values. 
TO Submitting Firm Type Status 1 99 99 A/N  See status code values. 
TO Receiver Customer Account 
Number Status  
1 100 100 A/N  See status code values. 
TO Deliverer Customer Account 
Number Status  
1 101 101 A/N  See status code values. 
TO ISIN Country Code Status  1 102 102 A/N  See status code values. 
TO ISIN Security Issue [[ID]] Status  1 103 103 A/N  See status code values. 
TO ISIN Security Check Digit 
Status  
1 104 104 A/N  See status code values. 
TO Put Call Indicator Status 1 105 105 A/N See status code values. 
TO [[Option]] Symbol Status  1 106 106 A/N  See status code values. 
TO [[Option]] Expiration Date Status  
–or– 
Last Factor Date (for MBS) Status 
1 107 107 A/N  See status code values. 
TO [[Option]] Strike Price Integer 
Status  
1 108 108 A/N  See status code values. 

---

## Page 9

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 9 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
TO [[Option]] Strike Price Decimal 
Status  
1 109 109 A/N  See status code values. 
TO [[Asset]] Description Status  1 110 110 A/N  See status code values. 
TO Certificate Number Prefix 
Status 
1 111 111 A/N  See status code values. 
TO Certificate Number Status 1 112 112 A/N  See status code values. 
Filler 1 113 113 A/N  Reserved for future use. Spaces. 
TO Noncovered /Pending Indicator 
Status 
1 114 114 A/N  See status code values. 
TO Taxes Reported by 
[[issuer]]/[[transfer agent]] Status 
1 115 115 A/N See status code values. 
TO Gifted or Inherited Indicator 
Status 
1 116 116 A/N  See status code values. 
TO Date of Gift Status 1 117 117 A/N  See status code values. 
TO Fair Market Value as of Date of 
Gift status 
1 118 118 A/N  See status code values. 
TO Tax Lot Quantity Status  1 119 119 A/N  See status code values. 
TO Position Code Status  1 120 120 A/N  See status code values. 
TO Acquisition Date of Tax Lot 
Status 
1 121 121 A/N  See status code values. 
TO Original Acquisition Date for 
Wash Sale Status 
1 122 122 A/N  See status code values. 
TO ISO Currency Code Status  1 123 123 A/N  See status code values. 
TO Exchange Rate Status 
–or– 
Last Factor (for MBS) Status 
1 124 124 A/N  See status code values. 
TO Tax Lot Original Cost Status  1 125 125 A/N  See status code values. 
TO Tax Lot Current Cost Status  1 126 126 A/N  See status code values. 
TO Zero Basis Indicator Status 1 127 127 A/N  See status code values. 
TO Tax Lot Original Unit Price 
Status  
1 128 128 A/N  See status code values. 
TO Employee Plan [[shares]] 
Indicator Status 
1 129 129 A/N See status code values. 

---

## Page 10

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 10 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
TO Exchange Rate for FMV as of 
Date of Gift Status 
1 130 130 A/N  See status code values. 
TO Purchase / [[Dividend]] 
Reinvestment Indicator Status  
1 131 131 A/N  See status code values. 
TO Wash Sale Adjustment Amount 
Status 
1 132 132 A/N  See status code values. 
TO Accrue Market Discount 
Election Status 
1 133 133 A/N  See status code values. 
TO Include Market Discount in 
Income Election Status 
1 134 134 A/N  See status code values. 
Filler 1 135 135 A/N Reserved for future use. Spaces. 
TO Amortize [[Premium]] Election 
Status 
1 136 136 A/N  See status code values. 
TO Spot Rate Election Status 1 137 137 A/N  See status code values. 
TO Market Discount Status 1 138 138 A/N  See status code values. 
TO Bond [[Premium]] Status 1 139 139 A/N  See status code values. 
TO Acquisition [[Premium]] Status 1 140 140 A/N  See status code values. 
TO Accrued OID Status 1 141 141 A/N  See status code values. 
TO Last Adjustment Date Status 1  142 142 A/N  See status code values. 
Filler 1 143 143 A/N  See status code values. 
TO Carryover Offset Status 1 144 144 A/N  See status code values. 
TO Prior Year Mark to Market 
Status 
1 145 145 A/N See status code values. 
TO [[settlement]] Date Status 1 146 146 A/N See status code values. 
TO Accrued Unrealized Market 
Discount Status 
1 147 147 A/N See status code values. 
Filler  5 148 152 A/N  Reserved for future use. Spaces. 
TO Record Type  1 153 153 A/N  Always T  
TO Record Length  4 154 157 NUM  Always 1000 
TO Record Content Indicator 2 158 159 A/N Values: 
• 01 = Original tax lot record 
• 02 = Corrected tax lot record 

---

## Page 11

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 11 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
TO Transaction Type 2 160 161 A/N  
TO Transfer Control Number  30 162 191 A/N   
TO Alternate Control Number 30 192 221 A/N  
Filler  20 222 241 A/N  Reserved for future use. Spaces. 
TO Contra Firm Number  8 242 249 A/N   
 Filler 2 250 251 A/N Reserved for future use. Spaces. 
TO Contra Firm Type 6 252 257 A/N  
Filler  10 258 267 A/N  Reserved for future use. Spaces. 
TO Submitting Firm Number  8 268 275 A/N   
 Filler 2 276 277 A/N Reserved for future use. Spaces. 
TO Submitting Firm Type 6 278 283 A/N  
Filler 18 284 301 A/N Reserved for future use. Spaces. 
TO Receiver Customer Account 
Number  
20 302 321 A/N   
Filler  10 322 331 A/N  Reserved for future use. Spaces. 
TO Deliverer Customer Account 
Number 
20 332 351 A/N  
Filler 10 352 361 A/N Reserved for future use. Spaces. 
TO ISIN Country Code  2 362 363 A/N   
TO ISIN Security Issue [[ID]]  9 364 372 A/N   
TO ISIN Security Check Digit  1 373 373 A/N   
Filler 10 374 383 A/N Reserved for future use. Spaces. 
TO Put/Call Indicator 1 384 384 A/N Values: 
• C = Call 
• P = Put 
TO [[Option]] Symbol  6 385 390 A/N   
TO [[Option]] Expiration Date 
–or– 
Last Factor Date (for MBS) 
8 391 398 A/N  Format: CCYYMMDD 
TO [[Option]] Strike Price Integer  5 399 403 A/N   

---

## Page 12

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 12 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
TO [[Option]] Strike Price Decimal  3 404 406 A/N  Only valid values are 000 through 999, which 
represent decimal format only. 
TO [[Asset]] Description  140 407 546 A/N   
TO Certificate Number Prefix 8 547 554 A/N  
TO Certificate Number 12 555 566 A/N  
Filler  12 567 578 A/N  Reserved for future use. Spaces. 
TO Noncovered /Pending Indicator  2 579 580 A/N Values: 
• 01 = Noncovered lot 
• 02 = Noncovered account 
• 03 = Pending 
• 04 = Certificate in Customer Name 
TO Taxes Reported by 
[[issuer]]/[[transfer agent]] 
1 581 581 A/N Values: 
• Y = Yes 
• N = No 
Filler  9 582 590 A/N Reserved for future use – spaces 
TO Gifted or Inherited Indicator 2 591 592 A/N Values: 
• 01 = Gifted 
• 02 = Inherited 
• 03 = Inherited then Gifted 
TO Date of Gift 8 593 600 A/N Format: CCYYMMDD 
Filler 10 601 610 A/N Reserved for future use. Spaces. 
TO Fair Market Value as of Date of 
Gift 
17 611 627 A/N Decimal position denoted by a comma (,). 
TO Exchange Rate for FMV as of 
Date of Gift 
19 628 646 A/N Decimal position denoted by a comma (,). 
Filler 1 647 647 A/N Reserved for future use. Spaces. 
TO Tax Lot Quantity  17 648 664 A/N  Decimal position denoted by a comma (,).  
Filler  10 665 674  Reserved for future use. Spaces. 
TO Position Code  1 675 675 A/N  Values: 
• L = Long 
• S = Short 
Filler 10 676 685  Reserved for future use. Spaces. 
TO Acquisition Date of Tax Lot 8 686 693 A/N  Format: CCYYMMDD  

---

## Page 13

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 13 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
TO Original Acquisition Date for 
Wash Sale Adjustment 
8 694 701 A/N Format: CCYYMMDD  
TO Wash Sale Adjustment Amount 17 702 718 A/N Decimal position denoted by a comma (,). 
Filler  3 719 721 A/N  Reserved for future use. Spaces. 
TO ISO Currency Code  3 722 724 A/N   
TO Exchange Rate 
–or– 
Last Factor (for MBS) 
19 725 743 A/N Format: nine digits, comma, nine digits 
Filler 20 744 763 A/N Reserved for future use. Spaces. 
TO Tax Lot Original Cost  17 764 780 A/N  Decimal position denoted by a comma (,).  
Filler 20 781 800 A/N Reserved for future use. Spaces. 
TO Tax Lot Current Cost  17 801 817 A/N  Decimal position denoted by a comma (,).  
Filler 20 818 837 A/N Reserved for future use. Spaces. 
TO Zero Basis Indicator 2 838 839 A/N  
TO Tax Lot Original Unit Price  17 840 856 A/N  Decimal position denoted by a comma (,).  
Filler  20 857 876 A/N  Reserved for future use. Spaces. 
TO Employee Plan [[shares]] 
Indicator 
2 877 878 A/N Values: 
• 01 = Qualified Employee [[Stock]] Purchase 
Plan  
• 02 = Incentive [[Stock]] [[Option]] Plan  
TO Accrue Market Discount 
Election 
1 879 879 A/N Values: 
• Y = Yes 
• N = No 
TO Include Market Discount in 
Income Election 
1 880 880 A/N Values: 
• Y = Yes 
• N = No 
Filler 1 881 881 A/N Reserved for future use. Spaces. 
TO Amortize [[Premium]] Election 1 882 882 A/N Values: 
• Y = Yes 
• N = No 
 
 

---

## Page 14

Cost Basis Transaction MRO 
AutoRoute Production 02400264 / PSE 02980264 14 
COST BASIS TRANSACTION MRO 
AUTOROUTE PRODUCT [[ID]]: 02400264 / PSE 02980264 
RECORD LENGTH: 1500 
RECORD TYPE: VARIABLE 
REVISION DATE: April 27, 2023 
FIELD NAME  LENGTH START END TYPE  COMMENTS  
TO Spot Rate Election 1 883 883 A/N Values: 
• Y = Yes 
• N = No 
Filler 2 884 885 A/N Reserved for future use. Spaces. 
TO Purchase / Reinvestment 
Indicator  
1 886 886 A/N  Values: 
• P = Purchase 
• R = Reinvestment  
TO Market Discount 17 887 903 A/N Decimal position denoted by a comma (,). 
TO Bond [[Premium]] 17 904 920 A/N Decimal position denoted by a comma (,). 
TO Acquisition [[Premium]] 17 921 937 A/N Decimal position denoted by a comma (,). 
TO Accrued OID 17 938 954 A/N Decimal position denoted by a comma (,). 
TO Last Adjustment Date   8 955 962 A/N Format: CCYYMMDD 
Filler  17 963   979 A/N Reserved for future use. Spaces. 
TO Carryover Offset  17 980 996 A/N Decimal position denoted by a comma (,). 
TO Prior Year Mark to Market 17 997 1013 A/N Decimal position denoted by a comma (,). 
TO [[settlement]] Date 8 1014 1021 A/N Format: CCYYMMDD 
TO Accrued Unrealized Market 
Discount 
17 1022 
1038 A/N Decimal position denoted by a comma (,). 
Filler  462 1039 1500 A/N  Reserved for future use. Spaces. 
END OF RECORD 
 

---

## Page 15

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: April 27, 2023  
Publication Code: CBRS141 
Service: Cost Basis Reporting Service (CBRS) 
Title: Cost Basis Transaction MRO: AutoRoute Production 02400264/Test 02980264 Record Layout 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 