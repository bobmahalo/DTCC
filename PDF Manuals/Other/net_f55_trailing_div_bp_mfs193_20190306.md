---
title: "Trailing Dividends - Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_f55_trailing_div_bp_mfs193_20190306.pdf"
pages: 9
size: "221.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Trailing Dividends - Best Practices

**Original File:** [net_f55_trailing_div_bp_mfs193_20190306.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_f55_trailing_div_bp_mfs193_20190306.pdf)  
**Category:** Other  
**Total Pages:** 9  
**File Size:** 221.4 KB  

---

## Page 1

 
 
NETWORKING 
TRAILING DIVIDENDS BEST PRACTICES - F55 ACTIVITY RECORD 
MARCH 06, 2019 
 
 
 


---

## Page 2

 
 
Copyright© 2019 by The Depository Trust & Clearing Corporation (“[[DTCC]]”) 
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
 
Doc Info: March 6, 2019  
Publication Code: MFS193 
Service: Networking 
Title: Trailing Dividends Best Practices – F55 Activity Record 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Background and Objectives ................................................................................................................................ 4 
Best Practice ......................................................................................................................................................... 5 
Benefits of Utilizing Transaction Type 13 (Direct Transfer) ................................................................................ 5 
Following Are Key Data Points That Should Be Provided When Utilizing the F55 Record to Report a Trailing 
[[Dividend]] .............................................................................................................................................................. 5 
Firm/Fund Identification Number field (F55 Activity, seq 1) .............................................................................. 5 
Underlying Customer Account Number field (F55 Activity, seq 4) .................................................................... 6 
Opposing Fund Account Number field (F55 Activity, seq 4) ............................................................................. 6 
Opposing Underlying Customer Account Number field (F55 Activity, seq 5) ................................................... 6 
Original Control Number field (F55 Activity, seq 4) ........................................................................................... 6 
Use Case ............................................................................................................................................................... 7 
Use Case - Best Practices for Populating F55 Fields ......................................................................................... 7 
Mapping of ACAT 018, Networking B52, and Manual Transfer Fields to Networking F55 Fields  ...................... 8 
 

---

## Page 4

Trailing Dividends Best Practices - F55 Activity Record 
Background and Objectives 4 
BACKGROUND AND OBJECTIVES 
A trailing [[Dividend]] occurs when a [[Dividend]] is paid in a mutual fund ([[Equity]] or accrual) prior to, or during, the 
process of a full transfer.  Fund Company [[transfer agent]] systems vary in how they send and report trailing 
dividends to intermediaries, which leads to many downstream impacts (especially to intermediaries) including 
omnibus-to-beneficial-owner account reconciliation issues and difficulty building related cost basis expectancy 
files.  To address this concern, the ICI Mutual Fund Transfers Working Group developed the best practices 
outlined in this document.  The scope of this document addresses trailing dividends that originally pay as a 
distribution in the delivering account, and then are moved to the receiving account via a subsequent Fund 
initiated transaction leveraging the [[NSCC]] F55 Networking Activity record.  
Explanation of current environment:  
The transaction types used to report the [[shares]] that ‘trail’ the initial transfer vary between Fund Company 
[[transfer agent]] systems.  The differences in usage are typically attributed to whether the [[transfer agent]] system 
can separately discern trailing dividends generated by transfer vs. other redemption activity . 
When reporting the trailing [[Dividend]] via a Fund initiated transaction utilizing the Networking Activity (F55) 
record, the Transaction Types commonly used are: 
• Transaction Type 12 (Reinvest from other Fund) 
• Transaction Type 13 (Direct Transfer)  
 

---

## Page 5

Trailing Dividends Best Practices - F55 Activity Record 
Best Practice 5 
BEST PRACTICE 
The best practice is for Fund [[Companies]] to utilize Transaction Type 13 (Direct Transfer) on the F55 record 
when sending a trailing [[Dividend]] following any full transfer (ACAT -Fund/SERV, Networking B52, or manual).  
Transaction Type 13 (Direct Transfer) requires F55 sequences 4 and 5, which include data point fields that are 
key for reconciliation of trailing dividends.   
Benefits of Utilizing Transaction Type 13 (Direct Transfer)   
• Requires the necessary record sequences containing key fields for reconciliation purposes  
• Triggers a firm to look for the necessary cost basis records (or request them if needed), as they realize a 
transfer occurred  
• Usage corresponds with Cost Basis Reporting Best Practices  
• Follows a similar process to an ACAT residual credit, transfer of dividends or any other activity that results 
in residual [[shares]] left in the account, that is used in the [[Broker]] to [[Broker]] transfer space  
• Reduces the risk of duplicate [[Dividend]] reporting since the [[intermediary]] will receive the [[Dividend]] as a 
transfer, alerting them to not apply it to the client account as a [[Dividend]] (the [[Dividend]] reporting information 
would have already been provided to the delivering side of the request).   
 
 
Notes: 
 
Since the full scope of changes to support this best practice may take some time to implement, when possible, changes 
should be phased in as incremental progress is made based on feedback from intermediaries.  
If a Transaction Type other than 13 (Direct Transfer) is used when reporting trailing dividends on the F55 record, the fields 
on sequences 4 and 5 identified in this document should be utilized. 
Following Are Key Data Points That Should Be Provided When 
Utilizing the F55 Record to Report a Trailing [[Dividend]] 
Firm/Fund Identification Number field (F55 Activity, seq 1) 
This field should be populated with the receiving firm’s account number at the fund company.  
• Fund Account Number or FIN  
• Firm’s account number at the fund company that the [[shares]] are moving to  
 
 
 
 
 

---

## Page 6

Trailing Dividends Best Practices - F55 Activity Record 
Best Practice 6 
 
Underlying Customer Account Number field (F55 Activity, seq 4) 
This field should be populated with the underlying client’s account number at the receiving firm. 
• For omnibus situations, the underlying account number (client account) to which the [[shares]] are moving  
 
Opposing Fund Account Number field (F55 Activity, seq 4) 
This field should be populated with the delivering firm’s account number at the fund company. 
• Fund Account Number or FIN 
• Account Number of the delivering firm at the fund company, where the [[shares]] are moving from  
• Considered by firms to be the account number at the contra firm 
• For Retail to [[Broker]] transfers, or direct from fund (PTF, manual B52) transfers, this would be the account 
number of the client’s account that was directly held by the fund company 
 
Opposing Underlying Customer Account Number field (F55 Activity, seq 5) 
This field should be populated with the underlying client’s account number at the delivering firm. 
• For omnibus situations, the underlying account number (client account) from which the [[shares]] are moving  
• Considered by firms to be the underlying customer account number at the contra firm  
 
Original Control Number field (F55 Activity, seq 4) 
This is the Control number of the original transfer if processed via [[NSCC]]. 
 
Note:  
The ability for Fund [[Companies]] to supply the above data is dependent upon the inclusion of the data on the original B52, 
ACAT, or within the letter of instruction from the [[intermediary]] for a manual transfer. 
 

---

## Page 7

Trailing Dividends Best Practices - F55 Activity Record 
Use Case 7 
USE CASE 
The following use case takes a common scenario and shows how the best practice can help close the trailing 
[[Dividend]] reconciliation and reporting gaps that exist today: 
Example – ACATS PTF without an Underlying Delivering Account Number, to an omnibus account with an 
underlying receiving client account number 
ABC [[Broker]]/Dealer (receiving firm) has initiated a full ACATS PTF transfer with the Ginormous Growth Fund 
(delivering firm) on behalf of Customer Jane Smith. The ACATS PTF is processed on payable date for the 
Ginormous Growth Fund.  
• ABC [[Broker]]/Dealer has an omnibus account at the fund (Account 99925) and tracks Ms. Smith’s position 
on their sub-accounting platform (Account 10065432).   
• Ms. Smith’s account at the fund is a directly-held position (Account 28723).  
 
Following the initial transfer, Ms. Smith’s trailing [[Dividend]] is paid out and reported via [[NSCC]] Networking F55 
(Activity Record).  
Use Case - Best Practices for Populating F55 Fields  
 
• Firm/Fund Identification Number field on F55 (Sequence #1, Position 25-44): 99925  
• Underlying Customer Account Number field on F55 (Sequence #4, Position 76-95): 10065432  
• Opposing Fund Account Number field on F55 (Sequence #4, Position 39-58): 28723  
• Opposing Underlying Customer Account Number field on F55 (Sequence #5, Position 28-47): “Blank” 
(there is no underlying account number at the Ginormous Growth Fund)  
• Original Control Number field on F55 (Sequence #4, Position 23-37): 1234567891011  
 
 
 

---

## Page 8

Trailing Dividends Best Practices - F55 Activity Record 
Use Case 8 
 
Mapping of ACAT 018, Networking B52, and Manual Transfer Fields to Networking F55 Fields 
 
 
 


---

## Page 9

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
corelearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 