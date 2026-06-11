---
title: "Mutual Fund Services - Interval Funds – Repurchase Processing User Guide & Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs_intervalfunds_repurchase_bp_mfs357_20240201.pdf"
pages: 36
size: "637.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Mutual Fund Services - Interval Funds – Repurchase Processing User Guide & Best Practices

**Original File:** [mfs_intervalfunds_repurchase_bp_mfs357_20240201.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs_intervalfunds_repurchase_bp_mfs357_20240201.pdf)  
**Category:** Other  
**Total Pages:** 36  
**File Size:** 637.4 KB  

---

## Page 1

 
 
 
Mutual Fund Services 
INTERVAL FUNDS – REPURCHASE PROCESSING 
USER GUIDE & BEST PRACTICES 
FEBRUARY 1, 2024 
 

---

## Page 2

 
 
CHANGE HISTORY 
Dates Changes 
February 1, 2024 Rebranded Document.  Document reviewed. 
January 11, 2022 Interval Funds Best Practices Published. 
March 17, 2022 • 3 rd bullet under ‘Role of the Acknowledgment Record’ updated on p. 19 
• Question # 10 updated on p. 23 
• Use Case # 7 updated on p. 33 
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
1. Background ...................................................................................................................................................... 4 
Introduction ......................................................................................................................................................... 4 
Changes .............................................................................................................................................................. 4 
Adoption .............................................................................................................................................................. 4 
2. Summary of Interval Fund Enhancements .................................................................................................... 5 
3. Interval Fund Repurchase Processsing ........................................................................................................ 6 
Updating/Adding Security Issue Type 48 (Interval Fund) in Fund/SERV ........................................................... 6 
Updating a Fund/SERV Security to Security Issue Type 48 (Interval Fund): ................................................... 6 
Adding a New Security Issue Type 48 (Interval Fund) in Fund/SERV: ............................................................. 6 
Updating/Adding Product Type 48 (Interval Fund) in Profile Security ................................................................ 7 
Updating a Security to Product Type ‘Interval Fund’ (48): ................................................................................ 7 
Adding a new ‘Interval Fund’ (48) Security: ...................................................................................................... 7 
Communicating Interval Fund Repurchase Event Schedules & Details............................................................. 8 
Fund/SERV - Future Dated Repurchase Processing ......................................................................................... 8 
Order (001) Record ........................................................................................................................................... 8 
Confirmation (005) Record ..............................................................................................................................10 
Correction (003) Record ..................................................................................................................................11 
Correction Confirm (025) Record ....................................................................................................................13 
Acknowledgement (030) Record .....................................................................................................................14 
4. FAQ’S .............................................................................................................................................................. 17 
5. Appendix – Use Cases ................................................................................................................................... 22 
Use Case Assumptions: ...................................................................................................................................22 
 

---

## Page 4

Interval Funds – Repurchase Processing User Guide & Best Practices 
Background 4 
1. BACKGROUND 
Introduction 
The financial services industry evolves by constantly innovating products and services to meet [[investor]] needs. 
One of these innovations is closed-end “interval” funds. While first permitted as an investment product some 25 
years ago, interval funds are receiving renewed attention from fund [[Companies]] and advisers alike who are 
seeking increased product and portfolio diversification while providing wider access to less -liquid, longer-term 
investments that typically make up interval fund portfolios.  Interval fund assets continue to expand within the 
marketplace, with aggregate assets over $40 billion as of August 2021, up nearly 30% year-over-year.
1  
Interval funds are subject to the same challenges as other financial products—how to provide innovative 
products and service them in a scalable, efficient, and [[investor]]-friendly operating environment. But interval 
funds, with hybrid operating attributes between open-end and closed-end funds, are currently challenged in 
their ability to deliver on these desired characteristics for both interval fund investors and the funds industry.  
The unique operating characteristics of interval funds place stress on current industry capabilities to support 
interval fund operations efficiently and effectively. These headwinds are felt across the servicing environment, 
arising from interval funds’ operational needs that [[DO]] not fully align with prevailing technologies and related 
service models used for either closed- or open-end funds. Disjointed processes, manual strategies to 
compensate for lack of automation, and inefficient processing models are a direct result of these factors.  
Changes 
In conjunction with the [[DTCC]], ICI [[Broker]]/Dealer Advisory Committee (“BDAC”) and the ICI BDAC Interval 
Funds Task Force (“IFTF”), valuable enhancements to [[NSCC]] Fund/SERV® have been identified to enable 
smooth and efficient processing among industry stakeholders. These changes will improve the shareholder 
experience, enable stronger risk management practices, and create greater transparency for 
Firms/intermediaries, Fund [[Companies]], and Service Providers.  This paper describes updates that provide for 
unique identification of Interval Funds as a security type, allow for future-dating of shareholder repurchase 
orders, support pre-confirmation acknowledgement of repurchase orders between Firms and Funds, and 
enable identification of de minimis repurchases as allowed under select Fund Company prospectuses.  
Adoption 
The [[DTCC]], ICI BDAC, and IFTF strongly encourage Fund/SERV participants supporting interval funds to 
consider adopting these enhancements. The operational and efficiency benefits of these changes will be 
directly correlated to the adoption and use by Firms, Fund [[Companies]], and their respective Service Providers.  
Like most changes, stakeholders will adopt the enhancements following different time horizons that consider 
their own business priorities and technology roadmaps. With that in mind and to facilitate effective planning, 
stakeholders are strongly encouraged to connect with their interval fund counterparties (e.g., Firms and Fund 
[[Companies]], Fund [[Companies]] and Service Providers, etc.) to understand implementation strategies, timing, 
and plans. 
 
1 Interval Fund Tracker, “Interval Fund Registrations Surge in 2021”.  https://intervalfundtracker.com/2021/08/17/interval-fund-registrations-surge-in-2021/  

---

## Page 5

Interval Funds – Repurchase Processing User Guide & Best Practices 
Summary of Interval Fund Enhancements 5 
2. SUMMARY OF INTERVAL FUND ENHANCEMENTS 
 
Key Dates Summary of Changes 
Summary of Fund/SERV 
enhancements, effective 
March 28, 2022. 
 
Important Notice a9044 
• New Security Issue Type ‘48 – Interval Fund’ to identify an Interval Fund and allow for 
future dated redemption (repurchase) orders.    
• New Fund/SERV Interval Fund Acknowledgement Record (Record Type 030) to 
allow Funds to notify Firms an Interval Fund repurchase Order (001), or Correction 
(003), has been received.   
• New optional “de-minimis repurchase waiver code” field to the Fund/SERV Order 
(001) and Correction (003) records to allow Firms to indicate the repurchase order is 
eligible for de-minimis treatment in the event of proration, in accordance with the 
Fund’s prospectus. 
• Changes to Fund/SERV ‘Anticipated [[settlement]] Date’ field logic to NOT allow Firms 
to override the [[settlement]] date for a current or future dated Interval Fund repurchase.   
• Changes to Fund/SERV purge rules to allow a future dated Interval Fund repurchase 
Order (001) that is Acknowledged (030) within 10 business days of the submission 
date to remain open for 10 business days after the future Trade Date.   
Summary of MFPS II – Profile 
Security enhancements, 
effective March 28, 2022. 
 
Important Notice a9044 
• New Product Type Code ’48 = Interval Fund’ added to Profile Security to identify an 
Interval Fund. 
 
 

---

## Page 6

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 6 
3. INTERVAL FUND REPURCHASE PROCESSSING 
Updating/Adding Security Issue Type 48 (Interval Fund) in Fund/SERV 
 
For security changes to be effective AFTER the implementation date of the enhancements (March 28, 
2022) - no action is required prior to the implementation date.  Change requests after the implementation date 
would follow the existing process outlined below. 
Updating a Fund/SERV Security to Security Issue Type 48 (Interval Fund):  
1. Requests to update an existing security to Security Issue Type 48 can be submitted by logging in to the 
MyDTCC web portal, selecting the Fund/SERV Modify Form under the Fund/SERV product menu [[Option]], 
and completing the following steps:  
2. In the Security Type section of the form (shown below), select the Interval Fund (48) radio button.  
 
3. Indicate the requested effective date in the ‘Effective Date’ field.  
4. Complete the remaining required fields indicated by an asterisk.  
5. Submit the form for processing.  
 
Note:  
In the event an update is made and there is a need to revert to a previous Security Issue Type, the same procedure as 
outlined above should be followed.  Please contact your [[DTCC]] Relationship Manager for assistance with time sensitive 
requests.  
Adding a New Security Issue Type 48 (Interval Fund) in Fund/SERV:  
Requests to add a new Interval Fund security would follow the process outlined in Steps 1-5 above leveraging 
the Fund/SERV Add Form.  
For security changes to be effective ON the implementation date of the enhancements (March 28, 2022) – 
special accommodations have been made to post the updated Fund/SERV Add and Fund/SERV Modify forms 
to production effective Friday, March 4, 2022.  Commencing on March 4, 2022, follow the steps outlined below 
to request a change be effective on the implementation date.  Requests must be received by March 11, 2022. 
1. Follow the steps outlined above to Update or Add a security.  
2. Ensure the ‘Effective Date’ field on the applicable form is populated with the date of March 28, 2022.  
3. Include the below text in the Special Instructions section:  
“The requested modifications should be effective March 28, 2022 in conjunction with implementation of 
the interval fund enhancements.”  
 


---

## Page 7

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 7 
Considerations: 
Clients should be aware when a security is updated to Security Issue Type 48 (Interval Fund), future dated 
Fund/SERV repurchase orders will be allowed.  It is strongly recommended that Funds not update their 
Interval Fund [[securities]] to Security Issue Type 48 until they are able to accept future dated repurchase orders.  
Prior to adding or updating their [[securities]] to Security Issue Type 48, Funds should communicate planned 
changes to Firms, and Firms should update their systems accordingly.  Following are r ecommended practices 
to facilitate the communication and synchronization of security updates. 
• Funds should communicate to Firms the timing of planned additions or updates to the new Security Issue 
Type 48 (Interval Fund).  Firms should not submit future dated repurchases without confirming the Fund is 
prepared to accept future dated orders through Fund/SERV, as there could be instances where a F und 
has enabled Security Issue Type 48 but is not prepared to accept future dated orders.  
• Funds should utilize [[DTCC]]’s MF Info Xchange ‘Issue’ notification to communicate Fund/SERV Interval 
Fund security additions or changes prior to the effective date, as well as the Fund’s readiness to accept 
future dated repurchases. The Issue notification can be utilized to provide a list of impacted [[securities]] and 
details of when a Fund plans to add or update a security to Security Issue Type 48 (Interval Fund). 
• After a security has been updated to Security Issue Type 48 in Fund/SERV, it will be reflected in the 
‘Security Issue Type’ field in the Fund/SERV Security Master Daily (02110802) and Security Master 
Weekly (02110335) output files.  Firms subscribing to these files should be prepared to receive ‘48’ as a 
new Security Issue Type.  Firms not leveraging these files should consider subscribing to keep apprised of 
security additions and updates. 
Updating/Adding Product Type 48 (Interval Fund) in Profile Security 
Updating a Security to Product Type ‘Interval Fund’ (48):  
Funds should update existing Interval Fund [[securities]] to Product Type ‘Interval Fund’ (48) by logging in to the 
MFPS II - Profile Security (Profile Security) web interface via the MyDTCC web portal and updating the Product 
Type at the Fund Portfolio level by selecting ‘Interval Fund’ from the drop-down list:  
 
Adding a new ‘Interval Fund’ (48) Security:  
Funds can add a new ‘Interval Fund’ (48)’ security by logging in to the Profile Security web interface via the 
MyDTCC web portal and following the existing process for adding a new security.  Detailed information for 
adding a new security can be found in the ‘[[Mutual Funds]] Profile Service II Security Database – Web User 
Guide’ on [[DTCC]] Learning.  


---

## Page 8

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 8 
Considerations: 
• Funds are strongly encouraged to review and update their Interval Fund [[securities]] in Profile Security to 
the new Product Type Code 48 (Interval Fund).  Prior to planned changes, it is strongly recommended 
Funds use the “future dating” capabilities of Profile Security to ensure sufficient notice is provided to Firms 
regarding the effective date.   For more information on the future dating capabilities of Profile Security,  see 
the ‘[[Mutual Funds]] Profile Service II Security Database – Web User Guide’ on [[DTCC]] Learning. 
• Firms should be prepared to receive the new Product Type value of ‘48’ in Record 20 of the Profile 
Security Global (02110824) and Specific (02110825) output files. 
Communicating Interval Fund Repurchase Event Schedules & Details 
Funds should communicate a calendar of Interval Fund repurchase event schedules to Firms as soon as the 
information becomes available, ideally by November for the upcoming year.  Funds are encouraged to 
leverage [[DTCC]]’s MF Info Xchange Interval/Tender Fund Notification to communicate repurchase event 
schedules and the associated details.   MF Info Xchange allows Funds to provide a standardized schedule of 
repurchase events to Firms, which will also be available on the Firms’ calendar through the web interface to 
minimize the chances of missing an event.  Several critical data points (including submission window dates, 
trade date, proration factors, [[settlement]] date) are included.  
Fund/SERV - Future Dated Repurchase Processing 
Order (001) Record  
Following are guidelines for populating key fields for an Interval Fund repurchase order with a future Trade 
Date.   
Field Name Best Practices / Comments 
Security Issue Type Security Issue Type is an optional field for all Security Issue Types with the exception of 24 
(Money Market).  If populated, [[DTCC]] will not utilize the value provided to drive processing 
rules. Processing rules for a security are determined based on the value in the Fund/SERV 
security master file.  If the value provided does not match security master file, [[DTCC]] will not 
reject the submission but will overwrite the field with the value in the security master file on 
output to Funds. 
 
If a repurchase order is submitted with a future Trade Date and the Security Issue Type in the 
Fund/SERV security master file is not = 48 (Interval Fund), [[DTCC]] will reject the trade. 
Transaction Code Only Transaction Codes 03 (Partial [[liquidation]]) and 04 (Full [[liquidation]]) are allowed for a 
future dated Interval Fund order.  If this requirement is not met, [[DTCC]] will reject with existing 
reject code 018 (Transaction Code Missing/Invalid) 
Submission Date Submission Date should be within the repurchase period communicated by the Fund. If the 
Submission Date is not within the repurchase period, Funds should reject the order using 
reject code 101 (Submission date missing/invalid or not equal to Trade Date). 
Trade Date Trade Date should be the Repurchase Pricing Date (NAV strike date) communicated by the 
Fund.  Funds will be responsible to validate the Trade Date is correct.  If the Trade Date is not 
correct, Funds should reject the order using reject code of 016 (Trade Date/Missing invalid). 
 
[[DTCC]] will reject a future dated repurchase order if the Security Issue Type in the Fund/SERV 
security master file is not = 48 (Interval Fund), using reject code 016 (Trade Date/Missing 
invalid). 

---

## Page 9

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 9 
Field Name Best Practices / Comments 
Anticipated [[settlement]] 
Date 
Firms should not populate the ‘Anticipated [[settlement]] Date’ field for current and future dated 
Interval Fund repurchases.  If a Firm populates the Anticipated [[settlement]] Date field on an 
Order (001), [[DTCC]] will not reject the order but will [[default]] the value to 12/31/9999 and pass it 
to the Fund.  When the order is confirmed, the [[settlement]] date for the repurchase will be 
determined based on the [[settlement]] cycle established on the security by the Fund in the 
Fund/SERV security master file; i.e., Trade Date +X  (X = [[settlement]] cycle, or any alternate 
[[settlement]] cycle, established on the security). 
De-minimis repurchase 
waiver code2 
Firms should only populate this field if an Interval Fund repurchase order is eligible for de-
minimis treatment in accordance with the Fund’s prospectus.  It will be up to the Fund to 
determine whether the request will be honored.  [[DTCC]] will only reject the submission if an 
invalid value is provided, using reject code 286 (de-minimis repurchase waiver code is invalid). 
Trade Date Forward 
Indicator 
The Trade Date Forward Indicator for a future dated repurchase order must be populated with 
a 1 (Trade Date Forwarded) or [[DTCC]] will reject with existing reject code 229 (Trade Date 
Forward Indicator missing/invalid).   
 
 
Important Notes: 
• In addition to the key fields referenced above, existing Fund/SERV order processing rules will continue to be 
enforced. 
• Interval Fund repurchase orders that are not future dated follow the same processing rules as Security Types Load 
(25) and No-Load (26), with the exception of Firms not being able to override the [[settlement]] date. 
• Future dated Interval Fund purchases and exchanges are not supported and follow the same processing rules as 
Security Types Load (25) and No-Load (26). 
• Firms should not populate the ‘Anticipated [[settlement]] Date’ field for current and future dated Interval Fund 
repurchases orders. 
• Funds should review and ensure the appropriate [[settlement]] cycles are established on their Interval Fund [[securities]] 
prior to receiving repurchase orders. 
 
Considerations: 
• Funds should ensure the necessary information for Interval Fund security updates and repurchase events 
have been communicated to Firms prior to any future dated repurchase orders being submitted.   
• Funds should send an Acknowledgement (030) record for all Interval Fund repurchase orders, regardless 
of whether the Fund subsequently accepts or rejects the transaction. Please refer to the section on 
Acknowledgements for more details. 
 
2   Some interval funds include prospectus language that waives proration on account closeout repurchases if the account balance is at a de-minimis level (e.g., 
100.000 [[shares]] or less) to enable a clean removal of smaller positions, thereby reducing operating costs for firms, service provid ers, and funds while improving 
small-balance shareholder outcomes. Such exemption may happen automatically, if the fund knows the shareholder’s account balance, or upon request from 
either the shareholder or [[intermediary]] if the account position is part of an omnibus arrangement with the fund.  Firm s should only populate this field on an Order 
(001) when all [[shares]] included in the order represent [[shares]] eligible for de-minimis treatment in accordance with the fund’s prospectus. The share quantity could 
represent one or more shareholder positions so the order could exceed the de -minimis amount. 

---

## Page 10

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 10 
• Firms need to aware of the repurchase event details when populating the below key fields for a future 
dated Interval Fund repurchase order:    
o Security Issue Type field  
If a Firm submits a future dated repurchase order and the security is not defined as Security Issue 
Type 48 (Interval Fund) in the Fund/SERV security master file, [[DTCC]] will reject the order .   
o S ubmission Date  
Firms should only submit repurchase orders during the repurchase period communicated by the 
Fund.  Funds will be responsible for validating the repurchase order was submitted within the 
repurchase period.   
o T
rade Date  
Firms should populate the Trade Date with the Repurchase Pricing Date (NAV Strike Date) 
communicated by the Fund for the applicable repurchase event.  Funds will be responsible for 
validating the Trade Date is correct.   
• Firms should adhere to the best practice of not populating the ‘Anticipated [[settlement]] Date’ field for 
current and future dated Interval Fund repurchases.  In the event a Firm populates the ‘Anticipated 
[[settlement]] Date’ field, [[DTCC]] will pass the value populated in this field along with the value populated in 
the ‘[[settlement]] Override Reason Code’ field since a [[settlement]] Override Reason Code is required when 
the ‘Anticipated [[settlement]] Date’ is populated.   Funds should be prepared to receive an ‘Anticipated 
[[settlement]] Date’ value of 12/31/9999, in conjunction with a ‘[[settlement]] Override Reason Code’ value, in 
these instances. 
 
As previously mentioned, MF Info Xchange, Profile Security, and the Fund/SERV Security Master files 
are tools that can be leveraged to provide the necessary interval fund communication and 
synchronization among counterparties. 
Confirmation (005) Record  
Following are guidelines for populating key fields when confirming an Interval Fund repurchase order with a 
future Trade Date.   
Field Name Best Practices / Comments 
Security Issue Type Security Issue Type is an optional field for all Security Issue Types with the exception of 24 
(Money Market).  If populated, [[DTCC]] will not utilize the value provided to drive processing 
rules. Processing rules for a security are determined based on the value in the Fund/SERV 
security master file.  If the value provided does not match security master file, [[DTCC]] will not 
reject the submission but will overwrite the field with the value in the security master file on 
output to Firms. 
Transaction Code Only Transaction Codes 03 (Partial [[liquidation]]) and 04 (Full [[liquidation]]) are allowed on the 
Confirm for a future dated Interval Fund order.  If this requirement is not met, [[DTCC]] will reject 
with existing reject code 018 (Transaction Code Missing/Invalid). 
Trade Date The Trade Date on the Confirm must match the Trade Date on the order.  If this requirement is 
not met, [[DTCC]] will reject with existing reject code of 016 (Trade Date/Missing invalid). 
 
Note:  
As previously mentioned under the Order (001) Record section, if the Trade Date is not 
correct, Funds should have rejected the order. 

---

## Page 11

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 11 
Field Name Best Practices / Comments 
Trade Date Forward 
Indicator 
The Trade Date Forward Indicator on the Confirm for a future dated repurchase order must = 1 
(Trade Date Forwarded) or [[DTCC]] will reject with existing reject code 229 (Trade Date Forward 
Indicator missing/invalid).   
 
Important Note: 
In addition to the key fields referenced above, existing Fund/SERV confirmation processing rules will continue to be 
enforced.   
 
Considerations: 
• The [[settlement]] date will be determined when the repurchase order is confirmed and will be based on the 
[[settlement]] cycle established on the security by the Fund in the Fund/SERV security master file; i.e., Trade 
Date +X  (X = [[settlement]] cycle, or any alternate [[settlement]] cycle, established on the security).   
• The Confirm (005) record will be populated with the Security Issue Type value in the Fund/SERV security 
master file – clients should be prepared to receive ‘48’ as a new Security Issue Type.  
• On a repurchase Order (001), if a Firm indicated the order was eligible for de-minimis treatment, the 
Confirm (005) record will include the number of [[shares]] tendered, signifying whether the [[shares]] were 
prorated or excluded from proration (if proration is applied to the repurchase offer).   
Correction (003) Record  
Following are guidelines for populating key fields for a correction to an Interval Fund repurchase order.   
Field Name Best Practices / Comments 
Security Issue Type Security Issue Type is an optional field for all Security Issue Types with the exception of 24 
(Money Market).  If populated, [[DTCC]] will not utilize the value provided to drive processing 
rules. Processing rules for a security are determined based on the value in the Fund/SERV 
security master file.  If the value provided does not match security master file, [[DTCC]] will not 
reject the submission but will overwrite the field with the value in security master file on output 
to Funds. 
 
If a repurchase order Correction is submitted with a future Trade Date and the Security Issue 
Type in the Fund/SERV security master file is not = 48 (Interval Fund), [[DTCC]] will reject the 
trade. 
Transaction Code Only Transaction Codes 03 (Partial [[liquidation]]) and 04 (Full [[liquidation]]) are allowed for a 
future dated Interval Fund Correction.  If this requirement is not met, [[DTCC]] will reject with 
existing reject code 018 (Transaction Code Missing/Invalid). 
Submission Date Submission Date should be within the repurchase period communicated by the Fund. If the 
Submission Date is not within the repurchase period, Funds should reject the order using 
reject code 101 (Submission date missing/invalid or not equal to Trade Date). 
Trade Date Trade Date should be the Repurchase Pricing Date (NAV strike date) communicated by the 
Fund.  Funds will be responsible to validate the Trade Date is correct.  If the Trade Date is not 
correct, Funds should reject the Correction using reject code of 016 (Trade Date/Missing 
invalid). 
 
[[DTCC]] will reject a future dated repurchase Correction if the Security Issue Type in the 

---

## Page 12

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 12 
Field Name Best Practices / Comments 
Fund/SERV security master file is not = 48 (Interval Fund) using reject code of 016 (Trade 
Date/Missing invalid). 
 
If the Trade Date is being modified: 
The Trade Date for an Interval Fund repurchase can be corrected to a current Trade 
Date or a future Trade Date, regardless of whether the original order was future dated.  
If the Trade Date is being corrected, the ‘Trade Date Forward Indicator’ field (see below) 
must be populated accordingly. 
 
If the Trade Date is not being modified: 
The Trade Date must match the date on the order.  If the Trade Date is not being 
corrected, the ‘Trade Date Forward Indicator’ (see below) must be populated 
accordingly. 
Anticipated [[settlement]] 
Date 
Firms should not populate the ‘Anticipated [[settlement]] Date’ field for current and future dated 
Interval Fund repurchases.  If a Firm populates the Anticipated [[settlement]] Date field on a 
Correction (003), [[DTCC]] will not reject the order but will [[default]] the value to 12/31/9999 and 
pass it to the Fund.  When the order is confirmed, the [[settlement]] date for the repurchase will 
be determined based on the [[settlement]] cycle established on the security by the Fund in the 
Fund/SERV security master file; i.e., Trade Date+X  (X = [[settlement]] cycle, or any alternate 
[[settlement]] cycle, established on the security). 
Correction Indicator Corrections to future dated Interval Fund repurchases are only supported for pre-[[settlement]] 
corrections (C-N = Pre-[[settlement]] Corrections).   
De-minimis repurchase 
waiver code 
Firms should only populate this field if an Interval Fund repurchase order is eligible for de-
minimis treatment in accordance with the Fund’s prospectus.  It will be up to the Fund to 
determine whether the request will be honored.  [[DTCC]] will only reject the submission if an 
invalid value is provided, using reject code 286 (de-minimis repurchase waiver code is invalid). 
Trade Date Forward 
Indicator 
If the Order (001) being corrected contained a future Trade Date, the Trade Date Forward 
Indicator on the Correction should be populated as follows:  
If the Trade Date will remain the same, Trade Date Forward Indicator must = 1.  
If the Trade Date on the Order (001) is being corrected to either a current Trade Date or 
another future Trade Date, the Trade Date Forward Indicator must = 2.  
Trade Date Forward Indicator = 0 does not apply and is not allowed if the Order (001) was 
future dated. 
 
If the Order (001) being corrected contained a current Trade Date (was not future dated), the 
Trade Date Forward Indicator on the Correction should be populated as follows:  
If the Trade Date will remain the same, Trade Date Forward Indicator must = 0 
If the Trade Date on the Order (001) is being corrected to either a current Trade Date or a 
future Trade Date, the Trade Date Forward Indicator must = 2.  
Trade Date Forward Indicator = 1 does not apply and is not allowed if the Order (001) was not 
future dated.   
 

---

## Page 13

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 13 
Field Name Best Practices / Comments 
If the above conditions are not met, [[DTCC]] will reject with existing reject code 229 (Trade Date 
Forward Indicator missing/invalid).    
 
Note:  
The values on the Correction Confirmation Record (025) must be the same as values on the 
Correction (003) record. 
 
Considerations: 
• Corrections should only be submitted during the repurchase period communicated by the Fund.  Funds 
will be responsible for validating the correction was submitted within the repurchase period.   
• Funds should send an Acknowledgement (030) record for all corrections, regardless of whether the Fund 
subsequently accepts or rejects the transaction. 
• The considerations under the Order (001) section also apply to Corrections. 
 
Important Notes: 
• In addition to the key fields referenced above, existing Fund/SERV correction processing rules will continue to be 
enforced for all future dated Interval Fund repurchase orders. 
• Interval Fund repurchase orders that are not future dated follow the same processing rules as Security Types Load 
(25) and No-Load (26), with the exception of Firms not being able to override the [[settlement]] date. 
• Firms should not populate the ‘Anticipated [[settlement]] Date’ field for current and future dated Interval Fund 
repurchases. 
 
Correction Confirm (025) Record  
Following are guidelines for populating key fields when confirming an Interval Fund repurchase correction.   
Field Name Best Practices / Comments 
Security Issue Type Security Issue Type is an optional field for all Security Issue Types with the exception of 24 
(Money Market).  If populated, [[DTCC]] will not utilize the value provided to drive processing 
rules. Processing rules for a security are determined based on the value in the Fund/SERV 
security master file.  If the value provided does not match security master file, [[DTCC]] will not 
reject the submission but will overwrite the field with the value in the security master file on 
output to Firms. 
Transaction Code Only Transaction Codes 03 (Partial [[liquidation]]) and 04 (Full [[liquidation]]) are allowed on the 
Confirm for a future dated Interval Fund order.  If this requirement is not met, [[DTCC]] will reject 
with existing reject code 018 (Transaction Code Missing/Invalid). 
Trade Date The Trade Date on the Confirm must match the Trade Date on the most recent correction.  If 
this requirement is not met, [[DTCC]] will reject with existing reject code of 016 (Trade 
Date/Missing invalid). 
Trade Date Forward 
Indicator 
The Trade Date Forward Indicator on the Confirm must match the value of the most recent 
correction or [[DTCC]] will reject with existing reject code 229 (Trade Date Forward Indicator 
missing/invalid).   

---

## Page 14

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 14 
Field Name Best Practices / Comments 
Correction Indicator The Correction Indicator must reflect the latest pre-[[settlement]] correction indicator (C-N).  If 
this requirement is not met, [[DTCC]] will reject with existing reject code 006 (Correction Indicator 
missing/invalid).  
 
Important Note: 
In addition to the key fields referenced above, existing Fund/SERV correction confirmation processing rules will continue to 
be enforced.   
 
Considerations: 
• The [[settlement]] date will be determined when the correction is confirmed and will be based on the 
[[settlement]] cycle established on the security by the Fund in the Fund/SERV security master file; i.e., 
Trade Date +X  (X = [[settlement]] cycle, or any alternate [[settlement]] cycle, established on the security).   
• The Correction Confirm (025) record will be populated with the Security Issue Type value in the 
Fund/SERV security master file – clients should be prepared to receive ‘48’ as a new Security Issue 
Type.  
• On a repurchase Correction (003), if a Firm indicated the order was eligible for de -minimis treatment, 
the Correction Confirm (025) record will include the number of [[shares]] tendered, signifying whether the 
[[shares]] were prorated or excluded from proration (if proration is applied to the repurchase offer).   
Acknowledgement (030) Record  
The Acknowledgement Record (030) allows Funds to acknowledge receipt of an Interval Fund repurchase 
order or correction.  The acknowledgement also plays a key role in ensuring a repurchase order remains open 
on the Fund/SERV system to accommodate a future Trade Date.   
The ICI BDAC Interval Fund Task Force viewed consistency in providing an acknowledgement record for every 
Interval Fund repurchase (order and correction) as important, so Firms may automate processes to always 
anticipate an Acknowledgement (030) record prior to or concurrent with confirmation.  This is even the case 
when the Interval Fund repurchase is not future dated (Trade Date is the same as its submission date), where 
an acknowledgement record may be viewed as redundant.   
Acknowledgement of a repurchase order or correction does not indicate the order is in good form.  The 
acknowledgement provides Firms with the confidence their transaction has been received at the Fund; 
however, the order or correction may be rejected by the Fund at any time prior to being confirmed.   
The following Acknowledgement (030) record best practices should be adhered to when a repurchase order, or 
a correction to a repurchase order, is received by the Fund: 
• Funds should acknowledge Interval Fund repurchase orders and corrections (current and future 
dated) in all instances regardless of the proximity to the Trade Date, even if received on Trade Date 
when a confirmation is also being sent. 
• The Fund should send the Acknowledgement (030) record as soon as practicable, preferably the same 
business day as the order is received. 
 
Following are guidelines for populating key fields on the Acknowledgement (030) Record.  
 

---

## Page 15

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 15 
Field Name Best Practices / Comments 
Security Issue Type Security Issue Type is an optional field for all Security Issue Types with the exception of 24 
(Money Market).  If populated, [[DTCC]] will not utilize the value provided to drive processing 
rules. Processing rules for a security are determined based on the value in the Fund/SERV 
security master file.  If the value provided does not match security master file, [[DTCC]] will not 
reject the submission but will overwrite the field with the value in the security master file on 
output to Firms. 
Control Number The Control Number must match the control number of the Order or Correction being 
acknowledged.  If this requirement is not met, [[DTCC]] will reject with existing reject code 005 
(Control Number missing/invalid). 
Correction Indicator Orders: 
The Correction Indicator field should not be populated when acknowledging an Order (001).  
This is important as this field identifies the type of transaction being acknowledged (order vs. 
correction) and also invokes the extended purge window when the order is acknowledged to 
ensure it remains in an open status to accommodate a future Trade Date. 
 
Corrections: 
The Correction Indicator for an acknowledgement of an Order (001) must be blank. The 
Correction Indicator for an acknowledgement of a Correction (003) must reflect the latest pre-
[[settlement]] correction indicator (C-N).  If this requirement is not met, [[DTCC]] will reject with 
existing reject code 006 (Correction Indicator missing/invalid).  
Trade Date Trade Date must match the date on the order or latest correction (if applicable). If this 
requirement is not met, [[DTCC]] will reject with existing reject code 016 (Trade Date/Missing 
invalid). 
 
 
Role of the Acknowledgement Record (030) to accommodate a future dated repurchase order : 
When a Fund submits the Acknowledgement (030) Record for a future dated repurchase Order (001), the 
order will remain open in Fund/SERV for 10 business days after the Trade Date indicated on the order.  If a 
Fund does not acknowledge the repurchase order, it will be purged 10 business days after the submission 
date of the order.    
To ensure future dated Interval Fund repurchase orders remain open to accommodate a future T rade Date: 
• Funds should adhere to the best practice of acknowledging all repurchase Orders (001), regardless of the proximity 
to the Trade Date.   
• When acknowledging a repurchase Order (001), Funds should ensure the ‘Correction Indicator’ field is not 
populated.  This is important as this field identifies the type of transaction being acknowledged (order vs. correction) 
and invokes the extended purge window when the order is acknowledged. 
• If a Correction (003) is accepted by [[DTCC]] prior to a future dated repurchase Order (001) being Acknowledged (030), 
the Correction (003) must be Acknowledged (030) within 10 business days from the Order (001) submission date for 
the order to remain open for 10 business days after the future trade date.  
 
 
Considerations: 
• Firms should be prepared to receive Acknowledgement (030), Confirm (005), and Correction Confirm 
(025) records in different cycles, or within the same output cycle. 
 
• Firms should be prepared to receive ‘48’ as a new Security Issue Type in the Acknowledgement Record.  

---

## Page 16

Interval Funds – Repurchase Processing User Guide & Best Practices 
Interval Fund Repurchase Processsing 16 
 
• If the TPA field is populated on the order, the respective TPA will also receive a copy of the 
Acknowledgement (030) record. 
 
• Funds should adhere to the best practice of acknowledging all Interval Fund repurchase Orders (001). 
  
If a future dated Interval Fund order is not acknowledged via the Acknowledgement (030) record, it will 
be purged from the Fund/SERV system 10 business days after the submission date.  If the future Trade 
Date extends beyond this 10-business day window, the trade will no longer be open on Fund/SERV and 
would have to be resubmitted or processed outside of Fund/SERV.  Further downstream impact could 
result in the trade missing the repurchase period window and not being processed.  Firms will also not 
be provided notice that their repurchase order was received, which may result in manual follow-up. 
Adhering to the best practice of acknowledging all Interval Fund repurchase orders will minimize the risk 
and manual processes mentioned above. 
 

---

## Page 17

Interval Funds – Repurchase Processing User Guide & Best Practices 
FAQ’S 17 
4. FAQ’S 
Adding/Updating Interval Fund Security Issue IDs 
 
1) What steps should Funds follow to update an existing security to an Interval Fund, or add a 
new Interval Fund security to Fund/SERV? 
Please see the Updating/Adding Security Type 48 (Interval Fund) in Fund/SERV section for guidance.  
 
2) After adding or updating a Fund/SERV security to Security Type 48 (Interval Fund), are any 
additional actions required to allow for future dated repurchases to process on Fund/SERV? 
No additional action is required.  When a security is designated as Security Type 48 in the Fund/SERV 
master file, future dated repurchases are automatically allowed. 
 
3) If a Fund updates an existing Fund/SERV Security to Security Type 48 (Interval Fund), how will 
this impact Orders (001) that were accepted by [[DTCC]] prior to the update? 
Orders (001) accepted by [[DTCC]] prior to an update to Security Type 48 will follow the processing and 
[[settlement]] rules of the Security Type at the time the Order (001) was accepted. 
 
4) If a Fund updates an existing Fund/SERV Security to Security Type 48 (Interval Fund), will  
repurchase Orders (001) that are not future dated be allowed? 
Yes, when a security is updated to Security Type 48 (Interval Fund) both current and future dated 
repurchase Orders (001) will be allowed.  Interval Fund repurchase orders that are not future dated follow 
the same processing rules as Security Issue Types Load (25) and No- Load (26), with the exception of 
Firms not being able to override the [[settlement]] date. 
 
Communicating Interval Fund Security Updates and Repurchase Events Details 
 
5) What [[DTCC]] services are available for Funds to communicate Fund/SERV security updates to 
the new Interval Fund Security Issue Type 48?    
It is recommended Funds utilize [[DTCC]]’s MF Info Xchange ‘Issue’ notification to c ommunicate changes 
prior to the effective date.  The Issue notification can be utilized to provide a list of the impacted [[securities]] 
and the details of when a Fund will add or update their [[securities]] to an Interval Fund. 
Prior to planned changes, it is also strongly recommended Funds review and update their I nterval Fund 
[[securities]] in MFPS II - Profile Security (Profile Security) to the new Product Type Code 48 and 
communicate updates through the “future dating” capabilities of Profile Security to ensure sufficient 
notice is provided to Firms regarding the effective date. 
 
 
 
 

---

## Page 18

Interval Funds – Repurchase Processing User Guide & Best Practices 
FAQ’S 18 
 
6) What [[DTCC]] services are available for Funds to communicate Interval Fund repurchase event 
schedules and the associated details?   
 
Funds are encouraged to utilize [[DTCC]]’s MF Info Xchange ‘Interval/Tender Fund’ n otification to 
communicate repurchase event schedules and the associated details to Firms.   MF Info Xchange allows 
Funds to provide a standardized schedule of repurchase events , which will also be available on the 
Firms’ calendar through the web interface to minimize the chances of missing an event.  
In addition to the web interface, Funds and Firms can utilize API calls to systematically submit and ingest 
MF Info Xchange notifications.  
 
Acknowledging an Order (001) or Correction (003) 
 
7) Should Funds acknowledge all Interval Fund repurchase Orders (001) and Corrections (003)?  
Yes, the best practice is for Funds to acknowledge all current and future dated Interval Fund repurchase 
Orders (001) and Corrections (003) via the Acknowledgement (030) record, regardless of the proximity 
to Trade Date. 
 
8) What impact, if any, will there be if a Fund does not acknowledge a future dated Interval Fund 
repurchase Order (001)? 
If a future dated Interval Fund order is not acknowledged via the Acknowledgement (030) record, it will 
be purged from the Fund/SERV system 10 business days after the submission date.  If the future Trade 
Date extends beyond this 10-business day window, the trade will no longer be open on Fund/SERV and 
would have to be resubmitted or processed outside of Fund/SERV.   Further downstream impact could 
result in the trade missing the repurchase period window and not being processed.  
Firms will also not be provided notice that their repurchase order was received, which may result in 
manual follow-up. 
Adhering to the best practice of acknowledging all Interval Fund repurchase orders will minimize risk and 
manual processes mentioned above. 
 
9) What impact, if any, will there be if a Fund does not acknowledge a current dated Interval Fund 
repurchase Order (001)? 
Current dated Interval Fund repurchases follow existing Fund/SERV purge rules and will remain open 
on Fund/SERV for 10 business days after the submission date.  Although there is no impact from a 
Fund/SERV perspective, not acknowledging a current dated order would deviate from the best practice 
of Funds acknowledging both current and future dated Interval Fund repurchase orders.   
Firms will also not be provided notice that their repurchase order was received, which may result in 
manual follow-up. 
 
 
 

---

## Page 19

Interval Funds – Repurchase Processing User Guide & Best Practices 
FAQ’S 19 
10) If a future dated Order (001) was not acknowledged before a Correction (003) was accepted  by 
[[NSCC]], does the Correction (003) need to be acknowledged to extend the purge window? 
Yes, it is imperative that the Correction (003) be acknowledged via the Acknowledged (030) record 
within 10 business days from the Order (001) submission date to extend the purge window to  
accommodate a future Trade Date. 
 
11) Will [[DTCC]] generate reminders to Funds if an Acknowledgement (030) record is not submitted 
for an order or correction? 
No reminders will not be generated if an acknowledgement was not submitted for an order or correction. 
 
12) Will [[DTCC]] only accept an Acknowledgement (030) record for Interval Fund repurchase Orders 
(001) or can other Fund/SERV orders be acknowledged? 
[[DTCC]] will only accept an Acknowledgement (030) record for I nterval Fund (Security Issue Type 48) 
repurchase (redemption) orders.  If an Acknowledgement (030) record is submitted for any other 
security/order type combination, including an Interval Fund purchase, it will be rejected.  
 
Future Dated Fund/SERV Orders 
 
13) If a Fund has not updated their Interval Fund security to Security Issue Type 48 in the 
Fund/SERV master file, will [[DTCC]] reject future dated Interval Fund repurchase orders 
submitted by Firms? 
Yes, the repurchase order would be rejected.  [[DTCC]] will only accept future dated Interval Fund 
repurchase orders if the Security Issue Type in the Fund/SERV master file is = 48.    
 
14) How will Firms be informed if a de-mimimis repurchase waiver request for an order, if 
applicable, was honored by the Fund?  
The Confirmation (005) or Correction Confirmation (025), if applicable, will indicate the number of [[shares]] 
tendered, signifying whether the [[shares]] were prorated or excluded from proration (if proration is applied 
to the repurchase offer).    
 
15) Are future dated Interval Fund purchase and exchanges allowed? 
No, only future dated Interval Fund repurchases are allowed.  Future dated Interval Fund purchases and 
exchange are not supported. 
 
16) If the ‘TPA Number’ field is populated on the order or correction, will a copy of the 
Acknowledgement (030) Record be sent to the TPA. 
Yes, if a Firm populates the TPA Number field on an Order (001) or Correction (003), accepted 
Acknowledgement (030) records will be sent to both the Firm and TPA. 
 
 

---

## Page 20

Interval Funds – Repurchase Processing User Guide & Best Practices 
FAQ’S 20 
17) Will [[DTCC]] generate reminders to Funds if a future dated repurchase order is not confirmed?   
Reminders records (081 and 086) for unconfirmed repurchase Orders (001) and Corrections (003), 
respectively, will be generated daily for up to 10 business days, commencing with the first business 
day after the Trade Date.   
 
18) If an Interval Fund future repurchase order was submitted with a current Trade Date, can the 
Trade Date be corrected to a future date?    
Yes, please see ‘Trade Date’ and ‘Trade Date Forward’ Indicator fields under the Correction Record 
section of this document, in addition to Use Case 10 in the Appendix, for guidance on correcting the 
Trade Date. 
 
19) If an Interval Fund future repurchase order was submitted with a future Trade Date, can the 
Trade Date be corrected to a current date?    
Yes, please see ‘Trade Date’ and ‘Trade Date Forward’ Indicator fields under the Correction Record 
section of this document, in addition to Use Case 11 in the Appendix, for guidance on correcting the 
Trade Date. 
 
20) If a Firm does not plan on submitting future dated repurchase orders today through 
Fund/SERV, are any coding changes required? 
Each client will need to socialize the enhancements with their technology team and/or service provider 
to determine whether changes are required.  When holding these conversations, clients should be 
aware of the following:   
If a Firm does not plan on submitting future dated repurchase orders, it is importa nt to note that the 
best practice is for Funds to acknowledge both current and future dated Interval Fund repurchase 
orders.  Bearing this in mind, if the Security Issue [[ID]] in the Fund/SERV security master file is defined 
as Security Issue Type 48 (Interval Fund), Firms and TPAs (if TPA field is populated on the order) 
should expect Acknowledgement (030), Confirm (005), and Correction Confirm (025) records with ‘48’ 
populated in the Security Issue Type field.    
21) Will Firms be allowed to override the [[settlement]] date on an Interval Fund repurchase order by 
populating the Anticipated [[settlement]] Date field? 
No, Firms will not be allowed to override the [[settlement]] date on a repurchase order –  this is the case 
for both current and future dated repurchases.  If the Anticipated [[settlement]] Date field is populated on 
an Order (001) or Correction (003), [[DTCC]] will not reject the order but will [[default]] the value to 
12/31/9999 and pass it to the Fund along with the value populated in the [[settlement]] Override Reason 
Code field. 
22) How is the [[settlement]] date determined for an Interval Fund repurchase order? 
For current dated and future dated Interval Fund repurchase orders, the [[settlement]] date follows 
existing Order (001) and Correction (003) logic and is calculated based on the future/current Trade 
Date indicated on the order.  When the order is confirmed, the [[settlement]] date is determined based on 
the [[settlement]] cycle established on the security by the Fund in the Fund/SERV security master file; 
i.e., Trade Date+X  (X = [[settlement]] cycle, or any alternate [[settlement]] cycle, established on the 
security). 
 
23) If a Fund has established an alternate [[settlement]] cycle with a Firm for a particular Interval Fund  
security, will the [[settlement]] date be determined based on the alternate settlemen t cycle? 
Yes, any alternate [[settlement]] cycle established on an Interval Fund security will follow existing 
Fund/SERV logic and the [[settlement]] date will be determined based on any alternate [[settlement]] cycle 

---

## Page 21

Interval Funds – Repurchase Processing User Guide & Best Practices 
FAQ’S 21 
established on the security by the Fund. 
 
24) What are the cutoff times for a future dated Interval Fund repurchase Firm Exit (139) or 
Correction (003)?  
The cutoff times follow existing Fund/SERV logic as indicated below: 
• For USD Currency Type, Firm Exits (confirmed and unconfirmed) and Corrections (confirmed and 
unconfirmed) must be received by the cutoff time (11:00am ET - Fund/SERV cycle 14) on the day 
of [[settlement]].   
 
• For USN Currency Type, Firm Exits (confirmed and unconfirmed) and Corrections (confirmed and 
unconfirmed) must be received by 8:00pm ET on the day prior to [[settlement]]. 
 
25) For Firms planning to submit future dated repurchase orders, what actions are required if the 
Trade Date is currently being utilized in the Julian date portion of the Fund/SERV control 
number? 
[[DTCC]] recommends the Julian date portion of the control number reflect the submission date  (see 
below), not the Trade Date.  If a F irm currently utilizes the Trade Date, they should consider modifying 
the process to leverage the submission date.  Not doing so poses the risk of generating duplicate control 
numbers, and subsequently rejected submissions.   
In instances where the Trade Date will continue to be uti lized, to minimize risk of creating a duplicate 
control number Firms will need to develop a process to track the sequent ial number (ssssss) of the last 
future dated trade for a particular date and continue with the next sequential number when the Trade 
Date in question arrives.  As an example, if the Julian date and sequence number part of control number 
272000015 (dddssssss) was used to submit future dated repurchase orders, when the calendar date 
hits 272, the first sequence number for a current dated order on day 272 would be 000016 (000015 +1).  
Control number format is ‘ppppydddssssssc’ where:  
pppp   = Originating [[participant]] (firm/fund/TPA/SP/investment agent) [[NSCC]] number  
y   = Last digit of year  
ddd   = Julian date  
ssssss  = Sequential number  
c   = Check digit  
Note:  
It is recommended that the Julian date 'yddd' reflects the order submission date (so it's easy to create unique control 
numbers). However, Fund/SERV® does not enforce that.  

---

## Page 22

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 22 
5. APPENDIX – USE CASES 
 
The following section provides use cases demonstrating how Interval Fund repurchases would function using 
the enhanced Fund/SERV platform.  
Use Case Assumptions: 
The following use cases will demonstrate Interval Fund repurchase scenarios, and associated outcomes, using 
the enhanced Fund/SERV platform and are based on the following assumptions: 
• Ginormous Interval Fund (Fund): Security Issue [[ID]] 135792468 
o Security Issue [[ID]] profile rules at [[DTCC]] include the following: 
» Interval Fund Security Issue Type = 48 (Interval Fund), which allows future dating of repurchase 
orders. 
» Order is future dated unless otherwise noted (orders that are not future dated would follow 
existing Fund/SERV logic)  
• Repurchase period runs 42 days, from January 12 – February 23, 20XX (determined and communicated 
by the Fund; managed by Fund and [[intermediary]]) 
• Trade Date: February 23, 20XX (all repurchase orders related to the repurchase period will use this Trade 
Date unless otherwise noted) 
• Shareholder of Colossal [[intermediary]] (Firm) submits repurchase order for 2,000.000 [[shares]]  
 
Use Case / Transaction(s) Submitted Use Case Scenario 
Use Case 1 - Order Fund acknowledges order, and subsequently rejects or confirms the 
order on Trade Date. 
Use Case 2 - Order Fund does not acknowledge the order and does not reject or confirm 
the order on Trade Date, resulting in the trade being purged 10 
business days after the submission date. 
Use Case 3 - Order Fund acknowledges the order but does not reject or confirm the order 
on Trade Date, resulting in the trade being purged 10 business days 
after the Trade Date. 
Use Case 4 - Order Fund does not acknowledge the order, but subsequently rejects or 
confirms the order on Trade Date. 
Use Case 5 - Order and Correction 
([[shares]]) 
Fund acknowledges both the order and correction, and subsequently 
rejects or confirms the corrected order on Trade Date. 
Use Case 6 - Order and Correction 
([[shares]]) 
Fund acknowledges the order but does not acknowledge the 
correction, and subsequently does not reject or confirm the corrected 
order on Trade Date, resulting in the trade being purged 10 business 
days after the Trade Date. 
Use Case 7 - Order and Correction 
([[shares]]) 
Fund does not acknowledge the order, but subsequently 
acknowledges the correction within 10 business days of submission of 
the order. 

---

## Page 23

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 23 
Use Case / Transaction(s) Submitted Use Case Scenario 
Use Case 8 - Order and Correction 
([[shares]]) 
Fund acknowledges the order and correction, but subsequently does 
not reject or confirm the corrected order on Trade Date, resulting in the 
trade being purged 10 business days after Trade Date. 
Use Case 9 - Order and Correction 
([[shares]]) 
Fund acknowledges the order but does not acknowledge the 
correction, and subsequently rejects or confirms the corrected order 
on Trade Date. 
Use Case 10 – Order and Correction 
(Trade Date) 
Firm submits a current dated order and subsequently submits a 
correction to change the Trade Date to a future date. 
Use Case 11 – Order and Correction 
(Trade Date) 
Firm submits a future dated order and subsequently submits a 
correction to change the Trade Date to a current date. 
Use Case 12 – Order and Firm Exit Fund acknowledges the order and Firm subsequently submits a Firm 
Exit to cancel the order. 
Use Case 13 – Order Firm submits an order with an invalid Trade Date for the repurchase 
period. 
Use Case 14 – Order Firm submits an order outside of the repurchase window. 
Use Case 15 - Order that is not future 
dated 
Fund does not acknowledge the order, but subsequently rejects or 
confirms the order on Trade Date. 
 
 
  

---

## Page 24

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 24 
Use Case 1 
Firm submits an order February 8, 20XX.  Fund acknowledges the order on February 8, 20XX and 
subsequently either rejects or confirms and processes the order on Trade Date.     
Result: If the Fund confirms the order on Trade Date (February 23, 20XX), [[settlement]] would occur based on 
the Fund’s rules set at [[DTCC]] (e.g., T+1, T+2, etc.). 
 
Key 001 Order Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date February 8, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 1 (Trade Date Forwarded) 
Share Quantity 2,000.0000 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
Key Acknowledgement Record Attributes: 
Control Number Control number for the Order submitted 
Correction Indicator Should not be populated 
Trade Date February 23, 20XX 
Transaction Code Same value as populated on order (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
 
Use Case 2 
Firm submits an order February 8, 20XX (10 business days prior to Trade Date) using same attributes as 
Use Case 1.  Fund fails to acknowledge the order and does not reject or confirm and process the order 
on Trade Date (February 23, 20XX). 
Result: The trade is purged from Fund/SERV on February 23, 20XX. 
• By the Fund failing to acknowledge or confirm the order within 10 business days of submission date, the 
order will purge from Fund/SERV on February 23, 20XX. 
 
• The order will not be included with activity associated with the repurchase window.  
 
 
 

---

## Page 25

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 25 
Use Case 3 
Firm submits an order February 16, 20XX.  Fund acknowledges the order on February 16, 20XX but fails 
to reject or confirm and process the order on Trade Date (February 23, 20XX ).   
Result: The trade is purged from Fund/SERV on March 9, 20XX. 
• By the Fund failing to reject or confirm the order on Trade Date (February 23, 20XX), the order will purge 
from Fund/SERV on March 9, 20XX, which is 10 business days after Trade Date.   
 
• The order will not be included with activity associated with the repurchase window.  
 
Key 001 Order Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date February 16, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 1 (Trade Date Forwarded) 
Share Quantity 2,000.0000 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
Key Acknowledgement Record Attributes: 
Control Number Control number for the Order submitted 
Correction Indicator Should not be populated 
Trade Date February 23, 20XX 
Transaction Code Same value as populated on order (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
 

---

## Page 26

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 26 
Use Case 4 
Firm submits an order February 16, 20XX using the same attributes as Use Case 3.   Fund does not 
acknowledge the order but subsequently rejects or confirms and processes the order on Trade Date 
(February 23, 20XX).  
Result:  If confirmed, [[settlement]] would occur based on the Fund’s rules set at [[DTCC]] (e.g., T+1, T+2, etc.). 
• While not a best practice, failure to acknowledge the order will not affect the order status at [[DTCC]] since 
the order remains open for 10 business days after submission date.  However, the Firm will not have 
assurance that its order has been received by the Fund and that the Fund plans to review its order for 
confirmation and processing on Trade Date. 
 
Use Case 5 
Firm submits an order February 1, 20XX.  Fund acknowledges the order on February 1, 20XX.  Firm 
corrects the order on February 11, 20XX, changing share amount from 2,000.00 to 1,000.00 [[shares]] (the 
correction replaces the original order).  Fund acknowledges the correction. Fund subsequently rejects 
or confirms and processes the corrected order on Trade Date (February 23, 20XX).  
Result:  If confirmed, [[settlement]] would occur based on the Fund’s rules set at [[DTCC]] (e.g., T+1, T+2, etc.).  
Key 001 Order Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date February 1, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 1 (Trade Date Forwarded) 
Share Quantity 2,000.0000 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
Key Acknowledgement Record Attributes for 001 Order: 
Control Number Control number for the order submitted 
Correction Indicator Should not be populated 
Trade Date February 23, 20XX 
Transaction Code Same value as populated on order (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
 
 

---

## Page 27

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 27 
Key 003 Correction Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date February 11, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 1 (Trade Date Forwarded) 
Share Quantity 1,000.0000 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
 
Key Acknowledgement Record Attributes for 003 Correction: 
Control Number Control number for the correction submitted 
Correction Indicator Should be populated with appropriate indicator (C-N) 
Trade Date February 23, 20XX 
Transaction Code Same value as populated on correction (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
Use Case 6 
Firm submits an order February 1, 20XX using the same attributes in Use Case 5.  Fund acknowledges 
the order on February 1, 20XX.  Firm corrects the order on February 16, 20XX changing share amount 
from 2,000.00 to 1,000.00 [[shares]] (the correction replaces the original order).  Fund fails to ac knowledge 
the correction and does not reject or confirm the corrected order on Trade Date (February 23, 20XX). 
Result: The order will be purged from Fund/SERV on March 9, 20XX. 
• By the Fund failing to reject or confirm the corrected order, the order will purge from Fund/SERV on March 
9, 20XX (10 business days after Trade Date). 
 
• The original or corrected order will not be included with activity associated with the repurchase window.  
 
 
 
Use Case 7 
Firm submits an order February 1, 20XX using the same attributes in Use Case 5.  Fund fails to 
acknowledge the order.  Firm corrects the order on February 11, 20XX changing share amount from 
2,000.00 to 1,000.00 [[shares]] (the correction replaces the original order).  Fund acknowledges the 
correction on February 11, 20XX. 
 

---

## Page 28

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 28 
Result:  If confirmed, [[settlement]] would occur based on the Fund’s rules set at [[DTCC]] (e.g., T+1, T+2, etc.).  
• While not a best practice, failure to acknowledge the order will not affect the order status at [[DTCC]] since 
the correction was acknowledged within 10 business days after submission date of the original order.   
 
 
Use Case 8 
Firm submits an order February 5, 20XX.  Fund acknowledges the order on February 5, 20XX.  Firm 
corrects the order on February 16, 20XX changing share amount from 2,000.00 to 1,000.00 [[shares]] (the 
correction replaces the original order).  Fund acknowledges the correction but fails to reject or confirm 
and process the order on Trade Date (February 23, 20XX). 
Result:  The order will be purged from Fund/SERV on March 9, 20XX (10 business days after Trade Date). 
• By the Fund failing to reject or confirm the corrected order, the corrected order will purge from Fund/SERV 
on March 9, 20XX, which is 10 business days after Trade Date. 
• The original order or corrected order will not be included with activity associated with the repurchase 
window. 
 
Key 001 Order Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date February 5, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 1 (Trade Date Forwarded) 
Share Quantity 2,000.0000 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
Key Acknowledgement Record Attributes for 001 Order: 
Control Number Control number for the order submitted 
Correction Indicator Should not be populated 
Trade Date February 23, 20XX 
Transaction Code Same value as populated on order (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
 
 
 

---

## Page 29

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 29 
Key 003 Correction Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date February 16, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 1 (Trade Date Forwarded) 
Share Quantity 1,000.0000 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
Key Acknowledgement Record Attributes for 003 Correction: 
Control Number Control number for the order submitted 
Correction Indicator Should be populated with appropriate indicator (C-N) 
Trade Date February 23, 20XX 
Transaction Code Same value as populated on correction (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
Use Case 9 
Firm submits an order February 5, 20XX using the same attributes as Use Case 8.  Fund acknowledges 
the order on February 5, 20XX.  Firm corrects the order on February 16, 20XX.  Fund fails to 
acknowledge the correction but subsequently rejects or confirms and processes the corrected order 
on Trade Date.   
Result:  If confirmed, [[settlement]] would occur based on the Fund’s rules set at [[DTCC]] (e.g., T+1, T+2, etc.).  
 
• While not a best practice, the failure to acknowledge the corrected order will not affect the order status at 
[[DTCC]]; since the original order was acknowledged, the corrected order will remain open until 10 business 
days after the Trade Date. However, the Firm will not have assurance that its corrected order has been 
received by the Fund and that the Fund plans to review its corrected order for confirmation and processing 
on Trade Date. 
 
Use Case 10 
Firm submits an order on January 19, 20XX that is not future dated.  Fund acknowledges the order on 
January 19, 20XX.  Firm corrects the order on January 20, 20XX, changing the Trade Date from January 
19, 20XX to February 23, 20XX (the correction replaces the original order).  Fund acknowledges the 
correction.  Fund subsequently rejects or confirms and processes the corrected order on Trade Date 
(February 23, 20XX).  
Result:  If confirmed, [[settlement]] would occur based on the Fund’s rules set at [[DTCC]] (e.g., T+1, T+2, etc.).  
 
 

---

## Page 30

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 30 
Key 001 Order Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date January 19, 20XX 
Trade Date January 19, 20XX 
Trade Date Forward Indicator 0 (Trade Date Not Forwarded) 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
Key Acknowledgement Record Attributes for 001 Order: 
Control Number Control number for the order submitted 
Correction Indicator Should not be populated 
Trade Date January 19, 20XX 
Transaction Code Same value as populated on order (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
Key 003 Correction Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date January 20, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 2 (Trade Date being corrected) 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
 
Key Acknowledgement Record Attributes for 003 Correction: 
Control Number Control number for the correction submitted 
Correction Indicator Should be populated with appropriate indicator (C-N) 
Trade Date February 23, 20XX 
Transaction Code Same value as populated on correction (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
 

---

## Page 31

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 31 
 
Use Case 11 
Firm submits an order on February 22, 20XX with a future Trade Date of February 26, 20XX.  Fund 
acknowledges the order on February 22, 20XX.  Firm corrects the order on February 23, 20XX, 
changing the Trade Date from February 22, 20XX to February 23, 20XX (the correction replaces the 
original order).  Fund acknowledges the correction.  Fund subsequently rejects or confirms and 
processes the corrected order on Trade Date (February 23, 20XX).  
Result:  If confirmed, [[settlement]] would occur based on the Fund’s rules set at [[DTCC]] (e.g., T+1, T+2, etc.).  
 
Key 001 Order Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date February 22, 20XX 
Trade Date February 26, 20XX 
Trade Date Forward Indicator 1 (Trade Date Forwarded) 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
Key Acknowledgement Record Attributes for 001 Order: 
Control Number Control number for the order submitted 
Correction Indicator Should not be populated 
Trade Date February 26, 20XX 
Transaction Code Same value as populated on order (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
Key 003 Correction Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date February 23, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 2 (Trade Date being corrected) 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
 
 

---

## Page 32

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 32 
 
Key Acknowledgement Record Attributes for 003 Correction: 
Control Number Control number for the correction submitted 
Correction Indicator Should be populated with appropriate indicator (C-N) 
Trade Date February 23, 20XX 
Transaction Code Same value as populated on correction (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
Use Case 12 
Firm submits an order January 19, 20XX.  Fund acknowledges the order on January 19, 20XX.  Firm 
cancels the trade on February 18, 20XX by submitting a 139 Firm Exit record.   
Result:  The order is cancelled. 
• If the 139 Firm Exit is received and accepted by [[DTCC]] prior to the required cutoff time of 11:00am ET on 
day of [[settlement]] (for USD Currency Type) and 8:00pm ET on day prior to [[settlement]] (for USN Currency 
Type), the trade would be cancelled.   
• The order will not be included with activity associated with the repurchase window. 
 
Key 001 Order Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date January 19, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 1 (Trade Date Forwarded) 
Share Quantity 2,000.0000 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
Key Acknowledgement Record Attributes for 001 Order: 
Control Number Control number for the order submitted 
Correction Indicator Should not be populated 
Trade Date February 23, 20XX 
Transaction Code Same value as populated on order (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 

---

## Page 33

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 33 
 
Key Firm Exit 139 Attributes: 
Control Number Control number for the order submitted 
Correction Indicator Should not be populated 
Trade Date February 23, 20XX 
Submission Date February 18, 20XX 
Transaction Code Same value as populated on order (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
 
Use Case 13 
Firm submits an order January 27, 20XX and designates the Trade Date as January 28, 20XX – one day 
after the order submission date.  The valid Trade Date for this repurchase window is February 23, 
20XX. 
Result: [[DTCC]] would allow this record to pass its edits, since the Trade Date is later than (forward of) the 
submission date.  It would be up to the Fund to edit for a valid Trade Date. Since the valid Trade Date for this 
repurchase window is February 23, 20XX, the Fund would reject the order back to [[DTCC]] with reject code 016: 
Trade Date missing/invalid. 
Key Fund/SERV 001 Order Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date January 27, 20XX 
Trade Date January 28, 20XX 
Trade Date Forward Indicator 1 (Trade Date Forwarded) 
Share Quantity 2,000.0000 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
 
Use Case 14 
Firm submits an order January 11, 20XX, which falls outside the repurchase processing window dates 
of January 12, 20XX - February 23, 20XX. 
Result:  [[DTCC]] would allow this record to pass its edits, since the Trade Date is later than (forward of) the 
submission date.  It would be up to the Fund to edit for a valid submission date.  Since the submission date for 
this repurchase window is any date between January 12, 20XX and February 23, 20XX, the Fund would reject 
the order back to [[DTCC]] with reject code 101: Submission date missing/invalid or not equal to Trade Date.  

---

## Page 34

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 34 
 
Key Fund/SERV 001 Order Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date January 11, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 1 (Trade Date Forwarded) 
Share Quantity 2,000.0000 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
 

---

## Page 35

Interval Funds – Repurchase Processing User Guide & Best Practices 
Appendix – Use Cases 35 
Use Case 15 
 
Firm submits an order February 23, 20XX that is not future dated.  Fund does not acknowledge the 
order but subsequently either rejects or confirms and processes the order on Trade Date (February 23, 
20XX).  
Result:  
 If confirmed, [[settlement]] would occur based on the Fund’s rules set at [[DTCC]] (e.g., T+1, T+2, etc.).  
• While not a best practice, failure to acknowledge the order will not affect the order status at [[DTCC]] since 
the order remains open for 10 business days after submission date.  All orders and corrections should be 
acknowledged by the Fund in all instances regardless of the proximity to the Trade Date, even if received 
on Trade Date when a confirmation is also being sent. 
 
Key 001 Order Attributes: 
Transaction Code 03 (Partial) or 04 (Full) [[liquidation]] (i.e., repurchase to an Interval Fund) 
Submission Date February 23, 20XX 
Trade Date February 23, 20XX 
Trade Date Forward Indicator 0 (Trade Date Not Forwarded) 
Share Quantity 2,000.0000 
Anticipated [[settlement]] Date Should not be provided. If provided, [[DTCC]] will override to 12319999 
 
Key Acknowledgement Record Attributes: 
Control Number Control number for the order submitted 
Correction Indicator Should not be populated 
Trade Date February 23, 20XX 
Transaction Code Same value as populated on order (03 or 04) 
Customer Account Number at Fund or Firm One of the two must be provided 
 
 
 
 

---

## Page 36

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: February 1, 2024 
Publication Code: MFS357 
Service: Mutual Fund Services 
Title: Interval Funds – Repurchase Processing User Guide & Best Practices 
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 
 