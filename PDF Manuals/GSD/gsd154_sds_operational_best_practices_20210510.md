---
title: "GSD Same Day Settling Operational Best Practices Reference Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd154_sds_operational_best_practices_20210510.pdf"
pages: 13
size: "219.9 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD Same Day Settling Operational Best Practices Reference Guide

**Original File:** [gsd154_sds_operational_best_practices_20210510.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd154_sds_operational_best_practices_20210510.pdf)  
**Category:** GSD  
**Total Pages:** 13  
**File Size:** 219.9 KB  

---

## Page 1

 
 
 
[[FICC]] – [[GSD]]  
[[GSD]] SAME-DAY SETTLING OPERATIONAL BEST PRACTICES REFERENCE 
GUIDE 
VERSION 1.0.3 
MAY 10, 2021 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: May 10, 2021 
Publication Code: GSD154 
Service: [[FICC]] – [[GSD]]  
Title: [[GSD]] Same-Day Settling Operational Best Practices Reference Guide 
 
 
The [[GSD]] Same-Day Settling Operational Best Practices Reference Guide (hereinafter, the "document") is provided as a 
convenience to Members and is for information purposes only. Although [[FICC]] may make this document available to 
Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have a continuing 
obligation to make available this document or other related information of a certain type.  
 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose 
of any information provided to Members in this document, which is provided as-is. [[FICC]] shall not be liable for any 
loss related to such information (or the act or process of providing such information) resulting directly or 
indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
 
Further, the information contained in this document is subject to change. Members and other authorized users of the 
document will find the most current version of the document on [[DTCC]]’s Learning Center site, 
www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow 
[[FICC]]’s most current document. 

---

## Page 3

 
 
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 4 
General Best Practices for the Same-Day Settling Service ............................................................................. 5 
Best Practices for Submission & Matching of Same-Day Settling Trades..................................................... 6 
Best Practices for the Modification of Same-Day Settling Trades .................................................................. 7 
Best Practices for the Cancellation or Dealer DK of Same-Day Settling Trades ........................................... 8 
Best Practices for the Fail Management of Same-Day [[securities]] [[settlement]] [[obligations]] .......................... 9 
Best Practices for Uncompared Same-Day Settling Trades .......................................................................... 10 
Best Practices for the [[settlement]] of Eligible As-of Repo Transactions ....................................................... 11 
As-of Overnight Repos Eligible for [[settlement]] via Same-Day Settling Service ............................................... 11 
As-of Term Repos Eligible for [[settlement]] via Same-Day Settling Service ....................................................... 11 
Related [[settlement]] Timeframes ........................................................................................................................ 12 
 

---

## Page 4

[[GSD]] Same-Day Settling Operational Best Practices Reference Guide 
Overview 4 
OVERVIEW 
[[GSD]]’s goal for the Same-Day Settling Initiative Working Group was to determine how Netting Members and 
[[GSD]] would operate within the confines of the Same-Day Settling Service. 
During the working group sessions, participants of the working group discussed best practices for timely 
submission and matching of Same-Day Settling Trades1, trade modifications, trade cancellations, daylight 
overdraft fees and fail management as it relates to the Same-Day Settling Initiative. This document aims to 
summarize the discussions held on those topics.  
 
 
1 “Same-Day Settling Trade” would mean (i) a Start Leg of a Netting [[Member]]’s Repo 
Transaction where the Scheduled [[settlement]] Date of the Start Leg is the current Business Day, 
(ii) an As-Of Trade of a Netting [[Member]] where the Scheduled [[settlement]] Date of the Start Leg 
is the previous Business Day and the End Leg is the current Business Day or thereafter, or (iii) a 
Sponsored [[Member]] Trade within the meaning of subsection (b) of that definition (refer to [[GSD]] Rulebook, 
Section 1 Definitions) that meets the requirements of either (i) or (ii) above. 

---

## Page 5

[[GSD]] Same-Day Settling Operational Best Practices Reference Guide 
General Best Practices for the Same-Day Settling Service 5 
GENERAL BEST PRACTICES FOR THE SAME-DAY 
SETTLING SERVICE 
1. The Same-Day Settling Service is voluntary for Repo Brokers. The Same-Day Settling Service is 
mandatory for all other Netting Members and Sponsored Members who execute transactions with Netting 
Members other than their Sponsoring [[Member]]. For Members who have executed Same-Day Settling 
Trades through a Repo [[Broker]] who has opted out of the Same-Day Settling Service, the Start Leg on 
such transactions must settle outside of [[GSD]]. 
2. For Repo Brokers Only: Submit all brokered Same-Day Settling Trades sent to [[GSD]] during the demand 
period as a “balanced set” for [[GSD]] to generate [[settlement]] [[obligations]] for the counterparties of such 
transactions.  
Note:  
See the next section of this document for to learn about balancing criteria. 
3. Actively monitor your firms’ trading activity including Same-Day Settling Trades via the Real-time Trade 
Matching (RTTM®) system, real-time messaging or a combination of the two. This includes monitoring 
trade submissions, trade status changes (such as advisories, modifications, cancel requests and DKs) 
and the [[settlement]] status of your [[securities]] [[settlement]] [[obligations]]. Take immediate action on all known 
advisories, cancel requests and DK Advices per [[GSD]] Rules. 
4. Actively maintain your firms contact information in the [[participant]] Contact List within RTTM
®. Refer to the 
[[FICC]] Contact List User Guide for instructions on how to access and/or update your firms contact 
information. 
5. Pursuant to [[GSD]] Rules, promptly settle all [[securities]] [[settlement]] [[obligations]] in a timely and accurate 
manner. 
6. Pursuant to [[GSD]] Rules, [[DO]] not attempt to deliver positions to [[GSD]] prior to your timely and accurate 
comparison of the related transactions and the subsequent generation of the related [[securities]] [[settlement]] 
[[obligations]] as reported by [[GSD]]. [[GSD]] is not obligated to accept receipt of [[securities]] that are not reported 
to the [[Member]] as [[obligations]]. 
7. [[DO]] not include either a repo tracking code or a contract date on [[securities]] [[settlement]] Instructions sent to 
[[GSD]] to settle [[securities]] [[settlement]] [[obligations]]. This is explained in more detail in Important Notice 
GOV611-19. 
8. Contact [[GSD]] Operations prior to making a return delivery (DK) of any [[securities]] [[settlement]] [[obligations]] 
sent by [[GSD]]. The [[GSD]] Operations hotline is 212-855-7600. 
9. Pursuant to [[GSD]] Rules, [[DO]] not use reversal codes when making an original delivery of [[securities]] 
[[settlement]] [[obligations]] to [[GSD]]. 
10. [[GSD]] will not process partial requests on same-day [[securities]] [[settlement]] [[obligations]] resulting from 
Same-Day Settling Trades. 
11. Promptly alert [[GSD]] Operations to any issues that impede your firms’ ability to submit and compare trades, 
settle cash and [[securities]] [[settlement]] [[obligations]] or otherwise action on trading activity displayed in 
RTTM. 
12. Regarding the Pair-Off Service, [[Broker]] fails are not be eligible for pair-off through the service. 

---

## Page 6

[[GSD]] Same-Day Settling Operational Best Practices Reference Guide 
Best Practices for Submission & Matching of Same-Day Settling Trades 6 
BEST PRACTICES FOR SUBMISSION & MATCHING OF 
SAME-DAY SETTLING TRADES  
1. Pursuant to [[GSD]] Rules, compare all known bilateral Same-Day Settling Trades in a timely and accurate 
manner, to facilitate the [[settlement]] of all same-day [[securities]] [[settlement]] [[obligations]].  
2. [[GSD]] strongly recommends Members compare all brokered Same-Day Settling Trades submitted as 
demand to promote efficiencies in the [[settlement]] process and to ensure Repo Brokers submit transaction 
details known by Dealers.  
3. For [[GSD]] to establish a “balanced set” on a Repo [[Broker]]’s brokered Same-Day Settling Trades submitted 
during the demand period, the Repo [[Broker]] should submit such transactions as follows:  
a. Balanced Set Criteria for 1:1 scenario, i.e. Repo = 1 X 50MM Par vs. Reverse Repo = 1 X 50MM Par:  
• Submission Date = Current Business Date = Start Date  
• Same [[Broker]] [[ID]] #  
• Same [[Broker]] Xref  
• Same [[CUSIP]]  
• Same Par Amount  
• Same Start Amount  
• Same Trade Date  
• Same Start Date  
• Same End Date / [[settlement]] Date  
• Opposite Transaction Type  
b. Balanced Set Criteria for 2:1 / 1:2 scenario, i.e. Repo = 2 X 25MM Par vs. Reverse Repo = 1 X 50MM 
Par or vice versa is Out of Scope for the Same-Day Settling Service.  
c. Balanced Set Criteria for Many : Many scenario, i.e. Repo = 2 X 25MM Par vs Reverse Repo = 5 X 
10MM Par or vice versa is Out of Scope for the Same-Day Settling Service.  
4. During the demand period, [[GSD]] generates same-day [[securities]] [[settlement]] [[obligations]] for the Repo 
Dealer & Reverse Repo Dealer as the counterparties to brokered Same-Day Settling Trades once [[GSD]] is 
in receipt of a “balanced set” for such transactions. These [[obligations]] are to be settled vs. [[GSD]]. In this 
instance, the Repo [[Broker]] will have no [[obligations]] vs. [[GSD]] due to the submission of a balanced position.  
5. Where a Repo [[Broker]] has only submitted one side of a balanced set on its’ brokered Same-Day Settling 
Trades prior to the demand cutoff, the system will generate a same-day [[securities]] [[settlement]] Obligation 
for the Party who is counterparty to the unbalanced brokered Same-Day Settling Trade once the deadline 
for the demand period has been reached. At that same time, the system will also generate an equal and 
opposite same-day [[securities]] [[settlement]] Obligation for the submitting Repo [[Broker]], to offset the 
obligation created for the counterparty. Any Same-Day Settling Trade submitted by a Repo [[Broker]] after 
the deadline for the demand period, will be processed for bilateral comparison, per the Schedule of 
Timeframes in the [[GSD]] Rules.  
6. Bilateral Same-Day Settling Trades are not required to be balanced for [[GSD]] to generate [[obligations]] for 
the counterparties of such transactions. Upon bilateral comparison, same-day [[securities]] [[settlement]] 
[[obligations]] will be generated for the counterparties of such transaction to settle vs. [[GSD]].  
 

---

## Page 7

[[GSD]] Same-Day Settling Operational Best Practices Reference Guide 
Best Practices for the Modification of Same-Day Settling Trades 7 
BEST PRACTICES FOR THE MODIFICATION OF SAME-
DAY SETTLING TRADES  
1. Modifications can affect the economic or non-economic components of a trade. 
2. Only non-economic trade components such as the external reference number (Xref) or secondary 
reference number, can be modified on matched Same-Day Settling Trades. 
3. The modification of an Xref or secondary reference number on any matched Same-Day Settling Trade will 
not impact or change the related same-day [[securities]] [[settlement]] obligation. 
4. For a bilateral unmatched Same-Day Settling Trade, all trade components can be modified, except for the 
submitting [[participant]]’s [[ID]]. 
5. Brokered Same-Day Settling Trades submitted during the demand period are deemed compared upon 
receipt of the trade data from the Repo [[Broker]]. However, until such transactions are matched bilaterally 
by the counterparty, the Repo [[Broker]] may modify all trade components except for the submitting 
[[participant]]’s [[ID]]. 
6. The modification of the Contract Repo Rate on an unmatched brokered Same-Day Settling Trade will not 
impact or change the related same-day [[securities]] [[settlement]] Obligation.  
Note:  
Modifications of other trade components on unmatched brokered Same-Day Settling Trades submitted during the 
demand period, may impact, change or cause the cancellation of the related same-day [[securities]] [[settlement]] 
Obligation. 

---

## Page 8

[[GSD]] Same-Day Settling Operational Best Practices Reference Guide 
Best Practices for the Cancellation or Dealer DK of Same-Day Settling Trades 8 
BEST PRACTICES FOR THE CANCELLATION OR 
DEALER DK OF SAME-DAY SETTLING TRADES  
1. Cancel requests can be submitted prior to matching or after the matching of a Same-Day Settling Trade.  
2. Counterparties to brokered Same-Day Settling Trades submitted during the demand period, can DK such 
transactions until 4:30 PM ET, if such transaction has not previously been matched.  
3. All [[GSD]] Netting Members should take immediate action on all cancel requests and DK Advices.  
4. A brokered Same-Day Settling Trade submitted during the demand period can be unilaterally cancelled by 
the submitting Repo [[Broker]] if the transaction has not been matched.  
5. A brokered Same-Day Settling Trade that has been DK’d, can be unilaterally cancelled by the submitting 
Repo [[Broker]] if the counterparty does not submit a DK Remove and subsequently matches the trade.  
6. Unmatched bilateral Same-Day Settling Trades can be unilaterally cancelled by the submitting [[participant]].  
7. Matched bilateral Same-Day Settling Trades require both parties to submit a cancel on such transactions 
for the system to fully cancel the transactions.  
 

---

## Page 9

[[GSD]] Same-Day Settling Operational Best Practices Reference Guide 
Best Practices for the Fail Management of Same-Day [[securities]] [[settlement]] [[obligations]] 9 
BEST PRACTICES FOR THE FAIL MANAGEMENT OF 
SAME-DAY [[securities]] [[settlement]] [[obligations]]  
1. At the time [[GSD]] ceases to settle [[securities]] [[settlement]] [[obligations]] on a given business day, all remaining 
same-day [[securities]] [[settlement]] [[obligations]] that are in the pending clearance state will be marked as 
fails, which will be netted at the end of the business day with other failed [[obligations]] and the trades that 
are due to settle on the following business day.  
2. Any same-day [[securities]] [[settlement]] Obligation that has failed to settle on its’ original scheduled 
[[settlement]] date, shall be marked-to-market and be accessed a TMPG fail charge (debit or credit).  
 

---

## Page 10

[[GSD]] Same-Day Settling Operational Best Practices Reference Guide 
Best Practices for Uncompared Same-Day Settling Trades 10 
BEST PRACTICES FOR UNCOMPARED SAME-DAY 
SETTLING TRADES  
1. [[GSD]] will not generate [[obligations]] to settle bilateral Same-Day Settling Trades that have not been 
matched, novated or guaranteed by [[GSD]].  
2. Uncompared Same-Day Settling Trades will be purged from the system either after the 2nd business day 
after the Repo Start Date or the 2nd business day after the date of submission.  
3. Same-Day Settling Trades that have been compared one business day after the original Scheduled 
[[settlement]] Date for the Start Leg, will be novated and guaranteed by [[GSD]].  
4. If an obligation is generated to settle a Same-Day Settling Trade that has:  
a. been compared one business day after the original Scheduled [[settlement]] Date for the Start Leg; and  
b. the [[settlement]] of the Start Leg occurred away from [[GSD]] on the original Scheduled [[settlement]] Date 
for the Start Leg, both counterparties to the transaction must contact [[GSD]] Operations to inform them 
that the [[settlement]] of the Start Leg occurred on the previous business day, away from [[GSD]] and that 
they wish for [[GSD]] to cancel their related [[obligations]].  
5. If the above referenced scenario were to occur, [[GSD]] Operations would cancel (terminate) the related 
obligation within the system. [[GSD]] may require written notification of a request to cancel an obligation via 
an electronic or other format. Notification must be made to [[GSD]] Operations by both counterparties, before 
the end of the [[settlement]] period on the day the obligation is generated, so that [[GSD]] Operations can 
cancel the relevant [[obligations]] in a timely manner. If the [[obligations]] are not cancelled or settled by the end 
of the [[settlement]] period for that day, the failing [[obligations]] will be marked-to-market and be accessed a 
TMPG fail charge.  
 

---

## Page 11

[[GSD]] Same-Day Settling Operational Best Practices Reference Guide 
Best Practices for the [[settlement]] of Eligible As-of Repo Transactions 11 
BEST PRACTICES FOR THE [[settlement]] OF ELIGIBLE 
AS-OF REPO TRANSACTIONS 
As-of Overnight Repos Eligible for [[settlement]] via Same-Day Settling 
Service  
[[GSD]] will generate [[obligations]] for the [[settlement]] of the Start Leg and Close Leg on brokered and bilateral 
overnight repo transactions that meet the following criteria:  
• comparison date = current business date,  
• start date = previous business date, and  
• end date = current business date.  
 
The [[settlement]] amount for [[obligations]] generated to settle the Start Leg on such transactions will be at contract 
value. The [[settlement]] amount for [[obligations]] generated to settle the Close Leg on such transactions will be at 
final money.  
As-of Term Repos Eligible for [[settlement]] via Same-Day Settling 
Service  
[[GSD]] will generate [[obligations]] for the [[settlement]] of the Start Leg on brokered and bilateral term repo 
transactions that meet the following criteria:  
• comparison date = current business date,  
• start date = previous business date, and  
• end date = a future business date.  
 
The [[settlement]] amount for [[obligations]] generated to settle the Start Leg on such transactions will be at the 
contract value. The Close Leg on such transactions will go into the net the night prior to [[settlement]] as they [[DO]] 
today.

---

## Page 12

[[GSD]] Same-Day Settling Operational Best Practices Reference Guide 
Related [[settlement]] Timeframes 12 
RELATED [[settlement]] TIMEFRAMES 
Timeframe* Description 
7:00 AM–3:00 PM [[GSD]] will attempt to settle all matched Same-Day Settling Trades. 
3:01 PM–3:15 PM [[GSD]] will attempt to settle Same-Day Settling Trades executed and matched after 3:00 PM on a 
reasonable basis. 
3:16 PM–3:30 PM In order to settle Same-Day Settling Trades executed and matched after 3:16 PM, clients must 
contact [[GSD]] Operations. [[GSD]] Operations will attempt to settle Same-Day Settling Trades on a 
reasonable basis. 
3:31 PM–5:00 PM In order to settle Same-Day Settling Trades executed and matched after 3:31 PM, clients must 
contact [[GSD]] Operations. [[GSD]] Operations will attempt to settle Same-Day Settling Trades that 
are settling within BNY on a reasonable efforts basis. 
*All times are ET. 

---

## Page 13

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 