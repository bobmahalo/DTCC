---
title: "20.17 MQ USER GUIDE MMI Proprietary Funding Messages"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_DO_%20Input_and_Output_for_MMI_Funding_Messages_20_17.pdf"
pages: 10
size: "125.9 KB"
category: "Connectivity_MQ"
ingested_on: "2026-06-05"
---

# 20.17 MQ USER GUIDE MMI Proprietary Funding Messages

**Original File:** [MQ_DO_ Input_and_Output_for_MMI_Funding_Messages_20_17.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_DO_%20Input_and_Output_for_MMI_Funding_Messages_20_17.pdf)  
**Category:** Connectivity_MQ  
**Total Pages:** 10  
**File Size:** 125.9 KB  

---

## Page 1

  CF2/MQ Transmission Guides 
 
 
 
 
20.17 MQ USER GUIDE  
MMI Proprietary Funding Messages 
 
 
 
 
 
 
 
The Depository Trust & Clearing Corporation     November 2018 
 
  


---

## Page 2

  Copyright  
 
20.17 MQ USER GUIDE FOR MMI Proprietary Funding Messages ii 
 
Copyright © 2018 by The Depository Trust & Clearing Corporation (“[[DTCC]]”). 
All rights reserved. This work (including, without limitation, all text, images, logos, compilation and design) is 
proprietary and protected by copyright, and is for the exclusive use of users authorized by [[DTCC]]. If this work is 
received from [[DTCC]] in any electronic medium, authorized users of this work are granted a limited, non-exclusive, 
non-transferable, non-sublicensable and freely revocable license to make reproductions and transmissions necessary 
for downloading and storage of this work on the users' computers and to print one or more paper copies from the 
electronic version for their own use. Other than to this limited extent, no part of this work (including any paper copies 
thereof or print versions thereof) may be printed, copied, altered, modified, posted, reproduced, displayed, published, 
sold, licensed, used or distributed (including by transmission) in any form or by any means, or stored in any 
information storage and retrieval system, without [[DTCC]]'s prior written permission.  
All product or service names are the property of their respective owners. 
 
 
 
 
 
 
 
 
 
 
 
Doc Info: November, 2018 
Publication Code: SET 109 
Service: [[settlement]] / CF2/MQ Transmission Guides 
Title: 20.17 - MQ MMI Proprietary Funding Messages User's Guide 
 

---

## Page 3

  Document History  
 
20.17 MQ USER GUIDE FOR MMI Proprietary Funding Messages iii 
 
Document History 
 
09/01/15 Created  – This new MQ format document describes, specifically, the MQ  input 
and output requirements for Deliver Order MMI funding messages as part of the 
MMI Finality Through Optimization initiative. 
10/14/16 Added the [[IPA]] [[participant]] [[ID]] field ( position 151) and changed Filler to position 
159. Both fields appear in section 3. [[participant]] Confirmation –  [[settlement]] 
Output. 
11/30/2018 Removed formatting and references to old changes. 
 
 
  

---

## Page 4

  Contents     
20.17 MQ USER GUIDE FOR MMI Proprietary Funding Messages iv 
 
Contents 
Copyright .................................................................................................  Error! Bookmark not defined. 
Document History ............................................................................................................................. iii 
1. Overview ....................................................................................................................................5  
2. Funding Messages – Proprietary Funding Messages .....................................................................6  
DMA1 Standard Transaction Header - [[settlement]] Input ......................................................................... 6 
DMA Input Record .................................................................................................................................... 6 
DMA1 Error Codes .................................................................................................................................... 8 
3. [[participant]] Confirmation – [[settlement]] Output ............................................................................9  
 
 

---

## Page 5

                                                              Overview 
20.17 MQ USER GUIDE FOR MMI Proprietary Funding Messages 5 
 
1. Overview 
This document describes the MQ input/output requirements for Deliver Order funding messages as part of 
the MMI Finality Through Optimization initiative. These messages will be used by IPAs to send funding 
messages to [[DTC]] and receive confirmation messages from [[DTC]]. 
 
 
 

---

## Page 6

                                                   MMI Proprietary Funding Messages - [[settlement]] Input 
 
20.17 MQ USER GUIDE FOR MMI Proprietary Funding Messages 6 
 
2. Funding Messages – Proprietary Funding Messages 
DMA1 Standard Transaction Header - [[settlement]] Input  
The Decision Making Application (DMA) is an application IPAs use to acknowledge funding for an acronym.  
Position Length Format Field Name Field Description 
1-1 1 Character Feedback 
Indicator 
Blank on input. Output, used to Indicate if 
any errors were encountered during 
processing 
2-2 1 Character Production/ 
Test 
Indicator 
P= Production 
T= Test 
3-8 6 Character Record Type MMIDMA 
9-10 2 Numeric Record 
Suffix 
Indicator of the Record Number on single 
and multiple data records within a 
transaction 
11-12 2 Numeric Version 
Number 
Indicator of which version the data is in; 
for example: latest or previous format 
13-18 6 Character User 
Reference 
Number 
Optional unique transmitter defined 
transaction identifier 
19-26 8 Character Addressee The entity on behalf of whom the 
transaction is being Processed. Right 
justified, zero filled for numeric addressee 
or ‘Mnnnnnnn’ for non-numeric 
addressee. 
DMA Input Record 
The DMA Input record allows the [[IPA]] to make funding decisions for an acronym.  This command will allow 
them to fund the acronym, cancel a transaction pending in the staging engine, or issue a refusal to pay. 
Position Length Format Field Name Field Description 
27-34 8 Numeric 
9(8) 
[[IPA]] Funding 
Agent [[ID]] 
Valid [[DTCC]] [[participant]] [[ID]] 
35-38 4 Character 
X(4) 
Acronym Acronym Code. The acronym 
that the command will act 
upon. 

---

## Page 7

                                                   MMI Proprietary Funding Messages - [[settlement]] Input 
 
20.17 MQ USER GUIDE FOR MMI Proprietary Funding Messages 7 
 
Position Length Format Field Name Field Description 
Required for FULL, PART, 
RTPY, TRTP 
 
39-42 4 Character 
X(4) 
Funding 
Type 
FULL = Fully Funded 
PART = Partially Funded 
RTPY = Refusal to Pay 
TRTP = Temporary Refusal to Pay 
PNCL = Pend Cancel 
43-56 14 Numeric 
9(12)V9(2) 
Funding 
Amount 
Required for PART funding type 0 
for other Funding Type 
55-106 50 Character Contact 
Name 
Optional Field 
Contact Person Name 
107-116 10 Character Contact 
Phone 
Optional Field 
 Contact Person's Phone Number 
117-171 55 Character [[IPA]] 
Comments 
Optional Field 
172-187 16 Character IMS Tran 
[[ID]] 
Required for PNCL command to 
indicate which transaction will be 
cancelled in the staging area 
188-200 13 Character  Filler  Reserved for future use  
  
  

---

## Page 8

                                                   MMI Proprietary Funding Messages - [[settlement]] Input 
 
20.17 MQ USER GUIDE FOR MMI Proprietary Funding Messages 8 
 
 
DMA1 Error Codes 
Field Code Error Code Explanation 
JAAA 9AAL Function past cutoff 
JAAA 9ABJ Function is quiesced 
CAAK 9AAA [[IPA]] Funding Agent [[ID]] is invalid 
CAAK 9AAF [[IPA]] Funding Agent [[ID]] is not numeric 
CAJC 9AAA Acronym is invalid 
CAJC 9ABB Acronym Not Found 
CAJF 9AAA Funding Type is invalid 
CAJE 9AAA Funding Amount is invalid 
AZZZ 9ACO Transaction Not Found in Database 
AZZZ 9AAA Transaction is invalid 
 
 
 
 
  

---

## Page 9

                                                   MMI Proprietary Funding Messages – [[participant]] Confirmation 
 
20.17 MQ USER GUIDE FOR MMI Proprietary Funding Messages 9 
 
3. [[participant]] Confirmation – [[settlement]] Output 
Field Name Position Length  Field Attributes 
CREATE-DATE 1 08 Date message created 
CREATE-TIME 9 08 Time message created 
REFERENCE-[[ID]] 17 16 Reference [[ID]] of transaction/command 
that trigged message. 
STATUS 33 04 ‘RCVD’ – Received 
‘ACPT’ – Accepted 
‘NACT’ – Not Accepted 
‘INFO’ – Informational 
REASON-CODE 37 04 ‘PROF’ –  Processed due to 
                 Partially/Fully Funded  
                 Message; or 
                 Funding profile has been 
                 accepted 
‘ANFF’  –  Issuances not exceed 
                 Maturities due to no enough 
                 fund  
‘UNRT’  –  Not processed due to  
                  unknown rate for acronym 
‘MPRP’  –  Partially Funded Message 
                  not processed due to no 
MPs 
‘FUND’  –  Partially Funded Message 
                 not processed because the  
                 funding amount is less than  
                 the current partial funding 
REASON-TEXT 41 80 Text of reason code 
ACRONYM 121 04 [[ID]] of the Acronym 
FUNDING-TYPE-
INDICATOR 
125 04 Funding Type of the Acronym 
‘FULL’ – Fully Funded 
‘PART’ – Partially Funded 
‘RTPY’ – Refusal To Pay 
‘TRTP’ – Temporary Refusal To Pay 
‘PNCL’ – Pend Cancel A Transaction in 
               Staging Area 
FUNDING-AMOUNT 129 14 Amount being funded partially 
Only used for Partially Funded Type 
For other fund types, the field will be 
zero. 
S9(12)V9(2) 

---

## Page 10

                                                   MMI Proprietary Funding Messages – [[participant]] Confirmation 
 
20.17 MQ USER GUIDE FOR MMI Proprietary Funding Messages 10 
 
Field Name Position Length  Field Attributes 
[[settlement]]-DATE 143 08 [[settlement]] date 
[[IPA]]-PART-[[ID]] 151 08 [[IPA]] Funding Agent [[ID]].  Must be a valid 
[[DTCC]] [[participant]] [[ID]].  Numeric eight-
digit format.  
Example 
12345678 
FILLER 159 16 Reserved for future use 
 