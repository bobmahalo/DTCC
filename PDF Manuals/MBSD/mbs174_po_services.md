---
title: "MBSD Pair-Off Service Enhancements Specifications"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs174_po_services.pdf"
pages: 25
size: "452.1 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD Pair-Off Service Enhancements Specifications

**Original File:** [mbs174_po_services.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs174_po_services.pdf)  
**Category:** MBSD  
**Total Pages:** 25  
**File Size:** 452.1 KB  

---

## Page 1

 [[DTCC]] Internal (Green)  
  
 
 
FIXED INCOME CLEARING 
CORPORATION 
 
MBSD PAIR-OFF SERVICE ENHANCEMENTS SPECIFICATIONS  
 
VERSION 1.0 
JUNE 1, 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular co untry or countries in which such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: June 1, 2023 
Publication Code:  MBS174 
Service: Fixed Income Clearing Corporation 
Title: MBSD Pair-Off Service Enhancements Specifications  
 

---

## Page 3

MBSD Pair-Off Service Enhancements Specifications  
 
 3 
TABLE OF CONTENTS 
 
1. Executive Summary ...............................................................................................................5  
2. Service Scope .......................................................................................................................6  
2.1 Out of Scope.............................................................................................................6  
2.2 Onboarding Assumptions ............................................................................................6  
3. Service Information ...............................................................................................................7  
3.1 PO Message Types and Validation Rules ......................................................................7  
3.1.1 Pair-Off Requests ......................................................................................................7  
3.1.2 DK of Pair-Off ...........................................................................................................7  
3.1.3 Affirm of Pair-Off........................................................................................................8  
3.1.4 Cancel of PO ............................................................................................................8  
3.1.5 Application Acknowledgment of Pair-Off Mes s ages.........................................................8  
3.2 Mess ag e Flo ws .........................................................................................................9  
3.2.1 Sub miss io n of PO req uest rejected  by [[FICC]] app lic atio n ..................................................9  
3.2.2 Original PO request passed to contra and affirmed by contra ......................................... 10 
3.2.3 Original PO request passe d to contra  but DKe d by con tra .............................................. 11 
3.2.4 Original PO request passed to contra but then canceled by submitted before contra is able to 
respond 12 
3.2.5 Original PO request passed to contra, affirmed by contra, and then canceled by submitter.. 13 
3.3 Web for Pair-Offs..................................................................................................... 14 
3.3.1 Pair-Off D as hbo ard .................................................................................................. 14 
3.3.2 Pair-Off Search Screens ........................................................................................... 14 
3.3.3 Pair-Off Entry .......................................................................................................... 15 
3.3.4 Pair-Off Bulk Upload ................................................................................................ 16 
3.4 Pair-Off Mess ag e Sp ec ific atio ns ................................................................................ 16 
3.4.1 Formatting Conventions............................................................................................ 16 
3.4.2 Mess ag e D etail Specification ..................................................................................... 17 
3.5 Pair-Off MRO Outp ut................................................................................................ 18 

---

## Page 4

MBSD Pair-Off Service Enhancements Specifications  
 
 4 
3.6 Pair-Off Rejec t and  DK cod es .................................................................................... 18 
Appendix A: Message Samples ................................................................................................ 20 
PO Request Submitted ........................................................................................................... 20 
PO AA – positive ack sent back to original submitter ................................................................... 21 
PO AA – neg ativ e ack  rejected  d ue to inco rrec t contra................................................................. 21 
PO req uest p ass ed to Co ntra................................................................................................... 22 
PO affirm sub mitted  by  co ntra .................................................................................................. 23 
PO DK s ubmitted by  co ntra with unk no wn trad e reaso n ............................................................... 23 
PO Canc el s ubmitted.............................................................................................................. 24 
 
 
 

---

## Page 5

MBSD Pair-Off Service Enhancements Specifications  
 
Executiv e Summary 5 
1. EXECUTIVE SUMMARY 
The Fixed Income Clearing Corporations (“[[FICC]]”) is offering the EPN Pair-off (PO) service to allow 
members who have two or more offsetting positions with the same TBA [[CUSIP]] and Contractual 
[[settlement]] Date (“CSD”) to “pair-off” these positions and exclude them from the allocation process, 
thereby avoiding the need to make delivery of these pools. [[FICC]] currently provides this service for 
positions that are known to MBSD Clearing members via [[DO]] Not Allocate (“DNA”) service. However, 
[[FICC]] might not be exposed to the full set of MBS trades that are facing buy-side clients. The new Pair-off 
service will enable all EPN users to submit pair-off requests (submit, affirm, DK, and cancel requests) 
within the contractual [[settlement]] month through [[FICC]] and receive reports for their activity. In the first 
phase of this service, the cash [[settlement]] of the pair-off will still be processed outside of [[FICC]]. 
 

---

## Page 6

MBSD Pair-Off Service Enhancements Specifications  
 
Service Sc ope 6 
2. SERVICE SCOPE 
As part of the current offering, [[FICC]] will: 
a) Provide the ability for members to submit pair-off (“PO”) messages (including original PO 
requests, Affirms, DKs, and Cancels) via the existing EPN system if the submitter and contra of 
the messages are subscribed to the PO services, 
b) Provide the ability to view PO messages and submit individual PO requests or bulk files via Web 
screens,  
c) Generate end-of-day output via MROs, and  
d) Provide the ability for users to search and export to spreadsheets historical PO requests for a 
given date within a period of 5 years. 
2.1 Out of Scope 
This offering will not address [[settlement]] of pair-off payments through [[FICC]]. 
2.2 Onboarding Assumptions 
• Only EPN users can subscribe to PO services. 
• PO input and output are segregated from existing EPN channels. 
 

---

## Page 7

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 7 
3. SERVICE INFORMATION 
3.1 PO Message Types and Validation Rules 
The following are the allowed message types for PO services: 
• PO – Pair-off request 
• PD – DK of pair-off 
• PC – Cancel of pair-off 
• PF – Affirm of pair-off 
• PA – Application acknowledgment for pair-off messages. 
3.1.1 Pair-Off Requests 
• Message type = “PO” 
• The submitter’s Account [[ID]] must be an active EPN account that is subscribed to PO services. 
• The contra account [[ID]] must be an active EPN account that is subscribed to PO services. 
• The TBA [[CUSIP]] must be a valid [[CUSIP]] [[ID]] known to EPN. 
• The [[settlement]] Date mus t be a business date for the current calendar month. It may be a past 
date as long as it still falls within the same month. 
• The Trade Date must be a valid date that cannot fall after the [[settlement]] Date. 
• The sum of pair-off par on the Sell side must match the sum of pair-off par on the Buy Side. The 
number of trades for Buy and Sell can be many-to-many, one-to-many, or many-to-one. 
• Pair-off par cannot exceed the Original Trade Par value for each trade. 
3.1.2 DK of Pair-Off  
• Message type = “PD.” 
• The target message [[ID]] must be a valid and active message (unaffirmed, uncanceled, and un-
DKed). 
• The submitter of the DK is the contra of the targeted pair-off message.  
• The contra of the DK is the submitter of the targeted pair-off message. 

---

## Page 8

MBSD Pair-Off Service Enhancements Specification s 
 
Service Information 8 
• A valid DK reason code mus t b e provided. 
• The values of the TBA [[CUSIP]], [[settlement]] Date, Sub-Contra, and Pair-Off Payment fields on the 
DK message must match the values on the targeted pair-off message. 
3.1.3 Affirm of Pair-Off 
• Message type = “PF.” 
• The target Message [[ID]] must be a valid and active message (unaffirmed, uncanceled, and un-
DKed). 
• The submitter of the Affirm is the contra of the targeted pair-off message.  
• The contra of the Affirm is the submitter of the targeted pair-off message. 
• The values of the TBA [[CUSIP]], [[settlement]] Date, Sub-Contra, and Pair-Off Payment fields on the 
Affirm message must match the values on the targeted pair-off message. 
3.1.4 Cancel of Pair-Off 
• Message type = “PC.” 
• The target Message [[ID]] must be a valid and active message (uncanceled and un-DKed). It may 
be either affirmed or pending. 
• The submitter of the Cancel is the submitter of the targeted pair-off message. 
• A Cancel is allowed until last day of the CSD month. 
• The values of the Contra, TBA [[CUSIP]], [[settlement]] Date, Sub-Contra, and Pair-Off Payment fields 
on the Affirm message must match the values on the targeted pair-off message. 
3.1.5 Application Acknowledgment of Pair-Off Messages 
The application will respond to each message submitted by members with a “PA” response, notifying the 
[[Member]] that the message has been processed by the application. If a request is rejected, the PA 
response will contain a corresponding reject code. 
  

---

## Page 9

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 9 
3.2 Message Flows 
The following subsections contain message flows for PO activities. 
3.2.1 Submission of PO request rejected by [[FICC]] application 
 
 
  


---

## Page 10

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 10 
3.2.2 Original PO request passed to contra and affirmed by contra 
 
 
 
  


---

## Page 11

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 11 
3.2.3 Original PO request passed to contra but DKed by contra 
 
 
  


---

## Page 12

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 12 
3.2.4 Original PO request passed to contra but then canceled by 
submitted before contra is able to respond 
 
 
  


---

## Page 13

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 13 
3.2.5 Original PO request passed to contra, affirmed by contra, and then 
canceled by submitter 
 
 
 
  


---

## Page 14

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 14 
3.3 Web for Pair-Offs 
To support the Pair-Off application, the following screens are available for Pair-Off clients:  
• Pair-Off Dashboard to present the statistics for PO requests and their status, 
• Pair-Off Search screen to search for individual or collected PO requests, with the subsequent 
ability to Affirm, DK, or Cancel existing PO requests, 
• Pair-Off Entry screen to submit individual requests, and 
• Pair-Off Bulk File Upload screen. 
3.3.1 Pair-Off Dashboard 
The dashboard will display the number of pair-off requests within each corresponding status with its net 
pair-off payment amount. A hyperlink for each pair-off item will enable users to view a summary of POs of 
that type. 
 
3.3.2 Pair-Off Search Screens 
Users will be able to search for pair-off requests either submitted by or to their account. 
User will be able to search individual pair-off requests by the Pair-Off Identifier assigned by the system or 
by using the Advanced Query to filter by: 
• State of Pair-Off (Pending, Affirmed, DKed, Canceled), 
• Submitter Account [[ID]], 
• Contra Account [[ID]], 
• Sub-Contra [[ID]], 
• TBA [[CUSIP]], and/or  
• [[settlement]] Date. 


---

## Page 15

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 15 
Users will have a choice to submit a search for active transactions or historical transactions by specifying 
the Business Date. 
For active transactions only, result screens will allow users to execute actions on existing active records, 
such as: 
• Affirm or DK for p air-off requests submitted to the user account, and 
• Cancel for pair-off requests submitted by the user’s account [[ID]]. 
 
3.3.3 Pair-Off Entry 
Users will be able to create and submit pair-off requests from the Web in case the user does not have the 
ability to submit pair-off messages via MQ. The screen will allow users to populate fields for the header 
and details. Once submitted, the application will construct (in the background) a JSON formatted 
message and submit it for p air-off. 
 


---

## Page 16

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 16 
3.3.4 Pair-Off Bulk Upload 
Users will be able to upload a file containing multiple pair-off requests in JSON format, in case the us er 
does not have the ability to submit pair-off requests via MQ. The application will parse the file and submit 
individual messages for processing. 
3.4 Pair-Off Message Specifications 
Pair-off messages will be communicated via MQ in JSON format. Refer to the below sections for the 
formatting conventions and message detail specifications. Message samples are available in Exhibit A of 
this document.  
3.4.1 Formatting Conventions 
Please note that all layouts for the JSON messages (included in this section of the document) are 
organized using the following columns of data: 
Column Heading  Description 
M/O/R The M/O/R column defines whether the field is always M - Mandatory or is R – 
Mandatory if block is present or O - Optional.   
Tag The Tag column defines the exact tag value that must precede the field. Tags are 
always delimited by “:” (meaning a “:” would be the character immediately before 
and after the tag).  
Field Description The Field Description column provides a text descri ption of the purpose or use of 
a data field.  
Data Format  The Data Format column specifies the size and characters allowed within a data 
field.  
 
The following characters may appear in the Data Format Column or in any discussion of data format and 
content: 
Character Meaning Example 
 
Example Usage 
a Upper Case Alpha Characters 6a ABCDEF 
c Alphanumeric Characters (upper case 
only) 
6c AB12EF 
d Decimal Number (decimal period) 15d 2035.45 
e Space 1e (1blank space) 
n Numeric Characters 8n 19950131 
x Any Printable ASCII Symbol 20x Anytime & Any place 
/ The literal “/” as a separator 6a/2a AB12EF/NY 

---

## Page 17

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 17 
Character Meaning Example 
 
Example Usage 
[ ] Optional element format [/4c] [op tional data] 
[-] Optional “sign” (negative) format [-]  “pairoff_payment”:”-5.45” 
! Fixed length field 12!c ABCDEFGHIJKL 
 
All fields are, by definition, variable in length with a maximum field size specified, unless a fixed length 
format is defined by inclusion of the “!”, in which case the size specified is the fixed field size. In the case 
where the data value in the fixed length field is smaller than the field size specified, the data should be 
left-justified with trailing blanks. 
3.4.2 Message Detail Specification 
M/O/R Tag Field Description Data Format 
M  PO_REQUEST_HEADER Header of pair -off request message  
M   { Block Start  
M “submitter_id”:  Submitter Account [[ID]]  “4!c”, 
M “userclass”:  A userclass - password will be pre -assigned 
by EPN.  
Note: Existing EPN users sending MQ 
messages can use any of their existing EPN 
passwords that they use for EPN Messages.  
Userclass will be blank filled on all response 
messages from MBSD.  
“12c”, 
M “submission_ts”:  Submission Timestamp  “YYYYMMDDHHMMSS”, 
M “contra_id”:  MBS contra account [[ID]] “4!c”, 
O “sub_contra_id”:  MBS sub-contra account [[ID]] “4!c”, 
M “message_type”:  Message type such as PO – pair -off request, 
PD – dk of pair -off, 
PF – affirm pair -off, PC – cancel of pair -off, PA 
– application ack for PO  
“2!c”, 
M “tba_cusip”:  TBA [[CUSIP]] “9c”, 
M “stl_date”:  [[settlement]] Date  “YYYYMMDD”, 
M “pairoff _payment”:  Pair-off payment “[-]15d”[,] 
M “message_xref”:  External Reference of the Message “16c”[,] 
O “message_id”:  Assigned by EPN Message [[ID]]. Submitter does 
not populate this [[ID]] but EPN will populate the 
[[ID]] as part of passthrough msg to Contra  
“15c”[,] 

---

## Page 18

MBSD Pair-Off Service Enhancements Specifications  
 
Service Information 18 
M/O/R Tag Field Description Data Format 
O “pairoff_id”:  Pair-off [[ID]] assigned by EPN and used by 
submitter for PO Affirm, PO DK or PO Cancel 
requests  
“15c”[,] 
O “reason_code”:  DK Reason Code or Reject Reason Code  “4c”[,] 
O “comment”:  Comments provi ded by submitter “32c”[,] 
O  “ack_ts”:  Application Ack Timestamp  “YYYYMMDDHHMMSS”[,] 
O “pairoff _detail”:  [[pair off]] request detail block as repeating block 
– only required for original PO requests  
 
R   [ Repeat Block Start  
R   { Block Start  
R “buy_sell”:  Transaction type of trade: B – buy, S – sell “1!a”, 
R “trade_date”:  Trade Date  “YYYYMMDD”, 
R “price”:  Price up to 9 decimal digits  “12d”, 
R “pairoff _par”:  Pair-off Par of trade. Note: non -0 decimal 
digits are not allowed 
“15d”, 
O “orig_trade_par”:  Original Trade Par of trade. Note: non- 0 
decimal digits are not allowed  
“15d”[,] 
O “trade_xref”:  Client Trade Reference Number  “16c” 
R } Block End  [,] 
R ] Repeat Block End   
M } Block End  
M  PO_REQUEST_TRAILER Trailer of pair -off request message  
3.5 Pair-Off MRO Output 
Pair-off output will consist of Daily Activities and Current Pair-Off status and will be generated at the same 
time as EPN [[EOD]] reports. MRO files will be sent via the existing AutoRoute mechanism that is used for 
EPN MROs, provided that members subscribe to new pair-off products. The MRO format is described in 
the JSON MRO f or Pair-Off. 
 
3.6 Pair-Off Reject and DK codes 

---

## Page 19

MBSD Pair-Off Service Enhancements S pecifications 
 
Service Information 19 
CODE Description 
0100 INCORRECT SUBMITTER [[ID]] 
0101 INCORRECT CONTRA [[ID]] 
0102 TRADE UNKNOWN 
0107 INCORRECT PRICE 
0111 TRADE ALREADY SETTLED 
0112 INCORRECT TBA [[CUSIP]] 
0114 INCORRECT TRADE DATE 
0115 INCORRECT [[settlement]] DATE 
0117 INCORRECT PAR VALUE 
0119 DUPLICATE MESSAGE 
0124 INCORRECT SUB-ACCOUNT 
0150 ACCOUNT NOT ELIGIBLE FOR [[pair off]] 
0151 INCORRECT MSG FORMAT FOR [[pair off]] 
0152 UNBALANCED PO PAR BUY AND SELL SETS 
0153 [[pair off]] EXCEEDS ORIGINAL TRADE PAR 
0154 INVALID STATUS OF [[pair off]] 
0155 INVALID ACTION 
0156 INVALID REASON CODE 
0157 INVALID [[pair off]] AMOUNT 
0208 INVALID MESSAGE TYPE 
0250 INVALID AUTHENTICATION OF MQ MESSAGE 
0251 INVALID SUBMISSION DATE 
 

---

## Page 20

MBSD Pair-Off Service Enhancements Specifications  
 
Appendix A: Mess age Samples 20 
APPENDIX A: MESSAGE SAMPLES 
PO Request Submitted  
PO_REQUEST_HEADER { 
“submitter_id”:”MBXX”, 
“userclass”:”ABCDE“, 
“submission_ts:”20221230120034”, 
“contra_id”:”MBYY”, 
“sub_contra_id”:”ABCD”, 
“message_type”:”PO”, 
“tba_cusip”:” 01F0126A9”, 
“stl_date”:”20211014”, 
“pairoff _payment”:” 5449.22”, 
“message_xref”:”MYXREF” 
“pairoff _detail”:[ 
         { 
         “buy_sell”:”S”, 
         “trade_date”:”20211007”, 
          “price”:”96.84375”, 
          “pairoff _par”:”375000”, 
          “orig_trade_par”:”10000000”, 
          “trade_xref”:”TRADE1” 
       }, 
                     { 
         “buy_sell”:”B”, 
         “trade_date”:”20211012”, 
          “price”:” 96.515625”, 
          “pairoff _par”:”675000”, 
          “orig_trade_par”:”2000000”, 
          “trade_xref”:”TRADE2” 
       }, 
                     { 
         “buy_sell”:”S”, 
         “trade_date”:”20210922”, 
          “price”:” 97.921875”, 
          “pairoff _par”:”300000”, 

---

## Page 21

MBSD Pair-Off Service Enhancements Specifications  
 
Appendix A: Mess age Samples 21 
          “orig_trade_par”:”300000”, 
          “trade_xref”:”TRADE3” 
       } 
] 
}PO_REQUEST_TRAILER 
PO AA – positive ack sent back to original submitter 
 
PO_REQUEST_HEADER{ 
“submitter_id”:”MBXX”, 
“userclass”:” “, 
“submission_ts:”20220330120034”, 
“contra_id”:”MBYY”, 
“sub_contra_id”:”ABCD”, 
“message_type”:”PA”, 
“tba_cusip”:” 01F0126A9”, 
“stl_date”:”20211014”, 
“pairoff _payment”:”5449.22”, 
“message_xref”:”MYXREF”, 
“message_id”:”202203300000001”, 
“pairoff _id”:”202203300000001”, 
“ack_ts”:”20220330124514” 
}PO_REQUEST_TRAILER 
PO AA – negative ack rejected due to incorrect contra 
 
PO_REQUEST_HEADER{ 
“submitter_id”:”MBXX”, 
“userclass”:” “, 
“submission_ts:”20220330120034”, 
“contra_id”:”MBYY”, 
“sub_contra_id”:”ABCD”, 
“message_type”:”PA”, 
“tba_cusip”:” 01F0126A9”, 
“stl_date”:”20211014”, 
“pairoff _payment”:”5449.22”, 

---

## Page 22

MBSD Pair-Off Service Enhancements Specifications  
 
Appendix A: Mess age Samples 22 
“message_xref”:”MYXREF”, 
“message_id”:”202203300000001”, 
“reason_code”:”0101”, 
“ack_ts”:”20220330124514” 
}PO_REQUEST_TRAILER 
 
PO request passed to Contra 
 
PO_REQUEST_HEADER { 
“submitter_id”:”MBXX”, 
“userclass”:” “, 
“submission_ts:”20220330120034”, 
“contra_id”:”MBYY”, 
“sub_contra_id”:”ABCD”, 
“message_type”:”PO”, 
“tba_cusip”:” 01F0126A9”, 
“stl_date”:”20211014”, 
“pairoff _payment”:”5449.22”, 
“message_xref”:”MYXREF”, 
“message_id”:”202203300000002”, 
“pairoff _id”:”202203300000001”, 
“pairoff _detail”:[ 
         { 
         “buy_sell”:”S”, 
         “trade_date”:”20211007”, 
          “price”:”96.84375”, 
          “pairoff _par”:”375000”, 
          “orig_trade_par”:”10000000”, 
          “trade_xref”:”TRADE1” 
       }, 
                     { 
         “buy_sell”:”B”, 
         “trade_date”:”20211012”, 
          “price”:”96.515625”, 
          “pairoff _par”:”675000”, 
          “orig_trade_par”:”2000000”, 

---

## Page 23

MBSD Pair-Off Service Enhancements Specifications  
 
Appendix A: Mess age Samples 23 
          “trade_xref”:”TRADE2” 
       }, 
                     { 
         “buy_sell”:”S”, 
         “trade_date”:”20210922”, 
          “price”:”97.921875”, 
          “pairoff _par”:”300000”, 
          “orig_trade_par”:”300000”, 
          “trade_xref”:”TRADE3” 
       } 
] 
}PO_REQUEST_TRAILER 
 
PO affirm submitted by contra 
 
PO_REQUEST_HEADER { 
“submitter_id”:”MBYY”, 
“userclass”:”XYZABC“, 
“submission_ts:”20220330120034”, 
“contra_id”:”MBXX”, 
“sub_contra_id”:”ABCD”, 
“message_type”:”PF”, 
“tba_cusip”:” 01F0126A9”, 
“stl_date”:”20211014”, 
“pairoff _payment”:”5449.22”, 
“message_xref”:”MYXREFAFFIRM”, 
“pairoff _id”:”202203300000001” 
} PO_REQUEST_TRAILER 
 
PO DK submitted by contra with unknown trade reason 
 
PO_REQUEST_HEADER { 
“submitter_id”:”MBYY”, 
“userclass”:”XYZABC“, 

---

## Page 24

MBSD Pair-Off Service Enhancements Specifications  
 
Appendix A: Mess age Samples 24 
“submission_ts:”20220330120034”, 
“contra_id”:”MBXX”, 
“sub_contra_id”:”ABCD”, 
“message_type”:”PD”, 
“tba_cusip”:”01F0126A9”, 
“stl_date”:”20211014”, 
“pairoff _payment”:”5449.22”, 
“message_xref”:”MYXREFDK”, 
“pairoff _id”:”202203300000001”, 
“reason_code”:”0102”, 
“comment”:”Unknown trade TRADE3” 
} PO_REQUEST_TRAILER 
 
PO Cancel submitted 
 
PO_REQUEST_HEADER { 
“submitter_id”:”MBXX”, 
“userclass”:”ABCDE“, 
“submission_ts:”20220330130034”, 
“contra_id”:”MBYY”, 
“sub_contra_id”:”ABCD”, 
“message_type”:”PC”, 
“tba_cusip”:”01F0126A9”, 
“stl_date”:”20211014”, 
“po_payment”:”5449.22”, 
“message_xref”:”MYXREFCAN”, 
“pairoff _id”:”202203300000001”, 
“comment”:”Need to restructure with new trades” 
} PO_REQUEST_TRAILER 

---

## Page 25

 
 
[[DTCC]] Internal (Green)  
 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 