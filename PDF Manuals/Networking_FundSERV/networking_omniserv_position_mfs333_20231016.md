---
title: "Networking - Omni/SERV - Omnibus Position Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/networking_omniserv_position_mfs333_20231016.pdf"
pages: 21
size: "395.0 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Networking - Omni/SERV - Omnibus Position Record Layouts

**Original File:** [networking_omniserv_position_mfs333_20231016.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/networking_omniserv_position_mfs333_20231016.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 21  
**File Size:** 395.0 KB  

---

## Page 1

 
 
 
Networking - Omni/SERV 
OMNIBUS POSITION RECORD LAYOUTS 
OCTOBER 16, 2023 

---

## Page 2

Omnibus Position Record Layouts 
History of Important Notices 2 
 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 3 
Record Layouts .................................................................................................................................................... 4 
Omnibus Position File - Header Record ............................................................................................................ 5 
Omnibus Position File – Account Detail Record .............................................................................................. 6 
Omnibus Position File – Account LOI Record ................................................................................................ 10 
Omnibus Position File – Account Name & Address Record ......................................................................... 11 
Omnibus Position File – 529 Plan Account Beneficiary Record ................................................................... 12 
Omnibus Position File - Trailer Record ........................................................................................................... 13 
Omnibus Position File – Grand Total Trailer Record ..................................................................................... 15 
Input Records’ Layout ....................................................................................................................................... 16 
Omnibus Position File Datatrak Header ...........................................................................................................16 
Omnibus Position File Datatrak Trailer .............................................................................................................17 
Output Records’ Layout .................................................................................................................................... 18 
Omnibus Position Output Header File (N00) ....................................................................................................18 
APPENDIX – Summary of Changes .................................................................................................................. 19 
Effective Q1, 2019 ............................................................................................................................................19 
Effective Q3, 2017 ............................................................................................................................................19 
Effective Q2, 2017 ............................................................................................................................................19 
Effective Q4, 2015 ............................................................................................................................................20 
Effective Q3, 2012 ............................................................................................................................................20 
 

---

## Page 3

Omnibus Position Record Layouts 
History of Important Notices 3 
 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date: Important Notice 
October 16, 2023 Record rebranded and reviewed.  
May 12, 2023 Record rebranded and reviewed. 
March 25, 2019 Please see Important Notice:  
a8658 P&S 8233 Dated December 19, 2018 
July 24, 2017 Please see Important Notice:  
a8408 P&S 7983 Dated June 12, 2017 
April 17, 2017 Please see Important Notice:  
a8377 P&S 7952 Dated April 17, 2017 
June 15, 2016 Please see Important Notice:  
a8211 P&S 7786 Dated June 15, 2016 
October 12, 2015 Please see Important Notice:  
a8097 P&S 7672 Dated October 12, 2015 
August 13, 2012 Please see Important Notice:  
a7470 P&S 7040 Dated August 13, 2012 
July 15, 2011 Please see Important Notice:  
a7246 P&S 6816 Dated July 15, 2011 
June 14, 2010 Please see Important Notice:  
a6948 P&S 6518 Dated February 18, 2010 

---

## Page 4

Omnibus Position Record Layouts 
Record Layouts 4 
 
RECORD LAYOUTS 
The following are Networking Omnibus Position Record Layouts. The column headings are as follows: 
Field Name - The name of the field. 
Start - The position in which the field starts 
End - The position in which the field ends 
Len - The length of the field in bytes 
Description - Field description (format, valid values, conditional requirements, etc.). 
Reject Code - The Networking reject code is used which indicates that this field is invalid. 
 
All fields are character format, alpha/numeric: 
• All dollar, price, and share fields include the decimal point, [[DO]] not include commas, and are right justified, 
blank- filled. 
• [[shares]] are always 3 decimal places. 
• Dollar and share fields will include a stated negative sign if the transaction type is a debit to the balance. 
For example, the dollars and [[shares]] sold on redemption will be negative as will a purchase reversal. 
• Prices can have from 0 to 9 decimal positions 
• All dates are in ccyymmdd format. (March 15, 2010, for example, would be represented as 20100315)  
• Percent fields include the decimal point and [[DO]] NOT include commas or the % sign  

---

## Page 5

Omnibus Position Record Layouts 
Omnibus Position File - Header Record 5 
 
OMNIBUS POSITION FILE - HEADER RECORD 
This is a required record. There is one record per file.  
Input from Firm 
Output from [[NSCC]] to Fund 
Omnibus Position File - Header Record 
Field Name Start End Len Description Opt/ 
Req 
Reject 
Code 
Record [[ID]] 
DSPRID 
1 3 3 ‘BAL’ - Balance R 02 
Balance Date 
DSPDTB 
4 11 8 ccyymmdd R K2 
Filler 12 15 4 Space O  
Filler 16 55 40 Space O  
Submitting Firm Number 
DSPHFRM 
56 59 4 Must be valid [[NSCC]] [[participant]] Number R 03 
Filler 
DSPPAD 
60 85 26 Space O  
Receiving Fund Number 
DSPHRFND 
86 89 4 Must be valid [[NSCC]] [[participant]] Number R 04 
Filler 90 293 204 Space O  
[[NSCC]] Reject Indicator 
NSCC_REJ_IND 
294 294 1 Input: Space  
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code 1 
NSCC_REJ_COD1 
295 296 2 Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 
NSCC_REJ_COD2 
297 298 2 Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 
NSCC_REJ_COD3 
299 300 2 Input: Space 
Output: Reject code or space 
R  

---

## Page 6

Omnibus Position Record Layouts 
Omnibus Position File – Account Detail Record 6 
 
OMNIBUS POSITION FILE – ACCOUNT DETAIL RECORD 
This is a required record. There is one record per fund position.  
Input from Firm 
Output from [[NSCC]] to Fund 
Omnibus Position File – Account Detail Record 
Field Name Start End Len Description 
Record [[ID]] 
DSPRID 
1 3 3 ‘ACT’ - Account 
[[Broker]] Account Number 
DSPACT 
4 23 20 Account Number 
[[Broker]] account number (BIN) 
Fund Symbol 
DSPFND 
24 29 6 Fund [[ID]] used by the Firm. Normally Fund Symbol. 
Share Balance 
DSPSHR 
30 46 17 9999999999999. 999 
NAV 
DSPNAV 
47 62 16 9999999999999. 99 
Last available NAV for the fund 
For funds other than Money Market funds, this field 
supports a NAV with up to 9 decimal positions, based on 
the price precision rules defined for the fund. 
This field is formatted as follows for money-market funds: 
• The field displays the NAV with 3 decimal positions if 
the fund's price precision is 2 or less, or if no price 
precision is defined. 
• The field displays the NAV with more than 3 decimal 
positions if the fund's price precision is more than 3. 
Dealer Number on Account 
DSPDLR 
63 67 5 Dealer number on the account 
Dealer’s Branch [[ID]] on Account 
DSPBRN 
68 72 5 Dealer’s Branch [[ID]] on the account 
Representative [[ID]] on Account 
DSPREP 
73 87 15 Representative [[ID]] on the account 
Wrap Program Allocation Table 
DSPPMX 
88 92 5 Wrap program allocation table 
Affiliate on Account 
DSPAFF 
93 97 5 Additional affiliate (TPA) on the account 

---

## Page 7

Omnibus Position Record Layouts 
Omnibus Position File – Account Detail Record 7 
 
Field Name Start End Len Description 
Last Name of Representative 
DSPRNM 
98 107 10 Last Name of Representative 
Security Issue [[ID]] 
DSPCUS 
108 116 9 Security Issue [[ID]] 
Account Type Code 
DSPTYP 
117 119 3 Code identifying the type of account. 
Listed below are some common (but not standard) account 
type codes: 
1xx - Regular, Corporations, UGMA, Trusts  
2xx - 401(k) 
3xx 
4xx - Retirement - Individual 
5xx - Retirement - Qualified Plans  
6xx 
7xx 
8xx - Internal/House Accounts  
9xx - Outside - Nontaxable 
Blank code description may be variable. Contact the firm 
for their codes and descriptions. 
Social Code 
DSPSOC 
120 121 2 Refer to the [[DTCC]] Learning for Social Codes 
https://dtcclearning.com/documents/mutual-fund-services-
1/mfs-cross-product/codes-8/2498-social-codes/file.html 
VIP Code 
DSPVIP 
122 122 1 VIP Code 
Full Name of Representative 
DSPRN1 
123 162 40 Full Name of the Representative 
State for Blue Sky Reporting 
DSPSKY 
163 164 2 State used for Blue Sky reporting 
State of Residence 
DSPSTA 
165 166 2 State of residence 
CDSC Flag 
DSPCDS 
167 167 1 Flag set to Y if the account has [[shares]] that are still liable 
for CDSC 
Account Last Name 
DSPNAM 
168 179 12 Account Last Name 
Zip Code 
DSPZIP 
180 189 10 99999-9999 
ZIP+4 

---

## Page 8

Omnibus Position Record Layouts 
Omnibus Position File – Account Detail Record 8 
 
Field Name Start End Len Description 
Tax [[ID]] / SSN 
DSPTAX 
190 200 11 Tax [[ID]] or SSN. The number is formatted with dashes (-). 
ROA Group Number 
DSPROA 
201 220 20 All accounts in same ROA group will be linked by an ROA 
Group Number 
TPA Number 
DSPTPA 
221 224 4 Third Party Administrator [[ID]] Number 
Bank or Trust [[ID]] Number 
DSPTID 
225 228 4 Bank or Trust [[ID]] Number 
Alternate branch [[ID]] 
DSPABR 
229 237 9 Alternate branch [[ID]] ([[NSCC]] 9-digit branch) 
CIP Government [[ID]] Type 
DSPGIT 
238 241 4 CIP Government [[ID]] type. Free form description of the 
following [[ID]] field 
CIP Government [[ID]] Number 
DSPGOV 
242 261 20 CIP Government [[ID]] Number 
NRA Country Code 
DSPNRA 
262 263 2 Non-resident alien (NRA) country code. 
Remaining Cost of [[shares]] 
DSPCST 
264 279 16 9999999999999. 99 
Calculated inception-to-date (ITD) remaining cost value for 
the [[Ledger]]. 
Date [[Ledger]] was Opened 
DSPDOP 
280 287 8 Date the [[Ledger]] was opened. Format ccyymmdd 
DSPPGI 288 291 4 Program Indicator 
DSPDCO 292 292 1 [[Dividend]], Long-Term Capital Gain (LTCG), and 
Short-Term Capital Gain (STCG) distribution options. 
 
 Dividends LTCG STCG  
0 = Cash Cash Cash 
1 = Reinvest Reinvest Reinvest  
2 = Cash Cash Reinvest 
3 = Cash Reinvest Reinvest 
4 = Cash Reinvest Cash  
5 = Reinvest Cash Cash  
6 = Reinvest Reinvest Cash 
7 = Reinvest Cash Reinvest 
 

---

## Page 9

Omnibus Position Record Layouts 
Omnibus Position File – Account Detail Record 9 
 
Field Name Start End Len Description 
DSPMAT 293 296 4 Managed Account Type 
Filler 
DSPPD1 
297 300 4 Filler 

---

## Page 10

Omnibus Position Record Layouts 
Omnibus Position File – Account LOI Record 10 
 
OMNIBUS POSITION FILE – ACCOUNT LOI RECORD 
This is an optional record. It will be present only if the account has an LOI.  
Input from Firm 
Output from [[NSCC]] to Fund 
Omnibus Position File – Account LOI Record 
Field Name Start End Len Description 
Record [[ID]] 
DSPRID 
1 3 3 ‘LOI’ - Letter of Intent 
Face Amount of LOI 
DSPLOI 
4 19 16 9999999999999. 99 
Face Amount of the Letter of Intent 
Start Date of LOI 
DSPDTL 
20 27 8 ccyymmdd 
Start date of the LOI 
Date LOI Expires 
DSPDTE 
28 35 8 ccyymmdd 
Date the LOI expires 
Total LOI Amount Invested To 
Date 
DSPLPD 
36 51 16 9999999999999. 99 
The total amount invested to date under the LOI 
Date the LOI Fulfilled 
DSPDTC 
52 59 8 ccyymmdd 
Date the LOI was fulfilled 
Prior Credit Amount Allowed 
DSPPRC 
60 75 16 9999999999999. 99 
Amount allowed as prior credit toward completion of the LOI 
Filler 
DSPPD2 
76 300 225 Space 

---

## Page 11

Omnibus Position Record Layouts 
Omnibus Position File – Account Name & Address Record 11 
 
OMNIBUS POSITION FILE – ACCOUNT NAME & 
ADDRESS RECORD 
This is an optional record. It will be present only if information is available on the sub- accounting system and 
the firm has agreed to provide to the fund group. 
Input from Firm 
Output from [[NSCC]] to Fund 
Omnibus Position File – Account Name & Address Record 
Field Name Start End Len Description 
Record [[ID]] 
DSPRID 
1 3 3 ‘AD1’ – Address 
Address First Line Number 
DSPADD 
4 4 1 The line number for the first line of address 
Registration Line 1 
DSPNA1 
5 44 40 The first line of registration 
Registration Line 2 
DSPNA2 
45 84 40 The second line of registration 
Registration Line 3 
DSPNA3 
85 124 40 The third line of registration 
Registration Line 4 
DSPNA4 
125 164 40 The fourth line of registration 
Registration Line 5 
DSPNA5 
165 204 40 The fifth line of registration 
City of Residence 
DSPCIT 
205 226 22 Note: residence State and ZIP provided on ACT record 
Province Name 
DSPPVC 
227 246 20 Province Name 
Country 
DSPCOU 
247 266 20 Country 
Filler 
DSPPD3 
267 300 34 Space 

---

## Page 12

Omnibus Position Record Layouts 
Omnibus Position File – 529 Plan Account Beneficiary Record 12 
 
OMNIBUS POSITION FILE – 529 PLAN ACCOUNT 
BENEFICIARY RECORD 
At least one record is required for each 529 Plan account. 
Field Name Start End Len Description 
DSPRID 1 3 3 Record Type ‘BEN’ 
DSPDES 4 6 3 Beneficiary designation. Valid values are  
PRI – Primary 
[[SEC]] - Secondary 
DSPBTX 7 17 11 Beneficiary tax [[ID]] number 
DSPBNM 18 59 42 Beneficiary Name 
DSPBDB 60 67 8 Beneficiary Date of Birth 
 
Format ccyymmdd 
DSPREL 68 75 8 Beneficiary relationship (such as spouse, relative, child) 
DSPCTZ 76 76 1 Beneficiary US non-citizenship flag. Valid values are:  
Y – Not a US citizen 
N – A US citizen 
DSPGEN 77 77 1 Beneficiary gender. Valid values are:  
F – female 
M – male 
DSPBPD 78 300 223 Filler 

---

## Page 13

Omnibus Position Record Layouts 
Omnibus Position File - Trailer Record 13 
 
OMNIBUS POSITION FILE - TRAILER RECORD 
This is a required record. It is the final record, one record per file.  
Input from Firm 
Output from [[NSCC]] to Fund 
Omnibus Position File - Trailer Record 
Field Name Start End Len Description Opt/ 
Req 
Reject 
Code 
Record [[ID]] 
DSPRID 
1 3 3 ‘TOT’ – Total R 02 
Total Number of ACT Records 
DSPCNT 
4 11 8 Number of detail (ACT) records O  
Total [[shares]] on ACT records 
DSPTSH 
12 28 17 9999999999999. 999 O  
Filler 29 32 4 Space O  
Filler 33 72 40 Space O  
Submitting Firm Number 
DSPTFRM 
73 76 4 Must be valid [[NSCC]] [[participant]] 
Number 
R 03 
Total Number of Records 
DSPTCN 
77 85 9 Total Number of records (including 
header & trailer) 
Total number of all detail records 
(ACT, LOI, AD1, USR, BEN) plus the 
management company header (BAL) 
and trailer (TOT) records. 
O  
Receiving Fund Number 
DSPTRFND 
86 89 4 Must be valid [[NSCC]] [[participant]] 
Number 
R 04 
Filler 90 293 204 Space O  
[[NSCC]] Reject Indicator 
NSCC_REJ_IND 
294 294 1 Input: Space Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code 1 
NSCC_REJ_COD1 
295 296 2 Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 
NSCC_REJ_COD2 
297 298 2 Input: Space 
Output: Reject code or space 
R  

---

## Page 14

Omnibus Position Record Layouts 
Omnibus Position File - Trailer Record 14 
 
Field Name Start End Len Description Opt/ 
Req 
Reject 
Code 
[[NSCC]] Reject Code 3 
NSCC_REJ_COD3 
299 300 2 Input: Space 
Output: Reject code or space 
R  

---

## Page 15

Omnibus Position Record Layouts 
Omnibus Position File – Grand Total Trailer Record 15 
 
OMNIBUS POSITION FILE – GRAND TOTAL TRAILER 
RECORD 
Optional Input record from Firm to [[NSCC]] 
Required Output record from [[NSCC]] to Fund if accepted, to Firm if rejected 
This record is used to recap all Omnibus Position records, including headers and trailers, for a [[participant]]’s 
entire transmission. 
Omnibus Position File – Grand Total Trailer Record 
Field Name Start End Len Description Opt/ 
Req 
Record [[ID]] 
DSPRID 
1 3 3 ‘GRT’ – Grand Total R 
Filler 4 72 69 Space O 
Submitting Firm Number/ Recipient 
Number 
DSPGFRM 
73 76 4 Submitting Firm Number on Input from Firm to 
[[NSCC]]; 
Recipient Number on Output from [[NSCC]] to 
[[participant]] 
R 
Total Number of Records 
DSPGCN 
77 85 9 99999999 
Number of records included in the file (including 
Headers and Trailers) 
R 
Filler 86 300 215 Space O 

---

## Page 16

Omnibus Position Record Layouts 
Input Records’ Layout 16 
 
INPUT RECORDS’ LAYOUT 
Omnibus Position File Datatrak Header 
Input from Firm to [[NSCC]] 
Omnibus Position File Datatrak Header 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'HDR.S' R 
DATATRAK SYSID 6 10 5 A/N Value ‘26944’ R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N Clearing/settling firm number assigned by the 
[[NSCC]]. 
R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N Clearing/settling firm number assigned by the 
[[NSCC]]. 
R 
Processing Date 27 34 8 N Mmddccyy 
Next processing date 
R 
File Description 35 59 25 A/N Value ‘NETW OMNI POSITION INPUT’ R 
Multi Batch Indicator 60 60 1 A/N N = Not last batch  
Y = Last batch 
Always set to N (NO) 
R 
Multi Batch Number 61 63 3 N Each management company file is assigned a 
unique sequential number 
R 
Filler 64 300 237 A/N Space R 
 
 
  

---

## Page 17

Omnibus Position Record Layouts 
Input Records’ Layout 17 
 
Omnibus Position File Datatrak Trailer 
Input from Firm to [[NSCC]] 
Omnibus Position File Datatrak Trailer 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'END.S' R 
DATATRAK SYSID 6 10 5 A/N Value '26944' R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N Clearing/settling firm number assigned by the 
[[NSCC]]. 
R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N Clearing/settling firm number assigned by the 
[[NSCC]]. 
R 
Data File Record Count 
TOTAL_RECS 
27 33 7 N Total count of all records in the file except the 
DATATRAK Header (HDR.S) and the 
DATATRAK Trailer (END.S) 
R 
Filler 34 300 267 A/N Space R 

---

## Page 18

Omnibus Position Record Layouts 
Output Records’ Layout 18 
 
OUTPUT RECORDS’ LAYOUT 
Omnibus Position Output Header File (N00) 
Omnibus Position Output Header File (N00) 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 5 2 A/N 01 
MRO Recipient Number 6 9 4 N  
Literal 10 20 11 A/N Value '11111111111' 
Transmission Date 21 28 8 N mmddccyy 
Autoroute File [[ID]] 29 36 8 A/N Value '02100944' 
Literal 37 54 18 A/N Value ‘NETW OMNI POSITION’ 
Filler 55 300 246 A/N Space 
 
 

---

## Page 19

Omnibus Position Record Layouts 
APPENDIX – Summary of Changes 19 
 
APPENDIX – SUMMARY OF CHANGES 
Effective Q1, 2019 
REJECT CODES 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 
Effective Q3, 2017 
NEW FIELD 
Omnibus Position File – Account Detail Record 
Field Name Start End Len Description 
DSPMAT 293 296 4 Managed Account Type 
Effective Q2, 2017 
NEW FIELD 
Omnibus Position File – Account Detail Record 
Field Name Start End Len Description 
DSPDCO 292 292 1 [[Dividend]], Long-Term Capital Gain (LTCG), and Short- Term 
Capital Gain (STCG) distribution options. 
 
 Dividends LTCG STCG 
0 = Cash Cash Cash 
1 = Reinvest Reinvest Reinvest 
2 = Cash Cash Reinvest 
3 = Cash Reinvest Reinvest 
4 = Cash Reinvest Cash  
5 = Reinvest Cash Cash  
6 = Reinvest Reinvest Cash 
7 = Reinvest Cash Reinvest 
 
 
  

---

## Page 20

Omnibus Position Record Layouts 
APPENDIX – Summary of Changes 20 
 
Effective Q4, 2015 
NEW FIELD 
Omnibus Position File – Account Detail Record 
Field Name Start End Len Description 
DSPPGI 288 291 4 Program Indicator 
Effective Q3, 2012 
NEW FIELD 
Omnibus Position File – Account Detail Record 
Field Name Start End Len Description 
DSPTAG 288 291 4 User defined field 
 
 

---

## Page 21

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 16, 2023 
Publication Code: MFS333 
Service: Networking - Omni/SERV 
Title: Omnibus Position Record Layouts 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 