---
title: "EPN MQ Implementation Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs179_epn-mq-impl-guide.pdf"
pages: 13
size: "366.9 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# EPN MQ Implementation Guide

**Original File:** [mbs179_epn-mq-impl-guide.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs179_epn-mq-impl-guide.pdf)  
**Category:** MBSD  
**Total Pages:** 13  
**File Size:** 366.9 KB  

---

## Page 1

Mortgage-Backed [[securities]]  
FIXED INCOME CLEARING CORPORATION: 
EPN MQ IMPLEMENTATION GUIDE 
JANUARY  12, 2024 

---

## Page 2

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEM ENTATION 2 
TABLE OF CONTENTS 
EPN MQ Implementation................................................................................................................... 3 
Client Onboarding to MQ ................................................................................................................. 3 
Client Changes for MQ .................................................................................................................... 3 
MQ Mess ag e Head er ...................................................................................................................... 3 
Client Sends an MQ Message to EPN Server – Inbound Message ......................................................... 3 
Client Receives an MQ Response from EPN Server – Outbound Message.............................................. 5 
Legend of Message Format.............................................................................................................. 6 
Channel Used for Inbound and Outbound Mess ag e ............................................................................. 7 
Migration Strategies and Considerations with Respect to EPN Connection [[ID]] .......................................... 7 
Mess ag e Flo w.............................................................................................................................. 10 
New Reject Code for MQ Header Validation Failures.......................................................................... 11 
New Start of D ay  TX Mess ag e ........................................................................................................ 11 
D ep rec ated Mess ag e Typ es ........................................................................................................... 11 
References .................................................................................................................................. 12 

---

## Page 3

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEM ENTATION 3 
EPN MQ IMPLEMENTATION 
Client Onboarding to MQ  
Please refer to [[DTCC]] onboarding documentation for the onboarding procedures.  
Using the above documentation with [[DTCC]] onboarding team, identify the Local and Remote queue that you 
will use for your organization communication via MQ.  
Client Changes for  MQ 
Update client code to add the MQ functionality to allow you to enqueue and dequeue message to MQ using the 
created remote and local queues from 2.5.1. In the MQ Payload add the message header and EPN message 
for outbound message, see further details below. For inbound message parse the payload extracting the 
message header and EPN message.   
MQ Message Header  
The MQ Message Header specifies the sending and receiving parties of the message. MBSD has added a 
password to this header to provide an additional level of security – password value is existing EPN passwor d 
(any existing EPN connection password used in the legacy Log On message can be used). The MQ Message 
Header is the first component of every message and is part of the message body and not the MQMD Header. 
EPN requires that the fields in the header have a fixed format. The header is populated as a continuous string 
of data, which terminates as a regular data field (with a carriage return line feed “CRLF”) input.  
When members receive messages, the password field mentioned would be our password and we would not 
populate it leaving the field as blanks.    
Client Sends an MQ Message to EPN Server –  Inbound Message  
Block/Tag   Notes   
Message Header   Each message must contain a message header.  All header fields are mandatory fixed format 
with trailing blanks, where required.   
Password   12!c   A password will be pre -assigned by EPN.  Left justified, padded with blanks  
Note:  
Existing EPN users sending MQ messages can use any of their existing EPN connections 
passwords that they use for legacy Logon Messages.    
Receiver   8!c   MBSEPN System w ill be the recipient of the inbound messages.  Left justified, padded with 
blanks  
Sender   8!c   MBSD account [[ID]] of the [[participant]] sending the message.  Left justified, padded with 
blanks  
Sender’s 
Submission 
Business Date  
8!c  Sender’s submission business date in format MMDDYYYY  
Message   This is the normal EPN messages body defined in “ MBS EPN Message Layouts.pdf”  Doc.   

---

## Page 4

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEM ENTATION 4 
Inbound Example Payload for MQ:  
The @ symbol represents one, single blank space in the following example block  
Field  Value/[[default]] Value  
Password 1  123456789012  
Receiver 2  MBSEPN@@  
Sender  ABCD@@@@  
Sender’s Submission Business Date  02032020  
1Password should be left justified and padded with spaces if the password length is less than 12 characters  2Hardcoded field with the value MBSEPN  
For the above example, the message header would look like the following line:  
123456789012MBSEPN@@ABCD@@@@02032020  
The message body should be constructed using the current message layout as defined in “MBS EPN Message 
Layouts.pdf” Doc. Following is a sample of a complete message that includes the EPN MQ header on line 1 
and the EPN message body starting on line 2.  
123456789012MBSEPN  ABCD    02032020  
ON00000300201231234ABCDAAAA01F123456 90000000000 
1000000000000001030120190312201904282019I123456756          0000      671 
TRID=1234567890=              00012       0BM381000152587705000006012031 671 
4832                          0009999998306553607103140 
040120180001000999999830000015277800100152761 
Note  
Start message indicator and End message indicator is not included in this example, because they are non -printable 
characters. Please ensure both are in the message body i.e. line 2.  

---

## Page 5

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEM ENTATION 5 
Client Receives an MQ Response from EPN Server –  Outbound 
Message 
Block/Tag   Notes   
Message 
Header   
Each message must contain a message header. All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password   12!c   Password will be blank filled on all response messages from MBSD.  Left justified, padded with 
blanks  
Sender   8!c   MBSEPN System will always be the sender of the outbound messages.  Left justified, padded 
with blanks  
Receiver   8!c   MBSD account [[ID]] of the [[participant]] receiving the message.  Left justified, padded with blanks  
Sender’s 
Submission 
Business Date   
8!c  Sender’s submission business date in format MMDDYYYY  
Original 
Submission 
Business Date  
8!c  Submission date of original message in format MMDDYYYY. Defaulted to current business 
date. For example, if a client sends a message with the Sender’s Submission business date of 
02032020 after EPN was shutdown  
Feb 3rd 2020, EPN will process the message on Feb 4th and populate 02032020 in this field in 
its response back to the client indicating the submission business date of the original message.  
Message This is the normal EPN messages body defined in “MBS EPN Message Layouts.pdf” Doc.  
Outbound Example Payload for MQ:   
The @ symbol represents one, single blank space in the following example block  
Field  Value/[[default]] Value  
Password 1  @@@@@@@@@@@@ 
Sender 2  MBSEPN@@ 
Receiver  ABCD@@@@ 
Sender’s Submission Business 
Date  
02032020 
Original Submission Date  02032020 
1Password should be left justified and padded with spaces if the password length is less than 12 characters 2Hardcoded field with the value MBSEPN  
For the above example, the message header would look like the following l ine. 
@@@@@@@@@@@@MBSEPN@@ABCD@@@@0203202002032020  
Example 1: Complete message response for a Valid incoming MQ message header  
The output message body from EPN will be constructed using the current message layout as defined in “MBS 
EPN Message Layouts.pdf” Doc.  The following is a sample of a complete AA message that includes the 
header on line 1 and the message body starting on line 2.  

---

## Page 6

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEM ENTATION 6 
ADVANCING FINANCIAL MARKETS. TOGETHER.TM 
            MBSEPN ABCD    0203202002032020  
AA00037800204351435020100008       201902220000200020010211800 
Note  
Start message indicator and End message indicator is not included in this example, because they are non -printable 
characters.  
Example 2: Complete message response for an Invalid incoming message  
In the event the inbound MQ header fails validation or authentication or empty date or invalid date format, EPN 
will send a negative AA message with the ACK code 0250. EPN will handle the inbound and outbound 
sequence numbers as described in the “Message Sequence Numbering and Gap Detection” section of the 
EPN Implementation guide.  
            MBSEPN  ABCD    0203202003feb2020      
AA00037800204351435020100008       201902220000250020010211800 
Example 3: Complete message response for incoming message that does not contain current   
business date 
In the event the inbound MQ header fails validation with submission date is not current business date, EPN will 
send a negative AA message with the ACK code 0251. EPN will handle the inbound and outbound sequence 
numbers as described in the “Message Sequence Numbering and Gap Detection” section of the EPN 
Implementation guide.  
            MBSEPN  ABCD    0203202002012020      
AA00037800204351435020100008       201902220000251020010211800 
Legend of Message Format  
Char  Meaning  Format  Example Usage  
a   Upper Case Alpha Characters   6a   ABCDEF   
c   Alphanumeric Characters (upper case only)   6c   AB12EF   
d   Decimal Number (decimal period)   15d   2035.45   
e   Space   1e   (1blank space)   
n   Numeric Characters   8n   19950131   
x   Any Printable ASCII Symbol   20x   Anytime &   
/   The literal “/” as a separator   6a/2a   AABny12plEacFe/N Y   
[   Optional element format   [/4c]   [optional data]   
]   
[-]   
Optional “sign” (negative) format   [-]   : “total_funds”:” -  
!   Fixed length field   12!c  ABCDEFGHIJKL   

---

## Page 7

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEM ENTATION 7 
Channel Used for Inbound and Outbound Message  
The acknowledge response will be sent to the client on the same channel on which EPN has received the 
response independent of the connection [[ID]] used in the message. In the case of forwarding the valid business 
message to the counterparty, EPN checks, if the account [[ID]] has been migrated to MQ. If it has been migrated 
to MQ, the business message will get redirected to the counterparty on MQ channel. Else, EPN will forward the 
message in TCP channel. Please refer the below tables.  
Receiving Channel for Acknowledgement from EPN:  
For messages sent by account, the acknowledge will be sent on the same channel in which EPN has received 
the message.  
Acknowledge Message  
Message Sent By  Type of Message  Channel Used by 
Client  
Acknowledge 
Sent to  
Response Channel 
Used  
ACC1  Admin Message  TCP  ACC1  TCP  
ACC1  Admin Message  MQ  ACC1  MQ  
ACC1  Business Message  TCP  ACC1  TCP  
ACC1  Business Message  MQ  ACC1  MQ  
Migration Strategies and Considerations with Respect to EPN 
Connection [[ID]]  
[[FICC]] suggests using a separate connection [[ID]] for the MQ connection and TCP connection. SR/RR/LS 
message retrieves the details for the Connection [[ID]]. By using the concept of separate connection [[ID]] for 
channel, client can ensure that the SR/RR/LS message sent through MQ will retrieve details for the MQ 
connection only. And the same will hold true for TCP.  
Clients who opt for communicating with EPN through MQ will have the ability to receive all of their incoming 
messages originating from EPN into multiple queues to support resiliency/DR requirements. This will work the 
same way as the existing setup that is in place for responding to TBA trade acknowledgements from MBS 
RTTM. Clients can work with the [[DTCC]] onboarding team at the time of MQ onboarding to configure multiple 
subscriptions and destinations as needed. Messages will be delivered to those destinations on an all or nothing 
basis. i.e. clients will not have the ability to choose what message type gets delivered to what dest ination 
(Example: AA to connection [[ID]] 1000 and ON to connection [[ID]] 2000 will not be supported).  
As far as EPN connection IDs are concerned, for clients who migrate to MQ, [[FICC]] recommends that client 
choose a single connection [[ID]]. Having multiple connection IDs will result in duplicate messages delivered from 
EPN to the clients on the same MQ channel.  
Following are the migration recommendations with different combination of account [[ID]] and connection [[ID]].  

---

## Page 8

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEM ENTATION 8 
Scenario  Account  Connection 
[[ID]]  
Migration Recommenda tion  Example  
1  One  One  If an EPN client has one account that uses a 
single connection [[ID]], our recommendation is:  
- Enable MQ at the account level  
- Clients should ensure that their CTCI & 
MQ communications are not active 
simultaneously  
- Use the existing connection [[ID]] to 
communicate with EPN for sending 
messages.   
- EPN will in turn use the same connection 
[[ID]] to messages sent back to the clients.  
CTCI Setup: 
- Client uses connection [[ID]] 
1200 to submit messages 
to EPN for account ACC1  
- EPN uses connection [[ID]] 
1200 to respond to 
messages for account 
ACC1 MQ Setup: 
Remains the same  
- Client uses connection [[ID]] 
1200 to submit messages 
to EPN for account ACC1  
- EPN uses connection [[ID]] 
1200 to respond to 
messages for account 
ACC1  
2  One  Many  If an EPN client has one account that uses 
many connection ids, our recommendation is:  
- Enable MQ at the account level  
- Keep a single connection [[ID]] (the lowest 
numbered connection [[ID]]) and disable 
others.  -  Use the one remaining 
connection [[ID]] to communicate with EPN 
for sending messages.  
- EPN will in turn use the same connection 
to send messages back to the clients.  
CTCI Setup: 
- Client has three 
connections 1200, 1201, 
1202 mapped to account 
ACC1 
- Client uses connection [[ID]] 
1200 submit ON 
messages and connection 
[[ID]] 1201 to submit all other 
messages to EPN for 
account ACC1  
- EPN uses connection [[ID]] 
1202 to respond to all 
messages for account 
ACC1 MQ Setup: 
- Client uses connection [[ID]] 
1200 to submit all 
messages to EPN for 
account ACC1  -  EPN 
uses connection [[ID]] 1200 to 
respond to all messages 
for account ACC1  

---

## Page 9

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEM ENTATION 9 
Scenario  Account  Connection 
[[ID]]  
Migration Recommenda tion  Example  
3  Many  One  If an EPN client has many accounts that use 
one connection [[ID]] as a shared connection, our 
recommendation is:  
- Enable MQ at the account level  
- Create a new connection [[ID]] that will be 
exclusively used for MQ 
submissions/receipt.  
- Migrate accounts that are designated for 
MQ submission to the new connection [[ID]] 
in batches or all at once based on client 
preference.  
- Use the new MQ specific connection [[ID]] to 
communicate with EPN for sending 
messages.   
- EPN will in turn use the same conne ction 
to messages sent back to the clients.  -  
EPN will disable the old CTCI connection 
[[ID]] once all client accounts are moved to 
MQ i.e. the new connection [[ID]].  
CTCI Setup: 
- Client has one 
connections 1200 mapped 
to multiple accounts 
ACC1, ACC2 and ACC3  
- Client uses connection [[ID]] 
1200 submit all messages 
for accounts ACC1, ACC2 
and ACC3  
- EPN uses connection [[ID]] 
1200 to respond to all 
messages for account 
ACC1, ACC2 and ACC3 
MQ Setup: 
- Client uses new 
connection [[ID]] 1300 to 
submit all messages to 
EPN for account s ACC1, 
ACC2 and ACC3  
- EPN uses connection [[ID]] 
1300 to respond to all 
messages for accounts 
ACC1,ACC2 and ACC3  
4  Many  Many  If an EPN client has many accounts that each 
use many connection ids as a shared 
connection, our recommendation is:  
- Enable MQ at the account level  
- Create a new connection [[ID]] that will be 
exclusively used for MQ 
submissions/receipt.  
- Migrate accounts that are designated for 
MQ submission to the new connection [[ID]] 
in batches or all at once based on client 
preference.  
- Use the new MQ specific connection [[ID]] to 
communicate with EPN for sending 
messages.   
- EPN will in turn use the same conne ction 
to messages sent back to the clients.  -  
EPN will disable the old CTCI connection 
[[ID]] once all client accounts are moved to 
MQ i.e. the new connection [[ID]].  
CTCI Setup: 
- Client uses connection [[ID]] 
1200 to submit ON 
messages for multiple 
accounts ACC1, AC C2 
and ACC3.  
- Client uses connection [[ID]] 
1201 to submit all other 
messages for multiple 
accounts ACC1, ACC2 
and ACC3   
- EPN uses connection [[ID]] 
1202 to respond to all 
messages for account 
ACC1, ACC2 and ACC3 
MQ Setup: 
- Client uses new 
connection [[ID]] 1300 to 
submit all messages to 
EPN for accounts ACC1, 
ACC2 and ACC3  
- EPN uses connection [[ID]] 
1300 to respond to all 
messages for accounts 
ACC1,ACC2 and ACC3  

---

## Page 10

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEM ENTATION 10 
Message Flow  
a. For every message received via MQ the EPN performs the following steps:   
• Parse the payload – the payload should have 2 lines, the first should be the message header the 
second should be the normal EPN message.  The MQ message header is populated as a continuous 
string of data, which terminates as a regular data field (with a carriage return line feed “CRLF”).  
• Validate the formatting and contents of all the fields in the MQ message header  
• If MQ message header is successfully validated and authenticated, the MQ message body will be 
processed and validated based on the formatting and validation rules described in the EPN 
Implementation guide.  
b. If the MQ message header fails validation or authentication, the message will be rejected. EPN will send a 
negative AA with ACK code of 0250 regardless of the type of the original message, as described above in 
example 2 under section 5.  
Following are the possible failure scenarios related to the MQ message header and body and how EPN 
will handle them 
Scenario Detail  EPN's Handling of the Scenario  
#  MQ Header 
Validation  
Message 
Body 
Validation  
Identifiable 
Source (Account)  
Sequence Handling  Response Sent  
1  Failed  Failed  No  No Sequences will be updated   No  
2  Failed  Failed  Yes  Input and Output sequences will 
be updated  
Yes  
3  Failed  Successful  Yes  Input and Output sequences will 
be updated  
Yes  
4  Successful  Failed  No  No Sequences will be updated   No  
5  Successful  Failed  Yes  Input and Output sequences will 
be updated  
Yes  
6  Successful  Successful  Yes  Input and Output sequences will 
be updated  
Yes  
c. For every message sent out:  
• EPN will add a message header at the beginning of the payload as described in section 5.  
• The recipient should parse the payload and extract the MQ message header before processing the 
MQ message body based on the rules laid out in the MBS EPN Message Layouts and  EPN 
Implementation guide. 

---

## Page 11

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEM ENTATION 11 
New Reject Code for MQ Header Validation Failures.  
Value  Ack Reason  Comments  
0250  Invalid MQ Message header  EPN will send an AA message with ACK code 0250 in the event 
the MQ message header failed validation and/or authentication  
0251  Invalid current business 
date 
EPN will send an AA message with ACK code 0251 in the event 
the submission date in header is not current business date.  
New Start of Day TX Message  
For all clients who have converted to MQ, EPN will send out a TX message first thing in the morning. This 
message will include the current business date in the MMDDYYYY format.  
The type of the TX message will be 22 and the sequence number will be 000001. The content of the Message 
Text field will be of the format: “START OF BUSINESS DAY MMDDYYYY”  
Following is a sample TX message that will be sent out.  
            MBSEPN  ABCD    0203202002032020 
TX0000010020384138422START OF BUSINESS DAY 02032020 
Note: 
Existing TCP (CTCI) clients will not receive this TX message.  
MQ Messages sent to EPN after the close of business for a given business day will get queued up 1. When 
EPN opens for business on the following business day, EPN will first send out the Start of day TX message as 
described above. It will then begin processing the messages available in the queue.  EPN will check the EPN 
MQ message headers of the queued messages for the current business day. If the previous business date is 
found within the MQ Message Header, the message will be rejected for reason code 0251 (INVALID 
CURRENT BUSINESS DATE).  All remaining messages submitted for the current business day will be 
validated and processed as per the normal validation rules.  
Deprecated Message Typ es 
As mentioned in the EPN MQ FAQ documentation, the following non-business EPN legacy message types will 
no longer be needed through the MQ channel due to the reliability and durability guaranteed by the MQ 
infrastructure.  
• Heartbeat Primary (HP)  
• Heartbeat Acknowledgement (HA)  
• Logon (LO)  
 
1 Refer to the MBSD Processing Schedule and Timeframes on [[DTCC]].com for the EPN System Availability EPN will continue to process and respond back to 
these messages during initial implementation but we recommend M Q clients not to use these messages as these will be deprecated in the future.  

---

## Page 12

Fixed Income Clearing Corporation: 
EPN MQ Implementation Guide  
EPN MQ IMPLEMENTATION 12 
References  
• EPN MQ User/FAQ document http://www.[[DTCC]].com/~/media/Files/Downloa ds/Clearing-
Services/[[FICC]]/MBSD/EPN-MQ-UserDocument.pdf  
• EPN Implementation Guide http://www.[[DTCC]].com/~/media /Files/Downloads/Clearing -
Services/[[FICC]]/MBSD/EPNImplementation- Guide.pdf  
• MBS EPN Message Layouts http://www.[[DTCC]].com/~/media/Files/Downloads/Clearing -
Services/[[FICC]]/MBSD /EPN_Message_Layout_011008a.pdf  
• MBS EPN Guidelines and Codes http://www.[[DTCC]].com/~/media/Files/Downloads/Clearing -
Services/[[FICC]]/MBSD/EPN_General_Guidelines_Codes_011608a.pdf  
 

---

## Page 13

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject  to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
Doc Date: January 12, 2024 
Publication Code : MBS179 
Service: Mortgage -Backed [[securities]]  
Title: Fixed Income Clearing Corporation: EPN MQ Implementation Guide  
For More Information  
Email [[DTCC]] Learning at:  
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 