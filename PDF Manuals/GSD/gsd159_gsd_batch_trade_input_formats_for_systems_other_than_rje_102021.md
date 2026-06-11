---
title: "GSD Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE "
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd159_gsd_batch_trade_input_formats_for_systems_other_than_rje_102021.pdf"
pages: 14
size: "274.1 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 

**Original File:** [gsd159_gsd_batch_trade_input_formats_for_systems_other_than_rje_102021.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd159_gsd_batch_trade_input_formats_for_systems_other_than_rje_102021.pdf)  
**Category:** GSD  
**Total Pages:** 14  
**File Size:** 274.1 KB  

---

## Page 1

  
 
 
 
[[FICC]] – [[GSD]] 
[[GSD]] BATCH TRADE INPUT FORMATS FOR ALL TYPES OF TRANSMISSION 
SYSTEMS OTHER THAN RJE  
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
Publication Code: GSD159 
Service: [[FICC]] – [[GSD]]   
Title: [[GSD]] Batch Trade Input Formats for All Types of Transmission Systems other than RJE 
 
 
The [[GSD]] Batch Trade Input Formats for All Types of Transmission Systems other than RJE (hereinafter, the "document") is 
provided as a convenience to Members and is for information purposes only. Although [[FICC]] may make this document 
available to Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have a 
continuing obligation to make available this document or other related information of a certain type.  
 
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
Trade Input Formats For Systems Other Than RJE ......................................................................................... 5 
DATATRAK Header Record ............................................................................................................................... 5 
Application Detail Record – Instruct / Replace (INST / REPL) ........................................................................... 6 
Application Detail Record – Cancel (CAN) ......................................................................................................... 9 
Application Detail Record – Modification of External Reference Number (MFX) ............................................. 10 
Application Detail Record – Modification of Commission (MFC) ...................................................................... 11 
Application Trailer Record ................................................................................................................................ 12 
DATATRAK Trailer Record - Production .......................................................................................................... 13 
 

---

## Page 4

[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 
Overview 4 
 
OVERVIEW 
[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems other than RJE  
Currently, [[GSD]] Members can submit DVP trades in a single or multi-batch method pursuant to [[GSD]] Rules, 
using SWIFT formats. This document details those specifications required for [[Member]] submission of batch 
files, which may be used in support of [[GSD]]’s products and services.  
Audience 
This document was written for systems and development personnel including managers, analysts and 
programmers of [[GSD]] [[Member]] firms. It presumes readers are familiar with technical concepts and terms as 
well as having a [[BASIC]] understanding of [[GSD]]'s products and services. 
Communication 
For information on [[FICC]] Connectivity, please contact [[FICC]] Integration at ficcintegration@[[DTCC]].com. 
  

---

## Page 5

[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 
Trade Input Formats For Systems Other Than RJE 5 
 
TRADE INPUT FORMATS FOR SYSTEMS OTHER THAN 
RJE 
DATATRAK Header Record 
DATATRAK Header Header 
Description Length Start End Type Comments 
Constant 1 5 1 5 A/N Always = ‘HDR.S’ 
DATATRAK SYSID 5 6 10 N System Identifier                                      
Production = 62371                                   
Test = 42371 
Constant 2 2 11 12 A/N Always = '.E' 
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
File Description 25 35  A/N Free form – field not validated 
Multi-Batch Indicator 1 60  A/N Space = No Multi-Batch                               
N = Multi-Batch, Not Last                             
Y = Multi-Batch, Last 
Multi-Batch Number 3 61 63 A/N Spaces = No Multi-Batch                               
Sequential # starting with 001 = Multi-Batch 
Reversed for Future Use 1 64 64 A/N Reserved 
Variable Length Record 
Indicator 
1 65 65 A/N 
Variable Length = ‘∗’                                        
Fixed Length = Space                                        
This file is fixed-length, so a space is 
expected in this field. 
Reserved for Future Use 335 66 400 A/N Spaces 
 END OF RECORD 
  

---

## Page 6

[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 
Trade Input Formats For Systems Other Than RJE 6 
 
Application Detail Record – Instruct / Replace (INST / REPL) 
Field Name Length Start End Type Comments 
Record Number 5 1 5 A/N Starting with 00001, in strict sequential 
order regardless of the Command Type 
Record Size 5 6 10 A/N Always = 00400 
Filler 5 11 15 A/N Always = Spaces 
Segment Number 1 16 16 A/N Always = 3 
Password 12 17 28 A/N To be assigned by [[GSD]] 
Command Type 4 29 32 A/N Always = ‘CAN’ (Left, Justified, Blank Filled) 
[[Member]] [[ID]] 4 33 36 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 6 37 42 A/N Always = Spaces 
[[Broker]] Reference Number 16 43 58 A/N [[Broker]]’s Reference Number. Required if the 
submitter is a [[Broker]], otherwise field must 
be left blank (Left Justified, Blank Filled). 
Filler 4 59 62 A/N Always = Spaces 
External Reference Number 16 63 78 A/N The Control Reference Number of the trade, 
provided by the [[Member]]. The transaction is 
modified using the External Reference 
Number in this field only if the Transaction 
[[ID]] field is blank (Left Justified, Blank Filled). 
Filler 4 79 82 A/N Always = Spaces 
Transaction Type 4 83 86 A/N One of the following:                                            
‘BUY’  (For Cash Trades)                                  
‘SELL’ (For Cash Trades)                                       
‘REPO’ (Identifies the [[Member]] delivering 
out [[securities]] on Start Date and receiving 
the [[securities]] back on [[settlement]] (End) 
Date.                                                           
‘REVR’ (Identifies the [[Member]] receiving the 
[[securities]] on Start Date and delivering bank 
the [[securities]] on [[settlement]] (End) Date).   
Trade Date 8 87 94 A/N MMDDYYYY – Cannot be greater than 
today 
[[settlement]] Date 8 95 102 A/N MMDDYYYY – Must be greater than or 
equal to the Trade Date. For Repos, this is 
the [[settlement]] (End) Date of the End Leg.  
[[CUSIP]] Number 9 103 111 A/N [[CUSIP]] Number 
Filler 6 112 117 A/N Always = Spaces 
Quantity 18 118 135 A/N The Par amount of the trade. Punctuation 
may be included. Left Justified, Blank Filled. 
Punctuation may be included. Cents may 

---

## Page 7

[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 
Trade Input Formats For Systems Other Than RJE 7 
 
Field Name Length Start End Type Comments 
be exclude. i.e., ‘1,250,000         ‘ or 
‘1.25MM         ‘. 
Price / Repo Rate 14 136 149 A/N For Cash Trades, it is the Contract Price, 
i.e., 
'8.125         ' or 
'8 32/256         ' or 
'97-1/8         '. 
For Repo/Revr Trades, it is the Contract 
Repo Rate on the trade, i.e., 
'4-1/8         ' or 
'4.125         ' or 
'-1-1/4         '. 
(Left Justified, Blank Filled) 
Pricing Method 1 150 150 A/N ‘Y’ = Yield                                                         
‘P’ = Dollar Price                                             
‘R’ = Contract Repo Rate (For Repo trades 
only) 
                                                                 
(Optional Field) 
Net Money 18 151 168 A/N The final [[settlement]] dollar amount for the 
trade. Format is the as Quantity. 
Contra Firm 4 169 172 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 6 173 178 A/N Always = Spaces 
Commission 11 179 189 A/N Used for When-Issued (WI) trades of 
coupon bearing instrument, before auction, 
when pricing method = ‘Y’, i.e., ‘0.008         ‘ 
or ‘1/256         ‘. 
(Left Justified, Blank Filled) 
Filler 4 190 193 A/N Always = Spaces 
Trade Time 6 194 199 A/N HHMMSS. i.e., 1:20 P.M. = 132000                
(Optional Field)                                 
[[Member]]’s Executing Firm 5 200 204 A/N Executing Firm associated with [[Member]]. 
Field will [[default]] to Submitting [[Member]]’s [[ID]] 
Number if field is left blank.                             
(Optional Field)  
Contra’s Executing firm 5 205 209 A/N Executing Firm associated with Contra 
[[Member]]. Field will [[default]] to Contra 
[[Member]]’s [[ID]] Number if field is left blank.                             
(Optional Field) 
  Locked-in 1 210 210 A/N Must be ‘Y’ if entered by the Submitter. 
Must be left blank if this is not a Locked-In 
Submission. 

---

## Page 8

[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 
Trade Input Formats For Systems Other Than RJE 8 
 
Field Name Length Start End Type Comments 
Submitter [[ID]] 4 211 214 A/N Can be entered by authorized Locked-In 
Submitters. Must be the same as the 
[[Member]] [[ID]] Number. 
Filler 6 215 220 A/N Always = Spaces 
Start Money 18 221 238 A/N The dollar amount being lent in the Repo 
Start Leg. Format is the same as Quantity. 
Must be blank for Cash trades.  
Start Date 8 239 246 A/N MMDDYYYY - For Repos, this is the 
[[settlement]] Date of the Start Leg. Must be 
left blank for Cash trades. 
Secondary Reference 
Number 
16 247 262 A/N 
May be used by the submitting party for 
Repo trades only. Must be entered as 
spaces if not used for Repo trades. Must be 
left blank for Cash trades.                            
    
(Optional Field for Repo/Revr trades) 
Filler 4 263 266 A/N Always = Spaces 
Give-up [[Broker]] 10 267 276 A/N As assigned by [[GSD]] or assigned by the 
[[Member]] as the in-house [[ID]] for the [[Broker]]. 
Must be left blank for Cash trades.     
(Optional Field for Repo/Revr trades) 
  Filler 124 277 400 A/N Always = Spaces 
Note: 
All fields are mandatory unless otherwise specified.  

---

## Page 9

[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 
Trade Input Formats For Systems Other Than RJE 9 
 
Application Detail Record – Cancel (CAN) 
Field Name Length Start End Type Comments 
Record Number 5 1 5 A/N Starting with 00001, in strict sequential 
order regardless of the Command Type 
Record Size 5 6 10 A/N Always = 00400 
Filler 5 11 15 A/N Always = Spaces 
Segment Number 1 16 16 A/N Always = 3 
Password 12 17 28 A/N To be assigned by [[GSD]] 
Command Type 4 29 32 A/N Always = ‘CAN’ (Left, Justified, Blank Filled) 
[[Member]] [[ID]] 4 33 36 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 6 37 42 A/N Always = Spaces 
External Reference Number 16 43 58 A/N The Control Reference Number of the trade, 
provided by the [[Member]]. The transaction is 
modified using the External Reference 
Number in this field only if the Transaction 
[[ID]] field is blank (Left Justified, Blank Filled). 
Filler 4 59 62 A/N Always = Spaces 
Transaction [[ID]] 11 63 73 A/N Transaction [[ID]] assigned to the trade by 
[[GSD]]. If field is left blank, the transaction will 
be cancelled using the External Reference 
Number. 
Filler 327 74 400 A/N Always = Spaces 
  

---

## Page 10

[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 
Trade Input Formats For Systems Other Than RJE 10 
 
Application Detail Record – Modification of External Reference 
Number (MFX) 
Field Name Length Start End Type Comments 
Record Number 5 1 5 A/N Starting with 00001, in strict sequential 
order regardless of the Command Type 
Record Size 5 6 10 A/N Always = 00400 
Filler 5 11 15 A/N Always = Spaces 
Segment Number 1 16 16 A/N Always = 3 
Password 12 17 28 A/N To be assigned by [[GSD]] 
Command Type 4 29 32 A/N Always = ‘MFX’ (Left, Justified, Blank Filled) 
[[Member]] [[ID]] 4 33 36 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 6 37 42 A/N Always = Spaces 
External Reference Number 16 43 58 A/N The Control Reference Number of the trade, 
provided by the [[Member]]. The transaction is 
modified using the External Reference 
Number in this field only if the Transaction 
[[ID]] field is blank (Left Justified, Blank Filled). 
Filler 4 59 62 A/N Always = Spaces 
Transaction [[ID]] 11 63 73 A/N Transaction [[ID]] assigned to the trade by 
[[GSD]]. If field is left blank, the transaction will 
be modified using the External Reference 
Number. 
New External Reference 
Number 
16 74 89 A/N The Control Reference Number of the trade, 
provided by the [[Member]]. This field cannot 
contain a duplicate External Reference from 
a another a trade in the system unless the 
original trade was cancelled prior to the 
submission of this record (Left Justified, 
Blank Filled). 
Filler 311 90 400 A/N Always = Spaces 
  

---

## Page 11

[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 
Trade Input Formats For Systems Other Than RJE 11 
 
Application Detail Record – Modification of Commission (MFC) 
Field Name Length Start End Type Comments 
Record Number 5 1 5 A/N Starting with 00001, in strict sequential 
order regardless of the Command Type 
Record Size 5 6 10 A/N Always = 00400 
Filler 5 11 15 A/N Always = Spaces 
Segment Number 1 16 16 A/N Always = 3 
Password 12 17 28 A/N To be assigned by [[GSD]] 
Command Type 4 29 32 A/N Always = ‘MFC’ (Left, Justified, Blank Filled) 
[[Member]] [[ID]] 4 33 36 A/N [[GSD]] [[Member]] [[ID]] Number 
Filler 6 37 42 A/N Always = Spaces 
External Reference Number 16 43 58 A/N The Control Reference Number of the trade, 
provided by the [[Member]]. The transaction is 
modified using the External Reference 
Number in this field only if the Transaction 
[[ID]] field is blank (Left Justified, Blank Filled). 
Filler 4 59 62 A/N Always = Spaces 
Transaction [[ID]] 11 63 73 A/N Transaction [[ID]] assigned to the trade by 
[[GSD]]. If field is left blank, the transaction will 
be modified using the External Reference 
Number. 
New Commission 11 74 84 A/N Left Justified, Blank Filled. i.e., ‘0.008         ‘ 
or ‘1/256         ‘. 
New Amount  18 85 102 A/N Left Justified, Blank Filled. Punctuation may 
be included. Cents may be exclude. i.e., 
‘1,250,000         ‘ or ‘1.25MM         ‘. 
Filler 298 103 400 A/N Always = Spaces 
  

---

## Page 12

[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 
Trade Input Formats For Systems Other Than RJE 12 
 
Application Trailer Record 
Field Name Length Start End Type Comments 
Trailer [[ID]] 5 1 5 A/N Always = “TRAIL” 
Record Count 5 6 10 N Total Number of records in file 
Filler 22 11 32 A/N Always = Spaces 
Submitting Firm 4 33 36 N [[GSD]] [[Member]] [[ID]] Number 
Filler 364 37 400 A/N Always = Spaces 
 
 
 
 
 
 
  

---

## Page 13

[[GSD]] Batch Trade Input Formats for All Types of Transmission Systems Other Than RJE 
Trade Input Formats For Systems Other Than RJE 13 
 
DATATRAK Trailer Record - Production 
DATATRAK Trailer Trailer 
Field Name Length Start End Type Comments 
Constant 1 5 1 5 A/N Always = ‘END.S’ 
DATATRAK SYSID 5 6 10 A/N System Identifier                                      
Production = 62371                                     
Test = 42371 
Constant 2 2 11 12 A/N Always = '.E'  
Constant 3 2 13 14 N Always = ‘00’ 
Constant 4 2 15 16 A/N Always = ‘.C’  
Originator 4 17 20 A/N [[GSD]] [[Member]] [[ID]] Number                              
Will be 4 characters for firms submitting on 
their own behalf. 
Constant 5 2 21 22 A/N Always = ‘.S’  
Sub-originator 4 23 26 A/N [[GSD]] [[Member]] [[ID]] Number                              
Will be 4 characters for firms submitting on 
their own behalf. 
Record Count  7 27 33 N Optional Field. Count of data file records. 
Reserved for Future Use 367 34 400 A/N Spaces 
 END OF RECORD 
 
  

---

## Page 14

 
  
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 