---
title: "Securities Financing Transactions (SFT) Clearing General User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sftc139_general_ug_2023March10.pdf"
pages: 209
size: "10713.9 KB"
category: "SFT"
ingested_on: "2026-06-05"
---

# Securities Financing Transactions (SFT) Clearing General User Guide

**Original File:** [sftc139_general_ug_2023March10.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sftc139_general_ug_2023March10.pdf)  
**Category:** SFT  
**Total Pages:** 209  
**File Size:** 10713.9 KB  

---

## Page 1

[[securities]] FINANCING 
TRANSACTION ([[SFT]]) CLEARING 
GENERAL USER GUIDE
MAY 31, 2022


---

## Page 2

© 2023 [[DTCC]]. All rights reserved.   [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. 
TOGETHER, and the Interlocker graphic are registered and unregistered trademarks of The Depository 
Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The 
Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of 
these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or 
countries in which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its 
affiliates and the services they offer.
Doc Info: March 10, 2023
Publication Code: SFT139
Service: [[securities]] Financing Transaction ([[SFT]]) Clearing
Title: General User Guide 

---

## Page 3

TABLE OF CONTENTS
1. ABOUT THIS GUIDE 7
1.1 Contact Us 7
1.2 Extension Guidelines 8
2. ABOUT THE [[SFT]] CLEARING SERVICE 9
2.1 Key Design Elements of the [[SFT]] Clearing Service 9
2.2 Sponsorship at [[NSCC]] 10
3. [[SFT]] CLEARING SERVICE ROLES AND RESPONSIBILITIES 11
3.1 Approved [[SFT]] Submitter 11
3.2 [[NSCC]] Full-Service [[Member]] 11
3.3 Sponsoring [[Member]] 11
3.4 Sponsored [[Member]] 11
3.5 Agent Clearing [[Member]] 12
3.6 Agent Client 12
3.7 Separation of Accounts 13
4. GENERAL SYSTEM FLOW 14
5. GENERAL OPERATIONAL FLOW 16
5.1 Processing a New [[SFT]] On-leg 16
5.1.1 Key Business Validations for On-leg Transactions 17
5.1.2 Post-Validation Processing 19
5.1.3 Identifying a [[settlement]] Account 19
5.1.4 DVP/RVP [[settlement]] 20
5.1.5 Reason Codes 20
5.1.6 [[DTC]] Reject 21
5.1.7 SAS Drop Message 21
5.2 Pre-established Bilaterally Settled SFTs 21
5.3 Other Actions on an Active [[SFT]] Transaction 21
5.3.1 Roll 21
5.3.2 Send-to-Settle Messages 24
5.3.3 Cancel 24
5.3.4 Terminate 24
5.3.5 Rate Modification 25
5.3.6 Recall 26
5.3.7 Buy-in Process 30
5.3.8 Buy-in Execution Applied to an Outstanding [[SFT]] Position 31
5.3.9 Cancel Recall 32
5.3.10 Cancel Buy-in Execution 32
5.4 Calculating the [[settlement]] Value of an [[SFT]] 33
5.5 Calculating and Processing Rate Payments 34

---

## Page 4

5.6 Corporate Actions Processing 35
5.7 Miscellaneous Activity Journal Entries for [[SFT]] Processing 38
5.8 Additional Reference IDs on [[SFT]] Submission to UTC 46
5.8.1 Execution [[ID]] Field (Tag 66) and its use in Cancel Messages 46
5.8.2 Buy Client Order [[ID]] (Tag 11) and Sell Client Order [[ID]] (Tag 11) 47
5.9 [[Broker]] Reorg 48
5.10 [[SFT]] Tax Implications on Participating Entities 48
5.11 Sponsoring and Sponsored [[Member]] Process 48
5.12 End of Day Activity Files 49
5.12.1 [[EOD]] [[mark-to-market]] MRO 49
5.12.2 Outstanding Loans at [[EOD]] 49
5.13 Closures 49
5.13.1 Bank holiday 49
5.13.2 Good Friday 49
5.13.3 Unexpected Close 49
5.14 [[settlement]] Reason Codes 50
5.15 [[SFT]] Money [[settlement]] Codes on the [[NSCC]] [[participant]] Account Statement 50
5.15.1 FFS Money [[settlement]] Code 130 – [[SFT]] Rebate Interest (Rate) on the [[NSCC]] [[participant]] 
Account Statement 50
5.15.2 FFS Money [[settlement]] Code 131 – [[SFT]] [[EOD]] [[mark-to-market]] on the [[NSCC]] [[participant]] 
Account Statement 50
5.15.3 FFS Money [[settlement]] Code 132 – Buy-In Exit & Reorg on the [[NSCC]] [[participant]] Account 
Statement 51
5.15.4 FFS Money [[settlement]] Code 133 – Cash Dividends on the [[NSCC]] [[participant]] Account 
Statement 51
6. MESSAGING FLOWS 52
6.1 New [[SFT]]/On-leg Made 52
6.2 New [[SFT]]/On-leg Dropped 54
6.2.1 Scenario 1 54
6.2.2 Scenario 2 55
6.3 New [[SFT]]/On-leg Canceled 57
6.3.1 Scenario 1 57
6.3.2 Scenario 2 59
6.4 Pre-established Bilateral [[SFT]]/On-leg Made 60
6.5 Roll/On-leg Made 61
6.6 Roll/On-leg Dropped 63
6.7 Roll/On-leg Canceled and Original Off-leg Made 65
6.8 Roll/On-leg Canceled and Original Off-leg Return Dropped 67
6.9 No Roll/Original Off-leg Return Made 69
6.10 No Roll/Original Off-leg Return Dropped 70
6.11 Partial Roll/On-leg Made and Remainder Off-leg Made 72
6.12 Partial Roll/On-leg Made and Remainder Off-leg Dropped 74
6.13 Partial Roll/On-leg Dropped and Remainder Off-leg Made 76
6.14 Partial Roll/On-leg Dropped and Remainder Off-leg Dropped 78
6.15 No Roll on Term Date/Send-to-Settle Received and Original Off-leg Return Made 80
6.16 No Roll on Term Date/Send-to-Settle Received and Original Off-leg Return Dropped 82
6.17 Send-to-Settle (Accelerated Return From the Next Business Day to Current Business Day)/Off-
leg Return Made 83

---

## Page 5

6.18 Send-to-Settle (Accelerated Return From the Next Business Day to Current Business Day)/Off-
leg Return Dropped 85
6.19 Rate Modification 87
6.20 [[SFT]] Loan Termination 89
6.21 [[NSCC]] Exit 91
6.22 Reject/Cancel of a New Loan On-leg Message 92
6.23 Reject/Cancel of a Roll Message 94
6.24 Cancel a [[DO]] Off-leg Return From the Previously Submitted Send-to-Settle (Accelerated) 96
6.25 Reject of a Cancel of [[DO]] Off-leg Return From the Previously Submitted Send-to-Settle 
(Accelerated) 98
6.26 [[NSCC]] Initiated Price Differential 100
6.27 Corporate Actions 102
6.27.1 Forward [[Stock]] Split 102
6.27.2 Reverse [[Stock]] Split 104
6.27.3 Cash Merger 106
6.27.4 [[Stock]] Merger 107
6.27.5 Cash & [[Stock]] Merger 109
6.27.6 Name Change 111
6.28 [[Broker]] Reorg 113
A. MESSAGE LAYOUTS 114
A.1 Messaging and File Types 114
A.2 UTC Message Types 115
A.3 UTC Input and Output Formats 119
UTC Input FIX/MQ Format 120
UTC Input [[EOD]] Totals FIX/MQ Format 130
UTC Output FIX/MQ Format 131
UTC Outbound Gap Fill Request FIX/MQ Format 144
UTC Outbound [[EOD]] Confirmation to Market FIX/MQ Format 146
UTC Outbound Buy-Side Cutoff FIX/MQ Format (3:00 P.M. ET) 148
UTC Outbound [[EOD]] Messages to Participants by Market 149
UTC Reject Codes 151
A.4 SAS ISO Message Output 154
A.5 [[DTC]] Input and Output Messages 159
A.6 MT548 Message Format 161
A.7 MT547/MT545 (Inclusive of Rate Modification) Message Format 167
A.8 MT542: Recall and Buy-In Input Message Formats 173
A.9 Recall and Buy-In Execution Output Message Formats 178
B. FILE AND REPORT LAYOUTS 183
B.1 Outstanding Loan MRO AutoRoute [[ID]]: Production 02043624 / PSE 02983624 183
Header Record 183
Loan Detail Record 184
Recall Detail Record 187
B.2 End of Day ([[EOD]]) [[mark-to-market]] MRO AutoRoute [[ID]]: Production 02043623 / PSE 02983623188
Header Record 188
Detail Record 188
B.3 Eligible Security  MRO: AutoRoute [[ID]] Production 02043626 / PSE 02983626 190
B.4 Record Date Print Image: AutoRoute [[ID]] Production 02042959 / PSE 02982959 190

---

## Page 6

B.5 [[Dividend]] Activity MRO: AutoRoute [[ID]] Production 02043700 / PSE 02983700 191
Header Record 191
Detail Record 191
Trailer Record 193
B.6 [[Dividend]] With Due Bill Activity MRO: AutoRoute [[ID]] Production 02043701 / PSE 02983701 194
Header Record 194
Detail Record 195
Trailer Record 197
B.7 Miscellaneous Activity (Extended) MRO: AutoRoute [[ID]] Production 02040343 / PSE 02980343 
(Night) and Production 02040331 / PSE 02980331 (Day) 197
Header Record 197
Detail Record 199
Sub-Total Detail Record 203
Trailer Record 205
C. TIME FRAMES 206

---

## Page 7

1. About This Guide 7
1. ABOUT THIS GUIDE
This general user guide is not legally binding and is only for information purposes.  It is designed to provide you with a 
detailed understanding of the roles and responsibilities of the various parties and Approved [[SFT]] Submitters involved 
in the clearance and [[settlement]] of an [[SFT]]. It contains the [[securities]] Financing Transaction ([[SFT]]) Clearing service 
operational flow, including management of life cycle events, and messaging inputs and outputs necessary to support 
[[SFT]] Clearing activity, including related message and file layouts.
For ease of reference, the terms [[SFT]] and loan are used interchangeably in this document.
Important Note
l This document should not be regarded as a substitute for the [[NSCC]] rules and procedures.  In all cases, Members
should refer to the [[NSCC]] rules and procedures for a complete statement of [[NSCC]]’s rules, procedures, [[obligations]],
and requirements.  Nothing in this document shall be deemed to impose any [[obligations]] on [[NSCC]] that are not set
forth in the [[NSCC]] rules and procedures, and in the case of any discrepancy between this document and the [[NSCC]]
rules and procedures, the [[NSCC]] rules and procedures shall govern. The [[NSCC]] Rules and Procedures are
available at http://www.[[DTCC]].com/legal/rules-and-prodcedures.aspx.
l This document is still in draft form and is subject to further review and changes by [[DTCC]].
1.1 Contact Us
Use the following [[NSCC]] contacts for information about the [[SFT]] Clearing service. You can also contact your [[DTCC]] 
Relationship Manager or obtain general assistance by visiting the [[DTCC]] Client Center.
For... Contact...
General questions and product 
support
Email [[NSCC]] Support at NSCCSupport@[[DTCC]].com.
Setup and testing Email [[NSCC]] Integration at NSCCIntegration@[[DTCC]].com.
Issues with logging on to the 
system
Contact [[DTCC]] Client Support. Call the following number, and then follow the prompt for 
product support.
 o For US and Canada, call 1 888–382–2721.
 o For the UK, Europe, and Asia, call +1 212–855–8099.
[[SFT]] Clearing: General User Guide

---

## Page 8

1. About This Guide 8
1.2 Extension Guidelines
If an extension is needed for any input submission, firms should use one of the following methods to obtain support:
l Email [[NSCC]] Support at NSCCSupport@[[DTCC]].com.
l Telephone [[DTCC]] Client Support at 1-888-382-2721 and follow the prompt for production support.
If [[DTCC]], at its sole discretion, extends a deadline that would significantly impact reporting times, a communication is 
sent out.
[[SFT]] Clearing: General User Guide

---

## Page 9

2. About the [[SFT]] Clearing Service 9
2. ABOUT THE [[SFT]] CLEARING SERVICE
National [[securities]] Clearing Corporation ([[NSCC]]) plans to provide a  central clearing service for overnight borrowing, 
lending, and REPO transactions, collectively, [[securities]] Financing Transaction ([[SFT]]) Clearing, for its full service 
members and institutional clients who are sponsored into [[NSCC]] by Sponsoring Members. The decision to provide the 
[[DTCC]] [[SFT]] Clearing service was based on:
l Informed discussions with various market participants.
l Gathering experiences and knowledge of other Central Counterparties (CCPs) in the space.
l Leveraging [[FICC]]'s recent experiences expanding its suite of institutional client fixed income repo clearing services
l Consulting with accounting and regulatory experts.
Consistent with the manner in which [[NSCC]] accepts cash market transactions, the [[SFT]] Clearing service would be 
required to be submitted to [[NSCC]] on a locked-in/matched basis by an approved [[SFT]] submitter.  [[securities]] eligible to 
be the subject of an [[SFT]] are certain [[NSCC]] [[CNS]]® eligible [[Equity]] [[securities]] and cash. 
2.1 Key Design Elements of the [[SFT]] Clearing Service
The [[SFT]] Clearing service enables  access to the following key design elements:
l Ability to settle DVP/RVP at [[DTC]].  [[SFT]] Deliver Orders are processed in accordance with the Depository Trust
Company ([[DTC]]) rules and procedures, including provisions relating to risk controls.
l Settlements would be allowed to [[pair off]] daily against new activity to minimize the operational burden of settling
overnight [[obligations]].  [[NSCC]] would calculate and process price differences/[[mark-to-market]] that are created by the
daily [[pair off]].
l Upon the initial [[settlement]] of the [[SFT]], its final [[settlement]] would novate to [[NSCC]].
l [[SFT]] activity would be risk managed by [[NSCC]] in a manner consistent with Members’ cash [[CNS]] positions, but  would
be separately margined. A separate Clearing Fund deposit would also be collected by [[NSCC]] for the [[Member]]'s [[SFT]]
activity.
l SFTs remain in the system, as long as they are rolled forward by the Approved [[SFT]] Submitter.
l [[SFT]]-eligible security universe would extend to the majority of [[CNS]]-eligible equities [[securities]].
[[NSCC]] would impose a $5 per share price minimum on [[SFT]]-eligible [[securities]] such that 100% [[Margin]] would be
charged for novated [[SFT]] transactions in which the per share price of the underlying [[Equity]] security falls below $5.
l [[NSCC]] would process certain mandatory corporate actions and cash dividends for novated [[SFT]] transactions.
[[SFT]] Clearing: General User Guide

---

## Page 10

2. About the [[SFT]] Clearing Service 10
2.2 Sponsorship at [[NSCC]]
Agent lender banks and prime brokers actively transact [[Equity]] [[SFT]] transactions on behalf of their institutional clients. 
Several of these firms are already established clients of [[NSCC]]’s clearing services. A growing number of firms are 
developing businesses to clear institutional client [[SFT]] activity as part of [[FICC]]’s Sponsoring [[Member]]/Sponsored 
[[Member]] Service.
The [[NSCC]] sponsorship model is designed to allow agent lender banks and prime brokers to play the role of credit 
intermediaries for their institutional clients in clearing in a capital efficient manner.  All full service [[NSCC]] members are 
eligible to apply to become Sponsoring Members or Agent Clearing Members in [[NSCC]], subject to comparable credit 
criteria as are applicable to Sponsoring Members in [[FICC]]’s Sponsoring [[Member]]/Sponsored [[Member]] Service.  
l A Sponsoring [[Member]] would be permitted to facilitate its institutional clients’ cleared [[SFT]] activity through two back-
to-back principal transactions, such as Client-to-Sponsoring [[Member]] and Sponsoring [[Member]]-to-[[Broker]] or to
another institutional client.
l An Agent Clearing [[Member]] would be permitted to facilitate a transaction directly between its institutional clients and
another full service [[NSCC]] [[Member]] through an Agent Clearing [[Member]] Customer Omnibus Account structure.
[[SFT]] Clearing: General User Guide

---

## Page 11

3. [[SFT]] Clearing Service Roles and Responsibilities 11
3. [[SFT]] CLEARING SERVICE ROLES AND
RESPONSIBILITIES
Processing an [[SFT]] through central clearing involves a number of parties. The following table outlines the roles and 
responsibilities of each of the involved parties:
Role Description
3.1 
Approved 
[[SFT]] 
Submitter
Submits a matched [[SFT]] to [[NSCC]] on a locked-in basis. May be an [[NSCC]] [[Member]] or a third-party 
vendor.  All data submitted into the [[SFT]] Clearing service must come through an Approved [[SFT]] Submitter 
who has been authorized to submit SFTs to [[NSCC]] on behalf of one or more [[NSCC]] members.
Prior to submitting an [[SFT]] to [[NSCC]], the Approved [[SFT]] Submitter is expected to:
l Perform matching functions.
l Determine eligibility for central clearing services.
l Submit the data to [[NSCC]] in near real-time and support subsequent actions on novated SFTs.
All Approved [[SFT]] Submitters, regardless of whether or not they are an [[NSCC]] [[Member]], are expected to
adhere to specific participation requirements, such as proven operational capabilities and other
requirements as outlined in the [[NSCC]] Rules & Procedures and the Approved [[SFT]] Submitter Agreement.
3.2 [[NSCC]] 
Full-Service 
[[Member]]
Any [[NSCC]] full-service [[Member]] that files a W-9 with the IRS can apply to participate in the [[SFT]] Clearing 
service. As described above, participation requires opening a separate [[SFT]] Clearing account at [[NSCC]] 
that will be eligible only for the clearance of [[SFT]] activities. The [[SFT]] Clearing account must be linked to a 
[[DTC]] settling account.
3.3 
Sponsoring 
[[Member]]
An [[NSCC]] full-service [[Member]] permitted to novate to [[NSCC]] its principal SFTs with its Sponsored 
Members. The Sponsoring [[Member]] is responsible to [[NSCC]] for:
l Posting all Clearing Funds associated with the [[SFT]] activity of its Sponsored Members.
l Providing a backup guaranty to [[NSCC]] for its Sponsored Members’ [[settlement]] [[obligations]]. This means
that in the event that one or more of its Sponsored Members [[default]] and [[DO]] not satisfy their [[settlement]]
[[obligations]] to [[NSCC]], the Sponsoring [[Member]] is required to satisfy those [[obligations]].
l Responsible for any [[default]] loss allocated to its Sponsored Members and its own loss allocation as an
[[NSCC]] full-service [[Member]].
3.4 
Sponsored 
[[Member]]
Eligible institutional client of a Sponsoring [[Member]]. A Sponsored [[Member]] is permitted to engage in two-
directional [[SFT]] activities, meaning it can borrow or lend [[securities]] through a linked account of its 
Sponsoring [[Member]] on the books of [[NSCC]]. 
                 [[SFT]] Clearing Service Roles and Responsibilities
[[SFT]] Clearing: General User Guide

---

## Page 12

3. [[SFT]] Clearing Service Roles and Responsibilities 12
Role Description
3.5 Agent 
Clearing 
[[Member]]
An [[NSCC]] full-service [[Member]] permitted to novate to [[NSCC]] SFTs that it has executed as agent on behalf 
of its customers with a third-party [[NSCC]] [[Member]]. The Agent Clearing [[Member]] is responsible to [[NSCC]] 
for:
l Posting all Clearing Funds associated with the activity of its customers.
l Covering any [[default]] loss allocatable to its customers, as well as its own [[default]] loss allocation as an
[[NSCC]] full-service [[Member]].
However, unlike a Sponsoring [[Member]], an Agent Clearing [[Member]] is not required to provide a backup 
guaranty to [[NSCC]] for its customers’ [[obligations]].  This is because the Agent Clearing [[Member]] is liable as 
a principal on all activities the Agent Clearing [[Member]] submits to [[NSCC]] on behalf of its customers.
3.6 Agent 
Client
An institutional client of an Agent Clearing [[Member]] that is eligible to participate in lending-only or 
borrowing-only activity through an omnibus account of its Agent Clearing [[Member]] on the books of [[NSCC]] 
(Agent Clearing [[Member]] Customer Omnibus Account).  Agent Clients are not members of [[NSCC]], and 
[[NSCC]] shall not have any liability or obligation to any Agent Client.
[[SFT]] Clearing Service Roles and Responsibilities (Continued)
[[SFT]] Clearing: General User Guide

---

## Page 13

3. [[SFT]] Clearing Service Roles and Responsibilities 13
3.7 Separation of Accounts 
All [[SFT]] activity, including all proprietary activity and institutional client activity, is cleared through an account 
designated for only [[SFT]] activity. You cannot use this account to clear and settle cash market activity, such as [[CNS]] 
activity.  For example, if an [[NSCC]] cash market clearing account is #123, the activity for the [[SFT]] account must be 
booked into a different account, such as #124, that only supports [[SFT]] activity.  Moreover, Agent Clearing [[Member]] 
Customer Omnibus Account activity would need to be conducted in an account separate from any Sponsored [[Member]] 
activity.  In addition, as described in the table in [[SFT]] Clearing Service Roles and Responsibilities, Agent Clearing 
[[Member]] Customer Omnibus Accounts may contain lending-only or borrowing-only client activities to ensure the gross 
margining of the [[SFT]] activity.  To summarize, if an [[SFT]] [[participant]] is engaged in proprietary and institutional client [[SFT]] 
activity, it may have as many as the following four different types of [[SFT]] Clearing accounts: 
l Proprietary Account for Principal Activity
l Sponsored [[Member]] accounts for individual Sponsored Members
l Agent Clearing [[Member]] Customer Omnibus Lending Account
l Agent Clearing [[Member]] Customer Omnibus Borrowing Account
[[SFT]] Clearing: General User Guide

---

## Page 14

4. General System Flow 14
4. GENERAL SYSTEM FLOW
Where possible, the [[SFT]] Clearing service leverages [[NSCC]]’s and [[DTC]]’s existing systems and makes modifications, 
where needed, to support the [[SFT]] business. This section provides a general flow of activity through the service.  This 
document also contains specific details for each of the components.
Note
All times listed in this guide are shown in Eastern Time.
[[NSCC]]’s trade capture application is its Universal Trade Capture (UTC) system. UTC accepts trades in near real-time 
from approved submitting entities. UTC is designed to capture the large volumes associated with cash market trading 
activity and receives in activity from over 50 trading venues. UTC will be modified and extended to receive and validate 
activity for the [[SFT]] Clearing service. It processes activity using a standard FIX format input message, submitted 
through MQ or FIX engine. UTC’s primary role in clearing is to capture and validate activity. Validations are done in 
near real-time. UTC then hands off the activity to multiple other systems involved in the clearing life cycle, namely the 
risk systems and the [[NSCC]] accounting systems ([[CNS]] for cash trades and [[securities]] Financing Accounting System 
(SAS) for [[SFT]] trades). 
SAS is responsible for maintaining the [[settlement]] status of an [[SFT]] and acts as a hub between UTC and [[DTC]]. It 
determines what to send to [[DTC]] for [[settlement]] and when to send it.  It also updates [[NSCC]]’s risk systems of [[settlement]] 
events to make sure the most current status of an obligation is provided to the risk systems for risk management. For 
the SAS process only, [[NSCC]] will have a new central counterparty clearing account at [[DTC]], which is the 881 account. 
SAS passes SFTs to [[DTC]] for [[settlement]] through the [[NSCC]] [[SFT]] account (881) at [[DTC]] Global. SFTs are settled on a 
receive-versus-payment (RVP) and deliver-versus-payment (DVP) basis. As such, all SFTs are subject to [[DTC]] 
controls and [[DTC]] rules and procedures.  [[NSCC]]’s account at [[DTC]] acts as a pass-through account and does not hold 
[[securities]] or money. To make sure that this condition is met, [[DTC]] employs the Look Ahead function  to ensure the 
[[Borrower]]’s and lender’s [[collateral]] controls support [[settlement]] of the transaction. If they cannot support [[settlement]] of 
the transaction, the transaction does not complete, meaning that [[securities]] and associated credits of cash will not 
move. 
UTC, SAS, and [[DTC]] are all part of a single workflow that manages the clearance and [[settlement]] of SFTs. [[NSCC]] 
provides message and file outputs to users of the system that offer information on the status of the [[SFT]] within our 
environment. [[SFT]] information is also available on a web enabled tool that users can access through [[NSCC]]’s Clearing 
Dashboard. In addition, [[DTC]] will also provide [[settlement]] status messages to clients who have a subscription set-up 
with [[DTC]] to receive this output.
[[NSCC]]’s risk systems are responsible for ensuring that the trading ecosystem as a whole is protected and that activity 
in the ecosystem is appropriately risk managed. At a high level, the risk systems assess each transaction in a portfolio 
against market moves, review the portfolio as a whole against predicted market moves and observe and react to 
changes in the portfolio outside the norm. [[NSCC]] processes a standard risk requirement once a day, made available to 
Members at approximately 7 A.M. ET with debits due for collection prior to 10 A.M. ET. The risk systems receive up-to-
date information on the status of street-side SFTs from UTC and SAS and the risk calculations are refreshed every 15 
minutes throughout the day. [[SFT]] activity is managed separately from cash activity with no offsets given between the 
two portfolios. Additionally, Sponsored [[Member]] sub-accounts and Agent Clearing [[Member]] Customer Omnibus 
Accounts are each managed on a gross basis, meaning that no offset is given between such accounts. 
[[SFT]] Clearing: General User Guide

---

## Page 15

4. General System Flow 15
The following figure represents a typical message flow between the [[DTCC]] systems  to process a new [[SFT]].  These 
systems are UTC (for accepting a new trade), SAS (for maintaining the [[SFT]]  status), and [[DTC]] (for moving positions 
between two counterparties).  For more information about specific-situation message flows, see Message Layouts.
[[SFT]] Clearing: General User Guide

---

## Page 16

5. General Operational Flow 16
5. GENERAL OPERATIONAL FLOW
To process [[SFT]] activity through a centrally cleared model, several life cycle event types need to be supported. 
Broadly, an [[SFT]] is made up of the following main [[settlement]] events:
l Initial movement of [[securities]] versus cash from the lender to the [[Borrower]]. This is referred to as on-leg throughout
this document.
l Return of the [[securities]] versus cash from the [[Borrower]] to the lender. This is referred to as off-leg throughout this
document.
l Price Differential, which is a payment order that results in a movement of cash among [[NSCC]], the lender, and the
[[Borrower]]. Typically, it is done as part of a daily roll by counterparties to the [[SFT]]. In some instances, however, it may
also be an [[NSCC]] Initiated Price Differential that is processed on specific off-leg returns, such as those where a
recall has been submitted against the [[DTCC]] Reference [[ID]] or where [[NSCC]] is processing a corporate action against
the [[DTCC]] Reference [[ID]].
Members and Approved Trade Submitters should keep in mind that during the life of an [[SFT]] transaction, they will 
interact with different [[NSCC]] systems.  The following naming conventions are used to differentiate various message 
product numbers:
1 UTCI [[SFT]] INPUT of new SFTs into the UTC system.
2 SFTO [[SFT]] OUTPUT from the UTC system.
3 CNSESFTO [[SFT]] SAS updates and MADE messages. 
This set of messages is depicted in the scenarios below.
4 CNSISOI [[SFT]] Recall and Buy-in ISO Input.
5 CNSISOO [[SFT]] Recall and Buy-in ISO Output.
The role of the [[SFT]] account number remains the same throughout the transaction. For example, if 1103 is the original 
lender and 1185 is the original [[Borrower]], they remain the Lender or [[Borrower]] on the transaction; however, the 
processing side changes. If the Lender is the deliverer for the on-leg transaction, they are the receiver for the off-leg 
transaction.
5.1 Processing a New [[SFT]] On-leg
The first step in centrally clearing an [[SFT]] activity is for [[NSCC]] to receive and validate a transaction into the [[SFT]] 
Clearing service. As part of this first step, [[NSCC]] reviews each field in the input record for conformity to the system 
requirements, any other criteria that are specified by [[NSCC]], or both. For the general format edits, see A.1, Messaging 
and File Types.  Some key business edits that are applied to a received [[SFT]] activity are outlined in 5.1.1, Key Business 
Validations for On-leg Transactions. 
For street-side activity, [[NSCC]]’s UTC system is available for new [[SFT]] on-leg input from its open at approximately 4:30 
A.M. Eastern Time through to close of [[settlement]] at approximately 3:00 P.M. Eastern Time.  After that time, it rejects
the activity until the system reopens the next business day.
[[SFT]] Clearing: General User Guide

---

## Page 17

5. General Operational Flow 17
5.1.1 Key Business Validations for On-leg Transactions
The following table shows the key business validations for on-leg transactions:
Business 
Validation
Description
Approved [[SFT]] 
Submitter
[[NSCC]] supports receipt of locked-in transactions through its UTC system. This means that an 
Approved [[SFT]] Submitter names the [[Borrower]] and lender to the transaction, and those 
counterparties who agreed to the trade terms through a matching facility offered by the Approved 
[[SFT]] Submitter. [[NSCC]] maintains relationship tables between the Approved [[SFT]] Submitters and 
counterparties to the [[SFT]] transactions. [[NSCC]] performs the following checks on all [[SFT]] activities: 
l Validates that the Approved [[SFT]] Submitter is eligible to submit [[SFT]] activity.
l Validates that the counterparties named on the trade are eligible to participate in [[SFT]] activity.
l Validates that the Approved [[SFT]] Submitter is eligible to submit on behalf of the counterparties to
the [[SFT]] activity.
If any condition is not met, [[NSCC]] rejects the submission and notifies the Approved [[SFT]] Submitter. 
Security [[ID]] [[NSCC]] validates that a security is eligible for the [[SFT]] Clearing service. Generally, all [[securities]], 
excluding rights, [[Warrants]], and unit investment trusts (UITs), are eligible for new [[SFT]] activity, if the 
following criteria are met:
l [[CNS]]-eligible
l [[DTC]] [[book-entry]] eligible for deliver order processing
l Contain an end-of-day closing price that equals or is greater than USD $5.00.
If a security’s end-of-day price has dropped below USD $5.00, it is ineligible for on-leg [[SFT]]
submission, but may still be eligible for the Roll process with an additional risk charge applied to the
position.
[[securities]] may fall in/out of [[SFT]] eligibility.  These could be due to circumstances outside of [[NSCC]]’s
control. For example, if a security is undergoing a corporate action that [[NSCC]] cannot support, [[NSCC]]
may mark it as [[SFT]] Ineligible. It could also result from an [[NSCC]] decision to make a particular
security no longer [[CNS]]-eligible,  such as trade-for-trades.  For more information about such an event,
see 5.6, Corporate Actions Processing.
Additionally, the [[SFT]] Clearing service is currently offered only for equities [[securities]]. Any [[SFT]]
activity in a [[CNS]] eligible corporate [[Bonds]], municipal [[Bonds]], or unit investment trusts will be rejected.
Trade Date Implied [[settlement]] date of the [[SFT]] activity  calculated off the trade date. To realize the capital 
benefits of this service, all [[SFT]] transactions in this service must be executed as term trades. [[NSCC]] 
is offering the [[SFT]] Clearing service for overnight term [[SFT]] transaction. This means that the 
[[settlement]] date of the off-leg of the [[SFT]] will be the Trade Date plus one business day. For example, 
if the trade date submitted is Wednesday, January 2, 2019, the [[settlement]] date on the off-leg is 
calculated as Thursday, January 3, 2019. If the trade date submitted is Friday, February 22, 2019, 
the [[settlement]] date of the off-leg is calculated as Monday, February 25, 2019.
[[SFT]] Clearing: General User Guide

---

## Page 18

5. General Operational Flow 18
Business 
Validation
Description
Reference IDs [[NSCC]] supports including several reference IDs to help identify [[SFT]] activity. In most cases, the 
reference [[ID]] is only for information purposes. However, one critical reference [[ID]] is the [[DTCC]] 
Reference [[ID]], which is a 14-byte [[ID]] applied to each transaction processed in the UTC system. This 
[[ID]] is required whenever a counterparty wants to take an action on an [[SFT]]. For example, initial on-leg 
deliver order at [[DTC]], roll, recall, buy-in execution, or cancel. 
Note: Other reference IDs can also be included on an [[SFT]], allowing the lender, [[Borrower]], and 
Approved [[SFT]] Submitter to include their transaction IDs to support reconciliation.  [[NSCC]] will not [[DO]] 
any processing on these other reference IDs, but instead will just carry them and pass them through 
on the output. 
Independent 
Amount (IA)
Due to certain laws and conventions in the marketplace, [[NSCC]] supports over collateralizing an [[SFT]]. 
As part of the input, Approved [[SFT]] Submitters provide [[NSCC]] the rate of the independent amount 
(IA).  [[NSCC]] uses this rate to calculate the IA amount and [[settlement]] value on the trade. For Roll 
transactions, the IA  rate must match the referenced [[SFT]] IA rate.
The IA is settled as part of [[settlement]] value of the trade, credited intraday to the lender account, and 
settled as part of end of day [[settlement]]. 
Rounding 
Rules
The [[SFT]] market assumes rounding rules as part of the [[settlement]] value. [[NSCC]] accommodates the 
rounding of the [[settlement]] price in increments of 1 cent, five cents, 10 cents, 25 cents, and dollar. 
Otherwise, if applicable, it can be submitted with no rounding flagged. 
[[NSCC]] always round up; it never rounds down. For example, if an Approved [[SFT]] Submitter indicated 
that rounding should be to the nearest $0.25 and an original price of $9.09, [[NSCC]] rounds the 
[[settlement]] price to $9.25.  For more information about rounding, see 5.4, Calculating the [[settlement]] 
Value of an [[SFT]] .
Market Price If the price is excluded from an input transaction to the UTC system or [[securities]] Financing 
Accounting System (SAS) has to process a [[mark-to-market]] for an [[SFT]] (such as in the case of a non-
returned [[SFT]]), [[NSCC]] always uses the prior day’s closing price from its risk system that is six digits to 
the right of the decimal as the price.
On-Leg 
[[settlement]]
Only activity between two [[NSCC]] Full Service Members will be sent for [[settlement]] at [[DTC]]. This can 
be: 
l A Sponsoring [[Member]] or Agent Clearing [[Member]] versus a [[Broker]]’s proprietary account.
l A Sponsoring [[Member]] or Agent Clearing [[Member]] versus another Sponsoring [[Member]] or Agent
Clearing [[Member]].
l Two brokers.
Any validated submissions between a Sponsoring [[Member]] and its Sponsored [[Member]] does not 
require [[settlement]] at [[DTC]] (as it is an accounting movement on the Sponsoring [[Member]]’s books) and 
the off-leg will be novated to [[NSCC]] after the off-leg return message is sent to the Sponsoring 
[[Member]], which will be at approximately 3:00 P.M. ET daily.    For more information, see 5.11, 
Sponsoring and Sponsored [[Member]] Process. 
[[SFT]] Clearing: General User Guide

---

## Page 19

5. General Operational Flow 19
5.1.2 Post-Validation Processing
After passing UTC’s edits and validations, [[NSCC]] responds in real-time to parties subscribed to real-time UTC output. 
This can include the [[Borrower]] and the lender to the [[SFT]], the Approved [[SFT]] Submitter, and any other service bureau 
destinations that may need to receive a copy of the receipt (as defined by the [[Borrower]] or lender). The output message 
is enriched with certain data (see A.4, SAS ISO Message Output), most notably the [[DTCC]] Reference [[ID]], which is the 
key identifier on the [[SFT]] from this point onwards, and the calculated [[settlement]] value of the [[SFT]] (see 5.4, Calculating 
the [[settlement]] Value of an [[SFT]] ). 
After passing UTC's edit and validation, the on-leg is set up for [[settlement]] at [[DTC]].  The [[SFT]] activity is housed in 
[[NSCC]]’s SAS system in anticipation of [[settlement]] and SAS interacts with [[DTC]] to get real-time updates of the 
[[settlement]] status. 
For availability and cut-off times for all actions described in this section, see C, Time Frames.
5.1.3 Identifying a [[settlement]] Account
To support [[settlement]] of the activity, each [[NSCC]] Full Service [[Member]] is required to identify a [[settlement]] account 
associated with its [[SFT]] activity. The following two options will be supported:
1. Members can settle [[SFT]] activity using its primary [[DTC]] account number, which is its Main Account (or Legal Entity
Account) only.  The [[Member]] cannot use another subaccount under their Main Account to settle [[SFT]] activity.  In this
case, any [[SFT]] activity of a [[Member]] would be commingled with the [[Member]]’s [[DTC]] activity for [[settlement]] purposes.
2. Members can settle [[SFT]] activity using a [[DTC]] account number specific for the [[SFT]].
l The lender can move (or hold) inventory into that account for use for only [[SFT]] activity.
l This account would be subject to its own [[DTC]] risk controls.
l End of day cash [[settlement]] would be rolled up into one single credit or debit at the legal entity level (for
example, one [[settlement]] credit/debit across all the [[Member]] accounts).
It is up to the [[Member]] to define the set up during their onboarding process.
[[SFT]] Clearing: General User Guide

---

## Page 20

5. General Operational Flow 20
5.1.4 DVP/RVP [[settlement]]
[[DTCC]] supports lenders’ ability to determine when [[securities]] should leave [[DTC]] accounts to be delivered to a [[Borrower]]. 
Through this process, lenders push [[securities]] to [[NSCC]] to kick-off the [[settlement]] of the on-leg of a new [[SFT]]. However, 
prior to kicking off [[settlement]], [[NSCC]] must first receive and validate the on-leg as described in the 5.1.1, Key Business 
Validations for On-leg Transactions.  
The output of that validation to the lender/[[Borrower]]/Approved [[SFT]] Submitter will contain the [[DTCC]] Reference [[ID]].  The 
lender must process and include this reference [[ID]] on any deliver orders that are pushed to the [[NSCC]] [[SFT]] account 
(881).  Therefore, this is a field that must be consumed by the lender. After they have the [[DTCC]] Reference [[ID]], the 
lender instructs [[DTC]] to deliver [[securities]] from its [[DTC]] account to the [[NSCC]] [[SFT]] account (881)  versus the [[settlement]] 
value provided on the output from UTC.  The lender must use [[DTC]] [[settlement]] Reason Code 200, and the comments 
field on the deliver order must include the [[DTCC]] Reference [[ID]] that was passed on to the UTC output with a leader of 
[[SFT]] followed by the [[DTCC]] Reference [[ID]]. 
[[DTC]] validates that SAS knows the [[DTCC]] Reference [[ID]], [[CUSIP]], [[settlement]] amount, and share value.  Upon 
confirmation, [[DTC]] accepts that transaction, and the SAS system sends to [[DTC]] the deliver order instruction to deliver 
from the 881 account to the [[Borrower]] for the same [[shares]], [[settlement]], reason code, and [[DTCC]] Reference [[ID]]. 
From there, [[DTC]] continues with its normal processing. For example, [[DTC]] confirms that the [[Borrower]]’s [[collateral]] 
controls can support the receive and, if it can, it credits the [[Borrower]] the [[shares]] and credits the lender the [[settlement]] 
value (and simultaneously debit the [[Borrower]] the [[settlement]] value and debit the lender the [[shares]]).  If the [[Borrower]]’s 
[[collateral]] controls cannot support receiving the [[shares]], [[DTC]] Pends the item, and the item recycles throughout the day. 
[[DTC]] also performs a [[collateral]] check on the lender’s account to ensure that there is satisfactory [[collateral]] to allow the 
transaction to be processed. If not, [[DTC]] will Pend the item and the item recycles throughout the day.  For more 
information about this [[DTC]] [[settlement]] process, see the [[DTC]] [[settlement]] Service Guide. You can also view the 
[[settlement]] section available in the [[DTCC]] Learning Center at https://dtcclearning.com/products-and-
services/[[settlement]].html.  
[[DTC]] must ensure that it is 100% collateralized to support [[settlement]] of the [[SFT]] obligation.  This means that [[DTC]] looks 
through the [[NSCC]] [[SFT]] account (881) through its Look Ahead. It only moves [[securities]] if the [[Borrower]] and the lender 
are sufficiently collateralized to support the on-leg [[settlement]] movement.  If the [[Borrower]] and lender are not sufficiently 
collateralized to support on-leg [[settlement]], no movement of the [[securities]] occurs. The [[SFT]] activity continues to be 
recycled until either sufficient [[collateral]] is available or until the [[EOD]] Drops process at [[DTC]] completes.  
Note
The on-leg of an [[SFT]] must settle in whole. No partial settlements are allowed.
Movement of [[shares]]/credit of [[settlement]] value also notifies SAS to set up a pending [[settlement]] off-leg item for next day 
[[settlement]].  Members can use this message as notification that the off-leg of the [[SFT]] is now novated to [[NSCC]].
At this point, [[NSCC]] will also calculate and store the rate amount associated with the [[SFT]], which will be novated to 
[[NSCC]] and will settle the following business day as part of end of day [[NSCC]] cash [[settlement]].
5.1.5 Reason Codes
[[SFT]] activity is identified through the use of specific reason codes at [[DTC]]. For more information, see 5.14, [[settlement]] 
Reason Codes.
[[SFT]] Clearing: General User Guide

---

## Page 21

5. General Operational Flow 21
5.1.6 [[DTC]] Reject
As noted in 5.1.4, DVP/RVP [[settlement]],  to push the [[securities]] for [[settlement]], the deliver order ([[DO]]) must include the 
[[DTCC]] Reference [[ID]], [[CUSIP]], and [[shares]] equal to a pending [[settlement]] on-leg in SAS.  If the [[DO]] does not match a 
pending [[settlement]] on-leg in SAS, [[DTC]] immediately rejects the obligation.
5.1.7 SAS Drop Message
At the end of the day, approximately 3:10 P.M. Eastern Time, [[DTC]] notifies clients of deliver orders that have dropped. 
A situation may occur where SAS has a pending [[settlement]] on-leg instruction; however, [[DTC]] never received the [[DO]] 
instruction from the lender. In this case, the end of day message informs firms that [[DTC]] never received the [[DO]] and it is 
dropped from SAS. As with a [[DTC]] drop, [[NSCC]] has no obligation with respect to the [[SFT]] if the on-leg is not processed 
at the end of day.
5.2 Pre-established Bilaterally Settled SFTs
Prior to the introduction of central clearing, the [[SFT]] market participants settled on a bilateral basis with borrowers 
facing lenders directly or through an agent.
Rather than require a lender and [[Borrower]] to unwind an active [[SFT]] just to move it into clearing, [[NSCC]] allows lenders 
and borrowers to submit a pre-established bilaterally settled [[SFT]] to the system.  When [[NSCC]] receives this type of 
message from an Approved [[SFT]] Submitter, it immediately generates an off-leg position that novates to [[NSCC]] (no 
[[shares]] need to move because they are already with the [[Borrower]]).  Members receive acceptance of the submitted on-
leg instruction by UTC and receive the PEND of the off-leg instruction from the SAS system after the SAS system 
receives the on-leg instruction from UTC.
It is important that any memo positions related to a bilaterally settled [[SFT]] (from [[Stock]] Loan [[DO]] reason codes 10s and 
20s) need to be updated or deleted from tracking at [[DTC]] by the two counterparties directly using the SLRM function.
5.3 Other Actions on an Active [[SFT]] Transaction
This section explains the different types of messages in the [[SFT]] Clearing service.
5.3.1 Roll
On the term date of an [[SFT]], [[NSCC]] permits the lender and the [[Borrower]] to agree to keep the [[shares]] out on loan and 
[[pair off]] their [[settlement]] [[obligations]] to each other on the termed [[SFT]] with their on-leg [[settlement]] [[obligations]] to each 
other on a new [[SFT]].  This is accomplished by the Approved [[SFT]] Submitter processing a Roll transaction.
Note
Based on market convention, [[NSCC]] anticipates that most Roll transactions will be submitted by the 
Approved [[SFT]] Submitters early in the morning on a given business day.
[[SFT]] Clearing: General User Guide

---

## Page 22

5. General Operational Flow 22
In connection with a Roll, the Approved [[SFT]] Submitter matches the new [[SFT]] trade between the two original 
counterparties.  It then submits the new on-leg details to [[NSCC]] through a Roll message. However, it also includes the 
[[DTCC]] Reference [[ID]] for the [[SFT]] that has reached term date. [[NSCC]] performs its standard validation process on the 
new [[SFT]] and passes validated activity to SAS for further processing.
In this case, no [[shares]] need to move because the [[shares]] are still with the [[Borrower]]. However, the market price of the 
[[securities]] may have changed, and that difference needs to be credited or debited to the lender. SAS calculates the 
cash difference between the termed [[SFT]] and the new on-leg.  This difference is known as the Price Differential.
Price Differential = Termed [[SFT]] [[settlement]] Value – New [[SFT]] [[settlement]] Value
SAS passes the calculated Price Differential on the [[SFT]] to [[DTC]] for processing through the [[NSCC]] [[SFT]] account (881) 
at [[DTC]] Global.  As with [[settlement]] of [[securities]], [[DTC]] employs its Look-Ahead feature and the Price Differential is 
subject to [[DTC]] risk controls. If [[settlement]] cannot be made because of [[DTC]] risk controls or any other reason, [[DTC]] 
continues to try to make the [[settlement]] throughout the day or until the [[EOD]] [[DTC]] Drops process at [[DTC]] completes.
[[DTC]] provides output to appropriate parties once the Price Differential is made. After the Price Differential is made, the 
new [[SFT]] is novated, guaranteed, and risk managed by [[NSCC]]. Simultaneously, the termed [[SFT]] is marked as settled 
and released from [[NSCC]]’s guaranty obligation.
Conversely, if the Price Differential (from a Roll transaction) does not settle at [[DTC]] before the [[EOD]] [[DTC]] Drops 
process completes, the termed [[SFT]] remains novated to, and risk managed by, [[NSCC]], while the new [[SFT]] will be 
dropped from the system and consequently not novated to, or risk managed by, [[NSCC]]. For any [[SFT]] where the Price 
Differential is not made, [[NSCC]] will update it in the following ways:
l [[mark-to-market]] the termed [[SFT]] and process the mark as part of the end of day process.  Members are provided
output from SAS to inform them that this has occurred.
l Refreshes the [[settlement]] date of the termed [[SFT]] to the next business day, while keeping the [[DTCC]] Reference [[ID]]
unchanged.
[[NSCC]]’s UTC system will be available for Roll input from its open at approximately 4:00 A.M. ET through Roll Cut-Off at 
11:30 A.M. ET.  After 11:30 A.M. ET, any Roll submission is rejected.  [[DTC]] begins processing Price Differentials in real 
time as they are sent from SAS. As noted elsewhere, it continues to recycle them through the [[EOD]] [[DTC]] Drops 
process.  
A Roll message can be submitted for full or partial [[shares]] on an active [[SFT]].  If such a Roll message is not received by 
11:30 A.M. ET, the SAS system automatically sends a [[DO]] return instruction to [[DTC]] to deliver the full [[shares]] from 
[[Borrower]]’s account at [[DTC]] versus the original [[SFT]] [[settlement]] value to the [[NSCC]] [[SFT]] account (881) at [[DTC]] Global, 
and from the [[NSCC]] [[SFT]] account (881) at [[DTC]] Global to the lender’s account at [[DTC]] for the same [[shares]] and 
[[settlement]] value.  A Roll message received for partial [[shares]] results in the SAS system immediately instructing [[DTC]] to 
deliver the remainder of [[shares]] (not rolled) and the equivalent [[settlement]] value from [[Borrower]]’s account at [[DTC]] versus 
the original [[SFT]] [[settlement]] value to the [[NSCC]] [[SFT]] account (881) at [[DTC]] Global, and from the 881 account at [[DTC]] to 
the lender’s account at [[DTC]].
[[SFT]] Clearing: General User Guide

---

## Page 23

5. General Operational Flow 23
The following examples help to show the process regarding rolls MADE versus those that DROP:
Event Day Event Outcome
Monday l New on-leg is received, validated, and the on-
leg [[DO]] is Made at [[DTC]].
l [[DTCC]] Reference [[ID]] = 05131901234567
(New [[SFT]] Reference [[ID]])
The off-leg of the [[SFT]] is novated to [[NSCC]]. 
Members are advised of the PEND off -leg set to be 
returned the next business day.
Tuesday
l New Roll (on-leg) is received and validated.
l [[DTCC]] Reference [[ID]] = 05131901234567
(Original [[SFT]] Reference [[ID]])
l [[DTCC]] Reference [[ID]] =05141989101112
(Roll Reference [[ID]])
l SAS calculates a Price Differential of $27.25
l Price Differential is MADE at [[DTC]].
l 05131901234567 (Original [[SFT]] Reference [[ID]])
is marked closed. Members receive a MADE
message.
l 05141989101112 (Roll Reference [[ID]]) is novated
to [[NSCC]]. Members receive a PEND message 
for the new off -leg return.
Example 1
Event Day Event Outcome
Monday l New on-leg is received, validated, and Made at
[[DTC]].
l [[DTCC]] Reference [[ID]] = 05131901234567
(New [[SFT]] Reference [[ID]])
The off-leg of the [[SFT]] is novated to [[NSCC]]. 
Members are advised of the PEND off -leg set to be 
returned the next business day.
Tuesday
l New on-leg is received and validated.
l [[DTCC]] Reference [[ID]] = 05131901234567
(Original [[SFT]] Reference [[ID]])
l [[DTCC]] Reference [[ID]] = 05141989101112
(Roll Reference [[ID]])
l SAS calculates a Price Differential of $27.25
l Price Differential is dropped at 3:10 P.M.
Eastern Time.
l 05131901234567 (Original [[SFT]] Reference [[ID]])
remains novated to [[NSCC]]. Members receive a
Non Return Fail message from SAS.
l [[NSCC]] processes a [[mark-to-market]] on
05131901234567 (Original [[SFT]] Reference [[ID]])
as part of its end of day process.
l [[mark-to-market]] will be for $27.25.
The SAS system sets the new [[settlement]] date to 
the next business day for 05131901234567 
(Original [[SFT]] Reference [[ID]]).
Example 2
[[SFT]] Clearing: General User Guide

---

## Page 24

5. General Operational Flow 24
5.3.2 Send-to-Settle Messages
The Send-to-Settle message is used by the [[Borrower]] to notify [[NSCC]] that it wants to return [[shares]] on an active [[SFT]]. It 
can be used to accelerate the full return of [[shares]] on the term date of an active [[SFT]] if received before the Roll cutoff 
time of 11:30 A.M. Eastern Time.   It can also be used on an [[SFT]] with a term date in the future (for example, the next 
business day), thus resulting in an accelerated return of those instructed [[shares]] on the current business day.  For the 
latter only, a Send-to-Settle message can be for the full amount of open [[shares]] or for a partial amount of the open 
[[shares]] of an active [[SFT]]. A maximum of 99 Send-to-Settle messages can be received per active [[SFT]] on a given 
business day.
Given that the [[Borrower]] is instructing [[NSCC]] to settle the [[shares]], [[NSCC]] expects that every Send-to-Settle message 
results in a MADE delivery. If the [[Borrower]] fails to make [[settlement]] on the instructed position (which becomes a Non-
Returned Fail), [[NSCC]] assesses an additional risk charge on the position (both to the [[Borrower]] and the lender) to 
address potential risk management concerns for [[NSCC]] related to such [[settlement]] failure.
The Send-to Settle message must be submitted by 3:00 P.M. Eastern Time.
5.3.3 Cancel
An Approved [[SFT]] Submitter instruction can be submitted to instruct [[NSCC]] to cancel certain pending transactions. For 
example, it can be used to cancel an on-leg that has not yet made at [[DTC]] (new [[SFT]] or Price Differential) or to cancel a 
[[DO]] instruction for an off-leg return that was sent to [[DTC]] and is still Pending  after a Send-to-Settle message was 
submitted that accelerated the return of [[shares]] from the next business day to the current business day.  A Cancel 
message cannot be used to cancel a [[DO]] off-leg return that is still Pending at [[DTC]] if the [[DO]] off-leg return was 
generated because there was no roll before 11:30 A.M. ET on the original off-leg return [[settlement]] date or if a Send-to-
Settle was received before 11:30 A.M. ET on the original off-leg return [[settlement]] date. 
Note
UTC rejects a Cancel message upon submission if the [[SFT]] is in a status where it cannot be canceled; however, the 
reject could also come from the SAS system if the Cancel message is accepted by UTC but the [[DTCC]] Reference [[ID]] 
of the [[SFT]] attempting to be canceled settles before SAS is able to cancel the Pending transaction at [[DTC]].
5.3.4 Terminate
An active [[SFT]] can be terminated either by the counterparties or, in certain circumstances, by [[NSCC]].
[[Member]] Initiated [[SFT]] Termination
At times, the [[Borrower]] and lender may choose, upon mutual agreement, to remove an active [[SFT]] from the [[SFT]] 
Clearing service. If they match such an instruction, an Approved [[SFT]] Submitter can instruct [[NSCC]] to terminate the 
[[SFT]].  [[NSCC]] removes the [[SFT]] from clearing and removes any [[obligations]] that the [[NSCC]] has to the [[SFT]].
[[SFT]] terminations can only be processed against an off-leg return and only according to one of the following scenarios:
[[SFT]] Clearing: General User Guide

---

## Page 25

5. General Operational Flow 25
Scenario 1: The [[SFT]] Termination Message is received on an active off-leg with [[settlement]] date in the future, such as 
the next business day, and there is no pending [[DO]] return at [[DTC]] due to the processing of a submitted Send-to-Settle 
instruction.
l In this scenario, the off-leg is terminated immediately. [[NSCC]] does not mark the off-leg return before processing the
[[SFT]] termination because the [[SFT]] should already have the most recent [[settlement]] value as the on-leg settled earlier
on the current business day.
Scenario 2: The [[SFT]] Termination Message is received on the [[settlement]] date of an off-leg, on or before 11:30 A.M. 
ET, and [[NSCC]] did not receive a Roll or Send-to-Settle instruction from the Approved [[SFT]] Submitter.  Given that the 
[[SFT]] Termination Message is received  prior to 11:30 A.M. ET, [[NSCC]] will not have instructed [[DTC]] to settle the 
obligation.
l In this scenario, before processing the [[SFT]] termination, the off-leg return is marked-to-market by [[NSCC]] and the
mark is passed as part of the end-of-day ([[EOD]]) money [[settlement]] value.
Scenario 3: The [[SFT]] Termination Message is received on the Non-Returned [[SFT]] after the [[EOD]] [[DTC]] DROP process 
occurs, but before the Loan Termination cutoff time. See Time Frames.
l In this scenario, SAS processes the [[SFT]] termination immediately.  Given that the [[mark-to-market]] is processed on a
Non-Returned [[SFT]] as part of the [[EOD]] money [[settlement]] process, no further processing is needed by [[NSCC]] on this
obligation.
In all of these cases, the [[SFT]] Termination Message must be submitted by 4:30 P.M. Eastern Time.
[[NSCC]] Initiated [[SFT]] Termination ([[NSCC]] Exit)
At times, a security may for reasons outside of [[NSCC]]’s control become ineligible for processing at [[NSCC]].  An example 
is if the security is undergoing a corporate action that cannot be supported through central clearing processing.  In 
these circumstances, [[NSCC]] may need to terminate the obligation in its systems. [[NSCC]] will provide clients with as 
much notice as possible that such a termination is anticipated to allow clients to attempt to [[Close Out]] the [[SFT]],  recall the 
position, terminate the [[SFT]] themselves, or all actions.  Typically, [[NSCC]]-Initiated [[SFT]] Terminations occur before the 
start-of-day [[settlement]] processing on the current business day.  When an [[NSCC]]-Initiated [[SFT]] Termination occurs, 
[[NSCC]] will [[mark-to-market]] the position to the end of day price from the prior business day (collect/pay the difference in 
end-of-day [[settlement]]) and update the [[SFT]] as settled on [[NSCC]]’s books.
5.3.5 Rate Modification
From time-to-time, the lender may need to reset the rate for an [[SFT]].  Any Rate Modification message causes [[NSCC]] to 
update its calculations for the rate payment due on the targeted [[SFT]], which is paid out the next business day.  A Rate 
Modification message can be submitted anytime throughout the business day, but will only be processed after both the 
[[DTC]] [[EOD]] drops process and the Rate Modification cutoff time (which is 3:45 P.M. Eastern Time) have occurred on a 
given business day.  In addition, [[NSCC]] only processes the latest Rate Modification message received for that [[SFT]].  The 
updated rate will only be guaranteed by [[NSCC]] after it is received by the risk system.
The Rate Modification message follows the standard flow whereby the [[DTCC]] Reference [[ID]] identifies which [[SFT]] to 
update for the new rate. 
The Rate Modification message must be submitted by 3:45 P.M. Eastern Time.
Note
A Rate Modification message can also be used to update which counterparty to the [[SFT]] is expected to receive the 
overnight rate.
[[SFT]] Clearing: General User Guide

---

## Page 26

5. General Operational Flow 26
5.3.6 Recall
A Recall message can be submitted by the lender at any time during the business day between 8:00 A.M. and 4:30 
P.M. Eastern Time for any outstanding off-leg return.  A Recall can be for full or partial [[shares]] of a [[DTCC]] Reference [[ID]].
If a Recall message exceeds the number of [[shares]] already recalled for a [[DTCC]] Reference [[ID]], it is rejected.  When a
Recall message is submitted, [[NSCC]] generates a unique Recall [[ID]] that is used to track the Recall.
l If a Recall message is received before 3:00 P.M. Eastern Time, the Recall Process Date equals the current
business day and the Allowed Buy-In Execution Date is two business days later after the [[DTC]] Drop cutoff time on
such day.
l If a Recall message is received on or after 3:00 P.M. Eastern Time, the Recall Process Date equals the current
business day, but the Allowed Buy-In Execution Date is three business days later after the [[DTC]] Drops cutoff time
on such day.
For example:
l [[NSCC]] receives a Recall message at 2:59:59 P.M. Eastern Time on Monday. The [[Borrower]] has until the end of
[[settlement]] at approximately 3:10 P.M. Eastern Time on Wednesday to deliver the [[shares]]. If they are not received,
the lender can execute the buy-in.
l [[NSCC]] receives a recall at 3:00 P.M. Eastern Time on Monday. The [[Borrower]] has until the end of [[settlement]] at
approximately 3:10 P.M. Eastern Time on Thursday to deliver the [[shares]]. If they are not received, the lender can
execute the buy-in.
[[NSCC]] tracks the amount of [[shares]] in each [[SFT]] separately by [[DTCC]] Reference [[ID]] and sub-tracks those [[shares]] of 
such [[SFT]] in the Recall status by individual Recall message received. For example:
l [[DTCC]] Reference [[ID]] A1 = 100 [[shares]] and there are two Recalls submitted – one for 20 [[shares]] and the other for 10
[[shares]].  The Recall share amounts is not combined.  They are sub-tracked at 20 [[shares]] (Recall), 10 [[shares]] (Recall),
and 70 [[shares]] (No Recall).
To maintain the [[DTCC]] Reference [[ID]] of a loan with a full or partial Recall applied to it, [[NSCC]] (rather than the industry) 
initiates the Price Differential on the loan.  In other words, a Roll message for that [[DTCC]] Reference [[ID]] that has a Recall 
is blocked. The Price Differential is performed by [[NSCC]] each business day that the Recall remains outstanding on the 
entire [[DTCC]] Reference [[ID]] by using prior business day’s closing risk price and other information from the most current 
on-leg message submission of the [[DTCC]] Reference [[ID]] (for example, IA Rate, Rounding Indicator).
[[NSCC]] begins sending Price Differentials for loans that have Recalls on them to [[DTC]] at 5:00 A.M. Eastern Time.  After 
[[NSCC]] receives a MADE message on the Price Differential from [[DTC]], [[NSCC]] keeps the original [[DTCC]] Reference [[ID]] 
and move the off-leg return [[settlement]] Date to the next business day.
Note
l Although a loan may have one or more Recalls applied to it that are being sub-tracked, when a Price Differential
settles, [[NSCC]] sends only one message (for the entire amount of the [[DTCC]] Reference [[ID]]) to Approved [[SFT]]
Submitters/Members with the status update of that Price Differential (for example, MADE).
l For SFTs that have Recalls applied to them, [[NSCC]] will not automatically generate any [[DO]] off-leg return to [[DTC]].
[[SFT]] Clearing: General User Guide

---

## Page 27

5. General Operational Flow 27
Send-to-Settle Messages and Recalls
An off-leg return is only processed by [[NSCC]] and sent to [[DTC]] when [[NSCC]] receives a full or partial Send-to-Settle 
message to return the [[shares]]. After receiving a MADE or DROP message from [[DTC]] as a result of processing a Send-
to-Settle message, [[NSCC]] distributes the messages to Members and Approved [[SFT]] Submitter as follows:
l If the Send-to-Settle is MADE and is for the full amount of the [[outstanding shares]], which closes out the entire
[[SFT]]:
o An ISO Message (CNSESFTO) is distributed informing that the off-leg [[DO]] return for that [[SFT]] (from the Send-to-
Settle message) was MADE.
o Regardless of the number of Recalls outstanding for that [[SFT]], there will be no Recall update messages
distributed, as the entire [[SFT]] was closed.
ll If the Send-to-Settle is MADE and is for a partial amount of the outstanding [[SFT]], which closes out part of the
[[SFT]]:
Note
Since a MADE [[DO]] off-leg return will always be applied against the oldest outstanding Recall (based on date and 
time order), a partial MADE [[DO]] return (ISO message CNSESFTO) will be followed up with an additional ISO 
Message (CNSISOO) for each Recall that was updated.
o An ISO Message (CNSESFTO) is distributed informing that the off-leg [[DO]] return (from the Send-to-Settle
message) was MADE.
o ISO message includes the number of Recall messages to follow plus the total Recall quantity of those
messages. (Note: This is for balancing).
o An ISO message (CNSISOO) for each impacted Recall [[ID]] is distributed informing that the outstanding position
for that Recall [[ID]] was reduced or closed out.
o The number of Recall messages and their total quantity must equal what was communicated in the ISO
message regarding the MADE update of the [[SFT]]
Note
Since the  updated [[SFT]] MADE message and the Recall update MADE messages are being distributed from 
separate systems, there is the remote possibility that a Recall update MADE message is received before the 
updated [[SFT]] MADE message.
l If the Send-to-Settle is a DROP and is for the full or partial amount of the outstanding [[SFT]]:
o An ISO message (CNSESFTO) is distributed to both Members and the Approved [[SFT]] Trade Submitter with a
status of NRET - Non Return Fail.
[[SFT]] Clearing: General User Guide

---

## Page 28

5. General Operational Flow 28
Corporate Actions and Recalls
l If a Recall message is submitted on a security undergoing a mandatory corporate action or [[Dividend]] distribution that
[[NSCC]] does support, the following occurs:
o If it is a forward [[Stock]] split, SAS will block the submission of a buy-in execution on both the business day prior to
due bill redemption date (which is ex-date of the forward split) and the due bill redemption date.  The reason for
this is that although the marketplace will adjust the price for the security on ex-date, both [[DTC]] and [[NSCC]] [[DO]] not
adjust the split [[shares]] and price until two days after the marketplace payable date.
o If it is a name change, [[Stock]] merger, cash merger, reverse split or cash and [[Stock]] merger, SAS will accept the
submission of a buy-in execution on the business day prior to payable date (or [[DTC]] Swing Date).
l If SAS processes a mandatory corporate action event (name change, [[Stock]] merger, cash & [[Stock]] merger, reverse
split) or forward [[Stock]] split and the [[SFT]] has a Recall, the Recall [[ID]] will be updated proportionately to the new
security and/or position after the corporate action was processed. The SAS system will distribute the following
messages to Members and the Approved [[SFT]] Submitter:
o An ISO Message (CNSESFTO) will be distributed informing that the current original off-leg return for that entire
[[SFT]] was MADE
o Regardless of the number of Recalls outstanding for that [[SFT]], there will be no Recall messages that will be
distributed as the entire [[SFT]] was closed
o An ISO message (CNSESFTO) is distributed informing of the new [[CUSIP]], quantity of the [[SFT]], or both after
processing the event. The ISO message is distributed with a status of PEND. This ISO message:
o Does not apply to a cash merger as the entire [[SFT]] is being cashed out.
o Includes the number of Recall messages to follow plus the total Recall quantity of those messages. (Note:
This is for balancing).
Note
The [[DTCC]] Reference [[ID]] of the [[SFT]] remains the same.
o An ISO message (CNSISOO) is distributed informing (for each impacted Recall) the number of outstanding
[[shares]] for that Recall that was updated as a result of processing the event.
o ISO message is distributed with a status of UPTD.
o Number of Recall messages and their total quantity must equal what was communicated in the ISO message
regarding the PEND status of the [[SFT]].
o Does not apply to a cash merger as the entire [[SFT]] was cashed out.
Note
Since the updated [[SFT]] PEND message (from processing event) and the Recall update UPTD messages are 
being distributed from separate systems, there is the remote possibility that a Recall update UPTD message 
is received before the updated [[SFT]] PEND message.
[[SFT]] Clearing: General User Guide

---

## Page 29

5. General Operational Flow 29
Example – Forward [[Stock]] Split
An [[SFT]] is outstanding for 1,000 [[shares]] and has one Recall of 100 [[shares]] on a security undergoing a 2 for 1 forward 
[[Stock]] split where the Marketplace payable date = Monday, Ex-Date =Tuesday, SAS Position Capture Date (at Close 
of Business) = Wednesday, and SAS Payable Date = Wednesday after [[DTCC]] [[settlement]] completes at the end of the 
day. 
l On Tuesday (Ex-Date) and Wednesday (due bill redemption date), a buy-in execution is blocked because SAS (like
[[DTC]]) does not split the [[shares]] and value (price split) until after [[settlement]] date completes on Wednesday for
Thursday's [[settlement]] date, and the security is already trading in the marketplace at the post-split price on Tuesday.
l When SAS updates the [[SFT]] position after paying the [[Stock]] split, the [[SFT]] will now be 2,000 and the Recall will be
200 [[shares]].
l An ISO message (CNSESFTO) is sent informing that [[SFT]] was updated from 1,000 [[shares]] to 2,000 [[shares]].
l An ISO message (CNSISOO) is sent informing that Recall was updated from 100 to 200 [[shares]].
Example – [[Stock]] Merger
An [[SFT]] is outstanding for 1,000 [[shares]] and has one recall of 130 [[shares]] and another of 20 [[shares]] on a security 
undergoing a [[Stock]] merger where for every 25 [[shares]] of the old security a payment is made to 1 share of the new 
security and where the industry effective date = Thursday and SAS Payable Date ([[DTC]] Swing Date) = Thursday.
l When SAS updates the [[SFT]] position after paying the [[Stock]] merger on Thursday, the [[SFT]] is updated to 40 [[shares]] of
the new security and the first Recall is calculated at 5.2 [[shares]] (130 / 25)
Note
Fractional [[shares]] should be dropped so it will be updated to 5 [[shares]]. The second Recall will be 0 [[shares]], as after 
processing proportionate the split, there are no remaining whole [[shares]]. 
l An ISO message (CNSESFTO) is sent informing that the [[SFT]] was updated to 40 [[shares]] (as a result of the [[Stock]]
merger), with a Recall counter of 2.
l Two ISO messages (CNSISOO) are sent to informing that the:
o First Recall was updated to 5 [[shares]].
o Second Recall was closed.
[[SFT]] Termination or Exit Message (applied to an [[SFT]] that has outstanding recall positions)
If an [[SFT]] Termination Message is received for an [[SFT]] that has been recalled, the [[SFT]] is terminated immediately even 
if it is received on the Allowed Buy-In Execution Date.
After processing an [[SFT]] termination or exit, an ISO message (CNSESFTO) is distributed informing that the original off-
leg return for the entire [[SFT]] was MADE.  Regardless of the number of Recalls outstanding for that [[SFT]],  no Recall 
messages are distributed as the entire [[SFT]] was closed.
[[SFT]] Clearing: General User Guide

---

## Page 30

5. General Operational Flow 30
5.3.7 Buy-in Process
When the Allowed Buy-In Execution Date has been reached, the lender is allowed to process a buy-in execution equal 
to or less than the total number of [[shares]] of all Recalls for that [[DTCC]] Reference [[ID]] which has reached the Allowed 
Buy-In Execution Date.
A buy-in execution can be submitted between [[DTC]] Drop cutoff time and 5:00 P.M. ET on the Allowed Buy-In 
Execution Date and on any subsequent business day as long as a Recall remains open on that [[DTCC]] Reference [[ID]].  If 
an execution message is received before 4:30 P.M. ET, the output status of the buy-in execution message is marked 
as Received. After a buy-in execution is received, [[NSCC]] issues a buy-in execution [[ID]].  [[NSCC]] then sends a follow-up 
message before 5:00 P.M. ET with a marked status of accepted or rejected. 
If an execution message is received between 4:30 P.M. ET and 5:00 P.M. ET, [[NSCC]] sends an immediate 
message with a status of accepted or rejected.  Between approximately 5:20 P.M. and 5:30 P.M. ET, [[NSCC]] 
processes the accepted buy-in execution message.  However, although processed by the SAS system the day it was 
received, the entries that report the collection/payment of money resulting from the buy-in execution are reported on 
the next business day’s Night Miscellaneous Activity file, which gets distributed around 12:30 A.M. ET. These entries 
allow [[NSCC]] to calculate the money difference between the [[settlement]] amount and the execution amount for each 
[[Member]].  It is reported on the Night Miscellaneous Activity file with the following entries:
l [[Borrower]] (deliverer) receives [[shares]].
l [[Borrower]] (deliverer) gets a credit of the [[settlement]] Amount.
l [[Borrower]] (deliverer) gets a debit of the Execution Amount.
l Lender (receiver) gets a Deliver of [[shares]].
l Lender (receiver) gets a debit of the [[settlement]] Amount.
l Lender (receiver) gets a credit of the Execution Amount.
The money difference (debit/credit) is included (along with other entries) in the [[Member]]’s overall Fed Funds [[settlement]] 
(FFS) code 132 ([[SFT]] Buy-in, Exit & Reorg) balance on their [[NSCC]] [[participant]] Account Statement collected/paid at the 
end of the next [[settlement]] day.
A buy-in execution that is submitted for more [[shares]] than the total number of [[shares]] of all Recalls outstanding in the 
database for a given [[DTCC]] Reference [[ID]] is rejected.
A buy-in execution can be submitted in multiple partials or as one total of all Recalls outstanding for that [[DTCC]] 
Reference [[ID]].  The first buy-in execution, depending on the way it is submitted, should be applied to [[shares]] of the 
oldest Recall in the database.  For any remaining [[shares]] of a Recall [[ID]] that have not been executed against, the Recall 
is still attached to such remaining [[shares]].
Input the buy-in execution messages in the MT542 format.  Unlike other [[SFT]] input messages, whose destination is the 
[[DTCC]]’s front-end UTC system, the buy-in messages are sent directly by clients to the core SAS system.  The output 
messages back to clients are sent in the MT548 (modified) format from SAS.  For more information about the layout 
fields of the input and the output buy-in messages, see Message Layouts.
[[SFT]] Clearing: General User Guide

---

## Page 31

5. General Operational Flow 31
5.3.8 Buy-in Execution Applied to an Outstanding [[SFT]] Position
When a Buy-in Execution is received by the SAS system and closes out the ENTIRE [[SFT]], an ISO message 
(CNSESFTO) is sent informing that as of the result of a Buy-in Execution, the [[SFT]] was MADE.  Regardless of the 
number of recalls outstanding for that [[SFT]], no recall update messages are distributed as the entire [[SFT]] is closed.
When a Buy-in Execution is received by the SAS system and closes out PART of [[SFT]], the Buy-in Execution is always 
applied against the oldest outstanding Recall based on date and time order. The buy-in execution results in the 
following messages to Members and the Approved [[SFT]] Submitter:
Note
This occurs even if the buy-in execution closes out all the outstanding recall positions that were eligible to be bought 
in.
l An ISO message (CNSESFTO) is distributed informing of the partial [[shares]] of the off-leg that were executed. This
ISO message is distributed with a status of MADE.
o This ISO message includes the number of Recall messages to follow plus the total recalled quantity of those
messages. (Note: This is for balancing).
l An ISO message (CNSISOO) for each impacted Recall [[ID]] is distributed informing of the number of outstanding
[[shares]] for that Recall [[ID]] that was reduced or closed out. This ISO message is distributed with a status of EXED.
o The number of Recall messages and their total quantity must equal what was communicated in the ISO message
(CNSESFTO) regarding the update of the [[SFT]].
Note
Since the updated [[SFT]] MADE message (from execution) and the recall update EXED messages are being 
distributed from separate systems, there is the remote possibility that a recall update EXED message is 
received before the updated [[SFT]] MADE message.
If an [[SFT]] Termination Message is received with respect to a given [[DTCC]] Reference [[ID]] on or after the Allowed Buy-In 
Execution Date (between [[DTC]] Drop cutoff time and 4:30 P.M. ET), it always supersedes any buy-in execution 
message received by [[NSCC]] that same day.  The buy-in execution will be rejected.
[[SFT]] Clearing: General User Guide

---

## Page 32

5. General Operational Flow 32
5.3.9 Cancel Recall
A Cancel Recall message can only be submitted between 8:00 A.M. and 4:30 P.M. Eastern Time.   A Cancel Recall 
message is immediately applied by [[NSCC]].  
Note
There can be no partial submission of a Cancel Recall message against a Recall [[ID]] for a [[DTCC]] Reference [[ID]].  A 
Cancel Recall message must always be for the full amount of recalled [[shares]].
If a [[DTCC]] Reference [[ID]] no longer has a Recall message attached to it, [[NSCC]] no longer applies the recall process to 
the [[DTCC]] Reference [[ID]]. [[NSCC]] also allows it to be rolled by the Members going forward.
If on the Allowed Buy-in Execution Date, after Drops have occurred at [[DTC]], both a Cancel Recall Message and a Buy-
in Execution message are received, the Cancel Recall message is applied regardless of which message was 
submitted first.
5.3.10 Cancel Buy-in Execution
A Cancel Buy-in Execution message can be submitted to cancel a previously submitted buy-in execution that was 
accepted on the same processing day. A Cancel Buy-In Execution message must be submitted with the buy-in 
execution [[ID]]. After being received and accepted by [[NSCC]], it voids the previously submitted Buy-In Execution 
message. A Cancel Buy-in Execution message can be submitted any time after the Buy-In Execution message was 
submitted until 5:00 P.M. ET.
[[SFT]] Clearing: General User Guide

---

## Page 33

5. General Operational Flow 33
5.4 Calculating the [[settlement]] Value of an [[SFT]] 
[[NSCC]] supports industry conventions around calculation of the [[settlement]] value of a transaction, namely, rounding 
conventions and over collateralizing an [[SFT]], referred to as Independent Amount (IA), due to either regulatory 
requirements or standardized agreements. The following table outlines the formula [[NSCC]] will take in calculating the 
[[settlement]] value of an [[SFT]]. It also provides an example.
Field Description Rounding 
Rule 
Applied 
[[DTCC]] 
Process
Calculation Rule Example
Original Price Security price agreed on 
the trade.
Receive, 
required
N/A 100.03
Quantity Share quantity agreed on 
the trade.
Receive, 
required
N/A 10
Independent Amount Percent of independent 
amount included on the 
trade.
Receive, 
required
N/A 2%
Rate Rate paid on the trade.
Receive, 
required
N/A 5%
Rounding Rule Rule requested by market 
for rounding calculation.
Receive, 
required
Round up to the nearest 
requested increment. For 
increments, see Rounding 
Rules.
4 = up to 
nearest 
$0.25
Settle Price Full price, inclusive of 
independent amount, 
agreed to for [[settlement]].
Yes Calculate Round [Original Price * (1+ IA 
Rate)]
102.25
[[settlement]] Value Value of the trade sent to 
[[settlement]].
Calculate Settle Price * Quantity 1,022.50
Contract Value Calculated contract 
amount of loan 
transaction.
Calculate Share Quantity * Share Price 1,000.30
Rate Amount Amount of rate paid on 
trade.
Calculate [[settlement]] value * interest 
rate 360
0.14
Independent Amount Independent amount 
applied on the trade.
Calculate [[settlement]] Value - (Quantity * 
Original Price)
22.20
Notes
[[DTCC]] rounds according to rules outlined in Key Business Validations for On-leg Transactions.
[[SFT]] Clearing: General User Guide

---

## Page 34

5. General Operational Flow 34
5.5 Calculating and Processing Rate Payments
Each [[SFT]] is a term trade; therefore, [[NSCC]] calculates and pays the rate on a daily basis. [[NSCC]] applies standard rate 
payment calculations to the [[SFT]] and notifies all parties to the transaction of that calculation in the Outstanding Loan 
[[EOD]] MRO file on a daily basis. 
The rate is due on term date. On the date that the [[SFT]] is received, [[NSCC]] sets up and guarantees the payment of the 
rate on the next business day. The rate is based on the following calculation:
Rate =  Rate on [[SFT]] x
[[settlement]] Value x Number of Days
360
Any [[SFT]] that is opened and settles or is terminated the same day has no rate paid. For example, if the [[Borrower]] loses 
purpose and returns [[shares]] to the lender on the same day that the [[SFT]] was opened, no rate is paid because the 
[[shares]] were returned on the same day that they were borrowed.
Members see the net amount of a rate that was applied on their Fed Funds [[settlement]] (FFS) code 130 balance ([[SFT]] 
Rebate Interest) on their [[NSCC]] [[participant]] Account Statement. Members have either a net debit, credit, or no balance. 
Each [[Member]] can reconcile what comprises their net rate amount by consuming the Outstanding Loan [[EOD]] MRO File 
that [[NSCC]] will distribute earlier around 5:45 P.M. Eastern Time.  Each open [[SFT]] transaction for a [[Member]] is in that file 
and have the calculated rate for that specific [[DTCC]] Reference [[ID]].
Note
Since [[NSCC]] pays out the rate on a daily basis and SFTs have an overnight term, [[NSCC]]’s guaranty of rate is complete 
once that rate payment is settled. If borrowers and lenders made errors to the rate on SFTs that have already settled, 
those errors must be corrected outside of [[NSCC]].
[[SFT]] Clearing: General User Guide

---

## Page 35

5. General Operational Flow 35
5.6 Corporate Actions Processing
[[NSCC]] supports the processing of certain corporate actions through its [[SFT]] Clearing service. To this end, the following 
table shows the supported mandatory dividends and corporate actions.
Dividends and Corporate Actions Code
Cash [[Dividend]] 08
Forward [[Stock]] Split 02
Reverse [[Stock]] Split* 73
Name Change* 91
Cash Merger 72
[[Stock]] Merger* 71
Cash and [[Stock]] Merger* 90
Table 5.1  Supported Corporate Actions
Note
Unlike a street-side loan, a buy-side loan (or loan between a Sponsoring [[Member]] and Sponsor, as outlined in Section 5.11 
Sponsoring and Sponsored [[Member]] Process, will not be updated in the system by [[SFT]] Clearing for a supported corporate action 
event. Specifically, when a forward [[Stock]] split is processed, although the forward split is paid in the marketplace on Ex-Date 
([[shares]] and price), [[NSCC]] does not process the split ([[shares]] and price) until after the end of day [[settlement]] completes on ex-date 
+1 (two full [[settlement]] days later). This is because the standard [[settlement]] cycle is T+2 and trades processed on the two previous
days prior to ex-date (with presplit [[shares]] and value) are settling on ex-date and ex-date +1. As a result, on ex-date and ex-date+1
when a security is undergoing a forward [[Stock]] split, a Sponsoring [[Member]] may have a mismatch on their books for reconciliation
between their buy-side and street-side loans. A buy-side loan on these days (ex-date and ex-date + 1) needs to be submitted to
[[NSCC]] with the post -split [[shares]] and price even though a street side loan (where a roll can occur) continues to be recorded and
processed in SAS with the presplit [[shares]] and price. Additionally, when the Approved Trade Submitter submits a buy-side loan on
these days (ex-date and ex-date+ 1), they must provide the market price upon submission of these transactions. They should not
leave the price blank and request that [[NSCC]] use its price because [[NSCC]] still applies the presplit price (price from SV),  which
greatly overvalues the buy-side loan that impacts the margining between the Sponsoring [[Member]] and Sponsor.
All other corporate actions, either voluntary or mandatory, are not supported. Corporate actions where there is a 
conversion of one security into multiple [[securities]] or a convergence of multiple supported corporate actions on the 
same day are not supported.  Moreover, the [[Proxy]] (assignment of [[Proxy]] votes) is not supported in the [[SFT]] Clearing 
service. The following process applies for SFTs in [[securities]] undergoing a corporate action (either supported or not 
supported, including cash dividends):
*Furthermore, when the Approved Trade Submitter submits a buy-side loan on the [[NSCC]] Payable Date in the new [[CUSIP]] of a
security resulting from a [[Stock]] merger (71), cash & [[Stock]] merger (90), reverse [[Stock]] split (73), or name change (91), the market price
should always be submitted on these [[SFT]] loan transactions. The Approved Trade submitter should not leave the price blank and
request that [[NSCC]] use its price because [[NSCC]] may apply a [[default]] price of a $0.01 for the new [[CUSIP]] as there was no closing
market price from the prior business day.
[[SFT]] Clearing: General User Guide

---

## Page 36

5. General Operational Flow 36
Expiration 
Date for a 
Voluntary 
Event 
(with protect 
date)
Expiration 
Date for a 
Voluntary 
Event (with 
no protect 
date)
Record Date or Due 
Bill Redemption 
Date for a [[Stock]] 
Distribution (such 
as [[Stock]] [[Dividend]] 
or Spinoff)
[[NSCC]] Payable Date for 
a Mandatory event 
(Name Change, Cash 
Merger, [[Stock]] Merger, 
Cash & [[Stock]] Merger & 
Reverse Split) 
[[NSCC]] 
Payable 
Date for a 
Forward 
[[Stock]] 
Split
Cash 
[[Dividend]]
Not Supported Not 
Supported
Not Supported Supported Supported Supported
Five 
Business 
Days Prior
New Loans 
Blocked; Rolls 
are Allowed
New Loans 
Blocked; 
Rolls are 
Allowed
New Loans Blocked; 
Rolls are Allowed
New Loans Blocked; 
Rolls are Allowed
New Loans 
Blocked; 
Rolls are 
Allowed
Both New 
Loans & 
Rolls 
Allowed
Three 
Business 
Days Prior 
Existing [[SFT]] 
Loans exited; 
Both New 
Loans & Rolls 
are Blocked
Existing [[SFT]] 
Loans exited; 
Both New 
Loans and 
Rolls are 
Blocked
Existing [[SFT]] Loans 
exited; Both New 
Loans & Rolls are 
Blocked
New Loans Blocked; 
Rolls are Allowed
New Loans 
Blocked; 
Rolls are 
Allowed
Both New 
Loans & 
Rolls 
Allowed
[[NSCC]] 
Payable 
Date 
N/A N/A N/A New Loans and Rolls are 
Blocked
New Loans 
Blocked; 
Rolls are 
Allowed
Both New 
Loans & 
Rolls 
Allowed
[[NSCC]] 
Payable 
Date +1 
N/A N/A N/A Old [[CUSIP]] is gone; New 
Loans & Rolls are 
Allowed for new [[CUSIP]] (if 
applicable)
New Loans 
are 
Allowed; 
Rolls are 
Blocked
Both New 
Loans & 
Rolls 
Allowed
[[NSCC]] 
Payable 
Date + 2
N/A N/A N/A Old [[CUSIP]] is gone; New 
Loans & Rolls are 
Allowed for new [[CUSIP]] (if 
applicable)
New Loans 
& Rolls are 
Allowed
Both New 
Loans & 
Rolls 
Allowed
Protect 
Date + 1 
Both New 
Loans & Rolls 
are Blocked
N/A N/A N/A N/A N/A
Protect 
Date + 2 
Both New 
Loans & Rolls 
Allowed
N/A N/A N/A N/A N/A
Expiration 
Date + 1
N/A Both New 
Loans & 
Rolls are 
Blocked
N/A N/A N/A N/A
[[SFT]] Clearing: General User Guide

---

## Page 37

5. General Operational Flow 37
Expiration 
Date for a 
Voluntary 
Event 
(with protect 
date)
Expiration 
Date for a 
Voluntary 
Event (with 
no protect 
date)
Record Date or Due 
Bill Redemption 
Date for a [[Stock]] 
Distribution (such 
as [[Stock]] [[Dividend]] 
or Spinoff)
[[NSCC]] Payable Date for 
a Mandatory event 
(Name Change, Cash 
Merger, [[Stock]] Merger, 
Cash & [[Stock]] Merger & 
Reverse Split) 
[[NSCC]] 
Payable 
Date for a 
Forward 
[[Stock]] 
Split
Cash 
[[Dividend]]
Expiration 
Date + 2 
N/A Both New 
Loans & 
Rolls Allowed
N/A N/A N/A N/A
Record 
Date + 1
N/A N/A Both New Loans & 
Rolls Allowed
N/A N/A Both New 
Loans & 
Rolls 
Allowed
Record 
Date + 2
N/A N/A Both New Loans & 
Rolls Allowed
N/A N/A Both New 
Loans & 
Rolls 
Allowed
Note
For American Depositary Receipts (ADRs) where the country of origin is not the United States, [[NSCC]] tracks the 
substitute payment at ONLY one rate, which is the most prevalent [[DTC]] rate.
[[SFT]] Clearing service does not perform corrections to terms for supported corporate actions following the payable date. 
This, however, does not apply to cash dividends, whose pay rate can be changed and subsequently adjusted by the 
[[SFT]] Clearing service after the original payable date.  Changes to all supported corporate actions that take place prior to 
the payable date are automatically adjusted and applied by the system. 
In support of the corporate action processing in [[SFT]], [[DTCC]] makes the following output available to [[NSCC]] [[Member]] 
firms:
l Miscellaneous Activity MRO (corporate action output is shown alongside with information relating to other activity)
l [[Dividend]] Activity MRO
l [[Dividend]] with Due Bill Activity MRO
l Record Date Print Image
For more information relating to the corporate action output as well other [[SFT]] outputs, see File and Report Layouts.
[[SFT]] Clearing: General User Guide

---

## Page 38

5. General Operational Flow 38
5.7 Miscellaneous Activity Journal Entries for [[SFT]] Processing
For [[SFT]] (Sub-Account T), Members should not use the Miscellaneous Activity file for updating the status of 
outstanding SFTs as a result of processing a buy-in execution, corporate action event, termination, or exit. As 
described above, [[SFT]] status updates from processing any of these events will be provided to both the Members and 
their Approved [[SFT]] Submitter via ISO message(s). The primary purpose of the Miscellaneous Activity file is to record 
Miscellaneous Journal entries that show updates to an outstanding [[SFT]] as a result of processing any buy-in execution, 
corporate action event, forward [[Stock]] split, termination, or exit that results in a collection/payment of money by [[NSCC]] 
against the counterparty to the [[SFT]]. However, in some cases, the recorded Miscellaneous Journal entries result in no 
payment (for example, name change).
In addition to Description, ISIN, and Code and Explanation, the Miscellaneous Activity file also has the following 
sections:
Received/Delivered
This section is used to communicate the quantity of the [[shares]] of the [[SFT]] that were impacted by the event.
It follows traditional [[CNS]] logic: 
l Received [[shares]] to the [[Borrower]] (deliverer) represents that their pending off-leg return owed to [[NSCC]] was offset.
l Delivered [[shares]] to the [[Borrower]] (deliverer) represent the new quantity of [[shares]] and/or [[CUSIP]] of that [[SFT]] that the
[[Borrower]] owes to [[NSCC]] as a result of processing the entry.
l Delivered [[shares]] to the Lender (receiver) represents that the pending off-leg return they are expecting to receive
from [[NSCC]] was offset.
l Received [[shares]] to the Lender (receiver) represents the new quantity of [[shares]] and/or [[CUSIP]] of that [[SFT]] that
[[NSCC]] owes to them as a result of processing the entry.
l Entries above are only for informational purposes and should not be used to process [[SFT]] updates.
Debit/Credit
This is the primary purpose of the Miscellaneous Journal entry. The posted entries should result in the 
collection/payment of money by [[NSCC]] for an [[SFT]]. The net money will be included in a [[Member]]’s new Fed Funds 
[[settlement]] Code 132 on their [[NSCC]] [[participant]] Account statement. Unlike the share entries above, the money entries 
recorded by [[NSCC]] are to effect the net cash that needs to be processed as a result of processing the updates.
The logic is as follows:
l Credit to the [[Borrower]] represents the [[settlement]] value of the [[SFT]] (or part of that [[SFT]]) being closed out.
l Debit to the [[Borrower]] represents the execution value from a buy-in execution, corporate action payment value, or
new [[settlement]] value after processing a mark for an [[SFT]] termination or exit.
o Debit to the [[Borrower]] also represents, for corporate action payments, any cash-in lieu owed by them on fractional
[[shares]] after processing the event.
l Debit to the Lender represents the [[settlement]] value of the [[SFT]] (or part of the [[SFT]]) being closed out.
l Credit to the Lender represents the execution value from a buy-in execution, corporate action payment value or new
[[settlement]] value after processing a mark for an [[SFT]] termination.
o Credit to the Lender also represents, for corporate action payments, any [[Cash-in-Lieu]] owed to them on fractional
[[shares]] after processing the event.
[[SFT]] Clearing: General User Guide

---

## Page 39

5. General Operational Flow 39
Examples of how Miscellaneous Activity is processed in MRO File
1. [[Member]]-Initiated [[SFT]] Termination (With Mark) or [[NSCC]]- Exit (With Mark).
l There is an outstanding off-leg return ([[SFT]] [[ID]] A1) for 100 [[shares]] versus $1,000.
o [[Borrower]] has a DVP obligation for (100) [[shares]] versus $1,000 against [[NSCC]].
o Lender has an RVP obligation for 100 [[shares]] versus ($1,000) against [[NSCC]].
l When [[SFT]] is terminated/exited, the market value is $1,100.
l When processed, the Miscellaneous Journal entries appear as follows:
Received Delivered Debit Credit Miscellaneous 
Code
Deliverer 
([[Borrower]])
100
$1,100
([[SFT]] Value at 
Termination)
$1,000 
(Original [[SFT]] Value)
02 – Ineligible 
Security 
Total $1,100 $1,000 
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $100 DB
Received Delivered Debit Credit Miscellaneous 
Code
Receiver 
(Lender) 
100 $1,000
(Original [[SFT]] Value)
$1,100
([[SFT]] Value at 
Termination)
02 – Ineligible 
Security 
Total $1,000 $1,100
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $100 CR
2. [[Member]]-Initiated [[SFT]] Termination (No Mark) or [[NSCC]] Exit (No Mark).
l There is an outstanding off-leg return ([[SFT]] [[ID]] A1) for 100 [[shares]] versus $1,000.
o [[Borrower]] has a DVP obligation for (100) [[shares]] versus $1,000 against [[NSCC]].
o Lender has an RVP obligation for 100 [[shares]] versus ($1,000) against [[NSCC]].
l When [[SFT]] is terminated/exited, the market value is still $1,000.
l When processed, the Miscellaneous Journal entries appear as follows:
Received Delivered Debit Credit Miscellaneous 
Code
Deliverer 
([[Borrower]])
100
$1,000
([[SFT]] Value at 
Termination)
$1,000 
(Original [[SFT]] Value)
02 – Ineligible 
Security 
Total $1,000 $1,000 
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $0
Received Delivered Debit Credit Miscellaneous 
Code
[[SFT]] Clearing: General User Guide

---

## Page 40

5. General Operational Flow 40
Received Delivered Debit Credit Miscellaneous 
Code
Receiver 
(Lender) 
100 $1,000
(Original [[SFT]] Value)
$1,000
([[SFT]] Value at 
Termination)
02 – Ineligible 
Security 
Total $1,000 $1,000
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $0
3. Buy-in Execution
l There is an outstanding off-leg return ([[SFT]] [[ID]] A1) for 100 [[shares]] versus $1,000.
o [[Borrower]] has a DVP obligation for (100) [[shares]] versus $1,000 against [[NSCC]].
o Lender has an RVP obligation for 100 [[shares]] versus ($1,000) against [[NSCC]].
l Buy-in execution submitted by the Lender on 100 [[shares]] is for $1,100 (Execution Value).
l When processed, the Miscellaneous Journal entries appear as follows:
Received Delivered Debit Credit Miscellaneous 
Code
Deliverer 
([[Borrower]])
100
$1,100
(Execution Value)
$1,000 
(Original [[SFT]] 
Value)
77 – Buy-in 
Execution 
Total $1,100 $1,000 
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $100 DB
Received Delivered Debit Credit Miscellaneous 
Code
Receiver (Lender) 
100 $1,000
(Original [[SFT]] 
Value)
$1,100
(Execution Value)
77 – Buy-in 
Execution 
Total $1,000 $1,100
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $100 CR
4. Cash Merger
l There is an outstanding off-leg return ([[SFT]] [[ID]] A1) for 100 [[shares]] versus $1,000.
o [[Borrower]] has a DVP obligation for (100) [[shares]] versus $1,000 against [[NSCC]].
o Lender has an RVP obligation for 100 [[shares]] versus ($1,000) against [[NSCC]].
l Cash merger value on 100 [[shares]] is for $1,100 (Cash Merger Value).
l When processed, the Miscellaneous Journal entries will appear as follows:
[[SFT]] Clearing: General User Guide

---

## Page 41

5. General Operational Flow 41
Received Delivered Debit Credit Miscellaneous Code
Deliverer 
([[Borrower]])
100 $1,100
(Cash Merger 
Value)
$1,000 
(Original [[SFT]] Value)
51 Merger
Total $1,100 $1,000 
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $100 DB
Received Delivered Debit Credit Miscellaneous Code
Receiver (Lender) 100 $1,000
(Original [[SFT]] Value)
$1,100
(Cash Merger 
Value)
51 Merger
Total $1,000 $1,100
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $100 CR
5. [[Stock]] Merger
l There is an outstanding off-leg return ([[SFT]] [[ID]] A1) for 100 [[shares]] versus $1,000.
o [[Borrower]] has a DVP obligation for (100) [[shares]] vs $1,000 against [[NSCC]]
o Lender has an RVP obligation for 100 [[shares]] vs ($1,000) against [[NSCC]]
l [[Stock]] merger value on 100 [[shares]] vs. $1,000 for [[CUSIP]] 123456789 will become 30 [[shares]] versus $1,000 for
[[CUSIP]] 987654321.
l Cash in Lieu Value = $8.
l When processed, the Miscellaneous Journal entries appear as follows:
Received Delivered Debit Credit Miscellaneous 
Code
Deliverer 
([[Borrower]])
100
CU 
123456789
$1,000
(Original [[SFT]] 
Value)
51 Merger
Deliverer 
([[Borrower]])
30
CU 
987654321
$1,000
(Original [[SFT]] 
Value)
51 Merger
Deliverer 
([[Borrower]])
$8.00
(Cash-in- Lieu)
51 Merger
Total $1,008 $1,000
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $8 DB
[[SFT]] Clearing: General User Guide

---

## Page 42

5. General Operational Flow 42
Received Delivered Debit Credit Miscellaneous 
Code
Received Delivered Debit Credit Miscellaneous 
Code
Receiver (Lender) 
100
CU 
123456789
$1,000
(Original [[SFT]] 
Value)
51 Merger
Receiver (Lender) 30
CU 
987654321
$1,000
(Original [[SFT]] 
Value)
51 Merger
Receiver (Lender) $8.00
(Cash-in- Lieu)
51 Merger
Total $1,000 $1,008
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $8 CR 
[[SFT]] Clearing: General User Guide

---

## Page 43

5. General Operational Flow 43
6. Reverse Split
l There is an outstanding off-leg return ([[SFT]] [[ID]] A1) for 90 [[shares]] versus $1,000.
o [[Borrower]] has a DVP obligation for (90) [[shares]] versus $1,000 against [[NSCC]]
o Lender has an RVP obligation for 90 [[shares]] versus ($1,000) against [[NSCC]]
l Reverse split on 90 [[shares]] versus $1,000 for [[CUSIP]] 123456789 becomes 30 [[shares]] versus $1,000 for [[CUSIP]]
987654321.
l When processed, the Miscellaneous Journal entries appear as follows:
Received Delivered Debit Credit Miscellaneous 
Code
Deliverer 
([[Borrower]])
90
CU 
123456789
$1,000
(Original [[SFT]] 
Value)
54 Reverse Split
Deliverer 
([[Borrower]])
30
CU 
987654321
$1,000
(Original [[SFT]] 
Value)
54 Reverse Split
Total $1,000 $1,000
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $0
Received Delivered Debit Credit Miscellaneous 
Code
Receiver (Lender) 
90
CU 
123456789
$1,000
(Original [[SFT]] 
Value)
54 Reverse Split
Receiver (Lender) 30
CU 
987654321
$1,000
(Original [[SFT]] 
Value)
54 Reverse Split
Total $1,000 $1,000
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $0
[[SFT]] Clearing: General User Guide

---

## Page 44

5. General Operational Flow 44
7. Name Change
l There is an outstanding off-leg return ([[SFT]] [[ID]] A1) for 100 [[shares]] versus $1,000.
o [[Borrower]] has a DVP obligation for (100) [[shares]] versus $1,000 against [[NSCC]].
o Lender has an RVP obligation for 100 [[shares]] versus ($1,000) against [[NSCC]].
l Name change for 100 [[shares]] versus $1,000 for [[CUSIP]] 123456789 becomes 100 [[shares]] versus $1,000 for [[CUSIP]]
987654321.
l When processed, the miscellaneous entries appear as follows:
Received Delivered Debit Credit Miscellaneous 
Code
Deliverer 
([[Borrower]])
100
CU 
123456789
$1,000
(Original [[SFT]] 
Value)
30 Name Change
Deliverer 
([[Borrower]])
100
CU 
987654321
$1,000
(Original [[SFT]] 
Value)
30 Name Change
Total $1,000 $1,000
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $0
Received Delivered Debit Credit Miscellaneous 
Code
Receiver (Lender) 
100
CU 
123456789
$1,000
(Original [[SFT]] 
Value)
30 Name Change
Receiver (Lender) 100
CU 
987654321
$1,000
(Original [[SFT]] 
Value)
30 Name Change
Total $1,000 $1,000
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $0
[[SFT]] Clearing: General User Guide

---

## Page 45

5. General Operational Flow 45
8. Cash & [[Stock]] Merger
l There is an outstanding off-leg return ([[SFT]] [[ID]] A1) for 100 [[shares]] versus $1,000.
o [[Borrower]] has a DVP obligation for (100) [[shares]] versus $1,000 against [[NSCC]]
o Lender has an RVP obligation for 100 [[shares]] versus ($1,000) against [[NSCC]]
l Cash and [[Stock]] merger for 100 [[shares]] versus $1,000 for [[CUSIP]] 123456789 pays as follows:
o Cash Merger Value: $600
o New Obligation: [[SFT]] [[ID]] A1 30 versus $1,000 [[CUSIP]] 987654321
o Cash-in Lieu Value = $12
l When processed, the miscellaneous entries appear as follows:
Received Delivered Debit Credit Miscellaneous 
Code
Deliverer 
([[Borrower]])
100
CU 
123456789
$600
(Cash Merger 
Value)
$1,000
(Original [[SFT]] 
Value)
51 Merger
Deliverer 
([[Borrower]])
30
CU 
987654321
$1,000
(Original [[SFT]] 
Value)
51 Merger
Deliverer 
([[Borrower]])
$12
(Cash-in- Lieu)
51 Merger
Total $1,612 $1,000
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $612 DB
Received Delivered Debit Credit Miscellaneous 
Code
Receiver (Lender) 100
CU 
123456789
$1,000
(Original [[SFT]] 
Value)
$600
(Cash Merger 
Value)
51 Merger
Receiver (Lender) 30
CU 
987654321
$1,000
(Original [[SFT]] 
Value)
51 Merger
Receiver (Lender) $12
(Cash-in- Lieu
51 Merger
Total $1,000 $1,612
Net [[NSCC]] Fed Funds [[settlement]] Code 132 = $612 CR
[[SFT]] Clearing: General User Guide

---

## Page 46

5. General Operational Flow 46
5.8 Additional Reference IDs on [[SFT]] Submission to UTC
The [[SFT]] Clearing service offers the capability to an Approved [[SFT]] Submitter to populate their own reference [[ID]], 
reference IDs of the counterparties, or both on their submission of an [[SFT]] to UTC. This information is passed to the 
SAS system and included on the SFTs processed at [[DTC]] in the ATP comments field. It is also included in the output 
distributed by both [[DTC]] and [[NSCC]]. The primary fields that should be used in UTC are as follows:
l Execution [[ID]] field (Tag 66) – This would be for the Approved [[SFT]] Submitter’s unique reference [[ID]]
l Buy Client Order [[ID]] (Tag 11) - This would be for the original [[Borrower]]’s unique reference [[ID]]
l Sell Client Order [[ID]] (Tag 11) - This would be for the original lender’s unique reference [[ID]]
Note
Although UTC allows for 32 bytes on the submission of these tags, only the first 16 bytes is reported and displayed in 
downstream systems and reported on the [[DTC]] and [[NSCC]] output.
5.8.1 Execution [[ID]] Field (Tag 66) and its use in Cancel Messages
The Execution [[ID]] field - Tag 66 has been reserved on UTC input to allow the Approved [[SFT]] Submitter to populate their 
unique internal reference [[ID]] (or Vendor [[ID]]) for a submitted [[SFT]]. Although it is an optional field for UTC input, it is 
recommended that the Approved [[SFT]] Submitter populate this Execution [[ID]] field - Tag 66 with a unique value for each 
New [[SFT]], Roll, and Send-to-Settle message. For a Cancel message, the Approved [[SFT]] Submitter should populate 
Execution [[ID]] field - Tag 66 with the previous submitted value in that field populated on the New [[SFT]], Roll, or Send-to-
Settle message.
The Execution [[ID]] field - Tag 66 is used by [[DTCC]] in the [[SFT]] Clearing service process flow as follows:
1. The value of the Execution [[ID]] field – Tag 66 (if populated) on UTC submission of a New [[SFT]], Roll, and Send-to-
Settle message is passed from UTC to the SAS system. The SAS system populates this value on the [[DO]] and PD
transactions that are sent to [[DTC]]. It is populated in the Comments section of the [[DTC]] transaction in field 19 - 36 as
follows:
l Field 19 and 20 = EX
Field 21 through 36 = will contain the Execution [[ID]] field – Tag 66 value (if populated in the UTC submission
record)
This value is also reported on all associated [[DTC]] and SAS output except when the Lender submits the on-leg push 
[[DO]] to [[DTC]]. Since this [[DO]] transaction is not being passed to [[DTC]] by the SAS system, it is up to the Lender to 
populate that Buy Execution Field -Tag 66 value in that specific field of the Comments when submitting their [[DTC]] 
[[DO]] transaction. The SAS system does not validate this field on Lender submission. The suggested [[DO]] submission 
by the Lender for an on-leg push [[DO]] to [[DTC]] should be: SFTXXXXXXXXXXXXXX_EXQQQQQQQQQQQQQQQQ 
l X = 14 Digit [[DTCC]] Reference [[ID]]
l Q = Up to 16 Digit Execution [[ID]] -Tag 66 value
l _ = Space
2. Value of the Execution [[ID]] field – Tag 66 (if populated) on the UTC submission of a Cancel message is used by
[[DTCC]] in the [[SFT]] process flow as follows:
[[SFT]] Clearing: General User Guide

---

## Page 47

5. General Operational Flow 47
l If to cancel an on-leg pending [[DO]] at [[DTC]] from a previously submitted New [[SFT]],
o In addition to [[DTCC]] Reference [[ID]] and quantity, the SAS system verifies that the value submitted in the
Execution Field - Tag 66 field on the Cancel message is the same value that was submitted on the New
[[SFT]] message. Otherwise, the Cancel message is not processed by the SAS system and is rejected.
Note
The reject is NOT processed by the UTC application upon submission. It is rejected by and then reported 
from the SAS system.
l If to cancel an on-leg pending PD at [[DTC]] from a previously submitted Roll,
o In addition to [[DTCC]] Reference [[ID]] and quantity, the SAS system verifies that the value submitted in the
Execution Field - Tag 66 field on the Cancel message is the same value that was submitted on the Roll
message. Otherwise, the Cancel message is not processed by the SAS system and is rejected.
Note
The reject is NOT processed by the UTC application upon submission. It is rejected by and then reported 
from the SAS system.
l If to cancel an on-leg pending [[DO]] at [[DTC]] from a previously submitted Send-to-Settle message,
o Additionally, if [[DTCC]] receives multiple to Send-to-Settle messages with the same Execution Field - Tag 66
field (and the same share quantity) and the DOs are pending at [[DTC]] and a Cancel message is received
with that same Execution Field - Tag 66 value, SAS will attempt to cancel oldest Send-to-Settle or pending
[[DO]] first. This same process would apply if there is no Execution Field - Tag 66 value submitted on the
Send-to-Settle messages and no Execution Field - Tag 66 value submitted in the Cancel message
5.8.2 Buy Client Order [[ID]] (Tag 11) and Sell Client Order [[ID]] (Tag 11)
The Buy Client Order [[ID]] – Tag 11 and Sell Client Order [[ID]] – Tag 11 have been reserved on UTC input to allow the 
Approved [[SFT]] Submitter to populate the unique internal reference [[ID]] of the respective [[Buyer]] ([[Borrower]]) or [[Seller]] 
(lender) for the submitted [[SFT]]. These fields are optional and are not used by [[DTCC]] in the [[SFT]] process flow. However, 
if populated, they are reported on the [[DO]] and PD transactions that are sent to [[DTC]] in the Comments section as follows 
based upon their role as receiver or deliverer in the processing of that transaction at [[DTC]].
l Field 38 and 39 = RC (Receiving Counterparty)
l Field 40 through 55 = Contain the Client Order [[ID]] field of the receiver of the transaction at [[DTC]].
l For a Price Differential, the receiver will be the payee (or counterparting getting the cash credit).
l Field 57 and 58 = DC (Delivering Counterparty)
l Field 59 through 74 = Contain the Client Order [[ID]] field of the deliverer of the transaction at [[DTC]].
l For a Price Differential, the deliverer is the payor (or counterparty getting the cash debit).
This value is also reported on all associated [[DTC]] and SAS output, except when the Lender submits the on-leg push 
[[DO]] to [[DTC]]. Since this [[DO]] transaction is not being passed to [[DTC]] by the SAS system, it is up to the Lender to populate 
those values in that specific field of the Comments section when submitting their [[DTC]] [[DO]] transaction.
[[SFT]] Clearing: General User Guide

---

## Page 48

5. General Operational Flow 48
5.9 [[Broker]] Reorg
The SAS system can automatically address situations where a [[Member]] moves an [[SFT]] from one [[SFT]] account to 
another due to a merger or other reasons.  All [[obligations]] in an OPEN status in the decommissioned number are closed 
and a new matched [[SFT]] is opened in the new [[SFT]] account number. The [[DTCC]] Reference [[ID]] is retained from the 
previous obligation to the new one.
The [[Broker]] Reorg takes place prior to opening the [[SFT]] Clearing service for a new business day.
5.10 [[SFT]] Tax Implications on Participating Entities
[[NSCC]] Members that participate in the [[SFT]] Clearing service are subject to pertinent U.S. tax laws, including but not 
limited to, U.S. federal tax withholding taxes and reporting requirements. These are generally imposed on all payments 
that are treated as U.S. sourced payments under the U.S. Tax Code and U.S. Treasury Regulations.  For example, 
certain credits processed in SAS on behalf of participating Members and the interest earned on the clearing funds 
deposited with the [[NSCC]] may be subject to withholding, reporting, or both.
5.11 Sponsoring and Sponsored [[Member]] Process
A Sponsoring [[Member]] may enter into a back-to-back trade when they are taking on a principal lending or principal 
borrowing relationship with a Sponsored [[Member]].  The back-to-back trade has [[NSCC]] in the middle of all [[obligations]] 
and as such, [[NSCC]] is the central counterparty to all part of the transaction.  The following table explains further:
Lender [[Borrower]]
Sponsored [[Member]] [[NSCC]]
[[NSCC]] Sponsoring [[Member]]
Sponsoring [[Member]] [[NSCC]]
[[NSCC]] Dealer
Sponsoring Members are expected to submit activity for the sponsored accounts. They are an Approved [[SFT]] 
Submitter for those accounts. Alternatively, the Sponsoring [[Member]] can choose to allow any other matching platform 
to submit in their Sponsored activity on their behalf.  Sponsored [[Member]] activity is always viewed and risk managed 
without offset against other Sponsored Members.  Because the Sponsored [[Member]] activity is essentially a record 
keeping entry on the Sponsoring [[Member]]’s accounts, [[NSCC]] does not need to process any [[securities]] movement on 
this activity.
SFTs between the Sponsoring [[Member]] and its Sponsored Members can be submitted to UTC throughout the 
processing day until 3:00 P.M. ET. Upon receipt and acceptance of a buy-side transaction, UTC provides a real time 
confirmation message back to the Sponsoring [[Member]] to inform them the on-leg message transaction was accepted. 
Since there are no security movements that need to occur at [[DTC]] for on-leg [[settlement]], at 3:00 P.M. ET, the cutoff 
time for buy-side transactions, UTC:
l Creates a pending off-leg return transaction message for each on-leg message received throughout the day and
send them to the [[NSCC]] risk system where the off-leg transaction begins to be margined.
l Sends the pending off-leg return messages maturing the next business day to the Sponsoring [[Member]].
These pending off-leg message shall constitute [[Novation]] of the off-leg of such buy-side transaction to [[NSCC]].
[[SFT]] Clearing: General User Guide

---

## Page 49

5. General Operational Flow 49
l Sends a global message to both the risk margining system and to the Sponsoring [[Member]] to inform them that their
maturing off-leg returns from the previous business day’s [[settlement]] of the on-leg has been released from [[NSCC]]’s
guaranty obligation.
Note
See Section 5.6 Corporate Actions Processing regarding submitting a Sponsoring [[Member]] trade with Sponsors (or 
buy-side loan) when a security is undergoing a forward [[Stock]] split and other corporate actions.
5.12 End of Day Activity Files
The SAS system creates and distributes the following MRO files at the end of the day:
l [[EOD]] [[mark-to-market]] MRO
l Outstanding Loans at [[EOD]]
5.12.1 [[EOD]] [[mark-to-market]] MRO
l Distributed immediately after the Drops occur in [[DTC]].
l Firms can use this to balance their net debit/credit of marks for Price Differential and [[DO]] off-leg returns (not rolled)
that did not settle at [[DTC]] where [[NSCC]] had to process a [[mark-to-market]] on the unsettled transaction. These marks
will be applied to a firm’s Fed Funds [[settlement]] (FFS) code 131 balance ([[SFT]] Marks) on their [[NSCC]] [[participant]]
Account statement.
l See End of Day ([[EOD]]) [[mark-to-market]] MRO AutoRoute [[ID]]: Production 02043623 / PSE 02983623.
5.12.2 Outstanding Loans at [[EOD]]
l Distributed at approximately 5:45 P.M. Eastern Time.
l Firms can use this to determine their open SFTs and also balance to their net debit/credit of overnight rebate interest
that will be applied the next business day to their Fed Funds [[settlement]] (FFS) code 130 balance (Rebate Interest)
on their [[NSCC]] [[participant]] Account statement.
l See Outstanding Loan MRO AutoRoute [[ID]]: Production 02043624 / PSE 02983624.
5.13 Closures
The following table shows the closures:
Closure Description
5.13.1 Bank holiday No [[settlement]] occurs for [[SFT]] activity and no new SFTs or Roll messages are accepted by UTC. 
New SFTs/Rolls processed on the day before a bank holiday expire on the business day after that 
bank holiday.
5.13.2 Good Friday No [[settlement]] occurs for [[SFT]] activity and no new SFTs or Roll messages are accepted by UTC. 
New SFTs/Rolls processed on the day before Good Friday  expire on the business day after Good 
Friday.
5.13.3 Unexpected 
Close
No [[settlement]] occurs for [[SFT]] activity and no new SFTs or Roll messages are accepted by UTC.  
New SFTs/Rolls processed on the day before an unexpected closure expire on the business day 
after the unexpected closure.
[[SFT]] Clearing: General User Guide

---

## Page 50

5. General Operational Flow 50
5.14 [[settlement]] Reason Codes
The following table shows the new reason codes for Deliver Order ([[DO]]) and Price Differential (PD) charges that are 
used for [[SFT]] processing:
Reason Code Activity Code 
[[DO]] - On-leg 200 26-20
[[DO]] - Off-leg 201 26-21
PD 800 78-05
5.15 [[SFT]] Money [[settlement]] Codes on the [[NSCC]] [[participant]] Account 
Statement
For [[SFT]], the following [[NSCC]] Money [[settlement]] codes are used for debit/credit cash as a result of transaction 
processing:
Code Description
5.15.1 FFS Money [[settlement]] Code 130 – 
[[SFT]] Rebate Interest (Rate) on the [[NSCC]] 
[[participant]] Account Statement
l Rate calculated by SAS for each [[SFT]] (or off-leg return) that remains open
when SAS changes its calendar for next business day processing.
l Each firm has either a net debit, credit, or no balance.
l Each firm can reconcile what comprises their net rate amount by
consuming the Outstanding Loans [[EOD]] MRO file that SAS distributes
earlier (around 5:45 P.M. ET). Each open [[SFT]] for a [[Member]] is in that file
and has the calculated rate amount for that specific [[SFT]] [[DTCC]] Reference
[[ID]].
5.15.2 FFS Money [[settlement]] Code 131 – 
[[SFT]] [[EOD]] [[mark-to-market]] on the [[NSCC]] 
[[participant]] Account Statement
l For those off-leg SFTs where either the off-leg return was not rolled (or
rolled but the PD did not settle) and SAS has to calculate the mark when
the [[DTC]] Drop cutoff time is reached.
l SAS sends one file to [[DTC]] approximately 3:30 P.M. ET (or 15 minutes after
Drops if there are extensions) with the net amount of each firm’s [[EOD]]
Mark-to Market transactions from non-return fails and price differentials
that did not settle at [[DTC]]. Each firm has either a net debit, credit, or no
balance.
l Each firm can reconcile what comprises their [[EOD]] Mark-to Market balance
by consuming the [[EOD]] [[mark-to-market]] that SAS distributes at
approximately 3:30 P.M. ET (or approximately 15 minutes after Drops if
there are extensions). Each [[SFT]] that was not returned that was marked by
[[NSCC]] for a [[Member]] is in that file.
[[SFT]] Clearing: General User Guide

---

## Page 51

5. General Operational Flow 51
Code Description
5.15.3 FFS Money [[settlement]] Code 132 – 
Buy-In Exit & Reorg on the [[NSCC]] 
[[participant]] Account Statement
l For cash processed on miscellaneous journal entries from buy-in
executions, corporate actions that were processed, such as cash mergers,
and marks on exits and [[SFT]] terminations.
l Existing Miscellaneous files will be leveraged (Sub-Account T). There are
two files sent to Members. This would be the same time as the existing
miscellaneous files are distributed today (1 - Night Miscellaneous – 12:30
A.M. ET after the night cycle and 2-Day Miscellaneous – 3:30 P.M. ET after
the Day Cycle). The balances in the two  files should equal the net amount
of each firm’s  miscellaneous activity and what is reported on the [[NSCC]]
[[participant]] [[settlement]] Statement for this FFS Code 132.
l Each firm has either a net debit, credit, or no balance.
l Each firm can reconcile what comprises their balance by using these
Miscellaneous files.
5.15.4 FFS Money [[settlement]] Code 133 – 
Cash Dividends on the [[NSCC]] [[participant]] 
Account Statement
l For cash dividends paid by SAS for open [[SFT]] positions on record date or
due bill redemption date.
l Each firm can reconcile what comprises their cash dividends balance by
consuming the SAS [[Dividend]] files. For the  [[SFT]] Clearing service, this is
Sub-Account T.
[[SFT]] Clearing: General User Guide

---

## Page 52

6. Messaging Flows 52
6. MESSAGING FLOWS
[[DTCC]] will support near real-time communication that updates interested parties of the status of an [[SFT]].  [[DTCC]] will 
operate under the following set of message distribution rules:
l For all output distributed from [[NSCC]], the output is distributed under their [[SFT]] Clearing [[Member]] Account.
l After an [[SFT]] message introducing an [[SFT]] is entered into the [[SFT]] Clearing service by an Approved [[SFT]] Submitter,
all subsequent input-into-[[DTCC]] messages are to come from that same entity, until the [[SFT]] is returned, exited, or
terminated (or whatever action ends the life of that [[SFT]]).
l Members can elect to receive output messages directly, authorize an Approved [[SFT]] Submitter to receive their
message output, or both.
l Members can allow their output messages to be submitted to a service provider.
l Approved [[SFT]] Submitters must subscribe and be approved to accept/reject output messages when they subscribe
to the service.
For format information about UTC messages and an inventory of all message output messages from the SAS and [[DTC]] 
types, see Message Layouts.
6.1 New [[SFT]]/On-leg Made
A new [[SFT]] on-leg instruction is submitted and accepted. The on-leg settles at [[DTC]]. [[NSCC]] set-ups up the off-leg with 
the scheduled return for the next business day.
On-leg or Off-leg What 
Occurred
Status When ISO 
Message 
Type
New Loan
1 On-leg New loan MADE On-leg Deliver Order ([[DO]])  settled at [[DTC]].
[[SFT]] Transaction Type: NEWL – New Loan
MT548
2 On-leg
Off-leg Setup (SD next 
business day)
New loan PEND On-leg Deliver Order ([[DO]])  settled at [[DTC]]. Off-leg set 
up. (Occurs after 1 is MADE).
[[SFT]] Transaction Type: NEWL – New Loan
MT548
Table 6.1  New [[SFT]]/On-leg Made
1. UTC receives a New Loan message. (UTC message type=N).
2. UTC sends a validated and accepted message back to the client.
3. SAS holds the SFTs in the database awaiting the lender to submit a valid [[DO]] instruction to [[DTC]].
4. The Lender submits a valid [[DO]] to [[DTC]] to deliver [[shares]] from the Lender's account to the [[NSCC]] [[SFT]] account (881)
versus  the [[settlement]] Amount for that Reference [[ID]] using the [[SFT]] [[DO]] reason code 200.
5. SAS sends the [[DO]] to [[DTC]] from the 881 account to the [[Borrower]]'s account for the same quantity and [[settlement]]
amount using the [[SFT]] [[DO]] reason code 200.
6. The [[SFT]] and [[DO]] are MADE at [[DTC]].
7. SAS notifies both the [[Borrower]] and lender of the MADE status. See row 1 in Table 6.1.
[[SFT]] Clearing: General User Guide

---

## Page 53

6. Messaging Flows 53
8. SAS sets up and sends out messaging with new off-leg details which is a PEND status for next business day
[[settlement]]. See row 2 in Table 6.1.
[[SFT]] Clearing: General User Guide

---

## Page 54

6. Messaging Flows 54
6.2 New [[SFT]]/On-leg Dropped
A new [[SFT]] on-leg instruction is submitted and accepted. The on-leg does not settle at [[DTC]] by the end of day DROP 
process. There is no off-leg return set-up by [[NSCC]].
On-leg or Off-leg What Occurred Status When ISO Message Type
New Loan
3 On-leg New loan DROP On-leg [[DO]] did not settled at [[DTC]].
[[SFT]] Transaction Type: NEWL – New Loan
MT548
Table 6.2  New [[SFT]]/On-leg Dropped
6.2.1 Scenario 1
1. UTC receives a New Loan message. (UTC message type=N).
2. UTC sends a validated and accepted message back to the client.
3. SAS holds the SFTs in the database awaiting the lender to submit a valid [[DO]] instruction to [[DTC]].
4. The Lender submits a valid [[DO]] to [[DTC]] to deliver [[shares]] from the Lender's account to the [[NSCC]] [[SFT]] account (881)
versus  the [[settlement]] Amount for that Reference [[ID]] using the [[SFT]] [[DO]] reason code 200.
5. SAS sends the [[DO]] to [[DTC]] from the 881 account to the [[Borrower]]'s account for the same quantity and [[settlement]]
amount using the [[SFT]] [[DO]] reason code 200.
6. The [[SFT]] and [[DO]] are dropped at [[DTC]].
7. SAS notifies both the [[Borrower]] and lender of the DROP status. See row 3 in Table 6.2.
[[SFT]] Clearing: General User Guide

---

## Page 55

6. Messaging Flows 55
- or -
6.2.2 Scenario 2
1. UTC receives a New Loan message. (UTC message type=N).
2. UTC sends a validated and accepted message back to the client.
3. SAS holds the SFTs in the database awaiting the lender to submit a valid [[DO]] instruction to [[DTC]].
4. The Lender never submits a valid [[DO]] instruction to [[DTC]].
5. [[SFT]] and [[DO]] are dropped from the SAS database.
6. SAS notifies both the [[Borrower]] and lender of the DROP status. See row 3 in Table 6.2.
[[SFT]] Clearing: General User Guide

---

## Page 56

6. Messaging Flows 56
[[SFT]] Clearing: General User Guide

---

## Page 57

6. Messaging Flows 57
6.3 New [[SFT]]/On-leg Canceled
A new [[SFT]] on-leg instruction is submitted and accepted. The on-leg has not settled yet at [[DTC]]. A cancel message is 
submitted and accepted. [[NSCC]] cancels the on-leg [[DO]] instruction at [[DTC]].
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
New Loan
4 On-leg Cancel (Against a 
New Loan)
Cancel message 
was submitted.
CANC On-leg [[DO]] was Pending at [[DTC]] and canceled 
through receipt of the Cancel message.
[[SFT]] Transaction Type: NEWL – New Loan
MT548
Table 6.3  New [[SFT]]/On-leg Canceled
6.3.1 Scenario 1
1. UTC receives a New Loan message. (UTC message type=N).
2. UTC sends a validated and accepted message back to the client.
3. SAS holds the SFTs in the database awaiting the lender to submit a valid [[DO]] instruction to [[DTC]].
4. The Lender submits a valid [[DO]] to [[DTC]] to deliver [[shares]] from the Lender's account to the [[NSCC]] [[SFT]] account (881)
versus the [[settlement]] Amount for that Reference [[ID]] using the new [[SFT]] [[DO]] reason code 200.
5. SAS sends the [[DO]] to [[DTC]] from the 881 account to the [[Borrower]]'s account for the same quantity and [[settlement]]
amount using the [[SFT]] [[DO]] reason code 200.
6. [[SFT]] and [[DO]] are in the PEND status at [[DTC]].
7. UTC receives a Cancel message. (UTC message type=C).
8. UTC sends a validated and accepted message back to the client.
9. SAS cancels the [[SFT]] and DOs that are in the PEND status at [[DTC]].
10. SAS notifies both the [[Borrower]] and Lender of the CANC – Canceled status. See row 4 in Table 6.3.
[[SFT]] Clearing: General User Guide

---

## Page 58

6. Messaging Flows 58
- or -
[[SFT]] Clearing: General User Guide

---

## Page 59

6. Messaging Flows 59
6.3.2 Scenario 2
1. UTC receives a New Loan message. (UTC message type=N).
2. UTC sends a validated and accepted message back to the client.
3. SAS holds the SFTs in the database awaiting the Lender to submit a valid [[DO]] instruction to [[DTC]].
4. UTC receives a Cancel message from the marketplace. (Marketplace =200).
5. UTC sends a validated and accepted message back to the client.
6. SAS cancels the [[SFT]] in its database.
7. SAS notifies both the [[Borrower]] and Lender of the CANC – Canceled  status to inform them that the new [[SFT]] was
canceled. See row 4 in Table 6.3.
[[SFT]] Clearing: General User Guide

---

## Page 60

6. Messaging Flows 60
6.4 Pre-established Bilateral [[SFT]]/On-leg Made
An outstanding [[SFT]] between two counterparties already settled bilaterally. The counterparties want to move the 
bilateral [[SFT]] to a cleared model. A Pre-established Bilateral Loan message is submitted and accepted. [[NSCC]] set-ups 
up the off-leg with the scheduled return for the next business day.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Pre-established Bilateral Loan
5 On-leg New Loan 
(Pre-established 
Bilateral Loan)
—
(No 
message 
sent)
Upon receipt and acceptance of the message 
from UTC. No [[DO]] on-leg occurs at [[DTC]].
[[SFT]] Transaction Type: None
N/A
6 Off-leg Setup 
([[settlement]] date 
next business day)
New Loan 
(Pre-established 
Bilateral Loan)
PEND Upon receipt and acceptance of the message 
from UTC. The off-leg is set up. 
[[SFT]] Transaction Type: NEWS – Pre-established 
Bilateral Loan
MT548
Table 6.4  Pre-established Bilateral [[SFT]]/On-leg Made
1. UTC receives a Pre-established Bilateral Loan message. (UTC message type=A).
2. UTC sends a validated and accepted message back to the client.
3. There are no on-leg DOs that settle at [[DTC]]. See row 5 in Table 6.4.
4. SAS sets up and sends messaging with new off-leg details, which is a PEND status for the next business day
[[settlement]]. See row 6 in Table 6.4.
[[SFT]] Clearing: General User Guide

---

## Page 61

6. Messaging Flows 61
6.5 Roll/On-leg Made
An off-leg is set to return on the current business day. The original counterparties want to extend the [[SFT]] for an 
additional business day. A Roll message is submitted and accepted for the full amount of [[shares]]. [[NSCC]] bilaterally nets 
the transactions and calculates the price differential. The price differential is sent to [[DTC]] and settles. [[NSCC]] updates 
the original off-leg return as settled and sets up the new off-leg (from roll) with the scheduled return for the next 
business day.
On-leg or Off-leg What 
Occurred
Status When ISO 
Message 
Type
Roll
7 On-leg Roll 
(Full or 
Partial)
MADE Price Differential (PD) settled at [[DTC]] between the 
roll (on-leg) and returning off-leg.
[[SFT]] Transaction Type: ROLL
MT548
8 Off-leg Setup From Roll
([[settlement]] date next 
business day)
Roll 
(Full or 
Partial)
PEND On-leg PD settled at [[DTC]]. Off-leg is setup (occurs 
after 7 is MADE).
[[SFT]] Transaction Type: ROLL
MT548
9 Off-leg 
(Original [[settlement]] date 
return is the current 
business day)
Roll 
(Full or 
Partial)
MADE PD settled at [[DTC]] so the off-leg return of [[shares]] 
that were bilaterally netted also settles. (Occurs 
simultaneously with 7).
[[SFT]] Transaction Type: ROLL
MT547/545
Table 6.5  Roll/On-leg Made
1. UTC receives a Roll message. (UTC message type=R).
2. UTC sends a validated and accepted message back to the client.
3. SAS calculates the Price Differential (PD) and sends to [[DTC]] using [[SFT]] PD reason code 800.
4. [[SFT]] and PD are MADE at [[DTC]].
5. SAS notifies both the [[Borrower]] and lender of the MADE status of the new loan created from the roll. See row 7 in
Table 6.5.
6. SAS notifies both the [[Borrower]] and lender of the MADE status of the original off-leg return. See row 9 in Table 6.5.
7. SAS sets up and sends messaging with the new off-leg details, which is a PEND status for the next business day
[[settlement]]. See row 8 in Table 6.5.
[[SFT]] Clearing: General User Guide

---

## Page 62

6. Messaging Flows 62
[[SFT]] Clearing: General User Guide

---

## Page 63

6. Messaging Flows 63
6.6 Roll/On-leg Dropped
An off-leg is set to return on the current business day. The original counterparties want to extend the [[SFT]] for an 
additional business day. A Roll message is submitted and accepted for the full amount of [[shares]]. [[NSCC]] bilaterally nets 
the transactions and calculates the price differential. The price differential is sent to [[DTC]] and does not settle by the end 
of day DROP process. The original off-leg remains open and there is no new off-leg return (for the roll) set-up by 
[[NSCC]].
On-leg or Off-leg What 
Occurred
Status When ISO 
Message 
Type
Roll
10 On-leg Roll 
(Full or 
Partial)
DROP Price Differential (PD) did not settle at [[DTC]] 
between the roll (on-leg) and returning off-leg.
[[SFT]] Transaction Type: ROLL
MT548
11 Off-leg 
(Original [[settlement]] date 
return is the current 
business day)
Roll 
(Full or 
Partial)
NRET PD dropped at [[DTC]] so the off-leg return of [[shares]] 
that were bilaterally netted also did not settle. 
(Occurs simultaneously with 10). 
[[SFT]] Transaction Type: ROLL
MT548
Table 6.6  Roll/On-leg Dropped
1. UTC receives a Roll message. (UTC message type=R).
2. UTC sends a validated and accepted message back to the client.
3. SAS calculates the Price Differential (PD) and sends to [[DTC]] using [[SFT]] PD reason code 800.
4. [[SFT]] and PD are dropped at [[DTC]].
5. SAS notifies both the [[Borrower]] and lender of the DROP – Dropped status of the new loan from the roll transaction.
See row 10 in Table 6.6.
6. SAS notifies both the [[Borrower]] and lender of the NRET – Non Return Fail status of the original off-leg return. See
row 11 in Table 6.6.
[[SFT]] Clearing: General User Guide

---

## Page 64

6. Messaging Flows 64
[[SFT]] Clearing: General User Guide

---

## Page 65

6. Messaging Flows 65
6.7 Roll/On-leg Canceled and Original Off-leg Made
An off-leg is set to return on the current business day. The original counterparties want to extend the [[SFT]] for an 
additional business day. A Roll message is submitted and accepted for the full amount of [[shares]]. [[NSCC]] bilaterally nets 
the transactions and calculates the price differential. The price differential is sent to [[DTC]] and has not settled yet. A 
cancel message is submitted and accepted. [[NSCC]] cancels the roll (by canceling the price differential) thus 
immediately prompting the original off-leg return of [[shares]] versus the original [[settlement]] value that is sent to [[DTC]] and 
settles.
On-leg or Off-leg What 
Occurred
Status When ISO 
Message 
Type
Roll
12 On-leg Cancel 
(Against a 
Full or 
Partial Roll)
Cancel 
message 
was 
submitted.
CANC Price Differential (PD) was pending at [[DTC]] and 
canceled through the receipt of the Cancel message.
[[SFT]] Transaction Type: ROLL
MT548
13 Off-leg 
(Original 
[[settlement]] date 
return is the current 
business day)
Cancel 
(Against a 
Full or 
Partial Roll)
Cancel 
message 
was 
submitted.
MADE PD from the roll on-leg was canceled resulting in the 
[[DO]] return of the off-leg [[shares]] (that were originally 
bilaterally netted), which settled at [[DTC]]. (Occurs 
after 12). 
[[SFT]] Transaction Type: NROL - No Roll
MT547/545
Table 6.7  Roll/On-leg Canceled and Original Off-leg Made
1. UTC receives a Roll message. (UTC message type=R).
2. UTC sends a validated and accepted message back to the client.
3. SAS calculates the Price Differential (PD) and sends to [[DTC]] using the [[SFT]] PD reason code 800.
4. Both PDs are in the PEND status at [[DTC]]
5. UTC receives a Cancel message. (UTC message type=C).
6. UTC sends a validated and accepted message back to the client.
7. SAS cancels both PDs that are in the PEND status at [[DTC]]
8. SAS notifies both the [[Borrower]] and lender of the CANC – Canceled  status of the new [[SFT]] from the roll transaction.
See row 12 in Table 6.7.
9. SAS sends [[DO]] instructions to [[DTC]] to immediately return the original off-leg using [[SFT]] reason code 201.
10. [[SFT]] and [[DO]] are MADE at [[DTC]].
11. SAS notifies both the [[Borrower]] and lender of the MADE status of the original off-leg return. See row 13 in Table 6.7.
[[SFT]] Clearing: General User Guide

---

## Page 66

6. Messaging Flows 66
[[SFT]] Clearing: General User Guide

---

## Page 67

6. Messaging Flows 67
6.8 Roll/On-leg Canceled and Original Off-leg Return Dropped
An off-leg is set to return on the current business day. The original counterparties want to extend the [[SFT]] for an 
additional business day. A Roll message is submitted and accepted for the full amount of [[shares]]. [[NSCC]] bilaterally nets 
the transactions and calculates the price differential. The price differential is sent to [[DTC]] and has not settled yet. A 
Cancel message is submitted and accepted. [[NSCC]] cancels the roll (by canceling the price differential) thus 
immediately prompting the original off-leg return of [[shares]] vs. original [[settlement]] value which is sent to [[DTC]] and does 
not settle by the end of day DROP process.
On-leg or Off-leg What 
Occurred
Status When ISO 
Message 
Type
Roll
12 On-leg Cancel 
(Against a Full 
or Partial Roll)
Cancel 
message was 
submitted.
CANC Price Differential (PD) was pending at [[DTC]] and 
canceled through the receipt of the Cancel 
message.
[[SFT]] Transaction Type: ROLL
MT548
14 Off-leg 
(Original [[settlement]] date 
return is the current 
business day)
Cancel 
(Against a Full 
or Partial Roll)
Cancel 
message was 
submitted.
NRET PD dropped at [[DTC]] so the off-leg return of 
[[shares]] that were bilaterally netted also did not 
settle. (Occurs after 12). 
[[SFT]] Transaction Type: NROL – No Roll
MT548
Table 6.8  Roll/On-leg Canceled and Original Off-leg Return Dropped
1. UTC receives a Roll message. (UTC message type=R).
2. UTC sends a validated and accepted message back to the client.
3. SAS calculates the Price Differential (PD) and sends to [[DTC]] using [[SFT]] PD reason code 800.
4. Both PDs are in the PEND status at [[DTC]]
5. UTC receives a Cancel message (UTC message type=C).
6. UTC sends a validated and accepted message back to the client.
7. SAS cancels both PDs that are in the PEND status at [[DTC]]
8. SAS notifies both the [[Borrower]] and lender of the CANC – Canceled  status of the new [[SFT]] from the roll transaction.
See row 12 in Table 6.7.
9. SAS sends [[DO]] instructions to [[DTC]] immediately to return the original off-leg using [[SFT]] reason code 201.
10. [[SFT]] and [[DO]] are dropped at [[DTC]]
11. SAS notifies both the [[Borrower]] and lender of the NRET – Non Return Fail status for the original off-leg return. See
row 14 in Table 6.7.
[[SFT]] Clearing: General User Guide

---

## Page 68

6. Messaging Flows 68
[[SFT]] Clearing: General User Guide

---

## Page 69

6. Messaging Flows 69
6.9 No Roll/Original Off-leg Return Made
An off-leg is set to return on the current business day. The original counterparties [[DO]] not submit a roll message. [[NSCC]] 
initiates the original off-leg return of [[shares]] versus the original [[settlement]] value, which is sent to [[DTC]] and settles.
On-leg or Off-leg What 
Occurred
Status When ISO Message 
Type
No Roll
15 Off-leg 
(Original [[settlement]] date return is the 
current business day)
No Roll MADE [[DO]] off-leg return settles at 
[[DTC]].
[[SFT]] Transaction Type: 
NROL – No Roll
MT547/545
Table 6.9  No Roll/Original Off-leg Return Made
1. SAS database has the original off-leg return for SFTs in the PEND status.
2. UTC receives the No Roll message by 11:30 A.M. Eastern Time.
3. SAS sends [[DO]] instructions to [[DTC]] to return the original off-leg using [[SFT]] reason code 201.
4. [[SFT]] and [[DO]] are MADE at [[DTC]].
5. SAS notifies both the [[Borrower]] and lender of the MADE status of the original off-leg return. See row 15 in Table 6.9
.
[[SFT]] Clearing: General User Guide

---

## Page 70

6. Messaging Flows 70
6.10 No Roll/Original Off-leg Return Dropped
An off-leg is set to returned on the current business day. The original counterparties [[DO]] not submit a roll message. 
[[NSCC]] initiates the original off-leg return of [[shares]] versus original [[settlement]] value, which is sent to [[DTC]] and does not 
settle by the end of day DROP process.
On-leg or Off-leg What 
Occurred
Status When ISO 
Message 
Type
No Roll
16 Off-leg 
(Original [[settlement]] date return is the 
current business day)
No Roll NRET [[DO]] off-leg return  did not settle 
(dropped) at [[DTC]].
[[SFT]] Transaction Type: NROL – 
No Roll
MT548
Table 6.10  No Roll/Off-leg Return Dropped
1. SAS database has the original off-leg return for SFTs in the PEND status.
2. UTC receives the o roll message by 11:30 A.M. Eastern Time.
3. SAS sends [[DO]] instructions to [[DTC]] to return the original off-leg using [[SFT]] reason code 201.
4. [[SFT]] and [[DO]] are dropped at [[DTC]].
5. SAS notifies both the [[Borrower]] and lender of the NRET – Non Return Fail status of the original off-leg return. See
row 16 in Table 6.10.
[[SFT]] Clearing: General User Guide

---

## Page 71

6. Messaging Flows 71
[[SFT]] Clearing: General User Guide

---

## Page 72

6. Messaging Flows 72
6.11 Partial Roll/On-leg Made and Remainder Off-leg Made
An off-leg is set to return on the current business day. The original counterparties want to extend the [[SFT]] for an 
additional business day. A Roll message is submitted and accepted for the partial amount of [[shares]]. For the rolled 
[[shares]], [[NSCC]] bilaterally nets the transactions and calculates the price differential. The price differential is sent to [[DTC]] 
and settles. [[NSCC]] updates the original off-leg return as settled and sets up the new off-leg (from roll) with the 
scheduled return for the next business day. For the remainder [[shares]] (not rolled), [[NSCC]] initiates the original off-leg 
return of [[shares]] versus calculated [[settlement]] value, which is sent to [[DTC]] and settles.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Roll
7 On-leg Roll 
(Full or Partial)
MADE Price Differential (PD) settled at [[DTC]] 
between the roll (on-leg) and returning 
off-leg.
[[SFT]] Transaction Type: ROLL
MT548
8 Off-leg Setup From 
Roll
([[settlement]] date 
next business day)
Roll 
(Full or Partial)
PEND On-leg PD settled at [[DTC]]. Off-leg is 
setup (occurs after 7 is MADE).
[[SFT]] Transaction Type: ROLL
MT548
9 Off-leg 
(Original 
[[settlement]] date 
return is the current 
business day)
Roll 
(Full or Partial)
MADE PD settled at [[DTC]] so the off-leg return 
of [[shares]] that were bilaterally netted 
also settles. (Occurs simultaneously 
with 7).
[[SFT]] Transaction Type: ROLL
MT547/545
No Roll
17 Off-leg 
(Original 
[[settlement]] date 
return is the current 
business day)
Remainder for a Partial 
Roll—Off-leg return [[shares]] 
that were not bilaterally 
netted.
MADE [[DO]] off-leg return settles at [[DTC]].
[[SFT]] Transaction Type: NROL – No 
Roll
MT547/545
Table 6.11  Partial Roll/On-leg Made and Remainder Off-leg Made
1. UTC receives a Roll message. (UTC message type=R).
The Roll is only for partial [[shares]].
2. UTC sends a validated and accepted message back to the client.
3. For the rolled portion of [[shares]], SAS calculates the Price Differential (PD) and sends to [[DTC]] using [[SFT]] PD reason
code 800.
4. For the remainder portion of [[shares]] ([[shares]] not rolled), SAS sends [[DO]] instructions to [[DTC]] to return the original
off-leg using [[SFT]] reason code 201.
[[SFT]] Clearing: General User Guide

---

## Page 73

6. Messaging Flows 73
5. For the rolled portion of [[shares]], both PDs are MADE at [[DTC]].
l SAS notifies both the [[Borrower]] and lender of the MADE status of the new [[SFT]] created from the roll. See row 7 in
Table 6.11.
l SAS notifies both the [[Borrower]] and lender of the MADE status of the original off-leg return. See row 9 in Table
6.11.
l SAS sets up and sends messaging with new off-leg details which is a PEND status for next business day
[[settlement]]. See row 8 in Table 6.11.
6. For the remainder portion of [[shares]] ([[shares]] not rolled), both DOs are MADE at [[DTC]].
l SAS notifies both the [[Borrower]] and lender of the MADE status of the original off-leg return. See row 17 in Table
6.11.
[[SFT]] Clearing: General User Guide

---

## Page 74

6. Messaging Flows 74
6.12 Partial Roll/On-leg Made and Remainder Off-leg Dropped
An off-leg is set to return on the current business day. The original counterparties want to extend the [[SFT]] for an 
additional business day. A Roll message is submitted and accepted for the partial amount of [[shares]]. For the rolled 
[[shares]], [[NSCC]] bilaterally nets the transactions and calculates the price differential. The price differential is sent to [[DTC]] 
and settles. [[NSCC]] updates the original off-leg return as settled and sets up the new off-leg (from roll) with the 
scheduled return for the next business day. For the remainder [[shares]] (not rolled), [[NSCC]] initiates the original off-leg 
return of [[shares]] versus the calculated [[settlement]] value, which is sent to [[DTC]] and does not settle by the end of day 
DROP process.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Roll
7 On-leg Roll 
(Full or Partial)
MADE Price Differential (PD) settled at [[DTC]] 
between the roll (on-leg) and returning 
off-leg.
[[SFT]] Transaction Type: ROLL
MT548
8 Off-leg Setup From 
Roll
([[settlement]] date 
next business day)
Roll 
(Full or Partial)
PEND On-leg PD settled at [[DTC]]. Off-leg is 
setup (occurs after 7 is MADE).
[[SFT]] Transaction Type: ROLL
MT548
9 Off-leg 
(Original 
[[settlement]] date 
return is the current 
business day)
Roll 
(Full or Partial)
MADE PD settled at [[DTC]] so the off-leg return 
of [[shares]] that were bilaterally netted 
also settles. (Occurs simultaneously 
with 7).
[[SFT]] Transaction Type: ROLL
MT547/545
No Roll
18 Off-leg 
(Original 
[[settlement]] date 
return is the current 
business day)
Remainder from a Partial 
Roll—Off-leg return [[shares]] 
that were not bilaterally 
netted.
NRET [[DO]] off-leg return did not settle 
(dropped) at [[DTC]].  
[[SFT]] Transaction Type: NROL – No 
Roll
MT548
Table 6.12  Partial Roll/On-leg Made and Remainder Off-leg Dropped
1. UTC receives a Roll message. (UTC message type=R).
l Roll is only for Partial [[shares]].
2. UTC sends a validated and accepted message back to the client.
3. For the rolled portion of [[shares]], SAS calculates the Price Differential (PD) and sends to [[DTC]] using [[SFT]] PD reason
code 800.
4. For the remainder portion of [[shares]] ([[shares]] not rolled), SAS sends [[DO]] instructions to [[DTC]] to return the original
off-leg using [[SFT]] reason code 201.
[[SFT]] Clearing: General User Guide

---

## Page 75

6. Messaging Flows 75
5. For the rolled portion of [[shares]], both PDs are MADE at [[DTC]].
l SAS notifies both the [[Borrower]] and lender of the MADE status of the new [[SFT]] created from the roll. See row 7 in
Table 6.12.
l SAS notifies both the [[Borrower]] and lender of the MADE status of the original off-leg return. See row 9  in Table
6.12.
l SAS sets up and sends messaging with new off-leg details which is a PEND status for next business day
[[settlement]]. See row 8  in Table 6.12.
6. For the remainder portion of [[shares]] ([[shares]] not rolled), both DOs are dropped at [[DTC]].
l SAS notifies both the [[Borrower]] and lender of the NRET – Non Return Fail status of the original off-leg return.
See row 18  in Table 6.12.
[[SFT]] Clearing: General User Guide

---

## Page 76

6. Messaging Flows 76
6.13 Partial Roll/On-leg Dropped and Remainder Off-leg Made
An off-leg is set to return on the current business day. The original counterparties want to extend the [[SFT]] for an 
additional business day. A Roll message is submitted and accepted for the partial amount of [[shares]]. For the rolled 
[[shares]], [[NSCC]] bilaterally nets the transactions and calculates the price differential. The price differential is sent to [[DTC]] 
and does not settle by the end of day DROP process. The original off-leg remains open and there is no new off-leg 
return (for the roll) set-up by [[NSCC]]. For the remainder [[shares]] (not rolled), [[NSCC]] initiates the original off-leg return of 
[[shares]] versus calculated [[settlement]] value, which is sent to [[DTC]] and settles.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Roll
10 On-leg Roll 
(Full or Partial)
DROP Price Differential (PD) did not settle  at 
[[DTC]] between the roll (on-leg) and 
returning off-leg.
[[SFT]] Transaction Type: ROLL
MT548
11 Off-leg 
(Original 
[[settlement]] date 
return is the current 
business day)
Roll 
(Full or Partial)
NRET PD dropped at [[DTC]] so the off-leg return 
of [[shares]] that were bilaterally netted 
also did not settle. (Occurs 
simultaneously with 10). 
[[SFT]] Transaction Type: ROLL
MT548
No Roll
17 Off-leg 
(Original 
[[settlement]] date 
return is the current 
business day)
Remainder for a Partial 
Roll—Off-leg return [[shares]] 
that were not bilaterally 
netted.
MADE [[DO]] off-leg return settles at [[DTC]].
[[SFT]] Transaction Type: NROL - No Roll
MT547/545
Table 6.13  Partial Roll/On-leg Dropped and Remainder Off-leg Made
1. UTC receives a Roll message. (UTC message type=R).
l Roll is only for Partial [[shares]].
2. UTC sends a validated and accepted message back to the client.
3. For the rolled portion of [[shares]], SAS calculates the Price Differential (PD) and sends to [[DTC]] using [[SFT]] PD reason
code 800.
4. For the remainder portion of [[shares]] ([[shares]] not rolled), SAS sends [[DO]] instructions to [[DTC]] to return the original
off-leg using [[SFT]] reason code 201.
5. [[SFT]] and PD are dropped at [[DTC]].
l SAS notifies both the [[Borrower]] and lender of the DROP status of the new [[SFT]] from the roll transaction. See row
10 in Table 6.13.
l SAS notifies both the [[Borrower]] and lender of the NRET – Non Return Fail status of the original off-leg return.
See row 11 in Table 6.13.
[[SFT]] Clearing: General User Guide

---

## Page 77

6. Messaging Flows 77
6. For the remainder portion of [[shares]] ([[shares]] not rolled), both DOs are MADE at [[DTC]].
l SAS notifies both the [[Borrower]] and lender of the MADE status of the original off-leg return. See row 17 in Table
6.13.
[[SFT]] Clearing: General User Guide

---

## Page 78

6. Messaging Flows 78
6.14 Partial Roll/On-leg Dropped and Remainder Off-leg Dropped
An off-leg is set to return on the current business day. The original counterparties want to extend the [[SFT]] for an 
additional business day. A Roll message is submitted and accepted for the partial amount of [[shares]]. For the rolled 
[[shares]], [[NSCC]] bilaterally nets the transactions and calculates the price differential.  The price differential is sent to [[DTC]] 
and does not settle by the end of day DROP process. For the remainder [[shares]] (not rolled), [[NSCC]] initiates the original 
off-leg return of [[shares]] versus calculated [[settlement]] value, which is sent to [[DTC]] and does not settle by the end of day 
DROP process.
On-leg or Off-leg What 
Occurred
Status When ISO 
Message 
Type
Roll
10 On-leg Roll 
(Full or 
Partial)
DROP Price Differential (PD) did not settle  at [[DTC]] 
between the roll (on-leg) and returning off-leg.
[[SFT]] Transaction Type: ROLL
MT548
11 Off-leg 
(Original [[settlement]] date 
return is the current 
business day)
Roll 
(Full or 
Partial)
NRET PD dropped at [[DTC]] so the off-leg return of [[shares]] 
that were bilaterally netted also did not settle. 
(Occurs simultaneously with 10). 
[[SFT]] Transaction Type: ROLL
MT548
Table 6.14  Partial Roll/On-leg Dropped and Remainder Off-leg Dropped
1. UTC receives a Roll message. (UTC message type=R).
The Roll is only for partial [[shares]].
2. UTC sends a validated and accepted message back to the client.
3. For the rolled portion of [[shares]], SAS calculates the Price Differential (PD) and sends to [[DTC]] using [[SFT]] PD reason
code 800.
4. For the remainder portion of the [[shares]] ([[shares]] not rolled), SAS sends [[DO]] instructions to [[DTC]] to return the original
off-leg using [[SFT]] reason code 201.
5. [[SFT]] and PD are dropped at [[DTC]].
l SAS notifies both the [[Borrower]] and lender of the DROP status of the new [[SFT]] from the roll transaction. See row
10 in Table 6.14.
6. For the remainder portion of [[shares]] ([[shares]] not rolled), both DOs are dropped at [[DTC]].
7. For the original off-leg return, where the [[shares]] rolled and remainder (portion of [[shares]] not rolled) both dropped,
SAS notifies both the [[Borrower]] and lender of the NRET – Non Return Fail status of the entire share amount of the
original off-leg return. See row 11 in Table 6.14.
[[SFT]] Clearing: General User Guide

---

## Page 79

6. Messaging Flows 79
[[SFT]] Clearing: General User Guide

---

## Page 80

6. Messaging Flows 80
6.15 No Roll on Term Date/Send-to-Settle Received and Original Off-leg 
Return Made
An off-leg is set to return on the current business day. Before 11:30 AM ET roll cutoff time, a Send-to-Settle message is 
received and accepted. [[NSCC]] immediately initiates the original off-leg return of [[shares]] versus original [[settlement]] 
value, which is sent to [[DTC]] and settles.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
No Roll
19 Off-leg 
(Original [[settlement]] date return 
is the current business day)
No Roll
(Send-to-Settle message 
received before 11:30 A.M.)
MADE [[DO]] off-leg return   settled 
at [[DTC]].
[[SFT]] Transaction Type: 
SNDS – Send-to-Settle
MT547/545
Table 6.15  No Roll on Term Date/Send-to-Settle Received and Original Off-leg Return Made
1. SAS database has the original off-leg return for [[SFT]] transactions in the PEND status.
2. UTC receives a Send-to-Settle message. (UTC message type=S).
3. UTC sends a validated and accepted message back to the client.
4. SAS sends [[DO]] instructions to [[DTC]] to return the original off-leg using [[SFT]] reason code 201.
5. [[SFT]] and [[DO]] are MADE at [[DTC]].
6. SAS notifies both the [[Borrower]] and lender of the MADE status of the original off-leg return. See row 19 in Table
6.15.
[[SFT]] Clearing: General User Guide

---

## Page 81

6. Messaging Flows 81
[[SFT]] Clearing: General User Guide

---

## Page 82

6. Messaging Flows 82
6.16 No Roll on Term Date/Send-to-Settle Received and Original Off-leg 
Return Dropped
An off-leg is set to return on the current business day. Before 11:30 A.M. ET roll cutoff time, a Send-to-Settle message 
is received and accepted. [[NSCC]] immediately initiates the original off-leg return of [[shares]] versus the original [[settlement]] 
value, which is sent to [[DTC]] and does not settle by the end of day DROP process
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
No Roll
20 Off-leg 
(Original [[settlement]] date return is 
the current business day)
No Roll
(Send-to-Settle message 
received before 11:30 A.M.)
NRET [[DO]] off-leg return 
dropped at [[DTC]]. 
[[SFT]] Transaction Type: 
SNDS– Send-to-Settle
MT548
Table 6.16  No Roll on Term Date/Send-to-Settle Received and Original Off-leg Return Dropped
1. The SAS system has the original off-leg return for [[SFT]] transactions in the PEND status.
2. UTC receives a Send-to-Settle message. (UTC message type=S).
3. UTC sends a validated and accepted message back to the client.
4. SAS sends [[DO]] instructions to [[DTC]] to return the original off-leg using [[SFT]] reason code 201.
5. [[SFT]] and [[DO]] are dropped at [[DTC]].
6. SAS notifies both the [[Borrower]] and lender of the NRET – Non Return Fail status of the original off-leg return. See
row 20 in Table 6.16.
[[SFT]] Clearing: General User Guide

---

## Page 83

6. Messaging Flows 83
6.17 Send-to-Settle (Accelerated Return From the Next Business Day to 
Current Business Day)/Off-leg Return Made
A new [[SFT]] or roll on-leg instruction is submitted and accepted. The on-leg settles at [[DTC]]. [[NSCC]] set-ups up the off-leg 
with the scheduled return for the next business day. A Send-to-Settle message is received and accepted to accelerate 
the return of [[shares]] from the next business day to the current business day. [[NSCC]] immediately accelerates the off-leg 
return of [[shares]] versus the [[settlement]] value, which is sent to [[DTC]] and settles.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Send-to-Settle
21 Off-leg 
([[settlement]] date 
next business day)
Send-to-Settle message results in an off-leg 
return accelerated from the next business day 
to the current business day.
Full or Partial
MADE [[DO]] off-leg return   
settled at [[DTC]].
(Occurs after 2, 6, or 
7).
[[SFT]] 
Transaction Type: 
SNDS –  
Send-to-Settle
MT547/545
Table 6.17  Send-to-Settle/Off-leg Return Made
[[SFT]] Clearing: General User Guide

---

## Page 84

6. Messaging Flows 84
1. The SAS system has the off-leg return for [[SFT]] transactions in the  PEND status set to return on the next business
day.
2. UTC receives a Send-to-Settle message. (UTC message type=S).
3. UTC sends a validated and accepted message back to the client.
4. SAS immediately sends [[DO]] instructions to [[DTC]] to return the original off-leg using [[SFT]] reason code 201.
5. [[SFT]] and [[DO]] are MADE at [[DTC]].
6. SAS notifies both the [[Borrower]] and lender of the MADE status of the accelerated off-leg return. See row 21 in
Table 6.17.
[[SFT]] Clearing: General User Guide

---

## Page 85

6. Messaging Flows 85
6.18 Send-to-Settle (Accelerated Return From the Next Business Day to 
Current Business Day)/Off-leg Return Dropped
A new [[SFT]] or roll on-leg instruction is submitted and accepted. The on-leg settles at [[DTC]]. [[NSCC]] sets up the off-leg 
with the scheduled return for the next business day. A Send-to-Settle message is received and accepted to accelerate 
the return of [[shares]] from the next business day to the current business day. [[NSCC]] immediately accelerates the off-leg 
return of [[shares]] versus the [[settlement]] value, which is sent to [[DTC]] and does not settle by the end of day DROP 
process.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Send-to-Settle
22 Off-leg 
([[settlement]] date 
next business day)
Send-to-Settle message results in the off-leg 
return accelerated from next.
Send-to-Settle message results in an off-leg return 
accelerated from the next business day to the 
current business day. 
Full or Partial
NRET [[DO]] off-leg return 
dropped at [[DTC]].
(Occurs after 2, 6, 
or 7).
[[SFT]] 
Transaction Type: 
SNDS –  
Send-to-Settle
MT548
Table 6.18  Send-to-Settle/Off-leg Return Dropped
1. SAS database has the off-leg return for [[SFT]] transactions in the PEND status set to return on the next business day.
2. UTC receives a Send-to-Settle message. (UTC message type=S).
3. UTC sends a validated and accepted message back to the client.
4. SAS immediately sends [[DO]] instructions to [[DTC]] to return the original off-leg using [[SFT]] reason code 201.
5. [[SFT]] and [[DO]] are dropped at [[DTC]].
6. SAS notifies both the [[Borrower]] and lender of the NRET – Non Return Fail status of the accelerated off-leg return.
See row 22 in Table 6.18.
[[SFT]] Clearing: General User Guide

---

## Page 86

6. Messaging Flows 86
[[SFT]] Clearing: General User Guide

---

## Page 87

6. Messaging Flows 87
6.19 Rate Modification
A rate modification message is submitted and accepted. [[NSCC]] applies the rate modification message to the [[DTCC]] 
Reference [[ID]] for that [[SFT]] only if an off-leg return remains outstanding after the end-of-day DROP process.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Rate Modification
23 Off-leg 
(Same day on-leg 
settled from either 
new loan, roll, or 
pre-established 
bilateral loan)
Rate modification received while 
the off-leg is set up and pending in 
the SAS system to be returned the 
next business day or SAS has 
received a Send-to-Settle to 
accelerate the off-leg return to the 
current business day. 
–
(Updated 
interest)
Send updated interest 
message after DROPS 
occurred at [[DTC]] and after 3:45 
P.M. Eastern Time (rate
modification cutoff time).
Note: SAS uses only the last 
rate modification message 
received. The Rate 
Modification message can be 
used to modify the rate or 
change the counterparty who 
[[NSCC]] should pay the 
overnight rebate interest to.
[[SFT]] Transaction Type: RMOD 
– Rate Modification
MT547/545
Table 6.19  Rate Modification
1. UTC receives a Rate Modification message. (UTC message type=M).
2. UTC sends a validated and accepted message back to the client.
3. SAS holds the Rate Modification message in the database until both:
l [[DTC]] DROPS occur at approximately 3:10 P.M. Eastern Time.
- and -
l Rate Modification cutoff time submission of 3:45 P.M. Eastern Time has been reached.
4. If there is an outstanding off-leg return in the SAS database for that [[DTC]] Reference [[ID]], SAS processes the rate
modification message for that [[DTC]] Reference [[ID]] using the most recent rate modification message received.
5. SAS notifies the [[Borrower]] and lender of updated interest (and/ or the change to the contra party getting paid the
rebate interest) as a result of processing the rate modification message. See row 23 in Table 6.19.
[[SFT]] Clearing: General User Guide

---

## Page 88

6. Messaging Flows 88
[[SFT]] Clearing: General User Guide

---

## Page 89

6. Messaging Flows 89
6.20 [[SFT]] Loan Termination
An [[SFT]] Loan Termination message is submitted and accepted. [[NSCC]] processes the [[SFT]] Loan Termination message 
and removes the outstanding off-leg return from the system.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
[[SFT]] Loan Termination
25 Off-leg [[SFT]] Loan Terminations can only be 
processed against an off-leg return at the 
following times during the course of a 
business day:
1) Until 11:30 A.M. EST (on the original
[[settlement]] date it was set to be returned) as
long as the off-leg return was not rolled or the
[[DO]] return was not sent to [[DTC]] for [[settlement]].
2) Anytime during the day (on the same day
the on-leg settled and the off-leg return is set
to be returned the next business day) provided
no Send-to-Settle message was received or if
a Send-to-Settle message was received, there
is no [[DO]] Pending at [[DTC]].
3) After the [[DTC]] DROP cutoff, but before the
Loan Termination cutoff time. See Time
Frames.
–
(Terminated)
SAS should 
send the [[SFT]] 
Loan 
Termination 
message 
immediately 
after receiving 
and processing 
it.
[[SFT]] 
Transaction 
Type: TERC – 
[[SFT]] Loan 
Termination
MT547/545
Table 6.20  [[SFT]] Loan Termination
1. UTC receives an [[SFT]] Loan Termination message. (UTC message type=T).
[[SFT]] Loan Termination messages are accepted only for an off-leg return when in certain SAS statuses and during
certain time frames during the processing day.
2. UTC sends a validated and accepted message back to the client.
3. SAS processes the [[SFT]] Loan Termination message.
4. SAS notifies the [[Borrower]] and lender of the [[SFT]] Loan Termination status of the off-leg return. See row 25 in Table
6.20.
[[SFT]] Clearing: General User Guide

---

## Page 90

6. Messaging Flows 90
[[SFT]] Clearing: General User Guide

---

## Page 91

6. Messaging Flows 91
6.21 [[NSCC]] Exit
[[NSCC]] determines an [[SFT]] is no longer eligible for the [[SFT]] Clearing service and removes the outstanding off-leg return 
from the system.
On-leg or Off-leg What 
Occurred
Status When ISO 
Message 
Type
Exits
29 Exits [[NSCC]] 
exits due 
to 
ineligible 
security.
–
(Terminated 
by [[NSCC]])
SAS should process after the Pricing file is received 
from Risk. SAS performs a mark and then exits. 
This occurs at approximately 8:15 P.M. Eastern 
Time (before the night cycle). The mark should be 
guaranteed through the day cycle.
[[SFT]] Transaction Type: TERN – [[NSCC]] Termination
MT547/545
Table 6.21  [[NSCC]] Exit
1. SAS database has the off-leg return for SFTs in the PEND status.
2. SAS determines the off-leg return loan needs to be exited.
3. SAS processes a [[mark-to-market]] for that loan.
4. SAS notifies both the [[Borrower]] and lender of the TERN – NCSS Termination status of the off-leg return. See row
29 in Table 6.21.
[[SFT]] Clearing: General User Guide

---

## Page 92

6. Messaging Flows 92
6.22 Reject/Cancel of a New Loan On-leg Message
A new [[SFT]] on-leg instruction is submitted and accepted. The on-leg has not settled yet at [[DTC]]. A cancel message is 
submitted and accepted. At [[NSCC]], the cancel message is passed to the SAS system that attempts to cancel the on-
leg, which settles before the cancellation could occur.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Cancel
31 On-leg Cancel
(New Loan or Roll)
On-leg [[DO]] or price 
differential (PD) is 
Pending at [[DTC]].
REJECT On-leg [[DO]] or PD cannot be canceled as it 
was already MADE after being accepted 
by UTC.
[[SFT]] Transaction Type: CANC – 
Canceled by Client
MT548
Table 6.22  Reject/Cancel of a New Loan On-leg Message
1. UTC receives a New Loan message. (UTC message type=N).
2. UTC sends a validated and accepted message back to the client.
3. SAS holds the [[SFT]] transactions in the database awaiting the Lender to submit a valid [[DO]] instruction to [[DTC]].
4. The Lender submits a valid [[DO]] to [[DTC]] to deliver [[shares]] from the Lender's account to the [[NSCC]] [[SFT]] account (881)
versus the [[settlement]] Amount for that Reference [[ID]] using the new [[SFT]] [[DO]] reason code 200.
5. SAS sends the [[DO]] to [[DTC]] from account 881 to the [[Borrower]]'s account for the same quantity and [[settlement]]
amount using the [[SFT]] [[DO]] reason code 200.
6. [[SFT]] and [[DO]] are in the PEND status at [[DTC]].
7. UTC receives a Cancel message. (UTC message type=C).
8. UTC sends a validated and accepted message back to the client.
9. SAS attempts to cancel both DOs in the PEND status at [[DTC]], but the DOs are MADE before they can be canceled.
10. SAS notifies both the [[Borrower]] and lender of the REJECT through a CANC - Canceled by Client message. See row
31 in Table 6.22.
[[SFT]] Clearing: General User Guide

---

## Page 93

6. Messaging Flows 93
[[SFT]] Clearing: General User Guide

---

## Page 94

6. Messaging Flows 94
6.23 Reject/Cancel of a Roll Message
A roll on-leg instruction is submitted and accepted. The on-leg (or price differential) has not settled yet at [[DTC]]. A cancel 
message is submitted and accepted. At [[NSCC]], the cancel message is passed to the SAS system that attempts to 
cancel the price differential, which settles before the cancellation could occur.
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Cancel
31 On-leg Cancel
(New Loan or Roll)
On-leg [[DO]] or price 
differential (PD) is 
pending at [[DTC]].
REJECT On-leg [[DO]] or PD cannot be canceled as it 
was already MADE after being accepted 
by UTC.
[[SFT]] Transaction Type: CANC – 
Canceled by Client
MT548
Table 6.23  Reject/Cancel of a Roll Message
1. UTC receives a Roll message. (UTC message type=R).
2. UTC sends a validated and accepted message back to the client.
3. SAS calculates the Price Differential (PD) and sends to [[DTC]] using [[SFT]] PD reason code 800.
4. [[SFT]] and PD are in the PEND status at [[DTC]].
5. UTC receives a Cancel message. (UTC message type=C).
6. UTC sends a validated and accepted message back to the client.
7. SAS attempts to cancel both PDs in the PEND status at [[DTC]], but the PDs are MADE before they can be canceled.
8. SAS notifies both the [[Borrower]] and lender of the REJECT  through a CANC  – Canceled by Client message. See
row 31 in Table 6.23.
[[SFT]] Clearing: General User Guide

---

## Page 95

6. Messaging Flows 95
[[SFT]] Clearing: General User Guide

---

## Page 96

6. Messaging Flows 96
6.24 Cancel a [[DO]] Off-leg Return From the Previously Submitted 
Send-to-Settle (Accelerated)
A new [[SFT]] or roll on-leg instruction is submitted and accepted. The on-leg settles at [[DTC]]. [[NSCC]] sets up the off-leg 
with the scheduled return for the next business day. A Send-to-Settle message is received and accepted to accelerate 
the return of [[shares]] from the next business day to the current business day. [[NSCC]] immediately accelerates the off-leg 
return of [[shares]] versus the [[settlement]] value, which is sent to [[DTC]] and has not yet settled. A cancel message is 
submitted and accepted. [[NSCC]] cancels the off-leg Send-to-Settle [[DO]] instruction at [[DTC]].
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Cancel
32 Off-leg 
([[DO]] Return)
Off-leg [[DO]] return is pending at 
[[DTC]] after a Send-to-Settle 
message was processed to 
return the [[shares]] that 
accelerated the return from the 
next business date to the 
current business date.
CANC The Cancels message cancels the off-
leg [[DO]] return. It does not cancel the 
off-leg (like it does with the on-leg). 
Before submitting this Cancel 
message, a Send-to-Settle message 
must be submitted to initiate the [[DO]] 
return at [[DTC]], which is pending.
[[SFT]] Transaction Type: SNDS – 
Send-to-Settle
MT548
Table 6.24  Cancel a [[DO]] Off-leg Return
1. SAS database has the off-leg return for [[SFT]] transactions in the PEND status set to return on the next business day.
2. UTC receives a Send-to-Settle message. (UTC message type=S).
3. UTC sends a validated and accepted message back to the client.
4. SAS immediately sends [[DO]] instructions to [[DTC]] to return the original off-leg using [[SFT]] reason code 201.
5. [[SFT]] and [[DO]] are in the PEND status at [[DTC]].
6. UTC receives a Cancel message (UTC message type=C).
7. UTC sends a validated and accepted message back to the client.
8. SAS cancels both DOs that are in the  PEND status at [[DTC]].
9. SAS notifies both the [[Borrower]] and lender of the CANC – Canceled  status of the accelerated off-leg return. See
row 32 in Table 6.24.
[[SFT]] Clearing: General User Guide

---

## Page 97

6. Messaging Flows 97
[[SFT]] Clearing: General User Guide

---

## Page 98

6. Messaging Flows 98
6.25 Reject of a Cancel of [[DO]] Off-leg Return From the Previously 
Submitted Send-to-Settle (Accelerated)
A new [[SFT]] or roll on-leg instruction is submitted and accepted. The on-leg settles at [[DTC]]. [[NSCC]] sets up the off-leg 
with the scheduled return for the next business day. A Send-to-Settle message is received and accepted to accelerate 
the return of [[shares]] from the next business day to the current business day. [[NSCC]] immediately accelerates the off-leg 
return of [[shares]] versus the [[settlement]] value, which is sent to [[DTC]] and has not yet settled. A cancel message is 
submitted and accepted. At [[NSCC]], the cancel message is passed to the SAS system that attempts to the cancel the 
off-leg Send-to-Settle [[DO]] instruction, which already settled at [[DTC]].
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Cancel
33 Off-leg 
([[DO]] Return)
Off-leg [[DO]] return is pending at [[DTC]] after 
a Send-to-Settle message was processed 
to return the [[shares]] that accelerated the 
return from the next business date to the 
current business date.
RJCT Off-leg [[DO]] return (after 
receiving a Send-to-Settle 
message) cannot be 
canceled as it was already 
MADE after being accepted 
by UTC.
[[SFT]] Transaction Type: 
CANC – Canceled by Client
MT548
Table 6.25  Reject of a Cancel of [[DO]] Off-leg Return
1. SAS has the off-leg return for [[SFT]] transactions in the PEND status set to return on the next business day.
2. UTC receives a Send-to-Settle message. (UTC message type=S).
3. UTC sends a validated and accepted message back to the client.
4. SAS immediately sends [[DO]] instructions to [[DTC]] to return the original off-leg using [[SFT]] reason code 201.
5. [[SFT]] and [[DO]] are in the  PEND status at [[DTC]].
6. UTC receives a Cancel message. (UTC message type=C).
7. UTC sends a validated and accepted message back to the client.
8. SAS attempts to cancel both DOs in the PEND status at [[DTC]], but the DOs are MADE before they can be canceled.
9. SAS notifies both the [[Borrower]] and lender of the RJCT – Reject of the cancel message of the accelerated off-leg
return. See row 33 in Table 6.25.
[[SFT]] Clearing: General User Guide

---

## Page 99

6. Messaging Flows 99
[[SFT]] Clearing: General User Guide

---

## Page 100

6. Messaging Flows 100
6.26 [[NSCC]] Initiated Price Differential
An off-leg is set to be returned the current business day. [[NSCC]] is blocking roll transactions. [[NSCC]] initiates the price 
differential at [[DTC]]. The price differential settles. [[NSCC]] keeps the [[DTCC]] Reference [[ID]] the same and updates the 
scheduled return to the next business day. 
On-leg or Off-leg What 
Occurred
Status When ISO 
Message 
Type
[[NSCC]] Initiated Price Differential
34 Off-leg [[NSCC]] 
Initiated 
Price 
Differential
MADE Off-leg is blocked from being rolled because of one of 
the following:
l Security is undergoing a mandatory corporate action
that [[NSCC]] is supporting.
l [[DTCC]] Reference Loan [[ID]] has a recall (as part of the
Buy-in process).
As a result, [[NSCC]] calculates and submits the PD to 
[[DTC]] and receives a MADE message. Upon completion, 
the [[DTCC]] Reference Loan [[ID]] remains the same as the 
[[settlement]] date is moved forward.
[[SFT]] Transaction Type: PDIF – Price Differential
Note: The following also occurs if [[NSCC]] receives a 
DROP message from [[DTC]]. When this occurs, the PD 
did not settle, but [[NSCC]] processes the mark at the 
DROP cutoff time and still reports a MADE message to 
members. The mark is collected as part of the [[NSCC]] 
final money [[settlement]].
MT547/545
35 Off-leg [[NSCC]] 
Initiated 
Price 
Differential
PEND Follows 34. This is the new off-leg, after the PD settles, 
that replaces the previous off-leg from 34. 
[[SFT]] Transaction Type: PDIF – Price Differential
Note: The following also occurs if [[NSCC]] receives a 
DROP message from [[DTC]]. When this occurs, the PD 
did not settle, but [[NSCC]] processes the mark at the 
DROP cutoff time and reports a MADE message to 
members. The mark is collected as part of the [[NSCC]] 
final money [[settlement]].
MT548
Table 6.26  [[NSCC]] Initiated Price Differential
1. SAS database has the off-leg return for the [[SFT]] transactions in the PEND status.
2. The [[DTCC]] Reference [[ID]] of the loan is blocked from being rolled by [[NSCC]].
3. SAS calculates the Price Differential (PD) and sends to [[DTC]] using [[SFT]] PD reason code 800.
4. [[SFT]] and PD are MADE.
[[SFT]] Clearing: General User Guide

---

## Page 101

6. Messaging Flows 101
5. SAS keeps the [[DTCC]] Reference [[ID]] the same for the [[SFT]] and updates the [[settlement]] date to the next business
date.
6. SAS notifies both the [[Borrower]] and lender that the original off-leg (at the previous [[settlement]] value) is MADE. See
row 34 in Table 6.26.
7. SAS notifies both the [[Borrower]] and lender that the new off-leg (which has the same [[DTCC]] Reference [[ID]] as the
original off-leg) is in the  PEND status with the new [[settlement]] value. See row 35 in Table 6.26.
[[SFT]] Clearing: General User Guide

---

## Page 102

6. Messaging Flows 102
6.27 Corporate Actions
SAS notifies clients about upcoming corporate actions using the Corporate Action Indicator in its ISO messages. This 
field is populated in all ISO client messages up to 30 days prior to the key event day for a corporate action. In the case 
of a supported corporate action, the Corporate Action indicator is set to a specific supported corporate action.  In the 
case of a non-supported corporate action, set the Corporate Action indicator to CAUN - Undergoing a Non-supported 
Corporate Action.
6.27.1 Forward [[Stock]] Split
The following table shows the forward [[Stock]] split details:
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Forward [[Stock]] Split
36 Off-leg ([[DO]] 
Return)
The company announces a forward [[Stock]] split, 
and SAS updates its positions accordingly. To 
this end, SAS sends TWO messages in support 
of this corporate action.
MADE The first message is 
sent and takes the 
previous position off 
its books. 
Corporate Action 
Indicator: FSSP – 
Forward [[Stock]] Split 
([[Stock]] component)
[[SFT]] Transaction 
Type: NRCA  – No 
Roll & Corporate 
Action
MT547/545
37 Off-leg ([[DO]] 
Return)
SAS already sent one message to remove the 
previous position. The second message is now 
sent.
PEND The second 
message is sent, 
and it adds on a 
new position. 
Corporate Action 
Indicator: FSSP – 
Forward [[Stock]] Split
[[SFT]] Transaction 
Type: NRCA – No 
Roll & Corporate 
Action
MT548
Table 6.27  Forward [[Stock]] Split
1. SAS system notifies clients of an upcoming forward [[Stock]] split in all ISO messages in that security (for example,
new SFTs or  rolls) up to 30 days prior to the key event date. In this case, the corporate action indicator  is set to
FSSP – Forward [[Stock]] Split.
[[SFT]] Clearing: General User Guide

---

## Page 103

6. Messaging Flows 103
2. On the forward [[Stock]] split payable date, SAS sends the first message and notifies both the [[Borrower]] and lender
that the original off-leg is MADE. This transaction takes down the pre-forward-[[Stock]]-split position. See row 36 in
Table 6.27.
3. Following the first message, SAS sends the second message and notifies both the [[Borrower]] and lender that the
new off-leg with the new share quantity (which is the same as [[DTCC]] Reference [[ID]] for the original off-leg) is in a
PEND status with the same [[settlement]] value as the previous transaction. See row 37 in Table 6.27.
[[SFT]] Clearing: General User Guide

---

## Page 104

6. Messaging Flows 104
6.27.2 Reverse [[Stock]] Split
The following table shows the reverse [[Stock]] split details:
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Reverse [[Stock]] Split
38 Off-leg ([[DO]] 
Return)
The company announces a reverse [[Stock]] 
split, and SAS updates its positions 
accordingly. To this end, SAS sends TWO 
messages in support of this corporate 
action.
MADE The first message is 
sent and takes the 
previous position off its 
books in the previous 
[[CUSIP]]. 
Corporate Action 
Indicator: RSSP – 
Reverse [[Stock]] Split
[[SFT]] Transaction Type: 
NRCA – No Roll & 
Corporate Action
MT547/545
39 Off-leg ([[DO]] 
Return)
SAS already sent one message to remove 
the previous position. The second message 
is now sent.
PEND The second message 
is sent, and it adds on a 
new position in the new 
[[CUSIP]]. 
Corporate Action 
Indicator: RSSP – 
Reverse [[Stock]] Split
[[SFT]] Transaction Type: 
NRCA  – No Roll & 
Corporate Action
MT548
Table 6.28  Reverse [[Stock]] Split
1. SAS system notifies clients of an upcoming reverse [[Stock]] split in all ISO messages in that security (for example,
new SFTs or  rolls) up to 30 days prior to the key event date. In this case, the corporate action indicator  is set to
RSSP  – Reverse [[Stock]] Split.
2. On the reverse [[Stock]] split payable date, SAS sends the first message and notifies both the [[Borrower]] and lender
that the original off-leg is MADE. This transaction takes down the pre-reverse-[[Stock]]-split position. See row 38 in
Table 6.28.
[[SFT]] Clearing: General User Guide

---

## Page 105

6. Messaging Flows 105
3. Following the first message, SAS sends the second message and notifies both the [[Borrower]] and lender that the
new off-leg with the new share quantity (which is the same [[DTCC]] Reference [[ID]] as the original off-leg) is in a PEND
status with the same [[settlement]] value as the previous transaction. See row 39 in Table 6.28.
[[SFT]] Clearing: General User Guide

---

## Page 106

6. Messaging Flows 106
6.27.3 Cash Merger
The following table provides the cash merger details:
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Cash Merger
40 Off-leg 
([[DO]] Return)
The company announces a cash merger, and 
SAS updates its positions accordingly. To this 
end, SAS sends only ONE message in 
support of this corporate action.
MADE A message is sent 
and takes the 
previous position off 
its books in the 
previous [[CUSIP]]. 
Corporate Action 
Indicator: CHMR – 
Cash Merger
[[SFT]] Transaction 
Type: NRCA – No Roll 
& Corporate Action
MT547/545
Table 6.29  Cash Merger
1. SAS system notifies clients of a cash merger in all ISO messages in that security (for example, new SFTs or  rolls)
up to 30 days prior to the key event date. In this case, the corporate action indicator  is set to CHMR  - Cash Merger.
2. On the cash merger date, SAS sends the first message and notifies both the [[Borrower]] and lender that the original
off-leg is MADE. This transaction takes down the cash merger position. See row 40 in Table 6.29.
3. SAS does not send a second message relating to the cash component to clients.
[[SFT]] Clearing: General User Guide

---

## Page 107

6. Messaging Flows 107
6.27.4 [[Stock]] Merger
The following table shows the [[Stock]] merger details:
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
[[Stock]] Merger
41 Off-leg ([[DO]] 
Return)
The company announces a [[Stock]] merger, 
and SAS updates its positions accordingly. 
To this end, SAS sends TWO messages in 
support of this corporate action.
MADE The first message is 
sent and takes the 
previous position off its 
books in the previous 
[[CUSIP]]. 
Corporate Action 
Indicator: STMR – 
[[Stock]] Merger
[[SFT]] Transaction Type: 
NRCA – No Roll & 
Corporate Action
MT547/545
42 Off-leg ([[DO]] 
Return)
SAS already sent one message to remove 
the previous position. The second message 
is now sent.
PEND The second message is 
sent, and it adds on a 
new position in the new 
[[CUSIP]]. 
Corporate Action 
Indicator: STMR – 
[[Stock]] Merger
[[SFT]] Transaction Type: 
NRCA – No Roll & 
Corporate Action
MT548
Table 6.30  [[Stock]] Merger
1. SAS system notifies clients of an upcoming [[Stock]] merger in all ISO messages in that security (for example, new
SFTs or  rolls) up to 30 days prior to the key event date. In this case, the corporate action indicator  is set to STMR  –
[[Stock]] Merger.
2. On the [[Stock]] merger date, SAS sends the first message and notifies both the [[Borrower]] and lender that the original
off-leg is MADE. This transaction takes down the pre-[[Stock]]-merger position. See row 41 in Table 6.30.
3. Following the first message, SAS sends the second message and notifies both the [[Borrower]] and lender that the
new off-leg with the new share quantity and [[CUSIP]] (which is the same [[DTCC]] Reference [[ID]] as the original off-leg)
is in a PEND status with the same [[settlement]] value as the previous transaction. See row 42 in Table 6.30.
[[SFT]] Clearing: General User Guide

---

## Page 108

6. Messaging Flows 108
[[SFT]] Clearing: General User Guide

---

## Page 109

6. Messaging Flows 109
6.27.5 Cash & [[Stock]] Merger
The following table shows the cash and [[Stock]] merger details:
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Cash and [[Stock]] Merger
43 Off-leg ([[DO]] 
Return)
The company announces a cash and [[Stock]] 
merger, and SAS updates its positions 
accordingly. To this end, SAS sends TWO 
messages in support of this corporate action.
MADE The first message is 
sent and takes the 
previous position off its 
books in the previous 
[[CUSIP]]. 
Corporate Action 
Indicator: CSMR – 
Cash and [[Stock]] 
Merger
[[SFT]] Transaction 
Type: NRCA – No Roll 
& Corporate Action
MT547/545
44 Off-leg ([[DO]] 
Return)
SAS already sent one message to remove 
the previous position. The second message 
is now sent.
PEND The second message 
is sent, and it adds on 
a new position in the 
new [[CUSIP]]. 
Corporate Action 
Indicator: CSMR – 
Cash and [[Stock]] 
Merger
[[SFT]] Transaction 
Type: NRCA – No Roll 
& Corporate Action
MT548
Table 6.31  Cash and [[Stock]] Merger
1. SAS system notifies clients of an upcoming cash and [[Stock]] merger in all ISO messages in that security (for
example, new SFTs or  rolls) up to 30 days prior to the key event date. In this case, the corporate action indicator  is
set to CSMR – Cash and [[Stock]] Merger.
2. On the cash and [[Stock]] merger date, SAS sends the first message and notifies both the [[Borrower]] and lender that the
original off-leg is MADE. This transaction takes down the pre-cash-and-[[Stock]]-merger position. See row 43 in Table
6.31.
3. Following the first message, SAS sends the second message and notifies both the [[Borrower]] and lender that the
new off-leg with the new share quantity and [[CUSIP]] (which is the same [[DTCC]] Reference [[ID]] as the original off-leg)
is in a PEND status with the same [[settlement]] value as the previous transaction. See row 44 in Table 6.31.
4. SAS does not send a second message relating to the cash component to clients.
[[SFT]] Clearing: General User Guide

---

## Page 110

6. Messaging Flows 110
[[SFT]] Clearing: General User Guide

---

## Page 111

6. Messaging Flows 111
6.27.6 Name Change
The following table shows the name change details:
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
Name Change
45 Off-leg ([[DO]] 
Return)
The company announces a [[Stock]] merger, 
and SAS updates its positions accordingly. 
To this end, SAS sends TWO messages in 
support of this corporate action.
MADE The first message is 
sent and takes the 
previous position off its 
books in the previous 
[[CUSIP]]. 
Corporate Action 
Indicator: NMCG – 
Name Change ([[Stock]] 
component)
[[SFT]] Transaction Type: 
NRCA – No Roll & 
Corporate Action
MT547/545
46 Off-leg ([[DO]] 
Return)
SAS already sent one message to remove 
the previous position. The second message 
is now sent.
PEND The second message is 
sent, and it adds on a 
new position in the new 
[[CUSIP]]. 
Corporate Action 
Indicator: NMCG – 
Name Change ([[Stock]] 
component)
[[SFT]] Transaction Type: 
NRCA – No Roll & 
Corporate Action
MT548
Table 6.32  Name Change
1. SAS system notifies clients of an upcoming name change in all ISO messages in that security (for example, new
SFTs or  rolls) up to 30 days prior to the key event date. In this case, the corporate action indicator  is set to NMCG –
Name Change.
2. On the name change date, SAS sends the first message and notifies both the [[Borrower]] and lender that the original
off-leg is MADE. This transaction takes down the pre-cash-and-[[Stock]]-merger position. See row 45 in Table 6.32.
3. Following the first message, SAS sends the second message and notifies both the [[Borrower]] and lender that the
new off-leg with the new  [[CUSIP]] (which is the same [[DTCC]] Reference [[ID]] as the original off-leg) is in a PEND status
with the same [[settlement]] value as the previous transaction. See row 46 in Table 6.32.
4. SAS does not send a second message relating to the cash component to clients.
[[SFT]] Clearing: General User Guide

---

## Page 112

6. Messaging Flows 112
[[SFT]] Clearing: General User Guide

---

## Page 113

6. Messaging Flows 113
6.28 [[Broker]] Reorg
The following table shows the [[Broker]] reorg details:
On-leg or Off-leg What Occurred Status When ISO 
Message 
Type
[[Broker]] Reorg
47 Off-leg ([[DO]] 
Return)
[[Broker]] Reorg announced. To 
this end, SAS sends TWO 
messages in support of this 
action.
MADE The first message is sent and takes 
the previous position off its books 
with the previous [[NSCC]] [[SFT]] 
Account number. 
[[SFT]] Transaction Type: BKRO – 
[[Broker]] Re-Org
MT547/545
48 Off-leg ([[DO]] 
Return)
SAS already sent one message 
to remove the previous position. 
The second message is now 
sent.
PEND The second message is sent, and it 
adds on a new position in the 
[[NSCC]]/[[SFT]] Account number. 
[[SFT]] Transaction Type: BKRO – 
[[Broker]] Re-Org
MT548
Table 6.33  [[Broker]] Reorg
1. On the [[Broker]] reorg date, SAS sends the first message and notifies both the [[Borrower]] and lender that the original
off-leg is MADE. This transaction takes down the pre-[[Broker]]-reorg [[SFT]]. See row 47 in Table 6.33.
2. Following the first message, SAS sends the second message and notifies both the [[Borrower]] and lender that the
new off-leg with the new [[Broker]] number (which is the same [[DTCC]] Reference [[ID]] as the original off-leg) is in a PEND
status with the same [[settlement]] value as the previous transaction. See row 48 in Table 6.33.
[[SFT]] Clearing: General User Guide

---

## Page 114

A. MESSAGE LAYOUTS
A.1 Messaging and File Types
To support [[SFT]] processing, [[DTCC]] leverages existing client interfaces. These include
l Universal Trade Capture (UTC)
The UTC data feed comprises a series of variable-length sequenced messages following the FIX version 4.4 conventions. While the FIX tag-based
structure is leveraged, messages may be sent through the FIX engine or Message Queue (MQ).
For more information about tag structure and requirements, see the Universal Trade Capture (UTC) User Guide located in the [[DTCC]] Learning Center.
l [[securities]] Financing Accounting System (SAS)
As a result of leveraging [[NSCC]]’s [[CNS]] processing structure, the SAS interface allows ISO messaging for transaction input and output and machine-
readable output (MRO) for end of day files. For each message and file type, see SAS ISO Message Output. For a specific MRO file, see File and Report
Layouts.
l [[DTC]]
[[DTC]] processing includes new [[settlement]] codes to support [[SFT]] processing; however, the messaging interface structure will not change.
[[SFT]] Clearing: General User Guide
A. Message Layouts 114

---

## Page 115

A.2 UTC Message Types
With the [[SFT]] Clearing service, there are eight message types that can be submitted for processing to the UTC system. For all message types, the 
counterparties on the message should always be populated in their role of how the on-leg was originally submitted to [[DTCC]]. For example, if [[Broker]] 0123 
was the original [[Borrower]] ([[Buyer]]) on the new Loan Message and [[Broker]] 0122 was the lender ([[Seller]]), for all other messages submitted to [[DTCC]] regarding 
that same [[DTCC]] Reference [[ID]], such as Send-to-Settle, [[Broker]] 0123 should always be the [[Borrower]] ([[Buyer]]) and 0122 the lender ([[Seller]]).
The output from the UTC system is based upon how the input was submitted. The following table provides a description of all the [[SFT]] Clearing message 
types:
Note
All times are in Eastern Time (ET). 
Message Type Input availability: Cutoff Submission Rules:
New Loan 
(Street-side)
4:00 A.M. - 3:00 P.M. ET A new [[SFT]] between two [[SFT]] members where the on-leg ([[shares]] 
and [[settlement]] value) is processed to settle through the [[NSCC]] 
Clearing account at [[DTC]]. After that transaction settles, the off-leg 
that is set to be returned the next business day will be novated to 
[[NSCC]].
Pre-established 
Bilateral Loan
4:00 A.M.  - 3:00 P.M. ET A new [[SFT]] between two [[SFT]] members where the on-leg ([[shares]] 
and [[settlement]] value) already settled directly between the [[SFT]] 
members at [[DTC]]. Upon receipt, the off-leg that is set to be returned 
the next business day will be novated to [[NSCC]].
Roll 4:00 A.M. - 11:30 A.M. ET A new [[SFT]] between two [[SFT]] members that instructs [[NSCC]] to net 
the new [[SFT]] against an off-leg [[SFT]] that is set to be returned the 
current business day. This results in [[NSCC]] processing a Price 
Differential charge that will settle between the [[SFT]] members through 
the [[NSCC]] Clearing account at [[DTC]]. 
[[SFT]] Clearing: General User Guide
A. Message Layouts 115

---

## Page 116

Message Type Input availability: Cutoff Submission Rules:
Send-to-Settle 4:00 A.M. -  3:00 P.M. ET A transaction message between two [[SFT]] members submitted 
against an existing off-leg return. Depending on the status of the 
[[DTCC]] Reference [[ID]], it does the following:
l Accelerates the full share return of the off-leg before 11:30 A.M.
ET on the original (or current) [[settlement]] date of the off-leg [[SFT]]
return.
l Accelerates the full or partial share return of the off-leg from the
original (or next) [[settlement]] date to the current [[settlement]] date.
l If the message is being used for
New Loans,   the quantity field must
be submitted with the full share
amount of the [[DTCC]] Reference
[[ID]].
l If the message is being used for
Pre-established Bilateral Loans,
the quantity field can be submitted
with a quantity equal to or less
than the [[DTCC]] Reference [[ID]] of
the off-leg return pending in the
database.
Cancel Message 4:00 A.M. –  3:00 P.M. ET A transaction message between two [[SFT]] members submitted 
against an existing on-leg or off-leg return. Depending on the status 
of the [[DTCC]] Reference [[ID]], it does one of the following:  
l Cancels the on-leg [[DO]] transaction that is Pending at [[DTC]] (from
receipt of a New Loan Message).
l Cancels the on-leg Price Differential charge that is Pending at
[[DTC]] (from receipt of a roll transaction).
l Cancels a Pending [[DO]] off-leg return at [[DTC]] after a
Send-to-Settle message was submitted that accelerated the
return of [[shares]] from the next business day to the current
business day.
l If the message is being used for
New Loans or Pre-established
Bilateral Loans, the quantity field
must be submitted with the full
share amount of the [[DTCC]]
Reference [[ID]] along with the
correct Tag 66 value.
l If the message is being used for
Rolls, the quantity field must be
submitted with a quantity equal to
a Send-to-Settle message that
was previously submitted which
generated the off-leg return
Pending at [[DTC]] along with the
correct associated Tag 66 value.
[[SFT]] Clearing: General User Guide
A. Message Layouts 116

---

## Page 117

Message Type Input availability: Cutoff Submission Rules:
Rate 
Modification
4:00 A.M. - 3:45 P.M. ET A transaction between two [[SFT]] members submitted against an 
existing [[DTCC]] Reference [[ID]]. This informs [[NSCC]] that either 1) the 
lending interest rate on the outstanding [[SFT]] has been updated or 2) 
the party who is getting paid the interest has been updated. [[NSCC]] 
will use this updated lending rate to calculate the overnight rebate 
interest. 
Rate modification messages can be 
received anytime of the day until 3:45 
P.M. ET.
Loan 
Termination
4:00 A.M. - 4:30 P.M. ET A transaction between two [[SFT]] members submitted against an 
existing [[DTCC]] Reference [[ID]]. This instructs [[NSCC]] to remove the 
outstanding [[DTCC]] Reference [[ID]] from clearing.
[[SFT]] Terminations can only be 
processed against an off-leg return at 
the following times during the course 
of a business day:
l Until 11:30 A.M. ET (on the
original SD it was set to be
returned) as long as the off-leg
return was not rolled or the [[DO]]
return was not sent to [[DTC]] for
[[settlement]].
l Anytime during the day (on the
same day the on-leg settled and
the off-leg return is set to be
returned the next business day)
provided no Send-to-Settle
Message was received or if a
Send-to-Settle Message was
received, there is no [[DO]] Pending
at [[DTC]].
l After [[DTC]] [[settlement]] DROP
cutoff 4:30 P.M. ET (Termination
cutoff time).
[[SFT]] Clearing: General User Guide
A. Message Layouts 117

---

## Page 118

Message Type Input availability: Cutoff Submission Rules:
Buy-side 4:00 A.M. - 3:00 P.M. ET An [[SFT]] between an [[SFT]] [[Member]], such as a Sponsoring [[Member]] 
and their Sponsored Members. The Sponsoring [[Member]] may enter 
into a back-to-back trade when they are taking on a principal lending 
or principal borrowing relationship with a Sponsored [[Member]].   The 
back-to-back trade has [[NSCC]] in the middle of all [[obligations]] and, as 
such, [[NSCC]] is the central counterparty to all parties of the 
transaction. There is no [[DTC]] [[settlement]] on the transaction.
[[SFT]] Clearing: General User Guide
A. Message Layouts 118

---

## Page 119

A.3 UTC  Input and Output Formats
The following table provides a description for all the UTC input/output formats:
Format Description
Input Formats
UTC Input FIX/MQ Format Input formats used by the Approved [[SFT]] Submitter to submit buy-side and/or street-side [[SFT]] message 
transactions to UTC using the FIX protocol via FIX engine or MQ channel.
UTC Input [[EOD]] Totals FIX/MQ Format Input format used by the Approved [[SFT]] Submitter that recaps the number of [[SFT]] message transactions 
they sent to UTC for the processing day. This will be an End of Day ([[EOD]]) balancing message which will be 
the last transaction message of the day sent by the Approved [[SFT]] Submitter. After this message is sent, no 
more message transactions will be accepted from that Approved [[SFT]] Submitter for that processing day. 
The [[EOD]] message will be used by UTC for reconciliation.
Output Formats
UTC Output FIX/MQ Format Output format sent by UTC to the Approved [[SFT]] Submitter and [[SFT]] Clearing Members that provides a real 
time update status (either Accepted or Rejected) of each [[SFT]] message transaction that was received after 
input submission. 
Note: A rejected message is just sent to the Approved [[SFT]] Submitter.
UTC Outbound Gap Fill Request FIX/MQ 
Format
Output format sent by to UTC to the Approved [[SFT]] Submitter to alert them that a message transaction gap 
was detected by UTC.
UTC Outbound [[EOD]] Confirmation to Market 
FIX/MQ Format 
Output format sent by UTC as the end of day confirmation to the market. 
UTC Outbound Buy-Side Cutoff FIX/MQ 
Format (3:00 P.M. ET)
Output format sent by UTC to the Sponsoring [[SFT]] Clearing [[Member]] to alert them that maturing off-leg 
return transactions (between them and their Sponsors) have been released from NSCCs guaranty 
obligation.
UTC Outbound [[EOD]] Messages to 
Participants by Market
Output format sent by UTC to each [[SFT]] Clearing [[Member]] that had transactions for the processing day 
which contains the aggregate total transactions, [[shares]], and amount for that [[SFT]] Clearing [[Member]]. This is 
a reconciliation message for [[SFT]] Clearing Members.
[[SFT]] Clearing: General User Guide
A. Message Layouts 119

---

## Page 120

UTC Input FIX/MQ Format
Note
When becoming an Approved Trade Submitter, you must indicate to [[NSCC]] if you will be submitting [[SFT]] transactions as either 1) a Vendor (independent 
third-party that is not a counterparty to an [[SFT]] transaction) or 2) a counterparty to the [[SFT]] transaction, which is also a direct [[NSCC]] [[SFT]] [[Member]].
If you are a Vendor, your Sending Entity must have relationships set up in UTC for the [[SFT]] members that you can submit for. UTC validates the [[SFT]] 
transaction input by checking your Sending Entity [[ID]] in the UTC table to see if it is a Vendor set up and whether that Vendor can submit for both Members 
in the [[SFT]] Clearing service. In Tag 448 (Submitted by Indicator), you must always set the Value=0.
If you are an [[NSCC]] [[SFT]] [[Member]], your Sending Entity must have a relationship(s) set up in UTC to their [[SFT]] [[Member]] they are submitting for. In Tag 448 
(Submitted by Indicator), you must always set the Value=1 or 2. Use the value of 1 if you are the [[Borrower]]/[[Buyer]] to the [[SFT]] transaction. Use the value of 2 
if you are the lender/[[Seller]] to the [[SFT]] transaction.
The following table provides the UTC input for the FIX/MQ format:
FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
 HEADER Y=Required / N=Optional
8 Begin String 7 A/N Identifies the beginning of a ne
w message generated by FIX.
[[default]] value: FIX.4.4
Y Y Y Y Y Y Y Y
9 Body Length 4 N Message length generated by 
FIX.
Note: Not required for MQ.
Y Y Y Y Y Y Y Y
35 Message Type 2 A/N AE = Trade Capture Report
The [[default]] value of AE is 
required.
Y Y Y Y Y Y Y Y
Table A.1  UTC Input FIX/MQ Format
[[SFT]] Clearing: General User Guide
A. Message Layouts 120

---

## Page 121

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
49 Sender Comp [[ID]] 8 A/N Assigned value used to 
identify firm sending the 
message.
TBD for each Sending Entity.
Note: Not required for MQ.
Y Y Y Y Y Y Y Y
115 Sending Entity 4 A/N Identifies the source 
submitting a trade or 
transaction. Used in 
conjunction with the Sending 
Subsystem and Trade 
Sequence Number to uniquely 
identify the trade message. 
Value predetermined by 
[[NSCC]].
Y Y Y Y Y Y Y Y
56 Target Comp [[ID]] 4 A/N Assigned value used to 
identify the receiving firm 
message.
[[default]] value: [[NSCC]]
Y Y Y Y Y Y Y Y
34 Trade Sequence 9 N Unique message identifier 
generated by FIX.
Note: Not required for MQ.
Y Y Y Y Y Y Y Y
52 Sending Time 21 A/N Timestamp generated by FIX.
Note: Not required for MQ.
Y Y Y Y Y Y Y Y
Table A.1  UTC Input FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 121

---

## Page 122

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
50 Sending Subsystem 3 A/N Used in conjunction with 
Sending Entity and Trade 
Sequence Number to uniquely 
identify the trade message.
N N N N N N N N
DETAIL (Y=Required / N=Optional)
571 Trade Sequence 
Number
8 A/N Sequential Trade Message 
Identifier generated by the 
Market. Must start at 
00000001 and increase 
sequentially with subsequent 
transactions.
In combination with tags 115 
and 50 (optional), it provides 
unique identification to each 
trade message, which will be 
used by UTC for detecting 
gaps in the trade message 
sequence number.    
Y Y Y Y Y Y Y Y
22 Security [[ID]] Source 1 A/N
l 1 = [[CUSIP]]
l 4 = ISIN
Y Y N Y Y Y N N
48 Security [[ID]] 12 A/N Security Identifier associated 
with Tag22.
Y Y N Y Y Y N N
Table A.1  UTC Input FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 122

---

## Page 123

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
32 Share QTY 11 N Share Quantity, Maximum 
value accepted 999,999,999 
Y Y N Y Y Y Y N
31 Unit Price 13 A/N Contract Price.
12 Digits + 1 (period indicating 
six decimal point offset)
N N N N N N N N
30 Market Code 3 A/N Numeric Code to identify 
submitting Exchange in UTC.
200 = [[SFT]] Market
Y Y Y Y Y Y Y Y
75 Trade Date 8 N YYYYMMDD = Format N N N N N N N N
60 Trade Execution Time 9 A/N HHMMSSMSS
Current Time Received by 
UTC = [[default]] 
N N N N N N N N
526 [[DTCC]] Reference [[ID]] 14 A/N Unique [[DTCC]] Reference [[ID]] of 
an On-leg or Off-leg 
transaction.
N N Y N Y Y Y Y
11 Buy Client Order [[ID]]
For more information 
about using Tag 11, 
see Section 5.8 and 
Section 5.8.2.
32 A/N First occurrence of the tag. 
Unique Client Order [[ID]] of the 
[[Borrower]].
Note: Only the first 16 bytes 
are passed downstream on the 
ISO messaging output.
N N N N N N N N
Table A.1  UTC Input FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 123

---

## Page 124

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
11 Sell Client Order [[ID]]
For more information 
about using Tag 11, 
see Section 5.8 and 
Section 5.8.2.
32 A/N Second occurrence of the tag. 
Unique Client Order [[ID]] of the 
Lender.
Note: Only the first 16 bytes 
are passed downstream on the 
ISO messaging output.
N N N N N N N N
66 Execution [[ID]]
For more information 
about using Tag 66, 
see Section 5.8 and 
Section 5.8.1.
32 A/N Vendor or Marketplace Unique 
Reference [[ID]].
Space=[[default]] 
N N N N N N N N
453 No Party [[ID]] 1 N Number of party IDs to follow. 
Must be at least three (Buy 
[[SFT]] 
Clearing [[Member]], Sell [[SFT]] 
Clearing [[Member]], and 
Submitted By [[participant]] are 
required) and up to a 
maximum of seven can be 
specified.
The following are required:
l Buy [[SFT]] Clearing [[Member]]
l Sell [[SFT]] Clearing [[Member]]
l Submitted By [[participant]]
Y Y Y Y Y Y Y Y
Table A.1  UTC Input FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 124

---

## Page 125

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
448 Buy [[SFT]] Clearing 
Account Number
8 A/N [[Buyer]] ([[Borrower]]) [[SFT]] 
Clearing Account Number
Y Y Y Y Y Y Y Y
452 Party Role 2 N 04 = [[SFT]] Clearing [[Member]] Y Y Y Y Y Y Y Y
448 Buy Entering / 
Executing [[Broker]]
8 A/N Market Mnemonic / MPID N N N N N N N N
452 Party Role 2 N 01 = Executing Firm N N N N N N N N
448 Buy Introducing Brok
er
8 A/N Buy Introducing [[Broker]] N N N N N N N N
452 Party Role 2 N 06 = Introducing Firm N N N N N N N N
448 Sell [[SFT]] Account 
Number
8 A/N [[Seller]] (Lender) [[SFT]] Account 
Number
Y Y Y Y Y Y Y Y
452 Party Role 2 N 18 = Contra [[SFT]] Clearing 
[[Member]]
Y Y Y Y Y Y Y Y
448 Sell Entering / 
Executing [[Broker]]
8 A/N Market Mnemonic / MPID N N N N N N N N
452 Party Role 2 N 37 = Contra Trader N N N N N N N N
448 Sell Introducing Broke
r
8
A/N Sell Introducing [[Broker]] N N N N N N N N
452 Party Role 2 N 17 = Contra Firm N N N N N N N N
Table A.1  UTC Input FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 125

---

## Page 126

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
448 Submitted By 
Indicator
Note: The value used 
in this tag determines 
the value used in Tag 
54 for an approved 
submitter output).
If Tag 448 has a value 
of 0 or 2, Tag 54 has a 
value of 2 on output 
([[Seller]]/Lender).
If Tag 448 has a value 
of 1, Tag 54 has a 
Value of 1 on output 
([[Buyer]]/[[Borrower]]).
1 A/N Value of either 
l 0 =by Market
(This value is used by an
Approved Trade Submitter
who is not a counterparty to
the [[SFT]], such as a
Vendor).
l 1 = by [[Buyer]] [[participant]]
(This value is used if the
Approved Trade Submitter
is also a counterparty to the
[[SFT]] in the role of the
[[Borrower]]).
l 2 = by [[Seller]] [[participant]]
(This value is used if the
Approved Trade Submitter
is also a counterparty to the
[[SFT]] in the role of the
lender).
Y Y Y Y Y Y Y Y
452 Party Role 2 N 36 = Entering Trader (which 
represents the Submitter of the 
message that goes with tag 
448 - Submitted by 
[[participant]]).
Y Y Y Y Y Y Y Y
Table A.1  UTC Input FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 126

---

## Page 127

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
81 [[SFT]] Transaction Type 
Code
1 A/N [[SFT]] Type Code:
l A = Pre-established
Bilateral Loan
l B = Buy-Side
l C = Cancel
l M = Rate Modification
l N = New Loan
l R = Roll
l S = Send-to-Settle
l T = Terminate
Y Y Y Y Y Y Y Y
578 Source of Transaction 
/ Market System
2 A/N Code that denotes the system 
at the market on which the 
execution occurred.
To be assigned by [[NSCC]] per 
user request. 
Examples:
l S1 – submitted by a
[[Member]] or buy-side
transaction
l S2 – submitted by vendor
Y Y Y Y Y Y Y Y
Table A.1  UTC Input FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 127

---

## Page 128

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
825 Lending / Interest 
Rate Indicator
1 A/N Lending / Interest Rate 
Indicator informs [[NSCC]] of the 
counterparty to the loan who 
should be credited the 
overnight rebate interest on 
the loan transaction:
l N=No Rate
l B=Paid to [[Borrower]]
l L=Paid to Lender
l space=N/A
Y Y Y Y Y N N N
158 Lending / Interest 
Rate
10 N Rate for Interest Amount 
calculation. 
9 Digits + 1 (period indicating 
four decimal point offset)  
Note 
* = Required for Tag 825=B or
L.
Y* Y* Y* Y* Y* N N N
159 Independent Amount 
Rate
10 N Rate for Independent Amount 
calculation.
9 Digits + 1 (period indicating 
four decimal point offset)  
N N N N N N N N
Table A.1  UTC Input FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 128

---

## Page 129

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
581 Rounding Rule Code 1 A/N Indicates Rounding Rule for 
Settle Price Calculation:
l 0 = no rounding
l 1 = up to nearest $0.01
l 2 = up to nearest $0.05
l 3 = up to nearest $0.10
l 4 = up to nearest $0.25
l 5 = up to nearest $1.00
Y Y N Y Y N N N
TRAILER (Y=Required / N=Optional)
10 Check Sum 3 A/N Generated by FIX.
Tag 10 is required on the last 
field of all messages to mark 
the end of the transaction.
Separate group transaction 
with tag 10 (Check Sum) or 
delimiter X'03'.
Y Y Y Y Y Y Y Y
Table A.1  UTC Input FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 129

---

## Page 130

UTC Input [[EOD]] Totals FIX/MQ Format
The following table provides the UTC input end of day totals for the FIX/MQ format:
FIX 
Tag
Name Length Type Description Y=Required / 
N=Optional
HEADER FIX MQ 
8 Begin String 7 A/N Identifies the beginning of a new message generated by FIX.
[[default]] Value: FIX.4.4
Y Y
9 Body Length 4 N Message length generated by FIX. Y N
35 Message Type 2 A/N h = Trading Session Status Y Y
56 Target Comp [[ID]] 4 A/N Assigned value used to identify receiving firm message.
[[default]] value: [[NSCC]]
Y Y
34 Trade Sequence 9 N Unique message identifier generated by FIX. Y N
52 Sending Time 21 A/N Timestamp generated by FIX. Y N
49 Sender Comp [[ID]] 8 A/N Assigned value used to identify firm sending message. Y N
115 Sending Entity 4 A/N Identifies the source submitting a trade or transaction. 
Value predetermined by [[NSCC]].
Y Y
DETAIL FIX MQ 
336 Trading Session [[ID]] 12 A/N MARKETTONSCC N N
340 Trading Session Status 1 A/N 3 = Closed N N
58 Process Date 8 N UTC process date. N N
387 Sending Entity Processing Total 9 N Number of [[Stock]] Loan records sent to UTC from the Sending Entity 
during the day.
Y Y
TRAILER FIX MQ 
10 Check Sum 3 A/N Generated by FIX. Y Y
Table A.2  UTC Input [[EOD]] Totals FIX/MQ Format
[[SFT]] Clearing: General User Guide
A. Message Layouts 130

---

## Page 131

UTC Output FIX/MQ Format
The following table provides the UTC output layout for the FIX/MQ format:
FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
HEADER Y=Required / N=Optional
8 Begin String 7 A/N Identifies the beginning 
of a new  message 
generated by FIX.
[[default]] Value: FIX.4.4
Y Y Y Y Y Y Y Y
9 Body Length 4 N Message length 
generated by FIX.
Note: Not required for 
MQ.
Y Y Y Y Y Y Y Y
35 Message Type 2 A/N AE = Trade Capture 
Report
Y Y Y Y Y Y Y Y
49 Sender Comp [[ID]] 8 A/N Assigned value used to 
identify firm sending 
message.
[[default]] value: [[NSCC]]
Y Y Y Y Y Y Y Y
56 Target Comp [[ID]] 4 A/N Assigned value used to 
identify receiving firm 
message.
TBD for each recipient
Y Y Y Y Y Y Y Y
Table A.3  UTC Output FIX / MQ Format
[[SFT]] Clearing: General User Guide
A. Message Layouts 131

---

## Page 132

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
34 Trade Sequence 9 N Unique message 
identifier generated by 
FIX.
Note: Not required for 
MQ.
Y Y Y Y Y Y Y Y
52 Sending Time 21 A/N Timestamp generated 
by FIX.
Y Y Y Y Y Y Y Y
DETAIL (Y=Required / N=Optional)
571 Trade Report [[ID]] 15 A/N Trade Identifier 
generated by the 
market, combination of 
input tags 115, 50 
(optional), and 571.
Y Y Y Y Y Y Y Y
22 Security [[ID]] Source 1 A/N
l 1=[[CUSIP]]
l 4=ISIN
Y Y N Y Y Y N N
48 Security [[ID]] 12 A/N Security Identifier 
associated with Tag22.
Y Y N Y Y Y N N
55 Security Symbol 15 A/N Symbol of traded 
security.
Y Y N Y Y Y N N
460 Security Type 
(Product)
2 N
l 3 = Corporate
l 5 = [[Equity]]
l 11 = Municipal
l 12 = Other
l 14 = [[UIT]]
Y Y N Y Y Y N N
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 132

---

## Page 133

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
32 Share QTY 11 N Share quantity. 
Maximum value 
accepted is 999,999,999 
Y Y N Y Y Y Y N
31 Unit Price 13 A/N Contract Price
12 Digits + 1 (period 
indicating six decimal 
point offset).
Yesterday's Market 
Close Price=[[default]] 
Y Y N Y Y N N N
30 Market Code 3 A/N Numeric Code to identify 
submitting Exchange in 
UTC.
200=[[SFT]] Market
Y Y Y Y Y Y Y Y
75 Trade Date 8 N YYYYMMDD=Format
Current Date=[[default]] 
Y Y Y Y Y Y Y Y
60 Trade Execution 
Time
9 A/N HHMMSSMSS
Current Time=[[default]] 
N N N N N N N N
64 [[settlement]] Date 8 N YYYYMMDD=Format Y Y Y Y Y Y Y Y
11 Client Order [[ID]] 32 A/N Unique Client Order [[ID]]
Note: 
Only the first 16 bytes 
are passed downstream 
on ISO messaging 
output.
N N N N N N N N
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 133

---

## Page 134

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
526 [[DTCC]] Reference 
[[ID]] - referring
14 A/N Unique [[DTCC]] 
Reference [[ID]] of a loan.
Note: Not required for 
MQ.
Y Y Y Y Y Y Y Y
526 [[DTCC]] Reference 
[[ID]]
14 A/N Unique [[DTCC]] 
Reference [[ID]] of a new 
Off-leg transaction for 
the roll 
N N N N Y N N N
66 Execution [[ID]] 32 A/N Market Execution [[ID]] N N N N N N N N
54 Side Indicator 1 A/N
l 1 = Buy/[[Borrower]]
l 2 = Sell/Lender
Y Y Y Y Y Y Y Y
453 No Party IDs 1 N Number of party IDs to 
follow.  Must be at least 
two (Buy and Sell [[SFT]] 
Clearing Members are 
required) and up to a 
maximum of nine can be 
specified.
Y Y Y Y Y Y Y Y
448 [[SFT]] Clearing 
[[Member]] Account 
Number
8 A/N [[SFT]] Clearing [[Member]] 
Account Number
Y Y Y Y Y Y Y Y
452 Party Role 2 N 04 = [[SFT]] Clearing 
[[Member]]
Y Y Y Y Y Y Y Y
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 134

---

## Page 135

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
448 Entering / 
Executing [[Broker]]
8 A/N Market Mnemonic / 
MPID 
N N N N N N N N
452 Party Role 2 N 01 = Executing Firm N N N N N N N N
448 Introducing [[Broker]] 8 A/N Introducing [[Broker]] N N N N N N N N
452 Party Role 2 N 06 = Introducing Firm N N N N N N N N
448 Settling [[Broker]] 8 A/N [[NSCC]] [[participant]] 
Number
Y Y Y Y Y Y Y Y
452 Party Role 2 N 11 = Settling Account Y Y Y Y Y Y Y Y
448 Contra [[SFT]] 
Clearing [[Member]] 
Account
8 A/N [[NSCC]] Contra [[SFT]] 
Clearing [[Member]] 
Number
Y Y Y Y Y Y Y Y
452 Party Role 2 N 18 = Contra [[SFT]] 
Clearing [[Member]]
Y Y Y Y Y Y Y Y
448 Contra Entering / 
Executing [[Broker]]
8 A/N Market Mnemonic / 
MPID
N N N N N N N N
452 Party Role 2 N 37 = Contra Trader N N N N N N N N
448 Contra Introducing 
[[Broker]]
8
A/N Contra Introducing 
[[Broker]]
N N N N N N N N
452 Party Role 2 N 17 = Contra Firm N N N N N N N N
448 Contra Settling 
[[Broker]]
8 A/N [[NSCC]] [[participant]] 
Number
Y Y Y Y Y Y Y Y
452 Party Role 2 N 12 = Contra Settling 
Account 
Y Y Y Y Y Y Y Y
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 135

---

## Page 136

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
448 Submitted By 
Indicator
1 A/N l 0 = by Market
l 1 = by [[Buyer]]
[[participant]]
l 2 = by [[Seller]]
[[participant]]
Y Y Y Y Y Y Y Y
452 Party Role 2 N 36 = Entering Trader Y Y Y Y Y Y Y Y
81 [[SFT]] Transaction 
Type Code
1 A/N [[SFT]] Type Code:
l A = Pre-established
Bilateral Loan
l B = Buy-Side
l C = Cancel
l M = Rate
Modification
l N = New Loan
l R = Roll
l S = Send-to-Settle
l T = Terminate
Y Y Y Y Y Y Y Y
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 136

---

## Page 137

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
578 Source of 
Transaction / 
Market System
2 A/N Code which denotes the 
system at the market on 
which the execution 
occurred. Examples:
l S1 = submitted by
[[Member]] or buy-side
transaction
l S2 = submitted by
vendor
Y Y Y Y Y Y Y Y
825 Lending / Interest 
Rate Indicator
1 A/N Lending / Interest Rate 
Indicator:
l N = No Rate
l B = Paid to [[Borrower]]
l L = Paid to Lender
l space = N/A
Y Y Y Y Y N N N
381 Principal/Contract 
Loan Amount
17 N Unit Price x Share 
Quantity
16 Digits + 1 (period 
indicating two decimal 
point offset)
Y Y N Y Y N N N
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 137

---

## Page 138

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
581 Rounding Rule 
Code
1 A/N Indicates Rounding Rule 
for Settle Price 
Calculation:
l 0 = no rounding
l 1 = up to nearest
$0.01
l 2 = up to nearest
$0.05
l 3 = up to nearest
$0.10
l 4 = up to nearest
$0.25
l 5 = up to nearest
$1.00
Y Y N Y Y N N N
6 [[settlement]] Price 13 A/N Settle Price
12 Digits + 1 (period 
indicating two decimal 
point offset).
[Unit price * (1+ IA rate)] 
rounded as directed by 
Rounding Rule Code in 
Tag 581.
Y Y N Y Y N N N
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 138

---

## Page 139

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
118 [[settlement]] 
Amount 
17 N Principal Amount + 
Independent Amount
16 Digits + 1 (period 
indicating two decimal 
point offset)
Y Y N Y Y N N N
158 Lending / Interest 
Rate
10 N Rate for Interest Amount 
calculation. 
9 Digits + 1 (period 
indicating four decimal 
point offset)  
*Required for Tag
825=B or L.
Y* Y* Y* Y Y* N N N
159 Independent 
Amount Rate
10 N Rate for Independent 
Amount calculation. 
9 Digits + 1 (period 
indicating four decimal 
point offset)  
N N N N N N N N
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 139

---

## Page 140

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
920 Rebate Interest 
Amount
17 N Interest Amount paid 
overnight, calculated as  
(Lending Rate /100 * Net 
[[settlement]] Amt  * #days / 
360). 16 Digits + 1 
(period indicating two 
decimal point offset).
This calculation is only 
populated on output if a 
value of B = Buy-side is 
populated in Tag 71; 
otherwise, the tag is 
populated with 0.00.
N N N Y* 
off-leg 
only
N N N N
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 140

---

## Page 141

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
751 [[NSCC]] Reject 
Code
2 N l 00 = Accepted Trade
l 01 = Invalid
[[participant]] Info
l 02 = Invalid Trade
Date
l 03 = Invalid Security
l 04 = Invalid Quantity
l 05 = Invalid Price
l 06 = Invalid Trade
Source
l 07 = Invalid Market
l 09 = Invalid
Relationship
l 11 = Duplicate Trade
l 12 = Invalid Message
Type
l 13 = Invalid Trade
Type
l 14 = Invalid Sending
Entity
l 15 = Invalid Trade
Sequence Number
l 16 = Invalid
Submitted-by
Indicator
Y Y Y Y Y Y Y Y
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 141

---

## Page 142

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
l 21 = Invalid
[[settlement]] Date
l 23 = Invalid Trade
Amount
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 142

---

## Page 143

FIX 
Tag
Name Length Type Description New 
Loan
Pre-
established 
Bilateral 
Loan
Rate 
Modification
Buy-
Side
Roll Send-
to-
Settle
Cancel Terminate
751 [[NSCC]] Reject 
Code
(Continued)
2 N
l 54 = Missed Cutoff
l 55 = Invalid Rate
l 56 = Invalid Loan
Status
l 57 = Invalid [[DTCC]]
reference [[ID]]
l 58 = Invalid
Transaction Type
l 59 = Invalid
Rounding Rule
Indicator
l 60 = Security
Undergoing
Corporate Action
l 61 = Loan is
ineligible for the
request due to a
recall action
Y Y Y Y Y Y Y Y
TRAILER (Y=Required / N=Optional)
10 Check Sum 3 A/N Generated by FIX. Y Y Y Y Y Y Y Y
Table A.3  UTC Output FIX / MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 143

---

## Page 144

UTC Outbound Gap Fill Request FIX/MQ Format
The following table provides the UTC outbound gap fill request for the FIX/MQ format:
FIX 
Tag
Name Length Type Description Y=Required / 
N=Optional
HEADER FIX MQ 
8 Begin String 7 A/N Identifies the beginning of a new message generated by FIX.
[[default]] value: FIX.4.4
Y Y
9 Body Length 4 N Message length generated by FIX. Y N
35 Message Type 2 A/N AD = Trade Capture Report Request Y Y
49 Sender Comp 
[[ID]]
4 A/N Assigned value used to identify firm sending message. 
[[default]] value = [[NSCC]]
Y N
56 Target Comp 
[[ID]]
8 A/N Assigned value used to identify receiving firm message.
TBD for each Sending Entity.
Note: Not required for MQ.
Y N
115 Sending Entity 4 A/N Identifies the submitting source for which a trade message gap was detected by UTC. Y Y
34 Trade 
Sequence
9 N Unique message identifier generated by FIX.
Note: Not required for MQ.
Y N
DETAIL FIX MQ 
50 Sending 
Subsystem
3 A Sending subsystem for which a trade message gap was detected by UTC. Used in conjunction 
with Sending Entity and Trade Sequence Number for unique identification of trade message.
This tag is sent only if it is provided on input by the market on the UTC Common Trade Input 
format for this sending entity.
Y Y
52 Sending Time 21 A/N Timestamp generated by FIX. Y N
568 Trade Request 
[[ID]]
14 A/N Value: GapFillRequest’ Y Y
569 Trade request 
Type
1 N 3 = Unreported Trades Y Y
Table A.4  UTC Outbound Gap Fill Request FIX/MQ Format
[[SFT]] Clearing: General User Guide
A. Message Layouts 144

---

## Page 145

FIX 
Tag
Name Length Type Description Y=Required / 
N=Optional
571 Beginning 
Sequence 
Number
8 A/N Beginning Sequence Number of the Gap Y Y
818 Ending 
Sequence 
Number
8 A/N Ending Sequence Number of the Gap Y Y
TRAILER FIX MQ 
10 Check Sum 3 A/N Generated by FIX.
Not required through the MQ Interface.
Y Y
Table A.4  UTC Outbound Gap Fill Request FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 145

---

## Page 146

UTC Outbound [[EOD]] Confirmation to Market FIX/MQ Format
The following table provides the UTC outbound end of day confirmation to market for the FIX/MQ format:
FIX 
Tag
Name Length Type Description Y=Required / 
N=Optional
HEADER 
8 Begin String 7 A/N Identifies the beginning of a new message generated by FIX.
[[default]] Value: FIX.4.4
Y
9 Body Length 4 N Message length generated by FIX. Y
35 Message Type 2 A/N h = Trading Session Status Y
56 Target Comp [[ID]] 8 A/N Assigned value used to identify receiving firm message.
[[default]] value: [[NSCC]]
Y
115 Sending Entity 4 A/N Assigned value used to identify the sending entity from which [[NSCC]] had 
received trade data during the day.
Value predetermined by [[NSCC]].
Y
97 PossResend 1 A/N Indicates that the message may contain information that has been sent under 
another sequence number.
l N = OrigTrans
l Y = PossResend
Y
34 Message Identifier
(Msg Seq Num)
9 N Unique message identifier generated by FIX.
May not arrive in sequence number order when transmitted over MQ.
Y
52 Sending Time 21 A/N Timestamp generated by FIX. Y
49 Sender Comp [[ID]] 4 A/N Assigned value used to identify firm sending message.
Possible value = [[NSCC]].
Y
DETAIL
336 Trading Session [[ID]] 12 A/N NSCCTOMARKET Y
340 Trading Session Status 1 A/N 3 = Closed Y
Table A.5  UTC Outbound [[EOD]] Confirmation to Market FIX/MQ Format
[[SFT]] Clearing: General User Guide
A. Message Layouts 146

---

## Page 147

FIX 
Tag
Name Length Type Description Y=Required / 
N=Optional
58 Process Date 8 N UTC process date. Y
20001 Balance Indicator 1 A/N
l Y = In balance
l N = Out of balance
Y
20002 [[NSCC]] Processing Total 9 N [[SFT]] records counter for the sending entity, including  valid and rejected 
transactions processed by [[NSCC]].
Y
387 Sending Entity Processing Total 8 N Number of [[Stock]] Loan records sent to UTC from the Sending Entity during the 
day and reported in the sending entity in the Good Night message.
Y
TRAILER
10 Check Sum 3 A/N FIX tag 10 is provided on all end of day messages. Y
Table A.5  UTC Outbound [[EOD]] Confirmation to Market FIX/MQ Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 147

---

## Page 148

UTC Outbound Buy-Side Cutoff FIX/MQ Format (3:00 P.M. ET)
The following table provides the UTC outbound buy-side cutoff  for the FIX/MQ format (3:00 P.M. Eastern Time):
FIX Tag Name Length Type Description Y=Required / N=Optional
HEADER FIX MQ 
8 Begin String 7 A/N Identifies the beginning of a new message 
generated by FIX.
[[default]] value: FIX.4.4
Y Y
9 Body Length 4 N Message length generated by FIX. Y N
35 Message Type 2 A/N B = News Y Y
49 Sender Comp [[ID]] 4 A/N Assigned value used to identify firm 
sending message. 
[[default]] value = [[NSCC]]
Y N
56 Target Comp [[ID]] 8 A/N Receiving Sponsor [[Member]] [[ID]] 
Example 00000111
Y Y
34 Trade Sequence 9 N Unique message identifier generated by 
FIX.
Note: Not required for MQ.
Y N
52 Sending Time 21 A/N Timestamp generated by FIX.
Note: Not required for MQ.
Y N
Detail FIX MQ 
148 Headline 8 A/N Current date in YYYYMMDD format Y Y
33 No lines of text. 1 N Value 1 Y Y
58 Text 47 A/N Body of the message:
Release maturing buy-side off-legs from 
[[Margin]].
Y Y
TRAILER FIX MQ 
10 Check Sum 3 A/N Generated by FIX. Y Y
[[SFT]] Clearing: General User Guide
A. Message Layouts 148

---

## Page 149

UTC Outbound [[EOD]] Messages to Participants by Market
The following table provides the UTC outbound end of day messages to participants by market:
FIX Tag Name Length Type Description Y=Required / N=Optional
HEADER FIX MQ 
8 Begin String 7 A/N Identifies the beginning of a new message 
generated by FIX.
[[default]] value: FIX.4.4
Y Y
9 Body Length 4 N Message length generated by FIX. Y N
35 Message Type 2 A/N h = Trading Session Status Y Y
49 Sender Comp [[ID]] 4 A/N Assigned value used to identify firm sending 
message. 
[[default]] value = [[NSCC]]
Y N
56 Target Comp [[ID]] 8 A/N Receiving [[SFT]] Clearing [[Member]] Account 
Number.
Example: 00000111
Y Y
34 Trade Sequence 9 N Unique message identifier generated by FIX.
Note: Not required for MQ.
Y N
52 Sending Time 21 A/N Timestamp generated by FIX.
Note: Not required for MQ.
Y N
DETAIL FIX MQ 
336 Trading Session [[ID]] 12 A/N NSCCTOPARTIC Y Y
340 Trade Session Status 1 A/N 5 = PreClose Y Y
58 Process Date 8 A/N Process Date YYYYMMDD Y Y
20003 Region Name 5 A/N Example: USA Y Y
20004 Market 5 A/N UTC market code. 
Example: 200
Y Y
Table A.6  UTC Outbound [[EOD]] Messages to Participants by Market
[[SFT]] Clearing: General User Guide
A. Message Layouts 149

---

## Page 150

FIX Tag Name Length Type Description Y=Required / N=Optional
387 Processing Total for a Market 9 N Total number of trades processed by UTC for 
the [[participant]], including valid and rejected 
trades
Y Y
20005 Number of Repeating Group Tags 2 N Number of Currency Totals 1 Y Y
20006 Currency Code 3 A/N Example: USD Y Y
20007 Valid Trade Total 9 N Number of valid trades processed by UTC for 
the [[participant]] and currency.
Y Y
20008 Valid Share Quantity Total 13 N Total Share Quantity in valid trades 
processed by UTC for the [[participant]] and 
currency.
Y Y
20009 Valid Contract Amount Total 16 N Total Contract Amount in valid trades 
processed by UTC for the [[participant]] and 
currency.
Y Y
TRAILER FIX MQ 
10 Check Sum 3 A/N Generated by FIX. Y Y
Table A.6  UTC Outbound [[EOD]] Messages to Participants by Market (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 150

---

## Page 151

UTC Reject Codes
The following table provides the UTC reject codes:
Code and Description Possible Cause
00 = Accepted Trade Transaction passed all validations and accepted for [[DTCC]] processing.
01 = Invalid [[participant]] Info l One or both [[SFT]] participants were not submitted.
l One or both submitted [[SFT]] participants are not valid for the [[SFT]] Clearing transaction.
02 = Invalid Trade Date l Submitted Trade date (FIX Tag 75) is not current process date.
l [[SFT]] submitted on a Bank holiday.
03 = Invalid Security l Security (FIX Tag 48) was not submitted the [[SFT]] Clearing transaction.
l Submitted security is not an [[Equity]] or an [[Equity]] that is eligible for [[SFT]] Clearing processing.
l Submitted security has an invalid trading status, inactive, or not found in [[DTCC]] Security Master tables.
l Security is ineligible for [[CNS]] or has a [[DTC]] Deliver Order ([[DO]]) chill.
l Submitted security for a Roll [[SFT]] Transaction (R) or Send-to-Settle [[SFT]] transaction (S) does not match the
security of the outstanding off-leg return.
04 = Invalid Quantity l [[shares]] (FIX Tag 32) were not submitted for  the [[SFT]] transaction type.
l [[shares]] submitted for the [[SFT]] transaction type exceeds threshold of 999,999,999.
l [[shares]] submitted for the [[SFT]] Roll transaction (R) is not equal or less than the [[shares]] of the outstanding off-leg
return.
l [[shares]] submitted for the [[SFT]] Cancel transaction (C) which is to cancel a [[DO]] off-leg return is not equal to the
same [[shares]] of the previously submitted [[SFT]] Send-to-Settle transaction (S).
l [[shares]] submitted for the [[SFT]] Cancel transaction (C) which is to cancel an on-leg is not equal to the same
[[shares]] of the previous submitted on-leg.
l [[shares]] submitted for the [[SFT]] Send-to-Settle transaction (S) which is for an outstanding off-leg return with a
[[settlement]] date of the next business date is not equal or less than the [[shares]] of the outstanding off-leg return.
l [[shares]] submitted for the [[SFT]] Send-to-Settle transaction (S) which is for an outstanding off-leg return with a
[[settlement]] date of the current business date is not equal to the same [[shares]] of the outstanding off-leg return.
05 = Invalid Price
l Price (FIX Tag 31) submitted for the [[SFT]] transaction is less than the minimum price allowed ($5.00).
l Market closing price for the submitted [[SFT]] transaction is less than the minimum allowed ($5.00).
06 = Invalid Trade Source Source of the Transaction / Market System (FIX Tag 578) was not submitted or invalid.
[[SFT]] Clearing: General User Guide
A. Message Layouts 151

---

## Page 152

Code and Description Possible Cause
07 = Invalid Market l Market Code (FIX Tag 30) is not submitted.
l Submitted Market Code is not defined in UTC.
l Submitted Market Code is not eligible for [[SFT]] Clearing.
08 = Multiple Rejects Not applicable for [[SFT]] Clearing.
09 = Invalid Relationship For Buy-side submitted [[SFT]] transaction type (B), the Sponsor-sponsored relationship is not valid.
11 = Duplicate Trade Not applicable for [[SFT]] Clearing. Will be bypassed, and not reported back to the sender.
12 = Invalid Message Type Not applicable for [[SFT]] Clearing.
13 = Invalid Trade Type Not applicable for [[SFT]] Clearing.
14 = Invalid Sending Entity l Sending Entity is not defined in UTC.
l Sending Entity / Market / Market Source / Submitting [[participant]] relationship is not defined in UTC database.
15 = Invalid Trade Sequence 
Number
Sequence Number (FIX Tag 571) was not submitted or not numeric.
16 = Invalid Submitted-by Indicator l Submitted-by Indicator (FIX Tag 448) was not submitted.
l Submitted submitted-by indicator is not 0, 1, or 2.
l Submitted-by Indicator is 0 for [[participant]] type of Sending Entity.
21 = Invalid [[settlement]] Date [[settlement]] date is not equal to current [[settlement]] date for submitted [[SFT]] transaction
23 = Invalid Trade Amount Calculated [[settlement]] Amount for submitted [[SFT]] transaction exceeds threshold 9,999,999,999.99.
25 = Invalid Currency Code Not applicable for [[SFT]].
27 = Other Not applicable for [[SFT]].
54 = Missed Cutoff Submitted [[SFT]] transaction received after cutoff.
[[SFT]] Clearing: General User Guide
A. Message Layouts 152

---

## Page 153

Code and Description Possible Cause
55 = Invalid Rate l Lending Rate Indicator (FIX Tag825) was not submitted or invalid for submitted [[SFT]] transaction.
l Lending Rate (FIX Tag158) was not submitted or not numeric for [[SFT]] transaction and submitted Lending Rate
Indicator has value of B or L.
l Lending Rate (FIX Tag158) was submitted and greater than zero for [[SFT]] transaction and submitted Lending
Rate Indicator has value of N.
l Both submitted Lending Rate and Lending Rate Indicator in Rate Modification [[SFT]] (M) match the rate and the
indicator in the original loan.
l Submitted Independent Amount Rate for a Roll [[SFT]] (R) does not match the rate in the original loan.
l IA rate (Fix Tag 159) that was submitted was invalid or not numeric for [[SFT]] transaction.
56 = Invalid loan status Off-leg return in SAS database has invalid status for submitted [[SFT]] transaction. 
57 = Invalid [[DTCC]] Reference [[ID]] l [[DTCC]] Loan Reference [[ID]] (FIX Tag526) was not submitted for the [[SFT]] transaction.
l Submitted [[DTCC]] Loan Reference [[ID]] (FIX Tag526) was not submitted for a [[SFT]] is not found in the SAS
database.
58 = Invalid Transaction Type [[SFT]] Type (FIX Tag81) was not submitted or invalid 
59 = Invalid Rounding Rule Indicator Rounding Rule Indicator (FIX Tag581) was not submitted or invalid for New loan or Roll [[SFT]] (A, N, or R).
60 = Security Undergoing Corporate 
Action
Security submitted for New Loan [[SFT]] transaction type (N or A) or Roll [[SFT]] transaction type (R) is undergoing a 
corporate action.
61 = [[DTCC]] Reference [[ID]] has a 
Recall
Submitted Roll [[SFT]] transaction (R) for [[DTCC]] Reference [[ID]] has a recall.
[[SFT]] Clearing: General User Guide
A. Message Layouts 153

---

## Page 154

A.4 SAS ISO Message Output
The SAS system uses the following message types:  MT548 and MT547/545.  MT548 is a status UPDATE message.  The MT548 ISO message is 
generated by the SAS system, which keeps track of outstanding SFTs.  This message is only generated after a new [[SFT]] is received and accepted by the 
UTC trade capture system first and then forwarded to SAS for processing.  The SAS system uses this message to update message subscribers (for 
example, submitting entities as well as counterparties to the [[SFT]]) about changes to the status of their [[SFT]].  These updates can include events such as 
pending, terminated, etc.
MT545 and MT547 are both MADE messages.  The MT547 MADE message is for the DELIVERER only, and the MT545 MADE message is for the 
RECEIVER.  The MT547/545 messages are generated from the SAS system, which uses them to communicate with message subscribers when MADEs 
are done.  The MT545/547 messages are also used for the rate modification purpose.  The Common Data Transfer Services (CDTS) product is 
CNSESFTO.
The following table provides an overview for SAS ISO messages:
Field Name Description / Values MT548 MT547/545 Rate Mod. 
(MT547/545)
Process/Message Timestamp Application process timestamp 
Format: ccyymmddhhmmss
X X X
[[DTCC]] Reference [[ID]] Loan reference [[ID]] assigned by UTC when new, Pre-established Bilateral Loan, 
buy-side, or roll loan transaction is received. Will be populated with previously 
assigned [[ID]] for rate modification, send-to-settle and termination message.
Format: YYMMDD of current date + eight digit sequence number.
X X X
Client Order [[ID]] Client Assigned Number on Buy or Sell side X X X
Execution [[ID]] Client Assigned (Vendor) Buy or Sell Execution [[ID]] X X X
[[SFT]] Trade Date Should always be the current date. X X X
[[SFT]] [[settlement]] Date Next Day [[settlement]] for off-leg transactions, current date for others. X X X
[[SFT]] Clearing: General User Guide
A. Message Layouts 154

---

## Page 155

Field Name Description / Values MT548 MT547/545 Rate Mod. 
(MT547/545)
[[SFT]] Transaction Type Code Values:
l NEWS - Pre-established Bilateral Loan
l NEWL - New Loan
l RMOD - Rate Modification
(applicable only for MT547/545)
l ROLL - Roll
l SNDS - Send-to-Settle
l TERN - [[NSCC]] Termination
(applicable only for MT547/545)
l TERC - Loan Termination
(applicable only for MT547/545)
l NROL - No Roll
l CANC - Canceled by Client
l PDIF - Price Differential
([[NSCC]] Initiated)
l NRCA - No Roll & Corporate Action
(applicable only in combination with specific corporate action)
l BEXE - Buy-In Execution
(applicable only for MT547/545)
l BKRO - [[Broker]] Re-Org
X X X
[[SFT]] Clearing: General User Guide
A. Message Layouts 155

---

## Page 156

Field Name Description / Values MT548 MT547/545 Rate Mod. 
(MT547/545)
[[SFT]] Status Code Values:
l PEND - Pending (in SAS pending off-let return)
l DROP - Dropped
l CANC - Canceled
l NRET - Non Return Fail
l TERN - Terminated by [[NSCC]]
l TERC - Terminated by Client
l RJCT - Rejected
l MADE - On-leg Settled
X Not 
Applicable 
since it is 
only for 
MADE.
Not 
Applicable 
since it is only 
for MADE.
Leg Indicator Values: 
l ONLG - On-leg
l OFFL - Off-leg
l OTHR – Other value
X X X
Security ISIN [[ID]] Security [[ID]] in a ISIN format. No spot X No spot
Security [[CUSIP]] [[ID]] Security [[ID]] in a [[CUSIP]] format. X X X
Buy [[participant]] [[settlement]] [[ID]] [[NSCC]] identifier of the Original Buy [[participant]]. X X X
Buy [[participant]] [[SFT]] [[ID]] [[NSCC]] identifier of the Original Buy [[participant]] - [[SFT]] account. X X X
Sell [[participant]] [[settlement]] [[ID]] [[NSCC]] identifier of the Original Sell [[participant]]. X X X
Sell [[participant]] [[SFT]] [[ID]] [[NSCC]] identifier of the Original Sell [[participant]] - [[SFT]] account. X X X
Number of [[shares]] Quantity of [[shares]] being traded. X X N/A
Share Price Price per share of the transaction. No spot X No spot
Lending Rate Indicator Values:
l NRTE - No Rate
l LEND - Paid to Lender of security
l BRRW - Paid to [[Borrower]] of security
X X X
[[SFT]] Clearing: General User Guide
A. Message Layouts 156

---

## Page 157

Field Name Description / Values MT548 MT547/545 Rate Mod. 
(MT547/545)
Lending Rate Interest / Lending Rate in percent (%) No spot X Repurpose 
the Number 
of [[shares]] 
field.
AMOR 
qualifier.
Independent Amount Rate Rate to calculate Independent Amount for the transaction in percent (%). No spot X No spot
Contract Amount in USD Calculated as Price x [[shares]] X X N/A
Lending/Interest Amount Lending / Interest Amount No spot X Repurpose 
the Contract 
Amount field
Rebate Interest Amount Overnight Rebate Interest No spot X No spot
[[settlement]] Amount Calculated as 
Contract Amount + Independent Amount
X X X
[[SFT]] Activity Type Value:
STKL - [[Stock]] Loan
X X X
Rounding Value Values:
l NRND - No Rounding
l RND1 - Rounded to nearest $0.01
l RND2 - Rounded to nearest $0.05
l RND3 - Rounded to nearest $0.10
l RND4 - Rounded to the nearest $0.25
l RND5 - Rounded to the nearest $1.00
X X X
[[SFT]] Clearing: General User Guide
A. Message Layouts 157

---

## Page 158

Field Name Description / Values MT548 MT547/545 Rate Mod. 
(MT547/545)
Corporate Actions Indicator Values:
l CPAN - Not Undergoing a Corporate Action
l CAUN - Undergoing a Non-supported Corporate Action
l FSSP - Forward [[Stock]] Split
l RSSP - Reverse [[Stock]] Split
l CHMR - Cash Merger
l STMR - [[Stock]] Merger
l CSMR - Cash and [[Stock]] Merger
l NMCG - Name Change
X X N/A
Free-Form Text Comments Reserved for future use. X X X
Rate Modification Indicator Values:
l UIND - Interest was Updated (refer to the Lending/Interest Amount field).
l PRTY - Parties were Updated (refer to the Lending Rate Indicator field).
l BOTH - Interest & Parties Updated (refer to both the Lending/Interest Amount
and Lending Rate Indicator fields).
N/A X X
Sending Entity [[ID]] [[NSCC]] identifier of the Sending Entity (Vendor). X X X
Recall Counter Number of recalls associated. X X N/A
Recall Total Quantity Total quantity of the associated recalls. X X N/A
[[SFT]] Clearing: General User Guide
A. Message Layouts 158

---

## Page 159

A.5 [[DTC]] Input and Output Messages
The following table provide links for the [[DTC]] input messages:
Note
To access the input and output messaging, including the Proprietary [[DO]], ISO [[DO]] Input, DTF [[DO]] Output, MQ [[DO]] Output, MQ PO Output, and ISO Output 
Message files, see the [[CCF]] [[settlement]] files available at:
https://www.[[DTCC]].com/[[settlement]]-and-[[Asset]]-services/[[settlement]]/[[CCF]]-new-[[settlement]] 
Message Type Format Message Type Comments
Deliver Order Input File
(DOI1/DOI5)
Proprietary l MQ
l FTP
l NDM
Modified to include [[SFT]] DOs (reason code 200, receiver 881 and cross reference in comments)
Deliver Orders 
(DOX1/DOX5)
Proprietary 
l MQ
l FTP
l NDM
Modified to include [[SFT]] DOs (reason code 200, receiver 881 and cross reference in comments)
Deliver Order Input ISO MT543 Modified to include [[SFT]] DOs (reason code 200, receiver 881 and cross reference in comments)
Table A.7  [[DTC]] Input Messages
[[SFT]] Clearing: General User Guide
A. Message Layouts 159

---

## Page 160

The following table provide links for the [[DTC]] output messages:
Message Type Format Message Type Comments
[[settlement]] [[participant]] Activity 
(DTFPART)
DTF MQ Modified to accommodate [[SFT]] DOs.
[[settlement]] Status ISO l MT545
l MT547
l MT548
Modified to accommodate all [[SFT]] activity.
[[settlement]] [[participant]] Activity 
(PARTPO) 
DTF MQ Modified to accommodate [[SFT]] POs.
Proprietary Output Proprietary SMART Modified to include [[SFT]] DOs and POs.
[[SFT]] Drop File Drops MT548 Modified to include proprietary and ISO drops (TBD).
Table A.8  [[DTC]] Output Messages
[[SFT]] Clearing: General User Guide
A. Message Layouts 160

---

## Page 161

A.6  MT548 Message Format
The following table shows the [[SFT]] Clearing MT548 message format:
MT548 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:16R:GENL N/A
:20C::SEME//xxxxxxxxxxxxxxxx [[DTCC]] generated. Used to track transaction from submission to final state. Char 16 N/A
:23G:INST N/A
:98C::PREP//ccyymmddhhmmss Application process timestamp Char 14 N/A
:16R:LINK N/A
:20C::RELA//xxxxxxxxxxxxxx [[DTCC]] Reference D assigned by UTC when new, new already settled, buy-
side, or roll loan transaction is received.
Format: YYMMDD of current date + eight-digit sequence number.
Char 14 Tag 526
:16S:LINK N/A
:16R:LINK N/A
:20C::TRRF//xxxxxxxxxxxxxx l Client Order [[ID]] assigned by the [[Buyer]] or [[Seller]].
l Only the first 16  out of 32 bytes are displayed.
l If greater than 16 bytes, the whole [[ID]] displays in the 70E SPRO field.
Char 16 Tag 11
:16S:LINK N/A
:16R:LINK N/A
:20C::COMM//xxxxxxxxxxxxxx l Execution (Vendor) [[ID]] assigned by the [[Buyer]] or [[Seller]].
l Only the first 16  out of 32 bytes are displayed.
l If greater than 16 bytes, the whole [[ID]] displays in the 70E SPRO field.
Char 16 Tag 66
:16S:LINK N/A
:16R:STAT N/A
Table A.9  MT548 Message Format
[[SFT]] Clearing: General User Guide
A. Message Layouts 161

---

## Page 162

MT548 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:25D:SETT/DTCY/xxxx [[SFT]] status code.
Values:
l PEND – Pending (processed by [[CNS]])
l DROP – Dropped
l CANC – Canceled
l NRET – Non-return Fail
l RJCT – Rejected
l MADE – On-leg Settled
l TERC – Terminated by Client
l TERN – Terminated by [[NSCC]]
Char 4 N/A
:16S:STAT N/A
:16S:GENL N/A
:16R:SETTRAN N/A
:35B:/US/XXXXXXXXX [[CUSIP]] Char 9 l Tag 48
(if Tag 22 = 4)
l N/A
(if Tag 22=1)
l :36B::SETT//UNIT/00000000000,0
- or -
l :36B::SETT//AMOR/00000,0000
l Quantity of [[shares]] being traded.
- or -
l Share quantity or lending rate. The  AMOR qualifier is used only when the
Transaction Type = RMOD.
9(11)
- or -
If AMOR, use
PIC 9(5).9(4)
Tag 32              
(Share Quantity)
-
or -
Tag 158
(Lending Rate)
:36B::SETT//FAMT/00000000000,0 Recall Total Quantity 9(11)
Table A.9  MT548 Message Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 162

---

## Page 163

MT548 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:19A::OCMT//USD000000000000,00 Contract amount, which is calculated as Price x [[shares]] (UNIT).
-
or -
Interest amount (AMOR).
9(12).9(2) N/A
:19A::SETT//USD000000000000,00 [[settlement]] Amount
Calculated as Contract Amount + Independent Amount
9(12).9(2) N/A
:97A::SAFE//xxxxxxx [[Seller]] for On-leg and [[Buyer]] for Off-leg
Identifies account where financial instruments are maintained. 
(On-leg = Lender, Off-leg = [[Borrower]])
Char 8 N/A
:22F::SETR/DTCYREAS/xxxx Leg indicator.
Values:
l ONLG – On-leg
l OFFL – Off-leg
l OTHR – Other value
Char 4 N/A
:22H::REDE//xxxx Values:
l DELI – Used if you are the deliverer of [[shares]] at [[DTC]].
l RECE – Used if you are the receiver of [[shares]] at [[DTC]].
Char 4 N/A
:22H::PAYM//xxxx Values:
l APMT – For valued transactions.
l FREE – For free transactions.
Char 4 N/A
Table A.9  MT548 Message Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 163

---

## Page 164

MT548 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:22F::STCO/DTCYTXNT/xxxx Transaction type.
Values:
l BKRO - [[Broker]] Re-Org
l CANC – Canceled by Client
l NEWS – Pre-established Bilateral Loan
l NEWL – New Loan
l NRCA - No Roll & Corporate Action
l NROL – No Roll
l PDIF – Price Differential
l ROLL – Roll
l RMOD – Rate Modification
l SNDS – Send-to-Settle
Char 4 Tag 81
(where applicable)
:22F::STCO/DTCYACTV/xxxx Activity type.
Value: 
STKL - [[Stock]] Loan
Char 4 N/A
:22F::STCO/DTCYDGCA/xxxx Values:
l CPAN – Not Undergoing a Corporate Action
l CAUN - Undergoing a Non-supported Corporate Action
l FSSP - Forward [[Stock]] Split
l RSSP - Reverse [[Stock]] Split
l CHMR - Cash Merger
l STMR - [[Stock]] Merger
l CSMR - Cash and [[Stock]] Merger
l NMCG - Name Change
Char 4 N/A
:22F::BLOC/DTCY/xxxx Recall Counter Char 4
Table A.9  MT548 Message Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 164

---

## Page 165

MT548 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:22F::SETS/DTCY/xxxx Interest/Lending Rate indicator.
Values:
l NRTE – No Rate
l LEND – Paid to the Lender of the security
l BRRW – Paid to the [[Borrower]] of the security
Char 4 Tag 825
:22F::COLA/DTCY/xxxx Rounding Values:
l NRND – No Rounding
l RND1 – Rounded to nearest $0.01
l RND2 – Rounded to nearest $0.05
l RND3 – Rounded to nearest $0.10
l RND4 – Rounded to the nearest $0.25
l RND5 - Rounded to the nearest $1.00
Char 4 Tag 581
:98A::SETT//ccyymmdd [[SFT]] [[settlement]] date. 
Next Day [[settlement]] for off-leg transactions, current date for others.
Char 8 N/A
:98A::TRAD//ccyymmdd [[SFT]] trade date. 
Should always be the current date. 
Char 8 Tag 75
:70E::SPRO//xxxxxxxxxxxxxxxxetc. Reserved for future use. Char 35*10 N/A
:16R:SETPRTY
N/A
:95Q::BUYR//xxxxxxxx [[NSCC]] identifier of the Original Buy [[participant]] – [[settlement]] account. For 
example, if the on-leg- [[Borrower]] is the [[Buyer]], the lender is the [[Seller]]; If the 
off-leg- lender is the [[Buyer]], the [[Borrower]] is the [[Seller]].
Char 8 Tag 448                                 
(with Tag 452 = 04)
:16S:SETPRTY
N/A
:16R:SETPRTY N/A
Table A.9  MT548 Message Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 165

---

## Page 166

MT548 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:95R::DEAG/DTCYPART/xxxxxxxx [[NSCC]] identifier of the Original Buy [[participant]] – [[SFT]] account. For example, 
if the on-leg- [[Borrower]] is the [[Buyer]], the lender is the [[Seller]]. If the off-leg- 
lender is the [[Buyer]], the [[Borrower]] is the [[Seller]].
Char 8 N/A
:16S:SETPRTY
N/A
:16R:SETPRTY N/A
:95Q::DEI1//xxxx [[NSCC]] identifier of the Sending Entity (vendor). Char 4 Tag 115
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95Q::SELL//xxxxxxxx [[NSCC]] identifier of the Original Sell [[participant]] – [[settlement]] account.  For 
example, if the on-leg- [[Borrower]] is the [[Buyer]], the lender is the [[Seller]]; If the 
off-leg- lender is the [[Buyer]], the [[Borrower]] is the [[Seller]].
Char 8 Tag 448 
(with Tag 452 =04)
:16S:SETPRTY
N/A
:16R:SETPRTY N/A
:95R::REAG/DTCYPART/xxxxxxxx [[NSCC]] identifier of the Original Sell [[participant]] – [[SFT]] account. For example, 
if the on-leg- [[Borrower]] is the [[Buyer]], the lender is the [[Seller]]; If the off-leg- 
lender is the [[Buyer]], the [[Borrower]] is the [[Seller]].
Char 8 N/A
:16S:SETPRTY
N/A
:16R:SETPRTY N/A
:95P::PSET//DTCYUS33 Place of [[settlement]] Char 8 N/A
:16S:SETPRTY N/A
:16S:SETTRAN N/A
Table A.9  MT548 Message Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 166

---

## Page 167

A.7 MT547/MT545 (Inclusive of Rate Modification) Message Format
The following table shows the message format for MT547/545, inclusive of the rate modification:
MT547/MT545 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:16R:GENL N/A
:20C::SEME//xxxxxxxxxxxxxxxx [[DTCC]] generated. Used to track transaction from submission to final state. Char 16 N/A
:23G:NEWM N/A
:98C::PREP//ccyymmddhhmmss Application process timestamp. Char 14 N/A
:16R:LINK N/A
:20C::RELA//xxxxxxxxxxxxxx [[DTCC]] Reference [[ID]] assigned by UTC for the transaction that is MADE.
Format: YYMMDD of current date + eight-digit sequence number.
Char 14 Tag 526
:16S:LINK
N/A
:16R:LINK N/A
:20C::TRRF//xxxxxxxxxxxxxx l Client Order [[ID]] assigned by the [[Buyer]] or [[Seller]].
l Only the first 16  out of 32 bytes are displayed.
l If greater than 16 bytes, the whole [[ID]] is displayed
l in the 70E SPRO field.
Char 16 Tag 11
:16S:LINK N/A
:16R:LINK N/A
:20C::COMM//xxxxxxxxxxxxxx l Execution (Vendor) [[ID]] assigned by the [[Buyer]] or [[Seller]].
l Only the first 16  out of 32 bytes are displayed.
l If greater than 16 bytes, the whole [[ID]] displays in the 70E SPRO field.
Char 16 Tag 66
:16S:LINK N/A
:16S:GENL N/A
:16R:TRADDET N/A
Table A.10  MT547/MT545 (Inclusive of Rate Modification) Message Format
[[SFT]] Clearing: General User Guide
A. Message Layouts 167

---

## Page 168

MT547/MT545 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:98A::TRAD//ccyymmdd [[SFT]] trade date. 
Should always be the current date. 
Char 8 Tag 75
:98A::ESET//ccyymmdd [[SFT]] [[settlement]] date.
Next Day [[settlement]] for Off-Leg transactions, current date for others.
Char 8 N/A
:90A::DEAL//ACTU/USD000000,00000 Price per share of the transaction. 9(6).9(5) Tag 31
:35B:ISIN XXXXXXXXXXXX ISIN [[ID]] Char 12
l Tag 48                    (if Tag 22
= 4)
l N/A  (if Tag
22=1)
:16R:FIA
N/A
:92A::CUFC//00000,0000 Rate to calculate the Independent Amount for the transaction in percent 
(%).
9(5).9(4) Tag 159
:92A::INTR//00000,0000 Interest/Lending Rate is in percent (%).
This field is populated only when [[SFT]] Transaction Type is RMOD for Rate 
Modification.
9(5).9(4) Tag 158
:35B:/US/XXXXXXXXX [[CUSIP]] Char 9 l Tag 48
(if Tag 22 = 1)
l N/A  (if Tag
22=4)
:16S:FIA
N/A
:70E::SPRO//xxxxxxxxxxxxxxxxetc. Reserved for future use. Char 35*10 N/A
:16S:TRADDET N/A
:16R:FIAC N/A
:36B::ESTT//UNIT/00000000000,0 Quantity of [[shares]] being traded. 9(11) Tag 32
:36B::RSTT//UNIT/00000000000,0 Recall Total Quantity 9(11)
Table A.10  MT547/MT545 (Inclusive of Rate Modification) Message Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 168

---

## Page 169

MT547/MT545 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:97A::SAFE//xxxxxxxx [[Seller]] for on-leg and [[Buyer]] for off-leg.
Identifies account where the financial instruments are maintained.
Char 8 N/A
:16S:FIAC
N/A
:16R:SETDET N/A
:22F::STCO/DTCYTXNT/xxxx [[SFT]] Transaction Type.
Values:
l BEXE – Buy-in Execution
l BKRO – [[Broker]] Reorg
l CANC – Canceled by Client
l NEWL – New Loan
l NEWS – Pre-established Bilateral Loan
l NROL – No Roll
l NRCA – No Roll & Corporate Action
l PDIF – Price Differential
l RMOD – Rate Modification
l ROLL – Roll
l SNDS – Send-to-Settle
l TERC – Loan Termination
l TERN – [[NSCC]] Termination
Char 4 Tag 81
:22F::STCO/DTCYACTV/xxxx Activity Type
Value: STKL – [[Stock]] Loan
Char 4 N/A
Table A.10  MT547/MT545 (Inclusive of Rate Modification) Message Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 169

---

## Page 170

MT547/MT545 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:22F::STCO/DTCYDGCA/xxxx Values:
l CAUN - Undergoing a Non-supported Corporate Action
l CHMR - Cash Merger
l CPAN – Not Undergoing a Corporate Action
l CSMR - Cash and [[Stock]] Merger
l FSSP - Forward [[Stock]] Split
l NMCG - Name Change
l RSSP - Reverse [[Stock]] Split
l STMR - [[Stock]] Merger
Char 4 N/A
:22F::STCO/DTCY/xxxx This field is displayed only when the Transaction Type is RMOD for Rate 
Modification.
Values:
l UIND – Interest was updated (refer to field Lending/Interest Amount).
l PRTY – Parties were updated (refer to field Lending Rate Indicator).
l BOTH – Interest and parties were updated (refer to both fields
Lending/Interest Amount & Lending Rate Indicator).
Char 4 N/A
:22F::SETR/DTCY/xxxx Leg Indicator
Values: 
l ONLG – On-leg
l OFFL – Off-leg
l OTHR – Other value
Char 4 N/A
:22F::BLOC/DTCY/xxxx Recall Counter Char 4
Table A.10  MT547/MT545 (Inclusive of Rate Modification) Message Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 170

---

## Page 171

MT547/MT545 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:22F::SETS/DTCY/xxxx Interest/Lending Rate Indicator 
Values:
l NRTE – No Rate
l LEND – Paid to Lender of security
l BRRW – Paid to [[Borrower]] of security
Char 4 Tag 825
:22F::COLA/DTCY/xxxx Rounding Values:
l NRND – No Rounding
l RND1 – Rounded to nearest $0.01
l RND2 – Rounded to nearest $0.05
l RND3 – Rounded to nearest $0.10
l RND4 – Rounded to the nearest $0.25
l RND5 - Rounded to the nearest $1.00
Char 4 Tag 581
:16R:SETPRTY N/A
:95Q::BUYR//xxxxxxxx [[NSCC]] identifier of the Original Buy [[participant]] – [[settlement]] Account. Char 8 Tag 448 
(with Tag 452 = 04)
:16S:SETPRTY
N/A
:16R:SETPRTY N/A
:95R::DEAG/DTCYPART/xxxxxxxx [[NSCC]] identifier of the Original Buy [[participant]] – [[SFT]] Account. Char 8 N/A
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95Q::DEI1//xxxx [[NSCC]] identifier of the Sending Entity (vendor). Char 4 Tag 115
:16S:SETPRTY N/A
:16R:SETPRTY N/A
Table A.10  MT547/MT545 (Inclusive of Rate Modification) Message Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 171

---

## Page 172

MT547/MT545 Description / Values Length of 
Data Field
Input Tag Number 
(if applicable)
:95Q::SELL//xxxxxxxx [[NSCC]] identifier of the Original Sell [[participant]] – [[settlement]] Account. Char 8 Tag 448                                 
(with Tag 452 = 04)
:16S:SETPRTY
N/A
:16R:SETPRTY N/A
:95R::REAG/DTCYPART/xxxxxxxx [[NSCC]] identifier of the Original Sell [[participant]] – [[SFT]] Account. Char 8 N/A
:16S:SETPRTY N/A
:16R:SETPRTY N/A
:95P::PSET//DTCYUS33 Place of [[settlement]] Char 8 N/A
:16S:SETPRTY N/A
:16R:AMT N/A
:19A::ACRU//USD000000000000,00 Lending / Interest Amount
Populated only when the Transaction Type is RMOD for Rate Modification.
9(12).9(2) N/A
:16S:AMT
N/A
:16R:AMT N/A
:19A::DEAL//USD000000000000,00 Contract Amount
Calculated as Price x [[shares]]
9(12).9(2) N/A
:16S:AMT
N/A
:16R:AMT N/A
:19A::ESTT//USD000000000000,00 [[settlement]] Amount
Calculated as Contract Amount + Independent Amount
9(12).9(2) N/A
:16S:AMT
N/A
:16R:AMT N/A
:19A::OTHR//USD000000000000,00 Independent amount. 9(12).9(2) N/A
:16S:AMT N/A
:16S:SETDET N/A
Table A.10  MT547/MT545 (Inclusive of Rate Modification) Message Format (Continued)
[[SFT]] Clearing: General User Guide
A. Message Layouts 172

---

## Page 173

A.8 MT542: Recall and Buy-In Input Message Formats
The following table shows the ISO MT542 input message formats for Recall and Buy-In transactions, CDTS Product -– CNSISOI. This message format will 
be used by the Approved [[SFT]] Submitter to input a recall, cancel recall, buy-in execution, or cancel buy-in execution message.
ISO Tag MT542 Input Values and Rules Length of Data 
Field
Mandatory Sequence A General Information
:16R:GENL Start of Block
:20C::SEME//xxxxxxxxxxxxxxxx Sender's reference number.
:23G:NEWM NEWM will be populated (New message).
Optional Repetitive Subsequence A1 Linkages
:16R:LINK Start of Block
:20C::RELA//xxxxxxxxxxxxxx [[DTCC]] Reference [[ID]] of the outstanding loan. 
Rule:
If not submitted, not found in [[NSCC]], or ineligible for the request, rejected with code 57.
Char 14
:16S:LINK End of Block
End of Subsequence A1 Linkages
Optional Repetitive Subsequence A1 Linkages
:16R:LINK Start of Block
[[SFT]] Clearing: General User Guide
A. Message Layouts 173

---

## Page 174

ISO Tag MT542 Input Values and Rules Length of Data 
Field
:20C::COMM//xx Recall [[ID]] or Buy-In [[ID]].
Rules:
l If not submitted for the required transaction types, CRCL=Cancel Recall or CBEX=
Cancel Buy-in Execution, rejected with code 09.
o Recall [[ID]] to be canceled for the CRCL=Cancel Recall message type.
o Reject with code 09 if it does not match any pending Recall in [[NSCC]].
l Buy-in Execution [[ID]] is canceled for the CBEX=Cancel Buy-in Execution message type.
o If  it does not match any pending Buy-In Execution in [[NSCC]], rejected with code 09.
o If submitted for the RCLL=Recall or BEXE=Buy-in Execution message type, [[NSCC]]
ignores.
Note: The Recall [[ID]] is not needed on a buy-in execution as the execution can be for multiple 
Recall IDs. [[NSCC]] always uses a buy-in execution to offset the [[shares]] outstanding of the 
oldest recall in the system first.
Char 2
:16S:LINK End of Block
End of Subsequence A1 Linkages
:16S:GENL End of Block
End of Sequence A General Information
Mandatory Sequence B Trade Details
:16R:TRADDET Start of Block
:98A::SETT//yyyymmdd Transaction processing date. Should be the current date in YYYYMMDD format. 
Rule: 
For BEXE,  if prior than the oldest Allowed Execution Date on open recalls for the loan, 
rejected with code 02.
Char 8
:35B:ISIN XXXXXXXXXXXX Security ISIN [[ID]] on the loan. 
Rule:
Must match ISIN on the original loan; otherwise, rejected with code 03.
Char 12
[[SFT]] Clearing: General User Guide
A. Message Layouts 174

---

## Page 175

ISO Tag MT542 Input Values and Rules Length of Data 
Field
:35B:/US/XXXXXXXXX [[CUSIP]] [[ID]] on the loan.
Rule:
Must match [[CUSIP]] on the original loan; otherwise, rejected with code 03.
CHAR 9
Optional Subsequence B1 Financial Instrument Attributes
:16R:FIA Start of Block
:92A::INTR//000000000000,00 For future use for Accrued Interest. 
Rules:
l Currently, not used by [[NSCC]]; ignored if submitted.
Num 5
:90B::EXER//ACTU/USD000000,000000 Average price per share for the execution.
Rules:
l Required for the BEXE= Buy-in Execution message type. If not submitted or non-
numeric, rejected with code 05.
l If submitted for the RCLL=Recall, CRCL=Cancel Recall, or CBEX=Cancel Buy-In
Execution message type, [[NSCC]] ignores.
Numeric 
999999,999999
:16S:FIA End of Block
End of Subsequence B1 Financial Instrument Attributes
:22F::PROC/DTCY/ISOI Message [[ID]]. 
Rule: 
ISOI = [[CNS]] ISO Input ([[default]])
Char 4
:70E::SPRO//xxxxxxxxxxxxxxxxetc Contact Information, 5 lines up to 35 characters each:
l Contact Name on the first line.
l Contact telephone number on the second line.
l Contact email on lines 3, 4, and 5.
Char 0-175
:16S:TRADDET End of Block
End of Sequence B Trade Details
[[SFT]] Clearing: General User Guide
A. Message Layouts 175

---

## Page 176

ISO Tag MT542 Input Values and Rules Length of Data 
Field
Mandatory Sequence C Financial Instrument/Account
:16R:FIAC Start of Block
:36B::SETT//UNIT/0000000000000,0 Share quantity.
Rules:
l Required for the RCLL=Recall or BEXE=Buy-in Execution message type.
l For CRCL=Cancel Recall and CBEX=Cancel Buy-in Execution, share quantity of zero
(0) is accepted.
l For RCLL=Recall, cannot exceed outstanding not-recalled [[shares]] of the off-leg;
otherwise, rejected with code 04.
l For BEXE=Buy-In Execution, cannot exceed sum of [[shares]] of all open recalls for the
loan; otherwise, rejected with code 04.
Note: No partial cancellation is allowed for a Recall or a Buy-In Execution. It must always be 
for the full amount of the [[shares]].
Num 11
:97A::SAFE//xxxxxxxx [[SFT]] Clearing Account [[ID]] of the original Lender submitting the message.
Rule: 
Must match Lender [[SFT]] [[participant]] [[ID]] on the original off-leg; otherwise, rejected with code 
01.
Char 8
:16S:FIAC End of Block
End of Sequence C Financial Instrument/Account
Mandatory Sequence E [[settlement]] Details
:16R:SETDET Start of Block
:22F::SETS/DTCY/SUBT [[NSCC]] Sub-Account Code.
l SUBT = Sub-Account, whereby T is the identifier for [[SFT]] Clearing.
Char 4
[[SFT]] Clearing: General User Guide
A. Message Layouts 176

---

## Page 177

ISO Tag MT542 Input Values and Rules Length of Data 
Field
:22F::SETR/DTCYTXNT/xxxx Transaction type. 
Allowed values:
l BEXE = Buy-in Execution
l CBEX = Cancel Buy-in Execution
l CRCL = Cancel Recall
l RCLL = Recall
Otherwise, the message is bypassed.
Char 4
Repetitive Mandatory Subsequence E1 [[settlement]] Parties
:16R:SETPRTY Start of Block
:95R::DEAG/DTCYPART/xxxx Submitting Firm [[ID]] / Sending Entity [[ID]]
[[DTC]] [[ID]] of the firm submitting the message; same as the Sending Entity in UTC.
Rule:
Must match the Submitting Firm [[ID]] on the original loan; otherwise, rejected with code 14.
Char 4
:16S:SETPRTY End of Block
:16R:SETPRTY Start of Block
:95P::PSET//DTCYUS33 [[settlement]] location. Depository [[ID]] 
Value:
DTCYUS33
Char 8 
:16S:SETPRTY End of Block
End of Subsequence E1 [[settlement]] Parties
:16S:SETDET End of Block
End of Subsequence E [[settlement]] Details
[[SFT]] Clearing: General User Guide
A. Message Layouts 177

---

## Page 178

A.9 Recall and Buy-In Execution Output Message Formats
The following table shows the ISO MT548 output message formats for Recall and Buy-In transactions. This output is provided to the Approved [[SFT]] 
Submitter, Members to the [[SFT]], or both. It includes output on a recall, cancel recall, buy-in execution, and cancel buy-in execution. It is also used for 
updates to outstanding recalls against an [[SFT]] that was updated resulting from a Send-to Settle or Corporate Action being processed. The output is MT548 
and the CDTS Product is CNSISOO.
ISO Tag MT548 Description Length of Data 
Field
Mandatory Sequence A General Information
:16R:GENL Start of Block
:20C::SEME//xxxxxxxxxxxxxxxx [[DTCC]] generated. Used to track the transaction from submission to the 
final state.
:23G:INST
:98C::PREP//yyyymmddhhmmss Processing timestamp. Char 14
Repetitive Mandatory Subsequence A1 Linkages
:16R:LINK Start of Block
:20C::RELA//xxxxxxxxxxxxxx [[DTCC]] Reference [[ID]] of the outstanding [[SFT]]. Char 14
:16S:LINK End of Block
:16R:LINK Start of Block
:20C::COMM//xx [[DTCC]] generated. 
Recall [[ID]] or Buy-in [[ID]]
Char 2
:16S:LINK End of Block
End of Subsequence A1 Linkages
Repetitive Mandatory Subsequence A2 Status
:16R:STAT Start of Block
[[SFT]] Clearing: General User Guide
A. Message Layouts 178

---

## Page 179

ISO Tag MT548 Description Length of Data 
Field
:25D:SETT/DTCY/xxxx Status of the transaction.
Values:
l ACPT = Accepted
l CLSD = Closed
l EXED = Full/Partial Recall Execution (will be sent for partial [[SFT]] Execution)
l MADE = Full/Partial Recall MADE (will be sent for partial [[SFT]] MADE)
l RCVD = Buy-In Execution Received
l RJCT = Rejected
l UPDT = Recall update due to a Corporate Action
Char 4
Repetitive Optional Subsequence A2a Reason
:16R:REAS Start of Block
:24B::REJT/DTCY/xxxx Optional. Used only for rejected transactions.
Value:
RJCT = Rejected 
Char 4
:70D::REAS//xxxxxxxxxxxxxxxxetc. Optional. Used only for rejected transactions.
Explains why the message was not processed.
Char 1 - 210
:16S:REAS End of Block
End of Subsequence A2a Reason
:16S:STAT End of Block
End of Subsequence A2 Status
:16S:GENL End of Block
End of Sequence A General Information
Optional Sequence B [[settlement]] Transaction Details
:16R:SETTRAN Start of Block
:35B:/US/XXXXXXXXX Security [[ID]] in a [[CUSIP]] format. Char 9
[[SFT]] Clearing: General User Guide
A. Message Layouts 179

---

## Page 180

ISO Tag MT548 Description Length of Data 
Field
l :36B::SETT//UNIT/00000000000,0
- or -
l :36B::SETT//AMOR/00000,0000
l Quantity of [[shares]] being traded.
- or -
l Share quantity or lending rate. The  AMOR qualifier is used only when the Transaction
Type = RMOD.
Num 11
- or -
If AMOR, use
PIC 9(5).9(4)
:19A::SETT//USD000000000000,00 Total amount of the buy-in execution calculated as:
Total [[shares]] of the Execution x Average Price 
Num 15
:19A::OCMT//USD000000000000,00 Accrued Interest. 
Future use for when expanded to Corporate [[Bonds]].
Num 15
:97A::SAFE//xxxxxxxx [[SFT]] Clearing [[Member]] (always [[Borrower]]) - in possession of [[securities]]. Char 8
:22F::SETR/DTCYREAS/xxxx Role of the message recipient.
Values:
l LEND = Lender
l BRRW = [[Borrower]]
Char 4
:22H::REDE//xxxx Deliverer / Recipient indicator for the message recipient.
Values:
l DELI = Used if you are the deliverer of [[shares]] at [[DTC]] ([[Borrower]]).
l RECE = Used if you are the receiver of [[shares]] at [[DTC]] (Lender).
Char 4
:22H::PAYM//xxxx Payment indicator.
Value:
FREE = for free transactions.
Char 4
[[SFT]] Clearing: General User Guide
A. Message Layouts 180

---

## Page 181

ISO Tag MT548 Description Length of Data 
Field
:22F::STCO/DTCYTXNT/xxxx Transaction Types
Values:
l BEXE = Buy-In Execution
l CBEX = Cancel Buy-In Execution
l CRCL = Cancel Recall
l RCLL = Recall
l RMOD = Rate Modification
l SNDS = Sent-to-Settle
Char 4
:22F::SETS/DTCY/xxxx Sub-Account Code.
Value: 
l SUBT = [[SFT]] Sub-account
Char 4
:22F::SETS/DTCY/xxxx Lend rate indicator. 
Values: 
l BRRW - Paid to the [[Borrower]]
l LEND - Paid to the Lender
l NRTE - No Rate
l OTHR - Other value
Char 4
:98C::EXSE//ccyymmddhhmmss Time the recall was received.
Used only for RCLL = Recall messages.
Char 14
:98A::SETT//yyyymmdd Date the recall was received. Char 8
:98A::TRAD//yyyymmdd Allowed date of the execution.
Used only for accepted RCLL = Recall messages.
Char 8
:70E::SPRO//xxxxxxxxxxxxxx etc. Contact Information, 5 lines up to 35 characters each:
l Contact Name on the first line.
l Contact telephone number on the second line.
l Contact email on lines 3, 4, and 5.
Char 0-175
[[SFT]] Clearing: General User Guide
A. Message Layouts 181

---

## Page 182

ISO Tag MT548 Description Length of Data 
Field
Repetitive Optional Subsequence B1 [[settlement]] Parties
:16R:SETPRTY Start of Block
:95Q::BUYR//xxxxxxxx [[SFT]] Clearing Account of the original lender submitting the message. Char 8
:16S:SETPRTY End of Block
:16R:SETPRTY Start of Block
:95R::DEAG/DTCYPART/xxxxxxxx Settling account of the original lender submitting the message. Char 8
:16S:SETPRTY End of Block
:16R:SETPRTY Start of Block
:95Q::DECI//xxxx Submitting Entity.
Party that submits on behalf of the [[Member]].
Char 4
:16S:SETPRTY End of Block
:16R:SETPRTY Start of Block
:95Q::SELL//xxxxxxxx [[SFT]] Clearing Account of the original [[Borrower]] submitting the message. Char 8
:16S:SETPRTY End of Block
:16R:SETPRTY Start of Block
:95R::REAG/DTCYPART/xxxxxxxx Settling account of the original [[Borrower]]. Char 8
:16S:SETPRTY End of Block
:16R:SETPRTY Start of Block
:95P::PSET//DTCYUS33 Depository [[ID]]. 
Value:
DTCYUS33
Char 8
:16S:SETPRTY End of Block
End of Sequence B1 [[settlement]] Parties
:16S:SETTRAN End of Block
End of Sequence B [[settlement]] Transaction Details
[[SFT]] Clearing: General User Guide
A. Message Layouts 182

---

## Page 183

B. File and Report Layouts 183
B. FILE AND REPORT LAYOUTS
Access the following files and reports:
l Outstanding Loan MRO AutoRoute [[ID]]: Production 02043624 / PSE 02983624
l End of Day ([[EOD]]) [[mark-to-market]] MRO AutoRoute [[ID]]: Production 02043623 / PSE 02983623
l Eligible Security  MRO: AutoRoute [[ID]] Production 02043626 / PSE 02983626
l Record Date Print Image: AutoRoute [[ID]] Production 02042959 / PSE 02982959
l [[Dividend]] Activity MRO: AutoRoute [[ID]] Production 02043700 / PSE 02983700
l [[Dividend]] With Due Bill Activity MRO: AutoRoute [[ID]] Production 02043701 / PSE 02983701
l Miscellaneous Activity (Extended) MRO: AutoRoute [[ID]] Production 02040343 / PSE 02980343 (Night) and
Production 02040331 / PSE 02980331 (Day)
B.1 Outstanding Loan MRO AutoRoute [[ID]]: Production 02043624 / PSE
02983624
The Outstanding Loan MRO is an end-of day file that will be distributed by [[NSCC]]. It will report to each [[Member]] their 
street-side SFTs that are outstanding with [[NSCC]] at the end of the business day, which is around 5:30 P.M. Eastern 
Time. It will also report all open recalls against those SFTs. The file will be distributed at approximately 5:45 P.M. 
Eastern Time. A [[Member]] can use this file to balance their net debit/credit of overnight rebate interest. This interest will 
be applied the next business day to their Fed Funds [[settlement]] (FFS) code 130 balance (Rebate Interest) on their 
[[NSCC]] [[participant]] account statement.
There will be three record types for this MRO as outlined below.
l Header Record with the processing date – One record per [[participant]].
l Outstanding Loan Detail Record – One per each outstanding [[SFT]] for each participating [[SFT]] Clearing [[Member]].
l Loan Recall Detail Record (if any) – One per each open recall for each participating [[SFT]] Clearing [[Member]]. The
recall detail section will only be populated if the Recall Indicator field =Y in the Outstanding Loan detail record (Byte
293).
Header Record
The following table show the Header record details for the Outstanding Loan MRO  AutoRoute [[ID]]: Production 
02043624 / PSE 02983624:
 AutoRoute [[ID]] Production 02043624 / PSE 02983624
Header Record 
Length = 400
No Description Length Start End Type Comments
1 Processing Date 8 1 8 A/N Format:
MM/DD/CCYY
2 Filler 392 9 400 A/N For future use.
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 184

B. File and Report Layouts 184
Loan Detail Record
The following table show the Loan Detail record details for the Outstanding Loan MRO  AutoRoute [[ID]]: Production 
02043624 / PSE 02983624:
 AutoRoute [[ID]] Production 02043624 / PSE 02983624
Loan Detail Record
Length = 400
No Description Length Start End Type Comments
1 [[SFT]] Clearing [[Member]] 
[[ID]] 
8 1 8 A/N [[SFT]] Clearing [[Member]]  account  of  the  Clearing 
[[Member]].
2 Clearing  [[Member]]  [[ID]] 8 9 16 A/N Party  receiving  the  MRO  file.
3 Record  type 2 17 18 A/N L  =  Loan 
4 [[DTCC]]  Reference  [[ID]] 14 19 32 A/N [[DTCC]]  Reference  [[ID]]  of  the outstanding  loan.
5 Side  Indicator 1 33 33 A/N
l D  =  Deliverer/Returner  of the  [[shares]]  ([[Borrower]])
l R  =  Receiver  of  the  [[shares]]  (Lender)
6 Leg  Indicator 1 34 34 A/N O  =  Off-leg 
7 Loan  Status 4 35 38 A/N PEND  =  Pending  [[settlement]] 
8 [[settlement]]  Date 8 39 46 A/N [[settlement]]  date.
Format:  YYYYMMDD 
9 ISIN 12 47 58 A/N Security  ISIN  [[ID]] of  the loaned [[shares]].
10 [[CUSIP]] 9 59 67 A/N Security  [[CUSIP]] [[ID]]  of the loaned [[shares]].
11 Share  Quantity 11 68 78 N Share  quantity  of the  outstanding  loan.
12 Share  Price 13 79 91 N Price  of  security in  loan  transaction.
1234567123456
The first seven digits are integers and the last six 
digits are decimals.
13 Contract  Amount 17 92 108 N Calculated  contract amount  of  the loan  transaction.
(Share  Quantity  *  Share  Price)
12345678901234512
The first fifteen digits are integers and the last two 
digits are decimals. 
14 Independent  Amount 
Rate 
10 109 118 N Rate  for  Independent  Amount  calculation.
1234561234
The first six digits are integers and the last four digits 
are decimals. 
15 Independent  Amount 17 119 135 N Calculated  Independent  Amount.
12345678901234512
The first fifteen digits are integers and the last two 
digits are decimals.  
[[SFT]] Clearing: General User Guide

---

## Page 185

B. File and Report Layouts 185
 AutoRoute [[ID]] Production 02043624 / PSE 02983624
Loan Detail Record
Length = 400
No Description Length Start End Type Comments
16 Rounding  Rule  Code 1 136 136 A/N Indicates  Rounding  Rule  for  Settle  Price  Calculation: 
l 0  =  No  rounding
l 1  =  Up  to the nearest  $0.01
l 2  = Up  to  nearest $0.05
l 3  = Up  to  nearest $0.10
l 4  =  Up  to  nearest  $0.25
l 5  =  Up  to  nearest  $1.00
17 [[settlement]]  Price 13 137 149 N Calculated  [[settlement]]  price  to  determine  the  Loan 
[[settlement]]  Amount.
1234567123456
The first seven digits are integers and the last six 
digits are decimals.  
18 [[settlement]]  Amount 17 150 166 N Outstanding  Contract  Amount  of  [[DTCC]]  Reference [[ID]].
12345678901234512
The first fifteen digits are integers and the last two 
digits are decimals. 
19 Rebate  Interest  Amount 17 167 183 N Calculated  as:
(Loan  Outstanding  [[settlement]]  Value  *  Number  of 
Days  *  Rate)  /360 
12345678901234512
The first fifteen digits are integers and the last two 
digits are decimals. 
20 Rebate  Interest  Amount 
Indicator 
1 184 184 A/N
l D  = Debit  of  Rebate  Interest
l C  = Credit  of  Rebate  Interest
l Spaces = No  Rebate  Interest
21 Lending/Interest  Rate 
Indicator 
1 185 185 A/N
l N = No  Rate
l B = Paid  to  Original  [[Borrower]]
l L = Paid  to  Original  Lender
22 Lending/  Interest  Rate 10 186 195 N Rate  for  Interest  Amount calculation.
1234561234
The first six digits are integers and the last four digits 
are decimals.  
[[SFT]] Clearing: General User Guide

---

## Page 186

B. File and Report Layouts 186
 AutoRoute [[ID]] Production 02043624 / PSE 02983624
Loan Detail Record
Length = 400
No Description Length Start End Type Comments
23 Corporate 
Action Indicator 
1 196 196 A/N Security   loan  is  undergoing  an  upcoming  corporate 
action. 
l N  =  No  Active  Corp  Actions  for  the  Security
l Y  =  Security  is  under  Corp  Action
24 Executing  [[participant]]  [[ID]] 8 197 204 A/N Executing  [[participant]]  [[ID]]  for  the  major  or  party 
receiving the  record. 
25 Introducing [[participant]] 
[[ID]] 
8 205 212 A/N Introducing  [[participant]]  [[ID]]  for  the  major  or  party 
receiving the  record 
26 Client  Order  [[ID]] 32 213 244 A/N Client  Order  [[ID]]  of  the  [[SFT]] Clearing [[Member]]. 
27 Execution  [[ID]] 32 245 276 A/N Vendor  or  Marketplace  unique  reference  [[ID]].
28 Contra  Clearing 
[[Member]]  [[ID]] 
8 277 284 A/N Original  Contra  [[participant]]  [[ID]]  to  the  loan  transaction.
29 Contra  [[SFT]] Clearing 
[[Member]]  [[ID]] 
8 285 292 A/N Original  [[SFT]] Clearing [[Member]]  account  of  the contra 
party  to  the  loan  transaction. 
30 Recall  Indicator 1 293 293 A/N
l Y =  Recall
l N  =  No  recall
If  populated  with  a Y,   see the Recall Detail Record.
31 Filler 107 294 400 A/N For future use.
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 187

B. File and Report Layouts 187
Recall Detail Record
The following table show the Recall Detail record details for the Outstanding Loan MRO  AutoRoute [[ID]]: Production 
02043624 / PSE 02983624:
 AutoRoute [[ID]] Production 02043624 / PSE 02983624
Recall Detail Record 
Length = 400
No Description Length Start End Type Comments
1 [[SFT]] Clearing 
[[Member]] [[ID]] 
8 1 8 A/N [[SFT]] Clearing [[Member]] account of the Clearing [[Member]].
2 Clearing [[Member]] [[ID]] 8 9 16 A/N [[ID]] of the Clearing [[Member]]. 
3 Record type 2 17 18 A/N R = Recall 
4 [[DTCC]] Reference [[ID]] 14 19 32 A/N [[DTCC]] Reference [[ID]] of the outstanding loan. 
5 Recall [[ID]] 2 33 34 A/N [[DTCC]] Recall [[ID]] 
6 Recall Status 4 35 38 A/N OPEN = Open 
7 Recall Date 8 39 46 A/N Date when the recall was initiated. 
Format: YYYYMMDD 
8 ISIN 12 47 58 A/N Security ISIN [[ID]] of the recalled [[shares]].
9 [[CUSIP]] 9 59 67 A/N Security [[CUSIP]] [[ID]] of the recalled [[shares]]. 
10 Share Quantity 11 68 78 N Share quantity of the outstanding recall.
11 Allowed Date of 
Execution 
8 79 86 A/N Recall allowed execution date. 
Format: YYYYMMDD 
12 Recall  Time 8 87 94 A/N Time when the recall was received by SAS. 
Format: HH.MM.SS 
13 Filler 306 95 400 A/N For future use.
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 188

B. File and Report Layouts 188
B.2 End of Day ([[EOD]]) [[mark-to-market]] MRO AutoRoute [[ID]]: Production
02043623 / PSE 02983623
The End of Day [[mark-to-market]] MRO is a file submitted by [[NSCC]] after the [[DTC]] drop cutoff time. A [[Member]] can use 
this file to balance their net debit/credit of marks for Price Differential and deliver order ([[DO]]) off-leg returns (not rolled) 
that did not settle at [[DTC]] where [[NSCC]] had to process a [[mark-to-market]] on the unsettled transaction. These marks will 
be applied to a firm’s Fed Funds [[settlement]] (FFS) code 131 balance ([[SFT]] Marks) on their [[NSCC]] [[participant]] Account 
Statement.
Note
The end of day [[mark-to-market]] MRO is from Non Return Fails and Price Differentials that did not settle at [[DTC]].
Header Record
The following table show the Header record details for the [[EOD]] [[mark-to-market]] MRO AutoRoute [[ID]]: Production 
02043623 / PSE 02983623:
AutoRoute [[ID]] Production 02043623 / PSE 02983623
Header Record 
Record Length = 300
No Description Length Start End Type Comments
1 Processing Date 8 1 8 A/N Format:
MMDDCCYY
2 Filler 272 9 300 A/N For future use.
END OF RECORD
Detail Record
The following table show the Detail record details for the [[EOD]] [[mark-to-market]] MRO AutoRoute [[ID]]: Production 
02043623 / PSE 02983623:
AutoRoute [[ID]] Production 02043623 / PSE 02983623
Detail Record 
Record Length = 300
No Description Length Start End Type Comments
1 Clearing  [[Member]]  [[ID]] 8 1 8 A/N Party  receiving  the MRO  file.
2 [[SFT]] Clearing 
[[Member]]  [[ID]] 
8 9 16 A/N [[SFT]] [[Member]] A/C of the Clearing [[Member]]. 
3 [[DTCC]]  Reference  [[ID]] 14 27 30 A/N [[DTCC]]  Reference  [[ID]]  for  the loan  that  had  an  [[EOD]]  mark-to-
market. 
4 [[CUSIP]] 9 31 39 A/N [[CUSIP]]  of the loaned  [[shares]].
5 ISIN 12 40 51 A/N ISIN  [[ID]]  of the loaned  [[shares]].
6 Client  Order  [[ID]] 32 52 83 A/N Client  Order  [[ID]]  for  the  [[SFT]] [[Member]].
7 Execution  [[ID]] 32 84 115 A/N Vendor  or  Marketplace  unique  reference.
[[SFT]] Clearing: General User Guide

---

## Page 189

B. File and Report Layouts 189
AutoRoute [[ID]] Production 02043623 / PSE 02983623
Detail Record 
Record Length = 300
No Description Length Start End Type Comments
8 Share  Quantity 11 116 126 N Share  quantity  of  the outstanding  loan.
9 Side  Indicator 1 127 127 A/N l D  =  Deliverer  of the security  ([[Borrower]])
l R  =  Receiver  of the security  (Lender)
10 [[settlement]]  Date 8 128 135 A/N [[settlement]]  date. 
Format:  YYYYMMDD 
11 [[mark-to-market]] 
Amount                          
17 136 152 N Difference  between  the prior  day  Loan [[settlement]] Amount 
of  the  loan  and  new  Loan [[settlement]]  Amount  for  the  
outstanding  Loan  Quantity. 
12345678901234512
The first fifteen digits are integers and the last two digits 
are decimals. 
12 [[mark-to-market]]  
Amount  Indicator 
1 153 153 A/N
l D  =  Debit  of  [[mark-to-market]]
l C  =  Credit  of  [[mark-to-market]]
13 Contra 
Clearing [[Member]] [[ID]]
8 154 161 A/N Original  Contra  party  to  that  loan  transaction.
14 Contra  [[SFT]] Clearing 
[[Member]]  [[ID]]                          
8 162 169 A/N Original  [[SFT]] Clearing [[Member]]  account  of  the contra  party 
to  that  loan  transaction.
15 Filler 170 130 300 A/N For future use.
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 190

B. File and Report Layouts 190
B.3 Eligible Security  MRO: AutoRoute [[ID]] Production 02043626 / PSE
02983626
The following table show the record details for the Eligible Security MRO output information for AutoRoute [[ID]]: 
Production 02043626 / PSE 02983626:
AutoRoute [[ID]] Production 02043626 / PSE 02983626
Record Type = Fixed
Record Length = 133
Revision Date = N/A
Description Length Start End Type Comments
[[settlement]] Date 8 1 8 A/N Payable date of the [[Dividend]], in the YYYYMMDD format.
[[CUSIP]] 9 9 17 A/N [[CUSIP]] identifier for the security.
ISIN 12 18 29 A/N ISIN identifier for the security.
Security Description 30 30 59 A/N Description of the security.
[[SFT]] New Loan 
Eligibility 
1 60 60 A Eligibility of the security for [[SFT]] accepting new loan 
instructions. Accepted values are:
l Y = Yes
l N = No
[[SFT]] Roll Eligibility 1 61 61 A Eligibility of the security for [[SFT]] accepting roll instructions. 
Accepted values are:
l Y = Yes
l N = No
Filler 72 62 133 A/N Reserved for future use. Spaces.
END OF RECORD
B.4 Record Date Print Image:  AutoRoute [[ID]] Production 02042959 /
PSE  02982959
The Record Date print image report for AutoRoute [[ID]] Production 02042959 / PSE 02982959 shows outstanding loan 
positions on a record date and due bill redemption date for a declared [[Dividend]]  distribution. This report does not need 
layout specifications to be viewed and read.
[[SFT]] Clearing: General User Guide

---

## Page 191

B. File and Report Layouts 191
B.5 [[Dividend]] Activity MRO: AutoRoute [[ID]] Production 02043700 / PSE
02983700
The [[Dividend]] Activity MRO output is a separate output in addition to the existing [[CNS]] [[Dividend]] Activity MRO. 
Specifications for the [[SFT]] Clearing service [[Dividend]] Activity MRO are as follows:
Header Record
The following table show the Header record details for the [[Dividend]] Activity MRO for AutoRoute [[ID]] Production 
02043700 / PSE 02983700:
AutoRoute [[ID]] Production 02043700 / PSE 02983700
Header Record 
Record Length = 220
Description Length Start End Type Comments
Record Type 1 1 1 A/N H
Title 44 2 45 A [[CNS]] [[Dividend]] ACTIVITY MRO
[[participant]] Number 4 46 49 A/N [[participant]] number
Process Date 10 50 59 A/N MM/DD/CCYY
[[settlement]] Date 10 60 69 A/N MM/DD/CCYY
Filler 151 70 220 A/N For future use.
END OF RECORD
Detail Record
The following table show the Detail record details for the [[Dividend]] Activity MRO for AutoRoute [[ID]] Production 02043700 
/ PSE 02983700:
AutoRoute [[ID]] Production 02043700 / PSE 02983700
Detail Record 
Record Length = 220
Description Length Start End Type Comments
Record Type 1 1 1 A/N l C = Cash payment
l S = [[Stock]] payment
l P = Spinoff [[Stock]] payment
Security Number 9 2 10 A/N [[CUSIP]] issuing [[Dividend]].
When Issued indicator 1 11 11 A/N When Issued indicator for issuing [[CUSIP]].
l 0 = Regular
l 1 = When issued
[[CUSIP]] Description 30 12 41 A/N [[CUSIP]] description
Action Sequence 
Number
4 42 45 N Internal tracking number for [[Dividend]].
[[participant]] Number 4 46 49 A/N [[participant]] number
[[SFT]] Clearing: General User Guide

---

## Page 192

B. File and Report Layouts 192
AutoRoute [[ID]] Production 02043700 / PSE 02983700
Detail Record 
Record Length = 220
Description Length Start End Type Comments
Sub-account type 1 50 50 A/N T = [[SFT]] Clearing Account 
Sub-account Name 23 51 73 A/N l Type A = Blanks
l Types C – H (See literal names above)
l Types I – Z = Blanks
Rate Sequence Number 4 74 77 A/N Internal tracking number for [[Dividend]] component rate.
Position Sequence 
Number
4 78 81 A/N Internal tracking number for eligible position.
Position Quantity 9 82 90 N Position on which [[Dividend]] is calculated. No decimal 
places.
Ratio 9 91 99 N Rate applied to position to determine payment.
123412345
The first four digits are integers and the last five digits are 
decimals. 
Payment Value 17 100 116 N Position Quantity * Rate
[[Stock]]/spinoff payments are always whole numbers.
12345678901234512
The first fifteen digits are integers and the last two digits 
are decimals. 
Sign 1 117 117 A/N + or - = Defines payment value.
Closing Price 12 118 129 A/N Used for cash in lieu calculations.
123456123456
The first six digits are integers and the last six digits are 
decimals. 
Pay Date 8 130 137 A/N Payable Date of [[Dividend]].
CCYYMMDD
Ex-[[Dividend]] Date 8 138 145 A/N Ex-[[Dividend]] date of [[Dividend]].
CCYYMMDD
Record Date 8 146 153 A/N Record Date of [[Dividend]].
CCYYMMDD
Remarks 35 154 188 A/N Description of unusual payments (such as late, reversals).
Currency indicator 3 189 191 A/N
l Spaces = USD
l No other values current.
Debit/Credit code 1 192 192 A/N l D = Debit
l C= Credit
[[SFT]] Clearing: General User Guide

---

## Page 193

B. File and Report Layouts 193
AutoRoute [[ID]] Production 02043700 / PSE 02983700
Detail Record 
Record Length = 220
Description Length Start End Type Comments
Spinoff [[CUSIP]] 9 193 201 A/N For spinoffs, [[CUSIP]] of [[Stock]] being paid; otherwise, 
spaces.
Spinoff When Issued 
indicator
1 202 202 A/N When issued indicator for spinoff [[CUSIP]].
l 0 = Regular
l 1 = When issued
l Otherwise, spaces
Filler 1 203 203 A/N For future use.
Cash in lieu indicator 1 204 204 A/N Y indicates cash payment is cash in lieu.
Long/Short indicator 1 205 205 A/N Defines Position Quantity 
l L=Long Position
l S=[[short position]]
[[DTCC]] Reference [[ID]] 14 206 219 A/N Unique [[DTCC]] reference [[ID]].
Filler 1 220 220 A/N For future use.
END OF RECORD
Trailer Record
The following table show the Trailer record details for the [[Dividend]] Activity MRO for AutoRoute [[ID]] Production 
02043700 / PSE 02983700:
AutoRoute [[ID]] Production 02043700 / PSE 02983700
Trailer Record 
Record Length = 220
Description Length Start End Type Comments
Record Type 1 1 1 A/N T
Filler 44 2 45 A Spaces
[[participant]] Number 4 46 49 A/N [[participant]] number
Detail Count 8 50 57 A/N Number of detail records sent.
99999999
Filler 163 58 220 A/N For future use.
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 194

B. File and Report Layouts 194
B.6 [[Dividend]] With Due Bill Activity MRO: AutoRoute [[ID]] Production
02043701 / PSE 02983701
The [[Dividend]] with Due Bill Activity MRO output is a separate output in addition to the existing [[CNS]] [[Dividend]] with Due 
Bill Activity MRO.  The specifications for this MRO for the [[SFT]] Clearing service are provided.
Header Record
The following table show the Header record details for the Due Bill Activity MRO output information for AutoRoute [[ID]]: 
Production 02043701 / PSE 02983701:
AutoRoute [[ID]] Production 02043701 / PSE 02983701
Header Record 
Record Length = 220
Description Length Start End Type Comments
Record Type 1 1 1 A/N H
Title 44 2 45 A [[CNS]] DUE BILL ACTIVITY MRO
[[participant]] Number 4 46 49 A/N [[participant]] number
Process Date 10 50 59 A/N MM/DD/CCYY
[[settlement]] Date 10 60 69 A/N MM/DD/CCYY
Filler 151 70 220 A/N For future use.
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 195

B. File and Report Layouts 195
Detail Record
The following table show the Detail record details for the Due Bill Activity MRO output information for AutoRoute [[ID]]: 
Production 02043701 / PSE 02983701:
AutoRoute [[ID]] Production 02043701 / PSE 02983701
Detail Record 
Record Length = 220
Description Length Start End Type Comments
Record Type 1 1 1 A/N l C = Cash payment
l S = [[Stock]] payment
l P = Spinoff [[Stock]] payment
Security Number 9 2 10 A/N [[CUSIP]] issuing due bill or bond payment.
When Issued indicator 1 11 11 A/N When Issued indicator for issuing [[CUSIP]]
l 0 = Regular
l 1 = When issued
[[CUSIP]] Description 30 12 41 A/N [[CUSIP]] description.
Action Sequence Number 4 42 45 N Internal tracking number for due bill or bond payment.
[[participant]] Number 4 46 49 A/N [[participant]] number
Sub-account type 1 50 50 A/N T = [[SFT]] Clearing Account 
Sub-account Name 23 51 73 A/N l Type A = Blanks
l Types C – H (See literal names above)
l Types I – Z = Blanks
Rate Sequence Number 4 74 77 A/N Internal tracking number for due bill or bond 
component rate.
Position Sequence Number 4 78 81 A/N Internal tracking number for eligible position.
Position Quantity 9 82 90 N Position on which due bill or bond is calculated. No 
decimal places.
Ratio 9 91 99 N Rate applied to position to determine payment.
123412345
The first four digits are integers and the last five 
digits are decimals. 
Payment Value 17 100 116 N Position Quantity * Rate.
[[Stock]]/spinoff payments always whole numbers.
12345678901234512
The first fifteen digits are integers and the last two 
digits are decimals. 
Sign 1 117 117 A/N + or - = Defines payment value.
[[SFT]] Clearing: General User Guide

---

## Page 196

B. File and Report Layouts 196
AutoRoute [[ID]] Production 02043701 / PSE 02983701
Detail Record 
Record Length = 220
Description Length Start End Type Comments
Closing Price 12 118 129 A/N Used for cash in lieu calculations.
123456123456
The first six digits are integers and the last six digits 
are decimals. 
Pay Date 8 130 137 A/N Payable date of due bill or bond.
CCYYMMDD
Ex-[[Dividend]] Date 8 138 145 A/N Ex-[[Dividend]] date of due bill.
CCYYMMDD
Spaces for bond payment.
Record Date 8 146 153 A/N Record Date of due bill or bond.
CCYYMMDD
Remarks 35 154 188 A/N Description of unusual payments, such as late, or 
reversals.
Currency indicator 3 189 191 A/N Spaces = USD
No other current values.
Debit/Credit Code 1 192 192 A/N
l D = Debit
l C= Credit
Spinoff [[CUSIP]] 9 193 201 A/N For spinoffs, [[CUSIP]] of [[Stock]] being paid, otherwise, 
spaces.
Spinoff When Issued Indicator 1 202 202 A/N When issued indicator for spinoff [[CUSIP]].
l 0 = Regular
l 1 = When issued
l Otherwise, spaces
Due bill Indicator 1 203 203 A/N D
Cash in lieu Indicator 1 204 204 A/N Y indicates cash payment is cash in lieu.
Long/Short Indicator 1 205 205 A/N Defines the position quantity.
l L=Long Position
l S=[[short position]]
[[DTCC]] Reference [[ID]] 14 206 219 A/N Unique [[DTCC]] reference [[ID]].
Filler 1 220 220 A/N For future use.
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 197

B. File and Report Layouts 197
Trailer Record
The following table show the Trailer record details for the Due Bill Activity MRO output information for AutoRoute [[ID]]: 
Production 02043701 / PSE 02983701:
AutoRoute [[ID]] Production 02043701 / PSE 02983701
Trailer Record 
Record Length = 220
Description Length Start End Type Comments
Record Type 1 1 1 A/N T
Filler 44 2 45 A Spaces
[[participant]] Number 4 46 49 A/N [[participant]] number
Detail Count 8 50 57 A/N Number of detail records sent.
99999999
Filler 163 58 220 A/N For future use.
END OF RECORD
B.7 Miscellaneous Activity (Extended) MRO: AutoRoute [[ID]] Production
02040343 / PSE 02980343 (Night) and Production 02040331 / PSE
02980331 (Day)
The purpose of the Miscellaneous Activity File is report record entries that update an outstanding [[SFT]] as a result of 
[[NSCC]] processing a buy-in execution, corporate action, termination, or exit. These events typically result in a 
collection/payment of money by [[NSCC]] against the contra members to the [[securities]] Financing Transaction ([[SFT]]) 
Clearing service. In some cases, the recorded entries result in no payment (for example, name change). Members 
should use these files to balance to their Fed Funds Money [[settlement]] Code 132 on the [[NSCC]] [[participant]] Account 
Statement.
Header Record
The following table show the Header record details for the Miscellaneous Activity (Extended) MRO for AutoRoute [[ID]]: 
Production 02040343 / PSE 02980343 (Night) and Production 02040331 / PSE 02980331 (Day):
AutoRoute [[ID]] Production 02040343 / PSE 02980343 (Night) 
and Production 02040331 / PSE 02980331 (Day)
Header Record 
Record Length = 100
Description Length Start End Type Comments
Record Type 1 1 1 A/N H
Literal 50 2 51 A/N [[NSCC]]-[[CNS]]-MISCELLANEOUS-ACTIVITY- FOR-
[[settlement]]-OF-
Date 10 52 61 A/N MM-DD-CCYY
Future Use 14 62 75 A/N Reserved
[[SFT]] Clearing: General User Guide

---

## Page 198

B. File and Report Layouts 198
AutoRoute [[ID]] Production 02040343 / PSE 02980343 (Night) 
and Production 02040331 / PSE 02980331 (Day)
Header Record 
Record Length = 100
Description Length Start End Type Comments
[[participant]] 
Clearing Number
4 76 79 A/N Four-digit number assigned by [[NSCC]].
[[participant]] Sub-
Account
1 80 80 A/N l A = Regular Account
l B = Open
l C – D = Open
l E = Fully Paid For
l F = Open
l G = Reorg #1
l H = Reorg #2
l I = Open
l J – M = Not Used (Reserved)
l N – Q = Open
l R = ACATS Long
l S = ACATS Short
l T = [[SFT]] Processing
l U  – Z = Open
Filler 20 81 100 A/N
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 199

B. File and Report Layouts 199
Detail Record
The following table show the Detail record details for the Miscellaneous Activity (Extended) for AutoRoute [[ID]]: 
Production 02040343 / PSE 02980343 (Night) and Production 02040331 / PSE 02980331 (Day):
AutoRoute [[ID]] Production 02040343 / PSE 02980343 (Night) 
and Production 02040331 / PSE 02980331 (Day)
Detail Record 
Record Length = 100
Description Length Start End Type Comments
Record [[ID]] 1 1 1 A/N D
[[CUSIP]] 9 2 10 A/N
Constant 3 11 13 N Always = 000
Quantity Received 9 14 22 N 999999999
Quantity Received Sign 1 23 23 A/N + = Received
Quantity Delivered 9 24 32 A/N 999999999
Quantity Delivered Sign 1 33 33 N - = Delivered
Currency Indicator 3 34 36 N USD = US Dollars
Debit Value 15 37 51 A/N 123456789012312
The first thirteen digits are integers and the last two digits 
are decimals. 
Debit Value Sign 1 52 52 A/N +
Credit Value 15 53 67 N 123456789012312
The first thirteen digits are integers and the last two digits 
are decimals. 
Credit Value Sign 1 68 68 A/N -
[[SFT]] Clearing: General User Guide

---

## Page 200

B. File and Report Layouts 200
AutoRoute [[ID]] Production 02040343 / PSE 02980343 (Night) 
and Production 02040331 / PSE 02980331 (Day)
Detail Record 
Record Length = 100
Description Length Start End Type Comments
Activity 2 69 70 A/N l 02 = [[CNS]] Ineligible / MUNI Bond Exit
l 15 = Obligation Warehouse
l 17 = [[ID]] Net
l 18 = [[ID]] Net Reject/Reversal
l 20 = [[Member]] Firm Merger
l 25 = Honest [[Broker]]
l 30 = Name Change
l 35 = ACATS-ODS ([[CNS]] eligible)
l 36 = ACATS-ODS ([[DTC]], not [[CNS]] eligible)
l 39 = Inactive (Formerly Order Out - [[DTC]] Portion)
l 40 = Inactive (Formerly Supplemental Trade-NISS)
l 50 = Reorg - Name Change
l 51 = Reorg - Merger
l 52 = Reorg - Redemption
l 53 = Reorg - Ineligible - Tender
l 54 = Reorg - Reverse Split
l 55 = Daily Bal After Allocation
l 56 = Reorg Exit
l 59 = Index WTS Exercise
Activity 2 69 70 A/N l 60 = [[Stock]] Borrow
l 65 = ACATS ([[CNS]] eligible)
l 66 = ACATS ([[DTC]], not [[CNS]] eligible)
l 71 = JNL - Trade Adjustment
l 73 = JNL - [[Dividend]] Adjustment
l 74 = Inter Acct Netting / Inter Acct Transfer
l 75 = JNL - Received/Delivered Adj
l 76 = RIO B/O Into [[CNS]]
l 77 = JNL - Buy-In Execution
l 79 = JNL - [[CNS]] Ineligible Adjustment
l 81 = JNL - Reorg Adjustment
l 83 = JNL - [[Member]] Firm Adjustment
l 92 = Transfer Into Fully Paid For Account
l 93 = Transfer Out Of Fully Paid For Account
Contra [[participant]] 4 71 74 A/N Minor [[participant]]
[[SFT]] Clearing: General User Guide

---

## Page 201

B. File and Report Layouts 201
AutoRoute [[ID]] Production 02040343 / PSE 02980343 (Night) 
and Production 02040331 / PSE 02980331 (Day)
Detail Record 
Record Length = 100
Description Length Start End Type Comments
Contra Sub-Account 1 75 75 A/N l A = Regular Account
l B = Open
l C – D = Open
l E = Fully Paid For
l F = Open
l G = Reorg #1
l H = Reorg #2
l I = Open
l J – M = Not Used (Reserved)
l N – Q = Open
l R = ACATS Long
l S = ACATS Short
l T – Z = Open
[[participant]] 
Clearing Number
4 76 79 A/N Four-digit number assigned by [[NSCC]].
[[participant]] Sub-Account 1 80 80 A/N l A = Regular Account
l B = Open
l C – D = Open
l E = Fully Paid For
l F = Open
l G = Reorg #1
l H = Reorg #2 I = Open
l J – M = Not Used (Reserved)
l N – Q = Open
l R = ACATS Long
l S = ACATS Short
l T = [[SFT]] Processing
l U – Z = Open
IMB Transaction [[ID]] 10 81 90 A/N l For Sub-Account A only ([[CNS]] Regular Account) – This
is the Transaction [[ID]] for [[ID]] Net.
l For Sub-Account T only ([[SFT]] Processing) – This
represents the first 10 digits of the 14 digit [[DTCC]] [[SFT]]
Reference [[ID]].
[[SFT]] Clearing: General User Guide

---

## Page 202

B. File and Report Layouts 202
AutoRoute [[ID]] Production 02040343 / PSE 02980343 (Night) 
and Production 02040331 / PSE 02980331 (Day)
Detail Record 
Record Length = 100
Description Length Start End Type Comments
Filler 10 91 100 A/N l For Sub-Account T only ([[SFT]] Processing) – The first
four bytes represents the last four digits of the 14 digit
[[DTCC]] [[SFT]] Reference [[ID]].
l For all other Sub-Accounts, this will always be a filler.
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 203

B. File and Report Layouts 203
Sub-Total Detail Record
The following table show the Sub-Total Detail record details for the Miscellaneous Activity (Extended) for AutoRoute 
[[ID]]: Production 02040343 / PSE 02980343 (Night) and Production 02040331 / PSE 02980331 (Day):
AutoRoute [[ID]] Production 02040343 / PSE 02980343 (Night) 
and Production 02040331 / PSE 02980331 (Day)
Sub-Total Detail Record 
Record Length = 100
Description Length Start End Type Comments
Record [[ID]] 1 1 1 A/N S
Future Use 9 2 10 A/N Reserved
Quantity Received 9 11 19 N 999999999
Quantity Received 
Sign
1 20 20 A/N + = Received
Quantity Delivered 9 21 29 N 999999999
Quantity Delivered 
Sign
1 30 30 A/N - = Delivered
Currency Indicator 3 31 33 A/N USD = US Dollars
Debit Value 16 34 49 N 1234567890123412
The first fourteen digits are integers and the last two digits 
are decimals. 
Debit Value Sign 1 50 50 A/N +
Credit Value 16 51 66 N 1234567890123412
The first fourteen digits are integers and the last two digits 
are decimals. 
Credit Value Sign 1 67 67 A/N -
Future Use 8 68 75 A/N Reserved
[[participant]] Clearing 
Number
4 76 79 A/N Four-digit number assigned by [[NSCC]].
[[SFT]] Clearing: General User Guide

---

## Page 204

B. File and Report Layouts 204
AutoRoute [[ID]] Production 02040343 / PSE 02980343 (Night) 
and Production 02040331 / PSE 02980331 (Day)
Sub-Total Detail Record 
Record Length = 100
Description Length Start End Type Comments
[[participant]] Sub-
Account
1 80 80 A/N l A = Regular Account
l B = Open
l C – D = Open
l E = Fully Paid For
l F = Open
l G = Reorg #1
l H = Reorg #2
l I = Open
l J – M = Not Used (Reserved)
l N – Q = Open
l R = ACATS Long
l S = ACATS Short
l T = [[SFT]] Processing
l U – Z = Open
Filler 20 81 100 A/N
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 205

B. File and Report Layouts 205
Trailer Record
The following table show the Trailer record details for the Miscellaneous Activity (Extended) MRO for AutoRoute [[ID]]: 
Production 02040343 / PSE 02980343 (Night) and Production 02040331 / PSE 02980331 (Day):
AutoRoute [[ID]] Production 02040343 / PSE 02980343 (Night) 
and Production 02040331 / PSE 02980331 (Day)
Trailer Record 
Record Length = 100
Description Length Start End Type Comments
Record [[ID]] 1 1 1 A/N T
Future use 68 2 69 A/N Reserved
Record Count 6 70 75 N Number Of Records (Including Header And 
Trailer)
[[participant]] Clearing 
Number
4 76 79 N Four-digit number assigned by [[NSCC]].
[[participant]] Sub-Account 1 80 80 A/N
l A = Regular Account
l B = Open
l C – D = Open
l E = Fully Paid For
l F = Open
l G = Reorg #1
l H = Reorg #2
l I = Open
l J – M = Not Used (Reserved)
l N – Q = Open
l R = ACATS Long
l S = ACATS Short
l T = [[SFT]] Processing
l U – Z = Open
Filler 20 81 100 A/N
END OF RECORD
[[SFT]] Clearing: General User Guide

---

## Page 206

C. Time Frames 206
C. TIME FRAMES
The following table shows the time frames of the message types:
Note
All times listed in this guide are shown in Eastern Time.
Interface Description Time
UTC [[SFT]] input of the following transaction types commences:
l New Loan
l Pre-established Bilateral Loan
l Roll
l Send-to Settle
l Cancel
l Loan Termination
l Rate Modification
l Buy-side
Note:
The status output of all [[SFT]] submission messages also commences at this time.
04:00
SAS [[NSCC]] Initiated Price Differentials (PDs) are sent to [[DTC]]. 05:00 
SAS Real time interfacing of transaction status updates throughout the day. Includes [[NSCC]] 
Initiated Price Differentials and status updates to loans as a result of processed 
mandatory corporate action and [[Stock]] split events.
05:00
RISK Distributes clearing fund letters. 07:05
SAS Submission of the following commences:
l Recall input
l Cancel Recall input
08:00
RISK Satisfaction for any funding requirements to clearing fund is due. 10:00
UTC / SAS Cutoff time for submission of the Roll transaction type.
l SAS creates/sends all off-leg [[DO]] returns not rolled to [[DTC]] [[settlement]].
11:30 
UTC Cutoff time for submission of the following transaction types:
l New Loan
l Pre-established Bilateral Loan
l Send-to Settle
l Cancel
l Buy-side
15:00
RISK The new buy-side off-leg transactions for each [[Member]] are included in the risk margining 
process.
15:00
[[SFT]] Clearing: General User Guide

---

## Page 207

C. Time Frames 207
Interface Description Time
UTC Global message is distributed to alert Members to alert that all maturing off-leg buy-side 
trades have been “released” from [[NSCC]]’s guaranty obligation.
15:00 - 15:15 
UTC Buy-Side Off-leg messages for buy-side transactions that received today are distributed to 
Members. 
15:00 - 15:15 
SAS Recall messages received after this time will be assigned a buy-in execution date of three 
business days later.
15:00
[[DTC]] All recycling [[DO]] and PD transactions at [[DTC]] are dropped. 15:10
SAS All PD and non-rolled [[DO]] transactions that dropped at [[DTC]] are marked by [[NSCC]]. 15:10
SAS Submission of the following commences:
l Buy-in Execution input
l Cancel Buy-in execution
Note:
Any buy-in execution submitted between 15:10 and 16:30 that is not rejected will be
placed in a RECEIVED status.
15:10
SAS Distribution of the End-of Day Mark-to Market MRO (resulting from Non-Return [[DO]] Fails 
non-rolled and PDs that DROP at [[DTC]]).
l Used to balance the new FFS [[NSCC]] Money [[settlement]] Code 131.
15:30
SAS Distribution of the Day Miscellaneous Activity file that mostly includes mandatory 
Corporate Actions that were updated.
l Used to balance the new [[NSCC]] Money FFS [[settlement]] Code 132.
15:30
UTC/SAS Cutoff time for submission of the Rate Modification transaction type. 15:45
SAS SAS recalculates overnight RATE for the latest rate modification message received for an 
outstanding loan and distributes ISO message. 
16:00
RISK Distributes funding letters for Independent Amount (IA). 16:00
SAS Cutoff time for submission of the following:
l Recall
l Cancel Recall
l Loan Termination
Note:
Any buy-in execution in a RECEIVED status is updated to either ACCEPTED or
REJECTED.
16:30
RISK Satisfaction of any funding requirements for the Independent Amount are due. 17:00
UTC All Approved [[SFT]] Submitters submit good night messages to UTC for the [[SFT]] 
marketplace.
17:00
[[SFT]] Clearing: General User Guide

---

## Page 208

C. Time Frames 208
Interface Description Time
SAS Cutoff time for submission of the following:
l Buy-in Execution
l Cancel Buy-in Execution
Note:
Any buy-in execution submitted between 16:30 and 17:00 is either immediately
ACCEPTED or REJECTED.
17:00
UTC UTC sends message that includes [[EOD]] Output totals to each [[SFT]] Clearing [[Member]] for 
reconciliation and balancing.
17:15
SAS Updates any outstanding [[SFT]] transactions impacted as a result of the processing of a 
buy-in execution and reports to Members through the ISO message.
Note: 
After these updates occur, [[NSCC]] removes the outstanding [[SFT]] (or portion thereof) that 
was executed on from its books and records before the end of the current processing day. 
However, the difference between the buy-in execution value and [[SFT]] [[settlement]] value will 
be paid/collected the next business in [[NSCC]] Money FFS [[settlement]] Code 132.
17:20
SAS Distribution of the Outstanding Loan End of Day MRO file.
l Used to balance the new FFS [[NSCC]] [[settlement]] Code 130 (RATE interest) that will be
paid/collected the next [[settlement]] date.
17:30
SAS SAS captures record date and due bill redemption date positions for any underlying 
security that has a declared [[Dividend]] for an outstanding [[SFT]].
17:30
SAS SAS processes the substitute payment of any outstanding [[Dividend]] distribution for next 
business day [[settlement]].
l Used to balance the new FFS [[NSCC]] Money [[settlement]] Code 133
The following files are distributed:
l [[Dividend]] Activity Payment
l Due Bill Redemption Payment
l Record Date Print Image
17:30
SAS Processes [[NSCC]] initiated exits (such as [[securities]] undergoing a corporate action) and 
sends ISO messages to Members.
20:00
SAS Distribution of the Night Miscellaneous Activity file that mostly includes:
l Mandatory Corporate Actions that were updated
l Buy-in Executions
l Marks on Exits
o Used to balance the new [[NSCC]] Money FFS [[settlement]] Code 132.
00:30 
[[SFT]] Clearing: General User Guide

---

## Page 209

FOR MORE INFORMATION
Email [[DTCC]] Learning at:
CoreLearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com