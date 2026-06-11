---
title: "AIP Best Practice Guide – Full Edition"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/AIP-Best-Practice-Guide-Full-Edition.pdf"
pages: 37
size: "722.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# AIP Best Practice Guide – Full Edition

**Original File:** [AIP-Best-Practice-Guide-Full-Edition.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/AIP-Best-Practice-Guide-Full-Edition.pdf)  
**Category:** Other  
**Total Pages:** 37  
**File Size:** 722.2 KB  

---

## Page 1

 [[DTCC]] Public (White) 
 
 
 
ALTERNATIVE INVESTMENT 
PRODUCTS 
BEST PRACTICE USER GUIDE – FULL EDITION 
 
MAY 16, 2023 
 


---

## Page 2

 
 [[DTCC]] Public (White) 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: May 16, 2023 
Publication Code: AIP107 
Service: Alternative Investment Products 
Title: Best Practice Guide – Full Edition 
 

---

## Page 3

 
 [[DTCC]] Public (White) 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 5 
Security General Profile ...................................................................................................................................... 6 
Best Practice for the Share Class Usage on the Security General Profile .......................................................... 6 
Best Practice for the Set-up of the Dummy [[CUSIP]] Number............................................................................... 6 
Security Announcement ...................................................................................................................................... 7 
[[Hedge Fund]] Purchases ...................................................................................................................................... 7 
Trade Date/Dealing Date – (Business Date) ..................................................................................................... 7 
Trade Date/Dealing Date – (Calendar Date) ..................................................................................................... 7 
NTR/BDC Redemptions ...................................................................................................................................... 8 
Security Contact ................................................................................................................................................... 9 
Activity & Distribution ....................................................................................................................................... 10 
Important Fields ................................................................................................................................................ 10 
(Share & Money) Debit/Credit Indicator ............................................................................................................ 11 
Capital Balance Funds – Debit/Credit Indicators .............................................................................................. 12 
Unitized Funds – Debit/Credit Indicators .......................................................................................................... 14 
Withholding Reporting ....................................................................................................................................... 16 
Class-to-Class Conversions ............................................................................................................................. 18 
Fund Assessed Fee .......................................................................................................................................... 19 
Position ............................................................................................................................................................... 20 
Account Registration ......................................................................................................................................... 21 
Account Responsibilities ................................................................................................................................... 23 
Responsibility Models ...................................................................................................................................... 24 
Orders .................................................................................................................................................................. 27 
[[Hedge Fund]] Purchases - Order with Registration ............................................................................................ 27 
Fund Acknowledgement .................................................................................................................................. 27 
Load Types ...................................................................................................................................................... 27 
Registration Fields ........................................................................................................................................... 27 
Contract Note .................................................................................................................................................. 27 

---

## Page 4

 
 [[DTCC]] Public (White) 
NTR/BDC Redemptions – Order ...................................................................................................................... 27 
Fund Exits........................................................................................................................................................ 28 
Miscellaneous .................................................................................................................................................. 28 
Private [[Equity]] – Order ...................................................................................................................................... 28 
Commitment Order Process ............................................................................................................................ 28 
Capital Call Order Process .............................................................................................................................. 29 
Delayed NAV Purchases .................................................................................................................................. 29 
Process Flow ................................................................................................................................................... 30 
Best Practices for Regular Processing ............................................................................................................ 30 
Best Practices for Exception Processing ........................................................................................................ 31 
Placement Fee Order Processing ..................................................................................................................... 31 
Net/Gross Indicator Usage ............................................................................................................................... 31 
Account Transfer................................................................................................................................................ 33 
Transaction Type Descriptions ......................................................................................................................... 33 
Miscellaneous .................................................................................................................................................. 33 
Transfer Types ................................................................................................................................................ 34 
Process Flow Types .......................................................................................................................................... 34 
Daily Funds – Process Flow Indicator (0 – REITS/BDC Processing) ............................................................. 34 
Periodic Funds – Process Flow Indicator (1 – [[Hedge Fund]] Processing) ........................................................ 34 
Document Transfer ............................................................................................................................................ 36 
Process Flow ................................................................................................................................................... 36 
Best Practices ................................................................................................................................................. 36 
 

---

## Page 5

Best Practice User Guide – Full Edition 
 
Introduction 5 
 [[DTCC]] Public (White) 
INTRODUCTION 
This guide is intended to document best practices that have been agreed upon by subcommittees and/or the 
AIP Roundtable committee. It is not intended to provide mandatory system requirements or explain how 
transactions work – the AIP Data Dictionary and Transactions Flows, respectively, provide detailed information 
on each. 
This guide documents common, agreed upon and/or expected client usage of AIP transactions that are not 
system requirements. The information contained here should be considered when transactions and records are 
being implemented. 
AIP documentation, including this guide, the Data Dictionary and the Transactions Flows can be found on 
http://www.[[DTCC]].com/aip
. 
 

---

## Page 6

Best Practice User Guide – Full Edition 
 
Security General Profile 6 
 [[DTCC]] Public (White) 
SECURITY GENERAL PROFILE  
Best Practice for the Share Class Usage on the Security General 
Profile 
The Fund ‘Share Class’ will be populated in the Share Class field on the Security General Profile 
• For Example, the Share Class Field will only display the value ‘A’ 
• The word ‘Class’ will not be included in the Share Class field 
• The Share Class should be included in both the Security Issue Name and the Share Class field 
Best Practice for the Set-up of the Dummy [[CUSIP]] Number 
Unregistered - When the fund is ‘unregistered’, it does not have a valid [[CUSIP]], therefore the Security Identifier 
should be established with the value (4 = Custom) 
• This is to identify the fund has an unregistered dummy number 
• A new [[NSCC]] Security Issue Number will be assigned for the unregistered fund 
 
Registered [[CUSIP]] - When the fund is ‘registered’ and has a valid [[CUSIP]] number, the Security Identifier should 
be changed to (3 = [[CUSIP]]) and the Security Issue [[ID]] should be updated with the valid [[CUSIP]] number 
 
• This is to identify that the fund has a valid registered [[CUSIP]] 
• An updated Security General Profile record will be sent with the new Security Identifier and Security Issue 
[[ID]] 
• Funds will also communicate the updated [[CUSIP]] to the firms outside of AIP to ensure they are aware of 
the change 
 
 

---

## Page 7

Best Practice User Guide – Full Edition 
 
Security Announcement 7 
 [[DTCC]] Public (White) 
SECURITY ANNOUNCEMENT 
[[Hedge Fund]] Purchases 
1. Individual vs. Recurring Announcements – Rather than try to build complex and varying logic for recurring 
Security Announcements dates into the record, functionality is included in the AIP Web Platform to set-up 
future-dated announcements and should be used by Funds and Fund Administrators 
2. Trade Date/Dealing Dates – There are two types of Trade Dates/Dealing Dates to accommodate existing 
convention and support system limitations. The two types are Trade Date/Dealing Date (Business Date) 
and Trade Date/Dealing Date (Calendar Date) 
Trade Date/Dealing Date – (Business Date) 
The Trade Date/Dealing Date – (Business Date) must be a valid [[settlement]] date and is generally used by the 
Firm to process trades. 
Examples: 
o If the 1st of the month falls on a (Saturday, Sunday, or Holiday), the user will populate the 
Trade Date/Dealing Date – (Business Date) with the next available business date 
o If the 1st of the month falls on a normal business date (Monday thru Friday), the user will populate 
the Trade Date/Dealing Date – (Business Date) with the 1st of the month. 
 
Trade Date/Dealing Date – (Calendar Date) 
The Trade Date/Dealing Date – (Calendar Date) is always the date specified in the fund documentation and 
can fall on a Saturday, Sunday, or Holiday. It is generally used by the Fund or Fund Administrators to process 
trades. 
Examples: 
o If the 1st of the month falls on a (Saturday, Sunday, or Holiday), the user will populate the 
Trade Date/Dealing Date (Business Date) with the next available business date. The Trade 
Date/Dealing Date (Calendar Date) should be populated with the 1st of the month. 
o If the 1st of the month falls on a normal business date (Monday thru Friday), the user will populate 
the Trade Date/Dealing Date (Business Date) with the same date as the Trade Date/Dealing 
Date (Calendar Date). 
 
 
To avoid reporting and tax issues, the Trade Date/Dealing Date (Business Date) and Trade Date/Dealing Date 
(Calendar Date) should occur in the same month. 

---

## Page 8

Best Practice User Guide – Full Edition 
 
Security Announcement 8 
 [[DTCC]] Public (White) 
NTR/BDC Redemptions 
1. There are two Security Announcement types that should be used as indicated below: 
a. Quarterly or monthly redemptions should use Announcement Type = 01 Tender Offer/Redemption, 
which is a non-recurring event 
b. Daily redemptions should use Announcement Type = 17 Recurring Redemption with a Recurring 
Transaction Frequency = 00 Daily 
i. For these Orders, the Firm should specify the Trade Date and [[settlement]] Date with 
recommended timing being T+3 to allow for processing (acknowledgement, confirmation, money 
[[settlement]], etc.) 
2. In cases where the redemption period is ‘active’, but the fund is restricting new redemption requests, the 
Security Announcement should remain active, and the fund should reject orders as needed; the Security 
Announcement should not be deleted 
3. In AIP, the last point for Firm (and Fund) Exits is C98 at 7pm ET, the processing day before the 
[[settlement]] Date. However, this cut-off can be superseded if the Fund populates an earlier date for the 
Rescission Date, which should be treated as the last day for Firm Corrections or Firm Exits 
 
 

---

## Page 9

Best Practice User Guide – Full Edition 
 
Security Contact 9 
 [[DTCC]] Public (White) 
SECURITY CONTACT  
The following fields must be provided on the Contact record, even though the fields are ‘optional’: 
 
Field Value 
Contact Name/Address Line 1 of Record 1 thru 5 Should only reflect the Contact Name 
Address Line 1,2,3 of Record 1 thru 5 Should only reflect the Street Address 
Contact City of Record 1 thru 5 Should reflect the City 
Contact Zip/Postal Code of Record 1 thru 5 Should reflect the Zip Code 
Contact Telephone Number of Record 1 thru 5 Should reflect the Telephone Number (no dashes i.e., 8134445555) 
Contact Email address of Record 1 thru 5 Should reflect the Email address, if applicable 
 
 

---

## Page 10

Best Practice User Guide – Full Edition 
 
Activity & Distribution 10 
 [[DTCC]] Public (White) 
ACTIVITY & DISTRIBUTION  
Important Fields 
 
Field Description 
Fund/Firm Account Number Field • Firm Account number should always be populated 
• Firms will accept and store Fund Account numbers if included in the 
record; both should be populated if available 
Effective Date (Business 
Date) Field (short term 
solution) 
Preferred Methods: 
• Populate with the Trade Date 
• Populate with the processing date, in which Trade Date will be listed in 
the “Original Trade Date/Payable Date for Adjustments” field 
 
Example 1: A [[Dividend]] adjustment should contain: 
• Payable Date Field: 01/30/2017 (Date the adjustment is eligible to be paid) 
• Effective Date Field: 01/30/2017 (New Trade Date) 
• Original Trade Date/Payable Date for Adjustment Field: 12/30/2016 (Date 
of the original trade/distribution) 
 
Example 2: A [[Dividend]] adjustment should contain: 
• Payable Date Field: 12/30/2017 (Date the adjustment is eligible to be paid) 
• Effective Date Field: 12/30/2017 (Process Date) 
• Original Trade Date/Payable Date for Adjustment Field: 12/30/2017 
(Trade Date) 
Payable Date Field This field is determined by the Fund 
Share Quantity Field Share Quantity should always be populated to include Capital Balance as $1 per 
share with the exception for Cash Distributions or Cash Adjustments transactions 
(see table below for list of transactions) 
 
 
Example: Capital Bank Fund submitting Transaction Type = 01 Direct Purchase 
of 10000.00: 
• Share Quantity field: 10000.00 
• Money Amount field: 10000.00 
• Price per Share field: 1.0 
Money Amount Field • Money Amount field should always be populated for Cash 
Distribution transactions 
• MRO Users must be aware of adding the additional 00 after the implied decimal 

---

## Page 11

Best Practice User Guide – Full Edition 
 
Activity & Distribution 11 
 [[DTCC]] Public (White) 
Field Description 
Price per Share • Should be populated for Direct Purchases 
• Capital Balance Funds should be populated as $1 per share 
 
Example: Capital Bank Fund submitting Transaction Type = 01 Direct Purchase 
of 10000.00: 
• Share Quantity field: 10000.00 
• Money Amount field: 10000.00 
• Price per Share field: 1.00 
Estimated or Actual Value Indicator • Funds should send actual values vs. estimated values for transactions 
• If an estimated value is sent, should be populated with “1 = Estimated” 
• Records sent with this value blank will be assumed as “Actual” 
Account Registration Name – 
Extended Field 
If this field is used, the account registration must start from the beginning 
(full account registration name) and entered in its entirety 
• *Account Registration Name formatting is usually driven by what is sent by the 
firm* 
Related Control Number Field When available this field should be populated for a Cancellations, and 
distribution adjustments/reversals, if available 
SSN/EIN/TIN Number Field Although not required, the [[investor]] SSN, TIN, or EIN should be populated 
as best practice 
Record Date Field Should be populated for distributions of funds with record dates 
Adjustment Indicator Field • Related control number should be provided if available 
• Adjustment Indicator field [[Option]] “1 = Adjustment” should be populated for 
AIP distribution adjustments 
Adjustment Indicator field [[Option]] “2 = Reversal” should be populated for 
distribution cancellations 
[[Dividend]] Reporting Use Transaction Type “59 = [[Dividend]] Cash” for cash [[Dividend]] distributions and 60 
• = [[Stock]] [[Dividend]] for dividends paid in [[shares]] 
 
(Share & Money) Debit/Credit Indicator 
The Activity & Distribution is used by Funds and Fund Administrators to report periodic reconciliation of the 
investors share and account balance to the Firms. This will ensure that both the Fund and Firms books are 
reflecting the most recent information for the [[investor]]’s statements. 
Step 1: The Fund is responsible to send an Activity & Distribution record to report any financial or non-financial 
transactions at the [[investor]] level. 
Step 2: The Fund will send the appropriate Activity Transaction Type to report a Distribution, Adjustment, 
Activity or Withholdings for the [[investor]]. 
Step 3: The Fund will provide the appropriate Share Debit/Credit and/or Money Debit/Credit Indicator to reflect 
which party will be debited or credited for the transaction. 

---

## Page 12

Best Practice User Guide – Full Edition 
 
Activity & Distribution 12 
 [[DTCC]] Public (White) 
Note: 
The Activity & Distribution transaction can be settling, which means monies will be debited and credited via AIP. If the 
transaction is ‘non-settling’, the monies will be settled outside of the AIP application. 
Step 4: If the Fund is ‘Unitized’ the Share Debit/Credit Indicator will be populated  
Share Debit/Credit Indicator 
• 1 = Debit Firm/Credit Fund – Decrease SHARE to FIRM (Redemption, Reversals, Adjustments, Purchase 
Cancellation) 
• 2 = Debit Fund/Credit Firm – Increase SHARE to FIRM  
(Purchase, Adjustments, Redemption Cancellation, [[Dividend]] Reinvestments)  
 
Step 5: If the Fund is ‘Capital Balance’’ the Money Debit/Credit Indicator will be populated 
Money Debit/Credit Indicator 
• 1 = Debit Firm/Credit Fund – Decrease MONEY to FIRM (Purchase, Reversals, Adjustments, Redemption 
Cancellation, Call Event – Client Debit) 
• 2 = Debit Fund/Credit Firm – Increase MONEY to FIRM (Redemption, Adjustments, Purchase 
Cancellation, Cash Dividends) 
 
Note: 
For Reinvested Distributions, both the Share Debit/Credit and Money Debit/Credit Indicator will be populated. 
Step 6: Below is a list of various AIP Transaction Types and their descriptions which outlines what the Funds 
will populate in the Share Quantity, Money Amount, Share Debit/Credit and/or Money Debit/Credit Indicator 
fields, when transmitting the Activity & Distribution record to the Firms. The chart is separated based on if the 
fund is Capital Balance (Non-Unitized) or Unitized. 
Capital Balance Funds – Debit/Credit Indicators 
Adjustments 
Transaction 
Description 
AIP Transaction 
Types 
Share 
Quantity 
Money 
Amount 
Share Debit/Credit 
Indicator 
Money Debit/Credit 
Indicator 
Increase Div 
Reinvest 
29 Yes Yes 2 2 
Decrease Div 
Reinvest 
29 Yes Yes 1 1 
Increase Div Cash 59 No Yes spaces 2 
Decrease Div 
Cash 
59 No Yes spaces 1 

---

## Page 13

Best Practice User Guide – Full Edition 
 
Activity & Distribution 13 
 [[DTCC]] Public (White) 
Adjustments 
Increase LTG 
Reinvest 
55 Yes Yes 2 2 
Decrease LTG 
Reinvest 
55 Yes Yes 1 1 
Increase LTG 
Cash 
56 No Yes spaces 2 
Decrease LTG 
Cash 
56 No Yes spaces 1 
Increase STG 
Reinvest 
57 Yes Yes 2 2 
Decrease STG 
Reinvest 
57 Yes Yes 1 1 
Increase STG 
Cash 
58 No Yes spaces 2 
Decrease STG 
Cash 
58 No Yes spaces 1 
 
 
Activity (Non-Distribution) 
Transaction Description AIP 
Transaction 
Types 
Share 
Quantity 
Money 
Amount 
Share 
Debit/Credit 
Indicator 
Money 
Debit/Credit 
Indicator 
Reinvested Div 29 Yes Yes 2 2 
Cash [[Dividend]] 59 No Yes Blank 2 
Redemption 02 Yes Yes 1 2 
Cancel Redemption 25 Yes Yes 2 1 
Purchase 01 Yes Yes 2 1 
Cancel Purchase 24 Yes Yes 1 2 
Exchange In 01 Yes Yes 2 1 
Exchange Out 02 Yes Yes 1 2 
Cancel Exchange In 24 Yes Yes 1 2 
Cancel Exchange Out 25 Yes Yes 2 1 
Non-Taxable 
Exchange Purchase 
23 Yes Yes 2 1 

---

## Page 14

Best Practice User Guide – Full Edition 
 
Activity & Distribution 14 
 [[DTCC]] Public (White) 
Activity (Non-Distribution) 
Non-Taxable 
Exchange Redeem 
02 Yes Yes 1 2 
Cancel Non-Taxable 
Exchange Purch 
24 Yes Yes 1 2 
Cancel Non-Taxable 
Exch Redeem 
25 Yes Yes 2 1 
Call Event - Client Debit 72 Yes Yes 2 1 
 
 
Withholding 
Transaction 
Description 
AIP Transaction 
Types 
Share 
Quantity 
Money 
Amount 
Share Debit/Credit 
Indicator 
Money Debit/Credit 
Indicator 
Increase 
[[Dividend]] w/h 
59, 60 Yes Yes 2 2 
Decrease 
[[Dividend]] w/h 
29, 55, 57 Yes Yes 1 1 
 
 
Unitized Funds – Debit/Credit Indicators 
 
Adjustments 
Transaction 
Description 
AIP Transaction 
Types 
Share 
Quantity 
Money 
Amount 
Share Debit/Credit 
Indicator 
Money Debit/Credit 
Indicator 
Increase Div 
Reinvest 
29 Yes Yes 2 2 
Decrease Div 
Reinvest 
29 Yes Yes 1 1 
Increase Div Cash 59 No Yes spaces 2 
Decrease Div 
Cash 
59 No Yes spaces 1 
Increase LTG 
Reinvest 
55 Yes Yes 2 2 
Decrease LTG 
Reinvest 
55 Yes Yes 1 1 
Increase LTG 
Cash 
56 No Yes spaces 2 
Decrease LTG 
Cash 
56 No Yes spaces 1 

---

## Page 15

Best Practice User Guide – Full Edition 
 
Activity & Distribution 15 
 [[DTCC]] Public (White) 
Adjustments 
Increase STG 
Reinvest 
57 Yes Yes 2 2 
Decrease STG 
Reinvest 
57 Yes Yes 1 1 
Increase STG 
Cash 
58 No Yes spaces 2 
Decrease STG 
Cash 
58 No Yes spaces 1 
Increase [[Stock]] 
Div 
60 Yes No 2 spaces 
Decrease [[Stock]] 
Div 
60 Yes No 1 spaces 
 
Activity (Non-Distribution) 
Transaction Description AIP Transaction 
Types 
Share 
Quantity 
Money 
Amount 
Share Debit/Credit 
Indicator 
Money 
Debit/Credit 
Indicator 
Reinvested Div 29 Yes Yes 2 2 
Cash [[Dividend]] 59 No Yes Blank 2 
Redemption 02 Yes Yes 1 2 
Cancel Redemption 25 Yes Yes 2 1 
Purchase 01 Yes Yes 2 1 
Cancel Purchase 24 Yes Yes 1 2 
Exchange In 01 Yes Yes 2 1 
Exchange Out 02 Yes Yes 1 2 
Cancel Exchange In 24 Yes Yes 1 2 
Cancel Exchange Out 25 Yes Yes 2 1 
Non-Taxable 
Exchange Purchase 
23 Yes Yes 2 1 
Non-Taxable 
Exchange Redeem 
02 Yes Yes 1 2 
Cancel Non- Taxable 
Exchange Purch 
24 Yes Yes 1 2 
Cancel Non- Taxable 
Exch Redeem 
25 Yes Yes 2 1 
Call Event – Client Debit 72 Yes Yes 2 1 
 
 

---

## Page 16

Best Practice User Guide – Full Edition 
 
Activity & Distribution 16 
 [[DTCC]] Public (White) 
Withholding 
Transaction 
Description 
AIP Transaction 
Types 
Share 
Quantity 
Money 
Amount 
Share Debit/Credit 
Indicator 
Money Debit/Credit 
Indicator 
Increase 
[[Dividend]] w/h 
59, 60 Yes Yes 2 2 
Decrease 
[[Dividend]] w/h 
29, 55, 57 Yes Yes 1 1 
 
Withholding Reporting 
Note:  
The effective date for industry implementation will be Monday April 8, 2024. 
Reinvested Distributions with Withholding when the Firm is the Withholding Agent would be processed as two 
separate transactions in the same cycle: 
• T ransaction #1  
o Transaction Type 29 = [[Dividend]] Reinvestment would be used to report a reinvested [[Dividend]] 
transaction with withholding (non-settling) 
o The following fields should be populated 
» Backup Withholding Indicator 
» Backup Withholding Amount 
» Total Distribution Amount (will reflect the total taxable amount of the transaction) 
 
• Transaction #2 
o Transaction Type 63 = Withholding for Reinvested Accounts would be used to report the 
withholding component and would be linked to Transaction Type 29 = [[Dividend]] Reinvestment by the 
Related Control Number (can be settling or non-settling) 
o The following fields will be required 
» Backup Withholding Indicator 
» Backup Withholding Amount 
» Related Control Number 
 
Reinvested Distributions with Withholding when the Fund is the Withholding Agent would be processed as one 
non-settling transaction: 
o Transaction Type 29 = [[Dividend]] Reinvestment would be used to report a reinvested [[Dividend]] 
transaction with withholding  
o The following fields should be populated 
» Backup Withholding Indicator 
» Backup Withholding Amount 
» Total Distribution Amount (will reflect the total taxable amount of the transaction) 

---

## Page 17

Best Practice User Guide – Full Edition 
 
Activity & Distribution 17 
 [[DTCC]] Public (White) 
 
Cash Distributions with Withholding when the Firm or Fund is the Withholding Agent would be processed as 
one settling or non-settling transaction: 
o Transaction Type 59 = [[Dividend]] Cash would be used to report a cash [[Dividend]] transaction with 
withholding 
o The following fields should be populated 
» Backup Withholding Indicator 
» Backup Withholding Amount 
» Total Distribution Amount (will reflect the total taxable amount of the transaction) 
 
Backup Withholding Scenarios: 
• Firm W/H Agent – Two Activity records are required to execute a Reinvested Distribution with 
Withholding. One Activity record is required to execute a Cash Distribution with Withholding. 
Fields [[Dividend]] Reinvestment 
Transaction Values 
Withholding Only 
Transaction with Related 
Control Number Values 
Cash [[Dividend]] Transaction 
Values 
Record Type 50 = Activity & Distribution 50 = Activity & Distribution 50 = Activity & Distribution 
Transaction Type 29 = [[Dividend]] Reinvestment 63 = Withholding for 
Reinvested Accounts 59 = [[Dividend]] Cash 
Control Number 00009429100200000001 00009429100200000002 00009429100200000005 
Account Number FH736B2 FH736B2 FH736B2 
[[settlement]] 
Indicator 2 = Non-Settling (ONLY) 1 = Settling or 2 = Non-
Settling 
1 = Settling or 2 = Non-
Settling  
Backup 
Withholding 
Indicator 
(Required for 
Withholding Only 
Transaction) 
1 = NRA, 2 = Tefra Backup, 
3 = Tefra Pension 
1 = NRA, 2 = Tefra Backup, 
3 = Tefra Pension 
1 = NRA, 2 = Tefra Backup, 
3 = Tefra Pension 
Backup 
Withholding 
Amount 
(Required for 
Withholding Only 
Transaction) 
10.00 10.00 10.00 
Money Amount 100.00 10.00 110.00 
Share Quantity 9.0000 Blank Blank 
Total Distribution 
Amount 110.00 Blank 110.00 
Share 
Debit/Credit 
Indicator 
2 = Debit Fund / Credit Firm Blank Blank 
Money 
Debit/Credit 
Indicator 
2 = Debit Fund / Credit Firm 2 = Debit Fund / Credit Firm 2 = Debit Fund / Credit Firm 

---

## Page 18

Best Practice User Guide – Full Edition 
 
Activity & Distribution 18 
 [[DTCC]] Public (White) 
Related Control 
Number 
(Required for 
Withholding Only 
Transaction) 
Blank 
00009429100200000001 * 
*Ties back to the original 
reinvest transaction 
Blank 
 
• Fund W/H Agent – One Activity record is required to execute a Reinvested Distribution with Withholding. 
One Activity record is required to execute a Cash Distribution with Withholding. 
Fields [[Dividend]] Reinvestment Transaction 
Values 
Cash [[Dividend]] Transaction Values 
Record Type 50 = Activity & Distribution 50 = Activity & Distribution 
Transaction Type 29 = [[Dividend]] Reinvestment 59 = [[Dividend]] Cash 
Control Number 00009429100200000003 00009429100200000007 
Account Number FH736B2 FH736B2 
[[settlement]] Indicator 2 = Non-Settling (ONLY) 1 = Settling or 2 = Non-Settling  
Backup Withholding 
Indicator 
1 = NRA, 2 = Tefra Backup, 3 = Tefra 
Pension 
1 = NRA, 2 = Tefra Backup, 3 = Tefra 
Pension 
Backup Withholding 
Amount 10.00 10.00 
Money Amount 100.00 100.00 
Share Quantity 9.0000 Blank 
Total Distribution 
Amount 110.00 110.00 
Share Debit/Credit 
Indicator 2 = Debit Fund / Credit Firm Blank 
Money Debit/Credit 
Indicator 2 = Debit Fund / Credit Firm 2 = Debit Fund / Credit Firm 
 
Class-to-Class Conversions 
• Share Class Exchanges within the same fund family  
o Funds send two Activity Records via AIP in the same file: 
» 1 st record:  51 = Share Class Exchange Out 
» 2 nd record: 22 = Share Class Exchange In 
• Both transactions should be sent in the same AIP cycle 
» Non-settling 
» Taxable Indicator should be 0 = No  
» Related Control Number field should be provided for each corresponding “Share Class 
Exchange” transaction 
• Feeder Exchanges within the same fund family 
o Funds send two Activity records via AIP in the same file: 
» Activity Type 46 = Swap Out  
» Activity Type 45 = Swap In 

---

## Page 19

Best Practice User Guide – Full Edition 
 
Activity & Distribution 19 
 [[DTCC]] Public (White) 
» Non-settling 
» Taxable Indicator should be 1 = Yes 
• Fund Mergers 
o If the new fund will be on AIP, utilize Activity Type 23 = Fund Merger Activity with New [[NSCC]] [[ID]] and 
populate the new [[NSCC]] [[ID]] in the Cross Security [[NSCC]] [[ID]] field 
o If the new fund will not be on AIP, utilize Activity Type 71 = Fund Merger Activity without New [[NSCC]] 
[[ID]] and [[DO]] not populate the Cross Security [[NSCC]] [[ID]] field since it’s not on AIP 
o Activity Type 68 = [[Cash-in-Lieu]] should be settling and used to return any partial [[shares]] as cash 
 
Fund Assessed Fee 
The Fund Assessed Fee Amount should be processed as one transaction. 
Fund Assessed Fee Scenarios: 
• Fund Assessed Fee – One Activity record is required to execute this process. 
Fields [[Dividend]] Reinvestment 
Transaction Values 
Cash [[Dividend]] Transaction Values 
Record Type 50 = Activity & Distribution 50 = Activity & Distribution 
Transaction Type 29 = [[Dividend]] Reinvestment 59 = [[Dividend]] Cash 
Control Number 00009219100200000005 00009219100200000006 
Account Number FH736B2 FH736B2 
[[settlement]] Indicator 2 = Non-Settling (ONLY) 1 = Settling or 2 = Non-Settling 
Fund Assessed Fee Amount 10.00 10.00 
Money Amount 100.00 100.00 
Share Quantity 9.0000 Blank 
Total Distribution Amount 110.00 110.00 
Share Debit/Credit Indicator 2 = Debit Fund / Credit Firm Blank 
Money Debit/Credit Indicator 2 = Debit Fund / Credit Firm 2 = Debit Fund / Credit Firm 
 
 

---

## Page 20

Best Practice User Guide – Full Edition 
 
Position 20 
 [[DTCC]] Public (White) 
POSITION  
 
Field Description 
DOL Enhancement Fields The following fields are optional but should be provided information if available: 
• Account Open Date 
• Account Type 
• Account Representative/Advisor Number 
• Account Representative/Advisor Name 
• Branch [[ID]] Number 
Negative Balance Reporting Negative Position Balances are not allowed in AIP 
NAV Effective Should be populated if not utilizing the valuation record with last reported NAV Date 
NAV Field Should be populated if not utilizing the valuation record with last reported NAV 
Fund/Firm Account Number Field Firm Account number should always be populated 
Firms will accept and store Fund Account numbers if included in the record; both 
should be populated if available 
Closing Share Balance Field Should always be populated for both Capital Balance and Unitized funds 
Closing Money Amount Field Should be populated for Capital Balance funds 
Invested Value Field If populated, should be populated with the total contribution amount 
Account Registration Name – 
Extended Field 
When populated should start the name from the beginning 
SSN/TIN/EIN Number Field Although not required, the [[investor]] SSN, TIN, or EIN should be populated as best 
practice 
 
 
 

---

## Page 21

Best Practice User Guide – Full Edition 
 
Account Registration 21 
 [[DTCC]] Public (White) 
ACCOUNT REGISTRATION  
 
Field Description 
New Firm Account 
Number Field 
• The “New Firm Account Number” field should only be populated on 053 = Account 
Maintenance record 
• Plan type or Owner type change should be processed as Account Transfers 
• Correction to an account number should be sent as a 053 = Account Maintenance 
record. The old/incorrect account number will be populated on the “Firm Account 
Number” field and the new/correct account number in the “New Firm Account Number” 
field 
 
Examples for field usage: 
• Account number changes which involve a new and previous account have same 
[[Broker]]/advisor and same registration type (i.e., change from a self-managed account to a 
managed account or vice versa) 
• Account number change – new and previous account have different [[Broker]]/advisor and 
same registration type 
Fund Account Number 
Field 
Fund will provide on the 026 = Registration Acknowledgement record if available 
Firm Account Number 
Field 
Fund will populate on the 026 = Registration Acknowledgement record 
Account 
Representative/Advisor 
Name Field 
Firm should include Account Representative/Advisor Name 
Account 
Representative/Advisor 
Number Field 
Firm should include the Account Representative/Advisor Number 
Branch [[ID]] Number 
Field 
Branch [[ID]] Number field should be included if available 
Firm CRD Number 
Field 
Firm should avoid populating with all zeros when no CRD Number is available 
[[Dividend]] [[Option]] Field Firm should populate when known and applicable. If left blank fund will elect the fund 
[[default]] [[Option]] 
Owner DOB Field Owner date of birth should be provided if available 
Custodian Name Field Custodian Name field should be populated 
Custodian Tax 
Identification Number 
Field 
Custodian Tax [[ID]] should be populated 

---

## Page 22

Best Practice User Guide – Full Edition 
 
Account Registration 22 
 [[DTCC]] Public (White) 
Field Description 
Individual 
CRD/IARD 
Number Field 
If a shared representative, the lead/primary presentative [[ID]] should be used 
Account 
Registration 
Name Field 
Begin with the Custodian Name 
Address information should not be included in the account registration field Include Account 
Type 
Formatting for domestic and foreign accounts should be the same 
Address of 
Records fields 
(Until 
Enhancements 
are 
implemented) 
The City/State should go in the line(s) directly after the street address: 
 
 
Phone Number of 
Record Field 
Phone Number should be provided 
If populated, should be left justified and include area code & country code for non-US [[DO]] not 
include dashes; pad with spaces not zeros 
Email Address 
of Record Field 
Email address should be provided 
Address Type of 
Record 2- 5 
Fields 
Funds should be notified via the Account Maintenance record of any temporary changes to 
mailing address 
If 02 = Secondary (Mailing) is selected, all account correspondence will go to that mailing 
address 
If the mailing address is not different from Primary address listed, it should not be duplicated 
on the same record 
Foreign addresses with Provinces should be included in the “City of Record” field 
 


---

## Page 23

Best Practice User Guide – Full Edition 
 
Account Registration 23 
 [[DTCC]] Public (White) 
Account Responsibilities 
Category Definition and Examples 
New Account Opening Account creation, TOD, Beneficiary Designation, Trust Documents, 
etc. 
Compliance/Regulatory USA PATRIOT ACT: CIP, AML/[[KYC]], OFAC, FINCEN (or applicable 
country’s compliance and [[regulation]]) 
Mailings Includes mailings for tender offers, capital calls, proxies, and 
regulatory mailings; lost shareholder tracking 
Tax Withholding Includes B and C notices, tax levy/lien, all tax withholding (Federal 
and State mandated, NRA and FATCA/backup) and tax payments 
Tax Reporting Includes sending 1099’s, cost basis reporting, etc. to the [[investor]]; for 
K-1 funds all tax reporting is done by the Fund to the [[investor]] 
regardless of the responsibility level 
Financial Transaction Authorization Includes processing requests or receiving instructions from the 
[[investor]] for purchases, redemptions, transfers, etc. and includes 
money [[settlement]] 
Account Maintenance Authorization Includes processing requests from the [[investor]] for address changes, 
distribution [[Option]] changes, BIN changes, withholding changes, 
registration changes, introducing [[Broker]] dealer changes, etc. 
Front-End Commissions Commissions paid to the [[Broker]]/advisor 
Back-End Payments Payments made ‘after the sale’ to the [[Broker]]/advisor, e.g., trailing 
type fees, service fees, etc. 
[[investor]] Reporting Includes sending trade confirmations, statements, etc. to the 
[[investor]] 
Distribution Payment Instructions Who receives distribution payments and where they go 
Escheatment Responsible for regulatory filings, reporting, due diligence mailings, 
tracking of [[investor]] contact information and transfer of assets to the 
state on behalf of the [[investor]] 
Document Retention Specifies the party responsible for storing documents 
 

---

## Page 24

Best Practice User Guide – Full Edition 
 
Account Registration 24 
 [[DTCC]] Public (White) 
Responsibility Models 
Note:  
Exceptions and additional details or clarifications should be defined in agreements outside of AIP.  
 
Fund Responsibility Model 
Network Control 
Indicator 
Hybrid 
Responsibility 
Indicator Responsibility Category 
Responsible 
Party 
C = Customer Controlled Space = No 
New Account Opening Fund 
Compliance/Regulatory Fund  
Mailings Fund 
Tax Withholding Fund 
Tax Reporting Fund 
Financial Transaction Authorization Fund 
Account Maintenance Authorization Fund 
Front-End Commissions Fund 
Back-End Payments Fund 
[[investor]] Reporting Fund 
Distribution Payment Instructions Fund 
Escheatment Fund 
Document Retention Fund 
 

---

## Page 25

Best Practice User Guide – Full Edition 
 
Account Registration 25 
 [[DTCC]] Public (White) 
Firm Responsibility Model 
Network Control 
Indicator 
Hybrid 
Responsibility 
Indicator Responsibility Category 
Responsible 
Party 
B = [[Broker]] Controlled Space = No 
New Account Opening Firm 
Compliance/Regulatory Firm 
Mailings Firm 
Tax Withholding Firm 
Tax Reporting Firm 
Financial Transaction Authorization Firm 
Account Maintenance Authorization Firm 
Front-End Commissions Firm 
Back-End Payments Firm 
[[investor]] Reporting Firm 
Distribution Payment Instructions Firm 
Escheatment Firm 
Document Retention Firm 
 

---

## Page 26

Best Practice User Guide – Full Edition 
 
Account Registration 26 
 [[DTCC]] Public (White) 
Hybrid Responsibility Model 
Network Control 
Indicator 
Hybrid 
Responsibility 
Indicator Responsibility Category 
Responsible 
Party 
 
 
 
 
 
 
B = [[Broker]] Controlled 
 
 
Note:  
‘Hybrid’ can only be selected 
if the Network Control 
Indicator is B = [[Broker]] 
Controlled  
1 = Yes 
New Account Opening 
Determined by 
Fund & Firm 
Compliance/Regulatory 
Mailings 
Tax Withholding 
Tax Reporting 
Financial Transaction Authorization 
Account Maintenance Authorization 
Front-End Commissions 
Back-End Payments 
[[investor]] Reporting 
Distribution Payment Instructions 
Escheatment 
Document Retention 
 
‘Hybrid Responsibility Indicator’ Usage 
• Because responsibilities are usually defined in agreements and have important impact, Firms can’t 
change the Hybrid Responsibility Indicator by sending an Account Maintenance record with a new value 
for the Hybrid Responsibility Indicator; this should be done outside of AIP 
 
 

---

## Page 27

Best Practice User Guide – Full Edition 
 
Orders 27 
 [[DTCC]] Public (White) 
ORDERS  
[[Hedge Fund]] Purchases - Order with Registration 
Fund Acknowledgement 
• The Order and Account Registration should be Fund Acknowledged within 24 hours to either ‘accept’ or 
‘reject’ the trade. 
Load Types 
• If the Load Type Indicator is populated to 9 = Placement Fee, either the Commission Amount or 
Commission Percentage should be populated but the Commission Amount is preferred 
• If the Load Type Indicator is populated to 3 = Front End Load, the following fields are used to populate the 
amount in conjunction with specifying the breakpoints on the Security General Profile: 
• Breakpoint Limit Number 
• Dealer Concession Percentage & Dealer Concession Amount 
Registration Fields 
• The ‘Address Type of Record 1’ should be populated to (01 = Primary). The ‘Address of Record 1 Line’ 
should reflect the shareholder’s physical address used for state reporting. 
• The following fields should be populated to assist in establishing the shareholder’s registration. 
o SSN/TIN/EIN Indicator 
o SSN/TIN/EIN Number 
o Owner Date of Birth 
Contract Note 
• For [[Hedge Fund]] purchases, the Contract Note record will not be used 
NTR/BDC Redemptions – Order 
• For Orders sent on Security Announcement Type = 17 Recurring Redemption, Firms should specify the 
Trade Date and [[settlement]] Date with recommended timing being T+3 to allow for processing, 
acknowledgement, confirmation, money [[settlement]], etc. 
• Orders should be sent as a Full Redemption or a Partial Redemption Request 
• The Share Lot Identifier fields on the Order record should not be used 
• The Dealer Concession, CDSC Amount, and Redemption Fee should not be populated on the Firm Order; 
only the Fund will populate them on the Confirmation if needed 

---

## Page 28

Best Practice User Guide – Full Edition 
 
Orders 28 
 [[DTCC]] Public (White) 
• For ‘exception’ cases where the Redemption Reason won’t be 01 = Regular, Firms should use one of the 
following Redemption Reason codes: 
o 02 = Death 
o 03 = Disability 
o 04 = Hardship 
o 05 = Odd lots 
o 06 = RMD - Required Minimum Distribution 
• Firms should not use Redemption Reason 07 = Other/Unknown Exception unless absolutely necessary 
• ‘Exceptions’ are expected to require paperwork such as death certificate, etc.; however, some firms will 
send documentation on all redemptions 
o Documentation will be sent outside AIP until the AIP E-Doc functionality is implemented, at which 
time it should be used with redemption orders 
Fund Exits 
• If a Fund will be exiting a redemption, they should contact the Firm directly to explain why they are 
sending an exit, which will cancel the transaction 
Miscellaneous 
• Sponsors should have primary exception reasons specified on their paper redemption forms 
• Paying a [[Dividend]] (or similar event) within a redemption period should be discouraged; however, if it 
happens or extra [[shares]] are accrued, they should be included in the request, so that there isn’t money left 
in the account after a full redemption request was processed 
o If a distribution is made after a full redemption is processed, a separate settling Activity record should 
be sent by the Fund 
Private [[Equity]] – Order 
Commitment Order Process 
• Fund should leverage the “ Call/Commitment Fund Indicator” on the Security General Profile to identify 
whether the fund is a call/commitment fund prior to the opening of a Security Announcement for a 
Commitment Order 
• The Security Announcement should be open-ended/future dated for the [[settlement]] Date and other 
applicable fields so the Fund can apply the correct [[settlement]] Date in the Order process once the close 
date is known 
• Subsequent Commitment Orders that have previously sent an Account Registration for the Commitment 
order will be sent as stand-alone Order and will not require registration but will require the “Account 
Registration Name” field to be populated 
• Trade Date (Business Date) will be populated with the commitment [[Close Out]] date 
• [[settlement]] Date will be needed to [[Close Out]] the transaction in AIP although there is no money [[settlement]] 
• Money Amount will be populated with the [[investor]] commitment amount 

---

## Page 29

Best Practice User Guide – Full Edition 
 
Orders 29 
 [[DTCC]] Public (White) 
• Trade Date (Calendar Date) may be used in certain scenarios when necessary 
• Firms will expect Total Commitment, Fulfilled Commitment and Remaining Commitment fields to be 
populated on the 052 = Position record once Commitment Orders are completed  
o Reporting should begin after initial call has been made and the commitment period has been closed  
• Placement fees and commission fields will remain optional and may be populated if necessary 
• In the case of prorated commitment amounts, the Fund will send multiple Order Confirmation records 
Capital Call Order Process 
• The Security Announcement should be open-ended/future dated for the [[settlement]] Date and other 
applicable fields so the Fund can apply the correct [[settlement]] Date in the Order process when known 
• Activity and Distribution Transaction Type 72 = Call Event Client Debit 
o Firms that leverage the information received in this Activity record will populate [[settlement]] Date and 
Activity Related Control Number on the Capital Call Order  
o Firms that don’t leverage the information received in this Activity record will need the Fund to update 
the correct [[settlement]] Date on the Order Confirmation record 
• Trade Date (Business Date) on the order should be populated with be the date the Capital Call Order is 
submitted 
• [[settlement]] Date should be the funding due date  
• If necessary, Funds will provide updated Share Amount on the Order Confirmation record 
• If commission amount for the transaction is not known, the Commission Amount field on the order should 
be left blank ([[DO]] not populate with 0’s) 
• Although not required, RIA/RR information may be provided to the Fund on the order  
o If a new RIA/RR information needs to be reported, it should be updated via the Account Maintenance 
record 
• After the Capital Call Order is complete, the Firm will expect the Fund to report the invested balance that 
is pending valuation on the “Pending Money Value” field on the Position record  
Delayed NAV Purchases  
Delayed NAV Purchases are AIP Orders where there is a purchase into a fund, usually a BDC with a monthly 
offering period, that will not strike a NAV until several weeks after the trade date and money [[settlement]] date; 
additionally, there is not an escrow fund.  For example, for a September 1 trade date period, [[settlement]] would 
occur on August 28 and the NAV would be struck on September 21. 

---

## Page 30

Best Practice User Guide – Full Edition 
 
Orders 30 
 [[DTCC]] Public (White) 
Process Flow 
 
 
Note:  
AIP Orders will complete on [[settlement]] Date and the final NAV/[[shares]] will be reported on a non-settling Activity record a 
few weeks later  
 
Best Practices for Regular Processing 
• On the Order Confirmation, the ‘Estimated or Actual Value Indicator’ should be populated with 1 = 
Estimated  
• The price on the Order Confirmation should be based on the previous month’s NAV 
• On the Activity record, the ‘Related Control Number’ should be populated with the Control Number of the 
Order 
• Position records should not be sent on any new investment until after the NAV struck 
 


---

## Page 31

Best Practice User Guide – Full Edition 
 
Orders 31 
 [[DTCC]] Public (White) 
Best Practices for Exception Processing 
• Scenario 1: TA/Fund is cancelling a completed AIP Order that settled via AIP, and reprocesses a new 
purchase transaction after order [[settlement]] (e.g., an incorrect discount category was applied) 
o I f the c orrection is completed after order [[settlement]] but before the final NAV is struck (Activity record 
with Transaction Type 74 has not been sent) 
» Activity Transaction Type 74 = Delayed NAV Purchase will be used for any AIP initiated Order 
and will have corrected information, if any, along with original Order Control Number populated 
in the Related Control Number field 
o If the correction is completed after order [[settlement]] and after the final NAV is struck (Activity record 
with Transaction Type 74 has been sent) 
» For AIP initiated Orders, if a correction is needed after an Activity record Transaction Type 74 = 
Delayed NAV Purchase has been sent, a second Activity record with Transaction Type 74 = 
Delayed NAV Purchase should be sent 
• Populate Adjustment Indicator of 1 = Adjustment  
• The original Order Control Number should be populated in the Related Control 
Number field 
• Scenario 2: A trade that never made it to the fund via AIP in good order (Fund reject of AIP order is an 
example) and cannot be resubmitted 
o The trade and money [[settlement]] must occur outside of AIP 
o An Activity record should be sent with a Transaction Type 01 = Direct Purchase as typical for orders 
processed outside of AIP but reported in AIP  
• Scenario 3: The AIP Order process completes and money settles but the Transaction did not post to TA 
system due to an error so transaction type 74 was not sent in the expected timeframe; the [[intermediary]]’s 
transaction is in good order, but the Trade must be reprocessed by TA 
o An Activity record with Transaction Type 74 = Delayed NAV Purchase should be sent as soon as 
possible 
 
Placement Fee Order Processing  
• If Load Type Indicator ‘9 = Placement Fee’ is indicated on the transaction, the Net/Gross Indicator, 
Commission Amount, Commission Percentage and Gross Amount of Trade fields will become ‘Required’ 
to populate 
Net/Gross Indicator Usage  
Below is a list of the Net/Gross Indicators and their descriptions which outlines what the Funds should populate 
as the Money Amount on the Confirmation Record when the Net/Gross Indicator field is populated on the 
transaction. 
Net/Gross Indicator 
• 1 = Net – Money Amount being settled is Net of Commissions, Fees etc. 

---

## Page 32

Best Practice User Guide – Full Edition 
 
Orders 32 
 [[DTCC]] Public (White) 
• 2 = Gross – Money Amount being settled is Gross of Commissions, Fees etc. 
• 3 = Net Down – Commission/Placement Fee Amount is added to the Gross Amount of Trade amount and 
Money Amount being settled is Net of Commissions, Fees etc. 
• 4 = Gross Up – Commission/Placement Fee Amount is added to the Gross Amount of Trade amount and 
Money Amount being settled is Gross of Commissions, Fees etc. 
 
 
 
 


---

## Page 33

Best Practice User Guide – Full Edition 
 
Account Transfer 33 
 [[DTCC]] Public (White) 
ACCOUNT TRANSFER  
Transaction Type Descriptions 
Account Transfer – Non-ACATS Transfer of [[shares]] that is staying within the same firm and the account 
requires to be re-registered 
[[Broker]] to Customer Transfer – N on-ACATS Transfer of [[shares]] when the account is [[Broker]] Controlled at the 
Firm and the client is requesting to ‘denetwork’ the account to be Customer Controlled directly at the Fund (Re- 
registering the account to reflect only the customer’s name) 
 
• No Registration is required to be transmitted via AIP 
• The [[Broker]] is required to provide the Receiving Fund Account Number on the Transfer 
• The Fund will ‘Reject’ a [[Broker]] to Customer Transfer 
o If the Fund cannot find the Delivering or Receiving Account 
o Share amount exceeds the balance of the account 
• The Firm will ‘Exit’ a [[Broker]] to Customer Transfer 
o If the Customer requests to cancel the transfer and stays with the [[Broker]] 
o If the Firm is required to balance their books based upon the request from Corporate Actions 
 
Customer to [[Broker]] Transfer – Non-ACATS Transfer of [[shares]] when the account is Customer Controlled at 
the Fund and the client is requesting to be [[Broker]] Controlled at the Firm (Re-registering the account to reflect 
the firm FBO the client) 
• The [[Broker]] is required to provide the Delivering Fund Account Number on the Transfer 
• The [[Broker]] can send either a New or Existing Registration to establish the Receiving Firm Account 
• The Registration must be set-up before or at the same time the Transfer is received at the fund 
o If not, it will be rejected by the Fund 
 
[[Broker]] to [[Broker]] Transfer - Non-ACATS Transfer when the entire book of business is moving within one AIP 
Firm 
Miscellaneous 
• A Security Announcement is not required to transmit an Account Transfer 
• Transfers using the same account type are not required to provide the paperwork from the sponsors 
o If it is not the same account type, the paperwork is required or else the Transfer cannot occur 
• The ‘Money Amount’ field will be used to support capital balance funds 
• The Firms will use the ACATS Related Control Number to support Cost Basis 
• The Transfer Reason Codes are needed for Cost Basis Purposes 
o If the Transfer Reason Code is both Death and a Custodian Change, the firm should send two (2) 
separate Transfer records 

---

## Page 34

Best Practice User Guide – Full Edition 
 
Account Transfer 34 
 [[DTCC]] Public (White) 
 
Transfer Types 
• Transfer Types designate if the Transfer is a Full Position Transfer or Partial Position Transfer 
• If the Transaction Type is populated to 01 – Full Fund Position Transfer, the Share Quantity field should 
be left ‘blank’ or populated with zero (0) 
o If the fund is capital balance, the money amount should be populated with zero (0) 
o The Fund will provide the Share Quantity and/or Money Amount in the Confirmation Process 
 
NOTE:  
If the intent is to close the account, please designate the Transfer Type as a Full Position Transfer 
 
• If the Transaction Type is populated to 02 – Partial Fund Position Transfer, the Share Quantity is 
required to be populated 
o If the fund is capital balance, the Money Amount must be provided 
 
Process Flow Types 
Daily Funds – Process Flow Indicator (0 – REITS/BDC Processing) 
• Daily funds are any funds that are priced (for example, Non-Traded REITs & BDCs) 
• Process Flow Indicator 0 will be used for all daily funds 
• The ‘Effective Date’ should be populated with the Trade Date of the transfer, but can be past or future 
dated 
• The Fund will transmit the acknowledgements within 24 hours 
• The anticipated Transfer Completion Date on the acknowledgement will be populated with the next 
business date 
• The Firm can cancel the transfer by either transferring the account back to the original account or reaching 
out to the Fund to transmit a Fund Reject 
 
Periodic Funds – Process Flow Indicator (1 – [[Hedge Fund]] Processing) 
• Periodic funds are any funds that are not priced (for example, Hedge Funds) 
• Process Flow Indicator 1 will be used for all periodic funds 
• The ‘Effective Date’ should be populated with the Trade Date of the transfer, but can be past or future 
dated 
• The Fund with transmit the acknowledgement within 24 hours 

---

## Page 35

Best Practice User Guide – Full Edition 
 
Account Transfer 35 
 [[DTCC]] Public (White) 
o The anticipated Transfer Completion Date on the acknowledgement will be populated with the next 
business date 
• Once the confirmation is successfully transmitted the [[shares]] will be moved 
 
Account Registration 
• The Registration record will be required if there is no account established at the firm 
• If there is an existing account established with [[shares]] at the firm, the Registration record should not be 
submitted 
 

---

## Page 36

Best Practice User Guide – Full Edition 
 
Document Transfer 36 
 [[DTCC]] Public (White) 
DOCUMENT TRANSFER 
The Document Transfer service provides the ability for any AIP [[Member]] (or their designated [[transfer agent]] or 
service provider) to send or receive electronic documents securely through the AIP system. 
Process Flow 
 
 
Best Practices 
• If there is an AIP transaction related to the document, senders should submit the transaction before the 
document, but both should be submitted on the same day  
• Receivers are expected to Acknowledge or Reject documents within 24 hours 
• If a document is sent to an incorrect receiver, please follow the existing protocols used today for AIP 
records and/or documents sent outside of AIP 
• If a document passes [[DTCC]]’s validation but is rejected by the recipient, the sender and receiver need to 
communicate outside of AIP what the issue is and/or how to address it over existing channels 
• Although the Firm Account Number and Fund Account Number fields are optional, the Firm should 
populate one of these fields, likely the BIN, whenever possible 
 
Note:  
These practices are based on pre-implementation working group feedback and will be updated as needed based on Test 
and Production usage 


---

## Page 37

 
 [[DTCC]] Public (White) 
 
FOR MORE INFORMATION 
 
Visit us on the web at: 
www.[[DTCC]].com/aip 