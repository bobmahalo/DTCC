---
title: "Cost Basis Reporting Service (CBRS)-Supplemental User Guide for Mutual Funds"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs_cbrs_supplemental_guide_mfs357_20240119.pdf"
pages: 111
size: "2493.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Cost Basis Reporting Service (CBRS)-Supplemental User Guide for Mutual Funds

**Original File:** [mfs_cbrs_supplemental_guide_mfs357_20240119.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs_cbrs_supplemental_guide_mfs357_20240119.pdf)  
**Category:** Other  
**Total Pages:** 111  
**File Size:** 2493.1 KB  

---

## Page 1

 
 
 
Mutual Fund Services 
COST BASIS REPORTING SERVICE (CBRS)-
SUPPLEMENTAL USER GUIDE FOR MUTUAL 
FUNDS 
January 19, 2024 

---

## Page 2

 
 
HISTORY OF REVISIONS 
Dates Revisions 
January 19, 2024 This document is updated with 2024 branding.  Content reviewed and refreshed.  Links in 
Appendix A Resource Reference Materials updated to articles. Info no longer available on 
IRS website. 
January 25, 2022 Content reviewed and refreshed due to rebranding of this document. 
September 30, 2019 Updated link to CBRS User Guide on Learning 
June 10, 2019 Reviewed and reference links updated to point to [[DTCC]] Learning Center. 
October 25, 2013 Changes effective November 18, 2013 in accordance with Important Notice A7665 (posted 
July 3/2013) and Important Notice A7702 (posted September 16, 2013) 
December 7, 2012 Changes effective February 4, 2013 in accordance with Important Notice A7472 (posted 
August 16, 2012) 
December 13, 2011 Changes effective December 5, 2011 in accordance with Important Notice A7256 (posted on 
July 29, 2011) 
May 10, 2011 Initial Publication. 
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Executive Summary ............................................................................................................................................. 6 
Background and Overview of [[Mutual Funds]] Guide ............................................................................................ 6 
Introduction and Background ............................................................................................................................. 8 
Background ......................................................................................................................................................... 8 
About this Guide ................................................................................................................................................. 8 
Special Considerations and Recommended Practices for [[Mutual Funds]].................................................... 10 
Lot Depletion Methodology ...............................................................................................................................10 
Average Cost Considerations for Transfers .....................................................................................................11 
Average Cost - [[Broker]] [[default]] Method & Changes ........................................................................................11 
Average Cost–Affirmative Election & Revocations .........................................................................................12 
Partial Average Cost Transfers of Like Registration under [[Broker]] [[default]] and/or Affirmative Election  .........12 
Single-Account Average Cost Transfers .........................................................................................................13 
Transfer Statement Corrections ........................................................................................................................13 
Processing Error Adjustment ..........................................................................................................................13 
Updated Tax Lot Information Adjustment ........................................................................................................14 
Corporate Action Adjustment ..........................................................................................................................15 
In-Kind Retirement Distributions to Non-Retirement Accounts ........................................................................15 
Firm-Initiated Redemptions on Fund-Controlled Accounts ...............................................................................15 
Networking Changes that Impact Cost Basis Reporting Responsibilities  ........................................................16 
The Role of Agents in Cost Basis Reporting ....................................................................................................17 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]]  .................................. 18 
Introduction .......................................................................................................................................................18 
General CBRS Considerations .........................................................................................................................18 
CBRS User Master File Considerations ...........................................................................................................21 
CBRS [[Asset]] Records .......................................................................................................................................22 
CBRS Tax Lot Records ....................................................................................................................................32 
Transfers of Mutual Fund [[securities]] ................................................................................................................ 42 
Overview ...........................................................................................................................................................42 
Transfer Methods and Tax Reporting .............................................................................................................42 

---

## Page 4

 
 
[[DTCC]] for Cost Basis Reporting ......................................................................................................................44 
CBRS Record Layouts ....................................................................................................................................52 
MyDTCC Web Portal .......................................................................................................................................52 
Cost Basis Reporting Transfer Types and Examples .....................................................................................53 
ACATS PTF Transfers and CBRS ....................................................................................................................53 
Introduction ......................................................................................................................................................53 
ACATS PTF – Firm Initiated In-Kind Transfer (“Firm Pull”) .............................................................................53 
ACATS PTF – Firm Initiated In-Kind Transfer to Fund (“Firm Push”) .............................................................54 
Special Considerations for ACATS PTF Transfers .........................................................................................55 
Networking Transfers and CBRS ......................................................................................................................58 
Introduction ......................................................................................................................................................58 
Overview–Networking Transfers .....................................................................................................................58 
Firm Initiated Networking Fund to Firm Transfer ............................................................................................59 
Firm Initiated De-Networking Firm to Fund Transfer .......................................................................................60 
Special Considerations for Networking ...........................................................................................................61 
Manual Transfers and CBRS ............................................................................................................................62 
Introduction ......................................................................................................................................................62 
Overview..........................................................................................................................................................63 
Special Considerations for Manual Transfers .................................................................................................68 
Transfer Examples – CBRS [[Asset]] and Tax Lot Records .................................................................................69 
Examples......................................................................................................................................................69 
Average Cost ...................................................................................................................................................70 
Gifted [[shares]] for FIFO Account ......................................................................................................................77 
Inherited [[shares]] for FIFO Account .................................................................................................................82 
Exception/Correction Processing ....................................................................................................................88 
Frequently Asked Questions: Transfer Reporting .......................................................................................... 91 
Appendix A: Resource Reference Materials ................................................................................................... 96 
A1 Internal Revenue Code & IRS Information ..................................................................................................96 
A2 IRS Forms ...................................................................................................................................................96 
A3 White Paper .................................................................................................................................................96 

---

## Page 5

 
 
A4 Information on [[DTCC]]’s Cost Basis Reporting Service (CBRS) ..................................................................96 
Appendix B: White Paper –  Recommended Practices for Firm -Initiated Fund/SERV ® Redemptions on 
Fund-Controlled Accounts ................................................................................................................................ 97 
B1 ICI White Paper ...........................................................................................................................................97 
B2 Investment Company Institute Memorandum ...........................................................................................105 
Appendix C: Glossary ...................................................................................................................................... 107 
 

---

## Page 6

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Executive Summary 6 
EXECUTIVE SUMMARY 
Background and Overview of [[Mutual Funds]] Guide 
The Emergency Economic Stabilization Act of 2008 was signed into law on October 3, 2008, which includes 
provisions from the Energy Improvement and Extension Act of 2008 that requires brokers to provide cost basis 
reporting for [[securities]]. The Internal Revenue Service (“IRS”) and Treasury Department released final 
regulations for implementing cost basis and other information reporting requirements on October 12, 2010. 1 
The purpose of these requirements is to ensure that investors accurately report gains and losses of applicable 
[[securities]] in their annual tax filings with the IRS. Under these regulations, brokers, banks, transfer agents, 
[[Mutual Funds]] and [[Custodians]] are required to report adjusted cost basis, gross proceeds, and the holding period 
of disposed [[securities]] (short-term or long-term) to the IRS and investors. The requirements apply to “covered 
[[securities]],” as defined by the IRS. The regulations also require that cost basis transfer reporting statements 
must be sent for assets of covered security types. The transfer reporting requirements are effective for 
transfers of covered mutual fund [[securities]] began on or after January 1, 2012. 
As a result of the legislation and final regulations, the cost basis reporting regime includes enhanced 
requirements for average cost, specific identification, wash sales, corporate actions, and gifted and inherited 
[[shares]]. The accurate calculation of adjusted basis for the various methodologies must be supported by firms 
who are subject to the reporting requirements outlined in this document. 
One of the most significant requirements under this legislation is the transfer reporting rules. Accurate basis 
information must be sent on transfer reporting statements when assets are moved to another firm for both full 
and partial transfers, within 15 days of when a transfer takes place.
2 
Additionally, receiving firms are required to request basis if it is not received within 15 days. If basis is still not 
received after such request, the [[shares]] transferred will be considered “non-covered.” 
Late or corrected transfer statements may require receiving firms to make adjustments to cost basis for 
investors. Post transfer adjustments (that could result from transaction corrections or corporate actions such as 
returns of capital) may require firms to send corrected transfer statements, which in turn will require receiving 
firms to make adjustments to cost basis records. These types of activities also may require amendments to 
Forms 1099 previously reported to the IRS and investors 3. Given the large volumes of transfers that occur 
between firms today, standardization and automation is necessary to achieve operational efficiencies and 
assist firms in meeting their compliance [[obligations]] for transfer reporting under the regulations . A lack of 
automation and use of manual transfer statements may be both costly and inefficient for both sending and 
receiving firms. 
In order to assist firms in complying with the transfer reporting requirements, the Depository Trust and Clearing 
Corporation ([[DTCC]]) has enhanced its Cost Basis Reporting Service (CBRS).
4 [[DTCC]] initially launched CBRS 
in 2003 to enable [[Broker]]-dealer and bank client firms to pass cost basis on assets transferred via [[DTCC]]’s 
 
1 Specific details regarding the legislation, regulations, and revised reporting forms may found in the Resource References contained in Appendix A . 
2 Under these regulations, a transfer statement must include: (i) the date the statement is furnished; (ii) the name, address and telephone number of the applicable 
person furnishing the statement; (iii) the name, address and telephone number of the [[Broker]] receiving [[custody]] of the security; (iv) the name and account number 
of the customer(s) for the account from which the security is transferred and, if different, the name and account number of t he customer(s) for the account to 
which the security is transferred; (v) the Committee on Uniform Security Identification Procedures ([[CUSIP]]) number of the security transferred; (vi)the date the 
transfer was initiated and the [[settlement]] date of the transfer (if known), and (vii) the total adjusted basis of the security, the original acquisition date of the security, 
and, if applicable, any holding period adjustment required due to a wash sale.  As provided in the proposed regulations, the person furnishing the transfer 
statement and the receiving [[Broker]] may agree to combine this information in any format or to use a code in place of one or more required items.  
3 Final regulations require brokers to report adjustments to cost basis. Corrected Transfer Reporting is required when an adjus tment is made within 18 months 
following [[settlement]] of the original transfer. Corrected IRS and shareholder 1099- B reporting is required when adjustment is made within 3 years following 
[[settlement]] of the original transfer. 
4 [[DTCC]] operates its businesses through several operating subsidiaries.  

---

## Page 7

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Executive Summary 7 
Automated Customer Account Transfer Service (ACATS). Prior to 2011, the CBRS service was utilized 
voluntarily by many ACATS clients. With the passage of cost basis legislation, the industry, including mutual 
funds, embraced the need for a system that would provide a centralized communications hub that would 
mitigate risk and promote standardization in order to meet their regulatory requirements in an efficient and 
cost-effective manner. 
In response to the needs expressed by the industry, [[DTCC]] established a cross functional committee with 
members from different segments of the industry, who played a key role in defining the system’s functionality 
and record layouts in order to help financial intermediaries that are reporting brokers comply with cost basis 
transfer reporting regulations. This extended the efficiencies and capabilities of the CBRS system to transfer 
agents, issuers, [[Mutual Funds]], custodian banks and [[Broker]]-dealers in order to move cost basis information 
from one financial firm to another in a standardized, automated, and timely fashion in a secure environment. 5 
This service was launched in 2010 and has continued to be enhanced to meet the needs of the industry in 
order to comply with cost basis reporting rules. 
Because [[Mutual Funds]] have unique attributes that must be considered when transferring cost basis 
information, a separate industry task force was formed in 2009 to develop a mutual fund user’s guide to 
augment [[DTCC]]’s CBRS User Guide, which is applicable to all security types.
6 This supplemental guide was 
created to encourage standardization and automation and contains recommended practices and resources that 
may be useful to firms implementing cost basis transfer reporting for [[Mutual Funds]]. The mutual fund guide is 
organized to address special considerations and recommended practices for mutual fund transfers and 
includes information on: lot depletion, average cost specific rules, transfer statement corrections, in- kind 
retirement distributions, the role of agents in cost basis transfers and recommended practices for firm- initiated 
Fund/SERV
®7 redemptions in fund-controlled accounts. The guide also provides annotated record layouts for 
[[Mutual Funds]] and related best practices, frequently asked questions about mutual fund transfers and transfer 
statements, a glossary of key terms and a resource listing of helpful information to assist reporting brokers for 
[[Mutual Funds]]. 
In December of 2011, this guide was updated to provide additional information, including examples and 
recommended practices, with respect to transfer reporting in the context of ACATS and ACATS -Fund/SERV, 
Networking transactions8, and leveraging CBRS for manual transfers. Recommended industry practices were 
also updated in response to issued IRS guidance9. 
The guide was further updated in November of 2012 in accordance with Important Notice a 7472. 
This supplemental guide is intended to assist both business and systems personnel and service providers 
tasked with implementing the cost basis rules for [[Mutual Funds]]. 
 
5 CBRS does not tell users what transactions trigger the need to pass cost basis or when to send basis, nor does it calculate or provide any reconciliation 
capabilities between expected and received records.  
6 Further information on the [[DTCC]]’s CBRS documentation may be found in the Resource References in Appendix A . 
7 Fund/SERV is a service offered by National [[securities]] Clearing Corporation (“[[NSCC]]”), a subsidiary of [[DTCC]].  
8 ACATS, ACATS-Fund/SERV and Networking are services offered by [[NSCC]] , a subsidiary of [[DTCC]]. 
9 The Internal Revenue Service issued Notice 2011- 56, which provides interim guidance on certain issues relating to cost basis reporting. The notice can be 
found on the IRS’s website at http://www.irs.gov/pub/irs-drop/n-11-56.pdf. 

---

## Page 8

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Introduction and Background 8 
INTRODUCTION AND BACKGROUND 
Background 
In early 2009, the Investment Company Institute (ICI), through its [[Broker]]/Dealer Advisory Committee (BDAC), 
brought together an industry Cost Basis Reporting (CBR) task force (the BDAC CBR Task Force, or “Task 
Force”) consisting of [[DTCC]], fund families, [[Broker]]-dealers, and service providers to address the requirement to 
transfer cost basis information associated with transfers of [[shares]] between tax reporting brokers.  
The Task Force worked in conjunction with two other ICI task forces on implementing cost basis reporting for 
[[Mutual Funds]]—those sponsored by the ICI Tax Committee and the ICI Transfer Agency Advisory Committee 
(TAAC). The Tax Committee focused its attention on the tax, legal and legislative processes surrounding 
mandatory cost basis, while the TAAC task force addressed the broader operational and shareholder servicing 
impacts of integrating mandatory cost basis into fund transfer agency operations.  
About this Guide 
This guide, focuses on the transfer of cost basis information for [[Mutual Funds]] between reporting brokers. It is 
supplemental and should always be used in conjunction with the CBRS User Guide, which can be found at 
https://dtcclearning.com/products-and-services/equities-clearing/cbrs.html under CBRS Users. 
The supplemental guide includes the following: 
• An Executive Summary, focused on senior-level executives within an organization, which frames the 
broad issues and considerations surrounding mandatory cost basis reporting , specific to the transfer of 
basis between reporting brokers. 
• An Introduction, providing background and an overview to the materials in this Guide.  
• A discussion of Special Considerations and Recommended Practices for [[Mutual Funds]],  which 
presents an overview of some of the major issues and considerations impacting cost basis transfer 
statements. Issues covered include: 
o Lot depletion methodology and its impact on transfers. 
o Average cost-specific rules which affect transfer statement options. 
o Transfer statement correction scenarios and considerations. 
o In-kind retirement distributions. 
o Firm-initiated redemptions on fund-controlled accounts. 
o Networking changes that impact cost basis reporting responsibilities; and  
o The role of agents in cost basis transfers. 
• Annotated [[Asset]] and Tax Lot Records for [[DTCC]]’s Cost Basis Reporting Service (CBRS) specifically 
focused on select fields that include mutual fund-specific details, recommended practices, and other 
considerations. 
• A discussion of Mutual Fund Transfer Processing and CBRS. This section provides an overview on 
transfers of mutual fund [[securities]] and covers (1) ACATS and ACATS-Fund/SERV, (2) Networking, and 
(3) manual transfer scenarios that should invoke a cost basis transfer reporting stat ement. A detailed 
description and processing workflows are provided for each transfer type, as well as special 
considerations and recommended practices. This section also includes examples that identify key fields 
and values for the various transfer types for Cost Basis reporting purposes that should be utilized when 
populating the CBRS record layouts. 
• Frequently Asked Questions (FAQs) about mutual fund transfers and transfer statements. 

---

## Page 9

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Introduction and Background 9 
• Resource Reference Materials that include helpful information to assist reporting brokers in the Mutual 
Fund space in implementing mandatory cost basis reporting, including the generation of transfer 
statements. 
• A copy of the Industry white paper, “Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled 
Accounts”, which details a necessary shift in tax reporting responsibilities brought about by mandatory 
cost basis reporting. 
• A Glossary of key terms used in the context of cost basis transfers between reporting brokers.  
 

---

## Page 10

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Special Considerations and Recommended Practices for [[Mutual Funds]] 10 
SPECIAL CONSIDERATIONS AND RECOMMENDED 
PRACTICES FOR [[Mutual Funds]] 
The transfer reporting requirement has many complexities that may impact its successful execution. The  Task 
Force identified a number of issues that impact the mutual fund transfer reporting process. The following 
special considerations are addressed in this chapter: 
• Lot depletion methodology and its impact on transfers. 
• Average cost-specific rules which affect transfer statement reporting. 
• Transfer statement correction scenarios and considerations. 
• In-kind retirement distributions. 
• Firm-initiated redemptions on fund-controlled accounts. 
• Networking changes that impact cost basis reporting responsibilities; and 
• The role of agents in cost basis transfers. 
 
For each issue identified above, an overview of the topic is presented, along with industry recommended 
practices, business decisions or considerations for mutual fund cost basis reporting. 
Lot Depletion Methodology 
The Task Force spent considerable time analyzing and discussing the recommended practices for reporting 
brokers when depleting tax lots. While seemingly a firm-by-firm decision, there is some desire to be consistent 
across reporting brokers, to minimize questions that could occur when lot depletion activities vary between 
reporting brokers for transfer transactions. 
For redemptions or transfers absent external instructions, 10 the IRS requirement is that tax lots in an account, 
whether covered or non-covered,11 are selected based on acquisition date from oldest to newest, or in first-
in/first-out (FIFO) order. The final IRS regulations also clarified that unless the customer specifically identifies 
the [[securities]] to be sold; the [[Broker]] must deplete and report the sale of any [[shares]] in the account with 
unknown acquisition dates first, regardless of the Cost Basis calculation method employed. 
Industry Recommended Practice:  
Absent shareholder instructions, all unknown [[shares]] should be depleted first followed by (i) the earliest non-covered [[shares]] 
acquired first (FIFO), then (ii) the earliest covered [[shares]] acquired first (FIFO). 
The Task Force recommendation is consistent with the IRS’ long-term goal of matching cost basis reported by 
shareholders and reporting brokers. 
Although the regulations provide that FIFO applies on an account-by-account basis, a shareholder may have 
non-covered [[shares]] with an acquisition date that is later than the acquisition date of covered [[shares]]. Thus, an 
alternative practice may be to deplete non-covered and covered [[shares]] on a combined FIFO basis, even 
though the [[shares]] are in two deemed-separate accounts for cost basis reporting purposes. 
 
10 The most common external instruction received is some form of proportional movement of tax lots, which often occurs when shar es are being transferred into 
a new legal ownership arrangement (registration), such as in response to an inheritance or divorce. 
11 Covered and non-covered [[shares]] are treated (“deemed”) as two separate accounts for cost basis reporting purposes.  

---

## Page 11

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Special Considerations and Recommended Practices for [[Mutual Funds]] 11 
Average Cost Considerations for Transfers 
The average cost method has some unique considerations with regard to the cost basis information provided 
by the delivering reporting [[Broker]] when transferring [[shares]]. Some questions in this area are left to 
interpretation, as the final regulations did not specifically address certain issues. The industry was tasked with 
striking a balance to ensure compliance with the final regulations, but also provide shareholders the maximum 
flexibility in utilizing cost basis methodologies availed to them for tax reporting purposes.  
Average Cost - [[Broker]] [[default]] Method & Changes 
Final IRS regulations permit reporting brokers (funds and firms) to select average cost as their [[default]] 
calculation method for [[Mutual Funds]]. In this situation, shareholders have two options for managing their 
accounts, which can impact how cost basis information must be provided when transferring [[shares]]:  
Prospective Change: Shareholders may change prospectively at any time from the average cost [[default]], if 
desired, by notifying their reporting [[Broker]] in writing of their change in method. All covered [[shares]] acquired 
prior to the requested change from a [[Broker]]’s [[default]] method of average cost must be tracked and transferred 
reflecting the average cost at the time of the shareholder’s change in method.  
Change from [[Broker]] [[default]]: The mutual fund industry asked the IRS to allow shareholders to choose a 
permitted method (e.g., FIFO) other than the [[Broker]]’s [[default]] method of average cost for existing [[shares]] if no 
redemptions have occurred in the account, rather than applying such a method choice prospectively only (as 
was required in the final regulations). Funds and firms thus could allow their customers to choose any method 
for all fund [[shares]] in an account, up until the first redemption. In response to this request, the IRS issued 
additional guidance
12 that permits shareholders to choose a method other than the [[Broker]]’s [[default]] of average 
cost under such circumstances.13 
Pursuant to Notice 2011-56, the shareholder must choose another method within one year following the 
notification of the reporting [[Broker]]’s [[default]] method, or prior to the date of first sale, transfer, or other 
disposition of [[shares]] subject to the [[Broker]] [[default]] method (the “change in method” period). Brokers at their 
discretion may extend this period longer than one year, but not beyond the first redemption.  
• If a shareholder chooses another method for an account other than average cost prior to transfer, the 
basis in the [[shares]] to which the method choice applies is the basis before averaging. Thus, if a transfer 
were to occur after the change, individual cost basis for the applicable share lots would be transferred. 
• When the period for choosing another basis, method ends for any qualifying reason, all covered [[shares]] 
acquired prior to the end of the change period must be tracked and transferred reflecting the average cost.  
• S hareholders also may request a change in writing from their average cost basis method prospectively at 
any time (including after the end of the “change in method” period). If a transfer subsequently occurs, the 
delivering [[Broker]] will send lot information that was calculated using two different basis methods:  
o Those valued using the average cost basis calculated prior to the change from average cost,  
o Those valued as individual share lots acquired after the change from average cost.  
 
For scenarios in which there is a request for a full or partial transfer of [[shares]] between reporting brokers 
involving accounts with identical or like registrations (an “in-kind” transfer), where the “change in method” 
period is still open (e.g., there has been no disposition of [[shares]] or “change in method” request prior to 
 
12 The Internal Revenue Service issued Notice 2011 -56, which provides interim guidance on certain issues relating to cost basis reporting. The notice can be 
found on the IRS’s website at http://www.irs.gov/pub/irs-drop/n-11-56.pdf. 
13 The IRS refers to this as a “change in method.” 

---

## Page 12

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Special Considerations and Recommended Practices for [[Mutual Funds]] 12 
transfer), there are two prevailing interpretations 14 that reporting brokers are utilizing in determining the basis 
information to be transferred: 
• Certain reporting brokers are treating the transfer of the [[shares]] to another reporting [[Broker]] as a 
“disposition of [[shares]],” which terminates the “change in method” period. In this scenario, covered [[shares]] 
are valued at average cost and then transferred. 
• Other reporting brokers are not treating the in-kind transfer as a disposition because it is not a change in 
ownership, but simply a change in reporting [[Broker]]. Because there has been no disposition resulting in a 
change in ownership, the “change in method” period is not considered terminated. These reporting 
brokers are transferring [[shares]] reflecting the adjusted cost basis of the individual share lots, and not the 
average cost basis. Under this approach, the shareholder retains the greatest flexibility in managing their 
cost basis options for the [[shares]] transferred into the new account at the receiving reporting [[Broker]].  
Average Cost–Affirmative Election & Revocations 
Once a shareholder affirmatively elects average cost, they have the ability to revoke, in writing, this election. 
The revocation period is in effect for the earlier of one year following the date of the affirmative average cost 
election, or the date of first sale, transfer, or disposition of those [[shares]] following the election. Brokers at their 
discretion may extend the revocation period longer than one year, but not beyond the first redemption.  
• If a shareholder revokes their affirmative average cost election in an account prior to transfer, the basis in 
the [[shares]] to which the revocation applies is the basis before averaging. Thus, if a transfer were to occur 
after revocation, individual cost basis for the applicable share lots would be transferred.  
• When a revocation period ends, all covered [[shares]] acquired prior to the end of the revocation period must 
be tracked and transferred reflecting the average cost. 
• Shareholders also may request a change in writing from their average cost basis method prospectively at 
any time (including after the end of a revocation period). If a transfer subsequently occurs, the delivering 
[[Broker]] will send lot information that was calculated using two different basis methods:  
o Those valued using the average cost basis calculated prior to the change from average cost,  
o Those valued as individual share lots acquired after the change from average cost.  
 
For scenarios in which there is a request for a full or partial transfer of [[shares]] between reporting brokers 
involving accounts with identical or like registrations (an “in-kind” transfer), where the revocation period is still 
open (e.g., there has been no disposition of [[shares]] or requests to change methods prior to transfer), the same 
prevailing interpretations discussed above in 
Average Cost - [[Broker]] [[default]] Method & Changes are utilized in 
determining the basis of information to be transferred. 
Partial Average Cost Transfers of Like Registration under [[Broker]] [[default]] 
and/or Affirmative Election 
Cost basis regulations require that except as provided under the computation of the average cost basis (where 
[[shares]] sold or transferred are deemed to be the [[shares]] first acquired, and thus are depleted in FIFO order) a 
transfer statement of less than an entire position in an account (partial transfer), absent a shareholder’s timely  
identification of the [[shares]] to be transferred, are depleted unknown acquisition date first, followed by the 
earliest [[shares]] acquired FIFO in the account. 
Where a partial transfer of like or identical registration occurs and average cost has been affirmatively elected 
by the shareholder or is the [[Broker]]’s [[default]] method and the shareholder is currently within the revocation or 
“change in method” period, respectively, there are two possible methods for determining which basis 
 
14 These scenarios are based on different interpretations of the Cost Basis regulations. Unless the IRS issues guidance on this matter, the industry’s approach 
will be guided by individual business decisions. Such decisions will be based on interpretations of the regulations, and other operational and legal considerations. 

---

## Page 13

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Special Considerations and Recommended Practices for [[Mutual Funds]] 13 
information to transfer. As with full transfers, certain reporting brokers are treating the partial transfer as a 
“disposition of [[shares]]” that terminates the revocation/“change in method” period.  
Therefore, those brokers are sending basis information using the average cost determined on the whole 
account before the partial transfer. Alternatively, other brokers are not treating a partial transfer of like 
registration as a disposition that ends the revocation/“change in method” period. Thus, these brokers are 
sending the adjusted cost basis of the individual share lots, rather than the average cost.  
It was suggested that for partial share transfers of like registration a reporting [[Broker]] could include both the 
average cost and adjusted original cost of each individual tax lot on transfer reporting statements, so receiving 
brokers can decide which basis information to use. Unfortunately, this is not a workable solution because the 
average cost number on the delivered [[shares]] is impacted by the cost basis of the [[shares]] not transferred. Thus, 
it is highly likely that a cost basis ‘out of balance’ situation would result for the shareholder if the same cost 
basis methodology was not applied by both the delivering and receiving reporting brokers when valuing partial 
transfers. 
Single-Account Average Cost Transfers 
Once average cost is affirmatively elected by the shareholder the reporting [[Broker]] has at its discretion, the 
[[Option]] of utilizing the “Single Account” cost basis method. This means that all [[shares]] in an account, regardless 
of acquisition date, will be considered covered for reporting and included in the average cost calculation. The 
Single Account election can only be “unwound” by a shareholder’s written revocation of average cost, which 
would follow the revocation guidelines outlined in Average Cost–Affirmative Election & Revocations section 
above. 
If an account under single-account average cost is fully or partially transferred to a like registration while [[shares]] 
are within their revocation period (meaning no disposition of [[shares]] has occurred and the time threshold has 
not been met), the reporting [[Broker]] must value all [[shares]] transferred under the single- account average cost. 
This is because the reporting [[Broker]]’s single account election is irrevocable by the [[Broker]] and can only be 
“unwound” by a shareholder revocation of average cost. Without shareholder revocation, there is no [[Option]] to 
send the adjusted basis of individual [[shares]]. 
Transfer Statement Corrections 
Despite all best intentions, there will inevitably be a need to correct information sent in a transfer statement. 
Such need may result from processing errors on the originating account, ensuing tax lot information received 
that impacts a previously generated transfer statement, or due to a corporate action such as a return of capital, 
which adjusts cost basis. 
Required Practice:  
In all instances, the reporting [[Broker]] in possession of the [[shares]] on the effective date of a correction is responsible for 
correcting the cost basis and sending updated transfer statements. 
Like original processing, a reporting [[Broker]] has 15 calendar days to forward corrected transfer statements, 
once the reporting [[Broker]] is made aware, they have received updated information. This obligation exists, based 
on final IRS regulations, for 18 months following the [[settlement]] date of the original transfer transac tion. 
Processing Error Adjustment 
An example of an adjustment originated by a processing error would be a transaction that should have been 
processed prior to a transfer to a new reporting [[Broker]], resulting in a different share amount transferred. The 
submitting reporting [[Broker]] would be required to send updated information to correct the transaction itself, plus 
the corresponding corrected transfer statement. 

---

## Page 14

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Special Considerations and Recommended Practices for [[Mutual Funds]] 14 
Required Practice:  
Reporting brokers must send sufficient details to tie the corrective processing to the original transaction. The receiving 
reporting [[Broker]] must update both the record-keeping and tax lot systems with the corrective transaction information. 
Transfer Corrections When Share Quantity Decreases through Correction 
Members of the Task Force analyzed the ramifications of transfer statement corrections for various cost basis 
reporting scenarios. As a result, the Task Force adopted a recommended practice of fully cancelling (voiding, 
reversing) the original transaction, and replacing it with a new transaction for the correct share amount. The 
transaction cancellation should reinstate the tax lots with the original delivering [[Broker]] and remove the related 
tax lots from the original receiving [[Broker]]’s records as if the original transfer transaction never occurred. 
Neither reporting [[Broker]] should generate or expect to receive a corrected cost basis transfer statement 
as a result of the cancellation transaction. 
Upon reprocessing the transfer transaction for the correct amount, a new transfer statement requirement is 
invoked, and cost basis would be processed and reported for the correct share request.  
Industry Recommended Practice:  
Industry recommended practice when correcting a transfer transaction is to cancel the original transfer transaction and 
deliver a (to and from) transfer cancelation using the Networking F55 Activity record utilizing the appropriate Transfer 
Cancelation transaction types. 
The original transaction is then voided by both parties, any impact from previously exchanged CBRS records are deleted 
from both the delivering and receiving entities’ cost basis systems, and a subsequent new transfer transaction and related 
CBRS records are transmitted. 
This recommended practice applies to cancellations/corrections which affect all or a portion of the original transfer and 
related cost basis records. 
Transfer Corrections When Share Quantity Increases through Correction 
When the number of transferred [[shares]] should be greater than the amount received as a result of an 
adjustment or corrective action, the party initiating the transfer may choose to initiate a second (separate) 
transfer for the omitted [[shares]]. Conversely, the aforementioned Industry Recommended Practice can also be 
followed. 
Identifying Transfer Cancellations 
For those parties receiving [[NSCC]] Networking Activity record F55, transfer cancellations will be identified by 
Transaction Types 33 (Transfer From–Cancellation) and 34 (Transfer To–Cancellation). Please refer to the 
Networking discussion in the Transfers Section of this guide for more details on these Transaction Types and 
how they are used to facilitate processing adjustment transactions as detailed in the Industry Recommended 
Practice above. 
Updated Tax Lot Information Adjustment 
In a multiple-reporting [[Broker]] transfer, and because tax lot information may lag actual transaction processing 
by one or more days, it is possible that a reporting [[Broker]] may have to transfer “pending cost basis” tax lots as 
part of a transfer statement. 
For example, Reporting [[Broker]] A is in the process of submitting a transfer statement to Reporting [[Broker]] B, 
when Reporting [[Broker]] B must submit a transfer statement covering the same [[shares]] that may have 
subsequently been transferred to Reporting [[Broker]] C. Depending on how Reporting [[Broker]] B approaches the 
situation, it may elect to send a transfer statement with “pending cost basis” noted. Once Reporting [[Broker]] A 
provides the final cost basis information to Reporting [[Broker]] B, Reporting [[Broker]] B generates a corrected 
transfer statement–with updated cost basis information–for Reporting [[Broker]] C. 
Final IRS regulations permit 15 calendar days following transfer [[settlement]] for delivery of the transfer 
statement. 

---

## Page 15

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Special Considerations and Recommended Practices for [[Mutual Funds]] 15 
Industry Recommended Practice:  
Reporting brokers should send available tax lot information in a transfer statement as soon as practicable and follow-up 
with any corrected or adjusted transfer statements for any pending cost basis information. 
Waiting to send the transfer statement until pending cost basis is received may risk a delay ed delivery of the 
transfer statement beyond 15 calendar days, which would cause the submitting reporting [[Broker]] to be out of 
compliance with transfer reporting requirements and would unnecessarily trigger a transfer statement request 
from the receiving reporting [[Broker]]. 
Corporate Action Adjustment 
There are certain fund events, such as returns of capital, which impact an account’s cost basis. Often, these 
declarations are made weeks or months after they are actually effective. 
The reporting [[Broker]] holding [[shares]] as of the effective date of the corporate action – regardless of the 
calendar date the corporate action is announced – is responsible for adjusting the cost basis of the affected tax 
lots and issuing a corrected transfer statement, in the event those [[shares]] were transferred to another reporting 
[[Broker]]. 
In-Kind Retirement Distributions to Non-Retirement Accounts 
In some unique situations, mutual fund [[shares]] can be transferred in-kind from a retirement account into a non-
retirement account. When this occurs, final IRS regulations require that a transfer statement be sent to the 
receiving [[Broker]] indicating that all [[shares]] transferred are non-covered for cost basis purposes. 
This situation is especially problematic for most mutual fund [[Companies]] because t he cost basis reporting 
system is not linked to retirement accounts–which by statute are otherwise exempt from the cost basis 
reporting requirements. The submitting reporting [[Broker]] must somehow generate a transfer statement, 
regardless of whether this is done systematically or manually. Likewise, the receiving reporting [[Broker]] must 
follow the requirement to request a transfer statement if not received within 15 calendar days.  
However, if the reporting [[Broker]] processes the corresponding retirement distribution by redeeming [[shares]] in 
the retirement account and purchasing corresponding [[shares]] in the non-retirement account at the receiving 
firm, this transaction scenario would not be subject to the cost basis transfer reporting requirement. Based on 
industry feedback, this is the most common way that mutual fund [[Companies]] process such transactions today.  
Please note:  
There is an information reporting impact to the [[Broker]] and shareholder for the scenario above. A purchase into the non-
retirement account would create covered [[shares]] for the reporting [[Broker]] and shareholder; whereas the in-kind transaction 
would allow the [[shares]] transferred to continue to be non-covered [[securities]] for 1099 reporting purposes. However, 
shareholders are still required to accurately report their basis in [[securities]] moved to a non-retirement account, regardless of 
whether the [[securities]] transferred are non-covered or covered for information reporting purposes. 
Firm-Initiated Redemptions on Fund-Controlled Accounts 
Prior to mandatory cost basis reporting, the industry followed a long-standing practice with regard to reporting 
gross proceeds from redemptions on fund-controlled accounts. If a firm initiated the redemption on a fund-
controlled account, the firm assumed tax reporting responsibilities for the redemption.  
Industry Recommended Practice:  
All required tax reporting completed on “fund-controlled” mutual fund accounts are the responsibility of the fund. 
The white paper entitled, “Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts” is provided 
in Appendix B of this document. The white paper provides detailed information on the basis for this 

---

## Page 16

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Special Considerations and Recommended Practices for [[Mutual Funds]] 16 
recommended practice and identifies areas where reporting brokers should review and remediate operational 
and legal arrangements that may be impacted by implementing the recommended practice.  
The primary reason for this change in practice is due to the impracticalities of retaining the former 
recommended practice of splitting Form 1099-B tax reporting on a given account. Since the cost basis 
reporting must accompany gross proceeds reporting, retaining the former recommended practice would require 
coordinated and/or dual tax lot tracking by firms and funds involved in the transactions. Extensive and costly 
enhancements would be required for Fund/SERV
® identification of specific lot transactions which, given the low 
volumes of these types of transactions, was not warranted or supported by industry clients . 
Firms may still initiate redemption activity against a fund-controlled account. Cost Basis lot depletion will be 
driven by the shareholder’s elected calculation method on the fund account, or, in the absence of an affirmative 
election, the fund’s [[default]] cost basis calculation method. Funds will report the gross proceeds and 
corresponding cost basis information for such transactions. 
It should be noted that the IRS recognizes both the firm and fund as entities with [[Broker]] reporting 
responsibilities in this situation and permits either to report the activity. The nature of the recommended 
practice is to consolidate reporting [[Broker]] responsibility, in this limited scenario, from the firm to the fund.  
Networking Changes that Impact Cost Basis Reporting 
Responsibilities 
Within [[NSCC]]’s Networking service, there is a capability for a Networking Maintenance B51 record to be sent to 
the fund which changes the Networking Matrix Level on an existing account. Any change from Matrix Level 3 or 
Trust-Networked Level 0—to Matrix Level 4 or Non-Networked Matrix 0 (or vice versa) also changes the party 
that is responsible for cost basis tracking and 1099 reporting for the account. 
Industry Recommended Practice:  
[[NSCC]]’s Networking service provides functionality that enables a Networking Maintenance B51 record to process a matrix 
level change on an account held at the fund. In some cases, the B51 Maintenance requested changes the control of the 
account and the tax reporting responsibility. Therefore, any networking maintenance change on an account that would 
change the existing tax reporting responsibility on mutual fund [[shares]] should be processed through a transfer transaction 
and not by utilizing the Networking Maintenance B51 record. 
The B51 Matrix Level change which changes tax reporting responsibilities creates issues in that there is no 
transfer transaction with which to associate the CBRS transfer statement. Likewise, other than a clerical 
transaction, there is no transaction-based audit trail to track the transfer. Finally, most fund systems strive to 
retain clarity about the responsible party for an account’s tax reporting for the entire year. The [[Broker]]/dealer is 
responsible for the tax reporting while the account is held in a firm-controlled Matrix Level, and the intra-year 
Matrix Level change can create tax reporting (and related cost basis reporting) challenges for the year in 
question by blending reportable and non-reportable activity in the same fund account. 
Also, within Networking is the “Change of Dealer” function, whereby an existing fund account has its 
[[Broker]]/dealer identifiers updated to a different firm. This may or may not also be accompanied by a change in 
Matrix Level (typically between firm-controlled Matrix Level 3 and Trust-Networked Level 0). This scenario most 
commonly occurs as a result of a firm merger or when a registered representative switches the firm to which 
they are associated. 
In these situations, it is incumbent upon the firms involved in the Change of Dealer process to ensure that cost 
basis information is transferred for the applicable accounts. In most instances, a fund’s cost basis reporting 
responsibilities are not impacted by these types of transactions. 
 
 
 
 

---

## Page 17

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Special Considerations and Recommended Practices for [[Mutual Funds]] 17 
The Role of Agents in Cost Basis Reporting 
Both Networking and ACATS accommodate for the use of an agent to facilitate processing on behalf of an 
originating or introducing party15. 
• In Networking, the Agent for Firm field is a field defined by the Clearing Firm to represent the originating or 
introducing firm. The values found in this field are not assigned by [[NSCC]]. 
• In ACATS, the identification of an MF Agent is less straightforward, due to the translation for certain 
business relationships when converting the ACATS transfer record into an ACATS -Fund/SERV 018 
record. The MF Agent is represented as the firm on the order, not the underlying or introducing firm.  
 
Regardless of how the agent relationship is designated, IRS regulations clarify that an agent for trading 
purposes does not have like-responsibilities for moving cost basis information between reporting brokers. In 
other words, the cost basis transfer should move outside the agent, when possible, when passing between 
reporting brokers. 
Within Networking, there are no [[NSCC]]-defined fields to specifically identify an agent (e.g. [[NSCC]] Firm 
Number). Therefore, with a Networking transfer (B52), the Clearing Firm number on the record will be used to 
identify the firm entity that should receive or send the cost basis information on a transfer statement. It ignores 
the Agent for Firm reference entirely because the Agent for Firm field value, by definition, represents an 
undefined value for identifying the originating or introducing firm in the context of Cost Basis transfers.
16 This 
approach will cause the transfer statement to be directed by the Clearing Firm to the introducing firm.  
With ACATS, the fields “Originating Delivering Firm Number” and “Originating Receiving Firm Number” (which 
correspond to the existing ACATS PTF/TI fields of the same name)—when populated—should be used to 
identify the contra-parties when generating transfer statements. Otherwise, the transfer statement should be 
directed to the “Firm Number” on the ACATS or ACATS-Fund/SERV transaction. 
 
15 An Agent in this context is defined as a third- party who serves as a trading conduit for an introducing firm. For instance, Firm A utilizes Agent B to receive its 
mutual fund orders and to transmit them through [[NSCC]] to Fund Company C for processing. Fund Company C’s responses are transmitted back through [[NSCC]], 
received by Agent B and then delivered by Agent B to Firm A.  
16 In some instances, Clearing Firms may pass a value in the Agent for Firm field that is equivalent to an [[NSCC]] client number. This is not universal nor is it a 
required use of the field. 

---

## Page 18

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 18 
ANNOTATED CBRS RECORD LAYOUTS AND 
RECOMMENDED PRACTICES FOR [[Mutual Funds]] 
Introduction 
The Cost Basis Reporting Service (CBRS) is a [[DTCC]] 17 product used to facilitate the exchange of tax lot 
information when [[investor]] assets are transferred between tax reporting brokers. Originally developed as a 
companion product to [[DTCC]]’s ACATS (Automated Customer Account Transfer Service), 18 CBRS has been 
expanded to support the passage of cost basis on other transfer types; for example, ACATS-Fund/SERV, 
Networking,19 and with manual transfers. Like other [[DTCC]] services, and to the benefit of the industry and 
investors, CBRS provides an automated, efficient and cost-effective process for transferring cost basis 
information. 
CBRS clients access the service in one of two methods: through automated file transmissions, or through 
MyDTCC web portal20 product. Please refer to the [[DTCC]] Learning site at https://dtcclearning.com/products-
and-services/equities-clearing/cost-basis-reporting-service-cbrs.html for in-depth information on CBRS, 
including a comprehensive User Guide, details on how to sign up for the service, and other important 
information about its use in either a file-based or web-based manner. 
Industry Recommended Practice:  
All Mutual Fund reporting brokers should adopt CBRS as the sole means of moving Cost Basis information between 
reporting brokers. 
General CBRS Considerations 
Because CBRS supports passing cost basis for many types of [[Asset]] transfers, the ICI BDAC Cost Basis 
Reporting Task Force (the Task Force) developed an annotated CBRS [[Asset]] record and a Tax Lot record 
which includes specific details for [[Mutual Funds]]. Each field that is pertinent to [[Mutual Funds]] is noted, along with 
instructions on how each field should be used. 
Please note that the [[DTCC]] CBRS User Guide serves as the primary document governing the use of 
CBRS and must be consulted for additional details regarding the [[BASIC]] use of the CBRS system.  
The following information supplements the [[DTCC]] CBRS User Guide and is designed to assist the mutual fund 
user community in the implementation of CBRS. The information is presented primarily from the perspective of 
a reporting [[Broker]] submitting an “original” or “corrected” [[Asset]] and tax lot record. “Reject” and “request” actions 
use a sub-set of this information when compared to “original” and “corrected” submissions; the differences are 
outlined in the [[DTCC]] CBRS User Guide. 
Listed below is explanatory information about certain fields and their general usage in the context of Mutual 
Funds: 
• Submitting Firm Number will always refer to the firm submitting the CBRS record. Stated differently, the 
party creating the CBRS file to deliver a record is the Submitting Firm. 
 
17 [[DTCC]] operates its businesses through several operating subsidiaries.  
18 ACATS is a National [[securities]] Clearing Corporation (“[[NSCC]]”) service. [[NSCC]] is a wholly owned subsidiary of [[DTCC]].  
19 ACATS-Fund/SERV is an [[NSCC]] service supporting the transfer of [[investor]] accounts.  Networking is an [[NSCC]] service that supports the transfer of account 
information such as account share balances. 
20 MyDTCC web portal is a secure, web-enabled portal offered by [[DTCC]], on behalf of its subsidiaries, which allows organizations that may not be able to support 
automated file transmissions to benefit from a file-based upload or download of CBRS information. 

---

## Page 19

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 19 
• Contra Firm Number will always refer to the firm receiving the CBRS record. Stated differently, the party 
receiving a CBRS record is the Contra Firm. 
• Record Content Indicator defines the type of information represented by the record. Both 01 = Original 
and 02 = Corrected are created and provided by the reporting [[Broker]] managing the “transfer-out” side of 
the transaction (“[[Asset]] Deliverer”) and will represent the actual Cost Basis information ([[Asset]] and Tax 
Lot(s) Records) corresponding to the transaction. 
 
The 03 = Firm Reject and 04 = Request records are created and provided by the reporting [[Broker]] 
managing the “transfer-in” side of the transaction (“[[Asset]] Receiver”) and are only sent when records are 
not received from the [[Asset]] Deliverer (in the case of 04 = Request) or are in some way unusable (in the 
case of 03 = Firm Reject) . 
 
As implied above, the [[Asset]] Deliverer (the party delivering the Cost Basis information through CBRS) and 
the [[Asset]] Receiver (the party receiving the Cost Basis information through CBRS) change roles 
depending on the Record Content Indicator value. As a result, the Submitting Firm Number and 
Contra Firm Number on the CBRS record also vary by Record Content Indicator: 
 
Record Content Indicator CBRS Submitting Firm Number CBRS Contra Firm Number 
Original (01) and Corrected (02) [[Asset]] Deliverer [[Asset]] Receiver 
Firm Reject (03) and Request (04) [[Asset]] Receiver [[Asset]] Deliverer 
 
Example: 
Colossal Mutual Fund Company, [[NSCC]] Client Number 8819 and CBRS user, transfers 1,250.500 [[shares]] to Ginormous 
[[Broker]]/Dealer, [[NSCC]] Client Number 2277 and CBRS user. The following matrix explains each party’s CBRS role, in the 
context of CBRS Record Content Indicator. 
Record Content Indicator CBRS Submitting Firm Number CBRS Contra Firm Number 
01 = Original 
(Colossal sends Original Cost Basis 
Information to Ginormous) 
8819 2277 
02 = Corrected 
(Colossal corrects the Cost Basis 
Information previously sent to 
Ginormous) 
8819 2277 
03 = Firm Reject 
(Ginormous rejects the Cost Basis 
Information sent by Colossal) 
2277 8819 
04 = Request 
(Ginormous requests Cost Basis 
Information from Colossal, in support 
of the completed transfer) 
2277 8819 
 

---

## Page 20

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 20 
• Transfer Control Number and Alternate Control Number, in the context of Transaction Type of 57 = 
Manual Mutual Fund Transfer, are noted to be populated with a mutually-agreeable identifier between 
the contra-parties. However, often these transactions are sent by the Fund through the [[NSCC]] Networking 
Activity File. Contra-parties should populate the CBRS record with the Control Number used on Record 4, 
position 23-37 of the Networking F55 record, and using it for matching purposes.  
 
Industry Recommended Practice: 
A Manual Mutual Fund Transfer completed in response to a failed ACATS-Fund/SERV PTF (Firm to Fund or Fund to Firm 
transfer) or Networking transaction should reference the respective Transfer Control Number and Alternate Control 
Number provided by the [[Broker]]/dealer in any manual instructions received to rectify the failed transaction. Depending on 
the firm and its system needs, this number may be the ACATS-Fund/SERV or Networking control number of the failed 
transaction or some other value. This will facilitate matching between the contra-parties. 
The [[NSCC]] Vendor Advisory Group, a consortium comprised of [[DTCC]], mutual fund service providers and fund 
families with proprietary mutual fund recordkeeping systems, has worked with representatives of major 
brokerage system platforms and proprietary brokerage system owners to develop a standard algorithm to 
generate Manual Transfer Control Numbers. A Manual Transfer Control Number will be used by the Fund on 
any manual transfer where no other Transfer Control Number has been designated for use. Through use in 
this manner, transaction activity and subsequent CBRS information can be easily linked together to fulfill 
transfer statement reporting [[obligations]]. 
Industry Recommended Practice:  
In the absence of instructions to the contrary, all manual transfers processed by the Fund should reference a Manual 
Transfer Control Number derived using the following algorithm: 
Position 1: ‘D’ = Direct Transfer Indicator 
Position 2-5: [[NSCC]] Client Number for the Fund 
Position 6: Last Digit of Current Year 
Position 7-9: Julian Date 
Position 10-15: Unique Number (randomly generated, sequential) 
This number should be provided as the Original Control Number on Record 4, Position 23-37 of the Networking F55 record, 
plus as the Transfer Control Number for all related CBRS records. 
• Contra Firm Number and Contra Firm Type must be confirmed by the CBRS User Master File 
(Autoroute Product [[ID]] 0256166)—updated and distributed daily by [[DTCC]]. This is necessary because 
[[DTCC]] requires confirmation of the Client Number AND Firm Type on all CBRS records. [[DTCC]] has 
overlapping assignments of client numbers across services of [[DTCC]] subsidiaries. Therefore, [[DTCC]] uses 
both the Firm Number and Firm Type to confirm routing of CBRS information between contra- parties. 
Likewise, there are CBRS-only clients that may need to submit or receive CBRS records; their 
identification numbers are only available through the CBRS User Master File and are not found on any 
corresponding ACATS-Fund/SERV or Networking transaction. Finally, because CBRS is an optional 
service, a [[DTCC]] client in another product (like ACATS-Fund/SERV or Networking) may not participate in 
CBRS, so verification before transmission is quite important. 
 
The recommended practice is to use the respective Client Numbers from the corresponding transaction, 
enriched by the CBRS User Master File guidelines that follow in this chapter, to search for a match on the 
CBRS User Master File. Additional validation against the CBRS User Master File Firm Name field would 
be a second check, when a match is found. Using this methodology may not result in a match– that may 
indicate the firm or fund does not participate in CBRS, or they are a CBRS-only client and are instead 
identified by the CBRS User Account Number field. 
 

---

## Page 21

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 21 
• Total Position Quantity on the [[Asset]] Record is edited by [[DTCC]] against the cumulative [[shares]] on the tax 
lot records, and the quantity can be provided with up to 4 places to the right of the decimal. Any fractional 
share amount up to 4 positions to the right of the decimal are accepted. For example, a transfer of 3.547 
[[shares]] can be provided as ‘3,5470’ or ‘3,547’ [[shares]], and a transfer of 100.100 [[shares]] could be provided 
as ‘100,1’ [[shares]]. (CBRS uses a comma ‘,’ instead of a decimal ‘.’ when reporting data in the Total 
Position Quantity field). 
 
Submitting a Total Position Quantity (including the 4 positions to the right of the decimal) that does not 
equal exactly the sum of the tax lot records will cause the record to be rejected back to the submitter.  
CBRS User Master File Considerations 
The CBRS User Master File, listing all eligible CBRS clients, will be updated and provided to CBRS clients, 
and/or their agents, on a daily basis. The file contains data which will help the user cross- reference information 
to correctly populate the CBRS Contra Firm Number and Contra Firm Type. 
Each CBRS Client is assigned a CBRS User Account Number. If the user is registered with [[DTCC]] for any 
service in addition to CBRS, the CBRS User Account Number will be cross-referenced to a Firm Account 
Number, Firm Account Type, and Firm Name. 
The following guidelines can be helpful in understanding the CBRS User Master File:  
1. For mutual fund purposes, if found on the CBRS User Master File the Firm Account Number  and a valid 
Firm Account Type should be the first choice to use when populating CBRS records. 
Example: 
Client uses CBRS and other [[DTCC]] services. CBRS User Master File contains: 
CBRS User Account Number: 12345678 
Firm Account Number: 8819 
Firm Account Type: NSCPRT 
Firm Name: Colossal Mutual Fund Company 
Any CBRS records for Colossal Mutual Fund Company should reference ‘8819’ as the Firm Number, and ‘NSCPRT’ as the 
Firm Type. The CBRS User Account Number is ignored in this situation since Colossal uses other [[DTCC]] services. 
2. If a CBRS User Master File record entry does not include a Firm Account Number, any CBRS records 
referencing the related client will require use of the CBRS User Account Number as the Contra Firm 
Number, and CBRACT as the Firm Type (in the corresponding field) on any CBRS records. 
Example: 
CBRS is the only [[DTCC]] service used by the Client. CBRS User Master File contains: 
CBRS User Account Number: 12345678 
Firm Account Number:  
Firm Account Type: CBRACT 
Firm Name: Colossal Mutual Fund Company 
Any CBRS records for Colossal Mutual Fund Company should reference ‘12345678’ as the Firm Number, and ‘CBRACT’ 
as the Firm Type. The CBRS User Account Number is used because the Firm Account Number is blank on the master 
file. 
3. [[Broker]]/Dealers that are both [[DTC]] clients and [[NSCC]] Members are always Firm Type DTCPRT. This 
value can be used, along with the [[DTCC]] Client Number on ACATS-Fund/SERV and Networking records, 
in the primary search of the CBRS User Master File to confirm the [[Broker]]/Dealer is a CBRS client . 

---

## Page 22

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 22 
4. Mutual fund families that are [[NSCC]] Members are always Firm Type NSCPRT. This value can be used, 
along with the [[DTCC]] Client Number on ACATS-Fund/SERV and Networking records, in the primary 
search of the CBRS User Master File to confirm the Mutual Fund is a CBRS client . 
5. Trust [[Companies]] can be either Firm Type DTCPRT or NSCPRT (it depends on whether they are [[DTC]] 
clients or [[NSCC]] Members). These values can be used, along with the [[DTCC]] Client Number on ACATS-
Fund/SERV and Networking records, in the primary search of the CBRS User Master File to confirm the 
Trust Company is a CBRS client. 
6. Firm Type AGTNBR is not relevant to [[Mutual Funds]]. 
7. CBRS record creation/delivery through CBRS should not be attempted if: 
a. The current date is prior to the CBRS Account Start Date for the CBRS client on the CBRS User 
Master File. 
b. The client cannot be located on the CBRS User Master File. 
Example: 
CBRS User Master File contains: 
CBRS User Account Number: 12345678 
Firm Account Number: 8819 
Firm Account Type: AGTNBR 
Firm Name: ABC [[Stock]] [[transfer agent]] 
In this case, if Colossal Mutual Fund Company was a contra-party to a CBRS transfer, a search of the CBRS User Master 
File on their [[DTCC]] Client Number of ‘8819’ would find this record. However, because this Firm Account Type is ‘AGTNBR’, 
it does not pertain to Colossal Mutual Fund Company. If this was the only record found under ‘8819’, the user can safely 
assume that Colossal Mutual Fund Company does not participate in CBRS, and the tax lot transfer must be completed 
through other means. 
CBRS [[Asset]] Records 
The following elaborates on the mutual fund usage and perspective on key fields comprising the CBRS [[Asset]] 
Records. Please note that record layouts are subject to change. Please visit the CBRS Record Layouts under 
CBRS Documents in the Equities/Cost Basis Reporting Service of the [[DTCC]] Learning Center  at 
https://dtcclearning.com/products-and-services/equities-clearing/cbrs/cbrs-technical-resources.html for most 
recent version of the layouts. In no way should this information be viewed as standalone. Instead it is 
supplemental to [[DTCC]]’s CBRS User Guide governing the overall usage of CBRS by the financial ser vices 
industry.  
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
FIELD NAME COMMENTS AND GUIDANCE FOR FIELD USAGE 
Record Content Indicator Record Content Indicator defines the type of information represented by this [[Asset]] 
Record. 
Regarding 01 = Original [[Asset]] Record. 
This record is sent by the Delivering Firm, or the reporting [[Broker]] that delivers [[shares]] 
as a result of the transfer. 
Regarding 02 = Corrected [[Asset]] Record. 
 
21 Please refer to [[DTCC]]’s CBRS User Guide for more detail on [[Asset]] Record, Required/Optional Field Designations and Usage.  

---

## Page 23

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 23 
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
This record is sent by the Delivering Firm, or the reporting [[Broker]] that delivers [[shares]] 
as a result of the transfer. 
When one tax lot is corrected, it is assumed the entire CBRS response requires 
correction. For example: 
Transfer 1,000.000 [[shares]] in three tax lots, as follows: 
Tax Lot 1 = 500.000 [[shares]] 
Tax Lot 2 = 250.000 [[shares]] 
Tax Lot 3 = 250.000 [[shares]] 
If details on Tax Lot 3 need to be corrected/resent, all three tax lot records should be 
included. Tax Lots 1 and 2 should also be resent, to maintain the integrity of the 
relationship between tax lots and transferred [[shares]]. 
NOTE: 
At least one (1) corresponding tax lot record must be indicated as Corrected. 
Regarding 03 = Firm Reject Record and 04 = Request Record. 
These records are sent by the Receiving Firm, or the reporting [[Broker]] that receives 
[[shares]] as a result of the transfer. 
Records are sent only when necessary and to maintain compliance with regulations. 
NOTE: 
The recommended practice is to not submit a Record Content Indicator 03 = Firm 
Reject Record in response to a 04 = Request Record received, even if it is not 
applicable to the receiving reporting [[Broker]]. 
Transaction Type Transaction Type identifies the actual [[DTCC]]-based or manual transaction that 
created the need to transfer cost basis through CBRS. 
The only applicable Transaction Types for [[Mutual Funds]] are as follows: 
46 = Fund to Firm Mutual Fund Transfer (ACATS PTF) 
51 = Firm to Fund Mutual Fund Transfer (ACATS PTF) 
56 = Networking Transaction 
57 = Manual Mutual Fund Transfer 
Transfer Control Number The Transfer Control Number corresponds to the unique identifier assigned to the 
corresponding transaction, either through use of a [[DTCC]] product (e.g., ACATS 
(ACATS-Fund/SERV) or Networking) or manually. The number is used by the 
recipient to link CBRS information to its corresponding transaction. 
If Transaction Type is 46 = Fund to Firm Mutual Fund Transfer or 51 = Firm to 
Fund Mutual Fund Transfer; this field is the Fund/SERV
® Control Number–Position 
45-59 (Variable) or Record 1, Position 41-55 (Fixed) on the Fund/SERV® 018 record. 
ACATS users can find this number in Position 153-163 (Variable) or Record 3, 
Position 8-18 (Fixed) of the ACATS Output Fund/SERV® Statistics file (SIAC720–
variable; SIAC726–fixed). 
Firms using the Fund/SERV Control Number from the ACATS-Fund/SERV Statistics 
file should add the letters “CATS” to the front of it, in order to match the number that 
Funds provide in this field. 
If transaction type is 56 = Networking Transaction, then the control number is the 
Networking Control Number, found in Record 1, Position 14-24 of the Networking 
Conversion/Acknowledgement B52/F53 record. 

---

## Page 24

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 24 
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
For all other transaction types, 57 = Manual Mutual Fund Transfer; this field is the 
control number agreed upon by the contra-parties involved in the original [[securities]] 
transaction. The Control Number is the same as what is provided on the Networking 
F55 Activity Record, Record 4, Position 23-37. 
In all instances, data should be left-justified and blank-filled in this alpha-numeric field 
on the CBRS file. 
Alternate Control Number The Alternate Control Number, when available, corresponds to an additional unique 
identifier assigned to a corresponding transaction, either through use of a [[DTCC]] 
product or manually. This field comes into play when data is being passed between 
two different [[DTCC]] products, such as ACATS and ACATS-Fund/SERV. 
If Transaction Type 46 = Fund to Firm Mutual Fund Transfer and 51 = Firm to 
Fund Mutual Fund Transfer, the ACATS Control Number must be provided in this 
Field, found in Position 683-702 (Variable) or Record 8, Position 28-47 (Fixed) of the 
Fund/SERV® 018 record. It is also found in Position 12-15 (Variable) or Record 1, 
Position 8-21 (Fixed) of the ACATS Transfer Input record (Autoroute 36667–variable; 
32667–fixed). If not provided, the record will reject. 
Data should be left-justified and blank-filled in this alpha-numeric field on the CBRS 
file. 
Contra Firm Number 
NOTE: 
This section applies to Record 
Content Indicator 01 (Original) 
and Record Content Indicator 
02 (Corrected) 
The Contra Firm Number corresponds to either the Firm Account Number, or, if 
not available, the CBRS User Account Number associated with the entity receiving 
this CBRS [[Asset]] Record. 
This number should always be obtained through validation against the CBRS User 
Master File, updated and distributed daily by [[DTCC]]. 
The Contra Firm Number is populated based on relationship to the CBRS record 
itself, and not the corresponding transaction record. Therefore, the entity receiving the 
CBRS record is always considered the receiving firm. 
The following fields can come into play in validating against the CBRS User Master 
File as to what the Contra Firm Number on the CBRS record should be. In all 
instances, data is passed with lead zeros and right-justified: 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 
The firm is the recipient of this record. 
If populated, Originating Receiver Firm Number–Position 745-748 (Variable) or 
Record 8, Position 90-93 (Fixed) on the Fund/SERV® 018 record–it means an MF 
Agent is in use. This can be used to assist with validation against the CBRS User 
Master File. 
ELSE 
Firm Number–Position 12-15 (Variable) or Record 1, Position 8-11 (Fixed) on the 
Fund/SERV
® 018 record can be used to assist with validation against the CBRS User 
Master File. 
Original Deliverer Number–Positions 49-52 (Variable) or Record 1, Position 45-48 
(Fixed) on the ACATS record can be used to assist with validation against the CBRS 
User Master File. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
The fund is the recipient of this record. 
Fund Number–Position 24-27 (Variable) or Record 1, Position 20-23 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User 
Master File. 
Original Receiver Number–Position 41-44 (Variable) or Record 1, Position 37-40 
(fixed) on the ACATS record can be used to assist with validation against the CBRS 
User Master File. 

---

## Page 25

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 25 
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3, or Trust-Networked Level 0 account assets in a 
Network Level 4 or non-networked account, the fund is the recipient of the CBRS 
record. If provided, the Clearing/Settling Fund Number–Position 10-13 on the 
Networking B52/F53 record can be used to assist with validation against the CBRS 
User Master File. 
If B52 places Network Level 4 or non-networked account assets in a Network Level 3 
or Trust-Networked Level 0 account, the firm is the recipient of the CBRS record. The 
Clearing/Settling Firm Number–Position 6-9 on the Networking B52/F53 record can 
be used to assist with validation against the CBRS User Master File. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account assets are transferred into a 
Network Level 4, or non-networked account, the fund is the recipient of the CBRS 
record. 
If Network Level 4 or non-networked account assets are transferred into a Network 
Level 3 or Trust-Networked Level 0 account, the firm is the recipient of the CBRS 
record. 
Information on the Manual Transfer instruction will need to be consulted against the 
CBRS User Master File to identify the appropriate reference. 
Contra Firm Number 
NOTE: 
This section applies to Record 
Content Indicator 03 (Firm 
Reject) and Record Content 
Indicator 04 (Request) 
The Contra Firm Number corresponds to either the Firm Account Number, or, if 
not available, the CBRS User Account Number associated with the entity receiving 
this CBRS [[Asset]] Record. 
This number should always be obtained through validation against the CBRS User 
Master File, updated and distributed daily by [[DTCC]]. 
The Contra Firm Number is populated based on the relationship to the CBRS record 
itself, and not the corresponding transaction record. Therefore, the entity receiving the 
CBRS record is always considered the receiving firm. 
The following fields can come into play in validating against the CBRS User Master 
File as to what the Contra Firm Number on the CBRS record should be. In all 
instances, data is passed with lead zeros and right-justified: 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 
The fund is the recipient of this record. 
Fund Number–Position 24-27 (Variable) or Record 1, Position 20-23 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User 
Master File. 
Original Receiver Number–Position 41-44 (Variable) or Record 1, Position 37-40 
(fixed) on the ACATS record can be used to assist with validation against the CBRS 
User Master File. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
The firm is the recipient of this record. 
If populated, Originating Receiver Firm Number–Position 745-748 (Variable) or 
Record 8, Position 90-93 (Fixed) on the Fund/SERV® 018 record–it means an MF 

---

## Page 26

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 26 
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
Agent is in use. This can be used to assist with validation against the CBRS User 
Master File. 
ELSE 
Firm Number–Position 12-15 (Variable) or Record 1, Position 8-11 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User 
Master File. 
Original Deliverer Number–Positions 49-52 (Variable) or Record 1, Position 45-48 
(Fixed) on the ACATS record can be used to assist with validation against the CBRS 
User Master File. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 or Trust-Networked Level 0 account assets in a 
Network Level 4 or non-networked account, the firm is the recipient of the CBRS 
record. The Clearing/Settling Firm Number–Position 6-9 on the Networking B52/F53 
record can be used to assist with validation against the CBRS User Master File. 
If B52 places Network Level 4 or non-networked account assets in a Network Level 3 
or Trust-Networked Level 0 account, the fund is the recipient of the CBRS record. If 
provided, the Clearing/Settling Fund Number–Position 10-13 on the Networking 
B52/F53 record can be used to assist with validation against the CBRS User Master 
File. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account assets are transferred into a 
Network Level 4 or non-networked account, the firm is the recipient of the CBRS 
record. 
If Network Level 4 or non-networked account assets are transferred into a Network 
Level 3 or Trust-Networked Level 0 account, the fund is the recipient of the CBRS 
record. 
Information on the Manual Transfer instruction will need to be consulted against the 
CBRS User Master File to identify the appropriate reference. 
Contra Firm Type Receiving Firm Type clarifies the type of entity receiving the CBRS record. This is 
important because the same client number can be assigned by [[DTCC]] to different 
firms across services of [[DTCC]] subsidiaries. This type corresponds to the type of 
number in the Contra Firm Number field and is obtained from the CBRS User 
Master File. 
Values: 
AGTNBR = [[transfer agent]] (not relevant to [[Mutual Funds]]) 
CBRACT = CBRS-Only User 
DTCPRT = [[DTC]] Client 
NSCPRT = [[NSCC]] Client 
Submitting Firm Number 
NOTE: 
This section applies to Record 
Content Indicator 01 (Original) 
and Record Content Indicator 
02 (Corrected) 
The Submitting Firm Number corresponds to the Firm Account Number, or, if not 
available, the CBRS User Account Number associated with the entity submitting this 
CBRS [[Asset]] Record. 
This number should always be obtained through validation against the CBRS User 
Master File, updated and distributed daily by [[DTCC]]. 
The Submitting Firm Number is populated based on relationship to the CBRS 
record itself, and not the corresponding transaction record. Therefore, the entity 
submitting the CBRS record is the submitting firm. 
The following fields can come into play in validating against the CBRS User Master 
File as to what the Submitting Firm Number on the CBRS record should be. In all 
instances, data is passed with lead zeros and right-justified: 

---

## Page 27

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 27 
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 
The fund is the submitter of this record. 
Fund Number–Position 24-27 (Variable) or Record 1, Position 20-23 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User 
Master File. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
The firm is the submitter of this record. 
If populated, Originating Receiver Firm Number–Position 745-748 (Variable) or 
Record 8, Position 90-93 (Fixed) on the Fund/SERV® 018 record–it means an MF 
Agent is in use. This can be used to assist with validation against the CBRS User 
Master File. 
ELSE 
Firm Number–Position 12-15 (Variable) or Record 1, Position 8-11 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User 
Master File. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 or Trust-Networked Level 0 account assets in a 
Network Level 4 or non-networked account, the firm is the submitter of the CBRS 
record. The Clearing/Settling Firm Number–Position 6-9 on the Networking B52/F53 
record can be used to assist with validation against the CBRS User Master File. 
If B52 places Network Level 4 or non-networked account assets in a Network Level 3 
or Trust-Networked Level 0 account, the fund is the submitter of the CBRS record. If 
provided, the Clearing/Settling Fund Number–Position 10-13 on the Networking 
B52/F53 record can be used to assist with validation against the CBRS User Master 
File. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account [[Asset]] is transferred into a 
Network Level 4, or non-networked account, the firm is the submitter of the CBRS 
record. 
If Network Level 4 or non-networked account [[Asset]] is transferred into a Network Level 
3 or Trust-Networked Level 0 account, the fund is the submitter of the CBRS record. 
Information on the Manual Transfer instruction will need to be consulted against the 
CBRS User Master File to identify the appropriate reference. 
Submitting Firm Number 
NOTE: 
This section applies to Record 
Content Indicator 03 (Firm 
Reject) and Record Content 
Indicator 04 (Request) 
The Submitting Firm Number corresponds to the Firm Account Number, or, if not 
available, the CBRS User Account Number associated with the entity submitting this 
CBRS [[Asset]] Record. 
This number should always be obtained through validation against the CBRS User 
Master File, updated and distributed daily by [[DTCC]]. 
The Submitting Firm Number is populated based on relationship to the CBRS 
record itself, and not the corresponding transaction record. Therefore, the entity 
submitting the CBRS record is the submitting firm. 
The following fields can come into play in validating against the CBRS User Master 
File as to what the Submitting Firm Number on the CBRS record should be. In all 
instances, data is passed with lead zeros and right-justified: 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 
The firm is the submitter of this record. 
If populated, Originating Receiver Firm Number–Position 745-748 (Variable) or 
Record 8, Position 90-93 (Fixed) on the Fund/SERV® 018 record–means an MF 

---

## Page 28

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 28 
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
Agent is in use. This can be used to assist with validation against the CBRS User 
Master File. 
ELSE 
Firm Number–Position 12-15 (Variable) or Record 1, Position 8-11 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User 
Master File. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
The fund is the submitter of this record. 
Fund Number–Position 24-27 (Variable) or Record 1, Position 20-23 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User 
Master File. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 or Trust-Networked Level 0 account assets in a 
Network Level 4 or non-networked account, the fund is the submitter of the CBRS 
record. If provided, the Clearing/Settling Fund Number–Position 10-13 on the 
Networking B52/F53 record can be used to assist with validation against the CBRS 
User Master File. 
If B52 places Network Level 4 or non-networked account assets in a Network Level 3 
or Trust-Networked Level 0 account, the firm is the submitter of the CBRS record. 
The Clearing/Settling Firm Number–Position 6-9 on the Networking B52/F53 record 
can be used to assist with validation against the CBRS User Master File. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account [[Asset]] is transferred into a 
Network Level 4, or non-networked account, the fund is the submitter of the CBRS 
record. 
If Network Level 4 or non-networked account [[Asset]] is transferred into a Network Level 
3 or Trust-Networked Level 0 account, the firm is the submitter of the CBRS record. 
Information on the Manual Transfer instruction will need to be consulted against the 
CBRS User Master File to identify the appropriate reference. 
Submitting Firm Type 
 
Submitting Firm Type clarifies the type of entity sending the CBRS record. This is 
important because the same client number can be assigned by [[DTCC]] to different 
firms across services of [[DTCC]] subsidiaries. This type corresponds to the type of 
number in the Submitting Firm Number field. 
Values: 
AGTNBR = [[transfer agent]] (not relevant to [[Mutual Funds]]) 
CBRACT = CBRS User 
DTCPRT = [[DTC]] Client 
NSCPRT = [[NSCC]] Client 
Receiver Customer Account 
Number 
The Receiver Customer Account Number identifies the customer’s account to 
which the CBRS data will be applied. This account number may differ from the BIN 
([[Broker]] Identification Number) and may represent an underlying sub-account 
available to the firm in question. 
The Receiver Customer Account Number is ALWAYS populated based on 
relationship to the corresponding transaction record; it ALWAYS references the 
account that should receive the cost basis information and is not impacted by the 
value of the Record Content Indicator. 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 

---

## Page 29

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 29 
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
If populated, Originating Receiver Customer Account Number at Firm–Position 547-
566 
(Variable) or Record 6, Position 78-97 (Fixed) on the Fund/SERV® 018 record–means 
an MF Agent is in use, and this field should be used. 
ELSE 
Customer Account Number at Firm–Position 572-591 (Variable) or Record 7, Position 
10-29 (Fixed) of the Fund/SERV® 018 record. 
Original Receiver Customer Account Number–Position 53-72 (Variable) or Record 1, 
Position 49-68 (Fixed) of the ACATS record. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
Customer Account Number at Fund–Position 140-159 (Variable) or Record 2, 
Position 43-62 (Fixed) of the Fund/SERV® 018 record. 
OR 
Original Receiver Customer Account Number–Position 53-72 (Variable) or Record 1, 
Position 49-68 (Fixed) of the ACATS Transfer record. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 or Trust-Networked Level 0 account assets in a 
Network 4 or non-networked account, use the Credit Account Number–Record 1, 
Position 57-76 of the Networking B52/F53 record, which should reference the Fund’s 
Account Number. 
If B52 places Network Level 4, or non-networked account assets in a Network Level 
3, or Trust-Networked Level 0 account, first use the Credit Sub-Account Number–
Record 4, Position 46-65 of the Networking B52/F53 record. If the Credit Sub-Account 
Number is blank, use the Credit Account Number–Record 1, Position 57-76 of the 
Networking B52/F53 record, which should reference the Firm’s Account Number. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account assets are transferred into 
Network Level 4, or non-networked account, this field should carry either the 
Underlying Customer Account Number or the Fund’s Account Number. 
If Network Level 4 or non-networked account assets are transferred into a Network 
Level 3 or Trust-Networked Level 0 account, this field should carry either the 
Underlying Customer Account Number or the Firm’s Account Number. 
Deliverer Customer Account 
Number 
The Deliverer Customer Account Number identifies the customer’s account from 
which the CBRS data will be sent. This account number may differ from the BIN 
([[Broker]] Identification Number) and may represent an underlying sub-account 
available to the firm in question. 
The Deliverer Customer Account Number is ALWAYS populated based on 
relationship to the corresponding transaction record; it ALWAYS references the 
account from which cost basis information is sent and is not impacted by the value of 
the Record Content Indicator. 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 
Customer Account Number at Fund–Position 596-615 (Variable) or Record 7, 
Position 54-73 (Fixed) of the Fund/SERV® 018 record. 
OR 
Original Deliverer Customer Account Number–Position 173-192 (Variable) or Record 
3, Position 38-57 (Fixed) of the ACATS Transfer record. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 

---

## Page 30

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 30 
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
If populated, Original Deliverer Customer Account Number–Position 177-196 
(Variable) or Record 2, Position 80-99 (Fixed) of the Fund/SERV 018 
ELSE 
Customer Account Number at Firm–Position 572-591 (Variable) or Record 7, Position 
10-29 (Fixed) of the Fund/SERV® 018 record. 
Original Deliverer Customer Account Number–Position 173-192 (Variable) or Record 
3, Position 38-57 (Fixed) of the ACATS Transfer record. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 and Trust-Networked Level 0 account assets in a 
Network 4 or non-networked account, first use the Debit Sub-Account Number–
Record 4, Position 66-85 of the Networking B52/F53 record. If the Debit Sub-Account 
Number is blank, use the Account Number–Record 1, Position 36-55 of the 
Networking B52/F53 record, which should reference the Firm’s Account Number. 
If B52 places Network Level 4, or non-networked account assets in a Network Level 
3, or Trust-Networked Level 0 account, use the Account Number–Record 1, Position 
36-55 of the Networking B52/F53 record, which should reference the Fund’s Account 
Number for the transaction. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account assets are transferred into a 
Network Level 4, or non-networked account, this field should carry either the 
Underlying Customer Account Number or the Firm’s Account Number. 
If Network Level 4 or non-networked account assets are transferred into a Network 
Level 3, or Trust-Networked Level 0 account, this field should carry either the 
Underlying Customer Account Number or the Fund’s Account Number. 
ISIN Country Code Value is US 
ISIN Security Issue [[ID]] ([[CUSIP]]) Security Issue [[ID]] of the Security in question 
ISIN Security Check Digit Leave Blank. 
[[Asset]] Description This field should be populated with the same Security Issue [[ID]] Fund Name found on 
Mutual Fund Profile, if a client. Otherwise, field should be populated in a way to 
clearly identify the Security Issue [[ID]]. 
[[Asset]] Category Value is always MFNM 
Total Position Quantity Total [[shares]] involved in the transfer should be provided. 
NOTE: 
In the context of Transaction Types 46 = Fund to Firm Mutual Fund Transfer, 51 = 
Firm to Fund Mutual Fund Transfer, and 56 = Networking Transfer, this amount 
typically should match the corresponding ACATS- Fund/SERV® or Networking B52 
transaction amount. 
It is feasible that the Total Position Quantity can exceed the transaction amount, in 
the instance of an accrued [[Dividend]] reinvestment/payout on an all-share transfer. 
Some systems may retain this amount for distribution at the end of the period; others 
may incorporate into the transferred [[shares]] sent with the transaction. 
Date Transfer was Initiated Leave Blank 

---

## Page 31

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 31 
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
NOTE: 
The record layouts state that either Transfer initiation or [[settlement]] Date must be 
populated. Because [[settlement]] Date is more relevant to the contra-parties in a 
Mutual Fund Transfer, it is used. 
[[settlement]] Date of Transfer Populate with the [[settlement]] Date of the Transfer. Format: CCYYMMDD. 
NOTE: 
The record layouts state either Transfer initiation or [[settlement]] Date must be 
populated. Because [[settlement]] Date is more relevant to the contra-parties in a 
Mutual Fund Transfer, it is used. 
NOTE: 
In the context of [[Mutual Funds]], transfers typically have the same initiation and 
[[settlement]] dates, from a fund’s books and records perspective. [[Broker]]/Dealers may 
recognize a different [[settlement]] Date than the Fund, because of the bookkeeping 
and [[settlement]] differences between ACATS and ACATS-Fund/SERV. 
Therefore, in the context of matching tax lots to a transaction, [[settlement]] Date should 
not be a primary matching field. 
Position Code Value is always ‘L’ 
Disposition Method Used Pass this information if the Disposition Method currently used by the shareholder is 
applicable to the transferred lots and matches one of the values supported by [[DTCC]]’s 
CBRS layout, or if the shareholder has specifically elected one of the methods 
supported by [[DTCC]]. Otherwise, leave Blank. 
[[shares]] to Cover Short Indicator Value is always ‘N’ 
Firm Reject Reason Code Use only if Record Content Indicator is 03 = Firm reject record. Otherwise, leave. 
Blank. 
In the Mutual Fund Context, Reject Reason Codes should be used as follows: 
01 = Receiver cannot apply received cost basis record 
Used when the underlying account position cannot be located or when related fields 
are not correctly populated on the record received. 
02 = CBRS quantity is greater than delivered quantity 
Because it is not possible, in this instance, to know which portion of basis is relevant, 
it is not possible to use any of it for tracking and calculation purposes. 
NOTE 1: 
Some [[Broker]]/dealer reporting brokers have indicated they may, from time to time, 
send a greater CBRS quantity than that indicated on the corresponding transaction. 
This is typically due to earned dividends received between placement and [[settlement]]. 
Users will need to decide how they will handle these situations (e.g. suspend activity 
for manual review and completion, reject outright). 
NOTE 2: 
If CBRS quantity is less than the delivered quantity, basis can be used. The 
remainder of [[shares]] should be considered non-covered for calculation and tracking 
purposes. As a reminder, it is the receiving firm’s responsibility to request information 
from the delivering firm, if data is not received. Therefore, the recommended practice 

---

## Page 32

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 32 
CBRS [[Asset]] Record–Elaboration on Select Fields for Mutual Funds21 
is to send a cost basis request record (Record Indicator 04 = Request) for any 
missing [[shares]], prior to making non-covered. 
03 = [[CUSIP]] does not belong to [[issuer]]/[[transfer agent]] 
Typically, this will not be encountered in the Mutual Fund space and was primarily 
intended for other entities using CBRS. However, this can be used if the Fund 
recipient cannot [[Locate]] the [[CUSIP]] under their [[NSCC]] and/or CBRS client number. 
CBRS Tax Lot Records 
The following elaborates on the mutual fund usage and perspective on key fields comprising the CBRS Tax Lot 
Records. Please note that record layouts are subject to change. Please visit https://dtcclearning.com/products -
and-services/equities-clearing/cbrs/cbrs-technical-resources.html for most recent version of the layouts. In no 
way should this information be viewed as standalone. Instead it is supplemental to [[DTCC]]’s CBRS User Guide 
governing the overall usage of CBRS by the financial services industry.  
CBRS Tax Lot Record–Elaboration on Select Fields for Mutual Funds22 
FIELD NAME COMMENTS AND GUIDANCE FOR FIELD USAGE 
Record Content 
Indicator 
Record Content Indicator defines the type of information represented by this Tax Lot 
Record. 
Regarding 01 = Original Tax Lot Record. 
This record is sent by the Delivering Firm, or the reporting [[Broker]] that delivers [[shares]] as a 
result of the transfer. 
Regarding 02 = Corrected Tax Lot Record. 
This record is sent by the Delivering Firm, or the reporting [[Broker]] that delivers [[shares]] as a 
result of the transfer. 
When one tax lot is corrected, it is assumed the entire CBRS response requires correction. 
For example: 
Transfer 1,000.000 [[shares]] in three tax lots, as follows: 
Tax Lot 1 = 500.000 [[shares]] 
Tax Lot 2 = 250.000 [[shares]] 
Tax Lot 3 = 250.000 [[shares]] 
If details on Tax Lot 3 need to be corrected/resent, all three tax lot records should be 
included. Tax Lots 1 and 2 should also be resent, to maintain the integrity of the relationship 
between tax lots and transferred [[shares]]. 
NOTE: 
At least one (1) corresponding tax lot record must be indicated as Corrected. 
Regarding 03 = Firm Reject Record and 04 = Request Record. 
These records are sent by the Receiving Firm, or the reporting [[Broker]] that receives [[shares]] as 
a result of the transfer. 
Records are sent only when necessary and to maintain compliance with regulations. 
 
22 Please refer to [[DTCC]]’s CBRS User Guide for more detail on Tax Lot Record, Required/Optional Field Designations and Usage  

---

## Page 33

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 33 
CBRS Tax Lot Record–Elaboration on Select Fields for Mutual Funds22 
NOTE: 
The recommended practice is to not submit a Record Content Indicator 03 = Firm Reject 
Record in response to a 04 = Request Record received, even if it is not applicable to the 
receiving reporting [[Broker]]. 
Transaction Type Transaction Type identifies the actual [[DTCC]]-based or manual transaction that created the 
need to transfer cost basis through CBRS. 
The only applicable Transaction Types for [[Mutual Funds]] are as follows: 
46 = Fund to Firm Mutual Fund Transfer (ACATS PTF) 
51 = Firm to Fund Mutual Fund Transfer (ACATS PTF) 
56 = Networking Transaction 
57 = Manual Mutual Fund Transfer 
Transfer Control 
Number 
The Transfer Control Number corresponds to the unique identifier assigned to the 
corresponding transaction, either through use of a [[DTCC]] product (e.g.: ACATS (ACATS 
Fund/SERV) or Networking) or manually. The number is used by the recipient to link CBRS 
information to its corresponding transaction. 
If Transaction Type is 46 = Fund to Firm Mutual Fund Transfer or 51 = Firm to Fund 
Mutual Fund Transfer; this field is the Fund/SERV® Control Number–Position 45-59 
(Variable) or Record 1, Position 41-55 (Fixed) on the Fund/SERV® 018 record. ACATS users 
can find this number in Position 153-163 (Variable) or Record 3, Position 8- 18 (Fixed) of the 
ACATS Output Fund/SERV® Statistics file (SIAC720–variable; SIAC726–fixed). 
Firms using the Fund/SERV Control # from the ACATS-Fund/SERV Statistics File should add 
the letters “CATS” to the front of it, in order to match the number that Funds should provide in 
this field. 
If transaction type is 56 = Networking Transaction, then the control number is the 
Networking Control Number, found in Record 1, Position 14-24 of the Networking 
Conversion/Acknowledgement B52/F53 record. 
For all other transaction types, 57 = Manual Mutual Fund Transfer; this field is the control 
number agreed upon by the contra-parties involved in the original [[securities]] transaction. The 
Control Number is the same as what is provided on the Networking F55 Activity Record, 
Record 4, Position 23-37. 
In all instances, data should be left-justified and blank-filled in this alpha-numeric field on the 
CBRS file. 
Alternate Control 
Number 
The Alternate Control Number, when available, corresponds to an additional unique 
identifier assigned to a corresponding transaction, either through use of a [[DTCC]] product or 
manually. This field comes into play when data is being passed between two different [[DTCC]] 
products, such as ACATS and ACATS-Fund/SERV. 
If Transaction Type 46 = Fund to Firm Mutual Fund Transfer and 51 = Firm to Fund 
Mutual Fund Transfer, the ACATS Control Number must be provided in this Field, found in 
Position 683-702 (Variable) or Record 8, Position 28-47 (Fixed) of the Fund/SERV® 018 
record. It is also found in Position 12-15 (Variable) or Record 1, Position 8-21 (Fixed) of the 
ACATS Transfer Input record (Autoroute 36667–variable; 32667–fixed). If not provided, the 
record will reject. 
Data should be left-justified and blank-filled in this alpha-numeric field on the CBRS file 
Contra Firm Number 
NOTE: 
This section applies to 
Record Content 
The Contra Firm Number corresponds to either the Firm Account Number, or, if not 
available, the CBRS User Account Number associated with the entity receiving this CBRS 
Tax Lot Record. 

---

## Page 34

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 34 
CBRS Tax Lot Record–Elaboration on Select Fields for Mutual Funds22 
Indicator 01 (Original) 
and Record Content 
Indicator 02 (Corrected) 
This number should always be obtained through validation against the CBRS User Master 
File, updated and distributed daily by [[DTCC]]. 
The Contra Firm Number is populated based on relationship to the CBRS record itself, and 
not the corresponding transaction record. Therefore, the entity receiving the CBRS record is 
always considered the receiving firm. 
The following fields can come into play in validating against the CBRS User Master File as to 
what the Contra Firm Number on the CBRS record should be. In all instances, data is 
passed with lead zeros and right-justified: 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 
The firm is the recipient of this record. 
If populated, Originating Receiver Firm Number–Position 745-748 (Variable) or Record 8, 
Position 90-93 (Fixed) on the Fund/SERV® 018 record–it means an MF Agent is in use. This 
can be used to assist with validation against the CBRS User Master File. 
ELSE 
Firm Number–Position 12-15 (Variable) or Record 1, Position 8-11 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User Master 
File. 
Original Deliverer Number–Positions 49-52 (Variable) or Record 1, Position 45-48 (Fixed) on 
the ACATS record can be used to assist with validation against the CBRS User Master File. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
The fund is the recipient of this record. 
Fund Number–Position 24-27 (Variable) or Record 1, Position 20-23 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User Master 
File. 
Original Receiver Number–Position 41-44 (Variable) or Record 1, Position 37-40 (fixed) on 
the ACATS record can be used to assist with validation against the CBRS User Master File. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 or Trust-Networked Level 0 account assets in a Network Level 
4 or non-networked account, the fund is the recipient of the CBRS record. If provided, the 
Clearing/Settling Fund Number–Position 10-13 on the Networking B52/F53 record can be 
used to assist with validation against the CBRS User Master File. 
If B52 places Network Level 4 or non-networked account assets in a Network Level 3 or 
Trust-Networked Level 0 account, the firm is the recipient of the CBRS record. The 
Clearing/Settling Firm Number–Position 6-9 on the Networking B52/F53 record can be used 
to assist with validation against the CBRS User Master File. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account assets are transferred into a Network 
Level 4, or non-networked account, the fund is the recipient of the CBRS record. 
If Network Level 4 or non-networked account assets are transferred into a Network Level 3 or 
Trust-Networked Level 0 account, the firm is the recipient of the CBRS record. 
Information on the Manual Transfer instruction will need to be consulted against the CBRS 
User Master File to identify the appropriate reference. 
Contra Firm Number 
NOTE: 
This section applies to 
Record Content 
Indicator 03 (Firm Reject) 
The Contra Firm Number corresponds to either the Firm Account Number, or, if not 
available, the CBRS User Account Number associated with the entity receiving this CBRS 
Tax Lot Record. 
This number should always be obtained through validation against the CBRS User Master 
File, updated and distributed daily by [[DTCC]]. 

---

## Page 35

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 35 
CBRS Tax Lot Record–Elaboration on Select Fields for Mutual Funds22 
and Record Content 
Indicator 04 (Request) 
The Contra Firm Number is populated based on relationship to the CBRS record itself, and 
not the corresponding transaction record. Therefore, the entity receiving the CBRS record is 
always considered the receiving firm. 
The following fields can come into play in validating against the CBRS User Master File as to 
what the Contra Firm Number on the CBRS record should be. In all instances, data is 
passed with lead zeros and right-justified: 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 
The fund is the recipient of this record. 
Fund Number–Position 24-27 (Variable) or Record 1, Position 20-23 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User Master 
File. 
Original Receiver Number–Position 41-44 (Variable) or Record 1, Position 37-40 (fixed) on 
the ACATS record can be used to assist with validation against the CBRS User Master File. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
The firm is the recipient of this record. 
If populated, Originating Receiver Firm Number–Position 745-748 (Variable) or Record 8, 
Position 90-93 (Fixed) on the Fund/SERV® 018 record–it means an MF Agent is in use. This 
can be used to assist with validation against the CBRS User Master File. 
ELSE 
Firm Number–Position 12-15 (Variable) or Record 1, Position 8-11 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User Master 
File. 
Original Deliverer Number–Positions 49-52 (Variable) or Record 1, Position 45-48 (Fixed) on 
the ACATS record can be used to assist with validation against the CBRS User Master File. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 or Trust-Networked Level 0 account assets in a Network Level 
4 or non-networked account, the firm is the recipient of the CBRS record. The 
Clearing/Settling Firm Number–Position 6-9 on the Networking B52/F53 record can be used 
to assist with validation against the CBRS User Master File. 
If B52 places Network Level 4 or non-networked account assets in a Network Level 3 or 
Trust-Networked Level 0 account, the fund is the recipient of the CBRS record. If provided, 
the Clearing/Settling Fund Number–Position 10-13 on the Networking B52/F53 record can be 
used to assist with validation against the CBRS User Master File. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account assets are transferred into a Network 
Level 4, or non-networked account, the firm is the recipient of the CBRS record. 
If Network Level 4 or non-networked account assets are transferred into a Network Level 3 or 
Trust-Networked Level 0 account, the fund is the recipient of the CBRS record. 
Information on the Manual Transfer instruction will need to be consulted against the CBRS 
User Master File to identify the appropriate reference. 
Contra Firm Type Receiving Firm Type clarifies the type of entity receiving the CBRS record. This is important 
because the same client number can be assigned by [[DTCC]] to different firms across services 
of [[DTCC]] subsidiaries. This type corresponds to the type of number in the Contra Firm 
Number field and is obtained from the CBRS User Master File. 
Values: 
AGTNBR = [[transfer agent]] (not relevant to [[Mutual Funds]]) 
CBRACT = CBRS-Only Use 
DTCPRT = [[DTC]] Client 

---

## Page 36

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 36 
CBRS Tax Lot Record–Elaboration on Select Fields for Mutual Funds22 
NSCPRT = [[NSCC]] Client 
Submitting Firm Number 
NOTE: 
This section applies to 
Record Content 
Indicator 01 (Original) 
and Record Content 
Indicator 02 (Corrected) 
The Submitting Firm Number corresponds to the Firm Account Number, or, if not 
available, the CBRS User Account Number associated with the entity submitting this CBRS 
Tax Lot Record. 
This number should always be obtained through validation against the CBRS User Master 
File, updated and distributed daily by [[DTCC]]. 
The Submitting Firm Number is populated based on relationship to the CBRS record itself, 
and not the corresponding transaction record. Therefore, the entity submitting the CBRS 
record is the submitting firm. 
The following fields can come into play in validating against the CBRS User Master File as to 
what the Submitting Firm Number on the CBRS record should be. In all instances, data is 
passed with lead zeros and right-justified: 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 
The fund is the submitter of this record. 
Fund Number–Position 24-27 (Variable) or Record 1, Position 20-23 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User Master 
File. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
The firm is the submitter of this record. 
If populated, Originating Receiver Firm Number–Position 745-748 (Variable) or Record 8, 
Position 90-93 (Fixed) on the Fund/SERV® 018 record–it means an MF Agent is in use. This 
can be used to assist with validation against the CBRS User Master File. 
ELSE 
Firm Number–Position 12-15 (Variable) or Record 1, Position 8-11 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User Master 
File. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 or Trust-Networked Level 0 account assets in a Network Level 
4 or non-networked account, the firm is the submitter of the CBRS record. The 
Clearing/Settling Firm Number–Position 6-9 on the Networking B52/F53 record can be used 
to assist with validation against the CBRS User Master File. 
If B52 places Network Level 4 or non-networked account assets in a Network Level 3 or 
Trust-Networked Level 0 account, the fund is the submitter of the CBRS record. If provided, 
the Clearing/Settling Fund Number–Position 10-13 on the Networking B52/F53 record can be 
used to assist with validation against the CBRS User Master File. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account [[Asset]] is transferred into a Network 
Level 4, or non-networked account, the firm is the submitter of the CBRS record. 
If Network Level 4 or non-networked account [[Asset]] is transferred into a Network Level 3 or 
Trust-Networked Level 0 account, the fund is the submitter of the CBRS record. 
Information on the Manual Transfer instruction will need to be consulted against the CBRS 
User Master File to identify the appropriate reference. 
Submitting Firm Number 
NOTE: 
This section applies to 
Record Content 
Indicator 03 (Firm Reject) 
The Submitting Firm Number corresponds to the Firm Account Number, or, if not 
available, the CBRS User Account Number associated with the entity submitting this CBRS 
Tax Lot Record. 
This number should always be obtained through validation against the CBRS User Master 
File, updated and distributed daily by [[DTCC]]. 

---

## Page 37

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 37 
CBRS Tax Lot Record–Elaboration on Select Fields for Mutual Funds22 
and Record Content 
Indicator 04 (Request) 
The Submitting Firm Number is populated based on relationship to the CBRS record itself, 
and not the corresponding transaction record. Therefore, the entity submitting the CBRS 
record is the submitting firm. 
The following fields can come into play in validating against the CBRS User Master File as to 
what the Submitting Firm Number on the CBRS record should be. In all instances, data is 
passed with lead zeros and right-justified: 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 
The firm is the submitter of this record. 
If populated, Originating Receiver Firm Number–Position 745-748 (Variable) or Record 8, 
Position 90-93 (Fixed) on the Fund/SERV® 018 record–means an MF Agent is in use. This 
can be used to assist with validation against the CBRS User Master File. 
ELSE 
Firm Number–Position 12-15 (Variable) or Record 1, Position 8-11 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User Master 
File. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
The fund is the submitter of this record. 
 
Fund Number–Position 24-27 (Variable) or Record 1, Position 20-23 (Fixed) on the 
Fund/SERV® 018 record can be used to assist with validation against the CBRS User Master 
File. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 or Trust-Networked Level 0 account assets in a Network Level 
4 or non-networked account, the fund is the submitter of the CBRS record. If provided, the 
Clearing/Settling Fund Number–Position 10-13 on the Networking B52/F53 record can be 
used to assist with validation against the CBRS User Master File. 
If B52 places Network Level 4 or non-networked account assets in a Network Level 3 or 
Trust-Networked Level 0 account, the firm is the submitter of the CBRS record. The 
Clearing/Settling Firm Number–Position 6-9 on the Networking B52/F53 record can be used 
to assist with validation against the CBRS User Master File. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account [[Asset]] is transferred into a Network 
Level 4, or non-networked account, the fund is the submitter of the CBRS record. 
If Network Level 4 or non-networked account [[Asset]] is transferred into a Network Level 3 or 
Trust-Networked Level 0 account, the firm is the submitter of the CBRS record. 
Information on the Manual Transfer instruction will need to be consulted against the CBRS 
User Master File to identify the appropriate reference. 
Submitting Firm Type Submitting Firm Type clarifies the type of entity sending the CBRS record. This is important 
because the same client number can be assigned by [[DTCC]] to multiple firms across the 
[[DTCC]] products utilizing CBRS. This type corresponds to the type of number in the 
Submitting Firm Number field. 
Values: 
AGTNBR = [[transfer agent]] (not relevant to [[Mutual Funds]]) 
CBRACT = CBRS User 
DTCPRT = [[DTC]] Client 
NSCPRT = [[NSCC]] Client 

---

## Page 38

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 38 
CBRS Tax Lot Record–Elaboration on Select Fields for Mutual Funds22 
Receiver Customer 
Account Number 
The Receiver Customer Account Number identifies the customer’s account to which the 
CBRS data will be applied. This account number may differ from the BIN ([[Broker]] 
Identification Number) and may represent an underlying sub-account available to the firm in 
question. 
Identification Number) and may represent an underlying sub-account available to the firm in 
question. 
The Receiver Customer Account Number is ALWAYS populated based on relationship to 
the corresponding transaction record; it ALWAYS references the account that should receive 
the cost basis information and is not impacted by the value of the Record Content Indicator. 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 
If populated, Originating Receiver Customer Account Number at Firm–Position 547-566 
(Variable) or Record 6, Position 78-97 (Fixed) on the Fund/SERV® 018 record–means an MF 
Agent is in use, and this field should be used. 
ELSE 
Customer Account Number at Firm–Position 572-591 (Variable) or Record 7, Position 10-29 
(Fixed) of the Fund/SERV® 018 record. 
Original Receiver Customer Account Number–Position 53-72 (Variable) or Record 1, Position 
49-68 (Fixed) of the ACATS record. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
Customer Account Number at Fund–Position 140-159 (Variable) or Record 2, Position 43-62 
(Fixed) of the Fund/SERV® 018 record. 
OR 
Original Receiver Customer Account Number–Position 53-72 (Variable) or Record 1, Position 
49-68 (Fixed) of the ACATS Transfer record. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 or Trust-Networked Level 0 account assets in a Network 4 or 
non-networked account, use the Credit Account Number–Record 1, Position 57-76 of the 
Networking B52/F53 record, which should reference the Fund’s Account Number. 
If B52 places Network Level 4 or non-networked account assets in a Network Level 3, or 
Trust-Networked Level 0 account, first use the Credit Sub-Account Number–Record 4, 
Position 46-65 of the Networking B52/F53 record. If the Credit Sub-Account Number is blank, 
use the Credit Account Number–Record 1, Position 57-76 of the Networking B52/F53 record, 
which should reference the Firm’s Account Number. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account assets are transferred into Network 
Level 4, or non-networked account, this field should carry either the Underlying Customer 
Account Number or the Fund’s Account Number. 
If Network Level 4 or non-networked account assets are transferred into a Network Level 3, 
or Trust-Networked Level 0 account, this field should carry either the Underlying Customer 
Account Number or the Firm’s Account Number. 
Deliverer Customer 
Account Number 
The Deliverer Customer Account Number identifies the customer’s account from which the 
CBRS data will be sent. This account number may differ from the BIN ([[Broker]] Identification 
Number) and may represent an underlying sub-account available to the firm in question. 
The Deliverer Customer Account Number is ALWAYS populated based on relationship to 
the corresponding transaction record; it ALWAYS references the account from which cost 
basis information is sent and is not impacted by the value of the Record Content Indicator. 
Transaction Type 46 = Fund to Firm Mutual Fund Transfer 

---

## Page 39

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 39 
CBRS Tax Lot Record–Elaboration on Select Fields for Mutual Funds22 
Customer Account Number at Fund–Position 596-615 (Variable) or Record 7, Position 54-73 
(Fixed) of the Fund/SERV® 018 record. 
OR 
Original Deliverer Customer Account Number–Position 173-192 (Variable) or Record 3, 
Position 38-57 (Fixed) of the ACATS Transfer record. 
Transaction Type 51 = Firm to Fund Mutual Fund Transfer 
If populated, Original Deliverer Customer Account Number–Position 177-196 (Variable) or 
Record 2, Position 80-99 (Fixed) of the Fund/SERV 018. 
ELSE 
Customer Account Number at Firm–Position 572-591 (Variable) or Record 7, Position 10-29 
(Fixed) of the Fund/SERV® 018 record. 
Original Deliverer Customer Account Number–Position 173-192 (Variable) or Record 3, 
Position 38-57 (Fixed) of the ACATS Transfer record. 
Transaction Type 56 = Networking Transaction 
If B52 places Network Level 3 and Trust-Networked Level 0 account assets in a Network 4 or 
non-networked account, first use the Debit Sub-Account Number–Record 4, Position 66-85 of 
the Networking B52/F53 record. If the Debit Sub-Account Number is blank, use the Account 
Number–Record 1, Position 36-55 of the Networking B52/F53 record, which should reference 
the Firm’s Account Number. 
If B52 places Network Level 4, or non-networked account assets in a Network Level 3, or 
Trust-Networked Level 0 account, use the Account Number–Record 1, Position 36-55 of the 
Networking B52/F53 record, which should reference the Fund’s Account Number for the 
transaction. 
Transaction Type 57 = Manual Mutual Fund Transfer 
If Network Level 3 or Trust-Networked Level 0 account assets are transferred into a Network 
Level 4, or non-networked account, this field should carry either the Underlying Customer 
Account Number or the Firm’s Account Number. 
If Network Level 4 or non-networked account assets are transferred into a Network Level 3, 
or Trust-Networked Level 0 account, this field should carry either the Underlying Customer 
Account Number or the Fund’s Account Number. 
ISIN Country Code Value is US 
ISIN Security Issue [[ID]] 
([[CUSIP]]) 
Security Issue [[ID]] ([[CUSIP]]) of the Security in question 
ISIN Security Check 
Digit 
If the ISIN Country Code passed is ‘US’, this field can be left blank. 
[[Asset]] Description This field should be populated with the same Security Issue [[ID]] ([[CUSIP]]) Fund Name found on 
Mutual Fund Profile, if a client. Otherwise, field should be populated in a way to clearly 
identify the Security Issue [[ID]]. 
Certificate Number 
Prefix 
Leave Blank 
Certificate Number Leave Blank 
Non-covered/Pending 
Indicator 
Field notes if the tax lot information is not covered by the IRS requirement to report cost 
basis. If the lot information is exempt from IRS reporting, indicates the reason the lot is 
exempt. 
Blank = If basis on this tax lot is covered 

---

## Page 40

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 40 
CBRS Tax Lot Record–Elaboration on Select Fields for Mutual Funds22 
01 = Non-covered Lot. This indicates the lot is not covered by the Cost Basis reporting 
requirement to the IRS. Non-covered lots can still carry valid cost basis information. 
02 = Non-covered Account. This indicates the account itself is not covered by the Cost 
Basis reporting requirement to the IRS. Lots in non-covered accounts can still carry valid cost 
basis information. An example would be a type of account (retirement) or recipient (C-
Corporation). 
03 = Pending. If basis on this tax lot is pending receipt by the delivering firm, which is 
sometimes the case in account consolidation/pass-through arrangements, this value should 
be used. 
04 = Certificate in Customer Name. This status is not applicable to [[Mutual Funds]]. Because 
the Fund’s [[transfer agent]] is the sole [[issuer]] of certificated [[shares]], [[shares]] transferred must 
either have the certificate deposited or a surety bond issued to replace the [[shares]]. In other 
words, these [[shares]] should always be available for cost basis calculation within the mutual 
fund account. 
Taxes Reported by 
[[issuer]]/[[transfer agent]] 
Leave Blank 
Gifted or Inherited 
Indicator 
Tax lots related to gift and/or inheritance transactions often receive special treatment for 
calculating, tracking, and reporting cost basis. Refer to the CBRS User Guide for all valid 
values. 
If the tax lot pertains to a transaction that is neither a gift nor inheritance, leave Blank. 
If the tax lot pertains to a gift transaction, either 01 = Gifted or 03 = Inherited then Gifted 
must be populated. Additionally, CBRS will expect Date of Gift and Fair Market Value as of 
Date of Gift to also be populated. 
Date of Gift If Gifted or Inherited Indicator is 01 = Gifted or 03 = Inherited then Gifted, field indicates 
date of gift. 
If not a Gift transaction, leave Blank. 
If a Gift transaction, must be a valid date. Format CCYYMMDD 
Fair Market Value as of 
Date of Gift 
If Gifted or Inherited Indicator is 01 = Gifted or 03 = Inherited then Gifted, field indicates 
the Fair Market Value on the date of gift. 
If not a Gift transaction, leave Blank. 
If a Gift transaction, a value is required. 
NOTE: 
Zeros are considered a valid value. 
Tax Lot Quantity The quantity of the tax lot being transferred. 
NOTE: 
The sum of the Tax Lot Quantity fields of the Tax Lot records must equal the Total Position 
Quantity reported on the corresponding [[Asset]] Record. 
Position Code Value is always ‘L’ 
Acquisition Date of Tax 
Lot 
Value reflects the original acquisition date of the [[shares]] by the shareholder, adjusted for any 
wash sales. This may or may not reflect the trade/transaction date held on the shareholder 
recordkeeping system. 
Format: CCYYMMDD 

---

## Page 41

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Annotated CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] 41 
CBRS Tax Lot Record–Elaboration on Select Fields for Mutual Funds22 
Additional considerations: 
• If the Tax Lot Current Cost is zero because it is an unknown value (Zero Basis 
Indicator is 02 = Unknown), the Tax Lot Current Cost field should be passed as Blank. 
[[DTCC]] will blank out the field if it is populated. 
• If the tax lot reflects an aggregation of multiple tax lots, a value of 19010101 is used to 
designate the IRS-permitted designation of VARIOUS on Cost Basis reporting to the 
shareholder and IRS. 
Original Acquisition 
Date for Wash Sale 
Adjustment 
Since the Acquisition Date of Tax Lot is adjusted for the impact of wash sales, it is 
suggested the original acquisition date for any tax lots that have been adjusted by a wash 
sale is provided in this field. 
ISO Currency Code Value is always ‘USD’ 
Exchange Rate Leave Blank 
Tax Lot Original Cost Leave Blank 
Tax Lot Current Cost Provide the current cost associated with the tax lot in question. The ICI BDAC CBR Task 
Force has selected this field as the required field to provide tax lot cost information, to provide 
standardization across the Industry in adopting CBRS. 
NOTE: 
All tax lots that have been valued at the account’s Average Cost should report that value in 
this field. 
A zero and/or blank value is accepted in this field, but it must be clarified by the Zero Basis 
Indicator field. 
Zero Basis Indicator Clarifies the intent of a zero or blank value in the Tax Lot Current Cost field. 
If Tax Lot Current Cost is greater than zero, then leave Blank. 
If Tax Lot Current Cost is equal to zero, then clarification must be provided in this field if that 
is 01 = True Zero or 02 = Unknown basis information. 
If Tax Lot Current Cost is equal to ‘blank’, then this field must be 02 = Unknown. 
Tax Lot Original Unit 
Price 
Leave Blank 
Employee Plan [[shares]] 
Indicator 
Leave Blank 
Purchase/[[Dividend]] 
Reinvestment Indicator 
Leave Blank, which will [[default]] to P = Purchase 
This field is no longer needed. It was originally to be used for Corporate Action adjustments to 
tax lots, but since the [[Broker]] holding the tax lot on the effective date of the Corporate action 
must adjust the cost basis for the Corporate Action, the field no longer is necessary. 

---

## Page 42

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 42 
TRANSFERS OF MUTUAL FUND [[securities]] 
Overview 
CBRS provides operating efficiencies to mutual fund transfer agents, [[Broker]]-dealers and other intermediaries 
by permitting the timely movement of cost basis information for mutual fund [[securities]] from one financial firm to 
another in a standardized, automated, and secure environment. Users should be aware that CBRS neither 
informs users which transactions trigger the need to send or receive cost basis information; nor does it 
calculate basis or provide any reconciliation capabilities for cost basis records that are expected and then 
received. Therefore, the transfer scenarios and other information provided in this section should be considered 
by funds, intermediaries and service providers when programming for the movement of cost basis information 
using CBRS. 
Transfer Methods and Tax Reporting 
Mutual fund transfer processing is not standardized among [[Broker]]/dealers, banks, and mutual fund [[Companies]]. 
The current state of the fund transfer processing remains fragmented with segments that are fully automated 
and other areas that are completely manual. Roughly 90% of transfer activity is initiated by firms. The following 
categories represent the customary methods used to execute fund transfers. If one of the automated solutions 
fails or is not supported by a fund or [[intermediary]], it is common for such transfer requests to be processed 
manually. 
• ACATS-Customer account transfers between [[Broker]]/dealers (firms) are highly automated through 
[[NSCC]]’s Automated Customer Account Transfer System (“ACATS”). ACATS may also be used to a limited 
extent for mutual fund transfers between banks and [[Broker]]/dealers. This guide does not address ACATS 
transfers between [[Broker]]/dealers, or banks and [[Broker]]/dealer firms for assets other than [[Mutual Funds]].  
• ACAT
S - Fund/SERV–This link between two [[NSCC]] systems automates the re-registration of mutual fund 
positions. Participation in ACATS and ACATS-Fund/SERV is required for brokers and voluntary for banks. 
Fund participation in ACATS-Fund/SERV is authorized on a fund-by-fund basis. 
• [[NSCC]]’s Fund/Firm Transfer Capabilities23 (ACATS PTF)-A transfer type which leverages ACATS and 
ACATS-Fund/SERV, [[Broker]]-initiated in-kind transfers may be submitted using this automation. [[Broker]]-
initiated in-kind transfers are submitted through ACATS. In turn, the [[NSCC]] processes the request and 
forwards it to the fund through ACATS-Fund/SERV. Fields are incorporated into ACATS-Fund/SERV to 
provide funds with sufficient transparency to systematically verify that only like account types (e.g., IRA to 
IRA for retirement scenarios) are being transferred, and to assist funds in validating customer information. 
Upon verification of the ACATS-Fund/SERV record, the fund can elect to systematically re-register the 
[[shares]] without the need of manual intervention. 
• N
etworking– While not originally designed to automate the transfer process, many brokerage firms, 
working directly with funds, have adapted the Networking functionality along with Change of Dealer 
enhancements to facilitate transfer processing. This method, however, does not generally cover all types 
of transfers or all types of accounts and cannot be used to move [[shares]] to be held directly by funds.  
• Man
ual (aka non -ACAT)–This costly, labor intensive, paper-based process relies on physical delivery of 
paperwork and manual processing without any automated tracking. Fund [[Companies]] and [[Broker]] dealers 
receive large numbers of manual transfer requests that are processed outside of the automated services 
 
23 This functionality addresses firm -initiated retirement and non -retirement account re- registrations that move [[shares]] from firm (i.e., Networking Level 3 or 
omnibus accounts) to existing fund direct accounts, as well as from fund direct accounts to firms. These types of re-registrations are referred to as “in -kind 
transfers” although, in fact, no [[Asset]] actually transfers between the fund and [[intermediary]], and the [[shares]] are simply re-registered on the books of the fund. See 
“Best Practices Fund Firm (PTF) Transfer Capa bility Best Practices” on the [[DTCC]] Learning at:  https://dtcclearning.com/products-and-services/equities-
clearing/acats/acats-best-practices.html 
 

---

## Page 43

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 43 
mentioned above. This lack of automation is a source of a disproportionate number of client complaints 
due to the time required to complete the transactions and has historically been a focus of regulators.  
 
A cost basis transfer reporting statement is required to be sent on 1099-B taxable accounts, when transfers 
occur between reporting brokers, including mutual fund transfer agents and financial intermediaries. The 
entities responsible for tax reporting on the account types listed below are as follows 24: 
Matrix Level/Account Type Tax Reporting Responsibility 
Level 0 Fund 
Level 3 Firm 
Level 4 Fund 
Omnibus or House Account (by social/any matrix level) Firm 
Trust Networked Accounts (Levels 0 or 4) Bank/Trust 
 
Reporting brokers use a number of identifiers to track when a transfer between reporting brokers occurs, the 
most common of which is the [[NSCC]] Network Control Indicator (commonly referred to as the Matrix Level). 
These transfers are triggering events that require the subsequent movement of cost basis reporting records 
(through CBRS). The table below illustrates the various account transfer methods that are utilized for trans fers 
between funds and financial intermediaries by account types when the 1099-B tax reporting responsibility 
changes. 
 
Tax Reporting Responsibilities for Transfers between Account Types:  
To Account Type: 
From Account Type: 
 Transfer Type Matrix 0,4 Matrix 3 Omnibus/House 
Acct 
Trust Networked 
CB moves within 
Fund internally 
Fund Delivers CB 
to Firm 
Fund Delivers CB 
to Firm 
Fund Delivers CB 
to Firm 
Matrix 0,4 ACATS FS - Alternate Alternate Alternate 
ACATS PTF - Preferred Preferred Alternate 
B52 - - - Preferred 
Manual Alternate Alternate Alternate Alternate 
 Fund Receives CB 
from Firm 
CB moves between 
firms 
CB moves between 
firms 
CB moves between 
firms 
Matrix 3 ACATS FS Alternate Preferred Preferred Alternate 
 
24 The list reflects tax reporting responsibilities by Matrix Level/Account Type as defined in the [[NSCC]] Networking Technical Guide. As noted in Appendix B, firms 
and funds must evaluate their business arrangements and legal agreements and implement changes, where tax reporting responsibilities are split between 
entities, to ensure that all shareholders receive accurate, timely and complete tax reporting.  

---

## Page 44

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 44 
To Account Type: 
ACATS PTF Preferred Alternate Alternate Alternate 
B52 - Preferred Preferred Preferred 
Manual Alternate Alternate Alternate Alternate 
Omnibus/ 
House 
ACATS FS Alternate Preferred Alternate Alternate 
ACATS PTF Preferred Alternate Alternate Alternate 
B52 Alternate Preferred Preferred Preferred 
Manual Alternate Alternate Alternate Alternate 
Trust 
Networked 
ACATS FS Alternate Alternate Alternate Alternate 
ACATS PTF Alternate Alternate Alternate Alternate 
B52 Preferred Preferred Preferred Preferred 
Manual Alternate Alternate Alternate Alternate 
 
Key Terms: 
• ACATS FS: ACATS-Fund/SERV Transfer (via 018 record) 
• ACATS PTF: ACATS-PTF/ACATS-Fund/SERV Transfer-in-kind or Fund to Firm’ (Pull initiated by Firm) or 
‘Firm to Fund’ (Push initiated by Firm) 
• B 52: Networking Transfer (via B52 record)  
• Manual: Manual Transfer 
• CB: Cost Basis Information 
Note: 
The preferred or recommended transfer method(s) used are highlighted above and alternate transfer methods utilized are 
also identified. 
Other maintenance transactions not captured above also can change existing tax reporting responsibilities. 
The following industry recommended practice was developed to prevent certain maintenance record requests 
from occurring that would change existing tax reporting responsibilities and trigger cost basis transfer reporting.  
Industry Recommended Practice:  
[[NSCC]]’s Networking service provides functionality that enables a Networking Maintenance B51 record to process a matrix 
level change on an account held at the fund. In some cases, the B51 Maintenance requested changes the control of the 
account and the tax reporting responsibility. Therefore, any networking maintenance change on an account that would 
change the existing tax reporting responsibility on mutual fund [[shares]] should be processed through a transfer transaction 
and not by utilizing the Networking Maintenance B51 record. 
[[DTCC]] for Cost Basis Reporting 
The records used to facilitate transfer activities are different than records passed through the [[DTCC]]’s Cost 
Basis Reporting Service. Funds and firms need to link the movement of [[shares]] (transfer activity)  to the CBRS 

---

## Page 45

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 45 
records that would follow in order to correctly apply cost basis information received to the correct customer 
account in an automated and standardized fashion.  
• Underlying Customer Account Numbers in an Omnibus environment (Activity Record F55) 
The “Underlying Customer Account Number” and “Opposing Underlying Customer Account Number” fields 
are found on the Activity Record F55 (Important Notices a7175 and a7241r). 
These fields facilitate greater transparency when transferring [[shares]] in an Omnibus environment, allowing 
funds to pass the sub-account number (if received on instructions for manual transfers to an omnibus 
account) which is communicated to the firms for direct transfers via the F55 Record.  
 
These fields should be populated from the perspective of the recipient of the F55. Therefore the 
“Underlying Customer Account Number” on the F55 generated for one side of the transfer becomes the 
“Opposing Underlying Customer Account Number” on the F55 generated for the other side of the transfer.  
 
Field Name Start End Len Type Description Opt/Req 
Underlying Customer Account 
Number 
76 95 20 A/N Underlying Customer Account Number 
at the Firm receiving the F55 record 
O 
 
Field Name Start End Len Type Description Opt/Req 
Opposing Underlying 
Customer Account Number 
28 47 20 A/N Underlying Customer Account Number 
at the Firm delivering the F55 record 
O 
 
• “Opposing Originating /Underlying Firm Number” and “Originating /Underlying Firm Number ” fields on the 
Activity Reporting Record F55 (Important Notice a7665) 
 
These fields will assist in reporting the Underlying Firm information on F55 records when an Introducing Firm 
(MF Agent) is involved. The data is used to communicate appropriate details on manual transfers and transfer 
cancellations. 
It is recommended that funds populate these fields with the [[NSCC]] [[ID]] number when MF Agent information is 
known for the above transaction types. These fields are Optional fields, as MF Agent is not always involved or 
known. 
It is recommended that on a manual transfer request, the Requesting Firm would provide the related 
Underlying Account details. The Fund would then be expected to pass this additional information on the F55 
record as follows: 
• Firm Debit Original Transfers (to a Fund or another Firm account held at the Fund) would pass the 
information as “Originating/Underlying Firm Number” on the Debit F55 and in the “Opposing 
Originating/Underlying Firm Number” on the Credit F55 sent through Direct Account Networking (i f 
produced). 
• Firm Credit Original Transfers (from a Fund or another Firm account held at the Fund) would pass the 
information as “Opposing Originating/Underlying Firm Number” on the Debit F55 sent through Direct 
Account Networking (if produced) and in the “Originating/Underlying Firm Number” on the Credit F55.  
• Firm to Firm Original Transfers could possibly have two sets of Underlying Account information. If only 
one side has Underlying Account information, it would be passed as indicated above. If BOTH Firms had 
Underlying Account information, a combination of both approaches would be pursued:  

---

## Page 46

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 46 
o DEBIT F55: Debit Firm = Originating/Underlying Firm Number; Credit Firm = Opposing 
Originating/Underlying Firm Number 
o CREDIT F55: Debit Firm = Opposing Originating/Underlying Firm Number; Credit Firm = 
Originating/Underlying Firm Number 
• On a Reversal/Cancel/Void of an ACATS PTF, the transaction is processed manually either from 
instructions or from data available on the 018/019 Fund/SERV record. Processing is similar to the Original 
Manual Transfers, as follows: 
o Reversal of Firm Debit PTF Transfers (to a Fund account)–also known as a PTF PUSH, passes the 
information as “Originating/Underlying Firm Number” on the F55 Transaction Type 33 and in the 
“Opposing Originating/Underlying Firm Number” on the F55 Transaction Type 34 sent through Direct 
Account Networking (if produced). 
o Reversal of Firm Credit PTF Transfers (from a Fund account)–also known as a PTF PULL, would 
pass the information as “Opposing Originating/Underlying Firm Number” on the F55 Transaction 
Type 33 sent through Direct Account Networking (if produced) and in the “Originating/Underlying Firm 
Number” on the F55 Transaction Type 34. 
o A Firm to Firm ACATS PTF is not a valid scenario. 
 
Field Name Start End Len Type Description Opt/Req 
Opposing 
Originating/Underlying Firm 
Number 
82 85 4 A/N Opposing Originating [[Broker]] Firm 
number 
(The underlying firm’s [[NSCC]] [[ID]] 
number, for firms transacting through 
an MF Agent) 
O 
Originating/Underlying Firm 
Number 
86 89 4 A/N Originating [[Broker]] Firm number 
(The underlying firm’s [[NSCC]] [[ID]] 
number, for firms transacting through 
an MF Agent) 
O 
 
• “Opposing Membership Identifier” field on the Activity Reporting Record F55 (Important Notice a7665) 
o This field will assist firms in building their Cost Basis expectancy files to correctly route tax lots to the 
Opposing Party on manual transfers and transfer cancellations. 
 
Field Name Start End Len Type Description Opt/Req 
Opposing Membership 
Identifier 
94 95 2 A/N Required for Transaction Types: 
13 (Direct Transfer) 
33 (Transfer from–Cancellation) 
34 (Transfer to–Cancellation) 
Opposing Membership Identifiers: 
00 = N/A 
01 = Trust 
OC 
 
• Original Control Number–This field is required on the Activity Reporting Record F55 if the transaction type 
is a “direct” (manual) transfer (Transaction Type 13) (Important Notice a7175). 

---

## Page 47

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 47 
 
This requirement allows funds to generate a transfer control number for direct (manual) transactions to 
populate in the F55 “Original Control Number” field. The same control number is also provided on the 
CBRS files, allowing firms to link the CBRS data to the direct (manual) transaction.  
 
Field Name Start End Len Type Description Opt/Req 
Original Control Number 23 37 15 A/N Required if Transaction Type 13 
(“Direct Transfer”) in record 
F55 sequence #1. 
OC 
 
The best practice recommendation for generating an “Original Control Number” for manual transfer 
transactions is as follows: 
Industry Recommended Practice:  
When a control number does not exist or is not provided a Manual Transfer Control Number should be 
generated. The algorithm for creating a Manual Transfer Control Number, which should be referenced in the 
Original Control Number field, is as follows: 
Position Length Field Description Value 
1 1 Direct transfer indicator D 
2 4 [[NSCC]] [[Member]] number for the fund 9999 
6 1 Last digit of current posting year for the transfer transaction 9 
7 3 Posting date of the transfer transaction in Julian date format 999 
10 6 Unique number (random-generated, sequential) 999999 
 
This number should be provided as the Original Control Number on Record 4, Position 23-37 of the Networking F55 
record, plus as the Transfer Control Number for all related CBRS records. 
 
An F55 is used to report manual transactions processed at the fund against a networked account. The 
activity file contains unique codes to identify the type of transaction. In this case the fund would deliver a 
transaction type “13” indicating a direct transfer. 
 
“Networking Control Number”– changed syntax 
Effective with Important Notice a7665 (November 2013), [[NSCC]] updated the syntax of the Networking 
Transfer Control Number to provide greater uniqueness; specifically addressing the need to identity the 
year a transaction takes place for the purposes of Cost Basis reporting.  
Networking Transfer Control Numbers are a key data match point between transactions and CBRS 
records; but they had the potential to repeat annually. This possible duplication could become signi ficant 
when managing CBRS records, especially when corrected tax lots are delivered to replace existing lots on 
a system. The change in the syntax accommodates unique Control Numbers for a 10-year period, which 
is consistent with Fund/SERV. The Control Number format is as follows:  

---

## Page 48

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 48 
Positions: 
1–3 Julian Date 
4 Year 
5–11 Alpha/Numeric 
 
• “Credit Sub-Account Number” and “Debit Sub-Account Number” fields added to the Transfer Detail/Fund 
Acknowledgement Record A/B/T52, F53 (Important Notice a7175) 
These fields allow clients to communicate the underlying sub-account number for Networking transfers 
into or out of an omnibus account. 
 
Field Name Start End Len Type Description Opt/Req 
52/53 
Credit Sub-Account Number 46 65 20 A/N Underlying Credit Customer Account 
Number 
O/O 
Debit Sub-Account Number 66 85 20 A/N Underlying Debit Customer Account 
Number 
O/O 
 
• “Originating Receiver Firm Number” and “Originating Delivering Firm Number” fields added to the 
ACATS–Fund/SERV Transfer Record 018 (Important Notice a7175) 
 
These fields assist the fund in an ACATS-PTF scenario where the firm uses a Mutual Fund Agent for 
processing ACATS transfers. This information will specify the originating parties and allow the fund further 
transparency with regard to the originating parties of the transfer transaction for cost basis reporting.  
 
Variable Format: 
Field Name Start End Len Type Description 
Originating Receiver Firm 
Number 
745 748 4 A/N Originating receiving [[Broker]] firm number 
Originating Delivering Firm 
Number 
749 752 4 A/N Originating delivering [[Broker]] firm number 
 
Fixed Format – sequence 8 
Field Name Start End Len Type Description 
Originating Receiver Firm 
Number 
90 93 4 A/N Originating receiving [[Broker]] firm number 
Originating Delivering Firm 
Number 
94 97 4 A/N Originating delivering [[Broker]] firm number 
 
• “Originating Receiver Customer Account Number at Firm” field to the ACATS– Fund/SERV Transfer 
Record 018 (Important Notice a7175) 

---

## Page 49

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 49 
In the case of an ACATS-PTF scenario, this field allows funds to identify the customer account number 
that is being transferred via the ACATS. The field permits further transparency of the underlying account 
information within an omnibus account. 
 
Variable Format: 
Field Name Start End Len Type Description 
Originating Receiver 
Customer Account Number at 
Firm 
547 566 20 A/N Underlying Customer Account Number at the 
Originating Firm 
 
Fixed Format–sequence 6 
Field Name Start End Len Type Description 
Originating Receiver 
Customer Account Number at 
Firm 
78 97 20 A/N Underlying Customer Account Number at the 
Originating Firm 
 
• “Original Deliverer Customer Account Number” field added to the ACATS–Fund/SERV Transfer Record 
018 (Important Notice a7256) 
In the case of an ACATS-PTF scenario, this field allows funds to identify the customer account number at 
the delivering firm. This field is beneficial in the Cost Basis transfer scenario if the deliverer fails to deliver 
cost basis to the receiving party and the receiver needs to send a request to the deliverer.  
 
Variable Format: 
Field Name Start End Len Type Description 
Original Deliverer Customer 
Account Number 
177 196 20 A/N Underlying Customer Account Number at the 
Delivering Firm 
 
Fixed Format–sequence 2 
Field Name Start End Len Type Description 
Originating Deliverer 
Customer Account Number 
80 99 20 A/N Underlying Customer Account Number at the 
Delivering Firm 
 
• Guidelines for required use of “Transaction Type” 13, 33, 34 on Networking Activity Reporting 
Record F55 (Important Notice a7472) 
 
When confirming transfer activity through Networking F55 records, brokers need to know the opposing account 
information when building their cost basis expectancy files. 
Changes were made to expand the use of the fields below from what was originally designated within the 
context of omnibus/share aging reconciliation. The data is used to communicate appropriate details on manual 

---

## Page 50

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 50 
transfers and transfer cancellation (Manual, ACATS PTF, and Networking) to identify appropriate treatment of 
cost basis on corresponding accounts. 
 Field Name Seq # Start End Opt/Req 
1 Opposing 
Clearing/Settling Firm 
Number 
5 23 26 Optional/Conditional 
Required for Transaction Type = 
13 (Direct Transfer)  
33 (Transfer From–Cancellation) 
34 (Transfer To–Cancellation) 
2 Opposing Network 
Control Indicator 
5 27 27 Optional/Conditional 
Required for Transaction Type =13, 33, 34 
3 Opposing Fund 
Account Number 
4 39 58 Optional/Conditional 
Required for Transaction Type = 13, 33, 34 
 
In the unlikely event that the Opposing Clearing/Settling Firm actually holding cost basis information is not an 
[[NSCC]] [[Member]], the industry recommended practice is to populate this field with the fund’s [[NSCC]] [[Member]] 
number. The fund will then have an additional responsibility to deliver the cost basis information to the non-
participating opposing firm. Firms who wish to explore a cost basis-only membership with [[DTCC]] should contact 
Wealth Management Services at (212) 855-8877. 
• Guidelines for using the “Initiating Firm” Field on the Account Conversion Transfer Detail/Fund 
found on Acknowledgement Record A/B/T52, F53 (Important Notice a7472) 
 
The BDAC CBR Task Force recommends leveraging Networking B52 Mass [[Broker]] to [[Broker]] (Transaction type 
4 = Mass [[Broker]] to [[Broker]]) for ad-hoc [[Broker]]-to-[[Broker]] transfers through Networking. Some funds restrict use 
of Mass [[Broker]] to [[Broker]] transfers by creating permissions which must be configured per -event (“open a 
window”). The Task Force agreed that, if the initiating firm was known and was ALSO the delivering firm, funds 
which restrict use of Transaction Type 4 should allow these “push” transfers (pushed from deliverer to receiver) 
to automatically process, thereby eliminating the manual per-event notification and configuration activities. 
This capability to automatically allow “push” transfers through networking will significantly reduce manual 
transfers, while providing the dual F53 notifications needed by brokers to build accurate cost basis expectancy 
files. The firm initiating the B52 will be required to provide their [[NSCC]] Client Number in the Initiating Firm field 
when completing a transfer with a Transaction Type of 4. It will be optionally included by funds on their F53 
response. 
Field Name Length Opt/Req Type Description 
Initiating Firm 4 Optional/Conditional 
Required on B52 for Transaction Type = 4 
A/N [[NSCC]] Client Number of the 
Firm submitting the transfer 
 
Gifting [[shares]] 
When transferring [[shares]] manually, through Networking B52 Transfer record, or an ACATS PTF 
“push”/ACATS 018 record, it is necessary to indicate whether the transfer is a gift. A gifting designation is 
required in order for special gifting rules to be triggered when applicable. The Networking B52 Transfer and 
ACATS 018 records both contain a field to denote a transfer is related to a gift.  
 

---

## Page 51

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 51 
Transfer Detail/Fund Acknowledgment (A/B/T52, F53) #1 (Important Notice a7256) 
Field Name Start End Len Type Description Opt/Req 
52/53 
Gift Indicator 94 94 1 A/N Space = No 1 = Yes O/O 
 
ACATS Transfer (018) Variable Format: 
Field Name Start End Len Type Description 
Gift/Donation Indicator 744 744 1 A/N 0 or Space = No, not a gift or donation 1 = Yes, it is a 
gift or donation 
 
ACATS Transfer (018) Fixed Format–sequence 8 
Field Name Start End Len Type Description 
Gift/Donation Indicator 89 89 1 A/N 0 or Space = No, not a gift or donation 1 = Yes, it is a 
gift or donation 
 
If the [[shares]] transferred have been gifted, the deliverer of the cost basis information would send the applicable 
[[Asset]] and tax lot(s) records indicating the donor’s original acquisition date, donor’s adjusted basis amount, date 
of gift and the Fair Market Value (FMV) basis on the date of gift. 
Note: 
ACATS PTF ‘Pull’ requests [[DO]] not support a transfer of [[shares]] due to gift (Important Notice a7256). Instead, the 
shareholder must contact the fund directly to execute the transfer. 
Industry Recommended Practice: 
Networking transfers should not be used to ‘pull’ [[shares]] for a transfer due to gift. Instead, the shareholder must contact the 
fund directly to execute the transfer. 
 
Exception/Correction Processing 
Following a full or partial transfer, a fund or firm may need to cancel/correct the actual transfer transaction (e.g. 
to correct the number of [[shares]]). Cancelation or correction of a previously posted transfer transaction must be 
reconciled between the delivering and receiving entities. 
The Industry recommended practice is to cancel the original transfer transaction completely and submit a new 
transfer with correct transaction information. CBRS records from the original transfer transaction should not be 
passed, or if already delivered, these records should be deleted by the receiving entity  as part of the 
cancellation. The fund or firm should not attempt to send CBRS records for a cancellation or correction of a 
transaction in an attempt to cancel out or correct previously sent CBRS records. In all cases, after a 
cancellation is complete, a correct or new transfer transaction and corresponding new CBRS records will then 
be passed. 
A firm may initiate a transfer cancelation/correction by submitting a letter of instruction to the fund. The letter 
should reference the original transfer control number assigned to the ACATS PTF, Networking, or manual 
transfer to be canceled. Alternatively, a fund may determine a transfer needs to be adjusted or canceled and 
will initiate the cancelation/correction process. 

---

## Page 52

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 52 
In either case, the fund should generate a Networking F55 Activity record notifying the firm that the 
correction/cancellation has been processed. This is accomplished through use of the following Networking 
Transaction Types (Important Notice a7256): 
 Field Name Start End Len Type Description 
1 Transaction Type 23 24 2 A/N 33 = Transfer From–Cancellation 
34 = Transfer To-Cancellation 
 
In addition to other required fields, the F55 record should also contain the Original Control Number and Original 
Control Number Indicator that corresponds to the original transfer transaction that is being canceled.  
When the correction is processed, a new transfer transaction and corresponding CBRS records are generated. 
The new transfer transaction should be processed using a new Control Number, and new CBRS records will 
reference only the new Control Number. 
Industry Recommended Practice:  
Industry recommended practice when correcting a transfer transaction is to cancel the original transfer transaction and 
deliver a (to and from) transfer cancelation using the Networking F55 Activity record utilizing the appropriate Transfer 
Cancelation transaction types. 
The original transaction is then voided by both parties, any impact from previously exchanged CBRS records are deleted 
from both the delivering and receiving entities cost basis systems, and a subsequent new transfer transaction and related 
CBRS records are transmitted. 
This recommended practice applies to cancellations/corrections that affect all or a portion of the original transfer and 
related cost basis records. 
Additional information on cancelations/corrections also may be found in Special Considerations and 
Recommended Practices for [[Mutual Funds]] of  this guide.  
CBRS Record Layouts 
The annotated CBRS record layouts and recommended practices for [[Mutual Funds]] are located in Annotated 
CBRS Record Layouts and Recommended Practices for [[Mutual Funds]] of this guide. The detailed CBRS record 
layouts, other guides and documentation may be accessed on [[DTCC]]’s Learning site: 
https://dtcclearning.com/products-and-services/equities-clearing/cbrs.html 
 
MyDTCC Web Portal 
MyDTCC provides [[DTCC]] clients with direct access to [[DTCC]]’s various services and systems by using a 
standard Internet browser. MyDTCC is primarily a menu-driven and transaction-oriented data entry application. 
Each client is provided with a customized menu of applications. 
MyDTCC allows members that have not programmed for an automated connection to CBRS to utilize data-
entry screens and Excel upload/download functionality to send and receive cost basis information through this 
secure web-based service. 
Specific instructions on how to utilize CBRS and MyDTCC are contained in the CBRS User Guide located on 
[[DTCC]]’s Learning site at: https://dtcclearning.com/products-and-services/equities-clearing/cbrs/cbrs-users.html 
 
 

---

## Page 53

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 53 
Cost Basis Reporting Transfer Types and Examples 
The following sub-sections provide greater detail about the transfer types supported by CBRS. Each sub-
section outlines the unique or special characteristics and recommended practices for the applicable transfer 
category. The final sub-section provides specific examples that illustrate how the cost basis information is 
transferred via the CBRS [[Asset]] and Tax lot records, and highlight data populated that will vary based on the 
transfer transaction types. The sub-sections are organized as follows: 
5.2: ACATS PTF Transfers–ACATS PTF “Pull” (the firm requests assets from the fund) and ACATS PTF 
“Push” (the firm sends assets to the fund) processes. 
5.3: Networking Transfers-Firm initiated transfers for networked accounts. 
5.4: Manual Transfers–Requests/instructions to transfer mutual fund [[shares]] are processed manually; 
however, the transfer of cost basis information is facilitated through CBRS. 
5.5: Examples–CBRS [[Asset]] and Tax Lot records are populated for transfer examples utilizing the various cost 
basis methods for mutual fund [[securities]]. The examples presented highlight details for the transfer types 
indicated above, as well as for populating tax lot records for gifted and inherited transactions.  
ACATS PTF Transfers and CBRS 
Introduction 
The ACATS-Fund/SERV Mutual Fund Transfer Capability, known as “ACATS PTF” was developed to eliminate 
manual processing of transfers in kind between fund [[Companies]] and firms in order to improve processing 
efficiencies and complete such transfers in a timely manner. The ACATS PTF process is different from 
“Networking” and "Manual Transfers," as it leverages the existing Automated Customer Account Transfer 
(ACAT) and ACATS-Fund/SERV interfaces. The ACATS PTF process is fully described in “Fund Firm (PTF) 
Transfer Capability User Guide – Best Practices” available on the [[DTCC]] Learning site at 
https://dtcclearning.com/products-and-services/mutual-fund-services/fund-serv.html#resources Those who are 
not members of [[NSCC]] but would be interested in knowing more about the ACATS PTF transfer process should 
contact Wealth Management Services at 212-855-8877. 
This sub-section summarizes the two ACATS PTF transfer scenarios and captures the recommended practices 
for cost basis transfer reporting utilizing CBRS. Both of the ACATS PTF transactions illustrated below are 
initiated by a firm through ACATS. The ACATS PTF “Pull” is where a firm is requesting a mutual fund [[Asset]] 
transfer from a fund-controlled account into a firm-controlled account. The ACATS PTF “Push” refers to a firm 
transferring assets from a firm-controlled account into a fund-controlled account. 
A description of the ACATS PTF [[Asset]] transfer scenarios, related workflows, industry practices and special 
considerations for cost basis transfer reporting are detailed below. 
ACATS PTF – Firm Initiated In-Kind Transfer (“Firm Pull”) 
Situation: Client owns [[shares]] directly with the Mutual Fund Company (Matrix level 0 (non- networked) or     
level 4) in a retirement account or non-retirement account and wishes to transfer those positions in-kind to a 
[[Broker]]/dealer or bank. Client completes all required transfer forms and requests [[Broker]] dealer/bank to begin 
the transfer process. 
Preconditions:  
• Account exists at firm. 
• Security is ACATS-Fund/SERV eligible. 
• Both Firm and Fund participate in the ACATS-Fund/SERV Mutual Fund Transfer Capability (ACATS PTF). 

---

## Page 54

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 54 
Industry Required Practice:  
The receiving firm should never initiate a Gift Transfer using the ACATS PTF “Pull” process. If a (receiving) firm initiates a 
Gift Transfer using the ACATS PTF “Pull” process, the [[NSCC]] will reject the transaction (see [[NSCC]] Importance Notice 
#a7256). 
 
ACATS PTF – Firm Initiated In-Kind Transfer to Fund (“Firm Push”) 
Situation: Client owns [[shares]] of a fund at a [[Broker]]/dealer in a retirement account or non- retirement account 
(Matrix level 3 or omnibus) and wishes to transfer those positions in-kind to a Mutual Fund Company (Matrix 
level 0 (non-networked) or level 4). 
Preconditions:  
• Account must exist directly at the Fund before the transfer can be initiated.  
• Security is ACATS-Fund/SERV eligible.  
• Both Firm and Fund Company participate in the ACATS-Fund/SERV Mutual Fund Transfer Capability. 


---

## Page 55

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 55 
 
Special Considerations for ACATS PTF Transfers 
Fund Rejects 
If the ACATS PTF in either a “Pull” or “Push” scenario is rejected by the fund, a Fund/SERV 019 record is sent 
back to [[NSCC]] indicating the reject code. [[NSCC]] sends the same reject code to the firm via the ACATS Output 
Fund/SERV Statistics file (SIAC720-variable, SIAC726-fixed). Cost basis information should never be 
transmitted if a transfer was rejected via the 019 record. 
Most firms treat the "reject" as a cancelled item. Any new transfer attempt for the same account could be 
handled as a new ACATS PTF transfer or as a manual transfer as described in the Manual Transfers sub-
section of this Guide. 
Resubmitting the new transfer as an ACATS PTF is preferred when possible. The new PTF transfer will receive 
its own Fund/SERV control number that should be used for the CBRS Transfer Control Number value.  
 
Exception Processing or Errors 
As with other transfer transactions, industry practice for ACATS PTF corrections is to reverse the entire 
transaction and reprocess a correct transaction separately. For example, if a PTF is processed against a wrong 
account, the error should be corrected by a full reversal of the original transact ion and not corrected as a 
subsequent PTF to put the [[shares]] in the correct account. Such action creates challenges for correctly moving 
cost basis. 
When processed as a full reversal, the correcting parties will reinstate the prior basis as if the transacti on did 
not occur, whereas a correction via PTF would result in the expectation of a cost basis record. Further details 


---

## Page 56

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 56 
on “Exception/Correction Processing” are contained in the Transfers Overview sub- section at the beginning of 
this chapter and in Special Considerations and Recommended Practices for [[Mutual Funds]] of this guide. 
 
3rd Party Mutual Fund Agent Processing 
Firms may leverage a 3rd Party Mutual Fund Agent (Agent) to clear/[[custody]] their mutual fund assets. In these 
situations, the firm is responsible for the tax reporting, including the cost basis reporting obligation, not the 
clearing agent. The originating firm initiates the ACATS PTF transfer through its third- party Agent, and the 
applicable ACATS FR record will identify the Agent’s firm number and account number.  
When a Mutual Fund Agent is associated with a transaction, the “Originating Delivering Firm Number” and 
“Originating Receiver Firm Number” fields (which correspond to the existing ACATS PTF/TI fields of the same 
name) should be populated in order to identify the party or underlying firm that is responsible for sending or 
receiving cost basis. When either of these fields is populated, the data identifies the firm (or contra-party) for 
the cost basis transfer reporting associated with the transaction. Otherwise, the transfer statement should be 
directed to the “Firm Number” on the ACATS or ACATS-Fund/SERV transaction. 
The Fund/SERV 018 record will identify the originating firm number and account number as well as the firm 
number and account number for the 3rd party agent. This enables the fund to complete cost basis transfer with 
the originating firm (as deliverer or receiver), while the [[Asset]] transaction continues with the 3rd party agent.  
 
Omnibus Processing and Underlying Firm Account Number (Fund to Firm “Pull”) 
Firm clients receiving assets from fund [[Companies]] should include the "Underlying Client Account Number" on 
the ACATS (TIF) Transfer Initiation Form record. [[NSCC]] will populate the "Originating Receiver Account 
Number at Firm" field on the ACATS-Fund/SERV Transfer Record (018) that is sent to the fund company.  
The fund should ensure the “Originating Receiver Account Number at Firm” is carried through to the ACATS 
Fund/SERV Transfer Acknowledgement/Rejection (019) and also to the corresponding CBRS Records for cost 
basis transfer. 
 
Transfer Control Number 
Fund [[Companies]] receive a 15 bytes alpha numeric control number on the ACATS Fund/SERV Transfer record 
(018). This number is returned on the ACATS Fund/SERV Transfer Acknowledgement/Rejection (019) record 
(Example: CATSA1234567890). The field is located in Position 45-59 (Variable) or Record 1, Position 41-55 
(Fixed) on the Fund/SERV 018 record. 
For firms, the Transfer Control Number is an 11-byte number, comprised of the last 11 characters of the 
ACATS Fund/SERV control number. (Example: A1234567890) The field is located in Position 153- 163 
(Variable) or Record 3, Position 8-18 (Fixed) of the ACATS Output Fund/SERV Statistics file (SIAC720-
variable, SIAC726-fixed). [[NSCC]] adds the letters ‘CATS’ to the ACATS Control Number to create the ACATS 
Fund/SERV Control Number, which is necessary due to differences in required field lengths for the respecti ve 
systems’ control numbers. 
The differences in Control Numbers must be managed in the context of CBRS. When a PTF “Pull” is processed 
the firm is receiving cost basis information. Firms should add “CATS” to the ACATS Fund/SERV Control 
Number on their expectancy record. When a PTF “Push” is processed the firm is delivering cost basis 
information. Firms should populate the ACATS Fund/SERV Control Number in the Transfer Control Number 
field on the [[Asset]] and Tax lot records to meet the CBRS requirements for populating the Transfer Control 
Number. The Transfer Control Number field is located in position 10-39 on the Cost Basis [[Asset]] and Tax Lot 
records. 
Industry Recommended Practice:  
Firms should use the ACATS Fund/SERV Control number from the ACATS Output Fund/SERV Statistics file and add the 
letters ‘CATS’ to the front of it, when building their expectancy files for Cost Basis [[Asset]] and Tax Lot Records. This will 
permit consistent matching with the CBRS requirements for the Transfer Control Number field of the CBRS records that will 

---

## Page 57

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 57 
be received. For Transaction types 46=Fund to Firm Mutual Fund Transfer or 51=Firm to Fund Mutual Fund Transfer the 
Alternate Control Number field on the [[Asset]] and Tax Lot records must be populated with the ACATS Control Number. 
 
Timing Considerations for CBRS Record Delivery 
When current CBRS workflows for the ACATS PTF process were reviewed, a timing gap was identified with 
respect to the delivery of tax lots from fund to firm. The timing issue occurs between when funds typically w ould 
send CBRS information, and when firms typically would be ready to receive it.  
When funds process an ACATS-Fund/SERV transfer, their systems are often prepared to send tax information 
on the business day following the posting of the transfer to the transfer agency system (T+1). Many brokerage 
systems, however, are not ready to receive cost basis records until after they have received notification that the 
transfer has been processed by the fund, and such updates have been committed to their systems (T+2).  
Because of the timing of when the notification through the ACATS Output Fund/SERV Statistics File is 
received, funds run the risk of sending cost basis information before firms can construct their cost basis 
transfer expectancy file. While some brokerage systems can compensate for this situation, others would either 
reject CBRS information as not matched to an expectancy file, or the firm would capture records received on 
reports for manual exception review and data entry. Both of these outcomes would result in significant 
processing inefficiencies and costly rework for cost basis transfer workflow, adversely impacting both firms and 
funds. 
Industry Recommended Practice:  
For ACATS PTF transfers, funds should make every effort to deliver CBRS data to the [[DTCC]] after 4:00 p.m. ET and before 
8:00 p.m. ET on the day following transfer processing (T+1). Delaying the delivery to this timeframe will eliminate the need 
for funds to change dates associated with the delivery of CBRS data on files, and delivery to firms will occur on T+2. This 
should allow sufficient time for firms to construct cost basis expectancy files to avoid timing-related rejects and manual 
processing of CBRS data. (Note: Most funds that provided input on the recommended industry practice will delay delivery of 
ALL CBRS data, and not just those that are ACATS PTF-related.) 
 
  

---

## Page 58

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 58 
Networking Transfers and CBRS 
Introduction 
Networking is the industry standard for account reconciliation and [[Dividend]] processing. Through Networking, all 
customer account-level information, either in an omnibus or non-omnibus environment, can be exchanged and 
reconciled between firms and fund [[Companies]], allowing identical information to appear on all parties’ records. 25 
Networking B50 (new account) and B52 (transfer) functionality may also be used to facilitate transfer 
processing between firms and funds, and to facilitate matching and reconciliation of cost basis data. This 
method, however, does not generally support all types of transfers or all types of accounts. Additional 
Networking fields also allow clients to communicate underlying sub-account information for transfers into or out 
of an omnibus account. Finally, a special Networking “mass [[Broker]]-to-[[Broker]]” process permits large quantities 
of firm-initiated transfers to move from one firm to another firm’s control. In some cases, such activity requires 
special systems permissions to be enabled prior to processing these types of transfers.  
Industry Recommended Practice:  
[[NSCC]]’s Networking service provides functionality that enables a Networking Maintenance B51 record to process a matrix 
level change on an account held at the fund. In some cases, the B51 Maintenance requested changes the control of the 
account and the tax reporting responsibility. Therefore, any networking maintenance change on an account that would 
change the existing tax reporting responsibility on mutual fund [[shares]] should be processed through a transfer transaction 
and not by utilizing the Networking Maintenance B51 record. 
This section provides an overview of the two networking transfer scenarios and related workflows and 
guidance on: 
• Both inbound and outbound considerations with regard to movement of cost basis information; and  
• Special considerations specifically related to networking transfers. 
Overview–Networking Transfers 
The scenarios below include a networking transfer moving [[shares]] from a fund to a firm, and also a “de-
networking” transfer moving [[shares]] from a firm to direct at fund. Detailed examples of networking transfers, 
including sample data populated on the related CBRS records, are included in the Examples sub- section at the 
end of this chapter. 
Please note the following flows [[DO]] not include mass [[Broker]] to [[Broker]] transfers or level 3 to level 3 transfers. 
Additionally, Matrix level changes between levels 3 and 4 for the same firm account where the tax reporting 
responsibility changes should be handled outside of this process using a method agreed upon by the firm and 
fund. For Matrix level 3 to 4 changes involving the same account, most fund systems restrict the number of 
accounts in which the same [[Broker]] Identification Number (BIN) can be assigned within the same Security 
Issue [[ID]]. As a result, the automated transfer through Networking fails. 
Note: 
In both networking scenarios, and as with all transfers, cost basis transfer statements are to be delivered within 15 calendar 
days from the transaction’s completion date. 
 
25 Additional details regarding networking transfers can be found in the Networking Technical  user guide available to [[NSCC]] members only on the Learning 
Center website under the Networking tab in Guides section at https://dtcclearning.com/products -and-services/mutual-fund-services/networking.html#resources 
 
  Those who are not members of [[NSCC]] but would be interested in knowing more about the Networking process should contact WMS Management Services at 
212-855-8877 or WMSConnect@[[DTCC]].com   

---

## Page 59

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 59 
Firm Initiated Networking Fund to Firm Transfer 
Situation: The submitting firm has established a new account by submitting a Networking Account Conversion 
Record B50 to the fund (networked) or to the sub accounting/omnibus provider (omnibus). The submitting firm 
then submits a B52 Networking transfer request to move the [[shares]] from a fund direct/level 0 (non- networked) 
account to the firm controlled networked or omnibus account. 
Preconditions:  
• Account exists at firm.  
• the Security is [[NSCC]] eligible.  
• Fund company and firm are participating in Networking. 
 
 


---

## Page 60

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 60 
Firm Initiated De-Networking Firm to Fund Transfer 
Situation: The submitting firm has established a new fund direct/level 0 (non-networked) account by submitting 
a Networking Account Conversion Record B50 to the fund (networked and omnibus). The submitting firm 
submits a Networking B52 transfer request to move the [[shares]] from the firm controlled networked or omnibus 
account, to the newly established direct/level 0 fund account. 
Preconditions:  
• Account exists at firm.  
• the Security is [[NSCC]] eligible.  
• Fund company and firm are participating in Networking. 
 


---

## Page 61

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 61 
Special Considerations for Networking 
Agent for Firm 
Originating or Introducing Firms may leverage a 3rd Party Mutual Fund Agent (Agent) to clear/[[custody]] their 
mutual fund assets. In these cases, the tax reporting, and therefore cost basis reporting obligation, is the 
responsibility of the introducing firm, not the 3rd Party Mutual Fund Agent. The introducing firm, if applicable, is 
typically defined in [[NSCC]] records as the “Agent for Firm.” 
Some Clearing Firms will define their introducing firms in the Agent for Firm field by using a unique 4-character 
value. Other Clearing Firms will define the value using the available [[NSCC]] Firm Number for their originating or 
introducing firms. Within Networking, there are no [[NSCC]]-defined values to specifically identify whether an 
Agent for Firm number is either the [[NSCC]] Firm Number for the introducing firm or a number that has been 
generated by the clearing firm. Therefore, with a Networking transfer (B52), the Agent for Firm field cannot be 
utilized for sending or receiving cost basis information for transfer reporting because it may not be a valid 
[[NSCC]] firm number. Thus, the Clearing/Settling Firm Number field will be used to identify the firm that should 
receive or send the cost basis information on a transfer statement. It will be the responsibility of Clearing Firms 
to direct transfer statements received to their introducing firms. 
Mass [[Broker]] to [[Broker]] Conversions 
Firms have the [[Option]] of using the Mass [[Broker]] to [[Broker]] Conversion feature in Networking to expedite bulk 
movement of accounts from one Firm to another as recorded on the fund [[transfer agent]] system. Mass [[Broker]] 
to [[Broker]] Conversions can be accomplished in an automated and controlled environment through the Account 
Set-Up/Update/Transfer and Acknowledgment function in Networking. Typically, the delivering firm initiates the 
transfer record (B52 with a Transaction Type 4). Due to timing of the passage of cost basis data systematically, 
the mass [[Broker]] to [[Broker]] process should be discussed between the parties as data can also be passed 
outside of the [[DTCC]] CBRS system if necessary. 
Both the delivering and receiving firms involved in a Mass [[Broker]] to [[Broker]] Conversion receive the same F53 
transfer acknowledgement record from the fund. Such information will be helpful for the receiving firm to create 
cost basis expectancy records. 
The Use of Networking and Cost Basis Expectancy 
Many Firms have created Cost Basis expectancy processes, which cross multiple trading platforms that 
interface with brokerage systems. Networking output provides much of the information that firms require to 
create cost basis expectancy records for both Networking and Manual mutual fund transfers.  
• Fund Transfer Acknowledgement Record (F53): This record is received by firms in response to a Firm 
Transfer Detail Record (B52) and provides the corresponding Control Number and related transaction 
details (account number(s), [[shares]] transferred, etc.), which will be used by the delivering party when 
generating CBRS records for the related transfer. In the case of Mass [[Broker]] to [[Broker]] Conversions, 
which are initiated by either the delivering or receiving firm, both parties will receive the same F53. This 
validates both parties have the key identifiers to effect the CBRS transfer movement. 
• F
und Activity Detail Record (F55) : This record is received by a firm in response to Manual Transfers 
(Networking Transaction Type 13) and Transfer Cancellations (Networking Transaction Types 33 and 34). 
Please refer to the sub-section on Manual Transfers in this chapter for details on the use of the F55 to 
effect the CBRS transfer movement. 
 
Exception/Correction Processing 
Following a Networking fund to firm or De-Networking firm to fund full or partial transfer, a fund or firm may 
need to cancel/correct the actual transfer transaction (e.g. to correct the number of [[shares]]). Any cancelation or 
correction to a previously posted transfer transaction must be reported to the firm. The Industry recommended 
practice is to cancel the original transfer transaction completely, and to submit a new transfer for the correct 
number of [[shares]], etc. No CBRS records are passed as a result of the cancel. If the original corresponding 
CBRS records have been sent, they should be voided by both parties and deleted from cost basis tracking 
systems. When the correction is processed new CBRS records for the new transfer transaction will be passed.  

---

## Page 62

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 62 
Industry Recommended Practice:  
Industry recommended practice when correcting a transfer transaction is to cancel the original transfer transaction and 
deliver a (to and from) transfer cancelation using the Networking F55 Activity record utilizing the appropriate Transfer 
Cancelation transaction types. 
The original transaction is then voided by both parties, any impact from previously exchanged CBRS records are deleted 
from both the delivering and receiving entities cost basis systems, and a subsequent new transfer transaction and related 
CBRS records are transmitted. 
This recommended practice applies to cancellations/corrections which affect all or a portion of the original transfer and 
related cost basis records. 
A firm may initiate a transfer cancelation/correction by submitting a letter of instruction to the fund. The letter 
should reference the original B52/F53 control number. Alternatively, a fund may determine a transfer needs to 
be corrected or canceled and initiate the cancelation/correction. In either case, the fund should generate a 
Networking F55 Activity record notifying the firm of the event. In addition to other required fields, the F55 
records should contain the following information: 
• Transaction Type 
o 33 = Transfer From – Cancellation (to cancel a ‘firm to fund’ transfer), or 
o 34 = Transfer To – Cancellation (to cancel a ‘fund to firm’ transfer) 
• Original Control Number Indicator value of 2 = Networking Control Number 
• Original Control Number = [[NSCC]] Control # from the original B52/F53 transfer  
 
When processing the new or correct transfer transaction, a new B52 transfer and corresponding CBRS records 
will be generated. The B52 will be assigned a new [[NSCC]] Original Control Number, and the new CBRS records 
passed will reference only the new [[NSCC]] Control Number. 
Further details on “Exception/Correction Processing” are contained in the Transfers Overview sub- section at 
the beginning of this chapter and in Section 3 (Special Considerations-Transfer Statement Corrections) of this 
guide. 
 
Manual Transfers and CBRS 
Introduction 
While progress has been made to eliminate manual transfers within the mutual fund industry, it remains a 
common practice for funds to manually process account transfers at the request of delivering/receiving firms. 
Requests for manual transfers are typically submitted by a firm to the fund in the form of an instruction or 
"transfer log." The transfer request will typically originate from an omnibus firm when [[shares]] are moving from a 
fund to a firm omnibus account. Transaction adjustments initiated by a fund company may also result in 
manual transfer transactions. 
Every effort should be made to transfer mutual fund [[securities]] using automated means in lieu of transferring 
[[shares]] manually. However, in the event a manual transfer must be processed, it is recommended that firms 
update their manual transfer instruction forms to include additional information, which is necessary to increase 
transparency, processing efficiency, and facilitate the transfer of cost basis information via CBRS. Use of the 
underlying customer account number (where applicable), a common control number on the transaction and the 
related CBRS records, and Mutual Fund Agent CBRS information will help recipients identify the transaction 
and accounts to which the CBRS records apply. The additional information provided permits automation of the 
expectancy and reconciliation processes for Cost Basis transfers. 

---

## Page 63

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 63 
Industry Recommended Practice:  
Firms should update their manual transfer instruction forms to include the following information: 
Underlying customer account number, when applicable. 
Either the original ACAT, Fund/SERV, or Networking control number or the manual transfer (fund/firm) generated control 
number (also known as “original control number”). 
Mutual Fund Agent CBRS information when utilizing a firm other than the share transfer recipient to track customer cost 
basis. 
Overview 
The three primary types of manual transfer scenarios addressed in this section include:  
1. A manual transfer moving [[shares]] from a fund to a firm, 
2. A manual transfer moving [[shares]] from a firm to a fund, and 
3. A manual transfer moving [[shares]] from one firm to another firm. 
 
The terms “Firm” or “[[intermediary]]” in the scenarios below represent transfers of [[Broker]]/Dealer (Level 3 or 
Omnibus) and Trust Networked (Level 0) accounts.  
 
 

---

## Page 64

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 64 
1. Manual Transfer – Fund to Firm 
Situation: An ACAT Fund/SERV PTF Pull or Networking B52 transaction has failed and cannot be 
completed systematically by the fund. The submitting firm sends a manual transfer log to the fund 
company to move [[shares]] from a fund-controlled account to a firm-controlled account. 
 


---

## Page 65

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 65 
2. Manual Transfer – Firm to Fund 
Situation: An ACAT Fund/SERV PTF Push or Networking B52 transaction has failed and cannot be 
completed systematically by the fund. The submitting firm sends a manual transfer log to the fund 
company to move [[shares]] from a firm-controlled account to a fund-controlled account. 
 
 


---

## Page 66

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 66 
3. Manual Transfers-Firm to Firm 
Situations: There are two Firm to Firm manual transfer scenarios depicted in the workflow which follows:  
 
a. Fails: An ACAT transfer or Networking B52 transfer has resulted in a fail. The delivering firm submits 
a manual transfer log to the fund company to move [[shares]] from a firm-controlled account to another 
firm-controlled account. 
b. Non-ACAT Transfers: One or more of the transferring firms is not an ACAT client and the transfer is 
processed outside of the ACATS system. Typically, the receiving firm establishes a (receiving) 
account at the fund and provides re-registration information to the delivering firm. Then the delivering 
firm sends a re-registration letter to the fund company to move [[shares]] from their firm-controlled 
account to the receiving firm (controlled) account that’s been established. 
 
For firm to firm ACAT failed items, the delivering firm most likely has already sent cost basis to the 
receiving firm. For failed Networking B52 transfers or non-ACAT firm to firm mutual fund manual transfers, 
the delivering firm should send cost basis when the fund company has confirmed [[shares]] have moved to 
the firm-controlled account via the Networking F55. The receiving firm should expect cost basis once the 
fund has confirmed that the [[shares]] have moved into the firm controlled receiving account via the 
Networking F55. 
The fund company will provide a control number on the F55, which is either the control number provided 
by the firm with the re-registration letter, or a fund generated manual transfer control number (also known 
as an original control number). The same control number should be utilized by both the delivering and 
receiving firm for populating and retrieving the related CBRS records. 

---

## Page 67

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 67 
 
 
 
 


---

## Page 68

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 68 
Special Considerations for Manual Transfers 
Control Numbers for Manual Transfers 
When a manual transfer is requested by a firm for a rejected Networking or ACATS -Fund/SERV transfer (which 
is referred to on the [[NSCC]] F55 Activity Record as transaction type 13 or a “Direct” transfer), the industry 
recommended practice is to provide the Control Number associated with the rejected transfer in the “Original 
Control Number” field on the F55 Activity Record. In addition, the “Original Control Number Indicator” field 
should be populated (on the F55 Activity Record) with the applicable indicator value (“1” for Fund/SERV 
Control Number or “2” for Networking Control Number). 
When the "Control/Reference Number Indicator" is populated on the [[NSCC]] F55 Activity Record with a “1” , 
[[NSCC]] will validate that the value supplied in the “Original Control Number” field follows the required format for 
a Fund/SERV control number. If the "Control/Reference Number Indicator" is populated with a value of “2” , 
[[NSCC]] will validate that the value supplied in the “Original Control Number” field follows the format for a 
Networking Control Number. If the supplied control number does not follow the appropriate format, the F55 
Activity record will be rejected. 
If a Control Number is not provided by the requesting firm, or for a manual (or direct) transfer, the fund should 
populate the F55 Activity Record with a fund “Originated Control Number” (the manual transfer (fund 
generated) control number) and the “Original Control Number Indicator” field should be updated with a value of 
”3” for the “Manual Reference Number.” The manual transfer (fund generated) control number will not be 
validated by [[NSCC]] when the Original Control Number Indicator is “3”. 
Industry Recommended Practice:  
When a control number is not provided by a firm as part of the manual (direct) transfer instructions, the Fund 
should generate and reference a Manual Transfer Control Number in the Original Control Number field that 
is created by using the following algorithm: 
Position Length Field Description Value 
1 1 Direct transfer indicator D 
2 4 [[NSCC]] [[Member]] number for the fund 9999 
6 1 Last digit of current posting year for the transfer transaction 9 
7 3 Posting date of the transfer transaction in Julian date format 999 
10 6 Unique number (random-generated, sequential) 999999 
 
This number should be provided as the Original Control Number on Record 4, Position 23-37 of the Networking F55 
record, plus as the Transfer Control Number for all related CBRS records. 
 
Utilizing the same control number on the transaction and the related CBRS records will help recipients identify 
the transaction and accounts to which the CBRS records apply. This permits automation of the expectancy and 
reconciliation processes for Cost Basis transfers. The transaction activity and subsequent CBRS information 
can easily be linked together to efficiently fulfill transfer statement reporting [[obligations]].  
 
ACAT PTF Transfer Ages to Reject 
It should be noted for firms that if an ACAT PTF Transfer Ages to Reject ([[NSCC]] Code 600), no cost basis 
should be expected or sent. If the next transfer request processed is done manually, the requirement to send 
or expect to receive basis should be treated as a separate or new event for that specific manual transfer.  

---

## Page 69

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 69 
Exception/Correction Processing 
Details on “Exception/Correction Processing” for manual transfers and other transfer types are contained in the 
Transfers Overview sub-section at the beginning of this chapter and in Section 3 (Special Considerations -
Transfer Statement Corrections) of this guide. 
 
Transfer Examples – CBRS [[Asset]] and Tax Lot Records 
This section provides examples that illustrate several scenarios that will trigger the exchange of cost basis data 
through CBRS. The examples below include shareholder transfers that involve Average Cost, FIFO, Gifted 
[[shares]], and Inherited [[shares]]. The examples also illustrate transfer transactions that originate from ACATS 
Fund/SERV PTF, Networking, and manual processing that result in a change in tax reporting responsibility 
(i.e., "fund to firm" or "firm to fund"). Cost basis information must be passed when  the tax reporting 
responsibility for an account changes as a result of a transfer. 
The cost basis data provided in the examples below include lot details for the "from" account, followed by data 
populated in the CBRS record layouts that will be systematically transmitted to the recipient’s account via 
CBRS. The examples also include the common fields from CBRS that must be populated, regardless of the 
transfer method. Additionally, specific fields that must be populated based on the transfer method are als o 
highlighted in the examples below. 
Information regarding exception/corrective processing is also included in this section. Specifically, the lot 
details and corresponding codes that should be used to cancel an original transfer transaction are summarized 
below. 
 
Examples 
Example A – Average Cost 
a. Common Fields for [[Asset]] & Tax Records 
b. ACATS Fund/SERV PTF Pull Specific Fields 
c. ACATS Fund/SERV PTF Push Specific Fields 
d. Networking Fund to Firm Specific Fields 
e. De-Networking Firm to Fund Specific Fields 
f. Manual Transfer Specific Fields 
 
Example B – Gifted [[shares]] for FIFO Account 
a. Common Fields for [[Asset]] & Tax Records 
b. ACATS Fund/SERV PTF Pull Specific Fields 
c. ACATS Fund/SERV PTF Push Specific Fields 
d. Networking Specific Fields 
e. Manual Transfer Specific Fields 
 
Example C – Inherited [[shares]] for FIFO Account 
a. Common Fields for [[Asset]] & Tax Records 
b. ACATS Fund/SERV PTF Pull Specific Fields 
c. ACATS Fund/SERV PTF Push Specific Fields 

---

## Page 70

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 70 
d. Networking Specific Fields 
e. Manual Transfer Specific Fields 
 
Exception/Correction Processing 
Average Cost 
Example A – Average Cost: On February 2, 2013, level 3 firm 9999 moves 500 [[shares]] from a direct at fund 
account at Fund Company 8819 (account number 1029384756) into its level 3 firm-controlled account 
(987654321). The transfer is not a gift. The security issue is identical on both sides. In addition to Fund/SERV 
and Networking, both 9999 and 8819 participate in CBRS. The shareholder’s cost basis (lot disposition) 
method is average cost and the revocation period (for choosing another method for existing [[shares]]) has 
ended. For the PTF Push (firm to fund) and the De-Networking (firm to fund) scenarios below, this 
transfer will move in the opposite direction – from a firm-controlled account to a fund-controlled 
account held within the same fund company. 
The detailed tax lots currently held by the shareholder at Fund Company 8819 that will be used in the 
subsequent scenarios are: 
Lot 
No. 
Transaction 
Type 
Acquisition 
Date 
Tax Lot 
[[shares]] 
Price 
Per 
Share 
(NAV) 
Purchase 
Cost 
Share 
Balance 
Share 
Type 
Account 
Cumulative 
Cost Basis 
Average 
Cost Per 
Share 
1 Purchase   6/1/2011 200.000 $5.27 $1,054.00 200.000 Non- 
Covered 
$1,054.00 $5.27 
2 Purchase 12/1/2011 100.000 $5.24 $524.00 300.000 Non- 
Covered 
$1,578.00 $5.26 
BEGINNING IN 2012, A SEPARATE AVERAGE COST PER SHARE IS CALCULATED FOR THE COVERED [[shares]] 
3 Purchase   12/1/2012 100.000 $5.26 $526.00 400.000 Covered $526.00 $5.26 
4 [[Dividend]] 12/31/2012  50.000 $5.08 $254.00 450.000 Covered $780.00 $5.20 
5 Purchase   2/1/2013 200.000 $5.11  $1,022.00 650.000 Covered  $1,802.50 $5.15 
 
The following tax lots are used, either fully or partially, to support the February 2, 2013 partial transfer out of 
500 [[shares]]. Only 50.000 [[shares]] are used from Lot 5 below: 
Lot No. Acquisition Date Tax Lot Quantity Price per Share Tax Lot Current Cost 
Basis 
Non-Covered/ 
Pending 
1    6/1/2011    200.000 $5.26           $1,052.00 01 
2  12/1/2011    100.000 $5.26              $526.00 01 
3  12/1/2012    100.000 $5.15              $515.00  
4  12/31/2012      50.000 $5.15              $257.00  
5    2/1/2013    200.000 $5.15           $1,030.00  
 

---

## Page 71

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 71 
As a result of the successful transfer transaction, which moves [[shares]] to Firm 9999, Fund Company 8819 
prepares a CBRS transfer statement and systematically generates a CBRS file that is sent to Firm 9999.  
Common Fields Populated on the CBRS Record Layouts 
The following details the common fields that need to be populated on the [[Asset]] Record and five Tax Lot 
Records required to be sent for this transfer example, regardless of the method of transfer (ACATS 
Fund/SERV PTF, Networking, or Manual). 
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Record Content 
Indicator 
01 Total Position Quantity 500,000 [[Asset]] Category MFNM 
Position Code L [[settlement]] Date of 
Transfer 
20130202 ISIN Country Code US 
[[Asset]] Description Name of 
Fund 
ISIN Security Issue [[ID]] 
([[CUSIP]]) 
Fund Security 
[[ID]] ([[CUSIP]]) 
Disposition Method 
Used 
05 
(Average Cost) 
 
Tax Lot Record: Includes the five separate tax lots related to the [[Asset]] Record  
FIELD NAME VALUE–TAX 
LOT 1 
VALUE–TAX 
LOT 2 
VALUE–TAX 
LOT 3 
VALUE–TAX 
LOT 4 
VALUE–TAX 
LOT 5 
Record Content Indicator 01 01 01 01 01 
ISIN Country Code US US US US US 
ISIN Security Issue [[ID]] 
([[CUSIP]]) 
Fund Security 
Issue [[ID]] ([[CUSIP]]) 
Fund Security 
Issue [[ID]] ([[CUSIP]]) 
Fund Security 
Issue [[ID]] ([[CUSIP]]) 
Fund Security 
Issue [[ID]] ([[CUSIP]]) 
Fund Security 
Issue [[ID]] ([[CUSIP]]) 
[[Asset]] Description Name of Fund Name of Fund Name of Fund Name of Fund Name of Fund 
Non-Covered/Pending 
Indicator 
01 01    
Tax Lot Quantity 200,0000 100,0000 100,0000 50,0000 50,0000 
Position Code L L L L L 
Acquisition Date of Tax 
Lot 
20110601 20111201 20121201 20121231 20130201 
Tax Lot Current Cost 1052,00 526,00 515,00 257,50 257,50 
 
ACATS Fund/SERV PTF Pull Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and five Tax Lot Records if the transfer was facilitated through A CATS 
Fund/SERV as a PTF Pull ([[shares]] moving from a fund controlled account to a firm controlled account).  
 
 
 

---

## Page 72

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 72 
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 46 Transfer Control 
Number 
Fund/SERV 
Control Number 
Alternate Control 
Number 
ACATS 
Control Number 
Submitting Firm 
Type 
NSCPRT Submitting Firm 
Customer Account 
Number 
1029384756 Receiving Firm 
Customer Account 
Number 
987654321 
Submitting Firm 
Number 
8819 Contra Firm Number 9999 Contra Firm Type DTCPRT 
 
Tax Lot Record: Includes the five separate tax lots related to the [[Asset]] Record  
FIELD NAME VALUE–TAX 
LOT 1 
VALUE–TAX LOT 
2 
VALUE–TAX  
LOT 3 
VALUE–TAX LOT 
4 
VALUE–TAX  
LOT 5 
Transaction 
Type 
46 46 46 46 46 
Transfer Control 
Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Alternate Control 
Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
Contra Firm 
Number 
9999 9999 9999 9999 9999 
Contra Firm 
Type 
DTCPRT DTCPRT DTCPRT DTCPRT DTCPRT 
Submitting Firm 
Number 
8819 8819 8819 8819 8819 
Submitting Firm 
Type 
NSCPRT NSCPRT NSCPRT NSCPRT NSCPRT 
Receiving Firm 
Customer 
Account Number 
987654321 987654321 987654321 987654321 987654321 
Submitting Firm 
Customer 
Account Number 
1029384756 1029384756 1029384756 1029384756 1029384756 
 
ACATS Fund/SERV PTF Push Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and five Tax Lot Records if the transfer was facilitated through ACATS 
Fund/SERV as a PTF Push ([[shares]] moving from a firm controlled account to a fund controlled account).  
 
 

---

## Page 73

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 73 
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 51 Transfer Control 
Number 
Fund/SERV 
Control Number 
Alternate Control 
Number 
ACATS 
Control Number 
Submitting Firm 
Type 
DTCPRT Submitting Firm 
Number 
9999 Receiving Firm 
Customer Account 
Number 
1029384756 
Submitting Firm 
Customer Account 
Number 
987654321 Contra Firm 
Number 
8819 Contra Firm Type NSCPRT 
 
 
Tax Lot Record: Includes the five separate tax lots related to the [[Asset]] Record 
FIELD NAME VALUE–TAX 
LOT 1 
VALUE–TAX LOT 
2 
VALUE–TAX  
LOT 3 
VALUE–TAX LOT 
4 
VALUE–TAX  
LOT 5 
Transaction 
Type 
51 51 51 51 51 
Transfer Control 
Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Alternate Control 
Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
Contra Firm 
Number 
8819 8819 8819 8819 8819 
Contra Firm 
Type 
NSCPRT NSCPRT NSCPRT NSCPRT NSCPRT 
Submitting Firm 
Number 
9999 9999 9999 9999 9999 
Submitting Firm 
Type 
DTCPRT DTCPRT DTCPRT DTCPRT DTCPRT 
Receiver 
Customer 
Account Number 
1029384756 1029384756 1029384756 1029384756 1029384756 
Deliverer 
Customer 
Account Number 
987654321 987654321 987654321 987654321 987654321 
 
  

---

## Page 74

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 74 
Networking Fund to Firm Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and five Tax Lot Records if the transfer was facilitated through Networking as a 
B52 fund to firm transfer ([[shares]] moving from a fund controlled account to a firm controlled account).  
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 56 Transfer Control 
Number 
Networking 
Control Number 
Alternate Control 
Number 
Blank 
Submitting Firm 
Type 
NSCPRT Submitting Firm 
Customer Account 
Number 
1029384756 Receiving Firm 
Customer Account 
Number 
987654321 
Submitting Firm 
Number 
8819 Contra Firm Number 9999 Contra Firm Type DTCPRT 
 
Tax Lot Record: Includes the five separate tax lots related to the [[Asset]] Record  
FIELD NAME VALUE–TAX  
LOT 1 
VALUE–TAX LOT 
2 
VALUE–TAX  
LOT 3 
VALUE–TAX LOT 
4 
VALUE–TAX  
LOT 5 
Transaction 
Type 
56 56 56 56 56 
Transfer Control 
Number 
Networking 
Control Number 
Networking 
Control Number 
Networking 
Control Number 
Networking 
Control Number 
Networking 
Control Number 
Alternate Control 
Number 
Blank 
 
Blank Blank Blank Blank 
Contra Firm 
Number 
9999 9999 9999 9999 9999 
Contra Firm 
Type 
DTCPRT DTCPRT DTCPRT DTCPRT DTCPRT 
Submitting Firm 
Number 
8819 8819 8819 8819 8819 
Submitting Firm 
Type 
NSCPRT NSCPRT NSCPRT NSCPRT NSCPRT 
Receiver 
Customer 
Account Number 
987654321 987654321 987654321 987654321 987654321 
Deliverer 
Customer 
Account Number 
1029384756 1029384756 1029384756 1029384756 1029384756 
 
 
 
 

---

## Page 75

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 75 
De-Networking Firm to Fund Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and five Tax Lot Records if the transfer was facilitated through Networking as a 
B52 firm to fund transfer ([[shares]] moving from a firm controlled account to a fund controlled account). 
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 56 Transfer Control 
Number 
Networking 
Control Number 
Alternate Control 
Number 
Blank 
Submitting Firm 
Type 
DTCPRT Submitting Firm 
Customer Account 
Number 
987654321 Receiving Firm 
Customer Account 
Number 
1029384756 
Submitting Firm 
Number 
9999 Contra Firm Number 8819 Contra Firm Type NSCPRT 
 
Tax Lot Record: Includes the five separate tax lots related to the [[Asset]] Record  
FIELD NAME VALUE–TAX 
LOT 1 
VALUE–TAX LOT 
2 
VALUE–TAX 
LOT 3 
VALUE–TAX LOT 
4 
VALUE–TAX 
LOT 5 
Transaction 
Type 
56 56 56 56 56 
Transfer Control 
Number 
Networking 
Control Number 
Networking 
Control Number 
Networking 
Control Number 
Networking 
Control Number 
Networking 
Control Number 
Alternate Control 
Number 
Blank Blank Blank Blank Blank 
Contra Firm 
Number 
8819 8819 8819 8819 8819 
Contra Firm 
Type 
NSCPRT NSCPRT NSCPRT NSCPRT NSCPRT 
Submitting Firm 
Number 
9999 9999 9999 9999 9999 
Submitting Firm 
Type 
DTCPRT DTCPRT DTCPRT DTCPRT DTCPRT 
Receiver 
Customer 
Account Number 
1029384756 1029384756 1029384756 1029384756 1029384756 
Deliverer 
Customer 
Account Number 
987654321 987654321 987654321 987654321 987654321 
 
 
 
 

---

## Page 76

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 76 
Manual Transfer Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and five Tax Lot Records in the case of the transfer being processed manually 
([[shares]] moving from a fund controlled account to a firm controlled account). 
Note: 
In most cases, the manual process is the result of a failed or rejected transfer originally passed through [[NSCC]] and is being 
handled manually as a service. The Industry recommended practice is to utilize the original control numbers from those 
transactions when processing these transactions manually so that the receiver can reconcile the CBRS records with the 
Networking F55 Activity. 
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 57 Transfer Control 
Number 
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number  
Alternate Control 
Number 
ACATS 
Control Number 
Submitting Firm 
Type 
NSCPRT Submitting Firm 
Customer Account 
Number 
1029384756 Receiving Firm 
Customer Account 
Number 
987654321 
Submitting Firm 
Number 
8819 Contra Firm Number 9999 Contra Firm Type DTCPRT 
 
Tax Lot Record: Includes the five separate tax lots related to the [[Asset]] Record  
FIELD NAME VALUE–TAX LOT 
1 
VALUE–TAX LOT 
2 
VALUE–TAX LOT 
3 
VALUE–TAX LOT 
4 
VALUE–TAX LOT 
5 
Transaction Type 57 57 57 57 57 
Transfer Control 
Number 
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number 
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number  
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number  
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number  
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number  
Alternate Control 
Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
Contra Firm 
Number 
9999 9999 9999 9999 9999 
Contra Firm Type DTCPRT DTCPRT DTCPRT DTCPRT DTCPRT 
Submitting Firm 
Number 
8819 8819 8819 8819 8819 
Submitting Firm 
Type 
NSCPRT NSCPRT NSCPRT NSCPRT NSCPRT 
Receiving Firm 
Customer 
Account Number 
987654321 987654321 987654321 987654321 987654321 

---

## Page 77

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 77 
FIELD NAME VALUE–TAX LOT 
1 
VALUE–TAX LOT 
2 
VALUE–TAX LOT 
3 
VALUE–TAX LOT 
4 
VALUE–TAX LOT 
5 
Submitting Firm 
Customer 
Account Number 
1029384756 1029384756 1029384756 1029384756 1029384756 
 
Gifted [[shares]] for FIFO Account 
Example B – Gift of [[shares]] Using FIFO: On February 2, 2013, a shareholder gifts 450 [[shares]] from a direct 
at fund account at Fund Company 8819 (account number 1029384756) into the recipient’s firm controlled 
account (987654321) at firm 9999. [[shares]] are not in physical form. 
The security issue is identical on both sides. Both accounts use CBRS. The shareholder’s cost basis (lot 
disposition) method is FIFO. The [[Dividend]] was reinvested. [[shares]] are priced at $5.32 on date of transfer.  
Note: 
For the PTF Push (firm to fund) scenario below, this transfer will move in the opposite direction-from a firm-controlled 
account to a fund-controlled account held within the same fund company. 
The detailed tax lots currently held by the shareholder at Fund Company 8819 that will be used in the 
subsequent scenarios are: 
Lot 
No. 
Transaction 
Type 
Acquisition 
Date 
Tax Lot 
[[shares]] 
Price Per Share 
(NAV) 
Purchase 
Cost 
Share 
Balance 
Share Type 
1 Purchase 6/1/2011 200.000 $5.27 $1,054.00 200.000 Non-Covered 
2 Purchase    12/1/2011 100.000 $5.24 $524.00 300.000 Non-Covered 
3 Purchase    12/1/2012 100.000 $5.26 $526.00 400.000 Covered 
4 [[Dividend]]  12/31/2012 50.000 $5.08 $254.00 450.000 Covered 
5 Purchase 2/1/2013 200.000 $5.11 $1,022.00 650.000 Covered 
 
The following tax lots are used to support the February 2, 2013 full transfer out of 450 [[shares]]:  
Lot No. Acquisition Date Tax Lot Quantity Price per Share Tax Lot Current Cost Non- Covered/ 
Pending 
1 6/1/2011    200.000 $5.27    $1,054.00 01 
2         12/1/2011    100.000 $5.24       $524.00 01 
3         12/1/2012    100.000 $5.26       $526.00  
4       12/31/2012      50.000 $5.08       $254.00  
 
As a result of the successful transfer transaction, which moves [[shares]] to the recipient’s account, Fund 
Company 8819 prepares a CBRS transfer statement and systematically transmits CBRS records to the 
recipient’s firm-controlled account, thereby fulfilling its transfer statement reporting requirement. It should be 

---

## Page 78

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 78 
noted that the cost basis will reflect the original purchase price of the covered [[shares]] and will look identical in 
both the “from” and “to” accounts. It is also assumed that the date of transfer equals the date of the gift.  
Common Fields Populated on the CBRS Record Layouts 
The following details the common fields that need to be populated on the [[Asset]] Record and four Tax Lot 
Records required to be sent for this transfer example, regardless of the method of transfer (ACATS 
Fund/SERV PTF, Networking, or Manual). The [[shares]] are priced at $5.32 on the date of transfer.  
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Record Content 
Indicator 
01 Total Position Quantity 450,0000 [[Asset]] Category MFNM 
Position Code L [[settlement]] Date of Transfer 20130202 ISIN Country Code US 
[[Asset]] Description Name of 
Fund 
ISIN Security Issue [[ID]] 
([[CUSIP]]) 
Fund Security [[ID]] 
([[CUSIP]]) 
Disposition Method 
Used 
01 (FIFO) 
 
Tax Lot Record: Includes the four separate tax lots related to the [[Asset]] Record  
FIELD NAME VALUE–TAX  
LOT 1 
VALUE–TAX  
LOT 2 
VALUE–TAX  
LOT 3 
VALUE–TAX  
LOT 4 
Record Content Indicator 01 01 01 01 
ISIN Country Code US US US US 
ISIN Security Issue [[ID]] 
([[CUSIP]]) 
Fund Security Issue 
[[ID]] ([[CUSIP]]) 
Fund Security Issue 
[[ID]] ([[CUSIP]]) 
Fund Security Issue 
[[ID]] ([[CUSIP]]) 
Fund Security Issue 
[[ID]] ([[CUSIP]]) 
[[Asset]] Description Name of Fund Name of Fund Name of Fund Name of Fund 
Non-Covered/Pending 
Indicator 
01 01   
Gifted or Inherited 
Indicator 
01 01 01 01 
Date of Gift 20130202 20130202 20130202 20130202 
Fair Market Value as of 
Date of Gift 
1064,00 532,00 532,00 266,00 
Tax Lot Quantity 200,0000 100,0000 100,0000 50,0000 
Position Code L L L L 
Acquisition Date of Tax 
Lot 
20110601 20111201 20121201 20121231 
Tax Lot Current Cost 1054,00 524,00 526,00 254,00 
 

---

## Page 79

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 79 
ACATS Fund/SERV PTF Pull Specific Fields 
Industry Required Practice:  
The receiving firm should never initiate a Gift Transfer using the ACATS PTF “Pull” process. If a (receiving) firm initiates a 
Gift Transfer using the ACATS PTF “Pull” process, the [[NSCC]] will reject the transaction. (See [[NSCC]] Importance Notice 
#a7256.) 
ACATS Fund/SERV PTF Push Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and four Tax Lot Records if the transfer was facilitated through ACATS 
Fund/SERV as a PTF Push ([[shares]] moving from a firm controlled account to a fund controlled account).  
 
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 51 Transfer Control 
Number 
Fund/SERV 
Control Number 
Alternate Control 
Number 
ACATS 
Control Number 
Submitting Firm 
Type 
DTCPRT Submitting Firm 
Number 
9999 Receiving Firm 
Customer Account 
Number 
1029384756 
Submitting Firm 
Customer Account 
Number 
987654321 Contra Firm 
Number 
8819 Contra Firm Type NSCPRT 
 
 
Tax Lot Record: Includes the four separate tax lots related to the [[Asset]] Record  
FIELD NAME VALUE–TAX  
LOT 1 
VALUE–TAX  
LOT 2 
VALUE–TAX  
LOT 3 
VALUE–TAX 
LOT 4 
Transaction Type 51 51 51 51 
Transfer Control 
Number 
Fund/SERV Control 
Number 
Fund/SERV Control 
Number 
Fund/SERV Control 
Number 
Fund/SERV Control 
Number 
Alternate Control 
Number 
ACATS Control 
Number 
ACATS Control 
Number 
ACATS Control 
Number 
ACATS Control 
Number 
Contra Firm Number 8819 8819 8819 8819 
Contra Firm Type NSCPRT NSCPRT NSCPRT NSCPRT 
Submitting Firm 
Number 
9999 9999 9999 9999 
Submitting Firm Type DTCPRT DTCPRT DTCPRT DTCPRT 
Receiving Firm 
Customer Account 
Number 
1029384756 1029384756 1029384756 1029384756 

---

## Page 80

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 80 
FIELD NAME VALUE–TAX  
LOT 1 
VALUE–TAX  
LOT 2 
VALUE–TAX  
LOT 3 
VALUE–TAX 
LOT 4 
Submitting Firm 
Customer Account 
Number 
987654321 987654321 987654321 987654321 
 
Networking Fund to Firm Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and four Tax Lot Records if the transfer was facilitated through Networking as a 
B52 transfer ([[shares]] moving from a fund controlled account to a firm controlled account).  
While Networking does not prohibit firms from ‘pulling’ gifted [[shares]] through a firm -to-fund transfer, the Task 
Force recommends that gift transactions should only be initiated by the delivering entity. This ensures that the 
gifted request is reviewed and processed in accordance with the fund’s policies and procedures for gifted 
[[shares]], and in good order, prior to the gifted share transfer. 
Industry Required Practice:  
Networking transfers should not be used to ‘pull’ [[shares]] for a transfer due to gift. Instead, the shareholder should contact 
the fund directly to execute the transfer. 
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 56 Transfer Control 
Number 
Networking 
Control Number 
Alternate Control 
Number 
Blank 
Submitting Firm 
Type 
NSCPRT Submitting Firm 
Customer Account 
Number 
1029384756 Receiving Firm 
Customer Account 
Number 
987654321 
Submitting Firm 
Number 
8819 Contra Firm Number 9999 Contra Firm Type DTCPRT 
 
Tax Lot Record: Includes the four separate tax lots related to the [[Asset]] Record  
FIELD NAME VALUE–TAX 
 LOT 1 
VALUE–TAX 
 LOT 2 
VALUE–TAX 
 LOT 3 
VALUE–TAX 
 LOT 4 
Transaction Type 56 56 56 56 
Transfer Control 
Number 
Networking Control 
Number 
Networking Control 
Number 
Networking Control 
Number 
Networking Control 
Number 
Alternate Control 
Number 
Blank Blank Blank Blank 
Contra Firm Number 9999 9999 9999 9999 
Contra Firm Type DTCPRT DTCPRT DTCPRT DTCPRT 
Submitting Firm 
Number 
8819 8819 8819 8819 

---

## Page 81

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 81 
FIELD NAME VALUE–TAX 
 LOT 1 
VALUE–TAX 
 LOT 2 
VALUE–TAX 
 LOT 3 
VALUE–TAX 
 LOT 4 
Submitting Firm Type NSCPRT NSCPRT NSCPRT NSCPRT 
Receiver Customer 
Account Number 
987654321 987654321 987654321 987654321 
Deliverer Customer 
Account Number 
1029384756 1029384756 1029384756 1029384756 
 
Manual Transfer Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and four Tax Lot Records in the case of the transfer being processed manually.  
Note: 
In most cases the manual process is the result of a failed or rejected transfer originally passed through [[NSCC]] and is being 
handled manually as a service. The Industry recommended practice is to utilize the original control numbers from those 
transactions when processing these transactions manually so that the receiver can reconcile the CBRS records with the 
Networking F55 Activity. 
 
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 57 Transfer Control 
Number 
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number 
Alternate Control 
Number 
ACATS 
Control Number 
Submitting Firm 
Type 
NSCPRT Submitting Firm 
Customer Account 
Number 
1029384756 Receiving Firm 
Customer Account 
Number 
987654321 
Submitting Firm 
Number 
8819 Contra Firm Number 9999 Contra Firm Type DTCPRT 
 
Tax Lot Record: Includes the four separate tax lots related to the [[Asset]] Record 
FIELD NAME VALUE–TAX  
LOT 1 
VALUE–TAX  
LOT 2 
VALUE–TAX  
LOT 3 
VALUE–TAX  
LOT 4 
Transaction Type 57 57 57 57 
Transfer Control 
Number 
Fund/SERV, 
Networking, or Fund 
Originated Control 
Number 
Fund/SERV, 
Networking, or Fund 
Originated Control 
Number 
Fund/SERV, 
Networking, or Fund 
Originated Control 
Number 
Fund/SERV, 
Networking, or Fund 
Originated Control 
Number 
Alternate Control 
Number 
Blank Blank Blank Blank 

---

## Page 82

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 82 
FIELD NAME VALUE–TAX  
LOT 1 
VALUE–TAX  
LOT 2 
VALUE–TAX  
LOT 3 
VALUE–TAX  
LOT 4 
Contra Firm 
Number 
9999 9999 9999 9999 
Contra Firm Type DTCPRT DTCPRT DTCPRT DTCPRT 
Submitting Firm 
Number 
8819 8819 8819 8819 
Submitting Firm 
Type 
NSCPRT NSCPRT NSCPRT NSCPRT 
Receiver 
Customer Account 
Number 
987654321 987654321 987654321 987654321 
Deliverer 
Customer Account 
Number 
1029384756 1029384756 1029384756 1029384756 
 
Inherited [[shares]] for FIFO Account 
Example C – Inherited [[shares]] Using FIFO: On February 15, 2013, a shareholder inherits all [[shares]] from a 
direct at fund account at Fund Company 8819 (account number 1029384756) that are transferred i nto their 
beneficiary account (987654321) at firm 9999. The donor’s date of death is February 2, 2013 and the [[shares]] 
are priced on the date of death at $5.32. [[shares]] are not in physical form. The security issue is identical on both 
sides. Both accounts use CBRS. The shareholder’s cost basis (lot disposition) method is FIFO.  
Note: 
For the PTF Push scenario below, this transfer will move in the opposite direction-from a firm-controlled account to a fund-
controlled account held within the same fund company. 
The detailed tax lots currently held by the shareholder at Fund Company 8819 that will be used in the 
subsequent scenarios are: 
Lot 
No. 
Transaction 
Type 
Acquisition 
Date 
Tax Lot 
[[shares]] 
Price Per Share 
(NAV) 
Purchase 
Cost 
Share 
Balance 
Share Type 
1 Purchase 6/1/2011 200.000 $5.27 $1,054.00 200.000 Non-Covered 
2 Purchase 12/1/2011 100.000 $5.24 $524.00 300.000 Non-Covered 
3 Purchase 12/1/2012 100.000 $5.26 $526.00 400.000 Covered 
4 [[Dividend]] 12/31/2012 50.000 $5.08 $254.00 450.000 Covered 
5 Purchase 2/1/2013 200.000 $5.11 $1,022.00 650.000 Covered 
  

---

## Page 83

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 83 
The following tax lots are used to support the February 2, 2013 full transfer out of 650 [[shares]]:  
Lot No. Acquisition 
Date 
Tax Lot 
Quantity 
Price per 
Share 
Tax Lot Current 
Cost 
Non-Covered/ 
Pending 
Fair Market Value as of 
Date of Death: 2/15/2013 
(NAV $5.32) 
1 6/1/2011 200.000 $5.27 $1,054.00 01 $1,064.00 
2 12/1/2011 100.000 $5.24 $524.00 01 $532.00 
3 12/1/2012 100.000 $5.26 $526.00  $532.00 
4 12/31/2012 50.000 $5.08 $254.00  $266.00 
5 2/1/2013 200,000 $5.11 $1,022.00  $1,064.00 
 
As a result of the successful transfer transaction, which moved [[shares]] to the recipient’s account, Fund 
Company 8819 prepares a CBRS transfer statement and systematically transmits the cost basis to the 
recipient’s account via CBRS. It should be noted that the cost basis presented above will be “stepped up” to 
reflect the Fair Market Value (FMV) of the [[shares]] on the date of death. Therefore, the acquisition date of the 
tax lots transferred will be the donor’s date of death. 
 
Common Fields Populated on the CBRS Record Layouts 
The following details the common fields that need to be populated on the [[Asset]] Record and five Tax Lot 
Records required to be sent for this transfer example regardless of the method of transfer (ACATS Fund/SERV 
PTF, Networking, or Manual). 
Note: 
In an inherited scenario, the acquisition date of the [[shares]] transferred is reflected as the original shareholder’s date of 
death. The tax lots are valued using the stepped-up basis, which is the FMV of the [[shares]] on February 2, 2013 (date of 
death) of $5.32. 
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Record Content 
Indicator 
01 Total Position Quantity 650,0000 [[Asset]] Category MFNM 
Position Code L [[settlement]] Date of 
Transfer 
20130202 ISIN Country Code US 
[[Asset]] Description Name of 
Fund 
ISIN Security Issue [[ID]] 
([[CUSIP]]) 
Fund Security 
Issue [[ID]] 
([[CUSIP]]) 
Disposition Method 
Used 
01 (FIFO) 
 
Tax Lot Record: Includes the five separate tax lots that fall under the [[Asset]] Record  
FIELD NAME VALUE–TAX 
LOT 1 
VALUE–TAX 
LOT 2 
VALUE–TAX 
LOT 3 
VALUE–TAX 
LOT 4 
VALUE–TAX 
LOT 5 
Record Content Indicator 01 01 01 01 01 
ISIN Country Code US US US US US 

---

## Page 84

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 84 
FIELD NAME VALUE–TAX 
LOT 1 
VALUE–TAX 
LOT 2 
VALUE–TAX 
LOT 3 
VALUE–TAX 
LOT 4 
VALUE–TAX 
LOT 5 
ISIN Security Issue [[ID]] 
([[CUSIP]]) 
Fund Security 
Issue [[ID]] 
Fund Security 
Issue [[ID]] 
Fund Security 
Issue [[ID]] 
Fund Security 
Issue [[ID]] 
Fund Security 
Issue [[ID]] 
[[Asset]] Description Name of Fund Name of Fund Name of Fund Name of Fund Name of Fund 
Non- Covered/Pending 
Indicator 
01 01    
Gifted or Inherited 
Indicator 
02 02 02 02 02 
Date of Gift Blank Blank Blank Blank Blank 
Fair Market Value as of 
Date of Gift 
Blank Blank Blank Blank Blank 
Tax Lot Quantity 200,0000 100,0000 100,0000 50,0000 200,0000 
Position Code L L L L L 
Acquisition Date of Tax 
Lot 
20130202 20130202 20130202 20130202 20130202 
Tax Lot Current Cost 1064,00 532,00 532,00 266,00 1064,00 
Zero Basis Indicator Blank Blank Blank Blank Blank 
 
ACATS Fund/SERV PTF Pull Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and five Tax Lot Records if the transfer was facilitated through ACATS 
Fund/SERV as a PTF Pull ([[shares]] moving from a fund controlled account to a firm controlled account).  
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 46 Transfer Control 
Number 
Fund/SERV 
Control Number 
Alternate Control 
Number 
ACATS 
Control Number 
Submitting Firm 
Type 
NSCPRT Submitting Firm 
Customer Account 
Number 
1029384756 Receiving Firm 
Customer Account 
Number 
987654321 
Submitting Firm 
Number 
8819 Contra Firm Number 9999 Contra Firm Type DTCPRT 
 
 
 
 
 

---

## Page 85

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 85 
Tax Lot Record: Includes the five separate tax lots related to the [[Asset]] Record  
FIELD NAME VALUE–TAX  
LOT 1 
VALUE–TAX LOT 
2 
VALUE–TAX 
 LOT 3 
VALUE–TAX LOT 
4 
VALUE–TAX 
 LOT 5 
Transaction 
Type 
46 46 46 46 46 
Transfer Control 
Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Alternate Control 
Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
Contra Firm 
Number 
9999 9999 9999 9999 9999 
Contra Firm 
Type 
DTCPRT DTCPRT DTCPRT DTCPRT DTCPRT 
Submitting Firm 
Number 
8819 8819 8819 8819 8819 
Submitting Firm 
Type 
NSCPRT NSCPRT NSCPRT NSCPRT NSCPRT 
Receiver 
Customer 
Account Number 
987654321 987654321 987654321 987654321 987654321 
Deliverer 
Customer 
Account Number 
1029384756 1029384756 1029384756 1029384756 1029384756 
 
ACATS Fund/SERV PTF Push Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and five Tax Lot Records if the transfer was facilitated through ACATS 
Fund/SERV as a PTF Push ([[shares]] moving from a firm controlled account to a fund controlled account).  
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 51 Transfer Control 
Number 
Fund/SERV 
Control 
Number 
Alternate Control 
Number 
ACATS 
Control Number 
Submitting Firm Type DTCPRT Submitting Firm 
Number 
9999 Receiving Firm 
Customer Account 
Number 
1029384756 
Submitting Firm 
Customer Account 
Number 
987654321 Contra Firm 
Number 
8819 Contra Firm Type NSCPRT 
 
 

---

## Page 86

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 86 
 
Tax Lot Record: Covers the five separate tax lots that fall under the [[Asset]] Record  
FIELD NAME VALUE–TAX  
LOT 1 
VALUE–TAX LOT 
2 
VALUE–TAX 
 LOT 3 
VALUE–TAX LOT 
4 
VALUE–TAX 
 LOT 5 
Transaction 
Type 
51 51 51 51 51 
Transfer Control 
Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Fund/SERV 
Control Number 
Alternate Control 
Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
ACATS 
Control Number 
Contra Firm 
Number 
8819 8819 8819 8819 8819 
Contra Firm 
Type 
NSCPRT NSCPRT NSCPRT NSCPRT NSCPRT 
Submitting Firm 
Number 
9999 9999 9999 9999 9999 
Submitting Firm 
Type 
DTCPRT DTCPRT DTCPRT DTCPRT DTCPRT 
Receiver 
Customer 
Account Number 
1029384756 1029384756 1029384756 1029384756 1029384756 
Deliverer 
Customer 
Account Number 
987654321 987654321 987654321 987654321 987654321 
 
Networking Fund to Firm Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and five Tax Lot Records if the transfer was facilitated through Networking as a 
B52 transfer ([[shares]] moving from a fund controlled account to a firm controlled account)  
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 46 Transfer Control 
Number 
Networking 
Control Number 
Alternate Control 
Number 
Blank 
Submitting Firm 
Type 
NSCPRT Deliverer Customer 
Account Number 
1029384756 Receiver Customer 
Account Number 
987654321 
Submitting Firm 
Number 
8819 Contra Firm Number 9999 Contra Firm Type DTCPRT 
 
 
 

---

## Page 87

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 87 
 
 
Tax Lot Record: Includes the five separate tax lots that fall under the [[Asset]] Record  
FIELD NAME VALUE–TAX  
LOT 1 
VALUE–TAX 
LOT 2 
VALUE–TAX 
 LOT 3 
VALUE–TAX 
LOT 4 
VALUE–TAX  
LOT 5 
Transaction Type 56 56 56 56 56 
Transfer Control 
Number 
Networking 
Control Number 
Networking 
Control Number 
Networking 
Control Number 
Networking 
Control Number 
Networking 
Control Number 
Alternate Control 
Number 
Blank Blank Blank Blank Blank 
Contra Firm 
Number 
9999 9999 9999 9999 9999 
Contra Firm Type DTCPRT DTCPRT DTCPRT DTCPRT DTCPRT 
Submitting Firm 
Number 
8819 8819 8819 8819 8819 
Submitting Firm 
Type 
NSCPRT NSCPRT NSCPRT NSCPRT NSCPRT 
Receiving Firm 
Customer Account 
Number 
987654321 987654321 987654321 987654321 987654321 
Submitting Firm 
Customer Account 
Number 
1029384756 1029384756 1029384756 1029384756 1029384756 
 
Manual Transfer Specific Fields 
In addition to the common fields noted above, the following details the specific fields that would need to be 
populated on the [[Asset]] Record and five Tax Lot Records in the case of the transfer being processed manually.  
Note: 
In most cases the manual process is the result of a failed or rejected transfer originally passed through [[NSCC]] and is being 
handled manually as a service. The Industry recommended practice is to utilize the original control numbers from those 
transactions when processing these transactions manually so that the receiver can reconcile the CBRS records with the 
Networking F55 Activity. 
[[Asset]] Record 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Transaction Type 57 Transfer Control 
Number 
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number 
Alternate Control 
Number 
Blank 
Submitting Firm 
Type 
NSCPRT Deliverer Customer 
Account Number 
1029384756 Receiver Customer 
Account Number 
987654321 

---

## Page 88

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 88 
FIELD NAME VALUE FIELD NAME VALUE FIELD NAME VALUE 
Submitting Firm 
Number 
8819 Contra Firm Number 9999 Contra Firm Type DTCPRT 
 
Tax Lot Record: Includes the five separate tax lots related to the [[Asset]] Record  
FIELD NAME VALUE–TAX LOT 
1 
VALUE–TAX LOT 
2 
VALUE–TAX LOT 
3 
VALUE–TAX LOT 
4 
VALUE–TAX LOT 
5 
Transaction Type 57 57 57 57 57 
Transfer Control 
Number 
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number 
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number 
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number 
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number 
Fund/SERV, 
Networking, or 
Fund Originated 
Control Number 
Alternate Control 
Number 
Blank Blank Blank Blank Blank 
Contra Firm 
Number 
9999 9999 9999 9999 9999 
Contra Firm Type DTCPRT DTCPRT DTCPRT DTCPRT DTCPRT 
Submitting Firm 
Number 
8819 8819 8819 8819 8819 
Submitting Firm 
Type 
NSCPRT NSCPRT NSCPRT NSCPRT NSCPRT 
Receiving Firm 
Customer Account 
Number 
987654321 987654321 987654321 987654321 987654321 
Submitting Firm 
Customer Account 
Number 
1029384756 1029384756 1029384756 1029384756 1029384756 
Exception/Correction Processing  
Industry Recommended Practice:  
Industry recommended practice when correcting a transfer transaction is to cancel the original transfer transaction and 
deliver a (to and from) transfer cancelation using the Networking F55 Activity record utilizing the appropriate Transfer 
Cancelation transaction types. 
The original transaction is then voided by both parties, any impact from previously exchanged CBRS records are deleted 
from both the delivering and receiving entities cost basis systems, and a subsequent new transfer transaction and related 
CBRS records are transmitted. 
This recommended practice applies to cancellations/corrections that affect all or a portion of the original transfer and 
related cost basis records. 
This recommended practice applies to cancelations or adjustments of all transfer types  – ACATS Fund/SERV 
PTF Pull and PTF Push, Networking and De-Networking, and manual transfers. Please refer to “[[DTCC]] 
Enhancements for Cost Basis Reporting” in this guide for further details on exception/correction processing. 
The two new transaction types that may be utilized to represent this activity on the F55 are:  

---

## Page 89

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 89 
• 33 = Transfer From–Cancellation 
• 34 = Transfer To–Cancellation 

---

## Page 90

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Transfers of Mutual Fund [[securities]] 90 
Example D – Exception/Correction Processing: The detailed tax lots currently held by the shareholder at Fund Company or Firm are as follows:  
Lot 
No. 
Transaction 
Type 
Acquisition 
Date 
[[NSCC]] Control 
Number 
Tax Lot 
[[shares]] 
Price Per 
Share 
(NAV) 
Purchase 
Cost 
Current 
Cost Basis 
Share 
Balance 
Share Type Account 
Cumulative 
Cost Basis 
Average Cost 
per Share 
1 Purchase 6/1/2011  200.000 $5.27 $1,054.00 200.000 Non-Covered $1,054.00 $5.27 
2 Purchase 12/1/2011  100.000 $5.24 $524.00 300.000 Non-Covered $1,578.00 $5.26 
BEGINNING IN 2012, A SEPARATE AVERAGE COST PER SHARE IS CALCULATED FOR THE COVERED [[shares]] 
3 Purchase 12/1/2012  100.000 $5.26 $526.00 400.000 Covered $526.00 $5.26 
4 [[Dividend]] 12/31/2012  50.000 $5.08 $254.00 450.000 Covered $780.00 $5.20 
5 Purchase 2/1/2013  200.000 $5.11 $1,022.00 650.000 Covered $1,802.50 $5.15 
7 Transfer Out 
to Firm 9999 
2/3/2013 CATSA1234567890 ALL       
8 Transfer 
Cancel 
5/5/2013 123456789123456 ALL       
 
On 5/5/2013, the fund received instructions that the full transfer processed on 2/3/2013 was for an incorrect amount.  
The fund manually processes a transfer cancellation on their system canceling both sides of the original transfer. As a result, the system generates an 
F55 Networking Activity record, reflecting the cancel, to the firm. The F55 transaction type ‘34’ represents the “to” side since the original transfer went 
“from” the fund “to” the firm. The recommended practice is to include the Original Control Number Indicator of 1=Fund/SERV Control Number and 
Original Control Number CATSA1234567890 of the transfer on the F55 record.  
No cost basis is passed as a result of the cancel. Upon receipt of the F55 Networking Activity record, the firm will remove the Cost Basis tax lots  
associated with the original transfer. It is expected that a new transfer will be submitted where new basis records will foll ow. 
 

---

## Page 91

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Frequently Asked Questions: Transfer Reporting 91 
FREQUENTLY ASKED QUESTIONS: TRANSFER 
REPORTING 
1. How [[DO]] fund [[Companies]] support firm-initiated redemptions and related tax reporting on fund-
controlled matrix Levels 0 and 4 accounts? 
It is recommended that the Fund, which acts as the primary record keeper for cost basis reporting purposes on 
fund-controlled matrix Levels 0 and 4 accounts, be responsible for all 1099-B reporting on [[Broker]]-initiated 
redemption activity. This was a change from the recommended practice whereby the party executing the 
redemption on these accounts also assumed the corresponding tax reporting for that specific redemption.  
The primary reason for this change in practice was due to the impracticalities of retaining the former 
recommended practice. Because the cost basis reporting must accompany gross proceeds reporting, retaining 
the former recommended practice would require coordinated and/or dual tax lot tracking by firms and funds. 
Extensive and costly enhancements would be required for Fund/SERV
® identification of specific lot 
transactions, which given the low volumes of these types of transactions, is not warranted or supported by 
industry clients. 
As a result of this change, some fund [[Companies]], and many [[Broker]]/dealers, no longer allow these transactions 
as of January 1, 2012. However, [[Broker]]/dealers may initiate redemption activity against a fund- controlled 
account. Cost Basis lot depletion will be driven by the shareholder’s elected calculation method on the fund 
account, or in the absence of an affirmative election, the fund’s [[default]] cost basis calculation method. Funds 
will report the gross proceeds and corresponding cost basis information for such transactions.  
The white paper entitled, “Firm-Initiated Fund/SERV
® Redemptions on Fund-Controlled Accounts” is provided 
in Appendix B of this document. The white paper provides detailed information on the basis for this 
recommended practice and identifies areas where reporting brokers should review and remediate operational 
and legal arrangements that may be impacted by implementing the recommended pr actice. [[Broker]]/Dealers 
and fund [[Companies]] are encouraged to confirm each other’s preferred policies, prior to January  1, 2012. 
2. How [[DO]] I know if an entity is participating in CBRS? 
[[DTCC]] CBRS clients are identified on the daily Cost Basis User Master File. The Cost Basis User Master File 
can be received electronically on a daily basis. For further details, please refer to the Master File record layouts 
available at https://dtcclearning.com/products-and-services/equities-clearing/cbrs/cbrs-technical-resources.html 
on the [[DTCC]] Learning site. Please note that clients may appear under their brokerage name or under their 
clearing firm’s name. 
3. How should firms and [[Mutual Funds]] adjust for an unfulfilled Letter of Intent (LOI) or CDSC Fee 
Reversal when an account is to be transferred? 
The recommended practice is to cancel and rebook the original trade(s) at the adjusted price per share before 
an account is transferred. Such action is needed to make sure basis at the tax lot level is calculated properly, 
which is critical for accurate basis reporting. Reporting brokers should be aware this course of action could 
trigger corrected 1099-B reporting, if applicable. 
4. When transferring an account in which a redemption or sale has occurred and the average cost 
basis method was used, does the delivering [[Broker]] need to communicate this fact to the receiving 
[[Broker]]? 
Reporting that the average cost basis method was used is not necessary. However, if a sale has occurred, the 
transfer statement should list each lot separately with their associated acquisition dates, and the adjusted cost 
basis for each lot should reflect the average cost of the position. Tax lots under the average cost method that 
are held for more than five years may be rolled up into a single tax lot with an acquisition date of “VARIOUS”. 
This is noted in the CBRS layouts through use of the Acquisition Date of ‘19010101.’  
5. When transferring an account to a new position at another [[Broker]] with an identical or like account 
registration in which the average cost method has been used and a redemption or sale has NOT 
occurred, what lot data should be sent to the delivering [[Broker]]? 

---

## Page 92

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Frequently Asked Questions: Transfer Reporting 92 
If the shareholder has affirmatively elected average cost and is still within the revocation period, or has chosen 
a method other than the [[Broker]]’s [[default]] of average cost and is still within the “change in method” period 26, 
there are differing views in the industry as to whether a transfer of like or identical registration between 
reporting brokers constitutes a “disposition of [[shares]]” as defined in the IRS regulations. Many believe that this 
scenario is not a disposition of [[shares]] and thus the change in reporting [[Broker]] does not end the revocation or 
“change in method” period. Therefore, the transfer statement may include the adjusted cost basis for each 
individual share lot. Passing individual lot data versus average cost provides the greatest degree of flexibility to 
the shareholder in declaring a basis method for future redemptions in the new account.  
Others view these types of transfers as a “disposition of [[shares]],” which would require the delivering [[Broker]] to 
value all covered [[shares]] at the average cost on the date of disposition upon transfer to the new reporting 
[[Broker]]. Because of these differing views, reporting brokers should consult with their legal and compliance 
advisors to determine what should be reported for these types of transfers. Special considerations for average 
cost and the impact on transfers are discussed more fully in the Average Cost Considerations for Transfers 
section of this guide. 
6. How does a Return of Capital or other corporate action event affect transfer statements previo usly 
sent? 
Delivering reporting brokers are required to provide receiving reporting brokers with corrected transfer 
statements for covered [[securities]] accounting for any corporate action events that are announced after the 
transfer but are effective as of a date the [[shares]] were on the delivering reporting [[Broker]]’s books. If such [[shares]] 
have been transferred after the corporate action, but before the account’s [[shares]] were adjusted, a corrected 
transfer reporting statement with adjusted cost basis information must be sent to the receiving reporting [[Broker]]. 
Please refer to Question 9 below for additional details on corrected transfer reporting requirements.  
7. What is the recommended practice for recording corrected tax lots on [[shares]] previously 
transferred through CBRS that have been impacted by a Return of Capital? 
Once the delivering reporting [[Broker]] has completed the correction described in Question 6, corrected CBRS 
lots must be sent. Since the CBRS [[Asset]] Record must equal the CBRS Tax Lot Record, all of the lots will be 
resent on the corrected transfer records. Each lot bears a designation whether it is comprised of original or 
corrected data. Affected lots should be updated for the Return of Capital adjustment where applicable. The 
CBRS record does not note the specific reason why the tax lot has been corrected because it is not required to 
be noted on a transfer reporting statement. Please refer to Question 9 below for additional details on corrected 
transfer reporting requirements. 
8. If a co-owner of a joint account dies, is the account considered inherited? Does an adjustment 
need to occur to step up the basis for the joint ownership portion of the account, or is the joint 
owner removed from the account as a right of survivorship? 
The answer to this question will depend on state law and the type of joint account, both subject to the legal 
interpretation of the reporting [[Broker]]. The regulations [[DO]] state that if the transferor cannot identify which 
[[securities]] in a joint account have been transferred from the decedent, then the transferor must treat each 
security in the account as if it were non-covered. 
9. What happens if a reporting [[Broker]] doesn’t send a transfer reporting statement with cost basis 
information for a taxable account? 
On taxable accounts, a transferor must furnish a transfer statement within fifteen (15) days after the date of 
[[settlement]] of the transfer of the covered [[shares]]. If a transfer statement is not received within 15 days, the 
receiving reporting [[Broker]] must notify the transferor that it did not receive a transfer statement and request that 
such a statement be sent. If no transfer statement is provided after this request, the regulations permit the 
receiving reporting [[Broker]] to treat the [[shares]] as “non-covered” on their records and for 1099-B reporting 
purposes. 
 
26 Pursuant to Notice 2011- 56, the IRS now permits shareholders to choose a method other than the [[Broker]]’s [[default]] of average cost for existing [[shares]] i n an 
account, until the earlier of (1) one year from the [[Broker]]’s notification that average cost is its [[default]] method, or (2) the first sale, transfer or other disposition of 
[[shares]] (the “change in method” period). 

---

## Page 93

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Frequently Asked Questions: Transfer Reporting 93 
The regulations provide that brokers and transferors must correct their Form 1099 -B and/or transfer statements 
to account for late or corrected transfer statements or [[issuer]] reports. Thus, if the delivering reporting [[Broker]] 
later provides the basis information within eighteen (18) months of the [[settlement]] date, the receiving reporting 
[[Broker]] must accept it and adjust the basis of the [[shares]] accordingly. If the receiving [[Broker]] no longer holds the 
[[shares]], due to subsequent transfer to another reporting [[Broker]], such updated basis information will require the 
receiving [[Broker]]–in their role as delivering [[Broker]] in the subsequent transfer–to send a corrected transfer 
statement to the receiving [[Broker]] for the subsequent transfer. If the [[shares]] have already been disposed of, the 
receiving reporting [[Broker]](s) must send a corrected Form 1099-B, subject to the three (3) year limitation on 
Form 1099-B corrections. 
10. If a transfer reporting statement is not received from the delivering reporting [[Broker]], who can the 
receiving reporting [[Broker]] contact through CBRS regarding the missing transfer reporting 
statement? 
Delivering reporting brokers have up to 15 calendar days to deliver their transfer statement to the receiving 
reporting [[Broker]]. If the delivering reporting [[Broker]] that fails to send the transfer statement is enrolled in CBRS, 
the receiving reporting [[Broker]] will be able to [[Locate]] them on the Cost Basis User Master File (a daily file 
including details on all firms enrolled in the service). CBRS has the ability for a receiving reporting [[Broker]] to 
request a transfer statement of the delivering reporting [[Broker]], referencing the specific transaction.  
If one firm uses CBRS, and the other does not, then a follow-up request for a transfer reporting statement must 
be handled manually (outside of CBRS). 
 
11. How will a firm convey that transferred [[shares]] were gifted or inherited [[shares]] on CBRS transfer 
reporting record layouts? 
For firms using CBRS, there is an “indicator” field that can be populated to show whether a tax lot is gifted, 
inherited, or inherited, then gifted. For firms not using CBRS, the presentment of the information will differ 
depending on the format of the manual transfer statement. 
12. When an original acquisition date is not available on a lot being transferred, what date should be 
provided for the lot? 
Covered tax lots, in the context of [[Mutual Funds]], will always have an acquisition date and cost basis, so this 
situation will only occur for non-covered tax lots. If a transfer statement with covered tax lots does not include 
acquisition dates on those tax lot(s), the transfer statement will be rejected by CBRS as an “incomplete” 
transfer statement. 
CBRS does support the delivery of transfer statements including non-covered [[shares]] with a ‘blank’ acquisition 
date. The recommended practice is not to reject transfer statements where original acquisition dates are ‘blank’ 
or not provided on non-covered tax lots. Such lots will typically have a zero (“0”) or unknown cost basis. 
Because the IRS requires that, absent shareholder instructions, all non-covered [[shares]] with unknown 
acquisition dates should be removed from an account first, it is important to clearly distinguish between truly 
unknown acquisition dates on non-covered [[shares]] versus non-covered [[shares]] with known acquisition dates. 
Industry Recommended Practice:  
Delivering reporting brokers should send all “known” basis information, even on non-covered [[shares]], to the receiving 
reporting [[Broker]]. 
In many instances, brokers are providing all known basis information to their shareholders, even on non- 
covered [[shares]], as a customer service. While basis information on non-covered [[shares]] is not required to be 
provided by the reporting [[Broker]] to the IRS, the shareholder may be using basis information voluntarily 
provided by the reporting [[Broker]] to accurately compute their gain or loss on Schedule D of their tax return. In 
all cases, reporting brokers should ensure they are only providing basis information on non- covered [[shares]] for 
which they have no reason to believe the basis is incorrect. 
It is recommended that if the delivering reporting [[Broker]] has voluntarily reported non- covered “known” basis 
information to the shareholder under Average Cost when [[shares]] are transferred the Average Cost basis sho uld 
also be reported to the receiving [[Broker]]. This practice will allow known basis on non- covered [[shares]] to 
continue to be consistently reported voluntarily to the shareholder using the average cost method.  

---

## Page 94

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Frequently Asked Questions: Transfer Reporting 94 
13. What is the recommended practice for transferring gifted mutual fund [[shares]]? 
Gifted share transfer statements require that the cost basis information transferred include both the fair market 
value on the date of the gift, and the carryover basis on the applicable tax lots. The CBRS record layouts allow 
clients to transfer the required information in these situations. 
There are special considerations for transferring gifted [[shares]]. For instance, average cost cannot be used if the 
[[shares]] are gifted at a loss. For gifted [[shares]] in this situation to be valued at average cost by the receiving 
reporting [[Broker]], an authorized individual associated with the account receiving the gifted [[shares]] must indicate, 
prior to or at transfer, that they will accept the fair market value—and not the donee’s carryover basis  for the 
[[shares]] in question. 
The IRS regulations governing transfer statements require that all transfers should be reported as gifts if the 
reason for the transfer is not clear. 
Operationally, the Task Force recommended that transfers due to gifts are never ‘ pulled’ from the delivering to 
the receiving firm. Instead, the shareholder is directed to the delivering firm to request the transfer due to gift. 
While ACATS PTF “Pull” does not permit this capability (the [[NSCC]] will reject the transaction), Networking does 
not prohibit a receiving firm from pulling gifted [[shares]]. 
 
14. Who is responsible for tracking and reporting cost basis information on [[NSCC]] Matrix Level 3 and 
Trust Networked Level 0 accounts? 
Firms ([[Broker]]/dealers) are responsible for tax reporting on Matrix Level 3 accounts and Bank Trusts are 
responsible for tax reporting on Trust Networked Level 0 accounts, per [[NSCC]]’s rules governing the [[NSCC]] 
Networking account matrix levels. The Firm or Trust is also responsible for tracking and administering cost 
basis reporting on behalf of their customers. 
 
15. Are reporting brokers permitted to accept shareowner provided basis information on covered 
[[shares]], including [[shares]] transferred to a new firm? 
Reporting brokers are permitted, but not required, to take into account customer requests for changes to cost 
basis on covered [[securities]] unless they know or have reason to know that the customer -provided information is 
incorrect. Firms should evaluate shareholder requests to change cost basis information on covered [[shares]] on  
a case-by-case basis, including the origin of the customer-provided data. 
In addition, delivering reporting brokers may also transfer customer-provided basis information for covered 
[[shares]] on CBRS tax lots (which will be flagged as such). The cost basis regulations require that unless the 
[[Broker]] knows or has reason to know that the information reported by the delivering reporting [[Broker]] is incorrect 
or incomplete, it must accept the basis information that is supplied on the transfer statement.  
 
16. What procedures and system controls does the Fund have in place for Networking level account 
changes, or Networking dealer changes on [[Broker]]-controlled accounts? 
Both of these types of changes affect who is responsible for cost basis tracking/reporting. The recommended 
practice for accounts changing networking levels (which move to/from direct-at-fund administration or [[Broker]]-
to-[[Broker]]) is to create a Networking B50 new account with the appropriate matrix level and to execute a 
Networking B52 transfer. Cost basis information can be submitted through CBRS as a result of the transaction.  
Recommended industry practice is for funds to not accept Networking B51 maintenance records that attempt to 
change networking matrix level/tax reporting responsibility between fund and firm control . Funds and their 
service providers should either reject the Networking B51 maintenance to matrix level change or convert the 
Networking B51 matrix level change request into a Networking-like new account and transfer transaction. 
Change of dealer functions through Networking requires the contra-parties to the transfer of the [[Broker]]-
controlled positions (Matrix Level 3 and Trust-Networked Level 0) to transfer the cost basis information for 
affected shareholders as a result of such transactions. This cost basis transfer reporting can be facilitated 
through CBRS. Changes of dealers that remain fund-controlled positions (Matrix Level 4 and non-networked 
Level 0 accounts) have no cost basis transfer reporting impact. 

---

## Page 95

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Frequently Asked Questions: Transfer Reporting 95 
 
17. How does a firm or fund receive cost basis data for a manual transfer? 
Utilization of CBRS is an industry recommended practice that ensures the seamless and timely transfer of cost 
basis information to receiving reporting brokers. CBRS has provisions for identifiers related to manual transfers 
(such as a mutual fund transfer that happens outside of ACATS-Fund/SERV or Networking), to facilitate an 
automated exchange of cost basis information for these transaction types. Please refer to [[DTCC]]’s CBRS User 
Guide and the Manual Transfers discussion in the Transfers section of this Supplemental User Guide for 
additional details. 
Reporting brokers must be prepared to accept completed manual transfer statements provided by a transferor. 
But there are many challenges with manual statements, including whether the delivering reporting [[Broker]] can 
correctly identify who to send the transfer statement to at a receiving reporting [[Broker]], and whether the 
receiving reporting [[Broker]] has procedures to redirect transfer statements that have been sent to i ncorrect 
locations. Manual delivery of the applicable information will be costly to input into basis reporting systems, and 
in many cases, will significantly delay the availability of cost basis information for receiving reporting brokers.  
However, through its “MyDTCC web portal” service, [[DTCC]] offers a product whereby manual transfer reporting 
of cost basis information may also be processed through CBRS. The cost basis transfer statement information 
can be manually input or uploaded into CBRS through a standardized layout and systematically transferred to 
receiving reporting brokers or received from a delivering reporting [[Broker]] in a download to Microsoft Excel™ 
format. MyDTCC web portal input and output has no impact on how CBRS routes and reports informati on to 
contra-parties; the contra-party can either use a transmission-based (automated computer-to-computer) 
connection, or MyDTCC web portal. 
Please visit https://dtcclearning.com/products-and-services/equities-clearing/cbrs.html for more details on the 
MyDTCC service for automating manual transfers of cost basis information. 

---

## Page 96

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix A: Resource Reference Materials 96 
APPENDIX A: RESOURCE REFERENCE MATERIALS 
A1 Internal Revenue Code & IRS Information 
For further information, please refer to the following articles on the following topics: 
Section 1012-Basis of Property-Cost - https://www.law.cornell.edu/uscode/text/26/6045 
Section 6045–Returns of Brokers - https://www.law.cornell.edu/uscode/text/26/6045A 
Section 6045A–Information Required in Connection with Transfers of Covered [[securities]] to Brokers - 
https://www.law.cornell.edu/uscode/text/26/6045A 
Section 6045B–Returns Relating to Actions Affecting Basis of Specified [[securities]] – 
https://www.govinfo.gov/app/details/USCODE-2015-title26/USCODE-2015-title26-subtitleF-chap61-subchapA-
partIII-subpartB-sec6045B 
IRS Notice 2011-56–Guidance on Average Cost [[default]] Method & Other Cost Basis Reporting Issues  (with a 
hyperlink to http://www.irs.gov/pub/irs-drop/n-11-56.pdf 
A2 IRS Forms 
Form 1099-B 
Form 1099-B Instructions 
Form W-9 
Form W-9 Instructions 
A3 White Paper 
The ICI BDAC CBR Task Force has developed a white paper that contains recommended practices for firm- 
initiated Fund/SERV® redemptions on fund-controlled accounts. See Appendix B for BEST PRACTICES: Firm-
Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts. 
A4 Information on [[DTCC]]’s Cost Basis Reporting Service (CBRS) 
Detailed information on CBRS may be found on [[DTCC]]’s Learning site at: https://dtcclearning.com/products -
and-services/equities-clearing/cbrs.html 

---

## Page 97

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix B: White Paper – Recommended Practices for Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts 97 
APPENDIX B: WHITE PAPER – RECOMMENDED 
PRACTICES FOR FIRM-INITIATED FUND/SERV® 
REDEMPTIONS ON FUND-CONTROLLED ACCOUNTS 
B1 ICI White Paper 
This section contains a facsimile of the white paper produced by the Investment Company Institute (ICI), 
authored by the ICI [[Broker]]/Dealer Advisory Committee Cost Basis Reporting task force and published on 
June 30, 2010. 
Disclaimer 
This Best Practices Guide (this “Guide”) was produced by the Investment Company Institute, through a Task 
Force of its [[Broker]]/Dealer Advisory Committee and is reproduced here with the permission of the Depository 
Trust & Clearing Corporation (“[[DTCC]]”). 
This Guide is not a legal document and the statements contained herein [[DO]] not set forth any legal [[obligations]] 
of [[DTCC]], National [[securities]] Clearing Corporation (“[[NSCC]]”) or any other [[DTCC]] subsidiary, nor [[DO]] any 
statements contained herein set forth any legal rights of any [[NSCC]] user. All such legal rights and [[obligations]] 
are set forth in [[NSCC]]’s Rules & Procedures and each user’s Membership Agreement with [[NSCC]] (together, the 
“Legal Documents”). The user is referred to the Legal Documents for a statement of all such legal [[obligations]]. 
In general, unless the context clearly indicates otherwise, terms used in this Guide have the same meanings  as 
in the Legal Documents. 
NEITHER [[DTCC]] NOR ANY OF ITS SUBSIDIARIES [[Warrants]] THE ACCURACY OR COMPLETENESS OF 
THE INFORMATION CONTAINED IN THIS GUIDE. FURTHER, NEITHER [[DTCC]] NOR ANY OF ITS 
SUBSIDIARIES [[Warrants]] THE ACCURACY OR COMPLETENESS OF ANY OTHER WEB SITE WHICH 
THE USER MAY ACCESS THROUGH THIS GUIDE. THE INFORMATION CONTAINED IN THIS GUIDE IS 
NOT INTENDED TO BE A SUBSTITUTE FOR OBTAINING LEGAL OR TAX ADVICE FROM AN 
APPROPRIATE PROFESSIONAL ADVISOR. IN NO EVENT WILL [[DTCC]] NOR ANY OF ITS SUBSIDIARIES 
BE LIABLE FOR LOSSES OR DAMAGES, INCLUDING LOSS OF PROFITS OR CONSEQUENTIAL 
DAMAGES, ARISING OUT OF THE USE OF THIS GUIDE OR OTHER HYPERLINKED WEB SITES 
CONTAINED HEREIN. 
TO ENSURE COMPLIANCE WITH INTERNAL REVENUE SERVICE CIRCULAR 230, YOU ARE HEREBY 
NOTIFIED THAT: (A) ANY DISCUSSION OF FEDERAL TAX ISSUES CONTAINED OR REFERRED TO 
HEREIN IS NOT INTENDED OR WRITTEN TO BE USED, AND CANNOT BE USED, FOR THE PURPOSE 
OF AVOIDING PENALTIES THAT MAY BE IMPOSED UNDER THE INTERNAL REVENUE CODE; AND (B) 
AS A MATTER OF POLICY, [[DTCC]] DOES NOT PROVIDE TAX, LEGAL OR ACCOUNTING ADVICE AND 
ACCORDINGLY, YOU SHOULD CONSULT YOUR OWN TAX, LEGAL AND ACCOUNTING ADVISOR 
BEFORE ENGAGING IN ANY TRANSACTION. 
Trademarks 
Content on this Guide, including graphical and other images displayed herein, is the property of [[DTCC]] or is 
used with permission of the copyright owner. The use of the content or these images by you, or anyone else 
authorized by you, is prohibited unless specifically authorized in writing by [[DTCC]]. Any unauthorized use of 
content may violate copyright laws, trademark laws, the laws of privacy and publicity, and communications 
regulations and statues. 
All names of [[DTCC]] and its affiliates, and their products and services, referenced herein are either registered 
trademarks or servicemarks of, or trademarks or servicemarks of, [[DTCC]] or its affiliates in the U.S. or 
elsewhere. 
Other names of [[Companies]], products or services appearing in this Guide are trademarks or servicemarks of 
their owners. 

---

## Page 98

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix B: White Paper – Recommended Practices for Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts 98 
The contents of this Guide are protected by copyright law. Except as otherwise expressly indicated in this 
Guide, no permission is granted to copy, distribute, modify, post or frame any contents of this Guide.  
© 2011 The Depository Trust & Clearing Corporation  
All rights reserved. 
 


---

## Page 99

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix B: White Paper – Recommended Practices for Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts 99 
 


---

## Page 100

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix B: White Paper – Recommended Practices for Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts 100 
 


---

## Page 101

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix B: White Paper – Recommended Practices for Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts 101 
 


---

## Page 102

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix B: White Paper – Recommended Practices for Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts 102 
 


---

## Page 103

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix B: White Paper – Recommended Practices for Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts 103 
 


---

## Page 104

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix B: White Paper – Recommended Practices for Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts 104 
 


---

## Page 105

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix B: White Paper – Recommended Practices for Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts 105 
B2 Investment Company Institute Memorandum 
The following two pages contain a facsimile of the original memorandum from ICI, dated October 1, 1992.  
 


---

## Page 106

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix B: White Paper – Recommended Practices for Firm-Initiated Fund/SERV® Redemptions on Fund-Controlled Accounts 106 
 


---

## Page 107

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix C: Glossary 107 
APPENDIX C: GLOSSARY 
Term Definition 
Average Cost A calculation methodology which combines the cost of all [[shares]] within the account to 
compute an average cost per share. 
Average cost can be applied as either an affirmative election by the shareholder or as the 
reporting [[Broker]]'s [[default]] method. Regardless of how applied, an election by the shareholder 
to switch to any other reporting method is required in writing. Shareholders may revoke an 
average cost election for up to 1 year or until the time of the first redemption. Reporting 
brokers have the [[Option]] to extend the revocation period for longer than 1 year but cannot 
extend it past the date of the first redemption. A revocation of average cost will "unwind" the 
average cost election and restore the individual basis of the lots in an account. If the 
revocation period is expired, a shareholder may request a change in their basis method 
prospectively. In addition, under the current [[regulation]] shareholders utilizing the [[Broker]]'s 
[[default]] method of the average cost method can only change their basis method prospectively. 
changed. 
Prior to the mandatory cost basis reporting requirement average cost served as the [[default]] 
cost basis calculation methodology for most mutual fund [[Companies]]. 
Acquisition Date The date [[shares]] were acquired by the shareholder. In most instances, the acquisition date will 
be the same as the trade date of the purchase. However, there may be occasion when the 
purchase date is not known. When this occurs, although the acquisition date may be defaulted 
to the date on which the [[shares]] were received in the account, the actual acquisition date must 
be treated as unknown. The IRS has special depletion guidelines for [[shares]] with unknown 
acquisition dates. 
Basis or Cost Basis The original and/or adjusted cost of [[shares]] acquired by a shareholder, used for calculating a 
gain or loss when [[shares]] are redeemed. 
The original basis of mutual fund [[shares]] depends on how the [[shares]] were acquired. The 
original basis for [[shares]] that were purchased or acquired through reinvestment of a [[Dividend]] is 
generally the original cost of the [[shares]]. If the mutual fund has had distributions that were 
identified as a return of capital, then basis would be adjusted by the amount of capital that was 
returned to the shareholder. This basis would be referred to as an adjusted basis. [[shares]] 
acquired through inheritance will generally have the market value of the [[shares]] on or around 
date of death as the adjusted cost basis. [[shares]] acquired as gift will generally retain the 
adjusted cost basis of the donor. 
Bifurcated Account A cost basis accounting method that uses two pools of [[shares]] in the same account. One pool 
is for "covered" [[shares]] and one pool is for "non-covered" [[shares]]. (See "Covered" and "Non-
covered" [[shares]]) 
[[Broker]] or Reporting 
[[Broker]] 
The tax reporting responsible party. Where cost basis is concerned, the "[[Broker]]" may be the 
[[Broker]]/dealer or bank [[intermediary]] and/or the mutual fund [[transfer agent]]. 
[[Broker]]-to-[[Broker]] 
Transfer 
Transfers that occur between reporting brokers that may or may not include a change in 
beneficial ownership. Transfers require the sending ("delivering") [[Broker]] to provide basis 
information (see "Transfer Statement") to the "receiving" [[Broker]] within 15 days of the transfer. 
Transfers between reporting brokers are generally the result of the following: 
1. The shareholder holds [[shares]] directly with the fund [[transfer agent]] and instead 
decides to hold those same [[shares]] as part of a brokerage account. 
2. The shareholder holds [[shares]] as part of a brokerage account with a particular 
[[Broker]]/dealer and instead decides to move their assets to a brokerage account with 
a different [[Broker]]/dealer. This is the most common circumstance. 
3. The shareholder holds [[shares]] as part of a brokerage account and instead decides to 
hold those same [[shares]] direct with the fund [[transfer agent]]. 

---

## Page 108

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix C: Glossary 108 
Term Definition 
Carry Over Basis When [[shares]] are gifted at a value greater than their adjusted cost basis (gifted as a gain), the 
cost basis moves intact with the transferred [[shares]]. This means the donor’s basis transfers 
without adjustment (carries over) to the donee. 
Change in Method 
Period 
Pursuant to IRS Notice 2011-56, a shareholder may choose a method other than the [[Broker]]’s 
[[default]] of average cost for existing [[shares]] in an account. A shareholder must choose another 
method by the earlier of (1) one year following the notification of the reporting [[Broker]]’s [[default]] 
method, or (2) the date of first sale, transfer, or other disposition of [[shares]] subject to the 
[[Broker]] [[default]] (the “change in method” period). Brokers at their discretion may extend this 
period longer than one year, but not beyond the first redemption. If a shareholder chooses 
another method other than the [[Broker]]’s [[default]] of average cost during the “change of method” 
period, the basis in the [[shares]] in the account to which the method choice applies is the basis 
before averaging. 
Cost Basis Reporting 
System ("CBRS") 
A service offered by the Depository Trust Clearing Corporation ("[[DTCC]]")27 that provides for 
the passing of [[Asset]] and tax lot level basis information. It is the preferred method for brokers 
to furnish transfer statements. 
Covered [[shares]] [[shares]] acquired after the effective date of the legislation (January 1, 2012 for [[Mutual Funds]]) 
and for which brokers have received basis information if the [[shares]] were transferred from 
another [[Broker]]. Also, this would include all [[shares]] in the account if the "Single Account" 
average cost reporting method is being used. 
Brokers are required to report cost basis information as prescribed on Form 1099-B in 
conjunction with the sale of covered [[shares]]. 
First-in, First-out (FIFO) One of the prescribed [[default]] basis calculation methodologies for reporting brokers. When 
using FIFO, the oldest available tax lots are depleted first when calculating gain/loss amounts. 
Gifted/Inherited [[shares]] [[shares]] that have been gifted to or inherited by the shareholder. When [[shares]] are gifted, both 
the donor's basis and the "fair market value" upon the date of the gift must be transferred to 
the recipient of the gift. The [[Broker]] must maintain both numbers, as the donee's basis may 
depend on the fair market value of the [[shares]] upon a subsequent sale. Even if [[shares]] are 
gifted at a gain (the value of the [[shares]] is greater than the donor's basis), brokers must carry 
both the fair market value on the date of the gift and the donor's basis for future gain/loss 
determinations. 
The basis for inherited [[shares]] defaults to the "fair market value" of those [[shares]] on the date of 
death unless an estate representative provides alternative basis information to the reporting 
[[Broker]]. 
Highest Cost-in, First-
out (HIFO) 
A cost basis methodology that is a form of Specific [[ID]], in which [[shares]] are depleted in the 
order of highest acquisition cost to lowest acquisition cost, regardless of how long they have 
been held in the account. 
Highest Long-Term 
Cost-in, First-out (HIFO-
Long Term) 
A cost basis methodology that is a form of Specific [[ID]], in which [[shares]] are depleted in the 
order of highest acquisition cost to lowest acquisition cost, giving first priority to those [[shares]] 
held in the account for at least 1 year. 
Highest Short-Term 
Cost-in, First-out (HIFO-
Short Term) 
A cost basis methodology that is a form of specific [[ID]], in which [[shares]] are depleted in the 
order of highest acquisition cost to lowest acquisition cost, giving first priority to those [[shares]] 
held in the account for less than 1 year. 
"In-kind" Transfer to 
"Like" Registration 
Transfers that occur between reporting brokers where there is no change in the beneficial 
ownership (or "customer") of the [[shares]] moved. An in-kind transfer occurs between two 
 
27 [[DTCC]] operates its businesses through several operating subsidiaries.  

---

## Page 109

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix C: Glossary 109 
Term Definition 
reporting brokers where [[shares]] are moved from one account to another account with a "like" 
or identical registration (transfer from [[Broker]] to [[Broker]] without change in beneficial ownership). 
Load Basis Deferral The load or commission on the purchase of mutual fund [[shares]] is normally included in the 
adjusted basis of the [[shares]] purchased. Most [[Mutual Funds]] that have a front-end commission 
will allow shareholders to exchange [[shares]] into other funds that have a similar commission 
structure without paying an additional commission. The IRS refers to this right to exchange to 
another fund without paying a commission as a reinvestment right. If a shareholder purchases 
[[shares]] in a mutual fund and acquires reinvestment rights, and then exchanges into another 
fund within 90 days by exercising their reinvestment right, then the shareholder will not be 
allowed to add the commission or load to the adjusted cost basis of the [[shares]] redeemed. The 
IRS Regulations specify that the commission should be deferred and added to the cost basis 
of the [[shares]] that were acquired by the exchange. 
Lowest Cost-in, First-
out (LOFO) 
A cost basis methodology that is a form of Specific [[ID]], in which [[shares]] are depleted in the 
order of lowest acquisition cost to highest acquisition cost, regardless of how long they have 
been held in the account. 
Lowest Long-Term 
Cost-in, First-out 
(LOFO-Long Term) 
A cost basis methodology that is a form of Specific [[ID]], in which [[shares]] are depleted in the 
order of lowest acquisition cost to highest acquisition cost, giving first priority to those [[shares]] 
held in the account for at least 1 year. 
Lowest Short-Term 
Cost-in, First-out 
(LOFO-Short Term) 
A cost basis methodology that is a form of Specific [[ID]], in which [[shares]] are depleted in the 
order of lowest acquisition cost to highest acquisition cost, giving first priority to those [[shares]] 
held in the account for less than 1 year. 
Mutual Fund Agent The mutual fund agent or “MF Agent" is represented as the firm on the National [[securities]] 
Clearing Corporation ("[[NSCC]]") order that is the party acting on behalf of an underlying or 
introducing firm. 
Non-covered [[shares]] Non-covered [[shares]] are any [[shares]] that are not "covered" [[shares]], as defined by IRS cost 
basis reporting regulations. Non-covered [[shares]] include those acquired prior to the effective 
date of cost basis rules. Brokers are required to send transfer reporting statements for non-
covered [[shares]] that otherwise are subject to 1099-B reporting. Brokers are only required to 
report "Gross Proceeds" on Form 1099-B in conjunction with the sale of non-covered [[shares]]. 
Return of Capital A distribution received by a shareholder that the mutual fund has concluded is not income, but 
instead is a return of a shareholder's capital investment. A return of capital differs from a sale 
in that the shareholder does not initiate the distribution. A return of capital occurs when a 
mutual fund determines, for any number of reasons, that distributions made to shareholders 
throughout the year have exceeded the earnings and profits of the mutual fund for that year. 
The shareholder's cost basis increases for all [[shares]] held as of the record date of the 
distribution characterized as a Return of Capital. 
Revocation Period The period in which a shareholder that has affirmatively elected the average cost method may 
revoke their election. The regulations state that the shareholder has either 12 months or until 
the first disposition of [[shares]] in which to revoke their average cost election. The regulations [[DO]] 
allow reporting brokers to extend the revocation period for any length of time but, in no 
circumstance, can they extend it past the point in which the first disposition of [[shares]] occurs. If 
a shareholder revokes their average cost election during the period, the basis of [[Stock]] to 
which the revocation applies is its basis before averaging. 
Single Account 
Average Cost ("SAAC") 
The regulations provide that a single-account election only applies to accounts with the same 
ownership. A [[Broker]] may elect to treat all [[shares]] in an account as covered in computing the 
average cost basis, regardless of when the [[shares]] were acquired. The [[Broker]] may only elect 
to use the single account average cost basis method when: 
1. The shareholder has affirmatively elected in writing to use the average cost basis 
reporting method. 

---

## Page 110

Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
Appendix C: Glossary 110 
Term Definition 
2. The [[Broker]] does not know or have reason to know that the basis information it has 
for the account (for both covered and non-covered [[shares]]) is inaccurate. 
3. The [[Broker]] knows that the shareholder has NOT averaged the cost of [[shares]] within 
the account with the cost of [[shares]] held in the same fund in another account. 
Once a single account election has been made by the [[Broker]], all [[shares]] in the account 
become "covered" [[shares]]. Once SAAC is implemented, it is irrevocable by the [[Broker]], but the 
shareholder may revoke their affirmative Average Cost election during the revocation period 
(see "Revocation Period"), which will unwind the SAAC election. Thus, brokers must retain 
individual lot information for [[shares]] in an account for which the single account election is made 
until the revocation period for that account has ended. [[shares]] that become covered [[shares]] 
only as a result of a single account election are no longer covered [[shares]] after the single 
account election is voided due to a revocation. 
Specific Lot 
Identification or 
Specific [[ID]] 
Specific lot identification is a cost basis reporting method, where the shareholder or their agent 
(if permissible) identifies the [[shares]] that will be disposed of for cost basis reporting purposes. 
When selling [[shares]], the shareholder individually identifies a specific acquisition lot of [[shares]] 
in which to redeem. The basis used for gain/loss reporting is calculated by summing the 
adjusted cost basis of the lots specifically identified by the shareholder. 
Specific [[ID]] may also include the application of certain formulaic methods for identifying lots 
including: 
• Highest Cost, First Out 
• Lowest Cost, First Out 
• Highest Cost Long-Term, First Out 
• Lowest Cost Long-Term, First Out 
• Highest Cost Short-Term, First Out 
• Lowest Cost Short-Term, First Out 
Stepped Up Basis When [[shares]] are inherited, and the fair market value on date of death exceeds the adjusted 
cost basis of those [[shares]], the cost basis of the transferred [[shares]] is adjusted ("stepped-up") 
to reflect the higher market value of the [[Asset]] as of the date of death. This reduces the 
potential gain an heir may realize on the future sale of [[shares]]. 
Transfer Statement Reporting brokers are required to provide a "Transfer Statement" upon the movement of 
[[shares]] from one [[Broker]] to another. The transfer statement must be provided by the delivering 
[[Broker]] within 15 days of the transfer and, if not delivered, the receiving [[Broker]] is compelled to 
make 1 follow up inquiry as to its receipt. 
Information required on the transfer statement includes: 
• The date the statement is furnished, 
• Name, address and telephone number of person furnishing the statement and [[Broker]] 
receiving [[custody]] of the security, 
• Name and account number of customer(s) (both transferring and receiving), 
• Security number of the security transferred, 
• Date transfer was initiated and [[settlement]] date of transfer (if known), 
• Total adjusted basis of the security, original acquisition date, and, if applicable, any holding 
period adjustment required due to a wash sale. 
Allowance is made in the regulations to allow brokers to agree to combine this information in 
any format or to use a code in place of one or more required items (e.g. use of [[NSCC]] Client 
Numbers). 
Wash Sales If mutual fund [[shares]] are sold at a loss and within 30 days before or after that sale a 
subsequent purchase of substantially identical [[shares]] is made, then a wash sale is deemed to 
have occurred. Shareholders are not permitted to deduct losses as a result of a wash sale. 
 
 

---

## Page 111

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: January 19, 2024 
Publication Code: MFS357 
Service: Mutual Fund Services 
Title: Cost Basis Reporting Service (CBRS)-Supplemental User Guide for [[Mutual Funds]] 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 