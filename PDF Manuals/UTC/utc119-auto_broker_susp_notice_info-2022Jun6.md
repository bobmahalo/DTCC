---
title: "Universal Trade Capture (UTC) Automated Broker Suspension Notice Information"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc119-auto_broker_susp_notice_info-2022Jun6.pdf"
pages: 3
size: "232.7 KB"
category: "UTC"
ingested_on: "2026-06-05"
---

# Universal Trade Capture (UTC) Automated Broker Suspension Notice Information

**Original File:** [utc119-auto_broker_susp_notice_info-2022Jun6.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc119-auto_broker_susp_notice_info-2022Jun6.pdf)  
**Category:** UTC  
**Total Pages:** 3  
**File Size:** 232.7 KB  

---

## Page 1

Automated [[Broker]] Suspension Notice Information 
Universal Trade Capture (UTC) 1 
UNIVERSAL TRADE CAPTURE (UTC) 
AUTOMATED [[Broker]] SUSPENSION NOTICE INFORMATION 
JUNE 6, 2022 
N
SCC generates a notification message when an [[NSCC]] [[Broker]] is suspended from clearing ([[NSCC]] “ceases to 
act”). Messages are written in FIX format and sent through Message Queue (MQ) or FIX protocol. [[NSCC]] has 
made the messages available, on a subscription basis, to all exchanges, other submitting entities and 
Members. There are no additional charges to firms that subscribe to this message. 
Message Details 
In addition to standard header and footer fields, the [[Broker]] suspension message includes a line of text to 
indicate that “00000000 [[Broker]] has been suspended from clearance input at [[NSCC]]”. Use the message header 
Message Type (tag 35) of “B” to distinguish this message from other trade capture output. 
How to Subscribe 
To receive the automated [[Broker]] suspension notice message, contact [[NSCC]] Integration by email at 
NSCCIntegration@[[DTCC]].com. The subscription can be enabled as long as the current clearance output MQ or 
FIX connectivity exists. 
Testing 
[[DTCC]] has created a canned test message that can be transmitted to subscribing firms. This test message is a 
sample of the message that will be distributed. The test message is transmitted from the [[NSCC]] test [[participant]] 
Services Environment (PSE) environment. 


---

## Page 2

Automated [[Broker]] Suspension Notice Information 
Universal Trade Capture (UTC). 2 
Production Subscription 
After the canned test file has been received, entities may contact [[NSCC]] Integration to request receipt of future 
production [[Broker]] suspension messages. [[NSCC]] activates the production subscription for this message and 
begin distributing it from the [[NSCC]] production environment as [[Broker]] suspensions occur. 
Further Information 
If you have additional questions regarding this message, contact your [[DTCC]] Relationship Manager. For 
information about the [[Broker]] Cease to Act formats, see the UTC Technical Resources section of the [[DTCC]] 
Learning Center. 

---

## Page 3

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: June 6, 2022 
Publication Code: UTC119 
Service: Universal Trade Capture (UTC) 
Title: Automated [[Broker]] Suspension Notice Information 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 