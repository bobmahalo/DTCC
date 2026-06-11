---
title: "MFPS I & II Reject Codes"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps_rejectcodes_mfs195_20201123.pdf"
pages: 36
size: "393.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS I & II Reject Codes

**Original File:** [mfps_rejectcodes_mfs195_20201123.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps_rejectcodes_mfs195_20201123.pdf)  
**Category:** Other  
**Total Pages:** 36  
**File Size:** 393.8 KB  

---

## Page 1

  
 
 
 
MUTUAL FUND PROFILE SERVICE I & 
II 
MFPS I & II REJECT CODES 
OCTOBER 30, 2020 
 


---

## Page 2

 
  
© 2020 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 30, 2020 
Publication Code: MFS195 
Service: Mutual Fund Profile Service I & II 
Title: MFPS I & II Reject Codes 
 
 

---

## Page 3

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 3  
MFPS I & II REJECT CODES 
For transactions that [[DO]] not meet the required editing criteria, the following MFPS reject codes are used by 
[[NSCC]]. 
Reject Code 
(MFPS, Phase I & II) 
Description 
LIMT Output message reached length limit; rest of input message not processed 
PRTL Message rejected partially forward 
Rnnn Following reject code applies to input Price/Rate section nnn (within Security Issue section) 
Snnn Following reject code applies to input Security Issue section nnn 
SECI Whole Security Issue section rejected 
WHLE Whole message rejected 
0001 [[BASIC]] Header missing or invalid initiation identifier 
0002 [[BASIC]] Header, invalid length 
0003 [[BASIC]] Header, invalid Application [[ID]] 
0004 [[BASIC]] Header, invalid APDU 
0005 [[BASIC]] Header, Swift Address, invalid Sender Number 
0006 [[BASIC]] Header, Swift Address, invalid bytes 5-7 
0007 [[BASIC]] Header, Swift Address, invalid bytes 8-12 
0008 [[BASIC]] Header, invalid Session Number 
0009 [[BASIC]] Header, invalid Sequence Number 
0010 Invalid Systems Testing indicator 
0011 Application Header missing or invalid initiation identifier 
0012 Application Header, invalid length 
0013 Application Header, invalid Input/Output Indicator 

---

## Page 4

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 4  
Reject Code 
(MFPS, Phase I & II) 
Description 
0014 Application Header, invalid Message Type 
0015 Application Header, Swift Address, invalid Recipient 
0016 Application Header, Swift Address, invalid bytes 5-7 
0017 Application Header, Swift Address, invalid bytes 8-12 
0018 Application Header, invalid Message Priority 
0019 Application Header, invalid Delivery Monitoring Indicator 
0020 Application Header, invalid Obsolescence Period 
0021 Application Header, invalid Input Time 
0022 Application Header, invalid Original Input Date 
0023 Application Header, Message Input Reference, invalid Input Date 
0024 Application Header, Message Input Reference, invalid bytes 11-14 
0025 Application Header, Message Input Reference, invalid bytes 15-17 
0026 Application Header, Message Input Reference, invalid bytes 18-22 
0027 Application Header, Message Input Reference, invalid bytes 23-30 
0028 Application Header, invalid Output Date 
0029 As of exchanges is invalid 
0030 Firm exit on exchanges is invalid 
0031 Text Block missing or invalid initiation identifier 
0032 Reference Number missing/invalid 
0033 Related Reference Number invalid 
0034 Transaction Type missing/invalid 
0035 Submission Date literal missing/invalid 

---

## Page 5

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 5  
Reject Code 
(MFPS, Phase I & II) 
Description 
0036 Submission Date missing/invalid 
0037 Submission Time missing/invalid 
0038 Submission Time country code invalid 
0039 Submission Time description invalid 
0040 Security Issue missing/invalid 
0041 Security Issue check digit invalid 
0042 Security Issue description invalid 
0043 Effective Date literal missing/invalid 
0044 Effective Date missing/invalid 
0045 Information Type missing/invalid 
0046 Information Type does not correspond Effective Date literal 
0047 Information Type description invalid 
0048 Amount sign indicator invalid 
0049 Amount currency code missing/invalid 
0050 Amount currency code does not correspond Information Type 
0051 Amount missing/invalid 
0052 Amount decimal comma missing 
0053 Amount integer/fraction length invalid, or integer missing 
0054 Amount integer/fraction length does not correspond Information Type 
0055 [[Dividend]] Day Count missing/invalid 
0056 [[Dividend]] Day Count not allowed for this Information Type 
0057 CDSC advance fee in error 

---

## Page 6

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 6  
Reject Code 
(MFPS, Phase I & II) 
Description 
0058 Security Issue invalid for submitting fund 
0059 Submitting [[participant]] not eligible for this service 
0060 No Security Issue section found 
0061 No Price/Rate section found in Security Issue section 
0062 Too many Price/Rate sections in Security Issue section 
0063 End of Text Block missing/invalid 
0064 Character does not belong to the S.W.I.F.T. character set 
0065 Field or sub-field starts or ends with character(s) not allowed by S.W.I.F.T. 
0066 Field or sub-field contains characters not allowed by S.W.I.F.T. 
0067 Field or sub-field is too long or not followed by CrLf or end of line 
0068 Duplicate Reference Number 
0069 Duplicate Price/Rate 
0070 Price/Rate not found 
0071 Trailer block missing or invalid initiation identifier 
0072 Trailer block, invalid length 
0073 Trailer block, invalid Sub-block Identifier 
0074 Trailer block, Training Indicator missing/invalid 
0075 Input message is too long 
0076 Fund maximum commission in error 
0077 Share class exchange invalid 
0078 Cutoff time invalid 
0079 All Share Classes Exchange Indicator invalid 

---

## Page 7

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 7  
Reject Code 
(MFPS, Phase I & II) 
Description 
0080 Sequence Number missing/invalid 
0081 Originator Type missing/invalid 
0082 Profile Type missing/invalid 
0083 Record Type missing/invalid 
0084 Correction Indicator missing/invalid 
0085 Price missing/invalid 
0086 Rate missing/invalid 
0087 Currency Indicator missing/invalid 
0088 Record Length missing/invalid 
0089 Test Indicator invalid 
0090 Duplicate Price 
0091 Duplicate Rate 
0092 Price not found 
0093 Rate not found 
0094 12b-1 Single Rate missing/invalid 
0095 Excessive information for action type `D' 
0096 Recipient is the Submitting [[participant]] 
0097 "From Date" versus "To Date" 
0098 Inconsistent extract parameters 
0099 Duplicate State Code 
0100 Submitting [[participant]] Number missing/invalid 
0101 Recipient Number missing/invalid 

---

## Page 8

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 8  
Reject Code 
(MFPS, Phase I & II) 
Description 
0102 Contact Type missing/invalid 
0103 Contact Name invalid 
0104 Contact Address 1 invalid 
0105 Contact Address 2 invalid 
0106 Contact Address 3 invalid 
0107 Contact Address 4 invalid 
0108 Contact Address 5 invalid 
0109 Contact Address 6 invalid 
0110 Contact Telephone Number invalid 
0111 Contact Fax Number invalid 
0112 [[participant]] e-mail address invalid 
0113 Clearing/Settling [[Broker]] invalid 
0114 ACAT-Fund/SERV Indicator invalid 
0115 Networking Level 1 Indicator invalid 
0116 Networking Level 2 Indicator invalid 
0117 Networking Level 3 Indicator invalid 
0118 Networking Level 4 Indicator invalid 
0119 Trust Level Processing Indicator invalid 
0120 Retirement [[Asset]] Transfer Processing Indicator invalid 
0121 Commission [[settlement]] for Front End Indicator invalid 
0122 Commission [[settlement]] for Basis Point Indicator invalid 
0123 Commission [[settlement]] for Re-invested [[Dividend]] Indicator invalid 

---

## Page 9

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 9  
Reject Code 
(MFPS, Phase I & II) 
Description 
0124 Commission [[settlement]] for CDSC Advance Indicator invalid 
0125 Commission [[settlement]] for Promotions Indicator invalid 
0126 Commission [[settlement]] for Finders Fee Indicator invalid 
0127 Commission [[settlement]] for 12B-1 Fee Indicator invalid 
0128 Commission [[settlement]] for Supplemental Commission Indicator invalid 
0129 Commission [[settlement]] for Negotiated Commission Indicator invalid 
0130 Commission [[settlement]] for Pre-paid Commission Indicator invalid 
0131 Global Update Indicator invalid 
0132 Global Update Account Level Indicator invalid 
0133 Extended Corrections Indicator invalid 
0134 Same Day Confirmations Indicator invalid 
0135 Reconfirmation Indicator invalid 
0136 Mass [[Broker]] to [[Broker]] Transfers Indicator invalid 
0137 [[settlement]] Override Indicator invalid 
0138 BIN on Level 0 Indicator invalid 
0139 SWP [[settlement]] thru Networking Indicator invalid 
0140 Direct Redemption [[settlement]] thru Networking Indicator invalid 
0141 [[Dividend]] Type invalid 
0142 Invalid ToRA eligibility indicator - security 
0143 Maximum Trade Size Indicator invalid 
0144 Share Class Identifier invalid 
0145 Share Class Definition invalid 

---

## Page 10

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 10  
Reject Code 
(MFPS, Phase I & II) 
Description 
0146 Number of Occurrences of Share Class Exchange Data invalid 
0147 Share Class Exchange From Class invalid 
0148 Share Class Exchange To Class invalid 
0149 Exchange Fee Indicator invalid 
0150 Exchange Fee Amount/Percent invalid 
0151 Actual Days in Pay Period is invalid 
0152 12b-1 Pre Rate invalid 
0153 Security Issue Country Code missing/invalid 
0154 Load Type invalid 
0155 LOI Eligible invalid 
0156 ROA Eligible invalid 
0157 Investment Mode invalid 
0158 Objective Goal Type invalid 
0159 Objective Sub Goal Type 1 invalid 
0160 Objective Sub Goal Type 2 invalid 
0161 Fund Name invalid 
0162 CDSC Minimum Identifier invalid 
0163 Quotron Symbol invalid 
0164 Currency Indicator Identifier invalid 
0165 Educational IRA Purchase Subsequent Minimum invalid 
0166 Purchase Initial Minimum invalid 
0167 Security Share Class Identifier invalid 

---

## Page 11

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 11  
Reject Code 
(MFPS, Phase I & II) 
Description 
0168 12b-1 Post Rate 
0169 Purchase Subsequent Minimum invalid 
0170 IRA Purchase Initial Minimum invalid 
0171 IRA Purchase Subsequent Minimum invalid 
0172 Minimum Redemption Amount invalid 
0173 Offering Type invalid 
0174 Offering First Trade Date invalid 
0175 Offering Last Trade Date invalid 
0176 Offering [[settlement]] Date invalid 
0177 Employee NAV Purchase Allowed invalid 
0178 Wrap Fee NAV Purchase Allowed invalid 
0179 CDSC Waiver Due to Correction Indicator invalid 
0180 Reinvest Eligible Indicator invalid 
0181 Account Cap invalid 
0182 Short [[settlement]] Minimum invalid 
0183 Short [[settlement]] Maximum invalid 
0184 Redemption Fee Indicator invalid 
0185 Redemption Fee invalid 
0186 IRA Maintenance Fee invalid 
0187 Wire Transfer Fee invalid 
0188 Cross Fund Reinvest Indicator invalid 
0189 Cross Fund Reinvest Load invalid 

---

## Page 12

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 12  
Reject Code 
(MFPS, Phase I & II) 
Description 
0190 Redemption Closeout Indicator invalid 
0191 Exchange Closeout Indicator invalid 
0192 Transfer Closeout Indicator invalid 
0193 PAC Cycle Indicator invalid 
0194 PAC Cycle Include/Exclude Indicator invalid 
0195 SWP Cycle Indicator invalid 
0196 SWP Cycle Include/Exclude Indicator invalid 
0197 Purchase Closed Indicator invalid 
0198 Redemption Closed Indicator invalid 
0199 Check Writing [[Option]] Indicator invalid 
0200 Internal Fund Number invalid 
0201 Certificates Available invalid 
0202 Min Acct Balance for IRA SWP Monthly invalid 
0203 Min Acct Balance for IRA SWP Quarterly invalid 
0204 Min Acct Balance for IRA SWP Semi-Annually invalid 
0205 Min Acct Balance for IRA SWP Annual invalid 
0206 Min Acct Balance for Non IRA SWP Monthly invalid 
0207 Min Acct Balance for Non IRA SWP Quarterly invalid 
0208 Min Acct Balance for Non IRA SWP Semi-Annually invalid 
0209 Min Acct Balance for Non IRA SWP Annual invalid 
0210 Re-Offering Date - Open invalid 
0211 Re-Offering Date - Close invalid 

---

## Page 13

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 13  
Reject Code 
(MFPS, Phase I & II) 
Description 
0212 [[Dividend]] Calculation Type invalid 
0213 [[Dividend]] Payable Type invalid 
0214 Exchange Fee invalid 
0215 Automatic Investment Eligible invalid 
0216 Systematic Withdrawal Eligible invalid 
0217 [[liquidation]] Repurchase at NAV Days invalid 
0218 Share Class Conversion Cycle Indicator invalid 
0219 Share Class Conversion To Security invalid 
0220 Share Class Conversion Recurring Date invalid 
0221 Share Class Conversion Date Last invalid 
0222 Share Class Conversion Rate Last invalid 
0223 Share Class Conversion Date Last invalid 
0224 Foreign Tax Credit Rate invalid 
0225 Additional Contact Indicator invalid 
0226 Contact Title invalid 
0227 Non Fund/Serv Security Type invalid 
0228 Educational IRA Purchase Initial Minimum invalid 
0229 Allowable Exchange 2 Delete Code invalid 
0230 Restrict/Allow Code invalid 
0231 Requested [[participant]] Type invalid 
0232 Requested Security Type invalid 
0233 Money Market Purchase Cutoff Time invalid 

---

## Page 14

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 14  
Reject Code 
(MFPS, Phase I & II) 
Description 
0234 Money Market [[liquidation]] Cutoff Time invalid 
0235 As Of Process Range Days invalid 
0236 Date of Last Prospectus invalid 
0237 Date of Last Annual Report invalid 
0238 Date of Last Semi-Annual Report invalid 
0239 Fund Status Indicator invalid 
0240 Closed Fund Disposition Indicator invalid 
0241 Merged Fund Security [[ID]] invalid 
0242 Blue Sky State invalid 
0243 Occurrences of Blue Sky States invalid 
0244 Occurrences of CDSC Schedule invalid 
0245 Age of [[shares]] invalid 
0246 CDSC Rate invalid 
0247 Occurrences of Breakpoint Schedules invalid 
0248 Breakpoint Lower Limit invalid 
0249 Breakpoint Upper Limit invalid 
0250 Percent of POP invalid 
0251 Dealer Concession invalid 
0252 12B-1 Calc Type invalid 
0253 12B-1 Payable Type Frequency invalid 
0254 12B-1 Agreement Date invalid 
0255 12B-1 Pre-Agreement Rate invalid 

---

## Page 15

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 15  
Reject Code 
(MFPS, Phase I & II) 
Description 
0256 Insufficient information for action types "A" or "C" 
0257 Invalid record length (not equal the actual record length) 
0258 Excessive information, Requested [[participant]] Type and Requested [[participant]] (*) 
0259 Requested [[participant]] Type disallowed with the Requested Profile Type (*) 
0266 12B-1 Post -Agreement Rate invalid 
0267 12B-1 Holding Period invalid 
0268 12B-1 Processing Hierarchy invalid 
0269 12B-1 Frequency invalid 
0270 Front End Commission Frequency invalid 
0271 Basis Point Commission Frequency invalid 
0272 CDSC Advance Frequency invalid 
0273 Finders Fee Frequency invalid 
0274 Number of Announcement Data Records to Follow invalid 
0275 Announcement Type invalid 
0276 Announcement Start Date invalid 
0277 Announcement End Date invalid 
0278 Announcement Free Form Data invalid 
0279 Occurrences of Portfolio Manager Data invalid 
0280 Portfolio Manager Name invalid 
0281 Manager Since Date invalid 
0282 Occurrences of State Earnings invalid 
0283 Projected/Actual Indicator invalid 

---

## Page 16

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 16  
Reject Code 
(MFPS, Phase I & II) 
Description 
0284 [[Dividend]] Record Date invalid 
0285 [[Dividend]] Ex Date invalid or missing 
0286 [[Dividend]] Reinvest Date invalid 
0287 [[Dividend]] Payable Date invalid 
0288 [[Dividend]] Payable Amount invalid 
0289 Capital Gain Record Date invalid 
0290 Capital Gain Ex Date invalid or missing 
0291 Capital Gain Reinvest Date invalid 
0292 Capital Gain Payable Date invalid 
0293 Capital Gain Amount invalid 
0294 Capital Gain Indicator invalid 
0295 Payout Rate Period Start Date invalid 
0296 Payout Rate Period End Date invalid 
0297 Reinvest Price invalid 
0298 12B-1 Pre Agreement Record Date Next invalid 
0299 12B-1 Pre Agreement Avg [[Asset]] Start Date invalid 
0300 12B-1 Pre Agreement Avg [[Asset]] End Date invalid 
0301 12B-1 Pre Agreement Payable Date invalid 
0302 12B-1 Post Agreement Record Date invalid 
0303 12B-1 Post Agreement Avg [[Asset]] Start Date invalid 
0304 12B-1 Post Agreement Avg [[Asset]] End Date invalid 
0305 12B-1 Post Agreement Payable Date invalid 

---

## Page 17

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 17  
Reject Code 
(MFPS, Phase I & II) 
Description 
0306 Earnings Subject to AMT invalid 
0307 Change or Delete - non existing row 
0308 Earnings From US Govt [[obligations]] invalid 
0309 Foreign Tax Credits invalid 
0310 Return of Capital invalid 
0311 Number of States invalid 
0312 State of Municipal Earnings Amount invalid 
0313 SWP Setup thru Networking Indicator invalid 
0314 SWP [[settlement]] Method invalid 
0315 Date of Last [[Proxy]] invalid 
0316 Date of Next Board of Directors Meeting invalid 
0317 [[Reg T]] Requirements Met invalid 
0318 Minimum Trade Size invalid 
0319 Minimum Check Writing Amount invalid 
0320 Wrap FEE Purchase Minimum Amount 
0321 Telephone Redemption Eligible invalid 
0322 Minimum Telephone Redemption Amount invalid 
0323 Maximum Telephone Redemption Amount invalid 
0324 NAV Repurchase invalid 
0325 NAV Employee invalid 
0326 NAV Error Correction invalid 
0327 Wrap Fee NAV Purchase Allowed invalid 

---

## Page 18

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 18  
Reject Code 
(MFPS, Phase I & II) 
Description 
0328 NAV Commissionable Defined Contribution Plan invalid 
0329 NAV Noncommissioned Defined Contribution Plan invalid 
0330 NAV Other invalid 
0331 Other Contact Type Description invalid 
0332 Contact Email Address invalid 
0333 Defined Contribution Processing Indicator invalid 
0334 Defined Contribution Processing Cutoff invalid 
0335 Maximum Defined Contribution Amount for Next Day [[settlement]] invalid 
0336 12B-1 Minimum Commission Payment invalid 
0337 Distribution Indicator invalid 
0338 Offshore Fund Indicator invalid 
0339 File Request Type Indicator invalid 
0340 Requested [[participant]] Number invalid 
0341 CDSC Waiver Due to Death Indicator invalid 
0342 CDSC Waiver Due to Disability Indicator invalid 
0343 CDSC Waiver Due to Mandatory Distrib Indicator invalid 
0344 12b-1 Tiered Age invalid 
0345 12b-1 Tiered Rate invalid 
0346 Occurrences of 12b-1 Tiered Data invalid 
0347 Duplicate information in database 
0348 Earnings Indicator value (State Earnings segment) invalid 
0349 Activity Type value invalid 

---

## Page 19

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 19  
Reject Code 
(MFPS, Phase I & II) 
Description 
0350 Number of occurrences of Share Class definitions in record type 011 invalid 
0351 Clearing/Settling [[Broker]] number, record type 011 invalid 
0352 Requested "From" Date invalid 
0353 Requested "To" Date invalid 
0354 Roth IRA Purchase Subsequent Minimum invalid 
0355 Roth IRA Purchase Initial Minimum invalid 
0356 Redemption Indicator invalid 
0357 Redemption Fee Type invalid 
0358 SWP for Networking Cycle Indicator invalid 
0359 SWP for Networking Cycle Include/Exclude Indicator invalid 
0360 SWP for Checking Cycle Indicator invalid 
0361 SWP for Checking Cycle Indicator Include/Exclude invalid 
0362 Exchange Closed Indicator invalid 
0363 Exchange Fee Type invalid 
0364 Age of [[shares]] for Conversion invalid 
0365 NAV Other Description invalid 
0366 Funds Age for Distribution Waiver invalid 
0367 CDSC Waiver Due to Divorce invalid 
0368 CDSV Waiver Due to Pre-purchased [[shares]] invalid 
0369 Year of Filing invalid 
0370 State Code invalid 
0371 Rate of Earnings invalid 

---

## Page 20

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 20  
Reject Code 
(MFPS, Phase I & II) 
Description 
0372 Year of Earnings invalid 
0373 Special Commission Advance invalid 
0374 Special Commission Rate invalid 
0375 Special Commission Starting Dollar Amount invalid 
0376 Payable Date invalid 
0377 Distribution Type invalid 
0378 403(B) ToRA Processing Indicator invalid 
0379 403(B) ToRA Eligibility Indicator invalid 
0380 Record type vis-N-vis Fund/Dealer indicator invalid 
0381 Transaction Record type & Action type vis-N-vis record length invalid 
0382 Security Issue [[ID]] belongs to another fund number 
0383 Record Type doesn't allow Recipient number 
0384 Redundant data for Action Type "Delete" 
0385 No data for this request 
0386 Originator Type not = Type in [[participant]] Master 
0387 # Occurrences contradicts the actual # of occurrences 
0388 [[participant]] is not valid for the Submitter and/or Product  
0389-0399 ** Unused 
0400 Security Issue Symbol Indicator missing/invalid 
0401 Security Issue Symbol missing/invalid 
0402 Cumulative Rate Correction Indictor missing/invalid 
0403 Cumulative Rate missing/invalid 

---

## Page 21

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 21  
Reject Code 
(MFPS, Phase I & II) 
Description 
0404 Cumulative Rate Day Count missing/invalid 
0405 Duplicate Cumulative Rate 
0406 Cumulative Rate not found 
0407 Negative Rate Correction Indicator is missing/invalid (effective 11/23/20) 
0408 Negative Rate is missing/invalid (effective 11/23/20) 
0409 ** Unused 
0410 Invalid Branch [[ID]] 
0411 Missing Representative Name 
0412 Invalid Update Indicator 
0415 Invalid Number Of Recipients 
0416-0418 ** Unused 
0419 Invalid Recipient Fund Number 
0420 Invalid Re-class 
0421 Estimated/Corrected Indicator Invalid 
0422 Invalid Record Date 
0423 Payable Date Invalid 
0424 Invalid Total Distributions Per Share 
0425 Invalid Prior Taxable Year Amount Per Share 
0426 Invalid Next Taxable Year Amount Per Share 
0427 Invalid Current Taxable Year Amount Per Share 
0428 Invalid Income Dividends 
0429 Invalid Short Term Capital Gains 

---

## Page 22

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 22  
Reject Code 
(MFPS, Phase I & II) 
Description 
0430 Invalid Foreign Tax Paid 
0431 Invalid Ordinary Dividends 
0432 Invalid 28% Rate Gain Amount 
0433 ** Unused 
0434 Invalid Section 1250 Gain Amount 
0435 Invalid Section 1202 Gain Amount 
0436 ** Unused 
0437 Invalid Non-Taxable Distributions 
0438 Invalid Cash [[liquidation]] Distributions 
0439 Invalid Non-Cash [[liquidation]] Distributions 
0440 Invalid Exempt Interest Dividends 
0441 Invalid Total Capital Gain Distributions 
0442 Invalid Foreign Tax Paid (Box 6) 
0443 ** Unused 
0444 ** Unused 
0445 ** Unused 
0446 Invalid Correction Indicator 
0447 Invalid Qualified Dividends 
0448 ** Unused 
0449 ** Unused 
0450 Invalid ROA Allowed 
0451 Invalid Counted / Allowed Toward ROA 

---

## Page 23

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 23  
Reject Code 
(MFPS, Phase I & II) 
Description 
0452 Invalid ROA Allowed for Money Markets 
0453 Invalid Money Market Counted / Allowed Toward ROA 
0454 Invalid ROA Calculation Methodology 
0455 Invalid ROA / LOI Calculated Price Date 
0456 Invalid LOI Allowed 
0457 Invalid Counted / Allowed Toward LOI 
0458 Invalid Money Market Counted / Allowed Toward LOI 
0459 Invalid LOI Fulfillment Calculation Methodology 
0460 Invalid LOI Fulfillment Period 
0461 Invalid LOI Fulfillment Period for Million Dollar LOI 
0462 Invalid LOI Minimum Dollar Investment 
0463 Invalid LOI Minimum Percentage Investment 
0464 Invalid Retroactive LOIs 
0465 Invalid Retroactive LOI Period 
0466 Invalid Retroactive LOI Calculation Methodology 
0467 Invalid NAV Transfer Allowed 
0468 Invalid NAV Transfer Period 
0469 Invalid NAV Transfer – Source of Investment 
0470 Invalid NAV Transfer Account Rules 
0471 Invalid NAV Reinstatements Allowed 
0472 Invalid NAV Reinstatements Period 
0473 Invalid NAV Reinstatement Account Rules 

---

## Page 24

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 24  
Reject Code 
(MFPS, Phase I & II) 
Description 
0474 Invalid NAV Reinstatement Frequency 
0475 Invalid NAV Purchase of Front End Load Eligible for ROA 
0476 Invalid NAV Purchase of Front End Load Eligible for LOI 
0477 Invalid Link by Spouse 
0478 Invalid Link by Civil Union 
0479 Invalid Link by Domestic Partnership 
0480 Invalid Link by Common Law Marriage 
0481 Invalid Link by Parent 
0482 Invalid Link by Step Parent 
0483 Invalid Link by Legal Guardian 
0484 Invalid Link by Child 
0485 Invalid Child Maturation Age 
0486 Invalid Link by Stepchild 
0487 Invalid Link by Sibling 
0488 Invalid Link by Grandchildren 
0489 Invalid Link by Grandparents 
0490 Invalid Link by Father-in-Law 
0491 Invalid Link by Mother-in-Law 
0492 Invalid Link by Brother-in-Law 
0493 Invalid Link by Sister-in-Law 
0494 Invalid 529 Products – ROA Eligible 
0495 Invalid 529 Products – LOI Eligible 

---

## Page 25

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 25  
Reject Code 
(MFPS, Phase I & II) 
Description 
0496 Invalid Annuities – ROA Eligible 
0497 Invalid Annuities – LOI Eligible 
0498 Invalid UITs – ROA Eligible 
0499 Invalid UITs – LOI Eligible 
0500 Invalid IRA accounts – ROA Eligible 
0501 Invalid IRA accounts – LOI Eligible 
0502 Invalid Link Trust Accounts by Trustee if primary owner or family related 
0503 Invalid Link Trust by Beneficiary 
0504 Invalid Link Trust by Grantor 
0505 Invalid [[DO]] all the CUSIPS in this Class have the Same Linkage Rules? 
0506 Invalid Link Trust by Other Means 
0507 Invalid [[NASDAQ]] Symbol 
0508 Invalid Blue Sky Record Applies 
0509 Invalid CDSC Information Record Applies 
0510 Invalid Breakpoint Schedule Record Applies 
0511 Invalid Commission Data Record Applies 
0512 Invalid Breakpoint Linkage Rules Applies 
0521 Invalid Maximum purchase amount 
0522 Invalid Distribution Reinvestment Load Code 
0523 Invalid Automatic Investment Eligible Code 
0524 Invalid Automatic Withdrawal Eligible Code 
0525 Invalid Defined Contribution Clearance & [[settlement]] (“DCC&S”) Cut-Off Time 

---

## Page 26

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 26  
Reject Code 
(MFPS, Phase I & II) 
Description 
0526 Invalid Class Name 
0527 Invalid Portfolio Name 
0528 Invalid Fund Family Brand Name 
0530 Invalid Minimum Wrap Subsequent Purchase Amount 
0531 Invalid Minimum "Qualified Plans" Initial Purchase Amount 
0532 Invalid Minimum "Qualified Plans" Subsequent Purchase Amount 
0533 Invalid Share Conversion Cycle Eligibility Code 
0534 Invalid Share Conversion Cycle Date Code 
0535 Invalid Share Conversion Cycle Date 
0536 Invalid Share Conversion Cycle Date Day Code 
0537 Invalid Periodic/Systematic Investment Purchase Amount 
0538 Invalid Maximum Account Value 
0539 Invalid Maximum Account Value Code 
0540 Invalid Share Conversion Age 
0541 Invalid Share Conversion Cycle Starting Month 
0542 Invalid NAV Repurchase Share Class 
0543 Invalid NAV Repurchase Days 
0544 Invalid NAV Repurchase Account Eligibility Code 
0545 Invalid NAV Repurchase CDSC Reimbursement Code 
0546 Invalid NAV Repurchase Frequency Code 
0547 Invalid Advanced Commission Rate 
0549 Invalid CDSC Systematic Withdrawal Waiver Code 

---

## Page 27

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 27  
Reject Code 
(MFPS, Phase I & II) 
Description 
0550 Invalid CDSC Defined Contribution Waiver Code 
0551 Invalid CDSC Hardship Waiver Code 
0552 Invalid CDSC Termination Distribution Waiver Code 
0553 Invalid CDSC Involuntary Distribution Waiver Code 
0554 Invalid CDSC Forfeiture Distribution Waiver Code 
0555 Invalid CDSC Loan Distribution Waiver Code 
0556 Invalid CDSC Excess Contribution Distribution Waiver Code 
0557 Invalid CDSC Qualified Distribution Waiver Code 
0558 Invalid CDSC Qualified Distribution Waiver Age 
0559 Invalid CDSC Aging Method Code 
0560 Invalid CDSC Calculation Method Code 
0561 Invalid CDSC Redemption Hierarchy Method Code (assumption is free [[shares]] always first) 
0562 Invalid CDSC Exchange Hierarchy Method Code 
0563 Invalid CDSC Transfer Hierarchy Method Code 
0564 Invalid CDSC Exchange Buy Aging Schedule Code 
0565 Invalid CDSC Aging Start Date 
0566 Invalid CDSC Death Waiver Time Period 
0567 Invalid CDSC Required Minimum Distribution Amount Code 
0568 Invalid Number of CDSC Schedules 
0569 Invalid CDSC Schedule Lower Limit 
0570 Invalid CDSC Schedule Upper Limit 
0571 Invalid Number of rates in Schedule 

---

## Page 28

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 28  
Reject Code 
(MFPS, Phase I & II) 
Description 
0572 Invalid 12b-1 Average Daily [[Asset]] Calculation Start Day 
0573 Invalid 12b -1 Record Date 
0574 Invalid 12b-1 Record Date Day Code 
0575 Invalid 12b-1 Start Month 
0576 Invalid 12b-1 [[Dividend]] Share Aging Code 
0579 Invalid Number of 12b-1 Agreements 
0580 Invalid STR Minimum Amount 
0581 Invalid STR Share Aging Method Code 
0582 Invalid STR Redemption Methodology Code 
0584 Invalid STR Correction Waiver Code 
0585 Invalid STR Death Waiver Code 
0586 Invalid STR Disability Waiver Code 
0587 Invalid STR Qualified Distribution Waiver Code 
0588 Invalid STR Qualified Distribution Waiver Age 
0589 Invalid STR Divorce Waiver Code 
0590 Invalid STR Systematic Withdrawal Waiver Code 
0591 Invalid STR Defined Contribution Waiver Code 
0592 Invalid STR Hardship Distribution Waiver Code 
0593 Invalid STR Automatic Rebalance Waiver Code 
0594 Invalid STR Termination Distribution Waiver Code 
0595 Invalid STR Involuntary Distribution Waiver Code 
0596 Invalid STR Forfeitures Distribution Waiver Code 

---

## Page 29

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 29  
Reject Code 
(MFPS, Phase I & II) 
Description 
0597 Invalid STR Loan Distribution Waiver Code 
0598 Invalid STR Excess Contribution Distribution Waiver Code 
0599 Invalid STR Wrap Fee Waiver Code 
0600 Invalid STR Plan Fee Waiver Code 
0601 Invalid STR Reinvested [[shares]] Waiver Code 
0602 Invalid STR Exchange Buy Schedule Code 
0603 Invalid STR Exchange Buy Aging Date Code 
0604 Invalid STR Aging Start Date Code 
0605 Invalid STR Eligible Transaction Code 
0606 Invalid STR Payout Calculation Amount Code 
0607 Invalid Number of STR Rates 
0608 Invalid STR Share Age 
0609 Invalid STR Rate 
0610 Invalid Finder’s Fee/ Jumbo Brkpoint Blending Applies Code 
0611 Invalid Breakpoint Sales Charge Rate 
0612 Invalid Breakpoint [[underwriter]] Rate 
0613 Invalid Fiscal Year-End Day 
0614 Invalid Date of Most Recent Prospectus Supplement 
0615 Invalid Redemption Fee Percentage 
0616 Invalid Exchange Sell Eligibility Code 
0617 Invalid [[Dividend]] Accrual Purchase T+2 Start Date Code 
0618 Invalid [[Dividend]] Accrual Redemption T+2 Stop Date Code 

---

## Page 30

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 30  
Reject Code 
(MFPS, Phase I & II) 
Description 
0619 Invalid Exchange Fee Percentage 
0621 Invalid STR Rules Apply Code 
0622 Invalid LOI Rules Apply Code 
0623 Invalid LOI Alternate Fulfillment Period 
0624 Invalid LOI Minimum Initial Purchase Amount Type Code 
0625 Invalid LOI Minimum Initial Purchase Amount 
0626 Invalid LOI Back-Dating Days 
0627 Invalid Share Conversion Receiving Security [[ID]] 
0628 Invalid Statement Security [[ID]] Short Name 
0629 Invalid Statement Security [[ID]] Medium Name 
0630 Invalid Statement Security [[ID]] Long Name 
0631 Invalid Link Across Dealer Code 
0632 Invalid ROA/LOI Aggregation Inclusion Code 
0633 Invalid [[Dividend]] Accrual Bulk Rate Method Code 
0634 Invalid [[Dividend]] Accrual Month End Bulk Rate Method Code 
0636 Invalid [[Dividend]] Accrual Full Exchange In Start Date Code 
0637 Invalid [[Dividend]] Accrual Full Exchange Out Stop Date Code 
0638 Invalid [[Dividend]] Accrual Full Transfer In Start Date Code 
0639 Invalid [[Dividend]] Accrual Partial Transfer In Start Date Code 
0640 Invalid [[Dividend]] Accrual Full Transfer Out Stop Date Code 
0641 Invalid Number of Eligible Social Codes 
0643 Invalid Eligible Social Code 

---

## Page 31

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 31  
Reject Code 
(MFPS, Phase I & II) 
Description 
0644 Invalid Eligibility Code 
0645 Invalid Eligible Date 
0646 Invalid Number of Eligible Participants Minimum 
0647 Invalid Number of Active Participants Minimum 
0648 Invalid Minimum [[Asset]] Size for Eligibility 
0649 Invalid Maximum [[Asset]] Size for Eligibility 
0650 Invalid Requested Data Level 
0651 Invalid LOI Back-Dating Allowed Code 
0660 Another Security Issue [[ID]] exists with the same fund number and Class name and Portfolio name 
0661 Security Issue [[ID]] exists with different fund number, or Class name or Portfolio name 
0662 NAV Repurchase Share Class must be blank 
0663 NAV Repurchase Share class must be same as class name 
0664 NAV Repurchase must be populated 
0670 Target Field is Missing /Invalid 
0671 New Security Issue Country Code Missing/Invalid 
0672 New Security [[ID]] Already Exists or Invalid 
0673 New Security Issue Check Digit Missing/Invalid 
0674 New Share Class Already Exists 
0675 New Portfolio Name Already Exists 
0700 CDSC Rules Apply Code Must Be “Yes” for the Load Type Code 
0701 CDSC Rules Apply Code Must Be “No” for the Load Type Code 
0702 Brkpoint Rules Apply Code Must Be “Yes” for the Load Type Code 

---

## Page 32

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 32  
Reject Code 
(MFPS, Phase I & II) 
Description 
0703 Brkpoint Rules Apply Code Must Be “No” for the Load Type Code 
0704 LOI Rules Apply Code Must Be “1” for NAV Purch. Elig. Code 
0705 NAV Repurch CDSC Reimb. Code Must Be “No” 
0706 Max Purch Amt Greater than Max Acct Value 
0707 Max Purch Amt Less than Min Init Purch Amt 
0708 Max Purch Amt Less than Periodic / SYS Inv Purch Amt 
0709 Max Purch Amt Less than Min. IRA/ Roth IRA Init Purch Amt 
0710 Max Purch Amt Less than Min. IRA/ Roth IRA Subseq Purch Amt 
0711 Max Purch Amt Less than Min. Coverdell IRA Init Purch Amt 
0712 Max Purch Amt Less than Min. Coverdell IRA Subseq Purch Amt 
0714 Max Purch Amt Less than Min. Wrap Init Purch Amt 
0715 Max Purch Amt Less than Min. Wrap Subseq Purch Amt 
0716 Max Purch Amt Less than Min Qual Plan Init Purch Amt 
0717 Max Purch Amt Less than Min Qual Plan Subseq Purch Amt 
0718 Max Acct Value Is Less than Min Init Purch Amt 
0719 Max Acct Value Is Less than Min Subseq Purch Amt 
0720 Max Acct Value Is Less than Min Periodic / SYS Invst Purch Amt 
0721 Min Init Purch Amt Less than Min Periodic / SYS Invst Purch Amt 
0722 Min Init Purch Amt Is Less than Min Subseq Purch Amt 
0723 Min IRA / Roth IRA Init Amt Is Less than Min IRA / Roth IRA Subseq Amt 
0724 Max Acct Value Amt Is Less than Min IRA / Roth IRA Init Amt 
0725 Max Acct Value Amt Is Less than Min IRA/ Roth IRA Subseq Amt 

---

## Page 33

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 33  
Reject Code 
(MFPS, Phase I & II) 
Description 
0726 Max Acct Value Amt Is Less than Min Coverdell IRA Purch Amt 
0727 Min Coverdell IRA Purch Amt Is Less than Min Coverdell IRA Subseq Amt 
0728 Max Acct Value Amt Is Less than Min Coverdell IRA Subseq Amt 
0729 Max Acct Value Amt Is Less than Min Wrap Init Purch Amt 
0730 Min Wrap Init Purch Amt Is Less than Min Wrap Subseq Purch Amt 
0731 Max Acct Value Amt Is Less than Min Wrap Subseq Purch Amt 
0732 Max Acct Value Amt Is Less than Min Q.P. Plans Init Purch Amt 
0733 Min Q.P. Plans Init Pur Amt Is Less than Min Q.P. Plans Subseq Pur Amt 
0734 Max Acct Value Amt Is less than Min Q.P. Plans Subseq Pur Amt 
0735 Relationship Between [[participant]] Min and [[Asset]] Size Is Not Met 
0736 Gap / Overlap Between CDSC Lower and CDSC Upper Limit 
0737 Div Type Is Invalid for the Product Type (02) 
0738 Investment Class Code Is Invalid for the Product Type (02) 
0739 Selling Period Close Date Is Invalid for Offering Type Code 
0740 Selling Period Close Date Is Less than Selling Period Open Date 
0741 Date of Curr Prospectus Is Greater than Date of Most Recent Suppl 
0742 Div Accrl Purch Start Date Code Is Invalid for Div Type Code 
0743 Div Accrl Redemp Stop Date Code Is Invalid for Div Type Code 
0744 Div Accrl Exchng Stop Date Code Is Invalid for Div Type Code 
0745 Div Accrl Exchng Start Date Code Is Invalid for Div Type Code 
0746 Div Accrl Full Trans Start Date Code Is Invalid for Div Type Code 
0747 Div Accrl Part Trans Start Date Code Is Invalid For Div Type Code 

---

## Page 34

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 34  
Reject Code 
(MFPS, Phase I & II) 
Description 
0748 Div Accrl Trans Stop Date Code Is Invalid for Div Type Code 
0749 Div Accrl Bulk Rate Method Code Is Invalid For Div Type Code 
0750 Div Accrl Bulk Month-End Rate Code Is Invalid For Div Type Code 
0752 Invalid Portfolio Turnover Rate 
0753 Invalid Minimum Initial Purchase Amount via Automatic Investment Plan 
0754 Invalid Minimum Subsequent Purchase Amount via Automatic Investment Plan 
0755 Invalid Minimum Initial Purchase Amount Non-Qualified Plan (Referral P93) 
0756 Invalid Minimum Subsequent Purchase Amount Non-Qualified Plan (Referral P93) 
0757 Invalid Minimum Initial Purchase Amount (Omnibus Account) 
0758 Invalid Minimum Subsequent Purchase Amount (Omnibus Account) 
0759 Invalid Minimum Initial Purchase Amount via an Exchange 
0770 Invalid Price (NAV) Start Time 
0771 Invalid Price (NAV) Start Date 
0772 Invalid Price (NAV) Strike Time 
0773 Invalid Price (NAV) Indicator 
0774 Original Price Single/Multiple NAV Has Been Submitted 
0780 Invalid Minimum Subsequent Purchase Amount via an Exchange 
0790 Money Market Fund Indicator Missing or Invalid 
0791 Money Market Fund NAV Strike Time Format Missing or Invalid 
0792 Money Market [[Liquidity]] Fee/ Redemption Gate Eligibility Indicator is Missing or Invalid 
0794 Money Market Funds Number of NAV Strikes Missing or Invalid” 
0810 DCC&S Eligible Indicator Missing or Invalid 

---

## Page 35

MFPS I & II Reject Codes 
MFPS I & II Reject Codes 35  
Reject Code 
(MFPS, Phase I & II) 
Description 
0811 Defined Contribution Clearance & [[settlement]] (“DCC&S”) Cut-Off Cycle Missing or Invalid 
0812 [[Dividend]] Accrual Purchase T+1 Start Date Missing or Invalid 
0813 [[Dividend]] Accrual Redemption T+1 Stop Date Missing or Invalid 
0814 [[Dividend]] Accrual Partial Exchange Out Stop Date Missing or Invalid 
0815 [[Dividend]] Accrual Partial Exchange In Start Date Missing or Invalid 
0816 [[Dividend]] Accrual Partial Transfer Out Stop Date Missing or Invalid 
0817 [[Dividend]] Accrual ACAT Transfer In Start Date Missing or Invalid 
0818 [[Dividend]] Accrual ACAT Transfer Out Stop Date Missing or Invalid 
0819 DCC&S [[Dividend]] Accrual Purchase Start Date Missing or Invalid 
0820 DCC&S [[Dividend]] Accrual Purchase “G” (Share Class Conversion) Start Date Missing or Invalid 
0821 DCC&S [[Dividend]] Accrual Purchase “L” (Omnibus [[Dividend]] Reconciliation) Start Date Missing or 
Invalid 
0822 DCC&S [[Dividend]] Accrual Redemption Stop Date Missing or Invalid 
0823 DCC&S [[Dividend]] Accrual Redemption “G” (Share Class Conversion) Stop Date Missing or 
Invalid 
0824 DCC&S [[Dividend]] Accrual Redemption “L” (Omnibus [[Dividend]] Reconciliation) Stop Date Missing 
or Invalid 
0825 Eligible for Externalized Commission Indicator Missing or Invalid 
0826 Large Trade Notification Indicator Missing or Invalid 
0827 Large trade Threshold Dollar Amount Missing or Invalid 
 
 

---

## Page 36

 
  
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 