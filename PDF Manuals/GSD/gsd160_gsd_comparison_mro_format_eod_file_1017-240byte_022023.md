---
title: "GSD Comparison MRO Format (EOD) File 1017 – 240 Byte"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd160_gsd_comparison_mro_format_eod_file_1017-240byte_022023.pdf"
pages: 35
size: "506.6 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD Comparison MRO Format (EOD) File 1017 – 240 Byte

**Original File:** [gsd160_gsd_comparison_mro_format_eod_file_1017-240byte_022023.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd160_gsd_comparison_mro_format_eod_file_1017-240byte_022023.pdf)  
**Category:** GSD  
**Total Pages:** 35  
**File Size:** 506.6 KB  

---

## Page 1

 
 
 
[[FICC]] – [[GSD]] 
[[GSD]] COMPARISON MRO FORMAT ([[EOD]]) FILE 1017 – 240 BYTE 
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
Publication Code:  GSD160 
Service: [[FICC]] – [[GSD]]   
Title: [[GSD]] Comparison  MRO Format ([[EOD]]) File 1017 – 240 Byte 
 
 
The [[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte (hereinafter, the " document ") is provided as a 
convenience to [[Member]] s and is for information purposes only. Although [[FICC]] may make this document  available to 
Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have a continuing 
obligation to make available this document  or other related information of a certain type.   
 
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
[[GSD]] [[EOD]] Comparison MRO Formats ................................................................................................ 7 
Application Header Record............................................................................................................... 7 
Recor d Type  01  – Comparison Confirmation....................................................................................... 8 
Recor d Type  02  – Modified Compared Confirmation .......................................................................... 10 
Recor d Type  03  – Canc ellatio n Co nfirmatio n .................................................................................... 14 
Recor d Type  06  – XREF Modified Confirmation................................................................................. 15 
Recor d Type  07  – Trade Inp ut Acc epted  Co nfirmatio n........................................................................ 16 
Recor d Type  09  – Trade Input Rejected Confirmation ........................................................................ 19 
Recor d Type  10  – Canc ellatio n Rejec ted  Co nfirmation ....................................................................... 22 
Recor d Type  13  – Canc el Req ues ted Co nfirmatio n ............................................................................ 23 
Recor d Type  22  – Comparison Requested Confirmation ..................................................................... 24 
Recor d Type  24  – Uncomp ared  D eleted Co nf irmatio n ........................................................................ 26 
Recor d Type  29  – Rec alc ulated  Mo ney  for Yield  Trad e ...................................................................... 28 
Recor d Type  32  – Expan de d C omparison  C on fir mation ...................................................................... 29 
Recor d Type  33  – C ommission  Modifie d C on firmation........................................................................ 30 
Application Trailer Record .............................................................................................................. 31 
Appendices ....................................................................................................................................32  
List of Appendices ........................................................................................................................ 32 
Appendix A – Message Flows (Reserved for Future Use) .................................................................. 33 
Appendix B – Message Samples (Reserved for Future Use) .............................................................. 34 
 

---

## Page 4

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
Overview 4 
OVERVIEW 
End of Day ([[EOD]]) Comparison Machine Readable Output (MRO) Specification 
This document provides Members of the Fixed Income Clearing Corporation‘s (“[[FICC]]”) Government [[securities]] 
Division (“[[GSD]]”) with machine readable output (MRO) specifications for [[GSD]] comparison related record types 
used to support [[GSD]]’s products and services.  
Audience 
This document was written for systems and development personnel including managers, analysts and 
programmers of [[GSD]] [[Member]] firms. It presumes readers are familiar with technical concepts and terms as 
well as having a [[BASIC]] understanding of [[GSD]]'s products and services. 
Communication 
For information on [[FICC]] Connectivity, please contact [[FICC]] Integration at ficcintegration@[[DTCC]].com. 
  

---

## Page 5

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
Introduction 5 
INTRODUCTION 
This document provides the formats for the [[GSD]] comparison related record types used to support [[GSD]]’s 
products and services, enabling [[GSD]] Members to receive trade status messages.  
Messages discussed in this document will give Members the ability to take in important trade status information 
and manage their trades at end of day. 
It should be noted that this document is a technical specification and is not, in any way, intended to 
communicate legal definitions as to when trades are guaranteed or novated by [[GSD]]. Members should refer to 
the [[FICC]] [[GSD]] Rulebook for such information. 
For additional service details, please refer to the Clearing Services > Fixed Income – [[GSD]] section available at 
www.[[DTCC]].com. 

---

## Page 6

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
Description of the Logical Detail Records 6 
DESCRIPTION OF THE LOGICAL DETAIL RECORDS 
A logical record is made up of one or more 240 Byte physical records. The first 16 Bytes of each physical 
record consists of four fields, identified with asterisks (**) in the example below, which are referred to in the 
description of each record type as the STANDARD 16 BYTES. 
First 240 Byte Record 
Field Name Length Start End Type Comments 
Physical Record Number **  5 1 5 N Sequential number of the physical record 
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
 01 – Compared  
 02 – Modified Compared 
 03 – Canceled, etc..  
Machine Readable Only  
Output 
222 19 240 A/N Refer to the description of each Record 
Type  
 
  

---

## Page 7

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 7 
[[GSD]] [[EOD]] COMPARISON MRO FORMATS 
Application Header Record 
Field Name Length Start End Type Comments 
Character Set 1 1 1 A/N "A" = ASCII, "E" = EBCDIC 
Block Size 5 2 6 N Block size of largest record  
Source Name 4 7 10 A/N “IONS” 
Filler  8 11 18 A/N  Always = Spaces  
Destination Name 4 19 22 A/N  [[GSD]] [[Member]] [[ID]] Number  
Filler  8 23 30 A/N Always = Spaces  
Date/Time 22 31 52 A/N DD-MMM-YYYY HH:MM:SS:H 
 i.e., 19-JAN-2021 22:45:15:2 
Filler  188 53 240 A/N Always = Spaces  
 
  

---

## Page 8

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 8 
Record Type 01 – Comparison Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 01 Always = Comparison  Confirmation  
External Reference Number  16 19 34 A/N As supplied by the [[Member]]  (a sequence 
number which remains unique to this 
Transaction as long as it is in the system)  
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Expected [[settlement]] 1 1 50 50 A/N Expected [[settlement]]: 
 “T” = Trade for Trade  
 “N” = Trade Expected to Net  
Contra’s External 
Reference Number 
16 51 66 A/N Cross reference to Contra’s side 
Filler  4 67 70 A/N Always = Spaces  
Expanded Comparison  1 71 71 A/N Cash-only Members: 
 “Y” = Additional Output  
“N” = No Additional Output  
Repo Members: 
 Always = Spaces  
Locked In Trade  1 72 72 A/N  “X” = Submitter of Locked -In Trade 
“L” = Recipient of Locked -In Trade 
 “  ” = Not Locked -In Trade 
Associated External 
Reference Number 2 
16 73 88 A/N Cross reference to the 2 nd [[Member]] side of 
the Par Summarized Trade 
Filler  4 89 92 A/N Always = Spaces  
Additional Contra External 
Reference Number2 
16 93 108 A/N Cross reference to the 2 nd contra side of the 
Par Summarized Trade 
Filler  4 109 112 A/N Always = Spaces  
Secondary External 
Reference Number 
16 113 128 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only.  
 
1 "Expected [[settlement]]" is only an estimate of netting eligibility. The "Transaction in Net" MRO, Record Type 
17,  should be used as final confirmation of whether the transaction was actually included in the net. See 
 the netting MRO layout specification for detail. 
2 The Associated External Reference and Additional Contra’s External Reference, found on the Expanded 
Comparison Confirmation (Record Type 32), are included in the Record Type 01 for repo members, who don’t 
receive the Record Type 32. Cash members will continue to receive the Record Type 32 confirmation, and the 
fields mentioned above will not appear in their Record Type 01’s. 

---

## Page 9

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 9 
Field Name Length Start End Type Comments 
Filler  4 129 132 A/N Always = Spaces  
Initiated By  4 133 136 A/N Filled in with the word “SUB” if the 
confirmation resulted from a [[CUSIP]] 
Substitution: Otherwise , field is kept blank  
Identifier  6 137 142 N Zero Filled Number. i.e., “000175”  
Filler  97 143 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
  

---

## Page 10

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 10 
Record Type 02 – Modified Compared Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 02 Always = Compar ed with Modification  
External Reference Number  16 19 34 A/N XREF As supplied by the [[Member]]   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
[[Broker]] Reference Number  16 50 65 A/N The [[Broker]] Reference supplied by the 
[[Member]] 
Filler  4 66 69 A/N Always = Spaces  
Transaction Type  4 70 73 A/N Buy / Sell Trades:  
 “BUY” or “SELL” 
Repo / Reverse Repo Trades:  
“REPO” or “REVR”  
Trade Date 10 74 83 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 84 93 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 94 102 A/N [[CUSIP]] Number 
Filler  6 103 108 A/N Always = Spaces  
Quantity  18 109 126 A/N Left Justified Blank Fille d, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “  
Price / Repo Rate 14 127 140 A/N Buy / Sell Trades:  
 Price as given to [[GSD]]  
Repo / Reverse Repo Trades:  
Repo Rate as given to [[GSD]]  
Price Method 1 141 141 A/N Buy / Sell Trades:  
 “D” = Discount  
 “P” = Price  
 “Y” = Yield  
 Repo / Reverse Repo Trades:  
“R” = Repo Rate  
Amount 18 142 159 A/N Format same as Quantity  
Commission  11 160 170 A/N As supplied by the [[Member]]   
Contra [[ID]] 4 171 174 A/N Contra’s [[GSD]] [[ID]] Number  
Filler  6 175 180 A/N Always = Spaces  
XREF Modified  1 181 181 A/N “Y” = Yes, “  “ = No  
[[Broker]] XREF Modified  1 182 182 A/N “Y” = Yes, “  “ = No  

---

## Page 11

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 11 
Field Name Length Start End Type Comments 
Transaction Type Modified 1 183 183 A/N “Y” = Yes, “  “ = No  
Trade Date Modified  1 184 184 A/N “Y” = Yes, “  “ = No  
[[settlement]] Date Modified  1 185 185 A/N “Y” = Yes, “  “ = No  
[[CUSIP]] Number Modified  1 186 186 A/N “Y” = Yes, “  “ = No  
Quantity Modified  1 187 187 A/N “Y” = Yes, “  “ = No  
Price Modified  1 188 188 A/N “Y” = Yes, “  “ = No  
Price Method Modified 1 189 189 A/N “Y” = Yes, “  “ = No  
Amount Modified 1 190 190 A/N “Y” = Yes, “  “ = No  (Modified or input 
amount did not match  contra amount, but 
fell within the tolerance, so amount was 
changed to match contra)  
Commission Modified 1 191 191 A/N “Y” = Yes, “  “ = No  
Contra [[ID]] Modified 1 192 192 A/N “Y” = Yes, “  “ = No  
Filler  6 193 198 A/N Always = Spaces  
Expected [[settlement]] 3 1 199 199 A/N Expected [[settlement]]: 
 “T” = Trade for Trade  
“N” = Trade Expected to Net  
Executing Firm  5 200 204 A/N Executing firm associated with [[Member]]  
Executing Firm Modified  1 205 205 A/N “Y” = Yes, “  “ = No  
Contra’s Executing Firm  5 206 210 A/N Executing firm associated with Contra  
Contra’s Executing Firm 
Modified  
1 211 211 A/N “Y” = Yes, “  “ = No  
Contra’s External 
Reference Number 
16 212 227 A/N Cross reference to contra’s side  
Filler  4 228 231 A/N Always = Spaces  
Expanded Comparison  1 232 232 A/N Cash-only Members:  
 “Y” = Additional Output  
“N” = No Additional Output  
Repo Members: 
Always = Spaces  
Filler  7 233 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
 
3  "Expected [[settlement]]" is only an estimate of netting eligibility. The "Transaction in Net" MRO, Record Type 
17,  should be used as final confirmation of whether the transaction was actually included in the net. See 
 the netting MRO layout specification for detail. 

---

## Page 12

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 12 
Field Name Length Start End Type Comments 
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 02 Always = Compar ed with Modification  
External Reference Number  16 19 34 A/N Matches the XREF listed in the 1st record   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N Matches the Transaction [[ID]] listed in the 1st 
record  
Associated External 
Reference Number 4 
16 50 65 A/N Cross reference to the 2 nd [[Member]] side of 
the Par Summarized Trade 
Filler  4 66 69 A/N Always = Spaces  
Additional Contra External 
Reference Number
4 
16 70 85 A/N Cross reference to the 2 nd contra side of the 
Par Summarized Trade 
Filler  4 86 89 A/N Always = Spaces  
Start Amount  18 90 107 A/N Left Justified Blank Fille d, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ . 
Applies to Repo Transactions only  
Start Date 10 108 117 A/N Format is MM/DD/YYYY. Apples to Repo 
Transactions only  
Give Up [[Broker]]  10 118 127 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Secondary External 
Reference Number 
16 128 143 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  4 144 147 A/N Always = Spaces  
Start Amount Modified  1 148 148 A/N “Y” = Yes, “  “ = No . Applies to Repo 
Transactions only  
Start Date Modified  1 149 149 A/N “Y” = Yes, “  “ = No . Applies to Repo 
Transactions only  
 
4 The Associated External Reference and Additional Contra’s External Reference, found on the Expanded 
Comparison Confirmation (Record Type 32), are included in the Record Type 01 for repo members, who don’t 
receive the Record Type 32. Cash members will continue to receive the Record Type 32 confirmation, and the 
fields mentioned above will not appear in their Record Type 01’s. 

---

## Page 13

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 13 
Field Name Length Start End Type Comments 
Give Up [[Broker]] Modified  1 150 150 A/N “Y” = Yes, “  “ = No . Applies to Repo 
Transactions only  
Secondary XREF Modified  1 151 151 A/N “Y” = Yes, “  “ = No . Applies to Repo 
Transactions only  
Filler  88 152 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
  

---

## Page 14

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 14 
Record Type 03 – Cancellation Confirmation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 03 Always = Cancellation Confirmation  
External Reference Number  16 19 34 A/N XREF As supplied by the [[Member]]   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Command Type 5 4 50 53 A/N  “CAN” = Cancellation  
“REPL” = Replacement  
Locked In Trade  1 54 54 A/N  “X” = Submitter of Locked -In Trade 
“L” = Recipient of Locked -In Trade 
 “  ” = Not Locked -In Trade 
Secondary External 
Reference Number 
16 55 70 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  4 71 74 A/N Always = Spaces  
Initiated By  4 75 78 A/N Filled in with the word “SUB” if the 
confirmation resulted from a [[CUSIP]] 
Substitution: Otherwise , field is kept blank  
Identifier  6 79 84 A/N Zero Filled Number. i.e., “000175”  
Filler  155 85 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
  
 
5 This is used to inform Members whether a cancel, or a cancel replace, generated the cancellation 
 confirmation. 

---

## Page 15

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 15 
Record Type 06 – XREF Modified Confirmation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 06 Always = XREF Modified Confirmation  
New External Reference 
Number 
16 19 34 A/N New XREF As supplied by the [[Member]]   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Previous External 
Reference Number 
16 50 65 A/N Previous XREF, replaced by new XREF 
Filler  4 66 69 A/N Always = Spaces  
Secondary External 
Reference Number 
16 70 85 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  154 86 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
 
  

---

## Page 16

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 16 
Record Type 07 – Trade Input Accepted Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 07 Always = Trade Input Accepted 
Confirmation 
External Reference Number  16 19 34 A/N XREF As supplied by the [[Member]]   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
[[Broker]] Reference Number  16 50 65 A/N The [[Broker]] Reference supplied by the 
Contra [[Member]] 
Filler  4 66 69 A/N Always = Spaces  
Transaction Type  4 70 73 A/N Buy / Sell Trades:  
 “BUY” or “SELL” 
Repo / Reverse Repo Trades:  
“REPO” or “REVR”  
Trade Date 10 74 83 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 84 93 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 94 102 A/N [[CUSIP]] Number 
Filler  6 103 108 A/N Always = Spaces  
Quantity  18 109 126 A/N Left Justified Blank Fille d, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “  
Price / Repo Rate 14 127 140 A/N Buy / Sell Trades:  
 Price as submitted by Contra 
Repo / Reverse Repo Trades:  
Repo Rate as submitted by Contra 
Price Method 1 141 141 A/N Buy / Sell Trades:  
 “D” = Discount  
 “P” = Price  
 “Y” = Yield  
 Repo / Reverse Repo Trades:  
“R” = Repo Rate  
Amount 18 142 159 A/N Format same as Quantity  
Commission  11 160 170 A/N As supplied by the [[Member]]   
Contra [[ID]] 4 171 174 A/N Contra’s [[GSD]] [[ID]] Number  
Filler  10 175 184 A/N Always = Spaces  
Origination  1 185 185 A/N “T” = Other Input  

---

## Page 17

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 17 
Field Name Length Start End Type Comments 
“N” = Screen Input  
Command  4 186 189 A/N “INST” = Instruct                                     
“REPL” = Replace 
Trade Time 6 190 195 A/N Format is HHMMSS 
Executing Firm  5 196 200 A/N Executing firm associated with [[Member]]  
Contra’s Executing Firm  5 201 205 A/N Executing firm associated with Contra  
Locked In Trade  1 206 206 A/N  “X” = Submitter of Locked -In Trade 
“L” = Recipient of Locked -In Trade 
 “  ” = Not Locked -In Trade 
Identifier  6 207 212 N Zero Filled Number. i.e., “000175”  
Filler  27 213 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 07 Always = Trade Input Accepted 
Confirmation 
External Reference Number  16 19 34 A/N Matches the XREF listed in the 1st record   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N Matches the Transaction [[ID]] listed in the 1st 
record  
Start Amount  18 50 67 A/N Left Justified Blank Fille d, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “. 
Applies to Repo Transactions only  
Start Date 10 68 77 A/N Format is MM/DD/YYYY. Apples to Repo 
Transactions only  
Give Up [[Broker]]  10 78 87 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Secondary External 
Reference Number 
16 88 103 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  4 104 107 A/N Always = Spaces  

---

## Page 18

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 18 
Field Name Length Start End Type Comments 
Initiated By  4 108 111 A/N Filled in with the word “SUB” if the 
confirmation resulted from a [[CUSIP]] 
Substitution: Otherwise , field is kept blank  
Filler  128 112 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
  

---

## Page 19

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 19 
Record Type 09 – Trade Input Rejected Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 09 Always = Trade Input Reject ed 
Confirmation 
Password  12 19 30 A/N As supplied by the [[Member]]   
External Reference Number  16 31 46 A/N XREF As supplied by the [[Member]]   
Filler  4 47 50 A/N Always = Spaces  
Command  4 51 54 A/N As supplied by the [[Member]]   
Transaction Type  4 55 58 A/N As supplied by the [[Member]]   
[[Broker]] Reference Number  16 59 74 A/N As supplied by the [[Member]]   
Filler  4 75 78 A/N Always = Spaces  
Trade Date 10 79 88 A/N As supplied by the [[Member]]   
[[settlement]] Date 10 89 98 A/N As supplied by the [[Member]]   
[[CUSIP]] Number 9 99 107 A/N As supplied by the [[Member]]   
Filler  6 108 113 A/N As supplied by the [[Member]]   
Quantity  18 114 131 A/N As supplied by the [[Member]]   
Price / Repo Rate 14 132 145 A/N As supplied by the [[Member]]   
Price Method  1 146 146 A/N As supplied by the [[Member]]   
Amount 18 147 164 A/N As supplied by the [[Member]]   
Commission  11 165 175 A/N As supplied by the [[Member]]   
Contra [[ID]] 4 176 179 A/N As supplied by the [[Member]]   
Filler  6 180 185 A/N Always = Spaces  
Password Error 1 186 186 A/N = “Y” If error 
Command Error  1 187 187 A/N = “Y” If error 
Transaction Type Error  1 188 188 A/N = “Y” If error 
[[Broker]] Reference Number 
Error 
1 189 189 A/N = “Y” If error 
Trade Date Error  1 190 190 A/N = “Y” If error 
[[settlement]] Date Error  1 191 191 A/N = “Y” If error 
[[CUSIP]] Number Error  1 192 192 A/N = “Y” If error 
Quantity Error  1 193 193 A/N = “Y” If error 
Price Error 1 194 194 A/N = “Y” If error 

---

## Page 20

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 20 
Field Name Length Start End Type Comments 
Price Method Error  1 195 195 A/N = “Y” If error 
Amount Error  1 196 196 A/N = “Y” If error 
Contra [[ID]] Error 1 197 197 A/N = “Y” If error 
Commission Error  1 198 198 A/N = “Y” If error 
Internal Process Error 1 199 199 A/N = “Y” If error 
External Reference Number 
Error 
1 200 200 A/N = “Y” If error 
[[Member]] [[ID]]  4 201 204 A/N As supplied by the [[Member]]   
Filler  6 205 210 A/N Always = Spaces  
Executing Firm  5 211 215 A/N As supplied by the [[Member]]   
Executing Firm Error 1 216 216 A/N = “Y” If error 
Contra’s Executing Firm  5 217 221 A/N As supplied by the [[Member]]   
Contra Executing Firm 
Error 
1 222 222 A/N = “Y” If error 
Filler  17 223 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 09 Always = Trade Input Rejected 
Confirmation 
External Reference Number  16 19 34 A/N Matches the XREF listed in the 1st record   
Filler  4 35 38 A/N Always = Spaces  
Start Amount  18 39 56 A/N As supplied by the [[Member]]. Apples to Repo 
Transactions only  
Start Date 10 57 66 A/N As supplied by the [[Member]]. Apples to Repo 
Transactions only  
Give Up [[Broker]]  10 67 76 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  

---

## Page 21

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO Formats 21 
Field Name Length Start End Type Comments 
Secondary External 
Reference Number 
16 77 92 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  4 93 96 A/N Always = Spaces  
Start Amount Error  1 97 97 A/N = “Y” If error. Applies to Repo Transactions 
only  
Start Date Error  1 98 98 A/N = “Y” If error. Applies to Repo Transactions 
only  
Give Up [[Broker]] Error 1 99 99 A/N = “Y” If error. Applies to Repo Transactions 
only  
Secondary External 
Reference Number Error  
1 100 100 A/N = “Y” If error. Applies to Repo Transactions 
only  
Filler  139 101 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
  

---

## Page 22

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 22 
Record Type 10 – Cancellation Rejected Confirmation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 10 Always = Cancellation Reject ed 
Confirmation 
Password  12 19 30 A/N As supplied by the [[Member]]  
External Reference Number  16 31 46 A/N XREF As supplied by the [[Member]]   
Filler  4 47 50 A/N Always = Spaces  
Transaction [[ID]]  11 51 61 A/N As supplied by the [[Member]]  
Filler  178 62 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
  

---

## Page 23

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 23 
Record Type 13 – Cancel Requested Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 13 Always = Cancellation Requested 
Confirmation 
External Reference Number  16 19 34 A/N XREF as supplied by the [[Member]]   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Contra’s Transaction [[ID]]  11 50 60 A/N The [[ID]] assigned to the Contra side of the 
Transaction by [[GSD]]. Format is XXXXXX-
XXXX 
Contra [[ID]] 4 61 64 A/N [[GSD]] [[ID]] of [[Member]] requesting cancellation 
Filler  6 65 70 A/N Always = Spaces  
Secondary External 
Reference Number 
16 71 86 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  153 87 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
  

---

## Page 24

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 24 
Record Type 22 – Comparison Requested Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 22 Always = Compar ison Requested  
External Reference Number  16 19 34 A/N XREF as supplied by the [[Member]]   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
[[Broker]] Reference Number  16 50 65 A/N The [[Broker]] Reference supplied by the 
Contra  [[Member]] 
Filler  4 66 69 A/N Always = Spaces  
Transaction Type  4 70 73 A/N Buy / Sell Trades:  
 “BUY” or “SELL” 
Repo / Reverse Repo Trades:  
“REPO” or “REVR” 
Trade Date 10 74 83 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 84 93 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 94 102 A/N [[CUSIP]] Number 
Filler  6 103 108 A/N Always = Spaces  
Quantity  18 109 126 A/N Left Justified Blank Fille d, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “  
Price / Repo Rate 14 127 140 A/N Buy / Sell Trades:  
 Price as submitted by Contra 
Repo / Reverse Repo Trades:  
Repo Rate as submitted by Contra 
Price Method  1 141 141 A/N Buy / Sell Trades:  
 “D” = Discount  
 “P” = Price  
 “Y” = Yield  
 Repo / Reverse Repo Trades:  
“R” = Repo Rate  
Amount 18 142 159 A/N Format same as Quantity  
Commission  11 160 170 A/N As supplied by Contra [[Member]]  
Contra [[ID]] 4 171 174 A/N Contra’s [[GSD]] [[ID]] Number  
Filler  10 175 184 A/N Always = Spaces  
Last Time Flag  1 185 185 A/N “Y” if trade will be deleted tonight, otherwise 
“N” 

---

## Page 25

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 25 
Field Name Length Start End Type Comments 
Filler  4 186 189 A/N Always = Spaces  
Trade Time 6 190 195 A/N Format is HHMMSS 
Executing Firm  5 196 200 A/N Executing firm associated with [[Member]]  
Contra’s Executing Firm  5 201 205 A/N Executing firm associated with Contra  
Filler  34 206 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 22 Always = Compar ison Requested  
External Reference Number  16 19 34 A/N Matches the XREF listed in the 1st record   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N Matches the Transaction [[ID]] listed in the 1st 
record  
Start Amount  18 50 67 A/N Left Justified Blank Fille d, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “. 
Applies to Repo Transactions only  
Start Date 10 68 77 A/N Format is MM/DD/YYYY. Apples to Repo 
Transactions only  
Give Up [[Broker]]  10 78 87 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Secondary External 
Reference Number 
16 88 103 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  136 104 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
  

---

## Page 26

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 26 
Record Type 24 – Uncompared Deleted Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 24 Always = Uncompared Deleted  
External Reference Number  16 19 34 A/N XREF as supplied by the [[Member]]   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
[[Broker]] Reference Number  16 50 65 A/N The [[Broker]] Reference supplied by the 
Contra [[Member]] 
Filler  4 66 69 A/N Always = Spaces  
Transaction Type  4 70 73 A/N Buy / Sell Trades:  
 “BUY” or “SELL” 
Repo / Reverse Repo Trades:  
“REPO” or “REVR”  
Trade Date 10 74 83 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 84 93 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 94 102 A/N [[CUSIP]] Number 
Filler  6 103 108 A/N Always = Spaces  
Quantity  18 109 126 A/N Left Justified Blank Fille d, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “  
Price / Repo Rate 14 127 140 A/N Buy / Sell Trades:  
 Price as submitted by Contra 
Repo / Reverse Repo Trades:  
Repo Rate as submitted by Contra 
Price Method  1 141 141 A/N Buy / Sell Trades:  
 “D” = Discount  
 “P” = Price  
 “Y” = Yield  
 Repo / Reverse Repo Trades:  
“R” = Repo Rate  
Amount 18 142 159 A/N Format same as Quantity  
Commission  11 160 170 A/N As supplied by the [[Member]]   
Contra [[ID]] 4 171 174 A/N Contra’s [[GSD]] [[ID]] Number  
Filler  10 175 184 A/N Always = Spaces  
Origination  1 185 185 A/N “T” = Other Input  
“N” = Screen Input  

---

## Page 27

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 27 
Field Name Length Start End Type Comments 
Filler  4 186 189 A/N Always = Spaces  
Trade Time 6 190 195 A/N Format is HHMMSS 
Executing Firm  5 196 200 A/N Executing firm associated with [[Member]]  
Contra’s Executing Firm  5 201 205 A/N Executing firm associated with Contra  
MRO Generation Time 6 206 211 A/N Format is HHMMSS 
Filler  28 212 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 24 Always = Uncompared Deleted  
External Reference Number  16 19 34 A/N Matches the XREF listed in the 1st record   
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N Matches the Transaction [[ID]] listed in the 1st 
record  
Start Amount  18 50 67 A/N Left Justified Blank Fille d, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “. 
Applies to Repo Transactions only  
Start Date 10 68 77 A/N Format is MM/DD/YYYY. Apples to Repo 
Transactions only  
Give Up [[Broker]]  10 78 87 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Secondary External 
Reference Number 
16 88 103 A/N As supplied by the [[Member]]. Applies to 
Repo Transactions only  
Filler  136 104 239 A/N Always = Spaces  
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
  

---

## Page 28

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 28 
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
Amount 11 51 61 A/N Right Justified Blank Fille d, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“  
 Recalculated amount for Yield Trade 
Compared on Yield 1 62 62 A/N “Y” = Yes, “  “ = No  
Compared on Money  1 63 63 A/N “Y” = Yes, “  “ = No  
Deleted Tonight  1 64 64 A/N “Y” = Yes, “  “ = No  
Filler  175 65 239 A/N Always = Spaces  
Confirmation Continued  1 240 240 A/N “  ” = Only record (no overflow record) 
“1” = First of many records (if overflow 
records are required)  
“2” = Last of many records (if 2 or more 
records are required)  
 
Note: 
If you select to receive Record Type 29 for comparison, the system will not allow you to receive Record Type 29 for netting.  
 
 
 
 
 
 
 

---

## Page 29

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 29 
Record Type 32 – Expanded Comparison Confirmation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 32 Always = Expanded Compar ison 
Confirmation 
External Reference Number  16 19 34 A/N XREF as supplied by the [[Member]]  
Filler  4 35 38 A/N Always = Spaces  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by  
[[GSD]]. Format is XXXXXX-XXXX 
Associated External 
Reference Number 
16 50 65 A/N Cross reference to the 2 nd [[Member]] side of 
the Par Summarized Trade 
Filler  4 66 69 A/N Always = Spaces  
Contra External Reference 
Number 
16 70 85 A/N Cross reference to the 1
st contra side of the 
Par Summarized Trade 
Filler  4 86 89 A/N Always = Spaces  
Additional Contra External 
Reference Number 
16 90 105 A/N Cross reference to the 2
nd contra side of the 
Par Summarized Trade 
Filler  135 106 240 A/N Always = Spaces  
 
Note: 
The Expanded Comparison Confirmation is generated only for cash market modified, or modified  compared, trades 
submitted by Members who are not Repo Service Members.   

---

## Page 30

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 30 
Record Type 33 – Commission Modified Confirmation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records  
Record [[ID]] 2 17 18 N 33 Always = Commission Modified 
Confirmation 
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
If you select to receive Record Type 33 for comparison, the system will not allow you to receive Record Type 33 for netting.  
  

---

## Page 31

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
[[GSD]] [[EOD]] Comparison MRO F ormats 31 
Application Trailer Record 
Field Name Length Start End Type Comments 
Trailer [[ID]] 5 1 5 A/N Always = “TRAIL” 
Number of Records  5 6 10 N Total Number of 240 Byte output records in 
file 
Checksum  5 11 15 A/N XOR of Checksums of all other data records 
(For Future Use)  
Filler  225 16 240 A/N Always = Spaces  
 
 

---

## Page 32

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
Appendices 32 
APPENDICES 
List of Appendices 
A. Message Flows (Reserved for Future Use) 
B. Message Samples (Reserved for Future Use) 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 33

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
Appendices 33 
Appendix A – Message Flows (Reserved for Future Use) 
This appendix of Message Flows will contain detailed diagrams depicting the flows of MRO Record Types sent 
by [[GSD]] to its Members for various transaction related scenarios. 
 
 
 
  

---

## Page 34

[[GSD]] Comparison MRO Format ([[EOD]]) File 1017 – 240 Byte 
Appendices 34 
Appendix B – Message Samples (Reserved for Future Use) 
This appendix of Message Samples will provide examples of a various MRO Record Types sent by [[GSD]] to its 
Members.   

---

## Page 35

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 