---
title: "FAR to Asset Managers Record layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/FAR-to-Asset-Managers-Record-Layouts.pdf"
pages: 10
size: "427.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# FAR to Asset Managers Record layouts

**Original File:** [FAR-to-Asset-Managers-Record-Layouts.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/FAR-to-Asset-Managers-Record-Layouts.pdf)  
**Category:** Other  
**Total Pages:** 10  
**File Size:** 427.1 KB  

---

## Page 1

 
 [[DTCC]] Public (White) 
 
 
 
 
 
Financial Activity to [[Asset]] Managers (FAM) file layout  
(As of:  09/2020) 
 
 


---

## Page 2

 
2 
 
[[DTCC]] Public (White) 
Document Revision History 
 
Date Author Change Description 
05/01/2018 O Grudnikov Initial implementation 
08/10/2018 J Smith Updated with field definitions 
10/16/2018 O Grudnikov Added new record with source type 4303 (zip code) 
01/24/2019 J.Smith Updated with field definition 
05/17/2019 J Smith Added Fund Correlation Number field to the 43/05 and 43/06 record. 
09/2019 O Grudnikov September 2019 changes – Agent Record 
04/29/2020 J Smith Modified the Filler byte location on Record 4303 
09/17/2020 J Smith September 2020 changes – Agent Record.  NPN and/or CRD must be present to pass edit on inbound FAR file from 
the carrier.  
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 3

 
3 
 
[[DTCC]] Public (White) 
Contents 
(As of:  04/29/2020) ................................................................................................................................................................................................................................................................................................................1 
1.1 Contract record (C43-01) ..................................................................................................................................................................................................................................................................................................4 
1.2 Contract Entity Address record (C43-03) ..........................................................................................................................................................................................................................................................................6 
1.3 Agent record (C43-04) ......................................................................................................................................................................................................................................................................................................7 
1.4 Transaction record (C43-05) .............................................................................................................................................................................................................................................................................................9 
1.5 Fund record (C43-06) ..................................................................................................................................................................................................................................................................................................... 10 
 
 
 
 
 Files for ‘FAR to [[Asset]] Managers’ process 
 
This document describes the record formats for the flat files created from the Insurance Financial Activity Reporting product.  These files will be made available on a daily basis for sending to [[Asset]] Managers or 
solution providers on behalf of [[Asset]] Managers. 
                   
File layout definitions:           
1. Optional fields that are not used will contain spaces for Alphanumeric or Date fields and zeros /spaces for Numeric fields. 
2. “Filler” fields will contain spaces.          
3. Numeric decimal fields are decimal implicit.          
4. Alphanumeric fields are left justified. 
5. Numeric fields are right justified with leading zeros. 
 
 
Column headings are as follows:                 
• Start:   The position where the field starts         
• End:   The position where the field ends         
• Length:   The length of the field in bytes         
• Type:    A/N = Alphanumeric, N = Numeric, D = Date Format (YYYYMMDD)     
• Field Name:  The name of the field           
• Description:   Field Usage and Definition 
• Allowed Values:  Field description   
• Item Number:   [[DTCC]] assigned item number       
• Required Indicator: O = Optional, M = Mandatory  
 
        

---

## Page 4

 
 [[DTCC]] Public (White) 
1.1 Contract record (C43-01) 
Start End Length Type Field name Description Allowed Values Item# Required 
Indicator 
1 8 8 D Extract date Date the I&RS process runs the extract file for delivery CCYYMMDD  M 
9 11 3 A/N Business Event FAR FAR 5001 M 
12 15 4 A/N Sender Used to identify the Carrier transmitting the transmission.  
This is the [[NSCC]] [[Member]] number. 
Alphanumeric 5007 M 
16 45 30 A/N Transmission [[ID]] Transmission Unique [[ID]] from record C40 Submitters [[NSCC]] [[participant]] Number 
Data Submitted 
Time Submitted 
Hard Coded File 
5002 M 
46 53 8 D Transmission Date Date this file was transmitted. 
 
CCYYMMDD 5003 M 
54 63 10 A/N Associated Sender Carrier with which the business transaction has been 
conducted.  This could differ from the Settling Carrier due to 
state regulations. 
Alphanumeric 5009 O 
64 67 4 A/N Receiver Contra [[participant]] Number from record C42   
[[ID]] of the Receiving Company. 
5017 M 
68 77 10 A/N Associated Receiver Associated Firm I.D. A number established by the [[Broker]]/Dealer to 
sub divide their business 
5019 M 
78 107 30 A/N Contract Number Unique number used to Identify the contract. Alphanumeric 5021 M 
108 111 4 N Source Record type 4301 4301 N/A M 
112 150 39 A/N Filler  Spaces N/A M 
151 159 9 A/N [[CUSIP]] Number The annuity plan or product’s [[CUSIP]]  5025 M 
160 184 25 A/N Contract Status This is reporting current status of the contract as of the 
transaction Activity. 
See full FAR record layouts for available 
statuses available on the code list. 
5026 M 
185 192 8 D Contract Date - 1 Date(s) associated with the contract, e.g. effective, 
certificate, mailing, maturity issue 
CCYYMMDD 5027 M 
193 217 25 A/N Contract Date Qualifier -1 Qualifies the dates above.  For example, contract effective 
date, issue date, surrendered date, mailed date, maturity, 
etc. 
See full FAR record layouts for available 
contract dates available on the code list. 
5028 M 
218 225 8 D Contract Date - 2 Date(s) associated with the contract, e.g. effective, 
certificate, mailing, maturity issue 
CCYYMMDD 5027 O 
226 250 25 A/N Contract Date Qualifier -2 Qualifies the dates above.  For example, contract effective 
date, issue date, surrendered date, mailed date, maturity, 
etc. 
See full FAR record layouts for available 
contract dates available on the code list. 
5028 O 
251 258 8 D Contract Date - 3 Date(s) associated with the contract, e.g. effective, 
certificate, mailing, maturity issue 
CCYYMMDD 5027 O 
259 283 25 A/N Contract Date Qualifier -3 Qualifies the dates above.  For example, contract effective 
date, issue date, surrendered date, mailed date, maturity, 
etc. 
See full FAR record layouts for available 
contract dates available on the code list. 
5028 O 
284 291 8 D Contract Date - 4 Date(s) associated with the contract, e.g. effective, 
certificate, mailing, maturity issue 
CCYYMMDD 5027 O 

---

## Page 5

 
5 
 
[[DTCC]] Public (White) 
292 316 25 A/N Contract Date Qualifier -4 Qualifies the dates above.  For example, contract effective 
date, issue date, surrendered date, mailed date, maturity, 
etc. 
See full FAR record layouts for available 
contract dates available on the code list. 
5028 O 
317 324 8 D Contract Date - 5 Date(s) associated with the contract, e.g. effective, 
certificate, mailing, maturity issue 
CCYYMMDD 5027 O 
325 349 25 A/N Contract Date Qualifier -5 Qualifies the dates above.  For example, contract effective 
date, issue date, surrendered date, mailed date, maturity, 
etc. 
See full FAR record layouts for available 
contract dates available on the code list. 
5028 O 
350 374 25 A/N Product Type Code Code List See full FAR record layouts for available 
product type available on the code list. 
5139 O 
375 450 76 A/N Filler  Spaces Spaces for future use. N/A M 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 6

 
6 
 
[[DTCC]] Public (White) 
1.2 Contract Entity Address record (C43-03) 
Start End Length Type Field name Description Allowed Values Item# Required 
Indicator 
1 8 8 D Extract date Date the I&RS process runs the extract file for delivery CCYYMMDD  M 
9 11 3 A/N Business Event FAR FAR 5001 M 
12 15 4 A/N Sender Used to identify the Carrier transmitting the transmission.  This 
is the [[NSCC]] [[Member]] number. 
Alphanumeric 5007 M 
16 45 30 A/N Transmission [[ID]] Transmission Unique [[ID]] from record C40 Submitters [[NSCC]] [[participant]] Number 
Data Submitted 
Time Submitted 
Hard Coded File 
5002 M 
46 53 8 D Transmission Date Date this file was transmitted. 
 
CCYYMMDD 5003 M 
54 63 10 A/N Associated Sender Carrier with which the business transaction has been 
conducted.  This could differ from the Settling Carrier due to 
state regulations. 
Alphanumeric 5009 O 
64 67 4 A/N Receiver Contra [[participant]] Number from record C42   
[[ID]] of the Receiving Company. 
5017 M 
68 77 10 A/N Associated Receiver Associated Firm I.D. A number established by the [[Broker]]/Dealer to sub 
divide their business 
5019 M 
78 107 30 A/N Contract Number Unique number used to Identify the contract. Alphanumeric 5021 M 
108 111 4 N Source Record type 4303 4301 N/A M 
112 150 39 A/N Filler  Spaces N/A M 
151 165 15 A/N Entity Zip Code The zip code of the contract or policy owner. Alphanumeric 5044 O 
166 450 192 A/N Filler  Spaces Spaces for future use. N/A M 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 7

 
7 
 
[[DTCC]] Public (White) 
1.3 Agent record (C43-04) 
Start End Length Type Field name Description Allowed Values Item# Required 
Indicator 
1 8 8 D Extract date Date the I&RS process runs the extract file for delivery CCYYMMDD  M 
9 11 3 A/N Business Event FAR FAR 5001 M 
12 15 4 A/N Sender Used to identify the Carrier transmitting the 
transmission.  This is the [[NSCC]] [[Member]].  
Alphanumeric 5007 M 
16 45 30 A/N Transmission [[ID]] Transmission Unique [[ID]] from record C40 Submitters [[NSCC]] [[participant]] Number 
Data Submitted 
Time Submitted 
Hard Coded File 
5002 M 
46 53 8 D Transmission Date Date this file was transmitted. 
 
CCYYMMDD 5003 M 
54 63 10 A/N Associated Sender Carrier with which the business transaction has been 
conducted.  This could differ from the Settling Carrier 
due to state regulations. 
Alphanumeric 5009 O 
64 67 4 A/N Receiver Contra [[participant]] Number from record C42 [[ID]] of the Receiving Company. 5017 M 
68 77 10 A/N Associated Receiver Associated Firm I.D. A number established by the 
[[Broker]]/Dealer to sub divide their business 
5019 M 
78 107 30 A/N Contract Number Unique number used to Identify the contract. Alphanumeric 5021 M 
108 111 4 N Source Record type 4304 4304 N/A M 
112 150 39 A/N Filler  Spaces N/A M 
151 170 20 A/N 
Agent Tax I.D. 
Agent tax identifier Agent of record on annuity contract or 
insurance policy 
5046 O 
171 195 25 A/N Agent Tax I.D. 
Qualifier 
Code List See full FAR record layouts for available 
tax [[ID]] qualifiers available on the code list. 
5047 O 
196 300 105 A/N 
Agent Name  
Actual Non-Natural Name for Agent such as House 
Account.   Please see note* 
If agent is non-natural, this will be 
populated with Team Name.  When not 
used, filled with spaces 
5131 M 
301 325 25 A/N 
Agent Role 
Identifies the role that the reported agent is playing 
(e.g. servicing, writing, primary, etc.) 
See full FAR record layouts for available 
agent roles available on the code list. 
5119 M 
326 350 
25 
A/N 
Agent Type Code 
Identifies the type of agent that is being identified (e.g. 
person, non-person, partnership, etc.) 
See full FAR record layouts for available 
agent types available on the code list. 
5118 O 
351 370 
20 
A/N Distributor Assigned 
Agent [[ID]] 
The agent identifier established by the [[Broker]]/dealer or 
insurance agency 
alphanumeric 5124 O 
371 371 1 A/N Agent Natural/Non-
Natural  
Name Indicator 
Indicates if the reported is a natural person or non-
natural entity. 
N = Natural,  X = Non-Natural 5129 M 
372 381 
10 
A/N 
National Producer 
Number (NPN) 
A unique sequential number that identifies each entity 
in PDB, including individual producers and business 
producers. It is a 10-digit number without leading zeros. 
alphanumeric 5130 C*** 
382 391 
10 
N 
Rep/Advisor Split % 
Defines the percentage of the reported Rep/Advisor 
split. 
When used format is 9(01)v9(09)               5144 O 

---

## Page 8

 
8 
 
[[DTCC]] Public (White) 
392 401 10 A/N CRD Number [[FINRA]] Central Repository Depository (CRD) identifier 
used by US [[securities]] industry and its regulators 
Alphanumeric 5151 C*** 
402 421 10 A/N Carrier Assigned 
Agent [[ID]] 
This identifier is created and defined by the insurance 
carrier (provider) where the defined advisor/agent is 
appointed with. 
Alphanumeric 5152 O 
422 450 59 A/N Filler   spaces N/A M 
 
Note *:  When item #5129 = ‘X’, bytes 223-327 are the Agent Non-Natural Name, item #5131.  Otherwise it is distributed as follows: 
 
 
 
196 230 35 A/N Agent Last Name The last name of the person who is listed as the agent 
of record. 
alphanumeric 5048 O 
231 255 25 A/N Agent First Name The first name of the person who is listed as the agent 
of record. 
alphanumeric 5049 O 
256 280 25 A/N Agent Middle Name The middle name of the person who is listed as the 
agent of record. 
alphanumeric 5050 O 
281 290 10 A/N Agent Prefix Prefix alphanumeric 5051 O 
291 300 10 A/N Agent Suffix Suffix alphanumeric 5052 O 
 
Note:  **:  when not used, filled with spaces; when used – format is 9(01)v9(09) 
 
Note:  ***:  when Agent Record is present, NPN and/or CRD must be present.   Both may be sent but one must be present.   

---

## Page 9

 
9 
 
[[DTCC]] Public (White) 
1.4 Transaction record (C43-05) 
Start End Length Type Field name Description Allowed Values Item# Required 
Indicator 
1 8 8 D Extract date Date the I&RS process runs the extract file for 
delivery 
CCYYMMDD  M 
9 11 3 A/N Business Event FAR FAR 5001 M 
12 15 4 A/N Sender Used to identify the Carrier transmitting the 
transmission.  This is the [[NSCC]] [[Member]].  
Alphanumeric 5007 M 
16 45 30 A/N Transmission [[ID]] Transmission Unique [[ID]] from record C40 
 
 
 
Submitters [[NSCC]] [[participant]] Number 
Data Submitted 
Time Submitted 
Hard Coded File 
5002 M 
46 53 8 D Transmission Date Date this file was transmitted. 
 
CCYYMMDD 5003 M 
54 63 10 A/N Associated Sender Carrier with which the business transaction has 
been conducted.  This could differ from the Settling 
Carrier due to state regulations. 
Alphanumeric 5009 O 
64 67 4 A/N Receiver Contra [[participant]] Number from record C42 [[ID]] of the Receiving Company. 5017 M 
68 77 10 A/N Associated Receiver Associated Firm I.D. A number established by the [[Broker]]/Dealer 
to sub divide their business 
5019 M 
78 107 30 A/N Contract Number Unique number used to Identify the contract. Alphanumeric 5021 M 
108 111 4 N Source Record type 4305 4305 N/A M 
112 131 20 A/N Fund Correlation Number File Processing Date (CCYYMMDD + 12 zeros) 
starting with 1 each processing date.   
CCYYMMDD000000000000 N/A M 
132 150 19 A/N Filler  spaces N/A M 
151 166 16 N Transaction Amount Total transaction amount, may be zeros 9(14)v9(02) 5055 M 
167 167 1 A/N Transaction Amount 
Debit/Credit Indicator 
Identifies if the transaction is a debit or credit to the 
annuity contract or insurance policy. 
D = Debit, C = Credit 5055 M 
168 192 
25 
A/N 
Transaction Source 
Indicator 
Indicates who initiated the transaction (ex- Agent, 
Client).  See FAR standard usage for more detail 
on when this field is needed. 
See full FAR record layouts for available 
transaction sources available on the code 
list. 5127 O 
193 217 
25 
A/N 
Transaction Identifier 
Qualifies type of transaction                                             
i.e., loan repayment, dollar cost average 
See full FAR record layouts for available 
transaction identifiers available on the 
code list. 5057 M 
218 242 
25 A/N Payment Type 
Specifies the type of payment selected from the 
code list. 
See full FAR record layouts for available 
payment types available on the code list. 5140 O 
243 250 
8 D 
Transaction Date 
(Effective) Effective date or as of value date. CCYYMMDD 5060 M 
251 258 
8 D Transaction Date (Process) 
Process date – system process date – may be the 
same as the effective date. CCYYMMDD 5061 M 
259 450 192 A/N Filler   Spaces N/A M 
 
 

---

## Page 10

 
10 
 
[[DTCC]] Public (White) 
               1.5 Fund record (C43-06) 
Start End Length Type Field name Description Allowed Values Item# Required 
Indicator 
1 8 8 D Extract date Date the I&RS process runs the extract file for 
delivery 
CCYYMMDD  M 
9 11 3 A/N Business Event FAR FAR 5001 M 
12 15 4 A/N Sender Used to identify the Carrier transmitting the 
transmission.  This is the [[NSCC]] [[Member]].  
Alphanumeric 5007 M 
16 45 30 A/N Transmission [[ID]] Transmission Unique [[ID]] from record C40 
 
 
 
Submitters [[NSCC]] [[participant]] Number 
Data Submitted 
Time Submitted 
Hard Coded File 
5002 M 
46 53 8 D Transmission Date Date this file was transmitted. 
 
CCYYMMDD 5003 M 
54 63 10 A/N Associated Sender Carrier with which the business transaction has 
been conducted.  This could differ from the Settling 
Carrier due to state regulations. 
Alphanumeric 5009 O 
64 67 4 A/N Receiver Contra [[participant]] Number from record C42 [[ID]] of the Receiving Company. 5017 M 
68 77 10 A/N Associated Receiver Associated Firm I.D. A number established by the [[Broker]]/Dealer 
to sub divide their business 
5019 M 
78 107 30 A/N Contract Number Unique number used to Identify the contract. Alphanumeric 5021 M 
108 111 4 N Source Record type 4306 4306 N/A M 
112 131 20 A/N Fund Correlation Number File Processing Date (CCYYMMDD + 12 zeros) 
starting with 1 each processing date.   
CCYYMMDD000000000000 N/A M 
132 150 19 A/N Filler  Spaces N/A M 
151 169 
19 A/N Fund Identifier 
Identifies the fund ([[CUSIP]] number plus the internal 
insurance company fund number) 
9+5+5 ([[CUSIP]] + Fund [[ID]] + Sub Fund [[ID]]) 
alphanumeric 5064 M 
170 185 16 N Fund Amount The fund value in dollars 9(14)v9(02) 5066 O 
186 186 1 A/N Fund Amount Debit/Credit 
Indicator 
Identifies if the transaction is a debit or credit to the 
reported fund. 
D = Debit, C = Credit 5065 O 
187 201 15 N Fund Unit Price Price of a single fund unit 9(06)v9(09) 5072 O 
202 219 18 N Fund Units Number of units in the fund 9(12)v9(6) 5073 O 
220 220 1 A/N Fund Units Debit/Credit 
Indicator 
Identifies if the transaction is a debit or credit in 
units on the reported fund. 
D = Debit, C = Credit 5073 O 
221 229 9 A/N Mutual Fund [[CUSIP]] 
Number 
[[CUSIP]] number of the mutual fund that underlying 
security is tied to 
Alphanumeric 5126 O 
230 241 
12 A/N Fund Account number 
The account number of the fund held at the mutual 
fund company. 
Alphanumeric 
5145 O 
242 450 209 A/N Filler  Spaces  N/A M 
 
 