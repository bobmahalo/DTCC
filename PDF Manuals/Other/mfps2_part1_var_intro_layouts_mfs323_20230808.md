---
title: "MFSPS II - Introduction to Variable Length Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part1_var_intro_layouts_mfs323_20230808.pdf"
pages: 13
size: "259.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFSPS II - Introduction to Variable Length Record Layouts

**Original File:** [mfps2_part1_var_intro_layouts_mfs323_20230808.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part1_var_intro_layouts_mfs323_20230808.pdf)  
**Category:** Other  
**Total Pages:** 13  
**File Size:** 259.7 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service II 
INTRODUCTION TO VARIABLE LENGTH RECORD 
LAYOUTS – PART 1 
 
AUGUST 8, 2023 
 

---

## Page 2

Introduction To Variable Length Record Layouts – Part 1 
Introduction 2 
 
HISTORY OF CHANGES 
Dates Description 
August 8, 2023 Record was rebranded and reviewed.  
Effective Date: May 1, 2023 MFSP2 [[participant]] database was decommissioned.  
Please See Important Notice a9279 P&S 8852 
Dated March 21, 2023 
July 8, 2022 Record was rebranded and reviewed. 
Effective Date: March 25, 2019 Please see Important Notice: a8658 P&S 8233 
Dated December 19, 2018 
Effective Date: March 27, 2006 Please see Important Notice: a6171 P&S 5741  
Dated December 21, 2005 
Effective Date: November 14, 2005 Please see Important Notice: a6084 P&S 5654  
Dated August 10, 2005 
Effective Date: August 29, 2005 Please see Important Notice a6062 P&S 5632  
Dated July 6, 2005 
 

---

## Page 3

Introduction To Variable Length Record Layouts – Part 1 
Introduction 3 
 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 4 
Variable Length Format ....................................................................................................................................... 5 
Recipient Number................................................................................................................................................. 6 
Record Length ...................................................................................................................................................... 7 
Key Data ................................................................................................................................................................ 8 
Replace Rules ....................................................................................................................................................... 9 
Delete Rules ........................................................................................................................................................ 10 
Record Layouts .................................................................................................................................................. 11 
 
 

---

## Page 4

Introduction To Variable Length Record Layouts – Part 1 
Introduction 4 
 
INTRODUCTION 
Some of the features of the Mutual Fund Profile Service (MFPS) [[NSCC]] (non-ISO) record layouts are: 
1. Records can be received in either of two formats: fixed length or variable length.  
2. This document describes the MFPS [[NSCC]] (non-ISO) variable length record layouts. 
3. Only [[NSCC]] rejected transactions are being returned by [[NSCC]] to the originating [[participant]]. Accepted 
transactions are being sent to the [[participant]] only. 
4. When rejecting a transaction for more than one reason, MFPS reports multiple rejects codes via record 
type 120 (see section 02.29) which follows the rejected transaction back to the originating [[participant]].  

---

## Page 5

Introduction To Variable Length Record Layouts – Part 1 
Variable Length Format 5 
 
VARIABLE LENGTH FORMAT 
Each variable length transaction is one record. Bytes 1-10 are control information which consist of the following 
fields: 
1. Record Length (bytes 1-4) 
2. Physical Sequence Number (bytes 5-6) 
3. Logical Sequence Number (bytes 7-8) 
4. Filler (for future use) (byte 9) 
5. Reminder Indicator (output only) (byte 10) 
 
Every section of 74 bytes thereafter is identical to bytes 7 through 80 of the respective 80- byte fixed length 
record. 

---

## Page 6

Introduction To Variable Length Record Layouts – Part 1 
Recipient Number 6 
 
RECIPIENT NUMBER 
In MFPS, the Recipient Number field is used to direct the output to the proper recipient(s). When the Recipient 
Number is left blank, the output is considered global and is sent globally. 
By supplying a Recipient Number, the originator can send specific data to specific recipients.  

---

## Page 7

Introduction To Variable Length Record Layouts – Part 1 
Record Length 7 
 
RECORD LENGTH 
The lowest value specified in the Record Length field does not apply if Action Code = ‘D’.  

---

## Page 8

Introduction To Variable Length Record Layouts – Part 1 
Key Data 8 
 
KEY DATA 
In order to apply any updates to the MFPS data stores key information must be supplied with the transaction.  
Key fields are identified in the record layouts by a '@' or a '@@'. 
Fields marked with ‘@’ must be present at all times for every sub-type of the transaction. 
For the key fields marked with ‘@@’ – only one of them should be present. 

---

## Page 9

Introduction To Variable Length Record Layouts – Part 1 
Replace Rules 9 
 
REPLACE RULES 
When a transaction is received with Action Type = C, the new data replaces the existing information in its 
entirety. 

---

## Page 10

Introduction To Variable Length Record Layouts – Part 1 
Delete Rules 10 
 
DELETE RULES 
When Action code = ‘D’, only the key information should be supplied. 

---

## Page 11

Introduction To Variable Length Record Layouts – Part 1 
Record Layouts 11 
 
RECORD LAYOUTS 
The following record types will be used by MFPS: 
000 –  [[NSCC]] Output Header 
020 – Security Issue General Profile 
021 – Security Blue Sky 
022 – Security CDSC Information 
023 – Security Breakpoint Schedules 
024 – Security Commission 
025 – [[NSCC]] Social Code Eligibility  
026 – Short Term Redemption Data 
027 – Fund/SERV Security Master File 
029 – Security Issue Breakpoint Linkage Rules 
040 – Distribution Declaration 12b-1 
041 – Distribution Declaration Cap Gains 
042 – Distribution Declaration [[Dividend]] 
043 – Distribution Declaration General Earnings 
044 – Distribution Declaration Municipal Earnings 
080 – User File Request 
120 – Multiple Reject Codes 
999 – Trailer 
 
The column headings in this document are as follows: 
Start - The position where the field starts. 
End - The position where the field ends. 
Len - The length of the field in bytes 
Type 
- The type of the field: 
A/N = Alphanumeric  
N = Numeric  
Field Name - The name of the field. 

---

## Page 12

Introduction To Variable Length Record Layouts – Part 1 
Record Layouts 12 
 
Description - Field description (format, valid values, conditional requirements, etc.). 
Opt/Req 
- Indicates whether the field is optional or required: 
O = Optional 
R = Required 
OC = Generally optional, but required upon specified conditions 
RC = Generally required, but optional upon specified conditions  
Reject Code - The reject code which indicates that this field is invalid.  
 
Notes: 
• Alphanumeric type fields may include any character in the computer character set but should not include unprintable 
characters such as Low-Value, High-Value, Comp-3 fields, etc., since these kinds of characters may cause problems 
during transmission time. 
• Numeric type fields may include digits (0-9) only. 
• Required fields mean the following: 
a. Fields with specified list of values must have one of those values. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above 
but must not be spaces. 
c. Numeric type fields without a specified list of values must be numeric greater than zero. 
d. Fields with other requirements must follow these requirements (for example Firm Number must be valid and 
eligible for Fund/SERV). 
• Optional fields means the following: 
a. Fields with specified list of values must have one of those values or space. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above. 
c. Numeric type fields without specified list of values must be numeric or space. 
d. Fields with other requirements must follow these requirements or may be space (for example Fund Number must 
be valid and eligible for Fund/SERV or may be space) 
• All dates in the layouts have the format ccyymmdd (except where otherwise indicated) where: 
cc = Century 
yy = Year in century 
mm = Month 
dd = Day in month 
Example: 
May 16, 2023, is represented as: 20230516 
December 13, 2023, is represented as 20231213 

---

## Page 13

© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: August 8, 2023 
Publication Code: MFS323 
Service: Mutual Fund Profile Service II 
Title: Introduction to Variable Length Record Layouts  
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 