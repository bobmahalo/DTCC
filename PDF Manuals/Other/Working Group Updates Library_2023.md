---
title: "Working Group Library 2023"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Working%20Group%20Updates%20Library_2023.pdf"
pages: 97
size: "1795.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Working Group Library 2023

**Original File:** [Working Group Updates Library_2023.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Working%20Group%20Updates%20Library_2023.pdf)  
**Category:** Other  
**Total Pages:** 97  
**File Size:** 1795.7 KB  

---

## Page 1

CONFIDENTIAL
North America Working Group – January 11, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 2

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - Jan 17th 2023 PROD – Jan 27th 2023
NOAGTR-124: [CDE - Fixed rate payment frequency period-Leg 1 is not read for Generic 
Products] for CO, CR, FX, IR
Xpaths have been updated and split into two configurations
• $productType/paymentFrequency[1]/period/text()
• $original/genericProduct/paymentFrequency[1]/period/text() | 
$productTypeLifcycleExtension/[[DTCC]]:genericProductLifcycleExtension/[[DTCC]]:paymentStream/[[DTCC]]:p
aymentFrequency/[[DTCC]]:period/period
NOAGTR-158: Error Message Update for  [Trade Party 2 - [[ID]] Type] = ‘INTERNAL’
NOAR-NACK-016 and NOAR-PPD-NACK-015 will be updated for clarity
• From: “The Trade Party 2 - [[ID]] Type must be blank when The 'Trade Party 1 - Reporting 
Destination' in ('[[SEC]]', '[[CFTC]]') and the 'Trade Party 2 - [[ID]] Type' in ('INTERNAL’)”
• To: “'Trade Party 2 - [[ID]] Type' cannot be ('INTERNAL') when 'Trade Party 1 - Reporting 
Destination' is ('[[SEC]]', '[[CFTC]]')”
NOAGTR-169: LNOFS for FX on EROR, TERM, and PRTO
The [Large Notional Off-Facility Swap Indicator] is being calculated for FX when
• [NoA – Action Type] = ‘EROR’, ‘TERM’, or ‘PRTO’
• The [SEF or DCM Indicator] and [Large Notional Off-Facility Swap Indicator] are both submitted 
as {blank} 
This will be corrected, and the [Large Notional Off-Facility Swap Indicator] will be populated as ‘False’ 
under the above conditions.

---

## Page 3

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - Jan 17th 2023 PROD – Jan 27th 2023
Learning Center Updates by End of Week
• Release Notes
• Message Spec V4.3
NOAGTR-193: CSV Submissions where [Version] is blank Causing Duplicate Trades
CSV submissions where [Version] = blank that contain multiple rows where [NoA – Action Type] 
‘NEWT’ for the same UTI+[Trade Party 1 – [[ID]]] result in duplicate positions. This will be corrected.
Workaround: A MODI will remove duplicates.

---

## Page 4

CONFIDENTIAL
North America Working Group – January 25, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 5

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - Jan 17th 2023 PROD – Jan 27th 2023
Learning Center Updates by End of Week
• Release Notes
UPDATE: NOAGTR-193: CSV Submissions where [Version] is blank Causing Duplicate Trades
CSV submissions where [Version] = blank that contain multiple rows where [NoA – Action Type] 
‘NEWT’ for the same UTI+[Trade Party 1 – [[ID]]] result in duplicate positions. This will be corrected.
Workaround: A MODI will remove duplicates.
As part of this update, validations were added. Only valid values from the message 
specifications will be accepted. 
• For PPD Harmonized CSV, the only valid value is “PPD1.0” 
• For Harmonized CSV and Harmonized Valuation Templates, the only valid value is 
"CORE1.0"
• For [[collateral]] Valuation, the only valid vale is "Coll1.0“
NOAGTR-190: [CDE - Fixed rate day count convention-leg 2] is not being read when populated 
on a FpML message
A metadata update will be made for [CDE - Fixed rate day count convention-leg 2] so the field will be 
read and reported. There are no updates to the current xpath. 

---

## Page 6

CONFIDENTIAL
North America Working Group – February 1, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 7

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - March 16th 2023 PROD – March 31th 2023
UPDATED RELEASE DATE: NOAGTR-156: Length Validation for [[Buyer]]/[[Seller]]/Payer/Receiver 
Fields
The following fields will accept up to 200 characters to accommodate submissions for Canada where 
[Trade Party 2 – [[ID]]] can be an internal identifier up to 200 characters.
• [CDE - Receiver identifier-Leg 2] Update for XML only –All other submission methods were 
updated on Dec 16th through NOAGTR-134
NOAGTR-200: Other Payment fields are not being read when populated on a FpML message
The message specification will be updated to remove the following xpaths that are parsing the literal 
PartyA/PartyB values:
• [CDE - Other payment payer] 
$transaction/otherPartyPayment/payerPartyReference/@href | 
$transaction/originalTrade/otherPartyPayment/payerPartyReference/@href
https://[[DTCC]]-edm.collibra.com/[[Asset]]/d1f40614-5e68-4702-94b1-71f07ed67365
• [CDE - Other payment receiver]
$transaction/otherPartyPayment/receiverPartyReference/@href | 
$transaction/originalTrade/otherPartyPayment/receiverPartyReference/@href
https://[[DTCC]]-edm.collibra.com/[[Asset]]/ef07d0f9-42d4-4bef-ac73-4d3dffaf90b4
The following are the available in the message spec xpaths that will parse the LEI instead of literal values: 
[CDE - Other payment payer]
//party[@[[ID]]=//otherPartyPayment/payerPartyReference/@href]/partyId/text()
[CDE - Other payment receiver]
//party[@[[ID]]=//otherPartyPayment/receiverPartyReference/@href]/partyId/text()

---

## Page 8

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - March 16th 2023 PROD – March 31th 2023
Learning Center Updates by End of Week
• Release Notes
• Message Specification v4.5 
NOAGTR-1041: Treatment of {blank} fields for PPD Time Delay calculations for TERM Action 
Types ([[CFTC]])
Time delays are applied to [[CFTC]] TERM PPD submissions when a value is required but {blank} fields 
are submitted. This will be corrected in this fix.
NOAGTR-1323: [[[settlement]] Type] validations for TS and PPD submissions ([[CFTC]]/[[SEC]]/CAD)
Transformations for this field will be removed and validation rules will be updated to reject 
submissions that [[DO]] not match the message spec list of valid values:
• Cash
• CashOrPhysical
• Election
• Not Applicable
• Optional
• Physical

---

## Page 9

CONFIDENTIAL
North America Working Group – February 22, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 10

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - March 16th 2023 PROD – March 31th 2023
NOAGTR-159: Fixed/Floating Day Count Fraction FpML xpaths will be updated so that submitted values are parsed into the 
leg populated for [[Equity]]. Other [[Asset]] Classes are under review. 
UPDATED xpaths for CDE - Fixed & Floating rate day count convention-leg 2 fields
Removed [2] from the xpaths. These fields will always be read from the <interestLeg> to be consistent with the Leg 2 Payment 
Frequency fields.
Before:
$productType/interestLeg[2]/interestCalculation/dayCountFraction | 
$original/[[DTCC]]:equitySwapTransactionSupplementDTCC/interestLeg[2]/interestCalculation/dayCountFraction | 
$LifcycleExtension/[[DTCC]]:interestCalculation/interestCalculation/dayCountFraction
After:
$productType/interestLeg/interestCalculation/dayCountFraction | 
$original/[[DTCC]]:equitySwapTransactionSupplementDTCC/interestLeg/interestCalculation/dayCountFraction | 
$LifcycleExtension/[[DTCC]]:interestCalculation/interestCalculation/dayCountFraction
REMOVED xpaths for CDE - Fixed & Floating rate day count convention-leg 1 fields
Per current behavior, <interestLeg> xpaths should be mapped to Leg 2 fields only for consistency.
Removed Xpaths:
$productType/interestLeg[1]/interestCalculation/dayCountFraction | 
$transaction/[[DTCC]]:originalProductReferenceDTCC/[[DTCC]]:equitySwapLifcycleExtension/[[DTCC]]:interestCalculation/interestCalculation/d
ayCountFraction | 
$transaction/[[DTCC]]:originalProductReferenceDTCC/[[DTCC]]:equitySwapLifcycleExtension/[[DTCC]]:interestCalculation/interestCalculation/d
ayCountFraction | $original/[[DTCC]]:equitySwapTransactionSupplementDTCC/interestLeg[1]/interestCalculation/dayCountFraction | 
$LifcycleExtension/[[DTCC]]:interestCalculation/interestCalculation/dayCountFraction

---

## Page 11

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - March 16th 2023 PROD – March 31th 2023
Learning Center Updates by End of Week
• Release Notes
• Working Group Updates 
• Message Specification v4.6
NOAGTR-1370: This update will apply the validation "Must be blank if [SEF or DCM Indicator] = True" to TERM, EROR 
or PRTO action types for the [Large Notional Off Facility Swap Indicator] field in line with the current message 
specifications. ([[CFTC]] only)
NOAGTR-1329: Only the USI/UTI submitted in a Revive (REVI) submission is reported in the TSR after a position has been 
Terminated, Errored or Expired even if both USI/UTI existed previously. This update will include both USI/UTIidentifiers in 
the TSR if they were previously reported when a Revive is submitted and a data fix will be applied to any REVIs previously 
submitted in the Re-Write. 
Previous 
Identifiers 
available:
REVI 
submission 
and identifier 
included:
Current TSR 
Reporting:
Reporting after 
fix:
USI/UTI USI USI USI/UTI
USI/UTI UTI USI USI/UTI
USI/UTI USI/UTI USI/UTI USI/UTI
UTI UTI UTI UTI
USI USI USI USI

---

## Page 12

CONFIDENTIAL
North America Working Group – March 15, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 13

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - March 16th 2023 PROD – March 31th 2023
Learning Center Updates by End of Week
• Release Notes
• Working Group Updates
• Message Spec v4.7  
NOAGTR-1816 (Previously NOA-13834): [Notional Amount 1] and [Notional Currency 1] for IR 
FRA Termination for FpML
[Notional Amount 1] and [Notional Currency 1] cannot be populated for FRA Termination. This will be 
corrected for the following Trade State and RT xpaths: 
[Notional Amount 1]:  
$original/fra/notional/amount/text()
//[[Novation]]/newTrade/fra/notional/amount/text()
[Notional Currency 1]: 
$original/fra/notional/currency/text()
//[[Novation]]/newTrade/fra/notional/currency/text()
Notes:
Updated Selectors for FRA RT [Notional Amount 1] and [Notional Currency 1]. 
Removed "RealTime-TransactionTypes" so that xpaths can be used for all RT Transactions (FpML Structures)

---

## Page 14

CONFIDENTIAL
North America Working Group – April 05, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 15

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - June 6th 2023   PROD – June 30th 2023
Rescheduled - An updated release date will be provided when available.
NOAGTR-200: Other Payment fields are not being read when populated on a FpML message
The Message Spec. has been updated for the following original xpaths:
• [CDE - Other payment payer] 
$transaction/otherPartyPayment/payerPartyReference/@href | 
$transaction/originalTrade/otherPartyPayment/payerPartyReference/@href
https://[[DTCC]]-edm.collibra.com/[[Asset]]/d1f40614-5e68-4702-94b1-71f07ed67365
• [CDE - Other payment receiver]
$transaction/otherPartyPayment/receiverPartyReference/@href | 
$transaction/originalTrade/otherPartyPayment/receiverPartyReference/@href
https://[[DTCC]]-edm.collibra.com/[[Asset]]/ef07d0f9-42d4-4bef-ac73-4d3dffaf90b4
Learning Center Updates by End of Week
• Release Notes
• Working Group Updates
• Message Spec v4.8  
NOAGTR–1815: Batch Download Reports Portal posting for Canada only submitters
BDRs for Canada only submitters are being posted into the Credit [[Asset]] class in the Submission 
Response section of the portal instead of the respective [[Asset]] class. This will be fixed in this update.

---

## Page 16

CONFIDENTIAL
North America Working Group – April 12, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 17

[[DTCC]] Public (White)
CONFIDENTIAL
NOAGTR–1326: Updates for [Trade Party 1 - [[ID]]] and [Trade Party 1 – [[ID]] Type] and 
[Trade Party 2 - [[ID]]] ([[CFTC]] Tech Spec – Aug 2022 update)
• Applicable Trade State, PPD, Valuation and [[collateral]] report for [[CFTC]]/[[SEC]]/CANADA jurisdictions
[Trade Party 1 – [[ID]] Type]:
• ‘NPID’ will be added as a valid value for [Trade Party 1 – [[ID]] Type] 
• The following validation will be added:
• ‘NPID’ is only accepted when [CDE - Platform Identifier] is not 'XXXX', 'XOFF', or 'BILT' AND 
[Clearing Status] = "I“
[Trade Party 1 – [[ID]]]:
• The following validation will be added:
• If [Trade Party 1 - [[ID]] Type] = 'NPID', then up to 72 characters only are accepted.The first 
20 characters in the [Trade Party 1 - [[ID]]] field is a valid (active or inactive) LEI per the 
GLEIF database.
[Trade Party 2 - [[ID]]]:
• The following validation will be updated:
• Current: If  [Trade Party 2 - [[ID]] Type] =  ‘NPID’ then up to 72 characters only are 
accepted. The first 20 characters must equal the value of [Trade Party 1 -[[ID]]]. 
• Updated: If [Trade Party 2 - [[ID]] Type] = ’NPID’ then up to 72 characters only are 
accepted. The first 20 characters must be a valid (active or inactive) LEI per the GLEIF 
database.
UAT - June 6th 2023   PROD – June 30th 2023

---

## Page 18

[[DTCC]] Public (White)
CONFIDENTIAL
NOAGTR-1325: Clearing [[Member]] update for the fields [Trade Party 1 - Clearing 
[[Broker]] [[ID]] Type] and [Trade Party 1 - Clearing [[Broker]] [[ID]]] ([[CFTC]] Tech Spec – Aug 
2022 update)
[Trade Party 1 - Clearing [[Broker]] [[ID]] Type]
• ‘NPID’ & ‘PLID’ will be added as valid values for Trade State messages for all jurisdictions.
• The following validation will be added:
• 'NPID' is only accepted for [Trade Party 1 - Clearing [[Broker]] [[ID]] Type] when[Trade Party 2 - [[ID]] 
Type] = 'NPID’
[Trade Party 1 - Clearing [[Broker]] [[ID]]]: 
• [Trade Party 1 - Clearing [[Broker]] [[ID]]] will be expanded from [[ID]]-Text-20 to [[ID]]-Text-72.
• The following validation will be added:
• If [Trade Party 1 - Clearing [[Broker]] [[ID]] Type] = 'NPID’, the first 20 characters must be a 
valid LEI as per the GLEIF database. The LEI DOES NOT NEED TO BE in ACTIVE 
status.
NOAGTR-1813: Update to MQ Submission response message in FpML/XML 
A “&quot;” is being included in response messages and will be removed as part of this 
update. Impacted error codes: RTD-NACK-0010, NOAR-NACK-041, NOAR-PPD-NACK-035
• Current Message Example: &quot;Latest Execution DateTime&quot; is after the &quot;Submission
Timestamp&quot; by more than 15 minutes => in response file
• Updated Message Example: The Latest Execution DateTime is after the Submission Timestamp by 
more than 15 minutes
UAT - June 6th 2023   PROD – June 30th 2023

---

## Page 19

[[DTCC]] Public (White)
CONFIDENTIAL
Learning Center Updates by End of Week
• Release Notes
• Working Group Updates
• Message Spec v4.9

---

## Page 20

CONFIDENTIAL
North America Working Group – April 19, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 21

[[DTCC]] Public (White)
CONFIDENTIAL
NOAGTR–1786: Validation update for [Primary [[Asset]] Class]
'IR' and 'FX' are currently accepted for [Primary [[Asset]] Class] and no longer will be 
accepted with this update. The valid values that will be accepted are listed in the current 
message specifications and the following error messages if 'IR' or 'FX' are submitted:
• [[CFTC]]: The Primary [[Asset]] Class must be in 
COMMODITY ,CREDIT,[[Equity]] ,FOREIGNEXCHANGE,INTERESTRATE
• CANADA: The Primary [[Asset]] Class must be in 
COMMODITY ,CREDIT,[[Equity]] ,FOREIGNEXCHANGE,INTERESTRATE
• [[SEC]]/Canada PPD: The Primary [[Asset]] Class must be in CREDIT,[[Equity]] ,INTERESTRATE
UAT - June 6th 2023   PROD – June 30th 2023
Learning Center Updates by End of Week
• Release Notes
• Working Group Updates
• NoA Error Codes (Posted last week on April 14th)

---

## Page 22

CONFIDENTIAL
North America Working Group – May 03, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 23

[[DTCC]] Public (White)
CONFIDENTIAL
UPDATED NOAGTR–1326: Updates for [Trade Party 1 - [[ID]]] and [Trade Party 1 – [[ID]] 
Type] and [Trade Party 2 - [[ID]]] ([[CFTC]] Tech Spec – Aug 2022 update)
• Applicable Trade State and PPD, Valuation and [[collateral]] report for [[CFTC]]/[[SEC]]/CANADA 
jurisdictions
[Trade Party 1 – [[ID]] Type]:
• ‘NPID’ will be added as a valid value for [Trade Party 1 – [[ID]] Type] 
• The following validation will be added:
• ‘NPID’ is only accepted when [CDE - Platform Identifier] is not 'XXXX', 'XOFF', or 'BILT' AND 
[Clearing Status] = "I“
[Trade Party 1 – [[ID]]]:
• The following validation will be added:
• If [Trade Party 1 - [[ID]] Type] = 'NPID', then up to 72 characters only are accepted.The first 
20 characters in the [Trade Party 1 - [[ID]]] field is a valid (active or inactive) LEI per the 
GLEIF database.
[Trade Party 2 - [[ID]]]:
• The following validation will be updated:
• Current: If  [Trade Party 2 - [[ID]] Type] =  ‘NPID’ then up to 72 characters only are 
accepted. The first 20 characters must equal the value of [Trade Party 1 -[[ID]]]. 
• Updated: If [Trade Party 2 - [[ID]] Type] = ’NPID’ then up to 72 characters only are 
accepted. The first 20 characters must be a valid (active or inactive) LEI per the GLEIF 
database.
UAT - June 6th 2023   PROD – June 30th 2023

---

## Page 24

[[DTCC]] Public (White)
CONFIDENTIAL
NOAGTR–1827: Additional Xpath conditions for CDE Floating Rate Leg 2 Fields for IR 
Inflation Swaps
Additional Inflation Swap-specific conditions have been added for the following CDE Floating Rate Leg 2 
fields so the fields can be populated.
• CDE - Floating rate payment frequency period multiplier-Leg 2
• CDE - Floating rate payment frequency period-Leg 2
• CDE - Floating rate day count convention-leg 2
The xpaths will remain the same and new conditions have been added. No changes have been made to 
existing xpaths and conditions.
We will read in Leg 2 Floating rate fields from 
boolean(//calculationPeriodAmount/calculation/inflationRateCalculation)
if
boolean(//swapStream[2]/calculationPeriodAmount/calculation/floatingRateCalculation)
has not been populated.
UAT - June 6th 2023   PROD – June 30th 2023

---

## Page 25

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - June 6th 2023   PROD – June 30th 2023
NOAGTR-200: Other Payment fields are not being read when populated on a FpML message
The Message Spec has been updated for the following original xpaths:
• [CDE - Other payment payer] 
$transaction/otherPartyPayment/payerPartyReference/@href | 
$transaction/originalTrade/otherPartyPayment/payerPartyReference/@href
https://[[DTCC]]-edm.collibra.com/[[Asset]]/d1f40614-5e68-4702-94b1-71f07ed67365
• [CDE - Other payment receiver]
$transaction/otherPartyPayment/receiverPartyReference/@href | 
$transaction/originalTrade/otherPartyPayment/receiverPartyReference/@href
https://[[DTCC]]-edm.collibra.com/[[Asset]]/ef07d0f9-42d4-4bef-ac73-4d3dffaf90b4
Learning Center Updates by End of Week
• Release Notes
• Working Group Updates
• Message Spec v5.0
• GTR North America Re-Write Phase 2 Message Specification – Summary of 
Updates
• North America Re-Write Phase 2 Message Specification DRAFT (posted last week)
• 2023-2024 Roadmap (posted last week)

---

## Page 26

CONFIDENTIAL
North America Working Group – May 10, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 27

[[DTCC]] Public (White)
CONFIDENTIAL
NOAGTR–2092: Addition of 'NEWT-UPDT' Action / Event Type for Trade State and 
PPD submissions
'NEWT-UPDT' will be an allowable Action Type/Event Type combo for Trade State and PPD 
messages for CSV, XML and FpML submissions.
Note: This change was originally scheduled for January 2024 as part of the [[CFTC]] Technical 
Specification version 3.2 updates: “ NEWT-UPDT is used for upgrading existing ‘exotic’, ‘complex’, 
or ‘non-standard’ swaps to accurately report and comply with the [[CFTC]] Technical Specification” 
Based on recent discussions, regulators would like firms to use this action/event type combo for 
backloading (see use case below) and this change has been moved to the June 2023 maintenance 
release.
UAT - June 6th 2023 PROD – June 30th 2023
Submission 
Date
Message 
Type Action
Trancation 
Type
Action 
Type Event Type UTI USI
Prior 
USI Comment
1/1/2020 Snapshot New Trade 123abc Trade was submitted and exited prior to the Re-arch 
implementation in Nov 2020. This trade was not 
initialized for the Re-Write implementation. 1/1/2020 Snapshot New Exit 123abc
7/1/2023 Trade State NEWT UPDT 456abc 123abc Firm needs to backload valuation message. A trade 
state message needs to be submitted to establish the 
base trade since this was not initialized in the Re-
Write implementation. A UTI must be submitted, and 
the USI can be included in the Prior USI trade state 
field. 
7/1/2023 Trade State TERM NOAV 456abc 123abc
7/1/2023 Valuation VALU 456abc
Backloading Use Case:
Note: Trades that are backloaded that are Expired or Terminated will not be reported on the Trade State Report. Submissions willbe 
reported in the Activity Reports. 

---

## Page 28

[[DTCC]] Public (White)
CONFIDENTIAL
Learning Center Updates by End of Week
• Release Notes
• Working Group Updates
• Message Specification v5.1
• NoA Re-Write Phase 2 Message Specification DRAFT v1.2 

---

## Page 29

CONFIDENTIAL
North America Working Group – May 24, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 30

[[DTCC]] Public (White)
CONFIDENTIAL
NOAGTR-2113: Correction in the CDE Floating Fields Xpath for IR Swap
Corrected typos in xpaths regarding the capitalization of swapStream
CDE - Floating rate day count convention-leg 1
Incorrect Xpath:
$original/swap/swapstream[1]calculationPeriodAmount/calculation/dayCountFraction
Correct Xpath:
$original/swap/swapStream[1]/calculationPeriodAmount/calculation/dayCountFraction
CDE - Floating rate day count convention-leg 2
Incorrect Xpath:
$original/swap/swapstream[2]calculationPeriodAmount/calculation/dayCountFraction
Correct Xpath:
$original/swap/swapStream[2]/calculationPeriodAmount/calculation/dayCountFraction
Leg 1 - Floating Rate Index
Incorrect Xpath:
$productType/swap/swapstream[1]/calculationPeriodAmount/calculation/floatingRateCalculation/floating
RateIndex/text()
Correct Xpath: 
$productType/swap/swapStream[1]/calculationPeriodAmount/calculation/floatingRateCalculation/floating
RateIndex/text()
UAT - June 6th 2023   PROD – June 30th 2023

---

## Page 31

[[DTCC]] Public (White)
CONFIDENTIAL
NOAGTR– 2119: Removal of Valid Values for field [Trade Party 2 – Reporting 
Destination]
The following valid values will be removed as part of this update:
•ESMA-N
•ESMA-X
•EUSF
•FCA-N
•FCA-X
•GTR
•MIFIR
•ODRF
•UKSF
Applicable to [[CFTC]]/[[SEC]]/CANADA for all the [[Asset]] Classes & Message Types
UAT - June 6th 2023   PROD – June 30th 2023
Learning Center Updates by End of Week
• Release Notes
• Working Group Updates 
• Release updates
• Phase 2 Message Specification Summary Updates
• Message Specification v5.2
• NoA Re-Write Phase 2 Message Specification DRAFT v1.3

---

## Page 32

CONFIDENTIAL
North America Working Group – May 31, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 33

[[DTCC]] Public (White)
CONFIDENTIAL
NOAGTR–2137: NoA Re-Write Maintenance UTI Identifier Update
• Currently, the UTI Identifier Service is generating [[DTCC]]’s Namespace 1010000236as the UTI prefix.
• The fix will address the UTI prefix issues so that the UTI Identifier Service will generate DDR’s LEI 
549300H9ZM7RDBM87W85 per GLEIF as the UTI prefix.   
UAT - June 6th 2023 PROD – June 30th 2023
Learning Center Updates by End of Week
• Release Notes
• Working Group Updates

---

## Page 34

CONFIDENTIAL
North America Working Group – June 7, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 35

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - June 13th 2023   PROD – June 30th 2023
Learning Center Updates by End of Week
• Release Notes
• Working Group Updates 
• Phase 2 - [[participant]] Report Change Summary
• [[participant]] Report Sample Layouts
• Functional Change Document – NoA Re-Write Phase 2 
RDSPORT-16659 – Duplicate transactions in PPD [[participant]] Reports
This fix will remove duplicate records in PPD [[participant]] Reports that occur when the 
Submitter, Trade Party 1 and Execution Agent have multiple LEIs and the same OCODE.
Note: Regulatory reporting and the public website are not impacted.

---

## Page 36

CONFIDENTIAL
North America Working Group – June 14, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 37

[[DTCC]] Public (White)
CONFIDENTIAL
UAT - June 13th 2023 PROD – June 30th 2023
NOAGTR- 2232 – Update to [Trade Party 2 - Reporting Destination] when 
[Submitted for Party] is 'Party1'
In UAT,values for [Trade Party 2 – Reporting Destination] should be ignored when the 
[Submitted for Party] = ‘Party1’ in line with the Message Spec. This will be corrected in this 
update.
1. [UPI] FpML and [[DTCC]] XML xpath updates
• FpML
//partyTradeInformation/category[@categoryScheme="http://www.[[DTCC]].com/coding-scheme/upi"]/text()
• [[DTCC]] XML 
/document/submission/core/upi/text()
2.  Updates to [Other payment payer [[ID]] Type] and [Other payment receiver [[ID]] Type]
o Cardinality has been updated to 18 in line with the respective CDE fields.
o The number of values must equal the number of values populated in [CDE - Other payment payer] 
or [CDE - Other payment receiver] for [Other Payment Payer [[ID]] Type] and [Other Payment 
Receiver [[ID]] Type]
NoA Re-Write Phase 2 Message Specification 
Updates (v1.4)

---

## Page 38

[[DTCC]] Public (White)
CONFIDENTIAL
• Release Notes
• Working Group Updates
• NoA Re-Write Message Specification v5.3
• NoA Re-Write Phase 2 Message Specification DRAFT v1.4
Learning Center Updates

---

## Page 39

North America Working Group – June 21, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 40

[[DTCC]] Public (White)
NoA Re-Write Phase 2 Message Specification 
Updates (v1.5)
1. Updates to [Other payment payer [[ID]] Type] and [Other payment receiver [[ID]] Type]
o The following FpML and [[DTCC]] XML xpaths will be added to the Phase 2 Message Specification
▪ FpML
[Other Payment Payer [[ID]] Type] 
//party[@[[ID]]=//otherPartyPayment/payerPartyReference/@href]/partyId/@partyIdScheme
[Other Payment Receiver [[ID]] Type]
//party[@[[ID]]=//otherPartyPayment/receiverPartyReference/@href]/partyId/@partyIdScheme
▪ [[DTCC]] XML
[Other Payment Payer [[ID]] Type] 
/document/submission/harmonizedRepeatableData/otherPaymentPayerIdType/text()
[Other Payment Receiver [[ID]] Type]
/document/submission/harmonizedRepeatableData/otherPaymentReceiverIdType/text()
2. Updated Prefix from “DSB” to “UPI” for outbound reporting field names that are based on the 
UPI values (56 Data Elements sourced from UPI) 

---

## Page 41

[[DTCC]] Public (White)
• Working Group Updates
• NoA Re-Write Phase 2 Message Specification DRAFT v1.5
• [[participant]] Report Samples 
• [[participant]] Report Summary
• [[CFTC]] Clearing Exceptions Update
Learning Center Updates

---

## Page 42

CONFIDENTIAL
North America Working Group – July 12, 2023
GTR North America Re-Write Upcoming Releases

---

## Page 43

[[DTCC]] Public (White)
CONFIDENTIAL
Update to Cardinality of Notional Schedule Fields : With the valid values update to allow 
negative values, total character limit for the below fields will exceed 500 characters. T o align 
with the regulatory reporting limit, cardinality will be reduced from 18 to 17. 
▪    [CDE - Notional amount in effect on associated effective date-Leg 1]
▪ [CDE - Notional amount in effect on associated effective date-Leg 2]
▪ [CDE - Effective date of the notional amount-Leg 1]
▪ [CDE - Effective date of the notional amount-Leg 2]
▪ [CDE - End date of the notional amount-Leg 1]
▪ [CDE - End date of the notional amount-Leg 2]
NoA Re-Write Phase 2 Message Specification 
Updates v1.6
[UPI] business rule updates for TERM/EROR: The following rules have been added due 
to PPD Capping and LNOFS calculation requirements:
• 'Required for Trade State when [Primary [[Asset]] Class] = 'Credit', [Large notional off-facility swap 
election indicator] is {blank} and [SEF or DCM Indicator] = 'False'
• Required for PPD when [Primary [[Asset]] Class] = 'Credit'
Other minor updates to the message specification are detailed in the change log. 

---

## Page 44

[[DTCC]] Public (White)
CONFIDENTIAL
• Working Group Updates
• NoA Re-Write Phase 2 Message Specification DRAFT v1.6
• NoA Re-Write Phase 2 PPD/LNOFS Update
• NoA Re-Write Phase 2 Large Trade Size Calculations 
• NoA Re-Write Phase 2 Public Price Dissemination (PPD) Transformation and Time Delay 
• NoA Re-Write Phase 2 UPI Examples
• NoA Re-Write Phase 2 [[participant]] Reports Sample v1.8
Learning Center Updates

---

## Page 45

[[DTCC]] Internal (Green)
GTR North America Re-
Write Upcoming Releases
North America Working Group – August 23, 2023

---

## Page 46

[[DTCC]] Internal (Green)
2UAT – August 29, 2023 PROD – September 29, 2023
Updated XA Xpath to be for Generic Only:
$productType/paymentFrequency[./underlyerReference[@href=//genericProduct/underlyer[1]/@[[ID]]]]/periodMultiplier/text() | 
$original/genericProduct/paymentFrequency[./underlyerReference[@href=//genericProduct/underlyer[1]/@[[ID]]]]/periodMultipli
er/text() | $productType/paymentFrequency[1]/periodMultiplier/text() | 
$original/genericProduct/paymentFrequency[1]/periodMultiplier/text()
Split Credit Xpath from above into new configuration for Credit [[default]] Swap products:
$productType/feeLeg/periodicPayment/paymentFrequency/periodMultiplier/text() | 
$original/creditDefaultSwap/feeLeg/periodicPayment/paymentFrequency/periodMultiplier/text()
NOAGTR-2358/2366 : Update for [CDE - Fixed rate payment frequency period multiplier-Leg 
1] Xpath

---

## Page 47

[[DTCC]] Internal (Green)
3North America Re-Write Phase 2 Updates 
Underlying [[Asset]] field updates:
• The following product fields will be added as 'Optional' for [[SEC]] and Canada for the October UAT release
• [Underlying [[Asset]] [[ID]]]
• [Leg 1 - Floating Rate Index]
• [Leg 2 - Floating Rate Index]
• [Underlying [[Asset]] [[ID]] Type]
• [Underlying [[Asset]] Name]
• These fields are not applicable for [[CFTC]]. However, the columns will still be included for reporting as Re-Write 
data will continue to be reported until a UPI is submitted. Once a UPI is submitted, the columns will contain blank 
values.
UPI update:
• UPI data from the ANNA-DSB UPI-ISIN UAT database will be included in the September 7th UAT release.

---

## Page 48

[[DTCC]] Internal (Green)
4
NoA Re-Write & NoA Re-Write Phase 2 Message Specification 
• Working Group Updates
• Release Notes
• NoA Re-Write Phase Message Specification v5.5
• NoA Re-Write Phase 2 Message Specification v1.9
• NoA Re-Write Phase 2 Submission Samples – Added FpML valuation submission samples
• Re-Write Phase 2 Message Response Samples (Already posted to the Learning Center)
• Error Codes v8 (Already posted to the Learning Center)
Learning Center Updates

---

## Page 49

[[DTCC]] Internal (Green)
5
© 2023. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL 
MARKETS. TOGETHER, and the Interlocker graphic are registered and unregistered 
trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain 
affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does 
not provide such services.  Each of these affiliates is a separate legal entity, subject 
to the laws and regulations of the particular country or countries in which such entity 
operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and 
the services they offer.

---

## Page 50

[[DTCC]] Internal (Green)

---

## Page 51

[[DTCC]] Internal (Green)
GTR North America Re-
Write Upcoming Releases
North America Working Group – Sept 20, 2023

---

## Page 52

[[DTCC]] Internal (Green)
2
UAT – Oct 26, 2023 PROD – Jan 28, 2024
• Added “INTERNAL” as a valid value for the [Other payment payer [[ID]] type] & [Other payment receiver [[ID]] type] fields
• For [CDE - Other payment payer] and [CDE - Other payment receiver] fields, the data type and valid values have been 
updated to:
• If [Trade Party 2 - [[ID]] Type] = "INTERNAL" then up to 200 characters are accepted
• Changes are applicable to Canada only
NOAGTR- 2494: Addition of 'INTERNAL' for Canada submissions for the Other Payment 
Payer/Receiver fields
NOAGTR- 2515: Update to the business rules for [CDE - Notional amount in effect on associated 
effective date-Leg 1] field
• Updates to business rule for [CDE - Notional amount in effect on associated effective date-Leg 1] to exclude {blank} UPI 
data elements during validation
• Required for IR if UPI.[Notional schedule] ≠ (‘Constant’ or {blank}), else {blank}

---

## Page 53

[[DTCC]] Internal (Green)
3
• NoA Re-Write Phase 2 Message Specification v2.1
• GTR Re-Write Phase 2 UAT Release Notes
Learning Center Updates
• The NoA Identifier Service for [[CFTC]], [[SEC]] and Canada will generate identifiers in the [UTI [[ID]]] field only
• The UTI [[ID]] will no longer be split between [UTI Prefix] and [UTI [[ID]]]
NOAGTR- 2422: Update to North America Identifier Service
UAT – Oct 26, 2023 PROD – Jan 28, 2024

---

## Page 54

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

## Page 55

[[DTCC]] Internal (Green)

---

## Page 56

[[DTCC]] Internal (Green)
North America 
Re-Write Phase 2
North America Working Group – Oct 4, 2023

---

## Page 57

[[DTCC]] Internal (Green)
2
• Updates to business rule for [CDE - Notional amount in effect on associated effective date-Leg 1] to 
exclude {blank} UPI data elements during validation
• Required for IR if UPI.[Notional schedule] ≠ (‘Constant’ or {blank}), else {blank}
• UAT: Oct 26th and PROD: Jan 28th
Update to the business rules for [CDE - Notional amount in effect on associated 
effective date-Leg 1] field

---

## Page 58

[[DTCC]] Internal (Green)
3
IR Fixed - Float Reporting Scenario 
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

## Page 59

[[DTCC]] Internal (Green)
4
UPDATE: IR Fixed - Float: Validation Change
**Updated** [Reset Frequency Period 1]: 
IR: Required if UPI.[Instrument type] = ‘Swap’ and UPI.[Underlying [[Asset]] Type] ≠ (‘Fixed - Fixed’ or {blank}) 
and [Leg 2 - Reset Frequency Period] is {blank}, else {blank} 
**NEW** [Leg 2 - Reset Frequency Period]: 
IR: Required if UPI.[Instrument type] = ‘Swap’ and UPI.[Underlying [[Asset]] Type] ≠ (‘Fixed - Fixed’ or {blank}) 
and [Reset Frequency Period 1] is {blank}, else {blank} 

---

## Page 60

[[DTCC]] Internal (Green)
5
FOR DISCUSSION: CDE- First Exercise Reporting Scenario 
Background: The [[CFTC]] Tech Spec states within the validation rules that CDE- First Exercise Date is required when the UPI  
Instrument Type is an [[Option]]. However, within the definition for the data element, specifically, in regards to knock-in options it 
states that for knock-in options, where the first exercise date is not known when a new transaction is reported, the first 
exercise date is updated as it becomes available. In the CDE- First Exercise scenario, the firm would like to report blank until 
the first exercise date becomes available. 
[[Asset]] 
Class
Inbound Field
Outbound field for 
[[participant]] 
Submission Report 
Only
Outbound 
Field Definition for Data Element
Rules -
Trade State 
for NEWT, 
MODI, 
CORR, REVI
Rules - PPD 
for NEWT, 
MODI, 
CORR, REVI
Data Type Valid Values Business Rules (Inbound Field Names) FIRM Submission 
Example:
XA CDE - First Exercise 
Date 
First Exercise 
Date
First unadjusted date during the 
exercise period in which an [[Option]] can 
be exercised. For European-style 
options, this date is same as the 
Expiration date. For American-style 
options, the first possible exercise date 
is the unadjusted date included in the 
Execution timestamp. For knock-in 
options, where the first exercise date is 
not known when a new transaction is 
reported, the first exercise date is 
updated as it becomes available. This 
data element is not applicable if the 
instrument is not an [[Option]] or does not 
embed any optionality.
C C
ISO8601-UTC-
Date YYYY-
MM-DD based 
on UTC
Any valid date. CR, EQ, FX, IR - Required if 
UPI.[Instrument type] = ‘[[Option]]’, else 
{blank}
NULL

---

## Page 61

[[DTCC]] Internal (Green)
6
FOR DISCUSSION: CDE- First Exercise Scenario: PROPOSAL
[[Option]] #1
Firms can submit a dummy value such as 0000-00-00.
[[Option]] #2
Firms can submit the initial knock-in barrier observation date (trade date of the [[Option]]) or the 
contractual barrier observation start date.
Note: This would not require a validation change at [[DTCC]] and will be raised to ISDA for 
industry best practices.

---

## Page 62

[[DTCC]] Internal (Green)
7
FOR DISCUSSION: IR Float - Float Reporting Scenario 
Background: The [[CFTC]] Tech Spec states the validations for spread amount should be placed in leg 1. In the IR Float-Float 
Swap scenario, the firm would like to report the spread in Leg 2. Due to the validations in leg 1, this would make the leg 1 
spread amount required. 
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
NULL
IR Reset Frequency Period 1 Floating rate reset 
frequency period-leg 1
C C Required if UPI.[Instrument type] = ‘Swap’ and UPI.[Underlier type] ≠ 
‘Fixed -Fixed’, else {blank}
When populated with ‘EXPI', [Reset Frequency Period Multiplier 1] 
must be ‘1’
MNTH
CO, CR, 
EQ, IR
Leg 1 - Spread Amount Spread-Leg 1 C C IR - Required if [Leg 1 - Fixed Rate Initial] is not populated and 
[Post-priced swap indicator] = ‘False’, and UPI.[Instrument type] 
≠ ‘[[Option]]’, else {blank}
Restricted to Amount-Numeric-21-10 if [CDE - Spread notation-Leg 1] 
= 3 (The length is not fixed but limited to 11 numerical characters 
including up to ten numerical characters after the decimal point.)
Restricted to Amount-Numeric-5-0 if [CDE - Spread notation-Leg 1] = 
4
NULL
NACK: A value will be 
required because this 
is an IR basis swap and 
it is Float Float.  Spread 
amount is expected to 
be populated in Leg 2. 
CO, CR, 
IR
Leg 2 - Fixed Rate Initial Fixed rate-Leg 2 O O NULL
IR Leg 2 - Reset Frequency 
Period
Floating rate reset 
frequency period-leg 2
C O When populated with ‘EXPI', [Leg 2 - Reset Frequency Period 
Multiplier] must be ‘1’ MNTH
CO, CR, 
EQ, IR
Leg 2 - Spread Amount Spread-Leg 2 O O Restricted to Amount-Numeric-21-10 if [CDE - Spread notation-Leg 2] 
= 3 (The length is not fixed but limited to 11 numerical characters 
including up to ten numerical characters after the decimal point.)
Restricted to Amount-Numeric-5-0 if [CDE - Spread notation-Leg 2] = 
4
0.000003

---

## Page 63

[[DTCC]] Internal (Green)
8
FOR DISCUSSION: IR Float - Float: Validation PROPOSAL
**Updated** [Leg 1 - Spread Amount]: 
IR: Required if [Leg 1 - Fixed Rate Initial] is not populated and [Post-priced swap indicator] = ‘False’, and 
UPI.[Instrument type] ≠ ‘[[Option]]’ and [Leg 2 - Spread Amount] is not populated, else {blank}
**New** [Leg 2 - Spread Amount]: 
IR: Required if [Leg 1 - Fixed Rate Initial] is not populated and [Post-priced swap indicator] = ‘False’, and 
UPI.[Instrument type] ≠ ‘[[Option]]’, and [Leg 1 - Spread Amount] is not populated, else {blank}

---

## Page 64

[[DTCC]] Internal (Green)
GTR North America Re-Write 
Upcoming Releases
North America Working Group – Oct 18th, 2023

---

## Page 65

[[DTCC]] Internal (Green)
2
UAT – Oct 26, 2023 PROD – Jan 28, 2024
**Updated** [Reset Frequency Period 1]: 
IR: Required if UPI.[Instrument type] = ‘Swap’ and UPI.[Underlying [[Asset]] Type] ≠ (‘Fixed - Fixed’ or {blank}) and 
[Leg 2 - Reset Frequency Period] is {blank}, else {blank} 
**NEW** [Leg 2 - Reset Frequency Period]: 
IR: Required if UPI.[Instrument type] = ‘Swap’ and UPI.[Underlying [[Asset]] Type] ≠ (‘Fixed - Fixed’ or {blank}) and 
[Reset Frequency Period 1] is {blank}, else {blank} 
NOAGTR-2581: IR Fixed - Float: UPI Validation Change
• [[[settlement]] Currency]
• For EQ, FX, IR and CR, Required if UPI.[Delivery Type] = ‘Cash’, else {blank}
• For CO Required if [[[settlement]] Type] = ‘Cash’
• [[[settlement]] Type] 
• This field is not applicable for [[SEC]] since it is commodities only
• This jurisdiction will be updated from 'YES' to 'NO' in the message spec
NOAGTR- 2599: UPI Validation Update for [[[settlement]] Currency] & [[[settlement]] Type] Fields 

---

## Page 66

[[DTCC]] Internal (Green)
3
UAT – Oct 26, 2023 PROD – Jan 28, 2024
The following UPI validations will be removed as PPD Capping and LNOFS changes have been deferred:
• For TERM and EROR on PPD:
• Required for PPD when [Primary [[Asset]] Class] = Credit
• For TERM and EROR on Trade State:
• Required for Trade State when [Primary [[Asset]] Class] = Credit , [Large notional off-facility swap election 
indicator] is blank and [SEF or DCM Indicator] = False
NOAGTR-2609: Removal of validation from [UPI] field for TERM & EROR action type
NOAGTR-2644: Update to UPI validation application for Canada submissions
UAT – Nov 21, 2023 PROD – Jan 28, 2024
The [Post-Priced Swap Indicator] field is not applicable for Canada submissions and is used in the following 
fields for UPI validations:
• [Leg 1 - Spread Amount]
• [Leg 1 - Fixed Rate Initial]
• [Price 1 – Price]
• [Strike Price]
After this change, these fields will no longer NACK when the [Post Priced Swap Indicator] is not populated 
for Canada submissions. Note: If the field is populated, the UPI validation will be applied for processing.

---

## Page 67

[[DTCC]] Internal (Green)
4
Learning Center Updates
• Re-Write Phase 2 Message Specification v2.3
• Re-Write Phase 2 UAT Release Notes
• Working Group Updates
• Re-Write Phase 2 Runbook October 26, 2023, UAT Implementation
• Re-Write Phase 2: Public Price Dissemination Transformation and Time Delay (Published 
10/13/23)
• Re-Write Phase 2: Roadmap (Published 10/13/23)

---

## Page 68

[[DTCC]] Internal (Green)
5
© 2023. All rights reserved. [[DTCC]], and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain 
affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does 
not provide such services.  Each of these affiliates is a separate legal entity, subject 
to the laws and regulations of the particular country or countries in which such entity 
operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and 
the services they offer.

---

## Page 69

[[DTCC]] Internal (Green)

---

## Page 70

[[DTCC]] Internal (Green)
GTR North America Re-Write 
Upcoming Releases
North America Working Group – Nov 1st 2023

---

## Page 71

[[DTCC]] Internal (Green)
2
NOAGTR- 2597: ‘INTERNAL’ and ‘PLID’ for [Other Payment Payer [[ID]] Type] &  [Other Payment 
Receiver Type] fields are NACKing in UAT. 
UAT – Nov 9, 2023 PROD – Jan 28, 2024
If the [Other payment receiver [[ID]] Type] & [Other payment payer [[ID]] Type] is ‘INTERNAL’ or ‘PLID’ 
values in [Other Payment Payer [[ID]]] & [Other Payment Receiver [[ID]]] fields are being validated 
against GLIEF for a valid LEI. This will be resolved in this update.  

---

## Page 72

[[DTCC]] Internal (Green)
3
UAT PPD Dashboard URL: https://portalu.[[DTCC]].com/ppd/ppd/index.html
PPD UAT Dashboard Enhancements - November 21, 2023 
NOAGTR-1874: Additional enhancements for the PPD Dashboard will be implemented in UAT in 
November including:
• Ticker and Search updates for fields that are not displaying all submitted values after the 
decimal (e.g. all 18 digits for Spread amount when notation = 1)
• Update to PPD Dashboard Ticker and Search showing 0's rather then NULL/{blank} for a subset 
of fields
• Ticker and Search field names will be updated to align to the slice files 
• Call and Put Amount and Currency, Price and [[settlement]] Location-Leg 1 are not showing in 
ticker/search and will be updated.
• Timestamp fields will be updated to include 'z' at the end.
• Addition of Report Center and download capability for search screen results
• Scrolling capabilities will be refined. 

---

## Page 73

[[DTCC]] Internal (Green)
4
Learning Center Updates
• Re-Write Phase 2 Message Specification v2.4
• Re-Write Phase 2 UAT Release Notes
• Working Group Updates
• Re-Write Phase 2 Functional Change v1.3
• PPD User Guide v2.2 
• Error Codes v9
• Re-Write Phase 2 Roadmap  

---

## Page 74

[[DTCC]] Internal (Green)
5
© 2023. All rights reserved. [[DTCC]], and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain 
affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does 
not provide such services.  Each of these affiliates is a separate legal entity, subject 
to the laws and regulations of the particular country or countries in which such entity 
operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and 
the services they offer.

---

## Page 75

[[DTCC]] Internal (Green)

---

## Page 76

[[DTCC]] Internal (Green)
GTR North America Re-Write 
Upcoming Releases
North America Working Group – Nov 1st 2023

---

## Page 77

[[DTCC]] Internal (Green)
2
NOAGTR- 2597: ‘INTERNAL’ and ‘PLID’ for [Other Payment Payer [[ID]] Type] &  [Other Payment 
Receiver Type] fields are NACKing in UAT. 
UAT – Nov 9, 2023 PROD – Jan 28, 2024
If the [Other payment receiver [[ID]] Type] & [Other payment payer [[ID]] Type] is ‘INTERNAL’ or ‘PLID’ 
values in [Other Payment Payer [[ID]]] & [Other Payment Receiver [[ID]]] fields are being validated 
against GLIEF for a valid LEI. This will be resolved in this update.  

---

## Page 78

[[DTCC]] Internal (Green)
3
UAT PPD Dashboard URL: https://portalu.[[DTCC]].com/ppd/ppd/index.html
PPD UAT Dashboard Enhancements - November 21, 2023 
NOAGTR-1874: Additional enhancements for the PPD Dashboard will be implemented in UAT in 
November including:
• Ticker and Search updates for fields that are not displaying all submitted values after the 
decimal (e.g. all 18 digits for Spread amount when notation = 1)
• Update to PPD Dashboard Ticker and Search showing 0's rather then NULL/{blank} for a subset 
of fields
• Ticker and Search field names will be updated to align to the slice files 
• Call and Put Amount and Currency, Price and [[settlement]] Location-Leg 1 are not showing in 
ticker/search and will be updated.
• Timestamp fields will be updated to include 'z' at the end.
• Addition of Report Center and download capability for search screen results
• Scrolling capabilities will be refined. 

---

## Page 79

[[DTCC]] Internal (Green)
4
Learning Center Updates
• Re-Write Phase 2 Message Specification v2.4
• Re-Write Phase 2 UAT Release Notes
• Working Group Updates
• Re-Write Phase 2 Functional Change v1.3
• PPD User Guide v2.2 
• Error Codes v9
• Re-Write Phase 2 Roadmap  

---

## Page 80

[[DTCC]] Internal (Green)
5
© 2023. All rights reserved. [[DTCC]], and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain 
affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does 
not provide such services.  Each of these affiliates is a separate legal entity, subject 
to the laws and regulations of the particular country or countries in which such entity 
operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and 
the services they offer.

---

## Page 81

[[DTCC]] Internal (Green)

---

## Page 82

[[DTCC]] Internal (Green)
GTR North America Re-Write 
Upcoming Releases
North America Working Group – Nov 29th 2023

---

## Page 83

[[DTCC]] Internal (Green)
2
UAT – Jan 11, 2024 PROD – Jan 28, 2024
Implementation of FpML Schema version 5.5 – 14 which includes the <step> element in the transparency 
schema.
After the FpML update, the below fields will be able to be submitted for IR PPD:
• CDE - Effective date of the notional amount-Leg 1
• CDE - Effective date of the notional amount-Leg 2
• CDE - Notional amount in effect on associated effective date-Leg 1
• CDE - Notional amount in effect on associated effective date-Leg 2
NOAGTR-2789: Implementation of Updated FpML Schema

---

## Page 84

[[DTCC]] Internal (Green)
3
Learning Center Updates
• PROD Message Specification v5.6
• Re-Write Phase 2 Message Specification v2.6
• Re-Write Phase 2 UAT Release Notes
• Re-Write Phase 2 Working Group Updates

---

## Page 85

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

## Page 86

[[DTCC]] Internal (Green)

---

## Page 87

[[DTCC]] Internal (Green)
GTR North America Re-Write 
Upcoming Releases
North America Working Group – Dec 13th 2023

---

## Page 88

[[DTCC]] Internal (Green)
2
UAT – Dec 7, 2023 PROD – Jan 28, 2024
Deployment of the Search tab onto the PPD Website.
• This screen allows for the use of filters to search for a particular transaction.
NOAGTR-2769: All Jurisdiction Search CSV Download
Additional xpaths added to support [[Novation]]/feeTrade FpML structure for [CDE - Effective date of the notional amount-
Leg 1] & [CDE - Effective date of the notional amount-Leg 2] on Trade State and PPD
CDE - Effective date of the notional amount-Leg 1
$transaction/capFloor/capFloorStream/calculationPeriodAmount/calculation/notionalSchedule/notionalStepSchedule/step/stepDate/text()| 
$transaction/swap/swapStream[1]/calculationPeriodAmount/calculation/notionalSchedule/notionalStepSchedule/step/stepDate/text() | 
$transaction/swaption/swap/swapStream[1]/calculationPeriodAmount/calculation/notionalSchedule/notionalStepSchedule/step/stepDate/text() | 
$transaction/capFloor/capFloorStream/calculationPeriodAmount/calculation/knownAmountSchedule/step/stepDate/text() | 
$transaction/swap/swapStream[1]/calculationPeriodAmount/calculation/knownAmountSchedule/step/stepDate/text() | 
$transaction/swaption/swap/swapStream[1]/calculationPeriodAmount/calculation/knownAmountSchedule/step/stepDate/text()
CDE - Effective date of the notional amount-Leg 2
$transaction/swap/swapStream[2]/calculationPeriodAmount/calculation/notionalSchedule/notionalStepSchedule/step/stepDate/text() | 
$transaction/swaption/swap/swapStream[2]/calculationPeriodAmount/calculation/notionalSchedule/notionalStepSchedule/step/stepDate/text() | 
$transaction/swap/swapStream[2]/calculationPeriodAmount/calculation/knownAmountSchedule/step/stepDate/text() | 
$transaction/swaption/swap/swapStream[2]/calculationPeriodAmount/calculation/knownAmountSchedule/step/stepDate/text()
NOAGTR-2800: FPML issue with FeeTrade for PPD and TS
UAT – Jan 11, 2024 PROD – Jan 28, 2024

---

## Page 89

[[DTCC]] Internal (Green)
3
UAT – Jan 11, 2024 PROD – Jan 28, 2024
Date and time within the PPD Website will all be in UTC.
NOAGTR-2817: Date Time in Search in UTC
PPD Dashboard is applying the capping indictor (+) to Total Notional Quantity Fields when 
99999999999999999999.99999 is submitted. This will be corrected after deployment.
NOAGTR-2826: PPD Dashboard - Capping Indicator is Being Applied to Quantity Fields when 25 9's

---

## Page 90

[[DTCC]] Internal (Green)
4
Learning Center Updates
• Re-Write Phase 2 Message Specification v2.8
• Re-Write Phase 2 UAT Release Notes
• Re-Write Phase 2 Working Group Updates

---

## Page 91

[[DTCC]] Internal (Green)
5
© 2023. All rights reserved. [[DTCC]], and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain 
affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does 
not provide such services.  Each of these affiliates is a separate legal entity, subject 
to the laws and regulations of the particular country or countries in which such entity 
operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and 
the services they offer.

---

## Page 92

[[DTCC]] Internal (Green)

---

## Page 93

[[DTCC]] Internal (Green)
GTR North America Re-Write 
Upcoming Releases
North America Working Group – Dec 20th 2023

---

## Page 94

[[DTCC]] Internal (Green)
2
UAT – Jan 11, 2024 PROD – Jan 28, 2024
[[[Premium]] Amount] field will be parsed when populated for CR Generic Products. This will be resolved in this update.
NOAGTR-2835: Xpath for [[[Premium]] Amount] field when populated for CR Generic is not being 
parsed

---

## Page 95

[[DTCC]] Internal (Green)
3
Learning Center Updates
• Re-Write Phase 2 Message Specification v2.9
• Re-Write Phase 2 UAT Release Notes
• Re-Write Phase 2 Working Group Updates
• NoA Re-Write Phase 2 PROD Runbook

---

## Page 96

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

## Page 97

[[DTCC]] Internal (Green)