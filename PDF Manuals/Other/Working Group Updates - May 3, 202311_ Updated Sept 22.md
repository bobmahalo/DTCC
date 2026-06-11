---
title: "NoA Re-Write upcoming release notes"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Working%20Group%20Updates%20-%20May%203%2C%20202311_%20Updated%20Sept%2022.pdf"
pages: 8
size: "129.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# NoA Re-Write upcoming release notes

**Original File:** [Working Group Updates - May 3, 202311_ Updated Sept 22.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Working%20Group%20Updates%20-%20May%203%2C%20202311_%20Updated%20Sept%2022.pdf)  
**Category:** Other  
**Total Pages:** 8  
**File Size:** 129.9 KB  

---

## Page 1

[[DTCC]] Internal (Green)
GTR North America Re-Write Phase 2
Message Specification – Summary of Updates
North America Working Group – May 03, 2023
Updated: North America Working Group – Sept 22, 2023

---

## Page 2

[[DTCC]] Internal (Green)
2
.
Summary 
Message Specification Changes
A new message specification draft has been created to capture changes for the 
Phase 2 implementation in January 2024.
North America Re-Write Phase 2 Message Specification DRAFT
Overall updates:
• The ‘Change log’ will start with Phase 2 changes. The current production message specification will be 
retained as a separate document. Both will be updated and posted to the Learning Center, as applicable.
• The ‘NoA [[OTC]] Specifications’ has been updated to reflect Phase 2 updates:
• Change Release Dates are for Phase 2 changes.
• Change details for the columns such as “New GTR Field”, “Change in Data Type”, “Change in Valid 
Values”, etc. represent changes between the North America Re-Write and North America Re-Write 
Phase 2.
• The ‘Removed Fields’ tab represents changes from the North America Re-Write and North America Re-
Write Phase 2.

---

## Page 3

[[DTCC]] Internal (Green)
3UPI 
Message Specification Changes
1. Addition of the [UPI] field for Trade State, PPD and Valuation messages
2. Updates to the following fields adding in UPI related validations in line with the 
[[CFTC]] Tech Spec:
• [Notional Amount 1] • [Fixing date-Leg 1] • [Strike Price] • [Index factor]
• [Notional Currency 1] • [Reset Frequency Period 
1]
• [[[Premium]] Amount] • [CDE - Delta]
• [CDE - Notional amount in 
effect on associated effective 
date-Leg 1]
• [Leg 1 - Fixed Rate Initial] • [CDE - First 
Exercise Date]
• [CDE - Call amount-Leg 1] • [Price 1 – Price] • [Attachment Point]
• [CDE - Put amount-Leg 1] • [Leg 1 - Spread Amount] • [Exhaustion Point]
3. Included the ~56 fields that will be reported by [[DTCC]] from DSB/ANNA based 
on the UPI submitted and included for Trade State Reports
4. Removed existing [[DTCC]] product fields applicable to Credits, [[Equity]], FX and 
Rates for inbound submission (~9 fields)
5. Reporting outbound field names per SDR Guidebook from the [[CFTC]] on new 
fields.

---

## Page 4

[[DTCC]] Internal (Green)
4
UPI 
Message Specification – CSV Template / FpML and XML xpaths
CSV 
[UPI] has been added to the Harmonized CSV Templates for Trade 
State, PPD, and Valuation
FpML – [UPI] xpath
//partyTradeInformation/category[@categoryScheme="http://www.[[DTC]]
c.com/coding-scheme/unique-product-identifier"]/text()
[[DTCC]] XML – [UPI] xpath
/document/submission/core/uniqueProductIdentifier/text()

---

## Page 5

[[DTCC]] Internal (Green)
5
[[CFTC]] Tech Spec (March 2023) 
Message Specification Changes
1. [Notional Amount 1] and [Notional Amount 2] valid values were updated to include any 
value. (Previously ‘Greater than Zero’)
2. Changed from "XA" to "FX" for [CDE - Call amount-Leg 1], [CDE - Call currency-Leg 1], 
[CDE - Put amount-Leg 1] and [CDE - Put currency-Leg 1] and removal of the equivalent 
Leg 2 fields.
3. Removal of [CDE - [[settlement]] location-Leg 2]
4. “NEWT-UPDT” was added as an allowed Trade State Action Type/Event Type (PROD: 
June 2023)
5. Updated definition for [Block Trade Election Indicator] valid values (No changes to 
submission)

---

## Page 6

[[DTCC]] Internal (Green)
6
[[CFTC]] SDR Guidebook Updates (v4.2 April 2023)
Message Specification Changes
• Valid values will be updated to include any value. (Previously ‘Greater 
than Zero’)
• [CDE - Notional amount in effect on associated effective date-Leg 1]
• [CDE - Notional amount in effect on associated effective date-Leg 2]
• [CDE - Call amount-Leg 1] and 
• [CDE - Put amount-Leg 1]
• Clearing [[Member]] [[ID]] source [ClrMbrIDSrc] is reportable on Trade State 
reports
Other Message Specification Changes
• Added two fields: (1) [Other Payment Payer [[ID]] Type] and (2) [Other 
Payment Receiver [[ID]] Type] for Trade State submissions
• Updated Validations for: [CDE - Other Payment Payer [[ID]]] and [CDE -
Other Payment Receiver [[ID]]] which will be validated based on respective 
[[ID]] Type entered (LEI, NPID)

---

## Page 7

[[DTCC]] Internal (Green)
7
Part 43 (PPD/LNOFS)
Update
• PPD and LNOFS changes related to Part 43 are deferred for the January implementation 
date. Date: TBD. 
• Updates will be provided once additional details are provided by regulators.

---

## Page 8

[[DTCC]] Internal (Green)
8
© 2023. All rights reserved. [[DTCC]], and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by 
certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] 
itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in 
which such entity operates. Please see www.[[DTCC]].com for more information on 
[[DTCC]], its affiliates and the services they offer.