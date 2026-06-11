---
title: "Mutual Fund Scrub File Overview and Best Practice"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_scrub-fund_ack_bp_mfs224_20210708.pdf"
pages: 20
size: "417.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Mutual Fund Scrub File Overview and Best Practice

**Original File:** [net_scrub-fund_ack_bp_mfs224_20210708.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_scrub-fund_ack_bp_mfs224_20210708.pdf)  
**Category:** Other  
**Total Pages:** 20  
**File Size:** 417.1 KB  

---

## Page 1

 
 
 
NETWORKING 
MUTUAL FUND SCRUB FILE OVERVIEW AND BEST PRACTICE 
JULY 8, 2021 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: July 8, 2021 
Publication Code: MFS224 
Service: Networking 
Title: Mutual Fund Scrub File Overview and Best Practice 
 
 
  

---

## Page 3

 
 
REVISION HISTORY 
Revision History 
Effective Date Note 
July 7, 2021 Modified to include a note for clients to go to the Networking 
Technical guide for Pre-Networking Conversion guidance. 
April 26, 2021 Document rebranded and reviewed. 
  

---

## Page 4

 
 
TABLE OF CONTENTS 
Executive Summary ............................................................................................................................................. 5 
Introduction .......................................................................................................................................................... 6 
Fund Requirements .............................................................................................................................................. 7 
SCRUB ............................................................................................................................................................... 7 
FUND ACCOUNT RESPONSE (FAR) ................................................................................................................ 7 
Firm Requirements .............................................................................................................................................. 9 
SCRUB ............................................................................................................................................................... 9 
FUND ACCOUNT RESPONSE (FAR) ................................................................................................................ 9 
SCRUB File Chart ............................................................................................................................................... 10 
Record Layout .................................................................................................................................................... 11 
User Scenario #1 – Scheduled SCRUB File ..................................................................................................... 12 
User Scenario #2 – Ad-Hoc SCRUB File .......................................................................................................... 14 
User Scenario #3 – No Fund Account Response Requested ........................................................................ 15 
User Scenario #4 – Always Send Fund Account Response ........................................................................... 16 
User Scenario #5 – Send Fund Account Response ONLY If... ...................................................................... 18 
 

---

## Page 5

Mutual Fund Scrub File Overview and Best Practice 
Executive Summary 5 
EXECUTIVE SUMMARY 
Potentially, there are several scenarios that could result in a break of non-financial information. For example: 
• firms have noted that non-financial data will be out of sync if/when a fund cannot fully comply with a firm’s 
instructions sent via a Networking B50 or B51, or 
• some funds run audit programs that firms are not aware of to “clean up” account level data 
 
The Investment Company Institute’s Bank, Trust and Recordkeeper Advisory Committee (BTRAC) requested 
that [[DTCC]] develop a programmatic solution with which firms and funds could reconcile static account data 
discrepancies. Both funds and firms should reflect identical information on their books and records. The 
approach utilizes the Networking file structure that includes a “SCRUB Indicator” and a “Fund Account 
Response Indicator”. These indicators identify records specifically designed to assist firms with identifying 
potential breaks of non-financial information. These files will help firms correct the issue with a client’s account 
either at the fund or within their own firm. 
 
NOTE:  
For Pre-Networking Conversion process, please reference the Networking Technical guide. 

---

## Page 6

Mutual Fund Scrub File Overview and Best Practice 
Introduction 6 
INTRODUCTION 
 
The concept of a Mutual Fund SCRUB File was born from a need within the industry to develop a 
programmatic means by which to identify breaks in non-financial information that exist between firms and 
funds. 

---

## Page 7

Mutual Fund Scrub File Overview and Best Practice 
Fund Requirements 7 
FUND REQUIREMENTS 
 
SCRUB 
1. The fund uses the “Scrub Indicator” to identify when a full set of F51 Scrub records are being transmitted 
per the firm’s request.  
Note:  
The firm’s request is done outside the Networking System, while the fund’s response is through the Networking System. The 
full set of F51 Scrub records can be embedded in the  Fund Conversion files or come in a separate file using the DataTrak 
SYSID. Typically, a Scrub file request is for all the firm’s Networked accounts at a particular fund. 
2. The Scrub file (F51 records contain the Scrub Indicator) should be a full set of records (containing all  
possible F51 records). However, Networking will not force that requirement. 
3. Funds should test the procedure in PSE ([[participant]] System Environment) prior to going live, using small 
files or a single security. 
4. The Scrub Indicator and the Fund Account Response Indicator (FAR) should not be populated on normal 
F51 record (e.g. when a fund is updating the firm on a change of non-financial information on one of the 
firm’s Networked accounts. Neither indicator should be populated on any Direct Networking records.) 
5. The Fund Account Response Indicator (FAR) should not be populated on the full set of F51 Scrub 
records. 
6. Since volumes can be potentially high, please coordinate with the firms and [[DTCC]] before sending a Scrub 
file. 
7. Funds will receive Scrub requests outside of the Networking System (usually with a phone call directly 
from the firm). 
8. When sending a Scrub file, the fund must populate the Reference Number. 
9. The Reference Number field is used to give both parties a way of identifying their transactions. It is similar 
to a Control Number in Fund/SERV; however, it is not maintained by [[NSCC]]. It is for firm and fund internal 
use. This unique 11-digit number is used to monitor non-financial transactions. The following convention 
has been adopted by [[NSCC]] for Reference Number generation on conversion records and 
acknowledgments of nonfinancial transactions only. Reference number refers to a [[Member]]-initiated 
Control Number using the standard format: JJJYXXXXXXX where: 
a. JJJ = Julian Date 
b. Y = Last digit of the year 
c. XXXXXXX = Alpha/numeric sequence 
FUND ACCOUNT RESPONSE (FAR) 
1. The fund will use the “Fund Account Response Indicator” to identify when a full set of F51 records are 
being transmitted per the firm’s request.  

---

## Page 8

Mutual Fund Scrub File Overview and Best Practice 
Fund Requirements 8 
Note:  
The firm’s request and the fund’s response are done through the Networking System. The firm’s FAR request is embedded 
within the B50 and B51 records going to the fund. The F51 FAR records can be within the Fund Conversion files or come in 
a separate file, using the  DataTrak SYSID. Unlike a Scrub file, FAR records are sent for only one specific individual 
Networked account. 
2. The FAR record (F51 containing the Fund Account Response Indicator) should be a full set of records for 
the Networked account specified in the firm’s B50/B51 request.  However, Networking will not force that 
requirement. 
3. If the firm sends a B50 or B51 record and has populated the Fund Account Response Indicator with a 
value of 1 (ALWAYS send a F51 FAR record) the fund should generate a full set of F51 records for the 
account and send it to the firm. The fund should echo back the Fund Account Response Indicator value 
submitted by the firm in the original B50/B51. (The fund should also use the same Reference Number 
from the B50/B51 [[Broker]] Conversion/[[Broker]] Update record.) 
4. If the fund cannot complete all of the firm’s requirements on a B50 or B51, and the firm has populated the 
Fund Account Response Indicator with a value 2 (ONLY send a FAR record when the fund could not 
comply with all of a firm’s instructions), the fund should generate a full set of F51 FAR records for that 
specific account only and send it to the firm. The fund should echo back the FAR Indicator value (2) 
submitted by the firm in the original B50/B51. (The fund should also use the same Reference Number 
from the B50/B51 [[Broker]] Conversion/[[Broker]] Update record.) 
5. Funds should test the procedure in the PSE ([[participant]] System Environment) prior to going live, using 
small files or a single security issue. 
6. The Scrub Indicator and the Fund Account Response Indicator (FAR) should not be populated on normal 
F51 record (e.g. when a fund is updating the firm on a change of non-financial information on one of the 
firm’s Networked accounts. Neither indicator should be populated on any Direct Networking records.) 
7. The Scrub Indicator should not be populated on any FAR F51 record. 
8. The fund cannot send a FAR record if the firm did not provide a Reference Number on the original 
B50/B51. 
 
 

---

## Page 9

Mutual Fund Scrub File Overview and Best Practice 
Firm Requirements 9 
 FIRM REQUIREMENTS   
SCRUB 
1. The firm will receive a Scrub file per their request.  
Note:  
There is no separate AutoRoute file designated specifically for Scrub files. The Scrub records (which are a full set of F51 
records with the Scrub Indicator set to 1) will be embedded in the normal Fund Conversion AutoRoute file. 
2. Firms will submit Scrub files requests outside of the Networking System (usually by directly contacting the 
fund). 
3. All firms must be able to recognize the Scrub Indicator value. 
4. Firms should test the procedure in the PSE prior to going live. 
5. Since volumes can be potentially high, please coordinate with the funds and [[DTCC]] before requesting a 
Scrub file. 
FUND ACCOUNT RESPONSE (FAR) 
1. The firm will receive a FAR record (which is a full set of F51 records with a FAR Indicator set to 1 or 2) per 
their request.  
Note:  
There is no separate AutoRoute file designated specifically for FAR records. The FAR records will be embedded in the 
normal Fund Conversion AutoRoute file. 
2. All firms must be able to recognize the Fund Account Response Indicator Value. 
3. Firms should test the procedure in the [[participant]] System Environment (PSE) prior to going live. 
4. The fund cannot send a FAR file if the firm did not provide a Reference Number on the original B50/B51. 
Please note, the fund uses the same Reference Number that is on the [[Broker]]/Conversion Update record. 
 
 
 

---

## Page 10

Mutual Fund Scrub File Overview and Best Practice 
SCRUB File Chart 10 
SCRUB FILE CHART 
 
The chart below describes what values are used by both the Funds and Firms to facilitate processing and 
identification of breaks between Funds and Firms of non-financial information. 
Please note, the Fund Account Response Indicator and Scrub Indicator are mutually exclusive. At least one of 
these fields should be equal to zero or a space on the same record. However, Networking will not force that 
requirement. 
 
  Firm Fund 
Scenario 
 
Examples & Usage 
B50/B51 
Fund Account 
Response 
Indicator 
F51 
SCRUB 
Indicator 
F51 
Fund Account 
Response 
Indicator 
1 Scheduled SCRUB 0 or Space 1 0 or Space 
2 One-OFF SCRUB 0 or Space 1 0 or Space 
3 NO Fund Account Response Requested 0 or Space 0 or Space 0 or Space 
4 ALWAYS Send Fund Account response 1 0 or Space 1 
5 Send a Fund Account Response ONLY if 
fund cannot comply with firm 2 0 or Space 2 
 
 

---

## Page 11

Mutual Fund Scrub File Overview and Best Practice 
Record Layout 11 
RECORD LAYOUT   
The firm uses record type 50 to establish a Networking account at the fund. Record type 51 allows the firm or 
fund to update an existing Networking account. Funds will use record type 51 to send non-financial 
(SCRUB) information. These records must be in sequential order and may be used to set up a cross-
reference file. The file will be sent in the Networking Fund Conversion stream (DataTrak SYSID 26598) along 
with all the other F51 records containing non-financial information. AutoRoute files sent to firms for Fund 
Conversions/Updates (02102084) can contain both SCRUB and non-SCRUB F51 records. The transmission of 
files must adhere to the time frames for Fund Conversion files. 
Account Conversion/Update/SCRUB (B/T50, B/T/F51) #1 Input/Output 
Field Name Start End Len Type Description Opt/Req.  
50/51 
System Code 1 1 1 A/N • A = Investment Agent 
• B = Firm 
• F = Fund 
• T = TPA 
R/R 
Record Type 2 3 2 N • 50 = New Account 
• 51 = Update to Existing Account or 
Scrub                                          or 
Fund Account Response 
R/R 
 
Field Name Start End Len Type Description Opt/Req. 
50/51  
Scrub 
Indicator 
81 81 1 A/N 0 = N/A 
1 = Scrub record. 
1 is allowed for fund input (System Code = F) only 
O/O 
Fund 
Account 
Response 
Indicator 
82 82 1 A/N 0 = Fund should NOT send a Fund Account Response record 
(F51) to the firm. 
1 = Fund should ALWAYS send a Fund Account Response record 
(F51) to the firm. 
2 = Fund should ONLY send a Fund Account Response record 
(F51) to the firm if the fund could not comply with the firm’s 
instructions 
O/O 
 

---

## Page 12

Mutual Fund Scrub File Overview and Best Practice 
User Scenario #1 – Scheduled SCRUB File 12 
USER SCENARIO #1 – SCHEDULED SCRUB FILE 
 
The Firm has made a business decision to request SCRUB records from the fund on a specific schedule. The 
firm contacts each fund representative to set up the scheduled job to provide SCRUB records to the firm. The 
firm and fund agree on the frequency and date(s) for which the fund will transmit F51 SCRUB Records to the 
firm. A scheduled SCRUB file transmission allows Firms and Funds to plan for potential spikes in volume as 
well as provide the Firm with non-financial account data at regular intervals. 
The fund transmits F51s for all firm accounts placing a value of “1” in the SCRUB Indicator field of record #1. 
The file will be sent in the Networking Fund Conversion stream (DataTrak SYSID 26598) along with all the 
other F51 records containing non-financial information. AutoRoute files sent to firms for Fund 
Conversions/Updates (02102084) will contain both SCRUB and non-SCRUB F51 records. The transmission of 
files must adhere to the time frames for Fund Conversion files.  
Account Conversion/Update/SCRUB (F51) #1 Output 
Field Name Start End Len Type Description Opt/Req.  
50/51 
System Code 1 1 1 A/N F = Fund R/R 
Record Type 2 3 2 N 51 = Update to Existing Account, or 
        Scrub 
R/R 
 
Field 
Name 
Start End Len Type Description Opt/Req.  
50/51 
Scrub 
Indicator 
81 81 1 A/N 1 = Scrub record O/O 
Fund 
Account 
Response 
Indicator 
82 82 1 A/N 0 or Space O/O 
 
  Firm Fund 
Scenario 
 
Examples & Usage 
B50/B51 
Fund Account 
Response 
Indicator 
F51 
SCRUB 
Indicator 
F51 
Fund Account 
Response 
Indicator 
1 Scheduled SCRUB 0 or Space 1 0 or Space 
2 One-OFF SCRUB 0 or Space 1 0 or Space 

---

## Page 13

Mutual Fund Scrub File Overview and Best Practice 
User Scenario #1 – Scheduled SCRUB File 13 
  Firm Fund 
3 NO Fund Account Response Requested 0 or Space 0 or 
Space 0 or Space 
4 ALWAYS Send Fund Account response 1 0 or 
Space 1 
5 Send a Fund Account Response ONLY if fund cannot comply 
with firm instructions 2 0 or 
Space 2 
 
 

---

## Page 14

Mutual Fund Scrub File Overview and Best Practice 
User Scenario #2 – Ad-Hoc SCRUB File 14 
USER SCENARIO #2 – AD-HOC SCRUB FILE   
The Firm has made a business decision to request SCRUB records from the fund on a one time only basis. 
The firm contacts each fund representative to set up the ad-hoc job to provide SCRUB records to the firm. The 
firm and fund agree on the specific date on which the fund will transmit F51 SCRUB Records to the firm. 
The fund transmits F51s for all firm accounts placing a value of “1” in the SCRUB Indicator field of record 1. 
The file will be sent in the Networking Fund Conversion stream (DataTrak SYSID 26598) along with all the 
other F51 records containing non-financial information. AutoRoute files sent to firms for Fund 
Conversions/Updates (02102084) can contain both SCRUB and non-SCRUB F51 records. The transmission of 
files must adhere to the time frames for Fund Conversion files. 
Account Conversion/Update/SCRUB (F51) #1 Output 
Field Name Start End Len Type Description Opt/Req.  
50/51 
System Code 1 1 1 A/N F = Fund R/R 
Record Type 2 3 2 N 51 = Update to Existing Account, or 
        Scrub 
R/R 
 
Field Name Start End Len Type Description Opt/Req.  
50/51 
Scrub Indicator 81 81 1 A/N 1 = Scrub record O/O 
Fund Account Response Indicator 82 82 1 A/N 0 or Space O/O 
 
  FIRM FUND 
Scenario 
 
Examples & Usage 
B50/B51 
Fund Account 
Response Indicator 
F51 
SCRUB Indicator 
F51 
Fund Account 
response 
Indicator 
1 Scheduled SCRUB 0 or Space 1 0 or Space 
2 One-OFF SCRUB 0 or Space 1 0 or Space 
3 NO Fund Account Response Requested 0 or Space 0 or Space 0 or Space 
4 ALWAYS Send Fund Account response 1 0 or Space 1 
5 Send a Fund Account Response ONLY if fund 
cannot comply with firm instructions 
2 0 or Space 2 
 

---

## Page 15

Mutual Fund Scrub File Overview and Best Practice 
User Scenario #3 – No Fund Account Response Requested 15 
USER SCENARIO #3 – NO FUND ACCOUNT RESPONSE 
REQUESTED 
 
The Firm has made a business decision not to participate in requesting SCRUB records from the fund at this 
time. In this scenario the firm will ignore the Fund Account Response Indicator by providing a value of ‘0’ or a 
“Space”. 
Account Conversion/Update/SCRUB (F51) #1 Output 
Field Name Start End Len Type Description Opt/Req.  
50/51 
System Code 1 1 1 A/N F = Fund R/R 
Record Type 2 3 2 N 51 = Update to Existing Account  or 
        Scrub 
R/R 
 
Field Name Start End Len Type Description Opt/Req.  
50/51 
Scrub Indicator 81 81 1 A/N 0 or Space O/O 
 
  Firm Fund 
Scenario 
 
Examples & Usage 
B50/B51 
Fund Account 
Response 
Indicator 
F51 
SCRUB Indicator 
F51 
Fund Account 
response 
Indicator 
1 Scheduled SCRUB 0 or Space 1 0 or Space 
2 One-OFF SCRUB 0 or Space 1 0 or Space 
3 NO Fund Account Response Requested 0 or Space 0 or Space 0 or Space 
4 ALWAYS Send Fund Account response 1 0 or Space 1 
5 Send a Fund Account Response ONLY if fund 
cannot comply with firm instructions 
2 0 or Space 2 
 
 

---

## Page 16

Mutual Fund Scrub File Overview and Best Practice 
User Scenario #4 – Always Send Fund Account Response 16 
USER SCENARIO #4 – ALWAYS SEND FUND ACCOUNT 
RESPONSE   
The Firm has made a business decision to request the fund to always send the full set of F51 records each 
time a B50 or B51 is submitted to a fund company. In this scenario the firm would make the request 
programmatically through Networking by placing a value of “1” in the Fund Account Response Indicator field. 
The fund would echo back the value of “1” in the Fund Account Response Indicator field along with the full set 
of F51 records. 
The file will be sent in the Networking Fund Conversion stream (DataTrak SYSID 26598) along with all the 
other F51 records containing non-financial information. AutoRoute files sent to firms for Fund 
Conversions/Updates (02102084) will contain both SCRUB and non-SCRUB F51 records. 
Account Conversion/Update/SCRUB (B/T50, B/T/F51) #1 Input/Output 
Field Name Start End Len Type Description Opt/Req.  
50/51 
System Code 1 1 1 A/N • A = Investment Agent 
• B = Firm 
• F = Fund 
• T = TPA 
R/R 
Record Type 2 3 2 N • 50 = New Account 
• 51 = Update to Existing Account, or 
        Scrub 
R/R 
 
Field Name Start End Len Type Description Opt/ 
Req.  
50/51 
Scrub Indicator 81 81 1 A/N 0 or Space O/O 
 
Field Name Start End Len Type Description Opt/ 
Req. 
50/51 
Fund Account Response 
Indicator 
82 82 1 A/N 1 = Fund should ALWAYS send A Fund 
Account Response record (F51) to 
O/O 
 
 
 

---

## Page 17

Mutual Fund Scrub File Overview and Best Practice 
User Scenario #4 – Always Send Fund Account Response 17 
  Firm Fund 
Scenario 
 
Examples & Usage 
B50/B51 
Fund Account 
Response 
Indicator 
F51 
SCRUB 
Indicator 
F51 
Fund Account 
Response 
Indicator 
1 Scheduled SCRUB 0 or Space 1 0 or Space 
2 One-OFF SCRUB 0 or Space 1 0 or Space 
3 NO Fund Account Response Requested 0 or Space 0 or Space 0 or Space 
4 ALWAYS Send Fund Account response 1 0 or Space 1 
5 Send a Fund Account Response ONLY if fund 
cannot comply with firm instructions 
2 0 or Space 2 
 
 
 

---

## Page 18

Mutual Fund Scrub File Overview and Best Practice 
User Scenario #5 – Send Fund Account Response ONLY If... 18 
USER SCENARIO #5 – SEND FUND ACCOUNT 
RESPONSE ONLY IF... 
 
The Firm has made a business decision to request a full set of F51 records only when the fund was unable to 
fully comply with the request on the B50 or B51. In this scenario the firm would make the request 
programmatically through Networking by placing a value of “2” in the Fund Account Response Indicator field. 
The Fund would echo back the value of “2” in the Fund Account Response Indicator field along with the full set 
of F51 records only if the Fund was unable to fully comply with the request on the B50 or B51. 
The file will be sent in the Networking Fund Conversion stream (DataTrak SYSID 26598) along with all the 
other F51 records containing non-financial information. AutoRoute files sent to firms for Fund 
Conversions/Updates (02102084) can contain both SCRUB and non-SCRUB F51 records. 
Account Conversion/Update/SCRUB (B/T50, B/T/F51) #1 Input/Output 
Field Name Start End Len Type Description Opt/Req. 
50/51 
System Code 1 1 1 A/N • A = Investment Agent 
• B = Firm 
• F = Fund 
• T = TPA 
R/R 
Record Type 2 3 2 N • 50 = New Account 
• 51 = Update to Existing Account, or  
Scrub 
R/R 
 
Field Name Start End Len Type Description Opt/Req.  
50/51 
Scrub Indicator 81 81 1 A/N 0 or Space O/O 
Fund Account 
Response Indicator 
82 82 1 A/N 2 = Fund should ONLY send a Fund Account Response 
record (F51) to the firm if the fund could not comply with 
the firm’s 
O/O 
 
 
 
 
 
 
 

---

## Page 19

Mutual Fund Scrub File Overview and Best Practice 
User Scenario #5 – Send Fund Account Response ONLY If... 19 
  Firm Fund 
Scenario 
 
Examples & Usage 
B50/B51 
Fund Account 
Response 
Indicator 
F51 
SCRUB 
Indicator 
F51 
Fund Account 
response 
Indicator 
1 Scheduled SCRUB 0 or Space 1 0 or Space 
2 One-OFF SCRUB 0 or Space 1 0 or Space 
3 NO Fund Account Response 
Requested 
0 or Space 0 or Space 0 or Space 
4 ALWAYS Send Fund Account response 1 0 or Space 1 
5 Send a Fund Account Response ONLY 
if fund cannot comply 
with firm instructions 
2 0 or Space 2 
 
 
 

---

## Page 20

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 