---
title: "Money Market Fund Reform and Best Practice"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs_money_mkt_reform_userguide_bp_mfs359_20240205.pdf"
pages: 57
size: "710.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Money Market Fund Reform and Best Practice

**Original File:** [mfs_money_mkt_reform_userguide_bp_mfs359_20240205.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs_money_mkt_reform_userguide_bp_mfs359_20240205.pdf)  
**Category:** Other  
**Total Pages:** 57  
**File Size:** 710.2 KB  

---

## Page 1

 
 
 
Mutual Fund Services 
MONEY MARKET FUND REFORM USER GUIDE & 
BEST PRACTICE 
FEBRUARY 5, 2024 
 

---

## Page 2

 
 
CHANGE HISTORY 
Dates Revisions 
February 5, 2024 Document was rebranded.  
July 22, 2022 Learning upgrade caused some link(s) to break.  Links have been corrected. 
September 30, 2020 Document was rebranded.  Links corrected. 
September 22, 2016 Money Market Fund Reform and Best Practice published 
  

---

## Page 3

 
 
TABLE OF CONTENTS 
Change History ..................................................................................................................................................... 2 
1. Background ...................................................................................................................................................... 5 
Introduction ......................................................................................................................................................... 5 
Operational Aspects of Money Market Fund Reform ......................................................................................... 5 
2. Mutual Fund Profile Service II (MFPS II) Security Database Impacts .......................................................... 7 
Summary of MFPS II Changes ........................................................................................................................... 7 
Money Market Fields in MFPS II Security Database .......................................................................................... 7 
Sample Money Market Fund Portfolio Level Set-up Parameters in MFPS-II ...................................................11 
Social Code Considerations .............................................................................................................................12 
Checklist for MFPS II Updates for New and Existing Money Market Funds ....................................................13 
3. Mutual Fund Profile Service (MFPS 1) – Price and Rate ............................................................................ 14 
General Money Market Fund Reform Price Delivery and Processing Considerations  .....................................14 
Summary of Changes to MFPS I Price and Rate Record 30 ...........................................................................14 
Key Money Market Fund Reform Fields in MFPS I ..........................................................................................15 
4. Transaction Eligibility .................................................................................................................................... 24 
5. Fund/Serv® Impacts ....................................................................................................................................... 29 
Fund/SERV® Trading Considerations ..............................................................................................................29 
Important Fund/SERV® Money Market fields....................................................................................................31 
Money Market Fields–Best Practices ...............................................................................................................35 
Summary .........................................................................................................................................................35 
Scenario 1: “Aggregated Order Indicator” field = “1 - Transactions are not aggregated” ...............................36 
Scenario 2: “Aggregated Order Indicator” field = “2 – Transactions are aggregated by “like” orders .............37 
Scenario 3: “Aggregated Order Indicator” field = “3 – Transaction are net of purchases and redemptions” ..39 
Scenario 4: “Aggregated Order Indicator” field = “4–Netting is unknown at time of placement” ....................40 
Scenario 5: “Aggregated Order Indicator” field is Blank ..................................................................................41 
[[Liquidity]] Fee Communication ...........................................................................................................................42 
6. Networking Impact ......................................................................................................................................... 44 
7. ACATS Considerations .................................................................................................................................. 47 
Appendix A – History of [[NSCC]] Money Market Fund Reform Enhancements Important Notices  .............. 49 

---

## Page 4

 
 
Appendix B - [[NSCC]] [[Mutual Funds]] Services Record Layouts–Price/NAV Fields ........................................ 50 
Fund/SERV®–Variable ......................................................................................................................................50 
Networking: .......................................................................................................................................................51 
Account Conversion ........................................................................................................................................51 
Activity Reporting ............................................................................................................................................52 
[[Dividend]] Activity ..............................................................................................................................................52 
Standardized Data Reporting ..........................................................................................................................52 
Share Aging .....................................................................................................................................................53 
[[DTCC]] Payment aXis® .......................................................................................................................................53 
Payment aXis®–Commission and Fee [[settlement]] ..........................................................................................53 
MFPS ................................................................................................................................................................54 
 

---

## Page 5

Money Market Fund Reform User Guide & Best Practice 
Change History 5 
1. BACKGROUND  
Introduction 
Amendments to the rules governing money market funds, adopted by the [[securities]] and Exchange 
Commission ([[SEC]]) in July 2014, imposed significant structural changes on the money market fund industry. 
According to the [[SEC]], the rules were designed to address money market funds’ susceptibility to heavy 
redemptions in times of stress, improve their ability to manage and mitigate potential contagion from such 
redemptions, and increase the transparency of their risks, while preserving, as much as possible, their benefits.  
The changes also allow or, in certain circumstances, require money market funds to impose a [[Liquidity]] fee or 
redemption gate if a fund’s weekly liquid assets fall below a certain threshold or if the fund’s board determines 
such action to be in the best interests of the fund. The new rules also require institutional prime and institutional 
tax-exempt money market funds to sell and redeem [[shares]] using a floating net [[Asset]] value (NAV) and to round 
prices to four decimal places. While not explicitly stated in the new rules, some [[Asset]] managers may calculate 
more than one NAV per day for institutional funds in order to meet customers’ [[Liquidity]] needs.  
In connection with Money Market Fund Reform implementation, [[NSCC]] in collaboration with a working group of 
the Investment Company Institute’s (ICI) [[Broker]]/Dealer and Bank, Trust and Retirement Advisory Committees 
(BDAC and BTRAC, respectively; the “Working Group”) to propose recommendations for enhancing [[NSCC]]’s 
Mutual Fund Services for purposes of helping our clients comply with the new Money Market Fund Reform 
operational requirements. The recommended enhancements allow for communication of (1) multiple price 
(NAV) strikes, (2) data points for funds to administer [[Liquidity]] Fees and Redemption Gates, (3) [[Liquidity]] fees 
withheld by funds and (4) access to Money Market Fund 
Reform-related data points as specified in the funds’ Prospectuses. 
This guide will focus on [[NSCC]] [[Mutual Funds]] services that were enhanced for purposes of helping our clients 
comply with the Money Market Fund Reform operational requirements. Best practices referenced in this 
document were identified by the ICI
1 Working Group and should be used in conjunction with the [[NSCC]] Mutual 
Funds Record Layouts located in the [[DTCC]] Learning Center at  https://dtcclearning.com/products-and-
services/mutual-fund-services/record-layouts.html 
Operational Aspects of Money Market Fund Reform 
The [[Securities and Exchange Commission]] (“Commission” or “[[SEC]]”) has adopted amendments to the rules that 
govern money market [[Mutual Funds]] (or “money market funds”) under the [[Investment Company Act]] of 1940 
(“[[Investment Company Act]]” or “Act”). Effective October 14, 2016 the [[SEC]] required institutional non-
government money market funds to sell and redeem [[shares]] based on the current market-based value of the 
[[securities]] in their underlying portfolios rounded to the fourth decimal place (e.g., $1.0000), i.e., transact at a 
“floating” NAV. The [[SEC]] also adopted amendments to give the boards of directors of money market funds new 
tools to stem heavy redemptions by giving them discretion to impose a [[Liquidity]] Fee if a fund’s weekly [[Liquidity]] 
level falls below the required regulatory threshold, and give them discretion to suspend redemptions 
temporarily, i.e., to “gate” funds, under the same circumstances. These amendments will require all non-
government money market funds to impose a [[Liquidity]] Fee if the fund’s weekly [[Liquidity]] level falls below a 
designated threshold, unless the fund’s board determines that imposing such a fe e is not in the best interests 
of the fund. 
 
1  Additionally, ICI created a “Money Market Fund Reform Implementation Resource Center” that contains various documents as well  as industry and ICI 
resources concerning money market funds and the Money Market Fund Reform. This resource center can be accesse d via the following link: 
https://www.ici.org/ops_mmf_reform 
 

---

## Page 6

Money Market Fund Reform User Guide & Best Practice 
Change History 6 
Compliance date for implementing Floating NAV and Money Market [[Liquidity]] Fees and Gates amendments 
was October 14, 2016. 
The following chart depicts the requirements as set forth by the [[regulation]]. 
 
Money Market Funds 
 Retail Institutional  Government 
Floating NAV Exempt Required Exempt 
[[Liquidity]] Fee Subject To Subject To May opt into 
Redemption Gate Subject To Subject To May opt into 
 
Note:  
[[NSCC]] supports Price field values with 4 decimal places throughout all [[NSCC]] [[Mutual Funds]] products. For a complete list of 
[[NSCC]] [[Mutual Funds]] NAV fields and field attributes, please refer to Appendix B. 
The remaining sections of the guide focus on the [[NSCC]] [[Mutual Funds]] services relevant to the support of Money 
Market Funds, highlighting money market-related fields and recommended best practices which will assist [[NSCC]] 
clients with Money Market Fund Reform implementation. The guide also addresses key operational impacts as 
they relate to the following [[NSCC]] services: 
• Mutual Fund Profile II – Security Database 
• Mutual Fund Profile I - Price and Rate 
• Fund/SERV® – Order processing 
o Subscription and Redemption 
o Omnibus and non-Omnibus 
• Networking - Activity Reporting 
 
 

---

## Page 7

Money Market Fund Reform User Guide & Best Practice 
Change History 7 
2. MUTUAL FUND PROFILE SERVICE II (MFPS II) 
SECURITY DATABASE IMPACTS 
Summary of MFPS II Changes 
Changes to MFPS II provide funds with the ability to accurately describe a money market fund’s type and [[BASIC]] 
operating parameters. The following MFPS II modifications were implemented in connection with Money Market 
Fund Reform operational requirements: 
Key Dates Summary of Changes 
Summary of MFPS II changes 
effective August 22, 2016 
Important Notice a8227 
• New Product Type Code “15 –Section 529 Money Market Fund” added to allow 
Funds to communicate Money Market Reform-related data points for Section 
529 Money Market Funds.  
• To view the above referenced field, please refer to the MFPS II record layouts or 
the Profile Security web application at the Fund Portfolio hierarchy level, General 
Profile tab. 
Summary of MFPS II changes 
effective May 31, 2016 
Important Notice a8139 
• New “Money Market Indicator” field added to provide definition of a money 
market fund type (i.e. retail, institutional or government). 
• New “Money Market [[Liquidity]] Fee/ Redemption Gate Eligibility Fund Indicator” 
field created to indicate whether the money market fund’s Board of Directors will 
consider the imposition of [[Liquidity]] fees and/or redemption gates when the 
average weekly [[Liquidity]] percentage of the Fund’s portfolio falls below a 
disclosed percentage (i.e., 10% or 30%) 
• New “NAV Strike Time” fields allow funds to indicate the number of and times 
when a fund calculates its NAV (i.e. NAV strikes) for an Institutional floating NAV 
(FNAV) money market fund. 
• A new Money Market Fund Data Record Type (033) contains all new fields. 
• To view the above referenced fields, please refer to the MFPS II record layouts 
or the Profile Security web application at the Fund Portfolio hierarchy level, 
General Profile tab. 
Summary of Social code changes 
effective November 30, 2015 
Important Notice a8073 
• [[NSCC]] added new and modified existing social codes to allow for the clear 
identification of Retail vs. Institutional account types. For additional information 
on [[NSCC]] Social Codes, please refer to Social Code Considerations section. 
 
Money Market Fields in MFPS II Security Database 
The following sections further describe key Money Market fields that funds are required to populate on MFPS II 
Security Database for their Money Market funds. 
Funds should review and update their money market Security Issue IDs on MFPS II Profile Security Fund 
Portfolio hierarchy level to ensure the “Product Type Code” for money market funds is “02” = Money Market 
Mutual Fund or “15” = Section 529 Money Market Fund. A value of “02” = Money Market Mutual Fund or “15” = 
Section 529 Money Market Fund controls the other Money Market -related fields that must be populated within 
MFPS II. 
It is strongly recommended that funds use the “future dating” capabilities of MFPS II to ensure sufficient notice 
is given to firms regarding the effective date for the new rules described in this section.  
 

---

## Page 8

Money Market Fund Reform User Guide & Best Practice 
Change History 8 
Web User Interface: 
1.  “Money Market Fund Indicator” field 
A “Money Market Fund Indicator” field exists at the Fund Portfolio hierarchy level, General Profile tab. 
This indicator will specify if the fund is a money market fund and the type of Money Market fund. The 
options available for selection are as follows: 
• Money Market Retail 
o The Money Market Indicator field should reflect the “Money Market Retail” value for  a stable net 
[[Asset]] value money market fund that has implemented policies and procedures reasonably 
designed to limit investment in the fund to individuals/natural persons. 
• Money Market Government 
o The Money Market Indicator field should reflect the “Money Market Government” value for a 
stable net [[Asset]] value money market fund that is investing at least 99.5% of its total assets in 
cash, government [[securities]], and/or repurchase agreements that use only government [[securities]] 
or cash as [[collateral]]. 
• Money Market Institutional 
o The “Money Market Fund Indicator” field should reflect the “Money Market Institutional” value for a 
floating net [[Asset]] value (FNAV) money market fund that is generally being marketed to the 
institutional/high net worth investors and has a higher investment minimum. 
The field is Required when “Product Type Code” field = “02 – Money Market Mutual Fund” or “15 – 
Section 529 Money Market Fund.” 
The “Money Market Fund Indicator” field will be considered a “Not In Document (NID)” data point until a 
determination can be made as to how this information will be included in the Fund’s prospectus and 
whether it can be classified as an extractable data point by the Profile Security Comparison Tool.  
2.  Money Market [[Liquidity]] Fee/Redemption Gate Eligibility Fund Indicator” field  
• “Money Market [[Liquidity]] Fee/Redemption Gate Eligibility Fund Indicator” field exists at the Fund 
Portfolio level and indicates whether the money market fund may be subject to liq uidity 
fees/redemption gates. Under Money Market Fund Reform, Retail and Institutional money market 
funds may be subject to [[Liquidity]] fees/redemption gates. Government money market funds may opt into 
the use of [[Liquidity]] fees/redemption gates; but are not required by the [[regulation]]. 
• The options available for this field should be applied as follows: 
o 0 – No, this money market fund is not subject to [[Liquidity]] Fees / Redemption Gates  
o 1 – Yes, this money market fund may potentially impose a [[Liquidity]] Fee / Redemption Gate  
 
The field is Required when “Product Type Code” field = “02 – Money Market Mutual Fund”. 
Considerations and Best Practices: 
• If the Board of Directors of a Government fund determines that it is appropriate to subject the fund to a 
[[Liquidity]] fee/redemption gate, the “Money Market [[Liquidity]] Fee/ Redemption Gate Eligibility Fund 
Indicator” field should be updated to “Yes” with an effective date that coincides with the effective date 
disclosed in the fund’s prospectus (at least 60-days advance notice is required.) This information should 
be communicated to intermediaries through all channels that the fund commonly uses for dissemination 
of policy updates (e.g., fax, email, etc.) and also disclosed in the fund’s prospectus.  
 
 

---

## Page 9

Money Market Fund Reform User Guide & Best Practice 
Change History 9 
3.  “NAV Strike Time” fields 
• Ten Optional/Conditional “NAV Strike Time” fields were added at the Fund Portfolio level and 
require entry in at least one of these fields when the “Money Market Indicator” field is populated 
with a value of “Money Market Institutional”: 
» “NAV Strike Time 1” 
» “NAV Strike Time 2” 
» “NAV Strike Time 3” 
» “NAV Strike Time 4” 
» “NAV Strike Time 5” 
» “NAV Strike Time 6” 
» “NAV Strike Time 7” 
» “NAV Strike Time 8” 
» “NAV Strike Time 9” 
» “NAV Strike Time 10” 
 
• When “Money Market Indicator” field = “Money Market Institutional”, the first “NAV Strike Time 1” field 
is Required. The “NAV Strike Time” fields allow money market funds to communicate up to 10 NAV 
strike times. These are the actual times when the fund will strike the NAV2. 
• These fields are to be entered in the military time format (e.g., hhmmss) and Eastern Time. 
• If the “Money Market Indicator” field is populated with “1=Retail Money Market” or “3=Government 
Money Market,” then the “NAV Strike Time” fields (1 through 10) will not be availabl e/allowed for 
entry by a user. 
• All 6 bytes are required to be populated for this field 
 
Considerations and Best Practices: 
• If the seconds (ss) are unknown (the 5th and 6th byte) then the fund user should use a [[default]] value of 
zeroes (00) in the last 2 bytes of the “NAV Strike Time” field. 
• Firms have indicated they will use this information to derive their cutoff time(s) for trading.  
• The number of NAV strikes in an Institutional FNAV money market fund may vary by fund and will be 
disclosed in the fund’s prospectus. Examples of some potential variations are listed below: 
o 4 NAV Strikes - Trades may be priced using a 9:00am, 12:00pm, 3:00pm or 5:00pm NAV. The 
5:00pm NAV will be used for transactions as well as valuations and income reinvestment 
calculations, etc. 
o 3 NAV Strikes – Trades may be priced using a 9:00 am, 12:00 pm, or 3:00pm NAV. The 3:00pm 
NAV will be used for transactions as well as valuations and income reinvestment calculations, etc.  
 
2 Additionally, ICI created a “Money Market Fund Reform Implementation Resource Center” that contains various documents as well as industry and ICI resources 
concerning money market funds and the Money Market Fund Reform. This resource center can be accessed via the following link: 
https://www.ici.org/ops_mmf_reform 
 

---

## Page 10

Money Market Fund Reform User Guide & Best Practice 
Change History 10 
o 1 Single NAV – Trades may be priced using a 3:00 pm. The 3:00pm NAV will be used for 
transactions as well as valuations, and income reinvestment calculations, etc.  
• Times should be entered in ascending chronological order. For the 4 NAV Strikes example above:  
» “NAV Strike Time 1” = 090000 
» “NAV Strike Time 2” = 120000 
» “NAV Strike Time 3” = 150000 
» “NAV Strike Time 4” = 170000 
• The “NAV Strike Time” fields will not be available/displayed for any Retail or Government money market 
funds or non-money market fund types. 
 
Mainframe Batch Files 
• Fixed length and Variable Length record layouts include the new record type Money Market Fund Data 
(033) 
• Record type (033) should be submitted when the “Product Type Code” field on the General Profile record 
(020) is “02 = Money Market Mutual Fund” or “15 = Section 529 Money Market Fund”.  
• Record type (033) will contain all new money market-related fields. In addition, it will contain a “Number of 
NAV Strikes” field. 
 
“Number of NAV Strikes” fields: 
• 2 byte Numeric field 
• This field was added to Record Type 033, but it will NOT be available on the Web  User Interface 
• The valid values are 00, 01, 02, 03, .., 09, 10. 
• This field is Required when the “Money Market Indicator” field = “2-Institutional Money Market Fund” 
and should be populated with at least “01” when required. 
• Values of “02” through “10” should be populated when the number of NAV Strike Times  for the fund is 
greater than “01”. 
• This field provides the number of NAV strikes times passed in the file. 
• Value of “00” should be provided when the “Money Market Indicator” field = “1- Retail Money Market 
Fund” or “3-Government Money Market Fund”. 
• The field will be reconciled with the number of “NAV Strike Time” fields passed in the file. For 
example, if “NAV Strike Time 1” and “NAV Strike Time 2” fields are populated then “Number of NAV 
Strikes” field should be populated with “02”. 
• The General Profile and Money Market Fund Data records should be submitted simultaneously for a new 
money market fund set up. 
 
Considerations and Best Practices: 
The General Profile record (020) will determine what other batch file records should be submitted. For 
example, if “CDSC Rules Apply” field = Yes on the General Profile Record, then funds must submit the CDSC 
Record (022). If the General Profile Record indicates “Product Type Code” as “02 =Money Market Mutual 
Fund” or “15 = Section 529 Money Market Fund”, then funds must also submit the new record (033) - Money 
Market Fund Data. 

---

## Page 11

Money Market Fund Reform User Guide & Best Practice 
Change History 11 
Sample Money Market Fund Portfolio Level Set-up Parameters in 
MFPS-II 
Retail Money Market Fund 
Field Name Value/Setting 
Money Market Indicator Money Market Retail 
Money Market [[Liquidity]] Fee/Redemption Gate Eligibility Fund Indicator Yes* 
*The “NAV Strike Time” field is not available for this type of money market fund.  
Government Money Market Fund 
Field Name Value/Setting 
Money Market Indicator Money Market Government 
Money Market [[Liquidity]] Fee/Redemption Gate Eligibility Fund Indicator No* 
*Government funds that may potentially impose [[Liquidity]] fees/redemption gates would enter “Yes  The “NAV Strike Time” field is not available for this type of 
money market fund. 
Institutional Money Market Fund– Institutional (FNAV-Single NAV Strike Per Day – 3pm)   
Field Name Value/Setting 
Money Market Indicator Money Market Institutional 
Money Market [[Liquidity]] Fee/Redemption Gate Eligibility Fund Indicator Yes 
NAV Strike Time 1  150000 
 
Institutional Money Market Fund– Institutional (FNAV- Multiple NAV Strikes Per Day). 4 Multi Day Strikes – 9am, 12pm, 
3pm and 5pm)   
Field Name Value/Setting 
Money Market Indicator Money Market Institutional 
Money Market [[Liquidity]] Fee/Redemption Gate Eligibility Fund Indicator Yes 
NAV Strike Time 1 090000 
NAV Strike Time 2 120000 
NAV Strike Time 3 150000 
NAV Strike Time 4 170000 
 
 
 

---

## Page 12

Money Market Fund Reform User Guide & Best Practice 
Change History 12 
Social Code Considerations 
Retail vs. Institutional Account Categorization for Trusts 
To comply with Money Market Fund Reform regulations, [[Mutual Funds]] must specify which money market funds 
are limited for investment to individuals/natural persons (i.e., Retail money market funds). By doing so funds 
may continue to offer the fund with a constant $1.00 NAV but must also have policies and procedures in place 
to identify and monitor the fund’s [[investor]] characteristics.  To assist firms in identifying these investment 
restrictions, it is recommended funds populate MFPS II with all eligible [[NSCC]] social codes for a given fund 
portfolio. 
During an analysis (conducted in 2015) by the ICI Money Market Fund Reform Retail vs. Institutional Working 
Group of the available social codes for categorization of either a Retail and/or Institutional account type, it was 
determined that social codes related to “Trust” accounts required further clarification. As a result , the following 
changes to the [[NSCC]] social codes were requested and approved (effective November 30, 2015):  
• Rename social code #15 from “Personal Trusts” to “Trust-Retail” 
• Rename social code #42 from “Institutional Trust Account” to “Bank/Trust FBO” 
• Add a new social code #95 defined as “Trust-Institutional” 
 
Social Code Social Code Definition Social Code Categorization 
15 Trust-Retail Retail 
42 Bank/Trust FBO Retail 
95 Trust-Institutional Institutional 
 
Social Codes are available in all WMS [[Mutual Funds]] products and layouts that contain a “Social Code” field, 
including Mutual Fund Profile Security. See Important Notice a8073, dated August 27, 2015 for more 
information. 
MFPS II User Interface: 
Fund clients complete the Money Market Social Codes at the Share Class Hierarchy level.  Social Codes can 
be overridden (modified) at the security issue [[ID]] level.  
MFPS II Mainframe Batch Files: 
Fund clients should submit the [[NSCC]] Social Code Eligibility record (Record type 025) for any Money Market 
funds on Profile. 
A complete list of [[NSCC]] Social Codes can be found in the [[DTCC]] Learning Center under Codes  
https://dtcclearning.com/documents/mutual-fund-services-1/mfs-cross-product/codes-8/2498-social-
codes/file.htm   
The ICI Retail vs. Institutional Customers Working Group has defined common practices for categori zing retail 
accounts using the [[NSCC]] Social Codes. The “Money Market Fund Social Code Categorization Matrix” pdf 
can be found the ICI’s Money Market Fund Reform Implementation Resources website under the Retail Versus 
Institutional Customers Working Group link. 
 
 

---

## Page 13

Money Market Fund Reform User Guide & Best Practice 
Change History 13 
Checklist for MFPS II Updates for New and Existing Money Market 
Funds 
Funds are strongly encouraged to follow the below guidelines when establishing new or updating existing 
Money Market funds on MFPS II Profile Security database. 
• Ensure that “Product Type Code” field is populated with “2 - Money Market Fund Mutual Fund” or “15 – 
Section Money Market Fund”. 
• Update the “Money Market Indicator” field to define the type of money market fund (i.e. Government, 
Retail or Institutional). 
• Update the “Money Market [[Liquidity]] Fee/ Redemption Gate Eligibility Fund Indicator” field to define 
whether the money market fund’s Board of Directors may consider the imposition of [[Liquidity]] fees and/or 
gates when the average weekly [[Liquidity]] percentage of the Fund’s portfolio falls below a percentage 
disclosed in the prospectus. 
• Update the “NAV Strike Time” fields to define all NAV price strike times for an Institutional Floating NAV 
(FNAV) money market fund. 
• Update the “Eligible Social Code” fields to define which social codes are acceptable account 
categorizations for the Fund. 
 

---

## Page 14

Money Market Fund Reform User Guide & Best Practice 
Change History 14 
3. MUTUAL FUND PROFILE SERVICE (MFPS 1) – PRICE 
AND RATE 
General Money Market Fund Reform Price Delivery and Processing 
Considerations 
• Starting October 14, 20163, the [[SEC]] is requiring Institutional money market funds to calculate floating 
NAVs using “basis point” pricing precision (to 0.01%). For a money market fund that wishes to target a 
$1.00 NAV, it will calculate and provide 4-decimal place NAVs (i.e., basis point pricing such as $1.0000 or 
$0.9998). 
• Institutional money market funds may elect to calculate and provide multiple intra- day NAVs4; others may 
elect to only calculate and provide one NAV per day. 
• The last NAV calculated in a given day will typically be used for valuating positions and calculating income 
reinvestments; however, the fund’s prospectus will describe actual practices for a fund providing multiple 
intra-day NAVs. 
• The general assumption in this Best Practice document is that for funds supporting next -day or T+1 
[[settlement]], the last/end of day NAV strike will be used for this purpose, including any applicable [[NSCC]] 
DCC&S trades received the next business morning. Intermediaries should consult fund prospectuses and 
business agreements with fund partners to ensure compliance with trading practices. 
• Firms offering money market products that calculate multiple intra-day NAVs may need to develop the 
ability to store more than one valid price per Security Issue [[ID]] per day. In some inst ances, firm transaction 
activities may allow them to only require the last/end of day NAV. 
 
Summary of Changes to MFPS I Price and Rate Record 30 
The following MFPS I modifications (Important Notice a8159) were implemented in connection with Money 
Market Fund Reform operational requirements: 
• Update the description of the field titled “Effective Date” to clarify that the data provided should represent 
the “Price Strike Date”. 
• Allow money market funds to disseminate multiple intra-day NAV’s, if appropriate. 
• Allow money market funds to distinguish NAV corrections, as needed, for funds with multiple intra- day 
NAV strikes. 
• [[NSCC]] updated both ISO and Non-ISO formats. All information (field names, etc.) in The Key Money 
Market Fund Reform Fields I MFPS I Section below is specific to Non-ISO record layouts. 
  
 
3 Some Funds might start calculating and distributing floating NAVs before October 14, 2016.  
 
4 Funds are typically providing multiple intra-day NAV strikes to also allow for same-day [[settlement]] (T+0) for direct-at-fund transactions. 

---

## Page 15

Money Market Fund Reform User Guide & Best Practice 
Change History 15 
Key Money Market Fund Reform Fields in MFPS I 
Field Name Comment 
1.  Effective Date Price Strike Date 
2.  Price Correction Indicator New Values were added effective September 26, 2016 to 
support Money Market Fund Reform: 
• “3=Multiple NAVs Fund – Original Price” 
• “4=Multiple NAVs Fund – Correction to Price” 
3.  Price (NAV)   Supports values with 4 decimal places 
4.  Price (NAV) Indicator 
• These fields were added on September 26, 2016 to 
support Money Market Fund Reform. 
• Required for use with Funds Calculating Multiple Intra-
Day NAV Strikes 
5.  Price (NAV) Start Time 
6.  Price (NAV) Start Date 
7.  Price (NAV) Strike Time 
Note: 
Historically, money market funds sought to maintain a stable $1.00 NAV per share. [[Mutual Funds]] avoided, and 
intermediaries did not expect, the passing of stable $1.00 per share NAV for money market funds through automated 
means like MFPS I. With institutional money market funds adopting a floating NAV model, and in an effort to standardize 
processing activities across products, it is recommended that funds send all money market funds’ NAVs (stable and 
floating) through MFPS I. 
[[NSCC]] MFPS I Price and Rate file layout supports values with 4 decimal places. For a list of [[NSCC]] NAV fields 
for all [[Mutual Funds]] products, please refer to Appendix B. 
The following sections are intended to provide MFPS I clients with guidelines and best practices for 
communicating price information (specifically Multiple NAVs Funds’ prices).  
1. “Effective Date” field-Funds need to populate the Required “Effective Date” field with the effective date 
(i.e., price strike date) of the price in the ccyymmdd format. For example, if the fund’s price is effective as 
of 12pm on 9/10/15, the “Effective Date” of this price will be “20150910”. 
 
2. “Price Correction Indicator” field-Funds need to populate the “Price Correction Indicator” field with one 
of the following values to specify whether the Fund calculates a single or multiple NAV’s per day:  
• 1 = Single NAV Fund-Original Price 
• 2 = Single NAV Fund-Correction to Price 
• 3 = Multiple NAVs Fund–Original Price 
• 4 = Multiple NAVs Fund–Correction to Price 
 
Single NAV Fund 
Single NAV funds should continue to use the following values to communicate single daily NAVs:  
o 1 = Single NAV Fund-Original Price 
o 2 = Single NAV Fund-Correction to Price 

---

## Page 16

Money Market Fund Reform User Guide & Best Practice 
Change History 16 
Values 1 and 2 were renamed effective September 26, 2016 (Important Notice a8159) to clarify that these 
values must be used for single NAV funds, which includes all retail and government money market funds as 
well as institutional money market funds that only calculate one NAV per day.  
Values 3 and 4 were specifically designed to allow Multiple NAVs funds to communicate multiple NAVs through 
MFPS I Price and Rate file and should not be used to communicate prices for single NAV funds.  
Multiple NAVs Fund 
Funds that calculate multiple NAV’s per day should submit original and/or corrected NAV information for a 
specific intra-day NAV in a timely manner. Institutional FNAV money market funds that will deliver multiple 
intra-day NAV’s must populate the “Price Correction Indicator” field with one of the following values:  
o 3 = Multiple NAVs Fund–Original Price 
o 4 = Multiple NAVs Fund–Correction to Price 
 
Considerations and Best Practices: 
• The Optional/Conditional “Price (NAV)” field is used to designate when a price (NAV), as opposed to an 
accrual factor/rate, is being communicated. This field is required if the “Price Correction Indicator” field is 
populated with a valid value (i.e.1, 2, 3 or 4). 
• Government, Retail and Institutional money market funds that calculate a single NAV strike per day, 
should use “Price Correction Indicator” values of either “1 = Single NAV Fund-Original Price” or “2 = 
Single NAV Fund-Correction to Price”. For funds that intend to strike multiple intra-day NAVs, the following 
fields must be provided. All four of these fields are required if the “Price Correction Indicator” field is 
populated with a value of 3 or 4 (see above section). All four of these fields are not allowed if “Price 
Correction Indicator” field is 1, 2 or space (blank): 
o Price (NAV) Indicator 
o Price (NAV) Start Time 
o Price (NAV) Start Date 
o Price (NAV) Strike Time 
• Firms wishing to ingest multiple intra-day NAVs will need to read the “Price (NAV) Indicator”, “Price (NAV) 
Start Time”, “Price (NAV) Start Date” and “Price (NAV) Strike Time” fields. 
• Firms that only wish to ingest the last/end of day NAV strike for a fund that calculates multiple intra- day 
NAV’s will need to read the above referenced fields and extract the NAV when the “Price (NAV) Indicator” 
field = “98” (the last NAV price strike of the day). 
• Funds must ensure NAVs for the same Security Issue [[ID]] and Effective Date are not transmitted to [[NSCC]] 
as both Single (“Price Correction Indicator” = 1) and Multiple (“Price Correction Indicator” = 3) original 
prices. In this scenario [[NSCC]] will reject the 2nd submission of the “original” price.  
 
In order to communicate multiple NAVs for FNAVs funds must provide the following fields on the Price 
and Rate file; 
1. “Price (NAV) Indicator” field 
This Optional/Conditional 2-byte “Price (NAV) Indicator” field is Required when the “Price Correction 
Indicator” field = 3 (”Multiple NAVs Fund–Original Price”) or 4 (”Multiple NAVs Fund –Correction to Price”). 
The value in this field will indicate whether a particular price is the 1st, 2nd, 3rd, etc. NAV strike of the day. 
Funds should enter the chronological value appropriate for the reflected NAV strike (i.e., 01, 02, 03, through 9 
or 98). 
Considerations and Best Practices: 
• The [[DTCC]] will reject any records where the value in the “Price (NAV) Indicator” field is zero.  

---

## Page 17

Money Market Fund Reform User Guide & Best Practice 
Change History 17 
• This field must be blank for single NAV funds 
• For funds with multiple intra-day NAV’s, the values should be 01, 02, 03 through 09. The last/end of day 
NAV strike should always be coded with a value of 98. 
o For regular business days, price occurrence should correspond to MFPS II NAV Strike Times listed 
for the fund in MFPS II Security Issue database and fund’s prospectus. 
o For holidays or business days with market disruptions, the recommended practice is for funds to pass 
“Price (NAV) Indicator” = 98 whenever the last NAV is struck. Funds and firms can also continue to 
rely on their existing processes to handle these situations. 
 
2. “Price (NAV) Start Time” field 
The Optional/Conditional “Price (NAV) Start Time” field is Required when the “Price Correction Indicator” 
field = 3 (”Multiple NAVs Fund–Original Price”) or 4 (”Multiple NAVs Fund–Correction to Price”). 
The start time of the price is 1 (one) second after the “Price (NAV) Strike Time” of the previous price. For 
example, the fund may strike a price three times a day: 9am, 12pm and 3pm. The “Price (NAV) Start Time” of 
the 12pm price would be “090001” (9:00:01am). Similarly, the “Price (NAV) Start Time” of the 9am price would 
be “150001” (3:00:01pm) since the previous price was calculated at 3pm on the previous day.  
This field will be in Military Format (hhmmss) and Eastern Time. 
3. “Price (NAV) Strike Time” field 
The Optional/Conditional “Price (NAV) Strike Time” field is Required when the “Price Correction Indicator” 
field = 3 (”Multiple NAVs Fund–Original Price”) or 4 (”Multiple NAVs Fund–Correction to Price”). 
This field must contain the strike time of the price. For example, if the fund strikes a price at 3pm, the “Price 
(NAV) Strike Time” will be “150000” (3:00:00pm). 
This field will be formatted in Military (hhmmss) and Eastern Time. 
4. “Price (NAV) Start Date” field 
The Optional/Conditional “Price (NAV) Start Date” field is Required when the “Price Correction Indicator” field 
= 3 (”Multiple NAVs Fund–Original Price”) or 4 (”Multiple NAVs Fund–Correction to Price”). 
This field will be formatted “ccyymmdd” and represents the date of the price start time. For example, if the fund 
strikes a price at 9am on 9/10/15 and the next one at 12pm on 9/10/15, the “Price (NAV) Start Date” of the 
12pm price will be “20150910” (9/10/2015). If the fund strikes a price at 3pm on 9/9/15 and the next one at 9am 
on 9/10/15, the “Price (NAV) Start Date” of the 9am price will be “20150909” (9/9/2015).  
The following graphic illustrates the above referenced example for a Multiple NAVs Fund:  

---

## Page 18

Money Market Fund Reform User Guide & Best Practice 
Change History 18 
 
Considerations for Multiple NAVs funds: 
• Funds should provide all NAV strikes/prices via MFPS I, including constant NAV (i.e., $1.00) prices. 
• MFPS I batch files are not cumulative throughout the day (See Single Batch exception below)  
o Single Batch Users–Receive one cumulative file daily. This file is distributed at the same time as 
Cycle 98 for multi-batch users. 
• Batch File Submitters: If multiple “Original Price” records for the same Security Issue [[ID]] and Effective 
Date (and Price (NAV) Indicator, Start Date, Start Time and Strike Time for mu ltiple intra-day NAV funds) 
are delivered to [[DTCC]] within the same [[DTCC]] cycle (or multiple cycles), the first submitted “Original Price” 
record will be distributed; all other “Original Price” records with the same attributes will be rejected by 
[[DTCC]]. 
• MQ Submitters: If multiple “Original Price” records for the same Security Issue [[ID]] and Effective Date (and 
Price (NAV) Indicator, Start Date, Start Time and Strike Time for multiple intra-day NAV funds) are 
delivered to [[DTCC]], the first submitted “Original Price” record will be distributed; all other “Original Price” 
records with the same attributes will be rejected by [[DTCC]]. 
• Timely transmission and receipt of mutual fund prices (NAVs) is extremely important for single NAV funds. 
Funds calculating multiple NAVs per day introduce additional level of complexity and the need for 
intermediaries to receive each calculated NAV for FNAV funds in a timely manner is of utmost importance. 
In addition to traditional batch file transmissions, [[NSCC]] supports MQ messages. For the fastest delivery 
and distribution of prices (NAVs), it is recommended that both submitting funds and receiving firms adopt 
and use the MQ protocol. 
 
For additional information on the MFPS I supported formats, transmission schedule and edit rules, please refer 
to the “Mutual Fund Profile 1 Price and Rate” located in the [[DTCC]] Learning Center – see MFPS I section 
https://dtcclearning.com/products-and-services/mutual-fund-services/mfpsi.html 
 
 
 
 
 


---

## Page 19

Money Market Fund Reform User Guide & Best Practice 
Change History 19 
The following charts provide additional examples of the FNAV fund field variations dependent upon the 
number of daily NAV strikes: 
4 4 NAV Strikes-9am, 12pm, 3pm 
and 5pm 
Price provided 
on 9/9/15 Price provided on 9/10/15 
 5pm 9am 12pm 3pm 5 pm 
Effective Date 9/9/2015 9/10/2015 9/10/2015 9/10/2015 9/10/2015 
Price Correction Indicator 3 3 3 3 3 
Price (NAV) 1.0000 0.9999 1.0000 1.0000 1.0001 
Price (NAV) Indicator 98 01 02 03 98 
Price (NAV) Start Date 9/9/2015 9/9/2015 9/10/2015 9/10/2015 9/10/2015 
Price (NAV) Start Time 15:00:01 17:00:01 09:00:01 12:00:01 15:00:01 
Price (NAV) Strike Time 17:00:00 09:00:00 12:00:00 15:00:00 17:00:00 
 
 
 
 
 
2 NAV Strikes (FNAV) – 
12pm and 3pm 
Price provided on 
9/9/15 Price provided on 9/10/15 
 3pm 12pm 3pm 
Effective Date 9/9/2015 9/10/2015 9/10/2015 
Price Correction Indicator 3 3 3 
Price (NAV) 1.0000 1.0000 1.0000 
Price (NAV) Indicator 98 01 98 
Price (NAV) Start Date 9/9/2015 9/9/2015 9/10/2015 
Price (NAV) Start Time 12:00:01 15:00:01 12:00:01 
Price (NAV) Strike Time 15:00:00 12:00:00 15:00:00 
 
 
 
 
  

---

## Page 20

Money Market Fund Reform User Guide & Best Practice 
Change History 20 
 
 
1 Single NAV Strike 
(FNAV)*- 4pm Price provided on 9/9/15 Price provided on 9/10/15 
 4pm 4pm 
Effective Date 9/9/2015 9/10/2015 
Price Correction Indicator 1 1 
Price (NAV) 1.0000 1.0001 
Price (NAV) Indicator Blank Blank 
Price (NAV) Effective Start Date Blank Blank 
Price (NAV) Effective Start Time Blank Blank 
Price (NAV) Effective Cut-off Time Blank Blank 
*Institutional FNAV money market funds that only calculate a single NAV strike per day should follow the same rules 
as applied to all single strike [[Mutual Funds]]. 
Price Corrections for Multiple NAVs Funds 
In order to communicate price corrections for multiple FNAV funds, the following fields will be necessary to 
properly identify the price being corrected: 
• “Effective Date” = Strike date of the price that is being corrected 
• “Price Correction Indicator” = 4 (“Multiple NAVs Fund–Correction to Price”) 
• Corrected “Price (NAV)” 
• “Price (NAV) Indicator”– Sequential number of the price that is being corrected (i.e., 01 through 09 or “98” 
for last/end of day price strike) 
• “Price (NAV) Start Time”–of the price that is being corrected 
• “Price (NAV) Start Date”–of the price that is being corrected 
• “Price (NAV) Strike Time”–of the price that is being corrected 
 
Considerations: 
Batch file submissions 
• [[DTCC]] extracts the most current correction for the Security Issue [[ID]] submitted within the same cycle 
for delivery to firms. 
• Funds attempting to correct NAV’s for Security Issue [[ID]]’s that calculate multiple intra- day NAVs, must 
ensure that all fields for the corrected records match the data submitted on the “Original Price” 
record, except the “Price Correction Indicator” and the “Price (NAV)”; otherwise, [[DTCC]] will reject the 
“Correction” record. 
• Funds submitting a “Correction” to a “Correction” record will need to follow the same rule above.  
• If multiple “Correction to Price” records for the same Security Issue [[ID]], Effective Date (and Price 
(NAV) Indicator, Price (NAV) Start Date, Price (NAV) Start Time and Price (NAV) Strike Time for 
multiple intra-day NAV funds) are delivered to [[DTCC]] within the same [[DTCC]] cycle, [[DTCC]] will 
distribute the latest correction received during this cycle. 

---

## Page 21

Money Market Fund Reform User Guide & Best Practice 
Change History 21 
• “Correction to Price” records provided in subsequent [[DTCC]] cycles will also be extracted and 
delivered by [[DTCC]], provided the above rules are followed. 
 
MQ submissions 
• If multiple “Correction to Price” records for the same Security Issue [[ID]] (and Price (NAV) Indicator, 
Start Date, Start Time, Effective Date and Strike Time for multiple intra-day NAV funds) are delivered 
to [[DTCC]], each of these corrections will be accepted by [[DTCC]]. 
• Firms subscribing to receive Price and Rate data via MQ will receive all corrections for the same 
combination of fields as described above. 
• Firms subscribing to receive Price and Rate data via batch files, will receive the last correction 
submitted within a given cycle. 
 
  

---

## Page 22

Money Market Fund Reform User Guide & Best Practice 
Change History 22 
 
The following charts provide price correction examples for the key MFPS I field variations: 
Correction to Last NAV of Prior 
Day (5:00 pm) Price provided on 9/9/15 Price provided on 9/10/15 
 5pm 5pm 
Effective Date 9/9/2015 9/10/2015 
Price Correction Indicator 3 4 
Price (NAV) 1.0001 0.9998 
Price (NAV) Indicator 98 98 
Price (NAV) Start Date 9/9/2015 9/9/2015 
Price (NAV) Start Time 15:00:01 15:00:01 
Price (NAV) Strike Time 17:00:00 17:00:00 
 
Correction to 2nd NAV Strike 
(3:00pm) Price provided on 9/9/15 Price provided on 9/10/15 
 3pm 3pm 
Effective Date 9/9/2015 9/9/2015 
Price Correction Indicator 3 4 
Price (NAV) 1.0001 1.0000 
Price (NAV) Indicator 2 2 
Price (NAV) Start Date 9/9/2015 9/9/2015 
Price (NAV) Start Time 12:00:01 12:00:01 
Price (NAV) Strike Time 15:00:00 15:00:00 
 
1 Single Strike (FNAV) (3pm) Price provided on 9/9/15 Price provided on 9/10/15 
 3pm 3pm 
Effective Date 9/9/2015 9/10/2015 
Price Correction Indicator 1 2 
Price (NAV) 1.0001 1.0000 
Price (NAV) Indicator Blank Blank 
Price (NAV) Start Date Blank Blank 

---

## Page 23

Money Market Fund Reform User Guide & Best Practice 
Change History 23 
1 Single Strike (FNAV) (3pm) Price provided on 9/9/15 Price provided on 9/10/15 
Price (NAV) Start Time Blank Blank 
Price (NAV) Strike Time Blank Blank 

---

## Page 24

Money Market Fund Reform User Guide & Best Practice 
Change History 24 
4. TRANSACTION ELIGIBILITY 
Background on Transaction Eligibility for [[Liquidity]] Fees and Redemption Gates  
In its simplest form, transactions that require a sale of money market fund [[shares]] may be subject to an 
applicable [[Liquidity]] fee (fee) and/or redemption gate (gate). This would include redemption and exchange- out 
transactions. For purposes of this Guide, unless otherwise stated, the term “redemption” is used generally to 
refer to the sale of fund [[shares]]. This would include any exchange-out activity from a mutual fund, whereby 
proceeds from the sale of a money market fund are immediately used to buy [[shares]] of a different fund.  
However, there are a number of regulatory and operational factors that may impact when and how such fee or 
gate may be applied to transaction activity, including applicability to additional transaction types. These factors 
and their potential impacts are described below: 
The omnibus processing model 
[[Mutual Funds]] are increasingly distributed through [[intermediary]] arrangements using an omnibus processing 
model. Under this model, an omnibus account includes the [[shares]] of multiple investors that are customers of 
the [[intermediary]] (also known as beneficial owners). Omnibus accounts are held on the books of a fund in the 
name of the [[intermediary]], acting on behalf of its customers. When an [[intermediary]] submits omnibus account 
transactions, it usually consolidates (aggregates) the transactions of all beneficial owners that are purchasing 
or redeeming [[shares]] of the same fund that day into one or a few “summary” (omnibus) transactions for 
processing by the fund. 
Omnibus trade aggregation generally occurs in one of two ways: 
• Aggregation within Transaction Type: This scenario combines all “like” transactions from the 
[[intermediary]]’s customers (also known as beneficial owners), prior to sending to the fund for processing 
into the firm’s omnibus account. For instance, all [[Beneficial Owner]] purchase transactions are combined 
and sent in one (or a few) large transaction(s) to the fund. 
• Aggregation across Transaction Type: This scenario combines both credit (purchase) and debit 
(redemption) transactions from beneficial owners prior to sending to the fund for processing into the firm’s 
omnibus account. For example, a purchase transaction of $1 million received by the fund and created 
under this method of aggregation could actually represent $10 million in purchases, netted with $9 million 
of redemptions. 
 
The Working Group considered the omnibus processing model when recommending changes to [[NSCC]] 
processing to ensure clear understanding of who is assessing applicable fees and applying gates, as needed.  
Effective date/time of fee and/or gate versus the transaction 
The adopting release for Money Market Fund reform requires funds to know and firms to communicate both the 
date and time when a transaction is considered “in good order” for processing by the fund. Such information 
can prove vitally important, in the event of the application of a fee or gate, to evaluate if or how a transaction 
may be processed by the fund (i.e., will it be subject to a fee or gate). The ICI Money Market Working Group 
considered the need for expanded date/time information on money market transactions and recommended 
addition of these fields for [[NSCC]] processing. 
Flexibility afforded fund boards when applying [[Liquidity]] fees and redemption gates  
With the adopting release for Money Market Fund reform, the [[SEC]] incorporated two key elements designed to 
provide fund boards with maximum flexibility when administering a [[Liquidity]] fee or redemption gate:  
• Permitting intraday application or removal of fees or gates (and fee changes), and 
• Allowing fund flexibility to define “good order” trade receipt for fee or gate purposes as either when 
received by the [[intermediary]] or when received by the fund. 
 

---

## Page 25

Money Market Fund Reform User Guide & Best Practice 
Change History 25 
In response to these factors, funds may take a more conservative stance regarding trade acceptance when the 
fund’s [[Liquidity]] is under stress. For instance, some funds may elect to more broadly gate all redemption5 activity 
(i.e. apply a “hard” gate) when an intraday redemption gate applies, to allow for a review of all transactions to 
determine accurate intraday fee/gate treatment
6. Funds may also determine that any redemption trade not 
already received by the fund when the board announces a redemption gate should be rejected and managed in 
a post-gate scenario. A fund typically outlines these transaction eligibility practices through its prospectus.  
Eligible Transactions for [[Liquidity]] Fee/Redemption Gate Purposes 
The following table outlines the Working Group’s recommended practices for eligible categories of transactions 
based on the July 2014 adopting release of Money Market Fund reform and expectations for the application of 
[[Liquidity]] fees and redemption gates. As stated above, the adopting release provides funds with flexibility when 
invoking and/or removing a [[Liquidity]] fee or redemption gate. The fund’s prospectus and statement of additional 
information should be consulted for specific guidelines and policies it follows:  
Transaction Type Fee/Gate Eligibility Comments/Recommended 
Practices 
Fund/SERV® and Networking 
Record Types 
Cash [[Dividend]]/Capital 
Gain Distributions 
No (for additional 
information please refer to 
“Redemptions through 
DCC&S” section) 
• These transaction types are 
the distribution of income or 
excess capital from the fund; 
cash payout does not directly 
impact the core [[Liquidity]] of the 
portfolio. 
 
• Networking [[Dividend]] 
Reporting–records 
61-69 
Exchange Yes (sell side)  
No (buy side) 
• Redemption/Sell side of 
transaction is eligible for 
fee/gate 
• Purchase/Buy side of 
transaction is ineligible for 
fee/gate 
 
• Exchange 015 
• Exchange Confirmation 016 
• Exchange Reconfirmation 
017 
• Post [[settlement]] Exchange 
Cancellation 021 
Purchase No • Not applicable at the beneficial 
owner level 
 
Additional Considerations 
• Omnibus account purchase 
may be partially eligible when 
trade aggregation occurs 
across transaction types and 
includes netted purchases and 
redemptions. 
 
• Order 001 
• Confirmation 
005/Reconfirmation 006 
• As-Of Order 004 
• Correction 003 
• Correction Confirmation 
025 
• Post [[settlement]] Correction 
by Fund 026 
• Post [[settlement]] 
Cancellation 140 
 
5 Some funds may choose to apply redemption gates (if imposed) to both redemptions and purchases. In addition, some funds might also choose to gate 
transactions that clearly indicate firms as the party that will administer a gate. 
6 Aggregation of buy and sell activity into a net order to the fund for omnibus accounts and institution of an intraday redemption gate may inhibit funds’ ability to 
accurately assess which transactions may be 
subject to fee and/or gate processing—including transactions “in-flight” as well as those already in the fund’s possession. For these reasons, funds may choose 
a more conservative approach, especially under a redemption gate, to limit transaction activity.  

---

## Page 26

Money Market Fund Reform User Guide & Best Practice 
Change History 26 
Transaction Type Fee/Gate Eligibility Comments/Recommended 
Practices 
Fund/SERV® and Networking 
Record Types 
Redemptions 
(excluding DCC&S 
activity) 
__________________ 
Redemptions through 
DCC&S 
Yes 
 
 
______________________ 
Varies 
Applicable at the [[Beneficial Owner]] 
level 
 
___________________________ 
• DCC&S activity is received 
during the early morning of 
T+1, and fund policies 
regarding fee/gate should be 
applied with this understanding 
of transaction effective date 
• Certain DCC&S transactions, 
as defined by “[[Asset]] Type”, 
are used to complete activity 
that does not impact [[Liquidity]] 
and, as such, should be 
exempt from fee/gate 
considerations 
Additional Considerations 
• Omnibus account redemptions 
may be partially eligible when 
trade aggregation occurs 
across transaction type and 
includes netted purchases and 
redemptions 
 
• Order 001 
• Confirmation 
005/Reconfirmation 006 
• As-Of Order 004 
• Correction 003 
• Correction Confirmation 
025 
• Post [[settlement]] Correction 
by Fund 026 
• Post [[settlement]] 
Cancellation 140 
Transfers (Manual, 
Networking, ACATS-
Fund/SERV®) 
Generally No (see 
Additional Considerations) 
• Transaction is a reregistration 
of fund [[shares]], which does not 
have a [[Liquidity]] impact 
Additional Considerations 
• Under an ACATS-
Fund/SERV
® transfer, if the 
receiving [[Broker]] is not eligible 
to hold the money market 
fund, the delivering [[Broker]] 
must first [[Liquidate]] the money 
market fund position and 
deliver cash. The [[liquidation]] 
would follow redemption 
guidelines (see above). 
• ACATS-Fund/SERV® 
Transfer 018 
• Networking Transfer B52 
 
  

---

## Page 27

Money Market Fund Reform User Guide & Best Practice 
Change History 27 
Redemptions through DCC&S 
Defined Contribution Clearance and [[settlement]] (DCC&S) leverages Fund/SERV ® records (As-Of record 004) 
to permit [[intermediary]] and fund participants to benefit from the efficiencies of regular Fund/SERV ® processing, 
except through placing and settling eligible transactions on a T+1 basis. Such activity is governed by 
agreements between counterparties that trading activity presented by intermediaries through DCC&S fully 
complies with fund’s prospectus regarding trading cut-off times and assignment of effective trade date. 
DCC&S makes use of an “[[Asset]] Type Indicator” field that defines the type of activity represented by the 
DCC&S order. The Working Group identified certain transactions, as defined by  ”[[Asset]] Type” that are offsetting 
or in some way not intended to affect the [[Liquidity]] of the fund. As such, it is the Working Group’s 
recommendation that funds and firms apply [[Liquidity]] fee and redemption gate eligibility to DCC&S redemptions 
as described below: 
[[Asset]] Type 
Indicator Description7 Fee/Gate 
Eligibility Comments/Recommended Practices 
B Defined Contribution Plan Yes  
F 529 Underlying Fund Trades Yes  
G Share Class Conversion No [[shares]] are moving between classes of the same 
portfolio; no net change to portfolio [[Liquidity]]. 
H Health Savings Accounts Yes  
I Insurance Fund Transactions Yes  
J Non-Qualified Retirement Plan Yes  
K Qualified Retirement Plan Yes  
L Omnibus [[Dividend]] 
Reconciliation* No 
The transaction is used by [[Broker]]/dealers to sell 
reinvested [[Dividend]] [[shares]] to cover beneficial owners 
that wish to receive income in cash. See below Note 
for additional details. 
M Variable Annuity Yes  
N Wrap Program Yes  
O Defined Benefit Plan Yes  
S Omnibus Short-term Capital Gain 
Reconciliation* No 
The transaction is used by [[Broker]]/dealers to sell 
reinvested capital gain [[shares]] to cover beneficial 
owners that wish to receive gains in cash. See below 
Note for additional details. 
T Omnibus Long-term Capital Gain 
Reconciliation* No 
The transaction is used by [[Broker]]/dealers to sell 
reinvested capital gain [[shares]] to cover beneficial 
owners that wish to receive gains in cash. See below 
Note for additional details. 
 
7 Refer to the list of [[Asset]] Type Indicator Codes in the [[DTCC]] Learning Center under “Codes” under the Fund//SERV dropdown https://dtcclearning.com/products-
and-services/mutual-fund-services/codes.html 
         

---

## Page 28

Money Market Fund Reform User Guide & Best Practice 
Change History 28 
 
*Note: 
 To simplify omnibus recordkeeping and reconciliation between funds and firms, many [[Broker]]/dealers use a single omnibus 
account at the fund to hold all [[Beneficial Owner]] [[shares]]. The fund’s omnibus account typically supports either [[Dividend]] and 
gain reinvestment or cash payment of earnings. Since the majority of beneficial owners typically reinvest [[Dividend]]/gains, 
firms typically submit a cash [[Dividend]]/gain redemption through DCC&S for the cash proceeds. In limited instances, the 
[[default]] [[Dividend]]/gain treatment is in cash, and the DCC&S purchase is made to buy back the appropriate amount of 
reinvested [[shares]] representing the [[Dividend]]/gains. 
Transaction Corrections 
With the advent of temporary fees and/or gates on a money market fund, it is incumbent upon both funds and 
firms to maintain a permanent record of the details surrounding such events. Any transaction corrections which 
backdate into the fee or gate period will also be subject to the same restrictions, as if the corrected transaction 
had originally occurred on the date in question8. 
  
 
8 For example, if a fund was under a 2% [[Liquidity]] fee on November 19, 2016, any eligible redemption activity corrected back to this date would need to be 
assessed the [[Liquidity]] fee. 

---

## Page 29

Money Market Fund Reform User Guide & Best Practice 
Change History 29 
5. FUND/SERV® IMPACTS  
Fund/SERV® Trading Considerations 
The [[SEC]] clearly indicated in its adopting release that notification of a [[Liquidity]] fee or redemption gate must be 
consistent, fair and not advantage one party over another. Industry recommended practices indicate that when 
possible funds should communicate fee or gate decisions (imposition, change (fees only) or removal) in 
advance of the effective time/date. However, funds generally will communicate the implementation of a fee or 
gate after the effective date/time has passed, especially in the context of an intraday fee/gate, to avoid any  
first-mover advantage. In other instances, funds may communicate the application of a fee or gate to coincide 
with the end of a business day.9 Regardless, money market fund trades, under the adopting release, must 
provide sufficient details so firms and funds may accurately apply a fee or gate at any point during order 
placement. 
Communicating fee/gate responsibility for Fund/SERV
® activity 
Intermediaries employ multiple trading models through Fund/SERV®, with the most notable variance in the use 
of aggregation for trading activity. Each approach has implications to Fund/SERV® trading and options for 
applying fees and/or gates. 
Transaction transparency: With sufficient transparency, funds can apply fees/gates to transaction  activity; 
otherwise, the [[intermediary]] is responsible. The modifications to Fund/SERV® (see Important Notice a8159) 
allow for intermediaries to indicate whether the fund should administer the fee/gate on the transaction and the 
nature of aggregation. If an [[intermediary]] is assuming responsibility for administering a fee or gate, 
Fund/SERV® also captures the nature of aggregation used when constructing the Fund/SERV® trade (e.g., no 
aggregation, aggregation by or across transaction type). 
Date and timestamp cons iderations: With the possibility of intraday fees and/or gates, it becomes especially 
important for the fund to know the date AND time a transaction is considered in good order. This may or may 
not coincide with the transaction’s effective date.
10 For this reason, Fund/SERV® has been updated for 
intermediaries to pass both date and time of receipt for money market fund transactions. Such information is 
separate and discrete from all existing transaction effective date fields and is only intended for use to 
determine money market [[Liquidity]] fee and/or redemption gate applicability.  
Fee calculation, estimation, and remittance: When the fund assesses the fee, the fund will automatically deduct 
the fee from the transaction gross amount, withholding is communicated on the Fund/SERV® order 
confirmation, and the fee payment is netted from [[NSCC]] trade [[settlement]] (typically will occur on the next 
business day). 
When the [[intermediary]] assesses the fee, the [[intermediary]] must promptly provide an estimated fee amount to 
funds and remit timely fee payment (outside of [[NSCC]]
11) to help funds in rebuilding portfolio [[Liquidity]]. The 
industry recommended practice is that intermediaries will provide a fee estimate to the money market fund prior 
to its next scheduled NAV calculation and that the monies will be remitted to the fund no later than two 
business days following the trade date.
12 
 
9 Refer to ICI’s “Event Processing Assumptions and Considerations” pdf (page 2) found under the https://www.ici.org/pdf/15_ops_event_processing.pdf link on 
the https://www.ici.org/ops_mmf_reform/[[Liquidity]] reference. 
10 For example: A web-initiated redemption in good order is received by an [[intermediary]] at 11:00 p.m. Tuesday for a money market fund that institutes a fee at 
10:00 a.m. Wednesday. Although the transaction’s effective date is Wednesday, the fact it was received in good order on Tuesday may allow the trade to be 
processed at the fund without the fee. This depends on when the transaction is ultimately delivered to the fund and the fund’s policies on trade receipt.  
11 The Working Group considered requesting modifications to Payment aXis® to permit [[Liquidity]] fee remittance but ultimately determined that expected  volumes 
would not be sufficient to support the initiative. 
12 Refer to ICI’s “Event Processing Assumptions and Considerations” pdf (page 6) found under the [[Liquidity]] Fees Redemptions Gates  link on the ICI Money 
Market Fund Reform Implementation reference.  

---

## Page 30

Money Market Fund Reform User Guide & Best Practice 
Change History 30 
Additional gate considerations 
Although Fund/SERV® orders have been enabled to communicate instances where an [[intermediary]] is 
assuming responsibility to apply a gate, some funds – under the discretion permitted them through the 
adopting release–may elect to gate all transaction activity (i.e. apply a “hard” gate) when redemptions are 
gated. In this instance, the [[intermediary]]’s transactions would be rejected by the fund and would need to be 
resubmitted by the [[intermediary]] after the gate has been lifted. 13 
Funds may choose to gate all activity for a variety of reasons. Most notably, funds will want to make sure any 
“in-flight”
14 transactions received near the initiation of a fee/gate have been accurately handled, especially 
those where intermediaries accept responsibility to administer fees/gates. Regardless, funds that employ a full 
gate should clearly communicate this information to their [[intermediary]] partners, so appropriate plans 
developed and, if ever necessary, implemented. 
Additional Considerations 
The fields added to Fund/SERV®, and described in this User Guide below, should only be evaluated when a 
fee/gate applies to the related money market fund. Intermediaries are strongly urged to provide money market 
related fields on all orders, even when a fee/gate is not anticipated. 
Fee and gate administration applies to all as-of and correction orders, as well. As previously noted, it will be 
necessary to maintain a permanent record of all fee and gate events, including effective dates/times and, in the 
case of fees, the percentage(s) withheld. Any as-of and/or correction order that falls into the time frame of an 
applicable fee/gate should have the fee/gate applied to it. 
Note: 
Intraday processing (i.e. same day T+0 [[settlement]]) of Institutional Money funds will continue to be transacted outside of 
[[NSCC]]. 
 
  
 
13 Fund treatment of transaction activity would be described in the prospectus and/or statement of additional information.  
14 In-Flight means a gate is implemented after trades are created by the firm and before receipt by the fund.  

---

## Page 31

Money Market Fund Reform User Guide & Best Practice 
Change History 31 
Important Fund/SERV® Money Market fields 
1. “Money Market [[Liquidity]] Fee/Redemption Gate Indicator” field 
This Optional field allows intermediaries to identify the party responsible for assessing and applying the 
[[Liquidity]] Fee/Redemption Gate. 
• Firms that [[DO]] not aggregate money market trades may prefer the fund to assess and apply the [[Liquidity]] fee 
and/or redemption gate. 
• Firms that aggregate transactions by “like” orders (purchases separate from redemptions) in omnibus 
arrangements may also prefer the fund to assess the [[Liquidity]] fee and/or redemption gate.  
• Firms that aggregate omnibus transactions into a net order (purchases netted against redemptions) will 
need to assess the [[Liquidity]] fee and/or redemption gate, as the fund will not have the necessary trade 
detail to appropriately assess a [[Liquidity]] fee or apply a redemption gate. 
• Valid values: 
o F–Fund 
o B–[[intermediary]] 
o Blank 
 
F – Fund is responsible for assessing and applying the fee/gate 
• Fund will require additional information to make fee/gate assessment (i.e., timestamp data and 
“Aggregated Order indicator”- see Section Money Market Fields–Best Practices) 
• Avoids the need for intermediaries to provide fee estimates or remit fee payments  
• Funds can only assess fee/gate for transactions that are NOT placed as netted buy/sell transactions. 
 
B – [[intermediary]] is responsible for assessing and applying the fee/gate  
• Fewer data elements are provided to the Fund (i.e., no timestamp data-see Section Money Market Fields–
Best Practices) 
• Requires timely fee estimates and fee remittance outside of [[NSCC]]. 
• Intermediaries that net their buy/sell transactions MUST be responsible for assessing a fee/gate.  
 
Blank 
• Will be treated by the fund as an “F” value – the fund will assess and apply the fee/gate if imposed by the 
fund’s board of directors. 
 
Considerations and Best Practices 
• Funds should ignore the “Money Market [[Liquidity]] Fee/Redemption Gate Indicator” field except when 
assessing a fee/gate. 
• All activity in a money market fund that may potentially impose a [[Liquidity]] fee/redemption gate should be 
submitted with an ‘F’ or a ‘B’ indicator. If an affected transaction is submitted with no value (blank) in this 
field, the best practice is for the fund to charge an applicable [[Liquidity]] fee or apply a gate (if in effect) and 
work directly with the [[intermediary]] to resolve any variances outside of [[NSCC]].  
• For redemptions where the fund is assessing the fee (i.e. “Money Market [[Liquidity]] Fee/Re demption Gate 
Indicator” field = “F” or Blank), the best practice is for Intermediaries to consider whether the transmitted 
redemption amount will meet the shareholder needs. The Funds will reduce the redemption proceeds by 

---

## Page 32

Money Market Fund Reform User Guide & Best Practice 
Change History 32 
the fee amount before [[settlement]]. For example, a $100 redemption request made during a 2% fee event 
will yield $98 in [[settlement]] proceeds (i.e., net the fee amount). 
• The industry stated best practice for intermediaries using a ‘B’ indicator is to provide fee amount estimates 
prior to the next NAV strike time. Any previously established guidelines with funds as to how and when 
estimated [[Liquidity]] fees will be communicated and actual [[Liquidity]] fees remitted to the fund should take 
precedence over the industry stated best practice. 
• Funds should return the field value received from the [[intermediary]] on their confirmation records. The 
[[DTCC]] will reject the confirmation record if the field value is not the same as the value supplied by the 
[[intermediary]]. 
 
[[DTCC]] Security Master Considerations: 
• [[DTCC]] eligible [[securities]] are defined in the [[DTCC]] Security Master – a stand-alone system for transacting 
with [[DTCC]]. [[Mutual Funds]] must complete a Mutual Fund Security Profile Form for each security they wish 
to make eligible for trading on the Fund/SERV® system. This setup allows funds to tailor how they trade 
[[securities]] on Fund/SERV®. 
• Not all money market funds are coded with a “Security Type 1940 Act Registered Fund” indicator of a 24 
(“Money Market Fund”) in the [[DTCC]] Security Master (i.e., “fund set-up”). Most money market funds are 
coded with “Security Type” = 26 (“No Load Fund”). The coding of a “Security Type” as a “24 = “Money 
Market Fund” causes a different behavior during [[settlement]] through [[DTCC]] than those commonly coded 
as 26 (“No-Load Fund)” or other fund type. In most instances there will be no need to alter “Security Type” 
in the [[DTCC]] Security Master to support money market fund reform. 
• Members of the ICI Money Market Working Group discussed a possible addition of a Money Market 
identifier to the [[DTCC]] Security Master File and/or a new Security Type to clearly identify Money Market 
funds and a business decision was agreed on, due to the scale of the effort to add another identifier, NOT 
to proceed with either of these enhancements. Therefore, [[DTCC]] will not perform edits on the values in the 
“Money Market [[Liquidity]] Fee/Redemption Gate Indicator” field against the values used in the [[DTCC]] 
Security Master. 
 
 
2. Date and Time Fields 
“Transaction Received Time” field (aka “timestamp”) 
Effective September 26, 2016 (Important Notice a8159) [[NSCC]] repurposed the existing “[[participant]] Processing 
Time” field. The field was renamed “Transaction Received Time” and additional edit rules were implemented as 
requested by the Working Group. 
• The value in this field (hhmmss) represents [[intermediary]]’s time stamp for when the trade was deemed to 
be in good order. 
• The field is optional/conditional and is required if “Money Market [[Liquidity]] Fee/Redemption Gate Indicator” 
field is populated with “F” 
• This field is only applicable on Money Market [[NSCC]] transactions related to administering a fee or gate.  
 
“Transaction Received Date” field 
“Transaction Received Date” is the calendar date (mmddccyy) corresponding to when the trade was deemed to 
be in good order by the [[intermediary]] from the shareholder. 
• The field is optional/conditional and is required if “Money Market [[Liquidity]] Fee/Redemption Gate Indicator” 
field is populated with “F” 
• This field is only applicable on Money Market [[NSCC]] transactions related to administering a fee or gate.  

---

## Page 33

Money Market Fund Reform User Guide & Best Practice 
Change History 33 
 
Considerations and Best Practices 
• Funds should use the value in “Transaction Received Date” field in conjunction with the “Transaction 
Received Time” field to determine if the trade was received in good order by the f irm prior to the fund’s 
fee/gate effective date/time. 
• “Transaction Received Time” and “Transaction Received Date” fields will NOT be used for assessing the 
appropriate NAV strike time. These fields will be used for [[Liquidity]] fee/redemption gate assessment and 
application. 
• When the “Money Market [[Liquidity]] Fee/Redemption Gate Indicator” field is populated with 
“B=[[intermediary]]”’ the best practice is that Intermediaries will assess and remit the fee in accordance 
with the industry best practice or previously-established guidelines to remit the fee to the [[Asset]] manager 
along with details that make up the fee remittance amount. 
o The best practice for trades that are submitted with a “Money Market [[Liquidity]] Fee/Redemption Gate 
Indicator” field = “B=[[intermediary]]” is to leave the “Transaction Received Date” and “Transaction 
Received Time” fields blank. If the date and/or time is supplied, the best practice is for the fund to 
disregard. However, funds are required to confirm transactions with the same date and time valu es 
as supplied by the [[intermediary]] (including blank values). 
• When the “Money Market [[Liquidity]] Fee/Redemption Gate indicator” field is left ‘blank’, firms should 
supply a date and time in the “Transaction Received Date” and “Transaction Received Time” fields 
respectively. 
o Funds should reject records received with a date (“Transaction Received Date”), but no timestamp 
(“Transaction Received Time”) and vice versa. 
o Blank value in both the “Transaction Received Date” and “Transaction Received Time” fields will 
cause funds to use an alternate date/time to determine fee/gate eligibility and to apply the fee/gate to 
the transaction: 
» Date/time received by the fund OR 
» Date/time processed by the fund’s system 
• Funds should return the field value received from the [[intermediary]] in the “Transaction Received Date” and 
“Transaction Received Time” fields on their confirmation records. The [[DTCC]] will reject the confirmation 
record if the field values are not the same as the values supplied by the [[intermediary]].  
 
3. “Aggregated Order Indicator” field 
“Aggregated Order Indicator” field allows firms to specify the nature of aggregation used when creating the 
order. Depending on field value, funds may use the data to assess or estimate a [[Liquidity]] fee to be received on 
the applicable transaction, determine applicability of a redemption gate, or to trigger follow up conversation with 
the [[intermediary]] for estimated [[Liquidity]] fee amounts. 
Valid values: 
• 1 = Transactions are not aggregated 
• 2 = Transactions are aggregated by “like” orders (purchases separate from redemptions)  
• 3 = Transactions are net of purchases and redemptions 
• 4 = Unknown at time of placement 
• Blank 
 
• 1=Transactions are not aggregated: Non-aggregated transactions represent the activity of one 
shareholder. As such, the [[intermediary]] may allow the fund to administer the fee/gate to the transaction.  

---

## Page 34

Money Market Fund Reform User Guide & Best Practice 
Change History 34 
• 2 = Transactions are aggregated by “like” orders (purchases separate from redemptions): 
Transactions aggregated by transaction type may represent the activity of multiple be neficial owners, but 
because all transactions are of the same type (e.g., purchase or redemption), the [[intermediary]] may allow 
the fund to administer the fee/gate to the redemption transaction, such as a sell or exchange- out order. 
• 3 = Transactions are net of purchases and redemptions: Aggregated transactions across transaction 
types also represents the activity of multiple beneficial owners, however, the activity is netted (e.g., 
purchases and redemptions) therefore the fund does not have sufficient transparency to administer the 
fee/gate to the transaction. The [[intermediary]] must take responsibility for administering the fee/gate on the 
transaction. 
• 4 = Unknown at time of placement: This value may be used by certain conduit platforms or clearing 
firms providing services to underling intermediaries. Due to timing of transactions vs. fee/gate imposition, 
it may be unclear as to what type of, if any, aggregation was used to construct the order. Functionally, 
funds should treat these orders like “3=Transactions are net of purchases and redemptions”, as follow up 
with the [[intermediary]] will be necessary to determine true fee/gate eligibility. 
• This optional/conditional field is required for trades that are submitted with a “Money Market [[Liquidity]] 
Fee/Redemption Gate indicator” field = ‘B’ or an ‘F’. 
 
Considerations and Best Practices 
• Funds should return the field value received from the [[intermediary]] in the “Aggregated Order Indicator” 
field on their confirmation/response records. The [[DTCC]] will reject the confirmation record if the field value 
is not the same as the value supplied by the [[intermediary]]. 
 
 
 

---

## Page 35

Money Market Fund Reform User Guide & Best Practice 
Change History 35 
Money Market Fields–Best Practices 
Summary 
The following table summarizes the results for each combination of money market -related Fund/SERV® fields 
previously described. For additional details on each combination, please refer to the section referenced in the 
“Results and Considerations” column: 
"Money Market 
[[Liquidity]] 
Fee/Redemption 
Gate Indicator" 
"Transaction Received 
Time" and "Transaction 
Received Date" 
"Aggregated Order 
Indicator" Results and Considerations 
F=Fund Required 1=Transactions are not 
aggregated 
Fund will apply a fee/gate on applicable 
transactions (See Scenario 1) 
F=Fund Required 
2=Transactions are 
aggregated by “like” 
orders 
Fund will apply a fee/gate. Trades could have 
pre and post fee/gate timestamps on the 
underlying sub-account transactions, therefore 
may require adjustment outside of the [[NSCC]] 
(See Scenario 2) 
F=Fund Required 
3=Transactions are net of 
purchases and 
redemptions 
Illogical. Funds should reject (See Scenario 3) 
F=Fund Required 4=Unknown at time of 
placement Illogical. Funds should reject (See Scenario 4) 
B=[[intermediary]] 
Optional  
(best practice–blank) 
1=Transactions are not 
aggregated 
Firm will apply a fee/gate on applicable 
transactions (See Scenario 1) 
B=[[intermediary]] 
Optional  
(best practice–blank) 
2=Transactions are 
aggregated by “like” 
orders 
Firm will apply a fee/gate on applicable 
transactions (See Scenario 2) 
B=[[intermediary]] 
Optional  
(best practice–blank) 
3=Transactions are net of 
purchases and 
redemptions 
Firm will apply a fee/gate on applicable 
transactions (See Scenario 3) 
B=[[intermediary]] 
Optional  
(best practice–blank) 
4=Unknown at time of 
placement 
Firm will apply a fee/gate on applicable 
transactions (See Scenario 4) 
Blank Optional (best practice–
firms should provide) Blank Fund will apply a fee/gate on applicable 
transactions (See Scenario 5) 
Blank 
Optional  
(best practice–firms 
should provide) 
1=Transactions are not 
aggregated 
Fund will apply a fee/gate on applicable 
transactions (See Scenario 1) 
Blank 
Optional  
(best practice–firms 
should provide) 
2=Transactions are 
aggregated by “like” 
orders 
Fund will apply a fee/gate. Trades could have 
pre and post fee/gate timestamps on the 
underlying sub-account transactions, therefore 
may require adjustment outside of the [[NSCC]] 
(See Scenario 2) 

---

## Page 36

Money Market Fund Reform User Guide & Best Practice 
Change History 36 
"Money Market 
[[Liquidity]] 
Fee/Redemption 
Gate Indicator" 
"Transaction Received 
Time" and "Transaction 
Received Date" 
"Aggregated Order 
Indicator" Results and Considerations 
Blank 
Optional  
(best practice–blank) 
3=Transactions are net of 
purchases and 
redemptions 
Illogical. Funds should reject (See Scenario 3) 
Blank 
Optional  
(best practice–blank) 
4=Unknown at time of 
placement Illogical. Funds should reject (See Scenario 4)  
 
 
Money Market-Related Fields Considerations 
Funds should return the field value received from the [[intermediary]] (including blanks) in the following four fields 
on their confirmation records: 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator” 
• “Transaction Received Time” 
• “Transaction Received Date” 
• “Aggregated Order Indicator” 
 
The [[DTCC]] will reject the confirmation record if the field values are not the same as the values supplied by the 
[[intermediary]]. 
 
The above referenced fields and best practices [[DO]] not apply to trades entered “direct -at-fund” and cannot be 
transmitted as Fund originated orders (Fund/SERV® records 007 and 009). 
The above referenced Money Market-related fields exist on a number of Fund/SERV® record layouts (including 
Order and Exchange records). For a complete list of impacted records, please refer to Important Notice a 8159. 
Scenario 1: “Aggregated Order Indicator” field = “1 - Transactions are not 
aggregated” 
• As a standalone transaction, it is possible for funds to accurately calculate an applicable fee or apply a 
gate. 
 
Fees 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “F-Fund” and transaction is a 
Redemption 
o Assuming the transaction’s date/time fields indicate it is fee-eligible, fund will calculate and charge 
applicable fee and communicate the following information on trade confirmation:  
» Fee Type 
» Fee Rate 
» Amount of fee withheld 

---

## Page 37

Money Market Fund Reform User Guide & Best Practice 
Change History 37 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator” =” F-Fund” and transaction is a 
Purchase 
o Fund will not charge a fee and needs to confirm this transaction 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]]” and transaction is a 
Redemption or Purchase 
o The recommended practice states that firms should expect funds to assess the [[Liquidity]] fee when 
“Aggregated Order Indicator” field = “1” (see above). However, if firms pass a transaction with this 
configuration, funds are advised to confirm these transactions and allow firms to perform fee 
assessment and application. 
 
Gates 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “=” F-Fund” and transaction is a 
Redemption 
o Fund will apply the gate based on the information provided by the [[intermediary]] in the “Transaction 
Received Date” and “Transaction Received Time” fields and the date/time of the gate imposition by 
the board. 
o If not able to process a transaction due to a redemption gate, funds will reject (gate) transactions with 
Fund/SERV® Reject Code =”177-Transaction not allowed against this fund” 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “=” F-Fund” and the transaction is a 
Purchase 
o Fund will process and confirm this transaction 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “=” B-[[intermediary]]” and transaction is a 
Redemption or Purchase 
o The recommended practice states that firms should expect funds to assess the redemption gate 
when “Aggregated Order Indicator” field = “1” (see above). However, if firms pass a transaction with 
this configuration, funds are advised to confirm these transactions and allow firms to perform gate 
assessment and application. 
Scenario 2: “Aggregated Order Indicator” field = “2 – Transactions are 
aggregated by “like” orders 
Fees 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]]” and transaction is a 
Redemption 
o Fund should process transaction without fees 
o Fund uses transaction amount to estimate receivable from [[intermediary]]. Fund and [[intermediary]] will 
need to confirm the fee amount, as it is possible the aggregated trade could include a combination of 
underlying trades that are (or are not) fee eligible based on their date and time stamps.  
» [[intermediary]] needs to assess, calculate and remit fees to fund by Trade Date + 2, or based on 
agreement between fund and [[intermediary]] 
» Fee Remittance occurs outside of [[NSCC]] 
» Fund needs to confirm the trade 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]]” and transaction is a 
Purchase 
» Fund will not charge a fee and needs to confirm the trade 

---

## Page 38

Money Market Fund Reform User Guide & Best Practice 
Change History 38 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “=” F-Fund” and transaction is a 
Redemption 
o While aggregated, since all [[shares]] in the transaction represent a sell, it is possible to accurately 
calculate a fee. However, it is also possible that the aggregated trade could have timestamps on the 
underlying sub-account transactions that reflect a time period prior to the imposition, with a change, 
or after the removal of a fee. In this instance, firms will need to work with the Funds to adjust the 
transaction outside of the [[NSCC]]. 
o Fund applies a fee based on the value provided by the [[intermediary]] in the “Transaction Received 
Date” and “Transaction Received Time” fields. 
o Fund will charge applicable fees based on the amount of the trade and provide the following 
information on trade confirmation: 
» Fee Type 
» Fee Rate 
» Amount of fee withheld 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “F-Fund” and transaction is a 
Purchase 
» Fund will not charge a fee and needs to confirm this transaction 
 
Gates 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]]” and transaction is a 
Redemption 
o Fund should assume that [[intermediary]] is only sending eligible redemptions and should process and 
confirm this transaction
15 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]]” and transaction is a 
Purchase 
o Fund should process and confirm the transaction 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “F-Fund” and transaction is a 
Redemption 
o While aggregated, since all [[shares]] in the transaction represent a buy or a sell, it is possible to 
accurately apply a gate. However, it is also possible that the aggregated trade could have 
timestamps on the underlying sub-account transactions that reflect a time period prior to the 
imposition of a fee/gate. In this instance, firms will need to work with the Funds to adjust the 
transaction outside of the [[NSCC]] 
o Fund applies gate based on the value provided by the [[intermediary]] in the “Transaction Received 
Date” and “Transaction Received Time” fields 
o Funds will reject (gate) transactions with code Fund/SERV
® Reject Code = 177-Transaction not 
allowed against this fund 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “F-Fund” and transaction is a 
Purchase 
o Fund should process and confirm the transaction 
 
15 In instances where a gate has just been implemented, this assumption may not be correct; funds and intermediaries may have alternate procedures to follow 
in that instance. 

---

## Page 39

Money Market Fund Reform User Guide & Best Practice 
Change History 39 
Scenario 3: “Aggregated Order Indicator” field = “3 – Transaction are net of 
purchases and redemptions” 
• Since transactions are fully aggregated it is not clear how much of the transaction represents redemption 
dollars which may be subject to a fee or gate. In this instance, the fund is reliant upon intermediaries to 
accurately enforce a fee/gate. Purchases can also be “subject” to a fee, due to the netting effect. For 
example: $1M net purchase may reflect $10M in purchases and $9M in redemptions. The redemptions 
may be subject to fee or gate. 
• The best practice is this value should only be used for orders submitted with a ‘B’ in the “Money Market 
[[Liquidity]] Fee/Redemption Gate Indicator” field. 
 
Fees 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]]“ and transaction is a 
Redemption 
o Fund should process transaction without fees 
o [[intermediary]] must provide fund with “timely” fee estimate prior to next NAV strike, or based on 
previously established agreement between fund and [[intermediary]] 
o [[intermediary]] must remit fees to fund by Trade Date + 2, or based on agreement between fund and 
[[intermediary]] 
» Fee Remittance occurs outside of [[NSCC]] 
o Funds should confirm this transaction 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]]” and transaction is a 
Purchase 
o Fund should process transaction without fees 
o [[intermediary]] must provide fund with “timely” fee estimate prior to next NAV strike, or based on 
agreement between fund and [[intermediary]] 
o [[intermediary]] must remit fees to fund by Trade Date + 2, or based on agreement between fund and 
[[intermediary]] 
» Fee Remittance occurs outside of [[NSCC]] 
» Fund should confirm this transaction 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “F-Fund” and transaction is a 
Redemption or Purchase 
o This condition is illogical – since transaction is aggregated across type, fund cannot take 
responsibility for fee as it does not have the transparency into the makeup of this transaction which 
can potentially include both redemptions and purchases 
o Intermediaries are strongly encouraged to restrict the sending of transactions with “Money Market 
[[Liquidity]] Fee/Redemption Gate Indicator” = “F” and “Aggregated Order Indicator” = ‘3’. Funds are 
encouraged to reject the receipt of such transactions with a reject code of ‘177–transaction not 
allowed against this fund’. 
 
Gates 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]] “and transaction is a 
Redemption 
o Fund should assume that [[intermediary]] is only sending eligible redemptions and should process and 
confirm transaction 

---

## Page 40

Money Market Fund Reform User Guide & Best Practice 
Change History 40 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]]” and transaction is a 
Purchase 
o Fund should process and confirm transaction 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “F-Fund” and transaction is a 
Redemption or Purchase 
o This condition is illogical – since transaction is aggregated across type, fund cannot take 
responsibility for a gate as it does not have the transparency into the makeup of this transaction 
which can potentially include both redemptions and purchases 
o Intermediaries are strongly encouraged to restrict the sending of a transaction with “Money  Market 
[[Liquidity]] Fee/Redemption Gate Indicator “= “F” and “Aggregated Order Indicator” = ‘3’. Funds are 
encouraged to reject the receipt of such transactions with a reject code of ‘177–transaction not 
allowed against this fund’. 
Scenario 4: “Aggregated Order Indicator” field = “4–Netting is unknown at 
time of placement” 
This value was created for transmission of conduit/clearing firms providing services to underling intermediaries. 
Due to timing of transactions vs. fee/gate imposition, it may be unclear as to what type of, if any, aggregation 
was used to construct the order. This value should only be used for orders submitted with “Money Market 
[[Liquidity]] Fee/Redemption Gate Indicator” field = “B”. 
Fees 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]]“ and transaction is a 
Redemption or Purchase 
o Fund should process transaction without fees 
o [[intermediary]] must provide fund with “timely” fee estimate prior to next NAV strike, or based on 
previously established agreement between fund and [[intermediary]] 
o [[intermediary]] must remit fees to fund by Trade Date + 2, or based on agreement between fund and 
[[intermediary]] 
» Fee Remittance occurs outside of [[NSCC]] 
o Funds should confirm this transaction 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “F-Fund” and transaction is a 
Redemption or Purchase 
o This condition is illogical – since transaction is aggregated across type, fund cannot take 
responsibility for fee as it does not have the transparency into the makeup of this transaction which 
can potentially include both redemptions and purchases 
o Intermediaries are strongly encouraged to restrict the sending of transactions with “Money Market 
[[Liquidity]] Fee/Redemption Gate Indicator “= “F” and “Aggregated Order Indicator” = ‘3’. Funds are 
encouraged to reject the receipt of such transactions with a reject code of ‘177–transaction not 
allowed against this fund’. 
 
  

---

## Page 41

Money Market Fund Reform User Guide & Best Practice 
Change History 41 
Gates 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “B-[[intermediary]] “and transaction is a 
Redemption or Purchase 
o Fund should assume that [[intermediary]] is only sending eligible redemptions and should process and 
confirm this transaction 
• “Money Market [[Liquidity]] Fee/Redemption Gate Indicator “= “F-Fund” and transaction is a 
Redemption or Purchase 
o This condition is illogical – since transaction is aggregated across type, fund cannot take 
responsibility for a gate as it does not have the transparency into the makeup of this transaction 
which can potentially include both redemptions and purchases 
o Intermediaries are strongly encouraged to restrict the sending of a transaction with “Money Market 
[[Liquidity]] Fee/Redemption Gate Indicator “= “F” and “Aggregated Order Indicator” = ‘3’. Funds are 
encouraged to reject the receipt of such transactions with a reject code of ‘177–transaction not 
allowed against this fund’. 
Scenario 5: “Aggregated Order Indicator” field is Blank 
This scenario is possible if “Money Market [[Liquidity]] Fee/ Redemption Gate Indicator” field is also ‘Blank (and 
therefore should be treated by funds like an ‘F’). 
Fees 
• Funds should treat redemptions as non-aggregated transactions for fee purposes 
• “Transaction Received Date” and “Transaction Received Time” fields are optional, but it is recommended 
that firms populate these fields when “Aggregated Order Indicator” is blank. 
o Funds should reject records received with a date (“Transaction Received Date”), but no timestamp 
(“Transaction Received Time”) and vice versa. 
• The best practice for redemptions submitted without an “Aggregated Order Indicator” field (i.e., blank) is 
for the fund to apply the fee/gate based on the “Transaction Received Date” and “Transaction Received 
Time” values provided by the Firm or the Fund’s receipt/ processing time if none was provided by the 
Firm. 
o Funds should communicate fee information on their confirmation record 
• Purchases without an “Aggregated Order Indicator” value may pose a risk to funds, since it is unclear 
whether fee estimation/remittance is required due to the unknown aggregation method.  
o Funds may attempt to clarify transaction aggregation status and the nature of aggregation with the 
[[intermediary]], prior to processing. 
o Funds may choose to reject purchases with code Fund/SERV
® Reject Code =”177-Transaction not 
allowed against this fund” 
 
Gates 
• Transaction Received Date” and “Transaction Received Time” fields are optional, but it is recommended 
that firms populate these fields when “Aggregated Order Indicator” is blank. 
o Funds should reject records received with a date (“Transaction Received Date”), but no timestamp 
(“Transaction Received Time”) and vice versa. 
• Funds are advised to use “Transaction Received Date” and “Transaction Received Time” values (if 
provided by the [[intermediary]]) or alternate date/time (i.e. fund receipt/process time) for evaluative 
purposes 

---

## Page 42

Money Market Fund Reform User Guide & Best Practice 
Change History 42 
• The best practice for redemptions submitted without an “Aggregate Order Indicator” field (i.e., blank) is for 
the fund to apply the gate based on the “Transaction Received Date” and 
• “Transaction Received Time” values provided by the Firm or the Fund’s receipt/processing time if none 
was provided by the Firm. 
• Funds will reject (gate) transactions that are subject to gate with Fund/SERV® Reject Code =”177-
Transaction not allowed against this fund” 
• Funds will confirm transactions that are not subject to gate 
 
[[Liquidity]] Fee Communication 
In the event a [[Liquidity]] Fee was imposed by a fund, the Fund is required to communicate the retained fee 
amount and rate to intermediaries on the Fund/SERV
® confirmation record for all fund-assessed transactions 
(where “Money Market [[Liquidity]] Fee/Redemption Gate Indicator” field = “F-Fund” or Blank). 
Fields previously used for Short-Term Redemption Fees were renamed effective September 26, 2016 
(important notice a8159) for use on confirmations to communicate [[Liquidity]] fees retained by the fund.  
Note: 
Members of the Working Group confirmed that Money Market funds cannot also have short-term redemption fees (not 
applicable under [[SEC]] Rule 22c-2, which does not apply to money market funds). 
Funds will use the following fields to provide the [[Liquidity]] fee rate and amount on confirmations to communicate 
[[Liquidity]] fees retained by the fund: 
• “Redemption Fee Indicator” field 
Funds must specify one of the following two options in the “Redemption Fee Indicator” field when 
confirming fund-assessed transactions. These two options were added in accordance with Important 
Notice a8159. 
o 2 = Money Market [[Liquidity]] Fee 
o 3 = Money Market [[Liquidity]] Fee with CDSC 
• “Redemption Fee Rate” field 
o Effective September 26, 2016, [[NSCC]] renamed “STR Fee Rate” to “Redemption Fee Rate” (Important 
Notice a8159). 
o This optional/conditional field is required when “Redemption Fee Indicator” is populated with “2” or “3” 
and must contain a [[Liquidity]] Fee Rate. 
o If the “Redemption Fee Indicator” field is populated with “0=Short Term Redemption (STR) Fee” or 
“1=STR Fee with CDSC”, the “Redemption Fee Rate” field must contain a Short-Term Redemption 
Fee Rate. 
• “Redemption Fee Money Amount” field 
o Effective September 26, 2016, [[NSCC]] renamed “STR Fee Money Amount” to “Redemption Fee 
Money Amount” (Important Notice a8159). 
o This optional/conditional field is required when “Redemption Fee Indicator” is populated with “2” or “3” 
and must contain a [[Liquidity]] Fee Amount. 
o If the “Redemption Fee Indicator” field is populated with “0=Short Term Redemption (STR) Fee”” or 
“1=STR Fee with CDSC”, the “Redemption Fee Money Amount” field must contain a Short -Term 
Redemption Fee Amount. 
 

---

## Page 43

Money Market Fund Reform User Guide & Best Practice 
Change History 43 
Considerations and Best Practices 
• Intermediaries should leave the “Redemption Fee Indicator” field blank on their transactions. Funds are 
advised to ignore values of “2” or “3” in this field (if supplied by the firm). Upon confirmation, fund will 
provide the appropriate value in this field. 
• Transactions where “Money Market [[Liquidity]] Fee/Redemption Indicator” field = “F-Fund” or ‘blank’ and 
“Aggregated Order Indicator” field = ‘1’ or ‘2’ should be confirmed by funds with the fee information 
provided in the following fields: 
o “Redemption Fee Indicator” 
o “Redemption Fee Rate” 
o “Redemption Money Amount” 
• For orders received with a “Money Market [[Liquidity]] Fee/Redemption Indicator” field = ‘B’, the best practice 
is for funds to confirm without a dollar amount/rate, or without assessing a fee. Funds and intermediaries 
should follow previously established policies for [[Liquidity]] fee estimation and remittance outside of [[NSCC]]
16. 
• “STR Fee Share Quantity” field is not permitted for [[Liquidity]] Fee purposes and is not allowed when 
“Redemption Fee Indicator” is “2 = Money Market [[Liquidity]] Fee” or “3 = Money Market [[Liquidity]] Fee with 
CDSC”. 
• Fee should be netted from the transaction amount 
o For redemptions where fund is assessing the fee (I.e., “Money Market [[Liquidity]] Fee/Redemption 
Indicator” field = “F” or Blank), the best practice is for Intermediaries to consider w hether the 
transmitted redemption amount will meet the shareholder needs. Funds will reduce the redemption 
proceeds by the fee amount before [[settlement]]. For example, a $100 redemption request made 
during a 2% fee event will yield $98 in [[settlement]] proceeds (i.e., net the fee amount). 
 
 
 
 
16 The Working Group considered requesting modifications to [[DTCC]] Payment aXis® to allow for [[Liquidity]] fee remittance but ultimat ely determined that expected 
volumes would not be sufficient to support the initiative. It was decided that for firm assessed transactions, firms will remit [[Liquidity]] fees outside of [[NSCC]].  

---

## Page 44

Money Market Fund Reform User Guide & Best Practice 
Change History 44 
6. NETWORKING IMPACT 
In the event a [[Liquidity]] Fee is imposed by a fund and directly charged to an account, the Fund will need to 
communicate the [[Liquidity]] Fee applied to accounts to intermediaries as part of their regular F55 A ctivity 
reporting. Funds will use the following fields to provide the [[Liquidity]] fee rate and amount on the direct 
redemption activity processed by the fund. 
• In order to indicate the applicable fee type, effective September 26, 2016 (Important Notice a 8159), 
“Transaction Type” field was expanded to include two new “Transaction Description Codes”  under 
“Transaction Type” =”02–Direct Redemption”: 
o BN = Money Market [[Liquidity]] Fee 
o BO = Money Market [[Liquidity]] Fee with CDSC 
• New Fields (“Redemption Fee Rate” and “Redemption Fee Money Amount”) were added to the F55 
Activity Reporting record sequence #6 (Important Notice a8159). Depending on the value provided in the 
“Transaction Type” field, the “Redemption Fee Rate” and “Redemption Fee Money Amount” fields can 
also be used to communicate STR or [[Liquidity]] Fee rate and amount. 
o “Redemption Fee Rate” field–Optional/Conditional. Format 99.99999 
» This field is Required when “Transaction Type” field is populated with one of the following 
“Transaction Description Codes”: ‘BN’ or ‘BO’. 
» Zero value is not allowed when this field is required and will be rejected by [[NSCC]].  
» This field can be used to pass the Redemption Fee Rate for the following fee types:  
• Money Market [[Liquidity]] Fee 
• Short Term Redemption (STR) Fee 
o “Redemption Fee Money Amount” field–Optional/Conditional. Format 99,999,999,999,999.99 
» This field is Required when “Transaction Type” field is populated with one of the following 
“Transaction Description Codes”: ‘BN’ or ‘BO’. 
» Zero value is not allowed when this field is required and will be rejected by [[NSCC]].  
» This field can be used to pass the Redemption Fee Money Amount for the following fee types:  
• Money Market [[Liquidity]] Fee 
• Short Term Redemption (STR) Fee 
 
Considerations and Best Practices 
• [[settlement]] through [[NSCC]] 
Certain activity for Direct Accounts at the fund can be settled through [[NSCC]], specifically, Direct 
Redemptions (“Transaction Type” = 02 or “Transaction Description Codes” starting with “B”) and 
Systematic Withdrawals. The fund must monitor their Direct Accounts and make sure they are coded 
appropriately to prevent [[settlement]] from occurring through the [[NSCC]] Networking System.  
To ensure that [[settlement]] does not happen, the fund must select the appropriate value in the “Cash 
Disbursement Indicator” field
17: 
o A value of “0 = Cash to Firm” or “6 = Cash to Trust” will result in [[settlement]] through [[NSCC]]  
o Values 1-5 will NOT cause [[settlement]] to occur 
 
17 In most instances, [[Mutual Funds]] would want to avoid [[settlement]] of [[Liquidity]] Fees through Networking.  

---

## Page 45

Money Market Fund Reform User Guide & Best Practice 
Change History 45 
• Single F55 transaction to report direct redemptions and exchanges 
Prior to September 26, 2016, funds reporting a Direct Redemption with an STR (or STR with CDSC) fee 
provided two F55 Activity transactions. 
o The 1st Activity transaction indicated “Transaction Type” = “02-Direct Redemption” and reported a 
redemption dollar amount 
o The 2nd Activity transaction had “Transaction Type” = BH (STR Fee) or BI (STR with CDSC) and the 
STR fee amount in the “Dollar Amount”. 
Effective September 26, 2016, funds are no longer required to send two F55 Activity transactions when 
reporting a direct redemption (or an exchange) with a Redemption Fee. The following best practice 
provides guidance on reporting direct redemptions (or exchanges) with STR* or Money Market [[Liquidity]] 
Fees: 
o In order to communicate a redemption fee (Short Term Redemption or Money Market [[Liquidity]] Fee) 
on the Activity Record funds should send a single F55 Activity transaction 
o Redemption Amount (netted of the fee) should be populated in the “Dollar Amount” field  
o “Redemption Fee Money Amount” field should contain the Money Market [[Liquidity]] Fee Amount (or 
STR Fee Amount) 
o “Redemption Fee Rate” should contain the Money Market [[Liquidity]] Fee Rate (or STR Fee Rate)  
o CDSC fee amount (if also applies) should be provided in the “Commission /CDSC Amount” field  
o “Transaction Type” field should be populated as follows: 
 
Direct activity at the Fund Transaction 
Description Code 
Direct Redemption with a Money Market [[Liquidity]] Fee BN 
Direct Redemption with a Money Market [[Liquidity]] Fee with CDSC BO 
Direct Redemption with an STR Fee BH 
Direct Redemption with an STR Fee with CDSC BI 
Exchange with a Money Market [[Liquidity]] Fee 10 
Exchange with a Money Market [[Liquidity]] Fee with CDSC 10 
 
*Note 
The above best practice was created for communication of Money Market [[Liquidity]] Fees, however for consistency purposes 
it is recommended that funds also adopt this method when reporting STR (and STR with CDSC) fees. Funds are strongly 
encouraged to adhere to these recommendations when reporting STR fees, however clients can also continue reporting 
STR fees by following their previously established practices (that have been in place prior to September 26, 2016.) 
• Single F55 transaction to report redemption cancellations 
Prior to September 26, 2016, funds reporting a cancelation of redemption activity with an STR (or STR 
with CDSC) fee provided two F55 Activity transactions. The 1st Activity transaction reported a cancelled 
redemption dollar amount. The 2nd Activity transaction reversed the fee associated with the original 
redemption.  

---

## Page 46

Money Market Fund Reform User Guide & Best Practice 
Change History 46 
Effective September 26, 2016, funds are no longer required to send two F55 Activity transactions when 
reporting cancelations of redemptions that included a Redemption Fee. It is recommended that Funds 
send a single F55 Activity transaction with the following data elements: 
o Redemption Amount (netted of the fee) should be populated in the “Dollar Amount” field 
o “Redemption Fee Money Amount” field should contain the Money Market [[Liquidity]] Fee Amount (or 
STR Fee Amount) 
o “Redemption Fee Rate” should contain the Money Market [[Liquidity]] Fee Rate (or STR Fee Rate)  
o CDSC fee amount (if also applies) should be provided in the “Commission/CDSC Amount” field  
o “Debit/Credit Indicator” should be set to “2=Credit” to indicate that transaction is a cancellation  
o “Transaction Type” should be populated with the same value that was provided on the original 
transaction
18 (see above section on reporting direct redemptions). 
*Note 
The above best practice was created for communication of cancellations of direct redemptions with [[Liquidity]] Fees, however 
for consistency purposes it is recommended that funds also adopt this method when reporting cancellations for 
redemptions that contained STR (and STR with CDSC) fees. Funds are strongly encouraged to adhere to these 
recommendations when reporting cancellations of redemptions with STR fees, however clients can also continue reporting 
cancellations of redemptions with STR fees by following their previously established practices (that have been in place prior 
to September 26, 2016.) 
  
 
18 Some funds might choose to provide the value of “25 = Redemption Cancellation” in the “Transaction Type” field.  

---

## Page 47

Money Market Fund Reform User Guide & Best Practice 
Change History 47 
7. ACATS CONSIDERATIONS 
Mutual fund transfer transactions, by definition, should not be subject to fees and gates because they are 
simply a reregistration of fund [[shares]]. A transfer transaction—whether a [[Broker]]-to-[[Broker]] ACATS or fund-to-
[[Broker]] ACATS PTF does not increase or decrease a fund’s [[shares]] outstanding so has no impact on the 
[[Liquidity]] of the fund portfolio. 
A unique situation may occur with regard to the transfer of money market fund assets through ACATS. In some 
instances, the [[intermediary]] receiving the transfer cannot hold the [[Asset]] to be transferred—such as a 
proprietary money market fund or sweep product. The delivering [[intermediary]] must first redeem the money 
market fund and then arrange to transfer the cash value to the receiving [[intermediary]] as part of the ACATS. 
The process is described below: 
1. During the review phase the delivering ACATS counterparty will add a record to the ACATS that will state 
the amount of cash that will be delivered on the last day of the ACATS cycle when assets and cash 
transfer. Once the cutoff for [[Asset]] delivery adjustment passes, the deliverer cannot change or remove any 
records on the ACATS–the ACATS is locked. 
2. Two days later, the ACATS reaches its final transfer date and cash is moved to the [[custody]] of the 
receiving firm. On this same date, the money market fund’s cash proceeds are received as an offset to 
this cash movement. 
 
A money market fee or gate in place when cash proceeds are to be received to fulfill the ACATS would impact 
the delivering [[intermediary]] and necessitate future adjustments to both sides of the transaction. The following 
table was assembled by an industry task force
19 to help intermediaries in this situation: 
Gate Placed on Money Market Fund 
ACATS Step and Scenario Best Practice 
ACATS Full Review Day (Post Deliverer Adjust Cutoff) 
Gate initiated between the deliverer adjust cutoff and 
Settle Close. In this situation a firm will deliver cash but will 
be unable to [[Liquidate]] the money market fund. As a result, 
they will have an outstanding debit for the cash amount 
but still hold the money market [[Asset]]. 
Deliverer should put up a reclaim for the cash amount. Once 
the gate is removed the deliverer should [[Liquidate]] the money 
market fund and the cash will move on a residual credit. 
ACATS Full Review Day (pre-Deliver Adjust) 
Gate initiated following the addition of assets to the 
ACATS record by the delivering firm and prior to the 
deliverer adjust cutoff. Because the deliverer adjust cutoff 
has not been reached, the delivering firm can change the 
ACATS record cash amount. 
Deliverer will adjust the cash amount to 0. Deliverer will 
memo the Money Market Fund on the ACATS, with the 
Security Issue [[ID]], and add an [[Asset]] level note that the fund is 
gated and will be redeemed for delivery once the gate is 
removed. 
ACATS Full Review Day (full review) 
Gate placed on a money market fund, prior to full review, 
so the delivering firm has not yet added the [[Asset]] list. 
Deliverer will memo the Money Market Fund on the ACATS, 
with the Security Issue [[ID]], and add an [[Asset]] level note that 
the fund is gated and will be redeemed for delivery once the 
gate is removed. 
 
19 The SIFMA [[CAT]] Division and ICI BDAC/BTRAC Transfers Task Force broadly collaborated on mutual fund transfer initiatives and A CATS Fund/SERV® 
initiatives in particular. For additional Money Market Fund Reform related enhancements for ACATS, please refer to Important Notice a8164. 

---

## Page 48

Money Market Fund Reform User Guide & Best Practice 
Change History 48 
Gate Placed on Money Market Fund 
All Cash 
(i.e., Money Market Fund is the only [[Asset]] in account, or 
cash is the only [[Asset]] being requested (PTR)) 
Gate placed on a money market fund and it is the only 
[[Asset]] in the account. 
Delivering firm should reject the ACATS with Reject code 
“9=Missing authorization signature”
20. 
Receiving firm must submit a new request once the gate is 
removed. 
Fee Placed on Money Market Fund 
Fees Known Pre-Full Review 
Fee placed on a money market fund prior to [[Asset]] list 
being added. 
Add cash amount minus fee amount. 
Fees Assessed between Full Review and [[liquidation]] 
Fee assessed following the assets being added to the 
record, and prior to the [[liquidation]] of the fund. Result is the 
fee lowers the amount expected from the sale. 
Delivering firm will reclaim the fee amount from the receiving 
firm. 
 
  
 
20 It is also recommended that the firm states that the Money Market Fund is gated in the “Comments” field on TI record.  

---

## Page 49

Money Market Fund Reform User Guide & Best Practice 
Appendix A – History of [[NSCC]] Money Market Fund Reform Enhancements Important Notices 49 
APPENDIX A – HISTORY OF [[NSCC]] MONEY MARKET 
FUND REFORM ENHANCEMENTS IMPORTANT NOTICES 
• a8073-[[NSCC]] implemented social code changes effective November 30, 2015 
• a8163-[[NSCC]] delivered enhancements to MFPS II on May 31, 2016 
• a8159-[[NSCC]] delivered enhancements to MFPS I and Networking on September 26, 2016  
  

---

## Page 50

Money Market Fund Reform User Guide & Best Practice 
Appendix B - [[NSCC]] [[Mutual Funds]] Services Record Layouts–Price/NAV Fields 50 
APPENDIX B - [[NSCC]] [[Mutual Funds]] SERVICES 
RECORD LAYOUTS–PRICE/NAV FIELDS  
Fund/SERV®–Variable 
Part I 
As-Of-Order 004 
Price Per Share 519 530 12 N 999,999.999999 
Optional for record type 004 
RC 027 
 
Exchange Confirmation 016 
Exch From Price Per 
Share 
498 509 12 N 999,999.999999 R 027 
 
Exch To Price Per 
Share 1 
709 720 12 N 999,999.999999 R 027 
 
Exch To Price Per 
Share 2 
802 813 12 N 999,999.999999 R 027 
 
Exch To Price Per 
Share 3 
895 906 12 N 999,999.999999 R 027 
 
Exch To Price Per 
Share 4 
988 999 12 N 999,999.999999 R 027 
 
Exch To Price Per 
Share 5 
1081 1092 12 N 999,999.999999 R 027 
 
Part II 
ToRA Acknowledgment (211) 
Price Per Share 316 327 12 N 999,999.999999 
Optional for record type 211 
RC 027 
 
 

---

## Page 51

Money Market Fund Reform User Guide & Best Practice 
Appendix B - [[NSCC]] [[Mutual Funds]] Services Record Layouts–Price/NAV Fields 51 
Part III 
Settling Trade Detail (070) 
*Price Per Share 129 140 12 N 999,999.999999 
 
Correction 003 
Price Per Share 519 530 12 N 999999.999999 
Optional for record type 003 
RC 027 
 
Original Price Per 
Share 
802 813 12 N 999,999.999999 
Required if Correction Indicator 
= P and Original Control Number is 
not provided 
OC 027 
Networking: 
Account Conversion 
Account Conversion/Update (A/B/T50, A/B/T/F51) #5 
Field Name Start End Len Type Description Opt/Req 
50/51 
NAV Account 
Indicator 
52 52 1 A/N 0 = Other 
1 = NAV Transfer 
2 = Repurchase 
3 = Employee 
4 = Firm/Error Account 
5 = Wrap Fee Account 
6 = No 
7 = Commissionable Defined Contribution 
Plan 
8 = Non-Commissionable- Defined 
Contribution Plan 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per Agreement 
R/O 

---

## Page 52

Money Market Fund Reform User Guide & Best Practice 
Appendix B - [[NSCC]] [[Mutual Funds]] Services Record Layouts–Price/NAV Fields 52 
Activity Reporting 
Activity Reporting Records Activity Detail (F55) #2 
Field Name Start End Len Type Description Opt/Req 
50/51 
Price 31 42 12 N 999999.999999 R 
[[Dividend]] Activity 
[[Dividend]]/Capital Gain Detail Record For Reinvest Accounts Not Subject To Withholding (F65) #1  
Field Name Start End Len Type Description Opt/Req 
50/51 
Reinvest Price 41 52 12 N 999,999.999999 R 
 
[[Dividend]]/Capital Gain Detail Record For Reinvest Accounts Subject To Withholding (F66) #1  
Field Name Start End Len Type Description Opt/Req 
50/51 
Reinvest Price 63 74 12 N 999999.999999 R 
Standardized Data Reporting 
SDR Detail (B/U24) Record 1 of 2 
Field Name Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Price 80 91 12 N 999,999.999999 
Optional if Transaction Type = 05 or 06, 
or if Transaction Code = 7 or 52. 
RC 38 

---

## Page 53

Money Market Fund Reform User Guide & Best Practice 
Appendix B - [[NSCC]] [[Mutual Funds]] Services Record Layouts–Price/NAV Fields 53 
Share Aging 
Share Aging Detail (B/F76) Record 1 of 2 
Field Name Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Price per Share 23 34 12 N 999,999.999999 
Required if Dollar Amount is not 
provided and Transaction Code is not = 
08 
OC 47 
[[DTCC]] Payment aXis® 
Payment aXis®–Commission and Fee [[settlement]] 
Mutual Fund [[DTCC]] Payment aXis® Detail Record #2 
Field Name Start End Len Type Description Opt/ 
Req 
Price per Share 55 66 12 N 999,999.999999 
Required if Commission Type = 01, 02, 03 or 
04 
O 
 
529 Aggregation–N/A 
Account Conversion & Transfer–N/A 
Account Maintenance–N/A 
Position Reporting Record–N/A 
Retirement Plan Reporting–N/A 
General Records–N/A 
Omni/SERV–Position–not our file 
Omni/SERV- Activity–not our file 
*Payment aXis®–Global–N/A 
*Payment aXis ®– Invoicing and Fee [[settlement]]–N/A 
  

---

## Page 54

Money Market Fund Reform User Guide & Best Practice 
Appendix B - [[NSCC]] [[Mutual Funds]] Services Record Layouts–Price/NAV Fields 54 
MFPS 
MFPS I Price and Rate-ISO 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
M 35H Cash Amount 
(Modified, 
Effective Q3, 
2016) 
Amount (NAV, Rate 
or Cumulative 
[[Dividend]] Rate) 
[N]3a19number 
 
N = indicates a negative 
amount 
3a = ISO currency 
code: USD, EUR, GBP, AUD, 
CAD, CHF, CNY, HKD, JPY, 
NOK, SEK or SGD 
19number = amount 
Edit: 
1. Amount not allowed to be 
negative (sub- field ‘N’ not 
allowed). 
2. Max digits in amount must 
correspond to Info Type as 
follows: 
If Info Type = PRCO, 
PRCC, PRMO, or PRMC, 
then max digits = 9n.9n 
If Info Type = DIVO or 
DIVC, then max digits = 
9n.9n 
If Info Type = CUMO or 
CUMC, then max digits = 
4n.9n 
3. If Info Type = PRCO, 
PRCC, PRMO, or PRMC 
then amount must be 
positive. Otherwise, 
amount can be zero 
For JPY Currency, a decimal 
point (,) followed by nine 0’s is 
required after the value. 
This field will contain the actual 
NAV, rate or cumulative 
[[Dividend]] rate. 
Examples for USD Only: 
1. A price of 1.023 per share 
would be expressed as: 
:IT:PRCO 
:35H:USD 1,023 
 
2. A zero rate would be 
expressed as: 
:IT:DIVO 
:35H:USD 0, 
 
Examples for JPY Only: 
 
1. A price of 111 Yen per 
share would be expressed 
as: 
:IT:PRCO 
:35H:JPY 111,000000000 
 
2. A rate of 2050 Yen would 
be expressed as: 
:IT:DIVO 
:35H:JPY 2050,000000000 
 
3. A cumulative rate of 8431 
Yen would be expressed 
as: 
:IT:CUMO 
:35H:JPY 8431,000000000 
 
 
 
 

---

## Page 55

Money Market Fund Reform User Guide & Best Practice 
Appendix B - [[NSCC]] [[Mutual Funds]] Services Record Layouts–Price/NAV Fields 55 
MFPS I Price and Rate–Record 30 Fixed and Variable 
Fixed 030 Record 1 or 4 
Field Name Start End  Len  Type Description Opt/ 
Req 
Reject 
Code 
Price (NAV) 46 63 18 N 999,999,999.999999999 
Required if Price Correction Indicator 
= 1, 2, 3, or 4. 
(Effective Q3, 2016). 
Not allowed if Price Correction 
Indicator = space. 
For JPY Currency only, each of the 
last nine positions must be populated 
with a value of 0. 
Example: A Price of JPY 111 should 
be entered as 000000111000000000 
OC 0085 
 
Variable  
Field Name Start End  Len  Type Description Opt/ Req Reject 
Code 
Price (NAV) 50 67 18 N 999,999,999.999999999  
 
Required if Price Correction 
Indicator = 1, 2, 3, or 4.   
 
Not allowed if Price Correction 
Indicator = space. 
 
For JPY Currency only, each of 
the last nine positions must be 
populated with a value of 
0.  Example: A Price of JPY 111 
should be entered as 
000000111000000000 
 
(Effective Q3, 2016) 
OC 0085 
 
 
 
 
 
 
 

---

## Page 56

Money Market Fund Reform User Guide & Best Practice 
Appendix B - [[NSCC]] [[Mutual Funds]] Services Record Layouts–Price/NAV Fields 56 
MFPS II Distribution Declaration–Record 041 Fixed and Variable 
Fixed 041 Record 2 of 2 
Field Name  Start End Len Type Description  Opt/
Req 
Reject 
Code 
Reinvest Price  59  76  18  N 999999999.999999999  O 0297 
 
 
Field Name  Start End Len Type Description  Opt/
Req 
Reject 
Code 
Reinvest Price  137  154  18  N 999999999.999999999  O 0297 
 
 

---

## Page 57

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: February 5, 2024 
Publication Code: MFS359 
Service: Mutual Fund Services 
Title: Money Market Fund Reform and Best Practice  
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 