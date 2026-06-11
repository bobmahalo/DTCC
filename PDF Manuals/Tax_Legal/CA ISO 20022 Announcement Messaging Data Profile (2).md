---
title: "CA ISO 20022 Announcement Messaging Data Profile (2).pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/CA%20ISO%2020022%20Announcement%20Messaging%20Data%20Profile%20%282%29.pdf"
pages: 7
size: "129.0 KB"
category: "Tax_Legal"
ingested_on: "2026-06-05"
---

# CA ISO 20022 Announcement Messaging Data Profile (2).pdf

**Original File:** [CA ISO 20022 Announcement Messaging Data Profile (2).pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/CA%20ISO%2020022%20Announcement%20Messaging%20Data%20Profile%20%282%29.pdf)  
**Category:** Tax_Legal  
**Total Pages:** 7  
**File Size:** 129.0 KB  

---

## Page 1

 
1 | Page  
[[DTCC]] Non-Confidential 
Corporate Actions ISO 20022 Announcement Messaging Service Data Profile 
What – ISO 20022 is the most current global standardized messaging platform set forth by ISO Technical 
Committee TC68 Financial Services.   The new ISO 20022 message format allows far greater flexibility and 
expandability through the use of standardized XML schemas.  The new ISO 20022 message format allows the use 
of extensions to include additional information to the core ISO 20022 message.  [[DTCC]] takes advantage of message 
extensions to provide far greater information than previous ISO standards allowed, making the ISO 20022 format 
the perfect conduit for Corporate Actions Announcement messaging.  [[DTCC]]’s Corporate Actions messaging service 
provides announcement information that is inclusive of 3 main types of Corporate Actions including: 
• Distributions 
• Redemptions 
• Reorganizations 
• Meetings 
• Factors 
• Maturity Cash 
[[DTCC]] is the first financial institution in the world to use the ISO 20022 message type for Corporate Actions 
Announcement dissemination.   
Source – [[DTCC]]’s [[Asset]] servicing process of Corporate Actions covers over 3.5 million [[DTCC]] eligible [[securities]].  
[[DTCC]] relies on 3 major contributors for its Corporate Action processing and announcement services.  The 3 major 
sources include: 
• [[securities]] Issuers 
• [[securities]] Service Agents 
• Third Party Vendors  
Coverage – [[DTCC]]’s role in the US financial markets makes it a substantial source for Corporate Actions 
announcement information.  [[DTCC]] processes Corporate Actions events for over 3.5 million eligible [[securities]].  By 
leveraging the new ISO 20022 XML message format, [[DTCC]] provides the most prevalent amount of Corporate 
Actions announcements with the most holistic amount of data per message in the industry.  [[DTCC]]’s Corporate 
Actions announcement service provides the following types of announcements:   
• Distributions 
 [[Stock]] Dividends 
 Special Dividends 
 Cash Dividends 
 Principal & Interest (P&I) 
 Capital Gain Distributions 
 Return of Capital 
 Spin-Offs 
 [[Stock]] Splits 
 Sale of Rights 
 Tax Refund 
 Interest 

---

## Page 2

 
2 | Page  
[[DTCC]] Non-Confidential 
 [[liquidation]] 
 Pay in Kind 
• Redemptions 
 Partial Calls 
 Final Pay Downs 
 Maturity 
 Full and Partial Pre-Funding 
 Partial Defeasances 
 Terminations 
 Full Calls 
• Reorganizations 
 Exchange Offers  
 Conversions 
 Dutch Auctions 
 Mergers 
 Puts 
 Reverse [[Stock]] Splits 
 Tender Offers 
 Rights and Warrant Exercises 
 Changes 
 General Information 
 Mandatory Exchanges 
 Liquidations 
 Name Changes 
 Security Separations 
 Worthless 
• Meetings 
 Annual General Shareholder Meeting Notification ([[Proxy]]) 
• Factors 
 Principal Factor Data on Issue Remainder 
• Maturity Cash 
 Cash Payout for Issue Maturity  
How – [[DTCC]]’s Corporate Actions Announcement messages are transmitted to customers using dedicated circuits 
on a real-time basis, as the announcement is made available to [[DTCC]].  Customers using FTP connections can 
receive messages via 16 batch files Sunday through Friday. 
Subscribing customers may use various methods to transfer ISO 20022 XML messages including: 
1. File Transfer Protocol (FTP) “get / pull” data via broadband internet 
2. Swift MQ (Real Time Delivery) 
3. TCPI = FTP push via the internet (Encrypted) 
TCP = FTP push via [[DTCC]] SMART Circuit 
NDM (Network Data Mover) via [[DTCC]] SMART Circuit 
 

---

## Page 3

 
3 | Page  
[[DTCC]] Non-Confidential 
FTP Time Slice Availability: 
Time SLICES Time SLICES 
1:30 Slice 01 15:00 Slice 09 
3:30 Slice 02 16:00 Slice 10 
6:00 Slice 03 17:00 Slice 11 
9:00 Slice 04 18:00 Slice 12 
11:00 Slice 05 19:00 Slice 13  
12:00 Slice 06 20:00 Slice 14 ([[EOD]]) 
13:00 Slice 07 21:00 Slice 15 
14:00 Slice 08 23:30 Slice 16 
 
Sample Message Layout- 
- <Document xmlns="XXX" xmlns:xsi="XXX"> 
- <CorpActnNtfctn> 
- <NtfctnGnlInf> 
  <NtfctnTp>XXXX</NtfctnTp>  
- <PrcgSts> 
- <Cd> 
  <EvtCmpltnsSts>XXXX</EvtCmpltnsSts>  
  <EvtConfSts>XXXX</EvtConfSts>  
  </Cd> 
  </PrcgSts> 
  </NtfctnGnlInf> 
- <PrvsNtfctnId> 
  <[[ID]]>XXXXXXXX</[[ID]]>  
  </PrvsNtfctnId> 
- <CorpActnGnlInf> 
  <CorpActnEvtId>XXXXXXXX</CorpActnEvtId>  
  <OffclCorpActnEvtId>XXXXXXXXXX</OffclCorpActnEvtId>  
- <EvtPrcgTp> 
  <Cd>XXXX</Cd>  
  </EvtPrcgTp> 
- <EvtTp> 
  <Cd>XXXX</Cd>  
  </EvtTp> 
- <MndtryVlntryEvtTp> 
  <Cd>XXXX</Cd>  
  </MndtryVlntryEvtTp> 
- <UndrlygScty> 
- <FinInstrmId> 
- <OthrId> 

---

## Page 4

 
4 | Page  
[[DTCC]] Non-Confidential 
  <[[ID]]>XXXXXXXXX</[[ID]]>  
- <Tp> 
  <Cd>XXXX</Cd>  
  </Tp> 
  </OthrId> 
  <Desc>XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX</Desc>  
  </FinInstrmId> 
- <PlcOfListg> 
  <MktIdrCd>XXXX</MktIdrCd>  
  </PlcOfListg> 
- <ClssfctnTp> 
  <ClssfctnFinInstrm>XXXXXX</ClssfctnFinInstrm>  
  </ClssfctnTp> 
  </UndrlygScty> 
  </CorpActnGnlInf> 
- <AcctDtls> 
- <ForAllAccts> 
  <IdCd>XXXX</IdCd>  
  </ForAllAccts> 
  </AcctDtls> 
- <CorpActnDtls> 
- <DtDtls> 
- <RcrdDt> 
- <Dt> 
  <Dt>XXXX-XX-XX</Dt>  
  </Dt> 
  </RcrdDt> 
- <ExDvddDt> 
- <Dt> 
  <Dt>XXXX-XX-XX</Dt>  
  </Dt> 
  </ExDvddDt> 
  </DtDtls> 
  </CorpActnDtls> 
- <CorpActnOptnDtls> 
  <OptnNb>XXX</OptnNb>  
- <OptnTp> 
  <Cd>XXXX</Cd>  
  </OptnTp> 
- <DfltPrcgOrStgInstr> 
  <DfltOptnInd>XXXX</DfltOptnInd>  
  </DfltPrcgOrStgInstr> 
- <CshMvmntDtls> 
  <CdtDbtInd>XXXX</CdtDbtInd>  
- <IncmTp> 
  <[[ID]]>XXXX</[[ID]]>  
  <Issr>IRSX</Issr>  

---

## Page 5

 
5 | Page  
[[DTCC]] Non-Confidential 
  </IncmTp> 
- <DtDtls> 
- <PmtDt> 
- <Dt> 
  <Dt>XXXX-XX-XX</Dt>  
  </Dt> 
  </PmtDt> 
  </DtDtls> 
- <RateAndAmtDtls> 
- <GrssDvddRate> 
- <RateTpAndAmtAndRateSts> 
- <RateTp> 
  <Cd>XXXX</Cd>  
  </RateTp> 
  <Amt Ccy="XXX">XXX</Amt>  
  </RateTpAndAmtAndRateSts> 
  </GrssDvddRate> 
- <NetDvddRate> 
  <Amt Ccy="XXX">XXXX</Amt>  
  </NetDvddRate> 
- <WhldgOfLclTax> 
  <Rate>X</Rate>  
  </WhldgOfLclTax> 
  </RateAndAmtDtls> 
  </CshMvmntDtls> 
  </CorpActnOptnDtls> 
- <Regar> 
- <NmAndAdr> 
  <Nm>XXXXXXXXXX</Nm>  
  </NmAndAdr> 
  </Regar> 
- <SplmtryData> 
- <Envlp> 
- <Document xmlns="XXX" xmlns:xsi="XXX"> 
- <DTCCCANOCSDDataSD1> 
- <NtfctnGnlInf> 
  <PlcAndNm>XXXXXX</PlcAndNm>  
  <CretDtAndTm>XXXX-XX-XXTXX:XX:XX</CretDtAndTm>  
  <UpdDtAndTm>XXXX-XX-XXTXX:XX:XX</UpdDtAndTm>  
  </NtfctnGnlInf> 
- <CorpActnGnlInf> 
  <PlcAndNm>XXXXX</PlcAndNm>  
  <AsstSvcrPrcgFlg>XXXX</AsstSvcrPrcgFlg>  
  </CorpActnGnlInf> 
- <UndrlygScty> 
  <PlcAndNm>XXXXX</PlcAndNm>  
  <CtryOfListg>XX</CtryOfListg>  

---

## Page 6

 
6 | Page  
[[DTCC]] Non-Confidential 
  <DTCAsstClss>XXXX</DTCAsstClss>  
  <DTCAsstTp>XXXX</DTCAsstTp>  
  <TckrSymb>XXX</TckrSymb>  
  </UndrlygScty> 
- <CorpActnDtls> 
  <PlcAndNm>XXXXX</PlcAndNm>  
  <CutOffDays>X</CutOffDays>  
  <RDPRefNb>XXXXXXXXXXXXXXXXXXXXXX</RDPRefNb>  
  </CorpActnDtls> 
- <CorpActnDtDtls> 
  <PlcAndNm>XXXXXXXXXX</PlcAndNm>  
  <DTCPosCaptrDt>XXXX-XX-XX</DTCPosCaptrDt>  
  </CorpActnDtDtls> 
- <OptnDtls> 
  <PlcAndNm>XXXXXXXXXX</PlcAndNm>  
  <DfltOptnFlg>XXXX</DfltOptnFlg>  
  <RDPRefNb>XXXXXXXXXXXXXXXXXXXXXX</RDPRefNb>  
  </OptnDtls> 
- <CshMvmntDtls> 
  <PlcAndNm>XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX</PlcAndNm>  
  <DTCPayMtd>X</DTCPayMtd>  
  <DTCPayOrdr>X</DTCPayOrdr>  
  <NRATaxRptblFlg>XXXX</NRATaxRptblFlg>  
- <DclrdGrssRate> 
- <AmtPric> 
  <AmtPricTp>XXXX</AmtPricTp>  
  <PricVal Ccy="XXX">XXX</PricVal>  
  </AmtPric> 
  </DclrdGrssRate> 
- <DTCUSTaxInstrPrd> 
- <StartDt> 
- <Dt> 
  <Dt>XXXX-XX-XX</Dt>  
  </Dt> 
  </StartDt> 
- <EndDt> 
- <Dt> 
  <Dt>XXXX-XX-XX</Dt>  
  </Dt> 
  </EndDt> 
  </DTCUSTaxInstrPrd> 
  <RDPRefNb>XXXXXXXXXXXXXXXXXXXXXXXXXXX</RDPRefNb>  
  </CshMvmntDtls> 
- <Agt> 
  <PlcAndNm>XXXXXXXXXXXXXXXXXXXXXXXX</PlcAndNm>  
  <AgtId>XXXXXXXX</AgtId>  
  </Agt> 

---

## Page 7

 
7 | Page  
[[DTCC]] Non-Confidential 
  </DTCCCANOCSDDataSD1> 
  </Document> 
  </Envlp> 
  </SplmtryData> 
  </CorpActnNtfctn> 
  </Document> 
 
 