---
title: "Upcoming Restructuring Event Testing Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/UAT%20Restructuring%20Event%20Test%20Guide.pdf"
pages: 6
size: "430.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Upcoming Restructuring Event Testing Guide

**Original File:** [UAT Restructuring Event Test Guide.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/UAT%20Restructuring%20Event%20Test%20Guide.pdf)  
**Category:** Other  
**Total Pages:** 6  
**File Size:** 430.7 KB  

---

## Page 1

The new home of MarkitServ, Traiana, TriOptima &Reset
Restructuring EventTesting Guide for Upcoming Restructuring April 2023

---

## Page 2

The new home of MarkitServ, Traiana, TriOptima &Reset 2
Restructuring Testing ScopeRestructuring Event processed on Single Name Trade (Standard European Corporate).[[Seller]] Trigger trumps [[Buyer]] Trigger within first 2 days.Scenario is based on a trade with 4 Maturity Buckets (2.5Y, 5Y, 7.5Y and 10Y). 7.5Y Bucket no auction. (if firms want to perform Movement, please ensure you book trades to fall in this bucket)*Triggering can be performed as following**Full Trigger, Partial Triggers, Partial Triggered with remain untriggered amount, Multiple Triggers***All Transaction must be booked by firmsRestructuring Event processed on Cleared Single Name Trade (Standard European Corporate).[[Seller]] Trigger trumps [[Buyer]] Trigger within first 2 days.Scenario is based on a trade with 4 Maturity Buckets (2.5Y, 5Y, 7.5Y and 10Y). 7.5Y Bucket no auction. . (if firms want to perform Movement, please ensure you book trades to fall in this bucket)*Triggering can be performed as following**Full Trigger, Partial Triggers, Partial Triggered with remain untriggered amount, Multiple Triggers***LCH has agreed to Participate.***All Transaction must be booked by firmsRestructuring Event processed on an Index Tranche.[[Seller]] Trigger trumps [[Buyer]] Trigger within first 2 days.Scenario is based on a trade with 4 Maturity Buckets (2.5Y, 5Y, 7.5Y and 10Y). 7.5Y Bucket no auction. . (if firms want to perform Movement, please ensure you book trades to fall in this bucket)*Triggering can be performed as following**Full Trigger, Partial Triggers, Partial Triggered with remain untriggered amount, Multiple Triggers***All Transaction must be booked by firms**** Tranches to be tested for Triggering purposes only.Restructuring Event processed on the Single Name Component of an Untranched Index.[[Seller]] Trigger trumps [[Buyer]] Trigger within first 2 days.[[Buyer]] Movement trumps [[Seller]] Movement.Scenario is based on a trade with 4 Maturity Buckets (2.5Y, 5Y, 7.5Y and 10Y). 7.5Y Bucket no auction. . (if firms want to perform Movement, please ensure you book trades to fall in this bucket)*Triggering can be performed as following**Full Trigger, Partial Triggers, Partial Triggered with remain untriggered amount, Multiple Triggers***All Transaction must be booked by firms

---

## Page 3

The new home of MarkitServ, Traiana, TriOptima &Reset 3
Restructuring Event DetailsPlease see the below event details, for Restructuring Event.•Please Note: iTraxxEurope trade must be confirmed and registered prior to April 17thto be “re-versioned”•Terminations, Exits and New “Spin-off” Trades will be automatically-generated in TIW after April 25th22:00 UTC – All Triggers must be submitted prior to this deadline to be applied.Event Name VUE APR23 Maturity Bucket DetailsEvent TypeRestructuring Event2.5Y Maturity Bucket Start Date2023-03-20Reference Entity NameVue Entertainment International Limited5Y Maturity Bucket Start Date2025-03-20Underlying Code (ISIN)XS09530851147.5Y Maturity Bucket Start Date2027-03-20Reference Entity [[default]] Date2023-01-2610Y Maturity Bucket Start Date2029-03-20Event Determination Date2023-02-02Re-versioning Process Start Date2023-04-192.5Y Maturity Bucket Recovery Rate0.450000Re-versioning Process End Date2023-04-215Y Maturity Bucket Recovery Rate0.350000Seller Trigger Period End Date2023-04-25 18:00:00 UTC7.5Y Maturity Bucket Recovery RateN/A - No AuctionBuyer Trigger Period End Date2023-04-27 18:00:00 UTC10Y Maturity Bucket Recovery Rate0.150000Movement [[Option]] Start Date2023-05-01 06:00:00 UTCMovement [[Option]] End Date2023-05-02 18:00:00 UTCEvent Processing Start Date (EPSD)2023-05-04Event Processing End Date (EPED)2023-05-04Auction Date2023-05-04Cash [[settlement]] Date2023-05-06Reversioning Amendment Details2.5Y Bucket 5Y Bucket 7.5Y Bucket 10Y BucketIndex NameN/A – The 7.5Y Maturity Bucket will not be auctioned in this Restructuring Event.VersionFactorRED IDTBDTBD TBD


---

## Page 4

The new home of MarkitServ, Traiana, TriOptima &Reset 4
Restructuring Event Schedule & Plan (1/3)Participants should review the below timeline, to better understand the expected test velocity and structure of Restructuring Event testing. Below are examples of Triggering and Movement examples that can be followed to go along with the time-lineCDS / ClearedCDT**For Triggering onlyWeekdayMonthsDate
CDX
AprilWEDTHUFRIMONApril 19April 20April 21April 24TUEApril 25iTraxxEurope Re-Versioning  -Index Trade is registered in TIWITraxxEurope is “Reversioned”Perform Spinoff of the Index and book single name trade which will be eligible for TriggeringValidate TIW ReportsFirms to check CDS transactions are tagged and eligible for TriggeringFirms to check CDS transactions are tagged and eligible for TriggeringLast Day for  ITraxxEurope to be “Reversioned”Continue Spinoff of the Index and book single name trade which will be eligible for Triggering.Validate TIW ReportsContinue Spinoff of the Index and book single name trade which will be eligible for Triggering.Validate TIW ReportsNo Scheduled ActivityTriggering Continues ( [[Seller]]/[[Buyer]] Trigger)Full Trigger, Partial Triggers, Partial Triggered with remain untriggered amount, Multiple TriggersBuyer / [[Seller]] Triggering continuesSeller last day of Triggering/ trumping*Perform Triggering as you would in Prod. (MQ, UI, Spreadsheet Upload)Validate TIW ReportsValidate TIW ReportsNo Scheduled ActivityTriggering WindowTriggering WindowRe-versioning End DateTriggering Continues ( [[Seller]]/[[Buyer]] Trigger)Full Trigger, Partial Triggers, Partial Triggered with remain untriggered amount, Multiple Triggers*Perform Triggering as you would in Prod. (MQ, UI, Spreadsheet Upload)Validate TIW ReportsFirms to check CDS transactions are tagged and eligible for Triggering

---

## Page 5

The new home of MarkitServ, Traiana, TriOptima &Reset 5
IAT Cycle 2: Restructuring Event Schedule & Plan (2/3)WeekdayMonthsDateAprilWEDTHUApril 26April 27FRIApril 28Triggering WindowTrigger End Date – Triggered Trades Terminated, Spin-offs Generated [[EOD]]-[[Buyer]] Triggering continuesBuyer Triggering continuesNo Scheduled ActivityCDS / ClearingCDT** For Triggering OnlyCDXNo Scheduled ActivityMovement [[Option]] begins Validate TIW ReportsMovement [[Option]] beginsValidate TIW ReportsMONTUEMay 1May 2Movement [[Option]] Start DateMovement [[Option]] End DateLast Day to Perform Movement OptionNo Scheduled ActivityNo Scheduled ActivityBuyer last day to triggerPartial Triggered Trade will be Terminated and ExitedNew “Spin-off” Trades GeneratedBuyer last day to triggerPartial Triggered Trade will be Terminated and ExitedNew “Spin-off” Trades GeneratedNo Scheduled Activity

---

## Page 6

The new home of MarkitServ, Traiana, TriOptima &Reset 6
Restructuring Event Schedule & Plan (3/3)WeekdayMonthsDateMAYWEDTHUFRIMONMay 3May 4May 5May 6TUEMay 7-EPSD / EPED / AUCTIONPayments “Lock” ahead of CSDExisting Coupons CancelledRecovery Payments CalculatedAccrual Coupons CalculatedNetting Amounts Calculated CorrectlyValidate TIW ReportsRecovery Payments Locked 12:00 ETAccrual Coupons Locked 12:00 ETValidate IPIS Reports 14:00 ETExisting Coupons CancelledRecovery Payments CalculatedAccrual/Rebate Coupons CalculatedNetting Amounts Calculated CorrectlyValidate TIW ReportsRecovery Payments Locked 12:00 ETAccrual Coupons Locked 12:00 ETValidate IPIS Reports 14:00 ETRecovery Payments Locked 12:00 ETAccrual Coupons Locked 12:00 ETValidate IPIS Reports 14:00 ETRecovery Payments Settled (~02:00 ET)Accrual Coupons Settled (~02:00 ET)Validate Final [[settlement]] Report (~08:30 ET)Positions “Auto-Exited” by TIW (~17:00 ET)Verify “Exits” at TradeServRecovery Payment Settled (~02:00 ET)Accrual Coupon Settled (~02:00 ET)Validate Final [[settlement]] Report (~08:30 ET)“Re-versioning Amendment” is reflected correctly Recovery Payments Settled (~02:00 ET)Accrual Coupons Settled (~02:00 ET)Validate Final [[settlement]] Report (~08:30 ET)Positions “Auto-Exited” by TIW (~17:00 ET)Verify “Exits” at TradeServExisting Coupons CancelledRecovery Payments CalculatedAccrual Coupons CalculatedCurrent Period’s Coupons RecalculatedNetting Amounts Calculated CorrectlyIndex Tranches are Successfully “Re-versioned”Re-versioning Amendments Register at TradeServValidate TIW ReportsCDS/ ClearingCDT**For Triggering OnlyCDX
Cash [[settlement]] Date (CSD)No Scheduled Activity-No Scheduled Activity