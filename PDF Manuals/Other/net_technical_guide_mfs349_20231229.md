---
title: "Networking Technical Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_technical_guide_mfs349_20231229.pdf"
pages: 79
size: "798.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Networking Technical Guide

**Original File:** [net_technical_guide_mfs349_20231229.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_technical_guide_mfs349_20231229.pdf)  
**Category:** Other  
**Total Pages:** 79  
**File Size:** 798.6 KB  

---

## Page 1

 
 
 
Networking 
NETWORKING TECHNICAL GUIDE 
December 29, 2023 
 

---

## Page 2

Networking Technical Guide 
 
Revision History 2 
 
TABLE OF CONTENTS 
Revision History ................................................................................................................................................... 8 
Introduction to Networking Technical Manual .................................................................................................. 9 
Networking System ............................................................................................................................................. 9 
Chapter 1–Introduction to Networking ............................................................................................................ 10 
Overview ...........................................................................................................................................................10 
Purpose of the Document .................................................................................................................................10 
Definitions ........................................................................................................................................................10 
CHAPTER 2, SECTION A–ABOUT THE NETWORKING SYSTEM .................................................................. 11 
Overview ...........................................................................................................................................................11 
Description ......................................................................................................................................................11 
Purpose of the System ....................................................................................................................................11 
Who Can Use the System ...............................................................................................................................11 
Benefits of the Networking System ...................................................................................................................12 
Pre-Conversion Processing ..............................................................................................................................13 
Account Scrubbing Process ............................................................................................................................13 
Determining Account Registration ...................................................................................................................13 
After Scrubbing ................................................................................................................................................13 
Networking Primary System Functions .............................................................................................................13 
Functionality ....................................................................................................................................................13 
Conversion Processing ...................................................................................................................................14 
Activity Reporting ............................................................................................................................................14 
Position Reporting ...........................................................................................................................................14 
[[Dividend]] Processing ........................................................................................................................................14 
Year-End processing .......................................................................................................................................15 
Communicating with Networking ......................................................................................................................15 
Communication Options ..................................................................................................................................15 
Processing Schedule .......................................................................................................................................15 

---

## Page 3

Networking Technical Guide 
 
Revision History 3 
 
Chapter 2, Section B–System Processing by the Firm .................................................................................. 16 
Overview ...........................................................................................................................................................16 
Account Conversion, Update, and Transfer Reporting .....................................................................................16 
Purpose ...........................................................................................................................................................16 
Input Requirements .........................................................................................................................................16 
Control Numbers .............................................................................................................................................16 
Reminders .......................................................................................................................................................17 
[[NSCC]] Response .............................................................................................................................................17 
Chapter 2, Section C–System Processing by the Fund ................................................................................. 18 
Overview ...........................................................................................................................................................18 
Account Conversion, Update, Transfer and Acknowledgement Reporting ......................................................18 
Purpose ...........................................................................................................................................................18 
Use by Fund ....................................................................................................................................................18 
Input Requirements .........................................................................................................................................18 
[[NSCC]] Response .............................................................................................................................................18 
Activity Processing ............................................................................................................................................19 
Purpose ...........................................................................................................................................................19 
Use by Fund ....................................................................................................................................................20 
Input Requirements .........................................................................................................................................20 
[[NSCC]] Response .............................................................................................................................................20 
Position Processing ..........................................................................................................................................21 
Purpose ...........................................................................................................................................................21 
Use by Fund ....................................................................................................................................................21 
Input Requirements .........................................................................................................................................21 
[[NSCC]] Response .............................................................................................................................................21 
[[Dividend]] and Capital Gains Processing ...........................................................................................................22 
Purpose ...........................................................................................................................................................22 
Division of Information .....................................................................................................................................22 
Header Information ..........................................................................................................................................22 

---

## Page 4

Networking Technical Guide 
 
Revision History 4 
 
Detail Information ............................................................................................................................................22 
Use by Fund ....................................................................................................................................................22 
Input Requirements .........................................................................................................................................22 
[[NSCC]] Response .............................................................................................................................................23 
[[settlement]] .......................................................................................................................................................23 
Cash Dividends Subject to Withholding Process ............................................................................................23 
Year-End Processing ........................................................................................................................................24 
Purpose ...........................................................................................................................................................24 
Use by Fund ....................................................................................................................................................24 
Reallocation Categories ..................................................................................................................................25 
Input Requirements .........................................................................................................................................25 
[[NSCC]] Response .............................................................................................................................................25 
Chapter 2, Section D–System Processing by [[NSCC]] ........................................................................................ 26 
Overview ...........................................................................................................................................................26 
Activity Cash [[settlement]] ...................................................................................................................................26 
Purpose ...........................................................................................................................................................26 
Processing Activity ..........................................................................................................................................26 
Networking Activity [[settlement]] File .................................................................................................................26 
[[Dividend]] Cash [[settlement]] ................................................................................................................................26 
Purpose ...........................................................................................................................................................26 
Processing Dividends ......................................................................................................................................26 
[[Dividend]] [[settlement]] File .................................................................................................................................26 
Money [[settlement]] ...........................................................................................................................................26 
Input Acknowledgment Records .......................................................................................................................27 
Purpose ...........................................................................................................................................................27 
Input Record Types .........................................................................................................................................27 
Rejects.............................................................................................................................................................27 
Account Base Transaction File .........................................................................................................................27 
Purpose ...........................................................................................................................................................27 

---

## Page 5

Networking Technical Guide 
 
Revision History 5 
 
Use by Fund ....................................................................................................................................................28 
Use by [[NSCC]] ..................................................................................................................................................28 
Input Requirements .........................................................................................................................................28 
[[NSCC]] Response .............................................................................................................................................28 
Chapter 3–System Specifications and Codes ................................................................................................. 29 
Overview ...........................................................................................................................................................29 
In This Chapter ................................................................................................................................................29 
Chapter 3, Section A–Networking Matrix Levels ............................................................................................ 30 
Overview ...........................................................................................................................................................30 
Networking Matrix Level Descriptions...............................................................................................................30 
Purpose ...........................................................................................................................................................30 
Definition..........................................................................................................................................................30 
Description of Networking Matrix Levels .........................................................................................................30 
Shareholder Reporting Responsibility ..............................................................................................................31 
Reporting Responsibilities ...............................................................................................................................31 
Beneficial Shareholder Privileges with a Company ..........................................................................................32 
Beneficial Shareholder privilege table .............................................................................................................32 
Firm or Trust Company Capabilities-Activity ....................................................................................................33 
Purpose ...........................................................................................................................................................33 
Capabilities ......................................................................................................................................................33 
Firm or Trust Company Capabilities–Account Maintenance ............................................................................34 
[[Broker]] or Trust Company Account Maintenance Table ..................................................................................34 
[[Dividend]] Privileges ...........................................................................................................................................36 
[[Dividend]] Privilege Table..................................................................................................................................36 
Shareholder Privileges ......................................................................................................................................36 
Client Privileges Table .....................................................................................................................................36 
Chapter 3, Section B–Networking Codes ........................................................................................................ 38 
Overview ...........................................................................................................................................................38 
Networking State Codes ...................................................................................................................................38 

---

## Page 6

Networking Technical Guide 
 
Revision History 6 
 
Purpose ...........................................................................................................................................................38 
State Code List ................................................................................................................................................38 
Special Circumstances: ...................................................................................................................................38 
Networking Country Codes ...............................................................................................................................38 
Purpose ...........................................................................................................................................................38 
Country Code List ............................................................................................................................................38 
Networking Social Codes ..................................................................................................................................39 
Purpose ...........................................................................................................................................................39 
Social Code List ..............................................................................................................................................39 
Networking Reject Codes .................................................................................................................................39 
Purpose ...........................................................................................................................................................39 
Reject Code List ..............................................................................................................................................39 
Transaction Description Codes .........................................................................................................................39 
Purpose ...........................................................................................................................................................39 
Transaction Description Code List ..................................................................................................................40 
Discontinuance of Networking Alpha Codes ....................................................................................................40 
Recommended Best Practices ........................................................................................................................40 
Chapter 3, Section C–Trust Processing .......................................................................................................... 41 
Overview ...........................................................................................................................................................41 
Description ......................................................................................................................................................41 
Dual Accounts-Matrix Levels ...........................................................................................................................41 
Restrictions and Guidelines.............................................................................................................................41 
Chapter 3, Section D–Mass [[Broker]] to [[Broker]] ................................................................................................. 42 
Overview ...........................................................................................................................................................42 
Description ......................................................................................................................................................42 
Processing Steps ............................................................................................................................................42 
Chapter 3, Section E–Change in [[Broker]]/Dealer .............................................................................................. 44 
Overview ...........................................................................................................................................................44 
Description ......................................................................................................................................................44 

---

## Page 7

Networking Technical Guide 
 
Revision History 7 
 
Prerequisites ...................................................................................................................................................44 
Process............................................................................................................................................................44 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices ........................................... 50 
Background .......................................................................................................................................................50 
Systematic Trades ............................................................................................................................................50 
Initial vs. Subsequent Purchase .......................................................................................................................60 
Account Open Date...........................................................................................................................................60 
Chapter 4–Networking Record Layouts ........................................................................................................... 61 
Overview ...........................................................................................................................................................61 
How to Read a Networking Record Layout ......................................................................................................61 
Rules ...............................................................................................................................................................61 
Column Headings ............................................................................................................................................61 
Alphanumeric and Numeric Fields ..................................................................................................................62 
Required Fields ...............................................................................................................................................62 
Optional Fields ................................................................................................................................................62 
Date Format ....................................................................................................................................................62 
Networking Record Layouts ..............................................................................................................................62 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts .................................................. 63 
Field Descriptions ............................................................................................................................................63 
Chapter 5, Section B–Glossary of Terms ........................................................................................................ 76 
Terms and Definitions .......................................................................................................................................76 
 

---

## Page 8

Networking Technical Guide 
 
Revision History 8 
 
REVISION HISTORY 
Effective Date Note 
December 29, 2023 • Document refreshed due to rebranding.  
• Corrected B53 field reference to F53 field in Process section. 
December 15, 2022 Learning upgrade caused some link(s) to break. Links have been 
corrected. 
Effective Date: April 19, 2021 Removed all references to the Account Maintenance services (records 
F71-74). This product was decommissioned, effective April 19, 2021. 
May 29, 2020 Document refreshed due to rebranding; links repointed to Learning. 
 
Effective Date: April 6, 2020 Updated Chapter 3 Section E - Added additional language and updated 
verbiage regarding Firm to Fund Change From B/D requests. 
Effective Date: March 25, 2020 Updated Chapter 3 Section F – Updated verbiage regarding rule’s 
applicability date and references to the rule. 
Effective Date: May 15, 2017 Updated Chapter 3 Section F - Added additional language regarding 
systematic redemptions in percentages and [[shares]]. Updated rule’s 
applicability date. 
Effective Date: February 27, 2017 Please see Important Notice A8286, Dated January 3, 2017 
DoL [[Fiduciary]] Rule. Added Section F (Chapter 3) – DoL [[Fiduciary]] Rule 
Effective Date: September 26, 2016 Please see Important Notice a8159, Dated February 3, 2016 
 Money Market Reform 
Effective Date: February 29, 2016 Please see Important Notice a8107, October 27, 2015 
Completion of Alpha Code Elimination Changes noted in guide 
Effective Date: June 28, 2014 Please see Important Notice a7687, p&s7357 Dated Feb 24, 2014 
Effective Date: November 18, 2013 Please see Important Notices: 
a7665, p&s 7235 Dated July 3, 2013 
a7702, p&s 7272 Dated Sept. 16, 2013 
Effective Date: March 18, 2013 Please see Important Notices: 
a7472, p&s 7042 Dated August 16, 2012 and 
a7567, p&s 7137 Dated January 9, 2013 
Effective Date: April 23, 2012 Please see Important Notice a7355 & a7356 
 
 

---

## Page 9

Networking Technical Guide 
 
Introduction to Networking Technical Manual 9 
 
INTRODUCTION TO NETWORKING TECHNICAL MANUAL 
Networking System 
The Networking Manual has been designed to provide a detailed view of this service and its processing 
requirements. Use of this guide and the related information will be helpful to you as you build the Networking 
interface to [[NSCC]], as well as provide answers to your processing questions once you begin to utilize the 
service. 
When you have finished reviewing this, you should have a better understanding of: 
• The functionality of the system 
• The communication requirements 
• The processing capabilities of the service 
• Each Client’s role within the service 
• Data submission formats 
• Related Forms 
• Reject Codes 
• Frequently Asked Questions 
 
If you have any questions about this document, please contact our Wealth Management Services team at 212-
855-8877. 

---

## Page 10

Networking Technical Guide 
 
Chapter 1–Introduction to Networking 10 
 
CHAPTER 1–INTRODUCTION TO NETWORKING 
Overview 
Purpose of the Document 
The purpose of this document is to acquaint users with the capabilities of the Networking System and to 
provide record layouts and specifications for all input and output requirements.  
Definitions 
Terms used throughout this document are defined in the table below. 
Term Definition 
Firm [[NSCC]] Settling [[Member]], TPA [[Member]], and Fund [[Member]] which is limited to a 
[[Broker]]/dealer, bank, trust company or any other financial [[intermediary]]. 
Fund [[NSCC]] Fund [[Member]] capable of accepting mutual fund orders. 
Matrix Level Level of control the Firm wants to maintain on a sub-account. The matrix level 
selected by the Firm specifically determines the activities allowed between the 
customer and the Fund. The matrix level also determines the associated 
reporting responsibilities. 
Reference: For further information on Networking matrix levels, refer to 
Chapter 3 Section A, Networking Matrix Levels. 
[[NSCC]] National [[securities]] Clearing Corporation and its Networking System 
Clients Firms and Funds 
Sub-account Customer position in a specific security 
System The Networking System 
Day of Days [[NSCC]] Business days. (Networking is available 6 days of the week, Monday 
through Saturday.) 
Note: 
Throughout this document, references to “[[NSCC]] or Fund/SERV® providing output” mean that the System makes 
information in automated form available to Clients for their retrieval and use. 

---

## Page 11

Networking Technical Guide 
 
CHAPTER 2, SECTION A–ABOUT THE NETWORKING SYSTEM 11 
 
CHAPTER 2, SECTION A–ABOUT THE NETWORKING 
SYSTEM 
Overview 
Description 
Networking is the industry standard for the exchange of mutual fund customer account maintenance and 
reporting. The Networking system allows non-trade related client information to appear identically on the 
records of 
• Firms and Funds, or 
• Transfer agents for Firms and Funds. 
 
With Networking, Firms and Funds can exchange timely and accurate information about their customers i n a 
controlled environment. 
Purpose of the System 
[[NSCC]] developed the Networking system to allow Firms to accurately control and maintain street -name and 
customer-name accounts while eliminating the need for physical [[shares]]. The system supports book-share 
accounts. For an account to be “Networked,” Firms convert any physical [[shares]] to book -share positions, 
relieving Firms of the control, record-keeping and audit functions related to physical certificates. 
Who Can Use the System 
[[Institutions]] that have been accepted for membership in [[NSCC]] can utilize the system. This includes, but is not 
limited to: 
• Banks 
• Brokers 
• Dealers 
• [[Mutual Funds]] 
• Trust [[Companies]] 
• Financial service firms 
• Third party administrators 
• Insurance [[Companies]], and 
• Other financial intermediaries. 
 
 

---

## Page 12

Networking Technical Guide 
 
CHAPTER 2, SECTION A–ABOUT THE NETWORKING SYSTEM 12 
 
Benefits of the Networking System 
Networking is the industry standard for the streamlined exchange of customer account -level information, 
delivering efficiencies by securely automating a host of activity reporting including creating new accounts, 
account maintenance and transfers between [[DTCC]] clients such as funds and [[Broker]]/dealers.  
 
• Automates and standardizes account reports for uniform record layouts.  
• Reduces operating costs and enhances processing efficiencies. 
• Mitigates risk associated with error-prone, manual processes. 
• Eliminates the need for proprietary communication lines, faxes and phone connections.  
• Simplifies the [[settlement]] process for dividends and capital gains by calculating a single [[settlement]] 
figure for each client, every day. 
• Enhances reporting control with a choice of customer reporting levels to best match a firm’s business 
practices and customer service objectives. 
• Optimizes regulatory reporting and compliance regarding breakpoint calculations, frequent trading and 
short-term redemption fees. 
• Increases accuracy, speed and transparency to funds and firms in Omnibus relationships.   

---

## Page 13

Networking Technical Guide 
 
CHAPTER 2, SECTION A–ABOUT THE NETWORKING SYSTEM 13 
 
Pre-Conversion Processing 
Account Scrubbing Process 
Before Networking participation can begin, a critical, pre-conversion process known as “scrubbing” must be 
completed by the Firm. 
Scrubbing involves reconciling the Firm’s positions with the Fund’s positions to ensure that the Firm and the 
Fund have identical sub-account records in place. This is usually accomplished with the delivery of position 
files from the Fund to Firms. 
Determining Account Registration 
The Firm and the Fund must decide how the sub-accounts are to be registered. 
Example: The Firm and the Fund determine if the sub-accounts are to be registered: 
• in the customer’s name, or 
• in the name of the firm, for the benefit of the customer. 
After Scrubbing 
After scrubbing is completed, Firms and Funds can then begin to exchange fund information on a regular basis 
through Networking. 
Networking Primary System Functions 
Functionality 
Using one of the System’s components: Conversion Processing, Activity Reporting, Position Reporting, 
[[Dividend]] Processing or Year-End Processing, 
Firms can 
• Establish sub-accounts, 
• Transfer [[shares]] between accounts, and 
• Update sub-accounts (registration and account options), and 
 
Funds can 
• Report account activity 
• Update accounts (registration and account options) 
• Acknowledge firm account changes 
• Report [[Dividend]]/capital gain distribution on an account level 
• Report year-end tax information 
• Report account positions, and 
• Report current account data. 

---

## Page 14

Networking Technical Guide 
 
CHAPTER 2, SECTION A–ABOUT THE NETWORKING SYSTEM 14 
 
Conversion Processing 
Conversion processing allows Networking sub-accounts to be established and credited with [[shares]]. The 
information submitted to Networking is similar to the information submitted to Fund/SERV in the regist ration 
process. The conversion process also allows the Firm, when necessary, to credit the new sub- account with 
[[shares]]. The number of [[shares]] and the account numbers to be debited and credited are identified in the 
Conversion transaction. These transactions are then assigned a Control Number by [[NSCC]] and transmitted to 
the Fund for processing. The Fund provides confirmation, including a closing share balance, to the Firm 
through the system. 
Additionally, any updates to existing sub-account registrations (address changes, [[Dividend]] [[Option]] changes, 
etc.) are included in the conversion process. 
Activity Reporting 
Activity reporting allows all non-Fund/SERV sub-account activity, processed at the Fund, to be reported to the 
Firm; with this component, Funds inform Firms of changes in share balances of a Networking sub-account. 
Fund activities include direct purchases, systematic withdrawal transactions, pre- authorized check transactions 
and share adjustments. For any transaction involving [[shares]], a closing share balance is included as part of the 
transaction/record. In addition, certain activity at the Fund can be settled through [[NSCC]], specifically, Direct 
Redemptions and Systematic Withdrawals. 
Funds use the Activity stream when transmitting their Year-End tax information. Input records are sorted by 
security and by Firm. 
Position Reporting 
Position reporting allows the Fund to report to the Firm, on a schedule agreed upon by both, the closing 
balance for each sub-account as of a specific date. The Firm uses this file to reconcile sub-accounts and 
produce consolidated monthly statements. Input records are sorted by security and by Firm.  
[[Dividend]] Processing 
[[Dividend]] processing permits Funds or their agents to communicate [[Dividend]] and capital gain information to 
Firms. The system divides [[Dividend]] information into two categories. 
The first category contains information for each mutual fund security on which the [[Dividend]] is being paid and 
includes the: 
• Record date 
• Posting date 
• Payable date, and 
• Rate. 
 
The second category contains detailed sub-account information including: 
• The amount of the [[Dividend]] or capital gain 
• The reinvested share quantity (when applicable) 
• The closing share balance as a result of the [[Dividend]] payment/capital gain 
• Any withholding information. 

---

## Page 15

Networking Technical Guide 
 
CHAPTER 2, SECTION A–ABOUT THE NETWORKING SYSTEM 15 
 
Year-End processing 
Funds may pay several types of cash distributions during the year: 
• Dividends 
• Short-term capital gains, 
• Long-term capital gains and 
• Other capital gains (Gain on Collectables, Section 1202 Gain and Un-recaptured Section 1250 Gain). 
 
At the end of the year, a Fund may need to reclassify incorrectly reported cash distributions.  
Year-End processing allows Funds to report reallocated distribution summary information. Please note that 
Year-End records are sent in the Activity stream of Networking. 
Note: 
 Input records are sorted by security and by Firm number. 
Communicating with Networking 
Communication Options 
Networking accepts input from Firms and Funds through a communications link. Clients may communicate via 
connecting to [[DTCC]]’s SMART Network. For options, please contact our Wealth Management Services  team at 
212-855-8877.   
Processing Schedule 
Reference: For detailed information on processing times, Datatrak Sysids and Autoroute numbers please see 
the “Schedules” on the Mutual Fund Services home page on the Learning website (password required) 
https://dtcclearning.com/products-and-services/mutual-fund-services/schedules.html 
 
 

---

## Page 16

Networking Technical Guide 
 
Chapter 2, Section B–System Processing by the Firm 16 
 
CHAPTER 2, SECTION B–SYSTEM PROCESSING BY THE 
FIRM 
Overview 
Account Conversion, Update, and Transfer Reporting 
Purpose 
Firms use the account conversion feature to establish customer accounts as “Networked” on the Fund’s 
records, including: 
• Registration information 
• [[Dividend]]/withholding options, and 
• Update account registration data. 
 
In addition, Firms have transfer capability which is used to instruct Funds to move [[shares]] from one account, 
including the house account, to individual sub-accounts. 
Input Requirements 
Firms prepare a file consisting of: 
• a DataTrak Header record, 
• Conversion/Update Detail records (Record Types B50-B51), 
• Transfer records (Record Type B52), 
• a Conversion/Update Trailer record (Record Type B54*) and 
• a DataTrak Trailer record. 
 
*Record B54 can be used by a service bureau to separate each client they submit for. Individual clients will 
have only one, at the end of their detail records. 
Control Numbers 
[[NSCC]] generates a Control Number for all share transfers (Record Type B52). Control Numbers are used by 
Funds to acknowledge the original Firm-initiated transaction (using Record Type F53). 
Note: 
Firms may include their own unique Reference Numbers for Conversion/Update records (Record Types B50 & B51) based 
on a formula outlined in the section “Glossary of Terms” located in Chapter 5 of this document. 
Funds in turn, use the Reference Number, supplied by the Firm, when acknowledging the firm’s B50 & B51 
transactions (using Record Type 53). 

---

## Page 17

Networking Technical Guide 
 
Chapter 2, Section B–System Processing by the Firm 17 
 
Reminders 
[[NSCC]] produces Reminder records for any Transfers not acknowledged (Record Type N49).  
[[NSCC]] Response 
When processing is complete, [[NSCC]] sorts the file, before sending it out, by:  
• Recipient’s Clearing Settling Number, 
• Recipient Type, 
• Record Type, 
• Security Issue [[ID]], 
• Control Number, and 
• Sequence Number. 
 
[[NSCC]] sends the following to the Fund: 
• An AutoRoute Output Header record, if requested by client, 
• An Application (System) Output Header, 
• Detail Conversion/Update records (Record Types B50-B51), 
• Transfer transactions (Record Type B52), 
• An Application Trailer record (Record Type B54*), and 
• An optional Grand Total Trailer record (Record Type GT- for the entire file). 
 
[[NSCC]] sends the following to the originating Firm: 
• An AutoRoute Output Header record, if requested by client, 
• An Application (System) Output Header, 
• An Input Acknowledgment record (Record Type CN), 
• Any Rejected Account Conversion/Update records (Record Types B50 & B51)  
• All Transfer records (Record Type 52) with [[NSCC]] generated Control Numbers,  
• An Application Trailer record (Record Type 54*), and 
• An optional Grand Total Trailer record (Record Type GT- for the entire file). 
 
*Record B54 can be used by a service bureau to separate each client they submit for. Individual clients will 
have only one, at the end of their detail records. 

---

## Page 18

Networking Technical Guide 
 
Chapter 2, Section C–System Processing by the Fund 18 
 
CHAPTER 2, SECTION C–SYSTEM PROCESSING BY THE 
FUND 
Overview 
Account Conversion, Update, Transfer and Acknowledgement 
Reporting 
Purpose 
The Conversion feature allows Firms to establish Networking sub-accounts on the books of the Fund (B50) and 
credit them with [[shares]] (B52) and update their accounts (B51). For the Fund, this component provides the 
ability to acknowledge a Firm’s sub-account set-up, any account updates or share transfers using a Record 
Type F53, the Fund Acknowledgment record. Funds also use Conversion records to report any non-financial 
information that may have changed on a Firm’s sub-account, such as an address change (F51). 
Use by Fund 
Funds use this file to: 
• Advise the Firm of any account maintenance activity transacted directly between the shareholder and the 
Fund, and 
• Acknowledge share transfers, account set-ups or maintenance instructions from a Firm. 
 
Funds must acknowledge records containing an [[NSCC]] Control Number using a F53 record. [[NSCC]] provides a 
Control Number for all Transfer share records (B52) initiated by a Firm. 
[[NSCC]] issues Reminders (N49 - “Pending Fund Acknowledgment”) to the Firm and Fund for any Transfer (B52) 
which is not acknowledged by the Fund. Reminders are found in [[NSCC]]’s Networking output file at 1:00 PM 
daily. 
Funds may acknowledge records containing a Reference Number when that field is populated by a Firm on 
their account set-ups or updates (B50 & B51). 
Input Requirements 
Funds must transmit a file that consists of: 
• A DataTrak Header record 
• Any Update Detail records (Record Type F51) 
• Any Acknowledgment records for Transfers, Updates or Account Set-ups (Record Type F53) 
• A Conversion/Update Trailer record (Record Type 54), and 
• A DataTrak Trailer record. 
[[NSCC]] Response 

---

## Page 19

Networking Technical Guide 
 
Chapter 2, Section C–System Processing by the Fund 19 
 
When processing is complete, [[NSCC]] sorts the data by: 
• Recipient’s Clearing Settling Number 
• Recipient Type 
• Record Type 
• Security Issue [[ID]] 
• Control Number (if any) 
• Sequence Number 
 
The Firms receive: 
• AutoRoute Header record, if requested 
• Application (System) Header record 
• Reminder records (Record Type N49) 
• Detail transaction records (in Record Type order, F51 & F53) 
• Application Trailer record (Record Type 54) 
• Optional Grand Total record (Record Type GT) 
 
Funds that originate these files receive: 
• AutoRoute Header record, if requested 
• Application (System) Header record 
• Reminder records (Record Type N49) 
• Input Acknowledgment (Record Type CN) record 
• Rejected transactions (Record Types F51 & F53) 
• Application Trailer record (Record Type 54) 
• Optional Grand Total record (Record Type GT) 
 
Activity Processing 
Purpose 
The Activity component of Networking allows the Fund to report all non-Fund/SERV sub-account activity 
(occurring at the fund) to the firm. This facility provides Firms with share balance changes whenever they occur 
at the Fund. 
Some direct Fund activities reported include: 
• Direct purchases 
• Systematic withdrawal transactions (SWP)** 

---

## Page 20

Networking Technical Guide 
 
Chapter 2, Section C–System Processing by the Fund 20 
 
• Pre-authorized check transactions (PAC) 
• Share adjustments, and 
• Direct liquidations**. 
Use by Fund 
The Activity file is used by Funds to inform the Firms of all non-Fund/SERV information, transacted directly 
between the shareholder and the Fund.  A Fund sends an Activity record whenever there is a change 
(unrelated to a [[Dividend]] payment) to the share balance on a shareholder’s account.  
Input Requirements 
The Transaction Type is used to describe a type of Activity. 
Files consist of: 
• DataTrak Header record 
• Year-End records (Record Type 45***) 
• Activity Detail record (Record Type 55) in sequence order for each transaction  
• Activity/Balance Trailer record (Record 56) 
• DataTrak Trailer record 
[[NSCC]] Response 
After editing, [[NSCC]] prepares output files for distribution to Firms. 
Firms receive, in ascending contra-side (Fund) order: 
• AutoRoute Header record, if requested 
• Application (System) Header record 
• Accepted Year-End records (Record Type 45***) 
• Accepted Activity detail records (Record Type 55) 
• Activity Trailer record (Record Type 56) 
• Optional Grand Total record (Record Type GT) 
 
Funds receive, in the following order: 
• AutoRoute Header record, if requested 
• Application (System) Header record 
• Input Acknowledgment record (Record Type AC) 
• Rejected Year-End records (Record Type 45***) 
• Rejected Detail records (Record Type 55) 
• Activity Trailer record (Record Type 56) 
• Optional Grand Total record (Record Type GT) 

---

## Page 21

Networking Technical Guide 
 
Chapter 2, Section C–System Processing by the Fund 21 
 
 
*Since Fund/SERV activity may result in a change to a sub-account’s share balance, Funds must send a 
closing balance record (Record Type 55 -Transaction Type 50). 
**Direct Liquidations and SWP transactions are special since they can settle using the Networking system. For 
any transaction involving [[shares]], a closing share balance is included as part of the transaction. Transaction 
Type 50 indicates the closing balance on an account as a result of the Activity.  
***Year-End Tax Reporting is related through the Activity stream as well. Input records should be sorted by 
Security Issue [[ID]] and firm. 
Position Processing 
Purpose 
Position processing allows the Fund to report to the Firm, on a schedule agreed upon by both, the closing 
balance for each sub-account as of a specific date. The Firm uses this file to reconcile its sub-accounts and 
produce consolidated monthly statements. 
 
Use by Fund 
The Position file is used by Funds to report account balances to Firms on a periodic or “on request” basis. 
Firms are charged for Position files received based on a fee schedule filed by the [[NSCC]] with the [[SEC]]. Fees 
may change periodically. 
Reference: To obtain the most recent copy of the Networking fees, please reference “Fee Schedule for Mutual 
Fund Services” on the [[DTCC]] website at https://www.[[DTCC]].com/wealth-management-services/mutual-fund-
services/mutual-funds-client-public-documentation 
If present, book-share and physical share positions are reported separately for each sub-account. It is the 
responsibility of the Fund and Firm to arrange a transmission schedule for Position files.  
Input Requirements 
Position files are sorted by the Funds in Security [[ID]] and firm order. For example: SECURITY ISSUE [[ID]] 1: Firm 
1, Firm 2, Firm 3, then SECURITY ISSUE [[ID]] 2: Firm 1, Firm 2. 
Each file consists of: 
• DataTrak Header record 
• Position Header record (Record Type 57) 
• Position Detail records (Record Type 58) 
• Position Trailer record (Record Type 59) 
• Required Grand Total Trailer record (Record Type 60) that includes the total of all records submitted as 
part of the file 
• DataTrak Trailer record 
[[NSCC]] Response 

---

## Page 22

Networking Technical Guide 
 
Chapter 2, Section C–System Processing by the Fund 22 
 
All records must pass [[NSCC]]’s edit criteria. Accepted records are transmitted to the recipient, sorted by 
receiver, Security number and Record Type. 
An Input Acknowledgment record (Record Type NPO), any Rejected transactions and the appropriate Trailer 
records are sent back to the originator. 
[[Dividend]] and Capital Gains Processing 
Purpose 
Permits Funds or their agents to communicate distribution information to Firms.  
Division of Information 
The system divides distribution data into two categories: 
• Header information, and 
• D etail information. 
Header Information 
The Header contains information for each Security Issue [[ID]] on which the distribution is being paid, and 
includes: 
• Record date 
• Posting date 
• Payable date 
• Rate 
Detail Information 
The Detail contains sub-account information including 
• The amount of the distribution 
• Reinvested share quantity (when applicable) 
• The closing share balance as a result of the distribution payment 
• Any withholding information. 
Note: 
Input records must be sorted by security and by Firm. 
Use by Fund 
The distribution file is used by Funds to report distributions of dividends and capital gains on the sub- account 
level. Funds must also provide closing share balances each time they report distributions.  
Input Requirements 

---

## Page 23

Networking Technical Guide 
 
Chapter 2, Section C–System Processing by the Fund 23 
 
Funds must transmit a file that consists of: 
• DataTrak Header record, 
• [[Dividend]] or Capital Gain Header record (Record Types 61-62), 
• Detail Distribution records (Record Types 63-67), 
• Two (2) Trailer records (Record Types 68-69), 
• Grand Total Trailer record (Record Types 70), and 
• DataTrak Trailer record. 
 
Note: 
 All records are required to be in security/Firm order. 
 
Example below depicts record order when both a [[Dividend]] and capital gain are being distributed by a 
Fund: 
Header record 61 (SECURITY ISSUE [[ID]] 1/Firm1) with multiple Records 63-67, followed by Trailers 68 and 69, 
then Header record 62 (SECURITY ISSUE [[ID]] 1/Firm 1) with multiple Records 63- 67, again with Trailers 68 and 
69; With the file then having a Grand Total record 70. 
With 5 kinds of Capital Gains, Record Type 62 can be repeated multiple times, each containing several detail 
records each. 
[[NSCC]] Response 
After editing, [[NSCC]] prepares output files for Firms. Firms receive: 
• AutoRoute Header record, if requested, 
• Application (System) Header record, 
• [[Dividend]]/Capital Gain Header record (Record Types 61-62), 
• Detail records for each category (Record Types 63-67), 
• Two (2) Detail Trailer records (Record Types 68 and 69), and 
• Grand Total Trailer (Record Type 70) record. 
Notes: 
On output to the firm, the [[Dividend]] records are sorted by Firm and security. 
[[NSCC]] will transmit an Input Acknowledgment record (Record Type DV) and any Rejected transactions along with 
appropriate Trailers to the Fund. 
[[settlement]] 
[[settlement]] of Cash [[Dividend]]/Capital Gains occur in the [[NSCC]] [[settlement]] System.  Distribution information 
reported to [[NSCC]] and designated “Cash to Firm” or “Cash to Trust” will be settled through [[NSCC]].  
Cash Dividends Subject to Withholding Process 

---

## Page 24

Networking Technical Guide 
 
Chapter 2, Section C–System Processing by the Fund 24 
 
1. Fund Submits Networking [[Dividend]] Record Type F64. 
o the cash [[Dividend]] amount should be net of withholding 
o any withholding should be declared and marked as TEFRA, NRA or FATCA 
2. Networking looks at whether the Cash Disbursement Indicator is 1 (Cash to [[Broker]]) or 6 (Cash to Trust). If 
yes, then the cash [[Dividend]] amount will settle via Networking. If not, it will settle via the selected [[Option]]. 
3. Networking looks at the Networking Control Indicator. If Networking Level = 3, then the withholding 
amount is settled via Networking. This applies even though the Cash Disbursement Indicator is not 1 or 6 
because the [[Broker]]/dealer must directly receive the withholding amount and declare it on the tax records.  
4. For NRA or TEFRA Withholding, if Networking Level = 3, then Networking looks at the Withholding 
Indicators. If NRA/TEFRA Withholding Indicator is 1 (TEFRA), then the amount entered in the Withholding 
Amount field settles as TEFRA. If the Withholding Indicator is 2 (NRA), then the amount entered in the 
Withholding Amount field settles as NRA. 
5. For FATCA Withholding, if Networking Level = 3, then Networking looks at the FATCA Withholding 
Amount field. If the FATCA Withholding Amount field is populated with an amount > 0, then the amount 
settles as FATCA. 
6. When Networking creates the Networking [[settlement]] file, it will create N80 for cash dividends that meet 
the conditions on Line 2 and mark the [[settlement]] Indicator as D ([[Dividend]] [[settlement]]) or S (Spillover 
Dividends) depending on Spillover Dividends Indicator in the header record (61 or 62). Networking will 
also create a separate N80 for withholding amounts that meet the conditions on Line 3, 4 and 5. There will 
be separate N80 records for [[settlement]] Indicator T (TEFRA Withholding), N (NRA Withholding) and F 
(FATCA Withholding). 
Note: 
N80 records are created per group (record combinations of header, detail and trailer). There may be up to four N80 records 
per group: one for D ([[Dividend]] [[settlement]]) or S (Spillover [[Dividend]]), one for T (TEFRA), one for N (NRA) and one for F 
(FATCA). 
Year-End Processing 
Purpose 
Year-End processing allows Funds to report any reallocated distribution summary information. Distributions are 
cash payments such as dividends and capital gains. 
Example of a reallocation: Re-classifying a short-term capital gain as a long-term capital gain would be an 
example of a reallocation. 
Use by Fund 
Funds use Year-End processing to report reallocated distribution summary information. The reports are sorted 
by security and by Firm. They include: 
• Reallocation amounts 
• Fees 
• Spill-over distributions 
 

---

## Page 25

Networking Technical Guide 
 
Chapter 2, Section C–System Processing by the Fund 25 
 
Reallocation Categories 
Categories of reallocation include: 
• Non-taxable distributions 
• Short term capital gains 
• Long term capital gains 
• Mid-term capital gains 
• Dividends 
• Return of capital (capital surplus) 
• Taxable distributions 
Input Requirements 
Year-End records are submitted to [[NSCC]] through the Activity component stream. Funds may submit this 
information at any time. Each file consists of one security per Firm. The Year-End records will be routed to the 
designated Firm as part of the Activity file. 
[[NSCC]] Response 
Year-End records (Record Type 45) are sorted along with Activity records (Record Type 55). 
Note: 
Each firm receives an Activity file which consists of all Year-End records, followed by all Activity records. The Activity Trailer 
record is the last record of the file. The Trailer is used for file control purposes and has a field for Total Number of Year-End 
Transactions. The Total Number of Records field includes the number of Year-End records and Activity records transmitted. 
Reference: See Activity Processing in this document. 

---

## Page 26

Networking Technical Guide 
 
Chapter 2, Section D–System Processing by [[NSCC]] 26 
 
CHAPTER 2, SECTION D–SYSTEM PROCESSING BY 
[[NSCC]] 
Overview 
Activity Cash [[settlement]] 
Purpose 
To provide for the net [[settlement]] of certain activity through Networking, specifically Systematic Withdrawal 
Plans (SWP) and Direct Redemptions. 
Processing Activity 
All SWPs and Direct Redemptions (Transaction Types 14 and 02) marked with a Cash Disbursement Indicator 
of zero (where 0=Settling through the [[NSCC]]), will result in an Activity [[settlement]] file. 
Networking Activity [[settlement]] File 
Cash [[settlement]] of SWPs and Direct Redemptions will be passed on to the [[NSCC]] Money [[settlement]] System 
for netting with other [[NSCC]] [[obligations]]. 
[[Dividend]] Cash [[settlement]] 
Purpose 
Provides information to the firms about their cash distributions. 
Processing Dividends 
All Networking [[Dividend]] files designated as “Cash to Firm” or “Cash to Trust” will be processed through [[NSCC]] 
Money [[settlement]]. 
All cash account dividends are reported as the net amount. All reinvest account div idends are reported as the 
gross amount. For matrix level three, the TEFRA withholding and NRA accounts are identified on the 
[[settlement]] summary file. 
[[Dividend]] [[settlement]] File 
The [[Dividend]] [[settlement]] file will be available the day before the Payable Date, at approximately 6 a.m. In 
addition, [[Dividend]] files received on or after Payable Date will be reported on the Networking [[settlement]] 
summary file on the day that the files are received, or in the case of a non-[[NSCC]] [[settlement]] Date (Federal 
holiday), the next available [[settlement]] Date, for [[settlement]] that day. For these [[Dividend]] updates, the Payable 
Date and [[settlement]] Date may be different. 
Money [[settlement]] 

---

## Page 27

Networking Technical Guide 
 
Chapter 2, Section D–System Processing by [[NSCC]] 27 
 
Each day, [[NSCC]] makes available money [[settlement]] figures.   WMS mutual fund figures can be made availabl e 
on [[DTCC]]’s [[settlement]] Web System at approximately 12:00 pm ET each business day.   Firms who [[DO]] not have 
access to [[DTCC]]’s [[settlement]] Web (such as Fund/SERV Only [[Broker]]/Dealers or [[Asset]] Managers) can receive 
their mutual fund [[settlement]] obligation within an MRO (Machine Readable Output) file ( 02132518 file).  Firms 
have all their [[obligations]] netted to one figure for payment (debit or credit) in Fed Funds each day.  
 
The Money [[settlement]] file contains information about [[Dividend]] payment including:  
• All [[Dividend]] files received from Funds on or one day before Payable Date (code 40). These amounts were 
previously summarized on the Networking [[settlement]] Summary file sent to Funds and Firms one day prior 
to their Payable Date. 
• All [[Dividend]] files received from Funds on Payable Date or later (code 41). These amounts are 
summarized on the Networking [[settlement]] Summary file for [[settlement]] the same day.  
• As a result of [[Dividend]] corrections and reversals, Funds’ [[Dividend]] [[settlement]] figures may be a credit. All 
credits to Funds will be netted with Funds’ other mutual fund [[settlement]] figures.  In the event a Firm 
disagrees with a correction that results in a debit, [[NSCC]] will make a best effort to reverse the debit 
provided Wealth Management Services (212-855-8877) is contacted prior to end of day [[settlement]] for the 
debit transaction. 
 
Input Acknowledgment Records 
Purpose 
The Input Acknowledgment is an affirmation from [[NSCC]] of a Firm’s or Fund’s Networking transmission. 
Records coming into [[NSCC]] will produce an output file directed back to the originator for each application 
submitted. These records indicate the type of input file acknowledged. A total record count of the input file 
received and the date the file was processed are included. 
Input Record Types 
The input record types are: 
• AC-Activity 
• CN-Conversion 
• DV-[[Dividend]], and 
• PO-Position. 
Rejects 
This file contains any rejects detected from the DataTrak system upon input. 
 
Account Base Transaction File 
Purpose 

---

## Page 28

Networking Technical Guide 
 
Chapter 2, Section D–System Processing by [[NSCC]] 28 
 
This file is used by [[NSCC]] to gain a more accurate count of how many Networking sub- accounts are supported 
by each Firm on the books of the Funds. This is an optional file that is submitted by Funds on a monthly 
basis. The file is used by the [[NSCC]] in conjunction with other information, when determining monthly 
Networking charges. 
Use by Fund 
Funds use the Account Base Transaction file to report the total number of sub-accounts supported by the 
Networking System for each of its Firms or security relationships. 
Use by [[NSCC]] 
[[NSCC]] uses this information: 
• To verify the monthly activity captured from the Position and [[Dividend]] files, and 
• For Networking billing purposes. 
Input Requirements 
The file consists of the account base transaction records, one for each Firm or security relationship. The 
records identify the: 
• Fund number 
• Firm number 
• Security number 
• Total number of Networking accounts supported by the System. 
Note: 
This file must be submitted by Funds between 4 a.m. and 9 a.m. on the last business day of each month. 
[[NSCC]] Response 
[[NSCC]] does not create any output files from this data. 

---

## Page 29

Networking Technical Guide 
 
Chapter 3–System Specifications and Codes 29 
 
CHAPTER 3–SYSTEM SPECIFICATIONS AND CODES 
Overview 
In This Chapter 
This chapter contains the following topics: 
• Networking Matrix Levels 
• Networking Codes 
• Trust Processing 
• Mass [[Broker]] to [[Broker]] Conversions 
• Change in [[Broker]]/Dealer 

---

## Page 30

Networking Technical Guide 
 
Chapter 3, Section A–Networking Matrix Levels 30 
 
CHAPTER 3, SECTION A–NETWORKING MATRIX 
LEVELS 
Overview 
Networking Matrix Level Descriptions 
Purpose 
Networking offers three levels of reporting, each one referencing different levels of account responsibilities for 
Firms and Funds. Each matrix level: 
• Provides Firms with the flexibility to select options consistent with their business philosophy . 
• Identifies the 
o Reporting responsibilities of the Firm and Fund with regard to each sub-account 
o Processing capabilities the Fund and Firm have in supporting the exchange of information for those 
sub-accounts 
Note: 
Levels of responsibility and user privileges can be changed depending on the specific needs of the Firms and Fund 
[[Companies]]. 
Definition 
The matrix level is the level of control on a sub-account provided to a Firm or Fund using Networking. The 
matrix level chosen by the Firm determines the activity allowed between the shareholder and the Fund.  
There are three matrix levels: 
• Level Zero = Non-Networked Account or a Networked Trust Account when used in conjunction with a 
Trust Membership Indicator 
• Level Three = Firm Controlled Account, and 
• Level Four = Fund Controlled Account 
Description of Networking Matrix Levels 
The table below describes each of the three matrix levels of Networking. 
Networking Level Name Description 
0 (zero) Non-Networked Account For most Firms, Level 0 means non-Networked. 
Exception: A Networked Trust Account is considered Level 
0 if the Membership Indicator denotes a Trust. 
3 (three) Firm Controlled Account Firms maintain maximum control over the mutual fund 
assets in a customer’s account including: 

---

## Page 31

Networking Technical Guide 
 
Chapter 3, Section A–Networking Matrix Levels 31 
 
Networking Level Name Description 
• all customer contact 
• orders 
• customer statements, and 
• tax reporting 
Note: 
Customers [[DO]] not deal directly with the fund. 
4 (four) Fund Controlled Account Firms allow the fund to maintain control over the mutual fund 
assets in a shareholder’s account. 
Firms process customer’s orders, but the Fund provides all 
other services for the shareholder including all accounting 
and tax reporting. 
Shareholders can deal with either the Firm or the Fund. 
Trust Networked Account Trust Company Controlled 
Account 
Trust Company maintains maximum control over the mutual 
fund assets in a customer’s account including: 
• all customer contact 
• orders 
• customer statements, and 
• tax reporting 
Note: 
Customers [[DO]] not deal directly with the fund. 
 
 
Shareholder Reporting Responsibility 
Reporting Responsibilities 
The table below illustrates who is responsible for: 
• Producing confirmations 
• Preparing monthly and quarterly statements, and 
• Tax reporting for investors. 
 
Reporting Responsibility Level Three Level Four Trust Networked** 
Confirm (Fund/SERV Trades) Firm Fund Trust Company 
Confirm (Non-Fund/SERV) Firm Fund Trust Company 
Monthly Statements Firm Fund Trust Company 

---

## Page 32

Networking Technical Guide 
 
Chapter 3, Section A–Networking Matrix Levels 32 
 
Reporting Responsibility Level Three Level Four Trust Networked** 
Quarterly Statements Firm Fund Trust Company 
Year-End Statements Firm Fund Trust Company 
1099D Firm Fund Trust Company 
1099B (Wire Orders) Firm Fund Trust Company 
1099B (Direct Liquidations) Firm Fund Trust Company 
1099 R/W2P (When Applicable) Custodian/ Trustee Custodian/ Trustee Trust Company 
5498 (When Applicable) Custodian/ Trustee Custodian/ Trustee Trust Company 
1042S Firm Fund Trust Company 
Proxies Firm/ Fund Fund Trust Company 
Interested Party Mailings Firm Fund Trust Company 
 
Custodian is defined as the financial institution acting as the caretaker for a mutual fund’s assets.  
*Direct Liquidations are not allowed. 
** Trust Networked accounts at the fund should not be subject to withholding. If withholding is appropriate, it 
should be applied by the trust on the trust's record-keeping system. The trust is responsible for filing and 
reporting. 
Note: 
The tables found in this chapter should be used as a guideline. They are not a requirement of [[NSCC]]. They are the 
recommendations set forth by the clients of the Networking system themselves. 
Beneficial Shareholder Privileges with a Company 
Beneficial Shareholder privilege table 
The table below illustrates the shareholder privileges that are available for the various Networking levels.  
Note: 
The beneficial shareholder does not refer to the Trust Company in this instance but the clients of the Trust Company. 
 
Beneficial Shareholder 
Privileges with Fund 
Level Three Level Four Trust Networked 
** 
Direct Purchases No Yes No 
Direct Liquidations No Yes No 

---

## Page 33

Networking Technical Guide 
 
Chapter 3, Section A–Networking Matrix Levels 33 
 
Beneficial Shareholder 
Privileges with Fund 
Level Three Level Four Trust Networked 
** 
Direct Exchanges No Yes No 
Direct Transfers No Yes No 
Check Redemptions No Yes No 
Systematic Withdrawals No* Yes No* 
Pre-authorized Checks No Yes No 
Dealer of Record Changes No Yes No 
Account Executive Changes No Yes No 
[[Dividend]] [[Option]] Changes No Yes No 
Address Changes No Yes No 
Payee Address Changes No Yes No 
 
* Yes, if “Cash to Firm/Cash to Trust”. 
** For Trust Networked Accounts “No” means that only the Trust Company can process the privileges listed.  
Firm or Trust Company Capabilities-Activity 
Purpose 
This table illustrates the [[BASIC]] functions that Firms or Trust [[Companies]] (for Trust Networked Accounts) can and 
cannot [[DO]] under the various levels of Networking. These functions include: 
• Purchases 
• Liquidations 
• Exchanges, and 
• Transfers 
Capabilities 
Firm or Trust Company (for Trust Networked Accounts) capabilities are summarized in the tables below.  
 
Note: If account is trust networked, only the Trust Company should submit the below listed transactions. 

---

## Page 34

Networking Technical Guide 
 
Chapter 3, Section A–Networking Matrix Levels 34 
 
Function Type Level 3 Level 4 Trust Networked 
Purchases Direct with Fund No Yes Yes 
 Fund/SERV Yes Yes Yes 
Liquidations Direct with Fund No Yes Yes 
 Fund/SERV Yes Yes Yes 
Exchanges Direct with Fund No Yes Yes 
 Fund/SERV Yes Yes Yes 
Transfers Direct with Fund No Yes Yes 
 Fund/SERV Yes Yes Yes 
 
 
Firm or Trust Company Capabilities–Account Maintenance 
[[Broker]] or Trust Company Account Maintenance Table 
There are several non-trade related functions in Networking. The table illustrates which of these non- trade 
related functions Firms can perform under the various levels of Networking. These include:  
• Dealer of record changes 
• Account executive changes 
• [[Dividend]] [[Option]] changes 
• Address changes, and 
• Payee address changes. 
 
Function Type Level 3 Level 4 Trust 
Networked 
Dealer of Record Changes Firm through Networking No Yes No 
 Trust Company through Networking N/A No Yes 
 Firm to Fund Direct No Yes No 
 Trust Company to Fund Direct N/A No Yes 
 Fund through Networking No Yes Yes* 
Account Executive Changes Firm through Networking Yes Yes Yes 

---

## Page 35

Networking Technical Guide 
 
Chapter 3, Section A–Networking Matrix Levels 35 
 
Function Type Level 3 Level 4 Trust 
Networked 
 Trust Company through Networking N/A No Yes 
 Firm to Fund Direct No Yes Yes 
 Trust Company to Fund Direct N/A No Yes 
 Fund through Networking No Yes Yes* 
[[Dividend]] [[Option]] Changes Firm through Networking Yes Yes No 
 Trust Company through Networking N/A No Yes 
 Firm to Fund Direct No Yes No 
 Trust Company to Fund Direct N/A No Yes 
 Fund through Networking No Yes No 
Address Changes Firm through Networking Yes Yes No 
 Trust Company through Networking N/A No Yes 
 Firm to Fund Direct No Yes No 
 Trust Company to Fund Direct N/A No Yes 
 Fund through Networking No Yes No 
Payee address Change Firm through Networking Yes Yes No 
 Trust Company through Networking N/A No Yes 
 Firm to Fund Direct No Yes No 
 Trust Company to Fund Direct N/A No Yes 
 Fund through Networking No Yes No 
Mass Dealer Change (branch, 
account executive) 
Fund through Networking Yes Yes Yes* 
 
*Notification of a change made to the dealer/branch/representative information on a Trust Networked account 
by the Fund must be sent to the Trust via an F51 Fund Acknowledgement 
 
 

---

## Page 36

Networking Technical Guide 
 
Chapter 3, Section A–Networking Matrix Levels 36 
 
[[Dividend]] Privileges 
[[Dividend]] Privilege Table 
The table below indicates the [[Dividend]] privileges available to the shareholder under the various Networking 
levels. 
Note: 
Shareholder in this instance does not mean the Trust Company but its clients. 
Privilege Level Three Level Four Trust Networked 
Cash to Firm Yes Yes No 
Cash to Trust Yes Yes Yes 
Cash to Shareholder No Yes No 
Cash to Payable Party Yes Yes Yes 
Cross Fund Re-Invest Yes Yes Yes 
 
Shareholder Privileges 
Client Privileges Table 
The table below indicates the availability of the privileges shareholders have under the various Networking 
levels. 
Note: 
Shareholder in this instance refers to the [[Registered Owner]] of the account [[shares]]. This may or may not be the Trust 
Company authorized to trade on the account. 
Shareholder Privileges with Fund Level Three** Level Four Trust Networked 
Direct Purchases Yes Yes Yes 
Direct Liquidations Yes Yes Yes* 
Direct Exchanges Yes Yes Yes* 
Direct Transfers Yes Yes Yes* 
Check Redemptions Yes Yes Yes* 
Systematic Withdrawals Yes*** Yes Yes* 
Pre-authorized Checks Yes Yes Yes* 

---

## Page 37

Networking Technical Guide 
 
Chapter 3, Section A–Networking Matrix Levels 37 
 
Shareholder Privileges with Fund Level Three** Level Four Trust Networked 
Dealer of Record Changes Yes Yes Yes 
Account Executive Changes Yes Yes Yes 
[[Dividend]] [[Option]] Changes Yes Yes Yes* 
Address Changes Yes Yes Yes* 
Payee Address Changes Yes Yes Yes* 
 
*Only the Trust Company can process the privileges listed directly with the fund.  
** Yes, if requested by the [[Broker]]/dealer. 
*** Yes, if “Cash to Firm/Cash to Trust” and requested by the [[Broker]]/Dealer.  
Caution: Whenever there is a change in matrix levels, it carries with it the loss of all privileges associated with 
the prior matrix level, and gains of all privileges associated with the new matrix level. 

---

## Page 38

Networking Technical Guide 
 
Chapter 3, Section B–Networking Codes 38 
 
CHAPTER 3, SECTION B–NETWORKING CODES 
Overview 
Networking State Codes 
Purpose 
Clients should use this table to find the appropriate code to use for the State of Sale field.  
State Code List 
The States Codes are used to assist in the monitoring of “Blue Sky” laws. Clients should use this table to find 
the appropriate code to use for the State of Sale Field. 
Reference: Please see ‘State Codes’ on the Mutual Fund Services home page on the Learning site 
https://dtcclearning.com/documents/mutual-fund-services-1/mfs-cross-product/codes-8/2239-state-
codes/file.html 
Special Circumstances: 
The following countries are generally considered domestic and use the U.S. postal abbreviation (State Code).  
Non-resident alien (NRA) tax withholding will not be imposed for these countries unless the shareholder 
provides a W-8 certifying foreign citizenship of that country (e.g., other than U.S. citizenship).  
Note: 
If foreign citizenship is certified for one of these countries, the code for foreign resident should be used and the applicable 
NRA tax withheld. 
Country Code (U.S. Citizen) Code (Foreign Resident) 
Guam GU GQ 
Northern Mariana Islands MP CQ 
Puerto Rico PR RQ 
Virgin Islands (US) VI VQ 
Networking Country Codes 
Purpose 
Clients should use this table when specifying the non-US citizenship of their client for determining the 
appropriate taxes. 
Country Code List 

---

## Page 39

Networking Technical Guide 
 
Chapter 3, Section B–Networking Codes 39 
 
Country Codes are used to qualify a customer’s country of origin. Non-resident alien (NRA) tax rates are based 
on these country codes. 
Reference: Please see ‘Country Codes’ under the documentation section for [[Mutual Funds]] on the Learning site 
https://dtcclearning.com/documents/mutual-fund-services-1/mfs-cross-product/codes-8/2242-irs-country-
codes/file.html  
 
Networking Social Codes 
Purpose 
These codes are used by the funds to categorize the type of account being established. 
Social Code List 
Firms may use the following Social Codes to categorize the type of accounting methods that they want to 
establish. 
Reference: You can find the Social Code list under “Codes” on the Mutual Fund Services home page, on the 
Learning site https://dtcclearning.com/documents/mutual-fund-services-1/mfs-cross-product/codes-8/2498-
social-codes/file.html 
Networking Reject Codes 
Purpose 
Reject codes are used by [[NSCC]] for transactions that [[DO]] not meet editing criteria assigned as required for the 
transactions. 
Reject Code List 
For transactions that [[DO]] not meet the required editing criteria, Networking reject codes are used by [[NSCC]]. In 
addition, these reject codes are also used by the [[DTCC]] Payment aXis service. 
Reference: For the list of Reject Codes, please see ‘Networking and [[DTCC]] Payment aXis Reject Codes” 
under the Reject Codes section for [[Mutual Funds]] on the Learning site 
https://dtcclearning.com/documents/mutual-fund-services-1/networking/codes-3/reject-codes-1/1658-
networking-and-[[DTCC]]-payment-axis-rejectcodes/file.html 
 
 
 
 
Transaction Description Codes 
Purpose 

---

## Page 40

Networking Technical Guide 
 
Chapter 3, Section B–Networking Codes 40 
 
Fund may use acceptable Transaction Description Codes to identify an activity which took place and affected a 
shareholder's position at the Fund. These codes are used in lieu of certain transaction codes on t he 
Networking Activity record and represent sub-categories of those transactions. 
Example: Transaction Code 01 is used when reporting a Direct Purchase at the Fund. If the fund wanted to be 
more specific about the type of Direct Purchase, they could use one of the alpha codes starting with the letter 
"A"*. 
Note: 
The reason the letter "A" is used is because it corresponds to the first letter of the alphabet and the Transaction Code for a 
Direct Purchase is "01". Alpha Codes beginning with the letter "B", the second letter of the alphabet, correspond to 
Transaction Code "02", Direct Redemptions. 
The fund would place the letter "A1" in the Transaction Code field of the Activity Detail record (Record Type 55) 
for a Direct Purchase as a result of a Payroll Deduction. 
Transaction Description Code List 
The “Networking Transaction Description Codes” list is available on Mutual Fund Services home page under 
“Codes” https://dtcclearning.com/documents/mutual-fund-services-1/networking/codes-3/1663-networking-
transaction-codes/file.html 
 
Discontinuance of Networking Alpha Codes 
Prior to July 28, 2014, funds and firms that subscribed to Networking services were issued a two- byte Alpha 
Code as a unique identifier. The number of available unassigned Networking Alpha Codes diminished over 
time, and the decision was made to discontinue issuing Alpha Codes (see Important Notice a7687). 
As a result, on July 28, 2014, all “Firm Alpha Code” and “Fund Alpha Code” fields were modified to filler space. 
In addition, the Networking Reference Number algorithm AAJJJ999999 was modified to JJJYXXXXXXX on the 
Networking Account Conversion/Update & Transfer/Acknowledgement (A/B/T50, A/B/T/F51 A/B/T52 and F53) 
records. 
In order to allow sufficient time for clients to update their systems, a twelve-month grace period was granted 
during which [[NSCC]] would not validate the Reference Number format. The grace period expired, and effective 
February 29, 2016 [[NSCC]] began enforcing the revised Reference Number format ( JJJYXXXXXXX). See 
Important Notice a8107 http://www.[[DTCC]].com/~/media/Files/pdf/2015/10/27/a8107.pdf  
Recommended Best Practices  
Reference Number 
To encourage uniqueness of the Reference Number, clients are advised to use a combination of fields: 
“Reference Number” + “[[participant]] Number” + “Record Number”. 
Former Alpha Code fields 
The former alpha code fields were modified to filler space. [[NSCC]] will not edit against these fields. The best 
practice is to NOT populate data in these fields. For a complete list of impacted fields and records, please refer 
to Important Notice a7687. 

---

## Page 41

Networking Technical Guide 
 
Chapter 3, Section C–Trust Processing 41 
 
CHAPTER 3, SECTION C–TRUST PROCESSING 
Overview 
Description 
Trusts and trust [[Companies]] may participate in Networking. A Membership Identifier of “01” indicates a Trust 
[[Member]]. This indicator is used to associate a sub-account with a trust organization and tells the Fund that the 
Trust should receive Networking information for that account. 
Networked Trust accounts may also be Networked by a Firm, sometimes referred to as a “dual” Networked 
account. If such a relationship exists, Networking information should be sent to both the Trust and the Firm, by 
the Fund, through the Networking system. 
Dual Accounts-Matrix Levels 
“Dual” Networked Trust accounts are identified by the Trusts and Funds with a Matrix Level of Zero (0) and a 
Membership Identifier of “01”. 
These same Networked Trust accounts are identified by the Firms and Funds by t heir appropriate Matrix Level 
of three through four (3-4). 
Funds correspond with Firms: 
• Using the Matrix Level assigned to the sub-account and 
• The Firm’s BIN ([[Broker]] Identification Number). 
 
Funds correspond with Trusts: 
• Using a Matrix Level of Zero (0), 
• A Membership Identifier of “01” and 
• The Fund’s account number. 
Restrictions and Guidelines 
For “dual” Networked accounts, where both a Trust and a Firm are on the account, a Matrix Level of Three (3) 
should not be used. 
For further information, please reference the “Trust Processing Best Practices” on the Learning Center under 
MFS Cross Products section https://dtcclearning.com/documents/mutual-fund-services-1/mfs-cross-
product/1681-trust-processing-best-practices-1.html 
 
 
 

---

## Page 42

Networking Technical Guide 
 
Chapter 3, Section D–Mass [[Broker]] to [[Broker]] 42 
 
CHAPTER 3, SECTION D–MASS [[Broker]] TO [[Broker]] 
Overview 
Description 
Firms have the [[Option]] of using the Mass [[Broker]] to [[Broker]] Conversion feature in Networking to expedite bulk 
movement of accounts from one Firm to another on the records of the Fund.  
Mass [[Broker]] to [[Broker]] Conversions can be accomplished in an automated and controlled environment through 
the Account Set-Up/Update/Transfer and Acknowledgment function in Networking.  
Processing Steps 
Listed below are the guidelines for affecting a Mass [[Broker]] to [[Broker]] Conversion:  
1. The receiving Firm establishes new (shell) accounts on the Fund’s books.  
2. These “shell” accounts contain Account Set-Up information. (Please refer to the Account Conversion 
Section in this manual.) 
3. The receiving Firm places its number in the Clearing/Settling Firm Number field of Record Type B50. 
4. The relaying of the receiving Firm’s account number and the account Matrix Level for these new accounts 
is critical to the accurate processing of the conversion. 
5. Funds acknowledge back to the receiving Firm that the accounts were set up properly. Using Record Type 
F53, Funds place the receiving Firm’s number in the Clearing/Settling Firm Number field and a three (3) in 
the Transaction Type. 
6. The receiving Firm conveys to the Firm delivering the accounts, the account numbers associated with the 
newly Networked shell accounts. (This is accomplished outside of Networking.)  
7. The delivering Firm then submits a Transfer Request to the Fund using Record Type B52 and a 
Transaction Type of 4. 
8. Record Type B52 is used when the delivering Firm requests the Fund to move the [[shares]] out of the 
existing accounts into the shell accounts of the receiving Firm. 
9. The delivering Firm’s number is placed in the Clearing/Settling Firm field and the receiving Firm’s number 
is placed in the Receiving Firm Clearing/Settling Number field. 
10. A Transaction Type of four (4) on Record Type B52 tells the Fund that these transfers are a result of a 
Mass [[Broker]] to [[Broker]] Conversion. 
11. [[NSCC]] will place a unique Control Number in the Control Number field of the B52 record and send it to all 
three clients, the receiving Firm, the delivering and the Fund. 
12. Using Record Type F53, the Fund acknowledges the transfer request. The Fund places the delivering 
Firm number in the Clearing/Settling Firm Number field and the receiving Firm’s number in the Receiving 
Firm Clearing/Settling field and a 4 in the Transfer Type field. 
13. When [[NSCC]] receives the F53, it sends a copy to the receiving Firm and a copy to the delivering Firm.  
14. Generated Reminders (N49) are sent to both the Firms and the Fund. The F53 and the N49 records 
contain the same [[NSCC]] Control Number as the original B52. This will help the parties to reference and 
track their Transfers. 

---

## Page 43

Networking Technical Guide 
 
Chapter 3, Section D–Mass [[Broker]] to [[Broker]] 43 
 
15. Funds will send Activity records to the Firms indicating the closing balance on each account that was 
converted. The receiving Firm’s shell accounts should show the transferred [[shares]]. The delivering Firm’s 
accounts should show a zero balance. 

---

## Page 44

Networking Technical Guide 
 
Chapter 3, Section E–Change in [[Broker]]/Dealer 44 
 
CHAPTER 3, SECTION E–CHANGE IN [[Broker]]/DEALER 
Overview 
Description 
The fund company/[[transfer agent]] must receive instructions to change the [[Broker]]/dealer of record on a m utual 
fund account. Firms may use the Networking B51 record to submit a request to change the [[Broker]]/dealer 
information. The B51 record contains pertinent information that will enable the fund to recognize and carry out 
the request. Funds may then use the Networking F53 record to reject or acknowledge the request.  
Prerequisites 
Use of this feature is contingent on the signing of indemnification agreements by firms with their fund partners. 
Funds will accept or reject requests from firms based on the existence of an agreement.  
Support of the functionality is contingent on firm and fund participation, which are optional. However, Clients 
must be able to handle output records containing change in [[Broker]]/dealer information. For example, Funds 
must be able to recognize change in [[Broker]]/dealer requests and either process them or reject them. Firms 
must be able to recognize change in [[Broker]]/dealer acknowledgments and process them accordingly.  
The change in [[Broker]]/dealer feature should only be used for accounts that are Networking levels 0 or 4, but not 
on Network level 3 [[Broker]]-controlled accounts. [[NSCC]] does not validate this restriction for a change in 
[[Broker]]/dealer, except when the change to [[Broker]]/dealer is a Fund (dealer resignation requests) - fund 
[[Companies]]/ transfer agents must perform the appropriate validation. Change in [[Broker]]/dealer on Network level 
3 [[Broker]]-controlled accounts should be processed through a transfer on [[NSCC]]’s ACATS system in accordance 
with [[FINRA]] rules and guidelines. 
Process 
The Change in [[Broker]]/Dealer process on Networking will primarily be initiated by the new or “Change To” 
[[Broker]]/dealer; but, may also accommodate a request initiated by the former or “Change From” [[Broker]]/dealer. 
Both processes are described below along with the relevant fields from the B51 and F53 Networking records  
Change in [[Broker]]/dealer requests to assign the Fund as the new dealer of record must be facilitated 
through the ‘Change From’ process. 
Change in [[Broker]]/Dealer Initiated by the Change to [[Broker]]/Dealer 
1. The Change to B/D submits a B51. Specific information in the B51 include: 
Networking B51 Fields–Sequences 01 and 09 Description 
Networking B51 Fields–Sequence 01 
Clearing /Settling [[Broker]] Number Change To B/D [[NSCC]] [[participant]] number 
Network Control Indicator 0 or 4 only.  [[NSCC]] does not validate. Funds/TAs must validate. 
Customer Account Number Change From B/D's account number or fund account number. 
The fund or [[transfer agent]] will be able to identify the account by using 
the fund account number or a combination of the current B/D account 
number (BIN) and the Change From B/D's firm number. 

---

## Page 45

Networking Technical Guide 
 
Chapter 3, Section E–Change in [[Broker]]/Dealer 45 
 
Networking B51 Fields–Sequences 01 and 09 Description 
The fund account number is necessary if the Change To B/D cannot 
provide the Change From B/D's Firm Number ([[NSCC]] [[participant]] 
Number) on this B51 record (see New/Contra [[Broker]] of Record). 
Customer Account Number Indicator 1 (Fund), 2 ([[Broker]]), or 3 (NA) respective of the Change From B/D’s 
account number 
Networking B51 Fields–Sequence 09 
Change in [[Broker]]/Dealer Indicator 1 (Change To B/D) 
New [[Broker]] Identification Number Change To B/D's account number, i.e., BIN 
New/Contra [[Broker]] of Record Since the Change in B/D is being requested by the Change To B/D, this 
field is taken to mean the “contra” B/D’s (i.e., Change From B/D’s) 
[[NSCC]] [[participant]] number. 
The fund will need this information when the Customer Account Number 
that is provided on this B51 record is the BIN. 
The validation that applies to this scenario is: 
Required if Change in [[Broker]]/Dealer Indicator = 1 and Customer 
Account Number Indicator = 2. 
Branch Identification Number Change To B/D Information. Required for Record Type 51 when there is 
a new Firm Identification Number (BIN). 
The Change To B/D may be required to provide this information. The 
information should always be provided so that the account can be 
updated with the Change To B/D information. 
Account Representative Number Change To B/D Information. Required when there is a new Firm 
Identification Number (BIN) Number and System Code = B. 
The Change To B/D may be required to provide this information. The 
information should always be provided so that the account can be 
updated with the Change To B/D information. 
 
2. The Fund receives the B51, and with the use of the new “Change in [[Broker]]/Dealer Indicator” field, 
immediately identifies the Account Update record as a Change in [[Broker]]/Dealer requested by the Change 
To B/D. 
3. The Fund processes the request and returns an F53 to the initiating B/D, which is the Change To B/D. 
Specific information in the F53 include: 
 
Networking F53 Fields–Sequences 01, 02 and 03 Description 
Networking F53 Fields–Sequence 01 
Clearing/Settling [[Broker]] Number Change To B/D [[NSCC]] [[participant]] number 
Transaction Type 6 (Change in [[Broker]]/Dealer–Change To B/D) 
Corresponds to the Change in [[Broker]]/Dealer Indicator field on the B51 record. 

---

## Page 46

Networking Technical Guide 
 
Chapter 3, Section E–Change in [[Broker]]/Dealer 46 
 
Networking F53 Fields–Sequences 01, 02 and 03 Description 
Account Number Indicator • 1 (Debit Change From B/D's Acct # or BIN), or 
• 2 (Debit Change From B/D's Fund Acct #) 
Corresponds to the Account Number field, below. 
Account Number Change From B/D's account number respective of the Account Number 
Indicator. 
Corresponds to the Customer Account Number field on the B51 record. The 
fund or TA should return the fund account number so that the Change To B/D 
may cross-reference the number to the BIN, when applicable. 
Credit Account Indicator • 1 (Change To B/D's Acct # or BIN), or 
• 2 (Change To B/D's Fund Acct #) 
Corresponds to the Credit Account Number field, below. 
Credit Account Number Change To B/D's Account Number respective of the Credit Account Indicator 
Corresponds to the New Firm Identification Number (BIN) field on the B51 
record. 
Networking F53 Fields–Sequence 02 
Book/Physical Share Indicator The field is required but is optional for a Change in [[Broker]]/Dealer. The 
description states "transfer in" but should be implied as "gained in" or 
"delivered in" for a Change in B/D. 
PI Delivery Indicator This field is required but is optional for a Change in [[Broker]]/Dealer. The value 
submitted should reflect the status on the account regarding physical [[shares]]. 
Closing Balance (Debit Account) Optional Conditional. The Change From B/D's balance will always be zero; 
therefore, this field may be left blank. 
Closing Balance (Credit Account) Optional Conditional. The closing balance on the account, which now belongs 
to the Change To B/D. This field can be used by B/D to determine the share 
amount that was gained or lost, respectively. 
Note that the Closing Balance (Credit)–Extended field can be used to 
accommodate balances past the billion-share threshold in Omnibus 
processing. 
If the Extended field is used, this field must be left blank. 
Share Amount This field is used on transfer-related records. On a Change in [[Broker]]/Dealer 
request, the Closing Balance (Credit Account) can be used instead. 
Networking F53 Fields–Sequence 03 
Physical Share Amount Record 3 is an optional for a change in [[Broker]]/dealer and is typically used to 
send a duplicate record to the "receiving firm" on a mass [[Broker]]-to- [[Broker]] 
transfer. 
The physical share amount indicates the amount of the position that was in 
physical share status. 
 
Change in [[Broker]]/Dealer Initiated by the Change From B/D 

---

## Page 47

Networking Technical Guide 
 
Chapter 3, Section E–Change in [[Broker]]/Dealer 47 
 
1. The Change From B/D submits a B51.  Specific information in the B51 includes the following. The fields 
and descriptions in bold italics are different relative to the process initiated by the Change To  B/D. 
 
2. Specific information in the B51 includes the following. The fields and descriptions in bold italics are 
different relative to the process initiated by the Change To B/D. 
Networking B51 Fields–Sequences 01 and 09 Description 
Networking B51 Fields–Sequence 01 
Clearing/Settling Firm Number Change From B/D [[NSCC]] [[participant]] number 
Network Control Indicator 0 or 4 only ([[NSCC]] validates for Firm to Fund requests) 
0 or 4 ([[NSCC]] does not validate for Firm to Firm requests - 
Fund/TAs must validate). 
Customer Account Number Change From B/Ds account number or fund account 
number 
Customer Account Number Indicator 1 (Fund), 2 ([[Broker]]), or 3 (NA) respective of the Change 
From B/D's Customer Account Number. 
Networking B51 Fields–Sequence 09 
Change in [[Broker]]/Dealer Indicator 2 (Change From B/D) 
New Firm Identification Number New Firm Identification Number 
New/Contra [[Broker]] of Record Since the Change in B/D is being requested by the Change 
From B/D, this field is taken to mean the “new” B/D’s (i.e., 
Change To B/D’s) [[NSCC]] [[participant]] number. 
When requesting the Fund be assigned as the new B/D, 
the Change From B/D would provide the Fund’s [[NSCC]] 
[[participant]] Number. 
The Change From B/D must provide this information to the 
Fund/TA to properly place the Change To B/D as the new 
[[Broker]] of record. 
The validation that applies to this scenario is: 
Required if Change in [[Broker]]/Dealer Indicator = 2. 
Branch Identification Number Change To B/D Information. Required for Record Type 51 
when there is a new Firm Identification Number. 
The Change From B/D may be required to provide this 
information. The information should always be provided so 
that the account can be updated with the Change To B/D 
information. 
Account Representative Number Change To B/D Information. Required when there is a new 
Firm Identification Number and System Code = B. 
The Change From B/D may be required to provide this 
information. The information should always be provided so 
that the account can be updated with the Change To B/D 
information. 

---

## Page 48

Networking Technical Guide 
 
Chapter 3, Section E–Change in [[Broker]]/Dealer 48 
 
Networking B51 Fields–Sequences 01 and 09 Description 
Account Representative Name Change To B/D Information. Required when there is a new 
[[Broker]] Identification Number and System Code = B. 
The Change From B/D may be required to provide this 
information. The information should always be provided so 
that the account can be updated with the Change To B/D 
information. 
  
 
3. The Fund receives the B51, and with the use of the new “Change in [[Broker]]/Dealer Indicator” field, 
immediately identifies the Account Update record as a Change in [[Broker]]/Dealer requested by the 
Change From B/D. 
4. The fund processes the request and returns an F53 to the initiating B/D, which is the Change From B/D. 
Specific information in the F53 include the following on the grid. The fields and descriptions in bold italics  
are different relative to the process initiated by the Change To B/D. 
 
Networking F53 Fields–Sequences 01, 02 and 03 Description 
Networking F53 Fields –Sequence 01 Description 
Clearing/Settling [[Broker]] Number Change From B/D [[NSCC]] [[participant]] number 
Transaction Type 7 (Change in [[Broker]]/Dealer–Change From B/D) 
Corresponds to the Change in [[Broker]]/Dealer Indicator field 
on the B51 record. 
Account Number Indicator • 1 (Debit Change From B/D's Acct # or BIN), or 
• 2 (Debit Change From B/D's Fund Acct #) 
Corresponds to the Account Number field, below. 
Account Number Change From B/D's Account Number respective of the 
Account Number Indicator. 
Corresponds to the Customer Account Number field on the 
B51 record. The fund or TA should return the information 
from the B51 record. 
Credit Account Indicator • 1 (Change To B/D's Acct # or BIN), or 
• 2 (Change To B/D's Fund Acct #) 
Corresponds to the Credit Account Number field, below. 
Credit Account Number Change To B/D's Account Number respective of the Credit 
Account Indicator 
Corresponds to the New [[Broker]] Identification Number field 
on the B51 record. 
Networking F53 Fields –Sequence 02 Description 
Book/Physical Share Indicator This field is required; but, is optional for a Change in 
[[Broker]]/Dealer. The description states "transfer in" but 

---

## Page 49

Networking Technical Guide 
 
Chapter 3, Section E–Change in [[Broker]]/Dealer 49 
 
Networking F53 Fields–Sequences 01, 02 and 03 Description 
should be implied as "gained in" or "delivered in" for a 
Change in B/D. 
PI Delivery Indicator This field is required; but, is optional for a Change in 
[[Broker]]/Dealer. The value submitted should reflect the status 
on the account regarding physical [[shares]]. 
Closing Balance (Debit Account) Optional Conditional. The Change From B/D's balance will 
always be zero; therefore, this field may be left blank. 
Closing Balance (Credit Account) Optional Conditional. The closing balance on the account, 
which now belongs to the Change To B/D. This field can be 
used by both the Change To and Change From B/D to 
determine the share amount that was gained or lost, 
respectively. 
Note that the Closing Balance (Credit)–Extended field can 
be used to accommodate balances past the billion-share 
threshold in Omnibus processing. 
If the Extended field is used, this field must be left blank. 
Networking F53 Fields – Sequences 01, 02 and 03 
Share Amount This field is used on transfer-related records. On a Change 
in [[Broker]]/Dealer request, the Closing Balance (Credit 
Account) can be used instead. 
Networking F53 Fields –Sequence 03 Description 
Physical Share Amount Record 3 is an optional record and is typically used to send 
a duplicate record to the "receiving firm" on a mass [[Broker]]-
to- [[Broker]] transfer. 
The physical share amount indicates the amount of the 
position that was in physical share status. 
 

---

## Page 50

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 50 
 
CHAPTER 3, SECTION F–DOL [[Fiduciary]] RULE: 
ENHANCEMENTS AND BEST PRACTICES 
Background 
On April 6, 2016, the Department of Labor (DoL) issued a final [[regulation]] defining who is a “[[Fiduciary]]” of an 
employee benefit plan under the Employee Retirement Income Security Act of 1974 (ERISA) as a result of 
giving investment advice to an employee benefit plan, plan [[Fiduciary]], plan [[participant]] or beneficiary, individual 
retirement account (IRA), or IRA owner. The rule defined persons who provide investment advice or 
recommendations for a fee or other compensation with respect to assets of a plan or IRA as fiduciaries in a 
wider array of advice relationships.  
[[NSCC]] in conjunction with the DoL [[NSCC]] Enhancements Working Group of the Investment Company Institute’s 
(ICI) [[Broker]]/Dealer Advisory Committee and Bank, Trust and Retirement Advisory Committee (respectively; the 
“Working Group”) defined enhancements to the [[Mutual Funds]] Services necessary for our clients to comply with 
the DoL rule.  To see a complete list of enhancements, please refer to Important Notice a8286.  All DoL- related 
best practices provided in this document have been identified and approved by the working group in advance 
of the rule’s applicability date. 
Note: 
The original applicability date of April 10, 2017 was delayed by DoL. On March 15, 2018, The Fifth Circuit Court of 
Appeals, based in New Orleans, vacated the [[Fiduciary]] rule. On June 21, 2018, The Fifth Circuit Court of Appeals 
confirmed its decision to vacate the ruling as such all references to requirements under the rule have been 
removed within this section. 
 
Systematic Trades 
Firms whose business models allow direct at fund business will need to collect additional data on direct 
accounts where they may be listed as the [[Broker]] To provide further transparency and support communication 
of systematic trade activity on the direct at fund accounts, the following fields were added to Account 
Conversion / Update & Transfer / Acknowledgment Record F51*: 
• SWIP Indicator 
• Systematic Trade Changed To (new) Amount 
• Systematic Trade Changed From (old) Amount 
• Systematic Trade Changed To (new) Frequency 
• Systematic Trade Changed From (old) Frequency 
*Note: 
These fields are NOT allowed on records A/B/T50 and A/B/T51, the working group agreed this information would not be 
passed by an Investment Agent, Firm or TPA but would be provided only by the Fund on direct accounts. 
These fields are to be used in combination with the “Systematic Contribution Indicator” and “SWP Indicator” 
fields to allow for communication of systematic investment and withdrawal activity on the client’s account along 
with the contribution/withdrawal amount and frequency of these systematic transactions. Funds will need to 
indicate if the systematic trade is Existing, New, Modified or Closed as instructed by the client. Funds will also 
need to indicate all changes in the contribution/withdrawal amount and frequency as instructed by the client.  

---

## Page 51

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 51 
 
Members of the DoL Working Group discussed systematic withdrawal plans and various options for systematic 
redemptions (cash amount, percentages or [[shares]]).  Firms whose business models allow direct at fund 
business indicated that they require systematic investment information for direct at fund accounts, specifically 
changes in systematic investment frequencies and cash amounts.   Firms who require systematic trade 
information also indicated that systematic redemption information is NOT needed by their organizations.   
Members of the working group agreed that in the case of a systematic redemption executed in percentages or 
[[shares]], firms will have to rely on the actual dollar amounts being passed by funds on the [[NSCC]] Networking 
Activity F55 files.  Members of the working group also agreed that additional enhancements to F51 to support 
systematic redemptions executed in percentages and [[shares]] are not required at this time.  
 
“SWIP Indicator” field 
• This Optional field is used to indicate the status of the systematic plan on the client’s account (new, 
modified, closed or existing). The field has the following values: 
o Blank = N/A, there is no systematic plan on the account 
o 1 = New 
o 2 = Modified 
o 3 = Closed 
o 4 = Existing 
 
Systematic Trade Amount: “Systematic Trade Changed To (new) Amount” and “Systematic Trade 
Changed From (old) Amount” fields 
These fields allow for communication of an amount that is being invested or redeemed on a 
predetermined frequency during the calendar year as requested by the client.  For example, if the client is 
systematically investing $100 each month of the calendar year and subsequently changed their 
investment selection to $200 each month of the calendar year, “Systematic trade changed to (new) 
amount” field should be populated with “200” ($200), while “Systematic trade changed from (old) amount” 
field should contain the value of “100” ($100). 
• “Systematic trade changed To (new) amount” field-Required if “SWIP Indicator” is populated with “1=New” 
or “2=Modified”. This field is NOT allowed if the “SWIP Indicator” is not provided (blank).  
• “Systematic trade changed From (old) amount” field-Required if “SWIP Indicator” is populated with 
“2=Modified” or “3=Closed”. This field is NOT allowed if the “SWIP Indicator” is not provided (blank).  
 
 
Systematic Trade Frequency: “Systematic Trade Changed To (new) Frequency” and “System atic Trade 
Changed From (old) Frequency” fields 
• These fields will be used to communicate frequency of a systematic investment/withdrawal during the 
calendar year. 
• These fields are Optional/Conditional and are NOT allowed if the “SWIP Indicator” is not prov ided (blank). 
• These fields have the following values: 
o Blank = N/A 
o 01 = 1 month per year 
o 02 = 2 months per year 
o 03 = 3 months per year 

---

## Page 52

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 52 
 
o 04 = 4 months per year 
o 05 = 5 months per year 
o 06 = 6 months per year 
o 07 = 7 months per year 
o 08 = 8 months per year 
o 09 = 9 months per year 
o 10 = 10 months per year 
o 11 = 11 months per year 
o 12 = 12 months per year 
 
• “Systematic Trade Changed To (new) Frequency” field-Required if “SWIP Indicator” is populated with 
“1=New” or “2=Modified” 
• “Systematic trade changed From (old) frequency” field–Required if “SWIP Indicator” is populated with 
“2=Modified” or “3=Closed 
• These fields must contain the frequency of the systematic plan. Values in these fields correspond to the 
number of months (during the calendar year) the systematic trade is setup to contribute/withdraw:  
o Annual = “01” 
o Semi-annual = “02” 
o Quarterly = “04” 
o Monthly = “12” 
o Three months per year (for example: January, February and March) = “03”, etc.  
 
For example, if the client has a systematic investment each month of the calendar year (monthly) and 
subsequently changes this election to quarterly, systematic trade frequency fields should be populated as 
follows: 
o “Systematic trade changed to (new) frequency” field should be populated with “04” (4 months = 
quarterly) 
o “Systematic trade changed from (old) frequency” field should contain the value of “12” (12 months = 
monthly). 
 
Systematic Trade–Contribution vs. Withdrawal 
In order to communicate the type of the systematic trade (contribution or withdrawal), the following fields mu st 
be populated as follows: 
• Systematic Contributions 
o “Systematic Contribution Indicator” field must be set to “1” = Yes 
o “SWP” field (systematic withdrawal plan) must be set to “0” = No 
 
• Systematic Withdrawals: 
o “SWP” field must be set to “1” =Yes 

---

## Page 53

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 53 
 
o “Systematic Contribution Indicator” field must be set to “0” = No 
 
Best Practices: 
• New systematic transaction on the client’s account 
o Populate the “SWIP Indicator” field with “1” = New 
o Populate the frequency and amount in the “Systematic Trade Changed To (new) Frequency” and 
“Systematic Trade Changed To (new) Amount” fields. 
o “Systematic Trade Changed From (old Frequency” and “Systematic Trade Changed From (old) 
Amount” fields should be blank. 
 
• Closed systematic transaction on the client’s account 
o Populate the “SWIP Indicator” field with “3” = Closed 
o Populate the values that were in effect prior to closing in the “Systematic Trade Changed From (old) 
Frequency” and “Systematic Trade Changed From (old) Amount” fields. 
o “Systematic Trade Changed To (new) Frequency” and “Systematic Trade Changed To (new) 
Amount” fields should be blank. 
 
• Modified systematic transaction on the client’s client account 
o Populate the “SWIP Indicator” field with “2” = Modified 
o If only the amount is changing, both the old and the new amount fields must be populated. The old 
and the new frequency fields should be populated with the same value (existing client selection)  
o If only the frequency is changing, both the old and the new frequency fields must be populated. The 
old and the new amount fields should be populated with the same value (existing customer 
selection). 
o If both the amount and the frequency are changing, new amount and new frequency fields should 
contain new client selections, while the old amount and old frequency fields should contain previous 
customer selections that are being changed. 
 
The following table depicts the requirements for the SWIP Indicator, Amount and Frequency fields:  
Systematic 
Trade Status 
SWIP 
Indicator 
Systematic Trade 
Changed From (old) 
Amount 
Systematic 
Trade 
Changed To 
(new) Amount 
Systematic 
Trade Changed 
From (old) 
Frequency 
Systematic 
Trade Changed 
To (new) 
Frequency 
New 1 = New Blank Required (zero 
value is not 
allowed) 
Blank Required (blank 
is not allowed) 
Modified 2 = Modified Required (zero value is not 
allowed) 
Required (zero 
value is not 
allowed) 
Required (blank 
is not allowed) 
Required (blank 
is not allowed) 
Closed 3 = Closed Required (zero value is not 
allowed) 
Blank Required (blank 
is not allowed) 
Blank 

---

## Page 54

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 54 
 
 
Update to Existing Account vs. Scrub (Full Refresh) File 
• Update to Existing Account 
o If there is a change to the systematic plan, “SWIP Indicator” should be populated as follows:  
» New systematic plan: “SWIP Indicator” = “1” 
» Modifications to the systematic plan: “SWIP Indicator” = “2” 
» Closed systematic plan: “SWIP Indicator” = “3” 
Systematic Trade Amount and Frequency fields must be populated as specified in the above section. 
o If there is a change to the client’s account (e.g. address change), but no change to the systematic 
plan, “SWIP Indicator” should be populated as follows: 
» If there is an existing systematic plan on this account: “SWIP Indicator” = 4. Systematic trade 
amount and frequency fields should be blank. 
» If there is no systematic plan on this account: “SWIP Indicator” = Blank 
 
• Scrub File 
o If there is a systematic plan on this account, “SWIP Indicator” should be populated with the value of 
“4”. Systematic trade amount and frequency fields should be populated as follows: 
» “Systematic trade changed To (new) amount” and “Systematic trade change To (new) 
frequency” fields should be populated with the client’s current systematic plan amount and 
frequency selections. 
» “Systematic trade changed From (old) amount” and “Systematic trade change From (old) 
frequency” fields should be blank. 
o If there is no systematic plan on this account, “SWIP Indicator”, systematic trade amount and 
frequency fields should be blank. 
 
The following table provides a high-level overview of the systematic trade fields for the Update vs. Scrub File:  
 
 Scenario Systematic 
Trade Status 
SWIP 
Indicator 
Systematic 
Trade 
Changed 
From (old) 
Amount 
Systematic 
Trade 
Changed To 
(new) Amount 
Systematic 
Trade Changed 
From (old) 
Frequency 
Systematic 
Trade Changed 
To (new) 
Frequency 
Updates to 
existing 
account 
There is a 
change to 
the 
systematic 
plan on the 
client’s 
account 
New 1 = New Blank Required (zero 
value is not 
allowed) 
Blank Required (blank 
is not allowed) 
Modified 2 = Modified Required (zero 
value is not 
allowed) 
Required (zero 
value is not 
allowed) 
Required (blank 
is not allowed) 
Required (blank 
is not allowed) 
Closed 3 = Closed Required (zero 
value is not 
allowed) 
Blank Required (blank 
is not allowed) 
Blank 

---

## Page 55

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 55 
 
 Scenario Systematic 
Trade Status 
SWIP 
Indicator 
Systematic 
Trade 
Changed 
From (old) 
Amount 
Systematic 
Trade 
Changed To 
(new) Amount 
Systematic 
Trade Changed 
From (old) 
Frequency 
Systematic 
Trade Changed 
To (new) 
Frequency 
There is a 
change to 
the client’s 
account 
(exchange of 
address), but 
no change to 
the 
systematic 
plan 
Systematic plan 
exists on the 
account 
4=Existing Blank Blank Blank Blank 
No systematic 
plan on the 
account 
Blank Blank Blank Blank Blank 
Scrub File 
(Full 
Refresh) 
 Systematic plan 
exists on the 
account 
4= Existing Blank Provide the 
existing 
systematic plan 
amount 
selection 
Blank Provide the 
existing 
systematic plan 
frequency 
selection 
No systematic 
plan on the 
account 
Blank Blank Blank Blank Blank 
 
• “Systematic Withdrawal/Contribution Effective Date” field should contain the day when this maintenance 
activity took place. If this field is not populated, assume prior business day.  
 
  

---

## Page 56

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 56 
 
Communication of Systematic Trades via Account Conversion/Update & Transfer/Acknowledgement 
Record F51 
The following scenarios are strictly for illustration purposes and are intended to provide guidance on the usage 
of the systematic trade fields. These are examples only and should not be considered a comprehensive list of 
all possible scenarios. 
# Scenario 
Number of F51 
transactions 
required to 
communicate the 
status of the 
systematic plan 
on the client’s 
account 
“SWIP 
Indicator” 
field 
“Systematic 
Trade From 
(Old) 
Amount” 
field 
“Systematic 
Trade To 
(New) 
Amount” 
field 
“Systematic 
Trade From 
(Old) 
Frequency” 
field 
“Systematic 
Trade To 
(New) 
Frequency” 
field 
“Payment Date 
Indicators” field 
Example 1 
1 New systematic 
plan. Invest 
$100 quarterly. 
 
Invest on the 1st 
of the month 
Send one F51 
transaction 
1 = New  100  04 
(quarterly) 
01 
(invest on the 1st 
of the month) 
2 Modify scenario 
1 to invest $100 
monthly (change 
frequency). 
 
Invest on the 1st 
of the month 
Send one F51 
transaction 
2 = Modify 100 100 04 
(quarterly) 
12 (monthly) 01 
(invest on the 1st 
of the month) 3 Modify scenario 
2 to invest $200 
monthly (change 
dollar amount). 
 
Invest on the 1st 
of the month 
Send one F51 
transaction 
2 = Modify 100 200 12 (monthly) 12 (monthly) 01  
(invest on the 1st 
of the month) 4 Modify scenario 
3 to invest $400 
semiannually 
(change 
frequency and 
amount). 
Invest on the 1st 
of the month 
Send one F51 
transaction 
2 = Modify 200 400 12 (monthly) 02 
(semiannually) 
01 
(invest on the 1st 
of the month) 
5 Modify client 
address, no 
change to the 
existing 
systematic plan 
from Scenario 4. 
Send one F51 
transaction 
(communicate the 
change of 
address) 
4= Existing      

---

## Page 57

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 57 
 
# Scenario 
Number of F51 
transactions 
required to 
communicate the 
status of the 
systematic plan 
on the client’s 
account 
“SWIP 
Indicator” 
field 
“Systematic 
Trade From 
(Old) 
Amount” 
field 
“Systematic 
Trade To 
(New) 
Amount” 
field 
“Systematic 
Trade From 
(Old) 
Frequency” 
field 
“Systematic 
Trade To 
(New) 
Frequency” 
field 
“Payment Date 
Indicators” field 
6 Modify scenario 
4 to two 
systematic plans 
that will invest 
as follows: 
 
Plan 1–Invest 
$100 on January 
1st and 
February 1st. 
 
Plan 2–Invest 
$300 on January 
15th and 
February 15th 
Send two F51 
transactions: 
 
 
1) Modify Scenario 
4 to invest $100 
on January 1st 
and Feb 1st 
 
2)Setup a new 
plan - monthly 
payments on the 
15th of the month 
for two months 
(January and 
February) 
 
 
 
 
2 = Modify 
 
 
 
 
1 = New 
 
 
 
 
400 
 
 
 
 
100 
 
 
 
 
300 
 
 
 
 
02 
(2 months–
January and 
February) 
 
 
 
 
02 
(2 months–
January and 
February) 
 
02 
(2 months–
January and 
February) 
 
 
 
 
01 
(invest on the 
1st of the 
month) 
 
15 
(invest on15th 
day of the 
month) 
Example 2 
1 Two new 
systematic 
plans (invest 
twice a month, 
three months 
per year). 
 
Plan 1: Invest 
$100 on 
January 2
nd, 
February 2nd 
and March 2nd. 
 
Plan 2: Invest 
$200 on 
January 16
th, 
February 16th 
and March 16th 
Send two F51 
transactions (one 
per each 
systematic plan) 
 
 
 
 
 
 
1 = New 
 
 
 
1 = New 
  
 
 
 
 
 
100 
 
 
 
200 
  
 
 
 
 
03 
(3 months-
January, 
February, 
March) 
 
03 
(3 months-
January, 
February, 
March) 
 
 
 
 
 
02 
(invest on the 
2nd day of the 
month) 
 
  
16 
(invest on 
the 16th day of 
the month) 

---

## Page 58

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 58 
 
# Scenario 
Number of F51 
transactions 
required to 
communicate the 
status of the 
systematic plan 
on the client’s 
account 
“SWIP 
Indicator” 
field 
“Systematic 
Trade From 
(Old) 
Amount” 
field 
“Systematic 
Trade To 
(New) 
Amount” 
field 
“Systematic 
Trade From 
(Old) 
Frequency” 
field 
“Systematic 
Trade To 
(New) 
Frequency” 
field 
“Payment Date 
Indicators” field 
2 Modify scenario 
1. 
 
Plan 1–modify 
to invest $150 
on January 2nd, 
February 2nd 
and March 2nd 
(change 
amount) 
 
Plan 2–NO 
changes 
(continue to 
invest 
$200 on 
January16, 
February 16, 
March 16). 
Send one F51 
record to modify 
Plan 1 (January 
2nd, February 2nd 
and March 2nd 
investments) 
 
 
 
2 = Modify 
 
 
 
100 
 
 
 
150 
 
 
 
03 
(3 months-
January, 
February, 
March) 
 
 
 
03 
(3 months-
January, 
February, 
March) 
 
 
 
02 
(invest on the 2
nd 
day of the 
month) 
3 Modify scenario 
2 (modify both 
plans’ 
frequencies 
from investing 
twice a month 
for 3 months to 
twice a month 
for 5 months per 
year) 
Send two F51 
transactions (one 
per each modified 
plan) 
      
 Plan 1–modify 
to invest $150 
on January 2, 
February 2, 
March 2, April 2, 
May 2. 
 2 = Modify 150 150 03  
(3 months -
January, 
February, 
March) 
05  
(5 months -
January, 
February, 
March, April, 
May 
02 
(invest on the 
2nd day of the 
month) 
 Plan 2–modify 
to invest $200 
on January 16, 
February 16, 
March 16, April 
16, May 16. 
 2 = Modify 200 200 03  
(3 months -
January, 
February, 
March) 
05  
(5 months -
January, 
February, 
March, April, 
May 
16 
(invest on the 
16th day of the 
month) 
4 Modify scenario 
3 (change 
investments 
from twice a 
month for 5 
months to once 
Send two F51 
transactions 
 
1) Close Plan 1 - 
$150 monthly 
3 = Close 150  05  
(5 months-
January, 
February, 
March, April, 
May 
 02 
(invest on the 2
nd 
day of the 
month) 

---

## Page 59

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 59 
 
# Scenario 
Number of F51 
transactions 
required to 
communicate the 
status of the 
systematic plan 
on the client’s 
account 
“SWIP 
Indicator” 
field 
“Systematic 
Trade From 
(Old) 
Amount” 
field 
“Systematic 
Trade To 
(New) 
Amount” 
field 
“Systematic 
Trade From 
(Old) 
Frequency” 
field 
“Systematic 
Trade To 
(New) 
Frequency” 
field 
“Payment Date 
Indicators” field 
a month for 5 
months). 
investment on the 
2nd of each month 
 
2) Modify Plan 2 -
$200 investment 
on the 16th of 
each month 
 Invest $350 
monthly–
January, 
February, 
March, April, 
May. Invest on 
the 16th of the 
month 
2 = Modify 200 350 05  
(5 months-
January, 
February, 
March, April, 
May 
05  
(5 months-
January, 
February, 
March, April, 
May 
16 
(invest on the 
16
th day of the 
month) 
5 Modify Scenario 
4 to invest $350 
monthly–
January, 
February, 
March, 
April on the 10th 
of the month. 
(modify 
investment day 
only) 
Send one F51 
transaction 
2 = Modify 350 350 05  
(5 months-
January, 
February, 
March, April, 
May 
05  
(5 months-
January, 
February, 
March, April, 
May 
10 
(invest on the 
10th day of the 
month) 
6 Scrub File: 
Communicate 
information 
about the 
existing plan 
(modified in 
Scenario 5) on 
the “Scrub” file 
Send one F51 
transaction 
4=Existing  350  05  
(5 months-
January, 
February, 
March, April, 
May 
10 
(invest on the 
10th day of the 
month) 
7 Close the plan 
that was 
modified in 
Scenario 5. 
Send one F51 
transaction 
3 = Close 350  05  
(5 months-
January, 
February, 
March, April, 
May 
 10 
(invest on the 
10
th day of the 
month) 
Example 3 
1 Three new 
systematic 
plans (invest 
three times a 
month, three 
months per 
year). 
Send three F51 
transactions (one 
per each 
systematic plan) 
      
 Plan 1: Invest 
$100 on 
January 2nd, 
 1 = New  100  03  01 

---

## Page 60

Networking Technical Guide 
 
Chapter 3, Section F–Dol [[Fiduciary]] Rule: Enhancements and Best Practices 60 
 
# Scenario 
Number of F51 
transactions 
required to 
communicate the 
status of the 
systematic plan 
on the client’s 
account 
“SWIP 
Indicator” 
field 
“Systematic 
Trade From 
(Old) 
Amount” 
field 
“Systematic 
Trade To 
(New) 
Amount” 
field 
“Systematic 
Trade From 
(Old) 
Frequency” 
field 
“Systematic 
Trade To 
(New) 
Frequency” 
field 
“Payment Date 
Indicators” field 
February 2nd 
and March 2nd 
(3 months-
January, 
February, 
March) 
(invest on the 2nd 
day of the 
month) 
 Plan 2: Invest 
$200 on 
January 10th, 
February 10th 
and March 10th 
 1 = New  200  03  
(3 months-
January, 
February, 
March) 
10 
(invest on the 
10th day of the 
month) 
 Plan 3: Invest 
$300 on 
January 20
th, 
February 20th 
and March 20th 
 1 = New  300  03  
(3 months-
January, 
February, 
March) 
20 
(invest on the 
20th day of the 
month) 
 
Initial vs. Subsequent Purchase 
“Transaction Type” field on the Activity Record F55 contains a number of transaction types/codes that can be 
provided in this field to specify the type of transaction being communicated. The following two additional 
Networking Transaction Codes were added under the existing “01-Direct Purchase” Transaction Type to 
Activity Record F55: 
• AZ = Initial Purchase 
• A@ = Subsequent Purchase 
 
Best Practice: 
• Transaction Description Codes “AZ=Initial Purchase” and “A@=Subsequent Purchase” should be used in 
lieu of Transaction Type “01=Direct Purchase”. 
• Direct Purchase transactions that utilize Transaction Description Codes (other than AZ and A@) listed 
under Transaction Type “01=Direct Purchase” on the Networking Transaction Codes list should continue  
to provide these sub-category codes. 
Account Open Date 
An optional “Account Open Date” was added to Activity Record F55 and Position Record F58. This field will 
allow funds to communicate the date of account establishment for the particular Security Issue [[ID]]. 
Best Practice: 
This field should be populated with the date of account establishment for the particular Security Issue [[ID]]. This 
field is NOT intended to communicate the date of account funding. 

---

## Page 61

Networking Technical Guide 
 
Chapter 4–Networking Record Layouts 61 
 
CHAPTER 4–NETWORKING RECORD LAYOUTS 
Overview 
How to Read a Networking Record Layout 
Rules 
When reading a Networking record layout, the following rules apply: 
• Only accepted transactions are sent to the contra [[participant]]. Transactions rejected by [[NSCC]] are returned 
to the originating [[participant]]. 
• On input records, a Fund’s number is always an optional field. If it is not provided, [[NSCC]] will fill it in based 
on the Security Issue [[ID]] number. The contra side will receive the records with the Fund number in the 
field. 
• When rejecting a transaction for more than one reason, Fund/SERV reports multiple reject codes via 
Record Type 120 which follows the rejected transaction back to the originating [[Member]].  
 
Reference: For a list of reject codes for Networking, please see the documentation section on the Learning 
site. 
Column Headings 
The record layout column headings are described in the table below. 
Heading Description 
Start The position where the field starts 
End The position where the field ends 
Length The length of the field in bytes 
Type The type of the field: 
• A/N = Alphanumeric, and 
• N = Numeric. 
Field Description Field name including allowable values and their meanings, format and 
conditional requirements when applicable. 
Optional/Required Indicates whether the field is optional or required: 
O Optional 
R Required 
OC Optional but conditionally required 
RC Required but conditionally optional 

---

## Page 62

Networking Technical Guide 
 
Chapter 4–Networking Record Layouts 62 
 
 
Alphanumeric and Numeric Fields 
Alphanumeric fields may include any character in the computer character set; but, should not include 
unprintable characters such as low-value, high-value, comp-3 fields, etc., since these types of characters may 
cause problems during transmission time. 
Note: 
Numeric type fields may include digits (0-9) only. 
Required Fields 
Required fields include: 
• Fields with a specified list of values that must contain one of those values 
• Alphanumeric type fields without a specified list of values that may have any value as described above, 
but without spaces 
• Numeric fields without a specified list of values that are numerically greater than zero, and 
• Fields with other requirements that must follow those requirements. (For example: the firm number must 
be valid and eligible for Networking.) 
Optional Fields 
Optional fields include: 
• Fields with a specified list of values that have one of those values or spaces  
• Alphanumeric fields without a specified list of values that are numeric or spaces  
• Numeric fields without a specified list of values that are numeric or space, and  
• Fields with other requirements that follow those other requirements or may contain spaces, e.g., the fund 
number must be valid and eligible for Networking or contain spaces. 
 
Date Format 
Year 2000 compliant dates follow the format of MMDDCCYY, unless otherwise indicated  in the applicable 
networking record layout. 
Networking Record Layouts 
Reference: Information on Networking data submission records can be accessed at the documentation section 
on the Learning site. 
[[NSCC]] strongly recommends that when programming for Networking you make accommodations for all record 
types. This is to protect you in the event that a firm or a fund submits a record that you may not normally 
receive. Under such circumstances, you will be aware of that record’s existence and will be able to discuss the 
transmission of that record with the originator. 

---

## Page 63

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 63 
 
CHAPTER 5, SECTION A–FIELD DESCRIPTIONS FOR 
NETWORKING RECORD LAYOUTS 
Field Descriptions 
The field descriptions for the Networking record layouts are listed alphabetically and are described in the table 
below. 
Field Description 
ABA Routing Number American Banking Association (ABA) Routing Number used to direct monies to the proper 
account. 
ACATS Control Number This is the original ACAT Control Number from the failed ACAT Transfer 
Account Number Account number to be debited. 
Account Number Indicator Indicates the account to be debited 
1 = firm number, and 
2 = fund. 
Note: 
A number 3 used by the fund in Record Type 53 indicates that a new account number has 
been supplied. 
Account Share Balance Share balance in the account, as of the balance date, including both book and physical 
[[shares]]. Used when the share balance is less than 16 bytes in length. 
Account Open Date Date of account establishment for the particular Security Issue [[ID]].  This is NOT the date of 
account funding. 
Account Share Balance 
- Extended 
Share balance in the account, as of the balance date, including both book and physical 
[[shares]]. It is used when the share balance exceeds the usual Share Balance field length. 
This field is required if the Account Share Balance is NOT provided. Otherwise it is not 
allowed. 
This field supports the reporting of omnibus account share balances which exceed the 
billion-share threshold. 
ACH Indicator Indicates Automated Clearing House. 
Accrual Starting Date Start of a [[Dividend]] period for accrual funds. 
Average Accrual Rate See [[Dividend]] Rate. 
Balance Date Date of the closing balance. 
Book/Physical Share 
Indicator 
Form of the [[shares]] being transferred 
1 = book [[shares]] transferred from the debit account into book [[shares]] in the credit account. 
2 = physical [[shares]] transferred from the debit account into book [[shares]] in the credit account. 

---

## Page 64

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 64 
 
 
Field Description 
([[Broker]]) Firm Identification 
Number (BIN) 
A unique number, up to 20-digit digits recognized by both the Number (BIN) Fund and the 
Firm and used in identifying customer accounts. 
Buy/Sell Indicator An informational field used to qualify a trade adjustment. This is an optional field that will not 
affect the debit/credit indicator. 
Cash Distribution Indicator Destination of the cash disbursement. 
1 Cash to Firm 
2 Cash to Customer 
3 Payable Address 
4 Cross Fund Reinvest 
5 1099 Update Only 
6 Cash to Trust 
Chapter 4 Status Code Indicates the FATCA status of an FFI. 
Check Writing Privileges Indicates whether a shareholder can write checks against the account. 
Clearing/Settling Firm 
Number 
A unique four-digit number identifying the [[NSCC]] Firm. 
Clearing/Settling Fund 
Number 
A unique four-digit number identifying the [[NSCC]] routing Fund. 
Clearing/Settling Recipient 
Number 
[[NSCC]] Fund or Firm number that will be receiving the file. 
Closing Balance (Credit 
Account) 
Final position of the “to” account after the [[shares]] are transferred. Used when the closing 
balance is less than 16 bytes in length. 
Closing Balance (Credit 
Account)–Extended 
Final position of the “to” account after the [[shares]] are transferred. It is used when the closing 
balance exceeds the usual Closing Balance (Credit Account) field length. 
This field is required if the Closing Balance (Credit Account) is NOT provided. Otherwise it is 
not allowed. 
Closing Balance (Debit 
Account) 
Final position of the “from” account after the [[shares]] are transferred. Used when the closing 
balance is less than 16 bytes in length. 
Closing Balance (Debit 
Account)-Extended 
Final position of the “from” account after the [[shares]] are transferred. It is used when the 
closing balance exceeds the usual Closing Balance (Debit Account) field length. 
This field is required if the Closing Balance (Debit Account) is NOT provided. Otherwise it is 
not allowed. 
This field supports the reporting of omnibus account share balances which exceed the 
billion-share threshold. 

---

## Page 65

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 65 
 
Field Description 
Closing Book/Physical 
Balance 
Final position for an account, including both book and physical [[shares]]. Used when the 
closing balance is less than 16 bytes in length. 
Closing Book/Physical 
Balance–Extended 
Final position for an account, including both book and physical [[shares]]. It is used when the 
closing balance exceeds the usual Closing Book/Physical Balance field length. 
This field is required if the Closing Book/Physical Balance is NOT provided. Otherwise it is 
not allowed. 
This field supports the reporting of omnibus account share balances which exceed the 
billion-share threshold. 
Combined TEFRA/NRA 
Withholding Indicator 
Used to identify withholding on an account level: 
1 TEFRA 
2 NRA 
3 None 
Commission Amount Commission money associated with activity (e.g., CDSC). 
Commissionable [[shares]] 
Indicator 
Used to identify whether [[shares]] are commissionable upon exchange. 
Cost Basis [[Option]] Indicates the cost basis method requested for the account: 
0 Unknown 
1 FIFO (First in First Out) 
2 LIFO (Last in First Out) 
3 High Cost 
4 Low Cost 
5 Average Cost 
6 Select Lot 
Country of Origin Used to determine the NRA tax rate needed to calculate the amount of tax to be withheld. 
Credit Account Indicator Defines the account number to be referenced (Firm or Fund). 
Credit Account Number Number that the Firm uses to identify the account to be credited on an existing account or to 
establish a cross-reference for a new account (see Transaction Code). 
Credit Sub-Account 
Number 
Underlying “credit” account customer account number at the Fund. 
Cross-Reinvest Used to identify the fund in which [[Dividend]] money was earned. 

---

## Page 66

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 66 
 
Field Description 
Customer Account Number Used in conjunction with the Customer Account Indicator to identify the shareholder account 
number. When establishing a Networking account at the Fund, this field contains the Firm 
identification number. Consequently, the Customer Account Number becomes the number 
that both the Firm and Fund must use in subsequent transactions (see Example 1). 
Example 1 
Customer Account Number, when Indicator= 2 (Firm) is the Firm Identification Number 
(sometimes referred to as a BIN or Firm or [[Broker]] Identification Number.) 
Example 2 
Record Types 50 and 51 can also be used to set up the cross-reference file at the Fund. 
If the Customer Account Number = Fund Account Number, then the Customer Account 
Number Indicator = 1 (Fund) 
New Firm I.D. Number = Firm I.D. Number (Firm’s Account Number) 
Note: 
This should not be a pre-existing number on the Fund’s cross- reference file. 
Example 3 
Record Type 51 can be used for Account Executive swings or account number changes. 
If the Customer Account Number = Old Firm’s I.D. Number and the Customer Account 
Number Indicator = 1 (Fund) 
New Firm’s I.D. Number = Firm’s I.D. Number 
Customer Account Number 
Indicator 
Number used to identify the customer’s account: 
1 = Fund 
2 = Firm. 
Debit/Credit Indicator Indicates whether the activity will reduce or increase the share amount (1 and 2, 
respectively). 
Note: 
The character 3 is used for Transaction Type 50 where a balance is sent, and this field does 
not apply. 
Debit Sub-Account Number Underlying “debit” customer account number at the Fund. 
Description Required for Record Type 55 and Transaction Types 20 and 21 but may be used for 
clarification of any transaction. 
[[Dividend]] Code Indicates whether dividends, long-term capital gains, and short-term capital gains will be 
distributed in cash or reinvested. 
[[Dividend]] Debit/Credit 
Indicator 
1 = Not Applicable 
2 = [[Dividend]] Reversal (Debit) 
3 = [[Dividend]] Correction (Credit) 
4 = [[Dividend]] Debit 
5 = [[Dividend]] Credit 

---

## Page 67

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 67 
 
Field Description 
[[Dividend]] Distribution Type 1 = Daily Accrual, and 
2 = Declared Distribution 
Daily Accruals are based on activity and balances through the period where Declared 
Distributions have a one-time [[Dividend]] applied to the balance of a specific record date. 
[[Dividend]] Rate Rate per share in the form 99.999. This field can also be used to define the average accrual 
rate. 
[[Dividend]] Rate/ Capital 
Gain Rate–Extended 
This field is used to support those recipients that require an extended rate. This is a 
REQUIRED field. Funds that [[DO]] not create an extended rate will provide the same rate as 
entered in the [[Dividend]] Rate/ Capital Gain Rate on Sequence 1 of F61 and F62 records. 
999,999.999999999 
Dollar Amount Dollar amount or value of the activity associated with a particular transaction. 
Effective Date Record Types 52 and 53 indicate the “Input” date on the transfer or the “Processing” date on 
the acknowledgment. 
Record Type 55 indicates the fund’s processing date. 
Exchange Fee Fee associated with an exchange transaction. 
Executing Firm Unique four-digit number associated with the Firm who has the relationship with the 
customer. 
Note: 
When there is no Executing Firm, the Clearing Firm’s number appears in this field. 
FATCA Withholding 
Amount 
Dollar amount of FATCA tax withheld. 
Notes: 
For dividends, the amount is reflected on Records 64 and 66. 
For Record 55, the amount is the tax withheld as a result of trade activity. 
FATCA Withholding Rate Rate used to determine the amount of money to be withheld for tax purposes (typically 
30%). 
FATCA Override Special 
Rate 
Provides the ability to transmit an amount other than the standard 30% withholding FATCA 
(Foreign Account Tax Compliance Act) rate to be applied to an account. 
Fee Amount Amount of money applied as fees to an account. 
Fee Type Type of fee. 
1 N/A 
2 Fund Expense (Credit) 
3 Fund Expense (Debit) 

---

## Page 68

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 68 
 
Field Description 
4 Other (Credit), and 
5 Other (Debit) 
Foreign Account Tax 
Compliance Act (FATCA) 
The Foreign Account Tax Compliance Act (FATCA) was enacted by Congress to target non- 
compliance by U.S. taxpayers using foreign accounts. FATCA requires foreign financial 
[[Institutions]] (FFIs) to report to the IRS information about financial accounts held by U.S. 
taxpayers, or by foreign entities in which U.S. taxpayers hold a substantial ownership 
interest. 
Foreign Financial Institution 
(FFI) 
For FATCA purposes, an FFI is defined as any financial institution that is a foreign entity, 
other than a financial institution organized under the laws of a possession of the United 
States. 
Fund Payout Cycle Used to indicate the fund’s [[Dividend]] payout cycle. 
01 Monthly 
02 Quarterly 
03 Semi-Annual 
04 Annual 
05 Periodic 
06 Special 
07 [[Stock]] Split 
Fund Reject Code Used to indicate the fund’s rejection of a transfer of assets. 
Fund/SERV Control 
Number 
Used by Funds to identify accounts that remain in a “paid-in-waiting” status. 
This situation occurs when a Fund/SERV order settles but the associated registration 
rejects. Funds can use this field to put the control number from the rejected registration on 
the Networking record. 
Networking does not validate the Fund/SERV control number. 
Gift Indicator Specifies if the transfer is a gift (1) or Not (Blank). Optional. 
Global [[intermediary]] 
Identification Number 
(GIIN) 
IRS issued number to identify and establish the FATCA status of a Foreign Financial 
Institution (FFI). The GIIN is issued to deemed-compliant FFI's who have registered with the 
IRS. 
Initiating Firm This field identifies the [[NSCC]] [[ID]] of the [[Member]] creating and delivering a transaction to 
[[NSCC]]. This was introduced for mass [[Broker]] to [[Broker]] conversion processing. 
For more information, reference the “Direct Transfer (Omni Reconciliation F55) Best 
Practices” under the Networking Resources tab on Learning filtered for Best Practices.  
IRA Year of Contribution For non-IRA accounts, the [[default]] of 3 is given. All other IRAs can apply to either: 
• The current year (1), or 

---

## Page 69

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 69 
 
Field Description 
• The previous year (2). 
LOI Escrow Balance Shows the number of [[shares]] held in escrow (both book and physical). 
LOI Number/Date Allows for the referencing of the contract. 
[[Margin]] Account Indicator Used to indicate whether an account has margined [[shares]] or not: 
0= No 
1=Yes 
Memo Field Can be used for any additional information needed on the [[Dividend]] Header Record, but 
specifically intended for the Fund Payout Cycles of: 
• 06 (Special), and 
• 07 ([[Stock]] Split). 
Note: 
Memo field on Record Types 50 and 51 are for Fund/SERV use only. 
NAV Account Indicator An indicator used to specify certain account such as an employee account, where purchases 
are made at the NAV price. 
Network Control Indicator A one-digit indicator showing the Matrix Level. A zero indicates a Non-Networked account, 
unless there is a Membership Indicator denoting a Trust. In this instanced it would be a Trust 
Networked account. 
New/Contra [[Broker]] of 
Record 
Facilitates Fund notification of a change in [[Broker]]/dealer on a direct account. 
New Firm Identification 
Number 
See Customer Account Number. 
New Firm of Record Used to indicate when a shareholder changes Firms. 
NRA Tax Non-Resident Alien Tax stated as a percentage; the amount of tax to be withheld based on 
the Country of Origin. 
[[NSCC]] Control Number A unique 11-digit [[NSCC]] number used to monitor financial transactions (Record 52, 53) that 
refers to a [[NSCC]] system generated Control Number that will require an acknowledgment 
from the fund. Reminders will be issued daily for any pending transactions. 
FORMAT: JJJYXXXXXXX where: 
JJJ Positions 1-3 = three-digit Julian date 
Y Position 4 = last digit of the Year (0 thru 9) 
XXXXXXX Positions 5-11 are alpha/numeric 
Opposing Clearing/Settling 
Firm Number (F55) 
[[NSCC]] [[participant]] number of the Firm or Fund 

---

## Page 70

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 70 
 
Field Description 
Opposing 
Originating/Underlying Firm 
Number (F55) 
The [[NSCC]] [[ID]] of the underlying firm, where the firm is transacting through an MF Agent. In 
instances where an ACATS transfer failed and a Direct Transfer was effected, this field 
provides the necessary cost basis transparency by identifying the underlying firms that 
would hold or receive the cost basis information 
Note: 
This field should be populated from the perspective of the recipient of the F55. 
Originating/Underlying Firm 
Number (F55) 
The [[NSCC]] [[ID]] of the underlying firm, where the firm is transacting through an MF Agent. In 
instances where an ACATS transfer failed and a Direct Transfer was effected, this field 
provides the necessary cost basis transparency by identifying the underlying firms that 
would hold or receive the cost basis information
 
Note: 
This field should be populated from the perspective of the recipient of the F55. 
Original Control Number The original control number is used to assist omnibus firms to identify fund-initiated transfers 
into their house accounts. 
Original Control Number 
Indicator 
Used to identify the source of the original control number: 
1 Fund/SERV Control Number 
2 Networking Control Number 
3 Manual Reference Number 
Original Trade Date/ 
Payable Date For Div. Adj. 
The Original Trade Date is for any adjustment transaction that needs to refer back to an 
earlier transaction. 
Note:  
For [[Dividend]] adjustments, the Payable Date is supplied. 
Payable Account Number Account number associated with the payable address where the monies are to be sent. 
Payable Address Options Specifies which monies are credited to the payable address. It may be for dividends, 
systematic withdrawals, automatic drafts or a combination. 
Payable Date Date payment of dividends is due the shareholder. 
Payable Information 
Indicator 
Indicates where money for Direct Redemptions will go. 
1 Firm 
2 Custodian 
3 Payee (for dividends) 
Payee Indicator The number of days in a payment cycle. Used for accrual funds. 
PI Delivery Indicator Physical Issuance Indicator. 

---

## Page 71

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 71 
 
Field Description 
Plan Account Number The account number of a plan at the Trust, TPA or Record Keeper 
Plan Account Number 
Indicator 
Distinguishes entity (Trust, TPA or Record Keeper) the plan account number provided is 
associated to. 
Posting Date The date the fund posts the dividends in the shareholder’s account. 
Price Refers to the price per share (999.999). 
Processing Date Record Type 56 (Activity/Balance Trailer) reflects the date that the file was processed. 
Record Date The date on which shareholders of record are entitled to a [[Dividend]]. 
Record Date [[shares]] Communicates the share amount a declared [[Dividend]] or capital gain is being paid on. 
Record Type Specifies a particular record. This field is present on all records. 
45 Year End Record 
49 Pending Transfer Reminder 
50 New Account 
51 Update to Existing Account 
52 Account Transfer 
53 Fund Acknowledgment 
54 Trailer Record for 50, 51, 52, and 53’s 
55 Activity Detail Record 
56 Trailer Record for Activity 
57 Position Header Record 
58 Position Detail Record 
59 Position Trailer Record 
60 Position Grand Total Trailer Record 
61 [[Dividend]] Header Record 
62 Capital Gain Header Record 
63 [[Dividend]]/Capital Gain–Detail Record for Cash Accounts not Subject to 
Withholding 
64 [[Dividend]] Capital Gain–Detail Record for Cash Accounts Subject to 
Withholding 

---

## Page 72

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 72 
 
Field Description 
65 [[Dividend]]/Capital Gain–Detail Record for Reinvest Accounts not Subject to 
Withholding 
66 [[Dividend]]/Capital Gain–Detail Record for Reinvest Accounts Subject to 
Withholding 
67 [[Dividend]]/Capital Gain–Detail Record for Reinvest Accounts (Supplemental 
Record) 
68 [[Dividend]]/Capital Gain–Second Trailer Record by Firm 
70 [[Dividend]]/Capital Gain Grand Total Trailer Record 
Redemption Fee Money 
Amount 
This field is used to pass the Redemption Fee Money amount for the following fee types 
• Money Market [[Liquidity]] Fee 
• Short Term Redemption (STR) Fee 
Note 
For more information on Money Market [[Liquidity]] Fees and best practices for “Redemption 
Fee Money Amount” and “Redemption Fee Rate” fields please refer to “Money Market Fund 
Reform User Guide and Best Practices” document located on www.[[DTCC]].com 
Redemption Fee Rate This field is used to pass the Redemption Fee Rate for the following fee types 
• Money Market [[Liquidity]] Fee 
• Short Term Redemption (STR) Fee 
Reference Number Used to give both parties a way of identifying their transactions. Similar to a Control Number 
in Fund/SERV; however, it is not maintained by [[NSCC]]. It is for Firm and Fund internal use. 
This unique 11-digit number is used to monitor non-financial transactions. The following 
convention has been adopted by [[NSCC]] for the Reference Number generation on 
Conversion records and Acknowledgments of non-financial transactions only. 
Reference number refers to a [[Member]]-initiated Control Number using the standard format, 
JJJYXXXXXXX where: 
• JJJ = Julian Date 
• Y = Last digit of the year 
• XXXXXXX = Alpha/numeric sequence. 
Re-Invest Date The date used to establish the NAV (Net [[Asset]] Value) for dividends. 
Re-Invest Price The price at which [[shares]] are re-invested (999.999). 
Re-Invest [[shares]] The number of [[shares]] to be re-invested (99,999,999.999). 
Reject Codes Descriptive codes used to indicate why a transaction was rejected by [[NSCC]]. 
Related Trade Indicator Used with the Related Account Number field to identify the breakpoint that applies to that 
sale. 
ROA/LOI Value Rights of Accumulation/Letter of Intent field contains the amount of money the customer 
agrees to purchase. 
Sales Charge Rate Sales charge associated with an activity. 

---

## Page 73

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 73 
 
Field Description 
Security Issue [[ID]] Committee on Uniform [[securities]] Identification Procedures established by Standards & 
Poor, Inc. A unique security identification number is assigned to each security issued. 
Sequence Number Used when there is more than one record associated with a particular record type. 
Example: Record types 50 and 51 have ten detail records, and consequently ten sequence 
numbers. 
Share Amount This specifies the number of [[shares]] transferred. For full transfers this field may be blank, but 
the acknowledgment must have a value. 
Share/Balance Amount Will contain the balance amount when the Transaction Code = 50, and the transaction 
amount for all other codes. Used when the share/balance amount is less than 16 bytes in 
length. 
Share/Balance Amount 
– Extended 
Contains the balance amount when the Transaction Code = 50, and the transaction amount 
for all other codes. This field is required if the Share/Balance Amount is NOT provided. 
Otherwise it is not allowed. 
This field supports the reporting of omnibus account share balances which exceed the 
billion-share threshold. 
Share/Balance Indicator Indicates the form of [[shares]]: 
1 = book [[shares]], and 
2 = physical [[shares]]. 
Social Code Two-digit number indicating the type of account. 
SSN/EIN Number Indicator Indicator Indicates whether the EIN/SS number is a corporation or individual: 0=Tax I.D. 
Number, and 
1=S.S. Number. 
SWIP (Systematic 
Withdrawal/ Investment 
Plan (F51) 
Indicates the status of the systematic plan on a client’s account (new, modified, closed or 
existing). 
SWP Indicator Specifies a shareowner as a [[participant]] in a Systematic Withdrawal Plan. This provides for 
the automatic [[liquidation]] of [[shares]] according to an agreed upon schedule and amount. 
System Code This field designates the source of transmission: 
• B = Firm 
• F = Fund 
Systematic Contribution 
Indicator 
A pre-authorized check for drafts against a shareholder’s personal bank account for the 
purpose of purchasing fund [[shares]] on a regular basis. 
Formally labeled “PAC Indicator”. 
Systematic Trade Changed 
from (old) Amount 
The dollar amount to be invested or redeemed on a predetermined frequency during the 
course of the calendar year as requested by the client. Investment/Withdrawal frequency is 
defined in the “Systematic trade changed from (old) frequency” and “Systematic trade 
changed to (new) frequency” fields.   
This is used in conjunction with SWIP Indicator on F51 

---

## Page 74

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 74 
 
Field Description 
Systematic Trade Change 
To (new) Amount 
The dollar amount to be invested or redeemed on a predetermined frequency during the 
course of the calendar year as requested by the client. Investment/Withdrawal frequency is 
defined in the “Systematic trade changed from (old) frequency” and “Systematic trade 
changed to (new) frequency” fields. 
This is used in conjunction with SWIP Indicator on F51 
Systematic 
Withdrawal/Contribution 
Effective Date 
Effective date for a systemic withdrawal/contribution. Systemic contributions/withdrawals 
occur for accounts for a set time, such as monthly, quarterly, etc. 
Formerly labeled “SWP/PAC Effective Date.” 
Target Date Fund Indicator Used to enroll in a payment strategy for a target date fund. 
0=No. [[DO]] not enroll 
1-Yes. Firm is telling the T/A to enroll the customer, for a specific SECURITY ISSUE [[ID]], into 
the target date payment. 
A target date fund is a fund whose investment strategy is actively managed toward a specific 
time period. Typically, the investment either gradually moves toward a more conservative 
position, or towards a gradual [[liquidation]] of an investment. 
Total Closing Book Share 
Balance 
Used to recap the Closing Book/Physical Balance field in sequences where the Share 
Balance Indicator = 1 (Book [[shares]]), and where the field length is less than 16 bytes. 
Total Closing Book Share 
Balance–Extended 
Used to recap the Closing Book/Physical Balance field in sequences where the Share 
Balance Indicator = 1 (Book [[shares]]), and where the field length is greater than 16 bytes. 
This field supports the reporting of omnibus account share balances which exceed the 
billion-share threshold. 
Total Physical Share 
Balance 
Used to recap the Closing Book/Physical Balance field in sequences where the Share 
Balance Indicator = 2 (Physical [[shares]]), and where the field length is less than 16 bytes. 
Total Physical Share 
Balance-Extended 
Used to recap the Closing Book/Physical Balance field in sequences where the Share 
Balance Indicator = 2 (Physical [[shares]]), and where the field length is greater than 16 bytes. 
This field supports the reporting of omnibus account share balances which exceed the 
billion-share threshold. 
Transaction Code Use 
1 when transferring to a new account, or 
2 when transferring to an existing account. 
Transaction Description 
Code 
A description code used to further define specific transaction types. 
Transaction Type Used to distinguish between: 
• A sub-account credit (as a result of a Conversion to Networking) 
• A Transfer (from one account to another), or 
• An Account Conversion/Update Acknowledgment (coming from the Fund). 
• Fund Closing 
• Small Balance [[liquidation]] 
• Money Market [[Liquidity]] Fee 
• Short Term Redemption Fee 
• Target Payment Plan 

---

## Page 75

Networking Technical Guide 
 
Chapter 5, Section A–Field Descriptions for Networking Record Layouts 75 
 
Field Description 
Underlying Client's Foreign 
Tax [[ID]] 
Establishes the foreign tax [[ID]] of the underlying client 
Underlying Customer 
Account Number 
Identifies the Customer Account Number (sub-account) at the firm when [[shares]] were held in 
an Omnibus environment. 
Withhold Indicator Describes customer’s tax status. For Conversion there are nine from which to choose. 
Withholding Indicator Used to identify the type of withholding on an activity. 
1=NRA 
2=TEFRA Backup, and 
3=TEFRA Pension. 
Note: 
For Dividends, it indicates either NRA (1) or TEFRA (2). 
Withholding Amount Dollar amount of NRA or TEFRA tax withheld. 
Notes: 
For dividends, the amount is reflected on Records 64 and 66. 
For Record 55, the amount is the tax withheld as a result of trade activity. 
Withholding Rate NRA or TEFRA Rate used to determine the amount of money to be withheld for tax 
purposes. 
 

---

## Page 76

Networking Technical Guide 
 
Chapter 5, Section B–Glossary of Terms 76 
 
CHAPTER 5, SECTION B–GLOSSARY OF TERMS 
Terms and Definitions 
Terms commonly used in Networking are listed alphabetically and defined in the table below. 
Term Definition 
Account Executive An Account Representative or “A.E.” A representative of a Firm assigned to 
handle shareholder accounts. 
Account Maintenance Designates the fields which can be modified on an account. These fields are non- 
financial and consist of 
Dealer of record changes 
A.E. (Account Representative) changes 
[[Dividend]] [[Option]] changes 
Account addresses, and 
Payee address changes. 
Address Changes Allows account address information to be changed on an account registration. 
Firm Capabilities Any transaction that a firm can [[DO]] directly with a Fund. 
Cash to Firm Cash proceeds from dividends and capital gains accrue to the Firm of record. 
Cash to Customer Cash proceeds from dividends and capital gains accrue to the customer. 
Cash to Payee Cash proceeds from dividends and capital gains accrue to the party designated as payee 
on the account’s registration. 
Cash to Trust Cash proceeds from dividends and capital gains accrue to the Trust. 
Check Redemptions A privilege allowing shareholders to use a draft or check against their fund accounts. 
Confirm A statement sent to shareholders, confirming a particular trade to their account. 
Note: 
This is sent for both Fund/SERV and non-Fund/SERV trades. 
Cross Fund Re-Invest Indicates that proceeds from one fund (dividends and capital gains) are to be reinvested 
into another Fund. 
(Dealer) Firm of Record Designates the firm who has the relationship with the shareholder. 
Direct Liquidations A Redemption/[[liquidation]] order placed directly with the Fund by the shareholder and 
bypassing the Firm. 
Direct Purchases Subsequent purchase orders placed directly with the Fund by the shareholder and 
bypassing the Firm. 
Direct Transfers Transfers done directly with the Fund by the shareholder and bypassing the Firm. 

---

## Page 77

Networking Technical Guide 
 
Chapter 5, Section B–Glossary of Terms 77 
 
Term Definition 
[[Dividend]] [[Option]] Code Describes how dividends and capital gains are to be applied. This can either be cash or 
reinvest. 
[[Dividend]] Privileges Designates where monies earned from dividends and capital gains are to be directed. It 
can be to the Firm, the shareholder, the payee or to another Fund account. 
Exchanges A privilege giving the shareholder the ability to exchange [[shares]] between different funds in 
the same family of funds. 
Level Profile of a particular Networking account or group of accounts. Each level has a certain 
combination of characteristics associated with it. 
• Level Zero = Non-Networking Firm Account 
• Level Three = Firm Controlled Firm Account 
• Level Four = Fund Controlled Firm Account 
Note: 
Networked Trust Accounts are considered Level Zero, if accompanied by a 
Membership Indicator of Trust. 
[[liquidation]] Selling of [[shares]] in an account. Also referred to as a Redemption. 
Monthly Statements For certain funds, monthly statements are generated. This statement contains all activity 
for an account. Also included is year-to-date tax information and account balances. 
Ocode A unique four-byte identifier that defines the ‘Originating’ entity that submitted the file to 
[[NSCC]] on behalf of themselves or their underlying client.  
Payee Address Change Allows payee address information to be changed on an account registration. 
Pre-Authorized Check Also called a “PAC.” This privilege allows drafts to be drawn against a shareholder’s bank 
account for the purpose of purchasing fund [[shares]] on a regular basis. 
[[Proxy]] Indicates who has the responsibility for distribution or mailing of proxies. A [[Proxy]] is the 
authority or instrument that permits a shareholder’s voting right to be granted to an agent 
of the shareholder. 
Purchase Buying of [[shares]] in an account. 
Quarterly Statement Produced once every three months. Contains the same information as the monthly 
statements. 
Reporting Responsibility Specifies who has the reporting to the shareholder and/or government on an account. The 
designation is: 
• B= firm (formerly called [[Broker]]), 
• F= fund or 
• C= custodian/trust. 
Shareholder Privileges Shareholder privileges denote the shareholder’s ability to deal directly with the Fund or 
agent for a given activity, privilege or account maintenance [[Option]]. 
Systematic Withdrawal Allows a shareholder to automatically [[Liquidate]] [[shares]] in the account according to an 
agreed upon schedule and amount. Also known as a “SWP.” 
Transfer Movement of [[shares]] between accounts in the same security issue. The new account may 
or may not be registered differently. 

---

## Page 78

Networking Technical Guide 
 
Chapter 5, Section B–Glossary of Terms 78 
 
Term Definition 
W-2P Designed to report retirement payments (other than lump sum distributions) received by 
individuals. 
Year-End Statements Produced at the end of the year to summarize all activity for an account during that period. 
See Monthly Statement. 
529 Plans A 529 plan is a tax-advantaged savings plan designed to encourage saving for future 
college costs, and in certain states, K-12 tuition. 529 plans, legally known as “qualified 
tuition plans,” are sponsored by states, state agencies, or educational [[Institutions]] and are 
authorized by Section 529 of the Internal Revenue Code.  
1042S Reports Non-Resident Alien Taxes. 
1099B Reports sales or redemptions of: 
• [[securities]] 
• Futures transactions 
• Commodities, and 
• Bartering exchange transactions. 
Performed on an individual transaction basis (Wire Orders and Direct Liquidations). 
1099D Reports the following information: 
• Gross dividends and other distributions, and 
• Foreign taxes paid on dividends and other distributions. 
Note: 
Withholdings of any federal income tax under the backup withholding rules are 
applicable to [[Dividend]] distributions. 
1099R Reports distributions to individuals from: 
• Retirement or profit-sharing plans, or 
• An IRA (Individual Retirement Account). 
Note: 
A 1099R is the reporting vehicle used only if the distribution closes the 
recipient’s account. 
5498 Reports the amounts of individual contributions for the taxable year to a(n) 
• IRA (Individual Retirement Account) 
• SEP (Simplified Employee Pension), or 
• DEC (Deductible Voluntary Employee Contribution). 
 

---

## Page 79

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date:  December 29, 2023 
Publication Code: MFS349 
Service: Networking  
Title: Networking Technical Guide 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
  