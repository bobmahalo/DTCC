---
title: "UTC Input Test Case Scenarios"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc114_input_test_case_scenarios_2022Jul25.pdf"
pages: 13
size: "351.6 KB"
category: "UTC"
ingested_on: "2026-06-05"
---

# UTC Input Test Case Scenarios

**Original File:** [utc114_input_test_case_scenarios_2022Jul25.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc114_input_test_case_scenarios_2022Jul25.pdf)  
**Category:** UTC  
**Total Pages:** 13  
**File Size:** 351.6 KB  

---

## Page 1

 
UNIVERSAL TRADE CAPTURE (UTC) 
UTC INPUT TEST CASE SCENARIOS 
JULY 25, 2022 
 


---

## Page 2

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios  2 
UTC INPUT TEST CASE SCENARIOS 
Notes: 
• Submit all test cases that apply to your firm. Any test cases that [[DO]] not apply to your submission may be excluded. 
• All orders should be entered as Buys, unless otherwise noted (See test cases C65 and C66). 
• For more information about market codes and other UTC fields and values, see the UTC Common Trade FIX Input Format document available in the UTC 
Technical Resources section of the Learning Center. 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C1 Tag 30 (Market) Valid buy-side trade is submitted with all required fields for the following 
exchange type: 
MARKET CODE 
Trade is successfully 
processed. 
C2 Tag 81 (Step In – Step Out Indicator) Valid buy-side trade is submitted with all required fields for the following 
exchange type: 
2 = StepIn 
Trade is successfully 
processed. 
C3 Tag 81 (Step In – Step Out Indicator) Valid buy-side trade is submitted with all required fields for the following 
exchange type: 
3 = StepOut 
Trade is successfully 
processed. 
C4 Tag 487 (Reversal / Correction(Trade 
Report Trans Type) Indicator) 
Valid buy-side trade is submitted with all required fields for the following 
Reversal / Correction (Trade Report Trans Type) indicator: 
2 = Replace 
Trade is successfully 
processed. 
C5 Tag 487 (Reversal / Correction(Trade 
Report Trans Type) Indicator) 
Valid buy-side trade is submitted with all required fields for the following 
Reversal / Correction (Trade Report Trans Type) indicator: 
4 = Reverse 
Trade is successfully 
processed. 
C6 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
A = Agency single order 
Trade is successfully 
processed. 

---

## Page 3

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios  3 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C7 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
B = Short exempt transaction(refer to A type) 
Trade is successfully 
processed. 
C8 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
C = Program Order, non-index arbitrage, for [[Member]] 
firm/organization 
Trade is successfully 
processed. 
C9 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
D = Program Order, index arbitrage, for [[Member]] firm/organization 
Trade is successfully 
processed. 
C10 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
E = Registered [[Equity]] [[Market Maker]] trades 
Trade is successfully 
processed. 
C11 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
F = Short exempt transaction (refer to W type) 
Trade is successfully 
processed. 
C12 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
H = Short exempt transaction (refer to I type) 
Trade is successfully 
processed. 
C13 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
I = Individual [[investor]] single order 
Trade is successfully 
processed. 
C14 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
J = Program Order, index arbitrage, for Individual Customer 
Trade is successfully 
processed. 
C15 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
K = Program Order, non-index arbitrage, For individual customer 
 
Trade is successfully 
processed. 

---

## Page 4

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios  4 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C16 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
L = Short exempt transaction for [[Member]] competing market- maker 
affiliated with the firm clearing the trade (refer to P and O types) 
Trade is successfully 
processed. 
C17 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
M = Program Order, index arbitrage, for other [[Member]]. 
Trade is successfully 
processed. 
C18 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
N = Program Order, non-index arbitrage, agent for other [[Member]] 
Trade is successfully 
processed. 
C19 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
O = Competing dealer trades 
Trade is successfully 
processed. 
C20 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
P = Principal 
Trade is successfully 
processed. 
C21 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
Q = OCS Correction 
Trade is successfully 
processed. 
C22 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
R = Competing dealer trades 
Trade is successfully 
processed. 
C23 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
S = Specialist trades 
Trade is successfully 
processed. 
C24 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
U = Program Order, index arbitrage, for other agency 
Trade is successfully 
processed. 

---

## Page 5

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios  5 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C25 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
W = All other orders as agent for other [[Member]] 
Trade is successfully 
processed. 
C26 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
X = Short exempt transaction for [[Member]] competing market- maker 
not affiliated with the firm clearing the trade (refer to W and T types) 
Trade is successfully 
processed. 
C27 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
Y = Program Order, non-index arbitrage, for other agency 
Trade is successfully 
processed. 
C28 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
Z = Program Order, non-index arbitrage, for other agency. 
Trade is successfully 
processed. 
C29 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[OTC]]: 
A = Agency 
Trade is successfully 
processed. 
C30 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[OTC]]: 
F = Firm 
Trade is successfully 
processed. 
C31 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[OTC]]: 
P = Principal 
Trade is successfully 
processed. 
C32 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[OTC]]: 
R = Riskless Principal 
Trade is successfully 
processed. 
C33 TAG 581 (Sell House Client Indicator) Buy-side trade is submitted with all required fields and the following Sell 
House Client Indicator: 
1 = AccountCustomer 
Trade is successfully 
processed. 

---

## Page 6

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios  6 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C34 TAG 581 (Sell House Client Indicator) Buy-side trade is submitted with all required fields and the following Sell 
House Client Indicator: 
3 = HouseTrader 
Trade is successfully 
processed. 
C35 TAG 581 (Sell House Client Indicator) Buy-side trade is submitted with all required fields and the following Sell 
House Client Indicator: 
4 = MarketMaker 
Trade is successfully 
processed. 
C36 TAG 460 (Security Type) Buy-side trade is submitted with all required fields and the following 
Security Type (Product) : 
15 = Call 
Trade is successfully 
processed. 
C37 TAG 460 (Security Type) Buy-side trade is submitted with all required fields and the following 
Security Type (Product) : 
17 = Futures 
Trade is successfully 
processed. 
C38 TAG 63 ([[settlement]] Type) Buy-side trade is submitted with all required fields and the following 
[[settlement]] Type: 
0 = Regular 
Trade is successfully 
processed. 
C39 TAG 63 ([[settlement]] Type) Buy-side trade is submitted with all required fields and the following 
[[settlement]] Type: 
1 = Cash 
Trade is successfully 
processed. 
C40 TAG 63 ([[settlement]] Type) Buy-side trade is submitted with all required fields and the following 
[[settlement]] Type: 
2 = Next Day 
Trade is successfully 
processed. 
C41 TAG 63 ([[settlement]] Type) Buy-side trade is submitted with all required fields and the following 
[[settlement]] Type: 
6 = [[Seller]]’s [[Option]] (Future) 
Trade is successfully 
processed. 
C42 TAG 63 ([[settlement]] Type) Buy-side trade is submitted with all required fields and the following 
[[settlement]] Type: 
7 = When Issued 
 
Trade is successfully 
processed. 

---

## Page 7

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios  7 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C43 TAG 577 (Special Trade indicator) Buy-side trade is submitted with all required fields and the following 
Special Trade Indicator (Clearing Instruction): 
0 = Process Normally 
Trade is successfully 
processed. 
C44 TAG 577 (Special Trade indicator) Buy-side trade is submitted with all required fields and the following 
Special Trade Indicator (Clearing Instruction): 
4 = Special Trade 
Trade is successfully 
processed. 
C45 TAG 58 (Don’t Count Indicator ([[SEC]] 31 
Fees)) 
Buy-side trade is submitted with all required fields and the following Don’t 
Count Indicator ([[SEC]] 31 Fees): 
D = Don’t Count 
Note:  
If a submitting exchange would like a transaction to be counted for Section 
31 processing, it should not include tag #58 in its FIX or MQ submission. 
[[NSCC]] counts Section 31 fees on transactions where this field/tag is not 
provided. Submitting entities that [[DO]] not want a transaction counted for 
Section 31 fees should specify a valid value (D or P) in tag #58. 
Trade is successfully 
processed. 
C46 TAG 58 (Don’t Count Indicator ([[SEC]] 31 
Fees)) 
Buy-side trade is submitted with all required fields and the following Don’t 
Count Indicator ([[SEC]] 31 Fees): 
P = Don’t Count; [[participant]] pays 
Note:  
If a submitting exchange would like a transaction to be counted for Section 
31 processing, it should not include tag #58 in its FIX or MQ submission. 
[[NSCC]] counts Section 31 fees on transactions where this field/tag is not 
provided. Submitting entities that [[DO]] not want a transaction counted for 
Section 31 fees should specify a valid value (D or P) in tag #58. 
Trade is successfully 
processed. 
C47 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted (For [[NYSE]] Execution) with all required fields 
and the following [[Liquidity]] Indicator: 
1 = Taker 
Trade is successfully 
processed. 
C48 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted (For [[NYSE]] Execution) with all required fields 
and the following [[Liquidity]] Indicator: 
2 = Provider 
Trade is successfully 
processed. 

---

## Page 8

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios  8 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C49 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted (For [[NYSE]] Execution) with all required fields 
and the following [[Liquidity]] Indicator: 
3 = Blended 
Trade is successfully 
processed. 
C50 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted (For [[NYSE]] Execution) with all required fields 
and the following [[Liquidity]] Indicator: 
4 = Opening/Prior Day Order 
Trade is successfully 
processed. 
C51 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted (For [[NYSE]] Execution) with all required fields 
and the following [[Liquidity]] Indicator: 
5 = Opening 
Trade is successfully 
processed. 
C52 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted (For [[NYSE]] Execution) with all required fields 
and the following [[Liquidity]] Indicator: 
6 = Closing 
Trade is successfully 
processed. 
C53 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted (For [[NYSE]] Execution) with all required fields 
and the following [[Liquidity]] Indicator: 
7 = Closing/MOC/LOC Order 
Trade is successfully 
processed. 
C54 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted (For [[NYSE]] Execution) with all required fields 
and the following [[Liquidity]] Indicator: 
8 = Specialist 
Trade is successfully 
processed. 
C55 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted (For [[NYSE]] Execution) with all required fields 
and the following [[Liquidity]] Indicator: 
F = 3rd Party Algo @ [[NYSE]] 
Trade is successfully 
processed. 
C56 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted (For [[NYSE]] Execution) with all required fields 
and the following [[Liquidity]] Indicator: 
G = 3rd Party Algo Away 
Trade is successfully 
processed. 
C57 TAG 825 (Buy [[Liquidity]] Indicator) Buy-side trade is submitted for Non-[[NYSE]] Market Centers with all 
required fields and the following Market Center Value Indicator: 
MARKET CODE 
 
Trade is successfully 
processed. 

---

## Page 9

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios  9 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C58 TAG 453 (NoPartyIDs Indicator) AND 
TAGs 452 and 448 (Party Role Indicators) 
Buy-side trade is submitted for all required fields and the following 
NoPartyIDs: 9 Party Role Indicators: 
• 448 (Clearing [[Broker]]), 452 (Party Role) = 4 
• 448 (Clearing [[Broker]]), 452 (Party Role) = 18 
• 448 (Entering/Executing [[Broker]]), 452 (Party Role) = 1 
• 448 (Contra Entering/Executing [[Broker]]), 452 (Party Role) = 37 
• 448 (Introducing [[Broker]]), 452 (Party Role) = 06 
• 448 (Contra Introducing [[Broker]]), 452 (Party Role) = 17 
• 448 (Badge [[ID]]), 452 (Party Role) = 11 
• 448 (Contra Badge [[ID]]), 452 (Party Role) = 12 
• 448 (Submitted by [[participant]]), 452 (Party Role) = 36 
Trade is successfully 
processed. 
C59 TAG 453 (NoPartyIDs Indicator) AND 
TAGs 452 and 448 (Party Role Indicators) 
Buy-side trade is submitted for all required fields and the following 
NoPartyIDs: 4 Party Role Indicators: 
• 448 (Clearing [[Broker]]), 452 (Party Role) = 4 
• 448 (Clearing [[Broker]]), 452 (Party Role) = 18 
• 448 (Entering/Executing [[Broker]]), 452 (Party Role) = 1 
• 448 (Contra Entering/Executing [[Broker]]), 452 (Party Role) = 37 
Trade is successfully 
processed. 
C60 TAG 453 (NoPartyIDs Indicator) AND 
TAGs 452 and 448 (Party Role Indicators) 
Buy-side trade is submitted for all required fields and the following 
NoPartyIDs: 2 Party Role Indicators: 
• 448 (Clearing [[Broker]]), 452 (Party Role) = 4 
• 448 (Clearing [[Broker]]), 452 (Party Role) = 18 
Trade is successfully 
processed. 
C61 TAG 136 (NoMiscFees) AND TAG 137 
and 
139 (Fee Types) 
Buy-side trade is submitted for all required fields with NoMiscFees 
Indicator: 4 NoMiscFees Indicators: 
• 137 (Commission/Explicit Fee), 139 (Fee Type) = 10 
• 137 (Other Fees), 139 (Fee Type) = 1 
• 137 (Taxes), 139 (Fee Type) = 2 
• 137 (Accrued Interest), 139 (Fee Type) = 7 
Trade is successfully 
processed. 
C62 TAG 570 (Previously Reported) Buy-side trade is submitted for all required fields with Previously Reported 
Indicator:  
N = No 
 
Trade is successfully 
processed. 

---

## Page 10

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios  10 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C63 TAG 570 (Previously Reported) Buy-side trade is submitted for all required fields with Previously Reported 
Indicator:  
Y = Yes 
Trade is successfully 
processed. 
C64 TAG 54 (Side Indicator) Buy-side trade is submitted for all required fields with Side Indicator:  
1 = Buy 
Trade is successfully 
processed. 
C65 TAG 54 (Side Indicator) Sell Trade is submitted for all required fields with Side Indicator: 
2 = Sell 
Trade is successfully 
processed. 
C66 TAG 54 (Side Indicator) Sell Short Trade is submitted for all required fields with Side Indicator: 
5 = Sell short 
Trade is successfully 
processed. 
C67 TAG 9426 (Displayed [[Liquidity]] Indicator) Buy-side trade is submitted for all required fields with the following 
Displayed [[Liquidity]] Indicator:  
0 = 0 round lots 
Trade is successfully 
processed. 
C68 TAG 9426 (Displayed [[Liquidity]] Indicator) Buy-side trade is submitted for all required fields with the following 
Displayed [[Liquidity]] Indicator: 
1 = Greater than 0 and less than 1 round lot. 
Trade is successfully 
processed. 
C69 TAG 9426 (Displayed [[Liquidity]] Indicator) Buy-side trade is submitted for all required fields with the following 
Displayed [[Liquidity]] Indicator:  
2 = From 1 to less than 20 round lots. 
Trade is successfully 
processed. 
C70 TAG 9426 (Displayed [[Liquidity]] Indicator) Buy-side trade is submitted for all required fields with the following 
Displayed [[Liquidity]] Indicator:  
3 = From 20 to less than 50 round lots. 
Trade is successfully 
processed. 
C71 TAG 9426 (Displayed [[Liquidity]] Indicator) Buy-side trade is submitted for all required fields with the following 
Displayed [[Liquidity]] Indicator:  
4 = 50 round lots and up. 
Trade is successfully 
processed. 
C72 TAG 578 Source of transaction/market 
system.  
(Trade Input Source) 
 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[NYSE]]/[[NYSE]](AMEX):  
O =OCS 
Trade is successfully 
processed. 

---

## Page 11

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios  11 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C73 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[NYSE]]/[[NYSE]](AMEX):  
P =PTP 
Trade is successfully 
processed. 
C74 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[NYSE]]/[[NYSE]](AMEX):  
S =Step Out 
Trade is successfully 
processed. 
C75 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[NYSE]]/[[NYSE]](AMEX):  
F = Force([[Broker]] or DMM) 
Trade is successfully 
processed. 
C76 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[NYSE]] 2:  
NB = [[NYSE]] [[Bonds]] 
Trade is successfully 
processed. 
C77 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[NYSE]] 2:  
BT = [[NYSE]] Blocked 
Trade is successfully 
processed. 
C78 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[NYSE]] 2: 
MP = [[NYSE]] Match Point 
Trade is successfully 
processed. 
C79 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[OTC]]:  
Q = QSR/ECN 
Trade is successfully 
processed. 
C80 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[OTC]]:  
A = TRF 
Trade is successfully 
processed. 
C81 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[OTC]]:  
D = Port 
Trade is successfully 
processed. 

---

## Page 12

UTC Input Test Case Scenarios 
UTC Input Test Case Scenarios 12 
Case 
[[ID]] 
Field Being Tested Description Expected Results 
C82 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[OTC]]:  
E = EACT 
Trade is successfully 
processed. 
C83 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for [[OTC]]:  
AD = Alt Display Facility 
Trade is successfully 
processed. 
C84 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the 
following Trade Input Source for CORR:  
P = Position Transfer 
Trade is successfully 
processed. 
C85 TAG 578 Source of transaction/market 
system. 
(Trade Input Source) 
Buy-side trade is submitted for all required fields with the following Trade 
Input Source for CORR:  
M = Internal Position Movement 
Trade is successfully 
processed. 
C86 Exchange submitter submits valid buy-side 
trade. T+1 
Buy-side trade is submitted for all required fields with the following dates: 
• Process Date- current
• Trade Date- current
• [[settlement]] Date- T+1
Trade is successfully 
processed. 
C87 Exchange submitter submits valid buy-side 
trade. T+2 
Buy-side trade is submitted for all required fields with the following dates: 
• Process Date - current
• Trade Date - current
• [[settlement]] Date - T+2
Trade is successfully 
processed. 
C88 TAG 528 (Buy order capacity) Buy-side trade is submitted with all required fields and the following Buy 
order capacity for [[NYSE]]: 
T = Competing dealer trades 
Trade is successfully 
processed. 
C89 Repeat test case C90 Repeat test case C90, using the exact information input in C90, including 
the trade sequence number. 
T rade rejects as a duplicate. 
C90 TAG 75 (Trade Date) [[DO]] not provide on input. Trade should reject, with an 
[[NSCC]] Reject Code (FIX tag 
751) of 2.

---

## Page 13

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself 
does not provide such services.  Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: July 25, 2022 
Publication Code: UTC114 
Service: Universal Trade Capture (UTC) 
Title: UTC Input Test Case Scenarios 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 