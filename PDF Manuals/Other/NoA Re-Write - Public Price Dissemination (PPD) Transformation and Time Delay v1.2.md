---
title: "NoA Re-Write Phase 2 PPD Transformation & Time Delay"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/NoA%20Re-Write%20-%20Public%20Price%20Dissemination%20%28PPD%29%20Transformation%20and%20Time%20Delay%20v1.2.pdf"
pages: 21
size: "382.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# NoA Re-Write Phase 2 PPD Transformation & Time Delay

**Original File:** [NoA Re-Write - Public Price Dissemination (PPD) Transformation and Time Delay v1.2.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/NoA%20Re-Write%20-%20Public%20Price%20Dissemination%20%28PPD%29%20Transformation%20and%20Time%20Delay%20v1.2.pdf)  
**Category:** Other  
**Total Pages:** 21  
**File Size:** 382.8 KB  

---

## Page 1

 
 
Global Trade Repository 
NORTH AMERICA (NOA) RE-WRITE PHASE 2: 
PUBLIC PRICE DISSEMINATION 
TRANSFORMATION AND TIME DELAY  
VERSION 1.2 
OCT 11, 2023 
 
 
 
 
  

---

## Page 2

 
 
Document Revision History 
Date Author Version Description 
June 30, 2022 JY 1.0 Initial Draft  
August 1, 2022 JY 1.1 Update to Tenor calculation to include Maturity Date 
of the Underlying field 
Oct 11, 2023 PC 1.2 Updated notional amounts to include negative values 
 
Changed from "XA" to "FX" for [CDE - Call amount-
Leg 1], [CDE - Call currency-Leg 1], [CDE - Put 
amount-Leg 1] and [CDE - Put currency-Leg 1] and 
removal of the equivalent Leg 2 fields 
 
Note: Production date for these changes is January 
28th 2024. 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Document Revision History ................................................................................................................................ 2 
1. Overview ........................................................................................................................................................... 4 
2. Rounding ........................................................................................................................................................... 6 
2.1: Rounding Scale for [[CFTC]] (Part 43) and [[SEC]] PPD..................................................................................... 6 
2.2: Rounding Scale for Canada PPD ................................................................................................................ 7 
3. CAPPING ........................................................................................................................................................... 9 
3.1:  Credit Capping Rules .................................................................................................................................. 9 
3.2:  Interest Rates Capping Rules ...................................................................................................................10 
3.3:  Foreign Exchange Capping Rules ............................................................................................................11 
3.4:  Equities Exchange Capping Rules ...........................................................................................................11 
3.5:  Commodities Capping Rules ....................................................................................................................11 
4. SCALING ......................................................................................................................................................... 12 
5. TIME DELAY .................................................................................................................................................... 13 
5.1:  [[CFTC]] Time Delay .....................................................................................................................................13 
5.2:  [[SEC]] Time Delay .......................................................................................................................................20 
5.3:  Canada Time Delay ..................................................................................................................................20 

---

## Page 4

 
 
1.  OVERVIEW 
This document describes Public Price Dissemination (PPD) transformation relating to the rounding, scaling, and 
capping of certain PPD fields performed by the GTR prior to public dissemination. The table below shows the 
applicability of the rules by jurisdiction & [[Asset]] class:  
Jurisdiction PPD 
Transformation 
FX IR EQ CR CO 
[[CFTC]] 
Rounding     
Capping     
Scaling     
[[SEC]] 
Rounding     
Capping     
Scaling     
Canada 
Rounding     
Capping     
Scaling     
 
Notional or Principal Amount fields for Rounding, Capping and Scaling 
 
Capping and Rounding rules are applied to the Notional Amount and Quantity fields listed below. The fields listed 
below are Cross [[Asset]] per the North America Re-Write Message Specification unless otherwise noted.  
 
Leg 1 Leg 2 
[Notional Amount 1]* [Notional Amount 2]* 
[CDE - Notional amount in effect on associated 
effective date-Leg 1] 
[CDE - Notional amount in effect on associated 
effective date-Leg 2] 
[CDE - Call amount-Leg 1] (FX Only)  
[CDE - Put amount-Leg 1] (FX Only)  
[Leg 1 - Total Notional Quantity] (EQ, CO only) [Leg 2 - Total Notional Quantity] (EQ, CO only) 
[Leg 1 - Notional Quantity] (CO only) [Leg 2 - Notional Quantity] (CO only) 
 
*First, a ‘Chosen Leg’ is determined using the larger of [Notional Amount 1] or [Notional Amount 2] (in USD) 
for FX, IR, EQ, CO and CR. Capping and rounding is applied to all fields in the Chosen Leg (all fields in Leg 1 
above or Leg 2 above) prior to scaling and the application of capping and rounding requirements to the other leg 
and other financial fields as detailed below for each [[Asset]] class.  
 
Notes:  
• If the Notional Amount is “99999999999999999999.99999” (which is accepted when the value is not 
available at the time of reporting), no capping, scaling, or rounding rules will be applied. The amount 
disseminated will be “99999999999999999999.99999” 
• The inbound field [Latest Execution DateTime] is used to determine exchange rate conversions. 

---

## Page 5

 
 
• If any submitted notional values are negative, DDR will take the absolute value.  This absolute value 
will be the value used in the process of capping, rounding, and scaling.  The result will be disseminated 
and reported in a negative value. 
 
 
Scaled fields 
Scaling is applied to proportionally scale applicable financial fields that are disseminat ed to avoid 
fingerprinting and distortion.   In addition to the Notional Amount and Quantity fields above, the following fields 
are scaled:  
• CDE - Other payment amount 
• [[Premium]] Amount 
• Price 1 – Price 
 
Time Delays 
This document also describes how Time Delays are calculated for the North America PPD submissions.  
 
Jurisdiction Time Delay 
[[CFTC]] Various times calculated based on [[CFTC]] Part 43 regulations. 
[[SEC]] No Time Delays applied 
Canada 48 hours for all PPD submissions 

---

## Page 6

 
 
2. ROUNDING 
Rounding rules are identical across all [[Asset]] classes  and aligned with the respective regulations.  Floor and 
Ceiling values represent the range to which the applicab le field (generally Notional amount type fields) will be 
rounded. Rounded results have no decimal places.  
2.1: Rounding Scale for [[CFTC]] (Part 43) and [[SEC]] PPD 
Floor Ceiling Round to (if equidistant, always to 
the highest multiple) 
Use Cases 
Notional Amount 
(Submitted Value) Rounded 
>= 0 < 5 5 (Value cannot be less than 5) 2 5 
          
>= 5 < 1,000 Nearest multiple of 5 
222 220 
222.5 225 
          
>= 1,000 < 10,000 Nearest multiple of 100 
8,640 8,600 
8,650 8,700 
          
>= 10,000  < 100,000 Nearest multiple of 1,000 
44,300 44,000 
44,500 45,000 
          
>= 100,000 < 1,000,000 Nearest multiple of 10,000 
744,500 740,000 
745,000 750,000 
          
>= 1,000,000 < 100,000,000 Nearest multiple of 1,000,000 
89,100,000 89,000,000 
89,800,000 90,000,000 
          
>= 100,000,000 < 500,000,000 Nearest multiple of 10,000,000 
372,000,000 370,000,000 
377,000,000 380,000,000 
          
>= 500,000,000 < 1,000,000,000 Nearest multiple of 50,000,000 
810,000,000 800,000,000 
835,000,000 850,000,000 

---

## Page 7

 
 
          
>= 1,000,000,000 < 100,000,000,000 Nearest multiple of 100,000,000 
66,650,000,000 67,700,000,000 
87,010,000,000 87,000,000,000 
          
>= 100,000,000,000 None Nearest multiple of 10,000,000,000 
101,000,000,000 100,000,000,000 
227,000,000,000 230,000,000,000 
2.2: Rounding Scale for Canada PPD 
Floor Ceiling Round to (if equidistant, always to 
the highest multiple) 
Use Cases 
Notional Amount 
(Submitted Value) Rounded 
>= 0 < 1,000 Nearest multiple of 5 
1 5 
986 985 
        
>= 1,000 < 10,000 Nearest multiple of 100 
8,867 8,900 
8,849 8,800 
        
>= 10,000  < 100,000 Nearest multiple of 1,000 
10,234 10,000 
10,598 11,000 
        
>= 100,000 < 1,000,000 Nearest multiple of 10,000 
478,237 480,000 
494,363 490,000 
        
>= 1,000,000 < 10,000,000 Nearest multiple of 100,000 
9,163,000 9,200,000 
9,130,000 9,100,000 
        
>= 10,000,000 < 50,000,000 Nearest multiple of 1,000,000 
48,650,000 49,000,000 
42,320,000 42,000,000 
        
61,500,000 60,000,000 

---

## Page 8

 
 
>= 50,000,000 < 100,000,000 Nearest multiple of 10,000,000 66,500,000 70,000,000 
        
>= 100,000,000 < 500,000,000 Nearest multiple of 50,000,000 
460,000,000 450,000,000 
380,000,000 400,000,000 
        
>= 500,000,000 < 1,000,000,000 Nearest multiple of 100,000,000 
625,000,000 600,000,000 
850,000,000 900,000,000 
        
>= 1,000,000,000 < 100,000,000,000 Nearest multiple of 500,000,000 
30,750,000,000 31,000,000,000 
56,535,530,000 56,500,000,000 
     
>= 100,000,000,000  Nearest multiple of 50,000,000,000 
175,000,000,000 200,000,000,000 
255,000,000,000 250,000,000,000 

---

## Page 9

 
 
3. CAPPING 
The following section illustrates how GTR applies the capping logic based on the PPD message received. When 
a notional amount has been capped a “+” will be displayed.  
3.1:  Credit Capping Rules 
The below requirements illustrate how GTR applies the capping rules for the credit [[Asset]] class.  
[[CFTC]] 
Submissions under the Credit [[Asset]] class will be capped in accordance with the below table when submitted in 
basis points under the applicable tenor.  
Tenor Calculation: Tenor is based on the End Date, [Maturity Date of the Underlying] when populated, else   
[CDE - Expiration Date] minus the greater of the Effective Date [CDE - Effective Date] or Trade/Execution 
Date [Original Execution TimeStamp], in days. 
Basis Point Spread Calculation: The CDE – Spread Notation fields must equal “4” for Basis Points and then 
the Spread Amount  (must be greater than 0) fields will be used for the Basis Point Spread amount for the 
respective notional leg. If the Spread Notation is not represented in Basis Points, GTR will utilize the cap of 100 
million (USD). 
Fields used: 
• [CDE - Spread notation-Leg 1]  
• [Leg 1 - Spread Amount] 
• [CDE - Spread notation-Leg 2] 
• [Leg 2 - Spread Amount]  
 
Basis Point Spread  
Tenor <=175 >175 <=350 >350 
0 - 746 Days (2 Years) 320* 140 100 
  747 Days (>2 Years) to 1,477 Days (>4 Years) 200 100 100 
1,478 Days (>4 Years) 2,207 Days (>6 Years) 110 100 100 
2,208 Days (>6 Years) 3,120 Days (>8 Years) 110 100 100 
3,121 Days (>8 Years) 4,581 Days (>12 Years) 130 100 100 
4,581 Days + (>12 Years)  100 100 100 
 
[[SEC]] 
All Credit PPD submissions will be capped at 5 million USD. 
 
Canada 
All Credit PPD submissions will be capped at 50 million CAD. 
 
 

---

## Page 10

 
 
3.2:  Interest Rates Capping Rules 
The below requirements illustrate how GTR applies the capping rules for the interest rate [[Asset]] class.   
 
[[CFTC]] and [[SEC]] 
Submissions under the Interest Rates [[Asset]] class will be capped in accordance with the below table based on 
the currency category under the applicable tenor.  
 
Tenor Calculation: Tenor is based on the End Date, [Maturity Date of the Underlying] when populated, else  
[CDE - Expiration Date] minus the greater of the Effective Date [CDE - Effective Date] or Trade/Execution 
Date [Original Execution TimeStamp], in days. 
 
Currency Category: The field being reviewed for capping will fall into Super Major, Major or Non -Major based 
on the currencies listed in the table below.  
 
Super Major 
(USD, EUR, GBP, JPY)  
Major 
(AUD, CHF, CAD, ZAR, 
KRW, SEK, NZD, NOK, 
DKK)  
Non-Major 
(All Other Currencies)  
 
Currencies used for each notional amount field to determine the category will be based on the below:  
 
Inbound Field Name Currency Field for Currency Category 
[Notional Amount 1]  [Notional Currency 1]  
 [Notional Amount 2] [Notional Currency 2] 
[CDE - Notional amount in effect on associated 
effective date-Leg 1] [Notional Currency 1] 
[CDE - Notional amount in effect on associated 
effective date-Leg 2] [Notional Currency 2] 
[CDE - Call amount-Leg 1] [CDE - Call Currency- Leg 1]  
[CDE - Call amount-Leg 2] [CDE - Call Currency-Leg 2] 
[CDE - Put amount-Leg 1] [CDE - Put Currency- Leg 1]  
[CDE - Put amount-Leg 2] [CDE - Put Currency- Leg 2] 
 
Below table illustrates the capping requirements per currency category and tenor.  
 
 Currency Category (Notional in USD Millions) 
Tenor Super Major Major Non-Major 
0 to 46 Days 6.4 billion 2.2 billion 250 million 
47 Days to Three Months (107 Days) 2.1 billion 580 million 250 million 
Three months (108 days) to Six months (198 days) 1.2 billion 440 million 250 million 
Six months (199 days) to One year (381 days) 1.1 billion 250 million 250 million 
One year (382 days) to Two years (746 days) 460 million 250 million 250 million 
Two years (747 days) to Five years (1,842 days) 240 million 100 million 100 million 
Five years (1,843 days) to Ten years (3,668 days) 170 million 100 million 100 million 
Ten years (3,669 days) 30 years (10,973 days) 120 million 75 million 75 million 
30 years + (10,974 days) 75 million 75 million 75 million 
 
 
Canada 

---

## Page 11

 
 
Submissions under the Interest Rates [[Asset]] class will be capped in accordance with the below table based on 
the applicable tenor.  
 
Tenor Calculation: Tenor is based on the End Date [CDE - Expiration Date] minus the greater of the Effective 
Date [CDE - Effective Date] or Trade/Execution Date [Original Execution TimeStamp], in days. 
 
[[Asset]] Class Tenor Capped Rounded Notional 
Amount in CAD 
Interest Rate  
Less than or equal to two years (0 to 730) 250M 
Greater than two years (731 days) and less 
than or equal to ten years (3,650 days) 100M 
Greater than ten years (3,651 days) 50M 
3.3:  Foreign Exchange Capping Rules 
[[CFTC]] 
All FX PPD submissions will be capped at 250 million USD. 
 
[[SEC]] and Canada 
Not Applicable 
3.4:  Equities Exchange Capping Rules 
[[CFTC]] and [[SEC]] 
All [[Equity]] PPD submissions will be capped at 250 million USD. 
 
Canada 
All [[Equity]] PPD submissions will be capped at 50 million CAD. 
3.5:  Commodities Capping Rules 
[[CFTC]] and [[SEC]] 
All Commodity PPD submissions will be capped at 25 million USD. This capped valued for the Notional Quantity 
and Total Notional Quantity fields will be based on the value in the [Notional Amount 1] field. 
 
[[SEC]] and Canada 
Not Applicable 
  

---

## Page 12

 
 
4. SCALING 
[[CFTC]]/[[SEC]]/Canada 
Scaling is applied to proportionally scale applicable financial fields that are disseminated to avoid  
fingerprinting and distortion.  
 
The scale factor is determined by the rounded/capped versus original Notional Amount of the Chosen Leg. F or 
example, if Leg 1 was the Chosen Leg, the scaling factor will be determined using. The scale will always use 
either [Notional Amount 1] or [Notional Amount 2].  
 
Scale Factor Example = Rounded or Capped [Notional Amount 1] / [Notional Amount 1]  
 
(Capped) 
Notional 
Amount 
Actual 
Notional Calculation Scaling Factor 
250 million 1 billion 250,000,000/1,000,000,000 0.25 
 
 
This scale is applied to all fields in the other Leg of Notional Amounts and Quantities and the following fields:  
• CDE - Other payment amount 
• [[Premium]] Amount 
• Price 1 - Price 
 
Example of scale factor applied: 
 
[[Premium]] Amount Scaling Factor Disseminated Amount 
6,250,000 6,250,000 *0.25 1,562,500 
 

---

## Page 13

 
 
5. TIME DELAY 
5.1:  [[CFTC]] Time Delay 
There are several scenarios where time delays are applied to [[CFTC]] PPD submissions. Inbound fields used to 
determine if the time delays are listed below and on the following page: 
 
Scenario Counterparties & Execution Description Time Delay  
1 Block Trades Executed on or Pursuant to the Rules of a Registered SEF or DCM 15 minutes 
2 Large Notional Off-facility Swaps Subject to the Mandatory Clearing Requirement With 
at Least One Swap Dealer or Major Swap [[participant]] Counterparty 
15 minutes 
3 Large Notional Off -facility Swaps Subject to the Mandatory Clearing Requirement in 
which neither counter party is a Swap Dealer or Major Swap [[participant]]  
1 hour  
4 Large Notional Off-facility Swaps not Subject to the Mandatory Clearing Requirement 
with at least one Swap dealer or Major Swap [[participant]] counterparty. (FX, Credit and 
Interest Rates [[Asset]] Classes) 
30 minutes 
5 Large Notional Off-facility Swaps not Subject to the Mandatory Clearing Requirement 
with at least one Swap Dealer or Major Swap [[participant]] counterparty. (Commodities 
[[Asset]] Class) 
2 hours 
6 Large Notional Off-facility Swaps not Subject to the Mandatory Clearing Requirement 
in which neither is a Swap Dealer or Major Swap [[participant]].  
24 hours 
7 All Others not stated in 1 through 6 None 
 
Inbound Fields used for Time Delay Scenarios 
 
Criteria Inbound Field Name Scenarios 
1 2 3 4 5 6 7 
Type of action taken on the swap 
transaction • [NoA - Action Type]       
Executed on swap execution facility 
(SEF) or designated contract market 
(DCM)? 
• [SEF or DCM Indicator]       
"Block" / "Large" 
• [Block trade election indicator]            
• [Large notional off-facility swap election 
indicator]        
Subject to Mandatory Clearing 
• [Mandatory Clearing Indicator]                        
• [Clearing Exception Type]                                 
• [Clearing Exception Type - Party 2]        
Are counterparties Swap Dealers or 
MSP? 
• [SD MSP indicator - Counterparty 1]         
• [SD MSP indicator - Counterparty 2]        
[[Asset]] Class • [Primary [[Asset]] Class            
 
Note: If NoA Action Type = ‘EROR’, no time delays will be applied.  
 
Field Logic applied to Time Delay Calculation 
Counterparties & Execution 
Description 
(“Scenarios”) 
Field Logic for Calculation Time 
Delay  
Credit 
Rates 
FX 
Commodity 
[[regulation]] 
Reference 
1.      Block Trades 
Executed on or Pursuant to 
[SEF or DCM Indicator] = 'True'    

---

## Page 14

 
 
the Rules of a Registered SEF 
or DCM [Block trade election indicator] = 'True' 15 
minutes 
[[CFTC]] 43.5 
(d) 
2.      Large Notional Off -
facility Swaps Subject to the 
Mandatory Clearing 
Requirement With at Least  
One Swap Dealer or Major 
Swap [[participant]] 
Counterparty 
[SEF or DCM Indicator] = 'False' 
15 
minutes     [[CFTC]] 43.5 
(e) (2) 
[Large notional off -facility swap election 
indicator] = 'True' (or blank and meets 
calculated reqt) 
[Mandatory Clearing Indicator ] = 'True' AND 
([Clearing Exception Type ] = (blank) AND 
[Clearing Exception Type - Party 2] = (blank)) 
[SD MSP indicator - Counterparty 1] = 'True'  
OR [ SD MSP indicator - Counterparty 2 ] = 
'True' 
3.      Large Notional Off -
facility Swaps Subject to the 
Mandatory Clearing 
Requirement in which neither 
counter party is a Swap 
Dealer or Major Swap 
[[participant]]  
[SEF or DCM Indicator] = 'False' 
1 hour      [[CFTC]] 43.5 
(e) (3) 
[Large notional off-facility swap election 
indicator] = 'True' (or blank and meets 
calculated reqt) 
[Mandatory Clearing Indicator ] = 'True' AND 
([Clearing Exception Type ] = (blank) AND 
[Clearing Exception Type - Party 2] = (blank)) 
[SD MSP indicator - Counterparty 1] = 'False'  
AND [ SD MSP indicator - Counterparty 2 ] = 
'False' 
4.      Large Notional Off -
facility Swaps not Subject to 
the Mandatory Clearing 
Requirement with at least one 
Swap dealer or Major Swap 
[[participant]] counterparty. (FX, 
Credit and Interest Rates 
[[Asset]] Classes) 
[SEF or DCM Indicator] = 'False' 
30 
minutes      [[CFTC]] 43.5 
(f)  
[Primary [[Asset]] Class ] = 'Credit' or 
'ForeignExchange' or 'InterestRate' 
[Large notional off -facility swap election 
indicator] = 'True' (or blank and meets 
calculated reqt) 
([Mandatory Clearing Indicator ] = 'False') OR 
([Mandatory Clearing Indicator ] = 'True' AND 
([Clearing Exception Type ] not= (blank) OR 
[Clearing Exception Type - Party 2 ] not= 
(blank))) 
[SD MSP indicator - Counterparty 1] = 'True' 
OR [ SD MSP indicator - Counterparty 2 ] = 
'True' 
5.      Large Notional Off -
facility Swaps not Subject to 
the Mandatory Clearing 
Requirement with at least one 
Swap Dealer or Major Swap 
[[participant]] counterparty. 
(Commodities [[Asset]] Class) 
[SEF or DCM Indicator] = 'False' 
2 hours        [[CFTC]] 43.5 
(g) 
[Primary [[Asset]] Class] = 'Commodity' 
[Large notional off -facility swap election 
indicator] = 'True' (or blank and meets 
calculated reqt) 
([Mandatory Clearing Indicator ] = 'False') OR 
([Mandatory Clearing Indicator ] = 'True' AND 
([Clearing Exception Type ] not= (blank) OR 
[Clearing Exception Type - Party 2 ] not= 
(blank))) 

---

## Page 15

 
 
[SD MSP indicator - Counterparty 1] = 'True' 
OR [ SD MSP indicator - Counterparty 2 ] = 
'True' 
6.      Large Notional Off -
facility Swaps not Subject to 
the Mandatory Clearing 
Requirement in which neither 
is a Swap Dealer or Major 
Swap [[participant]].  
[SEF or DCM Indicator] = 'False' 
24 
hours     [[CFTC]] 43.5 
(h) 
[Large notional off -facility swap election 
indicator] = 'True' (or blank and meets 
calculated reqt) 
([Mandatory Clearing Indicator ] = 'False') OR 
([Mandatory Clearing Indicator ] = 'True' AND 
([Clearing Exception Type ] not= (blank) OR 
[Clearing Exception Type - Party 2 ] not= 
(blank))) 
[SD MSP indicator - Counterparty 1] = 'False' 
AND [ SD MSP indicator - Counterparty 2 ] = 
'False' 
7.     All Others not stated in 1 
through 6 
([SEF or DCM Indicator ] = 'True' AND [ Block 
trade election indicator] = "False") 
None    
(Time delay 
does not 
apply) 
OR 
([SEF or DCM Indicator ] = 'False' AND [ Large 
notional off-facility swap election indicator] = 
"False") 
Note: Large trade size and time delays [[DO]] not apply to the Equities [[Asset]] Class.  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 16

 
 
Expected Dissemination Timestamp: 
Every submission staged for dissemination has an Expected Dissemination Timestamp  that will be based off of the [Latest Execution Timestamp] and 
any time delays calculated per above. 
 
Action Type Logic when there are Pending Submissions:  
In order to preserve the message sequencing, GTR will implement the following:  
 
For all action and event types, time delays will be calculated on new submissions and be compared to pending submissions. If the calculated dissemination 
time of the submission is: 
i. Equal or greater (later) than the pending transactions, no further action to take (sequencing will be in order)  
ii. Less (earlier) than the pending transactions, update the dissemination time to the pending time (to keep sequencing in order)  
 
While this may give a dditional time delays for some submissions, this will prevent fingerprinting of trades for firms to the public. Additionally,  while not 
explicitly stated, this is generally in line with the [[CFTC]] Guidebook which states that error messages should be dissemin ated after the time delay expires. 
 
Use Cases: 
 
Submitted Data  Dissemination 
Case 
Submission # 
Latest Execution 
Timestamp 
NoA Action 
Type 
Event Type 
System 
TimeStamp 
Dissemination 
[[ID]] 
Original 
Dissemination 
[[ID]] 
NoA Action 
Type 
Event Type 
Time Delay 
Expected Dissemination 
Timestamp Notes 
1 
1 
2022-03-
30T15:15:15Z NEWT TRAD 
2022-03-
30T15:15:15Z 1   NEWT TRAD 15 minutes 2022-03-30T15:30:15Z   
2 
2022-03-
31T06:15:30Z EROR   
2022-03-
31T06:15:30Z 2 1 EROR   None 2022-03-31T06:15:30Z 
No Time Delay applied to 
EROR. 
                         
2 
1 
2022-03-
30T16:05:15Z NEWT TRAD 
2022-03-
30T15:15:15Z 3   NEWT TRAD 2 hours 2022-03-30T18:05:15Z    
2 
2022-03-
30T16:15:30Z EROR   
2022-03-
31T06:15:30Z 4 3 EROR   None 
Calculated: 2022-03-
30T16:15:30Z / Applied: 
2022-03-30T18:05:15Z 
Disseminate both the pending 
NEWT and EROR after time 
delay expires 
                         

---

## Page 17

 
 
Submitted Data  Dissemination 
Case 
Submission # 
Latest Execution 
Timestamp 
NoA Action 
Type 
Event Type 
System 
TimeStamp 
Dissemination 
[[ID]] 
Original 
Dissemination 
[[ID]] 
NoA Action 
Type 
Event Type 
Time Delay 
Expected Dissemination 
Timestamp Notes 
3 
1 
2022-03-
30T16:05:15Z NEWT TRAD 
2022-03-
30T16:05:15Z 5   NEWT TRAD 2 hours 2022-03-30T18:05:15Z    
2 
2022-03-
30T16:15:30Z EROR   
2022-03-
30T16:15:30Z 6 5 EROR   None 
Calculated: 2022-03-
30T16:15:30Z / Applied: 
2022-03-30T18:05:15Z 
Disseminate both the pending 
NEWT and EROR after time 
delay expires 
3 
2022-04-
30T16:15:30Z REVI   
2022-04-
30T16:15:30Z 7 5 REVI   None 2022-04-30T16:15:30Z   
                         
4 
1 
2022-03-
30T15:15:15Z NEWT TRAD 
2022-03-
30T15:15:15Z 8   NEWT TRAD 1 hour 2022-03-30T16:15:15Z  Waiting for dissemination 
2 
2022-03-
30T15:20:15Z MODI TRAD 
2022-03-
30T15:20:15Z 9 8 MODI TRAD 1 hour 2022-03-30T16:20:15Z  
Waiting for dissemination - No 
change to timestamp since the 
new submission will be 
disseminated after the pending 
transaction. 
3 
2022-03-
30T15:30:15Z EROR   
2022-03-
30T15:30:15Z 10 8 EROR   None 
Calculated: 2022-03-
30T15:30:15Z Applied: 
2022-03-30T16:20:15Z 
ERORs are not disseminated 
until the time delay expires from 
the last pending submission. 
                          
5 
1 
2022-03-
30T15:15:15Z NEWT TRAD 
2022-03-
30T15:15:15Z 11   NEWT TRAD None 2022-03-30T15:15:15Z   
2 
2022-03-
30T15:20:15Z MODI TRAD 
2022-03-
30T15:20:15Z 12 11 MODI TRAD 1 hour 2022-03-30T16:20:15Z  
No pending submissions, 
therefore no updates to 
timestamps.  

---

## Page 18

 
 
Submitted Data  Dissemination 
Case 
Submission # 
Latest Execution 
Timestamp 
NoA Action 
Type 
Event Type 
System 
TimeStamp 
Dissemination 
[[ID]] 
Original 
Dissemination 
[[ID]] 
NoA Action 
Type 
Event Type 
Time Delay 
Expected Dissemination 
Timestamp Notes 
3 
2022-03-
30T15:30:15Z EROR   
2022-03-
30T15:30:15Z 13 11 EROR   None 
Calculated: 2022-03-
30T15:30:15Z Applied: 
2022-03-30T16:20:15Z 
ERORs are not disseminated 
until the time delay expires from 
the last pending submission. 
                          
6 
1 
2022-03-
30T15:15:15Z NEWT TRAD 
2022-03-
30T15:15:15Z 14   NEWT TRAD 15 minutes 2022-03-30T15:30:15Z   
2 
2022-03-
30T15:20:15Z MODI TRAD 
2022-03-
30T15:20:15Z 15 14 MODI TRAD 2 hours 2022-03-30T17:20:15Z  
No change to timestamp since 
the NEWT is disseminated 
before the MODI. Update the 
timestamp when the EROR 
comes in as Submission 4 
3 
2022-03-
30T15:30:15Z CORR   
2022-03-
30T15:30:15Z 16 14 CORR   1 hour 
Calculated: 2022-03-
30T16:30:15Z / Applied: 
2022-03-30T17:20:15Z 
2022-03-30T16:30:15Z  is  less 
than the previous pending  
submission of 2022 -03-
30T17:20:15Z therefore the 
greater (later) value of the 
current and pending 
submissions is used. (previous 
submission timestamp).  
4 
2022-03-
30T17:00:15Z CORR   
2022-03-
30T17:00:15Z 16 14 CORR   15 min 
Calculated: 2022-03-
30T17:15:15Z / Applied: 
2022-03-30T17:20:15Z  
5 
2022-03-
30T17:01:15Z EROR   
2022-03-
30T17:01:15Z 17 14 EROR   None 
Calculated: 2022-03-
30T17:01:15Z / Applied: 
2022-03-30T17:20:15Z 
ERORs are not dissemina ted 
until the time delay expires from 
the last pending submission 
                          

---

## Page 19

 
 
Submitted Data  Dissemination 
Case 
Submission # 
Latest Execution 
Timestamp 
NoA Action 
Type 
Event Type 
System 
TimeStamp 
Dissemination 
[[ID]] 
Original 
Dissemination 
[[ID]] 
NoA Action 
Type 
Event Type 
Time Delay 
Expected Dissemination 
Timestamp Notes 
7 
1 
2022-03-
30T15:15:15Z NEWT TRAD 
2022-03-
30T15:15:15Z 18   NEWT TRAD 24 hours 2022-03-31T15:15:15Z  
  
2 
2022-03-
30T18:20:15Z MODI TRAD 
2022-03-
30T18:20:15Z 19 18 MODI TRAD None 
Calculated: 2022-03-
30T18:20:15Z / Applied - 
2022-03-31T15:15:15Z 
Since the pending 
dissemination has a greater 
(later) timestamp than the 
current submission, the pending 
timestamp with the later 
dissemination time is applied. 
3 
2022-03-
31T18:30:15Z TERM NOVA 
2022-03-
31T18:30:15Z 20 18 TERM NOVA 1 hour 2022-03-31T19:30:15Z    
4 
2022-03-
31T18:30:15Z EROR   
2022-03-
31T18:30:15Z 21 18 EROR   None 
Calculated: 2022-03-
31T18:30:15Z / Applied: 
2022-03-31T19:30:15Z 
ERORs are not disseminated 
until the time delay expires from 
the last pending submission. 
 
  

---

## Page 20

 
 
5.2:  [[SEC]] Time Delay 
There are no time delays applied to [[SEC]] PPD submissions. 
5.3:  Canada Time Delay 
All Canadian PPD submissions have a 48 hour time delay applied

---

## Page 21

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. The services described herein are provided under the “[[DTCC]]” brand name by 
certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  
Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in 
which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they 
offer. 
Doc Date:  
Publication Code:  
Service:  
Title: 
For More Information 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 