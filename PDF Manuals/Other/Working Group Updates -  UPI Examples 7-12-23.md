---
title: "UPI Examples"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Working%20Group%20Updates%20-%20%20UPI%20Examples%207-12-23.pdf"
pages: 4
size: "206.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# UPI Examples

**Original File:** [Working Group Updates -  UPI Examples 7-12-23.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Working%20Group%20Updates%20-%20%20UPI%20Examples%207-12-23.pdf)  
**Category:** Other  
**Total Pages:** 4  
**File Size:** 206.1 KB  

---

## Page 1

North America Working Group – July 12, 2023
GTR North America Re-Write – UPI Examples

---

## Page 2

[[DTCC]] Public (White)
• There are no cross validations for [UPI] between message types (Trade State, Valuation, PPD). Firms 
are responsible to submit the correct [UPI] for regulatory compliance.
• [UPI] will NOT be merged from Valuation reports to Trade State reports. 
Example 1:
UPI validations for Trade State, PPD and Valuation 
Message Type Action Type UTI Trade Party 1 Trade Party 2 UPI
Trade State NEWT UTI123 LEIABC LEIDEF UPI123
Message Type Action Type UTI Trade Party 1 Trade Party 2 UPI
RT (PPD) NEWT UTI123 LEIABC LEIDEF UPI789
Message Type Action Type UTI Trade Party 1 Trade Party 2 UPI
Valuation VALU UTI123 LEIABC LEIDEF UPI456
Submission 1
Result: UTI123 is submitted as a new (NEWT) trade for Trade State and accepted. UPI123 is a valid UPI and 
will appear on Trade State Reports. 
Submission 3
Result: A valuation is submitted for UTI123 and accepted Note: Valuations w ill only be accepted if there is a 
base trade w hich matches the valuation submission (UTI/USI + Trade Party 1 + Trade Party 2 + Jurisdiction). 
UPI456 is a valid UPI and will appear on the Valuation Activity Report. UPI123 will continue to be reported on 
Trade State Reports. Valuation submissions w ill NOT update the [UPI] on Trade State Reports.
Submission 2
Result: UTI123 is submitted as a new (NEWT) trade for PPD and accepted. UPI789 is a valid UPI and will 
appear on PPD reports. UPI123 will continue to be reported on the Trade State Report for this UTI.

---

## Page 3

[[DTCC]] Public (White)
Example 2:
Modifying a UPI
• [UPI] is NOT part of Trade Uniqueness. [UPI] can be updated in subsequent submissions. 
• The latest [UPI] submitted will be used for reporting. DDR will not update the [UPI] or related UPI data 
elements until a subsequent message is submitted and processed. 
Msg Type Submission Date Action Type UTI Trade Party 1 Trade Party 2 UPI UPI-Instrument 
Type 
(Outbound)
Trade State 2/1/2024 NEWT UTI123 LEIABC LEIDEF UPI123 [[Option]]
Submission 1
Result: UTI123 is submitted as a new trade for Trade State and accepted. UPI123 is a valid UPI and will appear on Trade 
State Reports. UPI data element [UPI-Instrument Type] changes from ‘[[Option]]’ to ‘Swap’ on 2/5/23. Trade State Reports 
will continue to report [UPI-Instrument Type] as ‘[[Option]]’
Result: The MODI is accepted for UTI123. Trade State Reports will show [UPI-Instrument Type] as ‘Swap’ based on 
the latest UPI data pulled from ANNA-DSB.
Submission 2
Submission 3
Result: The CORR for UTI123 is accepted to correct the previous UPI. UPI456 is a valid UPI and will be reported on the 
Trade State Report.
Msg Type Submission Date Action Type UTI Trade Party 1 Trade Party 2 UPI UPI-Instrument 
Type 
(Outbound)
Trade State 2/10/2024 MODI UTI123 LEIABC LEIDEF UPI123 Swap
Msg Type Submission Date Action Type UTI Trade Party 1 Trade Party 2 UPI UPI-Instrument 
Type 
(Outbound)
Trade State 2/14/2024 CORR UTI123 LEIABC LEIDEF UPI456 [[Option]]

---

## Page 4

[[DTCC]] Public (White)
Example 3:
Submissions with the same UPI Data Elements and [[CFTC]] Tech Spec 
fields
• There are no cross validations for [UPI] between data elements and other [[CFTC]] Technical 
Specification fields. Firms are responsible to submit the correct [UPI] for regulatory compliance.
Submission 1
Msg Type Action 
Type
UTI Trade Party 1 [[Asset]] Class Notional 
Currency
UPI UPI-[[Asset]] 
Class 
(Outbound)
UPI-Notional 
Currency
(Outbound)
Trade State NEWT UTI123 LEIABC Credit USD UPI123 [[Equity]] EUR
Result: UTI123 is submitted as a new (NEWT) trade for Trade State and accepted. UPI123 is a valid UPI and will 
appear on Trade State Reports. 
Although the submitted [[Asset]] Class and Notional Currency (‘Credit’ and ‘USD’) are different from the UPI data 
elements reported from ANNA-DSB for similar fields (UPI-[[Asset]] Class and UPI-Notional Currency), there are no 
cross validations performed. 
UTI123 will appear on the Credit Trade State Report. Any calculations performed (e.g. Large Size Trade, etc.) will 
be based on the [[Asset]] Class(Credit)  and Notional Currency(USD) submitted if required in the logic. 