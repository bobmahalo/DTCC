---
title: "CBRS Daily Deposit Transfer Agent File for Web Output - AutoRoute Production ID: 02401649 / PSE 02981649"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs145-daily-deposit-ta-web-02401649-2023Jun5.pdf"
pages: 4
size: "300.3 KB"
category: "CBRS"
ingested_on: "2026-06-05"
---

# CBRS Daily Deposit Transfer Agent File for Web Output - AutoRoute Production ID: 02401649 / PSE 02981649

**Original File:** [cbrs145-daily-deposit-ta-web-02401649-2023Jun5.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs145-daily-deposit-ta-web-02401649-2023Jun5.pdf)  
**Category:** CBRS  
**Total Pages:** 4  
**File Size:** 300.3 KB  

---

## Page 1

COST BASIS REPORTING SERVICE
CBRS DAILY DEPOSIT WEB OUTPUT FILE FOR TRANSFER AGENTS – 
AUTOROUTE PRODUCTION [[ID]]: 02401649 / PSE 02981649 
MAY 5, 2022 


---

## Page 2

CBRS Daily Deposit WEb Output File for Transfer Agents – AutoRoute Production [[ID]]: 02401649 / PSE 02981649 
CBRS Daily Deposit For Transfer Agents 2 
CBRS DAILY DEPOSIT FOR TRANSFER AGENTS 
File format #2 – 300 bytes - retrieval through the CBRS Web Output Files page. This file has one record type. 
Each record contains both the deposit level information and the certificate information. For example, if a single 
deposit contains three certificates, there are three records each having the same deposit information (but 
different certificate information).  
Field Name Type Description Required 
(Y/N) 
CBRS Sign On 8 bytes alphanumeric [[DTCC]] CBRS sign on corresponding to the Transfer 
Agent Number. 
Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
[[transfer agent]] 
number 
8 bytes alphanumeric [[DTCC]] [[transfer agent]] number from [[securities]] 
Transfer Processing (STP) database. 
Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
M/N Transfer 
Agent Number 
8 bytes alphanumeric M/N [[transfer agent]] number from INFO database. N 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
[[CUSIP]] [[ID]] 12 bytes alphanumeric [[CUSIP]] identified with the deposit. Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
[[CUSIP]] 
Description 
20 bytes alphanumeric [[CUSIP]] description from Master File – [[CUSIP]] (MFC) 
database. 
Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
SCL Type 3 bytes alphanumeric Shipment Control List (SCL) type from STP 
system. 
Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
SCL [[ID]] 16 bytes alphanumeric SCL [[ID]] from STP system. Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
SCL Page 
Number 
2 bytes alphanumeric SCL page number. Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
SCL Line Item 
Number 
3 bytes alphanumeric SCL line number. Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
[[participant]] 
Number 
8 bytes alphanumeric [[participant]] number for the deposit. Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 

---

## Page 3

CBRS Daily Deposit WEb Output File for Transfer Agents – AutoRoute Production [[ID]]: 02401649 / PSE 02981649 
CBRS Daily Deposit For Transfer Agents 3 
Field Name Type Description Required 
(Y/N) 
[[participant]] 
Name 
20 bytes alphanumeric [[participant]] name from STP database. Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
Unique [[ID]] 26 bytes numeric Unique [[ID]] associated with the transaction: Julian 
Date (3 characters: DDD) + [[participant]] Number 
(5 characters) + Reference [[ID]] Number (up to 18 
characters). 
Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
Deposit 
Quantity 
19 bytes numeric Deposit quantity. 
9(13).9(5) 
Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
Certificate 
Count 
3 bytes numeric Number of certificates in the deposit. Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
Certificate 
Number 
12 bytes alphanumeric Certificate number. Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
Certificate 
Quantity 
17 bytes alphanumeric Deposit quantity. 
9(13).9(5) 
Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
Certificate 
Registration 
30 bytes alphanumeric Certificate first line of registration. Y 
Filler 1 byte alphanumeric Comma (,) delimiter. Y 
Filler 68 bytes alphanumeric Comma (,) delimiter. Y 

---

## Page 4

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
Doc Date: June 5, 2023 
Publication Code: CBRS145 
Service: Cost Basis Reporting Service (CBRS) 
Title: CBRS Daily Deposit Web Output File for Transfer Agents – AutoRoute Production [[ID]]: 02401649 / PSE 02981649 
Recipient acknowledges that the CBRS Record Layouts ("Information") provided herein are the property of The Depository 
Trust & Clearing Corporation and/or subsidiaries (collectively, "[[DTCC]]"). Recipient agrees to protect the proprietary position 
of [[DTCC]], and further agrees that without [[DTCC]]'s prior written consent, Recipient shall not publish, transfer or sell such 
Information or copies thereof, or any extracts or any of the Information therefrom in any form, or summaries thereof, to any 
other person or organization, or permit any other person or organization to use or distribute such Information, including 
clients of a recipient, who, to a Recipient's knowledge, provides the Information to an entity that does so; provided, 
however, that this restriction shall not be deemed to prohibit the use of the Information by Recipient for its internal purposes 
in the ordinary course of clearing and settling its [[securities]] transactions through [[DTCC]]. 
FOR MORE INFORMATION 
E
mail [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 