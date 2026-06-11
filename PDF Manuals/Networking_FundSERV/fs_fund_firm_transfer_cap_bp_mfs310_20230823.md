---
title: "ACATS-Fund/SERV® - Fund/Firm (PTF) Transfer Capability – Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_fund_firm_transfer_cap_bp_mfs310_20230823.pdf"
pages: 40
size: "1100.7 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# ACATS-Fund/SERV® - Fund/Firm (PTF) Transfer Capability – Best Practices

**Original File:** [fs_fund_firm_transfer_cap_bp_mfs310_20230823.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_fund_firm_transfer_cap_bp_mfs310_20230823.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 40  
**File Size:** 1100.7 KB  

---

## Page 1

 
 
 
ACATS-Fund/SERV® 
FUND/FIRM (PTF) TRANSFER CAPABILITY – BEST 
PRACTICES 
AUGUST 23, 2023 
 
  

---

## Page 2

Fund/Firm (PTF) Transfer Capability – Best Practices 
EXECUTIVE SUMMARY 2 
REVISION HISTORY 
Date Revisions 
08/23/2023 Document rebranded. Content reviewed and refreshed.  
04/03/2023 Reviewed.  Correction made (word missing in Frequently Asked Questions). 
08/11/2022 Content reviewed and refreshed: 
• Removed defunct example of letter needed to activate Fund/Firm Capability  
• Updated the Information on how clients can request activation. 
04/18/2022 Learning upgrade caused some link(s) to break.  Links have been corrected. 
02/19/2020 Content refreshed. Links updated.  
07/04/01/2019 Document was rebranded.  Content reviewed.  
Effective Date: 02/292016 New reject codes added. Please see Important Notice a8107, dated 10/27/2015. 
Effective Date: 03/18/2013 Please see Important Notices 
• a7472 Dated August 16, 2012, and 
• a7567 Dated January 9, 2013. 
Effective Date: April 23, 2012 Please see Important Notice a7355 & a7356. 
11/072008 Important Notice a6736 announced the addition of ACATS reject codes 15 and 28 
09/16/2008 Important Notice a6695 announced the enhancements that that would enable an ACATS 
[[Member]] firm ([[Broker]] dealer and bank) to transfer a mutual fund position directly with the 
mutual fund company. 
 
 
 

---

## Page 3

Fund/Firm (PTF) Transfer Capability – Best Practices 
EXECUTIVE SUMMARY 3 
TABLE OF CONTENTS 
EXECUTIVE SUMMARY ....................................................................................................................................... 5 
BACKGROUND .................................................................................................................................................. 5 
The Solution ...................................................................................................................................................... 5 
Cost / Benefit ..................................................................................................................................................... 6 
Transfer Process Between [[Broker]]/Dealers and Banks .................................................................................... 7 
ACATS Overview ................................................................................................................................................ 7 
Who Can Use the Service? ................................................................................................................................ 7 
Benefits ............................................................................................................................................................... 7 
How the Service Works ...................................................................................................................................... 7 
Transfer Process Between [[Broker]]/Dealers, Banks, and Mutual Fund [[Companies]]  ....................................... 9 
Overview ............................................................................................................................................................. 9 
What Services Were Available ........................................................................................................................... 9 
Industry Standardization ................................................................................................................................... 10 
Standardization .................................................................................................................................................10 
Benefits of Using the Fund/Firm Transfer Capability ........................................................................................10 
Fund/Firm Transfer Capability ..........................................................................................................................11 
Requirements ....................................................................................................................................................11 
How the Capability Works ................................................................................................................................. 12 
Firm-Initiated Transfer Reject Codes ............................................................................................................... 20 
Fund Company Error Handling .........................................................................................................................20 
Corresponding Fund/SERV Reject Codes ....................................................................................................... 21 
Frequently Asked Questions (FAQs) ................................................................................................................ 25 
Appendix A ......................................................................................................................................................... 27 
Definitions ........................................................................................................................................................... 36 
[[DTCC]] Resources – Links, Record Layouts and Related Rules ..................................................................... 37 
Links to Related ACATS & ACATS-Fund/SERV Documentation: ....................................................................37 
ACATS Documentation and Record Layouts can be located on the [[DTCC]] Learning site: .............................37 
ACATS-Fund/SERV documentation and record layouts are located at: ..........................................................37 
ToRA Plan Matrix (June 2009) ..........................................................................................................................37 

---

## Page 4

Fund/Firm (PTF) Transfer Capability – Best Practices 
EXECUTIVE SUMMARY 4 
[[NSCC]] Rule Changes .......................................................................................................................................... 39 
Rule Change .....................................................................................................................................................39 
 

---

## Page 5

Fund/Firm (PTF) Transfer Capability – Best Practices 
EXECUTIVE SUMMARY 5 
EXECUTIVE SUMMARY 
BACKGROUND  
Mutual Fund transfer processing was not standardized among [[Broker]]/dealers, banks, and mutual fund 
[[Companies]]. Fund transfer processing was fragmented with segments of both automated processing and other 
areas processing entirely manually.  
For example: 
• Retirement [[Asset]] transfers between mutual fund [[Custodians]] (funds) were highly automated through the 
National [[securities]] Clearing Corporation (“[[NSCC]]”) Transfer of Retirement Assets (“ToRA”) system.  
• Customer account transfers between [[Broker]]/dealers (firms) were also highly automated through [[NSCC]]’s 
Automated Customer Account Transfer System (“ACATS”). 
• However, there was a limited level of adoption of ACATS between banks and [[Broker]]/dealers for mutual 
fund transfers and as such they primarily relied on paper. 
 
Although highly regarded within their intended constituencies, both ToRA (developed for fund [[Companies]]) and 
ACATS (developed for [[Broker]]/dealers) were created in response to specific industry needs and offered limited 
appeal to non-participants.  Other methods existed that, to a lesser extent, had provided some automation 
where transfers were concerned, but no single transfer method alone met the complete needs of the industry 
and its clients. 
Even with the development of each of these methods, most transfers (including both transfers in-kind or re-
registrations and those that represented liquidations of fund positions held directly-at-fund or those being 
moved directly to the fund) were processed manually. Manual transfer processing was inefficient and costly to 
industry participants. It also caused numerous delays and market exposure.  On average, it was taking three 
weeks to manually move one mutual fund position, in either direction, between a firm ([[Broker]]/dealer or bank) 
and a fund company. 
Another consequence was the extensive number of bilateral agreements that existed between funds and firms. 
These agreements were executed to immobilize paperwork and allow transfer processing to become more 
automated through “point solutions” on a company-by-company basis. Even with these agreements, a 
significant portion of transfer processing was done through the movement of paper forms and spreadsheets 
and required manual intervention on behalf of all parties. 
The Solution  
The solution alleviates both the operational and legal concerns that combined, slowed the transfer process. 
All [[Broker]]-initiated in-kind transfers are to be submitted through ACATS. [[NSCC]] processes the request and 
forwards it on to the fund company through ACATS-Fund/SERV.  
ACATS-Fund/SERV provides funds with sufficient transparency to systematically ensure that only like account 
types (e.g., IRA to IRA for retirement scenarios) are being transferred and assist the funds in validating customer 
information. Upon verification of the ACATS-Fund/SERV record, the fund can elect to systematically re-register 
the [[shares]] without the need of manual intervention. By utilizing ACATS and ACATS-Fund/SERV, a transfer 
process is reduced to three business days. 
In addition, the solution introduced takes advantage of the legal constructs governing [[NSCC]] participation by 
removing the requirement for bilateral transfer agreements between parties (funds and firms) while still providing 
appropriate indemnifications for all parties. 

---

## Page 6

Cost / Benefit 
The design leveraged both ACATS and ACATS-Fund/SERV thus allowing funds and firms to utilize the existing 
functionality. 
[[Broker]]/dealers use ACATS to transfer thousands of customer accounts daily without the need of bilateral 
agreements between the firms or even a unilateral agreement with [[NSCC]]. Similarly, funds process retirement 
[[Asset]] transfers amongst each other through the use of ToRA without the need of bilateral agreements between 
fund participants. However, fund participants were, and still are, expected to execute a unilateral ToRA 
agreement with [[NSCC]] in order to utilize the service. Both funds and firms can take advantage of this transfer 
functionality while allowing the rules of engagement for ACATS and ACATS-Fund/SERV to govern their 
participation rather than a specific trading agreement between the parties. 
To eliminate the need for bilateral or unilateral agreements the [[NSCC]] Rules were expanded to satisfy the legal 
requirements and provide the needed protection. [[NSCC]] membership requires a signed application that binds 
members to,“… (a) to abide by the Rules of [[The Corporation]] and to be bound by all the provisions thereof, and 
that [[The Corporation]] shall have all the rights and remedies contemplated by said Rules; (b) the Rules of the 
Corporation shall be a part of the terms and conditions of every contract or transaction which the [[participant]] 
may take or have with or through [[The Corporation]]…” - This is from [[NSCC]] Rule 2A Section E.  Firms 
participating in the ACATS service rely on [[Section 17]] of [[NSCC]] Rule 50 for indemnity provisions regarding 
transfer requests between firms. [[NSCC]] filed a rule change in December of 2008 to Mutual Fund Services Rule 
52 allowing the transfer and re-registration of Fund/SERV eligible fund positions between brokers, banks and 
fund [[Companies]] that are [[NSCC]] members. The rule change amended section 18 of Rule 52 to include 
indemnification provisions for the re-registration transfer activity, so that funds and firms have the ability to rely 
on [[NSCC]] rules in lieu of entering into multiple indemnification agreements to engage in this transfer capability  
This language includes provisions for retirement transfers to provide assurances to [[Custodians]] that assets are 
being re-registered as permissible by law and that in all cases these transfers are trustee to trustee transfers, 
and as such are non-taxable and non-reportable for federal income tax and withholding purposes.   

---

## Page 7

Fund/Firm (PTF) Transfer Capability – Best Practices 
Transfer Process Between [[Broker]]/Dealers and Banks 7 
TRANSFER PROCESS BETWEEN [[Broker]]/DEALERS 
AND BANKS 
Brokerage Firms and Banks leverage ACATS to transfer assets in customer accounts. 
ACATS Overview 
The Automated Customer Account Transfer Service (ACATS) is a system that automates and standardizes 
procedures for the transfer of assets in a customer account from one brokerage firm and/or bank to another. 
Instruments handled by the system included equities, corporate and municipal [[Bonds]], unit investment trusts, 
[[Mutual Funds]], options, cash and other investment products. 
Who Can Use the Service? 
All eligible and qualified [[NSCC]] settling members and [[DTC]] [[Member]] banks are eligible for this service. 
Benefits 
ACATS facilitates the accurate and timely transfer of a customer's account, with the following 
operational advantages to users: 
• Uniform time frames, standardized reporting and automated control functions. 
• On [[Broker]] to [[Broker]] transfers, the service debits delivering firms the full market value of customers' 
[[securities]], promoting the timely transfer of assets. For account transfers where a bank is the contra side, 
the assets are delivered free. 
• ACATS requires the customer's Social Security/Tax Identification Numbers to enhance the ability of firms 
to identify individual accounts. 
• ACATS provides an automated transfer initiation procedure that incorporates the industry's effort to 
immobilize paper documents such as Transfer Initiation Forms (TIFs). 
• Automated residual credit processing allows credits that accumulate after a transfer is completed, such as 
[[Stock]] or cash dividends, to be transferred electronically from the delivering firm to the receiving firm 
through ACATS. 
• Through the ACATS-Fund/SERV link, users can easily re-register customers' fund assets. 
• Automated reclaims, partial transfers and fail reversals are available on a next-day [[settlement]] basis. 
How the Service Works 
Customers initiate account transfers by submitting completed TIFs to their new brokerage firm or bank (in the 
case of residual credits and other non-standard transfers, the delivering firm initiates the transfer). The TIF data 
is forwarded by the receiving [[Broker]] to the [[NSCC]], which assigns control numbers and sends control reports to 
both delivering and receiving brokers/banks. 
Delivering brokers/banks must submit [[Asset]] details or reject the transfer. Assets that are submitted are 
reported to the delivering and receiving firms. Receiving firms have one business day to reject the account, or 
request that the delivering firm make adjustments. During this one-day period, the delivering firm can add, 
delete or change an item. The receiving firm can also delete a mutual fund [[Asset]](s) where they don't have a 
selling agreement with the fund. 

---

## Page 8

Fund/Firm (PTF) Transfer Capability – Best Practices 
Transfer Process Between [[Broker]]/Dealers and Banks 8 
[[securities]] eligible for the Continuous Net [[settlement]] ([[CNS]]) System are automatically routed into [[CNS]], unless 
the delivering firm indicates otherwise. Other [[securities]] are transferred through ACATS Receive and Deliver 
instructions, or are sent to [[DTC]], if non-[[CNS]], [[DTC]]-eligible. Eligible mutual fund assets can be transferred 
through the automated ACATS-Fund/SERV interface. Options are routed to the Options Clearing Corporation, 
where transfers in customer options positions take place. 
On [[settlement]] date, for non-[[CNS]] eligible [[securities]], [[NSCC]] automatically debits the delivering [[Broker]] with the 
value of the assets being transferred through ACATS and credits the receiving [[Broker]] with the same amount. 
For assets that are delivered through [[NSCC]]'s physical delivery systems, [[NSCC]] will credit the delivering [[Broker]] 
with the value of those assets and debit a corresponding amount to the receiving [[Broker]]. 

---

## Page 9

Fund/Firm (PTF) Transfer Capability – Best Practices 
Transfer Process Between [[Broker]]/Dealers, Banks, and Mutual Fund [[Companies]] 9 
TRANSFER PROCESS BETWEEN [[Broker]]/DEALERS, 
BANKS, AND MUTUAL FUND [[Companies]] 
Overview 
Multiple methods had existed to transfer fund positions between [[Broker]]/dealers, banks, and mutual fund 
[[Companies]]. Each of these transfer methods were developed over time in response to specific industry needs.  
No single transfer method alone had met the complete needs of the industry and its clients. Firms and funds 
therefore developed their systems around one or more methods which best suited their needs.  
What Services Were Available 
• ACATS - The most mature of the automated transfer systems supporting [[Broker]] and bank functionality 
with the capability of transferring all types of accounts, cash, and various types of assets for both full and 
partial transfers. The ACATS-Fund/SERV link automates the re-registration of mutual fund positions. 
Participation in ACATS and ACATS-Fund/SERV is required for brokers and voluntary for banks. Firm 
participation in ACATS-Fund/SERV is authorized on a fund-by-fund basis. 
• Transfer of Retirement Assets (ToRA) – The second most mature method automates fund-to-fund 
retirement account cash transfers. ToRA enables funds to jointly initiate, acknowledge, confirm and settle 
the value of fund [[shares]] held in fund-sponsored IRA plans. ToRA is a separate service within 
Fund/SERV®, the industry standard for processing and settling fund orders. Funds must sign up to 
participate and execute a unilateral ToRA agreement with [[DTCC]]. 
• Networking – While not originally designed to automate the transfer process, many brokerage firms, 
working directly with a fund company, have adapted the Networking functionality along with Change of 
Dealer enhancements to facilitate transfer processing. This method, however, does not generally cover all 
types of transfers or all types of accounts and cannot be used to move [[shares]] for holding directly by a 
fund. 
• Manual (aka non-ACAT) – This labor intensive, paper-based process relies on physical delivery of 
paperwork and manual processing without any automated tracking. Fund [[Companies]] and [[Broker]] dealers 
received large numbers of manual transfer requests that were processed outside of the automated 
services mentioned above - this lack of automation was a source of a disproportionate number of client 
complaints due to the time required to complete the transactions and had historically been a focus of 
regulators. 
 
With the adoption of Fund/Firm transfer capability, in-kind transfers are now handled using ACATS and 
ACATS-Fund/SERV. 
  

---

## Page 10

Fund/Firm (PTF) Transfer Capability – Best Practices 
Industry Standardization 10 
INDUSTRY STANDARDIZATION 
Standardization 
The Fund/Firm Transfer Capability automates all types of transfers between each type of receiving and 
delivering entity-brokerage firms, banks, and mutual fund [[Companies]]. The implementation of Fund/Firm 
Transfer capability streamlined the transfer process by bringing together the existing systems and system 
users. In addition, the [[NSCC]] Rules were modified to satisfy the legal requirements and provide the needed 
protection for participants. The Fund/Firm Transfer Capability also addressed the historical problems and 
delays experienced by the industry when transferring accounts. 
Benefits of Using the Fund/Firm Transfer Capability 
The Fund/Firm Transfer Capability benefits brokerage firms, banks and funds in the following ways:  
• Lowers the cost of processing transfer requests by leveraging existing ACATS and ACATS -Fund/SERV 
functionality 
• Standardizes industry-wide automation 
• Provides controls around tracking the transfer process 
• Eliminates certain agreements governing transfer processing; expanded [[NSCC]] rules satisfy legal 
requirements and provide the needed protection 
• I ntegration of existing tools for transferring cost basis information (for details on current firm- related cost 
basis functionality visit  
https://dtcclearning.com/products-and-services/equities-clearing/cost-basis-
reporting-service-cbrs.html) 
 
The Fund/Firm Transfer Capability benefits investors in the following ways:  
 
• Reduces risk of [[Companies]] leaving [[shares]] unaccounted for during transfers  
• Reduces transfer cycle time 
• Improves tracking information 
• Reduces confusion 
• Improves overall client experience 
• Limits market exposure for subsequent activity 
 
 
 
 
 
 
 
 
 

---

## Page 11

Fund/Firm (PTF) Transfer Capability – Best Practices 
Industry Standardization 11 
Fund/Firm Transfer Capability 
The Fund/Firm Transfer Capability leverages both ACATS and ACATS-Fund/SERV and enables an ACATS 
[[Member]] to transfer a fund position directly from/to the fund company. For this capability, the fund company had 
two roles: one in its traditional role (processing re-registration instructions in a firm to firm transfer) and the 
other as contra party to the transfer. The adoption of Fund/Firm Transfers provides a single industry standard 
transfer system that automates in-kind mutual fund position transfers and simultaneously achieves the benefits 
previously mentioned by leveraging automated systems in the following manner: 
• In-kind transfers are handled using ACATS and ACATS-Fund/SERV 
Requirements 
For a fund to participate, the fund [[Member]] must join the Fund/Firm Transfer (PTF transfer) service and be 
ACATS-Fund/SERV eligible.  Additionally, the fund company’s Security Issue [[ID]] must also be ACATS-
Fund/SERV eligible and the [[Asset]] on the transfer request must always belong to the fund [[Member]] identified as 
the contra-party in the transaction.  In order to initiate fund/firm capability, please contact your Relationship 
Manager, Wealth Management Services team at 212-855-8877 or WMSConnect@[[DTCC]].com. 

---

## Page 12

Fund/Firm (PTF) Transfer Capability – Best Practices 
How the Capability Works 12 
HOW THE CAPABILITY WORKS 
 
 
 
 
 
 
 
 
 
 
 
 
  
Dealer Firm 
(Receiver) 
Initiator 
Submits ACAT 
PTF and Fund 
Registration
ACATS 
Transfer is 
Updated
[[NSCC]] ACATS
Processes 
Fund 
Registration 
Instruction
Receives 019 
Record, 
creates ACATS 
Fund/SERV 
Stat file
[[NSCC]] 
Fund/SERV
Transmits 018 
Record to Fund 
Company
Sends 019 
Record to 
ACATS
Fund Company 
(Deliverer)
Processes the 
018 Record
Submits the 
019 Record to 
Fund/SERV
How the Capability Works: Process Overview 
Day 2
Day 3
Day 4
Day 1
Firm Initiated In-Kind Transfer (“Firm Pull”) 
Situation: Client owns [[shares]] directly with the Mutual Fund Company (Matrix 
level 0 or level 4) in a retirement account or non-retirement account and wishes 
to transfer those positions in-kind to a [[Broker]]/dealer or bank. Client completes all 
required transfer forms and requests [[Broker]] dealer/bank to begin the transfer 
process 
Preconditions: 
• Account exists at firm; Security Issue [[ID]] is Fund/SERV eligible. 
• Security Issue [[ID]] is ACATS-Fund/SERV eligible. 
• Fund company is participating in the Fund/Firm Transfer Capability. 
High Level Process Flow 
****Day 1**** 
****Day 2-4**** 

---

## Page 13

Fund/Firm (PTF) Transfer Capability – Best Practices 
How the Capability Works 13 
 
 
 
 
 
 
 
 
Submits ACATS
PTF and Fund
Registration 
Processes Fund
Registration Instruction 
Transmits 018 Record
to Fund Company 
Processes the  
018 Record 
STEP 
 DETAIL 
Dealer Firm 
(Receiver)
Initiator 
Firm obtains Transfer Initiation Form (TIF) and fund account statement 
from the shareholder and enters a Position Transfer Fund (PTF) transfer 
request into the ACATS Transfer System. PTF includes Transfer Initiation 
(TI), [[Asset]] Transfer (AT) 
.[[Broker]] ACATS System transmits the PTF request to [[NSCC]] on next 
available transmission cycle. 
[[NSCC]] validates the [[participant]] and Security Issue [[ID]] eligibility, assigns 
an ACATS control number, sets the transfer status to “Review” and 
returns the ACATS control number to the initiating Firm. 
[[Broker]] system receives ACATS control number and status, creates an 
FR record and submits to [[NSCC]] with ACATS control number. 
[[NSCC]] 
ACATS 
After the Firm returns the FR, [[NSCC]] takes data from the FR, 
TI & AT records and creates an ACATS Transfer Record 
(018). 
[[NSCC]] 
Fund/SERV 
[[NSCC]] submits the 018 record to the Fund company. 
Fund 
Company
(Deliverer) 
Fund company receives record and validates the  018 record 
data as identified (See file record layout for all available fields for 
edit consideration). 
Fund company validates the 018 record, processes the request 
and sends the acknowledgement record 019 back to the Firm. 
How the Capability Works: Day One 
Process Detail: Firm Initiated In-Kind Transfer (“Firm Pull”) 
              Time Considerations 
Transfer Initiation (TI) & [[Asset]] Transfer (T) must be submitted by 
12:00 p.m. ET. 
Fund Registration (FR) must be submitted by 4:00 p.m. ET. 
 
Day 2
Day 3Day 4
Day 1

---

## Page 14

Fund/Firm (PTF) Transfer Capability – Best Practices 
How the Capability Works 14 
DETAIL 
STEP 
Submits the  
019 Record
to Fund/SERV 
Sends 019 Record 
to ACATS 
Receives 019 
Record, Creates 
ACATS
Fund/SERV Stat 
File 
ACATS Transfer 
is Updated 
Process Detail: Firm Initiated In-Kind Transfer (“Firm Pull”) 
              Time Considerations 
Fund Company must respond to 018 by 11:00 am ET. 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
  
  
 
  
 
 
  
  
   
 
   
 
 
  
Day 2
Day 3
Day 4
Day 1
How the Capability Works: Day Two – Day Four 
NOTE: Transfer details are passed through an edit 
process at the Fund Company. If failure occurs, 
determination will be made if transfer can be corrected 
and accepted, or if transfer must be rejected. 
Fund 
Company 
(Deliverer) 
Fund Company responds to 018 record by submitting 
acknowledgement or rejection on the 019 record by 11:00 am ET. 
[[shares]] are transferred into receiving fund/account as requested in 
the 018 record. 
[[NSCC]] 
Fund/SER
V 
 
The acknowledgement 019 is sent from Fund/SERV to ACATS. 
If no response from Fund company see, “Alternate Processing” 
below. [[NSCC]] 
ACATS 
[[NSCC]] sends ACATS Fund/SERV Stat file to Firm and if 
acknowledged, ages PTF transfer to “Settle Close” at end of day.  
If no response from Fund Company, see “Alternate Processing” 
below. 
Dealer 
Firm 
(Receiver) 
Day 2: Firm [[settlement]] System receives fund [[shares]] into 
customer’s firm account and networks position to fund account. 
Day 3: ACATS [[settlement]] Date – PTF transaction settles. 
Transfer is complete. 
 

---

## Page 15

Fund/Firm (PTF) Transfer Capability – Best Practices 
How the Capability Works 15 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
Dealer Firm 
(Deliverer) Initiator 
Submits ACAT 
PTF
ACATS 
Transfer is 
Updated
[[NSCC]] ACATS
Creates Fund 
Registration
Receives 019 
Record, 
creates ACATS 
Fund/SERV 
Stat file
[[NSCC]] 
Fund/SERV
Transmits 018 
Record to Fund 
Company
Sends 019 
Record to 
ACATS
Fund Company 
(Receiver)
Processes the 
018 Record
Submits the 
019 Record to 
Fund/SERV
How the Capability Works: Process Overview 
Day 2
Day 3
Day 4
Day 1Firm to Fund Company In-Kind Transfer (“Firm Push”) 
Situation: Client owns [[shares]] of a fund at a [[Broker]]/dealer in a retirement account 
or non-retirement account (Matrix level 3 or omnibus) and wishes to transfer those 
positions in-kind to a Mutual Fund Company (matrix level 0 or level 4). An account 
exists at the fund before this transfer can be initiated. 
Preconditions: 
• Account must exist directly at the Fund. 
• Security Issue [[ID]] is ACATS-Fund/SERV eligible. 
• Fund company is participating in the Fund/Firm Transfer Capability. 
High Level Process Flow 
****Day 1**** 
****Day 2-4**** 

---

## Page 16

Fund/Firm (PTF) Transfer Capability – Best Practices 
How the Capability Works 16 
 
DETAIL 
STEP 
Submits the 019 
Record to 
Fund/SERV 
Sends 019 Record 
to ACATS 
Receives 019 Record,
Creates ACATS
Fund/SERV Stat File 
ACATS Transfer 
is Updated 
Process Detail: Firm Initiated In-Kind Transfer (“Firm Push”) 
              Time Considerations 
Fund Company must respond to 018 by 11:00 am ET. 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
Day 2
Day 3
Day 4
Day 1
How the Capability Works: Day Two – Day Four 
NOTE: Transfer details are passed through an edit 
process at the Fund Company. If failure occurs, 
determination will be made if transfer can be corrected 
and accepted, or if transfer must be rejected. 
Fund Company responds to 018 record by submitting 
acknowledgement or rejection on the 019 record by 11:00 am ET. 
[[shares]] are transferred into receiving fund/account as requested in 
the 018 record. 
Fund 
Company 
(Receiver) 
[[NSCC]] 
Fund/SER
V 
The acknowledgement 019 is sent from Fund/SERV to ACATS. 
If no response from Fund company see, “Alternate Processing” 
below. 
[[NSCC]] 
ACATS 
[[NSCC]] sends ACATS Fund/SERV Stat File to Firm and ages PTF to 
“Settle Close” status at end of day.  
If no response from Fund company, see “Alternate Processing” 
below. 
 
Dealer 
Firm 
Deliverer 
(Initiator) 
Day 2: Firm [[settlement]] system delivers the fund [[shares]] out of the 
customer’s firm account. The fund [[shares]] are now held level 0 at 
the fund. The “[[Broker]] of record” will be retained or removed at the 
discretion of the Fund company. 
Day 3: ACATS [[settlement]] Date – PTF transaction settles. Transfer 
is complete. 
 
Day 2: All items not responded to will be given a status of “PEND” for one day and remain in ‘Review’ status.  If Fund Registration 
(FR) is acknowledged, transfer status is aged to ‘Settle Close’ at end of day. If FR is rejected, transfer status is aged to ‘Reject’ 
(Status 600) upon receipt of reject. 
Day 3: All pending items not responded to will be given a status of ‘System Purge’ and transfer status will be updated to ‘Reject’ (Status 600) 
If Fund Registration is acknowledged, age transfer status to ‘Settle Close’ at end of day.  If Fund Registration is rejected, transfer status will be 
updated to ‘Reject’ (Status 600) upon receipt of the reject. 
ACATS [[settlement]] Date: PTF transaction settles if account was aged to ‘Settle Close’ the previous day. (No money  
[[settlement]].) 
Day 4:  ACATS [[settlement]] Date:  PTF Transaction settles if account was aged to ‘Settle Close’ the previous day.  (No money [[settlement]].) 
 


---

## Page 17

Fund/Firm (PTF) Transfer Capability – Best Practices 
How the Capability Works 17 
Note:   
Unless otherwise designated, each section applies to both transfer types (“Pull” and “Push”). 
  
Best Practices: 
Firm Initiated In-Kind Transfer (‘Pull’) and Firm to Fund Company In-Kind Transfer (“Push”) 
[[NSCC]] Rejects – Security Issue [[ID]]  
Firms should establish controls to ensure a Security Issue [[ID]] submitted for the fund is held at the same fund company. This 
can be done by utilizing internal tables to ensure fund company X’s Security Issue [[ID]] is not submitted for fund company 
“Y’s’” [[participant]] #. 
 
Only 1 Security Issue [[ID]] per PTF transfer record can be submitted. Firms that utilize front end processes need to ensure 
that multiple AT records cannot be submitted per TI record. 
[[NSCC]] Rejects – [[participant]] # 
 
Firms should utilize the ACATS Master file to ensure the Fund [[participant]] # is eligible for a PTF Transfer Type. 
[[NSCC]] Rejects – Service Eligibility 
 
Firms should verify that the Fund Security Issue [[ID]] is ACATS-Fund/SERV eligible using the ACATS Transaction History 
Inquiry Application. 
Firm Rejects – SSN#/TIN# 
 
Firm to Fund Company In-Kind Transfer (Push): 
For accounts with no SSN/TIN (e.g., a non-US citizen with a non-US address): Firms should submit “000000000” in the 
SSN/TIN field and then a [[transfer agent]] can match against the remaining data fields. 
 
Firm Initiated In-Kind Transfer (Pull): 
Firms that use Omnibus Account processing should continue to populate the ACATS Fund Registration record using their 
TIN. ACATS will take both the customer’s SSN/TIN and the ACATS Account type input on the ACATS TI record and 
populate them both in new fields on the ACATS – Fund/SERV 018 Transfer Record to assist the Fund company with 
identifying the underlying customer. 

---

## Page 18

Fund/Firm (PTF) Transfer Capability – Best Practices 
How the Capability Works 18 
 
Best Practices: 
Firm-Initiated In-Kind Transfer (Pull) and  
Firm to Fund Company In-Kind Transfer (Push) 
Firm Rejects - Full [[shares]] 
When requesting a transfer of all [[shares]], use the full share indicator; [[DO]] not include a share amount 
Firm Rejects - Account Number 
Firms should submit entering "Account Number" and refrain from using "[[investor]] #", "Customer #', "Client #'', "Group #". 
• "Fund Number'' should not be used in conjunction with "Account Number" 
• No dashes or spaces should be used in entering "Account Number". 
Firm Rejects - Account Set-Up 
Firm to Fund Company In-Kind Transfer (Push Only): 
Firms should ensure an account has been set up at the receiving mutual fund company prior to submitting the request. This 
is a required element for initiating a PTF. Establishing a [[default]] new account number is not permissible for this transaction 
type. 
Fund Rejects - SS#/TIN# 
Firm Initiated In-Kind Transfer (Pull): 
• For Accounts where a Social Security or Tax [[ID]] # has not been established or populated systematically, firm should not 
submit PTF request until # is established.   Fund will reject for mismatch. 
• Fund [[Companies]] should use both the additional SSN/Tax [[ID]] number and ACATS Account Type fields on the ACATS-
Fund/SERV 018 Transfer record to assist them with identifying the underlying customer whenever the firm processes a 
Fund Registration for an Omnibus Account using their Tax [[ID]] number. 
 
Firm to Fund Company In-Kind Transfer (Push): 
• If Social Security Number / TIN on "From" and "To" accounts [[DO]] not match edit against secondary SS/TIN Field, and 
the firm sends a gift indicator, Fund Company should honor the transaction. 
 
 
 
 
 

---

## Page 19

Fund/Firm (PTF) Transfer Capability – Best Practices 
How the Capability Works 19 
Best Practices: 
Firm-Initiated In-Kind Transfer (Pull) and  
Firm to Fund Company In-Kind Transfer (Push) 
Fund Rejects – Account Type Codes 
Use the Account Type Code Matrix to help facilitate acknowledging transfer requests between certain mismatched Account 
Type Codes 
Fund Rejects – Fund Eligibility 
Firm Initiated In-Kind Transfer (Pull): 
• Verify that the Fund is eligible for transfer to a new account (ex. Not a closed fund). 
• No fund restrictions 
 
Firm to Fund Company In-Kind Transfer (Push): 
• Firms should verify that there are no fund restrictions. 
Fund Rejects – Account Number 
• Verify that the mutual fund and account numbers are valid. 
• Use correct Fund Account and Account Number and/or BIN (Matrix Level 3 can send only BIN) 
Additional Notes: 
• Residual balances in fund accounts following a transfer are possible but are out of scope for this project. 
• This service should not be used to orphan accounts. 
• This service was not developed for mass conversions - contact fund company prior to using this for conversion 
activity. 
 
  

---

## Page 20

Fund/Firm (PTF) Transfer Capability – Best Practices 
Firm-Initiated Transfer Reject Codes 20 
FIRM-INITIATED TRANSFER REJECT CODES 
This information is summarized in Important Notice a6736, dated November 7, 2008. 
• The Fund/SERV reject code assigned by the fund (see below) will be reported to the ACATS [[Member]] firms 
on the ACATS-Fund/SERV Statistics (STAT) file. 
• The corresponding PTF transfer request is moved to a Status of 600 (Reject). 
• The ACATS Position File will report one of two reject codes added as a result of the enhancement 
signifying that the in-kind transfer was not successful: 
» 015 – Position Transfer Fund (Deliverer) – Used for any rejected in-kind transfers from Fund 
control to Firm control. 
» 028 – Position Transfer Fund (Receiver) – Used for any rejected in-kind transfers from Firm 
control to Fund control. 
 
Firms are encouraged to use the ACATS-Fund/SERV Stat file, in the event of a PTF transfer request reject to 
Understand the reason why the transfer was rejected and adjust their subsequent PTF transfer request  
Submission accordingly. 
Fund Company Error Handling 
Every effort should be made to soft-reject Fund/SERV transfers that may not fully pass system edits, which 
may permit minor corrections to be made and permit successful processing of the order. However, it is 
inevitable that a fund may need to reject a transfer back to the firm for legitimate business and / or data 
purposes. 
Please reference the following best practices when a fund must reject an ACATS-Fund/SERV transfer initiated 
from the transfer capability. As noted previously, these codes are provided to firms on the ACATS-Fund/SERV 
Statistics File, and consistent usage can help firms in automating error handling, while providing a common 
language for the Industry to use when communicating trade rejects. 
The reject codes provided in the list are a subset of all available Fund/SERV rejects codes, which funds and 
firms already know in the context of ACATS-Fund/SERV firm to firm transfers. The list below does not include 
these general reject codes, examples of which pertain to stop codes, social codes, and file configuration 
concerns. However, these more general reject codes, pertaining to all aspects of ACATS-Fund/SERV, could 
also be used in the context of the transfer capability. 
The list provides the corresponding Fund/SERV reject code, its description, and the business context (as 
applicable) in which that reject code should be used. 
  

---

## Page 21

Fund/Firm (PTF) Transfer Capability – Best Practices 
Corresponding Fund/SERV Reject Codes 21 
CORRESPONDING FUND/SERV REJECT CODES 
 
CODE DESCRIPTION BUSINESS REASON & SUGGESTED BEST PRACTICE 
047 Network Control Indicator Missing/Invalid Business Reason: Delivering account matrix level not valid for 
fund to firm transfers; receiving account matrix level not valid for 
firm to fund transfers. 
Suggested Best Practice: Hard reject back to submitter. 
Note: Used in Pull / Push scenarios 
060   [[liquidation]] amount exceeds book share 
balance 
Business Reason: If the [[shares]]/dollar amount specified is 
greater than the account balance at the time the request is 
received by the fund. 
Suggested Best Practice: The fund should verify if all [[shares]] 
should be transferred and process or reject the ACATS-
Fund/SERV transaction accordingly. 
Notes:  Used in Pull / Push scenarios.  The code of 060 currently reads “[[liquidation]] Amount Exceeds Book Share 
Balance”.  Recommending “[[liquidation]]” be changed to “Transaction” so the error can be applied to transfers as well. 
073 Customer Account Number at Fund 
(ACATS Transfer From) invalid 
Business Reason: If the [[shares]] are being transferred from an 
existing fund account, the number provided in the Customer 
Account number at fund (DEL Firm) field should match the 
account number on the fund's books. 
Suggested Best Practice: The fund should verify the account 
number and process or reject the ACATS-Fund/SERV 
transaction accordingly. 
Note: Primarily used in Pull scenario when the delivering account is not networked (matrix level 0). If the delivering 
account is matrix level 4, the firm will provide a BIN on the 018 record. 
074 Customer Account Number at Fund 
(ACATS Transfer To) invalid 
Business Reason: If the [[shares]] are being transferred to an 
existing fund account, the number provided in the Customer 
Account number at fund field should match the account number 
on the fund's books. 
Suggested Best Practice: The fund should verify the account 
number and process or reject the ACATS-Fund/SERV 
transaction accordingly. 
Note: Used in Push scenario for the receiving account. The firm will provide a BIN on the 018 record for the delivering 
account. 
103 SSN/EIN number missing Business Reason: The shareholder SSN/EIN provided on the 
incoming record does not match the SSN/EIN on the account 
held at the fund. 
Suggested Best Practice: The fund should verify the SSN/EIN 
and process or reject the ACATS-Fund/SERV transaction 
accordingly. 
Notes:  Used in Pull / Push scenarios 

---

## Page 22

Fund/Firm (PTF) Transfer Capability – Best Practices 
Corresponding Fund/SERV Reject Codes 22 
CODE DESCRIPTION BUSINESS REASON & SUGGESTED BEST PRACTICE 
139 
 
Account Type missing/Invalid Business Reason: Fund prototype retirement plan types on 
delivering and receiving accounts not equal for ACATS transfer 
in kind.  The account/plan types must match or be compatible 
per the Plan Type Matrix (See [[DTCC]] resource listing below). 
Suggested Best Practice: The fund should verify the account 
type and process or reject the ACATS-Fund/SERV transaction 
accordingly. 
Notes: Used in Pull / Push scenarios.  For retirement accounts, this will be the retirement plan type. 
176 Transaction Not Allowed Against 
this Firm 
Business Reason: Fund to firm transfers not allowed for this firm; 
firm to fund transfers not allowed for this firm. 
Suggested Best Practice:  Hard reject back to submitter. 
Notes:  Used in Pull / Push scenarios 
178 Transaction Not Allowed Against this 
Security Issue 
Business Reason: The fund family participates in the ACATS 
service, but this specific Security Issue [[ID]] is not an ACATS 
[[participant]]/does not allow firm to fund transfers. 
Suggested Best Practice:  This Hard Reject should be used 
when a specific Security Issue [[ID]] does not participate in the 
transfer enhancement, but other Security Issue Ids within the 
Fund Company [[DO]] participate in the transfer enhancement 
Notes:  Used in Pull / Push scenarios 
098 Other error Business Reason: To be used only if error cannot be defined by 
an existing reject code. 
 
Suggested Best Practice: Contact fund or resubmit through 
manual channel 
099 Multiple Rejects Business Reason: To be used when there are multiple reasons 
for rejecting item. 
 
Suggested Best Practices: Contact fund or resubmit through 
manual channel. 
712 Zero Balance Account Business Reason: This reject should be used when the account 
to be transferred to new registration is zero balance 
Suggested Best Practice: Firm should contact client to 
determine necessary action. 
Note: Used in Pull / Push scenarios 
713 Requested Amount Exceeds [[shares]] 
Available  
Business Reason: This reject should be used when the account 
balance is greater than $0; but there are not enough [[shares]] in 
the account to satisfy the request. 

---

## Page 23

Fund/Firm (PTF) Transfer Capability – Best Practices 
Corresponding Fund/SERV Reject Codes 23 
CODE DESCRIPTION BUSINESS REASON & SUGGESTED BEST PRACTICE 
Recommended Best Practice: Contact client and resubmit for 
correct amount. 
Note: Used in Pull / Push scenarios 
714 Not PTF (Position Transfer Fund) Eligible Business Reason: This reject is to be used when an account 
type or fund is not able to transfer through a PTF (Example: 
retirement account, etc. or paperwork is needed) 
 
Recommended Best Practice: Firm should request a manual 
transfer be processed. 
Note: Used in Pull / Push scenarios 
 
 
 
 
 
 
 
 
 
 
 
CODE DESCRIPTION BUSINESS REASON & SUGGESTED BEST PRACTICE 
715 Simple IRA under 2 years Business Reason: This reject should be used when a Simple 
IRA account has not satisfied the 2-year holding period. 
 
Recommended Best Practice: Firm should review the fund 
policy and contact client 
Notes: Used in Pull / Push scenarios 
716 Account not found Business Reason: This account cannot be found. Possible 
reason for reject is incorrect account number. 
Recommended Best Practice: Firm should contact Fund or 
clarify with client 
Note: Used in Pull/Push scenarios 
717 Duplicate Request Business Reason: This reject should be used when a duplicate 
request has been submitted 
Recommended Best Practice: [[DO]] not resubmit. No action by 
firm necessary 

---

## Page 24

Fund/Firm (PTF) Transfer Capability – Best Practices 
Corresponding Fund/SERV Reject Codes 24 
Note: 
Funds should not use the following reject codes for PTFs.  See Recommended Best Practices noted for each. 
 
CODE DESCRIPTION BUSINESS REASON & SUGGESTED BEST PRACTICE 
019 Money Amount/Number of [[shares]] 
missing/invalid 
Recommended Best Practices for Funds: 
[[DO]] not use 019 if an account has $0 balance; use reject code 712 
(Zero Balance Account). 
[[DO]] not use 019 if there are not enough [[shares]] in the account to 
satisfy the request on an ACATS- Fund/SERV transfer, use 713 
(Requested amount exceeds [[shares]] available. 
Recommended Best Practices for Firms: 
Review if money amount or number of [[shares]] submitted were 
missing or an invalid format was sent. Resubmit if either of these 
scenarios can be corrected. 
060 [[liquidation]] amount exceeds book share 
balance 
 
Note: Only to be used for [[liquidation]] 
requests. 
Recommended Best Practices for Funds: 
[[DO]] not use for ACATS-Fund/SERV transfers. Use reject code 713 
when [[shares]] to be transferred exceed the book share balance. 
 
Recommended Best Practices for Firms: 
If reject code 060 is received for an ACATS- Fund/SERV transfer 
request, firms should contact funds or resubmit through manual 
channels. 

---

## Page 25

Fund/Firm (PTF) Transfer Capability – Best Practices 
Frequently Asked Questions (FAQs) 25 
FREQUENTLY ASKED QUESTIONS (FAQS) 
Q How can I begin using the standardized transfer process? 
A If you are an existing ACATS [[Member]] firm, you need to be ACATS-Fund/SERV eligible and set-up for 
[[settlement]] Location 10 (Fund/SERV) on the ACATS [[participant]] Master file. Firms who are not ACATS-
Fund/SERV eligible need to be activated for this service. If you are a Fund Company, you must first be 
both Fund/SERV and ACATS-Fund/SERV eligible as well as activated for Fund/Firm Transfer (PTF) 
service. In order to initiate any of these services, please contact your Relationship Manager, Wealth 
Management Services team at 212-855-8877 or WMSConnect@[[DTCC]].com. 
Q How will I know if a fund is participating? 
A Funds that have signed up for this capability will be listed on the WMS website and the ACATS website. 
Please reference the fund [[participant]] list prior to submitting a transfer request. Firms can also determine 
who is utilizing the enhancement by receiving the ACATS [[participant]] Master file AutoRoute # 02090068 
which is distributed weekly on Friday. There is a field on the file that identifies whether the ACATS 
[[Member]] is a [[Broker]], bank or mutual fund company. 
Q If I am a mutual fund [[transfer agent]], will I need to modify my systems even if we are not 
participating in the Fund/Firm Transfer Capability? 
A Programming is not required for [[NSCC]] participants that have not signed up for the Fund/Firm Transfer 
Capability for non-participating funds for this enhancement. [[DTCC]] will populate the additional data fields 
in the 018 record with spaces. 
Q How does [[DTCC]] handle a transfer request (PTF) submitted for a fund that isn’t signed up for 
Fund/Firm Transfer Capability? 
A The PTF request is rejected upon submission to ACATS so the 018 record will not be created. 
Q Can Trust [[Companies]] participate in Fund/Firm Transfer Capability? 
A Yes, it is available to all ACATS [[Member]] firms. ACATS allows a number for the Tax [[ID]] of the Trust 
Company. There is also a field for the Tax [[ID]] of the shareholder or owner of the account. This field is 
available to be passed as an individual SSN on the Fund/SERV 018 Record Type. 
Q Will agreements need to be amended? 
A We hope that the availability of the automation and the [[NSCC]] rule change is sufficient to obviate the 
need for separate agreements. However, each fund and firm will make their own determination as to 
whether existing bi-lateral agreements also need to be amended or additional agreements need to be 
executed prior to participating in this capability. Please note that separate bilateral agreements detract 
from one of the main benefits of the enhancement, which is to use [[DTCC]] rules in lieu of negotiating / 
amending agreements to guide and govern participation. Such rule changes were made in consultation 
with fund and firm representatives to ensure appropriate protection for delivering and receiving firms in 
the transfer transaction. 
 
Q How is the transfer of Cost Basis handled? 
A The enactment of Cost Basis Legislation, (became effective for [[Mutual Funds]] January 1, 2012) requires 
the industry to facilitate the transfer of share lot history as part of the transfers’ process.  See the Cost 
Basis Reporting Service (CBRS) Supplemental Guide on [[DTCC]]’s Learning Center at:  
https://dtcclearning.com/products-and-services/mutual-fund-services/mfs-cross-products.html 
Q What kind of transfers can be performed through the Fund/Firm Transfer Capability? 

---

## Page 26

Fund/Firm (PTF) Transfer Capability – Best Practices 
Frequently Asked Questions (FAQs) 26 
A Retail and retirement account positions held directly at the fund and fund positions held at a participating 
firm can be transferred to an account that was pre-established at the fund and/or firm prior to the 
transfer. 
Q Since ACATS-Fund/SERV allows transfers to new accounts, how are Customer Identification 
Program (CIP) requirements met by the fund company and their [[transfer agent]]?  
A ACATS allows transfers to new accounts for brokers, and the processes to support CIP exist. The initial 
implementation of the capability for “firm to fund” transfers is limited to transfers into accounts  at the 
funds that are already established. Examples include gifting of [[shares]] to someone or transfers of [[shares]] 
in kind to an account already established at the fund company or with the brokerage firm.  
Q Will a request be rejected by ACATS if a Fund Registration (FR) record is not submitted by the 
end of the first day if it is in transfer status “Review?” 
A No, ACATS will generate a fund registration on behalf of the receiver (either firm or fund) using pre- 
identified [[default]] values. 
Q When should the “gift indicator” be populated? 
A The gift indicator should be populated when the firm receives the proper paperwork, obtains the TIF from 
the fund TA or LOA from the shareholder. 
Q Can I send a fund more than one Security Issue [[ID]] per request? 
A No, only one Security Issue [[ID]] can be submitted per PTF transfer record. 
Q Can I use this to perform mass firm conversions? 
A The Networking Service should typically be used to facilitate these types of transfers. Please contact the 
fund company prior to sending any mass firm to firm or firm resignation activity so that the process can 
be managed effectively for all parties. 
Q How should the TIN be populated on the 018 record? 
A The TIN is a required field on the 018 record. When a firm is acting as a receiver, there is a required field 
on the ACATS Fund Registration (FR) record which is for the Social Security/Tax [[ID]] Indicator.  
Additionally, there is a field on the 018 record that will always be populated with the same Social 
Security/Tax [[ID]]# that was used on the PTF transfer request. For a fund acting as a receiver, ACATS will 
always [[default]] the Social Security Tax [[ID]]# indicator to Tax [[ID]]#. The number populated in that field and in 
the additional Social Security/Tax [[ID]]# field will always be the same number used on the PTF transfer 
request. 
Q Can this process be used to complete a mass representative / dealer change?  
A No, the ACATS Fund/SERV service is not intended to facilitate a mass representative / dealer change 
function or firm resignation activity. This is supported through Networking. 
Q What reject codes should be used for the 018 record? 
A Fund/SERV Reject codes are available on the Learning center. 
Q How long does a fund-to-firm transfer take to settle? 
A [[settlement]] will occur within 3 to 4 business days (the same time frame as ACATS) depending on when 
the reply (Fund/SERV record type 019) is received. The fund can either acknowledge or reject the 
request. If there is no reply to the request in the allotted time, the transfer will move to a “reject status” in 
the ACATS system. 

---

## Page 27

Fund/Firm (PTF) Transfer Capability – Best Practices 
Appendix A 27 
APPENDIX A 
FIRM AS RECEIVER 
Field Name ACATS Values 
Record Length 0755 
Physical Sequence Number 01 
Logical Sequence Number 01 
Originator Type ‘B’= Firm 
Firm Number Original Receiver Number (Firm) 
Record Type ‘018’ 
Test Indicator ‘0’=Production 
Fund Number Populated from Fund/SERV 
Security Issue Country Code ‘00’ 
Security Issue [[ID]] ISIN # populated from ACATS [[Asset]] Transfer (AT) Record 
Security Issue Check Digit ‘0’ 
Fund/SERV Control Number Populated from Fund/SERV 
Correction Indicator Spaces 
Processing Date ACATS Process Date 
*(R) Book/Physical Share Indicator ‘1’ – Transfer in and out: book [[shares]] 
*(C) PI Delivery Indicator Spaces 
*(O) TPA/Investment Agent Number Spaces 
*(O) Secondary Social Security Number Secondary Social Security Number associated to Account 
ACATS will populate this field with the value in the ‘Original Receiver 
Customer SS Number/Tax [[ID]] Secondary’ field from the Transfer Input 
(TI). This field is used for PTF’s when Fund is either the deliverer or 
receiver.   
If the Fund is a deliverer and the Firm is the receiver this field is the 
‘Original Receiver Customer SS Number Secondary’ from the TI 
record. The value in the ‘Original Receiver Customer SS Number 
Secondary’ on the TI record may be different from the SSN/EIN on 
the FR record or the Receiving Customer’s Primary Social Security 
Number on the TI record. 
Best Practice: The secondary social security number should be 
applied to search criteria when identifying accounts that may have 
multiple account owners 
*(O) Customer Name Original Receiver Customer Account Name populated from ACATS TI 
record 
*(R) Fund Account Indicator ‘0’ = New Account - domestic 
*(R) Customer Account Number at Fund Spaces 

---

## Page 28

Fund/Firm (PTF) Transfer Capability – Best Practices 
Appendix A 28 
FIRM AS RECEIVER 
Agent for Firm Number Original Receiver Number (Firm) 
*(R) Network Control Indicator The firm’s receiving [[participant]] [[default]] value populated from ACATS 
[[participant]] Instruction Database, if provided 
Otherwise - ‘0’ = Non-networked 
*(R) SSN/EIN Indicator ‘0’= Tax [[ID]]# 
*(R) SSN/EIN Number The firm’s receiving [[participant]]’s Tax [[ID]] # populated from the ACATS 
[[participant]] Instruction Database 
*(R) [[Dividend]] Code The firm’s receiving [[participant]] [[default]] value populated from the 
ACATS [[participant]] Instruction Database, if greater than spaces 
Otherwise - ‘1’ – Reinvest, Reinvest, Reinvest 
*(R) Withhold Indicator ‘0’ = Certified (W-9 on file) 
*(R) Payable Information Indicator ‘0’ = Address of Record 
*(R) Customer Name End Line Indicator ‘4’ = Line number where name ends 
*(O) Customer Zip Code 5 digits: 
The firm’s receiving [[participant]] [[default]] value populated from the 
ACATS [[participant]] Instruction Database, if provided 
Otherwise - Spaces 
 
4 digits: Spaces 
*(R) Social Code ‘15’ - When receiver is a bank 
‘18’ – When receiving [[participant]] Network Control Indicator on 
ACATS [[participant]] Instruction Database [[default]] value = ‘3’ 
‘06’ – Otherwise 
*(R) NAV Account Indicator ‘0’ = No 
*(R) [[Margin]] Account Indicator ‘0’ = No 
*(R) Check Writing Privileges Indicator ‘0’ = No 
*(O) State of Sale (State Code) Spaces 
*(C) Country of Origin (Country Code) Spaces 
*(R) Account Representative Name ‘ACATS [[default]]’ 
*(R) Account Representative Number '999999999' 
*(R) Branch Identification Number '999999999' 
*(C) Number of Payables 0 
*(C) W8 Certification Date Spaces 
*(C) W8 Expiration Date Spaces 
*(O) W8 Override NRA Special Rate Spaces 

---

## Page 29

Fund/Firm (PTF) Transfer Capability – Best Practices 
Appendix A 29 
FIRM AS RECEIVER 
*(C) W8 Qualified [[intermediary]] Indicator Spaces 
*(C) W8 Override Country Code Spaces 
*(R) Customer Name/Address Line 1 Receiving [[participant]]’s Name (Firm Name) 
*(C) Customer Name/Address Line 2 'FOR BENEFIT OF: Original Receiver Customer Account Name 
*(C) Customer Name/Address Line 3 Original Receiver Customer Account Name 
*(C) Customer Name/Address Line 4 Spaces 
*(C) Customer Name/Address Line 5 The firm’s Receiving [[participant]] [[default]] Customer Name/Address 
(Line 5) populated from ACATS [[participant]] Instruction Database, 
when exists 
Otherwise - Spaces 
*(C) Customer Name/Address Line 6 The firm’s Receiving [[participant]] [[default]] Customer Name/Address 
Line 6 populated from ACATS [[participant]] Instruction Database, when 
exists 
Otherwise - Spaces 
*(R) Transaction Type ‘1’=Transfer to new account 
Account Type Indicator ‘1’ = ‘Customer Name’ 
Customer Account Number at Firm The firm’s Receiving [[participant]] [[default]] Account Prefix (if exists on 
ACATS Database) + Original Receiver Customer Account Number + 
Receiving [[participant]] [[default]] Account Suffix (if exists) 
Delivering Firm Number Original Deliverer Number (Fund) 
Customer Account Number at Fund (Delivering 
Firm) 
Delivering Account Number of Fund populated from the ACATS TI 
record 
Customer Account Number at Firm (Delivering 
Firm) 
‘Spaces’ 
Network Control Indicator (Delivering Firm) ‘0’ – Not Networked 
Agent for Delivering Firm Number Original Deliverer Number (Fund) 
*(R) Fraction Indicator 1 = Transfer Fraction 
 2 = [[liquidation]] fraction 
Full/Partial Indicator This field will be populated from whatever the firm submits on the 
ACATS TI record 
Values 
‘0’ – (Full) - move all [[shares]] in the account at the Fund when AT MF 
Full/Partial Indicator = ‘1’ 
 
‘1’ - (Partial) - move the exact share quantity specified when AT MF 
Full/Partial Indicator = ‘2’ 

---

## Page 30

Fund/Firm (PTF) Transfer Capability – Best Practices 
Appendix A 30 
FIRM AS RECEIVER 
Transfer Share Quantity Populated from ACATS [[Asset]] Transfer (AT) record 
However, if the firm populates 0 in the field above, this should be 
SPACES 
CDSC Transfer Indicator Spaces 
Delivering Firm Share Aging Indicator ‘1’ - The delivering firm or fund company will provide the share aging 
information in an automated fashion through the Networking Share 
Aging file. 
Membership Identifier This is the firm’s Receiving [[participant]] [[default]] Membership Identifier 
populated from the ACATS [[participant]] Instruction Database when 
populated 
Otherwise – spaces 
Membership Identifier (Delivering Firm) ‘Spaces’ 
Transfer Money Amount ‘Spaces’ 
Currency Indicator This field is populated from the ACATS [[Asset]] Transfer (AT) record 
[[default]] Registration ‘1’ = [[default]] Registration 
ACATS Control Number ACATS Control Number + [[Asset]] Sequence# 
*(R) Transfer Disbursement [[Option]] – Accruals ‘4’= Reinvest - Receiving firm (bucket to bucket) 
*(R) Transfer Disbursement [[Option]] - Fractional 
[[Cash-in-Lieu]] 
‘4’= Reinvest - Receiving firm 
*(R) Transfer Disbursement [[Option]] – Residuals ‘4’= Reinvest - Receiving firm 
*(O) NRA Tax 0 
[[settlement]] Date ACATS [[settlement]] Date (Will always be 2 business days after 
processing date) 
Accrual Money Amount 0 
Accrual Money Amount Indicator Spaces 
Customer SSN/EIN Number SSN/EIN Number taken from ACATS Transfer Input (TI) Record 
ACATS populates this field with the value in the ‘Receiving 
Customer’s Primary Social Security’ field from the TI record.  This 
field is used for PTFs only, when Fund is either the deliverer or the 
receiver.   
The rule above is true in all circumstances, both when the receiver 
submits the FR record and when ACATS uses a [[default]] registration. 
Note: 
The value in the ‘Receiving Customer’s Primary Social Security 
Number’ on the TI record may be different from the SSN/EIN on the 
FR record.  

---

## Page 31

Fund/Firm (PTF) Transfer Capability – Best Practices 
Appendix A 31 
FIRM AS RECEIVER 
ACATS Account Type Account Type taken from ACATS Transfer Input (TI) Record 
Gift/Donation Indicator Taken from ACATS Transfer Input (TI) Record 
 
  

---

## Page 32

Fund/Firm (PTF) Transfer Capability – Best Practices 
Appendix A 32 
 
Fund as Receiver 
Field Name ACATS Values 
Record Length 0755 
Physical Sequence # 01 
Logical Sequence # 01 
Originator Type ‘B’ = Firm 
Firm Number Original Receiver # (Fund) 
Record Type ‘018’ 
Test Indicator ‘0’ = Production 
Fund Number Populated from Fund/SERV 
Security Issue Country Code ‘00’ 
Security Issue [[ID]] ISIN # from ACATS [[Asset]] Transfer (AT) Record 
Security Issue Check Digit ‘0’ 
Fund/SERV Control # Populated from Fund/SERV 
Correction Indicator Spaces 
Processing Date ACATS Process Date 
Book/Physical Share Indicator ‘1’ – Transfer in and out: book [[shares]] 
PI Delivery Indicator Spaces 
TPA/Investment Agent Number Spaces 
Secondary Social Security Number Secondary Social Security Number associated to Account 
ACATS will populate this field with the value in the ‘Original Receiver 
Customer SS Number/Tax [[ID]] Secondary’ field from the Transfer Input 
(TI). This field is used for PTF’s when Fund is either the deliverer or 
receiver.   
If the Fund is a deliverer and the Firm is the receiver this field is the 
‘Original Receiver Customer SS Number Secondary’ from the TI 
record. The value in the ‘Original Receiver Customer SS Number 
Secondary’ on the TI record may be different from the SSN/EIN on 
the FR record or the Receiving Customer’s Primary Social Security 
Number on the TI record. 
Best Practice: The secondary social security number should be 
applied to search criteria when identifying accounts that may have 
multiple account owners. 
Customer Name Original Receiver Customer Account Name 
Fund Account Indicator ‘2’ – Existing account – domestic 
Customer Account Number at Fund Receiver Customer Account # at Fund (This field will be populated 
from the ACATS TI record – Original Receiver Customer Account 
Field) 
Agent for Firm Number Original Receiver Number (Fund) 

---

## Page 33

Fund/Firm (PTF) Transfer Capability – Best Practices 
Appendix A 33 
Fund as Receiver 
Network Control Indicator ‘0’ – Not Networked 
SSN/EIN Indicator ‘0’ = Tax [[ID]] number 
SSN/EIN Number SSN/EIN Number taken from ACATS (Transfer) Input Record 
[[Dividend]] Code ‘1’ – Reinvest, Reinvest, Reinvest 
Withhold Indicator ‘0’ – Certified (W-9 on file) 
Payable Information Indicator ‘0’= Address of Record 
Customer Name End Line Indicator ‘4’ lines where name ends 
Customer Zip Code Spaces 
Social Code ‘ 99’ - ‘Other 
NAV Account Indicator ‘0’ = No 
[[Margin]] Account Indicator ‘0’ = No 
Check Writing Privileges Indicator ‘0’ = No 
State of Sale (State Code) Spaces 
Country of Origin (Country Code) Spaces 
Account Representative Name ‘ACATS [[default]]’ 
Account Representative Number '999999999' 
Branch Identification Number '999999999' 
Number of Payables 0 
W8 Certification Date Spaces 
W8 Expiration Date Spaces 
W8 Override NRA Special Rate Spaces 
W8 Qualified [[intermediary]] Indicator Spaces 
W8 Override Country Code Spaces 
Customer Name/Address Line 1 Receiving [[participant]]’s Name 
Customer Name/Address Line 2 'FOR BENEFIT OF: Original Receiver Customer Account Name 
Customer Name/Address Line 3 Original Receiver Customer Account Name 
Customer Name/Address Line 4 Spaces 
Customer Name/Address Line 5 Spaces 
Customer Name/Address Line 6 Spaces 
Transaction Type ‘2’ = Transfer to existing account’ 
Account Type Indicator Populated from Firm input as Deliverer on ACATS AT Record – 
Either ‘1’ Customer Name or ‘2’ [[street name]] 
Customer Account Number at Firm Receiver Customer Account # at Fund (Taken from the ACATS TI 
record) 
Delivering Firm Number Original Deliverer Number 

---

## Page 34

Fund/Firm (PTF) Transfer Capability – Best Practices 
Appendix A 34 
Fund as Receiver 
Customer Account Number at Fund (Delivering 
Firm) 
Populated from Firm Input as Deliverer on ACATS AT Record (Taken 
from Fund/SERV Customer Account Number Deliverer field) when AT 
(delivering side) Book/Physical Ind = 1 or 2 
Otherwise – spaces and Customer Account Number at Firm 
(Delivering firm) field below will be populated 
Customer Account Number at Firm (Delivering 
Firm) 
Populated from Firm Input as Deliverer on ACATS AT Record (Taken 
from Fund/SERV Customer Account Number Deliverer field) when AT 
(delivering side) Book/Physical Ind = 0 
Otherwise – spaces and Customer Account Number at Fund 
(Delivering firm) field above will be populated 
Network Control Indicator (Delivering Firm) Populated from Firm Input as Deliverer on ACATS AT Record (Taken 
from Network Control Indicator Field) 
Values 
0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
Agent for Delivering Firm Number Populated from Firm Input as Deliverer on ACATS AT Record (Taken 
from Executing [[Broker]], when populated) 
Otherwise Original Deliverer Number 
Fraction Indicator ‘1’ = Transfer Fraction 
Full/Partial Indicator Populated from Firm Input as Deliverer on ACATS AT Record 
‘0’ – Full – move all [[shares]] in the account at Fund when AT MF 
Full/Partial Indicator = ‘1’ 
‘1’ – Partial – move the exact share quantity specified when AT MF 
Full/Partial Indicator = ‘2’ 
Transfer Share Quantity Populated from ACATS AT Record (Quantity Field) 
A - However, if the firm populates 0 in the field above, this should be 
SPACES 
CDSC Transfer Indicator Spaces 
Delivering Firm Share Aging Indicator Populated from Firm Input as Deliverer on ACATS AT Record (Taken 
from the Share Aging Indicator field) 
Values 
1 = The delivering firm or fund company will provide the share aging 
information in an automated fashion through the Networking Share 
Aging file. 
2 = The delivering firm or fund company will provide the share aging 
information outside of the system 
Membership Identifier ‘SPACES’ 
Membership Identifier (Delivering Firm) Populated from Firm Input as Deliverer on ACATS AT Record (Taken 
from the Firm Membership Indicator – Deliverer) 
Transfer Money Amount Populated from Firm Input as Deliverer on ACATS AT Record 

---

## Page 35

Fund/Firm (PTF) Transfer Capability – Best Practices 
Appendix A 35 
Fund as Receiver 
Currency Indicator Populated from Firm Input as Deliverer on ACATS AT Record (ISO 
Currency Code) 
[[default]] Registration ‘1’ = [[default]] Registration 
ACATS Control Number ACATS Control Number + [[Asset]] Sequence# 
Transfer Disbursement [[Option]] - Accruals ‘4’ = Reinvest - Receiving firm (bucket to bucket) 
Transfer Disbursement [[Option]] - Fractional Cash-
in-lieu 
‘4’ = Reinvest - Receiving firm 
Transfer Disbursement [[Option]] – Residuals ‘4’ = Reinvest - Receiving firm 
NRA Tax 0 
[[settlement]] Date ACATS [[settlement]] Date (This will always be 2 business days after 
processing date) 
Accrual Money Amount 0 
Accrual Money Amount Indicator Spaces 
Customer SSN/EIN Number SSN/EIN Number taken from ACATS Transfer Input (TI) Record 
ACATS populates this field with the value in the ‘Receiving 
Customer’s Primary Social Security’ field from the TI record.  
This field is used for PTFs only, when Fund is either the 
deliverer or the receiver.   
The rule above is true in all circumstances, both when the 
receiver submits the FR record and when ACATS uses a 
[[default]] registration. 
Note: The value in the ‘Receiving Customer’s Primary Social 
Security Number’ on the TI record may be different from the 
SSN/EIN on the FR record. 
 
ACATS Account Type Account Type taken from ACATS Transfer Input (TI) Record 
Gift/Donation Indicator Taken from ACATS Transfer Input (TI) Record 
 

---

## Page 36

Fund/Firm (PTF) Transfer Capability – Best Practices 
Definitions 36 
DEFINITIONS 
• ACATS - The Automated Customer Account Transfer Service (ACATS) is a system that automates and 
standardizes procedures for the transfer of assets in a customer account from one brokerage firm and/or 
bank to another. 
• ACATS-Fund/SERV - An interface system that links [[NSCC]]'s Automated Customer Account Transfer 
Service (ACATS) with the Fund/SERV system. The interface allows mutual fund [[Companies]] to 
electronically update their account registrations when a customer account is transferred between [[Broker]] s 
or re-registered directly with the fund company. 
• ACATS TI Record - An automated transfer initiation procedure that immobilizes the paper document 
Transfer Initiation Form (TIF) when a customer transfers their [[securities]] account from one brokerage firm 
and/or bank to another. 
• ACATS AT Record - An automated input record that allows for the submission of security assets 
(associated to a TIF) that are to be included in a customer account transfer. 
• ACATS FR Record - An automated input record used to re-register an ACATS transferred mutual fund 
[[Asset]] at the Mutual Fund Company. 
• CBRS - The Cost Basis Reporting Service (CBRS) is an automated system that provides ACATS [[Member]] 
firms (brokers and banks) with the ability to transfer customer cost basis information to each other on any 
[[Asset]] transferred through the Automated Customer Account Transfer Service (ACATS). Contra- Party – 
The [[Broker]]/dealer or customer to whom [[shares]] have been sold or transferred: or from whom [[shares]] have 
been purchased/transferred. 
• In-Kind Transfer – A transfer type that is the re-registration of mutual fund assets on the books of a fund 
or a firm. 
• LOA – Letter of Acceptance 
• Position Transfer Fund (PTF) - An ACATS transfer type that allows a [[Member]] firm, acting as either 
receiver or deliverer, to initiate a transfer to have a mutual fund [[Asset]] re-registered to or from its account 
at the fund, whereby the fund is also acting as the contra-side to the transfer. 
• SARSEP – A term used when referring to a plan that was created in 1998 as the result of the Salary 
Reduction Simplified Employee Pension Act. 
• ToRA – Transfer of Retirement Assets (ToRA) is a function of the Fund/SERV system. It is an automated, 
centralized system that enables the fund to jointly initiate, acknowledge, confirm and settle the transfer of 
the value of fund [[shares]] held in Retirement Accounts. 
• Transfer Initiation Form (TIF) - A paper document form completed by a brokerage customer when they 
transfer their account from one financial institution to another. The form includes customer detail 
information such as the account name, account type, account number, the firm where the account is 
currently held, and the customer's social security or tax identification number.  

---

## Page 37

Fund/Firm (PTF) Transfer Capability – Best Practices 
[[DTCC]] Resources – Links, Record Layouts and Related Rules 37 
[[DTCC]] RESOURCES – LINKS, RECORD LAYOUTS AND 
RELATED RULES 
Links to Related ACATS & ACATS-Fund/SERV Documentation: 
ACATS Documentation and Record Layouts can be located on the [[DTCC]] 
Learning site: 
https://dtcclearning.com/products-and-services/equities-clearing/automated-customer-account-transfer-service-
acats/acats-documentation.html 
ACATS-Fund/SERV documentation and record layouts are located at: 
https://dtcclearning.com/products-and-services/mutual-fund-services/fund-serv/acats-fund-serv.html 
 
ToRA Plan Matrix (June 2009) 
TRANSFER TO 
TRANSFER FROM 
Allowable 
Combinations 
IRA IRA 
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

---

## Page 38

Fund/Firm (PTF) Transfer Capability – Best Practices 
[[DTCC]] Resources – Links, Record Layouts and Related Rules 38 
 
 
 
Inherited 
Traditional 
IRA 
   
      Yes   
Inherited Roth 
IRA 
          Yes  
Inherited Roth 
Conversion 
IRA 
   
        Yes 

---

## Page 39

Fund/Firm (PTF) Transfer Capability – Best Practices 
[[NSCC]] Rule Changes 39 
[[NSCC]] RULE CHANGES 
Rule Change 
The rule change amended Rule 52 of [[NSCC]]’s Rules to accommodate the following types of account re- 
registrations: 
Transfer of customer mutual fund [[shares]] registration, held by a customer directly at a mutual fund company, to 
be re-registered in the name of a financial [[intermediary]] (e.g., [[Broker]]-dealer, bank or other custodian). 
Transfer of customer mutual fund [[shares]] registration, held by a financial [[intermediary]], to be re-registered as a 
direct customer position at the mutual fund company. 
The transfer of registration can be requested by a [[Member]] in the capacity of the party receiving the re-registration, 
or in its capacity of the party from which the registration is to be transferred. 
Completion of the registration transfer request requires that the contra-side [[NSCC]] Fund [[Member]] accepts the re-
registration request, in order for it to be processed through [[NSCC]]. 
In connection with such transfer request, the rule also provides that, unless the parties agree otherwise, the 
[[Member]] and Fund [[Member]] agree with one another to comply with certain legal responsibilities that are 
associated with the re-registration. The [[Member]] agrees that, in initiating such request, it has obtained the 
requisite authorization from the account holder and that it will provide a copy of it to the Fund [[Member]] upon 
request. It also indemnifies the Fund [[Member]] from any liabilities associated with the request, other than those 
relating to the negligence or misconduct of the [[Member]]. In connection with re-registrations of IRA and other 
tax-deferred accounts, a [[Member]] that makes the transfer request in its capacity as a successor custodian 
agrees that it is so-qualified under the provisions of the Internal Revenue Code. The Rule further states that the 
participants agree that any dispute between them relating to these provisions will be resolved directly between 
them, and that [[NSCC]] is not a party to such dispute and has no responsibility with respect to the enforcement 
or satisfaction of such provisions. In addition, the submission or processing of a transfer transaction through 
[[NSCC]] will not extinguish or affect any legal rights of the participants arising out of the transaction. This is 
similar to the provisions that are currently contained in [[NSCC]] rules as they relate to other mutual fund services 
of [[NSCC]] (see for example Rule 52, Section 46 relating to Fund/SERV and ToRA services, and Rule 50, 
[[Section 17]] relating to ACATS.) 
Automating and standardizing the re-registrations involved in account transfer processing that must otherwise 
be done on a manual basis reduces processing errors, lower costs and reduces the time needed to complete 
the transfer process, to the benefit of investors and the firms that process transfers on their behalf.  
Thus, the [[NSCC]] Rules have been expanded to satisfy the legal requirements and provide the needed 
protection for participants. Funds and firms engaging in the new Fund/Firm Transfer Capability may rely on the 
new and amended [[NSCC]] Rules in lieu of entering into multiple indemnification agreements. The rules support 
the timely implementation of increased automation of mutual fund transfer processing.

---

## Page 40

 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. 
TOGETHER, and the Interlocker graphic are registered and unregistered trademarks of The Depository Trust & 
Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: August 23, 2023 
Publication Code: MFS310 
Service: ACATS-Fund/SERV® 
Title: Fund/Firm (PTF) Transfer Capability – Best Practices  
   