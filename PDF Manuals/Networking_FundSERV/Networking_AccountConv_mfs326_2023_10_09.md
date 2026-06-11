---
title: "Networking - Account Conversion/Update & Transfer/Acknowledgment Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Networking_AccountConv_mfs326_2023_10_09.pdf"
pages: 106
size: "936.1 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Networking - Account Conversion/Update & Transfer/Acknowledgment Record Layouts

**Original File:** [Networking_AccountConv_mfs326_2023_10_09.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Networking_AccountConv_mfs326_2023_10_09.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 106  
**File Size:** 936.1 KB  

---

## Page 1

 
 
 
Networking 
ACCOUNT CONVERSION/UPDATE & 
TRANSFER/ACKNOWLEDGMENT RECORD 
LAYOUTS 
OCTOBER 9, 2023  

---

## Page 2

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
History of Important Notices 2 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 6 
Account Conversion/Update (A/B/T50, A/B/T/F51) ........................................................................................... 8 
(A/B/T50, A/B/T/F51) #1 ..................................................................................................................................... 8 
(A/B/T50, A/B/T/F51) #2 ...................................................................................................................................14 
(A/B/T50, A/B/T/F51) #3 ...................................................................................................................................15 
(A/B/T50, A/B/T/F51) #4 ...................................................................................................................................17 
(A/B/T50, A/B/T/F51) #5 ...................................................................................................................................19 
(A/B/T50, A/B/T/F51) #6 ...................................................................................................................................23 
(A/B/T50, A/B/T/F51) #7 ...................................................................................................................................24 
(A/B/T50, A/B/T/F51) #8 ...................................................................................................................................25 
(A/B/T50, A/B/T/F51) #9 ...................................................................................................................................26 
(A/B/T50, A/B/T/F51) #10 .................................................................................................................................29 
(A/B/T50, A/B/T/F51) #11 .................................................................................................................................31 
(A/B/T50, A/B/T/F51) #12 .................................................................................................................................34 
(A/B/T50, A/B/T/F51) #13 .................................................................................................................................39 
(A/B/T50, A/B/T/F51) #14 .................................................................................................................................42 
(A/B/T50, A/B/T/F51) #15 .................................................................................................................................43 
(A/B/T50, A/B/T/F51) #16 .................................................................................................................................44 
(A/B/T50, A/B/T/F51) #17 Through #36 ............................................................................................................45 
(A/B/T50, A/B/T/F51) #37 .................................................................................................................................46 
(A/B/T50, A/B/T/F51) #38 (Effective On 03/28/2022) .......................................................................................47 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) .................................................................................. 49 
(A/B/T52, F53) #1 .............................................................................................................................................49 
(A/B/T52, F53) #2 .............................................................................................................................................52 
(A/B/T52, F53) #3 .............................................................................................................................................55 
(A/B/T52, F53) #4 .............................................................................................................................................57 
Conversion/Update And Transfer/Fund Acknowledgment Trailer (A/B/T/F 54) ........................................... 59 
Input Records’ Layout ....................................................................................................................................... 60 
Conversion File Datatrak Header .....................................................................................................................60 

---

## Page 3

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
History of Important Notices 3 
Conversion File Datatrak Trailer .......................................................................................................................61 
Output Records’ Layout .................................................................................................................................... 62 
Pending Transfer Reminder (N49) ....................................................................................................................62 
Output Header – Firm Conversion File (N00) ...................................................................................................63 
Output Header – Fund Conversion File (N00) ..................................................................................................64 
Input Acknowledgment - Conversion (NCN) .....................................................................................................65 
APPENDIX – Summary of Changes .................................................................................................................. 66 
Summary of changes – effective Q1, 2022 ...................................................................................................... 67 
Added New Record/Fields ................................................................................................................................67 
Summary of changes – effective Q4, 2020 ...................................................................................................... 69 
Change Requirements of the Existing Fields ...................................................................................................69 
Requirements Changed For Existing Records .................................................................................................71 
Documentation Update Only .............................................................................................................................72 
Reject Codes ....................................................................................................................................................72 
Summary of changes – effective Q2, 2020 ...................................................................................................... 73 
Change Requirements of the Existing Fields ...................................................................................................73 
Requirements Changed for Existing Records ..................................................................................................75 
Summary of changes – effective Q2, 2019 ...................................................................................................... 76 
Added New Field to Existing Records ..............................................................................................................76 
Rename / Add Values / Change Requirements of the Existing Fields .............................................................76 
Requirements Changed for Existing Records ..................................................................................................80 
Reject Codes ....................................................................................................................................................... 81 
Summary of changes – effective Q4, 2017 ...................................................................................................... 82 
Rename of Existing Fields ................................................................................................................................82 
Change to Description/Requirement to of Existing Fields ................................................................................82 
Summary of changes – effective Q1, 2017 ...................................................................................................... 83 
Requirements Changed for Existing Records ..................................................................................................83 
Added New Fields to Existing Records.............................................................................................................83 
Reject Codes ....................................................................................................................................................87 
Summary of changes – effective Q1, 2016 ...................................................................................................... 89 

---

## Page 4

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
History of Important Notices 4 
Effective, February 29, 2016, the JJJYXXXXXXX Algorithm will be Enforced on the Following Fields  ...........89 
Summary of changes – effective Q2, 2015 ...................................................................................................... 90 
Changes to Requirements of Existing Fields ....................................................................................................90 
Added New Field to Existing Records ..............................................................................................................92 
Requirements Changed for Existing Records ..................................................................................................93 
Summary of changes – effective Q3, 2014 ...................................................................................................... 94 
Changes to Description of Existing Fields ........................................................................................................94 
Summary of changes – effective Q4, 2013 ...................................................................................................... 95 
Changes to Description of Existing Fields ........................................................................................................95 
Added New Field to Existing Records ..............................................................................................................95 
Fatca: Added New Values to Existing Fields ....................................................................................................95 
Fatca: Added New Record/Fields .....................................................................................................................96 
Summary of changes – effective Q1, 2013 ...................................................................................................... 97 
Added New Field to Existing Records ..............................................................................................................97 
Requirements Changed for Existing Field ........................................................................................................97 
Summary of documentation changes – Q1, 2013 ........................................................................................... 98 
Changes to Description of Existing Values .......................................................................................................98 
Changes to Description of Existing Field ..........................................................................................................98 
Changes to Description of Existing Record ......................................................................................................99 
Summary of changes – effective Q2, 2012 .................................................................................................... 100 
Requirements Changed for Existing Field ......................................................................................................100 
Summary of changes – effective Q4 (December 5), 2011 ............................................................................ 101 
Added New Field to Existing Records ............................................................................................................101 
Summary of changes – effective Q4 (October 17), 2011 .............................................................................. 102 
Added New Field to Existing Records ............................................................................................................102 
Requirements Changed for Existing Field ......................................................................................................102 
Requirements Changed for Existing Records ................................................................................................103 
Summary of changes – effective Q4 (August 8), 2011 ................................................................................. 104 
Requirements Changed for Existing Field ......................................................................................................104 
Summary of changes – effective Q2, 2011 .................................................................................................... 105 

---

## Page 5

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
History of Important Notices 5 
Requirements Changed for Existing Field ......................................................................................................105 
Added New Fields to Existing Records...........................................................................................................105 
Requirements Changed for Existing Records ................................................................................................105 
 

---

## Page 6

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
History of Important Notices 6 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notice 
October 9, 2023 Document has been rebranded and reviewed. 
May 4, 2023 Document has been rebranded and reviewed. 
May 20, 2022 Links fixed due to Learning upgrade. 
March 28, 2022 Please see Important Notice: 
a9045 P&S 8618 Dated September 2, 2021 
November 16, 2020 Please see Important Notices: 
a8881 P&S 8454 Dated August 6, 2020  
April 06, 2020 Please see Important Notices: 
a8796 P&S 8369 Dated January 8, 2020  
June 17, 2019 Please see Important Notices: 
a8683 P&S 8258 Dated February 26, 2019  
November 20, 2017 Please see Important Notices: 
a8402 P&S 7977 Dated June 1, 2017  
February 27, 2017 Please see Important Notice: 
a8286 P&S 7861 Dated November 8, 2016 
February 29, 2016 Please see Important Notice: 
a8107 P&S 7682 Dated October 27, 2015 
April 27, 2015 Please see Important Notices: 
a7926 P&S 7501 Dated November 4, 2014 
July 28, 2014 Please see Important Notices: 
a7687 P&S 7357 Dated February 24, 2014 
November 18, 2013 Please see Important Notices: 
a7665 P&S 7235 Dated July 03, 2013 
March 18, 2013 Please see Important Notices: 
a7472 P&S 7042 Dated August 16, 2012, and  
a7567 P&S 7137 Dated January 9, 2013 
Documentation Changes Please see Important Notice: 
a7592 P&S 7162 Dated March 1, 2013 

---

## Page 7

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
History of Important Notices 7 
Effective Date Important Notice 
April 23, 2012 Please see Important Notices: 
a7355 P&S 6925 Dated January 12th, 2012 
December 5, 2011 Please see Important Notices: 
a7256 P&S 6826 Dated July 29th, 2011 
October 17, 2011 Please see Important Notices:  
a7241 P&S 6811 Dated July 8th, 2011 
August 8, 2011 Please see Important Notice: 
a7263 P&S 6833 Dated August 10th, 2011 
June 13, 2011 Please see Important Notices:  
a7175 P&S 6745 Dated March 7th, 2011 
November 22, 2010 Please see Important Notices:  
a7044 P&S 6615 Dated August 17th, 2010 
June 14, 2010 Please see Important Notices:  
a6948 P&S 6518 Dated February 18, 2010 
December 7, 2009 Please see Important Notices:  
a6874 P&S 6444 Dated September 17, 2009 
May 18, 2009 Please see Important Notices:  
a6791 P&S 6361 Dated February 17, 2009 
October 20, 2008 Please see Important Notices:  
a6658 P&S 6228 Dated July 11, 2008 
September 17, 2007 Please see Important Notices:  
 a6444 P&S 6014 Dated May 1, 2007 
November 20, 2006 Please see Important Notices:  
a6295 P&S 5865 Dated August 29, 2006 
a6272 P&S 5842 Dated July 17, 2006 
April 10, 2006 Please see Important Notice: 
a6173 P&S 5743 Dated December 22, 2005 
March 19, 2005 Please see Important Notice: 
a5976 P&S 5546 Dated February 4, 2005 

---

## Page 8

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 8 
ACCOUNT CONVERSION/UPDATE (A/B/T50, A/B/T/F51) 
(A/B/T50, A/B/T/F51) #1 
Required Record 
Input/Output 
The firm uses record type 50 to establish a Networking account at the fund. Record type 51 allows the firm or 
fund to update an existing Networking account. These records must be in sequential order and may also be 
used to set up a cross-reference file.  
Account Conversion/Update (A/B/T50, A/B/T/F51) #1 
#1 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
Scrub, or 
Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 01 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Reference Number 10 20 11 A/N Firm Reference Number Format: 
JJJYXXXXXXX, where: 
• JJJ- Julian date, 
• Y – Last digit of the current year, 
• XXXXXXX – Alphanumeric sequence. 
O/O 
Network Control 
Indicator 
21 21 1 A/N 0 = Matrix Level 0  
3 = Matrix Level 3 
4 = Matrix Level 4 
R/R 
Security Issue Number 22 30 9 A/N  R/R 

---

## Page 9

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 9 
#1 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Fund Account Indicator 31 31 1 A/N Required for Record Type 51 when any of the 
following fields is provided: 
Country of Origin 
State of Sale 
Withhold Indicator. 
 
0 = New Account – Domestic  
1 = New Account - Foreign  
2 = Existing Account - Domestic  
3 = Existing Account – Foreign 
4 = New account – US Tax Resident Living 
Abroad  
5 = Existing account – US Tax Resident 
Living Abroad  
R/OC 
Customer Account 
Number 
32 51 20 A/N Optional on Record Type 50 if Customer 
Account Number Indicator = '3' 
RC/R 
Book/Physical Share 
Indicator 
52 52 1 A/N (For Fund/SERV use)  
0 = Book [[shares]] - Name of Firm  
1 = Book [[shares]] - Name of Customer  
2 = Physical [[shares]]  
3 = Both Book and Physical [[shares]] 
O/O 
Payable Information 
Indicator 
53 53 1 A/N 0 = Address of Record  
1 = Payable Address  
2 = Automatic Clearing House  
3 = Cash to Firm  
4 = Cross Fund Re-Invest  
5 = Cash To Trust 
R/O 

---

## Page 10

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 10 
#1 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
[[Dividend]] Code 54 54 1 A/N 0 = [[Dividend]] Cash/LTCG-Cash/STCG - Cash 
1 = [[Dividend]] Reinvest/ LTCG-
Reinvest/STCG- Reinvest  
2 = [[Dividend]] Cash/LTCG- Cash/STCG-
Reinvest  
3 = [[Dividend]] Cash/LTCG- Reinvest/STCG - 
Reinvest  
4 = [[Dividend]] Cash/LTCG- Reinvest/STCG -
Cash  
5 = [[Dividend]] Reinvest/LTCG- Cash/STCG - 
Cash  
6 = [[Dividend]] Reinvest/ LTCG-
Reinvest/STCG- Cash  
7 = [[Dividend]] Reinvest/ LTCG-Cash/ STCG - 
Reinvest 
R/O 
SSN/EIN Number 
Indicator  
55 55 1 A/N Required for Record Type 51 when System 
Code = F 
0 = Tax Identification Number  
1 = Social Security Number 
2 = [[investor]] TIN/EIN 
R/OC SSN/EIN Number 56 64 9 A/N Required for Record Type 51 when System 
Code = F 
R/OC 

---

## Page 11

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 11 
#1 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Withhold Indicator 65 65 1 A/N W9 indications  
0 = Certified (W-9 on File)  
1 = Failure to Provide TIN  
2 = Failure to Certify TIN  
3 = Notification of incorrect TIN from the 
Secretary of Treasury (Withhold due to B 
Notice) 
4 = Failure to Certify Backup Withholding 
Status  
5 = Voluntary Disclosure from Payee of 
Affirmative Backup Withholding Status  
6 = Notification to commence Backup 
Withholding from Secretary of Treasury for 
underreporting [[Dividend]] and/or interest 
payments (Withhold due to C Notice) 
7 = Applied for Social Security Number  
8 = Exempt Recipient  
9 = Account(s) subject to both B and C Notice 
Withholding 
W8 indications  
A = Uncertified foreign account (no W8 form 
on file-backup withholding necessary)  
B = Certified foreign [[Beneficial Owner]] account 
(form W8-BEN on file)  
C = Certified foreign [[intermediary]] account 
(form W8-IMY on file)  
D = Certified valid foreign account (form W8-
ECI on file with ITIN)  
E = Certified foreign exempt account (form 
W8-IMY on file)  
F = W8 on file - no treaty rate claimed  
G = W8 Beneficiary with TIN on file  
H = W-8BEN-E on file/documentary evidence 
I = Voluntary FATCA withholding -W-8BEN-E 
on file/documentary evidence 
J = W8-IMY or W-8BEN-E  pending  
R/O 

---

## Page 12

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 12 
#1 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Account Line Indicator 66 66 1 A/N 1 = Account Name Ends on Line #1  
2 = Account Name Ends on Line #2  
3 = Account Name Ends on Line #3  
4 = Account Name Ends on Line #4 
 
Required for Record Type 50. 
 
Required for Record Type 51 when any 
Account Name/Address Line #1, #2, #3, #4 
are provided 
R/OC 
Customer Zip Code 67 75 9 A/N Required for Section 529 Account (Account 
Type = 1). 
OC/OC 
NRA Tax 76 77 2 N .99 O/O 
Social Code 78 79 2 A/N Required for Record Type 51 when System 
Code = F 
See Social Code list at 
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-
8/2498-social-codes/file.html under Codes in 
Mutual Fund section. 
R/OC 
 
Customer Account 
Number Indicator 
80 80 1 A/N 1 = Fund  
2 = Firm  
3 = Not Available (Record Type 50 only) 
R/R 
Scrub Indicator 81 81 1 A/N 0 = N/A 
1 = Scrub record. 
1 is allowed for fund input (System Code = F) 
only 
O/O 
Fund Account 
Response Indicator  
82 82 1 A/N 0 = Fund should NOT send a Fund Account 
Response record (F51) to the firm. 
1 = Fund should ALWAYS send a Fund 
Account Response record (F51) to the firm. 
2 = Fund should ONLY send a Fund Account 
Response record (F51) to the firm if the fund 
could not comply with the firm’s instructions 
O/O 
Clearing/Settling Fund 
Number 
83 86 4 N Required if System Code = F O/OC 
Returned from Post 
Office (RPO) Indicator 
87 87 1 A/N 0 = N/A 
1 = Returned from Post Office 
O/O 

---

## Page 13

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 13 
#1 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Account Type 88 88 1 A/N 0 = Regular Account 
1 = Section 529 Account 
 
Required for F51 (System Code = ‘F’) 
O/OC 
Account / Owner U.S. 
Citizenship Indicator 
89 89 1 A/N 0 = U.S. citizen 
1 = Not U.S. citizen 
 
Required for A/B/T50 and F51 (System Code 
= ‘F’) records when Account Type = 1 
(Section 529 Account)   
OC/OC Owner Date of Birth 90 97 8 A/N mmddccyy 
 
Best Practice: Provide Date of Birth if 
available 
O/O 
Filler 98 98 1 A/N  R/R 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R/R 
 
 
  

---

## Page 14

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 14 
(A/B/T50, A/B/T/F51) #2 
Optional Conditional Record 
Input/output 
This record is required for Record Type (A/B/T50).  
Account Conversion/Update (A/B/T50, A/B/T/F51) #2 
#2 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
Scrub, or 
Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 02 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Account Name/Address 
Line #1 
10 44 35 A/N  R/O 
Account Name/Address 
Line #2 
45 79 35 A/N  O/O 
PI Delivery Indicator 80 80 1 A/N (For Fund/SERV use)  
0 = Deliver to Customer  
1 = Deliver to Clearing /Settling Firm  
2 = Deliver to Agent for Firm 
O/O 
ROA Number 81 100 20 A/N Space O/O 
 
 
  

---

## Page 15

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 15 
(A/B/T50, A/B/T/F51) #3 
Optional Record 
Input/output 
Account Conversion/Update (A/B/T50, A/B/T/F51) #3 
#3 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
         Scrub, or 
         Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 03 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Account Name/Address  
Line #3 
10 44 35 A/N  O/O 
Account Name/Address  
Line #4 
45 79 35 A/N  O/O 
Fund/SERV Control 
Number 
80 94 15 A/N   O/O 
Target Date Fund 
Indicator 
95 95 1 A/N 0 = No  
1 = Yes 
O/O 
Age Based Indicator 96 96 1 A/N 1 = Aggressive  
2 = Moderate 
3 = Conservative 
O/O 
Age Based Roll 
Exempt Indicator 
97 97 1 A/N 0 = No, Account is not exempt and will be 
included within automatic age roll 
event; 
1 = Yes, Account is exempt from automatic 
age roll event. 
O/O 

---

## Page 16

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 16 
#3 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Account / Owner U.S. 
Resident Alien 
Indicator 
98 98 1 A/N 0 = No  
1 = Yes 
O/O 
Filler 99 100 2 A/N Space R/R 
 
 
  

---

## Page 17

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 17 
(A/B/T50, A/B/T/F51) #4 
Optional Conditional Record 
Input/output 
This record is required for Section 529 Account (Account Type = 1) and Record Type equals 50 or F51.  
Account Conversion/Update (A/B/T50, A/B/T/F51) #4 
#4 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
Scrub, or 
Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 04 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Account Name/Address 
Line #5 
10 44 35 A/N  O/O 
Columns 45-79 for regular Account (when Account Type = 0 or space) 
Account Name/Address 
Line #6 
 
45 79 35 A/N  O/O 
Columns 45-79 for Section 529 Account (when Account Type = 1) 
Account City 45 77 33 A/N Required for A/B/T50 and F51 (System 
Code = ‘F’) records when Account Type = 1 
(Section 529 Account).    
R/OC 
Account State 78 79 2 A/N Required for A/B/T50 and F51 (System 
Code = ‘F’) records when Account Type = 1 
(Section 529 Account).   
R/OC 

---

## Page 18

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 18 
#4 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Number of Beneficiaries 
and/or Successor 
Owner or Additional 
Account Owner 
80 81 2 N Required for A/B/T50 and F51 (System 
Code = ‘F’) records when Account Type = 1 
(Section 529 Account). 
 
If provided, valid values are 01-06.  Zeroes 
are not allowed. 
 
Space means there are no Beneficiaries 
and/or Successor or Additional Account 
Owner. 
OC/OC 
Successor Owner 
Indicator 
82 82 1 A/N 0 = No    
1 = Yes 
 
Only allowed when Account Type = 1 
(Section 529 Account).  
O/O 
Filler 83 100 18 A/N Space R/R 
 
 
  

---

## Page 19

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 19 
(A/B/T50, A/B/T/F51) #5 
Optional Conditional Record 
Input/output 
This record is required: 
• When the Payable Information Indicator (located on record #1) equals 1 or 2  
• When the System Code is A or T. 
Account Conversion/Update (A/B/T50, A/B/T/F51) #5 
#5 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account,  or 
        Scrub,                           or 
        Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 05 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Payable Account 
Number 
10 29 20 A/N Required if Payable Information Indicator 
equals 2. 
OC/OC 
Payable Zip Code 30 38 9 A/N Required if Payable Information Indicator 
equals 1. 
OC/OC 
Memo Field 39 50 12 A/N For Fund/SERV use O/O 
Payable Line Indicator 51 51 1 A/N Required if Payable Information Indicator 
equals 1 or 2  
1 = Payee Name Ends on Line 1  
2 = Payee Name Ends on Line 2  
3 = Payee Name Ends on Line 3  
4 = Payee Name Ends on Line 4 
OC/OC 

---

## Page 20

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 20 
#5 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
NAV Account Indicator 52 52 1 A/N 0 = Other  
1 = NAV Transfer  
2 = Repurchase  
3 = Employee  
4 = Firm/Error Account  
5 = Wrap Fee Account  
6 = No  
7 = Commissionable Defined Contribution 
Plan  
8 = Non-Commissionable- Defined 
Contribution Plan  
A = [[Dividend]] reinvestment trade  
B = Trust Company NAV per Agreement 
R/O 
Payable Address 
Options 
53 53 1 A/N Required if Payable Information Indicator 
equals 1 or 2  
1 = Dividends  
2 = Systematic Withdrawals  
3 = Automatic Drafts  
4 = Dividends and Automatic Drafts and 
Systematic Withdrawals  
5 = Dividends and Automatic Drafts  
6 = Dividends and Systematic Withdrawals  
7 = Automatic Drafts and Systematic 
Withdrawals  
8 = Cross Fund Reinvest  
9 = Alternate Payable 
OC/OC 
Purged Account 
Indicator 
54 54 1 A/N 0 = Not Applicable  
1 = Purged 
O/O 
Payable [[Option]] Delete 
Indicator 
55 55 1 A/N 0 = Not Applicable  
1 = Delete 
O/O 

---

## Page 21

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 21 
#5 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Payable Address Delete 
[[Option]] 
56 56 1 A/N  Required if Payable [[Option]] Delete Indicator 
= 1.  Not allowed otherwise. 
 
1 = Dividends  
2 = Systematic Withdrawals  
3 = Automatic Drafts  
4 = Dividends and Automatic Drafts and 
Systematic Withdrawals  
5 = Dividends & Automatic Drafts  
6 = Dividends and Systematic Withdrawals  
7 = Automatic Drafts and Systematic 
Withdrawals  
8 = Cross Fund Re-Invest  
9 = Alternate Payable 
OC/OC 
Payable A/C Number 
Indicator 
57 57 1 A/N 1 = Fund  
2 = Firm 
O/O 
Membership Identifier 58 59 2 A/N 01 = Trust [[Member]] information only  
02 = Networking Information Required for 
TPA/Investment Agent. 
 
For System Code = ‘A’ or ‘T’, if provided 
value must be = ‘02’. 
 
Best Practice: for F51 records,  
populate with ‘01’ for Trust Networked 
accounts and enter the Trust’s [[NSCC]]#  
in the “Trust/TPA/Investment Agent  
Number” field. 
O/O 
Trust/TPA/Investment 
Agent Number 
60 63 4 A/N Required if Membership Identifier = ‘02’ or 
System Code = ‘A’ or ‘T’. 
 
Required if Membership Identifier = ‘01’ and 
System Code = “F” (F51 records).  
OC/OC 
Underlying Firm Symbol 
(UFS) 
64 67 4 A/N Number that identifies the Underlying Firm 
(Banks/Trusts/Record Keepers/ TPA’s) that 
clear through another entity 
O/O 
Plan Account Number 68 87 20 A/N Plan account at the Trust, TPA, or Record 
Keeper 
O/O 

---

## Page 22

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 22 
#5 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Plan Account Number 
Indicator 
88 88 1 A/N Required if Plan Account Number is 
provided. 
1 = Trust 
2 = TPA 
3 = Record Keeper 
OC/OC Filler 89 100 12 A/N Space R/R 
 
 
  

---

## Page 23

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 23 
(A/B/T50, A/B/T/F51) #6 
Optional Conditional Record 
Input/output 
This record is required when the Payable Information Indicator (located on record #1) equals 1 or 2.  
Account Conversion/Update (A/B/T50, A/B/T/F51) #6 
#6 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account,  or 
        Scrub,                                    or 
        Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 06 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Payee Name/Address Line #1 10 44 35 A/N Required if Payable Information 
Indicator equals 1 or 2 
OC/OC 
Payee Name/Address Line #2 45 79 35 A/N  O/O 
Filler 80 100 21 A/N Space R/R 
 
 
  

---

## Page 24

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 24 
(A/B/T50, A/B/T/F51) #7 
Optional Record 
Input/output 
Account Conversion/Update (A/B/T50, A/B/T/F51) #7 
#7 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
        Scrub, or 
        Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 07 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Payee Name/Address Line #3 10 44 35 A/N  O/O 
Payee Name/Address Line #4 45 79 35 A/N  O/O 
Filler 80 100 21 A/N Space R/R 
 
 
  

---

## Page 25

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 25 
(A/B/T50, A/B/T/F51) #8 
Optional Record 
Input/output 
Account Conversion/Update (A/B/T50, A/B/T/F51) #8 
#8 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account,  or 
        Scrub,                                    or 
        Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 08 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Payee Name/Address Line #5 10 44 35 A/N  O/O 
Payee Name/Address Line #6 45 79 35 A/N  O/O 
Filler 80 100 21 A/N Space R/R 
 
 
  

---

## Page 26

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 26 
(A/B/T50, A/B/T/F51) #9 
Optional Conditional Record 
Input/output 
This record is required for Record Type 50 or for Fund input Record Type 51.  
Fields pertain to Change to B/D If Change in B/D Indicator equals 1 or 2, except when otherwise indicated.  
Account Conversion/Update (A/B/T50, A/B/T/F51) #9 
#9 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account,  or 
        Scrub,                                    or 
        Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 09 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Account Representative 
Number 
10 18 9 A/N Required when there is a new Firm [[ID]] # 
and System Code = B 
OC/OC 
Account Representative 
Name 
19 33 15 A/N Required when there is a new Firm [[ID]] # 
and System Code = B 
OC/OC 
Agent for Firm Number 34 37 4 A/N  O/O 
Branch Identification 
Number 
38 46 9 A/N Optional for Record Type 50, if 
Membership Identifier equals 01 or 02, 
and Agent for Firm Number is not 
provided.  
Required for Record Type 51, when 
there is a new Firm [[ID]] # 
RC/OC 
New Firm Identification # 47 66 20 A/N  O/O 
ACH Indicator 67 67 1 A/N Required when System Code = F  
0 = No  
1 = Yes 
OC/OC 
Systematic Contribution 
Indicator (SIP/PAC/PIP) 
68 68 1 A/N Required when System Code = F  
0 = No  
1 = Yes 
OC/OC 

---

## Page 27

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 27 
#9 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
SWP Indicator 69 69 1 A/N Required when System Code = F  
0 = No  
1 = Yes 
OC/OC 
Check Writing Privileges 70 70 1 A/N Required when System Code = F  
0 = No  
1 = Yes 
OC/OC 
New/Contra [[Broker]] of 
Record 
71 74 4 A/N Must be spaces if ‘Network Control 
Indicator’ is not zero and Change in 
[[Broker]]/Dealer Indicator is not provided.  
When System Code = ‘B’: 
• Required if Change in [[Broker]]/Dealer 
Indicator = 1 and Customer Account 
Number Indicator = 2.  
• Required if Change in [[Broker]]/Dealer 
Indicator = 2. 
 
A Fund’s [[NSCC]] # is only allowed for a 
B51 Record Type when:  
 
• ‘Network Control Indicator’ = 0 or 4, 
and ‘Change in [[Broker]]/Dealer 
Indicator’ = 2  (Change From 
[[Broker]]/Dealer).  
 
Otherwise, it is not validated. 
OC/OC 
[[Margin]] Account Indicator 75 75 1 A/N 0 = No  
1 = Yes 
R/O 
State of Sale 76 77 2 A/N  R/O 
Change in [[Broker]]/Dealer 
Indicator 
78 78 1 A/N 1 = Change To [[Broker]]/Dealer  
2 = Change From [[Broker]]/Dealer 
O/O 
SWIP (Systematic 
Withdrawal/ Investment 
Plan) Indicator 
79 79 1 A/N This field is Not allowed (must be blank) 
on records A/B/T50 and A/B/T51. 
Optional on F51. 
• Blank = N/A, no systematic plan on 
this account 
• 1 = New 
• 2 = Modified 
• 3 = Closed  
• 4 = Existing 
 
This field will be used to indicate the 
status of the systematic plan on the 
client’s account (new, modified, closed 
or existing). 
O 

---

## Page 28

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 28 
#9 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Account Open Date 80 87 8 A/N mmddccyy 
 
Must be a valid calendar date 
 
Required for F51 records (System Code 
= ‘F’). 
 
Best Practice: 
Date of account establishment for the 
particular Security Issue [[ID]]. This is NOT 
the date of account funding. 
O/OC 
Filler 88 100 13 A/N Space R/R 
 
 
  

---

## Page 29

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 29 
(A/B/T50, A/B/T/F51) #10 
Optional Conditional Record 
Input/Output 
This record is required: 
• When the Withhold Indicator (located on record #1) equals B, C, D or E   
• When the Payable Information Indicator (located on record #1) equals 2  
Account Conversion/Update (A/B/T50, A/B/T/F51) #10 
#10 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
Scrub, or 
Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 10 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
ABA Routing Number 10 18 9 A/N Required if Payable Information Indicator equals 2 OC/OC 
ROA/LOI Value 19 34 16 N 99,999,999,999,999.99 O/O 
LOI Number/Date 35 42 8 N  O/O 
Related Trade 
Indicator 
43 43 1 A/N 0 = No  
1 = Yes 
O/O 
Related Account 
Number 
44 63 20 A/N  O/O 
Country of Origin 64 65 2 A/N Required if Withhold Indicator = B, C, D, or E.  
In this case, the value 'OC' (Other Country) is not 
allowed 
OC/OC 
W8 Certification Date 66 73 8 N mmddccyy  
Required if Withhold Indicator = B, C, D, or E 
OC/OC 
W8 Expiration Date 74 81 8 N mmddccyy  
Required if Withhold Indicator = D or E or if 
Withhold Indicator = B and SSN/EIN Number is not 
provided 
OC/OC 

---

## Page 30

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 30 
#10 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
W8 Qualified 
[[intermediary]] Indicator 
82 82 1 A/N Required if Withhold Indicator = C.  
 
1 = QI (qualified [[intermediary]] - primary 
withholding)  
2 = QI (Qualified [[intermediary]] - non-withholding)  
3 = Non-QI (non-Qualified [[intermediary]] - non-
withholding, not the [[Beneficial Owner]])  
4 = Partnership (withholding)  
5 = Partnership (non-withholding)  
6 = U. S. branch (non-withholding)  
7 = Trust (withholding)  
8 = Trust (non-withholding) 
9 = Territory Financial Institution 
OC/OC 
W8 Override Country 
Code 
83 84 2 A/N The value 'OC' (Other Country) is not allowed O/O 
W8 Override NRA 
Special Rate 
85 89 5 N 99.999 O/O 
Filler 90 100 11 A/N Space R/R 
 
 
  

---

## Page 31

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 31 
(A/B/T50, A/B/T/F51) #11 
Optional Conditional Record 
Input/output 
This record is required when the Payable Address [[Option]] (located on record #5) equals 2, 4, 6, or 7   
Account Conversion/Update (A/B/T50, A/B/T/F51) #11 
#11 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
Scrub, or 
Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 11 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Systematic Withdrawal / 
Contribution Effective 
Date   
10 17 8 N mmddccyy O/O 
CDSC Payment Code 18 18 1 A/N 0 = Gross  
1 = Net  
2 = Not Applicable 
O/O 
Disbursement Options 19 19 1 A/N Required if Disbursement Amount is 
entered.  
0 = Fixed Cash Amount  
1 = Fixed %  
2 = Fixed [[shares]]  
3 = Declining Balance 
OC/OC 
Disbursement Amount 20 35 16 N Format according to Disbursement [[Option]] 
indicated above  
0 = 99,999,999,999,999.99  
1 = 99.9999999999999999  
2 = 999,999,999,999.9999  
3 = 999,999,999,999.9999 
O/O 

---

## Page 32

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 32 
#11 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Monthly Payment 
Indicators 
36 47 12 A/N 0 = No Payment  
1 = Payment 
O/O 
Payment Date Indicators 48 49 2 A/N Required if Monthly Payment Indicator = 1  
‘01 - 31’ = day of the month  
‘L’ = Last day of the month  
‘N’ = Normal Fund Cycle 
OC/OC 
Retirement Tax Indicator 50 51 2 A/N Required if Payable Address [[Option]] = 2, 4, 
6, 7 
01 = Premature Withdrawal 
02 = Rollover 
03 = Disability 
04 = Death 
05 = Prohibited 
06 = Other 
07 = Normal 
08 = Refund By Excess Contributions 
09 = Divorce 
10 = Plan Revoked 
11 = Fund Transfer 
99 = Not Applicable 
OC/OC 
Shareholder Bank 
Account Number 
52 71 20 A/N  O/O 
Shareholder Bank 
Account Type 
72 72 1 A/N Required if S/H Bank Account Number is 
Provided  
0 = Checking  
1 = Savings  
2 = Other 
OC/OC 
First Check Date 73 80 8 N mmddccyy O/O 

---

## Page 33

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 33 
#11 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Cost Basis [[Option]] 81 81 1 A/N 0 = Unknown 
1 = FIFO (First In First Out) 
2 = LIFO (Last In First Out)  
3 = High Cost 
4 = Low Cost 
5 = Average Cost 
6 = Select Lot  
O/O 
Filler 82 100 19 A/N Space R/R 
 
 
  

---

## Page 34

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 34 
(A/B/T50, A/B/T/F51) #12 
Optional Conditional Record 
Input/output 
This record is required: 
• for all System Codes when Payable Address [[Option]] in sequence #5 equals 8 or 9  
• for System Code = F (Fund) when “SWIP Indicator” in Sequence # 9 equals 1, 2 or 3  
Account Conversion/Update (A/B/T50, A/B/T/F51) #12 
#12 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
Scrub, or 
Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 12 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Payable Security Issue 
Country Code 
10 11 2 A/N Must be Space. For future use. R/R 
Payable Security Issue [[ID]] 12 20 9 A/N Required if Payable Address [[Option]] = 8 OC/OC 
Payable Security Issue 
Check Digit 
21 21 1 A/N Must be Space. For future use. R/R 
Alternate Payable Indicator 22 22 1 A/N Required if Payable Address [[Option]] = 9  
0 = Non-Payable Mailing Address 
(International Party)  
1 = Bank Registration (For Automatic Draft)  
2 = Other 
OC/OC 
Alternate Payable Reason 23 42 20 A/N Required if Alternate Payable Indicator is 
Equal to 2 
OC/OC 
Systematic Trade Changed 
From (old)  Amount 
43 58 16 N A dollar amount to be invested or redeemed 
on a predetermined frequency during the 
course of the calendar year as requested by 
the client. Investment/Withdrawal frequency 
is defined in the “Systematic trade changed 
from (old) frequency” and “Systematic trade 
changed to (new) frequency” fields. 
OC 

---

## Page 35

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 35 
#12 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
For example, if the client is systematically 
investing $100 each month of the calendar 
year and subsequently changed to $200 each 
month of the calendar year, “Systematic trade 
changed to (new) amount” field should be 
populated with “200” ($200), while 
“Systematic trade changed from (old) 
amount” field should contain the value of 
“100” ($100). 
 
99,999,999,999,999.99  
 
This field is NOT allowed (must be blank) on 
records A/B/T50 and A/B/T51. 
 
Required on record F51 if “SWIP Indicator” 
on F51 seq 9 is populated with “2=Modified” 
or “3=Closed”.  Zero value is not allowed 
when this field is Required. 
Not allowed and must be Blank if “SWIP 
Indicator” on F51 seq 9 is Blank. 
Best Practice: 
• This field should be blank when the 
“SWIP Indicator” field is populated with 
“1” = New 
• When “SWIP Indicator” is “2” = Modified, 
this field must be populated with a value 
that was in effect prior to this change 
• When “SWIP Indicator” is “3” = Closed, 
this field must be populated with the $ 
amount in effect prior to closing 
• When “SWIP Indicator” is “4” = Existing, 
this field should be blank. 
Systematic Trade Changed 
To (new) Amount 
59 74 16 N A dollar amount to be invested or redeemed 
on a predetermined frequency during the 
course of the calendar year as requested by 
the client. Investment/Withdrawal frequency 
is defined in the “Systematic trade changed 
from (old) frequency” and “Systematic trade 
changed to (new) frequency” fields. For 
example, if the client is systematically 
investing $100 each month of the calendar 
year and subsequently changed to $200 each 
month of the calendar year, “Systematic trade 
changed to (new) amount” field should be 
populated with “200” ($200), while 
“Systematic trade changed from (old) 
amount” field should contain the value of 
“100” ($100). 
 
99,999,999,999,999.99 
This field is NOT allowed (must be blank) on 
records A/B/T50 and A/B/T51. 
 
OC 

---

## Page 36

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 36 
#12 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Required on record F51 if “SWIP Indicator” 
field is populated with one of the following 
options: 
• “1” = New 
• “2” = Modified  
Zero value is not allowed when this field is 
Required. 
 
Not allowed and must be Blank if “SWIP 
Indicator” on F51 seq 9 is Blank. 
 
Best Practice 
• When “SWIP Indicator” is “1” = New, this 
field must be populated with $ amount 
(greater than zero) 
• When “SWIP Indicator” is “2” = Modified, 
this field must be populated with the new 
$ amount (greater than zero) 
• When “SWIP Indicator” is populated with 
“3” = Closed, this field should be blank.  
• When “SWIP Indicator” is “4” = Existing, 
this field should be populated as follows: 
If the F51 transaction provides an “update 
to existing account”, this field should be 
blank.   If the F51 transaction is a “Scrub 
file”, this field should be populated with 
the client’s systematic plan amount 
selection  
Systematic Trade Changed 
From (old) Frequency 
75 76 2 A/N Frequency of a systematic 
investment/withdrawal during the course of 
the calendar year.  For example, if the client 
has a systematic investment each month of 
the calendar year and subsequently changes 
this election to quarterly, “Systematic trade 
changed to (new) frequency” field should be 
populated with “04” (4 months = quarterly), 
while “Systematic trade changed from (old) 
frequency” field should contain the value of 
“12” (12 months = monthly). 
 
• Blank = N/A 
• 01 = 1 month per year 
• 02 = 2 months per year 
• 03 = 3 months per year 
• 04 = 4 months per year 
• 05 = 5 months per year 
• 06 = 6 months per year 
• 07 = 7 months per year 
• 08 = 8 months per year 
• 09 = 9 months per year 
• 10 = 10 months per year  
• 11 = 11 months per year 
• 12 = 12 months per year  
 
OC 

---

## Page 37

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 37 
#12 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
This field is Not allowed (must be blank) on 
records A/B/T50 and A/B/T51. 
 
Required on F51 if “SWIP Indicator” is 
populated with “2 = Modified” or “3 = Closed”.  
Blank is not allowed when this field is 
Required. 
Not allowed and must be Blank if “SWIP 
Indicator” on F51 seq 9 is Blank. 
 
Best Practice: 
• This field should be blank when the 
“SWIP Indicator” field is populated with 
“1” = New 
• When “SWIP Indicator” is populated with 
“2” = Modified, this field must be 
populated with the value that was in effect 
prior to this change (01-12) 
• When “SWIP Indicator” is “3 = Closed”, 
this field should be populated with the 
frequency that was in effect prior to 
closing (01-12) 
• When “SWIP Indicator” is “4” = Existing, 
this field should be blank.  
Systematic Trade Changed 
To (new) Frequency 
77 78 2 A/N Frequency of a systematic 
investment/withdrawal during the course of 
the calendar year.  For example, if the client 
has a systematic investment each month of 
the calendar year and subsequently changes 
this election to quarterly, “Systematic trade 
changed to (new) frequency” field should be 
populated with “04” (4 months = quarterly), 
while “Systematic trade changed from (old) 
frequency” field should contain the value of  
“12” (12 months = monthly). 
• Blank = N/A 
• 01 = 1 month per year 
• 02 = 2 months per year 
• 03 = 3 months per year 
• 04 = 4 months per year  
• 05 = 5 months per year 
• 06 = 6 months per year 
• 07 = 7 months per year 
• 08 = 8 months per year 
• 09 = 9 months per year 
• 10 = 10 months per year 
• 11 = 11 months per year 
• 12 = 12 months per year 
 
This field is Not allowed (must be blank) on 
records A/B/T50 and A/B/T51. 
Required on F51 if “SWIP Indicator” is 
populated with one of the following options: 
• “1” = New 
OC 

---

## Page 38

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 38 
#12 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
• “2” = Modified  
Blank is not allowed when this field is 
Required. 
 
Not allowed and must be Blank if “SWIP 
Indicator” is Blank. 
 
Best Practice:  
• When “SWIP Indicator” is “1” = New, this 
field must be populated with a value of 01 
- 12 
• When “SWIP Indicator” is “2” = Modified, 
this field must be populated with a value 
of 01 – 12 
• When “SWIP Indicator” is “3 = Closed”, 
this field should be blank 
• When “SWIP Indicator” is “4” = Existing, 
this field should be populated as follows: 
If the F51 transaction provides an “update 
to existing account”, this field should be 
blank.   If the F51 transaction is a “Scrub 
file”, this field should be populated with 
the client’s systematic plan frequency 
selection. 
Filler 79 100 22 A/N Space R/R 
 
 
  

---

## Page 39

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 39 
(A/B/T50, A/B/T/F51) #13 
Optional Conditional Record 
Input/output 
This record is required if the ‘Number of Beneficiaries/Successor Owner/Additional Account Owner’ field is 
populated with a value of 01 or greater: 
• For Section 529 (“Account Type” = 1): 
o At least one 529 Beneficiary (“Beneficiary/Successor Owner/Additional Account Owner Address 
[[Option]]” = ‘C’) is required.  
o If the “Successor Owner Indicator” = 1 and “Account Type” = 1, the “Beneficiary/Successor 
Owner/Additional Account Owner Address [[Option]]” must be populated with “D” (529 Successor 
Owner).  Only one 529 Successor Owner is allowed.  
• For Regular Account (“Account Type” = 0 or space): 
o The “Beneficiary/Successor Owner/ Additional Account Owner Address [[Option]]” field must be 
populated with either  ‘A’, ‘B’ or ‘E’.   No other values are allowed. 
Account Conversion/Update (A/B/T50, A/B/T/F51) #13 
#13 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
Scrub, or 
Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 13 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 

---

## Page 40

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 40 
#13 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Beneficiary/Successor 
Owner/Additional Account 
Owner Address [[Option]] 
10 10 1 A/N A = Primary IRA Beneficiary  
B = Secondary IRA Beneficiary  
C = 529 Beneficiary  
D = 529 Successor Owner  
E = Additional Account Owner 
 
Required for A/B/T50  
 
Required for F51 (System Code = ‘F’) 
records when Account Type = 1 
(Section 529 Account). 
 
Required when ‘Number of 
Beneficiaries/ and/or Successor Owner 
or Additional Account Owner” field (seq. 
4) is populated with a value of 01 or 
greater. 
 
For Account Type = 0 or space (Regular 
Account), value must = ‘A’, ‘B’, or ‘E’. 
 
For Account Type = 1 (Section 529 
Account), value must = ‘C’ or ‘D’.  
R/OC 
Beneficiary/Successor 
Owner/Additional Account 
Owner Date of Birth 
11 18 8 N mmddccyy 
 
Required for A/B/T50 when 
‘Beneficiary/Successor 
Owner/Additional Account Owner 
Address [[Option]]’ = 
 
A = Primary IRA Beneficiary 
B = Secondary IRA Beneficiary 
E = Additional Account Owner 
 
Best Practice: provide Date of Birth if 
available. 
OC/O 
Beneficiary/Successor 
Owner/Additional Account 
Owner U. S.  Citizenship 
Indicator  
19 19 1 A/N 0 = U.S. citizen  
1 = Not U.S. citizen 
 
Required for A/B/T50 and F51 records if 
‘Beneficiary/ Successor Owner/ 
Additional Account Owner Address 
[[Option]]’ = C (529 Beneficiary) 
 
Best Practice: Provide Citizenship 
Indicator if available. 
OC/OC 

---

## Page 41

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 41 
#13 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Beneficiary/Successor 
Owner/Additional Account 
Owner SSN/EIN Number 
20 28 9 A/N Required for A/B/T50 and F51 records if 
‘Beneficiary/ Successor Owner/ 
Additional Account Owner Address 
[[Option]]’ = C (529 Beneficiary). 
 
Best Practice: Provide SSN/EIN if 
available. 
OC/OC 
Beneficiary/Successor 
Owner/Additional Account 
Owner SSN/EIN Indicator 
29 29 1 A/N Required if Beneficiary/Successor 
Owner /Additional Account Owner 
SSN/EIN Number is provided 
 
0 = Tax [[ID]] number  
1 = Social security number  
OC/OC 
Beneficiary/Successor 
Owner /Additional Account 
Owner Relationship 
Indicator 
30 30 1 A/N 1 = Spouse  
2 = Non-Relative 
3 = Grandchild  
4 = Relative  
5 = Child 
O/O 
Beneficiary/Successor 
Owner/Additional Account 
Owner Name End Line 
Indicator  
31 31 1 A/N Required if Beneficiary/Successor 
Owner Name/Additional Account Owner 
Address is provided 
 
1-4 = Line number where name ends 
OC/OC 
Beneficiary/Successor 
Owner /Additional Account 
Owner Zip Code 
32 42 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 
digits for future postal expansion.  
 
Best Practice: Provide Zip Code if 
available. 
O/O 
Date of Event 
(The date when the 
Beneficiary will enter 
College) 
43 50 8 N mmddccyy O/O 
Filler 51 100 50 A/N Space R/R 
 
 
  

---

## Page 42

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 42 
(A/B/T50, A/B/T/F51) #14 
Optional Conditional Record 
Input/Output 
Required for A/B/T50 and F51 records if Beneficiary/Successor Owner/Additional Account Owner Address 
[[Option]] = C (529 Beneficiary).  
Account Conversion/Update (A/B/T50, A/B/T/F51) #14 
#14 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
        Scrub, or 
        Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 14 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Beneficiary/ Successor 
Owner/Additional Account 
Owner Name/Address    
Line #1 
10 44 35 A/N Required for A/B/T50 and F51 records if 
Beneficiary/ Successor Owner/Additional 
Account Owner Address [[Option]] = C (529 
Beneficiary). 
 
Best Practice: Provide Name/Address if 
available. 
OC/OC 
Beneficiary/ Successor 
Owner/Additional Account 
Owner Name/Address    
Line #2 
45 79 35 A/N  O/O 
Filler 80 100 21 A/N Space R/R 
 
 
  

---

## Page 43

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 43 
(A/B/T50, A/B/T/F51) #15  
Optional Record 
Input/output 
Account Conversion/Update (A/B/T50, A/B/T/F51) #15 
#15 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
        Scrub, or 
        Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 15 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Beneficiary/ Successor 
Owner/Additional Account 
Owner Name/Address 
Line #3 
10 44 35 A/N  O/O 
Beneficiary/ Successor 
Owner/Additional Account 
Owner Name/Address 
Line #4 
45 79 35 A/N  O/O 
Filler 80 100 21 A/N Space R/R 
 
 
  

---

## Page 44

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 44 
(A/B/T50, A/B/T/F51) #16  
Optional Record  
Input/output 
Account Conversion/Update (A/B/T50, A/B/T/F51) #16 
#16 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
        Scrub, or 
        Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 16 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Beneficiary/ Successor 
Owner /Additional Account 
Owner Name/Address 
Line #5 
 
10 44 35 A/N  O/O 
Beneficiary/ Successor 
Owner/Additional Account 
Owner City 
45 77 33 A/N Best Practice: Provide City if available. O/O 
Beneficiary/ Successor 
Owner/Additional Account 
Owner State 
78 79 2 A/N Best Practice: Provide State if available O/O 
Filler 80 100 21 A/N Space R/R 
 
 
  

---

## Page 45

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 45 
(A/B/T50, A/B/T/F51) #17 Through #36  
Input/output 
The previous group of four records (#13 through #16) may repeat itself up to 5 more times for additional 
Beneficiary information. 
Beneficiary/Successor Owner/Additional Account Owner information should be populated WITHOUT skipping 
repeatable sequence numbers.   
Sequence Numbers should be as follows: 
Sequences #17 through #20 are required if Number of Beneficiaries/ Successor Owner/A dditional Account 
Owner > 01.  
Sequences #21 through #24 are required if Number of Beneficiaries/ Successor Owner/Additional Account 
Owner > 02.  
Sequences #25 through #28 are required if Number of Beneficiaries/ Successor Owner/Additional Account 
Owner > 03.  
Sequences #29 through #32 are required if Number of Beneficiaries/ Successor Owner /Additional Account 
Owner > 04.  
Sequences #33 through #36 are required if Number of Beneficiaries/ Successor Owner/Additional Account 
Owner > 05. 
 
 
  

---

## Page 46

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 46 
(A/B/T50, A/B/T/F51) #37  
Optional Record 
Input/output 
Account Conversion/Update (A/B/T50, A/B/T/F51) #37 
#37 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
        Scrub, or 
        Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 37 R/R 
Clearing/Settling 
Firm Number 
6 9 4 N  R/R 
Chapter 4 Status 
Code 
10 11 2 A/N See list of values in the ‘Chapter 4 Status Codes’ 
at 
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-8/2240-
chapter-4-status-codes/file.html u nder the 
Documents section. 
O/O 
Global [[intermediary]] 
Identification Number 
12 36 25 A/N IRS issued number to identify and establish 
FATCA status of a Foreign Financial Institution 
(FFI) 
O/O 
Underlying Client’s 
Foreign Tax [[ID]]  
37 61 25 A/N Foreign Tax [[ID]] of Underlying Client O/O 
FATCA Override 
Special Rate 
62 66 5 N 99.999 O/O 
Filler 67 100 34 A/N Space R/R 
 
 
  

---

## Page 47

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 47 
(A/B/T50, A/B/T/F51) #38 (Effective On 03/28/2022) 
Optional Record 
Input/output 
Account Conversion/Update (A/B/T50, A/B/T/F51) #38 
#38 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 N 50 = New Account  
51 = Update to Existing Account, or 
        Scrub, or 
        Fund Account Response 
R/R 
Sequence Number 4 5 2 A/N 38 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
[[intermediary]] Program 
Indicator – 1 
10 13 4 A/N Indicates the program, platform, or channel 
applicable to an account.  
 
Examples may include: 
 
• Program indicator for advisory accounts 
• Distribution channel applicable to the   
account (e.g., retail, RIA, etc.) 
• Retirement platform pertaining to the 
account 
 
Values are uniquely defined by each 
[[intermediary]]. 
O/O 
[[intermediary]] Program 
Indicator – 2 
14 17 4 A/N Further defines the program, platform, or 
channel applicable to an account.  
 
Values are uniquely defined by each 
[[intermediary]]. 
O/O 

---

## Page 48

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Account Conversion/Update (A/B/T50, A/B/T/F51) 48 
#38 of 38 
Field Name  
Start End Len Type Description  Opt/Req 
50/51 
Servicing Group [[ID]] 18 26 9 A/N This field is used to communicate 
aggregated servicing relationships or define 
additional relationships on accounts. 
 
Examples may include: 
 
• Consolidating (Super) Branches 
• Third-party administrators (TPAs) 
• Investment Advisers 
• Consultants 
 
This field does not replace the main branch 
field on the account. 
 
Values are uniquely defined by each 
[[intermediary]]. 
O/O 
Additional Relationship 
[[ID]] – 1 
27 46 20 A/N This field is used to communicate additional 
relationship details to further define 
servicing relationships between accounts. 
 
Values are uniquely defined by each 
[[intermediary]]. 
O/O 
Additional Relationship 
[[ID]] – 2 
47 66 20 A/N This field is used to communicate additional 
relationship details to further define 
servicing relationships between accounts. 
 
Values are uniquely defined by each 
[[intermediary]]. 
O/O 
Filler 67 100 34 A/N Space R/R 

---

## Page 49

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) 49 
TRANSFER DETAIL/FUND ACKNOWLEDGMENT 
(A/B/T52, F53) 
(A/B/T52, F53) #1  
Required Record 
Input/output 
The transfer detail record is used by the firm to provide account detail to the fund for Networking account share 
transfers (A/B/T52).  
The fund uses record F53 to acknowledge the share movement or an account setup/update by a firm.  
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) #1 
#1 of 4 
Field Name  
Start End Len Type Description  Opt/Req 
52/53 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 A/N 52 = Account Transfer  
53 = Fund Acknowledgment 
R/R 
Sequence Number 4 5 2 N 01 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Clearing/Settling Fund 
Number 
10 13 4 A/N  O/R 
[[NSCC]] Control Number or 
Reference Number 
14 24 11 A/N 
For Record Type 52:  
Must be space on input;  
[[NSCC]] will create control number on output 
in the format of JJJYXXXXXXX. 
 
For Record Type 53:  
Must be either [[NSCC]] Control Number   
when Transaction Type = 1, 2, 4, 5, 8, 9  
or 
Firm Reference Number in the following 
format: JJJYXXXXXXX when Transaction 
Type = 3, 6 or 7. 
R/R 

---

## Page 50

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) 50 
#1 of 4 
Field Name  
Start End Len Type Description  Opt/Req 
52/53 
Transaction Type 25 25 1 A/N 1 = Sub-Account Credit  
2 = Transfer  
3 = Account Conversion / Update 
Acknowledgment  
4 = Mass [[Broker]] to [[Broker]] Conversion  
5 = Non-Networking Transfer  
6 = Change in [[Broker]]/Dealer - Change To 
B/D  
7 = Change in [[Broker]]/Dealer - Change 
From B/D  
8 = Non ACAT eligible transfer 
([[participant]] or [[CUSIP]] is not ACAT 
eligible) 
9 = ACAT Mutual Fund Fail Cleanup 
Transaction Type 6 or 7 allowed for 
Record Type F53 only.  
R/R 
Security Issue Number 26 34 9 A/N  R/R 
Account Number Indicator 35 35 1 A/N Optional for Transaction Type 3, 6 or 7.  
1 = Debit Firm Account #  
2 = Debit Fund Account #  
3 = New Fund Account #  (Credit Acct) 
O/RC 
Account Number 36 55 20 A/N Optional for Transaction Type 3, 6 or 7. O/RC 
Credit Account Indicator 56 56 1 A/N 1 = Firm Number  
2 = Fund Number  
3 = Not Available  
R/R 
Credit Account Number 57 76 20 A/N Optional if Credit Account Indicator = '3' RC/RC 
Transfer Type 77 77 1 A/N Optional For Transaction Type 3, 6 or 7.  
1 = Full Transfer  
2 = Partial Transfer 
RC/RC 
Network Control Indicator 78 78 1 A/N For Record Type 52, must be spaces.  
Required for Record Type 53, must be 
Transfer In Account or  
Conversion/Maintenance Account. 
0 = Matrix Level 0  
3 = Matrix Level 3 
4 = Matrix Level 4 
O/R 
Fund Reject Code 79 80 2 A/N  O/O 

---

## Page 51

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) 51 
#1 of 4 
Field Name  
Start End Len Type Description  Opt/Req 
52/53 
Firm Reference Number 81 91 11 A/N By using this field, Firm can link Record 
Type 52 with Record Type 50 when 
sending both at the same time 
 
Firm Reference Number Format: 
JJJYXXXXXXX, where 
• JJJ- Julian date, 
• Y – Last digit of the current year, 
• XXXXXXX – Alphanumeric sequence. 
O/O 
529 Transfer Reason 
Code 
92 92 1 A/N 1 = Owner - Resignation  
2 = Owner - Death 
3 = Owner - Divorce  
4 = Beneficiary Change – In Family  
5 = Beneficiary Change – Out of Family 
6 = In Kind  
7 = UGMA/UTMA (Age of Majority)  
O/O 
IRS 529 Annual Strategy 
Change Counter 
93 93 1 A/N 0 thru 9  O/O 
Gift Indicator 94 94 1 A/N Space = No  
1 = Yes 
O/O 
Filler 95 98 4 A/N Space R/R 
Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
O/O 
 
 
  

---

## Page 52

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) 52 
(A/B/T52, F53) #2  
Optional Conditional Record 
Input/output 
This Record is optional for Transaction Type 3, 6, or 7. 
The transfer detail record is used by the firm to provide account detail to the fund for Networking account share 
transfers.  
The fund uses this record to acknowledge the share movement or an account setup/update by a firm.  
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) #2 
#2 of 4 
Field Name  
Start End Len Type Description  Opt/Req 
52/53 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 A/N 52 = Account Transfer  
53 = Fund Acknowledgment 
R/R 
Sequence Number 4 5 2 N 02 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Clearing/Settling Fund 
Number 
10 13 4 A/N  O/R 
Share Amount 14 26 13 N Required for Transfer Type equals 2. 
999,999,999.9999 
OC/OC 
Effective Date 27 34 8 N Optional for Transaction Type 6 or 7. 
mmddccyy 
RC/RC 
Transaction Code 35 35 1 A/N 1 = Transfer to New Account  
2 = Transfer to Existing Account 
R/O 
Book / Physical Share 
Indicator 
36 36 1 A/N Optional for Transaction Type 6 or 7.  
1 = Transfer in & out: book [[shares]]  
2 = Transfer in: book [[shares]] Transfer out: 
physical [[shares]] 
RC/RC 
PI Delivery Indicator 37 37 1 A/N Optional for Transaction Type 6 or 7.  
0 = Deliver to Customer  
1 = Deliver to Clearing/ Settling Firm  
2 = Deliver to Agent for Firm  
3 = Not Applicable 
RC/RC 

---

## Page 53

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) 53 
#2 of 4 
Field Name  
Start End Len Type Description  Opt/Req 
52/53 
Agent for Firm Number 38 41 4 A/N  O/O 
Closing Balance (Debit 
Account) 
42 54 13 N 999,999,999.9999 
Will Not be allowed in record A/B/T52 
sequence #2 if Closing Balance (Debit 
Account) - Extended is provided in record 
A/B/T52 sequence #4.  
Required in record F53 sequence #2 if 
Closing Balance (Debit Account) - Extended is 
NOT provided in record F53 sequence #4 and 
Transaction Type is NOT equal to 6 or 7.  
Otherwise, it is not allowed. 
O/OC 
Closing Balance (Credit 
Account) 
55 67 13 N 999,999,999.9999 
Will Not be allowed on record A/B/T52 
sequence #2 if Closing Balance (Credit 
Account) - Extended is provided in record 
A/B/T52 sequence #4.  
Required in record F53 sequence #2 if 
Closing Balance (Credit Account) - Extended 
is NOT provided in record F53 sequence #4 
and Transaction Type is NOT equal to 6 or 7.  
Otherwise, it is not allowed. 
O/OC 
Firm Confirm Indicator 68 69 2 A/N  O/O 
Membership Identifier 70 71 2 A/N 01 = Trust [[Member]]  
02 = Networking information required for 
TPA/Investment Agent. 
O/O 
TPA/Investment Agent 
Number 
72 75 4 A/N Required if Membership Identifier = 02, or  
System Code = ‘A’ or ‘T’ 
OC/OC 
Receiving Firm 
Membership Identifier 
76 77 2 A/N 01 = Trust [[Member]] O/O 
Delivering Firm Share 
Aging Indicator 
78 78 1 A/N 1 = The delivering firm or fund company will 
provide the share aging information in an 
automated fashion through the Networking 
Share Aging file. 
2 = The delivering firm or fund company will 
provide the share aging information outside of 
the system. 
Note: Submitter of record type 52 is the 
Delivering Firm; Submitter of record type 53 is 
the Fund.) 
O/O 
Plan Account Number 79 98 20 A/N Plan account at the Trust, TPA, or Record 
Keeper 
O/O 

---

## Page 54

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) 54 
#2 of 4 
Field Name  
Start End Len Type Description  Opt/Req 
52/53 
Plan Account Number 
Indicator 
99 99 1 A/N Required if Plan Account Number is provided. 
1 = Trust 
2 = TPA 
3 = Record Keeper 
OC/OC 
Filler 100 100 1 A/N Space R/R 
 
 
  

---

## Page 55

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) 55 
(A/B/T52, F53) #3  
Optional Conditional Record 
Input/output 
This record is required when the Transaction Type (located on record sequence #1) equals:  
• 4 – Mass [[Broker]] to [[Broker]] Conversion   
• 8 – Non ACAT Eligible Transfer  
• 9 - ACAT Mutual Fund Fail Cleanup  
 
Otherwise, it is optional. 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) #3 
#3 of 4 
Field Name  
Start End Len Type Description  Opt/Req 
52/53 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 A/N 52 = Account Transfer  
53 = Fund Acknowledgment 
R/R 
Sequence Number 4 5 2 N 03 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Clearing/Settling Fund 
Number 
10 13 4 A/N  O/R 
Physical Share Amount 14 26 13 N 999,999,999.9999 O/O 
Receiving Firm 
Clearing/Settling Number 
27 30 4 A/N Required if Transaction Type equals: 
4 = Mass [[Broker]] to [[Broker]] 
Conversion 
8 = Non ACAT eligible transfer 
9 = ACAT Mutual Fund Fail Cleanup 
OC/OC 
Receiving Agent for Firm 
Number 
31 34 4 A/N  O/O 
Transfer Disbursement 
[[Option]] – Accruals 
35 35 1 A/N 2 = Cash to Customer – Delivering 
Firm  
4 = Reinvest – Receiving Firm  
(bucket to bucket) 
O/O 
Accrual Money Amount 36 51 16 N 99,999,999,999,999.99 O/O 

---

## Page 56

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) 56 
#3 of 4 
Field Name  
Start End Len Type Description  Opt/Req 
52/53 
ALL or NONE Indicator 52 52 1 A/N A = All  
B = None  
C = Not Accepted (C is Allowed for 
Record Type F53 only) 
O/O 
Cost Basis Money Amount 53 68 16 N 99,999,999,999,999.99 O/O 
Earnings to Date Money 
Amount 
69 84 16 N 99,999,999,999,999.99 O/O 
Negative Earnings to Date 
Indicator 
85 85 1 A/N N = Negative 
Spaces = Positive 
O/O 
Initiating Firm 86 89 4 A/N [[NSCC]] [[participant]] Number 
Required for A/B/T52 if Transaction 
Type equals: 
 
4 = Mass [[Broker]] to [[Broker]] 
Conversion 
8 = Non ACAT eligible transfer 
9 = ACAT Mutual Fund Fail Cleanup. 
 
Best Practices for Transaction Type 
4:  
[[NSCC]] [[ID]] of the [[Member]] creating and 
delivering this transaction to [[NSCC]]. 
 
Best Practices for Transaction Types 
8 & 9: 
The transfer request should be 
initiated by the delivering firm; the 
“Initiating Firm” [[NSCC]] [[ID]] should not 
match the [[NSCC]] [[ID]] of the “Receiving 
Firm Clearing /Settling Number” on 
seq. # 3. 
OC/O 
Filler 90 100 11 A/N Space R/R 
 
 
  

---

## Page 57

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) 57 
(A/B/T52, F53) #4   
Input/output 
• Record A/B/T52 sequence #4 is Optional Conditional  
This record will be required if: 
o Transaction Type = 4 (Mass [[Broker]] to [[Broker]] Conversion)   
o Transaction Type = 8 (Non ACAT Eligible Transfer) 
o Transaction Type = 9 (ACAT Mutual Fund Fail Cleanup) 
• Record F53 sequence #4 is Optional Conditional. 
This record will be required if: 
o Closing Balance (Debit Account) or Closing Balance (Credit Account) is NOT provided in record F53 
sequence #2; 
o Transaction Type = 4 (Mass [[Broker]] to [[Broker]] Conversion)    
o Transaction Type = 8 (Non ACAT Eligible Transfer) 
o Transaction Type = 9 (ACAT Mutual Fund Fail Cleanup) 
Otherwise, it is optional.  
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) #4 
#4 of 4 
Field Name  
Start End Len Type Description  Opt/Req 
52/53 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R/R 
Record Type 2 3 2 A/N 52 = Account Transfer  
53 = Fund Acknowledgment 
R/R 
Sequence Number 4 5 2 N 04 R/R 
Clearing/Settling Firm 
Number 
6 9 4 N  R/R 
Clearing/Settling Fund 
Number 
10 13 4 A/N  O/R 
Closing Balance (Debit 
Account) - Extended 
14 29 16 N 999,999,999,999.9999 
Will Not be allowed in record A/B/T52 
sequence #4 if Closing Balance (Debit 
Account) is provided in record A/B/T52 
sequence #2.  
Required in record F53 sequence #4 if Closing 
Balance (Debit Account) is NOT provided in 
record F53 sequence #2 and Transaction Type 
is NOT equal to 6 or 7.  Otherwise it is not 
allowed. 
O/OC 

---

## Page 58

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) 58 
#4 of 4 
Field Name  
Start End Len Type Description  Opt/Req 
52/53 
Closing Balance (Credit 
Account) - Extended 
30 45 16 N 999,999,999,999.9999 
Will Not be allowed in record A/B/T52 
sequence #4 if Closing Balance (Credit 
Account) is provided in record A/B/T52 
sequence #2.  
Required in record F53 sequence #4 if Closing 
Balance (Credit Account) is NOT provided in 
record F53 sequence #2 and Transaction Type 
is NOT equal to 6 or 7.  Otherwise it is not 
allowed. 
O/OC 
Credit Sub-Account 
Number 
46 65 20 A/N Underlying Credit Customer Account Number  
Required for Transaction Types: 
4 = Mass [[Broker]] to [[Broker]] Conversion 
8 = Non ACAT eligible transfer 
9 = ACAT Mutual Fund Fail Cleanup 
 
Best Practices for Transaction Types 4, 8 & 9: 
If the account is networked and the underlying 
sub-account number is not available, enter the 
Credit Account Number populated in seq. 1. 
OC/OC 
Debit Sub-Account 
Number 
66 85 20 A/N Underlying Debit Customer Account Number  
Required for Transaction Types: 
4 = Mass [[Broker]] to [[Broker]] Conversion 
8 = Non ACAT eligible transfer; 
9 = ACAT Mutual Fund Fail Cleanup 
 
Best Practices for Transaction Types 4, 8 & 9: 
If the account is networked and the underlying 
sub-account number is not available, enter the 
Debit Account Number populated in seq. 1. 
OC/OC 
ACATS Control Number 86 99 14 A/N  Required for Transaction Type 9 (ACAT 
Mutual Fund Fail Cleanup) 
 
(This is the original ACAT Control Number 
from the failed ACAT transfer) 
Format is: CCYYDDDNNNNNNN 
OC/OC 
Filler 100 100 1 A/N Space R 

---

## Page 59

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Conversion/Update And Transfer/Fund Acknowledgment Trailer (A/B/T/F 54) 59 
CONVERSION/UPDATE AND TRANSFER/FUND 
ACKNOWLEDGMENT TRAILER (A/B/T/F 54) 
Input/output Record 
Conversion/Update And Transfer/Fund Acknowledgment Trailer (A/B/T/F 54) 
Field Name  Start End Len Type Description  Opt/Req 
54 
System Code 1 1 1 A/N A = Investment Agent    
B = Firm  
F = Fund  
T = TPA 
R 
Record Type 2 3 2 A/N 54 R 
Filler 4 5 2 A/N Space R 
Clearing /Settling Number 
Of Submitting Firm 
6 9 4 N Firm or Fund R 
Total Conversion 
Transactions 
10 15 6 N 999,999 R 
Total Account Update 
Transactions 
16 21 6 N 999,999 R 
Total Account Transfers 22 27 6 N 999,999 R 
Total Acknowledgments 28 33 6 N 999,999 R 
Total Reminders 34 39 6 N 999,999  
Input: Space 
O 
Total Records 40 46 7 N 9,999,999 R 
Filler 47 100 54 A/N Space R 

---

## Page 60

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Input Records’ Layout 60 
INPUT RECORDS’ LAYOUT 
Conversion File Datatrak Header  
Input from Fund to [[NSCC]] or 
Input from Firm to [[NSCC]]  
Conversion File Datatrak Header 
Field Name  Start End Len Type Description  Opt/Req 
Literal 1 5 5 A/N Value 'HDR.S' R 
DATATRAK SYSID 6 10 5 A/N Value ‘26598’ (input from Fund) 
Or      ‘26599’ (input from Firm) 
R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N Value 'NETWORKING FUND CONV INP’ 
Or 'NETWORKING BRK CONV. INP’ 
R 
Multi Batch Indicator 60 60 1 A/N N = Not last batch  
Y = Last batch 
R 
Multi Batch Number 61 63 3 N  R 
Filler 64 100 37 A/N Space R 
 
 
  

---

## Page 61

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Input Records’ Layout 61 
Conversion File Datatrak Trailer  
Input from Fund to [[NSCC]] or 
Input from Firm to [[NSCC]]  
Conversion File Datatrak Trailer 
Field Name  Start End Len Type Description  Opt/Req 
Literal 1 5 5 A/N Value 'END.S' R 
DATATRAK SYSID 6 10 5 A/N Value '26598' (input from Fund) 
Or      ‘26599’ (input from Firm)    
R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Data File Record Count 27 33 7 N DATATRAK Header & Trailer not included in 
count 
R 
Filler 34 100 67 A/N Space R 

---

## Page 62

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Output Records’ Layout 62 
OUTPUT RECORDS’ LAYOUT 
Pending Transfer Reminder (N49)  
Output from [[NSCC]] to Funds and Firms  
Pending Transfer Reminder (N49) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 49 = Reminder Record 
Filler 4 5 2 A/N Space 
Clearing/Settling Firm # 6 9 4 N  
Clearing/Settling Fund 10 13 4 A/N  
[[NSCC]] Control Number 14 24 11 A/N  
Security Issue Number 25 33 9 A/N  
TPA/Investment Agent Number 34 37 4 A/N  
Receiving Firm Number 38 41 4 A/N This field will reflect the Receiving Firm 
Number if populated on the A/B/T52 seq#3. 
Filler 42 100 59 A/N Space 
 
 
  

---

## Page 63

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Output Records’ Layout 63 
Output Header – Firm Conversion File (N00)  
Output Header – Firm Conversion File (N00) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 5 2 A/N 01 
MRO Recipient Number 6 9 4 N  
Literal 10 20 11 A/N Value '11111111111' 
Transmission Date 21 28 8 N mmddccyy 
Autoroute File [[ID]] 29 36 8 A/N Value '02102070' 
Literal 37 53 17 A/N Value 'CONVERSION [[Broker]]’ 
Filler 54 100 47 A/N Space 
 
 
  

---

## Page 64

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Output Records’ Layout 64 
Output Header – Fund Conversion File (N00)  
Output Header – Fund Conversion File (N00) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 5 2 A/N 01 
MRO Recipient Number 6 9 4 N  
Literal 10 20 11 A/N Value '11111111111' 
Transmission Date 21 28 8 N mmddccyy 
Autoroute File [[ID]] 29 36 8 A/N Value '02102084' 
Literal 37 51 15 A/N Value 'CONVERSION FUND' 
Filler 52 100 49 A/N Space 
 
 
  

---

## Page 65

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Output Records’ Layout 65 
Input Acknowledgment - Conversion (NCN) 
Output from [[NSCC]] to Fund or Firm 
Input Acknowledgment - Conversion (NCN) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N CN = Conversion 
Filler 4 5 2 A/N Space 
Clearing/Settling # of Originator 
(Fund or Firm) 
6 9 4 N  
Processing Date 10 17 8 N mmddccyy 
Total Records Received 18 25 8 N 99,999,999  
Filler 26 100 75 A/N Space 
 

---

## Page 66

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
APPENDIX – Summary of Changes 66 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 

---

## Page 67

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q1, 2022 67 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2022 
Added New Record/Fields   
Record/Field Name Record Type and Location Description  
A/B/T50, A/B/T/F51 Sequence #38 Account Conversion/Update 
(A/B/T50, A/B/T/F51) #38 
 Optional Record 
[[intermediary]] Program Indicator - 1  A/B/T50, A/B/T/F51 seq.#38, start 10, 
end 13, length 4,  A/ N, O/O 
 
 
 
 
 
Indicates the program, platform, or channel 
applicable to an account.  
 
Examples may include: 
 
• Program indicator for advisory accounts 
• Distribution channel applicable to the   
account (e.g., retail, RIA, etc.) 
• Retirement platform pertaining to the 
account 
 
Values are uniquely defined by each 
[[intermediary]]. 
[[intermediary]] Program Indicator - 2   A/B/T50, A/B/T/F51 seq.#38, start 14, 
end 17, length 4, A/N, O/O 
Further defines the program, platform, or 
channel applicable to an account.  
 
Values are uniquely defined by each 
[[intermediary]]. 
Servicing Group [[ID]]    A/B/T50, A/B/T/F51 seq.#38, start 18, 
end 26, length 9, A/ N, O/O 
This field is used to communicate 
aggregated servicing relationships or define 
additional relationships on accounts.   
 
Examples may include: 
 
• Consolidating (Super) Branches 
• Third-party administrators (TPAs) 
• Investment Advisers 
• Consultants 
 
This field does not replace the main branch 
field on the account. 
 
Values are uniquely defined by each 
[[intermediary]]. 
Additional Relationship [[ID]] - 1 A/B/T50, A/B/T/F51 seq.#38, start 27, 
end 46, length 20, A/N, O/O 
This field is used to communicate additional 
relationship details to further define servicing 
relationships between accounts. 
 
Values are uniquely defined by each 
[[intermediary]]. 

---

## Page 68

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q1, 2022 68 
Record/Field Name Record Type and Location Description  
Additional Relationship [[ID]] - 2 A/B/T50, A/B/T/F51 seq.#38, start 47, 
end 66, length 20, A/N, O/O 
This field is used to communicate additional 
relationship details to further define servicing 
relationships between accounts. 
 
Values are uniquely defined by each 
[[intermediary]]. 

---

## Page 69

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4, 2020 69 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2020 
Change Requirements of the Existing Fields 
Field Name Record Type and Location Old Description New Description 
Owner Date of Birth A/B/T50, A/B/T/F51 seq.#1 
start 90 end 97, length 8, 
A/N, OC/OC 
 O/O 
mmddccyy 
Required for A/B/T50 and F51 
(System Code = ‘F’) records 
when Account Type = 1 (Section 
529 Account) 
mddccyy 
 
Best Practice: Provide Date of 
Birth if available 
Successor Owner 
Indicator 
A/B/T50, A/B/T/F51 seq.#4 
start 82 end 82, length 1, 
A/N, OC/OC 
 O/O 
Required for A/B/T50 and F51 
(System Code = ‘F’) records 
when Account Type = 1 (Section 
529 Account). 
0 = No    
1 = Yes 
 
Not allowed otherwise 
0 = No    
1 = Yes 
 
Only allowed when Account 
Type = 1 (Section 529 Account)  
Beneficiary/Successor 
Owner/Additional 
Account Owner Date 
of Birth 
A/B/T50, A/B/T/F51 seq.#13 
start 11 end 18, length 8, N, 
R/OC  OC/O 
mmddccyy 
 
Required for A/B/T50  
 
Required for F51 (System Code 
= ‘F’) records when Account 
Type = 1 (Section 529 Account) 
mmddccyy 
 
Required for A/B/T50 when 
‘Beneficiary/Successor 
Owner/Additional Account 
Owner Address [[Option]]’ = 
 
A = Primary IRA Beneficiary 
B = Secondary IRA Beneficiary 
E = Additional Account Owner 
 
Best Practice: provide Date of 
Birth if available 
Beneficiary/Successor 
Owner/Additional 
Account Owner U.S.  
Citizenship Indicator  
A/B/T50, A/B/T/F51 seq.#13 
start 19 end 19, length 1, 
A/N, OC/OC  
0 = U.S. citizen  
1 = Not U.S. citizen 
 
Required if Beneficiary/ 
Successor Owner/ Additional 
Account Owner Address [[Option]] 
= ‘C’ or ‘D’ for: 
 
• A/B/T50 records 
• F51 records 
0 = U.S. citizen  
1 = Not U.S. citizen 
 
Required for A/B/T50 and F51 
records if 
‘Beneficiary/Successor Owner/ 
Additional Account Owner 
Address [[Option]]’ = C (529 
Beneficiary). 
 
Best Practice: Provide 
Citizenship Indicator if 
available 

---

## Page 70

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4, 2020 70 
Field Name Record Type and Location Old Description New Description 
Beneficiary/Successor 
Owner/Additional 
Account Owner 
SSN/EIN Number 
A/B/T50, A/B/T/F51 seq.#13 
start 20 end 28, length 9, 
A/N, OC/OC  
Required if Beneficiary 
/Successor Owner/ Additional 
Account Owner Address [[Option]] 
= ‘C’ or ‘D’. 
 
• A/B/T50 records 
• F51 records 
Required for A/B/T50 and F51 
records if 
‘Beneficiary/Successor Owner/ 
Additional Account Owner 
Address [[Option]]’ = C (529 
Beneficiary). 
 
Best Practice: Provide SSN/EIN 
if available. 
Beneficiary/Successor 
Owner /Additional 
Account Owner Zip 
Code 
A/B/T50, A/B/T/F51 seq.#13 
start 32 end 42, length 11, 
A/N, O/OC   O/O  
5-digit Zip Code + 4-digit Zip-
Four + 2 digits for future postal 
expansion.  
Required for F51 records when 
Account Type = 1 (Section 529 
Account) 
5-digit Zip Code + 4-digit Zip-
Four + 2 digits for future postal 
expansion. 
 
Best Practice: Provide Zip 
Code if available 
Beneficiary/ Successor 
Owner/Additional 
Account Owner 
Name/Address Line #1 
A/B/T50, A/B/T/F51 seq.#14 
start 10 end 44, length 35, 
A/N, R/OC   OC/OC 
Required for A/B/T50 and F51 
(System Code = ‘F’) records 
when Account Type = 1 (Section 
529 Account)  
Required for A/B/T50 and F51 
records if 
‘Beneficiary/Successor 
Owner/Additional Account 
Owner Address [[Option]]’ = C 
(529 Beneficiary)  
 
Best Practice: Provide 
Name/Address if available. 
Beneficiary/ Successor 
Owner/Additional 
Account Owner City 
A/B/T50, A/B/T/F51 seq.#16 
start 45 end 77, length 33, 
A/N, O/OC   O/O 
Required for F51 records when 
Account Type = 1 (Section 529 
Account) 
Best Practice: Provide City if 
available 
Beneficiary/ Successor 
Owner/Additional 
Account Owner State 
A/B/T50, A/B/T/F51 seq.#16 
start 78 end 79, length 2, 
A/N, O/OC   O/O 
Required for F51 records when 
Account Type = 1 (Section 529 
Account). 
Best Practice: Provide State if 
available 

---

## Page 71

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4, 2020 71 
Requirements Changed For Existing Records 
Record Name Current Requirements New Requirements 
Record A/B/T50, 
A/B/T/F51 sequence 
#13 is Optional/ 
Conditional 
Record A/B/T50, A/B/T/F51 sequence #13 is 
Optional/ Conditional 
 
This record is required for Section 529 Account 
(“Account Type” =1). 
 
For Section 529 (“Account Type” = 1): 
• Sequences #13 through #16 are required if 
‘Number of Beneficiaries/ Successor 
Owner/Additional Account Owner” field is 
populated with a value of 01 or greater. 
• At least one 529 Beneficiary 
(“Beneficiary/Successor Owner/Additional 
Account Owner Address [[Option]]” = ‘C’) is 
required. 
• If the “Successor Owner Indicator” = 1 and 
“Account Type” = 1, the “Beneficiary/Successor 
Owner/Additional Account Owner Address 
[[Option]]” must be populated with “D” (529 
Successor Owner). Only one 529 Successor 
Owner is allowed. 
 
For Regular Account (“Account Type” = 0): 
• Sequences #13 through #16 are required if 
“Number of Beneficiaries/ Successor 
Owner/Additional Account Owner” field is 
populated with a value of 01 or greater. 
• The “Beneficiary/Successor Owner/ 
Additional Account Owner Address [[Option]]” 
field must be populated with either ‘A’, ‘B’ or 
‘E’. No other values are allowed. 
Record A/B/T50, A/B/T/F51 sequence #13 is 
Optional/ Conditional 
 
This record is required if the ‘Number of 
Beneficiaries/Successor/Owner/Additional 
Account Owner’ field is populated with a 
value of 01 or greater. 
 
For Section 529 (“Account Type” = 1): 
 
• At least one 529 Beneficiary 
(“Beneficiary/Successor Owner/Additional 
Account Owner Address [[Option]]” = ‘C’) is 
required.  
• If the “Successor Owner Indicator” = 1 and 
“Account Type” = 1, the 
“Beneficiary/Successor Owner/Additional 
Account Owner Address [[Option]]” must be 
populated with “D” (529 Successor Owner).  
Only one 529 Successor Owner is allowed.  
 
For Regular Account (“Account Type” = 0 or 
space): 
• The “Beneficiary/Successor Owner/ 
Additional Account Owner Address [[Option]]” 
field must be populated with either   ‘A’, ‘B’ or 
‘E’.   No other values are allowed. Account 
Conversion/Update 
Record (A/B/T50, 
(A/B/T/F51) #14 
Record A/B/T50, A/B/T/F51 sequence #14 is 
Optional/ Conditional  
This record is required for Section 529 Account 
(Account Type = 1) and Record Type equals 
50 or F51  
Record A/B/T50, A/B/T/F51 sequence #14 is 
Optional/ Conditional  
 
Required for A/B/T50 and F51 records if 
Beneficiary/Successor Owner/Additional 
Account Owner Address [[Option]] = C (529 
Beneficiary). 
Account 
Conversion/Update 
Record (A/B/T50, 
(A/B/T/F51) #16 
Record A/B/T50, A/B/T/F51 sequence #16 is 
Optional/ Conditional  
 
This record is required for Section 529 Account 
(Account Type = 1) and Record Type = F51 
 
Otherwise, it is optional.  
Record A/B/T50, A/B/T/F51 sequence #16 is 
an Optional Record. 
 

---

## Page 72

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4, 2020 72 
Documentation Update Only 
Field Name Record Type and 
Location 
Old Description New Description 
Account Line 
Indicator 
A/B/T50, A/B/T/F51 
seq.#1 start 66 end 
66, length 1, A/N, 
R/OC 
1 = Account Name Ends on Line #1  
2 = Account Name Ends on Line #2  
3 = Account Name Ends on Line #3  
4 = Account Name Ends on Line #4  
 
Required for Record Type 51 when any 
Account Name/Address Line #1, #2,  
#3, #4, #5, or #6 are provided. 
 
1 = Account Name Ends on Line #1  
2 = Account Name Ends on Line #2  
3 = Account Name Ends on Line #3  
4 = Account Name Ends on Line #4  
 
Required for Record Type 50.  
 
Required for Record Type 51 when 
any Account Name/Address Line #1, 
#2, #3, #4 are provided.  
Reject Codes 
The following reject codes have been eliminated: 
Reject Code Description 
H0 Beneficiary/Successor Owner Zip Code missing for Section 529 Account 
H1 Beneficiary/Successor Owner City or/and State missing for Section 529 Account 
 
Description of following existing reject codes have been updated: 
Reject Code Description New Description 
K9 Successor Owner Indicator is missing/invalid Successor Owner Indicator is invalid 
K4 Owner Date of Birth is missing/invalid Owner Date of Birth is invalid 

---

## Page 73

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2020 73 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2020 
Change Requirements of the Existing Fields 
Field Name Record Type and 
Location 
Old Description New Description 
A/B/T50, A/B/T/F51 seq.#9 
New/Contra [[Broker]] 
of Record 
A/B/T50, A/B/T/F51 
seq.#9 start 71 end 74, 
length 4, A/N, OC/OC 
Must be spaces if Networking 
Indicator is not zero and Change in 
[[Broker]]/Dealer Indicator is not 
provided.  
When System Code = ‘B’: 
• Required if Change in 
[[Broker]]/Dealer Indicator = 1 and 
Customer Account Number 
Indicator = 2.  
• Required if Change in 
[[Broker]]/Dealer Indicator = 2. 
 
Otherwise, it is not validated. 
Must be spaces if ‘Network Control 
Indicator’ is not zero and Change in 
[[Broker]]/Dealer Indicator is not 
provided.  
When System Code = ‘B’: 
• Required if Change in 
[[Broker]]/Dealer Indicator = 1 and 
Customer Account Number 
Indicator = 2.  
• Required if Change in 
[[Broker]]/Dealer Indicator = 2. 
 
A Fund’s [[NSCC]] # is only allowed  
for a B51 Record Type when:  
 
• ‘Network Control Indicator’  
= 0 or 4, and ‘Change in 
[[Broker]]/Dealer Indicator’ = 2 
(Change From [[Broker]]/Dealer).  
 
Otherwise, it is not validated. 
A/B/T52, F53 seq.#4 

---

## Page 74

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2020 74 
Field Name Record Type and 
Location 
Old Description New Description 
Credit Sub-Account 
Number 
A/B/T52, F53 seq.#4 
start 46 end 65, length 
20, A/N, OC/OC 
Underlying Credit Customer Account 
Number  
Required for Transaction Types: 
 
8 = Non ACAT eligible transfer 
9 = ACAT Mutual Fund Fail Cleanup 
 
Best Practices for Transaction Types 
8 & 9: 
If the account is networked and the 
underlying sub-account number is 
not available, enter the Credit 
Account Number populated in      
seq. 1. 
 
Best Practices for Transaction Type 
4 (Mass [[Broker]] to [[Broker]] 
Conversions):  
 
For TT4 this field is not required.  
However, it is recommended this 
field be populated in the same 
manner indicated above for TT8 and 
TT9. 
Underlying Credit Customer Account 
Number  
Required for Transaction Types: 
4 = Mass [[Broker]] to [[Broker]] 
Conversion 
8 = Non ACAT eligible transfer 
9 = ACAT Mutual Fund Fail Cleanup 
 
Best Practices for Transaction Types 
4, 8 & 9: 
If the account is networked and the 
underlying sub-account number is 
not available, enter the Credit 
Account Number populated in seq. 1.
 
 
 
Debit Sub-Account 
Number 
A/B/T52, F53 seq.#4 
start 66 end 85, length 
20, A/N, OC/OC 
Underlying Debit Customer Account 
Number  
Required for Transaction Types: 
8 = Non ACAT eligible transfer; 
9 = ACAT Mutual Fund Fail Cleanup 
 
Best Practices for Transaction Types 
8 & 9: 
If the account is networked and the 
underlying sub-account number is 
not available, enter the Debit 
Account Number populated in      
seq. 1. 
Best Practices for Transaction Type 
4 (Mass [[Broker]] to [[Broker]] 
Conversions):  
 
For TT4 this field is not required.  
However, it is recommended this 
field be populated in the same 
manner indicated above for TT8 and 
TT9. 
Underlying Debit Customer Account 
Number  
Required for Transaction Types: 
4 = Mass [[Broker]] to [[Broker]] 
Conversion 
8 = Non ACAT eligible transfer; 
9 = ACAT Mutual Fund Fail Cleanup 
 
Best Practices for Transaction Types 
4, 8 & 9: 
If the account is networked and the 
underlying sub-account number is 
not available, enter the Debit 
Account Number populated in seq. 1.
 

---

## Page 75

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2020 75 
Requirements Changed for Existing Records 
Record Name Current Requirements New Requirements 
Account Transfer/Fund 
Acknowledgment 
(A/B/T52, F53) #04 
Record A/B/T52 sequence #4 is Optional 
Conditional  
This record will be required if: 
• Transaction Type = 8 (Non ACAT Eligible 
Transfer) 
• Transaction Type = 9 (ACAT Mutual 
Fund Fail Cleanup) 
 
Record F53 sequence #4 is Optional 
Conditional. 
This record will be required if: 
• Closing Balance (Debit Account) or 
Closing Balance (Credit Account) is NOT 
provided in record F53 sequence #2; 
• Transaction Type = 8 (Non ACAT Eligible 
Transfer) 
• Transaction Type = 9 (ACAT Mutual 
Fund Fail Cleanup) 
Otherwise, it is optional.  
Record A/B/T52 sequence #4 is Optional 
Conditional  
This record will be required if: 
• Transaction Type = 4 (Mass [[Broker]] to 
[[Broker]] Conversion) 
• Transaction Type = 8 (Non ACAT Eligible 
Transfer) 
• Transaction Type = 9 (ACAT Mutual Fund Fail 
Cleanup) 
   
Record F53 sequence #4 is Optional Conditional. 
This record will be required if: 
• Closing Balance (Debit Account) or Closing 
Balance (Credit Account) is NOT provided in 
record F53 sequence #2; 
• Transaction Type = 4 (Mass [[Broker]] to 
[[Broker]] Conversion) 
• Transaction Type = 8 (Non ACAT Eligible 
Transfer) 
• Transaction Type = 9 (ACAT Mutual Fund Fail 
Cleanup) 
 
Otherwise, it is optional.  

---

## Page 76

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2019 76 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2019 
Added New Field to Existing Records 
New Field Name Record Type and Location Requirements  
Account Open 
Date 
A/B/T50, A/B/T/F51 seq.#9, 
start 80, end 87, length 8, A/N, 
O/OC 
mmddccyy 
 
Must be a valid Calendar Date 
 
Required for F51 records (System Code = F) 
 
Best Practice 
Date of account establishment for the particular Security 
Issue [[ID]].  This is NOT the date of account funding. 
Rename / Add Values / Change Requirements of the Existing Fields 
Field Name Record Type and 
Location 
Old Description New Description 
A/B/T50, A/B/T/F51 seq.#1 
Account Type A/B/T50, A/B/T/F51 
seq.#1 start 88 end 88, 
length 1, A/N, O/OC 
0 = Regular Account 
1 = Section 529 
Account 
0 = Regular Account 
1 = Section 529 Account 
 
Required for F51 (System Code = ‘F’) 
Account / Owner U.S. 
Citizenship Indicator 
A/B/T50, A/B/T/F51 
seq.#1 start 89 end 89, 
length 1, A/N, OC/OC 
Required for Section 
529 Account (Account 
Type = 1) 
0 = U.S. citizen 
1 = Not U.S. citizen 
Required for A/B/T50 and F51 (System 
Code = ‘F’) records when Account Type = 
1 (Section 529 Account)  
 
0 = U.S. citizen 
1 = Not U.S. citizen 
Owner Date of Birth A/B/T50, A/B/T/F51 
seq.#1 start 90 end 97, 
length 8, A/N, OC/OC 
Required for Section 
529 Account (Account 
Type = 1) 
mmddccyy 
Required for A/B/T50 and F51 (System 
Code = ‘F’) records when Account Type = 
1 (Section 529 Account)  
mmddccyy 
A/B/T50, A/B/T/F51 seq.#4 
Account City A/B/T50, A/B/T/F51 
seq.#4 start 45 end 77, 
length 33, A/N, R/OC 
Required for Section 
529 Account (Account 
Type = 1) 
Required A/B/T50 and F51 (System Code 
= ‘F’) records when Account Type = 1 
(Section 529 Account). 
Account State A/B/T50, A/B/T/F51 
seq.#4 start 78 end 79, 
length 2, A/N, R/OC 
Required for Section 
529 Account (Account 
Type = 1) 
Required A/B/T50 and F51 (System Code 
= ‘F’) records when Account Type = 1 
(Section 529 Account). 

---

## Page 77

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2019 77 
Field Name Record Type and 
Location 
Old Description New Description 
Number of Beneficiaries 
and/or Successor 
Owner, or Additional 
Account Owner 
/B/T50, A/B/T/F51 seq.#4 
start 80 end 81, length 2, 
A/N, OC/OC 
Required for Section 
529 Account (Account 
Type = 1) 
 
If provided, valid 
values are 01-06.  
Zeroes are not 
allowed. 
Space means there 
are no Beneficiaries 
and/or Successor 
Required A/B/T50 and F51 (System Code 
= ‘F’) records when Account Type = 1 
(Section 529 Account). 
 
If provided, valid values are 01-06.  Zeroes 
are not allowed. 
 
Space means there are no Beneficiaries 
and/or Successor or Additional Account 
Owner. 
Successor Owner 
Indicator 
/B/T50, A/B/T/F51 seq.#4 
start 80 end 81, length 2, 
A/N, OC/OC 
Required for Section 
529 Account (Account 
Type = 1) 
0 = No    
1 = Yes 
Not allowed otherwise 
Required A/B/T50 and F51 (System Code 
= ‘F’) records when Account Type = 1 
(Section 529 Account). 
0 = No    
1 = Yes 
 
Not allowed otherwise 
A/B/T50, A/B/T/F51 seq.#5 
Trust/TPA/Investment 
Agent Number 
A/B/T50, A/B/T/F51 
seq.#5, start 60 end 63, 
length 4, A/N, OC/OC 
Required if 
Membership Identifier 
= ‘02’ or System Code 
= ‘A’ or ‘T’.  
Required if Membership Identifier = ‘02’ or 
System Code = ‘A’ or ‘T’. 
 
For System Code = ‘A’ or ‘T’, if provided 
value must be = ‘02’. 
 
Required if Membership Identifier = ‘01’ 
and System Code = “F”  
(F51 records). 
A/B/T50, A/B/T/F51 seq.#13 

---

## Page 78

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2019 78 
Field Name Record Type and 
Location 
Old Description New Description 
Beneficiary/ 
Successor Owner/  
Additional Account 
Owner Address [[Option]] 
A/B/T50, A/B/T/F51 
seq.#13, start 10 end 10, 
length 1, A/N, OC/OC 
A = Primary IRA 
Beneficiary 
B = Secondary IRA 
Beneficiary 
C = 529 Beneficiary 
D = 529 Successor 
Owner 
A = Primary IRA Beneficiary 
B = Secondary IRA Beneficiary 
C = 529 Beneficiary 
D = 529 Successor Owner 
E = Additional Account Owner 
 
Required for A/B/T50.  
 
Required for F51 (System Code = ‘F’) 
records when Account Type = 1 
(Section 529 Account). 
 
Required when ‘Number of Beneficiaries/ 
and/or Successor Owner or Additional 
Account Owner” field (seq. 4) is populated 
with a value of 01 or greater. 
 
For Account Type = 0 (Regular Account), 
value must = ‘A’, ‘B’ or ‘E’. 
 
For Account Type = 1 (Section 529 
Account), value must = ‘C’ or ‘D’.  
Beneficiary/ 
Successor Owner/ 
Additional Account 
Owner  
Date of Birth 
A/B/T50, A/B/T/F51 
seq.#13, start 11 end 18, 
length 8, A/N, R/OC 
mmddccyy mmddccyy 
 
Required for A/B/T50  
 
Required for F51 (System Code = ‘F’) 
records when Account Type = 1 
(Section 529 Account). 
Beneficiary/ 
Successor Owner/ 
Additional Account 
Owner 
U.S. Citizenship 
Indicator  
A/B/T50, A/B/T/F51  
seq.#13, start 19 end 19, 
length 1, A/N, OC/OC 
Required if 
Beneficiary/Successor 
Owner Address [[Option]] 
= ‘C’ or ‘D’. 
 
0 = U.S. citizen  
1 = Not U.S. citizen 
Required if Beneficiary/Successor Owner/ 
Additional Account Owner Address 
[[Option]] = ‘C’ or ‘D’ for. 
 
• A/B/T50 
• F51 records 
 
0 = U.S. citizen  
1 = Not U.S. citizen 
Beneficiary/ 
Successor Owner/ 
Additional Account 
Owner 
SSN/EIN Number 
A/B/T50, A/B/T/F51  
seq.#13, start 20 end 28, 
length 9, A/N, OC/OC 
Required if 
Beneficiary/Successor 
Owner Address [[Option]] 
= ‘C’ or ‘D’. 
Required if Beneficiary/Successor Owner/ 
Additional Account Owner Address 
[[Option]] = ‘C’ or ‘D’ for. 
 
• A/B/T50 
• F51 records 

---

## Page 79

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2019 79 
Field Name Record Type and 
Location 
Old Description New Description 
Beneficiary/ 
Successor Owner/ 
Additional Account 
Owner 
SSN/EIN Indicator 
A/B/T50, A/B/T/F51  
seq.#13, start 29 end 29, 
length 1, A/N, OC/OC 
Required if 
Beneficiary/Successor 
Owner SSN/EIN 
Number is provided 
0 = Tax [[ID]] number 
1 = Social security 
number 
Required if Beneficiary/Successor 
Owner/Additional Account Owner 
SSN/EIN Number is provided 
 
0 = Tax [[ID]] number 
1 = Social security number 
Beneficiary/ 
Successor Owner/ 
Additional Account 
Owner 
Relationship Indicator 
A/B/T50, A/B/T/F51  
seq.#13, start 30 end 30, 
length 1, A/N, O/O 
 
 
1 = Spouse  
2 = Non-Relative 
3 = Grandchild  
4 = Relative  
5 = Child 
1 = Spouse  
2 = Non-Relative 
3 = Grandchild  
4 = Relative  
5 = Child 
Owner/Additional 
Account Owner Name 
End Line Indicator  
A/B/T50, A/B/T/F51  
seq.#13, start 31 end 31, 
length 1, A/N, OC/OC 
Required if 
Beneficiary/Successor 
Owner Name/Address 
is provided 
1-4 = Line number 
where name ends 
Required if Beneficiary/Successor Owner 
Name/Additional Account Owner 
Address is provided 
 
1-4 = Line number where name ends 
Beneficiary/ Successor 
Owner/ Additional 
Account Owner 
Zip Code 
A/B/T50, A/B/T/F51 
seq.#13, start 32 end 42, 
length 11, A/N, O/OC 
5digit Zip Code + 4digit 
Zip-Four + 2 digits for 
future postal 
expansion.  
5digit Zip Code + 4digit Zip-Four + 2 digits 
for future postal expansion.  
 
Required for F51 records when Account 
Type = 1 (Section 529 Account). 
A/B/T50, A/B/T/F51 seq.#14 
Beneficiary/ Successor 
Owner/ Additional 
Account Owner 
Name/Address Line #1 
A/B/T50, A/B/T/F51  
seq.#14, start 10 end 44, 
length 35, A/N, R/OC 
 Required for A/B/T50 and F51 (System 
Code = ‘F’) records when Account Type = 
1 (Section 529 Account) 
Beneficiary/ Successor 
Owner/ Additional 
Account Owner 
Name/Address Line #2 
A/B/T50, A/B/T/F51 
seq.#14, start 45 end 79, 
length 35, A/N, O/O 
  
A/B/T50, A/B/T/F51 seq.#15 
Beneficiary/ Successor 
Owner/ Additional 
Account Owner 
Name/Address Line #3 
A/B/T50, A/B/T/F51 
seq.#15, start 10 end 44, 
length 35, A/N, O/O 
  
Beneficiary/ Successor 
Owner/ Additional 
Account Owner 
Name/Address Line #4 
A/B/T50, A/B/T/F51 
seq.#15, start 45 end 79, 
length 35, A/N, O/O 
  

---

## Page 80

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2019 80 
Field Name Record Type and 
Location 
Old Description New Description 
A/B/T50, A/B/T/F51 seq.#16 
Beneficiary/ Successor 
Owner/ Additional 
Account Owner 
Name/Address Line #5 
A/B/T50, A/B/T/F51  
seq.#16, start 10 end 44, 
length 35, A/N, O/O 
  
Beneficiary/ Successor 
Owner/ Additional 
Account Owner City 
A/B/T50, A/B/T/F51  
seq.#16, start 45 end 77, 
length 33, A/N, O/OC 
 Required for F51 records when Account 
Type = 1 (Section 529 Account). 
Beneficiary/ Successor 
Owner/ Additional 
Account Owner State 
A/B/T50, A/B/T/F51  
seq.#16, start 78 end 79, 
length 2, A/N, O/OC 
 Required for F51 records when Account 
Type = 1 (Section 529 Account). 
Requirements Changed for Existing Records 
Record Name Current Requirements New Requirements 
Account 
Conversion/Update 
(A/B/T50, A/B/T/F51) 
#04 
This record is required for Section 
529 Account (Account Type = 1) 
and Record Type equals 50. 
This record is required for Section 529 Account (Account Type = 1) 
and Record Type equals 50 or F51.  
Account 
Conversion/Update 
(A/B/T50, A/B/T/F51) 
#14 
This record is required for Section 
529 Account (Account Type = 1) 
and Record Type equals 50.  
This record is required for Section 529 Account (Account Type = 1) 
and Record Type equals 50 or F51.  
Account 
Conversion/Update 
(A/B/T50, A/B/T/F51) 
#16 
This record is Optional  This record is required for Section 529 Account (Account Type 
= 1) and Record Type F51. 

---

## Page 81

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Reject Codes 81 
REJECT CODES 
Description of following reject codes have been updated: 
Reject Code Description 
G0 Trust/TPA/Investment Agent Number Missing/Invalid 
J4 Account Type is Missing/Invalid 
K8 Number of Beneficiaries/Successor Owners/Additional Account Owner is missing/invalid   
L0 Beneficiary/Successor Owner/Additional Account Owner Address [[Option]] is missing/invalid 
L1 Beneficiary/Successor Owner/Additional Account Owner Date of Birth is missing/invalid 
L2 Beneficiary/Successor Owner/ Additional Account Owner U.S. Citizenship Indicator is missing/invalid 
L3 Beneficiary/Successor Owner/ Additional Account Owner SSN/EIN Number is missing 
L4 Beneficiary/Successor Owner/Additional Account Owner SSN/EIN Indicator is missing/invalid 
L5 Beneficiary/Successor Owner/Additional Account Owner Relationship Indicator is invalid 
L6 Beneficiary/Successor Owner /Additional Account Owner Name End Line Indicator is missing/invalid  
M0 Beneficiary/ Successor Owner/ Additional Account Owner Name/Address Line #1 is missing 
M3 Beneficiary/Successor Owner/Additional Account Owner information does not correspond to Number 
of Bene/Succ/Additional Account Owners 
M5 Group of Sequence Records for Beneficiary/Successor Owner or Additional Account Owner is omitted  
Q8 Account Open Date is Missing/Invalid 
 
The following new reject codes have been added: 
Reject Code Description 
H0 Beneficiary/Successor Owner Zip Code missing for Section 529 Account 
H1 Beneficiary/Successor Owner City or/and State missing for Section 529 Account 

---

## Page 82

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4, 2017 82 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2017 
Rename of Existing Fields 
New Field Name Record Type and Location Old Name 
SSN/EIN Number Indicator A/B/T50, A/B/T/F51, seq#1, start 55, end 55, length 1, A/N, 
R/OC 
EIN/SS Number Indicator 
SSN/EIN Number A/B/T50, A/B/T/F51, seq#1, start 56, end 64, length 9, A/N, 
R/OC 
EIN/SS Number 
Change to Description/Requirement to of Existing Fields 
Field Name Record Type and Location Old Description New Description 
Credit Account 
Indicator 
A/B/T52/F53 seq#1, start 56, end 
56, length 1, A/N, RC 
1 = Firm Number  
2 = Fund Number  
3 = Not Available (Record Type 
52 only) 
1 = Firm Number  
2 = Fund Number  
3 = Not Available  
W8 Expiration Date A/B/T50, A/B/T/F51, seq#10, 
start 74, end 81, length 8, N, 
OC/OC 
mmddccyy  
Required if Withhold Indicator = 
D or E or if Withhold Indicator = 
B and EIN/SS Number is not 
provided 
mmddccyy  
Required if Withhold 
Indicator = D or E or if 
Withhold Indicator = B and 
SSN/EIN Number is not 
provided 

---

## Page 83

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q1, 2017 83 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2017 
Requirements Changed for Existing Records 
Record  Name Current Requirements New Requirements 
Account 
Conversion/Update 
(A/B/T50, A/B/T/F51) 
#12 
This record is required when: 
• Payable Address [[Option]] in 
sequence #5 equals 8 or 9 
This record is required: 
• for all System Codes when “Payable Address [[Option]]” in 
sequence #5 equals 8 or 9 
• for System Code = F (Fund) when “SWIP Indicator” in 
Sequence # 9 equals 1 or 2 or 3 
Added New Fields to Existing Records 
Field Name Record Type and Location Current  Description 
SWIP (Systematic 
Withdrawal/ 
Investment Plan) 
Indicator 
F51 seq.#9, start 79, end 79, 
length 1, A/N, Optional 
This field is Not allowed (must be blank) on records A/B/T50 
and A/B/T51. 
 Optional on F51. 
 
• Blank = N/A, no systematic plan on this account  
• 1 = New 
• 2 = Modified 
• 3 = Closed 
• 4 = Existing 
 
This field will be used to indicate the status of the systematic 
plan on the client’s account (new, modified, closed or existing). 

---

## Page 84

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q1, 2017 84 
Field Name Record Type and Location Current  Description 
Systematic Trade 
Changed From (old)  
Amount 
F51 seq#12, start 43, end 58, 
length 16, N, Optional/Conditional 
A dollar amount to be invested or redeemed on a 
predetermined frequency during the course of the calendar year 
as requested by the client. Investment/Withdrawal frequency is 
defined in the “Systematic trade changed from (old) frequency” 
and “Systematic trade changed to (new) frequency” fields. 
For example, if the client is systematically investing $100 each 
month of the calendar year and subsequently changed to $200 
each month of the calendar year, “Systematic trade changed to 
(new) amount” field should be populated with “200” ($200), 
while “Systematic trade changed from (old) amount” field should 
contain the value of  “100” ($100). 
 
99,999,999,999,999.99  
 
This field is NOT allowed (must be blank) on records A/B/T50 
and A/B/T51. 
 
Required on record F51 if “SWIP Indicator” on F51 seq 9 is 
populated with “2=Modified” or “3=Closed”.  Zero value is not 
allowed when this field is Required. 
Not allowed and must be Blank if “SWIP Indicator” on F51 seq 9 
is Blank. 
Best Practice: 
• This field should be blank when the “SWIP Indicator” field is 
populated with “1”=New 
• When “SWIP Indicator” is “2”=Modified, this field must be 
populated with a value that was in effect prior to this change 
• When “SWIP Indicator” is “3”=Closed, this field must be 
populated with the $ amount in effect prior to closing 
• When “SWIP Indicator” is “4”=Existing, this field should be 
blank.  

---

## Page 85

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q1, 2017 85 
Field Name Record Type and Location Current  Description 
Systematic Trade 
Change To (new)  
Amount 
F51 seq#12, start 59, end 74, 
length 16, N, Optional/Conditional 
A dollar amount to be invested or redeemed on a 
predetermined frequency during the course of the calendar year 
as requested by the client. Investment/Withdrawal frequency is 
defined in the “Systematic trade changed from (old) frequency” 
and “Systematic trade changed to (new) frequency” fields. For 
example, if the client is systematically investing $100 each 
month of the calendar year and subsequently changed to $200 
each month of the calendar year, “Systematic trade changed to 
(new) amount” field should be populated with “200” ($200), 
w
hile “Systematic trade changed from (old) amount” field should 
contain the value of  “100” ($100). 
 
99,999,999,999,999.99 
This field is NOT allowed (must be blank) on records A/B/T50 
and A/B/T51. 
 
Required on record F51 if  “SWIP Indicator” field is populated 
with one of the following options: 
• “1” = New 
• “2” = Modified  
Zero value is not allowed when this field is Required. 
 
Not allowed and must be Blank if “SWIP Indicator” on F51 seq 9 
is Blank. 
 
Best Practice 
• When “SWIP Indicator” is “1”=New, this field must be 
populated with $ amount (greater than zero) 
• When “SWIP Indicator” is “2”=Modified, this field must be 
populated with the new $ amount (greater than zero) 
• When “SWIP Indicator” is populated with “3”=Closed, this 
field should be blank.  
• When “SWIP Indicator” is “4”=Existing, this field should be 
populated as follows: If the F51 transaction provides an 
“update to existing account”, this field should be blank.   If 
the F51 transaction is a “Scrub file”, this field should be 
populated with the client’s systematic plan amount 
selection.  

---

## Page 86

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q1, 2017 86 
Field Name Record Type and Location Current  Description 
Systematic Trade 
Change From (old) 
Frequency 
F51 seq.#12, start 75, end 76, 
length 2, A/N, 
Optional/Conditional 
Frequency of a systematic investment/withdrawal during the 
course of the calendar year.  For example, if the client has a 
systematic investment each month of the calendar year and 
subsequently changes this election to quarterly, “Systematic 
trade changed to (new) frequency” field should be populated 
with “04” (4 months = quarterly), while “Systematic trade 
changed from (old) frequency” field should contain the value of  
“12” (12 months = monthly). 
 
• Blank = N/A 
• 01 = 1 month per year 
• 02 = 2 months per year 
• 03 = 3 months per year 
• 04 = 4 months  per year 
• 05 = 5 months per year 
• 06 = 6 months per year 
• 07 = 7 months per year 
• 08 = 8 months per year 
• 09 = 9 months per year 
• 10 = 10 months per year  
• 11 = 11 months per year 
• 12 = 12 months per year  
 
This field is Not allowed (must be blank) on records A/B/T50 
and A/B/T51. 
 
Required on F51 if “SWIP Indicator” is populated with 
“2=Modified” or “3=Closed”.  Blank is not allowed when this field 
is Required. 
 
Not allowed and must be Blank if “SWIP Indicator” on F51 seq 9 
is Blank. 
 
Best Practice: 
• This field should be blank when the “SWIP Indicator” field is 
populated with “1”=New 
• When “SWIP Indicator” is populated with “2”=Modified, this 
field must be populated with the value that was in effect 
prior to this change (01-12) 
• When “SWIP Indicator” is “3”=Closed, this field must be 
populated with the frequency that was in effect prior to 
closing (01-12) 
• When “SWIP Indicator” is “4”=Existing, this field should be 
blank. 

---

## Page 87

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q1, 2017 87 
Field Name Record Type and Location Current  Description 
Systematic Trade 
Change To (new) 
Frequency 
F51 seq.#12, start 77, end 78, 
length 2, A/N, 
Optional/Conditional 
Frequency of a systematic investment/withdrawal during the 
course of the calendar year.  For example, if the client has a 
systematic investment each month of the calendar year and 
subsequently changes this election to quarterly, “Systematic 
trade changed to (new) frequency” field should be populated 
with “04” (4 months = quarterly), while “Systematic trade 
changed from (old) frequency” field should contain the value of  
“12” (12 months = monthly). 
• Blank = N/A 
• 01 = 1 month per year 
• 02 = 2 months per year 
• 03 = 3 months per year 
• 04 = 4 months per year  
• 05 = 5 months per year 
• 06 = 6 months per year 
• 07 = 7 months per year 
• 08 = 8 months per year 
• 09 = 9 months per year 
• 10 = 10 months per year 
• 11 = 11 months per year 
• 12 = 12 months per year 
 
This field is Not allowed (must be blank) on records A/B/T50 
and A/B/T51. 
Required on F51 if “SWIP Indicator” is populated with one of the 
following options: 
• “1” = New 
• “2” = Modified  
Blank is not allowed when this field is Required. 
 
Not allowed and must be Blank if “SWIP Indicator” is Blank. 
 
 Best Practice:  
• When “SWIP Indicator” is “1”=New, this field must be 
populated with a value of 01 - 12 
• When “SWIP Indicator” is “2”=Modified, this field must be 
populated with a value of 01 – 12 
• When “SWIP Indicator” is “3=Closed”, this field should be 
blank 
• When “SWIP Indicator” is “4”=Existing, this field should be 
populated as follows: If the F51 transaction provides an 
“update to existing account”, this field should be blank.   If 
the F51 transaction is a “Scrub file”, this field should be 
populated with the client’s 
systematic plan frequency selection. 
Reject Codes 
The following new reject code have been added: 
 

---

## Page 88

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q1, 2017 88 
Reject Code Description 
X0 SWIP Indicator is invalid 
X1 Systematic Trade Changed From (old)  Amount is Missing/Invalid 
X2 Systematic Trade Changed To (new)  Amount is Missing/Invalid 
X3 Systematic Trade Changed From (old) frequency is Missing/Invalid 
X4 Systematic Trade changed To (new) frequency is Missing/Invalid 

---

## Page 89

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q1, 2016 89 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2016 
Effective, February 29, 2016, the JJJYXXXXXXX Algorithm will be 
Enforced on the Following Fields 
Field Name Record Type and Location Current Description 
Reference Number A/B/T50, AB/T/F51 seq.#1, start 10, 
end 20, length 11, A/N, O 
Firm Reference Number Format: JJJYXXXXXXX, 
where: 
• JJJ- Julian date, 
• Y – Last digit of the current year, 
• XXXXXXX – Alphanumeric sequence. 
[[NSCC]] Control Number or 
Reference Number 
A/B/T52, F53 seq.#1, start 14, end 24, 
length 11, A/N, R/R 
For Record Type 52:  
Must be space on input;  
[[NSCC]] will create control number on output in the 
format of JJJYXXXXXXX. 
 
For Record Type 53:  
Must be either [[NSCC]] Control Number   
when Transaction Type = 1, 2, 4, 5, 8, 9  
or 
Firm Reference Number in the following format: 
JJJYXXXXXXX when Transaction Type = 3, 6 or 
7 
Firm Reference Number A/B/T52, F53 seq.#1, start  81, end 91, 
length 11, A/N, O 
By using this field, Firm can link Record Type 52 
with Record Type 50 when sending both at the 
same time 
 
Firm Reference Number Format: JJJYXXXXXXX, 
where 
• JJJ- Julian date, 
• Y – Last digit of the current year, 
• XXXXXXX – Alphanumeric sequence. 

---

## Page 90

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2015 90 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2015 
Changes to Requirements of Existing Fields 
Field Name Record Type and 
Location 
Current  Description New Description 
[[NSCC]] Control 
Number or 
Reference 
Number 
A/B/T52, F53 seq.#1, 
start 14, end 24, 
length 11, A/N, R/R 
For Record Type 52:  
Must be space on input;  
[[NSCC]] will create control number on 
output in the format of 
JJJYXXXXXXX  
 
For Record Type 53: 
Must be either [[NSCC]] Control 
Number   
when Transaction Type = 1, 2, 4, 5  
or 
Firm Reference Number in the 
following format: JJJYXXXXXXX 
when Transaction Type = 3, 6 or 7.  
For Record Type 52:  
Must be space on input;  
[[NSCC]] will create control number on 
output in the format of JJJYXXXXXXX  
 
For Record Type 53:  
Must be either [[NSCC]] Control Number   
when Transaction Type = 1, 2, 4, 5, 8, 9  
or 
Firm Reference Number in the following 
format: JJJYXXXXXXX when 
Transaction Type = 3, 6 or 7.  
Transaction Type A/B/T52, F53 seq.#1, 
start 25, end 25, 
length 1, A/N, R/R 
1 = Sub-Account Credit  
2 = Transfer  
3 = Account Conversion / Update 
Acknowledgment  
4 = Mass [[Broker]] to [[Broker]] 
Conversion  
5 = Non-Networking Transfer  
6 = Change in [[Broker]]/Dealer - 
Change To B/D  
7 = Change in [[Broker]]/Dealer - 
Change From B/D  
 
Transaction Type 6 or 7 allowed for 
Record Type F53 only. 
1 = Sub-Account Credit  
2 = Transfer  
3 = Account Conversion / Update 
Acknowledgment  
4 = Mass [[Broker]] to [[Broker]] Conversion  
5 = Non-Networking Transfer  
6 = Change in [[Broker]]/Dealer - Change 
To B/D  
7 = Change in [[Broker]]/Dealer - Change 
From B/D  
8 = Non ACAT eligible transfer 
([[participant]] or [[CUSIP]] is not ACAT 
eligible) 
9 = ACAT Mutual Fund Fail Cleanup 
Transaction Type 6 or 7 allowed for 
Record Type F53 only. 
Receiving Firm 
Clearing/Settling 
Number 
A/B/T52, F53 seq.#3, 
start 27, end 30, 
length 4, A/N, OC/OC
 
Required if Transaction Type equals: 
 
4 = Mass [[Broker]] to [[Broker]] 
Conversion. 
Required if Transaction Type equals: 
 
4 = Mass [[Broker]] to [[Broker]] Conversion. 
8 = Non ACAT eligible transfer 
9 = ACAT Mutual Fund Fail Cleanup 

---

## Page 91

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2015 91 
Field Name Record Type and 
Location 
Current  Description New Description 
Initiating Firm A/B/T52, F53 seq.#3, 
start 86, end 89, 
length 4, A/N, OC/O 
[[NSCC]] [[participant]] Number 
Required for A/B/T52 if Transaction 
Type equals: 
 
4 = Mass [[Broker]] to [[Broker]] 
Conversion; 
[[NSCC]] [[participant]] Number 
Required for A/B/T52 if Transaction 
Type equals: 
 
4 = Mass [[Broker]] to [[Broker]] Conversion; 
8 = Non ACAT eligible transfer 
9 = ACAT Mutual Fund Fail Cleanup. 
 
Best Practices for Transaction Type 
4:  
[[NSCC]] [[ID]] of the [[Member]] creating and 
delivering this transaction to [[NSCC]]. 
 
Best Practices for Transaction Types 
8 & 9: 
The transfer request should be initiated 
by the delivering firm; the “Initiating 
Firm” [[NSCC]] [[ID]] should not match the 
[[NSCC]] [[ID]] of the “Receiving Firm 
Clearing /Settling Number” on seq. # 3. 
Credit Sub-
Account  Number 
A/B/T52, F53 seq.#4, 
start 46, end 65, 
length 20, A/N, 
OC/OC 
Underlying Credit Customer Account 
Number  
Underlying Credit Customer Account 
Number  
Required for Transaction Types: 
8 = Non ACAT eligible transfer 
9 = ACAT Mutual Fund Fail Cleanup 
 
Best Practices for Transaction Types 
8 & 9: 
If the account is networked and the 
underlying sub-account number is not 
available, enter the Credit Account 
Number populated in seq. 1. 
 
Best Practices for Transaction Type 
4 (Mass [[Broker]] to [[Broker]] 
Conversions):  
 
For TT4 this field is not required.  
However, it is recommended this field 
be populated in the same manner 
indicated above for TT8 and TT9. 

---

## Page 92

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2015 92 
Field Name Record Type and 
Location 
Current  Description New Description 
Debit Sub-
Account  Number 
A/B/T52, F53 seq.#4, 
start 66, end 85, 
length 20, A/N, 
OC/OC 
Underlying Credit Customer Account 
Number  
Underlying Debit Customer Account 
Number  
Required for Transaction Types: 
8 = Non ACAT eligible transfer 
9 = ACAT Mutual Fund Fail Cleanup 
 
Best Practices for Transaction Types 
8 & 9: 
If the account is networked and the 
underlying sub-account number is not 
available, enter the Debit Account 
Number populated in seq. 1. 
 
Best Practices for Transaction Type 
4 (Mass [[Broker]] to [[Broker]] 
Conversions): 
 
For TT4 this field is not required.  
However, it is recommended this field 
be populated in the same manner 
indicated above for TT8 and TT9. 
Receiving Firm 
Number 
N49 start 38, end 41, 
length 4, A/N  
Mass-[[Broker]]-to-[[Broker]] only This field will reflect the Receiving 
Firm Number if populated on the 
A/B/T52 seq#3. 
Added New Field to Existing Records 
New Field Name Record Type and Location Requirements  
ACATS Control 
Number 
A/B/T52, F53 seq.#4, start 86, end 99, length 
14, A/N, OC/OC 
Required for Transaction Type 9 (ACAT Mutual 
Fund Fail Cleanup) 
(This is the original ACAT Control Number from 
the failed ACAT transfer) 
Format is: CCYYDDDNNNNNNN 

---

## Page 93

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2015 93 
Requirements Changed for Existing Records 
Record Name Current Requirements New Requirements 
Transfer Detail/Fund 
Acknowledgment 
(A/B/T52, F53) #3 
This record is required when the 
Transaction Type (located on record 
sequence #1) equals 4.    Otherwise, it is 
optional. 
This record is required when the Transaction Type 
(located on record sequence #1) equals 
4 – Mass [[Broker]] to [[Broker]] Conversion; 
8 - Non ACAT Eligible Transfer, 
9 - ACAT Mutual Fund Fail Cleanup. 
Otherwise, it is optional. 
Transfer Detail/Fund 
Acknowledgment 
(A/B/T52, F53) #4 
Record A/B/T52 sequence #4 is Optional.  
 
Record F53 sequence #4 is Optional 
Conditional. This record will be required if 
Closing Balance (Debit Account) or 
Closing Balance (Credit Account) is NOT 
provided in record F53 sequence #2. 
Otherwise, it is optional.  
Record A/B/T52 sequence #4 is Optional 
Conditional. This record will be required if: 
- Transaction Type = 8 (Non ACAT Eligible 
Transfer) 
- Transaction Type = 9 (ACAT Mutual Fund Fail 
Cleanup) 
 
Record F53 sequence #4 is Optional Conditional.  
This record will be required if: 
- Closing Balance (Debit Account) or Closing Balance 
(Credit Account) is NOT provided in record F53 
sequence #2. 
- Transaction Type = 8 (Non ACAT Eligible 
Transfer) 
- Transaction Type = 9 (ACAT Mutual Fund Fail 
Cleanup) 
Otherwise, it is optional.  

---

## Page 94

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q3, 2014 94 
SUMMARY OF CHANGES – EFFECTIVE Q3, 2014 
Changes to Description of Existing Fields 
Field Name Record Type and 
Location 
Current  Description New Description 
Reference 
Number 
A/B/T50, A/B/T/F51, 
seq.#1, start 10, end 20, 
length 11, A/N, O/O 
Must be valid if used  Firm Reference Number Format: 
JJJYXXXXXXX, where: 
• JJJ- Julian date, 
• Y – Last digit of the current 
year, 
• XXXXXXX – Alphanumeric 
sequence. 
[[NSCC]] Control 
Number or 
Reference 
Number 
A/B/T52, F53 seq.#1, start 
14, end 24, length 11, 
A/N, R/R 
For Record Type 52:  
Must be space on input;  
[[NSCC]] will create control number on 
output in the format of 
JJJYXXXXXXX 
 
For Record Type 53:  
Must be either [[NSCC]] Control 
Number   
when Transaction Type = 1, 2, 4, 5  
or 
Firm Reference Number when 
Transaction Type = 3, 6 or 7. 
For Record Type 52:  
Must be space on input;  
[[NSCC]] will create control number on 
output in the format of 
JJJYXXXXXXX  
 
For Record Type 53:  
Must be either [[NSCC]] Control 
Number   
when Transaction Type = 1, 2, 4, 5  
or 
Firm Reference Number in the 
following format: JJJYXXXXXXX 
when Transaction Type = 3, 6 or 7. 
Firm 
Reference 
Number 
A/B/T52, F53 seq.#1, start 
81, end 91, length 11, 
A/N, O/O 
By using this field, Firm can link 
Record Type 52 with Record Type 
50 when sending both at the same 
time 
By using this field, Firm can link 
Record Type 52 with Record Type 
50 when sending both at the same 
time 
Firm Reference Number Format: 
JJJYXXXXXXX, where: 
• JJJ- Julian date, 
• Y – Last digit of the current 
year, 
• XXXXXXX – Alphanumeric 
sequence. 

---

## Page 95

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4, 2013 95 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2013 
Changes to Description of Existing Fields 
Field Name Record Type and Location Current  Description New Description 
[[NSCC]] Control 
Number or 
Reference 
Number 
A/B/T52, F53 seq.#1, start 14, 
end 24, length 11, A/N, R/R 
For Record Type 52:  
Must be space on input;  
[[NSCC]] will create control 
number on output  
For Record Type 52:  
Must be space on input;  
[[NSCC]] will create control number on 
output in the format of JJJYXXXXXXX  
Initiating Firm A/B/T52, F53 seq.#3, start 86, 
end 89, length 4, A/N, OC/O 
[[NSCC]] [[participant]] Number 
Required for A/B/T52 if 
Transaction Type = 4 
(Mass [[Broker]] to [[Broker]] 
Conversion) 
[[NSCC]] [[participant]] Number 
Required for A/B/T52 if Transaction Type 
= 4 (Mass [[Broker]] to [[Broker]] Conversion) 
[[NSCC]] [[ID]] of the [[Member]] creating and 
delivering this transaction to [[NSCC]]. 
Added New Field to Existing Records 
New Field Name Record Type and Location Requirements  
Plan Account Number A/B/T50, A/B/T/F51 seq.#5, start 68, end 87, length 20, 
A/N, O/O 
A/B/T52, F53 seq.#2, start 79, end 98, length 20, A/N, O/O 
Plan Account at the Trust, TPA, or 
Record Keeper 
Plan Account Number 
Indicator 
A/B/T50, A/B/T/F51 seq.#5, start 88, end 88, length 1, A/N, 
OC/OC 
A/B/T52, F53 seq.#2, start 99, end 99, length 1, A/N, 
OC/OC 
Required if Plan Account Number 
is provided 
 
1 = Trust 
2 = TPA 
3 = Record Keeper 
Fatca: Added New Values to Existing Fields 
Field Name Record Type and Location Added new values  
Withhold Indicator A/B/T50, A/B/T/F51 seq.#1, start 65, end 65, 
length 1, A/ N, R/O 
W8 indications 
H = W-8BEN-E on file/documentary evidence 
I = Voluntary FATCA withholding - W-8BEN-E on 
file/documentary evidence 
J = W8-IMY or W-8BEN-E  pending  
W8 Qualified 
[[intermediary]] 
Indicator 
A/B/T50, A/B/T/F51 seq.#10, start 82, end 82, 
length 1, A/ N, OC/OC 
9 = Territory Financial Institution 
 

---

## Page 96

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4, 2013 96 
Fatca: Added New Record/Fields   
Record/Field  
Name 
Record Type and Location Description  
A/B/T50, 
A/B/T/F51 
Sequence #37 
Account Conversion/Update (A/B/T50, A/B/T/F51) 
#37 
 Optional Record 
Chapter 4 Status 
Code 
A/B/T50, A/B/T/F51 seq.#37, start 10, end 11, 
length 2,  A/ N, O/O 
See List of values in the ‘Chapter 4 Status 
Codes’ document 
Global 
[[intermediary]] 
Identification 
Number 
A/B/T50, A/B/T/F51 seq.#37, start 12, end 36, 
length 25, A/N, O/O 
IRS issued number to identify and establish 
FATCA status of a Foreign Financial Institution 
(FFI) 
Underlying 
Client’s Foreign 
Tax [[ID]] 
A/B/T50, A/B/T/F51 seq.#37, start 37, end 61, 
length 25,  A/ N, O/O 
Foreign Tax [[ID]] of Underlying Client 
FATCA Override 
Special Rate 
A/B/T50, A/B/T/F51 seq.#37, start 62, end 66, 
length  5, N, O/O 
99.999 

---

## Page 97

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q1, 2013 97 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2013 
Added New Field to Existing Records 
New Field Name Record Type and Location Requirements  
Initiating Firm  A/B/T52, F53 seq.#3, start 86, end 89, length 4, 
A/N, O/OC 
Required for A/B/T52 if Transaction Type = 4 
(Mass [[Broker]] to [[Broker]] Conversion) 
Requirements Changed for Existing Field 
Field Name Record Type, Location, Current 
Requirements 
New Requirement and Description 
Network Control 
Indicator 
A/B/T52, F53 seq.#1, start 78, end 78, length 1, 
A/N, O/R 
For Record Type 52, must be spaces.  
Required for Record Type 53, must be 
Transfer In Account or 
Conversion/Maintenance Account. 
0 = Matrix Level 0  
3 = Matrix Level 3 
4 = matrix Level 4 
 
(Removed   1 = Level 1; 2 = Level 2 
effective Q1, 2013) 
Description also updated to ‘Matrix Level’ 

---

## Page 98

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of documentation changes – Q1, 2013 98 
SUMMARY OF DOCUMENTATION CHANGES – Q1, 2013 
Changes to Description of Existing Values 
Field Name Record Type, Location, 
Current Requirements 
Old  Description New  Description 
Withhold 
Indicator 
A/B/T50, A/B/T/F51 
seq.#1, start 65, end 65, 
length 1, A/ N, R/O 
W9 indications  
3 = Notification of Incorrect TIN 
From the Secretary Treasury 
 
6 = Notification to commence 
Backup Withholding from 
Secretary for under reporting 
Dividends 
9 = Withhold due b/c notice 
W9 indications  
3 = Notification of incorrect TIN from the 
Secretary of Treasury (Withhold due to B 
Notice) 
6 = Notification to commence Backup 
Withholding from Secretary of Treasury for 
underreporting [[Dividend]] and/or interest 
payments (Withhold due to C Notice) 
9 = Account(s) subject to both B and C 
Notice Withholding 
Changes to Description of Existing Field 
Field Name Record Type, Location, 
Current Requirements 
Old  Description New  Description 
Number of 
Beneficiaries 
and/or 
Successor 
Owner 
A/B/T50, A/B/T/F51 
seq.#4, start 80, end 81, 
length 2, N, OC/O 
Required for Section 529 Account 
(Account Type = 1) 
01-06. 
Required for Section 529 Account 
(Account Type = 1) 
If provided, valid values are 01-06.  
Zeroes are not allowed. 
Space means there are no 
Beneficiaries/and/or Successor. 

---

## Page 99

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of documentation changes – Q1, 2013 99 
Changes to Description of Existing Record 
Record  Name Current Description New Description 
ACCOUNT/CONVERSION 
/UPDATE  (A/B/T50, 
A/B/T/F51) #13 
Optional Conditional Record 
Input/output 
 
This record is required for Section 529 
Account (Account Type =1). 
• For Section 529 (Account Type = 1) at 
least one 529 Beneficiary 
(Beneficiary/Successor Owner Address 
[[Option]] = ‘C’) is required.  
• A Successor Owner 
(Beneficiary/Successor Owner Address 
[[Option]] = ‘D’) is required if    Successor 
Owner Indicator = 1 and Section 529 
(Account Type = 1) and not allowed 
otherwise.  
• Not more than one Successor Owner is 
allowed. 
• Beneficiary/Successor Owner Address 
[[Option]] = ‘C’ or ‘D’ are not allowed for 
Regular Account (Account Type = 0). 
• Sequences #13 through #16 are 
required if Number of Beneficiaries/ 
Successor Owner > 00. 
Optional Conditional Record 
Input/output 
 
This record is required for Section 529 Account 
(“Account Type” =1). 
• For Section 529 (“Account Type” = 1): 
Sequences #13 through #16 are required if 
‘Number of Beneficiaries/ Successor 
Owner” is 01 or greater.  
• At least one 529 Beneficiary 
(“Beneficiary/Successor Owner Address 
[[Option]]” = ‘C’) is required.  
• If the “Successor Owner Indicator”=1 
and “Account Type” = 1, the 
“Beneficiary/Successor Owner Address 
[[Option]]” must be populated with “D” (529 
Successor Owner).  Only one 529 
Successor Owner is allowed.  
 
• For Regular Account (“Account Type” = 
0):If Sequences #13 through #16 are 
provided, the “Number of Beneficiaries/ 
Successor Owner” field must be populated 
with a value of 01 or greater.  
• The “Beneficiary/Successor Owner 
Address [[Option]]” field must be populated 
with either   ‘A’ or B’.  No other values 
are allowed.  

---

## Page 100

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2012 100 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2012 
Requirements Changed for Existing Field 
Field Name Record Type, Location, Current 
Requirements 
New Requirement and Description 
Network Control 
Indicator 
A/B/T50, A/B/T/F51 seq.#1, start 21, end 21, 
length 1, A/N, R/R 
0 = Level 0  
3 = Level 3  
4 = Level 4  
 
(Removed 1 = Level 1;  2 = Level 2 ) 

---

## Page 101

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4 (December 5), 2011 101 
SUMMARY OF CHANGES – EFFECTIVE Q4 (DECEMBER 
5), 2011 
Added New Field to Existing Records 
New Field Name Record Type and Location Requirements  
Gift Indicator A/B/T52, F53 seq.#1, start 94, end 94, length 1, A/N, O/O Space = No  
1 = Yes 

---

## Page 102

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4 (October 17), 2011 102 
SUMMARY OF CHANGES – EFFECTIVE Q4 (OCTOBER 
17), 2011 
Added New Field to Existing Records 
New Field Name Record Type and Location Requirements  
Underlying Firm Symbol 
(UFS) 
A/B/T50, A/B/F/T51 seq.#5, start 64, end 67, 
length 4, A/N, O/O 
Number that identifies the Underlying Firm 
(Banks/Trusts/Record Keepers/ TPA’s) that clear 
through another entity 
Requirements Changed for Existing Field 
Field Name Record Type, Location, Current 
Requirements 
New Requirement and Description 
Beneficiary/ Successor 
Owner Relationship 
Indicator 
A/B/T50, A/B/T/F51 seq.#13, start 30, end 30, 
length 1, A/N,  OC/O 
A/B/T50, A/B/T/F51 seq.#17, start 30, end 30, 
length 1, A/N,  OC/O 
A/B/T50, A/B/T/F51 seq.#21, start 30, end 30, 
length 1, A/N,  OC/O 
A/B/T50, A/B/T/F51 seq.#25, start 30, end 30, 
length 1, A/N,  OC/O 
A/B/T50, A/B/T/F51 seq.#29, start 30, end 30, 
length 1, A/N,  OC/O 
A/B/T50, A/B/T/F51 seq.#33, start 30, end 30, 
length 1, A/N,  OC/O 
O/O  
1 = Spouse  
2 = Non-Relative 
3 = Grandchild  
4 = Relative  
5 = Child 
(Removed  - “Required if Beneficiary/Successor 
Owner Address [[Option]]  of ‘C’ is provided”) 
[[NSCC]] Control Number 
or Reference Number 
A/B/T52, F53 seq.#1, start 14, end 24, length 
11, A/N,  R/R 
For Record Type 52:  
Must be space on input; [[NSCC]] will create 
control number on output.  
For Record Type 53:  
Must be either [[NSCC]] Control Number when 
Transaction Type = 1, 2, 4, 5 (removed  ‘8’) 
or 
Firm Reference Number when Transaction Type 
= 3, 6 or 7. 
Transaction Type A/B/T52, F53 seq.#1, start 25, end 25, length 
1, A/N,  R/R 
(Removed  ‘8 = 529 Rollover ‘) 
Cost Basis Money 
Amount 
A/B/T52, F53 seq.#3, start 53, end 68, length 
16, N,  OC/OC 
O/O 
(Removed  ‘Required (but allowed to be zero)  if 
Transaction Type equals  8’) 
Earnings to Date 
Money Amount 
A/B/T52, F53 seq.#3, start 69, end 84, length 
16, N,  OC/OC 
O/O 

---

## Page 103

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4 (October 17), 2011 103 
Field Name Record Type, Location, Current 
Requirements 
New Requirement and Description 
(Removed  ‘Required (but allowed to be zero)  if 
Transaction Type equals  8’) 
Requirements Changed for Existing Records 
Record  Name Current Requirements New Requirements 
Transfer Detail/Fund 
Acknowledgment 
(A/B/T52, F53) #3 
This record is required when the 
Transaction Type (located on record 
sequence #1) equals 4 or 8.  Otherwise, it 
is optional. 
This record is required when the Transaction Type 
(located on record sequence #1) equals 4.    
Otherwise, it is optional. 

---

## Page 104

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q4 (August 8), 2011 104 
SUMMARY OF CHANGES – EFFECTIVE Q4 (AUGUST 8), 
2011 
Requirements Changed for Existing Field 
Field Name Record Type, Location, Current 
Requirements 
New Requirement and Description 
Agent for Firm Number Account Conversion/Update (A/B/T50, 
A/B/T/F51) #9, start 34, end 37, length 4, 
A/N, OC/OC 
O/O 
(Removed ‘Required when there is a new Firm [[ID]] 
# and System Code = B’) 
Agent for Firm Number Transfer Detail/Fund Acknowledgment 
(A/B/T52, F53) #2, start 38, end 41, length 
4, A/N, RC/RC 
O/O 
(Removed ‘Optional for Transaction Type  
6 or 7.’) 

---

## Page 105

Account Conversion/Update & Transfer/Acknowledgment Record Layouts 
Summary of changes – effective Q2, 2011 105 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2011 
Requirements Changed for Existing Field 
Field Name Record Type, Location, Current 
Requirements 
Changed values, requirements 
Cost Basis [[Option]] A/B/T50, A/B/T/F51 seq.#11, start 81, end 
81, length 1, A/N,  O/O 
0 = Unknown 
1 = FIFO (First In First Out) 
2 = LIFO (Last In First Out)  
3 = High Cost 
4 = Low Cost 
5 = Average Cost 
6 = Select Lot 
Added New Fields to Existing Records 
New Name Record Type and Location Requirements  
Credit Sub-Account  
Number 
A/B/T52, F53 seq.#4, start 46, end 65, 
length 20, A/N, O/O 
Underlying Credit Customer Account Number  
Debit Sub-Account  
Number 
A/B/T52, F53 seq.#4, start 66, end 85, 
length 20, A/N, O/O 
Underlying Debit Customer Account Number  
Requirements Changed for Existing Records 
Record  Name Current Requirements New Requirements 
Transfer Detail/Fund 
Acknowledgment 
(A/B/T52, F53) #4 
Record A/B/T52 sequence #4 is Optional. 
This record will not be allowed if Closing 
Balance (Debit Account) or Closing Balance 
(Credit Account) is provided in record A/B/T52 
sequence #2.   
Record F53 sequence #4 is Optional 
Conditional. This record will be required if 
Closing Balance (Debit Account) or Closing 
Balance (Credit Account) is NOT provided in 
record F53 sequence #2.  Otherwise, it is 
optional.  
Record A/B/T52 sequence #4 is Optional.  
 
Record F53 sequence #4 is Optional 
Conditional. This record will be required if 
Closing Balance (Debit Account) or Closing 
Balance (Credit Account) is NOT provided in 
record F53 sequence #2.  Otherwise, it is 
optional.  
 
 
 

---

## Page 106

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 9, 2023 
Publication Code: MFS326 
Service: Networking 
Title: Account Conversion/Update & Transfer/Acknowledgment Record Layouts  
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 