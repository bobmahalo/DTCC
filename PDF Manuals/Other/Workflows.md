---
title: "Workflows.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Workflows.pdf"
pages: 10
size: "541.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Workflows.pdf

**Original File:** [Workflows.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Workflows.pdf)  
**Category:** Other  
**Total Pages:** 10  
**File Size:** 541.9 KB  

---

## Page 1

1/29/24, 6:13 PM Workflows
https://dtcclearning.com/products-and-services/itp/ctm/workflows.html 1/10
VISIT [[DTCC]].COM
LEARNING CENTER
PORTALS CONTACT US
 
GTR APAC Notifications 26-Jan-2024
GTR ASIC REWRITE: ASIC TRADE MIGRATION SPECIFICATION was posted on 24-Jan-2024GTR ASIC/MAS REWRITE: ASIC USAGE GUIDELINES was updated on 24-Jan-2024GTR ASIC/MAS REWRITE: MAS MESSAGE SPECIFICATION was updated on 25-Jan-2024
GTR ASIC/MAS REWRITE: FUNCTIONAL CHANGE DOCUMENT was updated on 25-Jan-2024GTR ASIC/MAS REWRITE: ASIC MESSAGE SPECIFICATION was updated on 25-Jan-2024
WORKFLOWSHOMEINSTITUTIONAL TRADE PROCESSINGCTM®
CTM Workflows
In the CTM workflow, matching occurs firstly between block messages and then between allocations/confirms. The block level
workflow allows investment managers and [[Broker]]/dealers to tie trades to their upstream workflows providing better parity between
front and back office systems. 
The standard workflow is known as the Block Allocation Confirmation Workflow (BACW) and further details on how this works can be
found immediately below. In order to accommodate different market and/or [[Asset]]-class requirements, there are a number of
alternative workflows available which are outlined after the Block Allocation Confirmation Workflow.
 
 
Block Allocation Confirmation Workflow
 BookmarkOctober 06, 2021
ON THIS PAGE
BLOCK ALLOCATION CONFIRMATION WORKFLOW
US-SPECIFIC WORKFLOWS
STEPOUTS
SEPARATELY MANAGED ACCOUNT (SMA)


---

## Page 2

1/29/24, 6:13 PM Workflows
https://dtcclearning.com/products-and-services/itp/ctm/workflows.html 2/10
1. Both investment manager and [[Broker]]/dealer submit their block and allocation messages to CTM for matching.
2. The ALERT platform can be used to enrich standing [[settlement]] instructions (SSIs) to the trade information provided by the
submitting organizations. Please visit Enrichment to learn more about the different options available to enrich SSIs.
3. Once the block matches successfully, CTM proceeds to match the allocations.
4. Once all allocations are successfully matched, CTM sends updated statuses to the internal systems of both organizations.
5. If the investment subscribes to the ITP [[settlement]] Instruction Manager service, [[settlement]] messages for matched allocations are
created and sent to the identified [[Custodians]] and third parties.
 
US-Specific Workflows
The below workflow diagrams demonstrate the way in which our clients are currently processing US trades: using CTM and
TradeSuite [[ID]] with auto-affirmation, and CTM Match to Instruct (M2i) workflow to leverage no-touch processing.
EXPAND ALL COLLAPSE ALL
CTM Auto-Affirmation (USDA)

---

## Page 3

1/29/24, 6:13 PM Workflows
https://dtcclearning.com/products-and-services/itp/ctm/workflows.html 3/10
 
Workflow steps
1. The IM and [[Broker]] send their trade details to CTM for matching. Users can manage their matching exceptions through a
variety of interfaces.2. ALERT enriches both the [[Broker]] and IMs SSIs to the trades.
3. Once the trades match, updated statuses are sent back to both the [[Broker]] and IM.
4. Optional step: [[settlement]] Instruction Manager sends SWIFT/CSV messages to custodian/third parties with [[settlement]]
instruction details
5. CTM sends the matched allocation details to TradeSuite [[ID]].6. The [[Broker]] sends their confirms to TradeSuite [[ID]].
7. TradeMatch compares the CTM allocations with the brokers' confirms and auto-affirms the matched confirms.  IMs can
use Nearmatch to manage any exceptions and Confirm/Affirm to view their process confirms. 
8. Copies of the affirmed confirms are distributed to all parties and staged to settle at [[DTC]].
For more information please refer to the CTM: Match to Instruct (M2i) and AutoAffirmation: Implementation Guide forInvestment Managers
CTM Match to Instruct (M2i)

---

## Page 4

1/29/24, 6:13 PM Workflows
https://dtcclearning.com/products-and-services/itp/ctm/workflows.html 4/10
CTM Match to Instruct (M2i) is a workflow in CTM that automatically triggers trade affirmation and the delivery of [[DTC]] eligible
[[securities]] directly to the [[DTC]] for [[settlement]] when a trade match occurs between an investment manager and executing
[[Broker]]. This workflow helps eliminate the need for either party to take further action. Clients utilizing the M2i workflow benefitfrom central matching and auto-affirmation in comparison to the standard workflow which involves local matching and
affirmation by the custodian or institution.  
Further information: visit Match to Instruct to learn more about the M2i workflow and onboarding checklists.
To learn more about CTM M2i status codes visit CTM Product Help.
Straight to Match (STM) is a process within the CTM auto-affirmation workflow that allows investment managers to submit
trades to non-CTM [[Broker]]/dealers or those CTM [[Broker]]/dealers that [[DO]] not yet trade in the given [[Asset]] class in CTM.
Straight to Match (STM)

---

## Page 5

1/29/24, 6:13 PM Workflows
https://dtcclearning.com/products-and-services/itp/ctm/workflows.html 5/10
 
Stepouts
The below diagram demonstrates the way in which our clients are currently processing Stepouts using the CTM block
allocation/confirmation workflow. 
A video describing how to take action on stepout/stepin trades is available here.
Workflow steps
1. The IM send their trade details to a non-CTM [[Broker]] in CTM with the Executing [[Broker]] PartyType = STMB. Users can
manage their matching exceptions through a variety of interfaces.
2. CTM accepts the trade and interprets it as Straight to Match for Auto-Affirmation and assigns the applicable workflowmodifiers
3. Once the trades match, updated statuses are sent back to the IM.
4. ALERT enriches the IMs SSIs to the trades.
5. Optional step: [[settlement]] Instruction Manager sends SWIFT/CSV messages to custodian/third parties with settlementinstruction details
6. CTM will send the matched allocation details to TradeSuite [[ID]].
7. The [[Broker]] sends their confirms to TradeSuite [[ID]].
8. TradeMatch compares the CTM allocations with the brokers' confirms and auto-affirm the matched confirms.  IMs can use
Nearmatch to manage any exceptions and Confirm/Affirm to view their process confirms. 9. Copies of the affirmed confirms are distributed to all parties and staged to settle at [[DTC]].
For more information please refer to the  CTM Straight to Match (STM): Overview and Best Practices (316 KB)

---

## Page 6

1/29/24, 6:13 PM Workflows
https://dtcclearning.com/products-and-services/itp/ctm/workflows.html 6/10
Workflow steps
1. The IM sends a block with allocation 1 to the executing [[Broker]] and allocation 2 for the stepin [[Broker]] in CTM.  The Executing
[[Broker]] will send their trade details to CTM for matching. Users can manage their matching exceptions through a variety of
interfaces.  
2. ALERT enriches both the [[Broker]] and IMs SSIs to the trades.3. Once the trades match, updated statuses are sent back to both the [[Broker]] and IM.
4. When the trade is Match Agreed (MAGR), CTM will create a new trade with block 2 and allocation 2 that's sent to the Stepin
[[Broker]].  
5. The Stepin [[Broker]] sends their trade details to CTM for matching with the IM. 
CTM matching process for Stepouts at the allocation level (TradeDetail) requires L1 pairing fields for QuantityAllocated and
AllocationIsSteppedOut. To learn more about L1 pairing visit Matching Process.
 
Separately Managed Account (SMA)
A Separately Managed Account is an investment portfolio owned by an [[investor]] and managed by a professional investment firm (RIA).
Investment managers send SMA trades over CTM with commissions/fees to [[Broker]] [[Custodians]]. A subset of SMA [[Broker]] [[Custodians]] on
CTM are unable to send in commissions and fees which can cause mismatches between both parties. To assist with this challenge,
CTM allows investment managers (RIAs) to relax matching on commissions, fees, and net cash amount for SMA trades.
Investment managers (RIAs) who send SMA trades can create SMA specific matching profiles that are [[Asset]] specific with the naming
conventions SMA-DBT-[[default]] and/or SMA-EQT-[[default]] in the CTM Client Facing Dashboard and select which fields to matchon.  The Dashboard can be accessed through the MyDTCC portal and further information on using the Dashboard can be found in
the Client Facing Dashboard menu.
CTM will automatically invoke the [[Asset]] specific SMA profile, if present and based on the CTM's matching profile selection hierarchy,
when the executing [[Broker]] on the trade has the Return SMA Matching Profile Override Value (RSOV) Subscription [[Option]] set to Y-
Yes. If the correct SMA matching profile is not present, the traditional CTM matching profile hierarchy will be invoked to determine therelevant matching profile for the trade.

---

## Page 7

1/29/24, 6:13 PM Workflows
https://dtcclearning.com/products-and-services/itp/ctm/workflows.html 7/10
Please note, a SMA profile should not have a specific currency associated with it. To enable the RSOV Subscription [[Option]], the CTM
Product Administrator for the SMA [[Broker]] custodian can submit a MyDTCC support request.
Prior to sending SMA trades over CTM Investment managers will need to create the SMA matching profile for [[Equity]] and/or debt.
IM (RIA) creates a SMA Matching Profile selecting which fields to match on. For more information on how to create a Matching
Profile, visit Client Facing Dashboard to view our instructional videos. 
Below is a suggested Matching Profile for USD trades, using min/max for price, total trade amount, and trade amount.  If sending
cross border trades, it is suggested to use % tolerance for price, total trade amount, and trade amount (.001 % for a tolerance).
 
 
The SMA Matching Profile is invoked when an IM places trades while using the SMA matching profile. If the IM does not create a SMA
matching profile, the currency specific or [[default]] match profile will be invoked.
[[Broker]] enables SMA subscription [[Option]]. A [[Broker]]'s CTM Product Administrator can submit a case a support request through
MyDTCC to enable this subscription [[Option]].
SMA Matching Profile (MP) is invoked in preference to standard MP when trading with SMA brokers with SMA subscription optionSupported for [[Equity]] including stepouts and options
[[Broker]] Matching Groups (BRMG) are out of scope
Tolerance match allocations are passed to TradeSuite for AutoAffirmation BAU
Investment managers will have their financial values returned on the InfoSettlementResponse as the [[settlement]] values if the SMA-
DBT-[[default]]/SMA-EQT-[[default]] matching profile is used. A subscription [[Option]] is not required.
TotalTradeAmount TradeAmount
TotalNetCashAmount NetCashAmount
TotalSettlementAmount SettlementAmount
InfoSettlementResponseTradeLevel(ISRTL) Common Value Fields InfoSettlementResponseTradeDetail(ISRTD) Common Value Fields

---

## Page 8

1/29/24, 6:13 PM Workflows
https://dtcclearning.com/products-and-services/itp/ctm/workflows.html 8/10
RECOMMENDED FOR YOU
TotalAccruedInterestAmount AccruedInterestAmount
TradeCommFeesTaxes CommFeesTaxes
TradeCommissions Commissions
TradeChargesOrTaxes ChargesOrTaxes
 
A USDA investment manager trading an SMA account will have the following fields submitted to TradeMatch with the [[settlement]]
values they provided if the SMA-DBT-[[default]]/SMA-EQT-[[default]] matching profile is used. A subscription [[Option]] is not required.
 
BuySellIndicator AccountID
TypeOfFinancialInstrument TradeAmount
DealPrice NetCashAmount
Amount SettlementAmount
TradeDateTime AccruedInterestAmount
SettlementDate Commissions
 ChargesOrTaxes
InfoSettlementResponseTradeLevel(ISRTL) Common Value Fields InfoSettlementResponseTradeDetail(ISRTD) Common Value Fields
InfoSettlementResponseTradeLevel(ISRTL) Common Value Fields InfoSettlementResponseTradeDetail(ISRTD) Common Value Fields
ALERT KEY AUTO SELECT (AKAS)
READ MORE
ALERT Key Auto Select (AKAS)functionality enables rules-basedenrichment of CTM trades with preferredSSIs sourced from the ALERT platform.…
STANDARD ALERT ENRICHMENT
READ MORE
Enrichment using the standard ALERTenrichment process enables bothbroker/dealers and investment managers toselect which SSI should be enr…
CTM MANUAL INMANAGER - ONB
READ MORE
The below onboardweek-by-week guidcompleted by both ythe [[DTCC]] to ensu…


---

## Page 9

1/29/24, 6:13 PM Workflows
https://dtcclearning.com/products-and-services/itp/ctm/workflows.html 9/10
Institutional Trade Processing
Equities Clearing
Fixed Income Clearing
[[Asset]] Services
[[settlement]]
Mutual Fund Services
Alternative Investment Product Services
Insurance & Retirement Services
Repository Services
[[Derivatives]] Services
Data Services
My Dashboard
My Profile
My Subscriptions
Learning Center Navigation Guide
About [[DTCC]] Learning
About [[DTCC]]
Business & Subsidiaries
Our Stories
[[DTCC]] Connection
Press Releases
Careers
Important Notices
Registration/Login Inquiries
Request [[DTCC]] Learning Support
Client Support Contact
United States 1.888.382.2721
International 1.212.855.8099
PRODUCTS & SERVICES ON THE LEARNING CENTER
PERSONALIZING YOUR LEARNING EXPERIENCE
ABOUT
LEARNING CENTER CONTACT
[[DTCC]] CLIENT CONTACT
PORTALS

---

## Page 10

1/29/24, 6:13 PM Workflows
https://dtcclearning.com/products-and-services/itp/ctm/workflows.html 10/10
MyDTCC
MyDTCC-EMEA
API Marketplace
ITP Products
Important Notices
United States: 1-888-382-2721
International: +1-212-855-8099
   
Cookie Preferences
Contact Us
Privacy Policy
Terms & Conditions
Copyright 2024 [[DTCC]]. All Rights Reserved.
By Subsidiary
By Products & Services
CONTACT