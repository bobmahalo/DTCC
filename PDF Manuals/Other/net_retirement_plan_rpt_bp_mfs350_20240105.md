---
title: "Retirement Plan Reporting User Guide/Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_retirement_plan_rpt_bp_mfs350_20240105.pdf"
pages: 15
size: "333.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Retirement Plan Reporting User Guide/Best Practices

**Original File:** [net_retirement_plan_rpt_bp_mfs350_20240105.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_retirement_plan_rpt_bp_mfs350_20240105.pdf)  
**Category:** Other  
**Total Pages:** 15  
**File Size:** 333.1 KB  

---

## Page 1

 
 
  
Networking      
RETIREMENT PLAN REPORTING USER 
GUIDE/BEST PRACTICES 
JANUARY 5, 2024 
 

---

## Page 2

Retirement Plan Reporting User Guide/Best practices 
Change History 2 
CHANGE HISTORY 
01/05/2024 Document rebranded. Content reviewed.  
04/07/2022 Learning upgrade caused some link(s) to break.  Links have been corrected.  
04/21/2021 Document rebranded.  Content reviewed. 
01/08/2021 Updated Saturday cutoff processing time to 2:00pm (p.14) to align with revised processing 
schedule (Important Notice a8905) 
07/14/2020 Corrected broken links and modified transmission time cut off times. 
03/25/2020 Updated “DoL [[Fiduciary]] Rule” section - updated rule’s applicability date and references to 
the rule. 
  05/15/2017 Updated “DoL [[Fiduciary]] Rule” section - updated rule’s applicability date. 
2/27/2017 See Important Notice a8286 p&s 7861 Dated January 3, 2017 – added “DoL [[Fiduciary]] Rule” 
section 
3/18/2013 See Important Notices 
a7471 p&s7041 Dated August 16, 2012 and 
a7576 p&s 7146 Dated January 30, 2013 
 
  

---

## Page 3

Retirement Plan Reporting User Guide/Best practices 
Change History 3 
TABLE OF CONTENTS 
Change History ..................................................................................................................................................... 2 
Overview ............................................................................................................................................................... 4 
Background ......................................................................................................................................................... 4 
Project Goals ..................................................................................................... Error! Bookmark not defined. 
Client Benefits ..................................................................................................................................................... 5 
Definitions ............................................................................................................................................................. 6 
Best Practices ....................................................................................................................................................... 7 
File from Record Keeper/Retirement Platform to [[Broker]]/Dealer ........................................................................ 7 
Record Keeper Start & End Dates .................................................................................................................... 7 
Plan Status ........................................................................................................................................................ 7 
Branch [[ID]], Rep [[ID]] and Rep Name fields .......................................................................................................... 8 
Product Investment Type .................................................................................................................................. 8 
Record Keeper Name ........................................................................................................................................ 8 
Program Name .................................................................................................................................................. 8 
Product Provider ................................................................................................................................................ 8 
Distribution Amount ........................................................................................................................................... 8 
Email Addresses of Plan Sponsor and Plan [[Fiduciary]] ...................................................................................... 9 
DOL [[Fiduciary]] RULE – ENHANCEMENTS AND BEST PRACTICES .......................................................... 10 
Background .......................................................................................................................................................10 
Enhancements and Best Practices ...................................................................................................................10 
Best Practice: ....................................................................................................................................................11 
[[NSCC]] ................................................................................................................................................................... 12 
Getting Started ................................................................................................................................................... 13 
[[NSCC]] Membership Types...............................................................................................................................13 
DataTrak and Autoroute IDs .............................................................................................................................13 
Record Layouts .................................................................................................................................................14 
File Schedule ....................................................................................................................................................14 
Underlying Firm Symbol (UFS) .........................................................................................................................14 

---

## Page 4

Retirement Plan Reporting User Guide/Best practices 
Overview 4 
OVERVIEW 
Background 
As the market of [[participant]]-directed defined contribution plans has expanded, the need for  efficient information 
exchange between the various industry participants continues to increase. To date, this information exchange 
has been accomplished through mostly manual alternatives and varying formats where data is gathered 
through custom file extracts or spreadsheets and delivered through email, file transfer or other methods that 
can be cumbersome or provide less sophisticated data security. As the market grows and the number of 
business partners expands, this manual, non-standardized environment becomes increasingly costly to 
sustain, ultimately becoming inefficient and inflexible to meet ever-changing industry [[participant]] needs. 
The retirement industry has identified the need for a centralized and standardized method  of secure data 
communication to enable better transparency and solve compliance gaps that exist today. This need for 
information initiated the formation of the Retirement Industry Information Sharing (RIIS) working group 
organized in conjunction with the Investment Company Institute’s Bank, Trust and Retirement Advisory 
Committee and [[Broker]]/Dealer Advisory Committee. The working group is comprised of firms, funds, trusts and 
record keepers that are sharing information using many different methods today and a desire to  streamline and 
improve the efficiency, automation, and security of the data exchange. 
There are multiple stakeholders that represent the retirement industry such as plan sponsors, record keepers, 
[[Broker]]/dealer plan advisors, clearing agents, investment managers and transfer agents. Relationships between 
these groups can be multi-layered which creates fractured transparency between intermediaries. Fee payment, 
plan level information and compensation reporting are a few examples of areas where communication  needs to 
be improved. 
Data needs vary between each of these stakeholders. The following highlights some considerations for each of 
the key market participants as they view the need for retirement information sharing. 
 
Record Keepers 
There is a growing need for record keepers to receive data for various disclosure requirements through a more 
efficient method of communication. The information may be more static and investment specific or may relate 
to actual fee activity. [[NSCC]] has enhanced the Mutual Fund Profile Security database to obtain Department of 
Labor Rule 408(b)(2) data elements directly from source documents. Some of the information is currently 
available in public sources while other data elements can only be acquired by direct interaction with the source 
organization. 
As a data provider, record keepers are often requested to provide a number of customized data files and 
spreadsheets, delivered in a variety of ways, to [[Broker]]/dealers and funds that are requesting information on 
plans the record keeper administers. Record keepers would greatly benefit from the standardization afforded 
through adoption of an industry standard for information sharing. 
 
[[Broker]]/Dealers 
[[Broker]]/dealers need specific, plan-level information for 408(b)(2) pension disclosure. Typically this is 
necessary to ensure that appropriate regulatory supervision of plan business can be conducted, to accurately 
allocate compensation among their representatives, and to ensure different types of retirement plan 
businesses are supported in alignment with brokers’ requirements. Many brokers have created one-off 
reporting structures to gather data from business partners if possible. The reporting is not  standardized in form 
or delivery, and there are varying degrees of success in acquiring the information. Like all customized 
processes, any requests to change the data received must be separately coordinated with each delivering 
party, and adoption typically occurs over a period of time. This creates difficulties for the [[Broker]]/dealer to 
manage and receive benefit from the change. 
 
 

---

## Page 5

Retirement Plan Reporting User Guide/Best practices 
Overview 5 
[[Mutual Funds]] 
Standardization and compliance are two of the primary information drivers. Funds or their service providers 
currently produce one-off reports to provide dealers with transparency into their retirement plan business. 
Since 408(b)(2), the number of requests including variations of data record layouts have increased. Funds also 
want transparency in a standardized format from retirement plan platforms, especially those operating in a 
super-omnibus environment, to better ensure fulfillment of contractual requirements.  In addition, plan level 
disclosure can assist funds with their corporate reporting needs for an already large and growing distribution 
support channel. 
Client Benefits 
• The development of centralized files to standardize information communicated between multiple 
[[intermediary]] relationships would eliminate the need for various point to point connections between parties. 
• Establishes more conclusive method of communicating information, thereby providing better transparency 
for 5500 Schedule C and 408(b)(2) compliance requirements. Information on 5500 Sche dule C and 
408(b)(2) compliance requirements can be found at the Department of Labor website http://www.dol.gov/  
• Reduces need for call outs, faxes and email communications. 
• Intermediaries that [[DO]] not have an established connection to [[NSCC]] may become participating members. 
Many record keepers trade through various trading platform providers and will likely transmit information 
through those providers since the platforms perform account opening, trading and revenue share 
collection via [[NSCC]] on behalf of the record keepers. 
o Platform providers already have some of the Retirement Plan Reporting file data elements on their 
system and can facilitate limited data sharing. However, other information will need to be computed 
or derived from the record keeper’s system. 

---

## Page 6

Retirement Plan Reporting User Guide/Best practices 
Definitions 6 
DEFINITIONS 
Term Definition 
Record Keeper Start Date The effective date of the record keeping service agreement with the Plan (date 
the plan is officially live on the record keeping system). 
Record Keeper End Date The date the plan intends to deconvert from the record keeping system (service-
termination date). 
Dealer Maintenance Date The date a modification took place on the record keeping system. 
Rep Maintenance Date The date a modification took place on the record keeping system. 
Branch [[ID]] The branch number of the financial advisor. 
Rep [[ID]] The financial advisor affiliated with the plan. 
Plan [[Fiduciary]] Name The name of the [[Fiduciary]]/trustee of the plan to which [[Broker]]/dealers send their 
408(b)(2) disclosure information. 
 

---

## Page 7

Retirement Plan Reporting User Guide/Best practices 
Best Practices 7 
BEST PRACTICES 
File from Record Keeper/Retirement Platform to [[Broker]]/Dealer 
The file is intended to be a monthly file; however, record keepers and firms can agree to a transmission 
schedule and receipt that differs from a monthly schedule. 
For the purpose of this document, a monthly file is assumed to be generated. 
• Firms should contact the record keeper or retirement platform to discuss their intent to utilize the 
Retirement Plan Reporting files. 
• Firms and record keepers or retirement platform should agree upon their preferred transmissio n schedule 
(daily, weekly, monthly, etc.). 
• On a monthly basis (or a schedule timeframe agreed upon) the record keeper platform will generate the 
file and transmit it to [[NSCC]] for delivery to the [[Broker]]/dealer. 
 
Record Keeper Start & End Dates 
Record Keeper Start Date field 
In order to level-set a plan’s parameters, record keepers will provide the Record Keeper Start date (see 
definitions) the first time they transmit the Retirement Plan Reporting files to a [[Broker]]/dealer. If changes occur 
to the Record Keeper Start Date, record keepers will send the new date in their regular monthly file.  
Record Keeper End Date field 
If a plan will no longer be serviced by a record keeper, the Record Keeper End Date field should be populated 
with the expiration date of the plan (date the plan will deconvert from their system). If this information changes 
or needs to be modified, the record keeper will send the new date in their regular monthly file.  
If a record keeper is sending the Retirement Plan files for the first time but will no longer be servicing a plan, 
they should provide both the Record Keeper Start and End Dates. 
Plan Status 
Record keepers are required to provide the status of a plan in their monthly file. 
Active 
If a plan is active, enter a value of “A” (Active) in the Plan Status field. 
 
Abandoned 
A plan generally will be considered abandoned if no contributions to or distributions from the plan have been 
made for a period of at least 12 consecutive months, and following reasonable efforts to [[Locate]] the plan 
sponsor, it is determined that the sponsor no longer exists, cannot be located or is unable to maintain the plan. 
This is often the case in the event of the plan sponsor’s bankruptcy, and prior to any assignment of a Qualified 
Termination Administrator (QTA). 
If a plan is abandoned, the record keeper will enter a value of “B” (Abandoned) in the Plan Status field as well 
as enter the date of abandonment in the Plan Status Date field.  
 
 

---

## Page 8

Retirement Plan Reporting User Guide/Best practices 
Best Practices 8 
Service Termination 
The plan has assets, but the record keeper is no longer servicing. If a plan is deactivated from a record 
keeper’s system, but it is still an active plan, the record keeper will enter a value of “A” (Active) in the Plan 
Status field and will also designate the Record Keeper End Date. [[DO]] NOT enter a date in Plan Status Date 
field. (See Record Keeper End Date practices above for guidance on the Record Keeper End Date field.)  
Plan Termination 
Plans which are abandoned, or which are going through a controlled bankruptcy proceeding, can be terminated 
either through the bankruptcy process, or through following Department of Labor (DOL) abandoned plan 
procedures. If a plan is deemed terminated, the record keeper will enter a value of “T” in the Plan Status Date 
field as well as the date of termination in the Plan Status Date field. 
Branch [[ID]], Rep [[ID]] and Rep Name fields 
First Transmission: 
Record keepers will provide the Branch [[ID]], Rep [[ID]] and name of representative the first time they transmit the 
Retirement Plan Reporting files to a [[Broker]]/dealer. 
Modification: 
If changes occur to any of these fields, record keepers will enter the date of modification in the Dealer Maint 
Date or Rep Maint Date field in their regular monthly file. 
Product Investment Type 
A value of 99 ‘Other’ has been listed for flexibility in the event the Product Investment Type is a value other 
than the values provided. 
When a value of 99 is used – the “Define Product Investment Type” field is required. It is a free form field for 
the submitter to supply a Product Investment Type. Additionally, the submitter should notify [[NSCC]] that this 
investment type should be added to the Product Investment Type field. This can be accomplished by 
submitting a [[NSCC]] Enhancement Request form. 
Record Keeper Name 
Record Keeper name is the full name of the Record Keeper. No punctuations or abbreviations should be 
included. 
Program Name 
Program name is the name created by the Product Provider. N/A is a valid entry.  
Product Provider 
Product Provider is the entity that created the Program. N/A is a valid entry.  
The Program is the product and service arrangements between the [[Broker]]/dealer, retirement plan record 
keeper and the mutual fund. 
Distribution Amount 
Distribution Amount for the Plan is the net amount of all distributions at the plan level. This should not include 
transferred or exchanged assets. Zeros are allowed. 

---

## Page 9

Retirement Plan Reporting User Guide/Best practices 
Best Practices 9 
Email Addresses of Plan Sponsor and Plan [[Fiduciary]] 
If available, the Record Keeper should provide this information. 
  

---

## Page 10

Retirement Plan Reporting User Guide/Best practices 
DOL [[Fiduciary]] RULE – ENHANCEMENTS AND BEST PRACTICES 10 
DOL [[Fiduciary]] RULE – ENHANCEMENTS AND BEST 
PRACTICES 
Background 
On April 6, 2016, the Department of Labor (DoL) issued a [[regulation]] defining who is a “[[Fiduciary]]” of an 
employee benefit plan under the Employee Retirement Income Security Act of 1974 (ERISA) as a result of 
giving investment advice to an employee benefit plan, plan [[Fiduciary]], plan [[participant]] or beneficiary, individual 
retirement account (IRA), or IRA owner. The rule defined persons who provide investment advice or 
recommendations for a fee or other compensation with respect to assets of a plan or IRA as fiduciaries in a 
wider array of advice relationships. 
[[NSCC]] in conjunction with the DoL [[NSCC]] Enhancements Working Group of the Investment Company Institute’s 
(ICI) [[Broker]]/Dealer Advisory Committee and Bank, Trust and Retirement Advisory Committee (respectiv ely; the 
“Working Group”) defined enhancements to the [[Mutual Funds]] Services necessary for our clients to comply with 
the DoL rule. To see a complete list of enhancements, please refer to Important Notice a8286 . All DoL-related 
best practices provided in this document have been identified and approved by the working group in advance 
of the rule’s applicability date. 
Note: 
The original applicability date of April 10, 2017 was delayed by DoL. On March 15, 2018, The Fifth Circuit Court of Appeals, 
based in New Orleans, vacated the [[Fiduciary]] rule. On June 21, 2018, The Fifth Circuit Court of Appeals confirmed its 
decision to vacate the ruling as such all references to requirements under the rule have been removed within this section. 
Enhancements and Best Practices 
In order to provide additional transparency into retirement plan’s activity and position, the following fields were 
added to [[DTCC]] Retirement Plan Reporting (RPR) record layouts: 
• Optional “Contribution Amount Credit/Debit Indicator” field (Header Record) 
o Blank = Credit 
o D = Debit 
This enhancement allows clients to specify if the Contribution Amount is positive (credit) or negative (debit). 
Blank is a [[default]] value for transactions where Contribution Amount is positive. Firms will use this field in 
combination with the “Contribution Amount” field to determine assets gathered into the plan during the 
reporting period provided in the RPR file. 
• Optional “Distribution Amount Credit/Debit Indicator” field (Header Record) 
o Blank = Debit 
o C = Credit 
This enhancement allows clients to specify if the Distribution Amount is positive (debit) or negative (credit). 
Blank is a [[default]] value for transactions where Distribution Amount is positive. Firms will use this field in 
combination with the “Distribution Amount” field to determine assets distributed from the plan during the 
reporting period provided in the RPR file. 
• Required “Price” field (Detail Record) 
 
This field will be used to provide the price for each Security Issue [[ID]] in a plan. This field allow s for 
communication of prices for registered and unregistered Security Issue IDs. 
Zero prices are not allowed. 

---

## Page 11

Retirement Plan Reporting User Guide/Best practices 
DOL [[Fiduciary]] RULE – ENHANCEMENTS AND BEST PRACTICES 11 
Best Practice: 
This field should contain the price for the “Security Issue [[ID]]” (Detail Record 48 pos 6- 14) and reference the 
price that was used to calculate “Month End Assets for Security Issue [[ID]]” field value (Detail Record 48, position 
90-105). The value provided in this field should also reflect the price calculated on the last day of the reported 
period (“End date for Period” field – Header record 47, sequence 1 pos 56-63). 
  

---

## Page 12

Retirement Plan Reporting User Guide/Best practices 
[[NSCC]] 12 
[[NSCC]] 
[[NSCC]] will review the Retirement Plan Reporting files to validate that all data in applicable fields meets [[NSCC]] 
record layout requirements. 
[[NSCC]] will reject an entire file back to submitter if the either header or trailer records  [[DO]] not meet requirements 
(incorrect or incomplete information). 
Security Issue [[ID]] Specific Information detail records 
• If [[NSCC]] determines specific detail records contain errors, those specific records will be rejected back to 
submitter with reject code(s) to assist in identifying the reason for the reject. The remaining detail records 
that pass [[NSCC]] validation will be sent to the recipient. The trailer will be updated to show the correct 
number of expected records. 
 
All Retirement Plan Reporting files sent to [[NSCC]] after the last transmission deadline must be received by 
[[NSCC]] the same day by 9:00pm ET (Mon-Fri) for processing the next business day. Files received after 9:00pm 
ET will reject unless the Datatrak file header contains the next business day’s date, in which case accepted 
files will be processed during the first cycle of the next business day. Files received after 9PM ET with current 
date will reject. 
The cut off time for [[NSCC]] to receive Retirement Plan Reporting files with current date for Saturday processing 
is 2:00pm. 
  

---

## Page 13

Retirement Plan Reporting User Guide/Best practices 
Getting Started 13 
GETTING STARTED 
In order to participate in the Retirement Plan Reporting files, all current members are required to sign up for 
activation to this service. Contact the Wealth Management Services team at 212- 855-8877 to get started. 
If you wish to participate in Retirement Plan Reporting service; but are not a current [[NSCC]] [[Member]], please 
contact Wealth Management Services at 212-855-8877. 
[[NSCC]] Membership Types 
Intermediaries not currently connected to [[NSCC]] may partake in the Retirement Plan Reporting files by 
establishing one of the following [[NSCC]] membership types: 
Membership Type Description 
[[Broker]]/Dealer Membership [[Broker]]/Dealer Membership is available for any [[Broker]]/dealer that meets 
[[NSCC]] requirements and is registered under the [[securities]] Exchange Act of 
1934. 
Bank or Trust Company Membership 
 
Bank or Trust Company Membership is available to any bank or trust 
company that meets [[NSCC]] requirements. 
Insurance Company Membership 
 
Insurance Company Membership is available for any insurance company 
that meets [[NSCC]] requirements and would like to utilize Mutual Fund 
Services products. 
TPA Membership 
 
TPA Membership is available for any organization or entity that acts as a 
third-party administrator on behalf of a defined contribution plan. 
Data Services Only (DSO) Membership 
 
Data Services Only Membership is designed for those firms that want to 
access mutual fund information without money [[settlement]] capabilities. To 
acquire a DSO membership number, please reference contact Wealth 
Management Services at 212-855-8877. 
 
DataTrak and Autoroute IDs 
In order to send and receive Retirement Plan Reporting files, members will need to sign up for the Datatrak and 
Autoroute IDs: 
Production 
• Datatrak [[ID]] - 26590 
• Autoroute [[ID]] – 02101322 
 
[[participant]] Services Environment (Testing) 
• Datatrak [[ID]] – 46590 
• Autoroute [[ID]] – 02981322 

---

## Page 14

Retirement Plan Reporting User Guide/Best practices 
Getting Started 14 
Record Layouts 
For detailed information regarding the Retirement Plan Reporting Files, please review the record layouts at 
[[DTCC]]’s Learning Center under Networking Guides at: https://dtcclearning.com/products-and-services/mutual-
fund-services/record-layouts.html 
File Schedule 
For schedule information for the Retirement Plan Reporting files, please see the Networking transmission 
schedule at the link below. Schedules for Retirement Plan Reporting files are in the Networking & Omni/SERV 
document: https://dtcclearning.com/products-and-services/mutual-fund-services/schedules.html 
Underlying Firm Symbol (UFS) 
Underlying Firm Symbols were created to identify underlying banks, trusts, TPAs, plan sponsors, insurance 
[[Companies]] and consultants who are not [[NSCC]] members but clear through an [[NSCC]] [[Member]]. To access the 
UFS List, please access the link on Learning Center : https://dtcclearning.com/products-and-services/mutual-
fund-services/mfs-cross-products/underlying-firm-symbols-ufs.html 
Workflow 
 
Plan Sponsor 
 Plan Sponsor 
[[Broker]]/Dealer 
Record Keeper (Not a 
[[NSCC]] [[participant]]) will 
send to Clearing Firm 
for transit to [[NSCC]]. 
Record Keeper – 
direct [[NSCC]] 
[[participant]]. 
[[NSCC]] 
Clearing Firm/Record 
Keeping Platform - 
[[NSCC]] 

---

## Page 15

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: January 5, 2024  
Publication Code: MFS350 
Service: Networking 
Title: Retirement Plan Reporting User Guide/Best Practices 
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 
  