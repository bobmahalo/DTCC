---
title: "DTCC CA Transformation Industry Call - March 2022 Presentation"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ca233_dtcc_ca_mic_presentation_20220302.pdf"
pages: 11
size: "1910.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# DTCC CA Transformation Industry Call - March 2022 Presentation

**Original File:** [ca233_dtcc_ca_mic_presentation_20220302.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ca233_dtcc_ca_mic_presentation_20220302.pdf)  
**Category:** Other  
**Total Pages:** 11  
**File Size:** 1910.8 KB  

---

## Page 1

CORPORATE ACTIONS 
March 2022
Monthly Industry Call
[[Asset]] Services

---

## Page 2

Voluntary Reorg Instructions Automation –ISO 20022 & API 
Project Goals
2
Project seeks to 
solve a client-
facing / industry 
issue to provide 
automation for a 
fully manual 
process 
Project is a 
modernization 
effort which will 
ultimately 
eliminate [[DTC]]’s 
mainframe 
footprint for 
voluntary reorg 
instructions 
processing

---

## Page 3

“Bridge” Between Legacy Processors and New Interfaces
3
[[PTS]] / [[PBS]] ISO 20022 
Messaging
API’s Legacy 
Processors
NEW 
Modernized 
Processor

---

## Page 4

2018 - 2019 - Client Outreach & Requirements Gathering
o 22 one-on-one client meetings
o 51 clients expressed interest in [[DTC]] automating the Voluntary Reorganization 
instruction process
o Significant requirement gathering based on client feedback
o October 2, 2018 Client Day @ [[DTCC]]
2019 – 2020 – Industry Engagement & Internal Engagement
o Development begins August 2019
o Clients begin requirements gathering with [[DTCC]], analysis and mapping
o [[DTCC]] convenes working group
Background – Client Engagement
4

---

## Page 5

Scope
Events In Scope
• Tenders / Exchanges (AC 52) – including with 
Consents, Dutch Auctions
• Mergers with Elections (AC 52M)
• Optional Repayments – Puts (AC 58/B)
• Rights Subscription (AC 59)
• Mandatory Tender with the Right to Retain (AC 
65B/R)
5
ISO 20022 Messages In Scope
• CAIN - Corporate Action Instruction Message 
(Inbound) 
• CAIS - Corporate Action Instruction Status 
Message (Outbound)
• CAIC - Corporate Action Instruction Cancellation -
Withdrawal (Inbound)
• CACS - Corporate Action Instruction Cancellation -
Withdrawal (Outbound) 
• CAST - Corporate Action Instruction Statement 
Report (Outbound) 

---

## Page 6

Current State – Client Testing  ([[DTC]] PSE Environment)
2022 PSE Testing –
Currently Available
PTOP (Tenders etc.) and PUTS Event Types- ISO 20022 
CAIN instruction and CAIS response confirmation
CAIN pending instructions (recycles)
CAIN end-to-end with position check
Includes Cover Protect functionality 
Does not include automated withdrawals (CACS / CAIC 
messages) Cover on Behalf of Another functionality, 
APIs or PSOP events
6

---

## Page 7

Future State - 2022 Development and Client Testing Timeline  
([[DTC]] PSE Environment)
2022 - PSE Testing
 ISO 20022 -- PSOP event types available (March / April)
API testing for PTOP, PUTS, PSOP event types (Begin 
April for PTOP / PUTS)
Automated withdrawal functionality available -- CAIC and 
CACS message types (Q3)
Cover on Behalf of Another functionality available for 
testing (Q4)
7

---

## Page 8

• Instructions are predicated upon various information found in the ISO 20022 CANO Announcement 
message
o Instructions require certain data elements such as CA [[ID]] (COAF) and [[Option]] Number, among others, 
found in the CANO.  These elements are critical in order to have your instruction accepted and 
processed by [[DTC]]
o It is highly recommended that Participants receive this Announcement information in real-time (MQ 
connection)
• Participants are required to test annually (Sept/Oct) ISO 20022 Messaging and API ahead of the SWIFT 
Standards Release in November
• It is important that firms utilizing this new process take into account the usage of the Supplementary Data 
or Extension to ensure full event instruction coverage
o Supplementary Data is not available in the 15022 MT 565 or 567 messages
• Go-live is based on client readiness
o Clients must complete a minimum number of test cases and scripts provided by [[DTC]]
Important Client Considerations
8

---

## Page 9

Middleware / Network Infrastructure
• SMART MQ is the only network supported
o No File protocols (FTP / NDM) will be supported 
• System Availability / Response Times (see User Guide)
• ACK/NAK process for SMART (see User Guide)
Network Considerations 
9

---

## Page 10

• SWIFT MyStandards Readiness Portal allows client to test the CAIN (well formed structure based on specs) 
prior to business / message flow testing with [[DTC]] 
o [[Entitlement]] based upon request
• API Marketplace for API specs 
o [[Entitlement]] based upon request
• ISO 20022 messaging specs can be found at www.[[DTCC]].com/camodernization and SWIFT MyStandards
o [[Entitlement]] based upon request
• All testing will be handled by the [[DTC]] team
o Development and testing timeline is 3 – 9 months depending on level of client engagement / priority
o Velocity of testing will depend on client readiness / development etc.
• Clients can get started by engaging with the [[DTC]] Corporate Actions team – camodernization@[[DTCC]].com
o A meeting cadence will be established, usually weekly
o Mapping, development and test support will be available
Resources for Getting Started
10

---

## Page 11

Please e-mail camodernization@[[DTCC]].com for questions and support
Questions & Support
11