---
title: "Reject Codes for Networking & DTCC Payment aXis"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_rejectcodes_mfs196_20200915.pdf"
pages: 18
size: "365.3 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Reject Codes for Networking & DTCC Payment aXis

**Original File:** [net_rejectcodes_mfs196_20200915.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_rejectcodes_mfs196_20200915.pdf)  
**Category:** Other  
**Total Pages:** 18  
**File Size:** 365.3 KB  

---

## Page 1

 
 
 
NETWORKING 
REJECT CODES FOR NETWORKING & [[DTCC]] PAYMENT AXIS 
SEPTEMBER 15, 2020 
 


---

## Page 2

 
 
© 2020 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 15, 2020 
Publication Code: MFS196 
Service: Networking 
Title: Reject Codes for Networking & [[DTCC]] Payment aXis 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Networking Reject Codes .................................................................................................................................... 4 
Reject Codes Used by Funds to Reject [[Broker]] Initiated Networking Transactions ........................................... 9 
[[DTCC]] Payment aXis Invoicing and Fee [[settlement]] ........................................................................................ 17 
Reject Codes to be used by Funds to reject [[Broker]]-initiated Invoices for Fee Types = 50, 55, 56, 57 ............ 17 
Modification Codes to be used by Funds to Modify [[Broker]]-initiated Invoices for Fee Types = 55, 56, 57 ....... 17 
 

---

## Page 4

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 4 
NETWORKING REJECT CODES 
For transactions that [[DO]] not meet the required editing criteria, the following Networking reject codes are used 
by [[NSCC]].  In addition, these reject codes are also used by the [[DTCC]] Payment axis Service. 
  
Reject Code Description 
01 System Code missing/invalid 
02 Record Type missing/invalid 
03 Clearing Settling Firm Number missing/invalid                          
04 Clearing Settling Fund Number missing/invalid 
05 Fund [[CUSIP]] Number missing/invalid 
06 Balance Date missing/invalid 
07 Firm Identification Number missing 
08 Closing Balance missing/invalid 
09 LOI Escrow Field missing/invalid 
10 Share Balance Indicator missing/invalid 
11 Fund Alpha Code missing/invalid 
12 [[Broker]] Alpha Code missing/invalid 
13 Header Record missing/invalid 
14 Trailer Record missing/invalid 
15 Network Control Indicator missing/invalid 
16 [[Dividend]] Code missing/invalid or invalid for Matrix Level 
17 Fund Payout Cycle missing/invalid 
18 [[Dividend]] Distribution Type missing/invalid 
19 Record Date missing/invalid 
20 Reinvest Date missing/invalid 
21 Payable Date missing/invalid 
22 [[Dividend]] Rate missing/invalid 
23 Payable Line Indicator missing/invalid 
24 Posting Date missing/invalid 
25 [[Dividend]] Debit/Credit Indicator missing/invalid 

---

## Page 5

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 5 
Reject Code Description 
26 Accrual Starting Date missing/invalid 
27 Cash Div./Cap Gain Amount missing/invalid 
28 Fee Amount missing/invalid 
29 Fee Type missing/invalid 
30 Payment Date Non-Numeric 
31 Cash Disbursement Indicator missing/invalid 
32 Withholding Indicator missing/invalid 
33 Withholding Rate missing/invalid 
34 Withholding Amount missing/invalid 
35 Reinvest Price missing/invalid 
36 Reinvest [[shares]] missing/invalid 
37 Sequence Number missing/invalid 
38 Transaction Type missing/invalid 
39 Effective Date missing/invalid 
40 Share/Balance Amount missing/invalid 
41 Debit/Credit Indicator missing/invalid 
42 Dollar Amount Non-Numeric 
43 Buy/Sell Indicator invalid 
44 [[Margin]] Account Indicator missing/invalid 
45 Combined TEFRA/NRA Indicator missing/invalid 
46 Original Trade Date missing/invalid 
47 Price missing/invalid 
48 IRA Year missing/invalid 
49 Cross Reinvest [[CUSIP]] Number missing 
50 Description missing 
51 Sales Charge Rate invalid 
52 Commission Amount invalid 
53 Cash Disbursement Indicator missing/invalid 
54 Processing Date missing/invalid 

---

## Page 6

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 6 
Reject Code Description 
55 Payable Date Earlier than Record Date 
56 Sort Sequence invalid 
57 Network Control Indicator invalid for this Transaction Type 
58 Additional Input Required for this Input Type 
59 [[NSCC]] Control Number/Reference Number missing/invalid 
60 Fund Account Indicator missing/invalid 
61 Customer Account Number missing 
62 Book/Physical Share Indicator missing/invalid 
63 Payable Information Indicator missing/invalid 
64 SSN/EIN Number Indicator missing/invalid 
65 SSN/EIN Number missing 
66 Account Line Indicator missing/invalid 
67 NRA Tax is Non-Numeric 
68 Social Code missing/invalid 
69 Customer Account Number Indicator missing/invalid 
70 Account Name/Address missing 
71 PI Delivery Indicator missing/invalid 
72 Payable Account Number missing/invalid 
73 Payable Zip Code missing/invalid 
74 NAV Account Number missing/invalid 
75 Account Rep Number missing/invalid for Matrix Level 
76 Account Rep Name missing/invalid for Matrix Level 
77 Agent for Firm Number missing 
78 Branch Identification Number missing 
79 ACH Indicator missing/invalid 
80 Systematic Contribution Indicator (SIP/PAC/PIP) missing/invalid 
81 SWP Indicator missing/invalid 
82 Check Writing Privileges missing/invalid 
83 Payable Address Options missing/invalid 

---

## Page 7

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 7 
Reject Code Description 
84 ROA/LOI Value Non-Numeric 
85 LOI Number/Date Non-Numeric 
86 Related Trade Indicator invalid 
87 New [[Broker]] of Record invalid for Matrix Level 
88 Account Name/Address Line invalid for Matrix Level 
89 Payable Name/Address Line missing or invalid for Matrix Level 
90 Account Number Indicator missing/invalid 
91 Account Number missing 
92 Credit Account Number missing 
93 Transfer Type missing/invalid 
94 Fund Reject Code invalid 
95 Share Amount missing/invalid 
96 Transaction Code missing/invalid 
97 Closing Balance (Credit) missing/invalid 
98 Closing Balance (Debit) missing/invalid 
99 Multiple Error 
A0 Acknowledgment Info Does Not Match Original Transfer 
A1 State of Sale missing/invalid 
A2 Capital Gain Indicator missing/invalid 
A3 Fund’s Tax [[ID]] Number missing 
A4 Foreign Tax Credit invalid 
A5 Spill-Over Distribution Rate invalid 
A6 Reallocation Indicator missing/invalid 
A7 Spill-Over Distribution Indicator missing/invalid 
A8 Reallocation Percent missing/invalid 
A9 Ex-Date missing/invalid 
B0 Accrual Date missing/invalid 
B1 Accrual Rate missing/invalid 
B2 LOI/ROA Indicator missing/invalid 

---

## Page 8

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 8 
Reject Code Description 
B3 Alternate [[Dividend]] Payee Address Indicator missing/invalid 
B4 Commission Type missing/invalid 
B5 Debit Reason Code missing/invalid 
B6 [[settlement]] Indicator missing/invalid 
B7 Name Indicator missing/invalid 
B8 Name missing 
B9 Commission Rate missing/invalid 
C0 Credit Sub-Account Number is missing               
C1 Gross Amount of Trade/Total Security Assets missing/invalid 
C2 Share Quantity missing/invalid 
C3 Trade Date missing/invalid 
C4 Initial/Subsequent Indicator missing/invalid 
C5 From Branch Number missing 
C6 To Branch Number missing 
C7 Branch Address Line missing 
C8 From A/E Number missing 
C9 To A/E Name missing 
D0 Debit Sub-Account Number is missing                                        
D1 To A/E Number missing 
D2 From A/E Name missing 
D3 Original Control Number missing/invalid 
D4 Original Control Number Correction Indicator missing/invalid 
D5 Purged Account Indicator missing/invalid 
D6 Payable [[Option]] Delete Indicator missing/invalid 
D7 Payable Address Delete [[Option]] Indicator missing/invalid 
D8 Dollar Amount missing/invalid 
D9 ACATS Control Number is missing/invalid                                 
E0 Payable Account Number Indicator missing/invalid 
E1 ABA Routing Number missing 

---

## Page 9

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 9 
Reject Code Description 
E2 CDSC Payment Code missing/invalid 
E3 Disbursement [[Option]] missing/invalid 
E4 Disbursement Amount missing/invalid 
E5 Monthly Payment Indicator missing/invalid 
E6 Payment Date Indicator missing/invalid 
E7 Retirement Tax Indicator missing/invalid 
E8 Shareholder Bank Account Type missing/invalid 
E9 First Check Date invalid 
F0 Cost Basis [[Option]] invalid 
F1 Payable Security Issue [[ID]] missing 
F2 Alternate Payable Indicator missing/invalid 
F3 Alternate Payable Reason missing/invalid 
F4 Receiving Firm Clearing/Settling Number Missing/Invalid                  
F5 Physical Share Amount missing/invalid 
F6 Payable Security Issue Country Code missing/invalid 
F7 Payable Security Issue Check Digit missing/invalid 
F8 Wrap Account Indicator missing/invalid 
F9 Membership Identifier invalid                                                       
Reject Codes Used by Funds to Reject [[Broker]] Initiated Networking 
Transactions 
Funds may also assign an [[NSCC]] reject code in rejecting a transaction. 
Reject Code Description  
FA Matrix Level Does Not Match "Transfer to" Account 
FB Invalid [[Broker]] Identification Number 
FC Invalid Fund Account Number 
FD Debit Account Restricted 
FE Invalid Credit Account Number 

---

## Page 10

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 10 
Reject Code Description  
FF Credit Account Restricted 
FG Transaction invalid for this Matrix Level 
FH Invalid Book/Physical Indicator 
FI Invalid Share Amount 
FJ Insufficient Debit Account Balance 
FK Debit Account Not Networked 
FL Maintenance Request Identical to Account Information File 
FM Invalid Account Transfer 
FN Closed Account 
FO Invalid [[Broker]] of Record 
FP Invalid Executing [[Broker]] Number 
FQ Insufficient [[shares]] Available Due to [[shares]] Held in Escrow 
FR Prototype Retirement Account NOT Eligible for Networking 
FS Branch NOT on File at Fund 
FT Dealer NOT on Networking Matrix Level Indicated 
FU Duplicate Client Account 
FV Unassigned 
FW 529 Crossover Account                                                                     
End of Networking reject codes used by Funds 
G0 Trust/TPA /Investment Agent Number missing/invalid 
G1 Currency Indicator missing/invalid 
G2 W8 Certification Date missing/invalid 
G3 W8 Expiration Date missing/invalid 
G4 W8 Override NRA Special Rate missing/invalid 
G5 W8 Qualified [[intermediary]] Indicator missing/invalid 
G6 Country of Origin/W8 Override Country Code missing/invalid 
G7 [[settlement]] Date missing/invalid 
G8 Total Records/Items missing/invalid 
G9 Delivering Firm Share Aging Indicator invalid 

---

## Page 11

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 11 
Reject Code Description  
N/A H0 - Beneficiary/Successor Owner Zip Code missing for Section 529 Account                                                    
(Eliminated effective Q4, 2020)      
N/A H1 - Beneficiary/Successor Owner City or/and State missing for Section 529 Account  
(Eliminated effective Q4, 2020) 
H2 Change in [[Broker]]/Dealer Indicator invalid 
H3 Transfer Disbursement [[Option]] – Accruals invalid  
H4 Accrual Money Amount invalid  
H5 All or None Indicator invalid  
H6 Accrual Indicator missing/ invalid                                              
H7 Accrual Money Amount /Accrual Money Account Balance missing/invalid  
H8 Load Type Indicator missing/invalid 
H9 Assets Eligible for Trails invalid 
I0 Firm/Fund Identification Number missing 
I1 Firm/Fund Identification Indicator missing/invalid 
I2 Delivering Firm Number missing/invalid 
I3 [[default]] Lot Indicator missing/invalid 
I4 12b-1 Indicator missing/invalid 
I5 12b-1 Lot Date missing/invalid 
I6 Short Term Redemption Lot Date missing/invalid 
I7 Jumbo Transaction Indicator invalid 
I8 Commissionable Share Indicator is missing/invalid                      
I9 Scrub Indicator invalid 
J0 Fund Account Response Indicator invalid 
J1 RPO Indicator invalid 
J2 Spillover [[Dividend]] Indicator invalid 
J3 Target Date Fund Indicator is Invalid 
J4 Account Type is missing/Invalid 
J5 Account City or/and Account State missing for Section 529 Account 
J6 Cost Basis Money Amount missing/invalid 
J7 Earnings to Date Money Amount missing/invalid 
J8 Negative Earnings to Date Indicator invalid 

---

## Page 12

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 12 
Reject Code Description  
J9 Customer Zip Code missing  
K0 Population of both Share Balance and Share Balance Extended fields is not allowed 
K1 Population of both Closing Balance and Closing Balance Extended fields is not allowed 
K2 Date field has invalid date format 
K3 Account / Owner U.S. Citizenship Indicator is missing/invalid 
K4 Owner Date of Birth is invalid                              (Description modified effective Q4, 2020) 
K5 Age Based Indicator is invalid 
K6 Age Based Roll Exempt Indicator is invalid 
K7 Account /Owner US Resident Alien Indicator is invalid 
K8 Number of Beneficiaries/Successor Owners/Additional Account Owner is missing/invalid   
 
K9 Successor Owner Indicator is invalid              (Description modified effective Q4, 2020) 
L0 Beneficiary/Successor Owner/Additional Account Owner Address [[Option]] is missing/invalid         
L1 Beneficiary/Successor Owner/Additional Account Owner Date of Birth is missing/invalid 
L2 Beneficiary/Successor Owner/ Additional Account Owner U.S. Citizenship Indicator is 
missing/invalid  
L3 Beneficiary/Successor Owner/ Additional Account Owner SSN/EIN Number is missing  
L4 Beneficiary/Successor Owner/Additional Account Owner SSN/EIN Indicator is 
missing/invalid  
L5 Beneficiary/Successor Owner/Additional Account Owner Relationship Indicator is invalid  
L6 Beneficiary/Successor Owner/ Additional Account Owner Name End Line Indicator is 
missing/invalid  
L7 Date of Event has invalid date format 
L8 529 Transfer Reason Code is invalid 
L9 IRS 529 Annual Strategy Change Counter is invalid 
M0 Beneficiary/ Successor Owner/ Additional Account Owner Name/Address Line #1 is missing   
M1 Successor Owner information already provided   
M2 Beneficiary information is missing 
M3 Beneficiary/Successor Owner/Additional Account Owner information does not correspond to 
Number of Bene/Succ/Additional Account Owners  
M4 Successor Owner information is missing   
M5 Group of Sequence Records for Beneficiary/Successor Owner/Additional Account Owner is 
omitted  

---

## Page 13

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 13 
Reject Code Description  
M6 Detail Record is missing/invalid                                                                                            
M7 529 Aggregator Number is missing/invalid                                   
M8 Original Control Number Indicator is missing/invalid                 
M9 Control/Reference Number Indicator is missing/invalid                 
N0 Opposing Clearing/Settling Firm Number is missing/invalid                                                     
N1 Opposing Network Control Indicator is missing/invalid              
N2 Omnibus Account Indicator is invalid                                                          
N3 Opposing Fund Account Number is missing                                              
N4 Gift Indicator is invalid                                                                                  
N5 Structure of records/sequences is incorrect for provided fee type    
N6 Omnibus Account Number is missing                                            
N7 Period Start Date is missing/invalid                                                 
N8 Period End Date is missing/invalid                                                   
N9 Anticipated [[settlement]] Date is invalid                                              
O0 Invoiced / [[settlement]] Amount is missing/invalid                             
O1 Underlying BIN is missing                                                                           
O2 Rate is missing/invalid/duplicate                                                                
O3 Sub-Accounting Eligible Assets is missing/invalid               
O4 Sub-Accounting Ineligible Assets is missing/invalid        
O5 Sub-Accounting Excluded Assets is missing/invalid         
O6 Sub-Accounting Balance is missing/invalid                       
O7 Process Date of Trade is missing/invalid                                                 
O8 Sub–Account Transaction Amount is missing/invalid                           
O9 Sub-Account Trade Control Number is missing/invalid                            
P0 [[Asset]] Calculation Method is missing/invalid                                              
P1 Deliverer Reject Indicator is missing/invalid                                                
P2 Deliverer Reject Code is invalid                                                                   
P3 Invoice Initiator is Missing/Invalid    
P4 [[Asset]] Type is Invalid                                    

---

## Page 14

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 14 
Reject Code Description  
P5 Fund Account Number is Missing                                               
P6 Underlying Customer Type is Invalid                                              
P7 Number of Rates in Details does not correspond to Number of Rates in a Header                                                                                                                                                                                           
P8 Deliverer Reject code is missing on Rejected Invoice                               
P9 Omni Invoice Summary Record is missing/invalid                                    
Q0 Control Number is missing                                                                         
Q1 Confirm/Reject Code Indicator is missing/invalid                                     
Q2 Number of Rates is missing/invalid                                                            
Q3 Submitting [[participant]] is not eligible for this service                                
Q4 Plan TAX [[ID]] or EIN missing/invalid 
Q5 DOL Plan Code Number missing 
Q6 Redemption Fee Rate is Missing/Invalid  
Q7 Redemption Fee Money Amount is Missing/Invalid  
Q8 Account Open Date is missing/invalid  
Q9 Plan [[Fiduciary]] State missing/invalid 
R0 Security Issue [[ID]] Indicator is missing/invalid  
R1 Record Keeper Name missing 
R2 Program Name missing 
R3 Product Provider missing 
R4 Plan Type missing/invalid 
R5 Plan Status missing/invalid 
R6 Plan Status Date missing/invalid 
R7 Overall Plan Assets missing 
R8 Number of Security Issue [[ID]]’s in the Plan missing 
R9 Total [[participant]] in Plan missing/invalid 
S0 ERISA Flag missing/invalid 
S1 Contribution Amount for Plan missing/invalid 
S2 Distribution Amount for Plan missing/invalid 
S3 Plan Sponsor Address Line #1 missing 

---

## Page 15

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 15 
Reject Code Description  
S4 Plan Sponsor City missing 
S5 Plan Sponsor State missing/invalid 
S6 Plan Sponsor Zip missing/invalid 
S7 Secondary Plan [[Fiduciary]] Name missing/invalid 
S8 Secondary Plan [[Fiduciary]] Address Line #1 missing 
S9 Secondary Plan [[Fiduciary]] City missing/invalid 
T0 Secondary Plan [[Fiduciary]] State missing/invalid 
T1 Secondary Plan [[Fiduciary]] Zip missing/invalid 
T2 Product Investment Type missing/invalid 
T3 Define Product Investment type missing 
T4 QDIA missing/invalid 
T5 Participants in Security Issue [[ID]] missing/invalid 
T6 [[shares]] in Security Issue [[ID]] missing/invalid 
T7 Month End Assets for Security Issue [[ID]] missing/invalid 
T8 Total Security Issue [[ID]]’s missing/invalid 
T9 Clearing/Settling Firm Number (Deliverer Number) not affiliated with TPA 
U0 Initiating Firm missing/invalid 
U1 Plan [[ID]] Number missing 
U2 Avg. Daily Assets for Security Issue [[ID]] invalid 
U3 Opposing Membership Identifier is missing/invalid                          
U4 Opposing Originating/Underlying Firm Number is invalid               
U5 Originating/Underlying Firm Number is invalid                                 
U6 Record Date [[shares]] is missing/invalid                                               
U7 Plan Account Number Indicator is missing/invalid                            
U8 Chapter 4 Status Code is invalid                                                          
U9 FATCA Override Special Rate is invalid                                                
V0 FATCA Withholding Indicator is Missing/Invalid                                       
V1 FATCA Withholding Rate is Missing/Invalid                                          
V2 FATCA Withholding Amount is Missing/Invalid                                     

---

## Page 16

Reject Codes For Networking & [[DTCC]] Payment aXis 
Networking Reject Codes 16 
Reject Code Description  
V3 Modification Indicator is Missing/Invalid                                               
V4 Modification Reason Code is Missing/Invalid                                                                   
V5 Detail Record [[ID]] is Missing/Invalid                                                       
V6 Eligible [[participant]] Count is Missing/Invalid                                        
V7 Ineligible [[participant]] Count is Invalid                                                    
V8 Rate Type is Missing/Invalid                                                              
V9 Rate Category is Missing/Invalid                                                            
W0 Invalid Confirm/Reject and Deliverer Reject Indicator Combination   
W1 Number of Eligible Positions is Missing/Invalid                                     
W2 Number of Ineligible Positions is Invalid                                                
W3 Eligible Assets Missing/Invalid                                                                
W4 Ineligible Assets Missing/Invalid                                                              
W5 Detail Summary Record [[ID]] is Missing/Invalid                                         
W6 Invalid Confirm/Reject and Modification Indicator Combination          
W7 Invalid Confirm/Reject and [[settlement]] Indicator Combination             
W8 Contribution Amount Credit/Debit Indicator is Invalid  
W9 Distribution Amount Credit/Debit Indicator is Invalid  
X0 SWIP Indicator is Invalid  
X1 Systematic Trade Changed From (old) Amount is Missing/Invalid  
X2 Systematic Trade Changed To (new) Amount is Missing/Invalid  
X3 Systematic Trade Changed From (old) Frequency is Missing/Invalid  
X4 Systematic Trade Changed To (new) Frequency is Missing/Invalid 
X5 Returned Payment Reason Code is Missing/Invalid 
X6 Customer Account Indicator 2 is Missing/Invalid  
X7 Customer Account 2 is Missing  
X8 [[participant]] is not valid for the Submitter and/or Product  
 
 

---

## Page 17

Reject Codes For Networking & [[DTCC]] Payment aXis 
[[DTCC]] Payment aXis Invoicing and Fee [[settlement]] 17 
[[DTCC]] PAYMENT aXis INVOICING AND FEE [[settlement]] 
Reject Codes to be used by Funds to reject [[Broker]]-initiated Invoices for Fee 
Types = 50, 55, 56, 57  
 
Reject Code Description 
[[OA]] Duplicate Invoice 
OB Invalid Rate 
OC [[Asset]] Value Invalid 
OD [[Asset]] Calculation Method Invalid 
OE Ineligible [[CUSIP]] 
OF Unauthorized Firm Invoice 
OG Incorrect Period 
OH Invalid Omnibus Account Number 
OI Invalid Debit/Credit Indicator 
 
Modification Codes to be used by Funds to Modify [[Broker]]-initiated Invoices for 
Fee Types = 55, 56, 57  
 
Reject Code Description 
MA Invalid Rate 
MB [[Asset]] Value Invalid 
MC [[Asset]] Calculation Method Invalid 
MD Incorrect Period 
ME Invalid Debit/Credit Indicator 
MF Incorrect Calculation 
MG Incorrect Payee 
MH Incorrect Positions 
 
 

---

## Page 18

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 