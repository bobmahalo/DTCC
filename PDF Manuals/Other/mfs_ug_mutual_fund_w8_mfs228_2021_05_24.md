---
title: "MUTUAL FUND W8 USER GUIDE"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs_ug_mutual_fund_w8_mfs228_2021_05_24.pdf"
pages: 8
size: "292.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MUTUAL FUND W8 USER GUIDE

**Original File:** [mfs_ug_mutual_fund_w8_mfs228_2021_05_24.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs_ug_mutual_fund_w8_mfs228_2021_05_24.pdf)  
**Category:** Other  
**Total Pages:** 8  
**File Size:** 292.6 KB  

---

## Page 1

 
 
 
MUTUAL FUND SERVICES 
MUTUAL FUND W8 USER GUIDE 
MAY 24, 2021 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: May 24, 2021 
Publication Code: MFS228 
Service: Mutual Fund Services 
Title: Mutual Fund W8 User Guide 
 
 
  

---

## Page 3

 
 
 
CHANGE HISTORY 
 
Date Changes 
05/24/2021 Rebranded & content reviewed 
 
 

---

## Page 4

 
 
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 5 
Purpose ............................................................................................................................................................... 5 
About W8 ............................................................................................................................................................ 5 
Introduction ........................................................................................................................................................ 5 
Fields/Values ........................................................................................................................................................ 6 
Introduction ........................................................................................................................................................ 6 
 

---

## Page 5

Mutual Fund W8 User Guide 
 
Overview 5 
OVERVIEW 
Purpose 
The purpose of this guide is: 
• To familiarize [[NSCC]] members, which includes but is not limited to, [[Mutual Funds]], insurance [[Companies]], 
brokerage firms, dealers and trading partners participating in the mutual fund services, with the IRS 
(Internal Revenue Service) regulations regarding NRA (Non-Resident Alien) mutual fund accounts. 
About W8 
Introduction 
The primary purpose of this section is to familiarize Participants with the Internal Revenue Service regulations 
for W8 registrations. 
The NRA regulations require that each registered holder that is foreign submit one of the following W-8 forms: 
1. W-8BEN. Used by individuals (‘[[Beneficial Owner]]’) to identify foreign person status and, if applicable, to 
claim treaty benefits reducing the withholding rate. 
2. W-8IMY. Used by a foreign payee not the [[Beneficial Owner]] of the income (e.g., omnibus or corporate 
registration) to make representations regarding the status of the beneficial owners as to treaty reduction 
eligibility. Within this category are two types of Intermediaries – those considered Qualified (have a 
withholding agreement with the IRS that correct documentation of the underlying owner eligibility has been 
received). The other type is a Non-Qualified [[intermediary]], requiring that the documentation for the 
underlying owner(s) must be provided to the Withholding Agent. 
3. W-8ECI. Used by foreign persons to claim Exemption from Withholding on ‘Income effectively connected 
with the conduct of a trade business in the United States’.  This certification exempts the account from all 
NRA withholding as the income must be reported on 1040NR (by the owner) and taxed at federal income 
rates, and this form type requires an ITIN to be submitted. Note that all ITINs have ‘98’ as the first two 
digits of the number. 
4. W-8EXP. Used by foreign governments, or other foreign organizations and, if applicable, to claim reduced 
rate treaty benefits.
 

---

## Page 6

Mutual Fund W8 User Guide 
 
Fields/Values 6 
FIELDS/VALUES 
Introduction 
The fields and values listed in this document are used to communicate W8 information. 
Field Value 
Withhold Indicator Similar to the W9 indicator, the W8 indicator tells the fund what the status of the 
foreign account is. W8 values available: 
 
A = Uncertified foreign account (no W8 form on file-backup withholding necessary)  
B = Certified foreign [[Beneficial Owner]] account (form W8-BEN on file)  
C = Certified foreign [[intermediary]] account (form W8-IMY on file)  
D = Certified valid foreign account (form W8-ECI on file with ITIN)  
E = Certified foreign exempt account (form W8-EXP on file)  
F = W8 on file - no treaty rate claimed  
G = W8 Beneficiary with TIN on file 
H = W-8BEN-E on file/documentary evidence 
I = Voluntary FATCA withholding - W-8BEN-E on file/documentary evidence 
J = W8-IMY or W-8BEN-E pending 
 
Country of Origin The Country of Origin indicates the country of permanent residence as noted on the 
W8 form. 
 
If the Withhold Indicator = F (W8 on file - No Treaty Rate Claimed) or if Withhold 
Indicator = A (Uncertified Foreign Account - no W8 form on file - backup withholding 
necessary), then the Country of Origin field is not required. The understanding is that 
the fund will withhold at the highest rate. 
 
The Country of Origin is required when any other W8 indicator is used. The fund uses 
this code to apply the proper NRA tax rate on the account. For this reason, a value of 
"OC" (for "Other Country") in the Country of Origin field is not acceptable. 
W8 Override Country Code The W8 Override Country Code and W8 Override Special NRA Rate fields are used 
to accommodate a Special Treaty benefits on the W8 form. The W8 Override Country 
Code field can be used if the country code differs from the Country Code of Origin 
designated on the W8 form. 
W8 Override Special NRA 
Rate 
Brokers indicating a zero in the W8 Override Special NRA Rate field want the fund to 
withhold nothing. They want this in the case of a level 3 Networked account. Level 3 
accounts typically have their withholding done at the fund with the [[Broker]] doing the tax 
reporting. The [[Dividend]] file itself produces the appropriate breakout (TEFRA) depending 
on the Networking level. For level 3 accounts, the fund remits both the withholding 
amount and the distribution account to the [[Broker]]. 

---

## Page 7

Mutual Fund W8 User Guide 
 
Fields/Values 7 
Field Value 
W8 Certification Date W8's have an Expiration Date and a Certification Date associated with them. 
 
The Certification (Start) and Expiration Dates are required whenever the W8 indicator 
specifies a Certified Foreign account. The exceptions are if the Withhold Indicator = F 
(W8 on file - No Treaty Rate Claimed) or if Withhold Indicator = A (Uncertified Foreign 
Account-no W8 form on file- backup withholding necessary). 
W8 Expiration Date This field is required when the Withhold Indicator field is  
D = Certified valid foreign account (form W8-ECI on file with ITIN)  
E = Certified foreign exempt account (form W8-EXP on file)   
 
[[NSCC]] will edit both fields for valid dates. [[NSCC]] will not change any erroneous dates. It 
is up to the fund to determine the validity of the dates. 
W9 Values Funds and transfer agents have been receiving registrations containing W9 values for 
true foreign accounts and W8 values for U.S. citizens. An U.S. citizen living abroad 
should be coded as a domestic account and have W9 values. The value of "OC" is 
acceptable in this instance. 
 
A true NRA account should not have a W9 value. Brokers should use a W8 value of "D" 
or "E" to specify no withholding since these  are considered exempt accounts. 
 
 
 

---

## Page 8

Mutual Fund W8 User Guide 
 
Fields/Values 8 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 