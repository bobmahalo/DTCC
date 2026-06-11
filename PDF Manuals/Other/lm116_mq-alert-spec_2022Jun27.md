---
title: "DTCC Limit Monitoring Message Queue (MQ) Messages"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/lm116_mq-alert-spec_2022Jun27.pdf"
pages: 5
size: "253.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# DTCC Limit Monitoring Message Queue (MQ) Messages

**Original File:** [lm116_mq-alert-spec_2022Jun27.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/lm116_mq-alert-spec_2022Jun27.pdf)  
**Category:** Other  
**Total Pages:** 5  
**File Size:** 253.8 KB  

---

## Page 1

 
 
[[DTCC]] LIMIT MONITORING 
MESSAGE QUEUE (MQ) MESSAGES 
MARCH 11, 2015 
 
 
 


---

## Page 2

Message Queue (MQ) Messages 
MESSAGE QUEUE (mq) Alert AND Alert Resolution Message 2 
MESSAGE QUEUE (MQ) ALERT AND ALERT 
RESOLUTION MESSAGE 
A clearing firm receives a message when an alert is generated and resolved. Not all alerts are resolved; 
therefore, not all alert messages result in an alert resolution message. The following table provides the field 
details: 
Field Name Type Length Comments 
Destination Alpha Numeric 8 Clearing [[Member]] [[ID]] 
Message Type Alpha Numeric 2 
AL = Alert Message 
RE = Resolution Message 
Risk Entity [[ID]] Numeric 9 [[ID]] of the risk entity. 
Limit [[ID]] Alpha Numeric 2 
Identifies the limit for which the alert is 
generated: 
NN = Net Notional 
Alert Level Alpha Numeric 1 
1 = Level 1 
2 = Level 2 
3 = Level 3 
4 = Level 4 
 
Not populated on resolution messages 
Alert Time at Creation Alpha Numeric 6 Not populated on resolution messages 
Alert Value at Creation Numeric 17 Not populated on resolution messages 
Alert Limit at Creation Numeric 15 Not populated on resolution messages 
Alert Time at Resolution Alpha Numeric 6  
Alert Value at Resolution Numeric 17 
Format = 99999999999999999 with an 
assumed decimal point before the last two 
numbers. 
Alert Limit at Resolution Numeric 15  

---

## Page 3

Message Queue (MQ) Messages 
MQ Message of Risk Entity Changes 3 
MQ MESSAGE OF RISK ENTITY CHANGES 
A clearing firm receives a message through the Common Data Transfer System (CDTS) when any of the 
following changes are made to a risk entity: 
• Adding a risk entity. 
• Modifying a risk entity definition, limit, or trade array. 
• Deleting a risk entity. 
The following table provides the field details: 
Field Name Type Length Comments 
Destination Alpha Numeric 8 Clearing [[Member]] [[ID]] 
Message Type Alpha Numeric 2 
RA – Risk Entity Added 
RM – Risk Entity Modified 
RD – Risk Entity Deleted 
Risk Entity [[ID]] Numeric 9 [[ID]] of the risk entity. 
Risk Entity Name Alpha-Numeric 50 Name assigned to the risk entity. 
Modification Effective Date Date 8 Format: DDMMCCYY 
Modified By Alpha-Numeric 50 User [[ID]] of the user who made the update. 
Modification Date Date/Time 14 Format:  DDMMCCYYHHMMSS 

---

## Page 4

Message Queue (MQ) Messages 
MQ Message for an Unassigned Trade Flow 4 
MQ MESSAGE FOR AN UNASSIGNED TRADE FLOW 
The unassigned trade flow message is distributed to members when a trade side is applied by PTM to the 
unassigned risk entity.  
• Only one message per executing [[Broker]], on the first occurrence of a new executing [[Broker]]. 
• The message is distributed in near real time after the trade side is received. 
The following table provides the field details: 
Field Name Type Length Comments 
Destination Alpha Numeric 8 Clearing [[Member]] [[ID]] 
Message Type Alpha Numeric 2 UT – Unassigned Trade 
Executing [[Broker]] Alpha Numeric 8 [[ID]] of [[Broker]] who executed the trade. 
 
 

---

## Page 5

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: June 27, 2022 
Publication Code: LM116 
Service: [[DTCC]] Limit Monitoring 
Title:  Queue (MQ) Messages 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
