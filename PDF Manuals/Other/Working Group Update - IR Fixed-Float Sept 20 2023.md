---
title: "WG - IR Fixed Float"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Working%20Group%20Update%20-%20IR%20Fixed-Float%20Sept%2020%202023.pdf"
pages: 5
size: "189.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# WG - IR Fixed Float

**Original File:** [Working Group Update - IR Fixed-Float Sept 20 2023.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Working%20Group%20Update%20-%20IR%20Fixed-Float%20Sept%2020%202023.pdf)  
**Category:** Other  
**Total Pages:** 5  
**File Size:** 189.4 KB  

---

## Page 1

[[DTCC]] Internal (Green)
North America 
Re-Write Phase 2
North America Working Group – Sept 20, 2023

---

## Page 2

[[DTCC]] Internal (Green)
2
FOR DISCUSSION: IR Fixed - Float Reporting Scenario 
Background: The [[CFTC]] Tech Spec states the validations should be placed in leg 1. In the IR Fixed-Float Swap scenario, the 
firm would like to report the fixed leg in Leg 1 and the floating leg in Leg 2. Due to the validations in leg 1, this would make the 
floating leg [Floating rate reset frequency period-leg 1] required in Leg 1 along with the fixed leg details. 
[[Asset]] 
Class
Inbound Field
Outbound field for [[participant]] 
Submission Report Only
Outbound Field
Rules -
Trade 
State for 
NEWT, 
MODI, 
CORR, 
REVI
Rules -
PPD 
for NE
WT, 
MODI, 
CORR, 
REVI
Business Rules (Inbound Field Names) FIRM Submission 
Example: DDR Comments:
CO, CR, 
IR
Leg 1 - Fixed Rate Initial Fixed rate-Leg 1 C C IR
- Required if [Leg 1 - Spread Amount] is not populated and [Post-
priced swap indicator] = ‘False’, and UPI.[Instrument type] ≠ ‘[[Option]]’, 
else {blank} 
0.035025
IR Reset Frequency Period 1 Floating rate reset 
frequency period-leg 1
C C Required if UPI.[Instrument type] = ‘Swap’ and UPI.[Underlier 
type] ≠ ‘Fixed -Fixed’, else {blank}
When populated with ‘EXPI', [Reset Frequency Period Multiplier 1] 
must be ‘1’
NULL
NACK: A value will be 
required because this is 
an IR SWAP and it is 
Fixed-Floating
CO, CR, 
EQ, IR
Leg 1 - Spread Amount Spread-Leg 1 C C IR
- Required if [Leg 1 - Fixed Rate Initial] is not populated and [Post-
priced swap indicator] = ‘False’, and UPI.[Instrument type] ≠ ‘[[Option]]’, 
else {blank}
Restricted to Amount-Numeric-21-10 if [CDE - Spread notation-Leg 1] 
= 3 (The length is not fixed but limited to 11 numerical characters 
including up to ten numerical characters after the decimal point.)
Restricted to Amount-Numeric-5-0 if [CDE - Spread notation-Leg 1] = 
4
NULL
CO, CR, 
IR
Leg 2 - Fixed Rate Initial Fixed rate-Leg 2 O O NULL
IR Leg 2 - Reset Frequency 
Period
Floating rate reset 
frequency period-leg 2
C O When populated with ‘EXPI', [Leg 2 - Reset Frequency Period 
Multiplier] must be ‘1’ YEAR
CO, CR, 
EQ, IR
Leg 2 - Spread Amount Spread-Leg 2 O O Restricted to Amount-Numeric-21-10 if [CDE - Spread notation-Leg 2] 
= 3 (The length is not fixed but limited to 11 numerical characters 
including up to ten numerical characters after the decimal point.)
Restricted to Amount-Numeric-5-0 if [CDE - Spread notation-Leg 2] = 
4
75.7

---

## Page 3

[[DTCC]] Internal (Green)
3
FOR DISCUSSION: IR Fixed - Float: Validation PROPOSAL
**Updated** [Reset Frequency Period 1]: 
IR: Required if UPI.[Instrument type] = ‘Swap’ and UPI.[Underlying [[Asset]] Type] ≠ (‘Fixed - Fixed’ or {blank}) 
and [Leg 2 - Reset Frequency Period] is {blank}, else {blank} 
**NEW** [Leg 2 - Reset Frequency Period]: 
IR: Required if UPI.[Instrument type] = ‘Swap’ and UPI.[Underlying [[Asset]] Type] ≠ (‘Fixed - Fixed’ or {blank}) 
and [Reset Frequency Period 1] is {blank}, else {blank} 

---

## Page 4

[[DTCC]] Internal (Green)
4
© 2023. All rights reserved. [[DTCC]], and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain 
affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does 
not provide such services.  Each of these affiliates is a separate legal entity, subject 
to the laws and regulations of the particular country or countries in which such entity 
operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and 
the services they offer.

---

## Page 5

[[DTCC]] Internal (Green)