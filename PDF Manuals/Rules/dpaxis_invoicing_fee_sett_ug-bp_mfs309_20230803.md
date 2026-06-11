---
title: "dpaxis_invoicing_fee_sett_ug-bp_mfs309_20230803.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dpaxis_invoicing_fee_sett_ug-bp_mfs309_20230803.pdf"
pages: 50
size: "818.1 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# dpaxis_invoicing_fee_sett_ug-bp_mfs309_20230803.pdf

**Original File:** [dpaxis_invoicing_fee_sett_ug-bp_mfs309_20230803.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/dpaxis_invoicing_fee_sett_ug-bp_mfs309_20230803.pdf)  
**Category:** Rules  
**Total Pages:** 50  
**File Size:** 818.1 KB  

---

## Page 1

 
 
 
[[DTCC]] Payment aXis® 
CHAPTER 2: INVOICING AND FEE [[settlement]] 
USER GUIDE/BEST PRACTICES 
AUGUST 3, 2023 
 

---

## Page 2

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Invoicing and Fee [[settlement]] 2 
REVISION HISTORY 
Date Revisions 
August 3, 2023 Document rebranded. Content reviewed and refreshed. 
March 23, 2022 Learning upgrade caused some links to break.  These are now corrected. 
April 1, 2020 Guide was refreshed due to rebranding; links repointed to Learning. 

---

## Page 3

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Invoicing and Fee [[settlement]] 3 
TABLE OF CONTENTS 
Invoicing and Fee [[settlement]] ............................................................................................................................. 6 
Getting Started ..................................................................................................................................................... 7 
How [[DO]] I Sign Up? ............................................................................................................................................. 7 
Eligibility .............................................................................................................................................................. 7 
Datatrak & Autoroute IDs .................................................................................................................................... 8 
Record Layouts and Transmission Schedules ................................................................................................... 8 
General [[DTCC]] Payment aXis Invoice Information ............................................................................................ 9 
Benefits ............................................................................................................................................................... 9 
[[NSCC]] Validation ................................................................................................................................................. 9 
Transmission Times ............................................................................................................................................ 9 
Records .............................................................................................................................................................10 
“Rate” Field–Best Practice ................................................................................................................................10 
Control Number .................................................................................................................................................11 
[[settlement]] .........................................................................................................................................................12 
Use of Modify Functionality vs. Partial Reject ..................................................................................................13 
Anticipated [[settlement]] Date .............................................................................................................................13 
Zero Dollar Invoices ..........................................................................................................................................14 
Sub-Accounting 12b-1/Shareholder Service Fee (Type 50) ........................................................................... 15 
Firm Invoice ......................................................................................................................................................15 
Fund Response Structure .................................................................................................................................16 
Fund Response-Confirm the Invoice ................................................................................................................16 
Fund Response-Reject the Invoice...................................................................................................................17 
Fund Response-Release to [[settlement]] ............................................................................................................17 
Examples ..........................................................................................................................................................19 
[[settlement]] .........................................................................................................................................................19 
Transactional Fees -CDSC/[[Underwriting]] Fee Adjustment/Short- Term Redemption/Finder’s Fee 
Adjustment: [[Broker]] Invoice-Fee Types 51, 52, 53, 54 .................................................................................... 20 
[[Broker]] Invoice ...................................................................................................................................................20 
Examples ..........................................................................................................................................................21 

---

## Page 4

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Invoicing and Fee [[settlement]] 4 
[[settlement]] .......................................................................................................................................................21 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) .............................................................................. 23 
Sub-Accounting Service Fee (Fee type 55) vs Retirement/Bank Trust Service Fee (Fee Type 56)  ................23 
Sub-Accounting Service Fee–Fee Type 55 ......................................................................................................23 
Firm Invoice .....................................................................................................................................................23 
Fund Response ...............................................................................................................................................24 
Fund Response-Confirm the Invoice .............................................................................................................24 
Fund Response–Confirm with Modification ...................................................................................................25 
Fund Response–Confirm with Partial Rejection ............................................................................................25 
Modify vs. Partial Reject ................................................................................................................................26 
Fund Response-Reject the Invoice ...............................................................................................................26 
Fund Response-Release to [[settlement]].........................................................................................................27 
Examples .........................................................................................................................................................29 
[[settlement]] .......................................................................................................................................................29 
Retirement/Bank Trust Service Fee–Fee Type 56 ...........................................................................................29 
Firm Invoice .....................................................................................................................................................29 
Fund Response ...............................................................................................................................................31 
Fund Response-Confirm the Invoice .............................................................................................................31 
Fund Response–Confirm with Modification ...................................................................................................32 
Fund Response–Confirm with Partial Rejection ............................................................................................32 
Modify vs. Partial Reject ................................................................................................................................33 
Fund Response-Reject the Invoice ...............................................................................................................34 
Fund Response-Release to [[settlement]].........................................................................................................34 
Examples .........................................................................................................................................................37 
[[settlement]] .......................................................................................................................................................37 
Networking Service Fee–Fee Type 57 .............................................................................................................37 
Flow 1–Firm Initiated Invoice...........................................................................................................................37 
Firm Invoice ...................................................................................................................................................37 
Fund Response .............................................................................................................................................38 
Fund Response-Confirm the Invoice .............................................................................................................38 

---

## Page 5

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Invoicing and Fee [[settlement]] 5 
Fund Response–Confirm with Modification ...................................................................................................39 
Fund Response–Confirm with Partial Rejection ............................................................................................40 
Modify vs. Partial Reject ................................................................................................................................40 
Fund Response-Reject the Invoice ...............................................................................................................41 
Fund Response-Release to [[settlement]].........................................................................................................41 
Examples .........................................................................................................................................................42 
[[settlement]] .......................................................................................................................................................42 
Fund Initiated Remittance File (Flow 2) ..........................................................................................................42 
Fund Initiated Remittance File .......................................................................................................................42 
Examples .........................................................................................................................................................43 
[[settlement]] .......................................................................................................................................................43 
Testing ................................................................................................................................................................. 45 
Frequently Asked Questions ............................................................................................................................ 46 
Glossary .............................................................................................................................................................. 49 
 

---

## Page 6

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Invoicing and Fee [[settlement]] 6 
INVOICING AND FEE [[settlement]] 
Prior to the early 2000’s, few firms held consolidated client positions in mutual fund [[Companies]] in a single 
omnibus account. Since that time, more firms have converted to omnibus processing as a fund distribution 
model and the corresponding increase in, and variety of, distribution and sub- accounting fee arrangements 
have created a complex invoicing process for both firms and funds. As firms convert accounts fr om [[Broker]] 
Controlled Network level 3 accounts and/or individual client level accounts held on the fund’s books to firm 
level omnibus accounts, funds no longer have access to individual customer account activity and balances. 
Payments, such as 12b-1’s, previously calculated by the funds and paid to firms are now calculated by firms 
and invoiced to funds. 
Prior to [[NSCC]] creating Omnibus Invoicing functionality, in conjunction with the ICI [[Broker]]/Dealer Advisory 
Committee and the Bank, Trust and Retirement Advisory Committee, invoice processing was manually 
intensive and typically involved the exchange of reports and spreadsheets via fax, email, or regular mail. The 
[[settlement]] of invoices typically occurred by check, wire or ACH. Invoice processing was costly and inefficient, 
lacking standardization and industry-wide automation. 
In 2013 [[NSCC]] enhanced the existing Mutual Fund Commission [[settlement]] platform (renamed to [[DTCC]] 
Payment aXis
®) by creating the Omnibus Invoicing functionality (Important Notice a7512). This functionality 
enables firm invoicing and [[settlement]] to be facilitated through an existing automated platform. With the addition 
of Omnibus Invoicing functionality, [[NSCC]] has provided an automated solution to the exchange of Omnibus 
invoices and the [[settlement]] of various fees. 
In 2014 “Omnibus Invoicing” fee category was renamed to “Invoicing and Fee [[settlement]]”. “Non- Omnibus” fee 
category (previously known as “Commission [[settlement]]”) was renamed to “Commission and Fee [[settlement]]”. 
These labels were created to better categorize the types of fees supported by each category. 
This guide is intended for clients interested in utilizing the “Invoicing and Fee [[settlement]]” service
1. For 
information regarding “Commission and Fee [[settlement]]” functionality, please reference “ [[DTCC]] Payment aXis–
Commission and Fee [[settlement]] User Guide”. 
Invoicing and Fee [[settlement]] platform supports the following invoice fee types: 
Fee Type Description 
50 Sub-Accounting 12b-1/Shareholder Service Fee * 
51 Sub-Accounting CDSC 
52 Sub-Accounting [[Underwriting]] Fee Adjustment 
53 Sub-Accounting Short Term Redemption 
54 Sub-Accounting Finder’s Fee Adjustment 
55 Sub-Accounting Service Fee 
56 Retirement/Bank Trust Service Fee 
57 Networking Service Fee 
* This is not a record keeping fee, but rather an [[Asset]]-based 12b-1 or similar fee. 
For further information on historical modifications to the service please refer to the following important notices: 
a7464, a7510, a7512, and a7885. 
 
1 This guide should be used in conjunction with the Record Layouts located on www.dtcclearning.com under the Mutual Fund Services Record Layouts. 

---

## Page 7

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Getting Started 7 
GETTING STARTED 
How [[DO]] I Sign Up? 
In order to participate in the Invoicing and Fee [[settlement]] service, clients are required to sign up for activation 
to the service(s) they are interested in: 
• Omni Invoicing 12b-1/Service Fees 
• Omni Invoicing Transactional Fees-CDSC/[[Underwriting]] Fee Adjustment/Short Term Redemption/Finder’s 
Fee Adjustment–signing up for this service indicates participation in all 4 fee types 
• Omni Invoicing Sub-Accounting Service Fee 
• Retirement/Bank Trust Service Fee 
• Networking Service Fee 
Note: 
Clients utilizing [[DTCC]] Payment aXis® for Mutual Fund Commission and Fee [[settlement]] will still need to sign up for the 
applicable Invoicing and Fee [[settlement]] file(s). 
Clients will also need to sign up for the applicable Datatrak and Autoroute IDs (see  Datatrak & Autoroute IDs). 
To sign up for the Invoicing service, please contact your Relationship or Account Management Team at 212-
855-8877.   
Eligibility 
Clients may register for any combination of services that they choose to utilize.  
As an example, a firm may choose to register for [[DTCC]] Payment aXis, Omni-Invoicing 12b-1/Service fees and 
Networking Service Fee while another firm may choose to register for [[DTCC]] Payment aXis ® and Sub-
Accounting Service Fees. 
[[NSCC]] does not create and maintain eligibility information by counterparty. [[NSCC]] will report the eligibility by 
client information. For new clients, information on who is subscribing to this service can be found on the [[DTCC]] 
website (see List of Mutual Fund Products Utilized by Firm and Funds):  https://www.[[DTCC]].com/wealth-
management-services/mutual-fund-services/mutual-funds-client-public-documentation  
Firms are expected to review the listing to determine participating funds and should communicate with their 
counterparties prior to transmitting information to the fund. Funds and firms should work together to create a 
schedule for testing and processing the invoicing files. An invoice submitted for a client that is not eligible for 
the service will be rejected by [[NSCC]] to the submitter. 
Note: 
If a client has signed up for the service, all of its Security Issue IDs are considered eligible for this service. 
Available Services: 
• [[DTCC]] Payment aXis 
• 12b-1 Service Fee 
• CDSC/[[Underwriting]] Fee Adjustment/Short Term Redemption/Finder’s Fee Adjustment  
• Sub-Accounting Service Fee 
• Retirement/Bank Trust Service Fee 
• Networking Service Fee 

---

## Page 8

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Getting Started 8 
Datatrak & Autoroute IDs 
In order to send and receive Invoicing and Fee [[settlement]] files clients will need to sign up for the following 
Datatrak and Autoroute IDs: 
• Invoicing and Fee [[settlement]] DataTrak Sysid 26947 (Production) and 46947 (PSE)  
• Invoicing and Fee [[settlement]] AutoRoute 02101947 (Production) and 02981947 (P SE) 
• *Commission and Fee [[settlement]] Summary MRO Autoroute 02102203 (Production) and 02982203 (PSE)  
 
*[[DTCC]] Payment aXis® [[settlement]] Files 38, 39, 40 will be sent out by [[NSCC]] via this Autoroute [[ID]]. 
 
Record Layouts and Transmission Schedules 
The most recent record layouts can be found under [[DTCC]] Payment aXis tab on Learning Center at the 
following link: 
https://dtcclearning.com/products-and-services/mutual-fund-services/record-layouts.html 
To view the Transmission Schedule please see [[DTCC]] Payment aXis Time Schedule on Learning at the 
following link:  
https://dtcclearning.com/documents/mutual-fund-services-1/[[DTCC]]-payment-axis/schedules1-5/1808-[[DTCC]]-
payment-axis-time-schedule/file.html 
 
  


---

## Page 9

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
General [[DTCC]] Payment aXis Invoice Information 9 
GENERAL [[DTCC]] PAYMENT AXIS INVOICE 
INFORMATION 
Benefits 
The creation of a standard fee invoicing file: 
• Automates and standardizes firm-initiated invoices and data to funds. 
• Allows firms choosing to transmit sub-account information to the funds, eliminating the need for delivery of 
spreadsheets. 
• Simplifies the reconciliation and validation process by providing standardized formats for the exchange of 
information. 
• Provides greater transparency as it relates to the firm’s calculation of the fund’s fee rules and rates. 
• Automates [[settlement]] of the fees due to/from the firm. 
• Consolidates money [[settlement]] with daily [[NSCC]] activity 
• Creates a secure, standardized and efficient method for data exchange using existing [[NSCC]] 
communication links 
[[NSCC]] Validation 
[[NSCC]] will validate the Invoice to ensure the required invoice structure is preserved, all required fields are 
populated, and valid values are submitted. [[NSCC]] will reject the entire invoice back to the submitter if any of the 
data is missing or invalid. 
Transmission Times 
 
Monday-Friday:  
• All invoices received prior to the [[NSCC]] cut-off time will be processed on the same day.   
• All Invoicing and Fee [[settlement]] files sent to [[NSCC]] after the last transmission deadline must be 
received the same day by 4PM ET for processing the next business day.  
• Files received after 4PM ET will reject unless the Datatrak file header contains the nex t business day’s 
date, in which case accepted files will be processed on the next business day.  
 
Saturday: 
• All invoices received prior to the [[NSCC]] cut-off time will be processed on the same day. 
• All Invoicing and Fee [[settlement]] files sent to [[NSCC]] after the last transmission deadline must be 
received by 2PM ET for processing the next business day.   
• Files received after 2PM ET will reject unless the Datatrak file header contains the next business day’s 
date. 
 

---

## Page 10

Records 
The following records were created for Invoicing and Fee [[settlement]]: 
Record Type Record Description 
41 Mutual Fund Invoicing Header Record 
42 Mutual Fund Invoicing Account Detail Record 
43 Mutual Fund Invoicing Detail Summary Record 
44 Mutual Fund Invoicing Invoice Summary Record 
46 Mutual Fund Invoicing Total Trailer Record 
47 Mutual Fund Invoicing Grand Total Trailer Record 
“Rate” Field–Best Practice 
The following fields provide information regarding the rate(s) submitted within an invoice/remittance file. Rates 
are agreed upon between the contra parties prior to the utilization of the [[DTCC]] Payment aXis Invoicing files.  
• “Number of Rates” field is part of the Header record 41 and indicates the number of Detail Summary 43 
records that are contained in the invoice. 
• “Rate Type” field (see values below) is included in the Detail Summary record 43 for all negotiated fee 
types (55, 56, 57) and the Detail record 42 for Retirement fees (fee type = 56). For Fee Type 56 
(Retirement Fee) the value entered on the Detail Summary Record 43 must match the value entered on 
the 42 record. 
 
Rate Type 
1= [[Asset]] Based 
2= Account Based 
 
The “Rate Type” field is required for Fee Types 55, 56, 57 and not allowed for the other fee types. The 
value provided in the “Rate Type” field will identify whether the rate in the “Rate” field is expressed in 
Basis Points (bps) or Dollars ($). 
• “ Rate” field: This field must contain the annualized rate and is a part of both the Detail record 42 and/or 
the Detail Summary record 43 as applicable for the respective fee types. Zero rates are not allowed. This 
field’s format will depend upon the value in the “Rate Type” field. 
 
Rates expressed in basis points should be populated in the following format:  
999.99999 
 
Decimal point is implied 
 
Example: 
 

---

## Page 11

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
General [[DTCC]] Payment aXis Invoice Information 11 
25bps = 02500000 (with the decimal point it will read 025.00000) 
 
25.55 bps = 02555000 (with the decimal point it will read 025.55000)  
 
Rates expressed in dollar amounts should be populated in the following format:  
999999.99 
 
Decimal point is implied 
 
Example: 
 
$25 = 00002500 (with the decimal point it will read 000025.00) 
 
$25.55 = 00002555 (with the decimal point it will read 000025.55) 
 
Duplicate rates are allowed for Fee Types 55, 56, 57 and NOT allowed for fee type 50 ([[NSCC]] will reject the 
invoice). 
Fee Type 50: 
Rate should be expressed in basis points for Fee Type 50. 
Fee Type 55, 56, 57: 
The value provided in the “Rate Type” field will determine whether the value supplied in the “Rate” field is basis 
points vs dollar amount. 
Control Number 
“Control Number” field should be populated by the invoice originator with a unique number generated by the 
firm (or fund if the remittance file is initiated by the fund) using the following algorithm:  
o Alpha–1 byte–With Value of “S” 
o Submitting Firm Number–4 bytes 
o Last digit of current year–1 byte 
o Julian Date–3 bytes (submission date) 
o Sequence Number–11 bytes 
 
[[NSCC]] will not validate this algorithm. 
Due to the pass-through design of the platform, [[NSCC]] will not validate for duplicate control numbers received 
prior to each processing day. Clients are required to ensure the unique control numbers are generated for the 
files. [[NSCC]] will perform duplicate control number validation within each processing day and will allow duplicate 
control numbers for the same combination of “Receiving Firm/Fund Number”, “Delivering Firm/Fund Number”, 
“Security Issue [[ID]]”, and “Fee Type” fields for the invoices submitted on the same processing day. 

---

## Page 12

[[settlement]] 
[[settlement]] Indicator 
The “[[settlement]] Indicator” field on the Header Record 41 dictates whether [[settlement]] will occur via [[NSCC]], 
outside of [[NSCC]] or if no [[settlement]] is expected. The following are valid indicators for the [[settlement]] Indicator 
field: 
Indicator Description Purpose 
1 [[settlement]] Initiates [[settlement]] at [[NSCC]] 
2 Non-[[settlement]] Used by the Commission & Fee [[settlement]] service 
for transactions settled outside of [[NSCC]]. 
3 Test Only used for testing purposes 
4 Omni Invoice for [[settlement]] Invoice submitted by the firm must be populated 
with “4”, indicating that the invoice is intended to be 
settled via [[NSCC]] when the fund submits a Release 
to [[settlement]] Transaction (“[[settlement]] Indicator” = 
“1”) 
5 Omni Invoice for Non-[[settlement]] Must be sent when invoices are for informational 
purposes only and are not intended to settle via 
[[NSCC]]. 
 
Debit/Credit Indicator 
The Debit/Credit direction of the payment is ALWAYS from the file Receiver’s perspective, the party 
releasing to [[settlement]] must properly set the “Debit/Credit Indicator” field on their response. For example, if the 
[[Broker]] Invoice is valued with a “1” = Debit (Debit the fund/Credit the firm), the fund response must be valued 
with a “2” = Credit (Credit the firm/Debit the fund). 
Example–12b-1 Invoice: 
Firm ABC submits a 12b-1 Invoice (Fee Type = 50) to Fund XYZ with the following values: 
• “[[settlement]] Indicator” = “4”- Omni Invoice for [[settlement]] 
• “Debit/Credit Indicator” = “1”- Debit. Since the “Debit/Credit Indicator” is always from the file receiver’s 
perspective, a “Debit” value on the firm invoice indicates that the firm is expecting payment and the fund 
should be in a debit position. 
 
When the Fund sends a Confirmation only with no instructions to Settle through [[NSCC]], the following key 
fields must be provided: 
• “System Code” = F (Fund) 
• “[[settlement]] Indicator” = 4 (Omni Invoice for [[settlement]]) 
• “Debit/Credit Indicator” = 2 (Credit). Since the “Debit/Credit Indicator” is always from the file receiver’s 
perspective, the fund must provide the appropriate value by sending a “1” = Credit indicator on the fund’s 
response indicating that the Firm will be credited the [[settlement]] amount and the Fund will be debited.  
 
Please note that on Fund Confirmation, the Commission and Fee [[settlement]] records 38, 39 and 40 will NOT 
be generated for either party, since the “[[settlement]] Indicator” is set to “4”- Omni Invoice for [[settlement]]. 
When the Fund sends a Release to [[settlement]], the following key fields must be provided: 

---

## Page 13

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
General [[DTCC]] Payment aXis Invoice Information 13 
• “System Code” = F (Fund) 
• “[[settlement]] Indicator” = 1 ([[settlement]]) 
• “Debit/Credit Indicator” = 2 (Credit). Since the “Debit/Credit Indicator” is always from the file receiver’s 
perspective, the fund must provide the appropriate value by sending a “1” = Credit indicator on the fund’s 
response indicating that the Firm will be credited the [[settlement]] amount and the Fund will be debited.  
 
Both firms and funds should validate their [[settlement]] [[obligations]] ([[settlement]] amount and payment direction) by 
reviewing Commission and Fee [[settlement]] records 38, 39 and 40. These records will be generated on the 
business day prior to [[settlement]]. The [[settlement]] amount will appear in the “Omni [[settlement]] Value” field, 
payment direction will be populated in the “Omni Pay-Receive Code” (2 = Your Debit or 4 = Your Credit). 
[[settlement]] amount will also be reflected on the Money [[settlement]] ACT Fund/SERV File Autoroute #02132518 
under category “019” = Omnibus Invoicing. The [[settlement]] amount will appear in the “Credit Balance Amount” 
or “Debit Balance Amount” field, depending on the payment direction. 
[[DTCC]] does not validate the direction of the payment. [[settlement]] will occur based on the indicators provided by 
the party that is generating the “Release to [[settlement]]”. Both the firm and the fund are responsible for 
populating correct values and validating [[settlement]] amounts and payment directions for their respective 
invoices. 
Use of Modify Functionality vs. Partial Reject 
Funds have the ability to Modify or Partially Reject invoices for the following “Negotiated Fee” invoices:  
o Sub-Accounting Fee (Fee Type 55) 
o Retirement/Bank Trust Service Fee (Fee Type 56) 
o Networking Service Fee (Fee Type 57) 
 
Sub-Accounting 12b-1/Shareholder Fee Invoices (Fee Type = 50) can be confirmed, released to [[settlement]] or 
rejected by the fund. There is no partial rejection or partial payment of an invoice for this fee type.  
This functionality is NOT allowed for 12b-1 fee (Fee Type 50) or “Transactional” fee (Fee Types 51–54). For 
these fee types if the “Confirm/Reject Code Indicator” field is set to “4” = “Modified” or “5” = “Partially Rejected” 
the invoice will be rejected by [[NSCC]]. 
Prior to modifying or partially rejecting records in an invoice, the fund and firm should engage in conversations 
to ensure each side understands and agrees with the reason for modification and/or partial reject. Once a file 
has been modified or partially rejected it can be released to settle based on the modified file. 
When a record is being modified or partially rejected, the fund will indicate so by populating the appropriate 
fields/records with the required values. 
For a complete list of Modification and Fund Reject/Partial Reject reason codes, please refer to the “Reject 
Codes to be Used by Funds” and/or “Modification Reason Codes to be Used by Funds” section of the Record 
Layouts. 
Anticipated [[settlement]] Date 
All invoices that require a fund’s response must be confirmed, modified, partially rejected or released to 
[[settlement]] by the fund. 
The fund will review and validate the invoice and send a confirmation/modification/partial rejection (“response”) 
to the Firm. This response is intended to notify the firm that the fund has reviewed the invoice and intends to 
pay it on or about the Anticipated [[settlement]] Date. The Anticipated [[settlement]] date should be provided by the 
Fund on their response (Header Record 41), even though it is not required the best practice is to provide a 
target [[settlement]] date. The target [[settlement]] date will NOT create the actual [[settlement]] but will provide 

---

## Page 14

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
General [[DTCC]] Payment aXis Invoice Information 14 
the firm with the date the fund expects to release the invoice for [[settlement]]. Funds should respond 
with a confirmation as soon as the invoice has been validated. 
Zero Dollar Invoices 
In the event a Security Issue [[ID]] does not require a payment due to ineligible assets (for example, assets are 
not fully aged, therefore not eligible for a 12b-1 payment), clients should transmit a zero-dollar invoice through 
Invoicing and Fee [[settlement]] functionality. Funds require this information to reconcile total assets on the fund’s 
books with that on the firm’s books. The information is used by the Funds to complete verification of invoices in 
order to proceed with payment. 
Given the structure of a typical invoice, it is possible that the entire invoice will require no payment, or a 
particular component of a positive dollar invoice will equal $0. 
Example: 
A typical 12b-1 invoice will have the following structure: 
• Header Record 41 
o Rate 1 
» Optional Account Detail Records 42 
» Detail Summary Record 43 (includes a dollar amount for Rate 1) 
o Rate 2 
» Optional Account Detail Records 42 
» Detail Summary Record 43 (includes a dollar amount for Rate 2) 
• Summary Record 44–includes a total [[settlement]] dollar amount for this invoice 
 
The entire invoice can have a $0 value–this will be reflected on the Summary Record 44. Alternatively, an 
invoice can require a payment; however, one or more of the Summary Records 43 can be a $0.  
Key Data Elements: 
• Both Eligible and Ineligible assets are required, but can contain a value of zero  
• Rate is required (when applicable), but can be set to zero 
• The number of Eligible and Ineligible Positions are required (when applicable); but  can be set to zero. 
 
If the entire invoice does not require payment due to ALL assets for this Security Issue [[ID]] and invoice being 
ineligible for a payment, the Fund must confirm this invoice by sending a Confirmation through the Invoicing 
and Fee [[settlement]] system. Release to [[settlement]] is NOT required for such invoices. 
To ensure that funds receive a complete set of invoices through [[NSCC]], they must contact their firm partners to 
request zero-dollar invoices through Invoicing and Fee [[settlement]]. This will allow Funds to receiv e total assets 
and perform a meaningful invoice validation prior to payment processing through the automated solution–[[DTCC]] 
Payment aXis.  

---

## Page 15

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Sub-Accounting 12b-1/Shareholder Service Fee (Type 50) 15 
SUB-ACCOUNTING 12B-1/SHAREHOLDER SERVICE FEE 
(TYPE 50) 
Firm Invoice 
The process is initiated by a firm submitting a 12b-1/Service Fees Invoice to [[NSCC]] for transmission to a fund. 
Firm Invoice Structure 
Firm Invoice must contain the following records: 
• Header–Record Type 41 
• For each rate: 
o Optional Underlying Account Detail–Record Type 42–may be provided if requested by the fund. 
Although Underlying Account Detail records are optional, should the firm choose to submit these 
records, they must provide Sequences 1 and 2. This record should only be provided if mutually 
agreed between the firm and the fund. It is unlikely to be a recurring request from the fund. 
o Summary–Record Type 43 (there can be multiple rates per one [[CUSIP]]). 
• Invoice Summary–Record Type 44 
 
The following is a view of the Firm Invoice structure: 
• Header–Record Type 41 
• Rate 1 
o Optional Underlying Account Detail–Record Type 42 (Seq 1 & 2) 
o Summary–Record Type 43 
• Rate 2 
o Optional Underlying Account Detail–Record Type 42 (Seq 1 & 2) 
o Detail Summary–Record Type 43 
• Rate 3 
o Optional Underlying Account Detail–Record Type 42 (Seq 1 & 2) 
o Detail Summary–Record Type 43 
• Invoice Summary–Record Type 44 
 
The following key data elements are required on the Firm Invoice: 
Header–Record Type 41 
• “Control Number” field should be populated with a unique number generated by the firm using an industry 
defined algorithm. For additional information on this field and the suggested algorithm please reference 
“Control Number”. 
• “[[settlement]] Indicator” field must contain one of the following values: 
o “3” = Test 
o “4” = Invoice for [[settlement]]–indicates that this invoice is intended for [[settlement]] upon the fund’s 
release to [[settlement]] through [[NSCC]] 

---

## Page 16

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Sub-Accounting 12b-1/Shareholder Service Fee (Type 50) 16 
o “5” = Invoice for Non-[[settlement]] – indicates that this invoice will not be settled by [[NSCC]] 
 
[[NSCC]] Validation 
[[NSCC]] will validate the Invoice to ensure the required invoice structure is preserved, all required fields are 
populated, and valid values are submitted. If any of the criteria is not met, [[NSCC]] will reject the entire invoice 
back to the submitter. For additional information on [[NSCC]] invoice validation please reference “ [[NSCC]] 
Validation”. 
Fund Response Structure 
Fund response must contain the following records: 
• Header-Record Type 41 
• For each rate: Detail Summary Record Type 43 (there can be multiple rates per one  
• Invoice Summary-Record Type 44 
 
The following is a view of the Fund response structure: 
• Header–Record Type 41 
o Rate 1 
Detail Summary–Record Type 43 
o Rate 2 
Detail Summary–Record Type 43 
o Rate 3 
Detail Summary–Record Type 43 
• Invoice Summary–Record Type 44 
 
For each invoice the fund will respond in one of the following ways: 1) Confirm, 2) Reject or 3) Release to 
[[settlement]]. The fund CAN NOT modify or partially reject an invoice for this fee type. The fund is not expected 
or required to return Optional Underlying Account Detail–Record Type 42. The fund must send all Security 
Issue [[ID]] Detail Summary Records–Record Type 43 (one per each rate) on their response to the [[Broker]] 
Invoice. 
Fund Response-Confirm the Invoice 
The fund will review and validate the invoice and send a confirmation to the Firm. The confirmation is intended 
to notify the firm that the fund has reviewed the invoice and intends to pay it on or about the Anticipated 
[[settlement]] Date. For additional information on the Anticipated [[settlement]] Date please reference “Anticipated 
[[settlement]] Date”. 
The following key data elements should be populated when providing a confirm: 
Header–Record Type 41 
• “Confirm/Reject Code Indicator” field should be populated with “1” = Confirmed  
• “Anticipated [[settlement]] Date” field should be populated with the intended [[settlement]] date in the format 
mmddccyy. This is an optional field. 
• “[[settlement]] Indicator” field should be populated with “3” = Test, “4” = Omni Invoice for [[settlement]] or “5” = 
Omni Invoice for Non-[[settlement]]. 

---

## Page 17

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Sub-Accounting 12b-1/Shareholder Service Fee (Type 50) 17 
Fund Response-Reject the Invoice 
If the fund cannot validate an invoice (e.g. it is a duplicate invoice or the fund disagrees with information 
provided on the invoice), the fund will reject the ENTIRE invoice (an invoice consists of one Security [[ID]], Fee 
Type, Control Number, Omni Account number combination) back to the firm. There will be no partial rejection 
or partial payment of an invoice. The reason for rejecting the invoice should be indicated on the appropriate 
record. 
The industry best practice when a fund has previously confirmed an Invoice is that the fund should not 
subsequently reject that invoice. 
As invoices are sent by Security [[ID]] and Fee Type, and to maintain a clear audit trail of payment activity, a fund 
cannot change the [[settlement]] amount of an invoice. For example, if a firm invoice is $100.00, and the fund 
calculates payment of $90.00, the fund cannot make a partial payment. The fund should reject the invoice and 
indicate the appropriate reject reason. The firm will receive the reject and will either make the necessary 
adjustments and resubmit the invoice, or, at the firm’s discretion, contact the fund to discuss the discrepancy.  
The following key data elements should be populated on the Fund Response when rejecting an 
invoice: 
Header-Record Type 41 
• “Confirm Reject Code Indicator” field should be populated with “2” = “Rejected”  
 
Summary-Record Type 43 
• “Deliverer Reject Code Indicator” field should be populated on each Summary Record. If there was no 
issue with this Summary Record, this field should be populated with “1” = Valid. If there is an issue with 
the Summary Record, this field should be populated with “2” = Rejected, and the reason for rejection 
should be populated in at least one of the “Deliverer Reject Code” fields (starting with the “Deliverer Reject 
Code #1” field). 
Fund Response-Release to [[settlement]] 
If the fund is prepared to settle an invoice on the next business day, upon validating and approving the invoice, 
the Fund sends a Release to [[settlement]] instruction to [[NSCC]]. The [[settlement]] amount will be included with the 
fee [[settlement]] [[obligations]]-[[DTCC]] Payment aXis
® Files (Record Types 38, 39 and 40)-and [[settlement]] will occur 
on the next business day. 
[[settlement]] Amounts will be reflected on the existing report: 
• Money [[settlement]] ACT Fund/SERV® File Autoroute # 02132518 will be updated to reflect Invoicing and 
Fee [[settlement]] amounts. 
 
The following key data elements should be populated on the Fund Response when releasing to  
[[settlement]]: 
Header-Record Type 41 
• “Confirm Reject Code Indicator” field should be populated with “1” = Confirmed  
“[[settlement]] Indicator” field should be populated with “1” = [[settlement]]  

---

## Page 18

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Sub-Accounting 12b-1/Shareholder Service Fee (Type 50) 18 
 
The following flow depicts the entire 12b-1 process: 
  


---

## Page 19

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Sub-Accounting 12b-1/Shareholder Service Fee (Type 50) 19 
 
Examples 
To view a sample 12b-1/Service Fees invoice with various fund responses, please visit the following link:  
https://dtcclearning.com/products-and-services/mutual-fund-services/[[DTCC]]-payment-axis.html#Record-Layouts 
[[settlement]] 
[[NSCC]] will NOT settle a 12b-1/Service Fees Invoice until a Fund submits a “Release to [[settlement]]” instruction. 
The following conditions must be satisfied for [[settlement]] to occur: 
Header-Record Type 41 
• “System Code” field should be populated with “F” = Fund 
• “Fee Type” field should be populated with “50” = Sub-Accounting 12b-1/Service Fees 
• “[[settlement]] Indicator” field should be populated with “1” = [[settlement]] 
• “Confirm/Reject Code Indicator” field should be populated with “1” = Confirmed  
 
This process will be used for this fee type for both credits and debits. The net of the credit and debit detail 
records will be used for [[settlement]]. 
For additional information on the [[settlement]] Indicator, please reference “[[settlement]] Indicator”. 
  

---

## Page 20

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Transactional Fees-CDSC/[[Underwriting]] Fee Adjustment/Short-Term Redemption/Finder’s Fee Adjustment: [[Broker]] Invoice-Fee Types 51, 52, 53, 54 20 
TRANSACTIONAL FEES-CDSC/[[Underwriting]] FEE 
ADJUSTMENT/SHORT-TERM REDEMPTION/FINDER’S 
FEE ADJUSTMENT: [[Broker]] INVOICE-FEE TYPES 51, 
52, 53, 54 
[[Broker]] Invoice 
Typically, firms provide funds with a spreadsheet and payment for reimbursement of fees associated with these 
transactions. Therefore, the design of these fee types is to allow the firm to provide invoice and [[settlement]].  
The process is initiated when the Firm submits a remittance file to [[NSCC]]. 
Invoice Structure 
Firm Invoice should contain the following records: 
• Header-Record Type 41 
• Underlying Account Detail–Record Type 42 (sequence 1 and 3) 
• Detail (Security Issue [[ID]]) Summary–Record Type 43  
• Invoice Summary-Record Type 44 
 
This process will be used for these Fee types for both credits and debits. The net of the credit and debit detail 
records will be used for [[settlement]]. 
[[NSCC]] Validation 
[[NSCC]] will validate the Invoice to ensure the required invoice structure is preserved, all required fields are 
populated, and valid values are provided. If any of the criteria is not met, [[NSCC]] will reject the entire invoice 
back to the submitter. The fund will NOT send a response and the invoice will settle automatically on the 
next business day. 
For additional information on [[NSCC]] invoice validation please reference “[[NSCC]] Validation”. 
[[settlement]] Amounts will be reflected on the following report: 
• Money [[settlement]] ACT Fund/SERV® File Autoroute # 02132518 will be updated to reflect Invoicing and 
Fee [[settlement]] amounts. 
 
The following key data elements should be populated on the [[Broker]] Invoice: 
Header-Record Type 41 
• “Confirm Reject Code Indicator” field should be populated with “3” = N/A 
• “[[settlement]] Indicator” field should be populated with: 
o “1” = [[settlement]]–this indicator will trigger [[settlement]] at [[NSCC]] 
o “2” = No [[settlement]]–this indicator will be used for invoices that are sent for informational purposes 
only 
o “3” = Test–this indicator will be used for testing purposes 

---

## Page 21

Examples 
To view a sample invoice please visit the following link:  
https://dtcclearning.com/products-and-services/mutual-fund-services/[[DTCC]]-payment-axis.html#Record-Layouts 
[[settlement]] 
[[NSCC]] will NOT settle a Fee Invoice unless the following requirements are met: 
Header–Record Type 41 
• “System Code” field is set to “B” =Firm 
• “Fee Type” field is set to a value of “51”, “52”, “53”, or “54” depending on fee type  
• “[[settlement]] Indicator” field is set to “1” = [[settlement]] 
“Confirm/Reject Code Indicator” field is set to “1” = Confirmed  

---

## Page 22

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Transactional Fees-CDSC/[[Underwriting]] Fee Adjustment/Short-Term Redemption/Finder’s Fee Adjustment: [[Broker]] Invoice-Fee Types 51, 52, 53, 54 22 
 
The following flow depicts the entire process: 
Fund Omnibus FirmNSCC
Acknowledge or Reject 
(2:15 - 3 pm ET)
Pass Files 2:15 - 3pm ET 
(Records 41, 42, 43, 44, 46)
5 5
Next Business Day [[settlement]] (for 
files received  by 2pm ET on a 
previous business day) .  Send a 
summary file to the deliverer and the 
receiver 
Transactional Fees - CDSC / Short-Term Redemption / 
[[Underwriting]] Fee Adjustment / Finder’s Fee Adjustment Flow
3
Omni Firm Submits CDSC File 
to [[NSCC]] by 2pm ET (Records: 
41, 42, 43, 44) 
2
1
Transaction Date (TR)
[[settlement]] (TR + 1)
4
Notify both the Payer and the Receiver 
of their pending debits and credits - 
between 2:15pm - 3pm ET
Records 38, 39, 40 Records 38, 39, 40
4
  

---

## Page 23

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 23 
NEGOTIATED FEES/THIRD PARTY FEES (FEE TYPES 55, 
56, 57) 
The following third-party fees are supported by the system: 
• Sub-Accounting Service Fee (Fee Type 55) 
• Retirement/Bank Trust Service Fee (Fee Type 56) 
• Networking Service Fee (Fee Type 57) 
Sub-Accounting Service Fee (Fee type 55) vs Retirement/Bank Trust 
Service Fee (Fee Type 56) 
Sub-Accounting Service Fee (Fee Type 55) does not allow for passing of detail records 42 and was designed 
for invoices originated by [[Broker]] dealers. Retirement/Bank Trust Service Fee (Fee Type 56) requires detail 
records 42 and was designed for invoices originated by banks, trusts and record- keepers. During design and 
requirements gathering stages Omni Invoicing task force agreed that detail records 42 for Fee Type 55 was not 
necessary, as the underlying account information can be obtained from the Omni/SERV Transparency files and 
not provided today. However, [[NSCC]] had received feedback that certain clients [[DO]] ask for and receive this 
information from certain firms. An [[NSCC]] enhancement request to build Optional Detail Records 42 for Sub-
Accounting Service Fee (fee type 55) had been sent to [[NSCC]]. [[NSCC]] reviewed the request with the Omni 
Invoicing taskforce, and it was determined not to adopt this change.  
It is recommended that firms and funds agree upon the type of fee (record layout) they will transmit. The best 
practice is - an invoice should be submitted in the Retirement/Bank Trust (Fee Type 56) format, which allows 
for detail records, if the fund requires the sub account details. In the case where the fund does not receive 
detail information in the current manual invoice payment process, Fee Type 55 should be provided.  
Sub-Accounting Service Fee–Fee Type 55 
Firm Invoice 
The process is initiated when the Firm submits a Sub-Accounting Service Fee Invoice to [[NSCC]] for 
transmission to a fund. 
Invoice Structure 
Firm Invoice must contain the following records: 
o Header-Record Type 41 
» With CDSC: Detail (Security) Summary–Record Type 43* 
» Without CDSC: Detail (Security) Summary–Record Type 43* 
» With Zero Balance: Detail (Security) Summary–Record Type 43* 
o Invoice Summary-Record Type 44 
 
*At least one record 43 is required for a given invoice. 
Multiple Rates are allowed per security issue [[ID]]/invoice and the same rates can be submitted for the different 
Rate Categories (1=With CDSC, 2=Without CDSC, 3=Zero Balance). However, the best practice:  In situations 
where the same rate is applicable to different rate categories and the firm selects to submit one record, the 43 
record should be submitted using the “Without CDSC” Indicator. 

---

## Page 24

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 24 
The following key data elements are required on the Firm Invoice: 
Header–Record Type 41 
• “Control Number” field should be populated with a unique number generated by the firm using an industry 
defined algorithm. For additional information on this field and the suggested algorithm please reference 
“Control Number”. 
• “[[settlement]] Indicator” field must contain one of the following values: 
o “3” = Test 
o “4” = Omni Invoicing for [[settlement]]–indicates that this invoice is intended for [[settlement]] upon the 
fund’s release to [[settlement]] through [[NSCC]] 
o “5” = Omni Invoice for Non-[[settlement]]–indicates that this invoice will not be settled via [[NSCC]] 
 
[[NSCC]] Validation 
[[NSCC]] will validate the Invoice to ensure the required invoice structure is preserved, all required fields are 
populated, and other fields have valid values. If any of the criteria is not met, [[NSCC]] will reject the entire invoice 
to the submitter. 
For additional information on [[NSCC]] validation please reference “[[NSCC]] Validation”. 
Fund Response 
For each invoice the fund will respond in one of the following ways: 1) Confirm without modification, 2) Modify, 
3) Partially reject, 4) Reject the entire invoice or 5) Release to [[settlement]]. 
Fund Response must contain the following records: 
o Header-Record Type 41 
» With CDSC: Detail (Security) Summary–Record Type 43 
» Without CDSC: Detail (Security) Summary–Record Type 43 
» With Zero Balance: Detail (Security) Summary–Record Type 43 
o Invoice Summary-Record Type 44 
Fund Response-Confirm the Invoice 
The fund will review and validate the invoice and send a confirmation to the Firm. The confirmation is intended 
to notify the firm that the fund has reviewed the invoice and intends to pay it on or about the Anticipated 
[[settlement]] Date. 
For additional information on the Anticipated [[settlement]] Date please reference “ Anticipated [[settlement]] Date”. 
The following key data elements should be populated on the Confirmation:  
Header–Record Type 41 
• “Confirm/Reject Code Indicator” field should be populated with “1” = Confirmed  
• “Anticipated [[settlement]] Date” field should be populated with the intended [[settlement]] date in the format 
mmddccyy. This is an optional field. 
• “[[settlement]] Indicator” field should be populated with “3” = Test, “4” = Omni Invoice for [[settlement]] or “5” = 
Omni Invoice for Non-[[settlement]]. 
Detail Summary Record Type 43 
• “Deliverer Reject Indicator” field should be populated with “1” = Valid 

---

## Page 25

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 25 
Fund Response–Confirm with Modification 
The fund may modify an invoice and send a modification to the firm. The modification is intended to notify the 
firm that the fund has reviewed the invoice, modified certain information and intended to pay the modified 
invoice on or about the Anticipated [[settlement]] Date. 
The following key data elements should be populated on the Modification:  
Header–Record Type 41 
• “Confirm/Reject Code Indicator” field should be populated with “4” = Modified 
• “Anticipated [[settlement]] Date” field should be populated with the intended [[settlement]] date in the format 
mmddccyy. This is an optional field. 
• “[[settlement]] Indicator” field should be populated with “3” = Test, “4” = Omni Invoice for [[settlement]] or “5” = 
Omni Invoice for Non-[[settlement]]. 
 
Detail Summary Record Type 43 
• “Deliverer Reject Indicator” field should be populated with “1” = Valid 
• “Modification Indicator” field should be populated with “1” = Yes on the record/s that was modified and  
 “2” = No on the record/s that was not modified. 
• “Modification Reason Code” should be populated with the Modification Reason Code (for a complete list of 
codes, please refer to “Modification Reason Codes to be Used by Funds to Modify [[Broker]] Initiated 
Invoices” section of the record layouts) 
• “Dollar Amount” field should be modified (if necessary) 
 
Invoice Summary Record Type 44 
• “Dollar Amount” field should be modified (if necessary) 
Fund Response–Confirm with Partial Rejection 
The fund may partially reject an invoice and send a partial rejection to the firm. The partial rejection is intended 
to notify the firm that the fund has reviewed the invoice, rejected certain lines and intends to settle the adjusted 
invoice on or about the Anticipated [[settlement]] Date. 
The following key data elements should be populated on the Partial Rejection: 
Header–Record Type 41 
• “Confirm/Reject Code Indicator” field should be populated with “5” = Partially Rejected  
• “Anticipated [[settlement]] Date” field should be populated with the intended [[settlement]] date in the format 
mmddccyy. This is an optional field. 
• “[[settlement]] Indicator” field should be populated with “3” = Test, “4” = Omni Invoice for [[settlement]] or “5” = 
Omni Invoice for Non-[[settlement]]. 
 
Detail Summary Record Type 43 
• “Deliverer Reject Indicator” field should be populated with “2” = “Rejected” on the record(s) that was 
rejected. All remaining (“good”) records should be populated with “1” = Valid in this field. At least one of 
the Summary Records 43 should be rejected (cannot reject ALL Summary Records 43).  

---

## Page 26

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 26 
• “Deliverer Reject Indicator” should be populated with the Reject Reason Code on the rejected records. For 
a complete list of codes, please refer to “Reject Codes to be Used by Funds to Modify [[Broker]] Initiated 
Invoices” section of the record layouts. 
 
Invoice Summary Record Type 44 
• “Dollar Amount” field should be reduced by the dollar amount(s) on the rejected lines.  
Modify vs. Partial Reject 
The following are the best practices for when a fund should Modify an invoice as opposed to Partially Rejecting 
the invoice based on the field that is in question. 
Field Name Record Modify Partial Reject Note/Scenario 
Rate 43  Yes If any (but not all) of the rates are incorrect partially reject 
the invoice. If all of the rates are incorrect reject entire 
invoice. Reject Code “OB” = Invalid Rate 
Sub Accounting 
Eligible Assets 
43 Yes  Modify with a reason code “MB” = [[Asset]] Value Invalid. 
Only truly applicable when firm bills based on basis points 
(“Rate Type” =1–[[Asset]] Based). When billing is account 
based (“Rate type” =2-Account Based) assets would not 
affect the payment. If multiple Summary Records 43 exist 
funds should modify each one (if the fund has the ability to 
calculate). 
Rate Type 43  Yes Partial reject if any (but not all) of the rate types are 
incorrect. If all of the rate types are incorrect reject the 
entire invoice. 
Reject Code “OB” = Invalid Rate 
Rate Category 43  Yes Partial reject if any (but not all) of the rate categories are 
incorrect. If all of the rate categories are incorrect reject 
the entire invoice. Reject code “OF” = Unauthorized Firm 
invoice 
Number of Eligible 
Positions 
43 Yes  Reason Code “MH” = Incorrect Positions 
Fund Response-Reject the Invoice 
If the fund cannot validate an invoice (e.g. it is a duplicate invoice or the fund disagrees with information 
provided on the invoice), the fund will reject the ENTIRE invoice. The reason for rejecting the invoice should be 
indicated on the appropriate record. 
The industry best practice when a fund has previously confirmed an Invoice, the fund should not subsequently 
reject it. 
The following key data elements should be populated on the Fund Response when rejecting an 
invoice: 
Header-Record Type 41 
• “Confirm Reject Code Indicator” field should be populated with “2” = “Rejected”  
 

---

## Page 27

Detail Summary-Record Type 43 
• “Deliverer Reject Code Indicator” field should be populated on each Summary Record. If there is no issue 
with this Summary Record, this field should be populated with “1” = Valid. If there is an issue with the 
Summary Record, this field should be populated with “2” = Rejected, and the reason for rejection should 
be populated in at least one of the “Deliverer Reject Code” fields (starting with the “Deliverer Reject Code 
#1” field). 
Fund Response-Release to [[settlement]] 
If the fund is prepared to settle an invoice, upon validating and approving the invoice, the Fund should send a 
Release to [[settlement]] instruction to [[NSCC]]. The [[settlement]] amount will be included with the fee [[settlement]] 
[[obligations]] - [[DTCC]] Payment aXis
® Files (Record Types 38, 39 and 40) - and [[settlement]] will occur on the next 
business day. 
[[settlement]] Amounts will be reflected on the existing report: 
• Money [[settlement]] ACT Fund/SERV® File Autoroute # 02132518 will be updated to reflect Invoicing and 
Fee [[settlement]] amounts. 
 
The following key data elements should be populated on the Fund Response when releasing to  
[[settlement]]: 
Header-Record Type 41 
• “Confirm Reject Code Indicator” field should be populated with “1” = Confirmed, “4” = Modified or  
“5” = Partially Rejected 
• “[[settlement]] Indicator” field should be populated with “1” = [[settlement]] 
 
Detail Summary Record 43 
• If the invoice was modified or partially rejected, all of the affected Detail Records 43 should be marked 
with the modification or partial rejection indicator and the reason – the same way the fields were populated 
when the fund modified or partially rejected the invoice. 
 
[[settlement]] Amounts will be reflected on the following report: 
Money [[settlement]] ACT Fund/SERV ® File Autoroute # 02132518 will be updated to reflect Invoicing and Fee 
[[settlement]] amounts. 
  

---

## Page 28

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 28 
 
The following flow depicts the entire process: 
 
  


---

## Page 29

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 29 
Examples 
To view a sample Sub-Accounting Service Fee invoice with various fund responses, please visit the following 
link:  
https://dtcclearning.com/products-and-services/mutual-fund-services/[[DTCC]]-payment-axis.html#Record-Layouts 
[[settlement]] 
[[NSCC]] will NOT settle a Sub-Accounting Service Fee Invoice until a Fund sends a “Release to [[settlement]]” 
instruction. The following conditions must be satisfied for a [[settlement]] to occur:  
Header-Record Type 41 
• “System Code” field should be populated with “F” = Fund 
• “Fee Type” field should be populated with “55” = Sub-Accounting Service Fee 
• “[[settlement]] Indicator” field should be populated with “1” = [[settlement]] 
• “Confirm/Reject Code Indicator” field should be populated with “1” = Confirmed, “4” = Modified or “5” 
=Partially Rejected 
 
For additional information on the [[settlement]] Indicator, please reference “[[settlement]] Indicator”. 
Retirement/Bank Trust Service Fee–Fee Type 56 
Firm Invoice 
The process is initiated by the Firm submitting a Fee “Invoice” to [[NSCC]] for transmission to the fund.  
Invoice Structure 
Firm Invoice should contain the following records: 
• Header-Record Type 41 
o Rate 1* 
» Account Detail Record–Record Type 42** 
» Detail Summary–Record Type 43** 
o Rate 2* 
» Account Detail Record–Record Type 42 
» Detail Summary–Record Type 43 
o Rate 3* 
» Account Detail Record–Record Type 42 
» Detail Summary–Record Type 43 
• Invoice Summary-Record Type 44 
 
*Note: 
the number of rates in the invoice structure above is an example. An invoice can consist of any number of rates. 
**A combination of Detail Records 42 followed by a Detail Summary Record 43 is defined as a “rate block”.  

---

## Page 30

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 30 
Detail Records 42 are Required. 
The following key data elements are required on the Firm Invoice: 
Header–Record Type 41 
• “Control Number” field should be populated with a unique number generated by the firm using an industry 
defined algorithm. For additional information on this field and the suggested algorithm please reference 
3.5 “Control Number”. 
• “[[settlement]] Indicator” field must contain one of the following values: 
o “3” = Test 
o “4” = Omni Invoicing for [[settlement]]–indicates that this invoice is intended for [[settlement]] upon the 
fund’s release to [[settlement]] through [[NSCC]] 
o “5” = Omni Invoice for Non-[[settlement]] – indicates that this invoice will not be settled by [[NSCC]] 
 
Detail Records 42 
Detail records 42 are Required for: 
1. Invoice (submitted by the firm) 
2. Modification 
3. Partial Rejection 
4. Release to [[settlement]] with Modification 
5. Release to [[settlement]] with Partial Rejection 
 
Funds should submit ALL detail records received on the original firm invoice in the aforementioned responses. 
When modifying or partially rejecting an invoice, all detail records for the affected rate block must be provided 
by the fund. Release to [[settlement]] of modified or partially rejected invoices should also contain all detail 
records for the rate block that was modified or partially rejected. 
Detail records 42 are Optional for: 
1. Confirmation 
2. Full invoice rejection 
3. Release to [[settlement]] without Modification 
4. Release to [[settlement]] without Partial Rejection 
 
Detail records are not required for the aforementioned fund responses, however when the fund passes these 
records, ALL detail records received on the original firm invoice should be included for a given rate block.  
  

---

## Page 31

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 31 
[[NSCC]] Validation 
[[NSCC]] will validate the Invoice to ensure the required invoice structure is preserved, all required fields are 
populated, and other fields have valid values. If any of the criteria is not met, [[NSCC]] will reject the entire invoice 
back to the submitter. 
For additional information on [[NSCC]] validation, please reference “[[NSCC]] Validation.” 
Fund Response 
For each invoice the fund will respond in one of the following ways: 1) Confirm without modification, 2) Modify, 
3) Partially reject, 4) Reject the entire invoice or 5) Release to [[settlement]]. 
Fund Response must contain the following records: 
• Header-Record Type 41 
Rate 1 
o Account Detail Record–Record Type 42 (Required for Modify/Partial Reject/Release to [[settlement]] 
with Modification/Release to [[settlement]] with Partial Rejection) 
o Detail Summary–Record Type 43 
Rate 2 
o Account Detail Record–Record Type 42 (Required for Modify/Partial Reject/Release to [[settlement]] 
with Modification/Release to [[settlement]] with Partial Rejection) 
o Detail Summary–Record Type 43 
Rate 3 
o Account Detail Record–Record Type 42 (Required for Modify/Partial Reject/Release to [[settlement]] 
with Modification/Release to [[settlement]] with Partial Rejection) 
o Detail Summary–Record Type 43 
• Invoice Summary-Record Type 44 
Fund Response-Confirm the Invoice 
The fund will review and validate the invoice and send a confirmation to the firm. The confirmation is intended 
to notify the firm that the fund has reviewed the invoice and intends to pay it on or about the Anticipated 
[[settlement]] Date. 
For additional information on Anticipated [[settlement]] Date, please reference “Anticipated [[settlement]] Date”. 
The following key data elements should be populated on the Confirmation:  
Header–Record Type 41 
• “Confirm/Reject Code Indicator” field should be populated with “1” = Confirmed  
• “Anticipated [[settlement]] Date” field should be populated with the intended [[settlement]] date in the format 
mmddccyy. This is an optional field. 
• “[[settlement]] Indicator” field should be populated with “3” = Test, “4” = Omni Invoice for [[settlement]] or “5” = 
Omni Invoice for Non-[[settlement]]. 
 
Detail Record Type 42–Optional 
Detail Summary Record Type 43 
• “Deliverer Reject Indicator” field should be populated with “1” = Valid 

---

## Page 32

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 32 
Fund Response–Confirm with Modification 
The fund can modify the invoice and send a modification to the firm. The modification is intended to notify the 
firm that the fund has reviewed the invoice, modified certain information and intends to pay the modified invoice 
with a potential change in the [[settlement]] obligation on or about the Anticipated [[settlement]] Date.  
If there are any modifications to any of the Detail Records 42, ALL Detail Records 42 must be submitted for 
that rate block. 
The following key data elements should be populated on the Modification:  
Header–Record Type 41 
• “Confirm/Reject Code Indicator” field should be populated with “4” = Modified 
• “Anticipated [[settlement]] Date” field should be populated with the intended [[settlement]] date in the format 
mmddccyy. This is an optional field. 
• “[[settlement]] Indicator” field should be populated with “3” = Test, “4” = Omni Invoice for [[settlement]] or “5” = 
Omni Invoice for Non-[[settlement]]. 
 
Detail Record Type 42 
• “Modification Indicator” field should be populated with “Y” = Yes on the record(s) that was modified  
• “Modification Reason Code” should be populated with the Modification Reason Code (for a complete list of 
codes, please refer to “Modification Reason Codes to be Used by Funds to Modify [[Broker]] Initiated 
Invoices” section of the record layouts) 
• “Dollar Amount” field should be modified (if necessary) 
• “Deliverer Reject Indicator” field should be populated with “1” = Valid on ALL Records 42  
 
Detail Summary Record Type 43 
• “Deliverer Reject Indicator” field on all Records 43 should be populated with “1” = Valid  
• “Modification Indicator” field should be populated with “Y” = Yes on the record(s) that was modified or 
summarizes the block of Detail Records 42 that contained modifications. 
• “Modification Reason Code” is Optional, but can be populated with the Modification Reason Code (for a 
complete list of codes, please refer to “Modification Reason Codes to be Used by Funds to Modify [[Broker]] 
Initiated Invoices” section of the record layouts) 
• “Dollar Amount” field should be modified (if necessary) 
 
Invoice Summary Record Type 44 
• “Dollar Amount” field should be modified (if necessary) 
Fund Response–Confirm with Partial Rejection 
The fund can partially reject the invoice and send a partial rejection to the firm. The partial rejection is intended 
to notify the firm that the fund has reviewed the invoice, rejected certain records and intends  to pay the 
adjusted invoice on or about the Anticipated [[settlement]] Date. 
If any of the Detail Records 42 are rejected, ALL Detail Records 42 must be submitted for that rate block.  
The following key data elements should be populated on the Modification:  
Header–Record Type 41 

---

## Page 33

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 33 
• “Confirm/Reject Code Indicator” field should be populated with “5” = “Partially Rejected”  
• “Anticipated [[settlement]] Date” field should be populated with the intended [[settlement]] date in the format 
mmddccyy. This is an optional field. 
• “[[settlement]] Indicator” field should be populated with “3” = Test, “4” = Invoice for [[settlement]] or “5” = 
Invoice for Non-[[settlement]]. 
 
Summary Record Type 42 
• “Deliverer Reject Indicator” field should be populated with “2” = “Rejected” on the record(s) that was 
rejected. All remaining (“good”) records should be populated with “1” = Valid in this field.  
• “Deliverer Reject Indicator” should be populated with the Reject Reason Code (for a complete list of 
codes, please refer to “Reject Codes to be Used by Funds to Modify [[Broker]] Initiated Invoices” section of 
the record layouts) 
 
Detail Summary Record Type 43 
• “Deliverer Reject Indicator” field should be populated with “3” = “Partially Rejected” on the record(s) that 
was rejected. All remaining (“good”) records should be populated with “1” = Valid in this field.  
• “Deliverer Reject Indicator” should be populated with the Reject Reason Code on the Record that was 
rejected. For a complete list of codes, please refer to “Reject Codes to be Used by Funds to Modify [[Broker]] 
Initiated Invoices” section of the record layouts. 
• “Dollar Amount” field should be adjusted to remove the dollar amounts from the rejected lines.  
 
Invoice Summary Record Type 44 
• “Dollar Amount” field should be adjusted to remove the dollar amounts from the rejected lines.  
Modify vs. Partial Reject 
The following are the best practices for when a fund should Modify an invoice as opposed to Partially Rejecting 
the invoice based on the field that is in question. 
Field Name Record Modify Partial Reject Notes/Scenario 
Underlying 
Customer Type 
42 Yes  Modify the value and provide the correct Underlying 
Customer Type. 
Modification Reason Code = “MH”- Incorrect Positions 
Rate 42  Yes If any (but not all) of the rates are incorrect-partially 
reject. If all of the rates are incorrect reject entire invoice. 
Reject Code “OB” = Invalid Rate 
Sub Accounting 
Eligible Assets 
42 Yes  Modify with a reason code “MB” = [[Asset]] Value Invalid. 
Only truly applicable when firm bills based on basis 
points (“Rate Type” =1–[[Asset]] Based). When billing is 
account based (“Rate Type” = 2-Account Based) assets 
would not affect the payment. 
If multiple Detail Records 43 exists funds should modify 
each one (if the fund has the ability to calculate). 
Eligible 42 Yes  Modify the value and provide the correct 

---

## Page 34

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 34 
Field Name Record Modify Partial Reject Notes/Scenario 
[[participant]] Count    Eligible [[participant]] Count. Modification Reason Code = 
“MH”–Incorrect Positions 
Rate Type 42  Yes Partial reject if any (but not all) of the rate types are 
incorrect. If all of the rate types are incorrect reject the 
entire invoice. 
Reject Code “OB” = Invalid Rate 
Fund Response-Reject the Invoice 
If the fund cannot validate an invoice (e.g. it is a duplicate invoice or the fund disagrees with information 
provided on the invoice), the fund will reject the ENTIRE invoice. The reason for rejecting the invoice should be 
indicated on the appropriate record. 
The industry best practice when a fund has previously confirmed an Invoice, the fund should not subsequently 
reject it. 
The following key data elements should be populated on the Fund Response when rejecting an 
invoice: 
Header-Record Type 41 
• “Confirm Reject Code Indicator” field should be populated with “2” = “Rejected”  
 
Detail Records 42 are Optional 
Detail Summary-Record Type 43 
• “Deliverer Reject Code Indicator” field should be populated on each Summary Record. If there was no 
issue with this Summary Record, this field should be populated with “1” = Valid. If there is an issue with 
the Summary Record, this field should be populated with “2” = Rejected, and the reason for rejection 
should be populated in at least one of the “Deliverer Reject Code” fields. 
Fund Response-Release to [[settlement]] 
If the fund is prepared to settle an invoice, upon validating and approving the invoice, the Fund should send a 
Release to [[settlement]] instruction to [[NSCC]]. The [[settlement]] amount will be included with the fee [[settlement]] 
[[obligations]]-[[DTCC]] Payment aXis
® Files (Record Types 38, 39 and 40)-and [[settlement]] will occur on the next 
business day. 
[[settlement]] Amounts will be reflected on the existing report: 
• Money [[settlement]] ACT Fund/SERV® File Autoroute # 02132518 will be updated to reflect Invoicing and 
Fee [[settlement]] amounts. 
 
The following key data elements should be populated on the Fund Response when  releasing to 
[[settlement]]: 
Header-Record Type 41 
• “Confirm Reject Code Indicator” field should be populated with “1” = Confirmed, “4” = Modified or  
“5” = Partially Rejected 
• “[[settlement]] Indicator” field should be populated with “1” = [[settlement]] 
 

---

## Page 35

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 35 
Summary Record Type 42 
• If the invoice was modified or partially rejected, ALL Detail Records 42 must be submitted for the rate 
block that contained a modification or rejection. 
• All modified or rejected records must be marked the same way they were populated when the f und 
modified (or partially rejected) the invoice. 
 
Detail Summary Record 43 
If the invoice was modified or partially rejected, ALL of the affected Detail Records 43 should be marked with the 
modification (or partial rejection) and the reason– the same way they were populated when the fund modified 
(partially rejected) the invoice. 
  

---

## Page 36

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 36 
The following flow depicts the entire process: 
 


---

## Page 37

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 37 
Examples 
To view a sample Retirement/Bank Trust Service Fee invoice with various fund responses, please visit the 
following link:  
https://dtcclearning.com/products-and-services/mutual-fund-services/[[DTCC]]-payment-axis.html#Record-Layouts 
[[settlement]] 
[[NSCC]] will NOT settle a Retirement/Bank Trust Service Fee Invoice until a Fund submits a “Release to 
[[settlement]]” instruction. The following conditions must be satisfied for [[settlement]] to occur:  
Header-Record Type 41 
• “System Code” field should be populated with “F” = Fund 
• “Fee Type” field should be populated with “56” = Retirement/Bank Trust Service Fee  
• “[[settlement]] Indicator” field should be populated with “1” = [[settlement]] 
• “Confirm/Reject Code Indicator” field should be populated with “1” = Confirmed  
 
For additional information on the [[settlement]] Indicator, please reference “[[settlement]] Indicator”. 
Networking Service Fee–Fee Type 57 
Networking Service Fees payment process can be initiated by the firm or the fund. When the Networking fee is 
initiated by the firm it follows the same flow as the Sub-Accounting Service fee and the Retirement/Bank Trust 
Service fee (Flow 1) and will require a fund response to trigger [[settlement]].  
When initiated by the fund, the fund sends a remittance file, and the remittance file is auto settled on the next 
business day. No firm response will be received (Flow 2). 
Flow 1–Firm Initiated Invoice 
Firm Invoice 
The process is initiated when the [[Broker]] Firm submits a Networking Service Fee Invoice to [[NSCC]] for 
transmission to a fund. 
Invoice Structure 
Firm Invoice must contain the following records: 
• Header-Record Type 41 
o Detail Summary (Level 0)–Record Type 43 
o Detail Summary (Level 3)–Record Type 43 
o Detail Summary (Level 4)–Record Type 43 
• Invoice Summary-Record Type 44 
 

---

## Page 38

The following key data elements are required on the Firm Invoice: 
Header–Record Type 41 
• “Control Number” field should be populated with a unique number generated by the firm using an industry 
defined algorithm. For additional information on this field and the suggested algorithm please reference 
“Control Number”. 
• “[[settlement]] Indicator” field must contain one of the following values: 
o “3” = Test 
o “4” = Omni Invoicing for [[settlement]]–indicates that this invoice is intended for [[settlement]] upon the 
fund’s release to [[settlement]] through [[NSCC]] 
o “5” = Omni Invoice for Non-[[settlement]]–indicates that this invoice will not be settled by [[NSCC]] 
• “Invoice Initiator” field should be populated with “1” = Firm 
 
[[NSCC]] Validation 
[[NSCC]] will validate the Invoice to ensure the required invoice structure is preserved, all required fields are 
populated, and other fields have valid values. If any of the criteria is not met, [[NSCC]] will reject the entire invoice 
back to the submitter. 
For additional information on [[NSCC]] validation, please refer to Section 3.2 “[[NSCC]] Validation”. 
Fund Response 
For each invoice the fund will respond in one of the following ways: 1) Confirm without modification, 2) Modify, 
3) Partially reject, 4) Reject the entire invoice or 5) Release to [[settlement]]. 
Fund Response must contain the following records: 
• Header-Record Type 41 
o Detail Summary (Level 0)–Record Type 43 
o Detail Summary (Level 3)–Record Type 43 
o Detail Summary (Level 4)–Record Type 43 
• Invoice Summary-Record Type 44 
Fund Response-Confirm the Invoice 
The fund will review and validate the invoice and send a confirmation to the Firm. A confirmation is intended to 
notify the firm that the fund has reviewed the invoice and intends to pay it on or about the Anticipated 
[[settlement]] Date. 
For additional information on the Anticipated [[settlement]] Date, please reference  “Anticipated [[settlement]] Date”. 
The following key data elements should be populated on the Confirmation:  
Header–Record Type 41 
• “Confirm/Reject Code Indicator” field should be populated with “1” = Confirmed  
• “Anticipated [[settlement]] Date” field should be populated with the intended [[settlement]] date in the format 
mmddccyy. This is an optional field. 
• “[[settlement]] Indicator” field should be populated with “3” = Test, “4” = Omni Invoice for [[settlement]] or “5” = 
Omni Invoice for Non-[[settlement]]. 
 

---

## Page 39

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 39 
Detail Summary Record Type 43 
• “Deliverer Reject Indicator” field should be populated with “1” = Valid 
Fund Response–Confirm with Modification 
Funds have the ability to modify an invoice and send a modification response to the Firm. The modification is 
intended to notify the firm that the fund has reviewed the invoice, modified certain information and intends to 
pay the modified invoice on or about the Anticipated [[settlement]] Date. 
The following key data elements should be populated on the Modification:  
Header–Record Type 41 
• “Confirm/Reject Code Indicator” field should be populated with “4” = Modified 
• “Anticipated [[settlement]] Date” field should be populated with the intended [[settlement]] date in the format 
mmddccyy. 
• “[[settlement]] Indicator” field should be populated with “3” = Test, “4” = Invoice for [[settlement]] or “5” = 
Invoice for Non-[[settlement]]. 
 
Detail Summary Record Type 43 
• “Deliverer Reject Indicator” field should be populated with “1” = Valid 
• “Modification Indicator” field should be populated with “Y” = Yes on the record(s) that was modified  
• “Modification Reason Code” should be populated with the Modification Reason Code (for a complete list of 
codes, please refer to “Modification Reason Codes to be Used by Funds to Modify [[Broker]] Initiated 
Invoices” section of the record layouts) 
• “Dollar Amount” field should be modified (if necessary) 
 
Invoice Summary Record Type 44 
• “Dollar Amount” field should be modified (if necessary) 
 
 

---

## Page 40

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 40 
Fund Response–Confirm with Partial Rejection 
Funds have the ability to partially reject the invoice and send a partial rejection to the Firm. The partial rejection 
is intended to notify the firm that the fund has reviewed the invoice, rejected certain lines and intends to pay 
based on an adjusted invoice on or about the Anticipated [[settlement]] Date.  
The following key data elements should be populated on the Modification:  
Header–Record Type 41 
• “Confirm/Reject Code Indicator” field should be populated with “5” = Partially Rejected  
• “Anticipated [[settlement]] Date” field should be populated with the intended [[settlement]] date in the format 
mmddccyy. This is an optional field. 
• “[[settlement]] Indicator” field should be populated with “3” = Test, “4” = Omni Invoice for [[settlement]] or “5” = 
Omni Invoice for Non-[[settlement]]. 
 
Detail Summary Record Type 43 
• “Deliverer Reject Indicator” field should be populated with “2” = “Rejected” on the record(s) that was 
rejected. All remaining accepted records should be populated with “1” = Valid in this field.  
• “Deliverer Reject Indicator” should be populated with the Reject Reason Code on the rejected records. For 
a complete list of codes, please refer to “Reject Codes to be Used by Funds to Modify [[Broker]] Initiated 
Invoices” section of the record layouts. 
 
Invoice Summary Record Type 44 
• “Dollar Amount” field should be adjusted to remove the dollar amounts from the rejected lines.  
Modify vs. Partial Reject 
The following are best practices for when a fund should Modify an invoice as opposed to Partially Rejecting the 
invoice based on the field that is in question. 
Field Name Record Modify Partial Reject Note/Scenario 
Networking Control 
Indicator 
43  Yes Reject the incorrect Summary Record 43 but accept the 
remaining Records 43 (ex, 1st record 43 with “Networking 
Control Indicator” = Level 4 is incorrect, but 2nd record 43 
with “Networking Control Indicator” = Level 3 is correct) 
Reject Code “OF” = Unauthorized Firm Invoice 
Number of Eligible 
Positions 
43 Yes  Reason Code “MH” = Incorrect Positions. Fund has 
transparency to the number of network level accounts on 
their books; therefore such an adjustment is possible. 
Rate 43  Yes If any (but not all) of the rates are incorrect partially reject 
the invoice. If all of the rates are incorrect reject entire 
invoice. 
Reject Code “OB” = Invalid Rate 
Rate Type 43  Yes Partial reject if any (but not all) of the rate types are 
incorrect. If all of the rate types are incorrect reject the 
entire invoice. 
Reject Code “OB” = Invalid Rate 

---

## Page 41

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 41 
Field Name Record Modify Partial Reject Note/Scenario 
Eligible Assets 43 Yes  Modify with a reason code “MB” = [[Asset]] Value Invalid. 
Only truly applicable when firm bills based on basis 
points (“Rate Type” =1–[[Asset]] Based). When billing is 
account based (“Rate Type” =2-Account Based) assets 
would not affect the payment. 
If multiple Detail Records 43 exist funds should modify 
each one (if the fund has the ability to calculate). 
Fund Response-Reject the Invoice 
If a fund cannot validate an invoice (e.g. it is a duplicate invoice or the fund disagrees with information provided 
on the invoice), the fund should reject the ENTIRE invoice. The appropriate reject reason for rejecting the 
invoice should be indicated on the appropriate record. 
The following key data elements should be populated on a Fund Response when rejecting an invoice:  
Header-Record Type 41 
• “Confirm Reject Code Indicator” field should be populated with “2” = “Rejected”  
 
Detail Summary-Record Type 43 
• “Deliverer Reject Code Indicator” field should be populated on each Summary Record. If there was no 
issue with this Summary Record, this field should be populated with “1” = Valid. If there is an issue with 
the Summary Record, this field should be populated with “2” = Rejected, and the reason for rejection 
should be populated in at least one of the “Deliverer Reject Code” fields. 
Fund Response-Release to [[settlement]] 
If the fund is prepared to settle an invoice on the next business day, upon validating and approving the invoice, 
the Fund should submit a Release to [[settlement]] instruction to [[NSCC]]. The [[settlement]] amount will be included 
with the fee [[settlement]] [[obligations]]-[[DTCC]] Payment aXis
® Files (Record Types 38, 39 and 40)-and [[settlement]] 
will occur on the next business day. 
[[settlement]] Amounts will be reflected on the existing report: 
• Money [[settlement]] ACT Fund/SERV® File Autoroute # 02132518 will be updated to reflect Invoicing and 
Fee [[settlement]] amounts. 
 
The following key data elements should be populated on the Fund Response when releasing to  
[[settlement]]: 
Header-Record Type 41 
• “Confirm Reject Code Indicator” field should be populated with “1” = Confirmed  
• “[[settlement]] Indicator” field should be populated with “1” = [[settlement]] 
 
Detail Summary Record 43 
• If an invoice was modified or partially rejected, all of the affected Detail Records 43 should be marked with 
the modification (or partial rejection) and the reason–the same way they were populated when the fund 
modified (partially rejected) the invoice. 
 

---

## Page 42

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 42 
[[settlement]] Amounts will be reflected on the following report: 
• Money [[settlement]] ACT Fund/SERV® File Autoroute # 02132518 will be updated to reflect Invoicing and 
Fee [[settlement]] amounts. 
Examples 
To view a sample [[Broker]]-initiated Networking Service Fee invoice with various fund responses, please visit the 
following link:  
https://dtcclearning.com/products-and-services/mutual-fund-services/[[DTCC]]-payment-axis.html#Record-Layouts 
[[settlement]] 
[[NSCC]] will NOT settle a [[Broker]]-initiated Networking Service Fee Invoice until a Fund submits a “Release to 
[[settlement]]” instruction. The following conditions must be satisfied for [[settlement]] to occur:  
Header-Record Type 41 
• “System Code” field should be populated with “F” = Fund 
• “Fee Type” field should be populated with “56” = Retirement/Bank Trust Service Fee  
• “[[settlement]] Indicator” field should be populated with “1” = [[settlement]] 
• “Confirm/Reject Code Indicator” field should be populated with “1” = Confirmed, “4” = Modified or  
“5” = Partially Rejected 
 
For additional information on the [[settlement]] Indicator, please reference “[[settlement]] Indicator”. 
 
Fund Initiated Remittance File (Flow 2) 
When the Networking Service fee is initiated by the fund the remittance file will be auto-settled the following 
day. A firm response record is not available. 
Fund Initiated Remittance File 
Remittance file should contain the following records: 
• Header-Record Type 41 
o Detail Summary (Level 0)–Record Type 43 
o Detail Summary (Level 3)–Record Type 43 
o Detail Summary (Level 4)–Record Type 43 
• Invoice Summary-Record Type 44 
 
[[NSCC]] Validation 
[[NSCC]] will validate the Invoice to ensure the required invoice structure is preserved, all required fields are 
populated, and valid values are provided. If any of the criteria is not met, [[NSCC]] will reject the entire invoice 
back to the submitter. For additional information on [[NSCC]] invoice validation please reference “[[NSCC]] 
Validation”. 
The firm will NOT send a response and the invoice will settle automatically on the next business day.  

---

## Page 43

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 43 
[[settlement]] Amounts will be reflected on the following report: 
• Money [[settlement]] ACT Fund/SERV® File Autoroute # 02132518 will be updated to reflect Invoicing and 
Fee [[settlement]] amounts. 
 
The following key data elements should be populated on the Fund Initiated Remittance File:  
Header-Record Type 41 
• “Confirm Reject Code Indicator” field should be populated with “3” = N/A 
• “[[settlement]] Indicator” field should be populated with: 
o “1” = [[settlement]]–this indicator will trigger [[settlement]] at [[NSCC]] 
o “2” = No [[settlement]]–this indicator will be used for invoices that are sent for informational purposes 
only 
o “3” = Test–this indicator will be used for testing purposes 
• “Invoice Initiator” is set to “2” = Fund 
Examples 
To view a sample invoice, please visit the following link:  
https://dtcclearning.com/products-and-services/mutual-fund-services/[[DTCC]]-payment-axis.html#Record-Layouts 
 
[[settlement]] 
[[NSCC]] will NOT settle a Fee Invoice unless the following requirements are met: 
Header–Record Type 41 
• “System Code” field is set to “F” =Fund 
• “Fee Type” field is set to “57” = Networking Service Fee 
• “Invoice Initiator” is set to “2” = Fund 
• “[[settlement]] Indicator” field is set to “1” =[[settlement]] 
“Confirm/Reject Code Indicator” field is set to “1” =Confirmed  

---

## Page 44

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Negotiated Fees/Third Party Fees (Fee Types 55, 56, 57) 44 
 
The following flow depicts the entire process for Flow 2 Fund Initiated Remittance File:  
Fund FirmNSCC
Acknowledge or Reject 
(2:15-3pm ET)
Pass Files 
2:15-3pm ET 
(Records 41, 43, 44, 46)
5 5
Next Business Day [[settlement]] (for 
files received  by 2pm ET on a 
previous business day) .  Send a 
summary file to the deliverer and the 
receiver 
Networking Service Fee – Flow 2 (Fund Initiated)
2
Submit Networking Fee File to 
[[NSCC]] by 2pm ET (Records: 41, 
43, 44) 
3
Transaction Date (TR)
[[settlement]] (TR + 1)
4
Notify both the Payer and the Receiver 
of their pending debits and credits – 
2:15-3pm ET
Records 38, 39, 40 Records 38, 39, 40
4
1
  

---

## Page 45

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Testing 45 
TESTING 
User acceptance testing is not a pre-requisite prior to production; however, clients are strongly encouraged to 
test Invoicing and Fee [[settlement]] prior to launching this functionality in production. In order to test, clients need 
to make arrangements with a counterparty. Clients may view the list of clients who have subscribed to this 
service:  
https://dtcclearning.com/products-and-services/mutual-fund-services/contact-lists.html 
In order to test, both parties should agree on their preferred testing method: testing in PSE vs Production. 
[[NSCC]] shall have no responsibility or liability for any losses that may occur if parties choose to test in 
Production. 
Testing in PSE 
• Clients can test Invoicing and Fee [[settlement]] in PSE; however, [[settlement]] functionality is not available in 
this environment. Clients can validate their upcoming Debit/Credit [[obligations]] by reviewing [[DTCC]] 
Payment aXis® [[settlement]] Files–Record Types 38, 39 and 40. 
• Money [[settlement]] ACT Fund/SERV® File Autoroute # 02132518 will not be generated, and money will not 
move in PSE. 
 
Testing in Production 
Clients can test Invoicing and Fee [[settlement]] in Production in one of the following ways:  
• No [[settlement]]: Set the “[[settlement]] Indicator” field on the Header Record 41 to = “3” -Test 
• Small dollar amount [[settlement]]: Set the “[[settlement]] Indicator” field on the Header Record 41 to = “1” -
[[settlement]]. For example, in order to test clients can settle $1 Credit on Day 1 and $1 Debit on Day 2 this 
will net to $0. 

---

## Page 46

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Frequently Asked Questions 46 
FREQUENTLY ASKED QUESTIONS 
1. When I sign up for service, will I be able to control which contra parties can send invoices to me?  
 
No, [[NSCC]] does not create and maintain eligibility information by contra party. N SCC will report the eligibility by 
client. Information on who is subscribing to this service can be found on the [[DTCC]] website:  
https://www.[[DTCC]].com/wealth-management-services/mutual-fund-services/mutual-funds-client-public-
documentation 
For more information please reference “Eligibility”. 
 
2. How [[DO]] I send Financier Reports? 
 
The CDSC Distributor Liability, CDSC Waiver, CDSC Aging, CDSC Analysis, and CDSC Financier reports that 
are provided to the fund by the firm-are not included in this project and should be distributed as they are today.  
 
3. If I receive a CDSC, Short Term Redemption, [[underwriter]] or Finder’s Fee adjustment invoice that I 
[[DO]] not agree with, can I reject it? 
 
No. CDSC, Short-Term Redemption Fees, [[underwriter]] or Finder's Fee adjustments generally represent 
remittance payments. Prior to these enhancements, these fee types were paid by the Firm by check or wire 
without invoicing. The automated process follows the same business logic, therefore; the fund cannot confirm 
or reject these types of fee invoices and they will be automatically settled by [[NSCC]]. The fund should contact 
the firm and either settle the discrepancy outside of [[DTCC]] Payment aXis
® or request that the firm send a 
reversal invoice (reversing the debit/credit values) for the disputed invoice along with a new invoice record for 
the correct amount. 
 
4. Can I combine multiple rates for the same [[CUSIP]] on one 12b-1/Service Fees invoice? 
 
Yes. An Invoice consists of one Security [[ID]], one Fee Type, one omnibus account and a Control Number. 
Multiple rates within the same omnibus account for the same fee type by [[CUSIP]] i s supported by using multiple 
detail and a summary record for each rate. 
 
5. Can confirmation and release to [[settlement]] happen on the same day?  
 
Yes. The confirmation record associated with an invoice is informational only providing the sender an 
acknowledgement of receipt of the invoice. A fund may send a confirmation and release to [[settlement]] response 
on the same day. 
 
6. What happens if the fund does not settle on a previously communicated “Anticipated [[settlement]] 
Date”? 
 
The "Anticipated [[settlement]] Date" is an optional field for informational purposes to communicate the expected 
[[settlement]] date. [[settlement]] of an invoice is initiated by the fund sending a "Release to [[settlement]]."  

---

## Page 47

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Frequently Asked Questions 47 
7. How long does the fund have to respond to an invoice? 
 
The best practice is to confirm or reject the invoice immediately upon review then release [[settlement]] to pay the 
invoice in accordance with the fund's payment policy. Funds and firms are encouraged to discuss expected 
time horizons for invoice submission, review and payment. 
 
8. Is there a frequency that firms should use when invoicing funds? (i.e., Daily, Weekly, Monthly, 
Quarterly?) 
 
Firms and funds can set any frequency they agree upon, be it daily, weekly, monthly, quarterly or other.  
 
9. Will the [[DTCC]] retain or track invoices? 
 
No. invoicing through [[DTCC]] Payment aXis® facilitates the exchange of mutual fund invoice related data and 
centralizes payment. The system does not store or track invoices. 
 
10. I currently use [[DTCC]] Payment aXis®. [[DO]] I need to take action in order to participate in the new 
Invoicing and Fee [[settlement]] functionality? 
 
Yes, clients currently using [[DTCC]] Payment aXis® will need to sign up to transmit and receive the Transactional 
and Negotiated Fee Invoicing files.  For more information, please contact your [[NSCC]] Relationship Manager or 
Account Management at 212-855-8877.  
In addition, if appropriate, contact your service provider about adding the service.  
 
11. Can a firm participate with one fee type and not all? 
 
In order to participate in the Invoicing and Fee [[settlement]] service, clients are required to sign up for activation 
to the service(s) they are interested in: 
• 12b-1/Service Fees 
• CDSC, Short Term Trader Redemption, [[underwriter]] and Finder's Fee Adjustments (signing up for this fee 
type indicates participation in all four fee types) 
• Sub-Accounting Service Fee 
• Retirement/Bank Trust Service Fee 
• Networking Service Fee 
 
12. Will [[NSCC]] send Reminders? 
 
No. The [[NSCC]] system does not store or track invoices, therefore, reminders will not be generat ed. It is the 
responsibility of the clients to track invoicing activity. 

---

## Page 48

 
13. How [[DO]] I indicate rate type (basis points vs dollar amount) on the Negotiated Fees?  
 
“Rate Type” field is required on Detail Records 42 for Retirement/Bank Trust Service Fee (fee ty pe 56) and on 
Summary Records 43 for Sub-Accounting Service Fee (fee type 55), Retirement/Bank Trust Service Fee (fee 
type 56) and Networking Service Fee (fee type 57). This field should be populated with one of the following 
values: 
• 1 = [[Asset]] Based (for basis points) 
• 2 = Account Based (for dollar amount) 
 
The value provided in the “Rate Type” field will determine whether the value supplied in the “Rate” field is 
expressed as a basis points vs dollar amount. For additional information on rates please refere nce “Rate” field–
Best Practice. 
 
14. When should I Modify or Partially Reject an Invoice? 
 
Funds have the ability to Modify or Partially reject invoices for Negotiated fee types:  
• Sub-Accounting Service Fee (fee type 55) 
• Retirement/Bank Trust Service Fee (fee type 56) 
• Networking Service Fee (fee type 57) 
 
Prior to modifying or partially rejecting records in an invoice, the fund and firm should agree on the appropriate 
course of action and the reason for modificati on or partial rejection. Once a file has been modified or partially 
rejected it can be released to [[settlement]] based on the modified file. 
  

---

## Page 49

Chapter 2: Invoicing and Fee [[settlement]] User Guide/Best Practices 
Glossary 49 
GLOSSARY 
Term Definition 
Invoice One Security Issue [[ID]], Fee Type, Control Number combination 
Rate Block A grouping of Detail Records 42 followed by a Detail Summary Record 43 for a given rate 
Receiver [[NSCC]] [[ID]] of the Receiver. Receiver of the file. 
Deliverer [[NSCC]] [[ID]] of the Deliverer. Submitter of the file. 
Reject Codes There are 2 types of rejection: 
• Rejection by [[NSCC]] due to invalid format and missing records. To see a list of [[NSCC]] 
reject codes, please see the most recent version of the Networking and [[DTCC]] 
Payment aXis Reject Codes:  
https://dtcclearning.com/products-and-services/mutual-fund-services/codes.html 
 
  
• Rejection of Fee Type = 50, 55, 56, 57 invoice by the Fund. To see a list of Fund 
reject codes, please see the most recent version of the Networking and [[DTCC]] 
Payment aXis Reject Codes 
https://dtcclearning.com/products-and-services/mutual-fund-services/codes.html 
 
Modification Codes • To see a list of modification codes, please see the most recent version of the 
Networking and [[DTCC]] Payment aXis Reject Codes:  
https://dtcclearning.com/products-and-services/mutual-fund-services/codes.html 
Control Number Generated by a Delivering Firm. [[NSCC]] will not validate the format. The following 
algorithm should be followed: 
• Alpha–1 byte–valued with an “S” 
• Submitting Firm Number-4 bytes 
• Last digit of current year-1 byte 
• Julian Date-3 bytes 
• Sequence Number-11 bytes 
[[DTCC]] does not validate control numbers 
Anticipated [[settlement]] Date Provided by the Fund on Confirmation. The non-binding date when the fund anticipates 
settling this invoice. 
 

---

## Page 50

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: August 3, 2023 
Publication Code: MFS309  
Service: [[DTCC]] Payment aXis® 
Title: Chapter 2: Invoicing and Fee [[settlement]] User Guide / Best Practices 
 
For More Information 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
  