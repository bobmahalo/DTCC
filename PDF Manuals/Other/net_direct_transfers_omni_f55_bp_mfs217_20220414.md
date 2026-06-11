---
title: "Direct Transfer (Omni Reconciliation F55) Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_direct_transfers_omni_f55_bp_mfs217_20220414.pdf"
pages: 41
size: "2957.0 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Direct Transfer (Omni Reconciliation F55) Best Practices

**Original File:** [net_direct_transfers_omni_f55_bp_mfs217_20220414.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_direct_transfers_omni_f55_bp_mfs217_20220414.pdf)  
**Category:** Other  
**Total Pages:** 41  
**File Size:** 2957.0 KB  

---

## Page 1

 
 
 
 
NETWORKING 
DIRECT TRANSFER (OMNI RECONCILIATION F55) BEST PRACTICES 
APRIL 14, 2022 
 
 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
By accessing this document, you acknowledge, accept and agree to the foregoing [[obligations]] and restrictions. 
 
 
Doc Date: April 14, 2022 
Publication Code: MFS217 
Service: Networking 
Title: Direct Transfer (Omni Reconciliation F55) Best Practices 
 
 
  

---

## Page 3

 
 
CHANGE HISTORY 
Date Description 
04/14/2022 Learning upgrade caused some link(s) to break. Link has been corrected. 
07/21/2020 Corrected broken links 
Effective Date: October 17, 
2011 
Please see Important Notice a7241, p&S 6811  
Revised August 8, 2011 (First Publication July 8, 2011) 
 
 

---

## Page 4

 
 
TABLE OF CONTENTS 
Best Practices Direct Transfers: Populating F55 Records .............................................................................. 6 
Background and Objectives................................................................................................................................. 6 
F55 Record: Using Original Control Number and Original Control Number Indicator  ................................. 8 
Use of "Original Control Number" and "Original Control Number Indicator" in the Networking Activity 
Reporting (F55) Record ...................................................................................................................................... 8 
Population of Account Identification Fields in the Networking Activity Reporting (F55) Record  ............... 9 
Workflow A: Transfer from Omnibus Account ................................................................................................ 10 
From Omnibus Account to Omnibus Account ..................................................................................................10 
Omnibus Account to Networked Account (Level 3,4) .......................................................................................11 
Omnibus Account to Trust Networked (Level 0) Account .................................................................................12 
Omnibus Account to Trust Networked (Level 0) with TPA ...............................................................................13 
Omnibus Account to Direct (Level 0) Account ..................................................................................................14 
Example:..........................................................................................................................................................15 
Workflow B: Transfer from Networked Account ............................................................................................. 16 
Networked Account (Level 3,4) to Omnibus Account .......................................................................................16 
Networked Account (Level 3,4) to Networked Account (Level 3,4) ..................................................................17 
Networked Account (Level 3,4) to Trust Networked (Level 0) Account ............................................................18 
Networked Account (Level 3,4) to Trust Networked (Level 0) with TPA ..........................................................19 
Networked Account (Level 3,4) to Direct (Level 0) Account .............................................................................20 
Workflow C: Transfer from Trust Networked Account ................................................................................... 21 
Trust Networked Account (Level 0) to Omnibus Account .................................................................................21 
Trust Networked Account (Level 0) to Networked Account (Level 3,4) ............................................................22 
Trust Networked Account (Level 0) to Trust Networked (Level 0) Account ......................................................23 
Trust Networked Account (Level 0) to Trust Networked (Level 0) with TPA ....................................................23 
Trust Networked Account (Level 0) to Direct (Level 0) Account .......................................................................25 
Workflow D: Transfer from Trust Networked Account with TPA .................................................................. 26 
Trust Networked Account (Level 0) with TPA to Omnibus Account .................................................................26 
Trust Networked Account (Level 0) with TPA to Networked Account (Level 3,4)  ............................................27 
Trust Networked Account (Level 0) with TPA to Trust Networked (Level 0) Account  ......................................28 

---

## Page 5

 
 
Trust Networked Account (Level 0) with TPA to Trust Networked (Level 0) with TPA  .....................................29 
Trust Networked Account (Level 0) with TPA to Direct (Level 0) Account .......................................................30 
Workflow E: A Transfer from Direct Account .................................................................................................. 31 
From Direct Account (Level 0) to Omnibus Account ........................................................................................31 
Direct Account (Level 0) to Networked Account (Level 3,4) .............................................................................32 
Direct Account (Level 0) to Trust Networked (Level 0) Account .......................................................................33 
Direct Account (Level 0) to Trust Networked (Level 0) with TPA .....................................................................34 
Direct Account (Level 0) to Direct (Level 0) Account ........................................................................................35 
MF Agent - Direct Transfer Processing ........................................................................................................... 36 
ACAT Fails .......................................................................................................................................................... 37 
Direct Transfer .................................................................................................................................................... 38 
Cost Basis Information ...................................................................................................................................... 40 
 

---

## Page 6

Direct Transfer (Omni Reconciliation F55) Best Practices 
Best Practices Direct Transfers: Populating F55 Records 6 
BEST PRACTICES DIRECT TRANSFERS: POPULATING 
F55 RECORDS 
The proposed guidelines encompassed in these articles provide best practices for the use of various fields in 
the [[NSCC]] Networking Activity Reporting (F55) records when a direct transfer occurs at the Fund.  
Background and Objectives 
[[NSCC]], together with the Investment Company Institute's [[Broker]]/Dealer Advisory Committe e, endeavored to 
develop a standard and automated process to facilitate the transfer of account level detail required to 
effectively reconcile direct activity that takes place on Firms' accounts at the Fund. Historically, Firms and 
Funds attempted to reconcile from existing processes; these processes included, but are not limited to, [[NSCC]] 
Networking files, files from recordkeeping systems, ad-hoc reports, manual exchange of information, and 
manual validation from mutual fund portals. 
[[NSCC]] Networking Activity Reporting (F55) records are currently leveraged to communicate activities which 
have taken place on Firms' accounts at the Funds. To better support the [[investor]] and reduce reconciliation 
risk, enhancements to the existing Networking Activity Reporting records were implemented to provide Firms 
with information to effectively reconcile their client positions. The enhancements pertaining to direct transfers 
included the addition of the following fields to provide Firms with additional transparency necessary to reconcile 
their sub-account positions: 
• Membership Identifier - [[NSCC]] membership type. 
• Opposing Membership Identifier 
• Omnibus Account Indicator - identifies whether the account is set up as an Omnibus account at the 
Fund. 
• Opposing Underlying Customer Account Number - customer account number (sub-account) at the 
contra-side party. 
 
The "Opposing Underlying Customer Account Number" field allows Funds to indicate opposing Firms' sub-
account, when available. 
• Opposing Network Control Indicator - matrix level of the account at the contra-side party. 
 
The " Opposing Network Control Indicator" field assists Firms in identifying whether additional information from 
the opposing Firm is required; i.e., share-lot information for cost basis and tax reporting indicates the matrix 
level of the responsible party for communicating account information. Prior to the addition of this field, the F55 
record only included a field (Network Control Indicator) to identify the network control indicat or of the account 
from one of parties involved. 
• Opposing Clearing/Settling  Firm Number - [[NSCC]] number of the contra-side party. 
 

---

## Page 7

Direct Transfer (Omni Reconciliation F55) Best Practices 
Best Practices Direct Transfers: Populating F55 Records 7 
The "Opposing Clearing/Settling Firm Number " field allows Firms to identify the applicable party to contact 
should additional information be required. Prior to the addition of this field, the F55 record only included a field 
(Clearing/Settling Firm Number) to identify one of the contra-side parties involved. 
• Social Code - two-digit number indicating the type of account. 
 

---

## Page 8

Direct Transfer (Omni Reconciliation F55) Best Practices 
F55 Record: Using Original Control Number and Original Control Number Indicator 8 
F55 RECORD: USING ORIGINAL CONTROL NUMBER 
AND ORIGINAL CONTROL NUMBER INDICATOR 
Use of "Original Control Number" and "Original Control Number 
Indicator" in the Networking Activity Reporting (F55) Record 
When a direct transfer is requested by a Firm for a rejected Networking or ACATS-Fund/SERV® transfer, the 
best practice is for the Firm to provide the control number associated with the rejected transfer on the manual 
request submitted to the fund. The Fund should populate the "Original Control Num ber" and use the applicable 
"Original Control Number Indicator" value ("1" for Fund/SERV® Control Number or "2" for Networking Control 
Number). 
If a control number is not provided by the requesting Firm, or in the case of a Fund initiated direct transfer, the 
Fund should populate the "Original Control Number" with a Fund originated control number and the "Original 
Control Number Indicator" should be populated with a value of '3' for Manual Reference Number. 
Note:  
When a direct transfer occurs, the Share Aging Record (B/F75) should also be utilized by the Fund leveraging the same 
control number and indicator values populated in the F55 Networking Activity Reporting records and transmitted within 3 
business days of posting the transfer. Please see Share Aging Best Practices guide for details on the use of the Share 
Aging Record in conjunction with a direct transfer.  This can be found on the Learning Center in Networking section under 
Resources tab https://dtcclearning.com/products-and-services/mutual-fund-services/networking.html#resources  
 
 

---

## Page 9

Direct Transfer (Omni Reconciliation F55) Best Practices 
Population of Account Identification Fields in the Networking Activity Reporting (F55) Record 9 
POPULATION OF ACCOUNT IDENTIFICATION FIELDS IN 
THE NETWORKING ACTIVITY REPORTING (F55) 
RECORD 
When a direct transfer takes place at the Fund, a Networking Activity Reporting (F55) record is sent by the 
Fund to the applicable Firm(s). As a best practice to support Firms' needs for additional information required to 
reconcile direct transfer activity, Funds should indicate the underlying account details, when available. The 
following workflows depict best practices when populating the F55 records for th e following fields: 
• Firm/Fund Identification Number 
• Opposing Fund Account Number 
• Underlying Customer Account Number 
• Opposing Underlying Customer Account Number 
• Network Control Indicator 
• Opposing Network Control Indicator 
• Clearing/Settling Firm Number 
• Opposing Clearing/Settling Firm Number 
• Membership Identifier 
• Opposing Membership Identifier 
• TPA/Investment Agent Number 
Note:  
When the TPA/Investment Agent Number field is populated, [[NSCC]] automatically transmits a copy of the record to the 
[[NSCC]] [[participant]] identified in this field. 
 
 

---

## Page 10

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow A: Transfer from Omnibus Account 10 
WORKFLOW A: TRANSFER FROM OMNIBUS ACCOUNT 
Depicts direct transfer scenarios from an Omnibus account to an Omnibus, Networked, Trust Networked, Trust 
Networked with a TPA, or Direct account. In each scenario, the applicable values are populated in the "From" 
Firm and "To" Firm fields. 
From Omnibus Account to Omnibus Account 
 
 
 


---

## Page 11

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow A: Transfer from Omnibus Account 11 
Omnibus Account to Networked Account (Level 3,4) 
 
 


---

## Page 12

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow A: Transfer from Omnibus Account 12 
Omnibus Account to Trust Networked (Level 0) Account 
 
 


---

## Page 13

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow A: Transfer from Omnibus Account 13 
Omnibus Account to Trust Networked (Level 0) with TPA 
 
 


---

## Page 14

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow A: Transfer from Omnibus Account 14 
Omnibus Account to Direct (Level 0) Account 
 
 
Note: 
• If the opposing party to the transaction has a valid [[NSCC]] [[participant]] number, the value for the Firm or 
Fund (in the case of a direct level 0 account) should be populated in the "Opposing Clearing/Settling Firm 
Number" field; if not, this field should be left blank. 
• When a Fund transmits a F55 record to both the "From" and "To" Firm, which should be the case in all 
instances except when a direct level 0 account is involved, the value for a particular field at one Firm 
would be the same as the "opposing" cross reference field at the contra-side Firm; i.e., "Underlying 
Customer Account Number" and "Opposing Underlying Customer Account Number" (the example below 
depicts this situation). This also holds true for the network control indicator and clearing/settling Firm 
number fields. Providing each Firm with the opposing Firm's information promotes the transparency 
needed to effectively reconcile sub-account positions. 
 
 


---

## Page 15

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow A: Transfer from Omnibus Account 15 
Example: 
In the case of an Omnibus to Omnibus transfer (see Workflow A above), the value for the "Underlying 
Customer Account Number” transmitted to the "From" Firm is the same as "Opposing Underlying Customer 
Account Number" transmitted to the "To" Firm, and vice versa.  
 
 
  
 


---

## Page 16

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow B: Transfer from Networked Account 16 
WORKFLOW B: TRANSFER FROM NETWORKED 
ACCOUNT 
Depicts direct transfer scenarios from a Networked account to an Omnibus, Networked, Trust Networked, Trust 
Networked with a TPA, or Direct account.  In each scenario, the applicable values are populated in the "From" 
Firm and "To" Firm fields.  
Networked Account (Level 3,4) to Omnibus Account 
 


---

## Page 17

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow B: Transfer from Networked Account 17 
Networked Account (Level 3,4) to Networked Account (Level 3,4) 
 


---

## Page 18

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow B: Transfer from Networked Account 18 
Networked Account (Level 3,4) to Trust Networked (Level 0) Account 
 


---

## Page 19

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow B: Transfer from Networked Account 19 
Networked Account (Level 3,4) to Trust Networked (Level 0) with TPA 
 


---

## Page 20

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow B: Transfer from Networked Account 20 
Networked Account (Level 3,4) to Direct (Level 0) Account 
 
 


---

## Page 21

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow C: Transfer from Trust Networked Account 21 
WORKFLOW C: TRANSFER FROM TRUST NETWORKED 
ACCOUNT 
Depicts direct transfer scenarios from a Trust Networked account to an Omnibus, Networked, Trust Networked, 
Trust Networked with a TPA, or Direct account. In each scenario, the applicable values are populated in the 
"From" Firm and "To" Firm Fields.  
Trust Networked Account (Level 0) to Omnibus Account 
 


---

## Page 22

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow C: Transfer from Trust Networked Account 22 
Trust Networked Account (Level 0) to Networked Account (Level 3,4) 
 


---

## Page 23

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow C: Transfer from Trust Networked Account 23 
Trust Networked Account (Level 0) to Trust Networked (Level 0) 
Account 
 
Trust Networked Account (Level 0) to Trust Networked (Level 0) with 
TPA 


---

## Page 24

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow C: Transfer from Trust Networked Account 24 
 


---

## Page 25

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow C: Transfer from Trust Networked Account 25 
Trust Networked Account (Level 0) to Direct (Level 0) Account 
 
 
 


---

## Page 26

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow D: Transfer from Trust Networked Account with TPA 26 
WORKFLOW D: TRANSFER FROM TRUST NETWORKED 
ACCOUNT WITH TPA 
Depicts direct transfer scenarios from a Trust Networked with a TPA to an Omnibus, Networked, Trust 
Networked, Trust Networked with a TPA, or Direct account. In each scenario, the applicable values are 
populated in the "From" Firm and "To" Firm fields. 
Trust Networked Account (Level 0) with TPA to Omnibus Account 
 


---

## Page 27

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow D: Transfer from Trust Networked Account with TPA 27 
Trust Networked Account (Level 0) with TPA to Networked Account 
(Level 3,4) 
 


---

## Page 28

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow D: Transfer from Trust Networked Account with TPA 28 
Trust Networked Account (Level 0) with TPA to Trust Networked 
(Level 0) Account 
 


---

## Page 29

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow D: Transfer from Trust Networked Account with TPA 29 
Trust Networked Account (Level 0) with TPA to Trust Networked 
(Level 0) with TPA 
 


---

## Page 30

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow D: Transfer from Trust Networked Account with TPA 30 
Trust Networked Account (Level 0) with TPA to Direct (Level 0) 
Account 
 


---

## Page 31

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow E: A Transfer from Direct Account 31 
WORKFLOW E: A TRANSFER FROM DIRECT ACCOUNT 
Depicts direct transfer scenarios from a Direct account to an Omnibus, Networked, Trust Networked, Trust 
Networked with a TPA, or Direct account.  In each scenario, the applicable values are populated in  the "From" 
Firm and "To" Firm fields. 
From Direct Account (Level 0) to Omnibus Account 
 


---

## Page 32

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow E: A Transfer from Direct Account 32 
Direct Account (Level 0) to Networked Account (Level 3,4) 
 


---

## Page 33

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow E: A Transfer from Direct Account 33 
Direct Account (Level 0) to Trust Networked (Level 0) Account 
 


---

## Page 34

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow E: A Transfer from Direct Account 34 
Direct Account (Level 0) to Trust Networked (Level 0) with TPA 
 


---

## Page 35

Direct Transfer (Omni Reconciliation F55) Best Practices 
Workflow E: A Transfer from Direct Account 35 
Direct Account (Level 0) to Direct (Level 0) Account 
 
 


---

## Page 36

Direct Transfer (Omni Reconciliation F55) Best Practices 
MF Agent - Direct Transfer Processing 36 
MF AGENT - DIRECT TRANSFER PROCESSING 
MF Agent processing occurs when a [[participant]] designates another [[NSCC]] [[participant]] to serve as their  
ACATS-Fund/SERV® Agent. In this relationship, the firm designated to interface with ACATS-Fund/SERV® is 
known as the MF Agent. When an MF Agent initiates an ACATS-Fund/SERV® transfer which subsequently 
rejects, the MF Agent may instruct the fund to initiate a manual transfer. When a manu al transfer (via the F55) 
is initiated through the fund, the MF Agent is expected to provide the [[NSCC]] number of the underlying firm it is 
acting as MF Agent for to identify the party holding the cost basis information on the account. In order to 
identify the underlying firm on these transactions, the "Originating / Underlying Firm Number" and the 
"Opposing Originating / Underlying Firm Indicator' fields were added to the F55 Activity Reporting record . 
In addition to the aforementioned scenario where an MF Agent initiates a transfer (including ACATS-
Fund/SERV® transfers) the receiving firm may also use an MF Agent. 

---

## Page 37

Direct Transfer (Omni Reconciliation F55) Best Practices 
ACAT Fails 37 
ACAT FAILS 
 
 
 
 
 
 
When a transfer is submitted by an MF Agent via ACATS-Fund/SERV® and the transaction fails (rejects), the 
fund to which the transaction was submitted may process a direct transfer via the F55 Activity Record to 
complete the transaction. When a direct transfer is initiated, the fund will transmit F55's to both the "Delivering" 
and the "Receiving" firms. When an MF Agent is involved the F55 will be transmitted to the MF Agent who 
submitted the trade, as well as the receiving firm or their MF Agent. 
 


---

## Page 38

Direct Transfer (Omni Reconciliation F55) Best Practices 
Direct Transfer 38 
DIRECT TRANSFER 
 
 
 
 
 
On the F55 record the Originating / Underlying Firm Number and Opposing Originating / Underlying Firm 
Number will be populated from the perspective of the party receiving the F55; when the firm (Firm A) receives 
the F55 transmission, the Opposing Firm would be the counterparty (Firm B), and vice versa. The MF Agent's 
[[NSCC]] number is populated in the Clearing I Settling Firm Number field and the Opposing Clearing I 
Settling Firm Number field in the same manner (from the recipient's perspective). 
In the Direct Transfer graphical depiction above, which assumes an MF Agent was utilized on the delivering 
and receiving end of the transaction, the Firm Number fields on the F55 record would be populated as follows:  
 
 


---

## Page 39

Direct Transfer (Omni Reconciliation F55) Best Practices 
Direct Transfer 39 
F55 Field Name Delivering Firm  
(Sent to Firm A) 
Receiving Firm  
(Sent to Firm B) 
Originating / Underlying Firm Number * 1537 2920 
Clearing Settling Firm Number 7507 5348 
Opposing Clearing Settling Firm Number 5348 7507 
Opposing Originating / Underlying Firm Number * 2920 1537 
 
* fields in grey are populated with the MF Agent (from each recipient’s perspective)  

---

## Page 40

Direct Transfer (Omni Reconciliation F55) Best Practices 
Cost Basis Information 40 
COST BASIS INFORMATION 
As mentioned earlier, the cost basis information for the shareholder of the account being transferred would be 
held by the underlying delivering firm. 
When a direct transfer occurs, the Share Aging Record (B/F75) should also be utilized by the Fund leveraging 
the same control number and indicator values populated in the F55 Networking Activity Reporting records and 
transmitted within 3 business days of posting the transfer. Please see the Share Aging Best Practices  guide for 
details on the use of the Share Aging Record in conjunction with a direct transfer.  
 
 

---

## Page 41

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 