---
title: "GSD Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Output – Variable Lengths Records – File 1016"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd161_gsd_comparison-and_netting_batch_header_trailer_format_for_SWIFT_input_and_output_file_1016_102021.pdf"
pages: 13
size: "277.5 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Output – Variable Lengths Records – File 1016

**Original File:** [gsd161_gsd_comparison-and_netting_batch_header_trailer_format_for_SWIFT_input_and_output_file_1016_102021.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd161_gsd_comparison-and_netting_batch_header_trailer_format_for_SWIFT_input_and_output_file_1016_102021.pdf)  
**Category:** GSD  
**Total Pages:** 13  
**File Size:** 277.5 KB  

---

## Page 1

  
 
 
 
[[FICC]] – [[GSD]] 
[[GSD]] COMPARISON AND NETTING BATCH HEADER / TRAILER FORMATS 
FOR SWIFT INPUT / OUPUT – VARIABLE LENGTHS RECORDS – FILE 1016  
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
Publication Code: GSD161 
Service: [[FICC]] – [[GSD]]   
Title: [[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Output – Variable Length Records – 
File 1016 
 
 
The [[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Output – Variable Length Records – 
File 1016 (hereinafter, the "document") is provided as a convenience to Members and is for information purposes only. 
Although [[FICC]] may make this document available to Members, it shall be under no obligation to [[DO]] so, nor having once or 
more done so, shall [[FICC]] have a continuing obligation to make available this document or other related information of a 
certain type.  
 
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
Background ......................................................................................................................................................... 5 
File Structure ....................................................................................................................................................... 5 
Changes to Layouts ............................................................................................................................................ 5 
Delimiters ............................................................................................................................................................ 6 
Layouts ............................................................................................................................................................... 6 
Inbound to [[GSD]] DVP ........................................................................................................................................... 7 
DATATRAK Header ............................................................................................................................................ 7 
DATATRAK Trailer .............................................................................................................................................. 8 
Application Header Record ................................................................................................................................. 9 
Application Trailer Record .................................................................................................................................. 9 
Outbound to [[GSD]] Members .............................................................................................................................. 10 
AUTOROUTE Header ...................................................................................................................................... 10 
Application Header Record ............................................................................................................................... 12 
Application Trailer Record ................................................................................................................................ 12 
 

---

## Page 4

[[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Ouput – Variable Lengths Records – File 1016 
Overview 4 
 
OVERVIEW 
SWIFT Inbound and Outbound Batch File Transmission Specifications for [[GSD]] DVP Application 
Currently, [[GSD]] Members can submit DVP trades in a single or multi-batch method pursuant to [[GSD]] Rules, 
using SWIFT formats. [[GSD]] Members can also receive batch output from [[GSD]] on their DVP trades, using 
SWIFT formats. This document details those specifications required for both [[Member]] submission and receipt 
of batch files supporting SWIFT layouts, which may be used in support of [[GSD]]’s products and services.  
Audience 
This document was written for systems and development personnel including managers, analysts and 
programmers of [[GSD]] [[Member]] firms. It presumes readers are familiar with technical concepts and terms as 
well as having a [[BASIC]] understanding of [[GSD]]'s products and services. 
Communication 
For information on [[FICC]] Connectivity, please contact [[FICC]] Integration at ficcintegration@[[DTCC]].com. 
  

---

## Page 5

[[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Ouput – Variable Lengths Records – File 1016 
Introduction 5 
 
INTRODUCTION 
Background  
 
The application used to receive and route data from Members, DATATRAK, is different from that which sends 
out data to Members, AUTOROUTE. The header/trailer requirements for each application are different. 
File Structure 
Inbound to [[GSD]] DVP 
Each batch file of SWIFT formatted records received from Members must contain the following structure: 
• DATATRAK Header 
• Application Header 
• Data Records/Transactions 
• Application Trailer 
• DATATRAK Trailer 
 
Outbound to [[GSD]] Members 
Batch files of SWIFT messages sent from [[GSD]] DVP to Members will have the following structure: 
• AUTOROUTE Header (Optional- based on [[Member]] election) 
• Application Header 
• Data Records/Transactions 
• Application Trailer 
Changes to Layouts 
Header and Trailer formats/requirements can be different based on the content of the file. 
• Application header and trailer records will need to be placed on all inbound as well as outbound 
SWIFT files. 
• Application headers as well as application trailers, have similar, though not identical, formats on 
inbound and outbound files, and are populated differently based on the direction (inbound or 
outbound) of the file. All application headers and trailers will be 80-byte records. 
• DATATRAK headers and trailers on files inbound to [[GSD]] DVP consist of a minimum of 65 and 26 
bytes, respectively. 
• AUTOROUTE headers on outbound files sent to Members are fixed-format records consisting of 133 
bytes. 
 

---

## Page 6

[[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Ouput – Variable Lengths Records – File 1016 
Introduction 6 
 
Delimiters 
 
Regarding Data Record Delimiters, it should be noted that for submission to [[GSD]] DVP, each SWIFT message 
should consist of one line of data, with tag/field delimiters (carriage return line feeds (i.e., CRLF)) embedded in 
each record line. Each record/line should end with a “CRLF-“, followed by a CRLF to begin the following record 
on the next line. 
Layouts 
 
The layouts provided in this document are as follows: 
• Inbound to [[GSD]] DVP 
o DATATRAK Header 
o DATATRAK Trailer 
o Application Header 
o Application Trailer 
• Outbound to [[GSD]] Members  
o AUTOROUTE Header 
o Application Header 
o Application Trailer 
  

---

## Page 7

[[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Ouput – Variable Lengths Records – File 1016 
Inbound to [[GSD]] DVP 7 
 
INBOUND TO [[GSD]] DVP 
DATATRAK Header 
DATATRAK Header Header 
Field Name Length Start End Type Comments 
Constant 1 5 1 5 A/N Always = ‘HDR.S’ 
DATATRAK SYSID 5 6 10 N System Identifier                                      
SWIFT-in Production = 62326                 
SWIFT-in Test = 42326 
Constant 2 2 11 12 A/N Always = '.E' (period, E) 
Constant 3 2 13 14 N Always = ‘00’ 
Constant 4 2 15 16 A/N Always = ‘.C’  
Originator 4 17 20 A/N [[GSD]] [[Member]] [[ID]] Number                              
Will be 4 characters for firms submitting on 
their own behalf. 
Constant 5 2 21 22 A/N Always = ‘.S’  
Sub-originator 4 23 26 A/N [[GSD]] [[Member]] [[ID]] Number                                    
Will be 4 characters for firms submitting on 
their own behalf.  
Submission Date 8 27 34 N MMDDCCYY 
File Description 25 35 59 A/N SWIFT-in Production = ‘GSCC ISO EDIT’                 
SWIFT-in Test = ‘TEST GSCC ISO EDIT’ 
Multi-Batch Indicator 1 60 60 A/N Space = No Multi-Batch                               
N = Multi-Batch, Not Last                             
Y = Multi-Batch, Last 
Multi-Batch Number 3 61 63 N Spaces = No Multi-Batch                               
Sequential # starting with 001 = Multi-Batch 
Reversed for Future Use 1 64 64 A/N Reserved 
Variable Length Record 
Indicator 
1 65 65 A/N 
Variable Length = ‘∗’                                        
Fixed Length = Space                                        
All SWIFT message files should contain 
variable length records. 
Reserved for Future Use 15 66 80 A/N Spaces 
 END OF RECORD 
 
Note:  
When the data file is fixed-length, the header has the same record length as the data records. For a variable-length file, a 
minimum header length of 65 bytes is required.  

---

## Page 8

[[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Ouput – Variable Lengths Records – File 1016 
Inbound to [[GSD]] DVP 8 
 
DATATRAK Trailer 
DATATRAK Trailer Trailer 
Field Name Length Start End Type Comments 
Constant 1 5 1 5 A/N Always = ‘END.S’ 
DATATRAK SYS [[ID]] 5 6 10 A/N System Identifier                                      
SWIFT-in Production = 62326                 
SWIFT-in Test = 42326 
Constant 2 2 11 12 A/N Always = '.E'  
Constant 3 2 13 14 A/N Always = ‘00’ 
Constant 4 2 15 16 A/N Always = ‘.C’  
Originator 24 17 20 A/N [[GSD]] [[Member]] [[ID]] Number                              
Will be 4 characters for firms submitting on 
their own behalf. 
Constant 5 2 21 22 A/N Always = ‘.S’  
Sub-originator 4 23 26 A/N [[GSD]] [[Member]] [[ID]] Number                              
Will be 4 characters for firms submitting on 
their own behalf. 
Record Count  7 27 33 N Optional Field. Count of data file records. 
Reversed for Future Use 1 34 34 A/N Space 
Expanded Record Count 9 35 43 N Optional Field. Count of data file records. 
Reserved for Future Use 37 44 80 A/N Spaces 
 END OF RECORD 
 
Note:  
When the data file is fixed-length, its trailer record, if present, has the same record length as the data records. A trailer 
present for a variable length file has a minimum length of 26 bytes.  

---

## Page 9

[[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Ouput – Variable Lengths Records – File 1016 
Inbound to [[GSD]] DVP 9 
 
Application Header Record 
Field Name Length Start End Type Comments 
Constant 6 1 6 A/N Always = “HEADER” 
Destination 4 7 10 A/N Always = GSCC 
Application 4 11 14 A/N “TRRS” 
Filler 4 15 18 A/N  Reserved for Future Use 
Source Name 4 19 22 A/N  [[GSD]] [[Member]] [[ID]] Number 
File Format 8 23 30 A/N Always = “SWIFT   “ 
Date/Time 22 31 52 A/N DD-MMM-YYYY HH:MM:SS.H 
 i.e., 19-JAN-2021 10:45:15.2 
Filler 28 53 80 A/N Reserved for Future Use 
 
Application Trailer Record 
Field Name Length Start End Type Comments 
Trailer [[ID]] 5 1 5 A/N Always = “TRAIL” 
Record Count 5 6 10 N Total Number of records in file 
Filler 22 11 32 A/N Always = Spaces 
Submitting Firm 4 33 36 N [[GSD]] [[Member]] [[ID]] Number 
Filler 44 37 80 A/N Always = Spaces 
 
 
 
 
 
 
  

---

## Page 10

[[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Ouput – Variable Lengths Records – File 1016 
Outbound to [[GSD]] Members 10 
 
OUTBOUND TO [[GSD]] MEMBERS 
AUTOROUTE Header 
AUTOROUTE Header Header 
Field Name Length Start End Type Comments 
Header [[ID]] 6 1 6 A/N Always = 1TRANS 
Application Date 8 7 14 NUM CCYYMMDD (year,month,day) This is the 
processing date for the file. 
Reserved  2 15 16  [[DO]] not use 
Product Number 3 17 19 NUM Production SWIFT comparison output = 016 
Test SWIFT comparison output = 016 
Product Description 20 20 
 
39 A/N Alpha Production Description                          
Production SWIFT comparison output = 
‘GSCC ISO MRO’                                            
Test SWIFT comparison output = ‘TEST 
GSCC ISO MRO’ 
Reserved  3 40 42  [[DO]] not use 
Reserved 1 43 43  [[DO]] not use 
Multi-Cycle Transmission 
Counter 
2 44 45 A/N 01–99 Logical multi-cycle count of the job 
sent, or                                                     
Spaces = Not multi-cycle  
Possible Dupe Indicator 1 46 46 A/N Space = Original transmission                                
1 = Not multi-cycle 
Product [[ID]] 8 47 54 NUM 8-digit code issued to identify the report or 
file                                                             
Production SWIFT comparison output = 
08171016                                                  
Test SWIFT comparison output = 08981016 
Application’s Multi-Cycle 
Counter 
2 55 56 NUM 1, 2,...,97 = Applications which provide 
more than one output per day have a 
sequential number for each output.            
98 = Final output cycle number for a day.   
Spaces = Not multi-cycle 
Recipient [[ID]] 7 57 63 A/N This code is assigned to the destination of 
this 
transmission. It normally begins with the 
four-digit [[Member]] [[ID]] number. 
Constant     Always = 0 (zero) 
(Contains other values for internal 
distribution) 

---

## Page 11

[[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Ouput – Variable Lengths Records – File 1016 
Outbound to [[GSD]] Members 11 
 
AUTOROUTE Header Header 
Field Name Length Start End Type Comments 
Record Count 9 65 73 NUM Number of data records or print lines that 
follow 
Sender [[ID]] 4 74 77 A/N [[DTCC]] 
Constant 3 78 80 A/N Always = CDT                                              
(Last field of 80-byte RJE header) 
Reserved 1 81 81  [[DO]] not use 
Data Created 8 82 89 A/N MMDDCCYY 
Reserved 3 90 92  [[DO]] not use 
Time Created 5 93 97 A/N HH:MM 
Reserved 4 98 101  [[DO]] not use 
 Constant 3 102 104 A/N Always = RDT 
 Reserved 1 105 105 105 [[DO]] not use 
Date released 8 106 113 A/N MMDDCCYY (File transmission date) 
Reserved 3 114 116  [[DO]] not use 
Time released 5 117 121 A/N HH:MM (File transmission time) 
Reserved 12 122 133  [[DO]] not use 
 END OF RECORD 
 
  

---

## Page 12

[[GSD]] Comparison and Netting Batch Header / Trailer Formats for SWIFT Input / Ouput – Variable Lengths Records – File 1016 
Outbound to [[GSD]] Members 12 
 
Application Header Record 
Field Name Length Start End Type Comments 
Constant 6 1 6 A/N Always = “HEADER” 
Source Name 4 7 10 A/N Always = GSCC 
Application 4 11 14 A/N “TRRS” 
Filler 4 15 18 A/N  Reserved for Future Use 
Destination Name 4 19 22 A/N  [[GSD]] [[Member]] [[ID]] Number 
File Format 8 23 30 A/N Always = “SWIFT   “ 
Date/Time 22 31 52 A/N DD-MMM-YYYY HH:MM:SS.H 
 i.e., 19-JAN-2021 10:45:15.2 
Filler 28 53 80 A/N Reserved for Future Use 
 
Application Trailer Record 
Field Name Length Start End Type Comments 
Trailer [[ID]] 5 1 5 A/N Always = “TRAIL” 
Record Count 5 6 10 N Total Number of records in file 
Filler 5 11 15 A/N Always = Spaces 
[[Member]] [[ID]] 4 16 19 N [[GSD]] [[Member]] [[ID]] Number 
Date 11 20 30 A/N DD-MMM-YYYY                                           
i.e., 19-JAN-2021 
Filler 50 31 80 A/N Always = Spaces 
 
 
 
 
 
 
 
 
  

---

## Page 13

 
  
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 