---
title: "MFPS II - Introduction to Fixed Length Record Layouts - Part 1"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part1_fixed_intro_layouts_mfs322_20230808.pdf"
pages: 14
size: "261.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II - Introduction to Fixed Length Record Layouts - Part 1

**Original File:** [mfps2_part1_fixed_intro_layouts_mfs322_20230808.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part1_fixed_intro_layouts_mfs322_20230808.pdf)  
**Category:** Other  
**Total Pages:** 14  
**File Size:** 261.6 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service II 
INTRODUCTION TO FIXED LENGTH RECORD 
LAYOUTS – PART 1 
 
AUGUST 8, 2023 
 

---

## Page 2

Introduction to Fixed Length Record Layouts – Part 1 
Introduction 2 
HISTORY OF CHANGES 
Dates Descriptions 
August 8, 2023 Record was rebranded and reviewed.  
Effective Date: May 1, 2023 MFSP2 [[participant]] database was decommissioned.  
Please See Important Notice a9279 P&S 8852 
Dated March 21, 2023 
July 6, 2022 Record was rebranded and reviewed. 
Effective Date: March 25, 2019 Please see Important Notice: a8658 p&s 8233 
Dated December 19, 2018 
Effective Date: March 27, 2006 Please see Important Notice: a6171 p&s 5741  
Dated December 21, 2005 
Effective Date: November 14, 2005 Please see Important Notice: a6084 p&s 5654  
Dated August 10, 2005 
Effective Date: August 29, 2005 Please see Important Notice a6062 p&s 5632  
Dated July 6, 2005 
 

---

## Page 3

Introduction to Fixed Length Record Layouts – Part 1 
Introduction 3 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 4 
Fixed Length Format ............................................................................................................................................ 5 
Recipient Number................................................................................................................................................. 6 
"Required" Indication .......................................................................................................................................... 7 
Key Data ................................................................................................................................................................ 8 
Replace Rules ....................................................................................................................................................... 9 
Delete Rules ........................................................................................................................................................ 10 
Record Layouts .................................................................................................................................................. 11 
 
 
 
 
 
 
 
 
 

---

## Page 4

Introduction to Fixed Length Record Layouts – Part 1 
Introduction 4 
INTRODUCTION 
Some of the features of the Mutual Fund Profile Service (MFPS) [[NSCC]] (non-ISO) records layout features are:  
1. Records can be received or submitted in either of two formats: fixed length or variable length.  
2. This document describes the MFPS [[NSCC]] (non-ISO) fixed length record layouts.  
3. Only [[NSCC]] rejected transactions are being returned by [[NSCC]] to the originating [[participant]]. Accepted 
transactions are being sent to the recipient only.  
4. When rejecting a transaction for more than one reason, MFPS reports multiple rejects codes via record 
type 120 (see the Record Layouts section) which follows the rejected transaction back to the originating 
[[participant]]. 

---

## Page 5

Introduction to Fixed Length Record Layouts – Part 1 
Fixed Length Format 5 
FIXED LENGTH FORMAT 
Each fixed length transaction consists of one or more 80-byte long records.  
Each 80 byte long record starts with the following two fields: 
1. Physical Sequence Number (bytes 1-2) 
2. Logical Sequence Number (bytes 3-4) 
 
The physical sequence number of the first record in a submitted transaction must be 01 and should increase by 
one from record to record within the transaction. 
The physical sequence number of the last record in a submitted transaction must start with 9.  
The logical sequence numbers within a submitted transaction must be in ascending order and cannot exceed 
the maximum allowed for that transaction (see record layouts). 
Example: 
The following are valid sequence numbers for Price/Rate transactions:  
0101 9203 
Notes:  
1. The last physical sequence number is 92 (rather than 02) to indicate that it is the last physical record of this Price/Rate 
transaction.  
2. Logical sequence number 02 (optional record) is not included in this MFPS Profile transaction. 

---

## Page 6

Introduction to Fixed Length Record Layouts – Part 1 
Recipient Number 6 
RECIPIENT NUMBER 
In MFPS, the Recipient Number field is used to direct the output to the proper recipient(s). When the Recipient 
Number is left blank, the output is considered global and is sent globally. 
By supplying a Recipient Number, the originator can send specific data to specific recipients.  

---

## Page 7

Introduction to Fixed Length Record Layouts – Part 1 
"Required" Indication 7 
"REQUIRED" INDICATION 
When Action code = ‘D’ only the key fields are required (see below). 

---

## Page 8

Introduction to Fixed Length Record Layouts – Part 1 
Key Data 8 
KEY DATA 
In order to apply any updates to the MFPS data stores key information must be supplied with the transaction. 
Key fields are identified in the record layouts by a '@' or a '@@'. Fields marked with ‘@’ must be present at all 
times for every sub-type of the transaction. For the key fields marked with ‘@@’ – only one of them should be 
present. 

---

## Page 9

Introduction to Fixed Length Record Layouts – Part 1 
Replace Rules 9 
REPLACE RULES 
When a transaction is received with Action Type = C, the new data replaces the existing information in its 
entirety. 

---

## Page 10

Introduction to Fixed Length Record Layouts – Part 1 
Delete Rules 10 
DELETE RULES 
When Action code = ‘D’, only the key information should be supplied. 

---

## Page 11

Introduction to Fixed Length Record Layouts – Part 1 
Record Layouts 11 
RECORD LAYOUTS 
The following record types will be used by MFPS: 
000 — [[NSCC]] Output Header 
020 — Security Issue General Profile 
021 — Security Blue Sky 
022 — Security CDSC Information 
023 — Security Breakpoint Schedules 
024 — Security Commission 
025  — [[NSCC]] Social Code Eligibility  
026  — Short Term Redemption Data 
027 — Fund/SERV Security Master File 
029 — Security Issue Breakpoint Linkage Rules 
040 — Distribution Declaration 12b-1 
041 — Distribution Declaration Cap Gains 
042 — Distribution Declaration [[Dividend]] 
043 — Distribution Declaration General Earnings 
044 — Distribution Declaration Municipal Earnings 
080 — User File Request 
120 — Multiple Reject Codes 
999 — Trailer 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 12

Introduction to Fixed Length Record Layouts – Part 1 
Record Layouts 12 
Also detailed in this document are Datatrak Header, Datatrak Trailer and MFPS reject code list.  
The column headings in this document are as follows: 
Start - The position where the field starts. 
End - The position where the field ends. 
Len - The length of the field in bytes 
Type - The type of the field:  
A/N = Alphanumeric  
N = Numeric  
Field Name - The name of the field. 
Description - Field description (format, valid values, conditional requirements, etc.). 
Opt/Req - Indicates whether the field is optional or required:  
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
d. Fields with other requirements must follow those requirements (for example Firm Number must be valid and 
eligible for Fund/SERV).  
• Optional fields mean the following:  
a. Fields with specified list of values must have one of those values or space.  
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above.  
c. Numeric type fields without specified list of values must be numeric or space.  
d. Fields with other requirements must follow those requirements or may be space.  
• All data fields are presented as relating to the Submitting [[participant]], unless otherwise specified. So, Contact Name is 
the Submitting [[participant]]’s Contact Name.  

---

## Page 13

Introduction to Fixed Length Record Layouts – Part 1 
Record Layouts 13 
• All dates in the layouts have the format ccyymmdd (except where otherwise indicated) where:  
cc = Century  
yy = Year in century 
mm = Month  
dd = Day in month 
Examples:  
January 4, 2023, is represented as: 20230104 
December 13, 2023, is represented as: 20231213 
 

---

## Page 14

© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: August 8, 2023 
Publication Code: MFS322 
Service: Mutual Fund Profile Service II 
Title: Introduction to Fixed Length Record Layouts – Part 1 
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 