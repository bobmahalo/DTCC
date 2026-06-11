---
title: "Test Plan Certification for UTC Input"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc108_mq_fix_test_plan_2020Apr13.pdf"
pages: 5
size: "270.1 KB"
category: "UTC"
ingested_on: "2026-06-05"
---

# Test Plan Certification for UTC Input

**Original File:** [utc108_mq_fix_test_plan_2020Apr13.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc108_mq_fix_test_plan_2020Apr13.pdf)  
**Category:** UTC  
**Total Pages:** 5  
**File Size:** 270.1 KB  

---

## Page 1

Test Plan Certification for UTC Input 
UTC Test Plan  1 
 
 
 
 
 
UNIVERSAL TRADE CAPTURE (UTC) 
TEST PLAN CERTIFICATION FOR UTC INPUT 
APRIL 13, 2020 
 
 
 
 


---

## Page 2

Test Plan Certification for UTC Input 
UTC Test Plan  2 
UTC TEST PLAN 
Test Cycle # Test Cycle 
Name 
Business Description Test Case Description Date Tested [[DTCC]] 
Confirmation  
Comments/Results 
Test Cycle #1 Connectivity Test Exchange/QSR/Correspondent 
Clearing submits input through 
the FIX Engine or FIX over MQ  
Test normal connectivity 
Exchange/QSR/Correspondent 
Clearing submit valid messages 
to UTC and receive either Fix or 
MRO file output. 
Confirms connectivity, CDTS 
subscriptions output is 
generated. 
   
Test Cycle #2 Scenario Tests/ 
Admin Messages 
Scenario trades submitted to 
[[DTCC]] by Exchanges/QSR/ 
Correspondent Clearing  
Firms submit trades messages 
with commonly used tags using 
the Input test script as a guide. 
An exchange submits trades 
containing not-commonly found 
tags. 
   
“ MQ/ FIX 
exception 
processing 
[[DTCC]] handles a Reversal and 
Replacement 
Exchanges or Firms submit an 
original trade and a reversal. 
[[NSCC]] confirms reversal of buy 
and sell side. 
   
“ Invalid/Reject 
Messages 
Scenario trades submitted not 
to be accepted by [[DTCC]] 
Sending Entities submit trades 
with common tags populated 
incorrectly (ex. Bad [[CUSIP]], bad 
[[participant]]) to generate UTC 
rejects. 
 
 
 
 
   

---

## Page 3

Test Plan Certification for UTC Input 
UTC Test Plan  3 
Test Cycle # Test Cycle 
Name 
Business Description Test Case Description Date Tested [[DTCC]] 
Confirmation  
Comments/Results 
“ End of Day 
Processing 
[[EOD]] message is submitted Sending Entities submit Good 
Night indicating trade input is 
finished for the day, accounting 
for a valid count of sequence 
numbers. 
   
“ [[DTCC]] returns the [[EOD]] 
message 
[[DTCC]] returns a Good Night 
message confirmation to 
Exchange. 
   
“ Goodnight Out of Balance Sending Entity submits 
Goodnight with out of balance 
trade count. 
   
“ MQ/ FIX 
Exception 
Processing 
Data with a gap is submitted Sending Entity submits trades 
through MQ/FIX, with a gap in 
the sequence numbers.  
   
“ [[DTCC]] responds to a gap [[DTCC]] detects the gap and 
sends a gap fill request.  
   
“ Exchange/QSR responds to a 
gap fill request 
Gap fill request is received and 
processed.  
   
Test Cycle #3 Volume Test Exchange/QSR/Correspondent 
Clearing  
Transmits three times daily 
Production volume 
Submit three times the volume 
through MQ/FIX in PSE. 
 
 
 
 
 
 
 
 
   

---

## Page 4

Test Plan Certification for UTC Input 
UTC Test Plan  4 
Test Cycle # Test Cycle 
Name 
Business Description Test Case Description Date Tested [[DTCC]] 
Confirmation  
Comments/Results 
Test Cycle #4 Failover Test Prod/PSE Failover 
 
Optional testing of primary and 
failover connections for 
heartbeat or telnet only.  
Conversations regarding 
failover to ensure Clearing 
Firms have proper BCP in 
place. 
When firms begin connectivity 
through FIX or MQ they are 
required to set up their back up 
failover connections. 
 
Optional Saturday Testing 
Exchange/QSR/Correspondent 
Clearing firms send trades from 
their production environment to 
[[DTCC]] production FIX engine, 
(heartbeat only), then fails over 
to their secondary site. [[DTCC]] 
fails over from the primary FIX 
engine to the secondary for this 
client. 
   
Test Cycle #5 Cease-to-Act Optional message for 
informational purposes 
notifying Clearing members 
that [[NSCC]] has Ceased to Act 
on behalf of a Clearing firm 
who has been removed from 
our [[participant]] Master tables. 
[[DTCC]] notifies markets that it 
ceases to act on behalf of a 
[[Broker]]. Information message. 
 
Optional for Clearing Firms 
   
Test Cycle #6 Production 
Connectivity and 
Pre-production 
Test 
Implementation 
[[NSCC]] and Sending Entity to 
confirm all Production 
Connections, CDTS 
subscriptions and complete a 
pre-production test trade. 
    
 

---

## Page 5

 
UTC Test Plan  5 
© 2020 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and unregistered 
trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not 
provide such services.  Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which such entity operates. 
Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: April 13, 2020 
Publication Code: UTC108 
Service: Universal Trade Capture (UTC) 
Title: Test Plan Certification for UTC Input 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 