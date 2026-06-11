---
title: "ISO 20022 Messaging Subscription Options"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Subscription_Options-ISO_20022_20210224.pdf"
pages: 11
size: "314.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO 20022 Messaging Subscription Options

**Original File:** [Subscription_Options-ISO_20022_20210224.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Subscription_Options-ISO_20022_20210224.pdf)  
**Category:** Other  
**Total Pages:** 11  
**File Size:** 314.6 KB  

---

## Page 1

 
 
 
 
CORPORATE ACTIONS 
ISO 20022 MESSAGING SUBSCRIPTION OPTIONS 
VERSION 2.2 
FEBRUARY 23, 2021 
 
 
  


---

## Page 2

© 2021 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Info: February 23, 2021  
Publication Code: CA218 
Service: Corporate Actions 
Title: ISO 20022 Messaging Subscription Options 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Announcements ................................................................................................................................................... 4 
Distribution Events .............................................................................................................................................. 5 
Redemption Events .............................................................................................................................................. 7 
Reorganization Events ........................................................................................................................................ 9 
 

---

## Page 4

ISO 20022 Messaging Subscription Options 
Announcements 4 
ANNOUNCEMENTS 
ANNOUNCEMENTS  
CANO/CACN Subscription 
MQ Delivery File Transmission* Included Activity 
Real Time** Automatic 
Delivery 
1:30 AM 
3:30 AM 
6:00 AM 
9:00 AM 
11:00 AM 
12:00 AM 
1:00 PM 
2:00 PM 
3:00 PM 
4:00 PM 
5:00 PM 
6:00 PM 
7:00 PM 
8:00 PM (End of Day) 
9:00 PM 
11:30 PM 
9:00 AM (Saturday) 
 
*Any or all file times 
can be selected 
• Any available Announcements for the 
following issue and event types can 
be selected: 
o CD Early Redemption/PUT 
(with Survivor [[Option]]) 
o Distribution 
o Factors 
o Maturity Cash 
o Municipals New 
o Municipals Updates 
o Redemption 
o Meeting 
o MMI Commercial Paper 
o Reorganization 
 
 
 

---

## Page 5

ISO 20022 Messaging Subscription Options 
Distribution Events 5 
DISTRIBUTION EVENTS 
DISTRIBUTION EVENTS  
CANO-E Subscription 
MQ Delivery File 
Transmission*  Included Activity 
2:00 PM 2:00 PM • P&I late announcements created before 
1:45 PM on payable date 
11:30 PM 11:30 PM 
 
 
• Record Date Entitlements (Eligible Balance) 
resulting from money Market Instrument 
(MMI) and Principal & Interest (P&I) 
Distributions 
 
CAPA Subscription 
MQ Delivery File 
Transmission*  Included Activity 
1:30 AM 1:30 AM • Projected Allocations or Cancelled 
Projections resulting from all Canadian 
Dollar, Money Market Instrument (MMI), 
Principal & Interest (P&I) and [[Stock]] 
Distributions 
• NEWM messages sent on pay date minus 7 
days and REPL messages sent on pay date 
minus 1 day  - OR - 
NEWM messages sent on pay date minus 7 
days plus REPL (replacement/delta) 
messages sent each day thereafter until 
REPL messages pay date minus 1 day 
 
 
CAPC Subscription 
MQ Delivery File 
Transmission*  Included Activity 
1:30 AM and hourly on the 
half hour between 10:30 
AM ET and 6:30 PM ET   
 
1:30 AM • Projected Allocations or Cancelled 
Projections resulting from all Canadian 
Dollar, Money Market Instrument (MMI), 
Principal & Interest (P&I) and [[Stock]] 
Distributions 
• NEWM messages sent on pay date minus 7 
days and REPL messages sent on pay date 
minus 1 day - OR - 
NEWM messages sent on pay date minus 7 
days plus REPL (replacement/delta) 
messages sent each day thereafter until 
REPL messages pay date minus 1 day 
 
 
  

---

## Page 6

ISO 20022 Messaging Subscription Options 
Distribution Events 6 
CACO/CARE Subscription 
Note: CARE messages are only sent for P&I events 
MQ Delivery File 
Transmission*  Included Activity 
For MMI and P&I: Every 20 
minutes from 8:20 AM ET 
to 4:30 PM ET;  
For STKD: 8:20 AM ET and 
7:00 PM ET  
  
4:00 PM 
 
• Any available Money Market Instrument 
(MMI) Distribution Allocations and Principal 
& Interest (P&I) Allocations 
• Could also include any available [[Stock]] or 
Cash Allocations 
 
7:00 PM • Any available [[Stock]] Allocations 
• Could also include any available Cash 
Allocations 
 
1:30 AM • Any available [[Stock]] Allocations 
• Could also include any available Cash 
Allocations 
 
 
CAPS Subscription 
MQ Delivery File 
Transmission*  Included Activity 
Hourly from 1 PM to  
7 PM ET  
 
4:00 PM • Unallocated positions resulting from 
Canadian Dollar and Money Market 
Instrument (MMI) Distribution events 
 
5:00 PM • Unallocated positions resulting from 
Principal & Interest (P&I) Distribution events 
 
7:00 PM • Unallocated positions resulting from [[Stock]] 
Distribution events 
• Could also include any Unallocated 
positions resulting from Principal & Interest 
(P&I) Distribution events 
 
CAIS/CACS Subscription 
MQ Delivery File 
Transmission*  Included Activity 
Real Time** Automatic 
Delivery 
N/A • CAIS is an instruction reply for EDS Eligible 
events in correspondence with an incoming 
CAIN Instruction/Election message 
• CACS is a Withdrawal Reply for EDS 
Eligible events in correspondence with an 
incoming CAIC Instruction/Election 
withdrawal message 
 
CAST Subscription 
MQ Delivery File 
Transmission*  Included Activity 
10 PM ET 10 PM ET • Corporate Actions Instructions Report for 
Elective Dividends 
 
 

---

## Page 7

ISO 20022 Messaging Subscription Options 
Redemption Events 7 
REDEMPTION EVENTS 
REDEMPTION EVENTS  
CANO-E Subscription 
MQ Delivery File 
Transmission*  Included Activity 
12:30 AM 
1:45 PM  
5:30 PM 
6:50 PM 
12:30 AM 
1:45 PM  
5:30 PM 
6:50 PM 
• Record Date Entitlements (Eligible Balance) 
resulting from Lottery events 
 
CAPA Subscription 
MQ Delivery File 
Transmission*  Included Activity 
12:30 AM  
10:45 AM  
1:30 PM 
2:30 PM 
5:30 PM 
12:30 AM  
10:45 AM  
1:30 PM 
2:30 PM 
5:30 PM 
• Any available Projected Allocations resulting 
from Lottery events 
• Could also include any available Projected 
Allocations resulting from any Redemption 
event including Non-Lottery events (Full Call 
etc.) and Maturities 
 
1:30 AM 1:30 AM • Any available Projected Allocations resulting 
from all Redemption events (Non-Lottery and 
Maturities) 
 
 
CAPC Subscription 
MQ Delivery File 
Transmission*  Included Activity 
1:30AM, Hourly from 
10:30 AM to 6:30 PM ET  
 
12:30 AM  
10:45 AM  
1:30 PM 
2:30 PM 
5:30 PM 
• Any available Cancelled Projections resulting 
from Lottery events 
• Could also include any available Cancelled 
Projections resulting from any Redemption 
event including Non-Lottery events (Full Call 
etc.) and Maturities 
 
1:30 AM 1:30 AM • Any available Cancelled Projections resulting 
from all Redemption events (Non-Lottery and 
Maturities) 
 
 
  CACO Subscription 
MQ Delivery File 
Transmission* Included Activity 
Every 20 minutes  
from 8:20 AM ET to  
5:30 PM ET  
 
12:30 AM 
10:45 AM 
1:30 PM 
2:30 PM 
5:30 PM 
• Any available Allocations resulting from 
Lottery events and any available advices of 
allocation reversals 
• Could also include any available Allocations 
resulting from any Redemption event 
including Non-Lottery events (Full Call etc.) 
and Maturities 
 

---

## Page 8

ISO 20022 Messaging Subscription Options 
Redemption Events 8 
 4:00 PM • Any available Allocations resulting from any 
Redemption event including Lottery, Non-
Lottery events (Full Call etc.) and Maturities  
 
 
CAPS Subscription 
MQ Delivery File 
Transmission*  Included Activity 
Hourly from 1 PM to  
7 PM ET 
 
4:00 PM, 
5:00 PM,  
7:00 PM 
• Any Unallocated Positions resulting from 
Lottery, Non-Lottery and Maturity events 
 
 

---

## Page 9

ISO 20022 Messaging Subscription Options 
Reorganization Events 9 
REORGANIZATION EVENTS 
REORGANIZATION EVENTS  
CANO-E Subscription 
MQ Delivery File 
Transmission*  Included Activity 
12:00 PM,  
1:30 PM,  
4:00 PM,  
4:30 PM,  
5:00 PM,  
8:00 PM 
12:00 PM,  
1:30 PM,  
4:00 PM,  
4:30 PM,  
5:00 PM,  
8:00 PM 
• Record Date Entitlements (Eligible Balance) 
resulting from Reorganization events 
 
CACO Subscription 
MQ Delivery File 
Transmission*  Included Activity 
8 AM to 3:15 PM Real 
Time Automatic Delivery 
4:00 PM • Allocations resulting from all Reorganization 
events 
 
 
CAPA Subscription 
MQ Delivery File 
Transmission*  Included Activity 
1:10 AM 1:30 AM • Projected Allocations or Cancelled 
Projections resulting from all Reorganization 
events  
• NEWM messages sent on pay date minus 7 
days and REPL messages sent on pay date 
minus 1 day  - OR - 
NEWM messages sent on pay date minus 7 
days and REPL (replacement/delta) 
messages sent each day thereafter until 
REPL messages pay date minus 1 day 
 
 
CAPS Subscription 
MQ Delivery File 
Transmission*  Included Activity 
Hourly from 1 PM to 4 PM  4:00 PM • Unallocated positions resulting from all 
Reorganization events 
  
 
CAST Subscription 
MQ Delivery File 
Transmission* Included Activity 
12:00 PM  
1:30 PM  
4:00 PM  
4:30 PM  
8:00 PM 
12:00 PM  
1:30 PM  
4:00 PM  
4:30 PM  
8:00 PM 
• Instructions statements for all Reorganization 
instruction activity 
 
 
 
 

---

## Page 10

ISO 20022 Messaging Subscription Options 
Reorganization Events 10 
* Individual messages are accumulated and transmitted at the times specified 
** ”Real Time” is defined as messages that are immediately disseminated upon availability from [[DTC]] 
processing systems 
 

---

## Page 11

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 