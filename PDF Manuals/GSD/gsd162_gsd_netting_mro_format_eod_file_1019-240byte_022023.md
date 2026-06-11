---
title: "GSD Netting MRO Format (EOD) – File 1019 – 240 Byte"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd162_gsd_netting_mro_format_eod_file_1019-240byte_022023.pdf"
pages: 29
size: "454.4 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD Netting MRO Format (EOD) – File 1019 – 240 Byte

**Original File:** [gsd162_gsd_netting_mro_format_eod_file_1019-240byte_022023.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd162_gsd_netting_mro_format_eod_file_1019-240byte_022023.pdf)  
**Category:** GSD  
**Total Pages:** 29  
**File Size:** 454.4 KB  

---

## Page 1

 
 
 
[[FICC]] – [[GSD]] 
[[GSD]] NETTING MRO FORMAT ([[EOD]]) – FILE 1019 – 240 BYTE 
VERSION 2.1 
FEBRUARY 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in wh ich such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: February 2023 
Publication Code:  GSD162 
Service: [[FICC]] – [[GSD]]   
Title: [[GSD]] Netting  MRO Format ([[EOD]]) File 1019 – 240 Byte 
 
 
The [[GSD]] Netting  MRO Format ([[EOD]]) File 1019 – 240 Byte (hereinafter, the " document ") is provided as a convenience to 
Members and is for information purposes only. Although [[FICC]] may make this document  available to Members, it shall be 
under no obligation to [[DO]] so, nor  having once or more done so, shall [[FICC]] have a continuing obligation to make available 
this document  or other related information of a certain type.   
 
[[FICC]] does not represent the accuracy, adequacy, tim eliness, completeness, or fitness for any particular purpose 
of any information provided to M embers in this document , which is provided as -is. [[FICC]] shall not be liable for any 
loss related to such information (or the act or process of providing such inform ation) resulting directly or 
indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
 
Further, the information contained in this document is subject to change. Members  and other authorized users of the 
document  will find the most current version of the document on [[DTCC]]’s Learning Center  site, 
www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow  
[[FICC]]’s most current document . 
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Overview ......................................................................................................................................... 4 
Introduction..................................................................................................................................... 5 
Description of the Logical Detail Records .......................................................................................... 6 
First 240 Byte Record...................................................................................................................... 6 
[[GSD]] [[EOD]] Netting MRO Formats ....................................................................................................... 7 
Application Header Record............................................................................................................... 7 
Recor d Type  17  – Transaction In Net.................................................................................................  8 
Recor d Type  18  – Clearance Instruction............................................................................................. 9 
Recor d Type  20  – Security Net Summary ......................................................................................... 10 
Recor d Type  21  – End of Day [[participant]] Net Summary ..................................................................... 12 
Recor d Type  23  – Cleared Obligation .............................................................................................. 15 
Recor d Type  25  – Rec alc ulated  Mo ney  for Coupon Reset .................................................................. 16 
Recor d Type  26  – Forward Transaction Pended for Netting.................................................................  17 
Recor d Type  27  – Forward Transaction Pended – No Lo ng er in Net ..................................................... 18 
Recor d Type  28  – Forward Position Summary .................................................................................. 19 
Recor d Type  29  – Rec alc ulated  Mo ney  for Yield  Trad e ...................................................................... 20 
Recor d Type  33  – Commission Modification ..................................................................................... 21 
Recor d Type  38  – Repo Coupon Payment........................................................................................ 22 
Recor d Type  39  – Per-Trade Forward Mark ...................................................................................... 23 
Recor d Type  49  – Paired-Off Obligation ........................................................................................... 24 
Application Trailer Record .............................................................................................................. 25 
Appendices ....................................................................................................................................26  
List of Appendices ........................................................................................................................ 26 
Appendix A – Mes s ag e Flo ws (Reserv ed fo r Future Use) .................................................................. 27 
Appendix B – Message Samples (Reserved for Future Use) .............................................................. 28 
 

---

## Page 4

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
Overview 4 
OVERVIEW 
End of Day ([[EOD]]) Netting Machine Readable Output (MRO) Specification 
This document provides Members of the Fixed Income Clearing Corporation‘s (“[[FICC]]”) Government [[securities]] 
Division (“[[GSD]]”) with machine readable output (MRO) specifications for [[GSD]] netting related record types used 
to support [[GSD]]’s products and services.  
Audience 
This document was written for systems and development personnel including managers, analysts and 
programmers of [[GSD]] [[Member]] firms. It presumes readers are familiar with technical concepts and terms as 
well as having a [[BASIC]] understanding of [[GSD]]'s products and services. 
Communication 
For information on [[FICC]] Connectivity, please contact [[FICC]] Integration at ficcintegration@[[DTCC]].com. 
  

---

## Page 5

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
Introduction 5 
INTRODUCTION 
This document provides the formats for the [[GSD]] netting related record types used to support [[GSD]]’s products 
and services, enabling [[GSD]] Members to receive statuses on their trades and [[settlement]] [[obligations]] along with 
other trade related messages, i.e. coupon payments, recalculation of final money on yield trades, etc.  
Messages discussed in this document will give Members the ability to take in important trade and [[settlement]] 
information and manage their activity at end of day. 
It should be noted that this document is a technical specification and is not, in any way, intended to 
communicate legal definitions as to when trades are guaranteed or novated by [[GSD]]. Members should refer to 
the [[FICC]] [[GSD]] Rulebook for such information. 
For additional service details, please refer to the Clearing Services > Fixed Income – [[GSD]] section available at 
www.[[DTCC]].com. 
Note:  
Record Type 21 (End of Day [[participant]] Summary) and Record Type 50 (Intraday [[participant]] S ummary) will be 
decommissioned with the implementation of the proposed [[FICC]] Common Margining initiative. Currently, the [[FICC]] Common 
Margining initiative is pending regulatory approval.  
 

---

## Page 6

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
Description of the Logical Detail Records 6 
DESCRIPTION OF THE LOGICAL DETAIL RECORDS 
A logical record is made up of one or more 240 Byte physical records. The first 16 Bytes of each physical 
record consists of four fields, identified with asterisks (**) in the example below, which are referred to in the 
description of each record type as the STANDARD 16 BYTES. 
First 240 Byte Record 
Field Name Length Start End Type Comments 
Logical Record Number ** 5 1 5 N Sequential number of the logi cal record 
starting with 00001 
Physical Record Length **  5 6 10 N Not greater than 240 
Checksum ** 5 11 15 A/N The CRC16 of the physical record  
(reserved for future use)  
Segment Location **  1 16 16 N Where this physical recor d is located in the 
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

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 7 
[[GSD]] [[EOD]] NETTING MRO FORMATS 
Application Header Record 
Field Name Length Start End Type Comments 
Character Set 1 1 1 A/N "A" = ASCII, "E" = EBCDIC 
Block Size 5 2 6 N Unspecified, varies by Record Type 
Source Name 4 7 10 A/N “IONS” 
Filler  8 11 18 A/N  Always = Spaces  
Destination Name 4 19 22 A/N  [[GSD]] [[Member]] [[ID]] Number  
Filler  8 23 30 A/N Always = “_NET     “  
Date/Time 22 31 52 A/N DD-MMM-YYYY HH:MM:SS:H 
 i.e. 19-JAN-2021 22:45:15:2 
Filler  188 53 240 A/N Always = Spaces  
 
  

---

## Page 8

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 8 
Record Type 17 – Transaction In Net 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 17 Always = Transaction In Net  
External Reference Number  16 19 34 A/N As supplied by the [[Member]]  (a sequence 
number which remains unique to this 
Transaction as long as it is in the system)  
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
[[Member]] [[ID]] 4 50 53 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler  6 54 59 A/N Always = Spaces  
Locked In Trade  1 60 60 A/N  “X” = Submitter of Locked -In Trade 
“L” = Recipient of Locked -In Trade 
“  ” = Not Locked -In Trade 
Secondary External 
Reference Number 
16 61 76 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  4 77 80 A/N Always = Spaces  
Netting Status 9 81 89 A/N Indicates what type of trade, submitted by a 
Repo Netting [[Member]] is going into the net. 
The field is filled in with one of the following:  
“START LEG”,                                        
“END LEG”,                                               
“FAIL”,                                               
“TRADE” – For Cash Market Side                
or                                                                     
All blanks for a trade submitted by any other 
[[Member]] who  is not a Repo Netting [[Member]]  
Filler  150 90 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
 
  

---

## Page 9

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 9 
Record Type 18 – Clearance Instruction  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 18 Always = Clearance Instruction  
Transaction [[ID]]  11 19 29 A/N The [[ID]] assigned to this Obligation by [[GSD]]. 
Format is XXXXXX-XXXX 
[[Member]] [[ID]] 4 30 33 A/N [[GSD]] [[Member]] [[ID]] Number  
Filler  4 34 39 A/N Always = Spaces  
Transaction Code  1 40 40 A/N “L” = Long, “S” = Short  
[[CUSIP]] Number 9 41 49 A/N [[CUSIP]] Number 
Filler  6 50 55 A/N Always = Spaces  
Quantity  18 56 73 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“  
Amount 18 74 91 A/N Format same as Quantity  
Clearing Bank ABA 9 92 100 A/N ABA of [[GSD]] Clearing Bank provided by 
[[GSD]] 
Fed Address  40 101 140 A/N Fed Wire Address  
[[GSD]] Contra [[ID]] at [[Member]] 
Bank 
20 141 160 A/N [[Member]]’s Bank Short Name for [[GSD]] 
Account at its Bank for this Product  
Clearance Type 1 161 161 A/N “N” = Next Day, “F” = Fail, “H” = Held Fail  
[[settlement]] Date 10 162 171 A/N Format is MM/DD/YYYY 
Previous TID 11 172 182 A/N For Fail the format is XXXXXX-XXXX           
If not a Fail, then this field is Blank  
Original TID  11 183 193 A/N [[ID]] Assigned to Transactions when it first 
appeared as an Instruct.                         
Format is XXXXXX-XXXX 
Filler  46 194 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
 
  

---

## Page 10

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 10 
Record Type 20 – Security Net Summary  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 20 Always = Security Net Summary  
[[Member]] [[ID]] 4 19 22 A/N [[GSD]] [[Member]] [[ID]] Number  
Filler  6 23 28 A/N Always = Spaces  
[[CUSIP]] Number 9 29 37 A/N [[CUSIP]] Number 
Filler  6 38 43 A/N Always = Spaces  
[[settlement]] Price  14 44 57 A/N Right Justified Blank Filled, i.e., “     98.575“. 
Price used by [[GSD]] for all deliveries of this 
[[CUSIP]] for this [[settlement]] Date  
Next Day Position  18 58 75 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“. 
Net Par Position as reflected by Next Day 
Trades included in the net  
Long / Short Indicator  1 76 76 A/N “L” = Long, “S” = Short  
Fail Position  18 77 94 A/N Format same as Next Day Position. Net Par 
Position as reflected by Failed [[obligations]] 
included in the net  
Long / Short Indicator  1 95 95 A/N “L” = Long, “S” = Short  
Fail Mark 18 96 113 A/N Format same as Next Day Position. The 
[[Member]]’s mark as derived from Failed 
[[obligations]] in this [[CUSIP]]  
CR / DR Indicator  1 114 114 A/N “C” = Credit, “D” = Debit  
Coupon Payment  18 115 132 A/N Format same as Next Day Position. The 
Total Interest paid on Coupon Payment 
Date 
CR / DR Indicator  1 133 133 A/N “C” = Credit, “D” = Debit  
Fails that Matured  18 134 151 A/N Format same as Next Day Position. The 
mark and interest associated with Failed 
[[obligations]] that have matured  
CR / DR Indicator  1 152 152 A/N “C” = Credit, “D” = Debit  
Next Day TAP 18 153 170 A/N Format same as Next Day Position. The 
[[Member]]’s TAP as derived from Next Day 
Trades that were included in the net  
CR / DR Indicator  1 171 171 A/N “C” = Credit, “D” = Debit  
Clearance Differences  18 172 189 A/N Format same as Next Day Position.  
CR / DR Indicator  1 190 190 A/N “C” = Credit, “D” = Debit  

---

## Page 11

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 11 
Field Name Length Start End Type Comments 
Failed Accrued Interest  18 191 208 A/N Format same as Next Day Position. The 
accrued interest as der ived from the day’s 
Failed [[obligations]]  
CR / DR Indicator  1 209 209 A/N “C” = Credit, “D” = Debit  
Delivery Differential  18 210 227 A/N Format same as Next Day Position.  
CR / DR Indicator  1 228 228 A/N “C” = Credit, “D” = Debit  
Filler  11 229 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
 
  

---

## Page 12

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 12 
Record Type 21 – End of Day [[participant]] Net Summary 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 21 Always = [[participant]] Net Summary  
[[Member]] [[ID]] 4 19 22 A/N [[GSD]] [[Member]] [[ID]] Number  
Filler  6 23 28 A/N Always = Spaces  
Opening Balance  11 29 39 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“. 
Opening Balance taken from prior funds 
[[settlement]] cycle’s Total Funds Obligation 
amount 
CR / DR Indicator  1 40 40 A/N “C” = Credit, “D” = Debit  
Next Day TAP 11 41 51 A/N Format same as Opening Balance. The 
[[Member]]’s TAP as derived from Next Day 
Trades that were included in the net  
CR / DR Indicator  1 52 52 A/N “C” = Credit, “D” = Debit  
Fail Mark 11 53 63 A/N Format same as Opening Balance.  The 
[[Member]]’s mark as deri ved from Failed 
[[obligations]] in this [[CUSIP]]  
CR / DR Indicator  1 64 64 A/N “C” = Credit, “D” = Debit  
Coupon Payment  11 65 75 A/N Format same as Opening Balance. The 
Total Interest paid on Coupon Payment 
Date 
CR / DR Indicator  1 76 76 A/N “C” = Credit, “D” = Debit  
Fails that Matured  11 77 87 A/N Format same as Opening Balance . The 
mark and interest associated with Failed 
[[obligations]] that have matured  
CR / DR Indicator  1 88 88 A/N “C” = Credit, “D” = Debit  
Clearance Differences  11 89 99 A/N Format same as Opening Balance.  
CR / DR Indicator  1 100 100 A/N “C” = Credit, “D” = Debit  
Miscellaneous Adjustments  11 101 111 A/N Format same as Opening Balance.  
CR / DR Indicator  1 112 112 A/N “C” = Credit, “D” = Debit  
Miscellaneous Reason  30 113 142 A/N Reason for Miscellaneous Adjustment  
Forward Mark Allocation  11 143 153 A/N Format same as Opening Balance. Forwar d 
Mark allocation as as sessed by [[GSD]] for the 
current funds [[settlement]] cycle.  
CR / DR Indicator  1 154 154 A/N “C” = Credit, “D” = Debit 

---

## Page 13

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 13 
Field Name Length Start End Type Comments 
Forward Mark Allocation 
Return 
11 155 165 A/N Format same as Opening Balance. Return 
of Forward Mark allocation as assessed by 
[[GSD]] for prior funds [[settlement]] cycle.  
CR / DR Indicator  1 166 166 A/N “C” = Credit, “D” = Debit  
Collected / Paid  18 167 177 A/N Format same as Opening Balance.  Actual 
Amount of Total Funds Obligation settle d f or 
prior funds [[settlement]] cycle.  
CR / DR Indicator  1 178 178 A/N “C” = Credit, “D” = Debit  
Invoice  11 179 189 A/N Format same as Opening Balance. [[GSD]] 
Monthly Bill for [[Member]]  
CR / DR Indicator  1 190 190 A/N “C” = Credit, “D” = Debit  
Total Funds Obligation  11 191 201 A/N Format same as Opening Balance.  
Payment due to or from [[GSD]] for the current 
funds [[settlement]] cycle.  
CR / DR Indicator  1 202 202 A/N “C” = Credit, “D” = Debit  
Filler  12 203 214 A/N Always = Spaces  
Delivery Differential  11 215 225 A/N Format same as Opening Balance.  
CR / DR Indicator  1 226 226 A/N “C” = Credit, “D” = Debit  
Interest Adjustment 
Payment 
11 227 237 A/N Format same as Opening Balance. Accrued 
Interest paid / collected on Forward Mark 
Allocation collected / paid during pri or 
intraday funds [[settlement]] cycle.  
CR / DR Indicator  1 238 238 A/N “C” = Credit, “D” = Debit  
Filler  1 239 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
Note:  
Record Type 21 (End of Day [[participant]] Summary) and Record Type 50 (Intraday [[participant]] Summary) will be 
decommissioned with the implementation of the p roposed [[FICC]] Common Margining initiative. Currently, the [[FICC]] Common 
Margining initiative is pending regulatory approval.   

---

## Page 14

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 14 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 21 Always = [[participant]] Net Summary  
[[Member]] [[ID]] 4 19 22 A/N [[GSD]] [[Member]] [[ID]] Number  
Opening Balance  14 23 36 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“. 
Opening Balance taken from prior funds 
[[settlement]] cycle’s Total Funds Obligation 
amount 
CR / DR Indicator  1 37 37 A/N “C” = Credit, “D” = Debit  
Forward Mark Allocation  14 38 51 A/N Format same as Opening Balance. Forwar d 
Mark Allocation as assessed by [[GSD]] for the 
current funds [[settlement]] cycle.  
CR / DR Indicator  1 52 52 A/N “C” = Credit, “D” = Debit  
Forward Mark Allocation 
Return 
14 53 66 A/N Format same as Opening Balance . Return 
of Forward Mark allocation as assessed by 
[[GSD]] for prior funds [[settlement]] cycle.  
CR / DR Indicator  1 67 67 A/N “C” = Credit, “D” = Debit  
Collected / Paid  14 68 81 A/N Format same as Opening Balance.  Actual 
Amount of Total Funds Obligation settle d f or 
prior funds [[settlement]] cycle.  
CR / DR Indicator  1 82 82 A/N “C” = Credit, “D” = Debit  
Total Funds Obligation  14 83 96 A/N Format same as Opening Balance.  
Payment due to or from [[GSD]] for the current 
fund s [[settlement]] cycle.  
CR / DR Indicator  1 97 97 A/N “C” = Credit, “D” = Debit  
Filler  142 98 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
Note: 
The usage of the Overflow record is as follows:  
If a value of zero is encountered in the "OPENING BALANCE", "FORWARD MARK ALLOCATION", "FORWARD MARK 
ALLOCATION RETURN", "COLLE CTED / PAID" or "TOTAL FUNDS OBLIGATION" fields in Type 21 (non -OVERFLOW) 
and a non- blank value is found in the CONFIRMATION CONTINUED field (position 240) then an Overflow record will 
follow.   

---

## Page 15

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 15 
Record Type 23 – Cleared Obligation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 23 Always = Cleared Obligation  
Transaction [[ID]]  11 19 29 A/N The [[ID]] assigned to this Obligation by [[GSD]]. 
Format is XXXXXX-XXXX 
[[Member]] [[ID]] 4 30 33 A/N [[GSD]] [[Member]] [[ID]] Number  
Filler  4 34 39 A/N Always = Spaces  
Transaction Code  1 40 40 A/N “L” = Long, “S” = Short  
[[CUSIP]] Number 9 41 49 A/N [[CUSIP]] Number 
Filler  6 50 55 A/N Always = Spaces  
Quantity  Cleared 18 56 73 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“  
Amount Cleared 18 74 91 A/N Format same as Quantity  Cleared 
Remaining Clear Quantity  18 92 109 A/N Format same as Quantity Cleared 
Clearance Method  1 110 110 A/N “C” = Cleared                                                   
“B” = Bought In                                            
“H” = Held Fail Matured                                      
“M” = Matured                                              
“N” = Netted                                               
“P” = Pair-off 
Clearance Difference  18 111 128 A/N Format same as Quantity Cleared.  
CR / DR Indicator  1 129 129 A/N “C” = Credit, “D” = Debit  
Original TID  11 130 140 A/N [[ID]] Assigned to Transactions when it first 
appeared as an Instruct.                         
Format is XXXXXX-XXXX 
Opening Par  18 141 158 A/N Format same as Quantity Cleared. This is 
the Par on the Instruct at the opening of the 
day before any clearance occurs.  
Fail Mark 18 159 176 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“  
CR / DR Indicator  1 177 177 A/N “C” = Credit, “D” = Debit  
Filler  62 178 239 A/N Always = Spaces  
Confirmation Continued  1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
  

---

## Page 16

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 16 
Record Type 25 – Recalculated Money for Coupon Reset  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 25 Always = Recalculated Money for 
Coupon Reset  
External Reference Number  16 19 34 A/N XREF as supplied by the [[Member]]   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Coupon Indicator  1 50 50 A/N “F” = Floating Rate Reset  
“J” = Adjustable Rate Reset  
Final Money Amount  11 51 61 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“ . 
Recalculated amount  
Compared on Yield 1 62 62 A/N “Y” = Yes, “N“ = No  
Compared on Money  1 63 63 A/N “Y” = Yes, “N“ = No  
Deleted Tonight  1 64 64 A/N “Y” = Yes, “N“ = No 
Reset Rate 9 65 73 A/N Format is XX.XXXXXX 
Reset Basis  1 74 74 A/N “G” = GCF Index                                                         
“L” = LIBOR                                                       
“T” = TBILL Rate 
Reset Spread  9 75 83 A/N Format is XX.XXXXXX 
Reset Cycle  1 84 84 A/N “D” = Daily                                                        
“M” = Monthly                                                  
“Q” = Quarterly                                                     
“S” = Semi Annual                                           
“W” = Weekly  
Previous Rate 9 85 93 A/N Format is XX.XXXXXX 
Reset Date 10 94 103 A/N Format is MM/DD/YYY 
Filler  136 104 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
  

---

## Page 17

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 17 
Record Type 26 – Forward Transaction Pended for Netting  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 26 Always = Forward Transaction Pended 
for Netting  
External Reference Number  16 19 34 A/N As supplied by the [[Member]]  (a sequence 
number which remains unique to this 
Transaction as long as it is in the system)  
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Coupon Indicator  1 50 50 A/N “A” = Assumed Coupon 
“R” = Real Coupon  
Amount 11 51 61 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1365000“.  
Trade Novated at this amount  
Secondary External 
Reference Number 
16 62 77 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  4 78 81 A/N Always = Spaces  
Initiated By  4 82 85 A/N Filled in with the word “SUB” if the 
confirmation resulted from a [[CUSIP]] 
Substitution: Otherwise , field is kept blank  
Filler  154 86 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
 
  

---

## Page 18

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 18 
Record Type 27 – Forward Transaction Pended – No Longer in Net  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 27 Always = Forward Transaction Pended –  
No Longer in the Net  
External Reference Number 16 19 34 A/N As supplied by the [[Member]]  (a sequence 
number which remains unique to this 
Transaction as long as it is in the system)  
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Secondary External 
Reference Number 
16 50 65 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  4 66 69 A/N Always = Spaces  
Initiated By  4 70 73 A/N Filled in with the word “SUB” if the 
confirmation resulted from a [[CUSIP]] 
Substitution: Otherwise , field is kept blank  
Filler  166 74 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
 
  

---

## Page 19

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 19 
Record Type 28 – Forward Position Summary  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 28 Always = Forward Position Summary  
[[CUSIP]] Number 9 19 27 A/N [[CUSIP]] Number 
Filler  6 28 33 A/N Always = Spaces  
Price  14 34 47 A/N Right Justified Blank Filled, i.e., “     98.575“.  
Price used by [[GSD]] for Forward Mark 
Allocation  
Forward Position  18 48 65 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“. 
Net Par Position as reflected by Forward 
Trades Pended for Netting 
Long / Short Indicator  1 66 66 A/N “L” = Long, “S” = Short  
Forward Amount  18 67 84 A/N Format same as Forward Position. Net 
Amount as reflected by Forward Trades 
Pended for Netting 
CR / DR Indicator  1 85 85 A/N “C” = Credit, “D” = Debit  
Forward Mark  18 86 103 A/N Format same as Forward Position. 
Informational Only. Net of Forward Marks 
for each Trade Pended for Netting 
CR / DR Indicator  1 104 104 A/N “C” = Credit, “D” = Debit  
Forward Mark Allocation  18 105 122 A/N Format same as Forward Position. Net If 
Forward Mark is a Credit, the value in this 
field will be “0.00”. Otherwise, the value will 
be assessed by [[GSD]]  
CR / DR Indicator  1 123 123 A/N “C” = Credit, “D” = Debit  
[[Member]] [[ID]] 4 124 127 A/N [[GSD]] [[Member]] [[ID]] Number  
Filler  6 128 133 A/N Always = Spaces  
Coupon Indicator  1 134 134 A/N “A” = Assumed Coupon, “R” = Real Coupon  
Coupon Rate  10 135 144 A/N Right Justified Blank Filled, i.e., 9 Percent 
would be = “     9.000000“. Coupon Rate for 
this [[CUSIP]] 
Filler  95 145 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
  

---

## Page 20

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 20 
Record Type 29 – Recalculated Money for Yield Trade  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 29 Always = Recalculated Money for Yield 
Trade 
External Reference Number  16 19 34 A/N XREF as supplied by the [[Member]]   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Coupon Indicator  1 50 50 A/N “A” = Assumed Coupon, “R” = Real Coupon  
Amount 11 51 61 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1365000“  
 Recalculated amount for Yield Trade 
Compared on Yield 1 62 62 A/N “Y” = Yes, “  “ = No  
Compared on Money  1 63 63 A/N “Y” = Yes, “  “ = No  
Deleted Tonight  1 64 64 A/N “Y” = Yes, “  “ = No 
Filler  175 65 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
Note: 
If you select to receive Record Type 29 for netting, the system will not allow you to receive Record Type 29 for comparison.  
 
  

---

## Page 21

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 21 
Record Type 33 – Commission Modification  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 33 Always = Commission Modifica tion 
External Reference Number  16 19 34 A/N XREF as supplied by the [[Member]]   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
New Commission  11 50 60 A/N As supplied by the [[Member]], or as 
recalculated if the amount is submitted  
New Amount  18 61 78 A/N As supplied by the [[Member]], or as 
recalculated if blank and the commission is 
submitted 
Previous Commission  11 79 89 A/N The previous commission before 
modification  
Previous Amount  18 90 107 A/N The previous amount before modification 
Filler  132 108 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
Note:  
If you select to receive Record Type 33 for netting, the system will not allow you to receive Record Type 33 for comparison.  
  

---

## Page 22

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 22 
Record Type 38 – Repo Coupon Payment  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 38 Always = Repo Coupon Payment 
Confi rmation  
[[Member]] [[ID]] 4 19 22 A/N [[GSD]] [[Member]] [[ID]] Number  
Filler  6 23 28 A/N Always = Spaces  
[[CUSIP]] Number 9 29 37 A/N As supplied by the [[Member]]  
Filler  6 38 43 A/N Always = Spaces  
External Reference Number  16 44 59 A/N As supplied by the [[Member]]  (a sequence 
number which remains unique to this 
Transaction as long as it is in the system)  
Filler  4 60 63 A/N Always = Spaces  
Transaction [[ID]]  11 64 74 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Payment Amount  18 75 92 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00    “  
Credit / Debit 1 93 93 A/N “C” = Credit, “D” = Debit  
Secondary External 
Reference Number 
16 94 109 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  130 110 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
 
  

---

## Page 23

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 23 
Record Type 39 – Per-Trade Forward Mark  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 39 Always = Per-Trade Forward Mark 
Confirmation 
External Reference Number 16 19 34 A/N As supplied by the [[Member]]  (a sequence 
number which remains unique to this 
Transaction as long as it is in the system)  
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Filler  4 50 53 A/N Always = Spaces  
[[Member]] [[ID]] 4 54 57 A/N [[GSD]] [[Member]] [[ID]] Number  
Filler  6 58 63 A/N Always = Spaces  
Secondary External 
Reference Number 
16 64 79 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  4 80 83 A/N Always = Spaces  
Status 9 84 92 A/N Always = Spaces. Reserved for Future Use 
Forward Mark  18 93 110 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“  
Credit / Debit 1 111 111 A/N “C” = Credit, “D” = Debit  
Finance Mark  18 112 129 A/N Format same as Forward Mark  
Credit / Debit 1 130 130 A/N “C” = Credit, “D” = Debit  
Filler  109 131 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
 
  

---

## Page 24

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 24 
Record Type 49 – Paired-Off Obligation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 49 Always = Paired Off Obligation  
Transaction [[ID]]  11 19 29 A/N The [[ID]] assigned to this Obligation by [[GSD]]. 
Format is XXXXXX-XXXX 
[[Member]] [[ID]] 4 30 33  [[GSD]] [[Member]] [[ID]] Number 
Filler  4 34 39 A/N Always = Spaces  
Transaction Code  1 40 40 A/N “L” = Long, “S” = Short  
[[CUSIP]] Number 9 41 49 A/N [[CUSIP]] Number 
Filler  6 50 55 A/N Always = Spaces  
Quantity Cleared  18 56 73 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“  
Amount Cleared  18 74 91 A/N Format same as Quantity  Cleared 
Filler  18 92 109 A/N Always = Spaces  
Transaction [[ID]] of Paired 
Obligation  
11 130 140 A/N The [[ID]] assigned to the Obligation that this 
Obligation is paired with . Format is 
XXXXXX-XXXX 
Filler  99 141 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
 
  

---

## Page 25

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
[[GSD]] [[EOD]] Netting MRO Formats 25 
Application Trailer Record 
Field Name Length Start End Type Comments 
Trailer [[ID]] 5 1 5 A/N Always = “TRAIL” 
Number of Records  5 6 10 N Total Number of 240 Byte output records  in 
file 
Checksum  5 11 15 A/N XOR of Checksums of all other data records 
(For Future Use)  
Filler  225 16 240 A/N Always = Spaces  
 
 
 

---

## Page 26

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
Appendices 26 
APPENDICES 
List of Appendices 
A. Message Flows (Reserved for Future Use) 
B. Message Samples (Reserved for Future Use) 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 27

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
Appendices 27 
Appendix A – Message Flows (Reserved for Future Use) 
This appendix of Message Flows contains detailed diagrams depicting the flows of MRO Record Types sent by  
[[GSD]] to its Members for various transaction related scenarios. 
 
 
 
  

---

## Page 28

[[GSD]] Netting MRO Format ([[EOD]]) – File 1019 – 240 Byte 
Appendices 28 
Appendix B – Message Samples (Reserved for Future Use) 
This appendix of Message Samples provides examples of a various MRO Record Types sent by [[GSD]] to its 
Members.   

---

## Page 29

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 