---
title: "DTCC Structured Finance Kinetics User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat184_struc_finance_kinetics_fs_20230120.pdf"
pages: 4
size: "1110.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# DTCC Structured Finance Kinetics User Guide

**Original File:** [dat184_struc_finance_kinetics_fs_20230120.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dat184_struc_finance_kinetics_fs_20230120.pdf)  
**Category:** Other  
**Total Pages:** 4  
**File Size:** 1110.7 KB  

---

## Page 1

STRUCTUREDFINANCEKINETICS
ADTCCDATASERVICESOFFERING
TRANSACTIONREPORTFILEUSERGUIDE
JANUARY20,2023


---

## Page 2

©2023DTCC.Allrightsreserved.[[DTCC]],[[DTCC]](Stylized),ADVANCINGFINANCIALMARKETS.
TOGETHER,andtheInterlockergraphicareregisteredandunregisteredtrademarksofTheDepository
Trust&ClearingCorporation.
Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandnamebycertainaffiliatesofThe
DepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitselfdoesnotprovidesuchservices.Eachof
theseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsoftheparticularcountryor
countriesinwhichsuchentityoperates.Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,its
affiliatesandtheservicestheyoffer.
DocInfo:January20,2023
PublicationCode:DAT184
Service:StructuredFinanceKinetics
Title:TransactionReportFileUserGuide

---

## Page 3

TransactionReportFileSpecification 3
TRANSACTIONREPORTFILESPECIFICATION
[[DTCC]]'sStructuredFinanceKineticsServiceprovidesasingle,streamlinedfeedofanonymizedstructured-finance
transactionsdatatoenhanceuseranalysisofthiscomplexmarket.
Thedatafilecontainingalltransactionsforthedayisdeliveredendofdayeachtradingday,atapproximately
12:00AMET.
FieldName Type Width Description
DeliveryDate Int 10 TheDeliveryDateisdefinedas:
1. Thedateofthelasttradestatusupdate(MADE,DROPPED,
CANCELLED,OR REJECTED).
2. TheCurrentDatefortradeswithastatusof
UNPROCESSED,EXEMPTED,orAUTHORIZEDwithaSet-
tlementDatethatisequaltoorlessthantheCurrentDate.
Original
[[settlement]]
Date
int 7 TheTrade'sOriginalIntendedSettlementDate,expressedasaJulian
dateYYYYNNN,where:
l YYYY: Year
l NNN: SequentialCalendarDate
[[CUSIP]] alpha 9 9-digitU.S-issuedsecurityidentifier,consistingof:
l [[issuer]](6digits)
l Issue(2digits)
l CUSIPCheckDigit(1digit)
ShareQuantity dec 15 Theparquantityofthetransaction.
Amountofthe
Transaction
dec 18 Thevalueamountofthetransaction.
TradeDate alpha 8 ThedateofTradeExecution.
TradeType alpha 4 CASHorREPO.
DTCCStructuedFinanceKineticsUserGuide

---

## Page 4

FORMOREINFORMATION
EmailDTCCLearningat:
datalearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com