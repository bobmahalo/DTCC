---
title: "net-direct_acct_bp_mfs308_20230803.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net-direct_acct_bp_mfs308_20230803.pdf"
pages: 20
size: "592.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# net-direct_acct_bp_mfs308_20230803.pdf

**Original File:** [net-direct_acct_bp_mfs308_20230803.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net-direct_acct_bp_mfs308_20230803.pdf)  
**Category:** Other  
**Total Pages:** 20  
**File Size:** 592.1 KB  

---

## Page 1

 
 
 
Networking 
DIRECT ACCOUNT NETWORKING – BEST 
PRACTICES 
AUGUST 3, 2023 
 

---

## Page 2

Direct Account Networking – Best Practices 
Direct Account Networking Overview 2 
REVISION HISTORY 
Date Revisions 
08/03/2023 Document has been rebranded.  

---

## Page 3

Direct Account Networking – Best Practices 
Direct Account Networking Overview 3 
TABLE OF CONTENTS 
Direct Account Networking Overview ................................................................................................................ 5 
How the Networking System Relates to Direct Accounts .................................................................................... 5 
How Direct Networking Differs from Traditional Networking ................................................................................ 5 
Business Objectives of Direct Networking ........................................................................................................... 5 
System Functions ................................................................................................................................................ 6 
Fund Functionality ............................................................................................................................................... 6 
Firm Functionality ................................................................................................................................................ 6 
Conversion/Update Processing .......................................................................................................................... 6 
Activity Reporting ................................................................................................................................................ 8 
Position Reporting ............................................................................................................................................... 8 
[[Dividend]] Reporting .............................................................................................................................................. 9 
Processing Scenarios ........................................................................................................................................ 10 
Conversion/Update Processing .........................................................................................................................10 
Full Refresh- Reporting “Existing” Client Accounts from Mutual Fund to Firm (Flowchart 1)  .........................10 
Partial Refresh - Reporting “New Direct at Fund” Accounts from Mutual Fund to Firm (Flowchart 2) ............10 
Partial Refresh - Reporting “Selected” Non-Financial Activity from Mutual Fund to Firm (Flowchart 3) ..........11 
Activity Reporting ..............................................................................................................................................11 
Financial (Non-[[Dividend]]) Transactions from Mutual Fund to Firm (Flowchart 4) ............................................11 
Position Reporting .............................................................................................................................................12 
Periodic Position Reporting from Mutual Fund to Firm (Flowchart 5) ..............................................................12 
[[Dividend]] Reporting ...........................................................................................................................................12 
Reporting of [[Dividend]] Transactions from Mutual Fund to Firm (Flowchart 6) .................................................12 
Flow Charts ......................................................................................................................................................... 13 
Conversion/Update Processing ........................................................................................................................13 
Flowchart 1: Full Refresh – Reporting “Existing” Client Accounts from Mutual Fund to Firm ........................13 
Flowchart 2: Partial Refresh - Reporting “New Direct at Fund Accounts" from Mutual Fund to Firm ..............14 
Flowchart 3: Partial Refresh – Reporting “Selected” Non-Financial Activity from Mutual Fund to Firm .........15 
Activity Reporting ..............................................................................................................................................16 

---

## Page 4

Direct Account Networking – Best Practices 
Direct Account Networking Overview 4 
Flowchart 4: Reporting of Financial (Non-[[Dividend]]) Transactions from Mutual Fund to Firm ........................16 
Position Reporting.............................................................................................................................................17 
Flowchart 5:  Periodic Position Reporting from Mutual Fund to Firm .............................................................17 
[[Dividend]] Reporting ...........................................................................................................................................18 
Flowchart 6: Reporting of [[Dividend]] Transactions from Mutual Fund to Firm ..................................................18 
Exhibit A - Direct Account Networking File Request Form* .......................................................................... 19 
 

---

## Page 5

Direct Account Networking – Best Practices 
Direct Account Networking Overview 5 
DIRECT ACCOUNT NETWORKING OVERVIEW 
How the Networking System Relates to Direct Accounts 
Networking is a centralized and standardized data communications system for the exchange of customer 
account level activity and information. Networking was implemented in 1988 to permit the transmission of data 
between participants to reconcile the firm’s records with the fund’s records. 
Networking is the industry standard for the exchange of mutual fund customer account maintenance and 
reporting. The Networking system allows non-trade related client information to appear identically on the 
records of 
• Fi rms and funds, or 
• T ransfer agents for firms and funds 
 
With Ne
tworking, firms and funds can exchange timely and accurate information about their customers, in a 
controlled environment. 
 
How Direct Networking Differs from Traditional Networking 
In a traditional networking relationship (Networking Matrix Levels 3-4 and Trust Networked Matrix Level 0) a 
firm establishes shareholder accounts, whether firm controlled or fully disclosed, on the books of a fund. 
However, in a direct account networking relationship the shareholder accounts are typically established, 
maintained and controlled by the fund. In a direct account relationship, the fund will inform the firm of the 
account’s assets, activity, registration and additional account attributes. The firm will in turn gather the 
information from the fund for its “books & record” requirement. The firm may also use this information to 
determine the appropriate breakpoint for a client. 
Although Tr ust Networked Matrix Level 0 (Trust Networked) accounts are not fund controlled, firms still require 
information if they are listed as the [[Broker]] of record.  For purposes of this document, ‘direct at fund’ (Direct 
Accounts) will be defined as fully disclosed by the fund or Trust Networked. Trust Networked accounts are 
included in direct account networking to send applicable networking files to the [[Broker]] dealer of record on a 
Trust Networked account, if they are set up for direct networking at the fund. 
 
Business Objectives of Direct Networking 
(A firm and mutual fund data exchange) 
• Satisfy Recommendation (L) (“[[Broker]]/Dealer Transmission of TIN/BIN Data”) of the Joint  
[[NASD]]/Industry Task Force on Breakpoints 
• Assist firms in meeting their “books and records” requirements. Direct Networking satisfies this 
requirement. (See [[SEC]] [[Rule 17a-3]](a)(1) below) 
Note 
“[[Rule 17a-3]](a)(1) requires that a [[Broker]]-dealer make and keep current blotters containing, among other things, an itemized 
daily record of all purchases and sales of [[securities]] and all receipts and disbursements of cash.” Under [[Rule 17a-3]](a)(1), a 
[[Broker]]-dealer must record all purchases or sales of [[Mutual Funds]], variable contracts, or direct participation programs.” 
 
  

---

## Page 6

Direct Account Networking – Best Practices 
System Functions 6 
SYSTEM FUNCTIONS 
This section describes the primary systems functions for Direct Accounts through Networking. 
Fund Functionality 
Funds use the components of the Networking System as follows: 
1. CONVERSION/UPDATE PROCESSING 
2. ACTIVITY REPORTING 
3. POSITION REPORTING 
4. [[Dividend]] REPORTING 
 
Firm Functionality 
Firms receive Networking files for Direct Accounts submitted by the fund where the firm is the “[[Broker]] of record”. 
 
Conversion/Update Processing 
Funds can report the establishment and update of Direct Accounts to the respective “[[Broker]] of record” by 
submitting Fund Conversion Update records through Networking. These Fund Conversion Update records are 
submitted using the Networking Record Type F51 (registration and account records) sent to the [[Broker]] of 
record for that [[participant]] account. 
Full Refresh: Funds should submit a Networking Conversion Update (F51) record prior to beginning the daily 
process of submitting daily Fund Conversion Records.  This full refresh will provide an initial Direct Account 
base to the respective [[Broker]] of record.  Records sent should contain the full name, address, SSN/TIN, social 
code, date of birth (if available), and any optional fields outlined in this document as a best practice, for all 
“direct at fund” accounts established on their books.  
It is recommended that funds submit a full refresh to ensure that all non-financial information on the fund’s 
books are transmitted to the firm ensuring that both the fund and firms records are in synch. Funds and firms 
should coordinate the timing of their transmissions, and inform their respective transfer agents, if necessary.  
When a full refresh is submitted by the fund to the firm, the Scrub Indicator field (F51, record 01, position 81) 
should be populated with a value of 1 (Scrub Record). 
Partial Refresh: On an ongoing basis, new Direct Accounts and selected non-financial changes occurring on 
Direct Accounts, such as an address change, should be transmitted by the fund to the firm using the F51 
record. 
It is recommended that funds transmit the optional information outlined below, where available and/or 
applicable, in addition to all required fields on a F51 for a Direct Account.  Please reference the [[NSCC]] record 
layouts for applicable field values and descriptions.  Networking record layouts can be found on the Learning  
Center in the Mutual Fund Section at https://dtcclearning.com/products -and-services/mutual-fund-
services/record-layouts.html 

---

## Page 7

Direct Account Networking – Best Practices 
System Functions 7 
Field Name in F51 Record Layout Best Practice Usage 
Beneficiary/Successor owner/Additional 
account owners fields 
Provides firms with the name, address, SSN & DOB for any additional 
account holders, such as a joint tenant.   
Note: This information is required for 529 accounts but optional for regular 
accounts. 
Payable information Provide payable information to the firm for distributions and/or investments. 
Account/Owner US Citizenship Indicator Provides citizenship information to the firm. 
[[Dividend]] code Provides distribution elections to the firm. 
Owner date of birth Provides the shareholder DOB to the firm for “know your customer” 
reporting. 
Reference Number Assign a reference number according to [[NSCC]] rules.  This allows all 
parties to better [[Locate]] a record if issues are encountered. 
RPO Code Provides ‘Returned Post Office’ information to the firm. 
Withhold indicator Provides withholding information to the firm. 
Account Name and Address (Lines 1 and 
2) 
Populate if new account, scrub file, name/address change, or change of 
[[Broker]]/dealer. 
ROA number Provides rights of accumulation information to the firm for best pricing. 
Account Name and Address (Lines 3 and 
4) 
Populate if new account, scrub file, name/address change, or change of 
[[Broker]]/dealer. 
Account Name and Address (Lines 5 and 
6) 
Populate if new account, scrub file, name/address change, or change of 
[[Broker]]/dealer. 
Membership Identifier Populate with a value of 01 (trust [[Member]]) if the account is Trust 
Networked. This allows the firm to identify when an account is Trust 
Networked vs fund direct and identify the trust partner for the position.   
Plan account indicator If available, allows the firm to identify additional plan information when an 
account is Trust Networked.   
Plan account number If available, allows the firm to identify additional plan information when an 
account is Trust Networked.   
Trust/TPA/Investment Agent Number Populate with the [[NSCC]] [[participant]] number assigned to the trust if the 
account is Trust Networked. This allows the firm to identify when an 
account is Trust Networked vs fund direct and identify the trust partner for 
the position. 
Account Representative name Provides the account representative name on the account to the firm. 
Account Representative number Provides the account representative number on the account to the firm. 
Agent for firm number Provides the account dealer number to the firm. 
Branch identification number Provides the account branch number on the account to the firm. 

---

## Page 8

Direct Account Networking – Best Practices 
System Functions 8 
Field Name in F51 Record Layout Best Practice Usage 
Change in [[Broker]]/dealer indicator If a change in dealer of record is performed, provides the contra dealer 
information to the firm. 
New/Contra [[Broker]] of record If a change in [[Broker]] of record is performed, provides the account’s contra 
[[Broker]] number to the firm. 
State of sale Provides the account state of sale to the firm. 
Beneficiary Date of Birth Populate if a retirement plan – provides firms with the required information 
for managing retirement plan accounts. 
 
Note: This information is required for 529 accounts but optional for regular 
accounts. 
 
 
Activity Reporting 
Financial (Non-[[Dividend]]) Activity reporting on Direct Accounts is accomplished using Record Type F55, but 
normally without [[settlement]] through the Networking System. 
Typically, the Activity file is used by funds to inform the firms of all non-Fund/SERV activity, transacted directly 
between the shareholder and the fund. Funds inform firms of changes in share balances of their Direct 
Accounts. Activity reporting allows a fund to send information from its books to the “[[Broker]] of record.” 
Certain activity for Direct Accounts at the fund can be settled through [[NSCC]], specifically, Direct Redemptions 
and Systematic Withdrawals. The fund must monitor their Direct Accounts and make sure they are coded 
appropriately to prevent [[settlement]] from occurring through the Networking System. (Please refer to 
“Cash Disbursement Indicator” options in the Activity [[settlement]] box below.) 
 
Activity [[settlement]] 
Direct Liquidations and SWP transactions can settle using the Networking system. Funds should not settle these Activities 
for their Direct Accounts. To ensure that this does not happen, the fund must select the appropriate “Cash Disbursement 
Indicator.” A value of 0 = Cash to Firm or 6 = Cash to Trust will result in [[settlement]]. Values 1-5 will not cause [[settlement]] to 
occur. 
For any trans action involving [[shares]], a closing share balance is included as part of the transaction.  A closing share balance 
record is generated when a Fund/SERV transaction is settled.  Transaction Type 50 (Closing Balance Record) on Record 
Type F55 indicates the closing balance on an account as a result of the Activity. 
 
Position Reporting 
Position reporting for Direct Accounts is accomplished by using Record Type F58. 
Position reporting allows the fund to report to the firm, on a schedule agreed upon by both, the closing balance 
for each Direct Account as of a specific date. These files are sent to the firm listed as the “[[Broker]] of record” on 
the funds’ books. The firm can use this file to reconcile its “books & records” and to calculate the proper 
breakpoints for the client. 
The Position file is used by funds to report Direct Account balances to firms on a periodic or “on request” basis. 
Position files for Direct Accounts can be sent separately or in the same transmission as other Networked 
accounts (Matrix Level 3 and 4). 

---

## Page 9

Direct Account Networking – Best Practices 
System Functions 9 
It is the responsibility of the fund and firm to arrange a transmission schedule for Position files. 
Note 
To coordinate delivery of Direct Account networking transmissions, firms should complete the Direct Account Networking File 
Request Form (Exhibit A) and provide it to the fund. 
[[Dividend]] Reporting 
[[Dividend]] processing permits funds or their agents to communicate [[Dividend]] and capital gain information to 
firms on Direct Accounts.  Funds must also provide closing share balances each time they report distributions, 
including those for Direct Accounts. 
For [[Dividend]] processing for Direct Accounts, the [[Dividend]] Reporting Records (F61- F70) should be used to 
report [[Dividend]]/Capital Gain distributions without [[settlement]] occurring through the system. However, Trust 
Networked Level 0 accounts may be coded with a Cash Disbursement Indicator 6 (cash to trust) which will 
generate [[settlement]]. Only the record to the Trust will have the indicator = 6; the record to the firm should have 
a cash disbursement indicator = 2 (cash to customer). 
Direct Accounts must not be coded for [[settlement]] through the [[NSCC]] Networking System; doing so 
would create duplicate payments. (See “Cash Disbursement Indicator” options in the [[Dividend]] [[settlement]] box 
below). 
The system divides [[Dividend]] and capital gain information into two categories.  
• T
he first contains [[BASIC]] information for a mutual fund security when a distribution is being declared. This 
includes information such as Security Issue [[ID]] Number, Record Date, and Payable Date (Record Types 
F61 & F62 for the file Headers). 
• The second contains detailed information about individual accounts, such as: 
- The amount of the [[Dividend]] or capital gain 
- The r einvested share quantity (when applicable) 
- The c losing share balance as a result of the [[Dividend]] payment/capital gain 
- Any withholding information. 
 
Note 
Individual account details are reported using Record Types F63-F67. Record Types F68-F70 is for Trailer information. 
[[Dividend]] [[settlement]] 
[[settlement]] of Cash [[Dividend]]/Capital Gains can occur in the [[NSCC]] [[settlement]] System. Distribution information reported to 
[[NSCC]] and designated “Cash to Firm” or “Cash to Trust” will be settled through [[NSCC]]. Funds must make every effort to 
code the Cash Distribution Indicator correctly, so that [[settlement]] does not occur.  A value of 1 = Cash to Firm or 6 = Cash 
to Trust will result in [[settlement]]. Values 2-5 will not cause [[settlement]] to occur. 
 
  

---

## Page 10

Direct Account Networking – Best Practices 
Processing Scenarios 10 
PROCESSING SCENARIOS 
This section outlines the various scenarios that necessitate a Direct Account networking file to be delivered to a 
firm. 
Note 
To coordinate delivery of Direct Account networking transmissions, firms should complete the Direct Account Networking File 
Request Form (Exhibit A) and provide it to the fund. 
Account Number Fields  
The account number fields in the Networking records will reflect that of the fund (FIN or Fund Identification Numbers) and 
will be transmitted instead of BIN ([[Broker]] Identification Number), or in conjunction with a BIN. 
Conversion/Update Processing 
Full Refresh- Reporting “Existing” Client Accounts from Mutual Fund to Firm 
(Flowchart 1) 
• F unds deliver a Networking Conversion Update (F51) record containing the full name, address, SSN/TIN, 
social code, date of birth (if available), and any optional fields outlined in this document as a best practice, 
for all “direct at fund” accounts maintained on their books. 
• When a full refresh is submitted by the fund to the firm, the Scrub Indicator field (F51, record 01, position 
81) should be populated with a value of 1 (Scrub Record). 
• The timing of this file should be coordinated between funds and firms, and their respective [[transfer agent]].  
 
Partial Refresh - Reporting “New Direct at Fund” Accounts from Mutual Fund 
to Firm (Flowchart 2) 
When a new Direct Account is established by the fund, funds should submit a daily Networking Conversion 
Update (F51) record containing the full name, address, SSN/TIN, social code, date of birth (if available), and 
any optional fields outlined in this document as a best practice, for all new Direct Accounts established on their 
books. 
The F51 record for new “direct at fund” accounts should be submitted for: 
• New accounts established directly at the fund. 
• New accounts established due to a B to A roll or share class conversion. 
• Direct Accounts that are de-networked or networked to or from matrix levels of 3 or 4. 
• Accounts re-opened by new investment. 
• Accounts that reflect a new position as the result of [[Broker]]/dealer change.  
Note 
Funds should report [[Broker]]/dealer changes by submitting a Fund Conversion Update F51 record as indicated in “Partial 
Refresh - reporting of “Selected” Non-financial Activity from Mutual Fund to Firm” - Flowchart #3.  As a best practice, a 
change of [[Broker]]/dealer should generate a F51 to the delivering firm and the receiving firm.  The F51 sent to the delivering 
firm should only contain the new [[Broker]]/dealer information in record on sequence #9 and no other details (i.e., account 
registration). 

---

## Page 11

Direct Account Networking – Best Practices 
Processing Scenarios 11 
 
• B 50 transactions with Fund Account Response (FAR) indicator set to ‘1’ - fund should always send a Fund 
Account Response record (F51) to the firm.  For Trust Networked accounts, in addition to the F51 
response to the FAR, a second F51 should be generated to the [[Broker]] of record that is set up for direct 
account networking. 
Notes  
Trust Networked accounts - an F51 record should be generated to the [[Broker]] of record as the result of an applicable 
change occurring as requested by the trust, a Fund Account Response is not necessary in this situation. 
Trust submitted B50 transactions should generate a full set of F51 records to the [[Broker]] of record on the account, 
regardless of the Fund Account Response indicator.  
Fund Account Response (FAR) Indicator 
The Fund Account Response indicator field (FAR) is located on the F51, record 01, in position 82.  When a firm submits a 
B50 new account or B51 account maintenance to the fund, the FAR can be populated to tell the fund how to respond back 
to the firm in addition to the required F53 Acknowledgement.   
Valid values are: 
0 = Fund should NOT send a Fund Account Response record (F51) to the firm. 
1 = Fund should ALWAYS send a Fund Account Response record (F51) to the firm.  This indicator can apply to both B50 
and B51 records.  If the field is populated with a value = 1 on a B50/B51, the fund can respond with a F53 and a F51 
account record.   
2 = Fund should ONLY send a Fund Account Response record (F51) to the firm if the fund could not comply with the firm’s 
instructions.  This indicator applies to only B51 records.  If the field is populated with a value = 2 on the B51 and the fund is 
only able to process portions of the maintenance request, a F51 would be sent with the account information after the 
maintenance is processed.  This allows the firm to compare the B51 with the F51 and analyze the information processed 
vs. the information not applied to the shareholder account.  If none of the information can be applied by the fund, the firm 
will receive a F53 reject record.   
Partial Refresh - Reporting “Selected” Non-Financial Activity from Mutual Fund 
to Firm (Flowchart 3) 
Funds should submit a daily Networking Conversion Update (F51) record for all “direct at fund” accounts that 
had any of the following: 
• Change of address 
• Change of branch and/or representative 
• Change of social code 
• Change of SSN/TIN 
• ROA Number 
 
Activity Reporting 
Financial (Non-[[Dividend]]) Transactions from Mutual Fund to Firm (Flowchart 4) 
Funds submit a daily Networking Activity (F55) record for all “direct at fund” accounts that had financial activity. 

---

## Page 12

Direct Account Networking – Best Practices 
Processing Scenarios 12 
Position Reporting 
Periodic Position Reporting from Mutual Fund to Firm (Flowchart 5) 
Funds submit a Networking Position (F58) record for all “direct at fund” accounts on their books, on a schedule 
as agreed upon between the firm and the fund. 
[[Dividend]] Reporting  
Reporting of [[Dividend]] Transactions from Mutual Fund to Firm (Flowchart 6) 
Funds submit [[Dividend]] and Capital Gain Activity to firms for Direct Accounts using Record Types F61- F70. 
  

---

## Page 13

Direct Account Networking – Best Practices 
Flow Charts 13 
FLOW CHARTS 
Conversion/Update Processing 
Flowchart 1: Full Refresh – Reporting “Existing” Client Accounts from Mutual 
Fund to Firm 
 
 
  


---

## Page 14

Direct Account Networking – Best Practices 
Flow Charts 14 
Flowchart 2: Partial Refresh - Reporting “New Direct at Fund Accounts" from 
Mutual Fund to Firm 
 
Note 
Trust submitted B50 transactions should generate a full set of F51 records to the [[Broker]] of record on the account. 
 
 
 
  


---

## Page 15

Direct Account Networking – Best Practices 
Flow Charts 15 
Flowchart 3: Partial Refresh – Reporting “Selected” Non-Financial Activity 
from Mutual Fund to Firm 
 
 
 
 
 
  


---

## Page 16

Direct Account Networking – Best Practices 
Flow Charts 16 
Activity Reporting 
Flowchart 4: Reporting of Financial (Non-[[Dividend]]) Transactions from Mutual 
Fund to Firm 
 
  


---

## Page 17

Direct Account Networking – Best Practices 
Flow Charts 17 
Position Reporting 
Flowchart 5:  Periodic Position Reporting from Mutual Fund to Firm 
 
 
  


---

## Page 18

Direct Account Networking – Best Practices 
Flow Charts 18 
[[Dividend]] Reporting 
Flowchart 6: Reporting of [[Dividend]] Transactions from Mutual Fund to Firm 
 
 
 
 
 
 
  


---

## Page 19

Direct Account Networking – Best Practices 
Exhibit A - Direct Account Networking File Request Form* 19 
EXHIBIT A - DIRECT ACCOUNT NETWORKING FILE REQUEST FORM* 
 
 


---

## Page 20

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: August 3, 2023  
Publication Code: MFS308 
Service: Networking 
Title: Direct Account Networking – Best Practices  
For More Information 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 