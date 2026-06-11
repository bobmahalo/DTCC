---
title: "GCF Comparison MRO and Print Image Output Format - File 752"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd157_gcf_comparison_mro_and_print_image_output_format_file_752_112021.pdf"
pages: 34
size: "475.5 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GCF Comparison MRO and Print Image Output Format - File 752

**Original File:** [gsd157_gcf_comparison_mro_and_print_image_output_format_file_752_112021.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd157_gcf_comparison_mro_and_print_image_output_format_file_752_112021.pdf)  
**Category:** GSD  
**Total Pages:** 34  
**File Size:** 475.5 KB  

---

## Page 1

  
 
 
 
 
[[FICC]] – [[GSD]] 
GCF COMPARISON MRO AND PRINT IMAGE OUTPUT FORMAT – FILE 752 
VERSION 2.0 
NOVEMBER 2021 
 


---

## Page 2

 
  
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: November 2021 
Publication Code: GSD157 
Service: [[FICC]] – [[GSD]]   
Title: GCF Comparison MRO and Print Image Output Format – File 752 
 
 
The GCF Comparison MRO and Print Image Output Format – File 752 (hereinafter, the "document") is provided as a 
convenience to Members and is for information purposes only. Although [[FICC]] may make this document available to 
Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have a continuing 
obligation to make available this document or other related information of a certain type.  
 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose 
of any information provided to Members in this document, which is provided as-is. [[FICC]] shall not be liable for any 
loss related to such information (or the act or process of providing such information) resulting directly or 
indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
 
Further, the information contained in this document is subject to change. Members and other authorized users of the 
document will find the most current version of the document on [[DTCC]]’s Learning Center site, www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow 
[[FICC]]’s most current document. 
 
 

---

## Page 3

 
  
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 4 
Introduction .......................................................................................................................................................... 5 
Description of the Logical Detail Records ......................................................................................................... 6 
First 2,048 Byte Record ...................................................................................................................................... 6 
GCF Comparison MRO and Print Image Output Formats ................................................................................ 8 
Application Header Record ................................................................................................................................. 8 
Record Type 01 – Comparison Confirmation ..................................................................................................... 9 
Record Type 02 – Modified Compared Confirmation ....................................................................................... 12 
Record Type 03 – Cancellation Confirmation ................................................................................................... 15 
Record Type 06 – Modified Confirmation ......................................................................................................... 17 
Record Type 07 – Trade Input Accepted Confirmation .................................................................................... 19 
Record Type 09 – Trade Input Rejected Confirmation ..................................................................................... 21 
Record Type 10 – Cancellation Rejected Confirmation .................................................................................... 24 
Record Type 13 – Cancel Requested Confirmation ......................................................................................... 25 
Record Type 22 – Comparison Requested Confirmation ................................................................................. 27 
Record Type 24 – Uncompared Deleted Confirmation ..................................................................................... 29 
Record Type 40 – Affirmation Accepted Confirmation ..................................................................................... 31 
Application Trailer Record ................................................................................................................................ 33 
 

---

## Page 4

GCF Comparison MRO and Print Image Output Format – File 752 
Overview 4 
 
OVERVIEW 
General [[collateral]] Finance (GCF) Comparison Machine Readable Output (MRO) and Print Image Output 
Specification 
This document provides Members of the Fixed Income Clearing Corporation‘s (“[[FICC]]”) Government [[securities]] 
Division (“[[GSD]]”) that participate in the General [[collateral]] Finance Repo (GCF Repo®) Service and the 
Centrally Cleared Institutional Tri-party (CCIT™) Service with machine readable output (MRO) and print image 
output specifications for GCF comparison related record types used to support [[GSD]]’s GCF Repo Service and 
CCIT Service.  
Audience 
This document was written for systems and development personnel including managers, analysts and 
programmers of [[GSD]] [[Member]] firms. It presumes readers are familiar with technical concepts and terms as 
well as having a [[BASIC]] understanding of [[GSD]]'s products and services. 
Communication 
For information on [[FICC]] Connectivity, please contact [[FICC]] Integration at ficcintegration@[[DTCC]].com. 
  

---

## Page 5

GCF Comparison MRO and Print Image Output Format – File 752 
Introduction 5 
 
INTRODUCTION 
This document provides the formats for the GCF comparison related record types used to support [[GSD]]’s GCF 
Repo Service and CCIT Service, enabling [[GSD]] Members that participate in those services to receive trade 
status messages. 
The upcoming sections within this document will describe the GCF Comparison MRO file number 752 which 
include the following record types: 
• Description of the Logical Details Records 
• Application Header Record 
• Record Type 01 – Comparison Confirmation 
• Record Type 02 – Modified Compared Confirmation 
• Record Type 03 – Cancellation Confirmation 
• Record Type 06 – Modified Confirmation 
• Record Type 07 – Trade Input Accepted Confirmation 
• Record Type 09 – Trade Input Rejected Confirmation 
• Record Type 10 – Cancellation Rejected Confirmation 
• Record Type 13 – Cancel Requested Confirmation 
• Record Type 22 – Comparison Requested Confirmation 
• Record Type 24 – Uncompared Deleted Confirmation 
• Record Type 40 – Affirmation Accepted Confirmation 
• Application Trailer Record 
 
Record types discussed in this document will give Members the ability to take in important trade status 
information and manage their trades at end of day. 
It should be noted that this document is a technical specification and is not, in any way, intended to 
communicate legal definitions as to when trades are guaranteed or novated by [[GSD]]. Members should refer to 
the [[FICC]] [[GSD]] Rulebook for such information. 
For additional service details, please refer to the Clearing Services > Fixed Income – [[GSD]] section available at 
www.[[DTCC]].com
. 

---

## Page 6

GCF Comparison MRO and Print Image Output Format – File 752 
Description of the Logical Detail Records 6 
 
DESCRIPTION OF THE LOGICAL DETAIL RECORDS 
A logical record is made up of one or more 2,048 Byte physical records, depending on the size of the print 
image information. The first 16 bytes of each physical record consists of four fields, identified with asterisks (**) 
in the example below, which are referred to in the description of each record type as the STANDARD 16 
BYTES. 
First 2,048 Byte Record 
Field Name Length Start End Type Comments 
Physical Record Number ** 5 1 5 N Sequential number of the physical record 
starting with 00001 
Physical Record Length ** 5 6 10 N Not greater than 2048 
Checksum ** 5 11 15 A/N The CRC16 of the physical record  
(reserved for future use) 
Segment Location ** 1 16 16 N Where this physical record is located in the 
logical record: 
 0 = Middle Record  
 1 = First Record 
 2 = Last Record  
 3 = Only Record 
Record [[ID]] 2 17 18 N Record Type:  
 01 – Compared  
 03 – Canceled 
 06 – External Reference Modified, etc.. 
Machine Readable Only  
Output 
222 19 240 A/N Refer to the description of each Record 
Type 
Print Image 1808 241 2048 A/N Print Positioning is controlled by Carriage 
Return Line Feed (CRLF) Combinations. 
Form feeds may be imbedded after a CRLF 
Pair. Tabs may be imbedded anywhere in 
the text.  
Hex Value ASCII EBCDIC 
Carriage Return “0D” “0D” 
Form Feed “0C” “0C” 
Line Feed “0A” “25” 
Tab “05” “09” 
Tabs are set at intervals of 8:                      
8, 16, 24, 32, etc. 
 

---

## Page 7

GCF Comparison MRO and Print Image Output Format – File 752 
Description of the Logical Detail Records 7 
 
All subsequent 2,048 Byte Records 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See above 
Print Image 2032 17 2048 A/N See above 
 
The Print Image field is made up of two record types: 
1. One Header record 
2. One or more Detail records 
The descriptions for each section of the Print Image for the GCF Comparison MRO Record Types will be 
explained in upcoming sections of this document.  

---

## Page 8

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 8 
 
GCF COMPARISON MRO AND PRINT IMAGE OUTPUT 
FORMATS 
Application Header Record 
Field Name Length Start End Type Comments 
Character Set 1 1 1 A/N "A" = ASCII, "E" = EBCDIC 
Block Size 5 2 6 N Block size of largest record 
Source Name 4 7 10 A/N “GCF” 
Filler 8 11 18 A/N  Always = Spaces 
Destination Name 4 19 22 A/N  [[GSD]] [[Member]] [[ID]] Number 
Filler 8 23 30 A/N Always = Spaces 
Date/Time 22 31 52 A/N DD-MMM-YYYY HH:MM:SS:H 
 i.e., 19-JAN-2021 22:45:15:2 
Filler 1996 53 2048 A/N Always = Spaces 
 
  

---

## Page 9

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 9 
 
Record Type 01 – Comparison Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 01 Always = Comparison Confirmation 
External Reference Number 20 19 38 A/N As supplied by the [[Member]] (a sequence 
number which remains unique to this 
Transaction as long as it is in the system) 
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Expected Settlement1 1 50 50 A/N Expected [[settlement]]: 
 “T” = Trade for Trade 
 “N” = Trade Expected to Net 
Contra’s External 
Reference Number 
20 51 70 A/N Cross reference to Contra’s side 
Filler 1 71 71 A/N Always = Spaces 
Locked In Trade 1 72 72 A/N  “X” = Submitter of Locked-In Trade 
“L” = Recipient of Locked-In Trade 
 “  ” = Not Locked-In Trade 
Filler 40 73 112 A/N Always = Spaces 
Secondary External 
Reference Number 
20 113 132 A/N As supplied by the [[Member]]. 
Filler 4 133 136 A/N Always = Spaces 
Transaction Type 4 137  140 A/N “REPO” or “REVR” 
Trade Date 10 141 150 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 151 160 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 161 169 A/N [[CUSIP]] Number 
Repo Rate 14 170 183 A/N Repo Rate as given to [[GSD]] 
Amount 18 184 201 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Contra [[ID]] 4 202 205 A/N Contra’s [[GSD]] [[ID]] Number 
Origination 1 206 206 A/N “T” = Tape Input                                                   
“V” = Video (Terminal Input) 
Start Amount 18 207 224 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Start Date 10 225 234 A/N Format is MM/DD/YYYY 
 
1 "Expected [[settlement]]" is only an estimate of netting eligibility. The "In Net" MRO, record type 17, should be used as final 
confirmation of whether the transaction was actually included in the net. 

---

## Page 10

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 10 
 
Field Name Length Start End Type Comments 
Role 1 235 235 A/N Reserved for Future Use 
Submitter [[ID]] 4 236 239 A/N [[GSD]] [[ID]] of Submitter of Trade 
Confirmations Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records 
 
Print Image “Header” Record for Record Type 01 – Comparison 
Confirmation 
 Field Name Length Start End Type Comments 
Trade Event  53 1  53 Text  Provides information that the trade has   
 been COMPARED 
XREF 20 (max). 
Varying 
54   Right Justified. This might not occupy all 
20 bytes allocated for it. This is a varying 
string. 
Print Reference 
Information 
17 Next column after 
XREF field ends. 
  Provides information about the next field 
TID 11 Next column after end 
of Print Reference 
Information. 
  Trade [[ID]] of the Compared Trade 
Final Trade 
State 
27 (max). 
Varying 
Next Column after end 
of TID field. 
   
CRLF 2 Next Column after end 
of Final Trade State. 
  Carriage Return + Line Feed 
 
Note:  
The above Print Image Header format is similar for all the GCF Comparison Record Type listed in this document, with the 
exception of Record Type 06 (Modify Confirmation), which will have one additional field as described in the section titled 
Record Type 06.  
  

---

## Page 11

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 11 
 
Print Image “Detail” Record 
Field Name Length Start End Type Comments 
Filler1 42 1  42 (5 tabs and 2 
spaces. Each Tab 
equals 8 spaces. 
Space Fillers 
Label 20  43 62 Text Description of the field being 
displayed 
Data 20 (max). 
Varying 
63 20 (max). 
Varying 
Text Contents/value of the field 
(length varies depending on 
the data) 
CRLF 2 Next Column 
after end of Data 
field. 
2 bytes after 
start position 
of this field. 
ASCII control 
characters 
Carriage Return + Line Feed 
 
Note:  
The number of detail records depends on the number of Label/Data pairs for each MRO. 
Note: 
The above Print Image Details section format is similar for all of the GCF Comparison Record Types listed in this 
document.  

---

## Page 12

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 12 
 
Record Type 02 – Modified Compared Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 02 Always = Compared with Modification 
External Reference Number 20 19 38 A/N XREF As supplied by the [[Member]] – MAST 
field 
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Filler 20 50 69 A/N Always = Spaces 
Transaction Type 4 70 73 A/N “REPO” or “REVR” 
Trade Date 10 74 83 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 84 93 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 94 102 A/N [[CUSIP]] Number 
Filler 24 103 126 A/N Always = Spaces 
Repo Rate 14 127 140 A/N Repo Rate as given to [[GSD]] 
Filler 1 141 141 A/N Always = Spaces 
Amount 18 142 159 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Filler 11 160 170 A/N Always = Spaces 
Contra [[ID]] 4 171 174 A/N Contra’s [[GSD]] [[ID]] Number 
Filler 6 175 180 A/N Always = Spaces 
XREF Modified 1 181 181 A/N “Y” = Yes, “  “ = No 
Filler 1 182 182 A/N Always = Spaces 
Transaction Type Modified 1 183 183 A/N “Y” = Yes, “  “ = No 
Trade Date Modified 1 184 184 A/N “Y” = Yes, “  “ = No 
[[settlement]] Date Modified 1 185 185 A/N “Y” = Yes, “  “ = No 
[[CUSIP]] Number Modified 1 186 186 A/N “Y” = Yes, “  “ = No 
Filler 1 187 187 A/N Always = Spaces 
Repo Rate Modified 1 188 188 A/N “Y” = Yes, “  “ = No 
Filler 1 189 189 A/N Always = Spaces 
Amount Modified 1 190 190 A/N “Y” = Yes, “  “ = No   
Filler 1 191 191 A/N Always = Spaces 
Contra [[ID]] Modified 1 192 192 A/N “Y” = Yes, “  “ = No 

---

## Page 13

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 13 
 
Field Name Length Start End Type Comments 
Filler 6 193 198 A/N Always = Spaces 
Expected [[settlement]] 1 199 199 A/N Expected [[settlement]]: 
 “T” = Trade for Trade 
“N” = Trade Expected to Net                     
For GCF is always “N” 
Executing Firm  5 200 204 A/N Executing firm associated with [[Member]] 
Executing Firm Modified 1 205 205 A/N “Y” = Yes, “  “ = No 
Contra’s Executing Firm 5 206 210 A/N Executing firm associated with Contra 
Contra’s Executing Firm 
Modified 
1 211 211 A/N “Y” = Yes, “  “ = No 
Contra’s External 
Reference Number 
20 212 231 A/N Cross reference to contra’s side 
Filler 8 232 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “1” = First of many records (if overflow 
records are required) 
Print Image ** 241 ** A/N **See section on logical detail records 
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 02 Always = Compared with Modification 
External Reference Number 20 19 38 A/N Matches the XREF listed in the 1st record  
Transaction [[ID]]  11 39 49 A/N Matches the Transaction [[ID]] listed in the 1st 
record 
Filler 40 50 89 A/N Always = Spaces 
Start Amount 18 90 107 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “. 
Applies to Repo Transactions only 
Start Date 10 108 117 A/N Format is MM/DD/YYYY.  
Filler 10 118 127 A/N Always = Spaces 
Secondary External 
Reference Number 
20 128 147 A/N As supplied by the [[Member]].  
Start Amount Modified 1 148 148 A/N “Y” = Yes, “  “ = No. Applies to Repo 
Transactions only 
Start Date Modified 1 149 149 A/N “Y” = Yes, “  “ = No. 

---

## Page 14

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 14 
 
Field Name Length Start End Type Comments 
Filler 1 150 150 A/N Always = Spaces 
Secondary XREF Modified 1 151 151 A/N “Y” = Yes, “  “ = No.  
Filler 24 152 175 A/N Always = Spaces 
Role 1 176 176 A/N Reserved for Future Use 
Role Modified 1 177 177 A/N Reserved for Future Use 
Filler 62 178 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “2” = Last of many records (if 2 or more 
records are required) 
 
  

---

## Page 15

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 15 
 
Record Type 03 – Cancellation Confirmation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 03 Always = Cancellation Confirmation 
External Reference Number 20 19 38 A/N XREF As supplied by the [[Member]]  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Command Type 4 50 53 A/N  “CAN” = Cancellation 
“REPL” = Replacement 
“LRPL” = Locked-in Replace 
Locked In Trade 1 54 54 A/N  “X” = Submitter of Locked-In Trade 
“L” = Recipient of Locked-In Trade 
 “  ” = Not Locked-In Trade 
Secondary External 
Reference Number 
20 55 74 A/N As supplied by the [[Member]].  
Filler 4 75 78 A/N Always = Spaces 
Transaction Type 4 79 82 A/N “REPO” or “REVR” 
Trade Date 10 83 92 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 93 102 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9  103 111 A/N [[CUSIP]] Number 
Repo Rate 14 112 125 A/N Repo Rate as given to [[GSD]] 
Amount 18 126 143 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Contra [[ID]] 4 144 147 A/N Contra’s [[GSD]] [[ID]] Number 
Filler 4 148 151 A/N Always = Spaces 
Origination 1 206 206 A/N “T” = Tape Input                                                   
“V” = Video (Terminal Input) 
Trade Time 6 153 158 A/N Format is HHMMSS 
Executing Firm 5 159 163 A/N Executing firm associated with [[Member]] 
Contra’s Executing Firm 5 164 168 A/N Executing firm associated with Contra 
Start Amount 18 169 186 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Start Date 10 187 196 A/N Format is MM/DD/YYYY 
Role 1 197 197 A/N Reserved for Future Use 
Submitter [[ID]] 4 198 201 A/N [[GSD]] [[ID]] of Submitter of Trade 

---

## Page 16

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 16 
 
Field Name Length Start End Type Comments 
Filler 38 202 239  Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records 
 
Note: 
“Command Type” is used to inform participants whether a cancel, or a cancel replace, generated the cancellation 
confirmation. 
  

---

## Page 17

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 17 
 
Record Type 06 – Modified Confirmation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 06 Always = External Reference Modified 
Confirmation 
New External Reference 
Number 
20 19 38 A/N New XREF As supplied by the [[Member]]  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Previous External 
Reference Number 
16 50 65 A/N Previous XREF, replaced by new XREF 
Secondary External 
Reference Number 
16 70 85 A/N As supplied by the [[Member]].  
Transaction Type 4 79 82 A/N “REPO” or “REVR” 
Trade Date 10 83 92 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 93 102 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9  103 111 A/N [[CUSIP]] Number 
Repo Rate 14 112 125 A/N Repo Rate as given to [[GSD]] 
Amount 18 126 143 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Contra [[ID]] 4 144 147 A/N Contra’s [[GSD]] [[ID]] Number 
Origination 1 206 206 A/N “T” = Tape Input                                                   
“V” = Video (Terminal Input) 
Executing Firm 5 159 163 A/N Executing firm associated with [[Member]] 
Contra’s Executing Firm 5 164 168 A/N Executing firm associated with Contra 
Start Amount 18 169 186 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Start Date 10 187 196 A/N Format is MM/DD/YYYY 
Role 1 197 197 A/N Reserved for Future Use 
Submitter [[ID]] 4 198 201 A/N [[GSD]] [[ID]] of Submitter of Trade 
Filler 38 202 239  Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records 

---

## Page 18

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 18 
 
Note: 
The Print Image Header format of Record Type 06 (Modify Confirmation) is similar in format to Record Type 01 
(Comparison Confirmation) with the exception of one additional field, the OLD XREF field, which contains the previous 
XREF that was modified. The format of this Header field is shown below. 
Print Image “Header” Record for Record Type 06 – Modified 
Confirmation 
 Field Name Length Start End Type Comments 
Trade Event  53 1  53 Text Provides information that the trade has 
been CANCELLED. 
XREF 20 (max). 
Varying 
54 73 (if all bytes 
are used 
A/N XREF that replaces the previous XREF 
of the trade.                                                           
Right Justified. This might not occupy all 
20 bytes allocated for it. This is a varying 
string. 
Print Reference 
Information 
17 Next column 
after XREF field 
ends. 
17 bytes after 
start position 
of this field 
Text Provides information about the next field. 
TID 11 Next column 
after end of 
Print Reference 
Information. 
11 bytes after 
start position 
of this field 
Text Trade [[ID]] of the Cancelled Trade. 
Final Trade 
State 
11 Next Column 
after end of TID 
field. 
11 bytes after 
start position 
of this field 
Text Provides information about the next field. 
OLD XREF 20 (max). 
Varying 
Next Column 
after end of 
Final Trade 
State field. 
20 (max). 
Varying 
A/N The Previous XREF of the trade. 
CRLF 2 Next Column 
after end of 
OLD XREF 
field. 
2 bytes after 
start position 
of this field 
ASCII 
Control 
Characters 
Carriage Return + Line Feed 
  

---

## Page 19

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 19 
 
Record Type 07 – Trade Input Accepted Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 07 Always = Trade Input Accepted 
Confirmation 
External Reference Number 20 19 38 A/N XREF As supplied by the [[Member]]  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Filler 20 50 69 A/N Always = Spaces 
Transaction Type 4 70  73 A/N “REPO” or “REVR” 
Trade Date 10 74 83 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 84 93 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 94 102 A/N [[CUSIP]] Number 
Filler 24  103 126 A/N Always = Spaces 
Repo Rate 14 127 140 A/N Repo Rate as given to [[GSD]] 
Filler 1 141 141 A/N Always = Spaces 
Amount 18 142 159 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Filler 11 160 170 A/N Always = Spaces 
Contra [[ID]] 4 171 174 A/N Contra’s [[GSD]] [[ID]] Number 
Filler 10 175 184 A/N Always = Spaces 
Origination 1 185 185 A/N “T” = Tape Input                                                   
“V” = Video (Terminal Input) 
Command 4 186 189 A/N “INST” = Instruct                                     
“REPL” = Replacement                                          
“LINT” = Locked-in Instruct                                 
“REPL” = Locked-in Replace 
Trade Time 6 190 195 A/N Format is HHMMSS 
Executing Firm  5 196 200 A/N Executing firm associated with [[Member]] 
Contra’s Executing Firm 5 201 205 A/N Executing firm associated with Contra 
Locked In Trade 1 206 206 A/N  “X” = Submitter of Locked-In Trade 
“L” = Recipient of Locked-In Trade 
 “  ” = Not Locked-In Trade 
Filler 10 207 216 A/N Always = Spaces 
Submitter [[ID]] 4 217 220 A/N [[GSD]] [[ID]] of Submitter of Trade 
Filler 19 221 239 A/N Always = Spaces 

---

## Page 20

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 20 
 
Field Name Length Start End Type Comments 
Confirmations Continued 1 240 240 A/N “1” = First of many records (if overflow 
records are required) 
Print Image ** 241 ** A/N **See section on logical detail records 
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 07 Always = Trade Input Accepted 
Confirmation 
External Reference Number 20 19 38 A/N Matches the XREF listed in the 1st record  
Transaction [[ID]]  11 39 49 A/N Matches the Transaction [[ID]] listed in the 1st 
record 
Start Amount 18 50 67 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “. 
Applies to Repo Transactions only 
Start Date 10 68 77 A/N Format is MM/DD/YYYY.  
Filler 10 78 87 A/N Always = Spaces 
Secondary External 
Reference Number 
20 88 107 A/N As supplied by the [[Member]]. 
Filler 23 108 130 A/N Always = Spaces 
Role 1 131 131 A/N Reserved for Future Use 
Filler 108 132 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “2” = Last of many records (if 2 or more 
records are required) 
 
  

---

## Page 21

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 21 
 
Record Type 09 – Trade Input Rejected Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 09 Always = Trade Input Rejected 
Confirmation 
Password 12 19 30 A/N As supplied by the [[Member]] – field may be 
blank 
External Reference Number 20 31 50 A/N XREF As supplied by the [[Member]]  
Command 4 51 54 A/N As supplied by the [[Member]] : INST, CAN or 
MFY 
Transaction Type 4 55 58 A/N As supplied by the [[Member]]  
Filler 20 59 78 A/N Always = Spaces 
Trade Date 10 79 88 A/N As supplied by the [[Member]]  
[[settlement]] Date 10 89 98 A/N As supplied by the [[Member]]  
[[CUSIP]] Number 9 99 107 A/N As supplied by the [[Member]]  
Filler 24 108 131 A/N As supplied by the [[Member]]  
Repo Rate 14 132 145 A/N As supplied by the [[Member]]  
Filler 30 146 175 A/N Always = Spaces 
Contra [[ID]] 4 176 179 A/N As supplied by the [[Member]]  
Filler 6 180 185 A/N Always = Spaces 
Password Error 1 186 186 A/N = “Y” If error 
Command Error 1 187 187 A/N = “Y” If error 
Transaction Type Error 1 188 188 A/N = “Y” If error 
Filler 1 189 189 A/N Always = Spaces 
Trade Date Error 1 190 190 A/N = “Y” If error 
[[settlement]] Date Error 1 191 191 A/N = “Y” If error 
[[CUSIP]] Number Error 1 192 192 A/N = “Y” If error 
Filler 1 193 193 A/N Always = Spaces 
Repo Rate Error 1 194 194 A/N = “Y” If error 
Filler 2 195 196 A/N Always = Spaces 
Contra [[ID]] Error 1 197 197 A/N = “Y” If error 
Filler 6 198 198 A/N Always = Spaces 
Internal Process Error 1 199 199 A/N = “Y” If error 

---

## Page 22

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 22 
 
Field Name Length Start End Type Comments 
External Reference Number 
Error 
1 200 200 A/N = “Y” If error 
[[Member]] [[ID]]  4 201 204 A/N As supplied by the [[Member]]  
Filler 6 205 210 A/N Always = Spaces 
Executing Firm 5 211 215 A/N As supplied by the [[Member]]  
Executing Firm Error 1 216 216 A/N = “Y” If error 
Contra’s Executing Firm 5 217 221 A/N As supplied by the [[Member]]  
Contra Executing Firm 
Error 
1 222 222 A/N = “Y” If error 
Filler 17 223 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “1” = First of many records (if overflow 
records are required) 
Print Image ** 241 ** A/N **See section on logical detail records     
Will contain only one error. 
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 09 Always = Trade Input Rejected 
Confirmation 
External Reference Number 20 19 38 A/N Matches the XREF listed in the 1st record  
Start Amount 18 39 56 A/N As supplied by the [[Member]].  
Start Date 10 57 66 A/N As supplied by the [[Member]].  
Filler 10 67 76 A/N Always = Spaces 
Secondary External 
Reference Number 
20 77 96 A/N As supplied by the [[Member]].  
Start Amount Error 1 97 97 A/N = “Y” If error.  
Start Date Error  1 98 98 A/N = “Y” If error.  
Filler 1 99 99 A/N Always = Spaces 
Secondary External 
Reference Number Error 
1 100 100 A/N = “Y” If error.  
Filler 24 101 124 A/N Always = Spaces 
Role 1 125 125 A/N Reserved for Future Use 
Role Error 1 126 126 A/N Reserved for Future Use 

---

## Page 23

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 23 
 
Field Name Length Start End Type Comments 
Filler 113 127 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “2” = Last of many records (if 2 or more 
records are required) 
 
  

---

## Page 24

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 24 
 
Record Type 10 – Cancellation Rejected Confirmation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 10 Always = Cancellation Rejected 
Confirmation 
Password 12 19 30 A/N As supplied by the [[Member]] – field may be 
blank 
External Reference Number 20 31 50 A/N XREF As supplied by the [[Member]]  
Transaction [[ID]]  11 51 61 A/N As supplied by the [[Member]] 
Filler 178 62 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records      
 
  

---

## Page 25

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 25 
 
Record Type 13 – Cancel Requested Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 13 Always = Cancellation Requested 
Confirmation 
External Reference Number 20 19 38 A/N XREF as supplied by the [[Member]]  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Contra’s Transaction [[ID]]  11 50 60 A/N The [[ID]] assigned to the Contra side of the 
Transaction by [[GSD]]. Format is XXXXXX-
XXXX 
Contra [[ID]] 4 61 64 A/N [[GSD]] [[ID]] of [[Member]] requesting cancellation 
Filler 6 65 70 A/N Always = Spaces 
Secondary External 
Reference Number 
20 71 90 A/N As supplied by the [[Member]].  
Filler 21 91 111 A/N Always = Spaces 
Transaction Type 4 112 115 A/N “REPO” or “REVR” 
Trade Date 10 116 125 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 126 135 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 136 144 A/N [[CUSIP]] Number 
Repo Rate 14 145 158 A/N Repo Rate as given to [[GSD]] 
Amount 18 159 176 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Filler 8 177 184 A/N Always = Spaces 
Origination 1 185 185 A/N “T” = Tape Input                                                   
“V” = Video (Terminal Input) 
Trade Time 6 186 191 A/N Format is HHMMSS 
Executing Firm 5 192 196 A/N Executing firm associated with [[Member]] 
Contra’s Executing Firm 5 197 201 A/N Executing firm associated with Contra 
Start Amount 18 202 219 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Start Date 10 220 229 A/N Format is MM/DD/YYYY 
Role 1 230 230 A/N Reserved for Future Use 
Submitter [[ID]] 4 231 234 A/N [[GSD]] [[ID]] of Submitter of Trade 
Filler 5 235 239 A/N Always = Spaces 

---

## Page 26

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 26 
 
Field Name Length Start End Type Comments 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records     
Will contain only one error. 
 
  

---

## Page 27

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 27 
 
Record Type 22 – Comparison Requested Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 22 Always = Comparison Requested 
External Reference Number 20 19 38 A/N XREF as supplied by the [[Member]]  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Filler 20 50 69 A/N Always = Spaces 
Transaction Type 4 70 73 A/N “REPO” or “REVR” 
Trade Date 10 74 83 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 84 93 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 94 102 A/N [[CUSIP]] Number 
Filler 24 103 126 A/N Always = Spaces 
Repo Rate 14 127 140 A/N Repo Rate as given to [[GSD]] 
Filler 1 141 141 A/N Always = Spaces 
Amount 18 142 159 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Filler 11 160 170 A/N Always = Spaces 
Contra [[ID]] 4 171 174 A/N Contra’s [[GSD]] [[ID]] Number 
Filler 6 175 180 A/N Always = Spaces 
[[Member]] Location 2 181 182 A/N [[Member]]’s Location (field is obsolete) 
Contra Location 2 183 184 A/N Contra’s Location (field is obsolete) 
Last Time Flag 1 185 185 A/N “Y” if trade will be deleted tonight, otherwise 
“N” 
Filler 4 186 189 A/N Always = Spaces 
Trade Time 6 190 195 A/N Format is HHMMSS 
Executing Firm  5 196 200 A/N Executing firm associated with [[Member]] 
Contra’s Executing Firm 5 201 205 A/N Executing firm associated with Contra 
Locked In Trade 1 206 206 A/N  “X” = Submitter of Locked-In Trade 
“L” = Recipient of Locked-In Trade 
 “  ” = Not Locked-In Trade 
Filler 10 207 216 A/N Always = Spaces 
Submitter [[ID]] 4 217 220 A/N [[GSD]] [[ID]] of Submitter of Trade 
Filler  6 221 226 A/N Always = Spaces 

---

## Page 28

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 28 
 
Field Name Length Start End Type Comments 
Command 4 227 230 A/N “INST” = Instruct                                                     
“REPL” = Replacement 
Filler 9 231 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “1” = First of many records (if overflow 
records are required) 
Print Image ** 241 ** A/N **See section on logical detail records      
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 22 Always = Comparison Requested 
External Reference Number 20 19 38 A/N Matches the XREF listed in the 1st record  
Transaction [[ID]]  11 39 49 A/N Matches the Transaction [[ID]] listed in the 1st 
record 
Start Amount 18 50 67 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “. 
Applies to Repo Transactions only 
Start Date 10 68 77 A/N Format is MM/DD/YYYY.  
Filler 10 78 87 A/N Always = Spaces 
Secondary External 
Reference Number 
20 88 107 A/N As supplied by the [[Member]].  
Filler 23 108 130 A/N Always = Spaces 
Role 1 131 131 A/N Reserved for Future Use 
Filler 108 132 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “2” = Last of many records (if 2 or more 
records are required) 
  

---

## Page 29

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 29 
 
Record Type 24 – Uncompared Deleted Confirmation 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 24 Always = Uncompared Deleted 
External Reference Number 20 19 38 A/N XREF as supplied by the [[Member]]  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Filler 20 50 69 A/N Always = Spaces 
Transaction Type 4 70 73 A/N “REPO” or “REVR” 
Trade Date 10 74 83 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 84 93 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 94 102 A/N [[CUSIP]] Number 
Filler 24 103 126 A/N Always = Spaces 
Price / Repo Rate 14 127 140 A/N Repo Rate as given to [[GSD]] 
Filler 1 141 141 A/N Always = Spaces 
Amount 18 142 159 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Filler 11 160 170 A/N Always = Spaces 
Contra [[ID]] 4 171 174 A/N Contra’s [[GSD]] [[ID]] Number 
Filler 6 175 180 A/N Always = Spaces 
[[Member]] Location 2 181 182 A/N [[Member]]’s Location (field is obsolete) 
Contra Location 2 183 184 A/N Contra’s Location (field is obsolete) 
Origination 1 185 185 A/N “I” = IM Input 
“W” = Web Input  
Command 4 186 189 A/N “INST” = Instruct                                                     
“MFY” = MODIFY 
Trade Time 6 190 195 A/N Format is HHMMSS 
Executing Firm  5 196 200 A/N Executing firm associated with [[Member]] 
Contra’s Executing Firm 5 201 205 A/N Executing firm associated with Contra 
Locked In Trade 1 206 206 A/N  “X” = Submitter of Locked-In Trade 
“L” = Recipient of Locked-In Trade 
 “  ” = Not Locked-In Trade 
Filler 10 207 216 A/N Always = Spaces 
Submitter [[ID]] 4 217 220 A/N [[GSD]] [[ID]] of Submitter of Trade 

---

## Page 30

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 30 
 
Field Name Length Start End Type Comments 
Filler 19 221 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “1” = First of many records (if overflow 
records are required) 
Print Image ** 241 ** A/N **See section on logical detail records      
 
Overflow Record Section 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 24 Always = Uncompared Deleted  
External Reference Number 20 19 38 A/N Matches the XREF listed in the 1st record  
Transaction [[ID]]  11 39 49 A/N Matches the Transaction [[ID]] listed in the 1st 
record 
Start Amount 18 50 67 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “. 
Applies to Repo Transactions only 
Start Date 10 68 77 A/N Format is MM/DD/YYYY.  
Filler 10 78 87 A/N Always = Spaces 
Secondary External 
Reference Number 
20 88 107 A/N As supplied by the [[Member]].  
Filler 23 108 130 A/N Always = Spaces 
Role 1 131 131 A/N Reserved for Future Use 
Filler 108 132 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “2” = Last of many records (if 2 or more 
records are required) 
  

---

## Page 31

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 31 
 
Record Type 40 – Affirmation Accepted Confirmation  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 40 Always = Affirmation Accepted 
Confirmation 
External Reference Number 20 19 38 A/N XREF as supplied by the [[Member]]  
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Locked In Trade 1 50 50 A/N  “X” = Submitter of Locked-In Trade 
“L” = Recipient of Locked-In Trade 
 “  ” = Not Locked-In Trade 
Secondary External 
Reference Number 
20  51 70 A/N As supplied by the [[Member]].  
Transaction Type 4 71 74 A/N “REPO” or “REVR” 
Trade Date 10 75 84 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 85 94 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 95 103 A/N [[CUSIP]] Number 
Repo Rate 14 104 117 A/N Repo Rate as given to [[GSD]] 
Amount 18 118 135 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Contra [[ID]] 4 136 139 A/N [[GSD]] [[ID]] of [[Member]] requesting cancellation 
Filler 4 140 143 A/N Always = Spaces 
Origination 1 144 144 A/N “T” = Tape Input                                                   
“V” = Video (Terminal Input) 
Trade Time 6 145 150 A/N Format is HHMMSS 
Executing Firm 5 151 155 A/N Executing firm associated with [[Member]] 
Contra’s Executing Firm 5 156 160 A/N Executing firm associated with Contra 
Start Amount 18 161 178 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Start Date 10 179 188 A/N Format is MM/DD/YYYY 
Role 1 189 189 A/N Reserved for Future Use 
Submitter [[ID]] 4 190 193 A/N [[GSD]] [[ID]] of Submitter of Trade 
Filler 1 194 194 A/N Always = Spaces 
Affirmed By 6 195 200 A/N User [[ID]] or “System” 

---

## Page 32

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 32 
 
Field Name Length Start End Type Comments 
Affirmation Time 11 201 211 A/N Format is HH:MM:SS:SS if done by a user, 
otherwise “overnight” if done by the [[GSD]] 
system. 
Filler 28 212 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records      
 
  

---

## Page 33

GCF Comparison MRO and Print Image Output Format – File 752 
GCF Comparison MRO and Print Image Output Formats 33 
 
Application Trailer Record 
Field Name Length Start End Type Comments 
Trailer [[ID]] 5 1 5 A/N Always = “TRAIL” 
Number of Records 5 6 10 N Total Number of GCF 2048 Byte output 
records in file 
Checksum 5 11 15 A/N XOR of Checksums of all other data records 
(For Future Use) 
Filler 2033 16 2048 A/N Always = Spaces 
 
 
 
 
   

---

## Page 34

 
  
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 