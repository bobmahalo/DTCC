---
title: "CBRD: T0 Same Day Settling Create/Redeem Cycle With End of Day Cash True-up"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/etf245a_cbrd-T0_2024Jan22.pdf"
pages: 20
size: "735.9 KB"
category: "ETF"
ingested_on: "2026-06-05"
---

# CBRD: T0 Same Day Settling Create/Redeem Cycle With End of Day Cash True-up

**Original File:** [etf245a_cbrd-T0_2024Jan22.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/etf245a_cbrd-T0_2024Jan22.pdf)  
**Category:** ETF  
**Total Pages:** 20  
**File Size:** 735.9 KB  

---

## Page 1

Exchange Traded Fund ([[ETF]]) 
CLIENT BUSINESS REQUIREMENTS: 
T0 SAME DAY SETTLING CREATE/REDEEM CYCLE WITH END OF 
DAY CASH TRUE-UP 
DECEMBER 29, 2023 

---

## Page 2

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 2 
TABLE OF CONTENTS 
Introducing Same Day Settling T0 Create/Redeem Cycle ................................................................................................................................................ 3 
T0 Create/Redeem Cycle With Submission and Reporting of Cash [[collateral]] Amount and End of Day True-up [[collateral]] Cash Adjustment 4 
Dependencies ............................................................................................................................................................................................................... 4 
T0 SDS Cycle – Create/Redeem File Input Changes .................................................................................................................................................... 5 
[[ETF]] Agent Receipt/Reject Reports ................................................................................................................................................................................ 7 
Additional Warning and Reject Codes for the T0 Cycle................................................................................................................................................ 9 
Seq 20 Cash [[collateral]] Amount ................................................................................................................................................................................ 9 
Seq 21 [[collateral]] Cash Adjustment (True-up) ........................................................................................................................................................... 9 
Seq 21 [[collateral]] Cash Adjustment Sign Field (+-) ................................................................................................................................................... 9 
Seq 20 Cash [[collateral]] Amount ................................................................................................................................................................................ 9 
Additional Warning and Reject Codes Primary Cycle ................................................................................................................................................. 10 
Seq 21 [[collateral]] Cash Adjustment ......................................................................................................................................................................... 10 
Seq 22 Sign Field For [[collateral]] Cash Adjustment ................................................................................................................................................. 10 
True-Up Adjustment at End of Day .............................................................................................................................................................................. 11 
Output and Reporting ................................................................................................................................................................................................... 13 
Example Instruction Detail Blotter Reports at Different Times ..................................................................................................................................... 16 
Deposit Withdrawal at Custodian [[DWAC]] ..................................................................................................................................................................... 17 
Phase 1 and Phase 2 True-Up ..................................................................................................................................................................................... 17 
Update ..................................................................................................................................................................................................................... 18 
Backlog Enhancements / Minor Fixes .......................................................................................................................................................................... 18 
[[ETF]] Message Codes for This Release ........................................................................................................................................................................ 19 
 

---

## Page 3

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 3 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 
The issue of shortened [[settlement]] in the T+1 environment was raised at a high level as far back as December 2021 in the [[DTCC]] White Paper on 
Accelerating the [[settlement]] cycle. However, the issue was initially geared to global [[ETF]] Create/Redeem and the Capital Expense of collateralization 
that would result from the mismatch in [[settlement]] cycles for ETFs with global underlying. In January 2023 at an [[NSCC]] [[ETF]] Industry Working Group, 
the top Authorized Participants (APs) described the issue in more detail, stating that the lack of shortened [[settlement]] in the upcoming T+1 cycle 
would be an issue for [[Stock]] loan desks that frequently loan out large blocks of [[ETF]] [[shares]]. It is not an issue in the current T+2 [[settlement]] cycle as 
[[ETF]] [[shares]] are available for [[Stock]] Loan through T+1 shortened [[settlement]]. [[NSCC]] [[ETF]] Product Management encouraged the APs to raise the topic 
to SIFMA to gain momentum, and in mid Q1 2023, SIFMA created an [[ETF]] T+1 Committee. The issue became widespread, and it became quite clear 
that [[NSCC]] needed to develop a same day settling T0 Create/Redeem cycle. 
[[NSCC]] worked with the industry to define the requirements for T0 Create/Redeem, which includes a true-up to end of day net [[Asset]] value (NAV) as 
T0 Create/Redeem will be processed for [[NSCC]] eligible funds using the prior day NAV. The actual T0 cycle was defined at a May 04, 2023 [[NSCC]] 
[[ETF]] T0 Working Group, yet the guarantee of a [[collateral]] buffer and end of day true-up requirements were only recently defined by [[NSCC]] and the 
industry. 
[[ETF]] Sponsors and their servicing [[ETF]] Agent Banks (Agents) required a [[collateral]] buffer that will cover expected change in NAV day-over-day and 
requested the [[collateral]] buffer to be guaranteed by [[NSCC]]. [[NSCC]] worked with some of the top sponsors (iShares, Vanguard, State Street Global 
Advisors, and JPMAM to mention a few) on detailed analysis to determine a percentage of the total NAV that will cover anticipated change in NAV. 
[[NSCC]] Risk has agreed to guarantee a maximum of 3% of the ETFs prior nights NAV, and Agents / Issuers have agreed to submit the buffer at the 
lowest percentage they believe will cover the change on the NAV when struck at the end of trade date. 
[[NSCC]] has announced to the industry our commitment to develop the T0 cycle, targeting the end of May 2024, and will launch in conjunction with the 
T+1 launch. Due to excessive risk introduced by merging T0 code with T+1 code, [[NSCC]] will develop the cycle in a phased deployment with the T0 
cycle. Submission and reporting of Cash [[collateral]] Buffer and end of day Cash True-Up to be released in phase 1 (end of May 2024) and the actual 
true-up to end of day NAV through [[NSCC]] to be released in phase 2, the timing of which is still to be determined, yet will be as close as possible to 
the phase 1 release. 
This client business requirements document is a Draft as [[NSCC]] has not yet fully groomed all developments. The Phase 2 section on [[collateral]] Cash 
Adjustment (true-up) contains limited information, and it will be updated and redistributed, when finalized. 
Note: 
This Client BRD has been updated to reflect additional WARN and REJECT codes, industry best practices on redemptions and the [[NSCC]] Money [[settlement]] code 
that will be used in phase 2 true-up automation. This document will remain in DRAFT state until reviewed with the industry during the January 10-11 Industry Working 
Group. 
  

---

## Page 4

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 4 
T0 Create/Redeem Cycle With Submission and Reporting of Cash [[collateral]] Amount and End 
of Day True-up [[collateral]] Cash Adjustment 
For Phase 1, [[NSCC]] is targeting May 28, 2024 for the launch of the T0 Create/Redeem cycle with submission of a Cash [[collateral]] Amount (buffer) 
and [[EOD]] [[collateral]] Cash Adjustment (true-up).  
Same day [[settlement]] (SDS) T0 Create/Redeem orders will be processed and sent to Universal Trade Capture (UTC) in near real-time and reported 
downstream for [[CNS]]®. [[CNS]] transactions received will be included in the current net settling position in periodic intervals throughout the day cycle on 
[[settlement]] date between approximately 4:30 A.M. to 1:30 P.M. Eastern Time and will be reported on Cycle 3 Consolidated Trade Summary (CTS) at 
1:45 P.M. 
Dependencies 
To launch [[ETF]] T0 to Production on or close to the T+1 launch on May 28, 2024, [[ETF]] Agents and Authorized Participants are required to: 
• Complete and sign off on T+1 [[ETF]] testing by mid-November 2023 allowing for the T0 code to be merged with T+1 early in 2024. 
• Develop the T0 cycle requirements described herein.  
• Complete and sign off on T0 Client testing, which is targeted to begin in early April 2024 with sign off by May 09, 2024 – a narrow window for 
client testing. 
The timelines for development and testing are subject to change if significant issues arise. 
  

---

## Page 5

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 5 
T0 SDS Cycle – Create/Redeem File Input Changes 
[[ETF]] Agents 
• T0 c ycle will open at 12:30 A.M. ET with a hard cutoff at 1:30 P.M. ET. 
• [[NSCC]] will stream trades resulting from T0 orders to Universal Trade Capture (UTC) in near real-time (NRT), beginning when UTC start of day 
opens. 
• [[NSCC]] will allow submission of the DATATRAK Production 11300/PSE 41300 file for T0 Create/Redeem up until the [[CNS]] SDS cutoff at 
approximately 1:29:59  P.M. ET. 
• [[ETF]] Agents / Issuers are to submit the Enhanced Create/Redeem Instruction Data Input file.  
• For [[ETF]] Agents only, submit the DATATRAK Production 11300/PSE 41300 with [[settlement]] Code 0 for SDS T0 orders in type 02 record 
Seq 10. 
DATATRAK Production 11300/PSE 41300  
Type 2–Instruction Record 
Record length=300 
Required for all instructions. 
Seq Description Length Start Type Comments Required or Optional 
Field 
10 [[settlement]] Code 
(previously called Shortened 
[[settlement]] Code) 
1 58 A/N • Space = [[default]] for Regular Way (Next day 
[[settlement]] = regular way) 
• 1 = Next Day Regular Way 
• 0 =T0 Same Day [[settlement]] 
• 2 = Extended 2-day [[settlement]] 
• 3 = Three Day [[settlement]] 
• 4 = Four Day [[settlement]] 
• 5 = Five Day [[settlement]] 
Required 
 
  

---

## Page 6

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 6 
T0 Creation Orders will be processed by [[NSCC]] against the prior night’s end of day pricing which aligns to the prior night’s NAV and will then be 
adjusted (Phase 2) to end of trade date NAV. [[ETF]] sponsors and their clearing [[ETF]] Agent bank will submit a [[collateral]] cash adjustment (buffer) to 
ensure the value of intraday delivery of [[ETF]] [[shares]] will not exceed the value of the [[ETF]] [[shares]] after end of day NAV is calculated. 
• [[ETF]] will burst Create/Redeem orders using the latest PCF file submitted for that fund from the prior evening or in the Supplemental PCF cycle 
using the prior nights end of day [[CNS]] pricing. 
• Supplemental PCF cycle will not change, yet to be used for a T0 order the Supplemental PCF must be submitted prior to the T0 order. 
• To facilitate a collateralization buffer, Agents / Sponsors will submit a Cash [[collateral]] Amount (new field) to [[NSCC]] on the T0 order file 
DATATRAK Production 11300/PSE 41300. 
• Cash [[collateral]] Amount will be added to the [[ETF]] [[settlement]] Value. [[NSCC]] will guarantee the Cash [[collateral]] Amount to a maximum of 3% of 
the prior night’s NAV. [[ETF]] Sponsors have agreed they will submit this [[collateral]] buffer at the lowest percent expected dependent on the 
structure of the fund and current market conditions. 
• [[ETF]] Agents / Issuers to submit new Cash [[collateral]] Amount field on Enhanced Create/Redeem Instruction Data Input File (Agents only) 
DATATRAK Production 11300/PSE 41300 on all order files received only in the T0 cycle between 12:30 A.M. ET and 1:30 P.M. ET for current 
Trade and [[settlement]] Date. 
• Cash [[collateral]] Amount field is submitted by [[ETF]] Agents in Seq 20 on the Type 02 Instruction Record order input on the DATATRAK 
Production 11300/PSE 41300 file. 
• [[NSCC]] will generate the REJECT message code 583 on orders submitted with invalid characters in the Cash [[collateral]] Amount field on Agent 
Receipt/Reject reports. Spaces and zeroes (00000) are valid values, and [[NSCC]] will process the order without the Cash [[collateral]] Amount. This 
will result in a T0 order processed without a collateralized buffer amount. 
  

---

## Page 7

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 7 
[[ETF]] Agent Receipt/Reject Reports 
Report Name Test Production 
Enhanced [[ETF]] End of Day Instruction Create/Redeem Receipt/Reject Report 02980098 02120098 
Enhanced [[ETF]] Intraday Create/Redeem Receipt/Reject Report 02981954 02261954 
 
• [[NSCC]] will divide the buffer amount submitted on the T0 order into the [[ETF]] value and will reject if the buffer is over 3%. 
In the below example the Component [[settlement]] Value + Cash Component = [[ETF]] [[settlement]] Value (without buffer)  $593,382,350.70. divided 
by the Cash [[collateral]] Amount (buffer) $5,933,823.50 is equal to1% If the percentage is greater than 3, [[NSCC]] will generate REJECT message 
code 587 on the Receipt/Reject reports. 
Print Image example of the Instruction Detail Blotter which will be distributed at 12:30 P.M. if submitted prior to 12:15 P.M. It includes the Cash 
[[collateral]] Amount (buffer) and will be used to ensure the buffer does not exceed 3%.  
The [[collateral]] Cash Adjustment will not be distributed at 12:30 P.M. as this true-up amount has not yet been submitted. 
[[NSCC]] PORTFOLIO:                                      [[ETF]] TRADING:  
SYMBOL: 608GK            [[ID]]: 000003608               SYMBOL: SPY              ISIN/[[CUSIP]]: US78462F1030  
UNIT SIZE:       50,000                              NAME:    SPDR S&P 500 [[ETF]] TR           UNIT SER 1 STANDARD & POORS  
-------------------------------------------------------------------------------------------------------------------------------------------------  
TRANSACTION [[ID]]: 23191000027X     CONTRA [[Broker]]: 0000XXXX   EXEC [[Broker]]:              TRANSACTION FEE:      3,000.00CR  
TRANSACTION TIMESTAMP: 16:09:09.946                        REVERSAL INDICATOR: NEW C/R INSTRUCTION  
[[ETF]] UNITS CREATED:                  27  
TOTAL COMPONENT VALUE DEBITED:            593,021,058.300000  
CASH VALUE CREDITED:                          361,292.400000 
Cash [[collateral]] Amount                       5,933,823.50000 
                   
TOTAL [[ETF]] VALUE CREDITED:                  599,316,174.20 ([[ETF]] [[settlement]] Value reported with buffer) 
             
[[collateral]] Cash Adjustment     
                                                       
  

---

## Page 8

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 8 
• [[NSCC]] will reject Regular Way or extended [[settlement]] orders in the primary cycle if submitted with a Cash [[collateral]] Amount or [[collateral]] Cash 
Adjustment field generating REJECT code (590 or 591) on the Receipt/Reject reports.  
Log in to the Learning Center to access the full DATATRAK Production 11300/PSE 41300 format for this release from the [[ETF]] Release section. 
DATATRAK Production 11300/PSE 41300  
Type 2–Instruction Record 
Record length=300 
Required for all instructions. 
Seq Description Length Start Type Comments Required or Optional Field 
20 Cash [[collateral]] 
Amount 
12 112 N New field for T0 submission for the [[collateral]] buffer amount not to 
exceed 3% of the prior night’s net [[Asset]] value (NAV). Required on 
T0 Create/Redeem orders submitted in the T0 cycle between 
12:30 A.M. and 1:30 P.M. Eastern Time with the current day Trade 
and [[settlement]] date. 
Required for same day [[settlement]] (SDS) T0 orders. 
Spaces and zeroes (0000) are valid values. 
21 [[collateral]] Cash 
Adjustment 
12 124 N New field required in the Create/Redeem Primary cycle for all 
SDS T0 orders submitted in the T0 cycle. This true-up amount, 
calculated and submitted by [[ETF]] Agents / Sponsors, represents 
the difference between the Cash [[collateral]] Amount and the Cash 
Amount Adjusted that aligns with the end of trade date NAV. The 
[[collateral]] Cash Adjustment is reported on. 
Required only for T0 orders in the Primary 
Create/Redeem cycle. [[ETF]] Agents should submit 
the same order details in the Primary cycle for a 
true-up on a T0 order and the same transaction [[ID]] 
must be submitted in a follow-up 11300 file with a 
true-up value. 
[[NSCC]] does not fully edit previously reported 
fields, such as Cash [[collateral]] Amount or the 
original  Cash Component. 
22 [[collateral]] Cash 
Adjustment / 
Sign Indicator 
1 136 A/N New field required at the end of day submission of the [[collateral]] 
Cash Adjustment field. Due to limited bytes on the Instruction Detail 
Blotter output file, the indicator also indicates the direction of the 
true-up amount . 
+ = Authorized [[participant]] (AP) is the receiver and [[ETF]] Agent is 
the deliverer of the funds. 
– = [[ETF]] Agent is the receiver and AP is the deliverer of the funds. 
Required only for T0 orders, in the Primary 
Create/Redeem cycle, the same Transaction [[ID]] 
must be submitted in a follow-up 11300 file with a 
true-up value. 
 
Notes: 
[[NSCC]] has groomed all scenarios for submission of the Cash [[collateral]] Amount (Buffer). 

---

## Page 9

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 9 
Additional Warning and Reject Codes for the T0 Cycle 
Seq 20 Cash [[collateral]] Amount 
Spaces and zeroes are acceptable values for submission of the Cash [[collateral]] Amount. [[NSCC]] generates the 592 WARN message code. [[NSCC]] 
processes the order yet no buffer amount is added. If submitted in error, it is the responsibility of the AP and [[ETF]] Agent to satisfy any requirements.  
Message Code Message Type Record Type Description 
592 WARN 2 CASH [[collateral]] NOT SUBMITTED 
Seq 21 [[collateral]] Cash Adjustment (True-up) 
If submitted in the T0 cycle, [[NSCC]] generates the 589 WARN message code. 
Message Code Message Type Record Type Description 
589 WARN 2 [[collateral]] CASH ADJ SUBMITTED IN INCORRECT CYCLE 
Seq 21 [[collateral]] Cash Adjustment Sign Field (+-) 
If the Sign field for [[collateral]] Cash Adjustment is submitted in the T0 cycle, [[NSCC]] generates the 594 WARN message code. 
Message Code Message Type Record Type Description 
594 WARN 2 SIGN ON [[collateral]] CASH ADJ SUBMITTED IN T0 CYCLE 
Seq 20 Cash [[collateral]] Amount 
In all instances where a non-numeric value with bad characters are submitted in this field, [[NSCC]] generates the 583 REJECT message code. 
Message Code Message Type Record Type Description 
583 REJ 1 CASH [[collateral]] AMT NOT NUMERIC 
 
  

---

## Page 10

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 10 
Additional Warning and Reject Codes Primary Cycle 
Seq 21 [[collateral]] Cash Adjustment 
If the [[collateral]] Cash Adjustment is submitted as non-numeric with bad characters in Primary cycle, [[NSCC]] generates the 584 REJECT message 
code. 
Message Code Message Type Record Type Description 
584 REJ 1 [[collateral]] CASH ADJ AMT NOT NUMERIC 
 
If the [[collateral]] Cash Adjustment is submitted in the T0 cycle, [[NSCC]] generates the 588 REJECT message code. 
Message Code Message Type Record Type Description 
588 REJ 1 [[collateral]] CASH ADJ SUBMITTED IN T0 CYCLE 
Seq 22 Sign Field For [[collateral]] Cash Adjustment  
If an invalid character is submitted in the Seq 22 Sign field for [[collateral]] Cash Adjustment, [[NSCC]] generates the 585 REJECT message code. Keep 
in mind that  (+-) are the only valid signs for this field, 
Message Code Message Type Record Type Description 
585 REJ 1 SIGN FOR [[collateral]] CASH ADJ AMT INVALID 
 
If a sign field is submitted in either T0 Same Day [[settlement]] (SDS) or Supplemental cycle [[NSCC]] generates the 593 WARN message code. 
Message Code Message Type Record Type Description 
593 WARN 2 SIGN ON [[collateral]] CASH ADJ SUBMITTED ON NON T0 CYCLE 
 
If the sign field is submitted in either the T0 Same Day Settling or Supplemental cycle, [[NSCC]] generates the 594 WARN message code. 
Message Code Message Type Record Type Description 
594 WARN 2 SIGN ON [[collateral]] CASH ADJ SUBMITTED IN T0 CYCLE 
 

---

## Page 11

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 11 
If [[collateral]] Cash Adjustment is submitted with non-numeric bad characters in T0 (SDS) or Supplemental cycle, [[NSCC]] generates the 596 WARN 
message code. 
Message Code Message Type Record Type Description 
596 WARN 2 [[collateral]] CASH ADJ NOT NUMERIC AND SUBMITTED ON NON 
T0 CYCLE 
 
A full list of reject and warning message codes will be distributed under separate cover. See Also: [[ETF]] Message Codes for This Release in this 
document and the [[ETF]] Message Codes for the current release available in the Learning Center.  
True-Up Adjustment at End of Day 
[[ETF]] Agents submission of true up amount (output details in reporting section below) 
• [[ETF]] Agents / Sponsors to submit new [[collateral]] Cash Adjustment field in the Primary cycle (2:00 P.M. - 8:45 P.M. ET). This reflects the 
updated timing when T+1 is launched. 
• [[NSCC]] will generate a WARN message code 586 at the end of Primary Cycle if a [[collateral]] Cash Adjustment is not submitted. The associated 
T0 order has already been processed, hence, the WARN. In cases where a true-up has not been submitted, it will be the responsibility of the 
[[ETF]] Agent and AP to reconcile. When [[NSCC]] launches Phase 2 automation of the true-up, an [[NSCC]] money [[settlement]] code will not be 
processed if the true-up is not submitted. 
• [[NSCC]] will generate WARN message code 589 if a [[collateral]] Cash Adjustment is submitted on a T0 order in the Supplemental Create/Redeem 
cycle (9:00 P.M. -11:30 P.M.). [[NSCC]] will also generate a 589 WARN if [[collateral]] Cash Adjustment is submitted in the T0/Same Day Settling 
cycle. The Instruction Detail Blotter distributed at 9:00 P.M. has already reported this field as NOSUB. In this scenario, APs are responsible for 
contacting the [[ETF]] Agent and settling the true-up through Security Payment Orders (SPOs) until such time that [[NSCC]] launches the automated 
true-up planned in Phase 2. 
• [[collateral]] Cash Adjustment field to be submitted in the order input file Type 02 Record in Seq 21. 
  

---

## Page 12

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 12 
• [[ETF]] Agents / Sponsors to submit [[collateral]] Cash Adjustment / Sign Indicator field in Type 02 Record Seq 22 on the order input file. This 
submission indicates that this is a follow-up 11300 file with a true-up value on an order that was processed in the T0 cycle submission. A plus 
sign (+) indicates the true-up adjustment will be paid to APs, while a minus sign (-) indicates the true-up will be paid to the [[ETF]] Agent. 
Notes 
• Although [[ETF]] Agents will report the direction of true-up funds as a plus (+) or minus (-) on input, on the Machine Readable IDB output, the 
receiver of the true-up funds will be reported as C for a Credit or D for a Debit. 
• Based on analysis of NAV price changes over a 3-year period the [[collateral]] buffer is expected to cover change in NAV at end of trade and 
[[settlement]] date. Based on this analysis the true-up is expected to always be a credit to APs. However, [[NSCC]] will develop and allow for a true-up 
to be paid back to the Agent if the Cash [[collateral]] Amount does not cover change in NAV, yet [[ETF]] Sponsors are encouraged to not offer T0 for a 
fund where the 3% maximum [[collateral]] buffer may not cover change in NAV. 
• [[NSCC]] will report all T0 orders received in the T0 cycle (12:30 A.M. ET to 12:15 P.M. ET) in the 12:30 P.M. distribution of the Instruction Detail 
Blotter (IDB) AutoRoute Production 02261254/PSE 02981254.  
• PCF Supplemental cycle will end at 12:00 P.M., allowing all T0 orders received by 12:15 P.M. to be processed against the latest PCF received if 
late PCF revisions are submitted in the supplemental cycle. 
• IDB distribution will report the Cash [[collateral]] Amount at 12:30 P.M. ET. During this distribution time, the [[collateral]] Cash Adjustment will not 
include the true-up ([[collateral]] Cash Adjustment field) since the end of Trade Date NAV is unknown at this time. 
• Any orders received in the T0 cycle after 12:15 P.M. ET will be reported only on the 9:00 P.M. ET distribution of the IDB. 
Note 
For more information about reporting of  Cash [[collateral]] Amount,  [[collateral]] Cash Adjustment, and [[collateral]] Cash Adjustment Debit / Credit Indicator, [[ETF]] 
Agents and APs should review the Output and Reporting section. 
• “As Of” Create/Redeem processing in the Intraday cycle will not change for T0. This process will align with the T+1 processing. [[NSCC]] will allow 
reversals to be submitted “As Of” up to five days to accommodate extended [[settlement]] orders that may need to be reversed. As of the prior 
trade date for Regular Way [[settlement]] will settle the same day. As Of two through five days for Regular Way [[settlement]] will be assigned the 
next available [[settlement]] date. 
• [[NSCC]] will send Trade-for-Trade (TFT-Non [[CNS]] eligible components) SPOs to Inventory Management System (IMS) intraday for 
Create/Redeem orders processed in the T0 SDS cycle. This is consistent with the current process of “As Of” reversals submitted in the intraday 
cycle.  
[[ETF]] Agents / Authorized [[participant]] / [[ETF]] Sponsors 
• Redemptions – The industry has stated that T0 (SDS) Create/Redeem orders are primarily for Creations, yet it is possible that redemption 
orders for reversals or exceptions may be submitted. Redemptions will follow all input and output requirements described herein.  
  

---

## Page 13

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 13 
• [[NSCC]] will allow and process redemptions in the T0 cycle based on industry requirement, however a negative buffer value on redemptions has 
not been built. Therefore, a buffer on a redemption order will not protect the [[issuer]]. On Redemptions, [[ETF]] Agents are debited cash for receipt of 
[[ETF]] [[shares]] which would be escalated if a buffer is submitted. On a straight redemption order (not submitted for reversal), [[ETF]] Agents have 
[[Option]] to submit order with no buffer (spaces or zeroes) and then true-up with AP at end of day based on market fluctuation. The true-up does 
allow for a positive or negative value (+-) so the true-up can be a debit or credit for [[ETF]] Agent and AP. 
• Reversal/Correction Processing – As per the current process, any order that is submitted in error can be reversed and corrected in the 
T0 cycle. To reverse a creation order, the [[ETF]] Agent is required to submit a redemption inclusive of the same buffer amount that was submitted 
on the creation it is meant to correct. The redemption will net out with the creation and no true-up will be required at the end of day. A corrected 
creation can be submitted with the proper buffer amount and that will be the only order that requires a true-up at the end of day. 
Output and Reporting 
[[ETF]] Agents and Authorized Participants 
• [[NSCC]] will distribute the IDB for all T0 orders received before 12:15 P.M. on the 12:30 P.M. IDB distribution.  
• 12:30 IDB distribution: 
o L abeled as cycle 03 on the DataTrak header. 
o I ncludes the [[collateral]] buffer amount in the Cash [[collateral]] Amount field in Seq 33 in the Type 02 Record on the IDB.  
For more information, see the AutoRoute Production 02261254/PSE 02981254 output file. 
• [[NSCC]] will distribute all T0 orders received in the T0 cycle (12:30 A.M. – 1:30 P.M.) on the 9:00 P.M. IDB distribution, including all T0 orders 
processed between 12:15 P.M. and 1:30 P.M. ET.  
• [[collateral]] Cash Adjustment Amount received by [[ETF]] Agents in the primary Create/Redeem cycle for processed T0 orders will be distributed in 
Seq 34 in the Type 02 Record on the 9:00 P.M. ET distribution of the IDB. The [[collateral]] Cash Adjustment represents the true-up to end of day 
NAV. 
• [[collateral]] Cash Adjustment Debit /Credit Indicator will also be distributed during the 9:00 P.M. ET IDB. 
Note: 
[[ETF]] Agents report this true-up adjustment indicator on order input with a plus (+) or a minus  (-) sign as described above. On the Machine Readable IDB output 
this indicator is reported as a D for Debit or C for Credit. 
[[ETF]] Agents submitting a plus (+) on true-up input file indicate that the AP is the receiver of the true-up funds and the [[ETF]] Agent is the deliverer of the funds. On 
the IDB MRO output, a plus (+) on input will be reported as a C for Credit, which indicates that the AP is the receiver of true-up funds. 
[[ETF]] Agents submitting a minus (-) on true-up input file indicate that the [[ETF]] Agent is the receiver of the true-up funds and the AP is the deliverer of the funds. 
On the IDB MRO output, a minus (-) on input will be reported as a D for Debit, which indicates the [[ETF]] Agent is the receiver of the true-up funds. 
  

---

## Page 14

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 14 
• For only T0 orders, in the Primary Create/Redeem cycle, Agents must submit the same Transaction [[ID]] in a follow-up file with a true-up value in 
the Type 02 Seq 2 Instruction Record of the Prod 11300/PSE41300 file. [[ETF]] Agents can recycle the T0 order file and include all fields 
previously submitted with the addition of the true-up amount in the [[collateral]] Cash Adjustment field and (+-) sign field as described in this 
section. 
Note 
As described in the [[ETF]] Agent input section, [[ETF]] sponsors are discouraged from offering T0 if the buffer maximum of 3% cannot cover expected change in 
NAV. 
If an [[ETF]] Agent does not submit an End of Day Instruction file containing the true up value, [[NSCC]] generates a WARN code to Agents on the End of Day 
Create/Redeem Receipt/Reject report. The true-up to NAV for that T0 order will need to be addressed by the [[ETF]] Agent and AP as the true-up amount will not 
have been reported. 
• In cases when an [[ETF]] Agent does not submit the true-up Create/Redeem input file [[NSCC]] will distribute a message in the [[collateral]] Cash 
Adjustment field, (NOSUB) to indicate that the true-up was NOT SUBMITTED. Until [[NSCC]] launches an automated true-up, APs and [[ETF]] 
Agents will need to agree the true-up amount ex-clearing and submit an SPO. 
• I f a true-up is submitted on an T0 order in the Supplemental Create/Redeem cycle (9 P.M. – 11:30 P.M.), [[NSCC]] will generate WARN 589 on the 
Receipt/Reject reports ([[ETF]] Agents only). 
Here are the description of the new Instruction Detail Blotter fields for the Machine Readable and Print format. Log in to the Learning Center and 
access the full Prod 11300 format, along with the output 02261254 file, from the [[ETF]] Release section. 
DATATRAK Production 11300/PSE 41300  
Type 2–Instruction Record 
Record length=300 
Required for all instructions. 
Seq Description Length Start Type Comments Required or Optional Field 
1 Record Type 2 1 A/N 02 = Record Type 2 One per instruction. Required 
2 Transaction [[ID]] 12 3 N [[ETF]] agent assigned transaction [[ID]]. 
One per instruction. The same transaction [[ID]] should be used 
for each record of an instruction. For only T0 orders, in the 
Primary Create/Redeem cycle, the same Transaction [[ID]] must 
be submitted in a follow-up 11300 file with a true-up value. 
Required 
3 [[NSCC]] Portfolio [[ID]] 9 15 A/N [[NSCC]] assigned Portfolio [[ID]] of the basket. Required 
4 Trade Date 8 24 N CCYYMMDD – 
(Trade Date or As/Of Date) 
Required 

---

## Page 15

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 15 
DATATRAK Production 11300/PSE 41300  
Type 2–Instruction Record 
Record length=300 
Required for all instructions. 
5 [[ETF]] Agent 8 32 N [[NSCC]] assigned clearing number of the agent. Required 
6 Contra Clearing Firm 8 40 N [[NSCC]] assigned clearing number of the [[Broker]] dealer. Required 
7 Executing [[Broker]] [[ID]] 8 48 A/N Executing [[Broker]] [[ID]] provided by the [[ETF]] agent. Optional 
8 Create Redeem Code 1 56 A/N • C = Create 
• R = Redeem Required 
 
20 Cash [[collateral]] Amount 12 112 N New field for T0 submission for the [[collateral]] buffer amount not to 
exceed 3% of the prior night’s net [[Asset]] value (NAV). Required on 
T0 Create/Redeem orders submitted in the T0 cycle between 12:30 
A.M. and 1:30 P.M. Eastern Time with the current day Trade and 
[[settlement]] date. 
Required for same day [[settlement]] 
(SDS) T0 orders. 
Spaces and zeroes (0000) are valid 
values.  
21 [[collateral]] Cash 
Adjustment 
12 124 N New field required in the Create/Redeem Primary cycle for all SDS 
T0 orders submitted in the T0 cycle. This true-up amount, calculated 
and submitted by [[ETF]] Agents / Sponsors, represents the difference 
between the Cash [[collateral]] Amount and the Cash Amount 
Adjusted that aligns with the end of trade date NAV. The [[collateral]] 
Cash Adjustment is reported on. 
Required only for T0 orders, in the 
Primary Create/Redeem cycle. [[ETF]] 
Agents should submit the same order 
details in the Primary cycle for a true-
up on a T0 order and the same 
Transaction [[ID]] must be submitted in a 
follow-up 11300 file with a true-up 
value. 
[[NSCC]] does not fully edit previously 
reported fields. such as Cash 
[[collateral]] Amount or the original 
Cash Component. 
22 [[collateral]] Cash 
Adjustment / Sign Indicator 
1 136 A/N New field required at the end of day submission of the [[collateral]] 
Cash Adjustment field. Due to limited bytes on the Instruction Detail 
Blotter output file, the indicator also indicates the direction of the 
true-up amount . 
• + = Authorized [[participant]] (AP) is the receiver and [[ETF]] Agent is 
the deliverer of the funds. 
• – = [[ETF]] Agent is the receiver and AP is the deliverer of the funds. 
Required only for T0 orders, in the 
Primary Create/Redeem cycle, the 
same Transaction [[ID]] must be 
submitted in a follow-up 11300 file 
with a true-up value. 

---

## Page 16

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 16 
DATATRAK Production 11300/PSE 41300  
Type 2–Instruction Record 
Record length=300 
Required for all instructions. 
20 Future use 164 137    
END OF RECORD 
Example Instruction Detail Blotter Reports at Different Times 
Instruction Detail Blotter Print Image Mockup reported at 12:30 P.M. ET, which includes the buffer field Cash [[collateral]] Amount. 
[[NSCC]] PORTFOLIO:                                      [[ETF]] TRADING:  
SYMBOL: 608GK            [[ID]]: 000003608               SYMBOL: SPY              ISIN/[[CUSIP]]: US78462F1030  
UNIT SIZE:       50,000                              NAME:    SPDR S&P 500 [[ETF]] TR           UNIT SER 1 STANDARD & POORS  
-------------------------------------------------------------------------------------------------------------------------------------------------  
TRANSACTION [[ID]]: 23191000027X     CONTRA [[Broker]]: 0000XXXX   EXEC [[Broker]]:              TRANSACTION FEE:      3,000.00CR  
TRANSACTION TIMESTAMP: 16:09:09.946                        REVERSAL INDICATOR: NEW C/R INSTRUCTION  
[[ETF]] UNITS CREATED:                  27  
TOTAL COMPONENT VALUE DEBITED:            593,021,058.300000  
CASH VALUE CREDITED:                          361,292.400000 
Cash [[collateral]] Amount                       5,933,823.50000 
                   
TOTAL [[ETF]] VALUE CREDITED:                  599,316,174.20 ([[ETF]] [[settlement]] Value reported with buffer) 
             
[[collateral]] Cash Adjustment     
                                                       
Instruction Detail Blotter Print Image Mockup reported at 9:00 P.M. ET, which includes the true-up field [[collateral]] Cash Adjustment and 
[[collateral]] Cash Adjustment / Sign Indicator field. 
[[NSCC]] PORTFOLIO:                                      [[ETF]] TRADING:  
SYMBOL: 608GK            [[ID]]: 000003608               SYMBOL: SPY              ISIN/[[CUSIP]]: US78462F1030  
UNIT SIZE:       50,000                              NAME:    SPDR S&P 500 [[ETF]] TR           UNIT SER 1 STANDARD & POORS  
----------------------------------------------------------------------------------------------------------------------------------------  
TRANSACTION [[ID]]: 23191000027X     CONTRA [[Broker]]: 0000XXXX   EXEC [[Broker]]:              TRANSACTION FEE:      3,000.00CR  
TRANSACTION TIMESTAMP: 16:09:09.946                        REVERSAL INDICATOR: NEW C/R INSTRUCTION  

---

## Page 17

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 17 
[[ETF]] UNITS CREATED:                  27  
TOTAL COMPONENT VALUE DEBITED:            593,021,058.300000  
CASH VALUE CREDITED:                          361,292.400000 
Cash [[collateral]] Amount                      5,933,823.500000    
                   
TOTAL [[ETF]] VALUE CREDITED:                  599,316,174.20  
             
[[collateral]] Cash Adjustment CREDITED         500,000  
Deposit Withdrawal at Custodian [[DWAC]] 
• [[ETF]] Agents / Transfer Agents will have a short window to deposit [[ETF]] [[shares]] for the [[settlement]] of T0 Creation orders. [[ETF]] [[shares]] must be 
deposited and approved prior to final [[settlement]] at approximately 3:10 P.M. 
• Negotiated Baskets in T0 SDS cycle – Based on industry feedback Negotiated Create/Redeem orders are out of scope. Current editing of 
Negotiated PCF will remain, Negotiated PCF submitted in T0 cycle will be provisionally accepted and orders submitted for Regular Way or 
Extended [[settlement]] with the same transaction [[ID]] will be processed. 
• Negotiated Create/Redeem orders submitted in the T0 cycle generates REJECT code 580 on the [[ETF]] Agent Receipt/Reject reports. 
• [[NSCC]] can implement T0 Negotiated orders if and when the industry is ready.  
Phase 1 and Phase 2 True-Up 
[[ETF]] Agents / Authorized Participants 
In Phase 1, as described above, [[ETF]] Agents will submit an end of day Create/Redeem Order file, Production 11300/PSE41300, that will include a 
true-up amount ([[collateral]] Cash Adjustment field) and [[collateral]] Cash Adjustment Debit / Credit Indicator field. In most instances, APs will be 
responsible for submitting an SPO to claim the true-up value for each order. In rare instances, [[ETF]] Agents may also be responsible to claim funds if 
the [[collateral]] buffer amount did not cover the change in NAV. 
[[NSCC]] will coordinate additional discussions on standards for submission and approval of these SPOs until [[NSCC]] develops a solution. 
In Phase 2, [[NSCC]] will develop and launch a process for the collection of true-up amounts for each order. In most industry discussions to date, SPOs 
were considered the likely method of generating a true-up. However, through analysis and design discussions [[NSCC]] will now develop a new [[NSCC]] 
money [[settlement]] code similar to the Code 54 and 55 transactions fees. Money [[settlement]] codes are direct debits and credits to [[ETF]] Agent and AP 
accounts. This change in direction is expected to speed the launch of a true-up process to production and minimize [[ETF]] Agent and AP coding 
requirements. It also eliminates possible issues with the lack of the [[ETF]] Fund subaccount standing [[settlement]] instructions (SSI). 
[[NSCC]] expects to have full Client Requirements documented for the new [[NSCC]] Money [[settlement]] code in the coming weeks. Afterwards, this 
document will be updated and redistributed. 

---

## Page 18

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 18 
Update 
As stated above, [[NSCC]] automates the true-up process in a subsequent phase through [[NSCC]] Money [[settlement]]. Currently, [[NSCC]] Money 
[[settlement]] codes are used to pass transactions fees from [[ETF]] Agents to Authorized Participants (AP). [[NSCC]] Money [[settlement]] Code 54 is used for 
the Standard basket transaction fee and Code 55 for the Custom basket transaction fees. For the existing codes, the transaction fee is always a 
debit to the AP and a credit to the [[ETF]] Agent. 
For the true-up process, the new Money [[settlement]] Code will be 56. [[NSCC]] will process the [[collateral]] Cash Adjustment field (true-up) submitted by 
the [[ETF]] Agents in the primary cycle and pass it to [[NSCC]] Money [[settlement]] using Code 56. This code can appear as a credit or a debit to both [[ETF]] 
Agents and APs, depending on the sign field submitted. This is described in the True-Up Adjustment at End of Day section. All Money [[settlement]] 
debits and credits appear in [[settlement]] Web and are automatically processed against your clearing account. [[ETF]] Agents and APs should ensure 
they have access to the [[settlement]] Web in the PSE/U test environment to ensure that they are ready when released for client testing. 
The exact timeline for PSE/U client testing and release to production have yet to be determined and have several dependencies, as noted above. 
Backlog Enhancements / Minor Fixes 
The following enhancements have been in [[NSCC]]’s backlog and were expected to be released prior to T+1 before T0 took precedence. [[NSCC]] will 
develop these enhancements, as time allows, while developing T0. [[NSCC]] will update this document and announce PSE/U and Production launch 
dates as they become available. 
• Enhancement – Carry Forward Cash Only Baskets (Carry Forward all Non Custom) Standard, Create, Redeem, and Cash Only. 
• Enhancement – Create a new [[ID]] type (type 98 other) similar to [[ID]] type 99 Other, except with the new [[ID]] type [[NSCC]] will not mark the 
component as Cash in Lieu. This will allow Cash In Kind orders and may be used for future enhancements, specifically for [[Option]] Funds. 
• Bug Fix – Custom Record 04 Mandatory on Negotiated PCF- [[NSCC]] will currently process Negotiated PCF / Orders without a Custom Record. 
Negotiated (and all custom baskets) are supposed to be published to the submitting [[ETF]] Agent and the AP named in 04 Record in 
near real-time. 
• Bug Fix – Cash only with All components CIL, PCF format states a Space is any combination of Cash and [[Stock]]; however, [[NSCC]] is currently 
rejecting orders where the PCF has all underlying marked as CIL. 
  

---

## Page 19

Client Business Requirements: 
T0 Same Day Settling Create/Redeem Cycle with End of Day Cash True-up 
INTRODUCING SAME DAY SETTLING T0 CREATE/REDEEM CYCLE 19 
[[ETF]] Message Codes for This Release 
The following table shows the new message code for this release, along with the message type and descriptions. These message codes are 
available after the specific initiative is deployed and will be added to the current message codes available at [[ETF]] Message Codes. We will continue 
to add message codes for this release, as needed.  
Message Code Message Type Record Type Field File Type Message Description 
580 REJ 2 10 C/R T0 ORDER IS NOT ALLOWED IN THE NEGOTIATED CYCLE 
583 REJ 2 20 C/R CASH [[collateral]] AMOUNT NOT NUMERIC 
584 REJ 2 21 C/R [[collateral]] CASH ADJUSTMENT NOT NUMERIC 
585 REJ 2 22 C/R SIGN ON [[collateral]] CASH ADJUSTMENT IS INVALID 
586 WARN 2 21 C/R [[collateral]] CASH ADJUSTMENT NOT SUBMITTED 
587 REJ 2 20 C/R CASH [[collateral]] IS ABOVE THE 3% THRESHOLD 
588 REJ 2 21 C/R [[collateral]] CASH ADJUSTMENT SUBMITTED IN THE T0 CYCLE 
589 WARN 2 21 C/R [[collateral]] CASH ADJUSTMENT SUBMITTED IN THE INCORRECT CYCLE 
590 REJ 2 20 C/R CASH [[collateral]] AMOUNT ALLOWED ONLY ON T0 ORDERS 
591 REJ 2 21 C/R [[collateral]] CASH ADJUSTMENT ALLOWED ONLY ON T0 ORDERS 
592 WARN 2 C/R CASH [[collateral]] NOT SUBMITTED 
593 WARN 2 C/ R SIGN ON [[collateral]] CASH ADJ SUMMITED ON NON T0 CYCLE 
594 WARN 2 C/R SIGN ON [[collateral]] CASH ADJ SUBMITTED IN T0 CYCLE 
596 WARN 2 C/ R [[collateral]] CASH ADJ NOT NUMBERIC AND SUBMITTED ON NON T0 CYCLE 

---

## Page 20

© 2024 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and unregistered trademarks of The Depository 
Trust & Clearing Corporation [[DTCC]]. The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of 
the particular country or countries in which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
Doc Date: January 22, 2024 
Publication Code: ETF245a 
Service: Exchange Traded Fund ([[ETF]]) 
Title: Client Business Requirements: T0 Same Day Settling Create/Redeem Cycle With End of Day Cash True-up 
For More Information 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 