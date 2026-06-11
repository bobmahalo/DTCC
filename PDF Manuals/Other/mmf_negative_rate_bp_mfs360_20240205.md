---
title: "Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mmf_negative_rate_bp_mfs360_20240205.pdf"
pages: 14
size: "533.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices

**Original File:** [mmf_negative_rate_bp_mfs360_20240205.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mmf_negative_rate_bp_mfs360_20240205.pdf)  
**Category:** Other  
**Total Pages:** 14  
**File Size:** 533.1 KB  

---

## Page 1

 
 
 
Money Market Fund 
COMMUNICATING NEGATIVE RATE & SHARE 
CANCELLATION ACTIVITY FOR CNAV MONEY 
MARKET FUNDS: BEST PRACTICES 
FEBRUARY 5, 2024 
 

---

## Page 2

 
 
TABLE OF CONTENTS 
Change History ..................................................................................................................................................... 3 
Introduction .......................................................................................................................................................... 4 
Background and Objectives ................................................................................................................................ 4 
Scope .................................................................................................................................................................. 4 
Record Layouts ................................................................................................................................................... 4 
Best Practices ....................................................................................................................................................... 5 
MFPS I Price & Rate – Communicating a Rate .................................................................................................. 5 
Original Negative Rate ........................................................................................................................................ 6 
Correction to a Negative Rate (where corrected rate is ≤ 0) .............................................................................. 6 
Correction to a Negative Rate (where corrected rate is > 0) .............................................................................. 7 
Original Rate ....................................................................................................................................................... 8 
Correction to a Rate (where corrected rate is < 0) ............................................................................................. 8 
Correction to a Rate (where corrected rate is ≥ 0) ............................................................................................. 9 
MF Info Xchange – Communicating First Occurrence of a Negative Rate.......................................................10 
Networking F55 Activity Record – Communicating Share Cancellation Activity ..............................................12 
Appendix – Original Rate and Rate Correction Scenarios ............................................................................ 13 
 

---

## Page 3

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Change History 3 
CHANGE HISTORY 
Dates Revisions 
February 5, 2024 Document was rebranded.  
  

---

## Page 4

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Introduction 4 
INTRODUCTION 
Background and Objectives 
This guide and list of Best Practices was prepared by industry participants of the Investment Company Institute 
(ICI) Share Cancellation Working Group, formed in response to the Federal Reserve’s near -zero interest rate 
policies in spring, 2020. The working group’s focus was to identify requirements for the industry to 
systematically communicate a negative rate for a Constant NAV Money Market Fund (CNAV MMF). For those 
funds that choose to remain a CNAV MMF in a negative yield environment, the working group identified a need 
to uniquely identify Fund-generated share cancellation activity
1 related to a negative yield.  
The guidelines encompassed in this document provide “Best Practices” for the use of [[DTCC]]’s:  
• Mutual Fund Profile I – Price & Rate (MFPS I) and MF Info Xchange services when communicating a 
negative rate.  
• Networking F55 Activity record when communicating share cancellation activity related to a negative yield.  
Scope 
MFPS I Price & Rate – Implementation of enhancements to accommodate communication of a negative rate 2.  
MF Info Xchange – Best practices were established for a Fund to communicate the first occurrence of a 
negative rate. 
Networking Activity F55 Record: Best practices were established for a Fund to communicate s hare cancellation 
activity. 
Record Layouts 
Record Layouts referred to in this document can be found in the Record Layouts of the [[DTCC]] Learning Center 
under Record Layouts (password required). 
 
1 Money market funds that wish to retain a constant NAV while experiencing negative yield would need to reduce, or cancel, on a [[Pro-Rata]] basis, full and fractional 
[[shares]] equal to the negative yield. The reduction or cancellation of [[shares]] posted to shareholder accounts must be communicated between counterparties.    
2 See Important Notice a8917 dated October 19, 2020 for details.  

---

## Page 5

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Best Practices 5 
BEST PRACTICES 
MFPS I Price & Rate – Communicating a Rate 
The following Best Practices outline use of the MFPS I Price & Rate fields3 listed below when passing a rate, 
negative rate, or correction to a rate/negative rate.   
Field Name MFPS I Price & 
Rate File (030), 
Record # 
Position Type Values Reject Code4 
Rate Correcton 
Indicator 
2 8-8 (1 byte) A/N 1 = Original Rate 
2 = Correction to Rate 
Space = Rate not provided 
0084 – Correction 
Indicator missing/ 
invalid 
Rate 2 9-26  
(18 bytes) 
N 999,999,999.999999999 0086 – Rate missing/ 
invalid 
Negative Rate 
Correction 
Indicator 
2 51-51          
(1 byte) 
A/N 1 = Original Negative Rate 
2 = Correction to Negative  
Rate 
Space = Rate not provided 
0407 - Negative Rate 
Correction Indicator is 
missing/invalid 
Negative Rate 2 52-64       
(13 bytes) 
N 9,999.999999999 0408 - Negative Rate 
is missing/invalid 
 
The following table summarizes use of the rate correction indicator fields when communicating rates.  It is 
critically important these guidelines be followed to ensure intermediaries can understand the scenario 
taking place.  Examples of each scenario are outlined in the Best Practices.  
Rate 
Correction 
Indicator 
Negative Rate 
Correction 
Indicator 
Scenario 
1 blank Original rate (non-negative) is being communicated 
1 1 Original negative rate is being communicated 
2 1 Original rate (non-negative) is being corrected to a negative value 
2 blank Original rate (non-negative) is being corrected to either a positive value or 0 
2 2 Original negative rate is being corrected to a positive value  
blank 2 Original negative rate is being corrected to either a negative value or 0. 
 
3  Best Practices are effective 11/23/20 in conjunction with enhancements covered under Important Notice a8917 dated October 19, 2020. 
    The MFPS 1 Fixed Record layout fields/positions are referenced for illustration purposes.  
4 New reject codes were introduced for the Negative Rate Correction Indicator (0407) and Negative Rate (0408) fields.   Existing reject codes will be leveraged 
for the Rate Correction Indicator (0084) and Rate (0086) fields .  

---

## Page 6

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Best Practices 6 
Original Negative Rate  
 
When communicating an original negative rate, the ‘Negative Rate Correction Indicator’ field should be 
populated with a ‘1’ (Original Negative Rate), and the remaining rate fields should be populated as follows: 
• Rate Correction Indicator must be populated and should = 1 (Original Rate)  
• Rate must be populated and = 0  
• Negative Rate must be populated and > 0  
 
Example: Fund communicates an original negative rate of 0.12345 (scenario # 1 in Appendix). 
Field Name  Value 
Rate Correction Indicator  1  
Rate 000000000000000000 
Negative Rate Correction Indicator 1  
Negative Rate 0000123450000 
Important Notes: 
When the ‘Rate Correction Indicator’ and ‘Negative Rate Correction Indicator’ are both populated with a value of 1, 
it indicates an original negative rate is being passed. 
When the ‘Negative Rate Correction Indicator’ is populated with a value of 1 (Original Negative Rate), the ‘Rate’ 
field must = 0. 
 
Correction to a Negative Rate (where corrected rate is ≤ 0) 
When communicating a correction to an original negative rate (where the corrected value is ≤ 0), the 
‘Negative Rate Correction Indicator’ field should be populated with a ‘2’ (Correction to Negative Rate), and the 
remaining rate fields should be populated as follows: 
• Rate Correction Indicator should not be populated (blank)  
• Rate should not be populated (blank)  
• Negative Rate field must be populated (zeros allowed) 
 
Example: Fund communicated an original negative rate of 0.12345, and subsequently sends a 
corrected negative rate of 0.12346 (scenario # 2 in Appendix). 
Field Name  Value 
Rate Correction Indicator   
Rate  
Negative Rate Correction Indicator 2  
Negative Rate 0000123460000 
 

---

## Page 7

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Best Practices 7 
 
Example: Fund communicated a negative rate of 0.12345, and subsequently sends a corrected  rate of 0 
(scenario # 3 in Appendix). 
 
Field Name  Value 
Rate Correction Indicator   
Rate  
Negative Rate Correction Indicator 2  
Negative Rate 0000000000000 
 
Important Note: 
The ‘Rate Correction Indicator’ and ‘Rate’ fields should not be populated when a negative rate is being corrected 
to zero or another negative value. 
Correction to a Negative Rate (where corrected rate is > 0) 
When communicating a correction to an original negative rate (where the corrected rate is > 0), the ‘Negative 
Rate Correction Indicator’ field should be populated with a ‘2’ (Correction to Negative Rate), and the remaining 
rate fields should be populated as follows: 
• Rate Correction Indicator should = 2 (Correction to Rate) 
• Rate field must be populated, and value should be > 0  
• Negative Rate field must be populated, and value should be = 0  
 
Example: Fund communicated an original negative rate of 0.12345, and subsequently sends a 
corrected (positive) rate of 0.05 (scenario # 4 in Appendix). 
 
Field Name  Value 
Rate Correction Indicator  2 
Rate 000000000050000000 
Negative Rate Correction Indicator 2  
Negative Rate 0000000000000 
 
Important Notes: 
When the ‘Rate Correction Indicator’ and ‘Negative Rate Correction Indicator’ fields are both populated with a 
value of ‘2’, it indicates a negative rate is being corrected to a positive rate. 
 

---

## Page 8

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Best Practices 8 
Original Rate  
When communicating an original rate, the ‘Rate Correction Indicator’ should be populated with a ‘1 (Original 
Rate) and the remaining rate fields should be populated as follows:  
• Rate field must be populated and ≥ 0 
• Negative Rate Correction Indicator should not be populated (blank) 
• Negative Rate should not be populated (blank)   
 
Example: Fund communicates an original rate of 0.12345 (scenario # 5 in Appendix). 
 
Field Name  Value 
Rate Correction Indicator  1 
Rate 000000000123450000 
Negative Rate Correction Indicator  
Negative Rate  
 
Important Notes: 
When communicating an original (non-negative) rate, the ‘Negative Rate Correction Indicator’ and ‘Negative Rate’ fields 
should not be populated. 
When the ‘Rate Correction Indicator’ is populated with a value of 1 and the ‘Negative Rate Correction Indicator’ and 
‘Negative Rate’ fields are not populated (blank), it indicates an original rate (non-negative) rate is being communicated. 
Correction to a Rate (where corrected rate is < 0)  
When communicating a correction to an original rate (where the corrected value is < 0), the ‘Negative Rate 
Correction Indicator’ field should be populated with a ‘1’ (Original Negative Rate) and the remaining rate fields 
should be populated as follows: 
• Rate Correction must be populated and should = 2 (Correction to Rate) 
• Rate field must be = 0 
• Negative Rate field must be populated and > 0 
 
Example: Fund communicated an original rate of 0.12345, and subsequently corrects the rate  to 
negative 0.005 (scenario # 6 in Appendix). 
 
Field Name  Value 
Rate Correction Indicator  2 
Rate 000000000000000000 
Negative Rate Correction Indicator 1 
Negative Rate 00000005000000 
 

---

## Page 9

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Best Practices 9 
Important Note: 
When the ‘Rate Correction Indicator’ is populated with a value of 2 and ‘Negative Rate Correction Indicator’ is 
populated with a value of 1, it indicates an original (non-negative) rate is being corrected to a negative rate. 
Correction to a Rate (where corrected rate is ≥ 0) 
When communicating a correction to an original rate (where the corrected value is ≥ 0), the ‘Rate Correction 
Indicator’ field should be populated with a ‘2’ (Correction to Rate) and the remaining rate fields should be 
populated as follows: 
• Rate field must be populated and ≥ 0  
• Negative Rate Correction Indicator should not be populated (blank) 
• Negative Rate field should not be populated (blank) 
 
Example: Fund communicated an original rate of 0.12345, and subsequently corrects the rate to  
0.123456 (scenario # 7 in Appendix). 
 
Field Name Value 
Rate Correction Indicator  2 
Rate 000000000123456000 
Negative Rate Correction Indicator  
Negative Rate  
 
Example: Fund communicated an original rate of 0.12345, and subsequently corrects the rate to 0  
(scenario # 8 in Appendix). 
Field Name Value 
Rate Correction Indicator  2 
Rate 000000000000000000 
Negative Rate Correction Indicator  
Negative Rate  
  
Important Note:  
When communicating a correction to an original (non-negative) rate, where the corrected value is ≥ 0, the 
‘Negative Rate Correction Indicator’ and ‘Negative Rate’ fields should not be populated. 
 
 
 

---

## Page 10

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Best Practices 10 
MF Info Xchange – Communicating First Occurrence of a Negative Rate 
The following describes how to use [[DTCC]]’s MF Info Xchange solution to communicate the first occurrence of a 
negative yield for a CNAV Money Market Fund (CNAV MMF). 
The suggested verbiage could be used by any Fund when communicating the first occurrence of a negative 
yield for a CNAV MMF.  The appropriate verbiage could also be incorporated into email, fax, and other 
communication from the Fund to intermediaries prior to – or concurrent with – dissemination of the negative 
yield daily factor (rate). 
  
MFIX Step 1:  
1. Event Type = Issue Notification  
2. Event Status = Initial Notification5  
3. Effective Date = Today  
4. Effective Time = Close of Market  
5. Contact Name, Phone Number and Email = Party that should be contacted with questions about the 
negative yield  
 
 
 
MFIX Step 2:  
1. Issue Type = Other  
2. Issue Description = Negative Yield  
3. What is the level of impact for this issue = Specific to a Particular Fund  
4. Fill out the following:  
a. Fund Number  
b. Security Issue ID6  
 
5 This would be ‘update’ if the plan is to use MF  Info Xchange to communicate additional information, at a later time, about this notification (e.g., if the actual 
negative rates were being conveyed by MF Info Xchange). 
6 MF Info Xchange permits a lookup to Mutual Fund Profile to retrieve all funds that are part of a portfolio; each fund will be displayed indiv idually in the Fund 
List Grid. Such capability may be especially helpful, as the negative yield will apply to all share classes.  


---

## Page 11

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Best Practices 11 
c. Fund Name  
d. Ticker  
e. Share Class  
f. Effective Date = Today  
g. Anticipated Resolution Date and Time (blank)  
h. Comment @ Fund Level (see notation in # 5 below)  
 
5. If the Fund uses [[DTCC]]’s MFPS I Price/Rate service to communicate the negative rates, the following is 
recommended:  
a. Comment @ Fund Level (in the Fund List grid): Provide the negative yield for the Security in the 
Comment field.  If that is not available, leave blank.  
b. C omments box  (below the Fund List grid):  
 
 
 
 
 
 
 
 
 
 
 
 
6.  If the Fund does not use MFPS I Price/Rate service, the following is recommended:  
a. Comment @ Fund Level (in the Fund List grid): Provide the negative yield for the Security in the 
Comment field.  If that is not available, leave blank.  
b. C omments box  (below the Fund List grid):  
  
This fund will declare a negative yield for the listed CNAV MMFs. 
 
The negative yield daily rates are provided for each affected fund, above. [and/or] 
 
The negative yield daily rates will (also) be provided (by email, by fax, etc.) as soon as 
they are available. 
 This fund will declare a negative yield for the listed CNAV MMFs.  
 
The negative yield daily rates are provided for each affected fund, a bove, as well as 
through the [[DTCC]]’s MFPS I price/rate service, [or] 
 
The negative yield daily rates will be provided through the [[DTCC]]’s MFPS I price/rate 
service as soon as they are available.  

---

## Page 12

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Best Practices 12 
 
 
Networking F55 Activity Record – Communicating Share Cancellation Activity 
The following Best Practices outline the use of the Networking F55 Activity record to uniquely identify share 
cancellation activity related to a negative yield.  
Share Cancelation activity communicated by Funds related to a negative yield should be populated on the 
Networking F55 Activity file as follows:  
• Transaction Type: 21 (Share Adjustment)7  
• Description: Negative Yield Share Cancel 
 
The “Description” field is required when a Transaction Type 21 – Share Adjustment is used. 
Field Name  F55 Activity 
Record # 
Position Type Value 
Transaction Type   1 23-24 A/N 21 
Description 2 56-84 A/N Negative Yield Share Cancel 
  
Important Note: 
It is critically important the value entered in the “Description” field, a free-form field, is left-justified and uses the 
exact wording provided above (Negative Yield Share Cancel).  Intermediaries will use that information to 
distinguish share cancellation transactions from other share adjustments. 
 
7 The recommended practice is to utilize 21 – Share Adjustment for Share Cancellation activity as many intermediaries or service providers have varying degrees 
of automation tied to the other two potential Transaction Types  explored (07 – [[Dividend]] adjustment and 18 – [[Dividend]]-related transaction), both of which may 
affect [[Dividend]] (hence 1099-DIV) tax reporting.  


---

## Page 13

Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices 
Appendix – Original Rate and Rate Correction Scenarios 13 
APPENDIX – ORIGINAL RATE AND RATE CORRECTION 
SCENARIOS 
# Scenario Rate 
Correction 
Indicator 
Rate Negative Rate 
Correction 
Indicator 
Negative Rate 
1 Original Negative Rate 1 000000000.000000000 1 0000.123450000 
      
2 Original Negative Rate; 1 000000000.000000000 1 0000.123450000 
 
Corrected to Negative Rate blank blank 2 0000.123460000 
      
3 Original Negative Rate;  1 000000000.000000000 1 0000.123450000 
 
Corrected to Zero blank blank 2 0000.000000000 
 
  
    
4 Original Negative Rate;  1 000000000.000000000 1 0000.123450000 
 
Corrected to Positive Rate 2 000000000.050000000 2 0000.000000000 
      
5 Original Rate 1 000000000.123450000 Blank Blank 
      
6 Original Rate;  1 000000000.123450000 Blank Blank 
 Corrected to Negative Rate 2 000000000.000000000 1 0000.005000000 
      
7 Original Rate; 1 000000000.123450000 Blank Blank 
 
Corrected to Positive Rate 2 000000000.123460000 Blank Blank 
      
8 Original Rate;  1 000000000.123450000 Blank Blank 
 
Corrected to Zero 2 000000000.000000000 Blank Blank 
 
 
 
 

---

## Page 14

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: February 5, 2024 
Publication Code: MFS360 
Service: Money Market Fund 
Title: Communicating Negative Rate & Share Cancellation Activity for CNAV Money Market Funds: Best Practices  
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 