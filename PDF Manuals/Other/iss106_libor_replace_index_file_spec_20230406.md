---
title: "LIBOR Replacement Index File Specification Guide: Autoroute ID 05983676 (PSE); ID 05213676 (PROD)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/iss106_libor_replace_index_file_spec_20230406.pdf"
pages: 18
size: "340.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# LIBOR Replacement Index File Specification Guide: Autoroute ID 05983676 (PSE); ID 05213676 (PROD)

**Original File:** [iss106_libor_replace_index_file_spec_20230406.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/iss106_libor_replace_index_file_spec_20230406.pdf)  
**Category:** Other  
**Total Pages:** 18  
**File Size:** 340.7 KB  

---

## Page 1

 
 
 
[[issuer]] SERVICES  
LIBOR REPLACEMENT INDEX FILE SPECIFICATION GUIDE: AUTOROUTE [[ID]] 
05983676 (PSE); [[ID]] 05213676 (PROD)  
APRIL 6, 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the [[DTCC]] brand name by certain affiliates of The Depository Trust & 
Clearing Corporation ([[DTCC]]).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: April 6, 2023 
Publication Code: ISS 106 
Service: [[issuer]] Service 
Title: LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (PROD)

---

## Page 3

 
 
TABLE OF CONTENTS 
The LIBOR Replacement Index File.................................................................................................................... 4 
Header Record Layout: AutoRoute Header Record for ARR and Term SOFR  .............................................. 5 
Autoroute Header Record – 8-Digit Date Format ............................................................................................... 5 
Term SOFR and ARR Record Details ................................................................................................................. 7 
Term SOFR File Details ...................................................................................................................................... 7 
ARR (Alternative Reference Rate) File Details .................................................................................................10 
ARR and Term SOFR Data Dictionaries ........................................................................................................... 17 
ARR Data Dictionary .........................................................................................................................................17 
Term SOFR Data Dictionary .............................................................................................................................17 
 

---

## Page 4

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
The LIBOR Replacement Index File 4 
 
THE LIBOR REPLACEMENT INDEX FILE 
The London Inter-Bank Offered Rate index will be retired in June 2023. [[securities]] that are currently using 
LIBOR (USD) to calculate their interest rates will need to choose and communicate a replacement rate to the 
[[investor]] community ahead of the retirement date. 
By centralizing the communication of the replacement for LIBOR; issuers, their associated trustees, agents,  
and the [[investor]] community alike can use the new [[DTCC]] process to be prepared well in advance of the LIBOR  
retirement rate. 
To facilitate this communication, [[DTCC]] has created the LIBOR Replacement Index Communication Tool 
(Communication Tool) that will allow issuers, trustees and agent to: 
• Provide contact information for Information Submitters and Information Sources  
• Provide benchmark replacement details for multiple CUSIPs through .CSV or Excel upload  
The new process will allow for the fielding of descriptive reference data for efficient, machine- to-machine 
communication instead of assigning individuals or teams to review large, complex legal documents to 
determine these details. 
This file will be available for intraday pickup Monday – Friday at 8:00 AM ET, 3:00 PM ET and 8:00 PM ET.  
Each file slice will include submissions added after each slice run time. For example, data submitted through 
the LIBOR Replacement Index Communication Tool after 8:00 AM will be on the 3:00 PM file. In addition to the 
data received after 3:00 PM the 8:00 PM file will contain the entire day’s submissions (from 8:00 AM to 8:00 
PM). Data submitted through the Communication Tool after 8:00 PM on Friday, will be available on the 8:00 
AM file on Monday. 

---

## Page 5

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Header Record Layout: AutoRoute Header Record for ARR and Term SOFR 5 
 
HEADER RECORD LAYOUT: AUTOROUTE HEADER 
RECORD FOR ARR AND TERM SOFR  
ARR and Term SOFR AutoRoute product # 05213676 has an 8-byte header date format. 
Note 
AutoRoute files [[DO]] not have trailers. 
Autoroute Header Record – 8-Digit Date Format 
Field Name Length Start End Type  Comments 
Header [[ID]] 6 1 6 A/N Always = 1 TRANS 
Application Date 8 7 14 NUM CCKYYMMDD 
Reserved 2 15 16  [[DO]] not use 
Product Number 3 17 19 NUM  
Product 
Description 
20 20 39 A/N Alpha Product Description 
Reserved 3 40 42  [[DO]] not use 
Reserved 1 43 43  [[DO]] not use 
Multi-Cycle 
Transmission 
Counter 
2 44 45 A/N 01-99 Logical multi-cycle count of the job 
sent, or Spaces = Not multi-cycle 
Poss Dupe 
Indicator  
1 46 46 A/N Space = original transmission 
1 = Poss Dupe from [[DTCC]] 
Product [[ID]] 8 47 54 NUM 8-digit code issued by [[DTCC]] to identify the 
report or file 
Application's 
Multi- Cycle 
Counter  
 
2 55 56 NUM 1, 2,...,97 = Applications which provide more 
than one output per day have a sequential 
number for each output.  
Final output cycle number for a day = 98 
Spaces = Not multi-cycle 
Recipient [[ID]] 7 57 63 A/N This code is assigned to the destination of 
this transmission. It normally begins with the 
four-digit [[Broker]] [[ID]] number. 
Constant 
 
1 64 64 NUM Always = 0 (zeros) 
(Contains other values for [[DTCC]] internal 
distribution) 

---

## Page 6

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Header Record Layout: AutoRoute Header Record for ARR and Term SOFR 6 
 
Field Name Length Start End Type  Comments 
Record Count 9 65 73 NUM Number of data records or print lines that 
follow 
Sender [[ID]] 4 74 77 A/N Always = [[DTCC]] 
Constant 3 78 80 A/N Always = CDT 
Last field of 80-byte RJE header 
Reserved 1 81 81  [[DO]] not use 
Date Created 8 82 89 A/N MMDDCCYY 
Reserved 3 90 92  [[DO]] not use 
Time Created 5 93 97 A/N HH:MM 
Reserved 4 98 101  [[DO]] not use 
Constant 3 102 104 A/N Always = RDT 
Reserved 1 105 105  [[DO]] not use 
Date released 8 106 113 A/N MMDDCCYY 
File transmission date 
Reserved 3 114 116  [[DO]] not use 
Time released 5 117 121 A/N HH:MM  
File transmission time 
Reserved 12 122 133  [[DO]] not use 
Filler N 133 N  [[DO]] not use -- padding to match file record size 
END OF RECORD 
 

---

## Page 7

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Term SOFR and ARR Record Details 7 
 
TERM SOFR AND ARR RECORD DETAILS 
The layout below describes the Term SOFR rate type. The SOFR rate is the Secured Overnight Financing 
Rate produced by the [[U.S. Federal Reserve System]]. The indices described here are term or one month or 
greater.  
Term SOFR File Details  
Term SOFR File Details 
Position Length Format Field Name Field Description Valid Values 
1 4  Character Rate type Either Alternative Reference 
Rate (ARR) or Secured 
Overnight Financing Rate 
(SOFR) 
 
5 9 Character [[CUSIP]] A [[CUSIP]] is a security identifier 
and is composed of nine 
characters and can include 
letters and numbers  
Nine-digit alphanumeric 
security [[ID]] 
 
14 1 Character [[CUSIP]] on [[DTC]] 
Masterfile 
[[CUSIP]] is present on the [[DTCC]] 
Master Table 
Y or N 
• Y = Yes 
• N = No 
 
15 1 Character Replacement 
Choice Made 
Field that describes to the 
market whether the issue has 
chosen a LIBOR replacement.  
If set to Yes, a replacement has 
been made.  If set to No, it can 
be determined that a choice has 
not yet been made and that 
another record will be submitted 
once a replacement index has 
been decided upon.   
Y or N 
• Y = Yes 
• N = No 
 
16 1 Character Updated 
Submission 
To indicate if previously input 
data being updated with this 
record 
 
Y or N 
• Y = Yes 
• N = No 
 
17 70 Character Submitter 
Company 
The firm or organization, whose 
personnel are inputting a 
replacement rate change into 
the LIBOR Replacement Index 
Communication Tool.  
Enter a Company Name 

---

## Page 8

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Term SOFR and ARR Record Details 8 
 
Term SOFR File Details 
87 20 Character Submitter 
Entity Type 
The type of service that the firm 
is performing on behalf of or as 
the [[issuer]] of this security. 
• Paying Agent  
• [[transfer agent]] 
• Calculation Agent  
• Determining Person  
• [[issuer]]  
• Trustee  
• Other 
107 140 Character Submitter 
Contact Email 
The email address of the 
contact at the firm or 
organization inputting a 
replacement rate change into 
the LIBOR Replacement Index 
Communication Tool. 
Enter an e-mail address 
247 1 Character Information 
Source 
Indicator 
If the Information Source is 
different from the Submitter 
Y or N 
• Y = Yes 
• N = No 
 
248 70 Character Information 
Source / 
Provider 
Company 
Name 
The firm or organization that 
was responsible for the 
selection of replacement index  
Enter a Company Name 
318 20 Character Information 
Source / 
Provider Entity 
Type 
The type of service that the firm 
who selected the replacement 
index performs on behalf of the 
security 
• Paying Agent  
• [[transfer agent]]  
• Calculation Agent  
• Determining Person 
• [[issuer]]  
• Trustee  
• Other 
338 140 Character Information 
Source / 
Provider 
Contact email 
The email address of the 
contact at the firm or 
organization responsible for 
selecting the replacement index  
 
Enter an e-mail address 
478 55 Character Fallback Rate 
Index 
The fallback / replacement 
index.   
• CME Term SOFR  
• ICE Term SOFR  
• Term SOFR Refinitiv 
 Cash Fallback Rates-
 Consumer  
• Term SOFR Refinitiv 
 Cash Fallback Rates-
 Institutional 
533 3 Character Fallback Rate 
Tenor 
The tenor represents the 
interest rate period. 
1M / 3M / 6M / 12M 
536 2 Character Lookback Days The number of business or 
calendar days prior to the fixing 
reset day on which to determine 
the rate. 
Input the number of 
lookback days 
0-20 

---

## Page 9

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Term SOFR and ARR Record Details 9 
 
Term SOFR File Details 
538 15 Character Spread 
Adjustment 
Amount (bps) 
To adjust against LIBOR, the 
ARRC/ISDA recommends a 5-
year historical median for 
fallbacks to SOFR-based rates, 
however users can set spread 
level at any custom amount. 
This can be referred to as 
spread, [[Margin]], or applicable 
[[Margin]] 
See footnote: 1: 
• 1M = 11.448 
• 3M = 26.161  
• 6M = 42.826 
• 12M = 71.513 
• Other – please specify 
553 8 Character [[Margin]] Spread 
Amount (bps) 
Additional spread assigned by 
the [[issuer]]. This can be referred 
to as spread, [[Margin]], or 
applicable [[Margin]]. 
Input a basis point spread 
in whole basis points (e.g., 
a spread of .26161 in 
percentage points would 
be 26.161 in basis points). 
561 10 Character The First Non-
LIBOR Reset 
Date 
Start of ARR coupon period. 
This is used to determine day 
count fractions for act/act 
(ICMA) and act/365L 
conventions. All other 
calculations, including rate 
reference dates for term rates 
are based on the start date input
 
Use a calendar on the UI 
to input a date
 YYYY-
MM-DD 
571 28 Character Floating Rate 
Calendar 
The business calendar used for 
determining/applying fixing 
rates. 
See footnote 2:  
• US Government Bond 
Market  
• And/or add free-form 
text representing 
another Calendar Type 
599 202 
 
Character Filler For Future Use  
 
2 This value will appear blank on the LIBOR Replacement Index Communication Tool Review Submissions function unless a Reset Dat e has been specified 
and/or the Floating Rate Calendar field has been modified.  
 
  
 
1 Please remove the tenor when uploading a Spread Adjustment Amount when using the LIBOR Replacement Index Communication Tool.  For example, input 
11.448 instead of 1M = 11.448 on the upload spreadsheet.  

---

## Page 10

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Term SOFR and ARR Record Details 10 
 
ARR (Alternative Reference Rate) File Details  
The layout below describes the Alternative Reference Rate - rate type. The ARR represents many different 
types of indices across many different tenors, some of which are derived from the SOFR rate type.   
ARR File Details 
Position Length Format Field Name Field Description Valid Values 
1 4 Character Rate Type Either Alternative Reference 
Rate (ARR) or Secured 
Overnight Financing Rate 
(SOFR)  
 
5 9 Character [[CUSIP]] A [[CUSIP]] is a security identifier 
issued by [[CUSIP]] Global 
Services and is composed of 
nine characters and can include 
letters and numbers. 
Nine-digit alphanumeric 
security [[ID]] 
14 1 Character [[CUSIP]] on [[DTC]] 
Masterfile 
[[CUSIP]] is present on the [[DTCC]] 
Master Table 
Y or N 
• Y = Yes 
• N = No 
•  
15 1 Character Replacement 
Choice Made 
Field that describes to the 
market whether the issue has 
chosen a LIBOR replacement.  
If set to Yes, a replacement has 
been made.  If set to No, it can 
be determined that a choice has 
not yet been made, and that 
another record will be submitted 
once a replacement index has 
been decided upon.   
Y or N 
• Y = Yes 
• N = No 
 
16 1 Character Updated 
Submission 
Is previously input data being 
updated with this submission? 
Y or N 
• Y = Yes 
• N = No 
 
17 70 Character Submitter 
Company 
The firm or organization, whose 
personnel are inputting a 
replacement rate change into 
the LIBOR Replacement Index 
Communication Tool. 
Enter a Company Name 
87 20 Character Submitter 
Entity Type 
The type of service that the firm 
is performing on behalf of or as 
the [[issuer]] of this security. 
• Paying Agent  
• [[transfer agent]]  
• [[issuer]]  
• Calculation Agent  
• Trustee  
• Determining Person  

---

## Page 11

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Term SOFR and ARR Record Details 11 
 
ARR File Details 
• Other 
107 140 Character Submitter 
Contact Email 
The email address of the 
contact at the firm or 
organization inputting a 
replacement rate change into 
the LIBOR Replacement Index 
Communication Tool. 
Enter an email address 
247 1 Character Information 
Source 
Indicator 
If the Information Source is 
different from the Submitter 
Y or N 
• Y = Yes 
• N = No 
 
248 70 Character Information 
Source / 
Provider 
Company 
Name 
The firm or organization that 
was responsible for the 
selection of replacement index  
Enter Company Name 
318 20 Character Information 
Source / 
Provider Entity 
Type 
The type of service that the firm 
who selected the replacement 
index performs on behalf of the 
security 
• Paying Agent  
• [[transfer agent]]  
• Calculation Agent  
• Determining Person  
• [[issuer]]  
• Trustee  
• Other 
 
338 140 Character Information 
Source / 
Provider 
Contact email 
The email address of the 
contact at the firm or 
organization responsible for 
selecting the 
replacement index    
Enter Email address 
478 40 Character Fallback Rate 
Index 
The fallback / replacement 
index.   
SOFR Overnight Rate 
SOFR Averages  
As an extension of the 
Secured Overnight 
Financing Rate (SOFR), 
the SOFR Averages are 
compounded averages of 
the SOFR over rolling 30-, 
90-, and 180-calendar day 
periods. 
• SOFR 30-day avg 
• SOFR 90-day avg 
• SOFR 180-day avg 
SOFR Index 
The SOFR Index 
measures the cumulative 
impact of compounding 

---

## Page 12

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Term SOFR and ARR Record Details 12 
 
ARR File Details 
the SOFR on a unit of 
investment over time, with 
the initial value set to 
1.00000000 on April 2, 
2018, the first value date 
of the SOFR. 
Fed Funds 
• Effective Federal Funds 
Rate  
• Overnight Bank Funding 
Rate  
• Tri-Party General 
[[collateral]] Rate 
• Broad General 
[[collateral]] Rate  
Refinitiv Fallbacks  
• Refinitiv O/N 
• Refinitiv 1W 
• Refinitiv 1M 
• Refinitiv 2M 
• Refinitiv 3M 
• Refinitiv 6M 
• Refinitiv 12M 
BSBY 
• BSBY O/N 
• BSBY 1M 
• BSBY 3M 
• BSBY 6M 
• BSBY 12M 
AMERIBOR  
• AMERIBOR O/N 
• AMERIBOR 1W 
• AMERIBOR 1M 
• AMERIBOR 3M 
• AMERIBOR 6M 
• AMERIBOR 1Y 
• AMERIBOR 2Y 
• AMERIBOR 30-day 
average 
• AMERIBOR 90-day 
average 
• AMERIBOR 30T 
derived 
• AMERIBOR 90T 
derived  
 

---

## Page 13

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Term SOFR and ARR Record Details 13 
 
ARR File Details 
PRIME 
SOFR ICE Swap Rate 
• SOFR ISR 1Y 
• SOFR ISR 2Y 
• SOFR ISR 3Y 
• SOFR ISR 4Y 
• SOFR ISR 5Y 
• SOFR ISR 6Y 
• SOFR ISR 7Y 
• SOFR ISR 8Y 
• SOFR ISR 9Y 
• SOFR ISR 10Y 
• SOFR ISR 15Y 
• SOFR ISR 20Y 
• SOFR ISR 30Y 
Synthetic USD LIBOR 
SOFR ICE Spread-
Adjusted ICE Swap Rate 
• SOFR Spread-Adjusted 
ISR 1Y 
• SOFR Spread-Adjusted 
ISR 2Y 
• SOFR Spread-Adjusted 
ISR 3Y 
• SOFR Spread-Adjusted 
ISR 4Y 
• SOFR Spread-Adjusted 
ISR 5Y 
• SOFR Spread-Adjusted 
ISR 6Y 
• SOFR Spread-Adjusted 
ISR 7Y 
• SOFR Spread-Adjusted 
ISR 8Y 
• SOFR Spread-Adjusted 
ISR 9Y 
• SOFR Spread-Adjusted 
ISR 10Y 
• SOFR Spread-Adjusted 
ISR 15Y 
• SOFR Spread-Adjusted 
ISR 20Y 
• SOFR Spread-Adjusted 
ISR 30Y 
Other – Please see PDF 

---

## Page 14

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Term SOFR and ARR Record Details 14 
 
ARR File Details 
518 15 Character Spread 
Adjustment 
Amount (bps) 
To adjust against LIBOR, the 
ARRC/ISDA recommends a 5-
year historical median for 
fallbacks to SOFR-based rates, 
however users can set spread, 
[[Margin]], or applicable [[Margin]] 
See footnote 2: 
• O/N = .64 
• 1M = 11.448 
• 3M = 26.161  
• 6M = 42.826 
• 12M = 71.513 
• Other – please specify  
 
533 8 Character [[Margin]] Spread 
(bps) 
Additional spread assigned by 
the [[issuer]].  This can be referred 
to as spread, [[Margin]], or 
applicable [[Margin]]. 
Input a basis point spread 
in whole basis points (e.g., 
a spread of .26161 in 
percentage points would 
be 26.161 in basis points). 
541 18 Character Spread 
Methodology 
This defines how the spread will 
be incorporated into the interest 
calculation. 
• Spread Inclusive  
• Spread Exclusive  
• Flat 
559 25 Character Day Count 
Convention 
System representing the day 
count convention used for 
calculating yields and/or 
accrued interest 
• Act/360 
• Act/365L  
• Act/Act  
• Act/365F 
• 30/360 
• 30E/360 
584 25 Character Interest Accrual 
Methodology 
The interest accrual calculation 
methodology 
• Compound in-Arrears 
• Simple Daily in-Arrears 
• Average in-Arrears 
• Compound in-Advance 
• Term  
• Other 
609 8 Character Lookback Days 
Type 
The calendar usage type 
Defines whether the lookback 
days are counted in calendar 
days or business days only. 
• Business 
• Calendar 
617 2 Character Lookback Days The number of business or 
calendar days prior to the fixing 
reset day on which to determine 
the rate. 
Input the number of 
lookback days 
 0-20 days 
619 3 Character Observation 
Shift 
The Observation Shift is used to 
align the interest rate with the 
Input the observation shift 
-20 to 20 
 
2 Please remove the tenor when uploading a Spread Adjustment Amount when using the LIBOR Replacement Index Communication Tool.  For example, input 
11.448 instead of 1M = 11.448 on the upload spreadsheet.  

---

## Page 15

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Term SOFR and ARR Record Details 15 
 
ARR File Details 
appropriate day count weighting 
when a lookback is used 
622 2 Character Lockout Days Indicates the number of days 
prior to the end of the current 
coupon rate observation period 
where the current rate will 
cease being subject to reset. 
Input the number of 
lockout days 
0-20 days 
624 2 Character Payment Delay 
Days 
Delay between the end of the 
accrual period and the payment. 
Input the number of 
lockout days 
0-20 days 
626 26 Character Rounding 
Instructions 
Rounding can be applied to 
annualized rate of interest pre 
calculation, or round final 
output. 
Round Input rate  
Round Final Rate 
Round Final and Input 
Rate  
No Rounding 
652 1 Character Rounding 
Decimals 
Places 
The number of decimal places 
to round numbers to, rounding 
instruction can be found in term 
sheets and other [[securities]] 
prospectus including where to 
apply rounding in the calculation 
process. 
a value between 0 and 
8 
653 40 
 
Character Business Day 
Convention 
The business day convention 
determines how to proceed 
when a date which is relevant 
for the payment or calculation of 
interest falls on a non-business 
day. 
• Business Day Adjusted  
• Following Business Day 
Unadjusted  
• Modified Business Day 
Adjusted  
• Modified Business Day 
Unadjusted 
• Preceding Business 
Day Adjusted 
• Preceding Business 
Day Unadjusted 
693 
 
10 Character The First Non-
LIBOR Reset 
Date 
Start of ARR coupon period. 
This is used to determine day 
count fractions for act/act 
(ICMA) and act/365L 
conventions. All other 
calculations, including rate 
reference dates for term rates 
are based on the start date 
input. 
Use a calendar on the UI 
to input a date 
YYYY-MM-DD 
703 
 
28 Character Floating Rate 
Calendar 
The business calendar used for 
determining/applying fixing 
rates. 
See footnote 3:  
• US Government Bond 
Market  

---

## Page 16

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
Term SOFR and ARR Record Details 16 
 
ARR File Details 
• And/or add free-form 
text representing 
another Calendar Type 
 
731 
 
70 
 
Character Filler For Future Use  
 
3This value will appear blank on the LIBOR Replacement Index Communication Tool Review Submissions function unless a Reset Date has been specified 
and/or the Floating Rate Calendar field has been modified.  

---

## Page 17

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
ARR and Term SOFR Data Dictionaries 17 
 
ARR AND TERM SOFR DATA DICTIONARIES   
The following data dictionaries define the data elements available for communicating a LIBOR Replacement 
Index choice to [[DTCC]]. You can refer to the data dictionaries as a good source for detailed information. Within 
the dictionaries we include: 
• a description of the field,  
• whether the field was required or optional, and  
• why the field is important 
• t he valid values that can be added to a field. 
ARR Data Dictionary 
Click to open the ARR Data Dictionary.    
Term SOFR Data Dictionary 
Click to open the Term SOFR Data Dictionary. 
  

---

## Page 18

LIBOR Replacement Index File Specification Guide: Autoroute [[ID]] 05983676 (PSE); [[ID]] 05213676 (Prod) 
 
ARR and Term SOFR Data Dictionaries 18 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] at: 
DTCSupport@[[DTCC]].com 
or visit us on the web at: 
http://www.[[DTCC]].com/client-center 
 