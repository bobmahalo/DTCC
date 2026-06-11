---
title: "Networking - General Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_general_layouts_mfs365_202402123.pdf"
pages: 11
size: "319.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Networking - General Record Layouts

**Original File:** [net_general_layouts_mfs365_202402123.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_general_layouts_mfs365_202402123.pdf)  
**Category:** Other  
**Total Pages:** 11  
**File Size:** 319.6 KB  

---

## Page 1

 
 
 
Networking 
GENERAL RECORD LAYOUTS 
 
February 13, 2024 

---

## Page 2

 
 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 3 
Networking Record Layouts Description .......................................................................................................... 4 
Input Records’ Layout ......................................................................................................................................... 5 
Account Base Detail (F80) .................................................................................................................................. 5 
Input Records’ Layout ......................................................................................................................................... 6 
Account Base Trailer (F81) ................................................................................................................................. 6 
Input Records’ Layout ......................................................................................................................................... 7 
Account Base Transaction File Datatrak Header ............................................................................................... 7 
Input Records’ Layout ......................................................................................................................................... 8 
Account Base Transaction File Datatrak Trailer ................................................................................................. 8 
Output Records’ Layout ...................................................................................................................................... 9 
Grand Total Trailer (NGT) ................................................................................................................................... 9 
Summary of Changes – effective Q1, 2019 ...................................................................................................... 10 
 

---

## Page 3

General Record Layouts 
History of Important Notices 3 
HISTORY OF IMPORTANT NOTICES 
Dates Descriptions 
February 13, 2024 Rebranded with 2023 version & reviewed. 
July 5, 2022 Record was rebranded and reviewed. 
Effective Date: March 25, 2019 Important Notice a8658 p&s 8233 Dated December 19, 2018 (Ocode 
validation logic and introduction of Ocode Reject Codes.) 
 
 

---

## Page 4

General Record Layouts 
Networking Record Layouts Description 4 
NETWORKING RECORD LAYOUTS DESCRIPTION 
The column headings in Networking Record Layout Documents are as follows:  
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

---

## Page 5

General Record Layouts 
Input Records’ Layout 5 
INPUT RECORDS’ LAYOUT 
Account Base Detail (F80)  
Input From Fund To [[NSCC]]  
Each fund client is required to submit a file containing one record for each firm/Security Issue relationship. It 
verifies the total number of networking accounts supported in the system. 
Account Base Detail (F80) 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record type 2 3 2 N 80 = Detail R 
Filler 4 5 2 A/N Space R 
Clearing/Settling Firm # 6 9 4 N  R 
Clearing/Settling Fund # 10 13 4 N  R 
Security Issue Number 14 22 9 A/N  R 
Total Networking Accounts 23 31 9 N 999,999,999 R 
Date 32 39 8 N mmddccyy R 
TPA Number 40 43 4 A/N  O 
Filler 44 100 57 A/N Space R 

---

## Page 6

General Record Layouts 
Input Records’ Layout 6 
INPUT RECORDS’ LAYOUT 
Account Base Trailer (F81)  
Input From Fund To [[NSCC]]  
Account Base Trailer (F81) 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record type 2 3 2 N 81 = Trailer R 
Filler 4 5 2 A/N Space R 
Clearing/Settling Fund # 6 9 4 N  R 
Grand Total Networking 
Accounts 
10 17 8 N 99,999,999 R 
Total Records 18 23 6 N 999,999  
(Including Headers and Trailers) 
R 
Filler 24 100 77 A/N Space R 

---

## Page 7

General Record Layouts 
Input Records’ Layout 7 
INPUT RECORDS’ LAYOUT 
Account Base Transaction File Datatrak Header  
Input From Fund  
The account base transaction processes through a separate Networking SYSID. Each fund client  is required to 
submit a file containing one record for each firm/Security [[ID]] relationship. The record identifies the firm number, 
Security [[ID]] number, and the total Networking accounts supported in the system. [[NSCC]] uses this information 
for verification of the monthly activity captured from the position and [[Dividend]] files received throughout the 
billing cycle. The account base transaction file is submitted on the last business day of each month before   
9:00 A.M. New York time. No output files result from this data. 
Account Base Transaction File Datatrak Header 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'HDR.S' R 
DATATRAK SYSID 6 10 5 A/N Value ‘26186’ R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N Value 'NETWORKING ACCOUNT BASE’ R 
Multi Batch Indicator 60 60 1 A/N N = Not last batch  
Y = Last batch 
R 
Multi Batch Number 61 63 3 N  R 
Filler 64 100 37 A/N Space R 

---

## Page 8

General Record Layouts 
Input Records’ Layout 8 
INPUT RECORDS’ LAYOUT 
Account Base Transaction File Datatrak Trailer  
Input From Fund  
Account Base Transaction File Datatrak Trailer 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'END.S' R 
DATATRAK SYSID 6 10 5 A/N Value '26186' R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Data File Record Count 27 33 7 N DATATRAK Header & Trailer not included 
in count 
R 
Filler 34 100 67 A/N Space R 

---

## Page 9

General Record Layouts 
Output Records’ Layout 9 
OUTPUT RECORDS’ LAYOUT 
Grand Total Trailer (NGT)  
Output From [[NSCC]] to Firms and Funds  
This trailer record is available upon request. It is being used for service bureaus, transfer agents or any other 
processor who handles multiple [[NSCC]] members. 
Grand Total Trailer (NGT) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N GT = Grand Total 
Sequence # 4 4 1 A/N “1” 
Filler 5 6 2 A/N Space 
Transmit Date 7 14 8 N mmddccyy 
Total Records 15 23 9 N 999,999,999 
Filler 24 43 20 A/N GRAND TOTAL TRAILER 
File Number 44 51 8 A/N  
File Cycle 52 54 2 A/N  
Filler 55 200 147 A/N Space 
 
 

---

## Page 10

General Record Layouts 
Summary of Changes – effective Q1, 2019 10 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2019 
REJECT CODES 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 11

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: February 13, 2024 
Publication Code: MFS365 
Service: Networking 
Title: General Record Layouts 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 