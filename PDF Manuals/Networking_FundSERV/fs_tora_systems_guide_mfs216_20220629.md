---
title: "ToRA (Transfer of Retirement Assets): Systems Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_tora_systems_guide_mfs216_20220629.pdf"
pages: 19
size: "381.7 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# ToRA (Transfer of Retirement Assets): Systems Guide

**Original File:** [fs_tora_systems_guide_mfs216_20220629.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_tora_systems_guide_mfs216_20220629.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 19  
**File Size:** 381.7 KB  

---

## Page 1

 
 
 
FUND/SERV® 
TORA (TRANSFER OF RETIREMENT ASSETS) SYSTEMS GUIDE 
JUNE 29, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: June 29, 2022 
Publication Code: MFS216 
Service: Fund/SERV
® 
Title: ToRA (Transfer of Retirement Assets): Systems Guide 
 
  

---

## Page 3

 
 
 
CHANGE HISTORY 
Dates Description 
06/29/2022 ToRA Plan Type Matrix in this document has been rebranded. 
Learning upgrade caused some link(s) to break.  Links have been corrected.  
IRS Embedded IRS Rollover Chart did not open.  Replaced with links to IRS 
publication. 
  

---

## Page 4

 
 
TABLE OF CONTENTS 
Introduction to ToRA Systems ........................................................................................................................... 6 
ToRA Systems Overview ...................................................................................................................................... 7 
What Is ToRA? .................................................................................................................................................... 7 
Benefits of ToRA ................................................................................................................................................. 7 
How Does ToRA Work? ...................................................................................................................................... 7 
The Purpose of Industry Standardization ............................................................................................................ 7 
The ToRA Task Force ........................................................................................................................................ 7 
ToRA: Business Guide Best Practices and ToRA Systems Guide ....................................................................... 8 
Best System Practice for Receiving Fund .......................................................................................................... 9 
Best System Practices for ToRA – When Acting as the Receiving Fund ........................................................... 9 
Receive Daily Fund/SERV® Security Issue Master File from [[NSCC]] ................................................................... 9 
Share Class Field on the Fund/SERV® Security Master File ............................................................................... 9 
Validate Minimum and Maximum Purchase Amounts for Partial Transfers ........................................................ 9 
Validate Minimum and Maximum Purchase Amounts for Full Transfers ............................................................. 9 
Perform Standard Edits for the 210 Record ...................................................................................................... 10 
Best Systems Practices for Delivering Fund ................................................................................................... 12 
Best System Practices for ToRA – When Acting as the Delivering Fund ......................................................... 12 
Perform Recommended Hard-Reject Edits ....................................................................................................... 12 
Reject Code for Plan Type Not Compatible ................................................................................................... 12 
Reject Code to Indicate a Stop Code ............................................................................................................. 12 
Perform Recommended Soft-Reject Edits ....................................................................................................... 13 
Reject Codes for Tax [[ID]], Account and Security Issue [[ID]] Validation ............................................................. 13 
Reject Codes for Assets Not Available .......................................................................................................... 13 
Perform an Additional Soft-Reject Edit (Not Recommended) ......................................................................... 14 
Reject Code for Shareholder Name Validation ............................................................................................. 14 
Perform Standard Edits for the 211, 212, 213 Records................................................................................... 14 
Attachments ........................................................................................................................................................ 16 
ToRA Plan Type Matrix ..................................................................................................................................... 16 

---

## Page 5

 
 
Permitted ToRA Plan Type Rollovers ................................................................................................................ 16 
Definition of Terms ............................................................................................................................................ 17 
 

---

## Page 6

ToRA (Transfer of Retirement Assets) Systems Guide 
Introduction to ToRA Systems 6 
INTRODUCTION TO TORA SYSTEMS 
The ToRA Task Force created a Business Guide which recommends and explains best business practices for 
improving the way the Transfer of Retirement Assets (ToRA) system is used. This ToRA Systems guide was 
created to provide high-level technical instruction on how to code service provider and fund company systems. 

---

## Page 7

ToRA (Transfer of Retirement Assets) Systems Guide 
ToRA Systems Overview 7 
TORA SYSTEMS OVERVIEW 
What Is ToRA? 
Transfer of Retirement Assets ("ToRA") is a service offering of the National [[securities]] Clearing Corporation 
("[[NSCC]]"). ToRA enables mutual fund [[Companies]] to jointly initiate, acknowledge, confirm and settle the value of 
mutual fund [[shares]] held in fund- sponsored IRA plans. ToRA is a separate function within Fund/SERV®, the 
industry standard for processing and settling mutual fund orders. 
Benefits of ToRA 
• Automates and minimizes time required for retirement transfer processing to as little as three (3) days 
• Reduces paperwork and phone calls between fund [[Companies]] and shareholders 
• Reduces errors and improves efficiency through the use of a standardized record format 
How Does ToRA Work? 
ToRA processing occurs via a series of records transmitted between a Receiving Fund and a Delivering Fund, 
with [[NSCC]] filtering and passing the data. [[NSCC]] reviews the records to ensure all required information is present 
and correctly formatted. The content of the record must be verified by the Delivering and Receiving Funds. 
The Purpose of Industry Standardization 
The ToRA Task Force 
The Investment Company Institute's ("ICI") [[transfer agent]] Advisory Committee ("TAAC") and the Depository 
Trust Clearing Corporation ("[[DTCC]]") formed a sub- committee focused on improving ToRA processing. The 
ToRA Task Force developed the following objectives: 
• Standardize ToRA use across the industry 
• Substantially reduce the number of rejected ToRA trades 
• Increase cooperation between Fund [[Companies]] 
• Increase ToRA use throughout the industry 
 
These improvements are critical to the efficient Transfer of Retirement Assets process. They also serve to facilitate 
planned expansion of transfer capabilities to include fund-to-[[Broker]] and [[Broker]]-to-fund transactions. 

---

## Page 8

ToRA (Transfer of Retirement Assets) Systems Guide 
ToRA Systems Overview 8 
ToRA: Business Guide Best Practices and ToRA Systems Guide  
The ToRA Task Force created a Business Guide which recommends and explains best business practices for 
improving the way ToRA is used. This ToRA Systems Guide was created to provide high-level technical 
instruction on how to code service provider and fund company systems. 
If all service providers and fund [[Companies]] code their systems according to the best practices defined in this 
document, ToRA trades will no longer reject due to inconsistencies between systems. Rejected trades result in a 
delay in the completion of transfers, which frustrates the shareholder and increases the cost of doing business for 
fund [[Companies]]. 
 

---

## Page 9

ToRA (Transfer of Retirement Assets) Systems Guide 
Best System Practice for Receiving Fund 9 
BEST SYSTEM PRACTICE FOR RECEIVING FUND 
Best System Practices for ToRA – When Acting as the Receiving 
Fund 
Receive Daily Fund/SERV® Security Issue Master File from [[NSCC]] 
Fund [[Companies]] and service providers should ensure their systems are coded to accept the daily version of the 
Fund/SERV® Security Issue Master File (02110802) instead of the Weekly version (02110335). The "802" file is 
created every evening by [[NSCC]] from the Fund/SERV® Security Master File. By accepting the "802" file and 
updating their internal ToRA interfaces daily, fund [[Companies]] and service providers will have the most current 
fund information available for their processing associates, when initiating a ToRA transaction.  Record Layouts 
are available on the Learning Center at https://dtcclearning.com/products-and-services/mutual-fund-
services/record-layouts.html 
Share Class Field on the Fund/SERV® Security Master File  
Both fund [[Companies]] and services providers display the share class information in combination with the fund 
name in their internal ToRA interfaces. This information will allow processing associates to quickly and accurately 
identify the appropriate delivering Security Issue [[ID]] within their ToRA interface, when initiating a ToRA transaction. 
Validate Minimum and Maximum Purchase Amounts for Partial Transfers 
Fund company and service provider internal ToRA interfaces validate ToRA requests for a partial dollar transfer 
against the minimum and maximum purchase requirements for a specific Security Issue [[ID]]. This validation step 
ensures that processing associates can only initiate a partial dollar ToRA transaction for an amount that meets the 
purchase policy for that Security Issue [[ID]]. 
Validate Minimum and Maximum Purchase Amounts for Full Transfers 
Fund [[Companies]] and service providers validate the dollar amount of a "full" transfer, as indicated on the 
acknowledgement (211 record), against the applicable minimum and maximum purchase limits for a particular 
security issue [[ID]].   
If the transaction does not meet these limits, a Fund Exit (214 record) should be generated to the Delivering Fund. In 
addition, one of the following Reject Codes should be returned in the Fund Reject Code field (Receiving Fund Exit 
record 214, record 2 of 2). 
• 710 – Minimum purchase amount not met at Receiving Fund. 
• 711 – Maximum purchase amount exceeded at Receiving Fund. 
 

---

## Page 10

ToRA (Transfer of Retirement Assets) Systems Guide 
Best System Practice for Receiving Fund 10 
Notes 
• The Fund Exit (214 record) must be generated before the confirmation (212 record), to ensure that 
[[settlement]] does not occur for the ToRA transaction. 
• A complete list of reject codes, including those referred to in this document, can be found under 
Codes in the Mutual Fund section of the Learning Center:  https://dtcclearning.com/products -and-
services/mutual -fund-services/codes.html  
• The Fund Exit (214 record) must be generated before the confirmation (212 record), to ensure that 
[[settlement]] does not occur for the ToRA transaction. 
 
 
Perform Standard Edits for the 210 Record 
Fund [[Companies]] and service providers should perform internal edits, prior to generating a ToRA Transaction 
(210 record), to ensure that the transaction is accepted by [[NSCC]]. These edits include: 
• Proper formatting of the ToRA records 
o Physical Sequence Number and Logical Sequence Number 
o Originator Type ("F") 
o Record Type 
o Test Indicator 
o Control Number (must be unique) 
o Submission Date (must equal current date) 
• Valid Receiving Fund information 
o Receiving Fund Number 
o Receiving Plan Type 
• Valid Delivering Fund and Security [[ID]] information 
o Security Issue [[ID]] (validate against the daily "802" Security [[ID]] file) 
o Security [[ID]] is ToRA eligible (validate against the daily "802" Security [[ID]] file) 
o Customer Account Number at Fund 
o Delivering Fund Number 
• Valid transaction information 
o Transaction Type ("0" or "1") 
o Transaction Code ("01", "02", or "03", when the Transaction Type = "1") 
o Money Amount (when the Transaction Code = "03") 
o Share Quantity (when the Transaction Code = "02") 
o Percentage Rate (when the Transaction Code = "01") 
• Valid customer information at Receiving Fund 
o Customer Zip Code 
o Customer Name 
o Customer SSN/EIN 
• [[DO]] not populate these optional fields on any ToRA record: 
o Security Issue Type 

---

## Page 11

ToRA (Transfer of Retirement Assets) Systems Guide 
Best System Practice for Receiving Fund 11 
o Original Roth IRA Date (Exception for Record type 211,212,213 – Required if Delivering Fund Plan 
type = 4 (Roth IRA) or 8 (Roth Conversion IRA) 
o Currency Indicator 
o IRA Withholding Percentage (Exception for Record types 210, 211, 212 213 – Allowed only if 
Receiving Fund Plan Type = 9 (Traditional to Roth Conversion IRA).  
o SSN/EIN Indicator 
 

---

## Page 12

ToRA (Transfer of Retirement Assets) Systems Guide 
Best Systems Practices for Delivering Fund 12 
BEST SYSTEMS PRACTICES FOR DELIVERING FUND 
Best System Practices for ToRA – When Acting as the Delivering 
Fund 
Perform Recommended Hard-Reject Edits 
Reject Code for Plan Type Not Compatible 
Fund [[Companies]] and service providers should code their systems to validate the compatibility of retirement 
plan types by using the Rollover Chart found in IRS Publication 590 (see Section 5). When acting as the 
Delivering Fund, fund [[Companies]] and service providers should validate the account at the Receiving Fund. The 
Delivering Fund should verify that the Receiving Fund has an acceptable plan type that is compatible to the 
plan type on the delivering account. 
If the plan types aren't compatible as outlined in the ToRA Plan Type Matrix, the ToRA transaction should be 
rejected to the Receiving Fund along with reject code: 
• 704 - Plan Type Mismatch 
 
In addition, the correct plan type should be returned to the Receiving Fund populated in the new Delivering 
Fund Plan Type field (Fund Reject record 100, record 2 of 2). 
Note 
Receiving Fund [[Companies]] and service providers should update their reports and internal ToRA interfaces to display the 
plan type that is returned on the Fund Reject (100 record). 
Reject Code to Indicate a Stop Code 
Fund [[Companies]] and service providers should code their systems to validate all Stop Codes on the delivering 
account.  If a Stop Code exists, the ToRA transaction should be rejected to the Receiving Fund with the 
following Reject Code: 
• 709 – Stop Code on account 

---

## Page 13

ToRA (Transfer of Retirement Assets) Systems Guide 
Best Systems Practices for Delivering Fund 13 
Perform Recommended Soft-Reject Edits 
Reject Codes for Tax [[ID]], Account and Security Issue [[ID]] Validation 
 
Fund [[Companies]] and service providers validate certain Critical Data Elements within each ToRA trade: 
• Shareholder Tax [[ID]] (SSN) 
• Shareholder Account at Delivering Fund 
• Shareholder Security Issue [[ID]] at Delivering Fund 
 
ToRA transactions that [[DO]] not meet the Critical Data Element validation should be pended for review. The 
following reject codes should be used: 
• 701 – SSN mismatch. 
• 702 – Account number mismatch. 
• 703 – Account specified not invested in this Security Issue [[ID]]. 
 
The processing associate can review and fix the trade information to allow the transaction to process or reject the 
trade to the Receiving Fund with the applicable new reject codes. 
Reject Codes for Assets Not Available 
Fund [[Companies]] and service providers should validate the requested assets are available. If the assets are not 
available, the ToRA transaction should be pended for review. The following reject codes should be used: 
• 706 – [[shares]] held in escrow. 
• 707 – Uncollected [[shares]]. 
• 708 – Amount requested not available. 
 
The processing associate can review and fix the trade information to allow the transaction to process or reject 
the trade to the Receiving Fund, with the applicable Reject Code.  
In addition, if the transaction is processed and uncollected [[shares]] remain, the uncollected amount should be 
returned to the Receiving Fund in the new Uncollected Share Amount field on the ToRA Acknowledgement 
(record 211, Record 2 of 4). 
Note 
Receiving fund [[Companies]] and service providers should update their reports and internal ToRA interfaces to display the 
Uncollected Share Amount that is returned on the Acknowledgement (211 record). 
 
 

---

## Page 14

ToRA (Transfer of Retirement Assets) Systems Guide 
Best Systems Practices for Delivering Fund 14 
Perform an Additional Soft-Reject Edit (Not Recommended) 
Reject Code for Shareholder Name Validation 
Although not a recommended best practice, fund [[Companies]] and service providers may choose to code their 
systems to attempt to validate the shareholder's name. If the name is not systematically matched between the 
Delivering and Receiving Funds, the ToRA transaction should be pended for review. The following reject code 
should be used: 
• 
705 – Name mismatch 
 
The processing associate can review and fix the trade information to allow the transaction to process or reject 
the trade to the Receiving Fund with this reject code.  
Perform Standard Edits for the 211, 212, 213 Records 
Fund [[Companies]] and service providers sh ould perform internal edits, prior to generating a ToRA 
Acknowledgement, Confirmation or Reconfirmation transaction (211, 212, 213 records), to ensure that the 
transaction is accepted by [[NSCC]]. These edits include:  
• Proper formatting of the ToRA records 
o Physical Sequence Number and Logical Sequence Number 
o Originator Type ("F") 
o Record Type 
o Test Indicator 
o Control Number (from the original transaction) 
o Submission Date (must equal current date) 
• Valid Receiving Fund information 
o Receiving Fund Number 
• Valid Delivering Fund and Security [[ID]] information 
o Security [[ID]] (from the original transaction) 
o Security [[ID]] is ToRA eligible (from the original transaction) 
o Customer Account Number at Fund 
o Delivering Fund Number 
o Delivering Plan Type 
• Valid transaction information (from the original transaction) 
o Transaction Type ("0" or "1") 
o Transaction Code ("01", "02", or "03", when the Transaction Type = "1") 
o Money Amount (when the Transaction Code = "03") 
o Share Quantity (when the Transaction Code = "02") 
o Percentage Rate (when the Transaction Code = "01") 
• Valid customer information at Delivering Fund 
o Customer Zip Code 
o Customer Name 

---

## Page 15

ToRA (Transfer of Retirement Assets) Systems Guide 
Best Systems Practices for Delivering Fund 15 
o Customer SSN/EIN 
• Valid fee and accrual information: 
o Fee Amount 
o Fee Type 
o Accrual Amount 
o Accrual Indicator 
• [[DO]] not populate these optional fields on any ToRA record: 
o Security Issue Type 
o Original Roth IRA Date (Exception for Record type 211, 212, 213 – Required if Delivering Fund Plan 
type = 4 (Roth IRA) or 8 (Roth conversion IRA) 
o Currency Indicator 
o IRA Withholding Percentage (Exception for Record types 210, 211, 212 213 – Allowed only if Receiving 
Fund Plan Type = 9 (Traditional to Roth Conversion IRA).  
o SSN/EIN Indicator 
 

---

## Page 16

ToRA (Transfer of Retirement Assets) Systems Guide 
Attachments 16 
ATTACHMENTS 
ToRA Plan Type Matrix 
ICI [[transfer agent]] Advisory Committee 
ToRA Task Force 
June 2009 
TRANSFER TO 
TRANSFER FROM 
Allowable 
Combinations 
 
IRA 
 
 
IRA 
Rollover 
SEP 
IRA 
Roth 
IRA 
Simple 
IRA 
Coverdell 
Ed. IRA 
SAR-
SEP 
IRA 
Roth 
Conversion 
IRA 
Traditional 
to Roth 
Conversion 
Inherited 
Traditional 
IRA 
Inherited 
Roth IRA 
Inherited 
Roth 
Conversion 
IRA 
IRA Yes Yes Yes          
IRA Rollover Yes Yes Yes          
SEP IRA Yes Yes Yes          
Roth IRA    Yes    Yes Yes    
SIMPLE IRA Yes 
(after 2 
years) 
Yes 
(after 2 
years) 
Yes 
(after 2 
years) 
  
Yes 
       
Coverdell Ed. 
IRA 
     Yes       
SAR-SEP IRA       Yes      
Roth 
Conversion 
IRA 
            
Traditional to 
Roth 
Conversions 
   
Yes    Yes Yes    
Inherited 
Traditional IRA 
         Yes   
Inherited Roth 
IRA 
          Yes  
Inherited Roth 
Conversion 
IRA 
   
        Yes 
 
Permitted ToRA Plan Type Rollovers 
Additionally, please reference IRS Publication 590 which illustrates the various Individual Retirement Plan types 
eligible for rollover.  This publication will provide on rollover information as well as IRS Rollover Chart. 
 
   
 
 
 
 
 

---

## Page 17

ToRA (Transfer of Retirement Assets) Systems Guide 
Attachments 17 
Definition of Terms 
 
 
Term Definition 
Delivering Fund The fund company that delivers retirement plan assets to the Receiving Fund 
via ToRA. 
Receiving Fund The fund company that initiates a ToRA transaction and receives retirement 
plan assets via ToRA from the Delivering Fund. 
ToRA Transfer of Retirement Assets ("ToRA") is a function within [[NSCC]] 
Fund/SERV® that enables mutual fund [[Companies]] to jointly initiate, 
acknowledge,  confirm and settle the value of mutual fund [[shares]] held in 
fund supported retirement plans. 
ICI The Investment Company Institute ("ICI") is the national association of 
U.S. investment [[Companies]], including [[Mutual Funds]], close-end funds, 
exchange-traded funds, and unit investment trusts. 
TAAC The [[transfer agent]] Advisory Committee ("TAAC") is an ICI [[Member]] 
committee that provides a forum to discuss mutual fund [[transfer agent]] 
recordkeeping,  shareholder  servicing, regulatory and compliance related 
matters. 
[[DTCC]] The Depository Trust and Clearing Corporation ("[[DTCC]]"), through its [[NSCC]] 
subsidiary, provides clearing, [[settlement]] and information services for mutual 
fund transactions by linking fund [[Companies]] to their distribution partners. 
[[NSCC]] The National [[securities]] Clearing Corporation ("[[NSCC]]"), a wholly owned 
subsidiary of the [[DTCC]], provides centralized clearance, [[settlement]] and 
information services to fund [[Companies]]. ToRA is one of the [[NSCC]] service 
offerings for mutual fund transaction processing. 
Fund/SERV® A service offering of the [[NSCC]] that provides centralized processing of 
purchase, redemption, and exchange orders, and provides participants with 
a single daily net [[settlement]]. 
Fund Company A fund company establishes a family of [[Mutual Funds]] for distribution to 
investors. Individual [[Mutual Funds]] ("funds" or "Security Issue IDs") have 
different investments objectives and meet varying [[investor]] needs. 
Edit A set of code within a system that identifies data points within a ToRA record 
and reviews for inconsistent information. Edits are what drives ToRA 
requests to a pended or rejected status. 
Daily “805” file  A daily downloadable file produced by [[NSCC]]. This file provides fund 
[[Companies]]' ToRA participation information and includes details on Security 
Issue [[ID]]'s available for ToRA trading. This is the recommended file for 
download, as it provides the most accurate and up- to-date information to 
funds. 
Hard Reject A reject is an instruction to send the trade back through the [[NSCC]] to the 
other Fund without completing the request due to bad data. This is also 
known as a "hard reject." 

---

## Page 18

ToRA (Transfer of Retirement Assets) Systems Guide 
Attachments 18 
Term Definition 
Soft Reject To have a ToRA transaction reviewed by an associate in an attempt to 
resolve questionable data and complete the transaction. Also known as a 
"pended" transaction. 
 
 
 

---

## Page 19

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 