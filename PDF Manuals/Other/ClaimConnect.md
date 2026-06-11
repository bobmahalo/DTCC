---
title: "ClaimConnect™ Service Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ClaimConnect.pdf"
pages: 17
size: "197.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ClaimConnect™ Service Guide

**Original File:** [ClaimConnect.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ClaimConnect.pdf)  
**Category:** Other  
**Total Pages:** 17  
**File Size:** 197.2 KB  

---

## Page 1

 
 
 
[[Asset]] SERVICES 
CLAIMCONNECT™ SERVICE GUIDE 
 
MARCH 28, 2023 
 


---

## Page 2

 
 
TABLE OF CONTENTS 
Important Legal Information ............................................................................................................................... 3 
About the ClaimConnect™ Service .................................................................................................................... 6 
Introduction ......................................................................................................................................................... 6 
Overview............................................................................................................................................................ 6 
About ClaimConnect ......................................................................................................................................... 7 
Defined Terms ................................................................................................................................................... 7 
Preparing to Use ClaimConnect ........................................................................................................................ 8 
ClaimConnect via the MyDTCC Portal ............................................................................................................ 8 
ClaimConnect via the APIs .............................................................................................................................. 9 
Claim Lifecycle ................................................................................................................................................... 10 
About .................................................................................................................................................................10 
Submitting a Claim ............................................................................................................................................10 
Claim States ....................................................................................................................................................11 
Claim Validation and Matching ........................................................................................................................12 
Modifying / Canceling a Claim .........................................................................................................................12 
Affirming a Claim .............................................................................................................................................13 
DKing / Un-DKing a claim................................................................................................................................13 
Querying Claims ..............................................................................................................................................14 
CLAIM APPROVAL ............................................................................................................................................. 15 
About .................................................................................................................................................................15 
The Claim Approval Process ............................................................................................................................15 
CLAIM [[settlement]] ......................................................................................................................................... 17 
About .................................................................................................................................................................17 
How Claims Settle.............................................................................................................................................17 
 

---

## Page 3

 
 
IMPORTANT LEGAL INFORMATION 
The contents of all Service Guides constitute "Procedures" of The [[Depository Trust Company]] ("[[DTC]]") as 
defined in the Rules of [[DTC]]. If Participants or other authorized users of [[DTC]]'s services fail to follow these 
Procedures precisely, [[DTC]] shall bear no responsibility for any losses associated with such failures.  
In connection with their use of [[The Corporation]]’s services, Participants and Pledgees must comply with all 
applicable laws, including all applicable laws relating to [[securities]], taxation, and money laundering, as well as 
sanctions administered and enforced by the Office of Foreign Assets Control (“OFAC”).  As part of their 
compliance with OFAC sanctions regulations, all Participants and Pledgees must agree not to conduct any 
transaction or activity through [[DTC]] that violates sanctions administered and enforced by OFAC.  
From time to time, [[DTC]] receives from outside sources notices and other documents, including corporate action 
information, and communications concerning financial assets. Although [[DTC]] may make certain of such 
documents and communications, or extracts therefrom, ("Information") available to Participants and other 
authorized users, it shall be under no obligation to [[DO]] so nor, having once or more done so, shall [[DTC]] have a 
continuing obligation to make available Information of a certain type. Information is not independently verified 
by [[DTC]] and is not intended to be a substitute for obtaining advice from an appropriate professional advisor. 
Therefore, Participants and other authorized users are advised to obtain and monitor Information 
independently. In addition, nothing contained in Information made available to Participants and other 
authorized users shall relieve them of their responsibility under [[DTC]]'s Rules and Procedures or other 
applicable contractual [[obligations]] to check the accuracy, where applicable, of [[participant]] Daily Activity 
Statements and all other statements and reports received from [[DTC]] and to notify [[DTC]] of any discrepancies. 
[[DTC]] DOES NOT REPRESENT THE ACCURACY, ADEQUACY, TIMELINESS, COMPLETENESS, OR 
FITNESS FOR ANY PARTICULAR PURPOSE OF ANY INFORMATION (AS DEFINED ABOVE) PROVIDED 
TO PARTICIPANTS AND OTHER AUTHORIZED USERS, WHICH IS PROVIDED AS -IS. [[DTC]] SHALL NOT 
BE LIABLE FOR ANY LOSS RELATED TO SUCH INFORMATION (OR THE ACT OR PROCESS OF 
PROVIDING SUCH INFORMATION) RESULTING DIRECTLY OR INDIRECTLY FROM MISTAKES, 
ERRORS, OR OMISSIONS, OTHER THAN THOSE CAUSED DIRECTLY BY GROSS NEGLIGENCE OR 
WILLFUL MISCONDUCT ON THE PART OF [[DTC]]. Further, such Information is subject to change. Part icipants 
and other authorized users should obtain, monitor, and review independently any available documentation 
relating to their activities and should verify independently information received from [[DTC]].  
[[DTC]] SHALL NOT BE LIABLE FOR: (1) ANY LOSS RESULTING DIRECTLY OR INDIRECTLY FROM 
INTERRUPTIONS, DELAYS, OR DEFECTS ARISING FROM OR RELATED TO ITS SERVICES; AND (2) 
ANY SPECIAL, CONSEQUENTIAL, EXEMPLARY, INCIDENTAL, OR PUNITIVE DAMAGES.  
The services provided by [[DTC]] to its Participants and other authorized users are provided only pursuant to the 
terms and conditions of the Participants Agreement, which references the Rules and Procedures of [[DTC]], 
and/or other contractual documents (collectively, the "Contractual Documents"). [[DTC]]'s [[obligations]] to 
Participants and other authorized users are therefore contractual in nature and are limited solely to those 
[[obligations]] expressly set forth in the Contractual Documents. Participants and other authorized users are 
obligated to, among other things, follow precisely the procedures outlined in the Contractual Documents and 
provide [[DTC]] with complete and accurate information. In accepting financial assets from Participants and/or 

---

## Page 4

 
 
providing services to other authorized users, [[DTC]] relies, among other things, upon the duty of P articipants and 
other authorized users to exercise diligence in all aspects of each transaction processed through [[DTC]].  
Participants and other authorized users expressly acknowledge that the services provided by [[DTC]] are 
ministerial in nature. Moreover, as further reflected by [[DTC]]'s fee structure (which typically bears no relationship 
to the dollar value of any given transaction), [[DTC]] does not accept any risk of loss to Participants, other 
authorized users and possible third party beneficiaries with respect to transactions being processed by [[DTC]].  
Copyright © 2023 by The [[Depository Trust Company]] ("[[DTC]]"). All rights reserved. This work (including, without 
limitation, all text, images, logos, compilation and design) is copyrighted, is proprietary, and is intend ed for the 
exclusive use of [[DTC]]'s Participants and other authorized users of [[DTC]]'s services. If this work is received in 
any electronic medium, authorized users of this work are permitted the limited right to make reproductions and 
transmissions necessary for downloading and storage of this work on the users' computers. Such users are 
also permitted to print one or more paper copies from the electronic version for their own use. Other than to 
this limited extent, no part of this work (including any paper copies thereof or print versions thereof) may be 
altered, reproduced or distributed (including by transmission) in any form or by any means, or stored in any 
information storage and retrieval system, without [[DTC]]'s prior written permission.  
REDISTRIBUTION BY PARTICIPANTS OF CERTAIN DATA FILES AND THE INFORMATION PROVIDED BY 
[[DTC]] IS STRICTLY PROHIBITED. FOR PURPOSES OF THIS PROCEDURE, “DATA FILES” SHALL MEAN 
THE BULK CORPORATE ACTIONS DATA FILES PROVIDED BY [[DTC]] TO PARTICIPANTS. EACH DATA 
FILE PROVIDED BY [[DTC]] TO A [[participant]] IS AND SHALL CONTINUE TO BE THE PROPERTY OF [[DTC]] 
AND NOT OF ANY [[participant]] IN RECEIPT THEREOF; THIS PROCEDURE DOES NOT CONSTITUTE 
THE GRANT OF ANY LICENSE IN, TO OR FOR THE USE OF, ANY DATA FILE OR INFORMATION 
DISTRIBUTED HEREUNDER OTHER THAN TO DISTRIBUTE TO ITS ACCOUNT HOLDERS INFORMATION 
CONTAINED IN ANY DATA FILE IT RECEIVES TO THE EXTENT SUCH INFORMATION IS RELEVANT TO 
THE SECURITY HOLDINGS OF SUCH ACCOUNT HOLDERS, OR IS OTHERWISE REQUIRED BY 
APPLICABLE LAW. 
Participants shall not use, distribute, transmit or otherwise make available any Data File or Information, with or 
without any service charge or fee, as the basis for or as part of a data product or service offered for commercial 
gain to any other person. [[DTC]]’s affiliate [[DTCC]] Solutions LLC (“[[DTCC]] Solutions”) has the right to license 
usage of the Data Files for purposes other than those permitted in the first paragraph of this Procedure, and 
any [[participant]] which wishes to use or distribute Data Files other than as contemplated hereby must contract 
directly with [[DTCC]] Solutions prior to any such distribution. This restriction includes, but is not limited to, service 
bureaus and other third parties, whether or not affiliated with a [[participant]], regardless of whether such person 
as previously itself received and/or used any Data Files in the past; such entities may obtain the Data Files 
only upon execution of a license agreement with [[DTCC]] Solutions. 
[[DTC]] shall have the right, but not the obligation, to audit the use and distribution of Inform ation and Data Files 
by any [[participant]]. Unauthorized use or distribution by [[participant]], any of its Affiliates or any of its account 
holders may result in a fine or other reasonable penalty determined by [[DTC]] in accordance with its rules in light 
of the facts and circumstances of such unauthorized use or distribution. By its acceptance of Information or any 
Data File, each [[participant]] agrees that, in addition to all other remedies that may be available, [[DTC]] and its 
affiliate [[DTCC]] Solutions shall be entitled to seek specific performance and injunctive and other equitable relief 
as a remedy for any breach of this Procedure by such [[participant]], its officers, employees, advisors or agents. 

---

## Page 5

 
 
Neither [[DTC]] nor [[DTCC]] Solutions shall be liable for any loss, cost or expense arising out of the use of any Data 
File or the Information contained therein, or the gross negligence or willful misconduct of any [[participant]] with 
respect to any Data File or the Information contained therein, provided hereunder, the failure of any [[participant]] 
to comply with these Rules and Procedures or applicable law, or for any consequential, special or punitive 
damages related thereto. 
The contents of the Service Guides are updated in different formats on a periodic basis. Participants and other 
authorized users of the Service Guides will find the most current version of the Service Guides, as well as [[DTC]] 
Important Notices which address the contents of the Service Guides, at http://www.[[DTCC]].com. You can access 
the Important Notices at http://[[DTCC]].com/legal/important-notices.aspx. [[DTC]] shall bear no responsibility for any 
losses associated with the failure of Participants or other authorized users to follow [[DTC]]'s most current Service 
Guides and/or Important Notices.  

---

## Page 6

 
 
ABOUT THE CLAIMCONNECT™ SERVICE  
Introduction 
Overview  
This guide describes [[DTC]]’s claims processing service – ClaimConnect – a Corporate Actions product.  Claim 
processing referred to in this guide is available on the ClaimConnect web application, via the MyDTCC portal, 
and for machine-to-machine processing via the ClaimConnect Application Programming Interfaces (“APIs”).  
Notes: 
• ClaimConnect users (“Users”) are responsible for ensuring that their ClaimConnect activities are accounted for 
within the service, and that all activities are managed and reconciled properly.  
• Users are responsible for the accurate reporting and withholding of taxes on transactions using the service.    
• ClaimConnect APIs provide callable endpoints for creating and deleting data resources as well as reading and 
updating data resource values. Information including specifications related to ClaimConnect APIs can be found 
using https://developer.[[DTCC]].com or by navigating through the MyDTCC portal menu on www.[[DTCC]].com.  
• ClaimConnect training is available on the [[DTCC]] Learning Center – https://dtcclearning.com/products-and-
services/[[Asset]]-services/claimconnect-service.html 
• Note: [[DTC]], as it deems appropriate, may extend any deadline, timeframe, or cutoff established by [[DTC]], including, 
without limitation, to (i) address operational or other delays that could reasonably affect the ability of [[DTC]], a 
[[participant]] or other stakeholder from meeting the deadline, timeframe, or cutoff; or (ii) allow [[DTC]] time 
operationally to exercise its existing rights under the Rules and Procedures.  In addition, times applicable to [[DTC]] 
are standards and not deadlines; actual processing times may vary, based upon the circumstances.  Any action 
taken by [[DTC]] in connection with this paragraph shall not establish a precedent for any situation that may occur in 
the future (or otherwise bind [[DTC]] in any manner).  [[DTC]] disclaims all liability for any losses and/or expenses 
incurred by a [[participant]], stakeholder or any third-party resulting from, relating to, or arising from (i) any action 
taken by [[DTC]] in connection with this paragraph, (ii) the determination of [[DTC]] to decline to take action pursuant to 
this paragraph, and/or (iii) the failure of a [[participant]], stakeholder or any third-party to meet any deadline, 
timeframe, cutoff or requirement established by a party other than [[DTC]].  
Participants can contact their Relationship Manager for more information. 
Note: 
It is the sole responsibility of Participants to perform a daily reconciliation of their activity and positions with the information, 
reports and statements provided by [[DTC]].  Participants must immediately report to [[DTC]] any discrepancy between their 
activity and positions with the information, reports and statements provided by [[DTC]] or other issues relating to the accuracy 
of the information, reports and statements provided by [[DTC]].  Such reports must be made to [[DTC]] by (i) calling the Client 
Support hotline at 1-888-382-2721 (and selecting [[Option]] 1, [[Option]] 1) to speak with a [[DTC]] representative and (ii) providing 
a written detailed description of the discrepancy to the [[DTC]] representative, or as otherwise directed by [[DTC]] in writing.  
[[DTC]] shall not be liable for any loss resulting or arising directly or indirectly from mistakes, errors, or omissions related to 

---

## Page 7

 
 
the information, reports or statements provided by [[DTC]], other than those caused directly by gross negligence or willful 
misconduct on the part of [[DTC]]. 
About ClaimConnect 
ClaimConnect is an optional service available to all Participants. The service enables Participants to bilaterally 
match and settle claim transactions in one centralized location. 
A claim or claim transaction in ClaimConnect is a request for cash (i.e., an [[Entitlement]]) from one [[participant]] to 
another [[participant]]. Typically, claims arise as a result of trading exceptions from a Corporate Action event, 
where an [[Entitlement]] needs to be delivered from one holder to another. Trading exceptions include, but are not 
limited to, trades outside of the market’s agreed upon [[settlement]] cycle, lack of due bill fail tracking, [[Stock]] loan 
or repo transaction discrepancy, or tax treaty differences. 
As described below, ClaimConnect offers various claim processing functions, including end-of-day [[settlement]] 
of cash claims through systematic [[securities]] Payment Orders (“SPOs”) generated and submitted by 
ClaimConnect at set times intraday (“[[settlement]] time”) on a [[settlement]] date. 
Note: 
ClaimConnect functionality available via ClaimConnect APIs is more limited than the full suite of functionality available via 
the web application through the MyDTCC portal, as described below. 
Defined Terms 
Following is a table of key ClaimConnect terms used throughout this guide: 
Term Definition 
Affirm Describes the act of accepting a claim. Also known as “Affirmation.” Once Affirmed, 
the claim is moved to a Matched state. Users can only Affirm through the MyDTCC 
portal, not via an API. 
Approval A feature to help Users manage the cash debits that would leave their account to 
satisfy claims by requiring preapproval of such claims or certain actions on those 
claims when a predetermined dollar threshold is met.  
Auto-match 
 
The process by which ClaimConnectTM automatically matches two like claims, based 
upon certain matching data elements, submitted by both parties to the claim, either 
through the MyDTCC portal or a ClaimConnect™ API. 
Cancelled Describes a claim that is later deleted by the User that submitted it, removing it from 
the system. Only the User that submitted the claim can cancel it and only before it is 
acted upon by the receiving counterparty or after the counterparty DKs the claim.  
Claim [[ID]] A unique claim identification number that is assigned to a claim after all required data 
elements are entered and the claim is submitted.  
Claim [[settlement]] Date The date on which a claim will settle, as agreed upon by the claim parties. It is a data 
element in the claim submission process.  

---

## Page 8

 
 
Term Definition 
Closed Describes a Matched claim that settles or fails to settle, as part of [[DTC]]’s end-of-day 
[[settlement]] process, by the close of the scheduled [[settlement]] day.  
DK Short for “Don’t Know.” A User can DK a claim that it does not recognize or does not 
agree with. Once DK’d, the claim will be moved to a DK-uncompared state. 
DK-uncompared The state of a claim that has been DK’d.  
Exact Match A requirement that certain data elements on two individual claims be identical for the 
claim to match.    
Matched Describes a claim that has been Affirmed or two like claims that have been Auto-
matched. Once Matched, the claim will settle on the Claim [[settlement]] Date or Settle 
After Match, as agreed by the parties to the claim.   
Settle After Match A [[settlement]] [[Option]] where a Matched claim will settle at the next scheduled 
[[settlement]] time, as compared to a future [[settlement]] date. Both parties to the claim 
must select the Settle After Match [[Option]].  
Security Payment Order 
(SPO) 
Used by Participants to collect [[Option]] contract premiums, [[mark-to-market]] open 
contracts such as [[Stock]] loans, and to settle claim transactions via ClaimConnect.   
Uncompared The state of a submitted claim that has not been Affirmed, Auto-matched, or DK’d.   
Un-DK The act of reversing or “undoing” a DK, which returns the claim to an Uncompared 
state.   
Validate The process of confirming data elements of a claim, either by a User Affirming a claim 
or systematically via Auto-match.  
Note:  
When using ClaimConnect, Users will notice that the system uses the terms “advisory” and “comparison.”  An advisory 
describes a claim from the perspective of the claim receiver (i.e., a claim receiver receives an “advisory”). A comparison 
describes a claim from the perspective of the claim submitter (i.e., a claim submitter submits a “comparison”). 
Preparing to Use ClaimConnect 
To use ClaimConnect, a [[participant]] need only request to be a Claim [[participant]] by contacting its Relationship 
Manager. [[DTC]] Account Administration will then update the [[participant]]’s account information in the [[DTC]] Entity 
Masterfile, indicating that the [[participant]] is now a [[Member]] of the service (i.e., a User).  
Once permissioned, a User can engage ClaimConnect in two ways: 
• the ClaimConnect application via the MyDTCC portal; and  
• the ClaimConnect APIs. 
ClaimConnect via the MyDTCC Portal 
When using ClaimConnect through the web application on the MyDTCC portal, Users have access to all 
ClaimConnect functionality, including: 

---

## Page 9

 
 
• submitting new claims; 
• modifying claims submitted by the User; 
• attaching documents to claims; 
• Canceling claims submitted by the User; 
• DKing and Un-DKing claims;  
• Affirming claims;  
• utilizing the ClaimConnect Auto-match feature; 
• establishing Approvals; and  
• searching all claims submitted or received by the User.  
Additionally, the ClaimConnect dashboard, available via the MyDTCC portal, offers a comprehensive overview 
of the User’s claim activity, as well as daily and weekly email alerts on the status of claims, and the ability to 
pull reports and export data for manipulation and analysis. 
ClaimConnect via the APIs 
The ClaimConnect family of APIs enables Users to automate the claim process. Although ClaimConnect™ 
functionality is more limited through the APIs (i.e., APIs cannot Affirm claims, attach documents to claims, 
access the ClaimConnect™ dashboard or establish an Approval), Users can still:  
• submit new claims; 
• modify claims that it submitted; 
• Cancel claims that it submitted; 
• utilize the ClaimConnect Auto-match feature; 
• DK and Un-DK claims; and 
• search all claims that it submitted or received.  
Each ClaimConnect function is described in greater detail below.  
Note: 
The ClaimConnect APIs can be used separately for machine-to-machine processing of claims or in combination with the 
ClaimConnect web application through the MyDTCC portal. For detailed specifications and usage guidelines regarding the 
ClaimConnect APIs, please refer to https://developer.[[DTCC]].com. 
Note: 
Unless otherwise noted, the functions described in this guide apply to both the ClaimConnect service via the web 
application and the APIs. 

---

## Page 10

 
 
CLAIM LIFECYCLE 
About 
ClaimConnect monitors claim activity throughout the processing day. Certain activities will change the status of 
a claim. This section describes the lifecycle of a claim, its states, and how validation and matching occurs.  
Submitting a Claim 
If overpaid or underpaid a cash [[Entitlement]], a User can create a claim against a claim counterparty through 
ClaimConnect. To create a claim, the ClaimConnect system will require certain data elements to be included, 
such as:  
• Claim Cross Reference (“Xref”); 
• [[CUSIP]]; 
• Event Type; 
• Credit / Debit; 
• Cash Claim Amount (USD); 
• Counterparty (or Contra Party); and 
• Claim [[settlement]] Date. 
In addition to the required data elements, Users have the [[Option]] to input additional data elements. Optional 
data elements can help Users differentiate similar claims. Such optional data elements include: 
• Corporate Action Identifier; 
• Ex-[[Dividend]] Date; 
• Record Date; 
• Payable Date; 
• Effective Date; 
• Amount Per Share; 
• Settle After Match; 
• Original Trade – Trade Date; 
• Original Trade – Contractual [[settlement]] Date; 
• Original Trade – Actual [[settlement]] Date; 
• Original Trade – Share Quantity; 
• Original Trade – Cash Amount; 
• Xref; and  
• [[participant]] Notes. 
To help expedite the claim [[settlement]] process, Users can attach a document to a claim, through the 
ClaimConnect web application in the MyDTCC portal, that provides further details about the claim.  
Once all required data elements are entered and the claim is submitted, the claim is assigned a Claim [[ID]].  

---

## Page 11

 
 
Note: 
A complete list of data elements and whether the data elements are required or optional can be found on the ClaimConnect 
[[DTCC]] Learning Center page. 
Note: 
To more easily identify claims and expedite the [[settlement]] process, claim submitters should work with claim counterparties 
during the submission process. 
Claim States 
Once submitted, claims can undergo several different states depending upon the actions taken by the parties 
to the claim. Claims can exist in the following states: 
• Matched;  
• Uncompared; 
• DK-uncompared; 
• Cancelled; or  
• Closed.  
A claim is Matched when:  
• it has been Auto-matched by the ClaimConnect system, or  
• it has been Affirmed by the counterparty to the claim.  
A claim is Uncompared when it is awaiting action by the counterparty. This occurs when:  
• a claim is initially submitted, without any further action taken on the claim;  
• a claim is modified by the submitting party before the counterparty has acted on it;  
• a claim is modified by the submitting party after it has been DK’d by the counterparty; or  
• a claim is Un-DK’d, without any further action taken on the claim.  
A claim is DK-uncompared when it has been DK’d by the receiving counterparty, and the submitting party has 
not yet acted on the counterparty’s DK. The DK-uncompared state is synonymous with an Uncompared status 
but is distinguished in this guide to better depict the workflow. 
A claim is Cancelled when the submitting party determines that the claim is no longer needed. This occurs 
when:  
• the submitting party Cancels the claim before it has been acted on by the counterparty, or  
• the submitting party Cancels a claim that has been DK’d by the counterparty.  
A claim is Closed when a Matched claim settles or fails to settle, as part of [[DTC]]’s end- of-day [[settlement]] 
process, by the close of the scheduled [[settlement]] day, as described below.  
Note: 
Once a claim is either Matched or Closed, it can no longer be modified, DK’d, or moved into an Uncompared state. If a 
correction needs to be made to a Matched or Closed claim, a new claim will need to be submitted. 

---

## Page 12

 
 
Note: 
As a short form for Matched, the ClaimConnect system denotes the Matched state as “Open” or “OPEN.” 
Claim Validation and Matching 
ClaimConnect is a validation and matching engine that continually monitors claims throughout their lifecycle in 
order to settle and close claims through [[DTC]]’s [[settlement]] process. This continuous processing allows for both 
the manual matching of claims (i.e., Affirmation) and systematic matching of two like claims (i.e., Auto-
matching) based on the alignment of certain data elements. 
Validation, the process of confirming claim data elements, can happen in two ways:  
• when a claim is Affirmed (i.e., by Affirming a claim, the receiving counterparty is confirming the claim’s 
data elements), or 
• when ClaimConnect Auto-matches two claims.  
Once Validated, a claim will switch from an Uncompared to a Matched state.  
If certain data elements of two different claims [[DO]] not agree, the claims cannot be Validated and, thus, cannot 
be Matched. Such claims will remain in an Uncompared state until action is taken upon one or both claims.  
Note: 
For a complete list of data elements that require Exact Match, please refer to the training materials found on the 
ClaimConnect [[DTCC]] Learning Center page. 
Note: 
If both parties to a claim submit their respective sides to the claim (i.e., a debit claim and a credit claim), and the two sides 
of the claim are Auto-matched, then the claim will be identified by the Claim [[ID]] associated with the debit side of the claim. 
The Claim [[ID]] of the credit side of the claim will be viewable in the claim’s audit history. 
Modifying / Canceling a Claim 
Claims can be modified or Cancelled as described below.   
A claim can be modified if and only if: 
• the modifying User is the User that submitted the claim; and 
• the claim is Uncompared;  
• the claim has not been Cancelled;  
• the claim has not been Matched; or 
• the claim has not been Closed. 

---

## Page 13

 
 
Note: 
Not all claim information can be modified after submission. Users should refer to the ClaimConnect user guides and other 
training materials to determine which fields can be modified. 
A claim can be Cancelled if and only if: 
• the Canceling User is the User that submitted the claim; and 
• the claim is Uncompared;  
• the claim has not been Matched; or 
• the claim has not been Closed. 
Note: 
Once a claim is Cancelled, no further action can be made on the claim.   
Affirming a Claim 
If a counterparty receives a claim and agrees with the details of the claim (i.e., the data elements), then the 
counterparty can Affirm the claim. Affirming a claim is a confirmation of the claim’s data elements and moves 
the claim into a Matched state. Once Affirmed, the claim will be settled on the Claim [[settlement]] Date or Settle 
After Match, whichever the parties agree to. 
Because of the efficiency of the Auto-match process between two claims, Affirmation usually occurs only when 
one side of a claim is submitted because it affords the counterparty enough time to Affirm the claim. If both 
sides of a claim are submitted, and the applicable data elements align, then Auto- match will likely Match the 
claims before either party has time to make an Affirmation.  
Claims can be Affirmed only: 
• “manually” via the MyDTCC portal, not through an API; 
• by the counterparty that received the claim; and 
• when the claim is Uncompared; or 
• when the claim is not Cancelled or Closed. 
Note: 
Once Affirmed, the claim will move to a Matched state and no further action is permitted on the claim. 
DKing / Un-DKing a claim 
If a counterparty receives a claim that it does not know or does not agree with, then it can DK the claim. DKing 
a claim will return it to the submitting party and change the state of the claim to DK-uncompared. The 
submitting party can then modify the claim or Cancel it. 
Claims can be DK’d only: 

---

## Page 14

 
 
• by the User that received the claim; and 
• when the claim is Uncompared; or 
• when the claim is not Cancelled or Closed. 
Users that DK a claim must provide a reason for the DK, such as: 
• bad quantity; 
• bad trade date; 
• bad [[settlement]] date; 
• bad amount; 
• bad counterparty (or contra party); 
• duplicate record; 
• invalid security identifier; 
• need paperwork; 
• need medallion stamp; 
• [[settlement]] date difference; 
• other bad data; or 
• wrong event type. 
A claim DK’d in error can be Un-DK’d (i.e., reversed) by the party, and only that party, that DK’d the claim. 
Once Un-DK’d, the claim will be in an Uncompared state. Uncompared claims can be modified or Cancelled by 
the submitting party, or they can be Affirmed or DK’d by the receiving party.  
Querying Claims 
ClaimConnect enables Users to query claims throughout the lifecycle of the claim. ClaimConnect has both 
search and report functions.  
There are two types of searches: 
• Quick Search to look up a specific claim using either the unique Claim [[ID]] or Xref that the User assigned to 
the claim, and 
• Advanced Search to search for a range of claim activity, including claims submitted by the User or by a 
counterparty. 
From the search results, Users can select a claim to view more detailed information.  
ClaimConnect also enables Users to view all of their claims as of a given date (either on a current or historic 
day), which can then be downloaded into a CSV (Comma-Separated Value) file format report. 

---

## Page 15

 
 
CLAIM APPROVAL 
About 
To assist Users with the management of their claims, ClaimConnect offers an Approval feature. The Approval 
feature requires certain actions on a claim to be approved by a separate User employee, if the claim amount 
meets a predetermined dollar threshold set by the User, before that action can be completed. This feature is 
designed to enable Users to better monitor and manage certain cash debits that are leaving their account to 
satisfy claims. 
The Claim Approval Process 
Users can activate the Approval feature by updating their ClaimConnect client profile. When doing so, the User 
also must set the dollar threshold that will trigger the Approval process. For example, if a User wants all debit 
claims equaling $100.00 or greater to be Approved, the User would set the Approval threshold to $100.00.     
When the Approval process is activated and a dollar threshold set, Approval by another User employee is 
required when the dollar threshold is met for claims that are: 
• new;  
• being Affirmed; 
• being modified; or 
• being Cancelled after being previously Approved. 
If a claim is modified so that the dollar amount of the claim no longer meets or exceeds a previously 
established approval threshold, then the modification will not need to be Approved. Conversely, if a claim is 
modified so that the dollar amount of the claim now meets or exceeds a previously established Approval 
threshold, then the claim will need to be Approved. If a previously Approved claim is modified but the claim 
amount remains unchanged (i.e., it still meets or exceeds the Approval threshold), then the claim will need to 
be re-Approved. 
New claims that are pending Approval will not have a claim state, and the counterparty to the claim will not see 
the claim until it is Approved. Once Approved, the claim will be moved to an Uncompared state.  
Approval is not required to DK or Un-DK a claim.   
In order to modify a new claim that is still pending Approval, the submitting User should reject the claim, make 
the modification, and resubmit it for Approval. If the claim has already been Approved, a modification may 
require re-Approval, if the Approval threshold is met.  
  

---

## Page 16

 
 
Claim Approvers must be different than the User employee that created the claim. Approvers can view the 
details of the claim prior to Approving.  
If an Approver rejects a claim, the claim will need to be resubmitted for Approval or Cancelled.   
Note: 
Because of the manual aspects of the Approval feature, the feature is not available via APIs.   

---

## Page 17

 
 
CLAIM [[settlement]]  
About 
For ClaimConnect to Close a claim, the paying counterparty (i.e., the payor account) must pay the receiving 
counterparty (i.e., the payee account). The payment must be settled via an SPO. Once the payee account has 
been credited and the payor account money owed, the claim will be Closed. This section explains the 
[[settlement]] and claim closure process. 
How Claims Settle 
Matched claims will generate a ClaimConnect SPO for [[settlement]] on either the Claim [[settlement]] Date, the 
next applicable daily [[settlement]] time if the Settle After Match indicator has been agreed to by both parties, or 
the first [[settlement]] time on the next [[settlement]] day if the current day is a holiday or non- [[settlement]] date. The 
SPO will credit the payee [[participant]] and debit the payor [[participant]] the claim amount and will then be 
incorporated into [[DTC]]’s end-of-day [[settlement]] process. 
Although the ClaimConnect SPO is similar to and functions like other [[DTC]] SPOs, it is unique to ClaimConnect 
and its [[settlement]] process in several ways: 
• the reason code for ClaimConnect SPOs is used only for ClaimConnect cash movements;  
• the ClaimConnect SPO cannot be instructed manually, as it is an automated process through the 
ClaimConnect service; and 
• the ClaimConnect SPO bypasses [[DTC]]’s Receiver Authorized Delivery (RAD) function, meaning that there 
is no additional approval or rejection process for the ClaimConnect SPO. 
ClaimConnect will Close the claim once it settles or fails to settle by the close of the [[settlement]] day. Closed 
claims cannot be reopened, modified, or processed again. If an adjustment is needed, a new claim will need to 
be submitted and processed. 
ClaimConnect SPOs are subject to [[DTC]]’s Risk Controls (i.e., [[collateral]] Monitor and Net Debit Cap) and will 
“recycle” (i.e., pend) if the SPO cannot satisfy those controls. If a ClaimConnect SPO does not “make” (i.e., 
settle) by the end of the [[settlement]] day, the SPO will be “dropped” (i.e., Closed). Details on the failed claim will 
be available using the [[settlement]] Web activity inquiry function.   
Note: 
The intraday [[settlement]] times for processing ClaimConnect SPOs can be found on the ClaimConnect [[DTCC]] Learning 
Center page. 
 
 
 