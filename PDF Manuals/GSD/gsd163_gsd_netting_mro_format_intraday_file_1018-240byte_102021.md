---
title: "GSD Netting MRO Format (Intraday) – File 1018 – 240 Byte"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd163_gsd_netting_mro_format_intraday_file_1018-240byte_102021.pdf"
pages: 12
size: "245.3 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD Netting MRO Format (Intraday) – File 1018 – 240 Byte

**Original File:** [gsd163_gsd_netting_mro_format_intraday_file_1018-240byte_102021.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd163_gsd_netting_mro_format_intraday_file_1018-240byte_102021.pdf)  
**Category:** GSD  
**Total Pages:** 12  
**File Size:** 245.3 KB  

---

## Page 1

  
 
 
 
[[FICC]] – [[GSD]] 
[[GSD]] NETTING MRO FORMAT (INTRADAY) – FILE 1018 – 240 BYTE 
VERSION 2.0 
OCTOBER 2021 
 


---

## Page 2

 
  
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 2021 
Publication Code: GSD163 
Service: [[FICC]] – [[GSD]]   
Title: [[GSD]] Netting MRO Format (Intraday) File 1018 – 240 Byte 
 
 
The [[GSD]] Netting MRO Format (Intraday) File 1018 – 240 Byte (hereinafter, the "document") is provided as a convenience 
to Members and is for information purposes only. Although [[FICC]] may make this document available to Members, it shall be 
under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have a continuing obligation to make available 
this document or other related information of a certain type.  
 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose 
of any information provided to Members in this document, which is provided as-is. [[FICC]] shall not be liable for any 
loss related to such information (or the act or process of providing such information) resulting directly or 
indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
 
Further, the information contained in this document is subject to change. Members and other authorized users of the 
document will find the most current version of the document on [[DTCC]]’s Learning Center site, 
www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow 
[[FICC]]’s most current document. 
 
 

---

## Page 3

 
  
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 4 
Introduction .......................................................................................................................................................... 5 
Description of the Logical Detail Records ......................................................................................................... 6 
First 240 Byte Record ......................................................................................................................................... 6 
[[GSD]] Intraday Netting MRO Formats .................................................................................................................. 7 
Application Header Record ................................................................................................................................. 7 
Record Type 50 – Intraday [[participant]] Net Summary ........................................................................................ 8 
Application Trailer Record ................................................................................................................................ 11 
 

---

## Page 4

[[GSD]] Netting MRO Format (Intraday) – File 1018 – 240 Byte 
Overview 4 
 
OVERVIEW 
Intraday Netting Machine Readable Output (MRO) Specification 
This document provides Members of the Fixed Income Clearing Corporation‘s (“[[FICC]]”) Government [[securities]] 
Division (“[[GSD]]”) with machine readable output (MRO) specifications for [[GSD]] netting related record types used 
to support [[GSD]]’s products and services.  
Audience 
This document was written for systems and development personnel including managers, analysts and 
programmers of [[GSD]] [[Member]] firms. It presumes readers are familiar with technical concepts and terms as 
well as having a [[BASIC]] understanding of [[GSD]]'s products and services. 
Communication 
For information on [[FICC]] Connectivity, please contact [[FICC]] Integration at ficcintegration@[[DTCC]].com
. 
  

---

## Page 5

[[GSD]] Netting MRO Format (Intraday) – File 1018 – 240 Byte 
Introduction 5 
 
INTRODUCTION 
This document provides the formats for the [[GSD]] netting related record types used to support [[GSD]]’s products 
and services, enabling [[GSD]] Members to receive funds [[settlement]] obligation information related to the intraday 
funds [[settlement]] cycle.  
Messages discussed in this document will give Members the ability to take in important funds [[settlement]]  
information intraday. 
It should be noted that this document is a technical specification and is not, in any way, intended to 
communicate legal definitions as to when trades are guaranteed or novated by [[GSD]]. Members should refer to 
the [[FICC]] [[GSD]] Rulebook for such information. 
For additional service details, please refer to the Clearing Services > Fixed Income – [[GSD]] section available at 
www.[[DTCC]].com. 
Note:  
Record Type 50 (Intraday [[participant]] Summary) and Record Type 21 (End of Day [[participant]] Summary) will be 
decommissioned with the implementation of the proposed [[FICC]] Common Margining initiative. Currently, the [[FICC]] Common 
Margining initiative is pending regulatory approval.  

---

## Page 6

[[GSD]] Netting MRO Format (Intraday) – File 1018 – 240 Byte 
Description of the Logical Detail Records 6 
 
DESCRIPTION OF THE LOGICAL DETAIL RECORDS 
A logical record is made up of one or more 240 Byte physical records. The first 16 Bytes of each physical 
record consists of four fields, identified with asterisks (**) in the example below, which are referred to in the 
description of each record type as the STANDARD 16 BYTES. 
First 240 Byte Record 
Field Name Length Start End Type Comments 
Logical Record Number ** 5 1 5 N Sequential number of the logical record 
starting with 00001 
Physical Record Length ** 5 6 10 N Not greater than 240 
Checksum ** 5 11 15 A/N The CRC16 of the physical record  
(reserved for future use) 
Segment Location ** 1 16 16 N Where this physical record is located in the 
logical record 
 0 = Middle Record  
 1 = First Record 
 2 = Last Record  
 3 = Only Record 
Record [[ID]] 2 17 18 N Record Type:  
 17 – Transaction In Net  
 18 – Clearance Instruction  
 20 – Security Net Summary, etc.. 
Machine Readable Only  
Output 
222 19 240 A/N Refer to the description of each Record 
Type 
 
  

---

## Page 7

[[GSD]] Netting MRO Format (Intraday) – File 1018 – 240 Byte 
[[GSD]] Intraday Netting MRO Formats 7 
 
[[GSD]] INTRADAY NETTING MRO FORMATS 
Application Header Record 
Field Name Length Start End Type Comments 
Character Set 1 1 1 A/N "A" = ASCII, "E" = EBCDIC 
Block Size 5 2 6 N Unspecified, varies by Record Type 
Source Name 4 7 10 A/N “IONS” 
Filler 8 11 18 A/N  Always = Spaces 
Destination Name 4 19 22 A/N  [[GSD]] [[Member]] [[ID]] Number 
Filler 8 23 30 A/N Always = “_NET     “ 
Date/Time 22 31 52 A/N DD-MMM-YYYY HH:MM:SS:H 
 i.e. 19-JAN-2021 22:45:15:2 
Filler 188 53 240 A/N Always = Spaces 
 
  

---

## Page 8

[[GSD]] Netting MRO Format (Intraday) – File 1018 – 240 Byte 
[[GSD]] Intraday Netting MRO Formats 8 
 
Record Type 50 – Intraday [[participant]] Net Summary 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 50 Always = [[participant]] Net Summary  
[[Member]] [[ID]] 4 19 22 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 6 23 28 A/N Always = Spaces 
Opening Balance 11 29 39 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“. 
Opening Balance taken from prior funds 
[[settlement]] cycle’s Total Funds Obligation 
amount 
CR / DR Indicator 1 40 40 A/N “C” = Credit, “D” = Debit 
Next Day TAP 11 41 51 A/N Format same as Opening Balance. The 
[[Member]]’s TAP as derived from Trades that 
included in the net for next day [[settlement]] 
CR / DR Indicator 1 52 52 A/N “C” = Credit, “D” = Debit 
Fail Mark 11 53 63 A/N Format same as Opening Balance. The 
[[Member]]’s mark as derived from Failed 
[[obligations]] in this [[CUSIP]] 
CR / DR Indicator 1 64 64 A/N “C” = Credit, “D” = Debit 
Coupon Payment 11 65 75 A/N Format same as Opening Balance. The 
Total Interest paid on Coupon Payment 
Date 
CR / DR Indicator 1 76 76 A/N “C” = Credit, “D” = Debit 
Fails that Matured 11 77 87 A/N Format same as Opening Balance. The 
mark and interest associated with Failed 
[[obligations]] that have matured 
CR / DR Indicator 1 88 88 A/N “C” = Credit, “D” = Debit 
Clearance Differences 11 89 99 A/N Format same as Opening Balance. 
CR / DR Indicator 1 100 100 A/N “C” = Credit, “D” = Debit 
Miscellaneous Adjustments 11 101 111 A/N Format same as Opening Balance.  
CR / DR Indicator 1 112 112 A/N “C” = Credit, “D” = Debit 
Miscellaneous Reason 30 113 142 A/N Reason for Miscellaneous Adjustment 
Forward Mark Allocation 11 143 153 A/N Format same as Opening Balance. Forward 
Mark allocation as assessed by [[GSD]] for the 
current funds [[settlement]] cycle. 
CR / DR Indicator 1 154 154 A/N “C” = Credit, “D” = Debit 

---

## Page 9

[[GSD]] Netting MRO Format (Intraday) – File 1018 – 240 Byte 
[[GSD]] Intraday Netting MRO Formats 9 
 
Field Name Length Start End Type Comments 
Forward Mark Allocation 
Return 
11 155 165 A/N Format same as Opening Balance. Return 
of Forward Mark allocation as assessed by 
[[GSD]] for prior funds [[settlement]] cycle. 
CR / DR Indicator 1 166 166 A/N “C” = Credit, “D” = Debit 
Collected / Paid 18 167 177 A/N Format same as Opening Balance. Actual 
Amount of Total Funds Obligation settled for 
prior funds [[settlement]] cycle. 
CR / DR Indicator 1 178 178 A/N “C” = Credit, “D” = Debit 
Invoice 11 179 189 A/N Format same as Opening Balance. [[GSD]] 
Monthly Bill for [[Member]] 
CR / DR Indicator 1 190 190 A/N “C” = Credit, “D” = Debit 
Total Funds Obligation 11 191 201 A/N Format same as Opening Balance. 
Payment due to or from [[GSD]] for the current 
funds [[settlement]] cycle. 
CR / DR Indicator 1 202 202 A/N “C” = Credit, “D” = Debit 
Filler 12 203 214 A/N Always = Spaces 
Delivery Differential 11 215 225 A/N Format same as Opening Balance.  
CR / DR Indicator 1 226 226 A/N “C” = Credit, “D” = Debit 
Interest Adjustment 
Payment 
11 227 237 A/N Format same as Opening Balance. Accrued 
Interest paid / collected on Forward Mark 
Allocation collected / paid during prior 
intraday funds [[settlement]] cycle.  
CR / DR Indicator 1 238 238 A/N “C” = Credit, “D” = Debit 
Filler 1 239 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
“1” = First of many records (if overflow 
records are required) 
“2” = Last of many records (if 2 or more 
records are required) 
 
Note:  
Record Type 50 (Intraday [[participant]] Summary) and Record Type 21 (End of Day [[participant]] Summary) will be 
decommissioned with the implementation of the proposed [[FICC]] Common Margining initiative. Currently, the [[FICC]] Common 
Margining initiative is pending regulatory approval.  

---

## Page 10

[[GSD]] Netting MRO Format (Intraday) – File 1018 – 240 Byte 
[[GSD]] Intraday Netting MRO Formats 10 
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 50 Always = [[participant]] Net Summary  
[[Member]] [[ID]] 4 19 22 A/N [[GSD]] [[Member]] [[ID]] Number 
Opening Balance 14 23 36 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“. 
Opening Balance taken from prior funds 
[[settlement]] cycle’s Total Funds Obligation 
amount 
CR / DR Indicator 1 37 37 A/N “C” = Credit, “D” = Debit 
Forward Mark Allocation 14 38 51 A/N Format same as Opening Balance. Forward 
Mark Allocation as assessed by [[GSD]] for the 
current funds [[settlement]] cycle. 
CR / DR Indicator 1 52 52 A/N “C” = Credit, “D” = Debit 
Forward Mark Allocation 
Return 
14 53 66 A/N Format same as Opening Balance. Return 
of Forward Mark allocation as assessed by 
[[GSD]] for prior funds [[settlement]] cycle. 
CR / DR Indicator 1 67 67 A/N “C” = Credit, “D” = Debit 
Collected / Paid 14 68 81 A/N Format same as Opening Balance. Actual 
Amount of Total Funds Obligation settled for 
prior funds [[settlement]] cycle. 
CR / DR Indicator 1 82 82 A/N “C” = Credit, “D” = Debit 
Total Funds Obligation 14 83 96 A/N Format same as Opening Balance. 
Payment due to or from [[GSD]] for the current 
funds [[settlement]] cycle. 
CR / DR Indicator 1 97 97 A/N “C” = Credit, “D” = Debit 
Filler 142 98 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
“1” = First of many records (if overflow 
records are required) 
“2” = Last of many records (if 2 or more 
records are required) 
Note: 
The usage of the Overflow record is as follows:  
If a value of zero is encountered in the "OPENING BALANCE", "FORWARD MARK ALLOCATION", "FORWARD MARK 
ALLOCATION RETURN", "COLLECTED / PAID" or "TOTAL FUNDS OBLIGATION" fields in Record Type 50 (non-
OVERFLOW) and a non-blank value is found in the CONFIRMATION CONTINUED field (position 240) then an Overflow 
record will follow. 

---

## Page 11

[[GSD]] Netting MRO Format (Intraday) – File 1018 – 240 Byte 
[[GSD]] Intraday Netting MRO Formats 11 
 
Application Trailer Record 
Field Name Length Start End Type Comments 
Trailer [[ID]] 5 1 5 A/N Always = “TRAIL” 
Number of Records 5 6 10 N Total Number of 240 Byte output records in 
file 
Checksum 5 11 15 A/N XOR of Checksums of all other data records 
(For Future Use) 
Filler 225 16 240 A/N Always = Spaces 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 12

 
  
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 