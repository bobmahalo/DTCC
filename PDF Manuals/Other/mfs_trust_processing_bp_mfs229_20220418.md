---
title: "Trust Processing: Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs_trust_processing_bp_mfs229_20220418.pdf"
pages: 52
size: "748.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Trust Processing: Best Practices

**Original File:** [mfs_trust_processing_bp_mfs229_20220418.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs_trust_processing_bp_mfs229_20220418.pdf)  
**Category:** Other  
**Total Pages:** 52  
**File Size:** 748.4 KB  

---

## Page 1

 
 
 
MUTUAL FUND SERVICES 
TRUST PROCESSING: BEST PRACTICES 
APRIL 18, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: April 18, 2022 
Publication Code: MFS229 
Service: Mutual Fund Services  
Title: Trust Processing: Best Practices 
 
  

---

## Page 3

 
 
HISTORY OF CHANGES 
Dates Changes 
April 18, 2022 Reference link corrected. 
March 2, 2022 Document was rebranded. It’s content was reviewed 
and content refreshed.  
December 5, 2021 Broken links corrected 
July 17, 2020 Broken links corrected 
Effective Date: March 18, 2013 a7472 Dated August 16, 2012 
a7567 Dated January 9, 2013 (revised dates) 
Effective Date: April 23, 2012 Please see Important Notice a7355 & a7356   
Updated: June 2011  
 
 

---

## Page 4

 
 
TABLE OF CONTENTS 
Trust Processing ................................................................................................................................................ 10 
About Trust Processing .....................................................................................................................................10 
Timeline ............................................................................................................................................................10 
Trust Processing Trading ..................................................................................................................................11 
[[settlement]] Process ...........................................................................................................................................12 
Account Scrubbing Process ..............................................................................................................................13 
Field Definitions .................................................................................................................................................13 
Known Facts .....................................................................................................................................................16 
Glossary ............................................................................................................................................................17 
Appendix A. Networking Matrix Levels ............................................................................................................ 19 
About Matrix Level Controls ..............................................................................................................................19 
Definition ..........................................................................................................................................................19 
Description of Networking Matrix Levels ...........................................................................................................19 
Reporting Responsibilities .................................................................................................................................20 
Introduction ......................................................................................................................................................20 
Reporting Responsibilities ................................................................................................................................20 
Beneficial Shareholder Privileges with a Fund ..................................................................................................21 
Introduction ......................................................................................................................................................21 
Beneficial Shareholder Privilege table ...............................................................................................................21 
Firm or Trust Company Capabilities – Activity ..................................................................................................22 
Introduction ......................................................................................................................................................22 
Purpose ...........................................................................................................................................................22 
Capabilities.......................................................................................................................................................22 
Firm or Trust Company Capabilities – Account Maintenance ..........................................................................23 
Introduction ......................................................................................................................................................23 
[[Broker]] or Trust Company Account Maintenance table.......................................................................................23 
[[Dividend]] Privileges ............................................................................................................................................24 
Introduction ......................................................................................................................................................24 

---

## Page 5

 
 
[[Dividend]] Privilege table ....................................................................................................................................25 
Shareholder Privileges ......................................................................................................................................25 
Introduction .....................................................................................................................................................25 
Shareholder Privileges table .............................................................................................................................25 
Appendix B. Establishing [[Broker]]/Dealer Information ..................................................................................... 27 
Establishing [[Broker]]/Dealer Information on New Trust Networked Accounts Setup Via [[NSCC]] ........................27 
Background and Objectives ..............................................................................................................................27 
Scope ................................................................................................................................................................28 
Proposed Best Practices ...................................................................................................................................28 
Additional Information ......................................................................................................................................29 
Trust Processing Scenarios ............................................................................................................................... 30 
Scenario 1: Initial Fund/SERV® Purchases ......................................................................................................30 
Business Scenario ............................................................................................................................................30 
Trust Initiated Transaction ................................................................................................................................30 
Fund/SERV® Method .....................................................................................................................................30 
Networking Method .........................................................................................................................................30 
Fund Response (Fund/SERV®) ........................................................................................................................30 
Fund Response (Networking Method) ...............................................................................................................31 
Trust Processor - Fund/SERV® Example: ........................................................................................................31 
Scenario 2: Subsequent Fund/SERV® Purchases ...........................................................................................32 
Business Scenario ............................................................................................................................................32 
Trust Processor Initiated Transaction ................................................................................................................32 
Fund Response ...............................................................................................................................................32 
Trust Processor Example..................................................................................................................................33 
Scenario 3: Fund/SERV® Purchase Confirmations...........................................................................................33 
Business Scenario ............................................................................................................................................33 
Fund Initiated Transaction ................................................................................................................................34 
Trust Processor Example..................................................................................................................................34 
Scenario 4: Fund/SERV® Full Registrations .....................................................................................................35 
Business Scenario ............................................................................................................................................35 

---

## Page 6

 
 
Trust Processor Initiated Transaction ................................................................................................................35 
Fund Response ................................................................................................................................................35 
Trust Processor Example..................................................................................................................................35 
Scenario 5: T+1 [[settlement]] ..............................................................................................................................37 
Business Scenario ............................................................................................................................................37 
Trust Processor Initiated Transactions ..............................................................................................................37 
¶Scenario 6: Trust Processor Places Fund/SERV® Trade on an Invalid Trust [[ID]] ...........................................37 
Business Scenario ............................................................................................................................................37 
Trust Processor Initiated Transactions ..............................................................................................................37 
Fund Response ...............................................................................................................................................38 
Scenario 7: Trust Processor Places a Fund/SERV® Trade to Settle at Net ....................................................38 
Business Scenario ............................................................................................................................................38 
Trust Processor Initiated Transactions ..............................................................................................................38 
Fund Response ...............................................................................................................................................38 
Scenario 8: Purchase into Trust Processed/[[Broker]] Networked Account .........................................................38 
Business Scenario ............................................................................................................................................38 
Trust Processor Initiated Transactions ..............................................................................................................38 
Fund Response ...............................................................................................................................................39 
Fund/SERV® ..................................................................................................................................................39 
Networking .....................................................................................................................................................39 
Scenario 9: [[Broker]] Initiated Trade on a Trust Processed Account ...................................................................39 
Business Scenario ............................................................................................................................................39 
[[Broker]] Initiated Transaction ..............................................................................................................................40 
Fund Response ...............................................................................................................................................40 
Fund/SERV® ..................................................................................................................................................40 
Networking .....................................................................................................................................................40 
Scenario 10: Trust or TPA Clears Through Another Firm (Service Provider) ...................................................41 
Business Scenario ............................................................................................................................................41 
Trust Initiated Transactions ..............................................................................................................................41 
[[Broker]] Initiated Transactions ............................................................................................................................41 

---

## Page 7

 
 
Fund Response ...............................................................................................................................................41 
Scenario 11: Trust Processor Requests Processing on a [[Broker]] Networked Level 3 Account  .......................41 
Business Scenario ............................................................................................................................................41 
Trust Processor Initiated Transactions ..............................................................................................................42 
[[Broker]] Initiated Transactions ............................................................................................................................42 
Fund Response ...............................................................................................................................................42 
Scenario 12: Trust Processed Account – [[Broker]] Requests Level 3 ................................................................42 
Business Scenario ............................................................................................................................................42 
[[Broker]] Initiated Transactions ............................................................................................................................42 
Trust Processor Initiated Transactions ..............................................................................................................42 
Fund Response: The Fund Should Reject a B52 Sent by the B/D in This Scenario. ..........................................42 
Scenario 13: Non-[[Broker]] Networked/Non-Trust Processed Account to Trust Processing ...............................43 
Business Scenario ............................................................................................................................................43 
[[Broker]] Initiated Transactions ............................................................................................................................43 
Trust Processor Initiated Transactions ..............................................................................................................43 
Fund Response ................................................................................................................................................43 
Scenario 14: Removing an Account from Trust Processing .............................................................................44 
Business Scenario ............................................................................................................................................44 
Trust Initiated Transactions ..............................................................................................................................44 
Fund Response ................................................................................................................................................44 
Scenario 15: Transferring Trust Processed Accounts to Another Trust ............................................................44 
Business Scenario ............................................................................................................................................44 
Receiving Trust Initiated Transactions ..............................................................................................................44 
Delivering Trust Initiated Transactions ..............................................................................................................44 
[[Broker]] Initiated Transactions ............................................................................................................................45 
Fund Response ................................................................................................................................................45 
Scenario 16: Removing the [[Broker]] Matrix Level (De-Network) from a Trust Processed Account ....................45 
Business Scenario ............................................................................................................................................45 
Trust Initiated Transactions ..............................................................................................................................45 
[[Broker]] Initiated Transactions ............................................................................................................................45 

---

## Page 8

 
 
Fund Response ................................................................................................................................................45 
Scenario 17: Changing the [[Broker]]/Dealer of Record on a Trust Processed Account  ......................................46 
Business Scenario ...........................................................................................................................................46 
Trust Initiated Transactions .............................................................................................................................46 
[[Broker]] Initiated Transactions ..........................................................................................................................46 
Fund Response ...............................................................................................................................................46 
Scenario 18: ACAT Transfer Occurs on Trust Processed Account ..................................................................46 
Business Scenario ...........................................................................................................................................46 
[[Broker]] Initiated Transactions ..........................................................................................................................46 
Trust Initiated Transactions .............................................................................................................................47 
Fund Response ...............................................................................................................................................47 
Scenario 19: Cash [[Dividend]]/Capital Gain Payments .......................................................................................47 
Business Scenario ...........................................................................................................................................47 
Trust Initiated Transactions .............................................................................................................................47 
[[Broker]] Initiated Transactions ..........................................................................................................................47 
Fund Response ...............................................................................................................................................47 
Cash Disbursement Indicator to Be Used for Trust Processed Accounts  ......................................................48 
Scenario 20: Reinvested [[Dividend]]/Capital Gains .............................................................................................48 
Business Scenario ...........................................................................................................................................48 
Trust Initiated Transactions .............................................................................................................................48 
[[Broker]] Initiated Transactions ..........................................................................................................................49 
Fund Response ...............................................................................................................................................49 
Scenario 21: Reinvested [[Dividend]]/Capital Gains .............................................................................................49 
Business Scenario ...........................................................................................................................................49 
Trust Initiated Transactions .............................................................................................................................49 
[[Broker]] Initiated Transactions ..........................................................................................................................49 
Fund Response ...............................................................................................................................................49 
Scenario 22: Systematic Withdrawals ...............................................................................................................50 
Business Scenario ............................................................................................................................................50 
Trust Initiated Transactions .............................................................................................................................50 

---

## Page 9

 
 
[[Broker]] Initiated Transactions ..........................................................................................................................50 
Fund Response ...............................................................................................................................................50 
Cash Disbursement Indicator for SWP Activity to be used for Trust Processed and [[Broker]] Networked 
Accounts ..........................................................................................................................................................51 
 

---

## Page 10

Trust Processing: Best Practices 
Trust Processing 10 
TRUST PROCESSING 
About Trust Processing 
The Trust Processing Guidelines document was originally created by the Trust User Group and the ICI 
(Investment Company Institute) Bank, Trust and Retirement Advisory Committee to facilitate the exchange of 
information flowing between bank trust departments and fund groups utilizing [[NSCC]]’s Fund/SERV ® and 
Networking systems.  
Based on the assumption that clients (Trusts, TPA’s and Service Providers) will utilize both the Fund/SERV® and 
Networking systems for processing, the Trust Processing Guidelines offers a “how to” for the benefit of both the 
fund and trust processor’s community to reduce potential multiple processing methods. 
As these guidelines are used to develop a foundation for standardized trust processing, Trusts, TPA’s, Service 
Providers and funds must also develop good channels of communication with each other to understand the 
issues and ensure processing efficiencies.  
Refer to the Defined Contribution Processing Guidelines for detailed information on trade processing for defined 
contribution plans. 
Timeline 
All times are approximate ET for the sample. 
 
Table 1-Sample Life Cycle for Trust Processing Trades through [[NSCC]] * 
 When What By Whom 
Day 1 
Trade Date 
Until Market 
Closes 
Gather trades Bank trust, TPA, service 
provider 
4pm to 6am Trades are transmitted to [[NSCC]] Bank trust, TPA, service 
provider 
Day 2 
Trade Date+1 
3 am to 9am Confirms /rejects are sent to [[NSCC]] to forward to 
Bank/trust 
Funds** 
2 am to 9am Corrections or Firm Exits can be submitted Bank trust, TPA, service 
provider*** 
11:15 am [[settlement]] file sent to appropriate parties [[NSCC]]**** 
approx 4 pm [[settlement]] occurs with [[NSCC]] Bank trust, TPA, service 
provider and Funds 
Night Cycle Trades are posted to T/A and accounting systems Bank trust, TPS, service 
provider and funds 
Day 3  5 am Networking files are sent to Bank/Trust  

---

## Page 11

Trust Processing: Best Practices 
Trust Processing 11 
 When What By Whom 
Trade Date+2 11 am [[NSCC]] creates [[settlement]] records for confirmed trades 
that did not make the previous day's window and were 
not canceled. 
 
* This timeline does not address DCC&S trading. Please refer to the Defined Contribution Processing Guidelines  for this 
information 
** Contact individual  Fund for cycle cut off times 
*** Contact individual  Fund for support of this function with same day [[settlement]] 
**** 005 = Confirmation Record, 006 = Reconfirmation Record, 025 = Correction Confirmation.  
For a complete list of records, please refer to the Fund/SERV® Manual 
 
Trust Processing Trading 
The chart in Figure 1 on the next page illustrates the flow of trust processing activity between the 
bank/trust/TPA/service provider, fund company and the [[Broker]]/dealer (if one exists on the account). If a 
bank/trust or TPA uses the services of a clearing provider (service provider), then the clearing provider will 
perform the activity or receive information for the benefit of the bank/trust or TPA:  
• Fund [[Companies]] that utilize MFPS I (Price & Rate files) will transmit daily fund information to [[NSCC]] who, 
in turn, will transmit them to the bank/trust, TPA or service provider if they are eligible for the service.  
• The bank/trust, TPA or service provider will initiate orders and transmit them to [[NSCC]] for distribution to  
the fund company. Service providers will transmit transactions to [[NSCC]] on behalf of their bank/trust or 
TPA clients. 
• The fund will confirm orders to [[NSCC]] who, in turn, will transmit them to the bank/trust, TPA or service 
provider. 
• [[settlement]] of the orders will take place between [[NSCC]] and the bank/trust, TPA or service provider and 
between [[NSCC]] and the fund.1 
• The fund will transmit Networking files to [[NSCC]], who, in turn, will transmit them to the bank/trust, TPA or 
service provider and [[Broker]]/dealer, if one exists, on the account. 
• Fund [[Companies]] participating in MFPS II [Distribution Declaration-Check definition] will transmit [[Dividend]] 
information to [[NSCC]] who, in turn, will transmit the information to the bank/trust, TPA or clearing provider.  
 
Please note the chart in Figure 1
 displays the [[BASIC]] order flow of a trust processing trade. However, there are 
other Fund/SERV® records that can be passed between [[NSCC]] and clients. For a complete listing of those 
records, please consult the Fund/SERV® Chapter 5 technical manual. 
 
1 If necessary, before [[settlement]] a bank/trust, TPA or service provider may initiate a Fund/SERV® Firm Exit (139) record to cancel the order and remove it 
from the [[settlement]] process. 

---

## Page 12

Trust Processing: Best Practices 
Trust Processing 12 
 
Figure 1-Trust Processing Workflow 
[[settlement]] Process 
[[settlement]] of Fund/SERV® trades will occur as a net debit or credit by client number as part of [[NSCC]]’s net 
[[settlement]] process. The [[NSCC]] combines dollar amounts owed/due as the result of Fund/SERV ®, Networking 
and [[DTCC]] Payment aXis activity as part of their [[settlement]] process. 
 


---

## Page 13

Trust Processing: Best Practices 
Trust Processing 13 
Account Scrubbing Process 
Scrubbing involves reconciling the firm’s positions with the fund’s positions to ensure that the Firm and the Fund 
have identical sub-accounts records.  
 
1. Before processing can begin, a critical, pre-conversion process known as ‘scrubbing’ must be completed by 
the Firm. The term “scrubbing” came from the process of identifying dealer accounts prior to Networking. 
Because of the manner in which fund [[Companies]] may hold accounts on their books, dealers need a 
method of identifying existing fund accounts to solicit for Networking. The process requires funds to go over 
or “scrub” their books to find accounts belonging to a specific dealer.  
2. Identification of trust processing accounts for a given bank/trust, TPA or service provider will vary by fund 
company. The tax identification number (TIN) of the bank/trust, TPA, or service provider is the primary method 
of identification. It is expected that information will be passed back to the bank/trust, TPA or service provider via 
data file, e-mail, or some other manual process, which will vary by fund. 
3. As an [[Option]] a fund can send a scrub file to a firm at the bank trust, TPA or service provider’s request 
for non-financial information on its Networked ac counts. Scrub files are created by using the existing 
Fund Conversion (F51) records with a scrub indicator. Scrub files are sent through the fund conversion 
stream in Networking. Firms may request a scrub file by contacting the fund directly . 
4. Funds need to ensure that customer accounts on their internal systems have the correct dual -party 
networking relationship for the bank trust, TPA  or service provider and [[Broker]]/dealer, when necessary.  
Funds will also need to know  if the trust processor and [[Broker]]/deal er are to receive Networking files.  
5. Depending on the trust processor’s ability to use the [[settlement]] Date Override feature, the fund may 
need to update their Security Issue [[ID]]  profiles at the [[NSCC]] for the settling entity to allow for T+1 
[[settlement]].  
6. It is important to note that completion of the scrubbing process prior to utilizing the [[NSCC]] interface is 
critical to the success of your conversion. Please also note that each fund company may have 
additional requirements from the ones listed above. Please cont act your various fund [[Companies]] prior 
to beginning the scrubbing process. Also, please reference the following  
7. Networking Manuals available on the Learning Center  for further information on the scrub process:  
• Pre-Networking Scrubbing information is available in the Technical Networking guide  on the 
Learning Center at:   https://dtcclearning.com/products-and-services/mutual-fund-
services/networking.html Information within this guide  includes Conversion Processing, Activity, 
Position and [[Dividend]] processing information as well as Matrix Levels, Reporting Responsibilities, 
Shareholder Privileges, Firm or Trust Company Privileges and Reject Codes. 
 
• Networking Scrub File Overview and Best Practices on the Learning Center at 
https://dtcclearning.com/products-and-services/mutual-fund-
services/networking.html#resources 
 
Field Definitions 
The following field definitions relate to Trust Processing within the Fund/SERV® and Networking systems. It is 
not, however, an all-inclusive list.  

---

## Page 14

Trust Processing: Best Practices 
Trust Processing 14 
Originator Type - This field indicates the originating entity of a transaction. Available values are: 
• A = Investment Agent   
• B = Firm  
• T = TPA  
• S = Service Provider for B = Firm  
• P = Service Provider for T = TPA 
• V = TPP (Third Party Provider) 
 
Firm Number - This field identifies the 4-digit [[NSCC]] client number assigned to the trust. 
[[settlement]] Override Reason Code – This field is required if the Anticipated [[settlement]] Date is provided. This 
field will provide an explanation as to why the submitting entity is requesting to change the preset [[settlement]] 
date. A value of 03 = Other should be used in this field. 
Customer Account Number at F irm - Typically this field will be left blank on an initial purchase. On a 
subsequent purchase this field may contain the account number as maintained by the bank trust, TPA or 
service provider. The information provided will be transmitted back on the Fund Confirmation (005) record. 
Fund [[Companies]] may elect to maintain a cross-reference of this number and the fund account number on their 
internal systems. Please consult with your fund families. 
Customer A
 ccount Number at Fund – This field should always be populated with relevant information. This 
field should contain the account number at the fund as it is referenced when identifying the account to be traded 
on and may be necessary for the trade to be executed. Please consult with your individual fund families. This 
field may be blank for an initial purchase as the account number will not be known unless the account was 
established earlier. 
Agent fo r  Firm/Executing Firm - This field indicates the identifying symbol/number of the [[Broker]]/dealer. This 
symbol/number may be the [[Broker]]/dealers [[NSCC]] client number (if they are a [[NSCC]] [[Member]]), the firms [[OTC]] 
symbol or the fund’s internal identifier for the [[Broker]]/dealer. The [[NSCC]] does not require firms identified in this 
field to be members. The [[OTC]] symbol can be found in the [[NSCC]] the [[DTCC]] website under [[NSCC]] [[Member]] 
Directories (see [[NSCC]] MPID Directory) at https://www.[[DTCC]].com/client-center/[[NSCC]]-directories 
Networking-Control Indicator – This field may contain a value of [0] Non-Networked. 
[[Dividend]]-Code - This field, in conjunction with the “Payable Information Indicator” field will determine how  
dividends are paid. For instance, if dividends and capital gains are to be paid in cash, then this field will contain 
a value ‘0’. 
Payable I nformation Indicator - This field, in conjunction with the “[[Dividend]] Code”, will determine how 
dividends are paid. If cash dividends and/or capital gains are to be paid to the Address of Record, then this 
field will contain a value of ‘0’ and proceeds will be paid by check. If this field contains a value of ‘5’ (Cash to 
Trust), then the proceeds will be paid via Networking. 
If cash dividends and/or capital gains are to be paid to the shareholder or to a third party, then this field will 
contain a value of ‘1’ (Payable Address) and the associated payable address information would be provided 
beginning with record #9 (401 Full Registration record). 

---

## Page 15

Trust Processing: Best Practices 
Trust Processing 15 
Membership Identifier – This field identifies the type of entities involved and determines the level of detail they will 
receive in their Networking files. This field holds one of three values. 
• Bank/Trust – [01] (Clearing Providers also use a value of 01) 
• [[Broker]]/Dealer or Insurance Company – [blank] 
• TPA – [02] 
 
Gross [[settlement]] Indicator – This required field should be completed appropriately as it indicates to the fund 
whether the trade is to settle gross, net or if the indicator is not applicable.  
Anticipated [[settlement]] Date – T his optional conditional field is required if the [[settlement]] Override Reason 
Code is provided. This field will contain the T+1 date of [[settlement]] for the order. This field should only be used 
if the trust processor has not established an alternate [[settlement]] cycle with the fund.  
Branch Identification Number – T his field will contain the identifier, as assigned by the corresponding dealer 
firm, of the branch assigned to the account. 
Social Code – T his field can contain multiple values. For a complete list of the codes please refer to the social 
code listing located in the documentation section of the learning center at: https://dtcclearning.com/products-
and-services/mutual-fund-services/codes.html  Please consult with your fund families before choosing a code. 
For more information, see Known Facts. 
Account Representative Number – This field will contain the identifier, as assigned by the corresponding 
dealer firm, of the representative assigned to the account. 
Account Representative Name – T his field will contain the name of the representative assigned to the 
account. 
NAV Reason Code - T his Fund/SERV® field indicates whether any commission monies are due on the 
purchase amount. In Networking, the name of this field is the NAV Account Indicator and its use is different. 
The NAV Reason Code of “Trust Company NAV per Agreement” will more accurately communicate the 
business reason for a trust company obtaining NAV on a transaction or account. The value reflects a NAV 
price due to an agreement between a bank/trust and a fund family. 
[[Asset]] Type Indicator – T his field helps give a specific classification of transactions submitted in Fund/SERV. 
For a complete list of the [[Asset]] Type Indicator’s please refer to the Fund/SERV® codes on Learning site. Firms 
are advised to contact their fund partners to determine which of the codes are allowed by each of the funds.  
 
Please note 
In order to process a Share Class Conversion, the Bank/Trusts normally submit redemptions & subscriptions through the 
[[NSCC]]/DCC&S. These trades are processed as subscriptions and redemptions and should include the [[Asset]] Type Indicator 
of “G” (Share Class Conversion). 
Bank/Trusts that hold an Omnibus account with Fund [[Companies]] and process Share Class Conversions are to 
identify these transactions via the Fund/SERV® order placement process. This is accomplished by inputting a 

---

## Page 16

Trust Processing: Best Practices 
Trust Processing 16 
“G” (Share Class Conversion) indicator within Record Position 160, [[Asset]] Type Indicator field on the 
Fund/SERV® Order Record. 
Following this process will allow Fund [[Companies]] to utilize the “G” indicator to accurately report redemptions 
and subscriptions when pertaining to a Share Class Conversion. 
Short-Term Redemption Fee - This field enables firms and funds to process and settle STRs more efficiently. 
Known Facts 
1. [[NSCC]] edits all required and optional fields for correct values and rejects any transactions found to contain 
invalid data. Please reference Fund/SERV® and Networking record layouts for required and conditional 
fields on the Learning Center https://dtcclearning.com/products-and-services/mutual-fund-services.html 
2. . Trusts and service providers must submit their records with the Membership Identifier of ‘01’ (Trust) and 
Network Control Indicator of ‘0’ (Non-[[Broker]] Networked) to participate in Trust Processing. 
3. TPA’s must submit their record with the Membership Identifier of “02” (TPA) and Network Control Indicator 
of “0” (Non-[[Broker]] Networked) to participate in Trust Processing. 
4. The preferred method of communication between trusts, TPAs or service providers and funds is the fund 
account number. 
5. The fund account number can be up to 20 alphanumeric characters and must be sent left justified.  
6. The preferred method of [[settlement]] for trust processing transactions is “Gross” [[settlement]].  
7. [[NSCC]] provides an extensive list of "Social Codes". Trust processors should use codes that indicate to the 
fund that the trust processor will handle the tax reporting. The following are the most commonly used 
codes: 42 (Institutional Trust-fully disclosed), 07 (Financial [[Institutions]]-Bank/Trust Omnibus), 12 (non-
prototype 401k-plan level), 17 (Self Directed IRA-non-prototype), 19 (non-prototype 403b- plan level) and 
20 (non-prototype 457b-plan level 0) should be used for trust accounts. 
8. Funds will be required to send Networking Position Files independently to trust processors and 
[[Broker]]/dealers according to each entity’s internal schedules. 
9. Trust networked accounts are known as “network level 0”. The network level defines the roles and 
responsibilities of the entities involved. 
10. The “Customer Account Number at Firm” (BIN) field will typically be left blank on an initial purchase. On a 
subsequent purchase this field may contain the plan number as maintained by the trust processor. The 
information provided will be transmitted back on the Fund Confirmation (005) record. Fund [[Companies]] 
may elect to maintain a cross-reference of this number and the fund account number on their internal 
systems. Please consult with your fund families. 
11. The fund should not allow the trust processor to change the [[Broker]]/dealer’s networking matrix level.  
12. [[Broker]]/dealers can Network Trust Processing accounts at level 4. Depending on the fund’s policy, the 
fund response is either to reject or suspend the trade if submitted with an incorrect level code. If rej ected, 
a Fund Reject (100) record should be submitted. Funds can suspend trades by delaying confirmation until 
the issue can be resolved. 
13. Trust processing will not be allowed on [[Broker]] level 3 accounts. 
14. On trust processed/[[Broker]]/dealer networked accounts, the fund will report activity via Networking when an 
account balance at the fund changes. Fund/SERV
® activity will be reported as “direct” activity to the non-
submitting party. 

---

## Page 17

Trust Processing: Best Practices 
Trust Processing 17 
15. The trust processor can receive cash dividends via Networking [[Dividend]] [[settlement]] by indicating a 
“Payable Information Indicator” of ‘5’ (Cash to Trust) and not sending payable information on the 
registration (401) record or B50 record in Networking. Funds will send [[Broker]]/dealers non- [[settlement]] 
[[Dividend]] records if account is dual networked but not paying to the [[Broker]]/dealer. 
16. Trust processed accounts coded with cash distributions will be paid as “cash to trust” through Networking 
[[Dividend]] [[settlement]] unless there is a special payee on the account. 
17. The [[Broker]]/dealer can receive cash dividends via Networking [[Dividend]] [[settlement]] by indicating a 
“Payable Information Indicator” of ‘1’ (Cash to [[Broker]]). Funds will send trust processors non- [[settlement]] 
[[Dividend]] records if it is also a trust processed account. 
18. On subsequent trades, the “Agent for Firm”, the “Account Representative Number” and the “Branch 
Identification Number” can contain ‘spaces’ if the Membership Identifier = 01 (Trust [[Member]]/Service 
Provider) or 02=TPA. 
19. If a trust processor receives a Networking Fund Maintenance Record (F51) with only the “Customer 
Account Number at Fund” field and the “Clearing/Settling [[Broker]] Number” field populated, it is an 
indication that the account was updated by the fund and is now trust networked.  
20. Fund families may require that data fields be populated differently. If there is any uncertainty as to how to 
populate a field, you should contact your fund family for clarification. 
Glossary 
 
 
Table 2-Glossary 
Glossary Explanation 
ACATS Automated Customer Account Transfer Service automates and standardizes transfer of assets 
in a customer account from one brokerage firm to another. 
Agent for Firm 
(Fund/SERV®) 
Refers to the [[Broker]]/dealer associated with a trust Executing Firm (NETWORKING) mutual fund 
account. This number is usually one of three identifiers, the [[OTC]] symbol, the [[NSCC]] [[Member]] 
number or a fund created number 
Clearing/Settling 
[[Broker]] Number 
Refers to the [[NSCC]] Client Number of a firm that is initiating a Networking transaction De-
Network To remove from Networking and from receiving Networking information. 
[[OTC]] Symbol Over The Counter. A firm’s [[OTC]] numbers can be obtained on the mutual fund services web site. 
Firm Refers to any submitting party, which could be a bank trust, TPA, service provider or 
[[Broker]]/dealer. 
Fund Any mutual fund company client. 
Membership Identifier Field in Fund/SERV® and Networking records identifies records initiated by Trusts when 
populated with “01”. 
Client/[[participant]] 
Number 
The four-digit [[NSCC]] assigned number associated with that client/[[participant]]. 
Trust [[Member]] 
Number 
Field on every account that will carry the [[NSCC]] assigned 4-digit number assigned to the trust. 
The trust will populate the Firm field (Fund/SERV®) and Clearing/Settling Firm field 
(NETWORKING) with this number. 

---

## Page 18

Trust Processing: Best Practices 
Trust Processing 18 
Glossary Explanation 
Trust Processed 
Account 
Any account coded for trust processing. Membership identifier coded “01” and Networking level 
0 will indicate trust processing. The Trust will receive Networking information. 
[[Broker]] Networked 
Account 
Any account which carries a matrix code 3 or 4 and a [[Broker]] Identification Number (BIN). The 
[[Broker]]/dealer will receive Networking information. 
Dual-Networked 
Account 
An account, which is BOTH [[Broker]] Networked at level 4 and Trust Processed. [[Broker]] level 3 
accounts are excluded from trust processing. Underlying Firm Symbol This field allows 
firms/fund to identify an underlying [[intermediary]], creating further transparency. 
Underlying Firm 
Symbol 
This field allows firms/fund to identify an underlying [[intermediary]], creating further transparency. 
 
 
 

---

## Page 19

Trust Processing: Best Practices 
Appendix A. Networking Matrix Levels 19 
APPENDIX A. NETWORKING MATRIX LEVELS 
About Matrix Level Controls 
Networking offers several levels of reporting, each one referencing different levels of account responsibilities for 
Firms and Funds. Each matrix level: 
• Provides Firms with the flexibility to select options consistent with their business philosophy.  
• Identifies the: 
o Reporting responsibilities of the Firm and Fund with regard to each sub-account. 
o Processing capabilities the Fund and Firm have in supporting the exchange of information for those 
sub-accounts. 
 
Note 
Levels of responsibility and user privileges can be changed depending on the specific needs of the Firms and Fund 
[[Companies]]. 
Definition 
The matrix level is the level of control on a sub-account provided to a Firm or Fund using Networking. The 
matrix level chosen by the Firm determines the activity allowed between the shareholder and the Fund.  
There are three current matrix levels: 
• Level Zero = Non-Networked Account or a Networked Trust Account when used in conjunction with a 
Trust Membership Indicator 
• Level Three = Firm Controlled Account 
• Level Four = Fund Controlled Account 
Description of Networking Matrix Levels 
Table 3 describes each of the three matrix levels of Networking. 
Table 3-Networking Matrix Levels 
Networking 
Level 
Name Description 
0 (zero) Non-Networked 
Account 
For most Firms, Level 0 means non-Networked. 
Exception: A Networked Trust Account is considered Level 0 if the 
Membership Indicator denotes a Trust. 

---

## Page 20

Trust Processing: Best Practices 
Appendix A. Networking Matrix Levels 20 
Networking 
Level 
Name Description 
3 (three) Firm Controlled 
Account 
Firms maintain maximum control over the mutual fund assets in a 
customer’s account including: 
• all customer contact information 
• orders 
• customer statements 
• tax reporting 
Note:  
Customers [[DO]] not deal directly with the fund. 
4 (four) Fund Controlled 
Account 
Firms allow the fund to maintain control over the mutual fund assets in a 
shareholder’s account. 
Firms process a customer’s orders, but the Fund provides all other 
services for the shareholder including all accounting and tax reporting. 
Shareholders can deal with either the Firm or the Fund. 
Trust Networked 
Account 
Trust Company 
Controlled Account 
Trust Company maintains maximum control over the mutual fund assets in 
a customer’s account including: 
• all customer contact information 
• orders 
• customer statements 
• tax reporting 
Note:  
Customers [[DO]] not deal directly with the fund. 
 
Reporting Responsibilities 
Introduction 
This topic contains information on shareholder reporting responsibilities. 
Reporting Responsibilities 
Table 4 illustrates who is responsible for: 
• Producing confirmations 
• Preparing monthly and quarterly statements 
• Tax reporting for investors 
 
 

---

## Page 21

Trust Processing: Best Practices 
Appendix A. Networking Matrix Levels 21 
Table 4-Reporting Responsibilities 
Reporting Responsibility Level Three Level Four Trust Networked ** 
Confirm (Fund/SERV® Trades) Firm Fund Trust Company 
Confirm (Non-Fund/SERV®) Firm Fund Trust Company 
Monthly Statements Firm Fund Trust Company 
Quarterly Statements Firm Fund Trust Company 
Year-End Statements Firm Fund Trust Company 
1099D Firm Fund Trust Company 
1099B (Wire Orders) Firm Fund (as-of 1/1/2012) Trust Company 
1099B (Direct Liquidations)  Firm Fund Trust Company 
1099 R/W2P (When Applicable)  Custodian/ Trustee Custodian/ Trustee Trust Company 
5498 (When Applicable)  Custodian/ Trustee Custodian/ Trustee Trust Company 
1042S Firm Fund Trust Company 
Proxies Firm/Fund Fund Trust Company 
Interested Party Mailings Firm Fund Trust Company 
* Direct Liquidations  are not allowed. 
** Trust Networked accounts at the fund should not be subject to withholding. If withholding is appropriate, it should be 
applied by the trust on the trust's record-keeping system. The trust is responsible for filing and reporting. 
 
 
Notes 
"Custodian" is defined as the financial  institution acting as the caretaker for a mutual fund’s assets. 
The tables found in this chapter should be used as a guideline.  They are not a requirement  of [[NSCC]]. They are the 
recommendations  set forth by the clients of the Networking system themselves.  
 
Beneficial Shareholder Privileges with a Fund 
Introduction 
This topic contains information on the beneficial shareowner privileges with a Fund. 
Beneficial Shareholder Privilege table 
Table 5 illustrates the shareholder privileges that are available for the various Networking levels. 

---

## Page 22

Trust Processing: Best Practices 
Appendix A. Networking Matrix Levels 22 
Table 5-Beneficial Shareholder Privilege 
Beneficial Shareholder Privileges with Fund Level Three Level Four Trust Networked ** 
Direct Purchases No Yes No 
Direct Purchases No Yes No 
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
** For Trust Networked Accounts, “No” means that only the Trust Company can process the privileges  listed. 
 
Firm or Trust Company Capabilities – Activity 
Introduction 
This topic contains information on Firm or Trust Company capabilities - activity. 
Purpose 
Table 6 below illustrates the [[BASIC]] functions that Firms or Trust [[Companies]] (for Trust Networked Accounts) can 
and cannot [[DO]] under the various levels of Networking. 
These functions include: 
• Purchases 
• Liquidations 
• Exchanges 
• Transfers 
Capabilities 
Firm or Trust Company (for Trust Networked Accounts) capabilities are summarized in Table 6. 

---

## Page 23

Trust Processing: Best Practices 
Appendix A. Networking Matrix Levels 23 
 
Table 6-Purpose Capabilities 
Function Type Level Three Level Four Trust Networked 
Purchases Direct with Fund No Yes Yes 
Fund/SERV® Yes Yes Yes 
Liquidations  Direct with Fund No Yes Yes 
Fund/SERV® Yes Yes Yes 
Exchanges Direct with Fund No Yes Yes 
Fund/SERV® Yes Yes Yes 
Transfers Direct with Fund No Yes Yes 
Fund/SERV® Yes Yes Yes 
 
Firm or Trust Company Capabilities – Account Maintenance 
Introduction 
This topic contains information on Firm or Trust Company capabilities regarding account maintenance. 
[[Broker]] or Trust Company Account Maintenance table 
There are several non-trade related functions in Networking. Table 7 illustrates which of these non-trade 
related functions Firms can perform under the various levels of Networking. These include:  
• Dealer of record changes 
• Account executive changes 
• [[Dividend]] [[Option]] changes 
• Address changes 
• Payee address changes 
 
Table 7-[[Broker]] or Trust Company Account Maintenance 
Function Type Level Three Level Four Trust  
Networked 
Dealer of Record Changes Firm through Networking No Yes No 
Trust Company through Networking N/A No Yes 
Firm to Fund Direct No Yes No 
Trust Company to Fund Direct N/A No Yes 
Fund through Networking No Yes Yes* 

---

## Page 24

Trust Processing: Best Practices 
Appendix A. Networking Matrix Levels 24 
Function Type Level Three Level Four Trust  
Networked 
Account Executive Changes Firm through Networking Yes Yes Yes 
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
Payee Address Changes Firm through Networking Yes Yes No 
Trust Company through Networking N/A No Yes 
Firm to Fund Direct No Yes No 
Trust Company to Fund Direct N/A No Yes 
Fund through Networking No Yes No 
Mass Dealer Change (branch, 
account executive) 
Fund through Networking Yes Yes Yes* 
* Notification of a change made to the dealer/branch/representative information on a Trust Networked account by the 
Fund must be sent to the Trust via an F51 Fund Acknowledgement. 
 
[[Dividend]] Privileges 
Introduction 
This topic contains information on [[Dividend]] privileges. 

---

## Page 25

Trust Processing: Best Practices 
Appendix A. Networking Matrix Levels 25 
[[Dividend]] Privilege table 
Table 8 indicates the [[Dividend]] privileges available to the shareholder under the various Networking levels. 
 
Note 
"Shareholder" in this instance does not mean the Trust Company but its clients. 
 
 
Table 8-[[Dividend]] Privilege 
Privilege Level Three Level Four Trust Networked 
Cash to Firm Yes Yes No 
Cash to Trust Yes Yes Yes 
Cash to Shareholder  No Yes No 
Cash to Payable Party  Yes Yes Yes 
Cross Fund Re-Invest Yes Yes Yes 
 
Shareholder Privileges 
Introduction 
This topic contains information on shareholder privileges. 
Shareholder Privileges table 
Table 9 indicates the availability of the privileges shareholders have under the various Networking levels. 
 
Table 9-Shareholder Privilege 
Shareholder Privileges with Fund Level Three Level Four Trust Networked 
Direct Purchases Yes Yes Yes 
Direct Liquidations  Yes Yes Yes* 
Direct Exchanges Yes Yes Yes* 
Direct Transfers Yes Yes Yes* 
Check Redemptions Yes Yes Yes* 
Systematic Withdrawals Yes** Yes Yes* 
Pre-authorized Checks Yes Yes Yes* 
Dealer of Record Changes Yes Yes Yes 
Account Executive Changes Yes Yes Yes 

---

## Page 26

Trust Processing: Best Practices 
Appendix A. Networking Matrix Levels 26 
Shareholder Privileges with Fund Level Three Level Four Trust Networked 
[[Dividend]] [[Option]] Changes Yes Yes Yes* 
Address Changes Yes Yes Yes* 
Payee Address Changes Yes Yes Yes* 
* Only the Trust Company can process the privileges listed directly with the fund. 
** Yes, if “Cash to Firm/Cash to Trust” and requested by the [[Broker]]/Dealer. 
*** Yes, if “Cash to Firm/Cash to Trust” and requested by the [[Broker]]/Dealer. 
 
Caution:  
Whenever there is a change in matrix levels, it carries with it the loss of all privileges associated with the prior matrix level 
and gain of all privileges associated with the new matrix level. 
 
 

---

## Page 27

Trust Processing: Best Practices 
Appendix B. Establishing [[Broker]]/Dealer Information 27 
APPENDIX B. ESTABLISHING [[Broker]]/DEALER 
INFORMATION 
The appendix includes additional information about establishing [[Broker]]/dealer information on a Trust 
Networked account using the B50 or 401 records through the [[NSCC]]. This may require manual follow-up to 
ensure accurate set-up. 
Establishing [[Broker]]/Dealer Information on New Trust Networked 
Accounts Setup Via [[NSCC]] 
Background and Objectives 
Banks, Trust [[Companies]], and TPA’s can open new accounts with fund [[Companies]] via [[NSCC]] Networking using 
B50 records and via Fund/SERV® using 401 records. When these accounts are opened on behalf of a 
[[Broker]]/Dealer, it is important to get accurate dealer / branch / rep coding on these accounts. Accurate coding 
supports various processes at the fund including: 
• Commission payments and reporting 
• 12b-1 payments and reporting 
• Internet account access and statements (for example, Vision or Advisor Central) 
• E lectronic data feeds (for ex, [[NSCC]] files), 
• V arious other internal processes at the fund company 
 
[[NSCC]] allows the [[OTC]] symbol to be used to identify a Dealer when the Dealer does not have an [[NSCC]] number 
Inherently, the Banks, Trusts, and TPA’s are at a disadvantage as they [[DO]] not always know the various branch and 
rep code formats used by the different B/D’s. It is also common for [[Broker]]/Dealers to request changes to these 
codes directly with the Fund [[Companies]], so the Funds can help communicate along to the Intermediaries, when 
appropriate. 
The objective of this best practice is to promote and enhance communication between the Intermediaries and 
Fund [[Companies]] by providing  a “Day 2” communication that can be used by the fund [[Companies]] to review 
and update dealer / branch / rep coding on new accounts and communicate changes back to the 
Intermediaries.  
The addition of the Underlying Firm Symbol field on the Networking and Fund/SERV® new account records 
allows the firm and fund to identify the underlying firm.  
Please refer to the Learning Center for additional information on the Underlying Firm Symbol including a current list 
of firms, User Guide and request form https://dtcclearning.com/products-and-services/mutual-fund-services/mfs-
cross-products/underlying-firm-symbols-ufs.html 

---

## Page 28

Trust Processing: Best Practices 
Appendix B. Establishing [[Broker]]/Dealer Information 28 
Scope 
This document provides a recommended process and suggested detail for providing Day 2 information 
between Intermediaries and Fund [[Companies]]. 
Proposed Best Practices 
Intermediaries establish new accounts via Networking B50 and receive an acknowledgement record bac k from 
the fund (F53) when the account is established containing the fund account number. They can also establish a 
new account via Fund/Serv 401 record and receive an acknowledgement back from the fund (112) when the 
account is established which contains the fund account number. 
Typically, the account at the fund is established with the dealer / branch / rep info provided on the [[NSCC]] 
records. However, if the information is invalid or inaccurate, the fund will either use internal [[default]] coding or 
just use the invalid information on the account. 
On Day 2, the [[intermediary]] can send a communication via e-mail or fax containing the recommended 
information below (and if using e-mail, standard security / encryption controls should be in place). The Fund 
[[Companies]] can use this info to verify and update the data on the recently established accounts. If an update to 
an account is necessary, the fund company should determine the cause and address. For example: 
• If the correct dealer was not assigned, review and update an [[NSCC]] or [[OTC]] cross reference.  
• If the incorrect [[NSCC]] or [[OTC]] was provided, or if it was omitted, update and communicate to the 
[[intermediary]]. 
• If the branch code was invalid, correct it and communicate back to the [[intermediary]]. If it was just new to 
the fund, then add, update, and communicate. 
• If the rep code was invalid, correct it and communicate back to the [[intermediary]]. If it was just new to the 
fund, then add, update, and communicate. 
 
Communication back to the Intermediaries is necessary in order to help in providing more accurate information 
on future accounts. This communication is provided via [[NSCC]] F51 record sent to the [[intermediary]]. 
Intermediaries should review and update this information accordingly on their internal systems.  
In addition to the new account process, fund families routinely get requests to maintain dealer / branch / rep 
information directly from the [[Broker]]/Dealer community. A common example occurs when a rep is terminated or 
moves from one Dealer to another. The Dealer will send a request to the fund to assign the accounts from the 
old rep to a new rep. Another example is when a Dealer converts to a new branch an d / or rep code format. 
As the funds process these types of requests, a Networking F51 record should be sent to the [[intermediary]]. 
Intermediaries should review and update this information accordingly on their internal systems. It is important 
that the fund [[Companies]] review each type of maintenance that can be performed and verify that an F51 record 
is sent out on a Trust Networked account. Some examples are individual manual account level updates, mass 
move type events, and other system generated maintenances that can be caused by conversion activity.  

---

## Page 29

Trust Processing: Best Practices 
Appendix B. Establishing [[Broker]]/Dealer Information 29 
Recommended information for Day 2 communication from Intermediaries to Funds:  
• Account Open Date 
• [[settlement]] Issue [[ID]] 
• Fund Name 
• Fund Account number 
• [[Broker]] / Dealer Name 
• [[Broker]] / Dealer [[ID]] # ([[NSCC]] #, [[OTC]] Symbol) 
• Branch [[ID]] number 
• Rep Name 
• Rep [[ID]] Number 
• Rep Address (street, city, state, zip) 
 
Additional Information that can be helpful: 
• TPA name 
• UFS [[ID]] 
• Plan name 
o [[Asset]] Type / Social Code 
o NAV Type / Pricing 
Additional Information 
• Account Relationship Managers are available to provide information and respond to inquiries concerning 
[[NSCC]]’s mutual fund services.  You can reach Mutual Fund Services at 212-855-8877. 
• General information on [[NSCC]]’s mutual fund and other services is also available on [[NSCC]]’s corporate 
website at www.[[DTCC]].com. 
   
 

---

## Page 30

Trust Processing: Best Practices 
Trust Processing Scenarios 30 
TRUST PROCESSING SCENARIOS 
Scenario 1: Initial Fund/SERV® Purchases 
Business Scenario 
The trust processor submits an initial purchase transaction.  
Trust Initiated Transaction 
The establishment of accounts can be set up either through Networking or Fund /SERV®. The two methods 
are described below. 
Fund/SERV® Method 
The first method allows trade orders to be submitted on the same day as the establishment of the account. 
Trust processors should submit a Fund/SERV® Order with a Transaction Code of ‘01’ (initial purchase) 
followed by a Fund/SERV® Full Registration (401). In this scenario, the “Fund Account Number” will not be 
provided by the trust processor because it has not been assigned by the fund.  
Networking Method 
The second method would be used to establish new accounts at least one day prior to submitting trade order s. 
Trust processors should submit Networking New Account (B50) records to establish the account. Trust 
processors will receive the fund account number in the Customer Account Number At Fund field of the 
Networking Fund Acknowledgment (F53). Upon receipt of the Fund Account Number, the trust processor 
should submit a Fund/SERV® Order (001) with a Transaction Code of ‘02’ (subsequent purchase). Please 
refer to Subsequent Fund/SERV® Purchase. 
Fund Response (Fund/SERV®) 
The fund will respond by sending either a Confirmation (005) record or a Fund Reject  (100) record. 
Upon receipt of the Full Registration (401) record, the fund will assign a fund account number and confirm that 
number in the “Customer Account Number” field on the Registration Acknowledgment (112) record. In addition, 
the “Customer Account Number Indicator” will contain a value of ‘1’ (Fund). 
The fund account number assigned will be used by the trust processor for all subsequent activity submitted for 
the account. However, subsequent activity on the day following an initial purchase may require special 
handling because the trust processor may have yet to receive the Registration Acknowledgment (112) record 
containing the fund account number. 
 

---

## Page 31

Trust Processing: Best Practices 
Trust Processing Scenarios 31 
 
Fund Response (Networking Method) 
Funds will respond to the Networking account set-up by sending a Fund Acknowledgment (F53) record. 
The fund will respond to the order by sending either a Confirmation (005) record or a Fund Reject (100) record 
through Fund/SERV®. See Fund Response under Subsequent Fund/SERV® Purchase. 
Trust Processor - Fund/SERV® Example: 
A customer purchases 100.000 [[shares]] of Fund Company B - Growth Fund. The [[Broker]]/dealer of record on the 
account is Dealer C. The following offers a sample of how the Fund/SERV® Order (001) record (fixed-length 
format) may appear for this order: 
Where: 
• Trust Processor A [[NSCC]] [[Member]] Number = 3795  
• Fund Company B Fund Clearing Number = 5119 
• Fund Company B - Growth Fund Security [[ID]] = 937251803  
• Trade Date = 01/15/YYYY 
• S ettlement Date = 01/16/YYYY 
• Dealer C [[NSCC]] [[Member]] Number or [[OTC]] Symbol = ABCD  
• Dealer C Branch = AWY0 
• Dealer C Representative Number = AWY236  
• Dealer C Representative Name = LEMON 
 
 
Please note 
If a [[Broker]] is associated with the account the agent for firm, branch [[ID]], account rep number and account rep name should 
be completed. Otherwise, these fields are blank. Please see Appendix B for more information regarding setting up 
[[Broker]]/dealer information via a B50 or 401 record. 
 
 
Table 10-Field or Behavior 
Field or Behavior Trust Processor Submits an Initial Purchase 
Originator Type* B [Firm] 
Firm Number 3795 
Record Type 001 
Fund Number 5119 
Control Number 379557280000001  
Trade Date 0115YYYY 
[[settlement]] Over Reason 03 [Other] 

---

## Page 32

Trust Processing: Best Practices 
Trust Processing Scenarios 32 
Field or Behavior Trust Processor Submits an Initial Purchase 
Customer Account Number Fund blank 
Agent Firm Number Optional 
Network Control Indicator 0 
Gross [[settlement]] Indicator 2 [Gross] 
Membership [[ID]]** 01 [Trust [[Member]]] 
Anticipated [[settlement]] Date 0116YYYY 
Branch [[ID]] Number Optional 
Social Code 42 [Institutional Trust] 
Account Representative Number Optional 
Account Representative Name Optional 
* Originator Type values should align with the actual Trust Processing entity type: 
• B=Firm 
• T=TPA 
• S=Service Provider for Firm (B) 
• P=Service Provider for TPA (T) 
** Membership [[ID]] value of “01” should be used by Trusts and Service Providers; “02” for TPA’s. 
 
Please refer to the Fund/SERV® System Processing Manual for all required and optional field definitions.  
Scenario 2: Subsequent Fund/SERV® Purchases 
Business Scenario 
The trust processor submits a subsequent purchase transaction. 
Trust Processor Initiated Transaction 
A Fund/SERV® Order (001) record is transmitted to the receiving fund with a “Transaction Code” value of ‘02’ 
(Subsequent Purchase). The trust processor will always provide the fund account number for subsequent 
purchase activity. All other required and optional fields should be coded accordingly. Refer to Field Definitions 
for more detail. 
Fund Response 
The fund will respond by sending either a Confirmation (005) record or a Fund Reject (100) record. 
 
 
Please note 
A Fund/SERV® short registration record (400) must be submitted with a subsequent purchase. 

---

## Page 33

Trust Processing: Best Practices 
Trust Processing Scenarios 33 
 
 
Trust Processor Example 
A customer purchases 100.000 additional [[shares]] of Fund Company C - Balanced Fund. Fund Company C is a 
no-load mutual fund group. The following pages offer a sample of how the Fund/SERV® Order (001) record 
(fixed-length format) may appear for this order: 
Where: 
• Trust Processor A [[NSCC]] Firm Number = 3795  
• Fund Company C [[NSCC]] Fund Number = 5119 
•  Fund Company C - Balanced Fund Security [[ID]] = 937251803  
• Fund Account Number = 61542228 
 
Table 11-Field or Behavior 
Field or Behavior Trust Submits a Subsequent Purchase 
Originator Type B [Firm] 
Firm Number 3795 
Record Type 001 
Fund Number 5119 
Control Number 379557280000001  
Trade Date 0115YYYY 
[[settlement]] Over Reason 03 [Other] 
Cust Acct Number Fund 61542228 
Agent Firm Number blank 
Network Control Indicator 0 
Gross [[settlement]] Indicator 2 [Gross] 
Membership [[ID]] 01 [Trust [[Member]]] 
Anticipated [[settlement]] Date 0116YYYY 
Branch [[ID]] Number Optional 
Social Code 42 [Institutional Trust] 
Account Representative Number blank 
Account Representative Name blank 
 
Scenario 3: Fund/SERV® Purchase Confirmations 
Business Scenario 
Fund accepts trust processor Fund/SERV® Order Purchase. 

---

## Page 34

Trust Processing: Best Practices 
Trust Processing Scenarios 34 
Fund Initiated Transaction 
If the Fund/SERV® Order Purchase (new or subsequent) is accepted by the fund, a Fund/SERV® Order 
Confirmation (005) record will be generated and transmitted back to the trust processor on either trade date or 
trade date+1. 
Trust Processor Example 
A customer purchases 100.000 [[shares]] of Fund Company B - Growth Fund. The [[Broker]]/dealer of record on the 
account is Dealer C. The following offers a sample of how the Fund/SERV® Confirmation (005) record (fixed-
length format) may appear for this order: 
Where: 
• Trust Processor A [[NSCC]] Firm Number = 3795  
• Fund Company B [[NSCC]] Fund Number = 5119 
• Fund Company B - Growth Fund Security [[ID]] = 937251803  
• Dealer C [[NSCC]] [[Member]] Number or [[OTC]] Symbol = ABCD  
• Dealer C Branch = AWY0 
• Dealer C Representative Number = AWY236  
• Dealer C Representative Name = LEMON 
 
Table 12-Fields or Behavior 
Field or Behavior Fund Confirmation 
Originator Type F [Fund] 
Firm Number 3795 
Record Type 005 
Fund Number 5119 
Control Number Same as Original Order 
Trade Date Same as Original Order 
[[settlement]] Over Reason 03 [Other] 
Customer Account Number Fund blank 
Agent Firm Number blank 
Network Control Indicator 0 
Gross [[settlement]] Indicator 2 [Gross] 
Membership [[ID]] 01 [Trust [[Member]]] 
Anticipated [[settlement]] Date Same as Original Order 
Branch [[ID]] Number AWYO 
Social Code 42 [Institutional Trust] 
Account Representative Number blank 
Account Representative Name blank 

---

## Page 35

Trust Processing: Best Practices 
Trust Processing Scenarios 35 
Scenario 4: Fund/SERV® Full Registrations 
Business Scenario 
The trust processor submits registration information for an initial purchase transaction. 
Trust Processor Initiated Transaction 
A Fund/SERV® Full Registration (401) record is transmitted to the receiving fund with the initial purchase 
transactions. The trust processor could also submit a B50 record to establish the account one or more 
business days before the initial purchase. All required and optional fields should be coded accordingly. Please 
note that a Fund/SERV
® Short Registration (400) record should be transmitted to the fund with subsequent 
purchases.  Refer to the Field Definitions section for more detail. 
Fund Response 
The fund will respond by sending a Registration Acknowledgment (112) record.  
Upon receipt of the Full Registration, the fund will establish the new account.  
Please note 
This response will only occur if the registration is set-up through Fund/SERV®. Consult with your fund family as they may 
allow other registration set-ups. 
 
Trust Processor Example 
A customer purchases 100.000 [[shares]] of Fund Company B - Growth Fund. The [[Broker]]/dealer of record on the 
account is Dealer C. The following pages offer a sample of how the Fund/SERV ® Full Registration (401) 
record (fixed-length format) may appear for this order: 
Where: 
• Trust Processor A [[NSCC]] Firm Number = 3795  
• Fund Company B [[NSCC]] Fund Number = 5119 
• Fund Company B - Growth Fund Security [[ID]] = 937251803  
• Trade Date = 01/15/97 
• S ettlement Date = 01/16/97 
• Dealer C [[NSCC]] [[Member]] or [[OTC]] Symbol = ABCD (leave blank if no specific dealer requested on account) 
• Dealer C Branch = AWY0 
• Dealer C Representative Number = AWY236  
• Dealer C Representative Name = LEMON 
 
 

---

## Page 36

Trust Processing: Best Practices 
Trust Processing Scenarios 36 
Please note 
If a [[Broker]] is associated with the account the agent for firm, branch [[ID]], account rep number and account rep name should 
be completed. Otherwise, these fields are blank. Please see Appendix B. on page 27 for more information regarding 
setting up [[Broker]]/dealer information via a B50 or 401 record. 
 
Table 13-Fields or Behavior 
Field or Behavior Trust Submits a Registration 
Originator Type B [Firm] 
Firm Number 3795 
Record Type 401 
Fund Number 5119 
Control Number Same as the Order 
Submission Date 01/15/YYYY 
Customer Account Number  blank 
Customer Account Number  Indicator blank 
Agent Firm Number ABCD 
Network Control Indicator 0 
[[Dividend]] Code Choose most appropriate code for account set-up 
Payable Indicator Choose most appropriate code for account set-up 
Social Code 42 [Institutional Trust] 
Account Representative Name Lemon 
Account Representative Number blank 
Branch Identification Number blank 
 
  

---

## Page 37

Trust Processing: Best Practices 
Trust Processing Scenarios 37 
Scenario 5: T+1 [[settlement]] 
Business Scenario 
Trust processor places a trade through Fund/SERV® to be settled on T+1. 
Trust Processor Initiated Transactions 
There are three methods of processing T+1 [[settlement]] trades. 
A preferred method would require the trust processor to be set up on the fund’s [[NSCC]] Security [[ID]] profile with 
an alternate [[settlement]] cycle of T+1 for all transactions. Please contact your trading partner to discuss this 
[[Option]]. This is the best practice. 
The second method would be to use the [[settlement]] date override feature. This method requires the trust to 
submit the T+1 [[settlement]] date in the “Anticipated [[settlement]] Date” field along with a value of ‘03’ (Other) in 
the “[[settlement]] Date Override Reason Code” field. 
The third method would require the fund to change or establish their [[NSCC]] Security [[ID]] profile to indicate T+1 
[[settlement]] for all transactions for all firms. 
Note 
If the Security [[ID]]/ fund [[Member]] is already set up for T+1 [[settlement]] at [[DTCC]], no further action is required. 
 
 
¶Scenario 6: Trust Processor Places Fund/SERV® Trade on an Invalid 
Trust [[ID]] 
Business Scenario 
Trust processor places a trade on an account, which does not carry the same trust [[ID]] ([[NSCC]] Firm Number) as 
indicated on the order. 
Trust Processor Initiated Transactions 
There are two scenarios where the trust processor places a trade in an account to which they have no trust 
processing relationship. In the first scenario, a trust processor places a trade on an account, which has a different 
trust [[ID]]. The second is where there is no trust [[ID]] on the account into which the trade is being placed. 

---

## Page 38

Trust Processing: Best Practices 
Trust Processing Scenarios 38 
Fund Response 
Depending on the fund’s policy, the fund response in both scenarios is either to reject or suspend the trade. If 
rejected, a Fund Reject Record (100) should be submitted with a reject code of ‘008’ (firm number missing or 
invalid). Funds can suspend trades by delaying confirmation until the issue can be resolved. 
Scenario 7: Trust Processor Places a Fund/SERV® Trade to Settle at 
Net 
Business Scenario 
Trust processor submits a Fund/SERV order with a “Gross [[settlement]] Indicator” of ‘01’ (net).  A trust processor 
would choose this [[Option]] if they wanted to retain commissions on a trade. However, the best  practice is for a 
Trust Processor to settle gross (Gross [[settlement]] Indicator of ‘02’). 
Trust Processor Initiated Transactions 
The Fund/SERV Order (001) would contain a “Gross [[settlement]] Indicator” of ‘01’ and a “Membership Identifier” 
of ‘01’ (Trust/Service Provider) or “2” (TPA).  
Fund Response 
The preferred method is to confirm all trust processor-initiated transactions with a “Gross [[settlement]] Indicator” 
of ‘02’ (gross) and the “Amount Due” field adjusted to reflect gross [[settlement]].  The NS CC [[settlement]] is based 
on the value in the “Amount Due” field. 
An alternative method would be to settle the trade at net as indicated. 
Scenario 8: Purchase into Trust Processed/[[Broker]] Networked 
Account 
Business Scenario 
Trust processor places a trade for an account identified as Trust Processed and [[Broker]] Networked. This is 
considered a dual-networked account and it is treated the same as a single networked account. A trust 
processed account cannot be dual networked to a [[Broker]]/dealer level 3 account. 
Trust Processor Initiated Transactions 
The trust processor submits a Fund/SERV® Order (001) transaction instructing the fund to purchase dollars or 
[[shares]] into a trust account. All required and optional fields should be coded accordingly. 

---

## Page 39

Trust Processing: Best Practices 
Trust Processing Scenarios 39 
Fund Response 
Fund/SERV® 
Funds will either confirm or reject orders submitted by trust processors. The fund uses Fund/SERV ® 
Confirmation (005) records to accept transactions and Fund/SERV® Reject (100) records to reject them. 
Please consult the [[NSCC]] Fund/SERV® Processing Manual for a complete listing of all required and optional 
fields on the Confirmation (005) and Reject (100) transactions. 
Networking 
After settling the transaction to the shareholder’s account, the fund will transmit Networking Activity (F55) 
closing balance records to both the trust processor and [[Broker]]/dealer of record. Funds, most usually, update 
shareholder accounts upon receipt of the Fund/SERV® Registration (400/401) records. Networking Activity 
(F55) records are, most usually, transmitted the morning after the fund updates the shareholder’s account.  
Table 14 illustrates the necessary Networking Activity (F55) records for the fund to transmit:  
 
Table 14-Networking Activity (F55) records 
Transaction Type Description Send to Trust Processor Send to [[Broker]] 
01 Direct Purchase    
50 Closing Balance Record     
 
As illustrated in Table 12, the trust receives only a Closing Balance Record (Transaction Type = 50). The 
[[Broker]]/dealer, however, receives a Direct Purchase (Transaction Type = 01) and a Closing Balance Record 
(Transaction Type = 50). 
Networking Activity (F55) records generated for the trust processor should contain the four -digit [[Member]] 
number assigned by the [[NSCC]] to the trust in the “Clearing/Settling [[Broker]] Number” field. Records generated 
for the [[Broker]]/dealer should contain the 4-digit [[Member]] number assigned by the [[NSCC]] to the [[Broker]]/dealer in 
the “Clearing/Settling [[Broker]] Number” field. 
Please visit the Networking section of mutual fund products to reference the F55 record layouts for the most 
recent version of the Activity (F55) record to see some required and optional fields on the Activity (F55) record 
at  https://dtcclearning.com/products-and-services/mutual-fund-services/networking.html 
Scenario 9: [[Broker]] Initiated Trade on a Trust Processed Account 
Business Scenario 
The [[Broker]]/dealer places a trade for an account identified as trust processed. In this scenario, the account is 
NOT networked by the [[Broker]]/dealer. 

---

## Page 40

Trust Processing: Best Practices 
Trust Processing Scenarios 40 
[[Broker]] Initiated Transaction 
The [[Broker]]/dealer submits a Fund/SERV® Order (001) transaction instructing the fund to purchase dollars or 
[[shares]] into a trust processed account. While this is not the preferred method of the trust processing 
company; it may be possible for a [[Broker]]/dealer to place a trade on their account. It will not matter if the 
account is dual-networked or not; the initiating party will be responsible for [[settlement]]. 
 
Please note 
In this scenario, it may not be possible for funds to recognize that a [[Broker]] has placed a trade in a trust-processed account. 
It is important for the trust processor and the [[Broker]] to establish mutually agreed upon trading practices to avoid confusion. 
Fund Response 
Fund/SERV® 
Funds will either confirm or reject orders submitted by [[Broker]]/dealers. The fund uses Fund/SERV ® 
Confirmation (005) records to accept transactions and Fund/SERV® Reject (100) records to reject them. 
Please consult the [[NSCC]] Fund/SERV® Processing Manual for a complete listing of all required and optional 
fields on the Confirmation (005) and Reject (100) transactions. 
Networking 
After settling the transaction to the shareholder’s account, the fund will transmit Networking Activity (F55) 
records to the trust. Funds usually update shareholder accounts upon receipt of the Fund/SERV ® Registration 
(400/401) records. Networking Activity (F55) records are, most usually, transmitted the morning after the fund 
updates the shareholder’s account. 
Table 15
 on the next page illustrates the necessary Networking Activity (F55) records for the fund to transmit 
when the [[Broker]]/dealer is networked. If the [[Broker]]/dealer is not networked, they will not receive a record:  
Table 15-Networking Activity (F55) records 
Transaction Type Description Send to Trust Processor Send to [[Broker]] 
01 Direct Purchase    
50 Closing Balance Record     
 
As illustrated in Table 15, the trust receives a Direct Purchase (Transaction Type = 01) and a Closing Balance 
Record (Transaction Type = 50). Activity (F55) records are not sent to the [[Broker]]/dealer because the account  is 
not [[Broker]]/dealer Networked. 
Networking Activity (F55) records generated for the trust processor should contain the 4- digit [[Member]] number 
assigned by the [[NSCC]] to the trust processor in the “Clearing/Settling [[Broker]] Number” field.  

---

## Page 41

Trust Processing: Best Practices 
Trust Processing Scenarios 41 
Please visit the Networking section of mutual fund products to reference the F55 record layouts for the most 
recent version of the Activity (F55) record to see some required and optional fields on the Activity (F55) record 
at  https://dtcclearning.com/products-and-services/mutual-fund-services/networking.html 
Scenario 10: Trust or TPA Clears Through Another Firm (Service 
Provider) 
Business Scenario 
A trust uses a clearing firm to initiate and settle their Fund/SERV® activity. 
Trust Initiated Transactions 
The clearing firm (service provider) is responsible for initiating trust Fund/SERV® activity. In this scenario, the 
clearing firm will act as the trust processor. As such, the clearing firm must comply with all of the trust -initiated 
scenarios outlined in this document. 
The underlying trust or TPA may be populated in the Underlying Firm Symbol field on the new account record. 
The underlying Trust may have to sign agreements with the fund. The account may have the clearing firm’s 
[[Broker]]/dealer or an outside [[Broker]]/dealer on the account. 
Please refer to the other scenarios this document contains for details on trust-initiated transactions. 
[[Broker]] Initiated Transactions 
The [[Broker]] should not initiate a trade through networking in this scenario it should come from the trust processor. 
Fund Response 
Funds should respond to transactions initiated by a clearing provider as if submitted by the underlying 
trust/TPA itself. 
Please refer to the other scenarios this document contains for details on fund responses to trust initiated 
transactions. 
Scenario 11: Trust Processor Requests Processing on a [[Broker]] 
Networked Level 3 Account 
Business Scenario 
Trust processor wants to process on a [[Broker]]/dealer Networked level 3 account.  (Networking level 3 must be 
removed.) 

---

## Page 42

Trust Processing: Best Practices 
Trust Processing Scenarios 42 
Trust Processor Initiated Transactions 
The trust processor will submit a Networking New Account Set-up (B50) to establish a new account with the 
appropriate [[Broker]]/dealer information.  
[[Broker]] Initiated Transactions 
After the new account has been established, the [[Broker]] will submit a Networking Account Transfer (B52) record 
to transfer the [[shares]] to the new account. 
Fund Response 
The fund will send an Acknowledgment (F53) record in response to the Networking Account Transfer (B52) 
record. 
Scenario 12: Trust Processed Account – [[Broker]] Requests Level 3 
Business Scenario 
Trust processed account exists; [[Broker]]/dealer wants to network level 3. (Transfer must occur to a new 
account.) 
[[Broker]] Initiated Transactions 
The [[Broker]]/dealer will send a Networking New Account Setup (B50) record indicati ng level 3 and then contact 
the trust processor to have the trust processor submit a Networking Account Transfer (B52) record.  
Trust Processor Initiated Transactions 
The trust processor will submit the Networking Account Transfer (B52) record.  
Fund Response: The Fund Should Reject a B52 Sent by the B/D in This Scenario. 
In response to the [[Broker]]/ dealer-initiated Networking New Account Setup (B50) record the fund will send the 
[[Broker]]/dealer a Networking Acknowledgment (F53) record acknowledging the setup of the new -networked 
account. The new account will NOT be eligible for trust processing.  
In response to the B52  submitted by the trust processor, the fund will send an Activity Detail (F55) record to 
the trust processor indicating that the share position for the original account has reached zero.  
 

---

## Page 43

Trust Processing: Best Practices 
Trust Processing Scenarios 43 
Please note 
[[Fiduciary]] responsibilities associated with ownership of trust accounts may conflict with firm instructions to Network certain 
Trust Processed accounts at matrix level 3. Firms should consult with the Trust processor prior to initiating these 
transactions. Funds may process or reject these requests based on individual fund procedures. Also, be aware that a new 
matrix level 3 account may have to be set-up manually. Please consult your fund families to discuss this matter. 
Scenario 13: Non-[[Broker]] Networked/Non-Trust Processed Account to 
Trust Processing 
Business Scenario 
Trust processor has decided to begin trust processing on an existing non-[[Broker]]/dealer networked/non-trust 
processed account. 
[[Broker]] Initiated Transactions 
N/A 
Trust Processor Initiated Transactions 
 
Please note 
In most cases for this scenario, the trust processor has acquired a new customer and is looking to move the account into a 
standard processing environment. It is most likely that the fund will require authorization from the [[Beneficial Owner]] of the 
account before this action will be completed. 
The trust processor can send a Networking New Account (B50) record to establish a new account. When the 
account has been established, the trust processor can submit a manual transfer request with authorization 
documentation acceptable to the fund to move the [[shares]] to the new account. 
As an alternative method the trust processor may be able to send a Networking Account Maintenance (B51) 
record with their [[NSCC]] assigned trust [[Member]] number in the “Clearing/Settling [[Broker]]” field, “Membership 
Identifier” of ‘01’ (trust/service provider) or “2” TPA, and a “Network Control Indicator” of ‘0’ (Non- [[Broker]] 
Networked). However, not all funds may accommodate a Networking Account Maintenance (B51). This 
process may be manual, please consult your fund families. 
Fund Response 
The “Membership Identifier” of ‘01’ (trust/service provider) or “2” TPA and a “Network Control Indicator” of ‘0’ 
(Non-[[Broker]] Network) indicates to the fund that the account should now be trust processed.  
The fund should send a Networking Acknowledgment Record (F53) indicating addition of the “Membership [[ID]]” 
and trust/TPA [[Member]] number. 

---

## Page 44

Trust Processing: Best Practices 
Trust Processing Scenarios 44 
Scenario 14: Removing an Account from Trust Processing 
Business Scenario 
The trust processor has lost the trust account and needs to remove the account from Trust Processing. 
Trust Initiated Transactions 
The trust must contact the fund to remove the account from trust processing. The request  must occur outside 
the Networking system. 
Fund Response 
The fund should respond to the request by removing the account from trust processing. The best practice 
should be to transfer the [[shares]] to a new account that is not trust processed, as there will usually be a new 
registration including a new tax [[ID]]. 
Scenario 15: Transferring Trust Processed Accounts to Another Trust 
Business Scenario 
The trust processor has sold a branch to another trust. The existing accounts are trust processed, and the 
receiving trust also wants trust processing. 
Receiving Trust Initiated Transactions 
The receiving trust will send a Networking New Account Setup (B50) record with their [[NSCC]] assigned trust 
[[Member]] number in the “Clearing/Settling [[Broker]]” field, “Membership Identifier” of ‘01’(trust), and a “Network 
Control Indicator” of ‘0’ (Non- [[Broker]] Networked). 
Delivering Trust Initiated Transactions 
The delivering trust will send a Networking Account Transfer (B52) record with a “Transaction Type” of ‘4’ 
(mass [[Broker]]-to-[[Broker]] conversion). The delivering trust’s [[NSCC]] [[Member]] number should be used in the 
“Clearing/Settling [[Broker]] Number” field and the receiving trust’s [[NSCC]] [[Member]] number in the “Receiving Firm 
Clearing/Settling Number”, and a “Membership Identifier” of “01” (trust). This is considered special processing 
by the fund and they should be contacted prior to sending these transactions.  
 
Please note 
In this scenario there will probably be multiple fund families involved and coordination will be difficult at best. Typically, funds will 
receive transfer paperwork from the trust to process these manually. 

---

## Page 45

Trust Processing: Best Practices 
Trust Processing Scenarios 45 
[[Broker]] Initiated Transactions 
N/A 
Fund Response 
The fund should respond to the Networking New Account (B50) record with a Fund Acknowledgment (F53) 
record to the receiving trust. 
The fund will respond to the delivering trust’s Networking Account Transfer (B52) record with a Fund 
Acknowledgment (F53) record. Since the receiving account is trust processed, an Activity Detail (F55) record 
will be sent to the receiving trust to report the transfer and closing balance. The receiving trust’s [[NSCC]] 
[[Member]] number should be placed in the “Clearing/Settling [[Broker]] Number” field of the Activity Detail (F55) 
record. If either account is also dealer networked, the transfer and closing balance should be reported to the 
networked [[Broker]]/dealer using Activity Detail (F55) records. 
The [[Broker]]/dealer Network Control Indicator should not carry over to the “to” account. 
Scenario 16: Removing the [[Broker]] Matrix Level (De-Network) from a 
Trust Processed Account 
Business Scenario 
The [[Broker]]/dealer needs to de-network an account that is trust processed. 
Trust Initiated Transactions 
N/A 
[[Broker]] Initiated Transactions 
The [[Broker]]/dealer sends a Networking Maintenance (B51) record using the [[Broker]]/dealer’s  [[NSCC]] [[Member]] 
number in the “Clearing/Settling [[Broker]] Number” field, a “Membership Identifier”  of ‘spaces’ ([[Broker]]), and a 
“Network Control Indicator” of ‘0’ (non-[[Broker]] networked). 
Fund Response 
The fund should respond to the request with a Networking Fund Acknowledgment (F53) record to the 
[[Broker]]/dealer. The account remains trust processed. The [[Broker]]/dealer remains on the account at networking 
level 0. 

---

## Page 46

Trust Processing: Best Practices 
Trust Processing Scenarios 46 
Scenario 17: Changing the [[Broker]]/Dealer of Record on a Trust 
Processed Account 
Business Scenario 
A trust processor receives a request to change the dealer of record on the trust -processed account. 
Trust Initiated Transactions 
The trust processor send a Networking Account Maintenance (B51) record using the trust’s [[NSCC]] [[Member]] 
number in the “Clearing/Settling [[Broker]] Number” field, a “Membership Identifier” of ‘01’ (trust/service provider) 
or “2” TPA, and a “Network Control Indicator” of ‘0’ (non-[[Broker]] networked). The new [[Broker]]/dealer should be 
identified in the “New/Contra [[Broker]] of Record” field on record #9. As previously noted, this number will be the 
[[Broker]]/dealer’s [[NSCC]] client number (if they are an [[NSCC]] [[Member]]), the firms [[OTC]] symbol or the fund’s 
internal identifier for the [[Broker]]/dealer. If the [[Broker]] dealer does not have an [[NSCC]] or [[OTC]] number,  then a 
B51 should not be utilized. 
[[Broker]] Initiated Transactions 
N/A [Because of [[Fiduciary]] liability, [[Broker]]/dealer should not attempt to change the [[Broker]]/dealer of record on a 
trust processed account.] 
Fund Response 
If the Networking Account Maintenance (B51) record was submitted by the trust processor the fund should 
maintenance the account to change the [[Broker]]/dealer of record. If it was submitted by the [[Broker]]/dealer the 
fund should reject the request. If the [[Broker]]/dealer is manually changed by the fund, a F51 record should be 
sent to the trust from the fund. 
Scenario 18: ACAT Transfer Occurs on Trust Processed Account 
Business Scenario 
A customer has decided to move their account relationship from a trust processor to a  [[Broker]]/dealer. 
[[Broker]] Initiated Transactions 
[[Broker]]/dealer initiates ACAT transfer. 

---

## Page 47

Trust Processing: Best Practices 
Trust Processing Scenarios 47 
Trust Initiated Transactions 
The trust processor may reject the ACAT transfer if there has been no notification from the [[Beneficial Owner]] of 
the account. If notification has occurred, the trust processor will complete the ACAT Transfer in Kind form with 
the assets to be transferred. In many cases in this scenario the ACAT transfer will include multiple assets held 
at multiple locations. 
Fund Response 
When a trust processor is utilizing the ACAT service, the fund will transfer the account based upon the ACAT 
instructions to the new [[Broker]]/dealer. 
Please note 
The trust processor will validate the change of relationship moving the account to the [[Broker]]/dealer with the customer 
before processing the ACAT transfer. 
Scenario 19: Cash [[Dividend]]/Capital Gain Payments 
This scenario applies to Trust Processed Accounts. 
Business Scenario 
A cash [[Dividend]] and/or capital gain is paid by the fund on an account, which is Trust Processed, but is not 
networked by the [[Broker]]/dealer. In this case, the trust will receive the payout information in the Networking 
[[Dividend]] Records and the [[settlement]] obligation through [[NSCC]]’s Money [[settlement]] System. In this scenario, 
no information needs to be sent to the [[Broker]]/dealer. 
Trust Initiated Transactions 
N/A 
[[Broker]] Initiated Transactions 
N/A 
Fund Response 
A Networking [[Dividend]] Header (F61/F62) record referencing the trust [[Member]] number in the “Clearing/Settling 
[[Broker]] Number” field should be sent by the fund to the trust, followed by a [[Dividend]] Detail (F63/F64) record for 
the account. 
The [[Dividend]] Detail (F63/F64) record should contain the fund account number in the “Firm/Fund Identification 
# ” field, a “Network Control Indicator” of ‘0’ (non-[[Broker]] Networked), and a “Cash Disbursement Indicator” of ‘6’ 
(cash to trust) to report [[settlement]]. 

---

## Page 48

Trust Processing: Best Practices 
Trust Processing Scenarios 48 
This distribution amount will settle through [[NSCC]]’s Money [[settlement]] System. The attached table indicates the 
appropriate “Cash Disbursement Indicator” based on the payable information, distribution, and intended 
recipient of the distribution record. 
Appropriate [[Dividend]] Trailer (F68, 69 and 70) records must also be included. 
Cash Disbursement Indicator to Be Used for Trust Processed Accounts 
 
Table 16-Disbursement Type 
Account Payable Info 
Indicator Cash to 
Firm 
Cash to 
Customer 
Cash to 
Payable 
Cross-Fund 
Reinvest 
1099 
Update 
Cash to Trust 
(Service Provider 
or TPA) 
0=Address of Record      6 
1=Payable Address   3    
2=ACH   3    
3=Cash to Firm N/A      
4=Cross Fund Reinvest    4   
 
Cash Disbursement Indicators: 
• Cash to Firm (1) 
• Cash to Customer (2) 
• Cash to Payable (3) 
• Cross-fund Reinvest (4) 
• 1099 Update (5) 
• Cash to Trust (6) 
Scenario 20: Reinvested [[Dividend]]/Capital Gains 
This scenario applies to Trust Process Accounts. 
Business Scenario 
A [[Dividend]] and/or capital gain is paid by the fund on a reinvest account which is Trust Processed; but is not 
networked by the [[Broker]]/dealer. In this case, the trust processor will receive the reinvested [[Dividend]] 
information in the Networking [[Dividend]] Records.  In this scenario, no information needs to be sent to the 
[[Broker]]/dealer. 
Trust Initiated Transactions 
N/A 

---

## Page 49

Trust Processing: Best Practices 
Trust Processing Scenarios 49 
[[Broker]] Initiated Transactions 
N/A 
Fund Response 
A Networking [[Dividend]] Header (F61/F62) record referencing the trust (service provider/TP A) [[Member]] number 
in the “Clearing/Settling [[Broker]] Number” field should be sent by the fund to the trust, followed by a [[Dividend]] 
Detail (F65/66/67) record for the account. The [[Dividend]] Detail Record should contain the fund account number 
in the “Firm/Fund Identification #” field and a “Network Control Indicator” of ‘0’ (non-[[Broker]] Networked). 
Appropriate [[Dividend]] Trailer (F68, 69 and 70) records must also be included. 
Scenario 21: Reinvested [[Dividend]]/Capital Gains 
This scenario applies to Trust Processed and [[Broker]]/dealer Networked Accounts.  
Business Scenario 
A [[Dividend]] and/or capital gain is paid by the fund on a reinvest account which is Trust Processed and is also 
Networked by the [[Broker]]/dealer (Level 4). In this scenario, both the trust processor and the [[Broker]]/dealer will 
receive the reinvested information in the Networking [[Dividend]] Records. 
Trust Initiated Transactions 
N/A 
[[Broker]] Initiated Transactions 
N/A 
Fund Response 
A Networking [[Dividend]] Header (F61/62) record referencing the trust (service provider/TPA) [[Member]] number in 
the “Clearing/Settling [[Broker]] Number” field should be sent by the fund to the trust processor, followed by 
[[Dividend]] Detail (F65/66/67) records for the accounts. The [[Dividend]] Detail Record should contain the fund 
account number in the “Firm/Fund Identification #” field and a “Network Control Indicator” of ‘0’ (non- [[Broker]] 
Networked). Appropriate [[Dividend]] Trailer (F68/69/70) records must also be included.  
A second [[Dividend]] Header (F61/F62) record referencing the [[Broker]]/dealer number in the “Clearing/Settling 
[[Broker]] Number” field should be sent by the fund to the [[Broker]]/dealer, followed by a Detail record for the 
account. The [[Dividend]] Detail (F65/66/67) record should contain the BIN and the Network Control Indicator.  
Appropriate [[Dividend]] Trailer (F68/69/70) records must also be included. 

---

## Page 50

Trust Processing: Best Practices 
Trust Processing Scenarios 50 
Scenario 22: Systematic Withdrawals 
Business Scenario 
A systematic withdrawal is processed by the fund on an account which is Trust Processed and Networked by 
the [[Broker]]/dealer (Level 4) and [[settlement]] is to be processed through [[NSCC]] to the [[Broker]]/dealer or trust 
processor. In this scenario, the settling party (trust/service provider/TPA or [[Broker]]/dealer) will receive the 
payout information in the Networking Activity (F55) Records and the [[settlement]] obligation through [[NSCC]]’s 
Money [[settlement]] System. The non-settling party will receive information only record from the fund. 
Please note 
Some fund families may not allow systematic withdrawals. 
Trust Initiated Transactions 
N/A 
[[Broker]] Initiated Transactions 
N/A 
Fund Response 
A Networking Activity Detail (F55) record with a “Transaction Type” of ‘14’ (SWP) should be sent to the settling 
party (trust, service provider, TPA or [[Broker]]/dealer) by the fund. An additional Activity Detail Record should be 
sent to the non-settling party for informational purposes only. Activity Records with a “Transaction Type” of ‘50’ 
(closing balance records) and Activity Trailer (F56) records should be sent to both parties.  
The attached table indicates the appropriate “Cash Disbursement Indicator” based on the payable information, 
distribution, and intended recipient of the distribution record ([[Broker]]/dealer or trust processor).  
For [[settlement]] to the trust processor, the Activity Detail Record sent to the trust processor for each account 
should contain the trust/service provider/TPA [[Member]] number in the “Clearing/Settling [[Broker]] Number” field, 
the fund account number in the “Firm/Fund Identification Number” field, a “Network Control Indicator” of ‘0’ 
(non-[[Broker]] Networked), and a “Cash Disbursement Indicator” of ‘6’ (cash to trust) to indicate [[settlement]].  
A second Activity Detail Record should be sent to the [[Broker]]/dealer with the [[Broker]]/Dealer [[Member]] number, 
[[Broker]] identification number, the Network Control Indicator associated with the account, and a “Cash 
Disbursement Indicator” of ‘2’ (cash to customer) to provide distribution information only and indicate to the 
[[Broker]]/dealer that [[settlement]] was to the trust processor. Activity (closing balance) and Trailer Records also 
should be sent to the trust processor and [[Broker]]/dealer. 
When [[settlement]] is made to the [[Broker]]/dealer, the Activity Detail Record sent to the [[Broker]]/dealer should have 
the [[Broker]]/dealer [[Member]] number, BIN number, Network Control Indicator, and a “Cash Disb ursement 
Indicator” of ‘0’ (cash to [[Broker]]-[[settlement]] through [[NSCC]]) to indicate [[settlement]]. 

---

## Page 51

Trust Processing: Best Practices 
Trust Processing Scenarios 51 
A second Activity Detail Record should be sent to the trust processor using the trust/service provider/TPA 
[[Member]] number, fund account number, a Network Control Indicator of ‘0’ (non-[[Broker]] Networked), and a 
“Cash Disbursement Indicator” of ‘1’ (cash to firm) to provide distribution information only and indicate 
[[settlement]] to the [[Broker]]/dealer. Activity (closing balance) and Trailer Records also should be sent to the trust 
processor and [[Broker]]/dealer. 
Cash Disbursement Indicator for SWP Activity to be used for Trust Processed 
and [[Broker]] Networked Accounts 
 
Table 17-Disbursement Type 
Account Payable  Info 
Indicator 
 
Cash to B/D 
(for 
[[settlement]])* 
 
Cash to 
B/D 
Cash to 
Customer 
Cash to 
Payable 
Cross-Fund 
Reinvest 
1099 
Update 
Cash to 
Trust** 
0=Address of Record   2 (B)    6 (T) 
1=Payable Address    3 (B)(T)    
2=ACH    3 (B)(T)    
3=Cash to Firm 0 (B) 1 (T)      
4=Cross Fund Reinvest     4 (B)(T)   
* - will result in [[settlement]] to the [[Broker]]/dealer 
** - will result in [[settlement]] to the trust 
B - Networking record intended for [[Broker]]  
T - Networking Record intended for Trust 
 
 
 

---

## Page 52

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 