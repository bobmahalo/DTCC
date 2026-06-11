---
title: "Fund/SERV® Technical Guide, Chapter 1 – Introduction to FUND/SERV"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_techguide_ch1_mfs344_20230928.pdf"
pages: 10
size: "265.6 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Fund/SERV® Technical Guide, Chapter 1 – Introduction to FUND/SERV

**Original File:** [fs_techguide_ch1_mfs344_20230928.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_techguide_ch1_mfs344_20230928.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 10  
**File Size:** 265.6 KB  

---

## Page 1

 
 
 
FUND/SERV® 
FUND/SERV® TECHNICAL GUIDE, CHAPTER 1 – 
INTRODUCTION TO FUND/SERV 
September 28, 2023 
  

---

## Page 2

FUND/SERV® TECHNICAL GUIDE, CHAPTER 1 – Introduction to FUND/SERV 
Introduction to Fund/SERV 2 
CHANGE HISTORY 
Dates Description 
September 28, 2023 Document was rebranded and reviewed.  
July 2022 Learning upgrade caused some link(s) to break.  Links corrected. 
November 03, 2020 Document was rebranded.  Links corrected. 
September 24, 2013 Document was updated. 
  

---

## Page 3

FUND/SERV® TECHNICAL GUIDE, CHAPTER 1 – Introduction to FUND/SERV 
Introduction to Fund/SERV 3 
TABLE OF CONTENTS 
Introduction to Fund/SERV ................................................................................................................................. 4 
Introduction ......................................................................................................................................................... 4 
Executive Summary ............................................................................................................................................ 4 
Other Mutual Fund Services ............................................................................................................................... 5 
References .......................................................................................................................................................... 5 
Definition ............................................................................................................................................................. 5 
System Output .................................................................................................................................................... 6 
Background ......................................................................................................................................................... 6 
Fund/SERV Implementation ............................................................................................................................... 6 
ACATS Interface ................................................................................................................................................. 6 
Fund/SERV [[Member]] Profile and Security Profile ............................................................................................... 6 
Disaster Recovery............................................................................................................................................... 6 
Benefits ............................................................................................................................................................... 7 
Types of Orders .................................................................................................................................................. 7 
Security Types .................................................................................................................................................... 7 
Firm and Fund Capabilities ................................................................................................................................. 8 
Firm Capabilities ................................................................................................................................................ 8 
Fund Capabilities ............................................................................................................................................... 8 
 

---

## Page 4

FUND/SERV® TECHNICAL GUIDE, CHAPTER 1 – Introduction to FUND/SERV 
Introduction to Fund/SERV 4 
INTRODUCTION TO FUND/SERV 
Introduction 
The Fund/SERV technical manual has been designed to provide a detailed view of these services and their 
processing requirements. Use of this manual and the related information will be helpful to you as you build your 
Fund/SERV interface to National [[securities]] Clearing Corporation ([[NSCC]]), as well as provide answers to your 
processing questions once you begin to utilize these services. 
When you have finished reviewing you should have a better understanding of:  
• The functionality of the systems 
• The communication requirements 
• The processing capabilities of the services 
• Each [[participant]]’s role within the services 
• Data submission formats 
• Related Forms 
• Reject Codes 
 
We invite you to take a moment to review or print the information contained within and contact us with any 
question that you may have. Our Wealth Management Services can be reached at 212-855-8877 to assist you 
with your inquiries. 
Executive Summary 
This manual has two purposes: 
• To acquaint you with the capabilities of the mutual fund order entry, [[settlement]], registration, and 
verification system known as Fund/SERV 
• To provide you with the record layouts and specifications for all input and output capabilities with 
Fund/SERV. 
 
Fund/SERV, [[NSCC]]'s central processing system for mutual fund transactions, enables mutual fund distributors 
and firms to enter, confirm, settle and register purchase, exchange and redemption orders in an efficient and 
automated environment. The service standardizes mutual fund policies, reduces operating costs, and speeds 
transaction settlements. 
  

---

## Page 5

FUND/SERV® TECHNICAL GUIDE, CHAPTER 1 – Introduction to FUND/SERV 
Introduction to Fund/SERV 5 
Other Mutual Fund Services 
[[NSCC]] offers a number of ancillary services designed to assist in their efforts to achieve cost effective and 
efficient operations. These include the following: 
• Automated Customer Account Transfer System (ACATS): An automated system for the timely transfer of 
client accounts between firms, including their mutual fund positions. 
• Networking: A centralized and standardized data communication system for the exchange of mutual fund 
customer level information and activity, including net [[settlement]] of dividends and activity.  
• Mutual Fund Profile Service (MFPS): Provides participants with mutual fund information in an efficient, 
automated, affordable, and centralized facility. 
• [[DTCC]] Payment aXis: Automates the processing of commissions and various mutual fund fee types, 
including the transmission and [[settlement]] of invoices for [[Broker]] controlled and retirement plan accounts . 
• Transfer of Retirement Assets (TORA): Automates the transfer of retirement assets from one mutual fund 
company to another using Fund/SERV. 
• Defined Contribution Clearance and [[settlement]] (DCC&S): Standardizes, centralizes, and automates the 
processing of defined contribution mutual fund transactions, using existing and enhanced capabilities of 
Fund/SERV, Networking, and the Mutual Fund Profile Service. 
 
All these services provide clients with the advantages and benefits of automated mutual fund processing. 
Trusts doing mutual fund processing can also take advantage of Fund/SERV and Networking services.  
References 
For more information on Mutual Fund Services, please call 1-212-855-8877 or refer to Mutual Fund Services 
section on [[DTCC]].com @ https://www.[[DTCC]].com/wealth-management-services/mutual-fund-services 
Definition 
The following generic terms are used within this manual: 
• Firm refers to, but is not limited to, an [[NSCC]] Settling [[Member]] (e.g., [[Broker]]-dealer, bank, financial service 
firm, trust company or other financial [[intermediary]]). 
• Fund refers to a Fund [[Member]] accepting orders for mutual fund purchases and redemptions.  
• [[NSCC]] refers to the National [[securities]] Clearing Corporation. 
• Participants/clients refer to, but are not limited to, firms and funds. 
• System refers to Fund/SERV, [[NSCC]]'s Mutual Fund/[[settlement]], entry, Registration and verification 
System. 
• Day or days generally means [[NSCC]] business days. Fund/SERV operates five days a week, Monday 
through Friday, and follows the [[New York Stock Exchange]] holiday schedule.  
 
 
 

---

## Page 6

FUND/SERV® TECHNICAL GUIDE, CHAPTER 1 – Introduction to FUND/SERV 
Introduction to Fund/SERV 6 
System Output 
Throughout this manual, references to [[NSCC]] or Fund/SERV providing output, means that the System makes 
information available in automated form to clients for their retrieval and use. 
Background 
[[NSCC]] developed the Fund/SERV System at the request of the Investment Company Institute (ICI), the National 
Association of [[securities]] ([[NASD]]), and an industry task force composed of firms and [[Mutual Funds]] in response 
to the significant growth in [[Mutual Funds]] as an investment vehicle. 
The ICI/[[NASD]] Operations task Force was focusing attention on the industry's expanding volume and asked 
[[NSCC]] to provide a central processing system for automated order entry, confirmation, registration and [[settlement]] 
of mutual fund orders. 
Fund/SERV Implementation 
Fund/SERV was implemented in March 1986, with the help and support of a Joint Operations Task Force 
representing ICI and the [[NASD]]. 
ACATS Interface 
Fund/SERV also provides an interface with the Automated Customer Account Transfer System (ACATS), which 
is used to expedite the transfer of security positions when a client moves from one firm to another. ACATS, with 
the defined minimum requirements, standardizes mutual fund procedures, reduces operating costs, and speeds 
transaction settlements. 
Fund/SERV [[Member]] Profile and Security Profile 
The [[Member]] and Security Profiles (not to be confused with [[NSCC]]'s Mutual Fund Profile Service) allows firms 
and funds to set their processing capabilities for Fund/SERV. 
Participants may choose options for their communication level (e.g., single- batch, multi-batch, and interactive) 
or establish their ability to support functionality for exchanges, Cash adjustments, Firm Exits, etc. 
Additionally, funds may set their Security Issue [[ID]] descriptions and processing capabilities such as security type 
(e.g., Load, No-load), [[settlement]] file (e.g., Same Day or Next Day), and order processing cycle (e.g., T+1, T+2). 
Disaster Recovery 
Note: 
For further information on security, disaster recovery, and system back-ups, call Mutual Fund Services at (212) 855-8877. 
  

---

## Page 7

FUND/SERV® TECHNICAL GUIDE, CHAPTER 1 – Introduction to FUND/SERV 
Introduction to Fund/SERV 7 
Benefits 
Fund/SERV provides the following benefits to participants: 
• Centralized mutual fund order entry, confirmation, registration, and net [[settlement]] via [[NSCC]].  
• Increased volume capacity for [[Mutual Funds]] and firms, enabling them to easily expand along with the 
industry. 
• Simplified [[settlement]] process by calculating a net money [[settlement]] figure for each [[participant]] every day.  
• The support of multiple [[settlement]] cycles, including same-day [[settlement]]. 
• The accommodation of various processing capabilities, including single-batch, multi-batch, and interactive 
communications. 
Note:   
The system’s open format allows data entry throughout the day. 
• The support of complex, high-volume processing needs associated with accounts that are transferred. 
• The potential for cost savings to clients through economies of scale. 
• Flexible operating procedures and diversity of products, and 
• State of the art technology platforms. 
 
Types of Orders 
Fund/SERV processes five types of orders covering purchases, redemptions, and exchanges. These are 
described in the table below: 
Order Type Description 
Regular Regular orders are submitted by a firm on Trade Date, the day that an order is 
placed with a fund. 
As-Of As-Of orders are submitted by the firm through Fund/SERV after the Trade Date. 
Fund-Originated Order Fund-originated orders are submitted by the fund through Fund/SERV on Trade 
Date. 
Fund-Originated As-Of Order Fund-originated as-of orders are submitted by the fund through Fund/SERV after 
the Trade Date. 
Exchange Exchange orders are submitted by a firm on Trade date, the day that an order is 
placed with a fund. 
 
Security Types 
Security Types supported by Fund/SERV are available on the [[DTCC]] Learning Center site. Please reference 
the Fund/SERV® Security Types Identifiers https://dtcclearning.com/documents/mutual-fund-services-1/fund-
serv/codes/1969-fund-serv-security-types-identifiers/file.html  Login Required. 

---

## Page 8

FUND/SERV® TECHNICAL GUIDE, CHAPTER 1 – Introduction to FUND/SERV 
Introduction to Fund/SERV 8 
Firm and Fund Capabilities 
Firm Capabilities 
Firms have the following capabilities within Fund/SERV: 
• Regular order 
• As-Of Order 
• Correction 
• Exchange Order 
• As-Of Exchange Order 
• Short Registration 
• Full Registration 
• Firm Delete 
• Firm Exit 
• Extended Correction Transfer 
• Cash Adjustment 
• Defined Contribution 
• Post [[settlement]] Correction/Cancellation 
• Post [[settlement]] Exchange Cancellation 
• Alternate [[settlement]] Transaction (Non-[[NSCC]] Settling Transaction) 
 
Fund Capabilities 
Funds have the following capabilities within Fund/SERV: 
• Confirmation 
• Reconfirmation 
• Exchange Confirmation 
• Exchange Reconfirmation 
• Registration Acknowledgement 
• Delete Pending Registration 
• Release to [[settlement]] 
• Transfer of Retirement Assets (ToRA) 
• ToRA Confirmation 
• ToRA Reconfirmation 
• ACAT Transfer Acknowledgement/Rejection 
• Extended Correction Transfer Acknowledgement 
• Post [[settlement]] Cancellation/Correction by Fund 

---

## Page 9

FUND/SERV® TECHNICAL GUIDE, CHAPTER 1 – Introduction to FUND/SERV 
Introduction to Fund/SERV 9 
• Fund Reject 
• Fund Delete 
• Fund-Originated Order 
• Fund-Originated As-Of Order 
• Registration Rejection 
• Cash Adjustment 
• Delete Pending Release to [[settlement]] 
• Receiving Fund Exit from ToRA 
• ToRA Acknowledgement 
• Money Market Purchase Acknowledgement 
 

---

## Page 10

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 28, 2023 
Publication Code: MFS344 
Service: FUND/SERV® 
Title: Fund/SERV® Technical Guide, Chapter 1 – Introduction to FUND/SERV  
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 