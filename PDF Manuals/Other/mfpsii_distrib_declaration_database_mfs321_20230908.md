---
title: "MFPS II-Distribution Declaration Database"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfpsii_distrib_declaration_database_mfs321_20230908.pdf"
pages: 13
size: "779.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II-Distribution Declaration Database

**Original File:** [mfpsii_distrib_declaration_database_mfs321_20230908.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfpsii_distrib_declaration_database_mfs321_20230908.pdf)  
**Category:** Other  
**Total Pages:** 13  
**File Size:** 779.8 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service II 
MFPS II - DISTRIBUTION DECLARATION 
DATABASE 
SEPTEMBER 8, 2023 
 

---

## Page 2

MFPS II - Distribution Declaration Database 
Introduction 2 
CHANGE HISTORY 
 
Dates Changes 
September 8, 2023 • Document rebranded and reviewed.  
• Screenshots updated 
Changes effective 05/01/2023 See Important Notice a9279 dated 3/21/23  
 
Removed reference to the [[participant]] Database as it was decommissioned. 
07/15/2020 Broken links corrected 
Changes effective 02/29/2016 See Important Notice a8107, dated 10/27/2015 
Changes to Ex date fields on 041 & 042 records. Also removed the references to 
the cycle Changes implemented July 2012 (in “For Distribution Declaration 
Database only” section) 
Changes effective 07/23/2012 See Important Notice a7412, dated 04/20/2012 
20 Cycles added to Mutual Fund Profile Service II Distribution Declaration 
Transmission Schedule. 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 4 
MFPS II - Distribution Declaration Database ..................................................................................................... 5 
Common Terms and Definitions ......................................................................................................................... 5 
Record Types ...................................................................................................................................................... 6 
Retention of Data ................................................................................................................................................ 7 
Distribution Database Process Flow Example .................................................................................................... 7 
User File Request Processing ............................................................................................................................ 8 
Input .................................................................................................................................................................... 8 
Output ................................................................................................................................................................. 8 
User File Request Example – 080 Record ......................................................................................................... 8 
User File Request Example - MyDTCC Web Portal ........................................................................................... 9 
MyDTCC – MFPS II Distribution Declaration Database Web Screens ............................................................10 
 

---

## Page 4

MFPS II - Distribution Declaration Database 
Introduction 4 
INTRODUCTION 
In 1996, [[NSCC]] developed and implemented MFPS I to provide a systematic and standardized solution for 
funds to provide Daily Price and Rate information.  MFPS I replaced the highly manual and error prone process 
of providing this time-sensitive information through paper transmittals, faxes, and phone calls.  
To build on the efficiencies gained through MFPS I, the financial services industry sought a standardized and 
automated process to transmit a richer set of mutual fund distribution information, which was achieved through 
the introduction of the MFPS II - Distribution Declaration Database, which implemented in 1998. 

---

## Page 5

MFPS II - Distribution Declaration Database 
MFPS II - Distribution Declaration Database 5 
MFPS II - DISTRIBUTION DECLARATION DATABASE 
This database includes projected and actual information submitted by Fund clients, such as: record date, Ex -
date, reinvest date and payable date for dividends, and capital gains distributions. It can also include 12b- 1 
rates and other fund payout information. Only Funds can submit information to the Distribution Declaration 
database. 
Common Terms and Definitions 
Term Definition 
Distribution 
Declaration 
12b-1 
Cost (fee) incurred by a fund for a firm’s professional services (that is, maintaining mutual fund account 
assets).   
(12b-1 information is provided through record type 040) 
Distribution 
Declaration 
[[Dividend]] 
Distribution Declaration [[Dividend]]: Earnings (profits) on assets held by a shareholder and distributed 
periodically.  
([[Dividend]] information is provided through record type 042) 
Distribution 
Declaration 
Cap Gains 
Amount of profit (loss) paid on a security. The profit or loss can be long term, short term, or mid-term. The 
length of the loss depends on the length of time which the [[Asset]] is held (length of time between purchase 
and selling of [[shares]]). 
(Capital Gain information is provided through record type 041) 
Distribution 
Declaration 
General 
Earnings 
Distribution declaration general earning information refers to earnings and taxation other than local 
municipal or state, such as: US [[obligations]] or foreign taxes paid. Income ($) from or value of mutual fund 
[[shares]]. Classification of earnings can be either retained or current. Retained earnings reflect the net 
profits after payment of dividends.  
(General Earnings is provided through record type 043) 
Distribution 
Declaration 
Municipal 
Earnings 
Distribution declaration municipal earnings refers to earnings attributable to a specific state. [[NSCC]] 
creates one segment per state and earning type. Income (interest paid) on municipal [[Bonds]] issued by a 
state or local government. The federal government and the jurisdiction that issued the bond [[DO]] not usually 
tax the earnings 
(Municipal Earnings is provided through record type 044) 
User File 
Request   
(080 Record) 
Client requests information by submitting a User File Request. The system uses this request to extract the 
information from the database and deliver to the client.  
(User File Requests can be submitted through the MFPS II 080 record, or the MyDTCC web portal). 
 
 
 

---

## Page 6

MFPS II - Distribution Declaration Database 
MFPS II - Distribution Declaration Database 6 
Record Types 
The following Record Types make up the MFPS II - Distribution Declaration Database. These records are 
submitted by fund clients and out is distributed to firms. 
• Distribution Declaration 12b-1–Record type 040 
• Distribution Declaration Capital Gains–Record type 041 
• Distribution Declaration [[Dividend]]–Record type 042 
• Distribution Declaration General Earnings-Record type 043 
• Distribution Declaration Municipal Earnings Record type 044 
 
You can find the record layouts on the Learning Center under https://dtcclearning.com/products-and-
services/mutual-fund-services.html.   
Distribution Declaration database Input/Output is multi-cycle and consists of the following SYS IDs and 
Autoroutes: 
Input – Datatrak SYS IDs Output – Autoroutes and output included   
Fund submits distribution information 
through the following SYS IDs: 
26191 (fixed) 
26192 (variable) 
User File Requests (080) are also 
submitted through these SYS IDs. 
 
02110826 (MFPS II Global Distribution): 
• Firms receive all output for updates, changes, and deletes  
 
02110827 (MFPS II Specific Distribution): 
• User File Request output  
• Fund receives rejects on their input (with the exclusion of the 
rejects mentioned in 02110823 below) 
 
02110823 (MFPS II Specific Rejects): 
• Funds receive rejects on their input if the ‘Profile Type’ field in a 
MFPS II input record contains an invalid or blank value. 
Note 
Funds can also view rejects via MyDTCC if they are setup to receive the MFPS II Reject Report – autoroute 02110901 
(web only). Contact your WMS Relationship Manager or Wealth Management Services at 212-855-8877 for more 
information. 
[[NSCC]] processes the information in accordance with the input/output cycles posted in the MFPS Transmission 
Schedules. The transmission schedule is located on the [[DTCC]] Learning Center under 
https://dtcclearning.com/products-and-services/mutual-fund-services.html.   
For additional information on processing distribution information through the MFPS II – Distribution Declaration 
Database, please see the ‘Best Practices – [[Dividend]] and Capital Gain Distributions’ document located in the 
[[DTCC]] Learning Center under https://dtcclearning.com/products-and-services/mutual-fund-services.html.   

---

## Page 7

MFPS II - Distribution Declaration Database 
MFPS II - Distribution Declaration Database 7 
Retention of Data 
[[NSCC]] maintains historical data within the MFPS II – Distribution Declaration Database for a specified period of 
five years.  
Distribution Database Process Flow Example 
Fund submits to [[NSCC]] a 12b-1 Declaration Distribution "Add" for Security Issue [[ID]] 123456789. 
 
Steps 
1. On any business day, Fund submits a 12b-1 Declaration Distribution Add request for Security Issue [[ID]] 
123456789 to [[NSCC]]. 
2. [[NSCC]] stores the declaration of the Security Issue [[ID]] 123456789 in the current database.  
3. [[NSCC]] distributes the output in the next output cycle. 
 
 
 
 
 
 


---

## Page 8

MFPS II - Distribution Declaration Database 
User File Request Processing 8 
USER FILE REQUEST PROCESSING 
Input 
A Firm or a Fund can submit a User File Request record to obtain information stored in the MFPS II -  
Distribution Declaration database.  A User File Request can be submitted through the 080 User File Request 
Fixed or Variable record or via the MyDTCC web portal.  All User File Request system processing includes an 
initial check to verify that the originator is a valid MFPS II client. 
Output 
Only [[NSCC]] clients that are set up on the MFPS Master file will be able to receive User File Request output.  
[[NSCC]] distributes the output to the clients’ destination (batch or web) as indicated below:  
1. The 8:30 PM output cycle includes all data received by [[NSCC]] up to 8:15 PM and then, 
2. The cumulative 10:30 PM ET output cycle includes all data received by [[NSCC]] up to 10:15 PM ET.  
User File Request Example – 080 Record 
Fund A participates in the MFPS II – Distribution Declaration Database.  A firm submits a User File Request by 
submitting record 080 (User File Request) and populating the ‘Requested Profile Type Value’ field with a value 
of 03 = Distribution Database.  
 
 


---

## Page 9

MFPS II - Distribution Declaration Database 
User File Request Processing 9 
User File Request Example - MyDTCC Web Portal 
A User File Request can also be submitted through the MyDTCC web portal by selecting the ‘User File 
Request’ menu [[Option]] under the MFPS II - Distribution Declaration Database menu item and populating the 
‘Requested Profile Type Value’ field with a ‘03 = Distribution Database’.  
 
 
 
 
 
 
 
  


---

## Page 10

MFPS II - Distribution Declaration Database 
User File Request Processing 10 
MyDTCC – MFPS II Distribution Declaration Database Web Screens 
 
High Level Screen Tour of Web Screens 
 
Figure 1: MFPS II - Distribution Declaration Menu 
 
 
 
Figure 2: MFPS II - Distribution Declaration 12b-1 
 
 
 
 
 
 


---

## Page 11

MFPS II - Distribution Declaration Database 
User File Request Processing 11 
Figure 3: MFPS II - Distribution Declaration Capital Gain 
 
 
 
Figure 4: MFPS II - Distribution Declaration Dividends 
 
 
 
Figure 5: MFPS II - Distribution Declaration General Earnings  
 


---

## Page 12

MFPS II - Distribution Declaration Database 
User File Request Processing 12 
 
Figure 6: MFPS II Distribution Declaration Municipal Earnings  
 


---

## Page 13

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 8, 2023 
Publication Code: MFS321 
Service: Mutual Fund Profile Service II 
Title: MFPS II-Distribution Declaration Database 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
  