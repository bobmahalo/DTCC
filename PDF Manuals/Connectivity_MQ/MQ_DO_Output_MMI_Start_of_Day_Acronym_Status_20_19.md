---
title: "20.19 MQ USER GUIDE FOR MMI  Acronym Status Output"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_DO_Output_MMI_Start_of_Day_Acronym_Status_20_19.pdf"
pages: 8
size: "111.9 KB"
category: "Connectivity_MQ"
ingested_on: "2026-06-05"
---

# 20.19 MQ USER GUIDE FOR MMI  Acronym Status Output

**Original File:** [MQ_DO_Output_MMI_Start_of_Day_Acronym_Status_20_19.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/MQ_DO_Output_MMI_Start_of_Day_Acronym_Status_20_19.pdf)  
**Category:** Connectivity_MQ  
**Total Pages:** 8  
**File Size:** 111.9 KB  

---

## Page 1

    
 
 
  CF2/MQ Transmission Guides 
 
 
 
 
20.19 MQ USER GUIDE FOR MMI  
Acronym Status Output 
 
 
 
 
 
 
The Depository Trust & Clearing Corporation November 2018


---

## Page 2

    
 
ii 
 
 
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
Publication Code: SET 108 
Service: [[settlement]] / CF2/MQ Transmission Guides 
Title: 20.19 MQ User Guide For MMI Acronym Status Output 
 
    

---

## Page 3

  Document History  
 
iii 
 
Document History 
 
09/01/15 Created  – This new MQ format document describes, specifically, the MQ output 
requirements for Deliver Order MMI Acronym Statuses as part of the MMI 
Finality Through Optimization initiative. 
12/18/15 Revision – Updated to add additional Acronym Status values. 
07/10/2016 Revision – Updated to add two new principal payment fields: PP -Amount in 
position 77 and PP-Unknown-Rate-Indicator. 
07/18/2016 Revised document number in title to 20.19. 
09/01/2016 Revision – Updated Create-Date in position 177 and Create-Time in position 185 
to show format information. 
11/30/2018 Removed formatting and references to old changes. 
 
 
  

---

## Page 4

  Contents     
iv 
 
Contents 
Copyright .................................................................................................  Error! Bookmark not defined. 
Document History ............................................................................................................................. iii 
1. Overview ....................................................................................................................................5  
2. Acronym Status Proprietary Output ............................................................................................6  
 
 

---

## Page 5

                                                   Overview 
 
20.19 MQ USER GUIDE FOR MMI START OF DAY ACRONYM STATUS  
1. Overview 
This document describes, specifically, the MQ output requirements for  MMI Acronym Statuses as part of 
the MMI Finality Through Optimization initiative. The format will be used to send the acronym status & 
total amount of transactions to IPAs. 
 
 
 

---

## Page 6

                                       Acronym Status Proprietary Output 
 
20.19 MQ USER GUIDE FOR MMI START OF DAY ACRONYM STATUS  
2. Acronym Status Proprietary Output 
The format below is an example of an MMI Acronym Status transaction. 
Field Name Position Length Field Attributes 
ACRONYM 1 04 Acronym identifier 
[[IPA]] [[participant]] [[ID]] 5 08 [[IPA]] [[participant]] Number 
STATUS 13 04 Status of the Acronym 
‘PEND’ – Pending in Optimizer 
‘ATPP’ – ATP Processing 
‘DMAK’ – Decision Maker 
‘RTPY’– Refusal to Pay 
‘TRTP’– Temporary Refusal to Pay 
‘RTPM’– Refusal to Pay by other 
IPAs if there are multiple IPAs for an 
acronym 
‘TRTM’– Temporary Refusal to Pay 
by other IPAs if there are multiple 
IPAs for an acronym 
‘PNDM’– Pending in Staging Area 
and wait for other IPAs to make a 
funding decision if there are 
multiple IPAs for an acronym 
‘PNDU’– Pending Unknown Rate 
FUNDING-TYPE 17 04 Funding Type of the Acronym 
‘FULL’ – Fully Funded 
‘PART’ – Partially Funded 
‘RTPY’ – Refusal To Pay 
‘TRTP’ – Temporary Refusal To Pay 
‘PNCL’ – Pend Cancel a Transaction 

---

## Page 7

                                       Acronym Status Proprietary Output 
 
20.19 MQ USER GUIDE FOR MMI START OF DAY ACRONYM STATUS  
Field Name Position Length Field Attributes 
in Staging Area 
‘NONE’ – No decision 
FUNDING-AMOUNT 21 14 Partially Funded Amount 
S9(12)V9(2)  
Only populated when the fund-type 
is Partially Funded. For other 
Funding types, the field will be zero. 
MP-AMOUNT 35 14 Total value of Maturity [[obligations]] 
S9(12)V9(2)  
IP-AMOUNT 49 14 Total value of Income Presentment  
S9(12)V9(2) 
RP-AMOUNT 63 14 Total value of Reorganization 
Payments 
S9(12)V9(2) 
PP-AMOUNT 77 14 Total value of Principal Payments 
S9(12)V9(2) 
PENDING-RECEIVER-AUTH 91 14 Total value of Pending Receiver 
Authorization 
S9(12)V9(2) 
AUTHORIZED-CREDITS 105 14 Total value of Authorized Credits 
S9(12)V9(2) 
NET-AMOUNT 119 14 Total value of Net Amount 
S9(12)V9(2) 
POTENTIAL-NET-AMOUNT 133 14 Total value of Potential Net Amount 
S9(12)V9(2) 
MP-UNKNOWN-RATE-PAR- 147 14 Total par value of Unknown Rate 

---

## Page 8

                                       Acronym Status Proprietary Output 
 
20.19 MQ USER GUIDE FOR MMI START OF DAY ACRONYM STATUS  
Field Name Position Length Field Attributes 
VALUE Maturity [[obligations]] 
S9(12)V9(2) 
RP-UNKNOWN-RATE-PAR-
VALUE 
161 14 Total par value of Unknown Rate 
Reorganization Payments 
S9(12)V9(2) 
IP-UNKNOWN-RATE-
INDICATOR 
175 1 Unknown Rate Income 
Presentments Indicator 
‘Y’ – There are Unknown Rate 
Income Presentments transactions 
‘N’ – There are no Unknown Rate 
Income Presentments transactions 
PP-UNKNOWN-RATE-
INDICATOR 
176 1 Unknown Rate Principal Payments 
Indicator 
“Y” – There are Unknown Rate 
Principal Presentments transactions 
“N” – There are no Unknown Rate 
Principal Presentments transactions 
CREATE-DATE 177 08 Date message created 
Format CCYYMMDD 
CREATE-TIME 185 08 Time message created 
Format: HHMMSS 
The last two bytes are spaces. 
COMMAND-REFERENCE 193 16 Reference to the command that 
triggered this message. 
FILLER 209 16 Reserved for future use 
 