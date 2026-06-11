---
title: "Networking Records - Extended Share Balance: Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs302_net_extendedshare_balance_bp_20230726.pdf"
pages: 7
size: "377.3 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Networking Records - Extended Share Balance: Best Practices

**Original File:** [mfs302_net_extendedshare_balance_bp_20230726.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs302_net_extendedshare_balance_bp_20230726.pdf)  
**Category:** Other  
**Total Pages:** 7  
**File Size:** 377.3 KB  

---

## Page 1

 
 
 
Networking 
NETWORKING RECORDS - EXTENDED SHARE 
BALANCE BEST PRACTICES 
JULY 26, 2023 
 

---

## Page 2

REVISION HISTORY 
Date Changes 
July 26, 2023 Document rebranded. Content reviewed and refreshed.  One link modified. 
April 8, 2021 Document rebranded 

---

## Page 3

 
 
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 4 
Background & Objective ..................................................................................................................................... 4 
Networking Records ............................................................................................................................................ 4 
Best Practices ....................................................................................................................................................... 5 
Best Practice: Populating 13 Byte Share Balance Field(s) Field vs. 16 Byte "Extended" Field ......................... 5 
Best Practice: Populating Fields with Zeros and/or Values ................................................................................ 5 
Extended Share Balance Workflows ................................................................................................................... 6 
 

---

## Page 4

Networking Records - Extended Share Balance Best Practices 
Overview 4 
OVERVIEW 
Background & Objective 
Members of the Investment Company Institute's [[Broker]]/Dealer Advisory Committee recommended 
enhancements to accommodate the transmission of share balances exceeding the existing 13-byte length. 
Based upon industry feedback and internal research, [[DTCC]] concluded that to accommodate the larger share 
balance fields, a 16-byte Share Balance – Extended field needed to be created for impacted files. 
The Share Balance – Extended field allows participants to accurately communicate and reconcile share 
balances exceeding 1 billion [[shares]]. 
Networking Records 
The scope of the "best practices" contained in this document are applicable to the following Networking records 
and fields: 
• Account Conversion/Update & Transfer/Acknowledgment  
o Transfer Detail/Fund Acknowledgement (A/B/T52, F53) # 2 & # 4 
• Activity Reporting 
o Activity Detail (F55) #1 & #4 
• [[Dividend]] Reporting 
o [[Dividend]]/Capital Gain Detail for Cash Accounts Not Subject to Withholding (F63) #1 
o [[Dividend]]/Capital Gain Detail for Cash Accounts Subject to Withholding (F64) #1 & #2 
o [[Dividend]]/Capital Gain Detail for Reinvest Accounts Not Subject to Withholding (F65) #1 & #2 
o [[Dividend]]/Capital Gain Detail for Reinvest Accounts Subject to Withholding (F66) #1 & #2 
• Position Reporting 
o Position Detail (F58) # 1 & #2 
o Position Trailer (F59) #2 
 
 

---

## Page 5

Networking Records - Extended Share Balance Best Practices 
Best Practices 5 
BEST PRACTICES 
Best Practice: Populating 13 Byte Share Balance Field(s) Field vs. 16 
Byte "Extended" Field 
The best practices outlined below are to accommodate the transmission of share balances which exceed the    
13-byte share balance field(s). The  best practice is to ONLY populate the 16-byte Share Balance – Extended 
field when the share balance exceeds the 13 -byte Share Balance field. 
Best Practice: Populating Fields with Zeros and/or Values 
Only one share balance field (either the 16-byte Share Balance – Extended field or the 13-byte Share Balance 
field) should be populated with a valid value when the file is being transmitted. The other share balance field 
should be left blank. 
Because the impacted fields are share balances, zero is a valid value. Please see Table 1 for the full list of 
[[DTCC]]'s editing methodology: 
 
Table 1 [[DTCC]]'s Editing Methodology 
 Share balance 13-byte field value Share balance – extended 16-byte field value Accept / Reject 
1 Greater than zero Space or zero Accept 
2 Space or zero Greater than zero Accept 
3 Greater than zero Greater than zero Reject 
4 Zero Zero Accept 
5 Zero Space Accept 
6 Space Zero Accept 
7 Space Space Reject 
8 Non-numeric Greater than zero or zero Reject 
9 Greater than zero or zero Non-numeric Reject 
10 Greater than zero or zero Record sequence with a 16-byte field is not provided Accept 
11 Space Record sequence with a 16-byte field is not provided Reject 
 
 
Note 
The validation rules in Table 1 are not applicable to the Total Share Balance 15-byte and 17-byte fields in the Position 
Trailer record F59. 
 

---

## Page 6

Networking Records - Extended Share Balance Best Practices 
Best Practices 6 
Extended Share Balance Workflows 
 
 
 
 
 
Figure 1 - Workflow for Share Balances that [[DO]] NOT Exceed 13 Bytes 
Figure 2 - Workflow for Share Balances that Exceed 13 Bytes 

---

## Page 7

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date:  July 26, 2023 
Publication Code: MFS302 
Service: Networking 
Title: Networking Records - Extended Share Balance: Best Practices 
For More Information 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com  