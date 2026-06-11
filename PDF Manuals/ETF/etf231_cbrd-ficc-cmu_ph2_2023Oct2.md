---
title: "Phase 2: Clearing Enhancements to Support Fixed Income Assets for Corporate, Municipal, and UIT (CMU)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/etf231_cbrd-ficc-cmu_ph2_2023Oct2.pdf"
pages: 71
size: "1531.4 KB"
category: "ETF"
ingested_on: "2026-06-05"
---

# Phase 2: Clearing Enhancements to Support Fixed Income Assets for Corporate, Municipal, and UIT (CMU)

**Original File:** [etf231_cbrd-ficc-cmu_ph2_2023Oct2.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/etf231_cbrd-ficc-cmu_ph2_2023Oct2.pdf)  
**Category:** ETF  
**Total Pages:** 71  
**File Size:** 1531.4 KB  

---

## Page 1

Exchange Traded Fund ([[ETF]])
CLIENT BUSINESS REQUIREMENTS
PHASE 2: CLEARING ENHANCEMENTS TO 
SUPPORT FIXED INCOME ASSETS FOR 
CORPORATE, MUNICIPAL, AND [[UIT]] (CMU)
VERSION 9.2
OCTOBER 2
8, 2021


---

## Page 2

TABLE OF CONTENTS
What’s New? 5
Introducing Clearing Enhancements to Support Fixed Income Assets 6
Corporate and Municipal Bond Eligibility 6
Updates to the [[ETF]] Phase 2 Business Requirements 7
Viewing the [[ETF]] Eligibility Inquiry 7
Determining Eligibility for Fixed Income Components T-1 and T 8
Still Under Review 9
Corporate/MUNI Create Redeem Process Flows 10
Redeem Order Partial [[CNS]]/TFT Settle 10
Create Order Partial [[CNS]]/TFT Settle 11
Corporate and MUNI Bond Eligibility for Clearance 11
Eligibility Reporting 12
Reporting of TFT Items 13
Eligibility Scenarios 15
Subsequent Order Processing 11300 20
Negotiated Basket – Updated from the Phase 1 Client Business Requirements Effective for Phase 222
Enhanced [[ETF]] Create and Redeem Instruction 25
Print Image Create/Redeem [[ETF]] Blotter Report Mockup 27
Extended [[settlement]] Fixed Income ETFs 29
Extended [[settlement]] Equities 29
Extended [[settlement]] Fixed Income 29
Accrued Interest 31
Rules and Edits 32
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
TableOfContents
2

---

## Page 3

Standard, Restricted, Rebalance, Create Only, and Redeem Only Baskets for Fixed Income 32
Negotiated Baskets Accrued Interest Fixed Income 32
Message Codes 33
Accrued Interest Calculations 34
Standard Baskets, Restricted, Rebalance, Create and Redeem Baskets Fixed Income 34
Print Image Mockup: Standard Basket Accrued Interest 35
Negotiated Baskets Calculations 36
Print Image Mockup: Negotiated Fixed Income Basket Accrued Calculation 37
Accrued Interest Sourcing 38
Accrued Interest Type 5-Custom Added Components Record 39
[[Margin]] Impact/Clearing Fund and VaR Calculator 41
Benefits 41
Addendum Phase 2 – [[collateral]] Service 42
Eligibility 45
Eligibility Changes Inter-[[settlement]] Cycle 45
Calculation and Reporting of Payment Orders for Collateralization of TFT [[securities]] 45
Create/Redeem [[ETF]] Blotter Report Mockup 46
Sample Create/Redeem [[ETF]] Blotter Reports 50
Standard Creation – Authorized Participants 51
Standard Creation – [[ETF]] Agents 52
Negotiated Creation – Authorized Participants 53
Negotiated Creation – [[ETF]] Agents 54
Standard Redemption – Authorized Participants 55
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
TableOfContents
3

---

## Page 4

Standard Redemption – [[ETF]] Agents 56
Negotiated Redemption – Authorized Participants 57
Negotiated Redemption – [[ETF]] Agents 58
Create/Redeem Instruction Detail MRO 59
[[ETF]] Create and Redeem Instruction Input MRO: DATATRAK 11300 61
New Message Codes 62
Payment Orders Processing 64
Mockup 65
Appendix A: Sub-Issue Types and Eligibility 67
Appendix B: Glossary 70
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
TableOfContents
4

---

## Page 5

WHAT’S NEW?
This section provides links to updates since the previous version that are highlighted in red.
l Provided more explanation of the Reason Code 805 and removed the input links in the Payment
Orders Processing section.
l Added a Mockup that shows the 805 reason code on [[settlement]] Web.
l Included New Message Codes for Phase 2.
l Clarified handling Provisionally Accepted components after 7:00 PM. See the Determining Eligibility for
Fixed Income Components T-1 and T, Corporate and MUNI Bond Eligibility for Clearance, and Nego-
tiated Basket – Updated from the Phase 1 Client Business Requirements Effective for Phase 2 [[SEC]]-
tions.
l Modified the Start column for sequences 22 – 25 in the Type 5–Components Record for the
02261254/PSE 02981254 file. See the table for Type 5–Components Record.
l Updated the comments for Type 05, Sequence 13 in AutoRoute 02261254. See Eligibility Reporting or
access full file formats from the [[ETF]] Phase 2 Deployment tab.
l Updated the comments for Type 03, Sequence 13 in AutoRoute 02261256 and 02262335. See Eli-
gibility Reporting or access full file formats from the [[ETF]] Phase 2 Deployment tab.
l Expanded the note regarding the print image version for the instruction detail blotter. See Print Image
Create/Redeem [[ETF]] Blotter Report Mockup.
l Added the timing of the payment order processing. See Payment Orders Processing.
l Included an update about the [[Haircut]] percentage. See Calculation and Reporting of Payment Orders
for Collateralization of TFT [[securities]] and  Payment Orders Processing.
l Updated the Accrued Interest Calculations section to include the factor rate, where appropriate.
Note
Access all [[ETF]] Phase 2 Deployment MRO file format from the [[ETF]] Phase 2 Deployment tab.
Phase 2: Clearing Enhancements to Support Fixed Income Assets for Corporate, Municipal, and [[UIT]] (CMU)
What’s New?
5

---

## Page 6

INTRODUCING CLEARING 
ENHANCEMENTS TO SUPPORT FIXED 
INCOME ASSETS
Phase 1 PCF enhancements introduced features and automated controls to expand its existing [[ETF]] 
primary market clearing process to include processing of multiple basket types and add flexibility for order 
customization. Phase 1 PCF enhancements also included the addition of Accrued Interest in preparation 
for Phase 2. 
[[NSCC]] introduces enhancements in Phase 2 to enable clearance of Fixed Income ETFs with Corporate 
and Municipal Bond components.
Corporate and Municipal Bond Eligibility
[[NSCC]] and [[CNS]]® eligibility for Corporate and Municipal Bond components is critical for clearance through 
[[NSCC]]’s Create/Redeem Service. [[NSCC]] has completed an in-depth review of all fixed income 
components submitted through the [[ETF]] Portfolio Composition service. There is a vast universe of 
Corporate and Municipal [[Bonds]] that fall into a range of classifications represented at [[DTCC]] by sub-issue 
types (SIT). For risk-related reasons many SITs are not [[CNS]] eligible. Yet the SITs that are non-[[CNS]] 
eligible are frequently [[DTC]]/[[NSCC]] eligible, which allows for trade-for-trade (TFT) delivery through [[DTC]] 
(RVP / DVP).
In Phase 2, clearance of Corporate and Municipal Bond ETFs, [[NSCC]] will provide [[CNS]] versus TFT 
eligibility in near real-time through the PCF output, Enhanced Consolidated Portfolio Composition Output 
File: AutoRoute Production 02261256/Test 02981256 for Negotiated PCFs. For all other basket types, 
eligibility will be reported on the PCF output on T-1 at the end of the Primary PCF cycle.
Additionally, [[NSCC]] provides a lookup for underlying component eligibility through the [[ETF]] Dashboard 
user interface accessible from the Clearing Dashboard in the MyDTCC portal. This allows [[ETF]] agents and 
authorized participants (APs) the ability to gather [[CNS]], TFT, or ineligible information for substitution in 
instances when [[Bonds]] are not found. See the [[ETF]] Eligibility Inquiry user interface.
Although Phase 2 will focus on Corporate and Municipal [[securities]], any debt [[securities]] that are found on 
the [[DTC]] Security Master will be set up on the [[NSCC]] Security Master as TFT eligible. A TFT [[Broker]]-to-
[[Broker]] ticket will be issued through the Consolidated Trade Summary (CTS) for reconciliation purposes. 
For example, a Treasury Bond that is on the [[DTC]] master will generate a TFT ticket upon bursting of an 
[[ETF]] Create or Redeem order as long as the treasury is on the [[DTC]] master. In this instance, the Treasury 
security will be considered part of the In Kind order; however, [[settlement]] still occurs at the Federal 
Reserve.
On Day 1 after deployment of Phase 2, all Fixed Income CUSIPs that are not in the [[NSCC]] Security Master 
database currently will be added if they appear in the [[DTC]] Security Master File Data Service. After the 
initial load on day 1, new CUSIPs will be added to the [[NSCC]] Security Master as they appear in the 
Portfolio Composition file (PCF). 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
IntroducingClearingEnhancementsToSupportFixedIncomeAssets
6

---

## Page 7

For a list of [[DTC]] sub-issue types assigned to all debt [[securities]] with their assigned eligibility, [[CNS]] or TFT, 
see Appendix A: Sub-Issue Types and Eligibility. 
Updates to the [[ETF]] Phase 2 Business Requirements
This business requirement document has been updated to reflect the following changes:
 l Extended [[settlement]] for Clearance of Fixed Income ETFs, Phase 2.
 l Changes to the description in the Accrued Interest fields on the DATATRAK Production 11301/Test 
41301, AutoRoute Production 02261256/Test 02981256, and AutoRoute Production 02262335/Test 
02982335 record layouts. For more information, see Client Business Requirements: Phase 1 — PCF 
Enhancements for Processing Multiple Basket Types.
 l Addition of the Accrued Interest fields in the Type 5–Custom Added Components Record for 
DATATRAK Production 11300/PSE 41300.
 l Update to the Net Reason Code 55 which will reflect Trade-for-Trade (Non [[CNS]] eligible) for both Fixed 
Income and [[Equity]] components.
Note
 l All updates throughout this document are highlighted in red. For the main updates, see Extended 
Settle Fixed Income for ETFs.
 l For the requirements for   [[collateral]] Service, see Addendum Phase 2 – [[collateral]] Service. 
Viewing the [[ETF]] Eligibility Inquiry
The following figure shows an example of the [[ETF]] Eligibility Inquiry page available to [[ETF]] Agents and 
Authorized Participants. Access the [[ETF]] Dashboard through the Clearing Dashboard available through 
the MyDTCC portal. The [[ETF]] Eligibility Inquiry page will allow users to check [[CNS]] or TFT eligibility on a 
[[CUSIP]] level. This will be detailed in an Exchange Traded Fund ([[ETF]]) Web User Guide for Phase 2 that will 
be published at a later date.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
IntroducingClearingEnhancementsToSupportFixedIncomeAssets
7

---

## Page 8

Determining Eligibility for Fixed Income Components 
T-1 and T
 l In this phase, [[ETF]] agents and APs are able to determine [[CNS]] versus [[NSCC]]/[[DTC]] eligibility on T-1 as 
indicated in the AutoRoute 02261256 PCF output file for Standard, Create, Redeem, Restricted, and 
Rebalance basket types. 
 l On Trade Date (T), [[ETF]] agents and APs can also determine eligibility for Negotiated PCFs through the 
AutoRoute 02261256 PCF output file. [[NSCC]] will transmit the PCF output file in near real-time for nego-
tiated PCFs from 12:30 A.M. through 7 P.M. on trade date.
 l Negotiated PCFs can be submitted beginning at 12:30 A.M. Eastern Time on T, the beginning of the 
Supplemental PCF cycle.
 l At the end of the Supplemental cycle at 12:30 P.M., Negotiated PCFs will still be accepted between 
12:30 P.M. and the opening of the Primary cycle at 2 P.M. Any basket types, other than Negotiated bas-
kets, received during this time frame will be rejected until the start of the Primary cycle at 2 P.M.
 l Negotiated PCFs received after the start of the Primary cycle at 2 P.M. will still be transmitted in near 
real-time through the AutoRoute 02261256 PCF output file through 7 P.M.
The AutoRoute 02261256 PCF output file generated in near real time for negotiated PCFs will be 
available for submissions up until 7 P.M. on T. Negotiated PCFs received after 7 P.M. through the end 
of the Primary cycle will be distributed in the end-of-day Primary cycle distribution of the AutoRoute 
02261256 PCF output file. It is strongly recommended to submit the Negotiated PCFs prior to 
the Negotiated order so that eligibility is determined in advance of the order. [[NSCC]] will 
transmit the Intraday Receipt/Reject report for Negotiated only at 7:00 PM. At that time, 
provisionally accepted [[Bonds]] will be marked as CIL =X in the Cash In Lieu (CIL) indicator on 
the edit report. Fixed Income [[securities]] that are not found in the [[NSCC]] or [[DTC]] Security 
Master database will be rejected on the order submission (DATATRAK Production 
11300/PSE 41300) after 7:00 P.M.
 l The Intraday Edit report will also generate provisionally accepting negotiated PCFs. This report will 
include a warning for all underlying [[ETF]] components that are not found (in the [[DTC]] and [[NSCC]] Security 
Master databases) at the time of submission. The [[ETF]] system pends these [[securities]] and complete a 
check throughout the day to determine if the security was added.
At 7 P.M., a final Intraday Edit report will be generated for only the negotiated PCF with the final 
eligibility for pended components. Eligibility will be [[CNS]], TFT, or marked as CIL =X if not found 
and will subsequently be rejected on the order submission.
 l All other baskets types received during the Supplemental cycle will be delivered through either Near 
Real-Time Supplemental PCF (AutoRoute Production 02262335/ Test 02982335) or at the end of Sup-
plemental cycle through the AutoRoute 02261256 PCF output file.
 l In Phase 2, Negotiated PCFs will be distributed to the submitting agent and authorized [[participant]] des-
ignated in the Type 4-Custom/Restricted Distribution Record for DATATRAK Production 11301/Test 
41301. 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
IntroducingClearingEnhancementsToSupportFixedIncomeAssets
8

---

## Page 9

Still Under Review
 l [[NSCC]] is reviewing developing a real-time (API) view to its Security Master Database (SMD) to determ-
ine the eligibility of the fixed income underlying [[ETF]] components in real-time.
 l [[ETF]] agents and authorized participants that want to gain more data on Bond Eligibility can contact their 
Relationship Manager to inquire about the receipt of ELIS reports. These reports deliver different func-
tionality for requested [[Asset]] types and may need to be used in conjunction with each other to determine 
the [[CNS]], TFT, [[DO]], and [[FAST]] eligibility. For more information, see the following table:
Function Description
ELISC/ELISCD Use the Eligible Corporate [[securities]] (ELISC) and Eligible Corporate [[securities]] with Description (ELISCD) 
functions to receive information about corporate [[securities]] that are eligible for [[DTC]] transactions.
Each record contains the [[CUSIP]] number of a corporate security that is eligible for [[DTC]] transactions and a 
Status byte comprised of flags indicating additional information about the security (such as whether the 
security is a [[FAST]] issue, frozen issue, etc.).
If you require eligible corporate security information in greater detail, the ELISCD function includes a 
corporate security description in each ELISC record. This is the [[BASIC]] difference between the ELISC and 
ELISCD functions.
ELISCA Use the ELISCA function to receive a file of daily changes to the Eligible Corporate Security file, which is 
available in its entirety through the ELISC and ELISCD functions. Each record represents an Addition, 
Deletion, or Replacement of a security on the Eligible Corporate Security file.
ELISM/ ELISMD Use the Eligible Municipal [[securities]] (ELISM) and Eligible Municipal [[securities]] with Description (ELISMD) 
functions to receive information about municipal [[securities]] that are eligible for [[DTC]] transactions.
Each record contains the [[CUSIP]] number of a municipal security that is eligible for [[DTC]] transactions, a 
municipal bond type indicator, and a Status BYTE comprised of a set of flags indicating additional 
information about the security (such as whether the security is a [[FAST]] issue, a frozen issue, etc.).
If you require eligible municipal security information in greater detail, the ELISMD function incorporates a 
municipal security description into each ELISM record. This is the [[BASIC]] difference between the ELISM and 
ELISMD functions.
ELISMA Use the ELISMA function to receive changes to the Eligible Municipal Security file made available (in its 
entirety) by the ELISM and ELISMD functions. Each record represents an Addition, Deletion, or 
Replacement of a security on the Eligible Municipal Security file.
For T-1 and T-eligibility discovery and processing options, see the Eligibility Scenarios table. 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
IntroducingClearingEnhancementsToSupportFixedIncomeAssets
9

---

## Page 10

CORPORATE/MUNI CREATE REDEEM 
PROCESS FLOWS
 l Redeem Order Partial [[CNS]]/TFT Settle
 l Create Order Partial [[CNS]]/TFT Settle
Redeem Order Partial [[CNS]]/TFT Settle
The following figure shows the Workflow 1 – Fixed Income – Corporate and MUNI [[securities]] (Redeem). 
The AP instructs the agent bank to place an order with the [[issuer]] to redeem [[shares]] in Fixed Income [[ETF]] 
containing [[NSCC]] eligible [[securities]] ([[CNS]] and TFT). 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
Corporate/MUNICreateRedeemProcessFlows
10

---

## Page 11

Create Order Partial [[CNS]]/TFT Settle
The following figure shows the Workflow 2 – Fixed Income – Corporate and MUNI [[securities]] (Create). The 
AP instructs the agent bank to place an order with the [[issuer]] to create [[shares]] in Fixed Income [[ETF]] 
containing [[NSCC]] eligible [[securities]] ([[CNS]] and TFT). 
Corporate and MUNI Bond Eligibility for Clearance
Eligibility for Corporate and Municipal underlying components will be easily determined for PCF 
submission of Standard, Create, Redeem, Restricted, and Rebalance baskets on T-1.
Eligibility will be determined for Negotiated baskets submitted on T through the AutoRoute 02261256 PCF 
output file in near real-time. This report will be generated for all baskets received with an [[NSCC]] Portfolio [[ID]] 
that reflects a Negotiated basket.                   
CUSIPs that are not found in the [[NSCC]] and [[DTC]] Security Master databases or in the S&P [[CUSIP]] 
database will be rejected. These rejects will be reported on the intraday edit reports shown below. Use the 
Cash substitution or Add/Remove records 3 and 5 on the [[ETF]] Order file to remedy these rejects.
Enhanced Intraday Consolidated Portfolio Composition Receipt/Reject Print Image 02981955 02261955
Enhanced Intraday Consolidated Portfolio Composition Receipt/Reject Data File 02981255 02261255
While CUSIPs that are not found will be rejected, they will be pended intraday so that if a bond issuance is 
added after the initial submission, it will be eligible that evening. The edit reports will illustrate acceptance 
on the PCF level and a warning will be issued on the not found security intraday. At 7 P.M., if the [[CUSIP]] is 
still not found, it will appear on the Intraday Receipt/Reject   reports and marked as CIL = X in the Cash In 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
Corporate/MUNICreateRedeemProcessFlows
11

---

## Page 12

Lieu (CIL) indicator. These CUSIPs that are not found will subsequently be rejected on the DATATRAK 
Production 11300/PSE 41300 order file.
Eligibility Reporting
ETFs with Corporate and Municipal Bond components that are [[CNS]] eligible or [[NSCC]]/[[DTC]] eligible will be 
reported on the AutoRoute 02261256 file on T-1. Negotiated PCFs received on T will be transmitted in 
near real-time through the PCF output file as outlined in this document. Components (all Fixed Income 
Issue Types) that are eligible at [[DTC]] for Deliver Order ([[DO]]) will be reported on the AutoRoute 02261256 
PCF output file and the Create Redeem Instruction Blotter with the [[settlement]] Location. 
The [[settlement]] locations to be reported will be 1=[[CNS]], 2=TFT, 3=[[GSD]], 4=MBSD, 5=OCC. [[settlement]] 
Locations 3, 4, and 5 will not appear in Phase 2, but they are for future use. Components reported with 
[[settlement]] Location 2= TFT, but not [[CNS]] eligible will generate TFT Receive and Deliver instructions 
RVP/DVP (RO Receive Order/[[DO]] Deliver Order) through the Consolidated Trade Summary reporting 
(MRO – 02042339 and CSV – 02042340). [[CNS]] and [[NSCC]] eligibility indicators will be reported in 
sequence numbers 15 and 16 on the PCF output files (AutoRoute 02261256, 02262335) as shown below.
Previously, the PCF output only displayed the [[CNS]] Eligible Indicator of Y or N. This indicator will be 
replaced with the [[settlement]] Location as per above. It will be reported on the AutoRoute 02261256 PCF 
output file and the Near Real-Time Supplemental PCF AutoRoute 02262335 file in record Type 03, Seq 
15. Access the full file formats from the [[ETF]] Phase 2 Deployment tab. The following figure shows the 
replaced Type 03, Seq 15 for AutoRoute 02261256 and 02262335:
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
Corporate/MUNICreateRedeemProcessFlows
12

---

## Page 13

Reporting Scenarios
 l Y: When [[settlement]] Location (Seq 15) is reported as 1=[[CNS]], Seq 16 is always Y = [[CNS]] eligible.
 l N: When [[settlement]] Location (Seq 15) is reported as 2=TFT, Seq 16 is always N = Not [[CNS]] eligible.
 l Space: When a component identifier is not found in the [[NSCC]] or [[DTC]] security master, [[NSCC]] reports a 
space in the [[settlement]] Location and marks the component as Cash in Lieu.
The Component [[CNS]] Indicator, Seq 16, remains unchanged.
Previously, eligibility was reported in the [[ETF]] Instruction Detail Blotter as [[CNS]] Y or N, this will be replaced 
with the [[settlement]] Location as per above. The [[settlement]] Location field will also be reported on the 
Enhanced [[ETF]] Create and Redeem Instruction Data Output (MRO): AutoRoute Production 
02261254/PSE 02981254 in record Type 05, Seq 13. Access the full file formats from the [[ETF]] Phase 2 
Deployment tab. For an example of the [[settlement]] Location in a print version of the instruction detail 
blotter AutoRoute Production 02261254, see the Print Image Mockup. The following figure shows the 
replaced Type 05, Seq 13 for AutoRoute 02261254:
Reporting of TFT Items
In addition to eligibility reporting on the PCF and Create Redeem Blotter, TFT items will be reported in the 
CTS AutoRoute 02042339 and 02042340. See the [[NSCC]] File Formats for CTS.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
Corporate/MUNICreateRedeemProcessFlows
13

---

## Page 14

Non-[[CNS]] eligible components, when found in the [[DTC]] Security Master database, will be burst on 
Create/Redeem orders as Trade-for-Trade (TFT). The TFT [[securities]] will be reported with the Net Reason 
Code (NRC) 55 on CTS.
CUSIPs assigned as TFT and reported as NRC 55 will be [[Broker]]-to-agent receive and deliver tickets that 
will never be netted so that the original Create/Redeem counterparty is always maintained. This will apply 
to all TFT items regardless of the [[Asset]] type: Fixed Income or [[Equity]]. The NRC will be added to all UTC 
and CTS documentation as NRC 55-Non [[CNS]] [[ETF]] CR/RD. The TFT Non-[[CNS]] components will be 
reported in CTS as Code 55 with the description of 55-TFT, Non [[CNS]] [[ETF]] CR/RD.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
Corporate/MUNICreateRedeemProcessFlows
14

---

## Page 15

ELIGIBILITY SCENARIOS
The table outlines how and when eligibilities are determined and the options for substituting rejected components as well as components that are 
[[DTC]] eligible, which generate trade-for-trade (TFT) Receive and Deliver tickets, if desired.
As per existing functionality, [[NSCC]] will publish on output the last PCF submitted, allowing for updates to fund composition based on eligibility. 
Negotiated baskets submitted on T can also be updated through 7:00 P.M on T. Substituting [[Bonds]] on a negotiated PCF will be supported and 
[[NSCC]] will publish the final basket up until 8:00: P.M. The original Negotiated PCF will be populated with a Transaction [[ID]] that will be matched when 
the DATATRAK Production 11300/PSE 41300 file is submitted. In cases where an update is made to Negotiated baskets, the Transaction [[ID]] will 
remain the same. [[NSCC]] will use the final Negotiated PCF submitted to burst the matching order and will publish the last Negotiated PCF at the end 
of the day on the AutoRoute 02261256 PCF output file and in near real-time up until 7:00 P.M. 
Publishing of the Negotiated basket is optional and will be determined through the use of Record 4 on the PCF file. In Phase 1, the Negotiated 
baskets were not to be published. Yet the [[Option]] to publish to the designated AP (and [[ETF]] Agent) will be introduced in Phase 2 to assist in 
determining eligibility of bond components submitted in Negotiated baskets. The Features for Multiple Basket Types section of the Client Business 
Requirements: Phase 1 — PCF Enhancements for Processing Multiple Basket Types has been updated to reflect the distribution of Negotiated 
baskets for Phase 2. The Phase 2 updates are reflected in the sections below. The following table provides the eligibility PCF 11301 details:
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EligibilityScenarios
15

---

## Page 16

Submission 
Type
Timing Eligibility Sub 
Issue 
Type
Result Actions Comments Reporting
PCF 11301 
 l Standard 
(CR/RD)
 l Rebalance
 l Restricted
T-1 Non-[[CNS]] / Non [[DTC]]
Eligibility available on 
T-1.
N/A Reject  l Substitute 
for Cash 
 l Use 
Record 3 
and 5 to 
add or 
remove.
Rejected Component 
Warned on Edit Reports.
Not published on the 
PCF.
 l [[EOD]] (PCF) 
Receipt/Reject 
02260421
 l Intraday 
Rec/Rej Data 
02261955
 l Intraday 
Rec/Rej 
Report 
02261255
PCF 11301 
 l Standard 
(CR/RD)
 l Rebalance
 l Restricted
T-1 [[CNS]]
Eligibility available on 
T-1.
[[CNS]] 
Eligible
MUNI 310, 
311, 315, 
346, 
CORP 
500,533, 
572, 574, 
575, 577, 
579, 790, 
795
Components 
Published Com-
ponents burst 
to UTC/[[CNS]] 
upon order sub-
mission.
Business as usual 
(BAU)                                                 
[[CNS]] versus Non-[[CNS]] Sub 
Issue types are detailed in 
Appendix A: Sub-Issue 
Types and Eligibility.
Enhanced Consolidated 
AutoRoute 02261256 PCF 
output file.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EligibilityScenarios
16

---

## Page 17

Submission 
Type
Timing Eligibility Sub 
Issue 
Type
Result Actions Comments Reporting
PCF 11301 
 l Standard 
(CR/RD)
 l Rebalance
 l Restricted
T-1 Mix of [[CNS]] and [[DTC]] 
Eligible
Eligibility available on 
T-1.
For the 
[[Broker]]-to-
[[Broker]] 
trade-for-
trade (TFT 
Sub Issue 
Types 
(SIT) list, 
see 
Appendix 
A: Sub-
Issue 
Types and 
Eligibility.
Components 
Published 
MIX of TFT 
and [[CNS]]
Eligible items 
go to [[CNS]] 
[[DTC]] Eligible 
generate 
trade-for-
trade (TFT) 
balance 
orders.
 l Substitute 
Cash for 
TFT items 
(optional)
 l Use 
Record 3 
and 5 to 
add or 
remove.
TFT Balance orders will 
be generated on the 
Consolidated Trade 
Summary with the new 
Net Reason Code (TBD).
 l Enhanced Con-
solidated PCF 
output file: 
AutoRoute 
02261256.
 l [[EOD]] (PCF) 
Receipt/Reject 
02260421.
 l Intraday 
Rec/Rej Data 
02261955.
 l Intraday 
Rec/Rej 
Report 
02261255.
 l Consolidated 
Trade Sum-
mary (CTS) 
02042339, 
02042340.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EligibilityScenarios
17

---

## Page 18

Submission 
Type
Timing Eligibility Sub 
Issue 
Type
Result Actions Comments Reporting
Negotiated PCF
100% [[CNS]] 
T
Negotiated
 l Eligibility 
determined 
through the 
near real-time 
Supplemental 
PCF dis-
tributed for all 
Negotiated 
baskets.
 l Distribution to 
targeted AP 
through Type 
4–Custom Dis-
tribution 
Record.
[[CNS]] 
Eligible
Components 
Published
Components 
burst to 
UTC/[[CNS]] 
upon order 
submission.
Business as usual 
(BAU).                                                 
 l Negotiated PCF 
submission 
from 12:30 A.M. 
through 8:00 
P.M.
 l The near real-
time PCF output 
will be gen-
erated through 
7:00 P.M. 
receipt of Nego-
tiated PCF. The 
near real-time 
PCF output, 
that is available 
for distribution 
to AP, requires 
Type 4–Custom 
Distribution 
Record. 
 l 02261256 
PCF output file 
in near real-
time.
 l Intraday 
Rec/Rej Data 
02261955
 l Intraday 
Rec/Rej 
Report 
02261255
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EligibilityScenarios
18

---

## Page 19

Submission 
Type
Timing Eligibility Sub 
Issue 
Type
Result Actions Comments Reporting
Negotiated PCF
Partial [[CNS]] / TFT
T
Negotiated
Eligibility determined 
through the near real-
time Supplement PCF 
distributed for all 
Negotiated baskets to 
targeted AP through 
Type 4–Custom 
Distribution Record.
N/A [[CNS]] eligible 
go to [[CNS]] 
TFT eligible 
generate 
[[Broker]]-to-
[[Broker]] TFT 
eligible for 
DVP/RVP at 
[[DTC]].
 l Substitute 
Cash for 
TFT items
 l Use 
Record 3 
and 5 to 
add or 
remove.
 l [[Broker]]-to-
[[Broker]] TFT 
items will 
appear on 
Instruction 
Detail Blotter 
02261254 as 
[[NSCC]] Eligible.
 l [[CNS]] and TFT 
components 
use the same 
[[EOD]] pricing to 
allow for In Kind 
Create/Redeem 
transactions.
 l Enhanced Con-
solidated PCF 
output 
02261256.
 l [[EOD]] (PCF) 
Receipt/Reject 
02260421.
 l Intraday 
Rec/Rej Data 
02261955
 l Intraday 
Rec/Rej 
Report 
02261255.
 l Consolidated 
Trade Sum-
mary (CTS) 
02042339, 
02042340.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EligibilityScenarios
19

---

## Page 20

Subsequent Order Processing 11300
The following table provides the subsequent order processing 11300 details:
Submission 
Type
Timing Eligibility Sub Issue 
Type
Result Actions Comments Reporting
Standard 
(CR/RD) 
Rebalance, 
Restricted
T Outright 
Rejects Known 
From PCF and 
Edit Reports 
on T-1
N/A N/A  l Use Record 3 
and 5 to add or 
remove com-
ponents.
 l Substitute 
Cash for the 
rejected item.
 l Rejected 
Component 
Warned on 
Edit reports.
 l Not published 
on the PCF.
 l Current "As 
Of" func-
tionality 
remains in 
effect.
 l Enhanced Con-
solidated PCF 
02261256.
 l [[ETF]] Create and 
Redeem Instruc-
tion Output (Blot-
ter) MRO 
02261254.
Standard (CR/RD) 
Rebalance, 
Restricted
T [[CNS]] N/A Components 
Published and 
burst to UTC / 
[[CNS]] upon 
order 
submission.
Business as usual 
(BAU).                                                 
[[CNS]] [[EOD]] Pricing 
Applied and added to 
Accrued Interest for 
Bursting of Order.
Instruction Output (Blotter) 
MRO 02261254.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EligibilityScenarios
20

---

## Page 21

Submission 
Type
Timing Eligibility Sub Issue 
Type
Result Actions Comments Reporting
Negotiated T [[CNS]] versus 
TFT eligibility 
determine 
through the 
02261256 PCF 
output file in 
near real-time.
For the listing of 
[[Broker]]-to-[[Broker]] 
trade-for-trade 
(TFT) Sub Issue 
Types (SIT), see 
Appendix A: Sub-
Issue Types and 
Eligibility.
Mix of [[CNS]] 
and TFT items 
burst / TFT 
reported 
downstream in 
CTS.
 l Use Record 3 
and 5 to add or 
remove com-
ponents.
 l Substitute 
Cash for TFT 
items.
 l Leave TFT 
BALO in place 
for RVP/DVP.
 l Negotiated 
PCF sub-
mission from 
12:30 A.M. 
through 8:00 
P.M.
 l 02261256 
PCF output 
file will be gen-
erated in near 
real-time 
through 7:00 
P.M. receipt 
of the Nego-
tiated PCF.
 l Near real-
time output 
for distribution 
to AP requires 
Type 4–Cus-
tom Dis-
tribution 
Record.
 l Enhanced Con-
solidated PCF 
02261256.
 l [[EOD]] (PCF) 
Receipt/Reject 
02260421.
 l Intraday 
Rec/Rej Data 
02261955
 l Intraday 
Rec/Rej Report 
02261255.
 l Consolidated 
Trade Summary 
(CTS) 
02042339, 
02042340.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EligibilityScenarios
21

---

## Page 22

Negotiated Basket – Updated from the Phase 1 Client 
Business Requirements Effective for Phase 2
Consider the following items regarding the Negotiated basket shown in the Negotiated Basket table:
 l Sponsor/Agent-requested feature that provides flexibility for order customization.
 l [[ETF]] agents will be issued a single [[NSCC]] Portfolio [[ID]] for Negotiated baskets on new and existing ETFs, 
upon request.                         
 l Negotiated IDs are mapped to the trading [[CUSIP]] and are clearing eligible.                         
 l In Phase 2, the [[Option]] to publish the Negotiated Basket to [[ETF]] Agents and APs will be determined 
through Type 4–Custom Distribution Record. Only a single AP can be designated for each Negotiated 
basket. Due to this constraint, using LIST/ALL on Type 4–Custom Distribution Record will not be per-
mitted. Negotiated Baskets submitted with LIST or ALL will be rejected with the Message Code REJ 
418 – ALL or LIST not valid for Negotiated baskets. 
 l [[NSCC]] will create a subscription for the Negotiated basket and transmit the PCF output in near real 
time to the submitting agent and authorized [[participant]] listed on Type 4–Custom Distribution Record 
for DATATRAK Production 11301/Test 41301. If Type 4–Custom Distribution Record is not 
submitted, the Negotiated PCF will be processed and distributed in near real time only to the [[ETF]] 
agent through the AutoRoute Production 02261256/Test 02981256 record. In addition, warning 
message, WARN 402 – Custom record missing for negotiated basket, is issued.
In Phase 2, updates to Negotiated PCF will be permitted on T through 7:00 PM using the same 
transaction [[ID]]. [[NSCC]] will use the final submission of the same Negotiated PCF / Transaction [[ID]] for 
order bursting and distribution (in cases where Type 4–Custom Distribution Record is submitted). As 
described above, Negotiated PCFs will generate a near real time PCF output file (AutoRoute 
02261256) through 7 P.M. All Provisionally Accepted components will be marked as CIL = X on 
a 7:00 PM run of the Intraday Reject / Receipt Report generated for Negotiated PCFs. After 
7:00 PM all components not found that were marked as CIL = X on the edit report, will 
subsequently be rejected upon order submission (DATATRAK Production 11300/PSE 41300). 
 l Negotiated PCFs will be eligible for extended [[settlement]]. For more information, see Extended Set-
tlement Fixed Income ETFs.                         
 l Multiple Negotiated PCFs can be submitted for the same Negotiated [[NSCC]] Portfolio [[ID]]. This requires a 
unique Transaction [[ID]] in Type 5–Negotiated Record.                         
 l Type 5–Negotiated Record is required on the PCF for all negotiated orders, inclusive of trade date and 
transaction [[ID]].                         
 l Ensure that the Transaction [[ID]] submitted in Type 5–Negotiated Record of the DATATRAK Production 
11301/Test 41301 must match the Transaction [[ID]] on the DATATRAK Production 11300/Test 41300.
 l Negotiated orders will be based on the Creation Unit established in the Security Master Database 
(SMD), which will be used to calculate [[settlement]] of [[ETF]] [[shares]]. Quantity of Units times Creation Unit.
 l Underlying components will not be multiplied by the number of units. The components will be sent to 
[[settlement]] in the quantities submitted.
 l Submitted on trade date from 12:30 A.M. through 8 P.M. Eastern Time
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EligibilityScenarios
22

---

## Page 23

 l PCF output file AutoRoute 02261256 will be transmitted in near real time from 12:30 A.M. through 7 
P.M. Negotiated PCFs received after 7 P.M. will be distributed in the [[EOD]] AutoRoute 02261256 output 
file.
 l As Of submissions are allowable. As Of for same day [[settlement]], for PCF and [[ETF]] Order, must be sub-
mitted prior to 11:30 A.M. Eastern Time. Updates for As Of Negotiated PCF will not be permitted, they 
will be rejected.
 l Reversals follow existing reversal procedures.
 l Eliminates the existing multiple baskets approach using S&P acquired CUSIPs not associated with the 
[[ETF]] trading [[CUSIP]].
 l Clients will be required to adopt usage of this basket type for negotiated Fixed Income ETFs on the cre-
ate/redeem eligible baskets.
 l Retains the user-desired functionality to publish Sponsor-determined mnemonics containing alpha 
characters to allow trading desks to distinguish baskets from one another.
 l Allows [[ETF]] sponsors to distinguish component [[securities]] the fund must acquire/divest in various cir-
cumstances; especially for fixed income ETFs that have the necessary relief to allow order cus-
tomization, yet also inclusive of [[Equity]] ETFs.
 l Limits UW operations maintenance of S&P dummy CUSIPs that are never clearing eligible and cause 
confusion to other internal [[DTCC]] clients / control functions. Dummy [[CUSIP]] IDs are not accepted by 
UW operations upon deployment.
 l [[NSCC]] Portfolio IDs for Negotiated baskets are identified on output with the letter N in position three in 
Sequence 31 of the AutoRoute Production 02261256/Test 02981256 and AutoRoute Production 
02262335/Test 02982335 record layouts, as shown in the following table:
Seq Description Length Start Type Comments
31 Basket Type 2 290 A/N  l 01 = Standard
 l 02 = Restricted
 l 03 = Pricing
 l 04 = Rebalance
 l 05 = Creation
 l 06 = Redeem
 l 07 = Negotiated
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EligibilityScenarios
23

---

## Page 24

Negotiated Baskets
The following table provides the information for the Negotiated baskets:
Negotiated Basket Example
[[ETF]] Ticker ABC
Basket Mnemonic 
(Optional)
N/A
Basket Code/Label 07 / Negotiated
[[ETF]] [[CUSIP]] 123456789
[[NSCC]] Portfolio [[ID]] 01N123456
Primary Cycle Public-
ation Deadline
N/A
Cycle Publication 
Deadline
 l 12:30 A.M. through 8:00 P.M. Eastern Time on T for Near Real-Time 
02261256.
 l 12:30 A.M. through 8 P.M. with distribution to APs when Type 4–Custom 
Distribution Record is submitted.
Carry Forwards w/out 
Primary Receipt
No
Recipients Distributed to single AP through Type 4–Custom Distribution Record .
If Type 4–Custom Distribution Record   is not submitted, PCF will be processed and distributed to the 
submitting [[ETF]] agent, but NOT published to APs.
Clearing Eligible 
(Optional)
Yes
Basket Sizing Per Creation Unit
Cash Only (Optional) No
Eligible [[Asset]] Classes ALL
Unique Transaction [[ID]] Yes
Must match Transaction [[ID]] on the DATATRAK Production 11300/PSE 41300 order.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EligibilityScenarios
24

---

## Page 25

ENHANCED [[ETF]] CREATE AND REDEEM 
INSTRUCTION
The [[ETF]] order processing and submitting the Enhanced [[ETF]] Create and Redeem Instruction Input MRO: 
DATATRAK Production 11300/PSE 41300 will not change in Phase 2. All order file submissions will follow 
the existing schedules and cutoffs. However, the Enhanced [[ETF]] Create and Redeem Instruction Data 
Output (MRO): AutoRoute Production 02261254/PSE 02981254 and Enhanced [[ETF]] Create and Redeem 
Instruction Print Image Report: AutoRoute Production 02260291/PSE 02980291 will include the following 
minor enhancements: 
 l [[settlement]] Location will be added to report components that are not [[CNS]] eligible that will generate 
[[Broker]]-to-[[Broker]] TFT Deliver and Receive Instructions. The [[settlement]] Location indicator is shown in 
the Print Image Mockup. The updated AutoRoute Production 02261254/PSE 02981254 file format is 
available from the [[ETF]] Phase 2 Deployment tab.
 l Fields will also be added to display the accrued interest for each component. These fields will be sub-
mitted in the DATATRAK Production 11300/PSE 41300 file and populated with this value in the 
enhanced AutoRoute Production 02261256/Test 02981256 PCF output file for T1 or T2 Accrued 
Interest in Sequence numbers 12 and 13, as shown in the table. For the full enhanced format, review 
the Client Business Requirements: Phase 1 — PCF Enhancements for Processing Multiple Basket 
Types.
The accrued interest submitted on PCF for the appropriate [[settlement]] cycle will be added to the 
component Settling Price to define the total [[settlement]] Value for each component. The total [[settlement]] 
Value of all components combined, plus or minus the Cash Amount submitted on the order, will equal the 
[[settlement]] value of the [[ETF]] [[shares]], resulting in an In Kind Create or Redeem order. 
After [[ETF]] Phase 2 is deployed, the accrued interest fields in the Type 3–Detail Component Record of the 
Enhanced Consolidated Portfolio Composition Input Data File: DATATRAK Production 11301/Test 41301 
file will be updated as shown in the following table: 
Note
A similar descriptive change will occur for the accrued interest fields in Sequence 20 and 21 for the AutoRoute 
Production 02261256/Test 02981256 and AutoRoute Production 02262335/Test 02982335 output files.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
25

---

## Page 26

Seq Description Length Start Type Comments Required/Optional 
Field
12 Accrued Interest 
Nonstandard [[settlement]]
(Previously called Accrued 
Interest T1)
11 132 N 999,999,999.99 Optional*
*must be numeric or 
spaces
13 Accrued Interest Standard 
[[settlement]]
(Previously called Accrued 
Interest T2)
11 143 N 999,999,999.99 Optional*
*must be numeric or 
spaces
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
26

---

## Page 27

Additionally, the [[NSCC]] Create and Redeem service validates the DATATRAK Production 11300/PSE 
41300 order file upon submission. It also generates the Create Redeem Instruction Detail Blotter that 
reports [[CNS]] and [[NSCC]] eligible components determined upon submission of the PCF file T-1 or T) [[ETF]] 
then transmits trades to Universal Trade Capture (UTC) to effect [[settlement]]. 
UTC confirms eligibility and reports [[CNS]] eligible components through the Consolidated Trade Summary 
(CTS). Non-[[CNS]] eligible components are reported downstream in CTS as [[Broker]]-to-[[Broker]] trade-for-trade 
(TFT) instructions. UTC reports all bond components determined as non-[[CNS]] eligible as TFT in the Non-
[[CNS]] section of the CTS report. These TFT instructions will be reported with a new Net Reason Code. All 
Fixed Income and [[Equity]] components originating from the [[ETF]] market (920) assigned as TFT will be 
reported with the locked in counterparty identified from the order, no netting will be applied. This TFT 
[[Broker]]-to-[[Broker]] reporting will apply to components identified as Fixed Income and Equities. Both Equities 
and Fixed Income components that are Non-[[CNS]] eligible after Phase 2 is deployed, will be reported on 
CTS with NRC 55-Non [[CNS]] [[ETF]] CR/RD. This is also detailed in the Reporting of TFT Items section.
The Print Image Mockup of the enhanced Instruction Detail Blotter reflects the above detailed 
enhancements. The mockup illustrates a fund with six components, five are [[CNS]] eligible, and only one is 
[[NSCC]] eligible (Non-[[CNS]]) that would result in a trade-for-trade deliver order. This simplified print version 
also reflects component Settling Price, Accrued Interest, and [[settlement]] value. The updated AutoRoute 
Production 02261254/PSE 02981254 file format is available from the [[ETF]] Phase 2 Deployment tab.
Print Image Create/Redeem [[ETF]] Blotter Report 
Mockup 
Note: 
The Print Image Create/Redeem Instruction Detail Blotter report (02260291 / 02980291) shown below 
will be expanded from 123 byte length to 153 byte length. [[NSCC]] will update client destinations (for those 
subscribed) to reflect this expanded byte length. No client action is required. This report will not be 
available in PSE/U until early January 2021 when the destinations have been updated. This is a Print 
Image report; therefore, a format is not required, yet it is available upon request.                         
The original mockup in this Phase 2 document did not reflect the changes and new fields for the 
[[collateral]] Service. These original mockups have been replaced with versions that now include [[collateral]] 
payment order records.
The following image shows the print version of the instruction detail blotter for AutoRoute Production 
02261254/PSE 02981254:
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
27

---

## Page 28

 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
28

---

## Page 29

Extended [[settlement]] Fixed Income ETFs
Upon widespread request from the [[ETF]] Working Group, [[NSCC]] will allow for extended [[settlement]] for both 
[[Equity]] and Fixed Income ETFs. Although primarily intended for Rebalance orders, extended [[settlement]] 
will be permitted for all basket types eligible for [[NSCC]]’s Create/Redeem service.
Note
Extended [[settlement]] will be introduced for Equities only, in a separate release shortly after the Phase 1 PCF 
Enhancements are deployed. Extended [[settlement]] for Fixed Income Clearance will not be permitted until deploy-
ment of Phase 2 as [[NSCC]] does not currently clear ETFs with underlying fixed income components.
The [[Equity]] portion of the specifications for extended [[settlement]] is available separately as an addendum in 
the Client Business Requirements: Phase 1 — PCF Enhancements for Processing Multiple Basket Types.
Through discussions at Industry Working Group sessions, it has been clarified that [[ETF]] Agents and APs 
will not know if orders will be placed for extended [[settlement]] on Fixed Income Baskets on T-1 when 
Standard, Restricted, Rebalance, Create Only, and Redeem Only baskets are submitted. To facilitate the 
extended [[settlement]] for Fixed Income Create and Redeem orders, [[NSCC]] will limit orders with extended 
[[settlement]] to Negotiated PCF and associated orders when Fixed Income components are present.
Extended [[settlement]] Equities
Extended [[settlement]] for ETFs with 100% [[Equity]] Components can be submitted against all basket types 
submitted on T-1 (or T Supplemental cycle) as accrued interest is not required.
Extended [[settlement]] Fixed Income
Extended [[settlement]] for ETFs with partial or full fixed income components will be permitted only through 
Negotiated baskets. Orders submitted with extended [[settlement]] against Standard, Restricted, Rebalance, 
Create Only, and Redeem Only baskets will be rejected when any or all components are the Fixed Income 
[[Asset]] type.
The Enhanced [[ETF]] Create and Redeem Instruction Input MRO File: DATATRAK Production 11300/PSE 
41300 file submitted with values 3, 4, or 5 in sequence 10 of the Type 2–Instruction Record for extended 
[[settlement]] will be rejected if the Instruction [[CUSIP]] is a Standard, Restricted, Rebalance, Create Only, and 
Redeem Only basket type and Fixed Income components are present. [[NSCC]] transmits the reject 
message code 541 – Extended [[settlement]] invalid for standard portfolio with   Fixed Income components.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
29

---

## Page 30

The following table show Sequence 10 of the Type 2–Instruction Record details for DATATRAK 
Production 11300/PSE 41300:
DATATRAK Production 11300/PSE 41300 
Type 2–Instruction Record
Record length=300 
Required for all instructions.
Seq DescriptionLength Start Type Comments Required or 
Optional Field
10 [[settlement]] 
Code
1 58 A/N  l Space= [[default]] for Regular 
Way (2 day Regular Way)
 l 1 = Next Day
 l 2 = Regular Way (2 days)
 l 3 = 3 Day [[settlement]]
 l 4 = 4 Day [[settlement]]
 l 5 = 5 Day [[settlement]]
Required
The following table identifies the basket types that are available in Sequence 31 of the AutoRoute 
Production 02261256/Test 02981256 and AutoRoute Production 02262335/Test 02982335 record 
layouts:
Type 2 – Portfolio Header Record
Seq Description Length Start Type Comments
31 Basket Type 2 290 A/N  l 01 = Standard
 l 02 = Restricted
 l 03 = Pricing
 l 04 = Rebalance
 l 05 = Create Only
 l 06 = Redeem Only
 l 07 = Negotiated
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
30

---

## Page 31

Accrued Interest
This section describes the population of the Accrued Interest fields in Sequence 12 and 13 available in the 
Enhanced Consolidated Portfolio Composition Input Data File: DATATRAK Production 11301/Test 41301 
record layout for all basket types and all [[settlement]] codes (see the table for Sequence 10).
To facilitate the extended [[settlement]] for Fixed Income [[Asset]] types, the descriptions for sequence 12 and 
13 will change after [[ETF]] Phase 2 is deployed, as outlined in the following table:
Note
A similar descriptive change will occur for the accrued interest fields in Sequence 20 and 21 for the AutoRoute 
Production 02261256/Test 02981256 and AutoRoute Production 02262335/Test 02982335 output files.                 
D A T A T R A K  P r o d u c t i o n  1 1 3 0 1 / P S E  4 1 3 0 1 
Type 3–Detail Component Record
Record length=450
Seq Description Length Start Type Comments Required or Optional 
Field
12 Accrued Interest Nonstandard 
[[settlement]] 
(Previously called Accrued 
Interest T1)
11 132 N 999,999,999.99 Optional*
*must be numeric 
or spaces
13 Accrued Interest Standard 
[[settlement]]
(Previously called Accrued 
Interest T2)
11 143 N 999,999,999.99 Optional*
*must be numeric 
or spaces
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
31

---

## Page 32

Rules and Edits
[[ETF]] Agents must populate Accrued Interest as per below rules to ensure accurate calculation of total 
[[settlement]] value for each underlying Fixed Income component.
Standard, Restricted, Rebalance, Create Only, and Redeem 
Only Baskets for Fixed Income
 l Populate Accrued Interest in Sequence 12 for Next Day [[settlement]] (Nonstandard) for Fixed Income 
underlying components. (Extended [[settlement]] value 3, 4, or 5 in sequence 12 will be rejected for these 
basket types).
 l Populate Accrued Interest in Sequence 13 for Regular Way (two day) [[settlement]] for Fixed Income 
underlying components.
 l Orders received against Standard, Restricted, Rebalance, Create Only, and Redeem Only basket 
types with extended [[settlement]] will be rejected when the Fixed Income underlying components are 
present.
 l [[NSCC]] will generate a WARN message for components when accrued interest is not populated. In 
these instances, [[NSCC]] will calculate the Total [[settlement]] value of the component by multiplying 
[[shares]] times End of Day Price without the accrued interest. 
 l Accrued Interest should be calculated and submitted as per these rules based on the [[settlement]] Date. 
In instances where accrued interest is not submitted, it can be accounted for in the Cash Component in 
the order.
Negotiated Baskets Accrued Interest Fixed Income
 l Extended [[settlement]] will be permitted for Fixed Income baskets only through Negotiated PCFs.
 l Populate Accrued Interest in Sequence 12 for Next Day and when 3, 4, or 5 days [[settlement]] is expec-
ted. 
 l Accrued Interest to be populated in Sequence 13 when Regular Way (2 Day) [[settlement]] is expected.
 l Accrued Interest should be calculated and submitted as per these rules based on the [[settlement]] Date. 
In instances when accrued interest is not submitted, it can be accounted for in the Cash Component in 
the order.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
32

---

## Page 33

Message Codes
Based on the rules outlined above, [[NSCC]] issues reject and warning messages through the following 
reports, as outlined in the table:
 l Record layout - Enhanced [[ETF]] End of Day Create/Redeem Receipt/Reject Report 02980098 
02120098
 l Enhanced [[ETF]] Intraday Create/Redeem Receipt/Reject Report 02981954 02261954
 l End of Day Portfolio Composition File (PCF) Receipt/Reject ([[ETF]] Agent Only) 02980421 02260421
 l Enhanced Intraday Consolidated Portfolio Composition Receipt/Reject Print Image 02981955 
02261955
 l Enhanced Intraday Consolidated Portfolio Composition Receipt/Reject Data File 02981255 02261255
See also New Message Codes. For a full list of the [[ETF]] Message Codes, see [[ETF]] Guides.
Record Layout Message 
Type
Message 
Code
Record 
Type
Field File 
Type
Description
Enhanced Consolidated Portfolio 
Composition Input Data File: 
DATATRAK Production 11301/Test 
41301
WARN 346 3 12 PCF Accrued interest is 
not required for 
[[Equity]] component.
WARN 347 3 13 PCF Accrued interest is 
not provided for fixed 
income component.
Enhanced [[ETF]] Create and Redeem 
Instruction Input MRO File: 
DATATRAK Production 11300/PSE 
41300
REJ 541 2 10 C/R Extended [[settlement]] 
invalid for the 
Standard portfolio 
with   Fixed Income 
components.
WARN 346 5 6 C/R Accrued interest is 
not required for 
[[Equity]] component.
WARN 347 5 6 C/R Accrued interest is 
not provided for fixed 
income component.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
33

---

## Page 34

Accrued Interest Calculations
[[NSCC]] will calculate the total [[settlement]] value for Create and Redeem Orders using the accrued interest 
submitted in Sequence 12 and 13 on the Enhanced Consolidated Portfolio Composition Input Data File: 
DATATRAK Production 11301/Test 41301. [[ETF]] agents are responsible for submitting accrued interest 
properly, allowing for accurate calculations of the Total [[settlement]] Value that are sent to [[CNS]] and/or TFT 
items submitted by [[ETF]] agents and APs for [[settlement]].
Note
For [[Bonds]], you multiply by the factor rate; however, for stocks, there is no factor included. 
Standard Baskets, Restricted, Rebalance, Create and 
Redeem Baskets Fixed Income
For Nonstandard settlements (next day), [[NSCC]] sources the accrued interest from Sequence 12, 
Accrued Interest Nonstandard [[settlement]].                   
Nonstandard Next Day Calculation for Order Bursting: 
 l Factor included for [[Bonds]]:
 l Factor not included for stocks:
Note
Accrued Interest is populated in total for each component. [[NSCC]] includes accrued interest when calculating units.                 
For Standard [[settlement]] Regular Way (two day [[settlement]]), [[NSCC]] sources the accrued interest from 
Sequence 13, Accrued Interest Standard [[settlement]].                 
Standard [[settlement]] Regular Way Calculation for Order Bursting: 
 l Factor included for [[Bonds]]:
 l Factor not included for stocks:
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
34

---

## Page 35

Note
Accrued Interest is submitted for each component not the total accrued for Quantity times Price. [[NSCC]] will add 
Accrued interest to the end of day price and then multiply by Share Quantity and by Units.
Print Image Mockup: Standard Basket Accrued Interest
Note
The original mockup in this Phase 2 document did not reflect the changes and new fields for the [[collateral]] 
Service. These original mockups have been replaced with versions that now include [[collateral]] payment order 
records.
The following image shows the print version of the instruction detail blotter for AutoRoute Production 
02261254/PSE 02981254:
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
35

---

## Page 36

Negotiated Baskets Calculations
For Negotiated Baskets submitted for next day or extended [[settlement]], [[settlement]] Codes equal to one, 
three, four, or five day [[settlement]], [[NSCC]] sources the accrued interest from Sequence 12 for nonstandard 
[[settlement]].
Units will not be calculated for components on Negotiated baskets as Share Quantities are sent to 
[[settlement]] based on the share quantity submitted. To obtain the Total [[settlement]] value, multiply Share 
Quantity by the End of Day Price and add to the accrued interest submitted in Sequence 12, Accrued 
Interest Nonstandard [[settlement]].
Nonstandard Negotiated Basket Calculation for Order Bursting:
For Negotiated baskets submitted with the [[settlement]] Code of Space, 0, or 2 (for Regular Way - two day 
[[settlement]]), [[NSCC]] sources accrued interest from Sequence 13, Accrued Interest Standard [[settlement]].                 
Units will not be calculated for components on Negotiated baskets as Share Quantities sent to [[settlement]] 
are based on share quantity submitted. To obtain the Total [[settlement]] value, multiply Share Quantity by 
the End of Day Price plus Accrued Interest submitted in Sequence 13, Accrued Interest Standard 
[[settlement]].                 
Standard Negotiated Calculation for Order Bursting 
 l Factor included for [[Bonds]]:
 l Factor not included for stocks:
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
36

---

## Page 37

Print Image Mockup: Negotiated Fixed Income Basket 
Accrued Calculation
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
37

---

## Page 38

Accrued Interest Sourcing 
The following table reinforces the accrued interest sourcing outlined above:
Seq Description Length Start Type Comments Required/Optional 
Field
12 Accrued Interest 
Nonstandard 
[[settlement]]                                                 
11 132 N 999,999,999.99
 l As Of Same Day 
Settling
Standard Basket
 l No Extended 
[[settlement]]
 l Next Day Set-
tlement when 
[[settlement]] Code 
equals 1= Next 
Day                                                                 
Negotiated Basket
Next Day [[settlement]] when 
the [[settlement]] Code 
equals:                                                 
 l 3=Three Day 
[[settlement]]                                                                 
 l 4=Four Day Set-
tlement
 l 5= Five Day Set-
tlement
 l Not required 
for Equities.
 l Required for 
Fixed Income.
When [[settlement]] Code 
equals 1= Next Day                                                 
 
Negotiated Basket
 l 3=Three Day 
[[settlement]]                                                                 
 l 4=Four Day 
[[settlement]]                                                                 
 l 5= Five Day 
[[settlement]]                                                                 
*must be numeric or 
spaces
13
Accrued Interest 
Standard 
[[settlement]]
11 143 N 999,999,999.99
Standard Basket
Regular Way (2 Day 
[[settlement]])
 
Negotiated PCF
Space= [[default]] for 
Regular Way (two day 
Regular Way)                                                 
 l Not required 
for Equities.                                                                 
 l Required for 
Fixed Income.                                                                 
*must be numeric or 
spaces
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
38

---

## Page 39

Accrued Interest Type 5-Custom Added Components 
Record
[[NSCC]] has updated the Enhanced [[ETF]] Create and Redeem Instruction Input MRO: DATATRAK 
Production 11300/PSE 41300 file to account for the accrued interest for Fixed Income components added 
with order submission. As the component add is on the order file, only one Accrued Interest field is 
required. The [[settlement]] Code is also provided; therefore, [[NSCC]] will use only this field to calculate the 
Total [[settlement]] value.
Calculation for Order Bursting
[[NSCC]] will source the accrued interest from Sequence 6 of the Type 5-Custom Added Components 
Record, as highlighted in red in the table. [[NSCC]] will add the Accrued Interest to the Total [[settlement]] 
value. Accrued Interest must be submitted as a total value, and it will not be multiplied by Units.
DATATRAK Production 11300/PSE 41300 
Type 5–Custom Added Components Record 
Record length=300
Note: Optional for all instructions.
Seq DescriptionLength Start Type Comments Required or 
Optional 
Field
1 Record Type 2 1 A/N 05 = Record Type 5
One for each component added to the 
instruction.
Required
2 Transaction 
[[ID]]
12 3 N Identifies the Create/Redeem instruction being 
modified by this custom addition (should equal 
Transaction [[ID]] in Record Type 2).
Required
3 Component 
Code
2 15 A/N  l 01=[[CUSIP]]
 l 03=ISIN
 l 04=ISIN/SEDOL
Required
4 Component 
[[ID]]
25 17 A/N Defined by the Component Code. Required
5 Component 
Quantity
13 42 N Weighted share of this component in the portfolio Required
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
39

---

## Page 40

DATATRAK Production 11300/PSE 41300 
Type 5–Custom Added Components Record 
Record length=300
Note: Optional for all instructions.
Seq DescriptionLength Start Type Comments Required or 
Optional 
Field
6 Accrued 
Interest 
11 55 N Accrued interest to be used for Fixed Income 
components in 999999999.99 format.
Optional*
*must be 
numeric or 
spaces.
7 Future Use 235 66      
END OF RECORD
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
40

---

## Page 41

[[Margin]] Impact/Clearing Fund and VaR Calculator
In the current environment, Create and Redeem activity for [[ETF]] funds with Fixed Income components is 
transacted ex-clearing, outside of [[NSCC]]. The process is likely labor-intensive, requiring manual 
Deliver/Receive orders as well as [[collateral]] tracking and reconciliation.                   
The maximum benefit would be to provide In Kind clearance for 100% of Fixed Income, including the 
[[NSCC]] Trade Guarantee and netting through [[CNS]]. Yet due to the vast universe of Corporate and 
Municipal [[Bonds]] and wide classifications, many underlying components are not eligible for [[CNS]]. This 
results in partial clearance through [[CNS]] and partial [[Broker]]-to-[[Broker]] TFT Receive and Delivers through 
[[DTC]].                 
[[NSCC]] has reviewed the impact to [[Margin]] and Clearing Fund requirements for these hybrid 
Create/Redeem orders using a newly introduced VaR calculator within the [[NSCC]] Risk portal. [[NSCC]] ran 
the VaR calculator using a single [[ETF]] funds underlying components, which were a high percentage [[CNS]]-
eligible with a small portion TFT-eligible.                   
The model on a single Create order is quite simplified. Although it did not include all components and 
activity required to calculate Clearing Fund requirements, it revealed that partial [[CNS]] with TFT orders [[DO]] 
not have any adverse effect on Clearing Fund and [[Margin]]. [[ETF]] Fixed Income components that are not 
[[CNS]] eligible and go through TFT are not included in [[NSCC]] Risk management controls, and they may 
reduce the required [[collateral]] collected by [[NSCC]] for [[Margin]] purposes. [[ETF]] agents and APs need to 
maintain current [[collateral]] collection and monitoring for the TFT items not guaranteed by [[NSCC]].                 
Reducing manual Deliver and Receive [[obligations]] and collection of [[collateral]] on those [[obligations]] 
combined with the [[NSCC]] Trade Guaranty on [[ETF]] [[shares]] and [[CNS]] eligible underlying [[shares]] should be a 
benefit to [[ETF]] agents and APs. [[NSCC]] will provide access to the Risk portal and VaR calculator to all 
relevant stakeholders and encourages using the tool to quantify these benefits.                   
Although the Risk portal has already been introduced to most members, the user guides for Clearing Fund 
Calculation and the Risk portal will be distributed under separate cover along with information about how 
to gain access to the tool. A live demo of the VaR Calculator and [[NSCC]] Risk Portal was given at the 
October 9, 2019 [[ETF]] Industry Working Group session.                 
Benefits
 l Provides a standardized In Kind Create and Redeem transaction through [[NSCC]].                                                           
 l Adds accrued interest at the component [[securities]] level, reducing the need for cash substitution within 
eligible baskets and reducing reconciliation at [[settlement]] for APs.                                                           
 l Simplifies [[settlement]] reconciliation, reducing in manual deliver and receive instructions.                                                           
 l Reduces in [[collateral]] collection and tracking.                                                           
 l CCP guarantee provides balance sheet relief.                                                         
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
EnhancedETFCreateAndRedeemInstruction
41

---

## Page 42

ADDENDUM PHASE 2 – [[collateral]] 
SERVICE
[[NSCC]] has engaged with business and technology representatives from [[ETF]] agents and authorized 
participants (APs) in several forums, including the [[NSCC]] Trade Capture and [[ETF]] Industry Working 
Groups (IWG). [[NSCC]] has solicited feedback to develop requirements to provide a [[collateral]] collection 
service for non-[[CNS]] eligible (TFT) Fixed Income and [[Equity]] [[securities]] that pass through the primary 
market creation / redemption service. 
[[ETF]] Industry [[participant]] requested that [[NSCC]] develop this service in conjunction with Phase 2 Clearance 
of Fixed Income ETFs to allow for full collateralization of non-[[CNS]] Trade-for-Trade (TFT) [[securities]]. 
Through analysis of [[Bonds]] submitted to [[NSCC]]’s portfolio composition file (PCF) service and the 
development of above Phase 2, it has become clear that not all Fixed Income components are [[CNS]] 
eligible. (See eligibility section above).
This addendum to Phase 2 will detail requirements for [[ETF]] agents and authorized participants to fully 
collateralize [[securities]] that are non-[[CNS]] eligible. The newly developed [[collateral]] Service, initially focused 
on Fixed Income, yet through collaboration at working groups, it has been developed to include all non-
[[CNS]] eligible components, including equities and fixed income. Therefore, all [[ETF]] Agents and Authorized 
participants will be required to develop and implement this service.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
42

---

## Page 43

The following figure is a mid-level description of the new [[collateral]] service. Reporting of eligibility has been 
specified in the Phase 2 requirements. This addendum ties together both Fixed Income Clearing   and 
reporting of eligibility with the [[collateral]] service.
The numbers in the figure correspond to the following [[ETF]] workflow:
 1.  APs consummate an order with the [[ETF]] Sponsor, which is then transmitted to [[NSCC]] by the [[ETF]] 
Agent Bank through submission of the [[ETF]] Create and Redeem Instruction Input MRO: DATATRAK 
Prod 11300 file. 
[[NSCC]] will store the industry determined [[default]] [[Haircut]] percentage to calculate [[collateral]] and   will 
also provide the ability to update the percentage by fund and by contra through a new field on the 
11300 order file.                   
 2.  [[ETF]] validates order and bursts to UTC.
 a. Eligibility check of components done on PCF on T-1 or T for negotiated.
 b. UTC will use PCF eligibility and send components to [[CNS]], if eligible.
 c. Noneligible components will generate a TFT ticket in the CTS system as new Net Reason Code 
(NRC) 55. All NRC 55 reason codes will be Agent to [[Broker]] with no netting.                                                   
 d. TFT tickets generated to the CTS will include the Net [[settlement]] amount which is plus or minus   
the payment order amount depending on the direction of the order: Create or Redeem.                                                 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
43

---

## Page 44

 3.  [[ETF]] will also generate the Instruction Detail Blotter Print report (review below mockup) and the [[ETF]] 
Create and Redeem Instruction Output MRO: AutoRoute Production 02261254 file.                                 
 l [[CNS]] eligible and TFT components will include Accrued Interest sourced from PCF (standard or 
nonstandard [[settlement]]).                                                 
 l Eligibility on the Instruction Detail Blotter Print report and MRO 02261254 will be reported as   
[[settlement]] Location.                                                 
 o 1 = [[CNS]]
 o 2 = TFT
 l [[ETF]] will calculate the [[Haircut]] amount for non-[[CNS]] eligible components multiplying industry 
[[default]] percentage times total [[settlement]] amount. The total [[settlement]] amount equals quantity 
times the end-of-day price plus accrued interest from PCF. 
 l Create and Redeem Instruction Output MRO: AutoRoute Production 02261254/PSE 02981254 
will include:
 o New section for the individual Payment Order Amounts by [[CUSIP]] of the underlying 
component.                                                                   
 o Total Payment Order Amount.                                                                 
 o Individual PO amounts in Record 5 (Review MRO specs) and Total PO amount in Record 
02.
 l [[ETF]] will calculate and report the Net [[settlement]] amount on Instruction Detail Blotter as well as 
downstream to UTC and CTS inclusive of the payment order amount.                                                 
 l Net [[settlement]] value will include the payment order amount for creations and will deduct the 
payment order amount for redemptions.
 l [[ETF]] will calculate and report a new [[settlement]] price for the Net [[settlement]] Value after the 
payment order amount is added or deducted.                                                   
 l On Creation orders, the authorized participants will submit DVPs for the full [[settlement]] amount 
inclusive of the [[collateral]] payment order amount that will reclaim the [[collateral]] paid through a 
payment order.                                                 
 l On Redemption orders, [[ETF]] agent banks will submit DVPs for the full [[settlement]] amount minus 
the payment order amount so that APs can reclaim the [[collateral]].                                                 
 4.  During this step, the:
 l [[ETF]] system will calculate the payment order amount for collection of [[collateral]] based on an 
Industry determined [[Haircut]] percentage.                                                 
 l Payment orders will always be a debit to APs for both Creation and Redemption orders.
The figure and steps are mid-level descriptions of the workflow. Full specifications are detailed in the 
subsequent sections.                 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
44

---

## Page 45

Eligibility
Review the eligibility section of the Phase 2 requirements above. [[CNS]] eligibility is determined upon receipt 
of the portfolio composition file on T-1 or on T for Negotiated PCF or Supplemental PCF. Reporting of 
eligibility on PCF, [[ETF]] Clearing Dashboard, and [[ETF]] Create Redeem Instruction Detail Blotter is detailed 
in the original Phase 2 document. The Create/Redeem [[ETF]] Blotter Report Mockup will report final 
eligibility upon processing of the order.                 
Eligibility Changes Inter-[[settlement]] Cycle         
It is possible that a [[CNS]] eligible security can be exited from [[CNS]] processing after trade date but prior to 
[[settlement]] date. In this scenario the [[CNS]] items are reported as Multilateral Balance Orders and will 
appear on the [[CNS]] Miscellaneous Activity report [[CNS]] Miscellaneous Activity (Extended) MRO: 
AutoRoute [[ID]] 02040343 (Night) and 02040331 (Day) Although these [[securities]] are exited from [[CNS]] they 
will not be included in the [[collateral]] Service. They will continue to be guaranteed through [[settlement]] Date 
and will be reported as Multilateral Balance Orders.
[[NSCC]] will continue to review for inclusion in the [[collateral]] service in subsequent releases if possible.
Calculation and Reporting of Payment Orders for 
Collateralization of TFT [[securities]]         
[[NSCC]] will store a [[default]] [[Haircut]] percentage for calculation of [[collateral]] requirement for [[securities]] that are 
reported as trade-for-trade (TFT), non-[[CNS]] eligible. The [[collateral]] amount will be collected by [[ETF]] Agents 
from APs through Payment Orders generated from the [[ETF]] system to [[DTC]] [[settlement]]. This 
collateralization was requested by [[ETF]] Agents and APs to reduce risk and will provide operational 
efficiencies for [[collateral]] reconciliation currently in place for orders created and redeemed ex-clearing.                 
December 4, 2020 Update: [[NSCC]] has reviewed the [[Haircut]] percentages for collateralization with 
the  [[ETF]] agents and authorized participants. It has been determined that the [[default]] [[Haircut]] 
percentage rate will be 20%.         
Additionally, the [[ETF]] agent community has agreed to bypass the [[Haircut]] override functionality. 
All trade-for-trade [[securities]] will be collateralized at the industry [[default]] rate of 20%. [[NSCC]] will 
monitor the rate at Industry Working Groups to determine if any changes are required.         
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
45

---

## Page 46

Create/Redeem [[ETF]] Blotter Report Mockup
This section shows a mockup of the print image version of the [[ETF]] Create and Redeem Instruction Print Image Report: AutoRoute Production 
02260291.
Note
This mockup represents a Negotiated Creation order. As detailed in Phase 2 Specifications above, component share quantities on Negotiated orders are not 
multiplied by units.
The mockup is not to be used for format purposes. Each section has been labeled for illustrative purposes.
Section 1
The following figure shows an excerpt from the [[ETF]] Blotter Report mockup. In Section 1, the component value, cash amount, and assigned [[ETF]] 
value are provided. This does not change. Component Value plus or minus (±) Cash Amount equals (=) the value assigned to the [[ETF]] [[shares]] for 
[[settlement]].
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
46

---

## Page 47

Section 2
The following figure shows Section 2, which contains new fields to facilitate the [[settlement]] of fixed income:
 l [[CNS]] and [[NSCC]] eligibility records have been replaced by the [[settlement]] location (SETT LOC). 
 o 1 = [[CNS]]
 o 2 = Trade-for-Trade
 l Accrued interest (ACCRUED INT) has been added and will be taken from PCF input. 
In the example below the total component value 36,993.280000CR plus or minus the cash amount from Section 1 will be assigned as the 
[[settlement]] Value for the [[ETF]] [[shares]].
Section 3
The following figure shows Section 3, which has not been modified. It shows the quantity and assigned [[settlement]] value of the [[ETF]] [[shares]]. The 
[[settlement]] values depicted in SECTIONS 1, 2, and 3 represent the In-Kind [[settlement]] value for a creation or redemption order. 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
47

---

## Page 48

Section 4
The following figure shows a new section that details the individual, total payment order, and [[settlement]] value that is reported downstream. For an 
example of the full [[ETF]] Blotter report, see the figure below. 
This Payment Orders section includes only [[securities]] reported as TFT. 
 l [[settlement]] Value represents the original In-Kind [[settlement]] value for components prior to Payment Order.
 l [[Haircut]] represent the percent applied to calculate the payment order for collection of [[collateral]].
 l Payment Order Amount represents the calculation of the original In-Kind component [[settlement]] value times the [[Haircut]] percentage. The 
individual component [[Haircut]] values will be reported with the component [[CUSIP]]/ISIN.
 l Net Settling Price will be calculated at the request of the industry and represents the price at which the TFT [[securities]] will be reported to UTC 
plus or minus (±) the Payment Order Amount.
 o Instruction Detail Blotter mockups show reporting to the [[ETF]] Agent Bank. APs receive the same report with component and [[ETF]] values 
moving in opposite directions. The examples provided assume that the [[Seller]] of underlying components will book the DVP transactions.
 o On Creations the Payment Order Amount will be added to the Net [[settlement]] Value allowing APs to reclaim [[collateral]] when booking 
DVPs.
 o On Redemptions the Payment Order Amount will be deducted to the Net [[settlement]] Value. [[ETF]] Agents when booking DVPs for 
components will in effect be returning [[collateral]].
Note
TFT [[securities]] will be reported to UTC with the Net [[settlement]] Value and Price; however, the price is not carried to the Consolidated Trade Summary (CTS) sys-
tem. The Net Settling Price can be sourced from the Instruction Detail Blotter or from UTC output. Most APs receive the UTC output in near real-time or through the 
MRO file. Firms interested in subscribing for UTC output should contact NSCCIntegration@[[DTCC]].com. 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
48

---

## Page 49

Full Print Image Create/Redeem Instruction Detail Blotter
The following image shows a sample full Print Image Create/Redeem Instruction Detail Blotter:
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
49

---

## Page 50

Sample Create/Redeem [[ETF]] Blotter Reports
This section provides additional samples of the Print version of the Create/Redeem [[ETF]] Blotter report. 
Note
There are slight reporting differences for [[ETF]] agents compared with authorized participants. The Debits and Credits listed are reversed for authorized participants. 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
50

---

## Page 51

Standard Creation – Authorized Participants
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
51

---

## Page 52

Standard Creation – [[ETF]] Agents
 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
52

---

## Page 53

Negotiated Creation – Authorized Participants
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
53

---

## Page 54

Negotiated Creation – [[ETF]] Agents         
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
54

---

## Page 55

Standard Redemption – Authorized Participants         
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
55

---

## Page 56

Standard Redemption – [[ETF]] Agents         
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
56

---

## Page 57

Negotiated Redemption – Authorized Participants
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
57

---

## Page 58

Negotiated Redemption – [[ETF]] Agents
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
58

---

## Page 59

Create/Redeem Instruction Detail MRO
The above reports represent a print version of the Create/Redeem [[ETF]] Blotter report. The [[ETF]] Create and 
Redeem Instruction Data Output (MRO) for AutoRoute Production 02261254/PSE 02981254 file has been 
updated to include all new fields as described in the section. This section shows excerpts of the file 
formats. View the full format available from the [[ETF]] Phase 2 Deployment tab.
The following table show the new field for the Type 2–Instruction Record details for the 02261254/PSE 
02981254 file: 
AutoRoute Production 02261254/PSE 02981254 
Type 2–Instruction Record 
Record length=300 
Seq Description Length Start Type Comments
32 Total Payment Order Amount 12 264 N 9,999,999,999.99
The following table show only the new fields for the Type 5–Components Record for the 02261254/PSE 
02981254 file:     
AutoRoute Production 02261254/PSE 02981254
Type 5–Components Record
Record length=300 
Note: Optional for all instructions.
Seq Description Length Start Type Comments
13 [[settlement]] Location 1 107 A/N  l 1 = [[CNS]]
 l 2 = TFT
 l 3 = [[GSD]]*
 l 4 = MBSD*
 l 5 = OCC*
*Future enhancement. 
 
22 Accrued Interest 11 185                                                 N 999,999,999.99
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
59

---

## Page 60

AutoRoute Production 02261254/PSE 02981254
Type 5–Components Record
Record length=300 
Note: Optional for all instructions.
Seq Description Length Start Type Comments
23 Component Payment Order Amount 11 196                                                 N 999,999,999.99
24 Net Settling Price 16 207                                                 N 9,999,999,999.999999
25 Net [[settlement]] Value 20 223                                                 N 99,999,999,999,999.999999
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
60

---

## Page 61

[[ETF]] Create and Redeem Instruction Input MRO: 
DATATRAK 11300
The [[ETF]] Create and Redeem Instruction Input MRO: DATATRAK Production 11300/PSE 41300 file has 
been updated to include the [[Haircut]] Percentage field. As described above, [[NSCC]] will calculate a [[Haircut]] 
percent for collateralization of TFT non-[[CNS]] eligible [[securities]]. [[NSCC]] will calculate this amount using an 
industry determined [[Haircut]] percentage, which will be a [[default]] rate. The addition of this field on the Create 
and Redeem Instruction input file will allow [[ETF]] agent banks to adjust or update the [[default]] percentage. If 
this field is received on the 11300 instruction file, [[NSCC]] will use the submitted percentage to calculate the 
[[Haircut]] for collateralization. 
The following table shows the new field for the Type 2–Instruction Record of the DATATRAK Production 
11300/PSE 41300 file. View the full format available from the   [[ETF]] Phase 2 Deployment tab.
DATATRAK Production 11300/PSE 41300
Type 2–Instruction Record 
Record length=300
Required for all instructions.
Seq Description Length Start Type Comments
19 [[Haircut]] Percentage 2 110 N [[Haircut]] Percentage
Format: 99
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
61

---

## Page 62

New Message Codes
The following table provides the new message codes for the [[Haircut]] Percentage field. For a full list of 
message codes, see the [[ETF]] Message Codes in the Learning Center. 
 
Message Types
 l Reject = REJ = R
 l Warning = WARN = W
 l Informational = INFO = I
File Type
 l PCF = Portfolio Composition File
 l Both = Information applies to both 
PCF and Create/Redeem file types.
Message Description
 l FX = Foreign exchange
Message 
Code
Message 
Type 
Record 
Type
Field File 
Type
Message Description
291 REJ 2 19 PCF Cash only pricing basket.
295 WARN 3 19 C/R [[Haircut]] percentage is invalid. 
318 WARN 3 N/A PCF Component provisionally accepted.
319 WARN 3 N/A PCF Security added after the Trade Date. The cash in lieu 
(CIL) indicator is set to X.
320 WARN 3 4 PCF Component [[ID]] Check digit is invalid.
346 WARN 5 6 C/R Accrued interest is not required for the [[Equity]] 
component. 3 12 PCF
347 WARN 5 6 C/R Accrued interest is not provided for the fixed income 
component. 3 13 PCF
348 WARN 3 N/A PCF Baby [[Bonds]] not eligible for clearance. 
378 WARN 3 12 PCF Nonstandard accrued interest is invalid. 
379 WARN 3 13 PCF Standard accrued interest is invalid. 
402 WARN 2 N/A PCF Custom record missing for the Negotiated basket. 
418 REJ 4 3 PCF All or List is not valid for the Negotiated basket. 
419 REJ 4 N/A PCF More than one Custom record for the Negotiated basket. 
420 WARN 2 N/A PCF No valid distribution record for the Negotiated basket. 
421 WARN 2 N/A PCF Only one custom record is required for the Negotiated 
basket. 
422 REJ 5 N/A PCF Updates to the subscriber are not allowed for the Nego-
tiated portfolio.
525 REJ 3 and 5 N/A C/R Missing instruction record.
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
62

---

## Page 63

Message 
Code
Message 
Type 
Record 
Type
Field File 
Type
Message Description
531 REJ 5 3 PCF Update on the As Of Negotiated basket is not allowed.
541 REJ 2 10 C/R Extended [[settlement]] invalid for the Standard portfolio 
with Fixed Income components. 
542 WARN 5 6 C/R Accrued interest is invalid.
600 WARN 2 N/A PCF All components are provisionally accepted.
601 WARN 2 N/A PCF One or more component is provisionally accepted.
602 REJ 3 and 5 4 C/R One or more components are not in the security master 
database (SMD). 
603 REJ 5 N/A C/R Order with baby [[Bonds]] not eligible for clearance. 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
63

---

## Page 64

Payment Orders Processing
As described above, [[NSCC]] has developed a [[collateral]] Collection service to reduce exposure and risk 
associated with non-[[CNS]] eligible [[securities]] that trade-for-trade (TFT) [[securities]] are due for [[settlement]] as 
a result of a creation or redemption order. The calculation fully detailed in this document will be processed 
through a Special Payment Order (SPO) generated from the [[ETF]] system to [[DTC]] [[settlement]]. TFT 
[[securities]] that are not part of the [[NSCC]] Central Counterparty Guarantee can now be part of a Create or 
Redeem order with full collateralization.                 
 l SPOs also referred to as Payment Orders will be available through the following output methods:                                 
 o DTF PART PO
 o ICM MQ
 o ISO 15022 [[settlement]] Message
 o MDH
 l Payment Orders will be displayed in output with the Reason Code SF/805 – Description- [[ETF]] TFT 
[[collateral]].                                 
 l The Payment Orders detailed herein will always be generated by [[NSCC]]. [[participant]] input in these 
reason codes will be blocked.                                   
 l In [[settlement]] Web the output reason code that you will receive is 805. The Alpha reason code SF will 
be displayed in the Comments section. See Mockup.                                 
 l Output reason code that you will receive is 805 or SF, depending on the type of output you consume.   
If you receive SPOs through:                                 
 o PART PO – Reason code SF will be displayed.
 o MDH – Reason code SF will be displayed.
 o MQ – Reason code SF will be displayed.
 o DTFMTX – Reason code 805 will be displayed.                                                 
 l Payment Orders statuses will be displayed on the [[settlement]] Web Activity Inquiry screen.                                 
 l Payment Orders calculated by the [[ETF]] system on the Trade Date will be transmitted to [[DTC]] on the 
morning of the [[settlement]] Date at approximately 2:30 A.M Eastern Time and will be submitted for pro-
cessing immediately at [[DTC]].   The transaction will settle immediately if the transaction passes [[DTC]] risk 
controls (funds/[[collateral]] available in the payor’s [[collateral]] group); otherwise, it will pend until valued 
[[settlement]]. The Payment Orders will immediately be visible to the APs and [[ETF]] agents listed on the 
Create Redeem order.
 l Payment Orders will always be transmitted to [[DTC]] on the [[settlement]] Date regardless of the [[settlement]] 
cycle.                                 
 l Reason Code SF/805 will bypass RAD (Receiver Authorized Delivery).                                 
 l Reason Code SF/805 are subject to [[DTC]] Risk controls ([[collateral]] Monitor, Debit Cap).                                 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
64

---

## Page 65

 l Reason Code SF/805 is not actionable. The [[settlement]] Web will not provide any [[Option]] for Pend com-
mands (Pend Hold, Pend Cancel, Pend Hold with Blockage, Pend Release, and Activate).                                 
 l All [[settlement]] screens where it allows you to submit reclaimable actions are blocked.                                 
 l In the case that a payor cannot meet [[settlement]], the Payment Orders follow the existing procedures for 
deposits.                                 
 l Unsettled (pended) Payment Orders will DROP at [[settlement]] (approximately 3:30 P.M. Eastern Time) 
and will not be introduced. The payee and payor need to reconcile this difference when the com-
ponents are delivered.                                 
 l Funds are guaranteed to the payee when Payment Orders are in MADE status.                                 
 l POs, with Reason Code SF/805 generated by [[ETF]], will follow the [[settlement]] Holiday calendars. 
Create and Redeem also follow this same calendar.                                 
 l All [[Haircut]] payment orders will be calculated at the industry determined [[default]] rate of 20%.                                 
[[NSCC]] assumes that all [[ETF]] agents and authorized participants already receive payment orders through 
one of the above mentioned output protocols. To check the output protocol/location, firms can contact 
DTCSupport@[[DTCC]].com. Firms requiring new set ups for receipt of purchase orders should contact 
DTCIntegration@[[DTCC]].com.                   
For questions regarding the Payment Order transmission protocol (MDH, PARTPO, ISO), contact 
DTCSupport@[[DTCC]].com. The Payment Orders generated by [[NSCC]] will also be displayed on [[settlement]] 
Web (MyDTCC portal) and Activity Inquiry screens. Contact your firm’s super access coordinator (SAC) 
for access to these applications. The SAC can contact DTCIntegration@[[DTCC]].com for provisioning of these 
applications.                 
Mockup
The following mockup shows the 805 reason code on [[settlement]] Web. 
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
65

---

## Page 66

Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AddendumPhase2–CollateralService
66

---

## Page 67

APPENDIX A: SUB-ISSUE TYPES AND 
ELIGIBILITY
Note
 l Yellow highlighted items have been submitted to [[ETF]] and are included in the fund by fund listing.
 l *TFT – These sub-issue types (SITs) are frequently listed as [[DTC]] eligible for the Deliver and Receive, 
yet some of these items may require Fed delivery.
Sub-Issue Type                     Description [[ETF]] Processing                     
010  Common [[Stock]]                                           [[CNS]]                                         
011                                           Convertible Common [[Stock]]                                           [[CNS]]                                         
12                                         Common [[Stock]] REIT                                         [[CNS]]                                         
020                                           Preferred [[Stock]]                                         [[CNS]]                                         
22                                         Preferred [[Stock]] REIT                                         [[CNS]]                                         
23                                         Convertible Preferred [[Stock]]                                         [[CNS]]                                         
024                                         Tender Rate Preferred [[Stock]]                                         [[CNS]]                                         
040                                         CMO Denom in "Units" or "Undivided Interest"                                         TFT                                         
041                                           [[ABS]] Denom in "Units" or "Undivided Interest"                                           TFT                                         
042                                           Issue Denom in "Units" or "Undivided Interest"                                           TFT                                         
102                                           Auction Rate Preferred [[Stock]] (ARPS)                                         TFT                                         
110                                         American Depositary Receipt ([[ADR]])                                         TFT                                         
111                                         Depositary Share                                           TFT                                         
112                                         Municipal [[Option]] Call Right                                           TFT                                           
117                                         Exchange Traded Funds                                           [[CNS]]                                         
120                                         MMI Preferred [[Stock]] (in CP-like mode)                                           N/A                                         
125                                         Sealed Envelope                                         N/A                                         
126                                         [[custody]] User [[CUSIP]]                                           N/A                                         
130                                         Real-Estate Investment Trust (REIT)                                           TFT                                         
310                                         Municipal Bond                                           [[CNS]]                                         
311                                         Municipal Note                                           [[CNS]]                                         
312                                         Municipal Auction Rate Note (ARN)                                         TFT                                         
313                                         Municipal Variable Mode Obligation (VMO)                                         TFT                                         
314                                         Municipal Variable Rate Demand Obligation (VRDO)                                         TFT                                         
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AppendixA:Sub-IssueTypesAndEligibility
67

---

## Page 68

Sub-Issue Type                     Description [[ETF]] Processing                     
315                                         Municipal Insured Custodial Receipt                                         [[CNS]]                                         
320                                         MMI Municipal VRDO/CP                                           TFT                                         
330                                         MMI Municipal Commercial Paper                                         TFT                                         
340                                         Bearer, Callable Zero-Coupon Bond                                           TFT                                         
346                                         Other Tax Exempt                                         [[CNS]]                                         
450                                         GNMA REMIC [[securities]]                                           *TFT                                         
451                                         GNMA Pass-Through [[securities]]                                           *TFT                                         
452                                         GNMA Serial Note [[securities]]                                           *TFT                                         
500                                         Corporate Bond (CB) or Global Corp Bond (GCB)                                         [[CNS]]                                         
502                                         MMI Bankers' Acceptance Note (BA)                                           TFT                                         
504                                         MMI Institutional Certificates of Deposit                                           TFT                                         
505                                         Certificated Money Market Instrument                                           TFT                                         
506                                         Certificated Money Market - Periodic Payer                                           TFT                                         
507                                         Certificates of Deposit                                         TFT                                           
525                                         MMI Corporate Commercial Paper                                           TFT                                         
526                                         MMI Corporate VRDO/CP                                           TFT                                         
530                                         MTN Medium Term Note                                           TFT                                         
531                                         MMI Deposit Note                                         TFT                                         
532                                         MMI Medium-Term Bank Note                                           TFT                                         
533                                         MMI Medium Term Note                                           [[CNS]]                                         
540                                         Collateralized Mtge Obligation or Global CMO                                           TFT                                         
541                                         [[Asset]]-Backed Security ([[ABS]]) or Global [[ABS]] (GABS)                                           TFT                                         
542                                         Non-CMO/[[ABS]] Amortizing Issue                                           TFT                                         
550                                         MMI Short-Term Bank Note                                           TFT                                         
551                                           Z CPN Denom in Initial Principal Amt                                           TFT                                         
560                                           MMI Discount Note                                           TFT                                         
571                                           Corporate Auction Rate Note                                           TFT                                         
572                                           Convertible Corporate Debt                                         [[CNS]]                                         
573                                           Corporate Variable Mode Obligation (CVMO)                                         TFT                                         
574                                           Corporate Short-Term Note                                           [[CNS]]                                         
575                                           Corporate Debenture                                           [[CNS]]                                         
576                                           Corporate VRDO                                           TFT                                         
577                                           Corporate Insured Custodial Receipt                                           [[CNS]]                                         
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AppendixA:Sub-IssueTypesAndEligibility
68

---

## Page 69

Sub-Issue Type Description [[ETF]] Processing 
578                                          Tender Rate Note                                           TFT                                        
579                                          Zero Coupon Bond                                           [[CNS]]                                        
601                                          Government Security                                           *TFT
602                                          Government Trust Certificate                                           *TFT
610                                          US Treasury Security                                           *TFT
611                                          US Treasury Bill                                           *TFT
612                                          US Treasury Note                                           *TFT
613                                          US Treasury Bond                                           *TFT
620                                          US Government Agency Security                                          *TFT
700                                        Package                                           *TFT
704                                        Corporate Debt Derivative                                           TFT                                        
705                                        [[Equity]] Derivative                                           *TFT
706                                        Municipal Derivative                                           *TFT
708                                        Municipal Amortized Issue                                           TFT                                        
720                                        Warrant                                           TFT                                        
730                                        Right                                           TFT                                        
760                                        Mutual Fund                                           TFT                                        
761                                        Closed End Fund                                           TFT                                        
762                                        (IMMI) Institutional MMI Mutual Fund [[shares]]                                          TFT                                        
780                                        [[Equity]] Unit                                           TFT                                        
781                                        Debt Unit                                           TFT                                        
790                                        Unit Investment Trust ([[UIT]]) - Nuveen Only                                          [[CNS]]                                        
795                                        Unit Investment Trust ([[UIT]])                                           [[CNS]]                                        
Phase 2: Clearing Enhancements to Support Fixed Income Assets for Corporate, Municipal, and [[UIT]] (CMU)
Appendix A: Sub-Issue Types And Eligibility
69

---

## Page 70

APPENDIX B: GLOSSARY
The following table shows the glossary of terms used in the document:
Term Definition
[[ABS]] [[Asset]] Backed [[securities]]
[[ADR]] American Depositary Receipt 
ARPS Auction Rate Preferred [[Stock]]
CMO Collateralized Mortgage Obligation
[[DO]]  Deliver Order
PCF Portfolio Composition File
RO  Receive Order
RVP / DVP Receive/Deliver verse Payment
SMD Security Master Database 
[[NSCC]] and [[DTC]] Security Master files
SIT Sub Issue Types [[DTC]] classifications of Corp Debt Instruments
TFT Trade-for-trade 
[[Broker]]-to-[[Broker]] (no netting)
Phase2:ClearingEnhancementstoSupportFixedIncomeAssetsforCorporate,Municipal,andUIT(CMU)
AppendixB:Glossary
70

---

## Page 71

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), and the Interlocker graphic are registered and  
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust 
& Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate 
legal entity, subject to the laws and regulations of the particular country or countries in which such entity operates. 
Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Doc Date: October 02, 2023
Publication Code: ETF231
Service: Exchange Traded Fund ([[ETF]])
Title: Client Business RequirementsPhase 2: Clearing Enhancements to Support Fixed Income Assets for Corporate, Municipal, 
and [[UIT]] (CMU)
For More Information
Email [[DTCC]] Learning at:
DTCCLearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com