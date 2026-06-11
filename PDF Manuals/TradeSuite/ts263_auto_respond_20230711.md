---
title: "Agent and Institution Auto Responder Usage"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ts263_auto_respond_20230711.pdf"
pages: 5
size: "209.5 KB"
category: "TradeSuite"
ingested_on: "2026-06-05"
---

# Agent and Institution Auto Responder Usage

**Original File:** [ts263_auto_respond_20230711.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ts263_auto_respond_20230711.pdf)  
**Category:** TradeSuite  
**Total Pages:** 5  
**File Size:** 209.5 KB  

---

## Page 1

TradeSuiteID®
AGENTANDINSTITUTIONAUTORESPONDER
USAGE
VERSION8.1
OCTOBER19,2023

---

## Page 2

TABLEOFCONTENTS
Preface 3
Audience 3
ChangesinthisVersion 3
RelatedDocumentsandTraining 3
Questions? 3
1.IntroductiontoTradeSuiteAutoResponderUsage 4
AgentandInstitutionAutoResponderUsage
TableOfContents 2

---

## Page 3

PREFACE
ThisdocumentdescribestheusageforDTCCTradeSuiteIDAgentandInstitutionAutoResponder.
Audience
Thisdocumentisforagents,[[Institutions]],andotherswhousetheTradeSuiteIDautoresponderprocess.
ChangesinthisVersion
ThisdocumenthasbeencreatedtodescribetheDTCCTradeSuiteIDagentandinstitutionautoresponder
usage.
RelatedDocumentsandTraining
Forrelateddocumentsandtraining,seeTradeSuiteID®ontheDTCCLearningCenter.
Questions?
TheClientCenterprovidesgeneralassistanceandtechnicalhelp.Visitto:
l Enteraservicerequestorcheckthestatusofanexistingservicerequest.
l Searchtheknowledgebase.
l Obtaincontactinformation.
AgentandInstitutionAutoResponderUsage
Preface 3

---

## Page 4

1.INTRODUCTIONTOTRADESUITEAUTO
RESPONDERUSAGE
TheDTCCTradeSuiteIDagentandinstitutionautoresponderusageisdescribedinTable1.1.
[[ID]] Description Prerequisiteforuse
Agent
50721 1. BrokersubmitsTradeSuite
confirmtoAgentID50721.
2. TradeSuiteAutoResponder
willaffirmtheconfirmasthe
Agent.
3. TheconfirmwillsettlePDQ.
IfthebrokerconfirmsetstheAgentas50721andInstitutionas
64093orPrimeBrokeras94761thentheTradeSuiteAuto
ResponderwillaffirmastheInstitution.
Institution
64093 1. BrokersubmitsTradeSuite
confirmtoInstitutionID
64093.
2. TradeSuiteAutoResponder
willaffirmtheconfirmasthe
Institution.
3. TheconfirmwillsettlePDQ.
Prime
[[Broker]]
94761
1. BrokersubmitsTradeSuite
confirmtoInstitution&
AgentID94761.
2. TradeSuiteAutoResponder
willaffirmtheconfirmasthe
InstitutionPrimeBrokerID.
3. TheconfirmwillsettleCNSif
eligibleotherwisesettle
PDQ.
ForTestingCNSSettlement:
1. [[Broker]]&ClearingBrokermustbeeligibleforCNSin
Test/U-Region
2. SecurityCUSIPmustbeeligibleforCNSinTest/U-Region
AgentID94761usesClearingAgent00123whichissetupfor
CNSsettlement
Table1.1DTCCTradeSuiteAgentandInstitutionAutoResponderUsage
AgentandInstitutionAutoResponderUsage
1.IntroductionToTradeSuiteAutoResponderUsage 4

---

## Page 5

©2023DTCC.Allrightsreserved.DTCCandDTCC(Stylized)areregisteredandunregisteredtrademarksofThe
DepositoryTrust&ClearingCorporation.Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandname
bycertainaffiliatesofTheDepositoryTrust&ClearingCorporation(“[[DTCC]]”).DTCCitselfdoesnotprovidesuch
services.Eachoftheseaffiliatesisaseparatelegalentity,subjecttothelawsandregulationsoftheparticularcountry
orcountriesinwhichsuchentityoperates.Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,itsaffiliatesand
theservicestheyoffer.
DocDate:October19,2023
PublicationCode:TS263
Service:TradeSuiteID
Title:AgentandInstitutionAutoResponderUsage
ForMoreInformation
EmailDTCCLearningat:
DTCCLearning@[[DTCC]].com
orvisitusonthewebat:
www.dtcclearning.com