---
title: "GSD Same-Day Settling Service & Pair-Off Service Overview"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd146_sds_po_service_overview_20210120.pdf"
pages: 11
size: "251.2 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD Same-Day Settling Service & Pair-Off Service Overview

**Original File:** [gsd146_sds_po_service_overview_20210120.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd146_sds_po_service_overview_20210120.pdf)  
**Category:** GSD  
**Total Pages:** 11  
**File Size:** 251.2 KB  

---

## Page 1

 
 
 
 
 
[[FICC]] – [[GSD]] 
[[GSD]] SAME-DAY SETTLING SERVICE & PAIR-OFF SERVICE OVERVIEW 
VERSION 1.0.2 
JANUARY 20, 2021 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: January 20, 2021 
Publication Code: GSD146 
Service: [[FICC]] – [[GSD]]  
Title: [[GSD]] Same-Day Settling Service & Pair-Off Service Overview 
 
 
The [[GSD]] Same-Day Settling Service & Pair-Off Service Overview (hereinafter, the "document") is provided as a 
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
document will find the most current version of the document on [[DTCC]]’s Learning Center site, www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow 
[[FICC]]’s most current document. 

---

## Page 3

 
 
TABLE OF CONTENTS 
Background .......................................................................................................................................................... 4 
Overview of DVP Service Expansion ................................................................................................................. 5 
[[GSD]] Same-Day Settling Service ........................................................................................................................ 5 
[[GSD]] Pair-Off Service .......................................................................................................................................... 6 
Requirements for Members ................................................................................................................................. 7 
Additional Aspects of the Proposal ................................................................................................................... 8 
Client and Service Impact ................................................................................................................................... 9 
Client Base Impacted by New Services .............................................................................................................. 9 
Services Impacted .............................................................................................................................................. 9 
Appendix ............................................................................................................................................................. 10 
 

---

## Page 4

[[GSD]] Same-Day Settling Service & Pair-OFF Service Overview 
Background 4 
BACKGROUND 
• Feedback received from Members for [[FICC]] to consider same-day [[settlement]] of DVP repo transactions. 
• This expansion of the [[FICC]]/[[GSD]]”s DVP Service included: 
o Expanding its trade [[Novation]], guarantee of [[settlement]] and risk management services to Same-Day 
Settling Trades1. 
o Offering a facility to [[pair off]] Members’ failing [[obligations]] in an automated process. 
 
1 “Same-Day Settling Trade” would mean (i) a Start Leg of a Netting [[Member]]’s Repo 
Transaction where the Scheduled [[settlement]] Date of the Start Leg is the current Business Day, 
(ii) an As-Of Trade of a Netting [[Member]] where the Scheduled [[settlement]] Date of the Start Leg 
is the previous Business Day and the End Leg is the current Business Day or thereafter, or (iii) a 
Sponsored [[Member]] Trade within the meaning of subsection (b) of that definition (refer to [[GSD]] Rulebook, 
Section 1 Definitions) that meets the requirements of either (i) or (ii) above. 

---

## Page 5

[[GSD]] Same-Day Settling Service & Pair-OFF Service Overview 
Overview of DVP Service Expansion 5 
OVERVIEW OF DVP SERVICE EXPANSION 
[[GSD]] Same-Day Settling Service 
The following has been implemented as part of [[GSD]]’s Same-Day Settling Service: 
• [[GSD]] has expanded its [[Novation]], guarantee, risk management and [[settlement]] services to its Members’ 
eligible and compared Same-Day Settling Trades. 
• Same-day netting is not part of this expansion. 
• [[GSD]] settles compared Same-Day Settling Trades on a trade for trade basis at contract value. 
• [[GSD]] creates [[securities]] [[settlement]] [[obligations]] resulting from the compared trades and transmits 
[[settlement]] instructions to the Members. 
• [[settlement]] of [[securities]] [[settlement]] [[obligations]] resulting from compared Same-Day Settling Trades 
occurs between Members and [[GSD]]. 
• [[GSD]] expects no changes to Members’ trading practices as result of the service expansion.  
• [[GSD]] expects Members to submit all their eligible bilateral trades for comparison as per the current [[GSD]] 
rules. 
• The current criteria for trade submission, trade validation and trade matching applies to the Same-Day 
Settling Trades.  
• Comparison of the Same-Day Settling Trades occurs pursuant to Rules 6A and 6B. 
• Demand trades submitted by Repo Brokers are deemed compared upon receipt of the trade data from the 
Repo [[Broker]]. 
o For the Same-Day Settling Service, Repo Brokers are required to submit both sides of a repo 
transaction with matching [[Broker]] X-refs to generate [[obligations]] on compared brokered Same-Day 
Settling Trades. Repo Brokers may refer to the [[GSD]] Same-Day Settling Operational Best Practices 
Guide for more information. 
• Brokered Same-Day Settling Trades submitted after 4 PM ET continue to require bilateral comparison for 
[[settlement]] with [[GSD]]. 
• Non-brokered Same-Day Settling Trades between Members require bilateral comparison for [[settlement]] 
with [[GSD]]. 
• [[GSD]] utilizes established Interactive Messages (IM) to communicate to Members the status of their trades 
(MT509 & MT518) and [[obligations]] (MT548) throughout the day. Minor changes have been made to the 
MT509 and MT548 messages to support the Same-Day Settling Service and Pair-Off Service. You may 
refer to the [[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Comparison Input and Output v4.0 
and the [[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output v2.0 for more 
information. 
• [[GSD]] also utilizes established MRO files to provide Members with status updates on their trades and 
[[obligations]] at end of day. There will be no changes to these messaging specifications as a result of this 
initiative. However, paired off [[obligations]] are now reported under MRO 49. 
• [[GSD]] attempts to settle the Same-Day Settling Trades executed and compared after 3PM on a reasonable 
efforts basis*. Refer to the Appendix for more information. 
 
*Subject to Fedwire close.  

---

## Page 6

[[GSD]] Same-Day Settling Service & Pair-OFF Service Overview 
Overview of DVP Service Expansion 6 
[[GSD]] Pair-Off Service 
The following has been implemented as part of [[GSD]]’s Pair-Off Service: 
• Members may opt into the Pair-Off Service. However, once opted in, [[GSD]] controls the automated pair-off 
process. 
• The Pair-Off Service is not be a [[Member]] driven pair-off process. 
• At end of day, [[GSD]] initiates a systemic process to pair-off unsettled [[obligations]] with like par amounts and 
like or unlike monies. 
• Pair-offs are processed on a per [[Member]], per netting eligible [[CUSIP]] basis. There will be no partial pair-
offs. 
• The net par of the paired off [[obligations]] must equal to zero. 
• Any money differences resulting from the pair-off process are to be settled same-day through the intraday 
Funds-Only [[settlement]] (FOS) process. 
• The timing of [[settlement]] for intraday FOS changed to later in the day to accommodate the [[settlement]] of 
the pair-off amounts. Refer to the Appendix for more information. 
• Net money difference amounts (credit or debit) are applied to Members’ accounts as Miscellaneous 
Adjustments on their Intraday Funds [[settlement]] Statement. 
• [[securities]] [[settlement]] [[obligations]] cleared through the pair-off process and any resulting money difference 
amounts will be reported to Members. 
• All [[securities]] [[settlement]] [[obligations]] that remain after the pair-off process has completed are to be netted 
for [[settlement]] the following business day. 
• TMPG charges and mark to market will be applied to those failing [[securities]] [[settlement]] [[obligations]] as per 
the current [[GSD]] Rulebook (“[[GSD]] Rules”).

---

## Page 7

[[GSD]] Same-Day Settling Service & Pair-OFF Service Overview 
Requirements for Members 7 
REQUIREMENTS FOR MEMBERS 
• Submit to [[GSD]] trade details on all transactions upon trade execution. 
• [[DO]] not put repo tracking codes on [[securities]] [[settlement]] [[obligations]] submitted to [[GSD]]. 
• Take action on advisories and cancel requests in a timely and accurate manner. 
• Promptly respond to any inquiry made by [[GSD]] (Operations, Risk & Product Management). 
• Promptly satisfy Funds-Only [[settlement]], Clearing Fund and [[securities]] [[settlement]] [[obligations]] with [[GSD]]. 
• Promptly communicate to [[GSD]] any operational issues or any other issues that would limit the Members’ 
ability to satisfy their [[obligations]] to [[GSD]]. 
• Testing of these new services are mandatory. All affected [[GSD]] Members must attest to their operational 
readiness prior to production go-live.

---

## Page 8

[[GSD]] Same-Day Settling Service & Pair-OFF Service Overview 
Additional Aspects of the Proposal 8 
ADDITIONAL ASPECTS OF THE PROPOSAL 
• [[GSD]] guarantee the [[settlement]] of Members’ eligible Same-Day Settling Trades upon comparison. 
• Members are to adhere to established protocols as defined within the [[GSD]] Rules and applicable 
operational procedures. This may include, but is not limited to: 
o the Schedule of Required Match Data, 
o the Schedule of Required Data Submission Items, 
o the Schedule of Required and Other Data Submission Items. 
.

---

## Page 9

[[GSD]] Same-Day Settling Service & Pair-OFF Service Overview 
Client and Service Impact 9 
CLIENT AND SERVICE IMPACT 
Client Base Impacted by New Services 
• Netting Members and Sponsored Members who execute transactions with Netting Members other than 
their Sponsoring [[Member]] that participate in [[GSD]]’s Repo Netting Services who trade Same-Day Settling 
Trades will be impacted by the proposed expansion of [[GSD]]’s DVP Service. 
• After receiving feedback, [[GSD]] has determined that Repo Brokers have the choice to participate in the 
Same-Day Settling Service.   
• The Same-Day Settling Service is mandatory for all other Netting Members and Sponsored Members who 
execute transactions with Netting Members other than their Sponsoring [[Member]]. However, for Dealer 
Netting Members who have executed Same-Day Settling Trades through an IDB who has opted out of the 
service, the start leg on such transactions must settle outside of [[GSD]]. 
• The Pair-Off Service will be voluntary. Netting Members, excluding Repo Brokers and Sponsored 
Members who execute transactions with Netting Members other than their Sponsoring [[Member]] may opt 
into the Pair-Off Service.  
Services Impacted 
• This expansion would only impact the DVP Service.  
• There is no change to the GCF Repo® or CCIT™ Services.  

---

## Page 10

[[GSD]] Same-Day Settling Service & Pair-OFF Service Overview 
Appendix 10 
APPENDIX 
See below for new intraday Funds-Only [[settlement]] (FOS) processing times:  
Times* Description 
2:00 PM Initial intraday funds-only [[settlement]] (FOS) reports are made available. 
3:32 – 
4:00 PM 
[[GSD]] will commence the systemic pair-off process on participating members failing [[securities]] [[settlement]] 
[[obligations]]. 
4:00 PM Final intraday FOS reports are made available. These reports will include any miscellaneous adjustments 
applied as a result of the pair-off process. 
4:00 PM Funds-Only Settling Banks should be in receipt of Net FOS Figures. At this time Funds-Only Settling Banks 
may begin to acknowledge their Net FOS figures on behalf of Netting Members. 
4:30 PM Time in which Funds-Only Settling Banks must inform [[GSD]] of its acknowledgement and intent to settle or its 
refusal to settle on behalf of a Netting [[Member]]. 
4:30 PM The intraday FOS debits and credits will be executed via [[NSS]]. 
 *All times here in are ET. 
 
 
See below for [[settlement]] times of Same-Day Settling Trades:  
Timeframe* Description 
7:00 AM–3:00 PM [[GSD]] will attempt to settle all matched Same-Day Settling Trades. 
3:01 PM–3:15 PM [[GSD]] will attempt to settle Same-Day Settling Trades executed and matched after 3:00 PM on a 
reasonable efforts basis. 
3:16 PM–3:30 PM In order to settle Same-Day Settling Trades executed and matched after 3:16 PM, clients must 
contact [[GSD]] Operations. [[GSD]] Operations will attempt to settle Same-Day Settling Trades on a 
reasonable efforts basis. 
3:31 PM–5:00 PM In order to settle Same-Day Settling Trades executed and matched after 3:31 PM, clients must 
contact [[GSD]] Operations. [[GSD]] Operations will attempt to settle Same-Day Settling Trades that 
are settling within BNY on a reasonable efforts basis. 
*All times are ET. 
 
 
 
 

---

## Page 11

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 