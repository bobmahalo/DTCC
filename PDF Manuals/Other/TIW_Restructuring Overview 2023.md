---
title: "Restructuring Overview 2023"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/TIW_Restructuring%20Overview%202023.pdf"
pages: 27
size: "1824.0 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Restructuring Overview 2023

**Original File:** [TIW_Restructuring Overview 2023.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/TIW_Restructuring%20Overview%202023.pdf)  
**Category:** Other  
**Total Pages:** 27  
**File Size:** 1824.0 KB  

---

## Page 1

RESTRUCTURING OVERVIEWLucy PredaFebruary 14, 2023

---

## Page 2

• Overall Restructuring Process• Introduction• CDS Triggering Overview• Index Reversioning / Triggering Overview• Contingent Triggering on Cleared Positions• Accessing Restructuring Dashboard• Restructuring Master Record• CDS Triggering• CDS Trumping• Index Tranche Triggering• Index Tranche Trumping• [[DTCC]] Spinoff Post Triggering End Date• Movement [[Option]]• Auction2
Agenda

---

## Page 3

3
Reversion
•DC accepts request•https://www.cdsdeterminationscommittees.org/•[[DTCC]] will reversion the Index/Itraxx non-tranche trades based on the new RED S&P Provides•Firms book spin off from Index/Itraxx up until Triggering Period•Clearing Houses upload RMP tableTriggering
•ISDA publishes Final [[obligations]] including Maturity Buckets•[[Seller]] Trigger 2 Days ([[Seller]] Trumps)•[[Buyer]] Trigger Full 5 Days•Exercise Deadline on the 5thBusiness Day•Triggering Period End Date - [[DTCC]] will Exit and rebook Partial TriggersMovement
•Auction Details Published for each Maturity Bucket•3 Day Movement [[Option]]•[[Buyer]] Trumps [[Seller]]•Movement [[Option]] Deadline – on the 3rdBusiness DayAuction
•Auction Date / Final Price•Triggered/UnTriggered Index Tranches will be reversioned•Cash [[settlement]] Date•CDS Positions will be EXITED
Overall Restructuring Process

---

## Page 4

• RestructuringType of ‘soft’ credit event where a company has restructured the organization in such a way as to deplete its value. − A Soft Credit event provides the [[Option]] to trigger a contract. Firms needs to elect to participate in a restructuring event on a trade-by-trade level (Trader decision). Firms choose in opting into a credit event vs. a potential hard credit event that can take place some time in the future. − A hard Credit Event would automatically trigger your contract. On Oct 2010,  Warehouse rolled out its new functionality to support the Triggering of restructuring events. Following is specific to MMR/MR events.• The following is specific to MMR/MR events:− Firms may elect to fully or partially Trigger the notional amount which involves Warehouse splitting the trades to subject only the partial Trigger amount to the credit event.− Triggered trades, following Auction results, will get payment calculations updated and will be processed through the same process followed for Credit Events.• The TIW restructuring process in the is unique and complex as it consists of different variations of activity and Client interaction depending upon the Product that is being processed. Trade Confirmation; Index reversioning; Firm Spin Off; Triggering; [[DTCC]] Spin Off on Partial Triggered Trades; Movement; Auction Upon DC announcement, TIW will set up the Restructuring Event Master Record with agreed Reference Entity, ISIN, Indices4
Introduction

---

## Page 5

• There will be a 5-Day Triggering window for CDS and Index Tranches. [[Seller]] Triggers Trump [[Buyer]] Triggers (Trumping example below) [[Seller]] can Trigger first 2 days[[Buyer]] can Trigger all 5 days[[Seller]] Trigger Deadline 11:00 Eastern Standard Time / 4:00PM London time[[Buyer]] Trigger Deadline 11:00 Eastern Standard Time / 4:00PM London timeTriggers will be processed when received in [[DTCC]] queue. Trigger will be rejected at 11:00:01 / 4:00:01PM London time or laterThe [[Seller]] Trigger Trumps the [[Buyer]] Trigger throughout the entire Triggering period; however, the [[Buyer]] has three additional days to Trigger than the [[Seller]]. Triggering must be in 1mil increments. Once a Trigger is submitted, it cannot be retracted. [[Seller]] Trumps the [[Buyer]] on Full notional and if available notional is less than [[Seller]] Trigger amount.Example of [[Seller]] Trumping [[Buyer]]:Trade Notional = 100MMBuyer Trigger = 50MM(or RENA Amount if its an Index Tranche). [[Buyer]] Trigger gets applied according to its MaturitySeller Trigger = 80MM(or RENA Amount if its an Index Tranche). [[Seller]] Trigger gets applied to Longest available bucket. [[Seller]] will Trump [[Buyer]] Trigger and the outcome will be:**RENA (Reference Entity Notional Amount) [[Seller]] Trigger = 80MM(or RENA Amount)[[Buyer]] Trigger = 20MM(Remaining that can be allocated) (or RENA Amount)Index Tranche Triggers must be submitted in RENA amount which will be shown and available on the GUI.RENA = Pool size * Entity Component WeightingWhere Pool Size = Notional Amount / (Exhaustion Point - Attachment Point) Note: After [[Seller]] deadline the [[Buyer]] will only see what is remaining on the notional, in this case 20MM. (or RENA Amount)5
CDS Triggering Overview

---

## Page 6

•Triggerscan be submitted via MQ, CSVupload or through the Restructuring GUICEN(Credit Event Notice/Trigger) is single-sided; that is, it is unilateral and does not require acceptance from the counterparty. This is considered the legal delivery of the credit event notice.NOTIFYCENIndicates Triggering on the trade notional occurred outside of TIW (for example, by fax). This is not the legal Trigger until it is fully Applied in TIW. Firms tend to use this method if one of the party does not have access to [[DTCC]] portal and requests the other party to submit Trigger on their behalf. A NOTIFYCEN must be applied to the trade before the Trigger period end date/time in order to be reflected on the transaction, before the TIW performs the partial Trigger automated spin-off. The deadline for the manual acceptance of a NotifyCENmessage by the Receiver is Auction Date -1 calendar day. • Reports Triggering Status Report (Runs every 2 hours)Triggering Summary Report (Runs every 2 hours)Partial Trigger Spin-off Transaction Activity (Daily during spin-off processing period) • There are 10 Maturity Buckets (2.5Y, 5Y, 7.5Y, 10Y, 12.5Y, 15Y, 20Y and 20+Y). Each Triggered position will automatically be inserted in the appropriate Bucket according based on its Maturity Date published by ISDA DC. (**[[Seller]] Triggers go to longest available Bucket. [[Buyer]] Triggers go to corresponding Buckets according to their schedule termination date)Note: There are times where not all Buckets will be Active, nor would it have an Auction • Partially Triggered trades will be Terminated/Exited at [[EOD]] of Triggering period End Date and ends prior to Movement period Start Date. Job will continue to run daily in case some positions are in Uncertain status. [[DTCC]] will also book the new Triggered single name shapes and submit via DSMatch.6
CDS Triggering Overview Cont.

---

## Page 7

• Index/Itraxx Positions are booked and confirmed in [[Tradeserv]]• All TIW “Certain” index trades will be picked up for processing (excluding Options)• TIW will reversion the Index/Itraxx positions. Options are excluded• Report will be available during re-versioning periodUntranched Index Re-versioning Report Event Exception Report (Daily during re-versioning period)Event Exception Report (Daily during re-versioning period)• It is the firm's responsibility to book the Single name CDS Spin Off component from the Index and submit new trades via [[Tradeserv]]. These will be registered in the TIW for Triggering. Bilateral trades should be booked with original Trade Date. In order to follow this best practice without regenerating historic cash flows, a Spin-off Trade must be booked in [[Tradeserv]]: (i) as a “non-standard” Transaction Type (e.g. European Corporate, North America Corporate, etc.), and (ii) with the “First Payment Period Accrual Start Date” specified as the date of the Fixed Rate Payer Payment Date immediately prior to the relevant DC Credit Event Announcement.Cleared Spin-off Trades are booked/confirmed as new cleared single name positions with a Trade Date equal to the cleared date of the restructuring matched pairs (“RMP”) processing , an Effective Date equal to Trade Date + 1, and are netted with existing single name positions consistent with clearinghouse rules.7
Index Reversioning / Triggering Overview

---

## Page 8

• Since the overriding concern of the clearing house is to always remain in a flat position, TIW will automatically generate the Trigger/Movement messages to another cleared transaction (or transactions) to keep the clearing house in a flat position. Furthermore, cleared transactions can be Triggered by the [[participant]] and/or the clearing house, similar to non-cleared transactions. • Any Triggering activity by the dealers will then be automatically passed on by the TIW in accordance with the tables of RMPs. Restructuring Matched Pairs (RMPs), linking trades with one dealer to trades with other dealers. Example:
8
Contingent Triggering on Cleared Positions


---

## Page 9

In the Restructuring Dashboard, you can search for the restructuring event. Accessing Restructuring Dashboard

---

## Page 10

Restructuring Master record will show the triggering windows and the relevant dates
Restructuring Master Record

---

## Page 11

All auctionable buckets will have different RED IDs for the maturity buckets. E.g. New REDs 4 represents the 10Y maturity bucketRestructuring Master Record Cont.

---

## Page 12

12
Under "TriggerableTransaction" you can searchvia [[DTCC]] TRI, to see thetrades that can be triggered.By clicking on the "Trigger"tab in the restructuringdashboard and clicking onthe trade to be triggered thiswill allow the [[Buyer]] to triggerthe trades
CDS Triggering

---

## Page 13

13
You can then enter the Trigger Amount that you choose to trigger. Once this has been entered, the ‘Trigger’ key is selected thus triggering the trade.CDS Triggering Cont.
Note: Triggering must be in 1M increments unless remaining triggering is less than 1M (less than 1M Trigger Amount only occurs when Triggering RENA amount

---

## Page 14

14
CDS Triggering Cont.From the Restructuring Dashboard, you are now able to see both ‘Message Activity – Delivered’ and ‘Message Activity – Received’. This is an enhancement from the legacy platform.

---

## Page 15

Party B ([[Seller]]) trumps the [[Buyer]] as per the rule. Although the [[Buyer]] Trigger Amount was for 30M on the trade, the [[Seller]] trumpswill Trump the [[Buyer]] by Triggering 80M and 20M will be left for the [[Buyer]] . Again, [[Seller]] can only trump the first 2 days of triggering.
CDS Trumping


---

## Page 16

16
CDS Trumping Cont.On the Position under “Warehouse – Restructuring Event Summary” Tab, you can see the trumping taking place. The [[Seller]] has taken the full 80M and the [[Buyer]] now has 20M.  

---

## Page 17

By clicking on the Trigger tab in the restructuring dashboard and clicking on the trade to be triggered this will allow the [[Buyer]] to trigger the tradesYou can search via  [[DTCC]] TRI, to see the  trades that can be triggered.Index Tranche Triggering

---

## Page 18

You can then enter the amount in RENA that you choose to trigger. Once this has been entered, the ‘Trigger’ key is selected thus triggering the trade.
Note: Triggering must be in 1MM increments unless remaining triggering is less than 1MM. If amount is less than 1MM, you would then trigger the full amount or trigger 1MM. Index Tranche triggering must be entered in the RENA amount.
Index Tranche Triggering Cont.

---

## Page 19

The Trigger Process Results shows that the 5MM RENA has been successfully submitted by the [[Buyer]].
Index Tranche Triggering Cont.

---

## Page 20

20
From the Restructuring Dashboard, you are now able to see both ‘Message Activity – Delivered’ and ‘Message Activity – Received’Index Tranche Triggering Cont.

---

## Page 21

The Trigger Process shows 10MM RENA notional has been submitted by the SellerParty B ([[Seller]]) trumps the [[Buyer]] as per the rule. Although there was only an untriggered RENA amount of 8,340,000 on the trade, the [[Seller]] trumps the [[Buyer]] and thus can trigger and additional amount. (which was chosen to be 10MM) and the [[Buyer]] triggered amount is thus reduced from 5MM to the remaining 3,340,000 RENA amount.Index Tranche Trumping

---

## Page 22

The [[Buyer]]’s 5M triggered amount has been reduced to   3,340,000This is because the [[Seller]] triggered 10MM and trumped the [[Buyer]]. Index Tranche Trumping Cont.

---

## Page 23

After the Triggering window has ended for both [[Buyer]] and [[Seller]], the trade will then be Terminated and Exited and the Spin-off trades will be generated.The Termination and Restructuring Exit are shown in the Lifecyle Event SummaryNote: Only partial and multiple triggered trades will be spun off.Under “Warehouse – Restructuring Event Summary”, you will see the Spin-Off trades that were auto-generated. New [[DTCC]] TRIs will be provided.
[[DTCC]] Spinoff Post Triggering End Date

---

## Page 24

Firms are provided a 3-Day window for [[Buyer]]/[[Seller]] Movement. Movement [[Option]] is “Optional”Movement [[Option]] is only applicable on trades that are triggered to a maturity bucket that will nothave an Auction. This will be determined by the Determination committee. Movement  can be submitted via MQ, CSV upload or in the Restructuring GUIMovementwill only be available during the Movement Period. Movement submitted by the [[Buyer]] amends to the next-shortest maturity bucket where Auction = YMovement submitted by the [[Seller]] amends to the longest-dated maturity bucket where Auction = YMovement submitted by the [[Buyer]] trumps movement submitted by the [[Seller]].[[Seller]] will always fall in the longest Bucket regardless of Maturity Date. [[Seller]] cannot move if [[Seller]] Bucket does not have an Auction. However, [[Buyer]] can move on behalf of the [[Seller]].ReportsAny Movement record will be captured in the Triggering Status reports24
Movement [[Option]] 

---

## Page 25

By clicking on the Movement tab in the restructuring dashboard and clicking on the triggered trade, this will allow to move the trade to a different maturity bucket that has an Auction. Movement will always go to the next lowest applicable Auctionable bucket.  Again, [[Seller]] will always fall in the longest Bucket regardless of Maturity Date. [[Seller]] cannot move if [[Seller]] Bucket does not have an Auction. However, [[Buyer]] can move on behalf of the [[Seller]].
Movement [[Option]] Cont.  

---

## Page 26

Event Preconditions (CDS/Index Tranches)• The following will drive whether the trade will be included in the event:Event Determination Date, Event Processing Start Date, End date and Cash [[settlement]]Warehouse Trade Status must be "Certain"Positions must have ”Calc Flag” set to "Yes“Positions must have been Triggered26
Auction

---

## Page 27

27
Auction Cont.• Phase I (Event Processing Start Date (EPSD) / Event Processing End Date (EPED) / Auction Date Cancel all future dated coupon payments and Calculate the substitute coupon paymentCalculate the recovery amountFor Tranches, the latest version of the Index will be reflected on the position. An amendment will be posted. For each of the maturity Buckets there will be a revised Underlying Name and RED [[ID]]. (New Underlying Name and RED [[ID]] will be published by S&P)oThis will apply to both Triggered and Untriggered Positions oNew cashflows are created using the new index factor. oTranches will adjust for any loss/recovery regardless of paymentPrior/After [[settlement]]:Warehouse Sends Net Payment Instructions to CLS Firms receive Net [[settlement]] from CLS• Reports: Adherence Activity Report (Daily during Auction processing)Event Cashflow Report (Daily from Auction date to cash [[settlement]] date• Phase II – (CSD) Cash [[settlement]] DateCDS positions will Exit Untriggered trades will remain live in the TIWNote: Auction will be processed as a Hard Credit Event. 