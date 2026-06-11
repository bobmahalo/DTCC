---
title: "ToRA Business Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_tora_bus_guide_mfs215_20220629.pdf"
pages: 24
size: "502.6 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# ToRA Business Guide

**Original File:** [fs_tora_bus_guide_mfs215_20220629.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_tora_bus_guide_mfs215_20220629.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 24  
**File Size:** 502.6 KB  

---

## Page 1

 
 
 
FUND/SERV® 
TORA (TRANSFER OF RETIREMENT ASSETS) BUSINESS GUIDE 
JUNE 29, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and 
the Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: June 29, 2022 
Publication Code: MFS215 
Service: Fund/SERV
® 
Title: ToRA (Transfer of Retirement Assets) Business Guide 
 
 
  

---

## Page 3

 
 
 
 
CHANGE HISTORY 
Dates Description 
06/29/2022 ToRA Plan Type Matrix in this document has  been rebranded.  Additionally, 
Learning upgrade caused some link(s) to break.  Links have been corrected. 
 
 

---

## Page 4

 
 
TABLE OF CONTENTS 
Overview ............................................................................................................................................................ 6 
What is ToRA? ................................................................................................................................................. 6 
Overview ........................................................................................................................................................ 6 
Who Can Use the Service? ............................................................................................................................. 6 
Benefits .......................................................................................................................................................... 6 
How does ToRA Work? .................................................................................................................................. 6 
Background / Objective ................................................................................................................................... 8 
The Transfers Working Group ......................................................................................................................... 8 
The ToRA Task Force ..................................................................................................................................... 8 
Purpose of Industry Standardization ................................................................................................................ 8 
Increase Consistency Across the Industry ....................................................................................................... 8 
Increase Cooperation between Fund Families ................................................................................................. 9 
Best Business Practices ................................................................................................................................. 10 
Fund-to-Fund Procedural Differences ............................................................................................................ 10 
Exceptions to the Best Practices ................................................................................................................... 10 
Clean Up and Maintenance of ToRA Information ........................................................................................ 11 
Making ToRA Information Available to Associates ........................................................................................ 11 
File Types Available ...................................................................................................................................... 11 
Implementation of the ToRA Plan Type Matrix ............................................................................................. 13 
Creation and Use of a ToRA Plan Type Matrix .............................................................................................. 13 
Universal Standards....................................................................................................................................... 13 
Responsibilities of the Delivering Fund ......................................................................................................... 14 
Reject Code Standardization and Critical Data Elements ............................................................................. 14 
Delivering Fund Reject Code Standardization ............................................................................................... 14 
Critical Data Elements .................................................................................................................................. 14 
Critical Data Element Mismatches ................................................................................................................ 14 
Critical Data Element Reject Codes............................................................................................................... 15 
701 – SSN mismatch .................................................................................................................................... 15 

---

## Page 5

 
 
702 – Account Number Mismatch ................................................................................................................. 16 
703 – Account specified not invested in this Security Issue [[ID]] ....................................................................... 16 
704 – Plan Type mismatch ............................................................................................................................ 16 
Reject Codes for Other Data Elements ......................................................................................................... 17 
705 – Name Mismatch ................................................................................................................................. 17 
Assets Not Available Reject Codes ............................................................................................................... 17 
706 – [[shares]] Held in Escrow ........................................................................................................................ 17 
707 – Uncollected [[shares]] ............................................................................................................................. 18 
708 – Amount Requested not Available ......................................................................................................... 18 
Reject Codes That Indicate a Stop Code ....................................................................................................... 19 
709 – Stop Code on Account ......................................................................................................................... 19 
Responsibilities of the Receiving Fund ......................................................................................................... 20 
Collecting the Shareholder's Statement ........................................................................................................ 20 
Verifying Plan Type Portability ....................................................................................................................... 20 
Verifying ToRA Participation .......................................................................................................................... 20 
Collecting a Transfer Request Form .............................................................................................................. 20 
Reject Codes For Use By The Receiving Fund ............................................................................................. 21 
710 – Minimum purchase amount not met at receiving fund ........................................................................... 21 
711 – Maximum purchase amount exceeded at receiving fund ....................................................................... 21 
Definition of Terms .......................................................................................................................................... 22 
 

---

## Page 6

 
 
OVERVIEW 
What is ToRA? 
Transfer of Retirement Assets (ToRA) is a service offering of the National [[securities]] Clearing Corporation 
([[NSCC]]), a wholly owned subsidiary of The Depository Trust & Clearing Corporation ([[DTCC]]). 
Overview 
ToRA enables mutual fund [[Companies]] to jointly initiate, acknowledge, confirm and s ettle the value of mutual 
fund [[shares]] held in fund-sponsored IRA plans. ToRA is a separate function within Fund/SERV®, the industry 
standard for processing and settling mutual fund orders. 
ToRA is accessible via CPU-to-CPU links. 
Who Can Use the Service? 
Fund [[Companies]] that are members of [[NSCC]] and participate in Fund/SERV® can use the ToRA service. 
Benefits 
• Reduces the time required for retirement transfers to as little as three days 
• Decreases the manual paperwork and phone calls between funds and shareholders 
• Increases processing efficiency and reduces transfer costs 
• Reduces errors through the use of a standard record format and transfer process 
• Processes transfers of traditional IRAs, Roth IRAs, SAR SEPs, and others 
How does ToRA Work? 
ToRA works through transmission of records between the receiving fund and the delivering fund, with [[NSCC]] 
filtering and passing the information between the two funds. [[NSCC]] reviews the records to ensure all required 
information is present and c orrectly formatted. The content of the record, however, is to be verified by the 
delivering and receiving funds. 
The f low  chart in Figure 1.1 outlines the life cycle of a ToRA transaction. 
 
Note: 
For More Information please contact Wealth Management Services at (212) 855-8877. This description is for 
informational purposes only. This Service is governed by applicable Rules, Procedures, and Service Guides for each 
[[DTCC]] subsidiary, which contain the full terms, conditions, and limitations applicable to this Service. 

---

## Page 7

ToRA (Transfer of Retirement Assets) Business Guide 
Overview 7 
 
Figure 1.1 Graphical Representation of the ToRA Workflow 
Transfer Initiation 
The Receiving Fund electronically submits the ToRA transfer request record through Fund/SERV to the Delivering Fund. 
Transfer Acknowledgement 
The Delivering Fund Acknowledges the 
Transfer request 
Confirmation 
The Delivering Fund may submit a 
Confirmation between two and ten business 
days after submitting the Acknowledgement.  
The Confirmation states both the transfer 
and the [[liquidation]] of the position by the 
Delivering Fund at the price determined by 
the Delivering Fund. 
Reminder 
The [[NSCC]] sends daily reminders of any 
outstanding Transfer Acknowledgements or 
Confirmations 
 
Acknowledgement/Rejection 
The Delivering Fund may Acknowledge 
or Reject the trade within the two 
Reminder days 
 
No Action 
If no action is taken by the Delivering Fund 
within two business days, the trade is 
dropped from the system. 
Rejection 
The Delivering Fund Rejects the 
Transfer request.  A Rejection 
Notice is sent to the Receiving 
Fund informing them the trade 
will not be completed. 
 
[[settlement]] 
All Confirmed Transfers will appear 
on the Delivering Fund’s next 
available noon-day [[settlement]] file.  
The transaction will settle the same 
      
Reconfirmation 
The Delivering Fund may change any information previously 
submitted in the Confirmation, any time up before the 
[[settlement]] file is created. 
Cash Adjustments 
Either Fund can submit a Cash Adjustment record for a 
Transfer any time after the Transfer has settled. 
Exit by Receiving Fund 
The Receiving fund may cancel a Transfer any time before the 
[[settlement]] file is created. 
Reminder 
The [[NSCC]] sends daily Reminders of any 
outstanding Transfer Acknowledgements 
or Confirmations 
 

---

## Page 8

ToRA (Transfer of Retirement Assets) Business Guide 
Overview 8 
Background / Objective 
The Transfers Working Group 
The Investment Company Institute's ("ICI") [[Broker]] Dealer Advisory Committee ("BDAC") formed the Transfers 
Working Group in conjunction with [[DTCC]] in an effort to standardize transfer processing between brokers, 
banks and mutual fund [[Companies]] by leveraging the existing Automated Customer Account Transfer Service 
("ACATS") and ToRA applications. ACATS is used to systematically transfer mutual fund [[shares]] between two 
financial intermediaries. ToRA is used to systematically transfer retirement assets between two fund [[Companies]] 
by selling assets at the delivering fund and buying them at the receiving fund. Though these processes are 
largely automated, there may be situations where mutual fund transfer processing can be a manually intensive 
event. As a result of this inefficiency, transfer processing can be costly to both financial intermediaries and fund 
[[Companies]]. 
The ToRA Task Force 
As part of ongoing efforts to improve transfer processing, the [[transfer agent]] Advisory Committee ("TAAC") 
formed a subcommittee focused on improving ToRA. The ToRA Task Force developed the following 
objectives: 
• Standardize ToRA use across the industry 
• Substantially reduce the number of rejected trades 
• Increase cooperation between funds 
• Increase ToRA use throughout the industry 
 
These improvements are critical to the efficient transfer of retirement assets from one Fund Company to 
another. They will also serve to facilitate expanded transfer capabilities with [[Broker]]-dealers on fund-to-[[Broker]] 
and [[Broker]]-to-fund transactions. 
The ToRA Task Force developed this Business Guide to recommend best practices and explain the business 
reasons for improving the way ToRA is used. The Task Force also incorporated high-level technical instruction 
on how to code service provider and fund company systems in concert with the best practices outlined in this 
document. 
Purpose of Industry Standardization 
Increase Consistency Across the Industry 
Rejected trades cause delays in the completion of transfers, which can frustrate the shareholder and increase 
the cost of doing business for funds. If all system providers and fund [[Companies]] code their systems according 
to the ToRA Systems Guide, ToRA trades will no longer reject due to inconsistencies between systems. 

---

## Page 9

ToRA (Transfer of Retirement Assets) Business Guide 
Overview 9 
Reject codes will be assigned according to the ToRA reject code best practices described in Responsibilities of 
the Delivering Fund. If fund [[Companies]] assign reject codes based on a clearly defined set of universal data, 
the fund [[Companies]] receiving rejected trades will be able to quickly and accurately identify the cause of the 
rejects. They can then resolve the issue and re-submit the trade without calling the rejecting fund to clarify 
information. In addition, funds may be able to use this information to resolve trade issues without requiring the 
shareholder to contact the rejecting fund, leading to a more efficient process. 
Increase Cooperation between Fund Families 
Prior to development of the Best Practices outlined in this guide, responsibility for requesting a transfer through 
ToRA was placed solely on the receiving fund. 
Unfortunately, it is not always possible to obtain all necessary documentation from a shareholder or [[Broker]] to 
generate a ToRA trade. Information provided by shareholders can be incomplete or inaccurate. Through 
adoption of these best practices, increased responsibility will be placed on the delivering fund to resolve trade 
issues whenever possible by adopting the best practice recommendations in this document. 
• Delivering funds should utilize the critical data elements outlined within this guide (see Responsibilities of 
the Delivering Fund ) to identify what information is necessary for completing a transfer request through 
ToRA. 
• Delivering funds should 'pend' trades for review whenever possible, rather than rejecting them back to the 
receiving fund. 
 
Use of the best practices found in this Business Guide increases the reliability of transactions sent via the 
ToRA system. Fund [[Companies]] are able to predict the outcome of transfer requests through ToRA, prior to 
submitting the trade. Trades with incorrect or insufficient information can be researched on the front end to 
reduce the potential for trade rejects. The fund [[Companies]] will take on the responsibility of trying to resolve 
trade discrepancies using every means necessary to increase the likelihood that trades will settle 
successfully. 
In addition, funds are held more responsible for keeping updated and accurate information on file with [[NSCC]] 
in both their Fund and Security Issue Profiles. Fund [[Companies]] and system providers can make this 
information available to their processors by utilizing the Fund/SERV® Security Master Daily – 02110802 file. 
This will help make fund-level attributes available to all funds participating in Fund/SERV®, which will help to 
make trade processing more efficient and accurate. 

---

## Page 10

ToRA (Transfer of Retirement Assets) Business Guide 
Best Business Practices 10 
BEST BUSINESS PRACTICES 
Fund-to-Fund Procedural Differences 
Across the industry, fund families have different procedures for their associates to f ollow for ToRA transactions. 
In most instances, these procedures were developed using a combination of: 
• Fund interpretation of legislation 
• Fund interpretation of ToRA use guidelines 
• Fund interpretation of shareholder expectations 
 
Variances in these interpretations among fund [[Companies]] can cause inconsistencies in the use of the ToRA 
product. These inconsistencies can make it difficult to know what to expect when requesting assets from 
another fund, in addition to complicating the reject resolution process. Fund [[Companies]] are encouraged to 
review their current procedures with a critical eye, searching for ways to move these processes in line with the 
best practices outlined in this document. 
Exceptions to the Best Practices 
Not all fund [[Companies]] will be able to fully implement the best practice guidelines. However, each fund 
complex should implement as many as possible in order to streamline the ToRA process across the industry. 
Example:  
The best practice recommendations for the delivering funds are to not use the shareholder name as a method of account 
verification through the ToRA system. A fund may feel strongly that shareholder name verification is necessary to ensure 
the security of the account. In this instance, the Fund would continue to use shareholder name as a verification point but 
would choose to "pend" requests where the shareholder name on the request did not match the account registration. 
Associates would review these transactions and determine on a case-by-case basis that certain name variations (such 
as OConnel and O'Connel) are acceptable. In these instances, the processor would complete the trade in good 
confidence that account security has not been compromised. 

---

## Page 11

ToRA (Transfer of Retirement Assets) Business Guide 
Clean Up and Maintenance of ToRA Information 11 
CLEAN UP AND MAINTENANCE OF TORA 
INFORMATION 
• ToRA Participation: Fund [[Companies]] can sign up for ToRA by contacting Wealth Management 
Services Marketing at (212) 855-8877.  If a fund's ToRA participation status changes, the fund 
company should notify [[NSCC]] immediately. 
• Update [[Member]] Profile Information: Fund [[Companies]] should maintain up-to-date information on 
knowledgeable ToRA contacts within their organization. 
• Update Security Issue Information:  Fund [[Companies]] may add, modify, or delete a Security [[ID]] by 
accessing the Fund/SERV Security Issue [[ID]] Update Form on the MyDTCC portal 
https://portal.[[DTCC]].com.  This should be done both periodically and any time a security issue has a 
status change that will affect its ability to be traded through [[NSCC]].  
o Remove funds that are no longer trading via the Fund/SERV System, for example closed or 
merged funds that can no longer be transferred through ToRA.  
o Ensure that all Security IDs loaded to the [[NSCC]] system as eligible for trading through ToRA are 
coded as eligible on the fund’s system. 
• Update "Fund" (Security Issue) Name:  The "name" field of 60 bytes allows for more clear and 
accurate information to be displayed in this field. 
o Names that include abbreviations should be consistent across all fund [[Companies]]. 
o The Share Class name should be included at the end of the fund name. The words "share class" are 
not necessary – just the class indicator (such as A, B, etc.). However, if "share class" is used, it 
should be used on all names for consistency. 
• Update Share Class Field: A separate share class field is available for optional use on the    
Fund/SERV® Security Master Daily and Weekly Files. 
Making ToRA Information Available to Associates 
Fund [[Companies]] should make the information in the (daily and weekly) - Fund/SERV® Security Master Files 
available to their associates for more effective processing. These files carry information regarding fund 
participation and Security IDs that are eligible to trade through ToRA. Associates who are not provided this 
information are more likely to request ToRA trades from invalid fund [[Companies]] and invalid Security Issue IDs.  
File Types Available 
Daily (02110802): This file is created by [[NSCC]] every evening from the Fund/SERV® Security Master File. 
Fund [[Companies]] who download this file will have the most up-to- date fund information available. 

---

## Page 12

ToRA (Transfer of Retirement Assets) Business Guide 
Clean Up and Maintenance of ToRA Information 12 
Example:  
Fund A downloads the Daily 802 file from [[NSCC]] every evening. Fund B liquidates and closes Security [[ID]] 555555 on 
Tuesday and updates the information with [[NSCC]] in their closing process. Wednesday morning, the associates at Fund A 
are aware that Security [[ID]] 555555 is no longer available for trading through ToRA and will no longer request this Security 
[[ID]]. As a result, ToRA trades that would have been rejected will not be sent. 
 
Weekly (02110335): This file is created by [[NSCC]] every Friday evening. Fund [[Companies]] who download this 
file will have information that is current as-of close of business on Friday. 
Example:  
Fund C downloads the Weekly 335 file from [[NSCC]] on Friday evenings. Fund B liquidates and closes Security [[ID]] 555555 
on Tuesday but associates at Fund C will not be notified that Security [[ID]] 555555 is not available for trading through 
ToRA until Fund C downloads the Weekly file on Friday. As a result, several ToRA trades are requested by Fund C on an 
invalid Security [[ID]], creating ToRA rejects. 

---

## Page 13

ToRA (Transfer of Retirement Assets) Business Guide 
Implementation of the ToRA Plan Type Matrix 13 
IMPLEMENTATION OF THE TORA PLAN TYPE MATRIX 
Creation and Use of a ToRA Plan Type Matrix 
The ToRA Task Force drafted a ToRA Plan Type Matrix, which is intended as a quick-reference guide to 
[[Asset]] portability for fund [[Companies]]. The matrix illustrates the plan types compatible for transfer through 
ToRA at the time it was created. 
 
Note 
The matrix shown in Table 4.1 on the next page is an exhibit only. Since the taxable treatment and eligibility of retirement 
plan rollovers is subject to change from time to time, it is recommended that ToRA users prepare a similar Matrix for their 
own operations and ensure it is maintained consistent with current IRS rules, regulations or other legislation such as the 
Economic Growth and Tax Relief Reconciliation Act of 2001or any amendments thereof. 
Only non-taxable transfers between like accounts and/or plan types are allowed via ToRA. Tax reportable 
transactions, such as a 401(k) rolling into an IRA, or a Traditional IRA converting into a Roth IRA are out of the 
ToRA scope. 
Universal Standards 
The ToRA Plan Type Matrix should be provided to associates as a reference guide and should be used prior to 
submitting trades through ToRA to ensure plan type portability. Verifying this information prior to submitting 
transfer requests will decrease ToRA rejects caused by incompatible plan types. In addition, fund [[Companies]] 
and system providers should code their systems for the new ToRA Plan Type Matrix. Additional information 
on required system updates can be found on the learning site in the ToRA Systems Guide. 
Table 4.1 ToRA Plan Type Matrix (Exhibit Only) 
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
Traditional to 
Roth 
Conversion 
Inherited 
Traditional 
IRA 
Inherited 
Roth IRA 
Inherited Roth 
Conversion IRA 
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
       
Coverdell Ed. IRA      Yes       
SAR-SEP IRA       Yes      
Roth Conversion 
IRA 
            
Traditional to 
Roth Conversions 
   Yes    Yes Yes    
Inherited 
Traditional IRA 
         Yes   
Inherited Roth 
IRA 
          Yes  
Inherited Roth 
Conversion IRA 
           Yes 
 
 
 

---

## Page 14

ToRA (Transfer of Retirement Assets) Business Guide 
Responsibilities of the Delivering Fund 14 
RESPONSIBILITIES OF THE DELIVERING FUND 
Reject Code Standardization and Critical Data Elements 
Delivering Fund Reject Code Standardization 
The use of Fund/SERV® reject codes specifically for ToRA transactions is central to the drive toward industry 
standardization. There is little guidance surrounding the proper usage of existing reject codes for ToRA 
transactions, so they are used differently by each fund company. This lack of standardization makes it difficult 
to interpret the true reason for a rejected trade, resulting in the need to seek further clarification through phone 
calls between the fund [[Companies]]. 
To reduce the need for time consuming calls, the ToRA Task Force has developed a set of Fund/SERV® 
reject codes designated for use with ToRA transactions. These reject codes are described in subsequent 
articles within this guide. 
The Reject Codes are separated into three (3) categories: 
• Critical Data Elements. For more information, see Critical Data Element Reject Codes  in this guide. 
• Other Data Elements. For more information, see Reject Codes for Other Data Elements  in this guide. 
• Assets not Available. For more information, see Assets Not Available Reject Codes in this guide.  
• Stop Codes. For more information, see Reject Codes that Indicate a Stop Code in this guide. 
Critical Data Elements 
Each fund company should focus their account verification efforts on a set of critical data elements within each 
ToRA transfer request. These elements can be used to c orrectly identify the shareholder, investment position, 
and account, allowing each organization to verify that assets are not being moved fraudulently or in error. 
Critical data elements include: 
• Shareholder Tax [[ID]] (SSN) 
• Shareholder Account at Delivering Firm 
• Shareholder Security Issue [[ID]] at Delivering Firm 
• Shareholder Account/Plan Type 
Critical Data Element Mismatches 
The objective of the critical data element review is to enable funds to release assets for tra nsfer as requested 
In an instance where the critical data elements are not an exact match, rather than rejecting the trade back to 
the receiving fund the delivering fund should 'pend' the trade for internal review. 

---

## Page 15

ToRA (Transfer of Retirement Assets) Business Guide 
Responsibilities of the Delivering Fund 15 
In many instances, a "best three out of four" philosophy can be adopted for the critical data elements, provided 
the available information clearly identifies the assets being moved. If so, the delivering fund should release 
assets as requested. 
Example 1:  
John Doe has assets invested in a Roth IRA (account number 1234, Security [[ID]] 555555) at Fund Company A. Fund 
Company B requests the assets from Fund Company A – however, the request has a typographical error, and instead of a 
Security [[ID]] of 555555, Company B enters 555556. Because John has only one fund position associated with that account, 
and because all other Critical Data Elements match (SSN, Account Number, and Account Type), Company A could, in 
good confidence, release the assets to Company B. There is no necessary concern over John's identity or the validity of the 
request. 
Example 2:  
Jane Smith has assets invested in a Traditional IRA (account number 5678, Security IDs 555556 and 555557) at Fund 
Company A. Fund Company B requests the assets from Fund Company A – however, the request has a typo, and i nstead 
of a Security [[ID]] that is valid for the listed Account Number, Company B submitted the request with Security [[ID]] 777778. 
Although all other Critical Data Elements match, Company A cannot clearly tell which of the funds in Jane's account 
Company B is requesting, so it is reasonable that they reject the trade for unclear information. 
Critical Data Element Reject Codes 
Codes 701 through 704 should be issued when there are multiple data elements that [[DO]] not match. If one data 
element does not match, the trade should be pended for associate review and then processed if the assets 
being transferred are clearly identified. 
However, if there are multiple critical data elements that [[DO]] not match, the trade should be rejected to the 
receiving fund. The receiving fund should then review the information for accuracy, obtaining information from 
transfer documents, statements, and the shareholder. The receiving fund will need to re-submit a new ToRA 
trade via Fund/SERV®. 
701 – SSN mismatch 
• Example: Radar O'Neil's account at Fund A lists his SSN as 111-11-1111. His account at Fund B lists his 
SSN as 111-11-1112 due to a typo when the account was being established. A ToRA transaction will not 
be possible for this shareholder until the SSN is corrected at Fund B. 
• Action Needed: Pend the trade for associate review. 
• Business Reason: As one of the critical data elements, the shareholder's social security number ("SSN") 
at the delivering fund must match the SSN submitted by the receiving fund in order to verify the 
shareholder's identity and secure the account. 
• Be st  Practice Recommendation: The receiving fund should verify the shareholder's identity, including their 
SSN, in compliance with the U.S. Patriot Act. When opening a new mutual fund account, the shareholder 
may be required to present their Social Security card to help prevent incorrect submission of social 
security numbers. 
 
If the SSN on the delivering account is not identical to the receiving account, the delivering fund should 

---

## Page 16

ToRA (Transfer of Retirement Assets) Business Guide 
Responsibilities of the Delivering Fund 16 
pend the trade for review by an associate. If all other critical data elements are correct, and the SSN 
discrepancy review uncovers a typo, transposition or some other clerical error the trade should be 
processed. 
702 – Account Number Mismatch 
• Example: Fund (A) requests funds through ToRA from Fund B. The shareholder did not provide a 
statement to Fund A. When Fund A submitted the trade, the account number was missing a digit 
• Action Needed: Pend the trade for associate review. 
• Business Reason: The account number at the delivering fund and the account number submitted by the 
receiving fund must match. This is required as a means of verifying the shareholder's identity and to secure 
the account. This is one of the critical data elements. 
• Best Practice Recommendation: The receiving fund should verify account numbers and other information 
on the shareholder's current statement prior to submitting trades through ToRA. This will help prevent 
entry of incorrect information. If an incorrect account number is entered, the delivering fund should pend 
the trade for review by an associate. If all other critical data elements are correct, the trade should be 
processed. 
703 – Account specified not invested in this Security Issue [[ID]]  
• Example: Fund A requests a ToRA trade from Fund B. The record submitted by Fund A reflects a 
Security [[ID]] that is not a part of the shareholders' portfolio. 
• Action Needed: Pend the trade for associate review. 
• Business Reason: The shareholders' account number is not invested in the Security [[ID]] requested. This is 
one of the critical data elements. 
• Best Practice Recommendation: Receiving funds should review the most recent shareholder statement 
and utilize the daily 02110802 file to obtain valid account and Security [[ID]] information prior to submitting 
ToRA trades. This will reduce the number of trades rejected due to invalid Security [[ID]]/account 
combinations, and the number of calls needed to obtain the correct Security numbers. Delivering funds 
should pend these trades for review by an associate. If the account and investment position can be 
determined, the trade should be processed. If the lack of a correct Security prevents definitive account 
identification, the trade should be rejected. 
704 – Plan Type mismatch 
• Example: Fund (A) requests a ToRA transaction for their Roth IRA from Fund B's 403(b) account. 
• Action Needed: Reject the trade. 
• Business Reason: Retirement account types are only eligible to transfer into specific types of retirement 
accounts. ToRA will only allow trades between eligible plan types. This is one of the critical data elements. 
• Best Practice Recommendation: The receiving fund should review the ToRA Plan Type Matrix prior to 
initiating the trade. Only trades between compatible plan types should be submitted. In the event the 
receiving fund submits a trade for an incompatible plan type, the delivering fund should provide information 
on the account's existing plan type in the new Delivering Fund Plan Type field on the Fund Reject (100) 

---

## Page 17

ToRA (Transfer of Retirement Assets) Business Guide 
Responsibilities of the Delivering Fund 17 
record to the receiving fund1. This will reduce the number of calls needed to resolve ToRA rejects. Please 
note that trades between ineligible plan types cannot be allowed due to tax requirements, even if all other 
information on the trade is correct. 
 
Reject Codes for Other Data Elements 
Although many fund [[Companies]] use shareholder name when verifying the validity of a transfer via paper. It is 
recommended that the shareholder name not be used as a verification point on the ToRA system. Formatting 
of shareholder name may vary fund- to-fund, causing unnecessary rejects. 
If a fund company's compliance review yields a requirement to verify the shareholders' name, then reject 
code 705 (Name Mismatch) should be used. 
705 – Name Mismatch 
• Example: Fund A requests a ToRA transfer from Fund B. Fund A has the shareholder's name formatted 
as John Q. Public. Fund B has the shareholder's name formatted as Johnny Public. 
• Action Needed: Pend the trade for associate review. 
• Business Reason: The shareholder's name does not match on the delivering and receiving funds' 
systems. Verification of name is a means to ensure the shareholder's identity and to secure the account. 
• Best Practice Recommendation: The name should not be used as a point of verification due to differences 
in formatting between various systems. However, should a fund determine that the name field must be 
reviewed; every effort should be made to pass the trade. Formatting differences (such as O'CONNEL 
versus OCONNEL) should not cause a rejected trade. For true name mismatches, reject code 705 (Name 
Mismatch) should be generated to give the receiving fund a clear idea of what action is needed to 
complete subsequent trades for the shareholder. 
 
Other data elements provided in the ToRA records are not essential to verifying the
 identity of the 
shareholder and the assets they are requesting for transfer. 
Assets Not Available Reject Codes 
Prior to requesting trades through ToRA, fund [[Companies]] should review a recent copy of the shareholder's 
statement. Doing so will help identify an accurate share balance and dollar value for the account being 
requested. The delivering fund can use reject codes 706 through 708 when the amount requested is not 
available in the account. 
706 – [[shares]] Held in Escrow 
• Example 1: Fund A requests a ToRA trade from Fund B for "all assets." Parts of the assets held at Fund 
B are in escrow. 
 
1 See [[DTCC]] Important Notice # 6874 "Enhancements to Fund/SERV® and Networking for Transfer of Retirement [[Asset]] (ToRA) Service and Enhancements 
to Fund/SERV® and Networking for Section 529 Plan Processing," dated September 17, 2009. 

---

## Page 18

ToRA (Transfer of Retirement Assets) Business Guide 
Responsibilities of the Delivering Fund 18 
• Example 2: Fund A requests a ToRA trade from Fund B for $100.00 (NAV = 
• $10/share). The balance of the account at Fund B is 11 [[shares]], but 2 of them are held in escrow. 
• Action Needed: Pend the trade for associate review. 
• Business Reason: [[shares]] in the account are held in escrow and there are not enough non-escrow 
[[shares]] to complete the ToRA trade. ToRA trades cannot be performed against escrowed [[shares]]. 
• Best Practice Recommendation: If possible, the delivering fund should remove the escrow from the 
account and release the requested assets to the receiving fund. 
707 – Uncollected [[shares]] 
• Example: Fund (A) requests a ToRA trade from Fund B. The shareholder had a recent automatic 
investment from their bank into Fund B. The investment will be held in Uncollected [[shares]] for five (5) 
days. 
• Action Needed: Pend the trade for associate review. 
• Business Reason: Assets requested have not settled due to a recent trade. Assets must settle (become 
"collected") prior to transfer. 
• Best Practice Recommendation: The delivering fund should review the trade and complete the transaction 
for the 'collected' balance. The return file sent to the receiving fund should indicate there are remaining 
assets by using the new Uncollected Share Amount field on the ToRA Acknowledgement (211) record. 
As a result, the receiving fund must wait ten (10) business days, and then re-submit a trade for the 
remaining assets. [1] 
708 – Amount Requested not Available 
• Example 1: The shareholder instructs Fund (A) to transfer 13 [[shares]] from Fund (B) but does not have a 
statement available. Fund (A) requests the trade from Fund (B) through ToRA, but the actual share 
balance of the account is only 10 [[shares]]. 
• Example 2: Fund (A) reviews a statement for the account at Fund (B), which shows a balance of $112. 
Fund (A) requests a ToRA trade from Fund B for $100, but due to market fluctuations, the value of the 
account is now only $98. 
• Action Needed: Pend the trade for associate review. 
• Business Reason: The receiving fund requested a specific dollar amount. That amount is not available in 
the account. 

---

## Page 19

ToRA (Transfer of Retirement Assets) Business Guide 
Responsibilities of the Delivering Fund 19 
• Best Practice Recommendation: The receiving fund should review the most recent statement to ensure 
that specific dollar or share values are available. If not, the receiving fund should request an "all assets" 
transfer. The delivering fund should pend the trade for review by a processor. If the amount requested 
and the available balance of the account are within a reasonable variance (usually due to market 
fluctuation between statement production and the date the request is made), the processor should release 
the amount of [[shares]] or dollars available in the account as though the trade requested was for "all 
assets." If the amount requested and the available account balance are grossly different, the trade should 
be rejected, and reject code 708 (Amount Requested not Available) should be applied. 
 
Please note that this code should not be used to indicate uncollected [[shares]] in an account. 
Reject Codes That Indicate a Stop Code 
Many funds add stop codes to accounts to indicate that processing should be handled cautiously, or to prevent 
processing from occurring. Stop codes can be used to indicate many situations, including: 
• Returned mail (RPO) l Deceased shareholder l Divorce proceedings 
• Fraud alert 
 
Reject Code 709 (Stop Code on Account) is used by the delivering fund to indicate that a stop has been placed 
on the account, and that further action is required. 
709 – Stop Code on Account 
• Example: Fund A requests a ToRA trade from Fund B. Fund B shows a stop code on the account due to 
potentially fraudulent activity reported by the shareholder two years ago. 
• Action Needed: Trade is rejected. 
• Business Reason: The account requested has a stop code (i.e., restriction) on it. A fund can place a 
restriction on an account due to required documents that have not been returned by the customer. A 
restriction can be placed if fraudulent activity is suspected, or if notification is received that the shareholder 
is deceased or in the process of divorce proceedings. Some funds will place a restriction on an account or 
put it into a "black- out period," when a retirement plan has moved from one fund to another. 
• Best Practice Recommendation: The receiving fund must verify the validity of the shareholder's address 
due to U.S. Patriot Act requirements. Because of this, stop code rejects should not be sent for returned 
mail (RPO) or stop mail restrictions – the address at the receiving fund should be correct, even if the 
address at the delivering fund is not. For all other stop code types, the trade should be a hard reject. 
 

---

## Page 20

ToRA (Transfer of Retirement Assets) Business Guide 
Responsibilities of the Receiving Fund 20 
RESPONSIBILITIES OF THE RECEIVING FUND 
The receiving fund should ensure that every transfer request is as accurate and thorough as possible, prior to 
submitting the trade through the ToRA System. In order to be successful, the receiving fund must collect a 
complete set of documents from the shareholder prior to submitting trades. 
Collecting the Shareholder's Statement 
The shareholder's statement includes several pieces of information that are essential to completing a successful 
ToRA transfer. 
• The shareholder's correct account number at the delivering fund 
• The shareholder's investment positions at the delivering fund 
• The shareholder's plan type at the delivering fund 
• The shareholder's share balance and dollar value of their account at the delivering fund 
 
Failing to collect a copy of the most recent statement can lead to trades being rejected for incomplete or 
inaccurate information. 
Verifying Plan Type Portability 
After identifying the shareholder's plan type at the delivering fund, the receiving fund's a ssociate should verify 
that the plan type they have established is compatible with the delivering fund's plan type. This can be done by 
reviewing the ToRA Plan Type Matrix. To facilitate this review, systems should not only be coded using this 
Matrix, but it should be made available to associates for review. 
Verifying ToRA Participation 
Fund [[Companies]] should be downloading the Daily 02110802 file from the [[DTCC]] website. For assistance on 
how to accomplish this, contact your Relationship Manager. The 02110802 file includes fund company 
participation in the ToRA service, Security [[ID]] eligibility to trade through ToRA and other information. Processors 
should review this i nformation prior to submitting trades in order to avoid rejects. 
Collecting a Transfer Request Form 
The receiving fund should collect a transfer request form from their shareholder that includes important data 
needed to complete a transfer of assets.  
 

---

## Page 21

ToRA (Transfer of Retirement Assets) Business Guide 
Responsibilities of the Receiving Fund 21 
Reject Codes For Use By The Receiving Fund 
Reject codes are available for use by the receiving fund. These codes are used when the assets received are 
not in compliance with their fund's minimum or maximum investment limits. As a best practice, funds should not 
request assets that exceed fund maximums or [[DO]] not meet fund minimums. 
The reject codes for the receiving funds are contingent on fund minimums and maximums that are associated with 
their investment positions. These codes can be used to reject assets back to the delivering fund. The receiving 
[[Institutions]] should use both the share balance and dollar value that appears on the shareholder statement to 
determine if the shareholder is complying with the fund's minimum and maximum investments, prior to submitting 
trades. 
710 – Minimum purchase amount not met at receiving fund  
• Example: Fund A requests "all assets" from Fund B through ToRA. Fund A's minimum purchase amount 
is $50, but the account at Fund B holds only $23. 
• Action Needed: The trade is rejected back to the delivering fund. 
• Business Reason: Some funds have minimum purchase requirements that must be met in order for a 
transaction to be completed. 
• Best Practice Recommendation: Receiving funds should review the shareholder's most recent statement 
to determine if fund minimums will be met prior to requesting funds  through ToRA. This will reduce the 
number of rejected ToRA trades. 
711 – Maximum purchase amount exceeded at receiving fund  
• Example: Fund (A) requests "all assets" through ToRA from Fund (B) into their B- Share Index fund, 
which has a maximum purchase limit of $50,000. The account at Fund B has $52,000. 
• Action Needed: The trade is rejected back to the delivering fund. 
• Business Reason: Some funds have maximum purchase limits on backend loaded funds, which can 
charge a higher fee and can be less financially beneficial to high- dollar investors. 
• Best Practice Recommendation: Receiving funds should review the shareholder's most recent statement 
to determine if fund maximums will be exceeded or submit a trade for only the maximum amount allowed 
for purchases. This will reduce the number of rejected ToRA trades. 
 
 

---

## Page 22

ToRA (Transfer of Retirement Assets) Business Guide 
Definition of Terms 22 
DEFINITION OF TERMS 
The terms defined below and used throughout this document are standard to the mutual fund industry. Fund 
[[Companies]] should endeavor to use these terms when training their associates, which will aid in fund-to-fund 
communications. 
 
Term Definition 
ToRA Transfer of Retirement Assets ("ToRA") is a function within [[NSCC]] 
Fund/SERV® that enables mutual fund [[Companies]] to jointly initiate, 
acknowledge,  confirm and settle the value of mutual fund [[shares]] held 
in fund supported retirement plans. 
ICI The Investment Company Institute ("ICI") is the national association of 
U.S. investment [[Companies]], including [[Mutual Funds]], close-end funds, 
exchange-traded funds, and unit investment trusts. 
TAAC The [[transfer agent]] Advisory Committee ("TAAC") is an ICI [[Member]] 
committee that provides a forum to discuss mutual fund [[transfer agent]] 
recordkeeping,  shareholder  servicing, regulatory and compliance 
related matters. 
[[DTCC]] The Depository Trust and Clearing Corporation ("[[DTCC]]"), through its 
[[NSCC]] subsidiary, provides clearing, [[settlement]] and information 
services for mutual fund transactions by linking fund [[Companies]] to 
their distribution partners. 
[[NSCC]] The National [[securities]] Clearing Corporation ("[[NSCC]]"), a wholly 
owned subsidiary of the [[DTCC]], provides centralized clearance, 
[[settlement]] and information services to fund [[Companies]]. ToRA is one of 
the [[NSCC]] service offerings for mutual fund transaction processing. 
Fund/SERV® A service offering of the [[NSCC]] that provides centralized processing of 
purchase, redemption, and exchange orders, and provides 
participants with a single daily net [[settlement]]. 
Fund Company A fund company establishes a family of [[Mutual Funds]] for distribution to 
investors. Individual [[Mutual Funds]] ("funds" or "Security Issue IDs") 
have different investments objectives and meet varying [[investor]] needs. 
Edit A set of code within a system that identifies data points within a ToRA 
record and reviews for inconsistent information. Edits are what drives 
ToRA requests to a pended or rejected status. 
 
 
 

---

## Page 23

ToRA (Transfer of Retirement Assets) Business Guide 
Definition of Terms 23 
Term Definition 
Originator The fund company that initiates the transaction through ToRA. 
Receiving Fund The fund company that initiates a ToRA transaction and receives 
retirement plan assets from the delivering fund, through the ToRA 
System. 
Delivering  Fund The fund company that delivers Retirement Plan Assets to the 
receiving fund through the ToRA System. 
Record The data file transmitted between the receiving fund, the [[NSCC]], and 
the Delivering Fund. This data file contains information about the trade 
and dictates to the system what assets are moving, where they are 
going, where they are coming from, and how they are to be moved. 
Reject A reject is an instruction to send the trade back through the [[NSCC]] to 
the other Fund without completing the request due to bad data. This is 
also known as a "hard reject." 
Pend To hold the trade for review by an associate in order to potentially 
resolve questionable data and complete the trade. This is also known 
as a "soft reject." 
Weekly 02110335 File A weekly downloadable file produced by [[NSCC]]. This file provides 
fund [[Companies]]' ToRA participation information and includes details 
on Security IDs available for ToRA trading. 
Daily 02110802 File A daily downloadable file produced by [[NSCC]]. This file provides fund 
[[Companies]]' ToRA participation information and includes  details on 
Security IDs available for ToRA trading.* 
 
* Please note that this is the recommended file for download, as it provides the most accurate and up-to-date 
information to funds. 
 
 

---

## Page 24

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 