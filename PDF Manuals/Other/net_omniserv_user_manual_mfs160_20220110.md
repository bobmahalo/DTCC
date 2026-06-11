---
title: "Omni/SERV® User Manual"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_omniserv_user_manual_mfs160_20220110.pdf"
pages: 9
size: "292.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Omni/SERV® User Manual

**Original File:** [net_omniserv_user_manual_mfs160_20220110.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_omniserv_user_manual_mfs160_20220110.pdf)  
**Category:** Other  
**Total Pages:** 9  
**File Size:** 292.9 KB  

---

## Page 1

 
 
 
NETWORKING - OMNI/SERV® 
OMNI/SERV USER MANUAL 
JANUARY 10, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: January 10, 2022 
Publication Code: MFS160 
Service: Networking – Omni/SERV
® 
Title: Omni/SERV® User Manual 
 
  

---

## Page 3

 
 
CHANGE HISTORY 
Date Description 
01/10/2022 Links updated due to launch of redesigned learning center. 
07/14/2020 Broken links corrected. 
  
 
 

---

## Page 4

 
 
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 5 
Introduction ......................................................................................................................................................... 5 
Omnibus Processing ......................................................................................................................................... 5 
About the Omnibus Processing Enhancements ............................................................................................... 6 
Omnibus Activity File .......................................................................................................................................... 6 
Omnibus Position File ......................................................................................................................................... 6 
DataTrak and Autoroute [[ID]] and Transmission Schedules for Omni/SERV Activity and Position Files ............. 6 
Documentation .................................................................................................................................................... 7 
Frequently Asked Questions .............................................................................................................................. 8 
 

---

## Page 5

Omni/SERV User Manual 
Overview 5 
OVERVIEW 
Introduction 
Omnibus Processing 
Omnibus processing allows the accounts and transactions of multiple shareholder accounts to be combined 
under the name of a financial [[intermediary]]. To provide transparency of the underlying shareowners’ holdings, 
firms send omnibus activity (DSA) and omnibus position (DSP) files directly to the funds. 
Networking services have been enhanced to provide a pass-through service, called Omni/SERV®. This service 
provides a central location where participating firms can transmit their Omnibus Activity files and Omnibus 
Position files for funds that elect to use Omni/SERV® to obtain their files. These Omnibus files replicate the 
layouts of the DSA and DSP. It is recommended that the participating fund and firm agree upon the data 
elements that must be supplied to support their relationship. 
• Omnibus Activity File. This file allows firms to transmit sub accounting client activity through [[DTCC]] to 
fund [[Companies]]. 
• Omnibus Position File. This file allows firms to transmit sub accounting client positions through [[DTCC]] to 
fund [[Companies]]. 
 
Please note: 
[[NSCC]] only validates the required fields of the Omnibus Activity and Omnibus Position Header and Trailer. [[NSCC]] does not 
validate the Omnibus Activity or Omnibus Position Detail records. 

---

## Page 6

Omni/SERV User Manual 
About the Omnibus Processing Enhancements 6 
ABOUT THE OMNIBUS PROCESSING ENHANCEMENTS 
Omnibus Activity File 
Firms use the Omnibus Activity File to transmit their sub accounting client activity file through [[NSCC]] to fund 
[[Companies]]. 
Omnibus Activity File record layouts (Password required) are located on the Learning Center in the 
Omni/SERV section under Record Layout: https://dtcclearning.com/products-and-services/mutual-fund-
services/omni-serv.html#Record-Layouts 
Please note:  
[[NSCC]] only validates the required fields of the Omnibus Activity Header and Trailer. [[NSCC]] does not validate the Omnibus 
Activity Detail records. 
Omnibus Position File 
Firms use the Omnibus Position File to transmit their sub accounting client position file through [[NSCC]] to fund 
[[Companies]]. 
Omnibus Position file record layouts (Password required) are located on the Learning Center in the 
Omni/SERV section under Record Layout: https://dtcclearning.com/products-and-services/mutual-fund-
services/omni-serv.html#Record-Layouts 
Please note:  
[[NSCC]] only validates the required fields of the Omnibus Position Header and Trailer. [[NSCC]] does not validate the Omnibus 
Position Detail records. 
DataTrak and Autoroute [[ID]] and Transmission Schedules for 
Omni/SERV Activity and Position Files 
The SYSIDs and transmission cycle timeframes are available on the Networking & Omni/SERV Transmission 
Schedules.  This transmission schedule can be located on the Learning Center in the Mutual Fund Schedules 
section https://dtcclearning.com/products-and-services/mutual-fund-services/schedules.html 
Please note:  
The MRO process will begin immediately after the Edit process is complete, therefore the Output distribution may occur 
earlier than specified in the schedule. 
Please contact your WMS Relationship Manager to coordinate access to the DataTrak SYSIDs and the 
Autoroute IDs. 
 

---

## Page 7

Omni/SERV User Manual 
About the Omnibus Processing Enhancements 7 
Documentation 
The Networking record layouts and Networking Technical Guide are available on the Learning Center at 
https://dtcclearning.com/products-and-services/mutual-fund-services/networking.html#resources 
Any questions regarding these files can be directed to your Relationship Manager or Account Management 
Team at (212) 855-8877. 

---

## Page 8

Omni/SERV User Manual 
Frequently Asked Questions 8 
FREQUENTLY ASKED QUESTIONS 
Q: Does [[DTCC]] currently support the transmission of Omni/SERV® Transparency files through other 
transmission methods? 
A: [[DTCC]] currently supports mainframe-to-mainframe transmission methods. However, [[DTCC]] is 
researching the feasibility of FTPS transmission methodology for future releases. 
 
Q: How does a participating fund arrange to obtain a current day file not received (1) before the final MRO 
cycle time for the current day? (2) After the final MRO cycle time for the current day? 
A: Clients should contact their relationship manager to request a retransmission for any current day file 
not received before or after the final MRO cycle time. 
 
Q: How does a participating fund arrange to obtain a file for a date in the past (1) before the final MRO 
cycle time for the current day? (2) After the final MRO cycle time for the current day? 
A: [[DTCC]] can retransmit files for dates up to two weeks in the past upon request from the [[participant]]. 
Clients should contact their relationship manager to request a retransmission. 
 
 

---

## Page 9

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 