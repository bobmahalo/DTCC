---
title: "Custodial to Non-Custodial - Sample Message (with Sept 2000 requirement)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/irs105_20201021_bdr_cus2noncus_2020req_sm.pdf"
pages: 8
size: "140.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Custodial to Non-Custodial - Sample Message (with Sept 2000 requirement)

**Original File:** [irs105_20201021_bdr_cus2noncus_2020req_sm.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/irs105_20201021_bdr_cus2noncus_2020req_sm.pdf)  
**Category:** Other  
**Total Pages:** 8  
**File Size:** 140.8 KB  

---

## Page 1

 
 
XML SAMPLE 
[[DTCC]] Public (White) 
IFW [[Broker]] DEALER OF RECORD (BDR) CHANGE 
Custodial to Non-Custodial - Sample Message (with Sept 2020 requirement) 
OCTOBER 21, 2020 
<?xml version="1.0" encoding="UTF-8"?> 
<ns3:PolicyAdministration_Msg xmlns:ns3="http://ACORD.org/Standards/Life/2" 
xmlns:ns2="http://service.iwa.[[DTCC]].com/"> 
  <ns3:TXLife> 
    <ns3:TXLifeRequest [[ID]]="ID_1" PrimaryObjectID="ID_HOLDING_2"> 
      <ns3:TransRefGUID>0694c097-481d-4509-bc57-1b3b65378655-[[DTCC]]</ns3:TransRefGUID> 
      <ns3:TransType tc="1004900113">Policy Administration Transaction</ns3:TransType> 
      <ns3:TransSubType tc="11300">Policy Administration Transaction</ns3:TransSubType> 
      <ns3:TransExeDate>2020-09-04</ns3:TransExeDate> 
      <ns3:TransExeTime>13:06:19-04:00</ns3:TransExeTime> 
      <ns3:TransMode tc="2">Original request</ns3:TransMode> 
      <ns3:NoResponseOK tc="0">False</ns3:NoResponseOK> 
      <ns3:TestIndicator tc="0">False</ns3:TestIndicator> 
      <ns3:PrimaryObjectType tc="4">Holding</ns3:PrimaryObjectType> 
      <ns3:ChangeSubType [[ID]]="ID_25" ChangeID="ID_ADDRESS_5"> 
        <ns3:ChangeTC tc="30">Change Address</ns3:ChangeTC> 
        <ns3:TranContentCode tc="1">Insert</ns3:TranContentCode> 
      </ns3:ChangeSubType> 
      <ns3:ChangeSubType [[ID]]="ID_26" ChangeID="ID_OWNER_6"> 
        <ns3:ChangeTC tc="67">Owner Change</ns3:ChangeTC> 
        <ns3:TranContentCode tc="1">Insert</ns3:TranContentCode> 
      </ns3:ChangeSubType> 
      <ns3:ChangeSubType [[ID]]="ID_27" ChangeID="ID_BENE_12"> 
        <ns3:ChangeTC tc="74">Change Policy Beneficiary Percentage</ns3:ChangeTC> 

---

## Page 2

 
 
XML SAMPLE 
[[DTCC]] Public (White) 
        <ns3:TranContentCode tc="1">Insert</ns3:TranContentCode> 
      </ns3:ChangeSubType> 
      <ns3:ChangeSubType [[ID]]="ID_28" ChangeID="ID_BENE_12"> 
        <ns3:ChangeTC tc="66">Change Policy Beneficiary</ns3:ChangeTC> 
        <ns3:TranContentCode tc="1">Insert</ns3:TranContentCode> 
      </ns3:ChangeSubType> 
      <ns3:ChangeSubType [[ID]]="ID_29" ChangeID="ID_AGENT_15"> 
        <ns3:ChangeTC tc="27">Change Producer Information</ns3:ChangeTC> 
        <ns3:TranContentCode tc="1">Insert</ns3:TranContentCode> 
      </ns3:ChangeSubType> 
      <ns3:ChangeSubType [[ID]]="ID_30" ChangeID="ID_AGENT_17"> 
        <ns3:ChangeTC tc="27">Change Producer Information</ns3:ChangeTC> 
        <ns3:TranContentCode tc="1">Insert</ns3:TranContentCode> 
      </ns3:ChangeSubType> 
      <ns3:ChangeSubType [[ID]]="ID_31" ChangeID="ID_19"> 
        <ns3:ChangeTC tc="1004900077">Change of Financial Institution (BDofRC)</ns3:ChangeTC> 
        <ns3:TranContentCode tc="1">Insert</ns3:TranContentCode> 
      </ns3:ChangeSubType> 
      <ns3:OLifE> 
        <ns3:Holding [[ID]]="ID_HOLDING_2"> 
          <ns3:HoldingTypeCode tc="2">Policy</ns3:HoldingTypeCode> 
          <ns3:DistributorClientAcctNum>BIN1</ns3:DistributorClientAcctNum> 
          <ns3:Policy CarrierPartyID="ID_22"> 
            <ns3:PolNumber>Contact1</ns3:PolNumber> 
          </ns3:Policy> 
          <ns3:Arrangement [[ID]]="ID_POLICY_4"> 
            <ns3:ReferenceNo>3</ns3:ReferenceNo> 

---

## Page 3

 
 
XML SAMPLE 
[[DTCC]] Public (White) 
            <ns3:ArrType tc="38">Systematic Withdrawal</ns3:ArrType> 
            <ns3:OLifEExtension> 
              <ns3:ContinueArrangementInd tc="0">False</ns3:ContinueArrangementInd> 
            </ns3:OLifEExtension> 
          </ns3:Arrangement> 
        </ns3:Holding> 
        <ns3:Party [[ID]]="ID_OWNER_6"> 
          <ns3:PartyTypeCode tc="1">Person</ns3:PartyTypeCode> 
          <ns3:Person> 
            <ns3:FirstName>Robert</ns3:FirstName> 
            <ns3:LastName>****</ns3:LastName> 
          </ns3:Person> 
          <ns3:Address [[ID]]="ID_ADDRESS_5"> 
            <ns3:AddressTypeCode tc="1">Residence</ns3:AddressTypeCode> 
            <ns3:Line1>****</ns3:Line1> 
            <ns3:City>****</ns3:City> 
            <ns3:AddressStateTC tc="6">California</ns3:AddressStateTC> 
            <ns3:Zip>****</ns3:Zip> 
            <ns3:AddressCountryTC tc="1">USA</ns3:AddressCountryTC> 
          </ns3:Address> 
          <ns3:GovtIDInfo> 
            <ns3:GovtID>*****1111</ns3:GovtID> 
            <ns3:GovtIDTC tc="1">Social Security Number</ns3:GovtIDTC> 
          </ns3:GovtIDInfo> 
        </ns3:Party> 
        <ns3:Party [[ID]]="ID_ANNUITANT_7"> 
          <ns3:PartyTypeCode tc="1">Person</ns3:PartyTypeCode> 

---

## Page 4

 
 
XML SAMPLE 
[[DTCC]] Public (White) 
          <ns3:Person> 
            <ns3:FirstName>Robert</ns3:FirstName> 
            <ns3:LastName>****</ns3:LastName> 
          </ns3:Person> 
          <ns3:GovtIDInfo> 
            <ns3:GovtID>*****1111</ns3:GovtID> 
            <ns3:GovtIDTC tc="1">Social Security Number</ns3:GovtIDTC> 
          </ns3:GovtIDInfo> 
        </ns3:Party> 
        <ns3:Party [[ID]]="ID_BENE_12"> 
          <ns3:PartyTypeCode tc="1">Person</ns3:PartyTypeCode> 
          <ns3:Person> 
            <ns3:FirstName>Steve</ns3:FirstName> 
            <ns3:LastName>****</ns3:LastName> 
          </ns3:Person> 
          <ns3:GovtIDInfo> 
            <ns3:GovtID>*****2222</ns3:GovtID> 
            <ns3:GovtIDTC tc="1">Social Security Number</ns3:GovtIDTC> 
          </ns3:GovtIDInfo> 
        </ns3:Party> 
        <ns3:Party [[ID]]="ID_AGENT_15"> 
          <ns3:PartyTypeCode tc="1">Person</ns3:PartyTypeCode> 
          <ns3:Person> 
            <ns3:FirstName>Greg</ns3:FirstName> 
            <ns3:LastName>****</ns3:LastName> 
          </ns3:Person> 
          <ns3:Producer> 

---

## Page 5

 
 
XML SAMPLE 
[[DTCC]] Public (White) 
            <ns3:CRDNumber>CRD1</ns3:CRDNumber> 
          </ns3:Producer> 
          <ns3:GovtIDInfo> 
            <ns3:GovtID>*****3333</ns3:GovtID> 
            <ns3:GovtIDTC tc="1">Social Security Number</ns3:GovtIDTC> 
          </ns3:GovtIDInfo> 
        </ns3:Party> 
        <ns3:Party [[ID]]="ID_AGENT_17"> 
          <ns3:PartyTypeCode tc="1">Person</ns3:PartyTypeCode> 
          <ns3:Person> 
            <ns3:FirstName>Phillip</ns3:FirstName> 
            <ns3:LastName>****</ns3:LastName> 
          </ns3:Person> 
          <ns3:Producer> 
            <ns3:CRDNumber>CRD2</ns3:CRDNumber> 
          </ns3:Producer> 
          <ns3:GovtIDInfo> 
            <ns3:GovtID>*****4444</ns3:GovtID> 
            <ns3:GovtIDTC tc="1">Social Security Number</ns3:GovtIDTC> 
          </ns3:GovtIDInfo> 
        </ns3:Party> 
        <ns3:Party [[ID]]="ID_19"> 
          <ns3:PartyTypeCode tc="2">Organization</ns3:PartyTypeCode> 
          <ns3:FullName>Distributor</ns3:FullName> 
          <ns3:Organization> 
            <ns3:OrgForm tc="23">Corporation</ns3:OrgForm> 
            <ns3:DTCCMemberCode>0122</ns3:DTCCMemberCode> 

---

## Page 6

 
 
XML SAMPLE 
[[DTCC]] Public (White) 
          </ns3:Organization> 
        </ns3:Party> 
        <ns3:Party [[ID]]="ID_22"> 
          <ns3:PartyTypeCode tc="2">Organization</ns3:PartyTypeCode> 
          <ns3:FullName>Carrier</ns3:FullName> 
          <ns3:Organization> 
            <ns3:OrgForm tc="23">Corporation</ns3:OrgForm> 
            <ns3:DTCCMemberCode>5119</ns3:DTCCMemberCode> 
          </ns3:Organization> 
        </ns3:Party> 
        <ns3:Relation [[ID]]="ID_9" OriginatingObjectID="ID_HOLDING_2" RelatedObjectID="ID_ANNUITANT_7"> 
          <ns3:OriginatingObjectType tc="4">Holding</ns3:OriginatingObjectType> 
          <ns3:RelatedObjectType tc="6">Party</ns3:RelatedObjectType> 
          <ns3:RelationRoleCode tc="35">Annuitant</ns3:RelationRoleCode> 
        </ns3:Relation> 
        <ns3:Relation [[ID]]="ID_11" OriginatingObjectID="ID_HOLDING_2" RelatedObjectID="ID_OWNER_6"> 
          <ns3:OriginatingObjectType tc="4">Holding</ns3:OriginatingObjectType> 
          <ns3:RelatedObjectType tc="6">Party</ns3:RelatedObjectType> 
          <ns3:RelationRoleCode tc="8">Owner</ns3:RelationRoleCode> 
        </ns3:Relation> 
        <ns3:Relation [[ID]]="ID_14" OriginatingObjectID="ID_HOLDING_2" RelatedObjectID="ID_BENE_12"> 
          <ns3:OriginatingObjectType tc="4">Holding</ns3:OriginatingObjectType> 
          <ns3:RelatedObjectType tc="6">Party</ns3:RelatedObjectType> 
          <ns3:RelationRoleCode tc="34">Primary Beneficiary</ns3:RelationRoleCode> 
          <ns3:InterestPercent>100</ns3:InterestPercent> 
          <ns3:IrrevokableInd tc="0">False</ns3:IrrevokableInd> 
        </ns3:Relation> 

---

## Page 7

 
 
XML SAMPLE 
[[DTCC]] Public (White) 
        <ns3:Relation [[ID]]="ID_16" OriginatingObjectID="ID_HOLDING_2" RelatedObjectID="ID_AGENT_15"> 
          <ns3:OriginatingObjectType tc="4">Holding</ns3:OriginatingObjectType> 
          <ns3:RelatedObjectType tc="6">Party</ns3:RelatedObjectType> 
          <ns3:RelationRoleCode tc="37">Primary Agent</ns3:RelationRoleCode> 
          <ns3:InterestPercent>50</ns3:InterestPercent> 
        </ns3:Relation> 
        <ns3:Relation [[ID]]="ID_18" OriginatingObjectID="ID_HOLDING_2" RelatedObjectID="ID_AGENT_17"> 
          <ns3:OriginatingObjectType tc="4">Holding</ns3:OriginatingObjectType> 
          <ns3:RelatedObjectType tc="6">Party</ns3:RelatedObjectType> 
          <ns3:RelationRoleCode tc="11">Agent</ns3:RelationRoleCode> 
          <ns3:InterestPercent>50</ns3:InterestPercent> 
        </ns3:Relation> 
        <ns3:Relation [[ID]]="ID_21" OriginatingObjectID="ID_HOLDING_2" RelatedObjectID="ID_19"> 
          <ns3:OriginatingObjectType tc="4">Holding</ns3:OriginatingObjectType> 
          <ns3:RelatedObjectType tc="6">Party</ns3:RelatedObjectType> 
          <ns3:RelationRoleCode tc="83">[[Broker]]-Dealer</ns3:RelationRoleCode> 
        </ns3:Relation> 
        <ns3:Relation [[ID]]="ID_24" OriginatingObjectID="ID_HOLDING_2" RelatedObjectID="ID_22"> 
          <ns3:OriginatingObjectType tc="4">Holding</ns3:OriginatingObjectType> 
          <ns3:RelatedObjectType tc="6">Party</ns3:RelatedObjectType> 
          <ns3:RelationRoleCode tc="87">Carrier</ns3:RelationRoleCode> 
        </ns3:Relation> 
      </ns3:OLifE> 
    </ns3:TXLifeRequest> 
  </ns3:TXLife> 
</ns3:PolicyAdministration_Msg> 
 

---

## Page 8

 
 [[DTCC]] Public (White) 
© 2020 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: October 21, 2020  
Publication Code: IRS105 
Service: In-Force Web Services 
Title: Custodial to Non-Custodial - Sample Message (with Sept 2000 requirement) 
  
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 