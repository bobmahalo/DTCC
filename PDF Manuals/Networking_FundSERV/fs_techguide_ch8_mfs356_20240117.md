---
title: "Technical Guide, Chapter 8 – Linking SSN/EINs to Determine Breakpoint Eligibility"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_techguide_ch8_mfs356_20240117.pdf"
pages: 7
size: "295.9 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Technical Guide, Chapter 8 – Linking SSN/EINs to Determine Breakpoint Eligibility

**Original File:** [fs_techguide_ch8_mfs356_20240117.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_techguide_ch8_mfs356_20240117.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 7  
**File Size:** 295.9 KB  

---

## Page 1

 
 
 
FUND/SERV® 
TECHNICAL GUIDE, CHAPTER 8 – LINKING 
SSN/EINS TO DETERMINE BREAKPOINT 
ELIGIBILITY 
JANUARY 17, 2024 
 
 

---

## Page 2

 
 
CHANGE HISTORY 
01/17/2024 This document is updated with 2024 branding.  Content reviewed.  
05/03/2021 Learning upgrade caused some link(s) to break.  Links have been corrected. 
04/01/2021 Document rebranded. 
07/10/2020 Broken links corrected. 
  

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 4 
How the FUND/SERV System Relates to Additional SSN/EIN Information......................................................... 4 
Best Practices ....................................................................................................................................................... 5 
Flowchart .............................................................................................................................................................. 6 
 

---

## Page 4

Technical Guide, Chapter 8 – Linking SSN/EINs to Determine Breakpoint Eligibility 
Introduction 4 
INTRODUCTION 
Note: 
This User Guide was written by the Client Data Share (CDS) sub-committee of the Investment Company Institute (ICI) 
[[Broker]] / Dealer Advisory Committee (BDAC). It addresses the modifications made to the various National [[securities]] 
Clearing Corporation's ([[NSCC]]) mutual fund application(s) in order to comply with the Joint NASC / Industry Task Force on 
Breakpoints, specifically, Recommendation L. 
This guide has been designed to provide Fund/SERV processing requirements as it relates to pricing trades  
(via linking up to 99 additional Social Security Numbers (SSN) or Employer Identification Numbers (EIN)) on 
front- load purchases and exchanges and thereby having information necessary to calculate correct 
breakpoints). 
This document assumes users have a working knowledge of how Fund/SERV works today. When you have 
finished reviewing the User Guide you should have a better understanding of the: 
• Business reasons for providing additional SSN/EIN information on front-end load purchases and 
exchanges. 
• Fund/SERV requirements necessary for processing trades with the additional SSN/EIN information. 
• “Best practice” guidelines and the role of each [[participant]]. 
• Changes to the record layouts for processing trades with additional SSN/EIN information. 
• Flow Charts 
Please reference Fund/SERV® Technical Guides on the Learning Center.  
All other Fund/SERV documents can be found on Learning under the Fund/SERV Resources section 
https://dtcclearning.com/products-and-services/mutual-fund-services/fund-serv.html#resources.  
Fund/SERV Record Layouts are available on the Learning Center at https://dtcclearning.com/products -and-
services/mutual-fund-services/fund-serv.html#Fund/SERV%3Csup%3E%C2%AE%3C/sup%3E -Record-
Layouts. 
For more information, please call your Relationship Manager or Wealth Management Services at 212-855-
8877. 
How the FUND/SERV System Relates to Additional SSN/EIN 
Information 
Fund/SERV provides the following benefits to participants: 
• Centralized mutual fund order entry, confirmation, registration, and net [[settlement]] via [[NSCC]]. 
• Increased volume capacity for [[Mutual Funds]] and firms, enabling them to expand along with the industry. 
• Simplified [[settlement]] process by calculating a net money [[settlement]] figure for each [[participant]] every day. 
• The support of multiple [[settlement]] cycles, including same-day [[settlement]]. 
• The accommodation of various processing capabilities, including single-batch, multi-batch, and interactive 
communications. 
• The support of complex, high-volume processing needs associated with accounts that are transferred. 
• The potential for cost savings to participants through economies of scale. 
• Flexible operating procedures and diversity of products. 
• State of the art technology platforms. 

---

## Page 5

Technical Guide, Chapter 8 – Linking SSN/EINs to Determine Breakpoint Eligibility 
Best Practices 5 
BEST PRACTICES 
The best practices guidelines will: 
1. Provide standard, electronic functionality allowing firms to communicate to funds, all related or associated 
SSN/EIN's to be grouped or linked together for the purpose of determining breakpoint eligibility.  
2. Allow the fund an enhanced ability to properly identify and include related accounts where appropriate to 
determine breakpoint discount eligibility. 
Funds will link accounts based on the data from the SSN/EIN data fields of Record layouts for Orders (001), 
As-of Orders (004), Exchanges (015) and Corrections (003). Each fund company is in the best position to know 
and apply their prospectus linkage rules. 
If additional SSN/EIN's are submitted the "SSN/EIN Start Sequence Number" and the "Total SSN/EIN 
Records" fields will be required to indicate the SSN/EIN Suffix record will be included with the Orders (001), As -
of Orders (004), Exchanges (015) and Corrections (003) records. 
• The SSN/EIN Start Sequence Number will indicate the logical sequence number of the first  SSN/EIN 
record. 
• The Total SSN/EIN records field indicates the total SSN/EIN Records submitted.  
 
The SSN/EIN Suffix record allows for the reporting of additional SSN/EIN's up to 99 in total (up to 11 
SSN/EIN's can be submitted on each SSN/EIN Suffix record), Fund/SERV® Record Layouts and additional 
related information can be found within the learning center in the Fund/SERV section 
https://dtcclearning.com/products-and-services/mutual-fund-services/fund-serv.html#overview. 
 

---

## Page 6

Technical Guide, Chapter 8 – Linking SSN/EINs to Determine Breakpoint Eligibility 
Flowchart 6 
FLOWCHART 
  


---

## Page 7

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: January 17, 2024 
Publication Code: MFS356 
Service: FUND/SERV 
Title: Technical Guide, Chapter 8 – Linking SSN/EINs to Determine Breakpoint Eligibility 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 
 