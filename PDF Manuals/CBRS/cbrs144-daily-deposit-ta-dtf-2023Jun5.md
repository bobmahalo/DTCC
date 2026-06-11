---
title: "CBRS Daily Deposit Transfer Agent File for Data Transmission Facility (DTF)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs144-daily-deposit-ta-dtf-2023Jun5.pdf"
pages: 4
size: "245.6 KB"
category: "CBRS"
ingested_on: "2026-06-05"
---

# CBRS Daily Deposit Transfer Agent File for Data Transmission Facility (DTF)

**Original File:** [cbrs144-daily-deposit-ta-dtf-2023Jun5.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs144-daily-deposit-ta-dtf-2023Jun5.pdf)  
**Category:** CBRS  
**Total Pages:** 4  
**File Size:** 245.6 KB  

---

## Page 1

 
 
 
 
COST BASIS REPORTING SERVICE 
CBRS DAILY DEPOSIT [[transfer agent]] FILE FOR DATA TRANSMISSION 
FACILITY (DTF) 
MAY 5, 2022 
 


---

## Page 2

CBRS Daily Deposit [[transfer agent]] File for Data Transmission Facility (DTF) 
Data Transmission Facility (DTF) – DPCBRS 2 
DATA TRANSMISSION FACILITY (DTF) – DPCBRS 
File format #1 – 200 bytes - retrieval through the Data Transmission Facility (DTF) function – DPCBRS. This 
file has two record types – one for the deposit record and another for the certificate record. Each deposit record 
can be followed with anywhere from 1 to 99 certificate records. 
Record Type 01 – Deposit Record 
CBRS Daily Deposit [[transfer agent]] File for  Data Transmission Facility (DTF) – DPCBRS 
Record Type – Deposit Record 
Record Length: 200 
Field Name Type Description Required 
(Y/N) 
CBRS Signon 8 bytes alphanumeric [[DTCC]] CBRS sign on corresponding to the Transfer 
Agent Number. 
Y 
[[transfer agent]] 
Number 
8 bytes alphanumeric [[DTCC]] [[transfer agent]] number from the [[securities]] 
Transfer Processing (STP) database.  
Y 
M/N Sign-on 8 bytes alphanumeric [[DTCC]] [[transfer agent]] identifier used to send and receive 
files through DTF.  
N 
Record Type 2 bytes alphanumeric 01 – Deposit record type. Y 
[[CUSIP]] [[ID]] 12 bytes alphanumeric [[CUSIP]] identified with the deposit. Y 
[[CUSIP]] 
Description 
20 bytes alphanumeric [[CUSIP]] description from the Master File – [[CUSIP]] (MFC) 
database. 
Y 
SCL Type 3 bytes alphanumeric Shipment Control List (SCL) type from the STP system. Y 
SCL [[ID]] 16 bytes alphanumeric SCL [[ID]] from the STP system. Y 
SCL Page 
Number 
2 bytes alphanumeric SCL page number. Y 
SCL Line Item 
Number 
3 bytes alphanumeric SCL line item number. Y 
[[participant]] 
Number 
8 bytes alphanumeric [[participant]] number for the deposit. Y 
[[participant]] Name 20 bytes alphanumeric [[participant]] name from the master tables. Y 
Unique [[ID]] 26 bytes alphanumeric Unique [[ID]] associated with the transaction: 
Julian Date (3 characters: DDD) + [[participant]] Number 
(5 characters) + Reference [[ID]] Number (up  to 18 
characters). 
Y 
Deposit Quantity 18 bytes alphanumeric Deposit quantity.  
9(13)v9(05) 
Y 

---

## Page 3

CBRS Daily Deposit [[transfer agent]] File for Data Transmission Facility (DTF) 
Data Transmission Facility (DTF) – DPCBRS 3 
CBRS Daily Deposit [[transfer agent]] File for  Data Transmission Facility (DTF) – DPCBRS 
Record Type – Deposit Record 
Record Length: 200 
Field Name Type Description Required 
(Y/N) 
Certificate Count 3 bytes alphanumeric Number of certificates in the deposit. Y 
Filler 43 bytes alphanumeric For future use. Y 
Record Type 02 – Certificate Record 
CBRS Daily Deposit [[transfer agent]] File for Data Transmission Facility (DTF) – DPCBRS 
Record Type 02 – Certificate Record 
Record Length: 200 
Field Name  Type Description  Required 
(Y/N) 
CBRS Sign On 8 bytes alphanumeric [[DTCC]] CBRS sign on corresponding to the [[transfer agent]] 
number. 
Y 
[[transfer agent]] 
Number 
8 bytes alphanumeric [[DTCC]] [[transfer agent]] number from STP database. Y 
M/N Sign On 8 bytes alphanumeric [[DTCC]] [[transfer agent]] identifier used to send and receive  
files through DTF. 
N 
Record Type 2 bytes alphanumeric 02 – Certificate record type. Y 
Certificate 
Number 
12 bytes alphanumeric Certificate number. Y 
Certificate 
Quantity 
16 bytes numeric  Certificate quantity. 
9(11)v9(05) 
Y 
Certificate 
Registration 
30 bytes alphanumeric Certificate first line of registration. Y 
Filler 116 bytes alphanumeric For future use.  
 
 

---

## Page 4

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: May 19, 2023 
Publication Code: CBRS144 
Service: Cost Basis Reporting Service (CBRS) 
Title: CBRS Daily Deposit [[transfer agent]] File for Data Transmission Facility (DTF) 
 
 
 
 
Recipient acknowledges that the CBRS Record Layouts ("Information") provided herein are the property of The Depository 
Trust & Clearing Corporation and/or subsidiaries (collectively, "[[DTCC]]"). Recipient agrees to protect the proprietary position 
of [[DTCC]], and further agrees that without [[DTCC]]'s prior written consent, Recipient shall not publish, transfer or sell such 
Information or copies thereof, or any extracts or any of the Information therefrom in any form, or summaries thereof, to any 
other person or organization, or permit any other person or organization to use or distribute such Information, including 
clients of a recipient, who, to a Recipient's knowledge, provides the Information to an entity that does so; provided, 
however, that this restriction shall not be deemed to prohibit the use of the Information by Recipient for its internal purposes 
in the ordinary course of clearing and settling its [[securities]] transactions through [[DTCC]]. 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 