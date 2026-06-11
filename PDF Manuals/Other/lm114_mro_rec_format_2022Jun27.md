---
title: "DTCC Limit Monitoring MRO Record Format Specifications"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/lm114_mro_rec_format_2022Jun27.pdf"
pages: 16
size: "321.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# DTCC Limit Monitoring MRO Record Format Specifications

**Original File:** [lm114_mro_rec_format_2022Jun27.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/lm114_mro_rec_format_2022Jun27.pdf)  
**Category:** Other  
**Total Pages:** 16  
**File Size:** 321.2 KB  

---

## Page 1

 
 
[[DTCC]] LIMIT MONITORING 
MRO RECORD FORMAT SPECIFICATIONS 
DECEMBER 2, 2016 
 
 
 


---

## Page 2

MRO Record Format Specifications 
[[DTCC]] Limit Monitoring Reports 2 
[[DTCC]] LIMIT MONITORING REPORTS 
The following table shows the reports available through the [[DTCC]] Limit Monitoring application: 
Production File Numbers PSE File Numbers File Description 
[[DTCC]] Limit Monitoring - Risk Entity 
MRO File 02181079 
[[DTCC]] Limit Monitoring - Risk Entity 
MRO File 02981079 
Provides participants with the 
description, limits, and the end- of-day 
position for each of their risk entity. 
[[DTCC]] Limit Monitoring - Trade Array 
MRO File 02181080 
[[DTCC]] Limit Monitoring - Trade Array 
MRO File 02981080 
Provides participants with the trade 
arrays associated with each of their 
risk entity. 
[[DTCC]] Limit Monitoring - Alert History 
MRO File 02181081 
[[DTCC]] Limit Monitoring - Alert History 
MRO File 02981081 
Provides participants with all alerts 
generated for each of their risk 
entities. 
[[DTCC]] Limit Monitoring - Risk Entity 
Audit Trail MRO File 02181082 
[[DTCC]] Limit Monitoring - Risk Entity 
Audit Trail MRO File 02981082 
Provides participants with the history 
of changes to their risk entity limit 
value (net notional). 
[[DTCC]] Limit Monitoring - Risk Entity 
Definition Audit Trail MRO File 
02180109 
[[DTCC]] Limit Monitoring - Risk Entity 
Definition Audit Trail MRO File 
02980109 
Provides participants with the history 
of changes to their risk entity definition 
values, such as changes to the name 
or clearing [[Broker]] [[ID]]. 
[[DTCC]] Limit Monitoring - Trade Array 
Audit Trail MRO File 02181083 
[[DTCC]] Limit Monitoring - Trade Array 
Audit Trail MRO File 02981083 
Provides participants with the 
description, limits, and end of day 
position for each of their risk-entity 
definitions. 
[[DTCC]] Limit Monitoring - [[participant]] 
Position Rejects MRO File 02181084 
[[DTCC]] Limit Monitoring - [[participant]] 
Position Rejects MRO File 02981084 
Provides participants position rejects, 
such as invalid process date, invalid 
buy/sell indicator, invalid executing 
[[Broker]]. 
[[DTCC]] Limit Monitoring - Daily Net 
Notional MRO File 02182189 
[[DTCC]] Limit Monitoring - Risk Entity 
Daily Net Notional MRO File 
02982189 
Provide participants with information 
used to monitor the effectiveness of 
the current net notional limit amount 
as compared to trading volumes. 
[[DTCC]] Limit Monitoring - Unassigned 
Risk Entity Trade Side Count MRO 
File 02182189 
[[DTCC]] Limit Monitoring - Unassigned 
Risk Entity Trade Side Count MRO 
File 02982189 
MRO to provide participants with the 
number of trades that are not 
accounted for in user-defined risk 
entities and are applied to the 
unassigned risk entity. 
 

---

## Page 3

MRO Record Format Specifications 
Risk Entity MRO File 3 
RISK ENTITY MRO FILE 
The following tables describe the Risk Entity MRO file that provides clearing members with the description, 
limits, and end of day position for each of their risk entity definitions: 
[[DTCC]] Limit Monitoring - Risk Entity MRO File 
CDTS Product [[ID]]: 02181079 
Header Record 
Field Name Length Type Comments 
Process Date 8 Alpha Numeric Format = MMDDCCYY 
Filler 665 Alpha Numeric Value = Spaces 
 
The following table provides the detail record information for the Risk Entity MRO file: 
[[DTCC]] Limit Monitoring - Risk Entity MRO File 
CDTS Product [[ID]]: 02181079 
Detail Record 
Field Name Length Type Comments 
Risk Entity [[ID]] 9 Numeric [[ID]] of the risk entity. 
Risk Entity Name 100 Alpha Numeric Name of the risk entity. 
Entity Status Code 2 Alpha Numeric Values: 
A – Active 
PA – Pending Activation 
PD – Pending Delete 
Activation Date 8 Alpha Numeric Format = MMDDCCYY 
Termination Date 8 Alpha Numeric Format = MMDDCCYY 
Net Notional Amount 17 Numeric Format = 99999999999999999 with an assumed 
decimal point before the last two numbers. 
Adjusted Credit Contract 
Amount 
17 Numeric Format = 99999999999999999 with an assumed 
decimal point before the last two numbers. 
Adjusted Debit Contract 
Amount 
17 Numeric Format = 99999999999999999 with an assumed 
decimal point before the last two numbers. 
Monitored 1 Alpha Numeric Values: 
Y = Yes – The Risk Entity is being monitored 
N = No – The Risk Entity is not being monitored 
Filler 494 Alpha Numeric Value = spaces 

---

## Page 4

MRO Record Format Specifications 
Trade Array MRO File 4 
TRADE ARRAY MRO FILE 
The following tables describe the Trade Array MRO file that provides clearing members with the trade arrays 
associated with their risk entity definitions: 
[[DTCC]] Limit Monitoring – Trade Array MRO File 
CDTS Product [[ID]]: 02181080 
Header Record 
Field Name Length Type Comments 
Process Date 8 Alpha Numeric Format = MMDDCCYY 
Filler 304 Alpha Numeric Value = Spaces 
 
The following table provides the detail record information for the Trade Array MRO file: 
[[DTCC]] Limit Monitoring – Trade Array MRO File 
CDTS Product [[ID]]: 02181080 
Detail Record 
Field Name Length Type Comments 
Risk Entity [[ID]] 9 Numeric [[ID]] of the risk entity. 
Trade Array Sequence 4 Numeric Format = 9999 
Clearing [[Broker]] [[ID]] 8 Alpha Numeric Format = 99999999 
Executing [[Broker]] [[ID]] 8 Alpha Numeric [[ID]] of [[Broker]] who executed the trade. 
Array Status Code 2 Alpha Numeric Values: 
A – Active 
PA – Pending Activation 
PD – Pending Delete 
Activation Date 8 Alpha Numeric Format = MMDDCCYY 
Termination Date 8 Alpha Numeric Format = MMDDCCYY 
Submitting Firm [[ID]] (9a) 8 Alpha Numeric If populated, format = 999999999 
If not populated, format = spaces 
Submitting Market [[ID]] 3 Alpha Numeric Format = 999 
UTC Account [[ID]] 32 Alpha Numeric Account identifier provided on trade to which the side 
belongs. 
Counterparty Firm (9b) 8 Alpha Numeric If populated, format = 999999999  
If not populated, format = spaces 
Filler 214 Alpha Numeric Value = spaces 
 

---

## Page 5

MRO Record Format Specifications 
Alert History MRO File 5 
ALERT HISTORY MRO FILE 
The following tables describe the Alert History MRO file that provides clearing members with any alerts 
generated for their risk entity definitions: 
[[DTCC]] Limit Monitoring – Alert History MRO File 
CDTS Product [[ID]]: 02181081 
Header Record 
Field Name Length Type Comments 
Process Date 8 Alpha Numeric Format = MMDDCCYY 
Filler 542 Alpha Numeric Value = Spaces 
 
The following table provides the detail record information for the Alert History MRO file: 
[[DTCC]] Limit Monitoring – Alert History MRO File 
CDTS Product [[ID]]: 02181081 
Detail Record 
Field Name Length Type Comments 
Risk Entity [[ID]] 9 Numeric [[ID]] of the risk entity. 
Limit Identifier 2 Alpha Numeric Valid Values: 
BQ - Buy Quantity 
SQ - Sell Quantity 
CR - Credit Amount 
DB - Debit Amount 
AC - Adjusted Credit Amount 
NC - Net Credit Amount 
ND - Net Debit Amount 
AD - Adjusted Debit Amount 
NN – Net Notional Amount 
Alert Level Code 1 Alpha Numeric Valid Values: 
1 – Level 1 Alert 
2 – Level 2 Alert 
3 – Level 3 Alert 
Alert Time 6 Alpha Numeric Format = HHMMSS. 
Alert Amount 17 Numeric Format = 99999999999999999 with an assumed decimal 
point before the last two numbers. 
Alert Time End 6 Alpha Numeric Format = HHMMSS. 
Ending Alert Amount 17 Numeric Format = 99999999999999999 with an assumed decimal 
point before the last two numbers. 
Filler 492 Alpha Numeric Value = spaces 

---

## Page 6

MRO Record Format Specifications 
Risk Entity Limit Audit Trail MRO File 6 
RISK ENTITY LIMIT AUDIT TRAIL MRO FILE 
The following tables describe the Risk Entity Limit Audit Trail MRO file that provides clearing members with the 
history changes to risk entity values: 
[[DTCC]] Limit Monitoring - Risk Entity Audit Trail MRO File 
CDTS Product [[ID]]: 02181082 
Header Record 
Field Name Length Type Comments 
Process Date 8 Alpha Numeric Format = MMDDCCYY 
Filler 1152 Alpha Numeric Value = Spaces 
 
The following table provides the detail record information for the Risk Entity Limit Audit Trail MRO file: 
[[DTCC]] Limit Monitoring - Risk Entity Audit Trail MRO File 
CDTS Product [[ID]]: 02181082 
Detail Record 
Field Name Length Type Comments 
Audit Action Code 4 Alpha Numeric Valid Values: 
A001 - Add Risk Entity 
U001 - Update Risk Entity 
D001 - Delete Risk Entity 
User [[ID]] 100 Alpha Numeric User [[ID]] of the user who made the update. 
Entry Time 6 Alpha Numeric Format = HHMMSS 
Risk Entity [[ID]] 9 Numeric [[ID]] of the risk entity. 
Risk Entity Before Image 
Original Clearing [[Broker]] [[ID]] 8 Alpha Numeric Format = 99999999 
Original Net Notional Amount 15 Numeric Format = 999999999999999 
Monitored 1 Alpha Numeric Values: 
Y = Yes – The Risk Entity is being monitored 
N = No – The Risk Entity is not being monitored 
Filler 29 Alpha Numeric Value = spaces 
 
Risk Entity After Image 
Updated Clearing [[Broker]] [[ID]] 8 Alpha Numeric Format = 99999999 
Updated Net Notional Amount 15 Numeric Format = 999999999999999 
Monitored 1 Alpha Numeric Values: 

---

## Page 7

MRO Record Format Specifications 
Risk Entity Limit Audit Trail MRO File 7 
[[DTCC]] Limit Monitoring - Risk Entity Audit Trail MRO File 
CDTS Product [[ID]]: 02181082 
Detail Record 
Field Name Length Type Comments 
Y = Yes – The Risk Entity is being monitored 
N = No – The Risk Entity is not being monitored 
Filler 964 Alpha Numeric Value = spaces 
 

---

## Page 8

MRO Record Format Specifications 
Risk Entity Definition Audit Trail MRO File 8 
RISK ENTITY DEFINITION AUDIT TRAIL MRO FILE 
The following tables describe the Risk Entity Definition Audit Trail MRO file that provides clearing members 
with the history changes to risk entity values: 
[[DTCC]] Limit Monitoring - Risk Entity Definition Audit Trail MRO File 
CDTS Product [[ID]]: 02180109 
Header Record 
Field Name Length Type Comments 
Process Date 8 Alpha Numeric Format = MMDDCCYY 
Filler 1152 Alpha Numeric Value = Spaces 
 
The following table provides the detail record information for the Risk Entity Definition Audit Trail MRO file: 
[[DTCC]] Limit Monitoring - Risk Entity Definition Audit Trail MRO File 
CDTS Product [[ID]]: 02180109 
Detail Record 
Field Name Length Type Comments 
Audit Action Code 4 Alpha Numeric Valid Values: 
A001 - Add Risk Entity 
U001 - Update Risk Entity 
D001 - Delete Risk Entity 
User [[ID]] 100 Alpha Numeric User [[ID]] of the user who made the update. 
Entry Time 6 Alpha Numeric Format = HHMMSS 
Risk Entity [[ID]] 9 Numeric [[ID]] of the risk entity. 
Risk Entity Name 100 Numeric Name of the risk entity. 
Risk Entity Before Image 
Original Clearing [[Broker]] [[ID]] 8 Alpha Numeric Format = 99999999 
Original Risk Entity Name 100 Alpha Numeric Name of the risk entity prior to the image. 
Risk Entity After Image 
Updated Clearing [[Broker]] [[ID]] 8 Alpha Numeric Format = 99999999 
Updated Risk Entity Name 100 Alpha Numeric Name of the risk entity after the image. 
Filler 725 Alpha Numeric Value = spaces 

---

## Page 9

MRO Record Format Specifications 
Trade Array Audit Trail MRO File 9 
TRADE ARRAY AUDIT TRAIL MRO FILE 
The following tables describe the Trade Array Audit Trail MRO file that provides clearing members with the 
description, limits, and end of day position for each of their risk entity definitions: 
[[DTCC]] Limit Monitoring – Trade Array Audit Trail MRO File 
CDTS Product [[ID]]: 02181083 
Header Record 
Field Name Length Type Comments 
Process Date 8 Alpha Numeric Format = MMDDCCYY 
Filler 592 Alpha Numeric Value = Spaces 
 
The following table provides the detail record information for the Risk Entity Limit Audit Trail MRO file: 
[[DTCC]] Limit Monitoring – Trade Array Audit Trail MRO File 
CDTS Product [[ID]]: 02181083 
Detail Record 
Field Name Length Type Comments 
Audit Action Code 4 Alpha Numeric Valid Values: 
A001 - Add Trade Array 
U001 - Update Trade Array 
D001 - Delete Trade Array 
User [[ID]] 100 Alpha Numeric User [[ID]] of the user who made the update. 
Entry Time 6 Alpha Numeric Format = HHMMSS 
Risk Entity [[ID]] 9 Numeric [[ID]] of the Risk Entity. 
Trade Array Before Image 
Original Clearing [[Broker]] [[ID]] 8 Alpha Numeric Format = 99999999 
Original Executing [[Broker]] [[ID]] 8 Alpha Numeric Original [[ID]] of [[Broker]] who executed the trade. 
Original Submitting Firm (9a) [[ID]] 8 Alpha Numeric If populated, format = 99999999 
If not populated, format = spaces 
Original Submitting Market [[ID]] 3 Alpha Numeric Format = 999 
Original UTC Account [[ID]] 32 Alpha Numeric Account identifier provided on trade to which 
the side belongs (before). 
Original Counterparty Firm (9b) [[ID]] 8 Alpha Numeric If populated, format = 99999999 If not 
populated, format = spaces. 
Filler 168 Alpha Numeric Value = spaces 
Trade Array After Image 

---

## Page 10

MRO Record Format Specifications 
Trade Array Audit Trail MRO File 10 
[[DTCC]] Limit Monitoring – Trade Array Audit Trail MRO File 
CDTS Product [[ID]]: 02181083 
Detail Record 
Field Name Length Type Comments 
Updated Clearing [[Broker]] [[ID]] 8 Alpha Numeric Format = 99999999 
Updated Executing [[Broker]] 
[[ID]] 
8 Alpha Numeric Updated [[ID]] of [[Broker]] who executed the 
trade. 
Updated Submitting Firm [[ID]] 8 Alpha Numeric If populated, format = 99999999 
If not populated, format = spaces 
Updated Submitting Market [[ID]] 3 Alpha Numeric Format = 999 
Updated UTC Account [[ID]] 32 Alpha Numeric Account identifier provided on trade to 
which the side belongs (after). 
Original Counterparty Firm (9b) [[ID]] 8 Alpha Numeric If populated, format = 99999999   
If not populated, format = spaces. 
Filler 179 Alpha Numeric Value = spaces 
 

---

## Page 11

MRO Record Format Specifications 
[[participant]] Position Rejects MRO File 11 
[[participant]] POSITION REJECTS MRO FILE 
The following tables describe the header information for the [[participant]] Position Rejects MRO file: 
[[DTCC]] Limit Monitoring - [[participant]] Position Rejects MRO File 
CDTS Product [[ID]]: 02181084 
Header Record 
Field Name Length Type Comments 
Process Date 8 Alpha Numeric Format = MMDDCCYY 
Filler 296 Alpha Numeric Value = Spaces 
 
The following table provides the detail record information for the [[participant]] Position Rejects MRO file: 
[[DTCC]] Limit Monitoring - [[participant]] Position Rejects MRO File 
CDTS Product [[ID]]: 02181084 
Detail Record 
Field Name Length Type Comments 
Process Date 8 Alpha Numeric Format = MMDDCCYY 
Buy/Sell Indicator 1 Alpha Numeric Valid Values: 
B 
S 
Clearing [[Broker]] [[ID]] 8 Alpha Numeric Format = 99999999 
Executing [[Broker]] [[ID]] 8 Alpha Numeric Account identifier provided on trade to 
which the side belongs. 
Submitting Market [[ID]] 3 Alpha Numeric Format = 999 
Submitting Firm [[ID]] 8 Alpha Numeric If populated, format = 99999999 
If not populated, format = spaces 
Counterparty Firm (9b) 8 Alpha Numeric If populated, format = 99999999 
If not populated, format = spaces 
UTC Account [[ID]] 32 Alpha Numeric Account identifier provided on trade to 
which the side belongs. 
Security ISIN 12 Alpha Numeric 9 or 12 characters 
Trade Quantity 15 Numeric Format = 999999999999999 
Contract Amount 17 Numeric Format = 99999999999999999 with an 
assumed decimal point before the last 
two numbers. 

---

## Page 12

MRO Record Format Specifications 
[[participant]] Position Rejects MRO File 12 
[[DTCC]] Limit Monitoring - [[participant]] Position Rejects MRO File 
CDTS Product [[ID]]: 02181084 
Detail Record 
Field Name Length Type Comments 
Action Code 4 Alpha Numeric Values: 
INCR = Increase  
DECR = Decrease 
Error Code 2 Alpha Numeric Values: 
01 – Invalid Process Date 
02 – Invalid Buy/Sell Indicator 
03 – Invalid Clearing [[Broker]]  
04 – Invalid Executing [[Broker]] 
05 – Invalid Submitting Market 
06 – Invalid Submitting Firm (9a) 07 – Invalid UTC 
account 
08 – Invalid Security ISIN 
09 – Invalid Trade Quantity  
10 – Invalid Contract Amount 
11 – Share Quantity and Contract 
Amount Cannot both be zeros  
12 – Invalid Action Code 
13 – Submitting Market not on database 14 – Submitting 
Firm is valid with Submitting Markets [[OTC]] or CORR 
only  
15 – Invalid check digit for the Security [[ID]] 
16 – Trade Quantity exceeds 15 digits 
17 – Trade Amount exceeds 17 digits  
18 – Quantity or Contract Amount Exceeds Existing 
Position 
19 – Position to be updated / deleted does not exist in 
database 
20 – Counterparty Firm (9b) valid with Submitting 
Markets [[OTC]] or CORR only 21 – Invalid Counterparty 
(9b) 
22 – Submitting Firm (9a) not an active Clearing [[Broker]] 
23 – Counterparty Firm (9b) not an active Clearing 
[[Broker]] 
Error Message 100 Alpha Numeric Description of error message. 
Filler 78 Alpha Numeric Value = Spaces 

---

## Page 13

MRO Record Format Specifications 
Risk Entity Daily Net Notional MRO File 13 
RISK ENTITY DAILY NET NOTIONAL MRO FILE 
The following tables describe the header information for the Risk Entity Daily Net Notional MRO file: 
[[DTCC]] Limit Monitoring - Risk Entity Daily Net Notional MRO File 
CDTS Product [[ID]]: 02182189 
Header Record 
Field Name Length Type Comments 
Process Date 8 Alpha Numeric Format = MMDDCCYY 
Filler 392 Alpha Numeric Value = Spaces 
 
The following table provides the detail record information for the Risk Entity Limit Daily Net Notional MRO file: 
[[DTCC]] Limit Monitoring - Risk Entity Daily Net Notional MRO File 
CDTS Product [[ID]]: 02182189 
Detail Record 
Field Name Length Type Comments 
Risk Entity [[ID]] 9 Numeric [[ID]] of the risk entity. 
Risk Entity Name 50 Alpha 
Numeric 
Name of the risk entity. 
SOM Limit 15 Numeric Net notional limit as of first day of the current month. 
[[EOD]] Limit 15 Numeric Net notional limit at the end of the current day. 
[[EOD]] Net Notional High 17 Numeric Net Notional High for the current day Format is 
99999999999999999 
Two decimal places from the right of the 
amount is implied. For example, 999999999999999.99 
Month to Date Daily Net 
Notional High 
17 Numeric The highest of all day’s End of Day Net Notional Amount 
High from the beginning of the current month, including 
the current day. If the current day’s End of Day Limit is 
greater than the Month to Date Net Notional High 
Amounts, then this value will also be End of Day Net 
Notional Amount. 
Format is 99999999999999999 
Two decimal places from the right of the amount is 
implied. For example, 999999999999999.99 
Month to Date Peak Date 8 Date The date of the highest of all day’s End of Day Net 
Notional Amount High from the beginning of the current 
month, including the current day. 
Format: MMDDCCYY 

---

## Page 14

MRO Record Format Specifications 
Risk Entity Daily Net Notional MRO File 14 
Month to Date Limit Breaches 9 Numeric Count of the number of Level 4 limit breaches that hav e 
occurred since the beginning of the current month, 
including the current day. 
Month to Date Limit 
Adjustments 
9 Numeric Count of the number of times the Net Notional Limit 
Amount was modified since the beginning of the current 
month, including the current day. 
Risk Entity Effective Date 8 Date Date the Risk Entity became effective Format: 
MMDDCCYY 
Monitored? 1 Alpha Status of the [[DO]] Not Monitor Indicator. Values are: 
Y = Yes – The Risk Entity is being monitored 
N = No – The Risk Entity is not being monitored 
Month to Date Average Net 
Notional High 
22 Numeric The Average of all current month’s Month to Date Daily 
Net Notional High Amounts. 
Format is 99999999999999999 
Two decimal places from the right of the amount is 
implied. For example, 999999999999999.99 
Filler 220 Alpha 
Numeric 
 

---

## Page 15

MRO Record Format Specifications 
Unassigned Risk Entity Trade Side Count MRO File 15 
UNASSIGNED RISK ENTITY TRADE SIDE COUNT MRO 
FILE 
The following table describes the header information for the Unassigned Risk Entity Trade Side Count MRO 
file: 
[[DTCC]] Limit Monitoring – Unassigned Risk Entity Trade Side Count MRO File 
CDTS Product [[ID]]: 02182190 
Header Record 
Field Name Length Type Comments 
Process Date 8 Alpha Numeric Format = MMDDCCYY 
Filler 392 Alpha Numeric Value = Spaces 
 
The following table provides the detail record information for the Unassigned Risk Entity Trade Side Count 
MRO file: 
[[DTCC]] Limit Monitoring – Unassigned Risk Entity Trade Side Count MRO File 
CDTS Product [[ID]]: 02182190 
Detail Record 
Field Name Length Type Comments 
Risk Entity [[ID]] 9 Numeric [[ID]] of the risk entity. 
Net Notional Limit 15 Numeric Net Notional Limit of the Risk Entity. 
Net Notional High 18 Numeric Net Notional High for the day 
Format = 999999999999999999 with an assumed 
decimal point before the last two numbers. 
Executing [[Broker]] 8 Alpha 
Numeric 
[[ID]] of [[Broker]] who executed the trade. 
Count of Trade Sides 9 Numeric Number of trade sides for the executing [[Broker]]. 
Filler 341   
 
 

---

## Page 16

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: June 27, 2022  
Publication Code: LM114 
Service: [[DTCC]] Limit Monitoring 
Title: MRO Record Format Specifications 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 