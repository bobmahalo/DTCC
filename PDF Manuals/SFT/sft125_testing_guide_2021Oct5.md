---
title: "SFT Clearing Testing Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sft125_testing_guide_2021Oct5.pdf"
pages: 20
size: "351.6 KB"
category: "SFT"
ingested_on: "2026-06-05"
---

# SFT Clearing Testing Guide

**Original File:** [sft125_testing_guide_2021Oct5.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/sft125_testing_guide_2021Oct5.pdf)  
**Category:** SFT  
**Total Pages:** 20  
**File Size:** 351.6 KB  

---

## Page 1

 
 
 
[[securities]] FINANCING 
TRANSACTION ([[SFT]]) CLEARING 
[[SFT]] CLEARING TESTING GUIDE 
VERSION 2.0 
OCTOBER 5, 2021 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 5, 2021 
Publication Code: SFT125 
Service: [[securities]] Financing Transaction ([[SFT]]) Clearing 
Title: [[SFT]] Clearing Testing Guide 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
About This Guide ................................................................................................................................................. 4 
Commonly Used Acronyms and Terms .............................................................................................................. 4 
Accessing [[DTCC]] Learning ................................................................................................................................. 6 
[[DTCC]] Relationship Management Team ............................................................................................................. 6 
Phase-Zero: Pre-Test Preparation .................................................................................................................... 6 
[[DTCC]] Integration Team ...................................................................................................................................... 7 
PSE Region Access ([[DTCC]] Testing Environment) ............................................................................................ 7 
Testing Scope Approach ..................................................................................................................................... 8 
Phase-One: Approved [[SFT]] Submitter Only Testing ........................................................................................... 8 
Input/Output-Test Type Matrix ............................................................................................................................ 9 
Message Input/Output Scenario Case Scope ..................................................................................................14 
Phase-One: [[SFT]] Clearing [[Member]] Only Testing .............................................................................................16 
Phase-Two: Approved [[SFT]] Submitter and [[SFT]] Clearing [[Member]] Testing  .....................................................17 
MRO Testing (SAS File-Output Only) ...............................................................................................................18 
Test Security (Symbol) .....................................................................................................................................18 
Testing Schedule ..............................................................................................................................................19 
Testing Certification ..........................................................................................................................................19 
 

---

## Page 4

[[SFT]] Clearing Testing Guide 
About This Guide 4 
ABOUT THIS GUIDE 
This document is not legally binding and is only for information purposes. 1 It contains information designed to 
help clients gain a high-level understanding in preparation for the upcoming testing of your [[securities]] Financing 
Transaction ([[SFT]]) Clearing service. As with any testing program, the goal is to ascertain the proper flow of 
information so that you can successfully participate in the [[SFT]] Clearing service.  
As you review this document, a successful test might require a close coordination between your company and 
your testing partners, as well as a coordinating input and output communication among multiple [[DTCC]] systems 
and your firm’s internal systems. Depending on your role within [[SFT]] Clearing service, you will be getting some 
or all of the message traffic. 
For ease of reference, the terms [[SFT]] and loan are used interchangeably in this document.  
Commonly Used Acronyms and Terms 
Acronym Name Description 
 Agent Clearing [[Member]] An [[NSCC]] full-service [[Member]] permitted to novate to [[NSCC]] SFTs 
that it has executed as agent of behalf of its customers with a 
third-party [[NSCC]] [[Member]]. 
 Agent Client An institutional client of an Agent Clearing [[Member]] that is eligible 
to participate in lending-only or borrowing-only activity through an 
omnibus account of its Agent Clearing [[Member]] on the books of 
[[NSCC]] (Agent Clearing [[Member]] Customer Omnibus Account). 
Agent Clients are not members of [[NSCC]], and [[NSCC]] shall not 
have any liability or obligation to any Agent Client. 
 Approved [[SFT]] Submitter Submits a matched [[SFT]] to [[NSCC]] on a locked-in basis. May be an 
[[NSCC]] [[Member]] or a third-party vendor. All data submitted into the 
[[SFT]] Clearing service must come through an Approved [[SFT]] 
Submitter who has been authorized to submit SFTs to [[NSCC]] on 
behalf of one or more [[NSCC]] members. 
CDTS Common Data Transfer System Server-to-server message and file transport facility that supports 
receiving input data, retrieving output data, and processing data to 
[[participant]] firms through SWIFT and SMART protocols. 
FIX/MQ Financial Information 
eXchange/Message Queue 
Protocol used to send and receive messages leveraging the tag-
based FIX format using MQ or the FIX engine.  
MRO Machine-readable output Command supported output that is machine-readable.  
PROD Production Production environment. 
 [[NSCC]] Full-Service [[Member]] Any [[NSCC]] full-service [[Member]] that files a W-9 with the IRS can 
apply to participate in the [[SFT]] Clearing service. As described 
 
1 l This document should not be regarded as a substitute for the [[NSCC]] rules and procedures. In all cases, Members should refer to the [[NSCC]] rules and 
procedures for a complete statement of [[NSCC]]’s rules, procedures, [[obligations]], and requirements. Nothing in t his document shall be deemed to impose any 
[[obligations]] on [[NSCC]] that are not set forth in the [[NSCC]] rules and procedures, and in the case of any discrepancy between this document and the [[NSCC]] rules 
and procedures, the [[NSCC]] rules and procedures shall govern. The [[NSCC]] Rules and Procedures are available at https://www.[[DTCC]].com/legal/rules -and-
procedures. 

---

## Page 5

[[SFT]] Clearing Testing Guide 
About This Guide 5 
Acronym Name Description 
above, participation requires opening a separate [[SFT]] Clearing 
account at [[NSCC]] that will be eligible only for the clearance of [[SFT]] 
activities. The [[SFT]] Clearing account must be linked to a [[DTC]] 
settling account. 
PSE [[participant]] Services Environment Testing environment. 
SAS  [[securities]] Financing Accounting 
System 
Responsible for maintaining the [[settlement]] status of an [[SFT]] and 
acts as a hub between UTC and [[DTC]]. SAS determines what to 
send to [[DTC]] for [[settlement]] and when to send it. It also updates 
[[NSCC]]’s risk systems of [[settlement]] events to make sure the most 
current status of an obligation is provided to the risk systems for 
risk management. 
 Sending Entity Identifies the source submitting a trade or transaction. Used in 
conjunction with the Sending Subsystem and Trade Sequence 
Number to uniquely identify the trade message. Value 
predetermined by [[NSCC]]. 
[[SFT]] Clearing [[securities]] Financing Transaction 
([[SFT]]) Clearing 
Central clearing service that enables overnight borrowing, lending, 
and REPO transactions for [[NSCC]] full-service members and 
institutional clients who are sponsored into [[NSCC]] by Sponsoring 
Members. 
 Sponsoring [[Member]] An [[NSCC]] full-service [[Member]] permitted to novate to [[NSCC]] its 
principal SFTs with its Sponsored Members. 
 Sponsored [[Member]] Eligible institutional client of a Sponsoring [[Member]]. 
UTC Universal Trade Capture Trade recording and validation application that communicate 
through messages with marketplaces, exchanges, clearing firms, 
and service providers. 
 
  

---

## Page 6

[[SFT]] Clearing Testing Guide 
About This Guide 6 
Accessing [[DTCC]] Learning 
Prior to commencing testing with [[DTCC]], [[SFT]] Clearing clients are encouraged to visit and familiarize 
themselves with the [[DTCC]] Learning site. [[DTCC]] has developed a complete library of important [[SFT]] Clearing 
content that is designed to help firms gain an understanding of the service and the onboarding process. This 
library includes: 
• [[SFT]] Clearing General Service Guide 
• Input Message Layouts 
• Output Message Layouts 
• MRO Output Layouts (and others) 
For [[SFT]] Clearing content, see the [[DTCC]] Learning Center at: 
https://dtcclearning.com/products-and-services/equities-clearing/[[SFT]]-clearing/[[SFT]]-clearing-documentation.html  
Note:  
To view any information in the [[DTCC]] Learning site, you must first register directly through the [[DTCC]] Learning 
site. The registration process takes about one business day. 
[[DTCC]] Relationship Management Team 
One of the first steps in your firm’s onboarding process is to contact the [[DTCC]] [[SFT]] Clearing Relationship 
Management Team. Your [[SFT]] Clearing Relationship Manager will introduce you to the [[SFT]] Clearing service 
and the onboarding process as well as answer your questions. Your [[SFT]] Clearing Relationship Manager will 
also introduce you to other [[DTCC]] groups that will work alongside you in support of your [[SFT]] Clearing 
application process. Among these, the [[DTCC]] Integration Team will be the primary point of contact for your [[SFT]] 
Clearing onboarding and testing. 
Phase-Zero: Pre-Test Preparation 
As a part of the initial work with your [[SFT]] Clearing Relationship Manager, [[DTCC]] personnel can facilitate an 
[[SFT]] Clearing input/output demonstration to familiarize you with how the [[SFT]] Clearing service interacts with 
clients. 
To this end, [[DTCC]] has prepared a demo that covers the following input/output scenarios:  
• Entering a new loan into the [[SFT]] Clearing service, such as sending an on-leg message. 
• Extending a loan for an extra day, such as sending a roll message. 
• Sending a loan modification message, such as rate modification. 
• Closing the loan, for example, sending a send-to-settle message. 
Contact your [[SFT]] Clearing Relationship Manager to arrange your demo. 
  

---

## Page 7

[[SFT]] Clearing Testing Guide 
About This Guide 7 
[[DTCC]] Integration Team 
After your initial conversation with your [[SFT]] Clearing Relationship Manager takes place, the [[DTCC]] Integration 
Team will guide you through the onboarding process and help you complete your [[SFT]] Clearing testing. Your 
onboarding process will include the following: 
• Kick-off presentation 
• Connectivity discussions 
• Business requirements 
• Certifying the interface – conformance testing 
• Entitlements 
• Additional documentation as needed 
• Selection of the testing scope approach 
• Case testing and the final certification 
As a part of your pre-test preparation stage, the [[DTCC]] Integration Team will work with you to ascertain that 
your firm has all its enabling components ready to commence testing. Without these components, testing 
cannot take place. These include: 
• Connectivity. 
• [[SFT]] Clearing Account Number for [[SFT]] Clearing Members, if applicable. 
• Sending Entity Identifier for Approved Trade Submitters, if applicable. 
• Approved [[SFT]] Submitter-to-[[SFT]] Clearing [[Member]] relationship set up, including the relationship with 
[[DTCC]] test accounts. 
• Access to the PSE (testing) region. 
PSE Region Access ([[DTCC]] Testing Environment) 
Your [[SFT]] Clearing testing will take place in the [[participant]] Services Environment (PSE), which is the [[DTCC]] 
testing environment. As part of your connectivity testing, you will need to secure your connection to both the 
PSE and Production (PROD) environments. The [[DTCC]] Integration Team will guide and assist you in this effort. 
At the end of your connectivity work, your firm will conduct a short calibration test to ascert ain that messages 
seamlessly flow from your firm to [[DTCC]] and/or from [[DTCC]] to your firm. Your firm might need to secure access 
to the [[SFT]] Clearing PSE environment even if it does not plan to receive transactions information from [[DTCC]] 
directly, but instead utilizes a third-party service bureau. As an example, your firm might elect to receive 
optional message confirmations, alongside your service bureau, for reconciliation purposes. T o enable this 
message flow, your firm will need the PSE access for testing. When discussing your application with the [[SFT]] 
Clearing Relationship Management and the [[DTCC]] Integration Team, share your firm’s business requirements 
to identify all testing enablers beforehand. 
Once successful, your firm will be ready from the connectivity standpoint to conduct the next round of testing. 

---

## Page 8

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 8 
TESTING SCOPE APPROACH 
Your firm should keep in mind that your participation role in the [[SFT]] Clearing service determines the extent of 
your input/output onboarding testing. Firms can functionally act as: 
• Approved [[SFT]] Submitters, or  
• Lender and/or [[Borrower]] or  
• Both Approved [[SFT]] Submitter and Lender and/or [[Borrower]] 
Note:  
While an [[NSCC]] [[Member]] is eligible to participate as an Approved [[SFT]] Submitter and as a lender and/or 
[[Borrower]] at the same time, non-[[Member]] third-party vendors may only act as Approved [[SFT]] Submitters and/or 
as service bureaus and facilitate [[NSCC]] Members’ interaction with [[NSCC]] and [[DTC]].  
Phase-One: Approved [[SFT]] Submitter Only Testing 
Approved [[SFT]] Submitters that want to test in preparation for the subsequent onboarding of their clients, need 
to test their system’s ability to interact with [[DTCC]] systems. They also need to test the Approved [[SFT]] 
Submitter’s ability to send and receive messages relating to the status of its submitted loans.  
The following table shows tests commonly conducted as a part of the Approved [[SFT]] Submitter onboarding 
process. Some of these tests ensure connectivity to [[DTCC]], proper interaction with the [[DTCC]] input/output 
systems, as well as your firm’s ability to input and update loans in the system, for example, case tests.  
Table 2. System-to-System Tests 
System Mode Test Name Description 
[[NSCC]] 
UTC 
FIX/MQ 
Input/Output 
Connectivity Test Approved [[SFT]] Submitter sends message to UTC and receives 
output. 
[[NSCC]] 
UTC 
FIX/MQ 
Input/Output 
Invalid/Reject 
Messages  
Loans submitted are not to be accepted by [[DTCC]]. The Approved 
[[SFT]] Submitter receives an appropriate admin message in response. 
[[NSCC]] 
UTC 
FIX/MQ 
Input/Output 
Exception 
Processing 
Data with a gap is submitted. [[DTCC]] responds to the gap. Approved 
[[SFT]] Submitter responds to the gap fill request from [[DTCC]]. 
[[NSCC]] 
UTC 
FIX/MQ 
Input/Output 
End of Day 
Processing 
End-of-day message is submitted. [[DTCC]] returns good night 
confirmation; out-of-balance [[EOD]] message. 
[[NSCC]] 
UTC 
FIX/MQ Input Volume Test Approved [[SFT]] Submitter submits high volume to test its capacity. 
[[NSCC]] 
UTC 
FIX/MQ Input Failover Test Optional testing of primary and failover connections for heartbeat or 
telnet only. 
[[NSCC]] 
UTC 
FIX/MQ Input Pre-Production 
Test 
[[NSCC]] and Approved [[SFT]] Submitter to confirm all Production 
Connections. 
After the systems are fully inter-operational, your firm is ready to conduct further testing.  

---

## Page 9

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 9 
Input/Output-Test Type Matrix 
To successfully participate in the [[SFT]] Clearing service, clients are to assess the extent of testing needed to 
support their roles. To this end, refer to the following table for the [[SFT]] Clearing input/output testing and select 
those that your firm will need to include as a part of your testing strategy. Depending on your prospective role 
in the [[SFT]] Clearing service, you will have to complete some, but not others, to become [[SFT]] Clearing certified. 
Keep in mind that while input is message-based only, output is message- and MRO-based. 
Note:  
Failure to accurately identify your testing scope at the outset might significantly delay your product launch. If 
you have questions about the test cases in this table, engage your [[DTCC]] Integration Team point person or 
your [[SFT]] Clearing Relationship Manager. 
The following table shows the required and optional available inputs and output types that you must test. For 
more information about the file formats, see the [[NSCC]] File Formats for [[SFT]] Clearing.  
Table 3. [[SFT]] Clearing Test Type Scope Input/Output Matrix 
# System Format Test Type 
Name 
Description Mandated for Certification 
1 [[NSCC]] 
UTC 
FIX/MQ Input [[SFT]] Clearing 
Transaction 
Message 
Submission of a New Loan, Pre-
established Loan, Roll, Send-to-
Settle, Cancel, Termination, 
Rate Modification or Buy-side 
message. 
• Approved [[SFT]] 
Submitter – YES (both 
Vendor and [[Member]]) 
• [[Member]] Only – NO 
2 [[NSCC]] 
UTC 
FIX/MQ Input Input [[EOD]] 
Totals (Good 
Night 
Message) 
Input format used by the 
Approved [[SFT]] Submitter that 
recaps the number of [[SFT]] 
message transactions sent to 
UTC for the processing day. 
This will be an end-of-day ([[EOD]]) 
balancing message that will be 
the last transaction message of 
the day sent by the Approved 
[[SFT]] Submitter. The [[EOD]] 
message will be used by UTC 
for reconciliation. 
• Approved [[SFT]] 
Submitter – YES (both 
Vendor and [[Member]]) 
• [[Member]] Only – NO 
3 [[NSCC]] 
UTC 
FIX/MQ Output Message 
Output 
Output format generated to the 
Approved [[SFT]] Submitter and 
Members that provides a real 
time update status (either 
Accepted or Rejected) of each 
[[SFT]] Clearing transaction 
message that was received by 
UTC after input submission.  
Note: A rejected message is 
sent just to the Approved [[SFT]] 
Submitter. 
• Approved [[SFT]] 
Submitter – YES (both 
Vendor and [[Member]]) 
• [[Member]] Only – 
OPTIONAL 

---

## Page 10

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 10 
# System Format Test Type 
Name 
Description Mandated for Certification 
4 [[NSCC]] 
UTC 
FIX/MQ Output Outbound 
Gap Fill 
Request 
Output generated to the 
Approved [[SFT]] Submitter alerting 
them that a transaction gap was 
detected by UTC. 
• Approved [[SFT]] 
Submitter – YES (both 
Vendor and [[Member]]) 
• [[Member]] Only – NO 
5 [[NSCC]] 
UTC 
FIX/MQ Output Outbound 
Buy-side 
cutoff 
Output generated that alerts that 
all maturing off-leg return 
transactions (from the prior 
business day buy-side trades) 
have been released from 
[[NSCC]]’s guaranty obligation. 
• Approved [[SFT]] 
Submitter – OPTIONAL 
(both Vendor and 
[[Member]])  
(if submitting buy-side 
trades) 
• [[Member]] Only – 
OPTIONAL (if 
submitting buy-side 
trades) 
6 [[NSCC]] 
UTC 
FIX/MQ Output [[EOD]] Output 
Totals 
Output generated to each 
[[Member]] that had transaction 
messages for the processing 
day that contains the aggregate 
total transactions, [[shares]], and 
amount. This is a reconciliation 
message. 
• Approved [[SFT]] 
Submitter – YES (both 
Vendor and [[Member]]) 
• [[Member]] Only – 
OPTIONAL 
7 [[NSCC]] 
SAS 
ISO MT545 
Output 
Made 
Message 
(Receiver) 
A MADE message generated to 
the deliverer of the [[SFT]] 
transaction. The deliverer would 
be the Lender for the "on-leg" 
and the [[Borrower]] for the 
"off-leg". The CDTS Product is 
CNSESFTO. 
• Approved [[SFT]] 
Submitter – YES (both 
Vendor and [[Member]]) (if 
[[Member]] submitting 
street-side trades) 
• [[Member]] Only – 
OPTIONAL 
8 [[NSCC]] 
SAS 
ISO MT547 
Output 
Made 
Message 
(Deliverer) 
A MADE message generated to 
the deliverer of the [[SFT]]. The 
deliverer would be the Lender 
for the "on-
leg" and the [[Borrower]] 
for the "off-leg". The CDTS 
Product is CNSESFTO. 
• Approved [[SFT]] 
Submitter – YES (both 
Vendor and [[Member]])  
(if [[Member]] submitting 
street-side trades) 
• [[Member]] Only – 
OPTIONAL 
9 [[NSCC]] 
SAS 
ISO MT548 
Output 
Loan Status 
Update 
A status UPDATE message 
generated to both the receiver 
and deliverer. The message is 
used to inform subscribers about 
changes to the status of their 
[[SFT]] loan transactions such as 
pending, terminated, etc. from 
drops, non-returned fails, 
corporate actions, buy-ins, rate 
modifications, exits and cancels. 
The CDTS Product is 
CNSESFTO. 
• Approved [[SFT]] 
Submitter – YES (both 
Vendor and [[Member]]) 
• [[Member]] Only – 
OPTIONAL 

---

## Page 11

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 11 
# System Format Test Type 
Name 
Description Mandated for Certification 
10 [[NSCC]] 
SAS 
MRO Output 
AR# 02043624/ 
PSE 02983624 
[[EOD]] 
Outstanding 
Loan 
This is an end-of-day ([[EOD]]) 
MRO that reports to each 
[[Member]] their [[SFT]] Clearing 
street-side loans outstanding 
against [[NSCC]] at the end of the 
business day (which is around 
5:30 PM ET). It will also report 
any open recalls against those 
SFTs. The file will be distributed 
at approximately 5:45 PM ET. A 
[[Member]] can use this file to 
balance to their overnight rebate 
interest amount (debit or credit) 
that will be applied to their Fed 
Funds [[settlement]] (FFS) code 
130 balance (Rebate Interest) 
on their [[NSCC]] [[participant]] 
Account Statement for the next 
business day. 
• Approved [[SFT]] 
Submitter – OPTIONAL  
(both Vendor and 
[[Member]]) 
• [[Member]] Only – YES 
11 [[NSCC]] 
SAS 
MRO AR# 
02043623 / 
PSE 02983623 
[[EOD]] Mark-to-
Market 
This is an end-of-day Mark-to-
Market MRO that is generated 
after [[DTC]] drop cutoff time. A 
[[Member]] can use this file to 
balance their "mark" net 
debit/credit amount resulting 
from price differential and deliver 
order ([[DO]]) off-leg returns (not 
rolled) that did not settle at [[DTC]] 
where [[NSCC]] had to process a 
[[mark-to-market]] on the unsettled 
transaction. These marks will be 
applied to a firm’s Fed Funds 
[[settlement]] (FFS) code 131 
balance ([[SFT]] Marks) on their 
[[NSCC]] [[participant]] Account 
Statement. 
• Approved [[SFT]] 
Submitter – NO (both 
Vendor and [[Member]]) 
• [[Member]] Only – YES 
12 [[NSCC]] 
SAS 
MRO AR# 
02043626 / 
PSE 02983626 
Eligible 
Security 
This is an MRO file that provides 
a list of [[securities]] eligible for 
[[SFT]] Clearing processing. 
 
 
 
• Approved [[SFT]] 
Submitter – YES (both 
Vendor and [[Member]]) 
• [[Member]] Only – 
OPTIONAL 
13 [[NSCC]] 
SAS 
MRO AR# 
02040343 / 
PSE 02980343 
Night 
Miscellaneous 
Activity 
(Extended) 
This is an MRO file submitted 
approximately 12:30 A.M. EST 
(after the night cycle completes). 
It includes all the recorded 
entries resulting from an update 
• Approved [[SFT]] 
Submitter – NO (both 
Vendor and [[Member]]) 
• [[Member]] Only – YES 

---

## Page 12

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 12 
# System Format Test Type 
Name 
Description Mandated for Certification 
to an outstanding [[SFT]] after the 
processing of a buy-in 
execution, corporate action, 
termination, or exit. These 
events typically result in a 
collection/payment of money by 
[[NSCC]] against the contra 
members to the [[SFT]]. In some 
cases, the recorded entries 
result in no payment (for 
example, name change). 
Members should use this file 
(along with the Daytime 
Miscellaneous Activity File 
MRO) to balance to their Fed 
Funds Money [[settlement]] Code 
132 on the [[NSCC]] [[participant]] 
Account Statement. 
14 [[NSCC]] 
SAS 
MRO AR# 
02040331 / 
PSE 02980331 
Day 
Miscel
laneous 
Activity 
(Extended) 
This is an MRO file submitted 
approximately 3:30 P.M. EST 
(after the day cycle completes). 
It includes all the recorded 
entries resulting from an update 
to an outstanding [[SFT]] after the 
processing of a buy-in 
execution, corporate action, 
termination, or exit. These 
events typically result in a 
collection/payment of money by 
[[NSCC]] against the contra 
members to the [[SFT]]. In some 
cases, the recorded entries 
result in no payment (for 
example, name change). 
Members should use this file 
(along with the Night 
Miscellaneous Activity File 
MRO) to balance to their Fed 
Funds Money [[settlement]] Code 
132 on the [[NSCC]] [[participant]] 
Account Statement. 
 
• Approved [[SFT]] 
Submitter – NO (both 
Vendor and [[Member]]) 
• [[Member]] Only – YES 
15 [[NSCC]] 
SAS 
MRO AR# 
02043700 / 
PSE 02983700 
[[Dividend]] 
Activity 
This is an MRO output 
generated to Members that 
includes any [[Dividend]] payments 
that will be processed against 
their account by [[NSCC]] as a 
result of having open [[SFT]] 
positions on record date. The file 
includes all dividends that will be 
• Approved [[SFT]] 
Submitter – NO (both 
Vendor and [[Member]]) 
• [[Member]] Only – YES 

---

## Page 13

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 13 
# System Format Test Type 
Name 
Description Mandated for Certification 
paid the next business day. 
Members should use this file to 
balance their "[[Dividend]]" net 
debit/credit on their Fed Funds 
Money [[settlement]] Code 133 on 
the [[NSCC]] [[participant]] Account 
statement. 
16 [[NSCC]] 
SAS 
MRO AR# 
02043701 / 
PSE 02983701 
Due Bill 
Activity 
This is an MRO output 
generated to Members that 
includes any [[Dividend]] payments 
that will be processed against 
their account by [[NSCC]] as a 
result of having open [[SFT]] 
positions on due bill redemption 
date. The file includes all 
dividends that will be paid the 
next business day. Members 
should use this file to balance 
their "[[Dividend]]" net debit/credit 
on their Fed Funds Money 
[[settlement]] Code 133 on the 
[[NSCC]] [[participant]] Account 
statement. 
• Approved [[SFT]] 
Submitter – NO (both 
Vendor and [[Member]]) 
• [[Member]] Only – YES 
17 [[NSCC]] 
SAS 
AR# 02042959 
/PSE 02982959   
Record Date This is a print image report that 
shows outstanding loan 
positions on a record date/due 
bill redemption date for a 
declared record date distribution. 
No testing necessary. 
18 [[NSCC]] 
SAS 
ISO MT542 
Input 
Recall, 
Remove 
Recall, Buy-in 
Execution 
Input message used by the 
lender to instruct [[NSCC]] to 
process a recall, cancel recall, 
buy-in execution or cancel buy-
in execution on an outstanding 
[[SFT]]. 
 
 
• Approved [[SFT]] 
Submitter  
– YES (Vendor)  
– OPTIONAL ([[Member]]) 
 
• [[Member]] Only – 
OPTIONAL 
19 [[NSCC]] 
SAS 
ISO MT548 
Output 
Recall, 
Remove 
Recall, Buy-in 
Execution 
Output message to both the 
lender and [[Borrower]] providing 
the status update to recall, 
cancel recall, buy-in execution or 
cancel buy-in execution 
submitted to [[NSCC]] on an 
outstanding [[SFT]]. 
• Approved [[SFT]] 
Submitter  
– YES (Vendor)  
– OPTIONAL ([[Member]]) 
 
• [[Member]] Only – 
OPTIONAL 
Firms are responsible for evaluating the entire suite of all [[SFT]] Clearing input and output messages, as well as 
the available [[SFT]] Clearing MRO files, and deciding on what information they need to test to properly 
participate in the [[SFT]] Clearing service.  

---

## Page 14

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 14 
Keep in mind that some of the tests listed in the scenario table might comprise of multiple case scenarios. 
Some of these scenarios are mandatory, while others are optional. This is referred to as the Scenario Case 
Scope. Clients are to include all the mandated ones as a part of their testing approach but are also encouraged 
to include some or all optional scenarios, depending on their business needs. 
Message Input/Output Scenario Case Scope 
After your firm reviews the test scope in the scenario table, the next step is to review all relevant test cases for 
each grouping. For a list of all possible message cases, such as New [[SFT]]/On-leg Made, New [[SFT]]/On-leg 
Dropped, and others, along with their respective message sequence list and diagram, see the Message Flows 
section in the [[SFT]] Clearing General Service Guide. Keep in mind that your message testing will include the 
UTC, SAS, and [[DTC]] systems. 
Scenario cases are designed to ascertain that your firm’s systems can successfully interact in support of your 
[[SFT]] activity at [[DTC]]. Some of these scenarios are mandatory, while others are optional.  The mandatory cases 
can be completed as part of either your Phase-one or Phase-two testing.  In addition to these cases, you are 
encouraged to include some/all the optional cases, depending on your business needs.   
The following table lists all possible scenarios for you to test and identifies which are mandatory or optional for 
prospective firms: 
Table 4.  [[SFT]] Clearing Scenario Case Scope Matrix 
# Test Name [[SFT]] Clearing General 
Service Guide Location 
Scenario Testing 
1 New [[SFT]]/On-leg Made 6.1 Mandatory 
2 New [[SFT]]/On-leg Dropped 6.2.1, 6.2.2 Mandatory  
3 New [[SFT]]/On-leg Canceled 6.3.1, 6.3.2 Mandatory 
4 Pre-Established Bilateral [[SFT]]- On-leg Made 6.4 Mandatory 
5 Roll/On-leg Made 6.5 Mandatory 
6 Roll/On-leg Dropped 6.6 Mandatory 
7 Roll/On-leg Canceled and Original Off-leg 
Made 
6.7 Mandatory 
8 Roll/On-leg Canceled and Original Off-leg 
Return Dropped 
6.8 Mandatory 
9 No Roll/Original Off-leg Return Made 6.9 Mandatory 
10 No Roll/Original Off-leg Return Dropped 6.10 Mandatory 
11 Partial Roll/On-leg Made and Remainder Off-
leg Made 
6.11 Mandatory 
12 Partial Roll/On-leg Made and Remainder Off-
leg Dropped 
6.12 Mandatory 

---

## Page 15

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 15 
# Test Name [[SFT]] Clearing General 
Service Guide Location 
Scenario Testing 
13 Partial Roll/On-leg Dropped and Remainder 
Off-leg Made 
6.13 Mandatory 
14 Partial Roll/On-leg Dropped and Remainder 
Off-leg Dropped 
6.14 Mandatory 
15 No Roll on Term Date/Send-to-Settle 
Received and Original Off-leg Return Made 
6.15 Mandatory 
16 No Roll on Term Date/Send-to-Settle 
Received and Original Off-leg Return Dropped 
6.16 Mandatory 
17 Send-to-Settle (Accelerated Return From the 
Next Business Day to Current Business 
Day)/Off-leg Return Made 
6.17 Mandatory 
18 Send-to-Settle (Accelerated Return From the 
Next Business Day to Current Business 
Day)/Off-leg Return Dropped 
6.18 Mandatory 
19 Rate Modification 6.19 Mandatory 
20 [[SFT]] Loan Termination 6.20 Mandatory 
21 [[NSCC]] Exit 6.21 Mandatory 
22 Reject/Cancel of a New Loan On-leg Message 6.22 Mandatory 
24 Reject/Cancel of a Roll Message 6.23 Mandatory 
25 Cancel a [[DO]] Off-leg Return From the 
Previously Submitted Send-to-Settle 
(Accelerated) 
6.24 Mandatory 
26 Reject of a Cancel of [[DO]] Off-leg Return From 
the Previously Submitted Send-to-Settle 
(Accelerated) 
6.25 Mandatory 
27 [[NSCC]] Initiated Price Differential 6.26 Mandatory 
28 Corporate Actions 6.27.1, 6.27.2, 6.27.3, 
6.27.4, 6.27.5, 6.27.6, 
6.26.7 
Mandatory 
29 [[Broker]] Reorg 6.28 Mandatory 
30 Buy Side Trade Submission  Optional 
 
  

---

## Page 16

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 16 
Phase-One: [[SFT]] Clearing [[Member]] Only Testing 
The Phase-One [[SFT]] Clearing [[Member]] only testing is relevant only to those [[SFT]] participants that want to 
consume [[SFT]] messages and not rely solely on their respective third-party service bureaus.   
The purpose of the [[SFT]] Clearing [[Member]] Phase-One Testing is for clients to observe the processing of loans 
within the [[SFT]] Clearing service and its impact on client’s various outputs. To this end, your firm is to review the 
test scope in the table. See also the Message Flows section in the [[SFT]] Clearing General Service Guide.  
Note: 
Unlike the parallel Approved [[SFT]] Submitter Phase-One test, this test is done only between the client and 
[[DTCC]], for example, [[DTCC]]’s test accounts.  For more information, see the [[DTCC]] test accounts in Test Scope 
Approach.   
To facilitate this test, the [[DTCC]] Integration Team: 
• Submits prepared generic loans on behalf of a client into the system, which subsequently trigger 
customary output.   
• Preloads the client’s [[DTC]] account in the PSE environment with appropriate inventory to make subsequent 
[[DTC]] [[shares]] and funds movements possible.  These prepared trades show the client’s new [[SFT]] Account 
Number against the [[DTCC]] test account as the counterparty.   
In response to the loan input, the [[SFT]] Clearing service processes the input and subsequently returns all 
pertinent output to the [[SFT]] Clearing [[Member]], while the test account output remains at [[DTCC]].  The testing 
client is responsible for receiving the output from [[DTCC]] systems and sending it downstream within its firm, if so 
desired.  You should keep in mind that both [[NSCC]] and [[DTC]] components ought to be in-scope for your tests.  
Alongside [[NSCC]], [[DTC]] plays an important part in the process by facilitating the movement of [[shares]] and funds 
as a result of changes to the loan status.  Testing this component is critical to the overall production readiness. 
Note: 
While the [[SFT]] Clearing [[Member]]-only testing can be used to test all scenarios that an [[SFT]] Clearing [[Member]] is 
likely to encounter in the course of a regular business day, the goal of Phase-One testing is to ascertain the 
readiness of the [[Member]]’s systems as well as to confirm that the system can submit and receive different 
message types.  Extensive case testing should be addressed as part of your Phase- Two test with your 
Approved [[SFT]] Submitter. 
  

---

## Page 17

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 17 
Phase-Two: Approved [[SFT]] Submitter and [[SFT]] Clearing [[Member]] 
Testing 
When both an [[SFT]] Clearing [[Member]] AND its selected Approved [[SFT]] Submitter have BOTH completed the 
Phase-One testing, they can at this point progress to conduct a coordinated testing amongst themselves.  In 
this case, the [[DTCC]] Integration Team will only observe the progress of your test.  The goal of Phase- Two 
Testing is to conduct a loan input/output test, which objective is to trace the full lifecycle of your loan.  
Depending on your business circumstances, testing alongside a business partner, such as an Approved [[SFT]] 
Submitter (or vice versa) is likely to provide a much greater benefit to all parties involved, than a one- party test 
only.  Just as in the [[SFT]] Clearing [[Member]] Phase-One testing, this test should also involve the firm’s [[DTC]] 
function. 
Unlike the Phase-One test, which requires coordinating only between the firm and [[DTCC]] Integration Team, the 
input/output test might require greater coordination, depending on the selected approach.  These might 
include: 
• Approved [[SFT]] Submitter (Input) and [[SFT]] Clearing [[Member]] (Output) – In this test, an Approved [[SFT]] 
Submitter enters new loans and manages the input.  The [[SFT]] Clearing [[Member]] receives all pertinent 
outputs, including MROs, [[DTC]] output, etc. 
• [[SFT]] Clearing [[Member]] (Input and Output) – This test is possible in instances when the [[SFT]] Clearing 
[[Member]] acts as both an Approved [[SFT]] Submitter and a [[Borrower]] or Lender.   
The mechanics of the Phase-Two testing include submitting a loan between (i) a participating [[SFT]] Clearing 
[[Member]], whose [[NSCC]] Account Number is a party to the loan and (ii) a [[DTCC]] internal -test account, which 
takes the role of the counterparty.  It can also be done using the testing firm’s other [[SFT]] Clearing Account 
Numbers, if any, or another [[SFT]] Clearing client’s [[SFT]] Clearing Account Number.  Even though the test might 
occur completely outside of the [[DTCC]] test accounts, close coordination with the [[DTCC]] Integration Team is 
required.  [[DTC]] accounts of the test brokers are to be preloaded with proper inventories to facilitate the desired 
response from the [[NSCC]] SAS system.   
Note: 
A relationship between the Approved [[SFT]] Submitter and [[SFT]] Clearing [[Member]] must  be established first for 
loans to flow freely through the [[DTCC]] systems. 
In response to the loan input by the Approved [[SFT]] Submitter, the [[SFT]] Clearing service  returns all pertinent 
output to the Approved [[SFT]] Submitter as well as the [[SFT]] Clearing [[Member]] firm and or its third- party service 
bureau, while the test account output remains at [[DTCC]]. 
  

---

## Page 18

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 18 
MRO Testing (SAS File-Output Only) 
As a part of the overall effort, you should consider testing various available MRO outputs.  Unlike messaging 
testing, which pertains to both Approved [[SFT]] Submitters as well as [[SFT]] Clearing [[Member]] firms and/or their 
third-party service bureaus, the MRO output is provided solely to the [[SFT]] Clearing [[Member]] firms and/or their 
third-party service bureaus, and only these entities can conduct the MRO test.  
Access the MRO output, files, and reports from the [[NSCC]] File Formats for [[SFT]] Clearing  or the File and 
Report Layouts section of the [[SFT]] Clearing General Service Guide. The relevant file list includes: 
• Outstanding Loan MRO AutoRoute [[ID]]: Production 02043624 / PSE 02983624 
• End of Day ([[EOD]]) [[mark-to-market]] MRO AutoRoute [[ID]]: Production 02043623 / PSE 02983623 
• Eligible Security MRO: AutoRoute [[ID]] 02043626 / PSE 02983626 
• Record Date Print Image: AutoRoute [[ID]] 02042959 / PSE 02982959 
• [[Dividend]] Activity MRO: AutoRoute [[ID]] 02043700/PSE 02983700 
• [[Dividend]] with Due Bill Activity MRO: AutoRoute [[ID]] 02043701 / PSE 02983701  
• Miscellaneous Activity (Extended) MRO: AutoRoute [[ID]] 02040343 / PSE 02980343 (Night) and 02040331 
/ PSE 02980331 (Day) 
Firms should keep in mind that MRO file testing needs to occur in conjunction with pertinent input that 
generates the covered data.  
Note: 
Not all MRO testing can be done solely using the client’s loan input.  Testing of your [[Dividend]] MRO files 
requires close coordination between your testing team and the [[DTCC]] Integration Team because following your 
initial successful input of loans, a [[Dividend]] event needs to be triggered internally by the [[DTCC]] Integration 
Team to produce an appropriate funds transfers between the counterparties in the test environment. 
Test Security (Symbol) 
Use the following [[securities]] in all the [[SFT]] Clearing testing: 
Symbol  Description    [[CUSIP]] 
FB Facebook Inc 30303M102 
AMZN Amazon.com Inc 023135106 
AAPL Apple Inc. 037833100 
NFLX Netflix, Inc 64110L106 
GOOG Alphabet Inc 02079K107 
Discuss any additional security needs that your firm might have with the [[DTCC]] Integration Team.  
  

---

## Page 19

[[SFT]] Clearing Testing Guide 
Testing Scope Approach 19 
Testing Schedule 
[[DTCC]]’s PSE environment is open to testing for prospective [[SFT]] Clearing clients. To initiate testing, email the 
[[DTCC]] Integration Team at NSCCIntegration@[[DTCC]].com.   
Testing Certification 
As specified in the above sections, [[SFT]] Clearing testing is mandatory to be admitted to the [[SFT]] Production 
environment.  As a prospective [[SFT]] Clearing client, you must successfully test all mandatory components of 
your Test Type Scope and Scenario Test Scope.  Keep in mind that your firm is encouraged to conduct other 
tests beyond the mandated scope, depending on your [[SFT]] Clearing profile type. 
The [[DTCC]] Integration Team will be tracking your firm’s testing progress. Towards the end of testing, the [[DTCC]] 
Integration Team will request that you confirm you have completed testing and are ready for production. 
 

---

## Page 20

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 