---
title: "Short Orange Portrait"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_b52_transfers_bp_mfs_20200320.pdf"
pages: 19
size: "416.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Short Orange Portrait

**Original File:** [net_b52_transfers_bp_mfs_20200320.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_b52_transfers_bp_mfs_20200320.pdf)  
**Category:** Other  
**Total Pages:** 19  
**File Size:** 416.6 KB  

---

## Page 1

 
 
NETWORKING  
B52 NETWORKING TRANSFERS: TRANSACTION TYPES 4, 8, AND 9 - BEST 
PRACTICES 
MARCH 2, 2020 
 
 
 


---

## Page 2

 
 
Copyright © 2020 by The Depository Trust & Clearing Corporation (“[[DTCC]]”). 
All rights reserved. This work (including, without limitation, all text, images, logos, compilation and design) is proprietary and 
protected by copyright, and is for the exclusive use of users authorized by [[DTCC]]. If this work is received from [[DTCC]] in any 
electronic medium, authorized users of this work are granted a limited, non-exclusive, non-transferable, non-sublicensable 
and freely revocable license to make reproductions and transmissions necessary for downloading and storage of this work 
on the users' computers and to print one or more paper copies from the electronic version for their own use. Other than to 
this limited extent, no part of this work (including any paper copies thereof or print versions thereof) may be printed, copied, 
altered, modified, posted, reproduced, displayed, published, sold, licensed, used or distributed (including by transmission) 
in any form or by any means, or stored in any information storage and retrieval system, without [[DTCC]]'s prior written 
permission. All product or service names are the property of their respective owners.
 
  
Trademarks 
All names of [[DTCC]] and its affiliates, and their products and services, referenced herein are either registered trademarks or 
service marks of, or trademarks or service marks of, [[DTCC]] or its affiliates in the U.S. or elsewhere. Other names of 
[[Companies]], products or services appearing in this Guide are trademarks or service marks of their owners. 
 
Disclaimer 
This document is not a legal document and the statements contained herein [[DO]] not set forth any legal [[obligations]] of [[DTCC]], 
National [[securities]] Clearing Corporation (“[[NSCC]]”) or any other [[DTCC]] subsidiary, nor [[DO]] any statements contained herein 
set forth any legal rights of any [[NSCC]] user.  All such legal rights and [[obligations]] are set forth in [[NSCC]]’s Rules & 
Procedures and each user’s Membership Agreement with [[NSCC]] (together, the “Legal Documents”).  The user is referred to 
the Legal Documents for a statement of all legal [[obligations]].  In general, unless the context clearly indicates otherwise, 
terms used in this document have the same meanings as in the Legal Documents. 
  
NEITHER [[DTCC]] NOR ANY OF ITS SUBSIDIARIES [[Warrants]] THE ACCURACY OR COMPLETENESS OF THE 
INFORMATION CONTAINED IN THIS DOCUMENT.  FURTHER, NEITHER [[DTCC]] NOR ANY OF ITS SUBSIDIARIES 
[[Warrants]] THE ACCURACY OR COMPLETENESS OF ANY OTHER WEB SITE WHICH THE USER MAY ACCESS 
THROUGH THIS DOCUMENT. THE INFORMATION CONTAINED IN THIS DOCUMENT IS NOT INTENDED TO BE A 
SUBSTITUTE FOR OBTAINING LEGAL OR TAX ADVICE FROM AN APPROPRIATE PROFESSIONAL ADVISOR. IN NO 
EVENT WILL [[DTCC]] NOR ANY OF ITS SUBSIDIARIES BE LIABLE FOR LOSSES OR DAMAGES, INCLUDING LOSS OF 
PROFITS OR CONSEQUENTIAL DAMAGES, ARISING OUT OF THE USE OF THIS DOCUMENT OR OTHER 
HYPERLINKED WEB SITES CONTAINED HEREIN. 
  
TO ENSURE COMPLIANCE WITH INTERNAL REVENUE SERVICE CIRCULAR 230, YOU ARE HEREBY NOTIFIED 
THAT: (A) ANY DISCUSSION OF FEDERAL TAX ISSUES CONTAINED OR REFERRED TO HEREIN IS NOT INTENDED 
OR WRITTEN TO BE USED, AND CANNOT BE USED, FOR THE PURPOSE OF AVOIDING PENALTIES THAT MAY BE 
IMPOSED UNDER THE INTERNAL REVENUE CODE, AND (B) AS A MATTER OF POLICY, [[DTCC]] DOES NOT 
PROVIDE TAX, LEGAL OR ACCOUNTING ADVICE AND ACCORDINGLY, YOU SHOULD CONSULT YOUR OWN TAX, 
LEGAL AND ACCOUNTING ADVISOR BEFORE ENGAGING IN ANY TRANSACTION.
 
  
By accessing this document, you acknowledge, accept and agree to the foregoing [[obligations]] and restrictions. 
 
Doc Info: March 2, 2020 
Publication Code: MFS194 
Service: Networking 
Title: B52 Networking Transfers: Transaction Types 4, 8, and 9 – Best Practices 
 
 
 
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 4 
Mass [[Broker]] to [[Broker]] transfer: Transaction Type 4 ....................................................................................... 5 
Standards ............................................................................................................................................................ 5 
Processing steps ................................................................................................................................................. 5 
Non-ACAT eligible: Transaction Type 8 ............................................................................................................ 7 
Background ......................................................................................................................................................... 7 
Standards ............................................................................................................................................................ 7 
Processing steps ................................................................................................................................................. 8 
ACAT Mutual Fund fail cleanup: Transaction Type 9 ..................................................................................... 10 
Background ....................................................................................................................................................... 10 
Standards .......................................................................................................................................................... 10 
Processing Steps .............................................................................................................................................. 11 
Networking transfer best practices: workflows for B52 Transaction Types 4, 8 and 9 .............................. 13 
Mass [[Broker]] to [[Broker]] (Transaction Type 4) – Workflow ................................................................................ 13 
Non ACAT Transfer (Transaction Type 8) Workflow ........................................................................................ 14 
ACAT MF Fail Cleanup (ACAT Reconciliation) Transaction Type 9 Workflow ................................................ 15 
Appendix: Firm to Firm Non-ACAT Transfer Request Form — Templates .................................................. 16 
Firm to Firm Non-ACAT Transfer Request Form .............................................................................................. 16 
Description of Firm to Firm Letter .................................................................................................................... 16 
Best Practices ................................................................................................................................................. 16 
Firm to Firm Non-ACAT Transfer Request Form Sample ............................................................................... 18 
 

---

## Page 4

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Overview 4 
OVERVIEW 
This document has been developed to provide best practices for Transaction Types 4 (Mass [[Broker]] to 
[[Broker]]), 8 (Non-ACAT eligible transfer) and 9 (ACAT Mutual Fund Fail Cleanup) when used for B52 
Transfers. 
 
 
 
 
 
  

---

## Page 5

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Mass [[Broker]] to [[Broker]] transfer: Transaction Type 4 5 
MASS [[Broker]] TO [[Broker]] TRANSFER: 
TRANSACTION TYPE 4 
Standards 
Firms have the [[Option]] of using the Mass [[Broker]] to [[Broker]] Conversion feature in Networking to expedite bulk 
movement of accounts from one Firm to another on records of the Fund.  Mass [[Broker]] to [[Broker]] Conversions 
can be accomplished in an automated and controlled environment through the Account Setup/Update/Transfer 
and Acknowledgment function in Networking.  
• Firm contact with the Fund should be made first to prepare them for the request, and inform them that the 
‘window’ should be opened, if applicable.  
• There should not be a prior ACAT transfer (FUL, PTR, PTD, RCR) that aged to Settle Close. 
• The control number to be used for share aging purposes will be the [[NSCC]] Networking control number, 
which is located on the B52 and then confirmed by the Fund on the F53 record.  The control or reference 
number to leverage for cost basis should be discussed between the parties, as cost basis matching 
information can also be passed between the parties outside of [[DTCC]]. 
• If the account is networked, and therefore, no underlying account number is available, the Credit/Debit 
Account Numbers should be populated in the Credit Sub-Account Number and Debit Sub-Account 
Number fields. 
 
Processing steps 
Listed below are the guidelines for processing a Mass [[Broker]] to [[Broker]] Conversion: 
1. The receiving Firm establishes new (shell) accounts on the Fund’s books. These “shell” accounts contain 
account setup information. 
a) The receiving Firm places its [[NSCC]] number in the Clearing/Settling Firm Number field of Record 
type B50.  The relaying of the receiving Firm’s [[NSCC]] number and the account matrix level for 
these new accounts is critical to the accurate processing of the conversion. 
b) Funds acknowledge back to the receiving Firm that the accounts were set up properly, using 
Record Type F53 by placing the receiving Firm’s [[NSCC]] number in the Clearing/Settling Firm 
Number field and a three (3=Account Conversion/Update Acknowledgement) in the Transaction 
Type field. 
 
c) The receiving Firm conveys to the Firm delivering the accounts the numbers associated with the 
newly-networked shell accounts (this is accomplished outside of Networking). 
 

---

## Page 6

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Mass [[Broker]] to [[Broker]] transfer: Transaction Type 4 6 
 
 
2. The delivering Firm then submits a transfer request to the Fund using Record Type B52 and a Transaction 
Type of 4.  Record Type B52 is used when the delivering Firm requests the Fund to move the [[shares]] out 
of the existing accounts into the shell accounts of the receiving Firm. 
 
a) The delivering Firm’s [[NSCC]] number is placed in the Clearing/Settling Firm field and the receiving 
Firm’s [[NSCC]] number is placed in the Receiving Firm Clearing/Settling Number field. 
 
b) Credit Sub-Account Number (Underlying Credit Customer Account Number) and Debit Sub-
Account Number (Underlying Debit Customer Account Number) must also be provided.  If the 
account is networked and the sub-account numbers are not available, the account numbers 
populated in the Credit Account Number and Debit Account Number fields (Seq. 1) should be 
utilized. 
 
3. [[NSCC]] will place a unique control number in the Control Number field of the B52 record and send it to 
the receiving Firm, the delivering Firm, in addition to the Fund and TPA/ Investment agent if 
provided. 
 
4. Using Record Type F53, the Fund acknowledges the transfer request. The Fund places the delivering 
Firm’s number in the Clearing/Settling Firm Number field, the receiving Firm’s number in the Receiving Firm 
Clearing/Settling field, and a 4 in the Transaction Type field. 
 
5. When [[NSCC]] receives the F53, it sends a copy to the receiving Firm and delivering Firm, in addition to 
the TPA/Investment agent if provided. 
 
6. Generated Reminders (N49) are sent to both the Firms and the Fund.  The F53 and the N49 records 
contain the same [[NSCC]] Control Number as the original B52.  This helps the parties to reference and 
track their transfers. 
 
7. Funds will send F55 Activity records to the Firms indicating the closing balance on each account that 
was converted.  The receiving Firm’s shell accounts should show the transferred [[shares]].  The 
delivering Firm’s accounts should show a zero balance. 
 

---

## Page 7

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Non-ACAT eligible: Transaction Type 8 7 
NON-ACAT ELIGIBLE: TRANSACTION TYPE 8 
Background 
Transaction Type 8 (Non-ACAT eligible transfer) was implemented to the Networking Transfer Detail/Fund 
Acknowledgment (A/B/T52, F53) record to further standardize and expand the use of B52 transfer activity 
between Firms in instances where: 
• One or both Firms are not ACATs eligible, or a Security Issue [[ID]] is not ACATs eligible, and both Firms 
participate in [[NSCC]]’s Networking service. 
Transaction Type 8 should always be initiated by the delivering Firm and only utilized for Firm/Firm transfers.  
Transaction Type 2 (Transfer) should be utilized for Firm/Fund transfers. 
Standards 
The following standards apply to Transaction Type 8: 
• Transaction Type 8 is used when one or both Firms are not ACATs eligible, or a Security Issue [[ID]] is 
not ACATs eligible, and both Firms participate in [[NSCC]]’s Networking service. 
• There should not be a prior ACAT transfer (FUL, PTR, PTD, RCR) that aged to Settle Close.  
• Receiving Firm must establish new BIN (account), if necessary, prior to the delivering Firm submitting 
the B52. The new BIN should be established using the Networking B50 record. 
• The Non-ACAT eligible transfer process begins by the receiving Firm sending the transfer request, 
through the use of the Firm to Firm Non-ACATS Transfer Request Form (see Appendix), in addition to 
any other necessary paperwork, to the delivering Firm.   
• The delivering Firm must initiate the request through the B52. 
• The control number to be used for cost basis and share aging purposes should be the [[NSCC]] 
Networking control number, which is located on the B52 and then confirmed by the Fund on the F53 
record.  
• If the account is networked, and therefore, no underlying account number is available, the Credit/Debit 
Account Numbers should be populated in the Credit Sub-Account Number and Debit Sub-Account 
Number fields. 
 
 
  

---

## Page 8

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Non-ACAT eligible: Transaction Type 8 8 
Processing steps 
Listed below are the guidelines for processing a Non-ACAT eligible (Transaction Type 8) Transfer: 
 
1. If the account is not established on the Fund’s books, the receiving Firm establishes new (shell) 
accounts on the Fund’s books.  If the account is already established, proceed to Step 1(c). 
a) The receiving Firm places its [[NSCC]] number in the Clearing/Settling Firm Number field of 
Record Type B50.  The relaying of the receiving Firm’s [[NSCC]] number and the account matrix 
level for these new accounts is critical to the accurate processing of the conversion. 
b) Funds acknowledge back to the receiving Firm that the accounts were set up properly, using 
Record Type F53 by placing the receiving Firm’s [[NSCC]] number in the Clearing/Settling Firm 
Number field and a three (3=Account Conversion/Update Acknowledgement) in the 
Transaction Type field. 
c) The receiving Firm conveys to the delivering Firm the account number and additional 
information required to initiate the transfer request.   This is accomplished outside of 
networking utilizing the Firm to Firm Non-ACAT Transfer Request Form (see Appendix). 
 
2. The delivering Firm then submits a transfer request to the Fund using Record Type B52, placing an 8 
(8 = Non-ACAT eligible transfer) in the Transaction Type field.   
a) The delivering Firm’s [[NSCC]] number is placed in the Clearing/Settling Firm field and Initiating 
Firm fields, and the receiving Firm’s [[NSCC]] number is placed in the Receiving Firm 
Clearing/Settling Number field. 
b) Credit Sub-Account Number (Underlying Credit Customer Account Number) and Debit Sub-
Account Number (Underlying Debit Customer Account Number) must also be provided.  If the 
account is networked and the sub-account numbers are not available, the account numbers 
populated in the Credit Account Number and Debit Account Number fields (Seq. 1) should be 
utilized. 
3. [[NSCC]] will place a unique control number in the Control Number field of the B52 record and send it to 
the receiving Firm and delivering Firm, in addition to the Fund and TPA/ Investment agent if 
provided. 
4. Using Record Type F53, the Fund acknowledges the transfer request.  The Fund places the delivering 
Firm’s [[NSCC]] number in the Clearing/Settling Firm Number field, the receiving Firm’s [[NSCC]] number in 
the Receiving Firm Clearing/Settling field, and an 8 in the Transaction Type field. 
5. When [[NSCC]] receives the F53, it sends a copy to the receiving Firm and delivering Firm, in addition 
to the TPA/Investment agent if provided. 
 
 

---

## Page 9

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Non-ACAT eligible: Transaction Type 8 9 
 
6. Generated Reminders (N49) are sent to both the Firms and the Fund.  The F53 and the N49 records 
contain the same [[NSCC]] Control Number as the original B52.  This helps the parties to reference and 
track their transfers. 
 
7. Funds will send a F55 Activity record to the Firms indicating the closing balance on the account that 
was transferred.  The receiving Firm’s account should show the transferred [[shares]].  The delivering 
Firm’s account should show a zero balance. 
 

---

## Page 10

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
ACAT Mutual Fund fail cleanup: Transaction Type 9 10 
ACAT MUTUAL FUND FAIL CLEANUP: TRANSACTION 
TYPE 9 
Background 
Transaction Type 9 (ACAT Mutual Fund Fail Cleanup) was implemented to the Networking Transfer 
Detail/Fund Acknowledgment (A/B/T52, F53) record to further standardize and expand the use of B52 transfer 
activity between Firms in instances where: 
• A mutual Fund “fail” occurs between two ACATS participating Firms due to a reject or purge at the 
Fund.  
Transaction Type 9 should always be initiated by the delivering Firm and only utilized for Firm/Firm transfers.  
Transaction Type 2 (Transfer) should be utilized for Firm/Fund transfers. 
Standards 
The following standards apply to Transaction Type 9: 
• Transaction Type 9 is used only when an ACAT transfer (FUL, PTR, PTD, RCR) has aged to Settle 
Close and the Mutual Fund (Settling Location 10 and 50) has also failed.    
• Although banks [[DO]] not follow a similar fail process, Transaction Type 9 should also be used for failed 
Bank ACATs.  
• Receiving Firm must establish new BIN (account), if necessary, prior to the Delivery Firm submitting 
the B52 in order to avoid additional rejects. The new BIN should be established using the Networking 
B50 record. 
• Delivering Firm must initiate request using a B52 and will receive the information needed to complete 
the request by communicating with the receiving Firm. The receiving Firm should send the delivering 
Firm the Firm to Firm Non-ACAT Transfer Request Form (see Appendix) to provide the necessary 
instructions.  
• Delivering Firm will indicate the original ACAT Control # of the failed ACAT on the record, and the 
Fund company will populate and return this number on the F53. 
• If the account is networked, and therefore, no underlying account number is available, the Credit/Debit 
Account Numbers should be populated in the Credit Sub-Account Number and Debit Sub-Account 
Number fields. 
• The control number to be used for cost basis should be the original ACATs control number from the 
failed ACATs transfer (located in the B52 ‘ACATs Control Number’ field).  

---

## Page 11

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
ACAT Mutual Fund fail cleanup: Transaction Type 9 11 
• The control number to be used for share aging purposes should be the [[NSCC]] Networking Control 
number, which is located on the B52 and then confirmed by the Fund on the F53 record. 
Note 
For Firm to Firm ACAT failed items, the delivering Firm generally has already sent cost basis to the receiving Firm, with the 
[[settlement]] of the ACAT.  
 
Processing Steps 
Listed below are the guidelines for processing an ACAT Mutual Fund Fail Cleanup (Transaction Type 9) 
Transfer: 
1. If the account is not established on the Fund’s books, the receiving Firm establishes new (shell) 
accounts on the Fund’s books.  If the account is already established, proceed to Step 1(c). 
 
a) The receiving Firm places its [[NSCC]] number in the Clearing/Settling Firm Number field of 
Record Type B50. The relaying of the receiving Firm’s [[NSCC]] number and the account matrix 
level for these new accounts is critical to the accurate processing of the conversion. 
b) Funds acknowledge back to the receiving Firm that the accounts were set up properly, using 
Record Type F53 by placing the receiving Firm’s [[NSCC]] number in the Clearing/Settling Firm 
Number field and a three (3=Account Conversion/Update Acknowledgement) in the 
Transaction Type field. 
c) The receiving Firm conveys to the delivering Firm the account number and additional 
information required to initiate the transfer request.  This is accomplished outside of 
networking. 
 
2. The delivering Firm then submits a transfer request to the Fund using Record Type B52, placing a 9     
(ACAT Mutual Fund Fail Cleanup) in the Transaction Type field.   
a) The delivering Firm’s number is placed in the Clearing/Settling Firm field and Initiating Firm 
fields, and the receiving Firm’s number is placed in the Receiving Firm Clearing/Settling 
Number field. 
 
b) Credit Sub-Account Number (Underlying Credit Customer Account Number) and Debit Sub-
Account Number (Underlying Debit Customer Account Number) must also be provided.  If the 
account is networked and the sub-account numbers are not available, the account numbers 
populated in the Credit Account Number and Debit Account Number fields (Seq. 1) should be 
utilized. 
 
c) The original 14-byte ACATS control number from the failed ACAT transfer must be provided in 
the ACATS Control Number field. 

---

## Page 12

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
ACAT Mutual Fund fail cleanup: Transaction Type 9 12 
 
3. [[NSCC]] will place a unique control number in the Control Number field of the B52 record and send it to 
the receiving Firm and delivering Firm, in addition to the Fund and TPA/ Investment agent if 
provided. 
 
4. Using Record Type F53, the Fund acknowledges the transfer request.  The Fund places the delivering 
Firm’s [[NSCC]] number in the Clearing/Settling Firm Number field, the receiving Firm’s [[NSCC]] number in 
the Receiving Firm Clearing/Settling field, the ACATS control number in the ACATS Control Number 
field, and a 9 in the Transaction Type field. 
5. When [[NSCC]] receives the F53, it sends a copy to the receiving Firm and delivering Firm, in addition 
to the TPA/Investment agent if provided. 
 
6. Generated Reminders (N49) are sent to both the Firms and the Fund. The F53 and the N49 records 
contain the same [[NSCC]] Control Number as the original B52.  This helps the parties to reference and 
track their transfers. 
 
7. Funds will send a F55 Activity record to the Firms indicating the closing balance on the account that 
was transferred.  The receiving Firm’s account should show the transferred [[shares]].  The delivering 
Firm’s account should show a zero balance. 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 13

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Networking transfer best practices: workflows for B52 Transaction Types 4, 8 and 9 13 
NETWORKING TRANSFER BEST PRACTICES: WORKFLOWS FOR B52 
TRANSACTION TYPES 4, 8 AND 9 
Mass [[Broker]] to [[Broker]] (Transaction Type 4) – Workflow 
Mass [[Broker]] to [[Broker]] (Transaction Type 4) Workflow  
Fund Company Firm B
Delivers
Firm A
Receives
Firms A 
and B
Prior to Day 1 Day 1 Day 2
Notes:
*New Account Established – Omnibus accounts already established, others need to send B50 or manually open account
**Cost basis and share aging sent following the movement of the [[shares]]
New Account Established* and 
transfer details arranged with 
delivering firm
Send B52, 
Transaction Type 
4
Conversion 
Cleanup Occurs*
Receive B52 Move [[shares]] F53 Sent
Receive F53 
Client Accounts 
are credited and 
debited by 
respective firms
 
 
 

---

## Page 14

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Networking transfer best practices: workflows for B52 Transaction Types 4, 8 and 9 14 
Non ACAT Transfer (Transaction Type 8) Workflow 
Non-ACAT Transfer Workflow -- One or Both Firms are not ACAT participants and transfer processed through B52 
Transaction Type 8
Client Fund Company Firm B
Delivers
Firm A
Receives
Firms A 
and B
Prior to Transfer Day 1 Day 2
Paperwork sent 
to Firm B to 
request 
Transfer
Send B52, 
Transaction Type 
8
Receive F53 Bookkeeping 
entries made**
Notes:
*New Account Established – Omnibus accounts already established, others need to send 
B50 or manually open account
**Cost Basis and Share aging records sent following the movement of [[shares]] (referencing 
control number on the F53) 
Receive 
paperwork
Receive B52 [[shares]] Move F53 Sent
Client sees share 
movement
New Account 
Established*
 

---

## Page 15

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Networking transfer best practices: workflows for B52 Transaction Types 4, 8 and 9 15 
ACAT MF Fail Cleanup (ACAT Reconciliation) Transaction Type 9 Workflow 
ACAT Reconciliation Workflow - Firm A Initiates ACAT, Record is Fund/SERV Rejected or Purged, [[shares]] moved through B52 Transaction Type 9
Firm A 
Receivers
Firm B 
DeliversFund Company Firms A and B
Prior to Day 1 Day 1 Day 2
Receipt of F53
B52 received and 
[[shares]] move 
automatically
MFC Generated
Submit B52, 
Transaction Type 
9
F53 Confirmation 
Generated
MFC Accepted
Both firms clean 
up related fails**
Notes:
*Cost Basis sent between firms with the [[settlement]] of the ACAT
**Share aging files sent following the share movement, as applicable (referencing the 
control number on the F53)
Bank ACATs – Due to the unique process that occurs with banks (no fails are created), 
the ‘clean-up’ piece will differ from what is referenced above.  
Communication 
between firms 
FundSERV 
request rejects or 
purges (approx. 2 
days prior to ACAT 
[[settlement]])
[[settlement]] of 
ACAT*
Credit Client 
Account, Set up 
Fail to Receive 
Debit Client 
Account, Set up 
Fail to Deliver
 
 
 

---

## Page 16

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Appendix: Firm to Firm Non-ACAT Transfer Request Form — Templates 16 
APPENDIX: FIRM TO FIRM NON-ACAT TRANSFER 
REQUEST FORM — TEMPLATES 
Firm to Firm Non-ACAT Transfer Request Form 
Description of Firm to Firm Letter 
The purpose of the Firm to Firm Mutual Fund Letter is to allow communication of the Receiving Firm’s Fund 
Information to the Delivering Firm on a Non-ACAT transfer request.  This information is then used by the 
Delivering Firm to instruct the Fund Company to request a Networking B52 (Transaction Type 8 or 9) or 
manual transfer. 
Note 
The best practice is to use the B52 to automate the request whenever possible 
Best Practices 
• Fund Name: Description (name) of the [[Asset]]/fund product. 
• Security Issue [[ID]] ([[CUSIP]]): Committee on Uniform Security Identification Procedure, a unique 
identifier for the security. 
• Quantity: If the customer is requesting a full transfer, “ALL” can be placed in this field.  If the client is 
requesting a partial transfer, enter the share quantity that is being requested.   
• [[NSCC]] [[ID]]: By populating the [[NSCC]] [[ID]], you are authorizing the delivering Firm to transfer via B52. 
Enter the [[NSCC]] [[ID]] of the Firm receiving the Fund on behalf of the Firm. This Firm can be the same 
firm as the receiving Firm or a different Firm. 
• Underlying Receiving Account #: The client’s account number at the receiving Firm. 
• When submitting a B52 to the Fund company: 
o The delivering Firm should enter this information in the Credit Sub-Account Number 
(Sequence #4, Position 46-65) on the F53. 
 
• When submitting manual instructions to the Fund company 
o The delivering Firm should provide the Underlying Receiving Account #. 
 
 

---

## Page 17

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Appendix: Firm to Firm Non-ACAT Transfer Request Form — Templates 17 
• BIN & Fund Account #: Both the BIN and the Fund Account fields should be completed in order to 
clarify the request.  If only one of these numbers is available, the number should be placed in the 
appropriate column. 
• When submitting a B52 to the Fund company: 
o The delivering Firm can use either the BIN or Fund Account Number: 
• If the BIN is used, the Credit Account Indicator (B52/F53, Sequence #1, position 
56) should be populated with a 1. 
• If the Fund Account Number is used, the Credit Account Indicator (B52/F53, 
Sequence #1, position 56) should be populated with a 2. 
 
o The BIN or Fund Account Number should be populated on the B52 in the Credit Account 
Number field. 
 
• When submitting a B52 to the Fund company:  
o The delivering Firm should provide the BIN or Fund Account Number. 

---

## Page 18

B52 Networking Transfers: Transaction Types 4, 8, and 9 - Best Practices 
Appendix: Firm to Firm Non-ACAT Transfer Request Form — Templates 18 
Firm to Firm Non-ACAT Transfer Request Form Sample 
Firm Letterhead 
 
[Department’s Name]  
[Street Address]  
[City, State, Zip Code] 
 
[Date] 
Re: Deliver Non-ACATS Transfer 
 
Name of Client: 
Delivering Firm Account #: 
 
 
[Enter Firm-specific verbiage requesting transfer] 
Fund Name [[CUSIP]] Quantity 
[[NSCC]] 
[[ID]] 
Underlying 
Receiving 
Account # BIN 
Fund 
Account # 
            
 
[Enter Firm-specific verbiage authorizing transfer]  
 
Thank you for your prompt attention to this matter. 
[Enter Firm specific contact information] 
 
Sincerely, 
[Sender’s Name] 
[Sender’s Department]  
[Sender’s Telephone #] 
[Sender’s Fax#] 

---

## Page 19

 
 
 
 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
corelearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 