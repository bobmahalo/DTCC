---
title: "Sample Carrier Day 1 Response Message for Broker Dealer of Record Change (Carrier Reject for Business Reason)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/irs104_20201021_bdr_carrier_day1_rej_sm.pdf"
pages: 3
size: "132.9 KB"
category: "Tax_Legal"
ingested_on: "2026-06-05"
---

# Sample Carrier Day 1 Response Message for Broker Dealer of Record Change (Carrier Reject for Business Reason)

**Original File:** [irs104_20201021_bdr_carrier_day1_rej_sm.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/irs104_20201021_bdr_carrier_day1_rej_sm.pdf)  
**Category:** Tax_Legal  
**Total Pages:** 3  
**File Size:** 132.9 KB  

---

## Page 1

 
 
XML SAMPLE 
[[DTCC]] Public (White) 
IFW [[Broker]] DEALER OF RECORD (BDR) CHANGE 
Sample Carrier Day 1 Response Message for [[Broker]] Dealer of Record Change (Carrier 
Reject for Business Reason) 
OCTOBER 21, 2020 
<?xml version="1.0" encoding="UTF-8"?> 
<PolicyAdministration_Msg xmlns="http://ACORD.org/Standards/Life/2"> 
  <TXLife> 
    <TXLifeResponse [[ID]]="ID_1"> 
      <TransRefGUID>z1a97582-da48-41de-9999-eaf669999999</TransRefGUID> 
      <TransType tc="1004900113">Policy Administration Transaction</TransType> 
      <TransSubType tc="11300">Policy Administration Transaction</TransSubType> 
      <TransExeDate>2020-09-15</TransExeDate> 
      <TransExeTime>14:13:48-04:00</TransExeTime> 
      <TransMode tc="2">Original request</TransMode> 
      <NoResponseOK tc="0">False</NoResponseOK> 
      <TestIndicator tc="0">False</TestIndicator> 
      <PrimaryObjectType tc="4">Holding</PrimaryObjectType> 
      <TransResult> 
        <ResultCode tc="5">Failure</ResultCode> 
        <ResultInfo> 
          <ResultInfoCode tc="3026">No or Unknown Policy Number</ResultInfoCode> 
        </ResultInfo> 
        <ResultInfo> 
          <ResultInfoCode tc="100">General Error</ResultInfoCode> 
          <ResultInfoDesc>For agent with partial tax [[ID]] of 7777, no active appointment or affiliation 
exists.</ResultInfoDesc> 
        </ResultInfo> 
      </TransResult> 

---

## Page 2

 
 
XML SAMPLE 
[[DTCC]] Public (White) 
    </TXLifeResponse> 
  </TXLife> 
</PolicyAdministration_Msg> 
 

---

## Page 3

 
 [[DTCC]] Public (White) 
© 2020 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: October 21, 2020  
Publication Code: IRS104 
Service: In-Force Web Services 
Title: Sample Carrier Day 1 Response Message for [[Broker]] Dealer of Record Change (Carrier Reject for Business Reason) 
  
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 