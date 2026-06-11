---
title: "GCF Net MRO and Print Image Output Format - File 754"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd158_gcf_net_mro_and_print_image_output_format_file_754_112021.pdf"
pages: 23
size: "350.2 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GCF Net MRO and Print Image Output Format - File 754

**Original File:** [gsd158_gcf_net_mro_and_print_image_output_format_file_754_112021.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd158_gcf_net_mro_and_print_image_output_format_file_754_112021.pdf)  
**Category:** GSD  
**Total Pages:** 23  
**File Size:** 350.2 KB  

---

## Page 1

  
 
 
 
[[FICC]] – [[GSD]] 
GCF NET MRO AND PRINT IMAGE OUTPUT FORMAT – FILE 754 
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
Publication Code: GSD158 
Service: [[FICC]] – [[GSD]]   
Title: GCF Net MRO and Print Image Output Format – File 754 
 
 
The GCF Net MRO and Print Image Output Format – File 754 (hereinafter, the "document") is provided as a convenience to 
Members and is for information purposes only. Although [[FICC]] may make this document available to Members, it shall be 
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
GCF Net MRO and Print Image Output Formats ............................................................................................... 8 
Application Header Record ................................................................................................................................. 8 
Record Type 17 – Transaction In Net ................................................................................................................. 9 
Record Type 18 – Clearance Instruction .......................................................................................................... 11 
Record Type 20 – Security Net Summary ........................................................................................................ 12 
Record Type 21 – End of Day [[participant]] Net Summary ................................................................................. 13 
Record Type 26 – Forward Transaction Pended for Netting ............................................................................ 15 
Record Type 27 – Forward Transaction Pended – No Longer in Net .............................................................. 17 
Record Type 28 – Forward Position Summary ................................................................................................. 19 
Record Type 39 – Per-Trade Forward Mark ..................................................................................................... 20 
Application Trailer Record ................................................................................................................................ 22 
 

---

## Page 4

GCF Net MRO and Print Image Output Format – File 754 
Overview 4 
 
OVERVIEW 
General [[collateral]] Finance (GCF) Net Machine Readable Output (MRO) and Print Image Output 
Specification 
This document provides Members of the Fixed Income Clearing Corporation‘s (“[[FICC]]”) Government [[securities]] 
Division (“[[GSD]]”) that participate in the General [[collateral]] Finance Repo (GCF Repo®) Service and the 
Centrally Cleared Institutional Tri-party (CCIT™) Service with machine readable output (MRO) and print image 
output specifications for GCF netting related record types used to support [[GSD]]’s GCF Repo Service and CCIT 
Service.  
Audience 
This document was written for systems and development personnel including managers, analysts and 
programmers of [[GSD]] [[Member]] firms. It presumes readers are familiar with technical concepts and terms as 
well as having a [[BASIC]] understanding of [[GSD]]'s products and services. 
Communication 
For information on [[FICC]] Connectivity, please contact [[FICC]] Integration at ficcintegration@[[DTCC]].com. 
  

---

## Page 5

GCF Net MRO and Print Image Output Format – File 754 
Introduction 5 
 
INTRODUCTION 
This document provides the formats for the GCF netting related record types used to support [[GSD]]’s GCF 
Repo Service and CCIT Service, enabling [[GSD]] Members that participate in those services to receive trade 
status messages.  
The upcoming sections within this document will describe the GCF Netting MRO file number 754 which include 
the following record types: 
• Description of the Logical Details Records 
• Application Header Record 
• Record Type 17 – Transaction in Net 
• Record Type 18 – Clearance Instruction 
• Record Type 20 – Security Net Summary 
• Record Type 21 – End of Day [[participant]] Net Summary 
• Record Type 26 – Forward Transaction Pended for Netting 
• Record Type 27 – Forward Transaction Pended – No Longer in Net 
• Record Type 28 – Forward Position Summary 
• Record Type 39 – Per Trade Forward Mark  
• Application Trailer Record 
 
Record types discussed in this document will give Members the ability to take in important netting status 
information and manage their [[obligations]] at end of day. 
It should be noted that this document is a technical specification and is not, in any way, intended to 
communicate legal definitions as to when trades are guaranteed or novated by [[GSD]]. Members should refer to 
the [[FICC]] [[GSD]] Rulebook for such information. 
For additional service details, please refer to the Clearing Services > Fixed Income – [[GSD]] section available at 
www.[[DTCC]].com. 

---

## Page 6

GCF Net MRO and Print Image Output Format – File 754 
Description of the Logical Detail Records 6 
 
DESCRIPTION OF THE LOGICAL DETAIL RECORDS 
A logical record is made up of one or more 2,048 Byte physical records, depending on the size of the print 
image information. The first 16 bytes of each physical record consists of four fields, identified with asterisks (**) 
in the example below, which are referred to in the description of each record type as the STANDARD 16 
BYTES.  
First 2,048 Byte Record 
Field Name Length Start End Type Comments 
Logical Record Number ** 5 1 5 N Sequential number of the logical record 
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
 17 – Transaction in Net  
 18 – Clearance Instruction 
 20 – Security Net Summary, etc.. 
Machine Readable Only  
Output 
222 19 240 A/N Refer to the description of each Record 
Type 
Print Image 1808 241 2048 A/N Print Positioning is controlled by Carriage 
Return Line Feed (CRLF) Combinations. 
Form feeds may be imbedded a after CRLF 
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

GCF Net MRO and Print Image Output Format – File 754 
Description of the Logical Detail Records 7 
 
All subsequent 2,048 Byte Records 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See above 
Print Image 2032 17 2048 A/N See above 
 
The descriptions for each section of the Print Image for the GCF Netting MRO Record Types will be explained 
in upcoming sections of this document. 

---

## Page 8

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 8 
 
GCF NET MRO AND PRINT IMAGE OUTPUT FORMATS 
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

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 9 
 
Record Type 17 – Transaction In Net 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 17 Always = Transaction In Net 
External Reference Number 20 19 38 A/N As supplied by the [[Member]] (a sequence 
number which remains unique to this 
Transaction as long as it is in the system) 
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
[[Member]] [[ID]] 4 50 53 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 6 54 59 A/N Always = Spaces 
Locked In Trade 1 60 60 A/N  “X” = Submitter of Locked-In Trade 
“L” = Recipient of Locked-In Trade 
“  ” = Not Locked-In Trade 
Secondary External 
Reference Number 
20 61 80 A/N As supplied by the [[Member]]. 
Netting Status 9 81 89 A/N Indicates the current status of the trade. The 
field is filled in with one of the following:             
 “START LEG”  
“END LEG    ” 
 “BETWEEN ”  
Transaction Type 4 90 93 A/N “REPO” or “REVR” 
Trade Date 10 94 103 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 104 113 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 114 122 A/N [[CUSIP]] Number 
Filler 6 123 128 A/N Always = Spaces 
Repo Rate 14 129 142 A/N Repo Rate as given to [[GSD]] 
Amount 18 143 160 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Contra [[ID]] 4 161 164 A/N Contra’s [[GSD]] [[ID]] Number 
Filler 10 165 174 A/N Always = Spaces 
Origination 1 175 175 A/N “T” = Tape Input                                                   
“V” = Video (Terminal Input) 
Trade Time 6 176 181 A/N Format is HHMMSS 
Executing Firm 5 182 186 A/N Executing firm associated with [[Member]] 
Contra’s Executing Firm 5 187 191 A/N Executing firm associated with Contra 

---

## Page 10

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 10 
 
Field Name Length Start End Type Comments 
Start Amount 18 192 209 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Start Date 10 210 219 A/N Format is MM/DD/YYYY 
Role 1 220 220 A/N Reserved for Future Use 
Submitter [[ID]] 4 221 224 A/N [[GSD]] [[ID]] of Submitter of Trade 
Filler 15 225 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records      
 
 
  

---

## Page 11

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 11 
 
Record Type 18 – Clearance Instruction  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 18 Always = Clearance Instruction  
Filler 11 19 29 A/N Always = Spaces 
[[Member]] [[ID]] 4 30 33 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 4 34 39 A/N Always = Spaces 
Transaction Code 1 40 40 A/N “L” = Long, “S” = Short 
[[CUSIP]] Number 9 41 49 A/N [[CUSIP]] Number 
Filler 24 50 73 A/N Always = Spaces 
Amount 18 74 91 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“ 
Clearing Bank ABA 9 92 100 A/N ABA of [[GSD]] Clearing Bank provided by 
[[GSD]] 
Fed Address 40 101 140 A/N Fed Wire Address 
[[GSD]] Contra [[ID]] at [[Member]] 
Bank 
20 141 160 A/N [[Member]]’s Bank Short Name for [[GSD]] 
Account at its Bank for this Product 
Clearance Type 1 161 161 A/N “N” = Next Day 
[[settlement]] Date 10 162 171 A/N Format is MM/DD/YYYY 
Filler 68 172 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records      
 
 
  

---

## Page 12

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 12 
 
Record Type 20 – Security Net Summary  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 20 Always = Security Net Summary  
[[Member]] [[ID]] 4 19 22 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 6 23 28 A/N Always = Spaces 
[[CUSIP]] Number 9 29 37 A/N [[CUSIP]] Number 
Filler 20 38 57 A/N Always = Spaces 
Next Day Position 18 58 75 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“. 
Net Lock-up Position as reflected by Next 
Day Trades included in the net 
Long / Short Indicator 1 76 76 A/N “L” = Long, “S” = Short 
Filler 76 77 152 A/N Always = Spaces 
Next Day TAP 18 153 170 A/N Format same as Next Day Position. The 
[[Member]]’s TAP as derived from Next Day 
Trades that were included in the net 
CR / DR Indicator 1 171 171 A/N “C” = Credit, “D” = Debit 
Filler 68 172 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records      
 
 
  

---

## Page 13

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 13 
 
Record Type 21 – End of Day [[participant]] Net Summary 
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 21 Always = [[participant]] Net Summary  
[[Member]] [[ID]] 4 19 22 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 6 23 28 A/N Always = Spaces 
Opening Balance 11 29 39 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“. 
Opening Balance taken from prior day’s 
funds [[settlement]] cycle’s Total Funds 
Obligation amount 
CR / DR Indicator 1 40 40 A/N “C” = Credit, “D” = Debit 
Next Day TAP 11 41 51 A/N Format same as Opening Balance. The 
[[Member]]’s TAP as derived from trades 
included in the net for next day [[settlement]] 
CR / DR Indicator 1 52 52 A/N “C” = Credit, “D” = Debit 
Filler 48 53 100 A/N Always = Spaces 
Miscellaneous Adjustments 11 101 111 A/N Format same as Opening Balance.  
CR / DR Indicator 1 112 112 A/N “C” = Credit, “D” = Debit 
Miscellaneous Reason 30 113 142 A/N Reason for Miscellaneous Adjustment 
Forward Mark Allocation 11 143 153 A/N Format same as Opening Balance. Forward 
Mark allocation as assessed by [[GSD]] for the 
current funds [[settlement]] cycle. 
CR / DR Indicator 1 154 154 A/N “C” = Credit, “D” = Debit 
Forward Mark Allocation 
Return 
11 155 165 A/N Format same as Opening Balance. Return 
of Forward Mark allocation as assessed by 
[[GSD]] for prior day’s funds [[settlement]] cycle. 
CR / DR Indicator 1 166 166 A/N “C” = Credit, “D” = Debit 
Collected / Paid 18 167 177 A/N Format same as Opening Balance. Actual 
Amount of Total Funds Obligation settled. 
CR / DR Indicator 1 178 178 A/N “C” = Credit, “D” = Debit 
Invoice 11 179 189 A/N Format same as Opening Balance. [[GSD]] 
Monthly Bill for [[Member]] 
CR / DR Indicator 1 190 190 A/N “C” = Credit, “D” = Debit 
Total Funds Obligation 11 191 201 A/N Format same as Opening Balance. 
Payment due to or from [[GSD]] for the current 
funds [[settlement]] cycle. 
CR / DR Indicator 1 202 202 A/N “C” = Credit, “D” = Debit 

---

## Page 14

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 14 
 
Field Name Length Start End Type Comments 
[[collateral]] on Deposit for 
Forward Mark Allocation 
11 203 213 A/N Format same as Opening Balance. 
Informational Only. [[collateral]] on Deposit to 
satisfy part or all of the Forward Mark 
Allocation 
CR / DR Indicator 1 214 214 A/N “C” = Credit, “D” = Debit 
Filler 12 215 226 A/N Always = Spaces 
Interest Adjustment 
Payment 
11 227 237 A/N Format same as Opening Balance. Accrued 
Interest paid / collected on Forward Mark  
CR / DR Indicator 1 238 238 A/N “C” = Credit, “D” = Debit 
Filler 1 239 239 A/N Always = Space 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records      
 
Note:  
The sum of these values are carried over to the Funds-Only [[settlement]] application to be collected/paid as a single funds-
only [[settlement]] obligation with [[GSD]].  

---

## Page 15

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 15 
 
Record Type 26 – Forward Transaction Pended for Netting  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 26 Always = Forward Transaction Pended 
for Netting 
External Reference Number 20 19 38 A/N As supplied by the [[Member]] (a sequence 
number which remains unique to this 
Transaction as long as it is in the system) 
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Filler 1 50 50 A/N Always = Space 
Amount 11 51 61 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1365000“. 
Trade Novated at this amount  
Secondary External 
Reference Number 
20 62 81 A/N As supplied by the [[Member]].  
Filler 4 82 85 A/N Always = Spaces 
Transaction Type 4 86 89 A/N “REPO” or “REVR” 
Trade Date 10 90 99 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 100 109 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 110 118 A/N [[CUSIP]] Number 
Repo Rate 14 119 132 A/N Repo Rate as given to [[GSD]] 
Filler 4 133 136 A/N Always = Spaces 
Contra [[ID]] 4 137 140 A/N Contra’s [[GSD]] [[ID]] Number 
Origination 1 141 141 A/N “T” = Tape Input                                                   
“V” = Video (Terminal Input) 
Trade Time 6 142 147 A/N Format is HHMMSS 
Executing Firm 5 148 152 A/N Executing firm associated with [[Member]] 
Contra’s Executing Firm 5 153 157 A/N Executing firm associated with Contra 
Start Amount 18 158 175 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Start Date 10 176 185 A/N Format is MM/DD/YYYY 
Role 1 186 186 A/N Reserved for Future Use 
Submitter [[ID]] 4 187 190 A/N [[GSD]] [[ID]] of Submitter of Trade 
Filler 4 191 194 A/N Always = Spaces 
Locked In Trade 1 195 195 A/N  “X” = Submitter of Locked-In Trade 

---

## Page 16

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 16 
 
Field Name Length Start End Type Comments 
“L” = Recipient of Locked-In Trade 
 “  ” = Not Locked-In Trade 
Amount Indicator 1 196 196 A/N “N” Indicates that the amount in the 
Amount field is correct                                       
“Y” Indicates that the amount in the Amount 
Formatted field is correct and the amount in 
the Amount field is “   000” 
Amount Formatted 18 197 214 A/N Format same as Start Amount 
Filler 25 215 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records      
 
 
  

---

## Page 17

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 17 
 
Record Type 27 – Forward Transaction Pended – No Longer in Net  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 27 Always = Forward Transaction Pended – 
No Longer in Net 
External Reference Number 20 19 38 A/N As supplied by the [[Member]] (a sequence 
number which remains unique to this 
Transaction as long as it is in the system) 
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Secondary External 
Reference Number 
20 50 69 A/N As supplied by the [[Member]].  
Filler 4 70 73 A/N Always = Spaces 
Transaction Type 4 74 77 A/N “REPO” or “REVR” 
Trade Date 10 78 87 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 88 97 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 98 106 A/N [[CUSIP]] Number 
Repo Rate 14 107 120 A/N Repo Rate as given to [[GSD]] 
Amount 18 121 138 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Filler 4 139 142 A/N Always = Spaces 
Contra [[ID]] 4 143 146 A/N Contra’s [[GSD]] [[ID]] Number 
Origination 1 147 147 A/N “T” = Tape Input                                                   
“V” = Video (Terminal Input) 
Trade Time 6 148 153 A/N Format is HHMMSS 
Executing Firm 5 154 158 A/N Executing firm associated with [[Member]] 
Contra’s Executing Firm 5 159 163 A/N Executing firm associated with Contra 
Start Amount 18 164 181 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Start Date 10 182 191 A/N Format is MM/DD/YYYY 
Role 1 192 192 A/N Reserved for Future Use 
Submitter [[ID]] 4 193 196 A/N [[GSD]] [[ID]] of Submitter of Trade 
Filler 4 197 200 A/N Always = Spaces 
Locked In Trade 1 201 201 A/N  “X” = Submitter of Locked-In Trade 
“L” = Recipient of Locked-In Trade 
 “  ” = Not Locked-In Trade 

---

## Page 18

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 18 
 
Field Name Length Start End Type Comments 
Filler 38 202 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records      
 
 
  

---

## Page 19

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 19 
 
Record Type 28 – Forward Position Summary  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 28 Always = Forward Position Summary  
[[CUSIP]] Number 9 19 27 A/N [[CUSIP]] Number 
Filler 20 28 47 A/N Always = Spaces 
Forward Position 18 48 65 A/N Right Justified Blank Filled, i.e., 1 Million 
365 Thousand would be = “   1,365,000.00“. 
Net lock-up Position as reflected by 
Forward Trades Pended for Netting 
Long / Short Indicator 1 66 66 A/N “L” = Long, “S” = Short 
Forward Amount 18 67 84 A/N Format same as Forward Position. Net 
Amount as reflected by Forward Trades 
Pended for Netting 
CR / DR Indicator 1 85 85 A/N “C” = Credit, “D” = Debit 
Forward Mark 18 86 103 A/N Format same as Forward Position. 
Informational Only. Net of Forward Marks 
for each Trade Pended for Netting 
CR / DR Indicator 1 104 104 A/N “C” = Credit, “D” = Debit 
Forward Mark Allocation 18 105 122 A/N Format same as Forward Position. Net If 
Forward Mark is a Credit, the value in this 
field will be “0.00”. Otherwise, the value will 
be assessed by [[GSD]] 
CR / DR Indicator 1 123 123 A/N “C” = Credit, “D” = Debit 
[[Member]] [[ID]] 4 124 127 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 17 128 144 A/N Always = Spaces 
Product 6 145 150 A/N Product Type for the GCF Repo Generic 
[[CUSIP]] Number 
Filler 89 151 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record) 
Print Image ** 241 ** A/N **See section on logical detail records      
  

---

## Page 20

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 20 
 
Record Type 39 – Per-Trade Forward Mark  
Field Name Length Start End Type Comments 
Standard 16 Bytes 16 1 16 A/N See section Logical Detail Records 
Record [[ID]] 2 17 18 N 39 Always = Per-Trade Forward Mark  
External Reference Number 20 19 38 A/N As supplied by the [[Member]] (a sequence 
number which remains unique to this 
Transaction as long as it is in the system) 
Transaction [[ID]]  11 39 49 A/N The [[ID]] assigned to this Transaction by 
[[GSD]]. Format is XXXXXX-XXXX 
Filler 4  50 53 A/N Always = Spaces 
[[Member]] [[ID]] 4 54 57 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 6 58 63 A/N Always = Spaces 
Secondary External 
Reference Number 
20 64 83 A/N As supplied by the [[Member]].  
Status 9 84 92 A/N Always = Spaces. Reserved for Future Use 
Forward Mark 18 93 110 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “    
Credit / Debit 1 111 111 A/N “C” = Credit, “D” = Debit 
Finance Mark 18 112 129 A/N Format same as Forward Mark 
Credit / Debit 1 130 130 A/N “C” = Credit, “D” = Debit 
Transaction Type 4 131 134 A/N “REPO” or “REVR” 
Trade Date 10 135 144 A/N Format is MM/DD/YYYY 
[[settlement]] Date 10 145 154 A/N Format is MM/DD/YYYY 
[[CUSIP]] Number 9 155 163 A/N [[CUSIP]] Number 
Repo Rate 14 164 177 A/N Repo Rate as given to [[GSD]] 
Amount 18 178 195 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Contra [[ID]] 4 196 199 A/N Contra’s [[GSD]] [[ID]] Number 
Start Amount 18 200 217 A/N Left Justified Blank Filled, i.e., 1 Million 365 
Thousand would be = “1,365,000.00       “ 
Start Date 10 218 227 A/N Format is MM/DD/YYYY 
Role 1 228 228 A/N Reserved for Future Use 
Submitter [[ID]] 4 229 232 A/N [[GSD]] [[ID]] of Submitter of Trade 
Locked In Trade 1 233 233 A/N  “X” = Submitter of Locked-In Trade 
“L” = Recipient of Locked-In Trade 
 “  ” = Not Locked-In Trade 

---

## Page 21

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 21 
 
Field Name Length Start End Type Comments 
Filler 6 234 239 A/N Always = Spaces 
Confirmation Continued 1 240 240 A/N “  ” = Only record (no overflow record)  
Print Image ** 241 ** A/N **See section on logical detail records      
 
 
  

---

## Page 22

GCF Net MRO and Print Image Output Format – File 754 
GCF Net MRO and Print Image Output Formats 22 
 
Application Trailer Record 
Field Name Length Start End Type Comments 
Trailer [[ID]] 5 1 5 A/N Always = “TRAIL” 
Number of Records 5 6 10 N Total Number of GCF 2048 Byte output 
records in file 
Checksum 5 11 15 A/N XOR of Checksums of all other data records 
(For Future Use) 
Filler 2033 16 2048 A/N Always = Spaces 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 23

 
  
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 