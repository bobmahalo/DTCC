---
title: "Chapter 1: Commission and Fee Settlement User Guide / Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs299_dpaxis_comm-fee_sett_ug-bp_20230726.pdf"
pages: 19
size: "356.2 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# Chapter 1: Commission and Fee Settlement User Guide / Best Practices

**Original File:** [mfs299_dpaxis_comm-fee_sett_ug-bp_20230726.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs299_dpaxis_comm-fee_sett_ug-bp_20230726.pdf)  
**Category:** Rules  
**Total Pages:** 19  
**File Size:** 356.2 KB  

---

## Page 1

 
 
[[DTCC]] Payment aXis®  
CHAPTER 1: COMMISSION AND FEE [[settlement]] 
USER GUIDE/BEST PRACTICES  
JULY 26, 2023 

---

## Page 2

REVISION HISTORY 
Date Revisions 
July 26, 2023  Content reviewed and refreshed due to rebranding.  Link to Payment aXis 
schedules changed. 
July 15, 2022 Corrected links that broke due to Learning upgrade.  
Effective April 19, 2021 Removed Global Update chapter.  This product was decommissioned, effective 
April 19, 2021. 
April 1, 2020 Guide was refreshed due to rebranding; links repointed to Learning. 
March 25, 2020 Updated Section 4 DoL [[Fiduciary]] Rule – updated verbiage regarding rule’s 
applicability date and references to the rule. 
May 15, 2017 Updated Section 4 DoL [[Fiduciary]] Rule – updated rule’s applicability date. 
February 5, 2017 Added Section 4 – DoL [[Fiduciary]] Rule. 
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
1. [[DTCC]] Payment aXis® System Overview ........................................................................................................ 5 
Background ......................................................................................................................................................... 5 
Benefits ............................................................................................................................................................... 5 
2. Processing ........................................................................................................................................................ 6 
Transmission Schedule ...................................................................................................................................... 6 
Input Requirements............................................................................................................................................. 6 
Output Requirements .......................................................................................................................................... 8 
Rejected Records .............................................................................................................................................. 8 
Acknowledgement Record ................................................................................................................................ 8 
Accepted Records ............................................................................................................................................. 8 
[[DTCC]] Payment aXis® [[settlement]] File .............................................................................................................. 9 
Processing Overview ........................................................................................................................................10 
Input from Delivering Funds/Firms ..................................................................................................................10 
Output from [[NSCC]] ..........................................................................................................................................10 
[[settlement]] .......................................................................................................................................................10 
Corrections ......................................................................................................................................................10 
3. Processing Commission Payments Between Brokers............................................................................... 11 
Background .......................................................................................................................................................11 
Benefits .............................................................................................................................................................11 
[[DTCC]] Payment aXis® Procedures ...................................................................................................................12 
Requirements ....................................................................................................................................................12 
Record Layouts .................................................................................................................................................12 
4. DoL [[Fiduciary]] Rule–Enhancements and Best Practices ........................................................................... 13 
Background .......................................................................................................................................................13 
DoL Enhancements and Best Practices ...........................................................................................................13 
Level-Fee Based Compensation Fees ............................................................................................................13 
Client-Created Security Issue [[ID]] .....................................................................................................................14 
Return Payment functionality ..........................................................................................................................14 
Additional Fields/Values ..................................................................................................................................17 

---

## Page 4

 
 
5. Adding the Service ......................................................................................................................................... 18 
Existing [[NSCC]] Members ..................................................................................................................................18 
Prospective Members .......................................................................................................................................18 
 

---

## Page 5

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
1. [[DTCC]] Payment aXis® System Overview 5 
1. [[DTCC]] PAYMENT AXIS® SYSTEM OVERVIEW 
Background 
In 1992, [[NSCC]], in concert with the Investment Company Institute [[Broker]] Dealer Advisory Committee, 
developed the Mutual Fund Commission [[settlement]] Service. In 2012, the service was renamed to [[DTCC]] 
Payment aXis® (Important Notices a7464 and a7512). 
Initially, the service provided an automated mechanism allowing a Fund to transmit commission records and 
fee payments to specific Firms for their accounts via the same [[NSCC]] communications network they use for 
Fund/SERV and Networking. In 2005, the service was modified to allow a [[Broker]] dealer to transmit commission 
and various fee payments to other [[Broker]] dealers (see Section 3 - Processing Commission Payments Between 
Brokers). Transactions are settled the next available [[settlement]] date after they are accepted by N SCC. 
The automated payment system was further enhanced in 2013 to facilitate the payment of Omnibus record 
keeping fees. In 2014 [[NSCC]] introduced support for additional fees for [[Broker]] controlled and retirement plan 
accounts (please refer to “Invoicing and Fee [[settlement]] User Guide”). 
In 2017 [[DTCC]] Payment aXis
® was enhanced to allow firms to return payments to the original payment 
deliverer (Important Notice a8286) as a result of the DoL [[Fiduciary]] Rule implementation (please refer to 
Section 4–DoL [[Fiduciary]] Rule: Enhancements and Best Practices). 
The “[[DTCC]] Payment aXis®” guide consists of the following chapters: 
• Chapter I–Commission and Fee [[settlement]] User Guide 
• Chapter II–Invoicing and Fee [[settlement]] User Guide 
 
This guide (Chapter 1) is intended for clients interested in utilizing the “Commission and Fee [[settlement]]” 1. For 
information regarding “Invoicing and Fee [[settlement]]” functionality, please refer to the “[[DTCC]] Payment aXis®–
Invoicing and Fee [[settlement]] User Guide”. 
Benefits 
An automated commission and fee [[settlement]] system reduces the manual or individual automated procedures 
that may exist among Firms and Funds. The automation of this process reduces reliance on clerical personnel 
at Firms, Funds, and Fund distributors and expedites the payment [[settlement]] process. 
Previously Mutual Fund participants used manual and labor-intensive methods to distribute commission and 
fee payments and update each other’s records. 
The use of [[DTCC]] Payment aXis®: 
• Automates and standardizes commission and various fee payments 
• Simplifies the reconciliation of records between Funds and brokers 
• Reduces clerical costs. Eliminates the need to send or receive paper, diskettes, and tapes containing 
commission run information 
• Uses existing [[NSCC]] communications links 
• Consolidates money [[settlement]] with all other [[NSCC]] service transactions 
 
1 This guide should be used in conjunction with the [[DTCC]] Payment aXis Record Layouts located on Learning Center  https://dtcclearning.com/products-and-
services/mutual-fund-services/[[DTCC]]-payment-axis.html 

---

## Page 6

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
2. Processing 6 
2. PROCESSING 
Transmission Schedule 
Clients transmit commission and fee [[settlement]] transactions to [[NSCC]] using established DataTrak SYS -[[ID]] 
numbers. [[NSCC]] must receive these files no later than the prescribed file input cutoff time as specified in the 
transmission schedule. Files received later than the file input cutoff time will be held and processed for the next 
day’s cycle. The [[DTCC]] Payment aXis® service defines business days as Monday through Saturday, unless 
otherwise announced by [[NSCC]]. Please refer to [[DTCC]] Payment aXis® Transmission Schedule available in the 
Learning Center under the Schedules at https://dtcclearning.com/documents/mutual-fund-services-1/[[DTCC]]-
payment-axis/schedules1-5/1808-[[DTCC]]-payment-axis-time-schedule/file.html  
[[NSCC]] employs a multi-batch processing capability in addition to single batch facilities. Due to volume 
constraints, transmission time frames should be limited to not greater than 2 hours per file. Clients are advised 
to review their current mode of communications and upgrade accordingly. 
 
Input Requirements 
Files in their entirety must be received by the cutoff time as specified in the transmission schedule.  
A typical input file consists of a Security Header record 30, Detail record(s) 31, a Security Trailer record 32 and 
a Grand Total Trailer record 33 that summarizes the Deliverer’s inputs for a Specific Receiver. 
For the purposes of this guide, the following definitions will apply to the terms “Deliverer” and “Receiver”:  
• Deliverer – Submitter of the [[DTCC]] Payment aXis
® files/records intended for a specific Receiver (set of 
Receivers) 
• Receiver – Party identified by the Deliverer as the receiver of their transmitted files/records.  
   
For example, Fund A (Deliverer) may send the following set of records to [[NSCC]] intended for Firm B 
(Receiver) 
Security Issue [[ID]] 123456789 
• Security Header Record 30 
o Detail Record 31 
o Detail Record 31 
• Security Trailer Record 32 
 
Security Issue [[ID]] 987654321 
• Security Header Record 30 
o Detail Record 31 
o Detail Record 31 
• Security Trailer Record 32 
Grand Total Trailer Record 33 (summary record for Receiving Firm B) 
 
 
 

---

## Page 7

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
2. Processing 7 
Required Record Structure 
• The Security Header record (typically record type 30) introduces a series of records for a specific Security 
Issue [[ID]] and Fee Type (Commission Type) for which the Deliverer will send (or return2) a payment to a 
specific Receiver. 
• Following the Security Header record are detail records 31. Detail record sequence 1 is required. If the 
commission type represented on the header is for a trade related commission type, the second detail 
record must be used to facilitate trade related commission payout. Since this record has a field for a 
second name, it may be used for any payout, but its primary purpose is for trade related transactions. 
Detail record sequence 3 is optional. 
• A Security Trailer record 32 must follow all detail records relating to the Security Header record. This 
record recaps key information for the Security Issue [[ID]]: Deliverer [[NSCC]] [[participant]] number, total number 
of records, total debit dollar amount, and the total credit dollar amount. 
• A Grand Total Trailer record 33 is required for file control purposes to provide summary information for all 
records submitted by the Deliverer for a Specific Receiver. 
 
Corrections 
If a deliverer discovers that a file has been sent in error or contains inaccurate data, the deliverer may process 
another file to reverse the erroneous file. The deliverer will set the "Debit/Credit Indicator", in each Security 
Header, to offset the previous file and transmit to [[NSCC]] using the same DataTrak SYS-[[ID]] and input 
timeframes in accordance with the regular processing schedule. 
The submitted file must be sorted in Delivering Fund/Firm #, Receiving Firm/Fund number, and Security Issue 
[[ID]] order. Please note that the file sort sequence has been defined to maximize processing efficiencies. File 
sort sequence will be verified and out of sequence records will be rejected. 
Clients are able to transmit various types of commissions and fees through the [[DTCC]] Payment aXis
® system. 
To view the current [[DTCC]] Payment aXis® record layouts and commission/fee types go to 
https://dtcclearning.com/products-and-services/mutual-fund-services/[[DTCC]]-payment-axis.html#Record-Layouts
 
2 Return Payment Functionality was introduced in 2017. Return payment functionality utilizes Header Record 15. For additional information and best practices 
for return of payment, please refer to Section 4–DoL [[Fiduciary]] Rule: Enhancements and Best Practices.  

---

## Page 8

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
2. Processing 8 
Output Requirements 
[[NSCC]] creates two file outputs for the delivering and receiving clients: 
• Commission and Fee [[settlement]] MRO file (02102202) 
• Commission and Fee [[settlement]] Summary MRO (02102203) which contains payment [[settlement]] data.  
 
[[NSCC]] output files contain an AutoRoute Header which provides information such as the recipient [[participant]] 
number, the transmission date and the AutoRoute report [[ID]]. 
 
Rejected Records 
Upon receipt of records from the Deliverer of the file, [[NSCC]] will perform record validation to ensure the 
required record structure is preserved and fields are populated in accordance with the rules as specified in the 
record layouts. Records that [[DO]] not pass [[NSCC]] validation will be rejected and returned to the deliverer.  
Rejected detail records 31 are identified with a sequence number ‘9’ in place of detail record sequence 1. This 
record contains all fields as found on detail record number 1 with the exception of the "Name 1" field which is 
replaced by up to 7 reject code fields. If a record has more than 7 reject reasons, a reject code with a value of 
‘99’ is assigned in the 7th and last reject position. 
 
Acknowledgement Record 
An Acknowledgement record is an [[NSCC]] generated record sent to the Deliverer to acknowledge their input file 
that was accepted and processed by the system. This record summarizes input record counts, accepted and 
rejected debit and credit dollar amounts for input records submitted on the same file by the Deliverer.  
[[DTCC]] Payment aXis
® supports multiple input cycles and a single output cycle. [[NSCC]] will generate a separate 
Acknowledgement record for each deliverer for each input cycle. File deliverers can potentially receive multiple 
acknowledgements for a given cycle if more than one file is transmitted to [[NSCC]] during the cycle and other 
parties’ files were received in the same cycle (order of the received files will determine the number of 
acknowledgement records within a given cycle). 
 
Accepted Records 
Files/records (submitted by the Deliverer) that pass [[NSCC]] validation will be deemed “Accepted” by the system. 
The following accepted records will be transmitted to the intended Receiver(s): 
• Header Record 30 (or Header record 15 in the case of a returned payment) 
• Detail Record(s) 31 
• Trailer Record 32 
• Grand Total Trailer Record 34 is generated by [[NSCC]] and included at the end of the file for control 
purposes to provide information such as the total number of records, debit dollar amount and credit dollar 
amount for all accepted records submitted by the Deliverer(s) for this receiver. 
 
 

---

## Page 9

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
2. Processing 9 
[[DTCC]] Payment aXis® [[settlement]] File 
All [[DTCC]] Payment aXis® activity received by the cutoff time will be staged for [[settlement]]. This activity is 
summarized in the [[settlement]] Summary file (MRO 02102203). This file will be generated by [[NSCC]] and 
transmitted to all Delivering and Receiving parties. 
All delivering and receiving clients receive the summary [[settlement]] file, detailing the [[settlement]] activity due the 
following business day. The file will include the following records: 
• Security Issue [[ID]] [[settlement]] Detail record (record type 38) represents the total [[settlement]] amount of all 
the detail records transmitted the previous day for specific Security Issue [[ID]]’s for each 
Recipient/[[participant]]. 
• [[settlement]] Record by Contra [[participant]] (record type 39) is generated for each contra party of the 
Recipient. This record lists the total [[settlement]] amount of all Security Issue IDs for a contra party of the 
Recipient/[[participant]]. 
• Grand Total [[settlement]] record (record type 40) is generated for the Recipient to provide the Recipient’s 
net [[settlement]] amount for that specific date. 
Note: 
Detail Records 31 received in combination with a Header Record 30 (or Header Record 15) where “[[settlement]] Indicator” 
field is populated with “1=No [[settlement]]” or “2=Test” will NOT be settled through [[DTCC]] Payment aXis®

---

## Page 10

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
2. Processing 10 
Processing Overview 
Input from Delivering Funds/Firms 
The [[DTCC]] Payment aXis® process starts with the transmission of fee files from delivering Funds and Firms to 
[[NSCC]]. 
 
Output from [[NSCC]] 
[[NSCC]] passes all accepted [[DTCC]] Payment records received from the delivering Fund or Firm to the receiving 
Funds and Firms. These output files are available in a single-cycle transmission. 
 
[[settlement]] 
[[settlement]] for [[DTCC]] Payment aXis® files received by [[NSCC]] (by the cutoff time specified on the Transmission 
Schedule) occurs the next business day. [[NSCC]] notifies both parties (deliverer and receiver) of t heir pending 
debits and credits the day before [[settlement]]. 
The actual payment is netted on the [[settlement]] date with all other [[NSCC]] activity. On the [[settlement]] day, [[NSCC]] 
creates a summary [[settlement]] file (Autoroute 02132518), which is sent to receiving and delivering parties. The 
file contains [[DTCC]] Payment aXis
® [[settlement]] [[obligations]] for that day for this Autoroute recipient. The file will 
also specify [[settlement]] category as “18 = [[DTCC]] Payment aXis® Commission & Fee [[settlement]]”. 
[[DTCC]] Payment aXis® [[settlement]] is simplified by allowing delivering Funds and Firms to make one payment to 
[[NSCC]]. [[NSCC]] then distributes net payments to all brokers. 
 
Corrections 
Delivering Funds/Firms at times may need to adjust a payment that has been processed through the system. 
Funds/Firms may process corrections by transmitting another file with reversing entries through the [[DTCC]] 
Payment aXis
® system. It is recommended that contra parties (Receivers) receive corrections after their receipt 
of the incorrect communication. 

---

## Page 11

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
3. Processing Commission Payments Between Brokers 11 
3. PROCESSING COMMISSION PAYMENTS BETWEEN 
BROKERS 
Background 
Section C of Rule 52 of [[NSCC]]’s Rules and Procedures regarding [[NSCC]]’s Mutual Fund Commission 
[[settlement]] service (now known as the [[DTCC]] Payment aXis® service) was amended in 2005 to permit an 
[[NSCC]] mutual fund distributor [[Member]] to submit commission, fee payments, and data to another [[NSCC]] mutual 
fund distributor [[Member]]. As a result, [[NSCC]]’s [[DTCC]] Payment aXis® service allows a Firm to submit 
commissions and various fees to other Firms. 
[[DTCC]] Payment aXis® includes [[Broker]] to [[Broker]] transaction capability which provides increased efficiencies to 
the mutual Fund industry and to those Firms active in retirement planning.  
This functionality supports the way retirement plan processing commissions are handled today, wher e 
proprietary and non-proprietary Fund investments both figure in a plan’s offerings. 
 
Benefits 
In a non-automated environment when there is a [[Broker]]-to-[[Broker]] retirement plan relationship, mutual Fund 
commissions are paid directly by the Fund company to the initiating [[Broker]] by check or through other non-
standardized methods. Some payments may be lost or issued incorrectly, and compensation sometimes is 
sent without supporting documentation resulting in costly processing and reconciliation.  
[[DTCC]] Payment aXis® provides initiating brokers with a breakdown of information that helps them more 
accurately track payments; streamlining the process and providing the industry with a secure, automated, and 
operationally efficient pipeline. 
Within Funds’ 401(k) business, Funds offer proprietary Funds and non-proprietary Funds to [[Broker]] dealers who 
come to them because they have access to a broad range of Fund investments. By using [[DTCC]] Payment 
aXis® service to send out a rich set of data to accompany payment, Funds can provide a much- needed service 
to their business partners. 
What makes [[DTCC]] Payment aXis® beneficial, in addition to automation, is “equalization” of commission 
payments. For example, Funds pay different compensations, and on a customer statement that can be 
perceived as a conflict of interest in the eyes of a customer, especially if that person is holding [[shares]] in 
numerous Fund families. It can create an impression that a financial advisor is directing more money toward 
one Fund than another. And with continuous focus on fee disclosure and transparency, uniform compensation 
can make it easier to comply with requirements. 
In 2013 [[DTCC]] Payment aXis® system was enhanced to facilitate the payment of Omnibus fees. For information 
on this service and recommended practices please refer to the “[[DTCC]] Payment aXis® Invoicing and Fee 
[[settlement]] Guide” on Learning https://dtcclearning.com/documents/mutual-fund-services-1/[[DTCC]]-payment-
axis/guides-10/1806-[[DTCC]]-payment-axis-invoicing-and-fee-[[settlement]]-guide/file.html under the [[DTCC]] Payment 
aXis® section.  
 
 
 
 
 
 

---

## Page 12

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
3. Processing Commission Payments Between Brokers 12 
[[DTCC]] Payment aXis® Procedures 
This functionality is to be used when a retirement plan provider acting in the capacity of a record keeper or 
[[Broker]]/dealer of Funds (multiple mutual Fund families) offered in the plan program wishes to process a level or 
equalized commission across all mutual Fund investment choices. In this capacity, the Firm may receive a 
commission from the Funds in connection with the mutual Fund transactions in such Funds to pay a level or 
equalized amount over to another Firm which directed the purchase of the Fund [[shares]] in the plan.  
 
Requirements 
No new DataTrak SYSID numbers will be needed. However, Firms must contact their Relationship Manager for 
proper set up of SYSID to be able to input through the [[DTCC]] Payment aXis
® system. 
 
Record Layouts 
[[DTCC]] Payment aXis® record layouts are available on the Learning Center:  
https://dtcclearning.com/products-and-services/mutual-fund-services/[[DTCC]]-payment-axis.html#Record-Layouts 
 
 

---

## Page 13

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
4. DoL [[Fiduciary]] Rule–Enhancements and Best Practices 13 
4. DOL [[Fiduciary]] RULE–ENHANCEMENTS AND BEST 
PRACTICES 
Background 
On April 6, 2016, the Department of Labor (DoL) issued a [[regulation]] defining who is a “[[Fiduciary]]” of an employee 
benefit plan under the Employee Retirement Income Security Act of 1974 (ERISA) as a result of giving investment 
advice to an employee benefit plan, plan [[Fiduciary]], plan [[participant]] or beneficiary, individual retirement account 
(IRA), or IRA owner.  The rule defined persons who provide investment advice or recommendations for a fee or 
other compensation with respect to assets of a plan or IRA as fiduciaries in a wider array of advice relationships.  
[[NSCC]] in conjunction with the DoL [[NSCC]] Enhancements Working Group of the Investment Company Institute’s 
(ICI) [[Broker]]/Dealer Advisory Committee and Bank, Trust and Retirement Advisory Committee (respectively; the 
“Working Group”) defined enhancements to the [[Mutual Funds]] Services necessary for our clients to comply with 
the DoL rule.  To see a complete list of enhancements, please refer to Important Notice a8286.  All DoL-related 
best practices provided in this document were identified and approved by the working group in advance of the 
rule’s applicability date. 
Note: The original applicability date of April 10, 2017 was delayed by DoL. On March 15, 2018, The Fifth Circuit 
Court of Appeals, based in New Orleans, vacated the [[Fiduciary]] rule. On June 21, 2018, The Fifth Circuit Court of 
Appeals confirmed its decision to vacate the ruling as such all references to requirements under the rule have 
been removed within this section. 
 
DoL Enhancements and Best Practices 
In preparation for the DoL rule’s applicability date of June 9, 2017 intermediaries assessed their business 
models and compensation structures to determine their course of action to ensure they are compliant w ith the 
rule. In order to comply with the rule, a number of firms made business decisions to implement “levelized” 
compensation in lieu of commissions. This is accomplished by moving their retirement accounts into managed 
(advisory) account arrangements that allow for level-fee compensation structure. 
 
Level-Fee Based Compensation Fees 
In order to support the level-fee structure, [[NSCC]] added the following commission types to be used with the 
existing “Commission Type” field: 
• 17 = Level Indirect Retirement Plan Compensation 
o This fee is intended to represent a third party (for example from a trust, record keeper and not paid 
directly by the plan, plan sponsor, or plan [[participant]]) commission payment based upon a set 
(predetermined) rate calculated equally across all commissionable plan assets. 
• 18 = Level Fee Bases Retirement Plan Compensation 
o This fee is intended to represent plan-level advisory compensation in an amount based on a pre- 
arranged agreement between the service provider (e.g. RIA) and the plan. 
 
Commission types 17 and 18 allow for communication and [[settlement]] of level fee -based compensation. These 
fee types will be provided by record keepers when communicating and remitting “levelized” fees to firms that 
utilize a levelized compensation structure. It is expected that record keepers will act as common remitters 

---

## Page 14

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
4. DoL [[Fiduciary]] Rule–Enhancements and Best Practices 14 
where upon instruction by the firm they will collect fees from the funds, levelize all collected fees, aggregate the 
fees across a number of funds and remit the fee as one payment to the firm utilizing commission type 17 or 18. 
Best Practice: 
The following best practices were recommended by the working group when utilizing commission types 17 and 
18: 
• “Customer Account Indicator” field - populate with the value of “1=Dealer”. “Customer Account” field 
should provide the dealer account number. The levelized fee remitted by the record keeper will represent 
an aggregate fee across a number of various funds; therefore “Customer Account” must contain the firm 
number. 
• “SSN/TIN Number Indicator” field - populate with the TIN on the plan account. “SSN/TIN Number” field - 
provide the tax identification number (TIN) of the plan. 
• “Branch [[ID]] Number” field should be populated in the same manner as utilized by the other commission 
types. 
 
Client-Created Security Issue [[ID]] 
[[DTCC]] Payment aXis® allows for transmission and remittance of fees for registered as well as non- registered 
(internal client-created) Security Issue IDs (“Security Issue [[ID]]” field). 
The Optional/Conditional “Security Issue [[ID]] Indicator” field was added to [[DTCC]] Payment aXis ® to allow record 
keepers to specify if the Security Issue [[ID]] for a particular levelized compensation is an internal client -created or 
a registered Security Issue [[ID]]. The field contains the following options:  
• Blank. Blanks will be used for all commission types, excluding the level-fee types 17 and 18. 
• 1 = Internal client-created Security Issue [[ID]] 
• 2 = Registered Product-Level Security Issue [[ID]] 
 
This field is required for Commission Types 17 and 18 when provided by record keepers to communicate and 
remit levelized fees to the firms at the product level. The Security Issue [[ID]] associated with the product can be a 
registered or non-registered (created internally by the record keeper) [[ID]]. The new values will allow record  
keepers to specify whether the value provided in the “Security Issue [[ID]]” is a registered Security Issue [[ID]] or a 
non-registered product-level [[ID]] created by [[DTCC]]’s clients. 
It is recommended that clients follow the best practice algorithm when constructing a non-registered Security 
Issue [[ID]]: NNNNXXXXX 
• NNNN–[[NSCC]] [[participant]] number of the [[DTCC]] Payment aXis
® record submitter 
• XXXXX–alpha/numeric sequence 
 
Return Payment functionality 
Firms which made a business decision to utilize levelized compensation structure might have internal policies 
and procedures that will not permit them to collect certain commission types on their clients’ retirement 
accounts. In the event the firm will receive this type of payment through [[DTCC]] Payment aXis
® they will need 
the ability to return such a payment to the original payment deliverer. For example, firms  that will only allow 
levelized compensation may opt to return a payment for a 12b-1 commission on a retirement plan account with 
social code of “12=401(k) Plan non-prototype”. 
In order to provide our clients with a standardized automated solution that will allow for an efficient and 
centralized method to return prohibited payments, [[NSCC]] enhanced the existing [[DTCC]] Payment aXis
® 

---

## Page 15

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
4. DoL [[Fiduciary]] Rule–Enhancements and Best Practices 15 
functionality to allow intermediaries to return payments that are not allowed by their policies to the original 
payment deliverer and provide a reason code. 
Note: 
Return payment functionality was designed and implemented to allow intermediaries to return payments that are prohibited 
by their policies as a result of their implementation of the DoL [[Fiduciary]] Rule. Clients are advised NOT to use this 
functionality at this time to return other (non-DoL related) payments that were sent in error, etc. This functionality will be 
discussed with the members of the ICI BDAC and BTRAC committees to determine if there is an opportunity to expand the 
use of this system capability to all payments that clients need to return to their counterparties. 
Return payment functionality is not intended to and will not prevent the original payment from [[settlement]]. All 
payments submitted to [[DTCC]] Payment aXis® with the “[[settlement]] Indicator” field set to “[[settlement]]” (including 
the payments that may not be allowed by the firm’s policies) will continue to be settled through [[DTCC]] Payment 
aXis®. Subsequently, firms may return payments to the original payer and the returned payments will settle 
through [[DTCC]] Payment aXis® as a Credit to the original payer. It is important to note that returned payments 
functionality was modeled after the original commission payment functionality where payers send a payment 
through [[DTCC]] Payment aXis
® and it is settled based on the payer’s instructions.  
The receiving party (payee) does not have the ability to acknowledge, confirm or reject the payment. The return 
payment functionality follows the same logic where returned payments are settled based on the firm’s 
(submitter’s) instructions. The original payer will be credited the returned payment amount based on the 
submitter’s (firm’s) instructions. Returned payment receiver will not have the ability to acknowledge, confirm or 
reject this returned payment. 
[[NSCC]] does not store [[DTCC]] Payment aXis
® records, therefore each transaction is treated as a standalone 
payment instruction and returned payments are not systematically matched with the original payment that is 
being returned. 
In order to return a particular payment/set of payments that are not allowed by the firm’s internal policies and 
procedures, the firm will need to adhere to the required [[DTCC]] Payment aXis
® record structure and provide the 
following set of records*: 
Returned Payment 1 
• Header Record 15 
o Detail record(s) 31 
• Trailer Record 32 
Returned Payment 2 
• Header Record 15 
o Detail record(s) 31 
• Trailer Record 32 
Grand Total Trailer Record 33 
Note 
for additional record input/output information, please refer to Section 2 – Processing and [[DTCC]] Payment aXis® record 
layouts. 
Header Record 15 was specifically designed to return payments that are prohibited by the firm’s policies as a 
result of the DoL rule implementation. This header was built for Credit only where firms will return payments to 
original payers and specify a reason for returning these payments. 
Returned payments records will be included in the Commission and Fee [[settlement]] File (AutoRoute MRO 
02102202). Commission and Fee [[settlement]] Summary MRO File (AutoRoute 02102203) will reflect debits and 
credits from payment remittance as well as returned payment activity.  
 

---

## Page 16

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
4. DoL [[Fiduciary]] Rule–Enhancements and Best Practices 16 
Both files will continue to process in accordance with the [[DTCC]] Payment aXis® transmission schedule 
(available on the Learning Center) at https://dtcclearning.com/products-and-services/mutual-fund-
services/schedules.html.  
For information on input/output processing, please refer to Section 2–Processing. 
 
Important Fields 
• The following fields should be populated with the same value as provided on the original payment record 
that is being returned: 
o “Commission Type” field 
o “Social Code” 
o “Fund/Firm Processing Date” field 
• “Returned Payment Reason Code” field must be populated with the appropriate payment return reason 
code 
• “Debit/Credit Indicator” field must be “2” =Credit 
 
Best Practice 
Firms should make every effort to return payments to the original payment deliverer within 24 to 48 hours of 
receipt and not exceed five business days from the original [[settlement]] date 3. Firms are required to provide the 
reason for returning the payment in the “Returned Payment Reason Code” field. Firms should also contact the 
fund/original payment remitter to provide a detailed explanation for returning the payment and adjust the 
accounts accordingly to avoid future payments on the account. 
Firms are advised to work with their fund partners in advance of the June 9, 2017 implementation date to 
ensure client accounts reflect the appropriate social codes and discuss firms’ expectations for fee types that 
will be prohibited by the firm’s internal policies. 
It is recommended that firms return all prohibited payments in their entirety as it might be challenging for the 
receiver to match partial returns to the original payment. It is also recommended that firms populate the fields 
with the data provided by the original payment deliverer on the original set of Header, Detail and Trailer 
records. 
 
3 As firms initially implement return payment functionality, it may be difficult to meet the recommended practice return payment window. Factors that could slow 
turnaround include the number of affected payments, amount of research to identify and prepare payment returns, and adjustments to processes and procedures. 
Firms and funds should remain in close communication on progress being made toward adopting the recommended practice.  

---

## Page 17

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
4. DoL [[Fiduciary]] Rule–Enhancements and Best Practices 17 
Additional Fields/Values 
The following fields/values allow for communication of key data points related to IRA and retirement plan 
accounts. 
• Optional/Conditional “Customer Account Indicator 2” and “Customer Account 2” fields were added to 
Detail Record 31. This enhancement is intended to allow both the BIN and Customer Account numbers to 
be provided (if both accounts are available). These fields will be used in combination with the “Customer 
Account Indicator” and “Customer Account” fields. 
Best Practice: 
o “Customer Account Indicator 2” and “Customer Account 2” fields should be used in combination with 
the “Customer Account Indicator” and “Customer Account” fields. 
o Clients are advised to provide both the Dealer and Fund account numbers (if both accounts are 
available). 
o The value in the “Customer Account Indicator 2” and “Customer Account 2” fields should not be the 
same as the values in the “Customer Account Indicator” and “Customer Account” fields.  
• “Systematic Investment Purchase” value was added to the “Transaction Type” field, allowing clients to 
indicate commission payment is the result of a systematic investment purchase.  

---

## Page 18

Chapter 1: Commission and Fee [[settlement]] User Guide/Best Practices 
5. Adding the Service 18 
5. ADDING THE SERVICE 
Existing [[NSCC]] Members 
Contact your [[NSCC]] Relationship Manager. 
If appropriate, contact your service provider about adding the service. 
 
Prospective Members 
Begin contacting your Mutual Fund/[[Broker]] business partners and discuss how the service can be mutually 
beneficial. Please refer to the List of Mutual Fund Products Utilized by Firms and Funds on the [[DTCC]] website.  
These identify all participating Funds and brokers who are currently using all Mutual Fund services:  
https://www.[[DTCC]].com/wealth-management-services/mutual-fund-services/mutual-funds-client-public-
documentation 
If you have any questions, please contact your Relationship Manager or Wealth Management Services at 212-
855-8877. 
 
 
 

---

## Page 19

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Info: July 26, 2023 
Publication Code: MFS299 
Service: [[DTCC]] Payment aXis® 
Title: Chapter 1: Commission and Fee [[settlement]] User Guide / Best Practices 
 
 
 
For More Information 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com  