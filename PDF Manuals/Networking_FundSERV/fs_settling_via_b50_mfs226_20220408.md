---
title: "Settling Fund/SERV via B50"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_settling_via_b50_mfs226_20220408.pdf"
pages: 7
size: "309.9 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Settling Fund/SERV via B50

**Original File:** [fs_settling_via_b50_mfs226_20220408.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_settling_via_b50_mfs226_20220408.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 7  
**File Size:** 309.9 KB  

---

## Page 1

 
 
 
 
 
FUND/SERV® 
SETTLING FUND/SERV® VIA B50 
APRIL 8, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: April 8, 2022 
Publication Code: MFS226 
Service: Fund/SERV® 
Title: Settling Fund/SERV via B50 
 

---

## Page 3

 
 
CHANGE HISTORY 
Date Changes 
April 8, 2022 Learning upgrade caused some link(s) to break.  Links 
have been corrected. 
April 27, 2021 Rebranded & reviewed. 
 
  

---

## Page 4

 
 
TABLE OF CONTENTS 
Change History ..................................................................................................................................................... 3 
Overview ............................................................................................................................................................... 5 
Best Practices ....................................................................................................................................................... 6 
Networking New Account Record (B50) - Firm ................................................................................................... 6 
Networking New Account Record (B50) – Fund ................................................................................................. 6 
Workflow ............................................................................................................................................................. 6 
 

---

## Page 5

Settling Fund/SERV® via B50 
Overview 5 
OVERVIEW 
This guide provides best practices to systematically settle pending Fund/SERV® orders where the original 
registration received was not in good order. 
A Fund/SERV® registration record (401 or 400) must accompany all orders, where applicable. If for some 
reason the registration rejects, the order remains in a paid and waiting status at the fund.  
When the Fund/SERV® control number is provided along with the new account record, the Fund or their 
service provider can easily identify the outstanding trade and systematically settle the transaction into the 
account, eliminating manual intervention. 
The process outlined below provides an automated solution for a fund to identify an account in a "paid-in-
waiting" status. Having the Fund/SERV® order's Control Number on the B50/B51 Conversion record will help  
identify the account. 
This does not apply to transfers. 
Note: 
The Fund/SERV® Control Number field on the Networking Account Conversion/Update (A/B/T50, A/B/T51) record is 
located on Sequence 3. The complete record layout can be found within the Learning Center at: 
https://dtcclearning.com/products-and-services/mutual-fund-services/record-layouts.html 
 

---

## Page 6

Settling Fund/SERV® via B50 
Best Practices 6 
BEST PRACTICES 
Networking New Account Record (B50) - Firm 
Upon receiving the Fund/SERV® registration reject (114) from the fund, the firm should generate a Networking 
new account (B50) record back to the fund. The B50 should include the Fund/SERV® control number that 
relates to the outstanding trade. 
This same process can also be applied to corrections (003) records for a new account where the registration 
rejects. 
Networking New Account Record (B50) – Fund 
Upon receiving the Networking new account (B50) record from the firm, the fund should attempt to create the 
new account. If the record also contains the optional Fund/SERV® control number, the fund should attempt     
to settle the outstanding order into the new account systematically. 
B50 records that include a control number where the fund finds an existing account can be used to settle the 
trade into the account systematically. 
B50 records that include a control number where the fund is unable to find a match should not be rejected. The 
fund should accept the new account and report that the control number was invalid internally. 
Workflow 
Adding Fund/SERV® Control Number to Networking B50 Record 


---

## Page 7

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 