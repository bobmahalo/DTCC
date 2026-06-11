---
title: "UTC Broker Suspension Message"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc120_broker-suspension-message-2022Jun3.pdf"
pages: 4
size: "1138.7 KB"
category: "UTC"
ingested_on: "2026-06-05"
---

# UTC Broker Suspension Message

**Original File:** [utc120_broker-suspension-message-2022Jun3.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc120_broker-suspension-message-2022Jun3.pdf)  
**Category:** UTC  
**Total Pages:** 4  
**File Size:** 1138.7 KB  

---

## Page 1

UNIVERSAL TRADE CAPTURE (UTC) 
UTC [[Broker]] SUSPENSION MESSAGE
June 3, 2022


---

## Page 2

UTCBrokerSuspensionMessageFormat 2
UTC [[Broker]] SUSPENSION MESSAGE FORMAT
View the header, application sequence control, and standard trailer information for the UTC [[Broker]] Suspension 
message format.
Header
View the Header record details for the UTC [[Broker]] Suspension message format:
FIX 
Tag 
No.
Field Name XML Name Data Type Description Message Value Required 
(Y/N)
8 BeginString  String Identifies the beginning of the new message and 
protocol version. 
Value: FIX4.4
Y
9 BodyLength  Length Message length, in bytes, forward to the 
CheckSum field.
Y
35 Message @MsgTyp String Defines the message type.
Value: B
Y
49 SenderCompID@SID String Assigned value used to identify the firm sending 
the message.
Value: [[DTCC]]
Y
56 TargetCompID @TID String Assigned value used to identify the firm receiving 
the message.
Y
34 MsgSeqNum @SeqNum SeqNum Integer message sequence number. Y
52 SendingTime @Snt timestamp Time of the message transmission (always 
expressed in the universal time coordinated, also 
known as GMT). 
Y
UTCBrokerSuspensionMessage

---

## Page 3

UTCBrokerSuspensionMessageFormat 3
Application Sequence Control
View the Application Sequence Control record details for the UTC [[Broker]] Suspension message format:
FIX Tag 
No.
Field NameXML Name Data 
Type
Description Message Value Required 
(Y/N)
148 Headline @headline String Headline of the new message. 
Example:
00000000. [[Broker]] has been suspended from 
trading.
Where 00000000 is the [[DTCC]] [[Broker]] number.
Y
Standard Trailer
View the Standard Trailer record details for the UTC [[Broker]] Suspension message format:
FIX Tag No. Field Name XML Name Data Type Description Message Value Required (Y/N)
10 CheckSum  String Three byte, simple CheckSum. Y
UTCBrokerSuspensionMessage

---

## Page 4

FOR MORE INFORMATION
Email [[DTCC]] Learning at:
corelearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com
©2022DTCC.Allrightsreserved.   [[DTCC]],[[DTCC]](Stylized),ADVANCINGFINANCIALMARKETS.TOGETHER,
andtheInterlockergraphicareregisteredandunregisteredtrademarksofTheDepositoryTrust&Clearing
Corporation.
Theservicesdescribedhereinareprovidedunderthe“[[DTCC]]”brandnamebycertainaffiliatesofTheDepository
Trust&ClearingCorporation(“[[DTCC]]”).  DTCCitselfdoesnotprovidesuchservices.  Eachoftheseaffiliatesisa
separatelegalentity,subjecttothelawsandregulationsoftheparticularcountryorcountriesinwhichsuchentity
operates.Pleaseseewww.[[DTCC]].comformoreinformationonDTCC,itsaffiliatesandtheservicestheyoffer.
DocInfo:June3,2022
PublicationCode:UTC120
Service:UniversalTradeCapture(UTC)
Title:UTCBrokerSuspensionMessage